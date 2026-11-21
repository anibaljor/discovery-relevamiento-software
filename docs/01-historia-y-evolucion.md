# 1. Historia y evolución del relevamiento de requisitos

El "relevamiento" (en inglés *requirements elicitation*) y el "discovery" son dos nombres para una misma pregunta de fondo: **¿qué hay que construir, para quién y por qué?** La forma de responderla cambió mucho en los últimos 60 años. Entender esa evolución ayuda a saber por qué conviven hoy documentos tan distintos como un SRS de 80 páginas y una historia de usuario escrita en una tarjeta.

> Nota: las fechas indican el momento en que una idea se publicó o se popularizó; muchas prácticas existían informalmente antes.

---

## Línea de tiempo resumida

| Época | Paradigma dominante | Artefactos típicos |
|-------|--------------------|--------------------|
| 1960–1970 | Desarrollo "a medida" sin método formal; análisis de sistemas | Memorandos, diagramas de flujo, especificaciones funcionales libres |
| 1970–1980 | **Modelo en cascada** y **análisis estructurado** | Especificación funcional, diagramas de flujo de datos (DFD), diccionario de datos |
| 1977–1980s | **JAD** (Joint Application Design) en IBM | Talleres facilitados, documento de diseño consensuado |
| 1980s | Metodologías estructuradas de gobierno (SSADM, Métrica en España) | Estudios de viabilidad, catálogos de requisitos |
| 1984–1994 | Estándares de ingeniería de requisitos | **IEEE 830** (SRS), modelo Kano, FURPS |
| 1987–1999 | **Orientación a objetos**: casos de uso, UML, RUP | Modelo de casos de uso, especificaciones de casos de uso, documento de Visión |
| 1990s | **RAD**, DSDM, prototipado | Prototipos, priorización MoSCoW, timeboxing |
| 1995–2000 | Ingeniería de requisitos como disciplina madura | Plantilla **Volere**, libros de Wiegers, Robertson, Cockburn |
| 2001 | **Manifiesto Ágil** | Historias de usuario, product backlog |
| 2003–2010 | Ágil se masifica (Scrum, XP), BDD, Lean Startup | INVEST, criterios de aceptación, Gherkin, MVP, Lean Canvas |
| 2005–2015 | **Design Thinking** y UX en el centro | Personas, mapas de empatía, journey maps, Double Diamond |
| 2008–2017 | Product management moderno | User Story Mapping, Impact Mapping, Inception Deck, Event Storming, Design Sprint, Lean Inception |
| 2010s–hoy | **Discovery continuo** / dual-track | Opportunity Solution Tree, entrevistas semanales, experimentos |
| 2023–hoy | Discovery asistido por IA | Transcripción y resumen de entrevistas, generación de borradores de historias y prototipos |

---

## 1960–1980: del "análisis de sistemas" a la cascada

En los primeros años, el software lo construían equipos que también conocían el negocio (bancos, defensa, gobierno). El "analista de sistemas" relevaba procesos manuales y los traducía a programas. No había un formato estándar.

En **1970**, Winston Royce publica *Managing the Development of Large Software Systems*, el artículo que se suele citar como origen del **modelo en cascada** (irónicamente, Royce advertía sobre sus riesgos). La idea que se impuso fue: **primero se especifican todos los requisitos, se firman, y recién después se diseña y construye**.

A fines de los 70, Tom DeMarco (*Structured Analysis and System Specification*, 1978), Ed Yourdon, Larry Constantine, y Gane & Sarson popularizan el **análisis estructurado**:

- **Diagramas de flujo de datos (DFD)**: qué datos entran, se transforman y salen.
- **Diccionario de datos**: definición de cada dato.
- **Especificaciones de procesos** (mini-specs, pseudocódigo, tablas de decisión).
- **Diagramas Entidad-Relación** (Peter Chen, 1976) para el modelo de datos.

**Legado:** la idea de que el relevamiento produce un *documento contractual* que se aprueba ("firma del cliente") antes de construir.

## 1977–1980s: JAD, la primera técnica colaborativa

IBM desarrolla **JAD (Joint Application Design)** a fines de los 70 (se atribuye a Chuck Morris y Tony Crawford). En lugar de entrevistar a usuarios uno por uno durante meses, se reúne a usuarios, decisores y técnicos en **talleres facilitados** de varios días con roles definidos (facilitador, escriba, patrocinador). Fue la semilla de los *workshops* de requisitos que se usan hoy (Inception, Event Storming, Design Sprint).

## 1980s: metodologías de gobierno

Los gobiernos crearon metodologías obligatorias para sus proyectos:

- **SSADM** (Reino Unido, 1981): incluye *Feasibility Study* y *Requirements Analysis/Specification* como etapas formales.
- **Merise** (Francia).
- **Métrica** (España, versión 3 en 2001), muy usada en Hispanoamérica como referencia: define el *Estudio de Viabilidad del Sistema (EVS)* y el *Análisis del Sistema de Información (ASI)* con catálogos de requisitos.

**Legado:** los pliegos de licitación pública y los documentos de "análisis funcional" que todavía se ven en el sector público.

## 1984–1998: estándares y calidad

- **Modelo Kano** (Noriaki Kano, 1984): no todos los requisitos generan la misma satisfacción (básicos, de desempeño, de deleite).
- **FURPS** (Robert Grady, HP, fines de los 80): clasificación de requisitos en Funcionalidad, Usabilidad, Confiabilidad (*Reliability*), Rendimiento (*Performance*) y Soporte. Luego **FURPS+**.
- **IEEE 830** (primera versión 1984, revisión más citada **1998**): *Recommended Practice for Software Requirements Specifications*. Define qué es un buen SRS (correcto, no ambiguo, completo, consistente, priorizado, verificable, modificable, trazable) y una estructura de índice que se copió durante décadas.
- **ISO 9126** (1991), antecesor de ISO/IEC 25010, para clasificar atributos de calidad (requisitos no funcionales).

## 1987–2000: casos de uso, UML y RUP

**Ivar Jacobson** presenta los **casos de uso** en 1987 y los formaliza en *Object-Oriented Software Engineering* (1992). Por primera vez el requisito se expresa como **una interacción entre un actor y el sistema para lograr un objetivo**, en lenguaje del usuario.

- **UML** (1997) estandariza el diagrama de casos de uso.
- **RUP** (Rational Unified Process, 1998) define artefactos como el **Documento de Visión**, el **Modelo de Casos de Uso**, las **Especificaciones Suplementarias** y el **Glosario**, y una fase llamada **Inception** (concepción) dedicada al discovery.
- **Alistair Cockburn** (*Writing Effective Use Cases*, 2000) populariza la plantilla de caso de uso "completamente vestida" con escenario principal, extensiones, precondiciones y garantías.

## 1990s: RAD, prototipado y DSDM

Como reacción a la lentitud de la cascada aparecen **RAD** (James Martin, 1991) y **DSDM** (1994). Aportes clave:

- **Prototipado** como técnica de relevamiento: el cliente reacciona mejor ante algo visible que ante un documento.
- **MoSCoW** (Dai Clegg, 1994, adoptado por DSDM): *Must, Should, Could, Won't*.
- **Timeboxing**: fijar tiempo y costo, y variar el alcance.

## 1995–2005: la ingeniería de requisitos como disciplina

Aparecen las obras de referencia que todavía se estudian:

- **Suzanne y James Robertson**: *Mastering the Requirements Process* (1999) y la **plantilla Volere**, con "tarjetas de requisito" que incluyen *fit criterion* (criterio de ajuste medible).
- **Karl Wiegers**: *Software Requirements* (1999; 3.ª ed. con Joy Beatty, 2013). Introduce el **documento de Visión y Alcance** y distingue requisitos de negocio, de usuario y funcionales.
- **Ellen Gottesdiener**: *Requirements by Collaboration* (2002), sobre talleres.
- **Hugh Beyer y Karen Holtzblatt**: *Contextual Design* (1998), con la **indagación contextual** (observar al usuario en su lugar de trabajo).
- **Peter Checkland**: *Soft Systems Methodology* (desde los 80), para problemas difusos con muchos actores.
- **BABOK** (IIBA, 1.ª versión 2005) e **IREB** (2006) profesionalizan el rol de analista de negocio / ingeniero de requisitos.

## 2001–2010: el giro ágil

El **Manifiesto Ágil** (2001) prioriza "colaboración con el cliente sobre negociación contractual" y "software funcionando sobre documentación extensiva". El relevamiento deja de ser una fase y pasa a ser **continuo**:

- **Historias de usuario** (Kent Beck, XP, fines de los 90). Formato "Como <rol> quiero <algo> para <beneficio>" (Connextra, ~2001). **3C de Ron Jeffries** (Card, Conversation, Confirmation, 2001). **INVEST** (Bill Wake, 2003). *User Stories Applied* de Mike Cohn (2004).
- **Product Backlog** en Scrum como lista viva y priorizada.
- **BDD** (Dan North, ~2006) y **Gherkin** (*Given/When/Then*, Cucumber, ~2008): criterios de aceptación ejecutables.
- **Specification by Example** (Gojko Adzic, 2011).
- **Lean Startup** (Eric Ries, 2011; Steve Blank *Customer Development*, 2005): hipótesis, MVP, validar antes de construir.
- **Business Model Canvas** (Osterwalder, 2008/2010) y **Lean Canvas** (Ash Maurya, 2010).

## 2005–2015: Design Thinking y UX

- **Design Thinking** (IDEO, Stanford d.school): empatizar → definir → idear → prototipar → testear.
- **Double Diamond** (UK Design Council, 2005): divergir/converger en el problema y luego en la solución.
- **Personas** (Alan Cooper, *The Inmates Are Running the Asylum*, 1999), **mapas de empatía**, **customer journey maps**, **Jobs to be Done** (Clayton Christensen, Tony Ulwick).

## 2008–hoy: product discovery moderno

- **Inception Deck** (Jonathan Rasmusson, *The Agile Samurai*, 2010): 10 preguntas para alinear un proyecto.
- **Impact Mapping** (Gojko Adzic, 2012): objetivo → actores → impactos → entregables.
- **Event Storming** (Alberto Brandolini, ~2013): taller con post-its de eventos de dominio, muy ligado a DDD.
- **User Story Mapping** (Jeff Patton, libro 2014): ordenar historias según el recorrido del usuario y cortar releases.
- **Design Sprint** (Jake Knapp, Google Ventures; libro *Sprint*, 2016): de problema a prototipo testeado en 5 días.
- **Lean Inception** (Paulo Caroli, ThoughtWorks, 2017): taller de una semana para definir un MVP; muy usado en Latinoamérica.
- **Inspired** (Marty Cagan, 2008; 2.ª ed. 2017) y el concepto de **dual-track agile**: discovery y delivery en paralelo.
- **Continuous Discovery Habits** (Teresa Torres, 2021): entrevistas semanales con clientes y el **Opportunity Solution Tree**.

## Hoy: convivencia de enfoques

En la práctica, ningún enfoque "ganó". Lo habitual es combinar:

- **Contexto contractual** (licitaciones, proyectos a precio fijo, industrias reguladas): siguen vivos el SRS, el BRD, la matriz de trazabilidad y la firma formal.
- **Producto propio o contrato tiempo y materiales**: discovery liviano (Lean Inception, story mapping, prototipos) y backlog evolutivo.
- **Siempre**: entender el problema y los objetivos de negocio antes de hablar de pantallas.

> Idea clave: **los documentos cambiaron, el objetivo no**. Todos los artefactos de esta historia intentan reducir el mismo riesgo: construir lo equivocado.
