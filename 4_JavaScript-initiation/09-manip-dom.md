<!-- omit in toc -->
# Introduction à la Manipulation du DOM en JavaScript

Le DOM (Document Object Model) est la représentation en mémoire de la structure d’une page web. Grâce à JavaScript, il est possible d’interagir avec le DOM pour rendre nos pages dynamiques. Dans ce cours, nous allons voir comment manipuler les éléments de la page.

<!-- omit in toc -->
## Table des matières

- [Sélectionner des Éléments du DOM](#sélectionner-des-éléments-du-dom)
  - [Sélection par ID](#sélection-par-id)
  - [Sélection par Classe](#sélection-par-classe)
  - [Sélection par Tag (balise)](#sélection-par-tag-balise)
  - [Sélection avec querySelector et querySelectorAll](#sélection-avec-queryselector-et-queryselectorall)
- [Modifier des Classes et Attributs](#modifier-des-classes-et-attributs)
  - [Modifier les classes](#modifier-les-classes)
  - [Modifier les Attributs](#modifier-les-attributs)
- [Modifier le Contenu d’un Élément](#modifier-le-contenu-dun-élément)
  - [Modifier le Texte](#modifier-le-texte)
  - [Modifier le Contenu HTML](#modifier-le-contenu-html)
- [Ajouter ou Supprimer des Éléments](#ajouter-ou-supprimer-des-éléments)
  - [Créer et Ajouter des Éléments](#créer-et-ajouter-des-éléments)
    - [appendChild](#appendchild)
    - [insertBefore](#insertbefore)
  - [Supprimer un Élément](#supprimer-un-élément)

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

La méthode `getElementsByTagName` sélectionne tous les éléments d’un type de balise (ex. tous les `<p>`).

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

### Sélection avec querySelector et querySelectorAll

Ces deux méthodes permettent de sélectionner un ou plusieurs éléments en utilisant des sélecteurs CSS.

- `querySelector` sélectionne le premier élément qui correspond au sélecteur.
- `querySelectorAll` sélectionne tous les éléments qui correspondent au sélecteur. Retourne une `NodeList`, c’est-à-dire une collection d’éléments

```js
const premierTitre = document.querySelector('h1');
const tousLesParagraphes = document.querySelectorAll('p');
```

Il est possible de sélectionner un élément précis dans notre `NodeList` à la manière d'un tableau. Il suffit d'utiliser les crochets pour préciser l'index que l'on souhaite.

```js
const leParagraphe2DeTousLesParagraphes = document.querySelectorAll('p')[1];
```

## Modifier des Classes et Attributs

Maintenant qu'on sait comment sélectionner nos éléments HTML, il est temps de faire nos premières modifications. Voyons comment on peut modifier ses classes ou attributs.

### Modifier les classes

La propriété `classList` permet de manipuler les classes **d’un élément**.

- **add**: ajouter une classe
- **remove**: supprimer une classe
- **toggle**: ajouter ou retirer une classe selon qu’elle existe ou non
- **contains**: vérifier si une classe est présente

```js
const monElement = document.querySelector('div');
monElement.classList.add('nouvelle-classe');
monElement.classList.remove('ancienne-classe');
monElement.classList.toggle('visible');
```

Si on veut changer **tous** nos éléments, on peut utiliser `querySelectorAll`, ce dernier nous retourne une `NodeList` qu'on doit parcourir avec la fonction `forEach` comme dans l'exemple ci-dessous.

```js
const elements = document.querySelectorAll('.ma-classe');

// Boucler sur chaque élément de la NodeList
elements.forEach(function(element) {
    element.classList.add('nouvelle-classe');
});
```

### Modifier les Attributs

Utilisez `setAttribute` pour modifier ou ajouter un attribut à un élément. Pour supprimer un attribut, utilisez removeAttribute.

```js
const image = document.querySelector('img');
image.setAttribute('src', 'nouvelle-image.webp');
image.removeAttribute('alt');
```

## Modifier le Contenu d’un Élément

Il existe différentes façons de modifier le contenu d’un élément.

### Modifier le Texte

La propriété `textContent` permet de modifier (remplacer!) ou lire le texte à l’intérieur d’un élément.

```js
const paragraphe = document.querySelector('p');
paragraphe.textContent = 'Nouveau contenu de paragraphe';
```

### Modifier le Contenu HTML

La propriété `innerHTML` permet d’injecter (remplacer!) du contenu HTML dans un élément.

```js
const div = document.querySelector('div');
div.innerHTML = '<p>Ceci est un nouveau paragraphe</p>';
```

## Ajouter ou Supprimer des Éléments

### Créer et Ajouter des Éléments

Vous pouvez créer un nouvel élément avec `createElement` et l’ajouter au DOM avec `appendChild` ou `createBefore`.

#### appendChild

**Fonctionnement** : La méthode appendChild ajoute un élément en dernier enfant d'un élément parent. Elle place toujours le nouvel élément à la fin de la liste des enfants de ce parent.

```js
const nouvelleDiv = document.createElement('div');
nouvelleDiv.textContent = 'Ceci est une nouvelle div';
document.body.appendChild(nouvelleDiv); // Ajoute à la fin du body
```

**Quand l'utiliser ?**

Lorsqu'on veut ajouter un élément à la fin

#### insertBefore

**Fonctionnement** : La méthode insertBefore insère un élément avant un autre élément spécifique qui est déjà un enfant du même parent. Il te permet de définir plus précisément l'endroit où tu veux insérer l'élément dans la hiérarchie des enfants.

```js
const nouvelleDiv = document.createElement('div');
nouvelleDiv.textContent = 'Ceci est une nouvelle div';
const secondParagraphe = document.querySelectorAll('p')[1];
document.body.insertBefore(nouvelleDiv, secondParagraphe);
```

**Quand l'utiliser ?**

Lorsqu'on veut plus de contrôle sur la position (par exemple, avant un élément spécifique).

### Supprimer un Élément

La méthode `removeChild` permet de supprimer un élément enfant.

```js
const parent = document.querySelector('#parent');
const enfant = document.querySelector('.enfant');
parent.removeChild(enfant);
```
