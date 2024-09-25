<!-- omit in toc -->
# Exercices Events dans le DOM

Voici quelques exercices simples pour apprendre à manipuler les events dans le DOM en javascript.

<!-- omit in toc -->
## Légende des difficultés

Facile: 😄
Modéré: 😊
Exigeant: 😅
Épineux: 😰
Impossible?: 😡

<!-- omit in toc -->
## Liste des exercices

- [😄 Exercice 1 : Écouter un Clic](#-exercice-1--écouter-un-clic)
- [😊 Exercice 2 : Changer la Couleur d'un Élément au Survol](#-exercice-2--changer-la-couleur-dun-élément-au-survol)
- [😊 Exercice 3 : Afficher la Touche Pressée](#-exercice-3--afficher-la-touche-pressée)
- [😅 Exercice 4 : Supprimer un Écouteur d'Événement](#-exercice-4--supprimer-un-écouteur-dévénement)
- [😰 Exercice 5 : La calculatrice !!!! Mais la version Wish!](#-exercice-5--la-calculatrice--mais-la-version-wish)

<!-- omit in toc -->
## :memo: Objectifs

- Réaliser ses premiers scripts qui manipulent les events dans le DOM en utilisant la théorie déjà vue
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

## 😄 Exercice 1 : Écouter un Clic

> Sujets : variables, sélection, dom, events, addEventListener, alert

**Objectif**

Afficher une alerte avec le message "Bouton cliqué !" lorsqu'on clique sur le bouton.

```html
<body>
  <button id="monBouton">Cliquez-moi</button>
</body>
```

## 😊 Exercice 2 : Changer la Couleur d'un Élément au Survol

> Sujets : variables, sélection, dom, events, addEventListener, mouseover, mouseout

**Objectif**

Changer la couleur du carré en rouge lorsque la souris passe dessus, puis de la remettre en bleu lorsque la souris quitte le carré.

```html
<body>
  <div id="carre" style="width:100px; height:100px; background-color:blue;"></div>
</body>
```

## 😊 Exercice 3 : Afficher la Touche Pressée

> Sujets : variables, sélection, dom, events, addEventListener
**Objectif**

Capturer les événements du clavier avec `keydown` et à afficher dans la console la touche appuyé.

```html
<body>
  <div id="carre" style="width:100px; height:100px; background-color:blue;"></div>
</body>
```

## 😅 Exercice 4 : Supprimer un Écouteur d'Événement

> Sujets : variables, sélection, dom, events, addEventListener, function

**Objectif**

Afficher une alerte "Bouton cliqué !" au premier clic, puis de supprimer cet écouteur d'événement afin qu'il ne se déclenche plus lors des clics suivants.

```html
<body>
  <button id="monBouton">Cliquez-moi</button>
</body>
```

**Indices**

- Tu peux créer une fonction pour t'occuper du click

## 😰 Exercice 5 : La calculatrice !!!! Mais la version Wish!

> Sujets : variables, sélection, dom, events, addEventListener, function, switch, constructor

**Objectif**

Tu dois créer une calculatrice simple avec :

- Deux champs de texte pour saisir les chiffres.
- Quatre boutons correspondant aux quatre opérations de base (addition, soustraction, multiplication, division).
- Un champ pour afficher le résultat.

Lorsque l'utilisateur clique sur un des boutons, le résultat de l'opération choisie doit être affiché dans le champ du résultat.

```html
<form id="calculatrice">
  <input type="number" id="nombre1" placeholder="Nombre 1">
  <input type="number" id="nombre2" placeholder="Nombre 2">
  
  <button type="button" id="addition">+</button>
  <button type="button" id="soustraction">-</button>
  <button type="button" id="multiplication">x</button>
  <button type="button" id="division">÷</button>
  
  <input type="text" id="resultat" placeholder="Résultat" readonly>
</form>

```

**Instructions**

- Les utilisateurs doivent pouvoir entrer deux nombres.
- Les quatre boutons doivent correspondre aux quatre opérations : addition, soustraction, multiplication et division.
- Lorsque l'utilisateur clique sur un bouton, l'opération est effectuée et le résultat est affiché dans le champ "Résultat".
- Assure-toi que le champ de résultat ne peut pas être modifié par l'utilisateur (utilise readonly).

**Indices**

- Utilise des variables pour stocker tous les éléments html pour pouvoir facilement les utiliser dans ta logique
- Utilise une fonction `calculer(operation)` pour créer ta logique
- Tu devras t'assurer que la valeur du champ devient un nombre (vérifie avec `typeOf` et souviens-toi du constructor qu'on a utilisé précédemment)
- Tu peux vérifier que l'utilisateur à bien rentré un chiffre.
- Ensuite utilise un `switch` pour faire ton calcul.
- Affiche le résultat en changeant la valeur du champ (input) `resultat`
- Utilise des `eventListener` pour lancer ta fonction au clic sur un bouton d'opération.

Bonne chance 😊

![good-luck](https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExcm12N2Fla2M4NHNuZ2cwdmJyYmJzaTYxc3liYTZoeHlxdXRsZ2M5eCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/EqF5Y99mEH29HcxXnq/giphy.gif)