# DeteccionDeAnomalias

El presente proyecto tiene por objetivo probar diferentes algoritmos de detección de anomalías en una base de datos perteneciente a Challenge Data 2020 el cual es un proyecto
de École Normale Superieur y Collège de France a partir de la base de datos propuesta por Kayrros en el challenge "Asset production estimation".

Los datos utilizada provienen del Data Challenge propuesto por Kayrros disponible en:

https://challengedata.ens.fr/participants/challenges/39/ 

El objetivo es estimar la producción semanal de 83 activos industriales a partir de mediciones diarias disponibles para cada activo.

Para ello se utilizaran algoritmos de detección de anomalías para series de tiempo a fin de establecer el valor de la producción diaria con la siguiente regla:

0, si hay anomalías excedentes en una o más mediciones.
Capacidad nominal diaria si no.


Se utilizan los datos contenidos en los archivos x_train y y_train, además del archivo assets con la capacidad de producción nominal por activo.

Los algoritmos probados fueron:

Alisamiento Exponencial (Holt-Winters+Brutlag)
Envolvente elíptica
Elastic
Azure

Para cada uno de estos se presentan dos notebooks el primero para la visualización de la detección de una da las series de tiempo, y el segundo donde se pasa por el algoritmo cada de las mediciones de cada activo para 






