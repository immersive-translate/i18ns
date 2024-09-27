# Open AI (Azure OpenAI)

Direkter Zugang zu den Übersetzungsdiensten von OpenAI durch Eröffnung einer [Immersive Translate Pro-Mitgliedschaft](https://immersivetranslate.com/en/pricing/) (empfohlen)

[Hier klicken für Präsentation](https://immersivetranslate.com/en/pricing/)

## Einen API-Schlüssel von der offiziellen OpenAI-Entwicklerplattform erhalten.

- [offizielle Adresse der openAI API](https://openai.com/api/)
  - Hinweis: Derzeit ist OpenAI nicht für die Registrierung mit chinesischen Handynummern geöffnet.
- Nach der Registrierung eines OpenAI-Kontos, öffnen Sie [API Secret Key](https://platform.openai.com/account/api-keys), um einen API Secret Key zu erstellen
- Füllen Sie dann einfach den Schlüssel in der OpenAI-Konfiguration in der Immersive Translate-Erweiterung aus.

## Vorbehalt

1. **Wenn Sie keine Kreditkarte damit verknüpft haben oder ein neuer OpenAI 5-Klingen-Nutzer mit bis zu 3 Anfragen pro Minute sind**, ist es im Grunde unbrauchbar und es ist normal, Fehler zu erhalten. [Sie können hier klicken, um die Frequenzgrenzen für Ihre API zu sehen](https://platform.openai.com/account/rate-limits)
2. OpenAIs API und ChatGPT sind zwei verschiedene Dienste, die Immersive Translate Extension unterstützt OpenAIs API, nicht die Webversion von ChatGPT, also müssen Sie den OpenAI-API-Dienst öffnen, anstatt ChatGPT Plus zu öffnen, und den API-Schlüssel auf der Einstellungsseite eingeben, nachdem Sie ihn geöffnet haben.
3. 429-Fehler bedeutet, dass das Frequenzlimit von OpenAI überschritten wurde. Es wird empfohlen, die maximale Anzahl von Anfragen pro Sekunde zu reduzieren, insbesondere beim Übersetzen von E-Books, selbst wenn es sich um eine bezahlte Version handelt. Sie müssen die maximale Anzahl von Anfragen pro Sekunde reduzieren und auf 5 Anfragen pro Sekunde einstellen, um es stabiler zu machen.
4. Das OpenAI gpt-3.5-turbo Modell wird zu $0.002 / 1K Token berechnet und kostet etwa $1, um 660.000 englische Zeichen zu übersetzen und $0.25, um 170.000 englische Zeichen zu übersetzen.
5. Die Immersive Translate Extension unterstützt mehrere API-Schlüssel für Lastausgleich, bitte verwenden Sie ein Komma `,` um verschiedene Schlüssel zu trennen, wenn Sie das Formular ausfüllen.

## Aktuelle Empfehlung zur Anzahl der Anfragen

In letzter Zeit ist OpenAI auch für zahlende Nutzer sehr restriktiv geworden. Ab Version 0.5.0 wurde die Standardanfragenzahl auf Sekunden geändert, und die maximale Standardanzahl von Anfragen pro Sekunde wurde auf 10 Anfragen pro Sekunde geändert.

## Azure OpenAI

Der Übersetzungsdienst von OpenAI ist auch kompatibel mit der Azure OpenAI-Schnittstelle. Zuerst erstellen Sie den OpenAI-Dienst in der Azure-Konsole, dann gehen Sie zu Azure AI Studio: https://oai.azure.com, erstellen eine gpt-35-turbo-Bereitstellung und merken sich den Bereitstellungsnamen.

Nach der Bereitstellung des gpt-35-turbo-Modells öffnen Sie die OpenAI-Einstellungsseite für Immersive Translate:

1. Api-Schlüssel Bitte füllen Sie den Schlüssel aus, der von der Azure-Konsole bereitgestellt wurde.
2. Klicken Sie, um mehr Einstellungen zu erweitern, und setzen Sie die angepasste Adresse auf:

`https://{Ihr-benutzerdefinierter-Name}.openai.azure.com/openai/deployments/{Ihr-Bereitstellungsname}/chat/completions?api-version=2024-07-01-preview`

Ändern Sie `{Ihr-benutzerdefinierter-Name}` in Ihren eigenen Subdomain-Namen und `{Ihr-Bereitstellungsname}` in Ihren eigenen Bereitstellungsnamen.

3. Der Modellname muss manuell für das benutzerdefinierte Modell ausgewählt werden, um zu lesen: `gpt-35-turbo`,

> Wenn es noch Fragen gibt, können Sie in Azure AI Studio gehen, PlayGround öffnen, [Code anzeigen], und am Ende werden der finale [EndPoint] und [Schlüssel] angezeigt, wie folgt:

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

## Anpassen der API-Adresse von OpenAI

- Dies kann über `Weitere Einstellungen` mit dem folgenden Einstiegspunkt konfiguriert werden

---

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

---
