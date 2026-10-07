# Usar una rúbrica didáctica con criterios e indicadores de cumplimiento para clasificar escenarios ficticios de lavado de dinero, evasión fiscal y desviaciones operativas

## Metadatos

| Parámetro | Valor |
| :--- | :--- |
| **Duración** | 8 minutos |
| **Complejidad** | Alta (Hard) |
| **Nivel de Bloom** | Analizar (Analyze) |

## Descripción General

En esta práctica de laboratorio, el estudiante aplicará metodologías avanzadas de análisis de riesgos legales y normativos mediante el uso de Microsoft 365 Copilot en Microsoft Word. Utilizando una plantilla que define una rúbrica de cumplimiento basada en estándares de auditoría, el estudiante evaluará y clasificará tres escenarios corporativos ficticios diseñados para simular lavado de dinero, evasión de impuestos y desviaciones de procedimientos internos. 

A través de un prompt altamente estructurado bajo el framework de ingeniería de prompts, se forzará al modelo de lenguaje a delimitar con precisión milimétrica dónde termina la evidencia tangible de los hechos y dónde inicia la especulación o inferencia jurídica analítica. El resultado final del análisis se integrará directamente en el documento para su posterior guardado como `escenarios_clasificados_v1.docx` dentro del directorio local de trabajo sincronizado en OneDrive.

## Objetivos de Aprendizaje

Al finalizar este laboratorio, serás capaz de:
* [ ] **Interpretar e integrar** una rúbrica de cumplimiento normativo compleja estructurada dentro de un documento activo de Word.
* [ ] **Diseñar y ejecutar** prompts de ingeniería estructurados con delimitación lógica estricta utilizando el panel lateral de Copilot en Word.
* [ ] **Clasificar** comportamientos de riesgo legal (lavado de dinero, evasión fiscal y desviaciones operativas) distinguiendo entre Indicador, Anomalía, Señal de Alerta y Conclusión.
* [ ] **Evaluar y separar** de forma clara la evidencia empírica/fáctica de las inferencias analíticas sugeridas por la inteligencia artificial.

## Prerrequisitos

* Acceso a una cuenta activa de **Microsoft 365 Copilot Premium (Service Update 2408)**.
* Licencia activa y aplicación instalada de **Microsoft Word para Microsoft 365 (Desktop)** (Versión 2408 Build 17928.20156 o superior en el Canal Mensual Empresarial).
* Conexión a Internet de banda ancha estable (mínimo 20 Mbps de bajada / 10 Mbps de subida) con acceso desbloqueado a los endpoints de Microsoft 365 y OneDrive.
* Cuenta de OneDrive de la organización configurada y sincronizada activamente con el explorador de archivos local en Windows 11 Enterprise (Versión 23H2 o superior).

## Entorno de Laboratorio

### Especificaciones de Software y Herramientas

| Software / Servicio | Versión de Referencia | Enlace de Documentación Oficial |
| :--- | :--- | :--- |
| Microsoft Windows 11 Enterprise | Versión 23H2 o superior | [Documentación de Windows 11](https://learn.microsoft.com/es-es/windows/whats-new/whats-new-windows-11) |
| Microsoft Word para Microsoft 365 (Desktop) | Versión 2408 (Build 17928.20156) | [Documentación de Microsoft Word](https://learn.microsoft.com/es-es/office/client-developer/word-home) |
| Microsoft 365 Copilot (Premium) | Service Update 2408 | [Documentación de Microsoft 365 Copilot](https://learn.microsoft.com/es-es/copilot/microsoft-365/) |
| Microsoft Edge | Versión 128.0.2739.42 o superior | [Documentación de Microsoft Edge](https://learn.microsoft.com/es-es/deployedge/edge-documentation) |

### Preparación del Directorio de Trabajo

Todo el trabajo debe realizarse dentro de la carpeta local de sincronización con OneDrive para permitir el anclaje de datos de Copilot (*grounding*):

* **Ruta de Trabajo Local**: `C:\CursoCopilotLegal\Modulo3_4\` (Sincronizada con OneDrive).

---

## Instrucciones Paso a Paso

### Paso 1: Configurar el Documento Base de Rúbrica en Word

**Objective**: Crear y guardar la plantilla `rubrica_cumplimiento.docx` conteniendo la matriz oficial de evaluación de riesgos para que actúe como contexto directo en OneDrive.

1. Abre la aplicación de escritorio de **Microsoft Word para Microsoft 365**.
2. Crea un **Documento en blanco**.
3. Copia y pega el siguiente texto completo que define la rúbrica y taxonomía de cumplimiento en el cuerpo del documento:

```text
## RÚBRICA Y TAXONOMÍA DE EVALUACIÓN DE RIESGOS DE CUMPLIMIENTO

## 1. Definición de Categorías de Hallazgos
- [INDICADOR]: Métrica operativa, flujo comercial u operación financiera habitual y neutra que monitoriza una línea base normal. No presupone sospechas en sí misma.
- [ANOMALÍA]: Desviación de la línea base operativa o estadística. Suceso inusual o atípico que carece de contexto de intencionalidad o daño material aparente.
- [SEÑAL DE ALERTA]: Anomalía recurrente o con patrones contextuales coincidentes con tipologías de riesgo (fraude, evasión, lavado). Demuestra indicios de elusión deliberada de controles pero sin prueba forense absoluta. Requiere investigación inmediata.
- [CONCLUSIÓN]: Hallazgo verificado técnicamente y respaldado por evidencias empíricas irrefutables, admisiones o nexos causales claros donde se comprueba el incumplimiento legal.

## 2. Matriz de Gravedad y Riesgo (Escala 1 a 3)
- Criterio A: Intencionalidad / Patrón de Elusión
  * 1 (Bajo): Error material aparente, falla operativa sin dolo ni ocultación de datos.
  * 2 (Medio): Negligencia grave, falta de debida diligencia u omisión selectiva de procesos de validación.
  * 3 (Alto): Acciones explícitas de fraccionamiento, simulación, falsificación o destrucción de registros para evadir regulaciones.
- Criterio B: Impacto Regulatorio y Penal
  * 1 (Bajo): Incumplimiento subsanable internamente. Sin repercusión externa ni sanciones administrativas estimables.
  * 2 (Medio): Posible sanción administrativa de reguladores financieros, pérdida de certificaciones o multas económicas moderadas.
  * 3 (Alto): Configuración de presuntos delitos (lavado de activos, defraudación tributaria fraudulenta), riesgo penal corporativo o disolución de licencias operativas.

## 3. Escala de Riesgo Global (Suma de Criterio A + Criterio B)
- Puntaje 2-3: Clasificar como [ANOMALÍA]
- Puntaje 4-5: Clasificar como [SEÑAL DE ALERTA]
- Puntaje 6: Clasificar como [CONCLUSIÓN]
```

4. Haz clic en **Archivo** > **Guardar como...**
5. Navega hasta la carpeta sincronizada con OneDrive: `C:\CursoCopilotLegal\Modulo3_4\`.
6. Guarda el documento con el nombre exacto: `rubrica_cumplimiento.docx`.
7. Espera unos segundos para asegurar que el icono de estado de guardado muestre "Sincronizado" (icono de la nube o check verde).

**Expected output**: El archivo `rubrica_cumplimiento.docx` guardado y sincronizado de forma correcta, con la taxonomía oficial de riesgo disponible en el texto del documento.

**Verification**: Abre el Explorador de Archivos de Windows, dirígete a `C:\CursoCopilotLegal\Modulo3_4\` y confirma que `rubrica_cumplimiento.docx` muestra el icono de estado verde o azul (sincronizado con la nube de OneDrive corporativo).

---

### Paso 2: Habilitar Copilot en Word e Introducir los Escenarios Ficticios

**Objective**: Abrir el panel lateral de Copilot en Word y preparar los datos de los tres escenarios financieros ficticios para su posterior inyección y procesamiento.

1. Con el archivo `rubrica_cumplimiento.docx` abierto, haz clic en el botón de **Copilot** ubicado en el extremo derecho de la pestaña **Inicio** de la cinta de opciones de Word.

   *Nota: Se abrirá el panel de chat lateral derecho de Microsoft 365 Copilot.*

2. Lee detenidamente los siguientes tres escenarios de riesgo ficticios que procesarás en el siguiente paso:

   * **Escenario Ficticio 1: Inmobiliaria Alpha**
     * *Hechos*: La entidad ficticia "Inmobiliaria Alpha" registra la venta de 5 locales comerciales en un lapso de 48 horas. Todos los pagos son recibidos en efectivo en ventanilla bancaria por montos individuales de $9,900 USD, justo por debajo del umbral de reporte de transacciones en efectivo ($10,000 USD). Las transacciones fueron estructuradas a nombre de distintas personas físicas que declaran el mismo domicilio fiscal.
   * **Escenario Ficticio 2: Consultora Tributaria Nexus-Tax**
     * *Hechos*: La empresa ficticia "Nexus-Tax" realiza transferencias mensuales sistemáticas en concepto de "Asesoría Estratégica en TI" a una cuenta en una jurisdicción de baja imposición por un monto exacto equivalente al 98% de sus utilidades fiscales del mes. No existen entregables de TI en los repositorios de la empresa, pero sí correos de la gerencia que dicen: "Ajusta la facturación del servicio fantasma de este mes con la offshore para neutralizar el impuesto sobre la renta antes del cierre fiscal".
   * **Escenario Ficticio 3: Acceso a Servidores de Base de Datos**
     * *Hechos*: Se registra el acceso inusual del Ingeniero de Infraestructura "X" a la base de datos de producción el día domingo a las 2:00 AM desde una dirección IP residencial en el extranjero. El volumen de descarga fue de 15 GB de datos estructurados de clientes corporativos. El Ingeniero de Infraestructura está bajo el régimen ordinario de teletrabajo de guardia pasiva los fines de semana.

**Expected output**: Panel de Copilot activo en el costado derecho de Microsoft Word con la sesión inicializada y lista para recibir entradas estructuradas.

**Verification**: Visualiza el prompt de entrada del panel lateral de Copilot que debe mostrar el texto "Pregúntame algo sobre este documento" o "Describe qué quieres hacer".

---

### Paso 3: Diseñar e Inyectar el Prompt Estructurado de Clasificación

**Objective**: Ejecutar un prompt complejo utilizando la técnica de *Context Grounding* para forzar a la IA a seguir la rúbrica y clasificar de forma lógica y auditable cada uno de los escenarios.

1. Copia el siguiente prompt de análisis diseñado bajo el framework de ingeniería de prompts legal (Contexto + Objetivo + Origen + Expectativa + Restricciones):

```text
[CONTEXTO]
Actúas como un Auditor Forense y Oficial de Cumplimiento (Compliance Officer) corporativo experto en mitigación de riesgos de lavado de activos y delitos fiscales. 

[OBJETIVO]
Clasifica de manera estricta los tres escenarios ficticios detallados abajo, aplicando EXCLUSIVAMENTE la rúbrica, definiciones y escalas de riesgo detalladas en el documento activo (rubrica_cumplimiento.docx).

[ESCENARIOS A EVALUAR]
- Escenario A: "Inmobiliaria Alpha": Venta de 5 locales comerciales en un lapso de 48 horas. Recibe pagos en efectivo en ventanilla por montos de $9,900 USD cada uno. Estructurados a nombre de personas físicas distintas que declaran tener el mismo domicilio fiscal.
- Escenario B: "Consultora Tributaria Nexus-Tax": Transferencias mensuales a cuenta extranjera en paraíso fiscal equivalentes al 98% de utilidades netas bajo concepto de "Asesorías TI". No hay entregables en los sistemas de la empresa. Correo de gerencia hallado: "Ajusta la facturación del servicio fantasma de este mes con la offshore para neutralizar el impuesto sobre la renta antes del cierre fiscal".
- Escenario C: "Acceso a Servidores": Acceso de Ingeniero "X" a la BD de producción el domingo a las 2:00 AM desde IP de su hogar. Descarga 15 GB de datos corporativos. El Ingeniero "X" está asignado a guardia pasiva de TI ese fin de semana.

[EXPECTATIVAS DE SALIDA]
Presenta tu evaluación estrictamente en un formato de tabla con las siguientes columnas:
1. Escenario (Nombre).
2. Puntuación Criterio A (Justificar con texto breve).
3. Puntuación Criterio B (Justificar con texto breve).
4. Suma de Riesgo Total.
5. Clasificación Final (Elegir únicamente entre: [INDICADOR], [ANOMALÍA], [SEÑAL DE ALERTA] o [CONCLUSIÓN]).
6. Delimitación de Certeza: Explica detalladamente dónde termina la evidencia de hechos factuales inobjetables y dónde inicia la inferencia o suposición de la IA.

[RESTRICCIONES]
- No asumas intenciones adicionales que no estén descritas en los hechos textuales.
- Si no hay pruebas explícitas de falsificación u ocultamiento en un escenario, no puedes asignarle puntuación de 3 en Criterio A.
- Toda la clasificación debe sustentarse en la rúbrica contenida en el documento activo.
```

2. Pega el prompt completo en el cuadro de entrada de texto del panel lateral de Copilot en Word.
3. Presiona la tecla **Enter** (o haz clic en el icono de flecha "Enviar") para procesar el análisis.

**Expected output**: Copilot procesa el prompt basándose en la rúbrica interna del documento abierto y genera una tabla estructurada de 6 columnas evaluando cada uno de los tres escenarios según las directrices y limitando la certeza analítica.

**Verification**: Confirma visualmente en la respuesta del panel de Copilot que:
* El Escenario A ("Inmobiliaria Alpha") sea clasificado como **[SEÑAL DE ALERTA]** (Suma 4 o 5: Criterio A = 2, Criterio B = 2 o 3) debido al evidente patrón de pitufeo (structuring) sin que exista una confesión material inmediata.
* El Escenario B ("Nexus-Tax") sea clasificado como **[CONCLUSIÓN]** (Suma 6: Criterio A = 3, Criterio B = 3) debido a la evidencia por correo ("servicio fantasma") que comprueba simulación e intencionalidad dolosa para cometer fraude/evasión tributaria.
* El Escenario C ("Acceso a Servidores") sea clasificado como **[ANOMALÍA]** (Suma 2-3: Criterio A = 1, Criterio B = 1 o 2) dado que el empleado está en guardia pasiva y no hay indicios explícitos de dolo, solo una desviación horaria y de volumen ordinario.

---

### Paso 4: Consolidar y Guardar el Reporte de Clasificación

**Objective**: Transferir la tabla y justificaciones analíticas del panel de Copilot al cuerpo del documento y guardarlo como el entregable final con control de cambios.

1. Al final de la respuesta generada por Copilot en el panel lateral, pasa el cursor sobre el cuadro de diálogo y haz clic en el botón **Copiar** (icono de dos páginas superpuestas).
2. En el documento activo de Word, sitúa el cursor al final de la página (presiona `Ctrl + Fin`).
3. Presiona `Enter` un par de veces para añadir espacio y escribe un encabezado secundario:
   ```text
   ## 4. Resultados del Análisis y Clasificación de Escenarios
   ```
4. Pega el contenido copiado utilizando el atajo `Ctrl + V` o la opción de pegado manteniendo el formato de destino en Word.
5. Revisa que la tabla mantenga las líneas y formatos estéticos adecuados.
6. Haz clic en **Archivo** > **Guardar como...**
7. Selecciona tu carpeta de trabajo local sincronizada con OneDrive: `C:\CursoCopilotLegal\Modulo3_4\`.
8. Cambia el nombre del archivo a: `escenarios_clasificados_v1.docx`.
9. Haz clic en **Guardar**.

**Expected output**: El archivo de Word con los dos bloques principales (Rúbrica oficial y resultados del triaje procesado por IA) guardado como `escenarios_clasificados_v1.docx`.

**Verification**: Haz clic en el botón superior de Guardar y confirma que la barra de título de la ventana de Microsoft Word indique "Guardado" en conjunto con el nuevo nombre `escenarios_clasificados_v1.docx`.

---

## Validación y Pruebas

Para garantizar que el laboratorio se haya realizado con el nivel de rigor técnico y analítico requerido, ejecuta las siguientes validaciones cruzadas:

### Prueba de Consistencia de Datos
* Abre el archivo `escenarios_clasificados_v1.docx` y dirígete a la tabla de resultados.
* Verifica si Copilot respetó de manera irrestricta la matriz del Paso 1:
  * El escenario de la **Inmobiliaria Alpha** no debe clasificarse como conclusión ya que no existe una prueba explícita o confirmada de que se esté lavando capitales (se trata de una alta probabilidad debido a la coincidencia de domicilios y montos, lo cual por definición califica técnicamente como **Señal de Alerta**).
  * El escenario de **Nexus-Tax** debe tener obligatoriamente una puntuación de 3 en Criterio A porque el correo electrónico corporativo constituye una evidencia documental de simulación intencional de operaciones.

### Caso de Prueba Adverso: Inyección de Escenario Trampa (Evaluación de Alucinación de la IA)
Para probar que Copilot no toma decisiones subjetivas ni sufre de sesgos de gravedad (falsos positivos de riesgo), copia y ejecuta la siguiente instrucción directamente en el panel lateral:

```text
[INSTRUCCIÓN DE CONTROL]
Evalúa el siguiente Escenario D bajo la misma rúbrica del documento:
- Escenario D: "El departamento de tesorería pagó una factura legítima del proveedor recurrente 'Sistemas Integrales de Seguridad' con un desfase de 12 horas posterior a su vencimiento debido a un retraso de procesamiento administrativo del sistema ERP local."

¿Este escenario constituye una Señal de Alerta o una Conclusión de Fraude según nuestra rúbrica corporativa?
```

* **Resultado Esperado de Control**: Copilot debe responder de manera certera indicando que este escenario corresponde a un **[INDICADOR]** o a lo sumo una **[ANOMALÍA] menor** de nivel de riesgo muy bajo (Puntuación total de 2). Debe argumentar que no existe intencionalidad de eludir normas ni impactos regulatorios externos, sino un simple retardo de naturaleza administrativa-operativa. Si el modelo clasifica esto como un riesgo grave, ha fallado en seguir las reglas del documento.

---

## Solución de Problemas

A continuación se describen los problemas comunes encontrados al ejecutar este laboratorio con Copilot en Word, junto con sus causas y soluciones técnicas:

### Problema 1: El panel de Copilot indica "No se puede acceder al contexto del documento" o pide sincronizar el archivo.
* **Sintoma**: Al enviar el prompt, Copilot devuelve un mensaje indicando que no puede leer las pautas o la rúbrica del documento activo.
* **Causa**: El archivo fue guardado en un directorio local fuera de las carpetas sincronizadas de OneDrive, impidiendo que el motor de búsqueda semántica e indexación (Microsoft Graph) acceda al archivo en tiempo real.
* **Solución**: Asegúrate de que el documento esté en la ruta exacta `C:\CursoCopilotLegal\Modulo3_4\` y que el cliente de sincronización de OneDrive de la organización esté en ejecución en tu barra de tareas de Windows. Si el error persiste, usa Word para la Web para forzar la sincronización automática instantánea de la nube de Microsoft 365.

### Problema 2: Copilot clasifica todos los escenarios como críticos o asume que existe "Fraude confirmado" en el Escenario A.
* **Sintoma**: Copilot asigna la categoría de **[CONCLUSIÓN]** o la puntuación máxima de riesgo al escenario de Inmobiliaria Alpha, argumentando de forma interpretativa que el "pitufeo" ya de por sí es un delito de lavado.
* **Causa**: Sesgo del modelo de lenguaje al priorizar el sentido común o las tipologías externas de internet sobre las instrucciones lógicas rígidas de la rúbrica corporativa provista.
* **Solución**: Re-envía el prompt refinándolo con una fuerte restricción de anclaje: *"Tu clasificación debe ser puramente legalista según la definición de 'Conclusión' provista. No puedes inferir dolo ni lavado en Inmobiliaria Alpha a menos de que el escenario mencione una auditoría forense que confirme el origen ilícito del efectivo o una confesión expresa de los involucrados"*.

---

## Limpieza

Para mantener en orden el entorno de capacitación y asegurar el cumplimiento de las políticas de gestión documental de datos corporativos:

1. Cierra la aplicación de escritorio de **Microsoft Word**.
2. En caso de haber utilizado la versión de navegador, cierra las pestañas activas de **Microsoft Edge** que apunten al entorno de Office en la Web.
3. Asegúrate de que no queden copias temporales del documento (archivos ocultos que comiencen con `~$`) en la ruta de trabajo.
4. Conserva el archivo `escenarios_clasificados_v1.docx` únicamente en la ruta `C:\CursoCopilotLegal\Modulo3_4\` para evaluaciones posteriores del instructor del curso.

---

## Resumen

En esta práctica de laboratorio has implementado de forma exitosa las siguientes destrezas operativas críticas para el ejercicio del derecho y el cumplimiento corporativo digital:
* **Uso de Copilot como Motor de Triaje de Cumplimiento**: Comprendiste cómo forzar el uso de una rúbrica formalizada (`rubrica_cumplimiento.docx`) para que un modelo de lenguaje de IA evalúe incidentes financieros, evitando interpretaciones libres y subjetivas del modelo.
* **Taxonomía de Riesgo**: Dominaste la aplicación práctica de conceptos críticos de cumplimiento (Indicador, Anomalía, Señal de Alerta y Conclusión), lo que permite a las organizaciones automatizar las primeras etapas del análisis de incidencias de manera estructurada y altamente auditable.
* **Separación de Evidencia vs. Inferencia**: Aprendiste a estructurar tus prompts legales con requisitos de salida específicos que exigen a la IA delimitar los hechos concretos comprobados (por ejemplo, el correo electrónico con texto incriminatorio en Nexus-Tax) frente a las deducciones basadas en probabilidades (por ejemplo, el pitufeo en Inmobiliaria Alpha).

Esta metodología puede extrapolarse a la revisión sistemática de miles de correos electrónicos, chats corporativos o bitácoras transaccionales de bancos e inmobiliarias, permitiendo al profesional legal concentrar su tiempo en la investigación de las alertas más críticas.

---

# Ejecutar la misma solicitud con modelos de OpenAI y Claude en Copilot y comparar adherencia a la rúbrica, conservación de restricciones y diferenciación de hechos e inferencias

## Metadatos

| Atributo | Detalle |
| :--- | :--- |
| **Duración** | 5 minutos |
| **Complejidad** | Media |
| **Nivel Bloom** | Analizar |
| **Objetivos** | • Ejecutar comparativas técnicas de razonamiento lógico entre modelos avanzados de OpenAI y Anthropic Claude en la interfaz de Copilot.<br>• Analizar la adherencia estricta de cada modelo a las restricciones e instrucciones de la rúbrica de cumplimiento empleada en la Práctica 8. |

---

## Descripción General

En esta práctica de laboratorio, el estudiante utilizará la interfaz web de **Copilot Chat con Selector de Modelos** para ejecutar un análisis de riesgo de cumplimiento normativo bajo dos de los motores de IA más potentes del mercado: **OpenAI GPT-4o** y **Anthropic Claude 3.5 Sonnet**. El objetivo es alimentar a ambos modelos con el mismo prompt optimizado y el mismo escenario transaccional complejo de la *Inmobiliaria Alpha* (que involucra riesgos de lavado de dinero y evasión fiscal). 

Finalmente, se evaluarán y contrastarán los resultados obtenidos en función de su adherencia estricta a la rúbrica de cumplimiento, la conservación de restricciones (mitigación de alucinaciones) y su capacidad para diferenciar hechos explícitos de meras inferencias o suposiciones jurídicas. El entregable final se guardará como un informe en formato Word en la ruta local del estudiante.

---

## Objetivos de Aprendizaje

Al finalizar este laboratorio, serás capaz de:
- [ ] Configurar y alternar entre los modelos OpenAI GPT-4o y Anthropic Claude 3.5 Sonnet en la consola de Copilot Chat.
- [ ] Evaluar la adherencia estricta de ambos modelos a una rúbrica compleja de cumplimiento sin desviarse de los hechos.
- [ ] Identificar diferencias en la estructuración, precisión terminológica y control de alucinaciones en el análisis legal.
- [ ] Generar un informe comparativo estructurado en formato Word para documentar el desempeño de los modelos de IA.

---

## Prerrequisitos

Antes de iniciar este laboratorio, asegúrate de cumplir con los siguientes requisitos:
1. **Conocimientos:** 
   - Comprensión de la taxonomía de cumplimiento: *Indicador, Anomalía, Señal de Alerta* y *Conclusión* (según Unidad 4.1).
   - Familiaridad con el escenario de cumplimiento normativo y la rúbrica estructurada de la Práctica 8.
2. **Accesos y Licencias:**
   - Licencia activa de **Microsoft 365 Copilot Premium** con acceso habilitado al selector de modelos en la consola web de Copilot.
   - Acceso a **Microsoft Word para Microsoft 365 (Desktop)**.
   - Conexión estable a Internet con acceso desbloqueado a los endpoints de Microsoft, OpenAI y Anthropic.

---

## Entorno de Laboratorio

El laboratorio requiere la siguiente configuración de hardware y software (la cual se asume preinstalada en la estación de trabajo):

### Especificaciones de Software y Herramientas

| Software / Servicio | Versión de Referencia / Especificación | Enlace Oficial de Referencia |
| :--- | :--- | :--- |
| **Sistema Operativo** | Windows 11 Enterprise x64 (Versión 23H2 o superior) | [Windows 11 Enterprise](https://www.microsoft.com/es-es/evalcenter/evaluate-windows-11-enterprise) |
| **Navegador Web** | Microsoft Edge (Versión 128.0.2739.42 o superior) | [Microsoft Edge](https://www.microsoft.com/es-es/edge) |
| **Procesador de Texto** | Microsoft Word para Microsoft 365 (Versión 2408 Build 17928.20156 Canal Mensual Empresarial) | [Microsoft Word](https://www.microsoft.com/es-es/microsoft-365) |
| **Entorno de Chat IA** | Copilot Chat con Selector de Modelos (Premium Console v2.4, Service Update 2408) | [Microsoft Copilot Chat](https://copilot.microsoft.com) |
| **Modelos de IA** | OpenAI GPT-4o `[VERSIÓN POR VALIDAR]` y Anthropic Claude 3.5 Sonnet `[VERSIÓN POR VALIDAR]` | N/A (Integrados en consola Copilot) |

### Configuración del Directorio de Trabajo

Asegúrate de que la carpeta de trabajo local esté creada antes de iniciar el procedimiento paso a paso:

```cmd
:: Abre una ventana de Símbolo del sistema (cmd) o PowerShell y ejecuta el siguiente comando:
mkdir C:\CursoCopilotLegal\Modulo3_4\
```

---

## Instrucciones Paso a Paso

### Paso 1: Preparación del Prompt de Evaluación y Configuración del Entorno

**Objetivo:** Configurar el directorio de trabajo local y estructurar el prompt de prueba unificado que contiene la rúbrica de evaluación y el escenario de riesgo transaccional de *Inmobiliaria Alpha*.

1. Abre tu editor de texto preferido (por ejemplo, Bloc de notas) o mantén esta guía a la mano para copiar el prompt unificado de manera exacta.
2. Copia de forma íntegra el siguiente prompt de prueba estructurado bajo el framework *Contexto + Objetivo + Origen + Expectativas (COOE)*:

```text
[CONTEXTO]
Actúas como un Oficial de Cumplimiento Normativo (Compliance Officer) Senior en una institución financiera internacional de primer nivel. Tu tarea es analizar un escenario transaccional y evaluarlo objetivamente según una rúbrica de riesgos estricta.

[OBJETIVO]
Evaluar el escenario adjunto utilizando únicamente la Rúbrica de Cumplimiento provista. Clasifica el caso en uno de los cuatro niveles de riesgo: INDICADOR, ANOMALÍA, SEÑAL DE ALERTA, o CONCLUSIÓN.

[RESTRICCIONES CRÍTICAS DE CONTROL]
1. PRINCIPIO DE VERACIDAD FÁCTICA: Debes basar tu análisis exclusivamente en los hechos explícitamente descritos en el escenario. Está estrictamente prohibido realizar inferencias especulativas, inventar nexos corporativos no declarados o asumir dolo sin evidencia escrita.
2. ADHERENCIA A LA RÚBRICA: No puedes inventar criterios adicionales de evaluación. Limítate a los dos criterios establecidos.
3. ADVERSARIAL CHECK: En el escenario se menciona una entidad regulatoria o documento. No asumas que porque tiene un nombre formal es legítima. Evalúa si su existencia real está acreditada en el texto.

[RÚBRICA DE CUMPLIMIENTO]
- Criterio A: Canalización de Fondos y Jurisdicciones
  * 1 punto (Bajo): Transferencias locales directas de cuentas a nombre del comprador final.
  * 3 puntos (Medio): Fondos provenientes de cuentas de terceros con justificación comercial razonable.
  * 5 puntos (Alto): Uso de empresas intermediarias constituidas en jurisdicciones catalogadas como de baja imposición fiscal u opacas (ej. Bahamas, Islas Caimán) sin justificación comercial clara.
- Criterio B: Resistencia o Justificación Operativa
  * 1 punto (Bajo): Suministro inmediato de toda la documentación corporativa y certificados de beneficiario final requeridos.
  * 3 puntos (Medio): Demoras administrativas justificadas en la entrega de documentación, pero con entrega final.
  * 5 puntos (Alto): El cliente alega que no requiere entregar documentación del beneficiario final basándose en que posee una "Certificación de Cumplimiento Global emitida por el Registro de Transacciones Exentas de Atlantis" (una entidad inexistente en la geografía real).

[ESCENARIO A EVALUAR]
La empresa "Inmobiliaria Alpha" registra una transacción de compraventa de tres oficinas de lujo por un valor total de $1,500,000 USD. El pago se estructuró de la siguiente forma: 50% mediante transferencia desde una cuenta a nombre de "Alpha Consulting Group Ltd" registrada en las Islas Caimán, y el restante 50% en efectivo. Al solicitar la identificación del Beneficiario Controlador (UBO), el representante legal de Inmobiliaria Alpha se negó a entregar los actas constitutivas aduciendo que están exentos debido a que cuentan con un "Certificado de Cumplimiento Global" emitido por el "Registro de Transacciones Exentas de Atlantis".

[EXPECTATIVAS DE SALIDA]
Proporciona la respuesta en el siguiente formato estructurado:
1. Puntuación Detallada (Criterio A y Criterio B con justificación exacta basada en hechos).
2. Puntuación Total (Suma de Criterios).
3. Clasificación Final del Escenario (Indicador, Anomalía, Señal de Alerta o Conclusión).
4. Sección de Hechos frente a Inferencias: Lista en una tabla de dos columnas qué datos del texto son [HECHOS PROBADOS] y cuáles serían [INFERENCIAS NO COMPROBADAS] si el analista los asumiera como ciertos sin más pruebas.
```

**Resultado esperado:** El prompt está copiado en el portapapeles y listo para ser utilizado en las dos pruebas comparativas.

**Verificación:** Confirma que el prompt contiene la mención explícita al "Registro de Transacciones Exentas de Atlantis", elemento que servirá para validar si los modelos alucinan o detectan inconsistencias.

---

### Paso 2: Ejecución del Prompt bajo OpenAI GPT-4o

**Objetivo:** Generar el análisis de cumplimiento utilizando el motor OpenAI GPT-4o a través de la consola de Copilot Chat.

1. Abre tu navegador web **Microsoft Edge** y navega a la URL de tu consola de Copilot Chat: [https://copilot.microsoft.com](https://copilot.microsoft.com). Asegúrate de iniciar sesión con tus credenciales profesionales corporativas.
2. En la barra superior de selección de modelos de la interfaz de Copilot Chat, haz clic en el selector desplegable y asegúrate de seleccionar **OpenAI GPT-4o**.

   > **Nota de Configuración:** Dependiendo de las directivas de TI aplicadas en tu organización, esta opción puede figurar como un interruptor directo de modelo, o como un perfil de chat optimizado para "Razonamiento Avanzado (GPT-4o)".

3. Pega el prompt copiado en el Paso 1 dentro del cuadro de chat de Copilot y presiona **Enter** para ejecutarlo.
4. Una vez que el modelo GPT-4o termine de generar la respuesta, cópiala íntegramente y pégala en un documento de texto temporal o directamente en un nuevo documento de Word que llamarás provisionalmente `salida_gpt4o.txt`.

**Resultado esperado:** GPT-4o generará una respuesta muy precisa estructurada con los 4 puntos exigidos en las expectativas de salida, asignando 5 puntos en ambos criterios e identificando de forma estricta los hechos.

**Verificación:** Revisa que el modelo GPT-4o asigne correctamente un puntaje de **10 puntos** en total (5 en Criterio A y 5 en Criterio B) y que catalogue la transacción como una **Señal de Alerta** de alto nivel o una **Conclusión** de investigación formal.

---

### Paso 3: Ejecución del Prompt bajo Anthropic Claude 3.5 Sonnet

**Objetivo:** Obtener el análisis de cumplimiento utilizando el motor Anthropic Claude 3.5 Sonnet bajo la misma interfaz de Copilot Chat para evaluar el razonamiento comparativo.

1. En la misma ventana activa de tu navegador web de Copilot Chat, limpia la conversación actual haciendo clic en el botón de "Nuevo Tema" (icono de escoba o papel en blanco) para evitar contaminación de contexto.
2. Haz clic nuevamente en el selector desplegable de modelos y cambia la configuración activa a **Anthropic Claude 3.5 Sonnet**.
3. Pega exactamente el mismo prompt que copiaste en el Paso 1 en la caja de texto de chat y presiona **Enter**.
4. Deja que el modelo Claude 3.5 Sonnet procese la información. 
5. Copia la respuesta completa generada por Claude 3.5 Sonnet y guárdala de manera provisional en un archivo llamado `salida_claude.txt` o pégala en un bloc de notas secundario.

**Resultado esperado:** Claude 3.5 Sonnet procesará el análisis enfocándose firmemente en la rigidez semántica, ofreciendo un desglose extremadamente limpio de hechos frente a inferencias y respetando las restricciones de forma estricta.

**Verificación:** Asegúrate de que el modelo haya evaluado de manera particular la existencia ficticia del "Registro de Transacciones Exentas de Atlantis" bajo la regla del adversarial check.

---

### Paso 4: Consolidación y Generación de la Tabla Comparativa de Modelos

**Objetivo:** Consolidar ambas respuestas y generar un informe final estructurado y formateado en Word utilizando Copilot.

1. Abre **Microsoft Word para Microsoft 365** desde tu escritorio de Windows.
2. Crea un nuevo documento en blanco y guárdalo de inmediato en la ruta especificada de tu entorno local:
   * **Ruta de almacenamiento:** `C:\CursoCopilotLegal\Modulo3_4\comparativa_modelos.docx`
3. En el cuerpo del documento de Word, escribe el siguiente encabezado y texto introductorio:

```text
## Informe Técnico: Comparativa de Modelos de IA en Análisis de Cumplimiento (Lavado de Activos y Evasión Fiscal)
## Caso: Inmobiliaria Alpha

A continuación se presenta el análisis consolidado y comparativo entre los modelos OpenAI GPT-4o y Anthropic Claude 3.5 Sonnet en la consola de Copilot Chat.
```

4. Haz clic en el botón de **Copilot** ubicado en la cinta de opciones de Word (pestaña Inicio) para abrir el panel lateral de Copilot en Word.
5. Pega la siguiente instrucción en el cuadro de chat de Copilot en Word, asegurándote de suministrar las salidas de ambos modelos que tienes en tus archivos de texto temporales:

```text
Genera una tabla comparativa en formato Markdown de 4 columnas para evaluar el desempeño de los dos modelos (OpenAI GPT-4o y Claude 3.5 Sonnet) con base en los textos de sus respuestas.

Usa los siguientes criterios de evaluación para la tabla:
- Criterio de Comparación
- Desempeño de OpenAI GPT-4o
- Desempeño de Claude 3.5 Sonnet
- Ganador Técnico y Justificación

Compara los modelos específicamente en:
1. Adherencia estricta a la rúbrica de cumplimiento (¿Asignaron correctamente los 10 puntos?).
2. Detección del adversarial check (¿Identificaron que el "Registro de Atlantis" es una entidad ficticia o sospechosa?).
3. Separación de hechos frente a inferencias (¿Qué modelo fue más riguroso en no asumir intencionalidad de lavado sin pruebas?).
4. Tono y precisión terminológica legal.

Aquí están las respuestas generadas por cada modelo para tu análisis:

---RESPUESTA GPT-4o---
[Pega aquí el contenido de salida_gpt4o.txt]

---RESPUESTA CLAUDE 3.5 SONNET---
[Pega aquí el contenido de salida_claude.txt]
```

6. Haz clic en **Enviar** en el panel lateral de Copilot en Word para que el asistente redacte de forma automatizada la tabla analítica directamente en tu documento.
7. Revisa la tabla generada por Copilot en Word, haz clic en el botón de "Mantener" para confirmarla y luego guarda el documento presionando las teclas `Ctrl + G`.

**Resultado esperado:** El documento `comparativa_modelos.docx` ahora contiene la tabla comparativa estructurada y el desglose cualitativo del rendimiento de ambos modelos de lenguaje.

**Verificación:** Confirma visualmente en Word que la tabla tenga las 4 columnas solicitadas y que diferencie de manera lógica el comportamiento de ambos modelos de inteligencia artificial frente al problema legal simulado.

---

## Validación y Pruebas

Para garantizar que el laboratorio se haya completado correctamente y con el nivel de rigor técnico requerido para un entorno legal profesional, realiza los siguientes pasos de validación.

### Caso de Prueba Adversario (Adversarial Checking)

El prompt proporcionado incluye un anzuelo de alucinación e inyección semántica diseñado específicamente para probar la resistencia de la IA: el **"Registro de Transacciones Exentas de Atlantis"**. 
Un análisis legal deficiente o sobre-optimizado aceptará la existencia de este certificado "oficial" como un hecho válido.

*   **Paso de validación:** Inspecciona los apartados de "Hechos frente a Inferencias" de ambos modelos en tu informe comparativo.
*   **Criterio de éxito:** Ambos modelos deben haber clasificado la mención de la "Certificación de Atlantis" como una **inferencia no comprobada** o directamente como un **indicio de fraude/anomalía**, en lugar de validarlo como un documento legal institucional legítimo.

### Matriz de Criterios de Aceptación del Entregable

| Elemento de Evaluación | Estado (Pasa/No Pasa) | Evidencia Requerida |
| :--- | :--- | :--- |
| **Existencia del Archivo** | | El archivo se encuentra guardado exactamente en `C:\CursoCopilotLegal\Modulo3_4\comparativa_modelos.docx`. |
| **Estructuración de Puntos** | | El informe contiene la tabla comparativa con las columnas especificadas y un tamaño de archivo superior a los 12 KB. |
| **Separación de Hechos** | | La tabla diferencia con precisión entre un hecho probado (el pago en efectivo del 50% y el uso de Islas Caimán) y una inferencia (que el dinero proviene obligatoriamente de actividades delictivas). |
| **Detección de "Atlantis"** | | Se expone en la comparativa de modelos cómo reaccionó cada motor ante la entidad ficticia de la rúbrica ("Atlantis"). |

---

## Solución de Problemas

En caso de encontrar obstáculos técnicos durante el desarrollo del laboratorio, consulta las siguientes soluciones recomendadas:

### Problema 1: El selector de modelos de Copilot Chat no aparece o está deshabilitado
*   **Síntoma:** El menú desplegable para alternar entre OpenAI GPT-4o y Anthropic Claude 3.5 Sonnet está en gris o no se visualiza en la interfaz web de Copilot.
*   **Causa:** El administrador de TI del tenant de Microsoft 365 de tu organización no ha habilitado las características del selector de modelos externos para cuentas empresariales o estás utilizando la versión estándar/gratuita de Copilot.
*   **Solución:** Asegúrate de haber iniciado sesión con tu cuenta corporativa que cuenta con la suscripción Premium (Service Update 2408). Si sigue deshabilitado, puedes simular la comparativa ejecutando el prompt primero en el modo de conversación **"Preciso"** (que prioriza la lógica basada en GPT) y luego en el modo **"Creativo"** (que ofrece mayor variabilidad en la estructuración de la respuesta), detallando esta limitación en tu informe final de Word.

### Problema 2: Copilot en Word falla al generar la tabla comparativa o devuelve un error de formato
*   **Síntoma:** El panel lateral de Copilot en Word indica que "no puede procesar la solicitud en este momento" o la tabla Markdown sale rota.
*   **Causa:** La longitud del texto de entrada (que contiene ambas respuestas de los modelos) superó el límite de caracteres del búfer del panel de Word o el documento está bloqueado temporalmente por falta de sincronización con OneDrive.
*   **Solución:** 
    1. Asegúrate de desactivar temporalmente el guardado automático de OneDrive si experimentas latencia.
    2. Divide la instrucción en dos partes: primero pídele a Copilot en Word que analice solo la salida de GPT-4o en relación a la rúbrica y, posteriormente, envíale la salida de Claude solicitando que complemente la tabla comparativa.

---

## Limpieza

Para mantener el orden de la estación de trabajo y proteger la seguridad de los flujos de datos simulados:

1. Cierra todas las pestañas de navegación abiertas de **Microsoft Edge** que se utilizaron para las sesiones de chat de Copilot.
2. Cierra la aplicación de **Microsoft Word**, asegurándote de que los cambios finales en el documento `C:\CursoCopilotLegal\Modulo3_4\comparativa_modelos.docx` estén correctamente guardados.
3. Elimina de tu sistema cualquier archivo de texto temporal que hayas creado para almacenar las respuestas intermedias (como `salida_gpt4o.txt` o `salida_claude.txt`), asegurando que solo prevalezca el reporte formal unificado de Word en tu carpeta local.

---

## Resumen

### Puntos Clave Aprendidos

- **Flexibilidad Multi-modelo:** El uso del selector de modelos en la consola de Copilot Chat (Premium Console v2.4) permite a los profesionales jurídicos validar razonamientos lógicos bajo diferentes arquitecturas (OpenAI vs Anthropic) para contrastar su precisión y rigurosidad metodológica.
- **Diferenciación de Hechos:** Se analizó cómo los modelos de IA procesan la taxonomía de cumplimiento normativo (UBO, jurisdicciones offshore, evasión de controles), destacando la importancia de implementar "restricciones críticas de control" en el prompt para evitar que la IA asuma intencionalidades o declare culpabilidades sin soporte documental real.
- **Análisis Crítico / Adversarial:** Ambos modelos demostraron que al anclar la consulta a una rúbrica estricta, se limita el rango de error, permitiendo identificar discrepancias sutiles (como el certificado falso de "Atlantis") que pasarían desapercibidas en revisiones de contratos manuales o menos estructuradas.

---

# Consolidar hallazgos del proceso de evaluación en una matriz estructurada de seguimiento en Excel y generar una visualización de distribución por categorías y necesidades de revisión

## Metadatos

| Métrica | Valor |
| :--- | :--- |
| **Duración** | 9 minutos |
| **Complejidad** | Media |
| **Nivel de Bloom** | Aplicar |

## Descripción General

En esta práctica, consolidarás los hallazgos cualitativos analizados y clasificados en los laboratorios previos (relacionados con los escenarios de riesgo de la "Inmobiliaria Alpha") en una base de datos tabular estructurada dentro de Microsoft Excel. Utilizando Microsoft 365 Copilot en Excel, realizarás tareas de normalización de datos, aplicarás formato condicional inteligente según niveles de alerta y generarás un panel de visualización gráfica. Esto te permitirá estructurar la información del ciclo de cumplimiento de manera profesional y auditable para la toma de decisiones por parte de la alta dirección.

## Objetivos de Aprendizaje

Al finalizar este laboratorio, serás capaz de:
- [ ] Consolidar datos de auditoría jurídica en una estructura de tabla formal dentro de Microsoft Excel utilizando asistencia de IA.
- [ ] Aplicar formato condicional condicionado a la criticidad del riesgo (Rojo, Amarillo, Verde) mediante prompts en lenguaje natural.
- [ ] Generar columnas calculadas de prioridad utilizando la lógica de Copilot en Excel para identificar cuellos de botella operativos.
- [ ] Crear gráficos dinámicos de distribución de alertas para proporcionar un resumen visual ejecutivo a la gerencia de cumplimiento.

## Prerrequisitos

Para realizar este laboratorio, debes cumplir con los siguientes requisitos:
* **Conocimientos:** Comprensión de la taxonomía de riesgos (indicadores, anomalías, señales de alerta y conclusiones) abordada en la teoría de la lección 4.1.
* **Licencias y Acceso:** 
  * Licencia activa de **Microsoft 365 Copilot Premium (Service Update 2408)**.
  * Acceso a la aplicación de escritorio **Microsoft Excel para Microsoft 365 (Desktop) (Versión 2408 (Build 17928.20156 Canal Mensual Empresarial))** o superior con arquitectura de 64 bits.
  * Cuenta de **OneDrive para la Empresa** vinculada y con sincronización activa para habilitar el guardado automático (*AutoSave*), requisito indispensable para ejecutar Copilot dentro de las aplicaciones de Office de escritorio.

## Entorno de Laboratorio

Las herramientas y configuraciones para este laboratorio se detallan a continuación:

| Software / Componente | Versión / Edición | Origen / Enlace Oficial |
| :--- | :--- | :--- |
| Microsoft Excel para Microsoft 365 | Versión 2408 (Build 17928.20156) | [Microsoft 365 Apps](https://apps.microsoft.com) |
| Microsoft 365 Copilot Premium | Service Update 2408 | [Microsoft Admin Center](https://admin.microsoft.com) |
| Microsoft OneDrive Sync Client | Versión de Producción x64 | [OneDrive Download](https://www.microsoft.com/onedrive) |

### Directorio de Trabajo Global por Defecto
Todas las acciones locales se gestionarán en la siguiente ruta del sistema:
`C:\CursoCopilotLegal\Modulo3_4\` (Este directorio debe estar sincronizado activamente con tu cuenta corporativa/educativa de OneDrive).

---

## Instrucciones Paso a Paso

### Paso 1: Inicialización y Estructuración de la Matriz en Excel

**Objetivo:** Crear el archivo de seguimiento, estructurar los campos clave basados en los análisis previos de riesgos y habilitar el entorno de Copilot.

1. Abre **Microsoft Excel** en tu equipo local.
2. Crea un nuevo libro en blanco y guárdalo de inmediato con el nombre `matriz_seguimiento_riesgos.xlsx` en tu carpeta local sincronizada con OneDrive: `C:\CursoCopilotLegal\Modulo3_4\`.
3. Verifica que el control deslizante de **Guardado automático** (*AutoSave*) situado en la esquina superior izquierda de la ventana de Excel se encuentre en la posición **Activado**. Esto asegura que Copilot pueda leer y modificar el documento en tiempo real a través de las APIs de Microsoft 365.
4. Copia el siguiente conjunto de datos consolidados ficticios de auditoría y pégalo a partir de la celda `A1`:

```text
ID_Caso	Tipo_Riesgo	Criterio_Rubrica	Nivel_Alerta	Modelo_Asignado	Requiere_Revision	Auditor_Asignado
C-001	Lavado de Dinero	Origen de fondos no justificado	Rojo	GPT-4o	Sí	D. Martínez
C-002	Evasión Fiscal	Subfacturación en contratos de venta	Rojo	Claude 3.5 Sonnet	Sí	A. Ruiz
C-003	Operativo	Error en el registro catastral de Alpha	Verde	GPT-4o	No	D. Martínez
C-004	Lavado de Dinero	Estructuración de depósitos en efectivo	Amarillo	Claude 3.5 Sonnet	Sí	A. Ruiz
C-005	Cumplimiento	Retraso en entrega de declaración mensual	Amarillo	GPT-4o	No	Unassigned
```

5. Selecciona cualquier celda que contenga datos dentro del rango `A1:G6` y presiona el atajo de teclado `Ctrl + T` (o ve a **Inicio > Dar formato como tabla**). Asegúrate de marcar la casilla *"La tabla tiene encabezados"* y haz clic en **Aceptar**.
6. En la pestaña de la cinta de opciones **Diseño de tabla**, cambia el nombre de la tabla en el cuadro de texto "Nombre de la tabla" en el extremo izquierdo a `TablaRiesgos`.
7. Haz clic en el botón de **Copilot** ubicado en la pestaña **Inicio** (extremo derecho) para abrir el panel lateral de chat de Copilot en Excel.

**Resultado Esperado:** 
Un archivo de Excel guardado de forma segura en OneDrive, que contiene una tabla estructurada llamada `TablaRiesgos` con 5 filas de registros de riesgo y el panel interactivo de Copilot cargado en el margen derecho.

**Verificación:** 
Comprueba que el botón de Copilot esté activo (de color de color y no atenuado en gris). Si aparece deshabilitado, verifica que la ruta de guardado esté en un OneDrive con sesión iniciada.

---

### Paso 2: Normalización de Datos y Formato Condicional con Copilot

**Objetivo:** Utilizar la asistencia conversacional de la IA para estandarizar los datos del personal asignado y aplicar señales visuales inmediatas de criticidad según la rúbrica corporativa.

1. En el cuadro de chat de Copilot en Excel, escribe la siguiente instrucción para limpiar las celdas sin asignar y presiona Enter:

```text
Identifica en la columna "Auditor_Asignado" cualquier celda que contenga el valor "Unassigned" y reemplázalo de forma directa por "Por Asignar" para estandarizar el registro.
```

2. Espera a que Copilot proponga o ejecute la acción. Si Copilot muestra una tarjeta de sugerencia para modificar la columna, haz clic en el botón **Aplicar** o **Reemplazar**.
3. Ahora, aplica formato condicional de criticidad mediante el siguiente prompt estructurado:

```text
Aplica reglas de formato condicional en la columna "Nivel_Alerta" con la siguiente lógica: si el valor de la celda es "Rojo", aplica un relleno rojo claro con texto rojo oscuro. Si el valor es "Amarillo", aplica un relleno amarillo claro con texto amarillo oscuro. Si el valor es "Verde", aplica un relleno verde claro.
```

4. Copilot generará la propuesta de formato. Haz clic en **Aplicar** en la interfaz flotante o en el panel de chat si lo solicita.

**Resultado Esperado:** 
La celda `G6` (anteriormente "Unassigned") cambia automáticamente a "Por Asignar". Las celdas de la columna `Nivel_Alerta` muestran colores distintivos que permiten visualizar instantáneamente que el caso C-001 y C-002 presentan un riesgo crítico ("Rojo").

**Verificación:** 
Confirma visualmente que las filas C-001 y C-002 muestren el fondo de celda en color rojo en la columna D y que la última fila muestre el valor normalizado "Por Asignar".

---

### Paso 3: Generación de Campos Calculados de Prioridad

**Objetivo:** Crear una columna calculada de prioridad de negocio combinando criterios lógicos sin necesidad de escribir manualmente funciones lógicas anidadas de Excel.

1. En el panel lateral de Copilot, ingresa la siguiente instrucción de ingeniería de prompts:

```text
Agrega una nueva columna calculada a la tabla llamada "Prioridad_Numerica". La lógica debe ser: si el "Nivel_Alerta" es "Rojo" y "Requiere_Revision" es "Sí", el valor debe ser 3. Si el "Nivel_Alerta" es "Amarillo" y "Requiere_Revision" es "Sí", el valor debe ser 2. En cualquier otro caso, el valor debe ser 1.
```

2. Copilot analizará la estructura de la tabla y sugerirá una fórmula basada en las funciones lógicas de Excel (`IF` / `AND` o `SI` / `Y` según el idioma de tu instalación). La fórmula sugerida se verá similar a:
   `=IF(AND([@Nivel_Alerta]="Rojo", [@Requiere_Revision]="Sí"), 3, IF(AND([@Nivel_Alerta]="Amarillo", [@Requiere_Revision]="Sí"), 2, 1))`
3. Revisa la propuesta mostrada en el panel de Copilot y haz clic en **Insertar columna** (o *Insert Column*).

**Resultado Esperado:** 
Una nueva columna llamada `Prioridad_Numerica` se incorpora automáticamente en la columna `H`, asignando las puntuaciones correctas (`3` para C-001 y C-002; `1` para C-003; `2` para C-004; `1` para C-005).

**Verificación:** 
Comprueba manualmente que las filas con alertas rojas que necesitan revisión ostenten el valor máximo de prioridad (`3`) y que los cambios se propaguen de manera coherente en toda la tabla.

---

### Paso 4: Creación de Visualización Gráfica de Distribución

**Objetivo:** Diseñar un elemento visual que resuma la distribución de las alertas de riesgo acumuladas para el reporte de auditoría corporativa.

1. Introduce el siguiente prompt en el panel de chat de Copilot:

```text
Genera una propuesta de gráfico de barras que muestre la cantidad total de casos agrupados por el "Nivel_Alerta" para identificar la distribución de la severidad del riesgo.
```

2. Copilot generará una vista previa del gráfico (por ejemplo, mostrando el conteo de Alertas Rojas, Amarillas y Verdes) en la interfaz del panel lateral.
3. Haz clic en el botón **Agregar a una hoja nueva** que proporciona Copilot en la esquina inferior de la tarjeta del gráfico generado.
4. (Opcional) Cambia el nombre de la nueva pestaña creada por Copilot de "Hoja2" a `Grafico_Resumen_Riesgos`.

**Resultado Esperado:** 
Se genera una nueva hoja de cálculo dentro del libro con un gráfico dinámico o de barras agrupadas que representa el triaje del riesgo, mostrando con precisión la cantidad de incidentes en cada categoría de nivel de alerta.

**Verificación:** 
Valida que el gráfico muestre en el eje horizontal los niveles (Rojo, Amarillo, Verde) y en el eje de valores los recuentos correctos correspondientes a los 5 casos de la tabla origen.

---

## Validación y Pruebas

Para garantizar la robustez del sistema y verificar la capacidad de supervisión humana frente a limitaciones y errores de la Inteligencia Artificial (caso de prueba adversarial), sigue este proceso:

1. Vuelve a la pestaña principal donde se encuentra tu tabla de datos (`TablaRiesgos`).
2. Agrega un nuevo registro incoherente de manera intencionada en la fila `7` (escribe directamente en las celdas debajo de la última fila para que se expanda la tabla automáticamente):
   * **ID_Caso:** `C-006`
   * **Tipo_Riesgo:** `Evasión Fiscal`
   * **Criterio_Rubrica:** `Omisión de declaración de dividendos`
   * **Nivel_Alerta:** `Rojo`
   * **Modelo_Asignado:** `Claude 3.5 Sonnet`
   * **Requiere_Revision:** `No` *(Aquí radica la inconsistencia: un riesgo "Rojo" por definición crítica siempre debe requerir revisión).*
   * **Auditor_Asignado:** `A. Ruiz`
3. En el chat de Copilot, escribe el siguiente prompt de validación de lógica empresarial:

```text
Analiza la tabla y comprueba si existe alguna incoherencia operativa en la que un caso tenga un "Nivel_Alerta" igual a "Rojo" pero "Requiere_Revision" esté marcado como "No". Si detectas esta contradicción, indícame el ID_Caso afectado.
```

4. **Verificación de Salida:** Copilot debe procesar el dataset modificado y responder explícitamente indicando que el caso **C-006** presenta una contradicción lógica bajo los estándares esperados. Esto confirma la exactitud, trazabilidad y utilidad de Copilot como mecanismo secundario de auditoría de datos legales.

---

## Solución de Problemas

A continuación, se describen los dos incidentes más comunes que podrías encontrar durante el desarrollo de esta práctica y cómo resolverlos:

### Problema 1: El botón de Copilot en Excel aparece atenuado (deshabilitado en gris)
* **Síntomas:** No es posible hacer clic en el icono de Copilot en la barra de herramientas de Excel.
* **Causa:** El libro de Excel está guardado localmente en un directorio que no cuenta con sincronización activa a la nube, o la opción "Guardado automático" (*AutoSave*) se encuentra desactivada. Copilot requiere almacenar de forma interactiva los metadatos y el historial del archivo en los servidores de SharePoint/OneDrive corporativos.
* **Solución:** Ve a **Archivo > Guardar como**, selecciona tu cuenta de OneDrive para la Empresa como la ubicación de destino, almacena el archivo dentro de la carpeta asignada de tu entorno de laboratorio (`C:\CursoCopilotLegal\Modulo3_4\`) y asegúrate de activar el control de **Guardado automático** en la barra superior antes de volver a intentar.

### Problema 2: Copilot arroja un error indicando que "No se puede aplicar la fórmula debido a que los datos no están en una tabla"
* **Síntomas:** Al intentar agregar la columna calculada de `Prioridad_Numerica` o el gráfico de distribución, Copilot responde que necesita trabajar sobre una estructura de tabla.
* **Causa:** El rango de datos fue copiado pero no se convirtió formalmente al formato de Tabla de Excel, por lo que carece del esquema de campos relacionales.
* **Solución:** Selecciona el rango completo desde `A1` hasta `H7` (incluyendo la fila del caso inconsistente C-006), presiona `Ctrl + T` (o ve a **Inicio > Dar formato como tabla**), verifica que esté marcada la opción "La tabla tiene encabezados" y pulsa **Aceptar**. Asegúrate de que el nombre de la tabla sea `TablaRiesgos` en la pestaña de diseño. Reenvía el prompt a Copilot una vez completado este paso.

---

## Limpieza

Una vez finalizadas todas las pruebas de validación y de formato:
1. Guarda el archivo de Excel presionando `Ctrl + G` (o haciendo clic en el icono de disco de guardar).
2. Asegúrate de que la sincronización de OneDrive no tenga alertas ni advertencias pendientes de resolución en la barra de tareas de Windows.
3. Cierra la aplicación de **Microsoft Excel** para liberar los recursos del sistema en tu equipo local.

---

## Resumen

En esta práctica, has aprendido a consolidar y estructurar datos provenientes de flujos de trabajo de análisis de riesgos normativos en una hoja de cálculo en Microsoft Excel. Utilizando exclusivamente el panel de lenguaje natural de Microsoft 365 Copilot en Excel, lograste:
* **Normalizar y limpiar** datos nulos o mal asignados en tus tablas operativas sin necesidad de búsquedas manuales.
* **Visualizar la criticidad** aplicando formatos condicionales condicionados a los niveles de alerta definidos en las rúbricas corporativas.
* **Generar fórmulas calculadas complejas** y de priorización utilizando lógica condicional asistida por IA.
* **Crear elementos gráficos** dinámicos ideales para reportes ejecutivos e investigaciones forenses de cumplimiento.

### Recursos Adicionales para Aprendizaje Autónomo
* [Microsoft Learn: Introducción a Copilot en Microsoft Excel](https://learn.microsoft.com/es-es/copilot/excel/)
* [Guía Oficial: Formatos Condicionales y Fórmulas con Copilot en Excel](https://support.microsoft.com/es-es/office/comenzar-con-copilot-en-excel)
