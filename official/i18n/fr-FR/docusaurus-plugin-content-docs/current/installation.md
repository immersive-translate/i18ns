---
sidebar_position: 1
---

# Installation

<iframe width="560" height="315" src="https://www.youtube.com/embed/SHznc5kQCM4?si=RyZYUcjW560Bc57-" title="Lecteur vidéo YouTube" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Navigateur de bureau

- Navigateur Microsoft Edge : [Edge Store Immersive Translate](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg)
- Google Chrome : [Chrome Store Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh)
- Firefox : [Magasin d'extensions Firefox Immersive Translate](https://addons.mozilla.org/firefox/addon/immersive-translate/)

> Si vous ne pouvez pas accéder au Google Store officiel, vous pouvez télécharger directement le [dernier installateur zip Immersive Translate pour Chrome](https://download.immersivetranslate.com/latest/chrome-immersive-translate.zip), après le téléchargement, veuillez d'abord le décompresser dans un dossier que vous utilisez habituellement, puis tapez : `chrome://extensions` dans la barre d'adresse pour ouvrir la fenêtre de gestion des extensions, puis activez le "Mode développeur", sélectionnez "Charger des extensions non empaquetées", et choisissez le dossier que vous venez de décompresser et de charger. Sélectionnez le dossier que vous venez d'extraire et chargez-le.

## Safari

- [Cliquez ici pour installer depuis l'App Store](https://apps.apple.com/app/immersive-translate/id6447957425) **C'est GRATUIT !!!!**

<div align="center">
<img src="https://s.immersivetranslate.com/static/official-static/assets/immersive-app-store.png" width="150" alt="qrcode app store"/>
</div>

> Instructions : Après la première installation, vous devez activer l'extension Immersive Translate\*\* dans safari -> Gérer les extensions -> **Activer l'extension Immersive Translate** et lui accorder **Toujours autoriser l'accès à tous les sites Web**, si vous avez des questions, vous pouvez regarder le tutoriel vidéo suivant :

### Safari iOS

<video
controls style={{width:"100%", maxWidth:"350px"}}
controls
muted
height="800px"
poster="https://s.immersivetranslate.com/static/official-static/assets/docs/ios_safari_turorial_en.jpeg" src="https://s.immersivetranslate.com/videos/ios_safari_turorial_en.mp4"></video>

### Safari MacOS

<video
controls style={{width:"100%", maxWidth:"500px"}}
controls
muted
poster="https://s.immersivetranslate.com/static/official-static/assets/docs/macOS_safari_en.jpeg" src="https://s.immersivetranslate.com/videos/macOS_safari_tutorial_en.mp4"></video>

## Android

Cliquez pour télécharger le [Navigateur Android Immersive Translate](/android/), vous devez activer [Immersive Translate] manuellement dans [Extensions] après le téléchargement :

Vous pouvez également essayer d'installer Immersive Translate avec d'autres navigateurs Android, tels que ceux qui prennent en charge les extensions Firefox ou les extensions Chrome, comme

- [Firefox Beta ou Nightly](https://www.mozilla.org/firefox/channel/android/)
- [Lemur Browser](https://lemurbrowser.com/app/)
- [Kiwi Browser](https://kiwibrowser.com/)

Une fois installé, recherchez [Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh) directement dans le magasin Chrome pour l'installer.

## Installation via Tampermonkey

Si vous ne pouvez pas installer l'extension officielle pour Immersive Translates de la manière décrite ci-dessus, vous pouvez installer Tampermonkey en suivant ces étapes :

Adresse de Tampermonkey : https://download.immersivetranslate.com/immersive-translate.user.js

Ouvrez [cette adresse](https://download.immersivetranslate.com/immersive-translate.user.js) dans un navigateur ayant l'extension Grease Monkey installée pour l'installer. Voici quelques navigateurs qui supportent Tampermonkey :

**Firefox pour Android**

1. Téléchargez la [Dernière Version de Firefox](https://www.mozilla.org/firefox/browsers/mobile/android/)
2. Trouvez [Tamper Monkey](https://www.tampermonkey.net/) dans les add-ons recommandés de Firefox et installez-le.
3. Installez [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) pour cette extension (ouvrez ce lien dans votre navigateur Firefox pour voir la page d'installation)
4. Après l'installation, ouvrez n'importe quelle page web et l'icône de la fenêtre flottante de l'extension Immersive Translate apparaîtra sur le côté droit.

**Navigateur Apple Safari [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)**

1. Installez le [plugin safari Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887) et accordez-lui la permission "Toujours autoriser l'accès à n'importe quel site web".
2. Installez [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) pour cette extension (ouvrez ce lien dans le navigateur Safari et cliquez sur l'icône de l'extension Userscript pour voir la page d'installation)
3. Après l'installation, ouvrez n'importe quelle page web et rafraîchissez-la, une fenêtre flottante de cette extension apparaîtra sur le côté droit de la page. (Si vous rencontrez des problèmes avec les fenêtres flottantes qui n'apparaissent pas, nous recommandons de rafraîchir la page plus souvent ou de forcer le redémarrage de Safari pour que cela prenne effet)

## Installation manuelle (pour suivre les dernières fonctionnalités de développement)

L'avantage de l'installation manuelle est que vous n'avez pas à attendre que le magasin l'examine et vous pouvez immédiatement expérimenter les fonctionnalités de la dernière version de développement :

1. Téléchargez le paquet zip sur la [page de publication](https://github.com/immersive-translate/immersive-translate/releases/)
2. Extrayez le zip dans un dossier commun, tel que `Documents/chrome-immersive-translate`.
3. Installation

- Installer : (1) Tapez : `chrome://extensions` dans la barre d'adresse pour ouvrir la fenêtre du Gestionnaire d'Extensions ; (2) Ouvrez le "Mode Développeur", sélectionnez "Charger des Extensions Non Empaquetées", et choisissez le dossier que vous venez de dézipper pour le charger.
- Installation sur le navigateur Firefox : (1) Tapez : `about:debugging#/runtime/this-firefox` dans la barre d'adresse pour ouvrir la fenêtre du Gestionnaire d'Extensions ; (2) Chargez temporairement l'add-on et sélectionnez `firefox/manifest.json`.

### Comment mettre à jour une extension installée manuellement ?

Téléchargez le dernier installateur depuis la [page de publication](https://github.com/immersive-translate/immersive-translate/releases/), supprimez le contenu du dossier original, puis copiez le contenu de la dernière archive zip dans le dossier original, et enfin sur la page de gestion des extensions cliquez sur `Recharger`.

> Si vous êtes habitué à la ligne de commande, vous pouvez utiliser `git clone https://github.com/immersive-translate/immersive-translate.git`, puis installer `dist/chrome` et vous pourrez synchroniser avec `git pull` à chaque fois.
