# Laboratorio 1: Diseñar instrucciones para tareas jurídicas y de cumplimiento

**Duración:** 6 min

## Descripción
Los participantes conocerán el caso de una empresa ficticia que está siendo evaluada para establecer una relación comercial con el Banco. Como primer ejercicio, transformarán una solicitud genérica relacionada con la clasificación de peticiones, quejas, reclamos y requerimientos asociados con el proceso en una instrucción estructurada. Definirán una rúbrica con categorías, criterios, prioridad y formato esperado, incorporarán ejemplos de clasificación y solicitarán a Copilot justificar cada resultado con base en los criterios proporcionados.

## Pasos para ejecutar la práctica

1. **Evaluación de solicitud jurídica genérica:**
   * Abre Microsoft 365 Copilot Chat.
   * Envía la siguiente solicitud genérica:
     ```text
     Clasifica los reclamos y requerimientos legales que lleguen sobre un proveedor tecnológico.
     ```
   * Observa la respuesta superficial entregada por el modelo al carecer de marco jurídico estructurado.

2. **Diseño de instrucción estructurada mediante la fórmula de prompt:**
   * Envía la siguiente instrucción utilizando la fórmula Contexto + Objetivo + Origen + Expectativas:
     ```text
     Actúa como un Abogado Senior de Cumplimiento Normativo y Gobierno Corporativo.
     
     Contexto: El Banco está evaluando establecer una relación comercial con una empresa ficticia proveedora de soluciones tecnológicas.
     Objetivo: Diseñar una Rúbrica de Clasificación Legal para peticiones, quejas, reclamos y requerimientos regulatorios asociados al proveedor.
     Origen: Normativa de protección de datos, continuidad del servicio y prevención de riesgos legales.
     Expectativas: 
     1. Crea una tabla con las columnas: Categoria_Riesgo, Criterio_Legal, Prioridad (Alta/Media/Baja), Plazo_Atencion_Dias y Accion_Inmediata.
     2. Incluye 2 ejemplos de clasificación con casos ficticios.
     3. Exige que Copilot justifique cada resultado citando la norma o criterio legal aplicado.
     ```

3. **Exportación del marco de instrucción a Word:**
   * Haz clic en **Exportar a Word** y guarda el archivo generado con el nombre exacto: `Rubrica_Clasificacion_Requerimientos_Legales.docx`.

## Resultado esperado
Un documento guardado como `Rubrica_Clasificacion_Requerimientos_Legales.docx` que establece la rúbrica formal y estructurada para evaluar requerimientos y riesgos legales.
