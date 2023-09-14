# Resumen de Modelos Aplicados

## SVM (Support Vector Machine)
Se implementó un modelo SVM con un kernel lineal. Se realizó la carga y preparación de datos, incluida la eliminación de columnas irrelevantes y la codificación de variables categóricas. Luego, se dividió el dataset en entrenamiento y prueba, se estandarizaron las características y se entrenó el modelo SVM. Finalmente, se evaluó el modelo utilizando métricas como precisión, recall y F1-score. La precisión obtenida fue de 0.72.

## K-Nearest Neighbors (KNN)
Se realizó la preparación de datos y se dividió el conjunto de entrenamiento en características (X) y etiquetas (y). Se procesó el conjunto de prueba para que coincida con las características de entrenamiento y se inicializó el clasificador KNN. Se entrenó el modelo KNN en los datos de entrenamiento y se calcularon las predicciones en el conjunto de entrenamiento. La precisión obtenida fue de 0.70.

## Random Forest
Se eliminaron columnas no utilizadas y se codificaron variables categóricas. Luego, se dividió el conjunto de entrenamiento en subconjuntos de entrenamiento y validación. Se creó el modelo de Random Forest y se entrenó en el subconjunto de entrenamiento. Se hicieron predicciones en el subconjunto de validación y se calcularon métricas numéricas. La precisión obtenida fue de 0.82.

# Conclusión
El modelo que obtuvo la mejor precisión fue el Random Forest con una precisión de 0.82, seguido por el SVM con 0.72 y luego el KNN con 0.70. Por lo tanto, el modelo Random Forest fue el que se seleccionó para hacer predicciones en el conjunto de prueba y se guardó el archivo de submission para Kaggle.

