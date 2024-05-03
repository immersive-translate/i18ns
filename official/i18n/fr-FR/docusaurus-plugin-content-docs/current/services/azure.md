# Traduction Microsoft Azure

## Déclaration Brève

1. Site officiel : [Traduit par Microsoft Azure](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/text-translation-overview)
2. Description Officielle : Les traductions sont gratuites jusqu'à 2 millions de mots par mois, si vous dépassez 2 millions de mots par mois, nous vous facturerons au tarif de 10 $ / 1 million de mots. Pour plus de détails, veuillez vous référer à [Note de Tarification](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/)

## Processus d'Inscription

Le processus d'inscription est plus laborieux que pour d'autres services de traduction et nécessite de la patience.

Lien de Référence : [Documentation pour Commencer avec Microsoft Azure Translation](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)

## S'inscrire à un compte Azure

La première étape consiste à s'inscrire à un compte [Azure](https://azure.microsoft.com/en-us/free/cognitive-services/), ce qui nécessite de lier une carte de crédit internationale (Visa/Master). Sans cela, il ne sera pas possible de s'inscrire.

## Inscription à un compte de stockage Azure Blob

Étape 2 : S'inscrire pour un compte de stockage [Azure Blob](https://portal.azure.com/#create/Microsoft.StorageAccount).

1. Créer un nouveau groupe de ressources et remplir le nom du compte de stockage
2. Choisir une région qui est la plus proche de vous, par exemple, la région de Hong Kong serait `Asie de l'Est`.
3. Le reste du processus est juste une suite logique d'étapes. Sur la dernière page, après que le déploiement soit terminé, cliquez sur le bouton bleu "Créer" en bas à gauche.

## Création d'outils de traduction

Étape 3 : Créez [l'outil de traduction](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation)

1. Choisissez une région qui est la plus proche de vous, par exemple, la région de Hong Kong serait `Asie de l'Est`.
2. Les paliers de tarification sont sélectionnés selon les besoins, avec `Gratuit F0` disponible pour les utilisateurs gratuits. Le palier gratuit ne prend pas en charge la traduction de documents. Un essai standard S1 peut être utilisé si nécessaire.
3. Le reste du processus est juste une étape suivante simple. Sur la dernière page, après que le déploiement soit complet, cliquez sur le bouton bleu "Créer" en bas à gauche.

## Clé d'accès

Après un déploiement réussi, allez sur le [Tableau de bord Azure](https://portal.azure.com/#home), allez à la page pour les **Outils de Traduction**, et trouvez la clé dans le menu de gauche - Gestion des Ressources - `Clés et Points de terminaison`. Microsoft fournira 2 clés, choisissez-en une et remplissez la clé dans le `APIKEY` de l'Extension Immersive - Microsoft Translator.

Sous la clé, il y a aussi une information `emplacement/région`, par exemple, `eastasia`, qui doit également être renseignée dans la `région` de l'extension immersive - Microsoft Translate.

## Problèmes Communs

En cas de doute, veuillez donner votre avis [ici](https://github.com/immersive-translate/immersive-translate/issues/137).