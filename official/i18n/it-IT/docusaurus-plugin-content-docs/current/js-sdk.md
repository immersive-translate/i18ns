---
sidebar_position: 5
---

# JS SDK

Il JS SDK di Immersive Translate ti aiuta a implementare la traduzione bilingue sul tuo sito web.

## Come utilizzare

> Prima di eseguire il debug del JS SDK, disattiva l'estensione Immersive Translate

1. Imposta i parametri di inizializzazione (nota che se immersiveTranslateConfig non è impostato, l'inizializzazione del JS SDK fallirà, puoi impostare un oggetto vuoto)

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. Aggiungi il seguente codice `script` prima del `</head>` della tua pagina web

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
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

## Parametri

- `pageRule`
  Può essere configurato per personalizzare il sito web, decidere quali contenuti devono essere tradotti o regolare lo stile della pagina.
- `isAutoTranslate`
  Traduzione automatica immediata

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

Utilizzando `selectors` si sovrascrive l'ambito della traduzione intelligente, traducendo solo gli elementi corrispondenti al selettore.

Utilizzando `excludeSelectors` è possibile escludere elementi, non traducendo quella posizione.

Utilizzando `selectors.add` si aggiungeranno alcuni selettori alla base predefinita.

Utilizzando `selectors.remove` si ridurranno alcuni selettori dalla base predefinita.

Se desideri tradurre un'area considerandola come un blocco unico, senza suddividerla in righe, puoi utilizzare il selettore `atomicBlockSelectors`. È importante notare che, prima di utilizzare `atomicBlockSelectors`, è necessario selezionare con `selectors`.

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
  selectorMatches?: string | string[]; // Usa selettori per corrispondere, senza specificare tutti gli URL.
  excludeSelectorMatches?: string | string[]; // Regole di esclusione, come sopra.

// Specificare l'ambito della traduzione
  selectors?: string | string[]; // Tradurre solo gli elementi corrispondenti
  excludeSelectors?: string | string[]; // Escludere elementi, non tradurre gli elementi corrispondenti
  excludeTags?: string | string[]; // Escludere i Tag, non tradurre i Tag corrispondenti

  // Aggiungere l'ambito della traduzione, invece di sovrascrivere
  additionalSelectors?: string | string[]; // Aggiungere l'ambito della traduzione. Nelle aree di traduzione intelligente, aggiungere la posizione della traduzione.
  additionalExcludeSelectors?: string | string[]; // Aggiungere elementi da escludere, in modo che la traduzione intelligente non traduca posizioni specifiche.
  additionalExcludeTags?: string | string[]; // Aggiungere Tag da escludere

  // Mantenere invariato
  stayOriginalSelectors?: string | string[]; // Gli elementi corrispondenti rimarranno invariati. Utilizzato spesso per i tag dei siti di forum.
  stayOriginalTags?: string | string[]; // I Tag corrispondenti rimarranno invariati, ad esempio `code`

  // Traduzione di area
  atomicBlockSelectors?: string | string[]; // Selettori di area, gli elementi corrispondenti saranno considerati come un insieme e non verranno tradotti in segmenti
  atomicBlockTags?: string | string[]; // Selettori di Tag di area, come sopra

  // Block o Inline
  extraBlockSelectors?: string | string[]; // Selettori aggiuntivi, gli elementi corrispondenti saranno considerati come elementi block, occupando una riga.
  extraInlineSelectors?: string | string[]; // Selettori aggiuntivi, gli elementi corrispondenti saranno considerati come elementi inline.

  inlineTags?: string | string[]; // I Tag corrispondenti saranno considerati come elementi inline
  preWhitespaceDetectedTags?: string | string[]; // I Tag corrispondenti andranno automaticamente a capo

  // Stile della traduzione
  translationClasses?: string | string | string[]; // Aggiungere Classi extra alla traduzione

  // Stile globale
  globalStyles?: Record<string, string>; // Modificare lo stile della pagina, utile se la traduzione causa disallineamenti nella pagina.
  globalAttributes?: Record<string, Record<string, string>>; // Modificare gli attributi degli elementi della pagina

  // Stile incorporato
  injectedCss?: string | string[]; // Incorporare stili CSS
  additionalInjectedCss?: string | string[]; // Aggiungere stili CSS, invece di sovrascrivere direttamente.

  // Contesto
  wrapperPrefix?: string; // Prefisso dell'area di traduzione, predefinito è smart, decidere se andare a capo in base al numero di caratteri.
  wrapperSuffix?: string; // Suffisso dell'area di traduzione

  // Numero di caratteri per andare a capo nella traduzione
  blockMinTextCount?: number; // Numero minimo di caratteri per considerare la traduzione come block, altrimenti sarà un elemento inline.
  blockMinWordCount?: number; // Come sopra. Se si desidera che vadano sempre a capo, si può impostare entrambi a 0.

  // Numero minimo di caratteri per la traduzione del contenuto
  containerMinTextCount?: number; // Durante il riconoscimento intelligente, il numero minimo di caratteri che un elemento deve contenere per essere tradotto, predefinito è 18
  paragraphMinTextCount?: number; // Numero minimo di caratteri per il paragrafo originale, il contenuto superiore a questo numero verrà tradotto
  paragraphMinWordCount?: number; // Numero minimo di parole per il paragrafo originale

  // Numero massimo di caratteri per forzare l'andata a capo nei paragrafi lunghi
  lineBreakMaxTextCount?: number; // Quando si traduce un paragrafo lungo, il numero massimo di caratteri per forzare l'andata a capo.

```markdown
  // Avvio della traduzione
  urlChangeDelay?: number; // Dopo l'ingresso nella pagina, quanti millisecondi ritardare l'inizio della traduzione. Attualmente impostato a 250ms per attendere l'inizializzazione della pagina

  // Traduzione AI streaming
  aiRule: {
    streamingSelector: string; // Selettore per contrassegnare l'elemento in traduzione nella pagina gpt
    messageWrapperSelector: string; // Selettore del corpo del messaggio
    streamingChange: boolean; // Le ripetute modifiche dei messaggi nella pagina gpt sono aggiornamenti incrementali o completi. gpt è incrementale
  };
}
```