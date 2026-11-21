# Historia de usuario y criterios de aceptación

---

## Plantilla

**ID:** HU-XXX — **Épica:** EP-XX — **Prioridad:** — **Estimación:**

> **Como** [rol / persona]
> **quiero** [acción o funcionalidad]
> **para** [beneficio / valor de negocio]

**Contexto / notas de la conversación:**

**Reglas de negocio:**
- RN-XX:

**Criterios de aceptación** (formato lista o Gherkin):

```gherkin
Escenario: [nombre del escenario]
  Dado [contexto inicial]
  Y [más contexto]
  Cuando [acción del usuario]
  Entonces [resultado esperado]
  Y [otro resultado]
```

**Fuera del alcance de esta historia:**

**Dependencias:**

**Diseño / prototipo:** [enlace]

---

## Ejemplo

**ID:** HU-031 — **Épica:** EP-03 Gestión de pedidos — **Prioridad:** Must — **Estimación:** 5 pts

> **Como** vendedor
> **quiero** ver el stock disponible mientras cargo un pedido
> **para** no prometerle al cliente productos que no tenemos

**Reglas de negocio:**
- RN-11: el stock disponible = stock físico − stock reservado por pedidos confirmados.

**Criterios de aceptación**

```gherkin
Escenario: Producto con stock suficiente
  Dado que el producto "Tornillo M6" tiene 100 unidades disponibles
  Cuando el vendedor agrega 30 unidades al pedido
  Entonces el sistema muestra "Disponible: 100"
  Y permite confirmar la línea

Escenario: Producto con stock insuficiente
  Dado que el producto "Tornillo M6" tiene 10 unidades disponibles
  Cuando el vendedor agrega 30 unidades al pedido
  Entonces el sistema muestra una advertencia "Stock insuficiente: 10 disponibles"
  Y muestra la fecha estimada de reposición
  Y permite dejar las 20 unidades restantes como pendientes

Escenario: Stock actualizado en tiempo real
  Dado que dos vendedores cargan pedidos del mismo producto
  Cuando uno de ellos confirma su pedido
  Entonces el stock disponible que ve el otro vendedor se actualiza en menos de 5 segundos
```

**Fuera del alcance:** reservas de stock temporales mientras el pedido está en borrador (ver HU-045).

---

## Checklist INVEST

- [ ] **I**ndependiente: puede desarrollarse sin depender fuertemente de otra historia.
- [ ] **N**egociable: describe la necesidad, no un contrato cerrado de la solución.
- [ ] **V**aliosa: aporta valor a un usuario o al negocio.
- [ ] **E**stimable: el equipo entiende lo suficiente para estimarla.
- [ ] **S** (pequeña): entra en una iteración.
- [ ] **T**esteable: tiene criterios de aceptación verificables.

## Definition of Ready (ejemplo)

- [ ] Tiene formato rol / acción / beneficio.
- [ ] Criterios de aceptación acordados con el Product Owner.
- [ ] Dependencias identificadas.
- [ ] Diseño/prototipo disponible si tiene interfaz.
- [ ] Estimada por el equipo.

## Técnicas para dividir historias grandes

- Por **pasos del flujo** (workflow).
- Por **reglas de negocio** (primero el caso simple, después las variantes).
- **Camino feliz primero**, excepciones después.
- Por **tipo de dato o canal** (ej.: primero tarjeta de crédito, después transferencia).
- Por **operación** (crear / consultar / modificar / eliminar).
- Por **rendimiento** (primero que funcione, después que escale).
- **Spike**: historia de investigación con tiempo fijo cuando hay mucha incertidumbre.
