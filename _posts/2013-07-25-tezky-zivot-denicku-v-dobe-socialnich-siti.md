---
id: 1387
title: 'Těžký život deníčků v době sociálních sítí&#8230;'
date: 2013-07-25T20:11:43+01:00
author: Martin Malý
layout: post
guid: https://misantrop.eu/?p=1387
permalink: /tezky-zivot-denicku-v-dobe-socialnich-siti/
dsq_thread_id:
  - "1531397969"
mashsb_timestamp:
  - "1546022005"
mashsb_shares:
  - "0"
mashsb_jsonshares:
  - '{"total":0,"error":"","twitter":0,"facebook_shares":0}'
image: /wp-content/uploads/2013/07/1207153_wireless_2.jpg
categories:
  - Nezařazené
---
Narazili jsme v práci na takové dilema. Rádi bychom blogovali, ale vlastně vůbec nechceme psát blogy, taky na to nemáme čas, ale když máme ty sociální sítě, tak proč nepoužít je, že?

<!--more-->

Máme v IHNEDu takové dilema. Náš kreativní koutek (a.k.a. _chráněná dílna_) naráží na komunikační problém. Totiž:

Pan A. (říkejme mu třeba Adam, to bude vhodné) neustále experimentuje s webem, analýzou, metrikami a sleduje novinky ve světě a na internetech z hlediska novinářského. Jiný kolega zase přichází s nápady, další kolegové zase při šťourání nacházejí různé vývojářské perly a nástroje, ale cítíme, že nám to tak trošku proplouvá mezi prstama. Obzvlášť ve chvíli, kdy něco řešíte, a kolega od vedlejšího stolu řekne: &#8222;Hele, a není to to, jak o tom tuhle mluvil Honza, že na to je nějaký nástroj?&#8220;

Je to vono. Ale co s tím? Jak ty informace udržet a efektivně předat?

S panem Adamem jsme na to téma zavedli řeč. Adam říkal, že by rád tyhle informace s námi sdílel, ale nechce se mu blogovat, protože to jsou &#8222;jen takové útržky&#8220;, a vlastně by byl rád, kdyby ty informace šly jen dovnitř. Přišel tedy s nápadem, že by psal na Google Plus, pod firemním účtem (máme totiž všichni Google Accounts, heč!) Jenže když si udělal rychlý průzkum mezi ostatními, tak zjistil, že:

  * <span style="line-height: 13px">první potenciální čtenář leze na Google Plus jednou za měsíc, a to i když na něj svítí to číslíčko.</span>
  * druhý potenciální čtenář na svém Google Plus účtu byl naposledy před dvěma měsíci, a i když na něj svítí číslíčko, tak se ještě nedonutil kliknout. A to je řeč o soukromém účtu! O firemním ani nemluvě.
  * třetí, čtvrtý, pátý, šestý a sedmý potenciální čtenář prohlásili, že Google Plus asi ani nemají, mít nechtějí, a pokud mají, tak o tom ani nevědí.

A to jsou, prosím, vývojáři, novináři a částečně i geekové! Zbytečnější sociální síť je, z tohoto úhlu pohledu vzato, snad už jen Socl.

Nakonec jsme se shodli na tom, že asi nejjednodušší bude založit skupinu na Facebooku. Ve hře byly nejrůznější varianty i požadavky (-&#8222;Já bych chtěl, aby mi přišel mail pokaždé, když tam něco napíšeš.&#8220; -&#8222;To bys nechtěl, věř tomu!&#8220;), a nakonec jsme usoudili, že Facebook taknějak máme všichni, tak proč ho, v zásadě, nepoužít?

(Pokud si teď říkáte, proč se jen tak nesejdeme a nepokecáme, tak předesílám, že se scházíme a kecáme pravidelně, ale všichni máme natolik pestré životy, že nejsme schopni udržet všechno zajímavé, co potkáme cestou, v hlavě až do dalšího setkávání, a kdybychom se potkávali pokaždé, když nás něco napadne, tak v zásadě nebudeme mít čas na práci.)

To je první část problému. Říkejme mu třeba &#8222;problém pana Adama&#8220; (což by byl, mimochodem, dobrý název pro rockovou kapelu). Pak je tu druhá část, ta moje.

Děláme takové podivnosti, jako jsou různé klikací mapy a vizualizace a tabulky a grafy, a naše práce je trošku specifická v tom, že v pondělí ráno dostane šéfeditor nápad, co by se mohlo udělat, v úterý to musí být hotové a ve středu v 6:30 to jde na web. No a za týden to je už pasé jak týden staré noviny (_toto __přirovnání bylo schváleno Evropskou komisí pro velmi suchá přirovnání_). Takže občas musíme zaimprovizovat a pečlivě zvážit, co je únosný hack a co je už hodně velká prasárna. Princip good enough v praxi. Není čas psát krásný kód, za to žádného kodérského Pulitzera nedostaneme. Je třeba napsat kód dobrý (tedy funkční a znovupoužitelný), a napsat ho rychle.

No a při tom nacházíme jednak nástroje, co nám tu práci usnadní, jednak si taky něco píšeme my sami, a protože jsme tak trošku pankáči, tak něco z toho chceme dát ven jako open source. Ideální prostor pro to založit si blog&#8230;

&#8230; jsem si říkal. Ale kde a jak?

Datažurnalisti používají blogovací systém IHNEDu. Po konzultaci s kolegou, který se o něj stará, jsem došel k názoru, že to opravdu není vhodná cesta. WordPress.com jsem zkusil a zavrhl, když jsem zjistil, že si nemůžu nastavit hezké odkazy. Blogger.com jsem tuhle zase viděl, a přišel mi furt extrémně divný&#8230; WordPress na vlastním serveru by asi bylo rozumné řešení (na mém soukromém vlastním serveru, ne na IHNEDích&#8230;), ale furt se mi do toho nějak moc nechce, ani nevím proč.

A tak to možná dopadne tak, že budeme pankáči se vším všudy a uděláme si vývojářský blog na GitHubu s backendem v Node.js.