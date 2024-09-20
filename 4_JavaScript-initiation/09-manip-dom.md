<!-- omit in toc -->
# Introduction à la Manipulation du DOM en JavaScript

Le DOM (Document Object Model) est la représentation en mémoire de la structure d’une page web. Grâce à JavaScript, il est possible d’interagir avec le DOM pour rendre nos pages dynamiques. Dans ce cours, nous allons voir comment manipuler les éléments de la page.

<!-- omit in toc -->
## Table des matières

- [Sélectionner des Éléments du DOM](#sélectionner-des-éléments-du-dom)
  - [Sélection par ID](#sélection-par-id)
  - [Sélection par Classe](#sélection-par-classe)
  - [Sélection par Tag (balise)](#sélection-par-tag-balise)

## Sélectionner des Éléments du DOM

En JavaScript, il existe plusieurs manières de sélectionner des éléments dans le DOM. On utilise généralement une variable pour stocker l'élément sélectionné et l'utiliser dans notre logique.

Il faut également placer l'exécution de notre script après le chargement de notre page. Si on place notre balise `<script>` dans `<head>` alors il va essayer de sélectionner des éléments qui pour la navigateur n'existait pas encore au moment où il a lu le script. Donc soit on place notre balise à la fin de `<body>` ou alors vous pouvez rajouter l'attribut `defer` à `<script>` ce qui retardera son exécution.

### Sélection par ID

La méthode `getElementById` permet de sélectionner un élément via son ID. 

```html
<h1 id="titre">Coucou</h1>
```

```js
const titre = document.getElementById('titre');
console.log(titre);
// Résultat: <h1 id="titre">Coucou</h1>
```

> 🚨 Attention, il ne peut pas y avoir plusieurs éléments avec la même ID! JS sélectionnera le premier qu'il trouve!

### Sélection par Classe

La méthode `getElementsByClassName` renvoie une liste de tous les éléments ayant une classe spécifique.

```html
<div class="texte">1</div>
<p class="texte">2</p>
<span class="texte">3</span>
```

```js
const textes = document.getElementsByClassName('texte');
console.log(textes)
// Résultat: HTMLCollection(3) [div.texte, p.texte, span.texte]
```

### Sélection par Tag (balise)

La méthode `getElementsByTagName` sélectionne tous les éléments d’un type de balise (ex. tous les <p>).

```html
<p class="a">1</p>
<p id="b">2</p>
<p>3</p>
```

```js
const paragraphes = document.getElementsByTagName('p');
console.log(paragraphes);
// Résultat: HTMLCollection(3) [p.a, p#b, p, b: p#b]
```