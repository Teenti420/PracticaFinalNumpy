# PracticaFinalNumpy

Alumno: Sebastià Vicens Oliver

En esta práctica se ha estado trabajando sobre tres datasets distintos. Estos datasets debían ser tratados en python para intentar sacar varias conclusiones sobre los datos. Más en concreto se debía utilizar la librería Numpy para realizar el estudio.

A continuación vamos a comentar los indicadores que se han sacado y los resultados obtenidos, así como las conclusiones que podemos sacar de estos.

## A) Tabla de INEbase Balears
### Illes por municipios y fenómeno demográfico . MNP Estadística de Defunciones

En este primer caso, las métricas que se han intentado obtener son, primero de todo, las series de los *nacidos vivos por residencia materna*. En este caso, no hay mucho que explicar. En este caso hemos obtenido los registros *nacidos vivos por residencia materna* y hemos hecho el sumatorio de las muertes de cada municipio. De esta forma hemos obtenido un total de 9455 muertes. Después de eso se ha calculado la media de muertes de este tipo por municipio y esta ha sido de 141'12.

A continuación, se ha trabajado con las series de los *fallecidos por el lugar de residencia*. Una vez filtrados los datos se han obtenido las mismas métricas que en el anterior caso, añadiendo además la desviación estándard. En este caso, la suma total asciende a 8559 y la media 127'75. Por tanto, vemos que en este caso ha disminuïdo un poco la cantidad de muertes en las Islas debido a este fenómeno.

Con las series anteriores hemos seguido trabajando. Primero de todo, hemos realizado una ordenación ascendente, de la cual hemos podido obtener su ordenación descendente. Así, con el head hemos podido obtener los municipios con mayor y menor tasa de mortalidad según este fenómeno demográfico.

Para terminar, hemos obtenido la media y la desviación típica de los cinco indicadores por municipio. Para ello hemos realizado la agrupación de los datos por fenómeno demográfico y, después, se han realizado las métricas. Si observamos un poco, vemos que los nacidos vivos por residencia materna son los que tienen una tasa de mortalidad más elevada, mientras que las muertes fetales por residencia materna lo que menor tasa tienen. En cuanto a la desviación estándard, el premio a la mayor y menor se lo llevan los mismos fenómenos demográficos.

## B) Speculation Watch List

Para el dataset de **Speculation Watch List** teníamos bastantes métricas a mirar, ya que hay una cantidad bastante numerosa de variables. Es necesario comentar que he tenido que modificar el archivo data/Speculation_Watch_List.csv debido a que habia una columna de tipo string que tenía algunos registros de tipo string con comas. Por ejemplo, "ESTE ES UN, EJEMPLO". En estos casos, al leer el separador con las comas se perdia información. Por eso he modificado estas comas que se encontraban dentro de los strings a ';'. 

Primero de todo lo que se ha hecho ha sido leer la columna de precios, realizando el ordenamiento ascendente de dichos datos. Así hemos llegado a la conclusión que el precio menor es de 500000 y el mayor de 90000000.

Una vez tenemos esta métrica estudiada, vamos a compararla junto con otras variables. En concreto con la zona. La zona la obtendremos con las columnas del df borough y boro. Hemos querido observar las diferencias entre los precios. Para ello se ha obtenido un array con el *borough*, el *boro* y el *precio*. Después se han realizado agrupaciones por *borough* y se han aplicado varias métricas. Entre ellas esta a mediana y, además las zonas con una mediana más alta y con la más baja.

Ahora vamos a mirar si vemos algún patrón que pueda indicarnos que diferencias encontramos entre la zona con los precios mayores y menores. Para ello vamos a trabajar con las columnas que nos indican el ratio de capitalización. Estas son **cap_rate** y **borough_cap_rate**. En concreto hemos filtrado por zona de mayor precio y de menor. Y después, se han aplicado las métricas de media y mediana. Esto para la zona con el precio mayor y menor. Con esta métrica hemos llegado a la conclusión que  el cap_rate como el borough_cap_rate es mayor en la zona más barata.

Finalmente, hemos calculado la diferencia de puntos porcentuales de la métrica anterior entre la zona con mayor precio y menor. Hemos obtenido una diferencia de 1'7 puntos porcentuales en ambas variables, a favor de la zona con menor precio.

## C) Gov 10a exp page linear
