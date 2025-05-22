# jester

# Jester Recommender System

Este repositorio contiene el proyecto final de sistemas de recomendación, centrado en el uso del dataset **Jester**, una base de datos de puntuaciones de chistes recolectada de usuarios reales. El objetivo principal es comparar distintas técnicas de recomendación y evaluar su rendimiento.

## 📊 Dataset

- **Nombre**: Jester dataset (jester-data-1)
- **Características**:
  - Puntuaciones numéricas continuas entre **-10** y **10**
  - Las puntuaciones faltantes están marcadas como **99**
  - Contiene evaluaciones de **100 chistes** por más de **73.000 usuarios** (en nuestro caso: 943 usuarios y 1682 ítems seleccionados para evaluación)

## 🧠 Técnicas implementadas

Se han comparado cuatro enfoques principales para el sistema de recomendación:

1. **K-Nearest Neighbors (KNN)**  
   - Basado en similitud entre usuarios o ítems  
   - Uso de métricas como coseno o correlación de Pearson  
   - Buena interpretación, pero limitado en escalabilidad

2. **Matrix Factorization (MF)**  
   - Factorización de la matriz de utilidad mediante descenso por gradiente  
   - Variación de hiperparámetros como número de factores y tasa de aprendizaje  
   - Se evaluó con datos normalizados y sin normalizar

3. **Bernoulli Matrix Factorization**  
   - Modelo probabilístico que binariza las valoraciones (por ejemplo, likes/dislikes)  
   - Adaptado al Jester dataset mediante umbrales de satisfacción  
   - Implementación optimizada con NumPy

4. **Neural Collaborative Filtering (NCF)**  
   - Modelo basado en redes neuronales profundas  
   - Combina Generalized Matrix Factorization (GMF) y Multi-Layer Perceptrons (MLP)  
   - Entrenado con PyTorch/Keras y optimizado mediante Adam  
   - Mejora la capacidad del modelo para capturar interacciones no lineales complejas

## ⚙️ Evaluación y métricas

Las técnicas se evaluaron con las siguientes métricas:

- **MAE (Mean Absolute Error)**

También se comparó el rendimiento frente a una línea base simple: la media global de puntuaciones.

## 📈 Análisis

- Se incluyó un estudio sobre el impacto de los hiperparámetros (como el número de factores latentes o la profundidad de la red neuronal) en el rendimiento de los modelos.
- Las gráficas muestran la evolución de la pérdida, la precisión y otras métricas durante el entrenamiento.
- Se discuten ventajas, limitaciones y posibles aplicaciones de cada enfoque.


