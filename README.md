# Sentiment Analysis

En este ejercicio se entrena un modelo de una RNN para el análisis de sentimientos, con el uso de un dataset de reviews de películas de IMDB.

## Dataset

El dataset viene incluido dentro de la librería de **tensorflow_datasets** y se puede cargar de la siguiente manera:

```python
import tensorflow_datasets as tfds
```

## Modelo

El modelo consiste en una RNN con una capa de embedding, dos capas de GRU y una capa densa con una neurona de salida.

## Entrenamiento

El modelo se entrena con un optimizador Adam y una función de pérdida de entropía cruzada binaria.

## Resultados

El modelo alcanzó una precisión de **97.79%** durante el último epoch de entrenamiento, con un loss de **0.0619**.

## Predicciones

Se realizaron predicciones en 3 diferentes ocaciónes con el modelo entrenado, con los siguientes resultados:

| Review | Sentimiento |
| --- | --- |
| This movie sucks | Bad |
| This movie is awesome | Good |
| I like the movie, but it was okay | Neutral |

Tomando en cuenta que el rango para que una review sea considerada como positiva es de **0.7 a 1.0**, para ser considerada como neutral es de **0.4 a 0.7** y para ser considerada como negativa es de **0.0 a 0.4**, se puede ver que el modelo predijo correctamente las 3 reviews.
