<!-- omit in toc -->
# Exercices conditions JS

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

- [😊 Exercice 1 : Vérification de l'âge](#-exercice-1--vérification-de-lâge)
- [😅 Exercice 2 : Parité d'un nombre](#-exercice-2--parité-dun-nombre)
- [😊 Exercice 3 : Note d'examen](#-exercice-3--note-dexamen)
- [😰 Exercice 4 : Calcul de la réduction](#-exercice-4--calcul-de-la-réduction)
- [😰 Exercice 5 : Jeu de devinette](#-exercice-5--jeu-de-devinette)

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

## 😊 Exercice 1 : Vérification de l'âge

> Sujets: console, prompt, condition, variables

**Objectif** : Demander à l'utilisateur d'entrer son âge et afficher un message en fonction de l'âge entré.

1. Créez un nouveau document javascript.
2. Créez une variable `age` (number) et ajoutez un prompt qui demandera l'âge du visiteur. Soyez bien sûr de stocker **un nombre** dans cette variable.
3. Ajoutez ensuite une condition `if` pour vérifier si l'âge est inférieur à 18. Dans ce cas affichez "Vous êtes mineur" dans la console.
4. Faites ensuite un `if else` pour vérifier si l'âge est supérieur ou égal à 18 mais inférieur à 65. Il va falloir utiliser un opérateur logique. Ensuite affichez "Vous êtes adulte" dans la console.
5. Puis faites un `else` pour indiquer que la personne est "senior" si son age es égale ou supérieur à 65.

## 😅 Exercice 2 : Parité d'un nombre

> Sujets: console, prompt, condition, variables, modulo, opérateur arithmétique

**Objectif** : Vérifier si un nombre est pair ou impair.

1. Créez une variable `nombre` et ajoutez un prompt. Soyez bien sûr de stocker **un nombre** dans cette variable.
2. Créer une condition qui vérifie si le résultat de la division est égale à 0, si oui, cela veut dire que le nombre est paire, si non, qu'il est impaire. C'est ce qu'on appel le `modulo` et oui c'est dans le cours, mais pas totalement expliqué, il va falloir allez voir sur le net c'est quoi "modulo".
3. Indiquez le résultat dans la console.

**Bonus**: Utiliser `isNaN()`. Cela permet de vérifier que ce que le visiteur à indiqué est bien un nombre. `NaN` veut dire "Not A Number". C'est quelque chose qu'on reverra plus tard, mais si vous êtes chaud vous pouvez vous renseigner sur la [fonction ici](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/isNaN).

## 😊 Exercice 3 : Note d'examen

> Sujets: console, prompt, condition, switch

**Objectif** : Afficher une appréciation en fonction de la note obtenue.

1. Créez une variable `note` et ajoutez un prompt. Soyez bien sûr de stocker **un nombre** dans cette variable.
2. Créez un `switch` pour affichez dans la console un message en fonction de la note obtenue (voir tableau)

| Note | Message| 
| :--- |:------:|
| 16+  | Excellent |
| 16-12  | Bien |
| 11 - 8  | Passable |
| 7-0  | Insuffisant |

## 😰 Exercice 4 : Calcul de la réduction

> Sujets: console, prompt, condition, opérateur arithmétique

**Objectif** : Appliquer une réduction en fonction de l'âge.

1. Créez une variable `age` et ajoutez un prompt demandant l'âge du visiteur. Soyez bien sûr de stocker **un nombre** dans cette variable.
2. Créez une variable `prix` et ajoutez un prompt demandant le prix au visiteur. Soyez bien sûr de stocker **un nombre** dans cette variable.
3. Créez une variable `réduction` qui est égale à 0.
4. Créez une condition qui va appliquez une ristourne en % sur le prix en fonction de l'âge. Pour ce faire, il faut mettre à jour la variable `ristourne` avec la valeur **en décimal** du pourcentage (15% = 0.15). Voir tableau pour la valeur de la réduction
5. Créez une variable `prixFinal` qui va faire le calcul `prix - (prix * réduction)`
6. Affichez le résultat dans la console

| Age | Réduction| 
| :--- |:------:|
| -18  | 10% |
| 18-25  | 5% |
| 60+  | 15% |

**Bonus**: A la fin de la variable `prixFinal` vous pouvez rajouter la fonction `toFixed()` pour arrondir le chiffre obtenu à 2 décimales. [Plus d'info dans la doc](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed)

## 😰 Exercice 5 : Jeu de devinette

> Sujets: console, prompt, condition, opérateur arithmétique, Math.floor

**Objectif** : Deviner un nombre aléatoire.

1. Créez une variable `nombreMystere` et copiez le code suivant comme valeur: `Math.floor(Math.random() * 10) + 1`. Ceci va générer un chiffre aléatoire entre 1 et 10. Pas de panique, vous entendrez encore parler de `Math.floor` plus tard.
2. Créez un prompt dans une variable `nombreDevine` pour demander à votre visiteur un chiffre entre 1 et 10.
3. Vérifier avec des conditions si le chiffre entré est plus petit, plus grand ou égale au chiffre mystère.
4. Affichez un message dans la console en fonction du résultat.

**Bonus**: Utiliser `isNaN()` pour vérifier que ce que le visiteur à écrit est bien un numéro.