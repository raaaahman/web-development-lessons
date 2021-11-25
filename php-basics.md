---
title: PHP et les sites web dynamiques
date: 2021-11-15
cover:
---

# PHP et les sites web dynamiques

Sylvain Schellenberger

## Mon expérience 

<div class="row r-stretch">

![WordPress](assets/images/wordpress.png)

![Polylang](assets/images/polylang-parrot-green.png)

</div>

- 2.5 ans Développeur pour Polylang

## Sites statiques

![Un site statique contient un document HTML par page à afficher.](assets/images/static-site.png)
<!-- .element: class="r-stretch" -->

HTML + CSS (+ Javascript)

## WordPress (site dynamique)

![L'éditeur peut ajouter une page au site, que le visiteur peut ensuite consulter.](assets/images/wordpress-site.png)
<!-- .element: class="r-stretch" -->

???

## A l'intérieur de WordPress

<div class="r-stack r-stretch">

![La requête HTTP(S) arrive à l'intérieur de WordPress.](assets/images/wordpress-inside-01.png)
<!-- .element: class="fragment current-visible" data-fragment-index="0" -->

![Apache Httpd intercepte la requête HTTP(S)](assets/images/wordpress-inside-03.1.png)
<!-- .element: class="fragment current-visible" data-fragment-index="1" -->

![Apache Httpd envoie les informations de la requête au code PHP de WordPress.](assets/images/wordpress-inside-05.1.png)
<!-- .element: class="fragment current-visible" data-fragment-index="2"  -->

![Le code MySQL / MariaDB va chercher les informations dans la base de données..](assets/images/wordpress-inside-06.1.png)
<!-- .element: class="fragment current-visible" data-fragment-index="3" -->

![](assets/images/wordpress-inside-07.1.png)
<!-- .element: class="fragment current-visible" data-fragment-index="4" -->

![](assets/images/wordpress-inside-08.1.png)
<!-- .element: class="fragment"  data-fragment-index="5" -->

</div>

## La "stack"

<div class="row r-stretch">

<div>

![](assets/images/windows.png)

![](assets/images/apple-logo.png)

![](assets/images/linux.png)

</div>

![](assets/images/apache-logo.png)

<div>

![](assets/images/mySQL.png)

![](assets/images/mariadb.png)

</div>

![](assets/images/php-logo.png)

</div>

(**W**indows / **M**acOS / **L**inux) + **A**pache + ( **M**ySQL / **M**ariaDB ) + **P**HP
 
## 

<div class="row">

![Journal Apache Httpd](assets/images/apache-logs.png)<!-- .element: style="max-width: 100%; max-height: 100%" -->

![Edition de code PHP](assets/images/php-file.png)<!-- .element: style="max-width: 100%; max-height: 100%" -->

![Lignes de code MySQL](assets/images/sql-file.png)<!-- .element: style="max-width: 100%; max-height: 100%" -->

![PHPMyAdmin: interface pour base de données MySQL](assets/images/mysql-db.png)<!-- .element: style="max-width: 100%; max-height: 100%" -->
 
</div>
