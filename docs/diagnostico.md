# Diagnóstico UX · <tarea crítica>

## Caso
Persona usuaria · Tarea · Restricción · Fallo adicional

## Touchpoints y curva emocional
| N.º | Touchpoint | Qué hace el usuario | Emoción (−2 a +2) | Por qué | Nivel | ¿Momento de verdad? |
|---|---|---|---|---|---|---|

## Momentos de verdad
1. <touchpoint> · por qué se gana o pierde la confianza aquí
2. <touchpoint> · ...

## Hallazgos

| N.º | Problema | Heurística | Severidad | Issue |
|---|---|---|---|---|
| IHC-03 · H1 | La comisión inesperada aparece recién al final y el total pasa de $90.00 a $92.50, después de que el estudiante ya decidió pagar | H1 (visibilidad del estado), H5 (prevención de errores) | 4 (catastrófico): rompe la restricción de ver el costo total antes de aceptar | #1 |
| IHC-03 · H2 | El mensaje de error de pago es genérico: no dice qué pasó ni qué corregir | H9 (recuperación de errores) | 3 (mayor): un estudiante con presupuesto limitado no sabe si le cobraron | #2 |
| IHC-03 · H3 | El comprobante no deja verificar que el monto pagado es el total aceptado | H1 (visibilidad del estado) | 3 (mayor): genera desconfianza en el cobro | #3 |
| IHC-04 · H1 | El botón Pagar permite dos pagos consecutivos | H5 (prevención de errores) | 4 (catastrófico): doble cobro a nombre de otra persona | #1 |
| IHC-04 · H2 | No hay indicación de que el pago está en proceso, y el representante vuelve a pulsar | H1 (visibilidad del estado) | 3 (mayor): empuja al doble pago | #2 |
| IHC-04 · H3 | El método de pago no se reconoce sin ver datos bancarios completos | H5 (prevención de errores) | 3 (mayor): choca con la restricción de ocultar datos bancarios | #3 |
## Curva emocional inicial
![Curva antes](../diagramas/curva-antes.png)

## Medición real vs. estimación

**Observado:** nada todavía. En esta fase no hay prueba con usuarios.

**Estimación del equipo:**
- Las emociones (−2 a +2) y la curva emocional inicial son estimaciones basadas en la persona de cada tarjeta.
- Las severidades (0–4, escala de Nielsen) son juicio del equipo.
- Los tiempos y los errores no se estiman: se medirán en la sesión de la Fase 4 (`pruebas/sesion.md`).

**Se verificará en la Fase 4:** si el participante nota el costo total antes de aceptar (IHC-03) y si intenta pagar dos veces (IHC-04). Hasta entonces, los hallazgos son hipótesis.