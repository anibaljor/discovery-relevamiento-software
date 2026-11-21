# Especificación de Requisitos de Software (SRS) — Esqueleto

> Estructura basada en ISO/IEC/IEEE 29148:2018 (sección de contenido del SRS) y en la tradicional IEEE 830-1998. Adaptar: no todas las secciones aplican a todos los proyectos. Usar cuando el contexto exige especificación formal (precio fijo, licitación, industria regulada).

**Sistema:**
**Versión del documento:** — **Fecha:** — **Estado:**

| Versión | Fecha | Autor | Descripción del cambio |
|---------|-------|-------|----------------------|

---

## 1. Introducción
### 1.1 Propósito
Propósito del documento y audiencia.
### 1.2 Alcance
Nombre del producto, qué hará y qué no, beneficios, objetivos.
### 1.3 Visión general del producto
#### 1.3.1 Perspectiva del producto (relación con otros sistemas; diagrama de contexto)
#### 1.3.2 Funciones del producto (resumen)
#### 1.3.3 Características de los usuarios
#### 1.3.4 Limitaciones / restricciones
### 1.4 Definiciones, acrónimos y abreviaturas
### 1.5 Referencias
Documentos relacionados (visión y alcance, normativas, contratos, estándares).

## 2. Referencias normativas
Normas y regulaciones aplicables.

## 3. Requisitos específicos
> Cada requisito con: ID único, descripción ("El sistema deberá..."), justificación, origen, prioridad, criterio de verificación.

### 3.1 Interfaces externas
#### 3.1.1 Interfaces de usuario
#### 3.1.2 Interfaces de hardware
#### 3.1.3 Interfaces de software (integraciones, APIs)
#### 3.1.4 Interfaces de comunicación
### 3.2 Funciones (requisitos funcionales)
Organizados por: modo de operación, clase de usuario, objeto, característica, estímulo o caso de uso.

| ID | Requisito | Justificación | Origen | Prioridad | Verificación |
|----|-----------|--------------|--------|-----------|-------------|
| RF-001 | El sistema deberá permitir al vendedor registrar un pedido con uno o más productos. | Objetivo OBJ-1 | Entrevista Ventas 12/03 | Alta | Prueba funcional CP-014 |

### 3.3 Requisitos de usabilidad
### 3.4 Requisitos de rendimiento
### 3.5 Requisitos lógicos de base de datos (entidades, relaciones, retención, volúmenes)
### 3.6 Restricciones de diseño
### 3.7 Cumplimiento de estándares
### 3.8 Atributos del sistema de software
- Fiabilidad / disponibilidad
- Seguridad (de la información)
- Mantenibilidad
- Portabilidad
### 3.9 Información de soporte

## 4. Verificación
Cómo se verificará cada requisito o grupo (inspección, análisis, demostración, prueba).

## 5. Anexos
### 5.1 Supuestos y dependencias
### 5.2 Siglas
### 5.3 Modelos (casos de uso, modelo de datos, diagramas de estado, BPMN)
### 5.4 Matriz de trazabilidad
### 5.5 Preguntas abiertas

---

## Estructura tradicional IEEE 830-1998 (referencia histórica)

```
1. Introducción
   1.1 Propósito
   1.2 Alcance
   1.3 Definiciones, acrónimos y abreviaturas
   1.4 Referencias
   1.5 Visión general del documento
2. Descripción general
   2.1 Perspectiva del producto
   2.2 Funciones del producto
   2.3 Características de los usuarios
   2.4 Restricciones
   2.5 Supuestos y dependencias
3. Requisitos específicos
   3.1 Interfaces externas
   3.2 Funciones
   3.3 Requisitos de rendimiento
   3.4 Requisitos lógicos de base de datos
   3.5 Restricciones de diseño
   3.6 Atributos del sistema
   3.7 Otros requisitos
Apéndices
Índice
```

## Cómo redactar un requisito

- ✅ "El sistema **deberá** generar la factura electrónica en menos de 3 segundos desde la confirmación del pedido."
- ❌ "El sistema debería facturar rápido."

Patrón sugerido (inspirado en EARS, *Easy Approach to Requirements Syntax*, Mavin et al., 2009):
- **Ubicuo:** El `<sistema>` deberá `<respuesta>`.
- **Por evento:** **Cuando** `<disparador>`, el `<sistema>` deberá `<respuesta>`.
- **Por estado:** **Mientras** `<estado>`, el `<sistema>` deberá `<respuesta>`.
- **No deseado:** **Si** `<condición no deseada>`, **entonces** el `<sistema>` deberá `<respuesta>`.
- **Opcional:** **Donde** `<característica incluida>`, el `<sistema>` deberá `<respuesta>`.
