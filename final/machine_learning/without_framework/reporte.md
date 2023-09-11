**Regresión Logística: Resumen**

La regresión logística es un método estadístico utilizado principalmente para problemas de clasificación binaria, es decir, cuando quieres predecir si un evento o resultado pertenece a una de dos categorías, como sí/no, 1/0, o positivo/negativo. Aunque el nombre contiene la palabra "regresión", en realidad se trata de un algoritmo de clasificación.

**Cómo funciona:**

1. **Definición de variables independientes:** Comienza reuniendo datos y definiendo tus variables independientes (predictoras) y la variable dependiente (la que quieres predecir o clasificar). Por ejemplo, si deseas predecir si un estudiante aprobará o no un examen, las variables independientes podrían ser horas de estudio y calificaciones previas, y la variable dependiente sería si el estudiante aprobó (1) o no (0).

2. **Transformación logística:** La regresión logística utiliza una función logística (también conocida como función sigmoide) para transformar la combinación lineal de las variables independientes en un valor entre 0 y 1, que se interpreta como la probabilidad de que el resultado pertenezca a la categoría positiva (1). La función logística tiene la forma:

   \[P(Y=1) = \frac{1}{1 + e^{-(b_0 + b_1X_1 + b_2X_2 + \ldots + b_nX_n)}}\]

   Donde:
   - \(P(Y=1)\) es la probabilidad de que el resultado sea 1.
   - \(b_0, b_1, b_2, \ldots, b_n\) son los coeficientes de la regresión que se ajustan durante el entrenamiento.
   - \(X_1, X_2, \ldots, X_n\) son los valores de las variables independientes.

3. **Entrenamiento del modelo:** El objetivo es encontrar los mejores valores para los coeficientes \(b_0, b_1, b_2, \ldots, b_n\) que minimicen el error en las predicciones. Esto se hace mediante técnicas de optimización, como la maximización de la verosimilitud.

4. **Umbral de decisión:** Para realizar una clasificación, debes definir un umbral de decisión, típicamente 0.5. Si la probabilidad predicha es mayor que el umbral, clasificas el resultado como 1; de lo contrario, lo clasificas como 0.

5. **Evaluación del modelo:** Para evaluar qué tan bien funciona el modelo, se utilizan métricas como precisión, exhaustividad, F1-score y la curva ROC, entre otras.

6. **Predicciones:** Con el modelo entrenado y evaluado, puedes usarlo para hacer predicciones en nuevos datos desconocidos.

En resumen, la regresión logística es una técnica de aprendizaje supervisado que se utiliza para problemas de clasificación binaria. Transforma la combinación lineal de las variables independientes en una probabilidad utilizando una función logística y ajusta los coeficientes para hacer predicciones y tomar decisiones de clasificación.

## Dataestt: Heart Attack Analysis & Prediction Dataset

**Nombre del conjunto de datos:** Heart Attack Analysis & Prediction Dataset

**URL donde se encuentra:** [Heart Attack Analysis & Prediction Dataset](https://www.kaggle.com/rashikrahmanpritom/heart-attack-analysis-prediction-dataset)

Este conjunto de datos se encuentra alojado en Kaggle y es utilizado para el análisis y la predicción de ataques al corazón. Puedes acceder a él a través del enlace proporcionado y descargarlo desde la plataforma de Kaggle para su uso en análisis y proyectos relacionados con la salud cardiovascular.

**Descripción de las Variables:**
1. `age`: Edad del paciente.
2. `sex`: Género del paciente (0 = mujer, 1 = hombre).
3. `cp`: Tipo de dolor en el pecho (0 = típico angina, 1 = angina atípica, 2 = dolor no anginal, 3 = asintomático).
4. `trestbps`: Presión arterial en reposo (en mm Hg).
5. `chol`: Colesterol sérico en mg/dL.
6. `fbs`: Nivel de azúcar en sangre en ayunas (0 = no elevado, 1 = elevado).
7. `restecg`: Resultados del electrocardiograma en reposo (0 = normal, 1 = anormalidad en la onda ST-T, 2 = hipertrofia ventricular izquierda probable).
8. `thalach`: Frecuencia cardíaca máxima alcanzada.
9. `exang`: Angina inducida por ejercicio (0 = no, 1 = sí).
10. `oldpeak`: Depresión del ST inducida por el ejercicio en relación con el reposo.
11. `slope`: La pendiente del segmento ST de ejercicio (0 = ascendente, 1 = plano, 2 = descendente).
12. `ca`: Número de vasos principales (0-3) coloreados por fluoroscopia.
13. `thal`: Tipo de defecto cardíaco (3 = normal, 6 = defecto fijo, 7 = defecto reversible).

**Variable Objetivo (Clase):**
14. `output`: Variable binaria que indica la probabilidad de sufrir un ataque al corazón (0 = No tiene riesgo de ataque al corazón, 1 = Tiene riesgo de ataque al corazón).

## Problema a resolver

El tipo de problema a resolver utilizando el conjunto de datos "Heart Attack Analysis & Prediction Dataset" es un problema de **clasificación binaria**. En este tipo de problema, el objetivo es predecir una variable categórica que tiene dos clases posibles. En este caso, la variable objetivo es `output`, que indica si un paciente tiene riesgo de sufrir un ataque al corazón o no. Las dos clases en esta clasificación binaria son:

1. **Clase Positiva (1):** Indica que el paciente tiene riesgo de sufrir un ataque al corazón.

2. **Clase Negativa (0):** Indica que el paciente no tiene riesgo de sufrir un ataque al corazón.

Por lo tanto, el objetivo es desarrollar un modelo predictivo que, en función de las características médicas y clínicas de un paciente (las otras columnas del conjunto de datos), pueda predecir con precisión si ese paciente tiene riesgo de sufrir un ataque al corazón o no.

## Métricas de evaluación
Dado que se trata de un problema de clasificación binaria, las métricas de evaluación comunes incluyen la precisión, la sensibilidad (recall), la especificidad, el área bajo la curva ROC (AUC-ROC) y otras medidas relacionadas con la evaluación del rendimiento del modelo.

Este tipo de problema es crucial en el campo de la salud, ya que puede ayudar a identificar a las personas que corren un mayor riesgo de enfermedades cardíacas y, por lo tanto, permitir una intervención médica temprana y preventiva.

## Predicciones
![Matriz de confusión sin Framework]('cf_wo_fw.png')

## Evaluacion del modelo con base a las predicciones
Podemos ver en la matriz de confusión que nuestro modelo tuvo un buen desempeño clasificando a las personas que tendrán un ataque al corazón, sería interesante seguir trabajando en el modelo para mejorar la precisión de la clasificación de las personas que no tendrán un ataque al corazón. Igualmente  en las metricas de desempeño que se muestran a continuación se puede ver que el modelo tuvo un buen desempeño:

- Accuracy: 0.7869
- True Positives: 26
- True Negatives: 22
- False Positives: 7
- False Negatives: 6
- Precision: 0.7879
- Recall: 0.8125
- F1-Score: 0.8000

En general para mi destacan tanto el recall como el f1-score, ya que nos indican que el modelo tuvo un buen desempeño clasificando a las personas que tendrán un ataque al corazón que es lo que nos interesa predecir porque en este caso si bien no hay tanto problema al predecir que una persona no tendrá un ataque al corazón en comparación a alguien que lo va a tener, es por esto que en este caso en particula el recall es una de las metricas que más me interesan.

## Conclusiones

En conclusión, la regresión logística es una valiosa herramienta para abordar problemas de clasificación binaria, como la predicción de ataques al corazón. A través de la transformación logística de variables independientes y el ajuste de coeficientes, este método permite evaluar el riesgo de enfermedades cardíacas basado en una variedad de características médicas y clínicas.

El conjunto de datos "Heart Attack Analysis & Prediction Dataset" proporciona información detallada para abordar este desafío de clasificación binaria. Nuestro modelo logró un desempeño destacado, especialmente en la identificación de personas en riesgo de sufrir un ataque al corazón, lo que es crucial en el contexto de la salud cardiovascular. Las métricas de evaluación, incluyendo el recall y el f1-score, indican que el modelo es prometedor y podría mejorar aún más con refinamientos adicionales.

En última instancia, esta aplicación de la regresión logística demuestra su utilidad en la identificación temprana de personas en riesgo de enfermedades cardíacas, lo que puede llevar a una atención médica preventiva y mejorada.