---
id: 833
title: 'Zvu vás na ochutnávku&#8230;'
date: 2013-02-12T16:20:56+01:00
author: Martin Malý
layout: post
guid: https://misantrop.info/?p=833
permalink: /zvu-vas-na-ochutnavku/
dsq_thread_id:
  - "1079210068"
mashsb_timestamp:
  - "1575148200"
mashsb_shares:
  - "3"
mashsb_jsonshares:
  - '{"total":3,"error":"","twitter":3,"facebook_shares":0}'
image: /wp-content/uploads/2013/02/pacman.png
categories:
  - Nezařazené
---
Něco pro milovníky oldskool vintage her a [staré hráče](https://www.oldplayer.cz/), a taky pro JavaScriptaře. Jedni si užijou, ti druzí se poučí. Teď poodhrnu oponu chystaného webíku&#8230;

<!--more-->

Webů s hrami je na internetu neuvěřitelně moc. _<span style="text-decoration: underline;">Kdo jste nikdy neviděl Donkey Konga ve Flashi, tak ruku nahoru!</span>_ Přidávat další je jak nosit sovy do Athén a dříví do lesa. Dovolil jsem si jeden přidat, ale i s osvětou&#8230;

Mám totiž rád staré hry. [Od mládí](https://www.oldplayer.cz/hrichy-mladi/). Dokonce tak rád, že mám doma postavenou _úplně vlastnoruční vintage konzoli_, a až bude jednou čas, tak si pro ni přeportuju pár starých her.

Totiž, abyste věděli, staré hry nejsou vůbec složité. Přeprogramoval jsem si před pár lety Manic Minera do JavaScriptu. Je to triviální &#8211; pokud si tedy pamatujete, [jak to bylo původně udělané](https://www.seasip.demon.co.uk/Jsw/manic.mac). O jeho vývoji jsem napsal článek s takovým jako že &#8222;howto&#8220;, ale dřív, než jsem ho dopiloval, tak jsem ze Zdrojáku odešel, a už jsem se na to vykašlal.

Moje _úplně vlastnoruční vintage konzole_ používá jádro procesoru 6502, a to je, pokud to nevíte, extrémně jednoduchý procesor. A takhle extrémně jednoduchý procesor je extrémně jednoduché emulovat, třeba, hmmm&#8230; třeba v tom JavaScriptu. Takže jsem si napsal emulátor 6502 v JS, připravil správné časování, a když už jsem byl v tom, napsal jsem i takovou minisérii článků: Jak napsat emulátor CPU v JS. Ale než jsem ho dopiloval, tak jsem začal mít práce nad hlavu.

A když máte 6502 CPU, co takhle zkusit emulovat i něco víc? Hmmm&#8230; Co třeba Apple ][, šlo by? Jasně že by šlo, ale co třeba Atari 2600? To je výzva! Takže jsem si připravil emulátor Atari 2600 (ne, není to vůbec jednoduché a naemulovat zobrazovací mechanismus, který je převážně založený na principu přesného časování a čekání, je dost _tricky_). Ale než jsem ho dopiloval, tak mě pohltilo Druidly a já měl jiné starosti.

Říkal jsem si, ještě na Zdrojáku, že jsou čtenáři takoví hračičkové, že by nemuselo být marné je nechat, ať zkusí napsat nějakou hru do 1KB. V assembleru. Buď pro reálný stroj, třeba pro tu 2600, nebo pro něco fiktivního, vzniklého právě na základě toho emulátoru. Takže jsem k emulátoru dopsal i IDE a assembler, v JavaScriptu, s využitím LocalStorage pro ukládání souborů. Ale než jsem ho dopiloval&#8230; _Kruci, co to je?_

&#8212;

Bystřejší čtenáři už asi pochopili, kam tím mířím, a oběma je jasné, že mám plný pytel různých takových podobných javascriptových vyfikundací, k tomu v různém stádiu rozepsání i _sérku článků_ o tom, jak se takové věci v JS píšou, a že bych to teď třeba nějako chtěl zkonsolidovat. Assemblery a IDEčka dát na web jako službu, emulátory ke stažení, články vydat&#8230; Ono je to totiž velmi zajímavé, a začíná to být stále zajímavější, protože poslední prohlížeče už dokážou emulovat i zvuk.

Ale k věci: Nabízím vám ochutnávku [herní klasiky](https://herni-klasika.cz) &#8211; a vězte, že tam je jen JavaScript, žádný Flash, žádná Java, a ten zvuk, co slyšíte (ano, opravdu slyšíte tříkanálový zvuk ZX Spectra 128), je dělaný furt v tom JavaScriptu (samosebou s podporou prohlížeče) ((takže jo, nejlepší bude, když tam polezete s Chromem nebo novým FF; IE10 jsem netestoval, ale IE9 je úplně marný; Safari ani Operu jsem netestoval)).

No a o tomhle všem bych rád připravil takový seriál, k tomu nějaké ty zdrojáčky, _nech sa páči_&#8230; Ano, bude právě na tom webu, a budou tam i další klasické hry, nejen ze ZX Spectra, pokud to licence dovolí&#8230;

&nbsp;

Takže _stay tuned_ (a jestli to nemůžete vydržet, tak vám třeba pomůže [nějaká pěkná stará hra](https://herni-klasika.cz/)).