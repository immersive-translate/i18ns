---
sidebar_position: 6
---

# Journal des modifications

Ce journal des modifications est mis à jour en fonction de l'avancement du développement. La date après la version est la date de fusion du code, et non la date de Release dans les magasins d'applications (le temps de révision varie après la soumission à chaque magasin d'applications, certains prenant jusqu'à une semaine pour la révision). Actuellement, nous avançons deux versions.

La **version Release** est la version stable officielle, disponible sur les principaux magasins d'applications tels que [Chrome](https://chromewebstore.google.com/detail/bpoadfkcbjbfhfodiogcnhhhpibjhbnh), [Edge](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg), [Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate/), [Apple](https://apps.apple.com/app/id6447957425), etc.

La **version Preview** est publiée plus fréquemment et inclut certaines fonctionnalités expérimentales. Comparée à la version Release, elle peut contenir plus de bugs. Elle est principalement publiée sur

- [le userscript du site officiel](https://download.immersivetranslate.com/immersive-translate.user.js)
- [version bêta dans le magasin Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate-beta/)
- [Github Release Assets](https://github.com/immersive-translate/immersive-translate/releases)

## 1.15.9 Release (2025-03-23)

- Correction : Un problème où la traduction ne fonctionnait pas dans Safari 16.4.

## 1.15.8 Release (2025-03-20)

- Correction : Un problème où le raccourci de traduction au survol ne fonctionnait pas sur les appareils prenant en charge à la fois la souris et le tactile.
- Ajout : Prise en charge de la traduction du grand modèle Youdao Ziyue.

## 1.15.7 Release (2025-03-19)

- Ajout : Pré-traduction dynamique du contenu à traduire lors de la navigation sur les pages.
- Correction : Un problème où le service de traduction AI produisait incorrectement du chinois simplifié lors de la traduction du chinois traditionnel.
- Correction : Un problème avec la traduction au survol ne fonctionnant pas en mode "Traduction d'abord, texte original ensuite".
- Correction : Problèmes de compatibilité avec le mode "Traduction uniquement" lorsqu'il est utilisé avec des plugins de lecture comme Reader View.
- Optimisation : Amélioration de la qualité du service de traduction AI pour le contenu principal.
- Optimisation : Amélioration de la prise en charge de la traduction d'images sur certains sites web.
- Optimisation : Optimisation du formatage du texte mixte chinois et anglais.
- Optimisation : Le service de traduction Gemini prend en charge l'invite système personnalisée (System Prompt).
- Optimisation : Amélioration de la vitesse du userscript.

## 1.15.2 Release (2025-03-02)

- Ajout : Gemini prend en charge le portugais (Brésil).
- Ajout : Services de traduction Grok, Ollama, Groq, Azure-OpenAI.
- Correction : Problème de traduction des sous-titres dans Google Meet et Microsoft Teams.
- Correction : Problème de traduction Google avec les caractères d'échappement.
- Optimisation : Amélioration de la précision de l'identification automatique de la langue du contenu traduit.
- Optimisation : [Traduction d'image gratuite] prend en charge le formatage pour les langues de droite à gauche.
- Optimisation : Compatible avec les modèles comme o1, o3 qui ne prennent pas en charge le rôle système (le paramètre de rôle système ne sera pas passé lorsque la configuration de l'invite système est vide).

## 1.14.16 Release (2025-02-21)

- Ajout : Deepseek, Gemini, Claude prennent en charge le changement de contexte.
- Correction : La mise à jour des termes n'envoie pas de nouvelle demande de traduction.
- Amélioration : La langue de l'interface ajoute le hongrois.
- Amélioration : Qualité de traduction Google.
- Amélioration : Formatage d'image gratuit.

## 1.14.12 Release (2025-02-19)

- Amélioration : La pause de la traduction efface immédiatement la file d'attente des demandes.
- Amélioration : Filtre le texte indésirable dans le service de traduction deepl.
- Correction : Traduction de la barre latérale invalide dans les paramètres avancés.
- Correction : Problème d'affichage de la traduction personnalisée deepseek.

## 1.14.11 Release (2025-02-18)

- Correction : Erreur `401: Authentication Fails` de la clé API personnalisée DeepSeek.

## 1.14.10 Release (2025-02-17)

- Nouveau : L'adhésion Pro prend en charge le service de traduction DeepSeek (v3).
- Correction : Résolution du problème de dépassement de la taille limite du fichier de configuration utilisateur.
- Amélioration : L'élément du menu contextuel peut être fermé (opéré dans les paramètres avancés).
- Amélioration : Amélioration des capacités de reconnaissance linguistique pour Greasemonkey et Safari sur les pages avec des langues mineures.
- Amélioration : Accès à l'interface de test de la page de paramètres en ligne.
- Amélioration : Amélioration de l'expérience utilisateur de la fonctionnalité d'aperçu de comparaison de contexte.
- Amélioration : Logique de jugement du mode tactile et souris.

## 1.14.8 Release (2025-02-10)

- Correction : Problème où les longs fichiers PDF-Pro n'étaient pas traduits automatiquement.
- Amélioration : Microsoft, Google et Tencent prennent désormais en charge le cantonais.
- Amélioration : La BBC prend désormais en charge les sous-titres.

## 1.14.6 Preview (2025-02-08)

- Correction : Problème où la **traduction au survol de la souris** ne pouvait pas traduire le texte enrichi.
- Amélioration : La version Tampermonkey prend désormais en charge la traduction des sous-titres YouTube.

## 1.14.4 Release (2025-02-07)

- Correction : Problème de détection incorrecte de la langue dans la **boîte de saisie améliorée**.
- Correction : Problème de correspondance intelligente des experts AI dans les services de traduction personnalisés.
- Correction : Problème de synchronisation Google Drive sur certains navigateurs.
- Correction : Problème de traduction des commentaires en direct sur YouTube.
- Correction : Problème de sous-titres superposés dans certaines vidéos YouTube.
- Amélioration : Échec de la traduction de mangas sur des sites comme shonenjumpplus dans le navigateur Safari.

## 1.13.8 Release (2025-01-24)

- Nouveau : La traduction d'image gratuite est désormais disponible (actuellement prise en charge uniquement sur les versions PC des navigateurs Chrome et Edge), accessible via le menu contextuel.
- Correction : Résolution d'un problème où certains contenus étaient manqués lors de la traduction multi-segments dans Gemini.
- Optimisation : Amélioration du chargement des sous-titres YouTube.
- Nouveau : Le service de traduction AI prend désormais en charge le norvégien.

## 1.13.6 Preview (2025-01-17)

- Amélioration : **AI Expert** peut être utilisé avec **AI Context-Aware Translation**.
- Amélioration : **Traduction d'image** est désormais compatible avec weibo.com (pris en charge uniquement sur Chrome et Edge).
- Amélioration : Lorsque la langue de l'interface est définie sur l'anglais, la langue cible par défaut pour la **boîte de saisie améliorée** est changée en chinois.
- Amélioration : Ajout d'une entrée d'évaluation du magasin dans les options **Plus** sur le panneau.

## 1.13.5 Release (2025-01-14)

- Amélioration : Compatible avec le modèle de pensée Gemini 2.0.
- Amélioration : Prend en charge le style gras en mode traduction uniquement.

## 1.13.4 Preview (2025-01-13)

- Ajout : Les membres Pro peuvent désormais utiliser directement le modèle **Zhipu 4 Plus**.
- Amélioration : Traduction Gemini.

## 1.13.1 (2025-01-10)

- Ajout : Lorsque le texte traduit et le texte original appartiennent au même système d'écriture, afficher la traduction en utilisant un style spécialisé.
- Correction : Le problème où la **traduction au survol de la souris** ne fonctionne pas sur certains sites web.
- Amélioration : DeepLx prend désormais en charge l'arabe.
- Amélioration : Amélioration de la reconnaissance de la langue originale. Auparavant, les pages contenant plusieurs langues pouvaient ne pas être traduites, mais maintenant elles le sont correctement.
- Amélioration : Pour Twitter, les traductions de contenu multiligne sont définies pour ne pas s'enrouler par défaut. L'enroulement se produira uniquement lorsque le contenu dépasse 10 lignes ou 1000 caractères. L'enroulement peut être activé via les paramètres **Paramètres avancés** -> **Activer l'enroulement automatique des lignes pour les longs paragraphes**.

## 1.12.8 (2025-01-03)

- Correction : le problème où la page des paramètres iOS 18.3 ne peut pas s'afficher correctement.
- Correction : le manque de lignes vides lors de la traduction de tweets.
- Correction : le problème des nombres décimaux étant forcés à être coupés en ligne lors de la traduction de longs textes.

## 1.12.7 Release (2024-12-30)

- Amélioration : Bing/Google prennent désormais en charge le portugais (Brésil).
- Amélioration : Amélioration des descriptions pour l'interface utilisateur en chinois traditionnel.
- Amélioration : Ajustement de la mise en page pour les langues de droite à gauche dans les panneaux et les pages de paramètres.

## 1.12.6 (2024-12-26)

- Correction : Problème où la fonction de survol de la souris charge le mauvais service de traduction dans certaines conditions.
- Correction : Problème où l'activation temporaire des sous-titres bilingues sur YouTube ne fonctionne pas.
- Correction : Après avoir changé de services de traduction, le service de traduction dans la "**boîte de saisie améliorée**" ne se met pas à jour.
- Correction : Le commutateur "**YouTube Enable Bilingual**" dans la page des paramètres ne fonctionne pas.
- Amélioration : Suppression du modèle gemini-1.0-pro obsolète.

## 1.12.4 (2024-12-13)

- Ajout : **AI Context-Aware Translation** peut améliorer la précision de la traduction de contenu professionnel. (Disponible uniquement pour les membres Pro, pris en charge exclusivement par les modèles OpenAI) **Options** -> **Général** -> **Activer AI Context-Aware Translation**
- Correction : Certains bugs dans l'effet de traduction multiligne sur Twitter.
- Correction : Problèmes avec la traduction de certaines formules en raison du texte enrichi.
- Amélioration : Lors de la traduction sur **x.com**, les vidéos avec sous-titres auront automatiquement des sous-titres bilingues traduits.
- Amélioration : Les vidéos sans sous-titres afficheront une icône de traduction et fourniront une raison pour laquelle la traduction n'est pas possible.

## 1.11.7 (2024-11-25)

- Ajout : Bing/Google prennent désormais en charge le khmer (cambodgien).
- Ajout : Permettre aux fichiers ePub incomplets de continuer la traduction là où ils se sont arrêtés lors de la réimportation.
- Correction : Problème de traduction des images Twitter dans le navigateur Safari.
- Correction : Les raccourcis deviennent inefficaces lors de l'activation ou de la désactivation de la fonctionnalité "**Hover Translation**".
- Amélioration : Amélioration de l'affichage de la traduction bilingue multiligne sur Twitter et Youtube.
- Amélioration : La traduction de texte enrichi est désactivée par défaut en mode bilingue pour améliorer la qualité de la traduction.
- ~~Amélioration : Ajout de l'option de personnalisation de la "**Traduction de la barre latérale et de la barre de navigation**" dans les "**Paramètres avancés**".~~
- Amélioration : Les images ne sont plus traduites en mode "**Hover - traduire immédiatement ce paragraphe**".

## 1.11.4 (2024-11-16)

- Correction : Problème de traduction de formule causé par l'"Amélioration de la traduction Twitter" dans la version 1.11.2.

## 1.11.2 (2024-11-13)

- Correction : Problème où le contenu disparaît après avoir cliqué sur "voir plus" en mode traduction uniquement de Facebook.
- ~~Amélioration : Amélioration de l'affichage des traductions bilingues multiligne sur Twitter.~~
- Amélioration : Mise à jour de l'interface utilisateur de la liste déroulante du service de traduction dans le panneau.

## 1.11.1 (2024-11-05)

- Ajouté : La **traduction des sous-titres** en temps réel peut désormais être activée via la "balle flottante", disponible sur Zoom, Google Meet et Microsoft Teams.
- Corrigé : Problèmes de synchronisation des sous-titres sur YouTube après avoir regardé des publicités.
- Corrigé : Problèmes d'affichage avec le menu de traduction par clic droit dans Safari sur MacOS 15.
- Corrigé : Problèmes avec la fonctionnalité d'annulation Ctrl+Z dans l'**Enhanced input** sur certains sites web.

## 1.10.6 (2024-10-25)

- Corrigé : Problème avec les raccourcis clavier de l'**Enhanced input** qui ne se déclenchaient pas
- Amélioré : Réduction de la taille du package d'installation
- Amélioré : Solution d'affichage des sous-titres Netflix

## 1.10.5 (2024-10-23)

- Ajouté : Afficher un avertissement lorsque la langue source et la langue cible sont identiques
- Corrigé : Problème de traduction des caractères d'espacement dans le texte enrichi [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- Amélioré : Amélioration de l'entrée et de la fonctionnalité de survol de la souris dans les iframes intégrées sur les pages web

## 1.10.2 (2024-10-11)

- Ajouté : Traduction d'image (version Beta)
- Ajouté : Mode Forcer l'activation du support de la souris (Activez cette fonctionnalité uniquement si la fonction de survol de la souris n'est pas disponible sur les appareils tablette) **Paramètres** -> **Paramètres avancés** -> **Forcer l'activation du support de la souris**
- Ajouté : Afficher un message d'erreur lorsque la traduction des sous-titres vidéo échoue
- Corrigé : Problème de traduction du texte enrichi [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163)
- Amélioré : Résolution des problèmes où le bouton de traduction pourrait ne pas fonctionner lors de la traduction de PDF
- Amélioré : Amélioration du rendu des formules traduites
- Amélioré : Liste de sélection des langues

## 1.9.8 (2024-09-28)

- Ajouté : Service de traduction "Zhipu BigModel"
- Supprimé : Modèle "SiliconCloud" qwen1.5-7B-chat (en raison de l'arrêt officiel)
- Corrigé : Résolution du problème de compatibilité de connexion avec le plugin Safari sur macOS 15

## 1.9.7 (2024-09-20)

- Support d'entrée amélioré pour Baidu, Gmail et d'autres champs de saisie
- Support pour l'en-tête de requête anthropic-dangerous-direct-browser-access pour l'API Claude Anthropic
- Support pour le téléchargement de sous-titres à partir de vidéos Hulu, Bloomberg et Domestika
- DeepX prend en charge la traduction de texte enrichi
- Corrigé le problème de non-synchronisation des experts AI personnalisés

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) prend en charge la copie de formules (clic droit sur la formule pour voir le menu de copie)
- Corrigé le problème d'affichage des sous-titres bilingues pour plusieurs vidéos sur la même page Twitter
- Corrigé quelques bugs

## 1.9.3 (2024-09-05)

- L'option pour l'affichage de comparaison bilingue/traduction uniquement a été déplacée vers les paramètres généraux.
- Par défaut, le système se souviendra du mode basculé en cliquant sur l'icône dans le panneau pour l'affichage de comparaison bilingue ou de traduction uniquement. Pour basculer temporairement, cliquez sur "Plus" -> "Passer à l'affichage de traduction uniquement" dans le panneau.
- Par défaut, la traduction du chinois simplifié vers le chinois traditionnel et vice versa utilisera le mode de traduction uniquement, plutôt que le mode de comparaison bilingue.
- Corrigé quelques bugs.

## 1.9.1 (2024-09-03)

- Support pour configurer des exceptions pour les langues et les sites web en mode de contraste bilingue ou de traduction uniquement (configurer dans la page Paramètres -> Paramètres avancés). Par exemple : Si votre mode de traduction par défaut est le contraste bilingue, mais que vous ne souhaitez pas que le chinois traditionnel utilise également le contraste bilingue, vous pouvez ajouter le chinois traditionnel aux langues d'exception pour le contraste bilingue, de sorte que le chinois traditionnel utilisera le mode de traduction uniquement pour la traduction. De même, si votre mode de traduction par défaut est la traduction uniquement, mais que vous souhaitez qu'une certaine langue ou un site web utilise le mode de contraste bilingue, vous pouvez également ajouter cette langue ou ce site web aux langues d'exception.
- Corrigé un problème où la boîte de saisie dans l'interface de message privé de Tiktok était mal traduite
- Corrigé un problème où les bandes dessinées sur Read Comic Online ne pouvaient pas être traduites
- Corrigé un problème où le [Paramètres avancés -> Nombre minimum de caractères requis pour traduire un paragraphe] ne prenait pas effet dans certains cas

## 1.8.4 (2024-08-30)

- Le service de traduction DeepL prend désormais officiellement en charge le chinois traditionnel comme langue cible (auparavant, la traduction en chinois traditionnel avec DeepL impliquait un processus de conversion supplémentaire du chinois simplifié au chinois traditionnel par un tiers).
- Optimisation des performances de traduction de texte enrichi.

## 1.8.3

- Google Meet prend désormais en charge les sous-titres bilingues pour les réunions en direct : Désormais, vous pouvez profiter de la fonctionnalité de sous-titres bilingues dans les réunions Google Meet. Ouvrez simplement le lien de la réunion, activez les sous-titres bilingues dans le panneau de traduction immersive, puis actualisez la page pour en faire l'expérience.
- Ajout de l'option "Signaler les problèmes de traduction de la page actuelle" et de l'option "Activer/désactiver rapidement la balle flottante" dans les options supplémentaires du panneau.
- Après avoir ajusté la position des sous-titres bilingues de YouTube, le système se souviendra automatiquement de la nouvelle position.
- Optimisation de la logique de cache du plugin, maintenant le cache des données de plus de 30 jours est automatiquement effacé.
- Optimisation des blocs de code dans les paragraphes pour une restauration plus précise du texte original.
- Amélioration de la gestion des "mots non traduisibles" dans les paramètres avancés.

## 1.8.2

- Vous pouvez maintenant traduire le texte dans les boîtes de saisie avec le clic droit : Sélectionnez n'importe quel texte dans une boîte de saisie sur une page web, cliquez avec le bouton droit pour choisir traduire, et la traduction immersive traduira automatiquement le texte sélectionné dans la langue cible de la boîte de saisie, ce qui permet de traduire rapidement le texte en langue maternelle dans les boîtes de saisie vers d'autres langues.
- Vous pouvez maintenant signaler rapidement les problèmes de traduction des pages web dans la balle flottante de traduction immersive. Après avoir traduit une page web, s'il y a des problèmes, vous pouvez cliquer sur le bouton [Feedback] sur le côté droit de la balle flottante, remplir la description du problème, et nous le traiterons dès que possible.
- Les fichiers Epub prennent désormais en charge la traduction de texte enrichi (c'est-à-dire en préservant le format du texte original de chaque paragraphe, comme les liens, le gras, etc.)
- Support pour les sous-titres bilingues en temps réel dans les réunions vidéo de la version web de Microsoft Teams (Ouvrez le lien de la réunion Teams, activez les sous-titres bilingues dans le panneau de traduction immersive, puis actualisez)
- Optimisation des sous-titres bilingues pour la version anglaise d'iQIYI (iq.com)
- Fourniture de plus d'articles arXiv avec une mise en page de traduction bilingue optimisée
- En raison des restrictions du site YouTube, le script Chrome Tampermonkey ne prend plus en charge les sous-titres bilingues de YouTube. Veuillez utiliser la [version plugin](https://immersivetranslate.com/).

## 1.8.1

- Corrigé les problèmes de traduction avec le script Tampermonkey SiliconCloud
- La traduction Claude prend désormais en charge le tibétain et permet la configuration du paramètre de température
- La page de détails de l'expert AI affiche les invites utilisées par l'expert
- Les paramètres de raccourci permettent désormais d'attribuer des touches de raccourci uniques pour tout service de traduction
- Optimisation de la détection des traductions d'articles arXiv

## 1.7.9

- Corrigé les problèmes de traduction de texte enrichi pour les services de traduction tels que Google, DeepL (par exemple, les pages affichant directement `<button>` etc.)
- Corrigé le problème où le raccourci bilingue pour les vidéos YouTube ne pouvait pas être désactivé.

## 1.7.8

- DeepL, Microsoft Translate, Google Translate, OpenAI, Claude, Gemini et d'autres services de traduction prennent en charge la traduction pour conserver le formatage du texte original (par exemple, les liens, le gras, etc.)
- Après avoir sélectionné le texte, le menu clic droit changera en [Traduire le texte], en cliquant dessus, vous pouvez automatiquement accéder à la page de traduction de texte immersive
- Nouveau service de traduction gratuit pour les grands modèles : SiliconCloud, disponible pour tous les utilisateurs.
- Ajout de la traduction du grand modèle Zero-One-Thing, qui peut être utilisée en remplissant la clé API après inscription sur la plateforme Zero-One-Thing.
- Nouveau bouton de retour d'utilisateur pour la traduction de mangas (après avoir traduit un manga, cliquez sur le bouton [Feedback] sur le côté droit de la balle flottante pour donner votre avis sur la qualité de la traduction).

## 1.7.7

- Adoption de l'algorithme de découpage de phrases intelligent AI pour les sous-titres anglais auto-générés sur YouTube [Pro Disponible]
- Optimisation de la traduction par clic droit en "Traduire vers xx langue cible"
- Support de l'intégration immersive [JS SDK](https://immersivetranslate.com/docs/js-sdk/) pour les sites web tiers
- Optimisation de l'affichage des sous-titres Hulu
- Support de la traduction des sous-titres de réunion de la version web de ZOOM

## 1.7.6

- Support de la personnalisation des experts AI, l'entrée se trouve en bas de la page [Paramètres]->[Expert AI].
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

- Corrigé l'échec de la traduction de bandes dessinées dans le navigateur Firefox.

## 1.7.1

- Amélioration de la vitesse de traduction des bandes dessinées
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
- Les sous-titres bilingues de YouTube prennent désormais en charge le découpage intelligent des phrases (Beta) (Uniquement lors de l'activation manuelle de la traduction immersive des sous-titres YouTube dans [Paramètres] - [Sous-titres vidéo], et les sous-titres vidéo originaux sont des sous-titres anglais auto-générés)
- Ajout du service de traduction Tencent [【Hunyuan Large Model】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- Correction des problèmes de mise en page du texte des traductions de bandes dessinées pour les langues en écriture latine.
- Nouveaux sites pris en charge pour la traduction de bandes dessinées :
  - COMIC FUZCOMICFUZ(https://comic-fuz.com/)
  - MangaDexMangaDex(https://mangadex.org/)
  - KuaiKan ComicsKuaiKanComics(https://www.kuaikanmanhua.com/)
- Corrigé un problème où les services AI personnalisés ne pouvaient pas sélectionner d'experts AI.

## 1.6.4

- Lorsque des experts en IA sont utilisés pour la "Sélection Intelligente", différents experts en IA peuvent être personnalisés pour différents sites web. Cela peut être configuré dans [Paramètres] -> [Experts en IA] -> [Entrer n'importe quel expert].
- Correction du problème où les sous-titres ne s'affichaient pas sur YouTube en mode "Traduction uniquement".
- Correction du problème des sous-titres bilingues ne fonctionnant pas sur Mubi.
- Compatible avec les PDF ouverts avec le plugin Adobe Acrobat.
- Tous les utilisateurs peuvent [contribuer en ligne](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/) à la traduction multilingue de l'interface de traduction immersive.

## 1.6.3

- Nouvelle fonctionnalité : traduction de manga (Beta), sur les sites de manga pris en charge, un bouton de traduction de manga apparaîtra sous la bulle flottante de traduction rapide de la page web. En cliquant dessus, la traduction de manga sera activée. Cette fonctionnalité est disponible pour les membres Pro (500 pages par mois, des packs supplémentaires peuvent être achetés), actuellement prise en charge sur les sites suivants :
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)

## 1.6.2

- Nouvelle fonctionnalité : traduction de manga (Beta), sur les sites de manga pris en charge, un bouton de traduction de manga apparaîtra sous la bulle flottante de traduction rapide de la page web. En cliquant dessus, la traduction de manga sera activée. Cette fonctionnalité est disponible pour les membres Pro (500 pages par mois, des packs supplémentaires peuvent être achetés), actuellement prise en charge sur les sites suivants :
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- Nouvelle fonctionnalité : la traduction par IA prend en charge le [modèle large Doubao](https://www.volcengine.com/product/doubao)
- Nouvelle fonctionnalité : prise en charge du mode de comparaison bilingue avec la traduction d'abord et le texte original ensuite, qui peut être activé dans la page des paramètres -> paramètres avancés.
- La liste des modèles IA personnalisés prend en charge la syntaxe `-all`, qui peut supprimer tous les modèles prédéfinis.
- Dans les sous-titres vidéo bilingues, lorsque la langue cible est le chinois simplifié et que le texte original est en chinois traditionnel, le texte original sera automatiquement converti en chinois simplifié, et vice versa.
- Correction du problème où le raccourci de la bulle flottante ne pouvait pas traduire sous iOS 18.
- Correction du problème où les invites personnalisées étaient inefficaces lorsqu'elles étaient trop nombreuses.

## 1.6.1

- Prend en charge la plateforme de modèle large Baidu Qianfan, la plateforme de modèle large Alibaba Bailian, la plateforme de modèle large DeepSeek.
- Correction du problème où la modification de la langue cible et d'autres paramètres dans le panneau contextuel se réinitialisait lors du clic sur la bulle flottante de traduction.

## 1.5.8

- Les experts en IA prennent en charge le mode "Sélection Intelligente", où le système sélectionnera automatiquement l'expert en IA le plus adapté en fonction du site web actuel (par exemple, les experts en IA liés à la technologie seront automatiquement sélectionnés pour The Verge et Hacker News, tandis que l'amélioration de la traduction Twitter sera automatiquement sélectionnée pour Twitter).

## 1.5.7

- Prise en charge de l'ajout de services de traduction IA personnalisés compatibles avec OpenAI, accessibles en bas de la page [Paramètres]->[Services de Traduction].
- Correction d'un problème où les sous-titres bilingues ne fonctionnaient pas sur la plateforme vidéo Domestika dans Safari.

## 1.5.6

- Optimisation significative des performances de traduction des grandes pages web, de la création d'ePub et des fichiers de sous-titres.
- Correction du bug de synchronisation multi-appareils dans Pro.

## 1.5.4

- Les membres Pro prennent en charge les services de traduction Claude et Gemini prêts à l'emploi (Beta)
- Les sous-titres bilingues YouTube prennent en charge les paramètres de police et de poids de la police
- Correction des problèmes de limites de mots lors de l'emballage de longs paragraphes [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- Correction de la reconnaissance des langues japonaise et coréenne
- Correction du problème où les pages Reddit sur les appareils mobiles n'étaient pas traduites lors du défilement
- Correction de certaines pages manquant de traductions avec DeepL
- Correction du temps de synchronisation multi-appareils des utilisateurs Pro ne se synchronisant pas
- Optimisation des problèmes de couverture des paramètres de synchronisation cloud
- Optimisation des mots d'invite pour les services de traduction IA

## 1.5.2

- Correction du problème où les modifications de l'invite d'expert général remplaçaient l'invite d'expert IA spécifiée [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- Le nom de modèle IA personnalisé prend en charge la syntaxe avancée, utilisez + pour ajouter un modèle, utilisez - pour masquer un modèle, et utilisez model_name=display_name pour personnaliser le nom d'affichage du modèle, par exemple : +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- Correction de l'erreur retournée par Gemini
- Masquer la bulle flottante lors de l'impression de la page
- Correction de la taille de la police ne s'adaptant pas proportionnellement lorsque YouTube est en plein écran [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- Prise en charge des services de traduction IA pour définir [Expert IA] afin de spécifier la stratégie de traduction, actuellement une fonctionnalité Beta, qui peut être activée dans [Paramètres Développeur](https://dash.immersivetranslate.com/#developer) après avoir activé Beta, et le menu [Expert IA] peut être vu après actualisation.
- Les services de traduction IA peuvent désormais personnaliser la liste des modèles, tels que [OpenAI], le système n'a que quelques-uns des modèles les plus couramment utilisés intégrés. En cliquant sur la liste déroulante des modèles, le dernier élément que vous voyez est [Définir Plus de Modèles], après réglage, il sera automatiquement mémorisé pour la commodité des utilisateurs testant différents modèles personnalisés.
- Optimisation de l'incohérence dans la mise en page des traductions dans certains cas.
- Ajout d'un bouton de réinitialisation pour le style des sous-titres YouTube, qui peut rapidement restaurer le style par défaut.
- Correction du problème où les sous-titres chinois ne pouvaient pas être téléchargés sur YouTube.
- Optimisation de la copie de l'interface en chinois traditionnel.

## 1.4.12

- Correction du problème de boîte de dialogue de message non traduit lors de l'ouverture de la page reddit
- Ajout d'une fonctionnalité temporaire pour activer l'édition de traduction dans l'entrée "Plus" du panneau
- Correction du problème où les YouTube Shorts sans sous-titres affichent toujours les sous-titres de la vidéo précédente [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- Correction du problème où les sous-titres bilingues YouTube ne peuvent pas être ajustés de haut en bas en plein écran [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- Prise en charge des sous-titres bilingues pour [VK Video](https://vk.com/video)
- Prise en charge des paramètres d'activation indépendants pour les sous-titres bilingues des vidéos YouTube (activé par défaut pour les nouveaux utilisateurs)
- Optimisation des messages d'erreur pour la traduction des sous-titres bilingues locaux

## 1.4.11

- Compatible avec la traduction de la boîte de saisie de la page Bing Copilot
- Le contrôle du style des sous-titres YouTube prend en charge le style des bords
- Prise en charge de la sélection du service de traduction par défaut sur la page Paramètres -> Service de Traduction
- Correction du remplacement de l'espace réservé OpenAI SystemPrompt
- Correction du problème de fusion des règles utilisateur personnalisées
- Correction de l'affichage anormal des sous-titres pour certaines vidéos Netflix [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- Correction du problème où les changements fréquents de couleur de traduction via la palette de couleurs étaient inefficaces [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- Les services de traduction sont désormais distinctement organisés sous un onglet séparé, permettant une vue d'ensemble complète de tous les services de traduction disponibles. De plus, les utilisateurs ont la flexibilité de personnaliser les services de traduction affichés. Par défaut, seule une sélection limitée de services de traduction est affichée, mais les utilisateurs peuvent personnaliser leurs préférences d'affichage dans la section [Plus de Services](https://dash.immersivetranslate.com/#services).
- La page des paramètres permet désormais des ajustements aux [styles de sous-titres YouTube](https://dash.immersivetranslate.com/#subtitle).
- Des améliorations ont été apportées pour résoudre le problème où les sous-titres bilingues immersifs ne s'affichaient pas lorsque les utilisateurs définissaient la langue des sous-titres sur le chinois sur le site YouTube.
- Un nouveau raccourci a été introduit pour la traduction temporaire nommée Claude, qui peut être configuré dans la [page des paramètres de raccourci](https://dash.immersivetranslate.com/#shortcuts).

## 1.4.8

- Optimisation des performances de traduction pour les grands fichiers dans PDF-Pro
- Amélioration des performances de traduction pour les pages de contenu long
- Mise en œuvre de la prise en charge de l'internationalisation (i18n) pour la navigation dans les documents de page
- YouTube introduit une fonctionnalité pour activer temporairement les sous-titres bilingues
- YouTube prend en charge le téléchargement de sous-titres bilingues (membres uniquement)
- Mobile ajoute le contrôle gestuel, améliorant l'entrée via les [paramètres de raccourci](https://dash.immersivetranslate.com/#shortcuts)
- Prise en charge de la traduction bilingue pour Google Docs

## 1.4.7

- Correction du problème où la traduction échouait lors du changement des mots d'invite personnalisés OpenAI sous le bouton de test
- Correction du problème de l'icône de raccourci des sous-titres YouTube ne s'affichant pas
- Optimisation de la reconnaissance linguistique de l'extension

## 1.4.6

- Correction du problème où les mots d'invite définis par l'utilisateur étaient inefficaces
- Ajout d'options 50%, 150% pour la taille de la police des sous-titres YouTube

## 1.4.5

- Correction du problème où les modifications des styles de sous-titres YouTube n'étaient pas enregistrées
- Correction de la disparition des sous-titres en plein écran sur iOS Safari
- Optimisation supplémentaire de la vitesse de traduction des sous-titres YouTube
- Les options supplémentaires du panneau prennent désormais en charge [l'entrée de traduction de texte](https://app.immersivetranslate.com/text/)

## 1.4.2

- Prise en charge du service de traduction Claude
- Optimisation des mots d'invite multi-OpenAI, prenant en charge le format YAML, ce qui améliore la flexibilité et la facilité d'utilisation de la configuration
- Optimisation significative de la vitesse de traduction des sous-titres YouTube, et ajout de la prise en charge du changement d'ordre chinois-anglais, de la personnalisation de la couleur et de la taille de la police, etc.
- La plateforme de sous-titres vidéo prend en charge [l'Université de Southampton](https://southampton.cloud.panopto.eu)
- Les sous-titres bilingues Udemy compatibles avec l'affichage mobile
- Le service de traduction Gemini est masqué par défaut, peut être activé dans les paramètres développeur pour afficher la version bêta de ce service de traduction

## 1.3.4

- Prise en charge du service de traduction gratuit Yandex
- Optimisation des mots d'invite Gemini
- Les sous-titres vidéo prennent en charge le réglage pour l'affichage bilingue/original et traduction
- Prise en charge de l'espace entre le chinois et l'anglais dans les résultats de traduction OpenAI
- Le commutateur de panneau pour n'afficher que le bouton de traduction modifié pour ne prendre effet que sur la page actuelle

## 1.3.3

- Optimisé le problème d'affichage des sous-titres vidéo CC de Twitter.
- Le service DeepL a ajouté le support pour l'arabe.
- Le service de traduction Colorful Clouds prend désormais en charge le coréen, l'espagnol, le français et le russe.
- Le service OpenAI a ajouté le support pour le dialecte chinois du nord-est.
- La détection automatique du panneau affiche désormais la langue d'origine.
- Ajustement de la description des raccourcis pour le panneau mobile.

## 1.3.2

- Correction du problème où le panneau de contrôle ne pouvait pas être fermé sur les appareils mobiles

## 1.3.1

- Support de la plateforme de sous-titres vidéo [DeepLearning.ai](https://learn.deeplearning.ai)
- Support pour la traduction de pages web et de sous-titres vidéo dans des langues telles que l'arabe, l'hébreu, etc., résolvant les problèmes d'affichage RTL (de droite à gauche)
- Correction de la traduction de Gemini en hébreu
- Correction d'un problème où certains sous-titres chinois traditionnels sur YouTube ne s'affichaient pas correctement
- Correction du problème d'affichage des sous-titres Twitter sur Safari
- Correction du raccourci pour la traduction immédiate en bas de la page

## 1.2.4

- Correction du problème où les espaces réservés dans la création d'ePub n'étaient pas remplacés correctement
- Support de la traduction de sous-titres vidéo [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- Optimisation du contrôle de fréquence des requêtes de service de traduction
- Les récentes requêtes de service de traduction Microsoft depuis la Chine ont été instables ; en cas d'erreurs, le système détecte automatiquement le service de traduction actuellement disponible, permettant aux utilisateurs de basculer rapidement.
- Optimisation du message d'erreur pour les erreurs réseau
- Correction du problème où la configuration de la couleur du texte ne supportait pas l'aperçu RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Correction du problème où la mise à niveau de la version du plugin Safari affichait toujours la page de succès d'installation
- Microsoft a ajouté le support pour le vietnamien
- Correction du problème où les sous-titres traduits sur le site edx ne s'affichaient pas

## 1.2.2

- Support de la traduction de sous-titres vidéo pour [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). Supporte également la traduction de certaines vidéos sous-titrées CC sur Twitter.
- Optimisation des pop-ups d'erreur, les pop-ups d'erreur de problème réseau détectent automatiquement les services de traduction gratuits valides.
- Correction du support de l'application immersive iOS pour la lecture en plein écran sur YouTube.
- Correction du problème de traduction de paragraphe avec Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Support de la traduction de sous-titres vidéo pour [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/).
- Correction d'un problème où certains utilisateurs Pro ne pouvaient pas modifier les paramètres dans le navigateur Chrome.
- Support de l'affichage des sous-titres bilingues en mode plein écran sur YouTube sur iOS.

## 1.2.0

- Support de la traduction de sous-titres vidéo sur les plateformes [LinkedIn](https://www.linkedin.com/) et [Viu](https://www.viu.com/).
- Ajout de plus d'accès rapide aux sous-titres vidéo pour des plateformes supplémentaires.
- Support pour définir des sites web/langues spécifiques pour n'afficher que le texte traduit.
- Correction d'un problème où la page des paramètres affichait continuellement le chargement dans certains cas sur Safari.
- Support pour la traduction des nœuds de balise d'entrée.
- Optimisation de l'interface utilisateur des pop-ups d'erreur.

## 1.1.9

- Support de la traduction de sous-titres pour YouTube Live et la plateforme [Mubi](https://mubi.com/).
- Optimisation : Page des paramètres, interaction de la liste des URL (pour éviter l'ambiguïté, les cases à cocher ne sont pas affichées par défaut).
- Support pour définir la police de traduction en mode traduction uniquement.
- Ajout d'un accès rapide pour activer les sous-titres vidéo sur Netflix, Ted, Bloomberg, Udemy, Coursera.
- Correction : Certains styles traduits (comme les soulignements) n'étaient pas efficaces sur Safari.
- Correction : Pendant la traduction de page, le survol de la souris ne déclenchait pas la retraduction.

## 1.1.8

- Ajout d'une option pour que le service de traduction enfant suive le service de traduction principal
- Support des sous-titres bilingues pour [Amazon Prime Video](https://www.primevideo.com)
- Optimisation supplémentaire de la fonction de traduction de PDF intégré dans Sci-Hub
- Correction d'un problème avec les PDF en ligne ne s'ouvrant pas correctement
- Correction du problème de lecture continue des sous-titres bilingues sur Netflix

## 1.1.7

- Vous pouvez maintenant spécifier une police pour la traduction dans la page des paramètres -> [Paramètres de base] -> [Style de traduction]
- Ajout d'une configuration de raccourci pour [Traduire le paragraphe spécifié] dans le panneau de la balle flottante sur les appareils mobiles
- Optimisation de la sensibilité de la détection du survol de la souris sur Ctrl pour éviter de confondre `Ctrl+C` avec `Ctrl`
- Ajout d'un support pour un nouveau paramètre de raccourci permettant de basculer rapidement si les sous-titres vidéo utilisent les sous-titres de traduction automatique intégrés
- Sur le site Sci-Hub, cliquer sur la balle flottante traduira les PDF intégrés dans la page web

## 1.1.6

- **Support mobile pour la traduction de paragraphes spécifiques :** La version mobile prend désormais en charge la traduction de paragraphes spécifiés et a ajouté une variété d'opérations de raccourci, y compris le balayage vers la gauche, le balayage vers la droite, le double-tap, le triple-tap et les gestes de toucher multi-doigts. Ceux-ci ne sont pas activés par défaut et nécessitent que l'utilisateur sélectionne activement le geste de déclenchement dans la page des paramètres sous [Survol de la souris].
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
    - **Entrée de traduction de document :** L'entrée pour traduire des fichiers "PDF/ePub/sous-titres" a été déplacée vers le menu principal pour un accès rapide.
    - **Paramètres de traduction vidéo :** L'entrée pour les paramètres de "Traduction vidéo" a également été placée dans le menu principal pour des ajustements rapides.
    - **Nouvelle entrée pour la documentation d'utilisation :** Fournit des guides d'opération détaillés et des documents d'aide.

- **Entrée de traduction de document intégrée :** Désormais, vous pouvez traduire des fichiers PDF, ePub et de sous-titres via une entrée de téléchargement unifiée. Il suffit de cliquer sur le bouton [PDF/ePub] dans le panneau contextuel, plus besoin de sélectionner [Plus].

- **Ajout de support pour 5 sites web vidéo :**
  - Support pour les sous-titres des podcasts sur Youtube Music.
  - Ajout de support pour le site iview.abc.net.au.
  - Ajout de support pour le site www.nma.art.
  - Ajout de support pour le site creativecloud.adobe.com.
  - Ajout de support pour le site www.masterclass.com.

## 1.1.3

- Correction du problème d'anomalie d'affichage du plugin mobile lors de l'ouverture de pages PDF.
- Optimisation de l'effet de traduction des conversations GPT.
- Support de la traduction de domaine pour Baidu Translate.
- Ajout d'un mode traduction uniquement dans la page des paramètres.
- Ajout d'une fonction de rappel lors du changement de mode de traduction avec des raccourcis.
- Correction du problème où la traduction des champs d'entrée contenant des URL ne traduisait que des parties du contenu.

## 1.1.2

- Correction : Le problème où le changement de service de traduction ne prenait pas effet lorsque la page n'avait pas encore été traduite.
- Optimisation : Dans le processus de traduction d'Epub et de PDF, si certains contenus échouent à être traduits, il est maintenant possible de passer à un autre service de traduction sur le panneau sans redémarrer tout le processus de traduction (la logique précédente était d'utiliser immédiatement un nouveau service de traduction pour retraduire tout le livre). Cela signifie qu'à mi-chemin de la traduction, vous pouvez passer à un autre service de traduction et cliquer sur [Réessayer tous les paragraphes échoués], après quoi le système continuera la traduction en utilisant le nouveau service.
- Optimisation : Ajustement de la taille de la police des messages d'erreur de traduction pour améliorer la lisibilité.

## 1.1.1

- Correction du problème du raccourci des sous-titres bilingues pour YouTube ayant un texte anglais trop long.

## 1.1.0

### Nouvelles fonctionnalités

- **Paramètres de raccourcis clavier** : Ajout d'un nouveau menu de niveau supérieur "Raccourcis" et des fonctions de raccourcis clavier personnalisables suivantes :

  - Désigner une combinaison de touches pour traduire le contenu de la boîte d'entrée actuelle, en complément de la méthode précédente de frapper rapidement la barre d'espace trois fois.
  - Désigner une combinaison de touches pour activer temporairement la "traduction directe au survol de la souris" sur la page. En appuyant à nouveau, cette fonction sera annulée.
  - Ajout de raccourcis dédiés pour 6 services de traduction (tels que DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation) pour faciliter le changement temporaire entre les services de traduction.

- **Mise à jour de la page des paramètres du plugin** :

  - Dans "Paramètres avancés", une nouvelle option a été ajoutée pour permettre aux utilisateurs de spécifier certains mots (par exemple, "LLM") à exclure de la traduction.
  - Dans "Paramètres avancés", une nouvelle option a été ajoutée pour configurer le nombre minimum de caractères requis pour traduire un paragraphe. Le défaut est de 4 caractères, mais il peut être réglé plus haut (par exemple, 20), de sorte que seuls les paragraphes plus longs seront traduits.
  - Ajout d'un tutoriel pour les débutants, couvrant les paramètres de la balle flottante, les paramètres des sous-titres vidéo et les paramètres de survol de la souris.

- **Sous-titres bilingues YouTube** : Ajout d'un accès rapide dans la fenêtre de lecture vidéo YouTube pour activer ou masquer les sous-titres bilingues (cette fonctionnalité peut être désactivée).

- **Support linguistique Deepl** : Ajout du support pour le portugais (Brésil).

- **Guide pour les nouveaux utilisateurs** : Lorsque de nouveaux utilisateurs ouvrent pour la première fois une page dans une langue non cible, une bulle d'aide de la balle flottante est affichée.

### Optimisation et corrections

- **Optimisation de l'interface utilisateur** : Refonte de l'interface utilisateur pour les messages d'erreur de traduction de page pour les rendre plus compréhensibles. Lorsqu'il y a de nombreuses erreurs, une fenêtre contextuelle avertira activement l'utilisateur.

- **Corrections de bugs** :

- Correction du problème où la traduction au survol échouait lorsque la page perdait le focus.
- Correction du problème où moins de 3 caractères dans la fonctionnalité d'amélioration de la boîte de saisie n'étaient pas traduits.
- Correction du problème où certains répertoires n'étaient pas traduits lors de la production d'Epubs bilingues.

- **Suppression de fonctionnalité** : Suppression de la fonctionnalité d'amélioration de l'information bilingue (affichage simultané des résultats de recherche en anglais sur les pages de recherche Google).

### Autres mises à jour

- **Mise à jour de la configuration openAI** : Prend désormais en charge la configuration du nombre de configurations par seconde en décimales, comme 0.5, signifiant 1 requête toutes les 2 secondes.

## 0.12.14

- Correction : Problème de reconnaissance de la langue cible par défaut sur certaines machines après la première installation.
- Optimisation : L'ordre par défaut des titres de pages web est changé en [Chinois - Anglais].

## 0.12.13

- Correction : Problème de couture de traduction de longs paragraphes OpenAI dans certains cas. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Optimisation : Lors de l'utilisation du survol de la souris, le problème où la perte de focus sur la page et le re-déclenchement devenaient inefficaces.
- Correction : Le problème où le cache existait toujours après la modification de l'invite/modèle dans OpenAI.

## 0.12.12

- Mise à jour : Optimisation du panneau contextuel, suppression de certaines options pour le site web actuel.
- Optimisation : Amélioration du processus de fusion des sous-titres manuels.
- Optimisation : Définition automatique de la langue cible en fonction de la langue du navigateur.
- Ajout : Prise en charge des sous-titres bilingues pour la plateforme d'apprentissage [ArtStation](https://www.artstation.com/learning) et [ZDF](https://www.zdf.de/).
- Correction : Résolution du problème où les titres sur la page de liste jstor n'étaient pas traduits [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Correction : Correction du problème où seule une partie du contenu disparaissait sur Hacknews [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Ajout de la prise en charge des sous-titres bilingues pour les plateformes [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/), et [Domestika](https://www.domestika.org).

## 0.12.10

- Correction du problème d'autorisation du domaine Gemini sous le script Tampermonkey.
- Prise en charge de la traduction en temps réel des sous-titres pour Twitter Space.
- Pour les anciennes versions du script Tampermonkey, une invite de mise à jour a maintenant été ajoutée à la page des paramètres.

## 0.12.9

- Ajout de la prise en charge de la traduction Gemini.
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

- Ajout de sous-titres bilingues pour prendre en charge les plateformes [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) platforms. https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/) Platforms
- La hoverball est maintenant cachée par défaut lorsque la vidéo est en plein écran.
- Correction du problème de clic saccadé du panneau d'action de la hoverball de la page Firefox.
- Prise en charge de la collaboration sous le site pubmed.ncbi.nlm.nih.gov et le plugin scholarscope
- Correction du problème de saccade de la page de traduction de la boîte de saisie reddit

## 0.12.6

- Correction du problème où la traduction de YouTube/Web of Science etc. n'est pas sensible lors du changement d'onglets.
- La hoverball sur mobile prend désormais en charge l'opération de pression longue, pression courte pour traduire, pression longue pour ouvrir le panneau.
- La traduction des ebooks bilingues traduira désormais également la table des matières.
- La fonctionnalité d'amélioration de la recherche (certaines pages de recherche Google affichent des résultats de recherche bilingues) n'est désormais pas activée par défaut et sera supprimée dans la prochaine version.

## 0.12.5

- Correction de la création d'Epub à partir du panneau en cliquant sur les traductions qui ne fonctionnent pas

## 0.12.4

- Lorsque vous activez les sous-titres bilingues dans le panneau, il rafraîchira d'abord automatiquement la page (pour afficher plus précisément les sous-titres bilingues), et certains sites nécessitent encore que les utilisateurs cliquent manuellement sur le bouton "CC" sur le site pour activer les sous-titres.
- Optimisation de Grease Monkey, détection de la langue Safari
- Fournit un accès rapide aux versions bilingues de tous les articles sur le site d'articles [Arxiv](https://arxiv.org/abs/1910.06709).
- [Support de la hoverball configuré pour être fixé à gauche #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Correction du problème d'affichage du mode d'apprentissage #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Activer temporairement la traduction web pendant une période de temps ne désactive pas Toujours Traduire #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Optimisation des problèmes d'initialisation des fichiers PDF

## 0.12.3

- Correction pour la fonctionnalité [désactiver définitivement les sous-titres vidéo] ne fonctionnant pas [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)

## 0.12.2

- La prise en charge des sous-titres bilingues est fournie pour plus de plateformes vidéo, qui sont maintenant prises en charge : [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy] (https://www\.khanacademy.org/), [Coursera] (https://www\.coursera.org/), [Vimeo] (https://vimeo.com/), [Nebula] (https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), etc. (Notez que, en raison des limitations techniques, certains sites web doivent rafraîchir la page après avoir activé les sous-titres bilingues pour la première fois ou attendre que la traduction soit terminée pour afficher les sous-titres bilingues). (Notez que, en raison des limitations techniques, certains sites web doivent rafraîchir la page après avoir ouvert les sous-titres bilingues pour la première fois, ou doivent attendre que la traduction soit terminée pour afficher les sous-titres bilingues)
- Optimisation significative de la taille du fichier zip du plugin, réduite de moitié par rapport à l'original, téléchargement et mise à jour plus rapides.
- Correction des problèmes de téléchargement PDF étendu
- Ajout d'un portail de traduction rapide PDF sur le côté droit du site d'articles [Arxiv](https://arxiv.org/abs/1910.06709), qui mène à une page HTML propre (seulement pris en charge par certains articles, car cela nécessite que les auteurs originaux soumettent le code source, donc environ 50% des articles afficheront ce portail)
- Les pages PDF en ligne sans extension .pdf peuvent maintenant sauter directement à la page de traduction PDF en cliquant sur la hoverball sur la page.
- Correction de certains problèmes d'amélioration de la boîte de saisie sous Safari
- Optimisation de la détection de la langue dans Grease Monkey et Safari

## 0.11.6

- Ajout de 11 nouvelles langues d'interface pour le plugin et le site officiel, maintenant les langues d'interface prises en charge atteignent 14, y compris le chinois simplifié, le chinois traditionnel, l'anglais, le japonais, le coréen, le russe, l'espagnol, le portugais, l'hindi, l'italien, l'allemand, le français, l'arabe et le persan.
- Modification du partage bilingue (mode de rafraîchissement) ajouté dans la dernière version pour le partage de capture d'écran de page bilingue, afin que le contenu partagé soit plus original, ainsi qu'une adaptabilité plus large.
- Correction de l'emoji à la fin de la boîte de saisie Twitter qui ne peut pas être traduit
- Correction de la situation où le contenu des plug-ins tiers est traduit dans certains scénarios
- Réparation du clic non réactif de la hoverball PDF en ligne

## 0.11.5

- Vous pouvez maintenant générer un lien public vers la page bilingue traduite pour Immersive Translate.
  - [Cliquez](/docs/share/) sur l'icône de partage Immersive Translate pour le générer en un clic !
- Résolution du problème où certaines plateformes ne pouvaient pas reconnaître si la souris était prise en charge ou non
  - Il y a certains navigateurs de bureau qui prennent en charge à la fois l'écran tactile et la souris, et Immersive Translates est techniquement incapable de détecter si ces plateformes prennent en charge la souris, donc nous avons ajouté l'option [Forcer l'activation du support de la souris] dans le paramètre [Survol de la souris]

## 0.11.2-0.11.4

- Optimisation de l'expérience, correction de certains bugs

## 0.11.1

- Le modèle par défaut pour les traductions OpenAI est : GPT3.5-turbo-1106.
- Optimisation de l'invite chinoise pour OpenAI, maintenant moins sujette aux hallucinations !
- Réduction de la longueur des invites d'OpenAI de 90 à 40, économisant encore plus de trafic.

## 0.11.0

- Correction des clics saccadés de la hoverball de page
- Correction des problèmes de traduction Azure

## 0.10.9

- Correction de quelques problèmes mineurs

## 0.10.8

- Prise en charge de la configuration des boutons de traduction rapide de la hoverball (prise en charge PC/mobile)
- Optimisation du jugement de la langue Grease Monkey
- Correction de la traduction de fichiers txt

## 0.10.7

- Prise en charge du survol de la souris pour appuyer à nouveau sur Ctrl pour afficher le texte original
- Ignorer la langue jamais traduite lors du survol de la souris
- Optimisation des sous-titres bilingues de Youtube

## 0.10.6

- Prise en charge des sous-titres Youtube uniquement pour les traductions
- Ajout d'une alerte de mise à jour de la version basse de Grease Monkey
- Correction du problème où les fichiers txt locaux ne peuvent pas être traduits

## 0.10.5

- Correction du retour occasionnel de Youtube à la page d'accueil

## 0.10.4

- Correction du conflit de sous-titres Youtube avec le plugin de sous-titres doubles (Immersive Translate de la traduction des sous-titres Youtube n'est pas activé lorsque le plugin Youtube Dual est détecté pour éviter le conflit)
- Ajout de la [fonction de désactivation permanente des sous-titres vidéo], s'il y a d'autres problèmes de conflit et que vous ne souhaitez pas activer la fonction de sous-titres bilingues avec Immersive Translate.
- Optimisation des sauts de sous-titres

## 0.10.3

- Correction du problème de traduction de la clé d'authentification personnalisée DeppL

## 0.10.3

- Support parfait pour les vidéos Youtube avec sous-titres bilingues 🎉.
- Pour les pages d'articles, le texte principal sera désormais traduit avant le reste du contenu de la barre latérale
- Optimisation de la contextualisation de la traduction DeepL
- Optimisation de la traduction des fichiers de sous-titres par OpenAI pour la contextualisation

## 0.10.1

- Augmentation de la priorité de la traduction du corps pour optimiser l'expérience de traduction
- Correction du problème de texte non traduit lors du clic sur "plus" dans ins

## 0.9.8

- Optimisation de l'expérience, correction de certains bugs

## 0.9.7

- Correction de la traduction automatique lorsque readwise est surligné

## 0.9.6

- Correction du vidage du cache en déconnectant la connexion de l'utilisateur.

## 0.9.5

- Corrections de bugs pour les eBooks en ligne

## 0.9.4

- Optimisation de la détection de l'amélioration de l'entrée pour réduire les faux contacts
- Traduction en ligne des e-books et des sous-titres

## 0.9.3

- Traduction de la boîte de saisie : affiche un rappel contextuel lors de la première utilisation, et l'utilisateur peut choisir de le désactiver cette fois-ci ou de manière permanente pour éviter les contacts accidentels.
- Optimisation de la vitesse d'exportation de la traduction uniquement pour les PDF, si vous choisissez d'exporter uniquement la traduction, vous pouvez directement appeler l'aperçu PDF du système pour exporter, plus rapide.
- Deeplx prend en charge plusieurs URL, il suffit de les séparer par .

## 0.9.2

- L'outil de traduction PDF est migré vers la version en ligne : https://app.immersivetranslate.com/pdf/ , afin que Grease Monkey et Safari puissent utiliser la traduction PDF, et les problèmes peuvent être mieux itérés sans avoir besoin de publier une version pour résoudre le problème.
- Optimisation de l'UI POPUP, le panneau est plus beau !

## 0.9.1

- Correction des problèmes de nom de fichier lors de la création d'un ebook Epub

## 0.8.8

- Support PDF pour les ajustements d'espacement des lignes et des mots pour re-reconnaître les paragraphes
- Correction du problème de défilement automatique lors de la lecture en ligne d'epub sur mobile

## 0.8.7

- Support PDF pour les téléchargements de traduction uniquement
- Correction du problème de connexion Google sur Safari

## 0.8.2 - 0.8.6

- Permet de définir l'intervalle entre les déclencheurs de combo d'amélioration de l'entrée
- Correction de certains bugs

## 0.8.1

- Optimisation de la détection de la langue
- Fonctionnalités Beta : API personnalisée (Beta activée dans les paramètres développeur)
- Support pour la traduction AliCloud
- Correction de certains bugs

## 0.8.0

- Systèmes d'utilisateurs pris en charge
- Prend en charge [Enable Pro Membership](/pricing), ce qui permet aux utilisateurs de profiter des traductions Deepl et OpenAI et des paramètres de synchronisation cloud.
- Le service de traduction au survol de la souris peut être configuré individuellement
- Le service de traduction de la boîte de saisie peut être configuré séparément
- Optimisation de la traduction PDF
- Correction de certains bugs

## 0.7.16

- Traduction PDF avec de nouvelles options pour un contrôle rapide du style de traduction (les fichiers PDF sont très étranges et l'activation de ces options peut être utile pour certains fichiers PDF avec un formatage désordonné)
- Les versions iOS et macOS sont de retour sur l'Apple Store Country Store

## 0.7.15

- Nous avons été informés par Apple que les traductions OpenAI ont été temporairement retirées d'iOS et macOS, et nous essayons de les relancer en Chine.

## 0.7.11- 0.7.14

- Correction : problème de traduction de toutes les régions dans Gmail
- Désactivation temporaire de la fonction d'exportation PDF de Safari en raison de la restriction de Safari sur les téléchargements de plug-ins (bug).
- Correction de quelques autres problèmes

## 0.7.10

- Mise à niveau de l'UI du panneau d'icônes du navigateur contextuel, un peu plus de design ～
- Correction du problème que certains passages japonais ne sont pas traduits.

## 0.7.9

- Le PDF prend enfin en charge l'exportation de versions bilingues ! Vous pouvez cliquer sur le bouton [Enregistrer] pour exporter le fichier PDF bilingue traduit.
- Les règles personnalisées prennent désormais en charge la fusion avec les règles intégrées par défaut, par exemple : `{"id": "youtube", "selectors.add":["#test"]}` signifie ajouter un `#test` aux sélecteurs existants, `selectors` signifie remplacer le défaut, `selectors.remove` signifie supprimer un des sélecteurs par défaut, et `selectors.remove` signifie supprimer un des sélecteurs par défaut.
- Icône Safari mise à jour, un peu plus grande.
- Autres corrections de bugs

## 0.7.8

- Corrections de bugs

## 0.7.7

- Adapté au style système de Safari, l'icône de l'extension Safari est passée à un contour transparent.
- Ajout du changement de statut de l'icône du navigateur, lorsqu'une page web a été traduite, un ✅ sera automatiquement ajouté en bas à droite de l'icône du navigateur.
- Activer automatiquement la traduction des sites web anglais fréquemment utilisés pour les nouveaux utilisateurs
- Correction des problèmes de traduction avec https://claude.ai/

## 0.7.6

- Support de la traduction des résultats de l'amélioration de l'entrée avec ctrl+z Annuler
- Support de la traduction en mode de lecture de document Flying Book
- Adaptation https://pi.ai/talk

## 0.7.5

- Correction de l'icône Grease Monkey qui ne s'affiche pas
- Correction de plusieurs problèmes

## 0.7.4

- Correction de plusieurs problèmes
- La page de configuration prend en charge la suppression en lot des URL sélectionnées.
- Prend en charge l'activation/désactivation de la traduction des sous-titres Youtube pour éviter les conflits avec d'autres plugins connexes.
- Arigato Translator prend en charge le réglage des champs et de l'identifiant de la terminologie

## 0.7.2

- Amélioration de la boîte de saisie : permet d'omettre le préfixe // et de déclencher la traduction de l'ensemble de la boîte de saisie avec 3 espaces, ou vous pouvez désactiver cette option dans la page des paramètres.

## 0.7.1

- Support de l'amélioration de la recherche, lorsqu'elle est activée, lorsque vous effectuez une recherche sur Google/Google News en chinois, la colonne de droite affichera automatiquement les résultats de recherche des mots-clés anglais correspondants, ce qui est activé par défaut.
  - Raison : Nous avons constaté que dans la recherche Google, les résultats de recherche pour les mots-clés chinois et anglais peuvent être très différents, avec l'amélioration de la recherche traduite immersive activée, nous recherchons automatiquement les mêmes mots-clés en anglais pour vous et les affichons sur le côté droit. Vous pouvez choisir de le désactiver si vous n'avez pas besoin de la fonctionnalité.
  - Safari n'est pas pris en charge en raison des limitations de l'API.

## 0.6.20

- Modification des paramètres par défaut : En raison d'un grand nombre de retours d'utilisateurs indiquant qu'ils n'utiliseront pas l'outil de traduction après l'installation, leur attente de l'outil de traduction est qu'il traduise automatiquement les pages web en anglais après l'installation, donc à partir de cette version, pour les utilisateurs chinois, l'option de traduction des pages en anglais par défaut a été activée (si l'utilisateur a déjà défini une langue qui sera toujours traduite, alors elle sera respectée, et le changement ne modifie que les paramètres initiaux de l'extension), et il doit être annulé, il peut être facilement annulé dans [Panneau contextuel ou page des paramètres](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- Correction des bugs PDF
- Correction du bug du web of science
- Adaptation feeder.com
- Correction de l'epub ne traduisant pas certains livres

## 0.6.18

- Correction du problème de débordement de la largeur du Popup Safari.
- Optimisation du processus de construction

## 0.6.17

- Optimisation des alertes d'erreur
- Optimisation de la sélection de la langue cible, maintenant elle n'affichera que les langues prises en charge par le service de traduction correspondant
- Optimisation de la traduction PDF
- Adapté pour le site Good Reads, le site Amazon et le site South China Morning Post

## 0.6.16

- Ajout de l'affichage de la page sans permission PDF
- Réparation de l'affichage des paragraphes de la liste de texte PDF
- Agrandissement de l'échelle des petites polices PDF sur chrome et safari

## 0.6.15

- Réparation du problème que lors de l'ouverture de fichiers PDF, le panneau d'extension indique qu'il n'y a pas de permissions.
- Correction du problème que l'amélioration de la boîte de saisie n'est pas activée lorsque le site est configuré pour ne jamais traduire.

## 0.6.14

- Optimisation de la traduction PDF, la zone de traduction peut maintenant être éditée/traînée/supprimée
  - Traîner en haut à gauche, supprimer en haut à droite, changer la taille en bas à droite
- Alignement à gauche de la boîte déroulante Windows
- Support du chinois traditionnel et du chinois simplifié

## 0.6.13

- Correction du problème de traduction répétée au survol de la souris
- Support de la traduction PDF pour traîner pour changer la taille et éditer le contenu de la traduction

## 0.6.12

- Correction des images de traduction Epub devenant plus petites dans certains navigateurs
- Optimisation de la traduction de la boîte de saisie, fonctionne maintenant sans problème dans Bard !

## 0.6.10

- Modèle par défaut OpenAI changé en version 0613
- Correction de certains styles de boîte de saisie
- Plus intelligent pour déterminer s'il s'agit d'une zone de navigation, et si c'est le cas, aucune traduction n'est effectuée
- Correction des attaques possibles par injection XSS

## 0.6.8

- Le panneau d'extension peut maintenant indiquer les pages non prises en charge (par exemple, les pages sans permissions et les pages non-HTML)
- Amélioration de la boîte de saisie pour afficher le statut de chargement dans la traduction
- Mise à jour des couleurs de chargement par défaut dans les traductions
- Lorsque la boîte de saisie est configurée sans préfixe, elle prend en charge la traduction `ja Hello` en japonais et `English Hello` en anglais.

## 0.6.6

- Correction pour : certaines zones ne se traduisant pas (quora)

## 0.6.5

- Optimisation de Google Bard
- La traduction de la boîte de saisie prend en charge la traduction directe de l'ensemble de la boîte de texte sans préfixes.
- Optimisation du problème des traductions OpenAI ajoutant des points de manière insensée, (si aucun point n'est détecté dans le texte original, si openai renvoie un point, alors le supprimer)
- Problèmes avec les fichiers de sous-titres safari non reconnus

## 0.6.3

La langue par défaut pour la traduction de la boîte de saisie peut maintenant omettre l'espace, c'est-à-dire que //Hello World peut également être traduit.

## 0.6.2

La plus excitante amélioration de la boîte de saisie est ici :

- Tapez : // Hello World dans la boîte de saisie sur n'importe quelle page web, puis triple-cliquez sur la barre d'espace pour traduire le paragraphe en anglais
- Vous pouvez également spécifier la traduction dans une certaine langue : /ja Hello World, puis triple-cliquez sur la barre d'espace pour traduire le paragraphe en japonais

[Cliquez ici pour une introduction rapide de 30 secondes](/docs/input/)

## 0.6.0

- Première version en juin, migrée de l'ancien sous-domaine personnel https://immersive-translate.owenyoung.com vers le nouveau domaine https://immersivetranslate.com/
- Les fonctionnalités sont largement inchangées (de nouvelles fonctionnalités seront disponibles dans la prochaine version !)

## 0.5.17

- Correction du problème que : les eBooks bilingues n'ont pas d'images après l'exportation

## 0.5.16

- Correction : problème de traduction openai en chinois traditionnel

## 0.5.15

- Optimisation : Le nombre minimum de caractères dans un paragraphe qui déclenche la traduction a été modifié à un minimum de 4 caractères pour réduire la confusion, tout en utilisant d'autres fonctionnalités pour éviter de traduire les zones de navigation et de fin du site.
- Correction : Détails Github non traduits après expansion.

## 0.5.14

- Correction du problème que les images sur certaines pages web de : deviennent plus grandes après copie
- Correction : section de commentaires medium non traduite
- Correction du problème que les images sur certaines pages de : étaient copiées incorrectement

## 0.5.12

- Fonctionnalité : Le style de traduction en ligne divisée ajoute une ligne de séparation verticale pour les traductions sur une seule ligne
- Correction : Cas très rares de division de paragraphes.
- Une excellente page d'orientation pour la première configuration pour les nouveaux utilisateurs iOS.

## 0.5.11

- Support de la traduction des sous-titres pour l'exportation des traductions uniquement
- Correction : Certains éléments ne sont pas reconnus par le survol de la souris
- Correction : les sauts de ligne partiels des tweets non reconnus
- Correction : le style de création d'eBook ne fonctionne pas

## 0.5.10

- Correction : les sauts de ligne des tweets non reconnus
- Correction : la page de détail Reddit renvoie certains paragraphes qui ne peuvent pas être traduits
- Correction d'un problème avec : où certaines balises de code n'étaient pas reconnues correctement.

## 0.5.9

- Correction des sauts de paragraphes dans certains cas à :
- Correction : Tampermonkey Toggle n'affiche que les traductions
- Correction : le style de lecture en ligne d'eBook ne fonctionne pas

## 0.5.8

- Correction du problème que : le réglage temporaire de la durée de traduction du site web n'a pas d'effet.

## 0.5.7

- Super mise à jour !

- La fonctionnalité "Afficher uniquement les traductions" est là ! Cliquez sur [Plus] -> [Basculer pour afficher uniquement les traductions].

  - Support des raccourcis personnalisés, à définir dans les paramètres d'interface -> Paramètres des raccourcis

- Optimisation du problème de limitation de fréquence des requêtes OpenAI

- ChatGPT par défaut sur le modèle mobile, qui est plus rapide !

- Réusinage de l'analyse du noyau web, ce qui signifie :

  - Traduction de pages web à grande échelle en quelques secondes
    - Par exemple, : https://pve.proxmox.com/pve-docs/pve-admin-guide.html, qui prenait 30 secondes auparavant, est maintenant retourné en quelques secondes.
  - Utilisation ultra-faible de la mémoire pour les pages web complexes
    - Par exemple : https://www\.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Adaptation à plus de sites web

- Toutes les traductions du site web de ShadowRoot sont prises en charge.

  - Par exemple : https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - Par exemple, la section des commentaires de : https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Correction du problème d'écran blanc après la traduction de sites web avec hydratation comme Next.js.

  - Par exemple : https://webpack.js.org/

- Correction du problème que la modification du raccourci de survol de la souris nécessitait de rafraîchir la page pour prendre effet

- Correction d'un problème de reconnaissance des sauts de ligne dans les fichiers TXT.

- Beaucoup de mises à jour !

- La fonctionnalité "Afficher uniquement les traductions" est arrivée ! Cliquez sur "Plus" -> "Basculer pour afficher uniquement les traductions".

  - Supporte les raccourcis personnalisés, qui peuvent être définis dans "Paramètres d'interface" -> "Paramètres des raccourcis"

- Optimisé pour le problème de limitation du taux de requêtes OpenAI

- L'analyse du noyau web a été reconstruite, ce qui signifie.

  - Traduction instantanée pour les grands sites web
  - Utilisation minimale de la mémoire pour les pages web complexes
  - Meilleure compatibilité avec plus de sites web

- Prend désormais en charge les traductions pour tous les sites web avec ShadowRoot.

- Correction du problème d'écran blanc après la traduction de sites web avec hydratation, comme Next.js

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

- Correction : paramètres des raccourcis de survol de la souris pour userscript

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
- Performance : Exclure certaines pages publicitaires enfant sur le site web, et la performance s'est un peu améliorée

## 0.4.7

- Correction : popup userscript Firefox manquant.

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
- Fonctionnalité : supporte le site web ChatGPT Plus comme service de traduction, c'est une fonctionnalité bêta, vous pouvez y accéder en activant la fonctionnalité bêta dans les paramètres développeur. C'est très lent, car chatgpt ne peut envoyer qu'une requête à la fois. Assurez-vous d'avoir un compte ChatGPT Plus, car il y a plus de limites sur le compte gratuit, et je ne suis pas sûr si cela présente un risque pour votre compte, soyez prudent pour Assurez-vous d'avoir un compte ChatGPT Plus, car il y a plus de limites sur le compte gratuit, et je ne suis pas sûr si cela présente un risque pour votre compte, soyez prudent pour l'utiliser.

## 0.4.1

- Correction : le menu contextuel de Firefox disparaît après redémarrage.
- Support Azure openai

## 0.4.0

- Fonctionnalité : Supporte la traduction de fichiers de sous-titres locaux (.srt, .ass, etc.)

## 0.3.17

- Fonctionnalité : Supporte la traduction de fichiers .txt locaux.
- Correction : Le menu contextuel peut ne pas être disponible parfois. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Correction : conserver &nbsp; comme espace blanc.
- Suppression : Retirer Papago, car [le service est en panne](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI : permettre l'absence de clé API pour openai
- UI : permettre à Open AI de réinitialiser aux paramètres par défaut

## 0.3.14

- Dépendance : Mettre à jour pdf.js vers la dernière version
- Correction : couleur de fond de sélection pdf
- Correction : détection d'espace blanc

## 0.3.13

- Correction : problème de caractère spécifique du constructeur d'eBook, comme certains chemins de chapitre sont `xxx' xxxx`.
- UI : plier les options personnalisées openai par défaut.
- UI : Ajouter un statut d'exportation pour l'exportation epub.
- Correction : invite par défaut Gpt4

## 0.3.12

- Fonctionnalité : Nous pouvons maintenant personnaliser la couleur de fond du thème de traduction Marker.
- Correction : postMessage lors de l'initialisation de la page a cassé certains sites, maintenant nous ne le ferons que lorsque nous traduisons vraiment des pages
- Correction : problème de progression d'eBook.
- Correction : meilleur pour diviser un long paragraphe, 1,5 milliard, 25,5 %, M. ne sera pas considéré comme une limite

## 0.3.11

- Correction : couleur du texte en mode sombre du lecteur d'eBook
- Correction : invite openAI

## 0.3.10

- Meilleur : détecter le conteneur japonais/coréen.
- Correction : Progression du constructeur d'eBook arrêtée à 99 %.

## 0.3.9

- Correction : l'état d'entrée des services de traduction de commutateur UI Options n'a pas changé.

## 0.3.8

- UI : couleur de chargement plus transparente
- Correction : Détecter la langue de l'eBook.
- Fonctionnalité : Ajouter une progression de traduction pour le constructeur d'eBook, et une belle confettis après succès.
- Fonctionnalité : Ajouter un bouton de réessai pour tous les paragraphes échoués.
- Correction : Gestion des erreurs Deepl

## 0.3.7

- Correction : le lecteur d'eBook ne peut pas charger les images sur Chrome.

## 0.3.6

- UI : meilleur pour faire l'UI de la page d'eBook

## 0.3.5

- Correction : exportation d'eBook userscript
- Fonctionnalité : ajouter un point de terminaison API personnalisé pour OpenAI
- Fonctionnalité : ajouter des options de temps de traduction temporaire du site web dans `Paramètres avancés`

## 0.3.4

- CI : Échec de la construction

## 0.3.3

- Correction : constructeur d'eBook pour Kindle
- Changement : couleur de l'icône de chargement, du noir au bleu, pour s'adapter à la page web en mode sombre.
- Fonctionnalité : Supporte la traduction html locale pour l'extension

## 0.3.2

- Correction : déplacement du curseur de saisie du formulaire d'options.
- Fonctionnalité : OpenAI supporte l'apiUrl personnalisé pour les paramètres de développement.

## 0.3.1

- Fonctionnalité : mise à jour de l'icône sombre à la transparence.
- Correction : Mauvais ordre pour long paragraphe

## 0.3.0

- Version : À partir de maintenant, nous changerons le numéro de version mineure une fois par mois, par exemple, maintenant en mars, la version commencera à partir de 0.3.0, en avril, le numéro de version commencera à partir de 0.3.0, en avril, le numéro de version commencera à partir de 0.4.0, l'année prochaine en avril, le numéro de version sera 1.4.0, et ainsi de suite. Cela est dû au fait qu'il n'est pas logique pour les extensions de suivre Cela est dû au fait qu'il n'est pas logique pour les extensions de suivre les sémantiques, mais la standardisation des numéros de version selon les lois du temps est une motivation pour le développement de continuer à se mettre à jour, et pour les utilisateurs de trouver plus facilement des problèmes.
- Fonctionnalité : Supporte l'icône sombre pour Firefox

## 0.2.86

- Ajouter une option de longueur de texte maximale par requête avec Open AI
- Correction : identifiant d'eBook dupliqué
- Fonctionnalité : Supporte la traduction de page web txt

## 0.2.85

- Correction : certains fichiers epub ne peuvent pas être trouvés.

## 0.2.84

- Fonctionnalité : Supporte le lecteur et le créateur d'eBook

## 0.2.83

- Fonctionnalité : Permettre au formulaire de saisie de mot de passe d'afficher le mot de passe.

## 0.2.82

## 0.2.81

- Fix : m.youtube.com
- Fix : options form UI
- Fix : Open AI prompt
- Feat : Support OpenAI multiple keys, use `,` pour les séparer.

## 0.2.80

- Feat : Ajouter le menu Activer/Désactiver pour le popup -> plus
- Fix : Conflit de message DingTalk

## 0.2.79

- Fix : Open AI pour le paragraphe d'espace

## 0.2.78

- Feat : support OpenAI CHATGPT 3.5 (supporte l'interface OpenAI ChatGPT 3.5)
- Feat : Ajouter un nouveau thème Solid Border (nouveau thème ajouté, bordure pleine)

## 0.2.77

- Fix : erreur de balise de code multiple.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Fix : erreur de balise de code multiple [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Feat : Supporter le nombre de textes de traduction immédiate personnalisée pour différents services de traduction.

## 0.2.74

- Feat : Supporter Tencent (alpha)
- Fix : traduction openai
- Fix : vérification des balises inconnues en ligne

## 0.2.73

- Feat : Supporter le thème de traduction gris
- Fix : Page des tendances Github

## 0.2.72

- Fix : problème de réseau de vérification du service de traduction sur Firefox mobile.

## 0.2.71

- Fix : permission du userscript Open AI

## 0.2.70

- Fix : espace réservé Open AI

## 0.2.69

- Feat : Supporter Open AI en tant que service de traduction.
- Feat : Supporter la vérification du service de traduction sur options.html
- Feat : Supporter le cadre principal personnalisé car certains sites n'utilisent pas le corps comme cadre principal

## 0.2.68

- Supporter Caiyun (Alpha)
- Fix balises de bloc inconnues

## 0.2.67

- Feat : Ajouter `<all>` pour toujours traduire les langues, vous pouvez maintenant l'utiliser pour traduire toutes les langues sauf la langue cible, et ne jamais traduire les langues
- Fix : Permettre la configuration de l'API Google personnalisée
- Mieux : Support gratuit de Deepl
- Fix : utilisation élevée de la mémoire pour les userscripts et les extensions (en supprimant opencc zh-CN à zh-TW, à la place avec Google translate)
- Fix : Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Fix : configuration de la traduction Azure mais toujours affichée (besoin de configuration)

## 0.2.66

- Fix : échec de la traduction de fichiers PDF, bug de la version 0.2.60 pour le support de deepl de zh-CN à zh-TW

## 0.2.65

- Supporter la limitation des requêtes pour plusieurs cadres
- Ne pas traduire le titre de la page lorsqu'il est dans un iframe

## 0.2.64

- Fix : choisir les services de traduction openl
- Feat : Supporter l'option de traduction du titre

## 0.2.63

- Feat : Supporter le service de traduction Azure
- Feat : Supporter le service de traduction Papago
- Fix : synchronisation native de Google Drive sur Firefox Android.
- Fix : changer la transparence de 0.4 à 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Fix : conseils de raccourcis popup
- Performance : requêtes en série à concurrence
- Mieux pour détecter le nombre de japonais

## 0.2.62

- Feat : Ajouter la règle waitForSelectors, pour corriger certains sites comme reddit

## 0.2.61

- Fix : userscript est trop grand pour greasy fork
- Mieux : réduire la taille du fichier

## 0.2.60

- Feat : Supporter zh-CN à zh-TW pour Deepl
- Feat : Fonctionnalité Immersive Translate Deepl
- Feat : Supporter le zoom de la taille de police personnalisée
- Fix : style du forum Steam
- Fix : le style global ne change pas après la génération d'éléments dynamiques
- Fix : promouvoir la priorité d'exclusion
- UI : changement de la page à propos
- Fix : certains éléments mathématiques restent originaux

## 0.2.59

- Fix : Élément de bloc de balises inconnues
- Fix : élément translate=no override
- Fix : correspondance d'URL avec plusieurs \*

## 0.2.58

- Feat : Supporter la couleur de texte de traduction personnalisée, la couleur de la bordure.

## 0.2.57

- Pas de changements, reconstruire

## 0.2.56

- Fix traduction en double pour les éléments en ligne avec élément de code.
- Fix vérification des balises inconnues en ligne/bloc
- Feat : support css injecté sur le tableau de bord des développeurs
- Feat : réduire authKey, appid appSecret
- Mieux : ouvrir la page des paramètres dans un nouvel onglet (mais pas pour Stay)

## 0.2.55

- Essayer de corriger le charset de l'API deepl

## 0.2.54

- Supprimer la permission des onglets pour le rejet du Chrome Store
- Fix traduire toute la page, le pied de page est ignoré
- Ajouter des notes à la page à propos
- Supporter l'URL personnalisée à partir de la configuration intégrée

## 0.2.53

- Fix erreur de synchronisation de Google Drive pour userscript.

## 0.2.52

### Code

- Utiliser la dernière version d'esbuild
- Utiliser la dernière version de deno
- CI : soumettre le code source à Firefox

## 0.2.51

- Fix Google Auth besoin de connexion sur Chrome/Firefox
- Remplacer les liens de service de traduction
- Mieux pour la permission.
- supprimer la minification.

## 0.2.50

- Fix problème de téléchargement de Google Drive (vraiment) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Supprimer les raccourcis alt+d, alt+s car ils peuvent entrer en conflit avec les raccourcis natifs.
- Fix problème de téléchargement de Google Drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Mieux pour la vitesse, en ajoutant minLength à 50 pour la détection de la langue.
- Fix validation du jeton Google Drive.

## 0.2.47

- Fix API deepl

## 0.2.46

- corriger le marquage de bloc

## 0.2.45

- Fix innerText de l'élément est indéfini
- Fix traduction caiyun langue source indéfinie

## 0.2.44

- Fix bascule du masque userscript
- Fix logique de bascule du masque

## 0.2.43

- Fix bascule du masque userscript avec événement tactile.
- Fix vitesse (en supprimant sleep(300))

## 0.2.42

- Fix survol du masque lors de la bascule du masque à nouveau.
- Ajouter des raccourcis de masque pour mobile
- Fix problème de synchronisation cloud userscript
- Déplacer la page des options avancées vers le menu de gauche.
- Ajouter une logique de réessai au service de traduction

## 0.2.41

- Fix traduction niu userscript
- Fix traduction xhtml

## 0.2.40

- Fix affichage de la fonctionnalité bêta
- Fix page de paramètres popup sur la nouvelle page d'onglet
- Fix remplacement de l'espace réservé de traduction

## 0.2.39

- Supporter les raccourcis pour afficher la traduction du masque
- Supporter l'activation de la fonctionnalité bêta au panneau de développement
- Fix raccourcis dans l'extension mobile

## 0.2.38

- Supporter le thème de chargement
- Fix getpocket.com
- Fix pied de page pour la zone du corps
- Fix icône d'import/export

## 0.2.37

- Fix marquage d'exclusion de cadre

## 0.2.36

- Supporter la synchronisation avec Google Drive

## 0.2.35

- Fix balise japonaise rb, rt ignorée.
- Mieux pour l'interface utilisateur du popup plus
- Mieux pour les conseils de mauvais userscript
- Ajouter une contribution à la page à propos
- Fix traduction volc pour la détection automatique de la langue

## 0.2.34

- Fix vitesse de traduction de plusieurs langues

## 0.2.33

- Supporter le mode d'écriture vertical, comme le japonais.
- Ajouter 3 thèmes
- Ajouter le service de traduction Niu

## 0.2.32

- Fix traduction de base de PDF
- Fix sélection de service non configuré dans le popup, aller à la page des options.
- Fix rester ouvert les paramètres.
- Fix vitesse de détection de plusieurs langues

## 0.2.31

- Fix injection css iframe dynamique

## 0.2.30

- Supporter la traduction d'iframe en ligne userscript.
- Supporter la traduction shadowroot. Par exemple :
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Zone de conversation.
- vérifier également la règle de synchronisation sur le popup

## 0.2.29

- Fix traduction Facebook
- Supporter l'affichage de l'option du menu contextuel.

## 0.2.28

- Supprimer la correspondance non standard pour userscript

## 0.2.27

- Supporter la traduction d'iframe en ligne. (Seulement pour l'extension, non disponible pour
  userscript)
- Fix traduction de plusieurs langues

## 0.2.26

- Fix addon Firefox Android
- Ajouter des paramètres avancés pour la nouvelle ligne de traduction

## 0.2.25

- Supporter la traduction d'iframe, comme le courrier QQ, tweet intégré.

## 0.2.24

- Ajouter un site de traduction temporaire pour un moment
- Fix API du navigateur userscript stay.app
- Fix page des options stay.app

## 0.2.23

- Fix traduction de page de plusieurs langues

## 0.2.22

- Fix build userscript

## 0.2.21

- Fix traduction de PDF en ligne sur Firefox

## 0.2.20

- Fix problème de requête macaque
- Fix marquage de ligne de surbrillance

## 0.2.19

- Fix japonais intelligent tencent
- Fix navigateur haikuo world

## 0.2.18

- Fix changement d'URL client, rester automatiquement dans l'état de traduction.
- Supprimer le conteneur latéral comme conteneur de traduction.
- Réorganiser la position du popup.

## 0.2.17

- Changer la surbrillance en marquage
- Ajouter un thème de traduction en surbrillance

## 0.2.16

- Compatibilité Macaque

## 0.2.15

- Fix problème de rebond tactile

## 0.2.14

- Fix safari globalThis.GM ne fonctionne pas

## 0.2.13

- Supporter le glissement du popup Userscript
- Supporter trois doigts sur l'appareil tactile pour déclencher la bascule des pages de traduction
- Supporter la dissimulation de l'icône du popup userscript.

## 0.2.12

- Mieux pour inoreader

## 0.2.11

- Correction de
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas archive Le contenu principal de la page n'a pas pu être traduit

## 0.2.10

- Correction de la distance de hauteur de ligne dans les fichiers PDF

## 0.2.9

- Correction de l'exclusion des éléments marqués
- Correction de la vérification des types Deno
- Suppression de l'importmap
- Correction de la traduction des menus contextuels
- Restauration de la page lorsque l'option "ne jamais traduire ce site" est activée
- Ajout d'une description pour l'ajout d'URL

## 0.2.8

- Détection de la langue de l'agent utilisateur pour la langue de l'interface
- Correction du bug de saut de ligne

## 0.2.7

- Correction de la requête Grease Monkey

## 0.2.6

- Correction de
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  problème de correspondance des URL de fichiers

## 0.2.5

- Augmentation de la version pour le test CI

## 0.2.4

- Capture de l'erreur de connexion de message pour le popup

## 0.2.3

- Correction de
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  création de contexte multiple

## 0.2.2

- Correction du fichier PDF d'exemple
- Correction du fichier local PDF sur Firefox
- Correction des raccourcis PDF

## 0.2.1

- Support du gestionnaire de raccourcis Grease Monkey
- Correction de la correspondance regex
- Correction des commentaires YouTube
- Correction de la version mobile compacte de Reddit
- Correction du problème de traduction en texte intégral

## 0.2.0

- Correction des PDF à deux colonnes
- Correction du bug de la version Chrome/Edge Store
- Correction de
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Publication sur l'addon Firefox
- Publication sur Edge
- Correction de la marge PDF
- Changement du fichier PDF d'exemple

## 0.0.62

- Correction du format PDF, indentation
- Correction de la prévention des changements d'éléments sur telegra.ph

## 0.0.61

- Correction de la fermeture de l'élément span
- Correction des permissions pour les navigateurs anciens

## 0.0.60

- Correction du PDF sur Chrome

## 0.0.59

- Support initial pour PDF

## 0.0.58

- Modification de la description du thème de traduction

## 0.0.57

- Changement de l'interface utilisateur du popup, pour une utilisation plus facile

## 0.0.56

- Correction du timeout sur Chrome
- Correction de l'erreur de séparation des phrases

## 0.0.55

- Correction de l'affichage des éléments avec display none
- Refactorisation du marquage des éléments

## 0.0.54

- Support du saut de ligne pour X caractères

## 0.0.53

- Utilisation de sendMessage au lieu de connect, car Chrome déconnecte le port après
  5 minutes
- Meilleure détection des conteneurs de texte

## 0.0.52

- Ne pas traduire le paragraphe qui ne contient que des éléments de remplacement, par
  [exemple](https://github.com/nank1ro/solidart), la première ligne
- Meilleure détection des éléments enfants

## 0.0.51

- Correction du problème de cache
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7)
- Correction de la taille de la police de l'interface utilisateur des options

## 0.0.50

- Correction de la traduction des images en bloc

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

- Utilisation d'un seul fichier pour le userscript
- Ajout d'un timeout pour la requête de cache

## 0.0.44

- Correction de l'erreur de séparation Tencent
- Correction de l'erreur de l'élément sup en ligne
- Amélioration pour Twitter

## 0.0.43

- Correction du saut de ligne dans les tweets
- Correction de la traduction globale

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

- Correction du changement de service de traduction dans le popup
- Correction de la traduction du contenu des publications mobiles Reddit

## 0.0.36

- Correction des caractères spéciaux de Wikipedia
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Correction de la taille de l'icône du userscript
- Activation de la détection de la langue des paragraphes sur tous les sites

## 0.0.35

- Correction de la navigation vers la page suivante sur YouTube
- Support de la page de recherche YouTube
- Correction de l'interrupteur avancé des options
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

- La touche de raccourci par défaut pour basculer la traduction a été changée en `alt+A`, car c'est la touche la plus pratique à taper.

### Autres

- Support du mode de traduction immédiate, pour que vous puissiez laisser la page web se traduire aussi rapidement que possible.
- Support de la définition de la zone de la page à traduire, pour que vous puissiez traduire plus de zones.
- Support de la définition du nombre de premiers caractères à traduire immédiatement.
- Correction de la traduction en double lors du changement de traduction
- Meilleure interface utilisateur du popup

## 0.0.33

- Support de plus de langues, zh-TW, en

## 0.0.32

- Correction de la traduction du fichier local après enregistrement. Correction de
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Ajout du fichier dist js au dépôt public

## 0.0.31

- Support de la traduction de la page entière
- Support de la traduction immédiate de la page
- Plus d'interface utilisateur de configuration
- Réflexion du thème
- Ajout d'une nouvelle icône
- Ajout d'un nouveau thème de traduction dashedBorder

## 0.0.30

- Amélioration pour le thème en pointillés

## 0.0.29

- Correction de la validité des paragraphes
- Ajout des thèmes dotted, thinDashed
- Amélioration pour les thèmes en pointillés, surlignés

## 0.0.28

- Correction du soulignement
- Ajout des thèmes en pointillés, papier
- Correction de la détection des en-têtes

## 0.0.27

- Support du translationTheme

## 0.0.26

- Correction de la permission de connexion du userscript volc alpha
- Correction de la version cliquable

## 0.0.25

- Support de selectorMatches, pour que nous puissions maintenant correspondre à tous les manstondon
- Correction de l'erreur du userscript Firefox

## 0.0.23

- Amélioration pour la détection du chinois
- Correction du problème innerText de Reddit

## 0.0.22

- Support de deeplx
- Correction de la traduction multiple lors du changement de service

## 0.0.21

- Correction de certains tags span qui sont des éléments de bloc

## 0.0.20

- Support de la non-traduction des hashtags comme #hash, des tags at comme @xxx, $tag, comme $APPL
- Support des éléments de bloc

## 0.0.18

- Support de deepl, bing, baidu, youdao, volc, openl, caiyun

## 0.0.13

- Support du userscript

## 0.0.4.8

- Correction de l'ordre du code
- Support de l'interface utilisateur de base du popup

## 0.0.4.6

- Support de la vérification de nouvelle version

## 0.0.3

- Support des fichiers locaux

## 0.0.2

- Support des éléments dynamiques
- Support de la traduction visible