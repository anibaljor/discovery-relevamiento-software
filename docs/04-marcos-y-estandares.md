# 4. Marcos de referencia y estándares

Los marcos y estándares no son plantillas para copiar: son **cuerpos de conocimiento** que definen vocabulario, actividades y buenas prácticas. Sirven para estudiar, certificarse y justificar el proceso ante un cliente.

---

## 4.1 ISO/IEC/IEEE 29148 — *Requirements engineering*

- **Versiones:** 2011, revisión 2018.
- **Reemplaza a:** IEEE 830-1998 (SRS), IEEE 1233 (requisitos de sistema) e IEEE 1362 (ConOps).
- **Qué define:**
  - Procesos de ingeniería de requisitos a lo largo del ciclo de vida.
  - Características de un buen requisito individual: **necesario, apropiado, no ambiguo, completo, singular, factible, verificable, correcto, conforme**.
  - Características de un conjunto de requisitos: completo, consistente, factible, comprensible, validable.
  - Contenido de documentos de información: **StRS** (Stakeholder Requirements Specification), **SyRS** (System Requirements Specification), **SRS** (Software Requirements Specification), **BRS** (Business Requirements Specification) y **ConOps** (Concept of Operations).
  - Construcciones de lenguaje recomendadas: "deberá" (*shall*) para requisitos obligatorios; evitar términos vagos ("amigable", "rápido", "etc.", "y/o", "como mínimo", "soportar").

## 4.2 IEEE 830-1998 — *Recommended Practice for SRS*

Formalmente reemplazado, pero sigue siendo la referencia más citada en universidades y pliegos de Hispanoamérica. Define las 8 cualidades de un buen SRS y la estructura de índice que se usó durante décadas (ver [esqueleto SRS](../plantillas/10-srs-esqueleto.md)).

## 4.3 BABOK® Guide (IIBA)

- **Qué es:** *Business Analysis Body of Knowledge*, del International Institute of Business Analysis. Versión 3 publicada en 2015.
- **Áreas de conocimiento:**
  1. Planificación y monitoreo del análisis de negocio.
  2. **Elicitación y colaboración**.
  3. Gestión del ciclo de vida de los requisitos.
  4. Análisis de estrategia.
  5. Análisis de requisitos y definición del diseño.
  6. Evaluación de la solución.
- **Modelo conceptual (BACCM):** Cambio, Necesidad, Solución, Stakeholder, Valor, Contexto.
- **50 técnicas** documentadas (entrevistas, talleres, observación, prototipado, BPMN, casos de uso, historias, MoSCoW, etc.).
- **Clasificación de requisitos:** de negocio, de stakeholders, de solución (funcionales y no funcionales) y de transición.
- **Certificaciones:** ECBA, CCBA, CBAP.

## 4.4 IREB CPRE

- **Qué es:** *International Requirements Engineering Board* (fundado en 2006). Certificación **Certified Professional for Requirements Engineering**.
- **Niveles:** Foundation Level → Advanced Level (Elicitación, Modelado, Gestión, Requisitos en ágil) → Expert.
- **Actividades centrales:** elicitar, documentar, validar y gestionar requisitos.
- **Aporte conceptual importante:** las **fuentes de requisitos** (stakeholders, documentos, sistemas) y el **modelo de Kano** aplicado a la elicitación (las técnicas de preguntar descubren mejor los requisitos de desempeño; los básicos y de deleite requieren observación y creatividad).

## 4.5 Volere (Robertson & Robertson)

- **Qué es:** proceso y plantilla de especificación de requisitos (primera versión mediados de los 90, actualizada periódicamente).
- **Estructura de la plantilla:** impulsores del proyecto (propósito, stakeholders), restricciones (obligatorias, convenciones, hechos y supuestos), requisitos funcionales (alcance del trabajo, del producto, requisitos funcionales y de datos), requisitos no funcionales (apariencia, usabilidad, rendimiento, operación, mantenibilidad, seguridad, cultural, legal), cuestiones del proyecto (temas abiertos, soluciones listas, nuevos problemas, tareas, migración, riesgos, costos, documentación de usuario, sala de espera, ideas de solución).
- **Aportes clave:** el *fit criterion* (todo requisito tiene un criterio medible) y la **"sala de espera"** para requisitos pospuestos.

## 4.6 ISO/IEC 25010 — Modelo de calidad del producto

- **Versiones:** 2011 (reemplaza a ISO 9126), actualizada en 2023.
- **Uso en discovery:** checklist para no olvidar requisitos no funcionales.
- **Características (versión 2011):** adecuación funcional, eficiencia de desempeño, compatibilidad, usabilidad, fiabilidad, seguridad, mantenibilidad, portabilidad.
- **Cambios en 2023:** "usabilidad" pasa a llamarse *interaction capability*, "portabilidad" pasa a *flexibility*, y se agrega **seguridad física/operacional (*safety*)**.
- Ver [checklist de no funcionales](../plantillas/11-checklist-requisitos-no-funcionales.md).

## 4.7 PMBOK® Guide (PMI)

- Las ediciones 5 y 6 incluyen el proceso **"Recopilar requisitos"** (*Collect Requirements*) dentro de la gestión del alcance, con salidas como la **documentación de requisitos** y la **matriz de trazabilidad**, y el **Project Charter** como punto de partida.
- La 7.ª edición (2021) pasa a un enfoque por principios y dominios de desempeño, menos prescriptivo.
- El PMI publicó además *Business Analysis for Practitioners: A Practice Guide* (2015) y la certificación **PMI-PBA**.

## 4.8 SWEBOK (IEEE Computer Society)

*Software Engineering Body of Knowledge*. Su área de conocimiento **Software Requirements** cubre: fundamentos, proceso, elicitación, análisis, especificación, validación y consideraciones prácticas. La versión 4 se publicó en 2024. Buena referencia académica y gratuita.

## 4.9 Marcos ágiles

- **Scrum Guide**: no prescribe técnicas de requisitos, pero define el **Product Backlog**, el rol del **Product Owner** y el refinamiento continuo.
- **SAFe**: estructura de Epics → Features → Stories, *Lean Business Case*, *PI Planning*.
- **DSDM / Agile Business Consortium**: MoSCoW, *Foundations phase* (equivalente a un discovery acotado).
- **Disciplined Agile (PMI)**: fase de *Inception* explícita.

## 4.10 Métodos de diseño y producto

- **Design Thinking** (IDEO / d.school) y **Double Diamond** (UK Design Council).
- **Lean Startup** (Build–Measure–Learn).
- **Jobs to be Done**.
- **Domain-Driven Design** (Eric Evans, 2003): lenguaje ubicuo y contextos delimitados; Event Storming como técnica de descubrimiento.

---

## ¿Cuál estudiar primero?

| Si sos... | Empezá por |
|-----------|-----------|
| Analista funcional / de negocio | BABOK + Wiegers (*Software Requirements*) |
| Ingeniero/a de requisitos, contexto formal o regulado | IREB CPRE Foundation + ISO/IEC/IEEE 29148 |
| Product Owner / Product Manager | Cagan (*Inspired*), Patton (*User Story Mapping*), Torres (*Continuous Discovery Habits*) |
| Líder de proyecto | PMBOK (área de alcance) + Inception Deck |
| Estudiante | SWEBOK (gratuito) + IEEE 830 como ejemplo histórico |
