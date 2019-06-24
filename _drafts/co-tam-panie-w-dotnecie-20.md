---
layout: post
title: 'Co tam Panie w dotnecie? #20'
date: 2019-06-23 22:00:00 +0000
header-img: "/images/content/bernard-hermant-624964-unsplash.jpg"

---
Dotrwaliśmy do 20 edycji podsumowania tygodnia. W związku z jubileuszem kilka bomb wewnętrznych i zewnętrznych. Zaczynamy za 3...2..1..JUŻ!

## Nowy dotnetomaniak

[Mateusz Wiatrzyk](https://www.linkedin.com/in/mateusz-wiatrzyk-91637516b/) wykonał dużą pracę u podstaw naszego portalu. Zrobił upgrade większości bibliotek frontendowych oraz "ułożył" portal jeszcze raz używając Bootstrap. Dana wydania nowego portalu to 21:37 w środę przed długim weekendem. Choć mówi się że nie robi się release tuż przed weekendem, akurat w tym przypadku termin idealny - mniejszy ruch, obaj mieliśmy więcej czasu, itd.

Nie pozostało mi nic innego jak zaprosić Was na nową odsłonę: [https://dotnetomaniak.pl](http://dotnetomaniak.pl "http://dotnetomaniak.pl") i mam szczerą nadzieję, że poza widokiem mobile nie zauważycie dużej różnicy.

Przy okazji dotnetomaniak to już 404 strony. Jeżeli jesteś ciekaw co jest na ostatniej, a w zasadzie pierwszej to zapraszam: [https://dotnetomaniak.pl/404](https://dotnetomaniak.pl/404 "https://dotnetomaniak.pl/404")

## Jak ewoluowała infrastruktura build NET Core

Niesamowity artykuł, choć mięsa trochę w nim brakuje. Pełna ewolucja jak powstawały repozytoria NET Core i jak ich "build" został zoptymalizowany. Jeżeli macie dużą solucję, którą budujecie na raz to można się zainspirować (chociaż trochę) jak zrobić to lepiej (albo chociaż inaczej). Ponieważ w kilku zdaniach tego artykułu streścić się nie da to zapraszam do źródła: [https://devblogs.microsoft.com/dotnet/the-evolving-infrastructure-of-net-core/](https://devblogs.microsoft.com/dotnet/the-evolving-infrastructure-of-net-core/ "https://devblogs.microsoft.com/dotnet/the-evolving-infrastructure-of-net-core/")

Przy okazji też dowód na to że twórcy dotnet są tacy sami jak my:
<blockquote class="twitter-tweet" data-lang="en-gb"><p lang="en" dir="ltr">1. Rename some tests<br>2. Some tests start failing<br>3. Run the failing tests alone works...<br>4. Spend hours debugging<br>5. Discover renaming the test caused them to run in an order that fails<br>6. There's shared mutable state somewhere... <a href="https://t.co/3h8Jd8ml5m">pic.twitter.com/3h8Jd8ml5m</a></p>— David Fowler (@davidfowl) <a href="https://twitter.com/davidfowl/status/1142618508561244160?ref_src=twsrc%5Etfw">23 June 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## Nowa konsola już jest

Udało mi się zainstalować nową konsolę od Microsoft. Na moim komputerze wygląda ona tak:

![](/images/content/cmd.png)

Mówiąc szczerze to instalacja była dłuuuuggggaaaaa, ale jak widać zakończyła się szczęśliwie. Obiecuję, że napiszę o tym więcej następnym razem.

Jeżeli chcesz zacząć sam (i spełniasz wymagania) to link do sklepu Windows jest: [https://www.microsoft.com/pl-pl/p/windows-terminal-preview/9n0dx20hk701?activetab=pivot:overviewtab](https://www.microsoft.com/pl-pl/p/windows-terminal-preview/9n0dx20hk701?activetab=pivot:overviewtab "https://www.microsoft.com/pl-pl/p/windows-terminal-preview/9n0dx20hk701?activetab=pivot:overviewtab"), a jeżeli chcesz przeczytać więcej to [https://devblogs.microsoft.com/commandline/windows-terminal-microsoft-store-preview-release/](https://devblogs.microsoft.com/commandline/windows-terminal-microsoft-store-preview-release/ "https://devblogs.microsoft.com/commandline/windows-terminal-microsoft-store-preview-release/")

## Wydajność w konwersji Guid na Base64 

Steve Grodon jak zwykle w formie. Tym razem postanowił pochylić się nad poniższym kodem:

    Convert.ToBase64String(_guid.ToByteArray()).Replace("/", "-").Replace("+", "_").Replace("=", "")

Co z tego wynikło? Nie pozostaje Ci nic innego jak sprawdzić samemu: [https://www.stevejgordon.co.uk/using-high-performance-dotnetcore-csharp-techniques-to-base64-encode-a-guid](https://www.stevejgordon.co.uk/using-high-performance-dotnetcore-csharp-techniques-to-base64-encode-a-guid "https://www.stevejgordon.co.uk/using-high-performance-dotnetcore-csharp-techniques-to-base64-encode-a-guid")

p.s. Spoiler: Kod na pewno krótszy nie będzie 

## Kryptografia w .NET

Pełny opis (chyba) wszystkich rodzajów typów odpowiedzialnych za kryptografie w .NET. Co najważniejsze z rysunkami co jest czym. Jeżeli przygotowujesz się do rozmowy kwalifikacyjnej z tematyki .NET to na warto zajrzeć: [https://www.meziantou.net/cryptography-in-dotnet.htm](https://www.meziantou.net/cryptography-in-dotnet.htm "https://www.meziantou.net/cryptography-in-dotnet.htm")

## JWT i mapowanie

Przy okazji trafiłem na krótki, ale treściwy artykuł na temat mapowania claim w JWT w NET Core. Rok temu dałbym się za niego zastrzelić. Teraz wiedziałem już wszystko. Ale mam nadzieję, że Tobie się przyda i nie będziesz zrzucał mięsem jak ja, szukając jak to zrobić. Bo sama robota to 5 minut: [https://mderriey.com/2019/06/23/where-are-my-jwt-claims/](https://mderriey.com/2019/06/23/where-are-my-jwt-claims/ "https://mderriey.com/2019/06/23/where-are-my-jwt-claims/")

## Tydzień dotnetomaniaka

Jeżeli link do strony głównej Cię nie skusił to może chociaż podsumowanie tygodnia Cię zachęci. Dużo się nie działo - wiadomo długi weekend, ale 7 artykułów jest. Przy okazji polecam serię o Code reviews, która bardzo wpadła mi w oko: [https://dotnetomaniak.pl/weekly/2019/25](https://dotnetomaniak.pl/weekly/2019/25 "https://dotnetomaniak.pl/weekly/2019/25")