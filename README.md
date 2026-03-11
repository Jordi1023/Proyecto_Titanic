#  Proyecto Titanic - Predicción de Supervivencia

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Latest-purple?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Latest-orange?logo=scikitlearn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Latest-red?logo=python)
![Status](https://img.shields.io/badge/Estado-Completado-success)

## Descripción del Proyecto

Este es mi primer proyecto de **Data Science y Machine Learning**, basado en el famoso desafío de Kaggle: ["Titanic: Machine Learning from Disaster"](https://www.kaggle.com/c/titanic). 

El objetivo es predecir qué pasajeros tenían más probabilidades de sobrevivir al trágico hundimiento del Titanic en 1912, utilizando características como la edad, el sexo, la clase del ticket, entre otros.

## 🎯 Objetivo

Construir un modelo de clasificación que pueda predecir con precisión si un pasajero sobrevivió (1) o no (0), aplicando técnicas de limpieza de datos, análisis exploratorio y machine learning.

## 📊 Resultados Obtenidos

- **Precisión del modelo:** 79% en el conjunto de validación
- **Modelo utilizado:** Random Forest Classifier (200 árboles)
- **Mejores predictores:** Sexo, clase social (Pclass) y edad

## 🛠️ Tecnologías y Librerías Utilizadas

- **Python 3.x**
- **Pandas** - Manipulación y análisis de datos
- **NumPy** - Cálculos numéricos
- **Matplotlib y Seaborn** - Visualización de datos
- **Scikit-learn** - Machine learning (Random Forest, train/test split, métricas)
- **SciPy** - Estadística (cálculo de sesgo)

## 📋 Estructura del Análisis

### 1️⃣ Análisis Exploratorio de Datos (EDA)
- Exploración inicial de las variables
- Identificación de valores faltantes
- Análisis de outliers en la columna `Age` usando el método IQR
- Visualización de distribuciones (histogramas y KDE)

### 2️⃣ Limpieza y Transformación de Datos
- **Edad (Age):** 
  - Identificados 11 outliers
  - Sesgo de 0.388 (distribución aproximadamente simétrica)
  - Valores nulos imputados con la **mediana** (28 años)
  
- **Puerto de Embarque (Embarked):** 
  - 2 valores nulos imputados con la **moda**
  
- **Cabina (Cabin):** 
  - Extraída la primera letra (cubierta)
  - Valores nulos categorizados como 'UNKNOWN' para no perder información

### 3️⃣ Ingeniería de Características (Feature Engineering)
- Conversión de variables categóricas a numéricas mediante **one-hot encoding**:
  - `Sex`: male/female
  - `Embarked`: Q, S, C
  - `Cabin`: A, B, C, D, E, F, G, T, UNKNOWN
- **Variables finales:** 16 características para el modelo

### 4️⃣ Modelado
- División de datos: 80% entrenamiento, 20% validación
- Algoritmo: **Random Forest Classifier** con 200 árboles
- Entrenamiento y validación del modelo

### 5️⃣ Evaluación
- **Métrica utilizada:** Accuracy (precisión)
- **Resultado:** 79% de precisión en validación

## 📈 Visualizaciones Incluidas

- Box plot de edades (detección de outliers)
- Histograma con curva KDE de la distribución de edades
- Comparación visual entre media y mediana

## 🚀 Cómo Ejecutar el Proyecto

### Requisitos previos
Tener instalado Python 3.x y las siguientes librerías:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
