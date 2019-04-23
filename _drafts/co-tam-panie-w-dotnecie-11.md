---
layout: post
title: 'Co tam Panie w dotnecie? #11'
date: 2019-04-22 22:00:00 +0000
header-img: ''

---
11 tydzień lekko opóźniony, ale święta to święta i szkoda je przerywać

## dotnet core 3.0 preview 4

Data premiery coraz bliżej, pewnie nawet domyślacie się kiedy będzie (o ile nie jest to oficjalnie wiadome). Tym razem dołożono dodatki do WinForm oraz WPF. Wisienką na torcie jest update do Tiered Compilation.

[https://devblogs.microsoft.com/dotnet/announcing-net-core-3-preview-4/](https://devblogs.microsoft.com/dotnet/announcing-net-core-3-preview-4/ "https://devblogs.microsoft.com/dotnet/announcing-net-core-3-preview-4/")

## Blazor

Blazor wszedł w "official preview" - to już prawie stabilność jak service pack 2 do Windows XP. Nadal się boje, że rośnie drugi silverlight, a z drugiej storny cieszę się, na wszystkie możliwości wykorzystania WebAssembly. Więcej: [https://devblogs.microsoft.com/aspnet/blazor-now-in-official-preview/](https://devblogs.microsoft.com/aspnet/blazor-now-in-official-preview/ "https://devblogs.microsoft.com/aspnet/blazor-now-in-official-preview/")

A przykład użycia Blazor do budowy SPA można znaleźć tutaj: [https://exceptionnotfound.net/using-blazor-to-build-a-client-side-single-page-app-with-net-core/](https://exceptionnotfound.net/using-blazor-to-build-a-client-side-single-page-app-with-net-core/ "https://exceptionnotfound.net/using-blazor-to-build-a-client-side-single-page-app-with-net-core/")

## .NET Framework ma się dobrze

I właśnie wyszła jego nowa wersja: 4.8. Poprawki zawierają zmiany w obszarach:

* **\[Runtime\]** JIT and NGEN Improvements
* **\[BCL\]** Updated ZLib
* **\[BCL\]** Reducing FIPS Impact on Cryptography
* **\[WinForms\]** Accessibility Enhancements
* **\[WCF\]** Service Behavior Enhancements
* **\[WPF\]** High DPI Enhancements, UIAutomation Improvements

Więcej: [https://devblogs.microsoft.com/dotnet/announcing-the-net-framework-4-8/](https://devblogs.microsoft.com/dotnet/announcing-the-net-framework-4-8/ "https://devblogs.microsoft.com/dotnet/announcing-the-net-framework-4-8/")

## Dlaczego cieknie?

Ważne pytanie. 8 powodów, sensownie napisanych. Warto zerknąć czy którąś ze ścieżek sami nie użyliśmy: [https://michaelscodingspot.com/ways-to-cause-memory-leaks-in-dotnet/](https://michaelscodingspot.com/ways-to-cause-memory-leaks-in-dotnet/ "https://michaelscodingspot.com/ways-to-cause-memory-leaks-in-dotnet/")

## Tydzień dotnetomaniaka

Kolejny tydzień za nami, posty z wielu dziedzin. Idealne do kawy i mazurka. Polecam: [https://dotnetomaniak.pl/weekly/2019/16](https://dotnetomaniak.pl/weekly/2019/16 "https://dotnetomaniak.pl/weekly/2019/16")

## Zabawa na koniec

Nie do końca dotnet, bo SQL. Warto jednak zobaczyć czy pismo obrazkowe nadaje się do SQL.

    -- select the ratings for 'Example Book'
    SELECT 👤🏠📕.⭐
    FROM 👤🏠📕 JOIN 📕 ON 👤🏠📕.📕 = 📕.🔑
    WHERE 📕.💬 = 'Example Book';

UWAGA: powyższy kod działa, wystarczy zastosować się do porad z [http://baldi.me/blog/emoji-in-sql](http://baldi.me/blog/emoji-in-sql "http://baldi.me/blog/emoji-in-sql")