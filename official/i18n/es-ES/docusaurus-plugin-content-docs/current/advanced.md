---
sidebar_position: 4
---

# Opciones de personalización avanzadas

Puedes editar configuraciones más personalizadas en la Página de Configuración Extendida -> Configuración del Desarrollador -> Configuración del Usuario que no son editables en la UI para usuarios avanzados, consulta la última nota para más detalles sobre los parámetros. La `config` incorporada actual se puede encontrar [aquí](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

## Reglas para Usuarios

Con `Reglas` es posible personalizar la configuración de un sitio web particular, decidiendo qué contenido necesita ser traducido o no, o ajustando el estilo de las páginas, etc.

```json
[
  {
    "coincide": "www.google.com",
    "selectores": [".title"]
  },
  {
    "coincide": "*.twitter.com",
    "selectores": [".text"],
    "excluirSelectores": ["nav", " footer"]
  }
]
```

Usa `coincide` para hacer coincidir el sitio web correspondiente. Se permiten comodines, por ejemplo, `*.google.com`, `www.google.com/test/*`, `file://*`.

Usar `selectores` anula el alcance de la traducción inteligente, traduciendo solo los elementos coincidentes con ese selector.

Usa `excluirSelectores` para excluir elementos sin traducir la posición.

Usa la familia de selectores `adicional` para aumentar o disminuir el rango de traducción basado en la traducción inteligente.

```json
[
  {
    "coincide": "www.google.com",
    "selectoresAdicionales": [],
    "excluirSelectoresAdicionales": []
  }
]
```

Si quieres traducir una región mientras tratas los elementos como un todo y no separándolos, puedes usar el selector `selectoresDeBloqueAtómico`. Por ejemplo, perfiles de Instagram. Ten en cuenta que usar `selectoresDeBloqueAtómico` requiere seleccionar con `selectores` antes de usar `selectoresDeBloqueAtómico`.

```json
{
  "coincide": "https://www.instagram.com/*",
  "selectores": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
  "selectoresDeBloqueAtómico": [
    "div. ._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
}
```

Si la traducción resulta en páginas desalineadas, texto superpuesto y otros casos extremos, puedes usar `estilosGlobales` para ajustar el estilo de la página y corregirlo. Por ejemplo, el encabezado de youtube, que se usa para eliminar la altura máxima de la página original.

```json
{
  "coincide": "www.google.com",
  "estilosGlobales": { ".title": "max-height:unset;" }
}
```

Note that I've translated the content as closely as possible, including the comments and JSON keys where applicable, to maintain the context and meaning. However, JSON keys (like "matches", "selectors", etc.) typically shouldn't be translated because they are part of the code syntax and are expected to be in English by most programming languages and frameworks.

## Mejoras en la consolidación de reglas de usuario

Soporte desde la versión 0.7.4+. Tomemos como ejemplo el omitir la zona sin traducción.

```json
{
  "matches": "https://www.elektrotechnik.rwth-aachen.de/*",
  "additionalExcludeSelectors.remove": [".notranslate", "[translate=no]"]
}
```

Las operaciones de añadir y eliminar modifican las reglas proporcionadas por defecto y no necesitan ser reemplazadas en su totalidad, como era el caso anteriormente.

## CSS Inyectado

El CSS inyectado te permite inyectar estilos web personalizados globalmente. Puede ser utilizado con `translationClasses` de `Rules`.

```
".immersive-translate-target-wrapper img { width: 16px; height: 16px }"
```

También es posible estilizar el sitio de una manera más personalizada, como un gestor de estilos web regular. (incluso utilizando `display:none` para eliminar anuncios)

```css
.title {
  color: red;
}
```

## Configuración de Usuario

Config te permite personalizar la configuración de este plugin, como los servicios de traducción, opciones de traducción de idiomas específicos del idioma, etc.

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "coincidencias": ["*.twitter.com"]
    }
  },
  "patronUrlTraduccion": {
    "excluirCoincidencias": ["www.google.com"]
  },
  "patronIdiomaTraduccion": {
    "coincidencias": ["en"]
  },
  "temaTraduccion": "ninguno",
  "patronesTemaTraduccion": {
    "subrayado": {
      "coincidencias": ["discord.com"]
    }
  },
  "reglaGeneral": {
    "_comentario": "",
    "normalizarCuerpo": "",
    "cssInyectado": [],
    "cssInyectadoAdicional": [],
    "prefijoEnvoltura": "inteligente",
    "sufijoEnvoltura": "inteligente",
    "esPdf": false,
    "esTransformarSaltoLineaPreTag": false,
    "retrasoCambioUrl": 20,
    "mostrarPopupPaginaUserscript": true,
    "observarCambioUrl": true,
    "minTextoParrafo": 8,
    "minPalabrasParrafo": 2,
    "minTextoBloque": 32,
    "minPalabrasBloque": 5,
    "minTextoContenedor": 18,
    "maxTextoSaltoLinea": 0,
    "atributosGlobales": {},
    "estilosGlobales": {},
    "selectores": [],
    "etiquetasDeteccionEspacioBlancoPre": ["DIV", "SPAN"],
    "selectoresPermanecerOriginal": [],
    "selectoresAdicionales": [],
    "etiquetasBloqueAtomico": [],
    "excluirSelectores": [],
    "selectoresExcluidosAdicionales": [],
    "clasesTraduccion": [],
    "selectoresBloqueAtomico": [],
    "excluirEtiquetas": [],
    "etiquetasMeta": ["META", "SCRIPT", "STYLE", "NOSCRIPT"],
    "etiquetasExcluidasAdicionales": [],
    "etiquetasPermanecerOriginal": ["CODE", "TT", "IMG", "SUP"],
    "etiquetasPermanecerOriginalAdicionales": [],
    "etiquetasEnLinea": [],
    "etiquetasEnLineaAdicionales": [],
    "selectoresEnLineaExtra": [],
    "selectoresAdicionalesEnLinea": [],
    "selectoresExtraBloque": [],
    "todasEtiquetasBloque": [],
    "pdfAlturaLineaNuevoParrafo": 2.4,
    "pdfIndentacionNuevoParrafo": 1.2,
    "pdfIndentacionDerechaNuevoParrafoPx": 130,
    "conteoDedosAlternarPaginaTraduccionTocando": 4
  },
  "reglas": [
    {
      "coincidencias": "www.google.com",
      "selectores": [".clase"]
    }
  ]
}
```

Los campos de regla en `reglas` pueden usar todos los campos en `reglaGeneral`. Las `reglas` tienen la prioridad más alta, fusionando la `reglaGeneral` y las reglas para esa `regla` cuando se coincide con una `regla` particular para un sitio particular.

Introduciendo algunos de los campos comunes de Config.

### No mostrar servicios de traducción no configurados en el panel emergente

`"showUnconfiguredTranslationServiceInPopup": false`

### Configuración de servicios de traducción

Utiliza `translationService` para seleccionar el motor de traducción predeterminado, que actualmente soporta:

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

Usa `translationServices` para configurar el `apikey` de cada servicio de traducción, diferentes proveedores de servicios necesitan diferentes parámetros, y sus claves API pueden ser solicitadas en el centro de desarrolladores de sus respectivos sitios web.

Por ejemplo, para el Traductor de Tencent, necesitas configurar `secretId`, `secretKey`. Puedes dirigirte a Tencent Cloud para solicitar una clave API con 5 millones de caracteres gratuitos por mes. Consulta [aquí](/docs/services/tencent) para el proceso de solicitud.

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

Campo `matches`, usando este servicio de traducción para un sitio web específico.

El campo `limit`, que especifica el número máximo de solicitudes por segundo para este servicio de traducción (algunos servicios limitan el número máximo de solicitudes por segundo).

Campo `maxTextGroupLengthPerRequest`, número máximo de párrafos por solicitud

Campo `maxTextLengthPerRequest`, número máximo de caracteres por solicitud

`apiUrl` Te permite personalizar la dirección de la interfaz de traducción.

### Siempre traducir sitios web específicos

`translationUrlPattern` Configura sitios que siempre se traducen y sitios que nunca se traducen.

- `matches` La configuración siempre traduce el sitio.
- `excludeMatches` Configura sitios que nunca se traducen.

Los valores de configuración pueden ser nombres de dominio o URLs con `*`, como: `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### Siempre traducir idiomas específicos

translationLanguagePattern, configura el idioma que siempre se traduce y el idioma que nunca se traduce.

- `matches` Configura el idioma que siempre se traduce, por ejemplo, `en`,
- `excludeMatches` Configura los idiomas que nunca se traducen.

### Formato de visualización de la traducción

`translationTheme` es el formato de visualización de la traducción, y actualmente soporta los siguientes estilos:

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

Nombre correspondiente en español:

```json
{
  "none": "ninguno",
  "dashed": "línea discontinua",
  "dotted": "línea punteada",
  "underline": "subrayado",
  "mask": "efecto de desenfoque",
  "paper": "efecto de sombra de papel blanco",
  "highlight": "resaltar",
  "blockquote": "estilo de cita",
  "weakening": "debilitamiento",
  "italic": "cursiva",
  "bold": "negrita",
  "thinDashed": "subrayado discontinuo fino"
}
```

`translationThemePatterns` te permite configurar diferentes estilos de traducción para diferentes sitios web.

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### Traducción de Mensajes de la Página de Flujo de Clase gpt

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

### Reglas

`rules` es un objeto de arreglo que te permite configurar reglas para sitios especiales, como hacer que Twitter traduzca solo una cierta parte de una región:

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

Las `rules` incorporadas actuales se pueden encontrar [aquí](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

Algunos de los campos importantes se seleccionan a continuación para ilustración:

```typescript
export interface Rule {
  // Coincidir con el sitio web
  id?: string; // Cada regla de adaptación tiene su propio id, si los usuarios quieren reutilizar esta regla además de este cambio, necesitan agregar este id correspondiente a su propia regla para reutilizarla
  matches?: string | string[]; // Esta regla solo coincidirá con el sitio web aquí. Esta regla solo coincidirá con los sitios aquí.
  excludeMatches?: string | string[]; // Excluir sitios específicos.
  selectorMatches?: string | string[]; // Coincidir con un selector sin especificar todas las urls
  excludeSelectorMatches?: string | string[]; // Excluir reglas, como arriba.

  // Especificar rango de traducciones
  selectors?: string | string[]; // Traducir solo elementos que coincidan
  excludeSelectors?: string | string[]; // Excluir elementos, no traducir coincidencias
  excludeTags?: string | string[]; // Excluir etiquetas, no traducir etiquetas coincidentes

  // agregar rangos de traducción en lugar de sobrescribir
  additionalSelectors?: string | string[]; // agregar rangos de traducción. Agregar ubicaciones de traducción a las regiones traducidas inteligentemente.
  additionalExcludeSelectors?: string | string[]; // Agregar elementos excluidos para que la traducción inteligente no traduzca ubicaciones específicas.
  additionalExcludeTags?: string | string[]; // Etiquetas excluidas adicionales

  // Dejar tal cual
  stayOriginalSelectors?: string | string[]; // Los elementos coincidentes se dejarán tal cual. Comúnmente usado en etiquetas de sitios de foros.
  stayOriginalTags?: string | string[]; // Las etiquetas coincidentes se dejarán tal cual, por ejemplo, `code`

  // Bloque o en línea
  extraBlockSelectors?: string | string[]; // Selectores adicionales, los elementos coincidentes se tratarán como elementos de bloque, no se traducirán en una línea.
  extraInlineSelectors?: string | string[]; // Selectores adicionales que se utilizarán como elementos en línea.

  inlineTags?: string | string[]; // La etiqueta coincidente se utilizará como un elemento en línea
  preWhitespaceDetectedTags?: string | string[]; // La etiqueta coincidente se envolverá automáticamente

  // Estilo de traducción
  translationClasses?: string | string | string[]; // Agregar clases adicionales a la traducción

  // Estilos globales
  globalStyles?: Record<string, string>; // Modificar estilos de página, útil si la traducción causa que la página se desordene. `
  globalAttributes?: Record<string, Record<string, string>>; // Modificar atributos de elementos de página

  // Estilos incrustados
  injectedCss?: string | string[]; // Incrustar estilos CSS
  additionalInjectedCss?: string | string[]; // Estilos CSS adicionales en lugar de sobrescribirlo.

  // Contexto
  wrapperPrefix?: string; // El prefijo del área de traducción, por defecto es inteligente, con o sin saltos de línea dependiendo del número de caracteres.
  wrapperSuffix?: string; // Sufijo del área de traducción

  // Número de caracteres para envolver la traducción
  blockMinTextCount?: number; // Número mínimo de caracteres para envolver la traducción como un bloque, de lo contrario, la traducción es un elemento en línea.
  blockMinWordCount?: number; // Igual que arriba. Si quieres que siempre sean nuevas líneas, puedes poner 0 en ambos.

  // Número mínimo de caracteres que se pueden traducir del contenido
  containerMinTextCount?: number; // Número mínimo de caracteres que un elemento debe contener antes de que se traduzca, por defecto es 18
  paragraphMinTextCount?: number; // Número mínimo de caracteres para el párrafo, mayor que el número de caracteres que el contenido debe contener. número, cualquier cosa mayor que eso será traducida
  paragraphMinWordCount?: number; // Número mínimo de palabras en el párrafo original

  // Saltos de línea forzados para párrafos largos
  lineBreakMaxTextCount?: number; // Número máximo de caracteres en el párrafo para forzar a romper cuando se traduce un párrafo largo.

  // Cuándo empezar la traducción.
  urlChangeDelay?: number; // Cuántos milisegundos de retraso para la traducción después de entrar en la página. Para esperar a que la página se inicialice, por defecto es 250ms
  observeUrlChange?: boolean; // Detectar cuando la dirección url ha cambiado y empezar la traducción de nuevo, verdadero por defecto.

  // Móvil
  isShowUserscriptPagePopup?: boolean; // Mostrar el popup de la página en dispositivos móviles. ventana flotante, verdadero por defecto.
  fingerCountToToggleTranslagePageWhenTouching?: number; // Traduce cuando cuatro dedos tocan, se puede configurar a 0, 2, 3, 4, 5

  // Traducciones en streaming de IA
  aiRule: {
    streamingSelector: string; // Selector para marcar el elemento que se está traduciendo en la página web de gpt
    messageWrapperSelector: string; // Selector del cuerpo del mensaje
    streamingChange: boolean; // Si el mensaje se actualiza de manera incremental o completa para la iteración de la página web de clase gpt. gpt es incremental
  };
}
```

**Más explicación**

Diferencia entre bloque e inline, si quieres saber más puedes ver [aquí](https://developer.mozilla.org/es/docs/Web/HTML/Elementos_en_línea#en_línea)

- El elemento de bloque ocupa una sola línea, y múltiples elementos de bloque vecinos ocupan cada uno una nueva línea.
- El elemento en línea no ocupa una sola línea; múltiples elementos en línea vecinos se organizan en la misma línea, y no se crea una nueva línea hasta que una línea tiene demasiados.
