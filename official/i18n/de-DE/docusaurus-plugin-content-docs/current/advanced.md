---
sidebar_position: 4
---

# Erweiterte Anpassungsoptionen

Sie können weitere angepasste Konfigurationen auf der Erweiterten Konfigurationsseite -> Entwicklereinstellungen -> Benutzerkonfiguration bearbeiten, die für fortgeschrittene Benutzer nicht in der Benutzeroberfläche editierbar sind. Siehe die letzte Anmerkung für weitere Details über die Parameter. Die aktuelle integrierte `config` finden Sie [hier](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

## Benutzerregeln

Mit `Regeln` ist es möglich, die Konfiguration einer bestimmten Webseite anzupassen, indem entschieden wird, welcher Inhalt übersetzt werden soll oder nicht, oder indem der Stil der Seiten angepasst wird usw.

```json
[
  {
    "matches": "www.google.com",
    "selectors": [".title"]
  },
  {
    "matches": "*.twitter.com",
    "selectors": [".text"],
    "excludeSelectors": ["nav", " footer"]
  }
]
```

Verwenden Sie `matches`, um die entsprechende Webseite zu finden. Platzhalter sind erlaubt, z.B. `*.google.com`, `www.google.com/test/*`, `file://*`.

Durch die Verwendung von `selectors` wird der intelligente Übersetzungsbereich überschrieben, und es werden nur die Elemente übersetzt, die mit diesem Selektor übereinstimmen.

Verwenden Sie `excludeSelectors`, um Elemente ohne Übersetzung der Position auszuschließen.

Verwenden Sie die `additional`-Selektorgruppe, um den Übersetzungsbereich basierend auf der intelligenten Übersetzung zu erhöhen oder zu verringern.

```json
[
  {
    "matches": "www.google.com",
    "additionalSelectors": [],
    "additionalExcludeSelectors": []
  }
]
```

Wenn die Übersetzung zu verschobenen Seiten, überlappendem Text und anderen Randfällen führt, können Sie `globalStyles` verwenden, um den Seitenstil anzupassen und dies zu beheben. Zum Beispiel der Youtube-Header, der verwendet wird, um die maximale Höhe der Originalseite zu entfernen.

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## Verbesserungen bei der Zusammenführung von Nutzerregeln

Unterstützung ab Version 0.7.4. Nehmen Sie das Überspringen der Nicht-Übersetzungszone als Beispiel

```json
{
  "matches": "https://www.elektrotechnik.rwth-aachen.de/*",
  "additionalExcludeSelectors.remove": [".notranslate", "[translate=no]"]
}
```

Die Operationen Hinzufügen und Entfernen modifizieren die standardmäßig bereitgestellten Regeln und müssen nicht mehr vollständig ersetzt werden, wie es zuvor der Fall war.

## Eingefügtes CSS

Eingefügtes CSS ermöglicht es Ihnen, benutzerdefinierte Webstile global einzufügen. Kann mit `translationClasses` von `Rules` verwendet werden.

```
".immersive-translate-target-wrapper img { width: 16px; height: 16px }"
```

Es ist auch möglich, die Website auf eine persönlichere Weise zu gestalten, wie ein regulärer Webstil-Manager. (sogar unter Verwendung von `display:none`, um Anzeigen zu entfernen)

```css
.title {
  color: red;
}
```

## Benutzerkonfiguration

Die Konfiguration ermöglicht es Ihnen, die Einstellungen dieses Plugins anzupassen, wie zum Beispiel Übersetzungsdienste, sprachspezifische Übersetzungsoptionen usw.

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["*.twitter.com"]
    }
  },
  "translationUrlPattern": {
    "excludeMatches": ["www.google.com"]
  },
  "translationLanguagePattern": {
    "matches": ["en"]
  },
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  },
  "generalRule": {
    "_comment": "",
    "normalizeBody": "",
    "injectedCss": [],
    "additionalInjectedCss": [],
    "wrapperPrefix": "smart",
    "wrapperSuffix": "smart",
    "isPdf": false,
    "isTransformPreTagNewLine": false,
    "urlChangeDelay": 20,
    "isShowUserscriptPagePopup": true,
    "observeUrlChange": true,
    "paragraphMinTextCount": 8,
    "paragraphMinWordCount": 2,
    "blockMinTextCount": 32,
    "blockMinWordCount": 5,
    "containerMinTextCount": 18,
    "lineBreakMaxTextCount": 0,
    "globalAttributes": {},
    "globalStyles": {},
    "selectors": [],
    "preWhitespaceDetectedTags": ["DIV", "SPAN"],
    "stayOriginalSelectors": [],
    "additionalSelectors": [],
    "atomicBlockTags": [],
    "excludeSelectors": [],
    "additionalExcludeSelectors": [],
    "translationClasses": [],
    "excludeTags": [],
    "metaTags": ["META", "SCRIPT", "STYLE", "NOSCRIPT"],
    "additionalExcludeTags": [],
    "stayOriginalTags": ["CODE", "TT", "IMG", "SUP"],
    "additionalStayOriginalTags": [],
    "inlineTags": [],
    "additionalInlineTags": [],
    "extraInlineSelectors": [],
    "additionalInlineSelectors": [],
    "extraBlockSelectors": [],
    "allBlockTags": [],
    "pdfNewParagraphLineHeight": 2.4,
    "pdfNewParagraphIndent": 1.2,
    "pdfNewParagraphIndentRightIndentPx": 130,
    "fingerCountToToggleTranslatePageWhenTouching": 4
  },
  "rules": [
    {
      "matches": "www.google.com",
      "selectors": [".class"]
    }
  ]
}
```

Die Regel-Felder in `rules` können alle Felder in `generalRule` verwenden. Die `rules` haben die höchste Priorität, indem sie das `generalRule` und die Regeln für diese `rule` zusammenführen, wenn eine bestimmte `rule` für eine bestimmte Seite übereinstimmt.

Einführung einiger allgemeiner Felder der Konfiguration.

### Nicht konfigurierte Übersetzungsdienste im Popup-Panel nicht anzeigen

`"showUnconfiguredTranslationServiceInPopup": false`

### Konfiguration von Übersetzungsdiensten

Verwenden Sie `translationService`, um die Standardübersetzungsmaschine auszuwählen, die derzeit unterstützt:

```typescript
| "tencent"
| "google"
| "deepl"
| "baidu"
| "volc"
| "youdao"
| "caiyun"
| "openl"
| "bing"
| "transmart"
```

Verwenden Sie `translationServices`, um den `apikey` jedes Übersetzungsdienstes zu konfigurieren, verschiedene Dienstanbieter benötigen unterschiedliche Parameter, und ihre API-Schlüssel können im Entwicklerzentrum ihrer jeweiligen Websites angefordert werden.

Zum Beispiel, für den Tencent Übersetzer, müssen Sie `secretId`, `secretKey` konfigurieren. Sie können sich zu Tencent Cloud begeben, um einen API-Schlüssel mit 5 Millionen kostenlosen Zeichen pro Monat zu beantragen. Referenz [hier](/docs/services/tencent) für den Bewerbungsprozess.

```json
"translationServices": {
  "tencent": {
    "secretId": "xxx",
    "secretKey": "xxx",
    "matches":["*.twitter.com"],
    "limit": 3,
    "apiUrl":"",
    "maxTextGroupLengthPerRequest": 25,
    "maxTextLengthPerRequest": 1800
  }
}
```

`matches` Feld, verwendet diesen Übersetzungsdienst für eine spezifische Website.

Das `limit` Feld, welches die maximale Anzahl von Anfragen pro Sekunde für diesen Übersetzungsdienst angibt (einige Dienste begrenzen die maximale Anzahl von Anfragen pro Sekunde).

`maxTextGroupLengthPerRequest` Feld, maximale Anzahl von Absätzen pro Anfrage

`maxTextLengthPerRequest` Feld, maximale Anzahl von Zeichen pro Anfrage

`apiUrl` Ermöglicht es Ihnen, die Adresse der Übersetzungs-Schnittstelle anzupassen.

### Immer spezifische Websites übersetzen

`translationUrlPattern` Konfiguriert Websites, die immer übersetzt werden, und Websites, die nie übersetzt werden.

- `matches` Konfiguration übersetzt die Website immer.
- `excludeMatches` Konfiguriert Websites, die nie übersetzt werden.

Konfigurationswerte können Domainnamen oder URLs mit `*` sein, wie zum Beispiel: `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### Immer spezifische Sprachen übersetzen

`translationLanguagePattern` konfiguriert die Sprache, die immer übersetzt wird, und die Sprache, die nie übersetzt wird.

- `matches` Konfiguriert die Sprache, die immer übersetzt wird, z. B. `en`,
- `excludeMatches` Konfiguriert die Sprachen, die nie übersetzt werden.

### Übersetzungsanzeigeformat

`translationTheme` ist das Anzeigeformat der Übersetzung und unterstützt derzeit die folgenden Stile:

```typescript
| "none"
| "gestrichelt"
| "gepunktet"
| "unterstrichen"
| "maske"
| "papier"
| "hervorhebung"
| "zitatblock"
| "abschwächung"
| "kursiv"
| "fett"
| "dünnGestrichelt".
```

Entsprechender deutscher Name:

```json
{
  "none": "keine",
  "gestrichelt": "gestrichelte Unterstreichung",
  "gepunktet": "gepunktete Unterstreichung",
  "unterstrichen": "gerade Unterstreichung",
  "maske": "Unschärfeeffekt",
  "papier": "weißer Papier-Schatteneffekt",
  "hervorhebung": "Hervorhebung",
  "zitatblock": "Zitatstil",
  "abschwächung": "Abschwächung",
  "kursiv": "Kursiv",
  "fett": "Fett",
  "dünnGestrichelt": "dünne gestrichelte Unterstreichung"
}
```

`translationThemePatterns` ermöglicht es Ihnen, verschiedene Übersetzungsstile für verschiedene Websites zu konfigurieren.

```json
"translationThemePatterns": {
  "unterstrichen": {
    "matches": ["discord.com"]
  }
}
```

### Klasse gpt Seitenstrom Nachrichtenübersetzung

```json
{
  "matches": ["chat.openai.com"],
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown ",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

### Regeln

`rules` ist ein Array-Objekt, das es Ihnen ermöglicht, Regeln für spezielle Seiten zu konfigurieren, wie zum Beispiel, dass Twitter nur einen bestimmten Teil einer Region übersetzt:

```json
{
  "rules": [
    {
      "id": "twitter",
      "matches": ["twitter.com", "mobile.twitter.com", "tweetdeck.twitter.com"],
      "selectors": [
        "[data-testid='tweetText']",
        ".tweet-text",
        ".js-quoted-tweet-text",
        "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
        "[data-testid='developerBuiltCardContainer'] > div:nth-child(2)",
        "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)"
      ],
      "extraInlineSelectors": ["[data-testid=\"tweetText\"] div"]
    }
  ]
}
```

Die aktuellen eingebauten `rules` finden Sie [hier](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

Einige der wichtigen Felder sind unten zur Veranschaulichung ausgewählt:

```typescript
export interface Rule {
  // Die Webseite abgleichen
  id?: string; // Jede Anpassungsregel hat ihre eigene ID, wenn Benutzer diese Regel auf dieser Änderung wiederverwenden möchten, müssen sie diese entsprechende ID zu ihrer eigenen Regel hinzufügen, um sie wiederverwenden zu können
  matches?: string | string[]; // Diese Regel wird nur die hier angegebene Webseite abgleichen. Diese Regel wird nur Seiten hier abgleichen.
  excludeMatches?: string | string[]; // Bestimmte Seiten ausschließen.
  selectorMatches?: string | string[]; // Mit einem Selektor abgleichen, ohne alle URLs anzugeben
  excludeSelectorMatches?: string | string[]; // Regeln ausschließen, wie oben.

  // Übersetzungsbereich spezifizieren
  selectors?: string | string[]; // Übersetze nur Elemente, die übereinstimmen
  excludeSelectors?: string | string[]; // Elemente ausschließen, keine Übereinstimmungen übersetzen
  excludeTags?: string | string[]; // Tags ausschließen, keine übereinstimmenden Tags übersetzen

  // Übersetzungsbereiche hinzufügen statt zu überschreiben
  additionalSelectors?: string | string[]; // Übersetzungsbereiche hinzufügen. Übersetzungsorte zu den intelligent übersetzten Bereichen hinzufügen.
  additionalExcludeSelectors?: string | string[]; // Zusätzliche Elemente ausschließen, damit die intelligente Übersetzung spezifische Orte nicht übersetzt.
  additionalExcludeTags?: string | string[]; // Zusätzliche ausschließende Tags

  // So belassen
  stayOriginalSelectors?: string | string[]; // Übereinstimmende Elemente werden so belassen. Wird häufig in Forenseiten-Tags verwendet.
  stayOriginalTags?: string | string[]; // Übereinstimmende Tags werden so belassen, z.B. `code`

  // Block oder Inline
  extraBlockSelectors?: string | string[]; // Zusätzliche Selektoren, passende Elemente werden als Blockelemente behandelt, nicht in eine Zeile übersetzt.
  extraInlineSelectors?: string | string[]; // Zusätzliche Selektoren, die als Inline-Elemente verwendet werden.

  inlineTags?: string | string[]; // Übereinstimmendes Tag wird als Inline-Element verwendet
  preWhitespaceDetectedTags?: string | string[]; // Übereinstimmendes Tag wird automatisch umschlossen

  // Übersetzungsstil
  translationClasses?: string | string | string[]; // Zusätzliche Klassen zur Übersetzung hinzufügen

  // Globale Stile
  globalStyles?: Record<string, string>; // Seitenstile ändern, nützlich, wenn die Übersetzung die Seite durcheinanderbringt.
  globalAttributes?: Record<string, Record<string, string>>; // Attribute von Seitenelementen ändern

  // Eingebettete Stile
  injectedCss?: string | string[]; // CSS-Stile einbetten
  additionalInjectedCss?: string | string[]; // Zusätzliche CSS-Stile, anstatt sie zu überschreiben.

  // Kontext
  wrapperPrefix?: string; // Das Präfix des Übersetzungsbereichs, standardmäßig smart, mit oder ohne Zeilenumbrüche, abhängig von der Anzahl der Zeichen.
  wrapperSuffix?: string; // Suffix des Übersetzungsbereichs

  // Anzahl der Zeichen, um die Übersetzung umzubrechen
  blockMinTextCount?: number; // Mindestanzahl von Zeichen, um die Übersetzung als Block umzubrechen, andernfalls ist die Übersetzung ein Inline-Element.
  blockMinWordCount?: number; // Gleich wie oben. Wenn Sie immer einen Zeilenumbruch möchten, können Sie in beiden 0 einsetzen.

  // Mindestanzahl von Zeichen, die aus dem Inhalt übersetzt werden können
  containerMinTextCount?: number; // Mindestanzahl von Zeichen, die ein Element enthalten sollte, bevor es übersetzt wird, standardmäßig 18
  paragraphMinTextCount?: number; // Mindestanzahl von Zeichen für den Absatz, größer als die Anzahl der Zeichen, die der Inhalt enthalten sollte. number, alles darüber wird übersetzt
  paragraphMinWordCount?: number; // Mindestanzahl von Wörtern im ursprünglichen Absatz

  // Erzwungene Zeilenumbrüche für lange Absätze
  lineBreakMaxTextCount?: number; // Maximale Anzahl von Zeichen im Absatz, um beim Übersetzen eines langen Absatzes einen erzwungenen Umbruch zu erzeugen.

  // Wann mit der Übersetzung begonnen wird.
  urlChangeDelay?: number; // Wie viele Millisekunden die Übersetzung nach dem Betreten der Seite verzögert wird. Um auf die Initialisierung der Seite zu warten, standardmäßig 250ms
  observeUrlChange?: boolean; // Erkennt, wenn sich die URL-Adresse geändert hat und startet die Übersetzung erneut, standardmäßig true.

  // Mobil
  isShowUserscriptPagePopup?: boolean; // Das Seiten-Popup auf mobilen Geräten anzeigen. schwebendes Fenster, standardmäßig true.
  fingerCountToToggleTranslagePageWhenTouching?: number; // Übersetzt, wenn vier Finger berühren, kann auf 0, 2, 3, 4, 5 eingestellt werden

  // AI-Streaming-Übersetzungen
  aiRule: {
    streamingSelector: string; // Selektor zum Markieren des Elements, das auf der GPT-Webseite übersetzt wird
    messageWrapperSelector: string; // Nachrichtenkörper-Selektor
    streamingChange: boolean; // Ob die Nachricht für die GPT-Webseiteniteration inkrementell oder vollständig aktualisiert wird. GPT ist inkrementell
  };
}
```

**Mehr Erklärung**

Unterschied zwischen Block- und Inline-Elementen, wenn Sie mehr wissen möchten, können Sie [hier](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline) sehen.

- Das Blockelement nimmt eine einzelne Zeile ein, und mehrere benachbarte Blockelemente nehmen jeweils eine neue Zeile ein.
- Das Inline-Element nimmt keine einzelne Zeile ein; mehrere benachbarte Inline-Elemente sind auf derselben Zeile angeordnet, und eine neue Zeile wird erst erstellt, wenn eine Zeile zu viele hat.
