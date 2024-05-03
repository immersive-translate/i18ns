# Microsoft Azure Übersetzung

## Kurze Erklärung

1. Offizielle Webseite: [Übersetzt von Microsoft Azure](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/text-translation-overview)
2. Offizielle Beschreibung: Übersetzungen sind bis zu 2 Millionen Wörter pro Monat kostenlos, wenn Sie 2 Millionen Wörter pro Monat überschreiten, berechnen wir Ihnen einen Tarif von 10 $ / 1 Million Wörter. Für weitere Details siehe bitte [Preisinformation](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/)

## Registrierungsprozess

Der Registrierungsprozess ist umständlicher als bei anderen Übersetzungsdiensten und erfordert Geduld.

Referenzlink: [Microsoft Azure Übersetzung Einstieg Dokumentation](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)

## Registrieren Sie sich für ein Azure-Konto

Der erste Schritt besteht darin, sich für ein [Azure](https://azure.microsoft.com/en-us/free/cognitive-services/) Konto zu registrieren, was das Binden einer internationalen Kreditkarte (Visa/Master) erfordert. Ohne dies ist eine Registrierung nicht möglich.

## Registrierung für ein Azure Blob Speicherkonto

Schritt 2: Registrieren Sie sich für ein [Azure Blob](https://portal.azure.com/#create/Microsoft.StorageAccount) Speicherkonto.

1. Erstellen Sie eine neue Ressourcengruppe und füllen Sie den Namen des Speicherkontos aus.
2. Wählen Sie eine Region, die Ihnen am nächsten liegt, zum Beispiel wäre die Region Hongkong `Ostasien`.
3. Der Rest des Prozesses ist einfach der nächste Schritt. Auf der letzten Seite, nachdem die Bereitstellung abgeschlossen ist, klicken Sie auf den blauen Button "Erstellen" unten links.

## Erstellung von Übersetzungswerkzeugen

Schritt 3: Erstellen Sie ein [Übersetzungswerkzeug](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation)

1. Wählen Sie eine Region, die Ihnen am nächsten liegt, zum Beispiel wäre die Region Hongkong `Ostasien`.
2. Preiskategorien werden nach Bedarf ausgewählt, mit `Free F0` für kostenlose Nutzer verfügbar. Die kostenlose Stufe unterstützt keine Dokumentübersetzung. Ein Standard S1-Test kann bei Bedarf verwendet werden.
3. Der Rest des Prozesses ist einfach der nächste Schritt. Auf der letzten Seite, nachdem die Bereitstellung abgeschlossen ist, klicken Sie auf den blauen Button "Erstellen" unten links.

## Zugangsschlüssel

Nach erfolgreicher Bereitstellung gehen Sie zum [Azure-Dashboard](https://portal.azure.com/#home), gehen Sie zur Seite für **Übersetzungswerkzeuge** und finden Sie den Schlüssel im linken Menü - Ressourcenverwaltung - `Schlüssel und Endpunkte`. Microsoft wird 2 Schlüssel bereitstellen, wählen Sie einen aus und füllen Sie den Schlüssel in das `APIKEY` der Immersive Extension - Microsoft Translator.

Unterhalb des Schlüssels befinden sich auch Informationen zu `Standort/Region`, z. B. `ostasien`, die ebenfalls im `Region` der immersiven Erweiterung - Microsoft Translate - ausgefüllt werden müssen.

## Häufige Probleme

Bei Unklarheiten geben Sie bitte [hier](https://github.com/immersive-translate/immersive-translate/issues/137) ein Feedback.