---
sidebar_position: 6
---

# Änderungsprotokoll

Dieses Änderungsprotokoll wird entsprechend dem Entwicklungsfortschritt aktualisiert. Das Datum nach der Version ist das Datum der Codezusammenführung, nicht das Veröffentlichungsdatum in den App-Stores (die Überprüfungszeit variiert nach Einreichung in jedem App-Store, wobei einige bis zu einer Woche für die Überprüfung benötigen). Derzeit arbeiten wir an zwei Versionen.

Die **Release-Version** ist die offizielle stabile Version, verfügbar in den gängigen App-Stores wie
[Chrome](https://chromewebstore.google.com/detail/bpoadfkcbjbfhfodiogcnhhhpibjhbnh),
[Edge](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg),
[Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate/),
[Apple](https://apps.apple.com/app/id6447957425) usw.

Die **Preview-Version** wird häufiger veröffentlicht und enthält einige experimentelle Funktionen. Im Vergleich zur Release-Version kann sie mehr Fehler enthalten. Sie wird hauptsächlich veröffentlicht auf

- [Benutzerskript der offiziellen Website](https://download.immersivetranslate.com/immersive-translate.user.js)
- [Beta-Version im Firefox-Store](https://addons.mozilla.org/firefox/addon/immersive-translate-beta/)
- [Github Release Assets](https://github.com/immersive-translate/immersive-translate/releases)

## 1.29.4 Release (2026-05-14)

- Behoben: Ein Problem behoben, durch das für einige Videos auf Twitter keine KI-Untertitel generiert werden konnten.
- Behoben: Ein Problem behoben, durch das [Textauswahl-Übersetzung] auf Reddit nicht funktionierte.
- Behoben: Ein Problem behoben, durch das die Seitenleiste in Atlas Browser nicht geöffnet werden konnte.

## 1.29.1 Release (2026-05-07)

- Hinzugefügt: Unterstützung für den Übersetzungsdienst plamo.
- Verbessert: Layout-Markierungen für RTL-Sprachen im Nur-Übersetzung-Modus verbessert.
- Verbessert: Die Erkennung einiger Pluralformen englischer Begriffe verbessert, um verpasste Terminologie-Treffer zu reduzieren.
- Behoben: Ein Problem mit zitternden Untertiteln bei der Teams-Untertitelübersetzung behoben.
- Behoben: Ein Problem behoben, durch das [Textauswahl-Übersetzung] in ShadowRoot-Szenarien Text nicht korrekt erfassen konnte.

## 1.28.5 Release (2026-04-24)

- Fixed: Fixed an issue where direct translation content disappeared when hovering with the mouse.
- Fixed: Fixed an issue where Twitter subtitle downloads could fail.
- Added: Added Document Translation and Text Translation entries to the new panel.
- Fixed: Fixed a compatibility issue where document translation caching could fail in some browsers.
- Fixed: Fixed missing translations in complex text structures when using Translation Only mode.

## 1.28.3 Release (2026-04-10)

- Improved: Optimized the panel UI and interaction experience.
- Improved: Optimized the settings page structure and configuration experience.
- Added: Added support for Baidu Netdisk video subtitles.
- Improved: Improved long webpage translation performance for faster loading and rendering.
- Improved: Added adaptive translation support for collapsed content on list pages.
- Improved: Improved loading speed in multi-iframe scenarios.
- Fixed: Fixed Cloudflare human verification failures in Safari.
- Fixed: Fixed premature timeouts when iframe content translation was slow.
- Fixed: Fixed an issue where the "Remember this choice" option did not take effect in the long text dialog.
- Fixed: Fixed an issue where Input Translation did not work properly when pressing `Option + letter` in Firefox and Safari.
- Fixed: Fixed an issue where some iframe pages could not be translated in Firefox.

## 1.27.2 Release (2026-03-27)

- Improved: Enhanced performance and stability of the free AI translation service.
- Improved: Boosted AI contextual understanding in Korean and Japanese translation scenarios, resulting in higher translation quality.
- Improved: Improved the accuracy and stability of automatic language detection in input fields on non-Chrome browsers.
- Added: Google Translate now supports the Tamazight language.
- Fixed: Resolved an issue where subtitles were not translated when YouTube videos were played in full-screen mode on iOS.

## 1.26.6 Release (2026-03-02)

- Added: Support for subtitle translation in YouTube live streams.
- Fixed: [Input field translation] Fixed an issue where language-code prefixes were translated by mistake (e.g. `hi hello` was translated to `नमस्ते`).
- Fixed: Resolved an issue where extension status was not synced after upgrading membership in the Android Immersive Translate app.

## 1.26.4 Release (2026-02-11)

- Improved: [Input translation] Reduced unintentional triggers for a better typing experience.
- Improved: DeepL translation service now supports more languages.
- Improved: Icon compatibility on older versions of macOS.
- Improved: RTL language layout optimization.
- Fixed: [Translation only] Font style settings were not effective.

## 1.25.3 Release (2026-01-26)

- Improved: Compatibility with the Steam client.
- Added: Support for Tencent Hunyuan model HY-2.0-Instruct.

## 1.24.6 Release (2025-12-31)

- Fixed: In certain environments, the sidebar could not be triggered; improved interaction stability.
- Fixed: DingTalk, WeChat, and other third-party platform accounts were unable to log in due to iframe communication interference.
- Improved: [AI Writing] Added minimal mode.

## 1.23.10 Release (2025-12-05)

- Improved: Enhanced accuracy of information recognition in AIFW privacy mode.
- Improved: Added babel-lite translation service.

## 1.23.7 Release (2025-11-19)

- Improved: Enhanced error messages when subtitle translation fails, improving user experience.

## 1.23.5 Release (2025-11-14)

- Improved: [Input field translation] — Added an option to automatically detect the target language, enhancing the translation experience.
- Improved: Supported translation of dropdown menu content, expanding applicable scenarios.

## 1.22.7 Release (2025-10-30)

- Improved: Translation error messages are now more accurate and user-friendly.
- Improved: After logging in, the extension automatically refreshes the login status of the current webpage, eliminating the need to manually refresh the page.
- Improved: Enhanced accuracy in segmenting long paragraphs.
- Improved: More precise detection of the page language.

## 1.22.4 Release (2025-10-17)

- Fixed: Some bugs in the iOS extension.

## 1.14.16 Release (2025-02-21)

- Hinzugefügt: Deepseek, Gemini, Claude unterstützen Kontextwechsel.
- Behoben: Aktualisierte Begriffe senden keine neue Übersetzungsanfrage.
- Verbessert: Schnittstellensprache fügt Ungarisch hinzu.
- Verbessert: Google-Übersetzungsqualität.
- Verbessert: Kostenlose Bildformatierung.

## 1.14.12 Release (2025-02-19)

- Verbessert: Übersetzungspause leert sofort die Anforderungswarteschlange.
- Verbessert: Filtert schmutzigen Text im deepl Übersetzungsdienst.
- Behoben: Ungültige Seitenleistenübersetzung in den erweiterten Einstellungen.
- Behoben: Anzeigeproblem bei benutzerdefinierter deepseek Übersetzung.

## 1.14.11 Release (2025-02-18)

- Behoben: DeepSeek benutzerdefinierter API-Schlüssel `401: Authentication Fails` Fehler.

## 1.14.10 Release (2025-02-17)

- Neu: Pro-Mitgliedschaft unterstützt DeepSeek (v3) Übersetzungsdienst.
- Behoben: Problem mit der Überschreitung der Größenbeschränkung der Benutzerkonfigurationsdatei gelöst.
- Verbessert: Rechtsklick-Menüeintrag kann geschlossen werden (in den erweiterten Einstellungen bedienbar).
- Verbessert: Verbesserte Spracherkennungsfähigkeiten für Greasemonkey und Safari auf Seiten mit kleineren Sprachen.
- Verbessert: Zugriff auf die Testdienstschnittstelle der Online-Einstellungsseite.
- Verbessert: Verbesserte Benutzererfahrung der Kontextvergleichsvorschau-Funktion.
- Verbessert: Logik zur Beurteilung von Touch- und Mausmodus.

## 1.14.8 Release (2025-02-10)

- Behoben: Problem, bei dem PDF-Pro lange Dateien nicht automatisch übersetzt wurden.
- Verbessert: Microsoft, Google und Tencent unterstützen jetzt Kantonesisch.
- Verbessert: BBC unterstützt jetzt Untertitel.

## 1.14.6 Preview (2025-02-08)

- Behoben: Problem, bei dem **Mouse Hover Translation** keinen Rich-Text übersetzen konnte.
- Verbessert: Tampermonkey-Version unterstützt jetzt YouTube-Untertitelübersetzung.

## 1.14.4 Release (2025-02-07)

- Behoben: Problem mit falscher Spracherkennung im **Enhanced Input Box**.
- Behoben: Intelligentes Zuordnungsproblem von KI-Experten in benutzerdefinierten Übersetzungsdiensten.
- Behoben: Google Drive Synchronisationsfehler in einigen Browsern.
- Behoben: Übersetzungsproblem von YouTube-Live-Kommentaren.
- Behoben: Überlappungsproblem von Untertiteln in einigen YouTube-Videos.
- Verbessert: Fehler bei der Manga-Übersetzung auf Seiten wie shonenjumpplus im Safari-Browser.

## 1.13.8 Release (2025-01-24)

- Neu: Kostenlose Bildübersetzung ist jetzt verfügbar (derzeit nur auf PC-Versionen der Chrome- und Edge-Browser unterstützt), zugänglich über das Rechtsklick-Menü.
- Behoben: Ein Problem behoben, bei dem während der Mehrsegmentübersetzung in Gemini einige Inhalte übersehen wurden.
- Optimiert: Verbesserte das Laden von YouTube-Untertiteln.
- Neu: KI-Übersetzungsdienst unterstützt jetzt Norwegisch.

## 1.13.6 Preview (2025-01-17)

- Verbessert: **AI Expert** kann mit **AI Context-Aware Translation** verwendet werden.
- Verbessert: **Bildübersetzung** ist jetzt kompatibel mit weibo.com (nur auf Chrome und Edge unterstützt).
- Verbessert: Wenn die Schnittstellensprache auf Englisch eingestellt ist, wird die Standardsprache für **Enhanced Input Box** auf Chinesisch geändert.
- Verbessert: Ein Store-Bewertungseintrag wurde in den **Mehr** Optionen im Panel hinzugefügt.

## 1.13.5 Release (2025-01-14)

- Verbessert: Kompatibel mit dem Gemini 2.0 Denkmodell.
- Verbessert: Unterstützt Fettschriftstil im Nur-Übersetzungsmodus.

## 1.13.4 Preview (2025-01-13)

- Hinzugefügt: Pro-Mitglieder können jetzt direkt das **zhipu 4.5** Modell verwenden.
- Verbessert: Gemini-Übersetzung.

## 1.13.1 (2025-01-10)

- Hinzugefügt: Wenn der übersetzte Text und der Originaltext demselben Schriftsystem angehören, wird die Übersetzung in einem spezialisierten Stil angezeigt.
- Behoben: Das Problem, bei dem **Mouse Hover Translation** auf einigen Websites nicht funktioniert.
- Verbessert: DeepLx unterstützt jetzt Arabisch.
- Verbessert: Verbesserte Erkennung der Originalsprache. Früher wurden Seiten mit mehreren Sprachen möglicherweise nicht übersetzt, jetzt werden sie korrekt übersetzt.
- Verbessert: Für Twitter sind mehrzeilige Inhaltsübersetzungen standardmäßig so eingestellt, dass sie nicht umbrochen werden. Ein Umbruch erfolgt nur, wenn der Inhalt 10 Zeilen oder 1000 Zeichen überschreitet. Der Umbruch kann über die Einstellungen **Erweiterte Einstellungen** -> **Automatisches Zeilenumbruch für lange Absätze aktivieren** aktiviert werden.

## 1.12.8 (2025-01-03)

- Behoben: Das Problem, bei dem die iOS 18.3 Einstellungsseite nicht richtig angezeigt werden kann.
- Behoben: Das Fehlen von Leerzeilen bei der Übersetzung von Tweets.
- Behoben: Das Problem, dass Dezimalzahlen beim Übersetzen langer Texte zwangsweise umgebrochen werden.

## 1.12.7 Release (2024-12-30)

- Verbessert: Bing/Google unterstützen jetzt Portugiesisch (Brasilien).
- Verbessert: Verbesserte Beschreibungen für die Benutzeroberflächensprache Traditionelles Chinesisch.
- Verbessert: Layoutanpassung für von rechts nach links geschriebene Sprachen in Panels und Einstellungsseiten.

## 1.12.6 (2024-12-26)

- Behoben: Problem, bei dem die Maus-Hover-Funktion unter bestimmten Bedingungen den falschen Übersetzungsdienst lädt.
- Behoben: Problem, bei dem das vorübergehende Aktivieren von zweisprachigen Untertiteln auf YouTube nicht funktioniert.
- Behoben: Nach dem Wechseln der Übersetzungsdienste wird der Übersetzungsdienst in der "**Enhanced Input Box**" nicht aktualisiert.
- Behoben: Der "**YouTube Enable Bilingual**" Schalter auf der Einstellungsseite funktioniert nicht.
- Verbessert: Das veraltete gemini-1.0-pro Modell wurde entfernt.

## 1.12.4 (2024-12-13)

- Hinzugefügt: **AI Context-Aware Translation** kann die Genauigkeit der Übersetzung von Fachinhalten verbessern. (Nur für Pro-Mitglieder verfügbar, ausschließlich von OpenAI-Modellen unterstützt) **Optionen** -> **Allgemein** -> **AI Context-Aware Translation aktivieren**
- Behoben: Einige Fehler im mehrzeiligen Übersetzungseffekt auf Twitter.
- Behoben: Probleme mit der Übersetzung bestimmter Formeln aufgrund von Rich-Text.
- Verbessert: Beim Übersetzen auf **x.com** werden Videos mit Untertiteln automatisch zweisprachige Untertitel übersetzt.
- Verbessert: Videos ohne Untertitel zeigen ein Übersetzungssymbol an und geben einen Grund an, warum eine Übersetzung nicht möglich ist.

## 1.11.7 (2024-11-25)

- Hinzugefügt: Bing/Google unterstützen jetzt Khmer (Kambodschanisch).
- Hinzugefügt: Unvollständige ePub-Dateien können nach dem erneuten Importieren dort weiter übersetzt werden, wo sie aufgehört haben.
- Behoben: Problem mit der Übersetzung von Twitter-Bildern im Safari-Browser.
- Behoben: Tastenkombinationen werden unwirksam, wenn die "**Hover Translation**" Funktion ein- oder ausgeschaltet wird.
- Verbessert: Verbesserte Anzeige der mehrzeiligen zweisprachigen Übersetzung auf Twitter und YouTube.
- Verbessert: Rich-Text-Übersetzung ist im zweisprachigen Modus standardmäßig deaktiviert, um die Übersetzungsqualität zu verbessern.
- ~~Verbessert: Die Option zum Anpassen der "**Enable Sidebar & Navbar Translation**" in "**Advanced Settings**" hinzugefügt.~~
- Verbessert: Bilder werden im Modus "**Hover - sofort diesen Absatz übersetzen**" nicht mehr übersetzt.

## 1.11.4 (2024-11-16)

- Behoben: Problem mit der Formelübersetzung, verursacht durch die "Twitter Translation Improvement" in Version 1.11.2.

## 1.11.2 (2024-11-13)

- Behoben: Problem, bei dem Inhalte verschwinden, nachdem man im Nur-Übersetzungsmodus von Facebook auf "mehr sehen" klickt.
- ~~Verbessert: Verbesserte Anzeige der mehrzeiligen zweisprachigen Übersetzungen auf Twitter.~~
- Verbessert: Aktualisierte Benutzeroberfläche der Dropdown-Liste des Übersetzungsdienstes im Panel.

## 1.11.1 (2024-11-05)

- Hinzugefügt: Echtzeit-Meeting **Untertitelübersetzung** unterstützt jetzt die Aktivierung über "Schwebeball", verfügbar auf Zoom, Google Meet und Microsoft Teams.
- Behoben: Synchronisierte Untertitel-Timing-Probleme auf YouTube nach dem Ansehen von Werbung.
- Behoben: Anzeigeprobleme mit dem Rechtsklick-Übersetzungsmenü in Safari auf MacOS 15.
- Behoben: Probleme mit der Rückgängig-Funktionalität von Strg+Z im **Enhanced input** auf bestimmten Websites.

## 1.10.6 (2024-10-25)

- Behoben: Problem mit **Enhanced input** Tastenkombinationen, die nicht ausgelöst werden
- Verbessert: Reduzierung der Installationspaketgröße
- Verbessert: Netflix Untertitelanzeigelösung

## 1.10.5 (2024-10-23)

- Hinzugefügt: Warnung anzeigen, wenn die Quellsprache und die Zielsprache gleich sind
- Behoben: Rich-Text-Leerzeichen-Übersetzungsproblem [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- Verbessert: Eingabeverbesserung und Maus-Hover-Funktionalität innerhalb eingebetteter iframes auf Webseiten

## 1.10.2 (2024-10-11)

- Hinzugefügt: Bildübersetzung (Beta-Version)
- Hinzugefügt: Modus "Mausunterstützung erzwingen" aktivieren (Aktivieren Sie diese Funktion nur, wenn die Maus-Hover-Funktion auf Tablet-Geräten nicht verfügbar ist) **Einstellungen** -> **Erweiterte Einstellungen** -> **Mausunterstützung erzwingen**
- Hinzugefügt: Fehlermeldung anzeigen, wenn die Video-Untertitelübersetzung fehlschlägt
- Behoben: Rich-Text-Übersetzungsproblem [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163)
- Verbessert: Probleme behoben, bei denen die Übersetzungsschaltfläche bei der PDF-Übersetzung möglicherweise nicht funktioniert
- Verbessert: Verbesserte Darstellung von übersetzten Formeln
- Verbessert: Sprachauswahlliste

## 1.9.8 (2024-09-28)

- Hinzugefügt: Übersetzungsdienst "Zhipu BigModel"
- Entfernt: "SiliconCloud" Modell qwen1.5-7B-chat (aufgrund offizieller Einstellung)
- Behoben: Kompatibilitätsproblem mit dem Safari-Plugin auf macOS 15 beim Anmelden gelöst

## 1.9.7 (2024-09-20)

- Verbesserte Eingabeunterstützung für Baidu, Gmail und andere Eingabefelder
- Unterstützung für den anthropic-dangerous-direct-browser-access Anforderungsheader für die Claude Anthropic API
- Unterstützung für das Herunterladen von Untertiteln von Hulu-, Bloomberg- und Domestika-Videos
- DeepX unterstützt die Übersetzung von Rich Text
- Behebung des Problems mit der Synchronisation benutzerdefinierter KI-Experten

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) unterstützt das Kopieren von Formeln (Rechtsklick auf die Formel, um das Kopiermenü zu sehen)
- Behebung des Problems mit der Anzeige von zweisprachigen Untertiteln für mehrere Videos auf derselben Twitter-Seite
- Einige Fehler behoben

## 1.9.3 (2024-09-05)

- Die Option für den zweisprachigen Vergleich/Übersetzungsanzeige wurde in die allgemeinen Einstellungen verschoben.
- Standardmäßig merkt sich das System den Modus, der durch Klicken auf das Symbol im Panel für den zweisprachigen Vergleich oder die Übersetzungsanzeige umgeschaltet wird. Um vorübergehend zu wechseln, klicken Sie im Panel auf "Mehr" -> "Wechseln zur Übersetzungsanzeige".
- Standardmäßig wird beim Übersetzen von Vereinfachtem Chinesisch ins Traditionelle Chinesisch und umgekehrt der Übersetzungsmodus anstelle des zweisprachigen Vergleichsmodus verwendet.
- Einige Fehler behoben.

## 1.9.1 (2024-09-03)

- Unterstützung für die Konfiguration von Ausnahmen für Sprachen und Websites im zweisprachigen Kontrast- oder Übersetzungsmodus (Konfiguration auf der Einstellungsseite -> Erweiterte Einstellungen). Zum Beispiel: Wenn Ihr Standardübersetzungsmodus der zweisprachige Kontrast ist, Sie aber nicht möchten, dass Traditionelles Chinesisch ebenfalls den zweisprachigen Kontrast verwendet, können Sie Traditionelles Chinesisch zu den Ausnahmesprachen für den zweisprachigen Kontrast hinzufügen, sodass Traditionelles Chinesisch den Übersetzungsmodus verwendet. Ebenso, wenn Ihr Standardübersetzungsmodus der Übersetzungsmodus ist, Sie aber möchten, dass eine bestimmte Sprache oder Website den zweisprachigen Kontrastmodus verwendet, können Sie diese Sprache oder Website ebenfalls zu den Ausnahmesprachen hinzufügen.
- Behebung eines Problems, bei dem das Eingabefeld in der Tiktok-Privatnachrichtenschnittstelle falsch übersetzt wurde
- Behebung eines Problems, bei dem Comics auf Read Comic Online nicht übersetzt werden konnten
- Behebung eines Problems, bei dem die [Erweiterten Einstellungen -> Mindestanzahl von Zeichen, die für die Übersetzung eines Absatzes erforderlich sind] in einigen Fällen nicht wirksam waren

## 1.8.4 (2024-08-30)

- Der DeepL-Übersetzungsdienst unterstützt jetzt offiziell Traditionelles Chinesisch als Zielsprache (zuvor war das Übersetzen ins Traditionelle Chinesisch mit DeepL mit einem zusätzlichen Drittanbieterprozess zur Umwandlung von Vereinfachtem in Traditionelles Chinesisch verbunden).
- Optimierung der Leistung der Rich Text-Übersetzung.

## 1.8.3

- Google Meet unterstützt jetzt zweisprachige Untertitel für Live-Meetings: Jetzt können Sie die Funktion für zweisprachige Untertitel in Google Meet-Meetings genießen. Öffnen Sie einfach den Meeting-Link, aktivieren Sie die zweisprachigen Untertitel im immersiven Übersetzungspanel und aktualisieren Sie dann die Seite, um es zu erleben.
- Hinzufügen der Option "Übersetzungsprobleme der aktuellen Webseite melden" und der Option "Schwebeball schnell ein-/ausschalten" in den weiteren Optionen des Panels.
- Nach dem Anpassen der Position der zweisprachigen YouTube-Untertitel merkt sich das System automatisch die neue Position.
- Optimierung der Cache-Logik des Plugins, jetzt wird der Cache automatisch gelöscht, der älter als 30 Tage ist.
- Optimierung von Codeblöcken innerhalb von Absätzen für eine genauere Wiederherstellung des Originaltextes.
- Verbesserung der Handhabung von "nicht übersetzbaren Wörtern" in den erweiterten Einstellungen.

## 1.8.2

- Sie können jetzt Text in Eingabefeldern mit einem Rechtsklick übersetzen: Wählen Sie einen beliebigen Text in einem Eingabefeld auf einer Webseite aus, klicken Sie mit der rechten Maustaste, um die Übersetzung auszuwählen, und die immersive Übersetzung wird den ausgewählten Text automatisch in die Zielsprache des Eingabefelds übersetzen, was es bequem macht, schnell Text in Eingabefeldern in andere Sprachen zu übersetzen.
- Sie können jetzt schnell Übersetzungsprobleme von Webseiten im schwebenden Ball der immersiven Übersetzung melden. Nach der Übersetzung einer Webseite, wenn es Probleme gibt, können Sie auf die [Feedback]-Schaltfläche auf der rechten Seite des schwebenden Balls klicken, die Problembeschreibung ausfüllen, und wir werden es so schnell wie möglich bearbeiten.
- Epub-Dateien unterstützen jetzt die Übersetzung von Rich Text (d.h. die Beibehaltung des Formats des Originaltextes jedes Absatzes, wie Links, Fett, etc.)
- Unterstützung für Echtzeit-Zweisprachige Untertitel in Microsoft Teams Webversion Video-Meetings (Öffnen Sie den Teams-Meeting-Link, schalten Sie die zweisprachigen Untertitel im immersiven Übersetzungspanel ein und aktualisieren Sie dann)
- Optimierung der zweisprachigen Untertitel für die englische Version von iQIYI (iq.com)
- Bereitstellung von mehr arXiv-Papieren mit optimiertem zweisprachigem Übersetzungslayout
- Aufgrund von Einschränkungen der Youtube-Website unterstützt das Chrome Tampermonkey-Skript keine zweisprachigen YouTube-Untertitel mehr. Bitte verwenden Sie die [Plugin-Version](https://immersivetranslate.com/).

## 1.8.1

- Behebung von Übersetzungsproblemen mit dem Tampermonkey-Skript SiliconCloud
- Claude-Übersetzung unterstützt jetzt Tibetisch und ermöglicht die Konfiguration des Temperaturparameters
- Die Detailseite des KI-Experten zeigt die vom Experten verwendeten Eingabeaufforderungen an
- In den Shortcut-Einstellungen können jetzt eindeutige Tastenkombinationen für jeden Übersetzungsdienst zugewiesen werden
- Optimierung der Erkennung von arXiv-Papierübersetzungen

## 1.7.9

- Behebung von Problemen mit der Rich Text-Übersetzung für Übersetzungsdienste wie Google, DeepL (z.B. Seiten, die direkt `<button>` etc. anzeigen)
- Behebung des Problems, bei dem die zweisprachige Verknüpfung für YouTube-Videos nicht deaktiviert werden konnte.

## 1.7.8

- DeepL, Microsoft Translate, Google Translate, OpenAI, Claude, Gemini und andere Übersetzungsdienste unterstützen die Übersetzung zur Beibehaltung des Originaltextformats (z.B. Links, Fett, etc.)
- Nach der Auswahl des Textes ändert sich das Rechtsklick-Menü zu [Text übersetzen], klicken Sie darauf, um automatisch zur Immersive Translation Textübersetzungsseite zu springen
- Neuer kostenloser Übersetzungsdienst für große Modelle: SiliconCloud, verfügbar für alle Benutzer.
- Hinzufügen der Zero-One-Thing großen Modellübersetzung, die nach der Registrierung auf der Zero-One-Thing-Plattform durch Eingabe des API-Schlüssels verwendet werden kann.
- Neuer Benutzer-Feedback-Button für Manga-Übersetzungen (nach der Übersetzung eines Mangas klicken Sie auf die [Feedback]-Schaltfläche auf der rechten Seite des schwebenden Balls, um Feedback zur Übersetzungsqualität zu geben).

## 1.7.7

- Einführung eines KI-intelligenten Satztrennungsalgorithmus für automatisch generierte englische Untertitel auf YouTube [Pro Verfügbar]
- Optimierung der Rechtsklick-Übersetzung zu "Übersetzen in xx Zielsprache"
- Unterstützung der immersiven [JS SDK](https://immersivetranslate.com/docs/js-sdk/) Integration für Drittanbieter-Websites
- Optimierung der Hulu-Untertitelanzeige
- Unterstützung der ZOOM-Webversion-Meeting-Untertitelübersetzung

## 1.7.6

- Unterstützung für die Anpassung von KI-Experten, der Eingang befindet sich unten auf der Seite [Einstellungen]->[KI-Experte].
- Optimierung des Untertitelladens auf der TED-Website
- Portugiesisch (Brasilien) wird als Plugin-Sprache unterstützt.
- Unterstützte Seiten für Comic-Übersetzungen
  - [Antbyw](https://www.antbyw.com)
  - [Zerobywzz](https://www.zerobywzz.com)
  - [动漫之家](https://www.idmzj.com)
  - [Jmanga](https://jmanga.org)

## 1.7.5

- Aktiviertes Kopieren von YouTube-Untertiteln
- Optimierung der Untertitelanzeige auf einigen Videoseiten
- Verbesserung der Manga-Übersetzungsgeschwindigkeit

## 1.7.2

- Behebung des Fehlers bei der Comic-Übersetzung im Firefox-Browser.

## 1.7.1

- Verbesserung der Übersetzungsgeschwindigkeit für Comic-Übersetzungen
- Unterstützung neuer Seiten in Comic-Übersetzungen hinzugefügt:
  - [ShonenJumpPlus](https://shonenjumpplus.com)
  - [Heros Web](https://viewer.heros-web.com/)
  - [Comic Days](https://comic-days.com/)
  - [ComicWalker](https://comic-walker.com/)
  - [Web Ace](https://web-ace.jp/)

## 1.6.6

- Unterstützung neuer Seiten für Comic-Übersetzungen hinzugefügt:
  - [Mangabuddy](https://mangabuddy.com/)
  - [Hitomi](https://hitomi.la)
  - [Yamibo](https://www.yamibo.com)
  - [Copymanga](https://www.copymanga.site/)
- YouTube zweisprachige Untertitel unterstützen jetzt intelligentes Satztrennen (Beta) (Nur wenn die immersive Übersetzung von YouTube-Untertiteln manuell in [Einstellungen] - [Video-Untertitel] aktiviert wird und die Originalvideo-Untertitel automatisch generierte englische Untertitel sind)
- Hinzufügen des Übersetzungsdienstes Tencent [【Hunyuan Large Model】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- Behebung der Textlayout-Probleme bei Comic-Übersetzungen für Sprachen im lateinischen Schriftsystem.
- Neue unterstützte Seiten für Comic-Übersetzungen:
  - COMIC FUZCOMICFUZ(https://comic-fuz.com/)
  - MangaDexMangaDex(https://mangadex.org/)
  - KuaiKan ComicsKuaiKanComics(https://www.kuaikanmanhua.com/)
- Behebung eines Problems, bei dem benutzerdefinierte KI-Dienste keine KI-Experten auswählen konnten.

## 1.6.4

- Wenn KI-Experten für die "Intelligente Auswahl" verwendet werden, können verschiedene KI-Experten für verschiedene Websites angepasst werden. Dies kann in [Einstellungen] -> [KI-Experten] -> [Beliebigen Experten eingeben] eingestellt werden.
- Behebung des Problems, bei dem Untertitel in YouTube im "Nur Übersetzung"-Modus nicht angezeigt werden.
- Behebung des Problems, dass zweisprachige Untertitel auf Mubi nicht funktionierten.
- Kompatibel mit PDFs, die mit dem Adobe Acrobat-Plugin geöffnet wurden.
- Alle Benutzer können [online beitragen](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/) zur mehrsprachigen Übersetzung der immersiven Überschnittstelle.

## 1.6.3

- Neue Funktion: Manga-Übersetzung (Beta), auf unterstützten Manga-Websites erscheint ein Manga-Übersetzungsbutton unter dem schnellen Übersetzungs-Schwebeball der Webseite. Durch Klicken darauf wird die Manga-Übersetzung aktiviert. Diese Funktion ist für Pro-Mitglieder verfügbar (500 Seiten pro Monat, zusätzliche Pakete können erworben werden), derzeit werden die folgenden Seiten unterstützt:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)

## 1.6.2

- Neue Funktion: Manga-Übersetzung (Beta), auf unterstützten Manga-Websites erscheint ein Manga-Übersetzungsknopf unterhalb des schwebenden Balls für die schnelle Webseitenübersetzung. Durch Klicken darauf wird die Manga-Übersetzung aktiviert. Diese Funktion steht Pro-Mitgliedern zur Verfügung (500 Seiten pro Monat, zusätzliche Pakete können erworben werden) und unterstützt derzeit die folgenden Seiten:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- Neue Funktion: AI-Übersetzung unterstützt [Doubao large model](https://www.volcengine.com/product/doubao)
- Neue Funktion: Unterstützung für den zweisprachigen Vergleichsmodus mit Übersetzung zuerst und Originaltext danach, der auf der Einstellungsseite -> erweiterte Einstellungen aktiviert werden kann.
- Benutzerdefinierte AI-Modellliste unterstützt die `-all` Syntax, die alle voreingestellten Modelle löschen kann.
- Bei zweisprachigen Videountertiteln wird der Originaltext automatisch in vereinfachtes Chinesisch umgewandelt, wenn die Zielsprache vereinfachtes Chinesisch ist und der Originaltext traditionelles Chinesisch ist, und umgekehrt.
- Behebung des Problems, dass die schwebende Ballverknüpfung unter iOS 18 nicht übersetzen konnte.
- Behebung des Problems, dass benutzerdefinierte Prompts unwirksam waren, wenn zu viele verwendet wurden.

## 1.6.1

- Unterstützt Baidu Qianfan große Modellplattform, Alibaba Bailian große Modellplattform, DeepSeek große Modellplattform.
- Behebung des Problems, dass das Ändern der Zielsprache und anderer Einstellungen im Popup-Panel beim Klicken auf den Übersetzungs-Schwebeball zurückgesetzt wurde.

## 1.5.8

- AI-Experten unterstützen den "Intelligent Selection"-Modus, bei dem das System automatisch den am besten geeigneten AI-Experten basierend auf der aktuellen Website auswählt (zum Beispiel werden technologiebezogene AI-Experten automatisch für The Verge und Hacker News ausgewählt, während die Twitter-Übersetzungsverbesserung automatisch für Twitter ausgewählt wird).

## 1.5.7

- Unterstützung für das Hinzufügen benutzerdefinierter AI-Übersetzungsdienste, die mit OpenAI kompatibel sind, zugänglich am unteren Rand der Seite [Einstellungen]->[Übersetzungsdienste].
- Behebung eines Problems, bei dem zweisprachige Untertitel auf der Domestika-Videoplattform in Safari nicht funktionierten.

## 1.5.6

- Deutlich optimierte Leistung bei der Übersetzung großer Webseiten, der Erstellung von ePub und Untertiteldateien.
- Behebung des Fehlers der Multi-Geräte-Synchronisation in Pro.

## 1.5.4

- Pro-Mitglieder unterstützen die sofortige Nutzung von Claude- und Gemini-Übersetzungsdiensten (Beta)
- YouTube zweisprachige Untertitel unterstützen Schriftart- und Schriftgewichtseinstellungen
- Behebung von Wortgrenzenproblemen beim Umbruch langer Absätze [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- Behebung der Erkennung von japanischen und koreanischen Sprachen
- Behebung des Problems, dass Reddit-Seiten auf mobilen Geräten beim Scrollen nicht übersetzt wurden
- Behebung einiger Seiten, die mit DeepL fehlende Übersetzungen hatten
- Behebung der Multi-Geräte-Synchronisationszeit von Pro-Nutzern, die nicht synchronisiert wurde
- Optimierung der Abdeckungsprobleme der Cloud-Synchronisationseinstellungen
- Optimierung der Prompt-Wörter für AI-Übersetzungsdienste

## 1.5.2

- Behebung des Problems, dass Änderungen am allgemeinen Experten-Prompt den angegebenen AI-Experten-Prompt überschrieben [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- AI benutzerdefinierter Modellname unterstützt erweiterte Syntax, verwenden Sie +, um ein Modell hinzuzufügen, verwenden Sie -, um ein Modell auszublenden, und verwenden Sie model_name=display_name, um den Anzeigenamen des Modells anzupassen, z.B.: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- Behebung des Fehlers, der von Gemini zurückgegeben wurde
- Ausblenden des schwebenden Balls beim Drucken der Seite
- Behebung der Schriftgröße, die sich nicht proportional skaliert, wenn YouTube im Vollbildmodus ist [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- Unterstützung für AI-Übersetzungsdienste, um [AI Expert] festzulegen, um die Übersetzungsstrategie zu spezifizieren, derzeit eine Beta-Funktion, die in [Entwicklereinstellungen](https://dash.immersivetranslate.com/#developer) nach Aktivierung von Beta aktiviert werden kann, und das [AI Expert] Menü kann nach dem Aktualisieren gesehen werden.
- AI-Übersetzungsdienste können jetzt die Modellauswahl anpassen, wie z.B. [OpenAI], das System hat nur einige der am häufigsten verwendeten Modelle eingebaut. Beim Klicken auf die Modellauswahlliste ist der letzte Punkt, den Sie sehen, [Set More Models], nach der Einstellung wird es automatisch gespeichert, um den Benutzern das Testen verschiedener benutzerdefinierter Modelle zu erleichtern.
- Optimierung der Inkonsistenz im Layout von Übersetzungen in einigen Fällen.
- Hinzufügen einer Zurücksetzen-Schaltfläche für den YouTube-Untertitelstil, die schnell auf den Standardstil zurückgesetzt werden kann.
- Behebung des Problems, dass chinesische Untertitel auf YouTube nicht heruntergeladen werden konnten.
- Optimierung der traditionellen chinesischen Benutzeroberfläche.

## 1.4.12

- Behebung des Problems des nicht übersetzten Nachrichten-Dialogfelds beim Öffnen der Reddit-Seite
- Hinzufügen einer temporären Funktion zur Aktivierung der Übersetzungsbearbeitung im "Mehr"-Eintrag des Panels
- Behebung des Problems, dass YouTube Shorts ohne Untertitel immer Untertitel aus dem vorherigen Video anzeigen [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- Behebung des Problems, dass YouTube zweisprachige Untertitel im Vollbildmodus nicht nach oben und unten angepasst werden können [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- Unterstützung für [VK Video](https://vk.com/video) zweisprachige Untertitel
- Unterstützung für unabhängige Aktivierungseinstellungen für YouTube-Video zweisprachige Untertitel (standardmäßig für neue Benutzer aktiviert)
- Optimierung der Fehlermeldungen für die Übersetzung lokaler zweisprachiger Untertitel

## 1.4.11

- Kompatibel mit der Übersetzung des Bing Copilot-Seiteneingabefelds
- YouTube-Untertitelstilsteuerung unterstützt Randgestaltung
- Unterstützung für die Auswahl des Standardübersetzungsdienstes auf der Seite Einstellungen -> Übersetzungsdienst
- Behebung des OpenAI SystemPrompt Platzhalterersatzes
- Behebung des Problems beim Zusammenführen benutzerdefinierter Benutzerregeln
- Behebung der abnormalen Untertiteldarstellung für einige Netflix-Videos [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- Behebung des Problems, dass häufige Änderungen der Übersetzungsfarbe über die Farbpalette unwirksam waren [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- Übersetzungsdienste sind jetzt deutlich unter einem separaten Tab organisiert, was einen umfassenden Überblick über alle verfügbaren Übersetzungsdienste ermöglicht. Darüber hinaus haben Benutzer die Flexibilität, anzupassen, welche Übersetzungsdienste angezeigt werden. Standardmäßig wird nur eine begrenzte Auswahl an Übersetzungsdiensten angezeigt, aber Benutzer können ihre Anzeigepräferenzen im Abschnitt [Mehr Dienste](https://dash.immersivetranslate.com/#services) anpassen.
- Die Einstellungsseite ermöglicht jetzt Anpassungen der [YouTube-Untertitelstile](https://dash.immersivetranslate.com/#subtitle).
- Verbesserungen wurden vorgenommen, um das Problem zu beheben, dass immersive zweisprachige Untertitel nicht angezeigt wurden, wenn Benutzer die Untertitelsprache auf der YouTube-Website auf Chinesisch einstellten.
- Eine neue Verknüpfung wurde für die temporäre Übersetzung namens Claude eingeführt, die auf der [Verknüpfungseinstellungsseite](https://dash.immersivetranslate.com/#shortcuts) konfiguriert werden kann.

## 1.4.8

- Optimierung der Übersetzungsleistung für große Dateien in PDF-Pro
- Verbesserung der Übersetzungsleistung für lange Inhaltsseiten
- Implementierung der Unterstützung für Internationalisierung (i18n) für die Seitendokumentnavigation
- YouTube führt eine Funktion ein, um zweisprachige Untertitel vorübergehend zu aktivieren
- YouTube unterstützt den Download von zweisprachigen Untertiteln (nur für Mitglieder)
- Mobile Geräte fügen Gestensteuerung hinzu, um die Eingabe über [Verknüpfungseinstellungen](https://dash.immersivetranslate.com/#shortcuts) zu verbessern
- Unterstützung für zweisprachige Übersetzung in Google Docs

## 1.4.7

- Behebung des Problems, dass die Übersetzung fehlschlug, wenn OpenAI benutzerdefinierte Prompt-Wörter unter der Testschaltfläche gewechselt wurden
- Behebung des Problems, dass das YouTube-Untertitel-Verknüpfungssymbol nicht angezeigt wurde
- Optimierung der Erweiterungsspracheerkennung

## 1.4.6

- Behebung des Problems, dass benutzerdefinierte Prompt-Wörter unwirksam waren
- Hinzufügen von 50%, 150% Optionen für die Schriftgröße der YouTube-Untertitel

## 1.4.5

- Behebung des Problems, dass Änderungen an den YouTube-Untertitelstilen nicht gespeichert wurden
- Behebung des Verschwindens von Untertiteln im Vollbildmodus auf iOS Safari
- Weitere Optimierung der Übersetzungsgeschwindigkeit von YouTube-Untertiteln
- Das Panel "Mehr Optionen" unterstützt jetzt den [Textübersetzungseintrag](https://app.immersivetranslate.com/text/)

## 1.4.2

- Unterstützung für den Claude-Übersetzungsdienst
- Optimierung der OpenAI-Multi-Prompt-Wörter, Unterstützung des YAML-Formats, was die Flexibilität und Benutzerfreundlichkeit der Konfiguration verbessert
- Deutliche Optimierung der Übersetzungsgeschwindigkeit von YouTube-Untertiteln und Unterstützung für das Umschalten zwischen chinesischer und englischer Reihenfolge, Anpassung der Schriftfarbe und -größe usw.
- Video-Untertitelplattform unterstützt [University of Southampton](https://southampton.cloud.panopto.eu)
- Udemy zweisprachige Untertitel kompatibel mit mobiler Anzeige
- Gemini-Übersetzungsdienst ist standardmäßig ausgeblendet, kann in den Entwicklereinstellungen aktiviert werden, um die Beta dieses Übersetzungsdienstes anzuzeigen

## 1.3.4

- Unterstützung für den kostenlosen Yandex-Übersetzungsdienst
- Optimierung der Gemini-Prompt-Wörter
- Video-Untertitel unterstützen die Einstellung für zweisprachige/originale und Übersetzungsanzeige
- Unterstützung für Leerzeichen zwischen Chinesisch und Englisch in OpenAI-Übersetzungsergebnissen
- Panel-Schalter zur Anzeige nur der Übersetzungsschaltfläche wurde so geändert, dass er nur auf der aktuellen Seite wirksam ist

## 1.3.3

- Optimierung des Übersetzungsanzeigeproblems von Twitter CC-Video-Untertiteln.
- DeepL-Dienst hat Unterstützung für Arabisch hinzugefügt.
- Der Übersetzungsdienst Colorful Clouds unterstützt jetzt Koreanisch, Spanisch, Französisch und Russisch.
- Der OpenAI-Dienst hat Unterstützung für den nordostchinesischen Dialekt hinzugefügt.
- Die automatische Erkennung des Panels zeigt jetzt die Originalsprache an.
- Anpassung der Verknüpfungsbeschreibung für das mobile Panel.

## 1.3.2

- Behebung des Problems, dass das Steuerungsfeld auf mobilen Geräten nicht geschlossen werden konnte

## 1.3.1

- Video-Untertitelplattform unterstützt [DeepLearning.ai](https://learn.deeplearning.ai)
- Unterstützung für Webseitenübersetzung und Video-Untertitelübersetzung in Sprachen wie Arabisch, Hebräisch usw., die RTL (Rechts-nach-Links) Anzeigeprobleme adressieren
- Behebung der Gemini-Übersetzung ins Hebräische
- Behebung eines Problems, bei dem einige traditionelle chinesische Untertitel auf YouTube nicht korrekt angezeigt werden konnten
- Behebung des Anzeigeproblems von Twitter-Untertiteln auf Safari
- Behebung der Verknüpfung für die sofortige Übersetzung zum Seitenende

## 1.2.4

- Behebung des Problems, dass Platzhalter bei der Erstellung von ePub nicht richtig ersetzt wurden
- Unterstützung der Video-Untertitelübersetzung für [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- Optimierte die Frequenzkontrolle von Übersetzungsdienstanfragen
- Kürzliche Microsoft-Übersetzungsdienstanfragen aus China waren instabil; bei Fehlern erkennt das System automatisch den aktuell verfügbaren Übersetzungsdienst, sodass Benutzer schnell wechseln können.
- Optimierte die Fehlermeldung für Netzwerkfehler
- Behoben: Das Problem, dass die Konfiguration der Textfarbe keine RGBA-Vorschau unterstützte [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Behoben: Das Problem, dass beim Upgrade der Safari-Plugin-Version immer die Installations-Erfolgsseite angezeigt wurde
- Microsoft hat Unterstützung für Vietnamesisch hinzugefügt
- Behoben: Das Problem, dass übersetzte Untertitel auf der edx-Seite nicht angezeigt wurden

## 1.2.2

- Unterstützung der Video-Untertitelübersetzung für [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). Unterstützt auch die Übersetzung einiger CC-untertitelter Videos auf Twitter.
- Optimierte Fehler-Pop-ups, Netzwerkproblem-Fehler-Pop-ups erkennen automatisch gültige kostenlose Übersetzungsdienste.
- Behoben: Immersive iOS APP-Unterstützung für YouTube-Vollbildwiedergabe.
- Behoben: Absatzübersetzungsproblem mit Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Unterstützung der Video-Untertitelübersetzung für [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/).
- Behoben: Ein Problem, bei dem einige Pro-Benutzer die Einstellungen im Chrome-Browser nicht ändern konnten.
- Unterstützung der Anzeige von zweisprachigen Untertiteln im Vollbildmodus von YouTube auf iOS.

## 1.2.0

- Unterstützung der Video-Untertitelübersetzung auf [LinkedIn](https://www.linkedin.com/) und [Viu](https://www.viu.com/) Plattformen.
- Hinzugefügt: Mehr Video-Untertitel-Schnellzugriffe für zusätzliche Plattformen.
- Unterstützung für die Einstellung, dass bestimmte Websites/Sprachen nur den übersetzten Text anzeigen.
- Behoben: Ein Problem, bei dem die Einstellungsseite in einigen Fällen auf Safari kontinuierlich geladen wurde.
- Unterstützung für die Übersetzung von Eingabe-Tag-Knoten.
- Optimierte die Fehler-Popup-UI.

## 1.1.9

- Unterstützung der Untertitelübersetzung für YouTube Live und die [Mubi](https://mubi.com/) Plattform.
- Optimierung: Einstellungsseite, URL-Listen-Interaktions-UI (um Mehrdeutigkeiten zu vermeiden, werden Kontrollkästchen standardmäßig nicht angezeigt).
- Unterstützung für die Einstellung der Übersetzungs-Schriftart im Nur-Übersetzungsmodus.
- Hinzugefügt: Schnellzugriff für die Aktivierung von Video-Untertiteln auf Netflix, Ted, Bloomberg, Udemy, Coursera.
- Behoben: Einige übersetzte Stile (wie Unterstreichungen) waren in Safari nicht wirksam.
- Behoben: Während der Seitenübersetzung wurde das Problem, dass das Überfahren der Maus keine erneute Übersetzung auslöste.

## 1.1.8

- Hinzugefügt: Eine Option, dass der untergeordnete Übersetzungsdienst dem Hauptübersetzungsdienst folgt
- Unterstützung von zweisprachigen Untertiteln für [Amazon Prime Video](https://www.primevideo.com)
- Weitere Optimierung der eingebetteten PDF-Übersetzungsfunktion in Sci-Hub
- Behoben: Ein Problem mit dem korrekten Öffnen von Online-PDFs
- Behoben: Das Problem mit der kontinuierlichen Wiedergabe von zweisprachigen Untertiteln auf Netflix

## 1.1.7

- Sie können jetzt eine Schriftart für die Übersetzung auf der Einstellungsseite -> [Grundeinstellungen] -> [Übersetzungsstil] angeben
- Hinzugefügt: Eine Verknüpfungskonfiguration für [Spezifischen Absatz übersetzen] im schwebenden Ball-Panel auf mobilen Geräten
- Optimierte die Empfindlichkeit der Erkennung von Maus-Hover über Ctrl, um zu vermeiden, dass `Ctrl+C` als `Ctrl` missverstanden wird
- Hinzugefügt: Unterstützung für eine neue Verknüpfungseinstellung, die ein schnelles Umschalten ermöglicht, ob Video-Untertitel die eingebauten maschinellen Übersetzungsuntertitel verwenden
- Auf der Sci-Hub-Website wird durch Klicken auf den schwebenden Ball PDFs übersetzt, die in die Webseite eingebettet sind

## 1.1.6

- **Mobile Unterstützung für die Übersetzung spezifischer Absätze:** Die mobile Version unterstützt jetzt die Übersetzung spezifischer Absätze und hat eine Vielzahl von Schnellzugriffsoperationen hinzugefügt, darunter Wischen nach links, Wischen nach rechts, Doppeltippen, Dreifachtippen und Multi-Finger-Touch-Gesten. Diese sind standardmäßig nicht aktiviert und erfordern, dass der Benutzer aktiv die auslösende Geste auf der Einstellungsseite unter [Maus-Hover] auswählt.
- **Gemini Standardversion Update:** Die Standardversion ist jetzt `v1beta`.
- **Behoben: Klassische Chinesisch-Übersetzung:** Behoben: Die klassische Chinesisch-Übersetzungsfunktionalität von Microsoft und OpenAI.
- **Japanische Übersetzungsoptimierung:** Weiter optimiert: OpenAI's japanische Übersetzung zur Verbesserung der Genauigkeit und Flüssigkeit.
- **Immersive Übersetzungserfahrung:** Um sich besser an Benutzergewohnheiten anzupassen, haben wir die Verknüpfung für zweisprachige Untertitel im Vollbildmodus auf der YouTube-Plattform auf die linke Seite verschoben.

## 1.1.5

- Behoben: Das Problem, dass das Dropdown-Menü im Dunkelmodus auf Windows keine Farbe hatte.
- Behoben: Das Ausrichtungsproblem mit der "Mehr"-Option, die nicht linksbündig auf Windows war.

## 1.1.4

- **Popup-Panel-UI-Upgrade:** Das neue Design zielt darauf ab, die Benutzerfreundlichkeit und Verständlichkeit zu verbessern. Dieses Update umfasst:

  - **Neue Funktionen im Hauptmenü:**
    - **Zweisprachiger/Nur-Übersetzungsmodus-Schalter:** Sie können jetzt direkt im Hauptmenü zwischen "Zweisprachiger Übersetzungsmodus" und "Nur-Übersetzungsmodus" wechseln, links neben der Übersetzungsschaltfläche.
    - **Dokumentenübersetzungseintrag:** Der Eintrag für die Übersetzung von "PDF/ePub/Untertitel-Dateien" wurde für den schnellen Zugriff ins Hauptmenü verschoben.
    - **Video-Übersetzungseinstellungen:** Der Eintrag für "Video-Übersetzung" Einstellungen wurde ebenfalls ins Hauptmenü für schnelle Anpassungen platziert.
    - **Neuer Eintrag für Benutzerdokumentation:** Bietet detaillierte Bedienungsanleitungen und Hilfedokumente.

- **Integrierter Dokumentenübersetzungseintrag:** Jetzt können Sie PDF-, ePub- und Untertitel-Dateien über einen einheitlichen Upload-Eintrag übersetzen. Klicken Sie einfach auf die [PDF/ePub]-Schaltfläche im Popup-Panel, ohne [Mehr] auswählen zu müssen.

- **Unterstützung für 5 Video-Websites hinzugefügt:**
  - Unterstützung für Untertitel von Podcasts auf Youtube Music.
  - Unterstützung für die iview.abc.net.au-Website hinzugefügt.
  - Unterstützung für die www.nma.art-Website hinzugefügt.
  - Unterstützung für die creativecloud.adobe.com-Website hinzugefügt.
  - Unterstützung für die www.masterclass.com-Website hinzugefügt.

## 1.1.3

- Behoben: Das Anzeigeanomalieproblem des mobilen Plugins beim Öffnen von PDF-Seiten.
- Optimiert: Die Übersetzungswirkung von GPT-Konversationen.
- Unterstützt: Domain-Übersetzung für Baidu Translate.
- Hinzugefügt: Ein Nur-Übersetzungsmodus auf der Einstellungsseite.
- Hinzugefügt: Eine Erinnerungsfunktion beim Umschalten der Übersetzungsmodi mit Verknüpfungen.
- Behoben: Das Problem, dass beim Übersetzen von Eingabefeldern mit URLs nur Teile des Inhalts übersetzt wurden.

## 1.1.2

- Behoben: Das Problem, dass das Umschalten von Übersetzungsdiensten nicht wirksam wurde, wenn die Seite noch nicht übersetzt war.
- Optimierung: Im Prozess der Übersetzung von Epub und PDF, wenn einige Inhalte nicht übersetzt werden, ist es jetzt möglich, auf dem Panel zu einem anderen Übersetzungsdienst zu wechseln, ohne den gesamten Übersetzungsprozess neu zu starten (die vorherige Logik war, sofort einen neuen Übersetzungsdienst zu verwenden, um das gesamte Buch neu zu übersetzen). Das bedeutet, dass Sie während der Übersetzung zu einem anderen Übersetzungsdienst wechseln und auf [Alle fehlgeschlagenen Absätze erneut versuchen] klicken können, wonach das System die Übersetzung mit dem neuen Dienst fortsetzt.
- Optimierung: Anpassung der Schriftgröße der Übersetzungsfehlerhinweise zur Verbesserung der Lesbarkeit.

## 1.1.1

- Behoben: Das Problem der zu langen englischen Texte bei der Verknüpfung für zweisprachige Untertitel auf YouTube.

## 1.1.0

### Neue Funktionen

- **Verknüpfungseinstellungen**: Hinzugefügt: Ein neues oberes Menü "Verknüpfungen" und die folgenden anpassbaren Verknüpfungsfunktionen:

  - Bestimmen Sie eine Kombination von Tasten, um den Inhalt des aktuellen Eingabefelds zu übersetzen, als Ergänzung zur vorherigen Methode, dreimal schnell die Leertaste zu drücken.
  - Bestimmen Sie eine Kombination von Tasten, um "direkte Übersetzung bei Maus-Hover" auf der Seite vorübergehend zu aktivieren. Durch erneutes Drücken wird diese Funktion aufgehoben.
  - Hinzugefügt: Spezielle Verknüpfungstasten für 6 Übersetzungsdienste (wie DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation), um den temporären Wechsel zwischen Übersetzungsdiensten zu erleichtern.

- **Plugin-Einstellungsseite UI-Update**:

  - In "Erweiterte Einstellungen" wurde eine neue Option hinzugefügt, die es Benutzern ermöglicht, bestimmte Wörter (z.B. "LLM") von der Übersetzung auszuschließen.
  - In "Erweiterte Einstellungen" wurde eine neue Option hinzugefügt, um die minimale Anzahl von Zeichen zu konfigurieren, die erforderlich sind, um einen Absatz zu übersetzen. Der Standardwert ist 4 Zeichen, kann aber höher eingestellt werden (z.B. 20), sodass nur längere Absätze übersetzt werden.
  - Hinzugefügt: Ein Tutorial für Anfänger, das schwebende Ball-Einstellungen, Video-Untertitel-Einstellungen und Maus-Hover-Einstellungen abdeckt.

- **YouTube Zweisprachige Untertitel**: Hinzugefügt: Ein Schnellzugriff im YouTube-Video-Wiedergabefenster, um zweisprachige Untertitel zu aktivieren oder auszublenden (diese Funktion kann deaktiviert werden).

- **Deepl Sprachunterstützung**: Unterstützung für Portugiesisch (Brasilien) hinzugefügt.

- **Neuer Benutzerleitfaden**: Wenn neue Benutzer zum ersten Mal eine Seite in einer Nicht-Zielsprache öffnen, wird eine schwebende Ball-Hilfe-Leitblasen angezeigt.

### Optimierung und Fehlerbehebungen

- **UI-Optimierung**: Neugestaltung der UI für Seitenübersetzungsfehlerhinweise, um sie verständlicher zu machen. Bei vielen Fehlern wird ein Popup aktiv den Benutzer darauf hinweisen.

- **Fehlerbehebungen**:

  - Behoben: Das Problem, dass die Maus-Hover-Übersetzung fehlschlug, wenn die Seite den Fokus verlor.
  - Behoben: Das Problem, dass weniger als 3 Zeichen in der Eingabefeld-Verbesserungsfunktion nicht übersetzt wurden.
  - Behoben: Das Problem, dass einige Verzeichnisse bei der Erstellung von zweisprachigen Epubs nicht übersetzt wurden.

- **Feature-Entfernung**: Entfernt: Die zweisprachige Informationsverbesserungsfunktion (gleichzeitige Anzeige von englischen Suchergebnissen auf Google-Suchseiten).

### Weitere Updates

- **openAI Konfigurationsupdate**: Unterstützt jetzt die Einstellung der Anzahl der Konfigurationen pro Sekunde in Dezimalzahlen, wie 0.5, was 1 Anfrage alle 2 Sekunden bedeutet.

## 0.12.14

- Behoben: Das Problem der Erkennung der Standardsprache auf einigen Maschinen nach der ersten Installation.
- Optimierung: Die Standardreihenfolge der Webseitentitel wurde auf [Chinesisch - Englisch] geändert.

## 0.12.13

- Behoben: Problem mit der OpenAI-Übersetzung langer Absätze in einigen Fällen. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Optimiert: Bei Verwendung von Maus-Hover, das Problem, dass der Fokus auf der Seite verloren geht und dann das erneute Auslösen unwirksam wird.
- Behoben: Das Problem, dass der Cache nach der Änderung des Prompts/Modells in OpenAI weiterhin vorhanden war.

## 0.12.12

- Aktualisiert: Optimierung des Popup-Panels, einige Optionen für die aktuelle Website wurden entfernt.
- Optimiert: Verbesserter Prozess zum Zusammenführen manueller Untertitel.
- Optimiert: Automatische Einstellung der Zielsprache basierend auf der Browsersprache.
- Hinzugefügt: Unterstützung für zweisprachige Untertitel auf der [ArtStation](https://www.artstation.com/learning) Lernplattform und [ZDF](https://www.zdf.de/).
- Behoben: Problem gelöst, bei dem Titel auf der jstor Listen-Seite nicht übersetzt wurden [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Behoben: Problem behoben, bei dem nur ein Teil des Inhalts auf Hacknews verschwand [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Unterstützung für zweisprachige Untertitel für [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/) und [Domestika](https://www.domestika.org) Plattformen hinzugefügt.

## 0.12.10

- Problem mit der Autorisierung der Gemini-Domain unter dem Tampermonkey-Skript behoben.
- Unterstützung für Echtzeit-Untertitelübersetzung für Twitter Space.
- Für ältere Versionen des Tampermonkey-Skripts wurde nun ein Update-Hinweis auf der Einstellungsseite hinzugefügt.

## 0.12.9

- Unterstützung für Gemini-Übersetzung hinzugefügt.
- Problem behoben, bei dem Übersetzungen in einigen Fällen nicht rechtzeitig reagierten, wenn die Webseite in die mittlere Position gescrollt wurde.
- Fehler behoben, bei dem das Umschalten von Untertiteln auf einigen Video-Websites dazu führte, dass die Übersetzung wiederholt angezeigt wurde.
- Problem behoben, bei dem die Maus in einigen Fällen ohne Drücken der Tastenkombination weiter übersetzte.
- Auf macOS wurde der Anzeigename der Panel-Tastenkombination optimiert.

## 0.12.8

- Reparatur der Anzeige der Originalvideo-Untertitel, wenn "Aktuelle Seite nie übersetzen" eingestellt ist.
- Konflikt mit einigen Plug-ins behoben, die zu unendlichem Seiten-Reload führten.
- Reparatur der Nicht-Übersetzung einiger Absätze nach Aktivierung von Zeilenumbrüchen bei langen Absätzen.
- Behoben [Wenn die Webseitenübersetzung vorübergehend für eine lange Zeit aktiviert ist, wird durch Klicken auf das Panel [Immer diese Website übersetzen] die immer Übersetzung nicht aufgehoben #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Zweisprachige Untertitel hinzugefügt zur Unterstützung von [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) Plattformen. https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/) Plattformen
- Der Hoverball ist jetzt standardmäßig ausgeblendet, wenn das Video im Vollbildmodus ist.
- Problem mit ruckelndem Klicken im Firefox-Seiten-Hoverball-Aktionspanel behoben.
- Unterstützung für Zusammenarbeit unter der pubmed.ncbi.nlm.nih.gov Seite und dem scholarscope Plugin
- Problem mit ruckelnder Übersetzungsseite im Reddit-Eingabefeld behoben

## 0.12.6

- Problem behoben, dass die Übersetzung von YouTube/Web of Science etc. beim Wechseln der Tabs nicht empfindlich ist.
- Hoverball auf Mobilgeräten unterstützt jetzt Langdruckoperationen, Kurzdruck zum Übersetzen, Langdruck zum Öffnen des Panels.
- Beim Übersetzen von zweisprachigen E-Books wird jetzt auch das Inhaltsverzeichnis übersetzt.
- Die Suchverbesserung (einige Seiten von Google Search zeigen zweisprachige Suchergebnisse an) ist jetzt standardmäßig nicht aktiviert und wird im nächsten Release entfernt.

## 0.12.5

- Problem behoben, dass das Erstellen von E-Books aus dem Panel durch Klicken auf Übersetzungen nicht funktioniert

## 0.12.4

- Wenn Sie im Panel zweisprachige Untertitel aktivieren, wird die Seite zuerst automatisch aktualisiert (um zweisprachige Untertitel genauer anzuzeigen), und einige Seiten erfordern immer noch, dass Benutzer manuell auf die "CC"-Schaltfläche auf der Seite klicken, um Untertitel zu aktivieren.
- Optimierung von Grease Monkey, Safari-Spracherkennung
- Bietet schnellen Zugriff auf zweisprachige Versionen aller Papiere auf der [Arxiv](https://arxiv.org/abs/1910.06709) Papierseite.
- [Hoverball-Unterstützung konfiguriert, um links fixiert zu werden #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Fix Learning Mode Anzeigeproblem #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Vorübergehendes Aktivieren der Webseitenübersetzung für eine bestimmte Zeit hebt die immer Übersetzung nicht auf #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Optimierung von PDF-Datei-Initialisierungsproblemen

## 0.12.3

- Fix für [permanentes Deaktivieren der Video-Untertitel] Funktion funktioniert nicht [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)

## 0.12.2

- Zweisprachige Untertitelunterstützung wird für mehr Video-Plattformen bereitgestellt, die jetzt unterstützt werden: [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy] (https://www\.khanacademy.org/), [Coursera] (https://www\.coursera.org/), [Vimeo] (https://vimeo.com/), [Nebula] (https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), etc. (Beachten Sie, dass aufgrund technischer Einschränkungen einige Websites die Seite nach dem ersten Einschalten der zweisprachigen Untertitel aktualisieren müssen oder warten müssen, bis die Übersetzung abgeschlossen ist, um die zweisprachigen Untertitel anzuzeigen). (Beachten Sie, dass aufgrund technischer Einschränkungen einige Websites die Seite nach dem ersten Öffnen der zweisprachigen Untertitel aktualisieren müssen oder warten müssen, bis die Übersetzung abgeschlossen ist, um die zweisprachigen Untertitel anzuzeigen)
- Plugin-Zip-Größe erheblich optimiert, im Vergleich zum Original halbiert, schnellerer Download und Update.
- Problem mit erweitertem PDF-Download behoben
- Ein Schnellübersetzungs-PDF-Portal auf der rechten Seite der [Arxiv](https://arxiv.org/abs/1910.06709) Papierseite hinzugefügt, das zu einer sauberen HTML-Seite führt (nur von einigen Papieren unterstützt, da es erfordert, dass die Originalautoren den Quellcode einreichen, sodass ungefähr 50% der Papiere dieses Portal anzeigen)
- Online-PDF-Seiten ohne .pdf-Erweiterung können jetzt direkt zur PDF-Übersetzungsseite springen, indem Sie auf den Hoverball auf der Seite klicken.
- Einige Eingabefeld-Verbesserungsprobleme unter Safari behoben
- Optimierung der Spracherkennung in Grease Monkey und Safari

## 0.11.6

- 11 neue Schnittstellensprachen für das Plugin und die offizielle Website hinzugefügt, jetzt werden 14 Schnittstellensprachen unterstützt, darunter Chinesisch vereinfacht, Chinesisch traditionell, Englisch, Japanisch, Koreanisch, Russisch, Spanisch, Portugiesisch, Hindi, Italienisch, Deutsch, Französisch, Arabisch und Persisch.
- Die im letzten Release hinzugefügte zweisprachige Freigabe (Aktualisierungsmodus) wurde in zweisprachige Seiten-Snapshot-Freigabe geändert, sodass der geteilte Inhalt originaler ist und eine breitere Anpassungsfähigkeit aufweist.
- Problem mit Emoji am Ende des Twitter-Eingabefelds behoben, das nicht übersetzt werden kann
- Problem behoben, bei dem der Inhalt von Drittanbieter-Plug-ins in einigen Szenarien übersetzt wird
- Reparatur des Online-PDF-Hoverball-Klicks ohne Reaktion

## 0.11.5

- Sie können jetzt einen öffentlichen Link zur übersetzten zweisprachigen Seite für Immersive Translate generieren.
  - [Klicken](/docs/share/) Sie auf das Immersive Translate Sharing Icon, um es mit einem Klick zu generieren!
- Problem gelöst, dass einige Plattformen nicht erkennen konnten, ob die Maus unterstützt wird oder nicht
  - Es gibt einige Desktop-Browser, die sowohl Touchscreen als auch Maus unterstützen, und Immersive Translates kann technisch nicht erkennen, ob solche Plattformen die Maus unterstützen, daher haben wir die Option [Force Enable Mouse Support] in den [Mouse Hover] Einstellungen hinzugefügt

## 0.11.2-0.11.4

- Erfahrung optimieren, einige Fehler beheben

## 0.11.1

- Das Standardmodell für OpenAI-Übersetzungen ist: GPT3.5-turbo-1106.
- Optimierte den chinesischen Prompt für OpenAI, jetzt weniger anfällig für Halluzinationen!
- Die Länge der OpenAI-Prompts von 90 auf 40 reduziert, um noch mehr Traffic zu sparen.

## 0.11.0

- Ruckelnde Seiten-Hoverball-Klicks behoben
- Azure-Übersetzungsprobleme behoben

## 0.10.9

- Einige kleinere Probleme behoben

## 0.10.8

- Unterstützung für das Einrichten von Hoverball-Schnellübersetzungsschaltflächen (sowohl PC-/Mobilunterstützung)
- Optimierung der Grease Monkey Sprachbeurteilung
- Problem mit der Übersetzung von txt-Dateien behoben

## 0.10.7

- Maus-Hover-Unterstützung, erneut Strg drücken, um den Originaltext anzuzeigen
- Maus-Hover ignoriert nie zu übersetzende Sprache
- Youtube-Zweisprachige Untertitel-Optimierung

## 0.10.6

- Youtube-Untertitelunterstützung nur für Übersetzungen
- Grease Monkey Niedrigversion-Update-Warnung hinzufügen
- Problem behoben, dass lokale txt-Dateien nicht übersetzt werden können

## 0.10.5

- Problem behoben, dass Youtube gelegentlich zur Startseite zurückkehrt

## 0.10.4

- Problem mit Youtube-Untertitelkonflikt mit Dual-Untertitel-Plugin behoben (Immersive Translate der Youtube-Untertitelübersetzung ist nicht aktiviert, wenn das Youtube-Dual-Plugin erkannt wird, um Konflikte zu vermeiden)
- [Funktion zum dauerhaften Deaktivieren von Video-Untertiteln] hinzugefügt, wenn es andere Konfliktprobleme gibt und Sie die zweisprachige Untertitelfunktion mit Immersive Translate nicht aktivieren möchten.
- Optimierung von Untertitelumbrüchen

## 0.10.3

- Problem mit benutzerdefiniertem DeppL Auth Key Übersetzung behoben

## 0.10.3

- Perfekte Unterstützung für Youtube-Videos mit zweisprachigen Untertiteln 🎉.
- Bei Artikelseiten wird jetzt zuerst der Haupttext übersetzt, bevor der Rest des Seitenleisteninhalts übersetzt wird
- Optimierung der DeepL-Übersetzungskontextualisierung
- Optimierung der OpenAI-Übersetzung von Untertiteldateien für Kontextualisierung

## 0.10.1

- Priorität der Haupttextübersetzung erhöhen, um das Übersetzungserlebnis zu optimieren
- Problem behoben, dass ins Klick mehr Text nicht übersetzt wird

## 0.9.8

- Erfahrung optimieren, einige Fehler beheben

## 0.9.7

- Problem mit automatischer Übersetzung behoben, wenn readwise hervorgehoben ist

## 0.9.6

- Problem behoben, dass der Cache durch Abmelden des Benutzer-Logins gelöscht wird.

## 0.9.5

- Fehlerbehebungen für Online-E-Books

## 0.9.4

- Optimierung der Eingabeverbesserungserkennung zur Reduzierung von Fehltreffern
- E-Book- und Untertitelübersetzung online

## 0.9.3

- Übersetzung der Eingabebox: zeigt eine Pop-up-Erinnerung an, wenn sie zum ersten Mal verwendet wird, und der Benutzer kann wählen, ob er sie dieses Mal oder dauerhaft deaktivieren möchte, um versehentliche Berührungen zu vermeiden.
- Optimierung der Exportgeschwindigkeit nur für PDF-Übersetzungen, wenn Sie sich entscheiden, nur die Übersetzung zu exportieren, können Sie direkt die System-PDF-Vorschau aufrufen, um schneller zu exportieren.
- Deeplx unterstützt mehrere URLs, einfach mit trennen.

## 0.9.2

- Das PDF-Übersetzungstool wird auf die Online-Version migriert: https://app.immersivetranslate.com/pdf/ , sodass Grease Monkey und Safari PDF-Übersetzungen verwenden können und Probleme besser iteriert werden können, ohne eine Version herausgeben zu müssen, um das Problem zu lösen.
- POPUP UI-Optimierung, das Panel ist schöner!

## 0.9.1

- Behebung von Dateinamenproblemen bei der Erstellung von Epub-eBooks

## 0.8.8

- PDF unterstützt Zeilenabstand und Wortabstandsanpassungen zur erneuten Erkennung von Absätzen
- Behebung des automatischen Scrollens bei der mobilen Online-Lesung von Epub

## 0.8.7

- PDF-Unterstützung nur für Übersetzungsdownloads
- Behebung des Safari-Google-Anmeldeproblems

## 0.8.2 - 0.8.6

- Ermöglicht das Einstellen des Intervalls zwischen den Auslösern der Eingabeverbesserungskombination
- Behebung einiger Fehler

## 0.8.1

- Optimierung der Spracherkennung
- Beta-Funktionen: Benutzerdefinierte API (Beta in den Entwicklereinstellungen aktiviert)
- Unterstützung für AliCloud Translation
- Behebung einiger Fehler

## 0.8.0

- Unterstützte Benutzersysteme
- Unterstützt [Enable Pro Membership](/pricing), wodurch Benutzer Deepl- und OpenAI-Übersetzungen sowie Cloud-Synchronisationseinstellungen genießen können.
- Maus-Hover-Übersetzungsdienst kann individuell eingestellt werden
- Eingabebox-Übersetzungsdienst kann separat eingerichtet werden
- PDF-Übersetzungsoptimierung
- Behebung einiger Fehler

## 0.7.16

- PDF-Übersetzung mit neuen Optionen zur schnellen Steuerung des Übersetzungsstils (PDF-Dateien sind sehr seltsam und das Aktivieren dieser Optionen kann für einige PDF-Dateien mit unordentlichem Format nützlich sein)
- iOS- und macOS-Versionen sind zurück im Apple Store Country Store

## 0.7.15

- Wir wurden von Apple benachrichtigt, dass OpenAI-Übersetzungen vorübergehend aus iOS und macOS entfernt wurden, und wir versuchen, sie in China neu zu starten.

## 0.7.11- 0.7.14

- Behebung: Gmail-Übersetzungsproblem in allen Regionen
- Vorübergehende Deaktivierung der PDF-Exportfunktion von Safari aufgrund der Einschränkung von Safari bei Plug-in-Downloads (Fehler).
- Behebung einiger anderer Probleme

## 0.7.10

- Popup-Browser-Icon-Panel-UI-Upgrade, ein bisschen mehr Design ～
- Behebung des Problems, dass einige japanische Passagen nicht übersetzt werden.

## 0.7.9

- PDF unterstützt endlich den Export von zweisprachigen Versionen! Sie können auf die Schaltfläche [Speichern] klicken, um die übersetzte zweisprachige PDF-Datei zu exportieren.
- Benutzerdefinierte Regeln unterstützen jetzt das Zusammenführen mit den standardmäßig integrierten Regeln, z.B.: `{"id": "youtube", "selectors.add":["#test"]}` bedeutet, ein `#test` zu den vorhandenen Selektoren hinzuzufügen, `selectors` bedeutet, den Standard zu überschreiben, `selectors.remove` bedeutet, einen der Standardselektoren zu löschen, und `selectors.remove` bedeutet, einen der Standardselektoren zu löschen.
- Aktualisiertes Safari-Icon, etwas größer.
- Weitere Fehlerbehebungen

## 0.7.8

- Fehlerbehebungen

## 0.7.7

- Anpassung an Safaris Systemstil, Safaris Erweiterungs-Icon wurde in eine transparente Umrissform geändert.
- Hinzufügen von Statusänderungen des Browser-Icons, wenn eine Webseite übersetzt wurde, wird automatisch ein ✅ in der unteren rechten Ecke des Browser-Icons hinzugefügt.
- Automatische Aktivierung der Übersetzung häufig verwendeter englischer Websites für neue Benutzer
- Behebung von Übersetzungsproblemen mit https://claude.ai/

## 0.7.6

- Eingabeverbesserte Unterstützung für Übersetzungsergebnisse ctrl+z Rückgängig
- Unterstützung der Übersetzung im Flying Book-Dokumentlesemodus
- Anpassung https://pi.ai/talk

## 0.7.5

- Behebung des Problems, dass das Grease Monkey-Icon nicht angezeigt wird
- Behebung mehrerer Probleme

## 0.7.4

- Behebung mehrerer Probleme
- Die Einstellungsseite unterstützt das Löschen ausgewählter URLs im Batch.
- Unterstützt das Aktivieren/Deaktivieren der YouTube-Untertitelübersetzung, um Konflikte mit anderen verwandten Plugins zu vermeiden.
- Arigato Translator unterstützt das Festlegen von Feldern und Terminologie-ID

## 0.7.2

- Eingabebox-Verbesserung: ermöglicht das Weglassen des Präfixes // und das Auslösen der Übersetzung des gesamten Eingabefelds mit 3 Leerzeichen, oder Sie können diese Option auf der Einstellungsseite deaktivieren.

## 0.7.1

- Unterstützung der Suchverbesserung, wenn aktiviert, wenn Sie in Google/Google News auf Chinesisch suchen, wird die rechte Spalte automatisch die Suchergebnisse der entsprechenden englischen Schlüsselwörter anzeigen, die standardmäßig aktiviert ist.
  - Grund: Wir haben festgestellt, dass in der Google-Suche die Suchergebnisse für chinesische Schlüsselwörter und englische Schlüsselwörter sehr unterschiedlich sein können. Mit der aktivierten Immersive Translated Search Enhancement suchen wir automatisch nach denselben Schlüsselwörtern auf Englisch für Sie und zeigen sie auf der rechten Seite an. Sie können es deaktivieren, wenn Sie die Funktion nicht benötigen.
  - Safari wird aufgrund von API-Beschränkungen nicht unterstützt.

## 0.6.20

- Ändern der Standardeinstellungen: Aufgrund des Feedbacks einer großen Anzahl von Benutzern, dass sie das Übersetzungstool nach der Installation nicht verwenden werden, ist ihre Erwartung an das Übersetzungstool, dass es nach der Installation automatisch englische Webseiten übersetzt. Daher wurde ab dieser Version für chinesische Benutzer die Option, englische Seiten standardmäßig zu übersetzen, aktiviert (wenn der Benutzer zuvor eine Spracheinstellung hatte, die immer übersetzt wird, wird diese beibehalten, und die Änderung betrifft nur die anfänglichen Einstellungen der Erweiterung), und es muss storniert werden, kann leicht im [Popup-Panel oder auf der Einstellungsseite](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91) storniert werden.

## 0.6.19

- Behebung von PDF-Fehlern
- Behebung des Web of Science-Fehlers
- Anpassung an feeder.com
- Behebung, dass epub einige Bücher nicht übersetzt

## 0.6.18

- Behebung des Überlaufproblems der Safari-Popup-Breite.
- Optimierung des Erstellungsprozesses

## 0.6.17

- Optimierung von Fehlermeldungen
- Optimierung der Zielsprachenauswahl, jetzt werden nur die von dem entsprechenden Übersetzungsdienst unterstützten Sprachen angezeigt
- PDF-Übersetzungsoptimierung
- Anpassung an die Good Reads-Website, Amazon und South China Morning Post-Website

## 0.6.16

- Hinzufügen der Anzeige der PDF-Seite ohne Berechtigung
- Reparatur der Anzeige von PDF-Textlistenabsätzen
- Vergrößerung der PDF-Kleinbuchstabenskalierung auf Chrome und Safari

## 0.6.15

- Behebung des Problems, dass beim Öffnen von PDF-Dateien das Erweiterungspanel anzeigt, dass keine Berechtigungen vorhanden sind.
- Behebung des Problems, dass die Eingabebox-Verbesserung nicht aktiviert ist, wenn die Website auf "nie übersetzen" eingestellt ist.

## 0.6.14

- PDF-Übersetzungsoptimierung, der Übersetzungsbereich kann jetzt bearbeitet/gezogen/gelöscht werden
  - Ziehen oben links, löschen oben rechts, Größe ändern unten rechts
- Windows-Dropdown-Box linksbündig
- Unterstützung für Traditionelles Chinesisch und Vereinfachtes Chinesisch

## 0.6.13

- Behebung des Problems der wiederholten Übersetzung bei Maus-Hover
- PDF-Übersetzungsunterstützung zum Ziehen, um die Größe zu ändern und den Inhalt der Übersetzung zu bearbeiten

## 0.6.12

- Behebung, dass Epub-Übersetzungsbilder in einigen Browsern kleiner werden
- Optimierte Eingabebox-Übersetzung, funktioniert jetzt reibungslos in Bard!

## 0.6.10

- OpenAI-Standardmodell auf Version 0613 geändert
- Behebung einiger Eingabebox-Stile
- Intelligenteres Erkennen, ob es sich um einen Navigationsbereich handelt, und wenn ja, wird keine Übersetzung durchgeführt
- Behebung möglicher XSS-Injektionsangriffe

## 0.6.8

- Das Erweiterungspanel kann jetzt nicht unterstützte Seiten anzeigen (z.B. Seiten ohne Berechtigungen und nicht-HTML-Seiten)
- Eingabebox-Verbesserung zur Anzeige des Ladezustands in der Übersetzung
- Aktualisierung der Standardladefarben in Übersetzungen
- Wenn die Eingabebox ohne Präfix konfiguriert ist, unterstützt sie die Übersetzung `ja Hello` ins Japanische und `English Hello` ins Englische.

## 0.6.6

- Behebung: einige Bereiche werden nicht übersetzt (quora)

## 0.6.5

- Google Bard-Optimierung
- Eingabebox-Übersetzung unterstützt die direkte Übersetzung des gesamten Textfelds ohne Präfixe.
- Optimierung des Problems, dass OpenAI-Übersetzungen gedankenlos Punkte hinzufügen (wenn im Originaltext kein Punkt erkannt wird, wird er entfernt, wenn OpenAI einen Punkt zurückgibt)
- Probleme mit Safari-Untertiteldateien, die nicht erkannt werden

## 0.6.3

Die Standardsprache für die Eingabebox-Übersetzung kann jetzt das Leerzeichen weglassen, d.h. //Hello World kann ebenfalls übersetzt werden.

## 0.6.2

Die aufregendste Eingabebox-Verbesserung ist da:

- Geben Sie: // Hello World in die Eingabebox auf einer beliebigen Webseite ein, dann dreifach auf die Leertaste klicken, um den Absatz ins Englische zu übersetzen
- Sie können auch die Übersetzung in eine bestimmte Sprache angeben: /ja Hello World, dann dreifach auf die Leertaste klicken, um den Absatz ins Japanische zu übersetzen

[Klicken Sie hier für eine schnelle 30-Sekunden-Einführung](/docs/input/)

## 0.6.0

- Erste Veröffentlichung im Juni, migriert von der vorherigen persönlichen Subdomain https://immersive-translate.owenyoung.com zur neuen Domain https://immersivetranslate.com/
- Die Funktionalität ist weitgehend unverändert (neue Funktionen werden in der nächsten Version verfügbar sein!)

## 0.5.17

- Behebung des Problems, dass: zweisprachige eBooks nach dem Export keine Bilder haben

## 0.5.16

- Behebung: OpenAI-Übersetzungsproblem in Traditionellem Chinesisch

## 0.5.15

- Optimierung: Die Mindestanzahl von Zeichen in einem Absatz, die die Übersetzung auslöst, wurde auf mindestens 4 Zeichen geändert, um Verwirrung zu reduzieren, während andere Funktionen verwendet werden, um die Übersetzung der Navigations- und Endbereiche der Website zu vermeiden.
- Behebung: Github-Details werden nach dem Erweitern nicht übersetzt.

## 0.5.14

- Behebung des Problems, dass Bilder auf einigen Webseiten von: nach dem Kopieren größer werden
- Behebung: Medium-Kommentarbereich wird nicht übersetzt
- Behebung des Problems, dass Bilder auf einigen Seiten von: falsch kopiert wurden

## 0.5.12

- Funktion: Split Line Translation Style fügt eine vertikale Trennlinie für einzeilige Übersetzungen hinzu
- Behebung: Sehr seltene Fälle von Absatztrennungen.
- Eine großartige erste Einrichtungseinführungsseite für neue iOS-Benutzer.

## 0.5.11

- Unterstützung der Untertitelübersetzung für den Export von Übersetzungen nur
- Behebung: Einige Elemente werden beim Maus-Hover nicht erkannt
- Behebung: Tweet-Teilzeilenumbrüche werden nicht erkannt
- Behebung: eBook-Erstellungsstil funktioniert nicht

## 0.5.10

- Behebung: Tweet-Zeilenumbrüche werden nicht erkannt
- Behebung: Reddit-Detailseite gibt einige Absätze zurück, die nicht übersetzt werden können
- Behebung eines Problems mit: bei dem einige der Code-Tags nicht korrekt erkannt wurden.

## 0.5.9

- Behebt Absatzumbrüche in einigen Fällen bei:
- Behebung: Tampermonkey-Umschaltung zeigt nur Übersetzungen an
- Behebung: Problem mit dem Online-Lesestil von eBooks funktioniert nicht

## 0.5.8

- Behebt das Problem, dass die temporäre Einstellung der Übersetzungsdauer von Websites nicht wirksam wird.

## 0.5.7

- Super-Update!

- Die Funktion "Nur Übersetzungen anzeigen" ist da! Klicken Sie auf [Mehr] -> [Umschalten, um nur Übersetzungen anzuzeigen].

  - Unterstützt benutzerdefinierte Tastenkombinationen, die in den Schnittstelleneinstellungen -> Tastenkombinationen festgelegt werden

- Optimierung des OpenAI-Anfragefrequenz-Limitierungsproblems

- ChatGPT verwendet standardmäßig das mobile Modell, das schneller ist!

- Neugestaltung der Web-Kernanalyse, was bedeutet:

  - Großflächige Webseitenübersetzung in Sekunden
    - Zum Beispiel: https://pve.proxmox.com/pve-docs/pve-admin-guide.html, die vorher 30 Sekunden dauerte, wird jetzt in Sekunden umgeschaltet.
  - Sehr geringer Speicherverbrauch für komplexe Webseiten
    - Zum Beispiel: https://www\.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Anpassung an mehr Websites

- Alle Übersetzungen der ShadowRoot-Website werden unterstützt.

  - Zum Beispiel: https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - Zum Beispiel der Kommentarbereich von: https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Behebung des Weißbildschirmproblems nach der Übersetzung von Websites mit Hydration wie Next.js.

  - Zum Beispiel: https://webpack.js.org/

- Behebung des Problems, dass die Änderung der Maus-Hover-Tastenkombination eine Seitenaktualisierung erforderte, um wirksam zu werden

- Behebung eines Problems mit der Erkennung von Zeilenumbrüchen in TXT-Dateien.

- Viele Updates!

- Die Funktion "Nur Übersetzung anzeigen" ist da! Klicken Sie auf "Mehr" -> "Umschalten, um nur Übersetzungen anzuzeigen".

  - Unterstützt benutzerdefinierte Tastenkombinationen, die in "Schnittstelleneinstellungen" -> "Tastenkombinationen" festgelegt werden können

- Optimiert für das OpenAI-Anfrageratenlimitproblem

- Der Web-Kern wurde neu aufgebaut, was bedeutet.

  - Sofortige Übersetzung für große Websites
  - Minimaler Speicherverbrauch für komplexe Webseiten
  - Bessere Kompatibilität mit mehr Websites

- Unterstützt jetzt Übersetzungen für alle Websites mit ShadowRoot.

- Behebung des Weißbildschirmproblems nach der Übersetzung von Websites mit Hydration, wie Next.js

- Behebung des Problems, dass die Änderung der Maus-Hover-Tastenkombination eine Seitenaktualisierung erforderte, um wirksam zu werden

- Behebung des Problems mit der Erkennung von Zeilenumbrüchen in TXT-Dateien.

## 0.5.6

- Behebung: macOS neues Tab-Popup-Problem.
- Feature: Neue Leitfaden-Seite für neue Benutzer.

## 0.5.5

- Behebung: Problem mit dem Mauszeigerbereich.

## 0.5.4

- Behebung: Spa-Seite duplizieren

## 0.5.3

- Behebung: Maus-Hover-Hotkey-Listener.
- Behebung: PDF-Dokumentübersetzung
- Feature: Neue Kundenleitfaden-Seite hinzufügen

## 0.5.2

- Behebung: Benutzerskript-Maus-Hover-Tastenkombinationseinstellungen

## 0.5.1

- Behebung: OpenAI API funktioniert nicht.

## 0.5.0

- Feature: Übersetzen Sie den aktuellen Absatz, wenn die Maus darüber schwebt.
- Feature: PDF-Übersetzung neu gestalten, jetzt können Sie die meisten PDFs mit Immersive Translate übersetzen
- Behebung: Deaktivieren des Kontextmenüs funktioniert nicht [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Behebung: Vermeidung der Content Security Policy für [Mastondon](https://mastodon.social/)

## 0.4.11

- Behebung: Benutzerskript-Berechtigung (nur für Benutzerskript).

## 0.4.8

- Feature: Bing Translate zu Microsoft Translate für stabilere Qualität.
- Behebung: Reine TXT-Webseite wie [diese](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Leistung: Einige untergeordnete Werbeseiten auf der Website ausschließen, und die Leistung hat sich ein wenig verbessert

## 0.4.7

- Behebung: Firefox-Benutzerskript-Popup fehlt.

## 0.4.6

- Feature: Erlauben Sie Drittanbietern, Dokumentereignisse zu senden, um `toggleTranslatePage` aufzurufen
- Feature: iOS-App fügt Schaltfläche zum Aktivieren der Erweiterung und Link zu Communities hinzu
- UI: OpenAI-Einstellungsfeldmodell verwendet Auswahl anstelle von Texteingabefeld.

## 0.4.5

- Behebung: iOS 15.0 Safari-Erweiterungsproblem.
- Behebung: macOS Safari-Erweiterungstastenkombinationen
- Behebung: Popup der Content Security Policy für Erweiterung und teilweise für Benutzerskript.

## 0.4.4

- Chore: Entfernen von console.log

## 0.4.3

- Behebung: sup, sub Tag Leerzeichenerkennung.
- Feature: Unterstützung von ChatGPT Plus Website als Übersetzungsdienst, Dies ist eine Beta-Funktion, die Sie durch Aktivieren der Beta-Funktion in den Entwicklereinstellungen zugreifen können. Dies ist sehr langsam, da ChatGPT nur eine Anfrage gleichzeitig senden kann. Stellen Sie sicher, dass Sie ein ChatGPT Plus-Konto haben, da es mehr Einschränkungen für das kostenlose Konto gibt, und ich bin mir nicht sicher, ob dies ein Risiko für Ihr Konto darstellt, seien Sie vorsichtig, um sicherzustellen, dass Sie ein ChatGPT Plus-Konto haben, da es mehr Einschränkungen für das kostenlose Konto gibt, und ich bin mir nicht sicher, ob dies ein Risiko für Ihr Konto darstellt, seien Sie vorsichtig, es zu verwenden.

## 0.4.1

- Behebung: Firefox-Kontextmenü verschwand nach dem Neustart.
- Unterstützung von Azure OpenAI

## 0.4.0

- Feature: Unterstützung der Übersetzung lokaler Untertiteldateien (.srt,.ass,etc.)

## 0.3.17

- Feature: Unterstützung der Übersetzung lokaler .txt-Dateien.
- Behebung: Kontextmenü ist manchmal möglicherweise nicht verfügbar. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Behebung: Behalten Sie &nbsp; als Leerzeichen bei.
- Entfernen: Papago entfernen, da [der Dienst nicht verfügbar ist](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: Erlauben Sie keinen API-Schlüssel für OpenAI
- UI: Erlauben Sie das Zurücksetzen von Open AI auf die Standardeinstellungen

## 0.3.14

- Abhängigkeit: Upgrade von pdf.js auf die neueste Version
- Behebung: Hintergrundfarbe der PDF-Auswahl
- Behebung: Leerzeichenerkennung

## 0.3.13

- Behebung: E-Book-Builder spezifisches Zeichenproblem, wie einige Kapitelpfade `xxx' xxxx`.
- UI: OpenAI-Benutzerdefinierte Optionen standardmäßig einklappen.
- UI: Exportstatus für EPUB-Export hinzufügen.
- Behebung: GPT4-Standardaufforderung

## 0.3.12

- Feature: Wir können jetzt die Hintergrundfarbe des Markierungsübersetzungsthemas anpassen.
- Behebung: postMessage beim Initialisieren der Seite brach einige Websites, jetzt tun wir dies nur, wenn wir wirklich Seiten übersetzen
- Behebung: E-Book-Fortschrittsproblem.
- Behebung: Besser für das Aufteilen langer Absätze, 1,5 Milliarden, 25,5%, Mr. wird nicht als Grenze betrachtet

## 0.3.11

- Behebung: E-Book-Reader-Dunkelmodus-Textfarbe
- Behebung: OpenAI-Aufforderung

## 0.3.10

- Besser: Erkennung von japanischen/koreanischen Containern.
- Behebung: E-Book-Builder-Fortschritt 99% gestoppt.

## 0.3.9

- Behebung: Options-UI-Schalter Übersetzungsdienste Eingabestatus nicht geändert.

## 0.3.8

- UI: Ladefarbe transparenter
- Behebung: Erkennung der E-Book-Sprache.
- Feature: Übersetzungsfortschritt für E-Book-Builder hinzufügen und ein schönes Konfetti nach dem Erfolg.
- Feature: Alle fehlgeschlagenen Absätze für die Schaltfläche "Erneut versuchen" erneut versuchen.
- Behebung: Deepl-Fehlerbehandlung

## 0.3.7

- Behebung: E-Book-Reader kann keine Bilder in Chrome laden.

## 0.3.6

- UI: Besser für die Erstellung der E-Book-Seiten-UI

## 0.3.5

- Behebung: Benutzerskript-E-Book-Export
- Feature: Benutzerdefinierten API-Endpunkt für OpenAI hinzufügen
- Feature: Temporäre Übersetzungszeitoptionen auf der Website in `Erweiterte Einstellungen` hinzufügen

## 0.3.4

- CI: Build fehlgeschlagen

## 0.3.3

- Behebung: E-Book-Maker für Kindle
- Änderung: Lade-Icon-Farbe, von Schwarz zu Blau, um den Dunkelmodus der Webseite anzupassen.
- Feature: Unterstützung der lokalen HTML-Übersetzung für Erweiterung

## 0.3.2

- Behebung: Optionsformular-Eingabecursor bewegt sich.
- Feature: OpenAI unterstützt benutzerdefinierte apiUrl für Entwicklereinstellungen.

## 0.3.1

- Feature: Dunkles Icon auf Transparenz aktualisieren.
- Behebung: Falsche Reihenfolge für langen Absatz

## 0.3.0

- Version: Ab jetzt werden wir die Nebenversion einmal im Monat ändern, zum Beispiel jetzt im März, wird die Version mit 0.3.0 beginnen, im April wird die Versionsnummer mit 0.3.0 beginnen, im April wird die Versionsnummer mit 0.4.0 beginnen, im nächsten April wird die Versionsnummer 1.4.0 sein, und so weiter. Dies liegt daran, dass es keinen Sinn macht, dass Erweiterungen den Semantiken folgen, aber die Standardisierung der Versionsnummern nach den Gesetzen der Zeit ist Motivation für die Entwicklung, um kontinuierlich zu aktualisieren, und für Benutzer, um Probleme leichter zu finden.
- Feature: Unterstützung des dunklen Icons für Firefox

## 0.2.86

- Option für maximale Textlänge pro Anfrage mit Open AI hinzufügen
- Behebung: E-Book-Identifikator dupliziert
- Feature: Unterstützung der Übersetzung von TXT-Webseiten

## 0.2.85

- Behebung: Einige EPUB-Dateien können nicht gefunden werden.

## 0.2.84

- Feature: Unterstützung von E-Book-Reader und -Maker

## 0.2.83

- Feature: Erlauben Sie die Passwort-Eingabe im Formular, um das Passwort anzuzeigen.

## 0.2.82

- Behebung: Einige Websites verwenden `span` für Stile, daher verwenden wir `font` anstelle von span für den Übersetzungsziel-Wrapper
- Behebung: OpenAI maximale Token-Limit, ändern Sie die maximalen Zeichen von 1500 auf 1300.

## 0.2.81

- Behebung: m.youtube.com
- Behebung: Optionsformular-UI
- Behebung: Open AI-Aufforderung
- Feature: Unterstützung von OpenAI-Multipleschlüsseln, verwenden Sie `,` um sie zu trennen.

## 0.2.80

- Feature: Menü zum Aktivieren/Deaktivieren für Popup -> mehr hinzufügen
- Behebung: DingTalk-Nachrichtenkonflikt

## 0.2.79

- Behebung: Open AI für Leerzeichenabsatz

## 0.2.78

- Feature: Unterstützung von OpenAI CHATGPT 3.5 (unterstützt OpenAI ChatGPT 3.5-Schnittstelle)
- Feature: Neues Thema "Solid Border" hinzufügen (新增新主题，实线边框)

## 0.2.77

- Fix: Mehrere Code-Tag-Fehler.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Fix: Mehrere Code-Tag-Fehler [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Feat: Unterstützung für benutzerdefinierte sofortige Übersetzungstextanzahl für verschiedene Übersetzungsdienste.

## 0.2.74

- Feat: Unterstützung für Tencent (alpha)
- Fix: openai Übersetzung
- Fix: Unbekannte Tags Inline-Überprüfung

## 0.2.73

- Feat: Unterstützung für Grey Translation Theme
- Fix: Github Trending Page

## 0.2.72

- Fix: Firefox Mobile Überprüfungsproblem des Übersetzungsdienstes.

## 0.2.71

- Fix: Open AI Userscript-Berechtigung

## 0.2.70

- Fix: Open AI Platzhalter

## 0.2.69

- Feat: Unterstützung für Open AI als Übersetzungsdienst.
- Feat: Unterstützung für die Überprüfung des Übersetzungsdienstes auf options.html
- Feat: Unterstützung für benutzerdefinierten Hauptframe, da einige Seiten den Body nicht als Hauptframe verwenden

## 0.2.68

- Unterstützung für Caiyun (Alpha)
- Fix unbekannte Block-Tags

## 0.2.67

- Feat: Hinzufügen von `<all>` für immer zu übersetzende Sprachen, sodass Sie jetzt alle Sprachen außer der Zielsprache übersetzen und nie zu übersetzende Sprachen verwenden können
- Fix: Erlauben der Konfiguration benutzerdefinierter Google API
- Besser: Deepl Free Unterstützung
- Fix: Hoher Speicherverbrauch für Userscripts und Erweiterungen (durch Entfernen von opencc zh-CN zu zh-TW, stattdessen mit Google Translate)
- Fix: Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Fix: Azure Übersetzungseinrichtung, aber immer noch angezeigt (muss eingerichtet werden)

## 0.2.66

- Fix: PDF-Datei Übersetzung fehlgeschlagen, Fehler aus 0.2.60 für die Unterstützung von Deepl von zh-CN zu zh-TW

## 0.2.65

- Unterstützung für Drosselungsanfragen für mehrere Frames
- Nicht den Seitentitel übersetzen, wenn im iframe

## 0.2.64

- Fix: openl Auswahl der Übersetzungsdienste
- Feat: Unterstützung für die Option "Titel übersetzen"

## 0.2.63

- Feat: Unterstützung für Azure Übersetzungsdienst
- Feat: Unterstützung für Papago Übersetzungsdienst
- Fix: Native Firefox Android Google Drive Synchronisation.
- Fix: Transparenz von 0.4 auf 0.618 ändern [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Fix: Popup-Shortcuts-Tipps
- Leistung: Serielle zu gleichzeitigen Anfragen
- Besser für die Erkennung der japanischen Anzahl

## 0.2.62

- Feat: Hinzufügen der Regel waitForSelectors, um einige Seiten wie Reddit zu beheben

## 0.2.61

- Fix: Userscript ist zu groß für Greasy Fork
- Besser: Dateigröße reduzieren

## 0.2.60

- Feat: Unterstützung für zh-CN zu zh-TW für Deepl
- Feat: Immersive Translate Deepl Feature
- Feat: Unterstützung für benutzerdefinierte Schriftgröße Zoom
- Fix: Steam-Forum-Stil
- Fix: Globaler Stil nicht geändert, nachdem dynamische Elemente generiert wurden
- Fix: Ausschlusspriorität fördern
- UI: Über-Seite ändern
- Fix: Einige mathematische Elemente bleiben original

## 0.2.59

- Fix: Unbekannte Tags Blockelement
- Fix: translate=no Element überschreiben
- Fix: URL-Abgleich mit mehreren \*

## 0.2.58

- Feat: Unterstützung für benutzerdefinierte Übersetzungstextfarbe, Randfarbe.

## 0.2.57

- Keine Änderungen, neu erstellen

## 0.2.56

- Fix: Doppelte Übersetzung für Inline-Elemente mit Code-Element.
- Fix: Unbekannte Tags Inline/Block-Überprüfung
- Feat: Unterstützung für injiziertes CSS auf Entwicklerboard
- Feat: AuthKey, appid appSecret trimmen
- Besser: Einstellungsseite in neuem Tab öffnen (aber nicht für Stay)

## 0.2.55

- Versuch, Deepl API-Zeichensatz zu beheben

## 0.2.54

- Entfernen der Tabs-Berechtigung für Chrome Store Ablehnung
- Fix: Ganze Seite übersetzen, Fußzeile wird ignoriert
- Notizen zur Über-Seite hinzufügen
- Unterstützung für benutzerdefinierte URL aus eingebauter Konfiguration

## 0.2.53

- Fix: Userscript Google Drive Synchronisationsfehler.

## 0.2.52

### Code

- Verwenden der neuesten esbuild
- Verwenden der neuesten Deno-Version
- CI: Quellcode an Firefox übermitteln

## 0.2.51

- Fix: Google Auth benötigt Anmeldung auf Chrome/Firefox
- Ersetzen der Links des Übersetzungsdienstes
- Besser für Berechtigungen.
- Minify entfernen.

## 0.2.50

- Fix: Google Drive Upload-Problem (wirklich) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Entfernen der Shortcuts alt+d, alt+s, da sie möglicherweise mit nativen Shortcuts in Konflikt stehen.
- Fix: Google Drive Upload-Problem [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Besser für Geschwindigkeit, indem minLength auf 50 für die Spracherkennung gesetzt wird.
- Fix: Google Drive Token validieren.

## 0.2.47

- Fix: Deepl API

## 0.2.46

- Fix: Blockmarkierung

## 0.2.45

- Fix: Element innerText ist undefiniert
- Fix: Caiyun Übersetzung undefinierte Quellsprache

## 0.2.44

- Fix: Userscript Umschaltmaske
- Fix: Umschaltmaskenlogik

## 0.2.43

- Fix: Userscript Umschaltmaske mit Touch-Event.
- Fix: Geschwindigkeit (durch Entfernen von sleep(300))

## 0.2.42

- Fix: Maskenhover, wenn Maske erneut umgeschaltet wird.
- Masken-Shortcuts für Mobilgeräte hinzufügen
- Fix: Userscript Cloud-Synchronisationsproblem
- Erweiterte Optionsseite ins linke Menü verschieben.
- Wiederholungslogik für Übersetzungsdienst hinzufügen

## 0.2.41

- Fix: Userscript Niu Übersetzung
- Fix: XHTML Übersetzung

## 0.2.40

- Fix: Beta-Feature-Anzeige
- Fix: Popup-Einstellungsseite auf neuer Tab-Seite
- Fix: Übersetzungsplatzhalter ersetzen

## 0.2.39

- Unterstützung für Shortcuts zur Anzeige der Maskenübersetzung
- Unterstützung für die Aktivierung von Beta-Features im Entwicklerpanel
- Fix: Shortcuts in mobiler Erweiterung

## 0.2.38

- Unterstützung für Lade-Theme
- Fix: getpocket.com
- Fix: Nebenfußzeile für Körperbereich
- Fix: Import/Export-Symbol

## 0.2.37

- Fix: Frame-Ausschlussmarkierung

## 0.2.36

- Unterstützung für die Synchronisation mit Google Drive

## 0.2.35

- Fix: Japanische rb, rt Tag ignorieren.
- Besser für Popup-UI mehr
- Besser für schlechte Userscript-Tipps
- Beitrag zur Über-Seite hinzufügen
- Fix: Volc Übersetzung für automatische Spracherkennung

## 0.2.34

- Fix: Mehrsprachige Geschwindigkeit

## 0.2.33

- Unterstützung für vertikalen Schreibmodus, wie Japanisch.
- 3 Themes hinzufügen
- Niu Übersetzungsdienst hinzufügen

## 0.2.32

- Fix: PDF-Grundübersetzung
- Fix: Popup wählt einen nicht konfigurierten Dienst aus, geht zur Optionsseite.
- Fix: Bleiben Sie offene Einstellungen.
- Fix: Mehrsprachige Erkennungsgeschwindigkeit

## 0.2.31

- Fix: Dynamisches iframe CSS-Injekt

## 0.2.30

- Unterstützung für Userscript Inline-iframe-Übersetzung.
- Unterstützung für Shadowroot-Übersetzung. Zum Beispiel:
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Gesprächsbereich.
- Auch Synchronisierungsregel im Popup überprüfen

## 0.2.29

- Fix: Facebook Übersetzung
- Unterstützung für die Anzeige der Kontextmenüoption.

## 0.2.28

- Entfernen der nicht standardmäßigen Übereinstimmung für Userscript

## 0.2.27

- Unterstützung für Inline-iframe-Übersetzung. (Nur für Erweiterung, nicht verfügbar für
  Userscript)
- Fix: Mehrsprachige Übersetzung

## 0.2.26

- Fix: Firefox Android Addon
- Erweiterte Einstellungen für Übersetzungsneuzeile hinzufügen

## 0.2.25

- Unterstützung für iframe-Übersetzung, wie QQ Mail, eingebetteter Tweet.

## 0.2.24

- Temporäre Übersetzungsseite für eine Weile hinzufügen
- Fix: stay.app Userscript Browser-API
- Fix: stay.app Optionsseite

## 0.2.23

- Fix: Mehrsprachige Seitenübersetzung

## 0.2.22

- Fix: Userscript-Build

## 0.2.21

- Fix: Firefox Online-PDF-Übersetzung

## 0.2.20

- Fix: Macaque-Anfrageproblem
- Fix: Markieren Sie die Hervorhebungslinie Höhe

## 0.2.19

- Fix: Tencent Smart Japanisch
- Fix: Haikuo World Browser

## 0.2.18

- Fix: Client-URL-Änderung, Übersetzungsstatus automatisch beibehalten.
- Entfernen des Nebencontainers als Übersetzungscontainer.
- Popup-Position umgestalten.

## 0.2.17

- Hervorhebung in Markierung ändern
- Übersetzungsthema "Hervorhebung" hinzufügen

## 0.2.16

- Macaque-Kompatibilität

## 0.2.15

- Fix: Touch-Bounce-Problem

## 0.2.14

- Fix: Safari globalThis.GM funktioniert nicht

## 0.2.13

- Unterstützung für Userscript-Popup-Draging
- Unterstützung für drei Finger auf Touch-Gerät, um Umschaltübersetzungsseiten auszulösen
- Unterstützung für das Ausblenden des Userscript-Popup-Symbols.

## 0.2.12

- Besser für Inoreader

## 0.2.11

- Fix
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas Archiv Der Hauptinhalt der Seite konnte nicht übersetzt werden

## 0.2.10

- Fix: PDF-Zeilenhöhe Abstand

## 0.2.9

- Fix: Ausschlusselemente markieren
- Fix: Deno-Typüberprüfung
- Importmap entfernen
- Fix: Kontextmenüs Übersetzung
- Seite wiederherstellen, wenn diese Seite nie übersetzt wird
- Beschreibung für URL hinzufügen

## 0.2.8

- Erkennung der Benutzeragentensprache für die Schnittstellensprache
- Fix: Zeilenumbruchfehler.

## 0.2.7

- Fix: Grease Monkey Anfrage

## 0.2.6

- Fix
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  Datei-URL-Übereinstimmungsproblem

## 0.2.5

- Version für CI-Test erhöhen

## 0.2.4

- Nachrichtenverbindungsfehler für Popup abfangen.

## 0.2.3

- Behebung von
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  mehrfaches Erstellen von Kontexten

## 0.2.2

- Behebung der PDF-Beispieldatei
- Behebung von Firefox PDF-Lokaldaten
- Behebung von PDF-Verknüpfungen

## 0.2.1

- Unterstützung des Grease Monkey Shortcuts-Managers.
- Behebung des Regex-Abgleichs
- Behebung von YouTube-Kommentaren.
- Behebung der mobilen Reddit-Kompaktversion
- Behebung des Volltext-Übersetzungsproblems

## 0.2.0

- Behebung von PDF mit zwei Spalten.
- Behebung des Chrome/Edge Store Versionsfehlers.
- Behebung von
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Veröffentlichung als Firefox-Addon
- Veröffentlichung für Edge
- Behebung des PDF-Rands.
- Änderung der PDF-Beispieldatei

## 0.0.62

- Behebung des PDF-Formats, Einrückung.
- Behebung der Änderung von telegra.ph-Elementen

## 0.0.61

- Behebung des Schließens von Span-Elementen.
- Behebung der Berechtigung für frühe Browser

## 0.0.60

- Behebung von Chrome PDF

## 0.0.59

- Erste Unterstützung für PDF

## 0.0.58

- Bearbeitung der Übersetzungsthema-Beschreibung

## 0.0.57

- Änderung der Popup-UI für einfachere Nutzung

## 0.0.56

- Behebung des Chrome-Timeouts
- Behebung von Fehlern bei der Satztrennung.

## 0.0.55

- Behebung der Anzeige von Elementen mit "display:none".
- Refactoring der Elementmarkierung

## 0.0.54

- Unterstützung von Zeilenumbrüchen für X Zeichen.

## 0.0.53

- Verwendung von sendMessage anstelle von connect, da Chrome den Port nach
  5 Minuten trennt
- Bessere Erkennung von Textcontainern

## 0.0.52

- Keine Übersetzung von Absätzen, die nur Platzhalterelemente enthalten, z.B.
  [Beispiel](https://github.com/nank1ro/solidart), die erste Zeile.
- Bessere Erkennung von Kindelementen.

## 0.0.51

- Behebung des Cache-Problems
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7)
- Behebung der Schriftgröße der Optionen-UI

## 0.0.50

- Behebung der Übersetzung von blockierten Bildern.

## 0.0.49

- Behebung der Firefox-Erweiterung

## 0.0.48

- Behebung der Chrome-Erweiterung

## 0.0.47

- Umschreiben von Nachrichten mit Hintergrund, Verwendung von connect anstelle von sendMessage
- Hinzufügen von Unterstützung für mobiles Reddit
- Behebung von Leerzeichen in Artikeln

## 0.0.46

- Formatierung der Userscript-Metainformationen

## 0.0.45

- Userscript verwendet eine Datei.
- Hinzufügen eines Timeouts für Cache-Anfragen

## 0.0.44

- Behebung von Fehlern bei der Trennung von Tencent.
- Behebung von Inline-Sup-Element-Fehlern.
- Bessere Unterstützung für Twitter

## 0.0.43

- Behebung von Tweet-BR
- Behebung der globalen Übersetzung.

## 0.0.42

- Behebung des BR-Tags
- Behandlung von Block-Tags nach Regeln

## 0.0.41

- Behebung der Überprüfung von Inline-Elementen
- Hinzufügen einer Entwickler-Debug-Log-Option

## 0.0.39

- Behebung des Übersetzungsdienstes enthält mock2

## 0.0.38

- Unterstützung von Cache-Ergebnissen für Userscript
- Hinzufügen der Optionen-UI
- Unterstützung der Erkennung weiterer Inhaltscontainer

## 0.0.37

- Behebung der Änderung des Popup-Übersetzungsdienstes funktioniert nicht
- Behebung der Übersetzung von Reddit-Mobilinhalten.

## 0.0.36

- Behebung von Wikipedia-Sonderzeichen
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Behebung der Größe des Userscript-Icons.
- Aktivierung aller Websites zur Erkennung der Absatzsprache.

## 0.0.35

- Behebung von YouTube zum nächsten Seite gehen
- Unterstützung der YouTube-Suchseite.
- Behebung des erweiterten Optionsschalters.
- Behebung des img-Tags, verstecktes Tag
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Behebung des erzwungenen Neuladens der Google-Suche
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Unterstützung des Tabellenergebnisses von Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Behebung von Wikipedia-Leerzeichen
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Änderungen

- Die Standard-Hotkey zum Umschalten der Übersetzung wurde auf `alt+A` geändert, da
  es der bequemste Schlüssel zum Tippen ist.

### Sonstiges

- Unterstützung des sofortigen Übersetzungsmodus, damit Sie die Webseite so schnell wie möglich übersetzen lassen können.
- Unterstützung der Festlegung des zu übersetzenden Seitenbereichs, damit Sie mehr Bereiche übersetzen können.
- Unterstützung der Festlegung der ersten x Textanzahl zur sofortigen Übersetzung.
- Behebung der doppelten Übersetzung bei Änderung der Übersetzung
- Bessere Popup-UI

## 0.0.33

- Unterstützung weiterer Sprachen, zh-TW, en

## 0.0.32

- Behebung der Übersetzung lokaler Dateien nach dem Speichern. Behebung
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Hinzufügen der dist-js-Datei zum öffentlichen Repository

## 0.0.31

- Unterstützung der Übersetzung der gesamten Seite
- Unterstützung der sofortigen Übersetzung der Seite
- Mehr Konfigurations-UI
- Reflexion des Themas
- Hinzufügen eines neuen Icons
- Hinzufügen eines neuen Übersetzungsthemas dashedBorder

## 0.0.30

- Bessere Unterstützung für das gestrichelte Thema

## 0.0.29

- Behebung der Gültigkeit von Absätzen.
- Hinzufügen von gepunkteten, dünn gestrichelten Themen
- Bessere Unterstützung für gestrichelte, hervorgehobene Themen

## 0.0.28

- Behebung der Unterstreichung
- Hinzufügen von gestrichelten, Papier-Themen
- Behebung der Erkennung von Headern

## 0.0.27

- Unterstützung des translationTheme

## 0.0.26

- Behebung der Verbindungserlaubnis des volc alpha Userscripts.
- Behebung der Klickbarkeit der Version.

## 0.0.25

- Unterstützung von selectorMatches, sodass wir jetzt alle manstondon abgleichen können.
- Behebung des Firefox-Userscript-Fehlers.

## 0.0.23

- Bessere Erkennung von Chinesisch
- Behebung des Reddit-innerText-Problems

## 0.0.22

- Unterstützung von deeplx
- Behebung mehrfacher Übersetzungen beim Wechsel des Dienstes

## 0.0.21

- Behebung einiger span-Tags als Blockelemente

## 0.0.20

- Unterstützung der Nicht-Übersetzung von Hashtags wie #hash, bei Tags wie @xxx, $tag, wie $APPL
- Unterstützung von Blockelementen

## 0.0.18

- Unterstützung von deepl, bing, baidu, youdao, volc, openl, caiyun.

## 0.0.13

- Unterstützung von Userscript

## 0.0.4.8

- Behebung der Code-Reihenfolge.
- Unterstützung der grundlegenden Popup-UI

## 0.0.4.6

- Unterstützung der Überprüfung neuer Versionen

## 0.0.3

- Unterstützung lokaler Dateien

## 0.0.2

- Unterstützung dynamischer Elemente
- Unterstützung der sichtbaren Übersetzung
