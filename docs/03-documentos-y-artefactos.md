# 3. Documentos y artefactos del discovery

Catálogo de los documentos que se usan (o se usaron) para registrar lo relevado. Están ordenados aproximadamente según **el momento del proyecto** en que aparecen.

Para cada uno: **qué es**, **origen**, **contenido típico**, **cuándo usarlo** y **riesgos**.

---

## Mapa general

```
 PRE-VENTA / INICIO        DEFINICIÓN             ESPECIFICACIÓN               GESTIÓN
 ─────────────────         ──────────             ──────────────               ───────
 RFI / RFP                 Visión y Alcance       SRS / FRD                    Matriz de trazabilidad
 Cuestionario inicial      Business Case          Casos de uso                 Registro de cambios
 Propuesta comercial       Project Charter        Historias de usuario         Registro de decisiones (ADR)
 NDA                       BRD                    Criterios de aceptación      Backlog priorizado
 Estudio de viabilidad     PRD                    Prototipos / wireframes
                           Lean / Business Canvas Modelo de datos / dominio
                           Inception Deck         Requisitos no funcionales
                           Registro de stakeholders Glosario
                                                  SOW / Anexo técnico del contrato
```

---

## A. Documentos de pre-venta e inicio

### A.1 RFI — Request for Information (Solicitud de información)
- **Qué es:** el cliente pide a varios proveedores información general sobre capacidades, experiencia y enfoques. No es una oferta.
- **Cuándo:** el cliente todavía está explorando el mercado.

### A.2 RFP — Request for Proposal (Solicitud de propuesta) / Pliego
- **Qué es:** el cliente describe la necesidad y pide propuestas formales con precio y plazo. En el sector público toma la forma de **pliego de condiciones técnicas y particulares**.
- **Contenido típico:** contexto, objetivos, alcance, requisitos funcionales y no funcionales, criterios de evaluación, condiciones comerciales, plazos.
- **Variantes:** RFQ (*Request for Quotation*, cuando lo único a comparar es el precio).
- **Riesgo:** suele estar escrito sin discovery previo; los requisitos pueden ser incompletos o ser soluciones disfrazadas de necesidades.

### A.3 Cuestionario de primer contacto / *Discovery questionnaire*
- **Qué es:** formulario que la consultora envía antes o después de la primera reunión para entender la solicitud.
- **Ver:** [plantilla](../plantillas/01-cuestionario-primer-contacto.md).

### A.4 Estudio de viabilidad / factibilidad
- **Origen:** metodologías estructuradas (SSADM *Feasibility Study*, Métrica *EVS*).
- **Contenido:** viabilidad técnica, económica, operativa, legal y de plazos (TELOS: *Technical, Economic, Legal, Operational, Scheduling*). Alternativas de solución (construir, comprar, adaptar).

### A.5 Propuesta técnico-comercial
- **Qué es:** la respuesta del proveedor: entendimiento del problema, solución propuesta, enfoque, equipo, cronograma, supuestos, exclusiones y precio.
- **Clave:** la sección de **supuestos y exclusiones** es tan importante como el alcance.

### A.6 NDA — Acuerdo de confidencialidad
Suele firmarse antes de que el cliente comparta información sensible del negocio.

---

## B. Documentos de definición (el "por qué" y el "qué" de alto nivel)

### B.1 Business Case (Caso de negocio)
- **Qué es:** justificación económica del proyecto.
- **Contenido:** problema u oportunidad, opciones evaluadas, costos, beneficios esperados, ROI / payback, riesgos, recomendación.
- **Quién lo escribe:** normalmente el cliente (o el área de negocio), a veces con ayuda del proveedor.

### B.2 Project Charter (Acta de constitución del proyecto)
- **Origen:** PMBOK (PMI).
- **Qué es:** documento que **autoriza formalmente** el proyecto y nombra al director/a del proyecto.
- **Contenido:** propósito, objetivos medibles, requisitos de alto nivel, supuestos, restricciones, riesgos iniciales, hitos, presupuesto resumido, stakeholders clave, criterios de éxito, patrocinador.

### B.3 Documento de Visión y Alcance (*Vision and Scope Document*)
- **Origen:** Karl Wiegers (*Software Requirements*); el **Documento de Visión** de RUP es similar.
- **Qué es:** el documento más útil del discovery para proyectos medianos. Acuerda el problema, los objetivos de negocio y los límites del proyecto antes de entrar en detalle.
- **Contenido:** requisitos de negocio, oportunidad, objetivos y métricas de éxito, visión de la solución, características principales, **alcance y limitaciones (incluido "fuera de alcance")**, contexto de negocio, stakeholders, supuestos y dependencias.
- **Ver:** [plantilla](../plantillas/05-vision-y-alcance.md).

### B.4 BRD — Business Requirements Document
- **Qué es:** documento de requisitos **de negocio**: qué necesita lograr la organización, independientemente de la tecnología.
- **Contenido:** resumen ejecutivo, objetivos, alcance, stakeholders, procesos actuales y futuros, requisitos de negocio, reglas de negocio, supuestos, restricciones, glosario.
- **Relación:** BRD (negocio) → FRD/SRS (sistema). En muchas organizaciones se fusionan.

### B.5 PRD — Product Requirements Document
- **Origen:** gestión de producto en empresas de tecnología (Microsoft, Intel, luego startups).
- **Qué es:** describe un producto o una funcionalidad desde la perspectiva del usuario: problema, usuarios objetivo, objetivos, métricas, historias/casos, requisitos, diseño, preguntas abiertas, fuera de alcance.
- **Tendencia actual:** PRDs cortos ("one-pagers") y vivos, enlazados a prototipos y backlog, en lugar de documentos extensos.

### B.6 Lean Canvas / Business Model Canvas / Product Vision Board
- **Business Model Canvas** (Alex Osterwalder, 2008/2010): 9 bloques del modelo de negocio.
- **Lean Canvas** (Ash Maurya, 2010): adaptación para startups: problema, segmentos, propuesta de valor única, solución, canales, ingresos, costos, métricas clave, ventaja injusta.
- **Product Vision Board** (Roman Pichler): visión, grupo objetivo, necesidades, producto, objetivos de negocio.
- **Ver:** [plantilla](../plantillas/06-lean-canvas-y-vision-board.md).

### B.7 Inception Deck
- **Origen:** Jonathan Rasmusson, *The Agile Samurai* (2010).
- **Qué es:** 10 preguntas/ejercicios para alinear expectativas al inicio: ¿por qué estamos aquí?, *elevator pitch*, caja del producto, lista de "lo que NO es", vecindario (stakeholders), solución técnica, qué nos quita el sueño, tamaño, qué se negocia (trade-offs), costo.
- **Ver:** [plantilla](../plantillas/07-inception-deck.md).

### B.8 Lean Inception
- **Origen:** Paulo Caroli (2017).
- **Qué es:** taller de ~5 días que combina Inception Deck, personas, journey, brainstorming de funcionalidades, revisión técnica/de negocio/UX y el **Canvas MVP**, para terminar con un **secuenciador de funcionalidades** (qué entra en cada incremento).

### B.9 Registro de stakeholders (interesados)
- **Contenido:** nombre, rol, área, interés, influencia, expectativas, nivel de compromiso, canal de comunicación.
- Suele acompañarse de una **matriz poder/interés** y una **matriz RACI**.
- **Ver:** [plantilla](../plantillas/03-registro-de-stakeholders.md).

### B.10 Impact Map y Opportunity Solution Tree
- **Impact Map** (Gojko Adzic): Objetivo (*¿por qué?*) → Actores (*¿quién?*) → Impactos (*¿cómo cambia su comportamiento?*) → Entregables (*¿qué hacemos?*). Conecta cada funcionalidad con un objetivo de negocio.
- **Opportunity Solution Tree** (Teresa Torres): Resultado deseado → Oportunidades (necesidades, dolores) → Soluciones → Experimentos.

---

## C. Documentos de especificación (el "qué" en detalle)

### C.1 SRS — Software Requirements Specification
- **Origen:** IEEE 830 (1984/1998), reemplazado por **ISO/IEC/IEEE 29148** (2011, revisado 2018).
- **Qué es:** especificación completa de lo que el sistema debe hacer y cómo debe comportarse. Históricamente, el documento contractual por excelencia.
- **Estructura clásica (IEEE 830):** 1. Introducción (propósito, alcance, definiciones, referencias, visión general); 2. Descripción general (perspectiva del producto, funciones, características de usuarios, restricciones, supuestos); 3. Requisitos específicos (interfaces externas, funciones, rendimiento, base de datos lógica, restricciones de diseño, atributos de calidad).
- **Características de un buen requisito:** correcto, no ambiguo, completo, consistente, priorizado, verificable, modificable, trazable.
- **Ver:** [esqueleto](../plantillas/10-srs-esqueleto.md).

### C.2 FRD / FSD — Functional Requirements / Specification Document ("Análisis funcional")
- **Qué es:** detalle funcional del sistema: pantallas, campos, validaciones, reglas, flujos, reportes. En Hispanoamérica se lo llama comúnmente **"análisis funcional"** o **"especificación funcional"**.
- Suele incluir wireframes y casos de uso.

### C.3 Especificación de casos de uso
- **Origen:** Ivar Jacobson (1987/1992); plantilla popularizada por Alistair Cockburn (2000).
- **Contenido:** nombre (verbo + objeto), actor principal, stakeholders e intereses, nivel, precondiciones, garantías mínimas y de éxito, disparador, escenario principal de éxito, extensiones (flujos alternativos y de excepción), requisitos especiales, frecuencia.
- **Diagrama de casos de uso (UML):** vista general de actores y casos; es un índice, no la especificación.
- **Ver:** [plantilla](../plantillas/08-caso-de-uso.md).

### C.4 Historias de usuario y criterios de aceptación
- **Formato Connextra:** *Como* [rol] *quiero* [funcionalidad] *para* [beneficio].
- **3C:** Card (tarjeta), Conversation (conversación), Confirmation (criterios de aceptación).
- **INVEST:** Independiente, Negociable, Valiosa, Estimable, Pequeña (*Small*), Testeable.
- **Criterios de aceptación:** lista de reglas o escenarios **Gherkin** (*Dado / Cuando / Entonces*).
- **Agrupación:** Tema → Épica → Historia → Tarea.
- **Definition of Ready / Definition of Done:** acuerdos sobre cuándo una historia está lista para desarrollarse y cuándo se considera terminada.
- **Ver:** [plantilla](../plantillas/09-historia-de-usuario.md).

### C.5 Especificación de requisitos no funcionales (atributos de calidad)
- Rendimiento, disponibilidad, seguridad, usabilidad, accesibilidad, mantenibilidad, portabilidad, cumplimiento normativo, etc.
- Clasificaciones: **FURPS+**, **ISO/IEC 25010**.
- Deben ser **medibles** ("el 95 % de las búsquedas responde en menos de 2 s con 500 usuarios concurrentes", no "el sistema debe ser rápido").
- **Ver:** [checklist](../plantillas/11-checklist-requisitos-no-funcionales.md).

### C.6 Prototipos, wireframes y mockups
Hoy funcionan como especificación visual. Complementan (no reemplazan) las reglas de negocio y criterios de aceptación.

### C.7 Modelos de análisis
- Diagrama de contexto, DFD, modelo de dominio / diagrama entidad-relación, diagramas de estado, BPMN de procesos *to-be*, tablas de decisión.

### C.8 Glosario
Lista de términos del negocio y su significado acordado. Barato y de enorme valor: muchos malentendidos vienen de usar la misma palabra para cosas distintas ("cliente", "pedido", "activo").

### C.9 Catálogo de reglas de negocio
Reglas independientes de la interfaz: cálculos, políticas, restricciones ("un cliente con deuda vencida mayor a 90 días no puede generar pedidos"). Conviene mantenerlas separadas para reutilizarlas.

### C.10 Tarjeta de requisito Volere (*snow card*)
- **Origen:** Robertson & Robertson.
- **Campos:** ID, tipo, evento/caso relacionado, descripción, **justificación (*rationale*)**, origen, **criterio de ajuste (*fit criterion*)**, satisfacción y disgusto del cliente (escala 1–5), dependencias, conflictos, materiales de soporte, historial.

### C.11 SOW — Statement of Work (Declaración de trabajo) / Anexo de alcance del contrato
- **Qué es:** documento contractual que detalla entregables, alcance, plazos, criterios de aceptación, responsabilidades de cada parte, supuestos y exclusiones.
- Suele referenciar a la Visión y Alcance, al SRS o al backlog inicial.

---

## D. Documentos de gestión de requisitos

### D.1 Matriz de trazabilidad de requisitos (RTM)
Vincula objetivos de negocio ↔ requisitos ↔ diseño ↔ código ↔ casos de prueba. Permite saber qué se afecta ante un cambio y demostrar cobertura. Obligatoria en industrias reguladas (salud, aviación, finanzas). Ver [plantilla](../plantillas/12-matriz-de-trazabilidad.md).

### D.2 Registro de cambios / Solicitud de cambio (*Change Request*)
Formulario para pedir cambios al alcance aprobado: descripción, justificación, impacto (alcance, costo, plazo, riesgo), decisión del comité de control de cambios (CCB).

### D.3 Registro de decisiones / ADR (*Architecture Decision Record*)
Qué se decidió, cuándo, por quién, alternativas consideradas y por qué. Evita "re-discutir" lo mismo meses después.

### D.4 Registro de supuestos, riesgos, dudas y dependencias (RAID log)
*Risks, Assumptions, Issues, Dependencies.* Durante el discovery, la lista de **preguntas abiertas** es uno de los artefactos más importantes.

### D.5 Minutas de reunión
Registro de cada sesión de relevamiento. Ver [plantilla](../plantillas/04-minuta-de-relevamiento.md).

### D.6 Product Backlog
Lista priorizada y viva de todo lo que se podría hacer en el producto. En ágil reemplaza al SRS como "fuente de verdad" de requisitos.

---

## E. ¿Cuánta documentación hace falta?

| Factor | Más documentación formal | Menos documentación, más conversación |
|--------|-------------------------|-------------------------------------|
| Tipo de contrato | Precio fijo, licitación | Tiempo y materiales, equipo dedicado |
| Regulación | Salud, banca, aviación, sector público | Producto interno, startup |
| Distancia con el cliente | Cliente lejano, poca disponibilidad | Product Owner dedicado al equipo |
| Rotación del equipo | Alta, varios proveedores | Equipo estable |
| Criticidad | Vida humana, dinero, datos sensibles | Bajo impacto si falla |
| Tamaño | Cientos de requisitos, varios equipos | Un equipo pequeño |

> Regla práctica: **documentar lo suficiente para que dos personas que no estuvieron en la reunión entiendan lo mismo**.
