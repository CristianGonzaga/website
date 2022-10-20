# Los factores meteorológicos y la concentración de los contaminantes en la atmósfera

<!--more-->

## Acerca de
El proyecto encontró la relación entre los factores meteorológicos y la contaminación. Los datos 
utilizados fueron proporcionados por el Sistema de Monitoreo Atmosférico de la Zona Metropolitana 
de la Ciudad de México. A partir de ellos, se eligió el software R para realizar una limpieza y 
ordenamiento de los mismos y posteriormente generar una regresión lineal y múltiple.

Es importante mencionar que R es un lenguaje de programación especializado en el análisis estadístico. 
Se menciona lo anterior porque R proporcionó una gran variedad de herramientas útiles para el 
respectivo tratamiento y análisis de los datos. Para lo anterior, se usaron librerías especializadas 
en el manejo y graficación de datos como: *tidyverse*, *dplyr*, *gapminder* y *GGally*. Adicionalmente, 
se generó una aplicación web local en la que el usuario puede elegir tanto la estación de estudio 
como el periodo de tiempo que se quiere visualizar, esto al emplear las librerías *shiny* y 
*shinydashboard*. Además, por medio de la aplicación, R presenta tanto las gráfica de regresión lineal 
y múltiple junto con la información estadística dependiendo de la configuración que el usuario 
desee ingresar. De tal manera que resulta útil para los usuarios, siendo una manera eficiente para
analizar los resultados bajo diferentes circunstancia. 

Desarrollando así un modelo matemático que estima la concentración de partículas de
dióxido de azufre con base en la presión atmosférica (mmHG), la temperatura
(grados Celsius), humedad relativa (porcentaje), dirección del viento (grados) y
velocidad del viento (metros por segundo).


