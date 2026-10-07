# Transformar una solicitud genérica en una instrucción estructurada con rúbrica de clasificación de peticiones, quejas, reclamos y requerimientos

## Metadatos

| Atributo | Detalle |
| :--- | :--- |
| **Duración** | 6 minutos |
| **Complejidad** | Fácil |
| **Nivel de Bloom** | Aplicar |

## Descripción General

En este laboratorio, transformarás una instrucción informal y ambigua (prompt genérico) en un prompt estructurado de alto rendimiento utilizando el framework **COOE** (Contexto + Objetivo + Origen + Expectativas). Con esta instrucción, generarás una rúbrica de clasificación de Peticiones, Quejas, Reclamos y Requerimientos (PQRS) diseñada específicamente para mitigar riesgos legales y operativos en el sector inmobiliario ficticio (*Inmobiliaria Alpha*). El resultado final servirá como marco de referencia estructurado para futuros análisis contractuales y de cumplimiento.

## Objetivos de Aprendizaje

Al finalizar este laboratorio, serás capaz de:
- [ ] Aplicar de forma práctica el framework COOE para reestructurar prompts desorganizados en el ámbito jurídico.
- [ ] Definir criterios claros y plazos de respuesta regulatorios para clasificar PQRS sin ambigüedades.
- [ ] Utilizar Microsoft 365 Copilot Chat para generar estructuras de datos consistentes en formato Markdown.

## Prerrequisitos

- **Conocimientos teóricos:** Comprensión básica de la estructura del framework COOE (Contexto, Objetivo, Origen, Expectativas).
- **Acceso a plataformas:** Licencia activa de **Microsoft 365 Copilot Premium** con acceso a la interfaz de Copilot Chat.

## Entorno de Laboratorio

Este laboratorio se ejecuta en la nube de Microsoft utilizando los siguientes recursos mínimos:

### Software Requerido

| Software / Herramienta | Versión Requerida | Enlace Oficial / Origen |
| :--- | :--- | :--- |
| **Microsoft 365 Copilot Chat** | Premium (Service Update 2408 o superior) | [Portal de Microsoft 365](https://admin.microsoft.com) |
| **Microsoft Edge** | Versión 128.0.2739.42 (x64) o superior | [Descarga de Edge](https://www.microsoft.com/edge) |

### Estructura de Directorios (Opcional)
Se recomienda tener configurada la carpeta de trabajo local para almacenar los resultados:
- Directorio de Trabajo: `C:\CursoCopilotLegal\Modulo3_4\`

---

## Instrucciones Paso a Paso

### Paso 1: Identificar las deficiencias de un prompt genérico

**Objetivo:** Analizar las debilidades de una instrucción desestructurada y entender por qué genera respuestas de baja calidad o alucinaciones.

**Instrucciones:**
1. Abre tu navegador web **Microsoft Edge**.
2. Dirígete al portal de **Microsoft 365 Copilot Chat** (o accede mediante la barra lateral de Copilot en Edge con tu cuenta corporativa habilitada).
3. Lee con atención la siguiente solicitud informal (no la envíes aún):
   > *"Hola Copilot, ayúdame a hacer una rúbrica para clasificar quejas y reclamos de clientes de una inmobiliaria. Que sea sencilla y tenga ejemplos."*
4. **Análisis crítico:** Esta instrucción carece de rol (Contexto), no define qué tipo de quejas o regulaciones aplican (Origen), no especifica el formato esperado (Expectativas) y deja a la IA el criterio de inventar los plazos legales de respuesta.

**Resultado esperado:** Comprensión de las carencias operativas del prompt genérico.

**Verificación:** Identificar mentalmente que el prompt genérico no cumple con ninguno de los cuatro pilares del framework COOE.

---

### Paso 2: Redactar la instrucción estructurada con el Framework COOE

**Objetivo:** Escribir un prompt robusto utilizando delimitadores claros y aplicando el método COOE para forzar a la IA a seguir criterios jurídicos precisos.

**Instrucciones:**
1. Copia en tu portapapeles el siguiente prompt estructurado meticulosamente diseñado bajo la fórmula COOE:

```text
[CONTEXTO]: Actúas como un Oficial de Cumplimiento y Asesor Jurídico Senior de la empresa "Inmobiliaria Alpha". Tu especialidad es la gestión de atención al cliente y la mitigación de riesgos legales derivados de respuestas tardías o erróneas a reclamaciones bajo la normativa de protección al consumidor.

[OBJETIVO]: Diseñar una rúbrica de clasificación categórica y estricta para solicitudes recibidas de clientes, dividida exactamente en las cuatro categorías operativas: Petición, Queja, Reclamo y Requerimiento de Autoridad (PQRS).

[ORIGEN]: Basa los criterios en los estándares estándar de protección al consumidor de servicios inmobiliarios aplicables en España y Latinoamérica.

[EXPECTATIVAS]: Genera una rúbrica en formato de tabla Markdown que contenga exactamente las siguientes columnas:
1. Categoría (Petición, Queja, Reclamo, Requerimiento de Autoridad)
2. Criterio de Clasificación (Definición jurídica clara y límite operativo de la categoría)
3. Plazo Máximo de Respuesta Legal (en días hábiles, coherente con la normativa de protección al consumidor)
4. Ejemplo de Texto Crítico Ficticio (Un fragmento de texto realista que un cliente enviaría a la "Inmobiliaria Alpha" que tipifique esta categoría)

Restricciones:
- No incluyas introducciones ni conclusiones informales.
- La tabla debe ser autoexplicativa y utilizar un tono técnico, formal y altamente preventivo.
```

2. Pega este texto en el cuadro de entrada de **Microsoft 365 Copilot Chat**.
3. Presiona **Enter** o haz clic en el botón de enviar.

**Resultado esperado:** Copilot procesará la instrucción estructurada y generará una rúbrica precisa en formato Markdown sin rodeos introductorios innecesarios.

**Verificación:** La respuesta de Copilot debe contener una tabla estructurada con las cuatro columnas solicitadas.

---

### Paso 3: Analizar y guardar la rúbrica generada

**Objetivo:** Revisar la calidad legal de los criterios arrojados por Copilot y almacenar el entregable en el directorio local.

**Instrucciones:**
1. Revisa la tabla generada en la ventana del chat. Debe lucir similar a la siguiente estructura:

| Categoría | Criterio de Clasificación | Plazo Máximo de Respuesta Legal | Ejemplo de Texto Crítico Ficticio |
| :--- | :--- | :--- | :--- |
| **Petición** | Solicitud de información general, copias de documentos o trámites rutinarios sin disconformidad. | 15 días hábiles | "Solicito que me envíen una copia digital de mi contrato de compraventa del departamento 402..." |
| **Queja** | Manifestación de descontento relacionada con la calidad de la atención al cliente o retrasos administrativos. | 15 días hábiles | "Llevo tres días esperando que el asesor comercial me devuelva la llamada para coordinar la entrega de llaves..." |
| **Reclamo** | Pretensión directa por incumplimiento contractual, vicios ocultos en el inmueble o afectación patrimonial. | 15 días hábiles | "El grifo de la cocina gotea y ha dañado el mueble de madera. Exijo la reparación inmediata y el pago de daños..." |
| **Requerimiento de Autoridad** | Notificación de un organismo regulador o judicial que exige información bajo apercibimiento de sanción. | 5 a 10 días hábiles (según orden) | "Por medio de la presente, la Oficina de Protección al Consumidor requiere que Inmobiliaria Alpha remita el expediente..." |

2. Copia el contenido de la tabla de Markdown que Copilot generó en tu pantalla.
3. Abre un bloc de notas o tu editor de texto preferido y guárdalo en tu ruta local:
   `C:\CursoCopilotLegal\Modulo3_4\Rubrica_PQRS.txt`

**Resultado esperado:** Archivo de texto guardado localmente con la rúbrica estandarizada lista para ser utilizada en posteriores análisis automatizados.

**Verificación:** Asegurarse de que el archivo `Rubrica_PQRS.txt` contenga la rúbrica completa en formato de tabla de Markdown.

---

## Validación y Pruebas

Para garantizar que la rúbrica generada funciona de manera consistente y evaluar las limitaciones de la IA ante casos complejos, realiza la siguiente prueba de estrés adversarial.

### Prueba de Estrés: Caso Adversarial de Frontera Difusa

**Instrucciones:**
1. En el mismo chat de Copilot, ingresa la siguiente instrucción para evaluar la precisión de clasificación del modelo utilizando la rúbrica que acaba de generar:

```text
Clasifica el siguiente caso real utilizando EXCLUSIVAMENTE la rúbrica que acabas de generar. Indica la categoría, el plazo de respuesta que corresponde y justifica tu decisión en una sola oración.

Texto del cliente:
"Buenas tardes, escribo porque el grifo de la cocina de mi departamento nuevo gotea. Solicito que lo reparen hoy mismo, de lo contrario escalaré esto directamente a la Oficina de Protección al Consumidor y los demandaré por daños y perjuicios porque ya se inundó mi alfombra."
```

2. Envía el prompt y analiza cómo gestiona Copilot la ambigüedad (el texto tiene elementos de consulta/petición, queja por servicio, reclamo por daños e incluye una amenaza de escalamiento a autoridad).

### Criterios de Éxito de la Validación
- **Clasificación Correcta:** Copilot debe clasificar el caso como un **Reclamo** (y NO como un Requerimiento de Autoridad, ya que el cliente solo *amenaza* con ir a la autoridad, pero la comunicación aún proviene directamente del cliente).
- **Consistencia Temporal:** Debe asignar el plazo de respuesta correspondiente a "Reclamo" según la rúbrica generada en el Paso 2 (por ejemplo, 15 días hábiles).
- **Justificación:** La justificación debe identificar claramente que existe una afectación patrimonial (daño en la alfombra e instalación defectuosa del inmueble).

---

## Solución de Problemas

A continuación se presentan los dos problemas más comunes que pueden surgir durante la ejecución de esta práctica y cómo solucionarlos de manera inmediata:

### Problema 1: Copilot genera la rúbrica en párrafos de texto plano en lugar de una tabla de Markdown
- **Síntoma:** La salida de Copilot es una lista numerada o bullets de texto desorganizado, ignorando las columnas especificadas.
- **Causa:** El modelo de lenguaje sufrió una desviación de formato debido a la longitud de los tokens de salida o interpretó erróneamente la instrucción de formato.
- **Solución:** Envía un prompt de corrección de inmediato en el mismo chat:
  > *"Por favor, reformatea la información anterior exactamente en una tabla de Markdown que contenga las cuatro columnas requeridas: Categoría, Criterio de Clasificación, Plazo Máximo de Respuesta Legal y Ejemplo de Texto Crítico Ficticio."*

### Problema 2: El modelo asume leyes de una jurisdicción incorrecta o ajena (por ejemplo, legislación de EE.UU.)
- **Síntoma:** Los plazos de respuesta se muestran en días distintos o citan leyes como la CFPB estadounidense en lugar de leyes hispanoamericanas o españolas.
- **Causa:** El anclaje del origen (*grounding*) fue muy general y el modelo priorizó su base de datos de entrenamiento en inglés.
- **Solución:** Restringe geográficamente la instrucción enviando el siguiente mensaje correctivo:
  > *"Ajusta la columna de Plazo Máximo de Respuesta Legal para que se adapte estrictamente al estándar general de protección al consumidor de España o Latinoamérica (que establece un estándar máximo general de 15 días hábiles para dar respuesta a reclamos y quejas)."*

---

## Limpieza

Para mantener el entorno de trabajo ordenado y evitar fugas de contexto en el chat de Copilot:
1. Haz clic en el botón de **"Nuevo Tema"** (ícono de escoba o lápiz de reinicio) en tu interfaz de Copilot Chat para limpiar el historial de la sesión actual antes de pasar a la siguiente práctica.
2. Asegúrate de que el archivo `Rubrica_PQRS.txt` esté guardado de forma segura en `C:\CursoCopilotLegal\Modulo3_4\` y cierra la ventana del editor de texto.

---

## Resumen

En esta práctica rápida de 6 minutos, has aprendido a:
1. **Identificar los riesgos** asociados con los prompts desestructurados o genéricos en el entorno legal y corporativo.
2. **Estructurar instrucciones** robustas aplicando el framework **COOE** (Contexto, Objetivo, Origen y Expectativas) que reduce drásticamente las alucinaciones de la IA.
3. **Generar un entregable operativo** (una rúbrica categórica de PQRS en formato Markdown) con criterios jurídicos delimitados y plazos de respuesta automatizados que servirá para estandarizar la clasificación de riesgos en la *Inmobiliaria Alpha*.
4. **Validar el comportamiento de la IA** ante escenarios complejos y ambiguos (casos de frontera) mediante técnicas de prompting de prueba.

### Recursos Adicionales para Consulta
- [Guía oficial de Microsoft sobre diseño de prompts en Copilot](https://learn.microsoft.com/es-es/copilot/microsoft-365/microsoft-365-copilot-prompts)
- [Principios de ingeniería de instrucciones en Azure OpenAI](https://learn.microsoft.com/es-es/azure/ai-services/openai/concepts/prompt-engineering)
