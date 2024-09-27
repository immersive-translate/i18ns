# DeepL

## Accès direct aux services de traduction DeepL après l'ouverture d'un [Abonnement Immersive Translate Pro](https://immersivetranslate.com/en/pricing/) (Recommandé)

[Cliquez ici pour la présentation](https://immersivetranslate.com/en/pricing/)

## Obtenez l'API officielle DeepL via DeepL

1. Introduction officielle : [API DeepL](https://www.deepl.com/en/pro#developer)

   - Notez que : [API DeepL](https://www.deepl.com/en/pro#developer) et [DeepL Pro](https://www.deepl.com/pro) sont deux types de comptes différents, et le compte [API DeepL](https://www.deepl.com/en/pro/select-country#developer).

2. [Pourquoi](https://www.deepl.com/en/whydeepl) choisir DeepL ?

   - Anglais ⇄ Chinois 5 fois plus précis
   - Anglais ⇄ Japonais 6 fois plus précis
   - Moteur de traduction basé sur la technologie de l'intelligence artificielle (réseaux neuronaux)

3. L'API DeepL est divisée en [API gratuite et API Pro](https://www.deepl.com/en/pro#developer)

   - L'API gratuite fournit 500 000 caractères gratuits par mois.
   - Le [tarif officiel](https://www.deepl.com/en/pro#developer) pour l'API Pro est de : 25 $ pour 1 million de caractères.
   - Pour un utilisateur à haute fréquence, la quantité de caractères consommés dans un mois est d'environ 10 millions de caractères, et le prix est d'environ : 250 USD

4. Pour s'inscrire à un compte et ouvrir l'[API DeepL](https://www.deepl.com/en/pro#developer).

## Construisez votre propre API DeepL

Nous expérimentons le support pour notre propre service DeeplX dans la fonctionnalité Bêta (mais cela n'est pas bien adapté comme service de traduction web, comme testé. En raison de l'énorme quantité de demandes d'API pour la traduction de pages web, si vous construisez ce service, veuillez vous assurer de bien équilibrer la charge), voici comment activer les fonctionnalités expérimentales des instructions :

1. Activer les Fonctionnalités de Test Bêta dans les Paramètres Développeur
2. Trouver DeepLX (Bêta) dans les Paramètres de Base et entrer l'URL de l'API DeepL construite par soi-même, par exemple http\://votre-domaine/traduire

> Q : Comment construire le mien ?
>
> R : [OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate) ou [zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md) -->

## problèmes communs

### 1. La clé remplie n'est pas disponible.

DeepL API Pro et DeepL Pro sont deux types de comptes, la clé Auth qui peut être utilisée dans Immersive Translate est le compte DeepL API, veuillez cliquer ici pour [DeepL API Pro](https://www.deepl.com/en/pro/select-country#) développeur)

### 2. L'API gratuite Deepl indique 401 Pas de Privilège

Les clés de l'API gratuite Deepl se terminent toutes par `:fx`, tout le reste n'est pas une clé d'API gratuite.

### 3. 456, Le quota pour l'utilisateur a été atteint.

L'utilisation a dépassé la limite officielle stricte par utilisateur de DeepL, vous avez peut-être violé la politique d'utilisation équitable de DeepL et il est conseillé d'éviter un tel comportement. Si vous êtes un abonné payant, l'utilisation sera automatiquement réinitialisée le mois prochain.
