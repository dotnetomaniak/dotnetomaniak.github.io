---
layout: post
title: 'Co tam Panie w dotnecie? #23'
date: 2019-07-14 22:00:00 +0000
header-img: "/images/content/ross-findon-mG28olYFgHI-unsplash.jpg"

---
Podsumowanie świata dotnet - edycja 23. Wakacje w pełni, a na świecie cały czas coś się dzieje. Aż czasem żałuję, że nie mogę napisać: w tym tygodniu zawiało nudą i w sumie to nie mam co pisać. No dobra po marudziłem, czas do pracy. Jedziemy z koksem!

## .NET 5.0

To że będzie wszyscy wiem, ale jak co i dlaczego - to chyba pytania, które pojawiają się w głowach .NET devów. Z jednej strony mamy przecież świat tzw. tradycyjny z pełnym NET Framework, z drugiej nowe dziecko czyli NET Core. A NET pięć-zero ma za zadanie połączyć  oba światy - w sumie to ciekawy czy wyjdzie mutant jak w X-men czy raczej jak straszą z Czarnobyla.

Wstęp trochę przy długi a artykułu polecam dwa:

1. [.NET Reunified: Microsoft’s Plans for .NET 5 ](https://msdn.microsoft.com/en-us/magazine/mt833477.aspx)- w skrócie to zestaw odpowiedzi "dlaczego" i "po co"
2. [Future of .NET (.NET 5?) — Microsoft Build 2019 from a .NET developer point of view](https://medium.com/capgemini-dynamics-365-team/future-of-net-net-5-microsoft-build-2019-from-a-net-developer-point-of-view-7a1158fb0691) - krótkie uzupełnienie powyższego (lub wstęp jak kto woli)

## SQL Server 2019 na Linux jest ....

Ciekaw jestem jakie słowo pomyśleliście - jak możecie zostawcie w komentarzu.

A teraz prawda: szybszy. I twierdzi to MS we współpracy z RedHat. I choć brzmi to jak dowcip prima aprilis, to tak nie jest. Wystarczy obejrzeć PDF ze strony: [https://clouddamcdnprodep.azureedge.net/gdc/gdcaEDCeI/original](https://clouddamcdnprodep.azureedge.net/gdc/gdcaEDCeI/original "https://clouddamcdnprodep.azureedge.net/gdc/gdcaEDCeI/original"), a szczegóły odnajdziecie w artykule: [https://www.redhat.com/en/blog/microsoft-red-hat-and-hpe-collaboration-delivers-choice-value-enterprise-customers](https://www.redhat.com/en/blog/microsoft-red-hat-and-hpe-collaboration-delivers-choice-value-enterprise-customers "https://www.redhat.com/en/blog/microsoft-red-hat-and-hpe-collaboration-delivers-choice-value-enterprise-customers")

Zysk 6% to naprawdę DUŻO! A przy Linux (oczywiście nie Red Hat) są spore szanse na obniżenie kosztów :)

Jak już jesteśmy w tematyce SQL Server to jeszcze polecę Wam dwa linki:

1. [SQL Server 2019: Features for the Rest of Us](https://www.red-gate.com/simple-talk/opinion/editorials/sql-server-2019-features-for-the-rest-of-us/) - jak nazwa sama wskazuje, kilka przydatnych drobiazgów, które mogą się nam przydać w pracy
2. [One specific query runs slower in Azure DB than on-premises SQL Server?!](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/One-specific-query-runs-slower-in-Azure-DB-than-on-premises-SQL/ba-p/751165) - choć może pytanie które Was nie interesuje, to w odpowiedzi mamy "check-listę" rzeczy do sprawdzenia przy diagnostyce, dlaczego kwerenda na jednym środowisku jest szybsza niż na drugim

## Jak działa R# i dlaczego tak ...

R# ma zwolenników i przeciwników, jak wszystko z resztą :) Natomiast poczytanie o tym dlaczego jest tak wolny/szybki (w zależności od Twoich upodobań skreśl jedno), jest warte poczytania, gdyż mamy kawałek porządnego software.

Całość dotyczy w dużej mierze Rider, czyli uruchomiania ReSharper "obok". Więcej już nie spoileruję i zapraszam do artykułu [Long read: Where we are with “out of process” ReSharper](https://blog.jetbrains.com/dotnet/2019/07/11/where-we-are-with-out-of-process-resharper/)

## Jak Regex zabił pół Internetu

Jeżeli dwa tygodnie temu mieliście problem z dostępem do stron internetowych (dokładnie 2 lipca), to mogło być to "potknięcie" CloudFlare. Całość to zbyt zasobożerny regex i brak testów. Więcej w [Details of the Cloudflare outage on July 2, 2019](https://blog.cloudflare.com/details-of-the-cloudflare-outage-on-july-2-2019/). Jest też wersja polska opisu jak ktoś woli: [._(?:._=.*))) zabiło całe Cloudflare. Przerywamy spotkanie! Wszystkie ręce do konsol!](https://sekurak.pl/zabilo-cale-cloudflare-przerywamy-spotkanie-wszystkie-rece-do-konsol/)

Przy okazji przypomniał się stary dowcip: Niektórzy programiści gdy mają problem, wpadają na pomysł użycia wyrażeń regularnych. Od tego momentu mają dwa problemy.

A na temat tego dowcipu kiedyś został opublikowany bardzo dobry artykuł: [https://blog.codinghorror.com/regular-expressions-now-you-have-two-problems/](https://blog.codinghorror.com/regular-expressions-now-you-have-two-problems/ "https://blog.codinghorror.com/regular-expressions-now-you-have-two-problems/")

## Mały kącik wydajności

Krótko bo tylko jeden artykuł, ale za to jaki. Tematyka znana od zarania dziejów czyli: for vs. foreach w dotnet:

* [Performance Tip: for vs. foreach in Microsoft .NET](https://dotnettips.wordpress.com/2019/07/08/performance-tip-for-vs-foreach-in-microsoft-net/)

## Gra dla dotnetomaniaków

Konrad Kokosa udostępnił swoją grę do wydruku i grania w domu. Mówiąc szczerze sam by zagrał, ale nie mam z kim. Polecam serdecznie, szczególnie że przy okazji można też spróbować IT Startup Mateusza Kupilasa: [http://tooslowexception.com/outofmemory-and-it-startup-card-game-prototypes-available/](http://tooslowexception.com/outofmemory-and-it-startup-card-game-prototypes-available/ "http://tooslowexception.com/outofmemory-and-it-startup-card-game-prototypes-available/")

A jak już jesteśmy w tematyce dotnetomaniaków, to zapraszam na podsumowanie tygodnia dotnetomaniaka: [https://dotnetomaniak.pl/weekly/2019/28](https://dotnetomaniak.pl/weekly/2019/28 "https://dotnetomaniak.pl/weekly/2019/28"). Przy okazji otworzyliśmy ponownie nasz sklep z gadżetami: [http://dotnetomaniak.cupsell.pl/](http://dotnetomaniak.cupsell.pl/ "http://dotnetomaniak.cupsell.pl/") - dochód idzie na cele charytatywne. Jakie? O tym w przyszłości :)