---
layout: post
title: 'Co tam Panie w dotnecie? #18'
date: 2019-06-09 22:00:00 +0000
header-img: ''

---
Nowości ze świata .NET edycja 18. W tym tygodniu stojąca pod znakiem ciekawostek drobnych, ale użytecznych na co dzień. No to co, zaczynamy? TAK!

## Enity Framework w dwóch odsłonach

Dwie wiadomości dotyczące EF. Zacznijmy od ciekawostki. Jeff Hollan, czyli PM Azure Functions, pokazuje jak można używać Entity Framework właśnie w Azure Functions. Co więcej jako przykładu używa systemu do blogowania. O tym nietypowym wykorzystaniu można przeczytać w artykule:[ Using Entity Framework with Azure Functions](https://dev.to/azure/using-entity-framework-with-azure-functions-50aa)

Druga wiadomość jest bardziej interesująca i dla niektórych może okazać się bolesna. Nadchodzą "breaking changes" razem z wersję EF Core 3.0. I jest ich naprawdę sporo, bo aż 40! Najważniejsze moim zdaniem to:

1. Dotychczas gdy EF nie umiał wykonać konwersji LINQ na SQL - kwerenda wykonywała się częściowo po stronie klienckiej. Najbardziej znany przykład do GROUP BY do wersji 2.1. Od wersji 3.0 w takiej sytuacji, będzie wyjątek w domyślnych ustawieniach.
2. Funkcja `FromSQL` będzie zamieniona na `FromSqlRaw` i `FromSqlInterpolated`, by uniknąć niechcianych SQL injection
3. 