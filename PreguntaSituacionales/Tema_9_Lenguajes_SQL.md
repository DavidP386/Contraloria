# Tema 9 - Lenguajes y SQL (20 casos)

Pregunta 1.
Durante una auditoria, recibes una base en SQL donde las fechas vienen como texto con formato inconsistente ('01/02/2025', '2025-02-01', '02-01-25'). Debes preparar una consulta para ordenar por fecha real.

Que haces?

- A) Convertir la columna a un tipo DATE uniforme usando funciones de parseo y documentar la transformacion
- B) Ordenar directamente por la columna tal como esta
- C) Eliminar filas con formatos diferentes
- D) Asignar la fecha actual a las filas dudosas

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: A

Justificacion: El ordenamiento requiere un tipo de dato homogeneo; las fechas deben normalizarse.

</details>


Pregunta 2.
El area tecnica solicita un reporte donde se identifiquen pagos duplicados. La tabla tiene millones de registros y la consulta actual tarda demasiado.

Que haces?

- A) Crear un SELECT * sin filtros
- B) Usar indices apropiados en columnas de factura y proveedor; aplicar GROUP BY HAVING COUNT()>1
- C) Exportar todo a Excel
- D) Eliminar las filas que parecen repetidas sin verificar

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Los indices y clausulas HAVING permiten detectar duplicados eficientemente.

</details>


Pregunta 3.
Necesitas unir dos tablas de beneficiarios por identificacion, pero una tiene ceros a la izquierda ('00123') y la otra no ('123').

Que haces?

- A) Hacer el JOIN y confiar en coincidencias parciales
- B) Eliminar ceros a la izquierda sin revisar
- C) Normalizar ambas columnas (TRIM, LPAD o CAST) antes del JOIN
- D) Usar nombres en lugar de identificacion

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: C

Justificacion: La normalizacion asegura coincidencias correctas y evita perdidas de registros.

</details>


Pregunta 4.
Un analista usa SELECT DISTINCT * para eliminar duplicados, pero esto elimina filas que si eran diferentes en una sola columna.

Que haces?

- A) Usarlo igual para simplificar
- B) Pedir que envien otro dataset
- C) Eliminar columnas para que DISTINCT funcione
- D) Definir claves compuestas y aplicar deduplicacion precisa

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: D

Justificacion: La deduplicacion debe basarse en claves reales, no en todas las columnas juntas.

</details>


Pregunta 5.
Un script en Python que carga datos para auditoria se demora demasiado porque lee el archivo linea por linea.

Que haces?

- A) Aumentar el tiempo de ejecucion
- B) Usar lectura por bloques (chunks) o librerias optimizadas (pandas.read_csv con parametros)
- C) Convertir a Excel para que sea mas rapido
- D) Borrar lineas del archivo

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: La lectura por bloques mejora el rendimiento sin perdida de datos.

</details>


Pregunta 6.
Una consulta SQL genera resultados inconsistentes porque usa JOIN sin condiciones completas.

Que haces?

- A) Dejar que SQL haga el join automatico
- B) Quitar filtros para que 'todo coincida'
- C) Revisar condiciones ON, evitar joins cartesianos y probar incrementalmente
- D) Forzar coincidencias con LIKE

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: C

Justificacion: Joins incompletos producen combinaciones indeseadas que alteran resultados.

</details>


Pregunta 7.
Necesitas obtener el segundo valor mas alto de una tabla de pagos.

Que haces?

- A) Ordenar y tomar el primero
- B) Usar COUNT()
- C) Eliminar los valores mayores
- D) Usar funciones como ROW_NUMBER() o subconsulta con MAX() y <>

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: D

Justificacion: Las funciones analiticas permiten identificar posiciones especificas.

</details>


Pregunta 8.
Una base trae valores nulos en columna clave para unir contratos con proveedores.

Que haces?

- A) Identificar origen del nulo, imputar o excluir segun regla documental
- B) Hacer join igual
- C) Rellenar con cero siempre
- D) Concatenar con otra columna para 'improvisar' una llave

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: A

Justificacion: Los nulos en llaves deben corregirse o tratarse con criterio antes del join.

</details>


Pregunta 9.
Un informe requiere calcular sobrecostos por proveedor usando SQL.

Que haces?

- A) Usar SUM sin agrupar
- B) Duplicar los valores para que se vean altos
- C) Agrupar por proveedor y usar expresiones para comparar valor contratado vs ejecutado
- D) Registrar solo un proveedor

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: C

Justificacion: Las agregaciones deben segmentarse por proveedor para un analisis correcto.

</details>


Pregunta 10.
Encontraste columnas duplicadas en una tabla (ej. monto1, monto_duplicado) con valores distintos.

Que haces?

- A) Usar cualquiera
- B) Sumar ambas
- C) Eliminar la columna duplicada sin revisar
- D) Verificar trazabilidad, reglas de negocio y consolidar origen correcto

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: D

Justificacion: La consistencia depende de identificar cual columna es valida y su origen.

</details>


Pregunta 11.
Un proceso ETL falla porque cambio el nombre de una columna en la fuente.

Que haces?

- A) Implementar validaciones de esquema y actualizar mapeo documentado
- B) Cambiar el ETL sin registro
- C) Ignorar el error
- D) Quitar la columna

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: A

Justificacion: Los cambios deben registrarse y el ETL debe validarse contra el esquema.

</details>


Pregunta 12.
Necesitas transformar datos de formato ancho a formato largo para analisis.

Que haces?

- A) Quedarte con el formato ancho
- B) Usar funciones UNPIVOT o melt() en Python
- C) Crear columnas manualmente
- D) Multiplicar filas

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: El formato largo facilita analisis agregados y series temporales.

</details>


Pregunta 13.
Un analista usa SQL con SELECT * en tablas sensibles.

Que haces?

- A) Aceptarlo
- B) Dar permisos de administrador
- C) Exportar todo
- D) Restringir a columnas necesarias y proteger datos sensibles

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: D

Justificacion: Se debe limitar exposicion de datos y cumplir proteccion de informacion.

</details>


Pregunta 14.
Hay un error porque en Python concatenan cadenas y numeros sin conversion.

Que haces?

- A) Convertir tipos explicitamente segun su naturaleza
- B) Forzar a string todo
- C) Quitar numeros
- D) Evitar concatenaciones

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: A

Justificacion: La conversion de tipos evita errores y mantiene integridad.

</details>


Pregunta 15.
Requieres unir datos de un API json con una tabla SQL.

Que haces?

- A) Pegar los json en Excel
- B) Normalizar claves, convertir json a estructura tabular y luego unir
- C) Copiar y pegar los valores
- D) Unir por filas sin claves

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Los json deben tabularse para integrarse con SQL.

</details>


Pregunta 16.
Un calculo DAX se recalcula lento por usar columnas calculadas en vez de medidas.

Que haces?

- A) No cambiar nada
- B) Eliminar columnas
- C) Reemplazar con medidas basadas en contexto de filtro
- D) Duplicar tablas

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: C

Justificacion: Las medidas son mas eficientes y responden al contexto.

</details>


Pregunta 17.
El analista quiere meter logica compleja en SQL que corresponde al ETL.

Que haces?

- A) Mantener la logica en ETL y dejar SQL para consultas claras
- B) Permitirlo
- C) Dividir todo en muchas subconsultas
- D) Usar Excel

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: A

Justificacion: El ETL debe contener la transformacion y SQL enfocarse en consulta.

</details>


Pregunta 18.
Necesitas validar la integridad de un dataset masivo.

Que haces?

- A) Revisarlo manual
- B) Cortar la base
- C) Implementar checks automaticos (unicidad, nulos, rangos)
- D) Quitar columnas

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: C

Justificacion: Los checks garantizan calidad sin intervencion manual.

</details>


Pregunta 19.
En Python, un loop sobre filas causa lentitud en una transformacion masiva.

Que haces?

- A) Mantener loop
- B) Usar operaciones vectorizadas (pandas)
- C) Procesar una fila al mes
- D) Crear mas loops

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Las operaciones vectorizadas aceleran miles de veces el procesamiento.

</details>


Pregunta 20.
Un script SQL falla cuando usa LIKE con patrones sin escapar.

Que haces?

- A) Quitar LIKE
- B) Eliminar filas con errores
- C) Usar * en vez de %
- D) Escapar caracteres especiales y validar expresiones

<details><summary>Mostrar respuesta</summary>

Respuesta correcta: D

Justificacion: LIKE requiere manejo adecuado de caracteres especiales.

</details>

