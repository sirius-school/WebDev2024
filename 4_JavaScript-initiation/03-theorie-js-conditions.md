<!-- omit in toc -->
# JavaScript - Les boucles

Les conditions permettent d’exécuter des portions de code en fonction de certaines conditions définies par des expressions logiques. Ces expressions sont généralement des comparaisons entre des variables et des valeurs. Les conditions sont indispensables pour la prise de décision dans un programme.

<!-- omit in toc -->
## Table des matières

- [Le bloc if](#le-bloc-if)
- [Le bloc else](#le-bloc-else)
- [Le bloc else if](#le-bloc-else-if)
- [Comparaisons et opérateurs logiques dans les conditions](#comparaisons-et-opérateurs-logiques-dans-les-conditions)
  - [Opérateurs de comparaison](#opérateurs-de-comparaison)

## Le bloc if

La condition la plus basique est le bloc if. Il permet d’exécuter du code seulement si une condition est vraie. On écrit simplement le mot clé `if` suivi de parenthèse dans lesquelles on va y placer notre condition, puis à la suite on aura des accolades pour le code qu'on doit exécuter si la condition est vraie.

<!-- omit in toc -->
### Syntaxe

```js
if (condition) {
    // Code exécuté si la condition est vraie
}
```

<!-- omit in toc -->
### Exemple

```js
let age = 18;

if (age >= 18) {
    console.log("Vous êtes majeur.");
}
```

## Le bloc else

Le bloc else permet de définir une alternative qui sera exécutée si la condition du if est fausse.

<!-- omit in toc -->
### Syntaxe

```js
if (condition) {
    // Code exécuté si la condition est vraie
} else {
    // Code exécuté si la condition est fausse
}
```

<!-- omit in toc -->
### Exemple

```js
let age = 16;

if (age >= 18) {
    console.log("Vous êtes majeur.");
} else {
    console.log("Vous êtes mineur.");
}
```

## Le bloc else if

Le bloc else if permet d’ajouter des conditions supplémentaires. Il est utilisé lorsque nous avons plusieurs conditions à tester.

<!-- omit in toc -->
### Syntaxe

```js
if (condition1) {
    // Code exécuté si condition1 est vraie
} else if (condition2) {
    // Code exécuté si condition2 est vraie et condition1 est fausse
} else {
    // Code exécuté si aucune des conditions n'est vraie
}
```

<!-- omit in toc -->
### Exemple

```js
let note = 15;

if (note >= 18) {
    console.log("Excellent !");
} else if (note >= 12) {
    console.log("Bien !");
} else {
    console.log("Peut mieux faire.");
}
```

## Comparaisons et opérateurs logiques dans les conditions

### Opérateurs de comparaison

Les conditions sont généralement basées sur des comparaisons. Voici les principaux opérateurs de comparaison en JavaScript que l'on a déjà vu dans le [cours précédent](./01-theorie-js-bases.md#opérateurs) :

- == : égal à (vérifie l’égalité des valeurs sans tenir compte du type)
- === : strictement égal (vérifie l’égalité des valeurs et des types)
- != : différent de
- !== : strictement différent de
- \> : plus grand que
- < : plus petit que
- \>= : supérieur ou égal à
- <= : inférieur ou égal à