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


### Programmation Orientée Objet

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

Exemple:
```
class Player
{
    constructor() {
        this._x = (MAP_COLUMNS - PLAYER_WIDTH) / 2;
        this._y = MAP_ROWS - (PLAYER_HEIGHT + 1);
    }

    // Returns the X position of the player
    get x() {
        return this._x;
    }

    // Sets the X position of the player, checking bounds to make sure the player doesn't exit the screen
    set x(newX) {
        if (newX > (MAP_COLUMNS - PLAYER_WIDTH))
            this._x = MAP_COLUMNS - PLAYER_WIDTH;
        else if (newX < 0)
            this._x = 0;
        else
            this._x = newX;
    }


```


### Libraries

* [Lodash](https://lodash.com)
* [JQuery](http://jquery.com)
* [Lethargy](https://github.com/d4nyll/lethargy)
* [Tween](https://github.com/tweenjs/tween.js/)
* [Animejs](http://animejs.com)

### Ajax

Ajax (Asynchronous JavaScript and XML) est la technologie utilisée pour ce faire. Elle repose sur l'objet XMLHttpRequest qui permet de se connecter à un serveur, de lui envoyer des données et d'en recevoir en retour. Elle utilise le protocole HTTP ; le navigateur émet une requête et attend une réponse du serveur. Cette requête est asynchrone, elle ne bloque pas le navigateur, qui peut continuer à interagir avec l'utilisateur, et sera notifié lors du retour du serveur.

Effectuer une requête xhr
L'objet XMLHttpRequest permet d'effectuer des requêtes HTTP dans le navigateur. Il dispose de nombreuses méthodes afin d'indiquer le verbe, la ressource, les headers, le body et de s'abonner à la réponse du serveur.

#### XHR

**Requête ajax GET** :

```
var xhr = new XMLHttpRequest();
xhr.open('GET', 'http://www.thebeatles.com/news', true);
xhr.setRequestHeader('Content-Type', 'application/json');

xhr.onload = function() {
  var status = xhr.status;
  var body = JSON.parse(xhr.responseText);

  /* use body as a classic dictionnary */
}
xhr.send();
```

La méthode open de cet objet permet de configurer la requête, d'abord le verbe, ensuite l'URI et enfin un booléen indiquant qu'il s'agit d'une requête asynchrone. Les requêtes synchrones sont dépréciées dans les navigateurs modernes. Bloquer le code en attendant la réponse du serveur est considéré comment nuisant grandement à l'expérience utilisateur (puisque cela revient à blqouer complétement le navigateur tant que le serveur n'a pas répondu).

La méthode onload permet de s'abonner à la réponse du serveur. Dès que celle-ci advient, la méthode est exécutée et les attributs responseText et status de la requête sont disponibles. Afin de transformer la réponse obtenue en objet JavaScript, il est possible d'utiliser la méthode parse de la variable globale JSON.

La méthode send permet d'effectuer l'appel.

**Requêtes ajax POST** :

```
var xhr = new XMLHttpRequest();
xhr.open("POST", "http://www.thebeatles.com/subscribe", true);
xhr.setRequestHeader("Content-Type", "application/json");

xhr.onload = function() {
  var body = JSON.parse(xhr.responseText);
  var status = xhr.status;
}
xhr.send(JSON.stringify({name:"contact@mail.com"}));
```

La même logique s'applique lors de l'envoi de données au serveur, seule le verbe utilisé change et la méthode send peut alors recevoir une chaîne de caractère à transmettre au serveur. Ici aussi, le recours à JSON permet de transformer un objet JavaScript pour le transmettre au format texte au serveur.

#### FETCH

L'objet fetch a été ajouté récemment aux navigateurs dans l'optique de simplifier les requêtes Ajax. Comme certains navigateurs ne le supportent pas, il peut être nécessaire d'ajouter un polyfill pour ajouter cette fonctionnalité à ces anciens navigateurs. Fetch présentes deux différences majeures par rapport à xhr :

il retourne un stream plutôt qu'une réponse immédiate
il fonctionne avec des promesses, à la place de callback
Requête fetch GET :
```
fetch('http://www.thebeatles.com/news')
.then(function(response) {
    return response.json();
})
.then(function(body) {
    /* use body as a classic dictionnary */
});
```

Requête fetch POST :

```
fetch('http://www.thebeatles.com/subscribe', {
    method: 'POST',
    json: JSON.stringify({name:"contact@mail.com"})
}).then(function(response) {
    return response.json();
})
.then(function(body) {
    /* use body as a classic dictionnary */
});
```

L'objet response est de stype stream, celui-ci représente un flux de données. Il permet de choisir comment les données d'un serveur doivent être consommées. Avec l'appel response.json() le flux est lu en entier et retourné au format JSON. Si la requête retourne un fichier volumineux, il est possible de le lire morceau après morceau afin de ne pas télécharger l'intégralité de celui-ci dans la mémoire du navigateur.

#### Promesses

L'objet Promise a été inventé par jQuery avant d'être introduit en natif dans le langage. Il représente la réussite éventuelle, ou l'échec éventuel, d'une opération asynchrone et sa valeur de retour. Comme un callback traditionnel, il permet de s'abonner à cette réussite avec une fonction ou un échec avec une autre fonction dont l'une des deux sera invoquée à la résolution de l'opération asynchrone.

Très utilisées pour les appels serveur — l'application récupère la main et peut effectuer d'autres opérations en attendant la réponse — les promesses peuvent également servir à ordonner des opérations asynchrones de tout genre plus facilement.

Comme fetch et les stream, son support est encore partiel sur les navigateurs et il est parfois nécessaire d'ajouter un polyfill pour ce faire.

Une promesse propose deux méthodes pour s'abonner à son futur résultat, then et catch. La première permet de s'abonner au succès de l'appel, la second à son échec. La spécification A+ détaille ce fonctionnement, notamment :

les promesse sont thenable, il est possible de chaîner plusieurs then qui attendront que le précédent soit résolu avant de se résoudre elles-mêmes avec son résultat
un catch en bout de chaîne capture toutes les erreurs pouvant se produire sur la chaîne, et celle-ci est intérompue dès qu'une erreur se produit
Création d'une promesse, résolue si l'utilisateur clique sur le <body> en moins de 5 secondes :

```
var clicked = new Promise(function(resolve, reject) {
    setTimeout(reject, 5000);

    var start = new Date();
    document.body.addEventListener('click', function(e) {
        var end = new Date();
        resolve(end.getTime() - start.getTime());
    })
});
```

Les promesses A+ intégrées au langage (norme respectée par jQuery depuis sa version 3.0) prennent deux fonctions en paramètres, resolve et reject. L'une de ces deux fonctions — et une seule des deux — doit être appelée lorsque l'opération asynchrone encapsulée est terminée, resolve si c'est avec succès, reject sinon.

Une promesse ne peut être résolue qu'une fois. Dans cet exemple, soit l'utilisateur clique sur le body dans les 5 secondes, et la promesse est un succès, soit, ce n'est pas le cas, et le timeout déclenche un échec. Bien que l'utilisateur puisse cliquer à nouveau sur le body, seul le premier appel de la méthode resolve ou reject résoudra la promesse, les suivants sont ignorés. Une fois dans un état, succès ou échec, une promesse ne peut plus en changer.

Une fois cette promesse créée, le code qui l'utilise s'abonne à son résultat futur. Avec then il indique quelles opérations suivront cette opération quand elle sera terminée avec succès. Avec catch, quelles opérations suivront si elle se termine en erreur.

Abonnement à une promesse :

```
clicked.then(function(time) {
    console.log(time);
});

clicked.then(function(time) {
    return (time < 1000)
}).then(function(quick) {
    if (quick)
        console.log('quick click');
}).catch(console.error);

```

Une promesse peut avoir plusieurs souscriptions. Il est même possible de s'abonner alors qu'elle est déjà résolue, le then ou le catch étant alors immédiatement invoqués.

Les then sont chaînables, un then peut retourner une valeur ou une promesse. S'il retourne une promesse, le then suivant attendra le succès de cette promesse avant de s'exécuter à son tour. Le catch capture les erreurs (throw ou reject). Si un then est placé après lui, il reprendra la main une fois l'erreur gérée par le catch.

Ici, à titre d'exemple, si le temps de clic est inférieur à une seconde, un résultat est retourné, capturé à son tour par une nouvelle promesse qui reçoit le résultat de celle qui l'a précédé. Un exemple plus courant, est celui ou un appel asynchrone est retourné, dont le résultat est passé au then suivant quand l'appel succède ou échoue.

## Vue.js

## Cycle.js

## Node.js

## Miscellaneous 
