---
id: 2541
title: Raspberry Pi a domácí multimediální přehrávač
date: 2015-12-27T01:20:16+01:00
author: Martin Malý
layout: revision
guid: http://www.misantrop.info/711-revision-v1/
permalink: /711-revision-v1/
---
Raspberry Pi určitě znáte &#8211; jednodeskový počítač, poháněný ARMovým procesorem, s výkonným grafickým čipem (co zvládá video 1080p 30 a má H.264 HW dekodér), USB rozhraním, Ethernetovým připojením a výstupem přes HDMI. A takováhle sestava, to je vlastně ideální zařízení na to, abyste si ho připojili jedním koncem k televizi a druhým do domácí sítě. Něco jako svého času [Popcorn](http://www.amazon.com/gp/product/B005ZSBUC4/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B005ZSBUC4&linkCode=as2&tag=dein-20) a jiné NMT zařízení, nebo [Boxee Box](http://www.amazon.com/gp/product/B0038JE07O/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B0038JE07O&linkCode=as2&tag=dein-20).

<!--more-->

Udělal jsem to taky. Z minula jsem měl zkušenost s XBMC, což je velmi slušný a promakaný software pro domácí multimediální šmrdlání u televize. Bylo by divné, kdyby pro RPi neexistoval. A ono vida, existuje, a existují dokonce specializované distribuce.

Do Raspberry Pi (mám [256MB verzi](http://www.amazon.com/gp/product/B008XVAUPI/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B008XVAUPI&linkCode=as2&tag=dein-20), ale je k dostání i [512MB verze](http://www.amazon.com/gp/product/B009SQQF9C/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B009SQQF9C&linkCode=as2&tag=dein-20)) jsem si stáhnul celý software, který se jmenuje [Raspbmc](http://www.raspbmc.com/). Pár minut, zapojil jsem Raspberry, spustil, koukal na startovací linuxové povídání, a když došlo na síť, objevilo se &#8222;Sending discovery&#8220; &#8211; a na tom to celé shnilo. Googlil jsem řešení, nenašel jsem nic použitelného. Příčina byla pravděpodobně v tom, že nedostal adresu z DHCP. Chtěl jsem ho přepnout na statickou IP, ale jak? Přimountovat SD kartu k nějakému linuxovému zařízení a ručně přepsat konfiguraci by bylo asi nejsnazší, ale to narazilo na akutní nedostatek linuxových zařízení se SD sloty. Připojit se za běhu nešlo (nemělo IP adresu), nějak přerušit bootovací proces a dostat se do konzole se nepodařilo, takže jsem nakonec sáhnul jinam.

Existuje například distribuce OpenELEC, ale já sáhl po [Xbianu](http://xbian.org/). Instalace byla bezproblémová, změna IP konfigurace taky, a po spuštění se objevilo XBMC v plné kráse. Funkční a _cool_. Dokonce přehrává i HD filmy, tralala. Tím bychom tedy měli vyřešenou otázku &#8222;přehrávač médií&#8220;.

<a href="http://www.misantrop.info/raspberry-pi-a-domaci-multimedialni-prehravac/7167145172_46b1228dae/" rel="attachment wp-att-713"><img class="aligncenter size-full wp-image-713" title="7167145172_46b1228dae" src="http://www.misantrop.info/wp-content/uploads/2012/11/7167145172_46b1228dae.jpg" alt="" width="500" height="500" srcset="https://www.misantrop.info/wp-content/uploads/2012/11/7167145172_46b1228dae.jpg 500w, https://www.misantrop.info/wp-content/uploads/2012/11/7167145172_46b1228dae-200x200.jpg 200w" sizes="(max-width: 500px) 100vw, 500px" /></a>Mít přehrávač je jedna věc, mít k němu i slušné ovládání je věc druhá. Ale přeci nejsem jediný, kdo to používá, tak by někdo mohl mít nějaké řešení už vymyšlené, že&#8230; Tak jsem se zeptal:

<pre>Rozběhal jsem XBMC na <a title="RaspberryPi" href="http://hootsuite.com/dashboard#">#RaspberryPi</a>. Funguje skvěle, jen ovládání klávesnicí je nepraktické. Doporučíte nějaký ovladač?</pre>

Odpovědí jsem dostal několik:

  * @MichalJanda: Mne funguje ten od TV, mam to pripojene pres HDMI.
  * @Pebr0u: Pokud je připojená televize a ne monitor, lze ovládat přímo ovladačem od TV.<a href="http://t.co/8Al3waUi" target="_blank" rel="nofollow">goo.gl/Sw0Q3</a>
  * @klatys: pokud Ti nevadí, že to nebude opravdu ovladač, na všechny platformy je, pokud vím, mobilní aplikace&#8230;
  * @Solvina: Na IOS pouzivam (myslim ze oficialni) xbcmRemote. Daly by se tam vylepsit nejake detaily, ale u me nic zasadniho.
  * @tvrabec: Dálkový
  * @ivoshm: Ja používám YATSE z Androida, případně oficiální XBMC klienta &#8211; předpokládám, že bude něco podobného i na jiné mobilní OS.
  * @starenka: Ja jedu na openelecu. Ovladam to telefonem. Apek sou hromady. Na Androidu napr XBMC Remote
  * @Sustak: co ten od boxee? Onehdy sel koupit na Amazonu&#8230; (ale asi bude stat vic nez malina&#8230;)
  * @Bladezone: doma ho ovládám bezdrátovou bluetooth klávesnici z DealExtremu, i mámě vyhovuje. Možná něco podobnýho pro WP (+link na XBMC klient)
  * @SinyaWeo: Měláká tohle &#8211; <a href="http://t.co/5fOGJeIJ" target="_blank" rel="nofollow">dx.com/p/mele-f10-fly…</a> Ale až našetřím.
  * @tomasfejfar: a zkoušel jsi Lenovo &#8222;klávesnici do ruky&#8220;? <a href="http://t.co/FnH9VRNS" target="_blank" rel="nofollow">shop.lenovo.com/us/itemdetails…</a>
  * @fivebr: aplikace XBMC Remote do telefonu.
  * @v6ak: Já používal app pro Android. Pro WP možná taky něco je, případně jsou tu mobilní webové verze.

Takže když to shrnu: Spousta užitečných rad (za které děkuju), plus jedna úplně pitomá reakce. Užitečné rady si můžu rozdělit do tří kategorií:

1. Ovládání přes mobil / tablet. Ano, pro XBMC jsou klienti pro iOS, Android i WP, pro každou platformu hned několik, ale doporučuju udělat si takový pokus: Vezměte si dálkové ovládání od televize lomeno přehrávače, položte si ho na stůl, vedle něj položte svůj dotykový smartphone v klidovém stavu, a teď mi řekněte: Chci zapauzovat video. Co vezmu do ruky spíš? Bude to dálkové ovládání, kde se po hmatu zorientuju a zmáčknu pauzu, nebo to bude telefon, který tlačítkem rozsvítím, gestem odemknu, najdu tlačítko pro pauzu a dotknu se ho? (Neuvažuju situaci &#8222;&#8230; spustím XBMC Remote aplikaci, co se mezitím zavřela, a počkám, až se připojí&#8220;) Chci tím říct, že ovládání přehrávače mobilní aplikací v telefonu má možná svoje kouzlo (například že si můžete připadat übergeekovsky, nebo nemusíte hledat kam jste ovladač položili, stačí jen najít druhý mobil a na ten první si zavolat&#8230;), když vám je třiadvacet a žijete sami. Já chci, aby si i moje drahá dokázala pustit film, a nebudu jí kvůli tomu kupovat smartfon.

2. Možnost ovládat zařízení dálkovým ovladačem od televize, protože některé televize umí jaksi &#8222;protlačit&#8220; signál od ovladače skrz HDMI k tomu bazmegu, co posílá signál. XBMC to zvládne, pokud v něm máte knihovnu libCEC (a to v Xbianu je). Televize LG to zvládne taky (a jmenuje se to SmartLink). Jen holt to nezvládne, když je k HDMI připojeno víc zařízení, jak jsem se někde na nějakém fóru dočetl, když jsem zjistil, že mi to nefunguje&#8230; Ale kdyby to fungovalo, bylo by to boží!

3. Externí klávesnice, která nebude taková jako že od normálního PC, ale bude víc podobná dálkovému ovládání. To od Lenova se mi nelíbí, ale ta [Mele F10](http://www.amazon.com/gp/product/B009YPPR8M/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B009YPPR8M&linkCode=as2&tag=dein-20)&#8230; Za 35 dolarů to není vůbec zlé! (A možností je samosebou víc&#8230;) Tudy asi půjdu, to je, myslím, rozumný směr.

Díky všem, a až si nainstalujete, tak si nezapomeňte doinstalovat [ČSFD grabber](http://ldevel.blogspot.cz/2010/02/xbmc-scraper-pro-wwwcsfdcz.html).

<div class="alignleft">
</div>

<div class="alignleft">
</div>

<div class="alignleft">
</div>

<div class="alignleft">
</div>

<div class="alignleft">
</div>

<div class="alignleft">
</div>