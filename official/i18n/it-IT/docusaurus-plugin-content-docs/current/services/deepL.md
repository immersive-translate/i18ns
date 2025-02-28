# DeepL

## Accesso diretto ai servizi di traduzione DeepL dopo aver attivato un [Immersive Translate Pro Membership](https://immersivetranslate.com/en/pricing/) (Consigliato)

[Scopri di più](https://immersivetranslate.com/en/pricing/)

## Ottieni l'API ufficiale di DeepL tramite DeepL

1. Introduzione ufficiale: [DeepL API](https://www.deepl.com/en/pro#developer)

   - Nota che: [DeepL API](https://www.deepl.com/en/pro#developer) e [DeepL Pro](https://www.deepl.com/pro) sono due tipi di account diversi, e l'account [DeepL API](https://www.deepl.com/en/pro/select-country#developer).

2. [Perché](https://www.deepl.com/en/whydeepl) scegliere DeepL?

   - Inglese ⇄ Cinese 5 volte più accurato
   - Inglese ⇄ Giapponese 6 volte più accurato
   - Motore di traduzione basato su tecnologia di intelligenza artificiale (reti neurali)

3. L'API di DeepL è divisa in [Free API e Pro API](https://www.deepl.com/en/pro#developer)

   - La Free API fornisce 500.000 caratteri gratuiti al mese.
   - La [tariffa ufficiale](https://www.deepl.com/en/pro#developer) per la Pro API è: $25 per 1 milione di caratteri.
   - Per un utente ad alta frequenza, la quantità di caratteri consumati in un mese è di circa 10 milioni di caratteri, e il prezzo è di circa: 250 USD

4. Per registrare un account e attivare l'[API di DeepL](https://www.deepl.com/en/pro#developer).

## problemi comuni

### 1. La chiave inserita non è disponibile.

DeepL API Pro e DeepL Pro sono due tipi di account, la chiave di autenticazione che può essere utilizzata in Immersive Translate è l'account DeepL API, clicca qui per [DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer).

### 2. Risoluzione dei problemi di autenticazione 401, 403

Questi errori si verificano tipicamente quando si utilizza il tipo sbagliato di chiave di autenticazione. Si prega di notare:

1. DeepL offre due prodotti diversi: DeepL Pro (servizio di traduzione) e DeepL API (interfaccia per sviluppatori)
2. Le chiavi trovate nelle impostazioni del tuo account DeepL Pro **non sono compatibili** con le chiamate API
3. È necessario registrarsi specificamente per un account DeepL API per ottenere una chiave API
4. Le chiavi API gratuite di DeepL sono identificate dal suffisso `:fx`
5. Le chiavi API Pro di DeepL non hanno il suffisso `:fx` e appaiono come una normale stringa di caratteri

Assicurati di esserti registrato correttamente per il servizio DeepL API, non solo per il servizio di traduzione DeepL Pro.

### 3. 456, Quota per utente raggiunta.

L'uso ha superato il limite ufficiale massimo per utente di DeepL, potresti aver violato la politica di uso corretto di DeepL e ti viene consigliato di evitare tale comportamento. Se sei un abbonato a pagamento, l'uso verrà automaticamente reimpostato il mese successivo.
