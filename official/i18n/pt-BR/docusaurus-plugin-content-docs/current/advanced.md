---
sidebar_position: 4
---

# Opções avançadas de personalização

Você pode editar mais configurações personalizadas em Página de Configuração Estendida -> Configurações do Desenvolvedor -> Configuração do Usuário que não podem ser editadas na interface do usuário para usuários avançados, consulte a última nota para obter mais detalhes sobre os parâmetros. A configuração interna atual pode ser encontrada [aqui](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

## Regras do usuário

Com `Rules` (Regras), é possível personalizar a configuração de um site específico, decidindo qual conteúdo precisa ser traduzido ou não, ou ajustando o estilo das páginas, etc.

```json
[
  {
    "matches": "www.google.com",
    "selectors": [".title"]
  },
  {
    "matches": "*.twitter.com",
    "selectors": [".text"],
    "excludeSelectors": ["nav", "footer"]
  }
]
```

Use `matches` para corresponder ao site correspondente. Caracteres curinga são permitidos, por exemplo, `*.google.com`, `www.google.com/test/*`, `file://*`.

Usar `selectors` substitui o escopo de tradução inteligente, traduzindo apenas os elementos correspondidos por esse seletor.

Use `excludeSelectors` para excluir elementos sem traduzir a posição.

Use a família de seletores `additional` (adicional) para aumentar ou diminuir o intervalo de tradução com base na tradução inteligente.

```json
[
  {
    "matches": "www.google.com",
    "additionalSelectors": [],
    "additionalExcludeSelectors": []
  }
]
```

Se você quiser traduzir uma região enquanto trata os elementos como um todo e não os separa, você pode usar o seletor `atomicBlockSelectors`. Por exemplo, perfis do Instagram. Observe que usar `atomicBlockSelectors` exige selecionar com `selectors` antes de usar `atomicBlockSelectors`.

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div. ._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Se os resultados da tradução resultarem em páginas desalinhadas, texto sobreposto e outros casos extremos, você pode usar `globalStyles` para ajustar o estilo da página para corrigi-lo. Por exemplo, o cabeçalho do YouTube, que é usado para remover a altura máxima da página original.

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## Melhorias na consolidação de regras do usuário

Suporte a partir da versão 0.7.4. Veja o exemplo de pular a zona de não tradução:

```json
{
  "matches": "https://www.elektrotechnik.rwth-aachen.de/*",
  "additionalExcludeSelectors.remove": [".notranslate", "[translate=no]"]
}
```

As operações de adicionar e remover modificam as regras fornecidas por padrão e não precisam ser substituídas por completo, como era o caso anteriormente.

## CSS injetado

O CSS injetado permite que você injete estilos da web personalizados globalmente. Pode ser usado com `translationClasses` das `Rules`.

```
".immersive-translate-target-wrapper img { width: 16px; height: 16px }"
```

Também é possível estilizar o site de uma forma mais personalizada, como um gerenciador de estilos da web comum (até mesmo utilizando `display:none` para remover anúncios).

```css
.title {
  color: red;
}
```

## Configuração do usuário

A Configuração permite personalizar a configuração deste plugin, como serviços de tradução, opções de tradução de idiomas específicas de idioma, etc.

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
    "fingerCountToToggleTranslagePageWhenTouching": 4
  },
  "rules": [
    {
      "matches": "www.google.com",
      "selectors": [".class"]
    }
  ]
}
```

Os campos de regra em `rules` podem usar todos os campos em `generalRule`. As `rules` têm a prioridade mais alta, mesclando a `generalRule` e as regras para aquela `rule` quando uma `rule` específica para um site específico é correspondida.

Apresentando alguns dos campos comuns da Configuração.

### Não mostrar serviços de tradução não configurados no painel popup

`"showUnconfiguredTranslationServiceInPopup": false`

### Configuração de serviços de tradução

Use `translationService` para selecionar o mecanismo de tradução padrão, que atualmente suporta:

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

Use `translationServices` para configurar a `apikey` de cada serviço de tradução, diferentes provedores de serviço precisam de parâmetros diferentes, e suas chaves de API podem ser solicitadas no centro de desenvolvedores de seus respectivos sites.

Por exemplo, o Tencent Translator, você precisa configurar `secretId`, `secretKey`. Você pode ir para a Tencent Cloud para solicitar uma chave de API com 5 milhões de caracteres gratuitos por mês. Consulte [aqui](/docs/services/tencent) para o processo de solicitação.

```json
"translationServices": {
  "tencent": {
    "secretId": "xxx",
    "secretKey": "xxx",
    "matches":["*.twitter.com"],
    "limit": 3,
    "apiUrl":"",
    "maxTextGroupLengthPerRequest": 25,
    "maxTextLengthPerRequest": 1800
  }
}
```

Campo `matches`, usando este serviço de tradução para um site específico.

O campo `limit`, que especifica o número máximo de solicitações por segundo para este serviço de tradução (alguns serviços limitam o número máximo de solicitações por segundo).

Campo `maxTextGroupLengthPerRequest`, número máximo de parágrafos por solicitação.

Campo `maxTextLengthPerRequest`, número máximo de caracteres por solicitação.

`apiUrl` Permite personalizar o endereço da interface de tradução.

### Sempre traduzir sites específicos

`translationUrlPattern` Configura sites que são sempre traduzidos e sites que nunca são traduzidos.

- `matches` configura o site que é sempre traduzido.
- `excludeMatches` configura sites que nunca são traduzidos.

Os valores de configuração podem ser nomes de domínio ou URLs com `*`, como: `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### Sempre traduzir idiomas específicos

`translationLanguagePattern`, configura o idioma que é sempre traduzido e o idioma que nunca é traduzido.

- `matches` Configura o idioma que é sempre traduzido, por exemplo, `en`.
- `excludeMatches` Configura os idiomas que nunca são traduzidos.

### Formato de exibição da tradução

`translationTheme` é o formato de exibição da tradução e atualmente suporta os seguintes estilos:

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
| "thinDashed"
```

Nome correspondente em português:

```json
{
  "none": "nenhum",
  "dashed": "sublinhado tracejado",
  "dotted": "sublinhado pontilhado",
  "underline": "sublinhado com linha reta",
  "mask": "efeito de desfoque",
  "paper": "efeito de sombra de papel branco",
  "highlight": "Destacar",
  "blockquote": "estilo de citação",
  "weakening": "enfraquecimento",
  "italic": "itálico",
  "bold": "negrito",
  "thinDashed": "Linhas finas pontilhadas"
}
```

`translationThemePatterns` permite configurar diferentes estilos de tradução para diferentes sites.

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### Tradução de mensagens de fluxo de página do Class GPT

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

### Regras

`rules` é um objeto de matriz que permite configurar regras para sites especiais, como fazer o Twitter traduzir apenas uma determinada parte de uma região:

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

As `rules` internas atuais podem ser encontradas [aqui](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

Alguns dos campos importantes são selecionados abaixo para ilustração:

```typescript
export interface Rule {
  // Match the website (Corresponder ao site)
  id?: string; // Cada regra de adaptação tem seu próprio id, se os usuários quiserem reutilizar esta regra além desta alteração, eles precisam adicionar este id correspondente à sua própria regra para reutilizá-la.
  matches?: string | string[]; // Esta regra só corresponderá ao site aqui.
  excludeMatches?: string | string[]; // Excluir sites específicos.
  selectorMatches?: string | string[]; // Corresponder com um seletor sem especificar todos os URLs
  excludeSelectorMatches?: string | string[]; // Excluir regras, como acima.

  // Specify range of translations (Especificar intervalo de traduções)
  selectors?: string | string[]; // Traduzir apenas elementos que correspondem
  excludeSelectors?: string | string[]; // Excluir elementos, não traduzir correspondências
  excludeTags?: string | string[]; // Excluir tags, não traduzir tags correspondentes

  // append translation ranges instead of overriding (acrescentar intervalos de tradução em vez de substituir)
  additionalSelectors?: string | string[]; // acrescentar intervalos de tradução. Acrescentar locais de tradução às regiões traduzidas de forma inteligente.
  additionalExcludeSelectors?: string | string[]; // Acrescentar elementos de exclusão para que a tradução inteligente não traduza locais específicos.
  additionalExcludeTags?: string | string[]; // Tags de exclusão adicionais

  // Leave as is (Deixar como está)
  stayOriginalSelectors?: string | string[]; // Os elementos correspondentes serão deixados como estão. Comumente usado em tags de sites de fóruns.
  stayOriginalTags?: string | string[]; // As tags correspondentes serão deixadas como estão, por exemplo, `code`

  // Regional translations (Traduções regionais)
  atomicBlockSelectors?: string | string[]; // Seletores regionais, os elementos correspondentes serão tratados como um todo, não traduzidos em seções.
  atomicBlockTags?: string | string[]; // Seletores de tags de área, igual ao anterior

  // Block or Inline (Bloco ou Inline)
  extraBlockSelectors?: string | string[]; // Seletores extras, os elementos correspondentes serão tratados como elementos de bloco, não traduzidos em uma linha.
  extraInlineSelectors?: string | string[]; // Seletores extras que serão usados como elementos inline.

  inlineTags?: string | string[]; // A tag correspondente será usada como um elemento inline
  preWhitespaceDetectedTags?: string | string[]; // A tag correspondente será automaticamente envolvida

  // Translation style (Estilo de tradução)
  translationClasses?: string | string | string[]; // Adicionar classes adicionais à tradução

  // Global Styles (Estilos globais)
  globalStyles?: Record<string, string>; // Modificar estilos de página, útil se a tradução causar problemas na página.
  globalAttributes?: Record<string, Record<string, string>>; // Modificar atributos de elementos da página

  // Embedded styles (Estilos incorporados)
  injectedCss?: string | string[]; // Incorporar estilos CSS
  additionalInjectedCss?: string | string[]; // Estilos CSS adicionais em vez de substituí-los.

  // Context (Contexto)
  wrapperPrefix?: string; // O prefixo da área de tradução, o padrão é inteligente, com ou sem quebras de linha dependendo do número de caracteres.
  wrapperSuffix?: string; // Sufixo da área de tradução

  // Number of characters to wrap the translation (Número de caracteres para quebrar a tradução)
  blockMinTextCount?: number; // Número mínimo de caracteres para quebrar a tradução como um bloco, caso contrário, a tradução é um elemento inline.
  blockMinWordCount?: number; // Igual ao anterior. Se você quiser que eles sempre tenham uma nova linha, você pode colocar 0 em ambos.

  // Minimum number of characters that can be translated from the content (Número mínimo de caracteres que podem ser traduzidos do conteúdo)
  containerMinTextCount?: number; // Número mínimo de caracteres que um elemento deve conter antes de ser traduzido, o padrão é 18
  paragraphMinTextCount?: number; // Número mínimo de caracteres para o parágrafo, maior que o número de caracteres que o conteúdo deve conter.
  paragraphMinWordCount?: number; // Número mínimo de palavras no parágrafo original

  // Forced line breaks for long paragraphs (Quebras de linha forçadas para parágrafos longos)
  lineBreakMaxTextCount?: number; // Número máximo de caracteres no parágrafo para ser forçado a quebrar ao traduzir um parágrafo longo.

  // When to start translation. (Quando iniciar a tradução.)
  urlChangeDelay?: number; // Quantos milissegundos para atrasar a tradução após entrar na página. Para esperar a página inicializar, o padrão é 250ms.
  observeUrlChange?: boolean; // Detectar quando o endereço da URL mudou e iniciar a tradução novamente, verdadeiro por padrão.

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Mostrar o pop-up da página em dispositivos móveis. Janela flutuante, verdadeiro por padrão.
  fingerCountToToggleTranslagePageWhenTouching?: number; // Traduz quando quatro dedos tocam, pode ser definido como 0, 2, 3, 4, 5

  // AI streaming translations (Traduções de streaming de IA)
  aiRule: {
    streamingSelector: string; // Seletor para marcar o elemento sendo traduzido na página da web gpt
    messageWrapperSelector: string; // Seletor do corpo da mensagem
    streamingChange: boolean; // Se a mensagem é atualizada de forma incremental ou completa para a iteração da página da web do Class GPT. Class GPT é incremental.
  };
}
```

**Mais explicações**

Diferença entre bloco e inline, se você quiser saber mais, pode ver [aqui](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline)

- O elemento de bloco ocupa uma única linha e vários elementos de bloco vizinhos ocupam cada um uma nova linha.
- O elemento inline não ocupa uma única linha; vários elementos inline vizinhos são organizados na mesma linha e uma nova linha não é criada até que uma linha seja demais.
