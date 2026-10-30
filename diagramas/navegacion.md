# Navegación · Pagos académicos (IHC-03 e IHC-04)
Pasos del user flow: P1 ver Inicio · P2 continuar al pago · P3 completar el formulario · P4 pulsar Pagar (¿datos válidos?) · P4a error recuperable (vuelve a P3) · P5 Confirmación.

## IHC-03 · Consultar y pagar matrícula
| # | De | A | Con qué elemento | Paso del user flow | Heurística |
|---|---|---|---|---|---|
| 1 | Inicio | Formulario de pago | Botón "Continuar al pago · Total $X" | P2 | H1 |
| 2 | Formulario de pago | Error de pago | Botón "Pagar" con un dato inválido | P4 → P4a | H9 |
| 3 | Error de pago | Formulario de pago | Campo con foco y datos conservados | P4a → P3 | H9 |
| 4 | Formulario de pago | Confirmación | Botón "Pagar $X" con datos válidos | P5 | H1 |
| 5 | Formulario de pago | Inicio | Botón "Cancelar" (o tecla Esc) | Cancelar desde P3 | H3 |
| 6 | Confirmación | Inicio | Botón "Volver al inicio" | Fin | H3 |

Adónde regresa el usuario tras:
- Confirmar → Confirmación (muestra el comprobante); desde ahí "Volver al inicio" lleva a Inicio.
- Cancelar → Inicio, sin cobrar nada.
- Error → Formulario de pago, con foco en el campo con error y sin borrar lo escrito.

## IHC-04 · Pagar y obtener comprobante
| # | De | A | Con qué elemento | Paso del user flow | Heurística |
|---|---|---|---|---|---|
| 1 | Inicio | Formulario de pago | Botón "Continuar al pago" (persona, concepto y valor ya visibles) | P2 | H1 |
| 2 | Formulario de pago | Error de pago | Botón "Pagar" con un dato inválido | P4 → P4a | H9 |
| 3 | Error de pago | Formulario de pago | Campo con foco y datos conservados | P4a → P3 | H9 |
| 4 | Formulario de pago | Confirmación | Botón "Pagar" con datos válidos (debe deshabilitarse al pulsarlo) | P5 | H5 |
| 5 | Formulario de pago | Inicio | Botón "Cancelar" (o tecla Esc) | Cancelar desde P3 | H3 |
| 6 | Confirmación | Inicio | Botón "Volver al inicio" | Fin | H3 |

Adónde regresa el usuario tras:
- Confirmar → Confirmación (comprobante con tarjeta enmascarada); desde ahí "Volver al inicio" lleva a Inicio.
- Cancelar → Inicio, sin cobrar nada.
- Error → Formulario de pago, con foco en el campo con error y sin borrar lo escrito.
