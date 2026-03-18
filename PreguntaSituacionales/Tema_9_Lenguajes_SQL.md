# Tema 9: Conocimiento en Lenguajes de Programación y Consultas (SQL, Python, etc.)
1. Un auditor necesita extraer del sistema transaccional (base de datos relacional) todos los contratistas cuyo monto total sumado de contratos en el año supere los $500 millones. ¿Qué cláusula SQL es la correcta para filtrar este resultado después de agrupar por contratista?

A) WHERE SUM(monto) > 500000000

B) GROUP BY contratista HAVING SUM(monto) > 500000000

C) FILTER (monto > 500000000) GROUP BY contratista

D) ORDER BY monto > 500000000

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> En SQL, la cláusula WHERE filtra filas individuales antes de agrupar. Para filtrar resultados basados en una función de agregación (como SUM, COUNT o AVG), se debe utilizar obligatoriamente la cláusula HAVING después del GROUP BY.
</details>

2. Al desarrollar un script en Python utilizando la librería pandas para analizar un archivo CSV del SECOP con 10 millones de filas, el código arroja un error "MemoryError" y el computador se bloquea. ¿Cuál es la mejor práctica de programación para resolver esto sin cambiar de equipo?

A) Procesar el archivo por fragmentos (utilizando el parámetro chunksize en pd.read_csv) o cambiar los tipos de datos (ej. de float64 a float32 o category) para reducir el consumo de memoria RAM.

B) Convertir el CSV a formato PDF antes de leerlo.

C) Usar un bucle for tradicional de Python para leer el archivo línea por línea e imprimir el resultado en pantalla.

D) Dividir el archivo en 100 archivos pequeños de Excel manualmente usando el ratón.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> Pandas carga todo el dataset en la memoria RAM por defecto. Para Big Data, la técnica de Chunking (leer por trozos) y la optimización de los dtypes (tipos de datos) son fundamentales para procesar archivos que superan la capacidad física de la memoria del sistema.
</details>

3. Se requiere un reporte SQL que muestre la lista de todas las entidades territoriales, y a su lado, la cantidad de reportes fiscales que han enviado. Si una entidad no ha enviado ningún reporte, debe aparecer en la lista con un "0" o "NULL", pero no debe desaparecer. ¿Qué tipo de JOIN (unión) garantiza este resultado?

A) INNER JOIN

B) CROSS JOIN

C) LEFT JOIN (o RIGHT JOIN), tomando como tabla principal (izquierda) el catálogo maestro de entidades territoriales.

D) FULL OUTER JOIN

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> Un INNER JOIN solo trae los registros que coinciden en ambas tablas (desaparecería a las entidades sin reportes). Un LEFT JOIN trae todos los registros de la tabla de la izquierda (entidades) y los cruza con los de la derecha, poniendo NULL donde no hay coincidencia.
</details>

4. Dentro de una consulta SQL, el analista descubre que en la tabla de facturas la fecha está guardada como texto (VARCHAR) en formato 'DD/MM/YYYY'. Al usar la cláusula ORDER BY fecha_texto DESC, el mes de diciembre ('12/01/2023') aparece antes que febrero ('02/02/2024'). ¿Cómo se corrige este problema lógico?

A) Eliminando los registros del año 2023.

B) Aplicando una función de casteo o conversión (como CAST(fecha_texto AS DATE) o TO_DATE()) antes de realizar el ordenamiento.

C) Ordenando primero por el nombre del contratista.

D) Exportando a Excel para ordenar manualmente porque SQL no puede ordenar textos.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> Si una fecha está almacenada como texto, SQL la ordena alfabéticamente (el "1" de 12 es menor que el "0" de 02). Se debe convertir el tipo de dato explícitamente a formato DATE para que el motor entienda la cronología real.
</details>

5. En Python, tienes un DataFrame de pagos con un millón de filas. Necesitas crear una nueva columna que multiplique el valor del contrato por el impuesto. Un practicante escribe un bucle for que itera sobre cada fila con iterrows(), pero tarda 30 minutos en ejecutar. ¿Cómo optimizas este cálculo?

A) Utilizando operaciones vectorizadas directas de pandas (ej. df['total'] = df['valor'] * df['impuesto']), lo cual se ejecuta en milisegundos al estar optimizado en lenguaje C por debajo.

B) Poniendo un comando time.sleep(1) para que el procesador descanse.

C) Dividiendo el cálculo en dos bucles for distintos.

D) Guardando el archivo y haciendo el cálculo en la calculadora de Windows.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> En ciencia de datos con Python (pandas/NumPy), la regla de oro es evitar bucles for y métodos iterativos como apply() o iterrows() siempre que sea posible, utilizando la "vectorización" que procesa matrices enteras simultáneamente con altísimo rendimiento.
</details>

6. Al revisar una base de datos relacional de contratos, el analista necesita encontrar el contrato más reciente firmado por cada proveedor. ¿Qué función analítica avanzada de SQL permite numerar y rankear los contratos de cada proveedor cronológicamente sin agrupar y perder el detalle?

A) Funciones de Ventana (Window Functions) como ROW_NUMBER() OVER(PARTITION BY proveedor_id ORDER BY fecha DESC).

B) Usando simplemente un SELECT DISTINCT proveedor_id.

C) Haciendo un CROSS APPLY con la tabla de tiempos.

D) Es imposible hacerlo en una sola consulta SQL, se requiere un script en Java.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> Las Window Functions (ROW_NUMBER, RANK) son herramientas avanzadas en SQL. La partición (PARTITION BY) crea "ventanas" de datos por proveedor, y el ordenamiento (ORDER BY) enumera internamente los registros (1, 2, 3...) permitiendo filtrar solo el registro número 1 (el más reciente).
</details>

7. Un script en Python encargado de raspar (Web Scraping) el portal de contratación pública para buscar anomalías a veces falla de madrugada porque el servidor del portal se cae, lo que interrumpe todo el proceso. ¿Qué estructura de control de Python debe usarse para manejar este error sin que el programa se cierre abruptamente?

A) Una condicional if / else comprobando la memoria RAM.

B) Una función matemática de valor absoluto.

C) Bloques de manejo de excepciones try / except, que permiten al código "intentar" la conexión y, si falla, ejecutar una acción alternativa (como esperar 5 minutos y reintentar) en lugar de colapsar.

D) Un bucle infinito while True sin interrupción.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> El manejo de excepciones (try/except en Python) es fundamental en la automatización y extracción de datos. Permite capturar errores externos (como caídas de red, timeouts o datos faltantes) y gestionarlos de forma elegante para mantener la resiliencia del pipeline de datos.
</details>

8. En una consulta SQL, se utiliza el comodín LIKE '%construcción%'. ¿Cuál es el riesgo de rendimiento asociado con esta instrucción en una tabla con millones de registros?

A) Que el motor de base de datos borre accidentalmente las filas.

B) Ninguno, LIKE es la operación más rápida en SQL.

C) Que traducirá los textos al idioma inglés.

D) El uso del comodín % al principio de la cadena inhabilita el uso de índices de búsqueda (Full Table Scan), obligando al motor a leer secuencialmente cada fila de la tabla, lo que degrada críticamente el rendimiento.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: D</b>.


<i>Justificación:</i> Cuando se busca un texto que contiene una palabra en el medio (%texto%), el motor SQL no puede usar el índice estructurado (B-Tree). En analítica fiscal masiva, esto se soluciona usando índices Full-Text Search o bases de datos noSQL especializadas en texto.
</details>

9. Estás escribiendo un script de Python para limpiar una columna llamada "Valor_Contrato" que viene del SECOP. Los datos vienen con el símbolo de peso y puntos de miles (ej. "$ 1.500.000"). Para poder sumar estos valores matemáticamente, la instrucción correcta utilizando pandas (asumiendo df como el dataframe) es:

A) df['Valor_Contrato'] = df['Valor_Contrato'] * 100

B) df['Valor_Contrato'] = df['Valor_Contrato'].str.replace('$', '').str.replace('.', '').astype(float)

C) Dejarlo así, Python suma textos automáticamente.

D) df['Valor_Contrato'].drop_duplicates()

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> Antes de aplicar analítica matemática, los datos financieros deben ser "limpiados". La sintaxis .str.replace() elimina los caracteres especiales de texto (símbolos y puntos delimitadores) y .astype(float) convierte la cadena resultante en un valor numérico continuo (flotante).
</details>

10. La CGR implementa un formulario web interno para que los auditores busquen contratos. El desarrollador inserta el input del auditor directamente en la consulta: SELECT * FROM contratos WHERE id = ' + input + '. Un usuario malintencionado escribe 1' OR '1'='1. ¿Cómo se denomina esta vulnerabilidad crítica?

A) Inyección SQL (SQL Injection), que permite a un atacante manipular la consulta y acceder a información no autorizada. Se previene usando consultas parametrizadas (Prepared Statements).

B) Denegación de servicio distribuido (DDoS).

C) Fuga de memoria (Memory Leak).

D) Error de sintaxis benigno.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> La inyección SQL es la vulnerabilidad número uno en aplicaciones web. Al no sanitizar el input del usuario e inyectarlo en la cadena SQL, el atacante modifica la lógica de la base de datos (la condición OR &#39;1&#39;=&#39;1&#39; siempre es verdadera, devolviendo toda la tabla protegida).
</details>

11. Al hacer un cruce de datos (Merge/Join) entre la tabla de "Nómina" y "Funcionarios" usando como llave la cédula, el resultado final cuadruplica la cantidad de registros esperados. La causa técnica de este error analítico es:

A) Que se usó SQL Server en lugar de Oracle.

B) Que la cédula de algunos funcionarios está duplicada en la tabla destino, generando un producto cartesiano (relación de muchos a muchos) inintencionada.

C) Que se usó un INNER JOIN en lugar de un LEFT JOIN.

D) Que las variables tienen diferente color en el editor de código.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> Si la llave primaria utilizada para hacer el cruce (JOIN o pd.merge()) tiene valores duplicados en ambas tablas, el motor relacional multiplica las combinaciones (producto cartesiano local), inflando artificialmente el presupuesto y los registros. La tabla de dimensiones siempre debe tener llaves únicas.
</details>

12. En análisis de datos con Python, ¿qué utilidad tiene la librería scikit-learn en el entorno del control fiscal y la auditoría predictiva?

A) Se usa para diseñar las interfaces gráficas y botones de las páginas web.

B) Es la herramienta principal para la creación de reportes en PDF y formateo de texto legal.

C) Proporciona los algoritmos estándar de Machine Learning (como Random Forest, K-Means, Regresión) para crear modelos predictivos, detectar anomalías y clasificar riesgos automáticamente.

D) Se utiliza exclusivamente para conectarse a bases de datos en la nube.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> scikit-learn es la biblioteca de aprendizaje automático de código abierto más utilizada en Python. Ofrece herramientas de análisis predictivo simples y eficientes, fundamentales para que los científicos de datos de la CGR desarrollen modelos de detección de fraude.
</details>

13. Tienes una columna de texto "Observaciones" con miles de filas. Quieres extraer únicamente los números de las cuentas bancarias (que siempre tienen 11 dígitos numéricos seguidos) que los supervisores han dejado escritos entre el texto. ¿Qué tecnología de lenguajes de programación es la indicada para esta extracción de patrones?

A) HTML5 semántico.

B) Expresiones Regulares (RegEx), por ejemplo \b\d{11}\b, que permite buscar y extraer patrones específicos de cadenas dentro de texto no estructurado.

C) Funciones aritméticas básicas de Excel.

D) Agrupación por clústeres.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> Las Expresiones Regulares (Regex) son secuencias de caracteres que conforman un patrón de búsqueda. Son indispensables en analítica fiscal para extraer cédulas, números de contrato, correos o cuentas bancarias ocultas dentro de campos largos de texto libre (observaciones/minutas).
</details>

14. Una base de datos almacena los montos de ejecución diaria de una obra. Necesitas calcular el "Valor Acumulado" (Running Total) día tras día para comparar la curva de inversión física vs financiera. ¿Qué función en SQL y en pandas (Python) te permite calcular este acumulado dinámico?

A) En SQL se usa SUM(monto) OVER (ORDER BY fecha) y en pandas la función .cumsum().

B) En SQL se usa MAX(monto) y en pandas .max().

C) En SQL se usa COUNT() y en pandas .value_counts().

D) En SQL se usa DISTINCT y en pandas .unique().

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> El total acumulado (Running Total) es fundamental para analizar curvas de ejecución. En SQL se logra combinando una función de agregación con una cláusula de ventana ordenada. En Python (pandas), la función cumsum() (cumulative sum) realiza la operación vectorizada.
</details>

15. Un script de automatización fiscal ejecuta un procedimiento almacenado (Stored Procedure) que actualiza saldos contables, pero la red se corta a mitad del proceso. ¿Qué mecanismo del motor de base de datos SQL garantiza que no queden saldos a medias (o se actualiza todo o no se actualiza nada)?

A) El uso de índices Clustered.

B) La sentencia TRUNCATE TABLE.

C) El control de Transacciones (propiedades ACID), utilizando sentencias BEGIN TRAN, COMMIT para guardar todo si hay éxito, o ROLLBACK para deshacer todo si ocurre un error a mitad de camino.

D) El comando DROP DATABASE.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> La atomicidad (la 'A' en ACID) garantiza que una transacción de base de datos se trate como una unidad lógica indivisible. Si ocurre un fallo (ej. corte de energía o red), el ROLLBACK automático protege la base de datos de quedar en un estado corrupto o parcialmente actualizado.
</details>