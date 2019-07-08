---
layout: post
title: 'Co tam Panie w dotnecie? #22'
date: 2019-07-07 22:00:00 +0000
header-img: ''

---
## PooledAwait

Marc Gravell wpadł na genialny pomysł jak lekko oszukać publiczne API C# i uzyskać `PooledAwait` za pomocą `PooledValueTask`, który jest szczególnym przypadkiem `ValueTask`.  Dzięki takiemu zabiegowi, chce on uzyskać zero alokacji przy "niekompletnym" async/await. Udało się? Oceńcie sami, a po szczegóły (no i kod) zapraszam Was na Github Marka: [https://github.com/mgravell/PooledAwait](https://github.com/mgravell/PooledAwait "https://github.com/mgravell/PooledAwait")

##  F# VS. C# czyli clickbait w natarciu

Artykuł jest stary ma już ponad 2 lata, jednak akurat dla mnie jest on nowością. Nigdy wcześniej na niego nie trafiłem. 

Artykuł został u nas w firmie wrzucony z następującymi zdaniami:

> **F# is almost 3.3 times slower than C#.**

oraz

> **This time F# is almost 15 times slower than C#**

I co bać się? Czy może już cieszyć? Strach czy radość sugeruję przeczytać do końca i nie przerywać w trakcie. Dotyczy to zarówno zwolenników jak i przeciwników: [http://www.ybouglouan.pl/2017/04/fsharp-vs-charp-performance-comparison-with-benchmarkdotnet/](http://www.ybouglouan.pl/2017/04/fsharp-vs-charp-performance-comparison-with-benchmarkdotnet/ "http://www.ybouglouan.pl/2017/04/fsharp-vs-charp-performance-comparison-with-benchmarkdotnet/")

## 25 tys inżynierów MS na GitHub

Bardzo ciekawa opowieść (lepiej pasuje war-story) o tym jak zwiększyła się kontrybucja Microsoft na GitHub. Od 2 tysięcy do 25 tysięcy inżynierów. Można poczytać o wszystkim, czego użyli i używają do dziś. Polecam szczególnie, że pochodzi to z "wewnętrznego kręgu": [https://jeffwilcox.blog/2019/06/scaling-25k](https://jeffwilcox.blog/2019/06/scaling-25k "https://jeffwilcox.blog/2019/06/scaling-25k")

## Video wprowadzenie do ML.NET CLI

Jak chcecie poznać CLI do ML.NET to chyba najprostszy sposób:

<iframe width="560" height="315" src="https://www.youtube.com/embed/gjPRn3NRTvk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## d