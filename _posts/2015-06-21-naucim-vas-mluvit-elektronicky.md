---
id: 2320
title: Naučím vás mluvit elektronicky!
date: 2015-06-21T12:31:05+01:00
author: Martin Malý
layout: post
guid: https://misantrop.info/?p=2320
permalink: /naucim-vas-mluvit-elektronicky/
mashsb_timestamp:
  - "1576258648"
mashsb_shares:
  - "33"
mashsb_jsonshares:
  - '{"total":33,"error":"","facebook_shares":0,"twitter":33}'
image: /wp-content/uploads/2015/06/switch-2-909878-m.jpg
categories:
  - Nezařazené
tags:
  - elektronika
  - hobby
  - výuka
---
Chcete?

<!--more-->

Před nějakou dobou jsem si tak trošku postěžoval ([tady třeba](https://kcc.misantrop.info/2015/05/15/literatura/), nebo [tady](https://kcc.misantrop.info/2015/05/22/didaktika/), nepřímo i [tady](https://kcc.misantrop.info/2015/05/21/jednoduche/)), že mi připadá trochu nevyužitý potenciál současné elektroniky. Když to srovnám s dobou před třiceti lety, kdy jsem nesehnal skoro nic, ale zato jsem měl knížky s návody na stavbu lecčeho, tak mi přijde, že dneska máme skvělé a levné možnosti naučit se pracovat s elektronikou (kity za hubičku, součástky za půl darma, nástroje za cenu jednoho obědu s polévkou a limonádou), máme i lidi, které by to bavilo, ale nemáme k tomu _notičky_.

Co tím myslím: Není problém vzít do ruky Arduino, podle barevného obrázku propojit dráty, napsat sketch a spustit. Pokud neuděláte někde chybu, bude to fungovat. Jenže tomu něco chybí. Chybí tomu ten přístup &#8222;tak, teď víš všechno potřebné, zkus si udělat to a to a to&#8220; &#8211; tedy cvičení adekvátní probraným znalostem. Trochu se o to snaží příručka Začínáme s Arduinem ([zdarma na Arduino.cz](https://arduino.cz/))

Na něco podobného jsme kdysi narazili s Patrickem Zandlem při diskusi o tom, jak naučit děti programovat. Patrick měl děti ve věku, kdy už mohly začít s programováním, dokonce je to zajímalo, tak tehdy našel [Scratch](https://scratch.mit.edu/) a nechal děti, aby si hrály. Ideální nástroj pro edukační aktivity &#8222;otec &#8211; dítě&#8220;, ale problém je v tom, co Patrick pojmenoval &#8222;nedostatek metodických materiálů&#8220;. Tedy to, že ho nenapadaly vhodné příklady, co s dětma dělat, aby byly adekvátní znalostem, aby je nepřetížil nějakými složitostmi na začátku (a neotrávil je tím), nebo aby po nich nechtěl trapně jednoduché věci, zároveň aby to bylo dostatečně zábavné a poutavé&#8230;

Tentokrát jsme se potkali se Štěpánem Bechynským. On mnoho let vysvětloval programátorům Microsoftí produkty, takže v něm ta didaktická touha přetrvala. Ve mně zjevně taky. Navíc máme oba rádi elektroniku takovým tím amatérským způsobem (víte, že slovo _amatér_ pochází z _amare &#8211;_ tedy_ milovat?_) &#8211; neživíme se elektronikou, nestudovali jsme ji, není to pro nás denní chleba. Tyhle věci tak nějak zapadly do sebe a dohodli jsme se, že společnými silami, takříkajíc viribus unitis, připravíme přesně to, co by dle našeho názoru mohlo zaujmout. Nechci prozrazovat víc, zatím je vše ve stádiu příprav.

Ale zároveň mě minulý týden na dovolené napadl takový _spin-off_, který se s tou ideou, co máme se Štěpánem, potkává a rozšiřuje ji, takže by výrazně překročil rámec toho, co chceme dělat. Na druhou stranu by to bylo docela dobré doplnění a nadstavba pro to, co chystáme, pro trochu jinou cílovku.

Totiž &#8211; co to takhle vzít ještě z jiného konce? Představuju si člověka, co třeba umí programovat, ale zajímá ho elektronika a rád by se s ní seznámil nějak líp, intenzivněji a do hloubky. Tak pro takového člověka připravit praktického průvodce elektronikou a číslicovou technikou. Obsah nějak takhle, ale nikoli v tomto pořadí:

  * základy elektřiny někde na úrovni Ohmova zákona, ale spíš než abstraktní čísla bych raději popsal nějakou vizualizaci elektřiny, tedy &#8222;co si pod tím představit&#8220;
  * rychlokurs &#8222;jak číst schéma&#8220;
  * co to je rezistor, kondenzátor, cívka &#8211; ne počítat fázový posun, ale ukázat elementární fungování
  * jak a proč funguje dioda, tranzistor
  * hradla a logické výrazy (asi jen na úrovni fungování, de Morganovy zákony ano, Karnaughovy mapy spíš už ne)
  * jak se z hradel poskládají klopné obvody
  * &#8230; a ještě složitější obvody (paměti, dekodéry, čítače) &#8211; k tomu vždycky reprezentaci v &#8222;programátorském světě&#8220;
  * procesory, procesory, procesory! Jaké jsou, jak jsou uvnitř zapojené, jak se programují, k tomu [stroják](https://strojak.cz) čili assembler&#8230; Na úrovni osmibitových strojů
  * Arduino. Když už máme ten procesor, tak ať taky pracuje!
  * víc Arduina. Jak zapojit sofistikované shieldy (Ethernet, Bluetooth, Cojávímcoještě) a jak je rozchodit
  * internet věcí, věci na internetu&#8230;
  * jak si z procesoru a dalších věcí okolo poskládat počítač. Osmibit, jak jinak
  * jak fungují počítačové periferie, jak je postavit, jak využít existující
  * jak se pracuje s displejem. Textový displej, grafický displej, sprity, vlastní akcelerátor&#8230; Jak vzniká obraz, jak udělat výstup na TV i VGA
  * jak se dělá zvuk &#8211; od [jednobitového](https://retrocip.cz/symfonie-na-jednom-bitu/) po všechny ty SIDy a AY
  * jak se programují osmibity, prakticky a názorně na Z80, 6502, 6809, AVR, a k tomu i nějaké kuriozity
  * [VHDL](https://vhdl.cz), Verilog a [FPGA](https://fpga.cz)
  * jak si ve [VHDL](https://vhdl.cz) navrhnout vlastní mikroprocesor
  * jak ten vlastní mikroprocesor rozchodit
  * jak ten vlastní mikroprocesor [emulovat](https://webscript.cz/emulujeme-osmibit-javascriptem/)
  * [jak emulovat celé počítače](https://webscript.cz/emulujeme-osmibit-javascriptem-dil-druhy/)

Slušná nálož, co? V podstatě to je to, čemu jsem se věnoval posledních cca osm let, doplněné o znalosti, které sbírám od dětství. Možná bych to rozdělil na dva díly&#8230;

Každopádně bych nezačínal Ohmovým zákonem, to ani náhodou. Začal bych někde u Arduina, něčím, co můžete rychle připojit, rozchodit, a za dvacet minut vám to bliká. A k tomu přidávat. Blikání různě dlouhé, v různém rytmu, pak třeba semafor, reagování na tlačítko, nějaké vtipné zapojení, a pak postupně směrem dolů, k tomu Ohmovu zákonu. Tedy od toho, co člověk vidí a z čeho má hned zpětnou vazbu, na chvíli k teorii, od teorie zase zpátky do praxe, a tak dál. No a na konci by měl být člověk schopen nejen vymyslet vlastní zapojení a oživit ho, ale taky by měl vědět, co k čemu použít, jak to spolu funguje a hlavně: Kam jít, když ho bude zajímat víc teorie a víc do hloubky. Ode mne se nedozví, jak nastavit pracovní bod tranzistoru nebo spočítat Čebyševův filtr. Ale bude vědět všechno, co bude potřebovat ve chvíli, kdy ho napadne, že si postaví nějakou elektronickou věc.

(Mimochodem, jestli se ptáte, proč Arduino, proč ne Raspberry, Galileo, Beagle, Xpresso, &#8230; tak z mnoha důvodů: je jednoduché, dobře dostupné, dostatečně výkonné na to, aby si člověk udělal něco zajímavého, není překombinované, není složité&#8230; Pro seznámení s elektronikou a &#8222;osahání&#8220; je to ideální věc. Navíc mi připadá jednodušší připojit Arduino přes USB k počítači, než rozběhávat Raspberry s monitorem a klávesnicí a laborovat s Pythonem či čím&#8230;)

Analogicky k výuce jazyků: Dozvíte se, jak se &#8222;dorozumět elektronicky&#8220;. Nebude z vás překladatel ani spisovatel, natož lingvista, ale napíšete dopis a přečtete si noviny.

No a napadlo mě, že by bylo fajn k tomu průvodci nabízet i sady, kity k praktickému odzkoušení. Takže třeba to Arduino, pár shieldů, FPGA kit, hrst součástek, čidel, periferií&#8230;

A jak jsem si tak o dovolené točil volantem, tak jsem si řekl, že bych možná otestoval zájem na nějakém HitHitu či Startovači. Třeba se ukáže, že to nemá smysl, že by to chtělo deset lidí. Anebo naopak, kdo ví? Bylo by to fajn a asi by mě to i hodně bavilo&#8230;

Mimochodem, jestli chcete vědět, co mě inspirovalo, tak to byla skvělá kniha [Od krystalky k modelům s tranzistory](https://www.facebook.com/pages/Pavel-%C5%A0rait-Od-krystalky-k-model%C5%AFm-s-tranzistory/281815758886) od Pavla Šraita. Sice jsem měl jen dva tranzistory a když jsem si chtěl postavit něco jiného, musel jsem to předtím rozpájet, ani voltmetr jsem neměl a naprostá většina těch konstrukcí pro mne byla nedostupná, ale tu knihu jsem měl rád a vzbudila ve mně touhu stavět elektronické věci. Rád bych tu touhu předal dál.