# Sesión de prueba
**Participante:** P1 (otro grupo) · **Fecha/hora:** ____ · **Facilitador:** Martín · **Observador:** David
**Caso probado:** IHC-03 (`prototipo/v1/inicio.html?caso=03`) · **Versión:** v1

## Guion del facilitador
Leer en voz alta, sin dar pistas ni señalar nada en pantalla:

> "Eres estudiante y quieres pagar tu matrícula en este portal. Tienes un presupuesto ajustado. Paga con esta tarjeta: 4111 1111 1111 1111, y usa el correo p1@correo.com para el comprobante. Piensa en voz alta mientras lo haces. Yo no puedo ayudarte."

Reglas:
- No decir "comisión", "total" ni "error".
- Si pregunta algo: "¿Qué harías si yo no estuviera aquí?".
- Cronometrar desde que abre `inicio.html?caso=03` hasta que ve la confirmación.
- Al terminar, preguntar sin dirigir: **"¿Cuánto pagaste en total?"** y **"¿Cuánto esperabas pagar al empezar?"**

## Qué observar (observador)
- ¿Reacciona cuando aparece el cargo adicional en el formulario? ¿Qué dice o hace?
- ¿Sigue pagando, vuelve atrás o pulsa Cancelar?
- ¿Cuántas veces duda o relee? ¿Se equivoca al escribir?
- ¿Revisa el comprobante?

## Registro (llenar en vivo)
| Tarea | ¿Éxito? | Tiempo | Errores | Pausas / dudas | Cita textual |
|---|---|---|---|---|---|
| Consultar el valor de la matrícula | | | | | |
| Llegar al formulario y completarlo | | | | | |
| Pagar y llegar a la confirmación | | | | | |
| Decir cuánto pagó en total | | | | | |

## Hallazgo priorizado
<Problema · heurística · severidad · Issue #>

## Corrección aplicada en v2
<Qué cambió · archivo · commit>

## Antes / después
| Indicador | v1 | v2 |
|---|---|---|
| Total que dijo el participante vs. total real | | |
| Tiempo hasta la confirmación | | |
| Errores | | |

<Solo datos observados. Si v2 no se volvió a probar, decirlo.>

---
### Alternativa: caso IHC-04 (si prefieren probar este)
Tarea: "Eres representante y debes pagar la pensión de Ana Torres. Usa el correo p1@correo.com. Piensa en voz alta." Observar cuántas veces pulsa **Pagar** (el prototipo muestra el contador "Pagos enviados") y si entiende que el pago está en proceso. Preguntar al final: "¿Cuántas veces crees que se te cobró?".
