# 6b. Informe de cierre del proyecto — GP

**Proyecto:** TurnoSalud · **Grupo 6**
**Responsable:** Zaith Manangón (GP) · **Apoyo:** Matías Lugmaña (LT), Alexander Villacres (AN/DIS) y Andrea Raura (RP)
**Tareas de la norma:** GP.4.1 Formalizar el cierre según las instrucciones de entrega y obtener el registro de aceptación firmado · GP.4.2 Actualizar el repositorio del proyecto
**Roles:** GP y CL
**Semana del proyecto:** S12 · **Registro:** [Acta 08](../actas/ACTA-08_2026-11-23_cierre-proyecto.md)
**Estado:** Proyecto **cerrado** y producto **aceptado** por el cliente

> **Datos simulados.** Las horas reales, los defectos y los resultados de S3 a S12 son supuestos del ejercicio, coherentes con el plan. Los productos de IS.3 a IS.6 (diseño, código, informe de pruebas y manuales) se describen pero no están en este repositorio.

---

## 6.9 Entregables según las instrucciones de entrega

| Entregable | Semana plan | Semana real | Cómo se entregó | Aprobó | Estado |
|------------|-------------|-------------|-----------------|--------|--------|
| E1. Plan del proyecto | 2 | 2 | [Plan v1.0](../03-plan-proyecto/plan-proyecto.md) en GitHub ([Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md)); v1.1 por SC-01 ([Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md)) | CL | Aceptado |
| E2. Especificación de requisitos | 3 | 3 | [Especificación v1.0](../04-requisitos/especificacion-requisitos.md) y acta de validación ([Acta 06](../actas/ACTA-06_2026-11-23_validacion-requisitos.md)); v1.1 por SC-01 en S6 | CL | Validado |
| E3. Arquitectura y diseño detallado | 5 | 5 | Repositorio GitHub; v1.1 por SC-01 en S7 | LT y GP | Verificado |
| E4. Versión beta e informe de pruebas | 10 | 10 | Staging e informe de pruebas en GitHub | RP, LT y CL | Aceptado |
| E5. Configuración de software y cierre | 12 | 12 | Versión `v1.0.0` en GitHub, sistema en producción y registro de aceptación (6.15) | CL | Aceptado |

Todos los entregables llegaron en la semana acordada y con 48 horas de anticipación a su revisión.

## 6.10 Criterios de aceptación (Enunciado 2.8)

| # | Criterio | Resultado | ¿Cumple? |
|---|----------|-----------|----------|
| 1 | 100 % de las funciones del alcance | 25 casos de prueba (CP-01 a CP-25, incluida la lista de espera) ejecutados y aprobados. Sin defectos críticos ni mayores abiertos; 2 menores abiertos (6.14). | Sí |
| 2 | Sin cruces de horario por médico ni consultorio | 50 usuarios simultáneos intentaron 200 veces reservar el mismo bloque: 0 cruces. | Sí |
| 3 | Reserva en ≤ 4 pasos y < 2 minutos | El CL reservó en el sistema en 4 pasos y 1 min 10 s. | Sí |
| 4 | Responsivo en Chrome, Edge, Firefox y Safari | 8 combinaciones (4 navegadores × escritorio y móvil) probadas; un defecto visual menor en Safari para iOS. | Sí |
| 5 | Disponibilidad y confirmación en < 3 s | Con 50 usuarios simultáneos: 1,8 s la disponibilidad y 2,1 s la confirmación (percentil 95). | Sí |
| 6 | Entrega completa de la configuración de software | Lista de verificación de IS.6 completa (6.13). | Sí |

## 6.11 Plazo, esfuerzo y costo

**Plazo:** 12 semanas, como estaba planificado. Único hito atrasado: el primer incremento en staging, de S7 a S8 (una semana, dentro del umbral del plan); no afectó a E4 ni a E5.

**Esfuerzo:** 1 254 h reales frente a 1 202 h del plan v1.1 (+4,3 %). Detalle en la [Medición del retrabajo](medicion-retrabajo.md).

**Costo del trabajo por rol (tarifas del plan, 3.10):**

| Rol | Horas plan v1.1 | Horas reales | Tarifa (USD/h) | Costo plan v1.1 (USD) | Costo real (USD) |
|-----|-----------------|--------------|----------------|-----------------------|------------------|
| GP | 181 | 184 | 15 | 2 715 | 2 760 |
| LT | 199 | 204 | 14 | 2 786 | 2 856 |
| AN/DIS | 331 | 340 | 12 | 3 972 | 4 080 |
| PR | 308 | 334 | 11 | 3 388 | 3 674 |
| RP | 183 | 192 | 11 | 2 013 | 2 112 |
| **Total** | **1 202** | **1 254** | | **14 874** | **15 482** |

Las horas de PR son las de construcción de Matías (188 h) y Andrea (146 h); el resto de sus horas se paga como LT (204 h) y RP (192 h).

**Presupuesto:**

| Concepto | Plan v1.1 (USD) | Real (USD) |
|----------|-----------------|------------|
| Trabajo del equipo | 14 874 | 15 482 |
| Servicios y herramientas | 547 | 547 |
| Reserva para contingencias | 1 623 | — |
| **Total** | **17 044** | **16 029** |
| Tope del cliente | 18 000 | 18 000 |
| **No gastado** | | **1 971** |

**Uso de la reserva para contingencias:**

| Movimiento | Semana | Importe (USD) | Saldo (USD) |
|------------|--------|---------------|-------------|
| Reserva inicial (Plan v1.0) | S2 | | 2 270 |
| SC-01, lista de espera (R1) | S5 | − 647 | 1 623 |
| Horas sobre el plan en IS.4, IS.5 y otros (R2 y R4; AC-01) | S12 | − 608 | 1 015 |

Se usaron USD 1 255 de los USD 2 270 de la reserva. Lo no gastado (USD 1 971 = margen de 956 + reserva sobrante de 1 015) queda como ahorro para la clínica.

## 6.12 Riesgos al cierre

| Riesgo | ¿Ocurrió? | Efecto y respuesta |
|--------|-----------|--------------------|
| R1 Cambios después de E2 | Sí | SC-01 aceptada (USD 647 de la reserva); SC-02 rechazada. |
| R2 Cruces por concurrencia | En parte | 2 defectos en pruebas, corregidos en 14 h antes de E4; 0 cruces en la prueba final. |
| R3 Ausencia de un integrante | No | — |
| R4 Construcción subestimada | En parte | IS.4 llegó a +11 % en S8; AC-01 la cerró en +5,6 %. |
| R5 Exposición de datos | No | Revisión de seguridad en cada pull request; sin hallazgos críticos. |
| R6 Aumento de costos en la nube | No | Servicios en lo presupuestado (USD 547). |
| R7 CL no disponible | No | Todas las revisiones se hicieron en la semana acordada. |
| R8 Poca experiencia con NestJS o la norma | Mitigado | Taller y nivelación en S1 a S4 (38 h de prevención en total). |
| R9 Correos en spam | Sí, en staging | 1 defecto: SPF mal configurado; corregido en IS.5 antes de producción. |

## 6.13 Configuración de software entregada (IS.6)

- [x] Código fuente del frontend y del backend, versión `v1.0.0`
- [x] Scripts de creación y migración de la base de datos
- [x] Sistema desplegado en el servidor de producción
- [x] Especificación de requisitos v1.1
- [x] Arquitectura y diseño detallado v1.1
- [x] Casos de prueba e informe de pruebas
- [x] Manual de usuario (paciente, recepción, médico y administrador), con la lista de espera
- [x] Guía de mantenimiento, con los 2 defectos menores abiertos y cómo corregirlos
- [x] Guía de instalación y respaldo
- [x] Credenciales de administrador entregadas en persona al CL, fuera del repositorio
- [x] Capacitación de 2 horas al personal de recepción y administración
- [x] Traspaso del alojamiento: la clínica contrata el servidor a su nombre después del primer mes

## 6.14 Defectos abiertos al cierre

| ID | Gravedad | Descripción | Decisión del CL |
|----|----------|-------------|-----------------|
| D-72 | Menor | En Safari para iOS, la tabla del reporte (P-09) se corta a la derecha; se ve completa al girar el teléfono. | Aceptado; corregir en mantenimiento. |
| D-73 | Menor | En pantallas de 360 px, el mensaje de contraseña inválida ocupa tres líneas en P-01. | Aceptado; corregir en mantenimiento. |

Sin defectos críticos ni mayores abiertos.

## 6.15 Registro de aceptación (GP.4.1)

El cliente comprobó los seis criterios de aceptación (6.10), recibió la configuración de software (6.13) según las instrucciones de entrega del Enunciado (2.6) y **acepta el producto TurnoSalud, versión 1.0.0**. Con esta firma el proyecto queda cerrado.

| Cliente (CL) | Gestor del proyecto (GP) |
|--------------|--------------------------|
| Firma: ________________ | Firma: ________________ |
| Nombre: Docente de la asignatura | Nombre: Zaith Manangón |
| Fecha: 2026-11-23 (semana 12) | Fecha: 2026-11-23 (semana 12) |

## 6.16 Lecciones aprendidas

| Qué funcionó | Qué mejorar |
|--------------|-------------|
| Validar prototipos con el CL antes de diseñar: 4 problemas corregidos a 2,5 h cada uno. | Las reglas de «no cruce» deben llegar completas del requisito al diseño (lo del consultorio costó 14 h en pruebas). |
| Tener un proceso para solicitudes de cambio: SC-01 se aprobó con números y SC-02 se rechazó sin conflicto. | Aceptar cambios solo si nadie queda por encima de 36 h por semana; con SC-01 se perdió la holgura y apareció AC-01. |
| La reserva para contingencias por riesgo cubrió el cambio y el sobrecosto sin pasar el tope. | Fijar en el plan una meta de retrabajo (12 % o menos) y medirla desde S1. |
| Registrar horas por categoría permitió medir el retrabajo (14,5 %). | Escribir las pruebas de concurrencia antes de construir el agendamiento. |

**Mejora futura anotada:** recordatorios por WhatsApp ([SC-02](../05-solicitudes-cambio/SC-02_notificaciones-whatsapp.md)), como proyecto aparte con cotización del proveedor.

## 6.17 Actualización del repositorio (GP.4.2)

- Todos los productos de trabajo y las actas 01 a 08 están en `main`, enlazados desde el [README](../README.md).
- Etiquetas: `E1-v1.0`, `E2-v1.0`, `E2-v1.1`, `E3-v1.0`, `E3-v1.1`, `E4-v1.0` y `v1.0.0` (E5).
- Respaldo final: copia comprimida del repositorio y de la base de datos de producción en el almacenamiento de respaldos (Plan 3.15).
- Acceso: el CL mantiene lectura; los permisos de escritura del equipo se retiran 30 días después del cierre, al terminar la garantía.
