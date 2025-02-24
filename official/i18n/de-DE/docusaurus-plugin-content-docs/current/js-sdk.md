---
sidebar_position: 5
---

# JS SDK

Das Immersive Translate JS SDK kann Ihnen helfen, zweisprachige Übersetzungen auf Ihrer Website zu implementieren.

## Wie zu verwenden

> Schalten Sie die Immersive Translate-Erweiterung aus, bevor Sie das JS SDK debuggen

1. Initialisierungsparameter festlegen (Bitte beachten Sie, dass immersiveTranslateConfig nicht gesetzt wird, führt dies zu einem Fehler bei der Initialisierung des JS SDK. Sie können ein leeres Objekt setzen)

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. Fügen Sie den folgenden `script`-Code vor dem `</head>` Ihrer Webseite hinzu

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
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
    <div class=".text">
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

- `pageRule`
  Ermöglicht die benutzerdefinierte Konfiguration der Website, um zu entscheiden, welche Inhalte übersetzt werden sollen oder um das Webseitenlayout anzupassen.
- `isAutoTranslate`
  Sofortige automatische Übersetzung

```html
<script>
  window.immersiveTranslateConfig = {
    isAutoTranslate: true,
    pageRule: {
      selectors: [".text"],
      excludeSelectors: ["nav", "footer"],
    },
  };
</script>
```

Die Verwendung von `selectors` überschreibt den Bereich der intelligenten Übersetzung und übersetzt nur die Elemente, die mit diesem Selektor übereinstimmen.

Mit `excludeSelectors` können Elemente ausgeschlossen werden, die an dieser Stelle nicht übersetzt werden sollen.

Mit `selectors.add` können einige Selektoren zur Standardauswahl hinzugefügt werden.

Mit `selectors.remove` können einige Selektoren aus der Standardauswahl entfernt werden.

Wenn Sie möchten, dass ein Bereich als Ganzes übersetzt wird, ohne die Elemente in Zeilen zu unterteilen, können Sie den `atomicBlockSelectors`-Selektor verwenden. Beachten Sie, dass Sie vor der Verwendung von `atomicBlockSelectors` zuerst `selectors` verwenden müssen.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Weitere Parametererklärungen zu `pageRule`:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Bestimmte Websites ausschließen.
  selectorMatches?: string | string[]; // Mit Selektoren abgleichen, ohne alle URLs anzugeben.
  excludeSelectorMatches?: string | string[]; // Ausschlussregeln, wie oben.


你是一位专业的技术文档翻译专家。  
请将以下 Markdown 内容翻译成 German，并严格遵循以下规则：

1. 保持原有格式：
   - 保持所有 Markdown 语法不变
   - 保留所有代码块和 HTML 标签
   - 保持原有的换行和空格
   - 保持所有链接和 URL 不变
   - 请不要返回 ```markdown 开头和 ``` 结尾的代码块

2. 专业术语：
   - 保持所有技术术语为英文
   - 'Release'、'Preview' 等词保持英文
   - 保持所有版本号和技术规格不变

  // Übersetzungsbereich angeben
  selectors?: string | string[]; // Nur die übereinstimmenden Elemente übersetzen
  excludeSelectors?: string | string[]; // Elemente ausschließen, die übereinstimmenden Elemente nicht übersetzen
  excludeTags?: string | string[]; // Tags ausschließen, die übereinstimmenden Tags nicht übersetzen

  // Übersetzungsbereich hinzufügen, anstatt ihn zu überschreiben
  additionalSelectors?: string | string[]; // Übersetzungsbereich hinzufügen. Im Bereich der intelligenten Übersetzung die Übersetzungsposition hinzufügen.
  additionalExcludeSelectors?: string | string[]; // Zusätzliche Ausschlusselemente, damit die intelligente Übersetzung bestimmte Positionen nicht übersetzt.
  additionalExcludeTags?: string | string[]; // Zusätzliche Ausschluss-Tags

  // Im Originalzustand belassen
  stayOriginalSelectors?: string | string[]; // Übereinstimmende Elemente bleiben im Originalzustand. Häufig verwendet für Tags auf Foren-Websites.
  stayOriginalTags?: string | string[]; // Übereinstimmende Tags bleiben im Originalzustand, z.B. `code`

  // Bereichsübersetzung
  atomicBlockSelectors?: string | string[]; // Bereichsselektoren, übereinstimmende Elemente werden als Ganzes betrachtet und nicht segmentiert übersetzt
  atomicBlockTags?: string | string[]; // Bereichs-Tag-Selektoren, wie oben

  // Block oder Inline
  extraBlockSelectors?: string | string[]; // Zusätzliche Selektoren, übereinstimmende Elemente werden als Block-Elemente betrachtet und beanspruchen eine eigene Zeile.
  extraInlineSelectors?: string | string[]; // Zusätzliche Selektoren, übereinstimmende Elemente werden als Inline-Elemente betrachtet.

  inlineTags?: string | string[]; // Übereinstimmende Tags werden als Inline-Elemente betrachtet
  preWhitespaceDetectedTags?: string | string[]; // Übereinstimmende Tags werden automatisch umgebrochen

  // Übersetzungsstil
  translationClasses?: string | string | string[]; // Zusätzliche Klassen für die Übersetzung hinzufügen

  // Globale Stile
  globalStyles?: Record<string, string>; // Seitenstile ändern, nützlich, wenn die Übersetzung die Seite durcheinander bringt.
  globalAttributes?: Record<string, Record<string, string>>; // Attribute von Seitenelementen ändern

  // Eingebettete Stile
  injectedCss?: string | string[]; // Eingebettete CSS-Stile
  additionalInjectedCss?: string | string[]; // Zusätzliche CSS-Stile hinzufügen, anstatt sie direkt zu überschreiben.

  // Kontext
  wrapperPrefix?: string; // Präfix für den Übersetzungsbereich, standardmäßig smart, je nach Wortanzahl wird entschieden, ob ein Zeilenumbruch erfolgt.
  wrapperSuffix?: string; // Suffix für den Übersetzungsbereich

  // Zeilenumbruchanzahl für Übersetzung
  blockMinTextCount?: number; // Mindestanzahl von Zeichen, um die Übersetzung als Block zu betrachten, andernfalls wird die Übersetzung als Inline-Element betrachtet.
  blockMinWordCount?: number; // Wie oben. Wenn sie immer umgebrochen werden sollen, können beide auf 0 gesetzt werden.

  // Mindestanzahl von Zeichen für übersetzbaren Inhalt
  containerMinTextCount?: number; // Bei intelligenter Erkennung, die Mindestanzahl von Zeichen, die ein Element enthalten muss, um übersetzt zu werden, standardmäßig 18
  paragraphMinTextCount?: number; // Mindestanzahl von Zeichen im Originalabsatz, Inhalte mit mehr Zeichen werden übersetzt
  paragraphMinWordCount?: number; // Mindestanzahl von Wörtern im Originalabsatz

  // Maximale Zeichenanzahl für Zeilenumbruch bei langen Absätzen
  lineBreakMaxTextCount?: number; // Bei der Übersetzung langer Absätze wird die maximale Zeichenanzahl für erzwungene Zeilenumbrüche festgelegt.

```markdown
// Zeitpunkt des Übersetzungsstarts
urlChangeDelay?: number; // Nach dem Betreten der Seite, wie viele Millisekunden Verzögerung, bevor die Übersetzung beginnt. Um die Initialisierung der Webseite abzuwarten, beträgt der Standardwert derzeit 250ms

// AI streaming Übersetzung
aiRule: {
    streamingSelector: string; // Der Selektor, der das zu übersetzende Element auf der gpt-Webseite markiert
    messageWrapperSelector: string; // Selektor für den Nachrichtentext
    streamingChange: boolean; // Ob die wiederholten Nachrichten auf gpt-Webseiten inkrementelle oder vollständige Updates sind. gpt ist inkrementell
};
```