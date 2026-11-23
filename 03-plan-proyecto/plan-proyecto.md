# 3. Plan del proyecto — GP y LT

**Proyecto:** TurnoSalud · **Grupo 6**
**Responsables:** Zaith Manangón (GP) y Matías Lugmaña (LT) · **Apoyo:** Alexander Villacres (AN/DIS) y Andrea Raura (RP)
**Tareas de la norma:** GP.1.3 a GP.1.15
**Producto de entrada:** [Enunciado del trabajo revisado](../02-enunciado-trabajo/enunciado-trabajo.md)
**Versión:** 1.1 · **Estado:** Aceptado ([Acta 03](../actas/ACTA-03_2026-11-19_verificacion-plan.md) verificación · [Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md) aceptación de v1.0 · [Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md) aceptación de v1.1)

> **Versión 1.1:** las secciones 3.1 a 3.17 conservan la línea base v1.0. Los cambios por la solicitud SC-01 están en la sección [3.18](#318-control-de-cambios-del-plan); donde una cifra cambió, manda la 3.18.

---

## 3.1 Objetivo de la planificación

El plan traduce el Enunciado del trabajo revisado en un camino concreto para entregar TurnoSalud en 12 semanas y sin pasar de USD 18 000. Dice qué tareas se hacen en cada proceso del Perfil Básico, quién las hace, cuántas horas cuestan, en qué semana ocurren y cuánto dinero consumen. También deja anotados los riesgos y las reglas para trabajar en el repositorio. Sirve de línea base: durante el seguimiento (GP.2) el avance real se compara contra lo que está escrito aquí, y cualquier cambio de alcance, plazo o costo se gestiona como solicitud de cambio.

Técnicas que se usan en este plan. Ayudan a elaborarlo, pero la ISO/IEC 29110 no las exige:

- **Descomposición del trabajo por procesos:** las tareas se agrupan según los procesos GP e IS del Perfil Básico, en lugar de una EDT por módulos.
- **Estimación de tres puntos (PERT):** el esfuerzo de cada proceso sale de un valor optimista, uno más probable y uno pesimista.
- **Diagrama de Gantt simplificado:** el calendario se muestra por semanas, con los hitos de entrega.
- **Costeo de abajo hacia arriba:** el costo del trabajo se calcula con las horas de cada rol multiplicadas por su tarifa.
- **Valor monetario esperado:** la reserva para contingencias se calcula como probabilidad × impacto económico de cada riesgo.
- **Matriz probabilidad-impacto:** los riesgos se califican como baja, media o alta.

## 3.2 Roles y responsabilidades (GP.1.6)

| Integrante | Roles | Responsabilidades |
| ------ | ------ | ------ |
| Zaith Manangón | GP | Planificar, coordinar y controlar el proyecto; administrar el calendario, presupuesto y cambios (SC01); liderar reuniones del equipo y coordinar la validación y aceptación con el cliente. |
| Matías Lugmaña | LT, PR | Definir la arquitectura de software, tomar decisiones técnicas, liderar la programación backend y base de datos, realizar revisiones de código y administrar el repositorio GitHub. |
| Alexander Villacres | AN, DIS | Elucidar y especificar los requisitos de software, diseñar prototipos e interfaces de usuario, garantizar usabilidad, navegación y mantener la trazabilidad de requisitos a pruebas. |
| Andrea Raura | RP, PR | Diseñar y ejecutar planes/casos de prueba, programar módulos frontend, controlar la corrección de defectos y retrabajo, redactar actas y gestionar la documentación del proyecto. |
| Docente | CL | Representante hipotético del cliente (clínica); retroalimentar necesidades, validar la Especificación de Requisitos (SRS), revisar e instruir la entrega de artefactos (E1 a E5) y aprobar formalmente los cambios. |

**Significado de los códigos:** GP gestor del proyecto · LT líder técnico · AN analista · DIS diseñador · PR programador · RP responsable de pruebas · CL cliente · ET equipo de trabajo.

Los seis puestos del caso quedan cubiertos así: Matías y Andrea ocupan los dos puestos de programador además de su rol principal.

## 3.3 Descomposición del trabajo por procesos (GP.1.3)

| Proceso | Tareas incluidas | Producto de trabajo |
| ------ | ------ | ------ |
| GP.1 Planificación | Revisar el Enunciado, elaborar el Plan del proyecto, definir calendario, estimar esfuerzo y costos, analizar riesgos, establecer repositorio y verificar el plan. | Plan del proyecto (GP.1.12) y Registro de verificación (GP.1.13) |
| IS.1 Inicio de la implementación | Revisar el Plan con el equipo de trabajo, asignar tareas, preparar entornos de desarrollo, herramientas y repositorio. | Registro de inicio del proyecto e Instructivo de trabajo |
| IS.2 Análisis de requisitos | Elucidar requisitos con el cliente, redactar la Especificación de Requisitos de Software (SRS), verificarla internamente y validarla con el cliente. | Especificación de Requisitos de Software [validada] (IS.2.4) |
| IS.3 Arquitectura y diseño detallado | Diseñar la arquitectura web cliente-servidor, modelo de datos relacional, componentes de software, prototipos de interfaz y verificar el diseño. | Documento de Arquitectura y Diseño [verificado] (IS.3.3) |
| IS.4 Construcción | Programar módulos (autenticación, especialidades/horarios, agendamiento, administración), realizar pruebas unitarias y revisiones de código. | Componentes de software y Resultados de pruebas unitarias (IS.4.2) |
| IS.5 Integración y pruebas | Integrar componentes, ejecutar pruebas de integración, usabilidad, rendimiento y seguridad; registrar y corregir defectos. | Software integrado y Reporte de pruebas del sistema [verificado] (IS.5.2) |
| IS.6 Entrega del producto | Desplegar la aplicación en el servidor de producción, elaborar manuales de usuario e instalación, capacitar al personal y entregar la configuración. | Configuración de software entregada y Manuales (IS.6.5) |
| GP.2 a GP.4 Seguimiento y cierre | Evaluar el avance semanal, controlar desviaciones y solicitudes de cambio (SC01), medir el retrabajo, formalizar la aceptación del cliente y cerrar el proyecto. | Reportes de avance, Registro de cambios y Acta de Aceptación (GP.4.2) |


## 3.4 Esfuerzo y duración

El **esfuerzo** son las horas de trabajo que necesita una tarea, la haga una persona o tres. Se mide en horas-persona. La **duración** es cuánto tiempo de calendario pasa desde que la tarea empieza hasta que termina, y se mide en semanas. Están relacionadas, pero no son lo mismo: si dos personas trabajan en paralelo, el esfuerzo es el mismo y la duración baja.

Ejemplo en TurnoSalud: supongamos que el módulo de agendamiento (reservar, reprogramar y cancelar sin cruces de horario) necesita 120 horas-persona. Si Matías lo construye solo, con unas 36 horas semanales para construcción, tarda algo más de 3 semanas (120 ÷ 36 ≈ 3,3). Si Matías hace el backend y Andrea las pantallas en paralelo, el mismo trabajo se termina en menos de 2 semanas (120 ÷ 72 ≈ 1,7). El esfuerzo sigue siendo 120 horas-persona y por tanto cuesta lo mismo; solo se acorta la duración. En la práctica se suman algunas horas de coordinación entre los dos, y no todo trabajo se puede repartir: una tarea que depende de otra no se acelera con más personas.

Por eso el plan estima primero el esfuerzo (3.5), luego lo reparte entre las personas (3.6) y recién con eso arma el calendario (3.8).

## 3.5 Estimación del esfuerzo con PERT (GP.1.4)
**E = (O + 4M + P) ÷ 6**

- **O (optimista):** horas si todo sale bien, sin retrabajo ni dudas del cliente.
- **M (más probable):** horas en condiciones normales; por eso pesa cuatro veces.
- **P (pesimista):** horas si aparecen los problemas razonables (requisitos que cambian, defectos difíciles, ausencias), sin llegar a catástrofes.

Los valores los propuso quien hará la mayor parte de cada proceso: Zaith para GP.1 y GP.2 a GP.4, Matías para IS.1, IS.3, IS.4 e IS.6, Alexander para IS.2 y Andrea para IS.5.

| Proceso                              | O | M | P | Cálculo | Esfuerzo (h-persona) |
|--------------------------------------|---|---|---|---------|----------------------|
| GP.1 Planificación                   | 36 | 52 | 80 | (36 + 208 + 80) ÷ 6 = 324 ÷ 6 | 54 |
| IS.1 Inicio de la implementación     | 12 | 19 | 32 | (12 + 76 + 32) ÷ 6 = 120 ÷ 6 | 20 |
| IS.2 Análisis de requisitos          | 86 | 122 | 182 | (86 + 488 + 182) ÷ 6 = 756 ÷ 6 | 126 |
| IS.3 Arquitectura y diseño detallado | 104 | 146 | 212 | (104 + 584 + 212) ÷ 6 = 900 ÷ 6 | 150 |
| IS.4 Construcción                    | 330 | 420 | 618 | (330 + 1 680 + 618) ÷ 6 = 2 628 ÷ 6 | 438 |
| IS.5 Integración y pruebas           | 140 | 194 | 296 | (140 + 776 + 296) ÷ 6 = 1 212 ÷ 6 | 202 |
| IS.6 Entrega del producto            | 32 | 48 | 76 | (32 + 192 + 76) ÷ 6 = 300 ÷ 6 | 50 |
| GP.2 a GP.4 Seguimiento y cierre     | 72 | 104 | 160 | (72 + 416 + 160) ÷ 6 = 648 ÷ 6 | 108 |
| **Total**                            |   |   |   |         | **1 148**            |

**Ejemplo desarrollado (IS.4 Construcción):**

1. Valores propuestos por Matías: O = 330 h, M = 420 h, P = 618 h.
2. Se multiplica el más probable por 4: 4 × 420 = 1 680.
3. Se suman los tres términos: 330 + 1 680 + 618 = 2 628.
4. Se divide para 6: 2 628 ÷ 6 = **438 horas-persona**.

El resultado queda más cerca de M que del promedio simple ((330 + 420 + 618) ÷ 3 = 456), porque el pesimista solo pesa una sexta parte. Construcción es casi el 38 % del esfuerzo total, lo que es normal en un proyecto de desarrollo.

## 3.6 Distribución del esfuerzo por integrante

| Proceso                              | Zaith | Matías | Alexander | Andrea | Total |
|--------------------------------------|-------|--------|-----------|--------|-------|
| GP.1 Planificación                   | 24 | 16 | 8 | 6 | 54 |
| IS.1 Inicio de la implementación     | 6 | 8 | 3 | 3 | 20 |
| IS.2 Análisis de requisitos          | 18 | 20 | 56 | 32 | 126 |
| IS.3 Arquitectura y diseño detallado | 8 | 66 | 58 | 18 | 150 |
| IS.4 Construcción                    | 0 | 160 | 154 | 124 | 438 |
| IS.5 Integración y pruebas           | 24 | 52 | 24 | 102 | 202 |
| IS.6 Entrega del producto            | 14 | 20 | 8 | 8 | 50 |
| GP.2 a GP.4 Seguimiento y cierre     | 82 | 10 | 8 | 8 | 108 |
| **Total por integrante**             | **176** | **352** | **319** | **301** | **1 148** |

Zaith (GP) no programa: sus horas de IS.2, IS.5 e IS.6 son reuniones con el cliente, validaciones y la entrega formal. Las 154 h de Alexander en IS.4 corresponden a construir las vistas que él mismo diseñó.

## 3.7 Comprobación de capacidad

- Horas semanales supuestas por persona: **40** (jornada completa; el Enunciado indica que la VSE dedica su capacidad solo a este proyecto).
- Capacidad nominal = 4 personas × 40 h × 12 semanas = **1 920 horas-persona**.
- Utilización = 1 148 ÷ 1 920 × 100 = **59,8 %**.

| Integrante | Horas asignadas | Capacidad (40 × 12) | Utilización |
|------------|-----------------|---------------------|-------------|
| Zaith      | 176 | 480 | 36,7 % |
| Matías     | 352 | 480 | 73,3 % |
| Alexander  | 319 | 480 | 66,5 % |
| Andrea     | 301 | 480 | 62,7 % |

Carga semanal estimada (horas por persona):

| Integrante | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 | S10 | S11 | S12 |
|------------|----|----|----|----|----|----|----|----|----|-----|-----|-----|
| Zaith      | 14 | 22 | 20 | 12 | 12 | 8 | 8 | 8 | 12 | 18 | 24 | 18 |
| Matías     | 10 | 22 | 30 | 32 | 36 | 36 | 36 | 36 | 36 | 32 | 30 | 16 |
| Alexander  | 6 | 31 | 36 | 32 | 36 | 34 | 34 | 32 | 32 | 26 | 12 | 8 |
| Andrea     | 4 | 15 | 24 | 12 | 22 | 34 | 34 | 38 | 38 | 38 | 32 | 10 |

Nadie supera las 40 horas en ninguna semana, pero hay tres momentos de carga alta:

- **Alexander en S3 (36 h):** cierra la Especificación de requisitos (E2) y empieza el diseño al mismo tiempo.
- **Matías de S5 a S9 (36 h por semana):** termina el diseño y construye el backend, que es el camino crítico.
- **Andrea de S8 a S10 (38 h por semana):** termina sus módulos mientras ejecuta las pruebas que alimentan el Informe de pruebas (E4).

La utilización global es baja porque S1, S2 y S12 tienen poco trabajo técnico y porque el rol de GP no ocupa una jornada completa. Esa holgura no se elimina: es el margen para absorber solicitudes de cambio, ausencias o retrabajo sin mover las fechas de entrega. Si Matías o Andrea se retrasan en construcción, Alexander puede tomar pantallas de recepción desde S10 y Zaith puede apoyar la ejecución de pruebas de validación.

## 3.8 Calendario (GP.1.7)

| Proceso      | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 | S10 | S11 | S12 |
|--------------|----|----|----|----|----|----|----|----|----|-----|-----|-----|
| GP.1         | ■ | ■ | | | | | | | | | | |
| IS.1         | | ■ | | | | | | | | | | |
| IS.2         | | ■ | ■ | | | | | | | | | |
| IS.3         | | | ■ | ■ | ■ | | | | | | | |
| IS.4         | | | | | ■ | ■ | ■ | ■ | ■ | ■ | | |
| IS.5         | | | | | | | | ■ | ■ | ■ | ■ | |
| IS.6         | | | | | | | | | | | ■ | ■ |
| GP.2 a GP.4  | | | ■ | ■ | ■ | ■ | ■ | ■ | ■ | ■ | ■ | ■ |

Orden y solapamientos:

- El plan se acepta a mitad de S2; IS.1 y el arranque de IS.2 ocupan la segunda mitad de esa semana.
- En S3 el LT empieza la arquitectura general mientras el cliente valida los requisitos; el diseño detallado solo arranca con E2 validado.
- En S5 la construcción empieza por autenticación y catálogos, cuyo diseño se verifica primero; el resto de módulos espera a E3.
- La integración arranca en S8 con los módulos ya terminados; S10 deja solo ajustes de construcción y S11 se dedica a la validación con el cliente y a corregir defectos.

**Hitos:**

| Semana | Hito  | Cómo se comprueba |
|--------|-------|-------------------|
| 2  | **E1** Plan del proyecto aceptado y repositorio establecido | Resultados de verificación firmados ([Acta 03](../actas/ACTA-03_2026-11-19_verificacion-plan.md)) y aceptación del CL ([Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md)) |
| 2  | Entorno de implementación listo | Repositorio de código, servidor de pruebas y base de datos funcionando; revisado por el LT |
| 3  | **E2** Requisitos y prototipos validados | Acta de validación firmada por el CL |
| 5  | **E3** Arquitectura y diseño verificados | Resultados de verificación del diseño y matriz de trazabilidad revisados por LT y GP |
| 7  | Primer incremento en el servidor de pruebas | Autenticación, catálogos y agendamiento funcionando en staging, con pruebas unitarias aprobadas |
| 10 | **E4** Versión beta e Informe de pruebas | Informe de pruebas sin defectos críticos abiertos; demostración al CL en staging |
| 11 | Validación del sistema con el CL | Los 6 criterios de aceptación de la sección 2.8 del Enunciado comprobados y registrados en acta |
| 12 | **E5** Entrega final `v1.0.0` y cierre | Versión etiquetada en GitHub, sistema en producción y Acta de aceptación firmada (GP.4) |

## 3.9 Recursos y capacitación (GP.1.5)

| Recurso | Tipo (herramienta, servicio, equipo, capacitación) | Para qué se usa | Desde la semana |
|---------|----------------------------------------------------|-----------------|-----------------|
| Computadoras portátiles de los integrantes | Equipo (propio, sin costo) | Trabajo diario de todo el equipo | 1 |
| Repositorio GitHub `turno_salud` (plan gratuito) | Herramienta | Documentos, actas, código y control de versiones | 1 |
| Guía ISO/IEC 29110-5-1-2 (Perfil Básico) | Norma | Referencia de procesos, tareas y productos de trabajo | 1 |
| Google Meet | Herramienta (gratuita) | Reuniones del equipo y con el CL | 1 |
| Taller de ISO/IEC 29110 Perfil Básico | Capacitación (con costo) | Que los cuatro integrantes conozcan las tareas y productos que exige la norma | 1 |
| Figma Professional (1 editor) | Herramienta (con costo) | Prototipos y diseño de interfaz | 2 |
| VS Code, Node.js, Next.js, NestJS, Prisma, PostgreSQL | Herramientas (gratuitas, código abierto) | Construcción del frontend, backend y base de datos | 2 |
| Servidor en la nube de pruebas (staging) | Servicio (con costo) | Entorno de integración y demostraciones al CL | 2 |
| Almacenamiento de respaldos en la nube | Servicio (con costo) | Copias de la base de datos de pruebas y del repositorio | 2 |
| Autoaprendizaje guiado de NestJS y Prisma | Capacitación interna (sin costo extra) | Nivelar a Andrea y Alexander en el stack del backend; la imparte Matías | 2 |
| Jest, Playwright y Postman | Herramientas (gratuitas) | Pruebas unitarias, de extremo a extremo y de la API | 5 |
| Servicio de correo transaccional (SMTP) | Servicio (con costo) | Confirmaciones y recordatorios de turnos | 5 |
| Servidor en la nube de producción con PostgreSQL | Servicio (con costo) | Sistema final que usará la clínica | 9 |
| Dominio web | Servicio (con costo) | Dirección pública de TurnoSalud | 9 |
| BrowserStack Live | Herramienta (con costo) | Pruebas multinavegador, incluido Safari en iOS y macOS | 10 |

## 3.10 Costo del trabajo por rol (GP.1.8)
**Costo de un rol = horas del rol × tarifa del rol**

Las horas salen de 3.6: las horas de construcción (IS.4) de Matías y Andrea se pagan como PR y el resto de sus horas como LT y RP. Las tarifas son supuestos académicos: un sueldo mensual de referencia del mercado ecuatoriano para perfiles junior y semi-senior, más aportes patronales, dividido para 160 horas al mes, y redondeado.

| Rol    | Horas | Tarifa supuesta (USD/h) | Cálculo | Costo (USD) |
|--------|-------|-------------------------|---------|-------------|
| GP     | 176 | 15 | 176 × 15 | 2 640 |
| LT     | 192 | 14 | 192 × 14 | 2 688 |
| AN/DIS | 319 | 12 | 319 × 12 | 3 828 |
| PR     | 284 | 11 | 284 × 11 | 3 124 |
| RP     | 177 | 11 | 177 × 11 | 1 947 |
| **Total** | **1 148** |                    |         | **14 227** |

**Ejemplo desarrollado (PR):** las horas de programador son las de construcción de Matías (160 h) más las de Andrea (124 h): 160 + 124 = 284 h. Luego 284 h × USD 11/h = **USD 3 124**. Las otras 192 h de Matías (352 − 160) se cobran como LT y las otras 177 h de Andrea (301 − 124) como RP.

## 3.11 Servicios y herramientas
**Costo = cantidad × costo unitario**

Los precios son supuestos hasta tener cotizaciones. Las herramientas gratuitas de 3.9 no aparecen aquí.

| Servicio o herramienta | Cantidad | Precio supuesto | Cálculo | Costo (USD) |
|------------------------|----------|-----------------|---------|-------------|
| Servidor de pruebas (staging) | 3 meses | USD 24/mes | 3 × 24 | 72 |
| Servidor de producción con PostgreSQL | 2 meses | USD 48/mes | 2 × 48 | 96 |
| Correo transaccional SMTP (plan básico) | 3 meses | USD 15/mes | 3 × 15 | 45 |
| Dominio web | 1 año | USD 35/año | 1 × 35 | 35 |
| Figma Professional | 3 meses | USD 15/mes | 3 × 15 | 45 |
| Taller ISO/IEC 29110 Perfil Básico | 4 personas | USD 50/persona | 4 × 50 | 200 |
| Almacenamiento de respaldos | 3 meses | USD 5/mes | 3 × 5 | 15 |
| BrowserStack Live | 1 mes | USD 39/mes | 1 × 39 | 39 |
| **Total**              |          |                 |         | **547** |

El servidor de producción cubre desde S9 hasta la entrega y el primer mes de operación, mientras la clínica contrata su propio plan.

## 3.12 Reserva para contingencias
**Aporte a la reserva = probabilidad × impacto económico**

Solo se incluyen los riesgos de 3.14 que pueden costar dinero. El impacto es el trabajo o el gasto adicional que habría que pagar si el riesgo ocurre; no incluye horas que ya están en el presupuesto normal.

| Riesgo | Probabilidad | Impacto económico (USD) | Cálculo | Aporte (USD) |
|--------|--------------|-------------------------|---------|--------------|
| R1 Cambios de requisitos después de E2 | 0,40 | 2 000 | 0,40 × 2 000 | 800 |
| R2 Cruces de horario por concurrencia que obligan a rediseñar | 0,30 | 1 200 | 0,30 × 1 200 | 360 |
| R3 Ausencia temporal de un integrante | 0,25 | 1 600 | 0,25 × 1 600 | 400 |
| R4 Construcción subestimada | 0,30 | 1 500 | 0,30 × 1 500 | 450 |
| R5 Exposición de datos de pacientes | 0,10 | 2 000 | 0,10 × 2 000 | 200 |
| R6 Aumento del costo de servicios en la nube | 0,20 | 300 | 0,20 × 300 | 60 |
| **Reserva total** |   |                         |         | **2 270** |

La reserva la administra el GP y solo se usa con una solicitud de cambio o una acción correctiva registrada en acta.

## 3.13 Presupuesto total
**Presupuesto = trabajo + servicios + reserva**

| Concepto                        | Importe (USD) |
|---------------------------------|---------------|
| Trabajo del equipo (3.10)       | 14 227        |
| Servicios y herramientas (3.11) | 547           |
| Reserva (3.12)                  | 2 270         |
| **Total**                       | **17 044**    |
| Presupuesto máximo              | 18 000        |
| Margen                          | 956 (5,3 %)   |

El plan cabe en el presupuesto. El margen de USD 956 no es una segunda reserva: si no se usa, queda como ahorro para el cliente.

## 3.14 Riesgos (GP.1.9)

Escala: baja (≤ 20 %), media (21 % a 40 %), alta (> 40 %). Los riesgos R1 a R6 alimentan la reserva de 3.12.

| Riesgo | Probabilidad | Impacto | Qué haremos | Responsable |
|--------|--------------|---------|-------------|-------------|
| **R1** (cliente) El CL pide cambios de funciones después de validar los requisitos (E2). | Media | Alto | Validar prototipos antes de construir; registrar cada cambio como solicitud de cambio y evaluar su efecto en horas y costo antes de aprobarlo; posponer a una versión futura lo que no quepa. | Zaith (GP) |
| **R2** (técnico) Dos usuarios reservan el mismo médico y horario al mismo tiempo y se generan turnos cruzados. | Media | Alto | Restricción única en la base de datos (médico + fecha + hora), reserva dentro de una transacción y pruebas de concurrencia desde S8. | Matías (LT) |
| **R3** (equipo) Un integrante se ausenta por enfermedad o carga académica. | Media | Medio | Roles dobles ya cubiertos; documentación y código siempre en el repositorio; reasignar tareas usando la holgura de 3.7. | Zaith (GP) |
| **R4** (técnico) La construcción toma más horas que las estimadas. | Media | Alto | Comparar cada semana horas reales contra PERT; si la desviación pasa del 10 %, priorizar las funciones del alcance mínimo y mover apoyo de Alexander o Zaith. | Zaith (GP) y Matías (LT) |
| **R5** (técnico) Se exponen datos personales de los pacientes. | Baja | Alto | HTTPS, contraseñas cifradas con hash, control de acceso por rol, respaldos cifrados y revisión de seguridad en cada pull request. | Matías (LT) |
| **R6** (cliente/costos) Sube el precio de los servicios en la nube. | Baja | Bajo | Usar planes de precio fijo y activar alertas de facturación. | Zaith (GP) |
| **R7** (cliente) El CL no está disponible para validar a tiempo (E2, E4, aceptación). | Media | Medio | Agendar las reuniones quincenales desde S1 y enviar los entregables con 48 h de anticipación. | Zaith (GP) |
| **R8** (equipo) Poca experiencia de parte del equipo con NestJS o con la norma. | Media | Medio | Taller de ISO/IEC 29110 en S1 y nivelación técnica guiada por Matías en S2 a S4. | Matías (LT) |
| **R9** (técnico) Los correos de confirmación llegan a spam o no llegan. | Media | Bajo | Proveedor SMTP con SPF y DKIM configurados; pruebas de envío a varios proveedores de correo. | Andrea (RP) |

## 3.15 Control de versiones y repositorio (GP.1.10 y GP.1.15)

- **Repositorio:** https://github.com/zmanangon09/turno_salud. Los cuatro integrantes tienen permiso de escritura; el docente (CL) tiene acceso de lectura.
- **Qué se guarda:** todos los productos de trabajo en Markdown (selección del perfil, Enunciado, Plan, resultados de verificación, especificación, diseño, casos de prueba, informes, manuales y guías), las actas en `actas/`, las plantillas en `plantillas/` y, desde IS.1, el código fuente y los scripts de base de datos.
- **Ramas:** `main` contiene solo versiones revisadas. Cada trabajo se hace en una rama con el formato `<nombre>-<rol>/<tema>`, por ejemplo `andrea-rp-pr/docs-planificacion` o `matias-lt-pr/api-turnos`. Se fusiona a `main` mediante pull request revisado por al menos otro integrante; los cambios de código los aprueba el LT.
- **Cómo se nombran los cambios (commits):** formato `tipo(código): descripción en presente`, con `tipo` = `docs`, `feat`, `fix`, `test` o `chore` y el código de la tarea de la norma. Ejemplos: `docs(GP.1.8): calcular costo por rol` y `feat(IS.4): validar cruce de horarios al reservar`.
- **Cómo se identifican las versiones:** cada documento lleva en su encabezado **Versión** (0.x borrador, 1.0 aceptado, 1.1 en adelante cambios aprobados) y **Estado** (borrador, revisado, verificado, aceptado). Cada entregable aceptado se marca con una etiqueta (`E1-v1.0` a `E4-v1.0`) y el software usa versiones semánticas hasta `v1.0.0` en E5.
- **Respaldo:** GitHub es la copia principal y cada integrante mantiene un clon local actualizado. Cada viernes el GP descarga una copia comprimida del repositorio y de la base de datos de pruebas en el almacenamiento de respaldos (GP.2).

## 3.16 Seguimiento y control

El seguimiento no se hace en esta etapa: se ejecuta durante el proyecto en **GP.2 (evaluación del progreso)** y **GP.3 (control)**, usando este plan como referencia. Lo previsto es:

- **Reunión semanal del equipo** (lunes, 30 minutos, virtual): cada integrante informa lo terminado, lo pendiente y los bloqueos. El GP actualiza el Registro de estado del progreso.
- **Reunión quincenal con el CL:** demostración de avances, validación de entregables y decisión sobre solicitudes de cambio. Cada reunión deja un acta en `actas/`.
- **Qué se mide:** horas reales frente a las estimadas por proceso (3.5 y 3.6), entregables a tiempo frente a los hitos (3.8), gasto acumulado frente al presupuesto (3.13), defectos abiertos por gravedad, solicitudes de cambio y estado de los riesgos (3.14).
- **Cuándo se actúa:** si un proceso se desvía más del 10 % en horas o un hito se atrasa más de una semana, el GP propone una acción correctiva (GP.3) y, si cambia alcance, plazo o costo, se actualiza el plan con una nueva versión aprobada por el CL.

## 3.17 Verificación y aceptación del plan (GP.1.13 y GP.1.14)

- **Verificación con el equipo:** [Resultados de verificación](resultados-verificacion-plan.md), registrada en el [Acta 03](../actas/ACTA-03_2026-11-19_verificacion-plan.md) (2026-11-19).
- **Aceptación del cliente:** [Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md) (2026-11-20). El CL aceptó la versión 1.0 sin cambios.

**Productos de trabajo:** Plan del proyecto [verificado y aceptado], con las instrucciones de entrega de E1 a E5 incluidas · Resultados de verificación del plan · Registro de reunión (Actas 03 y 04) · Repositorio del proyecto establecido con la estrategia de control de versiones de 3.15.

## 3.18 Control de cambios del plan

| Versión | Semana | Cambio | Aprobó |
|---------|--------|--------|--------|
| 1.0 | S2 | Línea base del proyecto | CL ([Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md)) |
| 1.1 | S5 | Solicitud de cambio [SC-01](../05-solicitudes-cambio/SC-01_lista-de-espera.md), lista de espera: +54 h y USD 647 tomados de la reserva | CL ([Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md)) |

La solicitud [SC-02](../05-solicitudes-cambio/SC-02_notificaciones-whatsapp.md) (WhatsApp) fue rechazada y no cambia el plan. El detalle de cada solicitud está en el [Registro de solicitudes de cambio](../05-solicitudes-cambio/registro-solicitudes-cambio.md).

**Esfuerzo (reemplaza los totales de 3.5 y 3.6):**

| Proceso | v1.0 | SC-01 | v1.1 |
|---------|------|-------|------|
| GP.1 Planificación | 54 | 0 | 54 |
| IS.1 Inicio de la implementación | 20 | 0 | 20 |
| IS.2 Análisis de requisitos | 126 | +8 | 134 |
| IS.3 Arquitectura y diseño detallado | 150 | +8 | 158 |
| IS.4 Construcción | 438 | +24 | 462 |
| IS.5 Integración y pruebas | 202 | +8 | 210 |
| IS.6 Entrega del producto | 50 | +2 | 52 |
| GP.2 a GP.4 Seguimiento y cierre | 108 | +4 | 112 |
| **Total** | **1 148** | **+54** | **1 202** |

| Integrante | v1.0 | SC-01 | v1.1 | Utilización (sobre 480 h) |
|------------|------|-------|------|---------------------------|
| Zaith      | 176 | +5 | 181 | 37,7 % |
| Matías     | 352 | +21 | 373 | 77,7 % |
| Alexander  | 319 | +12 | 331 | 69,0 % |
| Andrea     | 301 | +16 | 317 | 66,0 % |
| **Total**  | **1 148** | **+54** | **1 202** | **62,6 %** |

**Carga semanal (reemplaza la tabla de 3.7 desde S5):**

| Integrante | S5 | S6 | S7 | S8 | S9 | S10 | S11 | S12 |
|------------|----|----|----|----|----|-----|-----|-----|
| Zaith      | 14 | 11 | 8 | 8 | 12 | 18 | 24 | 18 |
| Matías     | 37 | 40 | 40 | 40 | 38 | 36 | 32 | 16 |
| Alexander  | 36 | 40 | 38 | 32 | 32 | 26 | 14 | 8 |
| Andrea     | 22 | 34 | 38 | 40 | 40 | 40 | 38 | 10 |

Nadie pasa de 40 h, pero la holgura de 3.7 desaparece para Matías de S6 a S8 y para Andrea de S8 a S10. Por eso el riesgo R4 pasa de media a **alta** y el GP compara horas reales contra plan cada lunes.

**Calendario:** sin cambios en los hitos de 3.8. El diseño (E3) se actualiza a v1.1 en S7.

**Presupuesto (reemplaza 3.13):**

| Concepto | v1.0 (USD) | SC-01 | v1.1 (USD) |
|----------|------------|-------|------------|
| Trabajo del equipo | 14 227 | + 647 | 14 874 |
| Servicios y herramientas | 547 | 0 | 547 |
| Reserva para contingencias | 2 270 | − 647 | 1 623 |
| **Total** | **17 044** | **0** | **17 044** |
| Presupuesto máximo | 18 000 | | 18 000 |
| Margen | 956 | | 956 (5,3 %) |
