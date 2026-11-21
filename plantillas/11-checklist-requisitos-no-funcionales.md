# Checklist de requisitos no funcionales

> Basado en las características de calidad de ISO/IEC 25010 (2011, con los ajustes de 2023) y en preguntas prácticas de relevamiento. Para cada ítem: ¿aplica?, ¿cuál es el valor medible?, ¿quién lo definió?

## 1. Eficiencia de desempeño (rendimiento)
- [ ] ¿Cuántos usuarios en total? ¿Cuántos concurrentes en el pico?
- [ ] ¿Qué volumen de transacciones por hora/día/mes? ¿Hay picos estacionales?
- [ ] ¿Qué tiempo de respuesta es aceptable para las operaciones críticas?
- [ ] ¿Qué volumen de datos se espera hoy y en 3–5 años?
> Ej.: "El 95 % de las búsquedas de productos deberá responder en menos de 2 segundos con 300 usuarios concurrentes."

## 2. Fiabilidad / disponibilidad
- [ ] ¿En qué horarios debe estar disponible? ¿24×7?
- [ ] ¿Cuánto tiempo de caída es tolerable? (SLA, ej. 99,5 %)
- [ ] ¿Qué pasa si se cae? ¿Hay operación de contingencia manual?
- [ ] ¿Cuánta pérdida de datos es tolerable? (RPO) ¿En cuánto tiempo hay que recuperarse? (RTO)
- [ ] Frecuencia y retención de backups.
> Ej.: "Disponibilidad mensual ≥ 99,5 % en horario hábil; RPO ≤ 1 h; RTO ≤ 4 h."

## 3. Seguridad (de la información)
- [ ] ¿Cómo se autentican los usuarios? (usuario/contraseña, SSO, 2FA)
- [ ] ¿Qué roles y permisos existen?
- [ ] ¿Se manejan datos personales o sensibles? ¿Qué normativa aplica? (leyes de protección de datos personales, GDPR, PCI-DSS para tarjetas, HIPAA en salud, etc.)
- [ ] ¿Qué debe auditarse (log de quién hizo qué y cuándo)? ¿Por cuánto tiempo?
- [ ] ¿Requisitos de cifrado en tránsito y en reposo?
- [ ] ¿Políticas de seguridad del cliente a respetar? ¿Pruebas de penetración?
> Ej.: "Toda modificación de precios deberá registrarse con usuario, fecha, valor anterior y nuevo, conservándose 5 años."

## 4. Usabilidad / capacidad de interacción
- [ ] ¿Perfil de los usuarios (edad, experiencia, contexto de uso)?
- [ ] ¿Cuánto tiempo de capacitación es aceptable?
- [ ] ¿Idiomas? ¿Formatos regionales (moneda, fecha)?
- [ ] ¿Requisitos de **accesibilidad**? (WCAG 2.1/2.2 nivel AA es lo habitual; obligatorio en muchos organismos públicos)
- [ ] ¿Guía de estilo o identidad visual a respetar?
> Ej.: "Un vendedor nuevo deberá poder registrar un pedido sin ayuda tras 30 minutos de capacitación."

## 5. Compatibilidad
- [ ] ¿Navegadores y versiones? ¿Dispositivos móviles? ¿Sistemas operativos?
- [ ] ¿Con qué sistemas debe integrarse? ¿Mediante qué protocolo y formato?
- [ ] ¿Debe convivir con otros sistemas en la misma infraestructura?

## 6. Mantenibilidad
- [ ] ¿Quién mantendrá el sistema? ¿Equipo interno del cliente?
- [ ] ¿Estándares de código, documentación o tecnologías obligatorias?
- [ ] ¿Qué parámetros debe poder cambiar el negocio sin programar?
- [ ] ¿Requisitos de cobertura de pruebas automatizadas?

## 7. Portabilidad / flexibilidad
- [ ] ¿Nube (qué proveedor), on-premise o híbrido?
- [ ] ¿Debe poder migrarse de proveedor de nube?
- [ ] ¿Escalabilidad esperada (más usuarios, países, unidades de negocio)?

## 8. Seguridad operacional (*safety*, ISO 25010:2023)
- [ ] ¿Un fallo del sistema puede causar daño a personas, bienes o al ambiente?
- [ ] ¿Se requieren modos de fallo seguro?

## 9. Adecuación funcional
- [ ] ¿Precisión requerida en cálculos? (decimales, redondeo, monedas)
- [ ] ¿Qué funciones son críticas y deben ser exactas siempre?

## 10. Otros aspectos frecuentes
- [ ] **Legales / normativos**: facturación electrónica, firma digital, retención documental, normativas sectoriales.
- [ ] **Operación**: monitoreo, alertas, logs, ventanas de mantenimiento.
- [ ] **Migración de datos**: origen, volumen, calidad, limpieza, validación.
- [ ] **Despliegue**: ambientes (desarrollo, QA, producción), frecuencia de releases.
- [ ] **Soporte**: horarios, niveles, tiempos de respuesta.
- [ ] **Licenciamiento**: restricciones sobre software de terceros o de código abierto.
- [ ] **Costos de operación**: presupuesto de infraestructura mensual.
- [ ] **IA** (si aplica): explicabilidad, sesgos, supervisión humana, uso de datos para entrenamiento.

---

## Plantilla para registrar cada requisito no funcional

| ID | Característica | Requisito | Métrica / criterio de ajuste | Origen | Prioridad | Cómo se verifica |
|----|---------------|-----------|----------------------------|--------|-----------|-----------------|
| RNF-001 | Rendimiento | | | | | Prueba de carga |
