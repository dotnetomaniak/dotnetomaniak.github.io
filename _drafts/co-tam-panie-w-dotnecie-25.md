---
layout: post
title: 'Co tam Panie w dotnecie? #25'
date: 2019-09-15 22:00:00 +0000
header-img: ''

---
Edycja 25 jubileuszowa. Dziś dużo o migracjach, bo pewnie część z nas nie może się już doczekać na dotNET Core 3.0

## Migruj migruj migruj

Bardzo fajny artykuł jak krok po kroku Wałdis Iljuczonok (taki mniej znany Microsoft MVP) zrobił migrację jednego z Web Job w pełnym .NET Framework do dotNET Core.

Powoli, krok po kroku, więc można to przenieść na swój projekt o ile jeszcze nie próbowaliście: [https://blog.tech-fellow.net/2019/09/15/adding-di-package-to-webjobs-running-on-net-core/](https://blog.tech-fellow.net/2019/09/15/adding-di-package-to-webjobs-running-on-net-core/ "https://blog.tech-fellow.net/2019/09/15/adding-di-package-to-webjobs-running-on-net-core/")

Drugi artykuł to już migracja z 2.2 na 3.0. Jakość artykułu jak do na docs microsoft. Albo się lubi albo nie. Natomiast jak jesteście jeszcze przed (to na przykład ja) to na pewno się przyda Szczególnie sekcja "Json.NET support". Więcej: [https://docs.microsoft.com/en-us/aspnet/core/migration/22-to-30?view=aspnetcore-2.2&tabs=visual-studio](https://docs.microsoft.com/en-us/aspnet/core/migration/22-to-30?view=aspnetcore-2.2&tabs=visual-studio "https://docs.microsoft.com/en-us/aspnet/core/migration/22-to-30?view=aspnetcore-2.2&tabs=visual-studio")

Do tego na sam koniec w moim zdaniem bardziej przystępnej wersji porównanie kodu w _Startup.cs_ pomiędzy 2.2 a 3.0: [https://andrewlock.net/comparing-startup-between-the-asp-net-core-3-templates/](https://andrewlock.net/comparing-startup-between-the-asp-net-core-3-templates/ "https://andrewlock.net/comparing-startup-between-the-asp-net-core-3-templates/")

## A co z API?

Jak już jesteśmy w tematyce migracji to warto zerknąć na bibliotekę typu "utils" opisaną w artykule: [https://www.blogofpi.com/versioning-web-api/](https://www.blogofpi.com/versioning-web-api/ "https://www.blogofpi.com/versioning-web-api/") czyli Microsoft.AspNetCore.Mvc.Versioning.

Podoba mi się że wspiera wszystkie opcje, ale jak na Facebook zostało zauważone warto też przeczytać: [https://nordicapis.com/api-change-strategy/](https://nordicapis.com/api-change-strategy/ "https://nordicapis.com/api-change-strategy/") 