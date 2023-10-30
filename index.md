---
title: "Sintaxis Básica Markdown"
author: "Renzo Cáceres Rossi"
date: "30/10/23"
output:
  html_document:
    toc: TRUE
    toc_float: TRUE
abstract: El presente documento muestra el uso del lenguaje de marcado ligero Markdown
  para la creación de documentos reproducibles en formatos HTML,PDF y Microsoft Word;
  enfocandonos en su sintaxis básica, principales atributos y funcionalidades, haciendo
  uso del entorno de desarrollo RStudio.
subtitle: "Markdown - RMarkdown"
lang: "es-ES"
---

<a name="arriba"></a>

<a href="#abajo">Ir Abajo</a>

\pagebreak
<!-- Crear documentos reproducibles utilizando Markdown y etiquetas HTML -->


## Sintaxis Markdown

**Markdown** es un lenguaje de marcado ligero (***Lightweight Markpup Language***),siendo **RMarkdown**[^pie_pagina_01], uno de sus dialectos, una de sus variantes, uno de sus sabores (**Markdown Flavours**).

```

## Encabezados - Títulos

# Título 1
## Título 2
### Título 3
#### Título 4
##### Título 5
###### Título 6

Título 1
=========

Título 2
---------

```

## Separaciones - Líneas Horizontales

---

---

***

***

## Citas - Añadir citas a nuestro documento Markdown

> "La gente que está lo suficientemente loca para pensar que que pueden cambiar el mundo es la gente que lo consigue"
>
> **Steve Jobs**

## Formateo de texto - Negrita - Cursiva - Tachado - Subrayado

**Texto formateado como Negrita**

*Texto formateado como Cursiva*

***Texto formateado como Negrita y Cursiva***

~~Texto tachado~~

<u>Texto subrayado</u> <!-- HTML tags -->

## Listas

### Lista Viñetas - Lista Anidada

- Lista 1
- Lista 2
- Lista 3
- Lista 4
- Lista 5
  - Lista 5.1
  - Lista 5.2
  - Lista 5.3
- Lista 6
- Lista 7
- Lista 8

### Lista Numerada

1. Lista 1
2. Lista 2
3. Lista 3
4. Lista 4
5. Lista 5
6. Lista 6
7. Lista 7

### Lista Ordenada Alfabéticamente

a. Lista A
b. Lista B
c. Lista C
d. Lista D
e. Lista E
f. Lista F

### Casos - Ejemplos

- Lista 1
- Lista 2
- Lista 3
+ Lista 4
+ Lista 5
+ Lista 6
* Lista 7
* Lista 8
* Lista 9

---

1. Lista 1
3. Lista 2
5. Lista 3
7. Lista 4
9. Lista 5
11. Lista 6

<!--
## Tablas - Añadir tablas a nuestro documento Markdown


|TABLA A|TABLA B|TABLA C|
|:-----:|:-----:|:-----:|
|A      |B      |C      |
|A      |B      |C      |
|A      |B      |C      |
|A      |B      |C      |
|A      |B      |C      |
|A      |B      |C      |
|A      |B      |C      |

-->


## Enlaces - Añadir links a nuestro documento Markdown

<https://www.youtube.com/>

[YouTube](https://www.youtube.com/ "Ingresar a YouTUbe")


[YouTube Channels](https://www.youtube.com/){target=_blank}


## Imágenes - Añadir imágenes a nuestro documento Markdown

<center>

![](diagrama_barras_amano.jpg){width=400 height=300}

</center>

<center>


![](https://d33wubrfki0l68.cloudfront.net/aee91187a9c6811a802ddc524c3271302893a149/a7003/images/bandthree2.png){width=400 height=350}

</center>



## Vídeos - Añadir vídeo MP4 y YouTube a nuestro documento Markdown

<center>

<iframe width="560" height="315" src="https://www.youtube.com/embed/KJExTrNIjuw?si=faXsiM698rPX8oVR" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen data-external=1></iframe>

</center>

<br>

<!--
<center>

<video width=640 height=340 controls>

<source src="killbill_trainning.mp4" type="video/mp4">

</video>

</center>

-->

## Mapas - Añadir mapas a nuestro documento Markdown

<center>


<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3902.27539107557!2d-76.95205512570942!3d-12.024552241485992!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9105c43b2da7b2f7%3A0xfe48f9b1a4a409bd!2sEl%20Parque%20de%20las%20Aguas%2C%20Ate%2015011!5e0!3m2!1ses-419!2spe!4v1698694447861!5m2!1ses-419!2spe" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade" data-external=1></iframe>

</center>

## Código - Añadir código de distintos lenguajes de programación (R-Python-SQL)

    summary(mtcars)
    
La función base `barplot()` nos permite crear diagramas de barras (**Bar Charts**) en el lenguaje de programación R

~~~
x <- table(mtcars$cyl)

colores <- c("orange","blue","purple")

barplot(x,xlab="Cilindros",ylab="Frecuencias",main="Número de Cilindros",col=colores)
~~~

```R
x <- table(mtcars$cyl)

colores <- c("orange","blue","purple")

barplot(x,xlab="Cilindros",ylab="Frecuencias",main="Número de Cilindros",col=colores)
```

```Python
import matplotlib.pyplot as plt
 

eje_x = ['Python', 'R', 'Node.js', 'PHP']
 

eje_y = [50,20,35,47]
 

plt.bar(eje_x, eje_y)
 

plt.ylabel('Cantidad de usuarios')
 

plt.xlabel('Lenguajes de programación')
 

plt.title('Usuarios de lenguajes de programación')
 

plt.show()
```

```SQL

USE Northwind;

SELECT * FROM Products;

```

## Anular sintaxis Markdown


\ # Esto debería ser un título tipo 1

\**Esto debería ser texto formateado como Negrita**

\*Esto debería ser texto formateado como Cursiva*

## Pie de página

[^pie_pagina_01]: **RMarkdown es un paquete (package) del lenguaje de programación R que nos permite crear documentos reproducibles en formato HTML,PDF,Microsoft Word entre otros.**

## Correo electrónico

Si tienes alguna duda o pregunta, no dudes en contactarme:

email: <a href="mailto:arenzocaceresrossi@gmail.com">arenzocaceresrossi@gmail.com</a>

---

&copy; Renzo Cáceres Rossi



<div class="tocify-extend-page" data-unique="tocify-extend-page" style="height: 0;"></div>

<a name="abajo"></a>

<a href="#arriba">Ir Arriba</a>
