# Discovery y relevamiento de requisitos de software

Repositorio **educativo** que reúne, ordena y explica los procedimientos, técnicas, plantillas y documentos que se usan (y se usaron históricamente) para **relevar con el cliente** y hacer el **discovery** de un proyecto o solicitud de desarrollo de software.

> Objetivo: entender *qué* se usa, *de dónde viene*, *para qué sirve* y *cuándo conviene* cada herramienta, desde la ingeniería de requisitos clásica hasta el product discovery moderno.

## Cómo leer este repositorio

| # | Documento | Qué vas a encontrar |
|---|-----------|---------------------|
| 1 | [Historia y evolución](docs/01-historia-y-evolucion.md) | Línea de tiempo: del análisis estructurado y el SRS en cascada a las historias de usuario, Lean Inception y el discovery continuo. |
| 2 | [Técnicas de relevamiento (elicitación)](docs/02-tecnicas-de-relevamiento.md) | Entrevistas, cuestionarios, observación, talleres JAD, prototipos, story mapping, event storming y más, con pros, contras y cuándo usar cada una. |
| 3 | [Documentos y artefactos](docs/03-documentos-y-artefactos.md) | Catálogo: Project Charter, Business Case, Visión y Alcance, BRD, SRS, PRD, casos de uso, historias de usuario, Lean Canvas, RFP, SOW, etc. |
| 4 | [Marcos y estándares](docs/04-marcos-y-estandares.md) | BABOK, IREB CPRE, ISO/IEC/IEEE 29148, IEEE 830, Volere, ISO 25010, PMBOK, SWEBOK. |
| 5 | [Técnicas de priorización y análisis](docs/05-priorizacion-y-analisis.md) | MoSCoW, Kano, RICE, WSJF, matriz valor/esfuerzo, análisis de stakeholders, trazabilidad. |
| 6 | [Proceso de discovery paso a paso](docs/06-proceso-de-discovery.md) | Una propuesta práctica que combina lo anterior, desde el primer contacto hasta el backlog inicial y la estimación. |
| 7 | [Errores comunes y buenas prácticas](docs/07-errores-comunes.md) | Antipatrones clásicos del relevamiento y cómo evitarlos. |
| — | [Glosario](docs/glosario.md) | Términos clave en español e inglés. |
| — | [Bibliografía y fuentes](docs/bibliografia.md) | Libros, estándares y autores de referencia para profundizar. |

## Plantillas listas para usar

En [`plantillas/`](plantillas/) hay plantillas en Markdown que podés copiar y adaptar:

| Plantilla | Fase | Uso |
|-----------|------|-----|
| [Cuestionario de primer contacto](plantillas/01-cuestionario-primer-contacto.md) | Pre-venta / inicio | Entender la solicitud antes de la primera reunión. |
| [Guion de entrevista](plantillas/02-guion-de-entrevista.md) | Relevamiento | Preguntas abiertas por bloque temático. |
| [Registro de stakeholders](plantillas/03-registro-de-stakeholders.md) | Inicio | Quién es quién, interés, influencia, RACI. |
| [Minuta de reunión de relevamiento](plantillas/04-minuta-de-relevamiento.md) | Relevamiento | Registrar acuerdos, dudas y próximos pasos. |
| [Documento de Visión y Alcance](plantillas/05-vision-y-alcance.md) | Definición | Problema, objetivos, alcance, fuera de alcance, riesgos. |
| [Lean Canvas / Product Vision Board](plantillas/06-lean-canvas-y-vision-board.md) | Definición | Hipótesis de negocio en una página. |
| [Inception Deck](plantillas/07-inception-deck.md) | Kick-off | Las 10 preguntas para alinear al equipo y al cliente. |
| [Especificación de caso de uso](plantillas/08-caso-de-uso.md) | Especificación | Formato estilo Cockburn. |
| [Historia de usuario + criterios de aceptación](plantillas/09-historia-de-usuario.md) | Especificación | Formato Connextra, INVEST y Gherkin. |
| [Esqueleto de SRS (ISO/IEC/IEEE 29148)](plantillas/10-srs-esqueleto.md) | Especificación formal | Estructura de un SRS clásico. |
| [Checklist de requisitos no funcionales](plantillas/11-checklist-requisitos-no-funcionales.md) | Especificación | Basado en ISO/IEC 25010. |
| [Matriz de trazabilidad](plantillas/12-matriz-de-trazabilidad.md) | Gestión | Objetivo → requisito → diseño → prueba. |
| [Checklist de cierre de discovery](plantillas/13-checklist-cierre-discovery.md) | Cierre | ¿Estamos listos para estimar y construir? |

## Estado

🌱 Primera versión: base de investigación. Ideas para seguir:

- [ ] Casos de estudio (ejemplos completos de un relevamiento ficticio de punta a punta).
- [ ] Versiones en formato Word/Google Docs de las plantillas.
- [ ] Comparativa de herramientas (Jira, Miro, Notion, Confluence, Figma) para cada artefacto.
- [ ] Guía específica para relevamientos con clientes del sector público (pliegos/licitaciones).

## Licencia

Contenido bajo [CC BY 4.0](LICENSE): podés usarlo y adaptarlo citando la fuente.
