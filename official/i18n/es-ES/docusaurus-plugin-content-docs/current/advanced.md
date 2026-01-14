---
sidebar_position: 4
---

# Opciones avanzadas de personalización

Esta página está dirigida a usuarios avanzados con conocimientos básicos de HTML/CSS/JSON. La configuración avanzada puede mejorar significativamente la adaptabilidad, pero también es más fácil cometer errores que parecen correctos pero no funcionan. Se recomienda hacer una copia de seguridad antes de editar.

## Advertencias antes de usar

- La entrada está en [Configuración para desarrolladores](https://dash.immersivetranslate.com/#developer).
- Haz una copia de seguridad de "User Config" / "User Rules" antes de editar, para evitar que la configuración sea ignorada por errores en el formato.
- La configuración final integrada debe tomarse como referencia (campos, valores predeterminados, servicios disponibles) usando "Click to expand the final config".

## Entradas y prioridades

Entradas comunes (Configuración para desarrolladores):
- Edit Full User Config: configuración completa (incluye `rules`, servicios de traducción, estilos, etc.).
- Edit User Rules: solo edita el array `rules` (solo acepta array, no envuelvas en `{ "rules": [...] }`).
- Injected CSS: inyección global de CSS.

Prioridades (de mayor a menor): `rules` coincidentes > `generalRule` > configuración por defecto.
Al coincidir una `rule`, se combinará con `generalRule`, teniendo prioridad el campo en la `rule`.

## Comenzando Rápido (casos más comunes)

### 1) Solo traducir el contenido de un sitio

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

### 2) Siempre traducir / Nunca traducir

```json
{
  "translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
  }
}
```

### 3) Usar diferentes servicios de traducción en diferentes sitios

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

### 4) Estilos de traducción por sitio

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

### 5) Solucionar problemas de estilo causados por la traducción

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

### 6) No mostrar servicios de traducción no configurados en el panel

```json
{
  "showUnconfiguredTranslationServiceInPopup": false
}
```

## Reglas y coincidencias

### Combinación de reglas

- `generalRule`: reglas base aplicables a todos los sitios.
- `rules`: reglas a nivel de sitio, prioridad más alta si coinciden.

Los campos en `rules` pueden reutilizar la mayoría de los campos de `generalRule`.

### Formatos comunes para matches

`matches` soporta cadenas o arrays:
- Dominio: `example.com`
- URL completa: `https://example.com/path/`
- Comodines: `https://*/*q=*`
- Coincide todo: `*` / `*://*` / `*://*/*`
- Archivos locales: `file://*`

Nota: `*.twitter.com` solo coincide con subdominios, no con el dominio raíz `twitter.com`.

### selectors / excludeSelectors

- `selectors`: solo traduce los elementos que coinciden (sobrescribe el rango predeterminado).
- `excludeSelectors`: excluye elementos de la traducción.

Si solo necesitas añadir/eliminar del rango original, es preferible usar `.add` / `.remove` (ver siguiente sección).

### Herencia y modificaciones incrementales (.add / .remove)

Para campos tipo array u objeto, se soportan `.add` / `.remove` como modificaciones incrementales.
Se recomienda usar estas para evitar sobrescribir reglas predeterminadas:

```json
[
  {
    "id": "twitter",
    "selectors.add": ["[data-testid='tweetText'] a"],
    "excludeSelectors.add": ["header"]
  }
]
```

### Tabla rápida de campos comunes (extracto)

Coincidencia:
- `matches` / `excludeMatches`
- `selectorMatches` / `excludeSelectorMatches`

Ámbito de traducción:
- `selectors` / `excludeSelectors` / `excludeTags`
- `stayOriginalSelectors` / `stayOriginalTags`
- `extraInlineSelectors` / `extraBlockSelectors`

Estilos y disposición:
- `translationClasses`: añade clases extra al texto traducido
- `globalStyles` / `globalAttributes`
- `injectedCss` / `additionalInjectedCss`
- `wrapperPrefix` / `wrapperSuffix`
- `blockMinTextCount` / `blockMinWordCount`

Momento y móviles:
- `urlChangeDelay` / `observeUrlChange`
- `isShowUserscriptPagePopup`

### Traducción de mensajes en flujo tipo GPT

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

Encuentra más detalles sobre los campos al final en "Anexo: Referencia de campos Rule".

## Lógica de matches (explicación corta)

- Dominio puro (sin `*` ni ruta): compara solo el hostname.
- URL completa (sin `*`): compara protocolo + host + puerto + ruta.
- Con `*` o sin protocolo: coinciden según reglas de comodines (http/https/file por defecto).

Ejemplos comunes:
- `twitter.com` ✅ coincide con `https://twitter.com/home`
- `*.twitter.com` ✅ coincide con `https://mobile.twitter.com`, ❌ no coincide con `https://twitter.com`
- `https://twitter.com/home` solo coincide si la URL es exacta
- `twitter.com/*` coincide con todas las rutas bajo `twitter.com`

## Caso de adaptación de sitio (ejemplo Twitter)

A continuación una regla interna de Twitter (extracto), para ilustrar el uso típico de `selectors` / `excludeSelectors` / `globalStyles`:

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

- `selectors`: solo traducción del contenido del tweet, evitando nombres/acciones.
  ![tweet](https://s.immersivetranslate.com/assets/r2-uploads/tweet.png)
- `excludeSelectors`: excluye botones, navegación u otros elementos interactivos.
  ![twitter-follow](https://s.immersivetranslate.com/assets/r2-uploads/twitter-follow.png)
- `globalStyles`: elimina límites en el número de líneas, evitando que se corte la traducción.
  ![usuario](https://s.immersivetranslate.com/assets/r2-uploads/twitterUser.png)

## Personalización de adaptación de sitios

Puedes reutilizar una regla interna con `id` y modificar incrementalmente usando `.add/.remove`:

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

Explicación:
- `id` permite heredar reglas internas y evitar repetir `matches`.
- `.add/.remove` modifica arrays de manera incremental y es la forma recomendada.

Algunos `id` internos comunes (extracto):
- `isEbook`: página de lector epub
- `isEbookBuilder`: página para crear ebooks bilingües
- `pdf`: página con PDFs bilingües

Reglas internas completas:
- `https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json`

## Configuración del servicio de traducción

- `translationService`: motor de traducción por defecto.
- `translationServices`: configuración del servicio y sobreescritura por sitio.
- `showUnconfiguredTranslationServiceInPopup`: ocultar servicios no configurados.

Ejemplo (usando Tencent):

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

Explicación:
- `matches` especifica los sitios donde se usa ese servicio.
- `limit` es el límite de solicitudes por segundo.
- `maxTextGroupLengthPerRequest` / `maxTextLengthPerRequest` controla el tamaño de solicitudes.
- `apiUrl` puede personalizar la URL del servicio.

### Configuración de tiempo de espera (timeout máximo de solicitud)

Puedes configurar el tiempo de espera por servicio, en milisegundos (ms). Si usas el servicio Pro, puedes ajustar `proRequestTimeout`:

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

Consejos:
- Un tiempo de espera muy largo puede causar demoras prolongadas; uno muy corto puede llevar a errores frecuentes.
- El valor por defecto varía según el servicio, revisa la configuración final.
- `proRequestTimeout` solo aplica si el `provider` es `pro` (servicio de suscripción).

## Idioma y estrategia de traducción

### Siempre traducir / Nunca traducir ciertos idiomas

```json
{
  "translationLanguagePattern": {
    "matches": ["en"],
    "excludeMatches": ["zh"]
  }
}
```

### Fijar idioma de origen por sitio

```json
{
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  }
}
```

## Otras configuraciones globales frecuentes

### Permitir renderizar etiquetas HTML

Permite que la traducción conserve y renderice etiquetas HTML:

```json
{
  "enableRenderHtmlTag": true
}
```

## Estilos y temas del texto traducido

Estilos soportados por `translationTheme` (revisa configuración final):

```text
none, grey, dashed, dashedBorder, solidBorder, dotted, underline, mask, opacity,
paper, dividingLine, highlight, marker, marker2, blockquote, weakening, italic,
bold, thinDashed, nativeDotted, wavy, nativeDashed, nativeUnderline, background
```

Ejemplo de configuración por sitio:

```json
{
  "translationThemePatterns": {
    "highlight": {
      "matches": ["discord.com"]
    }
  }
}
```

## Parámetros avanzados / AI

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

### Personalizar cabeceras y cuerpo de la solicitud

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

### Cómo personalizar configuración para modelos Gemini

Los modelos Gemini tienen ajustes internos por defecto; para sobrescribirlos, usa `modelsOverrides`:

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

Consejo: `modelsOverrides` también aplica a otros servicios AI, sobreescribe la configuración al coincidir el nombre del modelo.

### Seguir estrictamente prompts personalizados

> Para reducir "alucinaciones" de modelos de lenguaje, el complemento tiene verificación de calidad de traducción. Compara la relación de tokens entre la respuesta y la petición para juzgar la consistencia. Si dicha relación es anormal (muy alta o baja), el resultado es inválido y se usará una traducción alternativa.
> Si tu prompt personalizado no es una traducción (p.ej. para reescritura/mejoras), puede que la relación de tokens no sea estándar. En ese caso, activa el modo estricto para saltar la comprobación.

```json
{
  "translationServices": {
    "claude": {
      "strictPrompt": true
    }
  }
}
```

### Prompts multilingües personalizados (ejemplo)

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

## Glosario de términos y traducción automática

Nueva función de [Glosario AI](https://dash.immersivetranslate.com/#terms), solo disponible con servicios de traducción AI.

Por defecto, el traductor automático no usa glosarios (suelen hacer sustituciones que afectan la calidad). Para forzar su uso (no recomendado):

```json
{
  "enableMachineTranslateTerms": true
}
```

## Ciclo de limpieza de caché

El complemento limpia automáticamente el caché cada 30 días para evitar exceso de datos y pérdida de rendimiento.

```json
{
  "cacheMaxAgeDay": 30
}
```

## Injected CSS y globalStyles

- Injected CSS: inyección CSS global, ideal para arreglos de página.
- globalStyles: reemplazo de estilo por regla, ideal para arreglos por sitio.

Ejemplo de Injected CSS:

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

## Solución de problemas y errores comunes

- `*.twitter.com` no incluye el dominio raíz, asegúrate de escribir también `twitter.com`.
- `selectors` sobrescribe el rango de texto traducido, usa `.add/.remove` cuando sea posible.
- Si escribes `matches` como `example.com/path`, se usará el modo "comodín"; aclara si quieres URL exacta.
- Si la configuración no funciona: verifica el resultado combinado en la configuración final y recarga la página.
- Un punto y coma extra en JSON lo invalida.

## Anexo: Referencia de campos Rule

Referencia de campos Rule (versión documentación), cubre los más comunes; para la lista más actualizada consulta la configuración final.
Consejo: en arrays u objetos, usa `.add` / `.remove` para modificar de forma incremental sin sobrescribir reglas por defecto.

```typescript
export interface Rule {
  // Coincidencia de sitio
  id?: string; // ID interno de la regla, para reutilizar reglas internas
  matches?: string | string[]; // Esta regla solo se aplica a estos sitios
  excludeMatches?: string | string[]; // Excluir sitios específicos
  selectorMatches?: string | string[]; // Coincidencia por selector, sin especificar URL
  excludeSelectorMatches?: string | string[]; // Exclusión por selector, igual que arriba

  // Ámbito de traducción
  selectors?: string | string[]; // Solo traduce los elementos coincidentes
  excludeSelectors?: string | string[]; // Excluye elementos, no se traducen
  excludeTags?: string | string[]; // Excluye etiquetas, no se traducen

  // Ámbito adicional de traducción (si falla, usa selectors.add / selectors.remove)
  additionalSelectors?: string | string[]; // Ámbito de traducción adicional
  additionalExcludeSelectors?: string | string[]; // Elementos a excluir adicionalmente
  additionalExcludeTags?: string | string[]; // Etiquetas a excluir adicionalmente (puede estar obsoleto)

  // Mantener originales
  stayOriginalSelectors?: string | string[]; // Los elementos coincidentes quedan como están
  stayOriginalTags?: string | string[]; // Etiquetas coincidentes como code quedan sin traducir

  // Block o Inline
  extraBlockSelectors?: string | string[]; // Elementos tratados como block
  extraInlineSelectors?: string | string[]; // Elementos tratados como inline
  inlineTags?: string | string[]; // Etiquetas tratadas como inline
  preWhitespaceDetectedTags?: string | string[]; // Etiquetas que detectan salto de línea automáticamente

  // Estilos de traducción
  translationClasses?: string | string[]; // Clases extra para el texto traducido

  // Estilos globales
  globalStyles?: Record<string, string>; // Modificar estilos de la página
  globalAttributes?: Record<string, Record<string, string | null>>; // Modificar atributos de elementos

  // Estilos inyectados
  injectedCss?: string | string[]; // Inyectar CSS
  additionalInjectedCss?: string | string[]; // Inyectar CSS adicional

  // Contexto
  wrapperPrefix?: string; // Prefijo para zona traducida
  wrapperSuffix?: string; // Sufijo para zona traducida

  // Número mínimo de caracteres en bloques traducidos
  blockMinTextCount?: number; // Mínimo de caracteres en block
  blockMinWordCount?: number; // Mínimo de palabras en block

  // Mínimo de texto traducible en contenedores
  containerMinTextCount?: number; // Mínimo de caracteres para reconocimiento automático
  paragraphMinTextCount?: number; // Mínimo de caracteres por párrafo
  paragraphMinWordCount?: number; // Mínimo de palabras por párrafo

  // Forzar salto en párrafos largos
  lineBreakMaxTextCount?: number; // Límite de caracteres antes de forzar salto

  // Momento para iniciar traducción
  urlChangeDelay?: number; // Milisegundos de retardo tras entrar a la página
  observeUrlChange?: boolean; // Volver a traducir al cambiar URL

  // Móviles
  isShowUserscriptPagePopup?: boolean; // Mostrar popup flotante en móviles
  fingerCountToToggleTranslagePageWhenTouching?: number; // Obsoleto

  // Traducción AI streaming
  aiRule?: {
    streamingSelector: string; // Selector del elemento en traducción
    messageWrapperSelector: string; // Selector del mensaje
    streamingChange: boolean; // Actualiza de forma incremental
  };
}
```
