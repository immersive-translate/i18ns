# Open AI (Azure OpenAI)

Accès direct aux services de traduction d'OpenAI en ouvrant un abonnement [Immersive Translate Pro](https://immersivetranslate.com/en/pricing/) (recommandé)

[Cliquez ici pour la présentation](https://immersivetranslate.com/en/pricing/)

## Obtenez une clé API de la plateforme officielle des développeurs OpenAI.

- [adresse officielle de l'API openAI](https://openai.com/api/)
  - Note : Actuellement, OpenAI n'est pas ouvert à l'inscription avec des numéros de téléphone chinois.
- Après vous être inscrit pour un compte OpenAI, ouvrez [Clé Secrète API](https://platform.openai.com/account/api-keys) pour créer une Clé Secrète API
- Ensuite, il suffit de remplir la clé dans la configuration OpenAI dans l'extension Immersive Translate.

## Mise en garde

1. **Si vous n'avez pas de carte de crédit associée, ou si vous êtes un nouvel utilisateur d'OpenAI 5-lames avec jusqu'à 3 requêtes par minute**, c'est pratiquement inutilisable et il est normal de recevoir des erreurs. [Vous pouvez cliquer ici pour voir les limites de fréquence pour votre API](https://platform.openai.com/account/rate-limits)
2. L'API d'OpenAI et ChatGPT sont deux services différents, l'extension Immersive Translate prend en charge l'API d'OpenAI, pas la version web de ChatGPT, donc vous devez ouvrir le service API d'OpenAI au lieu d'ouvrir ChatGPT plus, et remplir la clé API sur la page des paramètres après ouverture.
3. Erreur 429, cela signifie que la limite de fréquence d'openai a été dépassée, il est recommandé de réduire le nombre maximum de requêtes par seconde, surtout lors de la traduction de livres électroniques, même s'il s'agit d'une version payante, vous devez réduire le nombre maximum de requêtes par seconde, et l'ajuster à 5 requêtes par seconde pour le rendre plus stable.
4. Le modèle OpenAI gpt-3.5-turbo est tarifé à : $0.002 / 1K tokens, et coûte environ $1 pour traduire 660 000 caractères anglais et $0.25 pour traduire 170 000 caractères anglais.
5. L'extension Immersive Translate prend en charge plusieurs clés API pour l'équilibrage de charge, veuillez utiliser une virgule `,` pour séparer les différentes clés lorsque vous remplissez le formulaire.

## Recommandation actuelle du nombre de requêtes

Récemment, OpenAI est également devenu très restrictif pour les utilisateurs payants, à partir de la version 0.5.0 le nombre de requêtes par défaut a été changé en secondes, et le nombre maximum de requêtes par seconde par défaut a été changé à 10 requêtes par seconde.

## Azure OpenAI

Le service de traduction OpenAI est également compatible avec l'interface Azure OpenAI. Tout d'abord, créez le service OpenAI dans la console Azure, puis rendez-vous sur Azure AI Studio : https://oai.azure.com, créez un déploiement gpt-35-turbo, et souvenez-vous du nom du déploiement.

Après avoir déployé le modèle gpt-35-turbo, ouvrez la page des paramètres OpenAI pour Immersive Translate :

1. Clé API Veuillez remplir la clé fournie par la console Azure.
2. Cliquez pour développer plus de paramètres et définissez l'adresse personnalisée à :

`https://{votre-nom-personnalisé}.openai.azure.com/openai/deployments/{votre-nom-de-déploiement}/chat/completions?api-version=2023-03-15-preview`

Changez `{votre-nom-personnalisé}` par votre propre sous-domaine et `{votre-nom-de-déploiement}` par votre propre nom de déploiement.

3. Le nom du modèle doit être sélectionné manuellement pour que le modèle personnalisé puisse être lu : `gpt-35-turbo`,

> Si vous avez encore des questions, vous pouvez aller dans Azure AI Studio, ouvrir PlayGround, [Voir le Code], et il y aura le [EndPoint] final et la [Clé] en bas, comme suit :

![](/assets/docs/doc-assets/azure-openai-key.jpg)

## Personnalisation de l'adresse de l'API d'OpenAI

- Cela peut être configuré via `Plus de Paramètres` avec le point d'entrée suivant

***

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

***