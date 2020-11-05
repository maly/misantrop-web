---
id: 2040
title: Virtuální server snadno a rychle
date: 2014-05-25T14:30:01+01:00
author: Martin Malý
layout: revision
guid: http://www.misantrop.info/958-revision-v1/
permalink: /958-revision-v1/
---
Od doby, co jsem si [pořídil vlastní virtuální server](http://www.misantrop.info/virtualmaster-ze-zarodek-cloudu), zjišťuju, jaká to je pěkná hračka. Jestli si ji chcete vyzkoušet taky, můžete &#8211; [Virtualmaster](https://www.virtualmaster.cz/referral/7b00k) (_affiliate odkaz_) nabízí testovací virtuálky (64MB RAM, až 2GB HDD) na 14 dní zdarma. Můžete si jej zkusit, a pokud vám bude vyhovovat, tak si jej prostě převedete na placený tarif. Tato konfigurace vás bude stát necelých 40 Kč měsíčně a na malý web bude určitě stačit. A pokud ne, tak si zvětšíte disk nebo paměť nebo přidáte jádra, podle toho co vás bude pálit.

Jestli si chcete takový malý virtuálek vyzkoušet, nemusíte si jej nastavovat od začátku. Pokud chcete, mám tu pro vás dva předpřipravené kousky, které můžete použít jako takový &#8222;odrazový můstek&#8220;:

[Ubuntu server + Lighttpd + PHP5.3](https://www.virtualmaster.cz/images/detail/220) &#8211; jednoduchý WWW server Lighttpd s PHP5.3.2. Má zapnutý firewall a automatické bezpečnostní aktualizace. Nemusíte nic nastavovat, jen nahrajte soubory pro web do _/var/www_, a jedem!

[PhpSQLiteCMS-CZ](https://www.virtualmaster.cz/images/detail/221) vychází z předchozí šablony, ale navíc je nainstalována SQLite databáze a předpřipravený redakční systém [PhpSQLiteCMS](http://phpsqlitecms.rudice.cz/) v české verzi. Pokud si vytvoříte &#8222;testing server&#8220; z této šablony, máte během dvou minut běžící web s redakčním systémem, ke kterému se připojíte přes http://x.x.x.x/cms (vyplňte svou IP adresu) &#8211; jméno _admin_, heslo _admin_.

Obě šablony se vejdou do testovacího limitu, takže je můžete použít i na výše zmíněný čtrnáctidenní provoz zdarma.

Enjoy.