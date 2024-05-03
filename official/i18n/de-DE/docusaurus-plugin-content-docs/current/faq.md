---
sidebar_position: 9
---

# FAQ

## Download aus dem Apple Store nicht möglich

- 2023.07.28: Apple Store in China aufgrund von Richtlinien herabgestuft
- 2023.08.05: Wurde in China wieder eingeführt

## Automatische Übersetzung ausschalten

- Abbrechen im Popup-Fenster oder auf der Einstellungsseite.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="Automatische Übersetzung ausschalten" width="250" />

<!-- - Oder ändern: über die Einstellungsseite

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## Keine Berechtigung zur Übersetzung der aktuellen Seite

- Browser-Standardseite (keine Adresse in der Adressleiste)
- Seite eines Drittanbieter-Plugins
- Google-Plugin deaktiviert Google Store-Seite

## Wie verhindere ich die Anzeige des Originaltextes?

Tippen Sie auf das Immersive Translate-Symbol, um das Erweiterungsfenster zu öffnen, tippen Sie auf [Mehr], [Wechseln zu Nur-Übersetzung-Modus]

## Ausrufezeichen erscheint auf der Seite

Ein Ausrufezeichen auf der Seite zeigt an, dass der Übersetzungsdienst auf ein Problem gestoßen ist und einen Fehler zurückgegeben hat. Sie können den Mauszeiger über das Ausrufezeichen bewegen, um den spezifischen Fehler anzuzeigen.

### 429 Fehler

Dies ist einer der häufigsten Fehler, 429 zeigt an, dass die Anfragefrequenz zu hoch ist. Die Übersetzung von Webseiten hat eine sehr große Anzahl von Absätzen zu übersetzen, obwohl wir eine große Optimierung vorgenommen haben, einschließlich der Zusammenführung von Absätzen, Frequenzkontrolle usw., aber manchmal sind dennoch einige Übersetzungsdienste überlastet und geben den Fehler der Frequenzbegrenzung 429 zurück. In diesem Fall können Sie normalerweise vorübergehend zu anderen Übersetzungsdiensten wechseln oder eine Weile warten und es erneut versuchen.

Wenn Sie einen Google-Dienst nutzen und den Fehler 429 erhalten, handelt es sich in der Regel um eine Verkehrsbeschränkung von Google gegenüber Ihrem Knoten, und es wird empfohlen, den Knoten zu wechseln.

## Übersetzung lokaler Dokumente

Wenn Sie lokale HTML-Dateien, txt-Dateien oder PDF-Dateien übersetzen müssen, können Sie auf das Symbol der Immersive Translate-Erweiterung klicken, dann auf [Mehr] klicken, auf [PDF-Dateien übersetzen] oder [HTML-/txt-Dateien übersetzen] klicken, um lokale Dateien zu übersetzen.

Wenn Sie Chrome-ähnliche Browser verwenden, wie (Chrome, Arc, Edge-Browser), gibt es einen weiteren Weg, nämlich die Erweiterungsverwaltungsseite des Browsers `chrome://extensions` zu öffnen, das [Immersive Translate]-Plug-in zu finden, [Der Erweiterung erlauben, auf lokale Dateien zuzugreifen], und dann direkt im Browser die lokale HTML- oder lokale PDF-Datei zu öffnen, können Sie direkt per Rechtsklick [übersetzen].

## Wie aktualisiere ich die Erweiterung?

Allgemein gesprochen werden Erweiterungen, die im Browser-Store installiert sind, automatisch aktualisiert, normalerweise wird die Erweiterung innerhalb eines Tages nach dem Update automatisch aktualisiert. Wenn Sie sofort auf die neueste Version aktualisieren möchten, können Sie auf der Seite [Erweiterungsverwaltung] des Browsers den [Entwicklermodus] öffnen und dann oben auf [Updates] klicken, um sofort auf die neueste Version im Store zu aktualisieren.

![](/assets/docs/doc-assets/update-extension.png)

## Youtube-Untertiteleinstellungen

Du kannst auf die eigenen Untertiteleinstellungen von Youtube klicken, [Optionen], und dann kannst du die Größe, Farbe und so weiter anpassen.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Von Immersive Translate unterstützte Tampermonkey-Browser

Empfohlene Grease Monkey-Erweiterungen für Chrome, Firefox auf dem Desktop:

- [Tamper Monkey](https://www.tampermonkey.net/)

Für Safari empfohlene Grease Monkey-Erweiterung:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Wenn du [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) in Safari verwendest, suche bitte nach dem Immersive Translate Optimization Script, um es direkt aus dem eigenen Store von Stay herunterzuladen (speziell für Stay optimiert) -->

Für Android empfohlene Grease Monkey-Erweiterungen:

1. Du kannst die Erweiterung [Tamper Monkey](https://www.tampermonkey.net/) mit der [neuesten Version von Firefox](https://www.mozilla.org/firefox/browsers/mobile/android/) installieren.

<!-- 2. Du kannst auch direkt [X Browser](https://www.xbext.com/?ref=immersive-translate) verwenden, nach der Installation, öffne direkt [Immersive Translate Tampermonkey Adresse](https://download.immersivetranslate.com/immersive-translate.user.js), um es zu installieren! -->

<!-- Bekannte nicht unterstützte Grease Monkey-Erweiterungen:

- Android Via Browser
- iOS Alook Browser -->

(da solche Browser die erforderliche Grease Monkey API nicht implementieren)

## Problem mit abgeschotteter Google Translate-Schnittstelle

Bitte füge den Domainnamen `translate.googleapis.com` zur Proxy-Regel hinzu

## So aktualisieren Sie die neuesten Regeln

Die Erweiterung selbst wird regelmäßig mit den neuesten offiziellen Website-Anpassungsregeln synchronisiert, wenn Sie sie verwenden. Sie können auch manuell mit den neuesten Regeln synchronisieren, indem Sie auf das Symbol der Immersive Translate-Erweiterung im Browser klicken, um ein Popup-Fenster zu öffnen. Dort wird die Erweiterung automatisch die neuesten Anpassungsregeln erkennen und mit ihnen synchronisieren. Das Gleiche gilt für Tampermonkeys.

## Wie speichere ich mein Webseiten-Feedback, wenn ich Probleme mit der Webseitenübersetzung habe?

Sie müssen mit der rechten Maustaste auf "Speichern unter" klicken oder die Tastenkombination Strg+S im Web verwenden, als Speicheroption eine einzelne Datei wählen und schließlich ist das Dateiformat .mht/.mhtml. Senden Sie dann die Datei an support@immersivetranslate.com

<!-- ![save mht](/assets/save_mht.png) -->

## Fehler bei der Farbwolkenübersetzung

Wegtippen? Die Fehlermeldung für die Nummer "Unsupported trans_type" wird angezeigt. Sie können die Sprache so auswählen, dass sie durch die angegebene Sprache automatisch erkannt wird.

## WeChat-Lesen kann nicht übersetzt werden

Es kann nicht übersetzt werden, weil WeChat-Lesen eine spezielle Verarbeitung für den Inhalt durchgeführt hat, um den Zugriff auf den Inhalt durch Drittmittel zu verhindern.

## Auslösen der Übersetzung hat keine Wirkung

Andere Seiten übersetzen, aber eine Seite nicht.

- Wenn diese Seite weniger Besucher hat
  - Vorgeschlagene Absätze zum Übersetzen durch Überfahren mit der Maus
  - Wenn Sie die gesamte Seite übersetzen müssen, können Sie sie über [Benutzerregeln](/docs/advanced/#user-rules) anpassen
- Wenn diese Seite von vielen Menschen genutzt wird
  - Sie können beginnen, indem Sie mit der Maus darüberfahren, um die Nutzung zu übersetzen
  - Rufen Sie es in der Gruppe auf, und es wird später angepasst

## Verstärkung des Eingabefelds hat keine Wirkung

- Browser-Startseite Google-Suche

Das Google-Suchfeld muss sich auf der [Google](https://www.google.com/) URL der Webseite befinden und kann nicht auf der Browser-Startseite, den Adressleistenleerstellen verwendet werden

## Feedback-Debugprotokoll

- Debugprotokollierung aktivieren
  Öffnen Sie das Panel -> Einstellungen -> Entwicklereinstellungen -> Aktivieren Sie "Debugprotokoll in der Konsole ausgeben".
- Die Konsole der Website öffnen
  Klicken Sie mit der rechten Maustaste, um die Überprüfung zu öffnen -> Wechseln Sie in der rechten Spalte oben zur Konsole -> Führen Sie die Aktion aus, um die Protokolle zu sehen

## Wie man Hoverball ausschaltet

- Auf der aktuellen Seite verbergen

Stellen Sie es auf "Diese Seite nie übersetzen".

- Auf allen Seiten verbergen

Öffnen Sie [Einstellungsseite] - [Schnittstelleneinstellungen] und schalten Sie [Hoverball auf Seite anzeigen] aus.

## Fehler bei der Installation des Plugin-Installers auf Chrome

- ungültiger Wert für web_accessible_resource[0]

  Eine Chromium-Version größer als 88 wird benötigt, um manifest_version 3 zu unterstützen.

## Wie man den 360 Browser installiert

Nur der 360 Extreme Browser x wird unterstützt, denken Sie daran, es ist mit x. Wenn Sie Zugang zum Google Extensions Store haben, können Sie direkt dorthin gehen und ihn installieren. Wenn Sie keinen Zugang haben, [installieren Sie ihn manuell](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## Opera-Browser funktioniert nicht

- Er funktioniert nicht auf google.com und anderen Suchseiten, das Plugin zeigt `Bitte aktualisieren Sie die aktuelle Seite, bevor Sie mit der Übersetzung beginnen` an und das Aktualisieren der Seite fordert weiterhin diese Nachricht an.

Sie müssen "Immersive Translate" in den Opera-Plugin-Einstellungen finden und die Option "Zugriff auf Suchseitenergebnisse erlauben" aktivieren.

<!-- ![](/assets/opera-allow-search.png) -->

## YouTube zweisprachige Untertitel in traditionellem Chinesisch werden nicht angezeigt

YouTube bietet maschinenübersetzte Untertitel, und traditionelles Chinesisch wird Formatierungsfehler haben, was dazu führt, dass alle Untertitel zu Beginn mit einem großen Abschnitt von Untertiteln aufpoppen, basierend auf diesem Szenario wird empfohlen, die Option [Immersive Translate zur Übersetzung von Untertiteln verwenden] in [Einstellungen] [Video-Untertitel] zu aktivieren.

## Mehr Fragen (siehe sehr viel)

<details>
<summary>Wie kann ich meinen Cache bei Tampermonkey löschen?</summary>
<p>
Aufgrund der API-Beschränkung von Tampermonkey wird der Cache von Immersive Translate Tampermonkey im Cache der entsprechenden Website gespeichert. Wenn Sie ihn also löschen möchten, können Sie das Entwicklertools-Panel der entsprechenden Website in Ihrem Browser öffnen und dann den Cache dieser Website löschen.
</p>
</details>

<details>
<summary>Tampermonkey benutzerdefinierte Schnittstellenadressanfrage fehlgeschlagen?</summary>
<p>
Tampermonkey erfordert, dass alle Anfragen aus dem Skript zu Beginn des Skripts Berechtigungen deklarieren müssen, z.B.: `@connect api.google.com`, also wenn Sie einen neuen Domainnamen hinzufügen müssen, der nicht der Standard ist, bitte deklarieren Sie ihn am Anfang des Tampermonkey-Skripts nach dem Vorbild des anderen Domainnamens.
</p>
</details>