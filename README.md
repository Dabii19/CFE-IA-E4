# CFE-IA-E4


Este proyecto utiliza el dataset **Wine Quality Dataset** de Kaggle para predecir la calidad de un vino a partir de sus propiedades fisicoquímicas.

---

## Objetivo
Entrenar un modelo de clasificación que estime la **calidad del vino** en función de variables y realizar predicciones con valores ingresados manualmente.

---

## Datos:
- **Variables:**
  - `fixed acidity`: acidez fija  
  - `volatile acidity`: acidez volátil  
  - `citric acid`: ácido cítrico  
  - `residual sugar`: azúcar residual  
  - `chlorides`: cloruros  
  - `alcohol`: porcentaje de alcohol  
  - `quality`: variable objetivo (escala 0–10)

---

## Pasos realizados

### 1. Carga y preprocesamiento de datos
- Se cargó el dataset `winequality-red.csv`.  
- Se separaron las variables independientes (X) y la variable objetivo (`quality`).  
- Se aplicó **StandardScaler** para normalizar los datos.  

### 2. Creación de gráficos e implementación del modelo KNN
- Se creó un mapa de calor para observar las mejores relaciones entre variables, las seleccionadas fueron:
  - `sulphates`, `alcohol` y `citric acid` (Sulfato, alcohol y ácido cítrico)
- Se crearon gráficos de dispersión e histograma con las variables seleccionadas.
- Se entrenó un modelo `KNeighborsClassifier`.

  

### 3. Ingreso manual de datos y predicción
- Se ingresan los valores de alcohol, sulfato y ácido cítrico
- Se ejecuta el código y este mostrará el resultado.

## Observaciónes
- Con el sulfato fijo en 0.60 y el alcohol en 0.19 mientras se varía el ácido el resultado se mantiene en 3
- con el sulfato y el ácido fijos mientras varia el alcohol muestra estos resultados:
  - Con 6.0 de alcohol hacia abajo la calidad baja
  - Al llegar a 6 hacia arriba se mantiene la calidad en 6
- No se encontró combincación de valores que exedan la calidad de 6. 
