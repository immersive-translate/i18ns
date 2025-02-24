---
sidebar_position: 5
---

# JS SDK

Le JS SDK d'Immersive Translate peut vous aider à implémenter une traduction bilingue sur votre site web.

## Comment l'utiliser

> Avant de déboguer le JS SDK, veuillez désactiver l'extension Immersive Translate

1. Configurez les paramètres d'initialisation (veuillez noter que si immersiveTranslateConfig n'est pas défini, l'initialisation du JS SDK échouera, vous pouvez définir un objet vide)

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. Ajoutez le code `script` suivant avant `</head>` de votre page web

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
```

Exemple

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Immersive Translate JS SDK</title>
    <script>
      window.immersiveTranslateConfig = {
        pageRule: {},
      };
    </script>
    <script
      async
      src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
    ></script>
  </head>
  <body>
    <div class=".text">
      <p>
        Night gathers, and now my watch begins. It shall not end until my death.
        I shall take no wife, hold no lands, father no children. I shall wear no
        crowns and win no glory. I shall live and die at my post.
      </p>
    </div>
  </body>
</html>
```

## Paramètres

- `pageRule`
  Vous pouvez configurer le site web de manière personnalisée pour décider quels contenus doivent être traduits ou ajuster le style de la page web, etc.
- `isAutoTranslate`
  Traduction automatique immédiate

```html
<script>
  window.immersiveTranslateConfig = {
    isAutoTranslate: true,
    pageRule: {
      selectors: [".text"],
      excludeSelectors: ["nav", "footer"],
    },
  };
</script>
```

L'utilisation de `selectors` couvrira la portée de la traduction intelligente, ne traduisant que les éléments correspondant à ce sélecteur.

L'utilisation de `excludeSelectors` permet d'exclure des éléments, ne traduisant pas cet emplacement.

L'utilisation de `selectors.add` ajoutera certains sélecteurs sur la base par défaut.

L'utilisation de `selectors.remove` réduira certains sélecteurs sur la base par défaut.

Si vous souhaitez traduire une zone en considérant l'élément comme un tout, sans le diviser en lignes, vous pouvez utiliser le sélecteur `atomicBlockSelectors`. Notez que, avant d'utiliser `atomicBlockSelectors`, vous devez d'abord sélectionner avec `selectors`.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Plus d'explications sur les paramètres `pageRule` :

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Exclure des sites web spécifiques.
  selectorMatches?: string | string[]; // Utiliser un sélecteur pour correspondre, sans avoir à spécifier toutes les URL.
  excludeSelectorMatches?: string | string[]; // Règles d'exclusion, comme ci-dessus.


```markdown
  // Plage de traduction spécifiée
  selectors?: string | string[]; // Traduire uniquement les éléments correspondants
  excludeSelectors?: string | string[]; // Exclure les éléments, ne pas traduire les éléments correspondants
  excludeTags?: string | string[]; // Exclure les Tags, ne pas traduire les Tags correspondants

  // Ajouter une plage de traduction, au lieu de remplacer
  additionalSelectors?: string | string[]; // Ajouter une plage de traduction. Dans la zone de traduction intelligente, ajouter une position de traduction.
  additionalExcludeSelectors?: string | string[]; // Ajouter des éléments à exclure, pour que la traduction intelligente ne traduise pas des positions spécifiques.
  additionalExcludeTags?: string | string[]; // Ajouter des Tags à exclure

  // Conserver tel quel
  stayOriginalSelectors?: string | string[]; // Les éléments correspondants resteront tels quels. Souvent utilisé pour les tags des sites de forum.
  stayOriginalTags?: string | string[]; // Les Tags correspondants resteront tels quels, par exemple `code`

  // Traduction de zone
  atomicBlockSelectors?: string | string[]; // Sélecteurs de zone, les éléments correspondants seront considérés comme un tout, sans traduction segmentée
  atomicBlockTags?: string | string[]; // Sélecteurs de Tags de zone, idem

  // Block ou Inline
  extraBlockSelectors?: string | string[]; // Sélecteurs supplémentaires, les éléments correspondants seront traités comme des éléments block, occupant une ligne entière.
  extraInlineSelectors?: string | string[]; // Sélecteurs supplémentaires, les éléments correspondants seront traités comme des éléments inline.

  inlineTags?: string | string[]; // Les Tags correspondants seront traités comme des éléments inline
  preWhitespaceDetectedTags?: string | string[]; // Les Tags correspondants seront automatiquement mis à la ligne

  // Style de traduction
  translationClasses?: string | string | string[]; // Ajouter des classes supplémentaires à la traduction

  // Styles globaux
  globalStyles?: Record<string, string>; // Modifier le style de la page, utile si la traduction perturbe la mise en page.
  globalAttributes?: Record<string, Record<string, string>>; // Modifier les attributs des éléments de la page

  // Style intégré
  injectedCss?: string | string[]; // CSS intégré
  additionalInjectedCss?: string | string[]; // Ajouter du CSS, au lieu de remplacer directement.

  // Contexte
  wrapperPrefix?: string; // Préfixe de la zone de traduction, par défaut smart, décide de l'ajout d'une nouvelle ligne selon le nombre de mots.
  wrapperSuffix?: string; // Suffixe de la zone de traduction

  // Nombre de caractères pour le retour à la ligne de la traduction
  blockMinTextCount?: number; // Nombre minimum de caractères pour que la traduction soit considérée comme un block, sinon elle sera un élément inline.
  blockMinWordCount?: number; // Idem. Si vous souhaitez qu'ils soient toujours à la ligne, vous pouvez mettre 0.

  // Nombre minimum de caractères pour que le contenu soit traduisible
  containerMinTextCount?: number; // Lors de la reconnaissance intelligente, le nombre minimum de caractères que doit contenir un élément pour être traduit, par défaut 18
  paragraphMinTextCount?: number; // Nombre minimum de caractères d'un paragraphe original, le contenu supérieur à ce nombre sera traduit
  paragraphMinWordCount?: number; // Nombre minimum de mots d'un paragraphe original

  // Nombre de caractères pour forcer le retour à la ligne des longs paragraphes
  lineBreakMaxTextCount?: number; // Lors de la traduction de longs paragraphes, nombre maximum de caractères pour forcer le retour à la ligne.
```

```markdown
// Moment de démarrage de la traduction
urlChangeDelay?: number; // Combien de millisecondes après l'entrée sur la page pour commencer la traduction. Pour attendre l'initialisation de la page, la valeur par défaut est actuellement de 250ms

// Traduction AI streaming
aiRule: {
  streamingSelector: string; // Sélecteur pour marquer l'élément en cours de traduction sur la page gpt
  messageWrapperSelector: string; // Sélecteur du corps du message
  streamingChange: boolean; // Les messages répétés sur la page gpt sont-ils des mises à jour incrémentielles ou complètes. gpt est incrémentiel
};
```
