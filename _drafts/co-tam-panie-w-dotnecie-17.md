---
layout: post
title: 'Co tam Panie w dotnecie? #17'
date: 2019-06-02 22:00:00 +0000
header-img: ''

---
17 edycja podsumowania ze świata dotnet. Krótko i treściwie, akurat na przerwę.

## Tydzień dotnetomaniaka

Zacznijmy od polskiej blogosfery dotnetowej. W tym tygodniu 10 artykułów. Jest co czytać, więc zapraszam serdecznie: [https://dotnetomaniak.pl/weekly/2019/22](https://dotnetomaniak.pl/weekly/2019/22 "https://dotnetomaniak.pl/weekly/2019/22")

## FindRef czyli jak odszukać referencję

Raz na jakiś czas potrzebujemy na szybko sprawdzić, w którym projekcie używana jest dana biblioteka. Na pomoc spieszy małe narzędzie czyli FindRef. Instalacja banalna: `dotnet tool install --global findref`, a użycie: `dotnet tool install --global findref`. Więcej opcji i szczegółów: [https://hjerpbakk.com/blog/2019/05/27/findref](https://hjerpbakk.com/blog/2019/05/27/findref "https://hjerpbakk.com/blog/2019/05/27/findref")

## Szybki NullCheck

Co ja Wam będę pisał. Lepiej spójrzcie na tweeta: [https://twitter.com/RicoSuter/status/1133241761621598209](https://twitter.com/RicoSuter/status/1133241761621598209 "https://twitter.com/RicoSuter/status/1133241761621598209"). Całość kodu wygląda super:

    using System;
    public class C 
    {
        public void Foo(string bar)
        {
            _ = bar ?? throw new ArgumentNullException(nameof(bar));
        }
    }

A całość po kompilacji dostępna jest na [sharlab.io](https://sharplab.io/#v2:CYLg1APgAgTAjAWAFBQMwAJboMLuQb2XWMwygBZ0AxAexoAoo4AGdAIwEMAnASiJMJISw9AH10AXnbd0AflnoALgAsuNAO7oAdgFNNAQS4BzAK4BbHVsUA5EwBs7AUQAeAYx0AHRQEsaW+locFjQAZvScvDwA3PzEAL7IcUA)

## Desktop i .NET Core

Chyba pierwszy tak kompleksowy artykuł na temat portowania aplikacji Windows z .NET Framework na .NET Core. Krok po kroku, nawet z opisem jak naprawiać błędy. Dla chętnych też video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/upVQEUc_KwU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

A artykuł dostępny pod adresem: [https://devblogs.microsoft.com/dotnet/porting-desktop-apps-to-net-core/](https://devblogs.microsoft.com/dotnet/porting-desktop-apps-to-net-core/ "https://devblogs.microsoft.com/dotnet/porting-desktop-apps-to-net-core/")

## 2 tematy z od śmieciarzy

Dwa tematy związane z GC dla prawdziwych fanów ;)

1. [8 Techniques to Avoid GC Pressure and Improve Performance in C# .NET](https://michaelscodingspot.com/avoid-gc-pressure/)
2. [Spying on .NET Garbage Collector with .NET Core EventPipes](https://medium.com/criteo-labs/spying-on-net-garbage-collector-with-net-core-eventpipes-9f2a986d5705)

## A czy USA może zablokować open-source?

Po "Trump ban" dość ciekawy problem. Ale jak to zapytacie? No więc Github należy do MS, a MS jest firmą amerykańską i podlega. Dla zainteresowanych więcej : [US might have control of Open Source](https://www.fudzilla.com/news/48769-us-might-have-control-of-open-source)

## Czy jeszcze Win10 czy już może nie?

Ptaszki od jakiegoś czasu ćwierkają, że MS tworzy nowy system operacyjny typu Lite, określanego już oficjalnie jako Modern OS. Pytanie co Windows 10? Na ten moment to gracz innej ligi, który raczej ma konkurować z Chrome OS niż z pełnym systemem operacyjnym. Ale co wyjdzie z tego? Pożyjemy zobaczymy. Więcej: [https://www.spidersweb.pl/2019/05/microsoft-modern-os.html](https://www.spidersweb.pl/2019/05/microsoft-modern-os.html "https://www.spidersweb.pl/2019/05/microsoft-modern-os.html")