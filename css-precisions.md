---
title: CSS - Sélecteurs
date: 2021-10-18
cover: assets/images/last-child.png
---

# Sélecteurs CSS

## Descendance des éléments HTML

```html
<html>
	<body>
		<h1>Neskawa</h1>
		<p>Du bon kawa</p>
		<p>Issu du commerce (presque) équitable et de l'agriculture (un peu) biologique!</p>
	</body>
</html>
``` 
<!-- .element: style="display: inline-block; width: 45%;" -->

![html est le parent de body, qui est le parent de h1 et p, qui sont les descendants de html.](assets/images/html-descendance-4.png) 
<!-- .element: style="display: inline-block; width: 45%;" -->

## Enfants directs

```css
html > body
```

![](assets/images/direct-child.png)

## Descendant

```css
html p
```
![](assets/images/descendants.png)

## Frères et soeurs (adjacence)

```css
h1 + p
```

![](assets/images/adjacent-sibling.png)

## Frères et soeurs (général)

```css
h1 ~ p
```

![](assets/images/all-siblings.png)

## Plusieurs éléments

```css
h1, p
```

![](assets/images/several.png)

## Pseudo-éléments

```css
p::last-child
```

![](assets/images/last-child.png)

##

```css
h1::last-of-type
```

![](assets/images/last-of-type.png)

## Pseudo-classes

```css
a:hover {
	text-decoration: underline dotted;
}
```

<iframe style="backrgound-color: white;" srcdoc="
<head>
	<style>
		a:hover {
			text-decoration: underline dotted;
		}
	</style>
</head>
<body>
	<a href=#>Achète moi!</a>
</body>"></iframe>

##

```css
a:visited {
	color: red;
}
```

<iframe style="background-color: white;" srcdoc="
<head>
	<style>
		a:visited {
			color: red;
		}
	</style>
</head>
<body>
	<a href=#>Achète moi!</a>
</body>"></iframe>

## Ressources

- Sélecteurs CSS, Mozilla Developers Network: [https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/Selectors](https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/Selectors)
- CSS Diner, Flukeout: [https://flukeout.github.io/](https://flukeout.github.io/)

---

# La cascade

## Surcharge

```css
body {
	color: red;
	color: blue;
}
```

<iframe style="overflow: visible; width: 100%; height: 60vh;" 
		srcdoc="
				<head>
					<style>
						body {
							color: red;
							color: blue;
						}
					</style>
				</head>
				<body>
					<h1>Bob l'éponge</h1>
					<p>Cuisinier souriant</p>
					<h2>Sa vie</h2>
					<ul>
						<li>Habite à <strong>Bikini Bottom</strong></li>
						<li>Travaille au <strong>Crabe Croustillant</strong></li>
					</ul>
				</body>
			">
	</iframe>
	
## Heritage

```css
body {
	color: rgb(32, 32, 128);
}
```

![Les propriétés du body ruissellent dans ses éléments enfants](assets/images/cascading.png)

##

<iframe style="overflow: visible; width: 100%; height: 60vh;" 
		srcdoc="
				<head>
					<style>
						body {
							background-color: #c4c4c4;
							color: rgb(32, 32, 128);
						}
					</style>
				</head>
				<body>
					<h1>Bob l'éponge</h1>
					<p>Cuisinier souriant</p>
					<h2>Sa vie</h2>
					<ul>
						<li>Habite à <strong>Bikini Bottom</strong></li>
						<li>Travaille au <strong>Crabe Croustillant</strong></li>
					</ul>
				</body>
			">
	</iframe>
	
## Surcharger l'héritage

```css [5-7]
body {
	background-color: #c4c4c4;
	color: rgb(32, 32, 128);
}

h1 {
	color: gold;
}
```

![La règle sur l'élément h1 surcharge la règle sur le body](assets/images/css-overwrite.png)

##

<iframe style="overflow: visible; width: 100%; height: 60vh;" 
		srcdoc="
				<head>
					<style>
						body {
							background-color: #c4c4c4;
							color: rgb(32, 32, 128);
						}
						h1 {
							color: gold;
						}
					</style>
				</head>
				<body>
					<h1>Bob l'éponge</h1>
					<p>Cuisinier souriant</p>
					<h2>Sa vie</h2>
					<ul>
						<li>Habite à <strong>Bikini Bottom</strong></li>
						<li>Travaille au <strong>Crabe Croustillant</strong></li>
					</ul>
				</body>
			">
	</iframe>

## Spécificité

```html
<h1>Bob l'éponge</h1>
<p id="tagline">Cuisinier souriant</p>
<p>Héros de dessin animé, ainsi que de plusieurs films.</p>
```

```css
#tagline {
	font-size: 24px;
}
p {
	font-size: 12px;
}
```

##

<iframe style="overflow: visible; width: 100%; height: 60vh;" 
		srcdoc="
				<head>
					<style>
						#tagline {
							font-size: 24px;
						}
						p {
							font-size: 12px;
						}
					</style>
				</head>
				<body>
					<h1>Bob l'éponge</h1>
					<p id="tagline">Cuisinier souriant</p>
					<p>Héros de dessin animé, ainsi que de plusieurs films.</p>
				</body>
			">
	</iframe>

## Reset et Normalize

