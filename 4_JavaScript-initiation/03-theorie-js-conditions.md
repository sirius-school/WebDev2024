<!-- omit in toc -->
# JavaScript - Les conditions

Les conditions permettent d’exécuter des portions de code en fonction de certaines conditions définies par des expressions logiques. Ces expressions sont généralement des comparaisons entre des variables et des valeurs. Les conditions sont indispensables pour la prise de décision dans un programme.

<!-- omit in toc -->
## Table des matières

- [Le bloc if](#le-bloc-if)
- [Le bloc else](#le-bloc-else)
- [Le bloc else if](#le-bloc-else-if)
- [Comparaisons et opérateurs logiques dans les conditions](#comparaisons-et-opérateurs-logiques-dans-les-conditions)
  - [Opérateurs de comparaison](#opérateurs-de-comparaison)
  - [Opérateurs logiques](#opérateurs-logiques)
- [La condition ternaire](#la-condition-ternaire)
- [Le switch](#le-switch)
- [Conclusion](#conclusion)

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

Les conditions sont généralement basées sur des comparaisons. Voici les principaux opérateurs de comparaison en JavaScript que l'on a déjà vu dans le [cours précédent](./01-theorie-js-bases.md#opérateurs), voici un rappel :

- == : égal à (vérifie l’égalité des valeurs sans tenir compte du type)
- === : strictement égal (vérifie l’égalité des valeurs et des types)
- != : différent de
- !== : strictement différent de
- \> : plus grand que
- < : plus petit que
- \>= : supérieur ou égal à
- <= : inférieur ou égal à

### Opérateurs logiques

Les opérateurs logiques permettent de combiner plusieurs conditions :

- && : ET logique (les deux conditions doivent être vraies)
- || : OU logique (au moins une des conditions doit être vraie)
- ! : NON logique (inverse une condition)

<!-- omit in toc -->
#### Exemple avec && (ET logique)

```js
let age = 25;
let citoyen = true;

if (age >= 18 && citoyen === true) {
    console.log("Vous pouvez voter.");
}
```

> Ici, les deux conditions doivent être vraies pour que le message "Vous pouvez voter." soit affiché.

<!-- omit in toc -->
#### Exemple avec || (OU logique)

```js
let age = 16;

if (age < 18 || age > 65) {
    console.log("Vous avez droit à une réduction.");
}
```

> Ici, si l'une des deux conditions est vraie (soit l'âge est inférieur à 18, soit il est supérieur à 65), alors le message "Vous avez droit à une réduction." sera affiché.

<!-- omit in toc -->
#### Exemple avec ! (NON logique) 

```js
let majeur = false;

if (!majeur) {
    console.log("Vous êtes mineur.");
}
```

> Dans cet exemple, !majeur signifie "si majeur est faux". Donc, le message "Vous êtes mineur." sera affiché.

## La condition ternaire

Il existe une syntaxe plus courte pour les conditions, il s'agit de l'opérateur ternaire. Il permet de faire une condition en une seule ligne.

<!-- omit in toc -->
### Syntaxe

```js
condition ? codeSiVrai : codeSiFaux;
```

<!-- omit in toc -->
### Exemple

```js
let age = 20;
let statut = age >= 18 ? "majeur" : "mineur";

console.log(statut); // Affiche "majeur"
```

## Le switch

Le switch est une autre manière de gérer plusieurs conditions. Il est utile quand tu as plusieurs cas spécifiques à vérifier, souvent sur une seule variable.

<!-- omit in toc -->
### Syntaxe

```js
switch (expression) {
    case valeur1:
        // Code si expression === valeur1
        break;
    case valeur2:
        // Code si expression === valeur2
        break;
    default:
        // Code si aucune des valeurs ne correspond
}
```

<!-- omit in toc -->
### Exemple

```js
let jour = 3;

switch (jour) {
    case 1:
        console.log("Lundi");
        break;
    case 2:
        console.log("Mardi");
        break;
    case 3:
        console.log("Mercredi");
        break;
    default:
        console.log("Jour inconnu");
}
```

> Dans cet exemple, jour vaut 3, donc le message "Mercredi" sera affiché.

## Conclusion

Les conditions sont essentielles pour la prise de décision dans tout programme. Voici un résumé des principaux points :

- Le **bloc if** exécute un code si une condition est vraie.
- Le **bloc else** fournit une alternative si la condition est fausse.
- Le **bloc else if** permet de gérer plusieurs conditions.
- Les **opérateurs de comparaison** et **logiques** permettent de formuler des conditions complexes.
- L'**opérateur ternaire** offre une syntaxe concise pour les petites conditions.
- Le **switch** est une structure alternative utile lorsque tu as plusieurs cas possibles sur une même variable.
