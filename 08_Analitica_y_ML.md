# Cuestionario: Analítica Descriptiva, Predictiva y Machine Learning (20 preguntas)

> **Instrucciones:** Lee cada pregunta y despliega la respuesta solo cuando quieras verificarla. 
> Haz clic en **Mostrar respuesta** para revelar la solución y una breve explicación.

---

### 1. La analítica **descriptiva** busca…

- Predecir el futuro
- Entender qué ocurrió mediante resúmenes y visualizaciones
- Optimizar decisiones en tiempo real
- Simular escenarios

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Describe el pasado con KPIs y resúmenes.

</details>

### 2. La analítica **predictiva**…

- Explica causas
- Estima resultados futuros usando modelos estadísticos o ML
- Es solo descriptiva
- No usa datos históricos

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Usa patrones para pronosticar.

</details>

### 3. En ML supervisado, la **variable objetivo**…

- No existe
- Es la que se intenta predecir (y se conoce en entrenamiento)
- Es cualquier predictor
- Es siempre numérica

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** También llamada label.

</details>

### 4. Un ejemplo de modelo supervisado es…

- K-means
- Regresión logística
- Análisis de componentes principales
- Clustering jerárquico

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Clasificación binaria multiclase.

</details>

### 5. Un ejemplo de modelo no supervisado es…

- Árbol de decisión
- SVM
- K-means
- Regresión lineal

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** C

**Explicación:** Agrupa observaciones por similitud.

</details>

### 6. El **overfitting** ocurre cuando…

- El modelo generaliza bien
- El modelo aprende ruido del entrenamiento y falla en datos nuevos
- No aprende nada
- Los datos están balanceados

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Se mitiga con validación, regularización y más datos.

</details>

### 7. La **validación cruzada** sirve para…

- Reducir el tamaño del dataset
- Evaluar desempeño con particiones repetidas para estimar generalización
- Mejorar visualización
- Seleccionar variables automáticamente

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** K-fold es un esquema común.

</details>

### 8. Una métrica para clasificación binaria es…

- RMSE
- MAE
- Exactitud (accuracy), precisión, recall, F1
- R-cuadrado

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** C

**Explicación:** Para regresión se usa RMSE/MAE; para clasificación, F1 y otras.

</details>

### 9. El **AUC-ROC** mide…

- Error cuadrático
- Capacidad de separar clases a distintos umbrales
- Número de variables
- Relación señal/ruido

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Área bajo la curva ROC (TPR vs FPR).

</details>

### 10. La **regularización L2** (Ridge)…

- No afecta pesos
- Penaliza la suma de cuadrados de los coeficientes para reducir varianza
- Elimina variables automáticamente
- Siempre es peor que L1

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Controla complejidad del modelo.

</details>

### 11. La selección de características ayuda a…

- Aumentar overfitting
- Mejorar interpretabilidad y rendimiento
- Eliminar información clave siempre
- Duplicar columnas

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Reduce dimensionalidad y ruido.

</details>

### 12. El **pipeline** de ML incluye…

- Sólo modelado
- Ingesta → limpieza/transformación → partición → entrenamiento → validación → despliegue → monitoreo
- Presentación
- Visualización

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Ciclo de vida completo del modelo.

</details>

### 13. En problemas desbalanceados conviene…

- Ignorar el desbalance
- Ajustar umbral, usar métricas como AUC/PR, técnicas de re-muestreo
- Solo medir accuracy
- Eliminar la clase minoritaria

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Mejor evaluación y tratamiento del desbalance.

</details>

### 14. **PCA** se usa para…

- Clasificación binaria
- Reducir dimensionalidad preservando varianza
- Imputar valores faltantes
- Detectar outliers exclusivamente

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Componentes principales ortogonales.

</details>

### 15. Un conjunto de entrenamiento y prueba…

- Deben solaparse
- Deben ser disjuntos para evaluar generalización
- Deben ser idénticos
- No importa

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Evita fuga de información.

</details>

### 16. El **learning rate** en modelos de gradiente…

- No afecta
- Controla el tamaño del paso en la optimización; muy alto diverge, muy bajo lentifica
- Es número de épocas
- Define tamaño de lote

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Hiperparámetro crítico en entrenamiento.

</details>

### 17. **Random Forest** es…

- Un único árbol
- Un ensamble de árboles entrenados sobre muestras y subconjuntos de variables
- Regresión lineal
- K-means

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Reduce varianza y mejora generalización.

</details>

### 18. La **explicabilidad** de modelos busca…

- Ocultar criterios
- Entender contribuciones (feature importance, SHAP) para decisiones transparentes
- Optimizar velocidad únicamente
- Eliminar variables

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Clave en sector público y auditorías.

</details>

### 19. El **drift** de datos/modelo…

- Significa estabilidad
- Es el cambio en distribución de datos o relación entrada-salida que degrada el desempeño
- Mejora el AUC
- No existe

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Requiere monitoreo y recalibración.

</details>

### 20. Una métrica de error en regresión es…

- F1
- MAE o RMSE
- AUC
- Recall

<details><summary><strong>Mostrar respuesta</strong></summary>

**Respuesta correcta:** B

**Explicación:** Miden desviación promedio del valor real.

</details>
