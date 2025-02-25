---
sidebar_position: 6
---

# Journal des modifications

Ce journal des modifications est mis à jour en fonction de l'avancement du développement. La date après la version est la date de fusion du code, et non la date de Release dans les magasins d'applications (le temps de révision varie après la soumission à chaque magasin d'applications, certains prenant jusqu'à une semaine pour la révision). Actuellement, nous avançons deux versions.

La **version Release** est la version stable officielle, disponible sur les principaux magasins d'applications tels que
[Chrome](https://chromewebstore.google.com/detail/bpoadfkcbjbfhfodiogcnhhhpibjhbnh),
[Edge](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg),
[Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate/),
[Apple](https://apps.apple.com/app/id6447957425), etc.

La **version Preview** est publiée plus fréquemment et inclut certaines fonctionnalités expérimentales. Par rapport à la version Release, elle peut contenir plus de bugs. Elle est principalement publiée sur

- [le userscript du site officiel](https://download.immersivetranslate.com/immersive-translate.user.js)
- [version bêta dans le magasin Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate-beta/)
- [Github Release Assets](https://github.com/immersive-translate/immersive-translate/releases)

## 1.14.16 Preview (2025-02-21)

- Ajouté : Deepseek, Gemini, Cluade supportent le changement de contexte.
- Corrigé : Mise à jour des termes ne déclenche pas de nouvelle demande de traduction.
- Amélioré : Langue de l'interface ajoutée en hongrois.
- Amélioré : Qualité de la traduction Google.
- Amélioré : Formatage d'image gratuit.

## 1.14.12 Release (2025-02-19)

- Amélioré : La pause de la traduction vide immédiatement la file d'attente des demandes.
- Amélioré : Filtre le texte indésirable dans le service de traduction deepl.
- Corrigé : Traduction de la barre latérale invalide dans les paramètres avancés.
- Corrigé : Problème d'affichage de la traduction personnalisée deepseek.

## 1.14.11 Release (2025-02-18)

- Corrigé : Erreur `401: Authentication Fails` de la clé API personnalisée DeepSeek.

## 1.14.10 Release (2025-02-17)

- Nouveau : L'adhésion Pro prend en charge le service de traduction DeepSeek (v3).
- Corrigé : Résolution du problème de dépassement de la taille limite du fichier de configuration utilisateur.
- Amélioré : L'élément du menu contextuel peut être fermé (opéré dans les paramètres avancés).
- Amélioré : Amélioration des capacités de reconnaissance linguistique pour Greasemonkey et Safari sur les pages avec des langues mineures.
- Amélioré : Accès à l'interface de test de la page des paramètres en ligne.
- Amélioré : Amélioration de l'expérience utilisateur de la fonctionnalité d'aperçu de comparaison de contexte.
- Amélioré : Logique de jugement du mode tactile et souris.

## 1.14.8 Release (2025-02-10)

- Corrigé : Problème où les longs fichiers PDF-Pro n'étaient pas traduits automatiquement.
- Amélioré : Microsoft, Google et Tencent prennent désormais en charge le cantonais.
- Amélioré : BBC prend désormais en charge les sous-titres.

## 1.14.6 Preview (2025-02-08)

- Corrigé : Problème où la **Traduction au survol de la souris** ne pouvait pas traduire le texte enrichi.
- Amélioré : La version Tampermonkey prend désormais en charge la traduction des sous-titres YouTube.

## 1.14.4 Release (2025-02-07)

- Corrigé : Problème de détection incorrecte de la langue dans la **Boîte de saisie améliorée**.
- Corrigé : Problème de correspondance intelligente des experts en IA dans les services de traduction personnalisés.
- Corrigé : Problème d'échec de synchronisation Google Drive sur certains navigateurs.
- Corrigé : Problème de traduction des commentaires en direct sur YouTube.
- Corrigé : Problème de superposition des sous-titres dans certaines vidéos YouTube.
- Amélioré : Échec de la traduction de mangas sur des sites comme shonenjumpplus dans le navigateur Safari.

## 1.13.8 Release (2025-01-24)

- Nouveau : La traduction d'image gratuite est désormais disponible (actuellement prise en charge uniquement sur les versions PC des navigateurs Chrome et Edge), accessible via le menu contextuel.
- Corrigé : Problème où certains contenus étaient manqués lors de la traduction multi-segments dans Gemini.
- Optimisé : Amélioration du chargement des sous-titres YouTube.
- Nouveau : Le service de traduction AI prend désormais en charge le norvégien.

## 1.13.6 Preview (2025-01-17)

- Amélioré : **AI Expert** peut être utilisé avec **AI Context-Aware Translation**.
- Amélioré : **Traduction d'image** est désormais compatible avec weibo.com (pris en charge uniquement sur Chrome et Edge).
- Amélioré : Lorsque la langue de l'interface est définie sur l'anglais, la langue cible par défaut pour la **Boîte de saisie améliorée** est changée en chinois.
- Amélioré : Ajout d'une entrée de révision de magasin dans les options **Plus** sur le panneau.

## 1.13.5 Release (2025-01-14)

- Amélioré : Compatible avec le modèle de pensée Gemini 2.0.
- Amélioré : Prend en charge le style gras en mode traduction uniquement.

## 1.13.4 Preview (2025-01-13)

- Ajouté : Les membres Pro peuvent désormais utiliser directement le modèle **Zhipu 4 Plus**.
- Amélioré : Traduction Gemini.

## 1.13.1 (2025-01-10)

- Ajouté : Lorsque le texte traduit et le texte original appartiennent au même système d'écriture, afficher la traduction en utilisant un style spécialisé.
- Corrigé : Problème où la **Traduction au survol de la souris** ne fonctionne pas sur certains sites web.
- Amélioré : DeepLx prend désormais en charge l'arabe.
- Amélioré : Amélioration de la reconnaissance de la langue originale. Auparavant, les pages contenant plusieurs langues pouvaient ne pas être traduites, mais maintenant elles le sont correctement.
- Amélioré : Pour Twitter, les traductions de contenu multiligne sont définies pour ne pas s'enrouler par défaut. L'enroulement se produira uniquement lorsque le contenu dépasse 10 lignes ou 1000 caractères. L'enroulement peut être activé via les paramètres **Paramètres avancés** -> **Activer l'enroulement automatique des lignes pour les longs paragraphes**.

## 1.12.8 (2025-01-03)

- Corrigé : Problème où la page des paramètres iOS 18.3 ne s'affiche pas correctement.
- Corrigé : Manque de lignes vides lors de la traduction de tweets.
- Corrigé : Problème de rupture forcée des nombres décimaux lors de la traduction de longs textes.

## 1.12.7 Release (2024-12-30)

- Amélioré : Bing/Google prennent désormais en charge le portugais (Brésil).
- Amélioré : Amélioration des descriptions pour la langue de l'interface utilisateur en chinois traditionnel.
- Amélioré : Ajustement de la mise en page pour les langues de droite à gauche dans les panneaux et les pages de paramètres.

## 1.12.6 (2024-12-26)

- Corrigé : Problème où la fonction de survol de la souris charge le mauvais service de traduction dans certaines conditions.
- Corrigé : Problème où l'activation temporaire des sous-titres bilingues sur YouTube ne fonctionne pas.
- Corrigé : Après avoir changé de services de traduction, le service de traduction dans la "**Boîte de saisie améliorée**" ne se met pas à jour.
- Corrigé : Le commutateur "**YouTube Enable Bilingual**" dans la page des paramètres ne fonctionne pas.
- Amélioré : Suppression du modèle gemini-1.0-pro obsolète.

## 1.12.4 (2024-12-13)

- Ajouté : **AI Context-Aware Translation** peut améliorer la précision de la traduction de contenu professionnel. (Disponible uniquement pour les membres Pro, pris en charge exclusivement par les modèles OpenAI) **Options** -> **Général** -> **Activer AI Context-Aware Translation**
- Corrigé : Certains bugs dans l'effet de traduction multiligne sur Twitter.
- Corrigé : Problèmes avec la traduction de certaines formules en raison du texte enrichi.
- Amélioré : Lors de la traduction sur **x.com**, les vidéos avec sous-titres auront automatiquement des sous-titres bilingues traduits.
- Amélioré : Les vidéos sans sous-titres afficheront une icône de traduction et fourniront une raison pour laquelle la traduction n'est pas possible.

## 1.11.7 (2024-11-25)

- Ajouté : Bing/Google prennent désormais en charge le khmer (cambodgien).
- Ajouté : Permettre aux fichiers ePub incomplets de continuer la traduction là où ils se sont arrêtés lors de la réimportation.
- Corrigé : Problème de traduction des images Twitter dans le navigateur Safari.
- Corrigé : Les raccourcis clavier deviennent inefficaces lors de l'activation ou de la désactivation de la fonctionnalité "**Traduction au survol**".
- Amélioré : Amélioration de l'affichage de la traduction bilingue multiligne sur Twitter et Youtube.
- Amélioré : La traduction de texte enrichi est désactivée par défaut en mode bilingue pour améliorer la qualité de la traduction.
- ~~Amélioré : Ajout de l'option pour personnaliser la "**Traduction de la barre latérale et de la barre de navigation**" dans les "**Paramètres avancés**".~~
- Amélioré : Les images ne sont plus traduites en mode "**Survol - traduire immédiatement ce paragraphe**".

## 1.11.4 (2024-11-16)

- Corrigé : Problème de traduction de formule causé par l'"Amélioration de la traduction Twitter" dans la version 1.11.2.

## 1.11.2 (2024-11-13)

- Corrigé : Problème où le contenu disparaît après avoir cliqué sur "voir plus" en mode traduction uniquement de Facebook.
- ~~Amélioré : Amélioration de l'affichage des traductions bilingues multiligne sur Twitter.~~
- Amélioré : Mise à jour de l'interface utilisateur de la liste déroulante du service de traduction dans le panneau.

## 1.11.1 (2024-11-05)

- Ajouté : La **Traduction des sous-titres** en temps réel prend désormais en charge l'activation via "balle flottante", disponible sur Zoom, Google Meet et Microsoft Teams.
- Corrigé : Problèmes de synchronisation des sous-titres sur YouTube après avoir regardé des publicités.
- Corrigé : Problèmes d'affichage avec le menu de traduction par clic droit dans Safari sur MacOS 15.
- Corrigé : Problèmes avec la fonctionnalité d'annulation Ctrl+Z dans la **Boîte de saisie améliorée** sur certains sites web.

## 1.10.6 (2024-10-25)

- Corrigé : Problème avec les raccourcis de la **Boîte de saisie améliorée** ne se déclenchant pas.
- Amélioré : Réduction de la taille du package d'installation.
- Amélioré : Solution d'affichage des sous-titres Netflix.

## 1.10.5 (2024-10-23)

- Ajouté : Afficher un avertissement lorsque la langue source et la langue cible sont identiques.
- Corrigé : Problème de traduction des caractères d'espacement du texte enrichi [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175).
- Amélioré : Amélioration de l'entrée et de la fonctionnalité de survol de la souris dans les iframes intégrées sur les pages web.

## 1.10.2 (2024-10-11)

- Ajouté : Traduction d'image (version bêta).
- Ajouté : Mode Forcer l'activation du support de la souris (Activez cette fonctionnalité uniquement si la fonction de survol de la souris n'est pas disponible sur les appareils tablette) **Paramètres** -> **Paramètres avancés** -> **Forcer l'activation du support de la souris**.
- Ajouté : Afficher un message d'erreur lorsque la traduction des sous-titres vidéo échoue.
- Corrigé : Problème de traduction de texte enrichi [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163).
- Amélioré : Résolution des problèmes où le bouton de traduction pourrait ne pas fonctionner lors de la traduction de PDF.
- Amélioré : Amélioration du rendu des formules traduites.
- Amélioré : Liste de sélection des langues.

## 1.9.8 (2024-09-28)

- Ajouté : Service de traduction "Zhipu BigModel".
- Supprimé : Modèle "SiliconCloud" qwen1.5-7B-chat (en raison de l'arrêt officiel).
- Corrigé : Résolution du problème de compatibilité de connexion avec le plugin Safari sur macOS 15.

## 1.9.7 (2024-09-20)

- Prise en charge améliorée de l'entrée pour Baidu, Gmail et d'autres champs de saisie
- Prise en charge de l'en-tête de requête anthropic-dangerous-direct-browser-access pour l'API Claude Anthropic
- Prise en charge du téléchargement de sous-titres à partir de vidéos Hulu, Bloomberg et Domestika
- DeepX prend en charge la traduction de texte enrichi
- Correction du problème de non-synchronisation des experts AI personnalisés

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) prend en charge la copie de formules (cliquez avec le bouton droit sur la formule pour voir le menu de copie)
- Correction du problème d'affichage des sous-titres bilingues pour plusieurs vidéos sur la même page Twitter
- Correction de quelques bugs

## 1.9.3 (2024-09-05)

- L'option d'affichage de comparaison bilingue/traduction uniquement a été déplacée vers les paramètres généraux.
- Par défaut, le système se souviendra du mode basculé en cliquant sur l'icône dans le panneau pour l'affichage de comparaison bilingue ou de traduction uniquement. Pour basculer temporairement, cliquez sur "Plus" -> "Passer à l'affichage de traduction uniquement" dans le panneau.
- Par défaut, la traduction du chinois simplifié vers le chinois traditionnel et vice versa utilisera le mode de traduction uniquement, plutôt que le mode de comparaison bilingue.
- Correction de quelques bugs.

## 1.9.1 (2024-09-03)

- Prise en charge de la configuration des exceptions pour les langues et les sites web en mode de contraste bilingue ou de traduction uniquement (configurer dans la page Paramètres -> Paramètres avancés). Par exemple : Si votre mode de traduction par défaut est le contraste bilingue, mais que vous ne souhaitez pas que le chinois traditionnel utilise également le contraste bilingue, vous pouvez ajouter le chinois traditionnel aux langues d'exception pour le contraste bilingue, de sorte que le chinois traditionnel utilisera le mode de traduction uniquement pour la traduction. De même, si votre mode de traduction par défaut est la traduction uniquement, mais que vous souhaitez qu'une certaine langue ou un site web utilise le mode de contraste bilingue, vous pouvez également ajouter cette langue ou ce site web aux langues d'exception.
- Correction d'un problème où la boîte de saisie dans l'interface de message privé de Tiktok était mal traduite
- Correction d'un problème où les bandes dessinées sur Read Comic Online ne pouvaient pas être traduites
- Correction d'un problème où le [Paramètres avancés -> Nombre minimum de caractères requis pour traduire un paragraphe] ne prenait pas effet dans certains cas

## 1.8.4 (2024-08-30)

- Le service de traduction DeepL prend désormais officiellement en charge le chinois traditionnel comme langue cible (auparavant, la traduction en chinois traditionnel avec DeepL impliquait un processus de conversion supplémentaire du chinois simplifié au chinois traditionnel par un tiers).
- Optimisation des performances de traduction de texte enrichi.

## 1.8.3

- Google Meet prend désormais en charge les sous-titres bilingues pour les réunions en direct : Désormais, vous pouvez profiter de la fonctionnalité de sous-titres bilingues dans les réunions Google Meet. Ouvrez simplement le lien de la réunion, activez les sous-titres bilingues dans le panneau de traduction immersive, puis actualisez la page pour en faire l'expérience.
- Ajout de l'option "Signaler les problèmes de traduction de la page web actuelle" et de l'option "Activer/désactiver rapidement la boule flottante" dans les options supplémentaires du panneau.
- Après avoir ajusté la position des sous-titres bilingues de YouTube, le système se souviendra automatiquement de la nouvelle position.
- Optimisation de la logique de cache du plugin, maintenant le cache des données de plus de 30 jours est automatiquement effacé.
- Optimisation des blocs de code dans les paragraphes pour une restauration plus précise du texte original.
- Amélioration de la gestion des "mots non traduisibles" dans les paramètres avancés.

## 1.8.2

- Vous pouvez désormais traduire du texte dans les boîtes de saisie avec un clic droit : Sélectionnez n'importe quel texte dans une boîte de saisie sur une page web, cliquez avec le bouton droit pour choisir de traduire, et la traduction immersive traduira automatiquement le texte sélectionné dans la langue cible de la boîte de saisie, ce qui permet de traduire rapidement le texte en langue maternelle dans les boîtes de saisie vers d'autres langues.
- Vous pouvez désormais signaler rapidement les problèmes de traduction des pages web dans la boule flottante de traduction immersive. Après avoir traduit une page web, s'il y a des problèmes, vous pouvez cliquer sur le bouton [Feedback] sur le côté droit de la boule flottante, remplir la description du problème, et nous le traiterons dès que possible.
- Les fichiers Epub prennent désormais en charge la traduction de texte enrichi (c'est-à-dire en préservant le format du texte original de chaque paragraphe, comme les liens, le gras, etc.)
- Prise en charge des sous-titres bilingues en temps réel dans les réunions vidéo de la version web de Microsoft Teams (Ouvrez le lien de la réunion Teams, activez les sous-titres bilingues dans le panneau de traduction immersive, puis actualisez)
- Optimisation des sous-titres bilingues pour la version anglaise d'iQIYI (iq.com)
- Fourniture de plus d'articles arXiv avec une mise en page de traduction bilingue optimisée
- En raison des restrictions du site YouTube, le script Chrome Tampermonkey ne prend plus en charge les sous-titres bilingues de YouTube. Veuillez utiliser la [version plugin](https://immersivetranslate.com/).

## 1.8.1

- Correction des problèmes de traduction avec le script Tampermonkey SiliconCloud
- La traduction Claude prend désormais en charge le tibétain et permet la configuration du paramètre de température
- La page de détails de l'expert AI affiche les invites utilisées par l'expert
- Les paramètres de raccourci permettent désormais d'attribuer des touches de raccourci uniques pour tout service de traduction
- Optimisation de la détection des traductions d'articles arXiv

## 1.7.9

- Correction des problèmes de traduction de texte enrichi pour les services de traduction tels que Google, DeepL (par exemple, les pages affichant directement `<button>` etc.)
- Correction du problème où le raccourci bilingue pour les vidéos YouTube ne pouvait pas être désactivé.

## 1.7.8

- DeepL, Microsoft Translate, Google Translate, OpenAI, Claude, Gemini et d'autres services de traduction prennent en charge la traduction pour conserver le formatage du texte original (par exemple, les liens, le gras, etc.)
- Après avoir sélectionné le texte, le menu contextuel changera en [Traduire le texte], en cliquant dessus, vous pouvez automatiquement accéder à la page de traduction de texte immersive
- Nouveau service de traduction gratuit pour les grands modèles : SiliconCloud, disponible pour tous les utilisateurs.
- Ajout de la traduction de grand modèle Zero-One-Thing, qui peut être utilisée en remplissant la clé API après inscription sur la plateforme Zero-One-Thing.
- Nouveau bouton de retour d'utilisateur pour la traduction de mangas (après avoir traduit un manga, cliquez sur le bouton [Feedback] sur le côté droit de la boule flottante pour donner votre avis sur la qualité de la traduction).

## 1.7.7

- Adoption de l'algorithme de découpage de phrases intelligent AI pour les sous-titres anglais auto-générés sur YouTube [Pro Disponible]
- Optimisation de la traduction par clic droit en "Traduire vers xx langue cible"
- Prise en charge de l'intégration immersive [JS SDK](https://immersivetranslate.com/docs/js-sdk/) pour les sites web tiers
- Optimisation de l'affichage des sous-titres Hulu
- Prise en charge de la traduction des sous-titres des réunions de la version web de ZOOM

## 1.7.6

- Prise en charge de la personnalisation des experts AI, l'entrée se trouve en bas de la page [Paramètres]->[Expert AI].
- Optimisation du chargement des sous-titres sur le site TED
- Le portugais (Brésil) est pris en charge comme langue du plugin.
- Sites pris en charge pour la traduction de bandes dessinées
  - [Antbyw](https://www.antbyw.com)
  - [Zerobywzz](https://www.zerobywzz.com)
  - [动漫之家](https://www.idmzj.com)
  - [Jmanga](https://jmanga.org)

## 1.7.5

- Activation de la copie des sous-titres YouTube
- Optimisation de l'affichage des sous-titres sur certains sites vidéo
- Amélioration de la vitesse de traduction des mangas

## 1.7.2

- Correction de l'échec de la traduction de bandes dessinées dans le navigateur Firefox.

## 1.7.1

- Amélioration de la vitesse de traduction pour les traductions de bandes dessinées
- Ajout de la prise en charge de nouveaux sites dans les traductions de bandes dessinées :
  - [ShonenJumpPlus](https://shonenjumpplus.com)
  - [Heros Web](https://viewer.heros-web.com/)
  - [Comic Days](https://comic-days.com/)
  - [ComicWalker](https://comic-walker.com/)
  - [Web Ace](https://web-ace.jp/)

## 1.6.6

- Ajout de la prise en charge de nouveaux sites pour la traduction de bandes dessinées :
  - [Mangabuddy](https://mangabuddy.com/)
  - [Hitomi](https://hitomi.la)
  - [Yamibo](https://www.yamibo.com)
  - [Copymanga](https://www.copymanga.site/)
- Les sous-titres bilingues de YouTube prennent désormais en charge le découpage de phrases intelligent (Beta) (Uniquement lors de l'activation manuelle de la traduction immersive des sous-titres YouTube dans [Paramètres] - [Sous-titres vidéo], et les sous-titres vidéo originaux sont des sous-titres anglais auto-générés)
- Ajout du service de traduction Tencent [【Hunyuan Large Model】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- Correction des problèmes de mise en page du texte des traductions de bandes dessinées pour les langues en écriture latine.
- Nouveaux sites pris en charge pour la traduction de bandes dessinées :
  - COMIC FUZCOMICFUZ(https://comic-fuz.com/)
  - MangaDexMangaDex(https://mangadex.org/)
  - KuaiKan ComicsKuaiKanComics(https://www.kuaikanmanhua.com/)
- Correction d'un problème où les services AI personnalisés ne pouvaient pas sélectionner d'experts AI.

## 1.6.4

- Lorsque les experts AI sont utilisés pour la "Sélection intelligente", différents experts AI peuvent être personnalisés pour différents sites web. Cela peut être configuré dans [Paramètres] -> [Experts AI] -> [Entrer n'importe quel expert].
- Correction du problème où les sous-titres ne s'affichent pas sur YouTube en mode "Traduction uniquement".
- Correction du problème des sous-titres bilingues ne fonctionnant pas sur Mubi.
- Compatible avec les PDF ouverts avec le plugin Adobe Acrobat.
- Tous les utilisateurs peuvent [contribuer en ligne](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/) à la traduction multilingue de l'interface de traduction immersive.

## 1.6.3

- Nouvelle fonctionnalité : Traduction de mangas (Beta), sur les sites de mangas pris en charge, un bouton de traduction de mangas apparaîtra sous la boule flottante de traduction rapide de la page web. En cliquant dessus, vous activerez la traduction de mangas. Cette fonctionnalité est disponible pour les membres Pro (500 pages par mois, des packs supplémentaires peuvent être achetés), actuellement prise en charge sur les sites suivants :
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)

## 1.6.2

- Nouvelle fonctionnalité : Traduction de manga (Beta), sur les sites de manga pris en charge, un bouton de traduction de manga apparaîtra sous la bulle flottante de traduction rapide de la page web. En cliquant dessus, la traduction de manga sera activée. Cette fonctionnalité est disponible pour les membres Pro (500 pages par mois, des packs supplémentaires peuvent être achetés), actuellement prise en charge sur les sites suivants :
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- Nouvelle fonctionnalité : La traduction AI prend en charge le [modèle large Doubao](https://www.volcengine.com/product/doubao)
- Nouvelle fonctionnalité : Prise en charge du mode de comparaison bilingue avec la traduction d'abord et le texte original ensuite, qui peut être activé dans la page des paramètres -> paramètres avancés.
- La liste des modèles AI personnalisés prend en charge la syntaxe `-all`, qui peut supprimer tous les modèles prédéfinis.
- Dans les sous-titres vidéo bilingues, lorsque la langue cible est le chinois simplifié et que le texte original est en chinois traditionnel, le texte original sera automatiquement converti en chinois simplifié, et vice versa.
- Correction du problème où le raccourci de la bulle flottante ne pouvait pas traduire sous iOS 18.
- Correction du problème où les Prompts personnalisés étaient inefficaces lorsqu'ils étaient trop nombreux.

## 1.6.1

- Prend en charge la plateforme de modèle large Baidu Qianfan, la plateforme de modèle large Alibaba Bailian, la plateforme de modèle large DeepSeek.
- Correction du problème où la modification de la langue cible et d'autres paramètres dans le panneau contextuel se réinitialisait lors du clic sur la bulle flottante de traduction.

## 1.5.8

- Les experts AI prennent en charge le mode "Sélection Intelligente", où le système sélectionnera automatiquement l'expert AI le plus approprié en fonction du site web actuel (par exemple, les experts AI liés à la technologie seront automatiquement sélectionnés pour The Verge et Hacker News, tandis que l'amélioration de la traduction Twitter sera automatiquement sélectionnée pour Twitter).

## 1.5.7

- Prise en charge de l'ajout de services de traduction AI personnalisés compatibles avec OpenAI, accessibles en bas de la page [Paramètres]->[Services de Traduction].
- Correction d'un problème où les sous-titres bilingues ne fonctionnaient pas sur la plateforme vidéo Domestika dans Safari.

## 1.5.6

- Optimisation significative des performances de traduction de grandes pages web, de la création d'ePub et des fichiers de sous-titres.
- Correction du bug de synchronisation multi-appareils dans Pro.

## 1.5.4

- Les membres Pro prennent en charge les services de traduction Claude et Gemini prêts à l'emploi (Beta)
- Les sous-titres bilingues YouTube prennent en charge les paramètres de police et de poids de la police
- Correction des problèmes de limites de mots lors de l'emballage de longs paragraphes [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- Correction de la reconnaissance des langues japonaise et coréenne
- Correction du problème où les pages Reddit sur les appareils mobiles n'étaient pas traduites lors du défilement
- Correction de certaines pages manquant de traductions avec DeepL
- Correction du temps de synchronisation multi-appareils des utilisateurs Pro qui ne se synchronisait pas
- Optimisation des problèmes de couverture des paramètres de synchronisation cloud
- Optimisation des mots de prompt pour les services de traduction AI

## 1.5.2

- Correction du problème où les modifications du prompt expert général remplaçaient le prompt expert AI spécifié [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- Le nom du modèle AI personnalisé prend en charge la syntaxe avancée, utilisez + pour ajouter un modèle, utilisez - pour masquer un modèle, et utilisez model_name=display_name pour personnaliser le nom d'affichage du modèle, par exemple : +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- Correction de l'erreur retournée par Gemini
- Masquer la bulle flottante lors de l'impression de la page
- Correction de la taille de la police ne s'adaptant pas proportionnellement lorsque YouTube est en plein écran [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- Prise en charge des services de traduction AI pour définir [AI Expert] afin de spécifier la stratégie de traduction, actuellement une fonctionnalité Beta, qui peut être activée dans les [Paramètres Développeur](https://dash.immersivetranslate.com/#developer) après avoir activé Beta, et le menu [AI Expert] peut être vu après actualisation.
- Les services de traduction AI peuvent désormais personnaliser la liste des modèles, tels que [OpenAI], le système n'a que quelques-uns des modèles les plus couramment utilisés intégrés. En cliquant sur la liste déroulante des modèles, le dernier élément que vous voyez est [Définir Plus de Modèles], après réglage, il sera automatiquement mémorisé pour la commodité des utilisateurs testant différents modèles personnalisés.
- Optimisation de l'incohérence dans la mise en page des traductions dans certains cas.
- Ajout d'un bouton de réinitialisation pour le style des sous-titres YouTube, qui peut rapidement restaurer le style par défaut.
- Correction du problème où les sous-titres chinois ne pouvaient pas être téléchargés sur YouTube.
- Optimisation de la copie de l'interface en chinois traditionnel.

## 1.4.12

- Correction du problème de boîte de dialogue de message non traduit lors de l'ouverture de la page reddit
- Ajout d'une fonctionnalité temporaire pour activer l'édition de traduction dans l'entrée "Plus" du panneau
- Correction du problème où les Shorts YouTube sans sous-titres affichent toujours les sous-titres de la vidéo précédente [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- Correction du problème où les sous-titres bilingues YouTube ne peuvent pas être ajustés de haut en bas en plein écran [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- Prise en charge des sous-titres bilingues [VK Video](https://vk.com/video)
- Prise en charge des paramètres d'activation indépendants pour les sous-titres vidéo bilingues YouTube (activé par défaut pour les nouveaux utilisateurs)
- Optimisation des messages d'erreur pour la traduction des sous-titres bilingues locaux

## 1.4.11

- Compatible avec la traduction de la boîte de saisie de la page Bing Copilot
- Le contrôle du style des sous-titres YouTube prend en charge le style des bords
- Prise en charge de la sélection du service de traduction par défaut sur la page Paramètres -> Service de Traduction
- Correction du remplacement du placeholder OpenAI SystemPrompt
- Correction du problème de fusion des règles utilisateur personnalisées
- Correction de l'affichage anormal des sous-titres pour certaines vidéos Netflix [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- Correction du problème où les changements fréquents de couleur de traduction via la palette de couleurs étaient inefficaces [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- Les services de traduction sont désormais distinctement organisés sous un onglet séparé, permettant une vue d'ensemble complète de tous les services de traduction disponibles. De plus, les utilisateurs ont la flexibilité de personnaliser quels services de traduction sont affichés. Par défaut, seule une sélection limitée de services de traduction est affichée, mais les utilisateurs peuvent adapter leurs préférences d'affichage dans la section [Plus de Services](https://dash.immersivetranslate.com/#services).
- La page des paramètres permet désormais des ajustements aux [styles de sous-titres YouTube](https://dash.immersivetranslate.com/#subtitle).
- Des améliorations ont été apportées pour résoudre le problème où les sous-titres bilingues immersifs ne s'affichaient pas lorsque les utilisateurs définissaient la langue des sous-titres sur le chinois sur le site YouTube.
- Un nouveau raccourci a été introduit pour la traduction temporaire nommée Claude, qui peut être configuré dans la [page des Paramètres de Raccourci](https://dash.immersivetranslate.com/#shortcuts).

## 1.4.8

- Optimisation des performances de traduction pour les gros fichiers dans PDF-Pro
- Amélioration des performances de traduction pour les pages de contenu long
- Mise en œuvre de la prise en charge de l'internationalisation (i18n) pour la navigation dans les documents de page
- YouTube introduit une fonctionnalité pour activer temporairement les sous-titres bilingues
- YouTube prend en charge le téléchargement de sous-titres bilingues (membres uniquement)
- Mobile ajoute le contrôle gestuel, améliorant l'entrée via les [paramètres de raccourci](https://dash.immersivetranslate.com/#shortcuts)
- Prise en charge de la traduction bilingue pour Google Docs

## 1.4.7

- Correction du problème où la traduction échouait lors du changement de mots de prompt personnalisés OpenAI sous le bouton de test
- Correction du problème de l'icône de raccourci des sous-titres YouTube ne s'affichant pas
- Optimisation de la reconnaissance de la langue de l'extension

## 1.4.6

- Correction du problème où les mots de prompt définis par l'utilisateur étaient inefficaces
- Ajout d'options 50%, 150% pour la taille de la police des sous-titres YouTube

## 1.4.5

- Correction du problème où les changements de styles de sous-titres YouTube n'étaient pas enregistrés
- Correction de la disparition des sous-titres en plein écran sur iOS Safari
- Optimisation supplémentaire de la vitesse de traduction des sous-titres YouTube
- Les options supplémentaires du panneau prennent désormais en charge l'[entrée de traduction de texte](https://app.immersivetranslate.com/text/)

## 1.4.2

- Prise en charge du service de traduction Claude
- Optimisation des mots de prompt multi-OpenAI, prenant en charge le format YAML, ce qui améliore la flexibilité et la facilité d'utilisation de la configuration
- Optimisation significative de la vitesse de traduction des sous-titres YouTube, et ajout de la prise en charge du changement d'ordre chinois-anglais, de la personnalisation de la couleur et de la taille de la police, etc.
- La plateforme de sous-titres vidéo prend en charge [University of Southampton](https://southampton.cloud.panopto.eu)
- Les sous-titres bilingues Udemy compatibles avec l'affichage mobile
- Le service de traduction Gemini est masqué par défaut, peut être activé dans les paramètres développeur pour montrer la beta de ce service de traduction

## 1.3.4

- Prise en charge du service de traduction gratuit Yandex
- Optimisation des mots de prompt Gemini
- Les sous-titres vidéo prennent en charge le réglage pour l'affichage bilingue/original et traduction
- Prise en charge de l'espace entre le chinois et l'anglais dans les résultats de traduction OpenAI
- Le commutateur du panneau pour n'afficher que le bouton de traduction modifié pour ne prendre effet que sur la page actuelle

## 1.3.3

- Optimisation du problème d'affichage de la traduction des sous-titres vidéo Twitter CC.
- Le service DeepL a ajouté la prise en charge de l'arabe.
- Le service de traduction Colorful Clouds prend désormais en charge le coréen, l'espagnol, le français et le russe.
- Le service OpenAI a ajouté la prise en charge du dialecte chinois du nord-est.
- La détection automatique du panneau affiche désormais la langue originale.
- Ajustement de la description du raccourci pour le panneau mobile.

## 1.3.2

- Correction du problème où le panneau de contrôle ne pouvait pas être fermé sur les appareils mobiles

## 1.3.1

- La plateforme de sous-titres vidéo prend en charge [DeepLearning.ai](https://learn.deeplearning.ai)
- Prise en charge de la traduction de pages web et de sous-titres vidéo dans des langues telles que l'arabe, l'hébreu, etc., traitant des problèmes d'affichage RTL (de droite à gauche)
- Correction de la traduction Gemini en hébreu
- Correction d'un problème où certains sous-titres chinois traditionnels sur YouTube ne pouvaient pas être affichés correctement
- Correction du problème d'affichage des sous-titres Twitter sur Safari
- Correction du raccourci pour la traduction immédiate en bas de la page

## 1.2.4

- Correction du problème où les placeholders dans la création d'ePub n'étaient pas remplacés correctement
- Prise en charge de la traduction des sous-titres vidéo [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- Optimisation du contrôle de la fréquence des requêtes de service de traduction
- Les récentes requêtes de service de traduction Microsoft depuis la Chine ont été instables ; en cas d'erreurs, le système détecte automatiquement le service de traduction actuellement disponible, permettant aux utilisateurs de basculer rapidement.
- Optimisation du message d'erreur pour les erreurs réseau
- Correction du problème où la configuration de la couleur du texte ne supportait pas l'aperçu RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Correction du problème où la mise à jour de la version du plugin Safari affichait toujours la page de succès d'installation
- Microsoft a ajouté le support pour le vietnamien
- Correction du problème où les sous-titres traduits sur le site edx ne s'affichaient pas

## 1.2.2

- Support de la traduction des sous-titres vidéo pour [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). Supporte également la traduction de certaines vidéos sous-titrées CC sur Twitter.
- Optimisation des pop-ups d'erreur, les pop-ups d'erreur de problème réseau détectent automatiquement les services de traduction gratuits valides.
- Correction du support de l'application immersive iOS pour la lecture en plein écran sur YouTube.
- Correction du problème de traduction de paragraphe avec Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Support de la traduction des sous-titres vidéo pour [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/).
- Correction d'un problème où certains utilisateurs Pro ne pouvaient pas modifier les paramètres dans le navigateur Chrome.
- Support de l'affichage des sous-titres bilingues en mode plein écran sur YouTube sur iOS.

## 1.2.0

- Support de la traduction des sous-titres vidéo sur les plateformes [LinkedIn](https://www.linkedin.com/) et [Viu](https://www.viu.com/).
- Ajout de plus d'accès rapide aux sous-titres vidéo pour des plateformes supplémentaires.
- Support de la configuration de sites web/langues spécifiques pour n'afficher que le texte traduit.
- Correction d'un problème où la page des paramètres affichait continuellement le chargement dans certains cas sur Safari.
- Support de la traduction des nœuds de balise d'entrée.
- Optimisation de l'interface utilisateur des pop-ups d'erreur.

## 1.1.9

- Support de la traduction des sous-titres pour YouTube Live et la plateforme [Mubi](https://mubi.com/).
- Optimisation : Page des paramètres, interface utilisateur de la liste des URL (pour éviter toute ambiguïté, les cases à cocher ne sont pas affichées par défaut).
- Support de la configuration de la police de traduction en mode traduction uniquement.
- Ajout d'un accès rapide pour activer les sous-titres vidéo sur Netflix, Ted, Bloomberg, Udemy, Coursera.
- Correction : Certains styles traduits (comme les soulignements) n'étaient pas efficaces sur Safari.
- Correction : Lors de la traduction de la page, le problème où le survol de la souris ne déclenchait pas la retraduction.

## 1.1.8

- Ajout d'une option pour que le service de traduction enfant suive le service de traduction principal
- Support des sous-titres bilingues pour [Amazon Prime Video](https://www.primevideo.com)
- Optimisation supplémentaire de la fonction de traduction de PDF intégrée dans Sci-Hub
- Correction d'un problème avec les PDF en ligne ne s'ouvrant pas correctement
- Correction du problème de lecture continue des sous-titres bilingues sur Netflix

## 1.1.7

- Vous pouvez maintenant spécifier une police pour la traduction dans la page des paramètres -> [Paramètres de base] -> [Style de traduction]
- Ajout d'une configuration de raccourci pour [Traduire le paragraphe spécifié] dans le panneau de la boule flottante sur les appareils mobiles
- Optimisation de la sensibilité de la détection du survol de la souris sur Ctrl pour éviter de confondre `Ctrl+C` avec `Ctrl`
- Ajout du support pour un nouveau paramètre de raccourci permettant de basculer rapidement si les sous-titres vidéo utilisent les sous-titres de traduction automatique intégrés
- Sur le site Sci-Hub, cliquer sur la boule flottante traduira les PDF intégrés dans la page web

## 1.1.6

- **Support mobile pour la traduction de paragraphes spécifiques :** La version mobile supporte maintenant la traduction de paragraphes spécifiés et a ajouté une variété d'opérations de raccourci, y compris le balayage vers la gauche, le balayage vers la droite, le double tapotement, le triple tapotement et les gestes de toucher multi-doigts. Ceux-ci ne sont pas activés par défaut et nécessitent que l'utilisateur sélectionne activement le geste de déclenchement dans la page des paramètres sous [Survol de la souris].
- **Mise à jour de la version par défaut de Gemini :** La version par défaut est maintenant `v1beta`.
- **Correction de la traduction du chinois classique :** Correction de la fonctionnalité de traduction du chinois classique de Microsoft et OpenAI.
- **Optimisation de la traduction japonaise :** Optimisation supplémentaire de la traduction japonaise d'OpenAI pour améliorer la précision et la fluidité.
- **Expérience de traduction immersive :** Pour mieux s'adapter aux habitudes des utilisateurs, nous avons déplacé le raccourci pour les sous-titres bilingues en mode plein écran sur la plateforme YouTube vers le côté gauche.

## 1.1.5

- Correction du problème où le menu déroulant en mode sombre sur Windows n'avait pas de couleur.
- Correction du problème d'alignement avec l'option "Plus" n'étant pas alignée à gauche sur Windows.

## 1.1.4

- **Mise à niveau de l'interface utilisateur du panneau contextuel :** Le nouveau design vise à améliorer l'utilisabilité et la compréhension. Cette mise à jour inclut :

  - **Nouvelles fonctionnalités dans le menu principal :**
    - **Commutateur de mode bilingue/traduction uniquement :** Vous pouvez maintenant basculer entre le "Mode de traduction bilingue" et le "Mode de traduction uniquement" directement dans le menu principal, situé à gauche du bouton de traduction.
    - **Entrée de traduction de document :** L'entrée pour traduire les fichiers "PDF/ePub/sous-titres" a été déplacée vers le menu principal pour un accès rapide.
    - **Paramètres de traduction vidéo :** L'entrée pour les paramètres de "Traduction vidéo" a également été placée dans le menu principal pour des ajustements rapides.
    - **Nouvelle entrée pour la documentation d'utilisation :** Fournit des guides d'opération détaillés et des documents d'aide.

- **Entrée de traduction de document intégrée :** Vous pouvez maintenant traduire des fichiers PDF, ePub et de sous-titres via une entrée de téléchargement unifiée. Il suffit de cliquer sur le bouton [PDF/ePub] dans le panneau contextuel, plus besoin de sélectionner [Plus].

- **Ajout du support pour 5 sites web vidéo :**
  - Support des sous-titres des podcasts sur Youtube Music.
  - Ajout du support pour le site iview.abc.net.au.
  - Ajout du support pour le site www.nma.art.
  - Ajout du support pour le site creativecloud.adobe.com.
  - Ajout du support pour le site www.masterclass.com.

## 1.1.3

- Correction du problème d'anomalie d'affichage du plugin mobile lors de l'ouverture de pages PDF.
- Optimisation de l'effet de traduction des conversations GPT.
- Support de la traduction de domaine pour Baidu Translate.
- Ajout d'un mode traduction uniquement dans la page des paramètres.
- Ajout d'une fonction de rappel lors du changement de mode de traduction avec des raccourcis.
- Correction du problème où la traduction des champs d'entrée contenant des URL ne traduisait que des parties du contenu.

## 1.1.2

- Correction : Le problème où le changement de service de traduction ne prenait pas effet lorsque la page n'avait pas encore été traduite.
- Optimisation : Dans le processus de traduction d'Epub et de PDF, si certains contenus échouent à être traduits, il est maintenant possible de passer à un autre service de traduction sur le panneau sans redémarrer l'ensemble du processus de traduction (la logique précédente était d'utiliser immédiatement un nouveau service de traduction pour retraduire l'ensemble du livre). Cela signifie qu'à mi-chemin de la traduction, vous pouvez passer à un service de traduction différent et cliquer sur [Réessayer tous les paragraphes échoués], après quoi le système continuera la traduction en utilisant le nouveau service.
- Optimisation : Ajustement de la taille de la police des messages d'erreur de traduction pour améliorer la lisibilité.

## 1.1.1

- Correction du problème du raccourci des sous-titres bilingues pour YouTube ayant un texte anglais trop long.

## 1.1.0

### Nouvelles fonctionnalités

- **Paramètres de raccourci clavier** : Ajout d'un nouveau menu de niveau supérieur "Raccourcis" et des fonctions de raccourci clavier personnalisables suivantes :

  - Désigner une combinaison de touches pour traduire le contenu de la boîte d'entrée actuelle, en complément de la méthode précédente de frapper rapidement la barre d'espace trois fois.
  - Désigner une combinaison de touches pour activer temporairement la "traduction directe au survol de la souris" sur la page. Appuyer à nouveau annulera cette fonction.
  - Ajout de touches de raccourci dédiées pour 6 services de traduction (tels que DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation) pour faciliter le changement temporaire entre les services de traduction.

- **Mise à jour de l'interface utilisateur de la page des paramètres du plugin** :

  - Dans "Paramètres avancés", une nouvelle option a été ajoutée pour permettre aux utilisateurs de spécifier certains mots (par exemple, "LLM") à exclure de la traduction.
  - Dans "Paramètres avancés", une nouvelle option a été ajoutée pour configurer le nombre minimum de caractères requis pour traduire un paragraphe. Le défaut est de 4 caractères, mais il peut être réglé plus haut (par exemple, 20), de sorte que seuls les paragraphes plus longs seront traduits.
  - Ajout d'un tutoriel pour les débutants, couvrant les paramètres de la boule flottante, les paramètres des sous-titres vidéo et les paramètres de survol de la souris.

- **Sous-titres bilingues YouTube** : Ajout d'un accès rapide dans la fenêtre de lecture vidéo YouTube pour activer ou masquer les sous-titres bilingues (cette fonctionnalité peut être désactivée).

- **Support de la langue Deepl** : Ajout du support pour le portugais (Brésil).

- **Guide pour les nouveaux utilisateurs** : Lorsque de nouveaux utilisateurs ouvrent pour la première fois une page dans une langue non cible, une bulle d'aide de la boule flottante est affichée.

### Optimisation et corrections

- **Optimisation de l'interface utilisateur** : Refonte de l'interface utilisateur pour les messages d'erreur de traduction de page pour les rendre plus compréhensibles. Lorsqu'il y a de nombreuses erreurs, un pop-up avertira activement l'utilisateur.

- **Corrections de bugs** :

  - Correction du problème où la traduction au survol de la souris échouait lorsque la page perdait le focus.
  - Correction du problème où moins de 3 caractères dans la fonctionnalité d'amélioration de la boîte d'entrée n'étaient pas traduits.
  - Correction du problème où certains répertoires n'étaient pas traduits lors de la production de livres électroniques bilingues.

- **Suppression de fonctionnalité** : Suppression de la fonctionnalité d'amélioration de l'information bilingue (affichage simultané des résultats de recherche en anglais sur les pages de recherche Google).

### Autres mises à jour

- **Mise à jour de la configuration openAI** : Supporte maintenant la configuration du nombre de configurations par seconde en décimales, comme 0.5, signifiant 1 requête toutes les 2 secondes.

## 0.12.14

- Correction : Le problème de reconnaissance de la langue cible par défaut sur certaines machines après la première installation.
- Optimisation : L'ordre par défaut des titres de page web est changé en [Chinois - Anglais].

## 0.12.13

- Correction : Problème de couture de traduction de longs paragraphes OpenAI dans certains cas. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Optimisation : Lors de l'utilisation du survol de la souris, le problème où la perte de focus sur la page puis le retrigger devient inefficace.
- Correction : Le problème où le cache existe toujours après la modification de l'invite/modèle dans OpenAI.

## 0.12.12

- Mis à jour : Optimisation du panneau contextuel, suppression de certaines options pour le site web actuel.
- Optimisé : Amélioration du processus de fusion des sous-titres manuels.
- Optimisé : Définition automatique de la langue cible en fonction de la langue du navigateur.
- Ajouté : Support des sous-titres bilingues pour la plateforme d'apprentissage [ArtStation](https://www.artstation.com/learning) et [ZDF](https://www.zdf.de/).
- Corrigé : Résolution du problème où les titres sur la page de liste jstor n'étaient pas traduits [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Corrigé : Correction du problème où seule une partie du contenu disparaissait sur Hacknews [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Ajouté le support des sous-titres bilingues pour les plateformes [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/), et [Domestika](https://www.domestika.org).

## 0.12.10

- Correction du problème d'autorisation du domaine Gemini sous le script Tampermonkey.
- Support de la traduction en temps réel des sous-titres pour Twitter Space.
- Pour les anciennes versions du script Tampermonkey, une invite de mise à jour a maintenant été ajoutée à la page des paramètres.

## 0.12.9

- Ajout du support pour la traduction Gemini.
- Correction du problème où les traductions ne répondaient pas à temps lorsque la page web était défilée jusqu'à la position médiane dans certains cas.
- Correction du bug où le changement de sous-titres sur certains sites vidéo provoquait l'affichage répété de la traduction.
- Correction du problème où la souris survolait pour continuer à traduire sans maintenir la touche de raccourci dans certains cas.
- Sur macOS, optimisation du nom d'affichage du raccourci du panneau.

## 0.12.8

- Réparation des sous-titres vidéo originaux qui ne s'affichent pas lorsque "Le site actuel est défini pour ne jamais traduire".
- Réparation du conflit avec certains plug-ins qui causent un retour infini de la page.
- Réparation de la non-traduction de certains paragraphes après avoir activé les sauts de ligne de longs paragraphes.
- Correction [Lorsque la traduction de la page web est temporairement activée pendant une longue période, cliquer sur le panneau [Toujours traduire ce site web] ne désactive pas la traduction permanente #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Ajout de sous-titres bilingues pour les plateformes [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/).
- La hoverball est maintenant cachée par défaut lorsque la vidéo est en plein écran.
- Correction du problème de clic saccadé du panneau d'action de la hoverball sur la page Firefox.
- Support de la collaboration sous le site pubmed.ncbi.nlm.nih.gov et le plugin scholarscope.
- Correction du problème de saccade de la page de traduction de la boîte de saisie reddit.

## 0.12.6

- Correction du problème de sensibilité de la traduction de YouTube/Web of Science, etc. lors du changement d'onglet.
- La hoverball sur mobile supporte maintenant l'opération de pression longue, pression courte pour traduire, pression longue pour ouvrir le panneau.
- La traduction des ebooks bilingues traduira désormais également la table des matières.
- La fonction d'amélioration de la recherche (certaines pages de Google Search affichent des résultats de recherche bilingues) n'est plus activée par défaut et sera supprimée dans la prochaine Release.

## 0.12.5

- Correction de la création d'eBooks Epub à partir du panneau en cliquant sur les traductions qui ne fonctionnent pas.

## 0.12.4

- Lorsque vous activez les sous-titres bilingues dans le panneau, la page se rafraîchira automatiquement (pour afficher plus précisément les sous-titres bilingues), et certains sites nécessitent encore que les utilisateurs cliquent manuellement sur le bouton "CC" du site pour activer les sous-titres.
- Optimisation de Grease Monkey, détection de la langue Safari.
- Fournit un accès rapide aux versions bilingues de tous les articles sur le site de papiers [Arxiv](https://arxiv.org/abs/1910.06709).
- [Support de la hoverball configurée pour être fixée à gauche #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Correction du problème d'affichage du mode d'apprentissage #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Activer temporairement la traduction web pendant une période de temps ne désactive pas Toujours Traduire #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Optimisation des problèmes d'initialisation des fichiers PDF.

## 0.12.3

- Correction pour la fonction [désactiver définitivement les sous-titres vidéo] qui ne fonctionne pas [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175).

## 0.12.2

- Le support des sous-titres bilingues est fourni pour plus de plateformes vidéo, qui sont maintenant supportées : [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy](https://www.khanacademy.org/), [Coursera](https://www.coursera.org/), [Vimeo](https://vimeo.com/), [Nebula](https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), etc. (Notez qu'en raison des limitations techniques, certains sites web doivent rafraîchir la page après avoir activé les sous-titres bilingues pour la première fois ou attendre que la traduction soit terminée pour afficher les sous-titres bilingues).
- Optimisation significative de la taille du fichier zip du plugin, réduite de moitié par rapport à l'original, téléchargement et mise à jour plus rapides.
- Correction des problèmes de téléchargement PDF étendu.
- Ajout d'un portail PDF de traduction rapide sur le côté droit du site de papiers [Arxiv](https://arxiv.org/abs/1910.06709), qui mène à une page HTML propre (seulement supportée par certains papiers, car elle nécessite que les auteurs originaux soumettent le code source, donc environ 50% des papiers afficheront ce portail).
- Les pages PDF en ligne sans extension .pdf peuvent maintenant sauter directement à la page de traduction PDF en cliquant sur la hoverball sur la page.
- Correction de certains problèmes d'amélioration de la boîte de saisie sous Safari.
- Optimisation de la détection de la langue dans Grease Monkey et Safari.

## 0.11.6

- Ajout de 11 nouvelles langues d'interface pour le plugin et le site officiel, maintenant les langues d'interface supportées atteignent 14, y compris le chinois simplifié, le chinois traditionnel, l'anglais, le japonais, le coréen, le russe, l'espagnol, le portugais, l'hindi, l'italien, l'allemand, le français, l'arabe et le persan.
- Modification du partage bilingue (mode rafraîchissement) ajouté dans la dernière version pour le partage de capture d'écran de page bilingue, afin que le contenu partagé soit plus original, ainsi qu'une adaptabilité plus large.
- Correction de l'emoji à la fin de la boîte de saisie Twitter qui ne peut pas être traduit.
- Correction de la situation où le contenu des plug-ins tiers est traduit dans certains scénarios.
- Réparation du clic non réactif de la hoverball en ligne pdf.

## 0.11.5

- Vous pouvez maintenant générer un lien public vers la page bilingue traduite pour Immersive Translate.
  - [Cliquez](/docs/share/) sur l'icône de partage Immersive Translate pour le générer en un clic !
- Résolution du problème où certaines plateformes ne pouvaient pas reconnaître si la souris était supportée ou non.
  - Il existe certains navigateurs de bureau qui supportent à la fois l'écran tactile et la souris, et Immersive Translate est techniquement incapable de détecter si ces plateformes supportent la souris, nous avons donc ajouté l'option [Forcer l'activation du support de la souris] dans le paramètre [Survol de la souris].

## 0.11.2-0.11.4

- Optimisation de l'expérience, correction de certains bugs.

## 0.11.1

- Le modèle par défaut pour les traductions OpenAI est : GPT3.5-turbo-1106.
- Optimisation de l'invite chinoise pour OpenAI, maintenant moins sujette aux hallucinations !
- Réduction de la longueur des invites d'OpenAI de 90 à 40, économisant encore plus de trafic.

## 0.11.0

- Correction des clics saccadés de la hoverball de page.
- Correction des problèmes de traduction Azure.

## 0.10.9

- Correction de quelques problèmes mineurs.

## 0.10.8

- Support de la configuration des boutons de traduction rapide de la hoverball (support PC/mobile).
- Optimisation du jugement de la langue Grease Monkey.
- Correction de la traduction de fichiers txt.

## 0.10.7

- Support de la souris pour appuyer à nouveau sur Ctrl pour afficher le texte original.
- Ignorer la langue jamais traduite lors du survol de la souris.
- Optimisation des sous-titres bilingues de Youtube.

## 0.10.6

- Support des sous-titres Youtube uniquement pour les traductions.
- Ajout d'une alerte de mise à jour de la version basse de Grease Monkey.
- Correction du problème que les fichiers txt locaux ne peuvent pas être traduits.

## 0.10.5

- Correction de Youtube revenant occasionnellement à la page d'accueil.

## 0.10.4

- Correction du conflit de sous-titres Youtube avec le plugin de sous-titres doubles (Immersive Translate de la traduction des sous-titres Youtube n'est pas activé lorsque le plugin Youtube Dual est détecté pour éviter le conflit).
- Ajout de la [fonction de désactivation permanente des sous-titres vidéo], s'il y a d'autres problèmes de conflit et que vous ne souhaitez pas activer la fonction de sous-titres bilingues avec Immersive Translate.
- Optimisation des sauts de sous-titres.

## 0.10.3

- Correction du problème de traduction de la clé d'authentification personnalisée DeppL.

## 0.10.3

- Support parfait pour les vidéos Youtube avec sous-titres bilingues 🎉.
- Pour les pages d'articles, le texte principal sera maintenant traduit en premier avant le reste du contenu de la barre latérale.
- Optimisation de la contextualisation de la traduction DeepL.
- Optimisation de la traduction OpenAI des fichiers de sous-titres pour la contextualisation.

## 0.10.1

- Augmentation de la priorité de la traduction du corps pour optimiser l'expérience de traduction.
- Correction du problème de texte non traduit en cliquant sur plus de texte ins.

## 0.9.8

- Optimisation de l'expérience, correction de certains bugs.

## 0.9.7

- Correction de la traduction automatique lorsque readwise est mis en surbrillance.

## 0.9.6

- Correction de la suppression du cache en se déconnectant de la connexion de l'utilisateur.

## 0.9.5

- Corrections de bugs des eBooks en ligne.

## 0.9.4

- Optimisation de la détection d'amélioration de l'entrée pour réduire les faux contacts.
- Traduction en ligne des e-books et des sous-titres.

## 0.9.3

- Traduction de la boîte de saisie : affiche un rappel contextuel lors de sa première utilisation, et l'utilisateur peut choisir de le désactiver cette fois-ci ou de manière permanente pour éviter les touches accidentelles.
- Optimisation de la vitesse d'exportation de la traduction uniquement en PDF, si vous choisissez d'exporter uniquement la traduction, vous pouvez directement appeler l'aperçu PDF du système pour exporter, plus rapidement.
- Deeplx prend en charge plusieurs URL, il suffit de les séparer par .

## 0.9.2

- L'outil de traduction PDF est migré vers la version en ligne : https://app.immersivetranslate.com/pdf/ , afin que Grease Monkey et Safari puissent utiliser la traduction PDF, et les problèmes peuvent être mieux itérés sans avoir besoin de publier une version pour résoudre le problème.
- Optimisation de l'UI POPUP, le panneau est plus beau !

## 0.9.1

- Correction des problèmes de nom de fichier lors de la création de livres électroniques Epub

## 0.8.8

- pdf supporte les ajustements de l'espacement des lignes et des mots pour re-reconnaître les paragraphes
- correction du problème de défilement automatique en lecture mobile en ligne epub

## 0.8.7

- pdf supporte uniquement les téléchargements de traduction
- Correction du problème de connexion Google sur safari

## 0.8.2 - 0.8.6

- Permet de définir l'intervalle entre les déclencheurs de combo d'amélioration de saisie
- Correction de quelques bugs

## 0.8.1

- Optimisation de la détection de la langue
- Fonctionnalités Beta : API personnalisée (Beta activée dans les paramètres développeur)
- Support pour la traduction AliCloud
- Correction de quelques bugs

## 0.8.0

- Systèmes d'utilisateurs pris en charge
- Prend en charge [Enable Pro Membership](/pricing), qui permet aux utilisateurs de profiter des traductions Deepl et OpenAI et des paramètres de synchronisation cloud.
- Le service de traduction au survol de la souris peut être configuré individuellement
- Le service de traduction de la boîte de saisie peut être configuré séparément
- Optimisation de la traduction PDF
- Correction de quelques bugs

## 0.7.16

- Traduction PDF avec de nouvelles options pour un contrôle rapide du style de traduction (les fichiers PDF sont très étranges et activer ces options peut être utile pour certains fichiers PDF avec un formatage désordonné)
- Les versions iOS et macOS sont de retour sur l'Apple Store Country Store

## 0.7.15

- Nous avons été informés par Apple que les traductions OpenAI ont été temporairement retirées d'iOS et macOS, et nous essayons de les relancer en Chine.

## 0.7.11- 0.7.14

- Correction : problème de traduction de toutes les régions de Gmail
- Désactivation temporaire de la fonction d'exportation PDF de Safari en raison de la restriction de Safari sur les téléchargements de plug-ins (bug).
- Correction de quelques autres problèmes

## 0.7.10

- Mise à niveau de l'UI du panneau d'icônes du navigateur contextuel, un peu plus de design ～
- Correction du problème que certains passages japonais ne sont pas traduits.

## 0.7.9

- PDF prend enfin en charge l'exportation de versions bilingues ! Vous pouvez cliquer sur le bouton [Enregistrer] pour exporter le fichier PDF bilingue traduit.
- Les règles personnalisées prennent désormais en charge la fusion avec les règles intégrées par défaut, par exemple : `{"id": "youtube", "selectors.add":["#test"]}` signifie ajouter un `#test` aux sélecteurs existants, `selectors` signifie remplacer le défaut, `selectors.remove` signifie supprimer un des sélecteurs par défaut, et `selectors.remove` signifie supprimer un des sélecteurs par défaut.
- Icône Safari mise à jour, un peu plus grande.
- Autres corrections de bugs

## 0.7.8

- Corrections de bugs

## 0.7.7

- Adapté au style système de Safari, l'icône d'extension de Safari est passée à un contour transparent.
- Ajouter un changement de statut de l'icône du navigateur, lorsqu'une page web a été traduite, un ✅ sera ajouté automatiquement en bas à droite de l'icône du navigateur.
- Activer automatiquement la traduction des sites web anglais fréquemment utilisés pour les nouveaux utilisateurs
- Correction des problèmes de traduction avec https://claude.ai/

## 0.7.6

- Support de la traduction des résultats améliorés de saisie ctrl+z Annuler
- Support de la traduction en mode de lecture de documents Flying Book
- Adaptation https://pi.ai/talk

## 0.7.5

- Correction de l'icône Grease Monkey qui ne s'affiche pas
- Correction de plusieurs problèmes

## 0.7.4

- Correction de plusieurs problèmes
- La page de configuration prend en charge la suppression par lot des URL sélectionnées.
- Prend en charge l'activation/désactivation de la traduction des sous-titres Youtube pour éviter les conflits avec d'autres plugins connexes.
- Arigato Translator prend en charge le réglage des champs et de l'identifiant de terminologie

## 0.7.2

- Amélioration de la boîte de saisie : permet d'omettre le préfixe // et de déclencher la traduction de l'ensemble de la boîte de saisie avec 3 espaces, ou vous pouvez désactiver cette option dans la page des paramètres.

## 0.7.1

- Prend en charge l'amélioration de la recherche, lorsqu'elle est activée, lorsque vous effectuez une recherche sur Google/Google News en chinois, la colonne de droite affichera automatiquement les résultats de recherche des mots-clés anglais correspondants, qui est activée par défaut.
  - Raison : Nous avons constaté que dans la recherche Google, les résultats de recherche pour les mots-clés chinois et anglais peuvent être très différents, avec l'amélioration de la recherche traduite immersive activée, nous recherchons automatiquement les mêmes mots-clés en anglais pour vous et les affichons sur le côté droit. Vous pouvez choisir de le désactiver si vous n'avez pas besoin de la fonctionnalité.
  - Safari n'est pas pris en charge en raison des limitations de l'API.

## 0.6.20

- Modifier les paramètres par défaut : En raison d'un grand nombre de retours d'utilisateurs indiquant qu'ils n'utiliseront pas l'outil de traduction après l'installation, leur attente de l'outil de traduction est qu'il traduira automatiquement les pages web anglaises après l'installation, donc à partir de cette version, pour les utilisateurs chinois, l'option de traduction des pages anglaises par défaut a été activée (si l'utilisateur a déjà défini la langue qui sera toujours traduite, alors elle sera respectée, et le changement ne modifie que les paramètres initiaux de l'extension), et il doit être annulé, il peut être facilement annulé dans [Panneau contextuel ou page des paramètres](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- Correction des bugs PDF
- Correction du bug du web of science
- Adaptation feeder.com
- Correction de l'epub ne traduisant pas certains livres

## 0.6.18

- Correction du problème de débordement de largeur de la fenêtre contextuelle Safari.
- Optimisation du processus de construction

## 0.6.17

- Optimiser les alertes d'erreur
- Optimiser la sélection de la langue cible, maintenant elle n'affichera que les langues prises en charge par le service de traduction correspondant
- Optimisation de la traduction PDF
- Adapté pour le site Good Reads, Amazon et le site South China Morning Post

## 0.6.16

- Ajouter l'affichage de la page sans autorisation PDF
- Réparer l'affichage des paragraphes de la liste de texte PDF
- Agrandir le redimensionnement des petites polices PDF sur chrome et safari

## 0.6.15

- Réparer le problème que lors de l'ouverture de fichiers PDF, le panneau d'extension indique qu'il n'y a pas d'autorisations.
- Correction du problème que l'amélioration de la boîte de saisie n'est pas activée lorsque le site est configuré pour ne jamais traduire.

## 0.6.14

- Optimisation de la traduction PDF, la zone de traduction peut maintenant être éditée/traînée/supprimée
  - Traîner en haut à gauche, supprimer en haut à droite, changer la taille en bas à droite
- Alignement à gauche de la boîte déroulante Windows
- Prend en charge le chinois traditionnel et le chinois simplifié

## 0.6.13

- Correction du problème de traduction répétée au survol de la souris
- La traduction PDF prend en charge le glisser pour changer la taille et éditer le contenu de la traduction

## 0.6.12

- Correction des images de traduction Epub devenant plus petites dans certains navigateurs
- Optimisation de la traduction de la boîte de saisie, fonctionne maintenant sans problème dans Bard !

## 0.6.10

- Le modèle par défaut OpenAI est passé à la version 0613
- Correction de certains styles de boîte de saisie
- Plus intelligent pour déterminer s'il s'agit d'une zone de navigation, et si c'est le cas, aucune traduction n'est effectuée
- Correction des attaques possibles par injection XSS

## 0.6.8

- Le panneau d'extension peut maintenant indiquer les pages non prises en charge (par exemple, les pages sans autorisations et les pages non-HTML)
- Amélioration de la boîte de saisie pour afficher le statut de chargement dans la traduction
- Mettre à jour les couleurs de chargement par défaut dans les traductions
- Lorsque la boîte de saisie est configurée sans préfixe, elle prend en charge la traduction `ja Hello` en japonais et `English Hello` en anglais.

## 0.6.6

- Correction pour : certaines zones ne se traduisant pas (quora)

## 0.6.5

- Optimisation de Google Bard
- La traduction de la boîte de saisie prend en charge la traduction directe de l'ensemble de la boîte de texte sans préfixes.
- Optimiser le problème des traductions OpenAI ajoutant des points de manière insensée, (si aucun point n'est détecté dans le texte original, si openai renvoie un point, alors le supprimer)
- Problèmes avec les fichiers de sous-titres safari non reconnus

## 0.6.3

La langue par défaut pour la traduction de la boîte de saisie peut maintenant omettre l'espace, c'est-à-dire que //Hello World peut également être traduit.

## 0.6.2

La plus excitante amélioration de la boîte de saisie est ici :

- Tapez : // Hello World dans la boîte de saisie sur n'importe quelle page web, puis cliquez trois fois sur la barre d'espace pour traduire le paragraphe en anglais
- Vous pouvez également spécifier la traduction dans une certaine langue : /ja Hello World, puis cliquez trois fois sur la barre d'espace pour traduire le paragraphe en japonais

[Cliquez ici pour une introduction rapide de 30 secondes](/docs/input/)

## 0.6.0

- Première version en juin, migrée de l'ancien sous-domaine personnel https://immersive-translate.owenyoung.com vers le nouveau domaine https://immersivetranslate.com/
- La fonctionnalité est en grande partie inchangée (de nouvelles fonctionnalités seront disponibles dans la prochaine version !)

## 0.5.17

- Correction du problème que : les livres électroniques bilingues n'ont pas d'images après l'exportation

## 0.5.16

- Correction : problème de traduction openai en chinois traditionnel

## 0.5.15

- Optimisation : Le nombre minimum de caractères dans un paragraphe qui déclenche la traduction a été modifié à un minimum de 4 caractères pour réduire la confusion, tout en utilisant d'autres fonctionnalités pour éviter de traduire les zones de navigation et de fin du site.
- Correction : les détails de Github ne se traduisent pas après l'expansion.

## 0.5.14

- Correction du problème que les images sur certaines pages web de : deviennent plus grandes après la copie
- Correction : la section des commentaires de medium ne se traduit pas
- Correction du problème que les images sur certaines pages de : ont été copiées incorrectement

## 0.5.12

- Fonctionnalité : Le style de traduction de ligne de séparation ajoute une ligne de séparation verticale pour les traductions sur une seule ligne
- Correction : Cas très rares de fractionnement de paragraphe.
- Une excellente page d'orientation de première configuration pour les nouveaux utilisateurs iOS.

## 0.5.11

- Support de la traduction des sous-titres pour l'exportation des traductions uniquement
- Correction : certains éléments ne sont pas reconnus par le survol de la souris
- Correction : les sauts de ligne de tweet partiels ne sont pas reconnus
- Correction : le style de création de livres électroniques ne fonctionne pas

## 0.5.10

- Correction : les sauts de ligne de tweet ne sont pas reconnus
- Correction : la page de détail de Reddit renvoie certains paragraphes qui ne peuvent pas être traduits
- Correction d'un problème avec : où certaines balises de code n'étaient pas reconnues correctement.

## 0.5.9

- Corrige les sauts de paragraphe dans certains cas à :
- Correction : Tampermonkey Toggle n'affiche que les traductions
- Correction : problème de style de lecture en ligne d'eBook

## 0.5.8

- Correction du problème : la durée de traduction temporaire du site web ne prend pas effet.

## 0.5.7

- Super mise à jour !

- La fonctionnalité "Afficher uniquement les traductions" est là ! Cliquez sur [Plus] -> [Basculer pour afficher uniquement les traductions].

  - Prise en charge des raccourcis personnalisés, à définir dans les paramètres d'interface -> Paramètres des raccourcis

- Optimisation du problème de limitation de fréquence des requêtes OpenAI

- ChatGPT par défaut sur le modèle mobile, qui est plus rapide !

- Réusinage de l'analyse du noyau web, ce qui signifie :

  - Traduction de pages web à grande échelle en quelques secondes
    - Par exemple : https://pve.proxmox.com/pve-docs/pve-admin-guide.html, qui prenait 30 secondes auparavant, est maintenant retourné en quelques secondes.
  - Utilisation ultra-faible de la mémoire pour les pages web complexes
    - Par exemple : https://www.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Adaptation à plus de sites web

- Toutes les traductions du site web de ShadowRoot sont prises en charge.

  - Par exemple : https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - Par exemple, la section des commentaires de : https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Correction du problème d'écran blanc après la traduction de sites web avec hydratation tels que Next.js.

  - Par exemple : https://webpack.js.org/

- Correction du problème où la modification du raccourci de survol de la souris nécessitait un rafraîchissement de la page pour prendre effet

- Correction d'un problème de reconnaissance des sauts de ligne dans les fichiers TXT.

- Beaucoup de mises à jour !

- La fonctionnalité "Afficher uniquement les traductions" est arrivée ! Cliquez sur "Plus" -> "Basculer pour afficher uniquement les traductions".

  - Prend en charge les raccourcis personnalisés, qui peuvent être définis dans "Paramètres de l'interface" -> "Paramètres des raccourcis"

- Optimisé pour le problème de limitation de taux de requêtes OpenAI

- L'analyse du noyau web a été reconstruite, ce qui signifie.

  - Traduction instantanée pour les grands sites web
  - Utilisation minimale de la mémoire pour les pages web complexes
  - Meilleure compatibilité avec plus de sites web

- Prend désormais en charge les traductions pour tous les sites web avec ShadowRoot.

- Correction du problème d'écran blanc après la traduction de sites web avec hydratation, tels que Next.js

- Correction du problème où le changement du raccourci de survol de la souris nécessitait un rafraîchissement de la page pour prendre effet

- Correction du problème de reconnaissance des sauts de ligne dans les fichiers TXT.

## 0.5.6

- Correction : problème de popup de nouvel onglet sur macOS.
- Fonctionnalité : Nouvelle page de guide pour les nouveaux utilisateurs.

## 0.5.5

- Correction : problème de zone de survol de la souris.

## 0.5.4

- Correction : Page Spa dupliquée

## 0.5.3

- Correction : écouteur de raccourci de survol de la souris.
- Correction : traduction de document PDF
- Fonctionnalité : Ajouter une nouvelle page de guide client

## 0.5.2

- Correction : paramètres de raccourcis de survol de la souris pour userscript

## 0.5.1

- Correction : OpenAI API ne fonctionne pas.

## 0.5.0

- Fonctionnalité : Traduire le paragraphe actuel lors du survol de la souris.
- Fonctionnalité : Réusinage de la traduction PDF, vous pouvez maintenant traduire la plupart des PDF avec Immersive Translate
- Correction : Désactiver le menu contextuel ne fonctionne pas [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Correction : Éviter la politique de sécurité de contenu pour [Mastondon](https://mastodon.social/)

## 0.4.11

- Correction : permission userscript (uniquement pour userscript).

## 0.4.8

- Fonctionnalité : Bing Translate vers Microsoft Translate pour une qualité plus stable.
- Correction : Page web pure TXT comme [celle-ci](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Performance : Exclure certaines pages publicitaires enfant sur le site web, et la performance s'est améliorée un peu

## 0.4.7

- Correction : popup manquant pour Userscript Firefox.

## 0.4.6

- Fonctionnalité : Permettre à des tiers d'envoyer un événement de document pour appeler `toggleTranslatePage`
- Fonctionnalité : l'application iOS ajoute un bouton d'activation de l'extension et un lien vers les communautés
- UI : le modèle de champ de paramètres OpenAI utilise une sélection au lieu d'une boîte de saisie de texte.

## 0.4.5

- Correction : problème d'extension safari iOS 15.0.
- Correction : raccourcis d'extension safari macOS
- Correction : popup de politique de sécurité de contenu pour l'extension, et en partie pour userscript.

## 0.4.4

- Tâche : Supprimer console.log

## 0.4.3

- Correction : détection d'espace blanc pour les balises sup, sub.
- Fonctionnalité : supporte le site web ChatGPT Plus comme service de traduction, c'est une fonctionnalité bêta, vous pouvez y accéder en activant la fonctionnalité bêta dans les paramètres développeur. C'est très lent, car chatgpt ne peut envoyer qu'une requête à la fois. Assurez-vous d'avoir un compte ChatGPT Plus, car il y a plus de limites sur le compte gratuit, et je ne suis pas sûr si cela présente un risque pour votre compte, soyez prudent pour vous assurer d'avoir un compte ChatGPT Plus, car il y a plus de limites sur le compte gratuit, et je ne suis pas sûr si cela présente un risque pour votre compte, soyez prudent pour l'utiliser.

## 0.4.1

- Correction : le menu contextuel de Firefox disparaît après le redémarrage.
- Support Azure openai

## 0.4.0

- Fonctionnalité : Supporte la traduction de fichiers de sous-titres locaux (.srt, .ass, etc.)

## 0.3.17

- Fonctionnalité : Supporte la traduction de fichiers .txt locaux.
- Correction : le menu contextuel peut ne pas être disponible parfois. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Correction : garder &nbsp; comme espace blanc.
- Suppression : Retirer Papago, car [le service est en panne](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI : permettre l'absence de clé API pour openai
- UI : permettre à Open AI de réinitialiser les paramètres par défaut

## 0.3.14

- Dépendance : Mettre à jour pdf.js vers la dernière version
- Correction : couleur de fond de sélection pdf
- Correction : détection d'espace blanc

## 0.3.13

- Correction : problème de caractère spécifique du constructeur d'ebook, comme certains chemins de chapitre sont `xxx' xxxx`.
- UI : plier les options personnalisées openai par défaut.
- UI : Ajouter un statut d'exportation pour l'exportation epub.
- Correction : invite par défaut Gpt4

## 0.3.12

- Fonctionnalité : Nous pouvons maintenant personnaliser la couleur de fond du thème de traduction du marqueur.
- Correction : postMessage lors de l'initialisation de la page a cassé certains sites, maintenant nous le ferons seulement lorsque nous traduisons vraiment des pages
- Correction : problème de progression de l'ebook.
- Correction : meilleur pour diviser un long paragraphe, 1,5 milliard, 25,5%, M. ne sera pas considéré comme une limite

## 0.3.11

- Correction : couleur du texte en mode sombre du lecteur d'ebook
- Correction : invite openAI

## 0.3.10

- Meilleur : détecter le conteneur japonais/coréen.
- Correction : Progression du constructeur d'ebook arrêtée à 99%.

## 0.3.9

- Correction : l'état d'entrée des services de traduction de l'UI des options ne change pas.

## 0.3.8

- UI : couleur de chargement plus transparente
- Correction : Détecter la langue de l'ebook.
- Fonctionnalité : Ajouter la progression de la traduction pour le constructeur d'ebook, et un beau confetti après le succès.
- Fonctionnalité : Ajouter un bouton de réessai pour tous les paragraphes échoués.
- Correction : Gestion des erreurs Deepl

## 0.3.7

- Correction : le lecteur d'ebook ne peut pas charger les images sur Chrome.

## 0.3.6

- UI : meilleure interface utilisateur pour la page ebook

## 0.3.5

- Correction : exportation d'ebook userscript
- Fonctionnalité : ajouter un point de terminaison API personnalisé pour OpenAI
- Fonctionnalité : ajouter des options de temps de traduction temporaire du site web dans `Paramètres avancés`

## 0.3.4

- CI : Échec de la construction

## 0.3.3

- Correction : constructeur d'ebook pour Kindle
- Changement : couleur de l'icône de chargement, du noir au bleu, pour s'adapter à la page web en mode sombre.
- Fonctionnalité : Supporte la traduction html locale pour l'extension

## 0.3.2

- Correction : déplacement du curseur de saisie du formulaire d'options.
- Fonctionnalité : OpenAI supporte l'apiUrl personnalisé pour les paramètres de développement.

## 0.3.1

- Fonctionnalité : mise à jour de l'icône sombre à la transparence.
- Correction : ordre incorrect pour un long paragraphe

## 0.3.0

- Version : À partir de maintenant, nous changerons le numéro de version mineure une fois par mois, par exemple, maintenant en mars, la version commencera à partir de 0.3.0, en avril, le numéro de version commencera à partir de 0.3.0, en avril, le numéro de version commencera à partir de 0.4.0, l'année prochaine en avril, le numéro de version sera 1.4.0, et ainsi de suite. Cela est dû au fait qu'il n'est pas logique pour les extensions de suivre Cela est dû au fait qu'il n'est pas logique pour les extensions de suivre les sémantiques, mais standardiser les numéros de version selon les lois du temps est une motivation pour le développement de continuer à se mettre à jour, et pour les utilisateurs de trouver plus facilement des problèmes.
- Fonctionnalité : Supporte l'icône sombre pour firefox

## 0.2.86

- Ajouter une option de longueur de texte maximale par requête avec Open AI
- Correction : identifiant d'ebook dupliqué
- Fonctionnalité : Supporte la traduction de pages web txt

## 0.2.85

- Correction : certains fichiers epub ne peuvent pas être trouvés.

## 0.2.84

- Fonctionnalité : Supporte le lecteur et le créateur d'ebook

## 0.2.83

- Fonctionnalité : Permettre au formulaire de saisie de mot de passe d'afficher le mot de passe.

## 0.2.82

- Correction : Certains sites utilisent `span` pour les styles, donc nous utilisons `font` au lieu de span pour l'enveloppe de la cible de traduction
- Correction : limite maximale de tokens OpenAI, changer le nombre maximum de caractères de 1500 à 1300.

## 0.2.81

- Correction : m.youtube.com
- Correction : formulaire d'options UI
- Correction : invite Open AI
- Fonctionnalité : Supporte plusieurs clés OpenAI, utilisez `,` pour les séparer.

## 0.2.80

- Fonctionnalité : Ajouter un menu Activer/Désactiver pour le popup -> plus
- Correction : Conflit de message DingTalk

## 0.2.79

- Correction : Open AI pour le paragraphe d'espace

## 0.2.78

- Fonctionnalité : supporte OpenAI CHATGPT 3.5 (supporte l'interface OpenAI ChatGPT 3.5)
- Fonctionnalité : Ajouter un nouveau thème Solid Border (nouveau thème ajouté, bordure pleine)

## 0.2.77

- Correction : erreur de balise de code multiple.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Correction : erreur de balise de code multiple [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Fonctionnalité : Supporter le nombre de textes de traduction immédiate personnalisée pour différents services de traduction.

## 0.2.74

- Fonctionnalité : Supporter Tencent (alpha)
- Correction : traduction openai
- Correction : vérification des balises inconnues en ligne

## 0.2.73

- Fonctionnalité : Supporter le thème de traduction Grey
- Correction : Page des tendances Github

## 0.2.72

- Correction : problème de réseau de vérification du service de traduction sur Firefox mobile.

## 0.2.71

- Correction : permission du userscript Open AI

## 0.2.70

- Correction : espace réservé Open AI

## 0.2.69

- Fonctionnalité : Supporter Open AI en tant que service de traduction.
- Fonctionnalité : Supporter la vérification du service de traduction sur options.html
- Fonctionnalité : Supporter le cadre principal personnalisé car certains sites n'utilisent pas le corps comme cadre principal

## 0.2.68

- Supporter Caiyun (Alpha)
- Correction des balises de bloc inconnues

## 0.2.67

- Fonctionnalité : Ajouter `<all>` pour toujours traduire les langues, vous pouvez maintenant l'utiliser pour traduire toutes les langues sauf la langue cible, et ne jamais traduire les langues
- Correction : Permettre la configuration de l'API Google personnalisée
- Amélioration : Support gratuit de Deepl
- Correction : utilisation élevée de la mémoire pour les userscripts et les extensions (en supprimant opencc zh-CN à zh-TW, remplacé par Google translate)
- Correction : Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Correction : configuration de la traduction Azure mais toujours affichée (besoin de configuration)

## 0.2.66

- Correction : échec de la traduction de fichiers PDF, bug de la version 0.2.60 pour supporter deepl de zh-CN à zh-TW

## 0.2.65

- Supporter la limitation des requêtes pour plusieurs cadres
- Ne pas traduire le titre de la page lorsqu'il est dans un iframe

## 0.2.64

- Correction : choix des services de traduction openl
- Fonctionnalité : Supporter l'option de traduction du titre

## 0.2.63

- Fonctionnalité : Supporter le service de traduction Azure
- Fonctionnalité : Supporter le service de traduction Papago
- Correction : synchronisation native de Google Drive sur Firefox Android.
- Correction : changement de la transparence de 0.4 à 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Correction : conseils de raccourcis dans le popup
- Performance : requêtes en série à cocurrence
- Meilleure détection du nombre de caractères japonais

## 0.2.62

- Fonctionnalité : Ajouter la règle waitForSelectors, pour corriger certains sites comme reddit

## 0.2.61

- Correction : userscript trop volumineux pour greasy fork
- Amélioration : réduction de la taille du fichier

## 0.2.60

- Fonctionnalité : Supporter zh-CN à zh-TW pour Deepl
- Fonctionnalité : Fonctionnalité Deepl Immersive Translate
- Fonctionnalité : Supporter le zoom de la taille de police personnalisée
- Correction : style du forum Steam
- Correction : style global non modifié après la génération d'éléments dynamiques
- Correction : promotion de la priorité d'exclusion
- UI : changement de la page à propos
- Correction : certains éléments mathématiques restent originaux

## 0.2.59

- Correction : élément de bloc de balises inconnues
- Correction : élément translate=no surchargé
- Correction : correspondance d'URL avec plusieurs \*

## 0.2.58

- Fonctionnalité : Supporter la couleur de texte de traduction personnalisée, la couleur de bordure.

## 0.2.57

- Pas de changements, reconstruction

## 0.2.56

- Correction de la traduction en double pour les éléments en ligne avec élément de code.
- Correction de la vérification des balises inconnues en ligne/bloc
- Fonctionnalité : support de CSS injecté sur le tableau de bord des développeurs
- Fonctionnalité : suppression de authKey, appid appSecret
- Amélioration : ouverture de la page des paramètres dans un nouvel onglet (mais pas pour Stay)

## 0.2.55

- Essayer de corriger le charset de l'API deepl

## 0.2.54

- Suppression de l'autorisation des onglets pour le rejet du Chrome Store
- Correction de la traduction de la page entière, le pied de page est ignoré
- Ajout de notes à la page à propos
- Supporter l'URL personnalisée à partir de la configuration intégrée

## 0.2.53

- Correction de l'erreur de synchronisation de Google Drive pour userscript.

## 0.2.52

### Code

- Utiliser la dernière version d'esbuild
- Utiliser la dernière version de deno
- CI : soumettre le code source à Firefox

## 0.2.51

- Correction de l'authentification Google nécessitant une connexion sur Chrome/Firefox
- Remplacement des liens de service de traduction
- Meilleure gestion des permissions.
- suppression de la minification.

## 0.2.50

- Correction du problème de téléchargement de Google Drive (vraiment) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Suppression des raccourcis alt+d, alt+s car ils peuvent entrer en conflit avec les raccourcis natifs.
- Correction du problème de téléchargement de Google Drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Meilleure vitesse, en ajoutant minLength à 50 pour la détection de la langue.
- Correction de la validation du jeton Google Drive.

## 0.2.47

- Correction de l'API deepl

## 0.2.46

- correction de la marque de bloc

## 0.2.45

- Correction de l'élément innerText indéfini
- Correction de la traduction caiyun langue source indéfinie

## 0.2.44

- Correction du basculement du masque userscript
- Correction de la logique de basculement du masque

## 0.2.43

- Correction du basculement du masque userscript avec événement tactile.
- Correction de la vitesse (en supprimant sleep(300))

## 0.2.42

- Correction du survol du masque lors du basculement du masque à nouveau.
- Ajout de raccourcis de masque pour mobile
- Correction du problème de synchronisation cloud userscript
- Déplacement de la page des options avancées vers le menu de gauche.
- Ajout de la logique de réessai au service de traduction

## 0.2.41

- Correction de la traduction niu userscript
- Correction de la traduction xhtml

## 0.2.40

- Correction de l'affichage des fonctionnalités bêta
- Correction de la page de paramètres du popup sur la nouvelle page d'onglet
- Correction du remplacement de l'espace réservé de traduction

## 0.2.39

- Supporter les raccourcis pour afficher la traduction du masque
- Supporter l'activation des fonctionnalités bêta sur le panneau de développement
- Correction des raccourcis dans l'extension mobile

## 0.2.38

- Supporter le thème de chargement
- Correction de getpocket.com
- Correction du pied de page pour la zone du corps
- Correction de l'icône d'import/export

## 0.2.37

- Correction de la marque d'exclusion de cadre

## 0.2.36

- Supporter la synchronisation avec Google Drive

## 0.2.35

- Correction de l'ignorance des balises rb, rt japonaises.
- Meilleure interface utilisateur du popup
- Meilleurs conseils pour les mauvais userscripts
- Ajout de la contribution à la page à propos
- Correction de la traduction volc pour la détection automatique de la langue

## 0.2.34

- Correction de la vitesse de traduction de plusieurs langues

## 0.2.33

- Supporter le mode d'écriture vertical, comme le japonais.
- Ajout de 3 thèmes
- Ajout du service de traduction Niu

## 0.2.32

- Correction de la traduction de base des PDF
- Correction de la sélection du service non configuré dans le popup, aller à la page des options.
- Correction de l'ouverture des paramètres.
- Correction de la vitesse de détection de plusieurs langues

## 0.2.31

- Correction de l'injection CSS dans les iframes dynamiques

## 0.2.30

- Supporter la traduction des iframes en ligne userscript.
- Supporter la traduction shadowroot. Par exemple :
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Zone de conversation.
- vérifier également la règle de synchronisation sur le popup

## 0.2.29

- Correction de la traduction Facebook
- Supporter l'option de menu contextuel.

## 0.2.28

- Suppression de la correspondance non standard pour userscript

## 0.2.27

- Supporter la traduction des iframes en ligne. (Seulement pour l'extension, non disponible pour
  userscript)
- Correction de la traduction de plusieurs langues

## 0.2.26

- Correction de l'addon Firefox Android
- Ajout de paramètres avancés pour la nouvelle ligne de traduction

## 0.2.25

- Supporter la traduction des iframes, comme QQ mail, tweet intégré.

## 0.2.24

- Ajouter un site de traduction temporaire pour un moment
- Correction de l'API du navigateur userscript stay.app
- Correction de la page des options stay.app

## 0.2.23

- Correction de la traduction de pages en plusieurs langues

## 0.2.22

- Correction de la construction du userscript

## 0.2.21

- Correction de la traduction en ligne de PDF sur Firefox

## 0.2.20

- Correction du problème de requête macaque
- Correction de la hauteur de ligne de surlignage

## 0.2.19

- Correction du japonais intelligent de Tencent
- Correction du navigateur haikuo world

## 0.2.18

- Correction du changement d'URL client, rester automatiquement dans l'état de traduction.
- Suppression du conteneur latéral en tant que conteneur de traduction.
- Réorganisation de la position du popup.

## 0.2.17

- Changement de surlignage à marquer
- Ajout du thème de traduction surligné

## 0.2.16

- Compatibilité Macaque

## 0.2.15

- Correction du problème de rebond tactile

## 0.2.14

- Correction de safari globalThis.GM ne fonctionnant pas

## 0.2.13

- Supporter le glissement du popup Userscript
- Supporter trois doigts sur l'appareil tactile pour déclencher le basculement des pages de traduction
- Supporter la dissimulation de l'icône du popup userscript.

## 0.2.12

- Meilleur pour inoreader

## 0.2.11

- Correction
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas archive Le contenu principal de la page n'a pas pu être traduit

## 0.2.10

- Correction de la distance de hauteur de ligne PDF

## 0.2.9

- Correction des éléments d'exclusion de marque
- Correction de la vérification du type deno
- suppression de importmap
- Correction des menus contextuels de traduction
- restauration de la page lorsque ne jamais traduire ce site est activé
- Ajout de la description pour ajouter une URL

## 0.2.8

- Détecter la langue de l'agent utilisateur pour la langue de l'interface
- Correction du bug de saut de ligne.

## 0.2.7

- Correction de la requête grease monkey

## 0.2.6

- Correction
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  problème de correspondance d'URL de fichier

## 0.2.5

- augmentation de la version pour le test ci

## 0.2.4

- capture de l'erreur de connexion de message pour le popup.

## 0.2.3

- Correction du problème
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  création de contexte plusieurs fois

## 0.2.2

- Correction du fichier d'exemple PDF
- Correction du fichier local pdf sur Firefox
- Correction des raccourcis pdf

## 0.2.1

- Support du gestionnaire de raccourcis Grease Monkey.
- Correction de l'expression régulière de correspondance
- Correction des commentaires YouTube.
- Correction de la version compacte mobile de Reddit
- Correction du problème de traduction en texte intégral

## 0.2.0

- Correction des deux colonnes PDF.
- Correction du bug de la version Chrome/Edge Store.
- Correction du problème
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Publication sur l'addon Firefox
- Publication sur Edge
- Correction de la marge pdf.
- Changement du fichier d'exemple pdf

## 0.0.62

- Correction du format pdf, indentation.
- Correction de la prévention du changement d'élément sur telegra.ph

## 0.0.61

- Correction de la fermeture de l'élément span.
- Correction de la permission pour les navigateurs anciens

## 0.0.60

- Correction du PDF Chrome

## 0.0.59

- Support initial pour PDF

## 0.0.58

- Modification de la description du thème de traduction

## 0.0.57

- Changement de l'interface utilisateur du popup, pour une utilisation plus facile

## 0.0.56

- Correction du timeout de Chrome
- Correction de l'erreur de séparation des phrases.

## 0.0.55

- Correction de l'affichage des éléments avec display none.
- Refactorisation du marquage des éléments

## 0.0.54

- Support du saut de ligne pour X caractères.

## 0.0.53

- Utilisation de sendMessage au lieu de connect, car Chrome déconnectera le port après
  5 minutes
- Meilleure détection des conteneurs de texte

## 0.0.52

- Ne pas traduire le paragraphe qui ne contient que des éléments de remplacement, par
  [exemple](https://github.com/nank1ro/solidart), la première ligne.
- Meilleure détection des éléments enfants.

## 0.0.51

- Correction du problème de cache
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7)
- Correction de la taille de la police de l'interface utilisateur des options

## 0.0.50

- Correction de la traduction des images bloquées.

## 0.0.49

- Correction de l'extension Firefox

## 0.0.48

- Correction de l'extension Chrome

## 0.0.47

- Réécriture du message avec l'arrière-plan, utilisation de connect au lieu de sendMessage
- Ajout du support mobile Reddit
- Correction de l'espace blanc préformaté pour certains articles

## 0.0.46

- Formatage des informations méta du userscript

## 0.0.45

- Le userscript utilise un seul fichier.
- Ajout d'un timeout pour la requête de cache

## 0.0.44

- Correction de l'erreur de séparation Tencent.
- Correction de l'erreur de l'élément sup en ligne.
- Meilleur support pour Twitter

## 0.0.43

- Correction du saut de ligne dans les tweets
- Correction de la traduction globale.

## 0.0.42

- Correction de la balise BR
- Traitement des balises de bloc selon les règles

## 0.0.41

- Correction de la vérification des éléments en ligne
- Ajout de l'option de journal de débogage pour les développeurs

## 0.0.39

- Correction du service de traduction contenant mock2

## 0.0.38

- Support du résultat de cache pour le userscript
- Ajout de l'interface utilisateur des options
- Support de la détection de plus de conteneurs de contenu

## 0.0.37

- Correction du changement de service de traduction dans le popup qui ne fonctionne pas
- Correction de la traduction du contenu des publications mobiles Reddit.

## 0.0.36

- Correction des caractères spéciaux de Wikipedia
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Correction de la taille de l'icône du userscript.
- Activation de tous les sites pour détecter la langue des paragraphes.

## 0.0.35

- Correction de la navigation vers la page suivante sur YouTube
- Support de la page de recherche YouTube.
- Correction de l'interrupteur avancé des options.
- Correction de la balise img, balise cachée
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Correction du rafraîchissement forcé de la recherche Google
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Support du résultat de tableau de Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Correction du blanc de Wikipedia
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Changements Importants

- La touche de raccourci par défaut pour basculer la traduction a été changée en `alt+A`, car
  c'est la touche la plus pratique à taper.

### Autres

- Support du mode de traduction immédiate, pour que vous puissiez laisser la page web se traduire
  aussi rapidement que possible.
- Support de la définition de la zone de la page à traduire, pour que vous puissiez traduire plus de zones.
- Support de la définition du nombre de premiers caractères à traduire immédiatement.
- Correction de la traduction en double lors du changement de traduction
- Meilleure interface utilisateur du popup

## 0.0.33

- Support de plus de langues, zh-TW, en

## 0.0.32

- Correction de la traduction du fichier local après enregistrement. Correction
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Ajout du fichier js dist au dépôt public

## 0.0.31

- Support de la traduction de la page entière
- Support de la traduction immédiate de la page
- Plus d'interface utilisateur de configuration
- Réflexion du thème
- Ajout d'une nouvelle icône
- Ajout d'un nouveau thème de traduction dashedBorder

## 0.0.30

- Meilleur support pour le thème en pointillés

## 0.0.29

- Correction de la validité du paragraphe.
- Ajout des thèmes dotted, thinDashed
- Meilleur support pour les thèmes en pointillés, surlignés

## 0.0.28

- Correction du soulignement
- Ajout des thèmes en pointillés, papier
- Correction de la détection de l'en-tête

## 0.0.27

- Support du translationTheme

## 0.0.26

- Correction de la permission de connexion du userscript volc alpha.
- Correction de la version cliquable.

## 0.0.25

- Support de selectorMatches, pour que nous puissions maintenant correspondre à tous les manstondon.
- Correction de l'erreur du userscript Firefox.

## 0.0.23

- Meilleure détection du chinois
- Correction du problème innerText de Reddit

## 0.0.22

- Support de deeplx
- Correction de la traduction multiple lors du changement de service

## 0.0.21

- Correction de certains tags span qui sont des éléments de bloc

## 0.0.20

- Support de la non-traduction des hashtags comme #hash, des tags @ comme @xxx, $tag, comme $APPL
- Support des éléments de bloc

## 0.0.18

- Support de deepl, bing, baidu, youdao, volc, openl, caiyun.

## 0.0.13

- Support du userscript

## 0.0.4.8

- Correction de l'ordre du code.
- Support de l'interface utilisateur de base du popup

## 0.0.4.6

- Support de la vérification de la nouvelle version

## 0.0.3

- Support des fichiers locaux

## 0.0.2

- Support des éléments dynamiques
- Support de la traduction visible
