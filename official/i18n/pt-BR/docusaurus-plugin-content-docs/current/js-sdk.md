---
sidebar_position: 5
---

# JS SDK

O JS SDK do Immersive Translate pode ajudar você a implementar tradução bilíngue em seu site.

## Como usar

> Antes de depurar o JS SDK, desative a extensão do Immersive Translate

1. Configure os parâmetros de inicialização (observe que se o immersiveTranslateConfig não for configurado, o JS SDK falhará na inicialização, você pode definir um objeto vazio)

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. Adicione o seguinte código `script` antes do `</head>` da sua página

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
```

Exemplo

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

## Parâmetros

- `pageRule`
  Pode ser configurado para personalizar o site, decidindo quais conteúdos precisam ser traduzidos ou ajustando o estilo da página.
- `isAutoTranslate`
  Tradução automática imediata

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

Usar `selectors` irá sobrepor o alcance da tradução inteligente, traduzindo apenas os elementos que correspondem ao seletor.

Usar `excludeSelectors` pode excluir elementos, não traduzindo essa posição.

Usar `selectors.add` adicionará alguns seletores com base no padrão.

Usar `selectors.remove` removerá alguns seletores com base no padrão.

Se você deseja traduzir uma área específica tratando o elemento como um todo, sem dividi-lo em linhas, pode usar o seletor `atomicBlockSelectors`. É importante notar que, antes de usar `atomicBlockSelectors`, você precisa selecionar com `selectors`.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Mais explicações sobre os parâmetros de `pageRule`:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Excluir sites específicos.
  selectorMatches?: string | string[]; // Usar seletor para corresponder, sem precisar especificar todas as URLs.
  excludeSelectorMatches?: string | string[]; // Regras de exclusão, como acima.

  // Faixa de tradução especificada
  selectors?: string | string[]; // Apenas traduzir elementos correspondentes
  excludeSelectors?: string | string[]; // Excluir elementos, não traduzir elementos correspondentes
  excludeTags?: string | string[]; // Excluir Tags, não traduzir Tags correspondentes

  // Adicionar faixa de tradução, em vez de substituir
  additionalSelectors?: string | string[]; // Adicionar faixa de tradução. Na área de tradução inteligente, adicionar posição de tradução.
  additionalExcludeSelectors?: string | string[]; // Adicionar elementos de exclusão, para que a tradução inteligente não traduza posições específicas.
  additionalExcludeTags?: string | string[]; // Adicionar Tags de exclusão

  // Manter original
  stayOriginalSelectors?: string | string[]; // Elementos correspondentes serão mantidos como estão. Comumente usado para tags de sites de fórum.
  stayOriginalTags?: string | string[]; // Tags correspondentes serão mantidas como estão, como `code`

  // Tradução de área
  atomicBlockSelectors?: string | string[]; // Seletor de área, elementos correspondentes serão tratados como um todo, não serão traduzidos em partes
  atomicBlockTags?: string | string[]; // Seletor de Tag de área, como acima

  // Bloco ou Inline
  extraBlockSelectors?: string | string[]; // Seletor extra, elementos correspondentes serão tratados como elementos de bloco, ocupando uma linha inteira.
  extraInlineSelectors?: string | string[]; // Seletor extra, elementos correspondentes serão tratados como elementos inline.

  inlineTags?: string | string[]; // Tags correspondentes serão tratadas como elementos inline
  preWhitespaceDetectedTags?: string | string[]; // Tags correspondentes serão automaticamente quebradas em linhas

  // Estilo de tradução
  translationClasses?: string | string | string[]; // Adicionar classes extras à tradução

  // Estilos globais
  globalStyles?: Record<string, string>; // Modificar estilo da página, útil se a tradução causar desordem na página.
  globalAttributes?: Record<string, Record<string, string>>; // Modificar atributos de elementos da página

  // CSS embutido
  injectedCss?: string | string[]; // CSS embutido
  additionalInjectedCss?: string | string[]; // Adicionar CSS, em vez de substituir diretamente.

  // Contexto
  wrapperPrefix?: string; // Prefixo da área de tradução, padrão é smart, decide se quebra linha com base no número de palavras.
  wrapperSuffix?: string; // Sufixo da área de tradução

  // Número de caracteres para quebra de linha na tradução
  blockMinTextCount?: number; // Número mínimo de caracteres para que a tradução seja tratada como bloco, caso contrário, será elemento inline.
  blockMinWordCount?: number; // Igual ao acima. Se quiser que sempre quebre linha, pode preencher ambos com 0.

  // Número mínimo de caracteres para conteúdo traduzível
  containerMinTextCount?: number; // Na identificação inteligente, número mínimo de caracteres que o elemento deve conter para ser traduzido, padrão é 18
  paragraphMinTextCount?: number; // Número mínimo de caracteres do parágrafo original, conteúdo maior que o número será traduzido
  paragraphMinWordCount?: number; // Número mínimo de palavras do parágrafo original

  // Número de caracteres para forçar quebra de linha em parágrafos longos
  lineBreakMaxTextCount?: number; // Ao traduzir parágrafos longos, número máximo de caracteres do parágrafo para forçar quebra de linha.

```markdown
// Momento de iniciar a tradução
urlChangeDelay?: number; // Após entrar na página, quantos milissegundos de atraso antes de iniciar a tradução. Para aguardar a inicialização da página, atualmente o padrão é 250ms

// Tradução por streaming de AI
aiRule: {
    streamingSelector: string; // Seletor que marca o elemento em tradução na página gpt
    messageWrapperSelector: string; // Seletor do corpo da mensagem
    streamingChange: boolean; // Mensagens repetidas em páginas tipo gpt são atualizações incrementais ou totais. gpt é incremental
};
```
