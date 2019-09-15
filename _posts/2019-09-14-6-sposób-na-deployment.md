---
layout: post
title: 6 sposobów na deployment (teoria + praktyka)
date: 2019-09-14 22:00:00 +0000
header-img: "/images/content/pablo (5).jpg"

---
Niezależnie od technologii używanej w projekcie, raz na jakiś czas trzeba wdrożyć kod na produkcję. Sposobów na wdrożenie go jest N, gdzie N dąży do nieskończoności 😉. Tak jak każda firma ma w dzisiejszych czasach swój “scrum” albo “agile”, tak i ma swój sposób na instalacje. Jednym z moich ulubionych jest “sposób na PM’a”. Wygląda on następująco: PM tworzy task, a opsy go realizują...

Podchodząc do sprawy na poważnie, można N znacząco zredukować. Moim zdaniem do 6 i wszystkie 6 strategii opisałem poniżej.

## Autoreklama

Nim przejdziemy do teorii, chciałbym zaprosić Cię na drugą cześć LIVE Wieczoru z Kubernetes, który odbędzie się w najbliższy wtorek o godzinie 20:00. Więcej informacji na [Facebook ](https://www.facebook.com/events/381253005877591/)i [YouTube](http://poznajkubernetes.pl/live2).

**Jest też nowa strona przedsprzedaży kursu "Poznaj Kubernetes", szczególnie polecam** [**sekcję "Dla Kogo"**](https://poznajkubernetes.pl)**.**

## Okienko serwisowe

W przypadku systemu z dużym oknem serwisowym (bardziej znanym pod angielską nazwą _maintenance window_) problem rozwiązuje się sam. Dla niektórych firm to zamierzchła przeszłość, ale wiele systemów poważnych instytucji wciąż wykorzystuje okna serwisowe. Szczególnie dwie noce w roku mają podwyższone prawdopodobieństwo wystąpienia “tego zjawiska”. Najbliższa odbędzie się w ostatni weekend października, w związku ze zmianą czasu. Dlaczego tak się dzieje?  
Wyobraźmy sobie sytuację, w której o 2:31 w nocy zostanie wysłany przelew. Cofniemy zegarki z 3:00 na 2:00 i odeślemy go o 2:15. Żeby uniknąć tego typu problemu, banki stosują “przerwę techniczną” .  
Każdy też kiedyś słyszał o pociągu, który stał w szczerym polu w związku ze zmianą czasu. Prawda? Urban legend? Nie wiem, ale wydaje się to całkiem prawdopodobne.

Cóż to ma wspólnego z wdrażaniem oprogramowania? Możliwość skorzystania z okna serwisowego jest idealna do wdrożenia. System nie działa, nie ma użytkowników i nie ma zmian zagrażających przeprowadzanej procedurze instalacyjnej.  
Całość procesu można sprowadzić do poniższego “algorytmu”:

1. Czekamy, aż przeprocesują się kolejki
2. Czekamy, aż skończą działać zadania batch typu EOD (czyli End Of Day)
3. Dokonujemy backupu
4. Instalujemy nową wersję oprogramowania - nowy kod, migracje baz, nowe certyfikaty, nowe usługi, ...
5. Testujemy czy wszystko działa
6. Udostępniamy wersję użytkownikom, chyba że punkt 5 nie zakończył się sukcesem.

To rozwiązanie przyjemne z punktu widzenia deweloperów i administratorów jest w dzisiejszych czasach coraz gorzej widziane, gdyż cierpi na nim użytkownik aplikacji oraz "image” firmy 😉

## Recreate

Jeżeli nie ma możliwości skorzystania z okna serwisowego, musimy zastosować inne metody. Najbliższa opisanemu powyżej rozwiązaniu w Kubernetes jest metoda wdrażania typu _recreate_.  
Na proces składają się następujące etapy: najpierw "ubijamy" wszystkie instancje naszej aplikacji, potem uruchamiamy nową wersję. Jaka jest różnica pomiędzy _recreate_ a oknem serwisowym? W procesie bierze udział tylko aplikacja. Cała infrastruktura (np.: baza danych), którą mogliśmy włączyć/wyłączyć podczas okna serwisowego musimy mieć przygotowaną wcześniej.  
Ten sposób wdrożenia oszczędza nam sporo problemów, takich jak dwie równolegle działające wersje API, czy obsługa "starego" i "nowego" schematu bazy danych, szczególnie przy ORM.  
Opisany powyżej sposób instalacji jest wbudowany w K8s. Żeby z niego skorzystać, tworzymy plik YAML deployment zawierający:

    spec:replicas: 5 # "potrzebujemy" 5 replik serwisu
    strategy:type: Recreate # wymuszenie strategi recreate

Zalety:

* Całe środowisko jest tworzone od nowa.
* Nie ma problemu z migracją bazy danych - schemat bazy jest zgodny z wersją zaszytą w aplikacji, o ile migracje zaszyte są w kodzie.
* API klienckie jest spójne, gdyż mamy tylko jedną wersję.

Wady:

* Przestój (_downtime_) - czyli czas, w którym nasza aplikacja jest niedostępna.

## Blue green

O sposobie wdrażania kodu typu _blue-green_ usłyszałem bardzo dawno temu, w mojej pierwszej pracy. Sprowadza się on do posiadania dwukrotnie większej liczby serwerów niż nam potrzeba do prawidłowego działania aplikacji. Przynajmniej podczas wdrożenia. Nasze serwery dzielimy na dwie takie same grupy, jedną nazywamy _blue_,a drugą _green_. Przed nimi stawiamy element rozdzielający ruch (_router_) albo na jedną albo na druga grupę. W klasycznej architekturze trójwarstwowej można to zobrazować w ten sposób:  
![](https://lh5.googleusercontent.com/NJSFQMsEDBV4Nen8mwc_044Y5wHteRV0yDghVw0glJq7KICg3dRx-5tvOJADEjyxqOrzaMdwVR6UxR78CEXVO2n8fiVI4aqMfdCM5OgESXVugIA1InkvDI9nD0VZqyBvobM0dXNp =602x288)

Kiedy pierwszy raz przeczytałem o tym sposobie od razu nasunęło mi się pytanie: ale jak to, baza danych osobno? Jak widać na powyższym diagramie, pełny schemat _blue-green_ zakłada, że serwery _blue_ i serwery _green_ mają także osobne bazy danych. Tak zostało to przedstawione przez Martina Fowlera. W rzeczywistości rzadko spotykamy system, który może działać w ten sposób. Dlatego przeważnie _blue-green_ dotyczy tylko części aplikacyjnej.

Na schemacie mamy pokazaną sytuację w której wersja v1.0.0.0 jest wgrana na serwery _green_. Z niej korzystają użytkownicy, dzięki przekierowaniu całego ruchu przez _router_ (czyli sprzętowy bądź _softwareowy load-balancer_). Wersję v2.0.0 wgrywamy na serwery _blue_, rozgrzewamy, testujemy, itp. Gdy wszystko jest gotowe przełączamy wajchę na _router_ i kierujemy cały ruch na _blue_. A co robimy z serwerami _green_? Czekają sobie spokojnie, na kolejny _deployment_, w razie problemów umożliwiając szybki _rollback_. W wersji "taniej" po chwili możemy usunąć elementy _green_, ale wtedy tracimy możliwość _rollback_.

W Kubernetes, żeby uzyskać taki sposób wdrożenia, musimy stworzyć serwis, który równocześnie wybiera aplikację. Na przykład:

    apiVersion: v1  
    kind: Service  
    metadata:  
    name: my-app  
    labels:  
    app: my-app  
    spec:  
    type: NodePort  
    ports:
    - name: http  
      port: 8080  
      targetPort: 8080
    # Poniższe 3 linie "łapią" aplikację my-app z wersją v1.0.0
    # Po wykonaniu deployment z wersją v2.0.0 dokonujemy
    # aktualizacji wersji do v2.0.0
    selector:  
      app: my-app
      version: v1.0.0

Zalety:

* Bardzo szybki _rollout/rollback_ - wystarczy przełączyć wersję za pomocą _router_
* Nie mamy problemów z wersjonowaniem API ponieważ zmieniamy na "raz" cały klaster
* Możemy sprawdzić wersję v2.0.0 nim wpuścimy w nią użytkowników - wystarczy dodatkowy dostęp.

Wady:

* Jest "drogo" - potrzebujemy dwukrotnie więcej "zasobów" do wdrożeniu
* Może być "bardzo drogo” - jeżeli nie usuwamy "zasobów" po wdrożeniu, to przez cały czas mamy ich dwukrotnie więcej.
* Instalacja aplikacji typu _stateful_ może być niemożliwa ponieważ tracimy "stan" podczas instalacji, przenosząc aplikacje na inne "maszyny"

## Przerwa na ...

Jak na razie mamy za sobą sposoby, proste i przyjazne deweloperom. Jeżeli tematyka Cię zaciekawiła to zapraszam Cię na [**https://poznajkubernetes.pl**](https://poznajkubernetes.pl "https://poznajkubernetes.pl"). Podczas kursu będziesz miał okazję wypróbować powyższe i poniższe sposoby deployment :)

Teraz zajmiemy się bardziej delikatnymi rozwiązaniami, które wymagają pracy szarych komórek, żeby zainstalować je bez wpadki.

## Ramped

Po polsku słowo _ramped_ możemy przetłumaczyć jako wjazd i to słowo całkiem dobrze oddaje sens tej strategii. W Kubernetes funkcjonuje ona pod pojęciem rolling update, które moim zdaniem lepiej oddaje sens tej strategii. Idea polega na powolnym wdrażaniu nowej wersji aplikacji, zamieniając pojedynczo poszczególne instancje. Sposób postępowania jest następujący:

1. Mamy pulę aplikacji w wersji v1.0.0 udostępnionej przez load balancer sprzętowy lub softwareowy.
2. Dodajemy jedną instancję aplikacji w wersji v2.0.0.
3. Rozgrzewamy ją (m.in. sprawdzamy połączenie do bazy, inicjalizujemy DI, itd.)
4. Kiedy instancja jest gotowa do przyjmowania ruchu dodajemy ją do puli load balancer.
5. W tym momencie mamy jedną nową instancję v2.0.0 oraz kilka instancji v1.0.0
6. Usuwamy jedną instancję v1.0.0 z load balancer i wyłączamy ją.
7. Powtarzamy powyższy proces, aż wszystkie instancje będą w wersji v2.0.0

W Kubernetes jest to domyślny sposób na deployment, ale możemy też wpisać go w plik YAML jawnie określając ile instancji aplikacji wymieniamy w danym momencie oraz ile instancji może być niedostępne:

    spec:  
     replicas: 3  
     strategy:  
       type: RollingUpdate  
       rollingUpdate:  
         maxSurge: 2 # ile instancji dodajemy na raz  
         maxUnavailable: 0 # ile instancji może być niedostępnych  

Parametry _maxSurge_ oraz _maxUnavailable_ umożliwiają nam sterowanie szybkością instalacji, ewentualnymi kosztami oraz bezpieczeństwem korzystania z systemu

**Zalety:**

* Brak _downtime_
* Niskie koszty - minimalnie potrzebujemy jedną dodatkową instancję
* Wolna propagacja, dająca weryfikacji czy wszystko działa
* Można spokojnie odbudować “dane” na przykład w cache, bez ciężkich zapytań do bazy danych przez wszystkie instancje na raz
* Łatwość implementacji w Kubernetes ;)

**Wady:**

* Należy zaprojektować obsługę dwóch wersji API czy dwóch schematów bazy danych (szczególnie przy ORM)
* _Rollout_ i _rollback_ zajmują czas szczególnie “rozgrzewanie” instancji trwa długo

## Canary

Pewnie słyszeliście o tej metodzie, ale czy wiecie skąd wzięła się nazwa “kanarek”?

Pochodzi ona od starego sposobu stosowanego w brytyjskich (i nie tylko) kopalniach. Według [Kata Eschnera z museum Smithsonian](https://www.smithsonianmag.com/smart-news/story-real-canary-coal-mine-180961570/) polegała ona na używaniu żywych kanarków w celu wykrycia czadu i innych trujących gazów. Przy niskim stężeniu gazów ptaszek stroszył pióra, a przy większym omdlewał albo i nawet umierał. Brutalna metoda, ale bardzo skuteczna. Na pocieszenie dodam, że Brytyjscy górnicy po zauważeniu niepokojących objawów wychodzi i podawali kanarkom tlen.

A jak to jest powiązane z wytwarzaniem oprogramowania i wdrożeniami? W dużym uproszczeniu, gdy wypuszczamy nową wersję, część naszych użytkowników staje się takimi właśnie kanarkami. Obserwujemy ich bardzo uważnie i gdy wszystko jest w porządku, zwiększamy liczbę użytkowników. Sama metoda wdrażania jest więc bardzo podobna do _ramped_ (aka _rolling-update_). Jedyna różnica odpowiedzialność za liczbę replik v1.0.0 i v2.0.0, która spoczywa na “ludziach”, a nie K8s.

Najprostszym przepisem na taką instalację jest:

1. Wdrożyć v1.0.0 w 9 replikach
2. Wdrożyć v2.0.0 w 1 replice (10% ruchu trafia do _canary_)
3. Po weryfikacji zwiększać liczbą v2.0.0 i zmniejszać v1.0.0 za pomocą komendy _kubectl scale_

Jeżeli nasz ruch do aplikacji przechodzi przez Ingress (taki jeden serwis wystawiany na świat) i nie ma komunikacji wewnętrznej to możemy skorzystać z adnotacji w Ingress

     annotations:  
       kubernetes.io/ingress.class: "nginx"  
       # Włączenie canary i przekierowanie 10% ruchu  
       nginx.ingress.kubernetes.io/canary: "true"  
       nginx.ingress.kubernetes.io/canary-weight: "10"  

**Zalety:**

* Brak _downtime_
* Nowa wersja dotyka tylko części użytkowników
* Wymusza dobry monitoring :)
* Szybki _rollback_

**Wady:**

* Powolny _rollout_
* W zależności od implementacji może być zasobożerne, przez co drogie

## Shadow

Jestem przekonany, że słyszeliście o firmie Tesla, a także o autopilocie wbudowanym w ich samochody. Mała dygresja, wyobraź sobie drogi Czytelniku sytuację, w której w Tesli jedzie śpiący pijany kierowca. Czy popełnia on przestępstwo? Jedzie, ale nie prowadzi. To nie abstrakcja i takie sytuację miały już miejsce. Polecam poszukać w Google: _drunk driver tesla_.  
Wróćmy jednak do oprogramowania. Niezależnie od stanu prawnego, firma musi mieć pewność, że oprogramowanie autopilota jest 100% sprawne i wszystkie testy regresyjne przechodzą. Ciężko jednak wykonać takie testy, gdyż symulator nie odda wszystkich sytuacji, a ręcznie są one niewykonalne. Na samych testach jednostkowych, ja osobiście bym w tej sytuacji nie polegał. Co w takim razie można zrobić? Wgrać do wszystkich samochodów dwie wersje oprogramowania, z czego tylko jedna jest odpowiedzialna za pracę samochodu. Druga natomiast działa jak cień (czyli _shadow_), dostaje takie same dane jak pierwsza, natomiast wynik działania jest tylko zapisywany i nie wpływa na samochód. Dzięki temu możemy przetestować nasze oprogramowanie na wszystkich użytkownikach i przeanalizować miliony jak i nie miliardy operacji. W uproszczeniu ta metoda to testowanie na produkcji w bezpieczny sposób.

Niestety tej metody bez dużej liczby zmian w kodzie i infrastrukturze nie jesteśmy wstanie wprowadzić. Przykładowy problem to jak rozwiązać wirtualne zapisy do bazy danych, czy wirtualne wysłanie wiadomości na kolejki. Wszystkie interakcje ze światem, muszą być w aplikacji odpowiednio zamokowane. Dodatkowo potrzebujemy komponentu, który zbiera wyniki, porównuje je i wykonuje analizę. Podsumowując dużo pracy.

**Zalety:**

* Brak wpływu na użytkownika
* Bardzo dokładne testy na danych produkcyjnych
* Bezpieczny _rollout_

**Wady:**

* Bardzo dużo pracy
* Podwójna infrastruktura
* Może powodować niebezpieczeństwo przy złej konfiguracji

## Podsumowanie

Opisaliśmy 6 sposób na automatyczny deployment. Jeżeli kojarzysz jeszcze jakiś to napisz do mnie koniecznie!

**p.s. Jeszcze raz przypominam o LIVE (**[**Facebook**](https://www.facebook.com/events/381253005877591/) **i** [**YouTube**](http://poznajkubernetes.pl/live2)**) oraz samym kursie** [**https://poznajkubernetes.pl**](https://poznajkubernetes.pl "https://poznajkubernetes.pl")