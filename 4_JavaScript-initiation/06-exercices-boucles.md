<!-- omit in toc -->
# Exercices boucles JS

Voici quelques exercices simples pour apprendre à manipuler un peu tout le javascript qu'on vient de voir.

<!-- omit in toc -->
## Légende des difficultés

Facile: 😄
Modéré: 😊
Exigeant: 😅
Épineux: 😰
Impossible?: 😡

<!-- omit in toc -->
## Liste des exercices

- [😊 Exercice 1 : Compter de 1 à 10 avec une boucle for](#-exercice-1--compter-de-1-à-10-avec-une-boucle-for)
- [😊 Exercice 2 : Afficher les nombres pairs de 0 à 20](#-exercice-2--afficher-les-nombres-pairs-de-0-à-20)
- [😊 Exercice 3 : Compter à rebours](#-exercice-3--compter-à-rebours)
- [😅 Exercice 4 : Somme des nombres de 1 à 100](#-exercice-4--somme-des-nombres-de-1-à-100)
- [😅 Exercice 5 : Afficher les éléments d'un tableau](#-exercice-5--afficher-les-éléments-dun-tableau)
- [😰 Exercice 6 : Boucle imbriquée (tables de multiplication)](#-exercice-6--boucle-imbriquée-tables-de-multiplication)
- [😰 Exercice 7 : Trouver un élément dans un tableau](#-exercice-7--trouver-un-élément-dans-un-tableau)
- [😰 Exercice 8 : FizzBuzz](#-exercice-8--fizzbuzz)
- [😰 Exercice 9 : Jeu de devinette (avec plusieurs réponses)](#-exercice-9--jeu-de-devinette-avec-plusieurs-réponses)

<!-- omit in toc -->
## :memo: Objectifs

- Réaliser ses premier script JavaScript en utilisant la théorie déjà vue
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

## 😊 Exercice 1 : Compter de 1 à 10 avec une boucle for

> Sujets: console, variables, boucles

**Objectif** : Écris un programme qui utilise une boucle `for` pour afficher les nombres de 1 à 10 dans la console.

```js
// Résultat attendu : 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
```

**Indices** :

- Comprendre la boucle for en itérant un nombre défini de fois.

## 😊 Exercice 2 : Afficher les nombres pairs de 0 à 20

> Sujets: console, variables, boucles, conditions

**Objectif** : Utilise une boucle `while` pour afficher tous les nombres pairs entre 0 et 20 dans la console.

```js
// Résultat attendu : 0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20
```

**Indices** :

- Utiliser une boucle while.
- Comprendre la condition pour les nombres pairs (i.e. un nombre divisible par 2).

## 😊 Exercice 3 : Compter à rebours

> Sujets: console, variables, boucles

**Objectif** : Écris un programme qui utilise une boucle `do...while` pour afficher un compte à rebours de 10 à 1.

```js
// Résultat attendu : 10, 9, 8, 7, 6, 5, 4, 3, 2, 1
```

**Indices** :

- Utiliser la boucle do...while pour garantir au moins une exécution.
- Décrémenter la variable à chaque itération.

## 😅 Exercice 4 : Somme des nombres de 1 à 100

> Sujets: console, variables, boucles

**Objectif** : Crée une boucle qui calcule la somme des nombres de 1 à 100 et affiche le résultat.

```js
// Résultat attendu : 5050 (la somme des nombres de 1 à 100)
```

**Indices** :

- Comprendre l'accumulation dans une boucle.
- Utiliser une variable pour stocker la somme.

## 😅 Exercice 5 : Afficher les éléments d'un tableau

> Sujets: console, variables, boucles, array

**Objectif** : Écris un programme qui utilise une boucle `for...of` pour parcourir un tableau d'animaux et afficher chaque animal dans la console.

```js
const animaux = ["chien", "chat", "lapin", "oiseau"];
// Résultat attendu : chien, chat, lapin, oiseau
```

## 😰 Exercice 6 : Boucle imbriquée (tables de multiplication)

> Sujets: console, variables, boucles

**Objectif** : Écris un programme qui utilise deux boucles imbriquées pour afficher les tables de multiplication de 1 à 5.

```js
// Résultat attendu : 
// 1 x 1 = 1
// 1 x 2 = 2
// ...
// 5 x 5 = 25
```

**Indices** :

- Comprendre l'utilisation de boucles imbriquées.
- Utiliser une variable pour stocker la somme.

> :bulb: Pour pouvoir écrire facilement le résultat il va falloir utiliser ce qu'on appel un [template literal](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Template_literals). C'est une manière d'écrire du texte tout en incorporant des expressions (autrement dit, nos variables dans ce cas-ci).
>
> Voici un exemple: **console.log(\`${x} x ${y} = ${x*y}\`)**

## 😰 Exercice 7 : Trouver un élément dans un tableau

> Sujets: console, variables, boucles, array

**Objectif** : Écris un programme qui utilise une boucle pour rechercher si un certain nombre est présent dans un tableau. Si le nombre est trouvé, affiche un message disant qu'il est présent. Sinon, affiche un message disant qu'il ne l'est pas.

```js
const nombres = [10, 20, 30, 40, 50];
const nombreCherche = 30; 
// Résultat attendu : 30 est présent dans le tableau.
```

**Indices** :

- Utiliser une boucle pour parcourir un tableau.
- Utiliser une condition à l'intérieur de la boucle.
- Utiliser une variable `trouve` pour savoir si le nombre à été trouvé ou pas.
- Utiliser l'instruction `break` pour arrêter la boucle si le nombre est trouvé.

## 😰 Exercice 8 : FizzBuzz

> Sujets: console, variables, boucles

**Objectif** : Écris un programme qui affiche les nombres de 1 à 30. Mais pour les multiples de 3, affiche "Fizz", pour les multiples de 5, affiche "Buzz", et pour les multiples de 3 et 5, affiche "FizzBuzz".

```js
// Résultat attendu :
// 1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, FizzBuzz, etc.
```

**Indices** :

- Utiliser une boucle for.
- Manipuler des conditions multiples dans la boucle.
- Utiliser le modulo (%) pour vérifier si un chiffre est un multiple ou non.
- Utiliser plusieurs `else if`

## 😰 Exercice 9 : Jeu de devinette (avec plusieurs réponses)

> Sujets: console, variables, boucles, prompt, literal

**Objectif** : Reprend [l'exercice - jeu de devinette](./04-exercices-conditions.md#-exercice-5--jeu-de-devinette) qu'on a fait précédement. Cette-fois ci, fais en sorte que le comparaison soit affiché dans le prompt de l'utilisateur et qu'il puis essayer à nouveau de deviner le même chiffre.

**Indices** :

- Utiliser une boucle while.
- Créer une variable `résultat` pour stocker "Trop petit" ou "Trop grand".
- Dans le prompt qui redemande à l'utilisateur de choisir un nouveau nombre, indique la valeur de la variable résultat grâce à un `Template literals`. Exemple: \`${resultat}. Essayez encore, chiffre de 1 à 10 (ou appuyez sur Annuler pour quitter)\`