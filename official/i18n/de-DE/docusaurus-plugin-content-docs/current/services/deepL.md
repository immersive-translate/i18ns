# DeepL

## Direkter Zugriff auf DeepL-Übersetzungsdienste nach Eröffnung einer [Immersive Translate Pro-Mitgliedschaft](https://immersivetranslate.com/en/pricing/) (Empfohlen)

[Mehr erfahren](https://immersivetranslate.com/en/pricing/)

## Erhalten Sie die offizielle DeepL API über DeepL

1. Offizielle Einführung: [DeepL API](https://www.deepl.com/en/pro#developer)

   - Beachten Sie, dass: [DeepL API](https://www.deepl.com/en/pro#developer) und [DeepL Pro](https://www.deepl.com/pro) zwei verschiedene Kontotypen sind, und das [DeepL API](https://www.deepl.com/en/pro/select-country#developer) Konto.

2. [Warum](https://www.deepl.com/en/whydeepl) DeepL wählen?

   - Englisch ⇄ Chinesisch 5x genauer
   - Englisch ⇄ Japanisch 6x genauer
   - Übersetzungsmaschine basierend auf künstlicher Intelligenz-Technologie (neuronale Netzwerke)

3. Die DeepL API ist unterteilt in [Free API und Pro API](https://www.deepl.com/en/pro#developer)

   - Die Free API bietet 500.000 kostenlose Zeichen pro Monat.
   - Die [offizielle Gebühr](https://www.deepl.com/en/pro#developer) für die Pro API beträgt: 25 USD pro 1 Million Zeichen.
   - Für einen Hochfrequenzbenutzer beträgt die Anzahl der in einem Monat verbrauchten Zeichen etwa 10 Millionen Zeichen, und der Preis beträgt etwa: 250 USD

4. Um ein Konto zu registrieren und die [DeepL API](https://www.deepl.com/en/pro#developer) zu öffnen.

## Häufige Probleme

### 1. Der eingegebene Schlüssel ist nicht verfügbar.

DeepL API Pro und DeepL Pro sind zwei Arten von Konten, der Auth Key, der in Immersive Translate verwendet werden kann, ist das DeepL API-Konto, bitte klicken Sie hier für [DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer)

### 2. Fehlerbehebung bei 401, 403 Authentifizierungsfehlern

Diese Fehler treten typischerweise auf, wenn Sie den falschen Authentifizierungsschlüsseltyp verwenden. Bitte beachten Sie:

1. DeepL bietet zwei verschiedene Produkte an: DeepL Pro (Übersetzungsdienst) und DeepL API (Entwicklerschnittstelle)
2. Die in Ihren DeepL Pro-Kontoeinstellungen gefundenen Schlüssel sind **nicht kompatibel** mit API-Aufrufen
3. Sie müssen sich speziell für ein DeepL API-Konto registrieren, um einen API-Schlüssel zu erhalten
4. DeepL Free API-Schlüssel sind daran zu erkennen, dass sie mit `:fx` enden
5. DeepL Pro API-Schlüssel haben nicht das `:fx`-Suffix und erscheinen als reguläre Zeichenfolge

Bitte stellen Sie sicher, dass Sie sich ordnungsgemäß für den DeepL API-Dienst registriert haben, nicht nur für den DeepL Pro-Übersetzungsdienst.

### 3. 456, Kontingent für Benutzer wurde erreicht.

Die Nutzung hat das offizielle Hard-Limit von DeepL pro Benutzer überschritten, Sie haben möglicherweise gegen die Fair-Use-Richtlinie von DeepL verstoßen und sollten ein solches Verhalten vermeiden. Wenn Sie ein zahlender Abonnent sind, wird die Nutzung im nächsten Monat automatisch zurückgesetzt.