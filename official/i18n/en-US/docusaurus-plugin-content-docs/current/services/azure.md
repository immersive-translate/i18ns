# Microsoft Azure Translation

## Brief Statement

1. Official website:[Translated by Microsoft Azure](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/text-translation-overview)
2. Official Description: Translations are free up to 2 million words per month, if you exceed 2 million words per month, we will charge you at a rate of $10 / 1 million words.For more details, please refer to [Pricing Note](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/)

## Registration Process

The registration process is more cumbersome than other translation services and requires patience.

Reference Link:[Microsoft Azure Translation Getting Started Documentation](https://learn.microsoft.com/en-us/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)

## Sign up for an Azure account

The first step is to sign up for an [Azure](https://azure.microsoft.com/en-us/free/cognitive-services/) account, which requires an international credit card (Visa/Master) to be bound.If not, it will not be possible to register.

## Registering for an Azure Blob Storage Account

Step 2: Register for an [Azure Blob](https://portal.azure.com/#create/Microsoft.StorageAccount) storage account.

1. Create a new resource group and fill in the storage account name
2. Choose a region that is closest to you, for example, the Hong Kong region would be `East Asia`.
3. The rest of the process is just a straightforward next step.On the last page, after the deployment is complete, click the blue button "Create" at the bottom left.

## Creating Translation Tools

Step 3: Create [translation tool](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation)

1. Choose a region that is closest to you, for example, the Hong Kong region would be `East Asia`.
2. Pricing tiers are selected as needed, with `Free F0` available for free users.The free tier does not support document translation.A standard S1 trial can be used if required.
3. The rest of the process is just a straightforward next step.On the last page, after the deployment is complete, click the blue button "Create" at the bottom left.

## Access Key

After successful deployment, go to [Azure Dashboard](https://portal.azure.com/#home), go to the page for **Translation Tools**, and find the key in the left menu - Resource Management - `Keys and Endpoints`.Microsoft will provide 2 keys, choose one and fill the key into the `APIKEY` of the Immersive Extension - Microsoft Translator.

Below the key there is also a `location/region` information, e.g. `eastasia`, which also needs to be populated in the `region` of the immersive extension - Microsoft Translate.

## Common Problems

If in doubt, please give feedback [here](https://github.com/immersive-translate/immersive-translate/issues/137).
