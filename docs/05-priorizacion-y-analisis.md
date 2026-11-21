# 5. Técnicas de priorización y análisis

Relevar genera más pedidos de los que se pueden construir. Estas técnicas ayudan a **decidir qué entra, en qué orden y por qué**, y a analizar quién influye en el proyecto.

---

## 5.1 Análisis de stakeholders

### Identificación
Preguntas útiles: ¿quién paga?, ¿quién usa?, ¿quién se ve afectado?, ¿quién aprueba?, ¿quién puede bloquear?, ¿quién mantiene el sistema?, ¿qué entes externos regulan? Incluir también a los **"stakeholders silenciosos"**: soporte, seguridad informática, legales, auditoría, operaciones.

### Matriz poder / interés (Mendelow)

```
           Interés bajo             Interés alto
Poder    ┌─────────────────────┬─────────────────────┐
alto     │ MANTENER SATISFECHO │ GESTIONAR DE CERCA  │
         ├─────────────────────┼─────────────────────┤
Poder    │ MONITOREAR          │ MANTENER INFORMADO  │
bajo     └─────────────────────┴─────────────────────┘
```

### RACI
Para cada decisión o entregable: **R**esponsable (hace), **A**probador (rinde cuentas, uno solo), **C**onsultado, **I**nformado.

### Onion diagram (diagrama de cebolla)
Círculos concéntricos: sistema → usuarios directos → organización → entorno externo.

Ver [plantilla de registro de stakeholders](../plantillas/03-registro-de-stakeholders.md).

---

## 5.2 MoSCoW

Origen: Dai Clegg (Oracle, 1994), adoptado por DSDM.

| Categoría | Significado | Regla orientativa (DSDM) |
|-----------|------------|------------------------|
| **M**ust have | Sin esto la solución no sirve o no es legal | ≤ 60 % del esfuerzo |
| **S**hould have | Importante, pero hay alternativa temporal | ~20 % |
| **C**ould have | Deseable si hay tiempo | ~20 % (es la contingencia) |
| **W**on't have (this time) | Acordado explícitamente que no entra ahora | — |

**Ventaja:** simple y entendible por el cliente. **Riesgo:** todo termina siendo "Must". Pregunta de control: *"¿Saldrías a producción sin esto?"*

## 5.3 Modelo Kano

Origen: Noriaki Kano (1984). Clasifica atributos según su impacto en la satisfacción:

| Tipo | Si está | Si no está | Ejemplo |
|------|---------|-----------|---------|
| **Básico / obligatorio** | No genera satisfacción (se da por sentado) | Gran insatisfacción | Poder recuperar la contraseña |
| **De desempeño / lineal** | Más es mejor | Insatisfacción proporcional | Velocidad, cantidad de integraciones |
| **De deleite / atractivo** | Sorprende y satisface | No se extraña | Autocompletar inteligente |
| Indiferente | — | — | Funciones que nadie valora |
| Inverso | Molesta | — | Notificaciones excesivas |

Se evalúa con un cuestionario de pares de preguntas (funcional/disfuncional): "¿Qué sentirías si el producto tuviera X?" / "¿…si no tuviera X?". Con el tiempo, los atributos de deleite se convierten en básicos.

## 5.4 Matriz valor / esfuerzo (2×2)

```
          Esfuerzo bajo        Esfuerzo alto
Valor   ┌──────────────────┬──────────────────┐
alto    │ QUICK WINS ✅    │ PROYECTOS GRANDES│
        ├──────────────────┼──────────────────┤
Valor   │ RELLENO          │ EVITAR ❌        │
bajo    └──────────────────┴──────────────────┘
```

Rápida y visual para talleres.

## 5.5 RICE

Origen: Intercom (~2016). Puntaje = (**R**each × **I**mpact × **C**onfidence) / **E**ffort.
- Reach: cuántas personas afecta en un período.
- Impact: escala (3 = masivo, 2 = alto, 1 = medio, 0,5 = bajo, 0,25 = mínimo).
- Confidence: % de certeza en las estimaciones.
- Effort: persona-meses.

## 5.6 WSJF (Weighted Shortest Job First)

Origen: Don Reinertsen; popularizado por SAFe. WSJF = **Costo de la demora** / **Duración (o tamaño)**. El costo de la demora suma valor de negocio + criticidad temporal + reducción de riesgo/habilitación de oportunidades.

## 5.7 Otras técnicas

- **Votación por puntos (dot voting)**: cada participante distribuye N puntos.
- **Compra de funcionalidades (Buy a Feature)**: los participantes reciben "dinero" ficticio para comprar funcionalidades con precio.
- **Comparación por pares**.
- **100 puntos (cumulative voting)**.
- **Escala de prioridad de Wiegers**: valor, penalidad, costo y riesgo ponderados.
- **Cost of Delay** (sin dividir por tamaño).

---

## 5.8 Análisis y validación de requisitos

Después de relevar, hay que **revisar la calidad** de lo obtenido:

### Checklist de calidad de un requisito
- ¿Es **necesario**? ¿Qué objetivo de negocio cubre? (si no hay respuesta, sospechar)
- ¿Es **no ambiguo**? ¿Dos personas lo entenderían igual?
- ¿Es **verificable**? ¿Cómo se probaría?
- ¿Es **factible** técnica y económicamente?
- ¿Es **singular** (una sola cosa por requisito)?
- ¿Describe el **qué**, no el **cómo** (salvo restricciones reales)?
- ¿Tiene **origen** identificado (quién lo pidió)?
- ¿Está **priorizado**?

### Palabras peligrosas (señales de ambigüedad)
"fácil", "amigable", "rápido", "flexible", "eficiente", "robusto", "intuitivo", "moderno", "etc.", "y/o", "normalmente", "como mínimo", "soportar", "máximo posible", "adecuado", "todos", "nunca", "siempre".

### Técnicas de validación
- **Revisiones / walkthroughs / inspecciones** con stakeholders.
- **Prototipos** y tests de usabilidad.
- **Casos de prueba tempranos** (si no se puede escribir la prueba, el requisito no está claro).
- **Ejemplos concretos** (*Specification by Example*).
- **Firma / aprobación** formal (en contextos contractuales).

---

## 5.9 Trazabilidad

Capacidad de seguir un requisito hacia atrás (¿de dónde vino?, ¿qué objetivo cubre?) y hacia adelante (¿qué diseño, código y pruebas lo implementan?). Ver [matriz de trazabilidad](../plantillas/12-matriz-de-trazabilidad.md).

---

## 5.10 Estimación al cierre del discovery

El discovery suele terminar con una estimación. Técnicas habituales:

- **Por analogía / juicio experto**.
- **Tres puntos (PERT)**: (Optimista + 4 × Más probable + Pesimista) / 6.
- **Wideband Delphi**: estimaciones anónimas en rondas hasta converger.
- **Planning Poker** con puntos de historia.
- **T-shirt sizing** (XS, S, M, L, XL) para épicas.
- **Puntos de función** (IFPUG, COSMIC): medición funcional estandarizada, usada en contratos públicos.
- **Casos de uso ponderados (Use Case Points)**, Gustav Karner, 1993.

> El **cono de incertidumbre** (Barry Boehm, popularizado por Steve McConnell) recuerda que al inicio de un proyecto la estimación puede variar de 0,25× a 4×. El discovery existe, en parte, para estrechar ese cono antes de comprometer un precio.
