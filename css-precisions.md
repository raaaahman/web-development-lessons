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