---
title: CSS - Le positionnement
date: 2021-10-25
cover:
---

# CSS - Le positionnement

Sylvain Schellenberger

## Le flux HTML <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<article>
	<header>
		<h3>Projet 1</h3>	
	</header>
	<img src="https://via.placeholder.com/400x150">
	<p>Duplexque isdem diebus acciderat malum, [...]</p>
</article>
```

```css
* {
	position: static;
}
```

</div>

<iframe style="background-color: white;" srcdoc="
<head>
	<style>
		article {
			background-color: khaki;
			border: 1px solid goldenrod;
			padding: 1em;
		}
		article > * {
			margin: 0.25em;
			background-color: lightblue;
			border: 1px solid blue;
			padding: 0.5em;
		}
		article > * > * {
			background-color: indianred;
			border: 1px solid firebrick;
		}
	</style>
</head>
<body>
	<article>
		<header>
			<h3>Projet 1</h3>	
		</header>
		<img src=https://via.placeholder.com/400x150>
		<p>Duplexque isdem diebus acciderat malum, quod et Theophilum insontem atrox interceperat casus, et Serenianus dignus exsecratione cunctorum.</p>
	</article>
</body>"></iframe>

## Position relative <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<article>
	<header>
		<h3>Projet 1</h3>	
	</header>
	<img src="https://via.placeholder.com/400x150">
	<p>Duplexque isdem diebus acciderat malum, [...]</p>
</article>
```

```css
h3 {
	position: relative;
	top: 120px;
}
```

</div>

<iframe style="background-color: white;" srcdoc="
<head>
	<style>
		article {
			background-color: khaki;
			border: 1px solid goldenrod;
			padding: 1em;
		}
		article > * {
			margin: 0.25em;
			background-color: lightblue;
			border: 1px solid blue;
			padding: 0.5em;
		}
		article > * > * {
			background-color: indianred;
			border: 1px solid firebrick;
		}
		h3 {
			position: relative;
			top: 120px;
		}
	</style>
</head>
<body>
	<article>
		<header>
			<h3>Projet 1</h3>	
		</header>
		<img src=https://via.placeholder.com/400x150>
		<p>Duplexque isdem diebus acciderat malum, quod et Theophilum insontem atrox interceperat casus, et Serenianus dignus exsecratione cunctorum.</p>
	</article>
</body>"></iframe>

## Position absolue <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<article>
	<header>
		<h3>Projet 1</h3>	
	</header>
	<img src="https://via.placeholder.com/400x150">
	<p>Duplexque isdem diebus acciderat malum, [...]</p>
</article>
```

```css
h3 {
	position: absolute;
	top: 120px;
}
```

</div>

<iframe style="background-color: white;" srcdoc="
<head>
	<style>
		article {
			background-color: khaki;
			border: 1px solid goldenrod;
			padding: 1em;
		}
		article > * {
			margin: 0.25em;
			background-color: lightblue;
			border: 1px solid blue;
			padding: 0.5em;
		}
		article > * > * {
			background-color: indianred;
			border: 1px solid firebrick;
		}
		h3 {
			position: absolute;
			top: 120px;
		}
	</style>
</head>
<body>
	<article>
		<header>
			<h3>Projet 1</h3>	
		</header>
		<img src=https://via.placeholder.com/400x150>
		<p>Duplexque isdem diebus acciderat malum, quod et Theophilum insontem atrox interceperat casus, et Serenianus dignus exsecratione cunctorum.</p>
	</article>
</body>"></iframe>

## Contexte de positionnement <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<div class="wrapper">
	<header class="overlay">
		<h3>Projet 1</h3>
	</header>
	<img src=https://via.placeholder.com/400x150>
</div>
```

```css
.wrapper {
	position: relative;
}
.overlay {
	position: absolute;
	left: 0;
	right: 0;
	bottom: 0.5em;
}
```

</div>

<iframe style="background-color: white;" srcdoc="
<head>
	<style>
		* {
			box-sizing: border-box;
		}
		article {
			background-color: khaki;
			border: 1px solid goldenrod;
			padding: 1em;
		}
		article > * {
			margin: 0.25em;
			background-color: lightblue;
			border: 1px solid blue;
			padding: 0.5em;
		}
		article > * > * {
			background-color: indianred;
			border: 1px solid firebrick;
		}
		.wrapper {
			position: relative;
		}
		.overlay {
			position: absolute;
			left: 0;
			right: 0;
			bottom: 0.5em;
		}
	</style>
</head>
<body>
	<article>
		<div class=wrapper>
			<header class=overlay>
				<h3>Projet 1</h3>
			</header>
			<img src=https://via.placeholder.com/400x150>
		</div>
		<p>Duplexque isdem diebus acciderat malum, quod et Theophilum insontem atrox interceperat casus, et Serenianus dignus exsecratione cunctorum.</p>		
	</article>
</body>"></iframe>

## Position fixe <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<nav>
	<ul>
		<li><a href="#projets">Mes Projets</a></li>
	</ul>
</nav>
```

```css
nav {
	position: fixed;
	top: 0;
	right: 0;
	left: 0;
	height: 40px;
}
nav + * {
	position: relative;
	top: 40px;
}
```

</div>

<iframe srcdoc="<head>
	<style>
		nav {
			background-color: lightgrey;
			position: fixed;
			top: 0;
			right: 0;
			left: 0;
			height: 40px;
		}
		nav + * {
			position: relative;
			top: 40px;
		}
	</style>
</head>
<body>
	<nav>
		<ul>
			<li><a href=#projets>Mes Projets</a></li>
		</ul>
	</nav>
	<div>
		<p>Duplexque isdem diebus acciderat malum, quod et Theophilum insontem atrox interceperat casus, et Serenianus dignus exsecratione cunctorum, innoxius, modo non reclamante publico vigore, discessit.</p>
		<p>Haec igitur Epicuri non probo, inquam. De cetero vellem equidem aut ipse doctrinis fuisset instructior est enim, quod tibi ita videri necesse est, non satis politus iis artibus, quas qui tenent, eruditi appellantur aut ne deterruisset alios a studiis. quamquam te quidem video minime esse deterritum.</p>
		<p>Orientis vero limes in longum protentus et rectum ab Euphratis fluminis ripis ad usque supercilia porrigitur Nili, laeva Saracenis conterminans gentibus, dextra pelagi fragoribus patens, quam plagam Nicator Seleucus occupatam auxit magnum in modum, cum post Alexandri Macedonis obitum successorio iure teneret regna Persidis, efficaciae inpetrabilis rex, ut indicat cognomentum.</p>
		<p>Horum adventum praedocti speculationibus fidis rectores militum tessera data sollemni armatos omnes celeri eduxere procursu et agiliter praeterito Calycadni fluminis ponte, cuius undarum magnitudo murorum adluit turres, in speciem locavere pugnandi. neque tamen exiluit quisquam nec permissus est congredi. formidabatur enim flagrans vesania manus et superior numero et ruitura sine respectu salutis in ferrum.</p>
		<p>Ob haec et huius modi multa, quae cernebantur in paucis, omnibus timeri sunt coepta. et ne tot malis dissimulatis paulatimque serpentibus acervi crescerent aerumnarum, nobilitatis decreto legati mittuntur: Praetextatus ex urbi praefecto et ex vicario Venustus et ex consulari Minervius oraturi, ne delictis supplicia sint grandiora, neve senator quisquam inusitato et inlicito more tormentis exponeretur.</p>
		<p>Ardeo, mihi credite, Patres conscripti (id quod vosmet de me existimatis et facitis ipsi) incredibili quodam amore patriae, qui me amor et subvenire olim impendentibus periculis maximis cum dimicatione capitis, et rursum, cum omnia tela undique esse intenta in patriam viderem, subire coegit atque excipere unum pro universis. Hic me meus in rem publicam animus pristinus ac perennis cum C. Caesare reducit, reconciliat, restituit in gratiam.</p>
	</div>
</body>"></iframe>

## Position collante <!-- .slide: class="split-panel-50-50" -->

<div>

```html
<section id=welcome>
	<h1>Hello World!</h1>
</section>
<a href=# id=scroll-top>Retour à l'accueil</a>
```

```css
#welcome {
	height: 100vh;
}
#scroll-top {
	position: sticky;
	top: 90vh;
	left: 80vh;
}
```

</div>

<iframe srcdoc="<head>
	<style>
		#welcome {
			display: flex;
			flex-direction: column;
			justify-content: center;
			text-align: center;
			height: 100vh;
		}
		#scroll-top {
			background-color: slategrey;
			color: white;
			border-radius: 1.5em;
			padding: 0.5em;
			position: sticky;
			top: 90vh;
			left: 80vh;
		}
	</style>
</head>
<body>
		<section id=welcome>
			<h1>Hello World!</h1>
		</section>
		<a href=# id=scroll-top>Retour à l'accueil</a>
		<p>Duplexque isdem diebus acciderat malum, quod et Theophilum insontem atrox interceperat casus, et Serenianus dignus exsecratione cunctorum, innoxius, modo non reclamante publico vigore, discessit.</p>
		<p>Haec igitur Epicuri non probo, inquam. De cetero vellem equidem aut ipse doctrinis fuisset instructior est enim, quod tibi ita videri necesse est, non satis politus iis artibus, quas qui tenent, eruditi appellantur aut ne deterruisset alios a studiis. quamquam te quidem video minime esse deterritum.</p>
		<p>Orientis vero limes in longum protentus et rectum ab Euphratis fluminis ripis ad usque supercilia porrigitur Nili, laeva Saracenis conterminans gentibus, dextra pelagi fragoribus patens, quam plagam Nicator Seleucus occupatam auxit magnum in modum, cum post Alexandri Macedonis obitum successorio iure teneret regna Persidis, efficaciae inpetrabilis rex, ut indicat cognomentum.</p>
		<p>Horum adventum praedocti speculationibus fidis rectores militum tessera data sollemni armatos omnes celeri eduxere procursu et agiliter praeterito Calycadni fluminis ponte, cuius undarum magnitudo murorum adluit turres, in speciem locavere pugnandi. neque tamen exiluit quisquam nec permissus est congredi. formidabatur enim flagrans vesania manus et superior numero et ruitura sine respectu salutis in ferrum.</p>
		<p>Ob haec et huius modi multa, quae cernebantur in paucis, omnibus timeri sunt coepta. et ne tot malis dissimulatis paulatimque serpentibus acervi crescerent aerumnarum, nobilitatis decreto legati mittuntur: Praetextatus ex urbi praefecto et ex vicario Venustus et ex consulari Minervius oraturi, ne delictis supplicia sint grandiora, neve senator quisquam inusitato et inlicito more tormentis exponeretur.</p>
		<p>Ardeo, mihi credite, Patres conscripti (id quod vosmet de me existimatis et facitis ipsi) incredibili quodam amore patriae, qui me amor et subvenire olim impendentibus periculis maximis cum dimicatione capitis, et rursum, cum omnia tela undique esse intenta in patriam viderem, subire coegit atque excipere unum pro universis. Hic me meus in rem publicam animus pristinus ac perennis cum C. Caesare reducit, reconciliat, restituit in gratiam.</p>
</body>"></iframe>

## Ressources

- Le positionnement, Mozilla Developers Network, [https://developer.mozilla.org/fr/docs/Learn/CSS/CSS_layout/Positioning](https://developer.mozilla.org/fr/docs/Learn/CSS/CSS_layout/Positioning)