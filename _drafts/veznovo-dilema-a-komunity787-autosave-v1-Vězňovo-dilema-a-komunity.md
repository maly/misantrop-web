---
id: 789
title: Vězňovo dilema a komunity
date: 2017-05-24T15:39:08+01:00
author: Martin Malý
layout: revision
guid: http://www.misantrop.info/787-autosave/
permalink: /787-autosave-v1/
---
## Komunity a vězení

<p style="padding-left: 30px;">
  <em>Zde jsem na jednom místě shromáždil materiál z pěti svých článků, sepsaných v letech 2003 &#8211; 2006. Jde o články Trocha matematiky v mezilidských vztazích <a href="http://blog.maly.cz/index.php?item=132">díl 1</a> a <a href="http://blog.maly.cz/index.php?item=133">díl 2</a>, <a href="http://www.misantrop.info/462257-komunity-a-vezeni.php">Komunity a vězení</a>, <a href="http://www.misantrop.info/462259-utek-z-vezeni.php">Útěk z vězení</a> a <a href="http://www.misantrop.info/462261-vezeni-se-meni.php">Vězení se mění</a>. Články se zabývají hrou &#8222;Iterované vězňovo dilema&#8220;. Popisuju algoritmy v této hře používané, sleduju jejich chování a &#8222;evoluční výhodnost&#8220;, a závěry aplikuju na lidská společenství se zvláštním přihlédnutím k internetovým komunitám. K článkům je k dispozici i simulátor této hry.</em>
</p>

<p style="padding-left: 30px;">
  <em>Články vznikaly v době, kdy vznikaly nejrůznější internetové projekty s přídomkem &#8222;komunitní&#8220; či &#8222;sociální&#8220; a kdy se věřilo, že lidé budou komunitně sdílet, odkazovat, psát, tvořit&#8230;, jen když budou mít prostor. Poměrně rychle se ukázalo, že tomu tak není, a každý pomníček této snahy byl opentlen vzlyky o tom, jak se komunita rozpadla, protože skoro nikdo nedával, mnozí čerpali, jak komunita ani nevznikla, a jak byla komunita rozeštvána útokem zvenčí&#8230;</em>
</p>

<p style="padding-left: 30px;">
  <em>Aktualizace 8.2.2012: Jakub Vrána navázal na tento text a <a href="http://php.vrana.cz/veznovo-dilema.php">představil</a> optimalizované algoritmy, které rozpoznávají typ soupeře a tomu přizpůsobují svou strategii.</em>
</p>

Lze lidské chování nasimulovat hrou? Samozřejmě, v celé jeho komplexnosti asi těžko, ale přesto některé rysy lze nasimulovat poměrně věrně, a to i pomocí jednoduché hry, známé jako Iterované vězňovo dilema.

Nebojte se, žádná vysoká matematika a ezoterické poučky &#8211; jednoduchá hra, jednoduchá pravidla, více si o nich můžete přečíst na stránce [Trocha matematiky v mezilidských vztazích](http://www.misantrop.info/veznovo-dilema-a-komunity/trocha-matematiky-v-mezilidskych-vztazich/). Ve stručnosti zní pravidla takto:

_Představte si, že jste uvězněn spolu s vaším komplicem, jste držen každý zvlášť a jste zvlášť vyslýcháni. Máte možnost vypovídat proti tomu druhému nebo mlčet. Policie na vás skoro nic nemá a pokud se oba svorně rozhodnete mlčet, dostanete oba tak akorát podmínku. Pokud však pomůžete vašeho kolegu usvědčit, půjde on sedět na deset let a vy vyváznete bez trestu. Totéž platí i v opačném případě. A pokud se rozhodnete oba vypovídat proti tomu druhému, půjdete sedět na pět let oba. Jak se rozhodnete?_

Teď si tu hru zjednodušíme. Hrají dva lidi proti sobě a ve stejný okamžik volí &#8222;podrazit&#8220; nebo &#8222;spolupracovat&#8220;. _Pokud oba spolupracují, mají jistý malý zisk. Pokud jeden podrazí, hodně získá, ale ten druhý hodně tratí. Pokud podrazí oba, je jejich zisk mizivý._ Cílem je hrát tak, abyste získali co nejvíc – tedy cíl čistě egoistický.

Pokud dopředu víte, že se hraje jen jedno kolo, je vždy lepší podrazit. Jenže co když se hra opakuje podruhé, potřetí, počtvrté&#8230;? Musíte trošku přemýšlet – víte jak se váš protihráč dosud choval. Budete spolupracovat, když vás už několikrát podrazil? Budete-li se oba navzájem jen podrážet, je váš zisk menší než když budete oba spolupracovat. Váš egoistický cíl zde není v rozporu s cílem &#8222;altruistickým&#8220;.

Jedná se o tzv. **hru s nenulovým součtem**. V takových hrách není zisk jednoho hráče roven ztrátě druhého, ale za jistých okolností mohou oba získat. Takové hry odpovídají realitě mezilidských (mezistátních, mezispolečenských&#8230;) vztahů víc než hry s nulovým součtem, v nichž zisk jednoho je podmíněn ztrátou druhého.

V mé <a href="https://maly.cz/dilema/" target="_blank" rel="noopener noreferrer">simulaci</a> spolu hraje osm hráčů, metodou &#8222;každý s každým&#8220;. Během jedné hry spolu hrají předem neznámý počet kol. V každém kole se hráč rozhodne, s kým z ostatních hráčů bude spolupracovat a koho podrazí. Může spolupracovat se všemi, může všechny podrazit, o tom, jak se zachová ke konkrétnímu hráči rozhoduje jeho algoritmus. Po sehrání předem neznámého počtu kol je vyhodnocen zisk jednotlivých hráčů a hra končí. O konečném výsledku simulace rozhoduje součet zisků z deseti her.

Simulace používá 20 až 30 kol v každé hře, to kvůli srovnání výkonnosti jednotlivých sestav hráčů. Mnohem reálnější by byly hry, které by mohly mít počet kol mezi 1 a 100.

Vy si můžete vybrat jak se bude který hráč chovat. Na výběr máte následující algoritmy:

  1. **Kavka**. To je hipísácký algoritmus, který vždy spolupracuje.
  2. **Podrazák** je algoritmus, který vždy podrazí
  3. **TFT **je algoritmus _TIT-FOR-TAT_, neboli &#8222;Podraz za podraz&#8220;. Začne každou hru spoluprací. V každém dalším kole oplatí soupeři to co udělal soupeř, tedy na podraz soupeře odpoví podrazem, na spolupráci odpoví spoluprací.
  4. **TF2T** je upravený předchozí algoritmus, který odpovídá podrazem až na dva po sobě jdoucí podrazy protihráče.
  5. **Rozmar** je algoritmus, který se mezi spoluprací a podrazem rozhoduje zcela náhodně.

Aby to neměli hráči tak jednoduché, je do celé simulace vnesen rušivý prvek &#8222;náhody&#8220; – s určitou pravděpodobností je vstřícný krok vnímán a vyhodnocen jako podraz&#8230;

Nastavte si tedy &#8222;povahy&#8220; v této malé &#8222;komunitě&#8220; a nechte je hrát. Dvakrát, třikrát, desetkrát&#8230; Co uvidíte?

<a href="https://maly.cz/dilema/index.php?h0=1&h1=1&h2=1&h3=1&h4=1&h5=1&h6=1&h7=1&nahoda=40&hrajese=Hra" target="_blank" rel="noopener noreferrer">Společnost samých kavek</a> je společnost, kde všichni hráči získávají a jediné rozdíly mezi nimi jsou dány prvkem náhody, viz výše. Když se vliv náhody sníží (=lidé si víc věří), poklesnou i rozdíly mezi zisky: <a href="https://maly.cz/dilema/index.php?h0=1&h1=1&h2=1&h3=1&h4=1&h5=1&h6=1&h7=1&nahoda=400&hrajese=Hra" target="_blank" rel="noopener noreferrer">viz</a>. Průměrný zisk člena takovéto společnosti kavek je okolo 8500.

Ve <a href="https://maly.cz/dilema/index.php?h0=2&h1=2&h2=2&h3=2&h4=2&h5=2&h6=2&h7=2&nahoda=400&hrajese=Hra" target="_blank" rel="noopener noreferrer">společnosti samých podrazáků</a> neexistují rozdíly mezi zisky. Všichni mají stejně, náhoda zde nepůsobí. Průměrné zisky však jsou podstatně nižší, okolo 1700.

Když se do společnosti samých dobromyslných kavek dostane jeden podrazák, nemilosrdně je oškube: <a href="https://maly.cz/dilema/index.php?h0=2&h1=1&h2=1&h3=1&h4=1&h5=1&h6=1&h7=1&nahoda=400&hrajese=Hra" target="_blank" rel="noopener noreferrer">viz</a>. Zisky kavek jsou okolo 5000, podrazák však získává zhruba 17000. Průměrný zisk klesne na 6300.

Když do společnosti přijde <a href="http://www.maly.cz/dilema/index.php?h0=2&h1=2&h2=1&h3=1&h4=1&h5=1&h6=1&h7=1&nahoda=400&hrajese=Hra" target="_blank" rel="noopener noreferrer">druhý podrazák</a>, tak průměrný zisk společenství klesne na 4700, zisky kavek poklesnou na hodnoty okolo 1200 a zisky obou podrazáků klesnou na 15000 – což je ale desetkrát víc než jsou zisky nešťastných kavek.

<a href="http://www.maly.cz/dilema/index.php?h0=2&h1=2&h2=2&h3=1&h4=1&h5=1&h6=1&h7=1&nahoda=400&hrajese=Hra" target="_blank" rel="noopener noreferrer">Třetí podrazák</a> sníží opět výkon společenství na průměrnou hodnotu okolo 3100, zisky podrazáků klesnou na 12500, ale kavky jsou zde již ve ztrátě – průměrně -2500 každá.

S rostoucím počtem podrazáků v komunitě klesá pomalu i výkon společenství, klesají i zisky podrazáků a rapidně rostou ztráty &#8222;kavek&#8220;.

Ve společnosti samých podrazáků získává každý, jak jsme si už řekli, okolo 1700. Stačí však přidat jednu kavku a vše je rázem <a href="http://www.maly.cz/dilema/index.php?h0=2&h1=2&h2=2&h3=2&h4=2&h5=2&h6=2&h7=1&nahoda=400&hrajese=Hra" target="_blank" rel="noopener noreferrer">jiné</a>. Výkon společenství paradoxně poklesne (ze 1700 na 1200), kavka ztrácí okolo 17000, ale příjmy všech sedmi podrazáků vzrostou na více než dvojnásobek – na hodnoty okolo 3900.

Pro podrazáka je tedy nejlepší situace taková, když se ocitne sám samojediný ve společnosti nic netušících kavek. Jeho zisky jsou pak obrovské. Pokud ovšem společnost místo kavek tvoří <a href="http://www.maly.cz/dilema/index.php?h0=2&h1=3&h2=3&h3=3&h4=3&h5=3&h6=3&h7=3&nahoda=400&hrajese=Hra" target="_blank" rel="noopener noreferrer">TFT</a> (hrající nemilosrdně podle principu _oko za oko_), rázem se stane podrazák nejméně výkonným a jeho zisky jsou minimální – TFT dokáží vliv podrazáka eliminovat a udržet si své zisky (cca 7000); navíc výkon TFT podrazákovi zdvojnásobí zisky proti stavu, kdy byl ve společnosti sobě rovných&#8230; TFT algoritmy dokáží zůstat &#8222;výdělečné&#8220; i pokud jich je <a href="http://www.maly.cz/dilema/index.php?h0=2&h1=2&h2=2&h3=2&h4=3&h5=3&h6=3&h7=3&nahoda=400&hrajese=Hra" target="_blank" rel="noopener noreferrer">stejně jako podrazáků</a>, dokonce i při poměru 5:3 jsou na tom TFT stále lépe než podrazáci.

Zjišťování toho, co se stane, když TFT nahradíme TF2T algoritmem (to je ten &#8222;poprvé odpustím&#8220;) ve společnosti podrazáků, ve společnosti kavek, jestli je výhodnější být TFT nebo TF2T, jaký vliv má míra náhody na výhodnosti TF2T nebo co udělá s jakým společenstvím člověk, co se prostě přišel jen pobavit (&#8222;rozmar&#8220;) nechám na vás. A vyvození případných závěrů taky.

Já použiju jen to výše popsané, abych odvodil některé závěry, použitelné pro komunitní projekty:

  * Největší zisk přináší _Společenství Krásných A Hodných Lidí, co spolu vždy spolupracují_ – bohužel je samo nestabilní, navíc nereálné.
  * Takové společenství je zlatým dolem pro podrazáky, kteří se na podobných komunitách mohou neskutečně napakovat.
  * V malém počtu mohou podrazáci na kavkách úspěšně parazitovat – všem ostatním sice zisky klesají a výkon celého společenství se rovněž snižuje, oni však mají zisky vysoce převažující průměr.
  * TFT a TF2T postupy se sice neslučují s učením Pravdylásky, ale jsou nejefektivnější – minimalizují riziko rozkladu společenství. Pokud je společenství tvořeno pouze těmito algoritmy a hrozí vysoká míra &#8222;rušení&#8220;, je na tom lépe TF2T, tedy ten &#8222;více altruistický&#8220; algoritmus.
  * Dva TFT algoritmy se vlivem rušení mohou dostat do série vzájemných podrazů, ze které už nevybřednou, TF2T je zase citlivý na přítomnost čistého podrazáka.

## Útěk z vězení

Tato část rozvíjí předchozí a zároveň odpovídá na dotaz &#8222;**Jak by se mělo společenství chovat, aby bylo odolné proti podrazákům?**&#8220; Jako model bude opět použita moje <a href="http://www.maly.cz/dilema/" target="_blank" rel="noopener noreferrer">simulace iterovaného dilematu vězně</a> , který je sice jen prostým modelem, ale možné stavy společenství demonstruje velmi přesně.

Stručně zopakuji základní modely chování:

**Kavka** vždy spolupracuje s ostatními, **podrazák** je vždy podrazí. **TFT** začne spoluprací a na podraz odpovídá v dalším kroku podrazem, na spolupráci spoluprací. **TF2T** je totéž co TFT, ale podrazem odpovídá až na dva po sobě jdoucí podrazy. **Rozmar**, tedy náhodně se rozhodující, pro tuto část nebude použit.

**Pro komunitu je nejvýhodnější, začnou-li její členové vzájemnou spoluprací.** Společenství vždy spolupracujících je nejvýkonnější z hlediska celkového zisku a je odolné proti rušení – krok, omylem vnímaný jako podraz, nevede k rozpadu spolupráce v dalších krocích. Jejich spolupráce je založena na čistě egoistickém principu (_&#8222;maximalizovat zisk&#8220;_), ale vede k altruistickému chování (_&#8222;já vydělám když ty vyděláš&#8220;_). _Zde by bylo vhodné podotknout, že minimálně v Česku je taková úvaha naprosto utopická, tady totiž stále platí &#8222;Když já ne, tak ani ty ne!&#8220;_

Lidé ovšem nejsou mírní beránci a ačkoli je k modelu _&#8222;vždy spolupráce&#8220;_ nabádá křesťanství už téměř dvě tisícovky let, tak to pořád nějak ne a nechce fungovat. Stačí, že je člověk párkrát podražen, zjistí že tratí a že ten, kdo jej podrazil, vydělal. Komunita může snad jen silou své víry dosáhnout toho, že její členové budou stále jen spolupracovat – ale pak se jedná už o sektu. Reálná společenství nemívají tak silnou víru. Pokud společenství roste, bývá motivace nových členů nižší. (Webové komunitní projekty jsou až na výjimky otevřené, platí to tedy pro ně bezezbytku.)

V reálném světě se i silné přesvědčení o vhodnosti spolupráce snadno rozdrolí pod tíhou zjištění, že spolupráce může vést i k velkému prodělku. Na druhé straně člověk, který &#8222;omylem&#8220; podrazil, zjistí, že tak vydělal víc. Zde je přesvědčení v přímém rozporu s logikou věci, tedy maximalizovat svůj zisk.

<p style="padding-left: 30px;">
  Vsuvka: I když je to pro levicové blouznivce a pro sedmnáctileté studenty jistě hrozná představa, je lidské chování dáno především přírodou, která velí: <strong>Zachovat druh</strong>! Tento imperativ znamená &#8222;<em>minimalizovat ztráty</em>&#8220; a &#8222;<em>maximalizovat zisk</em>&#8220; (což <strong>není</strong> <em>totéž jinými slovy</em>). Zároveň má svou roli i Kantův kategorický imperativ, který dokáže sladit egoistické cíle s altruistickým přístupem. V ideálním případě je člověku jasné, že budou-li všichni kavky, tak se jemu vyplatí být podrazák. Jenže taky ví, že stejnou úvahou si projdou všichni, takže budou všichni podrazáci, a jejich zisk bude menší. Pokud tedy stejnou úvahou projdou všichni, tak jim musí být tohle jasné. A protože jsou všichni řízeni egoistickým příkazem &#8222;<em>maximalizovat zisk</em>&#8222;, tak – logicky – musí zvolit spolupráci. <em>Jenže chování lidí není čistě logické.</em>
</p>

Opustili jsme hippie komunitu ve chvíli, kdy někteří začali zjišťovat, že byli podraženi a jiní zjistili, že podrazit se vyplatilo. Ti podražení přemýšlí, zda to mají zapotřebí, a postupem času dochází k algoritmům z rodiny TFT (to ti &#8222;lepší&#8220;), popřípadě k modelu &#8222;podrazák&#8220; (ti horší). _V případě otevřené komunity není potřeba ani ničeho takového, tam přijde podrazák zvenčí, protože si spočítá, že takový zisk mu jinde nekápne._

Komunita se tedy dostane do stavu, kdy je buď paralyzována podrazákem zvenčí, nebo z vlastních řad, což je z jejího hlediska prašť jako uhoď. Pokud bude dále lpět na svém původním přesvědčení, stane se zlatým dolem pro podrazáka a nakonec nejspíš – vyčerpána – zahyne. Chce-li přežít, musí se bránit. Musí porušit své vstřícné a milé přesvědčení a musí oplatit stejným. (_V otevřených internetových komunitách není možno se podrazáka zbavit, vyhodit jej, &#8222;přestat s ním interagovat&#8220;. Je nutno s ním hrát tak, aby se mu jeho podrazácké chování přestalo vyplácet._) Komunita se tedy v rámci zachování začne měnit z komunity kavek na komunitu TFT (stále sleduje, jak si jistě všímáte, egoistický cíl &#8222;_maximalizovat vlastní zisk_&#8222;, a přitom se chová altruisticky).

V mé simulaci je takovým přechodovým stavem např. stav <a href="http://www.maly.cz/dilema/index.php?h0=2&h1=3&h2=3&h3=3&h4=3&h5=1&h6=1&h7=1&nahoda=400&hrajese=Hra" target="_blank" rel="noopener noreferrer">1 podrazák, 3 TFT, 4 kavky</a>. Podrazákovy zisky jsou nejvyšší (přes 10000), naopak kavky tratí (okolo 4800), TFT si udržují stále vysoké zisky (7000). Logický je tedy tlak na kavky, aby se začaly chovat také jako TFT, protože vysoké zisky podrazáka jsou umožněny především přítomností kavek. Přeměna jen dvou kavek na TFT sníží zisk podrazáka pod úroveň zisků TFT, přeměna další kavky na TFT srazí zisky podrazáka na nejnižší úroveň ze všech zúčastněných, jeho chování se mu přestane vyplácet a (opět egoistický cíl, tentokrát podrazákův) společnost opustí nebo své chování změní, což je žádoucí. Zde je zajímavý okamžik – pokud se změní na TFT, tak poslední a jediná kavka má rázem nejvyšší zisky (protože nemůže padnout do pasti vzájemných podrazů jako TFT).

Pokud se ve fázi &#8222;vyhánění podrazáka&#8220; mění kavky na &#8222;měkčí&#8220; TF2T, jsou jejich zisky nižší než kdyby se měnily na &#8222;tvrdé&#8220; TFT a nepodaří se jim snížit podrazákovy zisky na minimum, pokud bude mezi nimi zůstávat alespoň jedna kavka – podrazák získá &#8222;_o kousek víc_&#8220; než kavka, právě kvůli úvodnímu &#8222;kroku spolupráce navíc&#8220;, který má TF2T na rozdíl od TFT. To, že TF2T váhá s odvetou, způsobí, že se podrazákovi jeho strategie vyplatí. Pokud se však naprosto všichni důsledně drží TF2T strategie, dokáží podrazáka vyhnat (_=snížit mu zisky, čímž jej donutí, aby své chování změnil_).

**Společenství TF2T algoritmů je stejně výkonné jako společenství čistých kavek, odolává podrazákům stejně jako TFT algoritmy a není náchylné k řetězu vzájemných podrazů.** Je to snad cesta, jak uchránit komunity před napadením podrazáky?

Ano, byla by, kdyby&#8230;

TF2T společenství potřebuje, aby naprostá většina jeho členů dodržovala tento model. Bez výhrad. Aby všichni věděli, že na druhý podraz se musí (**MUSÍ!**) odpovědět stejně. A v tom je právě problém společenství pravdy a lásky, intelektuálního relativismu a dnešní doby vůbec. Stačí pár lidí (v mé simulaci jeden jediný), kteří na tento model vnitřně nepřistoupí, kteří budou tvrdit, že třeba ostatní jen špatně chápou podrazákovy kroky (vliv rušení), _že je potřeba odpouštět, že je potřeba o věci diskutovat, že ostatní nemají právo na podraz odpovídat podrazem, protože tak sami klesají na úroveň podrazáků&#8230;_

Jejich váhání s odplatou tak paradoxně pomáhá podrazákovi udržovat jeho model chování – stále ještě má dost vysoké zisky, takže se svého modelu chování nemusí vzdát. Nejnižší zisky totiž mají kavky, ty jsou těmi, kdo umožňují podrazákům chovat se dál podrazácky. Společenství se tedy musí, zdánlivě paradoxně, nejprve zbavit &#8222;humanistických&#8220; (spíš _pseudohumanistických_) kavek, aby donutila podrazáka změnit jeho chování.

Z modelu tedy vyplývá, že **nejstabilnější společenství je společenství TF2T algoritmů**, které **je spolupracující, odolné proti rušení a málo lákavé pro podrazáky**. Pokud je takové společenství podrazákem napadeno, odolává a podrazákovi se jeho chování nevyplácí. Což ovšem neplatí v případě, že jsou ve společenství nějaké čisté sluníčkové kavky, protože podrazák na nich může celkem úspěšně parazitovat.

Což podezřele přesně koresponduje s realitou vztahů mezilidských, vztahů mezi státy, vztahů na pracovištích&#8230; Já vím, je to jen matematický model. 🙂

Nyní zkusím navrhnout některé další algoritmy chování.

Nejprve dva algoritmy, které doplňují škálu mezi Kavkou, Rozmarem a Podrazákem. Tyto algoritmy se při svém rozhodování neřídí podle předchozích kroků.

**Špatný** je algoritmus, který se rozhoduje náhodně a ve třech případech ze čtyř podrazí. Jeho protipólem je Dobrý.  
**Dobrý** je algoritmus, který se stejně jako Špatný rozhoduje náhodně, ovšem podrazí jen v jednom případě ze čtyř.

Další algoritmy jsou dvě modifikace algoritmu _Pavlov_. Pavlov se rozhoduje podle předchozí hry. Pokud soupeř spolupracoval, zopakuje svůj postup z předchozího kroku (znovu spolupracuje/podrazí). Pokud soupeř podrazil, Pavlov změní svůj postup (pokud spolupracoval, teď podrazí, pokud podrazil, teď spolupracuje). Pavlova jsem rozdělil na dva modely:

**Velký pes** si je sebejistý, proto začíná spoluprací  
**Malý pes** nejprve zaštěká, protože je nejistý. Malý pes tak začíná podrazem.

Následuje algoritmus modifikující původní TFT algoritmus:

**TFTp** (TFT with pardon) je algoritmus, který umí odpustit, tedy místo podrazu někdy zvolí spolupráci. Tím se snaží vybřednout z pasti vzájemných podrazů, do kterých padají čisté TFT. Otázka je KDY zvolí spolupráci. Ideální mi připadá, když zvolí spolupráci místo podrazu tehdy, udělal-li dva podrazy za sebou a soupeř přitom v prvním kroku začal spoluprací.

### Simulátor



## Vězení se mění&#8230;

V závěrečné části si odpovíme na otázky: Jak se vyvíjí chování společenství, pokud všichni sledují egoistické cíle? Jak se jaké společenství brání zlu? Funguje samočištění? A konečně odpověď na hlavní otázku: **Jak se tedy chovat, pokud chceme být slušní, ale nechceme být za voly?**

Výše jsme si představili další algoritmy, simulovat si je můžete v &#8222;<a href="http://www.maly.cz/dilema/index2.php" target="_blank" rel="noopener noreferrer">Simulátoru 2</a>&#8222;. Tyto algoritmy tvoří naše startovní pole, tak si je ještě jednou představíme, seřazené podle &#8222;míry podrazovosti&#8220;:

  1. **Kavka.** Algoritmus, který nikdy nepodrazí, jedině když dojde k nějakému šumu, tak je jeho krok vnímán jako podraz. (_Beránčí algoritmus_)
  2. **TF2T.** Algoritmus který začíná spoluprací a podrazí jen tehdy, když byl dvakrát za sebou podražen.
  3. **Velký pes.** Algoritmus který začne spoluprací. Pokud v minulé hře oba spolupracovali, spolupracuje dál, pokud byl podražen, podrazí. Pokud v minulé hře podrazil a podraz se mu vyplatil (=soupeř spolupracoval), bude dál podrážet. Pokud podráží oba, nabídne spolupráci. (_Pragmatický algoritmus_)
  4. **TFT.** Algoritmus začne spoluprací a pak opakuje poslední krok soupeře – podrazí za podraz, spolupracuje při spolupráci. (_Čistící algoritmus_)
  5. **Dobrý.** Algoritmus se rozhoduje náhodně. Spolupracuje, ale v jednom případu ze čtyř podrazí.
  6. **Malý pes.** Chová se stejně jako velký pes, ale začíná podrazem.
  7. **Špatný.** Rozhoduje se náhodně, většinou podrazí, v jednom ze čtyř případů spolupracuje.
  8. **Podrazák. **Vždy podrazí.

Tyto algoritmy tedy spolu zápasí podle principů, které jsem popsal výše. Sehrají spolu deset her, prvních devět má 20-30 kol, poslední dorovnává počet kol na 280 (z hlediska pravidel je to jedno, algoritmy nevědí kolik kol která hra má; dorovnání je jen kvůli snazšímu porovnávání her). Po deseti hrách je vyhodnocen zisk jednotlivých hráčů a ten, jehož zisk byl nejnižší, _mutuje_.

**Mutace** probíhá dle jednoduchých pravidel:

  * V polovině případů se algoritmus změní tak, že převezme algoritmus nejúspěšnějšího hráče.
  * V druhé polovině případů se změní o jeden či dva kroky v &#8222;posloupnosti algoritmů&#8220; směrem k algoritmu výherce, tedy &#8222;horším&#8220; či &#8222;lepším&#8220; směrem. Pokud výherce i poražený používají stejný algoritmus, změní se poražený o jeden či dva kroky náhodným směrem. Posun je většinou o jeden krok, v jednom případě ze čtyř o dva.

Mutační algoritmus sleduje tím nejprostším způsobem egoistický cíl, tedy maximalizaci vlastního zisku, a zároveň simuluje jednak naprosté &#8222;bezzásadové&#8220; změny (&#8222;_Kašlu na to, budu to dělat jako ten co vyhrál_&#8222;), ale i povlovné posuny &#8222;o kousek&#8220;, kdy se hráč snaží své chování změnit co nejmíň, aby &#8222;neslevil ze zásad&#8220;, aby &#8222;se nezpronevěřil&#8220; či aby si &#8222;moc nezadal&#8220;.

Aplikací této jednoduché logiky vznikl <a href="http://www.maly.cz/dilema/mutant2.php" target="_blank" rel="noopener noreferrer">dynamický simulátor</a>. Můžete určit složení skupiny a klikáním na tlačítko Hra spouštět další a další generace. Můžete sledovat, jak algoritmy mutují a pomocí listboxů můžete simulovat např. napadení Podrazáky či velké mutace několika jedinců. Můžete také sledovat, jaké jsou zisky jednotlivých algoritmů, kdo kolikrát podrazil, jaké jsou průměrné zisky na 1000 kol, kolikrát jaký algoritmus během 1000 kol podrazí či jaký má který algoritmus z podrazu zisk.

### Dynamický simulátor



Hrál jsem si s ním několik večerů a dospěl jsem k několika zajímavým zjištěním.

Nejprve jsem zkoušel, nakolik je stabilní homogenní prostředí, tedy takové, kdy všichni hráči používají stejný vzorec chování. Nepřekvapilo, že **společenství samých podrazáků je velmi stabilní**. Jakoukoli mutaci směrem k &#8222;dobru&#8220; okamžitě využije a donutí jejího nositele, aby se stal taky podrazákem. Takové společenství dokáže narušit jen několik &#8222;čistících algoritmů&#8220;.

Nepřekvapuje ani to, že **společenství čistých kavek není nikterak stabilní**. Za čas se v takovém společenství vlivem mutace objeví TF2T či Velcí psi, získají převahu a donutí kavky zmutovat.

**TF2T je poměrně stabilní společenství**, ale za čas přemutuje do společenství Velkých psů.

**Skupina Velkých psů je evolučně úspěšná a tvoří druhou velmi stabilní skupinu. **Menší či větší mutace jednoho či dvou členů celkem bez potíží zvládne. Zároveň má mezi všemi algoritmy nejvyšší zisk na krok hry.

**TFT je algoritmus velmi zvláštní tím, že má tendenci mutovat &#8222;k lepšímu&#8220;.** Společenství není v čase stabilní a mutacemi se dopracuje nakonec na společenství Velkých psů. Spolu s TFT mohou dobře koexistovat TF2T. Ale tato koexistence netrvá dlouho a nakonec se drobnými mutacemi rozšíří Velký pes.

**Samí Dobří **mohou zmutovat přes TFT na Velké psy. Pokud ovšem některý zmutuje na Špatného, společenství se po několik generací propadá hlouběji a hlouběji a končí jako samí podrazáci.

**Malí psi jsou rovněž relativně stabilní** a odolní, pokud ovšem mutací nevznikne jeden podrazák. Ten se téměř okamžitě rozšíří a zaplní celé společenství.

**Špatní** během několika málo generací přejdou v samé Podrazáky.

Z hlediska stability jsou tedy dvě stabilní populace – samí Podrazáci nebo samí Velcí psi. Společenství podrazáků je dostatečně známé i z reality, společenství Velkých psů se vyznačuje tím, že jsou &#8222;_v jádru dobří_&#8222;, ale pokud jim projde podraz, budou podrážet dál, dokud to pro ně bude výhodné. Proto jsem Velkého psa nazval též &#8222;_Pragmatickým algoritmem_&#8222;.

Při testování proběhlo několik milionů kol a nakonec vykrystalizovalo pořadí algoritmů podle ziskovosti. Nejziskovější je Velký pes (cca 5000), následován těsně TF2T, pak TFT (oba cca 4500) a s dalším odstupem jsou Kavky (3000). Následuje Malý pes, Podrazák, Dobrý a Špatný. Pořadí podle toho, jak se &#8222;vyplatí&#8220; podraz, vedou kavky (ovšem hypoteticky, protože ty nikdy nepodrazí a takové zisky mohou mít jen díky neúmyslným podrazům, vznikajícím vlivem rušení a šumů). Po kavkách se s velkým náskokem před jinými vyplácí podraz Velkým psům. Pak zhruba stejně přináší podraz TFTa TF2T, s odstupem následuje Malý pes. Za Malým psem jsou Dobří, Podrazáci a nakonec Špatní – těm se podraz vyplatí ještě míň než Podrazákům&#8230; Zajímavý závěr: **Důsledné podrážení se tedy vyplatí víc než podrážení s občasnou snahou o spolupráci.** 🙂

Následně jsem zkoušel odolnost skupin proti &#8222;napadení zlem&#8220; – tedy proti objevení &#8222;špatných&#8220; algoritmů. Zde je už tolik možných kombinací, že popíšu jen několik zajímavostí:

**Skupina kavek napadená podrazákem** zmutuje na TF2T algoritmy, které dokáží nad podrazáky vyhrát. Následuje několik generací TFT/TF2T společenství a vývoj se ustálí na Velkých psech.

**Skupina Velkých psů, napadena** jedním, dvěma či třemi **podrazáky** útok ustojí – zmutuje na TFT algoritmy, které podrazáky vyženou a za čas se vrátí opět na Velké psy. Velcí psi ovšem neustojí útok Malých psů, kteří používají stejný postup jako ti Velcí, ale je na jejich straně výhoda onoho prvního kroku, kdy oni podrazí a Velcí spolupracují. Jsou tedy v takovémto souboji o trochu ziskovější, a to stačí k tomu, aby se rozšířili.

&#8222;Psí&#8220; algoritmy mají tu výhodu, že pokud nevyhrávají, tak často ani neprohrávají. Mohou tak relativně dobře přežít v cizích společenstvích (s výjimkou samých podrazáků či špatných) a využít toho, že mutují ostatní. Jakmile mutacemi vznikne většina Psů, tak se bleskurychle rozšíří po celé skupině.

TFT algoritmy jsem nazval &#8222;čistícími&#8220;. Jediné dokáží odolat útoku Špatných, Dobrých i Podrazáků, zastavit jejich šíření a konsolidovat skupinu. Pokud opravdu důsledně sledují egoistický cíl &#8222;maximálního zisku&#8220;, zmutují nakonec na pragmatické Velké psy, kteří nejsou tak náchylní k &#8222;šumovým&#8220; podrazům. Tím se výkon společenství opět dostane na nejvyšší reálné hodnoty.

Zajímavé je, že TFT nedokáže čistit, vyskytne-li se mezi nimi jedna jediná ortodoxní kavka, která odmítá spolupracovat na společném cíli &#8222;ochrany společenství&#8220;. Taková kavka se totiž stane okamžitě nejméně výnosným členem, ale protože odmítá mutovat, tak společenství nic nenutí k tomu, aby se měnilo. Bohužel takový status quo ale není pro zbytek skupiny výhodný – při kombinaci 6 TFT + 2 Podrazáci si TFT udržují zisky na téměř 7000 a nutí podrazáky zmutovat. Když se objeví ortodoxní kavka, tak toto nucení zeslábne, protože zisky podrazáků vzrostou na dvojnásobek a zisky TFT mírně poklesnou. Ortodoxní kavka tak nejenom brání vyčištění společenství tím, že se odmítá změnit, ale zároveň zvyšuje zisky podrazákům a tím zmenšuje tlak na změnu jejich chování.

Lze tedy říct, že **samočištění funguje tehdy, pokud všichni důsledně sledují egoistický cíl maximalizace zisku**. Sledování tohoto cíle totiž vede ke kooperaci a efektivnímu zničení škodiče. Ortodoxní pacifisté pomáhají paradoxně škůdci přežít a tak svým postojem škodí možná víc. (Paralely jistě najdete sami&#8230; _Nejsme jako oni, že&#8230;_)

Skupina podrazáků odolává jakýmkoli samovolným mutacím. Jediný způsob, jak ji proměnit, je nasadit do ní několik TFT. Ty jsou velmi tvrdé a svou drobnou ztrátu z prvního kroku spolupráce s podrazáckým okolím si dokáží vynahradit spoluprací s ostatními TFT. V simulaci leckdy stačilo vsadit mezi podrazáky dva TFT, které dokázaly přežít a díky mutacím &#8222;na vítěze&#8220; se nakonec pomalu rozšířily a převládly. Vyčistily tak společenství a pomalu se proměnily v efektivnější Velké psy.

Simulátor máte k dispozici, můžete si, pokud vás to baví, simulovat z plna hrdla a sledovat, jak se ty neživé algoritmy chovají docela inteligentně a racionálně&#8230; 🙂

A to i když jsou pravidla velmi prostá a zjednodušená&#8230;

## Závěr

**Závěr **je možná radostnější, než by se z předchozích dílů zdálo:

  1. Existuje vzorec chování, které odpovídá Kantovu imperativu (tedy mohou se tak chovat všichni), a společenství, která se jím řídí, jsou stabilní (nepodléhají příliš drobným mutacím a excesům) a jsou odolná (dokáží se vypořádat s napadením příživnickými algoritmy). Takové společenství zároveň zajišťuje maximální možný dlouhodobý zisk pro všechny své členy.
  2. Důsledné sledování egoistického cíle (maximálního zisku) nakonec často vede k vytvoření stabilního společenství nejefektivnějších algoritmů a k altruistickému výsledku – tedy nejvyššímu reálnému zisku pro všechny.
  3. Absolutní dobro, nenásilí a spolupráce jsou výhodné pouze v nerušených uzavřených společenstvích bez mutací a šumů. V &#8222;reálných&#8220; společenstvích je výhodnější chování pragmatické, zde naopak ortodoxně mírumilovní představují vysoké riziko pro bezpečí a stabilitu společenství v případě napadení.
  4. Zlo nemusí nakonec vždy zvítězit. Může být poraženo. Ovšem nejde to jinak, než být na zlého zlý a na hodného hodný. Nestačí být &#8222;jen hodný&#8220;.