---
id: 1442
title: Jak nečíst Zdroják
date: 2013-09-03T08:12:07+01:00
author: Martin Malý
layout: post
guid: http://www.misantrop.info/?p=1442
permalink: /jak-necist-zdrojak/
dsq_thread_id:
  - "1698875382"
mashsb_timestamp:
  - "1575902816"
mashsb_shares:
  - "10"
mashsb_jsonshares:
  - '{"total":10,"error":"","twitter":10,"facebook_shares":0}'
image: /wp-content/uploads/2013/07/1207153_wireless_2.jpg
categories:
  - Nezařazené
---
Martin Hassman má skvělou vlastnost &#8211; nebude si následující text brát osobně. Takže doufám, že ani další čtenáři, kterých se věc netýká tak bezprostředně, nebudou hledat v článku něco, co tam není.

<!--more-->

Vedení Zdrojáku rozhodně Martinovi nezávidím. Sám jsem si to zkusil, a vím, že platí ono úsloví o &#8222;dělání nemožného pro nevděčné&#8220;.

Před časem jsme se o Zdrojáku bavili s Davidem Grudlem. Říkal jsem mu, že Zdroják nečtu, protože tam není nic, co by pro mě bylo nějak zajímavé. Jenže &#8211; co když tam něco zajímavého je, a já o tom akorát nevím, protože to nečtu? A tak když jsem včera zachytil na Facebooku odkaz na nový článek o SQLite, klikl jsem a přečetl.

Článek ([SQLite: Databáze pro váš web](http://www.zdrojak.cz/clanky/sqlite-databaze-pro-vas-web/)) je špatný od začátku do konce. Zaprvé mě překvapilo, že v roce 2013 někdo &#8222;seznamuje se SQLite&#8220; &#8211; měl jsem zato, že SQLite je naprosto běžná a standardní součást výbavy webových kodérů. Poprvé jsem ji použil někdy v roce 2007 na jeden menší projekt. V roce 2010 jsem o ní psal v souvislosti s WebSQL jako o &#8222;databázi, kterou není nutné představovat&#8220;. Inu, asi je. Je to možné, přít se o to nebudu, ale pokud představit, tak trošku jinak.

Autor (Vlastimil Pospíchal) pojal článek jako&#8230; jako&#8230; těžko hledat označení. Posuďte sami:

&#8222;Většina webhostingů mívá sice v nabídce jen MySQL a případně i PostgreSQL, ale po prostudování konfigurace je obvykle možné najít i pět dalších databází.&#8220; Proč zrovna pět? Jakých pět?

&#8222;Jedna z těchto pěti databází se může pyšnit tím, že umí jazyk SQL. Je to databáze SQLite&#8230;&#8220; Ach! Jedno oko nezůstává suché. Jedna z (nejmenovaných) pěti databází se pyšní SQL!

Autor pak píše o tom, že SQLite není vhodná pro sdílená úložiště (budiž), že nepodporuje řazení podle UTF-8, a hned za tím píše: &#8222;Situace s PHP či Pythonem je zcela jiná.&#8220; Hu! Zcela jiná než co? V tom smyslu, že tam umí UTF? Ale kdeže: &#8222;SQLite je přímo jejich součástí. Databázové soubory se lokálně otevírají v režii jádra operačního systému a nejsou tedy problémy s distribuovanými vyrovnávacími pamětmi. Zámky fungují tak jak mají i v případě, že se souborem pracují stovky skriptů současně.&#8220; Mno, tak &#8211; není součástí těchto jazyků, ale tyto jazyky nabízejí připravenou knihovnu s API. Ve zbytku se autor pravděpodobně snaží naznačit, že runtime těchto jazyků používá pouze jednu kopii knihovny SQLite (logicky&#8230;), a nedochází tedy ke konfliktům s vícenásobným přístupem.

&#8222;Nejsou zde vnořené procedury, ale vzhledem k tomu, že mezi aplikací a databází nedochází k síťovým přenosům, nejsou ani potřebné.&#8220; Vnořenými procedurami myslí autor asi procedury &#8222;uložené&#8220; (stored). Souvislost stored procedures se síťovými přenosy je pak zcela volná&#8230;

Závěr je pak velkolepý: Autor zmiňuje, že existují verze 2, 3 a 4, že verze 2 je zastaralá, tu nedoporučuje, verze 3 je používaná, tu by doporučil, a s verzí 4 se ještě pořádně neseznámil. Informační hodnota: 0.4 RTNOZ ([jednotka informační hodnoty](http://blog.maly.cz/index.php?item=841), 1 RTNOZ = informační hodnota Reportáže Televizních Novin o Zvířátkách). Pokud autor chce psát seznámení, možná by si měl dát tu práci a sepsat rozdíly mezi verzemi, když už si tedy nedá práci a neseznámí se s tím, co chystá nová verze.

A tohle, prosím, bude mít pokračování. Příště o třídě PDO.

(Když David v komentářích kritizoval slabou úroveň, odpověděl mu autor, cituji: &#8222;A navíc nehodlám v dalších dílech ani zmínit Dibi či Nette. To je troufalost, co?&#8220; Tím to Davidovi tzv. _nandal_. Podle posledních zpráv sedí David zamčený v koupelně, pláče a cpe se zmrzlinou z kyblíku&#8230;)

Dobrá, dobrá, jedna sova půlnoc nedělá. Sednul jsem si a poctivě si prošel články za poslední tři měsíce.

Článek o bezpečnosti webů od Michala Špačka je skvělý. Tedy &#8211; minimálně předmluva, ve které zmiňuje, jak hodnotil weby ve WebTop100 a jak jsou na tom po bezpečnostní stránce bledě. Bohužel, zbytek článku, ve kterém Spaze popisuje nejčastější chyby a ukazuje, jak se jim vyhnout, jsem nenašel.

Seriál &#8222;ORM test PHP frameworků&#8220; byl přijat na začátku s rozpaky, které Martin Hassman v komentářích rozptyloval. Jeho snažení mu bohužel zkazil sám autor tím, že sepsal mnohadílné WTF.

Z toho, co jsem četl, vyčnívaly články Jakuba Mrozka a Ladislava Prskavce (i když jeho recenze knihy o AngularJS patří mezi slabší momenty). Tito dva autoři píšou věci, které jsou i pro mne zajímavé. Ne snad že bych chtěl stavět eshop, ale tipy na vývojářské nástroje jsou výborné. Fajn jsou i texty Honzy Javorka, i když evangelizace Pythonu nepatří k mému oblíbenému čtení. Potěšil mě Ondřej Žára, který píše velmi dobře, takže i když píše o věcech, které mě nezajímají, tak to čtu s chutí.

Zbytek je&#8230; inu, jak to říct? Asi tak: Nezávidím Martinu Hassmanovi. Znám to sám. Když nejsou autoři, nenaděláš nic! Takže Martinovi přeju co nejvíc psavých autorů, aby se Zdroják dostal na úroveň, kdy ho zase nebudu číst proto, že mě nezajímá, ne proto, že má jalový obsah!