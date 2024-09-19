<!-- omit in toc -->
# JavaScript - Les fonctions

Maintenant qu'on a vu comment créer un peu de logique de programmation, on va voir que tout cela peu être contenu dans une fonction pour pouvoir l'utiliser à plusieurs endroits ou de différentes manière.

<!-- omit in toc -->
## Table des matières

- [Introduction aux fonctions](#introduction-aux-fonctions)
- [Exemple simple d’une fonction](#exemple-simple-dune-fonction)
  - [Appeler une fonction](#appeler-une-fonction)
- [Fonctions avec paramètres](#fonctions-avec-paramètres)
- [Retourner une valeur avec return](#retourner-une-valeur-avec-return)
- [Fonctions avec des valeurs par défaut](#fonctions-avec-des-valeurs-par-défaut)
- [Les fonctions anonymes](#les-fonctions-anonymes)
- [Les fonctions fléchées (arrow functions)](#les-fonctions-fléchées-arrow-functions)
- [Portée des variables dans les fonctions](#portée-des-variables-dans-les-fonctions)

## Introduction aux fonctions

Une fonction est un bloc de code conçu pour effectuer une tâche spécifique. Les fonctions nous permettent de réutiliser du code, de rendre notre programme plus structuré et de mieux organiser les instructions.

<!-- omit in toc -->
### Syntaxe

```js
function nomDeLaFonction(parametre1, parametre2) {
    // Bloc de code
}
```

- **function** : Mot-clé pour déclarer une fonction.
- **nomDeLaFonction** : Nom de la fonction, choisi par le développeur.
- **parametre1**, **parametre2** : (Facultatif) Paramètres que la fonction peut accepter pour effectuer ses opérations.
- **Bloc de code**: Le code à exécuter lorsque la fonction est appelée.

## Exemple simple d’une fonction

```js
function direBonjour() {
    console.log("Bonjour tout le monde !");
}
```

> Dans cet exemple, la fonction direBonjour n’accepte pas de paramètres. Elle affiche simplement “Bonjour tout le monde !” quand elle est appelée.

### Appeler une fonction

Pour exécuter une fonction, il suffit de l’appeler en utilisant son nom suivi de parenthèses :

```js
direBonjour(); // Affiche "Bonjour tout le monde !" dans la console"
```

## Fonctions avec paramètres

Les fonctions peuvent également recevoir des informations (appelées paramètres) pour travailler avec. C'est ce qu'on place entre les parenthèses et qui devient utilisable dans la logique de notre fonction.

```js
function saluer(nom) {
    console.log("Bonjour, " + nom + " !");
}

saluer("Alice"); // Affiche "Bonjour, Alice !"
saluer("Bob");   // Affiche "Bonjour, Bob !"
```

> Dans cet exemple, la fonction saluer accepte un paramètre nom. Ce paramètre est utilisé pour personnaliser le message de salutation dans la console.

## Retourner une valeur avec return

Les fonctions peuvent aussi retourner une valeur en utilisant le mot-clé return. Cela signifie que la fonction renvoie un résultat que l’on peut utiliser ailleurs dans le programme.

```js
function addition(a, b) {
    return a + b;
}

let resultat = addition(5, 3);
console.log(resultat); // Affiche 8
```

> Ici, la fonction addition retourne la somme des deux paramètres. Cette valeur est ensuite stockée dans la variable `resultat` et affichée.
>
> La différence c'est qu'on a pas incorporé notre `console.log` dans notre fonction, ainsi on peut utiliser la fonction dans n'importe quelle autre logique. Comme par exemple une autre fonction

```js
function addition(a, b) {
    return a + b;
}

function soustraction(c) {
    console.log(addition(5, 3) - c );
}

soustraction(5) // Affiche 3
```

> C'est comme cela qu'on peut développer des applications de plus en plus complexe tout en restant logique.

## Fonctions avec des valeurs par défaut

Il est possible de donner des valeurs par défaut aux paramètres si jamais aucun argument n’est passé lors de l’appel de la fonction.

```js
function multiplier(a, b = 2) {
    return a * b;
}

console.log(multiplier(5));   // Affiche 10 (5 * 2)
console.log(multiplier(5, 3)); // Affiche 15 (5 * 3)
```

> Dans cet exemple, si aucun deuxième argument n’est fourni, la valeur par défaut de b sera 2.

## Les fonctions anonymes

Les fonctions anonymes sont des fonctions qui n’ont pas de nom. Elles sont souvent utilisées comme valeurs de variables ou comme arguments passés à d’autres fonctions.

```js
let direAuRevoir = function() {
    console.log("Au revoir !");
};

direAuRevoir(); // Affiche "Au revoir !"
```

## Les fonctions fléchées (arrow functions)

Les fonctions fléchées sont une autre manière d’écrire des fonctions de façon plus concise, en particulier pour les fonctions courtes.

```js
// Syntaxe complète
const multiplier = (a, b) => {
    return a * b;
};

// Équivalent
function multiplier(a, b) {
    return a * b;
}

// Simplification
const multiplier = (a, b) => a * b;
```

## Portée des variables dans les fonctions

La portée (ou scope) d’une variable fait référence à la partie du code où la variable est accessible.

- Les variables définies à l’intérieur d’une fonction sont locales à cette fonction et ne peuvent pas être accédées depuis l’extérieur.
- Les variables définies à l’extérieur d’une fonction sont globales et accessibles dans tout le programme.

```js
function calculerSomme() {
    let x = 10; // Variable locale à la fonction
    return x + 5;
}

console.log(calculerSomme()); // Affiche 15
console.log(x); // Erreur ! 'x' n'est pas accessible ici car elle est définie dans la fonction.
```
