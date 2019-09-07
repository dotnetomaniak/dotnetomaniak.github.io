---
layout: post
title: 'Co tam Panie w dotnecie? #24'
date: 2019-09-08 22:00:00 +0000
header-img: "/images/content/ahmad-odeh-TK_WT3dl2tw-unsplash (1).jpg"

---
Wakacje się skończyły, więc powracamy z cyklem news ze świata .NET. Dzisiejsza edycja wybiega poza ostatni tydzień, bo wiadomości w sierpniu się nazbierało. Ale wygrywa jedna na temat musicalu.

## ValueTask czyli Marc Gravell w formie

Jeżeli jeszcze nie bawiliście się ValueTask, to artykuł Marca na pewno Was przekona. Bardzo dogłębna analiza kiedy używać Task, a kiedy ValueTask. Całość moim zdaniem ułatwia lepsze zrozumienie asynchroniczności. Więcej: [https://blog.marcgravell.com/2019/08/prefer-valuetask-to-task-always-and.html](https://blog.marcgravell.com/2019/08/prefer-valuetask-to-task-always-and.html "https://blog.marcgravell.com/2019/08/prefer-valuetask-to-task-always-and.html")

Przy okazji jeszcze jeden drobiazg. Może się wydawać, że ValueTask ma pewne braki w API. Ale jest biblioteka, która dodaje metody WhenAny, WhenAll, Lazy właśnie do ValueTask. Więcej: [https://github.com/Cysharp/ValueTaskSupplement](https://github.com/Cysharp/ValueTaskSupplement "https://github.com/Cysharp/ValueTaskSupplement")

## Zaproszenie

Przy okazji chciałbym zaprosić Cię na "Wieczór z Kubernetes", który organizuję wraz z Jakubem Gutkowskim i Łukaszem Kałużnym. Porozmawiamy o nowoczesnej architekturze i jej problemach. Spojrzymy trochę na infrastrukturę i spróbujemy sobie odpowiedzieć czy potrafi ona nam pomóc. Postaramy się jak Kubernetes radzi sobie i w czym może nam pomóc.

Jeżeli masz ochotę się zapisać, dostać ebook "Jak zacząć pracę z Kubernetes" oraz dostawać co tydzień wiadomości w tematyce nowoczesnej architektury i Kubernetes to zapraszam na stronę: [http://webinar.poznajkubernetes.pl](http://webinar.poznajkubernetes.pl "http://webinar.poznajkubernetes.pl").

Możesz też dodać się do wydarzenia na Facebook: [https://www.facebook.com/events/489059444977239/](https://www.facebook.com/events/489059444977239/ "https://www.facebook.com/events/489059444977239/")

## Microsoft to musical

Obejrzałem już 2 raz i nadal nie jakoś nie mogę uwierzyć, że to jest naprawdę. Moim faworytem jest koszulka ze znaczkiem Excela. Prawie 8 minut (+ napisy na 2.5) śpiewanej opowieści o Microsoft

<iframe width="560" height="315" src="https://www.youtube.com/embed/ZGeWNR8CWnA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Przez powyższe video świat MS na zawsze się dla mnie zmienił :)

## Kącik wydajności

W tym tygodniu dwa tematy:

1. Seria artykułów która wchodzi głęboko w tematykę performance counters w nowym wydaniu w dotNet Core. Dla zainteresowanych: [https://medium.com/asos-techblog/maximising-net-core-api-performance-11ad883436c](https://medium.com/asos-techblog/maximising-net-core-api-performance-11ad883436c "https://medium.com/asos-techblog/maximising-net-core-api-performance-11ad883436c")
2. Biblioteka ArrayFire ([https://github.com/arrayfire/arrayfire-dotnet](https://github.com/arrayfire/arrayfire-dotnet "https://github.com/arrayfire/arrayfire-dotnet")), która umożliwia łatwiejsze pisanie (lepszego) "naukowego" kodu uruchamianego na CUDA, OpenCL czy CPU.

## Walidacja haseł

Słyszałeś o serwisie "have i been pwned"? Jeżeli nie to jak najszybciej czas nadrobić ten brak i wejść na [https://haveibeenpwned.com/](https://haveibeenpwned.com/ "https://haveibeenpwned.com/"). Dzięki niemu masz szansę dowiedzieć się kiedy Twoje hasło wyciekło.

Co jednak z naszymi użytkownikami? Czy możemy ich chronić? Szczególnie tych mało zaawansowanych techniczne. Jakiś czas temu Troy Hunt (autor powyższej strony) udostępnił API do weryfikacji, czy dane hasło wyciekło. Sam sposób sprawdzania jest bezpieczny, a opisy jak to jest zrobione są warte przeczytania.

Ale dlaczego o tym piszę? Czeski MVP - Valášek Altair - opublikował paczkę NuGet, dzięki której możemy sprawdzać API serwisu "have i been pwned" natywne w dotNET. Cały kod jest dostępny na GitHub: [https://github.com/ridercz/Altairis.Services.PwnedPasswordsValidator](https://github.com/ridercz/Altairis.Services.PwnedPasswordsValidator "https://github.com/ridercz/Altairis.Services.PwnedPasswordsValidator")

Warto przemyśleć wykorzystanie w swojej aplikacji.

## Canary Testing w .NET

Poniższy artykuł pokazuje jak za pomocą biblioteki Scientist, wykonać Canary Testing w sposób prawie bezbolesny. Mówiąc szczerze nigdy jej nie używałem, ale pomysł mi się podoba i mam zamiar niedługo spróbować. Bardzo ciekawy artykuł:

[https://dev.to/integerman/victimless-canary-testing-](https://dev.to/integerman/victimless-canary-testing-with-scientist-9nn "https://dev.to/integerman/victimless-canary-testing-with-scientist-9nn")

## DotNet najlepszą platformą jest i już

Na sam koniec małe heheszki, które umieścił Scott Hanselman w ramach zapowiedzi .NET Conf (23-25 września online)  
<blockquote class="twitter-tweet" data-conversation="none"><p lang="en" dir="ltr">What can you do with .NET? A teaser. <a href="https://twitter.com/hashtag/dotnet?src=hash&ref_src=twsrc%5Etfw">#dotnet</a> <a href="https://twitter.com/hashtag/dotnetconf?src=hash&ref_src=twsrc%5Etfw">#dotnetconf</a> <a href="https://t.co/bJbpgvziJZ">pic.twitter.com/bJbpgvziJZ</a></p>— Scott Hanselman (@shanselman) <a href="https://twitter.com/shanselman/status/1169403223016263680?ref_src=twsrc%5Etfw">September 5, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Więcej szczegółów na temat samej konferencji na oficjalnej stronie: [https://www.dotnetconf.net/](https://www.dotnetconf.net/ "https://www.dotnetconf.net/")