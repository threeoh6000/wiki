---
lang: fr-FR
layout: faq
section: twilightmenu
category: other
title: FAQ et dépannage
long_title: FAQ et dépannage de TWiLight Menu++
description: FAQ et dépannage pour TWiLight Menu++
---

Pour plus de FAQs, veuillez visiter le [fil GBAtemp](https://gbatemp.net/threads/ds-i-3ds-twilight-menu-gui-for-ds-i-games-and-ds-i-menu-replacement.472200/).
{:.alert .alert-info}

#### Pourquoi ma 3DS reste-t-elle bloquée sur des écrans noirs, se plante, s'éteint, etc. lors du lancement de TWiLight Menu++ ?
TWL_FIRM a pu être corrompu d'une manière ou d'une autre. Suivez ce guide pour résoudre le problème : <https://3ds.hacks.guide/troubleshooting#dsi--ds-functionality-is-broken-after-completing-the-guide>

#### Comment puis-je corriger l'obtention un écran blanc lors du démarrage de TWiLight Menu++ ?
- Redémarrez la console
- Si cela ne fonctionne pas, formatez votre carte SD en FAT32 avec une taille de cluster/d'allocation de 32 ko
- Si cela ne fonctionne pas non plus, essayez une autre carte SD

#### Où est le thème Acekard/Wood UI ?
Le thème Acekard (également appelé Wood UI) a été supprimé en raison de son comportement bogué et de la corruption de la carte SD qu'il entraînait. Veuillez attendre un correctif. La progression pour le retour de ce thème peut être trouvée sur [cette demande de tirage](https://github.com/DS-Homebrew/TWiLightMenu/pull/1109).

#### Comment réparer le fait que TWiLight Menu++ redémarre ou donne une erreur Guru Meditation lors du lancement d'un jeu ?
Allez dans les paramètres TWLMenu++ et désactivez `Màj des jeux joués récemment`.

#### Pourquoi est-ce que j'obtiens un écran blanc lorsque j'essaie de charger un jeu DS à partir de la carte SD ?
Consultez [J'ai des problèmes avec ma/mes ROM(s), que dois-je faire ?](../nds-bootstrap/faq?faq=im-having-issues-with-my-roms-what-should-i-do) sur la page de la FAQ de nds-bootstrap.

#### Comment utiliser des codes de triche ?
Vous avez besoin d'une base de données de codes de triche sous la forme d'un fichier `usrcheat.dat` dans le dossier `sd:/_nds/TWiLightMenu/extras/`. La base de données de codes de triche la plus mise à jour est la [base de données de codes de triche NDS(i) de DeadSkullzJr](https://gbatemp.net/threads/488711/).
- Sur la 3DS, cette base de données est disponible dans l'application Universal-Updater sous le nom « NDS(i) Cheat Databases ». Cela l'installera automatiquement à l'emplacement requis.

Vous pouvez également utiliser [r4cce](http://hp.vector.co.jp/authors/VA013928/soft_en.html) pour créer votre propre base de données de codes de triche.

#### Comment afficher une image personnalisée sur l'écran supérieur du thème DSi ?
Une image aléatoire `.png` dans `sd:/_nds/TWiLightMenu/dsimenu/photos/` sera affichée à chaque chargement du menu. S'il n'y a pas d'images applicables, des captures d'écran prises par nds-bootstrap seront utilisées à la place.

- La/les image(s) ne doivent pas dépasser 208 × 156
- Si vous obtenez des erreurs, il s'agit probablement d'une erreur dans la taille de l'image. Veuillez utiliser [tinypng](https://tinypng.com) pour réduire la taille

#### Comment obtenir des jeux ?
Vous pouvez télécharger des jeux homebrews sur [Universal-DB](https://db.universal-team.net/ds) et [GameBrew](https://www.gamebrew.org/wiki/List_of_all_DS_homebrew#Games). Pour obtenir des dumps de vos jeux commerciaux :
- Sur DS, vous pouvez utiliser [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases) pour dumper vos jeux GBA et, si vous avez un linker Slot-2, vos jeux DS. Si vous ne disposez que d'un linker Slot-1 et que vous souhaitez dumper un jeu DS, vous pouvez utiliser [Wooddumper](https://digiex.net/attachments/wooddumper_r89-zip.14735/), qui nécessite une connexion Wi-Fi compatible avec la DS, ainsi qu'un client FTP sur un appareil séparé pour recevoir la ROM
- Sur DSi, vous pouvez utiliser [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases) pour dumper vos jeux DS et DSiWare
- Sur 3DS, vous pouvez utiliser [GodMode9](https://github.com/d0k3/GodMode9/releases) pour vider vos jeux DS, DSiWare et titres de la console virtuelle

#### Puis-je transférer les fichiers de sauvegarde de mes cartes de jeu sur ma carte SD ou vice versa ?
Oui, vous pouvez utiliser [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases) sur DSi et 3DS ou [Checkpoint](https://github.com/FlagBrew/Checkpoint/releases) sur 3DS.

#### Comment changer la langue de TWiLight Menu++ ?
1. Ouvrez les paramètres de TWiLight Menu++, vous pouvez le faire en maintenant <kbd>SELECT</kbd> tout en chargeant TWiLight Menu++
1. Appuyez sur <kbd class="l">L</kbd> ou <kbd class="face">Y</kbd> une fois (sur linker/3DS) ou deux fois (sur DSi)
1. Modifiez la première option jusqu'à ce que la langue souhaitée apparaisse, puis quittez les paramètres
   - Vous pouvez également modifier les deux options suivantes, car elles contrôlent la langue des jeux DS et de leurs titres dans TWiLight Menu++

#### Est-ce un émulateur DS(i) ?
Non, ce n'est pas un émulateur. Le menu et les jeux DS (chargés via nds-bootstrap) sont exécutés nativement dans le mode DS/DSi de la console. Les seules consoles émulées sont les anciennes consoles, mais partiellement pour la GBA (car certaines ou toutes les parties comme les graphiques sont exécutées de manière native).

#### Quels sont les systèmes pris en charge par TWiLight Menu++ ?
Consultez [Liste des systèmes pris en charge par TWiLight Menu++](../ds-index/emulators#list-of-supported-systems-by-twilight-menu).

#### Les exploits des jeux Slot-1 peuvent-ils démarrer TWiLight Menu++ ?
Non. Comme il ne s'agit pas de titres DSiWare, l'accès à la carte SD est désactivé lors de l'utilisation des cartes Slot-1.

#### Pourquoi ne puis-je pas trouver/voir mes jeux ?
Il y a de multiples raisons pour lesquelles vous ne parvenez pas à les trouver.
- Si vous avez placé vos jeux dans le dossier `_nds` , vous ne pouvez pas y accéder car il est invisible en permanence dans TWiLight Menu++. Veuillez les déplacer vers un autre emplacement sur la carte SD
- Si vous avez plus de 39 éléments dans un dossier et que tous les emplacements du menu sont occupés, vos jeux peuvent se trouver sur la page suivante. Utilisez <kbd class="l">L</kbd>/<kbd class="r">R</kbd> ou <kbd>SELECT</kbd> + <kbd>Gauche</kbd>/<kbd>Droite</kbd> pour changer de page
- Si votre jeu ou votre dossier est caché, vous devrez peut-être afficher les fichiers cachés via les paramètres de l'interface graphique de TWiLight Menu++
- Si le type de jeu est configuré pour être caché dans les paramètres d'émulation/HB, il n'apparaîtra pas dans les menus. Modifiez ces paramètres pour qu'ils soient affichés
- Si votre jeu est dans une archive (`zip`, `rar`, `7z`, etc), il ne pourra pas être utilisé par TWiLight Menu++. Extrayez le jeu de l'archive pour l'utiliser
- Si votre jeu n'utilise pas l'une des [extensions supportées](../ds-index/emulators#list-of-systems-supported-by-twilight-menu), vous devrez peut-être modifier l'extension en renommant le fichier

#### Comment accéder aux paramètres de TWiLight Menu++ ?
La manière d'accéder aux paramètres de TWiLight Menu++ varie selon votre configuration.
- **Menu DS Classic :** Appuyez sur l'icône DS en bas de l'écran inférieur
- **Thèmes Nintendo DSi/SEGA Saturn/Homebrew Launcher : en utilisant le menu SELECT :** Appuyez sur <kbd>SELECT</kbd>, puis lancez l'applet des paramètres (utilisez le pad directionnel pour mettre les options en surbrillance)
- **Thèmes Nintendo DSi/SEGA Saturn/Homebrew Launcher : en n'utilisant pas le menu SELECT :** En appuyant sur <kbd>SELECT</kbd> vous arriverez au menu DS Classic
- **Thème Nintendo 3DS :** Appuyez sur l'icône de la clé à molette sur l'écran inférieur
- **Thème R4 Original :** Appuyez sur <kbd>START</kbd> (si vous êtes dans le navigateur de fichier), puis appuyez sur <kbd>SELECT</kbd>

Vous pouvez également maintenir <kbd>SELECT</kbd> tout en lançant TWiLight Menu++ pour accéder directement aux paramètres.
