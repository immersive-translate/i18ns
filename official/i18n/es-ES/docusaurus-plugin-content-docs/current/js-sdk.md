---
sidebar_position: 5
---

# JS SDK

El Immersive Translate JS SDK te ayuda a implementar traducción bilingüe en tu sitio web.

## Cómo Usar

1. Inicializa Immersive Translate:

```js
<script>
  window.immersiveTranslateConfig = {
    pageRule: {}
  }
</script>
```

2. Añade el siguiente código `script` a tu página web

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
```

Ejemplo

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

## Parámetros

Con `pageRule`, puedes personalizar la configuración del sitio web, decidiendo qué contenido necesita ser traducido o ajustando los estilos de la página web.

```js
initImmersiveTranslate({
  pageRule: {
    selectors: [".text"],
    excludeSelectors: ["nav", "footer"],
  },
});
```

Usar `selectors` sobrescribirá el rango de traducción inteligente, traduciendo solo los elementos que coincidan con el selector.

Usar `excludeSelectors` puede excluir elementos de la traducción.

Usar `selectors.add` añadirá algunos selectores además de los predeterminados.

Usar `selectors.remove` eliminará algunos selectores de los predeterminados.

Si deseas traducir un área específica y considerar un elemento como un todo sin dividirlo en líneas, puedes usar el selector `atomicBlockSelectors`. Ten en cuenta que necesitas seleccionar elementos usando `selectors` antes de usar `atomicBlockSelectors`.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Más explicaciones de parámetros de `pageRule`:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Excluir sitios web específicos.
  selectorMatches?: string | string[]; // Coincidir usando selectores sin especificar todas las URLs
  excludeSelectorMatches?: string | string[]; // Excluir reglas, igual que arriba.

  // Especificar rango de traducción
  selectors?: string | string[]; // Traducir solo elementos coincidentes
  excludeSelectors?: string | string[]; // Excluir elementos, no traducir elementos coincidentes
  excludeTags?: string | string[]; // Excluir etiquetas, no traducir etiquetas coincidentes

  // Añadir rango de traducción, no sobrescribir
  additionalSelectors?: string | string[]; // Añadir rango de traducción. Añadir posiciones de traducción en áreas de traducción inteligente.
  additionalExcludeSelectors?: string | string[]; // Añadir elementos excluidos para prevenir traducción inteligente en posiciones específicas.
  additionalExcludeTags?: string | string[]; // Añadir etiquetas excluidas

  // Mantener original
  stayOriginalSelectors?: string | string[]; // Elementos coincidentes permanecerán originales. Comúnmente usado para etiquetas en sitios web de foros.
  stayOriginalTags?: string | string[]; // Etiquetas coincidentes permanecerán originales, como `code`

  // Traducción de región
  atomicBlockSelectors?: string | string[]; // Selector de región, elementos coincidentes serán considerados como un todo, no traducidos en segmentos
  atomicBlockTags?: string | string[]; // Selector de etiqueta de región, igual que arriba

  // Bloque o Inline
  extraBlockSelectors?: string | string[]; // Selectores extra, elementos coincidentes serán tratados como elementos de bloque, ocupando una línea.
  extraInlineSelectors?: string | string[]; // Selectores extra, elementos coincidentes serán tratados como elementos en línea.

  inlineTags?: string | string[]; // Etiquetas coincidentes serán tratadas como elementos en línea
  preWhitespaceDetectedTags?: string | string[]; // Etiquetas coincidentes envolverán líneas automáticamente

  // Estilos de traducción
  translationClasses?: string | string | string[]; // Añadir clases extra a la traducción

  // Estilos globales
  globalStyles?: Record<string, string>; // Modificar estilos de página, útil cuando las traducciones causan desorden en la página.
  globalAttributes?: Record<string, Record<string, string>>; // Modificar atributos de elementos de la página

  // Estilos embebidos
  injectedCss?: string | string[]; // Incrustar estilos CSS
  additionalInjectedCss?: string | string[]; // Añadir estilos CSS en lugar de sobrescribir directamente.

  // Contexto
  wrapperPrefix?: string; // Prefijo del área de traducción, por defecto es inteligente, decide si envolver líneas basado en el número de caracteres.
  wrapperSuffix?: string; // Sufijo del área de traducción

  // Conteo de caracteres para envolver traducción
  blockMinTextCount?: number; // Conteo mínimo de caracteres para traducción como bloque, de lo contrario, la traducción será un elemento en línea.
  blockMinWordCount?: number; // Igual que arriba. Para envolver líneas siempre, establece ambos en 0.

  // Conteo mínimo de caracteres para contenido traducible
  containerMinTextCount?: number; // Conteo mínimo de caracteres para que los elementos sean traducidos durante el reconocimiento inteligente, por defecto es 18
  paragraphMinTextCount?: number; // Conteo mínimo de caracteres para párrafo original, contenido mayor que el número será traducido
  paragraphMinWordCount?: number; // Conteo mínimo de palabras para párrafo original

  // Conteo de caracteres para salto de línea forzado en párrafos largos
  lineBreakMaxTextCount?: number; // Conteo máximo de caracteres para salto de línea forzado al traducir párrafos largos.

  // Momento para iniciar la traducción
  urlChangeDelay?: number; // Retraso en milisegundos antes de iniciar la traducción después de entrar en la página. Por defecto es 250ms para esperar la inicialización de la página web.

  // Traducción en streaming de AI
  aiRule: {
    streamingSelector: string; // Selector de página web GPT marcando el elemento en traducción
    messageWrapperSelector: string; // Selector del cuerpo del mensaje
    streamingChange: boolean; // Actualización incremental o completa para mensajes repetidos en páginas web tipo GPT. GPT es incremental
  };
}
```