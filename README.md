# Detección De Anomalias en Series de Tiempo 

El presente proyecto tiene por objetivo probar diferentes algoritmos de detección de anomalías en una base de datos perteneciente a Challenge Data 2020 el cual es un proyecto
de École Normale Superieur y Collège de France a partir de la base de datos propuesta por Kayrros en el challenge "Asset production estimation".

Los datos están disponible en:

https://challengedata.ens.fr/participants/challenges/39/ 

El objetivo es estimar la producción semanal de 83 activos industriales a partir de mediciones diarias disponibles para cada activo.

Para ello se utilizaran algoritmos de detección de anomalías para series de tiempo a fin de establecer el valor de la producción diaria con la siguiente regla:

-  Asignar 0, si hay anomalías excedentes en una o más mediciones.
-  Asignar la capacidad nominal diaria en caso contrario


Se utilizan los datos contenidos en los archivos x_train y y_train, además del archivo assets con la capacidad de producción nominal por activo.

Los algoritmos probados fueron:

1. Alisamiento Exponencial (Holt-Winters+Brutlag)
2. Envolvente elíptica
3. Elastic
4. Azure

En este repositorio se presentan, para cada uno de los algoritmos, al menos dos  notebooks. Para Holt-Winters+Brutalg, Envolvente Elíptica y Azure, el codigo de los archivos enumerados como 1.1, 1.2 y 1.4, permite la visualización de la detección de anomalías para una serie de tiempo. 
De modo distinto, el código para implementar la detección de anomalías con Elastic, se presenta dividido en los archivos 1.3.1 y 1.3.2 ya que la ingestá de datos se realizó directamente en Kibana, y posteriormente se exportaron los resultados utilizando la interfaz de cliente para Python.

En los archivos 2.1, 2.2 y 2.4 se presenta la implementación de la detección de anomalías para todas las series de tiempo, la estimación de la producción diaria, por gurpo de activos y el cálculo del error entre la predicción de producción hecha y el dato de producción proporcionado en el archivo y_train.


