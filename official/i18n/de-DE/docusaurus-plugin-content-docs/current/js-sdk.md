---
sidebar_position: 5
---

# JS SDK

Das Immersive Translate JS SDK hilft Ihnen, zweisprachige Übersetzungen auf Ihrer Website zu implementieren.

## Verwendung

1. Initialisieren Sie Immersive Translate:

```js
<script>
  window.immersiveTranslateConfig = {
    pageRule: {}
  }
</script>
```

2. Fügen Sie den folgenden `script`-Code zu Ihrer Webseite hinzu

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
```

Beispiel

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Immersive Translate JS SDK</title>
    <script>
      window.immersiveTranslateConfig = {
        pageRule: {},
      };
    </script>
    <script
      async
      src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
    ></script>
  </head>

  <body>
    <div>
      <p>
        Night gathers, and now my watch begins. It shall not end until my death.
        I shall take no wife, hold no lands, father no children. I shall wear no
        crowns and win no glory. I shall live and die at my post.
      </p>
    </div>
  </body>
</html>
```

## Parameter

Mit `pageRule` können Sie die Konfiguration der Website anpassen, entscheiden, welche Inhalte übersetzt werden müssen oder die Webseitenstile anpassen.

```js
initImmersiveTranslate({
  pageRule: {
    selectors: [".text"],
    excludeSelectors: ["nav", "footer"],
  },
});
```

Die Verwendung von `selectors` überschreibt den intelligenten Übersetzungsbereich und übersetzt nur Elemente, die mit dem Selektor übereinstimmen.

Die Verwendung von `excludeSelectors` kann Elemente von der Übersetzung ausschließen.

Die Verwendung von `selectors.add` fügt einige Selektoren zu den Standardselektoren hinzu.

Die Verwendung von `selectors.remove` entfernt einige Selektoren von den Standardselektoren.

`pageRule` weitere Parametererklärungen:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Bestimmte Websites ausschließen.
  selectorMatches?: string | string[]; // Mit Selektoren abgleichen, ohne alle URLs anzugeben
  excludeSelectorMatches?: string | string[]; // Ausschlussregeln, wie oben.

  // Übersetzungsbereich angeben
  selectors?: string | string[]; // Nur übereinstimmende Elemente übersetzen
  excludeSelectors?: string | string[]; // Elemente ausschließen, keine übereinstimmenden Elemente übersetzen
  excludeTags?: string | string[]; // Tags ausschließen, keine übereinstimmenden Tags übersetzen

  // Übersetzungsbereich hinzufügen, nicht überschreiben
  additionalSelectors?: string | string[]; // Übersetzungsbereich hinzufügen. Übersetzungspositionen in intelligenten Übersetzungsbereichen hinzufügen.
  additionalExcludeSelectors?: string | string[]; // Ausgeschlossene Elemente hinzufügen, um intelligente Übersetzung an bestimmten Positionen zu verhindern.
  additionalExcludeTags?: string | string[]; // Ausgeschlossene Tags hinzufügen

  // Original beibehalten
  stayOriginalSelectors?: string | string[]; // Übereinstimmende Elemente bleiben original. Häufig für Tags auf Foren-Websites verwendet.
  stayOriginalTags?: string | string[]; // Übereinstimmende Tags bleiben original, wie `code`

  // Block oder Inline
  extraBlockSelectors?: string | string[]; // Zusätzliche Selektoren, übereinstimmende Elemente werden als Blockelemente behandelt, die eine Zeile einnehmen.
  extraInlineSelectors?: string | string[]; // Zusätzliche Selektoren, übereinstimmende Elemente werden als Inline-Elemente behandelt.

  inlineTags?: string | string[]; // Übereinstimmende Tags werden als Inline-Elemente behandelt
  preWhitespaceDetectedTags?: string | string[]; // Übereinstimmende Tags umbrechen automatisch Zeilen

  // Übersetzungsstile
  translationClasses?: string | string | string[]; // Zusätzliche Klassen zur Übersetzung hinzufügen

  // Globale Stile
  globalStyles?: Record<string, string>; // Seitenstile ändern, nützlich, wenn Übersetzungen Seitenstörungen verursachen.
  globalAttributes?: Record<string, Record<string, string>>; // Attribute von Seitenelementen ändern

  // Eingebettete Stile
  injectedCss?: string | string[]; // CSS-Stile einbetten
  additionalInjectedCss?: string | string[]; // CSS-Stile hinzufügen, anstatt direkt zu überschreiben.

  // Kontext
  wrapperPrefix?: string; // Präfix des Übersetzungsbereichs, Standard ist intelligent, entscheidet, ob Zeilen basierend auf der Anzahl der Zeichen umbrochen werden.
  wrapperSuffix?: string; // Suffix des Übersetzungsbereichs

  // Übersetzungsumbruch-Zeichenanzahl
  blockMinTextCount?: number; // Minimale Zeichenanzahl für die Übersetzung als Block, andernfalls wird die Übersetzung ein Inline-Element sein.
  blockMinWordCount?: number; // Wie oben. Um immer Zeilen umzubrechen, setzen Sie beide auf 0.

  // Minimale Zeichenanzahl für übersetzbare Inhalte
  containerMinTextCount?: number; // Minimale Zeichenanzahl für Elemente, die während der intelligenten Erkennung übersetzt werden sollen, Standard ist 18
  paragraphMinTextCount?: number; // Minimale Zeichenanzahl für den Originalabsatz, Inhalte, die größer als die Anzahl sind, werden übersetzt
  paragraphMinWordCount?: number; // Minimale Wortanzahl für den Originalabsatz

  // Erzwungene Zeilenumbruch-Zeichenanzahl für lange Absätze
  lineBreakMaxTextCount?: number; // Maximale Zeichenanzahl für erzwungenen Zeilenumbruch bei der Übersetzung langer Absätze.

  // Zeitpunkt des Übersetzungsbeginns
  urlChangeDelay?: number; // Verzögerung in Millisekunden, bevor die Übersetzung nach dem Betreten der Seite beginnt. Standard ist 250ms, um auf die Initialisierung der Webseite zu warten.

  // AI-Streaming-Übersetzung
  aiRule: {
    streamingSelector: string; // GPT-Webseiten-Selektor, der das übersetzende Element markiert
    messageWrapperSelector: string; // Nachrichtenkörper-Selektor
    streamingChange: boolean; // Inkrementelle oder vollständige Aktualisierung für wiederholte Nachrichten auf GPT-ähnlichen Webseiten. GPT ist inkrementell
  };
}
```
