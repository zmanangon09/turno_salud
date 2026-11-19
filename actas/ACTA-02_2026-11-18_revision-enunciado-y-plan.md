# VSE de Sangolquí — Proyecto TurnoSalud

ESPE · Aseguramiento de la Calidad de Software · **Grupo 6** · Caso «TurnoSalud» (ISO/IEC 29110, Perfil Básico)

## ACTA DE REUNIÓN No. 02

| Campo                  | Valor                                                    | Campo            | Valor                                             |
|------------------------|----------------------------------------------------------|------------------|---------------------------------------------------|
| **Tipo de reunión**    | [x] Ordinaria  [ ] Extraordinaria                        | **Fecha**        | 2026-11-18                                        |
| **Hora inicio**        | 18:30                                                    | **Hora cierre**  | HH:MM (completar al cerrar)                       |
| **Órgano reunido**     | Equipo de trabajo (ET) de la VSE                         | **Modalidad**    | [ ] Presencial  [x] Virtual  [ ] Mixta            |
| **Lugar / Plataforma** | Google Meet               |                  |                                                   |

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
| Andrea Raura | Responsable de pruebas (RP) y Programadora (PR). Organizadora y secretaria |

**Ausentes:** Ninguno

**Invitados:** Ninguno. El cliente (CL), representado por el docente, no participa en esta reunión; sus validaciones se registrarán aparte.

---

## Orden del día

1. Lectura y aprobación del Acta 01.
2. Organización del repositorio y de la forma de trabajo del equipo.
3. Revisión del Enunciado del trabajo (GP.1.1).
4. Propuesta de instrucciones de entrega (GP.1.2).
5. Distribución del trabajo para elaborar el Plan del proyecto (GP.1.3 a GP.1.12).

---

## Desarrollo de la reunión

### Punto 1: Lectura y aprobación del Acta 01

Resumen de lo discutido: se leyó el Acta 01 (2026-11-18, 10:00–11:00), que registra la elección del Perfil Básico y la asignación de roles. No hubo observaciones.

### Punto 2: Organización del repositorio y forma de trabajo

Resumen de lo discutido: se acordó documentar toda la actividad en el repositorio de GitHub `turno_salud`, en archivos Markdown (`.md`), con esta estructura:

| Carpeta / archivo        | Contenido                                                  |
|--------------------------|------------------------------------------------------------|
| `actas/`                 | Una acta por cada reunión del equipo o con el cliente      |
| `plantillas/`            | Plantilla de acta usada por el equipo                      |
| `01-seleccion-perfil/`   | Justificación del perfil elegido (paso 1)                  |
| `02-enunciado-trabajo/`  | Enunciado del trabajo [revisado] (paso 2: GP.1.1)          |
| `03-plan-proyecto/`      | Plan del proyecto y resultados de su verificación (paso 3) |

Cada documento indicará en su encabezado la tarea de la norma que lo produce, el rol que lo elabora, su versión y su estado (borrador, revisado, verificado, aceptado). El repositorio servirá también como base para la estrategia de control de versiones (GP.1.10) y como repositorio del proyecto (GP.1.15).

### Punto 3: Revisión del Enunciado del trabajo (GP.1.1)

Resumen de lo discutido: el GP y el LT revisaron el Enunciado recibido. Contiene el cliente (clínica privada), el producto (aplicación web de agendamiento de turnos), el plazo (12 semanas), el presupuesto (USD 18 000) y la condición de producto no crítico para la seguridad. Se detectaron estos vacíos:

| # | Vacío detectado en el Enunciado                                            | Tratamiento acordado                              |
|---|----------------------------------------------------------------------------|---------------------------------------------------|
| 1 | No detalla las funcionalidades que se esperan (alcance)                    | Proponer un alcance incluido y excluido           |
| 2 | No identifica a los usuarios del sistema (pacientes, recepción, profesionales, administración) | Proponer los tipos de usuario                    |
| 3 | No define los entregables ni cuándo se entregan                            | Proponer una lista de entregables (GP.1.2)        |
| 4 | No establece criterios de aceptación                                       | Proponer criterios medibles                       |
| 5 | No menciona restricciones técnicas (navegadores, alojamiento, datos)       | Registrarlas como supuestos                       |
| 6 | No nombra a un representante del cliente para las consultas                | Asumir al docente como CL                         |

Cada propuesta quedará marcada como **supuesto** hasta que el cliente la confirme.

### Punto 4: Propuesta de instrucciones de entrega (GP.1.2)

Resumen de lo discutido: según la norma, el GP define las instrucciones de entrega de cada entregable junto con el cliente, y el resultado pasa a formar parte del Plan del proyecto. Como el cliente es hipotético, el equipo preparará una propuesta (elementos de cada entregable, momento, forma de entrega y aceptación final) para que el docente, en su papel de CL, la valide.

### Punto 5: Distribución del trabajo para el Plan del proyecto

Resumen de lo discutido: el Plan será un solo documento, con una sección por cada tarea GP.1.3 a GP.1.12. La norma asigna estas tareas al GP y al LT. El AN/DIS aporta en lo relativo a requisitos y diseño, y el RP en las tareas de verificación, validación y pruebas. La verificación del plan con todo el equipo (GP.1.13) y su aceptación por el cliente (GP.1.14) se registrarán en actas posteriores.

---

## Decisiones y votaciones

| # | Decisión                                                                                   | Votación                                   |
|---|--------------------------------------------------------------------------------------------|--------------------------------------------|
| 1 | Aprobar el Acta 01 sin observaciones                                                       | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 2 | Documentar la actividad en GitHub, en Markdown, con la estructura descrita en el Punto 2    | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 3 | Completar los vacíos del Enunciado con supuestos explícitos, sujetos a confirmación del CL | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 4 | Incluir las instrucciones de entrega en el Plan como propuesta hasta que el CL las valide   | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 5 | Elaborar el Plan del proyecto como un único documento, con una sección por tarea GP.1.x    | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |

---

## Compromisos y tareas

| Compromiso / Tarea                                                                  | Responsable                                  | Fecha límite   |
|-------------------------------------------------------------------------------------|----------------------------------------------|----------------|
| Redactar la justificación de la selección del perfil (paso 1)                        | Zaith (GP), con apoyo de Andrea               | Por confirmar  |
| Documentar el Enunciado del trabajo [revisado] con los supuestos (GP.1.1)            | Zaith (GP) y Matías (LT)                      | Por confirmar  |
| Preparar la propuesta de instrucciones de entrega para validar con el CL (GP.1.2)    | Zaith (GP)                                    | Por confirmar  |
| Definir tareas, duración, recursos, equipo y calendario (GP.1.3 a GP.1.7)            | Zaith (GP) y Matías (LT), con apoyo de Alexander y Andrea | Por confirmar |
| Calcular el esfuerzo y el costo (GP.1.8)                                             | Zaith (GP)                                    | Por confirmar  |
| Identificar los riesgos del proyecto (GP.1.9)                                        | Zaith (GP) y Matías (LT), con apoyo de Andrea | Por confirmar  |
| Documentar la estrategia de control de versiones (GP.1.10)                           | Zaith (GP) y Matías (LT)                      | Por confirmar  |
| Mantener las actas y la estructura del repositorio                                  | Andrea                                        | Permanente     |

---

## Cierre

- **Hora de cierre:** HH:MM (completar al cerrar)
- **Próxima reunión:** Fecha por definir. Verificación del Plan del proyecto con el equipo (GP.1.13), Acta 03.

---

## Firmas y aprobación

| Organizadora y secretaria |
|---------------------------|
| Firma: ________________   |
| Nombre: Andrea Raura      |

| Asistente | Rol            | Firma            |
|-----------|----------------|------------------|
| Zaith Manangón | GP             | ________________ |
| Matías Lugmaña | LT, PR         | ________________ |
| Alexander Villacres | AN, DIS        | ________________ |
| Andrea Raura | RP, PR         | ________________ |

**Aprobado en sesión del:** YYYY-MM-DD (próxima reunión)
