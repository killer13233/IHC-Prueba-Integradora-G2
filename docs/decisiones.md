# Registro de decisiones

| N.º | Decisión | Motivo | Alternativa descartada |
|---|---|---|---|
| D1 | Prototipo **ejecutable en HTML + CSS + JS**, fidelidad media | El riesgo del caso es de confianza en montos y estados: el usuario debe ver valores, comisiones y mensajes reales. En HTML se prueban foco, teclado y validación de verdad | Papel o Figma: no permiten probar teclado ni validación real |
| D2 | Prototipo **vertical**: solo el flujo de pago (Inicio → Formulario de pago → Error → Confirmación) | La prueba mide si la persona completa la tarea crítica y se recupera de un error | Prototipo horizontal de todo el portal |
| D3 | **Un solo prototipo para los dos casos** con el parámetro `?caso=03` / `?caso=04` | Las cuatro pantallas son las mismas; cambian los datos. Evita duplicar archivos y mantiene los nombres iguales en todos los artefactos | Dos carpetas de prototipo separadas |
| D4 | **v1 conserva el fallo** de cada tarjeta (comisión tardía en 03, doble pago en 04) | Permite observarlo en la prueba y comparar v1 → v2 con evidencia | Corregirlo desde v1 sin poder comparar |
| D5 | **Foco y teclado**: foco inicial en el título de cada pantalla, Tab/Shift+Tab, Enter activa, Esc cancela o vuelve al inicio, contorno de foco visible | La guía exige navegación por teclado y foco visible | Probar solo con mouse |
| D6 | **Validación contextual**: mensaje bajo el campo, foco en el campo con error y datos conservados | H5 y H9: el usuario corrige sin volver a escribir todo | Mensaje general al final del formulario |
| D7 | Datos bancarios **enmascarados** (•••• 4821) en todas las pantallas de IHC-04 | Restricción obligatoria de la tarjeta | Mostrar el número completo |
| D8 | «Volver al inicio» lleva a `inicio.html?caso=XX` conservando el caso | El usuario regresa al mismo contexto (H4, regreso definido) | Volver a una página genérica |
| D9 | Participantes anotados como P1, P2 | Protege la identidad | Usar nombres |
| D10 | Uso de IA declarado en el README | Transparencia; autorizado por el docente | No declararlo |
| D11 | **v2 · IHC-03:** la comisión de $2.50 y el total $92.50 se muestran desde Inicio, y el total no cambia en el Formulario de pago | Corrige el hallazgo IHC-03·H1 (Issue #5) y cumple R2 y R3: el estudiante conoce el costo total antes de aceptar (H1, H5) | Mantener la comisión al final con un aviso |
| D12 | **v2 · IHC-04:** el botón Pagar se deshabilita al primer clic, cambia a «Procesando…» y el aviso dice «No cierres esta página ni vuelvas a pulsar Pagar» | Corrige el hallazgo IHC-04·H1 (Issue #6) y cumple R3 y R4: un solo pago (H5) y estado visible (H1) | Pedir confirmación en una ventana emergente |
| D13 | **v2 · ambos casos:** el rechazo del banco dice «No se hizo ningún cobro» y conserva los datos escritos | Corrige IHC-03·H2 e IHC-04·H3 (Issue #9): el usuario sabe que puede reintentar sin pagar dos veces (H9) | Mensaje genérico «Inténtalo de nuevo» |
| D14 | Se conserva **v1** sin cambios en `prototipo/v1/` y la corrección va en `prototipo/v2/` | La guía pide comparar v1 y v2 | Sobrescribir v1 |
| D15 | **v2 · por la prueba con P1:** texto de ayuda bajo cada campo, indicador de pasos y recuadro con quién paga y a qué entidad | P1 no sabía cómo llenar los campos y pidió ver los pasos y la entidad (H1, H5) | Dejar solo el placeholder dentro del campo |
