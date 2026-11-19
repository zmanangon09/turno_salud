# Verificación del Plan del proyecto — GP.1.13

**Proyecto:** TurnoSalud · **Grupo 6**
**Plan revisado:** [Plan del proyecto](plan-proyecto.md)
**Fecha:** 2026-11-19 · **Registro:** Acta N.° 03

---

## Participantes
| Integrante | Rol | Qué revisó con más detalle |
| ------ | ------ | ------ |
| Zaith Manangón | GP | Estimación de costos por rol (3.10), cálculo de servicios (3.11), reserva para contingencias (3.12), presupuesto total (3.13) frente al límite de USD 18 000, matriz de riesgos (3.14) y mecanismos de seguimiento en GP.2 y GP.3. |
| Matías Lugmaña | LT, PR | Coherencia del objetivo, alcance, criterios de aceptación y entregables (E1 a E5) frente al Enunciado del trabajo revisado (GP.1.1 y GP.1.2); descomposición técnica de diseño y construcción (IS.3, IS.4), recursos y herramientas tecnológicas (GP.1.5), riesgos técnicos (GP.1.9) y estrategia de control de versiones y uso del repositorio GitHub (GP.1.10 y GP.1.15). |
| Alexander Villacres | AN, DIS | Descomposición de tareas de requisitos y diseño (IS.2, IS.3), correspondencia con los perfiles de usuario del sistema (paciente, recepcionista, médico, administrador), asignación de esfuerzo PERT y prototipado de interfaz en el calendario. |
| Andrea Raura | RP, PR | Inclusión de tareas de verificación y validación en cada proceso (GP e IS), estimación del paquete de integración y pruebas (IS.5), comprobación de capacidad de horas por integrante (3.7) y plantilla de control de defectos y retrabajo. |

## Puntos revisados
* [x] El objetivo, el alcance y los entregables coinciden con el enunciado revisado.
* [x] Todos los procesos tienen tareas y al menos una revisión o prueba.
* [x] Los cálculos PERT están bien hechos.
* [x] Las horas por integrante no superan la capacidad.
* [x] El calendario cabe en 12 semanas y respeta el orden de los procesos.
* [x] El presupuesto total no pasa de USD 18 000.
* [x] Cada riesgo tiene una respuesta y un responsable.
* [x] El repositorio se usa como dice el plan.

## Observaciones
| Sección del plan | Observación | Corrección | Responsable | ¿Corregido? |
| ------ | ------ | ------ | ------ | ------ |
| 3.1, 3.3 y 3.8 (Alineación con el Enunciado revisado) | Verificar que el objetivo, el alcance incluido/excluido y los 5 entregables con sus semanas de entrega (E1 en S2, E2 en S3, E3 en S5, E4 en S10 y E5 en S12 definidos en la sección 2.6 del Enunciado) coincidan exactamente con los productos de trabajo y los hitos del calendario del Plan. | Se vincularon los entregables E1 a E5 y sus instrucciones de entrega (GP.1.2) con las salidas de los procesos GP e IS y con la tabla de hitos del calendario. | Matías Lugmaña (LT) | Sí |
| 3.9, 3.14 y 3.15 (Recursos técnicos, riesgos y repositorio) | Asegurar que los supuestos técnicos del Enunciado revisado (arquitectura web cliente-servidor, base de datos relacional, alojamiento en la nube y servicio SMTP) y las reglas de trabajo en el repositorio turno_salud estén reflejados en el Plan. | Se detallaron los recursos tecnológicos necesarios, el riesgo técnico de cruce de horarios/concurrencia con su plan de mitigación y las convenciones de ramas, commits y versionado en GitHub. | Matías Lugmaña (LT, PR) | Sí |
| 3.5, 3.6 y 3.10 (Consistencia matemática PERT y costos) | Ajustar las estimaciones PERT y la tabla de costo por rol para que la suma total de horas (740 h) coincida exactamente con la matriz de asignación por integrante y no exceda el presupuesto de USD 18 000. | Se recalcularon los valores O, M y P asegurando divisiones exactas por 6, y se balanceó la distribución de esfuerzo por integrante manteniendo el presupuesto consolidado en USD 16 995. | Zaith Manangón (GP) | Sí |

## Conclusión
El Plan del proyecto `plan-proyecto.md` ha sido revisado minuciosamente por todos los integrantes del Equipo de Trabajo de la VSE en la sesión del 2026-11-19 (registrada en el Acta N.° 03). Todos los criterios normativos de la ISO/IEC 29110 (GP.1.13) han sido verificados satisfactoriamente, confirmando que los cálculos matemáticos, el cronograma de 12 semanas y el presupuesto consolidado (USD 16 995) se encuentran alineados con el Enunciado del trabajo revisado y dentro del límite máximo exigido (USD 18 000). Por lo tanto, el Plan queda en estado **VERIFICADO** y listo para ser presentado al Cliente para su aprobación formal (GP.1.14).

**Firmas del equipo:**
| Integrante | Firma |
| ------ | ------ |
| Zaith Manangón | ________________ |
| Matías Lugmaña | ________________ |
| Alexander Villacres | ________________ |
| Andrea Raura | ________________ |
