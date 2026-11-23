# Validación de la Especificación de requisitos — IS.2.4

**Proyecto:** TurnoSalud · **Grupo 6**
**Documento validado:** [Especificación de requisitos](especificacion-requisitos.md), versión 0.2 [verificada] → versión 1.0 [validada]
**Semana del proyecto:** S3 · **Fecha:** 2026-11-23 · **Registro:** [Acta 06](../actas/ACTA-06_2026-11-23_validacion-requisitos.md)
**Tarea de la norma:** IS.2.4 Validar y obtener la aprobación de la Especificación de requisitos (incluye la usabilidad de la interfaz); se corrige hasta que el cliente la aprueba. **Roles:** CL y AN
**Resultado:** Especificación **validada** y aprobada por el CL (hito E2 cumplido en S3)

---

## Cómo se validó

1. Alexander (AN) explicó al CL los requisitos funcionales agrupados por usuario (4.3 y 4.4) y las reglas de negocio (4.5).
2. El CL recorrió los prototipos P-01 a P-09 haciendo de paciente y de recepcionista.
3. **Prueba de usabilidad (RNF-01):** el CL reservó un turno de Medicina General en el prototipo, sin ayuda. Andrea (RP) contó los pasos y midió el tiempo.
4. El CL dio sus observaciones, que se anotaron y clasificaron: corrección dentro del alcance o función nueva.
5. Las correcciones se aplicaron y el CL revisó la versión corregida (ronda 2).

## Prueba de usabilidad del flujo de reserva

| Ronda | Pasos | Tiempo | Resultado frente a RNF-01 (≤ 4 pasos y < 2 min) | Comentario del CL |
|-------|-------|--------|--------------------------------------------------|-------------------|
| 1 (versión 0.2) | 4 | 1 min 35 s | Cumple | Le obligó a elegir un médico aunque no tenía preferencia (observación V-03). |
| 2 (versión 1.0) | 4 | 1 min 20 s | Cumple | Con «cualquier médico disponible» encontró horario más rápido. |

## Observaciones del cliente

| # | Requisito | Observación del CL | Tipo | Corrección | ¿Corregido? |
|---|-----------|--------------------|------|------------|-------------|
| V-01 | RF-13 | Muchos pacientes mayores no tienen correo; recepción no podría registrarlos. | Corrección dentro del alcance | El correo es opcional cuando registra recepción; se agregó RN-06. | Sí |
| V-02 | RF-10, RF-11 | La clínica necesita al menos 4 horas para llenar un turno cancelado; el borrador no tenía plazo. | Corrección dentro del alcance | Se agregó RN-03: el paciente reprograma o cancela hasta 4 h antes; después, solo recepción. | Sí |
| V-03 | RF-07 | En el paso 2 el paciente debe elegir médico aunque le dé igual cuál. | Corrección de usabilidad | Opción «cualquier médico disponible» en RF-07 y en el prototipo P-02. | Sí |
| V-04 | RF-17 | El administrador necesita ver el reporte por médico, no solo por especialidad. | Corrección dentro del alcance | Se agregó el filtro por médico a RF-17 y a P-09. | Sí |
| V-05 | — | Cuando no hay horarios, al paciente le gustaría anotarse en una lista de espera y recibir un aviso si alguien cancela. | **Función nueva, fuera del alcance validado** | No se incluye en la versión 1.0. Se explicó al CL que, según el plan (3.14, R1), debe presentarse como solicitud de cambio para evaluar su costo y plazo. El CL dijo que la presentará en la siguiente reunión quincenal. | No aplica (ver [SC-01](../05-solicitudes-cambio/SC-01_lista-de-espera.md)) |

**Esfuerzo de corrección:** 10 horas-persona (Alexander 8 h en especificación y prototipos, Zaith 2 h en la ronda 2), registradas como retrabajo de IS.2.

## Ronda 2 y aprobación

Alexander aplicó V-01 a V-04 y subió la versión 1.0 al repositorio. En la ronda 2 el CL revisó solo los cambios, repitió la prueba de usabilidad y no tuvo observaciones nuevas. Con eso **aprueba la Especificación de requisitos, versión 1.0**, como línea base de requisitos.

Desde este momento, cualquier función nueva o cambio en un requisito validado se gestiona con una solicitud de cambio (GP.2.2), como pidió el mismo CL en el [Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md).

## Productos de trabajo

- **Resultados de validación** (este documento).
- **Especificación de requisitos [validada]**, versión 1.0, con la etiqueta `E2-v1.0` en el repositorio (IS.2.7).
- **Registro de reunión:** [Acta 06](../actas/ACTA-06_2026-11-23_validacion-requisitos.md).

**Aprobación:**

| Cliente (CL) | Analista (AN) |
|--------------|---------------|
| Firma: ________________ | Firma: ________________ |
| Nombre: Docente de la asignatura | Nombre: Alexander Villacres |
