---
id: 2034
title: Píšeme textovku, díl první
date: 2014-05-25T13:50:04+01:00
author: Martin Malý
layout: revision
guid: http://www.misantrop.info/1082-revision-v1/
permalink: /1082-revision-v1/
---
Pro mladší generaci musím dodat: &#8222;Textovka&#8220; tu neznamená SMS! 🙂

<!--more-->

Už jsem se [přiznal na Oldplayeru](http://www.oldplayer.cz/hrichy-mladi/), že jsem v mládí spáchal pár textovek. Tedy textových her, abych byl přesný.

Vsuvka pro ty, co nevědí: Textová hra je taková hra, kde informace o herním světě není grafická (bludiště, krajina, herní deska), ale textová. V té nejznámější podobě (Adventure) funguje tak, že hráč si přečte popis lokace, toho, co v dané lokaci vidí, a napíše, co chce dělat (někam jít, sebrat nějaký předmět, použít ho&#8230;) Hra na to nějak zareaguje, a zase mu napíše, co se děje. Typ her jak stvořený pro textové terminály.

Textové hry postupem času nabídly i jednoduchou ilustrační grafiku, ikonky předmětů, grafické rozhraní, později možnost ovládání pomocí menu, ale základ je stále textová informace. Později vznikly, a jednu dobu byly velmi populární, grafické adventury, kde textový popis už nebyl, hráč pohyboval postavičkou v animovaném světě a pomocí myši zkoumal prostředí, manipuloval s ním a zadával pokyny. Určitě znáte hry jako Loom, Beneath the Steel Sky, Leisure Suit Larry, různé Police Questy a King&#8217;s Questy&#8230;

Ale zpátky k textovkám. K napsání tohoto článku mě přiměla [diskuse o tvorbě textovek](http://textovky.panprase.cz/index.php?topic=168.0;prev_next=next#new). Docela mě zarazilo, co tam diskutující psali, tak jsem se rozhodl sepsat, jak taková textovka vypadá &#8222;programátorsky&#8220;. Není to obtížné, pojďme na to.  Je úplně jedno, jaký jazyk k tomu použijete, vystačíte si klidně i s BASICem&#8230;

Co potřebujete?

  1. <span style="font-size: 13px;"><strong>Seznam lokací.</strong> Potřebujete mít popis každé &#8222;místnosti&#8220;, který se vypíše, když do ní hráč vstoupí. U každé místnosti je potřeba mít i možné východy. K tomu poznámka: V textovkách se můžete pohybovat buď čtyřmi směry (Sever, Jih, Východ, Západ), šesti (S, J, V, Z, nahoru a dolů), osmi (světové strany + vedlejší světové strany), deseti (dtto + nahoru/dolů) nebo volně (kdy je směr určen popiskem, např. jako v Belegostu &#8211; &#8222;Můžete jít k hoře, do lesa nebo k potoku&#8220;). Místnosti jsou očíslované (doporučuju začít jedničkou) a pro každý směr si uložíte číslo místnosti, kam dotyčný dojde, když daný směr zvolí. Tento postup je mnohem jednodušší než se spoléhat na nějaké pravidelné členění plánku do mřížky apod.</span>
  2. **Seznam předmětů**. Stejně jako u místností &#8211; každý předmět je očíslovaný a u každého je napsaný jeho název a popis. Zároveň je u každého předmětu informace o tom, kde se nachází, tedy buď číslo místnosti, kde ho hráč najde, nebo třeba 255, pokud předmět zatím &#8222;neexistuje&#8220; a teprve ve hře &#8222;vznikne&#8220;.
  3. **Speciální pravidla** &#8211; k nim se ještě dostaneme.

Textovka začne inicializací &#8211; nastavíme si do proměnné, která ukládá informaci o lokaci, číslo výchozí lokace, do pracovní paměti si zkopírujeme výchozí pozice předmětů, mapu přechodů mezi místnostmi, a spustíme hlavní smyčku.

Hlavní smyčka nejprve vypíše informace o lokaci. Tj. vezme informaci z proměnné s pozicí, a vypíše odpovídající popis místnosti. Pak vypíše seznam předmětů, které hráč vidí &#8211; projede všechny pozice předmětů v pracovní paměti, a pokud je shodná s číslem lokace, vypíše jej. Pak vypíše informaci o tom, kam lze jít &#8211; zase k tomu použije informace z mapy přechodů. Pokud je ve hře nějaké specifické pravidlo, jako třeba že při vstupu do místnosti 26 spadne někde most, tak se tato pravidla v tuto chvíli ošetří a kdyžtak se vypíše hráči potřebná informace (&#8222;Bum! Spadnul most!&#8220;)

Teď je řada na hráči, který zadá nějaký příkaz. Ovládání textových her je možné buď klasickým způsobem, kdy hráč píše na klávesnici, co se má dělat, nebo pomocí nějaké volby z přednastaveného menu. Ovládání textem bych nechal na příští díly (je potřeba řešit parsování příkazů), zůstanu u jednoduššího ovládání pomocí menu. Základní příkazy v každé textovce jsou:

  1. <span style="line-height: 13px;"><strong>Pohyb.</strong> Buď pomocí světových stran, nebo pomocí popisných směrů (viz popis lokací). Najdu si číslo nové místnosti, uložím do proměnné s aktuální pozicí, a spustím znovu smyčku.</span>
  2. **Zvedni.** Parametr je název určitého předmětu. Implementačně jednoduché: zkontroluju, zda je předmět opravdu v té lokaci, kde je i hráč, a pokud ano, v pracovní paměti zapíšu k danému předmětu pozici 0. Co je 0, to je &#8222;u hráče&#8220;. Vypíšu &#8222;Sebral jsi X&#8220; a je to. Složitější hra bude mít například &#8222;nezvednutelné předměty&#8220; nebo bude počítat s váhou, ale to na principu nic nemění. Pokud předmět v místnosti není, vypíšu &#8222;X nikde nevidíš&#8220;. Může existovat speciální pravidlo &#8211; pokud hráč sebere předmět X v místnosti Y, stane se to a to&#8230; Takže to ošetřím.
  3. **Polož.** Parametr je název určitého předmětu. Opak předchozího. Hráč musí mít předmět u sebe (tj. v paměti musí být pozice 0). Pokud ano, a nic tomu nebrání, tak zapíšu číslo aktuální lokace &#8211; tím ho přesunu &#8222;do místnosti&#8220;. Zase &#8211; je-li zapotřebí nějaké pravidlo, provedu ho teď.
  4. **Prozkoumej.** Parametr je název určitého předmětu. Předmět musí mít hráč buď u sebe (tj. pozice 0), nebo musí být ve stejné místnosti (tj. aktuální pozice). Jestli ano, vypíšu popis předmětu. U zkoumání jsou speciální pravidla častá &#8211; hráč prozkoumá truhlu, najde pergamen. Zase je projdu a pokud všechno sedí, provedu požadované.
  5. **Použij.** Parametr je název určitého předmětu, u složitějších her dvou předmětů (použij něco na něco). Tady není obecné pravidlo, co se má stát. Hra musí mít nadefinované pro každé možné použití vlastní speciální pravidlo (&#8222;lze použít předmět X v místnosti Y, pokud tam je předmět Z, a pak se stane to a to&#8220;). Pokud pravidlo není, napíšu hráči, že předmět nelze použít.
  6. **Inventář.** Seznam věcí, co má hráč u sebe, je prostý &#8211; projdu si tabulku a vypíšu názvy předmětů, u kterých je pozice 0
  7. **Rozhlédni se.** Nic než skok na začátek smyčky, k výpisu místnosti.
  8. **Speciální příkazy** &#8211; save, load, konec atd. Save uloží pracovní paměť (tj. aktuální pozici, pozice předmětů a přechodovou mapu), load načte tyto proměnné, konec ukončí hru.

Několikrát jsem se odvolal na speciální pravidla. Pro ně nemůžu dát jednoznačný předpis, záleží na tom, jak je hra napsaná. Obecně jde o kombinace podmínek, které musí platit, pokud se má akce provést, a o vlastní akci. V podmínkách se kombinují podle potřeby následující požadavky:

  * <span style="line-height: 13px;">Typ akce &#8211; jestli se má něco stát při příchodu, při zvednutí, položení, použití, prozkoumání&#8230;</span>
  * Hráč musí být v určité lokaci / nesmí být v určité lokaci
  * Hráč u sebe musí / nesmí mít nějaký předmět
  * V téže lokaci musí / nesmí být nějaký předmět
  * &#8230; a další (např. lze využít interní čítače k nějakému odpočítávání apod.)

V případě, že jsou podmínky splněné, tak se stane jedna nebo více následujících akcí:

  * <span style="line-height: 13px;">Zmizí předmět. Do pozice se zapíše 255 (nebo jiné číslo pro &#8222;neexistující pozici&#8220;)</span>
  * Předmět se objeví, tj. do pozice se zapíše 0 nebo aktuální lokace
  * Otevřou / zavřou se dveře &#8211; technicky se to řeší zápisem do mapy přechodů mezi lokacemi.
  * &#8230; a další, například může přijít / odejít nějaká naskriptovaná postava apod.

Když akce proběhne, dostane o tom hráč zase informaci.

Příklad takového speciálního pravidla je třeba broušení sekery v Belegostu. Toto pravidlo by mohlo vypadat třeba takto:

  * <span style="font-size: 13px;">POKUD </span> 
      * <span style="font-size: 13px;">je akce POUŽIJ </span>
      * <span style="font-size: 13px;">a zvolený předmět je BROUSEK</span>
      * <span style="font-size: 13px;">a hráč má u sebe předmět TUPÁ SEKERA</span>
  * <span style="font-size: 13px;">TAK</span> 
      * <span style="font-size: 13px;">předmět TUPÁ SEKERA zmizí</span>
      * <span style="font-size: 13px;">a předmět OSTRÁ SEKERA se přesune do inventáře (pozice=0)</span>
  * <span style="font-size: 13px;">a vypíše se hlášení o nabroušení sekery</span>

Prosté, není-liž pravda?

Ve složitějších hrách budete používat nejrůznější čítače (počty kroků atd.) a k nim budou navázaná nějaká speciální pravidla, například pro časové zámky nebo pro pohyb postav&#8230; Ale výše popsané je kostra každé textové hry a stačí vám k tomu, abyste dokázali vytvořit jednoduchou textovou hru.

V dalším díle, pokud tedy bude zájem, napíšu něco o tvorbě scénáře, rozepíšu se o parsování příkazů, a pokud budete opravdu chtít, tak představím jednoduchý engine na tvorbu vlastních textovek.