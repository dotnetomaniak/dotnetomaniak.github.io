---
layout: post
title: 'Co tam Panie w dotnecie? #07/2020'
date: 2020-03-23 23:00:00 +0000
header-img: ''

---
## NET 5.0 i dużo przecieków

Zaczynają się "konkretne" przecieki na temat NET 5.0. Jest ich już całkiem sporo. Między innymi oficjalne:

* [Announcing .NET 5 Preview 1](https://devblogs.microsoft.com/dotnet/announcing-net-5-0-preview-1/)
* [Announcing Entity Framework Core 5.0 Preview 1](https://devblogs.microsoft.com/dotnet/announcing-entity-framework-core-5-0-preview-1/)
* [Async ValueTask Pooling in .NET 5](https://devblogs.microsoft.com/dotnet/async-valuetask-pooling-in-net-5/)

I dwa wpisy od Steve Gordon:

* Jak wykonać migrację z 3.1 na 5.0 (mało ekscytujące bo wszystko poszło jak bułka z masłem) - [https://www.stevejgordon.co.uk/upgrading-from-asp-net-core-3-1-to-5-0-preview-1](https://www.stevejgordon.co.uk/upgrading-from-asp-net-core-3-1-to-5-0-preview-1 "https://www.stevejgordon.co.uk/upgrading-from-asp-net-core-3-1-to-5-0-preview-1")
* Moje ulubione, czyli po co nam HttpProtocol - [https://www.stevejgordon.co.uk/asp-net-core-5-features-introducing-httpprotocol](https://www.stevejgordon.co.uk/asp-net-core-5-features-introducing-httpprotocol "https://www.stevejgordon.co.uk/asp-net-core-5-features-introducing-httpprotocol")

A na dodatek jeszcze bardziej agresywny IL Linker. Więcej na [Twitter](https://twitter.com/MStrehovsky/status/1238105719804755968) i [GitHub](https://github.com/mono/linker/pull/988)

## Migracja do NET Core 3.1 na przykładzie Octopus Server

Bardzo fajna prezentacja na temat co bolało z przeniesieniem się na NET Core i co ważniejsze Linux na przykładzie Octopus Server. Mówiąc szczerze mam podobną prezentację i część tych samych problemów. Jak planujesz to warto przeczytać i jak masz jakieś pytania to napisz do mnie, to opowiem o swoim przykładzie.

[https://octopus.com/blog/octopus-server-dotnet-core-lessons-learned#lessons-learned-porting-octopus-server-to-net-core-3-1](https://octopus.com/blog/octopus-server-dotnet-core-lessons-learned#lessons-learned-porting-octopus-server-to-net-core-3-1 "https://octopus.com/blog/octopus-server-dotnet-core-lessons-learned#lessons-learned-porting-octopus-server-to-net-core-3-1")

## Jak szybki może być CRUD na NET Core i Azure SQL

Bardzo prosta aplikacja, doprowadzona do MEGA wydajności: 10K requestów na sekundę z użyciem Azure SQL, Dapper i JSON. Warto przejrzeć: [https://techcommunity.microsoft.com/t5/azure-sql-database/10k-request-per-second-rest-api-with-azure-sql-dapper-and-json/ba-p/1189675](https://techcommunity.microsoft.com/t5/azure-sql-database/10k-request-per-second-rest-api-with-azure-sql-dapper-and-json/ba-p/1189675 "https://techcommunity.microsoft.com/t5/azure-sql-database/10k-request-per-second-rest-api-with-azure-sql-dapper-and-json/ba-p/1189675")

## Tydzień dotnetomaniaka

W zeszłym tygodniu, aż 14 postów. Jest MEGA i strasznie się cieszę. Wszystkie dostępne na: [https://dotnetomaniak.pl/weekly/2020/11](https://dotnetomaniak.pl/weekly/2020/11 "https://dotnetomaniak.pl/weekly/2020/11")