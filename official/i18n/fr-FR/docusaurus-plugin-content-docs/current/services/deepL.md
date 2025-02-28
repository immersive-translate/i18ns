# DeepL

## Accès direct aux services de traduction DeepL après l'ouverture d'un [Immersive Translate Pro Membership](https://immersivetranslate.com/en/pricing/) (Recommandé)

[En savoir plus](https://immersivetranslate.com/en/pricing/)

## Obtenez l'API officielle DeepL via DeepL

1. Introduction officielle : [DeepL API](https://www.deepl.com/en/pro#developer)

   - Notez que : [DeepL API](https://www.deepl.com/en/pro#developer) et [DeepL Pro](https://www.deepl.com/pro) sont deux types de comptes différents, et le compte [DeepL API](https://www.deepl.com/en/pro/select-country#developer).

2. [Pourquoi](https://www.deepl.com/en/whydeepl) choisir DeepL ?

   - Anglais ⇄ Chinois 5x plus précis
   - Anglais ⇄ Japonais 6x plus précis
   - Moteur de traduction basé sur la technologie d'intelligence artificielle (réseaux neuronaux)

3. L'API DeepL est divisée en [Free API et Pro API](https://www.deepl.com/en/pro#developer)

   - La Free API fournit 500 000 caractères gratuits par mois.
   - Le [tarif officiel](https://www.deepl.com/en/pro#developer) pour la Pro API est : 25 $ par million de caractères.
   - Pour un utilisateur à haute fréquence, le nombre de caractères consommés en un mois est d'environ 10 millions de caractères, et le prix est d'environ : 250 USD

4. Pour enregistrer un compte et ouvrir l'[API DeepL](https://www.deepl.com/en/pro#developer).

## problèmes courants

### 1. La clé remplie n'est pas disponible.

DeepL API Pro et DeepL Pro sont deux types de comptes, la clé d'authentification qui peut être utilisée dans Immersive Translate est le compte DeepL API, veuillez cliquer ici pour [DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer)

### 2. Résolution des erreurs d'authentification 401, 403

Ces erreurs se produisent généralement lorsque vous utilisez le mauvais type de clé d'authentification. Veuillez noter :

1. DeepL propose deux produits différents : DeepL Pro (service de traduction) et DeepL API (interface développeur)
2. Les clés trouvées dans les paramètres de votre compte DeepL Pro ne sont **pas compatibles** avec les appels API
3. Vous devez spécifiquement vous inscrire pour un compte DeepL API pour obtenir une clé API
4. Les clés API DeepL Free se terminent par `:fx`
5. Les clés API DeepL Pro n'ont pas le suffixe `:fx` et apparaissent comme une chaîne de caractères régulière

Veuillez vous assurer que vous vous êtes correctement inscrit au service API DeepL, et non seulement au service de traduction DeepL Pro.

### 3. 456, le quota pour l'utilisateur a été atteint.

L'utilisation a dépassé la limite officielle fixée par DeepL par utilisateur, vous avez peut-être violé la politique d'utilisation équitable de DeepL et il est conseillé d'éviter un tel comportement. Si vous êtes un abonné payant, l'utilisation sera automatiquement réinitialisée le mois prochain.