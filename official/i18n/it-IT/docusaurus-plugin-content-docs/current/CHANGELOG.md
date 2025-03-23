---
sidebar_position: 6
---

# Registro delle Modifiche

Questo registro delle modifiche viene aggiornato in base al progresso dello sviluppo. La data dopo la versione è la data di fusione del codice, non la data di release negli app store (il tempo di revisione varia dopo la sottomissione a ciascun app store, con alcuni che impiegano fino a una settimana per la revisione). Attualmente, stiamo avanzando con due versioni.

La **Release version** è la versione stabile ufficiale, disponibile nei principali app store come [Chrome](https://chromewebstore.google.com/detail/bpoadfkcbjbfhfodiogcnhhhpibjhbnh), [Edge](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg), [Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate/), [Apple](https://apps.apple.com/app/id6447957425), ecc.

La **Preview version** viene pubblicata più frequentemente e include alcune funzionalità sperimentali. Rispetto alla Release version, può contenere più bug. Viene principalmente rilasciata su

- [userscript del sito ufficiale](https://download.immersivetranslate.com/immersive-translate.user.js)
- [versione beta nel Firefox store](https://addons.mozilla.org/firefox/addon/immersive-translate-beta/)
- [Github Release Assets](https://github.com/immersive-translate/immersive-translate/releases)

## 1.15.9 Release (2025-03-23)

- Risolto: Un problema in cui la traduzione non funzionava in Safari 16.4.

## 1.15.8 Release (2025-03-20)

- Risolto: Un problema in cui il tasto di scelta rapida per la traduzione al passaggio del mouse non funzionava su dispositivi che supportano sia il mouse che il touch.
- Aggiunto: Supporto per la traduzione del grande modello Youdao Ziyue.

## 1.15.7 Release (2025-03-19)

- Aggiunto: Pre-traduzione dinamica del contenuto da tradurre durante la navigazione delle pagine.
- Risolto: Un problema in cui il servizio di traduzione AI emetteva erroneamente cinese semplificato quando traduceva cinese tradizionale.
- Risolto: Un problema con la traduzione al passaggio del mouse che non funzionava in modalità "Prima la traduzione, segue il testo originale".
- Risolto: Problemi di compatibilità con la modalità "Solo traduzione" quando utilizzata con plugin di lettura come Reader View.
- Ottimizzato: Migliorata la qualità del servizio di traduzione AI per il contenuto principale.
- Ottimizzato: Migliorato il supporto per la traduzione delle immagini su alcuni siti web.
- Ottimizzato: Ottimizzata la formattazione del testo misto cinese e inglese.
- Ottimizzato: Il servizio di traduzione Gemini supporta il prompt di sistema personalizzato (System Prompt).
- Ottimizzato: Migliorata la velocità dello userscript.

## 1.15.2 Release (2025-03-02)

- Aggiunto: Gemini supporta il portoghese (Brasile).
- Aggiunto: Servizio di traduzione Grok, Ollama, Groq, Azure-OpenAI.
- Risolto: Problema di traduzione dei sottotitoli in Google Meet e Microsoft Teams.
- Risolto: Problema di traduzione di Google con caratteri di escape.
- Ottimizzato: Migliorata l'accuratezza dell'identificazione automatica della lingua del contenuto tradotto.
- Ottimizzato: [Traduzione gratuita delle immagini] supporta la formattazione per le lingue da destra a sinistra.
- Ottimizzato: Compatibile con modelli come o1, o3 che non supportano il ruolo di sistema (il parametro del ruolo di sistema non verrà passato quando la configurazione del System Prompt è vuota).

## 1.14.16 Release (2025-02-21)

- Aggiunto: Deepseek, Gemini, Claude supportano il cambio di contesto.
- Risolto: L'aggiornamento dei termini non invia una nuova richiesta di traduzione.
- Migliorato: La lingua dell'interfaccia aggiunge l'ungherese.
- Migliorato: Qualità della traduzione di Google.
- Migliorato: Formattazione delle immagini gratuite.

## 1.14.12 Release (2025-02-19)

- Migliorato: La pausa della traduzione cancella immediatamente la coda delle richieste.
- Migliorato: Filtra il testo sporco nel servizio di traduzione deepl.
- Risolto: Traduzione della barra laterale non valida nelle impostazioni avanzate.
- Risolto: Problema di visualizzazione della traduzione personalizzata deepseek.

## 1.14.11 Release (2025-02-18)

- Risolto: Errore `401: Authentication Fails` della chiave API personalizzata di DeepSeek.

## 1.14.10 Release (2025-02-17)

- Nuovo: L'abbonamento Pro supporta il servizio di traduzione DeepSeek (v3).
- Risolto: Risolto il problema del file di configurazione utente che superava il limite di dimensione.
- Migliorato: L'elemento del menu contestuale può essere chiuso (operato nelle impostazioni avanzate).
- Migliorato: Migliorate le capacità di riconoscimento della lingua per Greasemonkey e Safari su pagine con lingue minori.
- Migliorato: Accesso all'interfaccia del servizio di test della pagina delle impostazioni online.
- Migliorato: Migliorata l'esperienza utente della funzione di anteprima del confronto del contesto.
- Migliorato: Logica di giudizio della modalità touch e mouse.

## 1.14.8 Release (2025-02-10)

- Risolto: Problema in cui i file lunghi PDF-Pro non venivano tradotti automaticamente.
- Migliorato: Microsoft, Google e Tencent ora supportano il cantonese.
- Migliorato: La BBC ora supporta i sottotitoli.

## 1.14.6 Preview (2025-02-08)

- Risolto: Problema in cui la **Mouse Hover Translation** non poteva tradurre il testo ricco.
- Migliorato: La versione Tampermonkey ora supporta la traduzione dei sottotitoli di YouTube.

## 1.14.4 Release (2025-02-07)

- Risolto: Problema con il rilevamento errato della lingua nella **Enhanced Input Box**.
- Risolto: Problema di abbinamento intelligente degli esperti AI nei servizi di traduzione personalizzati.
- Risolto: Problema di sincronizzazione di Google Drive su alcuni browser.
- Risolto: Problema di traduzione dei commenti live di YouTube.
- Risolto: Problema di sovrapposizione dei sottotitoli in alcuni video di YouTube.
- Migliorato: Fallimento nella traduzione dei manga su siti come shonenjumpplus nel browser Safari.

## 1.13.8 Release (2025-01-24)

- Nuovo: La traduzione gratuita delle immagini è ora disponibile (attualmente supportata solo sulle versioni PC dei browser Chrome e Edge), accessibile tramite il menu contestuale.
- Risolto: Risolto un problema in cui alcuni contenuti venivano persi durante la traduzione multi-segmento in Gemini.
- Ottimizzato: Migliorato il caricamento dei sottotitoli di YouTube.
- Nuovo: Il servizio di traduzione AI ora supporta il norvegese.

## 1.13.6 Preview (2025-01-17)

- Migliorato: **AI Expert** può essere utilizzato con **AI Context-Aware Translation**.
- Migliorato: **Image Translation** è ora compatibile con weibo.com (supportato solo su Chrome e Edge).
- Migliorato: Quando la lingua dell'interfaccia è impostata su inglese, la lingua di destinazione predefinita per la **Enhanced Input Box** è cambiata in cinese.
- Migliorato: Aggiunta una voce di revisione del negozio nelle opzioni **More** sul pannello.

## 1.13.5 Release (2025-01-14)

- Migliorato: Compatibile con il modello di pensiero Gemini 2.0.
- Migliorato: Supporta lo stile grassetto in modalità solo traduzione.

## 1.13.4 Preview (2025-01-13)

- Aggiunto: I membri Pro possono ora utilizzare direttamente il modello **Zhipu 4 Plus**.
- Migliorato: Traduzione Gemini.

## 1.13.1 (2025-01-10)

- Aggiunto: Quando il testo tradotto e il testo originale appartengono allo stesso sistema di scrittura, visualizza la traduzione utilizzando uno stile specializzato.
- Risolto: Il problema in cui **Mouse Hover Translation** non funziona su alcuni siti web.
- Migliorato: DeepLx ora supporta l'arabo.
- Migliorato: Migliorato il riconoscimento della lingua originale. In precedenza, le pagine contenenti più lingue potevano non essere tradotte, ma ora vengono tradotte correttamente.
- Migliorato: Per Twitter, le traduzioni di contenuti multilinea sono impostate per non andare a capo per impostazione predefinita. Il ritorno a capo avverrà solo quando il contenuto supera le 10 righe o i 1000 caratteri. Il ritorno a capo può essere abilitato tramite le impostazioni **Advanced Settings** -> **Enable automatic line wrapping for long paragraphs**.

## 1.12.8 (2025-01-03)

- Risolto: il problema in cui la pagina delle impostazioni di iOS 18.3 non può essere visualizzata correttamente.
- Risolto: la mancanza di righe vuote durante la traduzione dei tweet.
- Risolto: il problema dei numeri decimali che vengono forzatamente spezzati quando si traducono testi lunghi.

## 1.12.7 Release (2024-12-30)

- Migliorato: Bing/Google ora supportano il portoghese (Brasile).
- Migliorato: Migliorate le descrizioni per la lingua dell'interfaccia utente in cinese tradizionale.
- Migliorato: Regolazione del layout per le lingue da destra a sinistra nei pannelli e nelle pagine delle impostazioni.

## 1.12.6 (2024-12-26)

- Risolto: Problema in cui la funzione di passaggio del mouse carica il servizio di traduzione sbagliato in determinate condizioni.
- Risolto: Problema in cui l'abilitazione temporanea dei sottotitoli bilingue su YouTube non funziona.
- Risolto: Dopo aver cambiato i servizi di traduzione, il servizio di traduzione in "**Enhanced Input Box**" non si aggiorna.
- Risolto: L'interruttore "**YouTube Enable Bilingual**" nella pagina delle impostazioni non funziona.
- Migliorato: Rimosso il modello deprecato gemini-1.0-pro.

## 1.12.4 (2024-12-13)

- Aggiunto: **AI Context-Aware Translation** può migliorare l'accuratezza della traduzione di contenuti professionali. (Disponibile solo per i membri Pro, supportato esclusivamente dai modelli OpenAI) **Options** -> **Grneral** -> **Enable AI Context-Aware Translation**
- Risolto: Alcuni bug nell'effetto di traduzione multi-linea su Twitter.
- Risolto: Problemi con la traduzione di alcune formule a causa del testo ricco.
- Migliorato: Quando si traduce su **x.com**, i video con sottotitoli avranno automaticamente i sottotitoli bilingue tradotti.
- Migliorato: I video senza sottotitoli mostreranno un'icona di traduzione e forniranno una ragione per cui la traduzione non è possibile.

## 1.11.7 (2024-11-25)

- Aggiunto: Bing/Google ora supportano il khmer (cambogiano).
- Aggiunto: Consenti ai file ePub incompleti di continuare la traduzione da dove erano stati interrotti al momento della reimportazione.
- Risolto: Problema con la traduzione delle immagini di Twitter nel browser Safari.
- Risolto: I tasti di scelta rapida diventano inefficaci quando si attiva o disattiva la funzione "**Hover Translation**".
- Migliorato: Migliorata la visualizzazione della traduzione bilingue multilinea su Twitter e YouTube.
- Migliorato: La traduzione del testo ricco è disattivata per impostazione predefinita in modalità bilingue per migliorare la qualità della traduzione.
- ~~Migliorato: Aggiunta l'opzione per personalizzare la "**Enable Sidebar & Navbar Translation**" in "**Advanced Settings**".~~
- Migliorato: Le immagini non vengono più tradotte in modalità "**Hover - immediately translate this paragraph**".

## 1.11.4 (2024-11-16)

- Risolto: Problema con la traduzione delle formule causato dal "Twitter Translation Improvement" nella versione 1.11.2.

## 1.11.2 (2024-11-13)

- Risolto: Problema in cui il contenuto scompare dopo aver cliccato su "vedi di più" in modalità solo traduzione di Facebook.
- ~~Migliorato: Migliorata la visualizzazione delle traduzioni bilingue multilinea su Twitter.~~
- Migliorato: Aggiornata l'interfaccia utente dell'elenco a discesa del servizio di traduzione nel pannello.

## 1.11.1 (2024-11-05)

- Aggiunto: La traduzione dei **Sottotitoli in tempo reale** ora supporta l'attivazione tramite "float ball", disponibile su Zoom, Google Meet e Microsoft Teams.
- Risolto: Problemi di sincronizzazione dei sottotitoli su YouTube dopo la visione di annunci.
- Risolto: Problemi di visualizzazione con il menu di traduzione del tasto destro in Safari su MacOS 15.
- Risolto: Problemi con la funzionalità di annullamento Ctrl+Z nell'**Enhanced input** su alcuni siti web.

## 1.10.6 (2024-10-25)

- Risolto: Problema con i tasti di scelta rapida di **Enhanced input** che non si attivavano
- Migliorato: Riduzione delle dimensioni del pacchetto di installazione
- Migliorato: Soluzione per la visualizzazione dei sottotitoli su Netflix

## 1.10.5 (2024-10-23)

- Aggiunto: Visualizzazione di un avviso quando la lingua di origine e la lingua di destinazione sono le stesse
- Risolto: Problema di traduzione dei caratteri di spazio nel testo ricco [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- Migliorato: Miglioramento dell'input e della funzionalità di passaggio del mouse all'interno di iframe incorporati sulle pagine web

## 1.10.2 (2024-10-11)

- Aggiunto: Traduzione delle immagini (versione Beta)
- Aggiunto: Modalità Forza Abilita Supporto Mouse (Abilita questa funzione solo se la funzione di passaggio del mouse non è disponibile su dispositivi tablet) **Impostazioni** -> **Impostazioni Avanzate** -> **Forza Abilita Supporto Mouse**
- Aggiunto: Visualizzazione del messaggio di errore quando la traduzione dei sottotitoli video fallisce
- Risolto: Problema di traduzione del testo ricco [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163)
- Migliorato: Risolti problemi in cui il pulsante di traduzione potrebbe non funzionare durante la traduzione di PDF
- Migliorato: Migliorato il rendering delle formule tradotte
- Migliorato: Lista di selezione delle lingue

## 1.9.8 (2024-09-28)

- Aggiunto: Servizio di traduzione "Zhipu BigModel"
- Rimosso: Modello "SiliconCloud" qwen1.5-7B-chat (a causa della dismissione ufficiale)
- Risolto: Risolto problema di compatibilità di accesso con il plugin Safari su macOS 15

## 1.9.7 (2024-09-20)

- Supporto per l'input migliorato per Baidu, Gmail e altri campi di input
- Supporto per l'intestazione della richiesta anthropic-dangerous-direct-browser-access per l'API Claude Anthropic
- Supporto per il download di sottotitoli da video Hulu, Bloomberg e Domestika
- DeepX supporta la traduzione di testo ricco
- Risolto il problema con gli esperti AI personalizzati che non si sincronizzavano

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) supporta la copia delle formule (clic destro sulla formula per vedere il menu di copia)
- Risolto il problema della visualizzazione dei sottotitoli bilingue per più video sulla stessa pagina di Twitter
- Risolti alcuni bug

## 1.9.3 (2024-09-05)

- L'opzione per la visualizzazione solo traduzione/confronto bilingue è stata spostata nelle impostazioni generali.
- Per impostazione predefinita, il sistema ricorderà la modalità attivata cliccando sull'icona nel pannello per la visualizzazione solo traduzione o confronto bilingue. Per passare temporaneamente, clicca su "Altro" -> "Passa alla visualizzazione solo traduzione" nel pannello.
- Per impostazione predefinita, la traduzione dal cinese semplificato al cinese tradizionale e viceversa utilizzerà la modalità solo traduzione, piuttosto che la modalità di confronto bilingue.
- Risolti alcuni bug.

## 1.9.1 (2024-09-03)

- Supporto per configurare eccezioni per lingue e siti web in modalità di contrasto bilingue o solo traduzione (configura nella pagina Impostazioni -> Impostazioni Avanzate). Ad esempio: Se la tua modalità di traduzione predefinita è il contrasto bilingue, ma non desideri che il cinese tradizionale utilizzi anche il contrasto bilingue, puoi aggiungere il cinese tradizionale alle lingue di eccezione per il contrasto bilingue, in modo che il cinese tradizionale utilizzi la modalità solo traduzione per la traduzione. Allo stesso modo, se la tua modalità di traduzione predefinita è solo traduzione, ma desideri che una certa lingua o sito web utilizzi la modalità di contrasto bilingue, puoi anche aggiungere quella lingua o sito web alle lingue di eccezione.
- Risolto un problema in cui la casella di input nell'interfaccia dei messaggi privati di Tiktok veniva tradotta in modo errato
- Risolto un problema in cui i fumetti su Read Comic Online non potevano essere tradotti
- Risolto un problema in cui le [Impostazioni Avanzate -> Numero minimo di caratteri richiesti per tradurre un paragrafo] non avevano effetto in alcuni casi

## 1.8.4 (2024-08-30)

- Il servizio di traduzione DeepL ora supporta ufficialmente il cinese tradizionale come lingua di destinazione (in precedenza, la traduzione in cinese tradizionale con DeepL comportava un processo di conversione aggiuntivo da cinese semplificato a cinese tradizionale).
- Ottimizzata la performance della traduzione di testo ricco.

## 1.8.3

- Google Meet ora supporta i sottotitoli bilingue per le riunioni dal vivo: Ora puoi goderti la funzione di sottotitoli bilingue nelle riunioni di Google Meet. Basta aprire il link della riunione, attivare i sottotitoli bilingue nel pannello di traduzione immersiva e poi aggiornare la pagina per sperimentarlo.
- Aggiunta l'opzione per "Segnalare problemi di traduzione della pagina corrente" e l'opzione per "Accendere/spegnere rapidamente il float ball" nelle opzioni più del pannello.
- Dopo aver regolato la posizione dei sottotitoli bilingue di YouTube, il sistema ricorderà automaticamente la nuova posizione.
- Ottimizzata la logica della cache del plugin, ora cancellando automaticamente i dati della cache che hanno più di 30 giorni.
- Ottimizzati i blocchi di codice all'interno dei paragrafi per un ripristino più accurato del testo originale.
- Migliorata la gestione delle "parole non traducibili" nelle impostazioni avanzate.

## 1.8.2

- Ora puoi tradurre il testo nelle caselle di input con il clic destro: Seleziona qualsiasi testo in una casella di input su una pagina web, fai clic destro per scegliere traduci, e la traduzione immersiva tradurrà automaticamente il testo selezionato nella lingua di destinazione della casella di input, rendendo conveniente tradurre rapidamente il testo in lingua nativa nelle caselle di input in altre lingue.
- Ora puoi segnalare rapidamente problemi di traduzione delle pagine web nel float ball della traduzione immersiva. Dopo aver tradotto una pagina web, se ci sono problemi, puoi cliccare sul pulsante [Feedback] sul lato destro del float ball, compilare la descrizione del problema, e ce ne occuperemo il prima possibile.
- I file Epub ora supportano la traduzione di testo ricco (cioè, preservando il formato del testo originale di ogni paragrafo, come link, grassetto, ecc.)
- Supporto per sottotitoli bilingue in tempo reale nelle riunioni video della versione web di Microsoft Teams (Apri il link della riunione di Teams, attiva i sottotitoli bilingue nel pannello di traduzione immersiva e poi aggiorna)
- Ottimizzati i sottotitoli bilingue per la versione inglese di iQIYI (iq.com)
- Forniti più articoli arXiv con layout di traduzione bilingue ottimizzato
- A causa delle restrizioni del sito web di Youtube, lo script di Tampermonkey per Chrome non supporta più i sottotitoli bilingue di Youtube. Si prega di utilizzare la [versione del plugin](https://immersivetranslate.com/).

## 1.8.1

- Risolti problemi di traduzione con lo script Tampermonkey SiliconCloud
- La traduzione Claude ora supporta il tibetano e consente la configurazione del parametro Temperature
- La pagina dei dettagli dell'esperto AI visualizza i prompt utilizzati dall'esperto
- Le impostazioni dei tasti di scelta rapida ora consentono di assegnare tasti di scelta rapida unici per qualsiasi servizio di traduzione
- Ottimizzato il rilevamento delle traduzioni degli articoli arXiv

## 1.7.9

- Risolti problemi con la traduzione di testo ricco per servizi di traduzione come Google, DeepL (ad esempio, pagine che visualizzano direttamente `<button>` ecc.)
- Risolto il problema in cui il collegamento bilingue per i video di YouTube non poteva essere disattivato.

## 1.7.8

- DeepL, Microsoft Translate, Google Translate, OpenAI, Claude, Gemini e altri servizi di traduzione supportano la traduzione per mantenere il formato del testo originale (ad esempio, link, grassetto, ecc.)
- Dopo aver selezionato il testo, il menu del tasto destro cambierà in [Traduci il testo], cliccando sul quale puoi saltare automaticamente alla pagina di traduzione del testo di Immersive Translation
- Nuovo servizio di traduzione gratuito per grandi modelli: SiliconCloud, disponibile per tutti gli utenti.
- Aggiunto il modello di traduzione Zero-One-Thing, che può essere utilizzato compilando l'API Key dopo la registrazione sulla piattaforma Zero-One-Thing.
- Nuovo pulsante di feedback utente per la traduzione di manga (dopo aver tradotto un manga, clicca sul pulsante [Feedback] sul lato destro del float ball per dare feedback sulla qualità della traduzione).

## 1.7.7

- Adottato algoritmo di suddivisione intelligente delle frasi per i sottotitoli generati automaticamente in inglese su YouTube [Pro Disponibile]
- Ottimizza la traduzione con il tasto destro in "Traduci in xx lingua di destinazione"
- Supporto per l'integrazione immersiva [JS SDK](https://immersivetranslate.com/docs/js-sdk/) per siti web di terze parti
- Ottimizza la visualizzazione dei sottotitoli su Hulu
- Supporto per la traduzione dei sottotitoli delle riunioni nella versione web di ZOOM

## 1.7.6

- Supporto per la personalizzazione degli esperti AI, l'ingresso è in fondo alla pagina [Impostazioni]->[Esperto AI].
- Ottimizza il caricamento dei sottotitoli sul sito TED
- Il portoghese (Brasile) è supportato come lingua del plugin.
- Siti supportati per la traduzione di fumetti
  - [Antbyw](https://www.antbyw.com)
  - [Zerobywzz](https://www.zerobywzz.com)
  - [动漫之家](https://www.idmzj.com)
  - [Jmanga](https://jmanga.org)

## 1.7.5

- Abilitata la copia dei sottotitoli di YouTube
- Ottimizzata la visualizzazione dei sottotitoli su alcuni siti video
- Migliorata la velocità di traduzione dei manga

## 1.7.2

- Risolto il fallimento della traduzione dei fumetti nel browser Firefox.

## 1.7.1

- Migliorata la velocità di traduzione per le traduzioni di fumetti
- Aggiunto supporto per nuovi siti nelle traduzioni di fumetti:
  - [ShonenJumpPlus](https://shonenjumpplus.com)
  - [Heros Web](https://viewer.heros-web.com/)
  - [Comic Days](https://comic-days.com/)
  - [ComicWalker](https://comic-walker.com/)
  - [Web Ace](https://web-ace.jp/)

## 1.6.6

- Aggiunto supporto per nuovi siti per la traduzione di fumetti:
  - [Mangabuddy](https://mangabuddy.com/)
  - [Hitomi](https://hitomi.la)
  - [Yamibo](https://www.yamibo.com)
  - [Copymanga](https://www.copymanga.site/)
- I sottotitoli bilingue di YouTube ora supportano la suddivisione intelligente delle frasi (Beta) (Solo quando si abilita manualmente la traduzione immersiva dei sottotitoli di YouTube in [Impostazioni] - [Sottotitoli Video], e i sottotitoli originali del video sono sottotitoli generati automaticamente in inglese)
- Aggiunto servizio di traduzione Tencent [【Hunyuan Large Model】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- Risolvi i problemi di layout del testo delle traduzioni di fumetti per le lingue nel script latino.
- Nuovi siti supportati per la traduzione di fumetti:
  - COMIC FUZCOMICFUZ(https://comic-fuz.com/)
  - MangaDexMangaDex(https://mangadex.org/)
  - KuaiKan ComicsKuaiKanComics(https://www.kuaikanmanhua.com/)
- Risolto un problema in cui i servizi AI personalizzati non potevano selezionare esperti AI.

## 1.6.4

- Quando vengono utilizzati esperti AI per la "Selezione Intelligente", diversi esperti AI possono essere personalizzati per diversi siti web. Questo può essere impostato in [Impostazioni] -> [Esperti AI] -> [Inserisci qualsiasi esperto].
- Risolto il problema per cui i sottotitoli non venivano visualizzati su YouTube in modalità "Solo Traduzione".
- Risolto il problema dei sottotitoli bilingue che non funzionavano su Mubi.
- Compatibile con i PDF aperti con il plugin Adobe Acrobat.
- Tutti gli utenti possono [contribuire online](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/) alla traduzione multilingue dell'interfaccia di traduzione immersiva.

## 1.6.3

- Nuova funzionalità: traduzione Manga (Beta), nei siti web di manga supportati, un pulsante di traduzione manga apparirà sotto la sfera flottante di traduzione rapida della pagina web. Cliccandolo si attiverà la traduzione manga. Questa funzione è disponibile per i membri Pro (500 pagine al mese, pacchetti aggiuntivi possono essere acquistati), attualmente supporta i seguenti siti:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)

## 1.6.2

- Nuova funzionalità: traduzione Manga (Beta), nei siti web di manga supportati, un pulsante di traduzione manga apparirà sotto la sfera flottante di traduzione rapida della pagina web. Cliccandolo si attiverà la traduzione manga. Questa funzione è disponibile per i membri Pro (500 pagine al mese, pacchetti aggiuntivi possono essere acquistati), attualmente supporta i seguenti siti:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- Nuova funzionalità: la traduzione AI supporta il [modello grande Doubao](https://www.volcengine.com/product/doubao)
- Nuova funzionalità: supporto per la modalità di confronto bilingue con traduzione prima e testo originale a seguire, che può essere abilitata nella pagina delle impostazioni -> impostazioni avanzate.
- La lista dei modelli AI personalizzati supporta la sintassi `-all`, che può eliminare tutti i modelli preimpostati.
- Nei sottotitoli video bilingue, quando la lingua di destinazione è il cinese semplificato e il testo originale è in cinese tradizionale, il testo originale verrà automaticamente convertito in cinese semplificato, e viceversa.
- Risolto il problema per cui la scorciatoia della sfera flottante non poteva tradurre sotto iOS 18.
- Risolto il problema per cui i Prompts personalizzati erano inefficaci quando ne venivano utilizzati troppi.

## 1.6.1

- Supporta la piattaforma di modelli grandi Baidu Qianfan, la piattaforma di modelli grandi Alibaba Bailian, la piattaforma di modelli grandi DeepSeek.
- Risolto il problema per cui la modifica della lingua di destinazione e altre impostazioni nel pannello popup si resettava al cliccare sulla sfera flottante di traduzione.

## 1.5.8

- Gli esperti AI supportano la modalità "Selezione Intelligente", in cui il sistema selezionerà automaticamente l'esperto AI più adatto in base al sito web corrente (ad esempio, esperti AI legati alla tecnologia verranno selezionati automaticamente per The Verge e Hacker News, mentre il miglioramento della traduzione di Twitter verrà selezionato automaticamente per Twitter).

## 1.5.7

- Supporto per l'aggiunta di servizi di traduzione AI personalizzati compatibili con OpenAI, accessibili in fondo alla pagina [Impostazioni]->[Servizi di Traduzione].
- Risolto un problema per cui i sottotitoli bilingue non funzionavano sulla piattaforma video Domestika in Safari.

## 1.5.6

- Ottimizzato significativamente le prestazioni della traduzione di grandi pagine web, creazione di ePub e file di sottotitoli.
- Risolto il bug della sincronizzazione multi-dispositivo in Pro.

## 1.5.4

- I membri Pro supportano i servizi di traduzione Claude e Gemini (Beta)
- I sottotitoli bilingue di YouTube supportano le impostazioni di font e peso del font
- Risolti problemi di confine delle parole quando si avvolgono lunghi paragrafi [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- Risolto il riconoscimento delle lingue giapponese e coreana
- Risolto il problema per cui le pagine di Reddit su dispositivi mobili non venivano tradotte durante lo scorrimento
- Risolto il problema di alcune pagine mancanti di traduzioni con DeepL
- Risolto il problema di sincronizzazione del tempo multi-dispositivo per gli utenti Pro
- Ottimizzato i problemi di copertura delle impostazioni di sincronizzazione cloud
- Ottimizzato le parole di prompt per i servizi di traduzione AI

## 1.5.2

- Risolto il problema per cui le modifiche al prompt dell'esperto generale sovrascrivevano il prompt dell'esperto AI specificato [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- Il nome del modello AI personalizzato supporta la sintassi avanzata, usa + per aggiungere un modello, usa - per nascondere un modello e usa model_name=display_name per personalizzare il nome visualizzato del modello, ad esempio: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- Risolto l'errore restituito da Gemini
- Nascondi la sfera flottante quando si stampa la pagina
- Risolto il problema per cui la dimensione del font non si ridimensionava proporzionalmente quando YouTube era a schermo intero [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- Supporto per i servizi di traduzione AI per impostare [Esperto AI] per specificare la strategia di traduzione, attualmente una funzione Beta, che può essere abilitata in [Impostazioni Sviluppatore](https://dash.immersivetranslate.com/#developer) dopo aver abilitato Beta, e il menu [Esperto AI] può essere visto dopo il refresh.
- I servizi di traduzione AI possono ora personalizzare la lista dei modelli, come [OpenAI], il sistema ha solo alcuni dei modelli più comunemente usati integrati. Cliccando sulla lista a discesa dei modelli, l'ultimo elemento che vedi è [Imposta Più Modelli], dopo l'impostazione, verrà automaticamente ricordato per la comodità degli utenti che testano diversi modelli personalizzati.
- Ottimizzata l'incoerenza nel layout delle traduzioni in alcuni casi.
- Aggiunto un pulsante di reset per lo stile dei sottotitoli di YouTube, che può rapidamente ripristinare lo stile predefinito.
- Risolto il problema per cui i sottotitoli cinesi non potevano essere scaricati su YouTube.
- Ottimizzata la copia dell'interfaccia in cinese tradizionale.

## 1.4.12

- Risolto il problema della finestra di dialogo dei messaggi non tradotta quando si apriva la pagina di Reddit
- Aggiunta una funzione temporanea per abilitare la modifica della traduzione nella voce "Altro" del pannello
- Risolto il problema per cui YouTube Shorts senza sottotitoli visualizzava sempre i sottotitoli del video precedente [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- Risolto il problema per cui i sottotitoli bilingue di YouTube non potevano essere regolati su e giù a schermo intero [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- Supporto per i sottotitoli bilingue di [VK Video](https://vk.com/video)
- Supporto per impostazioni di attivazione indipendenti per i sottotitoli bilingue dei video di YouTube (abilitato per impostazione predefinita per i nuovi utenti)
- Ottimizzati i messaggi di errore per la traduzione di sottotitoli bilingue locali

## 1.4.11

- Compatibile con la traduzione della casella di input della pagina Bing Copilot
- Il controllo dello stile dei sottotitoli di YouTube supporta lo stile del bordo
- Supporto per la selezione del servizio di traduzione predefinito nella pagina Impostazioni -> Servizio di Traduzione
- Risolto il problema di sostituzione del placeholder di OpenAI SystemPrompt
- Risolto il problema di fusione delle regole utente personalizzate
- Risolto il problema di visualizzazione anomala dei sottotitoli per alcuni video di Netflix [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- Risolto il problema per cui i frequenti cambiamenti di colore della traduzione tramite la tavolozza dei colori erano inefficaci [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- I servizi di traduzione sono ora distintamente organizzati sotto una scheda separata, permettendo una panoramica completa di tutti i servizi di traduzione disponibili. Inoltre, gli utenti hanno la flessibilità di personalizzare quali servizi di traduzione vengono visualizzati. Per impostazione predefinita, viene mostrata solo una selezione limitata di servizi di traduzione, ma gli utenti possono personalizzare le loro preferenze di visualizzazione nella sezione [Più Servizi](https://dash.immersivetranslate.com/#services).
- La pagina delle impostazioni ora accoglie regolazioni agli [stili dei sottotitoli di YouTube](https://dash.immersivetranslate.com/#subtitle).
- Sono stati apportati miglioramenti per affrontare il problema per cui i sottotitoli bilingue immersivi non venivano visualizzati quando gli utenti impostavano la lingua dei sottotitoli su cinese sul sito web di YouTube.
- È stata introdotta una nuova scorciatoia per la traduzione temporanea chiamata Claude, che può essere configurata nella [pagina delle Impostazioni delle Scorciatoie](https://dash.immersivetranslate.com/#shortcuts).

## 1.4.8

- Ottimizza le prestazioni di traduzione per file di grandi dimensioni in PDF-Pro
- Migliora le prestazioni di traduzione per pagine di contenuti lunghi
- Implementa il supporto all'internazionalizzazione (i18n) per la navigazione dei documenti di pagina
- YouTube introduce una funzione per abilitare temporaneamente i sottotitoli bilingue
- YouTube supporta il download di sottotitoli bilingue (solo per i membri)
- Mobile aggiunge il controllo dei gesti, migliorando l'input tramite [impostazioni delle scorciatoie](https://dash.immersivetranslate.com/#shortcuts)
- Supporto per la traduzione bilingue per Google Docs

## 1.4.7

- Risolto il problema per cui la traduzione falliva quando si cambiavano le parole prompt personalizzate di OpenAI sotto il pulsante di test
- Risolto il problema dell'icona di scorciatoia dei sottotitoli di YouTube non visualizzata
- Ottimizzato il riconoscimento della lingua dell'estensione

## 1.4.6

- Risolto il problema per cui le parole prompt definite dall'utente erano inefficaci
- Aggiunte opzioni 50%, 150% per la dimensione del font dei sottotitoli di YouTube

## 1.4.5

- Risolto il problema per cui le modifiche agli stili dei sottotitoli di YouTube non venivano salvate
- Risolto il problema della scomparsa dei sottotitoli a schermo intero su iOS Safari
- Ulteriormente ottimizzata la velocità di traduzione dei sottotitoli di YouTube
- Le opzioni aggiuntive del pannello ora supportano [l'ingresso di traduzione del testo](https://app.immersivetranslate.com/text/)

## 1.4.2

- Supporto per il servizio di traduzione Claude
- Ottimizzati i multi-prompt di OpenAI, supportando il formato YAML, che migliora la flessibilità e la facilità d'uso della configurazione
- Ottimizzata significativamente la velocità di traduzione dei sottotitoli di YouTube, e aggiunto supporto per il passaggio tra ordine cinese e inglese, personalizzazione del colore e della dimensione del font, ecc.
- La piattaforma di sottotitoli video supporta [University of Southampton](https://southampton.cloud.panopto.eu)
- I sottotitoli bilingue di Udemy sono compatibili con la visualizzazione mobile
- Il servizio di traduzione Gemini è nascosto per impostazione predefinita, può essere abilitato nelle impostazioni sviluppatore per mostrare la beta di questo servizio di traduzione

## 1.3.4

- Supporto per il servizio di traduzione gratuito Yandex
- Ottimizzati i prompt di Gemini
- I sottotitoli video supportano l'impostazione per la visualizzazione bilingue/originale e traduzione
- Supporto per lo spazio tra cinese e inglese nei risultati di traduzione OpenAI
- Interruttore del pannello per visualizzare solo il pulsante di traduzione modificato per avere effetto solo sulla pagina corrente

## 1.3.3

- Ottimizzato il problema di visualizzazione della traduzione dei sottotitoli video di Twitter CC.
- Il servizio DeepL ha aggiunto il supporto per l'arabo.
- Il servizio di traduzione Colorful Clouds ora supporta coreano, spagnolo, francese e russo.
- Il servizio OpenAI ha aggiunto il supporto per il dialetto cinese nordorientale.
- Il rilevamento automatico del pannello ora mostra la lingua originale.
- Regolata la descrizione delle scorciatoie per il pannello mobile.

## 1.3.2

- Risolto il problema per cui il pannello di controllo non poteva essere chiuso sui dispositivi mobili

## 1.3.1

- Supporto della piattaforma di sottotitoli video [DeepLearning.ai](https://learn.deeplearning.ai)
- Supporto per la traduzione di pagine web e sottotitoli video in lingue come arabo, ebraico, ecc., affrontando i problemi di visualizzazione RTL (da destra a sinistra)
- Risolto il problema della traduzione di Gemini in ebraico
- Risolto un problema per cui alcuni sottotitoli in cinese tradizionale su YouTube non potevano essere visualizzati correttamente
- Risolto il problema di visualizzazione dei sottotitoli di Twitter su Safari
- Risolto il problema della scorciatoia per la traduzione immediata in fondo alla pagina

## 1.2.4

- Risolto il problema per cui i segnaposto nella creazione di ePub non venivano sostituiti correttamente
- Supporto per la traduzione dei sottotitoli video [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- Ottimizzato il controllo della frequenza delle richieste di servizio di traduzione
- Le recenti richieste di servizio di traduzione Microsoft dalla Cina sono state instabili; quando si verificano errori, il sistema rileva automaticamente il servizio di traduzione attualmente disponibile, consentendo agli utenti di passare rapidamente.
- Ottimizzato il messaggio di errore per gli errori di rete
- Risolto il problema per cui la configurazione del colore del testo non supportava l'anteprima RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Risolto il problema per cui l'aggiornamento della versione del plugin Safari richiedeva sempre la pagina di successo dell'installazione
- Microsoft ha aggiunto il supporto per il vietnamita
- Risolto il problema per cui i sottotitoli tradotti sul sito edx non venivano visualizzati

## 1.2.2

- Supporto per la traduzione dei sottotitoli video per [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). Supporta anche la traduzione di alcuni video con sottotitoli CC su Twitter.
- Ottimizzati i popup di errore, i popup di errore di problemi di rete rilevano automaticamente i servizi di traduzione gratuiti validi.
- Risolto il supporto dell'app iOS immersiva per la riproduzione a schermo intero di YouTube.
- Risolto il problema della traduzione dei paragrafi con Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Supporto per la traduzione dei sottotitoli video per [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/).
- Risolto un problema per cui alcuni utenti Pro non potevano modificare le impostazioni nel browser Chrome.
- Supportata la visualizzazione dei sottotitoli bilingue nella modalità a schermo intero di YouTube su iOS.

## 1.2.0

- Supporto per la traduzione dei sottotitoli video su piattaforme [LinkedIn](https://www.linkedin.com/) e [Viu](https://www.viu.com/).
- Aggiunto un accesso rapido ai sottotitoli video per piattaforme aggiuntive.
- Supporto per impostare siti web/lingue specifici per visualizzare solo il testo tradotto.
- Risolto un problema per cui la pagina delle impostazioni continuava a mostrare il caricamento in alcuni casi su Safari.
- Supporto per la traduzione dei nodi dei tag di input.
- Ottimizzata l'interfaccia utente dei popup di errore.

## 1.1.9

- Supporto per la traduzione dei sottotitoli per YouTube Live e la piattaforma [Mubi](https://mubi.com/).
- Ottimizzazione: pagina delle impostazioni, interfaccia utente dell'elenco URL (per evitare ambiguità, le caselle di controllo non vengono visualizzate per impostazione predefinita).
- Supporto per impostare il font di traduzione in modalità solo traduzione.
- Aggiunto accesso rapido per abilitare i sottotitoli video su Netflix, Ted, Bloomberg, Udemy, Coursera.
- Risolto: alcuni stili tradotti (come le sottolineature) non erano efficaci su Safari.
- Risolto: durante la traduzione della pagina, il problema per cui il passaggio del mouse non attivava la ritraduzione.

## 1.1.8

- Aggiunta un'opzione per il servizio di traduzione secondario per seguire il servizio di traduzione principale
- Supporto per sottotitoli bilingue per [Amazon Prime Video](https://www.primevideo.com)
- Ulteriore ottimizzazione della funzione di traduzione PDF incorporata in Sci-Hub
- Risolto un problema con i PDF online che non si aprivano correttamente
- Risolto il problema della riproduzione continua dei sottotitoli bilingue su Netflix

## 1.1.7

- Ora puoi specificare un font per la traduzione nella pagina delle impostazioni -> [Impostazioni di base] -> [Stile di traduzione]
- Aggiunta una configurazione di scorciatoie per [Traduci paragrafo specificato] nel pannello a sfera mobile
- Ottimizzata la sensibilità del rilevamento del passaggio del mouse su Ctrl per evitare di confondere `Ctrl+C` con `Ctrl`
- Aggiunto supporto per una nuova impostazione di scorciatoie che consente di attivare rapidamente se i sottotitoli video utilizzano i sottotitoli di traduzione automatica integrati
- Sul sito web di Sci-Hub, facendo clic sulla sfera mobile verranno tradotti i PDF incorporati nella pagina web

## 1.1.6

- **Supporto mobile per la traduzione di paragrafi specifici:** La versione mobile ora supporta la traduzione di paragrafi specificati e ha aggiunto una varietà di operazioni di scorciatoia, tra cui scorrimento a sinistra, scorrimento a destra, doppio tocco, triplo tocco e gesti multi-dito. Questi non sono abilitati per impostazione predefinita e richiedono all'utente di selezionare attivamente il gesto di attivazione nella pagina delle impostazioni sotto [Passaggio del mouse].
- **Aggiornamento della versione predefinita di Gemini:** La versione predefinita è ora `v1beta`.
- **Risolto il problema della traduzione del cinese classico:** Risolto il problema della funzionalità di traduzione del cinese classico di Microsoft e OpenAI.
- **Ottimizzazione della traduzione giapponese:** Ulteriormente ottimizzata la traduzione giapponese di OpenAI per migliorare l'accuratezza e la fluidità.
- **Esperienza di traduzione immersiva:** Per adattarsi meglio alle abitudini degli utenti, abbiamo spostato la scorciatoia per i sottotitoli bilingue in modalità a schermo intero sulla piattaforma YouTube a sinistra.

## 1.1.5

- Risolto il problema per cui il menu a discesa in modalità scura su Windows non aveva colore.
- Risolto il problema di allineamento con l'opzione "Altro" non allineata a sinistra su Windows.

## 1.1.4

- **Aggiornamento dell'interfaccia utente del pannello popup:** Il nuovo design mira a migliorare l'usabilità e la comprensibilità. Questo aggiornamento include:

  - **Nuove funzionalità nel menu principale:**
    - **Interruttore modalità bilingue/solo traduzione:** Ora puoi passare tra "Modalità di traduzione bilingue" e "Modalità solo traduzione" direttamente nel menu principale, situato a sinistra del pulsante di traduzione.
    - **Voce di traduzione documenti:** L'ingresso per tradurre "file PDF/ePub/sottotitoli" è stato spostato nel menu principale per un accesso rapido.
    - **Impostazioni di traduzione video:** L'ingresso per le impostazioni di "Traduzione video" è stato anche posizionato nel menu principale per regolazioni rapide.
    - **Nuova voce per la documentazione d'uso:** Fornisce guide operative dettagliate e documenti di aiuto.

- **Voce di traduzione documenti integrata:** Ora puoi tradurre file PDF, ePub e sottotitoli tramite un ingresso di caricamento unificato. Basta fare clic sul pulsante [PDF/ePub] nel pannello popup, non è più necessario selezionare [Altro].

- **Aggiunto supporto per 5 siti web video:**
  - Supporto per i sottotitoli dei podcast su Youtube Music.
  - Aggiunto supporto per il sito web iview.abc.net.au.
  - Aggiunto supporto per il sito web www.nma.art.
  - Aggiunto supporto per il sito web creativecloud.adobe.com.
  - Aggiunto supporto per il sito web www.masterclass.com.

## 1.1.3

- Risolto il problema di anomalia di visualizzazione del plugin mobile quando si aprivano pagine PDF.
- Ottimizzato l'effetto di traduzione delle conversazioni GPT.
- Supportata la traduzione di dominio per Baidu Translate.
- Aggiunta una modalità solo traduzione nella pagina delle impostazioni.
- Aggiunta una funzione di promemoria quando si cambia modalità di traduzione con scorciatoie.
- Risolto il problema per cui la traduzione dei campi di input contenenti URL traduceva solo parti del contenuto.

## 1.1.2

- Risolto: Il problema per cui il cambio di servizi di traduzione non aveva effetto quando la pagina non era ancora stata tradotta.
- Ottimizzazione: Nel processo di traduzione di Epub e PDF, se alcuni contenuti non riescono a essere tradotti, ora è possibile passare a un altro servizio di traduzione sul pannello senza riavviare l'intero processo di traduzione (la logica precedente era di utilizzare immediatamente un nuovo servizio di traduzione per ritradurre l'intero libro). Ciò significa che a metà della traduzione, puoi passare a un diverso servizio di traduzione e fare clic su [Riprova tutti i paragrafi non riusciti], dopodiché il sistema continuerà la traduzione utilizzando il nuovo servizio.
- Ottimizzazione: Regolata la dimensione del carattere dei messaggi di errore di traduzione per migliorare la leggibilità.

## 1.1.1

- Risolto il problema della scorciatoia dei sottotitoli bilingue per YouTube con testo inglese eccessivamente lungo.

## 1.1.0

### Nuove Funzionalità

- **Impostazioni delle Scorciatoie:** Aggiunto un nuovo menu di primo livello "Scorciatoie" e le seguenti funzioni di scorciatoia personalizzabili:

  - Designare una combinazione di tasti per tradurre il contenuto della casella di input corrente, integrando il precedente metodo di premere rapidamente la barra spaziatrice tre volte.
  - Designare una combinazione di tasti per abilitare temporaneamente "traduzione diretta al passaggio del mouse" sulla pagina. Premendolo di nuovo si annullerà questa funzione.
  - Aggiunte scorciatoie dedicate per 6 servizi di traduzione (come DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation) per facilitare il passaggio temporaneo tra i servizi di traduzione.

- **Aggiornamento dell'interfaccia utente della pagina delle impostazioni del plugin:**

  - In "Impostazioni avanzate", è stata aggiunta una nuova opzione per consentire agli utenti di specificare alcune parole (ad esempio, "LLM") da escludere dalla traduzione.
  - In "Impostazioni avanzate", è stata aggiunta una nuova opzione per configurare il numero minimo di caratteri richiesti per tradurre un paragrafo. Il valore predefinito è 4 caratteri, ma può essere impostato più alto (ad esempio, 20), in modo che solo i paragrafi più lunghi vengano tradotti.
  - Aggiunto un tutorial per principianti, che copre le impostazioni della sfera mobile, le impostazioni dei sottotitoli video e le impostazioni del passaggio del mouse.

- **Sottotitoli Bilingue di YouTube:** Aggiunto un accesso rapido nella finestra di riproduzione video di YouTube per abilitare o nascondere i sottotitoli bilingue (questa funzione può essere disattivata).

- **Supporto Lingua Deepl:** Aggiunto supporto per il portoghese (Brasile).

- **Guida per Nuovi Utenti:** Quando i nuovi utenti aprono per la prima volta una pagina in una lingua non target, viene visualizzata una bolla di guida di aiuto a sfera mobile.

### Ottimizzazione e Correzioni

- **Ottimizzazione dell'interfaccia utente:** Ridisegnata l'interfaccia utente per i messaggi di errore di traduzione della pagina per renderli più facili da comprendere. Quando ci sono molti errori, un popup avviserà attivamente l'utente.

- **Correzioni di Bug:**

- Risolto il problema in cui la traduzione al passaggio del mouse falliva quando la pagina perdeva il focus.
- Risolto il problema in cui meno di 3 caratteri nella funzione di miglioramento della casella di input non venivano tradotti.
- Risolto il problema in cui alcune directory non venivano tradotte durante la produzione di Epub bilingue.

- **Feature Removal**: Rimossa la funzione di miglioramento delle informazioni bilingue (visualizzazione simultanea dei risultati di ricerca in inglese sulle pagine di ricerca di Google).

### Altri Aggiornamenti

- **openAI Configuration Update**: Ora supporta l'impostazione del numero di configurazioni al secondo in decimali, come 0.5, che significa 1 richiesta ogni 2 secondi.

## 0.12.14

- Fix: Problema di riconoscimento della lingua di destinazione predefinita su alcune macchine dopo la prima installazione.
- Ottimizzazione: L'ordine predefinito dei titoli delle pagine web è cambiato in [Cinese - Inglese].

## 0.12.13

- Risolto: Problema con la cucitura della traduzione di paragrafi lunghi di OpenAI in alcuni casi. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Ottimizzato: Quando si utilizza il passaggio del mouse, il problema in cui la perdita di focus sulla pagina e poi il riattivamento diventa inefficace.
- Risolto: Il problema in cui la cache esiste ancora dopo aver modificato il prompt/modello in OpenAI.

## 0.12.12

- Aggiornato: Ottimizzato il pannello popup, rimuovendo alcune opzioni per il sito web corrente.
- Ottimizzato: Migliorato il processo di fusione dei sottotitoli manuali.
- Ottimizzato: Impostazione automatica della lingua di destinazione in base alla lingua del browser.
- Aggiunto: Supporto per sottotitoli bilingue per la piattaforma di apprendimento [ArtStation](https://www.artstation.com/learning) e [ZDF](https://www.zdf.de/).
- Risolto: Risolto il problema in cui i titoli sulla pagina dell'elenco jstor non venivano tradotti [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Risolto: Risolto il problema in cui solo parte del contenuto scompariva su Hacknews [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Aggiunto supporto per sottotitoli bilingue per le piattaforme [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/), e [Domestika](https://www.domestika.org).

## 0.12.10

- Risolto il problema di autorizzazione del dominio Gemini sotto lo script Tampermonkey.
- Supportata la traduzione in tempo reale dei sottotitoli per Twitter Space.
- Per le versioni precedenti dello script Tampermonkey, è stato ora aggiunto un prompt di aggiornamento alla pagina delle impostazioni.

## 0.12.9

- Aggiunto supporto per la traduzione Gemini.
- Risolto il problema in cui le traduzioni non rispondevano in tempo quando la pagina web veniva scorsa fino alla posizione centrale in alcuni casi.
- Risolto il bug in cui l'interruttore dei sottotitoli su alcuni siti video causava la visualizzazione ripetuta della traduzione.
- Risolto il problema in cui il mouse passava sopra per continuare a tradurre senza tenere premuto il tasto di scelta rapida in alcuni casi.
- Su macOS, ottimizzato il nome visualizzato del pannello di scelta rapida.

## 0.12.8

- Riparato i sottotitoli video originali non visualizzati quando "Il sito corrente è impostato per non tradurre mai".
- Riparato il conflitto con alcuni plug-in che causano il ritorno infinito della pagina.
- Riparato la non traduzione di alcuni paragrafi dopo aver attivato le interruzioni di riga dei paragrafi lunghi.
- Risolto [Quando si attiva temporaneamente la traduzione della pagina web per un lungo periodo, facendo clic sul pannello [Traduci sempre questo sito web] non si annulla la traduzione sempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Aggiunti sottotitoli bilingue per supportare le piattaforme [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) platforms. https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/) Platforms
- La hoverball è ora nascosta per impostazione predefinita quando il video è a schermo intero.
- Risolto il problema del clic tremolante del pannello di azione della hoverball della pagina di Firefox.
- Supporto per la collaborazione sotto il sito pubmed.ncbi.nlm.nih.gov e il plugin scholarscope
- Risolto il problema di tremolio della pagina di traduzione della casella di input di reddit

## 0.12.6

- Risolto il problema che la traduzione di YouTube/Web of Science ecc. non è sensibile quando si cambiano le schede.
- La hoverball su mobile ora supporta l'operazione di pressione lunga, pressione breve per tradurre, pressione lunga per aprire il pannello.
- Traducendo ebook bilingue ora tradurrà anche il sommario.
- La funzione di miglioramento della ricerca (alcune pagine di Google Search visualizzano risultati di ricerca bilingue) ora non è abilitata per impostazione predefinita e verrà rimossa nel prossimo release.

## 0.12.5

- Risolto il problema di creazione di eBook Epub dal pannello facendo clic sulle traduzioni non funzionanti

## 0.12.4

- Quando si attivano i sottotitoli bilingue nel pannello, verrà prima aggiornata automaticamente la pagina (per visualizzare i sottotitoli bilingue in modo più accurato), e alcuni siti richiedono ancora agli utenti di fare clic manualmente sul pulsante "CC" sul sito per attivare i sottotitoli.
- Ottimizza Grease Monkey, rilevamento della lingua Safari
- Fornisce un accesso rapido alle versioni bilingue di tutti i documenti sul sito di documenti [Arxiv](https://arxiv.org/abs/1910.06709).
- [Supporto hoverball configurato per essere fissato a sinistra #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Risolto il problema di visualizzazione della modalità di apprendimento #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Attivare temporaneamente la traduzione web per un periodo di tempo non annulla Traduci sempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Ottimizza i problemi di inizializzazione dei file PDF

## 0.12.3

- Risolto il problema della funzione [disabilita permanentemente i sottotitoli video] non funzionante [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)

## 0.12.2

- È fornito il supporto per sottotitoli bilingue per più piattaforme video, che ora sono supportate: [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy] (https://www\.khanacademy.org/), [Coursera] (https://www\.coursera.org/), [Vimeo] (https://vimeo.com/), [Nebula] (https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), ecc. (Nota che a causa delle limitazioni tecniche, alcuni siti web devono aggiornare la pagina dopo aver attivato i sottotitoli bilingue per la prima volta o attendere che la traduzione sia completata per visualizzare i sottotitoli bilingue). (Nota che a causa delle limitazioni tecniche, alcuni siti web devono aggiornare la pagina dopo aver aperto i sottotitoli bilingue per la prima volta, o devono attendere che la traduzione sia completata per visualizzare i sottotitoli bilingue)
- Ottimizzato significativamente la dimensione del file zip del plugin, ridotto della metà rispetto all'originale, download e aggiornamento più veloci.
- Risolto il problema di download esteso dei PDF
- Aggiunto un portale PDF di traduzione rapida sul lato destro del sito di documenti [Arxiv](https://arxiv.org/abs/1910.06709), che porta a una pagina HTML pulita (supportata solo da alcuni documenti, poiché richiede agli autori originali di inviare il codice sorgente, quindi circa il 50% dei documenti mostrerà questo portale)
- Le pagine PDF online senza estensione .pdf ora possono saltare direttamente alla pagina di traduzione PDF facendo clic sulla hoverball sulla pagina.
- Risolto alcuni problemi di miglioramento della casella di input sotto Safari
- Ottimizza il rilevamento della lingua in Grease Monkey e Safari

## 0.11.6

- Aggiunte 11 nuove lingue di interfaccia per il plugin e il sito ufficiale, ora le lingue di interfaccia supportate raggiungono 14, tra cui Cinese Semplificato, Cinese Tradizionale, Inglese, Giapponese, Coreano, Russo, Spagnolo, Portoghese, Hindi, Italiano, Tedesco, Francese, Arabo e Persiano.
- Modifica della condivisione bilingue (modalità di aggiornamento) aggiunta nella versione precedente alla condivisione di snapshot di pagina bilingue, in modo che il contenuto condiviso sia più originale, oltre a una maggiore adattabilità.
- Risolto l'emoji alla fine della casella di input di Twitter che non può essere tradotta
- Risolto il problema in cui il contenuto di plug-in di terze parti viene tradotto in alcuni scenari
- Riparato il clic non reattivo della hoverball online pdf

## 0.11.5

- Ora puoi generare un link pubblico alla pagina bilingue tradotta per Immersive Translate.
  - [Clicca](/docs/share/) sull'icona di condivisione di Immersive Translate per generarlo con un solo clic!
- Risolto il problema che alcune piattaforme non riuscivano a riconoscere se il mouse era supportato o meno
  - Ci sono alcuni browser desktop che supportano sia il touchscreen che il mouse, e Immersive Translates non è tecnicamente in grado di rilevare se tali piattaforme supportano il mouse, quindi abbiamo aggiunto l'opzione [Forza Abilita Supporto Mouse] nelle impostazioni [Mouse Hover]

## 0.11.2-0.11.4

- Ottimizza l'esperienza, risolvi alcuni bug

## 0.11.1

- Il modello predefinito per le traduzioni OpenAI è: GPT3.5-turbo-1106.
- Ottimizzato il Prompt Cinese per OpenAI, ora meno soggetto a allucinazioni!
- Ridotta la lunghezza dei prompt di OpenAI da 90 a 40, risparmiando ancora più traffico.

## 0.11.0

- Risolto il problema dei clic tremolanti della hoverball della pagina
- Risolto il problema delle traduzioni di Azure

## 0.10.9

- Risolti alcuni problemi minori

## 0.10.8

- Supporto per l'impostazione dei pulsanti di traduzione rapida della hoverball (supporto sia per PC che per mobile)
- Ottimizzazione del giudizio della lingua di Grease Monkey
- Risolto il problema della traduzione dei file txt

## 0.10.7

- Supporto per il passaggio del mouse premendo nuovamente Ctrl per mostrare il testo originale
- Ignora la lingua mai tradotta al passaggio del mouse
- Ottimizzazione dei sottotitoli bilingue di Youtube

## 0.10.6

- Supporto per la traduzione dei sottotitoli di Youtube solo
- Aggiungi avviso di aggiornamento della versione bassa di Grease Monkey
- Risolto il problema che i file txt locali non possono essere tradotti

## 0.10.5

- Risolto il problema di Youtube che occasionalmente ritorna alla homepage

## 0.10.4

- Risolto il conflitto dei sottotitoli di Youtube con il plugin Dual subtitle (Immersive Translate della traduzione dei sottotitoli di Youtube non è abilitato quando viene rilevato il plugin Youtube Dual per evitare conflitti)
- Aggiunta la [Funzione Disabilita Permanentemente i Sottotitoli Video], se ci sono altri problemi di conflitto e non si desidera abilitare la funzione di sottotitoli bilingue con Immersive Translate.
- Ottimizza le interruzioni dei sottotitoli

## 0.10.3

- Risolto il problema di traduzione della chiave di autenticazione personalizzata DeppL

## 0.10.3

- Supporto perfetto per i video di Youtube con sottotitoli bilingue 🎉.
- Per le pagine degli articoli, il testo del corpo verrà ora tradotto prima del resto del contenuto della barra laterale
- Ottimizzazione della contestualizzazione della traduzione DeepL
- Ottimizzazione della traduzione dei file di sottotitoli di OpenAI per la contestualizzazione

## 0.10.1

- Aumentata la priorità della traduzione del corpo per ottimizzare l'esperienza di traduzione
- Risolto il problema del testo non tradotto al clic su "ins more"

## 0.9.8

- Ottimizzazione dell'esperienza, risoluzione di alcuni bug

## 0.9.7

- Risolto il problema della traduzione automatica quando readwise è evidenziato

## 0.9.6

- Risolto il problema di cancellazione della cache disconnettendo l'accesso dell'utente.

## 0.9.5

- Correzioni di bug per eBook online

## 0.9.4

- Ottimizzazione del rilevamento del miglioramento dell'input per ridurre i tocchi accidentali
- Traduzione online di e-book e sottotitoli

## 0.9.3

- Traduzione della casella di input: visualizza un promemoria a comparsa quando viene utilizzata per la prima volta, e l'utente può scegliere di disabilitarla questa volta o permanentemente per evitare tocchi accidentali.
- Ottimizzazione della velocità di esportazione della traduzione solo PDF, se si sceglie di esportare solo la traduzione, è possibile chiamare direttamente l'anteprima PDF del sistema per esportare, più veloce.
- Deeplx supporta più URL, basta separarli con .

## 0.9.2

- Lo strumento di traduzione PDF è migrato alla versione online: https://app.immersivetranslate.com/pdf/ , in modo che Grease Monkey e Safari possano utilizzare la traduzione PDF, e i problemi possono essere meglio iterati senza la necessità di rilasciare una versione per risolvere il problema.
- Ottimizzazione dell'interfaccia utente POPUP, il pannello è più bello!

## 0.9.1

- Risolto il problema del nome file con la creazione di ebook Epub

## 0.8.8

- Supporto pdf per regolazioni di spaziatura tra righe e parole per riconoscere nuovamente i paragrafi
- Risoluzione del problema di scorrimento automatico della lettura online di epub su dispositivi mobili

## 0.8.7

- Supporto pdf per il download solo della traduzione
- Risolto il problema di accesso a Google su Safari

## 0.8.2 - 0.8.6

- Consente di impostare l'intervallo tra i trigger di combinazione di miglioramento dell'input
- Risoluzione di alcuni bug

## 0.8.1

- Ottimizzazione del rilevamento della lingua
- Funzionalità Beta: API personalizzata (Beta abilitata nelle impostazioni dello sviluppatore)
- Supporto per la traduzione AliCloud
- Risoluzione di alcuni bug

## 0.8.0

- Sistemi utente supportati
- Supporta [Enable Pro Membership](/pricing), che consente agli utenti di usufruire delle traduzioni Deepl e OpenAI e delle impostazioni di sincronizzazione cloud.
- Il servizio di traduzione al passaggio del mouse può essere impostato individualmente
- Il servizio di traduzione della casella di input può essere configurato separatamente
- Ottimizzazione della traduzione PDF
- Risoluzione di alcuni bug

## 0.7.16

- Traduzione PDF con nuove opzioni per il controllo rapido dello stile di traduzione (i file PDF sono molto strani e attivare queste opzioni può essere utile per alcuni file PDF con formattazione disordinata)
- Le versioni iOS e macOS sono tornate sull'Apple Store Country Store

## 0.7.15

- Siamo stati informati da Apple che le traduzioni OpenAI sono state temporaneamente rimosse da iOS e macOS, e stiamo cercando di rilanciarle in Cina.

## 0.7.11- 0.7.14

- Risolto: problema di traduzione di tutte le regioni di Gmail
- Disabilitata temporaneamente la funzione di esportazione PDF di Safari a causa della restrizione di Safari sui download dei plug-in (bug).
- Risoluzione di altri problemi

## 0.7.10

- Aggiornamento dell'interfaccia utente del pannello dell'icona del browser popup, un po' più di design ～
- Risolto il problema che alcuni passaggi in giapponese non venivano tradotti.

## 0.7.9

- Finalmente il PDF supporta l'esportazione di versioni bilingue! Puoi cliccare sul pulsante [Salva] per esportare il file PDF bilingue tradotto.
- Le regole personalizzate ora supportano la fusione con le regole predefinite integrate, ad esempio: `{"id": "youtube", "selectors.add":["#test"]}` significa aggiungere un `#test` ai selettori esistenti, `selectors` significa sovrascrivere il predefinito, `selectors.remove` significa eliminare uno dei selettori predefiniti, e `selectors.remove` significa eliminare uno dei selettori predefiniti.
- Aggiornata l'icona di Safari, un po' più grande.
- Altre correzioni di bug

## 0.7.8

- Correzioni di bug

## 0.7.7

- Adattato allo stile di sistema di Safari, l'icona dell'estensione di Safari è cambiata in contorno trasparente.
- Aggiunta la modifica dello stato dell'icona del browser, quando una pagina web è stata tradotta, verrà aggiunto un ✅ nell'angolo in basso a destra dell'icona del browser automaticamente.
- Abilitazione automatica della traduzione di siti web inglesi frequentemente utilizzati per i nuovi utenti
- Risolto il problema di traduzione con https://claude.ai/

## 0.7.6

- Supporto per la traduzione dei risultati di supporto migliorato dell'input ctrl+z Annulla
- Supporto per la traduzione in modalità di lettura documenti Flying Book
- Adattamento https://pi.ai/talk

## 0.7.5

- Risolto il problema dell'icona di Grease Monkey non visualizzata
- Risoluzione di numerosi problemi

## 0.7.4

- Risoluzione di numerosi problemi
- La pagina di configurazione supporta l'eliminazione in batch degli URL selezionati.
- Supporta l'abilitazione/disabilitazione della traduzione dei sottotitoli di Youtube per prevenire conflitti con altri plugin correlati.
- Arigato Translator supporta l'impostazione di campi e id di terminologia

## 0.7.2

- Miglioramento della casella di input: consente di omettere il prefisso // e attivare la traduzione dell'intera casella di input con 3 spazi, oppure è possibile disattivare questa opzione nella pagina delle impostazioni.

## 0.7.1

- Supporto per il miglioramento della ricerca, quando abilitato, quando si cerca su Google/Google News in cinese, la colonna di destra mostrerà automaticamente i risultati di ricerca delle parole chiave inglesi corrispondenti, che è abilitato per impostazione predefinita.
  - Motivo: Abbiamo scoperto che nella ricerca su Google, i risultati di ricerca per le parole chiave cinesi e inglesi possono essere molto diversi, con il miglioramento della ricerca tradotta immersiva abilitato, cerchiamo automaticamente le stesse parole chiave in inglese per te e le visualizziamo sul lato destro. Puoi scegliere di disabilitarlo se non hai bisogno della funzione.
  - Safari non è supportato a causa delle limitazioni dell'API.

## 0.6.20

- Modifica delle impostazioni predefinite: A causa del feedback di un gran numero di utenti che non utilizzeranno lo strumento di traduzione dopo l'installazione, la loro aspettativa dello strumento di traduzione è che traduca automaticamente le pagine web in inglese dopo l'installazione, quindi da questa versione in poi, per gli utenti cinesi, l'opzione di tradurre le pagine in inglese per impostazione predefinita è stata attivata (se l'utente ha avuto una precedente impostazione della lingua che verrà sempre tradotta, allora verrà rispettata, e la modifica modifica solo le impostazioni iniziali dell'estensione), e deve essere annullata, può essere facilmente annullata nel [pannello popup o nella pagina delle impostazioni](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- Risoluzione di bug PDF
- Risoluzione del bug del web of science
- Adattamento feeder.com
- Risolto il problema di epub che non traduceva alcuni libri

## 0.6.18

- Risolto il problema di overflow della larghezza del popup di Safari.
- Ottimizzazione del processo di costruzione

## 0.6.17

- Ottimizzazione degli avvisi di errore
- Ottimizzazione della selezione della lingua di destinazione, ora mostrerà solo le lingue supportate dal servizio di traduzione corrispondente
- Ottimizzazione della traduzione PDF
- Adattato per il sito web Good Reads, Amazon e South China Morning Post

## 0.6.16

- Aggiunta visualizzazione della pagina senza permessi PDF
- Riparazione della visualizzazione dei paragrafi dell'elenco di testo PDF
- Ingrandimento della scala dei piccoli caratteri PDF su Chrome e Safari

## 0.6.15

- Riparazione del problema che quando si aprono file PDF, il pannello dell'estensione avvisa che non ci sono permessi.
- Risolto il problema che il miglioramento della casella di input non è abilitato quando il sito è impostato per non tradurre mai.

## 0.6.14

- Ottimizzazione della traduzione PDF, l'area di traduzione può ora essere modificata/trascinata/eliminata
  - Trascina in alto a sinistra, elimina in alto a destra, cambia dimensione in basso a destra
- Allineamento a sinistra della casella a discesa di Windows
- Supporto per cinese tradizionale e cinese semplificato

## 0.6.13

- Risolto il problema della traduzione ripetuta al passaggio del mouse
- Supporto per la traduzione PDF trascinabile per cambiare la dimensione e modificare il contenuto della traduzione

## 0.6.12

- Risolto il problema delle immagini di traduzione Epub che diventano più piccole in alcuni browser
- Ottimizzazione della traduzione della casella di input, ora funziona senza problemi in Bard!

## 0.6.10

- Modello predefinito OpenAI cambiato alla versione 0613
- Risolto alcuni stili della casella di input
- Più intelligente nel determinare se è un'area di navigazione, e in tal caso, non viene eseguita alcuna traduzione
- Risolto possibile attacco di iniezione XSS

## 0.6.8

- Il pannello dell'estensione può ora indicare pagine non supportate (ad esempio, pagine senza permessi e pagine non HTML)
- Miglioramento della casella di input per mostrare lo stato di caricamento nella traduzione
- Aggiornamento dei colori di caricamento predefiniti nelle traduzioni
- Quando la casella di input è configurata senza prefisso, supporta la traduzione `ja Hello` in giapponese e `English Hello` in inglese.

## 0.6.6

- Risolto: alcune aree non tradotte (quora)

## 0.6.5

- Ottimizzazione di Google Bard
- La traduzione della casella di input supporta la traduzione diretta dell'intera casella di testo senza prefissi.
- Ottimizzazione del problema delle traduzioni OpenAI che aggiungono punti senza motivo, (se non viene rilevato alcun punto nel testo originale, se openai restituisce un punto, allora viene rimosso)
- Problemi con i file di sottotitoli di safari non riconosciuti

## 0.6.3

La lingua predefinita per la traduzione della casella di input può ora omettere lo spazio, cioè //Hello World può essere tradotto anche.

## 0.6.2

Il miglioramento della casella di input più entusiasmante è qui:

- Digita: // Hello World nella casella di input su qualsiasi pagina web, quindi fai triplo clic sulla barra spaziatrice per tradurre il paragrafo in inglese
- Puoi anche specificare la traduzione in una certa lingua: /ja Hello World, quindi fai triplo clic sulla barra spaziatrice per tradurre il paragrafo in giapponese

[Clicca qui per una rapida introduzione di 30 secondi](/docs/input/)

## 0.6.0

- Prima release di giugno, migrata dal precedente sottodominio personale https://immersive-translate.owenyoung.com al nuovo dominio https://immersivetranslate.com/
- La funzionalità è in gran parte invariata (nuove funzionalità saranno disponibili nella prossima release!)

## 0.5.17

- Risolto il problema che: gli eBook bilingue non hanno immagini dopo l'esportazione

## 0.5.16

- Risolto: problema di traduzione openai in cinese tradizionale

## 0.5.15

- Ottimizzazione: Il numero minimo di caratteri in un paragrafo che attiva la traduzione è stato modificato a un minimo di 4 caratteri per ridurre la confusione, mentre si utilizzano altre funzionalità per evitare di tradurre le aree di navigazione e di fine del sito.
- Risolto: dettagli di Github non tradotti dopo l'espansione.

## 0.5.14

- Risolto il problema per cui le immagini su alcune pagine web di: diventavano più grandi dopo la copia
- Risolto: sezione commenti di medium non tradotta
- Risolto il problema per cui le immagini su alcune pagine di: venivano copiate in modo errato

## 0.5.12

- Funzionalità: Lo stile di traduzione con linea di divisione aggiunge una linea di divisione verticale per le traduzioni su una sola riga
- Risolto: casi molto rari di divisione dei paragrafi.
- Una fantastica pagina di orientamento per la prima configurazione per i nuovi utenti iOS.

## 0.5.11

- Supporto alla traduzione dei sottotitoli per esportare solo le traduzioni
- Risolto: alcuni elementi non vengono riconosciuti dal passaggio del mouse
- Risolto: interruzioni di riga parziali nei tweet non riconosciute
- Risolto: lo stile di creazione degli eBook non funzionava

## 0.5.10

- Risolto: interruzioni di riga nei tweet non riconosciute
- Risolto: la pagina dei dettagli di Reddit restituisce alcuni paragrafi che non possono essere tradotti
- Risolto un problema con: dove alcuni tag di codice non venivano riconosciuti correttamente.

## 0.5.9

- Risolto: interruzioni di paragrafo in alcuni casi su:
- Risolto: Tampermonkey mostra solo le traduzioni
- Risolto: problema di funzionamento dello stile di lettura online degli eBook

## 0.5.8

- Risolto il problema per cui: l'impostazione temporanea della durata della traduzione del sito web non aveva effetto.

## 0.5.7

- Super aggiornamento!

- La funzione Mostra solo traduzioni è qui! Clicca su [Altro] -> [Passa a mostrare solo traduzioni].

  - Supporto scorciatoie personalizzate, impostate nelle impostazioni dell'interfaccia -> Impostazioni scorciatoie

- Ottimizzazione del problema di limitazione della frequenza delle richieste OpenAI

- ChatGPT predefinito al modello mobile, che è più veloce!

- Ristrutturazione dell'analisi del core web, il che significa:

  - Traduzione di pagine web su larga scala in pochi secondi
    - Ad esempio,: https://pve.proxmox.com/pve-docs/pve-admin-guide.html, che prima richiedeva 30 secondi, ora viene tradotta in pochi secondi.
  - Uso ultra-basso della memoria per pagine web complesse
    - Ad esempio: https://www\.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Adattamento a più siti web

- Tutte le traduzioni del sito web di ShadowRoot sono supportate.

  - Ad esempio: https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - Ad esempio, la sezione commenti di: https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Risolto il problema dello schermo bianco dopo la traduzione di siti web con idratazione come Next.js.

  - Ad esempio: https://webpack.js.org/

- Risolto il problema per cui la modifica della scorciatoia del passaggio del mouse richiedeva un aggiornamento della pagina per avere effetto

- Risolto un problema con il riconoscimento delle interruzioni di riga nei file TXT.

- Molti aggiornamenti!

- La funzione 'Mostra solo traduzioni' è arrivata! Clicca su 'Altro' -> 'Passa a mostrare solo traduzioni'.

  - Supporta scorciatoie personalizzate, che possono essere impostate in 'Impostazioni interfaccia' -> 'Impostazioni scorciatoie'

- Ottimizzato per il problema del limite di velocità delle richieste OpenAI

- L'analisi del core web è stata ricostruita, il che significa.

  - Traduzione istantanea per grandi siti web
  - Uso minimo della memoria per pagine web complesse
  - Migliore compatibilità con più siti web

- Ora supporta le traduzioni per tutti i siti web con ShadowRoot.

- Risolto il problema dello schermo bianco dopo la traduzione di siti web con idratazione, come Next.js

- Risolto il problema per cui la modifica della scorciatoia del passaggio del mouse richiedeva un aggiornamento della pagina per avere effetto

- Risolto il problema con il riconoscimento delle interruzioni di riga nei file TXT.

## 0.5.6

- Risolto: problema di popup della nuova scheda su macOS.
- Funzionalità: Nuova pagina guida per il nuovo utente.

## 0.5.5

- Risolto: problema dell'area del passaggio del mouse.

## 0.5.4

- Risolto: duplicato della pagina Spa

## 0.5.3

- Risolto: ascoltatore di tasti di scelta rapida per il passaggio del mouse.
- Risolto: traduzione del documento PDF
- Funzionalità: Aggiungi nuova pagina guida per il cliente

## 0.5.2

- Risolto: impostazioni delle scorciatoie del passaggio del mouse per userscript

## 0.5.1

- Risolto: OpenAI API non funziona.

## 0.5.0

- Funzionalità: Traduci il paragrafo corrente quando il mouse passa sopra.
- Funzionalità: Ristrutturazione della traduzione PDF, ora puoi tradurre la maggior parte dei PDF con Immersive Translate
- Risolto: Disabilita il menu contestuale non funzionante [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Risolto: Evita Content Security Policy per [Mastondon](https://mastodon.social/)

## 0.4.11

- Risolto: permesso userscript (solo per userscript).

## 0.4.8

- Funzionalità: Bing Translate a Microsoft Translate per una qualità più stabile.
- Risolto: pagina web TXT pura come [questa](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Prestazioni: Escludi alcune pagine pubblicitarie figlie nel sito web, e le prestazioni sono migliorate un po'

## 0.4.7

- Risolto: popup mancante per Userscript su Firefox.

## 0.4.6

- Funzionalità: Consenti a terze parti di inviare eventi di documento per chiamare `toggleTranslatePage`
- Funzionalità: l'app iOS aggiunge il pulsante di abilitazione dell'estensione e il link alle comunità
- UI: il modello del campo delle impostazioni OpenAI utilizza la selezione invece della casella di input del testo.

## 0.4.5

- Risolto: problema di estensione safari su iOS 15.0.
- Risolto: scorciatoie dell'estensione safari su macOS
- Risolto: popup della politica di sicurezza dei contenuti per l'estensione, e in parte per userscript.

## 0.4.4

- Chore: Rimuovi console.log

## 0.4.3

- Risolto: rilevamento degli spazi bianchi nei tag sup, sub.
- Funzionalità: supporta il sito web ChatGPT Plus come servizio di traduzione, questa è una funzionalità beta, quindi puoi accedervi abilitando la funzionalità Beta nelle impostazioni dello sviluppatore. È molto lento, perché chatgpt può inviare solo una richiesta alla volta. Assicurati di avere un account ChatGPT Plus, perché ci sono più limiti sull'account gratuito, e non sono sicuro se questo comporta rischi per il tuo account, fai attenzione ad usarlo.

## 0.4.1

- Risolto: il menu contestuale di Firefox scompare dopo il riavvio.
- Supporto Azure openai

## 0.4.0

- Funzionalità: Supporta la traduzione di file di sottotitoli locali (.srt,.ass,ecc.)

## 0.3.17

- Funzionalità: Supporta la traduzione di file .txt locali.
- Risolto: il menu contestuale potrebbe non essere disponibile a volte. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Risolto: mantieni &nbsp; come spazio bianco.
- Rimosso: Rimuovi Papago, poiché [il servizio è inattivo](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: consenti nessuna chiave API per openai
- UI: consenti il reset delle impostazioni predefinite di Open AI

## 0.3.14

- Dipendenza: Aggiorna pdf.js all'ultima versione
- Risolto: colore di sfondo della selezione pdf
- Risolto: rilevamento degli spazi bianchi

## 0.3.13

- Risolto: problema di caratteri specifici del costruttore di ebook, come alcuni percorsi di capitoli sono `xxx' xxxx`.
- UI: piega le opzioni personalizzate di openai per impostazione predefinita.
- UI: Aggiungi stato di esportazione per l'esportazione epub.
- Risolto: prompt predefinito di Gpt4

## 0.3.12

- Funzionalità: Ora possiamo personalizzare il colore di sfondo del tema di traduzione del marcatore.
- Risolto: postMessage quando la pagina iniziale rompe alcuni siti, ora lo faremo solo quando traduciamo davvero le pagine
- Risolto: problema di avanzamento degli ebook.
- Risolto: migliore per dividere lunghi paragrafi, 1.5 miliardi, 25.5%, Mr. non sarà considerato come un confine

## 0.3.11

- Risolto: colore del testo in modalità scura del lettore di ebook
- Risolto: prompt openAI

## 0.3.10

- Migliore: rileva contenitore giapponese/coreano.
- Risolto: Progresso del costruttore di ebook fermo al 99%.

## 0.3.9

- Risolto: lo stato di input dei servizi di traduzione dell'interruttore UI delle opzioni non cambiava.

## 0.3.8

- UI: colore di caricamento più trasparente
- Risolto: Rileva lingua ebook.
- Funzionalità: Aggiungi progresso di traduzione per il costruttore di ebook, e una bella pioggia di coriandoli dopo il successo.
- Funzionalità: Aggiungi riprova per tutti i paragrafi falliti per il pulsante di riprova.
- Risolto: Gestione errori Deepl

## 0.3.7

- Risolto: il lettore di ebook non può caricare immagini su Chrome.

## 0.3.6

- UI: migliore per creare l'interfaccia della pagina ebook

## 0.3.5

- Risolto: esportazione ebook userscript
- Funzionalità: aggiungi endpoint API personalizzato per OpenAI
- Funzionalità: aggiungi opzioni di tempo di traduzione temporanea del sito web su `Impostazioni avanzate`

## 0.3.4

- CI: Build fallita

## 0.3.3

- Risolto: costruttore di ebook per Kindle
- Modifica: colore dell'icona di caricamento, da nero a blu, per adattarsi alla pagina web in modalità scura.
- Funzionalità: Supporta la traduzione html locale per l'estensione

## 0.3.2

- Risolto: spostamento del cursore di input del modulo delle opzioni.
- Funzionalità: OpenAI supporta apiUrl personalizzato per le impostazioni dello sviluppatore.

## 0.3.1

- Funzionalità: aggiorna l'icona scura alla trasparenza.
- Risolto: Ordine errato per lungo paragrafo

## 0.3.0

- Versione: D'ora in poi, cambieremo il numero di versione minore una volta al mese, ad esempio, ora a marzo, la versione inizierà da 0.3.0, ad aprile, il numero di versione inizierà da 0.3.0, ad aprile, il numero di versione inizierà da 0.4.0, il prossimo aprile, il numero di versione sarà 1.4.0, e così via. Questo perché non ha senso per le estensioni seguire Questo perché non ha senso per le estensioni seguire la semantica, ma standardizzare i numeri di versione secondo le leggi del tempo è una motivazione per lo sviluppo per continuare ad aggiornarsi, e per gli utenti per trovare problemi più facilmente.
- Funzionalità: Supporta icona scura per firefox

## 0.2.86

- Aggiungi opzione di lunghezza massima del testo per richiesta con Open AI
- Risolto: identificatore ebook duplicato
- Funzionalità: Supporta la traduzione della pagina web txt

## 0.2.85

- Risolto: alcuni file epub non possono essere trovati.

## 0.2.84

- Funzionalità: Supporta Lettore e Creatore di Ebook

## 0.2.83

- Funzionalità: Consenti al modulo di input della password di mostrare la password.

## 0.2.82

## 0.2.81

- Fix: m.youtube.com
- Fix: opzioni form UI
- Fix: Open AI prompt
- Feat: Supporto OpenAI multiple keys, usa `,` per separarli.

## 0.2.80

- Feat: Aggiungi Abilita/Disabilita Menu per popup -> more
- Fix: Conflitto Messaggio DingTalk

## 0.2.79

- Fix: Open AI per paragrafo spazio

## 0.2.78

- Feat: supporto OpenAI CHATGPT 3.5 (supporta l'interfaccia OpenAI ChatGPT 3.5)
- Feat: Aggiungi nuovo tema Solid Border (新增新主题，实线边框)

## 0.2.77

- Fix: errore tag multipli di codice.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Fix: errore tag multipli di codice [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Feat: Supporto conteggio testo traduzione immediata personalizzata per diversi servizi di traduzione.

## 0.2.74

- Feat: Supporto Tencent (alpha)
- Fix: traduzione openai
- Fix: controllo inline tag sconosciuti

## 0.2.73

- Feat: Supporto Tema Traduzione Grigio
- Fix: Pagina Trending di Github

## 0.2.72

- Fix: problema di rete del servizio di traduzione verifica mobile firefox.

## 0.2.71

- Fix: permesso userscript Open AI

## 0.2.70

- Fix: placeholder Open AI

## 0.2.69

- Feat: Supporto Open AI come servizio di traduzione.
- Feat: Supporto verifica servizio di traduzione su options.html
- Feat: Supporto frame principale personalizzato poiché alcuni siti non usano il body come frame principale

## 0.2.68

- Supporto Caiyun (Alpha)
- Fix tag blocco sconosciuti

## 0.2.67

- Feat: Aggiungi `<all>` per tradurre sempre le lingue, quindi ora puoi usarlo per tradurre tutte le lingue tranne la lingua di destinazione, e mai tradurre le lingue
- Fix: Consenti configurazione API google personalizzata
- Migliore: Supporto Deepl Free
- Fix: uso elevato della memoria per userscripts ed estensioni (rimuovendo opencc zh-CN a zh-TW, invece con Google translate)
- Fix: Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Fix: configurazione traduzione Azure ma ancora mostra (necessita configurazione)

## 0.2.66

- Fix: traduzione file PDF fallita, Bug dalla 0.2.60 per supportare deepl da zh-CN a zh-TW

## 0.2.65

- Supporto richiesta throttle per frame multipli
- Non tradurre il titolo della pagina quando in iframe

## 0.2.64

- Fix: openl scegli servizi di traduzione
- Feat: Supporto opzione è tradurre titolo

## 0.2.63

- Feat: Supporto Servizio di Traduzione Azure
- Feat: Supporto Servizio di Traduzione Papago
- Fix: sincronizzazione google drive android firefox nativa.
- Fix: cambia trasparenza da 0.4 a 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Fix: suggerimenti scorciatoie popup
- Performance: richieste seriali a concorrenza
- Migliore per rilevare conteggio giapponese

## 0.2.62

- Feat: Aggiungi regola waitForSelectors, per correggere alcuni siti come reddit

## 0.2.61

- Fix: userscript è troppo grande per greasy fork
- Migliore: riduci dimensione file

## 0.2.60

- Feat: Supporto zh-CN a zh-TW per Deepl
- Feat: Funzionalità Immersive Translate Deepl
- Feat: Supporto zoom dimensione carattere personalizzato
- Fix: stile forum Steam
- Fix: stile globale non cambiato dopo elementi dinamici generati
- Fix: promuovi priorità esclusione
- UI: modifica pagina about
- Fix: alcuni elementi matematici rimangono originali

## 0.2.59

- Fix: Elemento Blocco Tag Sconosciuti
- Fix: traduci=no elemento sovrascrive
- Fix: corrispondenza url con multipli \*

## 0.2.58

- Feat: Supporto colore testo traduzione personalizzato, colore bordo.

## 0.2.57

- Nessuna modifica, ricostruzione

## 0.2.56

- Fix traduzione duplicata per elementi inline con elemento codice.
- Fix controllo inline/blocco tag sconosciuti
- Feat: supporto css iniettato su scheda sviluppatore
- Feat: taglia authKey, appid appSecret
- Migliore: apri pagina impostazioni su nuova scheda (ma non per Stay)

## 0.2.55

- Prova a correggere charset api deepl

## 0.2.54

- Rimuovi permesso schede per rifiuto chrome store
- Fix traduci l'intera pagina, il footer è ignorato
- Aggiungi note alla pagina about
- Supporto url personalizzato da Config integrato

## 0.2.53

- Fix errore sincronizzazione google drive userscript.

## 0.2.52

### Codice

- Usa l'ultima versione di esbuild
- Usa l'ultima versione di deno
- CI: invia codice sorgente a firefox

## 0.2.51

- Fix Google Auth Necessita Login su Chrome/Firefox
- Sostituisci link servizio di traduzione
- Migliore per permesso.
- rimuovi minify.

## 0.2.50

- Fix problema caricamento google drive (davvero) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Rimuovi scorciatoie alt+d, alt+s perché potrebbero confliggere con scorciatoie native.
- Fix problema caricamento google drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Migliore per velocità, aggiungendo minLength a 50 per rilevamento lingua.
- Fix convalida token Google Drive.

## 0.2.47

- Fix api deepl

## 0.2.46

- correggi segno blocco

## 0.2.45

- Fix innerText elemento è indefinito
- Fix traduzione caiyun lingua sorgente indefinita

## 0.2.44

- Fix maschera toggle userscript
- Fix logica maschera toggle

## 0.2.43

- Fix maschera toggle userscript con evento touch.
- Fix velocità (rimuovendo sleep(300))

## 0.2.42

- Fix maschera hover quando si attiva nuovamente la maschera.
- Aggiungi scorciatoie maschera per mobile
- Fix problema sincronizzazione cloud userscript
- Sposta pagina opzioni avanzate nel menu a sinistra.
- Aggiungi logica di riprova al servizio di traduzione

## 0.2.41

- Fix traduzione niu userscript
- Fix traduzione xhtml

## 0.2.40

- Fix mostra funzionalità beta
- Fix pagina impostazioni popup su nuova scheda
- Fix sostituzione placeholder traduzione

## 0.2.39

- Supporto scorciatoie per mostrare traduzione maschera
- Supporto abilita funzionalità beta nel pannello sviluppatore
- Fix scorciatoie in estensione mobile

## 0.2.38

- Supporto tema di caricamento
- Fix getpocket.com
- Fix footer a parte per area corpo
- Fix icona import/export

## 0.2.37

- Fix segno esclusione frame

## 0.2.36

- Supporto sincronizzazione su Google Drive

## 0.2.35

- Fix giapponese rb, rt tag ignora.
- Migliore per popup ui more
- Migliore per suggerimenti userscript errati
- Aggiungi contributo alla pagina about
- Fix volc traduci per rilevamento lingua automatico

## 0.2.34

- Fix velocità lingua multipla

## 0.2.33

- Supporto modalità di scrittura verticale, come il giapponese.
- Aggiungi 3 temi
- Aggiungi servizio di traduzione Niu

## 0.2.32

- Fix traduzione base PDF
- Fix selezione popup di un servizio non configurato, vai alla pagina opzioni.
- Fix rimani aperto impostazioni.
- Fix velocità rilevamento lingua multipla

## 0.2.31

- Fix iniezione css iframe dinamico

## 0.2.30

- Supporto traduzione iframe inline userscript.
- Supporto traduzione shadowroot. Per esempio:
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Area di conversazione.
- controlla anche la regola di sincronizzazione su popup

## 0.2.29

- Fix traduzione Facebook
- Supporto mostra opzione menu contestuale.

## 0.2.28

- Rimuovi corrispondenza non standard per userscript

## 0.2.27

- Supporto traduzione iframe inline. (Solo per estensione, non disponibile per
  userscript)
- Fix traduzione lingua multipla

## 0.2.26

- Fix addon android firefox
- Aggiungi impostazioni avanzate per traduzione nuova linea

## 0.2.25

- Supporto traduzione iframe, come QQ mail, tweet incorporato.

## 0.2.24

- Aggiungi sito di traduzione temporanea per un po'
- Fix API browser userscript stay.app
- Fix pagina opzioni stay.app

## 0.2.23

- Fix traduzione pagina lingua multipla

## 0.2.22

- Fix build userscript

## 0.2.21

- Fix traduzione pdf online firefox

## 0.2.20

- Fix problema richiesta macaque
- Fix segna altezza linea evidenziata

## 0.2.19

- Fix giapponese intelligente tencent
- Fix browser mondo haikuo

## 0.2.18

- Fix cambio url client, rimane automaticamente lo stato di traduzione.
- Rimuovi contenitore a parte come contenitore di traduzione.
- Refactor posizione popup.

## 0.2.17

- Cambia evidenziazione in segno
- Aggiungi tema traduzione evidenziata

## 0.2.16

- Compatibilità Macaque

## 0.2.15

- Fix problema rimbalzo touch

## 0.2.14

- Fix safari globalThis.GM non funzionante

## 0.2.13

- Supporto Trascinamento Popup Userscript
- Supporto Tre Dita su dispositivo Touch per attivare pagine di traduzione toggle
- Supporto Nascondere l'icona popup userscript.

## 0.2.12

- Migliore per inoreader

## 0.2.11

- Fix
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas archive Il contenuto principale della pagina non poteva essere tradotto

## 0.2.10

- Fix distanza tra le righe nel pdf

## 0.2.9

- Fix escludere elementi marcati
- Fix controllo tipo deno
- rimuovere importmap
- Fix traduzione dei menu contestuali
- ripristinare la pagina quando l'opzione "never translate this site" è abilitata
- Aggiungi descrizione per aggiungere url

## 0.2.8

- Rileva la lingua dell'agente utente per la lingua dell'interfaccia
- Fix bug di interruzione di riga.

## 0.2.7

- Fix richiesta grease monkey

## 0.2.6

- Fix
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  problema di corrispondenza dell'url del file

## 0.2.5

- aumentare la versione per il test ci

## 0.2.4

- catturare errore di connessione del messaggio per il popup.

## 0.2.3

- Fix
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  creare contesto più volte

## 0.2.2

- Fix file di esempio PDF
- Fix file locale pdf su Firefox
- Fix scorciatoie pdf

## 0.2.1

- Supporto per il gestore di scorciatoie di Grease Monkey.
- Fix regex di corrispondenza
- Fix commenti di youtube.
- Fix versione compatta mobile di reddit
- Fix problema di traduzione del testo completo

## 0.2.0

- Fix PDF a due colonne.
- Fix bug della versione Store di Chrome/Edge.
- Fix
  [#21] (https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Pubblicare su addon di Firefox
- Pubblicare su Edge
- fix margine pdf.
- Cambia file di esempio pdf

## 0.0.62

- Fix formato pdf, rientro.
- Fix telegra.ph prevenire il cambiamento degli elementi

## 0.0.61

- Fix chiusura elemento span.
- Fix permesso per browser precedenti

## 0.0.60

- Fix PDF di Chrome

## 0.0.59

- Supporto iniziale per PDF

## 0.0.58

- Modifica descrizione del tema di traduzione

## 0.0.57

- Cambia interfaccia utente del popup, per un uso più facile

## 0.0.56

- Fix timeout di chrome
- Fix errore di divisione della frase.

## 0.0.55

- Fix visualizzazione di elementi con display none.
- refactoring del marcatore di elementi

## 0.0.54

- Supporto per interruzione di riga per X caratteri.

## 0.0.53

- usa sendMessage invece di connect, perché chrome disconnetterà la porta dopo
  5 minuti
- migliore rilevamento dei contenitori di testo

## 0.0.52

- Non tradurre il paragrafo che ha solo elementi segnaposto, per
  [esempio](https://github.com/nank1ro/solidart), la prima riga.
- Migliore rilevamento degli elementi figli.

## 0.0.51

- Fix problema di cache
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive- translate/next-immersive-translate/issues/7)
- Fix dimensione del font dell'interfaccia utente delle opzioni

## 0.0.50

- Fix traduzione di img bloccate.

## 0.0.49

- Fix estensione firefox

## 0.0.48

- Fix estensione chrome

## 0.0.47

- riscrittura del messaggio con background, usa connect invece di sendMessage
- aggiungi supporto mobile per reddit
- fix spazio bianco pre per alcuni articoli

## 0.0.46

- Formatta informazioni meta dello userscript

## 0.0.45

- userscript usa un file unico.
- aggiungi timeout per richiesta cache

## 0.0.44

- Fix errore di divisione tencent.
- Fix errore elemento sup inline.
- Migliore per twitter

## 0.0.43

- Fix tweet br
- Fix traduzione globale.

## 0.0.42

- Fix tag BR
- trattare i tag di blocco secondo le regole

## 0.0.41

- Fix controllo elemento inline
- Aggiungi opzione di log di debug per sviluppatori

## 0.0.39

- Fix servizio di traduzione contiene mock2

## 0.0.38

- Supporto per il risultato della cache per userscript
- Aggiungi interfaccia utente delle opzioni
- Supporto per rilevare più contenitori di contenuti

## 0.0.37

- Fix cambio servizio di traduzione del popup non funziona
- Fix traduzione del contenuto del post mobile di reddit.

## 0.0.36

- Fix carattere speciale di Wikipedia
  [#6] (https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Fix dimensione dell'icona dello userscript.
- abilita tutti i siti a rilevare la lingua del paragrafo.

## 0.0.35

- Fix youtube vai alla pagina successiva
- Supporto per la pagina di ricerca di Youtube.
- Fix interruttore avanzato delle opzioni.
- Fix tag img, tag nascosto
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Fix aggiornamento forzato di Google Search
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Supporto per il risultato della tabella di Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Fix spazio vuoto di Wikipedia
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Modifiche Interrotte

- La scorciatoia predefinita per attivare la traduzione è stata cambiata in `alt+A`, perché
  è la chiave più conveniente da digitare.

### Altri

- Supporto per impostare la modalità di traduzione immediata, in modo da poter tradurre la pagina web
  il più rapidamente possibile.
- Supporto per impostare l'area della pagina che deve essere tradotta, in modo da poter tradurre più area.
- Supporto per impostare il primo x conteggio di testo da tradurre immediatamente.
- Fix traduzione duplicata quando si cambia traduzione
- Migliore interfaccia utente del popup

## 0.0.33

- Supporto per più lingue, zh-TW, en

## 0.0.32

- Fix traduzione del file locale dopo il salvataggio. Risolto
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Aggiungi file js dist al repository pubblico

## 0.0.31

- Supporto per tradurre l'intera pagina
- Supporto per tradurre la pagina immediatamente
- Più interfaccia utente di configurazione
- Riflette il tema
- Aggiungi nuova icona
- Aggiungi nuovo tema di traduzione dashedBorder

## 0.0.30

- Migliore per il tema tratteggiato

## 0.0.29

- Fix paragrafo valido.
- Aggiungi tema punteggiato, thinDashed
- Migliore per tema tratteggiato, evidenziato

## 0.0.28

- Fix sottolineatura
- Aggiungi tema tratteggiato, carta
- Fix rilevamento intestazione

## 0.0.27

- Supporto per translationTheme

## 0.0.26

- Fix permesso di connessione dello userscript volc alpha.
- Fix versione cliccabile.

## 0.0.25

- Supporto per selectorMatches, in modo da poter abbinare tutti i manstondon ora.
- Fix errore dello userscript di Firefox.

## 0.0.23

- Migliore rilevamento del cinese
- Fix problema di innerText di reddit

## 0.0.22

- Supporto per deeplx
- Fix traduzione multipla quando si cambia servizio

## 0.0.21

- Fix alcuni tag span sono elementi di blocco

## 0.0.20

- Supporto per non tradurre hashtag come #hash, tag come @xxx, $tag, come $APPL
- Supporto per elemento di blocco

## 0.0.18

- Supporto per deepl, bing, baidu, youdao, volc, openl, caiyun.

## 0.0.13

- Supporto per userscript

## 0.0.4.8

- Fix ordine del codice.
- Supporto per interfaccia utente popup di base

## 0.0.4.6

- Supporto per controllare nuova versione

## 0.0.3

- Supporto per file locali

## 0.0.2

- Supporto per elementi dinamici
- Supporto per traduzione visibile