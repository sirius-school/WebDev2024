<!-- omit in toc -->
# JavaScript - les bases

JavaScript est un langage de programmation utilisé principalement pour rendre les pages web interactives. C’est un langage interprété, ce qui signifie qu’il est exécuté directement par le navigateur sans besoin de compilation préalable. Ce cours d’initiation vous apprendra les bases nécessaires pour créer des programmes simples en JavaScript.

<!-- omit in toc -->
## Table des matières

- [Principe de base](#principe-de-base)
  - [Code directement dans la balise `<script>` (Inline JavaScript)](#code-directement-dans-la-balise-script-inline-javascript)
  - [Code dans un fichier JavaScript externe](#code-dans-un-fichier-javascript-externe)
  - [Quand utiliser quelle méthode ?](#quand-utiliser-quelle-méthode-)
  - [Conclusion](#conclusion)
- [Console.log](#consolelog)
  - [Exercice pratique](#exercice-pratique)
- [Variables](#variables)
- [Types de données](#types-de-données)
- [Conditions](#conditions)
- [Boucles](#boucles)
- [Fonctions](#fonctions)
- [Tableaux](#tableaux)
- [Objets](#objets)

## Principe de base

Tout d'abord, on va devoir écrire notre JavaScript quelque part. Tout comme pour l'HTML et le CSS, il y a un endroit bien spécifique pour. Soit on l'insère directement dans notre page HTML, mais du coup le code sera utilisable que sur cette page et risque d'agrandir le nombre de lignes de code de notre fichier HTML et par conséquent le rendre moins lisible. Ou alors on peut tout simplement créer une page `.js` qui contiendra notre code et qu'on appellera sur notre page HTML, comme notre CSS.

### Code directement dans la balise `<script>` (Inline JavaScript)

```html
<html>
<head>
    <title>Exemple</title>
</head>
<body>
    <h1>Bonjour</h1>

    <script>
        console.log('Ceci est du JavaScript inline'); // Cette ligne, c'est du JavaScript
    </script>
</body>
</html>
```

<!-- omit in toc -->
#### Avantages JS inline

- **Simple et rapide** pour les petits scripts ou des tests rapides.
- **Accès direct au DOM** juste après l’insertion de la balise `<script>`, surtout si elle est placée à la fin du document.
- **Pas de requête HTTP supplémentaire** pour récupérer un fichier JS externe, donc moins de latence.

<!-- omit in toc -->
#### Inconvénients JS inline

- **Moins maintenable** à mesure que le code grossit : si votre projet devient grand, le code inline peut rendre l’organisation difficile.
- **Problèmes de sécurité** potentiels liés au Cross-Site Scripting (XSS). Placer du code JavaScript directement dans l’HTML peut rendre votre site plus vulnérable aux injections de scripts malveillants.
- **Réutilisation difficile** : il est plus compliqué de réutiliser le même code sur différentes pages, car vous devrez le copier/coller manuellement.
- **Mélange de contenu et de comportement** : cela va à l’encontre des bonnes pratiques de séparation du code (HTML pour le contenu, CSS pour le style, JavaScript pour le comportement).

### Code dans un fichier JavaScript externe

```html
<html>
<head>
    <title>Exemple</title>
    <script src="script.js"></script>
</head>
<body>
    <h1>Bonjour</h1>
</body>
</html>
```

<!-- omit in toc -->
#### Avantages fichier externe

- **Meilleure organisation** : séparer le code JavaScript du HTML améliore la lisibilité et la maintenabilité.
- **Réutilisable** : un fichier JavaScript externe peut être réutilisé sur plusieurs pages, évitant la duplication de code.
- **Meilleure sécurité** : il est plus difficile d’introduire des failles XSS avec du JavaScript dans un fichier externe, surtout si les bonnes pratiques de sécurité (comme les en-têtes de sécurité HTTP) sont respectées.
- **Amélioration des performances** : un fichier JavaScript externe peut être mis en cache par le navigateur, ce qui améliore la performance des visites répétées.
- **Séparation des préoccupations** : garder le JavaScript dans un fichier séparé respecte le principe de séparation des préoccupations entre le HTML (structure), le CSS (style), et le JavaScript (comportement).

<!-- omit in toc -->
#### Inconvénients fichier externe

- **Requête HTTP supplémentaire**: l’utilisation d’un fichier externe nécessite une requête HTTP pour charger le fichier, ce qui peut introduire une légère latence (même si cela peut être minimisé par le cache).
- **Nécessité de connexion** : si le fichier JS externe n’est pas accessible (par exemple en cas de problème de serveur), le code ne s’exécutera pas.

### Quand utiliser quelle méthode ?

- **Inline JavaScript** (dans la balise `<script>`) est généralement utilisé pour les petits scripts, les tests rapides, ou lorsqu’il n’est pas nécessaire de réutiliser le code ailleurs. C’est également une bonne option pour des cas simples où la performance est critique et que vous voulez éviter des requêtes supplémentaires.
- **JavaScript externe** est recommandé pour les projets plus importants ou complexes, ou lorsque vous avez besoin de réutiliser le code sur plusieurs pages. Cela permet une organisation plus claire et suit les bonnes pratiques de développement.

### Conclusion

Bien que les deux approches fonctionnent, le JavaScript dans un fichier externe est généralement préféré dans les projets de taille moyenne à grande en raison des avantages liés à l’organisation, à la "réutilisabilité" et à la sécurité. Le JavaScript inline est utile pour les scripts simples, mais il peut devenir difficile à gérer dans des applications plus complexes.

## Console.log

On va souvent avoir besoin de tester notre script tout au long de sa conception. Pour ce faire il nous faut une méthode simple et efficace pour vérifier si ça fonctionne ou non. C'est là qu'entre en jeu notre premier bout de code: `console.log()`. Celui-ci va nous permettre d'afficher des messages dans la console de notre navigateur ou de VSCode pour vérifier si tout se passe comme prévu. 

Vous pouvez retrouver votre console dans les outils de développements de votre navigateur (F12 ou inspecter).

### Exercice pratique

Pour utiliser `console.log()` c'est fort simple, suivez les étapes suivantes:

1. Créez un nouveau fichier HTML comme d'habitude.
2. Dans la balise `<body>` on va insérer une balise `<script>`
3. A l'intérieur de `<script>` écrivez simplement `console.log()`
4. Ensuite à l'intérieur des parenthèses on va ajouter des guillemets et écrire un petit mot entre les guillemets
5. Ensuite ouvrez la page dans votre navigateur, ouvrez les outils de développements (F12) et allez dans l'onglet "Console" pour y retrouver votre message.

```js
console.log("Hello World!")
```

Bravo, tu as réalisé ta première ligne de code JavaScript! 🎉

Par après `console.log()` nous servira à de multiples occasions pour vérifier nos fonctions et autres bouts de code JS.

## Variables

Un des premiers concept à appréhender en JavaScript c'est le principe d'une variable.

Une variable c'est un espace de stockage pour des valeurs. Vous pouvez déclarer des variables en utilisant les mots-clés `var`, `let`, ou `const`.

-**var** : utilisé pour déclarer des variables, mais a un comportement global ou fonctionnel.
-**let** : similaire à var, mais sa portée est limitée au bloc de code dans lequel elle est déclarée.
-**const** : pour les variables dont la valeur ne doit pas changer.

Pour le moment on a pas encore parlé de porté ou **scope**, donc ne vous en faite pas et utiliser **tout le temps** `let` et tout ira bien. `var` est plus dangereux à utiliser car vous risquer d'avoir des problèmes plus vite. Mais il est juste bon de savoir que ça existe car vous allez souvent trouver des exemples de codes encore écrit avec `var`.

## Types de données

## Conditions

## Boucles

## Fonctions

## Tableaux

## Objets