# Trazabilidad

Pantallas (sitemap): **Inicio · Formulario de pago · Error de pago (estado) · Confirmación**.
Pasos del user flow: P1 ver Inicio · P2 continuar al pago · P3 completar el formulario · P4 pulsar Pagar (¿datos válidos?) · P4a error recuperable (vuelve a P3) · P5 Confirmación.
Navegación: número de fila de la tabla de cada caso en `diagramas/navegacion.md`. Componentes: nombres de `docs/componentes.md`.

## IHC-03 · Estudiante becado · Consultar y pagar matrícula
| Requisito | Pantalla (sitemap) | Navegación | Paso user flow | Componente | Wireframe | Prototipo v1 |
|---|---|---|---|---|---|---|
| **R1** Consultar el valor de la matrícula con el detalle por rubro | Inicio | Entrada al prototipo (`inicio.html?caso=03`) | P1 | Fila de resumen · Resumen de costo total | 01-inicio | inicio.html?caso=03 |
| **R2** Ver el costo total (matrícula + comisiones) antes de aceptar el pago | Inicio · Formulario de pago | Nav. 1 «Continuar al pago · Total $X» | P1, P2 | Resumen de costo total | 01-inicio, 02-formulario | inicio.html, pago.html |
| **R3** Comparar la comisión de cada método de pago antes de elegir uno | Formulario de pago | Nav. 1 | P3 | Resumen de costo total (estado «con comisión») | 02-formulario | pago.html?caso=03 |
| **R4** Pagar la matrícula por el mismo total que aceptó | Formulario de pago → Confirmación | Nav. 4 «Pagar $X» | P4 → P5 | Formulario de pago · Botón Pagar | 02-formulario | pago.html?caso=03 |
| **R5** Corregir un dato inválido sin perder lo que ya escribió | Error de pago (estado) | Nav. 2 y 3 (foco en el campo, datos conservados) | P4a → P3 | Etiqueta + campo de texto · Mensaje de error junto al campo · Aviso de estado | 03-error | pago.html?caso=03 |
| **R6** Verificar que el monto del comprobante coincide con el total aceptado | Confirmación | Nav. 6 «Volver al inicio» | P5 | Comprobante | 04-confirmacion | confirmacion.html?caso=03 |

## IHC-04 · Representante que paga por otra persona · Pagar y obtener comprobante
| Requisito | Pantalla (sitemap) | Navegación | Paso user flow | Componente | Wireframe | Prototipo v1 |
|---|---|---|---|---|---|---|
| **R1** Identificar a qué persona y qué concepto está pagando, con su valor | Inicio | Entrada al prototipo (`inicio.html?caso=04`) | P1 | Fila de resumen | 01-inicio | inicio.html?caso=04 |
| **R2** Reconocer su método de pago por los últimos 4 dígitos | Formulario de pago | Nav. 1 «Continuar al pago» | P2, P3 | Método de pago (últimos 4 dígitos) | 02-formulario | pago.html?caso=04 |
| **R3** Pagar una sola vez aunque pulse el botón varias veces | Formulario de pago → Confirmación | Nav. 4 «Pagar» (debe deshabilitarse) | P4 → P5 | Botón Pagar · Contador de pagos enviados (v1) | 02-formulario | pago.html?caso=04 |
| **R4** Ver que el pago está en proceso mientras espera | Formulario de pago (estado de carga) | Nav. 4 | P4 | Aviso de estado (carga) | 02-formulario | pago.html?caso=04 |
| **R5** Corregir un dato inválido sin perder lo que ya escribió | Error de pago (estado) | Nav. 2 y 3 (foco en el campo, datos conservados) | P4a → P3 | Etiqueta + campo de texto · Mensaje de error junto al campo · Aviso de estado | 03-error | pago.html?caso=04 |
| **R6** Obtener un comprobante que oculte los datos bancarios completos | Confirmación | Nav. 6 «Volver al inicio» | P5 | Comprobante · Método de pago (últimos 4 dígitos) | 04-confirmacion | confirmacion.html?caso=04 |

**Nota:** «Cancelar» (Nav. 5), «Volver al inicio» (Nav. 6) y la tecla Esc son salidas del usuario (H3, control y libertad): aparecen en navegación y componentes, no como requisito aparte.
