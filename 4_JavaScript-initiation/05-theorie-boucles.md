<!-- omit in toc -->
# JavaScript - Les boucles

Les boucles sont une des structures fondamentales de la programmation, permettant d’exécuter plusieurs fois un bloc de code. JavaScript offre plusieurs types de boucles, chacune ayant ses particularités et son utilité selon le contexte. Les boucles permettent d’automatiser des tâches répétitives, telles que l’affichage de plusieurs valeurs ou l’itération à travers des collections de données.

![loop](./img/05/loop2.gif)

<!-- omit in toc -->
## Table des matières

- [Principe général d’une boucle](#principe-général-dune-boucle)
- [La boucle while](#la-boucle-while)
- [La boucle do...While](#la-boucle-dowhile)
- [La boucle for](#la-boucle-for)
- [La boucle for...of](#la-boucle-forof)
- [La boucle for...in](#la-boucle-forin)
- [Les instructions break et continue](#les-instructions-break-et-continue)
- [Les boucles imbriquées](#les-boucles-imbriquées)
- [Différences entre les boucles](#différences-entre-les-boucles)
- [Conclusion](#conclusion)

## Principe général d’une boucle

L’idée derrière une boucle est de répéter une série d’instructions tant qu’une condition est vérifiée. Une boucle se compose de trois parties principales :

- Initialisation : C’est ici qu’on initialise une ou plusieurs variables de contrôle qui régulent la boucle.
- Condition : Tant que cette condition est vraie, la boucle continue de s’exécuter.
- Incrémentation/Décrémentation : À la fin de chaque itération, la variable de contrôle est modifiée pour que la condition puisse finir par être fausse.

<!-- omit in toc -->
### Exemple de syntaxe

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

> Dans cet exemple:
> `let i = 0` est l'initialisation.
> `i < 5` est la condition.
> `i++` est l'incrémentation/décrémentation.

## La boucle while

La boucle while exécute un bloc de code tant qu’une condition est vraie. Attention, si votre condition de fin n'est pas correcte, vous pouvez vous retrouver avec une boucle infinie!

<!-- omit in toc -->
### Syntaxe

```js
while (condition) {
  // bloc de code à exécuter tant que la condition est vraie
}
```

<!-- omit in toc -->
### Exemple

```js
let i = 0;
while (i < 5) {
  console.log("Valeur de i : " + i);
  i++; // Incrémentation de i pour éviter une boucle infinie
}
```

> Dans cet exemple, la boucle continue tant que la valeur de i est inférieure à 5. À chaque itération, la valeur de i est affichée, puis i est incrémenté de 1.

## La boucle do...While

La boucle do...while est similaire à la boucle while, à la différence près qu’elle exécute le bloc de code au moins une fois, même si la condition est fausse dès le début.

<!-- omit in toc -->
### Syntaxe

 ```js
do {
  // bloc de code à exécuter
} while (condition);
```

<!-- omit in toc -->
### Exemple

```js
let i = 0;
do {
  console.log("Valeur de i : " + i);
  i++;
} while (i < 5);
```

## La boucle for

La boucle for est la plus utilisée en JavaScript lorsqu’on sait à l’avance combien de fois on veut répéter un bloc de code. Elle combine l’initialisation, la condition et l’incrémentation en une seule ligne.

<!-- omit in toc -->
### Syntaxe

```js
for (initialisation; condition; incrémentation) {
  // bloc de code à exécuter
}
```

<!-- omit in toc -->
### Exemple

```js
for (let i = 0; i < 5; i++) {
  console.log("Valeur de i : " + i);
}
```

> Dans cet exemple :
>
> **Initialisation** : let i = 0; (on initialise la variable i à 0)
>
> **Condition** : i < 5; (la boucle continue tant que i est inférieur à 5)
> 
> **Incrémentation** : i++ (après chaque itération, i est incrémenté de 1)

## La boucle for...of

La boucle for...of permet d’itérer sur les éléments d’un tableau, une chaîne de caractères, ou d’autres objets itérables.

<!-- omit in toc -->
### Syntaxe

```js
for (const élément of collection) {
  // bloc de code à exécuter pour chaque élément
}
```

<!-- omit in toc -->
### Exemple

```js
let fruits = ["pomme", "banane", "orange"];
for (const fruit of fruits) {
  console.log(fruit);
}
```

> Dans cet exemple, la boucle for...of itère à travers chaque élément du tableau fruits et affiche chaque fruit dans la console.

## La boucle for...in

La boucle for...in permet d’itérer sur les propriétés énumérables d’un objet.

<!-- omit in toc -->
### Syntaxe

```js
for (const clé in objet) {
  // bloc de code à exécuter pour chaque propriété
}
```

<!-- omit in toc -->
### Exemple

```js
const voiture = { marque: "Toyota", modèle: "Corolla", année: 2020 };
for (const propriété in voiture) {
  console.log(propriété + " : " + voiture[propriété]);
}
```

> Dans cet exemple, la boucle for...in parcourt chaque propriété de l’objet voiture et affiche son nom et sa valeur.

## Les instructions break et continue

**break** : Cette instruction permet de sortir immédiatement de la boucle, même si la condition n’est pas encore fausse.

<!-- omit in toc -->
### Exemple

```js
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break; // La boucle s'arrête dès que i vaut 5
  }
  console.log(i);
}
```

**continue** : Cette instruction permet de sauter à l’itération suivante sans exécuter le reste du bloc de code.

<!-- omit in toc -->
### Exemple

```js
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    continue; // On saute l'itération quand i vaut 5
  }
  console.log(i);
}
```

## Les boucles imbriquées

Il est possible d’imbriquer des boucles, c’est-à-dire d’avoir une boucle à l’intérieur d’une autre boucle. Cela peut être utile pour parcourir des structures de données en deux dimensions, comme des tableaux de tableaux (matrices).

<!-- omit in toc -->
### Exemple

```js
let matrice = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

for (let i = 0; i < matrice.length; i++) {
  for (let j = 0; j < matrice[i].length; j++) {
    console.log(matrice[i][j]);
  }
}
```

> Dans cet exemple on va d'abord faire une boucle pour parcourir  le premier tableau en fonction de sa longueur (3). A chaque itération on va reparcourir le nouveau tableau autant de fois que sa longueur et console.log la valeur qu'on a à chaque position.

## Différences entre les boucles

- **while** et **do…while** : utiles quand on ne sait pas combien d’itérations sont nécessaires à l’avance.
- **for** : utilisé lorsque le nombre d’itérations est déterminé dès le départ.
- **for…of** : spécialement conçu pour itérer sur des collections (tableaux, chaînes).
- **for…in** : utilisé pour parcourir les propriétés d’un objet.

## Conclusion

Les boucles sont des outils indispensables pour effectuer des tâches répétitives en JavaScript. Il est important de bien choisir le type de boucle en fonction du problème à résoudre pour optimiser l’efficacité et la lisibilité de votre code.

N’oubliez pas d’utiliser les instructions break et continue avec parcimonie, car elles peuvent rendre votre code plus difficile à comprendre si elles sont utilisées de manière excessive.

![loop](./img/05/loop.gif)