---
sidebar_position: 5
---
# Guida alla Configurazione dei Prompt AI

## Panoramica

Immersive Translate supporta la configurazione personalizzata dei Prompt per la traduzione AI, consentendo agli utenti avanzati di regolare il comportamento della traduzione in base alle proprie esigenze. Questo documento fornisce istruzioni dettagliate sui metodi di configurazione, le variabili supportate e l'uso avanzato.

## Variabili Supportate

### Variabili di Base

- `{{text}}` - Il contenuto del testo da tradurre
- `{{from}}` - Lingua sorgente
- `{{to}}` - Lingua di destinazione
- `{{content_type}}` - Tipo di testo originale (`html` o `text`)

### Variabili di Contesto
- `{{title_prompt}}` - Titolo della pagina web (quando disponibile)
- `{{summary_prompt}}` - Riepilogo del contesto della pagina web (quando disponibile)
- `{{terms_prompt}}` - Terminologia professionale correlata (quando disponibile)

## Metodi di Configurazione

### 1. System Prompt(`systemPrompt`)
Richiesta di traduzione inviata all'AI come identità di sistema. Utilizzata per impostare il ruolo dell'AI e le regole di base.

### 2. Prompt(`prompt`)
Conversazione inviata all'AI come identità utente, contenente il contenuto effettivo da tradurre.

### 3. System Multiple Prompt(`systemMultiplePrompt`)
Richiesta di traduzione inviata all'AI come identità di sistema quando il numero di paragrafi è maggiore di 1. Utilizzata per gestire scenari di traduzione multi-paragrafo.

### 4. Multiple Prompt(`multiplePrompt`)
Richiesta inviata come identità utente per la traduzione multi-paragrafo. Supporta l'uso di separatori o formato YAML.

### 5. Subtitle Prompt(`subtitlePrompt`)

Quando è necessaria la traduzione dei sottotitoli, conversazione inviata all'AI come identità utente, contenente il contenuto effettivo da tradurre.

## Esempi di Configurazione Predefinita

Se viene raccolto solo un paragrafo, utilizzerà il Prompt a paragrafo singolo per impostazione predefinita. Se vengono raccolti più paragrafi, utilizzerà il Prompt multi-paragrafo per impostazione predefinita. La maggior parte dei casi saranno multi-paragrafo. Il separatore predefinito per i paragrafi multipli è `%%`. Utilizziamo deliberatamente questo separatore poco comune per ridurre le allucinazioni dei modelli di grandi dimensioni. Puoi usare questo Prompt come base per modificarlo secondo le tue esigenze. Ecco le configurazioni Prompt predefinite:

### Traduzione a Paragrafo Singolo

```yaml
systemPrompt: |
    Sei un traduttore madrelingua professionale di {{to}} che deve tradurre fluentemente il testo in {{to}}.

    ## Regole di Traduzione
    1. Genera solo il contenuto tradotto, senza spiegazioni o contenuti aggiuntivi (come "Ecco la traduzione:" o "Traduzione come segue:")
    2. La traduzione restituita deve mantenere esattamente lo stesso numero di paragrafi e formato del testo originale
    3. Se il testo contiene tag HTML, considera dove i tag dovrebbero essere posizionati nella traduzione mantenendo la fluidità
    4. Per i contenuti che non dovrebbero essere tradotti (come nomi propri, codice, ecc.), mantieni il testo originale
    5. Genera la traduzione direttamente (nessun separatore, nessun testo aggiuntivo){{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  Traduci in {{to}} (genera solo la traduzione):

  {{text}}
```

### Traduzione Multi-Paragrafo

```yaml
multipleSystemPrompt: |
    Sei un traduttore madrelingua professionale di {{to}} che deve tradurre fluentemente il testo in {{to}}.

    ## Regole di Traduzione
    1. Genera solo il contenuto tradotto, senza spiegazioni o contenuti aggiuntivi (come "Ecco la traduzione:" o "Traduzione come segue:")
    2. La traduzione restituita deve mantenere esattamente lo stesso numero di paragrafi e formato del testo originale
    3. Se il testo contiene tag HTML, considera dove i tag dovrebbero essere posizionati nella traduzione mantenendo la fluidità
    4. Per i contenuti che non dovrebbero essere tradotti (come nomi propri, codice, ecc.), mantieni il testo originale{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## Esempi di Formato Input-Output

    ### Esempio di Input:
    Paragraph A

    %%

    Paragraph B

    %%

    Paragraph C

    %%

    Paragraph D

    ### Esempio di Output:
    Translation A

    %%

    Translation B

    %%

    Translation C

    %%

    Translation D

multiplePrompt: |
  Traduci in {{to}}:

  {{text}}
subtitlePrompt: |
  Traduci in {{to}}:

  {{text}}
```

## Uso Avanzato (Formato YAML)

Per scenari che richiedono un controllo più preciso (ad esempio, output multi-step), è possibile utilizzare il formato YAML per la configurazione:

### Variabili Avanzate

- `{{yaml}}` - Dati di input in formato YAML

La variabile 'yaml' predefinita è così:

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

Prevediamo per impostazione predefinita che l'output del modello di grandi dimensioni sia così:

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好吗？
```

Se usi il `{{yaml}}` predefinito, devi esprimere chiaramente questa aspettativa nel prompt. Se desideri modificare il formato `yaml` predefinito e di risposta, questo non può essere risolto tramite l'interfaccia utente della pagina delle impostazioni di Immersive Translate. Devi modificare direttamente la configurazione utente in formato JSON di Immersive Translate.

Percorso di modifica della configurazione utente: `Pagina Impostazioni`->`Impostazioni Sviluppatore`->`Edit Full User Config` (Si prega di eseguire il backup della configurazione utente prima di modificare)

Puoi trovare la configurazione del servizio di traduzione nel JSON della configurazione utente (se non esiste, aggiungila semplicemente secondo questa struttura):

```
{
  ...
  "translationServices": {
    "openai": {
       ...
      }
  },
  ...

```

La variabile `yaml` è composta da `env.imt_yaml_item`, quindi puoi modificare il formato di `imt_yaml_item` così:

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

Un'altra variabile speciale è `imt_subtitle_yaml_item`, simile a `imt_yaml_item`, utilizzata per gli elementi YAML della traduzione dei sottotitoli.

Per altre variabili `env`, puoi aggiungere qualsiasi variabile `env` e usarla direttamente nel prompt nel formato `{{nome_variabile}}`, come le seguenti variabili `env` predefinite:

- `{{imt_source_field}}` - Nome del campo testo sorgente (predefinito: text)
- `{{imt_trans_field}}` - Nome del campo testo tradotto (predefinito: text)
- `{{imt_sub_source_field}}` - Nome del campo testo sorgente dei sottotitoli
- `{{imt_sub_trans_field}}` - Nome del campo testo tradotto dei sottotitoli

Including `title_prompt`, `summary_prompt`, `terms_prompt` sono anche configurati tramite `env`, predefinito come segue:

```
        "title_prompt": "\n\n## Consapevolezza del Contesto\nMetadati del Documento:\nTitolo: 《{{imt_title}}》",
        "summary_prompt": "\n\n## Consapevolezza del Contesto\nMetadati del Documento:\nRiepilogo: {{imt_theme}}...",
        "terms_prompt": "\n\nTerminologia Richiesta: DEVI usare i seguenti termini durante la traduzione. Se 'source':'target' e source == target, mantieni il termine sorgente invariato.\n\n Termini -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## Consapevolezza del Contesto\nMetadati del Documento:\nTipo: Sottotitolo\nRiepilogo: {{imt_theme}}...",
        "sub_terms_prompt": "\n\nTerminologia Richiesta: DEVI usare i seguenti termini durante la traduzione. Se 'source':'target' e source == target, mantieni il termine sorgente invariato.\n\n Termini -> \n\n {{imt_terms}}"

```

Dove `imt_title`, `imt_theme`, `imt_terms` sono variabili speciali iniettate dal sistema. `imt_title` è il titolo, `imt_theme` è il riepilogo dell'intera pagina web, `imt_terms` sono i termini chiave estratti dal modello.

> Nota: `imt_theme`, `imt_terms` sono estratti da un servizio proprietario e sono attualmente disponibili solo per i [membri Pro](https://immersivetranslate.com/pricing/).

### Esempio YAML Prompt

```yaml
systemPrompt: |
  Sei un motore di traduzione automatica professionale e autentico.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    Riceverai un input in formato YAML contenente voci con campi "id" e "{{imt_source_field}}". Ecco l'input:

    <yaml>
    {{yaml}}
    </yaml>

    Per ogni voce nel YAML, traduci il contenuto del campo "{{imt_source_field}}" in {{to}},{{html_only}} scrivi la traduzione nel campo "{{imt_source_field}}" di quella voce.

    Ecco un esempio del formato atteso:

    {{normal_result_yaml_example}}

    Si prega di restituire il YAML tradotto direttamente senza tag <yaml> o informazioni aggiuntive.
subtitlePrompt: |
    Riceverai un input di sottotitoli in formato YAML contenente voci con campi "id" e "{{imt_sub_source_field}}". Ecco l'input:

    <yaml>
    {{yaml}}
    </yaml>

    Per ogni voce nel YAML, traduci il contenuto del campo "{{imt_sub_source_field}}" in {{to}},{{html_only}} scrivi la traduzione nel campo "{{imt_sub_source_field}}" di quella voce.

    Ecco un esempio del formato atteso:

    {{subtitle_result_yaml_example}}

    Si prega di restituire il YAML tradotto direttamente senza tag <yaml> o informazioni aggiuntive.

```

`html_only` è una variabile speciale che esiste solo quando il testo originale da tradurre è in formato HTML. Il valore è: `\n\nNota: Se il testo contiene tag HTML, si prega di considerare dopo la traduzione dove i tag dovrebbero essere nel risultato della traduzione, mantenendo allo stesso tempo la fluidità del risultato.`, questa variabile esiste solo quando l'utente attiva attivamente "Traduzione Rich Text" nei servizi di traduzione AI. Altrimenti è vuota.

`normal_result_yaml_example` è impostato in `env`, il predefinito è:

```
<example>
Input:
  - id: 1
    {{imt_source_field}}: Source
Output:
  - id: 1
    {{imt_trans_field}}: Translation
</example>
```

`subtitle_result_yaml_example` è impostato in `env`, il valore predefinito è:

```
<example>
Input:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
Output:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
</example>

```

Puoi sovrascriverlo in `env`.

## Esempio Avanzato: Traduzione Riflessiva

Questo esempio mostra come usare il formato YAML per implementare un flusso di traduzione più complesso, includendo due passaggi: traduzione iniziale e traduzione ottimizzata:

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # La traduzione finale usa il campo step2
  imt_sub_source_field: source
  imt_sub_trans_field: step2
  imt_yaml_item: |-
    - id: {{id}}
      {{imt_source_field}}: {{text}}
  imt_subtitle_yaml_item: |-
    - id: {{id}}
      {{imt_sub_source_field}}: {{text}}

systemPrompt: |
  Sei un motore di traduzione automatica professionale e autentico.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  Ecco l'input YAML:
  <yaml>
  {{yaml}}
  </yaml>
  
  Si prega di seguire questi passaggi:
  1. Estrai il contenuto del campo "source" dall'oggetto YAML fornito.
  2. Traduci il contenuto estratto in {{to}}. Posiziona questa traduzione iniziale nel campo step1.
  3. Ottimizza la traduzione iniziale da step1 per renderla più naturale e comprensibile in {{to}}. 
     Posiziona questa traduzione ottimizzata nel campo step2.
  4. Formatta il risultato come un array YAML con campi id, step1 e step2, come mostrato in questo esempio:
  
  - id: 1 
    step1: Traduzione iniziale
    step2: Traduzione ottimizzata
  
  Si prega di restituire il YAML tradotto direttamente senza tag <example_output> o informazioni aggiuntive.
```

### Descrizione del Flusso di Lavoro

1. **Formato di Input**：
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **Passaggi di Elaborazione AI**：
   - Passo 1: Esegui la traduzione iniziale
   - Passo 2: Ottimizza la traduzione per renderla più naturale e fluida

3. **Formato di Output**：
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎么样？"
     step2: "你好吗？"
   ```
