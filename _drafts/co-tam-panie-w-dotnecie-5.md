---
layout: post
title: 'Co tam Panie w dotnecie? #5'
date: 2019-03-10 23:00:00 +0000
header-img: "/images/content/pablo (9)-1.png"

---
Najważniejsza wiadomość z tego tygodnia może być tylko jedna. Znalazłem wiele ciekawych tematów, ale król jest jeden. Chyba kiepsko idzie mi budowanie napięcia, ale co tam dasz radę. Gotowi? No to:

## Microsoft udostępnił jako open-source jedną z najbardziej używanych aplikacji

Mówiąc wprost - **Windows Calculator**. Całe źródła są dostępne na GitHub: [https://github.com/Microsoft/calculator](https://github.com/Microsoft/calculator "https://github.com/Microsoft/calculator"). Powiem więcej jest już całkiem sporo issue zgłoszonych, a co więcej bardzo dużo PR. Wydaje się to dziwne, ale działa :)

A teraz już na poważnie.

## Czy C# jest low-level?

Szybka odpowiedź to: NIE! A może jednak? Jeżeli chcecie dowiedzieć się więcej to jest bardzo ciekawy artykuł autorstwa Matta Warrena, który nie tylko patrzy na składnie, ale i na wydajność optymalizacje i dodatkowo pokazuje dużo ciekawej literatury. Warto przeczytać: [Is C# a low-level language?](https://mattwarren.org/2019/03/01/Is-CSharp-a-low-level-language/)

## Rekordy z C# 8.X

Już wiemy że w 8.0 rekordy się nie zmieszczą, ale może w 8.1 albo w 8.2. Jeżeli jeszcze nie wiecie o co chodzi to warto zajrzeć: [http://www.devsanon.com/c/c-8-is-introducing-records/](http://www.devsanon.com/c/c-8-is-introducing-records/ "http://www.devsanon.com/c/c-8-is-introducing-records/"). Moim zdaniem fajny dodatek do składni - mały a poprawiający czytelność kodu.

## Async + cancel

W telegraficznym skrócie. Od C# 8.0 będzie można napisać async enumerable, które wspiera cancellaion token. Jak? W artykule [Async Enumerables with Cancellation](http://blog.monstuff.com/archives/2019/03/async-enumerables-with-cancellation.html) znajdziecie odpowiedź.

## Nowości z .NET Core 3

W tej sekcji kilka spraw:

* Jest nowa wersja tym razem: [.NET Core 3.0 Preview 3](https://devblogs.microsoft.com/dotnet/announcing-net-core-3-preview-3/) przy okazji której pierwszy możemy obejrzeć .NET Standard 2.1. **UWAGA:** jak można się spodziewać potrzebne będzie nowe Visual Studio. Myślałem że już jakiś czas temu MS odszedł od łączenia wydań VS z dotnet, ale jak widać się myliłem
* Fajny opis poprawki wydajnościowej w .NET Core 3.0 czyli: [Floating-Point Parsing and Formatting improvements in .NET Core 3.0](https://devblogs.microsoft.com/dotnet/floating-point-parsing-and-formatting-improvements-in-net-core-3-0/)
* Nisko poziomowa wydajność, czyli człowiek z Intel opowiada o [hardware intrinsic for .NET Core.](https://fiigii.com/2019/03/03/Hardware-intrinsic-in-NET-Core-3-0-Introduction/) Warto wiedzieć że coś takiego jest. Ja tego raczej nie wykorzystam, ale znam kilka osób, które będą pewnie probować. Może i Ty drogi czytelniku też? Jak tak to nie zapomnij podzielić się swoimi doświadczeniami!

## mBank i dotNET

Część czytelników pewnie wie, że mBank dotnetem stoi. Ale o zmianach głęboko w systemach centralnych to już pewnie wie niewiele osób. A tu proszę publicznie na raincode labs pojawił się artykuł. Niestety wymagany jest email żeby pobrać cały artykuł - przychodzi jako PDF w email. Ale pewnie wiecie jak sobie z tym radzić ;)

Dużo przykładów nie nie ma, ale jak ktoś kodował kiedyś w "dziwnym" języku, może przeczytać podstawy jego transformacji. Więcej: [https://www.raincodelabs.com/blog/how-early-bad-smell-detection-can-save-your-project/](https://www.raincodelabs.com/blog/how-early-bad-smell-detection-can-save-your-project/ "https://www.raincodelabs.com/blog/how-early-bad-smell-detection-can-save-your-project/")

## F#

Zostałem wywołany do tablicy na temat F#. Niestety jestem kiepski w tej dziedzinie. No taki junior ze mnie i ciężko mi oceniać artykuły w tym temacie. Jednak jeden bardzo mnie zaciekawił, bo akurat F# do Azure Functions (czy też AWS Lambda) pasuje mi idealnie. A więc o to i [Azure Functions With F#](https://www.aaron-powell.com/posts/2019-03-05-azure-functions-with-fsharp/)

Dodatkowo w ramach [Announcing .NET Core 3 Preview 3](https://devblogs.microsoft.com/dotnet/announcing-net-core-3-preview-3/) pojawiła się jedna bardzo interesująca informacja. Komenda "dotnet fsi" czyli F# interactive jako natywna aplikacja dotnet core. 

p.s. Jeżeli chciałbyś mnie wspomóc w temacie F# to będę BARDZO wdzięczny!

## Let's make engineering great again!

Chyba prywata, bo w artykule występuje z imienia i nazwiska. Dotnet bezpośrednio nie dotyczy, ale CTO który to opisał ma pod sobą kilku dobrych kolesi z dotNET.

A chodzi o deweloperów i ich podejście, które z różnych powodów wydaje się coraz gorsze jeżeli chodzi o stosunek jakości do ceny. Warto przeczytać: [https://www.linkedin.com/pulse/lets-make-engineering-great-again-%C5%82ukasz-dziekan/](https://www.linkedin.com/pulse/lets-make-engineering-great-again-%C5%82ukasz-dziekan/ "https://www.linkedin.com/pulse/lets-make-engineering-great-again-%C5%82ukasz-dziekan/"). Warto przeczytać także komentarze pod artykułem. Mądre w nich słowa padają.

Po przeczytaniu tego artykułu może zaciekawi Cię:

* [Demystifying HttpClient Internals](https://www.stevejgordon.co.uk/demystifying-httpclient-internals-sendasync-flow-for-httprequestmessage)
* [Getting started with Azure Cosmos DB and .NET Core: Part #2 – string querying and ranged indexes](https://jeremylindsayni.wordpress.com/2019/03/03/getting-started-with-azure-cosmos-db-and-net-core-part-2-string-querying-and-ranged-indexes/) czy [Logging and monitoring cost of CosmosDB queries by using Application Insights](https://www.jankowskimichal.pl/en/2019/03/logging-and-monitoring-cost-of-cosmosdb-queries-by-using-application-insights/)
* [Performance comparison of .NET IoC containers](https://github.com/danielpalme/IocPerformance)

## Zabawka na koniec

Na sam koniec zabawa dla fanów LEGO i CSS czyli [CSS LEGO figure maker](https://codepen.io/joshbader/full/MZMzjr). Zabawa przednia a dla prawdziwych fanów, można kod obejrzeć :)