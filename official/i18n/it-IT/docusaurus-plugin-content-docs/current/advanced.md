---
sidebar_position: 4
---

# Opzioni di personalizzazione avanzate

È possibile modificare configurazioni più personalizzate nella Pagina di Configurazione Estesa -> Impostazioni Sviluppatore -> Config Utente che non sono modificabili nell'interfaccia utente per gli utenti avanzati, vedere l'ultima nota per maggiori dettagli sui parametri. La `config` integrata attuale può essere trovata [qui](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

## Regole Utente

Con `Regole` è possibile personalizzare la configurazione di un particolare sito web, decidendo quali contenuti devono essere tradotti o meno, o aggiustando lo stile delle pagine, ecc.

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

Usa `matches` per corrispondere al sito web desiderato. Sono consentiti caratteri jolly, ad es. `*.google.com`,`www.google.com/test/*`,`file://*`.

Utilizzando `selectors` si sovrascrive l'ambito di traduzione intelligente, traducendo solo gli elementi corrispondenti a quel selettore.

Usa `excludeSelectors` per escludere elementi senza tradurre la posizione.

Usa la famiglia di selettori `additional` per aumentare o diminuire l'ambito di traduzione basato sulla traduzione intelligente.

```json
[
  {
    "matches": "www.google.com",
    "additionalSelectors": [],
    "additionalExcludeSelectors": []
  }
]
```

Se vuoi tradurre una regione trattando gli elementi come un unico blocco e non separandoli, puoi usare il selettore `atomicBlockSelectors`. Per esempio, i profili Instagram. Nota che l'uso di `atomicBlockSelectors` richiede di selezionare con `selectors` prima di usare `atomicBlockSelectors`.

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div. ._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Se la traduzione risulta in pagine disallineate, testo sovrapposto e altri casi limite, puoi usare `globalStyles` per regolare lo stile della pagina per correggerlo. Per esempio, l'intestazione di youtube, che viene utilizzata per rimuovere l'altezza massima della pagina originale.

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## Miglioramenti alla consolidazione delle regole utente

Supporto dalla versione 0.7.4+. Prendiamo come esempio il saltare la zona senza traduzione

```json
{
  "matches": "https://www.elektrotechnik.rwth-aachen.de/*",
  "additionalExcludeSelectors.remove": [".notranslate", "[translate=no]"]
}
```

Le operazioni di aggiunta e rimozione modificano le regole fornite di default e non necessitano di essere sostituite completamente, come avveniva in precedenza.

## CSS Iniettato

Il CSS iniettato ti permette di inserire stili web personalizzati globalmente. Può essere utilizzato con `translationClasses` delle `Rules`.

```
".immersive-translate-target-wrapper img { width: 16px; height: 16px }"
```

È anche possibile personalizzare lo stile del sito in modo più specifico, come un normale gestore di stili web. (utilizzando anche `display:none` per rimuovere le pubblicità)

```css
.title {
  color: red;
}
```

## Configurazione Utente

La configurazione ti permette di personalizzare la configurazione di questo plugin, come i servizi di traduzione, le opzioni di traduzione specifiche per lingua, ecc.

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

I campi delle regole in `rules` possono utilizzare tutti i campi in `generalRule`. Le `rules` hanno la priorità più alta, unendo il `generalRule` e le regole per quella `rule` quando una particolare `rule` per un sito specifico viene corrisposta.

Introduzione ad alcuni dei campi comuni di Config.

### Non mostrare servizi di traduzione non configurati nel pannello popup

`"showUnconfiguredTranslationServiceInPopup": false`

### Configurazione dei servizi di traduzione

Usa `translationService` per selezionare il motore di traduzione predefinito, che attualmente supporta:

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

Usa `translationServices` per configurare l'`apikey` di ciascun servizio di traduzione, diversi fornitori di servizi necessitano di parametri differenti, e le loro chiavi API possono essere richieste nel centro sviluppatori dei rispettivi siti web.

Ad esempio, per il Traduttore Tencent, è necessario configurare `secretId`, `secretKey`. Puoi recarti su Tencent Cloud per richiedere una chiave API con 5 milioni di caratteri gratuiti al mese. Consulta [qui](/docs/services/tencent) per il processo di candidatura.

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

Campo `matches`, utilizzando questo servizio di traduzione per un sito web specifico.

Il campo `limit`, che specifica il numero massimo di richieste al secondo per questo servizio di traduzione (alcuni servizi limitano il numero massimo di richieste al secondo).

Campo `maxTextGroupLengthPerRequest`, numero massimo di paragrafi per richiesta

Campo `maxTextLengthPerRequest`, numero massimo di caratteri per richiesta

`apiUrl` Ti permette di personalizzare l'indirizzo dell'interfaccia di traduzione.

### Traduci sempre siti web specifici

`translationUrlPattern` Configura i siti che sono sempre tradotti, e i siti che non sono mai tradotti.

- `matches` la configurazione traduce sempre il sito.
- `excludeMatches` Configura i siti che non sono mai tradotti.

I valori di configurazione possono essere nomi di dominio o URL con `*`, come: `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### Traduci sempre lingue specifiche

translationLanguagePattern, configura la lingua che è sempre tradotta e la lingua che non è mai tradotta.

- `matches` Configura la lingua che è sempre tradotta, ad es. `en`,
- `excludeMatches` Configura le lingue che non sono mai tradotte.

### Formato di visualizzazione della traduzione

`translationTheme` è il formato di visualizzazione della traduzione e attualmente supporta i seguenti stili:

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

Nome corrispondente in italiano:

```json
{
  "none": "nessuno",
  "dashed": "tratteggio",
  "dotted": "punteggiato",
  "underline": "sottolineatura",
  "mask": "effetto sfocatura",
  "paper": "effetto ombra carta bianca",
  "highlight": "evidenziatore",
  "blockquote": "stile citazione",
  "weakening": "indebolimento",
  "italic": "corsivo",
  "bold": "grassetto",
  "thinDashed": "sottolineatura tratteggiata sottile"
}
```

`translationThemePatterns` ti permette di configurare diversi stili di traduzione per diversi siti web.

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### Traduzione dei messaggi della pagina dello stream di Class gpt

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

### Regole

`rules` è un oggetto array che ti permette di configurare regole per siti speciali, come avere Twitter che traduce solo una certa parte di una regione:

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

Le `rules` incorporate attuali possono essere trovate [qui](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

Alcuni dei campi importanti sono selezionati di seguito per illustrazione:

```typescript
export interface Rule {
  // Corrisponde al sito web
  id?: string; // Ogni regola di adattamento ha il proprio id, se gli utenti vogliono riutilizzare questa regola in aggiunta a questo cambiamento, devono aggiungere questo id corrispondente alla propria regola per riutilizzarla
  matches?: string | string[]; // Questa regola corrisponderà solo al sito web qui. Questa regola corrisponderà solo ai siti qui.
  excludeMatches?: string | string[]; // Escludi siti specifici.
  selectorMatches?: string | string[]; // Corrisponde con un selettore senza specificare tutti gli URL
  excludeSelectorMatches?: string | string[]; // Escludi regole, come sopra.

  // Specifica l'intervallo di traduzioni
  selectors?: string | string[]; // Traduci solo gli elementi che corrispondono
  excludeSelectors?: string | string[]; // Escludi elementi, non tradurre corrispondenze
  excludeTags?: string | string[]; // Escludi Tag, non tradurre i Tag corrispondenti

  // aggiungi intervalli di traduzione invece di sovrascrivere
  additionalSelectors?: string | string[]; // aggiungi intervalli di traduzione. Aggiungi località di traduzione alle regioni tradotte intelligentemente.
  additionalExcludeSelectors?: string | string[]; // Aggiungi elementi esclusi in modo che la traduzione intelligente non traduca località specifiche.
  additionalExcludeTags?: string | string[]; // Tag esclusi aggiuntivi

  // Lascia così com'è
  stayOriginalSelectors?: string | string[]; // Gli elementi corrispondenti saranno lasciati così come sono. Comunemente usato nei tag dei siti dei forum.
  stayOriginalTags?: string | string[]; // I tag corrispondenti saranno lasciati così come sono, ad es. `code`

  // Traduzioni regionali
  atomicBlockSelectors?: string | string[]; // Selettori regionali, gli elementi corrispondenti saranno trattati come un tutto, non tradotti in sezioni.
  atomicBlockTags?: string | string[]; // Selettori di Tag di area, come sopra

  // Blocco o Inline
  extraBlockSelectors?: string | string[]; // Selettori extra, gli elementi corrispondenti saranno trattati come elementi di blocco, non tradotti in una linea unica.
  extraInlineSelectors?: string | string[]; // Selettori extra che verranno utilizzati come elementi inline.

  inlineTags?: string | string[]; // Il tag corrispondente verrà utilizzato come elemento inline
  preWhitespaceDetectedTags?: string | string[]; // Il tag corrispondente verrà automaticamente incapsulato

  // Stile di traduzione
  translationClasses?: string | string | string[]; // Aggiungi classi aggiuntive alla traduzione

  // Stili Globali
  globalStyles?: Record<string, string>; // Modifica gli stili della pagina, utile se la traduzione causa disordine nella pagina.
  globalAttributes?: Record<string, Record<string, string>>; // Modifica gli attributi degli elementi della pagina

  // Stili incorporati
  injectedCss?: string | string[]; // Incorpora stili CSS
  additionalInjectedCss?: string | string[]; // Stili CSS aggiuntivi invece di sovrascriverli.

  // Contesto
  wrapperPrefix?: string; // Il prefisso dell'area di traduzione, di default è smart, con o senza interruzioni di linea a seconda del numero di caratteri.
  wrapperSuffix?: string; // Suffisso dell'area di traduzione

  // Numero di caratteri per incapsulare la traduzione
  blockMinTextCount?: number; // Numero minimo di caratteri per incapsulare la traduzione come blocco, altrimenti la traduzione è un elemento inline.
  blockMinWordCount?: number; // Come sopra. Se vuoi che siano sempre a capo, puoi mettere 0 in entrambi.

  // Numero minimo di caratteri che possono essere tradotti dal contenuto
  containerMinTextCount?: number; // Numero minimo di caratteri che un elemento deve contenere prima che venga tradotto, di default è 18
  paragraphMinTextCount?: number; // Numero minimo di caratteri per il paragrafo, maggiore del numero di caratteri che il contenuto deve contenere. numero, qualsiasi cosa più grande di quello verrà tradotta
  paragraphMinWordCount?: number; // Numero minimo di parole nel paragrafo originale

  // Interruzioni di linea forzate per lunghi paragrafi
  lineBreakMaxTextCount?: number; // Numero massimo di caratteri nel paragrafo per essere costretti a interrompere quando si traduce un lungo paragrafo.

  // Quando iniziare la traduzione.
  urlChangeDelay?: number; // Quanti millisecondi ritardare la traduzione dopo l'ingresso nella pagina. Per attendere l'inizializzazione della pagina, di default è 250ms
  observeUrlChange?: boolean; // Rileva quando l'indirizzo url è cambiato e inizia di nuovo la traduzione, vero per default.

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Mostra il popup della pagina sui dispositivi mobili. finestra mobile, vero per default.
  fingerCountToToggleTranslagePageWhenTouching?: number; // Traduce quando quattro dita toccano, può essere impostato su 0, 2, 3, 4, 5

  // Traduzioni in streaming AI
  aiRule: {
    streamingSelector: string; // Selettore per contrassegnare l'elemento che viene tradotto nella pagina web gpt
    messageWrapperSelector: string; // Selettore del corpo del messaggio
    streamingChange: boolean; // Se il messaggio viene aggiornato incrementalmente o completamente per l'iterazione della pagina web gpt. gpt è incrementale
  };
}
```

**Maggiori spiegazioni**

Differenza tra blocco e inline, se vuoi saperne di più puoi vedere [qui](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline)

- L'elemento di blocco occupa una singola linea, e più elementi di blocco adiacenti occupano ciascuno una nuova linea.
- L'elemento inline non occupa una singola linea; più elementi inline adiacenti sono disposti sulla stessa linea, e una nuova linea non viene creata fino a quando una linea è troppo piena.
