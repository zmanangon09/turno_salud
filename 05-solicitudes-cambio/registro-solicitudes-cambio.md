# Registro de solicitudes de cambio — GP.2 y GP.3

**Proyecto:** TurnoSalud · **Grupo 6**
**Responsable:** Zaith Manangón (GP) · **Apoyo:** Matías Lugmaña (LT)

---

## Cómo se gestiona una solicitud de cambio

```
Propuesta  →  Evaluada  →  Aceptada  →  Implementada y cerrada
                   └──────→  Rechazada
```

1. **Propuesta:** cualquiera puede pedir un cambio: el cliente, o el equipo cuando encuentra un problema (GP.3.3). Se llena una ficha con los datos de la sección «Producto de trabajo: la Solicitud de cambio» de la norma: propósito, estado, solicitante, sistemas afectados, impacto en la operación y en la documentación, criticidad y fecha requerida.
2. **Evaluada (GP.2.2):** el GP y el LT estiman horas por proceso y por persona, costo con las tarifas del plan, efecto en el calendario (que nadie pase de 40 h por semana) y en el presupuesto, e impacto técnico. Cuando conviene, se proponen opciones.
3. **Decisión:** si el cambio afecta lo acordado con el cliente (alcance, plazo, costo o entregables), se negocia con el CL y se registra en acta (GP.2.4). Si no lo afecta, lo deciden el GP y el LT en la reunión semanal del equipo (GP.2.3).
4. **Aceptada:** se actualizan los documentos afectados con una nueva versión y se paga con la reserva para contingencias si el riesgo estaba previsto.
5. **Cierre:** el cambio se cierra cuando sus casos de prueba pasan y el solicitante lo comprueba.

Una solicitud de cambio es trabajo nuevo, no retrabajo: sus horas se miden aparte de las correcciones por defectos ([Medición del retrabajo](../06-retrabajo-cierre/medicion-retrabajo.md)).

## Registro

| ID | Semana | Origen | Resumen | Criticidad | Horas | Costo (USD) | Pagado con | Estado | Ficha |
|----|--------|--------|---------|------------|-------|-------------|------------|--------|-------|
| SC-01 | S5 | CL | Lista de espera con aviso por correo cuando se libera un turno | Media | 54 | 647 | Reserva (R1) | **Aceptada** → implementada y cerrada en S11 | [SC-01](SC-01_lista-de-espera.md) |
| SC-02 | S5 | CL | Recordatorios por WhatsApp | Baja | ≈ 40 | ≈ 480 + costo recurrente | — | **Rechazada** (mejora futura) | [SC-02](SC-02_notificaciones-whatsapp.md) |

## Estado de la reserva para contingencias

| Movimiento | Semana | Importe (USD) | Saldo (USD) |
|------------|--------|---------------|-------------|
| Reserva inicial (Plan v1.0, 3.12) | S2 | | 2 270 |
| SC-01 aceptada | S5 | − 647 | 1 623 |

Los demás movimientos de la reserva se registran en el [Informe de cierre](../06-retrabajo-cierre/informe-cierre.md).
