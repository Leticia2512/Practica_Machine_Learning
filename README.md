# Practica-Machine_Learning
Práctica Módulo Machine Learning Bootcamp Big Data, Machine Leraning &amp; IA
___

Este repositorio contiene la implementación de modelos de **regresión** en **Python** para predecir los **precios de viviendas en Airbnb**, utilizando paar ello datos reales del dataset de **listings de Airbnb**.

---

## 🎯 Objetivos del Proyecto
- **Carga de datos y división en train y test**: Carga de datos del dataset y dividimos en el conjunto de train y test.
- **Análisis exploratorio de datos (EDA)**: Se examinan y visualizan los datos para comprender sus características principales y relaciones internas.    
- **Preprocesamiento de datos**: Limpieza, transformación y generación de variables para su uso en modelos.  
- **Desarrollo y entrenamiento de modelos**: Entrenamiento de los modelos, aplicando **GridSearch** para ajustar los hiperparámetros, con validación cruzada K-folds.
- **Selección y evaluación del mejor modelo**: Evaluación de las métricas adecuadas (MSE, RMSE, R²) y elección del modelo óptimo.
- **Predicción y evaluación del rendimiento**: Predecimos el precio de la vivienda con los datos de prueba y evaluamos el rendimiento final del modelo (MSE, RMSE, R²).

---

## 📊 Dataset
Para el proyecto se ha utiliza el dataset [**airbnb-listings-extract**](#) que contiene información detallada de viviendas listadas en Airbnb, incluyendo características como ubicación, número de habitaciones, servicios y precios.

---

## 🛠️ Lenguajes y Herramientas Utilizadas
- **Lenguaje:** Python (versión 3.12.9).
- **IDE:** Jupyter Notebook / VSCode  
- **Librerías principales:**  
  - `pandas`  
  - `numpy`  
  - `matplotlib` y `seaborn`  
  - `scikit-learn`  
  - `statsmodels`  
  - `xgboost`  
  - `category_encoders`  

---

## 📈 Conclusiones
Se han entrenado los siguientes modelos:
  - Regresión Lineal  
  - Regresión Lasso  
  - Random Forest Regressor  
  - XGBoost Regressor
    
Aunque los mejores resultados obtenidos durante el entrenamiento fueron con **Random Forest**, el modelo final escogido para evaluar con los datos de prueba fue **XGBoost**, debido a que a que tiene mejor capacidad de generalización, presenta regularización integrada (L1, L2) con penalización, y por tanto, tiene menor riesgo de **overfitting**.

El modelo XGBoost muestra un buen desempeño tanto en el conjunto de entrenamiento como en el de prueba.

- En entrenamiento, el RMSE de 16.25 y un R² de 0.872 indican que el modelo captura bien la relación entre las variables predictoras y el precio, pero sin sobreajustar excesivamente.

- En test, el RMSE de 22.99 y un R² de 0.755 muestran que el modelo generaliza adecuadamente a datos nuevos, con una caída razonable en desempeño.

El balance entre buen ajuste en train y capacidad de generalización en test sugiere que el modelo está bien entrenado y es robusto para predecir precios de viviendas en Airbnb dentro del rango de datos analizado.

