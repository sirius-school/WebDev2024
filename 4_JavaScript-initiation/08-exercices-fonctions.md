<!-- omit in toc -->
# Exercices fonctions JS

Voici quelques exercices simples pour apprendre à manipuler les fonctions en javascript.

<!-- omit in toc -->
## Légende des difficultés

Facile: 😄
Modéré: 😊
Exigeant: 😅
Épineux: 😰
Impossible?: 😡

<!-- omit in toc -->
## Liste des exercices

- [😄 Exercice 1 : Calculer l’aire d’un rectangle](#-exercice-1--calculer-laire-dun-rectangle)
- [😄 Exercice 2 : Conversion de température](#-exercice-2--conversion-de-température)
- [😊 Exercice 3 : Déterminer si un nombre est pair](#-exercice-3--déterminer-si-un-nombre-est-pair)
- [😊 Exercice 4 : Calculer la factorielle d’un nombre](#-exercice-4--calculer-la-factorielle-dun-nombre)
- [😅 Exercice 5 : Trouver le plus grand nombre dans un tableau](#-exercice-5--trouver-le-plus-grand-nombre-dans-un-tableau)
- [😰 Exercice 6 : Compter les voyelles dans une chaîne de caractères](#-exercice-6--compter-les-voyelles-dans-une-chaîne-de-caractères)
- [😊 Exercice 7 : Doubler un nombre avec une fonction fléchée](#-exercice-7--doubler-un-nombre-avec-une-fonction-fléchée)

<!-- omit in toc -->
## :memo: Objectifs

- Réaliser ses premières fonctions JavaScript en utilisant la théorie déjà vue
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

## 😄 Exercice 1 : Calculer l’aire d’un rectangle

> Sujets: variables, fonctions, opérateurs arithmétique

**Objectif**

Utiliser une fonction avec des paramètres et un retour de valeur.

**Énoncé**

Créez une fonction `calculerAireRectangle` qui prend en paramètres la largeur et la hauteur d’un rectangle et retourne l’aire du rectangle.

```js
console.log(calculerAireRectangle(5, 10)); // Affiche 50
console.log(calculerAireRectangle(8, 3));  // Affiche 24
```

**Indices**

- Si vous ne savez plus comment on calcule l'aire d'un rectangle, faites une petite recherche internet. C'est super simple!

## 😄 Exercice 2 : Conversion de température

> Sujets: variables, fonctions, opérateurs arithmétique

**Objectif**

Utiliser les fonctions pour effectuer une conversion avec des paramètres.

**Énoncé**

Créez une fonction `convertirEnCelsius` qui prend une température en Fahrenheit et la convertit en Celsius.

```js
console.log(convertirEnCelsius(32));  // Affiche 0
console.log(convertirEnCelsius(68));  // Affiche 20
```

**Indices**

- Formule : Celsius = (Fahrenheit - 32) * 5/9.

## 😊 Exercice 3 : Déterminer si un nombre est pair

> Sujets: variables, fonctions, opérateurs arithmétique

**Objectif**

Utiliser une fonction pour évaluer une condition.

**Énoncé**

Créez une fonction `estPair` qui prend un nombre en paramètre et retourne true si le nombre est pair, et false sinon.

```js
console.log(estPair(4)); // Affiche true
console.log(estPair(7)); // Affiche false
```

## 😊 Exercice 4 : Calculer la factorielle d’un nombre

> Sujets: variables, fonctions, opérateurs arithmétique

**Objectif**
Utiliser une boucle à l’intérieur d’une fonction pour effectuer une opération répétée.

**Énoncé**
Créez une fonction `factorielle` qui prend un nombre entier positif en paramètre et retourne la factorielle de ce nombre.
La factorielle d’un nombre  `n`  est le produit de tous les entiers de 1 à `n` . Par exemple, la factorielle de 5 est 5 × 4 × 3 × 2 × 1 = 120.

```js
console.log(factorielle(5)); // Affiche 120
console.log(factorielle(3)); // Affiche 6
```

## 😅 Exercice 5 : Trouver le plus grand nombre dans un tableau

> Sujets: variables, fonctions, opérateurs arithmétique, tableau

**Objectif**  

Manipuler les tableaux et utiliser une fonction pour parcourir des éléments.

**Énoncé**

Créez une fonction `trouverMax` qui prend un tableau de nombres en paramètre et retourne le plus grand nombre du tableau.

```js
console.log(trouverMax([3, 7, 2, 5, 10]));  // Affiche 10
console.log(trouverMax([1, 20, 3, 14]));    // Affiche 20
```

## 😰 Exercice 6 : Compter les voyelles dans une chaîne de caractères

> Sujets: variables, fonctions, opérateurs arithmétique, tableau, include()

**Objectif**

Parcourir une chaîne de caractères et utiliser des conditions pour filtrer les voyelles.

**Énoncé**

Créez une fonction compterVoyelles qui prend une chaîne de caractères en paramètre et retourne le nombre de voyelles (a, e, i, o, u) présentes dans la chaîne.

```js
console.log(compterVoyelles("Bonjour tout le monde"));  // Affiche 8
console.log(compterVoyelles("JavaScript"));             // Affiche 3
```

**Indices**

- Stocker les voyelles dans un tableau
- Utilisez la fonction [includes()](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array/includes) pour vérifier si les voyelles sont présentes dans le tableau qu'on passe en paramètres

## 😊 Exercice 7 : Doubler un nombre avec une fonction fléchée

> Sujets: variables, fonctions

**Objectif**

Utiliser une **fonction fléchée** pour retourner le double d’un nombre.

**Énoncé**

Créez une **fonction fléchée** `doubler` qui prend un nombre en paramètre et retourne le double de ce nombre.

```js
console.log(doubler(5));  // Affiche 10
console.log(doubler(7));  // Affiche 14
```

**Indices**

- Syntaxe d'une fonction fléchée: `(paramètre) => expression`