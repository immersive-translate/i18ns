# Vulkanübersetzung

## Kurze Aussage

1. Offizielle Webseite: [Maschinenübersetzung - Vulkan Engine](https://www.volcengine.com/product/machine-translation)
2. Offizielle Tarifbeschreibung: [Produktabrechnung Maschinenübersetzung - Vulkan Engine](https://www.volcengine.com/docs/4640/68515)
3. Der Vulkan Übersetzer ist für die ersten 2 Millionen Zeichen pro Monat kostenlos und berechnet 49 $ pro Million Zeichen für den überschreitenden Teil. Bitte überprüfen Sie das offizielle Tarifdokument für Details.

## Anwendungsschritte

1. [API-Zugriffsprozessübersicht Maschinenübersetzung - Vulkan Engine](https://www.volcengine.com/docs/4640/130872), folgen Sie der offiziellen Anleitung, um die drei Schritte der Registrierung eines Kontos, der Echtzeit-Authentifizierung und der Dienstöffnung abzuschließen. Dies muss über die Konsole erfolgen, [Vulkan Engine Konsole](https://console.volcengine.com/home)
2. Im vierten Schritt des Schlüsselerhalts bietet die Vulkan Engine zwei Optionen:
   1. Weiter erstellen (mit dem Hauptkonto den Schlüssel erstellen, bequemer, dieser Schlüssel kann die Hauptkontenressourcen aufrufen, weniger sicher), wählen Sie "Weiter erstellen", die Tabelle erscheint in einem neuen Daten, die den "Zugriffsschlüssel-ID" und "Geheimer Zugriffsschlüssel" enthält, den wir verwenden möchten.
   2. Erstellen Sie einen neuen Unterbenutzer (es wird empfohlen, einen Unterbenutzer zu verwenden, um den Schlüssel für mehr Sicherheit zu erstellen), erhalten Sie die "Zugriffsschlüssel-ID" und "Geheimer Zugriffsschlüssel", dieses Unterkonto muss die `TranslateFullAccess`-Berechtigung haben.
3. Öffnen Sie Grundlegende Einstellungen - Übersetzungsdienste für Immersive Translate und finden Sie die Vulkan-Übersetzungsoption zum Ausfüllen.
4. Fertig 🎉, wenn Sie Zweifel haben, geben Sie bitte [hier](https://github.com/immersive-translate/immersive-translate/issues/137) ein Feedback.