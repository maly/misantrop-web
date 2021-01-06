---
id: 2774
title: 'Kurz číslicové techniky &#8211; vaše názory'
date: 2017-02-23T12:16:27+01:00
author: Martin Malý
layout: post
guid: https://misantrop.info/?p=2774
permalink: /kurz-cislicove-techniky-vase-nazory/
mashsb_timestamp:
  - "1575140403"
mashsb_twitter_handle:
  - adent
mashsb_shares:
  - "30"
mashsb_jsonshares:
  - '{"total":30,"error":"","facebook_shares":30,"twitter":0}'
image: /wp-content/uploads/2017/02/mother-board-electronics-computer-board-39290.jpeg
categories:
  - Nezařazené
tags:
  - elektronika
  - Kurz
---
Díky všem, co [vyplnili anketu](https://misantrop.info/kurz-zakladu-cislicove-techniky/). Zatím se sešlo 74 odpovědí, takže klidně odpovídejte dál&#8230; Z dosud došlých reakcí usuzuju následující:

<!--more-->

**Videa** nejsou nezbytná. Pozitivně se vyslovilo 33 % (13 % spíše ano, 20 % rozhodně ano), 36 % odpovědělo spíš ne nebo ne, zbytek byl uprostřed. Vychází mi z toho, že video je vysloveně jako pikantérie a perlička, když budu ukazovat něco fakt zajímavého.

**Interaktivní webový simulátor** je oblíbená věc a trefa do černého. 66 % ho hodnotilo nejvyšším počtem bodů, 27 % pak čtyřmi hvězdičkami. Bude rozhodně pokračovat, nebojte.

**Sada součástek** je taky docela žádaný benefit. Možnost _Rozhodně ano_ volilo 30 %, možnost _Spíš ano_ dokonce 36 %. Takže asi nějakou sadu připravím, a to jak v podobě nákupního seznamu, tak v podobě hotové sady, kterou dodám já sám.

**Cena sady **trošku rozdělila respondenty. 23 % by se rádo vešlo do 200 Kč. Což by asi šlo pro tu nejjednodušší sestavu, ale i přesto zajímavou. 31 % by bylo ochotno jít až do 500 Kč. Sada do pětistovky by pokryla číslicovou logiku i kus analogové techniky (tranzistory, oscilátory, kondenzátory, senzory), a asi by se dalo pracovat i s nějakým hezkým jednočipem. 13 % zájemců by šlo i do tisícovky. Myslím, že bych byl schopen sestavit takovou sadu, aby v té tisícikoruně bylo vše podstatné &#8211; snad kromě plošných spojů a páječky. Rovná čtvrtina respondentů by byla ochotna zaplatit i víc, pokud by součástky byly fakt zajímavé. Asi by ani to nebyl problém. Co třeba vlastní FPGA na experimenty? Můj závěr: připravit třeba tři úrovně sad, beginner, experience, advanced, s tím, že by na sebe navazovaly a daly by se použít i společně, takže kdo by si koupil začátečnickou sadu a později šel do pokročilé, neměl by doma zbytečně sadu součástek.

**Workshop**, tedy cokoli naživo, celá polovina účastníků označila za něco, bez čeho se obejdou. Necelá třetina by si dala půldenní akci, pětina celodenní školení. Tady bych to prozatím nechal otevřené, především kvůli (svému) času.

**Papírová verze** je pro 30 % nezajímavá. Pro 43 % z vás by bylo fajn, kdyby byly k dispozici PDF s nějakou redakční úpravou. 19 % by přivítalo brožuru. Zamyslím se nad tím, a uvidíme podle dalších ohlasů.

**Můj plán** je následující: po kombinačních obvodech dáme sekvenční (klopné obvody, čítače, registry, paměti), a pak z toho, co už známe a máme, navrhneme a poskládáme vlastní procesor. Není to složité, není to nemožné, a vede k tomu cesta přes, odhadem, dalších 15 lekcí. Ve skutečnosti jich bude o něco víc, protože mezitím odbočíme k fyzikálním základům elektroniky, řekneme si, co je proud a co napětí, proč není dobrý nápad sahat do přístroje hned po jeho vypnutí, zkusíme si něco s kondenzátorem, něco s cívkou (připravte si špulku od nití a spoustu lakovaného drátu!), ukážeme si senzory světla, tepla, budeme pískat a blikat a taky si povíme takové ty věci, co je dobré vědět i při práci s číslicovou technikou, abychom se nedivili, že něco nefunguje, něco jiného hřeje a něco nesvítí tak, jak by svítit mělo. Nebudou to vysokoškolská skripta, spíš se připravte na to, že budete potřebovat místo na stole, baterku, drát, a že budete měřit, zkoušet, testovat, &#8230;

Tohle je de facto první část kurzu. Druhou část bych rád věnoval návrhu vlastního počítače a pokročilejším tématům. I na VHDL dojde.

Myslím, že jsem tím odpověděl i na několik dotazů ze **vzkazů**.

V první řadě: děkuju všem za podporu a pochvalu, moc mě to těší a motivuje k dalšímu psaní. Z dalších vzkazů vybírám:

> Mozna neni uplne spatny napad, pridavat jen tak na okraj i popis ve vhdl (viz tento dil). Nemusi byt nijak sahodlouze komentovan ale k dokresleni funkce obvodu by to bylo prima

Ano, bylo by to fajn, a já to zvážím. Možná alespoň v nějaké zjednodušené formě.

> Urcite chci pokracovat i v praktickych pokusech, tedy poridit si arduino a dalsi soucastky a zkouset si sestrojit ruzne aparatky.
> 
> Hlavne prakticke aplikace, teorie je sice fajn, me jde predevsim o pochopeni jak se to aplikuje -> chci se naucit jak veci funguji a pripadne si je pak sam (se synem) vytvorit.

Praxe je moje oblíbená disciplína, ale v tomto kurzu se chci věnovat i té teorii. Důvod je prostý: lidi se často podívají na nějaký návod &#8222;jak postavit to či ono&#8220; a zvládnou to postavit. Ale pak se, logicky, ptají: _Co jsem to vlastně udělal? A co je potřeba znát, abych to dokázal vymyslet sám?_ A právě v tomto jim chci pomoci.

> bohuzel chybi mi uplne elementarni zaklady fyziky abych se dostal ke skutecnemu hrani s HW. Pripadny online kurz na simulatorech muze byt ok, ale bez nutnosti skutecneho basteleni to nebude ono. Primlouval bych se, kdybyste nabidl k prodeji nejaky pripraveny HW kit (nebo dal dohromady seznam soucastek s odkazy na ebay) pomoci kterych by probihala vyuka. Pak placene sady clanku/video tutorialu kde bude mozne sestavit nejakou blbost. Clovek pak bude vedet, ze si koupi soucastky za 3 tisice a projde kurzem (samozrejme neni problem pokud bude placeny) a na konci (s jasne deklarovanou cenoou) si postavi treba pidirobota, dron, webserver na baterky etc.

Ano, plusmínus takto si to představuji. Na webu teorie a simulace, ale zároveň k tomu sady součástek pro reálné hraní. proto jsem se na to ptal a proto jsem se ptal i na to, kolik je pro vás přijatelná hranice.

> Určitě by bylo fajn to vzít z nějakého jiného konce než to berou všechny skripta a učitelé. Vysvětlit třeba nějaké reálné obvody, paměti.

Přesně to zazní. Třeba konkrétně u těch pamětí: začneme tím, jak vlastně donutit křemík, aby si něco pamatoval, ukážeme si základní stavební jednotku paměti SRAM, totiž klopný obvod, ukážeme si, jak se z nich poskládají registry a z registrů paměťové buňky a z kombinačních obvodů dekodéry a multiplexery dat, ukážeme si schéma té paměti, a pak si ji ukážeme i fyzicky: jako obvod, se kterým můžeme experimentovat. A po čase přidáme sériové paměti. Mimochodem, víte, jaký je rozdíl mezi sériiovou pamětí a paralelní? I to se dozvíte.

Nezapomněl jsem na něco? Nebylo tam v té anketě ještě něco? Bylo, a nezapomněl. Nechal jsem si to na konec. Otázka zněla: **Přispěju na vytvoření dalších dílů?**

10 % respondentů uvedlo odpověď _Ne, je to zbytečné_. Třetina respondentů by přispěla nějakým drobným příspěvkem v rozsahu desetikoruny za díl. Rovná polovina pak je ochotna zaplatit několik stokorun za ucelený kurz. Což mě potěšilo &#8211; lidé si uvědomují, že s tím mám nějakou práci a že na psaní věnuju svůj volný čas, a děkuju za to. Zároveň si říkám, jestli by nebylo na místě využít třeba [Patreon](https://misantrop.info/patreon/), kde je možnost přispívat na tvorbu obsahu, a to třeba od jednoho dolaru, což je cca dvacka. Některé díly by tak mohly být přístupné nejprve pro přispěvatele a veřejné až po čase, některé speciální by mohly být pouze pro přispěvatele&#8230; Co myslíte, je to dobrý nápad? Druhá možnost je nechat kurz veřejný a příspěvky ponechat dobrovolné s tím, že některé nepovinné lekce budou pouze pro přispěvatele.

Mimochodem, troška datového porna: Ve skupině &#8222;přispěju i v řádech stokorun za kurz&#8220; jsou lidé ochotni zaplatit za sadu součástek 500, 1000 i více Kč. Skupina &#8222;desetikoruny per lekce&#8220; zase nabízela nejčastější odpověď &#8222;součástky do 200, do 500 Kč&#8220;.