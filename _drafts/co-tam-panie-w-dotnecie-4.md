---
layout: post
title: 'Co tam Panie w dotnecie? #4'
date: 2019-03-02 23:00:00 +0000
header-img: ''

---
Od czego by tu zacząć? Tyle znalazłem, że mam problem z wyborem. No dobra jedziemy wedle kolejności.

## Nowe Visual Studio 2019 RC

Oficjalna premiera już 2 kwietnia, za miesiąc. Ale do pobrania jest release candidate. Patrząc po doświadczeniach z 2017, spokojnie można je pobrać i używać. Nie powinno być potem problemów z deinstalacją czy upgrade do pełnej wersji. Przy okazji co jak i gdzie - czyli wersje i usprawnienia w oficjalnym poście: [Visual Studio 2019 Release Candidate (RC) now available](https://devblogs.microsoft.com/visualstudio/visual-studio-2019-release-candidate-rc-now-available/)

Przy okazji może mielibyście ochotę się spotkać z okazji premiery w okolicy 2 kwietnia? Może nie są to Oskary, ale wiecie ... Jeżeli tak to dajcie mi znać!!

## Desktop i dotNET Core 3.0

Powoli pojawiają się pierwsze przykłady jak migrować aplikacje desktop do nowego Core 3.0. Nie wiem czy wszyscy zdecydują się na taką migrację, ale przynajmniej przestanie brakować głównego powodu: nie da się. Czy firmy się zdecydują to inna kwestia, ale wydaje mi się, że powoli NET Framework zostanie skazany na wymarcie. Żeby było jasne nie wszystko jeszcze działa. Na przykład nie ma designer do WinForms, ale są obejścia. Więcej w formie pełnego tutoriala w [How to port desktop applications to .NET Core 3.0](https://devblogs.microsoft.com/dotnet/how-to-port-desktop-applications-to-net-core-3-0/) oraz [video na Channel 9 ](https://channel9.msdn.com/Shows/On-NET/How-to-port-desktop-applications-to-NET-Core-30)

## JSON i ...

Ostatnio znany bloger powiązany z Microsoft - Scott H. opublikował na swoim blogu informacje jakoby jeden z głównych deweloperów dotnet Core David F. wraz z twórcą najbardziej popularnej paczki do JSON czyli Jamsem N.-K. szykowali rewolucję w obsłudze formatu JSON. Czy to prawda? To się okaże ale dowody na GitHub wskazują, że wymienione osoby mają coś na sumieniu. Więcej można przeczytać na [oficjalnym blogu Scotta H.](https://www.hanselman.com/blog/LearningAboutNETCoreFuturesByPokingAroundAtDavidFowlersGitHub.aspx)

Przy okazji JSON jeszcze jeden artykuł jak szybko można go parsować: [Parsing Gigabytes of JSON per Second](https://branchfree.org/2019/02/25/paper-parsing-gigabytes-of-json-per-second/) Nie jest z dotNET, ale poczytać i popatrzeć warto.

## ... i gRPC

Coś nowego w dotNET zaczyna się pojawiać. Standard zaprojektowany przez Google do komunikacji pomiędzy serwisami. I to kolejna nowość, którą ma przynieść 3.0. Więcej w [An Early Look at gRPC and ASP.NET Core 3.0](https://www.stevejgordon.co.uk/early-look-at-grpc-using-aspnet-core-3)

## Automapper

Pewnie używaliście, albo używać będziecie. Nie jest to ideał ale czasem ta biblioteka pomaga. Czasem też przeszkadza. Bo jak wiadomo silver bullet nie istnieje. Dlatego właśnie Jimmy Bogard opublikował kiedy warto a kiedy nie warto go używać czyli [AutoMapper Usage Guidelines](https://jimmybogard.com/automapper-usage-guidelines/)

A jak już przeczytacie to warto spojrzeć na wypowiedź tego właśnie autora na Twitter: [https://twitter.com/jbogard/status/1100394639155253250](https://twitter.com/jbogard/status/1100394639155253250 "https://twitter.com/jbogard/status/1100394639155253250") i oczywiście prześledzić całą dyskusję + artykuł Cezarego Piątka od którego się zaczęła :)

## Span<T> oraz System.IO.Pipelines

Dwa różne artykuły, na temat różnych kawałków, ale jakoś bliskie sobie:

* Pipelines.Sockets.Unofficial - [Arena Allocation ](https://github.com/mgravell/Pipelines.Sockets.Unofficial/blob/master/docs/arenas.md) autorstwa Marca Gravella
* [An Introduction to Optimising Code Using Span<T>](https://www.stevejgordon.co.uk/an-introduction-to-optimising-code-using-span-t) Steva Gordona

Solidna dawka wiedzy w obu, a moje podsumowanie chyba totalnie zbędne :)

## Co można zamiast licencji

Licencje, prawnicy, wykorzystanie - ile tego jest. Czasem aż głowa boli, że mamy open-source, a sami nie wiemy czy możemy go użyć. Jeden z wyjątków jest w kodzie SQLLiteDialect do Hibernate w Javie. Jest to błogosławieństwo. Nie wierzycie? To sprawdźcie sami: [https://github.com/gwenn/sqlite-dialect/blob/master/src/main/java/org/hibernate/dialect/SQLiteDialect.java#L1-L9](https://github.com/gwenn/sqlite-dialect/blob/master/src/main/java/org/hibernate/dialect/SQLiteDialect.java#L1-L9 "https://github.com/gwenn/sqlite-dialect/blob/master/src/main/java/org/hibernate/dialect/SQLiteDialect.java#L1-L9")

## Polskie blogi czyli podsumowanie dotnetomaniaka

Jeżeli jeszcze nie czytaliście to jest od wczoraj dostępne podsumowanie tygodnia dotnetomaniaka: [https://dotnetomaniak.pl/weekly/2019/08](https://dotnetomaniak.pl/weekly/2019/08 "https://dotnetomaniak.pl/weekly/2019/08")

Zapraszam serdecznie bo warto!

## Chwalimy się na koniec

Tym razem na koniec mój własny wkład w open-source. Udało mi się poprawić Azure DevOps i NuGet Publish Task. Dodałem obsługę konfliktów na Linux. Zmiana już zaakceptowana, ale jeszcze nie dostępna.  Jak ktoś jest ciekaw to zapraszam: [https://github.com/Microsoft/azure-pipelines-tasks/pull/9666](https://github.com/Microsoft/azure-pipelines-tasks/pull/9666 "https://github.com/Microsoft/azure-pipelines-tasks/pull/9666")

Po więcej zapraszam za tydzień!