<!-- omit in toc -->
# Animation CSS (introduction)

Les animations CSS permettent d'animer n'importe quel élément sur votre page web. Elles suppriment aussi le besoin d'utiliser du JavaScript ou du JQuerry. Elles sont facile à utiliser une fois qu'on a pris le pas.

Regarde [cette animation](https://codepen.io/miocene/pen/mjLPVp) ou encore cette [re-création de l'intro Netflix](https://codepen.io/claudio_bonfati/pen/mdryxPv), ça donne envie, n'est-ce pas? Et bien on va voir un petit peux les techniques employés dans ce genre d'animation. On ira pas aussi loin mais si ça te plaît, tu peux toi même t'entrainer à faire ce genre d'animation.

<!-- omit in toc -->
## Table des matières

- [Animations CSS](#animations-css)
- [Quelques nouvelles propriétés](#quelques-nouvelles-propriétés)
  - [Transform](#transform)
    - [Translate](#translate)
    - [Scale](#scale)
    - [Rotate](#rotate)
    - [Skew](#skew)
    - [Multiple valeurs](#multiple-valeurs)
  - [Transformation 3D](#transformation-3d)
    - [La propriété perspective](#la-propriété-perspective)
    - [Les transformations 3D](#les-transformations-3d)
    - [L'effet de perspective](#leffet-de-perspective)
  - [Filter](#filter)
- [Animation](#animation)
  - [Transition](#transition)
  - [Keyframes](#keyframes)
    - [From \& To](#from--to)
    - [Pourcentages](#pourcentages)
  - [Amusez-vous](#amusez-vous)

## Animations CSS

Les animations en CSS permettent de donner vie aux éléments HTML en changeant progressivement leurs propriétés. Les animations ajoutent du dynamisme et de l’interactivité à une page, sans nécessiter de JavaScript.

Voici quelques exemples d'animations courantes:

- [Fade in/out](https://codepen.io/naafi/pen/qBbYEXe)
- [Déplacement](https://codepen.io/Md-Tofajjal-Hossen/pen/rNVVXbE)
- [Rotation](https://codepen.io/snazsh/pen/yQWQwo)
- [Changement de couleur](https://codepen.io/Uchiha-Itachi-/pen/MWmabwe)
- [Perspective 3D](https://codepen.io/natewiley/pen/QWGdZJ)
- [Changement de taille](https://codepen.io/takaneichinose/pen/wRXryM)
- [Zoom](https://codepen.io/ainalem/pen/oNxXRgW)
- [Animation infinie](https://codepen.io/yuanchuan/pen/wZJqNK)
- [Effets de rebond](https://codepen.io/maud-leleux/pen/RwGVvvQ)

Il y en a tellement, comme on dit en anglais "Sky is the limit". Mais avant de se lancer dans des animations complexes, il faut comprendre comment ça fonctionne.

[:arrow_up: Revenir au top](#table-des-matières)

## Quelques nouvelles propriétés

Avant de commencer à animer, voyons quelques nouvelles propriétés animable.

### Transform

La propriété transform en CSS permet de manipuler un élément en appliquant des transformations géométriques, comme des rotations, des échelles, des translations, ou des inclinaisons. Elle est particulièrement utile pour ajouter des effets visuels et est souvent utilisée dans les animations CSS.

#### Translate

Permet de déplacer l'élément sur un axe horizontale (X) ou verticale (Y)

```css
.element {
  transform: translateX(200px) translateY(-50px);
}
```

> :bulb: il est intéressant de noter que en utilisant translate, les autres contenu ne vont pas être impacté.

![translate](./img/anim/translate.gif)

> :bulb: Il est également possible de combiner les deux axes en une seule ligne `transform: translate(200px, -50px)`

#### Scale

Redimensionne un élément en fonction des valeurs de x (largeur) et y (hauteur). Le paramètre accepté est un chiffre qui détermine le nombre de fois que l'élément est agrandis ou rétrécis.

```css
.element {
  transform: scale(3, 1.5);
}
```

> :bulb: il est possible d'utiliser `scaleX` ou `scaleY`

#### Rotate

Fait tourner un élément de l’angle spécifié dans le sens des aiguilles d'une montre (par défaut). Il faut indiquer un paramètre en `deg` (degrés) et il peut être positif ou négatif.

```css
.element {
  transform: rotate(45deg);
}
```

> :bulb: il est possible d'utiliser `rotateX`, `rotateY` ou `rotateZ`

[Voir des exemples de rotation](https://codepen.io/team/css-tricks/pen/d31be2118a19782d2c4fcfb048351ccf)

[Voir des exemples de rotation sur axes](https://codepen.io/team/css-tricks/pen/ebb6b5a5cec86aa04168f03e26c7501c)

#### Skew

Permet d'incliner un élément sur l'axe X ou Y. Prend comme paramètre une valeur en degrés (`deg`).

```css
.element {
  transform: skew(20deg, 20deg);
}
```

> :bulb: il est possible d'utiliser `skewX` et `skewY`

[Voir des exemples de skew](https://codepen.io/team/css-tricks/pen/povNBmQ)

#### Multiple valeurs

Il est tout à fait possible d'écrire plusieurs valeurs à la propriété transform, il suffit de les espacer.

```css
.element {
  transform: translate(200px, -50px) scale(20);
}
```

> 🚨 Il ne faut pas écrire une nouvelle propriété transform par transformation que l'on veut. Sinon c'est le dernier transform qui prendra le dessus.

[:arrow_up: Revenir au top](#table-des-matières)

### Transformation 3D

En CSS, les transformations 3D permettent de manipuler des éléments dans l’espace, en simulant profondeur et angles. C’est utile pour donner un effet de relief aux éléments HTML. Cela permet de créer des boutons ou des cartes avec des effets de profondeur, des animations d'éléments qui tournent ou basculent ou une galerie d'image avec vue en perspective.

#### La propriété perspective

Pour ajouter de la perspective à un élément et à son contenu, vous devez utiliser la propriété perspective. Cette propriété définit la distance à laquelle l'observateur (l'utilisateur) se trouve de l'élément en trois dimensions.

```css
.container {
  perspective: 1000px;
}
```

> Dans cet exemple, la valeur 1000px indique que l'observateur est situé à 1000 pixels de l'élément `.container`. Plus la valeur est petite, plus l'effet de perspective sera prononcé.

#### Les transformations 3D

Une fois que vous avez défini la perspective sur un conteneur, vous pouvez appliquer des transformations 3D aux éléments enfants de ce conteneur. Les transformations 3D incluent des propriétés telles que rotateX(), rotateY(), rotateZ(), translateZ(), etc vues plus haut.

```css
.box {
  transform: rotateY(45deg) translateZ(100px);
  background-color: red;
  width: 300px;
  aspect-ratio: 1;
}
```

> Dans cet exemple, l'élément avec la classe .box subit une rotation autour de l'axe Y de 45 degrés et est déplacé vers l'avant de 100 pixels en utilisant translateZ(). La perspective définie sur le conteneur parent influencera la façon dont cette transformation est rendue visuellement.

#### L'effet de perspective

Lorsque vous appliquez des transformations 3D aux éléments à l'intérieur du conteneur avec perspective, l'effet de perspective donnera l'illusion que les éléments se déplacent dans un espace en trois dimensions par rapport à l'observateur. Les éléments proches de l'observateur sembleront plus grands, tandis que les éléments éloignés sembleront plus petits, ce qui crée une sensation de profondeur.

```html
<div class="container">
  <div class="box"></div>
</div>
```

> Dans cet exemple, la .box à l'intérieur du .container semblera se déplacer dans un espace 3D lorsque des transformations 3D sont appliquées.

La perspective en CSS est particulièrement utile pour créer des animations et des transitions 3D réalistes, ainsi que pour donner un effet de profondeur à des scènes complexes. Elle peut être combinée avec d'autres propriétés CSS telles que `transform-origin`, `perspective-origin`, et `backface-visibility` pour un meilleur contrôle sur les effets 3D et leur apparence.

[:arrow_up: Revenir au top](#table-des-matières)

### Filter

Cette propriété permet la modification en temps réel de vos images, c'est comme un filtre Instagram. Ce qui est bien, c'est que c'est animable aussi! Il y a différent effets que voici: filter: none | blur() | brightness() | contrast() | drop-shadow() | grayscale() | hue-rotate() | invert() | opacity() | saturate() | sepia() | url();

```css
.blur {filter: blur(4px);}
.brightness {filter: brightness(0.30);}
.contrast {filter: contrast(180%);}
.grayscale {filter: grayscale(100%);}
.huerotate {filter: hue-rotate(180deg);}
.invert {filter: invert(100%);}
.opacity {filter: opacity(50%);}
.saturate {filter: saturate(7);}
.sepia {filter: sepia(100%);}
.shadow {filter: drop-shadow(8px 8px 10px green);}
```

Pour les découvrir je vous renvois sur [cet exemple sur la W3School](https://www.w3schools.com/cssref/tryit.php?filename=trycss3_filter_all)

## Animation

### Transition

Voyons maintenant comment on peut controller le passage d'un état à un autre. Ça s'appel une transition.

Pour ce faire définissons 2 états:

```css
.element {
  width: 100px;
  padding: 50px 0;
  line-height: 0;
  margin: 60px auto;
  background-color: red;
  color: yellow;
  border-radius: 50px;
  text-align: center;
}

.element:hover {
  background-color: black;
  transform: scale(2);
}
```

Tel quel notre "animation" se ferra correctement sur le survol de l'élément par le curseur. Mais ce n'est pas très "lisse", c'est trop "abrupte".

On peut donc appliquer une propriété `transition` à notre élément de base. On indique une valeur en temps (sec).

```css
.element {
  transition: 1s;
}
```

Comme nous avons modifié des propriétés animables en CSS, votre navigateur se charge de faire la transition entre les différentes propriétés.

Il est possible aussi de spécifier le temps de transition pour chacune de ces propriétés individuellement.

```css
.element {
  transition: background-color 1s, transform 2s;
}
```

Vous pouvez aussi spécifier un délai avant que la transition ne se lance. Pour se faire il suffit de préciser le temps du délai après avoir indiqué le temps de la transition

```css
.element {
  transition: background-color 1s 2s, transform 2s 5s;
}
```

Cela nous fait déjà beaucoup de contrôle sur notre transition, mais il existe une dernière valeur que l'on peut associer à notre transition. Il s'agit de la "fonction de temps" (timing-function). Cela détermine l'accélération de notre animation. Par défaut il s'agit de `linear` mais il en existe d'autres comme `ease-in`, `ease-out`,... Vous pouvez également créer votre propre accélération avec `cubic-bezier`.

```css
.element {
  transition: background-color 1s 2s ease-in, transform 2s 5s;
}
```

> :bulb: Retrouvez sur [Cubic-bezier.com](https://cubic-bezier.com) la possibilité de créer vos propres accélération mais aussi des exemples des paramètres tels que `linear` ou `ease-in`.

[:arrow_up: Revenir au top](#table-des-matières)

### Keyframes

#### From & To

C'est avec les keyframes qu'on va définir comment notre animation fonctionne et qu'on va pouvoir allez plus loin. Ce sont des "bloc" d'animation qu'on va pouvoir appliquer sur nos éléments. On va définir un état de base (from) et on va définir un état d'arrivé (to). Voyons cela en pratique.

```css
@keyframes move-right {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(500px);
  }
}
```

On définit notre animation, dans ce cas un déplacement de 500px vers la droite.

Pour appliquer cette animation à un élément il suffit d'utiliser la propriété `animation-name` et `animation-duration`.

```css
.element {
  animation-name: move-right;
  animation-duration: 3s;
}
```

> :exclamation: il est important de mettre le même nom que celui appliqué à la keyframe et il est également nécessaire de mettre une durée.

On retrouve également des propriétés tels que:

- **animation-timing-function**: détermine l'accélération de l'animation (ease-in, ease-out, **linear**,...)
- **animation-delay**: détermine le délai avant de commencer l'animation (en seconde)
- **animation-direction**: détermine le sens de l'animation (**normal**, reverse, alternate, alternate-reverse)
- **animation-iteration-count**: permet de définir le nombre de fois que l'animation doit se répéter (chiffre ou infinite)
- **animation-fill-mode**: Spécifie ce qui doit se passer avant et après l'animation.
- **animation-play-state**: Permet de mettre en pause ou de reprendre une animation.

[Voici des exemples d'animations et plus d'information](https://css-tricks.com/almanac/properties/a/animation/#sub-properties)

#### Pourcentages

Il est également possible de diviser votre animation en utilisant des %. Pour chaque x% on va définir les états de notre animation. De 0% à 100% est accompli en fonction de la durée définie.

```css
@keyframes mymove {
  0% {
    top: 0px;
  }
  25% {
    top: 200px;
  }
  50% {
    top: 100px;
  }
  75% {
    top: 200px;
  }
  100% {
    top: 0px;
  }
}
```

[:arrow_up: Revenir au top](#table-des-matières)

### Amusez-vous

C'est à vous de jouer maintenant, créez des animations, tentez des choses, voyez comment ça se comporte.

Voici [Animista](https://animista.net/) un site qui te permet d'expérimenter toutes sortes d'animation et d'en récupérer le code pour tes projets.

Consulte aussi [cette page interactive](https://rupl.github.io/unfold/) pour voir la puissance du CSS.

Et voici [5 frameworks](https://dev.to/aashishpanthi/top-5-javascript-animation-libraries-2021-17n7) pour réaliser des animations. C'est intéressant de savoir qu'ils existent mais il va falloir lire la documentation si tu veux les utiliser. Je te conseille de jeter un oeil à [KUTE.js](https://thednp.github.io/kute.js/index.html)

Et voici 3 petits jeux réalisés en HTML et CSS **uniquement**:

- [Roadmap](http://victordarras.fr/cssgame)
- [Target Carnival](https://codepen.io/una/pen/NxZaNr)
- [Tic-Tac-Toe](https://codepen.io/alvaromontoro/pen/BexWOw)

[:arrow_up: Revenir au top](#table-des-matières)

[:rewind: Retour au sommaire du cours](./README.md#table-des-matières)
