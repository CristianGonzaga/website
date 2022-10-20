---
weight: 1
title: "Optimización de Procesos. FEMSA Coca-Cola"
date: 2021-10-22T15:18:23-05:00
lastmod: 2022-10-04T15:18:23-05:00
draft: false

author: "Cristian Gonzaga"
description: "Se analizaron los datos de Femsa-Coca Cola de la producción en la planta de Altamira del
6/07/2021 al 30/07/21. Los datos fueron entregados por KOF en formato .csv (la primera versión) y en formato
Excel (la segunda versión creada, con los datos transpuestos y sin datos faltantes). 
El objetivo del análisis fue desarollar un modelo que explique la relación entre la energía 
necesaria para la cadena de producción y diferentes variables con la finalidad de 
minimizar el uso de energía."

tags: ["FEMSA Coca-Cola","Ciencia de Datos","R"]
categories: ["Proyectos Co-Curriculares"]

lightgallery: true

toc:
 auto: false
---
<!--more-->

## Acerca de
Se analizaron los datos de Femsa-Coca Cola de la producción en la planta de Altamira del
6/07/2021 al 30/07/21. Los datos fueron entregados por KOF en formato .csv (la primera versión) y en formato
Excel (la segunda versión creada, con los datos transpuestos y sin datos faltantes). 
El objetivo del análisis fue desarollar un modelo que explique la relación entre la energía 
necesaria para la cadena de producción y diferentes variables con la finalidad de 
minimizar el uso de energía.

El trabajo fue dividido en tres fases. En primera instancia, se hizo un análisis exploratorio
en virtud de familiarizarse con los datos, aprendiendo la estructura de la base de datos y 
empezando a conocer las variables. Dicho análisis se decidió hacer en un shiny dashboard en 
R, de tal forma que la información pueda ser accedida por la aplicación web generada 
por el código. 

Luego, se hizo un análisis de las variables de energía y potencia por SKU. Haciendo una prueba de hipótesis
de 2 colas para identificar si se producen más botellas para cierta SKU en cada compresor.

Por último, se hizo un algoritmo de Random Forest para predecir la potencia eléctrica de 
cada compresor en cada línea y con las líneas juntas. Además, se calculó la importancia de 
cada variable (en su uso para este algoritmo). Obteniendo así un algoritmo de Random Forest 
con 100 árboles que puede describir en gran medida la potencia eléctrica de los compresores


