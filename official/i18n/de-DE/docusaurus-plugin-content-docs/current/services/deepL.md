# DeepL

## Direkter Zugriff auf DeepL Übersetzungsdienste nach Eröffnung einer [Immersive Translate Pro Mitgliedschaft](https://immersivetranslate.com/en/pricing/) (Empfohlen)

[Klicken Sie hier für die Präsentation](https://immersivetranslate.com/en/pricing/)

## Holen Sie sich die offizielle DeepL API über DeepL

1. Offizielle Einführung: [DeepL API](https://www.deepl.com/en/pro#developer)
   - Beachten Sie, dass: [DeepL API](https://www.deepl.com/en/pro#developer) und [DeepL Pro](https://www.deepl.com/pro) zwei verschiedene Kontotypen sind, und das [DeepL API](https://www.deepl.com/en/pro/select-country#developer) Konto.

2. [Warum](https://www.deepl.com/en/whydeepl) DeepL wählen?

   - Englisch ⇄ Chinesisch 5x genauer
   - Englisch ⇄ Japanisch 6x genauer
   - Übersetzungsmotor basierend auf künstlicher Intelligenz Technologie (neuronale Netzwerke)

3. Die DeepL API ist unterteilt in [Free API und Pro API](https://www.deepl.com/en/pro#developer)

   - Die Free API bietet 500.000 kostenlose Zeichen pro Monat.
   - Die [offizielle Gebühr](https://www.deepl.com/en/pro#developer) für die Pro API beträgt: 25 $ pro 1 Million Zeichen.
   - Für einen Nutzer mit hoher Frequenz beträgt die Menge der verbrauchten Zeichen in einem Monat etwa 10 Millionen Zeichen, und der Preis beträgt etwa: 250 USD

4. Um ein Konto zu registrieren und die [DeepL API](https://www.deepl.com/en/pro#developer) zu eröffnen.

## Bauen Sie Ihre eigene DeepL API

Wir experimentieren mit der Unterstützung für unseren eigenen DeeplX-Dienst im Beta-Feature (aber es ist nicht gut als Webübersetzungsdienst geeignet, wie getestet. Aufgrund der riesigen Menge an API-Anfragen für die Übersetzung von Webseiten, wenn Sie diesen Dienst aufbauen, stellen Sie bitte sicher, dass Sie eine gute Lastverteilung durchführen), folgendes ist, wie man die experimentellen Funktionen der Anweisungen aktiviert:

1. Beta-Testfunktionen in den Entwicklereinstellungen aktivieren
2. Finden Sie DeepLX (Beta) in den Grundeinstellungen und geben Sie die selbstgebaute DeepL API URL ein, z.B. http\://ihre-domain/translate

> F: Wie baue ich meine eigene auf?
>
> A: [OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate) oder [zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md)

## Häufige Probleme

### 1. Der eingegebene Schlüssel ist nicht verfügbar.

DeepL API Pro und DeepL Pro sind zwei Arten von Konten, der Auth Key, der in Immersive Translate verwendet werden kann, ist das DeepL API-Konto, bitte klicken Sie hier für [DeepL API Pro](https://www.deepl.com/en/pro/select-country#) Entwickler)

### 2. Deepl Free API Meldung 401 Keine Berechtigung

Deepl Free API-Schlüssel enden alle auf `:fx`, alles andere ist kein Free API-Schlüssel.

### 3. 456, Kontingent für Benutzer wurde erreicht.

Die Nutzung hat das offizielle harte Limit von DeepL pro Benutzer überschritten, Sie haben möglicherweise die Fair-Use-Richtlinie von DeepL verletzt und werden darauf hingewiesen, solches Verhalten zu vermeiden. Wenn Sie ein zahlender Abonnent sind, wird die Nutzung im nächsten Monat automatisch zurückgesetzt.