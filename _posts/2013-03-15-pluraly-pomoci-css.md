---
id: 1170
title: Plurály pomocí CSS
date: 2013-03-15T14:23:56+01:00
author: Martin Malý
layout: post
guid: https://misantrop.info/?p=1170
permalink: /pluraly-pomoci-css/
dsq_thread_id:
  - "1138898891"
mashsb_timestamp:
  - "1554390153"
mashsb_shares:
  - "15"
mashsb_jsonshares:
  - '{"total":15,"error":"","twitter":15,"facebook_shares":0}'
image: /wp-content/uploads/2013/03/css-logo-vector-logo-primary.jpg
categories:
  - Nezařazené
tags:
  - CSS
---
Takový pěkný CSS hack na páteční odpoledne, aneb Jak vyřešit plurály, když máte v ruce jen CSS a HTML?

<!--more-->

Představte si redakční systém, kde máte přístup jen k HTML šablonám a k CSS. Obsah do nich vkládáte pomocí nějakých speciálních značek. A teď chcete vypsat počet komentářů.

S počtem komentářů je ten problém, že v češtině máme dvě množná čísla. Podívejte se sami:

  * 1 komentář
  * 2 komentáře
  * 3 komentáře
  * 4 komentáře
  * 5 komentářů
  * 6 komentářů

&#8230;atakdál. Podle starých pravidel se řídil tvar podle poslední číslice i v případech jako je 21, 22, 23&#8230; (21 komentář, 22 komentáře), ale nová pravidla kodifikují jako přijatelný i tvar &#8222;21 komentářů&#8220;. (Důvod je prostý &#8211; představte si větu &#8222;4721 divák nadšeně aplaudoval&#8220; &#8211; viz [Šílený korektor](https://interval.cz/clanky/hrichy-pro-sileneho-korektora-clovek-versus-psani-cislovek/)).

Takže tedy řešíme stavy 0, 1, 2-4 a 5+ a patřičný tvar.

A teď si představte, že redakční systém umí odlišit situaci, kdy nejsou žádné komentáře (a tu ošetří), no a pro všechno ostatní tu je jedna HTML šablona a v ní je:

<pre>&lt;p&gt;Diskuse obsahuje $CommentNum$ příspěvků&lt;/p&gt;</pre>

Ne, žádné podmínky šablona nenabízí. Takže výsledkem jsou hlášky &#8222;Diskuse obsahuje 3 příspěvků&#8220;, nemluvě o &#8222;Diskuse obsahuje 1 příspěvků&#8220;.

Jak to pořešit? Jedna z možností je využít JavaScript, no a druhá možnost, kterou mi dneska ukázal kolega Honza Drda, využívá CSS. Já takové řešení nenašel, tak ho zveřejňuju s nadějí, že se může někomu hodit (a s Honzovým souhlasem, samozřejmě).

HTML kód je:

<pre>&lt;p&gt;Diskuse obsahuje $CommentNum$ &lt;span class="none ek$CommentNum$"&gt;příspěvek&lt;/span&gt;&lt;span class="none ky$CommentNum$"&gt;příspěvky&lt;/span&gt;&lt;span class="ku$CommentNum$"&gt;příspěvků&lt;/span&gt;&lt;/p&gt;</pre>

a k tomu patří jednoduchá CSS pravidla:

<pre>.none,.ku1,.ku2,.ku3,.ku4 { display: none; } 
.ek1,.ky2,.ky3,.ky4 { display: inline;}</pre>

A to je celé&#8230; _Vyzkoušel jsem v Chrome, funguje, ale je možné, že někde to nepoběží._

**Samozřejmě ideální řešení je využít nástroj na straně serveru, který tohle umí ošetřit (gettext např.) Ale někdy holt není&#8230;**

**Update:** Krásné [řešení](https://jsfiddle.net/VLqJr/1/) navrhl v komentářích David Matějka (s použitím datových atributů a CSS3)

HTML:

<pre>&lt;div&gt;Diskuze obsahuje &lt;span data-count="$CommentNum$" data-plural-1="komentář" data-plural-2="komentáře" data-plural-3="komentářů"&gt;&lt;/span&gt;&lt;/div&gt;</pre>

CSS:

<pre>span[data-count]:before{
 content: attr(data-count) ' ';
}
span:after {
 content: attr(data-plural-3);
}
span[data-count='1']:after {
 content: attr(data-plural-1);
}
span[data-count='2']:after, span[data-count='3']:after, span[data-count='4']:after {
 content: attr(data-plural-2);
}</pre>

**Update 2:** [vylepšení](https://jsfiddle.net/7snZZ/) předchozího tak, že i v případě vypnutých CSS zůstane sémanticky správné sdělení, napsal Martin Keder

HTML:

<pre>&lt;div&gt;Diskuze obsahuje $CommentNum$ &lt;span data-count="$CommentNum$" data-plural-1="komentář" data-plural-2="komentáře"&gt;&lt;span&gt;komentářů&lt;/span&gt;&lt;/span&gt;&lt;/div&gt;</pre>

CSS:

<pre>span[data-count='1']:after
{
 content: attr(data-plural-1);
}
span[data-count='2']:after, 
span[data-count='3']:after, 
span[data-count='4']:after 
{
 content: attr(data-plural-2);
}</pre>

<pre>span[data-count='1'] span, 
span[data-count='2'] span, 
span[data-count='3'] span, 
span[data-count='4'] span
{
 display: none;
}</pre>