

##  Resumen del Problema
El objetivo es clasificar si un usuario comprará un producto (variable `Purchased`) analizando su **Edad**, **Género** y **Salario Estimado**. Este análisis es vital y puede ser utilizado en campañas de marketing digital y dirigir anuncios a los segmentos con mayor probabilidad de conversión de compra.

Es prácticamente un problema de **Clasificación Binaria** (0: No compra, 1: Sí compra).

---

##  Metodología

### 1. Análisis Exploratorio de Datos (EDA)
Se realizó una inspección inicial para entender la distribución de los datos y la relación entre variables. Las técnicas utilizadas incluyen:
* **Descripción estadística:** Uso de medidas de tendencia central y dispersión.
* **Matriz de Correlación:** Para identificar qué variables influyen más en la decisión de compra.
* **Visualización Avanzada:** Se añadieron gráficos para robustecer el análisis inicial:
    * **Balance de Clases:** Un gráfico de barras para confirmar si el dataset está equilibrado.
    * **Boxplots:** Implementados para detectar valores atípicos (outliers) y comparar cómo varían la Edad y el Salario entre compradores y no compradores.



### 2. Preprocesamiento
Para asegurar un entrenamiento óptimo, se aplicaron las siguientes transformaciones:
* **Limpieza:** Eliminación de la columna `User ID` por no aportar valor predictivo.
* **Codificación:** Transformación de la variable categórica `Gender` a formato numérico (0 y 1).
* **División de Datos:** Separación en conjuntos de entrenamiento (**80%**) y prueba (**20%**).
* **Escalado de Variables:** Uso de `StandardScaler` para normalizar las escalas de Edad y Salario, evitando que una variable domine sobre la otra por su magnitud.

### 3. Modelado y Evaluación
Se compararon tres algoritmos fundamentales:
1.  **Regresión Logística:** Como modelo base de clasificación lineal.
2.  **Máquinas de Soporte Vectorial (SVM):** Para capturar fronteras de decisión más complejas.
3.  **Árboles de Decisión:** Para un enfoque basado en reglas lógicas.