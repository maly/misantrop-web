---
id: 2030
title: Odhalené Druidly
date: 2014-05-25T13:47:53+01:00
author: Martin Malý
layout: revision
guid: http://www.misantrop.info/519-revision-v1/
permalink: /519-revision-v1/
---
Když jsme začali s Druidly, měli jsme úplně jiné starosti, než vysvětlovat všem, co že vlastně děláme. Věděli jsme to my, věděl to náš tým, a vědělo to pár lidí, co nám pomohli radou&#8230; Ne že bychom to nechtěli říct a stavěli na tom marketing. Jen prostě nebyl čas ani důvod to veřejně oznamovat.

<!--more-->

Ovšem stačilo říct, že &#8222;na něčem děláme&#8220;, a lidská zvědavost katalyzovala celé PR tak, že jsme si po krátké době řekli, že to je vlastně legrační &#8211; sledovat vlnu očekávání, dohadů, rozčilených reakcí (za všechny jmenuju Dana Steigerwalda, který několikrát svou zvědavost neunesl a vynadal nám, že &#8222;spamujeme vlastní účet&#8220;), a na druhé straně se bavit tím, že Rasťa Turek chodí a vykládá, že Druidly je navigační systém pro rakety, a to je tajné, &#8222;_lebo vieš čo&#8230; tieto armádne veci&#8230;_&#8220; 🙂

Dneska vyšlo [představení Druidly na Médiáři](http://www.mediar.cz/druidly-umozni-malym-casopisum-ci-blogum-publikovat-ve-vlastni-mobilni-aplikaci/). Pel tajemna byl setřen, a první reakce jsou vesměs pozitivní. Díky za ně!

Proč Windows 8 jako první? Je to nový trh, který je hladový po aplikacích. Zároveň je to tak silná platforma, resp. Microsoft má tak dominantní pozici (stále), že si ji málokdo může dovolit ignorovat. Náš tým má s publikováním aplikací pro Windows 8 zkušenosti už dnes, takže máme náskok před dalšími týmy. Vstupujeme na zcela nový trh, kde se dá očekávat prudká počáteční expanze zájmu, a my jsme se rozhodli, že u toho budeme. Další platformy ale budou samozřejmě následovat, nechceme být &#8222;Win8-only&#8220;, to by bylo krátkozraké.

Už tedy všechno víte, tak dodám jen pár slov pro techniky: Druidly běží na šesti různých serverech &#8211; jeden se stará o správu uživatelů, druhý o analýzy, třetí o generování aplikací, čtvrtý zpracovává obsah, pátý se stará jen o notifikace přes WebSockets, a šestý je origin server pro CDN. Vývoj probíhá v PHP/Nette a v Node.js (použito pro zpracování obsahu a práci s websockety), o velké toky dat (obsah, notifikace) se stará Redis a Memcache, analýzy běží nad PostgreSQL&#8230;

Druidly je v první řadě nástroj pro generování obsahových aplikací pro různé platformy. Zároveň zajišťuje kompletní distribuci obsahu přes vlastní CDN a dává vydavatelům zpětnou vazbu v podobě analýz chování jejich čtenářů. Díky této analýze zároveň dokáže každému uživateli prioritizovat články, tzn. na první místa dávat takové, které ho budou zajímat. Na druhou stranu není vázané jen na &#8222;mediální obsah&#8220; &#8211; díky univerzálnímu návrhu infrastruktury se může postarat o jakýkoli jiný obsah, od e-shopů po, řekněme, denní jídelní lístky pro restaurace.

Druidly vzniklo během sedmi týdnů. Do dvou týdnů bude spuštěná betaverze. Pokud máte zájem, přihlašte se na stránce Druidly, dáme vám vědět!