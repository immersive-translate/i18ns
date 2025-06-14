---
sidebar_position: 9
---

# FAQ

## Security Related

### 1. Android App, floating ball disappeared

Le vecchie versioni degli add-on sono disabilitate, disinstalla e installa l'ultima versione dal [sito ufficiale](https://immersivetranslate.com/).

## Installation Related

### 1. How to update the extension

In generale, le estensioni installate nel browser store verranno aggiornate automaticamente, di solito entro un giorno dall'aggiornamento dell'estensione. Se desideri aggiornare immediatamente all'ultima versione, puoi andare alla pagina [Gestione Estensioni] del browser, abilitare la [Modalità Sviluppatore] e quindi cliccare su [Aggiorna] in alto per aggiornare immediatamente all'ultima versione disponibile nello store.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

### 2. Immersive Translate Tampermonkey Supported Browsers

iOS:

- [Tamper Monkey Browser](https://www.tampermonkey.net/)
- Browser Safari con estensione Tampermonkey installata, estensioni compatibili:
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171): Si consiglia di cercare direttamente lo Script di Ottimizzazione Immersive Translate dallo store di Stay (ottimizzato appositamente per Stay).

Android:

- [Firefox Latest Version](https://www.firefox.com.cn/download/#product-android-release): Dopo l'installazione, installa l'estensione [Tamper Monkey](https://www.tampermonkey.net/).
- [X Browser](https://www.xbext.com/?ref=immersive-translate): Dopo l'installazione, apri direttamente l'[indirizzo dello script Tampermonkey di Immersive Translate](https://download.immersivetranslate.com/immersive-translate.user.js) per installarlo.

Browser noti che non supportano le estensioni Tampermonkey (questi browser non hanno implementato l'API Tampermonkey richiesta):

- Android Via Browser
- iOS Alook Browser

### 3. Error installing plugin installer on chrome

Errore `invalid value for web_accessible_resource[0]`: È richiesta una versione di Chromium superiore alla 88 per supportare manifest_version 3.

### 4. How to install 360 Browser

È supportato solo il 360 Extreme Browser X, ricorda che è con X. Se puoi accedere al Google Extensions store, puoi andare direttamente lì per installarlo. Se non puoi accedervi, [installalo manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features).

### 5. Opera browser does not work

Non funziona su google.com e altre pagine di ricerca, il plugin visualizza `Please refresh the current page before starting the translation` e aggiornando la pagina mostra ancora questo messaggio: Devi trovare "Immersive Translate" nelle impostazioni del plugin di Opera e abilitare l'opzione "Allow access to search page results".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

### 6. Cannot enable extensions on iOS devices

Se non puoi abilitare le estensioni sul tuo dispositivo iOS, segui questi passaggi:

1. Apri l'app [Impostazioni]
2. Scorri verso il basso e tocca [Tempo di utilizzo]
3. Seleziona [Restrizioni contenuti e privacy]
4. Tocca [Restrizioni contenuti]
5. Seleziona [Contenuti web] e impostalo su [Senza restrizioni]

Se non hai bisogno delle altre funzionalità di Restrizioni contenuti e privacy, puoi anche scegliere di disattivare semplicemente le Restrizioni contenuti e privacy:

1. Apri l'app [Impostazioni]
2. Seleziona [Tempo di utilizzo]
3. Disabilita [Restrizioni contenuti e privacy]

### 7. Safari settings page keeps loading

Impostazioni di sistema -> Browser Safari -> Avanzate -> Dati del sito web -> Modifica, trova immersivetranslate.com ed eliminalo.

### 8. After installing iOS18, redirected to blank page when logging in from settings page

Premi a lungo il palloncino fluttuante e clicca sull'avatar per accedere.

### 9. "File does not exist" when dragging crx file to browser extensions

Devi prima estrarre il file zip, quindi trascinare solo il file CRX.

### 10. Why is the crx download installing version 1.13.5 instead of the latest

Perché il tuo motore Chrome è rilevato come inferiore alla versione 115, che non supporta alcune funzionalità avanzate del plugin, quindi viene automaticamente declassato alla versione 1.13.5.

## Basic Translation Related

### 1. Main content on websites like Youtube, Facebook is translated, but some sidebars are not, I want to translate everything

Per la leggibilità della pagina, la traduzione immersiva per impostazione predefinita traduce solo l'area del contenuto principale. Se desideri tradurre tutte le aree:

Apri il pannello del palloncino fluttuante (premi a lungo su mobile) -> Clicca su altro in basso a destra -> Seleziona tutte le aree.

### 2. Floating Bubble Not Displayed in Apps on Mobile

- Il plugin Immersive Translate è un plugin del browser che può **funzionare solo nei browser**, non può essere utilizzato in altre app e non supporta la traduzione all'interno di altre app.

- Il plugin funziona solo nel browser in cui è installato e **non può funzionare tra browser diversi** (ad esempio, installarlo in Safari non ti permette di usarlo in Chrome)

### 3. Clicking on YouTube in iOS browser directly opens the App

Premi e tieni premuto il link di YouTube per far apparire una finestra fluttuante e scegli di aprirlo in una pagina web.

### 4. How to turn off automatic translation

- Annulla nel pannello Popup o nella pagina delle Impostazioni.
- Oppure cambia tramite la pagina delle impostazioni

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="turn off automatic translation" width="250" />

### 5. No permission to translate the current page

- Pagina predefinita del browser (nessun indirizzo nella barra degli indirizzi)
- Pagina del plugin di terze parti
- Google plugin disabilita la pagina dello store di Google

### 6. How do I not show the original text?

Tocca l'icona di Immersive Translate per aprire il pannello di espansione, tocca [Altro], [Passa alla modalità Solo Traduzione].

### 7. Exclamation mark appears on the page

Un punto esclamativo sulla pagina indica che il servizio di traduzione ha riscontrato un problema e ha restituito un errore. Puoi spostare il mouse sul punto esclamativo per visualizzare l'errore specifico.

#### Example: 429 Error

Questo è uno degli errori più comuni, 429 indica che la frequenza delle richieste è troppo veloce. La traduzione delle pagine web ha un numero molto elevato di paragrafi da tradurre, sebbene abbiamo fatto una grande ottimizzazione, inclusa la fusione dei paragrafi, il controllo della frequenza, ecc., a volte ci sono ancora alcuni servizi di traduzione sovraccarichi, che restituiscono un errore di limite di frequenza 429. In questo caso, puoi solitamente passare temporaneamente ad altri servizi di traduzione o attendere un po' e riprovare.

Se stai usando il servizio Google e riscontri un errore 429, generalmente è un caso di Google che applica un limite di traffico contro il tuo nodo, ed è consigliato cambiare nodo.

### 8. How to switch translation source and target language

Su mobile, premi a lungo il palloncino fluttuante; su desktop, sposta il mouse sul palloncino fluttuante per aprire le impostazioni, seleziona un altro servizio di traduzione/un'altra lingua di destinazione.

### 9. Google Translate Interface Walled Off Issue

Aggiungi il dominio `translate.googleapis.com` alla regola del proxy.

### 10. Does OpenAI's ban on API Keys in China affect member AI services

Nessun impatto, il prodotto utilizza Azure Enterprise OpenAI, che non è soggetto a restrizioni regionali delle API.

### 11. Color Cloud Translation Error

Cliccando sul messaggio di errore `?` viene visualizzato "Unsupported trans_type". Puoi selezionare manualmente di impostare la lingua rilevata automaticamente su una lingua specifica.

### 12. WeChat Reading Cannot Be Translated

Non può essere tradotto perché WeChat Reading ha effettuato un'elaborazione speciale per il contenuto per impedire l'accesso al contenuto tramite mezzi di terze parti.

### 13. Some content on web pages is not translated

Generalmente, è perché l'amministratore del sito web ha definito aree da non tradurre utilizzando `translate="no"` o `notranslate class`, ma puoi risolvere questo problema:

1. Abilitando la funzione di passaggio del mouse
2. Utilizzando il passaggio del mouse per forzare la traduzione del contenuto del paragrafo in quell'area

### 14. Trigger translation does not take effect

Quando altri siti possono essere tradotti ma un sito particolare no:

- Se questo sito ha meno visitatori
  - Si consiglia di tradurre i paragrafi passando il mouse
  - Se hai bisogno di tradurre l'intero sito, puoi adattarlo tramite [regole utente](/docs/advanced/#user-rules)
- Se questo sito è utilizzato da molte persone
  - Puoi iniziare utilizzando il passaggio del mouse per tradurre
  - Segnalalo nel gruppo, e verrà adattato successivamente

### 15. How do I save my webpage feedback if I have problems with the webpage translation?

Devi fare clic con il tasto destro su "Salva come" o utilizzare la scorciatoia Ctrl+S nella pagina web, scegliere file singolo per l'opzione di salvataggio e salvare con il formato file .mht/.mhtml. Quindi invia il file a support@immersivetranslate.com.

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

### 16. Feedback debug log

1. Abilita il logging di debug: Apri il Pannello -> Impostazioni -> Impostazioni Sviluppatore -> Abilita "Stampa log di debug nella console".
2. Apri la console del sito: Fai clic con il tasto destro per aprire l'ispezione -> Passa alla console in alto nella colonna di destra -> Esegui l'azione per vedere i log.

### 17. How to turn off hoverball

- Nascondi nella pagina corrente: Impostalo su "Non tradurre mai questo sito"
- Nascondi su tutte le pagine: Apri [Pagina delle Impostazioni] - [Impostazioni Interfaccia] e disattiva [Mostra Hoverball sulla Pagina]

### 18. Mouse hover + shortcut key translation function does not work

Per abilitare la funzione di traduzione con passaggio del mouse più tasto di scelta rapida, la pagina deve prima avere il focus. Se trovi che la funzione non si attiva, prova questi passaggi:

1. Clicca una volta in qualsiasi punto della pagina per assicurarti che la pagina abbia il focus.
2. Prova a utilizzare di nuovo il passaggio del mouse e il tasto di scelta rapida per la traduzione.
3. Se la funzione di traduzione non risponde ancora, verifica se le impostazioni del tuo tasto di scelta rapida sono corrette.

### 19. How to update the latest rules

L'estensione stessa sincronizzerà regolarmente con le ultime regole di adattamento del sito ufficiale quando la utilizzi. Puoi anche sincronizzare manualmente con le ultime regole cliccando sull'icona dell'Estensione Immersive Translate nel browser per aprire una finestra popup dove l'estensione rileverà automaticamente le ultime regole di adattamento e si sincronizzerà con esse. Lo stesso vale per gli script Tampermonkey.

### 20. Translation fails / Translation keeps spinning

1. Controlla il motivo del fallimento:
   - Se il limite di quota è stato raggiunto, significa che la quota mensile del membro per quella fonte di traduzione è esaurita
   - Se la traduzione mostra un errore di rete, controlla prima lo stato del tuo nodo/rete

2. Cambia la fonte di traduzione: premi a lungo la sfera fluttuante per selezionare un'altra fonte di traduzione

### 21. Come controllare la quota e l'utilizzo della traduzione per i membri Pro

- I membri Pro godono di una quota di traduzione base di 20 milioni di Token al mese, che può essere utilizzata per tutti i servizi di traduzione. Che si utilizzi tutto per DeepL (equivalente a 20 milioni di caratteri), tutto per OpenAI (20 milioni di Token), o una combinazione di più servizi, puoi allocare liberamente la quota in base alle tue esigenze effettive.

  > La tariffazione di OpenAI si basa sui token. Per il testo in inglese, 1 token corrisponde approssimativamente a 4 caratteri o 0,75 parole. Tipicamente, 1000 Token equivalgono a circa 750 parole in inglese o 400-500 caratteri cinesi.

- Indirizzo per la richiesta di utilizzo: [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. Perché la qualità della traduzione di Google del plugin non è buona come quella della traduzione della pagina web di Google

Perché il plugin utilizza l'API gratuita di Google, che è una vecchia API che Google non mantiene continuamente, mentre la traduzione ufficiale della pagina web di Google è mantenuta continuamente. Teoricamente, la qualità non è buona come la traduzione ufficiale di Google, e recentemente la qualità della traduzione dell'API gratuita di Google è diminuita significativamente. Si consiglia di passare ad altri servizi di traduzione e stiamo attivamente cercando soluzioni alternative. Discussione correlata: [#2574](https://github.com/immersive-translate/immersive-translate/issues/2547)

### 23. Mostrare la modalità touch quando si è in modalità mouse

In [Impostazioni Avanzate](https://dash.immersivetranslate.com/#advanced), abilita la modalità solo mouse. La versione 1.14.9 ottimizzerà questo rilevamento della modalità.

## Traduzione Video Correlata

### 1. Stile di configurazione dei sottotitoli di Youtube

Puoi cliccare sulle impostazioni dei sottotitoli di Youtube, [Opzioni], e poi puoi regolare la dimensione, il colore, e così via.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

### 2. I sottotitoli bilingue di YouTube in cinese tradizionale non vengono visualizzati

YouTube include sottotitoli tradotti automaticamente, e il cinese tradizionale avrà errori di formattazione, causando la comparsa di una grande sezione di sottotitoli all'inizio. In base a questo scenario, si consiglia di attivare l'opzione [Usa Immersive Translate per Tradurre i Sottotitoli] in [Impostazioni] [Sottotitoli Video].

### 3. Come abilitare la traduzione dei sottotitoli per Bilibili

Quando traduci i sottotitoli dei video di Bilibili, segui questi passaggi:

1. Prima, abilita i sottotitoli integrati di Bilibili cliccando sul pulsante "Sottotitoli" nell'angolo in basso a destra del lettore. Se il video non ha il pulsante dei sottotitoli o il contenuto dei sottotitoli, i sottotitoli bilingue non sono supportati.
2. Clicca sull'icona "Immersive Translate" nel lettore per abilitare la funzione dei sottotitoli bilingue.

Nota durante l'uso:

1. Assicurati che i sottotitoli integrati di Bilibili siano abilitati.
2. Assicurati che la lingua di destinazione di Immersive Translate sia diversa dalla lingua dei sottotitoli integrati di Bilibili per attivare la funzione di traduzione.

### 4. Traduzione dei sottotitoli di Netflix utilizzando lo stile originale dei sottotitoli

- L'approccio attuale di Netflix utilizza la traduzione progressiva, con uno stile di sottotitoli auto-ospitato, e non supporta i sottotitoli manuali.
- L'approccio vecchio richiede di aspettare che tutti i sottotitoli siano tradotti prima di visualizzarli, ma supporta i sottotitoli manuali.

Per tornare all'approccio vecchio, vai a [[Impostazioni Sviluppatore](https://dash.immersivetranslate.com/#developer)], trova [Modifica Regole Utente]
e aggiungi la seguente regola:

```json
[
  {
    "id": "netflix",
    "subtitleRule.add": {
      "attachRule": {
        "appendSelector": ""
      }
    }
  }
]
```

## Traduzione File Correlata

### 1. Traduzione di documenti locali

- Metodo 1: Vai al [sito web di Traduzione File Immersive Translate](https://app.immersivetranslate.com/), o clicca sull'icona dell'estensione Immersive Translate e clicca su [Traduzione File] per entrare.

- Metodo 2: Se stai usando browser simili a Chrome, come (Chrome, Arc, Edge browser), c'è un altro modo: apri la pagina di gestione delle estensioni del browser `chrome://extensions`, trova il plugin [Immersive Translate], [Consenti all'estensione di accedere ai file locali], e poi direttamente nel browser apri il file HTML locale o il file PDF locale, puoi cliccare con il tasto destro su [Traduzione].

**Nota**: Il browser Safari ha restrizioni severe sull'accesso delle estensioni ai file locali. Gli utenti di Safari dovrebbero usare direttamente il Metodo 1 - vai al [sito web di Traduzione File Immersive Translate](https://app.immersivetranslate.com/) per tradurre i file locali.

### 2. La traduzione dei PDF è lenta quando ci sono molte pagine

Si consiglia di dividere il documento in più parti di meno di 100 pagine ciascuna, tradurle separatamente e poi unirle dopo la traduzione.

### 3. Traduzioni duplicate o sovrapposte nei PDF

Questo è dovuto a problemi di riconoscimento del file sorgente. Attualmente, si consiglia di cliccare manualmente su quella sezione e cancellare le caselle di testo extra. Continueremo a ottimizzare questa situazione nei futuri aggiornamenti.

### 4. Esiste un glossario / traduzione speciale o non traduzione per determinati termini

La versione 1.16.1+ supporta la funzione [AI Terminology Library](https://dash.immersivetranslate.com/#terms).

La libreria di terminologia AI non supporta di default la terminologia della traduzione automatica di Google/Microsoft.

Metodo per forzare l'abilitazione:
(ps: la traduzione automatica utilizza la sostituzione dei segnaposto, la terminologia può ridurre la qualità della traduzione)

Vai a [[Impostazioni Sviluppatore](https://dash.immersivetranslate.com/#developer)] -> [Modifica Configurazione Utente Completa]

```
{
  ....
  "enableMachineTranslateTerms":true,
  ...
}
```

### 5. Impossibile esportare file Word tradotti in formato Word

Attualmente, ci sono alcuni problemi tecnici con l'esportazione dei file Word. Si consiglia di mantenere il formato esistente. Stiamo lavorando continuamente all'ottimizzazione.

### 6. Come regolare la dimensione minima del carattere nei PDF

Questo è dovuto alla restrizione della dimensione minima del carattere del browser. Regola il carattere del browser all'impostazione più bassa. Per Chrome, ad esempio: clicca su [Impostazioni dimensione carattere di Chrome](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)

## Traduzione Casella di Input Correlata

### 1. Il miglioramento della casella di input non ha effetto

- Browser noti per non essere supportati: Vedi la sezione di compatibilità di [Traduzione Casella di Input](https://immersivetranslate.com/docs/input/)
- Non è possibile tradurre nella barra degli URL o nella pagina iniziale del browser, supporta solo le barre di ricerca. Puoi testare su https://www.bing.com/
- Prova a premere il tasto spazio più velocemente

## Pagamento Correlato

### 1. Posso usare WeChat Pay

I pagamenti WeChat richiedono di inviare un messaggio privato ai membri del personale nel gruppo e annotare "pagamento WeChat". Dopo che il personale fornisce il codice QR per il pagamento, effettua il pagamento e fornisci i dettagli del pagamento. Il personale fornirà il codice di riscatto per l'abbonamento annuale/mensile richiesto, che può essere riscattato sulla [Pagina di Riscatto Membri](https://immersivetranslate.com/exchange/)

### 2. Posso ottenere una fattura

Attualmente, solo gli abbonamenti annuali possono ricevere fatture. Gli utenti che hanno già pagato e necessitano di una fattura devono inviare un messaggio privato ai membri del personale nel gruppo e annotare "emissione fattura". Gli utenti non pagati possono controllare: [Informazioni Fattura Abbonamento Annuale](https://immersivetranslate.com/bill/)

## Altre domande (non comuni)

<details>
<summary>Come posso cancellare la mia cache con Tampermonkeys?</summary>
<p>
A causa della limitazione dell'API di Tampermonkeys, la cache di Immersive Translate Tampermonkeys sarà salvata nella cache del sito web corrispondente, quindi se vuoi cancellarla, puoi aprire il pannello degli strumenti per sviluppatori del sito web corrispondente nel tuo browser e poi cancellare la cache di quel sito web.
</p>
</details>

<details>
<summary>Richiesta dell'indirizzo dell'interfaccia personalizzata di Tampermonkey fallita?</summary>
<p>
Tampermonkeys richiede che tutte le richieste dallo script debbano dichiarare i permessi all'inizio dello script, ad esempio: `@connect api.google.com`, quindi se hai bisogno di aggiungere un nuovo nome di dominio che non è quello predefinito, dichiaralo all'inizio del Tampermonkey modellato sull'altro nome di dominio.
</p>
</details>

<details>
<summary>Il plugin del browser Edge si apre vuoto e il browser segnala l'errore MANIFEST-000001</summary>
<p>
Apri l'applicazione [Quick File Finder (Everything)](https://www.voidtools.com/en-us/downloads/), cerca `amkbmndfnliijdhojkpoglbnaaahippg` (l'ID dell'estensione Immersive) nella cartella di archiviazione del browser, eliminala, poi disinstalla e reinstalla il plugin.
</p>
</details>

<details>
<summary>Come scaricare sottotitoli bilingue / I sottotitoli bilingue possono essere scaricati da altri siti web?</summary>
<p>
- Attualmente, il download dei sottotitoli è supportato solo su desktop.
- Inclusi YouTube, quando c'è un pulsante di download dei sottotitoli, il sito web corrente supporta il download dei sottotitoli bilingue.
</p>
</details>