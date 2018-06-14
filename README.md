# Documentation de connaissances générales sur le technologies Web

## Intégration

### HTML5

Le HTML5 est un langage de base pour la création de site internet, il sert à structurer le document. D’autre langage peuvent s’ajouter lors de la conception, mais tout les sites web contiennent du HTML. HTML5 désignant la version du langage HTML.

Il suit une structure dite **hiérarchisée** où chaque balise est ou bien parent ou bien enfant d'une autre balise parent.

* Balises
```
<html> // Balise principale
<head> // En-tête de la page
<body> //Corps de la page
<link /> //Liaison avec une feuille de style
<meta /> // Métadonnées de la page web (charset, mots-clés, etc.)
<script> //Code JavaScript
<style> //Code CSS
<title> //Titre de la page
<abbr> // Abréviation
<blockquote> // Citation (longue)
<cite> // Citation du titre d'une œuvre ou d'un évènement
<q> // Citation (courte)
<sup> // Exposant
<sub> // Indice
<strong> // Mise en valeur forte
<em> // Mise en valeur normale
<mark> // Mise en valeur visuelle
<h1> // Titre de niveau 1
<h2> // Titre de niveau 2
<h3> // Titre de niveau 3
<h4> // Titre de niveau 4
<h5> // Titre de niveau 5
<h6> // Titre de niveau 6
<img /> // Image
<figure> // Figure (image, code, etc.)
<figcaption> // Description de la figure
<audio> // Son
<video> // Vidéo
<source> // Format source pour les balises<audio>et<video>
<a> // Lien hypertexte
<br /> // Retour à la ligne
<p> // Paragraphe
<hr /> // Ligne de séparation horizontale
<address> // Adresse de contact
<del> // Texte supprimé
<ins> // Texte inséré
<dfn> // Définition
<kbd> // Saisie clavier
<pre> // Affichage formaté (pour les codes sources)
<progress> // Barre de progression
<time> // Date ou heure
```

* Nouvelles balises introduites avec HTML 5
  ```<article>
  <aside>
  <details>
  <figcaption>
  <figure>
  <footer>
  <header>
  <main>
  <mark>
  <nav>
  <section>
  <summary>
  <time>

### CSS3

CSS est l'acronyme de Cascading Style Sheet, ou feuille de style en cascade en français.
Le CSS permet d'insérer des styles sur un code HTML ou XHTMl et donc permet de définir très précisément le comportement de chaque élément de la page.
On voit déjà des sites fait entièrement en CSS (contrairement à la majorité des sites qui sont fait en tableau) mais le problème de la compatibilité avec certains explorateurs ne permettent pas d'exploiter toutes les fonctions des feuilles de style.

* Une feuille de style CSS externe peut se faire avec le simple bloc-note, et il est d'usage de lui faire porter l'extension .css. On la liera ensuite à la page html à l'aide d'un link placé dans l'en-tête de la page.
Mais on peut aussi déclarer les styles dans l'en-tête de la page, ou au sein des balises elles-mêmes. Cela peut-être intéressant pour appliquer des styles spécifiques et ils auront un ordre de priorité plus important. C'est ce qu'on appelle la "cascade".

* Structure et syntaxe
  * Selecteur (div, .nomDiv, .#id)
  * Proprieté (ex. color)
  * Attribut (ex. red)
  ```
  .nomDiv {
    color: red;
    }
  ```
  
  N.B En CSS on encapsule les proprietés dans les accolades et chaque attribut est toujours suivi par un point virgule. Ceci ne s'applique pas pour SASS (cf. SCCS/ SASS).
  
#### Responsive

La spécification CSS3 Media Queries définit les techniques pour l'application de feuilles de styles en fonction des périphériques de consultation utilisés pour du HTML. On nomme également cette pratique Responsive Web Design, pour dénoter qu'il s'agit d'adapter dynamiquement le design à l'aide de CSS.

Ces bonnes pratiques permettent d'exploiter encore plus les avantages de la séparation du contenu et de la présentation : l'intérêt est de pouvoir satisfaire des contraintes de dimensions, de résolutions et d'autres critères variés pour améliorer l'apparence graphique et la lisibilité (voire l'utilisabilité) d'un site web. Les plateformes exotiques sont concernées en premier lieu : navigateurs mobiles et tablettes, écrans à faibles résolutions, impression, tv, synthèses vocales, plages braille, etc.

Exemple media-query

```@media screen and (min-width: 200px) and (max-width: 640px) {
  .bloc {
    display:block;
    clear:both;
  }
}
```


#### Reset / Normalize

Source: https://stackoverflow.com/questions/6887336/what-is-the-difference-between-normalize-css-and-reset-css

>The main differences are:
>
>1. Normalize.css preserves useful defaults rather than "unstyling" everything. For example, elements like sup or sub "just >work" after including normalize.css (and are actually made more robust) whereas they are visually indistinguishable from >normal text after including reset.css. So, normalize.css does not impose a visual starting point (homogeny) upon you. This >may not be to everyone's taste. The best thing to do is experiment with both and see which gels with your preferences.
>
>2. Normalize.css corrects some common bugs that are out of scope for reset.css. It has a wider scope than reset.css, and also >provides bug fixes for common problems like: display settings for HTML5 elements, the lack of font inheritance by form >elements, correcting font-size rendering for pre, SVG overflow in IE9, and the button styling bug in iOS.
>
>3. Normalize.css doesn't clutter your dev tools. A common irritation when using reset.css is the large inheritance chain that >is displayed in browser CSS debugging tools. This is not such an issue with normalize.css because of the targeted stylings.
>
>4. Normalize.css is more modular. The project is broken down into relatively independent sections, making it easy for you to >potentially remove sections (like the form normalizations) if you know they will never be needed by your website.
>
>5. Normalize.css has better documentation. The normalize.css code is documented inline as well as more comprehensively in the >GitHub Wiki. This means you can find out what each line of code is doing, why it was included, what the differences are >between browsers, and more easily run your own tests. The project aims to help educate people on how browsers render elements >by default, and make it easier for them to be involved in submitting improvements.




### PUG (JADE)

Pug est un moteur de templating qui permet d'acceler le développement du HTML grâce à un rendu en JS et Node.js.
Il était connu sous le nom de *Jade* mais ils ont dû changer leur nom car Jade était déjà un nom enregistré.

Caractéristiques:

  * Pas de crochets ni de balises fermantes (gain en rapidité d'écriture)
  * La hiérachie des balises se fait à travers l'indentation qui doit être rigoreusement respectée
  * Possibilité de créer des conditions et des mixins



### SCSS / SASS 

Similairement à Pug, SCSS/ SASS sont des extensions du CSS qui permettent de gagner en rapidité et productivité.

SCSS :
  * Possibilité d'embriquer les selecteurs pour respecter le niveau de hiérarchie
  * Création de conditions, boucles et mixins (responsive)
  * Possibilité d'utiliser des variables
  
```
.jeSuisParent{
  color: $someColor; // VARIABLE
  
.jeSuisEnfant {
  color: yellow;
  }
}
```
  
SASS :
Mêmes carcatéristiques que le SCSS, mais différences à niveau syntaxique: alors que le SCSS respecte l'utilisation des accolades et des points virgules comme en CSS classique, en SASS il n'y a ni d'accolades ni de points virgules, ainsi la hiérarchie est gerée par l'indentation (comme en PUG, voir ci-dessus).

Exemple 

```
.jeSuisParent
  color: $someColor
  
  .jeSuisEnfant
    color: yellow
```

### Bundlers

* [Rollup](https://github.com/rollup/rollup)
* [Parcel](https://parceljs.org)
* [Webpack](https://webpack.js.org)
* [Webstarter Kit](https://developers.google.com/web/tools/starter-kit/)
* [Gulp](https://gulpjs.com)



## Javascript

### Vanilla JS

* Variables / Constantes
  - VAR 
  - CONST (ES6) 
  - LET (ES6)

* Conditions
  - IF .. ELSE
  - SWITCH ... CASE
  - Ternaire ( condition ? vrai : faux)

* Boucles 
  - for
  - while
  - do while 
  - for..in
  - for..of

* Fonctions
  - Fonction anonyme
  - Fonction nommée
  - Arrow fonction 
  - Fonction d'haut niveau (https://www.youtube.com/watch?v=BMUiFMZr7vk) 
  - Fermeture (*Closure*)
  - Encapsulation
  - Return, break, continue

* DOM
  - selectors (ex. querySelector, getElementById, getElementbyClass, querySelectorAll)
  - Fonctions: 
    - createElement
    - classlist (add, remove, toggle)
    - setAttribute
    - parentNode, childNode  

* Evenements
  - Mouse (click, wheel)
  - Window (scroll)
  - Keyboard (keyup, keydown, keypress)
  - Input (change, submit)
  - preventDefault

* Regex

https://regex101.com

  - Fonctions:
    - match()
    - search()
    - split()
    - replace()
    

* Tableaux 
  - Proprietés
    - length
    - Constructor
    - Prototype
  - Fonctions: 
    - map()
    - reduce()
    - indexOf()
    - find()
    - findIndex()
    - filter
    - pop()
    - push()
    - reverse()
    - splice()
    - join()
    - toString()
    - 

* Objets / dictionnaires
  ```
  var Objet = {
    clé : proprieté;
    deuxiemeClé : proprieté
  }
  ```


#### POO

Terminologie:

* **Espace de noms**
Un conteneur qui permet aux développeurs d'empaqueter les différentes fonctionnalités d'un programme sous un même nom d'application.

* **Classe**
Définit les caractéristiques de l'objet.

* **Objet**
Une instance (un « exemplaire ») d'une classe.

* **Propriété**
Une caractéristique d'un objet (sa couleur par exemple).

* **Méthode**
Une capacité d'un objet (changer de couleur par exemple).

* **Constructeur**
Une méthode appelée au moment de l'instantiation.

* **Héritage**
Une classe peut hériter des caractéristiques et des fonctionnalités d'une autre classe.

* **Encapsulation**
Une classe définit uniquement les caractéristiques de son objet, une méthode définit uniquement la façon dont elle s'exécute. On regroupe donc les données et les méthodes qui utilisent ces données.

* **Abstraction**
La conjonction entre l'utilisation de l'héritage, de méthodes ou de propriétés d'un objet pour simuler un modèle de la réalité.

* **Polymorphisme**
Poly signifie « plusieurs » et morphisme signifie « formes ». Cela signifie que différentes classes peuvent définir la même méthode ou la même propriété.

#### Libraries

#### Ajax

### Vue.js

### Cycle.js

### Node.js

## Miscellaneous 
