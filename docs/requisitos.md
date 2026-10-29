# Requisitos · Pagos académicos (IHC-03 e IHC-04)
Regla: un requisito, un verbo, desde el punto de vista del usuario.

## IHC-03 · Estudiante becado · Consultar y pagar matrícula
Restricción: costo total visible antes de aceptar. Fallo adicional: aparece una comisión inesperada al final.

| ID | El usuario debe poder... | Verbo | Origen (tarea / restricción / fallo) |
|---|---|---|---|
| R1 | Consultar el valor de su matrícula con el detalle por rubro | Consultar | tarea |
| R2 | Ver el costo total (matrícula + comisiones) antes de aceptar el pago | Ver | restricción |
| R3 | Comparar la comisión de cada método de pago antes de elegir uno | Comparar | fallo |
| R4 | Pagar la matrícula por el mismo total que aceptó | Pagar | tarea |
| R5 | Corregir un dato inválido sin perder lo que ya escribió | Corregir | tarea |
| R6 | Verificar que el monto del comprobante coincide con el total aceptado | Verificar | fallo |

## IHC-04 · Representante que paga por otra persona · Pagar y obtener comprobante
Restricción: no mostrar datos bancarios completos. Fallo adicional: el botón permite dos pagos consecutivos.

| ID | El usuario debe poder... | Verbo | Origen (tarea / restricción / fallo) |
|---|---|---|---|
| R1 | Identificar a qué persona y qué concepto está pagando, con su valor | Identificar | tarea |
| R2 | Reconocer su método de pago por los últimos 4 dígitos, sin ver el número completo | Reconocer | restricción |
| R3 | Pagar una sola vez aunque pulse el botón varias veces | Pagar | fallo |
| R4 | Ver que el pago está en proceso mientras espera | Ver | fallo |
| R5 | Corregir un dato inválido sin perder lo que ya escribió | Corregir | tarea |
| R6 | Obtener un comprobante que oculte los datos bancarios completos | Obtener | tarea / restricción |

Nota: Cancelar no es requisito; se atiende como H3 (control y libertad).
