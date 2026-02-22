# Telecom X – Análisis de Churn (ETL y Modelado Predictivo con Python)

## Propósito del Proyecto

Este proyecto tiene como objetivo analizar los factores que influyen en la cancelación de clientes (Churn) en la empresa **Telecom X**, utilizando un proceso completo de:

- ETL (Extract, Transform, Load)
- Análisis Exploratorio de Datos (EDA)
- Modelado Predictivo con Machine Learning
- Interpretación de variables
- Generación de estrategias de retención

El análisis busca generar insights que apoyen la toma de decisiones estratégicas orientadas a la reducción del churn y la mejora en la retención de clientes.

---

## Tecnologías Utilizadas

- Python
- Pandas
- NumPy
- Requests
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab
- Git & GitHub

---

## Proceso ETL

### 1. Extracción

Los datos se obtienen desde una API en formato JSON alojada en un repositorio de GitHub.

Se realiza la consulta mediante `requests` y se cargan los datos en un DataFrame de Pandas.

---

### 2. Transformación

Durante esta etapa se realizaron las siguientes tareas:

- Normalización de datos anidados
- Limpieza de valores faltantes (ej. registros con `Churn` vacío)
- Eliminación o imputación de valores nulos
- Conversión de tipos de datos numéricos
- Estandarización de nombres de columnas
- Codificación de variables categóricas (One-Hot Encoding)
- Escalamiento de variables numéricas para modelos sensibles a la distancia

---

### 3. Carga

El dataset limpio y transformado se exporta a un archivo CSV para su posterior análisis y modelado.

---

## Análisis Exploratorio de Datos (EDA)

Durante el análisis se identificaron los siguientes hallazgos clave:

- Los contratos **Month-to-month** presentan la mayor tasa de churn.
- Los clientes con menor antigüedad (`tenure`) tienden a cancelar con mayor frecuencia.
- Los cargos mensuales elevados están asociados a una mayor probabilidad de churn.
- El método de pago *Electronic Check* muestra mayor tasa de cancelación.
- Los clientes con contratos de largo plazo (One year / Two year) presentan menor churn.

### Visualizaciones Incluidas

- Distribución general de churn
- Churn por tipo de contrato
- Cargos mensuales vs churn
- Antigüedad del cliente vs churn
- Importancia de variables (Random Forest)

---

## Modelado Predictivo

Se entrenaron y evaluaron múltiples modelos de Machine Learning para predecir la cancelación:

- Regresión Logística
- K-Nearest Neighbors (KNN)
- Random Forest
- Support Vector Machine (SVM)

### División de Datos

- 80% entrenamiento
- 20% prueba
- División estratificada para mantener la proporción de clases

### Métricas Evaluadas

- Accuracy
- Precision
- Recall
- F1-Score
- Matriz de confusión

---

## Interpretación de Variables

El análisis de importancia de variables mostró que los factores más influyentes en la cancelación son:

1. Antigüedad del cliente (`tenure`)
2. Tipo de contrato
3. Cargo mensual
4. Método de pago
5. Tipo de servicio de internet

Los modelos coinciden en que:

- Clientes nuevos tienen mayor riesgo de churn.
- Contratos mensuales presentan mayor probabilidad de cancelación.
- Contratos de largo plazo reducen significativamente el riesgo.

---

## Conclusiones Estratégicas

Basado en los resultados obtenidos, se proponen las siguientes estrategias de retención:

- Incentivar contratos de largo plazo mediante descuentos.
- Implementar programas de retención temprana durante los primeros meses.
- Ofrecer beneficios por métodos de pago automáticos.
- Diseñar promociones personalizadas para clientes con altos cargos mensuales.
- Monitorear activamente clientes con contrato mensual.

---
