# Componentes (Atomic Design)

| Componente | Nivel | Estados | Requisito | Dónde aparece |
|---|---|---|---|---|
| Etiqueta + campo de texto | Átomo | normal, foco, error | IHC-03 R5, IHC-04 R5 | Formulario de pago |
| Mensaje de error junto al campo | Átomo | oculto, visible | IHC-03 R5, IHC-04 R5 | Formulario de pago |
| Botón Pagar | Átomo | normal, foco, deshabilitado (solo IHC-03; en IHC-04 queda activo en v1) | IHC-03 R4, IHC-04 R3 | Formulario de pago |
| Botón Cancelar | Átomo | normal, foco | H3 (control y libertad) | Inicio, Formulario de pago |
| Contador de pagos enviados (solo v1) | Átomo | visible | IHC-04 R3, R4 | Formulario de pago |
| Fila de resumen (concepto y valor) | Molécula | normal | IHC-03 R2, IHC-04 R1 | Inicio, Formulario de pago, Confirmación |
| Método de pago (últimos 4 dígitos) | Molécula | normal | IHC-04 R2, R6 | Formulario de pago, Confirmación |
| Aviso de estado (procesando, error, éxito) | Molécula | carga, error, éxito | IHC-04 R4 | Formulario de pago |
| Resumen de costo total | Organismo | normal, con comisión | IHC-03 R2, R3 | Inicio, Formulario de pago |
| Formulario de pago | Organismo | normal, error, carga, éxito | IHC-03 R4, R5, IHC-04 R3, R5 | Formulario de pago |
| Comprobante | Organismo | normal | IHC-03 R6, IHC-04 R6 | Confirmación |
| Plantilla de pantalla (título + contenido + acciones) | Plantilla | — | Todos | Las cuatro pantallas |
