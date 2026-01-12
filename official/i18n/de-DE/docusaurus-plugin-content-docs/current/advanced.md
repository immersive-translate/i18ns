---
sidebar_position: 4
---

# Erweiterte Anpassungsoptionen

Diese Seite richtet sich an fortgeschrittene Nutzer*innen mit Grundkenntnissen in HTML/CSS/JSON. Erweiterte Konfigurationsmöglichkeiten bieten deutlich mehr Anpassungsfähigkeit, erhöhen aber auch die Gefahr, scheinbar korrekte, aber tatsächlich unwirksame Einstellungen zu erstellen. Es wird empfohlen, vor Änderungen ein Backup anzulegen.

## Hinweise vor der Benutzung

- Der Einstiegspunkt ist in den [Entwicklereinstellungen](https://dash.immersivetranslate.com/#developer).
- Vor dem Bearbeiten bitte unbedingt ein Backup der User Config / User Rules anlegen, um zu verhindern, dass Konfigurationsfehler ignoriert werden.
- Die endgültige Built-in-Konfiguration findest du unter "Click to expand the final config" (enthält alle Felder, Defaultwerte, verfügbare Dienste).

## Einstiegspunkte und Priorität

Typische Einstiegspunkte (Entwicklereinstellungen):
- Edit Full User Config: Gesamte Konfiguration (inkl. `rules`, Übersetzungsdienste, Styles usw.)
- Edit User Rules: Bearbeite nur das `rules`-Array (an dieser Stelle nur Array, schreibe nicht `{ "rules": [...] }`).
- Injected CSS: Globale CSS-Injektion.

Prioritätsreihenfolge (von hoch nach niedrig): Treffer in `rules` > `generalRule` > Built-in Default.
Wenn eine spezifische `rule` greift, wird sie mit `generalRule` gemerged, Felder der `rule` haben Vorrang.

## Schnellstart (häufigste Anforderungen)

### 1) Nur den Hauptinhalt einer Webseite übersetzen

```json
{
  "rules": [
    {
      "matches": ["example.com"],
      "selectors": ["article", ".post-content"],
      "excludeSelectors": ["nav", "footer", ".comment"]
    }
  ]
}
```

### 2) Immer übersetzen / nie übersetzen

```json
{
  "translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
  }
}
```

### 3) Verschiedene Dienste pro Website nutzen

```json
{
  "translationService": "google",
  "translationServices": {
    "deepl": {
      "matches": ["sci-hub.se"]
    }
  }
}
```

### 4) Übersetzungsstil pro Website differenzieren

```json
{
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  }
}
```

### 5) Style-Probleme durch Übersetzungen beheben

```json
{
  "rules": [
    {
      "matches": ["youtube.com"],
      "globalStyles": {
        "#video-title": "max-height:unset;"
      }
    }
  ]
}
```

### 6) Unkonfigurierte Übersetzungsdienste im Popup ausblenden

```json
{
  "showUnconfiguredTranslationServiceInPopup": false
}
```

## Regeln & Matching

### Regel-Merging

- `generalRule`: Globale Baseline für alle Websites.
- `rules`: Website-spezifische Regeln, haben höchste Priorität, sobald sie greifen.

Die Felder in `rules` können meist ebenso in `generalRule` verwendet werden.

### Typische Formen von matches

`matches` unterstützt String oder Array:
- Domain: `example.com`
- Volle URL: `https://example.com/path/`
- Wildcard: `https://*/*q=*`
- Alles matchen: `*` / `*://*` / `*://*/*`
- Lokale Datei: `file://*`

Achtung: `*.twitter.com` matcht nur Subdomains, nicht das Root-Domain `twitter.com`.

### selectors / excludeSelectors

- `selectors`: Es werden nur die gematchten Elemente übersetzt (überschreibt die Standardbereiche!).
- `excludeSelectors`: Elemente, die von der Übersetzung ausgeschlossen werden.

Wenn du im ursprünglichen Bereich nur hinzufügen/entfernen möchtest, nutze am besten `.add` / `.remove` (siehe nächster Abschnitt).

### Vererbung & inkrementelle Änderungen (.add / .remove)

Für Array- oder Objektfelder sind `.add` / `.remove` zur inkrementellen Anpassung möglich.
Damit überschreibst du nicht direkt die Defaultwerte, sondern ergänzt oder entfernst gezielt:

```json
[
  {
    "id": "twitter",
    "selectors.add": ["[data-testid='tweetText'] a"],
    "excludeSelectors.add": ["header"]
  }
]
```

### Häufig genutzte Felder (Auswahl)

Matching:
- `matches` / `excludeMatches`
- `selectorMatches` / `excludeSelectorMatches`

Übersetzungsbereich:
- `selectors` / `excludeSelectors` / `excludeTags`
- `stayOriginalSelectors` / `stayOriginalTags`
- `extraInlineSelectors` / `extraBlockSelectors`

Styles & Layout:
- `translationClasses`: Füge zusätzliche CSS-Klasse zu Übersetzungen hinzu
- `globalStyles` / `globalAttributes`
- `injectedCss` / `additionalInjectedCss`
- `wrapperPrefix` / `wrapperSuffix`
- `blockMinTextCount` / `blockMinWordCount`

Timing & Mobile:
- `urlChangeDelay` / `observeUrlChange`
- `isShowUserscriptPagePopup`

### GPT-artige Streamnachrichten-Übersetzung

```json
{
  "matches": ["chat.openai.com"],
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

Weitere Felder siehe Anhang: "Rule Feldreferenz" am Ende dieses Dokuments.

## matches Match-Logik (Kurzfassung)

- Nur Domain (kein `*` und kein Pfad): Vergleicht nur hostname.
- Volle URL (ohne `*`): Protokoll + Host + Port + Pfad exakter Vergleich.
- Mit `*` oder fehlendem Protokoll: Wildcard-Matching (Standardmäßig http/https/file).

Typische Beispiele:
- `twitter.com` ✅ trifft auf `https://twitter.com/home`
- `*.twitter.com` ✅ trifft auf `https://mobile.twitter.com`, ❌ nicht auf `https://twitter.com`
- `https://twitter.com/home` trifft nur bei genau übereinstimmender URL
- `twitter.com/*` matcht alle Pfade unter `twitter.com`

## Beispiel für Website-Anpassung (Twitter)

Nachfolgend ein Auszug aus der Built-in Twitter-Regel, um typische Verwendung von `selectors` / `excludeSelectors` / `globalStyles` zu zeigen:

```json
[
  {
    "id": "twitter",
    "matches": [
      "twitter.com",
      "mobile.twitter.com",
      "tweetdeck.twitter.com",
      "pro.twitter.com",
      "https://platform.twitter.com/embed*"
    ],
    "selectors": [
      "[data-testid=\"tweetText\"]",
      ".tweet-text",
      ".js-quoted-tweet-text",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
      "[data-testid='developerBuiltCardContainer'] > div:nth-child(2)",
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)",
      "[data-testid='cellInnerDiv'] div[data-testid='UserCell'] > div> div:nth-child(2)",
      "[data-testid='UserDescription']",
      "[data-testid='HoverCard'] div[dir=auto]",
      "[data-testid='HoverCard'] span[dir=auto]",
      "[data-testid='HoverCard'] [role='dialog'] div[dir=ltr]",
      "[data-testid='birdwatch-pivot'] div[dir=ltr]"
    ],
    "excludeSelectors": [
      "[aria-describedby][role=button]",
      "header",
      "[data-testid='radioGroupplayback_rate'] div",
      "[data-testid='userFollowIndicator']",
      "[class='css-901oao r-14j79pv r-37j5jr r-n6v787 r-16dba41 r-1cwl3u0 r-bcqeeo r-qvutc0']",
      "[class='css-175oi2r r-1wbh5a2 r-dnmrzs']"
    ],
    "globalStyles": {
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  }
]
```

- `selectors`: Übersetze nur den eigentlichen Tweet-Text, keine Nutzernamen/Buttons.
  ![tweet](https://s.immersivetranslate.com/assets/r2-uploads/tweet.png)
- `excludeSelectors`: Schließt Buttons, Navigation und andere interaktive Elemente aus.
  ![twitter-follow](https://s.immersivetranslate.com/assets/r2-uploads/twitter-follow.png)
- `globalStyles`: Entfernt die Zeilen-Limitierung auf Twitter, damit Übersetzungen nicht abgeschnitten werden.
  ![用户主页](https://s.immersivetranslate.com/assets/r2-uploads/twitterUser.png)

## Eigene Website-Anpassungen

Du kannst mit `id` auf die Built-in-Regeln aufbauen und mit `.add/.remove` inkrementelle Änderungen machen:

```json
[
  {
    "id": "twitter",
    "selectors.remove": ["[data-testid=\"tweetText\"]"],
    "selectors.add": ["[data-testid=\"tweetText\"] a"],
    "excludeSelectors.add": ["header"],
    "excludeSelectors.remove": []
  }
]
```

Erläuterung:
- `id` kann eine Built-in-Regel erben, so sparst du dir das erneute Schreiben von `matches`.
- `.add/.remove` ist für Arrayfelder empfohlen, damit du Defaultwerte nicht komplett überschreibst.

Übliche Built-in-IDs (Auswahl):
- `isEbook`: ePub-Reader-Seite
- `isEbookBuilder`: Seite zum Generieren eines zweisprachigen ePub
- `pdf`: PDF-Zweisprachenansicht

Alle Built-in-Regeln:
- `https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json`

## Konfiguration von Übersetzungsdiensten

- `translationService`: Standard-Übersetzungsdienst.
- `translationServices`: Dienstkonfiguration und Matching pro Site.
- `showUnconfiguredTranslationServiceInPopup`: Nicht konfigurierte Dienste im Popup ausblenden.

Beispiel (Tencent):

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["twitter.com"],
      "limit": 3,
      "maxTextGroupLengthPerRequest": 25,
      "maxTextLengthPerRequest": 1800,
      "apiUrl": ""
    }
  }
}
```

Hinweis:
- `matches` gibt an, wo dieser Dienst eingesetzt wird.
- `limit` ist das Request-Limit (Requests/Sekunde).
- `maxTextGroupLengthPerRequest` / `maxTextLengthPerRequest` begrenzen die Größe einer Anfrage.
- `apiUrl` für eigene Endpunkte.

### Timeout für Anfragen (Maximale Anfragedauer)

Timeout kann pro Dienst eingestellt werden, in Millisekunden (ms). Bei Pro-Diensten kann separat `proRequestTimeout` gesetzt werden.

```json
{
  "translationServices": {
    "openai": {
      "requestTimeout": 60000
    },
    "gemini": {
      "proRequestTimeout": 90000
    }
  }
}
```

Hinweise:
- Zu hohe Timeouts = längere Wartezeiten. Zu kurz = viele Fehler durch Timeout.
- Defaultwerte sind je nach Dienst unterschiedlich, siehe finale Konfiguration.
- `proRequestTimeout` greift nur bei `provider` = `pro` (Premiumdienst).

## Sprachen und Übersetzungsstrategie

### Immer / nie bestimmte Sprache übersetzen

```json
{
  "translationLanguagePattern": {
    "matches": ["en"],
    "excludeMatches": ["zh"]
  }
}
```

### Quellsprache für bestimmte Websites setzen

```json
{
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  }
}
```

## Weitere häufige Globaleinstellungen

### Rendering von HTML-Tag in Übersetzung erlauben

Wenn du möchtest, dass HTML-Tags in der Übersetzung gerendert werden, aktiviere dies:

```json
{
  "enableRenderHtmlTag": true
}
```

## Übersetzungsstil & Themes

`translationTheme` unterstützt folgende Styles (siehe finale Config für Updates):

```text
none, grey, dashed, dashedBorder, solidBorder, dotted, underline, mask, opacity,
paper, dividingLine, highlight, marker, marker2, blockquote, weakening, italic,
bold, thinDashed, nativeDotted, wavy, nativeDashed, nativeUnderline, background
```

Styles nach Website setzen:

```json
{
  "translationThemePatterns": {
    "highlight": {
      "matches": ["discord.com"]
    }
  }
}
```

## AI- & Advanced-Parameter

### temperature (z.B. bei GPT)

```json
{
  "translationServices": {
    "openai": {
      "temperature": 0.2
    }
  }
}
```

### Eigene Header und Body für Requests setzen

```json
{
  "translationServices": {
    "claude": {
      "headerConfigs": {
        "anthropic-version": "2023-06-01",
        "anthropic-dangerous-direct-browser-access": "true"
      },
      "bodyConfigs": {
        "max_tokens": 2048
      }
    }
  }
}
```

### Spezielle Gemini Model-Konfiguration

Da Gemini-Modelle Default-Werte haben, überschreibst du deren Einstellugen am besten gezielt mit `modelsOverrides`:

```json
{
  "translationServices": {
    "gemini": {
      "modelsOverrides": [
        {
          "models": ["gemini-2.5-flash", "gemini-2.5-flash-lite"],
          "bodyConfigs": {
            "temperature": 0.1
          }
        }
      ]
    }
  }
}
```

Hinweis: `modelsOverrides` gilt auch für andere AI-Dienste und überschreibt gezielt Einstellungen für die genannten Modelle.

### Striktes Einhalten von Prompts

> Um Halluzinationen bei LLM-Modellen zu reduzieren, prüft das Plugin die Token-Relation zwischen Anfrage und Antwort. Ein zu hohes oder zu niedriges Verhältnis gilt als ungültig, Ergebnis wird verworfen, Backup-Dienst übernimmt.
> Solltest du den Prompt zweckentfremden (z.B. für Textverbesserung, nicht reine Übersetzung), könnten die Token-Relationen untypisch sein. Nutze dann `strictPrompt: true` für strikten Modus und überspringe die Prüfung.

```json
{
  "translationServices": {
    "claude": {
      "strictPrompt": true
    }
  }
}
```

### Eigene Prompt-Überschreibungen (Beispiel)

```json
{
  "translationServices": {
    "openai": {
      "langOverrides": [
        {
          "id": "auto2ja",
          "systemPrompt": "あなたはプロの翻訳エンジンです。",
          "prompt": "次のテキストを{{to}}に翻訳してください：\n\n<text>\n{{text}}\n</text>",
          "multiplePrompt": "<yaml>\n{{yaml}}\n</yaml>",
          "subtitlePrompt": "<yaml_subtitles>\n{{yaml}}\n</yaml_subtitles>"
        }
      ]
    }
  }
}
```

## Terminologie & Machine Translation

Aktuell wird die [AI-Terminologiefunktion](https://dash.immersivetranslate.com/#terms) nur für AI-Übersetzungsdienste unterstützt.

Machine Translation nutzt die Terminologie-DB standardmäßig nicht (würde meist per Platzhalter ersetzen und die Qualität verschlechtern). Erzwingen kannst du es (nicht empfohlen) mit:

```json
{
  "enableMachineTranslateTerms": true
}
```

## Cache-Leerungs-Intervall

Das Plugin leert standardmäßig alle 30 Tage den Übersetzungs-Cache automatisch, damit die Performance nicht leidet.

```json
{
  "cacheMaxAgeDay": 30
}
```

## Injected CSS vs. globalStyles

- Injected CSS: globale Style-Korrekturen pro Seite.
- globalStyles: Regelbasierte Style-Overrides für bestimmte Websites.

Injected CSS Beispiel:

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

## Fehlerbehebung & Stolperfallen

- `*.twitter.com` beinhaltet _nicht_ das Root-Domain, nutze zusätzlich `twitter.com`.
- `selectors` überschreibt den Default-Bereich, nutze `.add/.remove` für Ergänzungen!
- `matches` mit `/path` wird als Wildcard behandelt — prüfe, ob du explizit eine volle URL matchen willst.
- Wenn Config nicht greift: Im Resultat-Konfig nachschauen und Seite neu laden.
- Ein Komma am Ende von JSON-Listen führt zu Ignorierung der Config.

## Anhang: Rule Feldreferenz

Im Folgenden die Rule-Felder im Überblick (detaillierte/documented Version). Für alle Felder/neueste Änderungen siehe immer die finale Konfiguration.
Hinweis: Mit `.add` / `.remove` für Array/Objektfelder kannst du Defaults inkrementell ändern, ohne sie komplett zu überschreiben.

```typescript
export interface Rule {
  // Webseiten-Matching
  id?: string; // Built-in Rule-ID, zum Vererben von Regeln
  matches?: string | string[]; // Diese Regel greift nur für folgende Websites
  excludeMatches?: string | string[]; // Speziell auszuschließende Sites
  selectorMatches?: string | string[]; // CSS-Selektor-Matching, unabhängig von URLs
  excludeSelectorMatches?: string | string[]; // Ausschluss analog

  // Übersetzungsbereich spezifizieren
  selectors?: string | string[]; // Nur Elemente mit diesem Selektor übersetzen
  excludeSelectors?: string | string[]; // Übersetze diese Elemente NICHT
  excludeTags?: string | string[]; // Bestimmte HTML-Tags ausschließen

  // Zusätzliche Elemente (falls nicht mit .add / .remove lösbar)
  additionalSelectors?: string | string[]; // Zusätzliche Bereiche übersetzen
  additionalExcludeSelectors?: string | string[]; // Zusatz-Ausschlüsse
  additionalExcludeTags?: string | string[]; // Zusatz-Tags ausschließen (ggf. veraltet)

  // Im Original belassen
  stayOriginalSelectors?: string | string[]; // Bleibt unübersetzt
  stayOriginalTags?: string | string[]; // Bestimmte Tags bleiben unübersetzt (z.B. <code>)

  // Block oder Inline
  extraBlockSelectors?: string | string[]; // Diese Elemente gelten als Block
  extraInlineSelectors?: string | string[]; // Diese Elemente gelten als Inline
  inlineTags?: string | string[]; // Diese Tags gelten als Inline
  preWhitespaceDetectedTags?: string | string[]; // Bei diesen Tags automatische Zeilenumbrüche

  // Übersetzungs-Stile
  translationClasses?: string | string[]; // Zusätzliche Klasse für Übersetzungen

  // Globale Styles
  globalStyles?: Record<string, string>; // Überschreibe CSS auf Seite
  globalAttributes?: Record<string, Record<string, string | null>>; // Attribute für ausgewählte Elemente

  // Eingebettete Styles
  injectedCss?: string | string[]; // CSS-Injektion
  additionalInjectedCss?: string | string[]; // Zusätzliches CSS injizieren

  // Kontext
  wrapperPrefix?: string; // Text vor Übersetzung (z.B. für Labels)
  wrapperSuffix?: string; // Text nach Übersetzung

  // Umbruch/Zählung
  blockMinTextCount?: number; // Minimum Textlänge für Blockübersetzung (Zeichen)
  blockMinWordCount?: number; // Minimum Wortanzahl als Block

  // Mindestlänge für Übersetzung
  containerMinTextCount?: number; // Mindestzeichen in einem Element für Übersetzung
  paragraphMinTextCount?: number; // Mindestzeichen im Absatz
  paragraphMinWordCount?: number; // Mindestwörter im Absatz

  // Zeilenumbruch bei langen Absätzen
  lineBreakMaxTextCount?: number; // Maximal-Zeichen vor Zeilenumbruch

  // Übersetzungszeitpunkt
  urlChangeDelay?: number; // Verzögerung nach Seitenaufruf (ms)
  observeUrlChange?: boolean; // Übersetze erneut bei URL-Änderung

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Floating Popup auf Mobilgeräten anzeigen
  fingerCountToToggleTranslagePageWhenTouching?: number; // Veraltet

  // AI-Streaming Unterstützung
  aiRule?: {
    streamingSelector: string; // Selektor für zu übersetzende Stream-Elemente
    messageWrapperSelector: string; // Selektor für Nachrichtenkörper
    streamingChange: boolean; // Inkremmentelles Update aktivieren
  };
}
```
