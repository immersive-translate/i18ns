---
sidebar_position: 4
---

# Opções Avançadas de Personalização

Esta página destina-se a utilizadores avançados que tenham conhecimentos básicos de HTML/CSS/JSON. As configurações avançadas podem aumentar significativamente a capacidade de adaptação, mas também aumentam o risco de configurações "aparentemente corretas" que não funcionam. Recomenda-se fazer backup antes de editar.

## Avisos antes de usar

- A entrada está em [Definições de Programador](https://dash.immersivetranslate.com/#developer).
- Faça backup da Configuração do Utilizador / Regras do Utilizador antes de editar, para evitar que erros de formatação façam as configurações serem ignoradas.
- Para a configuração final interna, consulte "Click to expand the final config" (campos, valores padrão, serviços disponíveis).

## Entradas e Prioridades

Entradas comuns (Definições de Programador):
- Editar Configuração Completa do Utilizador: Configuração completa (incluindo `rules`, serviços de tradução, estilos, etc.).
- Editar Regras do Utilizador: Edita apenas o array `rules` (aceita apenas arrays, não coloque `{ "rules": [...] }`).
- CSS Injetado: Injeção global de CSS.

Prioridade (da mais alta para a mais baixa): `rules` correspondidas > `generalRule` > configuração padrão interna.
Ao corresponder uma regra, o `generalRule` é combinado com essa regra, prevalecendo os campos da regra.

## Início Rápido (Necessidades Mais Comuns)

### 1) Traduzir apenas o conteúdo principal de um site

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

### 2) Traduzir Sempre / Nunca Traduzir

```json
{
  "translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
  }
}
```

### 3) Usar diferentes serviços de tradução para diferentes sites

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

### 4) Estilo da tradução por site

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

### 5) Tradução causa problemas de estilo, corrija com CSS

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

### 6) Não mostrar serviços de tradução não configurados no painel

```json
{
  "showUnconfiguredTranslationServiceInPopup": false
}
```

## Regras e Combinações

### Combinação de Regras

- `generalRule`: regra base comum a todos os sites.
- `rules`: regras específicas por site, têm a prioridade mais alta quando ativadas.

Os campos do `rules` podem usar a maioria dos campos de `generalRule`.

### Formatos Comuns de matches

`matches` suporta string ou array:
- Domínio: `example.com`
- URL completa: `https://example.com/path/`
- Wildcard: `https://*/*q=*`
- Todos: `*` / `*://*` / `*://*/*`
- Arquivo local: `file://*`

Nota: `*.twitter.com` corresponde apenas a subdomínios, não ao domínio raiz `twitter.com`.

### selectors / excludeSelectors

- `selectors`: traduz apenas os elementos correspondentes (substitui o intervalo padrão).
- `excludeSelectors`: exclui da tradução elementos específicos.

Se deseja apenas adicionar/remover em relação ao padrão, prefira usar `.add` / `.remove` (ver secção seguinte).

### Herança e Modificação Incremental (.add / .remove)

Para campos tipo array ou objeto, suporta `.add` / `.remove` como "modificação incremental".
Recomenda-se usá-los para evitar sobrescrever as regras padrão:

```json
[
  {
    "id": "twitter",
    "selectors.add": ["[data-testid='tweetText'] a"],
    "excludeSelectors.add": ["header"]
  }
]
```

### Referência Rápida de Campos Comuns (excertos)

Relacionados à correspondência:
- `matches` / `excludeMatches`
- `selectorMatches` / `excludeSelectorMatches`

Âmbito da tradução:
- `selectors` / `excludeSelectors` / `excludeTags`
- `stayOriginalSelectors` / `stayOriginalTags`
- `extraInlineSelectors` / `extraBlockSelectors`

Estilo e Layout:
- `translationClasses`: adiciona classes extra à tradução
- `globalStyles` / `globalAttributes`
- `injectedCss` / `additionalInjectedCss`
- `wrapperPrefix` / `wrapperSuffix`
- `blockMinTextCount` / `blockMinWordCount`

Timing e Mobile:
- `urlChangeDelay` / `observeUrlChange`
- `isShowUserscriptPagePopup`

### Tradução tipo mensagem streaming (estilo GPT)

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

Para mais campos, consulte o apêndice "Referência de Campos Rule" no final.

## Lógica de correspondência de matches (Resumo)

- Domínio puro (sem `*` e sem caminho): compara apenas o hostname.
- URL completa (sem `*`): compara protocolo + host + porta + caminho.
- Com `*` ou sem protocolo: usa correspondência por wildcard (suporta por padrão http/https/file).

Exemplos comuns:
- `twitter.com` ✅ corresponde a `https://twitter.com/home`
- `*.twitter.com` ✅ corresponde a `https://mobile.twitter.com`, ❌ não corresponde a `https://twitter.com`
- `https://twitter.com/home` corresponde apenas à URL exata
- `twitter.com/*` corresponde a todos os caminhos sob `twitter.com`

## Exemplo de Adaptação de Site (Twitter)

Segue exemplo de regra interna para o Twitter (excerto), demonstrando uso típico de `selectors` / `excludeSelectors` / `globalStyles`:

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

- `selectors`: traduz apenas o conteúdo do tweet, evitando nomes/botões.
  ![tweet](https://s.immersivetranslate.com/assets/r2-uploads/tweet.png)
- `excludeSelectors`: exclui botões, navegação e outros elementos interativos.
  ![twitter-follow](https://s.immersivetranslate.com/assets/r2-uploads/twitter-follow.png)
- `globalStyles`: remove limite de linhas do tweet, evitando corte da tradução.
  ![twitterUser.png](https://s.immersivetranslate.com/assets/r2-uploads/twitterUser.png)

## Adaptação Personalizada de Sites

Pode reutilizar regras internas usando `id` e ajustar incrementalmente com `.add/.remove`:

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

Explicação:
- `id` permite herdar regras internas, evitando duplicar `matches`.
- `.add/.remove` faz alterações incrementais e é mais recomendado.

IDs internos comuns (excerto):
- `isEbook`: página de leitura de epub
- `isEbookBuilder`: gerar página de livro epub bilingue
- `pdf`: página de PDF bilingue

Regras internas completas:
- `https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json`

## Configuração de Serviços de Tradução

- `translationService`: motor de tradução padrão.
- `translationServices`: configurações do serviço e overrides por site.
- `showUnconfiguredTranslationServiceInPopup`: oculta serviços não configurados.

Exemplo (Tencent):

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

Explicação:
- `matches` define em que sites aplica o serviço.
- `limit` limita o número de requisições por segundo.
- `maxTextGroupLengthPerRequest` / `maxTextLengthPerRequest` controlam o volume por requisição.
- `apiUrl` permite definir URL do serviço manualmente.

### Configuração de Timeout de Requisão

Pode definir o tempo máximo de requisição por serviço (em milissegundos). Para serviços Pro, use `proRequestTimeout`.

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

Dicas:
- Demasiado alto: demorará a dar erro; demasiado baixo: mais erros por timeout.
- O padrão depende do serviço; consulte a configuração final.
- `proRequestTimeout` só tem efeito quando o `provider` é `pro` (serviço pago).

## Idioma e Estratégia de Tradução

### Sempre traduzir / Nunca traduzir determinado idioma

```json
{
  "translationLanguagePattern": {
    "matches": ["en"],
    "excludeMatches": ["zh"]
  }
}
```

### Definir língua de origem para sites específicos

```json
{
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  }
}
```

## Outras configurações globais frequentes

### Permitir renderizar tags HTML

Ative isto para manter e renderizar tags HTML nas traduções:

```json
{
  "enableRenderHtmlTag": true
}
```

## Estilo e Tema da Tradução

Estilos suportados por `translationTheme` (consulte a configuração final):

```text
none, grey, dashed, dashedBorder, solidBorder, dotted, underline, mask, opacity,
paper, dividingLine, highlight, marker, marker2, blockquote, weakening, italic,
bold, thinDashed, nativeDotted, wavy, nativeDashed, nativeUnderline, background
```

Configuração de tema por site:

```json
{
  "translationThemePatterns": {
    "highlight": {
      "matches": ["discord.com"]
    }
  }
}
```

## Parâmetros AI / Serviços avançados

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

### Cabeçalhos e Corpo da requisição personalizados

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

### Personalizar Gemini e outros modelos por modelo

Os modelos Gemini têm configurações padrão internas. Para sobrescrever use `modelsOverrides`:

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

Dica: `modelsOverrides` também se aplica a outros serviços de IA, permitindo sobrescrever por nome do modelo.

### Respeitar estritamente prompts personalizados

> Para diminuir "alucinações" dos modelos de linguagem, o plugin verifica a qualidade da tradução comparando a razão de tokens pedida vs resposta. Se a razão for anormal, o resultado é ignorado e tenta-se outro serviço.  
> Se o seu prompt personalizado não for estritamente de tradução (ex: reformulação, extensão...), pode falhar esse controlo. Ative modo estrito para ignorar a verificação.

```json
{
  "translationServices": {
    "claude": {
      "strictPrompt": true
    }
  }
}
```

### Exemplos de prompts multilíngua personalizados

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

## Glossário e Tradução Automática

É suportado [Glossário de IA](https://dash.immersivetranslate.com/#terms), válido apenas para serviços de IA.

Tradução automática normalmente não usa glossário (podem existir problemas de qualidade).
Para forçar a usar (não recomendado):

```json
{
  "enableMachineTranslateTerms": true
}
```

## Limpeza de Cache

Por padrão, a extensão elimina cache de traduções de 30 em 30 dias para não impactar a performance.

```json
{
  "cacheMaxAgeDay": 30
}
```

## CSS Injetado e globalStyles

- CSS Injetado: injeta CSS global (útil para correções do site inteiro).
- globalStyles: substitui estilos via regras (útil para correções por site).

Exemplo de CSS Injetado:

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

## Depuração e Armadilhas Comuns

- `*.twitter.com` não inclui o domínio raiz, escreva também `twitter.com`.
- `selectors` sobrescreve o intervalo padrão, prefira `.add/.remove`.
- Ao escrever `matches` como `example.com/path`, será considerado como wildcard. Confirme se quer URL exata.
- Se não funcionar: confirme config final e recarregue a página.
- Vírgulas a mais no final de arrays/objetos JSON fazem a configuração ser ignorada.

## Apêndice: Referência de Campos Rule

Esta é a referência dos campos Rule (versão documentação), incluindo os campos mais usados; consulte a configuração final para campos completos/atualizados.
Dica: Para campos do tipo array/objeto, pode usar `.add` / `.remove` para modificar sem sobrescrever as regras padrão.

```typescript
export interface Rule {
  // Corresponde ao site
  id?: string; // ID de regra interna, use ao reutilizar
  matches?: string | string[]; // Esta regra só será aplicada a estes sites
  excludeMatches?: string | string[]; // Exclui sites específicos
  selectorMatches?: string | string[]; // Corresponde por seletor, não URL
  excludeSelectorMatches?: string | string[]; // Exclusão por seletor

  // Define o âmbito de tradução
  selectors?: string | string[]; // Traduz apenas estes elementos
  excludeSelectors?: string | string[]; // Não traduz estes elementos
  excludeTags?: string | string[]; // Não traduz estas tags

  // Adicional (use selectors.add / selectors.remove se não funcionar)
  additionalSelectors?: string | string[]; // Adiciona seletores
  additionalExcludeSelectors?: string | string[]; // Adiciona exclusões
  additionalExcludeTags?: string | string[]; // Adiciona exclusões de tag (pode estar obsoleto)

  // Manter inalterado
  stayOriginalSelectors?: string | string[]; // Estes elementos mantêm-se
  stayOriginalTags?: string | string[]; // Estas tags mantêm-se, ex: code

  // Block ou Inline
  extraBlockSelectors?: string | string[]; // Força a ser block
  extraInlineSelectors?: string | string[]; // Força a ser inline
  inlineTags?: string | string[]; // Tags tratadas como inline
  preWhitespaceDetectedTags?: string | string[]; // Tags detetam pré-um espaço automático

  // Estilo da tradução
  translationClasses?: string | string[]; // Adiciona classe extra à tradução

  // Estilo global
  globalStyles?: Record<string, string>; // Edita estilos da página
  globalAttributes?: Record<string, Record<string, string | null>>; // Edita atributos de elementos

  // CSS injetado
  injectedCss?: string | string[]; // Injetar CSS
  additionalInjectedCss?: string | string[]; // CSS adicional

  // Contexto
  wrapperPrefix?: string; // Prefixo para o bloco de tradução
  wrapperSuffix?: string; // Sufixo para o bloco de tradução

  // Caracteres mínimos para quebrar linha
  blockMinTextCount?: number; // Mínimo de caracteres para block
  blockMinWordCount?: number; // Mínimo de palavras para block

  // Mínimo de texto para traduzir
  containerMinTextCount?: number; // Mínimo de caracteres num elemento
  paragraphMinTextCount?: number; // Mínimo de caracteres no parágrafo
  paragraphMinWordCount?: number; // Mínimo de palavras no parágrafo

  // Número máximo de caracteres por linha para quebrar
  lineBreakMaxTextCount?: number; // Máximo de caracteres para forçar quebra

  // Momento de acionar tradução
  urlChangeDelay?: number; // Atraso para início da tradução
  observeUrlChange?: boolean; // Retraduzir ao mudar URL

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Mostrar popup em mobile
  fingerCountToToggleTranslagePageWhenTouching?: number; // Obsoleto

  // Tradução streaming AI
  aiRule?: {
    streamingSelector: string; // Seletor do elemento traduzido
    messageWrapperSelector: string; // Seletor da mensagem central
    streamingChange: boolean; // Atualização incremental?
  };
}
```
