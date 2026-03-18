# Tema 8: Técnicas de Analítica de Datos (Descriptiva, Predictiva y Machine Learning)
1. El equipo de analítica de la CGR quiere agrupar a los 50.000 contratistas del Estado en 4 "perfiles de riesgo" según su comportamiento histórico (cantidad de multas, retrasos, varianza presupuestal). No se tiene una etiqueta previa de quién es fraudulento y quién no. ¿Qué técnica de Machine Learning es la adecuada para este problema?

A) Un modelo Supervisado de Regresión Lineal.

B) Un modelo No Supervisado de Clustering o Agrupamiento (como K-Means o DBSCAN) para descubrir agrupaciones naturales basadas en la similitud de sus variables.

C) Un algoritmo de Análisis de Sentimientos basado en texto.

D) Un modelo de Clasificación Binaria (Árbol de Decisión).

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> Cuando no tenemos una variable objetivo ("target" o etiqueta predefinida), usamos aprendizaje No Supervisado. El clustering evalúa las distancias matemáticas entre los datos y los agrupa por características similares, ideal para perfilamiento de riesgos exploratorio.
</details>

2. Al entrenar un modelo para predecir si un proyecto de infraestructura tendrá sobrecostos graves (Sí/No), el Científico de Datos nota que en los datos de entrenamiento introdujo la variable "Fecha de Liquidación Final". ¿Por qué esto es un error crítico conocido como "Data Leakage" (Fuga de Datos)?

A) Porque las fechas no pueden usarse en Machine Learning, solo los números.

B) Porque la variable incluye información del futuro (el proyecto solo se liquida cuando ya terminó). El modelo debe predecir el riesgo en la fase de planeación/adjudicación, usando solo la información que estaría disponible en ese momento.

C) Porque la fecha está en formato de Estados Unidos (Mes/Día/Año).

D) No es un error, cuantas más variables tenga el modelo, mejor será la predicción.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> El Data Leakage ocurre cuando usamos información para entrenar el modelo que, en la realidad, no conoceríamos al momento de hacer la predicción. Esto crea un modelo con una precisión engañosamente alta (casi 100%) que fracasará rotundamente en la vida real.
</details>

3. Se aplica un modelo de Clasificación (Regresión Logística) para detectar carteles de licitación. El modelo arroja una "Exactitud" (Accuracy) del 99%. Sin embargo, al revisar, el modelo clasificó absolutamente todas las licitaciones como "Sin Cartel" (Normales). Como los carteles representan el 1% de los casos reales, el modelo acertó en el 99%. ¿Qué métrica se debió usar en este caso de "Datos Desbalanceados"?

A) Precisión, Exhaustividad (Recall) o F1-Score, enfocándose en la capacidad del modelo para detectar correctamente la clase minoritaria (los fraudes).

B) Aumentar el margen de error estadístico.

C) Usar la moda estadística poblacional.

D) El Accuracy del 99% es perfecto y el modelo está listo para producción.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> En fraude, terrorismo o enfermedades raras (datos extremadamente desbalanceados), el Accuracy es inútil porque predecir "todo es normal" da una puntuación alta matemática. El Recall mide cuántos de los fraudes reales el modelo logró capturar, que es lo que realmente le importa a la Contraloría.
</details>

4. Durante la fase de "Análisis Exploratorio de Datos" (EDA) de la facturación de un hospital, el analista encuentra que el valor de un acetaminofén está registrado por $15.000.000 de pesos. Estadísticamente, esto es un:

A) Parámetro de tendencia central.

B) Valor atípico (Outlier). Desde el enfoque de control fiscal, no debe eliminarse de la base, sino separarse para iniciar una auditoría forense inmediata por presunto peculado o error de digitación sistemático.

C) Valor nulo (Missing value).

D) Sesgo de confirmación positivo.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> Los valores atípicos (outliers) son puntos de datos que difieren significativamente de las observaciones restantes. En estadística tradicional suelen eliminarse para no sesgar el modelo, pero en auditoría analítica, el outlier es a menudo la evidencia del fraude (la anomalía es el hallazgo).
</details>

5. El director pide calcular el "Salario Promedio" de una entidad pequeña. Hay 10 empleados que ganan $2.000.000 y el Gerente gana $50.000.000. Si usamos la "Media" (Promedio aritmético), dirá que en promedio ganan $6.360.000, lo cual no representa la realidad de la mayoría. ¿Qué medida de analítica descriptiva es robusta ante estos valores extremos?

A) La Desviación Estándar.

B) La Varianza absoluta.

C) La Mediana, porque divide la distribución exactamente por la mitad (el 50% de los datos está por debajo y el 50% por encima) y no se ve afectada por valores atípicos (outliers).

D) El Rango Intercuartílico (IQR).

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> La media es muy sensible a los extremos. La mediana es una medida de tendencia central "robusta". Al ordenar los sueldos, el valor central representará de manera mucho más fiel el salario típico de los trabajadores de esa entidad, aislando el efecto del salario desproporcionado del gerente.
</details>

6. Para predecir el valor monetario futuro exacto (ej. sobrecosto en millones de pesos) de una obra con base en sus dimensiones geométricas, tiempo de ejecución y materiales, el modelo de Machine Learning apropiado debe ser de tipo:

A) Clasificación (Classification).

B) Regresión (Regression), como Regresión Lineal Múltiple o Gradient Boosting Regressor, dado que la variable objetivo es un número continuo.

C) Agrupamiento (Clustering).

D) Reducción de dimensionalidad (PCA).

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> En Machine Learning Supervisado, si queremos predecir una categoría (ej. Fraude: Sí/No) usamos modelos de Clasificación. Si queremos predecir un valor numérico infinito o continuo (ej. precio, costo, temperatura), usamos modelos de Regresión.
</details>

7. Un modelo de Árbol de Decisión se entrenó para encontrar contratos direccionados. Al evaluarlo con los datos con los que aprendió (Train Data), acierta el 100%. Pero cuando se le presentan contratos nuevos que nunca ha visto (Test Data), su precisión cae al 45%. ¿Qué fenómeno de analítica de datos acaba de ocurrir?

A) Subajuste (Underfitting); el modelo es demasiado simple.

B) Sobreajuste (Overfitting); el modelo memorizó los datos de entrenamiento en lugar de aprender los patrones generales, perdiendo su capacidad de generalización.

C) Fuga de datos (Data Leakage).

D) Convergencia de los hiperparámetros.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> El overfitting ocurre cuando el algoritmo es tan complejo que "memoriza el ruido" de la muestra de entrenamiento. Para solucionarlo, se aplican técnicas de regularización (ej. limitar la profundidad del árbol) o se usan métodos de ensamble (Random Forest).
</details>

8. En analítica avanzada, la técnica de Procesamiento de Lenguaje Natural (NLP - Natural Language Processing) se utiliza en la Contraloría principalmente para:

A) Calcular la tasa de depreciación de los vehículos.

B) Ordenar alfabéticamente los nombres de los alcaldes.

C) Analizar e interpretar automáticamente miles de folios de texto no estructurado (como observaciones en minutas, objetos de contratos, y quejas ciudadanas) para extraer entidades nombradas, tópicos o sentimientos sin intervención humana manual.

D) Comprimir imágenes de alta resolución a formato PDF.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> El NLP (una rama de la IA) permite a las computadoras entender el lenguaje humano. Técnicas como Topic Modeling o extracción de entidades (NER) son fundamentales para minar textos de contratos o audios transcritos y hallar redes de corrupción ocultas en el lenguaje.
</details>

9. Al preparar una base de datos de contratistas, el Científico de Datos nota que la variable "Tipo de Empresa" contiene texto: "SAS", "Ltda", "SA". Los algoritmos matemáticos no entienden texto. ¿Qué técnica debe aplicar para transformar estos datos categóricos a formato numérico sin asumir un orden jerárquico inexistente?

A) One-Hot Encoding (Variables Dummys), creando una columna binaria (0/1) para cada tipo de empresa.

B) Asignarles los números 1, 2 y 3 (Label Encoding), lo que hará que el algoritmo crea que una SA vale el triple que una SAS.

C) Eliminar la columna porque el texto no sirve para analítica predictiva.

D) Encriptar las palabras con protocolo SHA-256.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> El One-Hot Encoding es la técnica estándar para variables categóricas nominales (sin orden intrínseco). Crea nuevas columnas donde la presencia del atributo se marca con 1 y la ausencia con 0, permitiendo que la matemática matricial del algoritmo funcione correctamente.
</details>

10. Para evaluar si la inversión en un programa de seguridad ciudadana realmente redujo el índice de criminalidad, un estadístico encuentra una alta correlación inversa (cuando la inversión sube, el crimen baja). ¿Es suficiente esta correlación matemática para que la CGR dictamine que el programa fue un éxito causal?

A) Sí, en estadística pura, la correlación es sinónimo exacto de causalidad empírica.

B) No. "Correlación no implica causalidad". Podrían existir variables de confusión (ej. cambios en la ley, desempleo, otra política pública paralela) que realmente causaron la reducción. Se requieren modelos de inferencia causal o grupos de control.

C) Sí, siempre y cuando el coeficiente de correlación de Pearson sea superior a 0.5.

D) No, porque los delitos no se pueden medir en términos financieros.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> Un concepto pilar de la analítica es que dos fenómenos que ocurren al mismo tiempo (correlación) no significan que uno cause el otro (causalidad). En evaluación de políticas públicas, para probar impacto, se usan diseños cuasiexperimentales (como Diferencias en Diferencias o Propensity Score Matching).
</details>

11. Tienes un dataset con 2.000 columnas (variables) relacionadas con las finanzas territoriales. Entrenar un modelo con tantas variables es computacionalmente inviable e introduce ruido. ¿Qué técnica No Supervisada utilizarías para reducir el número de variables reteniendo la mayor parte de la información (varianza) original?

A) Borrar aleatoriamente el 80% de las columnas.

B) Análisis de Componentes Principales (PCA).

C) Regresión Logística Múltiple.

D) Limpieza por imputación de la media.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> El Análisis de Componentes Principales (PCA) es una técnica matemática de reducción de dimensionalidad. Transforma cientos de variables correlacionadas en un número menor de variables nuevas incorrelacionadas (componentes principales) que retienen la máxima varianza de los datos originales.
</details>

12. En la validación de un modelo de Machine Learning, el enfoque de "Validación Cruzada de K-Pliegues" (K-Fold Cross Validation) consiste en:

A) Dividir el dataset aleatoriamente en K subconjuntos, entrenar el modelo K veces (usando cada vez un subconjunto distinto para validar y el resto para entrenar) y promediar los resultados para asegurar que el modelo no dependa de cómo se partió la data.

B) Validar que el modelo fue entrenado en computadores cruzados en red.

C) Evaluar el modelo usando exclusivamente la validación de los auditores externos.

D) Dividir los datos en K partes y borrar la parte más pequeña para limpiar ruido.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> La validación cruzada es crucial para garantizar que el rendimiento del modelo sea robusto y generalizable. Al iterar la división de entrenamiento/prueba múltiples veces, se descarta que el modelo sea bueno por simple "suerte" en la partición inicial de los datos.
</details>

13. El equipo de control interno de la CGR detecta que un modelo de IA implementado hace dos años para calcular el riesgo de los contratos ahora está fallando y emitiendo falsas alarmas. Los expertos determinan que hubo "Data Drift" (Deriva de los datos). Esto significa que:

A) Los hackers alteraron el código base de la IA.

B) La estructura o comportamiento subyacente de la realidad cambió (ej. una nueva ley de contratación o inflación post-pandemia) haciendo que los datos actuales tengan una distribución estadística distinta a los datos con los que el modelo aprendió en el pasado. Se requiere reentrenamiento.

C) El disco duro del servidor se desalineó magnéticamente.

D) El modelo procesó datos en un idioma distinto al programado.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> Los modelos de IA no son eternos. El Data Drift (o Concept Drift) es el fenómeno donde la realidad cambia (nuevas regulaciones, crisis económicas) y las reglas que el modelo aprendió en el pasado ya no aplican. El ciclo de vida de ML exige monitoreo y reentrenamiento continuo (MLOps).
</details>

14. A partir de una tabla de pagos que solo contiene "Identificación" y "Fecha de pago", el científico de datos programa código para crear nuevas columnas como: "Días desde el último pago", "Promedio pagado en los últimos 3 meses" y "¿Es fin de mes?". Este proceso crítico en analítica predictiva se denomina:

A) Minería de texto.

B) Scraping de datos.

C) Ingeniería de Características (Feature Engineering), que busca extraer información oculta y conocimiento de negocio a partir de variables crudas para ayudar al algoritmo a encontrar patrones complejos.

D) Falsificación de datos administrativos.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> El Feature Engineering es el arte de crear variables nuevas y más predictivas combinando o transformando los datos originales. Un buen algoritmo con malas variables falla; un algoritmo simple con excelente ingeniería de características suele ganar competiciones y hallar fraudes.
</details>

15. Un analista está revisando datos de contratación estatal para analítica descriptiva. Encuentra que el 15% de los registros en la columna "Fecha de Nacimiento del Representante Legal" están en blanco. Si elimina esas filas completas, perderá el 15% del presupuesto evaluado. ¿Cuál es la técnica analítica recomendada?

A) Reemplazar todos los blancos con la fecha del día de la auditoría.

B) Imputación de datos (Data Imputation), que puede ser usando la mediana/moda de edades, creando un modelo predictivo para estimar la edad faltante, o si no es crítica, simplemente asignar un valor de "Desconocido" sin perder la fila del contrato.

C) Eliminar los registros de todos modos porque los datos vacíos rompen las bases SQL.

D) Borrar toda la columna de fecha de nacimiento y también la cédula por si acaso.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> La eliminación de registros con datos faltantes (Listwise deletion) es el último recurso porque se pierde información valiosa (el valor del contrato, el objeto). La imputación permite salvar el registro utilizando técnicas estadísticas que estiman el valor faltante minimizando el sesgo.
</details>