---
title: CI / CD dotnetomaniaka czyli Azure DevOps w praktyce
layout: post
date: 2018-10-05 06:00:00 +0000
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

<blockquote class="twitter-tweet" data-lang="en-gb"><p lang="en" dir="ltr">Maintain an open source project? Build for free with Azure Pipelines. Unlimited build minutes across cloud hosted Linux, Windows and macOS servers. Get set-up from <a href="https://twitter.com/github?ref_src=twsrc%5Etfw">@GitHub</a> in minutes <a href="https://t.co/e6nt1uEb1L">https://t.co/e6nt1uEb1L</a> - With ❤ from <a href="https://twitter.com/Microsoft?ref_src=twsrc%5Etfw">@Microsoft</a> <a href="https://t.co/bF9ML7ciBM">pic.twitter.com/bF9ML7ciBM</a></p>— Azure DevOps (@AzureDevOps) <a href="https://twitter.com/AzureDevOps/status/1043160416396951552?ref_src=twsrc%5Etfw">21 September 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## Build czyli zabawa

Na pierwszy rzut oka to w sumie to 5 minut roboty. Jeżeli kiedykolwiek miałeś styczność z VSTS to wiesz, że można to wyklikać. Jeżeli TeamCity/Bamboo/Jenkins to Twoja domena, to jest podobnie, tłumaczyć nie ma co. To o czym piszesz? - pewnie zaświtało w głowie.

W Azure DevOps (czyli VSTS z nowościami) jest nowy sposób budowania definicji build. Można użyć pliku yaml. Hell yeah!!!! Jak to wygląda:

    pool:
      vmImage: 'VS2017-Win2016'
    
    variables:
      solution: 'v3.0/Source/Kigg.sln'
      buildPlatform: 'Any CPU'
      buildConfiguration: 'Release'
    
    steps:
    - task: NuGetToolInstaller@0
    
    - task: NuGetCommand@2
      inputs:
        restoreSolution: '$(solution)'
    
    - task: VSBuild@1
      inputs:
        solution: '$(solution)'
        msbuildArgs: '/p:DeployOnBuild=true /p:WebPublishMethod=Package /p:PackageAsSingleFile=true /p:SkipInvalidConfigurations=true /p:PackageLocation="$(build.artifactStagingDirectory)"'
        platform: '$(buildPlatform)'
        configuration: '$(buildConfiguration)'
    
    - task: VSTest@2
      inputs:
        platform: '$(buildPlatform)'
        configuration: '$(buildConfiguration)'
    
    - task: PublishBuildArtifacts@1
      inputs:
        pathtoPublish: '$(build.ArtifactStagingDirectory)' 
        artifactName: 'build'

Czy mówiąc wprost po ludzku. Na maszynie z _VS2017_ (i chyba Windows 2016) wywołujemy dla solucji _v3.0/Source/Kigg.sln_ pięć zadań:

* zainstaluj nuget
* zrób nuget restore
* zbuduj za pomocą msbuild i podanych argumentów typowych dla web apki
* puść osobno wszystkie testy
* "pobierz" artefakty (chociaż tłumaczenie "publish" na pobierz takie średnie)

I wszystko fajne tylko okazuje się, że powyższa definicja nie działa zawsze. Dla projektów na GitHub można uruchomić automatyczne uruchomienie CI, ale wtedy ostatni krok niestety wywala się z cudnym błędem, że nie ma uprawnień czy coś takiego. Masakra mówiąc szczerze. Stąd powstały dwa pliki:

* dla gałęzi master taki jak wyżej: [https://github.com/dotnetomaniak/dotnetomaniak/blob/master/ci.main.repo.yml](https://github.com/dotnetomaniak/dotnetomaniak/blob/master/ci.main.repo.yml "https://github.com/dotnetomaniak/dotnetomaniak/blob/master/ci.main.repo.yml")
* dla PR okrojony: [https://github.com/dotnetomaniak/dotnetomaniak/blob/master/ci.pull.requests.yml](https://github.com/dotnetomaniak/dotnetomaniak/blob/master/ci.pull.requests.yml "https://github.com/dotnetomaniak/dotnetomaniak/blob/master/ci.pull.requests.yml")

Dodatkowo każdy build jest widoczny dla szerokiej publiczności i jego stan można sobie sprawdzić na stronie: [https://dev.azure.com/dotnetomaniak/dotnetomaniak/_build?definitionId=2](https://dev.azure.com/dotnetomaniak/dotnetomaniak/_build?definitionId=2). Jako bonus dostępny jest badge: [![Build Status](https://dev.azure.com/dotnetomaniak/dotnetomaniak/_apis/build/status/dotnetomaniak.main.repo)](https://dev.azure.com/dotnetomaniak/dotnetomaniak/_build/latest?definitionId=2)

## Deplojuj mocium panie

Ponieważ dotnetomaniak jest na Azure, to instalacja zwana popularnie deplojem albo deplojmentem jest banalnie prosta. Nie ma jeszcze YAML w tej części, ale jeden task dałem radę wyklikać. Nawet na 2 środowiska.

![](/images/content/Zrzut ekranu 2018-10-04 o 20.53.01.png)Dla zainteresowanych, całość acz bez definicji ale z logami można sobie obejrzeć: [https://dev.azure.com/dotnetomaniak/dotnetomaniak/_releases2](https://dev.azure.com/dotnetomaniak/dotnetomaniak/_releases2 "https://dev.azure.com/dotnetomaniak/dotnetomaniak/_releases2")

Jeżeli ktoś jest zapalonym DevOps, albo wie z innych powodów, że zrobiłem źle, to niestety ma rację. Definicja powinna używać staging slot, żeby nie było efektu przerw, gdy jest wgrywana nowa wersja. A tak dzieje się regularnie. Ostatnio efekt był taki:

![](/images/content/41903743_10156684283323555_1620628238957019136_o.png)Dlaczego jednak tak nie zrobiłem? Niestety dotnetomaniak aktualnie korzysta z mojej subskrypcji i mówiąc wprost nie stać mnie na droższy plan na ten moment. Więc dopóki nie zdobędę dodatkowych środków to jest jak jest i trzeba się z tym pogodzić.