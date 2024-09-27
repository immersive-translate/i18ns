---
sidebar_position: 4
---

# PDF Hilfe

Immersive Translate PDF Bilingual Reader ist ein zweisprachiges, kreuzreferenziertes Echtzeit-Übersetzungstool, das als Lesehilfe verwendet werden kann.

Derzeit können Sonderzeichen wie mathematische Formeln, Tabellen usw. aufgrund der Technik zur Erkennung von Klartext nicht korrekt verarbeitet werden.

Wenn Ihr PDF Tabellen und mathematische Formeln enthält, es höhere Qualitätsanforderungen an deren Übersetzung gibt und Sie über einige Programmierkenntnisse verfügen, wird empfohlen, sich auf diesen [Nouga-OCR + Immersive Translate](https://app.immersivetranslate.com/pdf-pro/) Artikel zu beziehen.

Siehe [Dokumentation hier](/docs/usage/#pdf-file-translation) für grundlegende Nutzungsfagen.

Hier sind einige fortgeschrittene Tipps zur PDF-Übersetzung:

### Bearbeitungsfeld

Die Standardübersetzung ist bearbeitbar. Sie können sogar auf "Originaltext anzeigen" im Panel klicken, und der Inhalt des Textfeldes wird als der intelligent erkannte Originaltext angezeigt, und Sie können zu diesem Zeitpunkt Korrekturen am Originaltext im Bearbeitungsfeld vornehmen. Dann klicken Sie erneut auf die Panelübersetzung.

### Textfelder verschieben

Wenn einige Absätze an einer falschen Position erkannt werden, können Sie die Position des gesamten Absatz-Bearbeitungsfeldes verschieben, indem Sie die Maus in die obere linke Ecke setzen. (Wenn Sie auf eine Situation stoßen, in der Sie nicht ziehen können, können Sie hineinzoomen und die untere rechte Ecke nach unten ziehen, und die obere linke Ecke wird sich normal bewegen.)

### Textfeld löschen

Wenn einige Absätze Erkennungsprobleme haben könnten, manuell den vorherigen Absatz zusammenführen, könnte dieser Absatz überflüssig sein, in diesem Fall können Sie diesen Knopf klicken, um ihn zu löschen!

### Größenanpassung des Textfeldes

Da die Standardübersetzungshöhe und -breite standardmäßig dieselben wie beim ursprünglichen Absatz sind, kommt es zu einem Überlauf, wenn der Übersetzungsinhalt den ursprünglichen Text überschreitet. In diesem Fall können Sie ihn durch das innere Scrollen betrachten. Sie können auch in der unteren rechten Ecke ziehen und ablegen, um dieses Textfeld angemessen zu vergrößern, damit der Inhalt vollständig angezeigt werden kann.

### Bandwagen-Modus

Standardmäßig wird das Bild des ursprünglichen Textes in den übersetzten Bereich rechts wiederhergestellt. Es ist normal, einen weißen Hintergrundrahmen für den übersetzten Text zu sehen, da es notwendig ist, den ursprünglichen Text, der mit Canvas gezeichnet wurde, zu überdecken, damit der übersetzte Text ordnungsgemäß angezeigt werden kann.

Wenn Sie feststellen, dass der Unterlagemodus Ihre Lesbarkeit beeinträchtigt, schalten Sie ihn einfach aus.

### Überlappungsgrenze

Da wir so weit wie möglich versuchen, den ursprünglichen typografischen Effekt wiederherzustellen, ist die Ausgangsposition des Absatzes die Koordinate der oberen linken Ecke des ursprünglichen Absatzes. Unter normalen Umständen wird bei der Übersetzung von Englisch nach Chinesisch der chinesische Inhalt im Allgemeinen kleiner als der englische sein, sodass die Übersetzung vollständig dargestellt werden kann. Dies tritt auf, wenn der übersetzte Text in einigen Fällen mit dem ursprünglichen Text redundant ist. Um dies zu vermeiden, haben wir der Übersetzung eine Höhe gegeben, die der des ursprünglichen Absatzes entspricht.

Dies kann ausgeschaltet werden, wenn wir das Gefühl haben, dass der Abstand zwischen den oberen und unteren Absätzen ausreichend für die Präsentation des überschreitenden Teils der Übersetzung ist.

### Eng gesetzt

Dieses Ziel ist tatsächlich ähnlich wie das oben genannte, da es einen bestimmten Abstand zwischen jeder Textzeile gibt, um die Lesbarkeit des übersetzten Textes zu gewährleisten.

Wenn der Bildschirm klein ist und der Abstand zwischen den oberen und unteren Absätzen möglicherweise nicht ausreicht, um den Überlauf des übersetzten Textes anzuzeigen, können Sie diesen Punkt aktivieren und den Textzeilenabstand entfernen, sodass der Text der Absätze vollständig angezeigt werden kann.

### Absatzeinzüge

Aufgrund der Komplexität verschiedener PDF-Layouts können Absatzeinzüge nicht immer intelligent als solche erkannt werden. Fehlt der Einzug, könnte es schwierig werden, den Artikel flüssig zu lesen. Für diesen Typ von Absatz können Benutzer eine Funktion aktivieren, die den ersten Zeileneinzug jedes Absatzes hinzufügt, um dies zu verdeutlichen.

### Großer Zeilenabstand und nicht erkannte Absätze

Einige PDFs haben möglicherweise aus Darstellungsgründen einen relativ großen Absatzabstand, was bei der intelligenten Erkennung dazu führen kann, dass Sätze als eigenständige Absätze interpretiert werden. In solchen Fällen sollte der Abstand angemessen angepasst werden, beispielsweise auf 10px, um die Absätze auf der Seite neu zu erkennen.

### Anpassung der horizontalen Position von Übersetzungen

Da die horizontalen Koordinaten des übersetzten Textes aus den Original-PDF-Daten gelesen werden, können einige der horizontalen Koordinaten im PDF groß sein. In diesem Fall können Sie den übersetzten Inhalt nach links verschieben, indem Sie den Fortschrittsbalken ziehen.

### Anpassung der Skalierung von Übersetzungen

Die Größe des übersetzten Textes entspricht grundsätzlich der des Originaltextes. Wenn Sie jedoch das Gefühl haben, dass die Größe des übersetzten Textes nicht angemessen ist, können Sie den Fortschrittsbalken ziehen, um die Schriftgröße entsprechend dem Verhältnis anzupassen.

## Manuelle Anpassung von Fehlersegmenten

Wenn der intelligent erkannte Absatz falsch ist, kann er mit den folgenden Schritten manuell angepasst werden:

- Klicken Sie auf das Übersetzungsfeld, um den erkannten Originaltext anzuzeigen.
- Passen Sie dann manuell den Absatz gegenüber dem Originaltext auf der linken Seite durch Kopieren und Zeilenumbrüche usw. an.
- Wenn der Absatz als korrekt bestätigt wird, klicken Sie erneut auf Übersetzen.

Da unser Werkzeug auf dem Browser basiert, sind Download-Geschwindigkeiten und -Ergebnisse stark vom Browser selbst abhängig. Daher wird empfohlen, nicht mit mehr als 300 Seiten PDF umzugehen.

### Übersetzung herunterladen (Drucken)

Diese Funktion lädt nur Übersetzungen herunter, nicht zweisprachig.
Wenn die Standardübersetzung angezeigt wird, ist der Zoommodus auf Seitenbreite für den Leseffekt eingestellt.

Es wird jedoch empfohlen, den Zoommodus anzupassen, wenn Sie drucken und Zeit sparen möchten. Es wird allgemein empfohlen, auf 100 Prozent oder die tatsächliche Größe einzustellen, da der Druckeffekt besser sein wird.

### Zweisprachige Bewahrung

Aufgrund technischer Einschränkungen bei den Effekten der zweisprachigen Bewahrung werden Übersetzungen in Form von Bildern bewahrt, was die WYSIWYG-Bewahrung von Online-Übersetzungseffekten ermöglicht. Es dauert etwa 5/6 Minuten, um 300 Seiten PDF zu exportieren.

## Andere Situationen

### Unübersetzbar

- Überprüfen Sie, ob der ursprüngliche Text auf der linken Seite kopiert werden kann. Wenn er nicht kopiert werden kann, wird bewiesen, dass es sich um ein Bild-PDF handelt, die aktuelle vorübergehende Unterstützung für die Bild-PDF-Übersetzung
- Überprüfen Sie, dass die Übersetzung erkannt, aber nicht übersetzt wird, dass 🔄❓ nicht am Ende des Absatzes erscheint und dass die Schaltfläche im Panel des Plug-ins "Übersetzen" anzeigt. Klicken Sie in diesem Fall auf die Schaltfläche übersetzen, um die Übersetzung auszulösen.
- Wenn 🔄❓ existiert, klicken Sie unter ❓, um die Fehlermeldung zu sehen

### Mail-Feedback-Dokument

Sie können eine Beschreibung Ihres Problems + einen Screenshot mit dem ursprünglichen PDF an support@immersivetranslate.com senden. Wir werden die PDF-Situation überprüfen und den Plan in die intelligenten Erkennungsregeln aufnehmen.
