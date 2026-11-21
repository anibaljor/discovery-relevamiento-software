# 2. Técnicas de relevamiento (elicitación)

"Elicitar" significa **sacar a la luz** algo que no está explícito. El cliente rara vez llega con los requisitos listos: llega con un problema, una idea o una solución ya imaginada. Las técnicas de este capítulo sirven para descubrir necesidades, reglas, restricciones y supuestos.

BABOK e IREB agrupan las técnicas en tres familias:

1. **Preguntar** (entrevistas, cuestionarios).
2. **Observar y analizar lo existente** (observación, análisis de documentos, de sistemas, de datos).
3. **Crear juntos** (talleres, prototipos, mapas colaborativos).

Ninguna técnica alcanza sola: lo normal es combinar 3 o 4.

---

## Tabla comparativa rápida

| Técnica | Mejor para | Costo | Riesgo principal |
|---------|-----------|-------|------------------|
| Entrevista | Entender contexto, dolores, objetivos | Bajo-medio | Sesgo del entrevistado; solo se obtiene lo que la persona sabe decir |
| Cuestionario / encuesta | Muchos usuarios, datos cuantitativos | Bajo | Preguntas mal formuladas, baja tasa de respuesta |
| Observación / shadowing | Conocimiento tácito, procesos reales | Medio | Efecto Hawthorne (la gente actúa distinto al ser observada) |
| Indagación contextual | Trabajo complejo, expertos | Medio-alto | Requiere entrevistador entrenado |
| Análisis documental | Reglas, normativas, procesos formales | Bajo | Documentos desactualizados |
| Análisis de sistema existente | Migraciones, reemplazos | Medio | Copiar los defectos del sistema viejo |
| Análisis de datos / métricas | Validar hipótesis con evidencia | Medio | Datos sucios o sin contexto |
| Taller / workshop (JAD) | Consenso entre áreas, decisiones rápidas | Alto (tiempo de muchas personas) | Dominado por la voz más fuerte |
| Brainstorming | Generar muchas ideas | Bajo | Ideas sin filtrar |
| Focus group | Opiniones y percepciones | Medio | Pensamiento grupal |
| Prototipado | Interfaces, validar comprensión | Bajo (papel) a alto (funcional) | El cliente cree que "ya está hecho" |
| Casos de uso / escenarios | Interacciones y flujos alternativos | Medio | Sobre-detalle |
| User Story Mapping | Visión de punta a punta y releases | Medio | Quedarse en features sin objetivos |
| Event Storming | Dominios complejos, procesos de negocio | Medio | Requiere facilitador experto |
| Design Sprint | Problema acotado con alta incertidumbre | Alto (5 días) | Poco útil para problemas ya resueltos |
| Benchmark / análisis de competencia | Mercado, estándares de facto | Bajo | Copiar sin entender el porqué |

---

## 2.1 Entrevistas

La técnica más antigua y más usada.

**Tipos:**
- **Estructurada**: preguntas fijas en orden fijo. Comparables entre entrevistados.
- **Semi-estructurada**: guion de temas con libertad para profundizar. *La más recomendada.*
- **No estructurada / abierta**: conversación libre. Útil al comienzo.

**Buenas prácticas:**
- Preparar un [guion](../plantillas/02-guion-de-entrevista.md) pero no leerlo como formulario.
- Preguntas **abiertas** ("¿Cómo hacen hoy…?", "Contame la última vez que…") antes que cerradas ("¿Necesitan un botón para…?").
- Preguntar por **hechos pasados concretos**, no por opiniones sobre el futuro ("¿usarías…?" produce respuestas poco confiables; ver *The Mom Test*, Rob Fitzpatrick, 2013).
- Técnica de los **5 porqués** para llegar a la causa raíz.
- Ir de a dos: uno pregunta, otro toma notas.
- Entrevistar a distintos niveles: patrocinador (por qué), mandos medios (cómo se controla), usuarios finales (cómo se hace realmente).
- Cerrar siempre con: "¿Qué no te pregunté que debería haber preguntado?" y "¿Con quién más debería hablar?".
- Enviar una [minuta](../plantillas/04-minuta-de-relevamiento.md) dentro de las 24–48 h para validar lo entendido.

## 2.2 Cuestionarios y encuestas

Útiles cuando hay muchos usuarios o están dispersos geográficamente. Complementan, no reemplazan, a las entrevistas.

- Usar antes (para preparar entrevistas) o después (para cuantificar lo que surgió en entrevistas).
- Mezclar preguntas cerradas (escala Likert, opción múltiple) con pocas abiertas.
- Hacer una prueba piloto con 2–3 personas.
- En contexto B2B, el [cuestionario de primer contacto](../plantillas/01-cuestionario-primer-contacto.md) se envía antes de la reunión inicial.

## 2.3 Observación, *shadowing* e indagación contextual

Las personas no saben describir todo lo que hacen: gran parte del conocimiento es **tácito** (atajos, planillas paralelas, "esto siempre lo resuelve Marta").

- **Observación pasiva**: mirar sin interrumpir.
- **Observación activa / shadowing**: acompañar a la persona durante su jornada y hacer preguntas.
- **Aprendiz (apprenticing)**: el analista intenta hacer la tarea guiado por el usuario.
- **Indagación contextual** (Beyer & Holtzblatt): modelo maestro–aprendiz en el lugar real de trabajo, con interpretación conjunta.

Qué buscar: excepciones, *workarounds*, planillas Excel "no oficiales", papelitos pegados en el monitor, interrupciones, sistemas que se usan en paralelo.

## 2.4 Análisis documental

Revisar lo que ya existe por escrito:

- Manuales de procedimientos, políticas, normativas y regulaciones.
- Formularios en papel o digitales (cada campo es un requisito de datos).
- Reportes que se generan hoy (¿quién los usa y para qué decisión?).
- Contratos, pliegos, RFP.
- Tickets de soporte y reclamos de clientes (fuente riquísima de dolores reales).

## 2.5 Análisis de sistemas existentes (ingeniería inversa)

En proyectos de migración o reemplazo:

- Inventario de pantallas, reportes, integraciones y procesos batch.
- Modelo de datos actual.
- Reglas de negocio embebidas en código o stored procedures.
- **Cuidado:** distinguir qué funcionalidad se usa de verdad (pedir métricas de uso) para no replicar lo que nadie necesita.

## 2.6 Análisis de datos y métricas

- Analítica web/app, logs, embudos de conversión.
- Volúmenes de transacciones (dimensionan requisitos no funcionales).
- Datos de soporte: categorías de tickets más frecuentes.

## 2.7 Talleres (workshops) y JAD

Sesiones facilitadas con representantes de varias áreas para **decidir juntos**.

**Roles clásicos (JAD):** patrocinador, facilitador neutral, escriba/documentador, usuarios clave, expertos técnicos, observadores.

**Estructura típica:**
1. Objetivo claro y agenda enviada antes.
2. Reglas de juego (timebox, una conversación a la vez, decisiones visibles).
3. Actividades de divergencia (generar) y convergencia (priorizar, votar).
4. Cierre con decisiones, pendientes y responsables.

Formatos modernos derivados: **Inception**, **Lean Inception**, **Event Storming**, **Design Sprint**, **Story Mapping** (ver abajo).

## 2.8 Brainstorming y técnicas de creatividad

- **Brainstorming** clásico (Alex Osborn, 1953): cantidad antes que calidad, sin críticas.
- **Brainwriting / 6-3-5**: cada persona escribe ideas en silencio; evita que domine la voz más fuerte.
- **Crazy 8s**: 8 bocetos en 8 minutos (Design Sprint).
- **Mapas mentales**.
- **Votación por puntos (dot voting)** para converger.

## 2.9 Focus groups

Grupo de 6–10 usuarios moderado para explorar percepciones. Más usado en marketing y productos de consumo que en software a medida. Riesgo: el pensamiento grupal.

## 2.10 Prototipado

"No sé lo que quiero, pero lo reconozco cuando lo veo." El prototipo es una de las técnicas de validación más efectivas.

| Fidelidad | Ejemplos | Para qué |
|-----------|----------|----------|
| Baja | Bocetos en papel, pizarra, wireframes | Explorar flujos y estructura, barato de tirar |
| Media | Wireframes navegables (Figma, Balsamiq) | Validar navegación y contenido |
| Alta | Mockups con diseño visual, prototipos interactivos | Validar experiencia y obtener aprobación |
| Funcional | Prueba de concepto (PoC), spike técnico | Validar factibilidad técnica |

- **Desechable vs. evolutivo**: dejar claro con el cliente si el prototipo se tira o se convierte en el producto.
- **Mago de Oz (Wizard of Oz)**: el usuario cree que el sistema es automático pero una persona responde detrás.
- **Riesgo**: un prototipo muy pulido genera la expectativa de que "ya está casi listo".

## 2.11 Casos de uso y escenarios

Describen **cómo un actor usa el sistema para lograr un objetivo**, incluyendo flujos alternativos y de excepción. Muy útiles para descubrir "¿y qué pasa si…?". Ver [plantilla](../plantillas/08-caso-de-uso.md).

## 2.12 Historias de usuario

Unidad mínima de requisito en ágil: "**Como** <rol>, **quiero** <acción> **para** <beneficio>". La historia es una *promesa de conversación*; el detalle está en los **criterios de aceptación**. Ver [plantilla](../plantillas/09-historia-de-usuario.md).

## 2.13 User Story Mapping (Jeff Patton)

Taller donde se arma un mapa en dos dimensiones:

- **Horizontal (backbone)**: las actividades del usuario en orden cronológico (el recorrido).
- **Vertical**: historias bajo cada actividad, ordenadas por prioridad.
- **Cortes horizontales**: definen releases o el MVP ("walking skeleton").

Evita el problema del backlog plano donde se pierde la visión de conjunto.

## 2.14 Event Storming (Alberto Brandolini)

Taller con post-its de colores en una pared larga:

- 🟧 **Eventos de dominio** ("Pedido confirmado") en pasado, en orden temporal.
- 🟦 **Comandos** que los disparan.
- 🟨 **Actores**.
- 🟪 **Políticas/reglas** ("cuando X, entonces Y").
- 🟥 **Puntos calientes** (dudas, conflictos).
- Sistemas externos, read models, agregados.

Niveles: *Big Picture* (todo el negocio), *Process Level*, *Design Level* (para DDD). Excelente para dominios complejos y para que expertos de negocio y desarrolladores hablen el mismo idioma.

## 2.15 Mapeo de procesos

- **BPMN** (Business Process Model and Notation): estándar para diagramar procesos *as-is* (como es hoy) y *to-be* (como será).
- **Diagramas de carriles (swimlanes)**.
- **SIPOC** (Suppliers, Inputs, Process, Outputs, Customers) para una vista de alto nivel.
- **Value Stream Mapping** (Lean) para detectar desperdicios.

## 2.16 Técnicas centradas en el usuario (UX)

- **Personas**: arquetipos de usuarios basados en investigación.
- **Mapa de empatía**: qué piensa, siente, dice, hace, ve, oye.
- **Customer / User Journey Map**: etapas, acciones, emociones y puntos de dolor a lo largo de una experiencia.
- **Service Blueprint**: journey + lo que pasa "detrás de escena".
- **Jobs to be Done**: "¿qué *trabajo* contrata el cliente a este producto para que haga?".
- **Card sorting**: los usuarios agrupan conceptos para diseñar la arquitectura de información.
- **Test de usabilidad** sobre prototipos.

## 2.17 Design Sprint (Google Ventures)

Proceso de 5 días: **Entender/Mapear → Bocetar → Decidir → Prototipar → Testear** con 5 usuarios reales. Útil cuando hay una pregunta de negocio crítica y mucha incertidumbre.

## 2.18 Técnicas de modelado para análisis

- **Diagrama de contexto**: el sistema como caja negra y sus interacciones externas. Excelente para acordar el alcance en la primera semana.
- **Modelo de dominio / diagrama entidad-relación**: conceptos del negocio y sus relaciones.
- **Diagramas de estado**: ciclo de vida de entidades (pedido, expediente, ticket).
- **Tablas y árboles de decisión**: reglas de negocio con muchas combinaciones.
- **Glosario / lenguaje ubicuo**: acordar qué significa cada término.

## 2.19 Benchmark y análisis de competencia

Revisar soluciones existentes en el mercado: qué hacen, qué se espera como estándar (requisitos "básicos" en términos de Kano), qué diferencia podría aportar la solución nueva.

---

## ¿Qué técnica elegir? Guía práctica

| Situación | Combinación sugerida |
|-----------|---------------------|
| Cliente con idea difusa, startup | Entrevistas + Lean Canvas + Lean Inception + prototipo de baja fidelidad |
| Digitalizar un proceso interno manual | Observación + análisis documental + BPMN as-is/to-be + casos de uso |
| Reemplazo de sistema legado | Análisis del sistema existente + métricas de uso + entrevistas + matriz de trazabilidad |
| Muchas áreas con intereses en conflicto | Mapa de stakeholders + talleres JAD + priorización MoSCoW |
| Dominio complejo (seguros, logística, finanzas) | Event Storming + glosario + modelo de dominio + tablas de decisión |
| Producto de consumo masivo | Entrevistas + encuestas + personas + journey map + tests de usabilidad |
| Licitación pública / precio fijo | Análisis del pliego + entrevistas + SRS formal + trazabilidad |
