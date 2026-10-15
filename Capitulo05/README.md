# Laboratorio 5: Preparar una negociación contractual con Copilot

**Duración:** 20 min

## Descripción
A partir de la cláusula revisada previamente, los participantes solicitarán a Copilot generar tres alternativas de redacción que representen diferentes posiciones de negociación, manteniendo el propósito contractual pero modificando aspectos como distribución de responsabilidades, condiciones, excepciones o mecanismos de protección. Desarrollarán una evaluación de opción múltiple para simular la negociación y consolidarán la posición mediante Copilot en Word.

## Pasos para ejecutar la práctica

1. **Generación de alternativas de negociación contractual:**
   * Abre Copilot Chat, adjunta el documento `Contrato_Servicios_Tecnologicos.docx` y envía:
     ```text
     Con base en la Cláusula de Limitación de Responsabilidad modificada en el contrato, redacta 3 alternativas de posición de negociación:
     - Opción Conservadora (Protección máxima para el Banco sin concesiones).
     - Opción Moderada (Responsabilidad ilimitada en datos/seguridad, cap estándar en fallas operativas).
     - Opción Flexible (Tope de indemnización equivalente a 3 veces el valor anual del contrato).
     
     Para cada opción explica las ventajas y riesgos jurídicos para el Banco.
     ```

2. **Simulación de negociación mediante prueba de opción múltiple:**
   * En Copilot Chat, envía la siguiente instrucción para ejecutar la dinámica interactiva:
     ```text
     Actúa como el Abogado Contraparte del proveedor tecnológico durante la mesa de negociación contractual.

     Reglas:
     1. Hazme 3 preguntas consecutivas de selección múltiple (A, B, C, D) presentando las objeciones típicas que pondrías a las alternativas de negociación planteadas.
     2. Formula una pregunta a la vez y espera a que yo responda indicando solo la letra de la opción seleccionada.
     3. Entrega retroalimentación inmediata sobre la viabilidad jurídica y comercial de mi elección antes de pasar a la siguiente pregunta.
     ```

3. **Consolidación de la Nota de Negociación en Word:**
   * Abre **Microsoft Word**, activa Copilot, adjunta el archivo `Contrato_Servicios_Tecnologicos.docx` junto con el libro `Matriz_Seguimiento_Cumplimiento.xlsx` y envía:
     ```text
     Redacta la Nota Estratégica de Negociación Legal que consolide:
     1. Posición final recomendada sobre la cláusula de responsabilidad.
     2. Puntos no negociables (Líneas rojas de cumplimiento).
     3. Concesiones permitidas y estrategia de escalamiento al Comité Legal.
     ```
   * Guarda el archivo formal en Word con el nombre exacto: `Nota_Estrategica_Negociacion_Legal.docx`.

## Resultado esperado
Un documento técnico en Word guardado como `Nota_Estrategica_Negociacion_Legal.docx` con la postura oficial y líneas rojas para la mesa de negociación, junto con el ejercicio interactivo de opción múltiple completado en Copilot Chat.
