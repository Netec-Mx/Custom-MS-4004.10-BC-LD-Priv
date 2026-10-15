# Laboratorio 4: Analizar riesgos regulatorios y escenarios de cumplimiento mediante Copilot

**Duración:** 22 min

## Descripción
El usuario proporcionará en el prompt un conjunto de operaciones ficticias asociadas con la empresa evaluada en el caso. Los participantes proporcionarán a Copilot una rúbrica didáctica con criterios e indicadores de cumplimiento y solicitarán clasificar cada escenario, identificar qué criterio activa la revisión, justificarlo con la información disponible y señalar qué información adicional sería necesaria antes de escalarlo. Ejecutarán la misma solicitud utilizando modelos de OpenAI y Claude (si están disponibles) y convertirán los hallazgos en una matriz de revisión con Copilot en Excel.

## Pasos para ejecutar la práctica

1. **Clasificación de escenarios de cumplimiento y comparación de modelos:**
   * Abre Microsoft 365 Copilot Chat y envía el siguiente prompt con escenarios ficticios:
     ```text
     Analiza los siguientes 2 escenarios operativos ficticios del proveedor:
     - Escenario A: Transferencia internacional de base de datos a un servidor de un tercero sin cláusula estándar de protección.
     - Escenario B: Retraso repetido de 48 horas en la notificación de incidentes de seguridad de la información.
     
     Clasifica cada escenario según la gravedad (Bajo, Medio, Alto, Crítico), justifica qué principio o norma legal vulnera e indica la información adicional requerida antes de un escalamiento al Oficial de Cumplimiento.
     ```
   * En el selector de modelos de Copilot (si está disponible en el tenant), cambia entre los modelos disponibles (ej. OpenAI / Claude), reejecuta la solicitud y evalúa la precisión en el cumplimiento de las restricciones planteadas.

2. **Creación de la Matriz de Revisión en Microsoft Excel:**
   * Abre un libro nuevo en **Microsoft Excel** y guárdalo como `Matriz_Seguimiento_Cumplimiento.xlsx`.
   * En Copilot en Excel (modo **Edición**), envía el siguiente prompt:
     ```text
     Estructura una Matriz de Revisión de Cumplimiento con las columnas: Id_Hallazgo, Tipo_Riesgo, Senal_Identificada, Criterio_Normativo, Evidencia_Disponible, Nivel_Revision, Accion_Requerida y Estado.
     
     Puebla la tabla con 5 filas basadas en las cláusulas contractuales y los escenarios de cumplimiento analizados previamente.
     ```
   * Aplica un formato condicional en Excel sobre la columna `Nivel_Revision` para resaltar los hallazgos de nivel "Crítico".

## Resultado esperado
Un libro de Excel llamado `Matriz_Seguimiento_Cumplimiento.xlsx` con la matriz de riesgos regulatorios clasificados y formateados condicionalmente.
