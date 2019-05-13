---
layout: post
title: 'Co tam Panie w dotnecie? #14'
date: 2019-05-12 22:00:00 +0000
header-img: ''

---
W tym tygodniu za nami MS Build, ale ponieważ wszyscy już "wszystko" widzieli to w tym temacie krótko i raczej nietypowo. Poza tym kilka ciekawostek.

## No to Build

Na buildzie dużo nowości chociaż bardziej poprawnie będzie zapowiedzi.. Pełny wykaz sesji do obejrzenia jest dostępny: [https://mybuild.techcommunity.microsoft.com/sessions](https://mybuild.techcommunity.microsoft.com/sessions "https://mybuild.techcommunity.microsoft.com/sessions")

Cały świat zachywca się nowym terminalem, ale na razie to powiem szczerze do niczego się on nie nadaje. Projekt w wersji "jeszcze totalnie prawie nic nie ma". Próbowałem go uruchomić i dopiero VM postawione na Azure pomogło. Jak ktoś chciałby binarki to rozczaruję - u mnie lokalnie nie działa.

.NET 5.0 ([https://devblogs.microsoft.com/dotnet/introducing-net-5/](https://devblogs.microsoft.com/dotnet/introducing-net-5/ "https://devblogs.microsoft.com/dotnet/introducing-net-5/"))- kolejna nowość, z której ma połączyć wszystko. Myślałem że to miał zrobić .NET Standard a tu proszę jednak nie. Widać że jest problem z połączeniem światów NET Framework i NET Core, bo jednak piszą że [NET Core is the future](https://devblogs.microsoft.com/dotnet/net-core-is-the-future-of-net/). Trochę to tak jak by zjeść ciastko i mieć ciastko. Ech ....

## Nowy SqlClient

Nowość, która umknęła w gąszczu zapowiedzi. Pojawia się nowy SqlClient w pełni open-source: [https://devblogs.microsoft.com/dotnet/introducing-the-new-microsoftdatasqlclient](https://devblogs.microsoft.com/dotnet/introducing-the-new-microsoftdatasqlclient "https://devblogs.microsoft.com/dotnet/introducing-the-new-microsoftdatasqlclient")

Do tego też nowy EnitiyFramework 6.3 mający wsparcie dla NET Core. Czyli połączenie rozłączonych braci i wygląda na to, że od NET Core 3.0 przestaniemy mieć EF i EF.Core

## Inspect.Allocations

Na Sharplab.io pojawiała się nowa funkcjonalność: `Inspect.Allocations`. Niby proste a jednak bardzo fajne narzędzie. Co więcej jeszcze w wersji "niestabilnej" bo krzyczy na nas ostrzeżenie. Przykład w działaniu: [https://sharplab.io/#gist:5dd52b497575ec1f24a46f6c9287e144](https://sharplab.io/#gist:5dd52b497575ec1f24a46f6c9287e144 "https://sharplab.io/#gist:5dd52b497575ec1f24a46f6c9287e144")