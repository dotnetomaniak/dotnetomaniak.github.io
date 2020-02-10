---
layout: post
title: 'Co tam Panie w dotnecie? #01/2020'
date: 2020-02-01 23:00:00 +0000
header-img: "/images/content/patrick-fore-0gkw_9fy0eQ-unsplash.jpg"

---
Po długiej przerwie wracamy do nowości ze świata .NET. Przepraszam, że przez pół roku nic się nie działo, ale sprawy osobiste i zawodowe przeważyły i nie wyrabiałem się z czasem. Mam nadzieję, że to już za mną i regularnie będę mógł dostarczać Ci ciekawostek :)

Po pierwsze kwestia samego dotnetomaniaka. W zeszłym tygodniu 8 artykułów acz jak patrzę to głownie dotykające .NET, a nie osadzone w nim głęboko: CI/CD, bazy danych (SQL i NoSQL) oraz refaktoring. Warto zajrzeć na szybko przy kawce: [https://dotnetomaniak.pl/weekly/2020/5](https://dotnetomaniak.pl/weekly/2020/5 "https://dotnetomaniak.pl/weekly/2020/5")

Druga sprawa. Do tego tygodnia nie wiedziałem nie wiedziałem, że w dotnet istnieje atak ZIP bomb, a w znalezionym artykule jest nawet jego rozwiązanie. O co chodzi? Przy odpowiednio spreparowanym pliku wykonanie na nim archiwizacji zip potrafi nieźle "namieszać". Z 10 MB powstaje nam 281TB (to nie błąd: terabajtów). Więcej: [https://www.meziantou.net/prevent-zip-bombs-in-dotnet.htm](https://www.meziantou.net/prevent-zip-bombs-in-dotnet.htm "https://www.meziantou.net/prevent-zip-bombs-in-dotnet.htm")

Trzecia kwestia to NET5.0 i cicha nadzieja na łatwą migrację starego legacy w nowe? Niestety NIC Z TEGO! Dlaczego? Na to odpowiada poniższy artykuł: [https://medium.com/young-coder/the-reunification-of-net-5-5902744df9fe](https://medium.com/young-coder/the-reunification-of-net-5-5902744df9fe "https://medium.com/young-coder/the-reunification-of-net-5-5902744df9fe")[  
](https://medium.com/young-coder/the-reunification-of-net-5-5902744df9fe)  
Jak już jesteśmy przy NET 5.0 to właśnie na jego pokładzie znalazło się Mono. Więcej w zaakceptowanym już PR na GitHub: [https://github.com/dotnet/runtime/pull/1912](https://github.com/dotnet/runtime/pull/1912 "https://github.com/dotnet/runtime/pull/1912")

Jest nawet coś "śmiesznego" na ten tydzień. Na blogu Scotta pojawił się wpis zbierający pracę kilku osób (głównie jednej), którym trzeba było "potrzymać piwo". Okazuje się, że da się odpalić dotnet na Windows 3.11 czy DOS. Serio, serio: [https://www.hanselman.com/blog/NETEverywhereApparentlyAlsoMeansWindows311AndDOS.aspx](https://www.hanselman.com/blog/NETEverywhereApparentlyAlsoMeansWindows311AndDOS.aspx "https://www.hanselman.com/blog/NETEverywhereApparentlyAlsoMeansWindows311AndDOS.aspx")

A na sam koniec jeżeli ciekawi Cię migracja i głupie wpadki jakie zrobił mój zespół i w szczególności ja, to zapraszam do obejrzenia mojej prezentacji o pięknym tytule: "Buzzwords, cloud native, kubernetes a na końcu okazuje się, że engineering and nothing else matters" z konferencji bITconf 2019. To pewnie ostatnia prezentacja nagrana z logiem FinAi, więc to "unikalna" szansa: [https://www.youtube.com/watch?v=XCmBKEz8t3o](https://www.youtube.com/watch?v=XCmBKEz8t3o "https://www.youtube.com/watch?v=XCmBKEz8t3o")

I to by było na tyle  
Piotrek

p.s. Masz jakieś pytania, kwestie, artykuły albo chcesz się wyżalić lub pochwalić to pisz śmiało. Może być komentarz albo e-mail (admin na dotnetomaniak.pl). Mi będzie bardzo miło, a może dam radę pomóc :)