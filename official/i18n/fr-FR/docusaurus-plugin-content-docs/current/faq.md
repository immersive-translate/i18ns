---
sidebar_position: 9
---

# FAQ

### 1. L'application Android, la bulle flottante a disparu

Les anciennes versions des add-ons sont désactivées, désinstallez et installez la dernière version depuis le [site officiel](https://immersivetranslate.com/).

## Le contenu principal sur des sites comme Youtube, Facebook est traduit, mais certaines barres latérales ne le sont pas, je veux tout traduire

Pour la lisibilité de la page, la traduction immersive traduit par défaut uniquement la zone de contenu principal. Si vous souhaitez tout traduire.

Ouvrez le panneau de la bulle flottante (appui long sur mobile) -> Cliquez sur plus en bas à droite -> Sélectionnez toutes les zones

## La bulle flottante n'est pas affichée dans les applications Youtube (ou autres) sur mobile

Les plugins de navigateur ne peuvent fonctionner que dans les navigateurs et ne peuvent pas être utilisés dans d'autres applications.

- Cliquer sur YouTube dans un navigateur iOS ouvre directement l'application.

  Appuyez longuement sur le lien YouTube pour faire apparaître une fenêtre flottante et choisissez d'ouvrir dans une page web.

## Comment désactiver la traduction automatique

- Annulez dans le panneau Popup ou sur la page des paramètres.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="désactiver la traduction automatique" width="250" />

<!-- - Ou changez : via la page des paramètres

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## Pas de permission pour traduire la page actuelle

- Page par défaut du navigateur (pas d'adresse dans la barre d'adresse)
- Page de plugin tiers
- Le plugin Google désactive la page du Google Store

## Comment ne pas afficher le texte original ?

Appuyez sur l'icône Immersive Translate pour ouvrir le panneau d'expansion, appuyez sur [Plus], [Passer en mode traduction uniquement]

## Un point d'exclamation apparaît sur la page

Un point d'exclamation sur la page indique que le service de traduction a rencontré un problème et a renvoyé une erreur, vous pouvez déplacer votre souris sur le point d'exclamation pour voir l'erreur spécifique.

### Erreur 429

C'est l'une des erreurs les plus courantes, 429 indiquant que la fréquence des requêtes est trop rapide. La traduction de pages web a un très grand nombre de paragraphes à traduire, bien que nous ayons fait de grandes optimisations, y compris la fusion de paragraphes, le contrôle de la fréquence, etc., mais parfois il y a encore des services de traduction surchargés, renvoyant une erreur de limite de fréquence 429, à ce moment-là, vous pouvez généralement passer temporairement à d'autres services de traduction, ou attendre un moment et réessayer.

Si vous rencontrez une erreur 429 avec un service Google, c'est généralement parce que Google applique une limite de trafic à votre nœud, il est recommandé de changer de nœud.

## Traduction de documents locaux

Si vous avez besoin de traduire des fichiers HTML locaux, des fichiers txt ou des fichiers PDF, vous pouvez cliquer sur l'icône d'extension Immersive Translate, puis cliquer sur [Plus], cliquer sur [Traduire des fichiers PDF] ou [Traduire des fichiers HTML/txt] pour traduire des fichiers locaux.

Si vous utilisez des navigateurs de type Chrome, tels que (Chrome, Arc, Edge), il existe une autre méthode, qui consiste à ouvrir la page de gestion des extensions du navigateur `chrome://extensions`, trouver le plugin [Immersive Translate], [Autoriser l'extension à accéder aux fichiers locaux], puis directement dans le navigateur pour ouvrir le fichier HTML local ou le fichier PDF local, vous pouvez directement faire un clic droit [traduction].

**Remarque** : Le navigateur Safari a des restrictions strictes sur l'accès des extensions aux fichiers locaux. Les utilisateurs de Safari doivent utiliser directement la méthode 1 - cliquer sur l'icône d'extension Immersive Translate, puis cliquer sur [Plus], cliquer sur [Traduire des fichiers PDF] ou [Traduire des fichiers HTML/txt] pour traduire des fichiers locaux.

## Comment mettre à jour l'extension ?

En général, les extensions installées dans le magasin de navigateurs seront automatiquement mises à jour, la situation générale sera automatiquement mise à jour dans un délai d'un jour après la mise à jour de l'extension, si vous souhaitez mettre à jour immédiatement vers la dernière version, vous pouvez dans la page [Gestion des extensions] du navigateur, ouvrir le [Mode développeur], puis cliquer en haut sur [Mises à jour], vous pouvez immédiatement mettre à jour vers la dernière version du magasin.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Configuration du style des sous-titres YouTube

Vous pouvez cliquer sur les paramètres de sous-titres propres à YouTube, [Options], puis vous pouvez ajuster la taille, la couleur, etc.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Navigateurs pris en charge par Immersive Translate Tampermonkey

Extensions Grease Monkey recommandées pour Chrome, Firefox sur ordinateur de bureau :

- [Tamper Monkey](https://www.tampermonkey.net/)

Extension Grease Monkey recommandée pour Safari :

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Si vous utilisez [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) dans Safari, veuillez rechercher le script d'optimisation Immersive Translate pour le télécharger directement depuis le magasin de Stay (optimisé spécifiquement pour Stay) -->

Extensions Grease Monkey recommandées pour Android :

1. Vous pouvez installer l'extension [Tamper Monkey](https://www.tampermonkey.net/) en utilisant [Firefox Latest Version](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. Vous pouvez également utiliser directement [X Browser](https://www.xbext.com/?ref=immersive-translate), après l'installation, ouvrez directement [Immersive Translate Tampermonkey Address](https://download.immersivetranslate.com/immersive-translate.user.js) pour l'installer ! -->

<!-- Extensions Grease Monkey non prises en charge connues :

- Android Via Browser
- iOS Alook Browser -->

(comme ces navigateurs n'implémentent pas l'API Grease Monkey requise)

## Problème d'interface Google Translate bloquée

Veuillez ajouter le nom de domaine `translate.googleapis.com` à la règle de proxy

## Comment mettre à jour les dernières règles

L'extension elle-même synchronisera régulièrement les dernières règles d'adaptation du site officiel lorsque vous l'utilisez, vous pouvez également synchroniser manuellement les dernières règles en cliquant sur l'icône d'extension Immersive Translate du navigateur pour ouvrir une fenêtre contextuelle où l'extension détectera automatiquement les dernières règles d'adaptation et les synchronisera, il en va de même pour les Tampermonkeys.

## Comment enregistrer mes retours de page web si j'ai des problèmes avec la traduction de la page web ?

Vous devez faire un clic droit "Enregistrer sous" ou le raccourci ctrl+s dans la page web, choisir un fichier unique pour l'option d'enregistrement, et enfin le format de fichier est .mht/.mhtml. Ensuite, envoyez le fichier à support@immersivetranslate.com

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Erreur de traduction Color Cloud

Appuyez pour vous éloigner ? Le message d'erreur pour le numéro "Unsupported trans_type" est affiché. Vous pouvez sélectionner la langue à détecter automatiquement par le biais de la langue spécifiée.

## La lecture WeChat ne peut pas être traduite

Elle ne peut pas être traduite car la lecture WeChat a fait un traitement spécial pour le contenu afin d'empêcher l'accès au contenu par des moyens tiers.

## Le déclenchement de la traduction n'a pas d'effet

D'autres sites se traduisent, mais un site ne le fait pas.

- Si ce site a moins de visiteurs
  - Paragraphes suggérés à traduire en survolant la souris
  - Si vous avez besoin de traduire l'ensemble du site, vous pouvez l'adapter via [règles utilisateur](/docs/advanced/#user-rules)
- Si ce site est utilisé par beaucoup de gens
  - Vous pouvez commencer par survoler la souris pour traduire l'utilisation
  - Appelez-le dans le groupe et il sera adapté plus tard

## L'amélioration de la boîte de saisie n'a pas d'effet

- Page d'accueil du navigateur Recherche Google

La boîte de recherche Google doit être dans l'URL de la page web [Google](https://www.google.com/) et ne peut pas être utilisée dans la page d'accueil du navigateur, les endroits vides de la barre d'adresse

## Journal de débogage des retours

- Activer la journalisation de débogage
  Ouvrir le panneau -> Paramètres -> Paramètres du développeur -> Activer "Imprimer le journal de débogage dans la console".
- Ouvrir la console du site
  Clic droit pour ouvrir l'examen -> Passer à la console en haut de la colonne de droite -> Effectuer l'action pour voir les journaux

## Comment désactiver la bulle flottante

- Masquer sur la page actuelle

Réglez-le sur "Ne jamais traduire ce site".

- Masquer sur toutes les pages

Ouvrez [Page des paramètres] - [Paramètres de l'interface] et désactivez [Afficher la bulle flottante sur la page].

## Erreur d'installation du programme d'installation du plugin sur Chrome

- valeur invalide pour web_accessible_resource[0]

  La version Chromium supérieure à 88 est requise pour prendre en charge manifest_version 3.

## Comment installer le navigateur 360

Seul le navigateur 360 Extreme x est pris en charge, rappelez-vous qu'il est avec x. Si vous avez accès au magasin d'extensions Google, vous pouvez y aller directement et l'installer. Si vous ne pouvez pas y accéder [installez-le manuellement](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## Le navigateur Opera ne fonctionne pas

- Il ne fonctionne pas sur google.com et d'autres pages de recherche, le plugin affiche `Veuillez actualiser la page actuelle avant de commencer la traduction` et actualiser la page affiche toujours ce message.

Vous devez trouver "Immersive Translate" dans les paramètres du plugin Opera et activer l'option "Autoriser l'accès aux résultats de la page de recherche".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## Les sous-titres bilingues YouTube en chinois traditionnel ne s'affichent pas

YouTube est livré avec des sous-titres traduits automatiquement, et le chinois traditionnel aura des erreurs de formatage, provoquant l'apparition de tous les sous-titres avec une grande section de sous-titres au début, dans ce cas, il est recommandé d'activer l'option [Utiliser Immersive Translate pour traduire les sous-titres] dans [Paramètres] [Sous-titres vidéo].

## Plus de questions (voir beaucoup)

<details>
<summary>Comment effacer mon cache avec Tampermonkeys ?</summary>
<p>
En raison de la limitation de l'API de Tampermonkeys, le cache de Immersive Translate Tampermonkeys sera enregistré dans le cache du site web correspondant, donc si vous souhaitez l'effacer, vous pouvez ouvrir le panneau des outils de développement du site web correspondant dans votre navigateur, puis effacer le cache de ce site web.
</p>
</details>

<details>
<summary>La demande d'adresse de l'interface personnalisée de Tampermonkey a échoué ?</summary>
<p>
Tampermonkey exige que toutes les requêtes du script déclarent les permissions au début du script, par exemple : `@connect api.google.com`. Donc, si vous avez besoin d'ajouter un nouveau nom de domaine qui n'est pas par défaut, veuillez le déclarer au début du script Tampermonkey en vous basant sur l'autre nom de domaine.
</p>
</details>