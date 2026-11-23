# Solicitud de cambio SC-02 — Recordatorios por WhatsApp

**Proyecto:** TurnoSalud · **Grupo 6**
**Tareas de la norma:** GP.2.2 Analizar y evaluar la solicitud de cambio · GP.2.4 Revisar con el cliente y registrar el acuerdo
**Roles:** GP y LT (evaluación) · CL (decisión)
**Registro:** [Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md) · [Registro de solicitudes de cambio](registro-solicitudes-cambio.md)
**Estado actual:** **Rechazada** para la versión 1.0 (anotada como mejora futura)

---

## 1. Datos de la solicitud

| Campo | Valor |
|-------|-------|
| **Identificador** | SC-02 |
| **Origen** | Cliente |
| **Solicitante y contacto** | Docente de la asignatura (CL). Canal: reuniones quincenales y Zaith Manangón (GP) |
| **Fecha de solicitud** | Semana 5 del proyecto (2026-11-23) |
| **Propósito del cambio** | Mejora. Enviar el recordatorio de 24 h (RF-12) también por WhatsApp, porque varios pacientes no revisan el correo. |
| **Sistema afectado** | TurnoSalud: módulo de notificaciones. Requiere además un proveedor externo de la API comercial de WhatsApp. |
| **Impacto en la operación de sistemas existentes** | Ninguno en producción. Dentro del proyecto, agrega una integración externa nueva con su propia cuenta, plantillas aprobadas por el proveedor y manejo de errores de envío. |
| **Impacto en la documentación** | Enunciado (2.5 lo excluye expresamente), Especificación de requisitos, diseño, plan (costos recurrentes) y manual de usuario. |
| **Criticidad** | Baja: el correo ya cubre los recordatorios. |
| **Fecha requerida** | Con la entrega final E5 (semana 12). |

## 2. Historial de estados

| Estado | Semana | Quién | Qué pasó |
|--------|--------|-------|----------|
| **Propuesta** | S5 | CL | Presentada en la reunión quincenal, junto con SC-01. |
| **Evaluada** | S5 | Zaith (GP) y Matías (LT) | Estimación de horas, costo y riesgos (sección 3). |
| **Rechazada** | S5 | CL | Aceptó no incluirla en la v1.0 y dejarla como mejora para una versión futura. |

## 3. Evaluación (GP.2.2)

| Aspecto | Resultado |
|---------|-----------|
| **Alcance** | Está excluida en la sección 2.5 del Enunciado, y el CL confirmó esa exclusión en el [Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md). |
| **Esfuerzo** | ≈ 40 horas-persona: alta en el proveedor, aprobación de plantillas, integración, manejo de errores y pruebas *(supuesto)*. |
| **Costo del proyecto** | ≈ USD 480 (40 h × tarifa promedio de USD 12/h). Después de SC-01 la reserva quedaría en USD 1 143 para cubrir R2 a R6, cuyo aporte esperado suma USD 1 470. |
| **Costo para la clínica** | Cobro recurrente por cada mensaje y cuenta empresarial con el proveedor, que no está en el presupuesto *(supuesto; depende de la cotización)*. |
| **Calendario** | Con SC-01, Matías, Alexander y Andrea ya están en 40 h en varias semanas de S6 a S10; no hay capacidad sin mover hitos. |
| **Riesgos** | Depende de que el proveedor apruebe las plantillas a tiempo, algo que el equipo no controla. |

**Recomendación del GP y el LT:** no incluirla en la v1.0. Si la clínica la quiere, cotizar el proveedor y tratarla como un proyecto aparte después de la entrega.

## 4. Decisión (GP.2.4)

El CL aceptó la recomendación. La solicitud queda **rechazada** para esta versión y anotada en el [Informe de cierre](../06-retrabajo-cierre/informe-cierre.md) como mejora futura. No cambia ningún documento del proyecto.

**Aprobación:**

| Cliente (CL) | Gestor del proyecto (GP) |
|--------------|--------------------------|
| Firma: ________________ | Firma: ________________ |
| Docente de la asignatura | Zaith Manangón |
