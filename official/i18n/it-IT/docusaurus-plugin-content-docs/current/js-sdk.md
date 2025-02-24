---
sidebar_position: 5
---

# JS SDK

L'SDK Immersive Translate JS ti aiuta a implementare la traduzione bilingue sul tuo sito web.

## Come Utilizzare

1. Inizializza Immersive Translate:

```js
<script>
  window.immersiveTranslateConfig = {
    pageRule: {}
  }
</script>
```

2. Aggiungi il seguente codice `script` alla tua pagina web

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
```

Esempio

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

## Parametri

Con `pageRule`, puoi personalizzare la configurazione del sito web, decidendo quale contenuto deve essere tradotto o regolando gli stili della pagina web.

```js
initImmersiveTranslate({
  pageRule: {
    selectors: [".text"],
    excludeSelectors: ["nav", "footer"],
  },
});
```

Usare `selectors` sovrascriverà l'intervallo di traduzione intelligente, traducendo solo gli elementi corrispondenti al selettore.

Usare `excludeSelectors` può escludere elementi dalla traduzione.

Usare `selectors.add` aggiungerà alcuni selettori in cima a quelli predefiniti.

Usare `selectors.remove` rimuoverà alcuni selettori da quelli predefiniti.

Se vuoi tradurre un'area specifica e considerare un elemento come un tutto senza suddividerlo in righe, puoi usare il selettore `atomicBlockSelectors`. Nota che devi selezionare gli elementi usando `selectors` prima di usare `atomicBlockSelectors`.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Ulteriori spiegazioni sui parametri di `pageRule`:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Escludi siti web specifici.
  selectorMatches?: string | string[]; // Corrispondenza usando selettori senza specificare tutti gli URL
  excludeSelectorMatches?: string | string[]; // Escludi regole, come sopra.

  // Specifica l'intervallo di traduzione
  selectors?: string | string[]; // Traduci solo elementi corrispondenti
  excludeSelectors?: string | string[]; // Escludi elementi, non tradurre elementi corrispondenti
  excludeTags?: string | string[]; // Escludi tag, non tradurre tag corrispondenti

  // Aggiungi intervallo di traduzione, non sovrascrivere
  additionalSelectors?: string | string[]; // Aggiungi intervallo di traduzione. Aggiungi posizioni di traduzione in aree di traduzione intelligente.
  additionalExcludeSelectors?: string | string[]; // Aggiungi elementi esclusi per prevenire la traduzione intelligente in posizioni specifiche.
  additionalExcludeTags?: string | string[]; // Aggiungi tag esclusi

  // Mantieni originale
  stayOriginalSelectors?: string | string[]; // Gli elementi corrispondenti rimarranno originali. Comunemente usato per tag su siti web di forum.
  stayOriginalTags?: string | string[]; // I tag corrispondenti rimarranno originali, come `code`

  // Traduzione regionale
  atomicBlockSelectors?: string | string[]; // Selettore di regione, gli elementi corrispondenti saranno considerati come un tutto, non tradotti in segmenti
  atomicBlockTags?: string | string[]; // Selettore di tag di regione, come sopra

  // Blocco o Inline
  extraBlockSelectors?: string | string[]; // Selettori extra, gli elementi corrispondenti saranno trattati come elementi di blocco, occupando una linea.
  extraInlineSelectors?: string | string[]; // Selettori extra, gli elementi corrispondenti saranno trattati come elementi inline.

  inlineTags?: string | string[]; // I tag corrispondenti saranno trattati come elementi inline
  preWhitespaceDetectedTags?: string | string[]; // I tag corrispondenti avvolgeranno automaticamente le righe

  // Stili di traduzione
  translationClasses?: string | string | string[]; // Aggiungi classi extra alla traduzione

  // Stili globali
  globalStyles?: Record<string, string>; // Modifica gli stili della pagina, utile quando le traduzioni causano disordine nella pagina.
  globalAttributes?: Record<string, Record<string, string>>; // Modifica gli attributi degli elementi della pagina

  // Stili incorporati
  injectedCss?: string | string[]; // Incorpora stili CSS
  additionalInjectedCss?: string | string[]; // Aggiungi stili CSS invece di sovrascrivere direttamente.

  // Contesto
  wrapperPrefix?: string; // Prefisso dell'area di traduzione, predefinito è smart, decide se avvolgere le righe in base al numero di caratteri.
  wrapperSuffix?: string; // Suffisso dell'area di traduzione

  // Conteggio caratteri di avvolgimento traduzione
  blockMinTextCount?: number; // Conteggio minimo di caratteri per la traduzione come blocco, altrimenti, la traduzione sarà un elemento inline.
  blockMinWordCount?: number; // Come sopra. Per avvolgere sempre le righe, imposta entrambi a 0.

  // Conteggio minimo di caratteri per contenuto traducibile
  containerMinTextCount?: number; // Conteggio minimo di caratteri per elementi da tradurre durante il riconoscimento intelligente, predefinito è 18
  paragraphMinTextCount?: number; // Conteggio minimo di caratteri per paragrafo originale, contenuto maggiore del numero sarà tradotto
  paragraphMinWordCount?: number; // Conteggio minimo di parole per paragrafo originale

  // Conteggio caratteri di interruzione forzata per paragrafi lunghi
  lineBreakMaxTextCount?: number; // Conteggio massimo di caratteri per interruzione forzata quando si traducono paragrafi lunghi.

  // Momento per iniziare la traduzione
  urlChangeDelay?: number; // Ritardo in millisecondi prima di iniziare la traduzione dopo l'ingresso nella pagina. Predefinito è 250ms per attendere l'inizializzazione della pagina web.

  // Traduzione in streaming AI
  aiRule: {
    streamingSelector: string; // Selettore di pagina web GPT che segna l'elemento in traduzione
    messageWrapperSelector: string; // Selettore del corpo del messaggio
    streamingChange: boolean; // Aggiornamento incrementale o completo per messaggi ripetuti in pagine web simili a GPT. GPT è incrementale
  };
}
```