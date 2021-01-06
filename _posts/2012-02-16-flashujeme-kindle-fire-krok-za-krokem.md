---
id: 153
title: Flashujeme Kindle Fire krok za krokem
date: 2012-02-16T16:46:30+01:00
author: Martin Malý
layout: post
guid: https://misantrop.info/?p=153
permalink: /flashujeme-kindle-fire-krok-za-krokem/
dsq_thread_id:
  - "578487020"
mashsb_timestamp:
  - "1574496667"
mashsb_shares:
  - "4"
mashsb_jsonshares:
  - '{"total":4,"error":"","facebook_shares":0,"twitter":4}'
image: /wp-content/uploads/2012/02/20120216_007-990x180.jpg
categories:
  - Nezařazené
tags:
  - Amazon
  - Android
  - CyanogenMod
  - Fire
  - Kindle
  - Kindle Fire
  - tablet
---
Dnes mi přišel [Kindle Fire](https://www.amazon.com/gp/product/B0051VVOB2/ref=as_li_ss_tl?ie=UTF8&tag=dein-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B0051VVOB2) &#8211; androidí tablet od Amazonu. Nemá oslňující výbavu, ale na konzumaci obsahu a brouzdání po internetech je dostatečný. Jeho hlavní výhoda je jasná: je levný, ale na rozdíl od jiných &#8222;levných tabletů&#8220; to není naprostý shit s tragickým dotykovým displejem, podhodnoceným procesorem a zcela fórovým zpracováním&#8230; Kindle je solidní kus elektroniky, u kterého neplatí, že &#8222;levný&#8220; rovná se &#8222;nekvalitní&#8220;.

<!--more-->

Předem jsem věděl, že budu chtít [Fire](https://www.amazon.com/gp/product/B0051VVOB2/ref=as_li_ss_tl?ie=UTF8&tag=dein-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B0051VVOB2) přeflashnout na normální Android. Sice existují způsoby, jak do nepřeflashovaného [nainstalovat aplikace](https://spravodaj.madaj.net/view.php/2012/02-ako-sa-naborit-do-kindle-fire-bez-rootovania), ale z důvodů, které tu nebudu rozvádět (natož se o nich dohadovat) jsem chtěl Androida. Volba padla, přirozeně, na CyanogenMod 7, což je (jestli se nemýlím) zhruba Android 2.3.7. (Pracuje se na CyanogenMod9, což je Android 4, ale jsou s ním zatím ještě [nějaké problémy](https://docs.google.com/spreadsheet/ccc?key=0ArJmKQhhE5AFdGd2U0F3dFlkcno3dmdreFRtWUUtYVE#gid=0).)

<a href="https://misantrop.info/flashujeme-kindle-fire-krok-za-krokem/20120216_009/" rel="attachment wp-att-157"><img class="aligncenter size-medium wp-image-157" title="20120216_009" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_009-500x375.jpg" alt="" width="500" height="375" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_009-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_009-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_009-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_009.jpg 1280w" sizes="(max-width: 500px) 100vw, 500px" /></a>

Fajn. Máte Kindle Fire. Máte USB kabel s MicroB koncovkou. Máte PC s Windows, máte nainstalovaný Android SDK a chcete nainstalovat CM7. Jak?

_Následující postup použijete na vlastní nebezpečí, jasný?! Pokud nevíte, co a proč udělat, nepouštějte se do toho!_

1. Stáhnete a nainstalujete si [Kindle Fire Utility](https://forum.xda-developers.com/showthread.php?t=1399889)  
2. Stáhnete si [TWRP](https://techerrata.com/file/twrp2/twrp-blaze-2.0.0RC0.img), což je aplikace na zálohování a flashování.  
3. TWRP zkopírujete do adresáře ke Kindle Fire Utility &#8211; dáte ji do podadresáře &#8222;recovery&#8220; (vytvořte si!) a přejmenujete jej na recovery.img  
4. Připojíte [Kindle Fire](https://www.amazon.com/gp/product/B0051VVOB2/ref=as_li_ss_tl?ie=UTF8&tag=dein-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B0051VVOB2)  
5. Ovladače, až se Windows zeptají, najdete v podadresáři &#8222;drivers&#8220;.  
6. Spustíte Kindle Fire utility a vyberete možnost 5 (instalaci TWRP)  
7. Stáhnete si [CM7 Wipeall](https://www.mediafire.com/?7afc1173l7yc0qv) (smaže veškerá nastavení a ponechá čistý Kindle Fire)  
8. Stažený CM7 zkopírujete přes USB kabel do Fire (Fire se připojuje jako USB Mass Storage, takže postup stejný jako při kopírování na USB disk)  
9. Po restartu Fire se objeví žlutý trojúhelník. Podržte tlačítko POWER na několik sekund, tím se spustí TWRP  
10. V TWRP nejprve zvolte zálohu (Backup), čistě pro jistotu  
11. V TWRP zvolte Install. Vlevo vidíte adresáře, vpravo bude někde update-cm7-wipeall.zip (pokud jste ho nahráli do kořenového adresáře). Vyberte ho a zvolte FLASH.  
12. Buď se nainstaluje nová ROM, nebo jste si vyrobili cihlu. Doufejme, že se nainstalovala nová ROM.  
13. Restartujte.

Po restartu by měl naběhnout nový krásný modrozelený Android. Vyzkoušejte si ho.

<a href="https://misantrop.info/flashujeme-kindle-fire-krok-za-krokem/20120216_010/" rel="attachment wp-att-156"><img class="aligncenter size-medium wp-image-156" title="20120216_010" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_010-500x375.jpg" alt="" width="500" height="375" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_010-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_010-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_010-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_010.jpg 1280w" sizes="(max-width: 500px) 100vw, 500px" /></a>

TIP: Měl jsem wifi na kanálu 12 a divil se, že se nechce připojit. Musel jsem do Advanced settings a tam nastavit &#8222;regionální nastavení&#8220; &#8211; výchozí je &#8222;11 kanálů&#8220;.

14. Chcete Google Market &#8211; kdo by nechtěl. Stáhněte si [gApps](https://goo-inside.me/gapps/gapps-gb-20110828-signed.zip).  
15. Nakopírujte do Fire přes kabel  
16. Restartujte, podržte POWER (tj. spusťte TWRP, viz bod 9)  
17. Install, vyberte gApps, nainstalujte, restartujete

Pokud se vám stane, že se zacyklíte a bude se vám TWRP spouštět stále a stále, spusťte ADB shell a zadejte příkaz **idme bootmode 4000**

Fajn, teď máte Googlí aplikace. Já chtěl ještě jednu věc, totiž pustit si filmy přímo z externího síťového disku, co mám jako SMB.

1. Z Marketu jsem instaloval <a href="https://market.android.com/details?id=ws.plattner.cifsmanager&hl=en" rel="nofollow" target="_blank">CifsManager</a>, ES Správce souborů a MX Video Player.  
2. Stáhnul jsem si <a href="https://forum.xda-developers.com/showthread.php?t=1396960" rel="nofollow" target="_blank">ovladače pro CIFS</a>  
3. Zkopíroval jsem soubory ze ZIPu do adresáře &#8222;cifs&#8220; přes USB kabel.  
4. V CifsManageru jsem šel do Settings a nastavil následující hodnoty:

  * Load cifs module zaškrtnuto
  * Load via insmod zaškrtnuto
  * Path to cifs.ko na hodnotu &#8222;/sdcard/cifs/slow-work.ko:/sdcard/cifs/cifs.ko&#8220; (bez uvozovek)
  * Výchozí adresář na &#8222;/sdcard/mnt&#8220;

Nastavil jsem připojení externího SMB disku. Ten se objeví ve správci souborů. Proklikám se na film, kliknu na soubor, ES se mě zeptá, v čem chci přehrát, vyberu MX Video Player, a užívám si video. I s titulkama.

<a href="https://misantrop.info/flashujeme-kindle-fire-krok-za-krokem/20120216_012/" rel="attachment wp-att-154"><img class="aligncenter size-medium wp-image-154" title="20120216_012" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_012-500x375.jpg" alt="" width="500" height="375" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_012-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_012-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_012-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_012.jpg 1280w" sizes="(max-width: 500px) 100vw, 500px" /></a>

_(Celá ta legrace i s dovozem a clem přišla na 5.500 Kč. Pokud byste někdo za takovou cenu chtěli [Kindle Fire](https://www.amazon.com/gp/product/B0051VVOB2/ref=as_li_ss_tl?ie=UTF8&tag=dein-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B0051VVOB2) přivézt, ozvěte se mi; i popisovaný flash na CM7 bych vám mohl zařídit.)_

Zdroje:

  * <https://forum.xda-developers.com/showthread.php?t=1390773>
  * <https://liliputing.com/2011/12/kindle-fire-utility-can-now-root-kindle-os-6-2-1-install-custom-recovery-more.html>
  * <https://liliputing.com/2011/12/how-to-install-cyanogenmod-7-on-the-amazon-kindle-fire.html>
  * <https://liliputing.com/2011/12/how-to-install-twrp-2-0-touch-based-recovery-on-the-kindle-fire-backup-restore-flash-custom-firmware.html>
  * <https://blogs.unbolt.net/index.php/brinley/2010/10/13/stream-videos-from-windows-smb-share-to-android-device>

<div id='gallery-153-1' class='gallery gallery-153'>
  <div class='gallery-row gallery-clear'>
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_012.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_012-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_012-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_012-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_012-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_012.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
    
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_011.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_011-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_011-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_011-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_011-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_011.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
    
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_010.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_010-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_010-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_010-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_010-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_010.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
  </div>
  
  <div class='gallery-row gallery-clear'>
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_009.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_009-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_009-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_009-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_009-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_009.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
    
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_008.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_008-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_008-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_008-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_008-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_008.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
    
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_007.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_007-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_007-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_007-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_007-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_007.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
  </div>
  
  <div class='gallery-row gallery-clear'>
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_006.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_006-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_006-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_006-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_006-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_006.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
    
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_005.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_005-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_005-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_005-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_005-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_005.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
    
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_004.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_004-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_004-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_004-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_004-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_004.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
  </div>
  
  <div class='gallery-row gallery-clear'>
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_003.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_003-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_003-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_003-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_003-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_003.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
    
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_002.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_002-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_002-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_002-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_002-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_002.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
    
    <dl class='gallery-item col-3'>
      <dt class='gallery-icon'>
        <a href='https://misantrop.info/wp-content/uploads/2012/02/20120216_001.jpg'><img width="200" height="150" src="https://misantrop.info/wp-content/uploads/2012/02/20120216_001-200x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" srcset="https://misantrop.info/wp-content/uploads/2012/02/20120216_001-200x150.jpg 200w, https://misantrop.info/wp-content/uploads/2012/02/20120216_001-500x375.jpg 500w, https://misantrop.info/wp-content/uploads/2012/02/20120216_001-1024x768.jpg 1024w, https://misantrop.info/wp-content/uploads/2012/02/20120216_001.jpg 1280w" sizes="(max-width: 200px) 100vw, 200px" /></a>
      </dt>
    </dl>
  </div>
</div>

<!-- .gallery -->

 