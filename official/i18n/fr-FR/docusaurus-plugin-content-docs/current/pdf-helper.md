---
sidebar_position: 4
---

# Aide PDF

Immersive Translate PDF Bilingual Reader est un outil de traduction en temps réel bilingue et croisé adapté à l'utilisation comme aide à la lecture.

Actuellement, les caractères spéciaux tels que les formules mathématiques, les tableaux, etc., ne peuvent pas être traités correctement en raison de la technique de reconnaissance de texte brut.

Si votre PDF contient des tableaux et des formules mathématiques, et que vous avez des exigences de traduction de haute qualité pour ceux-ci et que vous avez quelques compétences en codage, il est recommandé de consulter cet article [Nouga-OCR + Immersive Translate](https://app.immersivetranslate.com/pdf-pro/)

Voir la [documentation ici](/docs/usage/#pdf-file-translation) pour les questions d'utilisation de base

Voici quelques astuces avancées pour la traduction de PDF :

### Modifier la boîte

La traduction par défaut est modifiable. Vous pouvez même cliquer sur "Afficher le texte original" dans le panneau, et le contenu de la boîte de texte sera affiché comme le texte original intelligemment reconnu, et vous pouvez à ce moment faire des corrections au texte original dans la boîte de modification. Puis recliquez sur la traduction du panneau

### Déplacer les boîtes de texte

Lorsque certains paragraphes sont reconnus dans une position incorrecte, vous pouvez choisir de déplacer la position de la boîte de modification du paragraphe entier en plaçant la souris dans le coin supérieur gauche. (Si vous rencontrez une situation où vous ne pouvez pas glisser, vous pouvez zoomer et glisser vers le bas le coin inférieur droit, et le coin supérieur gauche se déplacera normalement)

### Supprimer la boîte de texte

Lorsque certains paragraphes peuvent avoir des problèmes de reconnaissance, fusionner manuellement le paragraphe précédent, ce paragraphe peut être redondant, vous pouvez alors cliquer sur ce bouton pour le supprimer !

### Ajustement de la taille de la zone de texte

Étant donné que la hauteur et la largeur de traduction par défaut sont les mêmes que celles du paragraphe original par défaut, lorsque le contenu de la traduction dépasse le texte original, il y aura un débordement, dans ce cas, vous pouvez le visualiser à travers le défilement interne. Vous pouvez également cliquer et glisser dans le coin inférieur droit pour agrandir cette zone de texte de manière appropriée afin de permettre l'affichage complet du contenu.

### Mode Bandwagon

Le défaut est de restaurer l'image du texte original dans la zone traduite à droite. Il est normal de voir un cadre de fond blanc pour le texte traduit, car il est nécessaire de couvrir le texte original dessiné par canvas afin que le texte traduit puisse être affiché correctement.

Si vous trouvez que le mode sous-couche affecte votre lecture, désactivez-le simplement.

### Limite de Superposition

Parce que nous utilisons autant que possible pour restaurer l'effet typographique original, la position de départ du paragraphe est celle du coin supérieur gauche des coordonnées du paragraphe original. Dans des circonstances normales de traduction de l'anglais vers le chinois, le contenu en chinois sera généralement plus petit que l'anglais, cette fois la traduction peut être pleinement démontrée. Cela se produit lorsque le texte traduit est redondant avec le texte original dans certains cas. Afin d'éviter cela, nous avons donné à la traduction une hauteur égale à celle du paragraphe original.

Cela peut être désactivé lorsque nous estimons que la distance entre les paragraphes supérieur et inférieur est suffisante pour la présentation de la partie traduite dépassant

### Espacement Serré

Cet objectif est en fait similaire au précédent, car il y a un certain espacement entre chaque ligne de texte afin d'assurer la lisibilité du texte traduit.

Si l'écran est petit et que l'espacement entre les paragraphes supérieur et inférieur peut ne pas être suffisant pour montrer le débordement du texte traduit, vous pouvez activer cet élément et supprimer l'espacement des lignes de texte, de sorte que le texte des paragraphes puisse être entièrement affiché

### Indentation des en-têtes de paragraphes

En raison de la complexité des différentes mises en page PDF, il n'est pas possible d'identifier intelligemment si un paragraphe est conforme aux caractéristiques d'indentation. Cependant, en l'absence d'indentation, la lecture des paragraphes de l'article peut s'avérer quelque peu laborieuse. Pour ce type d'article, l'utilisateur peut activer l'option d'indentation et le premier paragraphe de chaque section sera indenté pour l'indiquer.

### Les lignes sont largement espacées et les paragraphes ne sont pas reconnus

Certains PDF peuvent, pour des raisons d'affichage, présenter un espacement de paragraphe relativement grand, ce qui, lors de la reconnaissance intelligente, peut amener à considérer cette phrase comme un paragraphe indépendant. Il est donc nécessaire d'ajuster cela de manière appropriée, par exemple à 10, afin que 10px soit utilisé comme espacement des lignes pour reconnaître à nouveau les paragraphes de la page.

### Ajustement de la position horizontale des traductions

Étant donné que les coordonnées horizontales du texte traduit sont lues à partir des données PDF originales, certaines des coordonnées horizontales du PDF peuvent être grandes. Dans ce cas, vous pouvez faire déplacer le contenu traduit vers la gauche en faisant glisser la barre de progression.

### Ajustement de l'échelle des traductions

La taille du texte traduit est essentiellement la même que celle du texte original. Lorsque vous estimez que la taille du texte traduit n'est pas appropriée, vous pouvez faire glisser la barre de progression pour ajuster la taille de la police selon le ratio.

## Ajustement manuel des segments erronés

Si le paragraphe reconnu intelligemment est incorrect, il peut être ajusté manuellement selon les étapes suivantes :

- Cliquez sur le panneau de traduction pour afficher le texte original reconnu.
- Ensuite, ajustez manuellement le paragraphe par rapport au texte original à gauche en copiant et en insérant des sauts de ligne, etc.
- Lorsque le paragraphe est confirmé comme étant correct, cliquez à nouveau sur Traduire.

Comme notre outil dépend du navigateur, la vitesse de téléchargement et les résultats dépendent fortement du navigateur lui-même. Il est donc recommandé de ne pas traiter plus de 300 pages de PDF.

### Téléchargement de la Traduction (Impression)

Cette fonctionnalité télécharge uniquement les traductions, pas le bilingue.
Lorsque la traduction par défaut est affichée, le mode de zoom est réglé sur la largeur de la page pour un effet de lecture.

Cependant, lorsqu'il est nécessaire d'imprimer et de sauvegarder du temps, il est recommandé d'ajuster le mode de zoom, il est généralement recommandé de l'ajuster à 100 pour cent ou à la taille réelle, l'effet d'impression sera meilleur.

### Conservation bilingue

En raison de limitations techniques sur les effets de conservation bilingue, les traductions sont conservées sous forme d'images, permettant une conservation WYSIWYG des effets de traduction en ligne. Il faut environ 5/6 minutes pour exporter 300 pages de PDF.

## Autres situations

### intraduisible

- Vérifiez si le texte original à gauche peut être copié, si cela n'est pas possible, cela prouve qu'il s'agit d'un PDF image, le support temporaire pour la traduction de PDF image est actuellement disponible
- Vérifiez que la traduction est reconnue mais pas traduite, que 🔄❓ n'apparaît pas à la fin du paragraphe, et que le bouton dans le panneau du plug-in montre "Traduire". À ce moment, cliquez sur le bouton de traduction pour déclencher la traduction.
- Si 🔄❓ existe, cliquez sous ❓ pour voir le message d'erreur

### Document de Retour par Mail

Vous pouvez envoyer une description de votre problème + une capture d'écran avec le PDF original à support@immersivetranslate.com. Nous vérifierons la situation du PDF et organiserons l'entrée du plan dans les règles de reconnaissance intelligente.
