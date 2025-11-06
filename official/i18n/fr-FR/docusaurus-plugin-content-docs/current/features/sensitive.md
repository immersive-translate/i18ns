---
sidebar_position: 7
---

# Mode confidentialité (Bêta)

## Guide de masquage des informations sensibles

> Cette fonctionnalité est prise en charge dans la version 1.23.1+ du plugin.

Après avoir activé [OneAIFW](https://github.com/funstory-ai/aifw) intégré ou personnalisé, le plugin identifiera et masquera automatiquement les informations sensibles (telles que les adresses e-mail, les numéros de téléphone, les numéros de carte d'identité, etc.) pendant la traduction pour protéger votre vie privée et votre sécurité. Ce guide vous montrera comment voir quelles informations sensibles ont été identifiées et masquées pendant la traduction.

### Affichage des journaux de masquage

#### Étape 1 : Activer la journalisation

1. Ouvrez la [**page des paramètres développeur**](https://dash.immersivetranslate.com/#advanced) du plugin
2. Activez l'option **"Activer la journalisation de la console"**

#### Étape 2 : Ouvrir la console développeur

1. Appuyez sur `F12` sur la page Web (ou faites un clic droit sur la page et sélectionnez "Inspecter" / "Inspecter l'élément")
2. Passez à l'onglet "Console"

#### Étape 3 : Filtrer les journaux de masquage

Entrez `sensitive-` dans la boîte de filtre de la console pour filtrer tous les journaux liés au masquage des informations sensibles.

### Explication du format des journaux

Dans la console, vous verrez des journaux au format suivant :

```
[sensitive-encode] "Email: tester.cn+alias@example.com" -> "Email: __PII_EMAIL_ADDRESS_1__"

[sensitive-decode] "Email: __PII_EMAIL_ADDRESS_1__" -> "Email: tester.cn+alias@example.com"
```

#### Signification des journaux

- **`[sensitive-encode]`** : Indique le processus d'identification et de masquage des informations sensibles
  - Le côté gauche est le texte original (contenant des informations sensibles)
  - Le côté droit est le texte masqué (`__PII_*` est le placeholder de masquage)

- **`[sensitive-decode]`** : Indique le processus de restauration du texte masqué
  - Le côté gauche est le texte masqué (contenant des placeholders)
  - Le côté droit est le texte original restauré

#### Explication des placeholders

Les placeholders au format `__PII_*` représentent le type d'informations sensibles qui ont été masquées, par exemple :
- `__PII_EMAIL_ADDRESS_1__` : Adresse e-mail
- `__PII_PHONE_NUMBER_1__` : Numéro de téléphone
- `__PII_ID_CARD_1__` : Numéro de carte d'identité
- etc.

### Principes de masquage

Pour les principes spécifiques et les détails d'implémentation du masquage des informations sensibles, vous pouvez consulter la documentation et le code du [projet OneAIFW](https://github.com/funstory-ai/aifw).

### Notes

- Cette fonctionnalité est actuellement en **phase de test bêta**, et il peut y avoir des cas d'identification inexacte ou d'échecs de masquage
- Si vous rencontrez des échecs de masquage ou des erreurs d'identification, veuillez soumettre des commentaires via [GitHub Issues](https://github.com/funstory-ai/aifw/issues), et nous continuerons à itérer et optimiser

