# Segundo examen parcial

## Descripción del Proyecto
Este repositorio contiene la solución al segundo examen parcial de Modelos No Lineales para Pronósticos, donde se implementan redes neuronales para predecir series de tiempo univariadas y multivariadas.

## Estructura del Repositorio

melanie257michel/

├── Daily_Demand_Forecasting_Orders.csv # Datos multivariados

├── Examen2_MNL_MMR_Mutli.ipynb # Notebook para análisis multivariado

├── Examen2_MNL_MMR_Uni.ipynb # Notebook para análisis univariado

├── Hourly-train.csv # Datos univariados (series horarias)

├── m4_info.csv # Metadatos de series univariadas

└── README.md # Este archivo



## Conjuntos de Datos

### 1. Datos Univariados
- **Archivos**:
  - `Hourly-train.csv`: Series de tiempo horarias del conjunto M4
  - `m4_info.csv`: Metadatos con frecuencia, horizonte y fecha de inicio
- **Series asignadas**: H115, H243, H384, H402, H44
- **Características**:
  - Cada fila representa una serie de tiempo
  - Cada columna representa un paso de tiempo
  - Horizonte de predicción variable por serie

### 2. Datos Multivariados
- **Archivo**: `Daily_Demand_Forecasting_Orders.csv`
- **Características**:
  - 60 días (filas) y 13 atributos (columnas)
  - Objetivo: Predecir el total de pedidos diarios (Target)
  - Variables predictoras incluyen:
    - Semana del mes
    - Día de la semana
    - Tipos de pedidos (urgentes, no urgentes, tipos A/B/C)
    - Sectores (fiscal, controlador de tráfico, bancarios)

## Implementación

### Notebooks Principales
1. **Examen2_MNL_MMR_Uni.ipynb**:
   - Clases implementadas:
     - `TimeSeriesAnalyzer`: Para análisis y visualización de datos
     - `TimeSeriesExamSolver`: Para implementación de modelos y optimización
   - Modelos implementados:
     - MLP, CNN, LSTM, CNN-LSTM
   - Proceso:
     - Carga y preprocesamiento de datos
     - División en train/val/test
     - Entrenamiento y evaluación de modelos
     - Optimización con Optuna

2. **Examen2_MNL_MMR_Mutli.ipynb**:
   - Clases implementadas:
     - `MultivariateForecaster`: Para análisis y modelado multivariado
     - `MultivariateOrderForecaster`: Para optimización con Optuna
   - Modelos implementados:
     - MLP, CNN, LSTM, CNN-LSTM
   - Proceso:
     - Análisis exploratorio
     - Normalización de datos
     - Entrenamiento y evaluación
     - Ajuste de hiperparámetros

## Métricas de Evaluación
Para ambos conjuntos de datos se utilizaron:
- RMSE (Root Mean Square Error)
- MAE (Mean Absolute Error)
- MAPE (Mean Absolute Percentage Error)
- R² (Coeficiente de determinación)

## Optimización con Optuna
Se ajustaron los siguientes hiperparámetros:
- Número de capas y unidades
- Tasa de aprendizaje
- Tipo de optimizador
- Funciones de activación
- Tamaño de ventana para series temporales

## Resultados y Conclusiones
Los notebooks contienen análisis detallados de:
- Preprocesamiento necesario para cada conjunto de datos
- Comparación de arquitecturas de redes neuronales
- Resultados antes y después de la optimización
- Visualizaciones de series y predicciones
- Conclusiones sobre el desempeño de cada modelo



Melanie Michel Rodríguez  
Curso: Modelos No Lineales para Pronósticos  
