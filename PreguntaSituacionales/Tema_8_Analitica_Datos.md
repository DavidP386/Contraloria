# Tema 8 - Analitica y Datos (20 casos)

Pregunta 1.
Recibes dataset con faltantes en montos y fechas clave para series temporales.

Que haces?

- A) Ignorar
- B) Imputar segun metodo apropiado (forward fill/mediana) y marcar imputados
- C) Eliminar todo
- D) Rellenar con cero
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: La imputacion documentada preserva analisis y evita sesgos.

</details>


Pregunta 2.
Se detectan outliers extremos en pagos; el jefe pide quitarlos para que el modelo 'luzca bien'.

Que haces?

- A) Quitarlos sin documentar
- B) Analizar causa (error, caso real) y usar metodos robustos o winsorizacion con soporte
- C) Promediar
- D) Ignorar
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Los outliers se tratan segun causa, con metodos y trazabilidad.

</details>


Pregunta 3.
Variables categoricas tienen alta cardinalidad (miles de niveles).

Que haces?

- A) One-hot a todo
- B) Agrupar niveles raros y usar codificacion target/WOE con validacion
- C) Eliminar variable
- D) Orden alfabetico
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Se controla cardinalidad y se usa codificacion adecuada.

</details>


Pregunta 4.
Data leakage: en entrenamiento aparece una variable creada con datos del futuro.

Que haces?

- A) Mantenerla
- B) Eliminarla del entrenamiento y rehacer validacion temporal
- C) Imputar
- D) Usar KNN
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Evitar leakage exige respetar corte temporal y reentrenar.

</details>


Pregunta 5.
Desbalance severo (1% positivos) en deteccion de fraude.

Que haces?

- A) Accuracy simple
- B) Ajustar umbral, usar metricas como AUC/PR y tecnicas de balance (SMOTE, class weights)
- C) Duplicar negativos
- D) RMSE
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Se usan metricas y tecnicas adecuadas para clases desbalanceadas.

</details>


Pregunta 6.
Solicitan explicabilidad del modelo para toma de decisiones.

Que haces?

- A) Modelo caja negra
- B) Aplicar interpretabilidad (SHAP/feature importance) y reporte de impacto
- C) Omitir
- D) Entregar solo el codigo
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: La explicabilidad es clave en gobierno de datos y auditoria.

</details>


Pregunta 7.
Pipeline ETL falla por cambios en esquema (columna nueva).

Que haces?

- A) Modificar a mano cada vez
- B) Implementar validaciones de esquema y contratos de datos; versionar
- C) Ignorar
- D) Desactivar alerta
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Contratos de datos y validacion de esquema previenen rupturas.

</details>


Pregunta 8.
Piden un pronostico mensual pero solo hay tres meses de datos.

Que haces?

- A) Pronosticar igual
- B) Advertir insuficiencia y proponer escenarios o datos externos
- C) Interpolar al año
- D) Duplicar valores
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Se requiere base historica; se proponen alternativas responsables.

</details>


Pregunta 9.
Duplicados exactos y casi-duplicados en beneficiarios.

Que haces?

- A) Ignorar
- B) Ejecutar deduplicacion (claves compuestas, distancia fuzzy) con bitacora
- C) Eliminar todo
- D) Pedir carta
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: La calidad de datos exige deduplicar con registro de cambios.

</details>


Pregunta 10.
Datos personales sensibles aparecen en un dataset de uso analitico abierto.

Que haces?

- A) Publicar
- B) Anonimizar/Testar y aplicar controles de acceso; registrar riesgo
- C) Pedir permiso general
- D) Poner contraseña
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Se protege la privacidad mediante tecnicas y controles.

</details>


Pregunta 11.
Un compañero propone evaluar el modelo solo con accuracy en clase desbalanceada.

Que haces?

- A) Aceptar
- B) Usar precision, recall, F1 y curva PR; justificar
- C) Solo AUC
- D) Solo matriz de confusion
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Metricas adecuadas evitan conclusiones engañosas.

</details>


Pregunta 12.
Solicitan unir pagos y beneficiarios con llaves inconsistentes por espacios y mayusculas.

Que haces?

- A) Join directo
- B) Estandarizar (trim, casefold) y validar cobertura del match
- C) Eliminar filas sin match
- D) Usar ID secuencial
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Normalizar llaves mejora la calidad del join.

</details>


Pregunta 13.
Modelo en produccion degrada su performance tras cambios de politica.

Que haces?

- A) Ignorar
- B) Implementar monitoreo de deriva de datos/etiquetas y reentrenar
- C) Bajar umbral
- D) Detener logs
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: El monitoreo y el reentrenamiento gestionan la deriva.

</details>


Pregunta 14.
Solicitan un score de riesgo pero no existe etiqueta historica.

Que haces?

- A) Modelar igual
- B) Proponer enfoque semisupervisado/reglas y plan para construir etiquetas
- C) Aleatorio
- D) Eliminar variables
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Sin etiqueta se usan metodos alternos y se planifica obtencion de labels.

</details>


Pregunta 15.
El jefe pide publicar los datos abiertos sin diccionario ni licencia.

Que haces?

- A) Publicar ya
- B) Publicar con diccionario, metadatos, licencia y versionado
- C) Solo CSV
- D) PDF
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Los datos abiertos requieren metadatos, licencia y versionado.

</details>


Pregunta 16.
Se necesita reproducibilidad del analisis en auditorias futuras.

Que haces?

- A) Guardar solo Excel final
- B) Versionar codigo/datos, usar notebooks parametrizados y seeds
- C) Guardar capturas de pantalla
- D) Enviar por correo
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: La reproducibilidad exige versionado y parametrizacion.

</details>


Pregunta 17.
Columnas de fecha tienen formatos mixtos y zonas horarias distintas.

Que haces?

- A) Convertir a texto
- B) Normalizar a ISO 8601 y zona definida; documentar
- C) Usar dia/mes segun vista
- D) Eliminar fechas
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Estandarizar fechas evita errores en series y joins.

</details>


Pregunta 18.
Solicitan comparar costos entre entidades con tamaños muy distintos.

Que haces?

- A) Usar totales
- B) Normalizar por indicadores (per capita, por contrato) y reportar intervalos
- C) Ordenar por nombre
- D) Solo promedio
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: La normalizacion permite comparaciones justas y replicables.

</details>


Pregunta 19.
Un analista usa datos de entrenamiento en el ajuste de hiperparametros sin validacion separada.

Que haces?

- A) Continuar
- B) Usar validacion cruzada o holdout; registrar pipeline de tuning
- C) Probar en el mismo set
- D) Ajustar a ojo
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Separar entrenamiento/validacion evita sobreajuste.

</details>


Pregunta 20.
Se requiere integrar logs de sistemas con distintos codigos de caracter y separadores.

Que haces?

- A) Importar como venga
- B) Estandarizar encoding (UTF-8) y delimitadores; probar con muestras y validaciones
- C) Cargar a mano
- D) Convertir a imagen
<details><summary>Mostrar respuesta</summary>

Respuesta correcta: B

Justificacion: Estandarizar formatos facilita ETL robusto.

</details>

