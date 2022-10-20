# Coppel Route Optimization

<!--more-->

## About

With the accelerated growth of e-commerce in recent years, it has become critical for 
companies to adapt to the new landscape. It is becoming increasingly common to order 
products online, and the companies must find the right logistics solutions to 
ensure that their products reach their customers. Efficiency and optimization are key to sucess, 
as companies seek to minimize distribution costs and delivery times while meeting customer 
expectations. These logistics strategies involve finding optimal routes, something that can be studied 
from problems such as the Traveling Salesman Problem and the Capacitated Vehicle Routing 
Problem (CVRP), which are applications of Linear Programming. This paper applies the above 
concepts, as well as Machine Learning algorithms, to solve a routing problem for the 
company Grupo Coppel, from one of its distribution centers in Azcapotzalco, Mexico City.


### Methodology

1. From the assigned database, the delivery locations for a specific day were selected. 
From these locations, the ones that were duplicated were removed. Then, to obtain the 
coordinates of each location, web scraping techniques were used; with 
the support of the *Selenium* library a bot was programmed in the Python programming language 
that searched for the addresses of each location in Google Maps, and saved 
the coordinates of each of those points in the database. To plot the coordinates on the map 
a WGS 84 projection was used, in order to adjust the position of the points on the 
corresponding map. This was done with the *Folium* library.

2. Once these data with the locations were obtained, only 300 were randomly selected, 
taking care that these data were properly scraped, in other words: correctly extracted. 
Some addresses were not properly located because some of the address names were incomplete, 
so they were not a real place or a real location. Therefore, manually, data that did not 
completely match their corresponding address were searched for.

3. Once these 300 random locations were obtained, they were plotted using the Python 
library "Folium", which plotted these points on an interactive map. This map shows the 
locations of each delivery point, the location of the Azcapotzalco CEDIS, and the 
municipalities to which this CEDIS delivers.

4. In order to obtain several delivery routes and not only 1 vehicle passing through 
all the points, it was decided to group these points by zones. For this, the K-means 
unsupervised Machine Learning algorithm was used to find these clusters. 

5. In order to use implement the Multiple Vehicle Routing Problem (MVRP), the cost of 
the trips between each point must be known, therefore, the API "OSMR" (Open Source 
Routing Machine) was used, which calculates the time that a vehicle would take 
between 2 given points. This makes it possible to obtain the variables
necessary to use the traveling agent algorithm.

6. Finally, the Python algorithm was used in order to trace the optimal route given by 
the CVRP.

Thus, in general, the solution to this problem took into account the 300 points to be 
visited, the delivery times for each item (the distances between each pair of points 
were also considered), the number of vehicles to meet the demand, and the capacity of 
these vehicles. 

