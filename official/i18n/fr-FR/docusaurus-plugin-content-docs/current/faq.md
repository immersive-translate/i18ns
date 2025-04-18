---
sidebar_position: 9
---

# FAQ

## Sécurité

### 1. Application Android, la bulle flottante a disparu

Les anciennes versions des add-ons sont désactivées, désinstallez et installez la dernière version depuis le [site officiel](https://immersivetranslate.com/).

## Installation

### 1. Comment mettre à jour l'extension

En général, les extensions installées dans le magasin de votre navigateur seront mises à jour automatiquement, généralement dans la journée suivant la mise à jour de l'extension. Si vous souhaitez mettre à jour immédiatement vers la dernière version, vous pouvez aller sur la page [Gestion des extensions] de votre navigateur, activer le [Mode développeur], puis cliquer sur [Mettre à jour] en haut pour mettre à jour immédiatement vers la dernière version disponible dans le magasin.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

### 2. Navigateurs supportés par Immersive Translate Tampermonkey

iOS :

- [Tamper Monkey Browser](https://www.tampermonkey.net/)
- Navigateur Safari avec l'extension Tampermonkey installée, extensions compatibles :
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) : Il est recommandé de rechercher directement le script d'optimisation Immersive Translate depuis le magasin de Stay (spécialement optimisé pour Stay).

Android :

- [Firefox Latest Version](https://www.firefox.com.cn/download/#product-android-release) : Après installation, installez l'extension [Tamper Monkey](https://www.tampermonkey.net/).
- [X Browser](https://www.xbext.com/?ref=immersive-translate) : Après installation, ouvrez directement l'[adresse du script Tampermonkey Immersive Translate](https://download.immersivetranslate.com/immersive-translate.user.js) pour l'installer.

Navigateurs connus qui ne supportent pas les extensions Tampermonkey (ces navigateurs n'ont pas implémenté l'API Tampermonkey requise) :

- Android Via Browser
- iOS Alook Browser

### 3. Erreur lors de l'installation du plugin sur Chrome

Erreur `invalid value for web_accessible_resource[0]` : Une version de Chromium supérieure à 88 est requise pour supporter manifest_version 3.

### 4. Comment installer le navigateur 360

Seul le 360 Extreme Browser X est supporté, rappelez-vous qu'il s'agit de la version X. Si vous pouvez accéder au magasin d'extensions Google, vous pouvez l'installer directement depuis là. Si vous ne pouvez pas y accéder, [installez-le manuellement](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features).

### 5. Le navigateur Opera ne fonctionne pas

Il ne fonctionne pas sur google.com et d'autres pages de recherche, le plugin affiche `Veuillez rafraîchir la page actuelle avant de commencer la traduction` et rafraîchir la page montre toujours ce message : Vous devez trouver "Immersive Translate" dans les paramètres du plugin Opera et activer l'option "Autoriser l'accès aux résultats des pages de recherche".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

### 6. Impossible d'activer les extensions sur les appareils iOS

Si vous ne pouvez pas activer les extensions sur votre appareil iOS, suivez ces étapes :

1. Ouvrez l'application [Réglages]
2. Faites défiler vers le bas et appuyez sur [Temps d'écran]
3. Sélectionnez [Restrictions de contenu et de confidentialité]
4. Appuyez sur [Restrictions de contenu]
5. Sélectionnez [Contenu Web] et réglez-le sur [Non restreint]

Si vous n'avez pas besoin des autres fonctionnalités des Restrictions de contenu et de confidentialité, vous pouvez également choisir de simplement désactiver les Restrictions de contenu et de confidentialité :

1. Ouvrez l'application [Réglages]
2. Sélectionnez [Temps d'écran]
3. Désactivez [Restrictions de contenu et de confidentialité]

### 7. La page des paramètres de Safari continue de charger

Réglages Système -> Navigateur Safari -> Avancé -> Données de site web -> Modifier, trouvez immersivetranslate.com et supprimez-le.

### 8. Après l'installation d'iOS18, redirigé vers une page blanche lors de la connexion depuis la page des paramètres

Appuyez longuement sur la bulle flottante et cliquez sur l'avatar pour vous connecter.

### 9. "Fichier inexistant" lors du glissement du fichier crx vers les extensions du navigateur

Vous devez d'abord extraire le fichier zip, puis ne glisser que le fichier CRX.

### 10. Pourquoi le téléchargement du crx installe la version 1.13.5 au lieu de la dernière

Parce que votre moteur Chrome est détecté comme étant en dessous de la version 115, ce qui ne supporte pas certaines fonctionnalités avancées du plugin, il rétrograde donc automatiquement à la version 1.13.5.

## Traduction de base

### 1. Le contenu principal sur des sites comme Youtube, Facebook est traduit, mais certaines barres latérales ne le sont pas, je veux tout traduire

Pour la lisibilité de la page, la traduction immersive traduit par défaut uniquement la zone de contenu principal. Si vous souhaitez traduire toutes les zones :

Ouvrez le panneau de la bulle flottante (appui long sur mobile) -> Cliquez sur plus en bas à droite -> Sélectionnez toutes les zones.

### 2. Bulle flottante non affichée dans les applications sur mobile

- Le plugin Immersive Translate est un plugin de navigateur qui peut **seulement fonctionner dans les navigateurs**, il ne peut pas être utilisé dans d'autres applications, et ne supporte pas la traduction au sein d'autres applications.

- Le plugin fonctionne uniquement dans le navigateur où il est installé et **ne peut pas fonctionner à travers les navigateurs** (par exemple, l'installation dans Safari ne vous permet pas de l'utiliser dans Chrome)

### 3. Cliquer sur YouTube dans le navigateur iOS ouvre directement l'application

Appuyez et maintenez le lien YouTube pour faire apparaître une fenêtre flottante et choisissez d'ouvrir dans une page web.

### 4. Comment désactiver la traduction automatique

- Annulez dans le panneau Popup ou sur la page des paramètres.
- Ou changez via la page des paramètres

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="désactiver la traduction automatique" width="250" />

### 5. Pas de permission pour traduire la page actuelle

- Page par défaut du navigateur (pas d'adresse dans la barre d'adresse)
- Page de plugin tiers
- Plugin Google désactive la page du magasin Google

### 6. Comment ne pas afficher le texte original ?

Appuyez sur l'icône Immersive Translate pour ouvrir le panneau d'expansion, appuyez sur [Plus], [Passer en mode traduction uniquement].

### 7. Un point d'exclamation apparaît sur la page

Un point d'exclamation sur la page indique que le service de traduction a rencontré un problème et a renvoyé une erreur. Vous pouvez déplacer votre souris sur le point d'exclamation pour voir l'erreur spécifique.

#### Exemple : Erreur 429

C'est l'une des erreurs les plus courantes, 429 indiquant que la fréquence des requêtes est trop rapide. La traduction de pages web a un très grand nombre de paragraphes à traduire, bien que nous ayons fait de grandes optimisations, y compris la fusion de paragraphes, le contrôle de la fréquence, etc., mais parfois il y a encore des services de traduction qui sont surchargés, renvoyant une erreur de limite de fréquence 429. Dans ce cas, vous pouvez généralement passer temporairement à d'autres services de traduction, ou attendre un moment et réessayer.

Si vous utilisez le service Google et rencontrez une erreur 429, c'est généralement un cas où Google applique une limite de trafic contre votre nœud, et il est recommandé de changer de nœud.

### 8. Comment changer la source et la langue cible de la traduction

Sur mobile, appuyez longuement sur la bulle flottante ; sur le bureau, déplacez votre souris sur la bulle flottante pour faire apparaître les paramètres, sélectionnez un autre service de traduction/une autre langue cible.

### 9. Problème d'interface Google Translate bloquée

Veuillez ajouter le nom de domaine `translate.googleapis.com` à la règle de proxy.

### 10. L'interdiction d'OpenAI sur les clés API en Chine affecte-t-elle les services AI des membres

Aucun impact, le produit utilise Azure Enterprise OpenAI, qui n'est pas soumis aux restrictions régionales de l'API.

### 11. Erreur de traduction Color Cloud

Cliquer sur le message d'erreur `?` montre "Unsupported trans_type". Vous pouvez sélectionner manuellement pour définir la langue détectée automatiquement sur une langue spécifique.

### 12. La lecture WeChat ne peut pas être traduite

Elle ne peut pas être traduite car WeChat Reading a fait un traitement spécial pour le contenu afin d'empêcher l'accès au contenu par des moyens tiers.

### 13. Certains contenus sur les pages web ne sont pas traduits

En général, c'est parce que l'administrateur du site a défini des zones à ne pas traduire en utilisant `translate="no"` ou `notranslate class`, mais vous pouvez résoudre cela en :

1. Activant la fonction de survol de la souris
2. Utilisant le survol de la souris pour forcer la traduction du contenu du paragraphe dans cette zone

### 14. Le déclenchement de la traduction n'a pas d'effet

Lorsque d'autres sites peuvent être traduits mais qu'un site particulier ne peut pas :

- Si ce site a moins de visiteurs
  - Il est suggéré de traduire les paragraphes en survolant la souris
  - Si vous avez besoin de traduire l'ensemble du site, vous pouvez l'adapter via [les règles utilisateur](/docs/advanced/#user-rules)
- Si ce site est utilisé par beaucoup de gens
  - Vous pouvez commencer par utiliser le survol de la souris pour traduire
  - Signalez-le dans le groupe, et il sera adapté plus tard

### 15. Comment sauvegarder mes retours de page web si j'ai des problèmes avec la traduction de la page web ?

Vous devez faire un clic droit "Enregistrer sous" ou utiliser le raccourci Ctrl+S dans la page web, choisir fichier unique pour l'option de sauvegarde, et enregistrer avec le format de fichier .mht/.mhtml. Ensuite, envoyez le fichier à support@immersivetranslate.com.

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

### 16. Retour de journal de débogage

1. Activer le journal de débogage : Ouvrir le panneau -> Paramètres -> Paramètres développeur -> Activer "Imprimer le journal de débogage dans la console".
2. Ouvrir la console du site : Clic droit pour ouvrir l'inspection -> Passer à la console en haut de la colonne de droite -> Effectuer l'action pour voir les journaux.

### 17. Comment désactiver la bulle flottante

- Masquer sur la page actuelle : Réglez-le sur "Ne jamais traduire ce site"
- Masquer sur toutes les pages : Ouvrez [Page des paramètres] - [Paramètres d'interface] et désactivez [Afficher la bulle flottante sur la page]

### 18. La fonction de traduction par survol de la souris + raccourci ne fonctionne pas

Pour activer la fonction de traduction par survol de la souris plus raccourci, la page doit d'abord avoir le focus. Si vous constatez que la fonction ne se déclenche pas, essayez ces étapes :

1. Cliquez n'importe où sur la page une fois pour vous assurer que la page a le focus.
2. Essayez d'utiliser à nouveau le survol de la souris et le raccourci pour la traduction.
3. Si la fonction de traduction ne répond toujours pas, vérifiez si vos paramètres de raccourci sont corrects.

### 19. Comment mettre à jour les dernières règles

L'extension elle-même synchronisera régulièrement avec les dernières règles d'adaptation du site officiel lorsque vous l'utilisez. Vous pouvez également synchroniser manuellement avec les dernières règles en cliquant sur l'icône de l'extension Immersive Translate dans le navigateur pour ouvrir une fenêtre popup où l'extension détectera automatiquement les dernières règles d'adaptation et les synchronisera. Il en va de même pour les scripts Tampermonkey.

### 20. La traduction échoue / La traduction continue de tourner

1. Vérifiez la raison de l'échec :
   - Si la limite de quota est atteinte, cela signifie que le quota mensuel du membre pour cette source de traduction est épuisé.
   - Si la traduction affiche une erreur réseau, vérifiez d'abord l'état de votre nœud/réseau.

2. Changez de source de traduction : appuyez longuement sur la boule flottante pour sélectionner une autre source de traduction.

### 21. Comment vérifier le quota et l'utilisation de traduction pour les membres Pro

- Les membres Pro bénéficient d'un quota de traduction de base de 20 millions de Tokens par mois, utilisable pour tous les services de traduction. Que ce soit pour tout utiliser avec DeepL (équivalent à 20 millions de caractères), tout avec OpenAI (20 millions de Tokens), ou un mélange de plusieurs services, vous pouvez librement allouer le quota selon vos besoins réels.

  > La tarification d'OpenAI est basée sur les tokens. Pour le texte en anglais, 1 token équivaut à environ 4 caractères ou 0,75 mot. En général, 1000 Tokens correspondent à environ 750 mots anglais ou 400-500 caractères chinois.

- Adresse de demande d'utilisation : [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. Pourquoi la qualité de traduction Google du plugin n'est-elle pas aussi bonne que celle de la page web Google

Parce que le plugin utilise l'API gratuite de Google, qui est une ancienne API que Google ne maintient pas continuellement, tandis que la traduction officielle de la page web de Google est continuellement maintenue. Théoriquement, la qualité n'est pas aussi bonne que celle de la traduction officielle de Google, et récemment, la qualité de traduction de l'API gratuite de Google a considérablement diminué. Nous recommandons de passer à d'autres services de traduction, et nous recherchons activement des solutions alternatives. Discussion connexe : [#2574](https://github.com/immersive-translate/immersive-translate/issues/2547)

### 23. Affichage du mode tactile en mode souris

Dans [Paramètres avancés](https://dash.immersivetranslate.com/#advanced), activez le mode uniquement souris. La version 1.14.9 optimisera cette détection de mode.

## Traduction vidéo

### 1. Style de configuration des sous-titres YouTube

Vous pouvez cliquer sur les paramètres de sous-titres propres à YouTube, [Options], puis vous pouvez ajuster la taille, la couleur, etc.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

### 2. Les sous-titres bilingues YouTube en chinois traditionnel ne s'affichent pas

YouTube propose des sous-titres traduits automatiquement, et le chinois traditionnel aura des erreurs de formatage, provoquant l'apparition de tous les sous-titres avec une grande section de sous-titres au début. Dans ce cas, il est recommandé d'activer l'option [Utiliser Immersive Translate pour traduire les sous-titres] dans [Paramètres] [Sous-titres vidéo].

### 3. Comment activer la traduction des sous-titres pour Bilibili

Lors de la traduction des sous-titres vidéo Bilibili, veuillez suivre ces étapes :

1. Tout d'abord, activez les sous-titres intégrés de Bilibili en cliquant sur le bouton "Sous-titre" en bas à droite du lecteur. Si la vidéo n'a pas de bouton de sous-titre ou de contenu de sous-titre, les sous-titres bilingues ne sont pas pris en charge.
2. Cliquez sur l'icône "Immersive Translate" dans le lecteur pour activer la fonction de sous-titres bilingues.

Remarque lors de l'utilisation :

1. Assurez-vous que les sous-titres intégrés de Bilibili sont activés.
2. Assurez-vous que la langue cible d'Immersive Translate est différente de la langue des sous-titres intégrés de Bilibili pour déclencher la fonction de traduction.

### 4. Traduction des sous-titres Netflix en utilisant le style de sous-titres original

- L'approche actuelle de Netflix utilise une traduction progressive, avec un style de sous-titres auto-hébergé, et ne prend pas en charge les sous-titres manuels.
- L'ancienne approche nécessite d'attendre que tous les sous-titres soient traduits avant de les afficher, mais prend en charge les sous-titres manuels.

Pour revenir à l'ancienne approche, allez dans [[Paramètres développeur](https://dash.immersivetranslate.com/#developer)], trouvez [Modifier les règles utilisateur] et ajoutez la règle suivante :

```json
[
  {
    "id": "netflix",
    "subtitleRule.add": {
      "attachRule": {
        "appendSelector": ""
      }
    }
  }
]
```

## Traduction de fichiers

### 1. Traduction de documents locaux

- Méthode 1 : Allez sur le [site de traduction de fichiers Immersive Translate](https://app.immersivetranslate.com/), ou cliquez sur l'icône de l'extension Immersive Translate et cliquez sur [Traduction de fichiers] pour entrer.

- Méthode 2 : Si vous utilisez des navigateurs de type Chrome, tels que (Chrome, Arc, Edge), il existe une autre méthode : ouvrez la page de gestion des extensions du navigateur `chrome://extensions`, trouvez le plugin [Immersive Translate], [Autoriser l'extension à accéder aux fichiers locaux], puis directement dans le navigateur pour ouvrir le fichier HTML local ou le fichier PDF local, vous pouvez directement faire un clic droit [Traduction].

**Remarque** : Le navigateur Safari a des restrictions strictes sur l'accès des extensions aux fichiers locaux. Les utilisateurs de Safari doivent utiliser directement la Méthode 1 - aller sur le [site de traduction de fichiers Immersive Translate](https://app.immersivetranslate.com/) pour traduire des fichiers locaux.

### 2. La traduction de PDF est lente lorsqu'il y a beaucoup de pages

Il est recommandé de diviser le document en plusieurs parties de moins de 100 pages chacune, de les traduire séparément, puis de les fusionner après traduction.

### 3. Traductions en double ou chevauchantes dans le PDF

Cela est dû à des problèmes de reconnaissance du fichier source. Actuellement, il est recommandé de cliquer manuellement sur cette section et de supprimer les boîtes de texte supplémentaires. Nous continuerons à optimiser cette situation dans les futures mises à jour.

### 4. Existe-t-il un glossaire / une traduction spéciale ou non-traduction pour certains termes

La version 1.16.1+ prend en charge la fonctionnalité [Bibliothèque de terminologie AI](https://dash.immersivetranslate.com/#terms).

La bibliothèque de terminologie AI ne prend pas en charge par défaut la terminologie de traduction automatique de Google/Microsoft.

Méthode pour forcer l'activation :
(ps : la traduction automatique utilise le remplacement de placeholder, la terminologie peut réduire la qualité de la traduction)

Allez dans [[Paramètres développeur](https://dash.immersivetranslate.com/#developer)] -> [Modifier la configuration complète de l'utilisateur]

```
{
  ....
  "enableMachineTranslateTerms":true,
  ...
}
```

### 5. Impossible d'exporter des fichiers Word traduits au format Word

Actuellement, il y a quelques problèmes techniques avec l'exportation de fichiers Word. Il est recommandé de conserver le format existant. Nous travaillons continuellement à l'optimisation.

### 6. Comment ajuster la taille de police minimale dans les PDFs

Cela est dû à la restriction de taille de police minimale du navigateur. Ajustez la police du navigateur au réglage le plus bas. Pour Chrome, par exemple : cliquez sur [Paramètres de taille de police de Chrome](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)

## Traduction de boîte de saisie

### 1. L'amélioration de la boîte de saisie ne prend pas effet

- Navigateurs connus pour ne pas être pris en charge : Voir la section de compatibilité de [Traduction de boîte de saisie](https://immersivetranslate.com/docs/input/)
- Ne peut pas traduire dans la barre d'URL ou la page initiale du navigateur, ne prend en charge que les barres de recherche. Vous pouvez tester sur https://www.bing.com/
- Essayez d'appuyer plus rapidement sur la touche espace

## Paiement

### 1. Puis-je utiliser WeChat Pay

Les paiements WeChat nécessitent de contacter en privé les membres du personnel dans le groupe et de noter "paiement WeChat". Après que le personnel ait fourni le code QR de paiement, effectuez le paiement et fournissez les détails du paiement. Le personnel fournira le code de rachat d'adhésion annuel/mensuel requis, qui peut être échangé sur la [Page de rachat des membres](https://immersivetranslate.com/exchange/)

### 2. Puis-je obtenir une facture

Actuellement, seules les adhésions annuelles peuvent recevoir des factures. Les utilisateurs qui ont déjà payé et qui ont besoin d'une facture doivent contacter en privé les membres du personnel dans le groupe et noter "émission de facture". Les utilisateurs non payés peuvent vérifier : [Informations sur la facture d'adhésion annuelle](https://immersivetranslate.com/bill/)

## Plus de questions (peu courantes)

<details>
<summary>Comment vider mon cache avec Tampermonkeys ?</summary>
<p>
En raison de la limitation de l'API de Tampermonkeys, le cache de Tampermonkeys Immersive Translate sera enregistré dans le cache du site web correspondant, donc si vous souhaitez le vider, vous pouvez ouvrir le panneau des outils de développement du site web correspondant dans votre navigateur, puis vider le cache de ce site web.
</p>
</details>

<details>
<summary>La demande d'adresse d'interface personnalisée de Tampermonkey a échoué ?</summary>
<p>
Tampermonkeys exige que toutes les requêtes du script déclarent des autorisations au début du script, par exemple : `@connect api.google.com`, donc si vous devez ajouter un nouveau nom de domaine qui n'est pas par défaut, veuillez le déclarer au début du script Tampermonkey en vous basant sur l'autre nom de domaine.
</p>
</details>

<details>
<summary>Le plugin du navigateur Edge s'ouvre vide et le navigateur signale une erreur MANIFEST-000001</summary>
<p>
Ouvrez l'application [Quick File Finder (Everything)](https://www.voidtools.com/en-us/downloads/), recherchez `amkbmndfnliijdhojkpoglbnaaahippg` (l'ID de l'extension Immersive) dans le dossier de stockage du navigateur, supprimez-le, puis désinstallez et réinstallez le plugin.
</p>
</details>

<details>
<summary>Comment télécharger des sous-titres bilingues / Les sous-titres bilingues peuvent-ils être téléchargés à partir d'autres sites web ?</summary>
<p>
- Actuellement, le téléchargement de sous-titres est uniquement pris en charge sur le bureau.
- Y compris YouTube, lorsqu'il y a un bouton de téléchargement de sous-titres, le site web actuel prend en charge le téléchargement de sous-titres bilingues.
</p>
</details>