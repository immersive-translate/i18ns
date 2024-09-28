# DeepL

## Accesso diretto ai servizi di traduzione di DeepL dopo aver aperto un [Abbonamento Immersive Translate Pro](https://immersivetranslate.com/en/pricing/) (Consigliato)

[Clicca qui per la presentazione](https://immersivetranslate.com/en/pricing/)

## Ottieni l'API ufficiale DeepL tramite DeepL

1. Introduzione ufficiale: [API DeepL](https://www.deepl.com/en/pro#developer)

   - Da notare che: [API DeepL](https://www.deepl.com/en/pro#developer) e [DeepL Pro](https://www.deepl.com/pro) sono due tipi di account differenti, e l'account [API DeepL](https://www.deepl.com/en/pro/select-country#developer).

2. [Perché](https://www.deepl.com/en/whydeepl) scegliere DeepL?

   - Inglese ⇄ Cinese 5 volte più accurato
   - Inglese ⇄ Giapponese 6 volte più accurato
   - Motore di traduzione basato su tecnologia di intelligenza artificiale (reti neurali)

3. L'API DeepL è divisa in [API Gratuita e API Pro](https://www.deepl.com/en/pro#developer)

   - L'API Gratuita fornisce 500.000 caratteri gratuiti al mese.
   - La [tariffa ufficiale](https://www.deepl.com/en/pro#developer) per l'API Pro è: $25 per 1 milione di caratteri.
   - Per un utente ad alta frequenza, la quantità di caratteri consumati in un mese è di circa 10 milioni di caratteri, e il prezzo è di circa: 250 USD

4. Per registrare un account e aprire l'[API DeepL](https://www.deepl.com/en/pro#developer).## Costruisci la tua API DeepL

Stiamo sperimentando il supporto per il nostro servizio DeeplX nella funzionalità Beta (ma non è ben adatto come servizio di traduzione web, come testato. A causa dell'enorme quantità di richieste API per la traduzione di pagine web, se costruisci questo servizio, assicurati di fare un buon lavoro di bilanciamento del carico), di seguito è riportato come attivare le funzionalità sperimentali delle istruzioni:

1. Abilitazione delle Funzionalità di Test Beta nelle Impostazioni Sviluppatore
2. Trova DeepLX (Beta) nelle Impostazioni Base e inserisci l'URL dell'API DeepL costruita da te, es. http\://tuo-dominio/traduci

> Q: Come posso costruire il mio?
>
> A: [OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate) o [zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md) -->

## Problemi comuni

### 1. La chiave inserita non è disponibile.

DeepL API Pro e DeepL Pro sono due tipi di account, la chiave Auth che può essere utilizzata in Immersive Translate è l'account DeepL API, clicca qui per [DeepL API Pro](https://www.deepl.com/en/pro/select-country#) sviluppatore)

### 2. Promemoria Deepl Free API 401 Nessun Privilegio

Le chiavi Deepl Free API terminano tutte con `:fx`, qualsiasi altra cosa non è una chiave Free API.

### 3. 456, Quota per l'utente è stata raggiunta.

L'uso ha superato il limite massimo ufficiale di DeepL per utente, potresti aver violato la politica di uso equo di DeepL e ti viene consigliato di evitare tale comportamento. Se sei un abbonato a pagamento, l'uso verrà reimpostato automaticamente il mese prossimo.
