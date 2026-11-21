# Matriz de trazabilidad de requisitos (RTM)

> Vincula cada requisito con su origen y con lo que lo implementa y verifica. En proyectos ágiles livianos puede bastar con enlazar historias a épicas y objetivos en la herramienta de gestión (Jira, Azure DevOps, etc.). En proyectos regulados suele ser obligatoria.

**Proyecto:** — **Versión:** — **Fecha:**

## Matriz principal

| ID Req. | Descripción breve | Tipo (F / NF / RN) | Objetivo de negocio | Origen (stakeholder / documento / reunión) | Prioridad | Caso de uso / historia | Diseño / componente | Caso(s) de prueba | Estado | Release |
|---------|------------------|------|-------|-------------|----|------|------|------|------|-----|
| RF-001 | Registrar pedido | F | OBJ-1 | Entrevista Ventas (M-03) | Must | CU-04 / HU-030 | Módulo Pedidos | CP-014, CP-015 | Aprobado | R1 |
| RNF-004 | Búsqueda < 2 s | NF | OBJ-1 | Taller Ventas (M-05) | Should | HU-033 | Índice de búsqueda | CP-PERF-02 | En desarrollo | R1 |
| RN-07 | Bloqueo por deuda > 90 días | RN | OBJ-3 | Política de Créditos v2 | Must | CU-04 ext. 2a | Servicio Cuentas | CP-021 | Propuesto | R1 |

**Estados sugeridos:** Propuesto → Aprobado → En desarrollo → Implementado → Verificado → Entregado | Diferido | Rechazado

## Trazabilidad hacia atrás y hacia adelante

```
Objetivo de negocio ──► Requisito de stakeholder ──► Requisito de sistema ──► Diseño ──► Código ──► Prueba
       ◄──────────────── hacia atrás (¿por qué existe?) ──────────────────
                         ──────────────── hacia adelante (¿cómo se cumple?) ──────────────────►
```

## Usos de la matriz

- **Análisis de impacto:** si cambia un requisito, ¿qué diseño, código y pruebas se ven afectados?
- **Cobertura:** ¿todos los requisitos tienen al menos una prueba? ¿Todos los objetivos tienen requisitos?
- **Detección de "gold plating":** requisitos sin objetivo de negocio asociado.
- **Auditoría y aceptación:** evidencia de que lo contratado se implementó y verificó.
