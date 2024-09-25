<!-- omit in toc -->
# Introduction aux événements du DOM JavaScript

Dans une page web, un événement est une interaction ou un changement qui se produit dans le navigateur, comme un clic, le survol d'un élément, ou la soumission d'un formulaire. JavaScript permet de réagir à ces événements pour rendre les pages interactives et dynamiques.

Les événements du DOM permettent aux développeurs de "capturer" ces actions et d'y répondre en exécutant du code. Comprendre comment manipuler les événements est fondamental pour développer des applications web interactives.

<!-- omit in toc -->
## Table des matières

- [Qu'est-ce qu'un Événement ?](#quest-ce-quun-événement-)
- [Écouter des Événements avec addEventListener](#écouter-des-événements-avec-addeventlistener)
- [Types d'Événements Courants](#types-dévénements-courants)
  - [Événements de la Souris](#événements-de-la-souris)
  - [Événements de Clavier](#événements-de-clavier)
  - [Événements de Formulaire](#événements-de-formulaire)
- [L'objet event](#lobjet-event)
- [Supprimer un Écouteur d'Événement](#supprimer-un-écouteur-dévénement)
- [Différences entre les Méthodes de Gestion d'Événements](#différences-entre-les-méthodes-de-gestion-dévénements)
  - [Ajouter un écouteur directement dans HTML](#ajouter-un-écouteur-directement-dans-html)
  - [Utiliser la propriété événement dans JavaScript](#utiliser-la-propriété-événement-dans-javascript)
  - [Utiliser `addEventListener` (recommandé)](#utiliser-addeventlistener-recommandé)

## Qu'est-ce qu'un Événement ?

Un événement est une action déclenchée par l'utilisateur ou le système. Voici quelques exemples courants d'événements :

- Clic (click)
- Survol de la souris (mouseover)
- Soumission d'un formulaire (submit)
- Appui sur une touche (keydown)
- Changement de valeur d'un champ (change)
  
## Écouter des Événements avec addEventListener

La méthode la plus courante pour intercepter et réagir aux événements est d'utiliser `addEventListener`. Elle permet d'attacher un écouteur d'événement à un élément du DOM. Cela signifie qu'on "écoute" un événement spécifique (comme un clic) et on réagit lorsqu'il se produit.

**Syntaxe**

```js
element.addEventListener('type', function(event) {
    // Action à exécuter lorsque l'événement est déclenché
});
```

- **element** : L'élément sur lequel on souhaite écouter l'événement.
- **type** : Le type d'événement (par exemple, 'click').
- **function** : La fonction qui sera exécutée lorsque l'événement se produit.
- **event** : L'objet événement, qui contient des informations sur l'événement (comme la position du clic, l'élément qui a déclenché l'événement, etc.).

```js
const bouton = document.querySelector('button');
bouton.addEventListener('click', function() {
    alert('Bouton cliqué!');
});
```

> Dans cet exemple, un message d'alerte apparaît chaque fois que l'utilisateur clique sur le bouton.

## Types d'Événements Courants

Voici quelques événements fréquemment utilisés dans le DOM :

### Événements de la Souris

- **click** : Se produit lorsqu'un élément est cliqué.
- **dblclick** : Se produit lorsqu'un élément est double-cliqué.
- **mouseover** : Se produit lorsque la souris passe au-dessus d'un élément.
- **mouseout** : Se produit lorsque la souris quitte un élément.

```js
const image = document.querySelector('img');
image.addEventListener('mouseover', function() {
    image.style.border = '2px solid red'; // Change la bordure de l'image lors du survol
});
```

### Événements de Clavier

- **keydown** : Se produit lorsqu'une touche du clavier est enfoncée.
- **keyup** : Se produit lorsqu'une touche du clavier est relâchée.

```js
document.addEventListener('keydown', function(event) {
    console.log('Touche appuyée : ' + event.key);
});
```

### Événements de Formulaire

- **submit** : Se produit lorsqu'un formulaire est soumis.
- **change** : Se produit lorsqu'une valeur dans un champ de formulaire change.

```js
const formulaire = document.querySelector('form');
formulaire.addEventListener('submit', function(event) {
    event.preventDefault(); // Empêche le rechargement de la page lors de la soumission
    alert('Formulaire soumis !');
});
```

## L'objet event

L'objet `event` est automatiquement passé à la fonction de gestion de l'événement (event handler). Il contient des informations utiles sur l'événement qui s'est produit.

Propriétés courantes de l'objet `event` :

- **event.target** : L'élément qui a déclenché l'événement.
- **event.type** : Le type d'événement (ex. 'click').
- **event.preventDefault()** : Empêche le comportement par défaut de l'événement (utile pour des événements comme submit ou des liens).

Exemple avec `event.target` :

```js
document.querySelectorAll('button').forEach(function(button) {
    button.addEventListener('click', function(event) {
        alert('Vous avez cliqué sur le bouton : ' + event.target.textContent);
    });
});
```

## Supprimer un Écouteur d'Événement

Si tu veux retirer un écouteur d'événement à un moment donné, tu peux utiliser la méthode `removeEventListener`. Cela permet d'empêcher un événement de continuer à être écouté.

```js
function alerteClic() {
    alert('Clic détecté');
}

const bouton = document.querySelector('button');
bouton.addEventListener('click', alerteClic);

// Pour supprimer l'écouteur après 5 secondes
setTimeout(function() {
    bouton.removeEventListener('click', alerteClic);
}, 5000);
```

## Différences entre les Méthodes de Gestion d'Événements

Il existe plusieurs façons de gérer les événements en JavaScript, mais certaines méthodes sont aujourd'hui moins courantes ou déconseillées. Voici un aperçu des trois méthodes principales à titre informatif car tu risques d'en croiser dans ton aventure JavaScript!

### Ajouter un écouteur directement dans HTML

```html
<button onclick="alert('Bouton cliqué!')">Cliquez-moi</button>
```

**Inconvénient** : Ce n'est pas une bonne pratique, car cela mélange le HTML et le JavaScript, ce qui complique la maintenance.

### Utiliser la propriété événement dans JavaScript

```js
const bouton = document.querySelector('button');
bouton.onclick = function() {
    alert('Bouton cliqué!');
};
```

**Limite** : Cette méthode écrase tout autre gestionnaire d'événement onclick précédent.

### Utiliser `addEventListener` (recommandé)

```js
const bouton = document.querySelector('button');
bouton.addEventListener('click', function() {
    alert('Bouton cliqué!');
});

```

**Avantage** : Permet d'ajouter plusieurs gestionnaires pour le même événement et garde le code séparé du HTML.

<!-- omit in toc -->
## Conclusion

La gestion des événements est un élément clé pour rendre une page web interactive et réactive aux actions des utilisateurs. Utiliser correctement les événements avec addEventListener et l'objet event permet de contrôler le comportement des pages web avec précision. Avec ce cours, tu es maintenant capable d'écouter, gérer et réagir à la plupart des événements courants du DOM.
