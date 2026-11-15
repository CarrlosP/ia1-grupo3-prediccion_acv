# Predicción Temprana de Riesgo de Accidentes Cerebrovasculares (ACV)

**Curso:** Inteligencia Artificial 1 — Grupo C2 (2026-2) | Universidad Industrial de Santander (UIS)  
**Equipo:** Grupo 3 
**Integrantes:**
* Carlos Pimienta
* Nelson Torres
* Juan Hernandez

---

## 🎥 Video Resumen Ejecutivo (Máx. 5 minutos)
* **Enlace al video:** [Ver presentación ejecutiva del proyecto]({PEGA_AQUI_EL_ENLACE_DE_YOUTUBE_O_DRIVE})

---

## 📂 Estructura del Repositorio
* `prediccion_acv_proyecto_final.ipynb`: Notebook principal que integra de forma secuencial las tres etapas del proyecto anotadas mediante celdas de Markdown:
  1. **Análisis Exploratorio de Datos (EDA):** Inspección estadística, análisis de asimetría, valores faltantes y desbalance de clases ($95.13\%$ vs. $4.87\%$).
  2. **Aprendizaje Supervisado:** Partición estratificada $80/20$, validación cruzada de $5$ pliegues, comparación de $5$ familias de algoritmos, optimización con `GridSearchCV` (modelo campeón: *Random Forest* con `max_depth=4`, `class_weight='balanced'`, Recall en Test $= 82.0\%$) y auditoría clínica de Falsos Negativos.
  3. **Aprendizaje No Supervisado y Reducción de Dimensionalidad:** Análisis de varianza acumulada mediante *PCA* ($10$ componentes para $\ge 85\%$ de varianza), comparación supervisada con vs. sin reducción dimensional y segmentación poblacional mediante *K-Means* ($k=3$) y agrupamiento jerárquico (*Ward*).

---

## 📊 Origen y Obtención de los Datos
* **Dataset:** *Healthcare Dataset Stroke Data* ($5,110$ registros iniciales, $12$ atributos clínicos y demográficos).
* **Ubicación y descarga:**
  * Archivo CSV procesado directamente en el notebook desde el repositorio público del proyecto:  
    `https://raw.githubusercontent.com/CarrlosP/Proyect_IA/refs/heads/main/healthcare-dataset-stroke-data.csv`
  * Fuente original en Kaggle: [Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset).
* **Instrucciones de ejecución:** Abrir `prediccion_acv_proyecto_final.ipynb` en Google Colab y ejecutar todas las celdas secuencialmente (`Entorno de ejecución -> Ejecutar todas`); el código descarga y preprocesa automáticamente los datos sin requerir configuración manual adicional.
