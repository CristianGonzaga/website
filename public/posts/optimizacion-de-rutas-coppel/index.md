# Optimización de Rutas de Coppel

<!--more-->

## Acerca de
Con el crecimiento acelerado del e-commerce en años recientes, se ha vuelto crítico 
para las empresas adaptarse al nuevo panorama. Cada vez es más común ordenar productos en 
línea, y las empresas en cuestión deben encontrar soluciones de logística adecuadas para 
procurar que sus productos lleguen a los clientes. Para lo anterior, la eficiencia 
y la  optimización son clave, dado que las empresas buscan minimizar costos de distribución 
y tiempos de entrega, y al mismo tiempo cumplir con las expectativas de los clientes. 
Estas estrategias de logística involucran encontrar rutas óptimas, algo que puede 
estudiarse a partir de problemas como el Problema del Agente Viajero y el Problema de 
Enrutamiento de Vehículos con Capacidades (MVRP), los cuales son aplicaciones de la Programación 
Lineal. El presente trabajo aplica los conceptos anteriores, así como algoritmos de 
Machine Learning, para resolver un problema de rutas a la empresa Grupo Coppel, desde 
uno de sus centros de distribución en Azcapotzalco, Ciudad de México.

### Metodología

1. A partir de la base de datos asignada, se seleccionaron las ubicaciones de entregas de un día 
específico. Con estas ubicaciones seleccionadas, se quitaron las ubicaciones
que estuvieran duplicadas. Posteriormente, para obtener las coordenadas de cada ubicacion, 
se usaron técnicas de web scraping para esta busqueda; con el apoyo de la 
librería de *Selenium* en el lenguaje de programación Python se programó un bot que 
buscaba las direcciones de cada ubicación en Google Maps, y guardaba las coordenadas 
de cada uno de esos puntos en la base de datos. Para graficar las coordenadas en el mapa 
se uso una proyección WGS 84, para así poder adecuar la posición de los puntos sobre el 
mapa correspondiente. Esto se hizo con la librería *Folium*.

2. Una vez obtenidos estos datos con las ubicaciones, se seleccionaron solo 300 de manera 
aleatoria, cuidando que estos datos hayan sido scrapeados de manera adecuada, dicho de otra forma: 
extraídos, correctamente. Algunas direcciones no fueron ubicadas adecuadamente debido a 
que algunos nombres de dichas direcciones estaban incompletos, por lo que no 
correspondían a un lugar real o a la ubicación correcta. Por lo tanto, manualmente, 
se buscaron los datos que no coincidieran por completo con su dirección correspondiente.

3. Una vez obtenidas estas 300 ubicaciones aleatorias, se graficaron usando la librería 
“Folium” de Python, misma que graficó estos puntos en un mapa interactivo. En dicho mapa se muestran 
las ubicaciones de cada punto de entrega, la ubicación del CEDIS de Azcapotzalco, y los 
municipios y alcaldías a los que hace entrega este CEDIS.

4. Con el fin de obtener varias rutas de entrega y que no solo 1 vehículo pase por todos 
los puntos, se decidió agrupar estos puntos por zonas. Para esto, se usó el algoritmo de 
Machine Learning no supervisado de agrupacion K-means para encontrar estas agrupaciones. 

5. Para poder usar el algoritmo de MVRP, se debe saber el costo de los viajes entre cada 
punto, por lo tanto, se usó la API “OSMR” (Open Source Routing Machine), que calcula el 
tiempo que haría un vehículo entre 2 puntos determinados. Esto permite obtener las variables
necesarias para usar posteriormente el algoritmo del agente viajero.

6. Finalmente, se utilizó el algoritmo en Python, con el fin de trazar la ruta optima 
dada por el CVRP.

De tal manera que, en general, para la solución de este problema, se tomaron en cuenta los 300 puntos a visitar, 
los tiempos de entrega de cada artículo (para llegar a esto también se 
consideraron las distancias entre cada par de puntos), el número de vehículos para cumplir 
con la demanda, y la capacidad de dichos vehículos. 

