---
title: CI / CD dotnetomaniaka czyli Azure DevOps w praktyce
layout: post
date: 2018-09-23 00:00:00 +0000
header-img: ''

---
Przyznam się szczerze, że gdy dostałem dotnetomaniaka w spadku po Pawle, deploy szedł z Visual Studio za pomocą przycisku "publish". Paweł też przyznał się ostatnio, że on używał do deploymentu XCOPY przez wiele lat. Dobre? Dobre bo działa. Skuteczne? Działa to skuteczne.

Ale bądźmy szczerzy, można lepiej, prawda? Jednak jeszcze kilka lat temu, nie było to takie oczywiste. Szczególnie, że mówmy o stronie, która  raczej nie przynosi dochodu. Nudzisz - pomyślałeś pewnie i chyba masz rację. Czas na mięso

## Wybór CI/CD

Dotnetomaniak stoi obecnie na Azure, dzięki temu, że jako MVP mam darmową subskrypcję. Gdzieś ją upchnąłem i choć żre sporo to daję radę. Ale to temat na osobny post.

Akurat tuż po opublikowaniu na GitHub kodu źródłowego okazało się, że MS dokonuje rebrandingu starego dobrego VSTS na Azure DevOps. Zmianę można oceniać różnie, ale z mojego punktu widzenia liczyło się jedno:

* jest za darmo dla OpenSource
* jest unlimited dla OpenSource
* możliwość puszczenia do 10 równoległych build dla Open Source
* i tak korzystam z niego w pracy i wiem że ma najlepszą integrację z Azurkiem

## Połączenie

Jest mega proste. MS udostępnia video, które pokazuje co i jak w 30 sekund. Więc zamiast pisać pozwolę sobie skorzystać, szczególnie, że filozofii wielkiej nie ma:

<blockquote class="twitter-tweet" data-lang="en-gb"><p lang="en" dir="ltr">Maintain an open source project? Build for free with Azure Pipelines. Unlimited build minutes across cloud hosted Linux, Windows and macOS servers. Get set-up from <a href="https://twitter.com/github?ref_src=twsrc%5Etfw">@GitHub</a> in minutes <a href="https://t.co/e6nt1uEb1L">https://t.co/e6nt1uEb1L</a> - With ❤ from <a href="https://twitter.com/Microsoft?ref_src=twsrc%5Etfw">@Microsoft</a> <a href="https://t.co/bF9ML7ciBM">pic.twitter.com/bF9ML7ciBM</a></p>&mdash; Azure DevOps (@AzureDevOps) <a href="https://twitter.com/AzureDevOps/status/1043160416396951552?ref_src=twsrc%5Etfw">21 September 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


s