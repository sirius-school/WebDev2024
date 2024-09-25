<!-- omit in toc -->
# Exercices Manipulation du DOM

Voici quelques exercices simples pour apprendre à manipuler le DOM en javascript.

<!-- omit in toc -->
## Légende des difficultés

Facile: 😄
Modéré: 😊
Exigeant: 😅
Épineux: 😰
Impossible?: 😡

<!-- omit in toc -->
## Liste des exercices

- [😄 Exercice 1 : Sélectionner et Modifier un Élément](#-exercice-1--sélectionner-et-modifier-un-élément)
- [😄 Exercice 2 : Ajouter un Élément au DOM](#-exercice-2--ajouter-un-élément-au-dom)
- [😄 Exercice 3 : Modifier une Classe d'Élément](#-exercice-3--modifier-une-classe-délément)
- [😊 Exercice 4 : Remplacer un Élément](#-exercice-4--remplacer-un-élément)
- [😊 Exercice 5 : Insérer un Élément à une Position Spécifique](#-exercice-5--insérer-un-élément-à-une-position-spécifique)
- [😊 Exercice 6 : Supprimer un Élément](#-exercice-6--supprimer-un-élément)

<!-- omit in toc -->
## :memo: Objectifs

- Réaliser ses premiers scripts qui manipulent le DOM en JavaScript en utilisant la théorie déjà vue
- Suivre des consignes précises

<!-- omit in toc -->
## :white_check_mark: Evaluations

- Respect des consignes
  - Le script présente tous les éléments demandés
  - Le script est fonctionnel
- La syntaxe est correcte
- L'indentation est correcte

<!-- omit in toc -->
## 🗒️ Conseil d'utilisation

Comme ce sont des petits exercices, pas besoin de créer un dossier et fichier pour chacun. Faites le premier, voyez si ça fonctionne et puis continuer avec le suivant et supprimer le code du précédent (ou non). Si ça ne fonctionne pas, demandez de l'aide ou une explication!

**Vous pouvez également lire uniquement l'objectif de l'exercice et essayer de trouver la solution par vous même plutôt que de suivre le pas à pas!**

## 😄 Exercice 1 : Sélectionner et Modifier un Élément

> Sujets : variables, sélection, modification

**Objectif**

Sélectionne le paragraphe et modifie son contenu pour qu'il affiche : "Paragraphe modifié via JavaScript."

```html
<body>
  <h1>Bienvenue sur ma page</h1>
  <p>Ceci est un paragraphe.</p>
</body>
```

## 😄 Exercice 2 : Ajouter un Élément au DOM

> Sujets : variables, sélection, ajout

**Objectif**

 Créer un nouvel élément `<p>` avec le texte **"Ceci est un nouveau paragraphe"**, puis de l'ajouter à l'intérieur de la div avec l'ID `conteneur`.

```html
<body>
  <div id="conteneur"></div>
</body>
```

## 😄 Exercice 3 : Modifier une Classe d'Élément

> Sujets : variables, sélection, modification classe

**Objectif**

Sélectionner la div avec la classe `box` et d'ajouter une nouvelle classe `highlight` pour la styliser différemment. Tu peux créer un fichier style.css pour tester!

```html
<body>
  <div class="box"></div>
</body>
```

## 😊 Exercice 4 : Remplacer un Élément

> Sujets : variables, sélection, remplacer

**Objectif**

Sélectionner le paragraphe existant dans le conteneur et de le remplacer par une nouvelle div contenant le texte "Nouveau contenu".

```html
<body>
  <div id="conteneur">
    <p>Paragraphe à remplacer</p>
  </div>
</body>
```

## 😊 Exercice 5 : Insérer un Élément à une Position Spécifique

> Sujets : variables, sélection, ajouter

**Objectif**

Créer un nouvel élément `<li>` avec le texte "Élément 1.5" et de l'insérer entre "Élément 1" et "Élément 2".

```html
<body>
  <ul id="liste">
    <li>Élément 1</li>
    <li>Élément 2</li>
    <li>Élément 3</li>
  </ul>
</body>
```

## 😊 Exercice 6 : Supprimer un Élément

> Sujets : variables, sélection, supprimer

**Objectif**

Supprimer l'élément "Élément 2" de la liste.

```html
<body>
  <ul id="liste">
    <li>Élément 1</li>
    <li>Élément 2</li>
    <li>Élément 3</li>
  </ul>
</body>
```
