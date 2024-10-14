<!-- omit in toc -->
# Les tableaux et leurs méthodes en JavaScript

On a déjà vu ce qu'étais un tableau en JavaScript et comment on pouvait le parcourir. Mais cela reste très basique et n'a pas encore de réel utilité.

Voyons comment manipuler un peu plus ces tableaux pour pouvoir gérer nos données.

<!-- omit in toc -->
## Table des matières

- [Rappel tableau (array) en JavaScript](#rappel-tableau-array-en-javascript)
- [Méthodes de base des Tableaux](#méthodes-de-base-des-tableaux)
  - [push()](#push)
  - [pop()](#pop)
  - [unshift()](#unshift)
  - [shift()](#shift)
- [Autres méthodes utiles des tableaux](#autres-méthodes-utiles-des-tableaux)
  - [length](#length)
  - [indexOf()](#indexof)
  - [includes()](#includes)
  - [splice()](#splice)
  - [slice()](#slice)
  - [join()](#join)
- [Itérations sur un Tableau](#itérations-sur-un-tableau)
  - [forEach()](#foreach)
  - [map()](#map)
  - [filter()](#filter)
  - [reduce()](#reduce)

## Rappel tableau (array) en JavaScript

Un tableau est une structure de données qui permet de stocker plusieurs valeurs dans une seule variable. Ces valeurs peuvent être de différents types : des nombres, des chaînes de caractères, des objets, voire d’autres tableaux (tableaux imbriqués).

```js
// Déclaration d'un tableau
let fruits = ["Pomme", "Banane", "Mangue"];

// Affichage d'un tableau
console.log(fruits); // ["Pomme", "Banane", "Mangue"]

// Accéder à un élément d'un tableau
console.log(fruits[0]); // "Pomme"
```

> :bulb: Rappel: Les indices des tableaux commencent toujours à 0.

## Méthodes de base des Tableaux

Reprenons notre tableaux de fruits et modifions le

```js
let fruits = ["Pomme", "Banane", "Mangue"];
```

### push()

Ajoute un ou plusieurs éléments à la fin d’un tableau.

```js
fruits.push("Orange");
console.log(fruits); // ["Pomme", "Banane", "Mangue", "Orange"]
```

### pop()

Supprime et renvoie le dernier élément du tableau.

```js
let dernier = fruits.pop();
console.log(dernier); // "Orange"
console.log(fruits);  // ["Pomme", "Banane", "Mangue"]
```

### unshift()

Ajoute un ou plusieurs éléments au début d’un tableau.

```js
fruits.unshift("Fraise");
console.log(fruits); // ["Fraise", "Pomme", "Banane", "Mangue"]
```

### shift()

Supprime et renvoie le premier élément du tableau.

```js
let premier = fruits.shift();
console.log(premier); // "Fraise"
console.log(fruits);  // ["Pomme", "Banane", "Mangue"]
```

## Autres méthodes utiles des tableaux

### length

Renvoie la taille du tableau, autrement dit, le nombre d’éléments.

```js
console.log(fruits.length); // 3
```

### indexOf()

Renvoie l’indice de la première occurrence d’un élément. Si l’élément n’est pas trouvé, la méthode renvoie -1.

```js
console.log(fruits.indexOf("Banane")); // 1
```

### includes()

Renvoie `true` si l’élément est présent dans le tableau, sinon `false`.

```js
console.log(fruits.includes("Mangue")); // true
```

### splice()

Permet de supprimer ou d’ajouter des éléments à un tableau.

- Le premier argument est l’indice à partir duquel tu veux commencer la suppression.
- Le second argument est le nombre d’éléments que tu veux supprimer.
- Le troisième argument optionnel sert à indiquer les éléments qu'on veut rajouter à la suite.

```js
let fruits = ["Pomme", "Banane", "Mangue"];
```

```js
// Supprimer 1 élément à partir de l'indice 1
fruits.splice(1, 2);
console.log(fruits); // ["Pomme"]

// Ajouter des éléments à partir de l'indice 1
fruits.splice(1, 0, "Banane", "Kiwi");
console.log(fruits); // ["Pomme", "Banane", "Kiwi"]
```

### slice()

Retourne une partie du tableau sans modifier l’original.

```js
let fruits = ["Pomme", "Banane", "Mangue"];
```

```js
let selection = fruits.slice(1, 3);
console.log(selection); // ["Banane", "Kiwi"]
console.log(fruits);    // ["Pomme", "Banane", "Kiwi", "Mangue"]
```

### join()

Transforme tous les éléments d’un tableau en une seule chaîne de caractères, en utilisant un séparateur.

```js
let chaine = fruits.join(", ");
console.log(chaine); // "Pomme, Banane, Kiwi, Mangue"
```

## Itérations sur un Tableau

### forEach()

Exécute une fonction pour chaque élément du tableau.

```js
fruits.forEach(function(fruit) {
  console.log(fruit);
});
// Affiche :
// Pomme
// Banane
// Kiwi
// Mangue
```

### map()

Crée un nouveau tableau avec les résultats de l’appel d’une fonction sur chaque élément.

```js
let longueurs = fruits.map(function(fruit) {
  return fruit.length;
});
console.log(longueurs); // [5, 6, 4, 6]
```

### filter()

Crée un nouveau tableau avec les éléments qui remplissent une condition.

```js
let fruitsAvecM = fruits.filter(function(fruit) {
  return fruit.includes('m');
});
console.log(fruitsAvecM); // ["Pomme", "Mangue"]
```

### reduce()

Réduit un tableau à une seule valeur, en appliquant une fonction à chaque élément (de gauche à droite).

```js
let totalLength = fruits.reduce(function(total, fruit) {
  return total + fruit.length;
}, 0);
console.log(totalLength); // 21
```
