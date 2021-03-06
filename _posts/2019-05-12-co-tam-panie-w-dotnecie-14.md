---
layout: post
title: 'Co tam Panie w dotnecie? #14'
date: 2019-05-12 22:00:00 +0000
header-img: "/images/content/randy-fath-531056-unsplash.jpg"

---
W tym tygodniu za nami MS Build, ale ponieważ wszyscy już "wszystko" widzieli to w tym temacie raczej nietypowo w formie ciekawostek.

## No to Build

Na buildzie dużo nowości chociaż bardziej poprawnie będzie zapowiedzi.. Pełny wykaz sesji do obejrzenia jest dostępny: [https://mybuild.techcommunity.microsoft.com/sessions](https://mybuild.techcommunity.microsoft.com/sessions "https://mybuild.techcommunity.microsoft.com/sessions") (oraz w formie YouTube:[https://www.youtube.com/playlist?list=PLlrxD0HtieHgspNIlv1x2H5_cxSRm7B17](https://www.youtube.com/playlist?list=PLlrxD0HtieHgspNIlv1x2H5_cxSRm7B17 "https://www.youtube.com/playlist?list=PLlrxD0HtieHgspNIlv1x2H5_cxSRm7B17")), a jak nie chce Wam się szukać samemu najciekawszych to "top" dostępny jest tutaj: [https://devblogs.microsoft.com/devops/top-stories-from-microsoft-build-2019-05-10/](https://devblogs.microsoft.com/devops/top-stories-from-microsoft-build-2019-05-10/ "https://devblogs.microsoft.com/devops/top-stories-from-microsoft-build-2019-05-10/")

## Nowy terminal

Cały świat zachwyca się nowym terminalem, ale na razie to powiem szczerze do niczego się on nie nadaje. Projekt w wersji "jeszcze totalnie prawie nic nie ma". Próbowałem go uruchomić i dopiero VM postawione na Azure pomogło. Jak ktoś chciałby binarki to rozczaruję - u mnie lokalnie nie działa.

## Przyszłość .NET

.NET 5.0 ([https://devblogs.microsoft.com/dotnet/introducing-net-5/](https://devblogs.microsoft.com/dotnet/introducing-net-5/ "https://devblogs.microsoft.com/dotnet/introducing-net-5/"))- kolejna nowość, z której ma połączyć wszystko. Myślałem że to miał zrobić .NET Standard a tu proszę jednak nie. Widać że jest problem z połączeniem światów NET Framework i NET Core, bo jednak piszą że [NET Core is the future](https://devblogs.microsoft.com/dotnet/net-core-is-the-future-of-net/). Trochę to tak jak by zjeść ciastko i mieć ciastko. Ech ....

## Nowości w Visual Studio

Jakiś czas temu VisualStudioOnline zmieniło nazwę na Azure DevOps. Dwa słowa klucze: Azure i DevOps, wydawało mi się, że to zmiana podyktowana dla szczęścia i radości marketingu. A jednak ten rebranding umożliwił zrobienie miejsca dla "prawdziwego" Visual Studio Online. Wedle doniesień będzie ono oparte na VS Code i dostępne pod adresem: [https://online.visualstudio.com](https://online.visualstudio.com "https://online.visualstudio.com") (na razie jest tam tylko wpis na ten temat)

## Nowy SqlClient

Nowość, która umknęła w gąszczu zapowiedzi. Pojawia się nowy SqlClient w pełni open-source: [https://devblogs.microsoft.com/dotnet/introducing-the-new-microsoftdatasqlclient](https://devblogs.microsoft.com/dotnet/introducing-the-new-microsoftdatasqlclient "https://devblogs.microsoft.com/dotnet/introducing-the-new-microsoftdatasqlclient")

Do tego też nowy EnitiyFramework 6.3 mający wsparcie dla NET Core. Czyli połączenie rozłączonych braci i wygląda na to, że od NET Core 3.0 przestaniemy mieć EF i EF.Core

## Inspect.Allocations

Na Sharplab.io pojawiała się nowa funkcjonalność: `Inspect.Allocations`. Niby proste a jednak bardzo fajne narzędzie. Co więcej jeszcze w wersji "niestabilnej" bo krzyczy na nas ostrzeżenie. Przykład w działaniu: [https://sharplab.io/#gist:5dd52b497575ec1f24a46f6c9287e144](https://sharplab.io/#gist:5dd52b497575ec1f24a46f6c9287e144 "https://sharplab.io/#gist:5dd52b497575ec1f24a46f6c9287e144")

## Tydzień dotnetomaniaka

A na dotnetomaniaku klika bardzo ciekawych artykułów z zeszłego tygodnia. 12 artykułów, zero builda. Polecam zajrzeć: [https://dotnetomaniak.pl/weekly/2019/19](https://dotnetomaniak.pl/weekly/2019/19 "https://dotnetomaniak.pl/weekly/2019/19") i jestem przekonany, że znajdziesz coś dla siebie.