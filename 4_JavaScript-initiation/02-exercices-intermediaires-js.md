<!-- omit in toc -->
# Exercices intermédiaires JS

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

- [😄 Exercice 1 - Afficher un message dans la console](#-exercice-1---afficher-un-message-dans-la-console)
- [😄 Exercice 2 - Déclaration de variables et affichages](#-exercice-2---déclaration-de-variables-et-affichages)
- [😊 Exercice 3 - Calculatrice simple en code uniquement](#-exercice-3---calculatrice-simple-en-code-uniquement)
- [😅 Exercice 4 - Calculatrice simple avec prompt et alert](#-exercice-4---calculatrice-simple-avec-prompt-et-alert)
- [😊 Exercice 5 - Création d'un tableau](#-exercice-5---création-dun-tableau)
- [😊 Exercice 6 - Création d'un objet](#-exercice-6---création-dun-objet)
- [😅 Exercice 7 - Comparaison entre deux nombres](#-exercice-7---comparaison-entre-deux-nombres)


<!-- omit in toc -->
## :memo: Objectifs

- Réaliser sa première page de script JavaScript en utilisant la théorie déjà vue
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

## 😄 Exercice 1 - Afficher un message dans la console

> Sujet: console

Faites en sorte que la phrase "Bienvenue dans les exercices JavaScript" s'affiche dans votre console

## 😄 Exercice 2 - Déclaration de variables et affichages

> Sujets: console, variables

1. Déclarez 5 variables: `title` (string), `genre` (number), `year` (number), `actor1` (string) et `actor2` (string)
2. Stockez des valeurs pour chacune de vos variables correspondant à un film au choix.
3. Affichez les 5 valeurs dans un ou de multiples `console.log()`

## 😊 Exercice 3 - Calculatrice simple en code uniquement

> Sujets: console, variables, opérateurs arithmétique

On va créer une calculatrice juste en utilisant les variables et la console.

1. Créez 2 variables: `nombre1` (number) et `nombre2` (number)
2. Pour chaque variable, indiquez un nombre.
3. Créez 4 `console.log` pour indiquez la `Somme` (+), la `Différence` (-), le `Produit` (*) et le `Quotient` (/) de ces 4 nombres.

## 😅 Exercice 4 - Calculatrice simple avec prompt et alert

> Sujets: console, variables, opérateurs arithmétique, prompt, alert

On va un peu améliorer notre calculatrice et la rendre un peu moins statique.

1. Créez 2 variables: `nombre1` (number) et `nombre2` (number)
2. Insérer la valeur suivante pour `nombre1` : `Number(prompt("Entrez le premier nombre :"));`
3. Insérer la valeur suivante pour `nombre2` : `Number(prompt("Entrez le deuxième nombre :"));`
4. Créer 4 variables: `somme`, la `différence`, le `produit` et `quotient` pour y exécuter l'opération.
5. Créer une alert contenant les 4 variables et donc les résultats.

> 💡 Dans cet exercice je vous fournis le prompt pour une bonne raison. Lorsqu'on demande à l'utilisateur de répondre, JS va interpréter la réponse comme étant une string (texte). Du coup si on veut faire des opérations mathématiques avec les nombres introduits par l'utilisateur ça n'ira pas car ça reviendrait à faire "Pomme + Steak", ça n'a pas de sens tel quel.
> Du coup la solution est d'utiliser un constructeur (constructor) pour préciser à JS que la valeur qu'on va recevoir n'est pas une string mais bien un number. Nous reverrons sûrement les constructeurs plus tard.

## 😊 Exercice 5 - Création d'un tableau

> Sujets: console, variables, tableaux

1. Créez une variable `etudiants`
2. Insérer comme valeur un tableau contenant le prénom de vos camarades de classes (5 valeurs minimum)
3. Faites un `console.log` du premier prénom et un deuxième `console.log` du cinquième.

## 😊 Exercice 6 - Création d'un objet

> Sujets: console, variables, objets

1. Créez une variable `monFilmCulte`
2. Insérer comme valeur un objet contenant les clés suivantes: `title` (string), `genre` (number), `year` (number), `actor1` (string) et `actor2` (string) et insérer les valeurs de votre film préféré.
3. Faites un `console.log` de chacune des 5 clés.

## 😅 Exercice 7 - Comparaison entre deux nombres

> Sujets: console, variables, opérateurs de comparaison

1. Créez 2 variables: `nombre1` (number) et `nombre2` (number)
2. Insérer la valeur suivante pour `nombre1` : `Number(prompt("Entrez le premier nombre :"));`
3. Insérer la valeur suivante pour `nombre2` : `Number(prompt("Entrez le deuxième nombre :"));`
4. Faites un `console.log` qui va vérifier si `nombre1` est plus grand que `nombre2` et affichez `true` ou `false`


![well-done](https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExMzV6NjY5Z2d4MGJ1eWVpcmRjaG85YzljbzljajlvNzk5YTNrOHRpZCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/JLFq4Jh5bSJEDHZjSB/giphy.gif)
