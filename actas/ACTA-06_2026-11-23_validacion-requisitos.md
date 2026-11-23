# VSE de Sangolquí — Proyecto TurnoSalud

ESPE · Aseguramiento de la Calidad de Software · **Grupo 6** · Caso «TurnoSalud» (ISO/IEC 29110, Perfil Básico)

## ACTA DE REUNIÓN No. 06

| Campo                  | Valor                                                    | Campo            | Valor                                             |
|------------------------|----------------------------------------------------------|------------------|---------------------------------------------------|
| **Tipo de reunión**    | [x] Ordinaria  [ ] Extraordinaria                        | **Fecha**        | 2026-11-23 (semana 3 del proyecto)                |
| **Hora inicio**        | 10:00                                                    | **Hora cierre**  | 11:00                                             |
| **Órgano reunido**     | Equipo de trabajo (ET) de la VSE y Cliente (CL)          | **Modalidad**    | [x] Presencial  [ ] Virtual  [ ] Mixta            |
| **Lugar / Plataforma** | ESPE, campus Sangolquí (aula de clase)                   |                  |                                                   |

---

## Asistentes y quórum

- **Quórum requerido presente:** [x] Sí  [ ] No
- **Miembros presentes:** 4 de 4 del equipo, más el cliente

### Asistentes

| Nombre    | Cargo (rol ISO/IEC 29110)                       |
|-----------|-------------------------------------------------|
| Zaith Manangón | Gestor del proyecto (GP)                       |
| Matías Lugmaña | Líder técnico (LT) y Programador (PR)           |
| Alexander Villacres | Analista (AN) y Diseñador (DIS)                 |
| Andrea Raura | Responsable de pruebas (RP) y Programadora (PR). Secretaria |
| Docente de la asignatura | Cliente (CL), en representación de la clínica |

**Ausentes:** Ninguno

---

## Orden del día

1. Lectura y aprobación del Acta 05.
2. Presentación de la Especificación de requisitos verificada.
3. Recorrido de prototipos y prueba de usabilidad.
4. Observaciones del cliente.
5. Aprobación de la especificación (IS.2.4).

---

## Desarrollo de la reunión

### Punto 1: Lectura y aprobación del Acta 05

Resumen de lo discutido: se leyó el Acta 05, que registra la verificación interna de la especificación. Sin observaciones.

### Punto 2: Presentación de la especificación

Resumen de lo discutido: Alexander (AN) presentó los requisitos por usuario, las reglas de negocio y los requisitos no funcionales, y mostró cómo cada criterio de aceptación del Enunciado (2.8) está enlazado a requisitos y casos de prueba (sección 4.8).

### Punto 3: Recorrido de prototipos y prueba de usabilidad

Resumen de lo discutido: el CL recorrió los prototipos P-01 a P-09 como paciente y como recepcionista. En la prueba de usabilidad reservó un turno en 4 pasos y 1 min 35 s, dentro de lo exigido (RNF-01).

### Punto 4: Observaciones del cliente

Resumen de lo discutido: el CL hizo cinco observaciones:

| # | Observación | Clasificación |
|---|-------------|---------------|
| V-01 | Pacientes sin correo registrados por recepción | Corrección dentro del alcance |
| V-02 | Plazo para que el paciente cancele o reprograme: 4 h antes | Corrección dentro del alcance |
| V-03 | Opción «cualquier médico disponible» al buscar | Corrección de usabilidad |
| V-04 | Filtro por médico en el reporte | Corrección dentro del alcance |
| V-05 | Lista de espera con aviso cuando alguien cancela | Función nueva, fuera del alcance |

Zaith (GP) explicó que V-05 no entra a la línea base de requisitos: según el plan (3.14, riesgo R1) debe presentarse como solicitud de cambio, para evaluar sus horas, costo y efecto en el calendario antes de decidir. El CL estuvo de acuerdo.

### Punto 5: Aprobación de la especificación

Resumen de lo discutido: el CL aprobó la especificación con la condición de revisar las correcciones V-01 a V-04 en una segunda ronda. Alexander aplicó los cambios y en la ronda 2 el CL repitió la prueba de usabilidad (4 pasos, 1 min 20 s) y no tuvo observaciones nuevas. La especificación queda **validada** en su versión 1.0. Detalle en [Resultados de validación](../04-requisitos/resultados-validacion-requisitos.md).

---

## Decisiones y votaciones

| # | Decisión                                                                                   | Votación                                   |
|---|--------------------------------------------------------------------------------------------|--------------------------------------------|
| 1 | Aprobar el Acta 05 sin observaciones                                                       | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 2 | Incorporar V-01 a V-04 a la especificación                                                 | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 3 | No incorporar V-05; el CL la presentará como solicitud de cambio                           | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 4 | **Aprobar** la Especificación de requisitos, versión 1.0, como línea base (IS.2.4, hito E2) | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |

---

## Compromisos y tareas

| Compromiso / Tarea                                                         | Responsable   | Fecha límite |
|----------------------------------------------------------------------------|---------------|--------------|
| Subir la versión 1.0 y etiquetar `E2-v1.0` (IS.2.7)                        | Matías (LT)   | 2026-11-23   |
| Presentar la lista de espera como solicitud de cambio                      | CL            | Siguiente reunión quincenal (S5) |
| Iniciar el diseño detallado con la especificación validada (IS.3)          | Matías (LT) y Alexander (DIS) | S3 |
| Registrar esta acta en el repositorio                                      | Andrea        | 2026-11-23   |

---

## Cierre

- **Hora de cierre:** 11:00
- **Próxima reunión:** reunión quincenal con el CL en S5 (revisión de E3 y solicitudes de cambio).

---

## Firmas y aprobación

| Cliente (CL)              | Secretaria                |
|---------------------------|---------------------------|
| Firma: ________________   | Firma: ________________   |
| Nombre: Docente de la asignatura | Nombre: Andrea Raura |

| Asistente | Rol            | Firma            |
|-----------|----------------|------------------|
| Zaith Manangón | GP             | ________________ |
| Matías Lugmaña | LT, PR         | ________________ |
| Alexander Villacres | AN, DIS        | ________________ |
| Andrea Raura | RP, PR         | ________________ |

**Aprobado en sesión del:** pendiente (próxima reunión)
