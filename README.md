# Deteccion De Anomalias en Series de Tiempo 

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

Para cada loa algoritmos 1,2 y 4 se presentan dos notebooks:
- el primero para la visualización de la detección de una de las series de tiempo, y 
- el donde se pasan por el algoritmo todas las series de teimpo y se calcula la producción.

Para el algoritmo de Elastic, el proceso fue distinto ya que la ingesta de datos se realizó utilizando Kibana, mientras que los resultados fueron exportados utilizando la interfaz de cliente para Python.  



