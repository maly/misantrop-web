---
id: 1410
title: 'Arthur Dent inspirující&#8230;'
date: 2013-08-18T09:39:48+01:00
author: Martin Malý
layout: post
guid: http://www.misantrop.info/?p=1410
permalink: /arthur-dent-inspirujici/
dsq_thread_id:
  - "1614692813"
mashsb_timestamp:
  - "1575348082"
mashsb_shares:
  - "3"
mashsb_jsonshares:
  - '{"total":3,"error":"","twitter":3,"facebook_shares":0}'
image: /wp-content/uploads/2013/08/zx_badaloc_02.jpg
categories:
  - Nezařazené
tags:
  - Osmibity
---
Hledal jsem drobnost o elektronice a našel jsem sám sebe&#8230;

<!--more-->

Jak p.t. čtenářstvo asi ví (možná ne), mým koníčkem je kromě programování a dráždění blbů i mikroelektronika. Mám o ní dokonce jeden takový [bložík](http://www.uelectronics.info/), s bohatým [archivem](http://www.uelectronics.info/index-old), ale dnes skomírající a živený jen [&#8222;curated news&#8220; Twitterem](https://twitter.com/uelectronics), který používám jako odkladiště na nápady, co jednou realizuju&#8230;

Ono to totiž souvisí se [starým snem](http://blog.maly.cz/index.php?cmt=786). Stále mě nepustil, i když pájka dočasně zahálí a já se musím věnovat jiným věcem. Jednoho dne ale opráším fotocuprextit a vrhnu se zas na stavbu nějakého gadgetu. Do té doby si musím vybít svoje nutkání jinak.

Tak například takovým osmibitovým webovým IDE, tedy editorem / assemblerem / emulátorem. IDEa mě napadla už před lety, a tehdy jsem si zbastlil první prototyp pro procesor Z-80. Na webu je velký editor (JS) a emulátor (Flash), assembler funguje na serveru (Pasmo), no a ultimátní test byl překlad Manic Minera ze [zdrojáku](http://www.seasip.demon.co.uk/Jsw/manic.mac). Nojo, ale elektrošotouši jsou, čest výjimkám, spolek ještě konzervativnější než programátoři. &#8222;Cože? Na co, používám DOSový assembler a bohatě mi stačí!&#8220; (Extrémní varianta: &#8222;Používám Prometheus!&#8220;) Příliš velké novoty! Dodnes si živě pamatuju svůj odchod z mailové konference o ZX Spectru poté, co jsem se odvážil odpovědět na otázku &#8222;Má někdo v grafickém rozhraní paměti, které se dají najednou číst i zapisovat&#8220; ve smyslu, že některé grafické karty pro PC to používají. Byl jsem vyhozen za &#8222;řeči o PeCi&#8220; &#8211; předpokládám, že ostatní do té konference přispívali z gumáků. (_Jo, tuším že v té konferenci byl i Zil0gator, který si na mně chladil žáhu na Zdrojáku a jehož verbální agresivita vůči &#8222;bloatware&#8220; a &#8222;prznění programátorstva&#8220; mě bavila tak, že jsem si z něj udělal etalon&#8230;_)

Takže jsem to IDE přebudoval tak, aby se co nejvíc tvářilo jako aplikace. Tedy AppCache, ukládání souborů do localStorage atakdál. Šlo to, jen ten assembler byl stále na serveru.

Pak jsem se věnoval jiným věcem, nebyl na to čas, až teď, s pravidelnou pracovní dobou, jsem ho zase nalezl. Takže jsem jednak vylepšil svoje souborové úložiště v prohlížeči, vytvořil jsem si k tomu serverový backend, kam si můžu lokální soubory &#8222;přesypat&#8220;, když chci, no a přepsal jsem hlavně celý assembler do JavaScriptu. Díky oddělení na tři části můžu použít společný základ pro libovolný procesor (parser, dvouprůchodový generátor, preprocesor), a k němu dopsat specifické části pro ten který procesor. Začal jsem s 8080/8085, pak jsem přidal 6502 &#8211; sám jsem byl překvapený, že vytvoření téhle mutace zabralo jen asi čtyři hodiny, z nichž jsem se většinu času snažil sepsat pravidla pro vyhodnocování adresních módů. Ještě mě čeká Z-80, a s tím bude trošku problém, vzhledem k tomu, že některé instrukce, když na to přijde, zaberou až pět bajtů&#8230;

Emulátor 6502 v JS mám, jen co najdu zdrojáky, tak ho budu moci nasadit. Přemýšlel jsem, co s 8080 &#8211; napsat emulační engine v JavaScriptu není problém, to za jedno odpoledne sfouknu, ale napadlo mě, že by se rovnou dalo připsat i něco víc. Co třeba emulátor [BOB-85](http://www.nostalcomp.cz/bob85.php)? Anebo &#8211; co takhle rovnou [emulátor PMD-85](http://pmd85.borik.net/wiki/Emul%C3%A1tor) v JavaScriptu? Das ist výzva!

No a tak jsem chvilku bloumal po osmibitových webech, pročítal jsem si nostalgicky [Nostalcomp](http://www.nostalcomp.cz/), četl si [Martinův osmibitový blog](http://www.8bity.cz/), a tam jsem objevil svůj starý komentář, a u něho [odpověď](http://www.8bity.cz/2012/replika-osobniho-mikropocitace-mistrum/#comment-697), která mě tehdy minula.

> Á propos Martine, právě vaše deset let staré zápisky na blogu o touze postavit si po letech jednodeskáč mě přiměly, abych se svou úchylkou vylezl na světlo a založil Nostalcomp ![:-)](http://www.8bity.cz/wp-includes/images/smilies/icon_smile.gif)  
> Ale to ješně nebyl Martin Malý, ale Arthur Dent ![:-)](http://www.8bity.cz/wp-includes/images/smilies/icon_smile.gif)

Kruh se uzavřel. Udělalo mi to velkou radost. Tak velkou, že jsem si dodal odvahy a o svém assembleru jsem [tweetnul](https://twitter.com/adent/status/367263750623330304). No a na ten tweet se ozval [mborik128](https://twitter.com/mborik128/status/367273168731254784) &#8211; ano, (spolu)autor těch stránek o emulátoru PMD-85! To nemůže být náhoda, teď už to tedy musím dodělat&#8230; Právě jsem se pustil do webového rozhraní s editorem, a pokud bude situace příznivá, tak příští víkend můžu pustit neveřejnou alfaverzi. Chcete někdo ochutnat?