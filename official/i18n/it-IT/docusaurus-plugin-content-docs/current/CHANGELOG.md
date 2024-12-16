---
sidebar_position: 6
---

# Registro delle modifiche

## 1.12.3 (2024-12-13)


- Aggiunto: **Traduzione Contestuale AI** può migliorare l'accuratezza della traduzione di contenuti professionali. (Disponibile solo per membri Pro) **Opzioni** -> **Generale** -> **Abilita Traduzione Contestuale AI**
- Corretto: Alcuni bug nell'effetto di traduzione multilinea su Twitter.
- Corretto: Problemi con la traduzione di alcune formule a causa del testo ricco
- Migliorato: Durante la traduzione su **x.com**, i video con sottotitoli avranno automaticamente i sottotitoli bilingue tradotti.
- Migliorato: I video senza sottotitoli mostreranno un'icona di traduzione e forniranno un motivo per cui la traduzione non è possibile.

## 1.11.7 (2024-11-25)

- Aggiunto: Bing/Google ora supporta il Khmer (Cambogiano).
- Aggiunto: Permette ai file ePub incompleti di continuare la traduzione da dove si erano interrotti al reimporto.
- Corretto: Problema con la traduzione delle immagini di Twitter nel browser Safari.
- Corretto: Tasti di scelta rapida che diventano inefficaci quando si attiva o disattiva la funzione "**Traduzione al passaggio del mouse**".
- Migliorato: Visualizzazione migliorata della traduzione bilingue multilinea su Twitter e Youtube.
- Migliorato: La traduzione del testo ricco è disattivata per impostazione predefinita in modalità bilingue per migliorare la qualità della traduzione.
- ~~Migliorato: Aggiunta l'opzione per personalizzare "**Abilita Traduzione Barra Laterale & Navigazione**" nelle "**Impostazioni Avanzate**".~~
- Migliorato: Le immagini non vengono più tradotte in modalità "**Passaggio del mouse - traduci immediatamente questo paragrafo**".

## 1.11.4 (2024-11-16)

- Corretto: Problema con la traduzione delle formule causato dal "Miglioramento della traduzione di Twitter" nella versione 1.11.2.

## 1.11.2 (2024-11-13)

- Corretto: Problema in cui il contenuto scompare dopo aver cliccato su "vedi altro" nella modalità solo traduzione di Facebook.
- ~~Migliorato: Visualizzazione migliorata delle traduzioni bilingue multilinea su Twitter.~~
- Migliorato: Aggiornata l'interfaccia utente dell'elenco a discesa del servizio di traduzione nel pannello.

## 1.11.1 (2024-11-05)

- Aggiunto: La **Traduzione dei Sottotitoli** delle riunioni in tempo reale ora supporta l'attivazione tramite "palla fluttuante", disponibile su Zoom, Google Meet e Microsoft Teams.
- Corretto: Problemi di sincronizzazione dei sottotitoli su YouTube dopo la visualizzazione degli annunci.
- Corretto: Problemi di visualizzazione con il menu di traduzione del tasto destro in Safari su MacOS 15.
- Corretto: Problemi con la funzionalità Ctrl+Z per annullare nell'**Input Migliorato** su alcuni siti web.

## 1.10.6 (2024-10-25)

- Corretto: Problema con i tasti di scelta rapida dell'**Input Migliorato** che non si attivavano
- Migliorato: Riduzione della dimensione del pacchetto di installazione
- Migliorato: Soluzione per la visualizzazione dei sottotitoli Netflix

## 1.10.5 (2024-10-23)

- Aggiunto: Visualizzazione di un avviso quando la lingua di origine e la lingua di destinazione sono le stesse
- Corretto: Problema di traduzione dei caratteri spazio nel testo ricco [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- Migliorato: Miglioramento dell'input e funzionalità del passaggio del mouse all'interno degli iframe incorporati nelle pagine web

## 1.10.2 (2024-10-11)

- Aggiunto: Traduzione delle immagini (versione Beta)
- Aggiunto: Modalità Forza Abilitazione Supporto Mouse (Abilita questa funzione solo se la funzione di passaggio del mouse non è disponibile sui dispositivi tablet) **Impostazioni** -> **Impostazioni Avanzate** -> **Forza Abilitazione Supporto Mouse**
- Aggiunto: Visualizzazione del messaggio di errore quando la traduzione dei sottotitoli video fallisce
- Corretto: Problema di traduzione del testo ricco [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163)
- Migliorato: Risolti i problemi in cui il pulsante di traduzione potrebbe non funzionare durante la traduzione PDF
- Migliorato: Migliorato il rendering delle formule tradotte
- Migliorato: Lista di selezione della lingua

## 1.9.8 (2024-09-28)

- Aggiunto: Servizio di traduzione "Zhipu BigModel"
- Rimosso: Modello "SiliconCloud" qwen1.5-7B-chat (a causa della discontinuazione ufficiale)
- Corretto: Risolto il problema di compatibilità del login con il plugin Safari su macOS 15

## 1.9.7 (2024-09-20)


- Supporto input migliorato per Baidu, Gmail e altri campi di input
- Supporto per l'header della richiesta anthropic-dangerous-direct-browser-access per l'API Claude Anthropic
- Supporto per il download dei sottotitoli dai video di Hulu, Bloomberg e Domestika
- DeepX supporta la traduzione del testo ricco
- Risolto il problema della mancata sincronizzazione degli esperti AI personalizzati

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) supporta la copia delle formule (fare clic con il tasto destro sulla formula per vedere il menu di copia)
- Risolto il problema della visualizzazione dei sottotitoli bilingue per più video sulla stessa pagina Twitter
- Risolti alcuni bug

## 1.9.3 (2024-09-05)

- L'opzione per la visualizzazione confronto bilingue/solo traduzione è stata spostata nelle impostazioni generali.
- Per impostazione predefinita, il sistema ricorderà la modalità attivata cliccando sull'icona nel pannello per il confronto bilingue o la visualizzazione solo traduzione. Per cambiare temporaneamente, cliccare su "Altro" -> "Passa alla visualizzazione solo traduzione" nel pannello.
- Per impostazione predefinita, la traduzione dal cinese semplificato al tradizionale e viceversa utilizzerà la modalità solo traduzione, anziché la modalità confronto bilingue.
- Risolti alcuni bug.

## 1.9.1 (2024-09-03)

- Supporto per la configurazione delle eccezioni per lingue e siti web in modalità contrasto bilingue o solo traduzione (configurare nella pagina Impostazioni -> Impostazioni Avanzate). Per esempio: Se la tua modalità di traduzione predefinita è il contrasto bilingue, ma non desideri che il cinese tradizionale utilizzi anche il contrasto bilingue, puoi aggiungere il cinese tradizionale alle lingue di eccezione per il contrasto bilingue, così il cinese tradizionale utilizzerà la modalità solo traduzione per la traduzione. Allo stesso modo, se la tua modalità di traduzione predefinita è solo traduzione, ma desideri che una certa lingua o sito web utilizzi la modalità contrasto bilingue, puoi anche aggiungere quella lingua o sito web alle lingue di eccezione.
- Risolto un problema in cui la casella di input nell'interfaccia dei messaggi privati di Tiktok veniva tradotta in modo errato
- Risolto un problema in cui i fumetti su Read Comic Online non potevano essere tradotti
- Risolto un problema in cui le 【Impostazioni Avanzate -> Numero minimo di caratteri richiesti per tradurre un paragrafo】 non avevano effetto in alcuni casi

## 1.8.4 (2024-08-30)

- Il servizio di traduzione DeepL ora supporta ufficialmente il cinese tradizionale come lingua di destinazione (in precedenza, la traduzione in cinese tradizionale con DeepL comportava un ulteriore processo di conversione da cinese semplificato a tradizionale di terze parti).
- Ottimizzate le prestazioni di traduzione del testo ricco.

## 0.12.8

- Riparazione dei sottotitoli originali del video non visualizzati quando "Il sito corrente è impostato per non tradurre mai".
- Risolto il conflitto con alcuni plug-in che causano il ritorno infinito della pagina.
- Riparazione della non traduzione di alcuni paragrafi dopo aver attivato gli interruzioni di riga dei paragrafi lunghi.
- Risolto [Quando si attiva temporaneamente la traduzione della pagina web per un lungo periodo, cliccando sul pannello [Traduci sempre questo sito web] non si annulla la traduzione sempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Aggiunti sottotitoli bilingue per supportare le piattaforme [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/)
- L'hoverball è ora nascosto per impostazione predefinita quando il video è a schermo intero.
- Risolto il problema del clic tremolante del pannello di azione hoverball della pagina di firefox.
- Supporto per la collaborazione sotto il sito pubmed.ncbi.nlm.nih.gov e il plugin scholarscope
- Risolto il problema della tremolazione della pagina di traduzione della casella di input di reddit

## 0.12.6

- Risolto il problema che la traduzione di YouTube/Web of Science ecc. non è sensibile quando si cambiano le schede.
- L'hoverball su mobile ora supporta l'operazione a lunga pressione, pressione breve per tradurre, pressione lunga per aprire il pannello.
- Traducendo ebook bilingue ora verrà tradotto anche l'indice.
- La funzione di Miglioramento della Ricerca (alcune pagine di Ricerca Google mostrano risultati di ricerca bilingue) ora non è abilitata per impostazione predefinita e verrà rimossa nella prossima release.## 0.12.5

- Correzione della creazione di eBook in formato Epub dal pannello cliccando sulle traduzioni che non funzionava

## 0.12.4

- Quando si attivano i sottotitoli bilingui nel pannello, la pagina verrà prima aggiornata automaticamente (per visualizzare i sottotitoli bilingui con maggiore precisione), e alcuni siti richiedono ancora agli utenti di cliccare manualmente sul pulsante "CC" sul sito per attivare i sottotitoli.
- Ottimizzazione del rilevamento della lingua in Grease Monkey e Safari
- Fornisce un accesso rapido alle versioni bilingui di tutti gli articoli sul sito dei [documenti Arxiv](https://arxiv.org/abs/1910.06709).
- [Supporto Hoverball configurato per essere fissato a sinistra #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Correzione del problema di visualizzazione della Modalità Apprendimento #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Attivare temporaneamente la traduzione web per un certo periodo di tempo non annulla la funzione Traduci Sempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Ottimizzazione dei problemi di inizializzazione dei file PDF

## 0.12.3

- Correzione per la funzione [disabilitare permanentemente i sottotitoli video] che non funzionava [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)## 0.12.2

- Supporto sottotitoli bilingue fornito per più piattaforme video, ora supportate: [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy](https://www.khanacademy.org/), [Coursera](https://www.coursera.org/), [Vimeo](https://vimeo.com/), [Nebula](https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), ecc. (Nota che a causa delle limitazioni tecniche, alcuni siti web necessitano di aggiornare la pagina dopo aver attivato per la prima volta i sottotitoli bilingue o attendere il completamento della traduzione per visualizzare i sottotitoli bilingue).
- Ottimizzazione significativa della dimensione del file zip del plugin, ridotta della metà rispetto all'originale, più veloce nel download e nell'aggiornamento.
- Risolti problemi di download di PDF estesi.
- Aggiunto un portale di traduzione rapida PDF sul lato destro del sito degli articoli [Arxiv](https://arxiv.org/abs/1910.06709), che porta a una pagina HTML pulita (supportato solo da alcuni articoli, poiché richiede che gli autori originali inviino il codice sorgente, quindi circa il 50% degli articoli mostrerà questo portale).
- Le pagine PDF online senza estensione .pdf possono ora saltare direttamente alla pagina di traduzione PDF cliccando sulla hoverball sulla pagina.
- Risolti alcuni problemi di miglioramento delle caselle di input sotto Safari.
- Ottimizzazione del rilevamento della lingua in Grease Monkey e Safari.## 0.11.6

- Aggiunte 11 nuove lingue dell'interfaccia per il plugin e il sito ufficiale, ora le lingue dell'interfaccia supportate raggiungono quota 14, incluse Cinese Semplificato, Cinese Tradizionale, Inglese, Giapponese, Coreano, Russo, Spagnolo, Portoghese, Hindi, Italiano, Tedesco, Francese, Arabo e Persiano.
- Modifica della condivisione bilingue (modalità di aggiornamento) aggiunta nell'ultima versione alla condivisione di snapshot di pagine bilingue, in modo che il contenuto condiviso sia più originale, oltre a una maggiore adattabilità.
- Correzione degli emoji alla fine del box di inserimento di Twitter che non possono essere tradotti
- Correzione della situazione in cui il contenuto di plugin di terze parti viene tradotto in alcuni scenari
- Riparazione del click non responsivo dell'hoverball pdf online

## 0.11.5

- Ora puoi generare un link pubblico alla pagina bilingue tradotta per Immersive Translate.
  - [Clicca](/docs/share/) sull'icona di condivisione di Immersive Translate per generarlo con un clic!
- Risolto il problema che alcune piattaforme non potevano riconoscere se il mouse era supportato o meno
  - Ci sono alcuni browser desktop che supportano sia il touchscreen che il mouse, e Immersive Translates è tecnicamente incapace di rilevare se tali piattaforme supportano il mouse, quindi abbiamo aggiunto l'opzione [Forza Abilitazione Supporto Mouse] nelle impostazioni [Mouse Hover]

## 0.11.2-0.11.4

- Ottimizzazione dell'esperienza, correzione di alcuni bug

## 0.11.1

- Il modello predefinito per le traduzioni OpenAI è: GPT3.5-turbo-1106.
- Ottimizzata la Prompt Cinese per OpenAI, ora meno incline a allucinazioni!
- Ridotta la lunghezza delle prompt di OpenAI da 90 a 40, risparmiando ancora più traffico.

## 0.11.0

- Correzione dei click dell'hoverball di pagina instabili
- Risoluzione dei problemi di traduzione di Azure

## 0.10.9

- Correzione di alcuni problemi minori## 0.10.8

- Supporto per l'impostazione dei pulsanti di traduzione rapida hoverball (supporto sia per PC/mobile)
- Ottimizzazione del giudizio linguistico di Grease Monkey
- Correzione della traduzione dei file txt

## 0.10.7

- Supporto al passaggio del mouse premere di nuovo Ctrl per mostrare il testo originale
- Ignora al passaggio del mouse Mai tradurre la lingua
- Ottimizzazione dei sottotitoli bilingui di Youtube

## 0.10.6

- Supporto ai sottotitoli di Youtube solo per le traduzioni
- Aggiunta di un avviso di aggiornamento per la versione bassa di Grease Monkey
- Risolto il problema che i file txt locali non potevano essere tradotti

## 0.10.5

- Correzione del ritorno occasionale alla homepage di Youtube

## 0.10.4

- Correzione del conflitto dei sottotitoli di Youtube con il plugin Dual subtitle (La traduzione dei sottotitoli immersiva di Youtube non è abilitata quando viene rilevato il plugin Dual di Youtube per evitare conflitti)
- Aggiunta [Disabilitazione permanente della funzione dei sottotitoli video], se ci sono altri problemi di conflitto e non si desidera abilitare la funzione di sottotitoli bilingui con Immersive Translate.
- Ottimizzazione delle interruzioni dei sottotitoli

## 0.10.3

- Correzione del problema di traduzione con la chiave Auth Custom DeppL

## 0.10.3

- Supporto perfetto per i video di Youtube con sottotitoli bilingui 🎉.
- Per le pagine degli articoli, il testo principale sarà ora tradotto prima del resto del contenuto della barra laterale
- Ottimizzazione della contestualizzazione della traduzione DeepL
- Ottimizzazione della contestualizzazione della traduzione dei file di sottotitoli con OpenAI

## 0.10.1

- Aumento della priorità della traduzione del corpo per ottimizzare l'esperienza di traduzione
- Correzione del problema di non traduzione del testo cliccato su ins più volte

## 0.9.8

- Ottimizzazione dell'esperienza, correzione di alcuni bug

## 0.9.7

- Correzione della traduzione automatica quando readwise è evidenziato

## 0.9.6

- Correzione della cancellazione della cache effettuando il logout del login dell'utente.

## 0.9.5

- Correzioni di bug per gli eBook online## 0.9.4

- Ottimizzazione del rilevamento del miglioramento dell'input per ridurre i tocchi accidentali
- Traduzione online di e-book e sottotitoli

## 0.9.3

- Traduzione della Casella di Input: visualizza un promemoria pop-up quando viene utilizzato per la prima volta, e l'utente può scegliere di disabilitarlo questa volta o permanentemente per evitare tocchi accidentali.
- Ottimizzazione della velocità di esportazione della traduzione solo PDF, se si sceglie di esportare solo la traduzione, si può chiamare direttamente l'anteprima PDF del sistema per esportare, più velocemente.
- Deeplx supporta più URL, basta dividerli con un punto.

## 0.9.2

- Lo strumento di traduzione PDF è migrato alla versione online: https://app.immersivetranslate.com/pdf/ , così che Grease Monkey e Safari possano utilizzare la traduzione PDF, e i problemi possono essere iterati meglio senza la necessità di emettere una versione per risolvere il problema.
- Ottimizzazione dell'UI POPUP, il pannello è più bello!

## 0.9.1

- Risoluzione dei problemi di nome file con la creazione di ebook Epub

## 0.8.8

- supporto pdf per gli aggiustamenti di spaziatura delle linee e delle parole per riconoscere nuovamente i paragrafi
- risoluzione del problema dello scorrimento automatico mobile per la lettura online di epub

## 0.8.7

- supporto pdf per il download della traduzione soltanto
- Risoluzione del problema di accesso Google con Safari

## 0.8.2 - 0.8.6

- Consente di impostare l'intervallo tra i trigger combinati del miglioramento dell'input
- Risoluzione di alcuni bug

## 0.8.1

- Ottimizzazione del Rilevamento della Lingua
- Funzionalità Beta: API Personalizzata (Beta abilitata nelle impostazioni dello sviluppatore)
- Supporto per la Traduzione di AliCloud
- Risolti alcuni bug## 0.8.0

- Sistemi Utente Supportati
- Supporta [Abilita Abbonamento Pro](/pricing), che permette agli utenti di godere delle traduzioni di Deepl e OpenAI e delle impostazioni di sincronizzazione cloud.
- Il servizio di traduzione al passaggio del mouse può essere impostato individualmente
- Il servizio di traduzione del box di input può essere configurato separatamente
- Ottimizzazione della Traduzione PDF
- Risolti alcuni bug

## 0.7.16

- Traduzione PDF con nuove opzioni per un rapido controllo dello stile di traduzione (i file PDF sono molto strani e attivare queste opzioni può essere utile per alcuni file PDF con formattazione disordinata)
- Le versioni iOS e macOS sono tornate sullo Store di Apple per i Paesi

## 0.7.15

- Siamo stati informati da Apple che le Traduzioni OpenAI sono state temporaneamente rimosse da iOS e macOS, e stiamo cercando di rilanciarle in Cina.

## 0.7.11- 0.7.14

- Correzione: problema di Traduzione di Gmail in Tutte le Regioni
- Disabilitazione temporanea della funzione di esportazione PDF di Safari a causa della restrizione di Safari sui download di plug-in (bug).
- Risolti alcuni altri problemi

## 0.7.10

- Aggiornamento dell'UI del Pannello Icone del Browser Popup, un po' più di design ～
- Risolto il problema che alcuni passaggi in giapponese non venivano tradotti.

## 0.7.9

- Il PDF supporta finalmente l'esportazione delle versioni bilingui! Puoi cliccare il pulsante [Salva] per esportare il file PDF tradotto bilingue.
- Le regole personalizzate ora supportano la fusione con le regole predefinite integrate, es.: `{"id": "youtube", "selectors.add":["#test"]}` significa aggiungere un `#test` ai selettori esistenti, `selectors` significa sovrascrivere il predefinito, `selectors.remove` significa eliminare uno dei selettori predefiniti, e `selectors.remove` significa eliminare uno dei selettori predefiniti, e `selectors.remove` significa eliminare uno dei selettori predefiniti. rimuove uno dei selettori predefiniti.
- Aggiornata l'icona di Safari, un po' più grande.
- Altre Correzioni di Bug## 0.7.8

- Correzioni di bug

## 0.7.7

- Adattato allo stile di sistema di Safari, l'icona dell'estensione di Safari è stata cambiata in un contorno trasparente.
- Aggiunto il cambio di stato dell'icona del browser, quando una pagina web è stata tradotta, un ✅ verrà aggiunto automaticamente nell'angolo in basso a destra dell'icona del browser.
- Abilitazione automatica della traduzione dei siti web in inglese più utilizzati per i nuovi utenti
- Risolti problemi di traduzione con https://claude.ai/

## 0.7.6

- Supporto Migliorato all'Input per i Risultati di Traduzione ctrl+z Annulla
- Supporto alla traduzione in modalità di lettura del documento Flying Book
- Adattamento per https://pi.ai/talk

## 0.7.5

- Risolto il problema dell'icona di Grease Monkey che non viene visualizzata
- Risolti numerosi problemi

## 0.7.4

- Risolti numerosi problemi
- La pagina di configurazione supporta l'eliminazione in batch degli URL selezionati.
- Supporta l'abilitazione/disabilitazione della traduzione dei sottotitoli di Youtube per prevenire conflitti con altri plugin correlati.
- Arigato Translator supporta l'impostazione di campi e l'ID di terminologia

## 0.7.2

- Miglioramento Casella di Input: permette di omettere il prefisso // e attiva la traduzione dell'intera casella di input con 3 spazi, oppure puoi disattivare questa opzione nella pagina delle impostazioni.

## 0.7.1

- Supporto al Miglioramento della Ricerca, quando abilitato, quando cerchi su Google/Google News in cinese, la colonna di destra mostrerà automaticamente i risultati di ricerca delle corrispondenti parole chiave in inglese, che è abilitato per impostazione predefinita.

  - Motivo: Abbiamo scoperto che nella ricerca Google, i risultati di ricerca per le parole chiave in cinese e in inglese possono essere molto diversi, con il Miglioramento della Ricerca Tradotta Immersiva abilitato, cerchiamo automaticamente per te le stesse parole chiave in inglese e le visualizziamo sul lato destro. Puoi scegliere di disabilitarlo se non hai bisogno della funzione.
  - Safari non è supportato a causa delle limitazioni dell'API.## 0.6.20

- Modifica delle impostazioni predefinite: A seguito del feedback di un gran numero di utenti che non utilizzeranno lo strumento di traduzione dopo l'installazione, la loro aspettativa riguardo allo strumento di traduzione è che traduca automaticamente le pagine web in inglese dopo l'installazione, quindi da questa versione in poi, per gli utenti cinesi, l'opzione di tradurre automaticamente le pagine in inglese è stata attivata (se l'utente aveva precedentemente impostato una lingua che sarebbe sempre stata tradotta, questa verrà rispettata, e il cambiamento modifica solo le impostazioni iniziali dell'estensione), e se necessario disattivarla, può essere facilmente disattivata nel [Pannello popup o nella pagina delle impostazioni](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- Correzione di bug nei PDF
- Correzione del bug di Web of Science
- Adattamento per feeder.com
- Correzione della mancata traduzione di alcuni libri in formato epub

## 0.6.18

- Correzione del problema di sovrapposizione della larghezza del popup in Safari.
- Ottimizzazione del processo di costruzione

## 0.6.17

- Ottimizzazione degli avvisi di errore
- Ottimizzazione della selezione della lingua di destinazione, ora verranno mostrate solo le lingue supportate dal servizio di traduzione corrispondente
- Ottimizzazione della traduzione dei PDF
- Adattato per il sito web di Good Reads, Amazon e South China Morning Post

## 0.6.16

- Aggiunta della visualizzazione della pagina di mancato permesso per i PDF
- Riparazione della visualizzazione dei paragrafi dell'elenco di testo dei PDF
- Ingrandimento della scala del font piccolo nei PDF su Chrome e Safari

## 0.6.15

- Riparazione del problema che si verifica all'apertura dei file PDF, quando il pannello dell'estensione segnala che non ci sono permessi.
- Correzione del problema per cui il miglioramento del box di input non è abilitato quando il sito è impostato per non tradurre mai.## 0.6.14

- Ottimizzazione della traduzione PDF, l'area di traduzione può ora essere modificata/trascinata/eliminata
  - Trascina in alto a sinistra, elimina in alto a destra, cambia dimensione in basso a destra
- Allineamento a sinistra del box a discesa di Windows
- Supporto per il cinese tradizionale e il cinese semplificato

## 0.6.13

- Risolto il problema della traduzione ripetuta al passaggio del mouse
- Supporto alla traduzione dei PDF con trascinamento per cambiare le dimensioni e modificare il contenuto della traduzione

## 0.6.12

- Risolti i problemi delle immagini di traduzione Epub che si riducono in alcuni browser
- Ottimizzata la traduzione del box di input, ora funziona senza intoppi in Bard!

## 0.6.10

- Modello di default di OpenAI cambiato alla versione 0613
- Risolti alcuni stili del box di input
- Più intelligente nel determinare se si tratta di un'area di navigazione, e in tal caso, non viene eseguita la traduzione
- Risolto possibile attacco di iniezione XSS

## 0.6.8

- Il pannello dell'estensione può ora indicare pagine non supportate (ad es. pagine senza permessi e pagine non HTML)
- Miglioramento del box di input per mostrare lo stato di caricamento nella traduzione
- Aggiornati i colori di caricamento predefiniti nelle traduzioni
- Quando il box di input è configurato senza prefisso, supporta la traduzione in giapponese con `ja Ciao` e in inglese con `Inglese Ciao`.

## 0.6.6

- Correzione per: alcune aree non tradotte (quora)

## 0.6.5

- Ottimizzazione Google Bard
- La traduzione del box di input supporta la traduzione diretta dell'intero box di testo senza prefissi.
- Ottimizzato il problema delle traduzioni di OpenAI che aggiungono punti senza motivo, (se non viene rilevato un punto nel testo originale, se OpenAI restituisce un punto, allora rimuoverlo)
- Problemi con i file di sottotitoli di safari non riconosciuti

## 0.6.3

Il linguaggio predefinito per la traduzione del box di input può ora omettere lo spazio, ovvero //Ciao Mondo può essere tradotto altrettanto bene.## 0.6.2

L'aggiornamento più entusiasmante per il box di inserimento è qui:

- Digita: // Hello World nella casella di inserimento su qualsiasi pagina web, poi premi tre volte lo spazio per tradurre il paragrafo in inglese
- Puoi anche specificare la traduzione in una certa lingua: /ja Hello World, poi premi tre volte lo spazio per tradurre il paragrafo in giapponese

[Clicca qui per una rapida introduzione di 30 secondi](/docs/input/)

## 0.6.0

- Primo rilascio a giugno, migrato dal precedente sottodominio personale https://immersive-translate.owenyoung.com al nuovo dominio https://immersivetranslate.com/
- La funzionalità è in gran parte invariata (nuove funzionalità saranno disponibili nella prossima release!)

## 0.5.17

- Risolto il problema che: gli eBook bilingui non hanno immagini dopo l'esportazione

## 0.5.16

- Risolto: problema di traduzione openai in cinese tradizionale

## 0.5.15

- Ottimizzato: Il numero minimo di caratteri in un paragrafo che attiva la traduzione è stato modificato in un minimo di 4 caratteri per ridurre la confusione, utilizzando al contempo altre funzionalità per evitare di tradurre le aree di navigazione e di fine del sito.
- Risolto: Dettagli Github non tradotti dopo l'espansione.

## 0.5.14

- Risolto il problema che le immagini su alcune pagine web: diventano più grandi dopo la copia
- Risolto: sezione commenti di medium non tradotta
- Risolto il problema che le immagini su alcune pagine: venivano copiate in modo errato

## 0.5.12

- Funzionalità: Stile di Traduzione con Linea di Divisione aggiunge una linea verticale di divisione per le traduzioni su singola linea
- Risolto: Casi molto rari di divisione dei paragrafi.
- Una fantastica pagina di orientamento per la prima configurazione per i nuovi utenti iOS.## 0.5.11

- Supporto alla traduzione dei sottotitoli per esportare solo le traduzioni
- Correzione: Alcuni elementi non vengono riconosciuti al passaggio del mouse
- Correzione: Interruzioni parziali di riga nei tweet non riconosciute
- Correzione: Stile di autore di eBook non funzionante

## 0.5.10

- Correzione: Interruzioni di riga nei tweet non riconosciute
- Correzione: La pagina di dettaglio di Reddit restituisce alcuni paragrafi che non possono essere tradotti
- Risolto un problema con: dove alcuni dei tag Code non venivano riconosciuti correttamente.

## 0.5.9

- Corregge le interruzioni di paragrafo in alcuni casi a:
- Correzione: L'interruttore Tampermonkey Mostra Solo Traduzioni
- Correzione: Problema con lo stile di lettura online di eBook non funzionante

## 0.5.8

- Risolto il problema che: l'impostazione temporanea della durata della traduzione del sito web non ha effetto.## 0.5.7

- Super aggiornamento!

- La funzione Mostra Solo Traduzioni è qui! Clicca su [Altro] -> [Passa a mostra solo traduzioni].

  - Supporto per scorciatoie personalizzate, impostabili in impostazioni interfaccia -> Impostazioni Scorciatoie

- Ottimizzazione del problema di limitazione della frequenza di richiesta OpenAI

- ChatGPT di default al modello mobile, che è più veloce!

- Refactoring del parsing del core web, il che significa:

  - Traduzione di pagine web su larga scala in secondi
    - Per esempio: https://pve.proxmox.com/pve-docs/pve-admin-guide.html, che prima richiedeva 30 secondi, ora è istantanea.
  - Uso della memoria ultra-basso per pagine web complesse
    - Per esempio: https://www.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Adattamento a più siti web

- Supportate tutte le traduzioni dei siti web ShadowRoot.

  - Per esempio: https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - Per esempio, la sezione commenti di: https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Risolto il problema dello schermo bianco dopo la traduzione di siti web con idratazione come Next.js.

  - Per esempio: https://webpack.js.org/

- Risolto il problema che richiedeva l'aggiornamento della pagina per rendere effettiva la modifica della scorciatoia al passaggio del mouse

- Risolto un problema con il riconoscimento degli a capo nei file TXT.

- Tanti aggiornamenti!

- La funzione 'Mostra Solo Traduzioni' è arrivata! Clicca su 'Altro' -> 'Passa a Mostra Solo Traduzioni'.

  - Supporta scorciatoie personalizzate, che possono essere impostate in 'Impostazioni Interfaccia' -> 'Impostazioni Scorciatoie'

- Ottimizzato per il problema del limite di frequenza delle richieste OpenAI

- Il parsing del core web è stato ricostruito, il che significa.

  - Traduzione istantanea per siti web di grandi dimensioni
  - Uso minimo della memoria per pagine web complesse
  - Migliore compatibilità con più siti web

- Ora supporta traduzioni per tutti i siti web con ShadowRoot.

- Risolto il problema dello schermo bianco dopo la traduzione di siti web con idratazione, come Next.js

- Risolto il problema per cui era necessario aggiornare la pagina per rendere effettiva la modifica della scorciatoia al passaggio del mouse

- Risolto il problema con il riconoscimento degli a capo nei file TXT.## 0.5.6

- Correzione: problema della finestra di nuova scheda su macOS.
- Novità: Nuova pagina guida per l'utente nuovo.

## 0.5.5

- Correzione: Problema dell'area al passaggio del mouse.

## 0.5.4

- Correzione: Duplicazione della pagina Spa

## 0.5.3

- Correzione: Ascoltatore di scelta rapida al passaggio del mouse.
- Correzione: Traduzione del documento PDF
- Novità: Aggiunta nuova pagina guida per il cliente

## 0.5.2

- Correzione: impostazioni delle scorciatoie del mouse hover per gli userscript

## 0.5.1

- Correzione: L'API di OpenAI non funziona.

## 0.5.0

- Novità: Traduci il paragrafo corrente al passaggio del mouse.
- Novità: Rifacimento della traduzione PDF, ora puoi tradurre la maggior parte dei PDF con Immersive Translate
- Correzione: Disabilitazione del menu contestuale non funzionante [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Correzione: Evita la Politica di Sicurezza dei Contenuti per [Mastodon](https://mastodon.social/)

## 0.4.11

- Correzione: permesso dello userscript (solo per userscript).

## 0.4.8

- Novità: Bing Translate a Microsoft Translate per una qualità più stabile.
- Correzione: Pagina web TXT puro come [questa](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Prestazioni: Esclusione di alcune pagine pubblicitarie figlie nel sito web, e le prestazioni sono leggermente migliorate

## 0.4.7

- Correzione: Mancanza del popup dello Userscript su Firefox.

## 0.4.6

- Novità: Consenti a terze parti di inviare l'evento del documento per chiamare `toggleTranslatePage`
- Novità: L'app iOS aggiunge il pulsante di abilitazione dell'estensione e il link alle comunità
- UI: Nel campo delle impostazioni di OpenAI si usa un menu a tendina invece di una casella di testo.## 0.4.5

- Correzione: problema con l'estensione safari su iOS 15.0.
- Correzione: scorciatoie per l'estensione safari su macOS.
- Correzione: popup della politica di sicurezza dei contenuti per l'estensione, e parzialmente per lo userscript.

## 0.4.4

- Operazione: Rimozione di console.log

## 0.4.3

- Correzione: rilevamento degli spazi bianchi nei tag sup, sub.
- Funzionalità: supporto del sito web ChatGPT Plus come servizio di traduzione. Questa è una funzionalità beta, quindi è possibile accedervi abilitando la Funzionalità Beta nelle impostazioni dello sviluppatore. Questo processo è molto lento, poiché chatgpt può inviare solo una richiesta alla volta. Assicurati di avere un account ChatGPT Plus, poiché ci sono più limitazioni sull'Account Gratuito, e non sono sicuro se ciò possa comportare rischi per il tuo account, fai attenzione nell'usarlo.

## 0.4.1

- Correzione: il menu contestuale di firefox scompare dopo il riavvio.
- Supporto per Azure openai

## 0.4.0

- Funzionalità: Supporto per la traduzione di file di sottotitoli locali (.srt, .ass, ecc.)

## 0.3.17

- Funzionalità: Supporto per la traduzione di file .txt locali.
- Correzione: Il Menu Contestuale potrebbe non essere disponibile a volte. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Correzione: mantenere &nbsp; come spazio bianco.
- Rimozione: Rimozione di Papago, poiché [il servizio non è più disponibile](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: permettere l'uso senza chiave API per openai
- UI: permettere il ripristino delle impostazioni predefinite di Open AI## 0.3.14

- Dipendenza: Aggiorna pdf.js all'ultima versione
- Correzione: colore di sfondo della selezione pdf
- Correzione: rilevamento degli spazi bianchi

## 0.3.13

- Correzione: problema di caratteri specifici del costruttore di ebook, come alcuni percorsi di capitolo sono `xxx' xxxx`.
- UI: nasconde per impostazione predefinita le opzioni personalizzate di openai.
- UI: Aggiungi lo stato di esportazione per l'esportazione in epub.
- Correzione: prompt predefinito di Gpt4

## 0.3.12

- Funzionalità: Ora possiamo personalizzare il colore di sfondo del tema di traduzione di Marker.
- Correzione: postMessage quando si inizializza la pagina ha interrotto alcuni siti, ora lo faremo solo quando traduciamo realmente le pagine
- Correzione: problema di avanzamento dell'ebook.
- Correzione: migliore per dividere lunghi paragrafi, 1,5 miliardi, 25,5%, Mr. non sarà considerato come un confine

## 0.3.11

- Correzione: colore del testo della modalità scura del lettore di ebook
- Correzione: prompt di openAI

## 0.3.10

- Migliore: rileva il contenitore giapponese/coreano.
- Correzione: Progresso Costruttore Ebook fermo al 99%.

## 0.3.9

- Correzione: Lo stato dell'input dei servizi di traduzione dello switch dell'UI Opzioni non cambiato.

## 0.3.8

- UI: colore di caricamento più trasparente
- Correzione: Rileva la lingua dell'Ebook.
- Funzionalità: Aggiungi progresso di traduzione per il costruttore di ebook, e una bella pioggia di coriandoli dopo il successo.
- Funzionalità: Aggiungi riprova tutti i paragrafi falliti per il pulsante di riprova.
- Correzione: Gestione dell'errore Deepl

## 0.3.7

- Correzione: il lettore di ebook non può caricare immagini su Chrome.

## 0.3.6

- UI: migliore per rendere l'interfaccia utente della pagina dell'ebook

## 0.3.5

- Correzione: esportazione dell'ebook userscript
- Funzionalità: aggiungi endpoint API personalizzato per OpenAI
- Funzionalità: aggiungi opzioni temporanee di traduzione del sito web su `Impostazioni Avanzate`## 0.3.4

- CI: Costruzione fallita

## 0.3.3

- Correzione: creatore di ebook per Kindle
- Modifica: Colore dell'icona di caricamento, da nero a blu, per adattarsi alla pagina web in modalità scura.
- Funzionalità: Supporto per la traduzione locale di html per estensione

## 0.3.2

- Correzione: Movimento del cursore nel Form di opzioni.
- Funzionalità: Supporto OpenAI per apiUrl personalizzato per impostazioni di sviluppo.

## 0.3.1

- Funzionalità: aggiornamento dell'icona scura a trasparenza.
- Correzione: Ordine errato per paragrafi lunghi

## 0.3.0

- Versione: D'ora in poi, cambieremo il numero di versione minore una volta al mese, per esempio, ora in marzo, la versione inizierà da 0.3.0, in aprile, il numero di versione inizierà da 0.4.0, il prossimo aprile, il numero di versione sarà 1.4.0, e così via. Questo perché non ha senso che le estensioni seguano Questo perché non ha senso che le estensioni seguano la semantica, ma standardizzare i numeri di versione secondo le leggi del tempo è una motivazione per lo sviluppo per continuare ad aggiornarsi, e per gli utenti per trovare problemi più facilmente.
- Funzionalità: Supporto per icona scura su firefox

## 0.2.86

- Aggiunta opzione di lunghezza massima del testo per richiesta con Open AI
- Correzione: identificatore di ebook duplicato
- Funzionalità: Supporto per la traduzione di pagine web txt

## 0.2.85

- Correzione: alcuni file epub non possono essere trovati.

## 0.2.84

- Funzionalità: Supporto per Ebook Reader e Maker

## 0.2.83

- Funzionalità: Permettere al Form di inserimento password di mostrare la password.## 0.2.82

- Correzione: Alcuni siti utilizzano `span` per gli stili, quindi usiamo `font` invece di span per il wrapper dell'obiettivo di traduzione
- Correzione: Limite massimo di token di OpenAI, cambia il numero massimo di caratteri da 1500 a 1300.

## 0.2.81

- Correzione: m.youtube.com
- Correzione: interfaccia utente del modulo opzioni
- Correzione: prompt di Open AI
- Funzionalità: Supporto per più chiavi OpenAI, usare `,` per dividerle.

## 0.2.80

- Funzionalità: Aggiungi Menu Abilita/Disabilita per popup -> altro
- Correzione: Conflitto messaggi DingTalk

## 0.2.79

- Correzione: Open AI per paragrafo con spazi

## 0.2.78

- Funzionalità: supporto per OpenAI CHATGPT 3.5 (supporta l'interfaccia OpenAI ChatGPT 3.5)
- Funzionalità: Aggiungi nuovo tema Bordo Solido

## 0.2.77

- Correzione: errore multiplo tag codice.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Correzione: errore multiplo tag codice [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Funzionalità: Supporto per il conteggio del testo di traduzione immediata personalizzato per diversi servizi di traduzione.

## 0.2.74

- Funzionalità: Supporto Tencent (alpha)
- Correzione: traduzione openai
- Correzione: controllo inline tag sconosciuti

## 0.2.73

- Funzionalità: Supporto per il Tema di Traduzione Grigio
- Correzione: Pagina Trending di Github

## 0.2.72

- Correzione: verifica del servizio di traduzione di firefox mobile net issue.

## 0.2.71

- Correzione: permesso userscript di Open AI## 0.2.70

- Correzione: segnaposto Open AI

## 0.2.69

- Funzionalità: Supporto a Open AI come servizio di traduzione.
- Funzionalità: Verifica del servizio di traduzione su options.html
- Funzionalità: Supporto per frame principale personalizzato poiché alcuni siti non utilizzano body come frame principale

## 0.2.68

- Supporto a Caiyun (Alpha)
- Correzione di tag di blocco sconosciuti

## 0.2.67

- Funzionalità: Aggiunta di `<all>` per tradurre sempre le lingue, quindi ora puoi usarlo per tradurre tutte le lingue eccetto la lingua di destinazione, e mai le lingue da non tradurre
- Correzione: Consenti configurazione personalizzata dell'API Google
- Miglioramento: Supporto Deepl Free
- Correzione: uso elevato di memoria per userscripts ed estensioni (rimuovendo opencc da zh-CN a zh-TW, sostituendolo con Google translate)
- Correzione: Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Correzione: configurazione di Azure translate ma continua a mostrare (necessita configurazione)

## 0.2.66

- Correzione: Fallimento nella traduzione di file PDF, Bug dalla versione 0.2.60 per il supporto di deepl da zh-CN a zh-TW

## 0.2.65

- Supporto alla limitazione delle richieste per frame multipli
- Non tradurre il titolo della pagina quando in iframe

## 0.2.64

- Correzione: scelta dei servizi di traduzione openl
- Funzionalità: Supporto all'opzione di traduzione del titolo

## 0.2.63

- Funzionalità: Supporto al servizio di traduzione Azure
- Funzionalità: Supporto al servizio di traduzione Papago
- Correzione: sincronizzazione di Google Drive su Firefox Android nativo.
- Correzione: cambiamento della trasparenza da 0.4 a 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Correzione: suggerimenti scorciatoie popup
- Prestazione: da richieste seriali a concorrenti
- Miglioramento nel rilevamento del conteggio giapponese## 0.2.62

- Novità: Aggiunta regola waitForSelectors, per risolvere alcuni siti come reddit

## 0.2.61

- Correzione: lo userscript è troppo grande per greasy fork
- Miglioramento: riduzione delle dimensioni del file

## 0.2.60

- Novità: Supporto da zh-CN a zh-TW per Deepl
- Novità: Funzione di Traduzione Immersiva Deepl
- Novità: Supporto per l'ingrandimento personalizzato delle dimensioni del font
- Correzione: Stile del forum di Steam
- Correzione: lo stile globale non cambia dopo la generazione di elementi dinamici
- Correzione: promuovere la priorità di esclusione
- UI: cambiamento della pagina delle informazioni
- Correzione: alcuni elementi matematici rimangono originali

## 0.2.59

- Correzione: Blocco Elemento per Tag Sconosciuti
- Correzione: sovrascrittura dell'elemento translate=no
- Correzione: corrispondenza dell'url con più \*

## 0.2.58

- Novità: Supporto per il colore del testo di traduzione personalizzato, colore del bordo.

## 0.2.57

- Nessun cambiamento, ricostruzione

## 0.2.56

- Correzione: duplicazione della traduzione per elementi inline con elemento di codice.
- Correzione: controllo inline/block per tag sconosciuti
- Novità: supporto per css iniettato sul pannello degli sviluppatori
- Novità: taglio di authKey, appid appSecret
- Miglioramento: apertura della pagina delle impostazioni in una nuova scheda (ma non per Stay)

## 0.2.55

- Tentativo di correzione della codifica dell'api deepl

## 0.2.54

- Rimozione del permesso tabs per il rifiuto del chrome store
- Correzione: traduzione dell'intera pagina, il piè di pagina è ignorato
- Aggiunta di note alla pagina delle informazioni
- Supporto per url personalizzato da Config incorporato

## 0.2.53

- Correzione: errore di sincronizzazione di google drive dello userscript.

## 0.2.52

### Codice

- Uso dell'ultima versione di esbuild
- Uso dell'ultima versione di deno
- CI: invio del codice sorgente a firefox## 0.2.51

- Risolto il bisogno di accesso a Google Auth su Chrome/Firefox
- Sostituiti i link dei servizi di traduzione
- Migliorato per il permesso.
- rimosso minify.

## 0.2.50

- Risolto il problema di caricamento su Google Drive (davvero) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Rimossi i collegamenti rapidi alt+d, alt+s perché potrebbero entrare in conflitto con i collegamenti nativi.
- Risolto il problema di caricamento su Google Drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Migliorato per velocità, aggiungendo minLength a 50 per il rilevamento della lingua.
- Risolto il problema di validazione del token di Google Drive.

## 0.2.47

- Risolto problema api deepl

## 0.2.46

- risolto problema del blocco segna

## 0.2.45

- Risolto il problema di innerText dell'elemento non definito
- Risolto problema di lingua sorgente non definita nella traduzione di caiyun

## 0.2.44

- Risolto il problema di attivazione/disattivazione della maschera degli userscript
- Risolto la logica di attivazione/disattivazione della maschera

## 0.2.43

- Risolto il problema di attivazione/disattivazione della maschera degli userscript con evento touch.
- Migliorata la velocità (rimuovendo sleep(300))

## 0.2.42

- Risolto il problema di hover della maschera quando si attiva nuovamente la maschera.
- Aggiunti collegamenti rapidi per la maschera su mobile
- Risolto problema di sincronizzazione cloud degli userscript
- Spostata la pagina delle opzioni avanzate nel menu a sinistra.
- Aggiunta logica di riprova al servizio di traduzione

## 0.2.41

- Risolto problema di traduzione userscript niu
- Risolto problema di traduzione xhtml

## 0.2.40

- Risolto problema di visualizzazione della funzione beta
- Risolta la pagina delle impostazioni popup su nuova scheda
- Risolto problema di sostituzione del segnaposto di traduzione

## 0.2.39

- Supporto per collegamenti rapidi per mostrare la traduzione della maschera
- Supporto per abilitare la funzione beta nel pannello degli sviluppatori
- Risolti i collegamenti rapidi nell'estensione mobile## 0.2.38

- Supporto al caricamento del tema
- Correzione di getpocket.com
- Correzione del piè di pagina a parte per l'area del corpo
- Correzione dell'icona di importazione/esportazione

## 0.2.37

- Correzione del segno di esclusione del frame

## 0.2.36

- Supporto alla sincronizzazione con Google Drive

## 0.2.35

- Correzione dell'ignorare i tag giapponesi rb, rt.
- Miglioramenti per l'interfaccia utente popup
- Consigli migliori per gli utenti con script dannosi
- Aggiunta di un contributo alla pagina delle informazioni
- Correzione della traduzione automatica di Volc per il rilevamento automatico della lingua

## 0.2.34

- Correzione della velocità di traduzione multilingue

## 0.2.33

- Supporto alla modalità di scrittura verticale, come il giapponese.
- Aggiunta di 3 temi
- Aggiunto il servizio di traduzione Niu

## 0.2.32

- Correzione della traduzione di base dei PDF
- Correzione della selezione di un servizio non configurato nel popup, vai alla pagina delle opzioni.
- Correzione delle impostazioni rimanenti aperte.
- Correzione della velocità di rilevamento della lingua multilingue

## 0.2.31

- Correzione dell'iniezione dinamica del CSS in iframe

## 0.2.30

- Supporto alla traduzione inline di iframe in userscript.
- Supporto alla traduzione di shadowroot. Ad esempio:
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Area di conversazione.
- verifica anche la regola di sincronizzazione nel popup

## 0.2.29

- Correzione della traduzione di Facebook
- Supporto all'opzione del menu contestuale.

## 0.2.28

- Rimozione del match non standard per userscript

## 0.2.27

- Supporto alla traduzione inline di iframe. (Solo per estensione, non disponibile per
  userscript)
- Correzione della traduzione multilingue

## 0.2.26

- Correzione dell'addon di Firefox per Android
- Aggiunta di impostazioni avanzate per la traduzione di newline

## 0.2.25

- Supporto alla traduzione di iframe, come la mail di QQ, tweet incorporati.## 0.2.24

- Aggiungi temporaneamente il sito di traduzione per un po'
- Correggi l'API del browser degli userscript di stay.app
- Correggi la pagina delle opzioni di stay.app

## 0.2.23

- Correggi la traduzione di pagine in più lingue

## 0.2.22

- Correggi la compilazione degli userscript

## 0.2.21

- Correggi la traduzione online di pdf su Firefox

## 0.2.20

- Correggi il problema della richiesta di macaque
- Correggi l'altezza della linea di evidenziazione

## 0.2.19

- Correggi il giapponese intelligente di Tencent
- Correggi il browser del mondo di haikuo

## 0.2.18

- Correggi il cambio dell'URL del client, mantieni automaticamente lo stato di traduzione.
- Rimuovi il contenitore laterale come contenitore di traduzione.
- Rifattorizza la posizione del popup.

## 0.2.17

- Cambia evidenziazione in marca
- Aggiungi tema di traduzione evidenziato

## 0.2.16

- Compatibilità con macaque

## 0.2.15

- Correggi il problema del rimbalzo al tocco

## 0.2.14

- Correggi il non funzionamento di globalThis.GM su Safari

## 0.2.13

- Supporto per il trascinamento del Popup degli Userscript
- Supporto per l'attivazione della traduzione delle pagine con Tre Dita su dispositivi touch
- Supporto per nascondere l'icona del popup degli userscript.

## 0.2.12

- Miglioramenti per inoreader

## 0.2.11

- Correzione
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  L'archivio di Annas Il contenuto principale della pagina non poteva essere tradotto

## 0.2.10

- Correggi la distanza dell'altezza della linea in pdf

## 0.2.9

- Correggi l'esclusione degli elementi da marcare
- Correggi il controllo del tipo in deno
- Rimuovi importmap
- Correggi la traduzione dei menu contestuali
- Ripristina la pagina quando è abilitata l'opzione "mai tradurre questo sito"
- Aggiungi descrizione per aggiungere URL## 0.2.8

- Rileva la lingua dell'agente utente per la lingua dell'interfaccia
- Correggi il bug dell'interruzione di linea.

## 0.2.7

- Correggi la richiesta di Grease Monkey

## 0.2.6

- Correggi
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  problema di corrispondenza dell'URL del file

## 0.2.5

- Aumenta la versione per il test CI

## 0.2.4

- Interrompi l'errore di connessione del messaggio per il popup.

## 0.2.3

- Correggi
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  creazione del contesto più volte

## 0.2.2

- Correggi il file campione PDF
- Correggi il file locale PDF di Firefox
- Correggi le scorciatoie PDF

## 0.2.1

- Supporta il gestore delle scorciatoie di Grease Monkey.
- Correggi la regex di corrispondenza
- Correggi i commenti su YouTube.
- Correggi la versione mobile compatta di Reddit
- Correggi il problema della traduzione del testo completo

## 0.2.0

- Correggi il PDF a due colonne.
- Correggi il bug della versione di Chrome/Edge Store.
- Correggi
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Pubblica su addon di Firefox
- Pubblica su Edge
- correggi il margine del pdf.
- Cambia il file pdf campione

## 0.0.62

- Correggi il formato pdf, l'indentazione.
- Correggi telegra.ph per prevenire il cambio dell'elemento

## 0.0.61

- Correggi la chiusura dell'elemento span.
- Correggi il permesso per il browser iniziale

## 0.0.60

- Correggi il PDF di Chrome

## 0.0.59

- Supporto iniziale per PDF

## 0.0.58

- Modifica la descrizione del tema di traduzione

## 0.0.57

- Cambia l'UI del popup, per un uso più semplice## 0.0.56

- Risolto il timeout di Chrome
- Risolto l'errore di suddivisione delle frasi.

## 0.0.55

- Risolto il problema della visualizzazione di elementi nascosti.
- Rifattorizzazione della marcatura degli elementi

## 0.0.54

- Supporto all'interruzione di linea per X caratteri.

## 0.0.53

- Utilizzare sendMessage invece di connect, poiché Chrome disconnetterà la porta dopo
  5 minuti
- Migliorato il rilevamento dei contenitori di testo

## 0.0.52

- Non tradurre il paragrafo che contiene solo elementi segnaposto, per
  [esempio](https://github.com/nank1ro/solidart), la prima riga.
- Migliorato il rilevamento degli elementi figlio.

## 0.0.51

- Risolto problema di cache
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7)
- Risolto il problema della dimensione del font nell'UI delle opzioni

## 0.0.50

- Risolto il problema della traduzione delle immagini bloccate.

## 0.0.49

- Risolto il problema dell'estensione per Firefox

## 0.0.48

- Risolto il problema dell'estensione per Chrome

## 0.0.47

- Riscrittura del messaggio con background, utilizzare connect invece di sendMessage
- Aggiunto il supporto per Reddit mobile
- Risolto il problema dello spazio bianco preformattato per alcuni articoli

## 0.0.46

- Formattazione delle informazioni meta degli userscript

## 0.0.45

- Gli userscript utilizzano un unico file.
- Aggiunto un timeout per la richiesta della cache

## 0.0.44

- Risolto l'errore di suddivisione di Tencent.
- Risolto l'errore dell'elemento sup inline.
- Migliorato per Twitter

## 0.0.43

- Risolto l'errore di tweet br
- Risolto il problema della traduzione globale.

## 0.0.42

- Risolto il problema del tag BR
- Trattati i tag di blocco secondo le regole## 0.0.41

- Correzione del controllo degli elementi in linea
- Aggiunta dell'opzione di log di debug per sviluppatori

## 0.0.39

- Correzione del servizio di traduzione che contiene mock2

## 0.0.38

- Supporto alla memorizzazione nella cache del risultato per gli userscript
- Aggiunta dell'interfaccia utente delle opzioni
- Supporto al rilevamento di più contenitori di contenuto

## 0.0.37

- Correzione del cambio del servizio di traduzione popup che non funziona
- Correzione della traduzione del contenuto dei post su reddit mobile.

## 0.0.36

- Correzione dei caratteri speciali su Wikipedia
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Correzione della dimensione dell'icona degli userscript.
- Abilitazione del rilevamento della lingua del paragrafo su tutti i siti.

## 0.0.35

- Correzione del passaggio alla pagina successiva su YouTube
- Supporto alla pagina di ricerca di YouTube.
- Correzione dell'interruttore avanzato delle opzioni.
- Correzione del tag img, tag nascosto
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Correzione del refresh forzato di Google Search
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Supporto al risultato della tabella di Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Correzione della pagina bianca su Wikipedia
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Cambiamenti Importanti

- La scorciatoia predefinita per attivare la traduzione è stata cambiata in `alt+A`, perché
  è il tasto più comodo da digitare.

### Altri

- Supporto alla modalità di traduzione immediata, così puoi far tradurre la pagina web il più velocemente possibile.
- Supporto alla definizione dell'area della pagina che necessita di traduzione, così puoi tradurre più aree.
- Supporto alla definizione del conteggio dei primi x testi da tradurre immediatamente.
- Correzione della traduzione duplicata quando si cambia traduzione
- Miglioramento dell'interfaccia utente del popup## 0.0.33

- Supporto per più lingue, zh-TW, en

## 0.0.32

- Correzione della traduzione di file locali dopo il salvataggio. Corretto
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Aggiunto file js dist al repo pubblico

## 0.0.31

- Supporto per la traduzione dell'intera pagina
- Supporto per la traduzione immediata della pagina
- Più configurazioni UI
- Riflessione del tema
- Aggiunta di una nuova icona
- Aggiunto nuovo tema di traduzione dashedBorder

## 0.0.30

- Miglioramenti per il tema tratteggiato

## 0.0.29

- Correzione validità paragrafo.
- Aggiunti temi puntinato, thinDashed
- Miglioramenti per i temi tratteggiato, evidenziato

## 0.0.28

- Correzione del sottolineato
- Aggiunti temi tratteggiato, carta
- Correzione rilevamento intestazione

## 0.0.27

- Supporto per translationTheme

## 0.0.26

- Correzione del permesso di connessione dello script utente di volc alpha.
- Correzione della versione cliccabile.

## 0.0.25

- Supporto per selectorMatches, così possiamo abbinare tutti i manstondon ora.
- Correzione dell'errore dello script utente di Firefox.

## 0.0.23

- Miglioramenti per il rilevamento del cinese
- Correzione del problema di innerText su reddit

## 0.0.22

- Supporto per deeplx
- Correzione di molteplici traduzioni quando si cambia servizio

## 0.0.21

- Correzione di alcuni tag span che sono elementi blocco

## 0.0.20

- Supporto per non tradurre hashtag come #hash, tag at come @xxx, $tag, come $APPL
- Supporto per l'elemento blocco

## 0.0.18

- Supporto per deepl, bing, baidu, youdao, volc, openl, caiyun.

## 0.0.13

- Supporto per userscript## 0.0.4.8

- Correzione dell'ordine del codice.
- Supporto per l'interfaccia utente popup di base

## 0.0.4.6

- Supporto per il controllo della nuova versione

## 0.0.3

- Supporto per i file locali

## 0.0.2

- Supporto per Elementi Dinamici
- Supporto per la traduzione visibile
