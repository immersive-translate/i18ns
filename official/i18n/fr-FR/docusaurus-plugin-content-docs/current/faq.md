---
sidebar_position: 9
---

# FAQ

## Impossible de télécharger depuis l'Apple Store

- 2023.07.28 : L'Apple Store a été rétrogradé en Chine conformément à la politique
- 2023.08.05 : a été relancé en Chine

## Comment désactiver la traduction automatique

- Annuler dans le panneau Popup ou sur la page des paramètres.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="désactiver la traduction automatique" width="250" />

<!-- - Ou changer : via la page des paramètres

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## Pas la permission de traduire la page actuelle

- Page par défaut du navigateur (pas d'adresse dans la barre d'adresse)
- Page de plugin tiers
- Le plugin Google désactive la page du Google Store

## Comment ne pas afficher le texte original ?

Tapez sur l'icône Immersive Translate pour ouvrir le panneau d'expansion, tapez sur [Plus], [Passer en mode Traduction Seule]

## Un point d'exclamation apparaît sur la page

Un point d'exclamation sur la page indique que le service de traduction a rencontré un problème et a renvoyé une erreur, vous pouvez déplacer votre souris sur le point d'exclamation pour voir l'erreur spécifique.

### Erreur 429

Ceci est l'une des erreurs les plus courantes, l'erreur 429 indiquant que la fréquence des requêtes est trop rapide. La traduction de pages web implique un très grand nombre de paragraphes à traduire, bien que nous ayons réalisé une grande optimisation, incluant la fusion de paragraphes, le contrôle de fréquence, etc. Cependant, il arrive parfois que certains services de traduction soient surchargés, renvoyant une erreur de limite de fréquence 429. Dans ce cas, vous pouvez généralement passer temporairement à d'autres services de traduction, ou attendre un moment et réessayer.

Si vous rencontrez une erreur 429 avec un service de Google, il s'agit généralement d'une limitation de trafic imposée par Google à votre nœud, et il est recommandé de changer de nœud.

## Traduction de documents locaux

Si vous avez besoin de traduire des fichiers HTML locaux, des fichiers txt ou des fichiers PDF, vous pouvez cliquer sur l'icône de l'extension Immersive Translate, puis cliquer sur [Plus], cliquer sur [Traduire des fichiers PDF] ou [Traduire des fichiers HTML/txt] pour traduire des fichiers locaux.

Si vous utilisez des navigateurs de type Chrome, tels que (Chrome, Arc, navigateur Edge), il existe une autre méthode, qui consiste à ouvrir la page de gestion des extensions du navigateur `chrome://extensions`, trouver le plug-in [Immersive Translate], [Permettre à l'extension d'accéder aux fichiers locaux], puis directement dans le navigateur pour ouvrir le fichier HTML local ou le fichier PDF local, vous pouvez directement cliquer avec le bouton droit sur [traduction].

## Comment mettre à jour l'extension ?

En général, pour les extensions installées depuis le magasin du navigateur, le navigateur les mettra automatiquement à jour. La situation générale sera mise à jour automatiquement dans un délai d'un jour après la mise à jour de l'extension. Si vous souhaitez immédiatement mettre à jour vers la dernière version, vous pouvez, sur la page [Gestion des extensions] du navigateur, ouvrir le [Mode développeur], puis cliquer sur [Mises à jour] en haut, pour mettre à jour immédiatement vers la dernière version disponible dans le magasin.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Configuration des sous-titres sur Youtube

Vous pouvez cliquer sur les paramètres de sous-titres propres à Youtube, [Options], puis vous pouvez ajuster la taille, la couleur, etc.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Navigateurs pris en charge par Immersive Translate Tampermonkey

Extensions Grease Monkey recommandées pour Chrome, Firefox sur ordinateur :

- [Tamper Monkey](https://www.tampermonkey.net/)

Extension Grease Monkey recommandée pour Safari :

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Si vous utilisez [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) dans Safari, veuillez rechercher le script d'optimisation Immersive Translate pour le télécharger directement depuis le magasin de Stay (optimisé spécifiquement pour Stay) -->

Extensions Grease Monkey recommandées pour Android :

1. Vous pouvez installer l'extension [Tamper Monkey](https://www.tampermonkey.net/) en utilisant [Firefox Dernière Version](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. Vous pouvez également utiliser directement [X Browser](https://www.xbext.com/?ref=immersive-translate), après l'installation, ouvrez directement [Adresse Tampermonkey Immersive Translate](https://download.immersivetranslate.com/immersive-translate.user.js) pour l'installer ! -->

<!-- Extensions Grease Monkey connues non prises en charge :

- Navigateur Android Via
- Navigateur iOS Alook -->

(car ces navigateurs n'implémentent pas l'API Grease Monkey requise)

## Problème d'accès bloqué à l'interface de Google Translate

Veuillez ajouter le nom de domaine `translate.googleapis.com` à la règle de proxy

## Comment mettre à jour les dernières règles

L'extension elle-même se synchronisera régulièrement avec les dernières règles d'adaptation du site officiel lorsque vous l'utilisez, vous pouvez également synchroniser manuellement avec les dernières règles en cliquant sur l'icône de l'Extension de Traduction Immersive du navigateur pour ouvrir une fenêtre pop-up où l'extension détectera automatiquement les dernières règles d'adaptation et se synchronisera avec elles, il en va de même pour Tampermonkeys.

## Comment puis-je sauvegarder mon retour d'information sur la page web si j'ai des problèmes avec la traduction de la page web ?

Vous devez cliquer droit "Enregistrer sous" ou utiliser le raccourci ctrl+s dans la page web, choisir l'option de sauvegarde de fichier unique, et finalement le format de fichier est .mht/.mhtml. Ensuite, envoyez le fichier à support@immersivetranslate.com

<!-- ![sauvegarder mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Erreur de Traduction Nuage de Couleurs

Tapez à côté ? Le message d'erreur pour le numéro "Type de traduction non pris en charge" est affiché. Vous pouvez sélectionner la langue pour être détectée automatiquement au moyen de la langue spécifiée.

## La Lecture WeChat Ne Peut Pas Être Traduite

Elle ne peut pas être traduite car La Lecture WeChat a effectué un traitement spécial sur le contenu pour empêcher l'accès au contenu par des moyens tiers.

## La traduction déclenchée n'est pas effective

D'autres sites traduisent, mais pas un site en particulier.

- Si ce site a moins de visiteurs
  - Paragraphes suggérés à traduire en survolant avec la souris
  - Si vous avez besoin de traduire tout le site, vous pouvez l'adapter via [règles utilisateur](/docs/advanced/#user-rules)
- Si ce site est utilisé par beaucoup de personnes
  - Vous pouvez commencer par survoler avec la souris pour utiliser la traduction
  - Appelez-le dans le groupe et il sera adapté plus tard

## L'amélioration de la boîte de saisie n'est pas effective

- Page d'accueil du navigateur Recherche Google

La boîte de recherche Google doit se trouver dans l'URL de la page web [Google](https://www.google.com/) et ne peut pas être utilisée dans la page d'accueil du navigateur, les espaces de la barre d'adresse vide

## Journal de débogage des retours

- Activer la journalisation de débogage
  Ouvrir le Panneau -> Paramètres -> Paramètres du développeur -> Activer "Imprimer le journal de débogage dans la console".
- Ouvrir la console du site
  Clic droit pour ouvrir la révision -> Passer à la console en haut de la colonne de droite -> Effectuer l'action pour voir les journaux

## Comment désactiver le hoverball

- Masquer sur la page actuelle

Définissez-le sur "Ne jamais traduire ce site".

- Masquer sur toutes les pages

Ouvrez [Page des Paramètres] - [Paramètres de l'Interface] et désactivez [Afficher le Hoverball sur la Page].

## Erreur lors de l'installation du programme d'installation du plugin sur chrome

- valeur invalide pour web_accessible_resource[0]

  Une version de Chromium supérieure à 88 est requise pour prendre en charge manifest_version 3.

## Comment installer le navigateur 360

Seul le navigateur 360 Extreme x est pris en charge, souvenez-vous, c'est avec un x. Si vous avez accès au magasin d'extensions Google, vous pouvez y aller directement et l'installer. Si vous ne pouvez pas y accéder [installez-le manuellement](/docs/installation/#installation-manuelle-pour-suivre-les-dernières-fonctionnalités-de-développement)

## Le navigateur Opera ne fonctionne pas

- Il ne fonctionne pas sur google.com et d'autres pages de recherche, le plugin affiche `Veuillez actualiser la page actuelle avant de commencer la traduction` et l'actualisation de la page invite toujours ce message.

Vous devez trouver "Immersive Translate" dans les paramètres des plugins d'Opera et activer l'option "Autoriser l'accès aux résultats des pages de recherche".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## Sous-titres bilingues sur YouTube en chinois traditionnel non affichés

YouTube propose des sous-titres traduits par machine, et le chinois traditionnel présentera des erreurs de formatage, provoquant l'affichage de tous les sous-titres avec une grande section de sous-titres au début, sur la base de ce scénario, il est recommandé d'activer l'option [Utiliser Immersive Translate pour Traduire les Sous-titres] dans [Paramètres] [Sous-titres Vidéo].

## Plus de questions (voir beaucoup plus)

<details>
<summary>Comment puis-je vider mon cache avec Tampermonkey ?</summary>
<p>
En raison de la limitation de l'API de Tampermonkey, le cache de Immersive Translate Tampermonkey sera sauvegardé dans le cache du site web correspondant, donc si vous souhaitez le vider, vous pouvez ouvrir le panneau des outils de développement du site web correspondant dans votre navigateur puis vider le cache de ce site web.
</p>
</details>

<details>
<summary>La demande d'adresse d'interface personnalisée de Tampermonkey a échoué ?</summary>
<p>
Tampermonkey exige que toutes les demandes provenant du script doivent déclarer des permissions au début du script, par exemple : `@connect api.google.com`, donc si vous avez besoin d'ajouter un nouveau nom de domaine qui n'est pas le défaut, veuillez le déclarer au début du script de Tampermonkey en prenant modèle sur l'autre nom de domaine.
</p>
</details>
