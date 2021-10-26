---
title: CSS - La cascade
date: 2021-10-25
cover: assets/images/waterfall.jpeg
---

# CSS - La cascade

![La cascade éclabousse Bruce.](assets/images/waterfall.jpeg)

Sylvain Schellenberger

## Ordre d'apparition <!-- .slide: class="split-panel-50-50" -->

```css
p {
	color: red;
	color: green;
}

p {
	color: blue;
}
```

<iframe style="overflow: visible; width: 100%;" 
	srcdoc="
			<head>
				<style>
					p {
						color: red;
						color: green;
					}
					p {
						color: blue;
					}
				</style>
			</head>
			<body>
				<h1>Bob l'éponge</h1>
				<p>Cuisinier souriant</p>
				<p>Héros de dessin animé, ainsi que de plusieurs films.</p>
				<h2>Sa vie</h2>
				<p>Il habite à Bikini Bottom</p>
				<p>Travaille au Crabe Croustillant</p>
			</body>
		">
	</iframe>
	
## Spécificité <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<h1>Bob l'éponge</h1>
<p id="tagline">Cuisinier souriant</p>
<p>Héros de dessin animé, ainsi que de plusieurs films.</p>
```

```css
#tagline {
	color: gold;
}
p {
	color: blue;
}
```

</div>

<iframe style="overflow: visible; width: 100%;" 
		srcdoc="
				<head>
					<style>
						#tagline {
							color: gold;
						}
						p {
							color: blue;
						}
					</style>
				</head>
			<body>
				<h1>Bob l'éponge</h1>
				<p id=tagline>Cuisinier souriant</p>
				<p>Héros de dessin animé, ainsi que de plusieurs films.</p>
				<h2>Sa vie</h2>
				<p>Il habite à Bikini Bottom</p>
				<p>Travaille au Crabe Croustillant</p>
			</body>
			">
	</iframe>
	
## Spécificité, les priorités <!-- .slide: class="split-panel-50-50" -->

1. Les sélecteurs d'identifiant (ex: `#tagline`)
2. Les sélecteurs de classe (ex: `.container`)
3. Les sélecteurs d'éléments (ex: `p`)

## Héritage <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<body>
	<h1>Bob l'éponge</h1>
	<p id=tagline>Cuisinier souriant</p>
	<p>Héros de dessin animé, ainsi que de plusieurs films.</p>
	<h2>Sa vie</h2>
	<p>Il habite à Bikini Bottom</p>
	<p>Travaille au Crabe Croustillant</p>
</body>
```

```css
body {
	color: blue;
}
```

</div>

<iframe style="overflow: visible; width: 100%;" 
		srcdoc="
				<head>
					<style>
						body {
							color: blue;
						}
					</style>
				</head>
				<body>
					<h1>Bob l'éponge</h1>
					<p id=tagline>Cuisinier souriant</p>
					<p>Héros de dessin animé, ainsi que de plusieurs films.</p>
					<h2>Sa vie</h2>
					<p>Il habite à Bikini Bottom</p>
					<p>Travaille au Crabe Croustillant</p>
				</body>
			">
	</iframe>
	
## Surcharger l'héritage <!-- .slide: class="split-panel-50-50" -->

```css
h1 {
	color: gold;
}

body {
	color: blue;
}
```

<iframe style="overflow: visible; width: 100%;" 
		srcdoc="
				<head>
					<style>
						h1 {
							color: gold;
						}
						body {
							color: blue;
						}
					</style>
				</head>
				<body>
					<h1>Bob l'éponge</h1>
					<p>Cuisinier souriant</p>
					<p>Héros de dessin animé, ainsi que de plusieurs films.</p>
					<h2>Sa vie</h2>
					<p>Habite à Bikini Bottom</p>
					<p>Crabe Croustillant</p>
				</body>
			">
	</iframe>
	
## Propriétés héritables <!-- .slide: class="split-panel-50-50" -->

<div>

Héritables:

- color
- font-family, font-size, font-weight
- text-align

</div>

<div>

Non héritables:

- background-color
- margin, padding, border
- display
- width, height

</div>

## Importance <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<h1 id="pagetitle">Bob l'éponge</h1>
<p>Cuisinier souriant</p>
```

```css
h1 {
	color: red !important;
}
#pagetitle {
	color: gold;
}
```

</div>

<iframe style="overflow: visible; width: 100%;" 
		srcdoc="
				<head>
					<style>
						h1 {
							color: red !important;
						}
						#pagetitle {
							color: gold;
						}
						body {
							color: blue;
						}
											</style>
				</head>
				<body>
					<h1 id=pagetitle>Bob l'éponge</h1>
					<p>Cuisinier souriant</p>
					<p>Héros de dessin animé, ainsi que de plusieurs films.</p>
					<h2>Sa vie</h2>
					<p>Habite à Bikini Bottom</p>
					<p>Crabe Croustillant</p>
				</body>
			">
	</iframe>

## Normalize.css

```html
<link rel="stylesheet" href="normalize.css">
<link rel="stylesheet" href="mon-style.css">
```

[https://necolas.github.io/normalize.css/latest/normalize.css](https://necolas.github.io/normalize.css/latest/normalize.css)

## Ressources

- Cascade et héritage, Mozilla Developers Network, [https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance](https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance)
