---
layout: post
title: 5 mitów o kontenerach
date: 2019-11-02 23:00:00 +0000
header-img: "/images/content/pablo (6) (1).jpg"

---
Jeżeli używasz kontenerów to większość mitów pewnie znasz, a jeżeli nie używasz to słyszałeś je na 100%. Taki paradoks. 5 mitów, które krążą na temat konteneryzacji, jest tak powszechnych, że aż postanowiłem się z nimi rozprawić.

## Kontenery to tylko Docker

To jeden z najczęściej spotykanych mitów. To nieprawda. Po pierwsze jest firma Docker Incorporated, czyli tłumacząc na polski Doker S.A. (ten brak “c” to nie pomyłka, słowo doker funkcjonuje w języku polskim i oznacza pracownika doków, tak samo jak w języku angielskim). Wypuściła ona oprogramowanie, które umożliwia radzenie sobie w sposób przyjazny dla programistów i administratorów, z pakowaniem i uruchamianiem aplikacji w luźno odizolowanym środowisku. Brzmi dziwnie, ale lepszego tłumaczenia dla “loosely isolated” nie mam.

Wracając jednak do tematu. Docker to nie jedyna platforma do uruchamiania kontenerów. Są też starsze niż Docker, a najbardziej mi znane z nich to: LXC i Solaris Zones. Powstało też sporo nowych np: rkt ([https://coreos.com/rkt/](https://coreos.com/rkt/ "https://coreos.com/rkt/")) wymawiany jako “rocket”.

Podsumowując Docker to nie jedyny wybór, ale jest on najbardziej popularny.

## Kontenery działają tylko na Linux

Kiedyś rzeczywiście tak było i dla większości technologii od kontenerów tak jest nadal, ale akurat Docker jest wyjątkiem. Po pierwsze mamy Docker for Windows, czyli narzędzia, które umożliwia nam uruchomienie kontenerów w Windows. Na ten moment jest to małe oszustwo, ponieważ wykorzystuje ono uruchomioną na Hyper-V maszynę moby linux. Ale na pewno też słyszałeś, o Windows Containers. Ten ekosystem powoli zaczyna już działać produkcyjnie, a nie jako ciekawostka. Całkiem niedawno nawet chmura AWS (tak nie Azure, tylko AWS) ogłosiła wsparcie GA dla Windows Containers 2019. GA oznacza Global Available, czyli z pełnym wsparciem, a nie żadne preview/beta/alfa. Więcej możesz przeczytać na oficjalnej stronie: [https://aws.amazon.com/about-aws/whats-new/2019/06/amazon-ecs-support-windows-server-2019-containers-generally-available/](https://aws.amazon.com/about-aws/whats-new/2019/06/amazon-ecs-support-windows-server-2019-containers-generally-available/ "https://aws.amazon.com/about-aws/whats-new/2019/06/amazon-ecs-support-windows-server-2019-containers-generally-available/")

## Kontenery są szybsze niż VM

Słowo “szybsze” jest trudne do definicji, bo pojawia się pytanie: o ile szybsze? Zacznijmy jednak od początku. Mówi się (i są na to dowody), że aktualne techniki wirtualizacji powodują, że VM są jedynie 2-3% wolniejsze niż “bare metal”. No to jak ten docker ma być szybszy? Pewnie nie jest, a jak już jest to nie dużo. Ale nie to jest jego głównym zadaniem. Dzięki małemu nakładowi jaki potrzebuje, jest lżejszy niż VM, a dzięki temu umożliwia wykorzystanie zasobów fizycznej maszyny w bardziej efektywny sposób. Czyli na tych samych zasobach fizycznych upychamy więcej.

Podsumowując można zgodzić się z tym mitem, o ile rozszerzymy go o dodatkowe stwierdzenie, że kontenery nie potrzebują marnować CPU i RAM na system operacyjny maszyny wirtualnej i dzięki temu mogą pracować "szybciej".

## Kontenery są ciężkie w setup

To znowu półprawda. Jeżeli podejdziemy od strony, że informatyka jest ciężka to kontenery też są. Oczywiście użycie niektórych technologii jest trudne, ale Docker jest naprawdę przyjazny. Wystarczy kilka dobrych praktyk, które mój kolega Gutek, jest wstanie opisać w 15 minut i dać Ci kilka ćwiczeń do domu, po których masz naprawdę wystarczającą wiedzę.

Taki zakres wystarcza w 95% przypadków. A co z 5%? Pozwolę sobie użyć słynnego powiedzenia w świecie IT “to zależy”. Doświadczenie jednak mi mówi, że większość tych 5% to błędy nie w kontenerach, tylko w aplikacji :)

## Jak odpalę Docker to będzie lepiej

To kolejna półprawda, albo nawet totalne kłamstwo. Sam Docker rozwiązuje określoną gamę problemów, a poza tym jest takim plikiem ZIP, który zawiera naszą aplikację oraz wszystkie jej zależności. Żeby jednak całość działała dobrze, potrzebne jest magiczne narzędzie do uruchamiania i zarządzania kontenerami. Zawodników było wielu, ale na placu boju wygląda, że zostanie jeden - Kubernetes.

## Podsumowanie

Jeżeli temat Cię zainteresował i chcesz dowiedzieć się więcej to zapraszam Cię serdecznie na webinar “Wieczór z Kubernetes”. Tym razem motywem przewodnim będzie dyskusja na temat konteneryzacji, możesz dołączyć do wydarzenia:

* [na YouTube](https://k8s.buzz/live-youtube)
* [na Facebook](https://k8s.buzz/live-facebook)

p.s. Wystartował też kurs “Poznaj Kubernetes”, na którym dowiesz się jak wejść w świat kontenerów nie tylko od praktycznej strony, ale też od teoretycznej. Dotykamy nie tylko Kubernetes, bo sam w sobie jest on tylko “młotkiem”. Omówimy tematy architektury systemów rozproszonych, jak używać docker czy jakie health check powinna mieć nasza aplikacja. Więcej na oficjalnej stronie: [http://poznajkubernetes.pl](http://poznajkubernetes.pl "http://poznajkubernetes.pl")