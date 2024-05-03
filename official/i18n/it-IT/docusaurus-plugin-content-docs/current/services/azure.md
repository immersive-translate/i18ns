# Traduzione Microsoft Azure

## Dichiarazione Breve

1. Sito ufficiale: [Tradotto da Microsoft Azure](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/text-translation-overview)
2. Descrizione Ufficiale: Le traduzioni sono gratuite fino a 2 milioni di parole al mese, se superi i 2 milioni di parole al mese, ti verrà addebitato un costo di $10 / 1 milione di parole. Per maggiori dettagli, si prega di fare riferimento a [Nota sui Prezzi](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/)

## Processo di Registrazione

Il processo di registrazione è più laborioso rispetto ad altri servizi di traduzione e richiede pazienza.

Link di Riferimento: [Documentazione per Iniziare con Microsoft Azure Translation](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)

## Iscriviti a un account Azure

Il primo passo è iscriversi a un account [Azure](https://azure.microsoft.com/en-us/free/cognitive-services/), che richiede di essere associato a una carta di credito internazionale (Visa/Master). In assenza, non sarà possibile registrarsi.

## Registrazione per un Account di Archiviazione Azure Blob

Passo 2: Registrati per un account di archiviazione [Azure Blob](https://portal.azure.com/#create/Microsoft.StorageAccount).

1. Crea un nuovo gruppo di risorse e compila il nome dell'account di archiviazione
2. Scegli una regione che sia la più vicina a te, per esempio, la regione di Hong Kong sarebbe `Asia Orientale`.
3. Il resto del processo è solo un semplice passaggio successivo. Nell'ultima pagina, dopo che il dispiegamento è completo, clicca sul pulsante blu "Crea" in basso a sinistra.## Creazione di Strumenti di Traduzione

Passo 3: Crea [strumento di traduzione](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation)

1. Scegli una regione che è più vicina a te, per esempio, la regione di Hong Kong sarebbe `Asia Orientale`.
2. I livelli di prezzo sono selezionati secondo le necessità, con `Free F0` disponibile gratuitamente per gli utenti. Il livello gratuito non supporta la traduzione di documenti. Se necessario, può essere utilizzata una prova standard S1.
3. Il resto del processo è solo un semplice passo successivo. Nell'ultima pagina, dopo che il dispiegamento è completo, clicca il pulsante blu "Crea" in basso a sinistra.

## Chiave di Accesso

Dopo il dispiegamento di successo, vai al [Dashboard di Azure](https://portal.azure.com/#home), vai alla pagina per **Strumenti di Traduzione**, e trova la chiave nel menu a sinistra - Gestione Risorse - `Chiavi e Endpoint`. Microsoft fornirà 2 chiavi, scegline una e inserisci la chiave nell'`APIKEY` dell'Estensione Immersiva - Microsoft Translator.

Sotto la chiave c'è anche un'informazione `location/region`, ad es. `eastasia`, che deve essere anche popolata nella `regione` dell'estensione immersiva - Microsoft Translate.

## Problemi Comuni

In caso di dubbi, si prega di fornire feedback [qui](https://github.com/immersive-translate/immersive-translate/issues/137).