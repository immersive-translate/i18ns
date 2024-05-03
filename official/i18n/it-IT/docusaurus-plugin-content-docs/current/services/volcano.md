# Traduzione Volcano

## Dichiarazione Breve

1. Sito Ufficiale: [Traduzione Automatica - Motore Volcano](https://www.volcengine.com/product/machine-translation)
2. Descrizione ufficiale delle tariffe: [Fatturazione del Prodotto Traduzione Automatica - Motore Volcano](https://www.volcengine.com/docs/4640/68515)
3. Il Traduttore Volcano è gratuito per i primi 2 milioni di caratteri al mese e addebiterà $49 per ogni milione di caratteri eccedente, si prega di controllare il documento ufficiale delle tariffe per i dettagli.

## Passaggi per l'Applicazione

1. [Panoramica del Processo di Accesso API Traduzione Automatica - Motore Volcano](https://www.volcengine.com/docs/4640/130872), seguire la guida ufficiale per completare i tre passaggi di registrazione di un account, autenticazione con nome reale e attivazione dei servizi. Deve essere fatto dalla console, [Console del Motore Volcano](https://console.volcengine.com/home)
2. Nel quarto passo per ottenere la chiave, il Motore Volcano offre due opzioni:
   1. Continuare a creare (usando l'account principale per creare la chiave, più conveniente, questa chiave può chiamare le risorse dell'account principale, meno sicuro), selezionare "Continuare a creare", apparirà una nuova tabella, che contiene l'"ID Chiave di Accesso" e la "Chiave di Accesso Segreta" che vogliamo usare.
   2. Procedere alla creazione di un nuovo sottoutente (si consiglia di usare un sottoutente per creare la chiave per maggiore sicurezza), ottenere l'"ID Chiave di Accesso" e la "Chiave di Accesso Segreta", questo sottaccount deve avere il permesso `TranslateFullAccess`.
3. Aprire Impostazioni Base - Servizi di Traduzione per Immersive Translate e trovare l'opzione Traduzione Volcano da compilare.
4. Fatto 🎉, se avete dubbi, si prega di fornire feedback [qui](https://github.com/immersive-translate/immersive-translate/issues/137).