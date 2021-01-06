---
id: 887
title: 'Milý Twittere, nezkracuj, když neumíš&#8230;'
date: 2011-09-06T16:51:00+01:00
author: Martin Malý
layout: post
guid: https://misantrop.info/mily-twittere-nezkracuj-kdyz-neumis/
permalink: /mily-twittere-nezkracuj-kdyz-neumis/
posterous_869f584d59a8506ee6c71421743d2e0f_post_id:
  - "68745351"
posterous_869f584d59a8506ee6c71421743d2e0f_permalink:
  - https://adent.posterous.com/mily-twittere-nezkracuj-kdyz-neumis
mashsb_timestamp:
  - "1546030381"
mashsb_shares:
  - "0"
mashsb_jsonshares:
  - '{"total":0,"error":"","twitter":0,"facebook_shares":0}'
categories:
  - Nezařazené
---
Když jsem před lety představil Jdem jako zkracovací službu, vhodnou pro Twitter, záhy jsem zjistil (a @davidgrudl tuším taky upozornil&#8230;), že má jednu drobnou&#8230; maličký problém! Vše fungovalo skvěle, pokud stál odkaz sám: <https://jdem.cz/q3hx2> Pokud za ním byla tečka, čárka, středník nebo závorka, tak ten znak Twitter započítal do URL:

<p style="padding-left: 30px">
  Koupili jste si už Kindle? (Např. na <a href="https://jdem.cz/q3hx2)">https://jdem.cz/q3hx2)</a>
</p>

No a odkaz rázem zněl &#8222;https://jdem.cz/q3hx2)&#8220; &#8211; a to mi Jdem vyhodilo, že &#8222;neznámá stránka&#8220;. A tak jsem sedl a během dvaceti minut opravil kód Jdem.cz tak, že případný balast za zkráceninou ignoruje.

Dělají to tak snad všechny zkracovače.

Kromě t.co&#8230; závorka, tečka, čárka, cokoli za odkazem t.co se započítá Twitterským parserem do URL, ale samotný zkracovač zařve, že PROBLÉM, že tu adresu nezná. Kdo to zažil, ať udělá čárku (hřebíkem do mezerníku).

Blbé je, že všechny odkazy začal Twitter tímhle zkracovačem prznit jaksi povinně.

**Milý Twittere, když už všichni přes t.co, tak si buď zlepši URL parser, kterým děláš z textu odkazy, nebo si pošteluj t.co, aby se dal odkaz použít i s balastem za zkratkou!**

_Anebo se na to vykašli úplně a nech to jak to bylo &#8211; na uživatelích; pěkně děkuji._