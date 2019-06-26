---
layout: post
title: Windows Terminal
date: 2019-06-25 22:00:00 +0000
header-img: "/images/content/cmd.png"

---
W ostatnim [podsumowaniu tygodnia](https://blog.dotnetomaniak.pl/co-tam-panie-w-dotnecie-20/) pochwaliłem się, że udało mi się zainstalować nowy _Windows Terminal (Preview)_. Przy okazji czemu wszystko w dzisiejszych czasach musi być preview? Nie wiem, ale instalacja tego cuda prosta nie była.

Jeżeli masz ochotę mieć go u siebie to zapraszam, zaoszczędzę Ci chwili drapania się w głowę.

## Skąd?

Opcje są dwie. Po pierwsze jest GitHub, ale jak tylko się pojawił terminal to próbowałem go skompilować i prosto nie było. Teraz może jest łatwiej, ale wolę gotowca.

Po drugie jest Windows Store: [https://www.microsoft.com/pl-pl/p/windows-terminal-preview/9n0dx20hk701](https://www.microsoft.com/pl-pl/p/windows-terminal-preview/9n0dx20hk701 "https://www.microsoft.com/pl-pl/p/windows-terminal-preview/9n0dx20hk701"). Link łatwy do zapamiętania bo:

* 9 - takiej wersji systemu Windows nie było
* n - to pierwsza litera jednego z lepszych Windows czyli Windows **N**T
* 0 - bo każdy programista liczy od zera
* d - jak d...obrze że już jest
* x - wiadomo X zawsze powoduje, że jest lepiej
* 20 - była taka piosenka - ja mam 20 lat, ty masz 20 lat, a dotnet zaraz będzie mieć 20 lat
* hk - to jakiś skrót ale nie wiem jaki -> już mam dzięki Piotrowi Ferencowi - "haj kłality"
* 701 - tutaj prosto o ile mieszkacie/mieszkaliście w gminie Izabelin. 701 to autobus, który zawsze tu dojeżdżał, ale w tym roku zmienili mu nazwę na 210.
* no a sam początek można zgadnąć ;)

(przepraszam nie mogłem się powstrzymać)

Jak wejdziecie do sklepu to waszym oczom ukaże się:

![](/images/content/terminal-store.jpg)

Pewnie tak jak ja (i kilku moich kolegów) naciśniecie szybko **Get** i wiecie co? Najprawdopodobniej, NIC się nie stanie. Dlaczego tak jest? Polecam zakładkę System Requirements, która u mnie wyglądała tak:

![](/images/content/terminal-store1.jpg)

No właśnie potrzebny jest build Windows 10 o numerze 18362 lub wyższej - czyli mówiąc wprost majowy update (numerek kodowy 1903)

## Update do 18362

Macie teraz trochę czasu? To puszczajcie ściąganie. W zależności od internetu chwilę to zajmie. Ja mam wolny, więc zajęło to długo, ale kolegom w pracy poszło już szybciej. Niestety instalacja tego update może zając do 90 minut. Tak instalacja, nie samo ściąganie. Nawet jest to napisane gdy komputer jest gotowy do instalacji:

![](/images/content/terminal-update-windows2.jpg)

No nic, trudno się mówi czego się nie zrobi dla nowego terminala.

A co daje ten update poza terminalem? Jedną wspaniała rzecz. Tak zwany "dark mode", dzięki któremu na przykład explorator wygląda tak:

![](/images/content/windows-dark-mode.jpg)

Jak by ktoś miał problem po instalacji z odszukaniem tej opcji to ścieżka jest następująca:

* Wpisujemy w wyszukiwarkę czy tam start: "Themes"
* Wybieramy "Themes and related settings"
* Potem Color

I mamy następujące "combo":

![](/images/content/windows-dark-mode-settings.jpg)

A jeszcze jedno, jeżeli chcecie ukryć duży textbox do wyszukiwania obok przycisku start to trzeba kliknąć to:

![](/images/content/windows-dark-mode-settings2.jpg)

## No to instalujemy Terminal

I po całej tej zabawie nareszcie możemy zainstalować Windows Terminal (Preview) ze sklepu. Jeżeli ktoś nie zapamiętał linka to podaję go jeszcze raz: [https://www.microsoft.com/pl-pl/p/windows-terminal-preview/9n0dx20hk701](https://www.microsoft.com/pl-pl/p/windows-terminal-preview/9n0dx20hk701 "https://www.microsoft.com/pl-pl/p/windows-terminal-preview/9n0dx20hk701")

Po instalacji istnieją następujące możliwości (o ile je macie zainstalowane):

* cmd - to na pewno macie
* PowerShell - to też
* PowerShell 6 - o ile go ściągneliście
* Różne Linux - o ile macie WSL (albo nawet i WSL2) - ja nie mam więc mi się nie pojawiło, bo czekam na oficjalne WSL2

Do tego mamy zwykły JSON z ustawieniami (czytać Settings). Można wybrać, kolejność, tło, przezroczystość, katalog "startowy" i inne. Chwilę się pobawiłem i jest "tak jak lubię"

Podsumowując używam już prawie tydzień i powiem, że jestem zadowolony. A wygląda on u mnie tak:

![](/images/content/cmd.png)

![](/images/content/terminal.png)

I to by było na tyle. Dużo bólu w instalacji, ale potem już jest spoko. No i dark-mode w Explorer wymiata jako bonus do całości ;)