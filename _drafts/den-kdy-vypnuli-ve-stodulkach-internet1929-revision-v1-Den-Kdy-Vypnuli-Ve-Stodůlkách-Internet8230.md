---
id: 1932
title: 'Den, Kdy Vypnuli Ve Stodůlkách Internet&#8230;'
date: 2014-03-02T12:21:18+01:00
author: Martin Malý
layout: revision
guid: http://www.misantrop.info/1929-revision-v1/
permalink: /1929-revision-v1/
---
Od anarchie takovejhle krůček!

<!--more-->

Včera ráno jsem zasedl k PC a sesynchronizoval GIT, že budu pokračovat v práci. Ještě jsem odpověděl na dva maily, a pak se najednou zaseklo načítání nových stránek&#8230;

&#8230; a taky mailů&#8230;

&#8230; a ani PING nevracel nic zajímavého.

Aha, nevadí &#8211; restartoval jsem router a &#8230; furt nic. Zkusil jsem se z notebooku připojit &#8211; furt nic. Aha, routerem to nebude, je to někde venku. Což v zásadě nevadí, protože mám mobilní &#8211; é, vlastně nemám nic mobilního! Zapomněl jsem, že přecházím z předchozího tarifu na neveřejný tarif, a je tam potřeba udělat mezikrok přes Twist. A já jsem teď právě v tom mezikroku. Na Twistu data nemám, ale můžu si je zapnout&#8230; v internetové samoobsluze! Nebo na infolince, jejíž číslo najdu na internetu!

Našel jsem smlouvu s T-Systems, tam byl telefon na zákaznickou linku (úmyslně tam nenapsali hotline), na kterou jsem se bez problémů dovolal, stisknul jsem 5 pro hlášení poruch a dozvěděl se, že &#8222;jsou mi k dispozici ve všední dny od osmi do 18 hodin, ale pokud opravdu chci nahlásit poruchu, tak tam mají záznamník&#8220;.

OMFG! WTF? DPRDL! Cože? V roce 2014 nemá poskytovatel vysokorychlostního internetu možnost nahlásit poruchu o víkendu?

Pustil jsem si na PC &#8222;ping 8.8.8.8 -t&#8220; a šel si číst.

Když jsem přečetl první knížku, bylo poledne a na PC furt běželo &#8222;cílová síť nedostupná&#8220;.

Fajn, co v takové situaci dělat? Relaxovat! Jenže nemůžete relaxovat, když jste nasraní, že nefunguje internet. Relaxovat můžu ve chvíli, kdy internet funguje a já se rozhodnu, že vypnu PC a budu relaxovat. To jsem v klidu, protože vím, že kdybych náhodou potřeboval, tak internet funguje.

Naštěstí mám spoustu práce offline&#8230;

Dočetl jsem dvě knížky o zločinu. Na Kindlu.

Zkusil jsem připojit PS/2 myš k [Atari ST](http://retrocip.cz/dva-prirustky-do-archivu/) (mám k tomu [nějaký takovýhle adaptér](http://www.ebay.com/sch/i.html?_trksid=p2047675.m570.l1313.TR0.TRC0.H0.X+Atari+ST+ps2+Mouse+Adapter&_nkw=+Atari+ST+ps2+Mouse+Adapter&_sacat=0&_from=R40)), což docela fungovalo, jen mi nedošlo, že bez nějakého SW na disketě s tím nenadělám nic.

Zkusil jsem si v Eagle navrhnout plošňáky k několika zapojením, co bych tu rád realizoval, totiž jednoduchý terminál (pro retrostroje), postavený pomocí starého 15&#8243; LCD a PS/2 klávesnice, mikropočítač s 68k a mikropočítač s nejúžasnějším osmibitovým procesorem 6809 (přesněji s jeho lehce vylepšenou variantou HD6309P).

Chvilku jsem si připravoval základ pro emulátor 6809 v JavaScriptu, porochnil se přitom v LiveScriptu&#8230;

Přečetl jsem si pořádně manuál ke Sharp PC.

Připravil jsem si další dva díly svého [kurzu programování osmibitů v assembleru](http://strojak.cz/). Už jsem se dostal za procesor 6502, teď probíráme základy práce s &#8222;reálným&#8220; hardware. Samozřejmě že emulátor, ale kdyby na to přišlo, postavit si ho můžete &#8211; autor Grant Searle mi dal souhlas s použitím jeho konstrukcí na mých stránkách, takže vesele používám jeho [SBC6502](http://searle.hostei.com/grant/6502/Simple6502.html). Teď jsme doprobrali výpis znaků na terminál, dokonce hned v několika různých variantách, v dalších dílech bude čtení klávesnice, dekódování, pár převodních rutin, no a skončím to jednoduchým monitorem. A pak, pak se asi vrhnu na tu Z80&#8230;

No a bylo šest hodin, internet furt nefungoval, já měl tohle všechno za sebou, navíc jsem viděl asi čtyři díly Mythbusters, a pobavil mě kolega Štěpán, který volal a chtěl něco poradit s IHNEDem. Chudák. Poradil jsem mu, ale taky jsem mu třikrát zopakoval, že mi nefunguje internet a popsal celou anabázi.

V půl sedmé jsem měl připravený scénář pro variantu &#8222;Odpojili mě!&#8220;, včetně toho, jak v pondělí v osm ráno křičím do telefonu: &#8222;Cože? Tak podívejte se, já tam k vám jedu, za 30 minut jsem tam, a doufám, že si do té doby najdete setsakra dobrý argument, protože vás tam utluču podepsanou smlouvou a potvrzením o zaplacení!&#8220;

V sedm jsem si šel lehnout, kouknul jsem na dalších pět dílů Mythbusters a spal.

Ráno se probudím, a na telefonu vidím, že mi v noci telefon stáhnul 26 nových mailů! Jupí, internet funguje! A záhy jsem zjistil, že T-Systems měli výpadek na celých Stodůlkách, dokonce i David Grudl, co bydlí nedaleko, [popisuje svou trýznivou zkušenost](https://www.facebook.com/davidgrudl/posts/10203067681553685?stream_ref=10). Prý nescházelo moc, a šel si povídat se sousedy! Po pravdě řečeno, variantu &#8222;zazvonit u sousedů a zeptat se, jestli jim taky nejde&#8220; jsem zvažoval, ale pak jsem si uvědomil, že bych se musel oblíkat, a že by mi ani kladná, ani záporná odpověď nijak nepomohly, tak jsem buddhisticky zůstal sedět doma v trenýrkách.

Jako cvičení dobré, ale přesto bych byl příště radši, kdyby to bylo dobrovolné&#8230; (A nejradši bych byl, kdyby si T-Systems laskavě zřídili hotline na víkendové výpadky!)