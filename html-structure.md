---
title: HTML - Structure d'un site web
date: 2021-10-18
cover: assets/images/website-parts.png
---

# HTML - Structure d'un site web 

Sylvain Schellenberger

## Principales parties <!-- .slide: class="split-panel-50-50" -->

```html
<body>
	<header></header>
	<main></main>
	<footer></footer>
</body>
```

![Principales parties d'un site web: header, main, footer.](assets/images/website-parts.png) 

## Le plus important <!-- .slide: class="split-panel-50-50" -->

```html
<main>
	<h1>Kiwi Coffee Revolution</h1>
	<p id="tagline">Lorem ipsum dolor - Sit amet</p>
</main>
```

![Le main contient le titre de la page ainsi que la plupart des informations.](assets/images/website-main.png)

Un seul `main`!

### Les sections <!-- .slide: class="split-panel-50-50" -->

```html
<main>
	<section>
		<h1>Kiwi Coffee Revolution</h1>
		<p id="tagline">Lorem ipsum dolor - Sit amet</p>
	</section>
	<section>
		<h2>Services</h2>
	</section>
	<section>
		<h2>Nos produits</h2>
	</section>
</main>
```

![Les sections divisent le main en plusieurs rubriques distinctes.](assets/images/website-sections.png)

Un seul `h1` recommandé!

### Les articles

```html
<section>
	<h2>Nos produits</h2>
	<article>
		<h3>Pur Arabica</h3>
		<img src="images/arabica.png">
	</article>
	<article>
		<h3>Robusta</h3>
		<img src="images/robusta.png">
	</article>
</section>
```

![Chaque article représente un seul produit.](assets/images/website-articles.png)

## L'en-tête du site

```html [2-4]
<body>
	<header>
		<img src="images/logo.png" alt="Kiwi Coffee Revolution"/>
	</header>
	<nav>
	</nav>
</body>
```

![L'en-tête du site contient souvent un logo et des liens de navigation.](assets/images/website-header.png)

### La navigation 

```html [3-7]
<header>
	<img src="images/logo.png" alt="Neskawa"/>
	<nav>
		<ul>
			<li><a href="a-propos.html">A Propos</a></li>
		</ul>
	<nav>
</header>
```

![La navigation contient une liste de liens de navigation](assets/images/website-nav.png)

### Les ancres <!-- .slide: class="split-panel-50-50" -->

```html
<ul>
	<li><a href="#accueil">Accueil</a></li>
	<li><a href="#produits">Produits</a></li>
</ul>

<section id="accueil">
	<h1>Kiwi Coffee Revolution</h1>
</section>
<section id="produits">
	<h2>Nos produits</h2>
</section>
```

![Les ancres centrent le navigateurs sur les sections dont les id correspondent à leur cible](assets/images/anchors.png)

## Pied de page

```html
<footer>
	<div id="adress"></div>
	<div id="facebook-feed"></div>
	<div id="twitter-feed"></div>
	<div id="newsletter"></div>
	<p id="copyright">&copy; Kiwi Coffee Revolution 2021</p>
</footer>
```

![Le footer contient généralement le copyright, en plus d'informations de contact.](assets/images/website-footer.png)

### Navigation de pied de page

```html
<footer>
	<nav>
		<li><a href="#">Accueil</a></li>
	</nav>
</footer>
```

## Ressources

- Structure de site Web et de document, Mozilla Developers Network, [https://developer.mozilla.org/fr/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure](https://developer.mozilla.org/fr/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)