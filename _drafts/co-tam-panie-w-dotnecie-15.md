---
layout: post
title: 'Co tam Panie w dotnecie? #15'
date: 2019-05-19 22:00:00 +0000
header-img: ''

---
Piekło zamarzło. Ostatnio nadużywam tego określenia, podobnie jak Microsoft określa wszystko jako przełomowe. Cóż zapraszam Cię do 15 podsumowania tygodnia w świecie .NET

## Tydzień dotnetomaniaka

13 jest pechowa, ale nie tym razem. W zeszłym tygodniu na dotnetomaniaku opublikowano aż 13 artykułów. Jest z czego czerpać wiedzę, więc zapraszam Cię serdecznie do kliknięcia i poczytania: [https://dotnetomaniak.pl/weekly/2019/20](https://dotnetomaniak.pl/weekly/2019/20 "https://dotnetomaniak.pl/weekly/2019/20")

## Msbuild raz jeszcze

Parę podsumowań MsBuild już jest na przykład u [programmer-girl]() (skrót najważniejszych wiadomości) czy [Tomasza Wiśniewskiego](https://tomaszwisniewski.com/build/conference/event/build-2019-recap.html) (tu warto przeczytać które sesje obejrzeć). Jeżeli jednak potrzebujecie "indeksu" to dostępny jest oficjalny ebook ze wszystkimi wiadomościami: [https://news.microsoft.com/wp-content/uploads/prod/sites/558/2019/05/FINAL-Book-of-News-Build-2019.pdf](https://news.microsoft.com/wp-content/uploads/prod/sites/558/2019/05/FINAL-Book-of-News-Build-2019.pdf "https://news.microsoft.com/wp-content/uploads/prod/sites/558/2019/05/FINAL-Book-of-News-Build-2019.pdf") - w sumie 64 strony ze wszystkim co zostało ogłoszone :)

## Dlaczego Bing jest "inteligentny"?

Jeżeli ciekawi Cię w jaki sposób wyszukiwarka Bing umie zinterpretować pytanie: "jak wysoki jest pałac kultury i nauki?" to mam coś dla Ciebie. Microsoft opublikował właśnie jako open-source swój algorytm o nazwie SPTAG ("Space Partition Tree and Graph"). Po więcej informacji można sięgnąć w 3 miejsca:

* zajawka - [https://arstechnica.com/gadgets/2019/05/microsoft-open-sources-algorithm-that-gives-bing-some-of-its-smarts/](https://arstechnica.com/gadgets/2019/05/microsoft-open-sources-algorithm-that-gives-bing-some-of-its-smarts/ "https://arstechnica.com/gadgets/2019/05/microsoft-open-sources-algorithm-that-gives-bing-some-of-its-smarts/")
* pełny artykuł [https://blogs.microsoft.com/ai/bing-vector-search/](https://blogs.microsoft.com/ai/bing-vector-search/ "https://blogs.microsoft.com/ai/bing-vector-search/")
* źródła na Github - [https://github.com/microsoft/SPTAG](https://github.com/microsoft/SPTAG "https://github.com/microsoft/SPTAG")

## Co jest nie tak z moją aplikacją

Bardzo przydatny zestaw artykułów z cyklu jak diagnozować co jest nie tak z aplikacją w .NET Core. Kilka konkretnych scenariuszy (memory leak, slow, hanging, momry spikes) wraz z demo. Życzę sobie i Wam żeby ta wiedza nigdy się nie przydała, ale wiedzieć warto. Całość na github: [https://github.com/dotnet/diagnostics/tree/master/documentation/tutorial](https://github.com/dotnet/diagnostics/tree/master/documentation/tutorial "https://github.com/dotnet/diagnostics/tree/master/documentation/tutorial")

## Wydajność i wydajność

W tym tygodniu dwa artykuły o wydajności. Jak zwykle "edge cases", ale poczytać warto:

* [Creating Strings with No Allocation Overhead Using String.Create](https://www.stevejgordon.co.uk/creating-strings-with-no-allocation-overhead-using-string-create-csharp)
* [Performance Improvements in .NET Core 3.0](https://devblogs.microsoft.com/dotnet/performance-improvements-in-net-core-3-0)

## Umbraco idzie w kierunku .NET Core

Nie wiem czy znacie ten CMS, ale jest w 100% napisany w .NET i wygląda na to że powoli zmierza do migracji na .NET Core:
<blockquote class="twitter-tweet" data-lang="en-gb"><p lang="en" dir="ltr">Plans for moving to .NET Core being discussed at the <a href="https://twitter.com/hashtag/cgretreat?src=hash&ref_src=twsrc%5Etfw">#cgretreat</a> <a href="https://twitter.com/hashtag/codegarden?src=hash&ref_src=twsrc%5Etfw">#codegarden</a> <a href="https://twitter.com/hashtag/umbraco?src=hash&ref_src=twsrc%5Etfw">#umbraco</a> <a href="https://t.co/gU9ZAKrvjB">pic.twitter.com/gU9ZAKrvjB</a></p>— Niels Hartvig (@thechiefunicorn) <a href="https://twitter.com/thechiefunicorn/status/1130065816978939904?ref_src=twsrc%5Etfw">19 May 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## Piekło zamarzło część 1 - interfejsy

Możliwość implementacji ciała metody w interfejsie właśnie stała się faktem. Czy to dobrze czy źle - ciężko mi ocenić, ale sporo pytań rekrutacyjnych szlag trafiło ;)

Nie mam co się wywnętrzać tylko zapraszam do kliknięcia: [https://devblogs.microsoft.com/dotnet/default-implementations-in-interfaces/](https://devblogs.microsoft.com/dotnet/default-implementations-in-interfaces/ "https://devblogs.microsoft.com/dotnet/default-implementations-in-interfaces/")

## Piekło zamarzło część 2 - Windows Containers

Jak wiecie interesuję się Kubernetesem - zawodowo i prywatnie. Tak samo kontenerami - kocham i nienawidzę jednocześnie. Myślałem, że Microsoft odpuści, szczególnie gdy wpadł mi w ręce [commit z przed 2 tygodni](https://github.com/MicrosoftDocs/azure-docs/commit/0e0a57467efb91c029083ecabfb16b8af091f437) do dokumentacji Azure Kubernetes Service (AKS). Ale jednak się myliłem - na AKS pojawiło się publiczne preview dla kontenerów Windows. W pełni oficjalnie:

[https://azure.microsoft.com/en-us/blog/announcing-the-preview-of-windows-server-containers-support-in-azure-kubernetes-service/](https://azure.microsoft.com/en-us/blog/announcing-the-preview-of-windows-server-containers-support-in-azure-kubernetes-service/ "https://azure.microsoft.com/en-us/blog/announcing-the-preview-of-windows-server-containers-support-in-azure-kubernetes-service/")