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

Finalmente, vamos a ver los diferentes indicadores utilizados para este tercer estudio. El primero de todos que se ha realizado es realizar un pequeño estudio sobre los datos para ver que es lo que podemos sacar de ellos, ya que a primera vista podemos ver algunas variables que parece que nos van a dar poca información. Para ello hemos hecho el sumatorio de los registros diferentes que hay en cada una de las variables. Con esto hemos concluido que solo nos interesará tratar con las variables *geo*, *TIME_PERIOD*, y *OBS_FLAG*.

Vamos a empezar a trabajar con la variable *geo* que se refiere a la zona. Primero de todo vamos a obtener los registros únicos que tenemos y realizar una agrupación de esta para obtener información sobre el *OBS_VALUE*. La primera métrica que sacamos es el sumatorio de los *OBS_VALUE* para cada zona. Al final hemos visto que esta métrica no nos da mucha información sobre esta. Por esto hemos decidido sacar la media por zona.

Una vez se ha sacado la media, se ha realizado una ordenación ascendente y obtenemos la zona con un valor mayor y menor. La que tiene un valor menor es 'IE' y con un valor mayor 'FR'.

Ahora vamos a ver que tal el valor de la zona de España, abreviada como 'ES'. Con esto obtendemos la media del *OBS_VALUE* y vemos que tiene un valor de 44'8, un valor que se encuentra en medio entre la zona con mayor valor y con menor.

A continuación vamos a empezar a trabajar con los años, *TIME_PERIOD*. Vamos a ver si hay algún tipo de relación entre el *TIME_PERIOD* y el *OBS_VALUE*. Primero de todo se ha ordenado por *OBS_VALUE* y se ha llegado a la conclusión que el valor menor es de 2019 y el mayor de 2013.

Después se ha agrupado por año para ver cuales de los años han tenido una mayor repercusión en cuanto al valor del *OBS_VALUE*. Aquí se han calculado dos métricas sobre esta agrupación, la media y la desviación típica. LLegando a la conclusión que el mejor año en términos de *OBS_VALUE* es el 2021 con un valor de 51'13 de media y el peor el 2017 con una media de 43'35. El año con la desviación típica mayor es 2013.
