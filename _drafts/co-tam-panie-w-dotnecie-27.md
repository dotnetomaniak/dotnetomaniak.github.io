---
layout: post
title: 'Co tam Panie w dotnecie? #27'
date: 2019-10-20 22:00:00 +0000
header-img: ''

---
27 podsumowanie tygodnia. W tym tygodniu najważniejszy news to cytat z JetBrains:

> But if the results are normalized by sample size, C# is the most loved language

Sorry F# i VB.NET. Takie życie. No to jedziemy z koksem :)

## Skąd cytat?

Jak co roku JetBrains zaprasza do ankiety deweloperów z całego świata. W tym roku w ankiecie wzięło udział 7000 deweloperów. Czego się nauczyli (poza tym że C# to najbardziej kochany język programowania)? Aż ciężko podsumować, ale na pewno warto przejrzeć: [https://www.jetbrains.com/lp/devecosystem-2019/](https://www.jetbrains.com/lp/devecosystem-2019/ "https://www.jetbrains.com/lp/devecosystem-2019/")

## NET Core <3 Docker (i działa)

Jeżeli używacie NET Core na Linux to wreszcie w trybie Server GC nie będzie on kradł mega dużo pamięci. A no i możecie wprowadzić też limit na CPU :)

Przy okazji dowcip ze świata Java. W JVM liczba CPU przekłada się na liczbę wątków. Ponieważ do Java 11 nie działały ograniczenia na CPU, tak jak w dotnet nie działały limity na RAM, to nagły upgrade do 11 w pewnej firmie spowodował mały stop na produkcji. 

Więcej w temacie (+ obrazy do docker): [https://devblogs.microsoft.com/dotnet/using-net-and-docker-together-dockercon-2019-update/](https://devblogs.microsoft.com/dotnet/using-net-and-docker-together-dockercon-2019-update/ "https://devblogs.microsoft.com/dotnet/using-net-and-docker-together-dockercon-2019-update/")