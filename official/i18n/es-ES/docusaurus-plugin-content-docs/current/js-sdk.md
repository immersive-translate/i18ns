---
sidebar_position: 5
---

# JS SDK

El JS SDK de Immersive Translate puede ayudarte a implementar traducción bilingüe en tu sitio web.

## Cómo usar

> Antes de depurar el JS SDK, asegúrate de desactivar la extensión de Immersive Translate

1. Configura los parámetros de inicialización (ten en cuenta que si no configuras immersiveTranslateConfig, la inicialización del JS SDK fallará, puedes configurarlo como un objeto vacío)

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. Añade el siguiente código `script` antes de `</head>` en tu página web

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
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

## Parámetros

- `pageRule`
  Permite configurar el sitio web de manera personalizada, decidiendo qué contenido debe ser traducido o ajustando el estilo de la página.
- `isAutoTranslate`
  Traducción automática inmediata

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

Usar `selectors` sobrescribirá el rango de traducción inteligente, traduciendo solo los elementos que coincidan con ese selector.

Usar `excludeSelectors` permite excluir elementos, no traduciendo esa ubicación.

Usar `selectors.add` añadirá algunos selectores sobre la base predeterminada.

Usar `selectors.remove` reducirá algunos selectores sobre la base predeterminada.

Si deseas traducir una área específica tratando el elemento como un todo, sin dividirlo en líneas, puedes usar el selector `atomicBlockSelectors`. Es importante notar que antes de usar `atomicBlockSelectors`, debes seleccionar con `selectors`.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Más detalles sobre los parámetros de `pageRule`:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Excluir sitios web específicos.
  selectorMatches?: string | string[]; // Coincidir usando selectores, sin necesidad de especificar todas las URL.
  excludeSelectorMatches?: string | string[]; // Reglas de exclusión, igual que arriba.

```markdown
  // Rango de traducción especificado
  selectors?: string | string[]; // Solo traducir los elementos coincidentes
  excludeSelectors?: string | string[]; // Excluir elementos, no traducir los elementos coincidentes
  excludeTags?: string | string[]; // Excluir Tags, no traducir los Tags coincidentes

  // Añadir rango de traducción, en lugar de sobrescribir
  additionalSelectors?: string | string[]; // Añadir rango de traducción. En el área de traducción inteligente, añadir posición de traducción.
  additionalExcludeSelectors?: string | string[]; // Añadir elementos excluidos, para que la traducción inteligente no traduzca en posiciones específicas.
  additionalExcludeTags?: string | string[]; // Añadir Tags excluidos

  // Mantener original
  stayOriginalSelectors?: string | string[]; // Los elementos coincidentes se mantendrán originales. Comúnmente usado para etiquetas de sitios web de foros.
  stayOriginalTags?: string | string[]; // Los Tags coincidentes se mantendrán originales, como `code`

  // Traducción de área
  atomicBlockSelectors?: string | string[]; // Selector de área, los elementos coincidentes se tratarán como un todo, no se traducirán por partes
  atomicBlockTags?: string | string[]; // Selector de Tags de área, igual que arriba

  // Bloque o Inline
  extraBlockSelectors?: string | string[]; // Selectores adicionales, los elementos coincidentes se tratarán como elementos de bloque, ocupando una línea completa.
  extraInlineSelectors?: string | string[]; // Selectores adicionales, los elementos coincidentes se tratarán como elementos en línea.

  inlineTags?: string | string[]; // Los Tags coincidentes se tratarán como elementos en línea
  preWhitespaceDetectedTags?: string | string[]; // Los Tags coincidentes se detectarán automáticamente para el salto de línea

  // Estilo de traducción
  translationClasses?: string | string | string[]; // Añadir clases adicionales a la traducción

  // Estilo global
  globalStyles?: Record<string, string>; // Modificar el estilo de la página, útil si la traducción causa desorden en la página.
  globalAttributes?: Record<string, Record<string, string>>; // Modificar los atributos de los elementos de la página

  // CSS incrustado
  injectedCss?: string | string[]; // CSS incrustado
  additionalInjectedCss?: string | string[]; // Añadir CSS en lugar de sobrescribir directamente.

  // Contexto
  wrapperPrefix?: string; // Prefijo del área de traducción, por defecto es smart, decide si hacer un salto de línea según el número de palabras.
  wrapperSuffix?: string; // Sufijo del área de traducción

  // Número de caracteres para el salto de línea de la traducción
  blockMinTextCount?: number; // Número mínimo de caracteres para tratar la traducción como un bloque, de lo contrario, la traducción será un elemento en línea.
  blockMinWordCount?: number; // Igual que arriba. Si desea que siempre haya un salto de línea, puede establecer ambos en 0.

  // Número mínimo de caracteres traducibles en el contenido
  containerMinTextCount?: number; // En reconocimiento inteligente, el número mínimo de caracteres que debe contener un elemento para ser traducido, por defecto es 18
  paragraphMinTextCount?: number; // Número mínimo de caracteres en el párrafo original, el contenido mayor que este número será traducido
  paragraphMinWordCount?: number; // Número mínimo de palabras en el párrafo original

  // Número de caracteres para forzar el salto de línea en párrafos largos
  lineBreakMaxTextCount?: number; // Al traducir párrafos largos, el número máximo de caracteres del párrafo para forzar el salto de línea.
```

```markdown
// Momento para iniciar la traducción
urlChangeDelay?: number; // Después de entrar en la página, cuántos milisegundos esperar antes de comenzar la traducción. Para esperar la inicialización de la página, actualmente se establece en 250ms

// Traducción AI streaming
aiRule: {
  streamingSelector: string; // Selector que marca el elemento que se está traduciendo en la página de gpt
  messageWrapperSelector: string; // Selector del cuerpo del mensaje
  streamingChange: boolean; // Si los mensajes repetidos en la página tipo gpt son actualizaciones incrementales o actualizaciones completas. gpt es incremental
};
```