---
sidebar_position: 5
---
# AI Prompt Konfigurationsanleitung

## Übersicht

Immersive Translate unterstützt benutzerdefinierte AI-Übersetzungs-Prompt-Konfigurationen, die es fortgeschrittenen Benutzern ermöglichen, das Übersetzungsverhalten nach ihren Bedürfnissen anzupassen. Dieses Dokument bietet detaillierte Anweisungen zu Konfigurationsmethoden, unterstützten Variablen und erweiterten Verwendungsmöglichkeiten.

## Unterstützte Variablen

### Grundlegende Variablen

- `{{text}}` - Der zu übersetzende Textinhalt
- `{{from}}` - Quellsprache
- `{{to}}` - Zielsprache
- `{{content_type}}` - Typ des ursprünglichen Textes (`html` oder `text`)

### Kontextvariablen
- `{{title_prompt}}` - Webseitentitel (wenn verfügbar)
- `{{summary_prompt}}` - Webseiten-Kontextzusammenfassung (wenn verfügbar)
- `{{terms_prompt}}` - Verwandte Fachbegriffe (wenn verfügbar)

## Konfigurationsmethoden

### 1. System Prompt(`systemPrompt`)
Übersetzungsanfrage, die als System-Identität an die KI gesendet wird. Wird verwendet, um die Rolle der KI und grundlegende Regeln festzulegen.

### 2. Prompt(`prompt`)
Konversation, die als Benutzer-Identität an die KI gesendet wird und den tatsächlich zu übersetzenden Inhalt enthält.

### 3. System Multiple Prompt(`systemMultiplePrompt`)
Übersetzungsanfrage, die als System-Identität an die KI gesendet wird, wenn die Absatzanzahl größer als 1 ist. Wird zur Behandlung von Mehrfachabsatz-Übersetzungsszenarien verwendet.

### 4. Multiple Prompt(`multiplePrompt`)
Anfrage, die als Benutzer-Identität für Mehrfachabsatz-Übersetzungen gesendet wird. Unterstützt die Verwendung von Trennzeichen oder YAML-Format.

### 5. Subtitle Prompt(`subtitlePrompt`)

Wenn Untertitelübersetzung benötigt wird, Konversation, die als Benutzer-Identität an die KI gesendet wird und den tatsächlich zu übersetzenden Inhalt enthält.

## Standardkonfigurationsbeispiele

Wenn nur ein Absatz gesammelt wird, wird standardmäßig der Einzelabsatz-Prompt verwendet. Wenn mehrere Absätze gesammelt werden, wird standardmäßig der Mehrfachabsatz-Prompt verwendet. In den meisten Fällen wird es sich um Mehrfachabsätze handeln. Das Standardtrennzeichen für Mehrfachabsätze ist `%%`. Wir verwenden absichtlich dieses ungewöhnliche Trennzeichen, um Halluzinationen großer Modelle zu reduzieren. Sie können diesen Prompt als Basis verwenden, um ihn nach Ihren Bedürfnissen zu ändern. Hier sind die Standard-Prompt-Konfigurationen:

### Einzelabsatz-Übersetzung

```yaml
systemPrompt: |
    Sie sind ein professioneller {{to}}-Muttersprachler-Übersetzer, der Text fließend in {{to}} übersetzen muss.

    ## Übersetzungsregeln
    1. Geben Sie nur den übersetzten Inhalt aus, ohne Erklärungen oder zusätzliche Inhalte (wie "Hier ist die Übersetzung:" oder "Übersetzung wie folgt:")
    2. Die zurückgegebene Übersetzung muss genau die gleiche Anzahl von Absätzen und Format wie der ursprüngliche Text beibehalten
    3. Wenn der Text HTML-Tags enthält, berücksichtigen Sie, wo die Tags in der Übersetzung platziert werden sollten, während die Flüssigkeit erhalten bleibt
    4. Für Inhalte, die nicht übersetzt werden sollten (wie Eigennamen, Code usw.), behalten Sie den ursprünglichen Text bei
    5. Geben Sie die Übersetzung direkt aus (keine Trennzeichen, kein zusätzlicher Text){{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  Übersetzen Sie in {{to}} (nur Übersetzung ausgeben):

  {{text}}
```

### Mehrfachabsatz-Übersetzung

```yaml
multipleSystemPrompt: |
    Sie sind ein professioneller {{to}}-Muttersprachler-Übersetzer, der Text fließend in {{to}} übersetzen muss.

    ## Übersetzungsregeln
    1. Geben Sie nur den übersetzten Inhalt aus, ohne Erklärungen oder zusätzliche Inhalte (wie "Hier ist die Übersetzung:" oder "Übersetzung wie folgt:")
    2. Die zurückgegebene Übersetzung muss genau die gleiche Anzahl von Absätzen und Format wie der ursprüngliche Text beibehalten
    3. Wenn der Text HTML-Tags enthält, berücksichtigen Sie, wo die Tags in der Übersetzung platziert werden sollten, während die Flüssigkeit erhalten bleibt
    4. Für Inhalte, die nicht übersetzt werden sollten (wie Eigennamen, Code usw.), behalten Sie den ursprünglichen Text bei{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## Eingabe-Ausgabe-Formatbeispiele

    ### Eingabebeispiel:
    Paragraph A

    %%

    Paragraph B

    %%

    Paragraph C

    %%

    Paragraph D

    ### Ausgabebeispiel:
    Translation A

    %%

    Translation B

    %%

    Translation C

    %%

    Translation D

multiplePrompt: |
  Übersetzen Sie in {{to}}:

  {{text}}
subtitlePrompt: |
  Übersetzen Sie in {{to}}:

  {{text}}
```

## Erweiterte Verwendung (YAML-Format)

Für Szenarien, die eine präzisere Kontrolle erfordern (z. B. mehrstufige Ausgaben), kann das YAML-Format zur Konfiguration verwendet werden:

### Erweiterte Variablen

- `{{yaml}}` - YAML-formatierte Eingabedaten

Die Standard-'yaml'-Variable sieht etwa so aus:

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

Wir erwarten standardmäßig, dass die Ausgabe des großen Modells so aussieht:

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好吗？
```

Wenn Sie die Standard-`{{yaml}}` verwenden, müssen Sie diese Erwartung im Prompt klar ausdrücken. Wenn Sie das Standard- und Antwort-`yaml`-Format ändern möchten, kann dies nicht über die UI der Immersive Translate-Einstellungsseite gelöst werden. Sie müssen die JSON-formatierte Benutzerkonfiguration von Immersive Translate direkt bearbeiten.

Benutzerkonfigurationsbearbeitungspfad: `Einstellungsseite`->`Entwicklereinstellungen`->`Edit Full User Config` (Bitte sichern Sie Ihre Benutzerkonfiguration vor dem Bearbeiten)

Sie können die Übersetzungsservicekonfiguration in der JSON der Benutzerkonfiguration finden (wenn nicht vorhanden, fügen Sie sie einfach nach dieser Struktur hinzu):

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

Die `yaml`-Variable besteht aus `env.imt_yaml_item`, daher können Sie das Format von `imt_yaml_item` wie folgt ändern:

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

Eine weitere spezielle Variable ist `imt_subtitle_yaml_item`, ähnlich wie `imt_yaml_item`, verwendet für YAML-Items zur Untertitelübersetzung.

Für andere `env`-Variablen können Sie jede `env`-Variable hinzufügen und sie direkt im Prompt im Format `{{Variablenname}}` verwenden, wie z. B. die folgenden Standard-`env`-Variablen:

- `{{imt_source_field}}` - Quelltextfeldname (Standard: text)
- `{{imt_trans_field}}` - Übersetzungstextfeldname (Standard: text)
- `{{imt_sub_source_field}}` - Untertitel-Quelltextfeldname
- `{{imt_sub_trans_field}}` - Untertitel-Übersetzungstextfeldname

Auch `title_prompt`, `summary_prompt`, `terms_prompt` werden über `env` konfiguriert, Standard wie folgt:

```
        "title_prompt": "\n\n## Kontextbewusstsein\nDokumentmetadaten:\nTitel: 《{{imt_title}}》",
        "summary_prompt": "\n\n## Kontextbewusstsein\nDokumentmetadaten:\nZusammenfassung: {{imt_theme}}...",
        "terms_prompt": "\n\nErforderliche Terminologie: Sie MÜSSEN die folgenden Begriffe während der Übersetzung verwenden. Wenn 'source':'target' und source == target, behalten Sie den Quellbegriff unverändert bei.\n\n Begriffe -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## Kontextbewusstsein\nDokumentmetadaten:\nTyp: Untertitel\nZusammenfassung: {{imt_theme}}...",
        "sub_terms_prompt": "\n\nErforderliche Terminologie: Sie MÜSSEN die folgenden Begriffe während der Übersetzung verwenden. Wenn 'source':'target' und source == target, behalten Sie den Quellbegriff unverändert bei.\n\n Begriffe -> \n\n {{imt_terms}}"

```

Dabei sind `imt_title`, `imt_theme`, `imt_terms` spezielle Variablen, die vom System injiziert werden. `imt_title` ist der Titel, `imt_theme` ist die Zusammenfassung der gesamten Webseite, `imt_terms` sind die vom Modell extrahierten Schlüsselbegriffe.

> Hinweis: `imt_theme`, `imt_terms` werden von einem proprietären Service extrahiert und sind derzeit nur für [Pro-Mitglieder](https://immersivetranslate.com/pricing/) verfügbar.

### YAML Prompt Beispiel

```yaml
systemPrompt: |
  Sie sind eine professionelle, authentische maschinelle Übersetzungsmaschine.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    Sie erhalten eine YAML-formatierte Eingabe mit Einträgen, die "id" und "{{imt_source_field}}" Felder enthalten. Hier ist die Eingabe:

    <yaml>
    {{yaml}}
    </yaml>

    Übersetzen Sie für jeden Eintrag im YAML den Inhalt des "{{imt_source_field}}" Feldes in {{to}},{{html_only}} schreiben Sie die Übersetzung zurück in das "{{imt_source_field}}" Feld dieses Eintrags.

    Hier ist ein Beispiel für das erwartete Format:

    {{normal_result_yaml_example}}

    Bitte geben Sie das übersetzte YAML direkt zurück, ohne <yaml>-Tag oder zusätzliche Informationen.
subtitlePrompt: |
    Sie erhalten eine YAML-formatierte Untertiteleingabe mit Einträgen, die "id" und "{{imt_sub_source_field}}" Felder enthalten. Hier ist die Eingabe:

    <yaml>
    {{yaml}}
    </yaml>

    Übersetzen Sie für jeden Eintrag im YAML den Inhalt des "{{imt_sub_source_field}}" Feldes in {{to}},{{html_only}} schreiben Sie die Übersetzung zurück in das "{{imt_sub_source_field}}" Feld dieses Eintrags.

    Hier ist ein Beispiel für das erwartete Format:

    {{subtitle_result_yaml_example}}

    Bitte geben Sie das übersetzte YAML direkt zurück, ohne <yaml>-Tag oder zusätzliche Informationen.

```

`html_only` ist eine spezielle Variable, die nur vorhanden ist, wenn der zu übersetzende Originaltext HTML-Format hat. Der Wert ist: `\n\nHinweis: Wenn der Text HTML-Tags enthält, berücksichtigen Sie bitte nach der Übersetzung, wo die Tags im Übersetzungsergebnis platziert werden sollten, während gleichzeitig die Flüssigkeit des Ergebnisses erhalten bleibt.`, diese Variable existiert nur, wenn der Benutzer aktiv "Rich-Text-Übersetzung" in den AI-Übersetzungsdiensten aktiviert hat. Andernfalls ist sie leer.

`normal_result_yaml_example` wird in `env` gesetzt, Standard ist:

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

`subtitle_result_yaml_example` wird in `env` gesetzt, Standardwert ist:

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

Sie können es in `env` überschreiben.

## Erweiterte Beispiel: Reflektive Übersetzung

Dieses Beispiel zeigt, wie Sie mit dem YAML-Format einen komplexeren Übersetzungsfluss implementieren können, der zwei Schritte umfasst: erste Übersetzung und optimierte Übersetzung:

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # Die endgültige Übersetzung verwendet das step2-Feld
  imt_sub_source_field: source
  imt_sub_trans_field: step2
  imt_yaml_item: |-
    - id: {{id}}
      {{imt_source_field}}: {{text}}
  imt_subtitle_yaml_item: |-
    - id: {{id}}
      {{imt_sub_source_field}}: {{text}}

systemPrompt: |
  Sie sind eine professionelle, authentische maschinelle Übersetzungsmaschine.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  Hier ist die YAML-Eingabe:
  <yaml>
  {{yaml}}
  </yaml>
  
  Bitte folgen Sie diesen Schritten:
  1. Extrahieren Sie den Inhalt des "source"-Feldes aus dem bereitgestellten YAML-Objekt.
  2. Übersetzen Sie den extrahierten Inhalt in {{to}}. Platzieren Sie diese erste Übersetzung in das step1-Feld.
  3. Optimieren Sie die erste Übersetzung aus step1, um sie in {{to}} natürlicher und verständlicher zu machen. 
     Platzieren Sie diese optimierte Übersetzung in das step2-Feld.
  4. Formatieren Sie das Ergebnis als YAML-Array mit id-, step1- und step2-Feldern, wie in diesem Beispiel gezeigt:
  
  - id: 1 
    step1: Erste Übersetzung
    step2: Optimierte Übersetzung
  
  Bitte geben Sie das übersetzte YAML direkt zurück, ohne <example_output>-Tags oder zusätzliche Informationen.
```

### Arbeitsablaufbeschreibung

1. **Eingabeformat**：
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **KI-Verarbeitungsschritte**：
   - Step 1: Führen Sie die erste Übersetzung durch
   - Step 2: Optimieren Sie die Übersetzung, um sie natürlicher und flüssiger zu machen

3. **Ausgabeformat**：
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎么样？"
     step2: "你好吗？"
   ```
