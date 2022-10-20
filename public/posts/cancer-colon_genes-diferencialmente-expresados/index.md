# Análisis de Genes Diferencialmente Expresados en el Cáncer de Colón

<!--more-->

## Acerca de
Este proyecto identificó los genes involucrados en la formación 
de tejidos cancerosos, centrándose en los genes diferencialmente expresados en cáncer de 
colon en adultos de 50 a 60 años, aprovechando la inmensa cantidad de información encontrada 
en distintas bases de datos respecto al tema y del lenguaje de programación R.

El código del dataset analizado GSE44076 fue recuperado de la base de datos Geo DataSets, 
el cual refiere a diferentes tipos de mucosa en el colon, en los cuales algunos se 
detectaron células de adenocarcinomas y tumores. De dichos datos se hizo una 
clasificación de sujetos con mucosas de colon sanas y con tumores cancerígenos en el 
colon de 50 a 60 años (adultos) y de 70 a 85 años (personas de la tercera edad). 

En el caso de la búsqueda de genes diferencialmente expresados, se hicieron distintas consideraciones 
(edad, sexo, nacionalidad, entre otros) para la formación de los grupos. Además, se determinó la cantidad 
de muestras a emplear para cada grupo, la cantidad de genes a analizar, 
la magnitud de cambio (cambio de logaritmo base) y la significación estadística (valor de 
p-value) para calcular su influencia significativa en los resultados. 

Tras el procesamiento estadístico en R Studio, utilizando los paquetes de limma y GEOquery, 
aunado al algoritmo implementado para encontrar los p-values y tamaños de efecto más 
significativos, se obtuvieron 10 genes diferencialmente expresados de la clasificación 
de la razón entre adultos saludables y en un estado patológico, que son: CRNDE, MMP7, 
MEPB1B, CA7, entre otros.

Una vez se obtuvieron los genes, se utilizaron distintos recursos bioinformáticos para 
darle un sentido a los genes. Dicha etapa permitió validar la información, aunado a dar 
un sustento, de tal manera que se identificaron las funciones que tienen los respectivos 
genes, su relación a procesos biológicos, su identidad, el tipo de moléculas que son, 
entre otros. Así, se consiguió un mejor análisis y entendimiento del impacto de los 
genes.
 
Por último, una vez comprobado que los genes seleccionados tienen una estrecha relación 
con el objeto de estudio, es propio considerar como determinantes a dichos genes 
en los procesos patológicos, en virtud de lo cual se pueden idear soluciones 
y estrategias a partir de estos. Así, al identificar un gen que se presenta en 
específico en las personas adultas en un determinado rango de edad con cáncer de colon, 
se puede comprender su amenaza (hasta cierto punto), o bien, atenderlo si se presta a ello. 
Aunado a que se pueden desarrollar distintas alternativas a la colonoscopia, 
como la implementación de micro chip de bajo costo encargados de analizar los 
biomarcadores causantes del cáncer de colon.


