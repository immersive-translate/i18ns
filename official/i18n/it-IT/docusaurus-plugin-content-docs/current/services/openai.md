# Open AI (Azure OpenAI)

Accesso diretto ai servizi di traduzione di OpenAI aprendo un [abbonamento a Immersive Translate Pro](https://immersivetranslate.com/en/pricing/) (raccomandato)

[Clicca qui per la presentazione](https://immersivetranslate.com/en/pricing/)

## Ottenere una chiave API dalla piattaforma ufficiale degli sviluppatori OpenAI.

- [indirizzo ufficiale API openAI](https://openai.com/api/)
  - Nota: Attualmente, OpenAI non è aperto alla registrazione con numeri di cellulare cinesi.
- Dopo esserti registrato per un account OpenAI, apri [Chiave Segreta API](https://platform.openai.com/account/api-keys) per creare una Chiave Segreta API
- Poi basta inserire la chiave nella configurazione OpenAI nell'estensione Immersive Translate.## Avvertenza

1. **Se non hai una carta di credito associata, o sei un nuovo utente OpenAI a 5 lame con fino a 3 richieste al minuto**, è praticamente inutilizzabile ed è normale ricevere errori. [Puoi cliccare qui per vedere i limiti di frequenza per la tua API](https://platform.openai.com/account/rate-limits)
2. L'API di OpenAI e ChatGPT sono due servizi differenti, l'estensione Immersive Translate supporta l'API di OpenAI, non la versione web di ChatGPT, quindi è necessario aprire il servizio API di OpenAI invece di aprire ChatGPT plus, e inserire la chiave API nella pagina delle Impostazioni dopo l'apertura.
3. Errore 429, significa che è stato superato il limite di frequenza di openai, si raccomanda di ridurre il numero massimo di richieste al secondo, specialmente quando si traducono e-book, anche se si tratta di una versione a pagamento, è necessario ridurre il numero massimo di richieste al secondo e regolarlo a 5 richieste al secondo per renderlo più stabile.
4. Il modello OpenAI gpt-3.5-turbo ha un prezzo di: $0.002 / 1K token, e costa circa $1 per tradurre 660.000 caratteri inglesi e $0.25 per tradurre 170.000 caratteri inglesi.
5. L'estensione Immersive Translate supporta più chiavi API per il bilanciamento del carico, si prega di usare la virgola `,` per separare le diverse chiavi quando si compila il modulo.

## Raccomandazione attuale sul numero di richieste

Recentemente, anche OpenAI è diventata molto restrittiva per gli utenti paganti, a partire dalla versione 0.5.0 il conteggio delle richieste di default è stato cambiato in secondi, e il numero massimo di default di richieste al secondo è stato cambiato a 10 richieste al secondo.## Azure OpenAI

Il servizio di traduzione OpenAI è compatibile anche con l'interfaccia di Azure OpenAI. Prima, crea il servizio OpenAI nella console di Azure, poi vai su Azure AI Studio: https://oai.azure.com, crea un dispiegamento gpt-35-turbo e ricorda il nome del dispiegamento.

Dopo aver dispiegato il modello gpt-35-turbo, apri la pagina delle impostazioni di OpenAI per Immersive Translate:

1. Api Key Si prega di inserire la chiave fornita dalla console di Azure.
2. Clicca per espandere altre impostazioni e imposta l'indirizzo personalizzato a:

`https://{your-custom-name}.openai.azure.com/openai/deployments/{you-deployment-name}/chat/completions?api-version=2023-03-15-preview`

Cambia `{your-custom-name}` con il tuo sottodominio e `{you-deployment-name}` con il nome del tuo dispiegamento.

3. Il nome del modello deve essere selezionato manualmente affinché il modello personalizzato possa leggere: `gpt-35-turbo`,

> Se ci sono ancora domande, puoi andare dentro Azure AI Studio, aprire PlayGround, [Visualizza Codice], e ci saranno il [EndPoint] e la [Chiave] finali in fondo, come segue:

![](/assets/docs/doc-assets/azure-openai-key.jpg)

## Personalizzazione dell'indirizzo API di OpenAI

- Questo può essere configurato tramite `Altre Impostazioni` con il seguente punto di ingresso

***

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

***