# Especificación de caso de uso

> Formato basado en Alistair Cockburn, *Writing Effective Use Cases* (2000), versión "completamente vestida". Para casos simples alcanza con el formato breve (nombre + escenario principal en un párrafo).

---

## Plantilla

| Campo | Contenido |
|-------|----------|
| **ID y nombre** | CU-XX — *Verbo + objeto* (ej.: "Registrar pedido") |
| **Actor principal** | Quien inicia el caso para lograr su objetivo |
| **Actores secundarios** | Otros actores o sistemas que participan |
| **Alcance** | Sistema que se está especificando |
| **Nivel** | Objetivo de usuario (☁️ resumen · 🌊 usuario · 🐟 subfunción) |
| **Stakeholders e intereses** | Quién más se ve afectado y qué le importa |
| **Precondiciones** | Lo que debe ser cierto antes de comenzar |
| **Garantías mínimas** | Lo que se asegura aunque el caso falle |
| **Garantías de éxito (postcondiciones)** | Lo que es cierto si el caso termina bien |
| **Disparador** | Evento que inicia el caso |
| **Prioridad / frecuencia** | |
| **Reglas de negocio relacionadas** | RN-XX |
| **Requisitos especiales** | No funcionales específicos de este caso |
| **Preguntas abiertas** | |

**Escenario principal de éxito**
1. El actor ...
2. El sistema ...
3. ...

**Extensiones (flujos alternativos y de excepción)**
- *2a.* Si [condición]:
  - 2a1. El sistema ...
  - 2a2. Vuelve al paso 3 / el caso termina.
- *\*a.* En cualquier momento, si [condición]: ...

---

## Ejemplo

| Campo | Contenido |
|-------|----------|
| **ID y nombre** | CU-04 — Registrar pedido de cliente |
| **Actor principal** | Vendedor |
| **Actores secundarios** | Sistema de stock, Sistema de facturación |
| **Alcance** | Sistema de Gestión Comercial |
| **Nivel** | 🌊 Objetivo de usuario |
| **Stakeholders e intereses** | Cliente: recibir lo pedido en tiempo. Depósito: pedidos con stock real. Finanzas: no vender a clientes con deuda vencida. |
| **Precondiciones** | El vendedor inició sesión. |
| **Garantías mínimas** | No se reserva stock de un pedido no confirmado. Se registra el intento en el log. |
| **Garantías de éxito** | El pedido queda confirmado, el stock reservado y el cliente notificado. |
| **Disparador** | Un cliente solicita productos al vendedor. |
| **Reglas de negocio** | RN-07: un cliente con deuda vencida > 90 días no puede generar pedidos. |

**Escenario principal de éxito**
1. El vendedor busca al cliente por nombre o CUIT/ID fiscal.
2. El sistema muestra los datos del cliente y su estado de cuenta.
3. El vendedor agrega productos y cantidades.
4. El sistema consulta el stock disponible y muestra precio y subtotal.
5. El vendedor confirma el pedido.
6. El sistema reserva el stock, registra el pedido y envía la confirmación al cliente por email.

**Extensiones**
- *2a.* El cliente tiene deuda vencida mayor a 90 días (RN-07):
  - 2a1. El sistema informa el bloqueo y el monto adeudado.
  - 2a2. El caso termina.
- *2b.* El cliente no existe:
  - 2b1. El vendedor da de alta al cliente (CU-02) y continúa en el paso 3.
- *4a.* No hay stock suficiente de un producto:
  - 4a1. El sistema muestra el stock disponible y la fecha estimada de reposición.
  - 4a2. El vendedor ajusta la cantidad o deja el producto como pendiente.
- *6a.* Falla el envío de email:
  - 6a1. El sistema registra el pedido igual y marca la notificación para reintento.
