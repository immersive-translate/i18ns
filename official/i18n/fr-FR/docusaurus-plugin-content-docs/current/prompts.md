---
sidebar_position: 5
---
# Guide de Configuration des Prompts IA

## Vue d'ensemble

Immersive Translate prend en charge la configuration personnalisée des Prompts de traduction IA, permettant aux utilisateurs avancés d'ajuster le comportement de traduction selon leurs besoins. Ce document fournit des instructions détaillées sur les méthodes de configuration, les variables prises en charge et l'utilisation avancée.

## Variables Prises en Charge

### Variables de Base

- `{{text}}` - Le contenu texte à traduire
- `{{from}}` - Langue source
- `{{to}}` - Langue cible
- `{{content_type}}` - Type de texte original (`html` ou `text`)

### Variables de Contexte
- `{{title_prompt}}` - Titre de la page web (lorsqu'il est disponible)
- `{{summary_prompt}}` - Résumé du contexte de la page web (lorsqu'il est disponible)
- `{{terms_prompt}}` - Terminologie professionnelle connexe (lorsqu'elle est disponible)

## Méthodes de Configuration

### 1. System Prompt(`systemPrompt`)
Demande de traduction envoyée à l'IA en tant qu'identité système. Utilisée pour définir le rôle de l'IA et les règles de base.

### 2. Prompt(`prompt`)
Conversation envoyée à l'IA en tant qu'identité utilisateur, contenant le contenu réel à traduire.

### 3. System Multiple Prompt(`systemMultiplePrompt`)
Demande de traduction envoyée à l'IA en tant qu'identité système lorsque le nombre de paragraphes est supérieur à 1. Utilisée pour gérer les scénarios de traduction multi-paragraphes.

### 4. Multiple Prompt(`multiplePrompt`)
Demande envoyée en tant qu'identité utilisateur pour la traduction multi-paragraphes. Prend en charge l'utilisation de séparateurs ou du format YAML.

### 5. Subtitle Prompt(`subtitlePrompt`)

Lorsqu'une traduction de sous-titres est nécessaire, conversation envoyée à l'IA en tant qu'identité utilisateur, contenant le contenu réel à traduire.

## Exemples de Configuration par Défaut

Si un seul paragraphe est collecté, il utilisera le Prompt de paragraphe unique par défaut. Si plusieurs paragraphes sont collectés, il utilisera le Prompt multi-paragraphes par défaut. La plupart des cas seront multi-paragraphes. Le séparateur par défaut pour les paragraphes multiples est `%%`. Nous utilisons délibérément ce séparateur peu commun pour réduire les hallucinations des grands modèles. Vous pouvez utiliser ce Prompt comme base pour le modifier selon vos besoins. Voici les configurations de Prompt par défaut :

### Traduction de Paragraphe Unique

```yaml
systemPrompt: |
    Vous êtes un traducteur natif professionnel de {{to}} qui doit traduire le texte avec fluidité en {{to}}.

    ## Règles de Traduction
    1. Générez uniquement le contenu traduit, sans explications ni contenu supplémentaire (comme "Voici la traduction :" ou "Traduction comme suit :")
    2. La traduction renvoyée doit maintenir exactement le même nombre de paragraphes et le même format que le texte original
    3. Si le texte contient des balises HTML, considérez où les balises doivent être placées dans la traduction tout en maintenant la fluidité
    4. Pour le contenu qui ne doit pas être traduit (comme les noms propres, le code, etc.), conservez le texte original
    5. Générez la traduction directement (sans séparateurs, sans texte supplémentaire){{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  Traduisez en {{to}} (générez uniquement la traduction) :

  {{text}}
```

### Traduction Multi-Paragraphes

```yaml
multipleSystemPrompt: |
    Vous êtes un traducteur natif professionnel de {{to}} qui doit traduire le texte avec fluidité en {{to}}.

    ## Règles de Traduction
    1. Générez uniquement le contenu traduit, sans explications ni contenu supplémentaire (comme "Voici la traduction :" ou "Traduction comme suit :")
    2. La traduction renvoyée doit maintenir exactement le même nombre de paragraphes et le même format que le texte original
    3. Si le texte contient des balises HTML, considérez où les balises doivent être placées dans la traduction tout en maintenant la fluidité
    4. Pour le contenu qui ne doit pas être traduit (comme les noms propres, le code, etc.), conservez le texte original{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## Exemples de Format Entrée-Sortie

    ### Exemple d'Entrée :
    Paragraph A

    %%

    Paragraph B

    %%

    Paragraph C

    %%

    Paragraph D

    ### Exemple de Sortie :
    Translation A

    %%

    Translation B

    %%

    Translation C

    %%

    Translation D

multiplePrompt: |
  Traduisez en {{to}} :

  {{text}}
subtitlePrompt: |
  Traduisez en {{to}} :

  {{text}}
```

## Utilisation Avancée (Format YAML)

Pour les scénarios nécessitant un contrôle plus précis (par exemple, des sorties multi-étapes), le format YAML peut être utilisé pour la configuration :

### Variables Avancées

- `{{yaml}}` - Données d'entrée au format YAML

La variable 'yaml' par défaut ressemble à ceci :

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

Nous attendons par défaut que la sortie du grand modèle soit ainsi :

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好吗？
```

Si vous utilisez le `{{yaml}}` par défaut, vous devez exprimer clairement cette attente dans le prompt. Si vous souhaitez modifier le format `yaml` par défaut et de réponse, cela ne peut pas être résolu via l'interface utilisateur de la page de paramètres d'Immersive Translate. Vous devez modifier directement la configuration utilisateur au format JSON d'Immersive Translate.

Chemin d'édition de la configuration utilisateur : `Page des Paramètres`->`Paramètres du Développeur`->`Edit Full User Config` (Veuillez sauvegarder votre configuration utilisateur avant de modifier)

Vous pouvez trouver la configuration du service de traduction dans le JSON de la configuration utilisateur (si elle n'existe pas, ajoutez-la simplement selon cette structure) :

```
{
  ...
  "translationServices": {
    "openai": {
       ...
      }
  },
  ...

```

La variable `yaml` est composée de `env.imt_yaml_item`, vous pouvez donc modifier le format de `imt_yaml_item` comme suit :

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

Une autre variable spéciale est `imt_subtitle_yaml_item`, similaire à `imt_yaml_item`, utilisée pour les éléments YAML de traduction de sous-titres.

Pour les autres variables `env`, vous pouvez ajouter n'importe quelle variable `env` et l'utiliser directement dans le prompt au format `{{nom_variable}}`, comme les variables `env` par défaut suivantes :

- `{{imt_source_field}}` - Nom du champ de texte source (par défaut : text)
- `{{imt_trans_field}}` - Nom du champ de texte traduit (par défaut : text)
- `{{imt_sub_source_field}}` - Nom du champ de texte source des sous-titres
- `{{imt_sub_trans_field}}` - Nom du champ de texte traduit des sous-titres

Y compris `title_prompt`, `summary_prompt`, `terms_prompt` sont également configurés via `env`, par défaut comme suit :

```
        "title_prompt": "\n\n## Conscience du Contexte\nMétadonnées du Document :\nTitre : 《{{imt_title}}》",
        "summary_prompt": "\n\n## Conscience du Contexte\nMétadonnées du Document :\nRésumé : {{imt_theme}}...",
        "terms_prompt": "\n\nTerminologie Requise : Vous DEVEZ utiliser les termes suivants pendant la traduction. Si 'source':'target' et source == target, gardez le terme source inchangé.\n\n Termes -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## Conscience du Contexte\nMétadonnées du Document :\nType : Sous-titre\nRésumé : {{imt_theme}}...",
        "sub_terms_prompt": "\n\nTerminologie Requise : Vous DEVEZ utiliser les termes suivants pendant la traduction. Si 'source':'target' et source == target, gardez le terme source inchangé.\n\n Termes -> \n\n {{imt_terms}}"

```

Où `imt_title`, `imt_theme`, `imt_terms` sont des variables spéciales injectées par le système. `imt_title` est le titre, `imt_theme` est le résumé de toute la page web, `imt_terms` sont les termes clés extraits par le modèle.

> Note : `imt_theme`, `imt_terms` sont extraits par un service propriétaire et ne sont actuellement disponibles que pour les [membres Pro](https://immersivetranslate.com/pricing/).

### Exemple de YAML Prompt

```yaml
systemPrompt: |
  Vous êtes un moteur de traduction automatique professionnel et authentique.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    Vous recevrez une entrée au format YAML contenant des entrées avec les champs "id" et "{{imt_source_field}}". Voici l'entrée :

    <yaml>
    {{yaml}}
    </yaml>

    Pour chaque entrée dans le YAML, traduisez le contenu du champ "{{imt_source_field}}" en {{to}},{{html_only}} écrivez la traduction dans le champ "{{imt_source_field}}" de cette entrée.

    Voici un exemple du format attendu :

    {{normal_result_yaml_example}}

    Veuillez renvoyer le YAML traduit directement sans balise <yaml> ou informations supplémentaires.
subtitlePrompt: |
    Vous recevrez une entrée de sous-titres au format YAML contenant des entrées avec les champs "id" et "{{imt_sub_source_field}}". Voici l'entrée :

    <yaml>
    {{yaml}}
    </yaml>

    Pour chaque entrée dans le YAML, traduisez le contenu du champ "{{imt_sub_source_field}}" en {{to}},{{html_only}} écrivez la traduction dans le champ "{{imt_sub_source_field}}" de cette entrée.

    Voici un exemple du format attendu :

    {{subtitle_result_yaml_example}}

    Veuillez renvoyer le YAML traduit directement sans balise <yaml> ou informations supplémentaires.

```

`html_only` est une variable spéciale qui n'existe que lorsque le texte original à traduire est au format HTML. La valeur est : `\n\nNote : Si le texte contient des balises HTML, veuillez considérer après la traduction où les balises doivent être dans le résultat de la traduction, tout en maintenant la fluidité du résultat.`, cette variable n'existe que lorsque l'utilisateur active activement "Traduction de Texte Enrichi" dans les services de traduction IA. Sinon, elle est vide.

`normal_result_yaml_example` est défini dans `env`, la valeur par défaut est :

```
<example>
Input:
  - id: 1
    {{imt_source_field}}: Source
Output:
  - id: 1
    {{imt_trans_field}}: Translation
</example>
```

`subtitle_result_yaml_example` est défini dans `env`, la valeur par défaut est :

```
<example>
Input:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
Output:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
</example>

```

Vous pouvez le remplacer dans `env`.

## Exemple Avancé : Traduction Réflexive

Cet exemple montre comment utiliser le format YAML pour implémenter un flux de traduction plus complexe, incluant deux étapes : traduction initiale et traduction optimisée :

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # La traduction finale utilise le champ step2
  imt_sub_source_field: source
  imt_sub_trans_field: step2
  imt_yaml_item: |-
    - id: {{id}}
      {{imt_source_field}}: {{text}}
  imt_subtitle_yaml_item: |-
    - id: {{id}}
      {{imt_sub_source_field}}: {{text}}

systemPrompt: |
  Vous êtes un moteur de traduction automatique professionnel et authentique.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  Voici l'entrée YAML :
  <yaml>
  {{yaml}}
  </yaml>
  
  Veuillez suivre ces étapes :
  1. Extrayez le contenu du champ "source" de l'objet YAML fourni.
  2. Traduisez le contenu extrait en {{to}}. Placez cette traduction initiale dans le champ step1.
  3. Optimisez la traduction initiale de step1 pour qu'elle soit plus naturelle et compréhensible en {{to}}. 
     Placez cette traduction optimisée dans le champ step2.
  4. Formatez le résultat comme un tableau YAML avec les champs id, step1 et step2, comme illustré dans cet exemple :
  
  - id: 1 
    step1: Traduction initiale
    step2: Traduction optimisée
  
  Veuillez renvoyer le YAML traduit directement sans balises <example_output> ou informations supplémentaires.
```

### Description du Flux de Travail

1. **Format d'Entrée**：
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **Étapes de Traitement IA**：
   - Étape 1 : Effectuez la traduction initiale
   - Étape 2 : Optimisez la traduction pour qu'elle soit plus naturelle et fluide

3. **Format de Sortie**：
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎么样？"
     step2: "你好吗？"
   ```
