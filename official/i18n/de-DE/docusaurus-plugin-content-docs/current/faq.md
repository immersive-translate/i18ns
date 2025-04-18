---
sidebar_position: 9
---

# FAQ

## Sicherheitsbezogen

### 1. Android App, schwebender Ball verschwunden

Alte Versionen von Add-ons sind deaktiviert. Deinstallieren Sie sie und installieren Sie die neueste Version von der [offiziellen Website](https://immersivetranslate.com/).

## Installationsbezogen

### 1. Wie man die Erweiterung aktualisiert

Im Allgemeinen werden Erweiterungen, die im Browser-Store installiert sind, automatisch aktualisiert, normalerweise innerhalb eines Tages nach dem Update der Erweiterung. Wenn Sie sofort auf die neueste Version aktualisieren möchten, können Sie die [Erweiterungsverwaltung] des Browsers aufrufen, den [Entwicklermodus] aktivieren und dann oben auf [Aktualisieren] klicken, um sofort auf die neueste Version im Store zu aktualisieren.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

### 2. Immersive Translate Tampermonkey unterstützte Browser

iOS:

- [Tamper Monkey Browser](https://www.tampermonkey.net/)
- Safari-Browser mit installierter Tampermonkey-Erweiterung, kompatible Erweiterungen:
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171): Es wird empfohlen, das Immersive Translate Optimierungsskript direkt aus dem eigenen Store von Stay zu suchen (speziell für Stay optimiert).

Android:

- [Firefox neueste Version](https://www.firefox.com.cn/download/#product-android-release): Nach der Installation die [Tamper Monkey](https://www.tampermonkey.net/) Erweiterung installieren.
- [X Browser](https://www.xbext.com/?ref=immersive-translate): Nach der Installation direkt die [Immersive Translate Tampermonkey Skriptadresse](https://download.immersivetranslate.com/immersive-translate.user.js) öffnen, um zu installieren.

Bekannte Browser, die Tampermonkey-Erweiterungen nicht unterstützen (diese Browser haben die erforderliche Tampermonkey-API nicht implementiert):

- Android Via Browser
- iOS Alook Browser

### 3. Fehler bei der Installation des Plugin-Installers auf Chrome

Fehler `invalid value for web_accessible_resource[0]`: Chromium-Version größer als 88 ist erforderlich, um manifest_version 3 zu unterstützen.

### 4. Wie man den 360 Browser installiert

Nur der 360 Extreme Browser X wird unterstützt, denken Sie daran, dass es mit X ist. Wenn Sie auf den Google Extensions Store zugreifen können, können Sie direkt dort installieren. Wenn Sie keinen Zugriff haben, [installieren Sie es manuell](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features).

### 5. Opera-Browser funktioniert nicht

Es funktioniert nicht auf google.com und anderen Suchseiten, das Plugin zeigt `Bitte aktualisieren Sie die aktuelle Seite, bevor Sie mit der Übersetzung beginnen` und das Aktualisieren der Seite zeigt weiterhin diese Nachricht: Sie müssen "Immersive Translate" in den Opera-Plugin-Einstellungen finden und die Option "Zugriff auf Suchergebnisseiten erlauben" aktivieren.

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

### 6. Kann Erweiterungen auf iOS-Geräten nicht aktivieren

Wenn Sie Erweiterungen auf Ihrem iOS-Gerät nicht aktivieren können, folgen Sie diesen Schritten:

1. Öffnen Sie die [Einstellungen] App
2. Scrollen Sie nach unten und tippen Sie auf [Bildschirmzeit]
3. Wählen Sie [Inhalts- & Datenschutzbeschränkungen]
4. Tippen Sie auf [Inhaltsbeschränkungen]
5. Wählen Sie [Web-Inhalte] und setzen Sie es auf [Unbeschränkt]

Wenn Sie die anderen Funktionen der Inhalts- & Datenschutzbeschränkungen nicht benötigen, können Sie auch einfach die Inhalts- & Datenschutzbeschränkungen deaktivieren:

1. Öffnen Sie die [Einstellungen] App
2. Wählen Sie [Bildschirmzeit]
3. Deaktivieren Sie [Inhalts- & Datenschutzbeschränkungen]

### 7. Safari-Einstellungsseite lädt ständig

Systemeinstellungen -> Safari-Browser -> Erweitert -> Website-Daten -> Bearbeiten, suchen Sie immersivetranslate.com und löschen Sie es.

### 8. Nach der Installation von iOS18 wird beim Anmelden von der Einstellungsseite auf eine leere Seite umgeleitet

Drücken Sie lange auf den schwebenden Ball und klicken Sie auf den Avatar, um sich anzumelden.

### 9. "Datei existiert nicht" beim Ziehen der crx-Datei zu den Browser-Erweiterungen

Sie müssen zuerst die Zip-Datei extrahieren und dann nur die CRX-Datei ziehen.

### 10. Warum installiert der crx-Download Version 1.13.5 anstelle der neuesten

Weil Ihr Chrome-Engine als unter Version 115 erkannt wird, die einige erweiterte Funktionen des Plugins nicht unterstützt, wird es automatisch auf Version 1.13.5 heruntergestuft.

## Grundlegende Übersetzungsbezogene

### 1. Hauptinhalt auf Websites wie Youtube, Facebook wird übersetzt, aber einige Seitenleisten nicht, ich möchte alles übersetzen

Aus Gründen der Lesbarkeit der Seite übersetzt die immersive Übersetzung standardmäßig nur den Hauptinhaltsbereich. Wenn Sie alle Bereiche übersetzen möchten:

Öffnen Sie das schwebende Ball-Panel (lange drücken auf Mobilgeräten) -> Klicken Sie unten rechts auf mehr -> Wählen Sie alle Bereiche.

### 2. Schwebende Blase wird in Apps auf Mobilgeräten nicht angezeigt

- Das Immersive Translate Plugin ist ein Browser-Plugin, das **nur in Browsern** ausgeführt werden kann, es kann nicht in anderen Apps verwendet werden und unterstützt keine Übersetzung innerhalb anderer Apps.

- Das Plugin funktioniert nur in dem Browser, in dem es installiert ist, und **kann nicht über Browser hinweg arbeiten** (z.B. Installation in Safari erlaubt es nicht, es in Chrome zu verwenden)

### 3. Klicken auf YouTube im iOS-Browser öffnet direkt die App

Drücken und halten Sie den YouTube-Link, um ein schwebendes Fenster zu öffnen, und wählen Sie, in einer Webseite zu öffnen.

### 4. Wie man die automatische Übersetzung ausschaltet

- Abbrechen im Popup-Panel oder auf der Einstellungsseite.
- Oder über die Einstellungsseite ändern

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="automatische Übersetzung ausschalten" width="250" />

### 5. Keine Berechtigung, die aktuelle Seite zu übersetzen

- Standard-Browserseite (keine Adresse in der Adressleiste)
- Drittanbieter-Plugin-Seite
- Google-Plugin deaktiviert Google Store-Seite

### 6. Wie zeige ich den Originaltext nicht an?

Tippen Sie auf das Immersive Translate-Symbol, um das Erweiterungspanel zu öffnen, tippen Sie auf [Mehr], [Wechseln zu Nur-Übersetzungsmodus].

### 7. Ausrufezeichen erscheint auf der Seite

Ein Ausrufezeichen auf der Seite zeigt an, dass der Übersetzungsdienst auf ein Problem gestoßen ist und einen Fehler zurückgegeben hat. Sie können die Maus über das Ausrufezeichen bewegen, um den spezifischen Fehler anzuzeigen.

#### Beispiel: 429 Fehler

Dies ist einer der häufigsten Fehler, 429 zeigt an, dass die Anforderungsfrequenz zu schnell ist. Die Übersetzung von Webseiten hat eine sehr große Anzahl von Absätzen zu übersetzen, obwohl wir große Optimierungen vorgenommen haben, einschließlich der Zusammenführung von Absätzen, Frequenzkontrolle usw., gibt es manchmal immer noch einige Übersetzungsdienste, die überlastet sind und einen 429-Frequenzlimit-Fehler zurückgeben. In diesem Fall können Sie normalerweise vorübergehend zu anderen Übersetzungsdiensten wechseln oder eine Weile warten und es erneut versuchen.

Wenn Sie den Google-Dienst verwenden und einen 429-Fehler erleben, ist es im Allgemeinen ein Fall, dass Google eine Verkehrsbeschränkung gegen Ihren Knoten durchführt, und es wird empfohlen, die Knoten zu wechseln.

### 8. Wie wechselt man die Übersetzungsquelle und Zielsprache

Auf Mobilgeräten, lange auf den schwebenden Ball drücken; auf dem Desktop, die Maus zum schwebenden Ball bewegen, um die Einstellungen aufzurufen, anderen Übersetzungsdienst/andere Zielsprache auswählen.

### 9. Google Translate Schnittstelle blockiert Problem

Bitte fügen Sie den Domainnamen `translate.googleapis.com` zur Proxy-Regel hinzu.

### 10. Beeinflusst OpenAIs Verbot von API-Schlüsseln in China die Mitglieds-AI-Dienste

Keine Auswirkungen, das Produkt verwendet Azure Enterprise OpenAI, das nicht den regionalen API-Beschränkungen unterliegt.

### 11. Farbwolken-Übersetzungsfehler

Das Klicken auf die `?` Fehlermeldung zeigt "Unsupported trans_type". Sie können manuell auswählen, um die automatisch erkannte Sprache auf eine bestimmte Sprache einzustellen.

### 12. WeChat Reading kann nicht übersetzt werden

Es kann nicht übersetzt werden, da WeChat Reading spezielle Verarbeitung für den Inhalt vorgenommen hat, um den Zugriff auf den Inhalt durch Dritte zu verhindern.

### 13. Einige Inhalte auf Webseiten werden nicht übersetzt

Im Allgemeinen liegt es daran, dass der Website-Administrator Bereiche definiert hat, die nicht übersetzt werden sollen, indem er `translate="no"` oder `notranslate class` verwendet, aber Sie können dies lösen, indem Sie:

1. Die Maus-Hover-Funktion aktivieren
2. Mit der Maus über den Bereich fahren, um den Absatzinhalt in diesem Bereich zu erzwingen

### 14. Auslösen der Übersetzung hat keine Wirkung

Wenn andere Seiten übersetzt werden können, aber eine bestimmte Seite nicht:

- Wenn diese Seite weniger Besucher hat
  - Es wird empfohlen, Absätze durch Maus-Hover zu übersetzen
  - Wenn Sie die gesamte Seite übersetzen müssen, können Sie sie über [Benutzerregeln](/docs/advanced/#user-rules) anpassen
- Wenn diese Seite von vielen Menschen genutzt wird
  - Sie können mit der Maus-Hover-Übersetzung beginnen
  - Melden Sie es in der Gruppe, und es wird später angepasst

### 15. Wie speichere ich mein Webseiten-Feedback, wenn ich Probleme mit der Webseitenübersetzung habe?

Sie müssen mit der rechten Maustaste auf "Speichern unter" klicken oder die Strg+S-Tastenkombination auf der Webseite verwenden, die Einzeldatei als Speicheroption wählen und im Dateiformat .mht/.mhtml speichern. Senden Sie dann die Datei an support@immersivetranslate.com.

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

### 16. Feedback-Debug-Log

1. Debug-Logging aktivieren: Panel öffnen -> Einstellungen -> Entwicklereinstellungen -> "Debug-Log in Konsole drucken" aktivieren.
2. Konsole der Seite öffnen: Rechtsklick, um die Inspektion zu öffnen -> Zur Konsole oben in der rechten Spalte wechseln -> Die Aktion ausführen, um die Logs zu sehen.

### 17. Wie man den Hoverball ausschaltet

- Auf der aktuellen Seite ausblenden: Auf "Diese Seite nie übersetzen" setzen
- Auf allen Seiten ausblenden: [Einstellungsseite] - [Schnittstelleneinstellungen] öffnen und [Hoverball auf Seite anzeigen] ausschalten

### 18. Maus-Hover + Tastenkombination Übersetzungsfunktion funktioniert nicht

Um die Maus-Hover plus Tastenkombination Übersetzungsfunktion zu aktivieren, muss die Seite zuerst den Fokus haben. Wenn Sie feststellen, dass die Funktion nicht ausgelöst wird, versuchen Sie diese Schritte:

1. Klicken Sie einmal irgendwo auf der Seite, um sicherzustellen, dass die Seite den Fokus hat.
2. Versuchen Sie erneut, die Maus-Hover- und Tastenkombination für die Übersetzung zu verwenden.
3. Wenn die Übersetzungsfunktion immer noch nicht reagiert, überprüfen Sie, ob Ihre Tastenkombinationseinstellungen korrekt sind.

### 19. Wie man die neuesten Regeln aktualisiert

Die Erweiterung selbst wird regelmäßig mit den neuesten Anpassungsregeln der offiziellen Website synchronisiert, wenn Sie sie verwenden. Sie können auch manuell mit den neuesten Regeln synchronisieren, indem Sie auf das Immersive Translate Erweiterungssymbol im Browser klicken, um ein Popup-Fenster zu öffnen, in dem die Erweiterung automatisch die neuesten Anpassungsregeln erkennt und mit ihnen synchronisiert. Dasselbe gilt für Tampermonkey-Skripte.

### 20. Übersetzung schlägt fehl / Übersetzung dreht sich weiter



## Übersetzung von technischen Dokumenten

1. Überprüfen Sie den Grund für das Scheitern:
   - Wenn das Kontingentlimit erreicht ist, bedeutet dies, dass das monatliche Kontingent des Mitglieds für diese Übersetzungsquelle erschöpft ist.
   - Wenn die Übersetzung einen Netzwerkfehler anzeigt, überprüfen Sie zuerst den Status Ihres Knotens/Netzwerks.

2. Wechseln Sie die Übersetzungsquelle: Halten Sie die schwebende Kugel gedrückt, um eine andere Übersetzungsquelle auszuwählen.

### 21. Wie man das Übersetzungskontingent und die Nutzung von Pro-Mitgliedern überprüft

- Pro-Mitglieder genießen ein Basisübersetzungskontingent von 20 Millionen Tokens pro Monat, das für alle Übersetzungsdienste verwendet werden kann. Ob Sie es vollständig für DeepL (entspricht 20 Millionen Zeichen), vollständig für OpenAI (20 Millionen Tokens) oder eine Mischung aus mehreren Diensten verwenden, Sie können das Kontingent frei nach Ihren tatsächlichen Bedürfnissen zuweisen.

  > Die Preisgestaltung von OpenAI basiert auf Tokens. Für englischen Text entspricht 1 Token ungefähr 4 Zeichen oder 0,75 Wörtern. Typischerweise entsprechen 1000 Tokens etwa 750 englischen Wörtern oder 400-500 chinesischen Zeichen.

- Nutzungsanfrageadresse: [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. Warum ist die Google-Übersetzungsqualität des Plugins nicht so gut wie die der Google-Webseitenübersetzung

Weil das Plugin die kostenlose API von Google aufruft, die eine alte API ist, die Google nicht kontinuierlich pflegt, während die offizielle Webseitenübersetzung von Google kontinuierlich gepflegt wird. Theoretisch ist die Qualität nicht so gut wie die offizielle Übersetzung von Google, und kürzlich hat sich die Übersetzungsqualität der kostenlosen API von Google erheblich verschlechtert. Wir empfehlen, auf andere Übersetzungsdienste umzusteigen, und wir suchen aktiv nach alternativen Lösungen. Verwandte Diskussion: [#2574](https://github.com/immersive-translate/immersive-translate/issues/2547)

### 23. Anzeige des Touch-Modus im Mausmodus

In den [Erweiterten Einstellungen](https://dash.immersivetranslate.com/#advanced) den Mausmodus aktivieren. Version 1.14.9 wird diese Moduserkennung optimieren.

## Videoübersetzung

### 1. Youtube-Untertitel-Einrichtungsstil

Sie können auf die eigenen Untertiteleinstellungen von Youtube klicken, [Optionen], und dann können Sie die Größe, Farbe usw. anpassen.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

### 2. YouTube-Bilinguale Untertitel in traditionellem Chinesisch werden nicht angezeigt

YouTube bietet maschinell übersetzte Untertitel, und traditionelles Chinesisch weist Formatierungsfehler auf, die dazu führen, dass alle Untertitel mit einem großen Abschnitt von Untertiteln am Anfang erscheinen. Basierend auf diesem Szenario wird empfohlen, die Option [Immersive Translate zur Übersetzung von Untertiteln verwenden] in [Einstellungen] [Video-Untertitel] zu aktivieren.

### 3. Wie man die Untertitelübersetzung für Bilibili aktiviert

Wenn Sie Bilibili-Video-Untertitel übersetzen, befolgen Sie bitte diese Schritte:

1. Aktivieren Sie zuerst die eingebauten Untertitel von Bilibili, indem Sie auf die Schaltfläche "Untertitel" in der unteren rechten Ecke des Players klicken. Wenn das Video keine Untertitelschaltfläche oder Untertitelinhalt hat, werden keine zweisprachigen Untertitel unterstützt.
2. Klicken Sie auf das "Immersive Translate"-Symbol im Player, um die Funktion für zweisprachige Untertitel zu aktivieren.

Hinweis bei der Verwendung:

1. Stellen Sie sicher, dass die eingebauten Untertitel von Bilibili aktiviert sind.
2. Stellen Sie sicher, dass die Zielsprache von Immersive Translate von der eingebauten Untertitelsprache von Bilibili abweicht, um die Übersetzungsfunktion auszulösen.

### 4. Netflix-Untertitelübersetzung mit originalem Untertitelstil

- Der aktuelle Netflix-Ansatz verwendet progressive Übersetzung mit selbst gehostetem Untertitelstil und unterstützt keine manuellen Untertitel.
- Der alte Ansatz erfordert das Warten, bis alle Untertitel übersetzt sind, bevor sie angezeigt werden, unterstützt jedoch manuelle Untertitel.

Um zum alten Ansatz zurückzukehren, gehen Sie zu [[Entwicklereinstellungen](https://dash.immersivetranslate.com/#developer)], finden Sie [Benutzerregeln bearbeiten] und fügen Sie die folgende Regel hinzu:

```json
[
  {
    "id": "netflix",
    "subtitleRule.add": {
      "attachRule": {
        "appendSelector": ""
      }
    }
  }
]
```

## Dateibezogene Übersetzung

### 1. Übersetzung lokaler Dokumente

- Methode 1: Gehen Sie zur [Immersive Translate Dateibezogene Übersetzungswebsite](https://app.immersivetranslate.com/), oder klicken Sie auf das Immersive Translate-Erweiterungssymbol und klicken Sie auf [Dateiübersetzung], um einzutreten.

- Methode 2: Wenn Sie Chrome-ähnliche Browser verwenden, wie (Chrome, Arc, Edge-Browser), gibt es eine andere Möglichkeit: Öffnen Sie die Browsererweiterungsverwaltungsseite `chrome://extensions`, finden Sie das [Immersive Translate]-Plugin, [Erlauben Sie der Erweiterung, auf lokale Dateien zuzugreifen], und öffnen Sie dann direkt im Browser die lokale HTML- oder lokale PDF-Datei, Sie können direkt mit der rechten Maustaste auf [Übersetzung] klicken.

**Hinweis**: Der Safari-Browser hat strenge Einschränkungen für den Zugriff von Erweiterungen auf lokale Dateien. Safari-Benutzer sollten Methode 1 direkt verwenden - gehen Sie zur [Immersive Translate Dateibezogene Übersetzungswebsite](https://app.immersivetranslate.com/), um lokale Dateien zu übersetzen.

### 2. PDF-Übersetzung ist langsam, wenn viele Seiten vorhanden sind

Es wird empfohlen, das Dokument in mehrere Teile von jeweils weniger als 100 Seiten zu unterteilen, sie separat zu übersetzen und dann nach der Übersetzung zusammenzuführen.

### 3. Doppelte oder überlappende Übersetzungen in PDF

Dies liegt an Erkennungsproblemen der Quelldatei. Derzeit wird empfohlen, manuell auf diesen Abschnitt zu klicken und die zusätzlichen Textfelder zu löschen. Wir werden diese Situation in zukünftigen Updates weiter optimieren.

### 4. Gibt es ein Glossar / spezielle Übersetzung oder Nicht-Übersetzung für bestimmte Begriffe

Version 1.16.1+ unterstützt die Funktion [AI Terminology Library](https://dash.immersivetranslate.com/#terms).

Die AI-Terminologiebibliothek unterstützt standardmäßig keine Google/Microsoft-Maschinenübersetzungsterminologie.

Methode zur erzwungenen Aktivierung:
(ps: Maschinenübersetzung verwendet Platzhalterersetzung, Terminologie kann die Übersetzungsqualität verringern)

Gehen Sie zu [[Entwicklereinstellungen](https://dash.immersivetranslate.com/#developer)] -> [Vollständige Benutzerkonfiguration bearbeiten]

```
{
  ....
  "enableMachineTranslateTerms":true,
  ...
}
```

### 5. Kann keine übersetzten Word-Dateien im Word-Format exportieren

Derzeit gibt es einige technische Probleme beim Export von Word-Dateien. Es wird empfohlen, das vorhandene Format beizubehalten. Wir arbeiten kontinuierlich an der Optimierung.

### 6. Wie man die minimale Schriftgröße in PDFs anpasst

Dies liegt an der Mindestschriftgrößenbeschränkung des Browsers. Passen Sie die Schriftart des Browsers auf die niedrigste Einstellung an. Für Chrome zum Beispiel: klicken Sie auf [Chrome-Schriftgrößeneinstellungen](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)

## Eingabefeldbezogene Übersetzung

### 1. Eingabefeldverbesserung hat keine Wirkung

- Browser, die nicht unterstützt werden: Siehe den Kompatibilitätsabschnitt von [Eingabefeldübersetzung](https://immersivetranslate.com/docs/input/)
- Kann nicht in der URL-Leiste oder auf der Startseite des Browsers übersetzen, unterstützt nur Suchleisten. Sie können es unter https://www.bing.com/ testen.
- Versuchen Sie, die Leertaste schneller zu drücken.

## Zahlungsbezogene Informationen

### 1. Kann ich WeChat Pay verwenden

WeChat-Zahlungen erfordern private Nachrichten an Mitarbeiter in der Gruppe und die Notiz "WeChat-Zahlung". Nachdem die Mitarbeiter den Zahlungs-QR-Code bereitgestellt haben, führen Sie die Zahlung durch und geben die Zahlungsdetails an. Die Mitarbeiter werden den erforderlichen Jahres-/Monatsmitgliedschafts-Einlösungscode bereitstellen, der auf der [Mitgliedseinlösungsseite](https://immersivetranslate.com/exchange/) eingelöst werden kann.

### 2. Kann ich eine Rechnung erhalten

Derzeit können nur Jahresmitgliedschaften Rechnungen erhalten. Benutzer, die bereits bezahlt haben und eine Rechnung benötigen, sollten private Nachrichten an Mitarbeiter in der Gruppe senden und die Notiz "Rechnungsausstellung" hinzufügen. Unbezahlte Benutzer können überprüfen: [Jahresmitgliedschafts-Rechnungsinformationen](https://immersivetranslate.com/bill/)

## Weitere Fragen (ungewöhnlich)

<details>
<summary>Wie lösche ich meinen Cache mit Tampermonkeys?</summary>
<p>
Aufgrund der API-Beschränkung von Tampermonkeys wird der Cache von Immersive Translate Tampermonkeys im Cache der entsprechenden Website gespeichert. Wenn Sie ihn löschen möchten, können Sie das Entwicklerwerkzeug-Panel der entsprechenden Website in Ihrem Browser öffnen und dann den Cache dieser Website löschen.
</p>
</details>

<details>
<summary>Fehlgeschlagene Anfrage der Tampermonkey-Benutzeroberfläche?</summary>
<p>
Tampermonkeys erfordern, dass alle Anfragen aus dem Skript Berechtigungen am Anfang des Skripts deklarieren, z.B.:`@connect api.google.com`, also wenn Sie einen neuen Domainnamen hinzufügen müssen, der nicht der Standard ist, deklarieren Sie ihn bitte am Anfang des Tampermonkey-Skripts nach dem Vorbild des anderen Domainnamens.
</p>
</details>

<details>
<summary>Edge-Browser-Plugin öffnet sich leer und der Browser meldet MANIFEST-000001-Fehler</summary>
<p>
Öffnen Sie die Anwendung [Quick File Finder (Everything)](https://www.voidtools.com/en-us/downloads/), suchen Sie nach `amkbmndfnliijdhojkpoglbnaaahippg` (der Immersive-Erweiterungs-ID) im Browser-Speicherordner, löschen Sie ihn, deinstallieren Sie das Plugin und installieren Sie es erneut.
</p>
</details>

<details>
<summary>Wie kann man zweisprachige Untertitel herunterladen / Können zweisprachige Untertitel von anderen Websites heruntergeladen werden?</summary>
<p>
- Derzeit wird der Untertitel-Download nur auf dem Desktop unterstützt.
- Einschließlich YouTube, wenn es eine Untertitel-Download-Schaltfläche gibt, unterstützt die aktuelle Website den Download von zweisprachigen Untertiteln.
</p>
</details>