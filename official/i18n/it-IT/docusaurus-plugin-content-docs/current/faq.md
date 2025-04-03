---
sidebar_position: 9
---

# FAQ

### 1. Android App, floating ball disappeared

Le vecchie versioni degli add-on sono disabilitate, disinstalla e installa l'ultima versione dal [sito ufficiale](https://immersivetranslate.com/).

## Il contenuto principale su siti come Youtube, Facebook è tradotto, ma alcune barre laterali no, voglio tradurre tutto

Per la leggibilità della pagina, la traduzione immersiva di default traduce solo l'area del contenuto principale. Se vuoi tradurre tutto.

Apri il pannello della sfera fluttuante (pressione prolungata su mobile) -> Clicca su altro in basso a destra -> Seleziona tutte le aree

## Bolla fluttuante non visualizzata nelle app di Youtube (o altre) su mobile

I plugin del browser possono funzionare solo nei browser e non possono essere utilizzati in altre app.

- Cliccando su YouTube in un browser iOS si apre direttamente l'app.

  Premi e tieni premuto il link di YouTube per far apparire una finestra fluttuante e scegli di aprirlo in una pagina web.

## Come disattivare la traduzione automatica

- Annulla nel pannello popup o nella pagina delle impostazioni.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="disattiva traduzione automatica" width="250" />

<!-- - Oppure cambia: tramite la pagina delle impostazioni

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## Nessuna autorizzazione per tradurre la pagina corrente

- Pagina predefinita del browser (nessun indirizzo nella barra degli indirizzi)
- Pagina del plugin di terze parti
- Plugin di Google disabilita la pagina del Google Store

## Come non mostrare il testo originale?

Tocca l'icona di Immersive Translate per aprire il pannello di espansione, tocca [Altro], [Passa alla modalità solo traduzione]

## Punto esclamativo appare sulla pagina

Un punto esclamativo sulla pagina indica che il servizio di traduzione ha riscontrato un problema e ha restituito un errore, puoi spostare il mouse sul punto esclamativo per visualizzare l'errore specifico.

### Errore 429

Questo è uno degli errori più comuni, 429 indica che la frequenza delle richieste è troppo veloce. La traduzione delle pagine web ha un numero molto elevato di paragrafi da tradurre, sebbene abbiamo fatto una grande ottimizzazione, inclusa la fusione dei paragrafi, il controllo della frequenza, ecc., a volte ci sono ancora alcuni servizi di traduzione sovraccarichi, restituendo l'errore di limite di frequenza 429, in questo caso puoi solitamente passare temporaneamente ad altri servizi di traduzione, o aspettare un po' e riprovare.

Se stai utilizzando un servizio Google e riscontri un errore 429, generalmente è un caso di Google che applica un limite di traffico al tuo nodo, ed è consigliato cambiare nodo.

## Traduzione di documenti locali

Se hai bisogno di tradurre file HTML locali, file txt o file PDF, puoi cliccare sull'icona dell'estensione Immersive Translate, poi cliccare su [Altro], cliccare su [Traduci file PDF] o [Traduci file HTML/txt] per tradurre i file locali.

Se stai utilizzando browser simili a Chrome, come (Chrome, Arc, Edge browser), c'è un altro modo, è aprire la pagina di gestione delle estensioni del browser `chrome://extensions`, trovare il plugin [Immersive Translate], [Consenti all'estensione di accedere ai file locali], e poi direttamente nel browser aprire il file HTML locale o il file PDF locale, puoi direttamente fare clic con il tasto destro [traduzione].

**Nota**: Il browser Safari ha restrizioni severe sull'accesso delle estensioni ai file locali. Gli utenti di Safari dovrebbero utilizzare direttamente il Metodo 1 - cliccare sull'icona dell'estensione Immersive Translate, poi cliccare su [Altro], cliccare su [Traduci file PDF] o [Traduci file HTML/txt] per tradurre i file locali.

## Come aggiornare l'estensione?

Generalmente parlando, le estensioni installate nel negozio del browser verranno aggiornate automaticamente dal browser, la situazione generale sarà aggiornata automaticamente entro un giorno dall'aggiornamento dell'estensione, se vuoi aggiornare immediatamente all'ultima versione, puoi nella pagina [Gestione Estensioni] del browser, aprire la [Modalità Sviluppatore], e poi cliccare in alto su [Aggiornamenti], puoi aggiornare immediatamente all'ultima versione del negozio.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Impostazione dello stile dei sottotitoli di Youtube

Puoi cliccare sulle impostazioni dei sottotitoli di Youtube, [Opzioni], e poi puoi regolare la dimensione, il colore, e così via.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Browser supportati da Immersive Translate Tampermonkey

Estensioni Grease Monkey raccomandate per Chrome, Firefox su desktop:

- [Tamper Monkey](https://www.tampermonkey.net/)

Estensione Grease Monkey raccomandata per Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Se usi [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) in Safari, cerca lo Script di Ottimizzazione di Immersive Translate per scaricarlo direttamente dal negozio di Stay (ottimizzato specificamente per Stay) -->

Estensioni Grease Monkey raccomandate per Android:

1. Puoi installare l'estensione [Tamper Monkey](https://www.tampermonkey.net/) utilizzando [Firefox Ultima Versione](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. Puoi anche utilizzare direttamente [X Browser](https://www.xbext.com/?ref=immersive-translate), dopo l'installazione, apri direttamente [Indirizzo Tampermonkey di Immersive Translate](https://download.immersivetranslate.com/immersive-translate.user.js) per installarlo! -->

<!-- Estensioni Grease Monkey non supportate conosciute：

- Android Via Browser
- iOS Alook Browser -->

(poiché tali browser non implementano l'API Grease Monkey richiesta)

## Problema di interfaccia di Google Translate bloccata

Aggiungi il nome di dominio `translate.googleapis.com` alla regola del proxy

## Come aggiornare le ultime regole

L'estensione stessa si sincronizzerà regolarmente con le ultime regole di adattamento del sito ufficiale quando la usi, puoi anche sincronizzarti manualmente con le ultime regole cliccando sull'icona dell'estensione Immersive Translate del browser per aprire una finestra pop-up dove l'estensione rileverà automaticamente le ultime regole di adattamento e si sincronizzerà con esse, lo stesso vale per Tampermonkeys.

## Come salvare il feedback della mia pagina web se ho problemi con la traduzione della pagina web?

Devi fare clic con il tasto destro su "Salva come" o la scorciatoia ctrl+s nella pagina web, scegliere file singolo per l'opzione di salvataggio, e infine il formato del file è .mht/.mhtml. Poi invia il file a support@immersivetranslate.com

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Errore di traduzione di Color Cloud

Tocca via? Viene visualizzato il messaggio di errore per il numero "trans_type non supportato". Puoi selezionare la lingua da rilevare automaticamente tramite la lingua specificata.

## WeChat Reading non può essere tradotto

Non può essere tradotto perché WeChat Reading ha fatto un'elaborazione speciale per il contenuto per prevenire l'accesso al contenuto tramite mezzi di terze parti.

## Attivare la traduzione non ha effetto

Altri siti traducono, ma un sito no.

- Se questo sito ha meno visitatori
  - Suggeriti paragrafi da tradurre passando il mouse
  - Se hai bisogno di tradurre l'intero sito puoi adattarlo tramite [regole utente](/docs/advanced/#user-rules)
- Se questo sito è utilizzato da molte persone
  - Puoi iniziare passando il mouse per tradurre l'uso
  - Chiamalo nel gruppo e verrà adattato in seguito

## Il miglioramento della casella di input non ha effetto

- Home del browser Ricerca Google

La casella di ricerca di Google deve essere nell'URL della pagina web di [Google](https://www.google.com/), e non può essere utilizzata nella home del browser, nei luoghi vuoti della barra degli indirizzi

## Feedback log di debug

- Abilita il log di debug
  Apri Pannello -> Impostazioni -> Impostazioni Sviluppatore -> Abilita "Stampa log di debug nella console".
- Apri la console del sito
  Fai clic con il tasto destro per aprire la revisione -> Passa alla console in alto nella colonna di destra -> Esegui l'azione per vedere i log

## Come disattivare la sfera fluttuante

- Nascondi nella pagina corrente

Impostalo su "Non tradurre mai questo sito".

- Nascondi su tutte le pagine

Apri [Pagina Impostazioni] - [Impostazioni Interfaccia] e disattiva [Mostra Sfera Fluttuante sulla Pagina].

## Errore installazione plugin su chrome

- valore non valido per web_accessible_resource[0]

  È richiesta una versione di Chromium maggiore di 88 per supportare manifest_version 3.

## Come installare il Browser 360

Supporta solo 360 Extreme Browser x, ricorda che è con x. Se hai accesso al negozio di estensioni di Google, puoi andare direttamente lì e installarlo. Se non puoi accedervi [installalo manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## Il browser Opera non funziona

- Non funziona su google.com e altre pagine di ricerca, il plugin visualizza `Si prega di aggiornare la pagina corrente prima di iniziare la traduzione` e aggiornando la pagina viene ancora visualizzato questo messaggio.

Devi trovare "Immersive Translate" nelle impostazioni del plugin di Opera e attivare l'opzione "Consenti accesso ai risultati delle pagine di ricerca".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## Sottotitoli bilingue di YouTube in cinese tradizionale non visualizzati

YouTube viene fornito con sottotitoli tradotti automaticamente, e il cinese tradizionale avrà errori di formattazione, causando la visualizzazione di tutti i sottotitoli con una grande sezione di sottotitoli all'inizio, in base a questo scenario è consigliato attivare l'opzione [Usa Immersive Translate per Tradurre i Sottotitoli] in [Impostazioni] [Sottotitoli Video].

## Altre domande (vedi molto)

<details>
<summary>Come posso cancellare la mia cache con Tampermonkeys?</summary>
<p>
A causa della limitazione dell'API di Tampermonkeys, la cache di Immersive Translate Tampermonkeys verrà salvata nella cache del sito web corrispondente, quindi se vuoi cancellarla, puoi aprire il pannello degli strumenti per sviluppatori del sito web corrispondente nel tuo browser e poi cancellare la cache di quel sito web.
</p>
</details>

<details>
<summary>Richiesta di indirizzo dell'interfaccia personalizzata di Tampermonkey fallita?</summary>
<p>
Tampermonkey richiede che tutte le richieste dallo script dichiarino i permessi all'inizio dello script, ad esempio: `@connect api.google.com`, quindi se hai bisogno di aggiungere un nuovo nome di dominio che non è quello predefinito, dichiaralo all'inizio del Tampermonkey modellato sull'altro nome di dominio.
</p>
</details>