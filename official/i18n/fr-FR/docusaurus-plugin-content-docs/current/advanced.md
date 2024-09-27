---
sidebar_position: 4
---

# Options de personnalisation avancées

Vous pouvez modifier des configurations plus personnalisées dans la Page de Configuration Étendue -> Paramètres Développeur -> Config Utilisateur qui ne sont pas modifiables dans l'UI pour les utilisateurs avancés, voir la dernière note pour plus de détails sur les paramètres. La `config` intégrée actuelle peut être trouvée [ici](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

## Règles Utilisateur

Avec `Règles`, il est possible de personnaliser la configuration d'un site web particulier, en décidant quel contenu doit être traduit ou non, ou en ajustant le style des pages, etc.

```json
[
  {
    "matches": "www.google.com",
    "selectors": [".title"]
  },
  {
    "matches": "*.twitter.com",
    "selectors": [".text"],
    "excludeSelectors": ["nav", " footer"]
  }
]
```

Utilisez `matches` pour correspondre au site web concerné. Les caractères génériques sont autorisés, par ex. `*.google.com`, `www.google.com/test/*`, `file://*`.

Utiliser `selectors` remplace le champ de traduction intelligent, en traduisant uniquement les éléments correspondant à ce sélecteur.

Utilisez `excludeSelectors` pour exclure des éléments sans traduire la position.

Utilisez la famille de sélecteurs `additional` pour augmenter ou diminuer la portée de la traduction basée sur la traduction intelligente.

```json
[
  {
    "matches": "www.google.com",
    "additionalSelectors": [],
    "additionalExcludeSelectors": []
  }
]
```

Si vous souhaitez traduire une région en traitant les éléments comme un tout et non en les séparant, vous pouvez utiliser le sélecteur `atomicBlockSelectors`. Par exemple, les profils Instagram. Notez que l'utilisation de `atomicBlockSelectors` nécessite de sélectionner avec `selectors` avant d'utiliser `atomicBlockSelectors`.

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Si la traduction entraîne des pages mal alignées, du texte qui se chevauche et d'autres cas limites, vous pouvez utiliser `globalStyles` pour ajuster le style de la page afin de corriger cela. Par exemple, l'en-tête de YouTube, qui est utilisé pour supprimer la hauteur maximale de la page originale.

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## Améliorations de la consolidation des règles utilisateur

Support à partir de la version 0.7.4. Prenons l'exemple de l'omission de la zone sans traduction

```json
{
  "matches": "https://www.elektrotechnik.rwth-aachen.de/*",
  "additionalExcludeSelectors.remove": [".notranslate", "[translate=no]"]
}
```

Les opérations d'ajout et de suppression modifient les règles fournies par défaut et ne nécessitent pas d'être remplacées dans leur intégralité, comme c'était le cas auparavant.

## CSS injecté

Le CSS injecté vous permet d'injecter des styles web personnalisés globalement. Peut être utilisé avec `translationClasses` des `Rules`.

```
".immersive-translate-target-wrapper img { width: 16px; height: 16px }"
```

Il est également possible de personnaliser le style du site de manière plus personnalisée, comme un gestionnaire de style web régulier. (en utilisant même `display:none` pour supprimer les publicités)

```css
.title {
  color: red;
}
```

## Configuration Utilisateur

La configuration vous permet de personnaliser la configuration de ce plugin, telles que les services de traduction, les options de traduction de langue spécifiques à une langue, etc.

```json
{
  "serviceDeTraduction": "tencent",
  "servicesDeTraduction": {
    "tencent": {
      "idSecret": "xxx",
      "cleSecret": "xxx",
      "correspondances": ["*.twitter.com"]
    }
  },
  "modeleUrlDeTraduction": {
    "exclureCorrespondances": ["www.google.com"]
  },
  "modeleLangueDeTraduction": {
    "correspondances": ["fr"]
  },
  "themeDeTraduction": "aucun",
  "modelesThemeDeTraduction": {
    "soulignement": {
      "correspondances": ["discord.com"]
    }
  },
  "regleGenerale": {
    "_commentaire": "",
    "normaliserCorps": "",
    "cssInjecte": [],
    "cssInjecteSupplementaire": [],
    "prefixeConteneur": "intelligent",
    "suffixeConteneur": "intelligent",
    "estPdf": false,
    "transformerSautLignePreTag": false,
    "delaiChangementUrl": 20,
    "afficherPopupPageUserscript": true,
    "observerChangementUrl": true,
    "minTexteParagraphe": 8,
    "minMotsParagraphe": 2,
    "minTexteBloc": 32,
    "minMotsBloc": 5,
    "minTexteConteneur": 18,
    "maxTexteSautLigne": 0,
    "attributsGlobaux": {},
    "stylesGlobaux": {},
    "selecteurs": [],
    "balisesDetectionEspacePre": ["DIV", "SPAN"],
    "selecteursOriginaux": [],
    "selecteursSupplementaires": [],
    "balisesBlocAtomiques": [],
    "exclureSelecteurs": [],
    "selecteursExclusSupplementaires": [],
    "classesDeTraduction": [],
    "selecteursBlocAtomiques": [],
    "exclureBalises": [],
    "metaBalises": ["META", "SCRIPT", "STYLE", "NOSCRIPT"],
    "balisesExcluesSupplementaires": [],
    "balisesOriginales": ["CODE", "TT", "IMG", "SUP"],
    "balisesOriginalesSupplementaires": [],
    "balisesEnLigne": [],
    "balisesEnLigneSupplementaires": [],
    "selecteursEnLigneSupplementaires": [],
    "selecteursBlocSupplementaires": [],
    "toutesLesBalisesBloc": [],
    "interligneNouveauParagraphePdf": 2.4,
    "indentationNouveauParagraphePdf": 1.2,
    "indentationDroiteNouveauParagraphePdfPx": 130,
    "nombreDoigtsBasculerPageTraductionTactile": 4
  },
  "regles": [
    {
      "correspondances": "www.google.com",
      "selecteurs": [".classe"]
    }
  ]
}
```

Les champs de règle dans `regles` peuvent utiliser tous les champs dans `regleGenerale`. Les `regles` ont la priorité la plus élevée, fusionnant la `regleGenerale` et les règles pour cette `regle` lorsqu'une `regle` particulière pour un site particulier est correspondante.

Introduction de certains champs communs de Config.

### Ne pas afficher les services de traduction non configurés dans le panneau popup

`"showUnconfiguredTranslationServiceInPopup": false`

### Configuration des services de traduction

Utilisez `translationService` pour sélectionner le moteur de traduction par défaut, qui prend actuellement en charge :

```typescript
| "tencent"
| "google"
| "deepl"
| "baidu"
| "volc"
| "youdao"
| "caiyun"
| "openl"
| "bing"
| "transmart"
```

Utilisez `translationServices` pour configurer la `apikey` de chaque service de traduction, différents fournisseurs de services nécessitent différents paramètres, et leurs clés API peuvent être demandées dans le centre de développeurs de leurs sites web respectifs.

Par exemple, pour le Traducteur Tencent, vous devez configurer `secretId`, `secretKey`. Vous pouvez vous rendre sur Tencent Cloud pour demander une clé API avec 5 millions de caractères gratuits par mois. Référez-vous [ici](/docs/services/tencent) pour le processus de demande.

```json
"translationServices": {
  "tencent": {
    "secretId": "xxx",
    "secretKey": "xxx",
    "matches":["*.twitter.com"],
    "limit": 3,
    "apiUrl":"",
    " maxTextGroupLengthPerRequest": 25,
    "maxTextLengthPerRequest": 1800
  }
}
```

Champ `matches`, utilisant ce service de traduction pour un site web spécifique.

Le champ `limit`, qui spécifie le nombre maximum de demandes par seconde pour ce service de traduction (certains services limitent le nombre maximum de demandes par seconde).

Champ `maxTextGroupLengthPerRequest`, nombre maximum de paragraphes par demande

Champ `maxTextLengthPerRequest`, nombre maximum de caractères par demande

`apiUrl` Vous permet de personnaliser l'adresse de l'interface de traduction.

### Toujours traduire des sites web spécifiques

`translationUrlPattern` Configure les sites qui sont toujours traduits, et les sites qui ne le sont jamais.

- `matches` la configuration traduit toujours le site.
- `excludeMatches` Configure les sites qui ne sont jamais traduits.

Les valeurs de configuration peuvent être des noms de domaine ou des URL avec `*`, tel que : `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### Toujours traduire des langues spécifiques

translationLanguagePattern, configure la langue qui est toujours traduite et la langue qui ne l'est jamais.

- `matches` Configure la langue qui est toujours traduite, par ex. `en`,
- `excludeMatches` Configure les langues qui ne sont jamais traduites.

### Format d'affichage de la traduction

`translationTheme` est le format d'affichage de la traduction, et prend actuellement en charge les styles suivants :

```typescript
| "none"
| "dashed"
| "dotted"
| "underline"
| "mask"
| "paper"
| "highlight"
| "blockquote"
| "weakening"
| "italic"
| "bold"
| "thinDashed".
```

Nom correspondant en français :

```json
{
  "none": "aucun",
  "dashed": "tireté",
  "dotted": "pointillé",
  "underline": "souligné",
  "mask": "effet de flou",
  "paper": "effet d'ombre de papier blanc",
  "highlight": "surlignage",
  "blockquote": "style de citation",
  "weakening": "affaiblissement",
  "italic": "italique",
  "bold": "gras",
  "thinDashed": "souligné en pointillés fins"
}
```

`translationThemePatterns` vous permet de configurer différents styles de traduction pour différents sites web.

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### Traduction de message de flux de page de classe gpt

```json
{
  "matches": ["chat.openai.com"],
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown ",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

### Règles

`rules` est un objet tableau qui vous permet de configurer des règles pour des sites spéciaux, comme avoir Twitter pour traduire seulement une certaine partie d'une région :

```json
{
  "rules": [
    {
      "id": "twitter",
      "matches": ["twitter.com", "mobile.twitter.com", "tweetdeck.twitter.com"],
      "selectors": [
        "[data-testid='tweetText']",
        ".tweet-text",
        ".js-quoted-tweet-text",
        "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
        "[data-testid='developerBuiltCardContainer'] > div:nth-child(2)",
        "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)"
      ],
      "extraInlineSelectors": ["[data-testid=\"tweetText\"] div"]
    }
  ]
}
```

Les `rules` intégrées actuelles peuvent être trouvées [ici](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

Certains des champs importants sont sélectionnés ci-dessous pour illustration：

```typescript
export interface Rule {
  // Correspond au site web
  id?: string; // Chaque règle d'adaptation a son propre id, si les utilisateurs veulent réutiliser cette règle en plus de ce changement, ils doivent ajouter cet id correspondant à leur propre règle pour la réutiliser
  matches?: string | string[]; // Cette règle ne correspondra qu'au site web ici. Cette règle ne correspondra qu'aux sites ici.
  excludeMatches?: string | string[]; // Exclure des sites spécifiques.
  selectorMatches?: string | string[]; // Correspondre avec un sélecteur sans spécifier tous les urls
  excludeSelectorMatches?: string | string[]; // Exclure des règles, comme ci-dessus.

  // Spécifier la portée des traductions
  selectors?: string | string[]; // Traduire uniquement les éléments qui correspondent
  excludeSelectors?: string | string[]; // Exclure des éléments, ne pas traduire les correspondances
  excludeTags?: string | string[]; // Exclure des Tags, ne pas traduire les Tags correspondants

  // ajouter des plages de traduction au lieu de remplacer
  additionalSelectors?: string | string[]; // ajouter des plages de traduction. Ajouter des emplacements de traduction aux régions traduites intelligemment.
  additionalExcludeSelectors?: string | string[]; // Ajouter des éléments exclus pour que la traduction intelligente ne traduise pas des emplacements spécifiques.
  additionalExcludeTags?: string | string[]; // Tags exclus supplémentaires

  // Laisser tel quel
  stayOriginalSelectors?: string | string[]; // Les éléments correspondants seront laissés tels quels. Communément utilisé dans les tags de sites de forums.
  stayOriginalTags?: string | string[]; // Les tags correspondants seront laissés tels quels, par exemple `code`

  // Traductions régionales
  atomicBlockSelectors?: string | string[]; // Sélecteurs régionaux, les éléments correspondants seront traités comme un tout, pas traduits en sections.
  atomicBlockTags?: string | string[]; // Sélecteurs de Tags de zone, identique ci-dessus

  // Bloc ou En ligne
  extraBlockSelectors?: string | string[]; // Sélecteurs supplémentaires, les éléments correspondants seront traités comme des éléments de bloc, non traduits en une seule ligne.
  extraInlineSelectors?: string | string[]; // Sélecteurs supplémentaires qui seront utilisés comme éléments en ligne.

  inlineTags?: string | string[]; // Le tag correspondant sera utilisé comme un élément en ligne
  preWhitespaceDetectedTags?: string | string[]; // Le tag correspondant sera automatiquement encapsulé

  // Style de traduction
  translationClasses?: string | string | string[]; // Ajouter des classes supplémentaires à la traduction

  // Styles globaux
  globalStyles?: Record<string, string>; // Modifier les styles de la page, utile si la traduction cause un désordre sur la page.
  globalAttributes?: Record<string, Record<string, string>>; // Modifier les attributs des éléments de la page

  // Styles intégrés
  injectedCss?: string | string[]; // Intégrer des styles CSS
  additionalInjectedCss?: string | string[]; // Styles CSS supplémentaires au lieu de les remplacer.

  // Contexte
  wrapperPrefix?: string; // Le préfixe de la zone de traduction, par défaut intelligent, avec ou sans sauts de ligne en fonction du nombre de caractères.
  wrapperSuffix?: string; // Suffixe de la zone de traduction

  // Nombre de caractères pour encapsuler la traduction
  blockMinTextCount?: number; // Nombre minimum de caractères pour encapsuler la traduction en tant que bloc, sinon la traduction est un élément en ligne.
  blockMinWordCount?: number; // Idem ci-dessus. Si vous voulez qu'ils soient toujours à la ligne, vous pouvez mettre 0 dans les deux.

  // Nombre minimum de caractères pouvant être traduits du contenu
  containerMinTextCount?: number; // Nombre minimum de caractères qu'un élément doit contenir avant qu'il ne soit traduit, par défaut à 18
  paragraphMinTextCount?: number; // Nombre minimum de caractères pour le paragraphe, supérieur au nombre de caractères que le contenu doit contenir. number, tout ce qui est plus grand que cela sera traduit
  paragraphMinWordCount?: number; // Nombre minimum de mots dans le paragraphe original

  // Sauts de ligne forcés pour les longs paragraphes
  lineBreakMaxTextCount?: number; // Nombre maximum de caractères dans le paragraphe pour être forcé de sauter une ligne lors de la traduction d'un long paragraphe.

  // Quand commencer la traduction.
  urlChangeDelay?: number; // Combien de millisecondes retarder la traduction après être entré sur la page. Pour attendre que la page s'initialise, cela par défaut à 250ms
  observeUrlChange?: boolean; // Détecter quand l'adresse url a changé et recommencer la traduction, vrai par défaut.

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Afficher le popup de la page sur les appareils mobiles. fenêtre flottante, vrai par défaut.
  fingerCountToToggleTranslagePageWhenTouching?: number; // Traduit lorsque quatre doigts touchent, peut être réglé sur 0, 2, 3, 4, 5

  // Traductions en streaming AI
  aiRule: {
    streamingSelector: string; // Sélecteur pour marquer l'élément en cours de traduction dans la page web gpt
    messageWrapperSelector: string; // Sélecteur du corps du message
    streamingChange: boolean; // Si le message est mis à jour de manière incrémentielle ou complète pour l'itération de la page web de classe gpt. gpt est incrémentiel
  };
}
```

**Plus d'explications**

Différence entre bloc et en ligne, si vous voulez en savoir plus, vous pouvez voir [ici](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline)

- L'élément de bloc occupe une seule ligne, et plusieurs éléments de bloc voisins occupent chacun une nouvelle ligne.
- L'élément en ligne n'occupe pas une seule ligne ; plusieurs éléments en ligne voisins sont disposés sur la même ligne, et une nouvelle ligne n'est pas créée jusqu'à ce qu'une ligne soit trop chargée.
