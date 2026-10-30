# Trazabilidad

Pantallas: **Inicio · Formulario de pago · Error de pago (estado) · Confirmación**. Pasos del user flow: P1 ver Inicio · P2 continuar al pago · P3 completar formulario · P4 pulsar Pagar (¿datos válidos?) · P4a error recuperable · P5 Confirmación.

## IHC-03 · Estudiante becado · Consultar y pagar matrícula
| Requisito | Pantalla (sitemap) | Navegación | Paso user flow | Componente | Wireframe | Prototipo v1 |
|---|---|---|---|---|---|---|
| **R1** Consultar el valor de la matrícula | Inicio | Entrada al portal | P1 | Tarjeta de desglose | 01-inicio | inicio.html?caso=03 |
| **R2** Ver el total con comisiones antes de aceptar | Inicio · Formulario de pago | Inicio → «Continuar al pago» | P1, P2 | Tarjeta de desglose · aviso de total | 01-inicio, 02-formulario | inicio.html, pago.html |
| **R3** Comparar la comisión de cada método | Formulario de pago | Ya está en la pantalla | P3 | Desglose con fila «Comisión» | 02-formulario | pago.html?caso=03 |
| **R4** Pagar por el total aceptado | Formulario de pago | «Pagar» → Confirmación | P4 → P5 | Campos de tarjeta · botón Pagar | 02-formulario | pago.html?caso=03 |
| **R5** Corregir sin perder lo escrito | Error de pago (estado) | Error → Formulario con foco en el campo | P4a → P3 | Campo en error · mensaje bajo el campo · aviso | 03-error | pago.html?caso=03 |
| **R6** Verificar que el comprobante = total aceptado | Confirmación | «Volver al inicio» → Inicio | P5 | Comprobante · botón Descargar | 04-confirmacion | confirmacion.html?caso=03 |

## IHC-04 · Representante · Pagar y obtener comprobante
| Requisito | Pantalla (sitemap) | Navegación | Paso user flow | Componente | Wireframe | Prototipo v1 |
|---|---|---|---|---|---|---|
| **R1** Identificar persona y concepto | Inicio | Entrada al portal | P1 | Tarjeta del estudiante (Ana Torres, Pensión de octubre) | 01-inicio | inicio.html?caso=04 |
| **R2** Reconocer el método por los últimos 4 dígitos | Formulario de pago | Inicio → «Continuar al pago» | P2, P3 | Selector de método enmascarado (•••• 4821) | 02-formulario | pago.html?caso=04 |
| **R3** Pagar una sola vez | Formulario de pago | «Pagar» → Confirmación | P4 | Botón Pagar (bloqueado al pulsar en v2) | 02-formulario | pago.html?caso=04 |
| **R4** Ver que el pago está en proceso | Formulario de pago (estado de carga) | Automático tras «Pagar» | P4 | Indicador de carga · aviso de estado | 02-formulario | pago.html?caso=04 |
| **R5** Corregir sin perder lo escrito | Error de pago (estado) | Error → Formulario con foco en el campo | P4a → P3 | Campo en error · mensaje bajo el campo · aviso | 03-error | pago.html?caso=04 |
| **R6** Obtener comprobante con datos bancarios ocultos | Confirmación | «Volver al inicio» → Inicio | P5 | Comprobante · dato enmascarado · botón Descargar | 04-confirmacion | confirmacion.html?caso=04 |

**Nota:** «Cancelar», «Volver al inicio» y la tecla Esc son salidas del usuario (H3): aparecen en navegación y componentes, no como requisito aparte.
