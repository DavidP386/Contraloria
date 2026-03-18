# Tema 10: Criminalística Aplicada a Casos Fiscales
1. Durante una inspección sorpresa a una alcaldía intervenida, el equipo de auditoría forense encuentra un computador portátil encendido en el escritorio del tesorero con una sesión bancaria abierta. Para garantizar el principio de cadena de custodia y recolección técnica de la evidencia digital, la instrucción al perito informático debe ser:

A) Apagar de inmediato el equipo desconectándolo de la corriente (Pull the plug) para que no envíen virus por internet.

B) Realizar una adquisición en vivo (Live Forensics) priorizando el volcado de la memoria RAM (donde están contraseñas, sesiones activas y procesos en ejecución) antes de aislar el equipo de la red.

C) Tomar fotos a la pantalla y dejar el computador encendido para que el tesorero lo siga usando.

D) Guardar el computador en una bolsa plástica negra y enviarlo por correo tradicional a Bogotá.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> En criminalística digital moderna, desconectar un equipo encendido (procedimiento clásico) destruye la memoria volátil (RAM), perdiendo evidencia irrecuperable de malware, comunicaciones no cifradas y sesiones activas. Se debe asegurar la RAM primero mediante "adquisición en vivo".
</details>

2. Al revisar las facturas originales de compra de maquinaria pesada, el perito en documentoscopia observa que en el valor total ("$150.000.000"), el número "1" presenta una tonalidad de tinta ligeramente diferente bajo luz ultravioleta, y las fibras del papel alrededor presentan un leve levantamiento. Esto es evidencia técnica de:

A) Falsedad ideológica pura.

B) Un defecto de fábrica inofensivo de las impresoras matriciales.

C) Una alteración material por adición y raspado (borrado mecánico). Se configuró un presunto fraude al alterar físicamente el monto original.

D) Que la factura es 100% auténtica y fue impresa en un clima muy húmedo.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> La alteración de fibras de papel evidencia un intento de borrado (con goma o bisturí), y la luminiscencia dispar de las tintas bajo luz UV delata que un número fue agregado a posteriori con otro bolígrafo o impresora. Esto tipifica la alteración física del documento (Falsedad Material).
</details>

3. Un denunciante anónimo entrega a la gerencia departamental de la CGR un fólder de cartón que contiene planos confidenciales con firmas originales. Al recibirlo, el investigador nota huellas dactilares visibles y manchas oscuras en los documentos. ¿Cuál es el procedimiento inmediato?

A) Fotocopiar los documentos y destruir el fólder físico para proteger la identidad del denunciante.

B) Limpiar las manchas oscuras con alcohol y manipular los folios con las manos desnudas.

C) Embalar el fólder en bolsas de papel (no plástico, para evitar degradación), rotularlo, iniciar el registro de cadena de custodia y solicitar análisis lofoscópico (huellas) al laboratorio forense.

D) Entregar el fólder al alcalde para que verifique si los planos son ciertos.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> Los documentos no solo aportan evidencia por su texto, sino por los rastros biológicos y lofoscópicos que contienen. Su manipulación debe ser técnica (guantes, evitar bolsas plásticas que generen humedad/hongos) y la cadena de custodia debe nacer en el momento de la recepción.
</details>

4. En una investigación por "empresas de papel", la CGR requiere certificar que la dirección IP desde donde se subieron las propuestas de dos empresas supuestamente competidoras al portal SECOP, es exactamente la misma. ¿Qué utilidad tiene el "Hash" (MD5, SHA-256) en la recolección de este registro digital?

A) Traduce el lenguaje binario de las direcciones IP a lenguaje humano comprensible.

B) Oculta la identidad del auditor frente al contratista.

C) Actúa como un algoritmo de cifrado para que nadie pueda leer el documento sin clave.

D) Actúa como una huella dactilar matemática inalterable del archivo recolectado. Si el archivo es modificado un solo byte posteriormente, el hash cambiará por completo, garantizando ante un juez la integridad y no repudio de la evidencia.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: D</b>.


<i>Justificación:</i> Las funciones Hash generan una cadena de caracteres única a partir de un archivo digital. Es el estándar mundial en informática forense para demostrar que la evidencia (logs, correos, bases de datos) presentada en juicio es idéntica bit a bit a la recolectada originalmente, sin haber sido manipulada.
</details>

5. El equipo de auditoría llega a inspeccionar el almacén municipal y encuentra que las puertas están violentadas. El inventario de computadores parece incompleto y las planillas de registro están tiradas en el piso. ¿Qué principio de la criminalística de campo prima en este momento?

A) Proceder de inmediato a contar qué falta para ir avanzando con el acta.

B) Entrevistar a los transeúntes de la calle.

C) Observación, protección y acordonamiento (fijación de la escena). Nadie debe entrar o tocar elementos hasta que los técnicos realicen la inspección planimétrica y fotográfica, pues todo contacto deja un rastro (Principio de Intercambio de Locard).

D) Reorganizar las planillas del piso para que la bodega se vea ordenada antes de tomar las fotos oficiales.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> El Principio de Locard establece que todo criminal deja una parte de sí en la escena y se lleva algo consigo. La protección del lugar de los hechos (acordonamiento y fijación) evita la contaminación, destrucción o alteración de estas evidencias físicas.
</details>

6. Al evaluar un contrato de nómina fantasma, se descubren nóminas firmadas físicamente por "Juan Pérez", pero la auditoría demuestra que él había fallecido 3 meses antes de las fechas de las firmas. Un experto caligráfico es llamado. Si las firmas en la nómina son burdas imitaciones sin parecido a la original, ¿ante qué tipo de alteración estamos?

A) Falsificación por calco.

B) Falsedad ideológica atípica.

C) Falsificación por imitación servil (o libre), donde el falsario intenta copiar los rasgos morfológicos de la firma original a partir de un modelo, pero deja trazos de inseguridad, paradas o retomas evaluables forensemente.

D) Un error administrativo sin dolo de los recursos humanos.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> En grafoscopía, la imitación servil es la reproducción manual de una firma teniendo un modelo a la vista. El análisis forense detecta anomalías en la velocidad, presión y dinamismo del trazo (temblores), que delatan la falsedad frente al automatismo natural del autor original.
</details>

7. Un municipio adquirió camionetas 4x4 blindadas para sus directivos. Al inspeccionarlas, el perito forense en automotores decide aplicar reactivos químicos (revenidos químicos) sobre el número de chasis (VIN) y el bloque del motor. ¿Cuál es el objetivo técnico de esta prueba?

A) Revelar si los números de identificación originales fueron regrabados, limados o adulterados, lo que indicaría que los vehículos entregados al Estado podrían ser robados o de contrabando (gemeleados).

B) Comprobar si el nivel de aceite del motor está en condiciones óptimas.

C) Limpiar el óxido de las piezas metálicas para su correcto mantenimiento patrimonial.

D) Determinar si el blindaje cumple con la norma balística.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> El revenido químico es una técnica metalográfica. Cuando se lima un número de chasis en el metal, la alteración molecular profunda persiste. El ácido corroe el metal revelando espectralmente los números originales que fueron borrados, descubriendo la falsedad marcaria.
</details>

8. En una indagación, se allegan grabaciones de audio interceptadas legalmente donde se discute el desvío de recursos del sistema de salud. La defensa del implicado alega que "esa no es su voz". ¿Qué disciplina forense entra a dirimir esta controversia científica?

A) La Documentoscopia visual.

B) La Biometría Dactilar.

C) La Acústica Forense y fonética (cotejo de voz), que analiza los formantes, frecuencia, tono, intensidad y características articulatorias espectrográficas para determinar identidad o edición del archivo de audio.

D) El polígrafo (detector de mentiras).

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> La acústica forense analiza las grabaciones de sonido. Mediante espectrogramas y análisis de software especializado, el perito compara una muestra indubitada (voz real del sospechoso) contra la muestra cuestionada para certificar la biometría vocal y la ausencia de montajes.
</details>

9. Al momento de incautar un dispositivo móvil corporativo de un funcionario investigado por colusión, el perito informático lo coloca inmediatamente dentro de una "Bolsa de Faraday" antes de transportarlo al laboratorio. Esta acción técnica busca:

A) Proteger el dispositivo de los golpes físicos durante el traslado en el vehículo oficial.

B) Evitar que el dispositivo se descargue por falta de batería.

C) Aislar electromagnéticamente el equipo, bloqueando señales Wi-Fi, Bluetooth y celulares, para evitar que terceros ordenen el borrado remoto de los datos (Wipe) o alteren la información desde afuera.

D) Cumplir con un protocolo estético de embalaje institucional.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: C</b>.


<i>Justificación:</i> En la preservación de evidencia móvil, el mayor riesgo es el borrado remoto (Ej. Find my iPhone - Erase Device). La jaula o bolsa de Faraday bloquea totalmente las ondas de radiofrecuencia, garantizando el aislamiento del celular de la red mientras llega al laboratorio para la extracción forense.
</details>

10. Dentro del informe técnico-pericial de un auditor forense de la CGR, ¿cuál de las siguientes declaraciones compromete la objetividad y neutralidad exigida por la criminalística fiscal?

A) "Se concluye que el Gobernador es culpable del delito penal de peculado y concusión, actuando con dolo premeditado para robar el erario".

B) "Se evidenció una diferencia de $50 millones entre los comprobantes físicos y los saldos en el software contable".

C) "El análisis grafológico determinó que la firma dubitada no corresponde a los trazos de la muestra patrón".

D) "Los núcleos de asfalto extraídos presentan un espesor de 5cm, contraviniendo los 10cm exigidos en el pliego de condiciones".

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> El perito forense o auditor debe ser netamente objetivo, descriptivo y técnico en sus hallazgos fácticos. La imputación de culpabilidad, delitos penales y la calificación del "dolo" o la intención, son juicios de valor exclusivos del Fiscal o el Juez en un tribunal, nunca del técnico investigativo.
</details>

11. Un investigador revisa las declaraciones juramentadas de tres proveedores diferentes que certifican haber transportado alimentos el mismo día al mismo lugar. Al analizar los documentos mediante perfilamiento criminalístico, nota que los tres textos, aunque firmados por distintas empresas, tienen exactamente los mismos errores ortográficos, el mismo espaciado irregular y la misma fuente tipográfica. ¿A qué conclusión orienta este indicio?

A) Que se usó el mismo modelo de Word amparado por el SECOP.

B) Sugiere un "origen común" (fabricación documental centralizada). Es un fuerte indicio de carrusel o simulación, donde un solo actor elaboró toda la documentación presuntamente falsa para dar apariencia de pluralidad.

C) Que los proveedores asistieron a la misma escuela.

D) Es una simple coincidencia irrelevante en auditoría financiera.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> En criminalística documental, la identificación de patrones de redacción idénticos, "copy-paste", o los mismos errores tipográficos en documentos que deberían ser independientes, delata que fueron creados por la misma persona u oficina, configurando simulación de competencia (falsedad).
</details>

12. En la investigación de una red de desvío de fondos (Lavado de Activos / Corrupción Fiscal), el analista utiliza una herramienta gráfica (como Analyst's Notebook o Gephi) para crear mapas de nodos y enlaces conectando IPs, socios comerciales, representantes legales y cuentas bancarias. Esta técnica criminalística se conoce como:

A) Análisis de Vínculos o Redes (Link Analysis), fundamental para mapear el entramado criminal, identificar empresas fachada, beneficiarios ocultos y testaferros en casos de complejidad financiera.

B) Fotogrametría aérea.

C) Dactiloscopia corporativa.

D) Grafoscopía de transacciones.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: A</b>.


<i>Justificación:</i> El Análisis de Vínculos es la columna vertebral de la inteligencia financiera y forense. Permite visualizar relaciones encubiertas entre personas aparentemente no relacionadas, descubriendo la estructura jerárquica y operativa de las redes de corrupción para seguir la "ruta del dinero".
</details>

13. Para que un elemento material probatorio o evidencia física (ej. un contrato original alterado) sea admisible y tenga fuerza vinculante dentro de un proceso de Responsabilidad Fiscal o Penal, debe cumplir con los requisitos de Legalidad, Autenticidad, y:

A) Ser publicitado previamente en los medios masivos de comunicación.

B) Mismidad, asegurada a través de un riguroso registro de Cadena de Custodia que documente su historia desde la recolección hasta la presentación en audiencia, evitando la contaminación.

C) Haber sido obtenido por un ciudadano de forma anónima rompiendo chapas.

D) Estar firmado digitalmente por el Presidente de la República.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> La mismidad garantiza que el objeto físico presentado ante el fallador (juez/contralor) es exactamente el mismo que se halló en la escena, sin haber sufrido mutaciones, sustituciones o alteraciones. Si la cadena de custodia se rompe, la prueba se vuelve nula.
</details>

14. Durante el interrogatorio (entrevista técnica) a un almacenista municipal por la desaparición de medicamentos, el investigador nota indicadores de comunicación no verbal: sudoración excesiva, contacto visual evasivo, rigidez muscular y frotamiento constante de las manos. Desde la técnica de la entrevista investigativa, estas señales:

A) Son prueba irrefutable, legal y suficiente de que la persona robó los medicamentos.

B) Son irrelevantes; en forense solo sirve lo que está escrito.

C) Indican que el empleado requiere atención médica de urgencia.

D) Son reacciones fisiológicas asociadas al estrés o la carga cognitiva (posible engaño o temor). Sirven como "alertas rojas" tácticas para profundizar el interrogatorio en esas áreas temáticas, pero nunca constituyen prueba plena por sí solas.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: D</b>.


<i>Justificación:</i> La kinésica (lenguaje corporal) y la proxémica son herramientas auxiliares de la entrevista investigativa. Permiten evaluar la reacción fisiológica ante preguntas críticas para guiar la estrategia interrogatoria (detectar estrés/engaño), pero no reemplazan la prueba física o documental.
</details>

15. Un equipo auditor realiza una inspección física a un colegio recién inaugurado. Al golpear las columnas de concreto que debían ser sólidas, se escucha un sonido hueco. Para comprobar sin destruir el colegio si el contratista rellenó las columnas con icopor (poliestireno) en lugar de acero y cemento estructural, la técnica criminalística no destructiva idónea es:

A) Pedirle al alcalde los recibos de compra del cemento.

B) El uso de Escáneres de Ferroscan (Georradar o ultrasonido), que permiten mapear y "ver" a través de las estructuras sólidas la densidad y la disposición del acero interno sin perforar.

C) Demoler completamente tres columnas y observar.

D) Medir el perímetro externo con una cinta métrica escolar.

<details><summary><b>Ver respuesta y justificación</b></summary>
<b>Respuesta correcta: B</b>.


<i>Justificación:</i> En la auditoría forense de obras civiles, se recurre a la ingeniería forense. Cuando hay sospecha de "calidad encubierta", las pruebas no destructivas (NDT) como el ultrasonido, esclerometría o ferroscan permiten evaluar la integridad de los materiales sin comprometer o dañar la obra estatal.
</details>