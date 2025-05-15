# forest-cover-type-classification
Multiclass classification of forest cover types using K-Nearest Neighbors and Decision Tree algorithms. This project compares the performance of both models, analyzes their outcomes, and includes visualizations. Based on the U.S. Forest Service dataset

# 🌲 Forest Cover Type Classification: KNN vs Decision Tree  
### Clasificación del tipo de cobertura forestal: KNN vs Árbol de Decisión

## 📌 Project Overview / Descripción del Proyecto

**English:**  
This project compares two classification models—K-Nearest Neighbors (KNN) and Decision Tree—to predict the forest cover type based on cartographic and environmental features. It was developed as a second partial project for a data science course, aiming to evaluate performance differences between the two models on a multi-class dataset.

**Español:**  
Este proyecto compara dos modelos de clasificación—K Vecinos más Cercanos (KNN) y Árbol de Decisión—para predecir el tipo de cobertura forestal a partir de características cartográficas y ambientales. Fue desarrollado como proyecto del segundo parcial de un curso de ciencia de datos, con el objetivo de evaluar el rendimiento de ambos modelos en un conjunto de datos multiclase.

## 🔗 Dataset

- **Source / Fuente:** [Kaggle - Forest Cover Type Prediction](https://www.kaggle.com/competitions/forest-cover-type-prediction/data)  
- The dataset contains over 500,000 entries and 50+ columns.

## 📊 Dataset Description / Descripción del Conjunto de Datos

**English:**  
The DataFrame includes topographical features such as `Elevation`, `Aspect`, and `Slope`, hydrological and roadway distances (`Horizontal_Distance_To_Hydrology`, `Horizontal_Distance_To_Roadways`), and hillshade indices like `Hillshade_9am`. It also contains binary indicators for wilderness areas and soil types (`Wilderness_Area1`, `Soil_Type1`, etc.), as well as the target variable `Cover_type`. Most columns are numerical (`int64`), and the target variable represents forest cover categories.

**Español:**  
El DataFrame incluye características topográficas como `Elevation` (Elevación), `Aspect` (Orientación) y `Slope` (Pendiente), distancias hidrológicas y a carreteras (`Horizontal_Distance_To_Hydrology`, `Horizontal_Distance_To_Roadways`) e índices de sombreado como `Hillshade_9am`. También contiene indicadores binarios para áreas silvestres y tipos de suelo (`Wilderness_Area1`, `Soil_Type1`, etc.), así como la variable objetivo `Cover_type`. La mayoría de las columnas son numéricas (`int64`) y la variable objetivo representa las categorías de cobertura forestal.

## 🧹 Preprocessing / Preprocesamiento

**English:**  
The columns `Unnamed: 0`, `Unnamed: 1`, and `Unnamed: 2` were removed because they did not contain meaningful information for the analysis. These columns were artifacts from the original file (likely indexes or unlabelled values) and were not related to the actual features of the dataset.

**Español:**  
Se eliminaron las columnas `Unnamed: 0`, `Unnamed: 1` y `Unnamed: 2` porque no contenían información relevante para el análisis. Estas columnas eran artefactos del archivo original (probablemente índices o valores sin contexto) y no estaban relacionadas con las características reales del conjunto de datos.

## 🧪 Models and Evaluation / Modelos y Evaluación

### ✅ K-Nearest Neighbors (KNN)

- GridSearch was used to find the optimal value of `k`.
- The best value found was `k = X` (reemplaza con tu resultado).
- Accuracy: **0.5820**

### 🌳 Decision Tree Classifier

- Trained with default parameters.
- Accuracy: **0.9092**

### 📈 Metrics Compared / Métricas Comparadas

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

## 🧠 Conclusion / Conclusión

**English:**  
The Decision Tree model achieved a significantly higher accuracy (0.9092) compared to the K-Nearest Neighbors model (0.5820). Additionally, the decision tree showed better precision, recall, and f1-score values in almost all classes.

This may be because decision trees better handle non-linear relationships and complex hierarchical structures in the data, while KNN can be negatively affected by variable scale and noisy or unrepresentative nearby instances.

**Español:**  
El modelo de Árbol de Decisión obtuvo una exactitud significativamente mayor (0.9092) en comparación con el modelo de K Vecinos más Cercanos (0.5820). Además, el árbol de decisión presentó mejores valores en precisión, recall y f1-score en casi todas las clases.

Esto puede deberse a que los árboles de decisión se adaptan mejor a relaciones no lineales y a estructuras jerárquicas complejas en los datos, mientras que KNN puede verse afectado negativamente por la escala de las variables y la cantidad de ruido o datos poco representativos en sus vecinos más cercanos.

## 🛠️ Requirements

To run this project, install the dependencies using:

```bash
pip install -r requirements.txt
