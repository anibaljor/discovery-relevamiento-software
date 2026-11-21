# 6. Proceso de discovery paso a paso

Propuesta práctica que combina las técnicas y documentos de los capítulos anteriores. Está pensada para una **consultora o equipo que recibe una solicitud de desarrollo** de un cliente. Es un punto de partida: hay que adaptarla al tamaño y tipo de proyecto.

**Duración orientativa:** de 1 semana (proyecto chico) a 6–8 semanas (proyecto grande o regulado).

---

## Vista general

```
 Fase 0           Fase 1            Fase 2              Fase 3             Fase 4             Fase 5
 PREPARACIÓN  →   ENTENDER EL   →   EXPLORAR Y      →   DEFINIR LA     →   DETALLAR Y     →   CERRAR Y
                  PROBLEMA          MODELAR             SOLUCIÓN           VALIDAR            ACORDAR
 ───────────      ─────────────     ────────────        ────────────       ──────────         ─────────
 Primer contacto  Kick-off          Entrevistas         Visión y alcance   Historias / CU     Estimación
 Cuestionario     Stakeholders      Observación         Story map / MVP    Prototipos         Roadmap
 NDA              Objetivos         Procesos as-is      Priorización       No funcionales     Propuesta / SOW
 Investigación    Contexto          Event Storming      Arquitectura       Validación         Aprobación
 previa                             Datos y sistemas    preliminar
```

> No es una cascada: las fases se superponen y se itera. Por ejemplo, un prototipo en la fase 4 puede revelar un stakeholder olvidado de la fase 1.

---

## Fase 0 — Preparación (antes de la primera reunión)

**Objetivo:** llegar a la primera reunión sabiendo lo básico y con buenas preguntas.

Actividades:
1. Recibir la solicitud (email, RFP, llamada).
2. Investigar al cliente: industria, tamaño, competidores, noticias, sistemas que probablemente usa.
3. Enviar el [cuestionario de primer contacto](../plantillas/01-cuestionario-primer-contacto.md).
4. Firmar NDA si corresponde.
5. Acordar el **formato del discovery** (¿es pago?, ¿cuánto dura?, ¿qué se entrega al final?).

> 💡 Buena práctica comercial: ofrecer el discovery como un **servicio separado y pago** con entregables definidos. Reduce el riesgo para ambas partes antes de comprometer un precio cerrado del desarrollo.

Salida: entendimiento inicial, lista de preguntas, agenda del kick-off.

---

## Fase 1 — Entender el problema (el "por qué")

**Objetivo:** acordar el problema, los objetivos de negocio y quiénes participan, **antes de hablar de soluciones**.

Actividades:
1. **Reunión de kick-off** con patrocinador y referentes clave.
2. Preguntas centrales:
   - ¿Qué problema u oportunidad hay? ¿Cómo se manifiesta hoy?
   - ¿Por qué ahora? ¿Qué pasa si no se hace nada?
   - ¿Cómo sabremos que el proyecto fue un éxito? (métricas)
   - ¿Qué restricciones hay? (presupuesto, fecha, tecnología, normativa)
   - ¿Qué se intentó antes?
3. Armar el [registro de stakeholders](../plantillas/03-registro-de-stakeholders.md) y la matriz poder/interés.
4. Opcional: ejercicios del [Inception Deck](../plantillas/07-inception-deck.md) ("¿por qué estamos aquí?", "elevator pitch", "lista de lo que NO es").
5. Planificar el resto del discovery: a quién entrevistar, qué observar, qué documentos pedir.

Salidas: objetivos de negocio, stakeholders, plan de relevamiento, primeras restricciones y supuestos.

---

## Fase 2 — Explorar y modelar el dominio (el "cómo es hoy")

**Objetivo:** entender en profundidad la situación actual y las necesidades de cada tipo de usuario.

Actividades (elegir según el caso, ver [capítulo 2](02-tecnicas-de-relevamiento.md)):
- **Entrevistas** semi-estructuradas con cada perfil ([guion](../plantillas/02-guion-de-entrevista.md)).
- **Observación / shadowing** de usuarios reales.
- **Análisis documental**: procedimientos, formularios, reportes, normativa.
- **Análisis de sistemas existentes** e integraciones.
- **Mapeo de procesos as-is** (BPMN, swimlanes) o **Event Storming** big picture.
- **Personas** y **journey maps** si hay usuarios externos/consumidores.
- **Glosario** del negocio desde el día uno.
- **Minuta** después de cada sesión ([plantilla](../plantillas/04-minuta-de-relevamiento.md)).

Salidas: procesos actuales, dolores priorizados, perfiles de usuario, glosario, diagrama de contexto, lista de preguntas abiertas.

---

## Fase 3 — Definir la solución (el "qué" de alto nivel)

**Objetivo:** acordar qué se va a construir, qué no, y en qué orden.

Actividades:
1. **Procesos to-be** o journey futuro.
2. Taller de ideación de funcionalidades (brainstorming, Lean Inception).
3. **User Story Mapping**: backbone de actividades y cortes de releases / MVP.
4. **Priorización** con el cliente (MoSCoW, valor/esfuerzo; ver [capítulo 5](05-priorizacion-y-analisis.md)).
5. **Arquitectura preliminar**: integraciones, tecnología candidata, riesgos técnicos, necesidad de pruebas de concepto.
6. Redactar el [Documento de Visión y Alcance](../plantillas/05-vision-y-alcance.md), con **"fuera de alcance"** explícito.

Salidas: visión y alcance, story map, MVP definido, arquitectura de alto nivel, riesgos.

---

## Fase 4 — Detallar y validar (el "qué" en detalle)

**Objetivo:** bajar a un nivel de detalle suficiente para estimar y empezar a construir, y verificar que se entendió bien.

Nivel de detalle según el contexto:
- **Ágil / tiempo y materiales:** detallar solo el primer release (épicas + historias del MVP con criterios de aceptación); el resto queda a nivel épica.
- **Precio fijo / licitación:** detallar todo el alcance (casos de uso o SRS/análisis funcional completo).

Actividades:
- [Historias de usuario](../plantillas/09-historia-de-usuario.md) con criterios de aceptación, o [casos de uso](../plantillas/08-caso-de-uso.md).
- Reglas de negocio y tablas de decisión.
- Modelo de datos / dominio preliminar.
- [Requisitos no funcionales](../plantillas/11-checklist-requisitos-no-funcionales.md) medibles.
- **Prototipos** (wireframes → mockups) y validación con usuarios reales.
- **Revisión** de todo con stakeholders (walkthrough).
- Para contextos formales: [SRS](../plantillas/10-srs-esqueleto.md) y [matriz de trazabilidad](../plantillas/12-matriz-de-trazabilidad.md).

Salidas: backlog inicial o especificación, prototipos validados, requisitos no funcionales, preguntas abiertas resueltas (o explícitamente asumidas).

---

## Fase 5 — Cerrar y acordar

**Objetivo:** convertir lo relevado en un acuerdo para construir.

Actividades:
1. **Estimación** (rango, no un número único; explicitar supuestos).
2. **Roadmap** / plan de releases.
3. Propuesta técnico-comercial o **SOW** con entregables, supuestos, exclusiones, criterios de aceptación y proceso de gestión de cambios.
4. **Presentación de cierre** del discovery al patrocinador.
5. **Aprobación formal**.
6. Repasar el [checklist de cierre](../plantillas/13-checklist-cierre-discovery.md).

Entregables típicos del discovery:
- Documento de Visión y Alcance.
- Story map / backlog priorizado del MVP.
- Prototipos navegables.
- Arquitectura de alto nivel y riesgos técnicos.
- Estimación y roadmap.
- Glosario, registro de stakeholders, supuestos y decisiones.

---

## Después del discovery: el relevamiento continúa

En enfoques ágiles el discovery no termina: se transforma en **refinamiento continuo del backlog** y, en producto, en **discovery continuo** (entrevistas y experimentos semanales en paralelo al desarrollo, *dual-track*). Lo importante es mantener:

- Un **Product Owner** (o referente del cliente) con disponibilidad y poder de decisión.
- Un **proceso de gestión de cambios** acordado.
- El **glosario** y el **registro de decisiones** actualizados.

---

## Variantes según el tipo de proyecto

| Tipo de proyecto | Énfasis del discovery |
|------------------|----------------------|
| Startup / producto nuevo | Validar el problema y el mercado antes que el detalle: entrevistas con clientes potenciales, Lean Canvas, prototipos, experimentos. |
| Sistema interno de gestión | Procesos as-is/to-be, reglas de negocio, integraciones, migración de datos, gestión del cambio organizacional. |
| Reemplazo de sistema legado | Inventario funcional, uso real, datos, convivencia y migración, riesgos de corte. |
| E-commerce / app de consumo | UX, journeys, analítica, rendimiento, pagos, regulaciones de protección de datos. |
| Integración entre sistemas | APIs, contratos de datos, volúmenes, errores y reintentos, seguridad, SLA. |
| Sector público / licitación | Análisis del pliego, cumplimiento normativo, accesibilidad, documentación formal y trazabilidad. |
| Proyecto con IA / datos | Disponibilidad y calidad de datos, métricas de éxito del modelo, sesgos, explicabilidad, supervisión humana, normativa. |
