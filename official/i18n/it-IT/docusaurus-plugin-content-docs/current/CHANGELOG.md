---
sidebar_position: 6
---

# Registro delle Modifiche

Questo registro delle modifiche viene aggiornato in base al progresso dello sviluppo. La data dopo la versione è la data di fusione del codice, non la data di release negli app store (il tempo di revisione varia dopo la sottomissione a ciascun app store, con alcuni che impiegano fino a una settimana per la revisione). Attualmente, stiamo avanzando con due versioni.

La **Release version** è la versione stabile ufficiale, disponibile nei principali app store come
[Chrome](https://chromewebstore.google.com/detail/bpoadfkcbjbfhfodiogcnhhhpibjhbnh),
[Edge](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg),
[Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate/),
[Apple](https://apps.apple.com/app/id6447957425), ecc.

La **Preview version** viene pubblicata più frequentemente e include alcune funzionalità sperimentali. Rispetto alla versione Release, può contenere più bug. Viene rilasciata principalmente su

- [userscript del sito ufficiale](https://download.immersivetranslate.com/immersive-translate.user.js)
- [versione beta nel Firefox store](https://addons.mozilla.org/firefox/addon/immersive-translate-beta/)
- [Github Release Assets](https://github.com/immersive-translate/immersive-translate/releases)

## 1.14.16 Release (2025-02-21)

- Aggiunto: Supporto al cambio di contesto per Deepseek, Gemini, Claude.
- Risolto: L'aggiornamento dei termini non invia nuove richieste di traduzione.
- Migliorato: Aggiunta della lingua ungherese nell'interfaccia.
- Migliorato: Qualità della traduzione di Google.
- Migliorato: Formattazione delle immagini gratuita.

## 1.14.12 Release (2025-02-19)

- Migliorato: La pausa della traduzione cancella immediatamente la coda delle richieste.
- Migliorato: Filtri per il testo sporco nel servizio di traduzione deepl.
- Risolto: Traduzione della barra laterale non valida nelle impostazioni avanzate.
- Risolto: Problema di visualizzazione della traduzione personalizzata deepseek.

## 1.14.11 Release (2025-02-18)

- Risolto: Errore `401: Authentication Fails` per la chiave API personalizzata di DeepSeek.

## 1.14.10 Release (2025-02-17)

- Nuovo: L'abbonamento Pro supporta il servizio di traduzione DeepSeek (v3).
- Risolto: Risolto il problema del file di configurazione utente che supera il limite di dimensione.
- Migliorato: L'elemento del menu contestuale può essere chiuso (operazione nelle impostazioni avanzate).
- Migliorato: Migliorate le capacità di riconoscimento della lingua per Greasemonkey e Safari su pagine con lingue minori.
- Migliorato: Accesso all'interfaccia del servizio di test della pagina delle impostazioni online.
- Migliorato: Migliorata l'esperienza utente della funzione di anteprima del confronto del contesto.
- Migliorato: Logica di giudizio della modalità touch e mouse.

## 1.14.8 Release (2025-02-10)

- Risolto: Problema in cui i file lunghi PDF-Pro non venivano tradotti automaticamente.
- Migliorato: Microsoft, Google e Tencent ora supportano il cantonese.
- Migliorato: La BBC ora supporta i sottotitoli.

## 1.14.6 Preview (2025-02-08)

- Risolto: Problema in cui **Mouse Hover Translation** non poteva tradurre il testo ricco.
- Migliorato: La versione Tampermonkey ora supporta la traduzione dei sottotitoli di YouTube.

## 1.14.4 Release (2025-02-07)

- Risolto: Problema con il rilevamento errato della lingua in **Enhanced Input Box**.
- Risolto: Problema di abbinamento intelligente degli esperti AI nei servizi di traduzione personalizzati.
- Risolto: Problema di sincronizzazione di Google Drive su alcuni browser.
- Risolto: Problema di traduzione dei commenti live di YouTube.
- Risolto: Problema di sovrapposizione dei sottotitoli in alcuni video di YouTube.
- Migliorato: Fallimento nella traduzione di manga su siti come shonenjumpplus nel browser Safari.

## 1.13.8 Release (2025-01-24)

- Nuovo: La traduzione di immagini gratuita è ora disponibile (attualmente supportata solo su versioni PC dei browser Chrome e Edge), accessibile tramite il menu contestuale.
- Risolto: Affrontato un problema in cui alcuni contenuti venivano persi durante la traduzione multi-segmento in Gemini.
- Ottimizzato: Migliorato il caricamento dei sottotitoli di YouTube.
- Nuovo: Il servizio di traduzione AI ora supporta il norvegese.

## 1.13.6 Preview (2025-01-17)

- Migliorato: **AI Expert** può essere utilizzato con **AI Context-Aware Translation**.
- Migliorato: **Image Translation** è ora compatibile con weibo.com (supportato solo su Chrome e Edge).
- Migliorato: Quando la lingua dell'interfaccia è impostata su inglese, la lingua di destinazione predefinita per **Enhanced Input Box** è cambiata in cinese.
- Migliorato: Aggiunta una voce di revisione del negozio nelle opzioni **More** sul pannello.

## 1.13.5 Release (2025-01-14)

- Migliorato: Compatibile con il modello di pensiero Gemini 2.0.
- Migliorato: Supporta lo stile grassetto in modalità solo traduzione.

## 1.13.4 Preview (2025-01-13)

- Aggiunto: I membri Pro possono ora utilizzare direttamente il modello **zhipu 4.5**.
- Migliorato: Traduzione Gemini.

## 1.13.1 (2025-01-10)

- Aggiunto: Quando il testo tradotto e il testo originale appartengono allo stesso sistema di scrittura, visualizza la traduzione utilizzando uno stile specializzato.
- Risolto: Il problema in cui **Mouse Hover Translation** non funziona su alcuni siti web.
- Migliorato: DeepLx ora supporta l'arabo.
- Migliorato: Migliorato il riconoscimento della lingua originale. In precedenza, le pagine contenenti più lingue potevano non essere tradotte, ma ora vengono tradotte correttamente.
- Migliorato: Per Twitter, le traduzioni di contenuti multilinea sono impostate per non andare a capo per impostazione predefinita. Il ritorno a capo avverrà solo quando il contenuto supera le 10 righe o i 1000 caratteri. Il ritorno a capo può essere abilitato tramite le impostazioni **Advanced Settings** -> **Enable automatic line wrapping for long paragraphs**.

## 1.12.8 (2025-01-03)

- Risolto: il problema in cui la pagina delle impostazioni di iOS 18.3 non può essere visualizzata correttamente.
- Risolto: la mancanza di righe vuote durante la traduzione di tweet.
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
- Migliorato: Rimosso il modello gemini-1.0-pro deprecato.

## 1.12.4 (2024-12-13)

- Aggiunto: **AI Context-Aware Translation** può migliorare l'accuratezza della traduzione di contenuti professionali. (Disponibile solo per i membri Pro, supportato esclusivamente dai modelli OpenAI) **Options** -> **Grneral** -> **Enable AI Context-Aware Translation**
- Risolto: Alcuni bug nell'effetto di traduzione multilinea su Twitter.
- Risolto: Problemi con la traduzione di alcune formule a causa del testo ricco.
- Migliorato: Quando si traduce su **x.com**, i video con sottotitoli avranno automaticamente i sottotitoli bilingue tradotti.
- Migliorato: I video senza sottotitoli mostreranno un'icona di traduzione e forniranno una ragione per cui la traduzione non è possibile.

## 1.11.7 (2024-11-25)

- Aggiunto: Bing/Google ora supportano il khmer (cambogiano).
- Aggiunto: Consenti ai file ePub incompleti di continuare la traduzione da dove si erano interrotti al momento della reimportazione.
- Risolto: Problema con la traduzione delle immagini di Twitter nel browser Safari.
- Risolto: I tasti di scelta rapida diventano inefficaci quando si attiva o disattiva la funzione "**Hover Translation**".
- Migliorato: Migliorata la visualizzazione della traduzione bilingue multilinea su Twitter e Youtube.
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

- Aggiunto: La **Subtitles Translation** in tempo reale ora supporta l'attivazione tramite "float ball", disponibile su Zoom, Google Meet e Microsoft Teams.
- Risolto: Problemi di sincronizzazione dei sottotitoli su YouTube dopo aver guardato annunci.
- Risolto: Problemi di visualizzazione con il menu di traduzione del tasto destro in Safari su MacOS 15.
- Risolto: Problemi con la funzionalità di annullamento Ctrl+Z nell'**Enhanced input** su alcuni siti web.

## 1.10.6 (2024-10-25)

- Risolto: Problema con i tasti di scelta rapida dell'**Enhanced input** che non si attivano.
- Migliorato: Riduzione delle dimensioni del pacchetto di installazione.
- Migliorato: Soluzione di visualizzazione dei sottotitoli di Netflix.

## 1.10.5 (2024-10-23)

- Aggiunto: Visualizza un avviso quando la lingua di origine e la lingua di destinazione sono le stesse.
- Risolto: Problema di traduzione dei caratteri di spazio nel testo ricco [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175).
- Migliorato: Miglioramento dell'input e della funzionalità di passaggio del mouse all'interno di iframe incorporati nelle pagine web.

## 1.10.2 (2024-10-11)

- Aggiunto: Traduzione di immagini (versione Beta).
- Aggiunto: Modalità Forza Abilitazione Supporto Mouse (Abilita questa funzione solo se la funzione di passaggio del mouse non è disponibile su dispositivi tablet) **Settings** -> **Advanced Settings** -> **Forece Enable Mouse Support**.
- Aggiunto: Visualizza un messaggio di errore quando la traduzione dei sottotitoli video fallisce.
- Risolto: Problema di traduzione del testo ricco [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163).
- Migliorato: Affrontati problemi in cui il pulsante di traduzione potrebbe non funzionare durante la traduzione di PDF.
- Migliorato: Migliorato il rendering delle formule tradotte.
- Migliorato: Elenco di selezione della lingua.

## 1.9.8 (2024-09-28)

- Aggiunto: Servizio di traduzione "Zhipu BigModel".
- Rimosso: Modello "SiliconCloud" qwen1.5-7B-chat (a causa della discontinuità ufficiale).
- Risolto: Risolto problema di compatibilità di accesso con il plugin Safari su macOS 15.

## 1.9.7 (2024-09-20)

- Supporto migliorato per l'input nei campi di Baidu, Gmail e altri
- Supporto per l'header della richiesta anthropic-dangerous-direct-browser-access per l'API di Claude Anthropic
- Supporto per il download dei sottotitoli dai video di Hulu, Bloomberg e Domestika
- DeepX supporta la traduzione di testo ricco
- Risolto il problema con la mancata sincronizzazione degli esperti AI personalizzati

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

- Supporto per la configurazione delle eccezioni per lingue e siti web in modalità di contrasto bilingue o solo traduzione (configurare nella pagina Impostazioni -> Impostazioni avanzate). Ad esempio: Se la tua modalità di traduzione predefinita è il contrasto bilingue, ma non desideri che il cinese tradizionale utilizzi anche il contrasto bilingue, puoi aggiungere il cinese tradizionale alle lingue di eccezione per il contrasto bilingue, in modo che il cinese tradizionale utilizzi la modalità solo traduzione per la traduzione. Allo stesso modo, se la tua modalità di traduzione predefinita è solo traduzione, ma desideri che una certa lingua o sito web utilizzi la modalità di contrasto bilingue, puoi anche aggiungere quella lingua o sito web alle lingue di eccezione.
- Risolto un problema in cui la casella di input nell'interfaccia dei messaggi privati di Tiktok veniva tradotta in modo errato
- Risolto un problema in cui i fumetti su Read Comic Online non potevano essere tradotti
- Risolto un problema in cui [Impostazioni avanzate -> Numero minimo di caratteri richiesti per tradurre un paragrafo] non aveva effetto in alcuni casi

## 1.8.4 (2024-08-30)

- Il servizio di traduzione DeepL ora supporta ufficialmente il cinese tradizionale come lingua di destinazione (in precedenza, la traduzione in cinese tradizionale con DeepL comportava un processo di conversione aggiuntivo da cinese semplificato a cinese tradizionale tramite terze parti).
- Ottimizzata la performance della traduzione di testo ricco.

## 1.8.3

- Google Meet ora supporta i sottotitoli bilingue per le riunioni dal vivo: Ora puoi goderti la funzione di sottotitoli bilingue nelle riunioni di Google Meet. Basta aprire il link della riunione, attivare i sottotitoli bilingue nel pannello di traduzione immersiva e poi aggiornare la pagina per sperimentarlo.
- Aggiunta l'opzione per "Segnalare problemi di traduzione della pagina web corrente" e l'opzione per "Attivare/disattivare rapidamente la sfera fluttuante" nelle opzioni aggiuntive del pannello.
- Dopo aver regolato la posizione dei sottotitoli bilingue di YouTube, il sistema ricorderà automaticamente la nuova posizione.
- Ottimizzata la logica della cache del plugin, ora cancellando automaticamente i dati della cache che hanno più di 30 giorni.
- Ottimizzati i blocchi di codice all'interno dei paragrafi per un ripristino più accurato del testo originale.
- Migliorata la gestione delle "parole non traducibili" nelle impostazioni avanzate.

## 1.8.2

- Ora puoi tradurre il testo nelle caselle di input con il clic destro: Seleziona qualsiasi testo in una casella di input su una pagina web, fai clic destro per scegliere traduci, e la traduzione immersiva tradurrà automaticamente il testo selezionato nella lingua di destinazione della casella di input, rendendo conveniente tradurre rapidamente il testo nella lingua nativa in altre lingue.
- Ora puoi segnalare rapidamente i problemi di traduzione delle pagine web nella sfera fluttuante della traduzione immersiva. Dopo aver tradotto una pagina web, se ci sono problemi, puoi cliccare sul pulsante [Feedback] sul lato destro della sfera fluttuante, compilare la descrizione del problema, e ce ne occuperemo il prima possibile.
- I file Epub ora supportano la traduzione di testo ricco (cioè, preservando il formato del testo originale di ogni paragrafo, come link, grassetto, ecc.)
- Supporto per sottotitoli bilingue in tempo reale nelle riunioni video della versione web di Microsoft Teams (Apri il link della riunione di Teams, attiva i sottotitoli bilingue nel pannello di traduzione immersiva e poi aggiorna)
- Ottimizzati i sottotitoli bilingue per la versione inglese di iQIYI (iq.com)
- Fornite più carte arXiv con layout di traduzione bilingue ottimizzato
- A causa delle restrizioni del sito web di Youtube, lo script di Tampermonkey per Chrome non supporta più i sottotitoli bilingue di Youtube. Si prega di utilizzare la [versione del plugin](https://immersivetranslate.com/).

## 1.8.1

- Risolti problemi di traduzione con lo script di Tampermonkey SiliconCloud
- La traduzione Claude ora supporta il tibetano e consente la configurazione del parametro Temperature
- La pagina dei dettagli dell'esperto AI mostra i prompt utilizzati dall'esperto
- Le impostazioni di scorciatoia ora consentono di assegnare tasti di scelta rapida unici per qualsiasi servizio di traduzione
- Ottimizzato il rilevamento delle traduzioni dei documenti arXiv

## 1.7.9

- Risolti problemi con la traduzione di testo ricco per servizi di traduzione come Google, DeepL (ad esempio, pagine che visualizzano direttamente `<button>` ecc.)
- Risolto il problema in cui la scorciatoia bilingue per i video di YouTube non poteva essere disattivata.

## 1.7.8

- DeepL, Microsoft Translate, Google Translate, OpenAI, Claude, Gemini e altri servizi di traduzione supportano la traduzione per mantenere il formato del testo originale (ad esempio, link, grassetto, ecc.)
- Dopo aver selezionato il testo, il menu del clic destro cambierà in [Traduci il testo], cliccando su di esso si può automaticamente saltare alla pagina di traduzione del testo immersiva
- Nuovo servizio di traduzione gratuito per grandi modelli: SiliconCloud, disponibile per tutti gli utenti.
- Aggiunto il modello di traduzione Zero-One-Thing, che può essere utilizzato compilando l'API Key dopo essersi registrati sulla piattaforma Zero-One-Thing.
- Nuovo pulsante di feedback utente per la traduzione di manga (dopo aver tradotto un manga, clicca sul pulsante [Feedback] sul lato destro della sfera fluttuante per dare feedback sulla qualità della traduzione).

## 1.7.7

- Adottato algoritmo di suddivisione intelligente delle frasi AI per sottotitoli inglesi auto-generati su YouTube [Pro Disponibile]
- Ottimizza la traduzione con clic destro in "Traduci in xx lingua di destinazione"
- Supporto per l'integrazione immersiva [JS SDK](https://immersivetranslate.com/docs/js-sdk/) per siti web di terze parti
- Ottimizza la visualizzazione dei sottotitoli di Hulu
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
- Aggiunto supporto per nuovi siti nella traduzione di fumetti:
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
- I sottotitoli bilingue di YouTube ora supportano la suddivisione intelligente delle frasi (Beta) (Solo quando si abilita manualmente la traduzione immersiva dei sottotitoli di YouTube in [Impostazioni] - [Sottotitoli Video], e i sottotitoli video originali sono sottotitoli inglesi auto-generati)
- Aggiunto il servizio di traduzione Tencent [【Hunyuan Large Model】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- Risolvi i problemi di layout del testo delle traduzioni di fumetti per le lingue in script latino.
- Nuovi siti supportati per la traduzione di fumetti:
  - COMIC FUZCOMICFUZ(https://comic-fuz.com/)
  - MangaDexMangaDex(https://mangadex.org/)
  - KuaiKan ComicsKuaiKanComics(https://www.kuaikanmanhua.com/)
- Risolto un problema in cui i servizi AI personalizzati non potevano selezionare esperti AI.

## 1.6.4

- Quando gli esperti AI sono utilizzati per la "Selezione Intelligente", diversi esperti AI possono essere personalizzati per diversi siti web. Questo può essere impostato in [Impostazioni] -> [Esperti AI] -> [Inserisci qualsiasi esperto].
- Risolto il problema in cui i sottotitoli non vengono visualizzati su YouTube in modalità "Solo Traduzione".
- Risolto il problema dei sottotitoli bilingue non funzionanti su Mubi.
- Compatibile con i PDF aperti con il plugin Adobe Acrobat.
- Tutti gli utenti possono [contribuire online](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/) alla traduzione multilingue dell'interfaccia di traduzione immersiva.

## 1.6.3

- Nuova funzionalità: traduzione di manga (Beta), nei siti web di manga supportati, apparirà un pulsante di traduzione di manga sotto la sfera fluttuante di traduzione rapida della pagina web. Cliccandolo si attiverà la traduzione di manga. Questa funzionalità è disponibile per i membri Pro (500 pagine al mese, pacchetti aggiuntivi possono essere acquistati), attualmente supportando i seguenti siti:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)

## 1.6.2

- Nuova funzionalità: traduzione Manga (Beta), nei siti web di manga supportati, un pulsante di traduzione manga apparirà sotto la sfera di traduzione rapida della pagina web. Cliccandolo si attiverà la traduzione manga. Questa funzionalità è disponibile per i membri Pro (500 pagine al mese, pacchetti aggiuntivi possono essere acquistati), attualmente supporta i seguenti siti:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- Nuova funzionalità: la traduzione AI supporta il [modello grande Doubao](https://www.volcengine.com/product/doubao)
- Nuova funzionalità: supporto per la modalità di confronto bilingue con traduzione prima e testo originale a seguire, che può essere abilitata nella pagina delle impostazioni -> impostazioni avanzate.
- La lista dei modelli AI personalizzati supporta la sintassi `-all`, che può eliminare tutti i modelli preimpostati.
- Nei sottotitoli bilingue dei video, quando la lingua di destinazione è il cinese semplificato e il testo originale è in cinese tradizionale, il testo originale verrà automaticamente convertito in cinese semplificato, e viceversa.
- Risolto il problema per cui il collegamento rapido della sfera fluttuante non poteva tradurre su iOS 18.
- Risolto il problema per cui i Prompts personalizzati erano inefficaci quando ne venivano utilizzati troppi.

## 1.6.1

- Supporta la piattaforma di modelli grandi Baidu Qianfan, la piattaforma di modelli grandi Alibaba Bailian, la piattaforma di modelli grandi DeepSeek.
- Risolto il problema per cui la modifica della lingua di destinazione e altre impostazioni nel pannello popup si resettava al cliccare sulla sfera fluttuante di traduzione.

## 1.5.8

- Gli esperti AI supportano la modalità "Selezione Intelligente", in cui il sistema selezionerà automaticamente l'esperto AI più adatto in base al sito web corrente (ad esempio, gli esperti AI legati alla tecnologia verranno selezionati automaticamente per The Verge e Hacker News, mentre il miglioramento della traduzione di Twitter verrà selezionato automaticamente per Twitter).

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

- Risolto il problema per cui le modifiche al prompt generale dell'esperto sovrascrivevano il prompt dell'esperto AI specificato [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- Il nome del modello AI personalizzato supporta la sintassi avanzata, usa + per aggiungere un modello, usa - per nascondere un modello, e usa model_name=display_name per personalizzare il nome visualizzato del modello, ad esempio: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- Risolto l'errore restituito da Gemini
- Nascondi la sfera fluttuante quando si stampa la pagina
- Risolto il problema per cui la dimensione del font non si ridimensionava proporzionalmente quando YouTube era a schermo intero [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- Supporto per i servizi di traduzione AI per impostare [AI Expert] per specificare la strategia di traduzione, attualmente una funzionalità Beta, che può essere abilitata in [Impostazioni Sviluppatore](https://dash.immersivetranslate.com/#developer) dopo aver abilitato Beta, e il menu [AI Expert] può essere visto dopo il refresh.
- I servizi di traduzione AI possono ora personalizzare la lista dei modelli, come [OpenAI], il sistema ha solo alcuni dei modelli più comunemente usati integrati. Cliccando sulla lista a discesa del modello, l'ultimo elemento che vedi è [Imposta Più Modelli], dopo l'impostazione, verrà automaticamente ricordato per la comodità degli utenti che testano diversi modelli personalizzati.
- Ottimizzata l'incoerenza nel layout delle traduzioni in alcuni casi.
- Aggiunto un pulsante di reset per lo stile dei sottotitoli di YouTube, che può rapidamente ripristinare lo stile predefinito.
- Risolto il problema per cui i sottotitoli cinesi non potevano essere scaricati su YouTube.
- Ottimizzata la copia dell'interfaccia in cinese tradizionale.

## 1.4.12

- Risolto il problema della finestra di dialogo dei messaggi non tradotta quando si apriva la pagina di Reddit
- Aggiunta una funzionalità temporanea per abilitare la modifica della traduzione nella voce "Altro" del pannello
- Risolto il problema per cui YouTube Shorts senza sottotitoli mostrava sempre i sottotitoli del video precedente [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
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
- Implementa il supporto all'internazionalizzazione (i18n) per la navigazione dei documenti della pagina
- YouTube introduce una funzionalità per abilitare temporaneamente i sottotitoli bilingue
- YouTube supporta il download di sottotitoli bilingue (solo per membri)
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
- I sottotitoli bilingue di Udemy compatibili con la visualizzazione mobile
- Il servizio di traduzione Gemini è nascosto per impostazione predefinita, può essere abilitato nelle impostazioni sviluppatore per mostrare la beta di questo servizio di traduzione

## 1.3.4

- Supporto per il servizio di traduzione gratuito Yandex
- Ottimizzati i prompt di Gemini
- I sottotitoli video supportano l'impostazione per la visualizzazione bilingue/originale e traduzione
- Supporto per lo spazio tra cinese e inglese nei risultati di traduzione OpenAI
- L'interruttore del pannello per visualizzare solo il pulsante di traduzione modificato per avere effetto solo sulla pagina corrente

## 1.3.3

- Ottimizzato il problema di visualizzazione della traduzione dei sottotitoli video CC di Twitter.
- Il servizio DeepL ha aggiunto il supporto per l'arabo.
- Il servizio di traduzione Colorful Clouds ora supporta coreano, spagnolo, francese e russo.
- Il servizio OpenAI ha aggiunto il supporto per il dialetto cinese nordorientale.
- Il rilevamento automatico del pannello ora visualizza la lingua originale.
- Regolata la descrizione della scorciatoia per il pannello mobile.

## 1.3.2

- Risolto il problema per cui il pannello di controllo non poteva essere chiuso su dispositivi mobili

## 1.3.1

- La piattaforma di sottotitoli video supporta [DeepLearning.ai](https://learn.deeplearning.ai)
- Supporto per la traduzione di pagine web e sottotitoli video in lingue come arabo, ebraico, ecc., affrontando problemi di visualizzazione RTL (da destra a sinistra)
- Risolto il problema della traduzione di Gemini in ebraico
- Risolto un problema per cui alcuni sottotitoli in cinese tradizionale su YouTube non potevano essere visualizzati correttamente
- Risolto il problema di visualizzazione dei sottotitoli di Twitter su Safari
- Risolto il collegamento per la traduzione immediata in fondo alla pagina

## 1.2.4

- Risolto il problema per cui i segnaposto nella creazione di ePub non venivano sostituiti correttamente
- Supporto per la traduzione dei sottotitoli video [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- Ottimizzata la frequenza di controllo delle richieste del servizio di traduzione
- Le recenti richieste al servizio di traduzione Microsoft dalla Cina sono state instabili; quando si verificano errori, il sistema rileva automaticamente il servizio di traduzione attualmente disponibile, consentendo agli utenti di passare rapidamente.
- Ottimizzato il messaggio di errore per errori di rete
- Risolto il problema per cui la configurazione del colore del testo non supportava l'anteprima RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Risolto il problema per cui l'aggiornamento della versione del plugin Safari mostrava sempre la pagina di successo dell'installazione
- Microsoft ha aggiunto il supporto per il vietnamita
- Risolto il problema per cui i sottotitoli tradotti sul sito edx non venivano visualizzati

## 1.2.2

- Supporto alla traduzione dei sottotitoli video per [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). Supporta anche la traduzione di alcuni video con sottotitoli CC su Twitter.
- Ottimizzati i popup di errore, i popup di errore di problemi di rete rilevano automaticamente i servizi di traduzione gratuiti validi.
- Risolto il supporto dell'app iOS immersiva per la riproduzione a schermo intero su YouTube.
- Risolto il problema di traduzione dei paragrafi con Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Supporto alla traduzione dei sottotitoli video per [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/).
- Risolto un problema per cui alcuni utenti Pro non potevano modificare le impostazioni nel browser Chrome.
- Supportata la visualizzazione di sottotitoli bilingue nella modalità a schermo intero di YouTube su iOS.

## 1.2.0

- Supporto per la traduzione dei sottotitoli video sulle piattaforme [LinkedIn](https://www.linkedin.com/) e [Viu](https://www.viu.com/).
- Aggiunto un accesso rapido ai sottotitoli video per ulteriori piattaforme.
- Supporto per impostare siti web/lingue specifici per visualizzare solo il testo tradotto.
- Risolto un problema per cui la pagina delle impostazioni continuava a mostrare il caricamento in alcuni casi su Safari.
- Supporto per la traduzione dei nodi del tag di input.
- Ottimizzata l'interfaccia utente del popup di errore.

## 1.1.9

- Supporto alla traduzione dei sottotitoli per YouTube Live e la piattaforma [Mubi](https://mubi.com/).
- Ottimizzazione: Pagina delle impostazioni, interfaccia utente della lista URL (per evitare ambiguità, le caselle di controllo non sono visualizzate di default).
- Supporto per impostare il font di traduzione in modalità solo traduzione.
- Aggiunto un accesso rapido per abilitare i sottotitoli video su Netflix, Ted, Bloomberg, Udemy, Coursera.
- Risolto: Alcuni stili tradotti (come le sottolineature) non erano efficaci su Safari.
- Risolto: Durante la traduzione della pagina, il problema per cui il passaggio del mouse non attivava la ritraduzione.

## 1.1.8

- Aggiunta un'opzione per il servizio di traduzione secondario per seguire il servizio di traduzione principale
- Supporto per sottotitoli bilingue per [Amazon Prime Video](https://www.primevideo.com)
- Ulteriore ottimizzazione della funzione di traduzione PDF incorporata in Sci-Hub
- Risolto un problema con i PDF online che non si aprivano correttamente
- Risolto il problema con la riproduzione continua di sottotitoli bilingue su Netflix

## 1.1.7

- Ora è possibile specificare un font per la traduzione nella pagina delle impostazioni -> [Impostazioni di base] -> [Stile di traduzione]
- Aggiunta una configurazione di scorciatoia per [Traduci paragrafo specificato] nel pannello a sfera mobile sui dispositivi mobili
- Ottimizzata la sensibilità del rilevamento del passaggio del mouse su Ctrl per evitare di confondere `Ctrl+C` con `Ctrl`
- Aggiunto supporto per una nuova impostazione di scorciatoia che consente di attivare rapidamente se i sottotitoli video utilizzano i sottotitoli di traduzione automatica integrati
- Sul sito web di Sci-Hub, cliccando sulla sfera mobile si tradurranno i PDF incorporati nella pagina web

## 1.1.6

- **Supporto mobile per la traduzione di paragrafi specifici:** La versione mobile ora supporta la traduzione di paragrafi specificati e ha aggiunto una varietà di operazioni di scorciatoia, tra cui scorrimento a sinistra, scorrimento a destra, doppio tocco, triplo tocco e gesti multi-dito. Questi non sono abilitati di default e richiedono che l'utente selezioni attivamente il gesto di attivazione nella pagina delle impostazioni sotto [Passaggio del mouse].
- **Aggiornamento della versione predefinita di Gemini:** La versione predefinita è ora `v1beta`.
- **Risolta la traduzione del cinese classico:** Risolta la funzionalità di traduzione del cinese classico di Microsoft e OpenAI.
- **Ottimizzazione della traduzione giapponese:** Ulteriormente ottimizzata la traduzione giapponese di OpenAI per migliorare l'accuratezza e la fluidità.
- **Esperienza di traduzione immersiva:** Per adattarsi meglio alle abitudini degli utenti, abbiamo spostato la scorciatoia per i sottotitoli bilingue in modalità a schermo intero sulla piattaforma YouTube a sinistra.

## 1.1.5

- Risolto il problema per cui il menu a discesa in modalità scura su Windows non aveva colore.
- Risolto il problema di allineamento con l'opzione "Altro" non allineata a sinistra su Windows.

## 1.1.4

- **Aggiornamento dell'interfaccia utente del pannello popup:** Il nuovo design mira a migliorare l'usabilità e la comprensibilità. Questo aggiornamento include:

  - **Nuove funzionalità nel menu principale:**
    - **Interruttore modalità bilingue/solo traduzione:** Ora puoi passare tra "Modalità traduzione bilingue" e "Modalità solo traduzione" direttamente nel menu principale, situato a sinistra del pulsante di traduzione.
    - **Voce di traduzione documenti:** L'ingresso per tradurre "file PDF/ePub/sottotitoli" è stato spostato nel menu principale per un accesso rapido.
    - **Impostazioni di traduzione video:** L'ingresso per le impostazioni di "Traduzione video" è stato anche posizionato nel menu principale per regolazioni rapide.
    - **Nuova voce per la documentazione d'uso:** Fornisce guide operative dettagliate e documenti di aiuto.

- **Voce di traduzione documenti integrata:** Ora puoi tradurre file PDF, ePub e sottotitoli tramite un ingresso di caricamento unificato. Basta cliccare sul pulsante [PDF/ePub] nel pannello popup, non è più necessario selezionare [Altro].

- **Aggiunto supporto per 5 siti web video:**
  - Supporto per i sottotitoli dei podcast su Youtube Music.
  - Aggiunto supporto per il sito web iview.abc.net.au.
  - Aggiunto supporto per il sito web www.nma.art.
  - Aggiunto supporto per il sito web creativecloud.adobe.com.
  - Aggiunto supporto per il sito web www.masterclass.com.

## 1.1.3

- Risolto il problema di visualizzazione anomala del plugin mobile quando si aprono pagine PDF.
- Ottimizzato l'effetto di traduzione delle conversazioni GPT.
- Supportata la traduzione di dominio per Baidu Translate.
- Aggiunta una modalità solo traduzione nella pagina delle impostazioni.
- Aggiunta una funzione di promemoria quando si cambia modalità di traduzione con scorciatoie.
- Risolto il problema per cui la traduzione dei campi di input contenenti URL traduceva solo parti del contenuto.

## 1.1.2

- Risolto: Il problema per cui il cambio di servizi di traduzione non aveva effetto quando la pagina non era ancora stata tradotta.
- Ottimizzazione: Nel processo di traduzione di Epub e PDF, se alcuni contenuti non riescono a essere tradotti, ora è possibile passare a un altro servizio di traduzione sul pannello senza riavviare l'intero processo di traduzione (la logica precedente era di utilizzare immediatamente un nuovo servizio di traduzione per ritradurre l'intero libro). Ciò significa che a metà della traduzione, puoi passare a un diverso servizio di traduzione e cliccare su [Riprova tutti i paragrafi falliti], dopodiché il sistema continuerà la traduzione utilizzando il nuovo servizio.
- Ottimizzazione: Regolata la dimensione del carattere dei messaggi di errore di traduzione per migliorare la leggibilità.

## 1.1.1

- Risolto il problema della scorciatoia dei sottotitoli bilingue per YouTube con testo inglese eccessivamente lungo.

## 1.1.0

### Nuove Funzionalità

- **Impostazioni Scorciatoie:** Aggiunto un nuovo menu di primo livello "Scorciatoie" e le seguenti funzioni di scorciatoia personalizzabili:

  - Designare una combinazione di tasti per tradurre il contenuto della casella di input corrente, integrando il metodo precedente di premere rapidamente la barra spaziatrice tre volte.
  - Designare una combinazione di tasti per abilitare temporaneamente la "traduzione diretta al passaggio del mouse" sulla pagina. Premendolo di nuovo si annullerà questa funzione.
  - Aggiunte scorciatoie dedicate per 6 servizi di traduzione (come DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation) per facilitare il passaggio temporaneo tra i servizi di traduzione.

- **Aggiornamento dell'interfaccia utente della pagina delle impostazioni del plugin**:

  - In "Impostazioni avanzate", è stata aggiunta una nuova opzione per consentire agli utenti di specificare alcune parole (ad esempio, "LLM") da escludere dalla traduzione.
  - In "Impostazioni avanzate", è stata aggiunta una nuova opzione per configurare il numero minimo di caratteri richiesti per tradurre un paragrafo. Il default è 4 caratteri, ma può essere impostato più alto (ad esempio, 20), in modo che solo i paragrafi più lunghi vengano tradotti.
  - Aggiunto un tutorial per principianti, che copre le impostazioni della sfera mobile, le impostazioni dei sottotitoli video e le impostazioni del passaggio del mouse.

- **Sottotitoli Bilingue YouTube:** Aggiunto un accesso rapido nella finestra di riproduzione video di YouTube per abilitare o nascondere i sottotitoli bilingue (questa funzione può essere disattivata).

- **Supporto Lingua Deepl:** Aggiunto supporto per il portoghese (Brasile).

- **Guida per Nuovi Utenti:** Quando i nuovi utenti aprono per la prima volta una pagina in una lingua non target, viene visualizzata una bolla di guida di aiuto della sfera mobile.

### Ottimizzazione e Correzioni

- **Ottimizzazione UI:** Ridisegnata l'interfaccia utente per i messaggi di errore di traduzione della pagina per renderli più facili da comprendere. Quando ci sono molti errori, un popup avviserà attivamente l'utente.

- **Correzioni di Bug**:

  - Risolto il problema per cui la traduzione al passaggio del mouse falliva quando la pagina perdeva il focus.
  - Risolto il problema per cui meno di 3 caratteri nella funzione di miglioramento della casella di input non venivano tradotti.
  - Risolto il problema per cui alcune directory non venivano tradotte durante la produzione di Epub bilingue.

- **Rimozione di Funzionalità:** Rimossa la funzione di miglioramento delle informazioni bilingue (visualizzazione simultanea dei risultati di ricerca in inglese sulle pagine di ricerca di Google).

### Altri Aggiornamenti

- **Aggiornamento Configurazione openAI:** Ora supporta l'impostazione del numero di configurazioni al secondo in decimali, come 0.5, che significa 1 richiesta ogni 2 secondi.

## 0.12.14

- Risolto: Il problema di riconoscimento della lingua target predefinita su alcune macchine dopo la prima installazione.
- Ottimizzazione: L'ordine predefinito dei titoli delle pagine web è cambiato in [Cinese - Inglese].

## 0.12.13

- Risolto: Problema con la cucitura della traduzione di paragrafi lunghi di OpenAI in alcuni casi. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Ottimizzato: Quando si utilizza il passaggio del mouse, il problema per cui la perdita di focus sulla pagina e poi il riattivamento diventano inefficaci.
- Risolto: Il problema per cui la cache esiste ancora dopo aver modificato il prompt/modello in OpenAI.

## 0.12.12

- Aggiornato: Ottimizzato il pannello popup, rimuovendo alcune opzioni per il sito web corrente.
- Ottimizzato: Migliorato il processo di fusione dei sottotitoli manuali.
- Ottimizzato: Impostazione automatica della lingua di destinazione basata sulla lingua del browser.
- Aggiunto: Supporto per sottotitoli bilingue per la piattaforma di apprendimento [ArtStation](https://www.artstation.com/learning) e [ZDF](https://www.zdf.de/).
- Risolto: Risolto il problema per cui i titoli nella pagina dell'elenco jstor non venivano tradotti [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Risolto: Risolto il problema per cui solo una parte del contenuto scompariva su Hacknews [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Aggiunto supporto per sottotitoli bilingue per le piattaforme [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/), e [Domestika](https://www.domestika.org).

## 0.12.10

- Risolto il problema di autorizzazione del dominio Gemini sotto lo script Tampermonkey.
- Supportata la traduzione in tempo reale dei sottotitoli per Twitter Space.
- Per le versioni precedenti dello script Tampermonkey, è stato ora aggiunto un avviso di aggiornamento nella pagina delle impostazioni.

## 0.12.9

- Aggiunto supporto per la traduzione Gemini.
- Risolto il problema per cui le traduzioni non rispondevano in tempo quando la pagina web veniva scorsa fino alla posizione centrale in alcuni casi.
- Risolto il bug per cui il cambio di sottotitoli su alcuni siti video causava la visualizzazione ripetuta della traduzione.
- Risolto il problema per cui il mouse si posizionava per continuare a tradurre senza tenere premuto il tasto di scelta rapida in alcuni casi.
- Su macOS, ottimizzato il nome visualizzato del pannello di scelta rapida.

## 0.12.8

- Riparato il problema per cui i sottotitoli video originali non venivano visualizzati quando "Il sito corrente è impostato per non tradurre mai".
- Riparato il conflitto con alcuni plug-in che causavano un ritorno infinito della pagina.
- Riparato la non traduzione di alcuni paragrafi dopo aver attivato l'interruzione di riga per paragrafi lunghi.
- Risolto [Quando si attiva temporaneamente la traduzione della pagina web per un lungo periodo, cliccando sul pannello [Traduci sempre questo sito web] non si annulla la traduzione sempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Aggiunti sottotitoli bilingue per supportare le piattaforme [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) platforms. https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/) Platforms
- La hoverball è ora nascosta per impostazione predefinita quando il video è a schermo intero.
- Risolto il problema di clic instabile del pannello di azione hoverball della pagina di Firefox.
- Supporto per la collaborazione sotto il sito pubmed.ncbi.nlm.nih.gov e il plugin scholarscope
- Risolto il problema di instabilità della pagina di traduzione della casella di input di reddit

## 0.12.6

- Risolto il problema per cui la traduzione di YouTube/Web of Science ecc. non era sensibile quando si cambiavano le schede.
- Hoverball su mobile ora supporta l'operazione di pressione lunga, pressione breve per tradurre, pressione lunga per aprire il pannello.
- Traducendo eBook bilingue ora verrà tradotto anche l'indice.
- La funzione di miglioramento della ricerca (alcune pagine di Google Search mostrano risultati di ricerca bilingue) ora non è abilitata per impostazione predefinita e verrà rimossa nel prossimo Release.

## 0.12.5

- Risolto il problema di creazione di eBook Epub dal pannello cliccando sulle traduzioni non funzionanti

## 0.12.4

- Quando si attivano i sottotitoli bilingue nel pannello, la pagina verrà prima aggiornata automaticamente (per visualizzare i sottotitoli bilingue in modo più accurato), e alcuni siti richiedono ancora agli utenti di cliccare manualmente sul pulsante "CC" sul sito per attivare i sottotitoli.
- Ottimizza Grease Monkey, rilevamento della lingua Safari
- Fornisce un accesso rapido alle versioni bilingue di tutti i documenti sul sito di documenti [Arxiv](https://arxiv.org/abs/1910.06709).
- [Supporto hoverball configurato per essere fissato a sinistra #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Risolto il problema di visualizzazione della modalità di apprendimento #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Attivare temporaneamente la traduzione web per un periodo di tempo non annulla Traduci sempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Ottimizza i problemi di inizializzazione del file PDF

## 0.12.3

- Risolto il problema per cui la funzione [disabilita permanentemente i sottotitoli video] non funzionava [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)

## 0.12.2

- È fornito il supporto per sottotitoli bilingue per più piattaforme video, che ora sono supportate: [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy] (https://www\.khanacademy.org/), [Coursera] (https://www\.coursera.org/), [Vimeo] (https://vimeo.com/), [Nebula] (https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), ecc. (Nota che a causa delle limitazioni tecniche, alcuni siti web devono aggiornare la pagina dopo aver attivato i sottotitoli bilingue per la prima volta o attendere che la traduzione sia completata per visualizzare i sottotitoli bilingue). (Nota che a causa delle limitazioni tecniche, alcuni siti web devono aggiornare la pagina dopo aver aperto i sottotitoli bilingue per la prima volta, o devono attendere che la traduzione sia completata per visualizzare i sottotitoli bilingue)
- Ottimizzato significativamente la dimensione del file zip del plugin, ridotto della metà rispetto all'originale, download e aggiornamento più veloci.
- Risolto il problema di download esteso dei PDF
- Aggiunto un portale PDF di traduzione rapida sul lato destro del sito di documenti [Arxiv](https://arxiv.org/abs/1910.06709), che porta a una pagina HTML pulita (supportata solo da alcuni documenti, poiché richiede agli autori originali di inviare il codice sorgente, quindi circa il 50% dei documenti mostrerà questo portale)
- Le pagine PDF online senza estensione .pdf ora possono saltare direttamente alla pagina di traduzione PDF cliccando sulla hoverball sulla pagina.
- Risolti alcuni problemi di miglioramento della casella di input sotto Safari
- Ottimizza il rilevamento della lingua in Grease Monkey e Safari

## 0.11.6

- Aggiunte 11 nuove lingue di interfaccia per il plugin e il sito ufficiale, ora le lingue di interfaccia supportate raggiungono 14, tra cui cinese semplificato, cinese tradizionale, inglese, giapponese, coreano, russo, spagnolo, portoghese, hindi, italiano, tedesco, francese, arabo e persiano.
- Modifica della condivisione bilingue (modalità di aggiornamento) aggiunta nella versione precedente alla condivisione di snapshot di pagina bilingue, in modo che il contenuto condiviso sia più originale, oltre a una maggiore adattabilità.
- Risolto il problema degli emoji alla fine della casella di input di Twitter che non possono essere tradotti
- Risolto il problema per cui il contenuto di plug-in di terze parti veniva tradotto in alcuni scenari
- Riparato il clic non reattivo della hoverball PDF online

## 0.11.5

- Ora puoi generare un link pubblico alla pagina bilingue tradotta per Immersive Translate.
  - [Clicca](/docs/share/) sull'icona di condivisione di Immersive Translate per generarlo con un solo clic!
- Risolto il problema per cui alcune piattaforme non riuscivano a riconoscere se il mouse era supportato o meno
  - Ci sono alcuni browser desktop che supportano sia touchscreen che mouse, e Immersive Translate non è tecnicamente in grado di rilevare se tali piattaforme supportano il mouse, quindi abbiamo aggiunto l'opzione [Forza abilitazione supporto mouse] nelle impostazioni [Mouse Hover]

## 0.11.2-0.11.4

- Ottimizza l'esperienza, risolvi alcuni bug

## 0.11.1

- Il modello predefinito per le traduzioni OpenAI è: GPT3.5-turbo-1106.
- Ottimizzato il Prompt cinese per OpenAI, ora meno soggetto a allucinazioni!
- Ridotta la lunghezza dei prompt di OpenAI da 90 a 40, risparmiando ancora più traffico.

## 0.11.0

- Risolto il problema di clic instabile della hoverball della pagina
- Risolti problemi di traduzione Azure

## 0.10.9

- Risolti alcuni problemi minori

## 0.10.8

- Supporto per l'impostazione di pulsanti di traduzione rapida hoverball (supporto sia per PC che per mobile)
- Ottimizzazione del giudizio della lingua di Grease Monkey
- Risolto il problema di traduzione del file txt

## 0.10.7

- Supporto per il passaggio del mouse premendo nuovamente Ctrl per mostrare il testo originale
- Ignora la lingua mai tradotta con il passaggio del mouse
- Ottimizzazione dei sottotitoli bilingue di Youtube

## 0.10.6

- Supporto per la traduzione dei sottotitoli di Youtube solo
- Aggiungi avviso di aggiornamento per versione bassa di Grease Monkey
- Risolto il problema per cui i file txt locali non potevano essere tradotti

## 0.10.5

- Risolto il problema per cui Youtube occasionalmente tornava alla homepage

## 0.10.4

- Risolto il conflitto dei sottotitoli di Youtube con il plugin Dual subtitle (Immersive Translate della traduzione dei sottotitoli di Youtube non è abilitato quando viene rilevato il plugin Youtube Dual per evitare conflitti)
- Aggiunta la [Funzione di disabilitazione permanente dei sottotitoli video], se ci sono altri problemi di conflitto e non si desidera abilitare la funzione di sottotitoli bilingue con Immersive Translate.
- Ottimizza le interruzioni dei sottotitoli

## 0.10.3

- Risolto il problema di traduzione della chiave di autenticazione personalizzata DeppL

## 0.10.3

- Supporto perfetto per i video di Youtube con sottotitoli bilingue 🎉.
- Per le pagine degli articoli, il testo del corpo verrà ora tradotto prima del resto del contenuto della barra laterale
- Ottimizza contestualizzazione della traduzione DeepL
- Ottimizza la traduzione dei file di sottotitoli di OpenAI per la contestualizzazione

## 0.10.1

- Aumenta la priorità della traduzione del corpo per ottimizzare l'esperienza di traduzione
- Risolto il problema del clic su ins più testo non tradotto

## 0.9.8

- Ottimizza l'esperienza, risolvi alcuni bug

## 0.9.7

- Risolto il problema di traduzione automatica quando readwise è evidenziato

## 0.9.6

- Risolto il problema di cancellazione della cache disconnettendo l'accesso dell'utente.

## 0.9.5

- Risolti bug degli eBook online

## 0.9.4

- Ottimizza il rilevamento del miglioramento dell'input per ridurre i tocchi falsi
- Traduzione online di e-book e sottotitoli

## 0.9.3

- Traduzione della Input Box: visualizza un promemoria pop-up quando viene utilizzata per la prima volta, e l'utente può scegliere di disabilitarlo temporaneamente o permanentemente per evitare tocchi accidentali.
- Ottimizzazione della velocità di esportazione della traduzione solo in PDF, se si sceglie di esportare solo la traduzione, è possibile chiamare direttamente l'anteprima PDF del sistema per esportare, più velocemente.
- Deeplx supporta più URL, basta separarli con .

## 0.9.2

- Lo strumento di traduzione PDF è migrato alla versione online: https://app.immersivetranslate.com/pdf/ , in modo che Grease Monkey e Safari possano utilizzare la traduzione PDF, e i problemi possono essere meglio iterati senza la necessità di rilasciare una versione per risolvere il problema.
- Ottimizzazione dell'interfaccia utente POPUP, il pannello è più bello!

## 0.9.1

- Risolto il problema del nome file con la creazione di ebook Epub

## 0.8.8

- Supporto PDF per regolazioni della spaziatura delle righe e delle parole per riconoscere nuovamente i paragrafi
- Risoluzione del problema di scorrimento automatico nella lettura online di epub su dispositivi mobili

## 0.8.7

- Supporto PDF per il download solo della traduzione
- Risolto il problema di accesso a Google su Safari

## 0.8.2 - 0.8.6

- Consente di impostare l'intervallo tra i trigger della combinazione di miglioramento dell'input
- Risolti alcuni bug

## 0.8.1

- Ottimizzazione del rilevamento della lingua
- Funzionalità Beta: API personalizzata (Beta abilitata nelle impostazioni dello sviluppatore)
- Supporto per la traduzione AliCloud
- Risolti alcuni bug

## 0.8.0

- Sistemi utente supportati
- Supporta [Enable Pro Membership](/pricing), che consente agli utenti di usufruire delle traduzioni Deepl e OpenAI e delle impostazioni di sincronizzazione cloud.
- Il servizio di traduzione al passaggio del mouse può essere impostato individualmente
- Il servizio di traduzione della casella di input può essere configurato separatamente
- Ottimizzazione della traduzione PDF
- Risolti alcuni bug

## 0.7.16

- Traduzione PDF con nuove opzioni per il controllo rapido dello stile di traduzione (i file PDF sono molto strani e attivare queste opzioni può essere utile per alcuni file PDF con formattazione disordinata)
- Le versioni iOS e macOS sono tornate sull'Apple Store Country Store

## 0.7.15

- Siamo stati informati da Apple che le traduzioni OpenAI sono state temporaneamente rimosse da iOS e macOS, e stiamo cercando di rilanciarle in Cina.

## 0.7.11- 0.7.14

- Risolto: problema di traduzione di tutte le regioni di Gmail
- Disabilitata temporaneamente la funzione di esportazione PDF di Safari a causa della restrizione di Safari sui download dei plug-in (bug).
- Risolti alcuni altri problemi

## 0.7.10

- Aggiornamento dell'interfaccia utente del pannello dell'icona del browser popup, un po' più di design ～
- Risolto il problema che alcuni passaggi in giapponese non venivano tradotti.

## 0.7.9

- Finalmente il PDF supporta l'esportazione di versioni bilingue! Puoi cliccare sul pulsante [Salva] per esportare il file PDF bilingue tradotto.
- Le regole personalizzate ora supportano la fusione con le regole predefinite integrate, ad esempio: `{"id": "youtube", "selectors.add":["#test"]}` significa aggiungere un `#test` ai selettori esistenti, `selectors` significa sovrascrivere il predefinito, `selectors.remove` significa eliminare uno dei selettori predefiniti, e `selectors.remove` significa eliminare uno dei selettori predefiniti.
- Icona di Safari aggiornata, un po' più grande.
- Altre correzioni di bug

## 0.7.8

- Correzioni di bug

## 0.7.7

- Adattato allo stile di sistema di Safari, l'icona dell'estensione di Safari è cambiata in contorno trasparente.
- Aggiungi il cambiamento di stato dell'icona del browser, quando una pagina web è stata tradotta, un ✅ verrà aggiunto automaticamente nell'angolo in basso a destra dell'icona del browser.
- Abilita automaticamente la traduzione dei siti web inglesi più utilizzati per i nuovi utenti
- Risolto il problema di traduzione con https://claude.ai/

## 0.7.6

- Supporto migliorato per la traduzione dei risultati ctrl+z Annulla
- Supporto alla traduzione in modalità di lettura documenti Flying Book
- Adattamento https://pi.ai/talk

## 0.7.5

- Risolto il problema dell'icona di Grease Monkey non visualizzata
- Risoluzione di numerosi problemi

## 0.7.4

- Risoluzione di numerosi problemi
- La pagina di configurazione supporta l'eliminazione in batch degli URL selezionati.
- Supporta l'abilitazione/disabilitazione della traduzione dei sottotitoli di Youtube per prevenire conflitti con altri plugin correlati.
- Arigato Translator supporta l'impostazione di campi e ID terminologia

## 0.7.2

- Miglioramento della casella di input: consente di omettere il prefisso // e attivare la traduzione dell'intera casella di input con 3 spazi, oppure è possibile disattivare questa opzione nella pagina delle impostazioni.

## 0.7.1

- Supporto al miglioramento della ricerca, quando abilitato, quando si cerca su Google/Google News in cinese, la colonna di destra mostrerà automaticamente i risultati di ricerca delle parole chiave inglesi corrispondenti, che è abilitato per impostazione predefinita.
  - Motivo: Abbiamo scoperto che nella ricerca su Google, i risultati di ricerca per le parole chiave cinesi e inglesi possono essere molto diversi, con il miglioramento della ricerca tradotta immersiva abilitato, cerchiamo automaticamente le stesse parole chiave in inglese per te e le visualizziamo sul lato destro. Puoi scegliere di disabilitarlo se non hai bisogno della funzione.
  - Safari non è supportato a causa delle limitazioni dell'API.

## 0.6.20

- Modifica delle impostazioni predefinite: a causa del feedback di un gran numero di utenti che non utilizzeranno lo strumento di traduzione dopo l'installazione, la loro aspettativa dello strumento di traduzione è che traduca automaticamente le pagine web in inglese dopo l'installazione, quindi da questa versione in poi, per gli utenti cinesi, l'opzione di tradurre le pagine in inglese per impostazione predefinita è stata attivata (se l'utente ha avuto una precedente impostazione della lingua che verrà sempre tradotta, allora verrà rispettata, e la modifica modifica solo le impostazioni iniziali dell'estensione), e deve essere annullata, può essere facilmente annullata nel [pannello popup o nella pagina delle impostazioni](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- Risolti bug PDF
- Risolto bug del web of science
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

- Aggiungi visualizzazione della pagina senza permessi PDF
- Ripara la visualizzazione dei paragrafi dell'elenco di testo PDF
- Ingrandisci la scala dei piccoli font PDF su Chrome e Safari

## 0.6.15

- Ripara il problema che quando si aprono file PDF, il pannello dell'estensione avvisa che non ci sono permessi.
- Risolto il problema che il miglioramento della casella di input non è abilitato quando il sito è impostato per non tradurre mai.

## 0.6.14

- Ottimizzazione della traduzione PDF, l'area di traduzione può ora essere modificata/trascinata/eliminata
  - Trascina in alto a sinistra, elimina in alto a destra, cambia dimensione in basso a destra
- Allineamento a sinistra della casella a discesa di Windows
- Supporto per cinese tradizionale e cinese semplificato

## 0.6.13

- Risolto il problema della traduzione ripetuta al passaggio del mouse
- Supporto alla traduzione PDF per trascinare per cambiare la dimensione e modificare il contenuto della traduzione

## 0.6.12

- Risolto il problema delle immagini di traduzione Epub che diventano più piccole in alcuni browser
- Ottimizzata la traduzione della casella di input, ora funziona senza problemi in Bard!

## 0.6.10

- Modello predefinito OpenAI cambiato alla versione 0613
- Risolti alcuni stili della casella di input
- Più intelligente nel determinare se è un'area di navigazione, e in tal caso, non viene eseguita alcuna traduzione
- Risolto possibile attacco di iniezione XSS

## 0.6.8

- Il pannello dell'estensione può ora indicare pagine non supportate (ad esempio pagine senza permessi e pagine non HTML)
- Miglioramento della casella di input per mostrare lo stato di caricamento nella traduzione
- Aggiorna i colori di caricamento predefiniti nelle traduzioni
- Quando la casella di input è configurata senza prefisso, supporta la traduzione `ja Hello` in giapponese e `English Hello` in inglese.

## 0.6.6

- Risolto: alcune aree non tradotte (quora)

## 0.6.5

- Ottimizzazione di Google Bard
- La traduzione della casella di input supporta la traduzione diretta dell'intera casella di testo senza prefissi.
- Ottimizza il problema delle traduzioni OpenAI che aggiungono punti senza motivo, (se non viene rilevato alcun punto nel testo originale, se openai restituisce un punto, allora rimuovilo)
- Problemi con i file dei sottotitoli di Safari non riconosciuti

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

- Ottimizza: il numero minimo di caratteri in un paragrafo che attiva la traduzione è stato modificato a un minimo di 4 caratteri per ridurre la confusione, mentre si utilizzano altre funzionalità per evitare di tradurre le aree di navigazione e di fine del sito.
- Risolto: i dettagli di Github non vengono tradotti dopo l'espansione.

## 0.5.14

- Risolto il problema che le immagini su alcune pagine web di: diventano più grandi dopo la copia
- Risolto: la sezione dei commenti di medium non viene tradotta
- Risolto il problema che le immagini su alcune pagine di: venivano copiate in modo errato

## 0.5.12

- Funzione: lo stile di traduzione della linea di divisione aggiunge una linea di divisione verticale per le traduzioni su una sola riga
- Risolto: casi molto rari di divisione dei paragrafi.
- Una grande pagina di orientamento per la configurazione iniziale per i nuovi utenti iOS.

## 0.5.11

- Supporto alla traduzione dei sottotitoli per l'esportazione solo delle traduzioni
- Risolto: alcuni elementi non vengono riconosciuti dal passaggio del mouse
- Risolto: interruzioni di riga parziali dei tweet non riconosciute
- Risolto: lo stile di creazione degli eBook non funziona

## 0.5.10

- Risolto: interruzioni di riga dei tweet non riconosciute
- Risolto: la pagina dei dettagli di Reddit restituisce alcuni paragrafi che non possono essere tradotti
- Risolto un problema con: dove alcuni tag di codice non venivano riconosciuti correttamente.

## 0.5.9

- Corregge le interruzioni di paragrafo in alcuni casi a:
- Correzione: Tampermonkey Toggle mostra solo traduzioni
- Correzione: problema di stile di lettura online eBook non funzionante

## 0.5.8

- Corregge il problema che: l'impostazione temporanea della durata della traduzione del sito web non ha effetto.

## 0.5.7

- Super aggiornamento!

- La funzione Mostra solo traduzioni è qui! Clicca su [More] -> [Switch to show translations only].

  - Supporta scorciatoie personalizzate, impostate nelle impostazioni dell'interfaccia -> Impostazioni scorciatoie

- Ottimizza il problema di limitazione della frequenza delle richieste OpenAI

- ChatGPT predefinito al modello mobile, che è più veloce!

- Ristrutturazione del parsing del core web, il che significa:

  - Traduzione di pagine web su larga scala in pochi secondi
    - Ad esempio,: https://pve.proxmox.com/pve-docs/pve-admin-guide.html, che prima richiedeva 30 secondi, ora viene tradotto in pochi secondi.
  - Uso ultra-basso della memoria per pagine web complesse
    - Ad esempio: https://www\.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Adattamento a più siti web

- Tutte le traduzioni del sito web di ShadowRoot sono supportate.

  - Ad esempio: https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - Ad esempio, la sezione commenti di: https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Corregge il problema dello schermo bianco dopo la traduzione di siti web con idratazione come Next.js.

  - Ad esempio: https://webpack.js.org/

- Risolto il problema che la modifica della scorciatoia del mouse hover richiedeva un aggiornamento della pagina per avere effetto

- Risolto un problema con il riconoscimento dell'interruzione di riga nei file TXT.

- Molti aggiornamenti!

- La funzione 'Mostra solo traduzioni' è arrivata! Clicca su 'More' -> 'Switch to Show Translations Only'.

  - Supporta scorciatoie personalizzate, che possono essere impostate in 'Impostazioni Interfaccia' -> 'Impostazioni Scorciatoie'

- Ottimizzato per il problema del limite di velocità delle richieste OpenAI

- Il parsing del core web è stato ricostruito, il che significa.

  - Traduzione istantanea per grandi siti web
  - Uso minimo della memoria per pagine web complesse
  - Migliore compatibilità con più siti web

- Ora supporta le traduzioni per tutti i siti web con ShadowRoot.

- Risolto il problema dello schermo bianco dopo la traduzione di siti web con idratazione, come Next.js

- Risolto il problema in cui la modifica della scorciatoia del mouse hover richiedeva un aggiornamento della pagina per avere effetto

- Risolto il problema con il riconoscimento delle interruzioni di riga nei file TXT.

## 0.5.6

- Correzione: problema di popup della nuova scheda macOS.
- Funzione: Nuova pagina guida per il nuovo utente.

## 0.5.5

- Correzione: problema dell'area del mouse over.

## 0.5.4

- Correzione: duplicato della pagina Spa

## 0.5.3

- Correzione: ascoltatore di tasti di scelta rapida del mouse hover.
- Correzione: traduzione del documento PDF
- Funzione: Aggiungi nuova pagina guida cliente

## 0.5.2

- Correzione: impostazioni scorciatoie mouse hover userscript

## 0.5.1

- Correzione: OpenAI API non funziona.

## 0.5.0

- Funzione: Traduci il paragrafo corrente quando il mouse passa sopra.
- Funzione: Ristrutturazione della traduzione PDF, ora puoi tradurre la maggior parte dei PDF con Immersive Translate
- Correzione: Disabilita il menu contestuale non funzionante [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Correzione: Evita Content Security Policy per [Mastondon](https://mastodon.social/)

## 0.4.11

- Correzione: permesso userscript (solo per userscript).

## 0.4.8

- Funzione: Bing Translate a Microsoft Translate per una qualità più stabile.
- Correzione: pagina web TXT pura come [questa](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Prestazioni: Escludi alcune pagine pubblicitarie figlie nel sito web, e le prestazioni sono migliorate un po'

## 0.4.7

- Correzione: popup mancante di Firefox Userscript.

## 0.4.6

- Funzione: Consenti a terze parti di inviare eventi di documento per chiamare `toggleTranslatePage`
- Funzione: app iOS aggiunge pulsante di abilitazione estensione e link alle comunità
- UI: il modello del campo delle impostazioni OpenAI utilizza la selezione invece della casella di input del testo.

## 0.4.5

- Correzione: problema di estensione safari iOS 15.0.
- Correzione: scorciatoie estensione safari macOS
- Correzione: popup della politica di sicurezza dei contenuti per l'estensione, e in parte per userscript.

## 0.4.4

- Chore: Rimuovi console.log

## 0.4.3

- Correzione: rilevamento spazi bianchi tag sup, sub.
- Funzione: supporta ChatGPT Plus Website come servizio di traduzione, questa è una funzione beta, quindi puoi accedervi abilitando la funzione Beta nelle impostazioni dello sviluppatore. È molto lento, perché chatgpt può inviare solo una richiesta alla volta. Assicurati di avere un account ChatGPT Plus, perché ci sono più limiti sull'account gratuito, e non sono sicuro se questo comporta rischi per il tuo account, fai attenzione ad usarlo.

## 0.4.1

- Correzione: menu contestuale di Firefox scomparso dopo il riavvio.
- Supporto Azure openai

## 0.4.0

- Funzione: Supporta la traduzione di file di sottotitoli locali (.srt,.ass,etc.)

## 0.3.17

- Funzione: Supporta la traduzione di file .txt locali.
- Correzione: il menu contestuale potrebbe non essere disponibile a volte. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Correzione: mantieni &nbsp; come spazio bianco.
- Rimozione: Rimuovi Papago, poiché [il servizio è inattivo](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: consenti nessuna chiave API per openai
- UI: consenti il reset di Open AI alle impostazioni predefinite

## 0.3.14

- Dipendenza: Aggiorna pdf.js all'ultima versione
- Correzione: colore di sfondo della selezione pdf
- Correzione: rilevamento spazi bianchi

## 0.3.13

- Correzione: problema di carattere specifico del costruttore di ebook, come alcuni percorsi di capitolo sono `xxx' xxxx`.
- UI: piega le opzioni personalizzate openai per impostazione predefinita.
- UI: Aggiungi stato di esportazione per l'esportazione epub.
- Correzione: prompt predefinito Gpt4

## 0.3.12

- Funzione: Ora possiamo personalizzare il colore di sfondo del tema di traduzione del Marker.
- Correzione: postMessage quando la pagina di avvio ha rotto alcuni siti, ora lo faremo solo quando traduciamo davvero le pagine
- Correzione: problema di avanzamento ebook.
- Correzione: migliore per dividere il lungo paragrafo, 1.5 miliardi, 25.5%, Mr. non sarà considerato come un confine

## 0.3.11

- Correzione: colore del testo in modalità scura del lettore ebook
- Correzione: prompt openAI

## 0.3.10

- Migliore: rileva contenitore giapponese/coreano.
- Correzione: Avanzamento del costruttore di Ebook fermo al 99%.

## 0.3.9

- Correzione: lo stato di input dei servizi di traduzione switch UI delle opzioni non è cambiato.

## 0.3.8

- UI: colore di caricamento più trasparente
- Correzione: Rileva lingua Ebook.
- Funzione: Aggiungi avanzamento traduzione per il costruttore di ebook, e un bel coriandolo dopo il successo.
- Funzione: Aggiungi riprova tutti i paragrafi falliti per il pulsante di riprova.
- Correzione: Gestione errore Deepl

## 0.3.7

- Correzione: il lettore ebook non può caricare immagini su Chrome.

## 0.3.6

- UI: migliore per creare l'interfaccia della pagina ebook

## 0.3.5

- Correzione: esportazione ebook userscript
- Funzione: aggiungi endpoint API personalizzato per OpenAI
- Funzione: aggiungi opzioni di tempo di traduzione temporanea del sito web su `Impostazioni Avanzate`

## 0.3.4

- CI: Build fallita

## 0.3.3

- Correzione: creatore di ebook per Kindle
- Modifica: Colore dell'icona di caricamento, da nero a blu, per adattarsi alla pagina web in modalità scura.
- Funzione: Supporta la traduzione html locale per l'estensione

## 0.3.2

- Correzione: spostamento del cursore del modulo di input delle opzioni.
- Funzione: OpenAI supporta apiUrl personalizzato per le impostazioni dello sviluppatore.

## 0.3.1

- Funzione: aggiorna l'icona scura alla trasparenza.
- Correzione: Ordine errato per lungo paragrafo

## 0.3.0

- Versione: D'ora in poi, cambieremo il numero di versione minore una volta al mese, ad esempio, ora a marzo, la versione inizierà da 0.3.0, ad aprile, il numero di versione inizierà da 0.3.0, ad aprile, il numero di versione inizierà da 0.4.0, il prossimo aprile, il numero di versione sarà 1.4.0, e così via. Questo perché non ha senso per le estensioni seguire Questo perché non ha senso per le estensioni seguire la semantica, ma standardizzare i numeri di versione secondo le leggi del tempo è una motivazione per lo sviluppo per continuare ad aggiornare, e per gli utenti per trovare problemi più facilmente.
- Funzione: Supporta icona scura per firefox

## 0.2.86

- Aggiungi opzione di lunghezza massima del testo per richiesta con Open AI
- Correzione: identificatore ebook duplicato
- Funzione: Supporta la traduzione della pagina web txt

## 0.2.85

- Correzione: alcuni file epub non possono essere trovati.

## 0.2.84

- Funzione: Supporta Lettore e Creatore di Ebook

## 0.2.83

- Funzione: Consenti al modulo di input password di mostrare la password.

## 0.2.82

- Correzione: Alcuni siti utilizzano `span` per gli stili, quindi utilizziamo `font` invece di span per l'involucro del target di traduzione
- Correzione: limite massimo di token OpenAI, cambia caratteri massimi da 1500 a 1300.

## 0.2.81

- Correzione: m.youtube.com
- Correzione: modulo opzioni UI
- Correzione: prompt Open AI
- Funzione: Supporta chiavi multiple OpenAI, usa `,` per dividerle.

## 0.2.80

- Funzione: Aggiungi Menu Abilita/Disabilita per popup -> more
- Correzione: conflitto messaggio DingTalk

## 0.2.79

- Correzione: Open AI per paragrafo spazio

## 0.2.78

- Funzione: supporta OpenAI CHATGPT 3.5 (supporta l'interfaccia OpenAI ChatGPT 3.5)
- Funzione: Aggiungi nuovo tema Solid Border (新增新主题，实线边框)

## 0.2.77

- Correzione: errore di tag multiplo nel codice.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Correzione: errore di tag multiplo nel codice [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Funzionalità: Supporto per il conteggio personalizzato del testo di traduzione immediata per diversi servizi di traduzione.

## 0.2.74

- Funzionalità: Supporto per Tencent (alpha)
- Correzione: traduzione openai
- Correzione: controllo inline dei tag sconosciuti

## 0.2.73

- Funzionalità: Supporto per il tema di traduzione Grey
- Correzione: Pagina di tendenza di Github

## 0.2.72

- Correzione: problema di rete del servizio di traduzione su Firefox mobile.

## 0.2.71

- Correzione: permesso dello userscript Open AI

## 0.2.70

- Correzione: segnaposto Open AI

## 0.2.69

- Funzionalità: Supporto per Open AI come servizio di traduzione.
- Funzionalità: Supporto per la verifica del servizio di traduzione su options.html
- Funzionalità: Supporto per il frame principale personalizzato poiché alcuni siti non utilizzano il body come frame principale

## 0.2.68

- Supporto per Caiyun (Alpha)
- Correzione dei tag di blocco sconosciuti

## 0.2.67

- Funzionalità: Aggiunta di `<all>` per tradurre sempre le lingue, quindi ora puoi usarlo per tradurre tutte le lingue tranne la lingua di destinazione, e mai tradurre le lingue
- Correzione: Consenti la configurazione dell'API di Google personalizzata
- Miglioramento: Supporto gratuito per Deepl
- Correzione: alto utilizzo di memoria per userscripts ed estensioni (rimuovendo opencc zh-CN a zh-TW, invece con Google translate)
- Correzione: Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Correzione: configurazione di Azure translate ma ancora mostra (necessita configurazione)

## 0.2.66

- Correzione: traduzione del file PDF fallita, bug dalla versione 0.2.60 per supportare deepl da zh-CN a zh-TW

## 0.2.65

- Supporto per la richiesta di throttling per più frame
- Non tradurre il titolo della pagina quando si è in iframe

## 0.2.64

- Correzione: scelta dei servizi di traduzione openl
- Funzionalità: Supporto per l'opzione di traduzione del titolo

## 0.2.63

- Funzionalità: Supporto per il servizio di traduzione Azure
- Funzionalità: Supporto per il servizio di traduzione Papago
- Correzione: sincronizzazione nativa di Google Drive su Firefox Android.
- Correzione: modifica della trasparenza da 0.4 a 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Correzione: suggerimenti per le scorciatoie popup
- Prestazioni: richieste seriali a concorrenza
- Miglioramento per il rilevamento del conteggio giapponese

## 0.2.62

- Funzionalità: Aggiunta della regola waitForSelectors, per correggere alcuni siti come reddit

## 0.2.61

- Correzione: lo userscript è troppo grande per greasy fork
- Miglioramento: riduzione delle dimensioni del file

## 0.2.60

- Funzionalità: Supporto per zh-CN a zh-TW per Deepl
- Funzionalità: Caratteristica Deepl di Immersive Translate
- Funzionalità: Supporto per lo zoom della dimensione del font personalizzato
- Correzione: stile del forum di Steam
- Correzione: lo stile globale non cambia dopo la generazione di elementi dinamici
- Correzione: promuovere l'esclusione prioritaria
- UI: modifica della pagina about
- Correzione: alcuni elementi matematici rimangono originali

## 0.2.59

- Correzione: Elemento di blocco dei tag sconosciuti
- Correzione: elemento translate=no sovrascritto
- Correzione: corrispondenza URL con più \*

## 0.2.58

- Funzionalità: Supporto per il colore del testo di traduzione personalizzato, colore del bordo.

## 0.2.57

- Nessuna modifica, ricostruzione

## 0.2.56

- Correzione della traduzione duplicata per elementi inline con elemento codice.
- Correzione del controllo inline/blocco dei tag sconosciuti
- Funzionalità: supporto per css iniettato sulla scheda sviluppatore
- Funzionalità: tagliare authKey, appid appSecret
- Miglioramento: aprire la pagina delle impostazioni in una nuova scheda (ma non per Stay)

## 0.2.55

- Tentativo di correggere il charset dell'API deepl

## 0.2.54

- Rimozione del permesso di schede per il rifiuto del Chrome Store
- Correzione della traduzione dell'intera pagina, il footer viene ignorato
- Aggiunta di note alla pagina about
- Supporto per URL personalizzati dalla configurazione integrata

## 0.2.53

- Correzione dell'errore di sincronizzazione di Google Drive nello userscript.

## 0.2.52

### Codice

- Utilizzo dell'ultima versione di esbuild
- Utilizzo dell'ultima versione di deno
- CI: invio del codice sorgente a Firefox

## 0.2.51

- Correzione: Google Auth richiede il login su Chrome/Firefox
- Sostituzione dei link del servizio di traduzione
- Miglioramento per i permessi.
- rimozione della minificazione.

## 0.2.50

- Correzione del problema di caricamento su Google Drive (davvero) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Rimozione delle scorciatoie alt+d, alt+s perché potrebbero entrare in conflitto con le scorciatoie native.
- Correzione del problema di caricamento su Google Drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Miglioramento della velocità, aggiungendo minLength a 50 per il rilevamento della lingua.
- Correzione della convalida del token di Google Drive.

## 0.2.47

- Correzione dell'API deepl

## 0.2.46

- correzione del segno di blocco

## 0.2.45

- Correzione: innerText dell'elemento è undefined
- Correzione: lingua sorgente della traduzione caiyun undefined

## 0.2.44

- Correzione: attivazione/disattivazione della maschera nello userscript
- Correzione della logica di attivazione/disattivazione della maschera

## 0.2.43

- Correzione: attivazione/disattivazione della maschera nello userscript con evento touch.
- Correzione della velocità (rimuovendo sleep(300))

## 0.2.42

- Correzione: hover della maschera quando si attiva/disattiva nuovamente la maschera.
- Aggiunta di scorciatoie per la maschera su mobile
- Correzione del problema di sincronizzazione cloud nello userscript
- Spostamento della pagina delle opzioni avanzate nel menu a sinistra.
- Aggiunta della logica di ripetizione al servizio di traduzione

## 0.2.41

- Correzione: traduzione niu nello userscript
- Correzione: traduzione xhtml

## 0.2.40

- Correzione: visualizzazione delle funzionalità beta
- Correzione: impostazione della pagina popup su una nuova scheda
- Correzione: sostituzione del segnaposto di traduzione

## 0.2.39

- Supporto per le scorciatoie per mostrare la traduzione della maschera
- Supporto per abilitare la funzionalità beta nel pannello sviluppatore
- Correzione delle scorciatoie nell'estensione mobile

## 0.2.38

- Supporto per il tema di caricamento
- Correzione di getpocket.com
- Correzione del footer a parte per l'area del body
- Correzione dell'icona di importazione/esportazione

## 0.2.37

- Correzione del segno di esclusione del frame

## 0.2.36

- Supporto per la sincronizzazione con Google Drive

## 0.2.35

- Correzione: ignorare i tag rb, rt giapponesi.
- Miglioramento dell'interfaccia utente popup
- Miglioramento dei suggerimenti per gli userscript difettosi
- Aggiunta di contributi alla pagina about
- Correzione: traduzione volc per il rilevamento automatico della lingua

## 0.2.34

- Correzione della velocità per più lingue

## 0.2.33

- Supporto per la modalità di scrittura verticale, come il giapponese.
- Aggiunta di 3 temi
- Aggiunta del servizio di traduzione Niu

## 0.2.32

- Correzione della traduzione di base dei PDF
- Correzione della selezione popup di un servizio non configurato, vai alla pagina delle opzioni.
- Correzione: mantenere aperte le impostazioni.
- Correzione della velocità di rilevamento di più lingue

## 0.2.31

- Correzione dell'iniezione css nell'iframe dinamico

## 0.2.30

- Supporto per la traduzione inline dell'iframe nello userscript.
- Supporto per la traduzione shadowroot. Ad esempio:
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Area di conversazione.
- controlla anche la regola di sincronizzazione nel popup

## 0.2.29

- Correzione della traduzione di Facebook
- Supporto per mostrare l'opzione del menu contestuale.

## 0.2.28

- Rimozione della corrispondenza non standard per lo userscript

## 0.2.27

- Supporto per la traduzione inline dell'iframe. (Solo per estensione, non disponibile per
  userscript)
- Correzione della traduzione di più lingue

## 0.2.26

- Correzione dell'addon di Firefox Android
- Aggiunta di impostazioni avanzate per la traduzione di newline

## 0.2.25

- Supporto per la traduzione dell'iframe, come QQ mail, tweet incorporato.

## 0.2.24

- Aggiunta di un sito di traduzione temporaneo per un po'
- Correzione: API del browser dello userscript stay.app
- Correzione: pagina delle opzioni di stay.app

## 0.2.23

- Correzione della traduzione della pagina in più lingue

## 0.2.22

- Correzione della build dello userscript

## 0.2.21

- Correzione della traduzione online dei PDF su Firefox

## 0.2.20

- Correzione del problema di richiesta di macaque
- Correzione del segno di evidenziazione della linea

## 0.2.19

- Correzione del giapponese intelligente di tencent
- Correzione del browser haikuo world

## 0.2.18

- Correzione del cambio di URL del client, mantenere automaticamente lo stato di traduzione.
- Rimozione del contenitore a parte come contenitore di traduzione.
- Refactoring della posizione del popup.

## 0.2.17

- Cambiamento dell'evidenziazione in segno
- Aggiunta del tema di traduzione evidenziato

## 0.2.16

- Compatibilità con Macaque

## 0.2.15

- Correzione del problema di rimbalzo al tocco

## 0.2.14

- Correzione: globalThis.GM non funziona su Safari

## 0.2.13

- Supporto per il trascinamento del popup dello userscript
- Supporto per tre dita su dispositivi touch per attivare/disattivare le pagine di traduzione
- Supporto per nascondere l'icona del popup dello userscript.

## 0.2.12

- Miglioramento per inoreader

## 0.2.11

- Correzione
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas archive Il contenuto principale della pagina non può essere tradotto

## 0.2.10

- Correzione della distanza dell'altezza della linea nei PDF

## 0.2.9

- Correzione dei segni di esclusione degli elementi
- Correzione del controllo del tipo di deno
- rimozione di importmap
- Correzione della traduzione dei menu contestuali
- ripristino della pagina quando non tradurre mai questo sito è abilitato
- Aggiunta di una descrizione per aggiungere URL

## 0.2.8

- Rilevamento della lingua dell'agente utente per la lingua dell'interfaccia
- Correzione del bug di interruzione di riga.

## 0.2.7

- Correzione della richiesta di grease monkey

## 0.2.6

- Correzione
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  problema di corrispondenza dell'URL del file

## 0.2.5

- aumento della versione per il test ci

## 0.2.4

- cattura l'errore di connessione del messaggio per il popup.

## 0.2.3

- Fix
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  crea contesto più volte

## 0.2.2

- Fix file di esempio PDF
- Fix file locale pdf su Firefox
- Fix scorciatoie pdf

## 0.2.1

- Supporto per Grease Monkey Shortcuts manager.
- Fix regex di corrispondenza
- Fix commenti su YouTube.
- Fix versione compatta mobile di Reddit
- Fix problema di traduzione fulltext

## 0.2.0

- Fix PDF a due colonne.
- Fix bug versione Chrome/Edge Store.
- Fix
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Pubblicazione su addon Firefox
- Pubblicazione su Edge
- fix margine pdf.
- Cambia file di esempio pdf

## 0.0.62

- Fix formato pdf, rientro.
- Fix telegra.ph prevenzione modifica elemento

## 0.0.61

- Fix chiusura elemento span.
- Fix permessi per browser precedenti

## 0.0.60

- Fix Chrome PDF

## 0.0.59

- Supporto iniziale per PDF

## 0.0.58

- Modifica descrizione tema traduzione

## 0.0.57

- Cambia interfaccia popup, per un uso più semplice

## 0.0.56

- Fix timeout chrome
- Fix errore di divisione frase.

## 0.0.55

- Fix visualizzazione elemento none.
- refactoring elemento mark

## 0.0.54

- Supporto interruzione di riga per X caratteri.

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
  [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7)
- Fix dimensione font UI opzioni

## 0.0.50

- Fix traduzione blocco img.

## 0.0.49

- Fix estensione Firefox

## 0.0.48

- Fix estensione Chrome

## 0.0.47

- riscrittura messaggio con background, usa connect invece di sendMessage
- aggiungi supporto mobile Reddit
- fix spazio bianco pre per alcuni articoli

## 0.0.46

- Formatta info meta userscript

## 0.0.45

- userscript usa un file.
- aggiungi timeout per richiesta cache

## 0.0.44

- Fix errore divisione tencent.
- Fix errore elemento sup inline.
- Migliore per Twitter

## 0.0.43

- Fix tweet br
- Fix traduzione globale.

## 0.0.42

- Fix tag BR
- tratta i tag di blocco come regole

## 0.0.41

- Fix controllo elemento inline
- Aggiungi opzione log debug sviluppatore

## 0.0.39

- Fix servizio di traduzione contiene mock2

## 0.0.38

- Supporto cache risultato per userscript
- Aggiungi opzioni UI
- Supporto rilevamento più contenitori di contenuti

## 0.0.37

- Fix cambio servizio di traduzione popup non funziona
- Fix traduzione contenuto post mobile Reddit.

## 0.0.36

- Fix carattere speciale Wikipedia
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Fix dimensione icona userscript.
- abilita tutti i siti a rilevare la lingua del paragrafo.

## 0.0.35

- Fix YouTube vai alla pagina successiva
- Supporto pagina di ricerca YouTube.
- Fix interruttore avanzato opzioni.
- Fix tag img, tag nascosto
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Fix aggiornamento forzato ricerca Google
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Supporto risultato tabella di Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Fix spazio vuoto Wikipedia
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Modifiche Interrotte

- La scorciatoia predefinita per attivare la traduzione è stata cambiata in `alt+A`, perché è la chiave più conveniente da digitare.

### Altri

- Supporto modalità di traduzione immediata, così puoi far tradurre la pagina web il più rapidamente possibile.
- Supporto impostazione area della pagina da tradurre. così puoi tradurre più aree.
- Supporto impostazione del primo x conteggio di testo da tradurre immediatamente.
- Fix traduzione duplicata quando si cambia traduzione
- Migliore interfaccia popup

## 0.0.33

- Supporto più lingue, zh-TW, en

## 0.0.32

- Fix traduzione file locale dopo il salvataggio. Risolto
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Aggiungi file dist js al repository pubblico

## 0.0.31

- Supporto traduzione dell'intera pagina
- Supporto traduzione pagina immediatamente
- Più Config UI
- Riflette il tema
- Aggiungi nuova icona
- Aggiungi nuovo tema di traduzione dashedBorder

## 0.0.30

- Migliore per tema tratteggiato

## 0.0.29

- Fix paragrafo valido.
- Aggiungi tema punteggiato, thinDashed
- Migliore per tema tratteggiato, evidenziato

## 0.0.28

- Fix sottolineatura
- Aggiungi tema tratteggiato, carta
- Fix rilevamento intestazione

## 0.0.27

- Supporto translationTheme

## 0.0.26

- Fix permesso di connessione userscript volc alpha.
- Fix versione cliccabile.

## 0.0.25

- Supporto selectorMatches, così possiamo abbinare tutti i manstondon ora.
- Fix errore userscript Firefox.

## 0.0.23

- Migliore rilevamento cinese
- Fix problema innerText Reddit

## 0.0.22

- Supporto deeplx
- Fix traduzione multipla quando si cambia servizio

## 0.0.21

- Fix alcuni tag span sono elementi di blocco

## 0.0.20

- Supporto non tradurre hashtag come #hash, tag come @xxx, $tag, come $APPL
- Supporto elemento di blocco

## 0.0.18

- Supporto deepl, bing, baidu, youdao, volc, openl, caiyun.

## 0.0.13

- Supporto userscript

## 0.0.4.8

- Fix ordine codice.
- Supporto interfaccia popup di base

## 0.0.4.6

- Supporto controllo nuova versione

## 0.0.3

- Supporto file locali

## 0.0.2

- Supporto elementi dinamici
- Supporto traduzione visibile
