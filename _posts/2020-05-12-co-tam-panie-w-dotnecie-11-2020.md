---
layout: post
title: 'Co tam Panie w dotnecie? #11/2020'
date: 2020-05-12 22:00:00 +0000
header-img: "/images/content/pablo-11-1.jpg"

---
W tym tygodniu Azure, kolejki i .NET. Dość fajny mix. Zapraszam serdecznie :)

## Nowe datacenter Azure

Pewnie o tym już wiesz, ale dla formalności umieszczę, szczególnie że idzie za tym całkiem spora kasa dla Polski:

* [Microsoft ogłasza plan inwestycji 1 miliarda dolarów w transformację cyfrową w Polsce, w tym dostęp do lokalnych usług w chmurze z pierwszego regionu przetwarzania danych](https://news.microsoft.com/pl-pl/2020/05/05/polskadolinacyfrowa/)

A do tego mamy też wiadomość na temat Włoch: [Microsoft announces $1.5 billion investment plan to accelerate digital transformation in Italy, including its first cloud datacenter region](https://news.microsoft.com/europe/2020/05/08/microsoft-announces-1-5-billion-investment-plan-to-accelerate-digital-transformation-in-italy-including-its-first-cloud-datacenter-region/)

Jak widać Włosi dostali więcej niż Polacy. Co cóż takie życie ;)

## Kochamy kolejki ale czy rozumiemy je dobrze?

No właśnie. W tym tygodniu znalazłem bardzo ciekawy artykuł na temat Kafki jak postawić ją w wielu regionach i obsługiwać ten problem. Jeżeli chodzi o samo rozwiązanie to oczywiście omawiane są typowe przez pryzmat tego co może Kafka, ale jeżeli chodzi o problemy to są one uniwersalne.

Mówiąc wprost - warto. Całość: [https://tech.ebayinc.com/engineering/resiliency-and-disaster-recovery-with-kafka/](https://tech.ebayinc.com/engineering/resiliency-and-disaster-recovery-with-kafka/ "https://tech.ebayinc.com/engineering/resiliency-and-disaster-recovery-with-kafka/")

A jeżeli planujesz siedzieć w Azure to cała seria artykułów na temat Azure Service Bus od początku do pewnego etapu ;) Aktualnie 8 postów, szczególnie dla osób które mało dotykały ten komponent

[https://markheath.net/post/azure-service-bus-messaging-1](https://markheath.net/post/azure-service-bus-messaging-1 "https://markheath.net/post/azure-service-bus-messaging-1")

## Migrujesz do dotNET Core? To narzędzie może się przydać

Część z Was pewnie wie, że mam plan serwis dotnetomaniaka przenieść na dotnet core (i pewnie też NET 5.0). Pierwszy etap właśnie się kończy: usunęliśmy Linq2SQL i zastąpiliśmy go EF.Core. Właśnie idą finalne testy.Na pytania dlaczego EF.Core a nie dapper, albo Hibernate, albo XYZ, to odpowiedź jest prosta: chętna osoba tak wybrała, a było co przepisywać. Chcesz ORM to zapraszamy do kontrybucji :)

Co do dalszych zmian jest fajne narzędzie i właśnie je chcę Ci polecić dzisiaj czyli try-convert. Całość na github: [https://github.com/dotnet/try-convert](https://github.com/dotnet/try-convert "https://github.com/dotnet/try-convert")

## 10 książek które każdy NET developer ??powinien??przeczytać.

Lista jest: [https://blog.elmah.io/top-10-books-every-net-c-developer-should-read/](https://blog.elmah.io/top-10-books-every-net-c-developer-should-read/ "https://blog.elmah.io/top-10-books-every-net-c-developer-should-read/")

Mi na niej brakuje przede wszystkim książki Konrada Kokosy, a u Was jak jest? Ja chyba zrobię swoją listę

## Tydzień dotnetomaniaka

Jak co tydzień zapraszam Cię na ostatnie podsumowanie tygodnia: [https://dotnetomaniak.pl/weekly/2020/19](https://dotnetomaniak.pl/weekly/2020/19 "https://dotnetomaniak.pl/weekly/2020/19")