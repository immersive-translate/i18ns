---
sidebar_position: 4
---

# Aiuto PDF

Immersive Translate PDF Bilingual Reader è uno strumento di traduzione bilingue incrociata in tempo reale adatto per essere utilizzato come aiuto alla lettura.

Attualmente, caratteri speciali come formule matematiche, tabelle, ecc., non possono essere gestiti correttamente a causa della tecnica di riconoscimento del testo semplice.

Se il tuo PDF contiene tabelle e formule matematiche, ci sono requisiti di traduzione di qualità superiore per loro e hai alcune competenze di programmazione. Si raccomanda di fare riferimento a questo articolo [Nouga-OCR + Immersive Translate](https://app.immersivetranslate.com/pdf-pro/)

Vedi [qui la documentazione](/docs/usage/#pdf-file-translation) per domande sull'uso di base

Ecco alcuni consigli avanzati per la traduzione di PDF:

<!--
## Sposta per regolare il riquadro di traduzione

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/pdf-move.png) -->

### Modifica Riquadro

La traduzione predefinita è modificabile. Puoi anche fare clic su "Mostra testo originale" nel pannello, e il contenuto del riquadro di testo verrà visualizzato come il testo originale riconosciuto in modo intelligente, e puoi apportare correzioni al testo originale nel riquadro di modifica in questo momento. Poi fai nuovamente clic sulla traduzione nel pannello

### Spostamento Riquadri di Testo

Quando alcuni paragrafi sono riconosciuti in una posizione errata, puoi scegliere di spostare la posizione dell'intero riquadro di modifica del paragrafo posizionando il mouse nell'angolo in alto a sinistra. (Se incontri una situazione in cui non puoi trascinare, puoi ingrandire e trascinare verso il basso l'angolo in basso a destra, e l'angolo in alto a sinistra si muoverà normalmente)

### Elimina riquadro di testo

Quando alcuni paragrafi possono avere problemi di riconoscimento, unisci manualmente il paragrafo precedente, questo paragrafo può essere ridondante, in questo momento puoi fare clic su questo pulsante per eliminarlo!### Ridimensionamento della dimensione del riquadro di testo

Poiché l'altezza e la larghezza della traduzione predefinite sono le stesse del paragrafo originale per impostazione predefinita, quando il contenuto della traduzione supera il testo originale ci sarà un sovrappiù, in questo caso è possibile visualizzarlo attraverso lo scorrimento interno. È anche possibile trascinare e rilasciare nell'angolo in basso a destra per ingrandire adeguatamente questo riquadro di testo in modo da consentire la visualizzazione completa del contenuto.

<!-- ## Pulsanti di Controllo dello Stile

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/pdf-control.png) -->

### Modalità Bandwagon

L'impostazione predefinita è quella di ripristinare l'immagine del testo originale nell'area tradotta sulla destra. È normale vedere una cornice di sfondo bianco per il testo tradotto, perché è necessario coprire il testo originale disegnato su tela affinché il testo tradotto possa essere visualizzato correttamente.

Se trovi che la modalità di sottofondo influisce sulla tua lettura, basta disattivarla.

### Limite di Sovrapposizione

Poiché usiamo il più possibile per ripristinare l'effetto tipografico originale, quindi la posizione di inizio del paragrafo è quella del paragrafo originale dell'angolo superiore sinistro delle coordinate prevalenti. In circostanze normali dalla traduzione dall'inglese al cinese, il contenuto cinese sarà generalmente più piccolo dell'inglese, questa volta la traduzione può essere pienamente dimostrata. Questo si verifica quando il testo tradotto è ridondante con il testo originale in alcuni casi. Per evitare ciò abbiamo dato alla traduzione un'altezza uguale a quella del paragrafo originale.

Questo può essere disattivato quando riteniamo che la distanza tra i paragrafi superiori e inferiori sia sufficiente per la presentazione della parte tradotta che eccede

### Strettamente Spaziato

Questo obiettivo è in realtà simile a quello sopra, perché c'è una certa spaziatura tra ogni riga di testo al fine di garantire la leggibilità del testo tradotto.

Se lo schermo è piccolo e lo spazio tra i paragrafi superiori e inferiori potrebbe non essere sufficiente per mostrare il sovrappiù del testo tradotto, è possibile attivare questa voce e rimuovere la spaziatura delle righe di testo, in modo che il testo dei paragrafi possa essere completamente visualizzato### Indentazione dell'intestazione del paragrafo

A causa della complessità dei vari layout PDF, non è possibile identificare in modo intelligente se un paragrafo sia in linea con le caratteristiche dell'indentazione, ma se non vi è indentazione, allora potrebbe risultare un po' difficile leggere il paragrafo dell'articolo. Quindi, per questo tipo di paragrafo, l'utente può attivarlo e il primo rigo di ogni paragrafo sarà indentato per mostrare

### Le righe sono ampiamente distanziate e i paragrafi non sono riconosciuti

Alcuni PDF possono, per motivi di visualizzazione, avere uno spazio tra i paragrafi piuttosto ampio, risultando in un riconoscimento intelligente che potrebbe interpretare questa frase come un paragrafo indipendente. Quindi, necessita di essere adeguatamente aggiustato, diciamo di 10, così che 10px venga utilizzato come spaziatura delle righe per riconoscere nuovamente i paragrafi sulla pagina.

### Regolazione della posizione orizzontale delle traduzioni

Poiché le coordinate orizzontali del testo tradotto sono lette dai dati originali del pdf, alcune delle coordinate orizzontali del pdf saranno grandi. In questo caso, è possibile far muovere il contenuto tradotto verso sinistra trascinando la barra di progresso.

### Regolazione della scala delle traduzioni

La dimensione del testo tradotto è sostanzialmente la stessa del testo originale, quando si ritiene che la dimensione del testo tradotto non sia appropriata, è possibile trascinare la barra di progresso per far sì che la dimensione del font sia regolata secondo il rapporto

## Regolazione manuale dei segmenti errati

Se il paragrafo riconosciuto in modo intelligente è incorretto, può essere regolato manualmente seguendo i passaggi

- Cliccare sul pannello di traduzione per visualizzare il testo originale riconosciuto
- Quindi regolare manualmente il paragrafo rispetto al testo originale sulla sinistra copiando e inserendo interruzioni di riga, ecc.
- Quando il paragrafo è confermato essere corretto, cliccare nuovamente su Traduci

<!-- ## Scarica Stampa

Clicca sull'icona di download nell'angolo in alto a destra

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/pdf-download.png) -->

Poiché il nostro strumento si basa sul browser, la velocità di download e i risultati dipendono fortemente dal browser stesso. Pertanto, si raccomanda di non gestire più di 300 pagine di PDF

### Download Traduzione (Stampa)

Questa funzionalità permette di scaricare solo le traduzioni, non il testo bilingue.
Quando viene visualizzata la traduzione predefinita, la modalità di zoom è impostata sulla larghezza della pagina per un effetto di lettura.

Tuttavia, quando si necessita di stampare e si vuole risparmiare tempo, si raccomanda di regolare la modalità di zoom, generalmente si consiglia di impostarla al 100 percento o alla dimensione reale, per ottenere un effetto di stampa migliore.

### Conservazione Bilingue

A causa delle limitazioni tecniche sugli effetti di conservazione bilingue, le traduzioni sono conservate sotto forma di immagini, consentendo la conservazione WYSIWYG degli effetti di traduzione online. Ci vogliono circa 5/6 minuti per esportare 300 pagine di PDF.

## Altre situazioni

### Intraducibile

- Verifica se il testo originale sulla sinistra può essere copiato, se non può essere copiato, significa che è un PDF immagine, attualmente si supporta temporaneamente la traduzione di PDF immagine
- Controlla che la traduzione sia riconosciuta ma non tradotta, che 🔄❓ non appaia alla fine del paragrafo, e che il pulsante nel pannello del plug-in mostri "Traduci". A questo punto, clicca sul pulsante di traduzione per attivare la traduzione.
- Se esiste 🔄❓, clicca sotto ❓ per vedere il messaggio di errore

### Documento di Feedback via Email

Puoi inviare una descrizione del tuo problema + uno screenshot con il PDF originale a support@immersivetranslate.com\. Controlleremo la situazione del PDF e organizzeremo il piano per essere inserito nelle regole di riconoscimento intelligente.
