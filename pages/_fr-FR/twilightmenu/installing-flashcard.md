---
lang: fr-FR
layout: wiki
section: twilightmenu
category: installing
title: Installation (linker)
long_title: Installation de TWiLight Menu++ (linker)
description: Comment installer TWiLight Menu++ sur un linker Nintendo DS
---

### Installation
1. Téléchargez le dernier [`TwiLightMenu-Flashcard.7z`](https://github.com/DS-Homebrew/TWiLightMenu/releases/latest/download/TWiLightMenu-Flashcard.7z)
1. Extrayez `TWiLightMenu-Flashcard.7z`
1. Copiez le dossier `_nds` à la racine de la carte microSD de votre linker
1. Copiez le fichier `BOOT.NDS` à la racine de la carte microSD de votre linker
1. Copiez le dossier `roms` à la racine de la carte microSD de votre linker
1. Si vous avez déjà des données de sauvegarde, déplacez vos fichiers `.sav`, qui se trouvent dans l'emplacement de vos ROMs DS, vers un nouveau dossier appelé `saves`, qui va également dans l'emplacement de vos ROMs DS
1. ...
   - **Utilisateurs d'une DS Tank/Lite :** Si le démarrage de `BOOT.NDS` provoque un écran blanc figé, insérez un DS Memory Expansion Pak et réessayez
   - **Utilisateurs d'une DSi/3DS :** Exécutez TWLMenu++ sur la carte SD de la console, activez `Accès au SCFG par le Slot-1` et définissez `Slot-1: Mode tactile` sur `Mode DSi`
      - Ceci vous permet d'utiliser la vitesse d'horloge TWL et/ou le boost VRAM pour vos jeux sur linker, ainsi que d'accéder à la carte SD de la console et d'exécuter les jeux optimisés DSi/exclusifs DSi/DSiWare en mode DSi depuis votre linker

### Pour exécuter des jeux en utilisant le logiciel de votre linker

Veuillez noter que tous les linkers ne permettent pas d'exécuter des jeux de cette manière. Si les étapes ci-dessous ne s'appliquent pas à votre linker, vous pouvez sauter cette section.
{:.alert .alert-warning}

1. Extrayez ce qui est dans `Flashcart Loader/(votre linker)` à la racine de la carte microSD
   - Si vous l'avez fait, passez à l'étape 3. Si ce n'est pas le cas, suivez les étapes de la liste de linkers ci-dessous

1. Pour ces linkers :
   - R4i-SDHC (r4i-sdhc.com)
   - r4isdhc.com 2014-2020 cards
   - R4i SDHC Upgrade Revolution
   - R4DSiXL3D
   - R4i Advance
   - R4-IIIi
   - R4 SDHC Revolution
   - R4(i) Pocket
   - R4i Gold (v1.4.1) (3DS)
   - R4xDS
   - DSTT(i)
   - M3 DS Real
   - M3i Zero (modèle non GMP-Z003)
   - DSONE SDHC & DSONEi

   Installez le [YSMenu de RetroGameFan](https://gbatemp.net/threads/retrogamefan-updates-releases.267243/).
      - Assurez-vous d'avoir `YSMenu.nds` (renommé depuis `TTMenu.dat` s'il n'y en a pas) et le dossier `TTMenu` à la racine de la carte microSD du linker
1. Définissez `Utiliser nds-bootstrap` à `Non` pour que le firmware du linker soit utilisé au lieu de nds-bootstrap

### Démarrage automatique de TWiLight Menu++
1. Extrayez le contenu de `Autoboot/(votre linker)` à la racine de la carte microSD du linker
   - Sautez cette étape si vous ne voyez pas votre linker
1. ...
   - **Utilisateurs de DS Phat/Lite :** Allez dans les paramètres du menu principal de la DS, et activez le mode automatique pour que votre linker se lance au démarrage
   - **Utilisateurs d'une DSi/3DS :** Exécutez TWLMenu++ sur la carte SD de la console et activez `Démarrage automatique Slot-1`
