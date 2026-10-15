# Laboratorio 2: Revisar documentos jurídicos mediante Copilot en Word

**Duración:** 23 min

## Descripción
A partir de un contrato ficticio generado durante la sesión, los participantes abrirán el contrato en Word y utilizarán Copilot para identificar objeto, obligaciones de las partes, vigencia, terminación, responsabilidades, confidencialidad, tratamiento de información y otras condiciones relevantes. El resultado deberá distinguir entre contenido explícitamente establecido en el contrato, información no encontrada e interpretaciones que requieren revisión profesional. Posteriormente, proporcionarán a Copilot una rúbrica ficticia con criterios jurídicos y operativos que deberán verificarse en determinadas cláusulas, clasificarán cada criterio y reformularán cláusulas en modo Edición.

## Pasos para ejecutar la práctica

1. **Generación del contrato ficticio y análisis en Word:**
   * Abre Microsoft 365 Copilot Chat y solicita la creación del contrato base:
     ```text
     Genera la estructura de un Contrato Marco de Prestación de Servicios Tecnológicos Ficticio de 6 cláusulas:
     1. Objeto del Contrato.
     2. Obligaciones del Proveedor.
     3. Nivel de Servicio (SLA) y Penalidades.
     4. Confidencialidad y Tratamiento de Datos Personales.
     5. Limitación de Responsabilidad y Sanciones.
     6. Vigencia y Terminación Anticipada.
     ```
   * Exporta esta respuesta a Microsoft Word y guárdala como: `Contrato_Servicios_Tecnologicos.docx`.

2. **Aplicación de rúbrica sobre las cláusulas en Microsoft Word:**
   * Abre `Contrato_Servicios_Tecnologicos.docx` en Microsoft Word y activa Copilot en modo **Edición**.
   * Adjunta el archivo `Rubrica_Clasificacion_Requerimientos_Legales.docx` y envía el siguiente prompt:
     ```text
     Aplica los criterios de la rúbrica adjunta sobre el texto del contrato abierto.
     
     Para cada cláusula identifica y clasifica en una tabla:
     - Estado: Cumple / Requiere Revisión / No se Identifica.
     - Evidencia explícita hallada en el texto.
     - Observación o riesgo legal detectado.
     ```

3. **Reformulación de cláusula de responsabilidad y guardado:**
   * Selecciona el texto de la "Cláusula 5: Limitación de Responsabilidad" y utiliza Copilot en Word para reescribirla enviando:
     ```text
     Reescribe esta cláusula para eliminar la limitación de responsabilidad en casos de brechas de seguridad o fuga de datos personales, garantizando indemnidad total para el Banco.
     ```
   * Guarda los cambios realizados en el archivo `Contrato_Servicios_Tecnologicos.docx`.

## Resultado esperado
Un contrato revisado y ajustado guardado como `Contrato_Servicios_Tecnologicos.docx` con la matriz de cumplimiento de cláusulas y la redacción mejorada de la cláusula de responsabilidad.
