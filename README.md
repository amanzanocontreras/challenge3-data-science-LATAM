# Telecom X – Análisis de Churn (ETL con Python)

## Propósito del Proyecto
Este proyecto tiene como objetivo analizar los factores que influyen en la cancelación de clientes (Churn) en la empresa Telecom X, utilizando un proceso ETL completo (Extract, Transform, Load) y análisis exploratorio de datos con Python.

El análisis busca generar insights que apoyen la toma de decisiones estratégicas orientadas a la retención de clientes.

---

## Tecnologías Utilizadas
- Python
- Pandas
- Requests
- Matplotlib
- Jupyter Notebook / Google Colab
- Git & GitHub

---

## Proceso ETL

### Extracción
Los datos se obtienen desde una API en formato JSON alojada en un repositorio de GitHub.

### Transformación
- Normalización de datos anidados
- Limpieza y tratamiento de valores nulos
- Conversión de tipos de datos
- Estandarización de nombres de columnas

### Carga
El dataset limpio se exporta a un archivo CSV para su posterior análisis.

---

## Análisis y Visualizaciones

Durante el análisis se identificaron los siguientes hallazgos clave:

- Los contratos mensuales presentan la mayor tasa de churn.
- Los clientes con menor antigüedad tienden a cancelar con mayor frecuencia.
- Los cargos mensuales elevados están asociados a una mayor probabilidad de churn.

Ejemplos de visualizaciones incluidas:
- Distribución general de churn
- Churn por tipo de contrato
- Cargos mensuales vs churn
- Antigüedad del cliente vs churn
