---
sidebar_position: 4
---

# Opções de personalização avançadas

Você pode editar configurações personalizadas mais avançadas na Página de Configuração Estendida -> Configurações do Desenvolvedor -> Configuração do Usuário que não são editáveis na UI para usuários avançados, veja a última nota para mais detalhes sobre os parâmetros. A `config` integrada atual pode ser encontrada [aqui](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

## Regras do Usuário

Com `Regras`, é possível personalizar a configuração de um site específico, decidindo que conteúdo precisa ser traduzido ou não, ou ajustando o estilo das páginas, etc.

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

Use `matches` para corresponder ao site correspondente. Curingas são permitidos, por exemplo, `*.google.com`, `www.google.com/test/*`, `file://*`.

Usar `selectors` substitui o escopo de tradução inteligente, traduzindo apenas os elementos correspondidos por esse seletor.

Use `excludeSelectors` para excluir elementos sem traduzir a posição.

Use a família de seletores `additional` para aumentar ou diminuir o alcance da tradução com base na tradução inteligente.

```json
[
  {
    "matches": "www.google.com",
    "additionalSelectors": [],
    "additionalExcludeSelectors": []
  }
]
```

Se você quiser traduzir uma região tratando os elementos como um todo e não separando-os, você pode usar o seletor `atomicBlockSelectors`. Por exemplo, perfis no Instagram. Note que usar `atomicBlockSelectors` requer selecionar com `selectors` antes de usar `atomicBlockSelectors`.

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Se a tradução resultar em páginas desalinhadas, texto sobreposto e outros casos extremos, você pode usar `globalStyles` para ajustar o estilo da página para corrigi-lo. Por exemplo, o cabeçalho do youtube, que é usado para remover a altura máxima da página original.

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## Aprimoramentos na consolidação de regras de usuário

Suporte a partir da versão 0.7.4. Tomando como exemplo a opção de pular a zona sem tradução

```json
{
  "matches": "https://www.elektrotechnik.rwth-aachen.de/*",
  "additionalExcludeSelectors.remove": [".notranslate", "[translate=no]"]
}
```

As operações de adicionar e remover modificam as regras fornecidas por padrão e não precisam ser substituídas por completo, como era o caso anteriormente.

## CSS Injetado

CSS injetado permite que você insira estilos web personalizados globalmente. Pode ser usado com `translationClasses` das `Rules`.

```
".immersive-translate-target-wrapper img { width: 16px; height: 16px }"
```

Também é possível estilizar o site de uma maneira mais personalizada, como um gerenciador de estilo web regular. (inclusive utilizando `display:none` para remover anúncios)

```css
.title {
  color: red;
}
```

## Configuração do Usuário

A configuração permite que você personalize a configuração deste plugin, como serviços de tradução, opções de tradução de idiomas específicos, etc.

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["*.twitter.com"]
    }
  },
  "translationUrlPattern": {
    "excludeMatches": ["www.google.com"]
  },
  "translationLanguagePattern": {
    "matches": ["en"]
  },
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  },
  "generalRule": {
    "_comment": "",
    "normalizeBody": "",
    "injectedCss": [],
    "additionalInjectedCss": [],
    "wrapperPrefix": "smart",
    "wrapperSuffix": "smart",
    "isPdf": false,
    "isTransformPreTagNewLine": false,
    "urlChangeDelay": 20,
    "isShowUserscriptPagePopup": true,
    "observeUrlChange": true,
    "paragraphMinTextCount": 8,
    "paragraphMinWordCount": 2,
    "blockMinTextCount": 32,
    "blockMinWordCount": 5,
    "containerMinTextCount": 18,
    "lineBreakMaxTextCount": 0,
    "globalAttributes": {},
    "globalStyles": {},
    "selectors": [],
    "preWhitespaceDetectedTags": ["DIV", "SPAN"],
    "stayOriginalSelectors": [],
    "additionalSelectors": [],
    "atomicBlockTags": [],
    "excludeSelectors": [],
    "additionalExcludeSelectors": [],
    "translationClasses": [],
    "atomicBlockSelectors": [],
    "excludeTags": [],
    "metaTags": ["META", "SCRIPT", "STYLE", "NOSCRIPT"],
    "additionalExcludeTags": [],
    "stayOriginalTags": ["CODE", "TT", "IMG", "SUP"],
    "additionalStayOriginalTags": [],
    "inlineTags": [],
    "additionalInlineTags": [],
    "extraInlineSelectors": [],
    "additionalInlineSelectors": [],
    "extraBlockSelectors": [],
    "allBlockTags": [],
    "pdfNewParagraphLineHeight": 2.4,
    "pdfNewParagraphIndent": 1.2,
    "pdfNewParagraphIndentRightIndentPx": 130,
    "fingerCountToToggleTranslatePageWhenTouching": 4
  },
  "rules": [
    {
      "matches": "www.google.com",
      "selectors": [".class"]
    }
  ]
}
```

Os campos de regra em `rules` podem usar todos os campos em `generalRule`. As `rules` têm a maior prioridade, mesclando o `generalRule` e as regras para aquela `rule` quando uma `rule` específica para um site específico é correspondida.

Introduzindo alguns dos campos comuns de Config.

### Não exibir serviços de tradução não configurados no painel popup

`"showUnconfiguredTranslationServiceInPopup": false`

### Configuração dos serviços de tradução

Use `translationService` para selecionar o motor de tradução padrão, que atualmente suporta:

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

Use `translationServices` para configurar o `apikey` de cada serviço de tradução, diferentes provedores de serviços precisam de diferentes parâmetros, e suas chaves API podem ser solicitadas no centro de desenvolvedores de seus respectivos sites.

Por exemplo, para o Tradutor da Tencent, você precisa configurar `secretId`, `secretKey`. Você pode ir até a Nuvem da Tencent para solicitar uma chave API com 5 milhões de caracteres gratuitos por mês. Consulte [aqui](/docs/services/tencent) para o processo de aplicação.

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

Campo `matches`, usando este serviço de tradução para um site específico.

O campo `limit`, que especifica o número máximo de solicitações por segundo para este serviço de tradução (alguns serviços limitam o número máximo de solicitações por segundo).

Campo `maxTextGroupLengthPerRequest`, número máximo de parágrafos por solicitação.

Campo `maxTextLengthPerRequest`, número máximo de caracteres por solicitação.

`apiUrl` Permite personalizar o endereço da interface de tradução.

### Sempre traduza sites específicos

`translationUrlPattern` Configura sites que são sempre traduzidos, e sites que nunca são traduzidos.

- `matches` configuração sempre traduz o site.
- `excludeMatches` Configura sites que nunca são traduzidos.

Os valores de configuração podem ser nomes de domínio ou URLs com `*`, como: `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### Sempre traduza idiomas específicos

translationLanguagePattern, configura o idioma que é sempre traduzido e o idioma que nunca é traduzido.

- `matches` Configura o idioma que é sempre traduzido, por exemplo, `en`,
- `excludeMatches` Configura os idiomas que nunca são traduzidos.

### Formato de exibição da tradução

`translationTheme` é o formato de exibição da tradução, e atualmente suporta os seguintes estilos:

```typescript
| "none"
| "tracejado"
| "pontilhado"
| "sublinhado"
| "mascara"
| "papel"
| "destaque"
| "blocoDeCitação"
| "enfraquecimento"
| "italico"
| "negrito"
| "tracejadoFino".
```

Nome correspondente em português:

```json
{
  "none": "nenhum",
  "tracejado": "sublinhado tracejado",
  "pontilhado": "sublinhado pontilhado",
  "sublinhado": "sublinhado reto",
  "mascara": "efeito de desfoque",
  "papel": "efeito de sombra de papel branco",
  "destaque": "destaque",
  "blocoDeCitação": "estilo de citação",
  "enfraquecimento": "enfraquecimento",
  "italico": "itálico",
  "negrito": "negrito",
  "tracejadoFino": "sublinhado tracejado fino"
}
```

`translationThemePatterns` permite configurar diferentes estilos de tradução para diferentes sites.

```json
"translationThemePatterns": {
  "sublinhado": {
    "matches": ["discord.com"]
  }
}
```

### Tradução de Mensagem de Fluxo de Página gpt Class

```json
{
  "matches": ["chat.openai.com"],
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".resultado-streaming.markdown ",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

### Regras

`rules` é um objeto de array que permite configurar regras para sites especiais, como fazer com que o Twitter traduza apenas uma certa parte de uma região:

```json
{
  "rules": [
    {
      "id": "twitter",
      "matches": ["twitter.com", "mobile.twitter.com", "tweetdeck.twitter.com"],
      "selectors": [
        "[data-testid=' tweetText']",
        ".tweet-text",
        ".js-quoted-tweet-text",
        "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
        "[data-testid=' developerBuiltCardContainer'] > div:nth-child(2)",
        "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)"
      ],
      "extraInlineSelectors": ["[data-testid=\"tweetText\"] div"]
    }
  ]
}
```

As `rules` integradas atuais podem ser encontradas [aqui](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

Alguns dos campos importantes são selecionados abaixo para ilustração:

````typescript
export interface Rule {
  // Corresponder ao site
  id?: string; // Cada regra de adaptação tem seu próprio id, se os usuários quiserem reutilizar esta regra além desta mudança, eles precisam adicionar este id correspondente à sua própria regra para reutilizá-la
  matches?: string | string[]; // Esta regra só corresponderá ao site aqui. Esta regra só corresponderá aos sites aqui.
  excludeMatches?: string | string[]; // Excluir sites específicos.
  selectorMatches?: string | string[]; // Corresponder com um seletor sem especificar todos os URLs
  excludeSelectorMatches?: string | string[]; // Excluir regras, como acima.

  // Especificar alcance das traduções
  selectors?: string | string[]; // Traduzir apenas elementos que correspondam
  excludeSelectors?: string | string[]; // Excluir elementos, não traduzir correspondências
  excludeTags?: string | string[]; // Excluir Tags, não traduzir Tags correspondentes

  // acrescentar alcances de tradução em vez de substituir
  additionalSelectors?: string | string[]; // acrescentar alcances de tradução. Acrescentar locais de tradução às regiões traduzidas inteligentemente.
  additionalExcludeSelectors?: string | string[]; // Acrescentar elementos excluídos para que a tradução inteligente não traduza locais específicos.
  additionalExcludeTags?: string | string[]; // Tags excluídas adicionais

  // Deixar como está
  stayOriginalSelectors?: string | string[]; // Elementos correspondentes serão deixados como estão. Comumente usado em tags de sites de fóruns.
  stayOriginalTags?: string | string[]; // Tags correspondentes serão deixadas como estão, por exemplo, `code`

  // Traduções regionais
  atomicBlockSelectors?: string | string[]; // Seletores regionais, elementos correspondentes serão tratados como um todo, não traduzidos em seções.
  atomicBlockTags?: string | string[]; // Seletores de Tag de área, o mesmo que acima

  // Bloco ou Linha
```javascript
  extraBlockSelectors?: string | string[]; // Seletores extras, elementos correspondentes serão tratados como elementos de bloco, não traduzidos em uma linha.
  extraInlineSelectors?: string | string[]; // Seletores extras que serão usados como elementos inline.

  inlineTags?: string | string[]; // Tag correspondente será usada como um elemento inline
  preWhitespaceDetectedTags?: string | string[]; // Tag correspondente será automaticamente envolvida

  // Estilo de tradução
  translationClasses?: string | string | string[]; // Adicionar classes adicionais à tradução

  // Estilos Globais
  globalStyles?: Record<string, string>; // Modificar estilos da página, útil se a tradução fizer a página ficar bagunçada.
  globalAttributes?: Record<string, Record<string, string>>; // Modificar atributos dos elementos da página

  // Estilos embutidos
  injectedCss?: string | string[]; // Embutir estilos CSS
  additionalInjectedCss?: string | string[]; // Estilos CSS adicionais em vez de substituí-los.

  // Contexto
  wrapperPrefix?: string; // O prefixo da área de tradução, padrão é inteligente, com ou sem quebras de linha dependendo do número de caracteres.
  wrapperSuffix?: string; // Sufixo da área de tradução

  // Número de caracteres para envolver a tradução
  blockMinTextCount?: number; // Número mínimo de caracteres para envolver a tradução como um bloco, caso contrário, a tradução é um elemento inline.
  blockMinWordCount?: number; // O mesmo que acima. Se você quiser que eles sejam sempre em nova linha, você pode colocar 0 em ambos.

  // Número mínimo de caracteres que podem ser traduzidos do conteúdo
  containerMinTextCount?: number; // Número mínimo de caracteres que um elemento deve conter antes de ser traduzido, padrão é 18
  paragraphMinTextCount?: number; // Número mínimo de caracteres para o parágrafo, maior que o número de caracteres que o conteúdo deve conter.
  paragraphMinWordCount?: number; // Número mínimo de palavras no parágrafo original

  // Quebras de linha forçadas para parágrafos longos
  lineBreakMaxTextCount?: number; // Número máximo de caracteres no parágrafo para ser forçado a quebrar quando traduzindo um parágrafo longo.

  // Quando começar a tradução.
  urlChangeDelay?: number; // Quantos milissegundos para atrasar a tradução após entrar na página. Para esperar a página inicializar, padrão é 250ms
  observeUrlChange?: boolean; // Detectar quando o endereço da url mudou e começar a tradução novamente, verdadeiro por padrão.

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Mostrar o popup da página em dispositivos móveis. janela flutuante, verdadeiro por padrão.
  fingerCountToToggleTranslagePageWhenTouching?: number; // Traduz quando quatro dedos tocam, pode ser definido para 0, 2, 3, 4, 5

  // Traduções em streaming de IA
  aiRule: {
    streamingSelector: string; // Seletor para marcar o elemento sendo traduzido na página web gpt
    messageWrapperSelector: string; // Seletor do corpo da mensagem
    streamingChange: boolean; // Se a mensagem é atualizada incrementalmente ou completamente para a iteração da página web gpt. gpt é incremental
  };
}
````

**Mais explicações**

Diferença entre bloco e inline, se você quiser saber mais, pode ver [aqui](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline)

- O elemento de bloco ocupa uma única linha, e múltiplos elementos de bloco vizinhos ocupam cada um uma nova linha.
- O elemento inline não ocupa uma única linha; múltiplos elementos inline vizinhos são organizados na mesma linha, e uma nova linha não é criada até que uma linha esteja demasiado cheia.
