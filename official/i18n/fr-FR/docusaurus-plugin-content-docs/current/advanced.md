---
sidebar_position: 4
---

# Options avancées de personnalisation

Cette page s'adresse aux utilisateurs avancés ayant des connaissances en HTML/CSS/JSON. La configuration avancée permet une grande capacité d'adaptation, mais il est également plus facile d’écrire une configuration "apparemment correcte mais qui ne fonctionne pas". Sauvegardez vos réglages avant toute modification.

## Conseils avant utilisation

- Le point d'entrée se trouve dans les [Paramètres développeur](https://dash.immersivetranslate.com/#developer).
- Sauvegardez d’abord User Config / User Rules pour éviter la perte en cas d’erreur de format.
- Pour la configuration finale intégrée, fiez-vous au bouton « Click to expand the final config » (champs, valeurs par défaut, services disponibles).

## Points d'entrée et priorité

Points d'entrée habituels (Paramètres développeur) :
- Edit Full User Config : configuration complète (inclut `rules`, services de traduction, styles, etc.).
- Edit User Rules : ne modifie que le tableau `rules` (n'accepte qu'un tableau, sans `{ "rules": [...] }`).
- Injected CSS : injection CSS globale.

Ordre de priorité (du plus élevé au plus faible) : règle trouvée dans `rules` > `generalRule` > configuration par défaut intégrée.
Quand une `rule` correspond, elle est fusionnée avec `generalRule`, les champs de la `rule` priment.

## Démarrage rapide (besoins courants)

### 1) Traduire uniquement le contenu d'un site

```json
{
  "rules": [
    {
      "matches": ["example.com"],
      "selectors": ["article", ".post-content"],
      "excludeSelectors": ["nav", "footer", ".comment"]
    }
  ]
}
```

### 2) Toujours traduire / Ne jamais traduire

```json
{
  "translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
  }
}
```

### 3) Utiliser différents services par site

```json
{
  "translationService": "google",
  "translationServices": {
    "deepl": {
      "matches": ["sci-hub.se"]
    }
  }
}
```

### 4) Styles différents selon le site

```json
{
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  }
}
```

### 5) Traduction déforme le style, appliquer un correctif CSS

```json
{
  "rules": [
    {
      "matches": ["youtube.com"],
      "globalStyles": {
        "#video-title": "max-height:unset;"
      }
    }
  ]
}
```

### 6) Ne pas afficher les services non configurés dans le panneau

```json
{
  "showUnconfiguredTranslationServiceInPopup": false
}
```

## Règles et correspondances

### Fusion des règles

- `generalRule` : base des règles communes à tous les sites.
- `rules` : règles spécifiques au site, priorité la plus haute en cas de correspondance.

Les champs de `rules` peuvent utiliser la plupart de ceux disponibles dans `generalRule`.

### Formes courantes de matches

`matches` accepte une chaîne ou un tableau :
- Nom de domaine : `example.com`
- URL complète : `https://example.com/path/`
- Joker : `https://*/*q=*`
- Pour tout : `*` / `*://*` / `*://*/*`
- Fichier local : `file://*`

Attention : `*.twitter.com` ne correspond qu’aux sous-domaines, pas au domaine racine `twitter.com`.

### selectors / excludeSelectors

- `selectors` : ne traduire que les éléments correspondant (écrase la plage par défaut).
- `excludeSelectors` : exclure ces éléments de la traduction.

Si vous voulez simplement « ajouter/retirer » sur la plage originale, privilégiez `.add` / `.remove` (voir ci-dessous).

### Héritage et modification incrémentale (.add / .remove)

Pour les champs tableaux ou objets, `.add` / `.remove` permettent une édition incrémentale.
Privilégiez cette méthode pour éviter d’écraser les règles par défaut :

```json
[
  {
    "id": "twitter",
    "selectors.add": ["[data-testid='tweetText'] a"],
    "excludeSelectors.add": ["header"]
  }
]
```

### Répertoire des champs courants (extrait)

Correspondance :
- `matches` / `excludeMatches`
- `selectorMatches` / `excludeSelectorMatches`

Plage de traduction :
- `selectors` / `excludeSelectors` / `excludeTags`
- `stayOriginalSelectors` / `stayOriginalTags`
- `extraInlineSelectors` / `extraBlockSelectors`

Style et mise en page :
- `translationClasses` : classes supplémentaires appliquées à la traduction
- `globalStyles` / `globalAttributes`
- `injectedCss` / `additionalInjectedCss`
- `wrapperPrefix` / `wrapperSuffix`
- `blockMinTextCount` / `blockMinWordCount`

Timing et mobile :
- `urlChangeDelay` / `observeUrlChange`
- `isShowUserscriptPagePopup`

### Traduction de messages stream façon GPT

```json
{
  "matches": ["chat.openai.com"],
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

Pour plus de détails champ par champ, voir l’annexe « Référence du champ Rule » en fin de page.

## Logique de correspondance de matches (résumé)

- Domaine simple (pas de `*` ni de chemin) : compare simplement le hostname.
- URL complète (sans `*`) : compare protocole + hôte + port + chemin.
- Avec `*` ou sans protocole : correspondance par wildcard (http/https/file pris en charge par défaut).

Exemples courants :
- `twitter.com` ✅ correspond à `https://twitter.com/home`
- `*.twitter.com` ✅ correspond à `https://mobile.twitter.com`, ❌ ne correspond pas à `https://twitter.com`
- `https://twitter.com/home` ne correspond qu’à cette URL exacte
- `twitter.com/*` correspond à tous les chemins sous `twitter.com`

## Exemple d’adaptation de site (Twitter)

Voici un extrait de la règle Twitter intégrée pour illustrer l’usage typique de `selectors` / `excludeSelectors` / `globalStyles` :

```json
[
  {
    "id": "twitter",
    "matches": [
      "twitter.com",
      "mobile.twitter.com",
      "tweetdeck.twitter.com",
      "pro.twitter.com",
      "https://platform.twitter.com/embed*"
    ],
    "selectors": [
      "[data-testid=\"tweetText\"]",
      ".tweet-text",
      ".js-quoted-tweet-text",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
      "[data-testid='developerBuiltCardContainer'] > div:nth-child(2)",
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)",
      "[data-testid='cellInnerDiv'] div[data-testid='UserCell'] > div> div:nth-child(2)",
      "[data-testid='UserDescription']",
      "[data-testid='HoverCard'] div[dir=auto]",
      "[data-testid='HoverCard'] span[dir=auto]",
      "[data-testid='HoverCard'] [role='dialog'] div[dir=ltr]",
      "[data-testid='birdwatch-pivot'] div[dir=ltr]"
    ],
    "excludeSelectors": [
      "[aria-describedby][role=button]",
      "header",
      "[data-testid='radioGroupplayback_rate'] div",
      "[data-testid='userFollowIndicator']",
      "[class='css-901oao r-14j79pv r-37j5jr r-n6v787 r-16dba41 r-1cwl3u0 r-bcqeeo r-qvutc0']",
      "[class='css-175oi2r r-1wbh5a2 r-dnmrzs']"
    ],
    "globalStyles": {
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  }
]
```

- `selectors` : traduit uniquement le contenu principal comme le texte des tweets, évite d’altérer pseudo et boutons.
  ![tweet](https://s.immersivetranslate.com/assets/r2-uploads/tweet.png)
- `excludeSelectors` : exclut les boutons, menus, éléments d’interaction.
  ![twitter-follow](https://s.immersivetranslate.com/assets/r2-uploads/twitter-follow.png)
- `globalStyles` : retire la limitation de lignes pour que la traduction ne soit pas tronquée.
  ![用户主页](https://s.immersivetranslate.com/assets/r2-uploads/twitterUser.png)

## Adapter un site personnalisé

Pour réutiliser une règle intégrée (`id`) et faire une modification incrémentale avec `.add`/`.remove` :

```json
[
  {
    "id": "twitter",
    "selectors.remove": ["[data-testid=\"tweetText\"]"],
    "selectors.add": ["[data-testid=\"tweetText\"] a"],
    "excludeSelectors.add": ["header"],
    "excludeSelectors.remove": []
  }
]
```

Explications :
- L’`id` permet d’hériter de la règle sans réécrire `matches`.
- `.add`/`.remove` modifie les tableaux sans écraser la règle, à privilégier.

Exemples d'`id` intégrés courants :
- `isEbook` : liseuse epub
- `isEbookBuilder` : générateur epub bilingue
- `pdf` : page PDF bilingue

Règles intégrées complètes :
- `https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json`

## Configuration du service de traduction

- `translationService` : moteur de traduction par défaut.
- `translationServices` : configuration des services avec surcharge possible par site.
- `showUnconfiguredTranslationServiceInPopup` : cacher les services non configurés.

Exemple (Tencent) :

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["twitter.com"],
      "limit": 3,
      "maxTextGroupLengthPerRequest": 25,
      "maxTextLengthPerRequest": 1800,
      "apiUrl": ""
    }
  }
}
```

Détails :
- `matches` restreint ce service à certains sites.
- `limit` : quota de requêtes par seconde.
- `maxTextGroupLengthPerRequest` / `maxTextLengthPerRequest` : taille max de requête.
- `apiUrl` : URL personnalisable du service.

### Délai maximum par requête

Chaque service accepte une configuration de timeout (en ms). Pour les services *Pro*, utilisez `proRequestTimeout`.

```json
{
  "translationServices": {
    "openai": {
      "requestTimeout": 60000
    },
    "gemini": {
      "proRequestTimeout": 90000
    }
  }
}
```

Conseils :
- Une durée trop longue = attente longue ; trop courte = erreurs fréquentes.
- La valeur par défaut dépend du service, voir la config finale.
- `proRequestTimeout` n’est utilisé que si `provider` est `pro` (service abonné).

## Langues et stratégies de traduction

### Toujours/ne jamais traduire certaines langues

```json
{
  "translationLanguagePattern": {
    "matches": ["en"],
    "excludeMatches": ["zh"]
  }
}
```

### Forcer une langue source par site

```json
{
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  }
}
```

## Autres options globales courantes

### Autoriser le rendu de balises HTML dans la traduction

Activez ceci si vous voulez que les balises HTML soient rendues dans la traduction :

```json
{
  "enableRenderHtmlTag": true
}
```

## Styles de traduction et thèmes

Styles valides pour `translationTheme` (se référer à la config finale) :

```text
none, grey, dashed, dashedBorder, solidBorder, dotted, underline, mask, opacity,
paper, dividingLine, highlight, marker, marker2, blockquote, weakening, italic,
bold, thinDashed, nativeDotted, wavy, nativeDashed, nativeUnderline, background
```

Style par site :

```json
{
  "translationThemePatterns": {
    "highlight": {
      "matches": ["discord.com"]
    }
  }
}
```

## Paramètres IA / avancés

### temperature

```json
{
  "translationServices": {
    "openai": {
      "temperature": 0.2
    }
  }
}
```

### Personnaliser headers et corps de requête

```json
{
  "translationServices": {
    "claude": {
      "headerConfigs": {
        "anthropic-version": "2023-06-01",
        "anthropic-dangerous-direct-browser-access": "true"
      },
      "bodyConfigs": {
        "max_tokens": 2048
      }
    }
  }
}
```

### Personnalisation pour la famille Gemini

Gemini dispose de paramètres par défaut. Pour les écraser, utilisez `modelsOverrides` selon le nom du modèle :

```json
{
  "translationServices": {
    "gemini": {
      "modelsOverrides": [
        {
          "models": ["gemini-2.5-flash", "gemini-2.5-flash-lite"],
          "bodyConfigs": {
            "temperature": 0.1
          }
        }
      ]
    }
  }
}
```

Note : `modelsOverrides` fonctionne aussi avec d’autres IA – le nom du modèle fait foi pour la surcharge.

### Respect strict des prompts personnalisés

> Pour réduire les hallucinations, le plugin intègre un mécanisme de vérification de qualité. Le système compare le nombre de tokens entre demande et réponse pour juger de la pertinence de la traduction. Si le ratio est anormal, le résultat est ignoré au profit d’une alternative.
> Si votre prompt personnalisé ne concerne pas la traduction (ex : reformulation, amélioration de texte), ce ratio peut être hors-norme. Activez alors le mode strict pour désactiver la vérification.

```json
{
  "translationServices": {
    "claude": {
      "strictPrompt": true
    }
  }
}
```

### Prompts multilingues personnalisés (exemple)

```json
{
  "translationServices": {
    "openai": {
      "langOverrides": [
        {
          "id": "auto2ja",
          "systemPrompt": "あなたはプロの翻訳エンジンです。",
          "prompt": "次のテキストを{{to}}に翻訳してください：\n\n<text>\n{{text}}\n</text>",
          "multiplePrompt": "<yaml>\n{{yaml}}\n</yaml>",
          "subtitlePrompt": "<yaml_subtitles>\n{{yaml}}\n</yaml_subtitles>"
        }
      ]
    }
  }
}
```

## Glossaire et traduction automatique

Nouveau : [Glossaire IA](https://dash.immersivetranslate.com/#terms), fonctionne seulement avec les IA.

Par défaut, la TA n’utilise pas le glossaire — elle utilise en général des remplacements par placeholder, ce qui peut nuire à la qualité. Pour l’activer (déconseillé) :

```json
{
  "enableMachineTranslateTerms": true
}
```

## Durée de vie du cache

Le plugin nettoie son cache de traductions automatiquement tous les 30 jours pour prévenir toute perte de performance.

```json
{
  "cacheMaxAgeDay": 30
}
```

## Injected CSS et globalStyles

- Injected CSS : injection CSS globale, utile pour corriger tout un site.
- globalStyles : styles appliqués par règle, pour la correction par site.

Exemple d’Injected CSS :

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

## Dépannage et pièges fréquents

- `*.twitter.com` n’inclut pas le domaine racine — listez aussi `twitter.com`.
- `selectors` écrase la plage par défaut, utilisez plutôt `.add`/`.remove` si besoin.
- Mettre `example.com/path` dans `matches` active le mode wildcard — précisez si vous voulez matcher l’URL complète.
- Si la configuration ne marche pas : vérifiez la config finale puis rechargez la page.
- Une virgule en trop à la fin du JSON rend la configuration invalide.

## Annexe : Référence des champs Rule

Voici la référence des principaux champs Rule (documentée ci-dessous). Pour la liste complète/à jour, voyez la config finale.
Astuce : pour tableau et objets, utilisez `.add`/`.remove` pour ne pas écraser les règles par défaut.

```typescript
export interface Rule {
  // Correspondance de site
  id?: string; // ID d'une règle intégrée, à utiliser pour l’héritage
  matches?: string | string[]; // Correspond uniquement à ce(s) site(s)
  excludeMatches?: string | string[]; // Exclure certains sites
  selectorMatches?: string | string[]; // Correspondance par sélecteur
  excludeSelectorMatches?: string | string[]; // Exclure via sélecteur, même syntaxe

  // Cible de traduction
  selectors?: string | string[]; // Eléments à traduire uniquement
  excludeSelectors?: string | string[]; // Eléments à exclure de la traduction
  excludeTags?: string | string[]; // Tags à exclure

  // Ajouts supplémentaires (si non fonctionnel, utilisez selectors.add / selectors.remove)
  additionalSelectors?: string | string[]; // Ajouter à la cible de traduction
  additionalExcludeSelectors?: string | string[]; // Ajouter à l'exclusion
  additionalExcludeTags?: string | string[]; // Exclusion supplémentaire de tags (obsolète dans certaines versions)

  // Rester à l’original
  stayOriginalSelectors?: string | string[]; // Ces éléments restent inchangés
  stayOriginalTags?: string | string[]; // Ces tags restent inchangés (ex : code)

  // Block ou Inline
  extraBlockSelectors?: string | string[]; // Ces éléments sont traités comme des block
  extraInlineSelectors?: string | string[]; // Ces éléments sont traités comme des inline
  inlineTags?: string | string[]; // Ces tags sont traités comme inline
  preWhitespaceDetectedTags?: string | string[]; // Ces tags forcent un retour à la ligne

  // Styles de traduction
  translationClasses?: string | string[]; // Class CSS supplémentaire

  // Styles globaux
  globalStyles?: Record<string, string>; // Modifier les styles de la page
  globalAttributes?: Record<string, Record<string, string | null>>; // Modifier les attributs d’un élément

  // CSS intégré
  injectedCss?: string | string[]; // CSS intégré
  additionalInjectedCss?: string | string[]; // CSS supplémentaire à intégrer

  // Contexte
  wrapperPrefix?: string; // Préfixe du bloc de traduction
  wrapperSuffix?: string; // Suffixe du bloc de traduction

  // Nombre de caractères avant saut de ligne
  blockMinTextCount?: number; // Min caractères pour block
  blockMinWordCount?: number; // Min mots pour block

  // Taille minimale pour traduire
  containerMinTextCount?: number; // Minimum de caractères du conteneur
  paragraphMinTextCount?: number; // Minimum de caractères du paragraphe
  paragraphMinWordCount?: number; // Minimum de mots du paragraphe

  // Découpage fort pour paragraphes longs
  lineBreakMaxTextCount?: number; // Max de caractères avant saut forcé

  // Timing de lancement
  urlChangeDelay?: number; // Délai après chargement de la page
  observeUrlChange?: boolean; // Traduire à chaque changement d’URL

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Afficher le popup flottant sur mobile
  fingerCountToToggleTranslagePageWhenTouching?: number; // Obsolète

  // Traduction IA en streaming
  aiRule?: {
    streamingSelector: string; // Sélecteur de l’élément courant à traduire
    messageWrapperSelector: string; // Sélecteur du message principal
    streamingChange: boolean; // Mode incrémental
  };
}
```
