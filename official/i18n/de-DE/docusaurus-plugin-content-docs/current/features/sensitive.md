---
sidebar_position: 7
---

# Datenschutzmodus (Beta)

## Leitfaden zur Maskierung sensibler Informationen

> Diese Funktion wird in Plugin-Version 1.23.1+ unterstützt.

Nach der Aktivierung des integrierten oder benutzerdefinierten [OneAIFW](https://github.com/funstory-ai/aifw) identifiziert und maskiert das Plugin automatisch sensible Informationen (wie E-Mail-Adressen, Telefonnummern, Ausweisnummern usw.) während der Übersetzung, um Ihre Privatsphäre und Sicherheit zu schützen. Dieser Leitfaden zeigt Ihnen, wie Sie sehen können, welche sensiblen Informationen während der Übersetzung identifiziert und maskiert wurden.

### Anzeigen der Maskierungsprotokolle

#### Schritt 1: Protokollierung aktivieren

1. Öffnen Sie die [**Entwicklereinstellungsseite**](https://dash.immersivetranslate.com/#advanced) des Plugins
2. Aktivieren Sie die Option **"Konsolenprotokollierung aktivieren"**

#### Schritt 2: Entwicklerkonsole öffnen

1. Drücken Sie `F12` auf der Webseite (oder klicken Sie mit der rechten Maustaste auf die Seite und wählen Sie "Untersuchen" / "Element untersuchen")
2. Wechseln Sie zum Tab "Console" (Konsole)

#### Schritt 3: Maskierungsprotokolle filtern

Geben Sie `sensitive-` in das Filterfeld der Konsole ein, um alle Protokolle im Zusammenhang mit der Maskierung sensibler Informationen zu filtern.

### Erklärung des Protokollformats

In der Konsole sehen Sie Protokolle im folgenden Format:

```
[sensitive-encode] "E-Mail: tester.cn+alias@example.com" -> "E-Mail: __PII_EMAIL_ADDRESS_1__"

[sensitive-decode] "E-Mail: __PII_EMAIL_ADDRESS_1__" -> "E-Mail: tester.cn+alias@example.com"
```

#### Bedeutung der Protokolle

- **`[sensitive-encode]`**: Zeigt den Prozess der Identifizierung und Maskierung sensibler Informationen an
  - Die linke Seite ist der ursprüngliche Text (enthält sensible Informationen)
  - Die rechte Seite ist der maskierte Text (`__PII_*` ist der Maskierungsplatzhalter)

- **`[sensitive-decode]`**: Zeigt den Prozess der Wiederherstellung des maskierten Textes an
  - Die linke Seite ist der maskierte Text (enthält Platzhalter)
  - Die rechte Seite ist der wiederhergestellte ursprüngliche Text

#### Erklärung der Platzhalter

Platzhalter im Format `__PII_*` repräsentieren den Typ der maskierten sensiblen Informationen, zum Beispiel:
- `__PII_EMAIL_ADDRESS_1__`: E-Mail-Adresse
- `__PII_PHONE_NUMBER_1__`: Telefonnummer
- `__PII_ID_CARD_1__`: Ausweisnummer
- usw.

### Prinzipien der Maskierung

Für spezifische Prinzipien und Implementierungsdetails zur Maskierung sensibler Informationen können Sie die Dokumentation und den Code des [OneAIFW-Projekts](https://github.com/funstory-ai/aifw) einsehen.

### Hinweise

- Diese Funktion befindet sich derzeit in der **Beta-Testphase**, und es kann Fälle von ungenauer Identifizierung oder Maskierungsfehlern geben
- Wenn Sie auf Maskierungsfehler oder Identifizierungsfehler stoßen, senden Sie bitte Feedback über [GitHub Issues](https://github.com/funstory-ai/aifw/issues), und wir werden weiter iterieren und optimieren

