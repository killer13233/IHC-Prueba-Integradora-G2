# Sesión de prueba
**Participante:** P1 (sin datos personales) · **Fecha/hora:** 29/10/2026 · 11:30 · **Facilitación y observación:** Sheyla
**Versión probada:** v1 · **Guion usado:** `pruebas/guion-facilitador.md` (textos exactos de las tareas y reglas)

## Registro
| Tarea | ¿Éxito? | Tiempo | Errores | Pausas / dudas (>5 s) | Cita textual |
|---|---|---|---|---|---|
| 1 · IHC-03 · Pagar la matrícula | Con ayuda | ≈ 5 min | Varios al llenar los campos: al principio no sabía para qué era cada campo ni cómo llenarlo (detalle no registrado) | En cada campo del Formulario de pago | No se registró |
| 2 · IHC-04 · Pagar la pensión de Ana Torres | Sí | ≈ 1 min | Ninguno | Ninguna | No se registró |

## Observaciones por tarea
**Tarea 1 (IHC-03):** el participante no supo para qué servían los campos del Formulario de pago y necesitó ayuda para completarlos. **No notó la comisión de $2.50 ni el cambio del total ($90.00 → $92.50).** El equipo tuvo que señalárselo y aun así no entendía por qué aparecía.
> Desviación del guion: hubo ayuda del facilitador y se le indicó la comisión. Por eso la tarea se registra como «Con ayuda» y el tiempo no es comparable con una tarea sin intervención.

**Tarea 2 (IHC-04):** pulsó Pagar más de una vez, pero el contador mostró **«Pagos enviados: 1»**, así que el doble pago no se registró en esta sesión. No se registró si reconoció el método de pago.

## Preguntas de cierre (respuestas del participante)
Las respuestas se dieron al final de la sesión y no se separaron por tarea.

| Pregunta | Respuesta |
|---|---|
| ¿Qué fue lo más difícil o confuso? | «Nada» |
| ¿Confiaría en este sistema para pagar? ¿Por qué? | Indeciso (no se registró el motivo) |
| ¿Algo que cambiaría? | Que se vieran los pasos, quién paga y a qué entidad se paga |

## Hallazgo priorizado
| Caso | Hallazgo observado | Heurística | Severidad | Issue |
|---|---|---|---|---|
| IHC-03 | El participante no percibió la comisión ni el cambio del total; necesitó que se la señalaran. Confirma que el costo total no es visible antes de aceptar | H1 (visibilidad del estado), H5 (prevención de errores) | 4 | #5 |
| IHC-03 | No supo para qué era cada campo del Formulario de pago ni cómo llenarlo | H5 (prevención de errores) | 3 | #3 |
| Ambos | Pidió ver los pasos del proceso, quién paga y a qué entidad | H1 (visibilidad del estado) | 2 | #3 |

Nota: en IHC-04 el doble pago **no** se observó (contador = 1); el hallazgo #6 se mantiene como estimación del equipo.

## Corrección aplicada en v2
| Caso | Qué cambió | Archivo | Origen |
|---|---|---|---|
| IHC-03 | La comisión de $2.50 y el total $92.50 se ven desde Inicio; el total ya no cambia al pagar | `prototipo/v2/inicio.html`, `prototipo/v2/pago.html` | Prueba (P1 no notó la comisión) · #5 |
| IHC-03 | Cada campo tiene un texto de ayuda («Los 16 números que están en el frente de su tarjeta…», «Aquí le enviaremos el comprobante…») | `prototipo/v2/pago.html` | Prueba (P1 no sabía cómo llenar los campos) · #3 |
| Ambos | Indicador de pasos (1. Revisar · 2. Pagar · 3. Comprobante) y recuadro con quién paga y a qué entidad | `prototipo/v2/*.html`, `prototipo/v2/styles.css` | Prueba (sugerencia de P1) |
| IHC-04 | El botón Pagar se bloquea al primer clic y el aviso dice «No cierres esta página ni vuelvas a pulsar Pagar» | `prototipo/v2/pago.html` | Diagnóstico · #6 |
| Ambos | El rechazo del banco dice «No se hizo ningún cobro» y conserva los datos | `prototipo/v2/pago.html` | Diagnóstico · #3 |

Capturas: `evidencias/v1-*` (antes) y `evidencias/v2-*` (después).

## Antes / después
| Indicador | v1 (observado con P1) | v2 |
|---|---|---|
| Tarea 1 · éxito | Con ayuda | No se volvió a probar |
| Tarea 1 · tiempo | ≈ 5 min | No se volvió a probar |
| Tarea 1 · notó la comisión | No | No se volvió a probar (en v2 se muestra desde Inicio) |
| Tarea 2 · éxito | Sí | No se volvió a probar |
| Tarea 2 · tiempo | ≈ 1 min | No se volvió a probar |
| Tarea 2 · pagos enviados | 1 | No se volvió a probar |

v2 no se volvió a probar con un participante. La curva emocional después (`diagramas/curva-despues.png`) es una **estimación del equipo**.
