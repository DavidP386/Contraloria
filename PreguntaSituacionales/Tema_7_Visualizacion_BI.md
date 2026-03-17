# Tema 7 - Visualizacion y BI (20 casos)

Pregunta 1.
Durante la presentacion de un dashboard de contratacion, indicadores no coinciden con el total del dataset filtrado por año.

Que haces?

- A) Ignorar
- B) Revisar filtros a nivel de pagina y visual, y relaciones en el modelo; explicar y corregir
- C) Culpar al origen
- D) Cerrar la presentacion
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Los filtros y relaciones pueden desalinear medidas; se valida el modelo y se corrige en vivo si es posible.

</details>


Pregunta 2.
Un mapa de calor en Power BI tarda demasiado; usas una tabla de 5 millones de filas sin agregaciones.

Que haces?

- A) Aumentar RAM
- B) Implementar agregaciones/summary tables y reducir cardinalidad de columnas
- C) Quitar el mapa
- D) Exportar a Excel
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Las agregaciones y la reduccion de cardinalidad mejoran el performance en BI.

</details>


Pregunta 3.
La direccion solicita un indicador 'porcentaje de sobrecostos evitados' que no existe en fuente.

Que haces?

- A) Inventarlo
- B) Negarte
- C) Definir formula (sobreprecio detectado/precio proyectado) con trazabilidad y supuestos
- D) Usar valor promedio del sector
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: C

Justificacion: Se diseña la metrica con definicion clara, supuestos y trazabilidad para interpretacion.

</details>


Pregunta 4.
Un slicer por entidad oculta valores en un grafico apilado; usuarios creen que faltan datos.

Que haces?

- A) Eliminar slicer
- B) Agregar etiqueta 'datos filtrados' y tooltips explicativos; revisar interacciones entre visuales
- C) Bloquear cambios
- D) Publicar sin cambios
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Se documenta el contexto del filtro y se ajustan interacciones para transparencia.

</details>


Pregunta 5.
Solicitan compartir un dashboard con entidades territoriales externas que no tienen licencias.

Que haces?

- A) Enviar PBIX
- B) Publicar en web abierta
- C) Usar app con permisos y/o exportar reporte paginado/archivo estatico segun politica
- D) Dar usuario generico
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: C

Justificacion: Se respeta el modelo de seguridad y, de ser necesario, se entrega version estatica segun politica.

</details>


Pregunta 6.
Una medida DAX suma montos duplicados por relaciones muchos-a-muchos.

Que haces?

- A) Dividir entre 2
- B) Crear tablas puente y ajustar direccion de filtro; usar SUMX sobre contexto correcto
- C) Sumar en Excel
- D) Eliminar una tabla
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Las M:M requieren tabla puente o modelado adecuado para evitar doble conteo.

</details>


Pregunta 7.
Un grafico muestra valores negativos por devoluciones, confundiendo a la audiencia.

Que haces?

- A) Ocultar negativos
- B) Separar devoluciones con color/tooltip y explicar definiciones
- C) Tomar valor absoluto
- D) Eliminar devoluciones
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Se mantiene integridad y se comunica el significado de negativos.

</details>


Pregunta 8.
Piden un KPI de cumplimiento con semaforos; no hay metas oficiales definidas.

Que haces?

- A) Usar meta arbitraria
- B) Solicitar acto/soporte de metas; mientras tanto, mostrar tendencia sin semaforos
- C) No mostrar nada
- D) Pedir meta verbal
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Los semaforos requieren metas oficiales; se muestra tendencia hasta contar con soporte.

</details>


Pregunta 9.
El dashboard tarda en abrir por columnas de texto de alta cardinalidad no usadas en visuales.

Que haces?

- A) Nada
- B) Remover columnas innecesarias del modelo y deshabilitar carga de consultas auxiliares
- C) Comprar hardware
- D) Exportar a CSV
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Reducir el modelo mejora tiempos de carga y memoria.

</details>


Pregunta 10.
Un indicador de promedio ponderado usa mal la agregacion simple.

Que haces?

- A) Dejarlo asi
- B) Construir medida con SUMX(peso*valor)/SUM(peso)
- C) Usar promedio simple
- D) Promediar promedios
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: El promedio ponderado requiere ponderar por pesos en la medida.

</details>


Pregunta 11.
Directivos quieren un ranking de 'peores proveedores' y publicarlo sin contexto.

Que haces?

- A) Publicarlo
- B) Agregar metodologia, periodo, umbrales y derecho de replica antes de publicar
- C) Negarse sin alternativa
- D) Usar ranking del mes pasado
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Se debe incluir metodologia y contexto para evitar interpretaciones engañosas.

</details>


Pregunta 12.
Usuarios piden exportar a Excel cada visual con mas de 150k filas.

Que haces?

- A) Permitir libremente
- B) Implementar reportes paginados o vistas resumidas y controles de acceso
- C) Enviar todo por correo
- D) Negar toda exportacion
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Exportaciones masivas requieren paginacion/resumen y seguridad.

</details>


Pregunta 13.
Una pagina 'Movil' no se ve bien en telefonos institucionales.

Que haces?

- A) Usar la de escritorio
- B) Rediseñar vista movil con menos visuales y tarjetas clave
- C) Recomendar tablets
- D) Ocultar la pagina
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: La vista movil exige diseno especifico y jerarquia de informacion.

</details>


Pregunta 14.
El color del semaforo no cumple contraste para accesibilidad.

Que haces?

- A) Ignorar
- B) Ajustar paleta con suficiente contraste y patrones alternativos
- C) Quitar colores
- D) Bajar brillo
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Accesibilidad requiere contraste adecuado y refuerzos visuales.

</details>


Pregunta 15.
Una medida TIME INTELLIGENCE no respeta el calendario fiscal (julio-junio).

Que haces?

- A) Usar calendario natural
- B) Crear tabla calendario fiscal con marcas y usar funciones adecuadas
- C) Sumar meses manual
- D) Cambiar formato de fecha
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: La inteligencia de tiempo depende de un calendario fiscal bien definido.

</details>


Pregunta 16.
Hay sospecha de manipulacion de datos fuente antes del ETL.

Que haces?

- A) Confiar
- B) Establecer linaje de datos, auditoria de cambios y checksum de archivos
- C) Borrar cache
- D) No registrar
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: El linaje y auditoria permiten detectar alteraciones y preservar trazabilidad.

</details>


Pregunta 17.
Solicitan unir dos fuentes con codigos de entidades inconsistentes (ceros a la izquierda).

Que haces?

- A) Concatenar sin revisar
- B) Normalizar codigos (padding/trimming) y documentar
- C) Eliminar ceros
- D) Usar nombres
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: La normalizacion de claves garantiza joins correctos.

</details>


Pregunta 18.
Usuarios interpretan mal un grafico de barras apiladas con muchos segmentos.

Que haces?

- A) Dejarlo
- B) Cambiar a barras agrupadas o small multiples y agregar explicaciones
- C) Usar torta
- D) Ocultar leyenda
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Se elige visual que facilite comparacion y lectura.

</details>


Pregunta 19.
Un KPI muestra 105% por error de redondeo y doble conteo de meta.

Que haces?

- A) Redondear a 100%
- B) Corregir formula y deduplicar meta; mostrar decimales razonables
- C) Esconder porcentaje
- D) Cambiar meta
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Se corrige logica y se exponen decimales con criterio.

</details>


Pregunta 20.
Una consulta DirectQuery a base transaccional causa bloqueos en horas pico.

Que haces?

- A) Mantener DirectQuery
- B) Considerar import con actualizaciones programadas y vistas optimizadas
- C) Pedir mas CPU
- D) Duplicar base
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Import reduce cargas en pico; se optimizan vistas para BI.

</details>

