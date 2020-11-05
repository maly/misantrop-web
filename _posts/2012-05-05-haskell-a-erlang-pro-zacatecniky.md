---
id: 853
title: Haskell a Erlang pro začátečníky
date: 2012-05-05T07:42:00+01:00
author: Martin Malý
layout: post
guid: http://www.misantrop.info/haskell-a-erlang-pro-zacatecniky/
permalink: /haskell-a-erlang-pro-zacatecniky/
posterous_869f584d59a8506ee6c71421743d2e0f_post_id:
  - "128751245"
posterous_869f584d59a8506ee6c71421743d2e0f_permalink:
  - http://adent.posterous.com/haskell-a-erlang-pro-zacatecniky
mashsb_timestamp:
  - "1568832582"
mashsb_shares:
  - "0"
mashsb_jsonshares:
  - '{"total":0,"error":"","facebook_shares":0,"twitter":0}'
categories:
  - Nezařazené
---
To v&iacute;te, důchodce&#8230; Dneska se to je&scaron;tě nauč&iacute;m, za deset let těžko.

Na &uacute;vod _vysvětlen&iacute;_: Postavit si ZX80 z diskr&eacute;tn&iacute;ch souč&aacute;stek je pěkn&aacute; v&yacute;zva (a informace k tomu nab&iacute;z&iacute; [Martinův osmibitov&yacute; blog](http://www.8bity.cz/)). Ale když j&aacute; nem&aacute;m moc televiz&iacute;, zato VGA monitorů habakuk, tak na to mus&iacute;m j&iacute;t jinudy.

Idea klasick&eacute; osmibitov&eacute; konzole s modern&iacute;mi souč&aacute;stkami mě l&aacute;k&aacute; už řadu let. Nakonec jsem použil Propeller, což je takov&yacute; &scaron;ikovn&yacute; jednočip, kter&yacute; m&aacute; v sobě osm jader. Jo, osm. Do jednoho si zadr&aacute;tujete zobrazovac&iacute; jednotku, kter&aacute; pos&iacute;l&aacute; ven sign&aacute;l pro VGA, do druh&eacute;ho nějakou repliku SIDa nebo AY-3-8912 nebo něčeho takov&eacute;ho, do třet&iacute;ho třeba CPU z 6502, a je&scaron;tě m&aacute;te pět jad&yacute;rek na vym&yacute;&scaron;len&iacute; veselost&iacute;. Takže do jednoho kl&aacute;vesnici a my&scaron;, do dal&scaron;&iacute;ho joystick a pr&aacute;ci se SD kartou&#8230; V&iacute;te vy, jak&aacute; je to kr&aacute;sn&aacute; pr&aacute;ce? Do toho [důchodu](http://strucny.misantrop.info/nova-petiletka) ide&aacute;ln&iacute;!

Osmij&aacute;drov&yacute; procesor, to člověka l&aacute;k&aacute;, že by si zkusil nějak&eacute; paraleln&iacute; programov&aacute;n&iacute;, pocvičil se v asynchronn&iacute;ch jazyc&iacute;ch&#8230; A pak si ř&iacute;k&aacute;: &#8222;Nojo, to je fajn, a co udělat opravdu velkou desku se spoustou (spousta == 16, prozat&iacute;m) mal&yacute;ch blb&yacute;ch jednočipů, co by dělaly mal&eacute; &uacute;lohy, a v&scaron;ichni dohromady udělaj&iacute; moc?&#8220;

A v tu chv&iacute;li naraz&iacute;te na to, že _ps&aacute;t pro tohle v C&eacute;čku nebo v ASM bude tot&aacute;l brut&aacute;l harakiri_. Takže co jin&eacute;ho? Nab&iacute;z&iacute; se Lua, pro kterou už implementace na jednočipy jsou. Nab&iacute;zej&iacute; se dal&scaron;&iacute; jazyky, kter&eacute; jsou dělan&eacute; pro paraleln&iacute; prostřed&iacute; (Erlang). A když už jsme u toho, co je&scaron;tě zkusit něco interaktivn&iacute;ho ve stylu &#8222;program jako stav syst&eacute;mu&#8220;, a la Smalltalk? Ale ne objektov&eacute;, sp&iacute;&scaron; funkcion&aacute;ln&iacute;&#8230; Haskell?

Na Erlang i Haskell jsem se koukal a oboj&iacute; se mi něč&iacute;m zamlouvalo. Chtělo by to ale tro&scaron;ku systematicky&#8230; Tak jsem se zeptal na Twitteru na nějak&eacute; dobr&eacute; materi&aacute;ly. Zde jsou jejich doporučen&iacute; (v&scaron;em, co doporučili, patř&iacute; d&iacute;ky), můžete se inspirovat:

<span style="font-size: medium;">Haskell:</span>

  * <http://learnyouahaskell.com/> (česky jako <http://naucte-se.haskell.cz/> &#8211; překlad nen&iacute; &uacute;pln&yacute;)
  * Tot&eacute;ž jako e-book: [Learn You a Haskell for Great Good!](http://www.amazon.com/gp/product/B004VB3V0K/ref=as_li_ss_tl?ie=UTF8&tag=dein-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B004VB3V0K)
  * [Real World Haskell](http://www.amazon.com/gp/product/B0026OR2FY/ref=as_li_ss_tl?ie=UTF8&tag=dein-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B0026OR2FY) (e-book, Amazon)
  * [Haskell Hero](http://www.fi.muni.cz/~xnovak34/haskellhero/index.php?page=lessons) (česk&aacute; interaktivn&iacute; online učebnice Haskellu, trp&iacute; bohužel značnou skriptitidou a trochu připom&iacute;n&aacute; styl psan&iacute; př&iacute;ruček v 90. letech, ale obsahem dobr&aacute;; jako velk&eacute; plus hodnot&iacute;m př&iacute;klady!)
  * [A Gentle Introduction to Haskell](http://www.haskell.org/tutorial/)
  * [Haskell: The Craft of Functional Programming](http://www.amazon.com/gp/product/0201882957/ref=as_li_ss_tl?ie=UTF8&tag=dein-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=0201882957) (kniha)
  * [Functional Programming Fundamentals](http://channel9.msdn.com/Shows/Going+Deep/Lecture-Series-Erik-Meijer-Functional-Programming-Fundamentals-Chapter-1) (video)

<span style="font-size: medium;">Erlang:</span>

  * [Learn You some Erlang](http://learnyousomeerlang.com/)
  * [Programming Erlang](http://www.amazon.com/gp/product/193435600X/ref=as_li_ss_tl?ie=UTF8&tag=dein-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=193435600X) (kniha)
  * J&aacute; za sebe je&scaron;tě doporuč&iacute;m [Getting Started with Erlang](http://www.erlang.org/download/getting_started-5.4.pdf) (PDF)

&nbsp;