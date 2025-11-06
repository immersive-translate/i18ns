---
sidebar_position: 7
---

# Modalità privacy (Beta)

## Guida alla mascheramento delle informazioni sensibili

> Questa funzionalità è supportata nella versione 1.23.1+ del plugin.

Dopo aver abilitato [OneAIFW](https://github.com/funstory-ai/aifw) integrato o personalizzato, il plugin identificherà e maschera automaticamente le informazioni sensibili (come indirizzi email, numeri di telefono, numeri di carta d'identità, ecc.) durante la traduzione per proteggere la tua privacy e sicurezza. Questa guida ti mostrerà come vedere quali informazioni sensibili sono state identificate e mascherate durante la traduzione.

### Visualizzazione dei log di mascheramento

#### Passo 1: Abilitare la registrazione

1. Apri la [**pagina delle impostazioni sviluppatore**](https://dash.immersivetranslate.com/#advanced) del plugin
2. Abilita l'opzione **"Abilita registrazione console"**

#### Passo 2: Aprire la console sviluppatore

1. Premi `F12` sulla pagina web (o fai clic destro sulla pagina e seleziona "Ispeziona" / "Ispeziona elemento")
2. Passa alla scheda "Console"

#### Passo 3: Filtrare i log di mascheramento

Inserisci `sensitive-` nella casella di filtro della console per filtrare tutti i log relativi al mascheramento delle informazioni sensibili.

### Spiegazione del formato del log

Nella console, vedrai log nel seguente formato:

```
[sensitive-encode] "Email: tester.cn+alias@example.com" -> "Email: __PII_EMAIL_ADDRESS_1__"

[sensitive-decode] "Email: __PII_EMAIL_ADDRESS_1__" -> "Email: tester.cn+alias@example.com"
```

#### Significato dei log

- **`[sensitive-encode]`**: Indica il processo di identificazione e mascheramento delle informazioni sensibili
  - Il lato sinistro è il testo originale (che contiene informazioni sensibili)
  - Il lato destro è il testo mascherato (`__PII_*` è il segnaposto di mascheramento)

- **`[sensitive-decode]`**: Indica il processo di ripristino del testo mascherato
  - Il lato sinistro è il testo mascherato (che contiene segnaposto)
  - Il lato destro è il testo originale ripristinato

#### Spiegazione dei segnaposto

I segnaposto nel formato `__PII_*` rappresentano il tipo di informazioni sensibili che sono state mascherate, ad esempio:
- `__PII_EMAIL_ADDRESS_1__`: Indirizzo email
- `__PII_PHONE_NUMBER_1__`: Numero di telefono
- `__PII_ID_CARD_1__`: Numero di carta d'identità
- ecc.

### Principi di mascheramento

Per i principi specifici e i dettagli di implementazione del mascheramento delle informazioni sensibili, puoi consultare la documentazione e il codice del [progetto OneAIFW](https://github.com/funstory-ai/aifw).

### Note

- Questa funzionalità è attualmente in **fase di test beta**, e potrebbero esserci casi di identificazione imprecisa o fallimenti di mascheramento
- Se riscontri fallimenti di mascheramento o errori di identificazione, invia feedback tramite [GitHub Issues](https://github.com/funstory-ai/aifw/issues), e continueremo a iterare e ottimizzare

