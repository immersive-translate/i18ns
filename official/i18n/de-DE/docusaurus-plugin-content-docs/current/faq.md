---
sidebar_position: 9
---

# FAQ

### 1. Android App, schwebende Kugel verschwunden

Alte Versionen von Add-ons sind deaktiviert. Deinstallieren Sie sie und installieren Sie die neueste Version von der [offiziellen Website](https://immersivetranslate.com/).

## Hauptinhalte auf Websites wie Youtube, Facebook werden übersetzt, aber einige Seitenleisten nicht. Ich möchte alles übersetzen

Um die Lesbarkeit der Seite zu gewährleisten, übersetzt die immersive Übersetzung standardmäßig nur den Hauptinhaltsbereich. Wenn Sie alles übersetzen möchten.

Öffnen Sie das schwebende Kugel-Panel (lange drücken auf dem Handy) -> Klicken Sie unten rechts auf mehr -> Wählen Sie alle Bereiche aus

## Schwebende Blase wird in Youtube (oder anderen) Apps auf dem Handy nicht angezeigt

Browser-Plugins können nur in Browsern ausgeführt werden und nicht in anderen Apps verwendet werden.

- Beim Klicken auf YouTube in einem iOS-Browser wird die App direkt geöffnet.

  Halten Sie den YouTube-Link gedrückt, um ein schwebendes Fenster zu öffnen, und wählen Sie, in einer Webseite zu öffnen.

## Wie schalte ich die automatische Übersetzung aus?

- Abbrechen im Popup-Panel oder auf der Einstellungsseite.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="turn off automatic translation" width="250" />

<!-- - Oder ändern: über die Einstellungsseite

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## Keine Berechtigung, die aktuelle Seite zu übersetzen

- Standardseite des Browsers (keine Adresse in der Adressleiste)
- Seite eines Drittanbieter-Plugins
- Google-Plugin deaktiviert Google Store-Seite

## Wie zeige ich den Originaltext nicht an?

Tippen Sie auf das Immersive Translate-Symbol, um das Erweiterungspanel zu öffnen, tippen Sie auf [Mehr], [Nur-Übersetzungsmodus wechseln]

## Ausrufezeichen erscheint auf der Seite

Ein Ausrufezeichen auf der Seite zeigt an, dass der Übersetzungsdienst auf ein Problem gestoßen ist und einen Fehler zurückgegeben hat. Sie können mit der Maus über das Ausrufezeichen fahren, um den spezifischen Fehler anzuzeigen.

### 429 Fehler

Dies ist einer der häufigsten Fehler, 429 zeigt an, dass die Anforderungsfrequenz zu schnell ist. Die Übersetzung von Webseiten hat eine sehr große Anzahl von Absätzen zu übersetzen, obwohl wir eine großartige Optimierung vorgenommen haben, einschließlich der Zusammenführung von Absätzen, Frequenzkontrolle usw., gibt es manchmal immer noch einige Übersetzungsdienste, die überlastet sind und den 429-Frequenzbegrenzungsfehler zurückgeben. In diesem Fall können Sie normalerweise vorübergehend zu anderen Übersetzungsdiensten wechseln oder eine Weile warten und es erneut versuchen.

Wenn Sie einen Google-Dienst verwenden und 429 erleben, handelt es sich in der Regel um eine Verkehrsbeschränkung von Google gegen Ihren Knoten, und es wird empfohlen, die Knoten zu wechseln.

## Übersetzung lokaler Dokumente

Wenn Sie lokale HTML-Dateien, txt-Dateien oder PDF-Dateien übersetzen müssen, können Sie auf das Immersive Translate-Erweiterungssymbol klicken, dann auf [Mehr] klicken, [PDF-Dateien übersetzen] oder [HTML/txt-Dateien übersetzen] auswählen, um lokale Dateien zu übersetzen.

Wenn Sie Chrome-ähnliche Browser verwenden, wie (Chrome, Arc, Edge-Browser), gibt es eine andere Möglichkeit, die Browser-Erweiterungsverwaltungsseite `chrome://extensions` zu öffnen, das [Immersive Translate]-Plugin zu finden, [Erweiterung den Zugriff auf lokale Dateien erlauben] und dann direkt im Browser die lokale HTML- oder lokale PDF-Datei zu öffnen, können Sie direkt mit der rechten Maustaste auf [Übersetzung] klicken.

## Wie aktualisiere ich die Erweiterung?

Im Allgemeinen werden Erweiterungen, die im Browser-Store installiert sind, automatisch vom Browser aktualisiert. In der Regel wird innerhalb eines Tages nach dem Update der Erweiterung automatisch aktualisiert. Wenn Sie sofort auf die neueste Version aktualisieren möchten, können Sie auf der [Erweiterungsverwaltungs]-Seite des Browsers den [Entwicklermodus] öffnen und dann oben auf [Updates] klicken, um sofort auf die neueste Version des Stores zu aktualisieren.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Youtube-Untertitel-Einstellungsstil

Sie können auf die eigenen Untertiteleinstellungen von Youtube klicken, [Optionen], und dann die Größe, Farbe usw. anpassen.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Immersive Translate Tampermonkey unterstützte Browser

Empfohlene Grease Monkey-Erweiterungen für Chrome, Firefox auf dem Desktop:

- [Tamper Monkey](https://www.tampermonkey.net/)

Empfohlene Grease Monkey-Erweiterung für Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Wenn Sie [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) in Safari verwenden, suchen Sie bitte nach dem Immersive Translate Optimization Script, um es direkt aus dem eigenen Store von Stay herunterzuladen (speziell für Stay optimiert) -->

Empfohlene Grease Monkey-Erweiterungen für Android:

1. Sie können die [Tamper Monkey](https://www.tampermonkey.net/) Erweiterung mit [Firefox Latest Version](https://www.mozilla.org/firefox/browsers/mobile/android/) installieren.

<!-- 2. Sie können auch direkt [X Browser](https://www.xbext.com/?ref=immersive-translate) verwenden, nach der Installation direkt die [Immersive Translate Tampermonkey Adresse](https://download.immersivetranslate.com/immersive-translate.user.js) öffnen, um es zu installieren! -->

<!-- Bekannte nicht unterstützte Grease Monkey-Erweiterungen：

- Android Via Browser
- iOS Alook Browser -->

(da solche Browser die erforderliche Grease Monkey API nicht implementieren)

## Google Translate Interface Walled Off Issue

Bitte fügen Sie den Domainnamen `translate.googleapis.com` zur Proxy-Regel hinzu

## Wie aktualisiere ich die neuesten Regeln

Die Erweiterung selbst wird regelmäßig mit den neuesten Anpassungsregeln der offiziellen Website synchronisiert, wenn Sie sie verwenden. Sie können auch manuell mit den neuesten Regeln synchronisieren, indem Sie auf das Immersive Translate-Erweiterungssymbol des Browsers klicken, um ein Popup-Fenster zu öffnen, in dem die Erweiterung automatisch die neuesten Anpassungsregeln erkennt und mit ihnen synchronisiert, das Gleiche gilt für Tampermonkeys.

## Wie speichere ich mein Webseiten-Feedback, wenn ich Probleme mit der Webseitenübersetzung habe?

Sie müssen mit der rechten Maustaste auf "Speichern unter" klicken oder die Tastenkombination Strg+s auf der Webseite verwenden, die Option "Einzelne Datei" für die Speicheroption auswählen und schließlich das Dateiformat .mht/.mhtml verwenden. Senden Sie dann die Datei an support@immersivetranslate.com

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Farbwolken-Übersetzungsfehler

Tippen Sie weg? Die Fehlermeldung für die Nummer "Unsupported trans_type" wird angezeigt. Sie können die Sprache auswählen, die automatisch durch die angegebene Sprache erkannt werden soll.

## WeChat Reading kann nicht übersetzt werden

Es kann nicht übersetzt werden, da WeChat Reading eine spezielle Verarbeitung für den Inhalt vorgenommen hat, um den Zugriff auf den Inhalt durch Dritte zu verhindern.

## Auslösen der Übersetzung hat keine Wirkung

Andere Seiten werden übersetzt, aber eine Seite nicht.

- Wenn diese Seite weniger Besucher hat
  - Vorgeschlagene Absätze durch Bewegen der Maus übersetzen
  - Wenn Sie die gesamte Seite übersetzen müssen, können Sie sie über [Benutzerregeln](/docs/advanced/#user-rules) anpassen
- Wenn diese Seite von vielen Menschen genutzt wird
  - Sie können zunächst durch Bewegen der Maus die Verwendung der Übersetzung starten
  - Rufen Sie es in der Gruppe auf und es wird später angepasst

## Eingabefeldverstärkung hat keine Wirkung

- Browser-Startseite Google-Suche

Das Google-Suchfeld muss sich auf der Webseite der URL [Google](https://www.google.com/) befinden und kann nicht auf der Startseite des Browsers, an leeren Stellen der Adressleiste, verwendet werden

## Feedback-Debug-Log

- Debug-Logging aktivieren
  Panel öffnen -> Einstellungen -> Entwicklereinstellungen -> "Debug-Log in Konsole drucken" aktivieren.
- Konsole der Seite öffnen
  Rechtsklick, um die Überprüfung zu öffnen -> Zur Konsole oben in der rechten Spalte wechseln -> Aktion ausführen, um die Logs zu sehen

## Wie schalte ich die Hoverball aus?

- Auf der aktuellen Seite ausblenden

Stellen Sie es auf "Diese Seite niemals übersetzen".

- Auf allen Seiten ausblenden

Öffnen Sie [Einstellungsseite] - [Schnittstelleneinstellungen] und schalten Sie [Hoverball auf Seite anzeigen] aus.

## Fehler beim Installieren des Plugin-Installers auf Chrome

- ungültiger Wert für web_accessible_resource[0]

  Chromium-Version größer als 88 ist erforderlich, um manifest_version 3 zu unterstützen.

## Wie installiere ich den 360 Browser

Nur 360 Extreme Browser x wird unterstützt, denken Sie daran, dass es mit x ist. Wenn Sie Zugriff auf den Google Extensions Store haben, können Sie direkt dorthin gehen und ihn installieren. Wenn Sie keinen Zugriff haben, [installieren Sie ihn manuell](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## Opera-Browser funktioniert nicht

- Es funktioniert nicht auf google.com und anderen Suchseiten, das Plugin zeigt `Bitte aktualisieren Sie die aktuelle Seite, bevor Sie die Übersetzung starten` an und das Aktualisieren der Seite zeigt weiterhin diese Nachricht an.

Sie müssen "Immersive Translate" in den Opera-Plugin-Einstellungen finden und die Option "Zugriff auf Suchergebnisseiten erlauben" aktivieren.

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## YouTube zweisprachige Untertitel in traditionellem Chinesisch werden nicht angezeigt

YouTube bietet maschinell übersetzte Untertitel, und traditionelles Chinesisch hat Formatierungsfehler, die dazu führen, dass alle Untertitel mit einem großen Abschnitt von Untertiteln am Anfang angezeigt werden. Basierend auf diesem Szenario wird empfohlen, die Option [Immersive Translate zur Übersetzung von Untertiteln verwenden] in [Einstellungen] [Video-Untertitel] zu aktivieren.

## Weitere Fragen (siehe sehr viel)

<details>
<summary>Wie lösche ich meinen Cache mit Tampermonkeys?</summary>
<p>
Aufgrund der API-Beschränkung von Tampermonkeys wird der Cache von Immersive Translate Tampermonkeys im Cache der entsprechenden Website gespeichert. Wenn Sie ihn löschen möchten, können Sie das Entwickler-Tools-Panel der entsprechenden Website in Ihrem Browser öffnen und dann den Cache dieser Website löschen.
</p>
</details>

<details>
<summary>Tampermonkey benutzerdefinierte Schnittstellenadressanforderung fehlgeschlagen?</summary>
<p>
Tampermonkeys erfordern, dass alle Anfragen aus dem Skript Berechtigungen am Anfang des Skripts deklarieren müssen, z.B.:`@connect api.google.com`, also wenn Sie einen neuen Domainnamen hinzufügen müssen, der nicht der Standard ist, deklarieren Sie ihn bitte am Anfang des Tampermonkey nach dem anderen Domainnamen.
</p>
</details>