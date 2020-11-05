---
id: 800
title: Trocha matematiky v mezilidských vztazích
date: 2013-02-02T14:40:08+01:00
author: Martin Malý
layout: revision
guid: http://www.misantrop.info/792-revision-3/
permalink: /792-revision-3/
---
Matematika není jen nuda a šeď vzorců a pouček. Může být i zajímavá a poučná a právě tuto podobu matematiky se vám teď pokusím nastínit na příkladě disciplíny, populárně nazývané „teorie her”, která se nechá aplikovat na širokou škálu situací, od her jako takových až po mezilidské a mezistátní vztahy.

Představte si, že dostanete nabídku účastnit se společenské hry, kde můžete jen vyhrát. Nabídku přijmete a dozvíte se tato pravidla: Kromě vás hraje ještě dalších 19 lidí, kteří se vzájemně neznají a nemohou se domluvit. Hra začíná v neděli přesně v poledne, trvá deset minut a všichni dostanete jedno telefonní číslo. Pokud během těchto deseti minut nikdo z vás na to číslo nezavolá, dostanete všichni 10000 Kč. Pokud někdo z vás však během těchto deseti minut zavolá, dostane 1000 Kč a ostatní nedostanou nic. Jak se rozhodnete? Zkuste přemýšlet, než budete číst dál&#8230;

Vaše úvahy budou asi v tomto duchu: _Nejlepší bude, když nikdo nezavolá. Ale určitě se najde alespoň jeden pitomec, který zavolá a já nedostanu nic. Proto je třeba, abych zavolal dřív než on&#8230; Ale ostatní uvažují úplně stejně jako já a proto je potřeba, abych zavolal úplně nejdřív&#8230;_

Když matematici tento pokus provedli, potvrdilo se očekávání — telefon zazvonil během několika vteřin po dvanácté hodině. Takže ze hry, kde mohlo dvacet lidí dostat po deseti tisících, odcházelo devatenáct lidí s prázdnou a jeden s tisícovkou. Základem tohoto chování je **situace, v níž člověk propadá pokušení udělat něco, co by bylo velkou chybou, kdyby to udělali i ostatní,** laicky řečeno **pokušení zachovat se jako svině.**

Pokud by ovšem účastníci hry uvažovali logicky, došli by zákonitě k této úvaze:_Všichni máme stejné počáteční podmínky a stejná pravidla, všichni uvažujeme stejně a proto se všichni rozhodneme stejně. Buď všichni zavoláme nebo nezavolá nikdo. No a z těchto dvou možností je lepší ta druhá, pak budeme mít všichni nejvyšší zisk._

Takovéto hry se nazývají **&#8222;hry s nenulovým součtem&#8220;**. Na rozdíl od **&#8222;her s nulovým součtem&#8220;**, kde součet výher a proher účastníků je roven nule (kolik vyhraje jeden, tolik musí druhý prohrát, např. karetní hry, přeneseně třeba i ekonomika) a proto se účastníci snaží maximalizovat svůj zisk a minimalizovat ztráty bez ohledu na to, co udělá protivník (podobnost s „morálkou” není náhodná), v hrách s nenulovým součtem výhra jednoho neznamená ještě nutně prohru druhého. Bohužel lidé si málo uvědomují, že většina rozhodování v mezilidských vztazích je právě tohoto druhu, situace typu „můžeme na tom vydělat oba, aniž by kdokoli další prodělal” nebo naopak „ať vyhraje kdo vyhraje, prodělají všichni”.

Jiným příkladem „hry s nenulovým součtem” je chování řidičů jedoucích proti sobě. Vyhnou-li se, oběma to prospěje, budou-li čekat „až ten druhý uhne”, šeredně na to doplatí (modifikace: Kdo v noci dřív ztlumí dálková světla).

Pro nalezení nejvhodnějšího algoritmu byly podmínky hry poněkud upraveny (na tzv. iterované dilema vězně):

Hráči byli simulováni počítačovými algoritmy. Každý se rozhodl zda SPOLUPRACOVAT nebo PODRAZIT. Pokud oba účastníci spolupracovali, dostali 7 bodů. Pokud oba podrazili, dostali po dvou bodech. Pokud jeden podrazil a druhý spolupracoval, „podrazák” získal 10 bodů a „slušňák” nic. Hrálo více účastníků předem neznámý počet kol a v každém kole sehrál každý s každým jednu partii. O výsledku rozhodoval konečný součet bodů. Hra tím dostala novou dimenzi — účastníci (zde počítačové algoritmy) si mohli pamatovat, jak se kdy kdo vůči nim zachoval a podle toho upravit své chování. A kdo zvítězil?

Algoritmy „křesťanské”, tj. vždy spolupracující, byly téměř okamžitě zničeny, pokud se mezi nimi ocitl jediný „podrazák”. Na druhou stranu nezvítězily ani algoritmy, které podrážely jak mohly. Nejúspěšnějším algoritmem se stal algoritmus TFT filosofa A. Rappaporta, popsaný jednoduše: **Začni spoluprací a pak vždy zopakuj předchozí krok partnera.** Tedy pokud partner spolupracuje, spolupracuj, pokud podrazil, podraž ho taky — jak ty mně, tak já tobě (už to začíná připomínat lidské chování, že?). Ukázalo se, že v prostředí s převahou algoritmů TFT nemají „podrazáci” šanci se prosadit, jsou izolovány a „hynou”. Tato strategie je úspěšná ale pouze tehdy, hraje-li se hra na více kol. Pokud předem víme, že hra bude mít jen jedno kolo a hráči se již nikdy nesetkají, je vždy výhodnější podrazit (o fungování tohoto pravidla se přesvědčují lidé v oblastech lásky i obchodních vztahů). Ale ruku na srdce — kdy opravdu na sto procent víme, že se už nikdy nepotkáme?

Strategie TFT svádí k domněnce, že je „evolučně stabilní” a vhodná k přežití, ale stejně stabilní je i vytrvalé podrazáctví. Navíc algoritmus TFT v prostředí plném podrazů brzy osamocen zahyne.  
Problém je, pokud do hry zavedeme náhodný prvek „nedorozumění”, tedy že spolupráce může být chybně pochopena jako podraz. Pak se algoritmy TFT můžou dostat do série vzájemných podrazů, ze kterých již nevybřednou. Proto byl tento algoritmus různě modifikován, např. TFTT — „Odpověz podrazem až na dva po sobě jdoucí podrazy protivníka” nebo na algoritmus, který občas „odpustil” a místo podrazu spolupracoval. Ale jako nejvýhodnější se v tomto případě ukázal jiný algoritmus, nazvaný Pavlov, který říká: **Neměň postup, jestliže tvůj protihráč spolupracuje, anebo jestliže se ti podaří podraz. Změň postup, jakmile ses stal obětí podrazu, anebo podrážíte-li oba.**

Tyto teorie se nechají aplikovat i na společenské vědy a dozvíme se z nich mnoho o motivech chování, o tom proč jsou jedinci (či spíše jejich ega) schopny altruismu atd. Na druhou stranu — v těchto fiktivních situacích se jedná o společnosti, v nichž všichni mohou zcela svobodně sledovat ty nejprotichůdnější zájmy, omezováni pouze doporučeními absolutně nestranných pravidel. Teorie her ovšem „nereálnost svého světa” nijak nezastírá.

Zájemce odkazuji např. na knihu **Keller, J.: Dvanáct omylů sociologie, Slon, Praha 1995, kap. Člověk pod rentgenem teorie her**, na díla Nashe (ano, toho z filmu **čistá duše**), Hofstadtera, Axelroda, na prameny o dilematu vězně, skvělý článek [sociobiologický exkurs — srovnávací etika a zdůvodnění etiky v sociobiologické a evoluční perspektivě](http://www.phil.muni.cz/fil/etika/kniha/kniha5.html) a pro hračičky nabízím odkaz na [hry o spolupráci](http://sweb.cz/isev/hry/spolupra.htm).