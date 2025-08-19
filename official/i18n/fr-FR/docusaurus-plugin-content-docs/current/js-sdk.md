---
sidebar_position: 5
---

# JS SDK

Le SDK Immersive Translate JS vous aide à implémenter la traduction bilingue sur votre site web.

## Comment Utiliser

1. Initialisez Immersive Translate :

```js
<script>
  window.immersiveTranslateConfig = {
    pageRule: {}
  }
</script>
```

2. Ajoutez le code `script` suivant à votre page web

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
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
    <div>
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

Avec `pageRule`, vous pouvez personnaliser la configuration du site web, décider quel contenu doit être traduit ou ajuster les styles de la page web.

```js
initImmersiveTranslate({
  pageRule: {
    selectors: [".text"],
    excludeSelectors: ["nav", "footer"],
  },
});
```

L'utilisation de `selectors` remplacera la plage de traduction intelligente, ne traduisant que les éléments correspondant au sélecteur.

L'utilisation de `excludeSelectors` peut exclure des éléments de la traduction.

L'utilisation de `selectors.add` ajoutera certains sélecteurs en plus de ceux par défaut.

L'utilisation de `selectors.remove` supprimera certains sélecteurs de ceux par défaut.

Explications supplémentaires des paramètres `pageRule` :

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Exclure des sites web spécifiques.
  selectorMatches?: string | string[]; // Correspondre en utilisant des sélecteurs sans spécifier toutes les URL
  excludeSelectorMatches?: string | string[]; // Exclure des règles, comme ci-dessus.

  // Spécifier la plage de traduction
  selectors?: string | string[]; // Traduire uniquement les éléments correspondants
  excludeSelectors?: string | string[]; // Exclure des éléments, ne pas traduire les éléments correspondants
  excludeTags?: string | string[]; // Exclure des balises, ne pas traduire les balises correspondantes

  // Ajouter une plage de traduction, ne pas remplacer
  additionalSelectors?: string | string[]; // Ajouter une plage de traduction. Ajouter des positions de traduction dans les zones de traduction intelligente.
  additionalExcludeSelectors?: string | string[]; // Ajouter des éléments exclus pour empêcher la traduction intelligente à des positions spécifiques.
  additionalExcludeTags?: string | string[]; // Ajouter des balises exclues

  // Conserver l'original
  stayOriginalSelectors?: string | string[]; // Les éléments correspondants resteront originaux. Couramment utilisé pour les balises sur les sites de forum.
  stayOriginalTags?: string | string[]; // Les balises correspondantes resteront originales, comme `code`

  // Bloc ou Inline
  extraBlockSelectors?: string | string[]; // Sélecteurs supplémentaires, les éléments correspondants seront traités comme des éléments de bloc, occupant une ligne.
  extraInlineSelectors?: string | string[]; // Sélecteurs supplémentaires, les éléments correspondants seront traités comme des éléments en ligne.

  inlineTags?: string | string[]; // Les balises correspondantes seront traitées comme des éléments en ligne
  preWhitespaceDetectedTags?: string | string[]; // Les balises correspondantes envelopperont automatiquement les lignes

  // Styles de traduction
  translationClasses?: string | string | string[]; // Ajouter des classes supplémentaires à la traduction

  // Styles globaux
  globalStyles?: Record<string, string>; // Modifier les styles de la page, utile lorsque les traductions causent un désordre de la page.
  globalAttributes?: Record<string, Record<string, string>>; // Modifier les attributs des éléments de la page

  // Styles intégrés
  injectedCss?: string | string[]; // Intégrer des styles CSS
  additionalInjectedCss?: string | string[]; // Ajouter des styles CSS au lieu de remplacer directement.

  // Contexte
  wrapperPrefix?: string; // Préfixe de la zone de traduction, par défaut est intelligent, décide d'envelopper les lignes en fonction du nombre de caractères.
  wrapperSuffix?: string; // Suffixe de la zone de traduction

  // Nombre de caractères d'enveloppement de traduction
  blockMinTextCount?: number; // Nombre minimum de caractères pour la traduction en tant que bloc, sinon, la traduction sera un élément en ligne.
  blockMinWordCount?: number; // Comme ci-dessus. Pour toujours envelopper les lignes, réglez les deux à 0.

  // Nombre minimum de caractères pour le contenu traduisible
  containerMinTextCount?: number; // Nombre minimum de caractères pour que les éléments soient traduits lors de la reconnaissance intelligente, par défaut est 18
  paragraphMinTextCount?: number; // Nombre minimum de caractères pour le paragraphe original, le contenu supérieur au nombre sera traduit
  paragraphMinWordCount?: number; // Nombre minimum de mots pour le paragraphe original

  // Nombre de caractères de saut de ligne forcé pour les longs paragraphes
  lineBreakMaxTextCount?: number; // Nombre maximum de caractères pour le saut de ligne forcé lors de la traduction de longs paragraphes.

  // Moment pour commencer la traduction
  urlChangeDelay?: number; // Délai en millisecondes avant de commencer la traduction après être entré sur la page. Par défaut est 250ms pour attendre l'initialisation de la page web.

  // Traduction en streaming AI
  aiRule: {
    streamingSelector: string; // Sélecteur de page web GPT marquant l'élément en cours de traduction
    messageWrapperSelector: string; // Sélecteur de corps de message
    streamingChange: boolean; // Mise à jour incrémentielle ou complète pour les messages répétés dans les pages web de type GPT. GPT est incrémentiel
  };
}
```
