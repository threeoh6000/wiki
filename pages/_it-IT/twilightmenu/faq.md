---
lang: it-IT
layout: faq
section: twilightmenu
category: other
title: FAQ & Risoluzione dei problemi
long_title: TWiLight Menu++ FAQ & Risoluzione dei problemi
description: FAQ e risoluzione dei problemi per il menu TWiLight ++
---

Per ulteriori FAQ, visita il thread [GBAtemp](https://gbatemp.net/threads/ds-i-3ds-twilight-menu-gui-for-ds-i-games-and-ds-i-menu-replacement.472200/).
{:.alert .alert-info}

#### Why does my 3DS get stuck on black screens, crash, power off, etc when launching TWiLight Menu++?
TWL_FIRM potrebbe in qualche modo essere danneggiato. Segui questa guida per risolvere il problema: <https://3ds.hacks.guide/troubleshooting#dsi--ds-functionality-is-broken-after-completing-the-guide>

#### Come faccio a risolvere il problema di ottenere uno schermo bianco quando avvio TWiLight Menu++?
- Reboot the console
- Se ciò non funziona, formatta la scheda SD in FAT32 con 32 KB cluster/ memoria d'allocazione
- Se anche questo non funziona, prova una scheda SD diversa

#### Dov'è il tema Acekard/Wood IU?
The Acekard (also called Wood UI) theme was removed due to its buggy behavior and causing SD card corruption. Si prega di aspettare che venga corretto. I progressi per il ritorno di questo tema possono essere trovati in [questo PR](https://github.com/DS-Homebrew/TWiLightMenu/pull/1109).

#### Come faccio a risolvere TWiLight Menu++ che si riavvia o mi dà un Guru Meditation Error quando avvio un gioco?
Vai nelle impostazioni di TWLMenu++ e disabilita `Aggiorna la lista giochi recenti`.

#### Why do I get a white screen when trying to load a DS game from SD card?
See [I’m having issues with my ROM(s), what should I do?](../nds-bootstrap/faq?faq=im-having-issues-with-my-roms-what-should-i-do) on the nds-bootstrap FAQ page.

#### Come posso usare i trucchi?
You need to have a cheat DB in the form of a `usrcheat.dat` file in the `sd:/_nds/TWiLightMenu/extras/` folder. The most updated cheat database is [DeadSkullzJr's NDS(i) Cheat Databases](https://gbatemp.net/threads/488711/).
- On the 3DS, this database is available in the Universal-Updater app as "NDS(i) Cheat Databases". This will automatically install it to the required location.

Alternatively, you can use [r4cce](http://hp.vector.co.jp/authors/VA013928/soft_en.html) to create your own cheat DB.

#### Come faccio a mostrare un'immagine personalizzata sullo schermo superiore nel tema DSi?
A random `.png` image in `sd:/_nds/TWiLightMenu/dsimenu/photos/` will be shown each time the menu is loaded. If there are no applicable images, screenshots taken by nds-bootstrap will be used instead.

- The images(s) must be no bigger than 208x156
- If you have errors, it's most likely an error with the image size. Please use [tinypng](https://tinypng.com) to reduce the size

#### Come posso ottenere i giochi?
You can download homebrew games from [Universal-DB](https://db.universal-team.net/ds) and [GameBrew](https://www.gamebrew.org/wiki/List_of_all_DS_homebrew#Games). To get dumps of your retail games:
- On DS you can use [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases) to dump your GBA games and, if you have a Slot-2 flashcart, DS games. If you only have a Slot-1 flashcard and would like to dump a DS game, you can use [Wooddumper](https://digiex.net/attachments/wooddumper_r89-zip.14735/), which requires a Wi-Fi connection compatible with the DS, as well as an FTP client on a separate device to receive the ROM
- On DSi you can use [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases) to dump your DS games and DSiWare
- On 3DS you can use [GodMode9](https://github.com/d0k3/GodMode9/releases) to dump your DS games, DSiWare, and Virtual Console titles

#### Can I get the save files from my Game Cards onto my SD card or vice versa?
Yes, you can use [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases) on DSi and 3DS or [Checkpoint](https://github.com/FlagBrew/Checkpoint/releases) on 3DS.

#### Come faccio a cambiare la lingua di TWiLight Menu+?
1. Apri le impostazioni di TWiLight Menu++ puoi farlo tenendo premuto <kbd>SELECT</kbd> durante il caricamento di TWiLight Menu++
1. Premi <kbd class="l">L</kbd> o <kbd class="face">Y</kbd> una volta (su flashcard/3DS) o due volte (su DSi)
1. Cambia la prima opzione finché non vedi la lingua che vuoi, poi esci dalle impostazioni
   - Potresti anche voler cambiare le due opzioni successive in quanto controllano la lingua dei giochi del DS e i loro titoli in TWiLight Menu++

#### Questo è un emulatore del DS(i)?
No, this is not an emulator. The menu and DS games (loaded via nds-bootstrap) are ran natively in the console's DS/DSi mode. The only consoles emulated are the past consoles, but partially for GBA (as some or all parts like graphics are ran natively).

#### Quali sistemi supporta TWiLight Menu++?
See [List of Systems Supported by TWiLight Menu++](../ds-index/emulators#list-of-supported-systems-by-twilight-menu).

#### Can exploits of Slot-1 games boot TWiLight Menu++?
No. As they're not DSiWare titles, SD access is disabled when running Slot-1 cards.

#### Why can't I find/see my games?
There are a multiple reasons you may be unable to find them.
- If you placed your games in the `_nds` folder, you are unable to access it because it is permanently invisible in TWiLight Menu++. Please move them to any other location on the SD card
- If you have more than 39 items in a folder and all of the slots on the menu are taken, your games may be on the next page. Use <kbd class="l">L</kbd>/<kbd class="r">R</kbd> or <kbd>SELECT</kbd> + <kbd>Left</kbd>/<kbd>Right</kbd> to switch pages
- If your game or folder is hidden, you may need to show hidden files via TWiLight Menu++'s GUI settings
- If the game type is set to be hidden in Emulation/HB settings, it won't appear on menus. Change these settings so that they will be displayed
- If your game is in an archive (`zip`, `rar`, `7z`, etc), it cannot be used by TWiLight Menu++. Extract the game from the archive to use it
- If your game does not use one of the [supported extensions](../ds-index/emulators#list-of-systems-supported-by-twilight-menu), you may have to change the extension by renaming the file

#### How do I access TWiLight Menu++ settings?
The way to access the TWiLight Menu++ settings varies between your configuration.
- **DS Classic Menu:** Tap the DS icon at the bottom of the lower screen
- **Nintendo DSi/SEGA Saturn/Homebrew Launcher themes: using SELECT Menu:** Press <kbd>SELECT</kbd>, then launch the Settings Applet (use the D-PAD to highlight options)
- **Nintendo DSi/SEGA Saturn/Homebrew Launcher themes not using SELECT Menu:** Hitting <kbd>SELECT</kbd> will bring you to the DS Classic Menu
- **Nintendo 3DS theme:** Tap the the wrench icon on the lower screen
- **R4 Original theme:** Hit <kbd>START</kbd> (if you’re in the file browser), then hit <kbd>SELECT</kbd>

You can also hold <kbd>SELECT</kbd> while launching TWiLight Menu++ to directly access the settings.
