# Laboratorio 3: Investigar señales de riesgo mediante el agente Investigador y Copilot Notebooks

**Duración:** 23 min

## Descripción
Los participantes utilizarán Investigador (Researcher) para realizar una investigación de fuentes públicas sobre una empresa real o de referencia para el ejercicio de investigación del caso ficticio. Solicitarán identificar noticias, litigios, sanciones regulatorias, investigaciones gubernamentales, controversias reputacionales o eventos que puedan representar riesgos legales o de cumplimiento. El resultado deberá conservar las fuentes y fechas, diferenciar hechos documentados de opiniones o especulaciones y presentar los hallazgos de forma objetiva. Posteriormente, consolidarán la información en Copilot Notebooks y generarán un mapa mental.

## Pasos para ejecutar la práctica

1. **Investigación de prensa adversa y litigios con el agente Investigador:**
   * En Microsoft 365 Copilot, activa el agente **Investigador (Researcher)**.
   * Envía el siguiente prompt estructurado con plan directo:
     ```text
     Escribe primero un PLAN DE INVESTIGACIÓN de 2 pasos para analizar litigios públicos, sanciones regulatorias y noticias adversas sobre empresas de servicios tecnológicos en la región (últimos 12 meses):
     1. Búsqueda de sanciones regulatorias y temas de protección de datos.
     2. Menciones en prensa sobre disputas contractuales y fallas operativas.

     A continuación, ejecuta el plan y entrega un informe de 3 viñetas objetivas con fuentes y fechas explícitas, separando hechos probados de opiniones.
     ```
   * Exporta la respuesta a Word guardándola con el nombre: `Informe_Investigacion_Riesgo_Prensa.docx`.

2. **Consolidación de investigación en Copilot Notebooks y Mapa Mental:**
   * Abre **Copilot Notebooks** (Bloc de notas de Copilot).
   * Adjunta como fuentes los archivos `Contrato_Servicios_Tecnologicos.docx` e `Informe_Investigacion_Riesgo_Prensa.docx`.
   * En el panel de instrucciones de Notebooks, envía el siguiente prompt:
     ```text
     Consolida las fuentes vinculadas en este Notebook y genera la estructura jerárquica de un Mapa Mental de Diagnóstico Legal.
     
     Estructura con sangría:
     - Nodo Central: Evaluación de Riesgo Legal del Proveedor
       - Rama 1: Hallazgos en Cláusulas Contractuales (Word)
       - Rama 2: Señales Externas y Litigios (Investigador)
       - Rama 3: Brechas que Requieren Mitigación en Negociación
     ```

3. **Exportación del mapa mental y síntesis:**
   * Copia o exporta la estructura jerárquica del mapa mental a un documento de Word con el nombre exacto: `Sintesis_Investigacion_Notebook.docx`.

## Resultado esperado
El informe de investigación de riesgo `Informe_Investigacion_Riesgo_Prensa.docx` y la síntesis consolidada en Word `Sintesis_Investigacion_Notebook.docx` con el mapa mental del expediente legal.
