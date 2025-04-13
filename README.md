# Análisis de Desempeño y Decisión de Cierre de Tiendas

Este repositorio contiene un análisis de desempeño de cuatro tiendas (Tienda_1, Tienda_2, Tienda_3 y Tienda_4) a partir de datos de ventas, calificaciones de clientes y costos logísticos (envío). El objetivo principal es determinar, mediante un enfoque multicriterio, cuál tienda debería cerrarse en función de su bajo desempeño general.

##Contenido
Datos:
Los datos utilizados se encuentran en cuatro archivos CSV:

tienda_1.csv

tienda_2.csv

tienda_3.csv

tienda_4.csv

(Se incluyen en este repositorio o se pueden descargar desde GitHub)

## Métricas Evaluadas:

Ventas Totales: Suma de los precios de productos vendidos.

Calificación Promedio: Satisfacción de los clientes.

% de Calificaciones Malas: Porcentaje de calificaciones de 1 y 2 estrellas.

Costo de Envío Promedio: Promedio del costo de envío en cada tienda.

## Metodología:
Se aplicaron los siguientes pasos en el análisis:

Carga y procesamiento de los archivos CSV (usando Pandas).

Cálculo de indicadores individuales para cada tienda:

Total de ventas.

Calificación promedio.

Distribución de calificaciones, enfocándose en el porcentaje de calificaciones malas.

Costo de envío promedio.

## Normalización de variables:
Para comparar indicadores con unidades distintas, se utilizó MinMaxScaler de scikit-learn. Las métricas donde un valor alto es malo (% de calificaciones malas y costo de envío) se invirtieron.

Cálculo de un puntaje compuesto que es el promedio de las métricas normalizadas.

Ranking de tiendas: La tienda con el menor puntaje compuesto es recomendada para cerrar.

## Ejecución
Descarga o clona este repositorio.

Asegúrate de tener en la raíz del proyecto los archivos CSV de las tiendas.

Ejecuta el script principal (por ejemplo, en un Jupyter Notebook o un script Python):

python analysis.py
Donde analysis.py contiene el siguiente código (resumen):


# Resultados y Conclusión
El análisis indicó que la tienda con el puntaje total más bajo es la Tienda_1, por lo que se recomienda su cierre. Esta conclusión se basa en la comparación de:

Ventas Totales: Tienda con altos ingresos, no justifica lo que viene a continuación.

Calificación Promedio: Bajo nivel de satisfacción de clientes.

% de Calificaciones Malas: Mayor porcentaje de clientes insatisfechos.

Costo de Envío Promedio: Costos logísticos relativamente altos.
