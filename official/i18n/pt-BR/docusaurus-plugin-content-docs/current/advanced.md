---
sidebar_position: 4
---

# Opções Avançadas de Personalização

Esta página destina-se a usuários avançados com alguma experiência em HTML/CSS/JSON. Configurações avançadas podem melhorar significativamente a adaptabilidade, mas também aumentam a chance de criar configurações que "parecem corretas mas não funcionam". Recomenda-se fazer backup antes de editar.

## Avisos Antes de Usar

- Acesse em [Configurações de Desenvolvedor](https://dash.immersivetranslate.com/#developer).
- Faça backup de User Config / User Rules antes de editar, para evitar perda de configuração por erro de formatação.
- Considere a configuração final interna como referência (“Click to expand the final config”) para campos, valores padrão e serviços disponíveis.

## Pontos de Entrada e Prioridade

Entradas comuns (Configurações de Desenvolvedor):
- Edit Full User Config: configuração completa (inclui `rules`, serviços de tradução, estilos, etc).
- Edit User Rules: edita somente o array `rules` (aceita apenas array, não inclua `{ "rules": [...] }`).
- Injected CSS: injeção global de CSS.

Prioridade (maior para menor): `rules` correspondentes > `generalRule` > configuração padrão interna.
Ao corresponder uma `rule`, ela é mesclada com `generalRule`, prevalecendo os campos da `rule`.

## Início Rápido (Requisitos Mais Comuns)

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

### 2) Sempre/Nunca traduzir

```json
{
  "translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
  }
}
```

### 3) Usar diferentes serviços de tradução por site

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

### 5) Corrigir problemas de estilo causados pela tradução

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

## Regras e Correspondência

### Mesclagem de Regras

- `generalRule`: base de regras comuns a todos os sites.
- `rules`: regra específica do site, com prioridade máxima se corresponder.

Campos dentro de `rules` podem usar a maioria dos campos disponíveis em `generalRule`.

### Formatos comuns de "matches"

`matches` aceita string ou array:
- Domínio: `example.com`
- URL completa: `https://example.com/path/`
- Curinga: `https://*/*q=*`
- Corresponder tudo: `*` / `*://*` / `*://*/*`
- Arquivo local: `file://*`

Observação: `*.twitter.com` só corresponde subdomínios, não o domínio raiz `twitter.com`.

### selectors / excludeSelectors

- `selectors`: traduz apenas elementos correspondentes (substitui o escopo padrão).
- `excludeSelectors`: elementos a serem excluídos da tradução.

Para apenas adicionar/remover do escopo original, prefira usar `.add` / `.remove` (veja próxima seção).

### Herança e Modificações Incrementais (.add / .remove)

Para campos array ou objeto, suporte a `.add` / `.remove` para modificações incrementais.
Recomenda-se seu uso para evitar sobrescrever regras padrão:

```json
[
  {
    "id": "twitter",
    "selectors.add": ["[data-testid='tweetText'] a"],
    "excludeSelectors.add": ["header"]
  }
]
```

### Referência Rápida de Campos Comuns (parcial)

Relacionados à correspondência:
- `matches` / `excludeMatches`
- `selectorMatches` / `excludeSelectorMatches`

Escopo da tradução:
- `selectors` / `excludeSelectors` / `excludeTags`
- `stayOriginalSelectors` / `stayOriginalTags`
- `extraInlineSelectors` / `extraBlockSelectors`

Estilo e layout:
- `translationClasses`: classes extras para o texto traduzido
- `globalStyles` / `globalAttributes`
- `injectedCss` / `additionalInjectedCss`
- `wrapperPrefix` / `wrapperSuffix`
- `blockMinTextCount` / `blockMinWordCount`

Momento e mobile:
- `urlChangeDelay` / `observeUrlChange`
- `isShowUserscriptPagePopup`

### Tradução de mensagens em fluxo estilo GPT

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

Mais detalhes de campos: veja no final em "Apêndice: Referência de Campos de Rule".

## Lógica de correspondência em "matches" (resumo)

- Domínio puro (sem `*`, sem caminho): compara apenas hostname.
- URL completa (sem `*`): compara protocolo + host + porta + caminho.
- Com `*` ou sem protocolo: usa regras de coringa (http/https/file suportados por padrão).

Exemplos comuns:
- `twitter.com` ✅ corresponde a `https://twitter.com/home`
- `*.twitter.com` ✅ corresponde a `https://mobile.twitter.com`, ❌ não corresponde a `https://twitter.com`
- `https://twitter.com/home` só corresponde a essa URL exata
- `twitter.com/*` corresponde a todas as rotas sob `twitter.com`

## Caso de adaptação de site (exemplo com Twitter)

Exemplo de regra interna do Twitter, mostrando uso típico de `selectors` / `excludeSelectors` / `globalStyles`:

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

- `selectors`: traduz apenas o conteúdo principal do tweet, evitando nomes/botões.
  ![tweet](https://s.immersivetranslate.com/assets/r2-uploads/tweet.png)
- `excludeSelectors`: exclui botões, navegação e elementos interativos.
  ![twitter-follow](https://s.immersivetranslate.com/assets/r2-uploads/twitter-follow.png)
- `globalStyles`: remove o limite de linhas para evitar corte na tradução.
  ![用户主页](https://s.immersivetranslate.com/assets/r2-uploads/twitterUser.png)

## Adaptação personalizada de sites

Você pode reutilizar regras internas via `id` e modificar incrementando com `.add/.remove`:

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

Observação:
- `id` herda regras internas, evitando repetição de `matches`.
- `.add/.remove` só altera itens no respectivo array, evitando sobrescrever.

IDs internos comuns (parcial):
- `isEbook`: leitor de epub
- `isEbookBuilder`: gerador de epub bilíngue
- `pdf`: página bilíngue para PDF

Lista completa de regras internas:
- `https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json`

## Configurando serviços de tradução

- `translationService`: motor de tradução padrão.
- `translationServices`: configurações por serviço e sobrescritas por site.
- `showUnconfiguredTranslationServiceInPopup`: esconde serviços não configurados.

Exemplo (com Tencent):

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

Notas:
- `matches` define onde o serviço é aplicado.
- `limit` limita a taxa de requisições por segundo.
- `maxTextGroupLengthPerRequest` / `maxTextLengthPerRequest` controlam o tamanho máximo de cada requisição.
- `apiUrl` permite definir URL personalizada.

### Configurando tempo limite da requisição (timeout máximo)

Pode-se definir o timeout (em ms) por serviço. Para serviços Pro, defina `proRequestTimeout`.

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
- Timeout muito alto faz aguardar muito; muito baixo, pode falhar frequentemente.
- O valor padrão depende do serviço (consulte a configuração final).
- `proRequestTimeout` só surte efeito quando `provider` for `pro` (serviço para assinantes).

## Idioma e Estratégia de Tradução

### Sempre/Nunca traduzir certos idiomas

```json
{
  "translationLanguagePattern": {
    "matches": ["en"],
    "excludeMatches": ["zh"]
  }
}
```

### Definindo idioma de origem para um site específico

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

Se desejar manter/renderizar HTML na tradução:

```json
{
  "enableRenderHtmlTag": true
}
```

## Estilo e tema da tradução

Temas suportados por `translationTheme` (confira configuração final):

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

## Parâmetros AI / Serviços Avançados

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

### Headers e body customizados

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

### Como usuários de modelos Gemini podem personalizar configurações

Modelos Gemini vêm com configs padrão internas; para sobrescrever, use `modelsOverrides`:

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

Dica: `modelsOverrides` funciona para outros serviços AI — corresponde pelo nome do modelo.

### Obedecer estritamente prompts customizados

> Para reduzir "alucinações" em LLMs, o plugin valida a contagem de tokens de resposta vs. requisição. Proporção muito alta/baixa = resultado inválido e uso de serviço secundário.
> Se seu prompt não for sobre tradução (mas expansão, revisão etc), pode disparar falso positivo; ative o modo estrito para ignorar a validação.

```json
{
  "translationServices": {
    "claude": {
      "strictPrompt": true
    }
  }
}
```

### Prompts multilíngues personalizados (exemplo)

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

Novo suporte a [Glossário AI](https://dash.immersivetranslate.com/#terms), válido só para serviços de tradução AI.

MT não usa glossário por padrão (pode degradar resultados). Para forçar (NÃO recomendado):

```json
{
  "enableMachineTranslateTerms": true
}
```

## Limpeza do Cache

Cache de tradução é limpo automaticamente a cada 30 dias para evitar sobrecarga.

```json
{
  "cacheMaxAgeDay": 30
}
```

## Injected CSS e globalStyles

- Injected CSS: CSS global para correção geral da página.
- globalStyles: aplica CSS por regra, útil para adaptação por site.

Exemplo de Injected CSS:

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

## Dicas de Troubleshooting

- `*.twitter.com` não cobre domínio raiz; escreva também `twitter.com`.
- `selectors` substitui o escopo original; prefira `.add/.remove`.
- Especificar `matches` como `example.com/path` ativa coringa; verifique se precisa da URL completa.
- Configuração não funciona? Consulte o resultado de merge final e recarregue a página.
- Vírgula extra no fim do JSON invalida a configuração.

## Apêndice: Referência de Campos Rule

Referência dos campos de Rule (documentação, lista parcial); consulte a config final para campos completos ou atualizados.
Dica: para arrays/objetos, use `.add` / `.remove` para modificar sem sobrescrever:

```typescript
export interface Rule {
  // Site correspondente
  id?: string; // ID de regra interna, para reutilizar regras internas
  matches?: string | string[]; // Sites para corresponder esta Rule
  excludeMatches?: string | string[]; // Excluir sites específicos
  selectorMatches?: string | string[]; // Corresponde por selector CSS, não por URL
  excludeSelectorMatches?: string | string[]; // Exclude por selector

  // Escopo de tradução
  selectors?: string | string[]; // Só traduz elementos correspondentes
  excludeSelectors?: string | string[]; // Não traduz elementos correspondentes
  excludeTags?: string | string[]; // Não traduz tags correspondentes

  // Adição incremental de escopos (caso falhe, use selectors.add / selectors.remove)
  additionalSelectors?: string | string[]; // Adiciona seleção para tradução
  additionalExcludeSelectors?: string | string[]; // Adiciona exclusão
  additionalExcludeTags?: string | string[]; // Adiciona exclusão (algumas versões obsoleto)

  // Manter original
  stayOriginalSelectors?: string | string[]; // Elementos mantidos originais
  stayOriginalTags?: string | string[]; // Tags mantidas originais, ex: code

  // Block ou Inline
  extraBlockSelectors?: string | string[]; // Elementos são blocos
  extraInlineSelectors?: string | string[]; // Elementos são inline
  inlineTags?: string | string[]; // Tags como inline
  preWhitespaceDetectedTags?: string | string[]; // Tags que detectam quebra de linha automática

  // Estilos na tradução
  translationClasses?: string | string[]; // Classes extras para o texto traduzido

  // Estilos globais
  globalStyles?: Record<string, string>; // Modifica CSS da página
  globalAttributes?: Record<string, Record<string, string | null>>; // Modifica atributos de elementos

  // CSS embutido
  injectedCss?: string | string[]; // CSS embutido
  additionalInjectedCss?: string | string[]; // CSS adicional

  // Contexto
  wrapperPrefix?: string; // Prefixo antes da área traduzida
  wrapperSuffix?: string; // Sufixo após a área traduzida

  // Troca de linha no texto traduzido
  blockMinTextCount?: number; // Tamanho mínimo de caracteres para bloco
  blockMinWordCount?: number; // Mínimo de palavras por bloco

  // Mínimo para traduzir
  containerMinTextCount?: number; // Mínimo de caracteres por elemento
  paragraphMinTextCount?: number; // Mínimo de caracteres por parágrafo
  paragraphMinWordCount?: number; // Mínimo de palavras por parágrafo

  // Máximo por linha para forçar quebra
  lineBreakMaxTextCount?: number; // Máximo de caracteres por linha

  // Momento de iniciar tradução
  urlChangeDelay?: number; // Delay após entrar na página
  observeUrlChange?: boolean; // Traduz novamente ao mudar URL

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Mostrar popup em mobile
  fingerCountToToggleTranslagePageWhenTouching?: number; // (obsoleto)

  // Tradução de streaming AI
  aiRule?: {
    streamingSelector: string; // Selector para marcar elemento em tradução
    messageWrapperSelector: string; // Selector do conteúdo da mensagem
    streamingChange: boolean; // Atualização incremental
  };
}
```
