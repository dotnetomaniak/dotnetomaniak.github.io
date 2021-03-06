---
layout: post
title: 'Co tam Panie w dotnecie? #18'
date: 2019-06-09 22:00:00 +0000
header-img: "/images/content/hayden-walker-705539-unsplash.png"

---
Nowości ze świata .NET edycja 18. W tym tygodniu stojąca pod znakiem ciekawostek drobnych, ale użytecznych na co dzień. No to co, zaczynamy? TAK!

## Enity Framework w dwóch odsłonach

Dwie wiadomości dotyczące EF. Zacznijmy od ciekawostki. Jeff Hollan, czyli PM Azure Functions, pokazuje jak można używać Entity Framework właśnie w Azure Functions. Co więcej jako przykładu używa systemu do blogowania. O tym nietypowym wykorzystaniu można przeczytać w artykule:[ Using Entity Framework with Azure Functions](https://dev.to/azure/using-entity-framework-with-azure-functions-50aa)

Druga wiadomość jest bardziej interesująca i dla niektórych może okazać się bolesna. Nadchodzą "breaking changes" razem z wersję EF Core 3.0. I jest ich naprawdę sporo, bo aż 40! Najważniejsze moim zdaniem to:

1. Dotychczas gdy EF nie umiał wykonać konwersji LINQ na SQL - kwerenda wykonywała się częściowo po stronie klienckiej. Najbardziej znany przykład do GROUP BY do wersji 2.1. Od wersji 3.0 w takiej sytuacji, będzie wyjątek w domyślnych ustawieniach.
2. Funkcja `FromSQL` będzie zamieniona na `FromSqlRaw` i `FromSqlInterpolated`, by uniknąć niechcianych SQL injection
3. Zmiany dotyczące użycia getter i setter - w nowej wersji zostaną one pominięte i od razu zapis nastąpi do tzw. "backing field"

Więcej informacji dostępnych pod URL: [https://docs.microsoft.com/en-us/ef/core/what-is-new/ef-core-3.0/breaking-changes#query-types-are-consolidated-with-entity-types](https://docs.microsoft.com/en-us/ef/core/what-is-new/ef-core-3.0/breaking-changes#query-types-are-consolidated-with-entity-types "https://docs.microsoft.com/en-us/ef/core/what-is-new/ef-core-3.0/breaking-changes#query-types-are-consolidated-with-entity-types")

## Core WF i WCF

Duży strach przed migracją do .NET Core to 2 skróty: WCF i WF. Jeżeli nie znasz ich to pewnie jesteś szczęśliwym człowiekiem :) Microsoft nadal nie zamierza ich przenosić na .NET Core, ale pojawiły się dwa projekty open-source, które mogą Cię wspomóc: Core WCF i Core WF. Więcej na ich temat (i minimalnym wsparciu) można przeczytać na stronie: [https://devblogs.microsoft.com/dotnet/supporting-the-community-with-wf-and-wcf-oss-projects/](https://devblogs.microsoft.com/dotnet/supporting-the-community-with-wf-and-wcf-oss-projects/ "https://devblogs.microsoft.com/dotnet/supporting-the-community-with-wf-and-wcf-oss-projects/"). Dodatkowo .NET Foundation wita oba na swoim pokładzie: [https://dotnetfoundation.org/blog/2019/06/07/welcoming-core-wcf-to-the-net-foundation](https://dotnetfoundation.org/blog/2019/06/07/welcoming-core-wcf-to-the-net-foundation "https://dotnetfoundation.org/blog/2019/06/07/welcoming-core-wcf-to-the-net-foundation")

## Alternatywa do WCF

Mark Rendle na swoim nowym blogu, pokazuje porównanie w użyciu gRPC oraz WCF. Patrzy pod rożnymi kątami i sprawdza jak można się migrować. Warto poczytać:

* Odcinek 1 - [https://unwcf.com/posts/wcf-vs-grpc/](https://unwcf.com/posts/wcf-vs-grpc/ "https://unwcf.com/posts/wcf-vs-grpc/")
* Odcinek 2 - [https://unwcf.com/posts/wcf-vs-grpc-round-2/](https://unwcf.com/posts/wcf-vs-grpc-round-2/ "https://unwcf.com/posts/wcf-vs-grpc-round-2/")

Pozostałe artykuły na temat uwolnienia się z WCF, są też warte spojrzenia: [https://unwcf.com/](https://unwcf.com/ "https://unwcf.com/")

A przy okazji gRPC to 4 czerwca zespół gRPC gościł w ASP.NET Community Standup: [https://www.youtube.com/watch?v=Pa6qtu1wIs8](https://www.youtube.com/watch?v=Pa6qtu1wIs8 "https://www.youtube.com/watch?v=Pa6qtu1wIs8")

## Blazor + Material Design = <3

Cały czas nie mogę uwierzyć jak rozwija się Blazor. I mówiąc szczerze nadal traktuje go jako ciekawostkę. Pewnie któregoś dnia się to zmieni, patrząc na to co się dzieje wokół tego projektu. Tym razem komponenty w stylu Material Design do Blazor o nazwie idealnie pasującej: [MatBlazor](https://www.matblazor.com/)

## Oracle i Microsoft łączą siły

Ten nagłówek to nie dowcip. Jeszcze nie do końca wiadomo co z tego wyniknie, ale współpraca została ogłoszona. Połączenie jest w tematyce chmur, a dokładniej Oracle Cloud i Azure. Więcej w artykułach:

* od TechCrunch: [https://techcrunch.com/2019/06/05/microsoft-and-oracle-link-up-their-clouds/](https://techcrunch.com/2019/06/05/microsoft-and-oracle-link-up-their-clouds/ "https://techcrunch.com/2019/06/05/microsoft-and-oracle-link-up-their-clouds/")
* i od MS: [https://news.microsoft.com/2019/06/05/microsoft-and-oracle-to-interconnect-microsoft-azure-and-oracle-cloud/](https://news.microsoft.com/2019/06/05/microsoft-and-oracle-to-interconnect-microsoft-azure-and-oracle-cloud/ "https://news.microsoft.com/2019/06/05/microsoft-and-oracle-to-interconnect-microsoft-azure-and-oracle-cloud/")

## Jak zmienił się świat

Na sam koniec historia zmiany. Jak wiecie ostatnimi laty Microsoft zrobił kilka naprawdę niesamowitych ruchów. Jednym z nich było przejęcie GitHub. Ale plan ten był już od 2014 roku. Microsoft nie był jednak na to gotowy. Całość historii o tym jak wróg numer 1, zaczął wygrywać wśród developerów można przeczytać na Bloomberg: [https://www.bloomberg.com/news/articles/2019-06-03/open-source-great-satan-no-more-microsoft-wins-over-skeptics](https://www.bloomberg.com/news/articles/2019-06-03/open-source-great-satan-no-more-microsoft-wins-over-skeptics "https://www.bloomberg.com/news/articles/2019-06-03/open-source-great-satan-no-more-microsoft-wins-over-skeptics") 