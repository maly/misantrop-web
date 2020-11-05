---
id: 1660
title: Programátorské věci se přesouvají
date: 2013-11-17T15:07:08+01:00
author: Martin Malý
layout: revision
guid: http://www.misantrop.info/1655-revision-v1/
permalink: /1655-revision-v1/
---
K tomu jedno oznámení pro milovníky osmibitů (ano, je to to s tím assemblerem) a jedno zcela nesystémové HEČ!

<!--more-->

S věcma okolo programování se přesunu na [webscript.cz](http://webscript.cz/). Pokud se vám tedy zajídají moje bloggerské historky a chcete číst jen o programování, račte prosím tam. Stejně tak i pokud se vám moje bloggerské historky nezajídají, A NAVÍC si chcete číst o různých xxxScriptech a o tom, jak s nima válčím a co v nich píšu. A přidejte si [RSS Webscriptu do čtečky](http://feeds.feedburner.com/webscriptcz).

Teď jsem přidal na webscript stránku, věnovanou mému [online assembleru ASM80](http://webscript.cz/asm80/) (už jsem tu o tom [několikrát](http://www.misantrop.info/dlouhe-podzimni-vecery/)&#8230;) &#8211; najdete tam popis toho, co to umí a jak to funguje. Ne, assembler se z toho nenaučíte. Jen popisuju, co ten můj (ne)umí a jakou používá syntax. Je to první alfaverze (build 1100, jak se dozvíte dole), takže pravděpodobnost objevení chyby je spíš vysoká. Pokud nějakou objevíte, použijte Uservoice (to je ten otazník vpravo nahoře) a nahlašte mi ji. Díky.

&nbsp;

Uživatelské rozhraní alfaverze je spartánské, je to &#8222;programátor programátorům&#8220;. Alfaverze kromě assemblerů pro procesory 8080, 8085, 6502 a Z80 obsahuje i emulátory 8080 a 6502, takže si můžete své výtvory rovnou vyzkoušet, odkrokovat a tak. Emulátor pro Z80 je ve vývoji, stejně jako emulátory počítačových sestav.

V roadmapě najdete i informace o tom, co se chystá dál. Kromě nového emulačního jádra, virtuálních počítačových sestav a nového procesoru je to hlavně funkce vzdáleného ukládání souborů na serveru a jejich publikování pro ostatní uživatele.

ASM80 vyžaduje moderní prohlížeč (využívá localStorage, využívá některé funkce z ES5 apod.), takže s IE8 a starším se nechytíte. IE9+ by měl být v pořádku.

Celé IDE běží z cloudu (Amazon S3), v tuto chvíli je totiž &#8222;backendless&#8220; a funguje pouze v prohlížeči. Ani gram serverové podpory.

Takže &#8211; milovníci osmibitů, můžete zkusit [online assembler ASM80](http://webscript.cz/asm80/) a budu rád za zpětnou vazbu.

Jo a to slibované HEČ? Tady je: dostanu originál PMI-80! Heč! 🙂