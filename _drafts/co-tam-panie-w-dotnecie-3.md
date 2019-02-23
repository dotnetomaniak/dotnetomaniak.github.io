---
layout: post
title: 'Co tam Panie w dotnecie? #3'
date: 2019-02-24 23:00:00 +0000
header-img: ''

---
No to jedziemy z podsumowaniem numer 3. W tym tygodniu zebrało się naprawdę sporo dobrego.

## dotNET Core - niedługo umrze król, niech żyje nowy król

Z jednej strony niedługo umrze dotNET Core 1.0 i 1.1, [już 27 czerwca](https://devblogs.microsoft.com/dotnet/net-core-1-0-and-1-1-will-reach-end-of-life-on-june-27-2019/). Aktualnie proponują migrację do 2.1. Śmiesznie bo ja już używam 2.2 regularnie :)

Natomiast ogłoszenia dotyczące "nowego" króla są coraz ciekawsze. W tym tygodniu najbardziej zainteresowały mnie 2 artykuły. Jeden od NDepend, co tu mówić reklama ich produktu, ale pokazują co **znika** w 3.0 w stosunku do 2.2 oraz co mniej ciekawe co się pojawia. Na poziomie klas i metod. Więcej: [https://blog.ndepend.com/exploring-net-core-3-0-new-api/](https://blog.ndepend.com/exploring-net-core-3-0-new-api/ "https://blog.ndepend.com/exploring-net-core-3-0-new-api/").

Drugi artykuł to: [Features To Build Better Applications With .NET Core 3](https://hackernoon.com/features-to-build-better-applications-with-net-core-3-dc320740e0a9) raczej do przelecenia wzrokiem i upewnienia się że wszystko już wiemy, niż głębokiego czytania. Dla mnie zaskoczeniem było "Server-Side Blazor". Coś czuje, rośnie "Silverlight 2.0". Odpowiedź na pytanie czy to dobrze czy źle zostawiam już Wam :)

## ML.NET na fali wschodzącej

ML.NET - nie mam doświadczenia to się wypowiem ;) 

Czy ML.NET rzeczywiście będzie częścią NET Core 3.0? Tego jeszcze na 100% nie wiemy, ale jak ktoś chce zacząć to Ładny, łopatologiczny wstęp do ML.NET jest dostępny na: [https://rubikscode.net/2019/02/18/ultimate-guide-to-machine-learning-with-ml-net/](https://rubikscode.net/2019/02/18/ultimate-guide-to-machine-learning-with-ml-net/ "https://rubikscode.net/2019/02/18/ultimate-guide-to-machine-learning-with-ml-net/")

## Stary dobry NET Framework jeszcze się trzyma

4\.8 ogłoszony już dawno. Aktualnie do "testów" udostępniona do użycia wersja Early Access Build 3745. Więcej na [oficjalnym blogu ](https://devblogs.microsoft.com/dotnet/announcing-net-framework-4-8-early-access-build-3745/)

## Wydajność na 1 miejscu

Nie wiem jak u Was, ale z wydajnością bywa różnie. Często nie ma ona znaczenia, aż do tego strasznego dnia gdy coś zaczyna boleć. Poczytać zawsze warto, a nuż widelec coś w głowie zostanie i się przyda ;) W tej tematyce aż 3 artykuły w tym tygodniu:

* Jak "szybki" potrafi być [Azure SQL w ładowaniu danych.](https://www.brentozar.com/archive/2019/02/how-fast-can-a-21468-mo-azure-sql-db-load-data/) Polecam przeczytać cały artykuł. Spędzić chwilę i zacząć czytać komentarze. Dlaczego? Bo czasem potrzebny jest DBA nim deweloper zacznie liczyć :)
* Drugi temat z czytania z bazy danych. Tym razem AKS (Azure Kubrenetes Service) + SQL lite montowany jako Azure File share. Więcej pod linkiem: [https://zimmergren.net/processing-sqlite-on-azure-files-share-azure-kubernetes-services/](https://zimmergren.net/processing-sqlite-on-azure-files-share-azure-kubernetes-services/ "https://zimmergren.net/processing-sqlite-on-azure-files-share-azure-kubernetes-services/")
* Do szybkiego przelecenia porównanie szybkości routing w [ASP.NET MVC i ASP.NET Core MVC](https://www.khalidabuhakmeh.com/comparing-asp-net-core-routing-performance-to-asp-net-mvc). Może komuś pomoże przy argumentacji czy warto się przesiąść na Core ;)
* Wstęp do serii postów na [blogu Steva Gordona](https://www.stevejgordon.co.uk/motivations-for-writing-high-performance-csharp-code) dlaczego warto pisać wysoko wydajny kod w C#. Wstęp przyjemny, mam nadzieję że seria też będzie trzymała poziom. Pożyjemy zobaczymy :)
* Na sam koniec post, który podobał mi się najbardziej. Marc Gravell pokazuje jak to łatwo ubić StackOverflow. Sam tytuł już zachęca do czytania: [Fun with the Spiral of Death](https://blog.marcgravell.com/2019/02/fun-with-spiral-of-death.html), a podtytuł: "a cautionary tale of SemaphoreSlim" spowodował że kliknąłem bez wahania. Co i Wam radzę :)

## Serverless - czy już?

Wiele osób myśli o serverless. Wielu znam krytyków, wielu też zwolenników. Sam mam zdanie, że warto użyć. Oczywiście nie wszędzie i nie zawsze, ale nie ma w informatyce narzędzi uniwersalnych :)

Tym razem kilka argumentów dla przeciwników w artykule: [Why we're not moving our web APIs to azure functions yet](https://mithunshanbhag.github.io/2019/02/18/not-moving-web-apis-to-azure-functions.html)

## Ciekawostki inne :)

Nie wiem czy Robertowi Kubicy MS Teams pomoże, ale w Nascar podobno prowadzi do zwycięstwa. Nie dajecie wiary? No to obejrzyjcie reklamę: [https://www.youtube.com/watch?v=BmucQOIavmM&feature=youtu.be&_lrsc=1420a17e-72a5-483e-b4b4-066838bd3ca5](https://www.youtube.com/watch?v=BmucQOIavmM&feature=youtu.be&_lrsc=1420a17e-72a5-483e-b4b4-066838bd3ca5 "https://www.youtube.com/watch?v=BmucQOIavmM&feature=youtu.be&_lrsc=1420a17e-72a5-483e-b4b4-066838bd3ca5")

Na sam koniec perełka na temat biegania. Nie ma nic wspólnego z programowaniem, ale wielu programistów chwali się że biega. Ciekawi jesteście jaki wpływ ma to na Wasze zdrowie? Na pewno. A więc dla tych co biegają i będą biegać, a także dla tych co im się nie chce polecam artykuł: [Bieganie rekreacyjne - czy rzeczywiście zdrowe](https://tadeusz-szopa.blogspot.com/2019/02/bieganie-rekreacyjne-czy-rzeczywiscie.html)

## Polska blogosfera o dotnet

Jak co tydzień zapraszam na [podsumowanie tygodnia dotnetomaniaka](https://dotnetomaniak.pl/weekly/2019/08). 18 postów w sumie. Tematy od C# 8.0 aż do protobuf czy testów.

## Podobało się?

Daj znać! Wszelki feedback mile widziany. Zarówno kciuk w górę jak i smutna minka :)