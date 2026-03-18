# Tema 7: Visualización de Datos y Software de Inteligencia de Negocios (BI)
1. Al diseñar un dashboard en Power BI para mostrar el histórico de hallazgos fiscales de los últimos 10 años, el analista decide utilizar un gráfico de torta (pie chart) con 120 porciones (una por cada mes). Durante la presentación, el Contralor indica que no se entiende nada. ¿Cuál es el error técnico y la solución en términos de visualización efectiva?

A) El error es no haberle puesto etiquetas de datos a las 120 porciones. La solución es reducir el tamaño de la fuente.

B) El error es utilizar un gráfico de torta para series de tiempo largas y con demasiadas categorías, rompiendo el principio de legibilidad. La solución es cambiar a un gráfico de líneas o de barras continuas que muestre la tendencia temporal de forma clara.

C) El error es que los colores son muy opacos. La solución es aplicar un degradado 3D a la torta.

D) El error es de la herramienta. Power BI no soporta gráficos de torta con más de 10 variables, por lo que se debe usar Excel.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> En "Storytelling con datos", los gráficos de torta o anillos solo son útiles para mostrar la composición de un todo con muy pocas categorías (máximo 3 a 5). Para series de tiempo (meses/años) y tendencias, el estándar universal es el gráfico de líneas o barras.
</details>

2. En un tablero de control de la CGR, un auditor que vigila el sector "Defensa" se queja de que al abrir el reporte puede ver los contratos confidenciales del sector "Salud", lo cual vulnera las políticas de acceso a la información. En el desarrollo del modelo BI, ¿qué mecanismo se omitió implementar?

A) La instalación de un firewall físico en el computador del auditor.

B) La eliminación manual de los datos de Salud antes de enviarle el reporte por correo.

C) La configuración de RLS (Row-Level Security o Seguridad a Nivel de Fila) en el modelo de datos, que filtra dinámicamente la información según el rol y los permisos del usuario que inicia sesión.

D) El cifrado de extremo a extremo del archivo .pbix con contraseña de WinRAR.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> La Seguridad a Nivel de Fila (RLS) es la característica de las herramientas de BI (como Power BI o Tableau) que permite que un solo modelo o reporte sea compartido por toda la entidad, pero que cada usuario solo vea los datos que su rol o departamento le permite ver.
</details>

3. Un informe interactivo que conecta la base de datos de contratación pública (SECOP) mediante consulta directa (DirectQuery) está tardando más de 5 minutos en cargar cada vez que el auditor hace clic en un filtro, bloqueando la base transaccional. ¿Cuál es la mejor estrategia técnica de BI para resolver este problema?

A) Prohibir a los auditores usar filtros en el tablero.

B) Cambiar el modo de conexión a "Importar" (Import Mode) implementando actualizaciones programadas en horas no pico, o diseñar una tabla de agregaciones que resuma los datos y reduzca la carga sobre la base transaccional.

C) Comprar computadores con mayor memoria RAM para todos los auditores de la CGR.

D) Exportar los 50 millones de registros a un archivo CSV plano y leerlos desde ahí.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> DirectQuery envía consultas SQL al origen por cada interacción, lo que colapsa bases masivas. El modo Importación carga los datos en el motor en memoria (VertiPaq) haciéndolos ultrarrápidos, y las agregaciones permiten tener el detalle sin sacrificar rendimiento.
</details>

4. Al cruzar la tabla de "Contratistas" (10.000 registros) con la tabla de "Pagos" (50.000 registros), el analista nota que el tablero muestra valores "En blanco" (Blank/Null) en el total de pagos de algunos contratistas que sí tienen pagos registrados en el sistema origen. El error se debe a que la cédula en una tabla tiene espacios al final (ej. "12345 "). ¿En qué fase de BI se debió corregir esto?

A) En la fase de Visualización, ocultando los valores en blanco.

B) En la fase de Modelado, creando una relación de Muchos a Muchos.

C) En la fase de ETL (Extracción, Transformación y Carga) usando Power Query o SQL para aplicar funciones de limpieza (Trim/Limpiar) y normalizar las llaves primarias antes de cargarlas al modelo.

D) En el origen, pidiendo al contratista que cambie su número de cédula.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> Los problemas de calidad de datos (como espacios extra, ceros a la izquierda inconsistentes o mayúsculas/minúsculas) rompen las relaciones entre tablas (Joins). Deben solucionarse en el proceso de Transformación (ETL) para garantizar un modelo de datos íntegro.
</details>

5. Se le pide al equipo de BI diseñar un visual que permita identificar rápidamente, entre 1.100 municipios, cuáles concentran el mayor número de obras inconclusas ("Elefantes Blancos") de manera geográfica. ¿Cuál es el elemento visual más idóneo?

A) Un gráfico de dispersión (Scatter plot) con 1.100 puntos.

B) Una tabla matriz (Matrix) ordenada alfabéticamente.

C) Un mapa coroplético (mapa de calor por regiones) donde la intensidad del color dependa de la cantidad de obras inconclusas o su valor en riesgo.

D) Un gráfico de cascada (Waterfall chart).

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> Para representar variables cuantitativas (como cantidad de obras o presupuestos) asociadas a divisiones geográficas o territoriales, el mapa coroplético es la visualización más intuitiva y efectiva para detectar concentraciones espaciales.
</details>

6. El principio de la "Proporción Tinta-Datos" (Data-Ink Ratio) introducido por Edward Tufte en la visualización de datos establece que:

A) Un buen tablero de control debe eliminar cualquier elemento decorativo, bordes innecesarios, fondos recargados o efectos 3D que no aporten información, maximizando la tinta (o pixeles) usada para mostrar los datos reales.

B) Se deben usar al menos 10 colores vibrantes distintos para mantener la atención del espectador.

C) Siempre se debe imprimir el reporte a color antes de presentarlo al Contralor.

D) Las tablas de datos deben tener colores de fondo oscuros con letras claras para parecer más modernas.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> El "Data-Ink Ratio" es un pilar del diseño de tableros de control. Postula que todo elemento visual que no transmita datos (gridlines gruesas, logos gigantes, sombras, gradientes) es "ruido visual" y debe ser minimizado o eliminado para facilitar la interpretación cognitiva.
</details>

7. Un analista crea una métrica (Medida DAX) para calcular el "Crecimiento del detrimento patrimonial respecto al mes anterior". Sin embargo, la fórmula arroja error al aplicarla a diferentes años. ¿Qué elemento estructural del modelo dimensional es indispensable para que las funciones de Inteligencia de Tiempo (Time Intelligence) funcionen correctamente?

A) Una tabla de jerarquía geográfica.

B) Una tabla separada solo para los años bisiestos.

C) Una "Tabla Calendario" (Date Table) dedicada, continua, que cubra todos los años de los datos sin saltos de días y que esté relacionada con la fecha de los hechos.

D) Formatear todas las fechas a formato de texto (String).

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> En modelado tabular (Power BI / Analysis Services), cualquier cálculo comparativo temporal (YTD, MTD, SAMEPERIODLASTYEAR) requiere obligatoriamente una dimensión de Fecha/Calendario continua y marcada como tal en el modelo.
</details>

8. En una tabla que muestra 500 contratos con sus respectivos márgenes de utilidad, el director de auditoría quiere identificar de un solo vistazo cuáles contratos superan el 30% de utilidad (riesgo de sobrecosto) sin tener que leer número por número. La técnica de visualización indicada es:

A) Borrar de la tabla los que tienen menos del 30%.

B) Imprimir la tabla y resaltarlos con un marcador.

C) Aplicar Formato Condicional (Conditional Formatting) a la columna, asignando un color de fondo rojo o un icono de alerta a los valores que superen el umbral del 30%.

D) Cambiar la tabla por un diagrama de Venn.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> El formato condicional es la herramienta de diseño interactivo que permite aplicar atributos preatentivos (color, iconos) a tablas o matrices para resaltar desviaciones, metas u outliers inmediatamente a los ojos del usuario.
</details>

9. Al revisar un tablero, notas que el KPI "Presupuesto Total Ejecutado" muestra la suma de 500.000 millones. Sin embargo, al cruzar la tabla "Presupuesto" y la tabla "Municipios", el valor se duplica a 1 billón porque un presupuesto está asignado a varios municipios a la vez. En inteligencia de negocios, este problema de modelado se conoce como:

A) Una relación de Muchos a Muchos (Many-to-Many) mal resuelta, que requiere una tabla puente (Bridge table) o una asignación porcentual para evitar la duplicación (doble conteo) de la variable cuantitativa.

B) Un error de la base de datos de la Gobernación.

C) Un problema de filtrado cruzado bidireccional que no tiene solución técnica.

D) Una métrica subestimada por falta de decimales.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> El doble conteo es el error más grave y común en modelos dimensionales. Ocurre cuando se relacionan tablas de hechos directamente o hay cardinalidad Muchos a Muchos sin una tabla puente que normalice la granularidad de los datos.
</details>

10. Quieres mostrar cómo está distribuido el presupuesto general de la nación desglosado jerárquicamente: primero por Sectores (Salud, Educación, Defensa), luego dentro de cada sector por Entidades, y finalmente por Programas. ¿Qué tipo de visualización permite explorar esta composición jerárquica de la parte al todo de manera interactiva?

A) Un gráfico de embudo (Funnel chart).

B) Un Mapa de Árbol (Treemap) o una Matriz jerárquica con capacidad de "Drill-down" (profundizar).

C) Un medidor o velocímetro (Gauge).

D) Un gráfico de radar (Spider chart).

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> Los Treemaps utilizan rectángulos anidados (cuyo tamaño es proporcional al valor numérico) para visualizar datos jerárquicos. El drill-down es la capacidad de hacer clic en un sector y descender al nivel de "Entidades" de ese sector específico.
</details>

11. Un analista crea una Columna Calculada en Power BI con una fórmula DAX extremadamente compleja que evalúa 10 millones de filas. Posteriormente, el archivo se vuelve lentísimo de actualizar y pesa el doble. ¿Por qué ocurre esto y cómo se optimiza?

A) Ocurre porque DAX es ineficiente; se soluciona haciendo el cálculo en una calculadora manual.

B) Ocurre porque la conexión a internet es lenta.

C) Ocurre porque las Columnas Calculadas se materializan (ocupan memoria RAM y espacio en disco) durante la actualización. Se debe reemplazar por una "Medida" (Measure), que se calcula al vuelo (en tiempo de consulta) y no ocupa espacio en disco.

D) Ocurre porque la fórmula tiene errores de sintaxis; se soluciona agregando comentarios al código.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> Regla de oro en modelado tabular: usar columnas calculadas solo cuando sea estrictamente necesario (ej. para categorizar un eje). Para cálculos aritméticos, agregaciones o ratios, siempre se deben usar Medidas (Measures) para optimizar el motor VertiPaq.
</details>

12. En una presentación de hallazgos ante la ciudadanía (Control Fiscal Participativo), se utiliza una técnica de "Storytelling" con datos. ¿Cuál es el objetivo principal de esta técnica en el contexto fiscal?

A) Traducir hallazgos técnicos complejos en una narrativa clara, contextualizada y visualmente persuasiva que conduzca a la audiencia a comprender el impacto real del daño patrimonial y la llamada a la acción.

B) Exponer el código fuente (SQL y Python) completo frente al público para demostrar transparencia algorítmica.

C) Ocultar los datos reales bajo historias ficticias para proteger el nombre de los contratistas investigados.

D) Utilizar animaciones y sonidos en cada transición de diapositiva para que la presentación sea entretenida.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> El Data Storytelling busca cerrar la brecha entre el análisis profundo y la audiencia no experta (ciudadanía, periodistas). Usa los datos para contar el "qué", el "por qué" y el "para qué" de manera digerible e impactante, impulsando la toma de decisiones informadas.
</details>

13. Tienes un "Modelo de Estrella" (Star Schema). En el centro tienes la tabla de "Contratos" (Tabla de Hechos) y alrededor tienes "Proveedores", "Tiempo", "Geografía" y "Sectores" (Tablas de Dimensiones). ¿Por qué se prefiere este modelo en BI en lugar de tener todo en una sola tabla gigante de Excel?

A) Porque tener muchas tablas hace que el reporte se vea más sofisticado ante los jefes.

B) Porque permite que el software aplique colores automáticos a las tablas.

C) Porque optimiza drásticamente el rendimiento de las consultas, evita la redundancia de datos (repetición innecesaria de nombres de proveedores) y simplifica la creación de filtros estandarizados.

D) En realidad no se prefiere; la mejor práctica es tener todo en una única tabla plana masiva para evitar los "Joins".

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> El esquema de estrella es el estándar de oro en BI formulado por Ralph Kimball. Separa las métricas (hechos) de los contextos (dimensiones), garantizando el más alto rendimiento de filtrado, compresión de datos y escalabilidad del modelo.
</details>

14. Un tablero de BI de la CGR integra datos de tres sistemas de información diferentes. Se descubre que en uno la ciudad se llama "BOGOTA", en otro "Bogotá D.C." y en otro "11001" (Código DANE). Al hacer los gráficos, salen como si fueran tres ciudades distintas. ¿Qué proceso analítico falló?

A) La Master Data Management (Gestión de Datos Maestros) y la estandarización/homologación en el proceso ETL (crear catálogos unificados).

B) El licenciamiento del software de BI, que es gratuito y no reconoce ciudades.

C) La configuración de la tarjeta gráfica del servidor.

D) El diseño de la paleta de colores del tablero.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> Integrar fuentes dispares requiere crear o referenciar "Datos Maestros" (ej. tabla oficial DIVIPOLA del DANE). Si no se homologan (cruzan y traducen) estos valores en el ETL, la herramienta de BI los tratará como entidades separadas, fragmentando los indicadores.
</details>

15. ¿Qué significa que un informe de Power BI esté configurado con una actualización de "Actualización Incremental" (Incremental Refresh) aplicada a la tabla de pagos de regalías?

A) Que el software de BI actualiza su versión a la más reciente de forma automática.

B) Que el reporte es público y cualquier persona puede insertar datos temporalmente.

C) Que el sistema solo consulta y carga a la memoria los registros nuevos o modificados (ej. el último mes) en lugar de recargar los 20 años de historia cada noche, optimizando recursos y tiempos de procesamiento.

D) Que los cálculos DAX aumentan progresivamente de dificultad.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> La actualización incremental es una técnica avanzada de rendimiento. Establece parámetros temporales para mantener estáticos los datos históricos ("archivados") y solo refrescar los datos recientes, evitando sobrecargar tanto el motor de BI como la base de datos de origen de la entidad.
</details>