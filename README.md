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



### PUG (JADE)

### SCSS / SASS 

## Javascript

### Vanilla JS

#### POO

#### Libraries

### Vue.js

### Cycle.js

### Node.js

## PHP

### POO

### Symfony


## Miscellaneous 
