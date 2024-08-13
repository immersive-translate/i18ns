---
sidebar_position: 4
---

# PDF Help

Immersive Translate PDF Bilingual Reader is a bilingual cross-referenced real-time translation tool suitable for use as a reading aid.

Currently, special characters such as mathematical formulas, tables, etc. cannot be handled correctly because of the plain text recognition technique.

If your PDF contains tables and mathematical formulas that require higher quality translation, you can experience our [PDF PRO](https://app.immersivetranslate.com/pdf-pro/)

See [documentation here](/docs/usage/#pdf-file-translation) for basic usage questions 

Here are some advanced PDF translation tips：
<!-- 
## Move to adjust the translation box

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/pdf-move.png) -->

### Edit Box

The default translation is editable.You can even click "Show original text" in the panel, and the content of the text box will be displayed as the original text intelligently recognized, and you can make corrections to the original text in the edit box at this time.Then re-click on the panel translation

### Moving Text Boxes

When some paragraphs are recognized in an incorrect position, you can choose to move the position of the entire paragraph edit box by placing the mouse in the upper left corner.(If you encounter a situation where you can't drag, you can zoom and drag down the lower right corner, and the upper left corner will move normally)

### Delete text box

When some paragraphs may have recognition problems, manually merge the previous paragraph, this paragraph may be redundant, this time you can click this button to delete it!

### Scaling text box size

Because the default translation height and width are the same as the original paragraph by default, when the translation content exceeds the original text there will be an overflow, in this case you can view it through the inner scroll.You can also drag and drop in the lower right corner to enlarge this text box appropriately to allow the content to be fully displayed.

<!-- ## Control Style Buttons

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/pdf-control.png) -->

### Bandwagon Mode

The default is to restore the image of the original text to the translated area on the right.It is normal to see a white background frame for the translated text, because it is necessary to cover the original text drawn by canvas so that the translated text can be displayed properly.

If you find that the underlay mode affects your reading, just turn it off.

### Overlap Limit

Because we use as much as possible to restore the original typographical effect, so the paragraph starting position is the original paragraph of the upper left corner of the coordinates prevail.Under normal circumstances English to Chinese translation, the Chinese content will generally be smaller than the English, this time the translation can be fully demonstrated.This occurs when the translated text is redundant with the original text in some cases.In order to avoid this we have given the translation a height equal to that of the original paragraph.

This can be turned off when we feel that the distance between the upper and lower paragraphs is sufficient for the presentation of the translated portion of the exceeding

### Tightly Spaced

This objective is actually similar to the one above, because there is a certain spacing between each line of text in order to ensure the readability of the translated text.

If the screen is small and the spacing between the top and bottom paragraphs may not be enough to show the overflow of the translated text, you can turn on this item and remove the text line spacing, so that the text of the paragraphs can be fully displayed

### Paragraph header indentation

Because of the complexity of the various PDF layout, can not be intelligently identified as a paragraph is in line with the characteristics of indentation, but there is no indentation, then you may look at the article paragraph is a little bit of a struggle.So it's this article type of paragraph, the user can turn it on and the first paragraph of each paragraph will be indented to show the

### Lines are widely spaced and paragraphs are not recognized

Some PDF may be in order to display the reasons, paragraph spacing is relatively large, resulting in intelligent recognition of the time will be judged to be this sentence into an independent paragraph.So it needs to be adjusted appropriately by say 10, so that 10px is used as the line spacing to re-recognize the paragraphs on the page.

### Adjusting the horizontal position of translations

Because the horizontal coordinates of the translated text are read from the original pdf data, some of the horizontal coordinates of the pdf will be large.In this case you can make the translated content move to the left by dragging the progress bar.

### Adjusting the scaling of translations

The size of the translated text is basically the same as the original text, when you feel that the size of the translated text is not appropriate, you can drag the progress bar to let the font size adjusted according to the ratio

## Manual adjustment of error segments

If the intelligently recognized paragraph is incorrect, it can be manually adjusted by the following steps

- Click on the translation panel to display the recognized original text
- Then manually adjust the paragraph against the original text on the left by copying and line breaks, etc.
- When the paragraph is confirmed to be correct, click on Translate again

<!-- ## Download Print

Click on the download icon in the upper right corner

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/pdf-download.png) -->

Because our tool relies on the browser, download speeds and results are heavily dependent on the browser itself.So it is recommended not to deal with more than 300 pages of PDF

### Translation Download (Print)

This feature downloads translations only, not bilingual.
When the default translation is displayed, the zoom mode is set to page width for reading effect.

However, when the need to print and save the time it is recommended to adjust the zoom mode, it is generally recommended to adjust to 100 percent or the actual size, the printing effect will be better.

## Can the White Background of Text in a PDF Be Removed?
It cannot be removed. Removing it would reveal the English text underneath.

### Bilingual preservation

Due to technical limitations on bilingual preservation effects, translations are preserved in the form of images, enabling WYSIWYG preservation of online translation effects.It takes about 5/6 minutes to export 300 pages of PDF.

## Other situations

### untranslatable

- Check whether the original text on the left can be copied, if it can not be copied, it is proved to be a picture PDF, the current temporary support for the picture PDF translation
- Check that the translation is recognized but not translated, that 🔄❓ does not appear at the end of the paragraph, and that the button in the plug-in's panel shows "Translate".At this point, click on the translate button to trigger the translation.
- If 🔄❓ exists, click under ❓ to see the error message

### Mail Feedback Document

You can send a description of your problem + a screenshot with the original PDF to support@immersivetranslate.com\. We will check the PDF situation and arrange for the plan to be entered into the intelligent recognition rules.
