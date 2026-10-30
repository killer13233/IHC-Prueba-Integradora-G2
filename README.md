# Pagos académicos · Prueba Práctica Integradora IHC

**Tarjetas:** IHC-03 e IHC-04 · **Variante:** B · Pagos académicos · **Grupo:** 2 · **Paralelo:** B
**Universidad Técnica de Ambato · FISEI · Software · Interacción Humano–Computador**

## Integrantes y roles
| Integrante | Usuario GitHub | Rol |
|---|---|---|
| Martín Palacios | [@killer13233](https://github.com/killer13233) | Diagnóstico (touchpoints, hallazgos), requisitos, sitemap, navegación, `inicio.html`, conducción de la prueba |
| David Pérez | [@DavidPe1307](https://github.com/DavidPe1307) | Issues, componentes, `pago.html` (validación y estados), `styles.css`, registro de la prueba |
| Sheyla Pacha | [@Zzzheyla](https://github.com/Zzzheyla) | Niveles emocionales, curvas antes/después, user flow, wireframes, trazabilidad, `confirmacion.html`, decisiones, prototipo v2 |

## Caso
| | IHC-03 | IHC-04 |
|---|---|---|
| Persona usuaria | Estudiante becado con presupuesto limitado | Representante que paga por otra persona (Ana Torres) |
| Tarea crítica | Consultar y pagar matrícula | Pagar y obtener comprobante |
| Restricción obligatoria | Costo total visible antes de aceptar | No mostrar datos bancarios completos |
| Fallo adicional | Aparece comisión inesperada al final ($90.00 → $92.50) | El botón permite dos pagos consecutivos |

## Cómo ejecutar
1. Clonar el repositorio: `git clone https://github.com/killer13233/IHC-Prueba-Integradora-G2.git`
2. Abrir `prototipo/v1/index.html` con doble clic (Chrome, Edge o Firefox). No necesita instalación ni servidor.
3. Elegir el caso con el parámetro de la URL:
   - IHC-03: `prototipo/v1/inicio.html?caso=03`
   - IHC-04: `prototipo/v1/inicio.html?caso=04`
4. Recorrido: **Inicio → Formulario de pago → (Error de pago) → Confirmación**.
5. Teclado: `Tab` / `Shift+Tab` mueven el foco · `Enter` activa · `Esc` cancela o vuelve al inicio.
6. Simular el rechazo del banco: en IHC-03 una tarjeta que termine en `0000`; en IHC-04 un correo que termine en `@falla.com`.
7. Versión corregida: los mismos archivos en `prototipo/v2/` (por ejemplo `prototipo/v2/inicio.html?caso=03`).

## Instrucciones de prueba
Guion completo y reglas para no dirigir al participante: [`pruebas/guion-facilitador.md`](pruebas/guion-facilitador.md). Registro: [`pruebas/sesion.md`](pruebas/sesion.md).
- **Tarea 1 (IHC-03):** "Usted es estudiante becado y este mes tiene poco dinero. Necesita pagar su matrícula desde esta página. Hágalo como lo haría normalmente y avise cuando crea que terminó."
- **Tarea 2 (IHC-04):** "Usted va a pagar la pensión de octubre de Ana Torres, una familiar suya, con tarjeta. Quiere dejar el pago hecho y quedarse con un comprobante. Hágalo como lo haría normalmente y avise cuando crea que terminó."

## Versiones
| | v1 (`prototipo/v1/`) | v2 (`prototipo/v2/`) |
|---|---|---|
| IHC-03 | La comisión de $2.50 aparece recién al pagar | Comisión y total $92.50 visibles desde Inicio |
| IHC-04 | El botón Pagar sigue activo y permite dos pagos | El botón se bloquea al primer clic y explica el estado |
| Rechazo del banco | «No se pudo procesar el pago. Inténtalo de nuevo.» | Indica «No se hizo ningún cobro» y conserva los datos |

Evidencias antes/después: [`evidencias/`](evidencias/) · Curvas: [`diagramas/curva-antes.png`](diagramas/curva-antes.png), [`diagramas/curva-despues.png`](diagramas/curva-despues.png)

## Documentación
| Fase | Archivos |
|---|---|
| F1 Diagnóstico | [`docs/diagnostico.md`](docs/diagnostico.md) · [`docs/niveles-emocionales.md`](docs/niveles-emocionales.md) · [`diagramas/curva-antes.png`](diagramas/curva-antes.png) |
| F2 Arquitectura | [`docs/requisitos.md`](docs/requisitos.md) · [`diagramas/sitemap.png`](diagramas/sitemap.png) · [`diagramas/navegacion.md`](diagramas/navegacion.md) · [`diagramas/user-flow.png`](diagramas/user-flow.png) · [`docs/componentes.md`](docs/componentes.md) · [`wireframes/`](wireframes/) · [`docs/trazabilidad.md`](docs/trazabilidad.md) |
| F3 Prototipo | [`prototipo/v1/`](prototipo/v1/) · [`docs/decisiones.md`](docs/decisiones.md) |
| F4 Prueba | [`pruebas/guion-facilitador.md`](pruebas/guion-facilitador.md) · [`pruebas/sesion.md`](pruebas/sesion.md) · [`prototipo/v2/`](prototipo/v2/) · [`diagramas/curva-despues.png`](diagramas/curva-despues.png) |
| F5 Defensa | [`docs/defensa.md`](docs/defensa.md) |

## Issues y Pull Requests
- Issues: [#3](../../issues/3) · [#5](../../issues/5) · [#6](../../issues/6) — [ver todos](../../issues?q=is%3Aissue)
- Pull Requests: [#1](../../pull/1) · [#2](../../pull/2) · [#4](../../pull/4) · [#7](../../pull/7) — [ver todos](../../pulls?q=is%3Apr)

## Decisiones
Ver [`docs/decisiones.md`](docs/decisiones.md): prototipo en HTML ejecutable (D1), un solo prototipo para los dos casos con `?caso=` (D3), fallo conservado en v1 (D4), foco y teclado (D5) y correcciones de v2 (D11–D13).

## Commit final
<enlace al último commit de main al cerrar la prueba>

## Uso de IA
Se usó Claude (Anthropic) como asistente para estructurar plantillas, redactar borradores y revisar documentos. El equipo revisó, adaptó y es responsable del contenido entregado.
