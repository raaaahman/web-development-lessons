---
title: CSS - Flexbox
date: 2021-10-24
cover: assets/images/flex-direction.png
---

# CSS - Flexbox

Sylvain Schellenberger

## Disposition <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<div class="container">
	<article>Projet 1</article>
	<article>Projet 2</article>
	<article>Projet 3</article>
</div>
```

```css
.container {
	display: flex;
}
```

</div>

<iframe srcdoc="<head>
    <style>
        .container {
            display: flex;
        }
        article {
            box-sizing: border-box;
            text-align: center;
            border: 1px solid blue;
        }
        article:nth-child(odd) {
            background-color: lightblue;
            color: darkslategray;
        }
        article:nth-child(even) {
            background-color: cornflowerblue;
            color: whitesmoke;
        }
    </style>
</head>
<body>
    <div class=container>
        <article>Projet 1</article>
        <article>Projet 2</article>
        <article>Projet 3</article>
    </div>
</body>"></iframe>

## Redimensionnement des objets <!-- .slide: class="split-panel-50-50" -->

```css
article {
	flex-grow: 1;
	flex-shrink: 0;
	flex-basis: 50%;
}
```

<iframe srcdoc="
<head>
	<style>
        .container {
            display: flex;
        }
        article {
            box-sizing: border-box;
            border: 1px solid blue;
            text-align: center;
            flex-grow: 1;
            flex-shrink: 0;
            flex-basis: 50%;
        }
        article:nth-child(odd) {
            background-color: lightblue;
            color: darkslategray;
        }
        article:nth-child(even) {
            background-color: cornflowerblue;
            color: whitesmoke;
        }
    </style>
</head>
<body>
    <div class=container>
        <article>Projet 1</article>
        <article>Projet 2</article>
        <article>Projet 3</article>
    </div>
</body>"></iframe>

## Retour à ligne <!-- .slide: class="split-panel-50-50" -->

```css
.container {
	display: flex;
	flex-wrap: wrap;
}
```

<iframe srcdoc="<head>
    <style>
        .container {
            display: flex;
            flex-wrap: wrap;
        }
        article {
            box-sizing: border-box;
            border: 1px solid blue;
            text-align: center;
            flex-grow: 1;
            flex-shrink: 0;
            flex-basis: 50%;
        }
        article:nth-child(odd) {
            background-color: lightblue;
            color: darkslategray;
        }
        article:nth-child(even) {
            background-color: cornflowerblue;
            color: whitesmoke;
        }
    </style>
</head>
<body>
    <div class=container>
        <article>Projet 1</article>
        <article>Projet 2</article>
        <article>Projet 3</article>
    </div>
</body>"></iframe>

## Direction <!-- .slide: class="split-panel-50-50" -->

```css
.container {
	display: flex;
	flex-direction: column;
}
```

<iframe srcdoc="<head>
<style>
        .container {
            display: flex;
            flex-wrap: wrap;
			flex-direction: column;
        }
        article {
            box-sizing: border-box;
            border: 1px solid blue;
            text-align: center;
            flex-grow: 1;
            flex-shrink: 0;
            flex-basis: 50%;
        }
        article:nth-child(odd) {
            background-color: lightblue;
            color: darkslategray;
        }
        article:nth-child(even) {
            background-color: cornflowerblue;
            color: whitesmoke;
        }
    </style>
</head>
<body>
    <div class=container>
        <article>Projet 1</article>
        <article>Projet 2</article>
        <article>Projet 3</article>
    </div>
</body>"></iframe>

## Alignement (axe principal) <!-- .slide: class="split-panel-50-50" -->

```css
.container {
    height: 200px;
    display: flex;
	flex-direction: column;
    justify-content: space-between;
}
```

<iframe srcdoc="
<head>
	<style>
        .container {
            height: 200px;
            display: flex;
			flex-direction: column;
            justify-content: space-between;
        }
        article {
            box-sizing: border-box;
            border: 1px solid blue;
            text-align: center;
        }
        article:nth-child(odd) {
            background-color: lightblue;
            color: darkslategray;
        }
        article:nth-child(even) {
            background-color: cornflowerblue;
            color: whitesmoke;
        }
    </style>
</head>
<body>
    <div class=container>
        <article>Projet 1</article>
        <article>Projet 2</article>
        <article>Projet 3</article>
    </div>
</body>"></iframe>

## Alignement (axe croisé) <!-- .slide: class="split-panel-50-50" -->

```css
.container {
    height: 200px;
    display: flex;
	flex-direction: column;
    justify-content: space-between;
    align-items: center;
}
```

<iframe srcdoc="
<head>
	<style>
        .container {
            height: 200px;
            display: flex;
			flex-direction: column;
            justify-content: space-between;
            align-items: center;
        }
        article {
            box-sizing: border-box;
            border: 1px solid blue;
            text-align: center;
        }
        article:nth-child(odd) {
            background-color: lightblue;
            color: darkslategray;
        }
        article:nth-child(even) {
            background-color: cornflowerblue;
            color: whitesmoke;
        }
    </style>
</head>
<body>
    <div class=container>
        <article>Projet 1</article>
        <article>Projet 2</article>
        <article>Projet 3</article>
    </div>
</body>"></iframe>

## Directions et alignement

![L'axe principal est vertical lorsque la direction est en colonne, et horizontal lorsque la direction est en rang. Pour l'axe croisé, c'est l'inverse](assets/images/flex-direction.png)

## Mise en pratique <!-- .slide: class="split-panel-50-50" -->

```css
.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: stretch;
}
.container > article {
    box-sizing: border-box;
    flex-basis: 30%;
    background-color: lightblue;
    padding: 1em;
}
img {
    width: 100%;
}
```


<iframe srcdoc="
<head>
	<style>
        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: stretch;
        }
        .container > article {
            box-sizing: border-box;
            flex-basis: 30%;
            background-color: lightblue;
            padding: 1em;
        }
        img {
            width: 100%;
        }
    </style>
</head>
<body>
    <div class=container>
        <article>
            <h3>Projet 1</h3>
            <img src=https://via.placeholder.com/300 alt=Projet1 >
            <p>Nemo quaeso miretur, si post exsudatos labores itinerum longos congestosque adfatim commeatus.</p>
        </article>
        <article>
            <h3>Projet 2</h3>
            <img src=https://via.placeholder.com/300 alt=Projet2 >
            <p>Ut enim benefici liberalesque sumus, non ut exigamus gratiam .</p>
        </article>
        <article>
            <h3>Projet 3</h3>
            <img src=https://via.placeholder.com/300 alt=Projet3 >
            <p>Illud tamen clausos vehementer angebat quod captis navigiis, quae frumenta vehebant per flumen.</p>
        </article>
    </div>
</body>"></iframe>

## Ressources

- Flexbox, Mozilla Developers Network, [https://developer.mozilla.org/fr/docs/Learn/CSS/CSS_layout/Flexbox](https://developer.mozilla.org/fr/docs/Learn/CSS/CSS_layout/Flexbox)
- A complete Guide to Flexbox, CSS Tricks, [https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- Flexbox Froggy, [https://flexboxfroggy.com/#fr](https://flexboxfroggy.com/#fr)
- Solved by flexbox, Philip Walton, [https://philipwalton.github.io/solved-by-flexbox/](https://philipwalton.github.io/solved-by-flexbox/)