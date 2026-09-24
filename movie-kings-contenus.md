# Movie Kings

## Contenus et indications de travail

Ce document rassemble les contenus textuels de la page d’accueil **Movie Kings** ainsi que les principales indications nécessaires à son intégration.

L’objectif n’est pas de reproduire la maquette comme une image figée, mais de construire une page HTML sémantique, responsive et accessible à partir de composants réutilisables.

---

## 1. En-tête

### Identité

**Movie Kings**

### Navigation principale

- Accueil
- Jouer
- Classement

### Choix de la langue

- EN
- FR
- DE

> **Indications de travail**
>
> - Le logo doit permettre de revenir à la page d’accueil.
> - Utilisez un élément de navigation sémantique et une liste de liens.
> - L’état de la page active doit être perceptible autrement que par la couleur seule.
> - Le sélecteur de langue doit également présenter un état actif.
> - Sur mobile, prévoyez une adaptation de la navigation sans réduire excessivement la taille des zones cliquables.
> - Les pictogrammes de navigation peuvent être réalisés en SVG.

---

## 2. Hero

### Titre principal

# Deviens le roi de la réplique !

### Introduction

Reconnais la réplique et choisis le bon film.  
Grimpe au classement et tente de gagner des places.

### Action principale

**Jouer maintenant**

> **Indications de travail**
>
> - Cette zone contient le seul titre de niveau 1 de la page.
> - Le bouton est un lien menant vers la page de préparation du quiz.
> - Le texte et l’illustration forment deux zones distinctes sur grand écran.
> - Sur petit écran, choisissez un ordre de lecture logique avant de modifier la disposition visuelle.
> - La forme inclinée du bloc peut être obtenue en CSS. Évitez d’exporter toute la zone comme une seule image.
> - Déterminez si l’illustration apporte une information ou si elle est décorative afin de choisir un texte alternatif pertinent.

---

## 3. Comment jouer

### Surtitre

**PHASES DU JEU**

### Titre

## Comment jouer ?

### Introduction

Chaque semaine, les meilleurs joueurs sont couronnés et remportent des récompenses.

### Étape 1

#### Lis la réplique

Toujours culte, en VO ou en VF, selon la catégorie que tu as choisie.

### Étape 2

#### Devine le film

Dévoile les propositions ou devine directement pour gagner plus de points !

### Étape 3

#### Gagne des points

Décroche la couronne et tente de gagner des places de cinéma.

> **Indications de travail**
>
> - Les trois étapes appartiennent à une même liste ordonnée.
> - Les numéros doivent rester du texte ou être générés automatiquement par la liste, pas intégrés dans une image.
> - Utilisez une grille pour organiser les étapes sur grand écran.
> - La disposition doit pouvoir passer naturellement de trois colonnes à une seule colonne.
> - Les séparateurs sont décoratifs et ne doivent pas perturber la lecture par un lecteur d’écran.
> - La couronne ou les étoiles placées dans cette zone peuvent être intégrées comme SVG décoratifs.

---

## 4. Cultissime

### Titre

## Cultissime

### Introduction

→ Citation du jour à retrouver. **Teste-toi !**

### Citation

> « Il nous faudrait un plus gros bateau. »

### Texte d’accompagnement

La réponse est cachée pour ne pas gâcher le plaisir.  
Tu ne trouves pas ? **Découvre la réponse →**

### Action

**Révéler la réponse**

### Réponse à prévoir dans l’interface

**Les Dents de la mer**  
Steven Spielberg, 1975

> **Indications de travail**
>
> - La citation doit utiliser une balise prévue pour une citation et non un simple paragraphe.
> - La révélation peut être construite avec des éléments HTML natifs tels que `details` et `summary`.
> - Le contenu révélé doit rester accessible au clavier.
> - N’utilisez pas uniquement `display: none` pour cacher une information qui devrait pouvoir être découverte.
> - La mascotte chevauche visuellement deux sections : réfléchissez au positionnement sans la retirer du flux de lecture si elle influence la hauteur du contenu.
> - Sur mobile, la citation, le texte et l’action doivent être réorganisés sans perdre leur relation.

---

## 5. Catégories

### Surtitre

**CATÉGORIES**

### Titre

## Explore les catégories

### Introduction

Choisis l’univers qui te fait vibrer et découvre de nouvelles répliques à chaque session.

### Action

Poursuites, héros et répliques qui ont marqué le cinéma d’action.

### Comédie

Répliques cultes, personnages inoubliables et humour qui fait encore rire aujourd’hui.

### Drame

Moments forts, personnages complexes et dialogues qui restent en mémoire.

### Science-fiction

Mondes futurs, héros légendaires et répliques interstellaires.

### Horreur

Répliques glaçantes, suspense et frissons garantis.

### Animation

Répliques inoubliables des films d’animation qui font sourire petits et grands.

### Classiques

Répliques emblématiques des films qui ont marqué l’histoire du cinéma.

### Cultes

Ces répliques que tout le monde connaît, même sans avoir vu le film.

> **Indications de travail**
>
> - Chaque catégorie est un même composant présentant un pictogramme, un titre et une description.
> - Chaque carte doit être entièrement cliquable et mener vers le quiz correspondant.
> - Les huit cartes doivent être placées avec CSS Grid.
> - La grille doit s’adapter au nombre de colonnes réellement disponibles.
> - Les cartes peuvent utiliser une variable CSS locale pour définir leur couleur d’accent.
> - Les pictogrammes sont fournis en SVG. Vérifiez leur alignement et leur comportement lors du redimensionnement.
> - Prévoyez les états `hover`, `focus-visible` et actif sans déplacer brutalement la mise en page.
> - Une container query peut modifier la composition interne d’une carte selon la place dont elle dispose.

---

## 6. Pied de page

### Identité et copyright

**Movie Kings**  
© 2027 Movie Kings

### Réseaux et communautés

- Instagram
- TikTok
- YouTube
- Discord

> **Indications de travail**
>
> - Utilisez un élément `footer`.
> - Les liens externes doivent être identifiables et accessibles au clavier.
> - Si une icône accompagne un nom visible, elle peut être considérée comme décorative.
> - Le pied de page doit rester simple et ne pas devenir une nouvelle navigation principale.

---

## 7. Comportements attendus

### Responsive

- La page doit fonctionner au minimum sur une largeur mobile et une largeur desktop.
- Les contenus doivent rester lisibles aux dimensions intermédiaires.
- Le hero ne doit pas dépendre d’une hauteur fixe.
- Les étapes et les catégories doivent changer de composition lorsque l’espace devient insuffisant.
- Aucun contenu ne peut être coupé ou sortir horizontalement de la page.

### Navigation au clavier

- Tous les liens et contrôles doivent être accessibles avec la touche `Tab`.
- L’élément ciblé doit présenter un état `focus-visible` clairement perceptible.
- L’ordre de tabulation doit suivre l’ordre logique du document.

### États interactifs

Prévoyez au minimum les états suivants :

- normal ;
- survolé ;
- ciblé au clavier ;
- actif ou sélectionné ;
- désactivé lorsque le composant le justifie.

### Images et SVG

- Utilisez un format adapté à la nature de chaque visuel.
- Ne transformez pas les textes de la maquette en images.
- Les SVG doivent rester nets et redimensionnables.
- Une image informative reçoit un texte alternatif utile ; une image purement décorative reçoit un texte alternatif vide.

---

## 8. Organisation conseillée des composants

La nomenclature exacte reste libre, mais la page devrait au minimum faire apparaître les composants suivants :

- en-tête ;
- navigation principale ;
- sélecteur de langue ;
- hero ;
- bouton principal ;
- liste des étapes ;
- carte de la citation du jour ;
- grille des catégories ;
- carte de catégorie ;
- pied de page.

> **Réflexion attendue**
>
> Avant de commencer le SCSS, identifiez ce qui relève :
>
> - de la structure générale de la page ;
> - d’un composant réutilisable ;
> - d’une variante de composant ;
> - d’un état interactif ;
> - d’une adaptation liée au viewport ;
> - d’une adaptation liée au conteneur du composant.

---

## 9. Contraintes générales

- Utiliser un HTML sémantique.
- Respecter une nomenclature BEM cohérente.
- Écrire le style en SCSS simple et organisé.
- Employer des propriétés logiques lorsque cela est pertinent.
- Centraliser les couleurs, espacements et dimensions récurrentes dans des variables.
- Éviter les valeurs dupliquées sans justification.
- Utiliser Grid et Flexbox selon la nature de la composition.
- Prévoir les états de focus et vérifier les contrastes.
- Ne pas utiliser de framework CSS.
- Ne pas exporter les sections complètes de la maquette sous forme d’images.

