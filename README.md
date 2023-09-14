# Equipo2_AI_Titanic

# Resumen de Logros

A lo largo de este proyecto, logramos construir y optimizar un modelo de clasificación usando Random Forest para predecir la supervivencia de los pasajeros del Titanic.

## Evolución del Modelo

### Random Forest Base
Iniciamos el proyecto construyendo un modelo base de Random Forest sin ninguna optimización de hiperparámetros ni ingeniería de características. El modelo base fue construido usando todas las características disponibles en el conjunto de datos sin ningún preprocesamiento adicional. Los resultados obtenidos fueron:

- Accuracy: 0.8268
- Precision: 0.8116
- Recall: 0.7568
- F1 Score: 0.7832

En Kaggle obtuvimos este resultado:
![Random Forest Base](imagenes/RandomForestBase.png)

### Random Forest con Grid Search
Después de construir el modelo base, realizamos una búsqueda de hiperparámetros usando Grid Search. Grid Search es una técnica que permite explorar múltiples combinaciones de hiperparámetros para encontrar la combinación que produce el mejor rendimiento del modelo. Los hiperparámetros optimizados incluyeron el número de árboles en el bosque (`n_estimators`), la profundidad máxima de los árboles (`max_depth`), el número mínimo de muestras necesarias para dividir un nodo interno (`min_samples_split`), y el número mínimo de muestras necesarias para estar en un nodo hoja (`min_samples_leaf`). Los resultados obtenidos con esta optimización fueron:

- Accuracy: 0.8212
- Precision: 0.8
- Recall: 0.7568
- F1 Score: 0.7778

En Kaggle obtuvimos este resultado:

![Random Forest Grid](imagenes/RandomForestGrid.png)

### Random Forest Optimizado
Finalmente, realizamos ingeniería de características, añadiendo nuevas variables como el título, el tamaño de la familia, si el pasajero era niño, y la tarifa por persona. Estas características adicionales se crearon a partir de las características existentes en el conjunto de datos. Por ejemplo, el título se extrajo del nombre, el tamaño de la familia se calculó sumando el número de hermanos/cónyuges y padres/hijos, y la tarifa por persona se calculó dividiendo la tarifa por el tamaño de la familia. También ajustamos manualmente los hiperparámetros, obteniendo los siguientes resultados:

- Accuracy: 0.8547
- Precision: 0.8529
- Recall: 0.7838
- F1 Score: 0.8169

En Kaggle obtuvimos este resultado:

![Random Forest Optimizado](imagenes/RandomForestOptimizado.png)

## Correcciones Realizadas

Durante el desarrollo del proyecto, recibimos retroalimentación valiosa que nos ayudó a mejorar nuestro modelo:

1. **Overfitting**: En una de las primeras iteraciones, nuestro modelo sufría de sobreajuste, lo que significa que el modelo aprendía muy bien los datos de entrenamiento, pero no generalizaba bien a datos nuevos. Para solucionar este problema, ajustamos los hiperparámetros del modelo, en particular `max_depth`, `min_samples_split`, y `min_samples_leaf`, para controlar la complejidad del modelo y reducir el riesgo de sobreajuste.

2. **Ingeniería de Características**: Inicialmente, utilizamos el conjunto de datos sin realizar ninguna ingeniería de características. Sin embargo, después de la retroalimentación, añadimos varias nuevas características que ayudaron a mejorar el rendimiento del modelo. Por ejemplo, añadimos una característica que indicaba si el pasajero era un niño, ya que los niños tenían más probabilidades de ser rescatados.

3. **Selección de Características**: Basándonos en la retroalimentación recibida, realizamos una selección de características más cuidadosa, eliminando características que no aportaban información significativa al modelo. Por ejemplo, eliminamos la característica 'Cabin' porque tenía muchos valores faltantes y no aportaba información útil para predecir la supervivencia.

---


