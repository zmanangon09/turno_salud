# VSE de Sangolquí — Proyecto TurnoSalud

ESPE · Aseguramiento de la Calidad de Software · **Grupo 6** · Caso «TurnoSalud» (ISO/IEC 29110, Perfil Básico)

## ACTA DE REUNIÓN No. 05

| Campo                  | Valor                                                    | Campo            | Valor                                             |
|------------------------|----------------------------------------------------------|------------------|---------------------------------------------------|
| **Tipo de reunión**    | [x] Ordinaria  [ ] Extraordinaria                        | **Fecha**        | 2026-11-23 (semana 3 del proyecto)                |
| **Hora inicio**        | 08:00                                                    | **Hora cierre**  | 09:10                                             |
| **Órgano reunido**     | Equipo de trabajo (ET) de la VSE                         | **Modalidad**    | [ ] Presencial  [x] Virtual  [ ] Mixta            |
| **Lugar / Plataforma** | Google Meet                                              |                  |                                                   |

---

## Asistentes y quórum

- **Quórum requerido presente:** [x] Sí  [ ] No
- **Miembros presentes:** 4 de 4

### Asistentes

| Nombre    | Cargo (rol ISO/IEC 29110)                       |
|-----------|-------------------------------------------------|
| Zaith Manangón | Gestor del proyecto (GP)                       |
| Matías Lugmaña | Líder técnico (LT) y Programador (PR)           |
| Alexander Villacres | Analista (AN) y Diseñador (DIS)                 |
| Andrea Raura | Responsable de pruebas (RP) y Programadora (PR). Secretaria |

**Ausentes:** Ninguno

**Invitados:** Ninguno. La validación con el cliente (CL) se hace en una reunión aparte (Acta 06).

---

## Orden del día

1. Lectura y aprobación del Acta 04.
2. Inicio de la implementación (IS.1) y asignación de tareas de requisitos (IS.2.1).
3. Verificación de la Especificación de requisitos, versión 0.1 (IS.2.3).
4. Preparación de la validación con el cliente (IS.2.4).

---

## Desarrollo de la reunión

### Punto 1: Lectura y aprobación del Acta 04

Resumen de lo discutido: se leyó el Acta 04 (2026-11-20), en la que el CL aceptó el Plan del proyecto, versión 1.0. Sin observaciones.

### Punto 2: Inicio de la implementación y asignación de tareas

Resumen de lo discutido: Zaith (GP) recordó que en S2 se revisó el plan con todo el equipo (IS.1.1) y que el hito «Entorno de implementación listo» se cumplió: Matías (LT) confirmó que el repositorio de código, el servidor de pruebas y la base de datos de pruebas funcionan. Para IS.2 quedaron estas tareas (IS.2.1):

| Tarea | Responsable |
|-------|-------------|
| Redactar la especificación y los prototipos | Alexander (AN, DIS) |
| Revisar factibilidad técnica y seguridad | Matías (LT) |
| Revisar que cada requisito se pueda probar y reservar los casos de prueba | Andrea (RP) |
| Revisar el alcance y coordinar la validación con el CL | Zaith (GP) |

### Punto 3: Verificación de la Especificación de requisitos

Resumen de lo discutido: Alexander presentó la versión 0.1 (18 requisitos funcionales, 7 reglas de negocio, 7 no funcionales y 9 prototipos). El equipo aplicó la lista de verificación y encontró siete observaciones: requisitos sin medida (RF-08, RF-12, RNF-04), cruces por consultorio y reservas simultáneas (RF-09), turnos afectados por ausencias (RF-06), vencimiento del enlace de recuperación (RF-02) y una exportación a Excel que no estaba en el alcance (RF-17). Alexander las corrigió durante la reunión y en la tarde, y el equipo revisó la versión 0.2. Detalle en [Resultados de verificación](../04-requisitos/resultados-verificacion-requisitos.md).

### Punto 4: Preparación de la validación

Resumen de lo discutido: se acordó que Alexander conduce la validación, Andrea mide la prueba de usabilidad del flujo de reserva (pasos y tiempo) y Zaith anota las observaciones del CL. Se acordó también separar, en el momento, lo que es corrección dentro del alcance de lo que es función nueva: lo segundo no se agrega a la especificación, se deriva a solicitud de cambio (riesgo R1).

---

## Decisiones y votaciones

| # | Decisión                                                                                   | Votación                                   |
|---|--------------------------------------------------------------------------------------------|--------------------------------------------|
| 1 | Aprobar el Acta 04 sin observaciones                                                       | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 2 | Dar por **verificada** la Especificación de requisitos, versión 0.2 (IS.2.3)               | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 3 | Enviar la especificación y los prototipos al CL con 48 h de anticipación                   | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |

---

## Compromisos y tareas

| Compromiso / Tarea                                                         | Responsable   | Fecha límite |
|----------------------------------------------------------------------------|---------------|--------------|
| Subir la versión 0.2 y los resultados de verificación al repositorio       | Alexander (AN) | 2026-11-23  |
| Enviar la especificación al CL y convocar la validación                     | Zaith (GP)    | 2026-11-23   |
| Preparar el guion y el cronómetro de la prueba de usabilidad               | Andrea (RP)   | 2026-11-23   |
| Registrar esta acta en el repositorio                                      | Andrea        | 2026-11-23   |

---

## Cierre

- **Hora de cierre:** 09:10
- **Próxima reunión:** validación de requisitos con el CL (Acta 06).

---

## Firmas y aprobación

| Presidente (GP)           | Secretaria                |
|---------------------------|---------------------------|
| Firma: ________________   | Firma: ________________   |
| Nombre: Zaith Manangón    | Nombre: Andrea Raura      |

**Aprobado en sesión del:** pendiente (próxima reunión)
