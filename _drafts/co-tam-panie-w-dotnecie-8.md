---
layout: post
title: 'Co tam Panie w dotnecie? #8'
date: 2019-03-31 22:00:00 +0000
header-img: ''

---

## News tygodnia

Pierwszy kwietnia, więc pewnie nie dacie wiary. Chociaż news z poprzedniego tygodnia, więc może się uda: oficjalnie Kubernetes 1.14 wspiera Windows Containers. Serio, nie żartuję. Nim zaczniecie tańczyć z radości to żeby było jasne: nie ma jeszcze pełnego wsparcia z support dla Windows Containers, ale wygląda na to że projekt coraz bliżej brzegu.

Więcej o nowości: [https://kubernetes.io/blog/2019/03/25/kubernetes-1-14-release-announcement/](https://kubernetes.io/blog/2019/03/25/kubernetes-1-14-release-announcement/ "https://kubernetes.io/blog/2019/03/25/kubernetes-1-14-release-announcement/")

## SpecFlow 3

SpecFlow w wersji 3 już jest. Z pełnym wsparciem dla .NET Core, co oznacza brak upierdliwych pluginów do IDE, żeby to działało. Jeżeli nigdy nie pisaliście testów biznesowych/E2E w sposób zrozumiały dla osoby bez wiedzy programistycznej, to pewnie o narzędziu nie słyszeliście. Ja jednak się do niego przekonałem i strasznie się cieszę że będziemy mogli na naszych testach dokonać "upgrade".

Release notes: [https://specflow.org/2019/specflow-3-is-here/](https://specflow.org/2019/specflow-3-is-here/ "https://specflow.org/2019/specflow-3-is-here/")

## UriHelper "lekko" mniej pamięciożerny

Znów PR a nie prawdziwy artykuł, ale wiadomo kod czyta się łatwiej ;) 

Dzięki "drobnej" zmiana w podanym przykładzie udało się zejść z \~630GB do \~22MB (tak GB i MB) co przy okazji przełożyło się na zysk czasu z \~14s do \~0.05s.

Ale to nie jest najważniejsze w tym PR. Przy okazji zostało pokazane jak zostało to zrobione, a to już naprawdę warte świeczki (i przeczytania). Całość: [https://github.com/dotnet/corefx/pull/36056](https://github.com/dotnet/corefx/pull/36056 "https://github.com/dotnet/corefx/pull/36056")

## AutoMapper's Design Philosophy

Jimmy Bogard po raz kolejny. Tym razem wyjaśnia do czego i po co służy AutoMapper. Naprawdę warto wiedzieć niż używać go bez sensu:

[https://jimmybogard.com/automappers-design-philosophy/](https://jimmybogard.com/automappers-design-philosophy/ "https://jimmybogard.com/automappers-design-philosophy/")