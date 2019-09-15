---
layout: post
title: 6 sposób na deployment
date: 2019-09-14 22:00:00 +0000
header-img: ''

---
Niezależnie od technologii używanej w projekcie, raz na jakiś czas trzeba wdrożyć kod na produkcję. Sposobów na wdrożenie go jest N, gdzie N dąży do nieskończoności 😉. Tak jak każda firma ma w dzisiejszych czasach swój “scrum” albo “agile”, tak i ma swój sposób na instalacje. Jednym z moich ulubionych jest “sposób na PM’a”. Wygląda on następująco: PM tworzy task, a opsy go realizują...

Podchodząc do sprawy na poważnie, można N znacząco zredukować. Dzisiaj zaprezentuję 3 z pośród najbardziej popularnych technik wdrożeniowych. Kolejne przybliżę w przyszłym tygodniu.

## Autoreklama

Nim przejdziemy do teorii, chciałbym zaprosić Cię na drugą cześć LIVE Wieczoru z Kubernetes, który odbędzie się w najbliższy wtorek o godzinie 20:00. Więcej informacji na [Facebook ](https://www.facebook.com/events/381253005877591/)i [YouTube](http://poznajkubernetes.pl/live2).

Jest też nowa strona przedsprzedaży kursu "Poznaj Kubernetes", szczególnie polecam [sekcję "Dla Kogo"](https://poznajkubernetes.pl).

## Okienko serwisowe

W przypadku systemu z dużym oknem serwisowym (bardziej znanym pod angielską nazwą_maintenance window_) problem rozwiązuje się sam. Dla niektórych firm to zamierzchła przeszłość, ale wiele systemów poważnych instytucji wciąż wykorzystuje okna serwisowe. Szczególnie dwie noce w roku mają podwyższone prawdopodobieństwo wystąpienia “tego zjawiska”. Najbliższa odbędzie się w ostatni weekend października, w związku ze zmianą czasu. Dlaczego tak się dzieje?  
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

Jeżeli nie ma możliwości skorzystania z okna serwisowego, musimy zastosować inne metody. Najbliższa opisanemu powyżej rozwiązaniu w Kubernetes jest metoda wdrażania typu_recreate_.  
Na proces składają się następujące etapy: najpierw "ubijamy" wszystkie instancje naszej aplikacji, potem uruchamiamy nową wersję. Jaka jest różnica pomiędzy_recreate_a oknem serwisowym? W procesie bierze udział tylko aplikacja. Cała infrastruktura (np.: baza danych), którą mogliśmy włączyć/wyłączyć podczas okna serwisowego musimy mieć przygotowaną wcześniej.  
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

O sposobie wdrażania kodu typu_blue-green_usłyszałem bardzo dawno temu, w mojej pierwszej pracy. Sprowadza się on do posiadania dwukrotnie większej liczby serwerów niż nam potrzeba do prawidłowego działania aplikacji. Przynajmniej podczas wdrożenia. Nasze serwery dzielimy na dwie takie same grupy, jedną nazywamy_blue,_a drugą_green_. Przed nimi stawiamy element rozdzielający ruch (_router_) albo na jedną albo na druga grupę. W klasycznej architekturze trójwarstwowej można to zobrazować w ten sposób:  
![](https://lh5.googleusercontent.com/NJSFQMsEDBV4Nen8mwc_044Y5wHteRV0yDghVw0glJq7KICg3dRx-5tvOJADEjyxqOrzaMdwVR6UxR78CEXVO2n8fiVI4aqMfdCM5OgESXVugIA1InkvDI9nD0VZqyBvobM0dXNp =602x288)

Kiedy pierwszy raz przeczytałem o tym sposobie od razu nasunęło mi się pytanie: ale jak to, baza danych osobno? Jak widać na powyższym diagramie, pełny schemat_blue-green_zakłada, że serwery_blue_i serwery_green_mają także osobne bazy danych. Tak zostało to przedstawione przez Martina Fowlera. W rzeczywistości rzadko spotykamy system, który może działać w ten sposób. Dlatego przeważnie_blue-green_dotyczy tylko części aplikacyjnej.

Na schemacie mamy pokazaną sytuację w której wersja v1.0.0.0 jest wgrana na serwery_green_. Z niej korzystają użytkownicy, dzięki przekierowaniu całego ruchu przez_router_(czyli sprzętowy bądź_softwareowy load-balancer_). Wersję v2.0.0 wgrywamy na serwery_blue_, rozgrzewamy, testujemy, itp. Gdy wszystko jest gotowe przełączamy wajchę na_router_i kierujemy cały ruch na_blue_. A co robimy z serwerami_green_? Czekają sobie spokojnie, na kolejny_deployment_, w razie problemów umożliwiając szybki_rollback_. W wersji "taniej" po chwili możemy usunąć elementy_green_, ale wtedy tracimy możliwość_rollback_.

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

Jak na razie mamy za sobą sposoby, proste i przyjazne deweloperom. Jeżeli tematyka Cię zaciekawiła to zapraszam Cię na [https://poznajkubernetes.pl](https://poznajkubernetes.pl "https://poznajkubernetes.pl"). Podczas kursu będziesz miał okazję wypróbować powyższe i poniższe sposoby deployment :)