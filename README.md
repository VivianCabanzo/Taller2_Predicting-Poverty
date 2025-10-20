# Taller2_BigData_MachineLearning  
### Predicción de Pobreza (GEIH 2018)

[![Kaggle](https://img.shields.io/badge/Data-Kaggle-orange.svg)](https://www.kaggle.com/)
[![Made with](https://img.shields.io/badge/Made%20with-RStudio-75AADB.svg)](https://posit.co/)

---

## Descripción general

Este repositorio contiene el desarrollo del **Taller 2 — Big Data y Machine Learning**, realizado en el marco de la **Maestría en Economía Aplicada** de la **Universidad de Los Andes**.  

El objetivo del trabajo es **predecir la condición de pobreza de hogares en Colombia** utilizando la **Gran Encuesta Integrada de Hogares (GEIH) 2018**, elaborada por el **DANE**.  

El análisis abarca todo el ciclo de modelamiento predictivo: desde la limpieza y estructuración de los datos hasta el entrenamiento, validación y comparación de modelos de aprendizaje automático.

---

## Contenido del análisis

### 1. Preparación y limpieza de datos
- Integración de bases a nivel de **hogares** y **personas**.  
- Creación de variables derivadas y tratamiento de valores faltantes.  
- Análisis exploratorio de variables socioeconómicas y demográficas.

### 2. Entrenamiento y validación de modelos
Se implementan diferentes algoritmos de aprendizaje supervisado para la predicción binaria de pobreza:

1. Regresión Lineal  
2. Modelo Probabilístico Logit  
3. Elastic Net  
4. CART (árbol de decisión)  
5. Random Forest  
6. Boosting  
7. Ensamble CART + Boosting  

### 3. Evaluación del desempeño
- Métricas empleadas: **F1-Score**, **Precisión**, **Recall**, **ROC-AUC**.  
- Validación cruzada.  

---

## Estructura del repositorio

| Carpeta / Archivo | Descripción |
|--------------------|-------------|
| **Bases de datos/** | Datasets de entrenamiento y prueba (GEIH 2018). |
| **Documentos complementarios/** | Informe del DANE y documentos de referencia. |
| **Scripts/** | Código fuente del proyecto (`PredictingPoverty.Rmd`). |
| **Predicciones/** | Archivos `.csv` listos para envío en Kaggle. |
| **Tablas y Gráficos/** | Tablas resumen y visualizaciones finales. |
| **Presentaciones/** | Diapositivas con resultados y conclusiones. |
| **Documento final/** | Informe consolidado con análisis y resultados. |

---

## Resultados destacados

- En Elastic Net el **ajuste del umbral de clasificación** mejoró el equilibrio entre precisión y sensibilidad, elevando el F1-score del modelo.  

---

## Equipo de trabajo

| Integrante | Código |
|-------------|------|
| **Vivian Cabanzo Fernández** | 202513800 | 
| **Laura Daniela Diaz Torres** | 202425507 |
| **Cristian Felipe Muñoz Guerrero** | | 
| **Zeneth Olivero Tapia** | 202512665 |

> Cada integrante realizó al menos cinco contribuciones significativas al repositorio.

---

## Fuente de datos

**DANE (2018)** — *Gran Encuesta Integrada de Hogares (GEIH)*  
---

## Requisitos de ejecución

- **Lenguaje:** R (versión ≥ 4.2)  
- **Entorno:** RStudio / Posit  
- **Librerías principales:**  
  ```r
  library(tidyverse) # Incluye dplyr, tidyr, ggplot2, readr, purrr
  library(caret) # Herramientas preprocesamiento, selección de modelos y evaluación de algoritmos de ML
  library(glmnet) # Implementación eficiente de modelos de regresión regularizados (EN, Lasso y Ridge)
  library(rpart) # Implementar arboles de decision
  library(xgboost) # Algoritmo de Gradient Boosting optimizado
  library(gt) # Presentación de Tablas
  library(webshot2) # Guardar Tablas y Gráficos en HTML y PDF
  
