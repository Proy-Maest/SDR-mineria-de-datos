# Autores:
- Carlos Andrés Cuartas Murillo - cacuartasm@eafit.edu.co
- Santiago Mejía Chitiva - smejiac3@eafit.edu.co
- Daniel Enrique Pinto Restrepo - dpintor1@eafit.edu.co
- Daniel Román Ramírez - dromanr@eafit.edu.co

**Mineria de datos**

**Universidad EAFIT - Medellín**

# SISTEMA DE RECOMENDACIÓN PARA EL SECTOR COMERCIAL ARTÍCULOS DE BELLEZA

# Objetivo General

- Desarrollar un sistema de recomendación escalable y eficiente en Big Data que permita la promoción de productos de belleza.


# MODELOS APLICADOS

- Baseline.
- Singular Value Decomposition (SVD).
- Alternating Least Square (ALS) escalado en Spark.
- Alternating Least Square (ALS) escalado en Spark versión mejorada

# Resultados obtenidos de los modelos aplicados

A continuación se exponen los resultados finales de los modelos aplicados para el sistema de recomendación

### Modelos escalados en Spark

- ALSE 3: Con un parámetro diferente y normalizando los ratings con la media, obtuvo un RMSE de 
**0.99** con un tiempo de ejecución de 230 segundos.

- ALS 2: Con un solo parámetro y normalizando los ratings con la media, obtuvo un RMSE de **0.95** con un tiempo de ejecución de 230 segundos.

- ALS 1: Con un solo parámetro y sin normalizar los ratings, obtuvo un RMSE de **1.11** con un tiempo de ejecución de 230 segundos.

- SVD, obtuvo un RMSE de **1.516** con un tiempo de ejecución de 230 segundos.

### Modelos realizado en Python
- Baseline, obtuvo un RMSE de **1.115** con un tiempo de ejecución de 60 segundos.
- KNN con Small data,se filtró la base de datos por usuarios e ítems más frecuentes, obtuvo un RMSE de **1.36** con un tiempo de ejecución de 9 segundos. 

# Métrica de evaluación de modelos

- RMSE: root-mean-square error

# Cloud Services BIG DATA

- AWS - S3- EMR

#  SOURCE DATA

- https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Beauty_v1_00.tsv.gz

# Conclusiones

- Para crear un buen sistema de recomendación el tratamiento de datos es fundamental para obtener una buena estimación.

- El impacto en la exactitud del modelo aumentó significativamente al normalizar las puntuaciones de representadas con ceros y las puntuaciones de los usuarios.

- Con base en los resultados obtenidos en el RMSE, la mejor metodología obtenida para desarrollar el sistema de recomendación es el modelo de ALS desarrollado en Spark.

- Se utiliza un solo parámetro como un primer acercamiento de experimentación y luego se intenta realizar diferentes iteraciones con diferente parámetro logrando finalmente mejorar el RMSE a 0.98, concluyendo así que los parámetros son significativos al ejecutar el modelo