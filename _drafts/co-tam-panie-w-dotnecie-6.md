---
layout: post
title: 'Co tam Panie w dotnecie? #6'
date: 2019-03-16 23:00:00 +0000
header-img: ''

---
6 wydanie nowości ze świata dotnet

## A jednak książka o GC może się przydać

Chciałbym przyznać się do złej oceny. Uważałem, że książka Konrada Kokosy o [zarządzaniu pamięcią](https://prodotnetmemory.com) jest z gatunku ciekawostki, która może kiedyś mi się przyda. Wiecie taki błysk, że gdzieś tam coś zadzwoni i będę wiedział czego szukać. No więc to "kiedyś-gdzieś" trwało niecałe 2 tygodnie, od skończenia odpowiedniego rozdziału, bo książka jest jeszcze nie skończona (Kindle wskazuje 95%). A o co chodzi? O puszczanie dotnet w linux na dokerze. Jeżeli jesteś ciekawy to niestety w formie tweetów cała treść (link wskazuje na środek dyskusji bo miała za dużo wątków, a ten jest najciekawszy) [https://twitter.com/gutek/status/1105196689634312198](https://twitter.com/gutek/status/1105196689634312198 "https://twitter.com/gutek/status/1105196689634312198"). Jest tam kilka linków, które warto sobie przeczytać. Dla osób nie lubiących "twitera" poniżej kilka

* Troubleshooting high memory usage with ASP.NET Core on Kubernetes - [https://blog.markvincze.com/troubleshooting-high-memory-usage-with-asp-net-core-on-kubernetes/](https://blog.markvincze.com/troubleshooting-high-memory-usage-with-asp-net-core-on-kubernetes/ "https://blog.markvincze.com/troubleshooting-high-memory-usage-with-asp-net-core-on-kubernetes/")
* PR Determine memory load based on cgroup usage - [https://github.com/dotnet/coreclr/pull/19650](https://github.com/dotnet/coreclr/pull/19650 "https://github.com/dotnet/coreclr/pull/19650")
* .NET Core Docker Limits Test - [https://gist.github.com/richlander/48bb0ad51a2406937b61bea01de7cf87](https://gist.github.com/richlander/48bb0ad51a2406937b61bea01de7cf87 "https://gist.github.com/richlander/48bb0ad51a2406937b61bea01de7cf87")

Dla wszystkich, którzy bawią się na Linux, a za dużo pamięci zabiera im dotnet powyższe to lektura obowiązkowa.

## SOLID

Ostatnio jakoś temat znów popularny ;) A na serio, ciekawy rozwijający artykuł na temat jak SOLID ma się do ASP.NET Controllers czyli: [Visualizing thin ASP.NET Controllers via SOLID Principles](https://makingloops.com/visualizing-thin-controllers/)

## Czy umiesz używać async/awiat tak żeby było szybko?

Klasyczny problem który mamy to kod który wygląda tak:

    await FirstMethodAsync();
    await SecondMethodAsync();
    await ThirdMethodAsync();

I co dobrze jest? Dobrze bo działa. A mogłoby być lepiej? Ano mogło, a jak? Dla wszystkich którzy są ciekawi polecam: [Using async/await and Task.WhenAll to improve the overall speed of your C# code](https://jeremylindsayni.wordpress.com/2019/03/11/using-async-await-and-task-whenall-to-improve-the-overall-speed-of-your-c-code/)