# 🌳 Laboratorio: Entrenamiento y Evaluación de Modelos de Clasificación (Decision Trees)
## Escuela Colombiana de Ingeniería Julio Garavito
## Juan David Zambrano Gonzalez

## 📘 Descripción general

Este proyecto tiene como objetivo **entrenar, evaluar y comparar modelos de clasificación supervisada** utilizando el conjunto de datos **Adult Census Income (adult.data)**.  
Se busca determinar si una persona gana más o menos de 50K al año en función de características socioeconómicas, aplicando **Árboles de Decisión**, **Bosques Aleatorios (Random Forest)** y **Gradient Boosting**.

El laboratorio forma parte de las prácticas de aprendizaje automático y se enfoca en la comprensión de los procesos de **entrenamiento, validación, prueba y evaluación de desempeño** mediante métricas como **F1-score** y **exactitud (accuracy)**.

---

## 🔍 Dataset

El **dataset Adult** proviene de la base de datos del *Census Bureau* y contiene información sobre edad, nivel educativo, ocupación, estado civil, horas trabajadas, entre otras variables.

**Objetivo:** predecir si una persona tiene un ingreso `>50K` o `<=50K`.

**Cantidad de registros:**
- Entrenamiento: 80%
- Prueba: 20%

**Número de atributos:** 14 características (numéricas y categóricas).

---

## 🧠 Modelos implementados

### 1. Árbol de Decisión (Decision Tree)
- Criterio: `entropy`
- Profundidad máxima: `10`
- Métrica: **F1-score = 0.654**

Permite observar la estructura jerárquica de decisiones y entender cómo se dividen los datos según su ganancia de información.

---

### 2. Bosque Aleatorio (Random Forest)
- Número de árboles: `100`
- Criterio: `entropy`
- Métrica: **F1-score = 0.676**

Reduce la varianza respecto al árbol simple y mejora la generalización combinando múltiples árboles de decisión.

---

### 3. Gradient Boosting
- Número de estimadores: `100`
- Tasa de aprendizaje: `0.1`
- Profundidad máxima: `3`
- Métrica: **F1-score = 0.689**

Este modelo mostró el **mejor desempeño** en la validación y prueba, alcanzando una precisión promedio del **87%**. Combina árboles de decisión débiles que se ajustan progresivamente a los errores de los anteriores.

---

## 🧩 Metodología

1. **Preprocesamiento de datos**
   - Manejo de valores faltantes.
   - Codificación de variables categóricas con `OneHotEncoder`.
   - Normalización de variables numéricas con `StandardScaler`.

2. **División de datos**
   - 80% entrenamiento / 20% prueba.
   - Se utilizó un conjunto de **validación** adicional para seleccionar el mejor modelo.

3. **Entrenamiento de modelos**
   - Implementación de los tres modelos en `scikit-learn`.
   - Ajuste de hiperparámetros básicos.

4. **Evaluación**
   - Métricas: F1-score, precisión, recall y accuracy.
   - Comparación de desempeño entre modelos.
   - Selección del modelo con mejor F1-score (Gradient Boosting).

---

## 📈 Resultados comparativos

| Modelo              | Accuracy | F1-score | Observaciones                            |
|---------------------|-----------|-----------|-------------------------------------------|
| Árbol de Decisión   | 0.85      | 0.654     | Más interpretable, pero mayor varianza.   |
| Bosque Aleatorio    | 0.86      | 0.676     | Mejor generalización y menor sobreajuste. |
| Gradient Boosting   | 0.87      | 0.689     | Mejor desempeño global. Modelo elegido.   |

---

## 🧾 Conclusiones

- El modelo **Gradient Boosting** fue el más preciso, mostrando mejor equilibrio entre sesgo y varianza.
- El **Árbol de Decisión** sirvió como base conceptual para entender los demás modelos.
- El **Bosque Aleatorio** mejoró la estabilidad de las predicciones, pero no superó al boosting en F1.
- Se confirma que los métodos de *ensemble* logran una mayor capacidad predictiva en problemas de clasificación con datos heterogéneos.

---

## 👥 Equipo de trabajo

- Juan David Zambrano  

**Tiempo total invertido:** 7 horas  
**Estado del laboratorio:** Completo ✅

---

## 📚 Referencias

- Scikit-learn Developers. (2024). *Scikit-learn Documentation*. https://scikit-learn.org/stable/  
- Géron, A. (2022). *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (3rd ed.). O'Reilly Media.  
- IBM. (2023). *Decision Trees and Ensemble Methods in Machine Learning*. IBM Developer. https://developer.ibm.com/

---

## 💡 Licencia

Este proyecto se distribuye bajo la licencia **MIT**. Puedes usar, modificar o compartir el código con fines educativos y de investigación.
