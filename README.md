# Visualización de datos - PEC 2

Alumno: `Darío Fervenza García`

# Cartograma

El cartograma es un mapa temático en el que una variable, por ejemplo, la tasa de mortalidad, es representada en diferentes regiones mediante el uso de colores.

## Origen

La primera vez que se ha usado este término fue en el siglo XIX, por el ingeniero Francés `Charles Minard`. Se han empleado en diferentes contextos, por ejemplo en el ámbito de la política en el Washington Post en 1929. Además, se crearon por primera vez con la ayuda de una computadora en la década de 1960, siendo `Waldo Tobler` la primera persona en dar este paso.

## Ejemplos de aplicación

- Representación de la **población** en diferentes paises del mundo
- Visualizaciones del **avance de una enfermedad** a través de diferentes áreas
- Representación de la **calidad del aire** en diferentes barrios de una ciudad

Existen cartogramas **contiguos**, donde las regiones mantienen la conexión geográfica, y **no contiguos**, donde las áreas pueden estar separadas, pero distorsionadas en función de los datos.

## Tipos de datos empleados

El cartograma suele representar una **variable cuantitativa** continua, aunque también se puede adaptar para el caso discreto. Esta variable debe ir acompañada de otra que asocie cada dato numérico a una región del mapa. Por tanto, se necesita una variable númerica y una **variable geográfica** (por ejemplo España - 16.9).
Además, es necesario traducir la variable geográfica a las coordenadas que delimitan la ubicación de la zona geográfica a representar en el mapa.

## Limitaciones

La principal limitación es que no se puede saber el valor exacto que se está representando, aunque si las regiones a representar son lo suficientemente grandes, se pueden añadir etiquetas númericas.

En cuanto a datos, no existe un límite como tal, se podría representar desde menos infinito hasta más infinito. Sin embargo, esto no resulta posible en la práctica porque el hecho de representar datos muy dispares puede dificultar la asimilación de la información por parte del usuario. Por tanto, se debe limitar el rango a representar, sobretodo si la cantidad de regiones con valores diferentes es grande. En casos en los que sea totalmente necesario representar un gran rango de datos, se debe aplicar una discretización más amplia, lo cual conlleva pérdida de información y puede hacer dificil realizar comparaciones.

## Resultado

![Imagen cartograma](https://github.com/dariofervenza/M2.859_PC2/blob/main/images/mapa_eeuu_bueno.png?raw=true)

### Objetivo y resultados de la técnica

El objetivo es hacer una rápida comparativa entre diferentes regiones de modo que se pueda apreciar que regiones tienen mejores salarios. La técnica ayuda a esto porque permite comprobar de un vistazo que estados tienen un income superior sin tener que pararse a ver el detalle de los datos en cada región.

# Gauge diagram

Este diagrama consiste en una representación circular de una variable en el que se pueden añadir marcas o colores para delimitar valores comunes o críticos. 

## Origen

Surge en la `industria del automovil` a finales del siglo XIX, cuando se comienza a incorporar para medir velocidad, temperatura y cantidad de combustible. Su éxito y popularidad ha hecho que se extienda a otras áreas como la industria o los negocios.

El término "gauge" hace referencia a la palabra del antiguo inglés "gaugen" la cual significa medida.

## Ejemplos de aplicación

- Manómetros
- **KPI's** en cuadros de mando
- Mediciones de la **velocidad de internet**

## Tipos de datos empleados

Estas representaciones requieren una **variable numérica continua** que se representa dentro de un `rango de valores` y que puede incluir o marcas de valores clave. Por ejemplo, en un medidor de presión o caudal, se suele indicar la zona segura de trabajo (por ejemplo, en **verde** o sin color) y la zona en la que el valor comienza a ser peligroso (habitualmente en **rojo**).

## Limitaciones

La principal limitación es la gran cantidad de espacio que necesita para representar un único valor. Por tanto cuando se desean observar varios indicadores puede no ser la mejor opción. Además, en ocasiones es complicado saber el valor exacto que se está representando, por lo cual puede ser necesario añadir anotaciones. Es importante que el **rango** del gauge se elija cuidadosamente para evitar representaciones confusas, especialmente si el rango de valores es amplio.


## Resultado


![Imagen gauge](https://github.com/dariofervenza/M2.859_PC2/blob/main/images/gauge_chart.png?raw=true)

![Imagen gauge porcentual](https://github.com/dariofervenza/M2.859_PC2/blob/main/images/gauge_chart_2.png?raw=true)

### Objetivo y resultados de la técnica

El objetivo es representar una variable dentro de un rango aceptable. De tal modo, se puede comprobar si el valor actual se encuentra en una zona segura o aceptable o bien si se trata de una anomalía. En el primer caso se ha representado el valor absoluto por lo que es necesaria información adicional para establecer los valores máximo y mínimo que acepta el diagrama. Mientras que en el segundo caso se ha representado un valor porcentual, lo cual establece intrínsicamente los límites de representación. Aunque es necesaria información para establecer una marca en el valor mínimo esperado, por ejemplo, se requiere que haya un mínimo de un 50% de inspecciones favorables.

La técnica permite obtener una representación muy visual en la que se puede comprobar facilmente si nuestro proceso se encuentra en los valores que nos interesan y es muy util para visualizar indicadores clave.

# Contour plot

El **contour plot** permite visualizar tres variables numéricas en dos dimensiones mediante el uso de una proyección de la tercera variable sobre el espacio de las dos primeras. Se emplean diferentes líneas, cada una de las cuales representa una zona en la que el valor de la tercera variable es constante.

## Origen

Estas representaciones han sido utilizadas históricamente para representar zonas a igual nivel en un mapa geográfico pero su uso a nivel matemático surge en el experimento Schiehallion, hecho por el matemático `Charles Hutton`.

## Ejemplos de aplicación

- Estudio del efecto de la **profundidad** en la biomasa del océano
- **Mapas isobáricos** para la predicción del tiempo metereológico
- **Estudio de la temperatura en un reactor** según los valores de la presión y profundidad del líquido.

## Tipos de datos empleados

Requiere tres **variables numéricas continuas** (X, Y y Z), entre las cuales una es la variable dependiente (Z) y otras dos son variables independientes. Por tanto, el valor de Z dependerá de los valores de las otras dos variables.

## Limitaciones

La principal limitación se produce cuando el valor de Z varía mucho con pequeños cambios en X o en Y y por tanto es necesario incrementar el número de líneas. Esto puede **dificultar la interpetación** del gráfico y reducir su eficacia.

## Resultado

![Imagen contour](https://github.com/dariofervenza/M2.859_PC2/blob/main/images/contour_plot.png?raw=true)


### Objetivo y resultados de la técnica

El objetivo es conocer la distribución de la variable Z en diferentes combinaciones de la variables X e Y. Se hace especial énfasis en las zonas de valor constante de Z. 
Los resultados en el caso del contour plot de una función de coste son la representación del movimiento de las variables  ajustables al aplicar el algoritmo de Gradient Descent. Esto permite visualizar los posibles mínimos locales que presente el sistema y ayuda a investigar nuevas técnicas de aprendizaje automático como pueden ser diferentes métodos de inicialización de las variables.

# Referencias

- https://think.design/services/data-visualization-data-design/cartogram/
- https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html
- https://worldpopulationreview.com/state-rankings/median-household-income-by-state
- https://python-graph-gallery.com/choropleth-map-geopandas-python/
- https://saberpunto.com/tecnologia/cartograma-ejemplos/
- https://datos.gob.es/en/catalogo/a10002983-datos-del-numero-de-inspecciones-de-itv-2021
- https://clusterdesign.io/gauge-charts-best-practices-and-examples/
- https://www.jaspersoft.com/articles/what-is-a-gauge-chart#:~:text=Space%20Limitations,an%20effective%20overview%20of%20performance.
- https://mapreading.co.uk/history-of-contour-lines/
- https://victordonnay.digital.brynmawr.edu/fall-2021-poster-gallery/the-history-of-the-contour-plot/
- https://statisticsbyjim.com/graphs/contour-plots/
- https://medium.com/analytics-vidhya/visualize-the-gradient-descent-of-a-cost-function-with-its-level-circles-python-d8c850731b0a

