---
sidebar_position: 9
---

# FAQ

## Impossibile scaricare dall'Apple Store

- 2023.07.28: Apple Store declassato in Cina secondo la politica
- 2023.08.05: è stato rilanciato in Cina

## Come disattivare la traduzione automatica

- Annulla nel pannello Popup o nella pagina delle Impostazioni.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="disattivare la traduzione automatica" width="250" />



## Nessun permesso per tradurre la pagina corrente

- Pagina predefinita del browser (nessun indirizzo nella barra degli indirizzi)
- Pagina del plugin di terze parti
- Il plugin di Google disabilita la pagina del Google Store

## Come faccio a non mostrare il testo originale?

Tocca l'icona di Immersive Translate per aprire il pannello di espansione, tocca [Altro], [Passa alla modalità Solo Traduzione]

## Un punto esclamativo appare sulla pagina

Un punto esclamativo sulla pagina indica che il servizio di traduzione ha incontrato un problema e ha restituito un errore, puoi muovere il mouse sul punto esclamativo per visualizzare l'errore specifico.


### Errore 429

Questo è uno degli errori più comuni, il 429 indica che la frequenza delle richieste è troppo veloce. La traduzione delle pagine web ha un numero molto elevato di paragrafi da tradurre, anche se abbiamo fatto grandi ottimizzazioni, inclusa l'unione dei paragrafi, il controllo della frequenza, ecc., ma a volte alcuni servizi di traduzione sono sovraccarichi, restituendo l'errore di limite di frequenza 429, in questo caso di solito si può temporaneamente passare ad altri servizi di traduzione, o attendere un po' e riprovare.

Se sei un servizio Google che sperimenta il 429, generalmente è un caso di Google che impone un limite di traffico al tuo nodo, ed è consigliato cambiare nodo.

## Traduzione di documenti locali

Se hai bisogno di tradurre file HTML locali, file txt o file PDF, puoi fare clic sull'icona dell'estensione Immersive Translate, quindi cliccare su [Altro], cliccare su [Traduci file PDF] o [Traduci file HTML/txt] per tradurre file locali.

Se stai utilizzando browser simili a Chrome, come (Chrome, Arc, browser Edge), c'è un altro modo, è aprire la pagina di gestione delle estensioni del browser `chrome://extensions`, trovare il plug-in [Immersive Translate], [Consentire all'estensione di accedere ai file locali], e poi direttamente nel browser aprire il file HTML locale o il file PDF locale, puoi direttamente fare clic con il tasto destro [traduzione].

## Come faccio ad aggiornare l'estensione?

Generalmente parlando, le estensioni installate dallo store del browser verranno aggiornate automaticamente, la situazione generale sarà aggiornata automaticamente entro un giorno dall'aggiornamento dell'estensione, se vuoi aggiornare immediatamente alla versione più recente, puoi nella pagina [Gestione Estensioni] del browser, aprire la [Modalità Sviluppatore], e poi cliccare in alto su [Aggiornamenti], puoi immediatamente aggiornare alla versione più recente dello store.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Impostazioni dei sottotitoli su Youtube

Puoi cliccare sulle impostazioni dei sottotitoli di Youtube, [Opzioni], e poi puoi regolare la dimensione, il colore, e così via.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Browser supportati da Immersive Translate Tampermonkey

Estensioni Grease Monkey consigliate per Chrome, Firefox su desktop:

- [Tamper Monkey](https://www.tampermonkey.net/)

Estensione Grease Monkey consigliata per Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)



Estensioni Grease Monkey consigliate per Android:

1. Puoi installare l'estensione [Tamper Monkey](https://www.tampermonkey.net/) usando [Firefox Ultima Versione](https://www.mozilla.org/firefox/browsers/mobile/android/).


(poiché tali browser non implementano l'API Grease Monkey richiesta)

## Problema di accesso all'interfaccia di Google Translate

Si prega di aggiungere il nome di dominio `translate.googleapis.com` alla regola del proxy

## Come aggiornare le ultime regole

L'estensione si sincronizzerà regolarmente con le ultime regole di adattamento del sito ufficiale quando la utilizzi, puoi anche sincronizzare manualmente con le ultime regole cliccando sull'icona dell'Estensione di Traduzione Immersiva del browser per aprire una finestra pop-up dove l'estensione rileverà automaticamente le ultime regole di adattamento e si sincronizzerà con esse, lo stesso vale per Tampermonkey.

## Come posso salvare il feedback della mia pagina web se ho problemi con la traduzione della pagina?

Devi fare clic destro su "Salva con nome" o usare la scorciatoia ctrl+s nella pagina web, scegliere l'opzione di salvataggio file singolo, e infine il formato del file è .mht/.mhtml. Poi invia il file a support@immersivetranslate.com

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Errore nella Traduzione di Color Cloud

Toccare per allontanarsi? Viene visualizzato il messaggio di errore "Unsupported trans_type". Puoi selezionare la lingua da rilevare automaticamente mediante la lingua specificata.

## La Lettura su WeChat Non Può Essere Tradotta

Non può essere tradotta perché la Lettura su WeChat ha effettuato una elaborazione speciale dei contenuti per impedire l'accesso ai contenuti tramite mezzi di terze parti.

## La traduzione non si attiva

Altri siti si traducono, ma uno no.

- Se questo sito ha meno visitatori
  - Si suggerisce di tradurre i paragrafi passando il mouse sopra
  - Se hai bisogno di tradurre l'intero sito puoi adattarlo tramite [regole utente](/docs/advanced/#user-rules)
- Se questo sito è usato da molte persone
  - Puoi iniziare passando il mouse sopra per tradurre l'uso
  - Chiamalo nel gruppo e verrà adattato in seguito

## Il miglioramento della casella di input non ha effetto

- Ricerca Google dalla Home del Browser

La casella di ricerca Google deve trovarsi nell'URL della pagina web di [Google](https://www.google.com/) e non può essere utilizzata nella home page del browser, negli spazi vuoti della barra degli indirizzi

## Registro di debug del feedback

- Attiva il registro di debug
  Apri il Pannello -> Impostazioni -> Impostazioni Sviluppatore -> Attiva "Stampa il registro di debug nella console".
- Apri la console del sito
  Clicca con il tasto destro per aprire la revisione -> Passa alla console nella parte superiore della colonna di destra -> Esegui l'azione per vedere i log

## Come disattivare l'hoverball

- Nascondi sulla pagina corrente

Impostalo su "Non tradurre mai questo sito".

- Nascondi su tutte le pagine

Apri [Pagina delle Impostazioni] - [Impostazioni Interfaccia] e disattiva [Mostra Hoverball sulla Pagina].

## Errore nell'installazione del plugin su chrome

- valore non valido per web_accessible_resource[0]

  È richiesta una versione di Chromium maggiore di 88 per supportare manifest_version 3.

## Come installare il Browser 360

È supportato solo il Browser 360 Extreme x, ricordalo è con la x. Se hai accesso al negozio delle Estensioni Google, puoi andare direttamente lì e installarlo. Se non puoi accedervi [installalo manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## Il browser Opera non funziona

- Non funziona su google.com e altre pagine di ricerca, il plugin mostra `Si prega di aggiornare la pagina corrente prima di iniziare la traduzione` e l'aggiornamento della pagina sollecita ancora questo messaggio.

Devi trovare "Immersive Translate" nelle impostazioni dei plugin di Opera e attivare l'opzione "Consenti l'accesso ai risultati delle pagine di ricerca".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## Sottotitoli bilingui in cinese tradizionale su YouTube non visualizzati

YouTube offre sottotitoli tradotti automaticamente, e il cinese tradizionale presenterà errori di formattazione, causando la comparsa di tutti i sottotitoli con una grande sezione di sottotitoli all'inizio, basandosi su questo scenario si consiglia di attivare l'opzione [Usa Immersive Translate per Tradurre i Sottotitoli] in [Impostazioni] [Sottotitoli Video].

## Altre domande (vedere molto)

<details>
<summary>Come faccio a cancellare la mia cache con Tampermonkey?</summary>
<p>
A causa della limitazione dell'API di Tampermonkey, la cache di Immersive Translate Tampermonkey verrà salvata nella cache del sito web corrispondente, quindi, se vuoi cancellarla, puoi aprire il pannello degli strumenti per sviluppatori del sito web corrispondente nel tuo browser e poi cancellare la cache di quel sito web.
</p>
</details>

<details>
<summary>La richiesta dell'indirizzo dell'interfaccia personalizzata di Tampermonkey è fallita?</summary>
<p>
Tampermonkey richiede che tutte le richieste dello script debbano dichiarare i permessi all'inizio dello script, ad esempio: `@connect api.google.com`, quindi, se hai bisogno di aggiungere un nuovo nome di dominio che non è quello predefinito, per favore dichiaralo all'inizio del modello Tampermonkey dopo l'altro nome di dominio.
</p>
</details>