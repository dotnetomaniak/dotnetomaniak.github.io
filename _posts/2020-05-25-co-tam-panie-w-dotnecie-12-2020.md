---
layout: post
title: 'Co tam Panie w dotnecie? #12/2020'
date: 2020-05-25 22:00:00 +0000
header-img: "/images/content/pablo-12.jpg"

---
W zeszły tygodniu tak dużo wpadało nowości, że odsunąłem podsumowanie tygodnia :) MsBuild przyniósł naprawdę potężną dawkę nowości zapowiadanych wcześniej oraz niespodzianek.

## Web+Mikroserwisy

* Blazor WebAssebly ma oficialny release. Wersja v3.2.0 co jak sugeruje nie jest to już preview. Kiedyś takim wyznacznikiem było 1.0, a teraz taki postęp;) Oczywiście całość komunikatu jest dostępna: [https://devblogs.microsoft.com/aspnet/blazor-webassembly-3-2-0-now-available/](https://devblogs.microsoft.com/aspnet/blazor-webassembly-3-2-0-now-available/ "https://devblogs.microsoft.com/aspnet/blazor-webassembly-3-2-0-now-available/")
* [Project Tye ](https://devblogs.microsoft.com/aspnet/introducing-project-tye/)- ponieważ kilka osób w MS zauważyło, że praca z mikro serwisami jest trudna to zaproponowali nam nowy framework, który ma to uprościć. Szczególnie, gdy planujesz hosting na Kubernetes (p.s. kurs "Dotknij Kubernetes" nadal jest dostępny za darmo - [https://poznajkubernetes.pl/mini-szkolenie.html](https://poznajkubernetes.pl/mini-szkolenie.html "https://poznajkubernetes.pl/mini-szkolenie.html"))
* Dapr - kolejna wersja, kolejne rozszerzenie. Trochę kłóci się to z Tye, a może lepiej powiedzieć, że konkuruje. Nie jest to jeszcze production ready bo wersja v0.7.0, ale nadal uważam, że warto oglądać to ten właśnie projekt z uwagą. Jak nigdy nie widziałeś/aś to polecam [zerknąć na sesje](https://mybuild.microsoft.com/sessions?t=%257B%2522from%2522%253A%25222020-05-19T00%253A00%253A00%252B02%253A00%2522%252C%2522to%2522%253A%25222020-05-21T23%253A59%253A00%252B02%253A00%2522%257D&q=dapr&s=%257B%2522name%2522%253A%2522translate.refine.label.sort.relevance%2522%252C%2522type%2522%253A0%257D) albo na artykuł [https://dev.to/arschles/what-is-dapr-526a](https://dev.to/arschles/what-is-dapr-526a "https://dev.to/arschles/what-is-dapr-526a")
* [YARP](https://devblogs.microsoft.com/dotnet/introducing-yarp-preview-1/) - szukasz reverse proxy? Nie chcesz NGiNX, a lubisz dotnet core, to może być dla Ciebie idealna oferta. Jak to będzie działało? Pożyjemy zobaczymy na razie wersja 0.1 preview, więc prawie production-ready ;)

## .NET

* [C# 9 Preview]() - dużo dodatków. Jedni się śmieją, drudzy cieszą. Jak będę miał na co dzień to na pewno będę się cieszył :)
* [F# 5 preview](https://devblogs.microsoft.com/dotnet/f-5-update-for-net-5-preview-4/) - jak wyżej :)

## GUI

* [Project Reunion](https://github.com/microsoft/ProjectReunion) - próba uporządkowania i połączenia aplikacji Win32 oraz UWP.
* [MAUI](https://devblogs.microsoft.com/dotnet/introducing-net-multi-platform-app-ui/) - ewolucja Xamarin.Forms w coś nowego i lepszego, co w dłuższej perspektywie ma zastąpić Xamarin.Forms

## Windows

* [Windows Terminal 1.0 ](https://devblogs.microsoft.com/commandline/windows-terminal-1-0/)- nie jest to preview, tylko wreszcie "stable". Ja się cieszę, bo używam jak tylko jestem na Windows. Na mac i Linux nie działa :(
* [WSL2](https://devblogs.microsoft.com/commandline/the-windows-subsystem-for-linux-build-2020-summary/) - już powoli chyba spływa najnowszy update Windows (May 2020 Update) i w nim jest właśnie WSL2 i a także pełnoprawny Linux wewnątrz Windows. Co zmieni pracę szczególnie z Docker (oraz pewnie i Kubernetes). Osobiście najbardziej podoba mi się, że niedługo aplikacje GUI z Linux będą dostępne na Windows.
* [winget](https://devblogs.microsoft.com/commandline/windows-package-manager-preview/) - package manager dla Windows. Niby już istnieje chocolatey, ale wiadomo, że trzeba zrobić swój ;) Ciekawy jestem kto zostanie choco czy winget :)

No i to by było chyba na tyle. A jak potrzebujesz spisu treści co jeszcze się wydarzyło to dostępna jest "Book of News": [https://news.microsoft.com/build-2020-book-of-news/](https://news.microsoft.com/build-2020-book-of-news/ "https://news.microsoft.com/build-2020-book-of-news/")

Miłego tygodnia!