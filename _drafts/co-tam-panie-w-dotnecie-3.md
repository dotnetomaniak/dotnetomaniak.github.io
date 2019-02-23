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

## Stary dobry NET Framework jeszcze się trzyma

4\.8 ogłoszony już dawno. Aktualnie do "testów" udostępniona do użycia wersja Early Access Build 3745. Więcej na [oficjalnym blogu ](https://devblogs.microsoft.com/dotnet/announcing-net-framework-4-8-early-access-build-3745/)

## Wydajność na 1 miejscu

Nie wiem jak u Was, ale z wydajnością bywa różnie. Często nie ma ona znaczenia, aż do tego strasznego dnia gdy coś zaczyna boleć. Poczytać zawsze warto, a nuż widelec coś w głowie zostanie i się przyda ;) W tej tematyce aż 3 artykuły w tym tygodniu:

* Jak "szybki" potrafi być [Azure SQL w ładowaniu danych.](https://www.brentozar.com/archive/2019/02/how-fast-can-a-21468-mo-azure-sql-db-load-data/) Polecam przeczytać cały artykuł. Spędzić chwilę i zacząć czytać komentarze. Dlaczego? Bo czasem potrzebny jest DBA nim deweloper zacznie liczyć :)
* Drugi temat z czytania z bazy danych. Tym razem AKS (Azure Kubrenetes Service) + SQL lite montowany jako Azure File share. Więcej pod linkiem: [https://zimmergren.net/processing-sqlite-on-azure-files-share-azure-kubernetes-services/](https://zimmergren.net/processing-sqlite-on-azure-files-share-azure-kubernetes-services/ "https://zimmergren.net/processing-sqlite-on-azure-files-share-azure-kubernetes-services/")
* Do szybkiego przelecenia porównanie szybkości routing w [ASP.NET MVC i ASP.NET Core MVC](https://www.khalidabuhakmeh.com/comparing-asp-net-core-routing-performance-to-asp-net-mvc). Może komuś pomoże przy argumentacji czy warto się przesiąść na Core ;)
* Wstęp do serii postów na [blogu Steva Gordona](https://www.stevejgordon.co.uk/motivations-for-writing-high-performance-csharp-code) dlaczego warto pisać wysoko wydajny kod w C#. Wstęp przyjemny, mam nadzieję że seria też będzie trzymała poziom. Pożyjemy zobaczymy :)
* 