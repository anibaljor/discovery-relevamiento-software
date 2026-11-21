# 7. Errores comunes y buenas prácticas

Los problemas de requisitos aparecen una y otra vez en los estudios sobre fracaso de proyectos de software. Algunas cifras clásicas se discuten metodológicamente (por ejemplo, los informes CHAOS de Standish Group), pero hay amplio consenso en que **los defectos de requisitos son de los más caros de corregir** cuanto más tarde se detectan (Boehm, *Software Engineering Economics*, 1981).

---

## Antipatrones frecuentes

| # | Antipatrón | Cómo se ve | Qué hacer |
|---|-----------|-----------|-----------|
| 1 | **Saltar a la solución** | "Necesitamos una app" antes de entender el problema | Preguntar "¿para qué?" y "¿qué problema resuelve?"; separar necesidad de solución propuesta |
| 2 | **Hablar solo con el patrocinador** | Quien paga describe cómo trabaja otra gente | Entrevistar y observar a los usuarios reales |
| 3 | **Requisitos como lista de deseos** | Todo es prioridad alta | Priorizar con MoSCoW y preguntar "¿saldrías a producción sin esto?" |
| 4 | **Ambigüedad** | "El sistema debe ser rápido y fácil de usar" | Requisitos medibles, ejemplos concretos, criterios de aceptación |
| 5 | **Olvidar lo no funcional** | Se descubre la carga real o la normativa en producción | Usar un checklist (ISO 25010) desde el discovery |
| 6 | **Alcance sin límites** | No hay "fuera de alcance" escrito | Documentar explícitamente lo que NO se hace |
| 7 | ***Scope creep*** | "Ya que estamos, agreguemos..." | Proceso de gestión de cambios acordado de antemano |
| 8 | **Replicar el sistema viejo** | Migrar todo, incluso lo que nadie usa | Pedir métricas de uso; repensar el proceso |
| 9 | **Documento que nadie lee** | SRS de 200 páginas firmado sin leer | Documentos cortos, visuales, revisados en reuniones; prototipos |
| 10 | **Supuestos implícitos** | "Pensé que la integración la hacían ustedes" | Registro de supuestos y responsabilidades (RACI) |
| 11 | **Vocabulario distinto** | "Cliente" significa cosas diferentes para Ventas y para Facturación | Glosario desde el día uno |
| 12 | **Olvidar stakeholders** | Seguridad informática o Legales bloquean al final | Mapa de stakeholders con preguntas de "quién puede bloquear" |
| 13 | **Ignorar los datos** | Se descubre tarde que los datos a migrar están sucios | Revisar calidad y volumen de datos en el discovery |
| 14 | **Prototipo confundido con producto** | "Si ya está la pantalla, ¿por qué tarda 3 meses?" | Explicar qué es un prototipo; usar baja fidelidad al inicio |
| 15 | **Discovery gratis e interminable** | Meses de reuniones sin compromiso | Discovery con duración, entregables y precio definidos |
| 16 | **Preguntas que inducen la respuesta** | "¿No le parece que sería útil un dashboard?" | Preguntas abiertas sobre hechos pasados |
| 17 | **No validar lo entendido** | El cliente ve el resultado recién en la entrega | Minutas, resúmenes, prototipos y demos frecuentes |
| 18 | **Ignorar la gestión del cambio** | El sistema funciona pero nadie lo adopta | Relevar capacitación, comunicación y resistencia al cambio |

---

## Buenas prácticas resumidas

1. **Problema antes que solución.** Entender objetivos de negocio y métricas de éxito antes de hablar de pantallas.
2. **Hablar con usuarios reales**, no solo con intermediarios.
3. **Observar**, no solo preguntar: la gente no sabe describir todo lo que hace.
4. **Mostrar temprano**: bocetos, prototipos, ejemplos.
5. **Escribir lo que NO se hace.**
6. **Hacer visibles los supuestos y las preguntas abiertas.**
7. **Requisitos medibles y verificables.**
8. **Un glosario compartido.**
9. **Validar por escrito lo entendido** (minutas en 24–48 h).
10. **Priorizar con el cliente**, no por el cliente.
11. **Ajustar la formalidad al contexto** (contrato, regulación, riesgo).
12. **Acordar cómo se gestionan los cambios** antes de que aparezcan.

---

## Habilidades blandas del buen relevador

- **Escucha activa**: parafrasear ("si entendí bien, ustedes...").
- **Curiosidad y humildad**: el cliente es el experto en su negocio.
- **Neutralidad**: no tomar partido entre áreas en conflicto.
- **Facilitación**: manejar talleres, dar voz a todos, controlar el tiempo.
- **Pensamiento crítico**: detectar contradicciones y huecos.
- **Comunicación escrita clara**.
- **Negociación**: ayudar a decidir entre alternativas con costos visibles.
- **Empatía**: entender el miedo al cambio, la presión política y las urgencias de cada persona.
