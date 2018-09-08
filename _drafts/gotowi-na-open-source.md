---
title: Gotowi na open-source
date: 2018-09-07 21:02:46 +0000
layout: post
header-img: ''

---
Żebym mógł podzielić się pracą nad dotnetomaniakiem muszę wykonać jeden bardzo ważny krok. Muszę upublicznić repozytorium. Na początku myślałem, że po prostu będę dawał dostęp do swojego prywatnego repo. Jednak ciągle czytałem - a będzie open-source?

## Jeden (doświadczony) deweloper to same problemy

Wiele lat pracy wymagało ode mnie pilnowania się. Myślenia jak inżynier, a nie jak haker. Doprowadzania i pilnowania procesów CD i CI. Czyli mówiąc wprost tak zwanej solidnej roboty. Co zrobiłem gdy dostałem w swoje ręce dotnetomaniaka? Zagryzłem zęby, walną pięścią w stół, rzuciłem mięsem i puściłem deploy z Visual Studio. Oczywiście dodałem w myślach klasyczny tekst - przy najbliższej okazji to zmienie. 3 miesiące później, kilka(naście) deploymentów później sytułacja się nie zmieniła. Ale co to ma wspólnego z open-source? Sekrety są wrzucone w web.config. Częściowo tak już było, część "nowych" sam dodałem. Historia w git ma tłum haseł, czyli bądźmy szczerzy porażka na całego. No i co teraz?

## Pomysły na sekrety

Posiedziałem, podumałem, pojeździłem i pobębniłem palcami w biurko. Burza mózgów dała mi następujące pomysły:- Pominać całą historię i rozpocząć ją na nowo. Rozwiązanie łatwe, proste i do załatwienia w 10 minut. Jedyny problem moje sumienie. Ten portal to praca kilku ludzi. Historia to szacunek dla ich pracy.- Przepisać historię tak by hasła znikneły. W teorii prosty rebase. W praktyce... sami dobrze wiecie jak praktyka wygląda. Skończyłbym jako masowy producent mięsa słownego.- I tu wreszcie zaświtało. Nie wiem czy coś mi się przypomniało, czy po prostu wpadłem na amerykę w konserwie. Poszukałem w dokumentacji git'a i jest "git-filter-branch". Ale opis mnie rozwalił:

> git-filter-branch allows you to make complex shell-scripted rewrites of your Git history, but you probably don’t need this flexibility if you’re simply removing unwanted data like large files or passwords. For those operations you may want to consider The BFG Repo-Cleaner, a JVM-based alternative to git-filter-branch, typically at least 10-50x faster for those use-cases, and with quite different characteristics

## Java jest cool?

Techniczne zmagania zajęły 2 dni. W teorii były to 3 polecenia:

```
git clone --mirror `
	https://bitbucket.org/ptrstpp950/dotnetomaniak.git
java -jar bfg.jar `
	--delete-files Web.config dotnetomaniak.git
java -jar bfg.jar `
	--delete-files maniak_deepzoom.zip dotnetomaniak.git
```
Praktyka zajęła 4 godziny. Rada dla Ciebie: przeczytaj całość [dokumentacji dokładnie](https://rtyley.github.io/bfg-repo-cleaner/). A odpowiadając na pytanie tak Java w tym przypadku jest bardzo cool, tylko ja nie umiem czytać :D

## To już jest koniec?

Źródła już są na github. Jest lepiej, no ba. A gdzie teraz są sekrety? Na razie to u mnie na komputerze. Co więcej brakuje:

* procesu CI/CD
* konfiguracji dla deweloperów
* skryptu z bazą testową