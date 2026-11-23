# 2. Revisar el Enunciado del trabajo — GP y LT

**Proyecto:** TurnoSalud · **Grupo 6**
**Responsables:** Zaith Manangón (GP) y Matías Lugmaña (LT) · **Apoyo:** Alexander Villacres (AN/DIS) y Andrea Raura (RP)
**Tareas de la norma:** GP.1.1 Revisar el Enunciado del trabajo · GP.1.2 Definir con el cliente las instrucciones de entrega
**Registro:** [Acta 02](../actas/ACTA-02_2026-11-18_revision-enunciado-y-plan.md) (revisión) · [Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md) (instrucciones de entrega acordadas con el CL)
**Versión:** 1.2 · **Estado:** Revisado · Cambio de alcance aprobado: [SC-01](../05-solicitudes-cambio/SC-01_lista-de-espera.md) ([Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md))

---

## 2.1 Lo que dice el enunciado

**Enunciado unificado del proyecto :**
Una clínica privada requiere el desarrollo de **TurnoSalud**, una aplicación web de agendamiento de turnos médicos que permita organizar, agilizar y centralizar la atención de sus pacientes sin depender de registros manuales. Para llevarlo a cabo, contrata a una entidad muy pequeña (VSE) de Sangolquí integrada por 6 puestos de trabajo (1 gestora de proyecto, 1 líder técnico, 1 analista-diseñadora, 2 programadores y 1 responsable de pruebas), la cual dedicará su capacidad exclusivamente a este único proyecto durante el periodo. Se espera que el equipo entregue una solución web funcional, segura en el manejo de datos y fácil de usar para pacientes, recepción, médicos y administración, cumpliendo un plazo máximo de **12 semanas** y un presupuesto cerrado de **USD 18 000**, bajo la premisa de que el software es de gestión operativa y no es crítico para la seguridad humana.

**Datos base recibidos en el enunciado del deber:**
- **VSE desarrolladora:** Equipo de Sangolquí de 6 personas (1 gestora, 1 líder técnico, 1 analista-diseñadora, 2 programadores y 1 responsable de pruebas).
- **Cliente y necesidad:** Clínica privada que necesita una aplicación web de agendamiento de turnos.
- **Plazo y presupuesto:** 12 semanas de duración y USD 18 000 de presupuesto.
- **Contexto del proyecto:** Único proyecto ejecutado por la VSE en este periodo; el producto no es crítico para la seguridad.

## 2.2 Observaciones de la revisión

| Lo que falta o no está claro | Cómo lo resolvemos |
|------------------------------|--------------------|
| No detalla las funcionalidades específicas que debe tener la aplicación (alcance funcional). | Proponemos en la sección 2.5 las funciones incluidas en esta versión y las excluidas con su justificación *(supuesto)*. |
| No identifica los tipos de usuarios que interactuarán con el sistema ni sus permisos. | Definimos cuatro perfiles de usuario en la sección 2.4: paciente, recepcionista, médico y administrador de la clínica *(supuesto)*. |
| No especifica la lista de entregables, el calendario de entregas ni el medio de recepción. | Elaboramos en la sección 2.6 la propuesta de entregables e instrucciones de entrega (GP.1.2) alineada con las 12 semanas *(supuesto)*. |
| No establece criterios de aceptación para validar el producto final. | Formulamos en la sección 2.8 criterios medibles y su método de comprobación junto con la Responsable de Pruebas (RP) *(supuesto)*. |
| No menciona restricciones técnicas (arquitectura, navegadores soportados, alojamiento o protección de datos). | El Líder Técnico (LT) define en la sección 2.9 los supuestos técnicos de arquitectura web, despliegue y resguardo de datos *(supuesto)*. |
| No designa a un representante de la clínica para resolver dudas y aprobar entregables. | Asumimos al docente de la asignatura como Cliente (CL) para las validaciones y entregas formales *(supuesto)*. |

## 2.3 Objetivo del proyecto

Desarrollar y poner en marcha la aplicación web **TurnoSalud** para una clínica privada, permitiendo gestionar en línea la reserva, reprogramación, cancelación y control de turnos médicos por especialidad en un plazo de 12 semanas y dentro del presupuesto de USD 18 000 *(supuesto)*.

## 2.4 Usuarios del sistema

| Usuario | Qué necesita hacer en la aplicación |
|---------|-------------------------------------|
| **Paciente** *(supuesto)* | Registrarse e iniciar sesión, consultar especialidades y horarios disponibles, reservar, reprogramar o cancelar turnos y recibir confirmaciones por correo electrónico. |
| **Recepcionista** *(supuesto)* | Registrar pacientes que acuden o llaman a la clínica, agendar o modificar turnos en su nombre, registrar la llegada del paciente y consultar la agenda del día. |
| **Médico / Profesional de salud** *(supuesto)* | Visualizar su agenda diaria y semanal de pacientes citados, definir sus bloques de atención o ausencias y actualizar el estado del turno (atendido o no asistió). |
| **Administrador de la clínica** *(supuesto)* | Gestionar el catálogo de especialidades, médicos, consultorios y horarios base, administrar cuentas de usuario y consultar reportes básicos de turnos. |

## 2.5 Alcance

| Incluido | No incluido |
|----------|-------------|
| Módulo de registro, inicio de sesión y control de acceso por roles (paciente, recepcionista, médico y administrador) *(supuesto)*. | Historia clínica electrónica (HCE) y emisión de recetas médicas, porque requieren normativa sanitaria adicional y superan el plazo de 12 semanas *(supuesto)*. |
| Gestión de catálogo de especialidades, médicos, consultorios y parametrización de horarios de atención *(supuesto)*. | Pasarela de pagos en línea y facturación electrónica con el SRI; el cobro de consultas se mantiene en la recepción de la clínica en esta versión *(supuesto)*. |
| Agendamiento, reprogramación y cancelación de turnos con validación automática para evitar cruces de horario *(supuesto)*. | Aplicaciones móviles nativas (Android / iOS); se cubre el acceso móvil mediante una interfaz web responsiva *(supuesto)*. |
| Envío automático de notificaciones y recordatorios por correo electrónico al confirmar, cambiar o cancelar un turno *(supuesto)*. | Notificaciones por SMS o API comercial de WhatsApp, para evitar costos recurrentes no contemplados en el presupuesto *(supuesto)*. |
| Panel de recepción y vista administrativa con resumen de citas programadas, atendidas y canceladas *(supuesto)*. | Módulo de telemedicina o videoconsultas integradas, ya que la clínica requiere gestionar la atención presencial *(supuesto)*. |
| **(v1.2, SC-01)** Lista de espera por especialidad y fecha, con aviso por correo cuando se libera un turno. | |

La solicitud de recordatorios por WhatsApp ([SC-02](../05-solicitudes-cambio/SC-02_notificaciones-whatsapp.md)) fue rechazada: la exclusión de SMS y WhatsApp se mantiene.

## 2.6 Entregables e instrucciones de entrega (GP.1.2)

| Entregable | Qué contiene | Semana | Cómo se entrega | Quién lo aprueba |
|------------|--------------|--------|-----------------|------------------|
| **E1. Plan del proyecto** *(supuesto)* | Alcance, descomposición de tareas, estimación PERT, calendario de 12 semanas, presupuesto, riesgos e instrucciones de entrega. | 2 | Documento Markdown en el repositorio GitHub (`03-plan-proyecto/`) y revisión en reunión con el cliente. | Cliente (CL) |
| **E2. Especificación de requisitos** *(supuesto)* | Requisitos funcionales y no funcionales, historias de usuario/casos de uso y prototipos de interfaz verificados y validados (IS.2). | 3 | Documento y prototipos en el repositorio GitHub con acta de validación del cliente. | Cliente (CL) |
| **E3. Arquitectura y diseño detallado** *(supuesto)* | Diagrama de arquitectura web, modelo de base de datos, diseño de componentes y matriz de trazabilidad frente a requisitos (IS.3). | 5 | Documentación técnica y diagramas versionados en el repositorio del proyecto. | Líder Técnico (LT) y Gestor del Proyecto (GP) |
| **E4. Versión beta e informe de pruebas** *(supuesto)* | Componentes integrados, pruebas unitarias y de integración ejecutadas, casos de prueba e informe de resultados (IS.4, IS.5). | 10 | Despliegue en entorno de pruebas (staging) accesible por navegador y reporte de pruebas en GitHub. | Responsable de Pruebas (RP), LT y validación del CL |
| **E5. Configuración de software y cierre** *(supuesto)* | Código fuente final, base de datos, sistema desplegado, manual de usuario, guía de mantenimiento y acta de aceptación (IS.6, GP.4). | 12 | Versión etiquetada (`v1.0.0`) en GitHub, despliegue final y firma del Acta de aceptación. | Cliente (CL) |

## 2.7 Plazo y presupuesto

- **Plazo:** 12 semanas (equivalentes a 3 meses calendario), organizadas desde la planificación y análisis (semanas 1 a 3), diseño y construcción (semanas 4 a 9), hasta integración, pruebas y entrega final (semanas 10 a 12) *(supuesto)*.
- **Presupuesto:** USD 18 000 como límite máximo establecido por el cliente, destinado a cubrir el esfuerzo del equipo de la VSE, servicios de infraestructura/herramientas y reserva de contingencia *(supuesto)*.
- **Seguimiento con el cliente:** Reuniones quincenales de seguimiento y validación de entregables con el Cliente (CL), dejando constancia en actas de reunión y gestionando cualquier ajuste mediante solicitudes de cambio formales *(supuesto)*.

## 2.8 Criterios de aceptación

| Criterio | Cómo se comprueba |
|----------|-------------------|
| Cumplimiento del 100 % de las funcionalidades del alcance incluido (registro, horarios, reserva, reprogramación, cancelación y recepción) *(supuesto)*. | Ejecución completa de los casos de prueba funcionales diseñados por Andrea (RP), verificando que no existan defectos críticos ni mayores pendientes *(supuesto)*. |
| Ausencia de duplicidad o cruce de horarios para un mismo médico y consultorio *(supuesto)*. | Pruebas funcionales y de concurrencia intentando registrar dos citas en el mismo bloque horario desde sesiones distintas *(supuesto)*. |
| Facilidad de uso en el flujo de agendamiento (reserva completada en máximo 4 pasos y menos de 2 minutos para un usuario registrado) *(supuesto)*. | Prueba de validación de usabilidad con el Cliente (CL) sobre los prototipos (IS.2.4) y sobre el sistema integrado (IS.5) *(supuesto)*. |
| Visualización adaptable (responsiva) y operación correcta en navegadores modernos (Chrome, Edge, Firefox y Safari) en escritorio y móvil *(supuesto)*. | Pruebas de interfaz en distintas resoluciones de pantalla ejecutadas por RP y revisadas por el Líder Técnico (LT) *(supuesto)*. |
| Tiempo de carga de disponibilidad de horarios y confirmación de turno inferior a 3 segundos en condiciones normales de operación *(supuesto)*. | Pruebas de respuesta en el entorno de preproducción previas a la entrega final *(supuesto)*. |
| Entrega completa de la configuración de software (código fuente, manual de usuario y guía de mantenimiento) *(supuesto)*. | Lista de verificación de entrega (IS.6) revisada por GP y LT, y firma del Acta de aceptación por el Cliente (CL) (GP.4) *(supuesto)*. |

## 2.9 Supuestos técnicos

Propuestos por Matías Lugmaña (LT). Quedan como supuestos hasta que el cliente los confirme.

| Tema | Supuesto |
|------|----------|
| **Arquitectura** | Aplicación web cliente-servidor: frontend en Next.js, backend con una API REST en NestJS y base de datos relacional PostgreSQL *(supuesto)*. |
| **Navegadores y dispositivos** | Últimas dos versiones de Chrome, Edge, Firefox y Safari, en escritorio y móvil, con interfaz responsiva; no se instala nada en los equipos de la clínica *(supuesto)*. |
| **Alojamiento** | Un servidor en la nube para pruebas (staging) y otro para producción. Después del primer mes de operación, la clínica contrata el alojamiento a su nombre *(supuesto)*. |
| **Correo electrónico** | Las confirmaciones y los recordatorios se envían mediante un servicio de correo transaccional SMTP con SPF y DKIM configurados *(supuesto)*. |
| **Datos que se guardan** | Solo datos de identificación y contacto del paciente y datos del turno; no se guarda información clínica, porque la historia clínica está fuera del alcance *(supuesto)*. |
| **Protección de datos** | HTTPS en todo el sistema, contraseñas guardadas con hash, acceso según el rol del usuario y respaldos cifrados, conforme a la Ley Orgánica de Protección de Datos Personales del Ecuador *(supuesto)*. |
| **Zona horaria e idioma** | Horarios en la zona horaria de Ecuador continental (UTC-5) e interfaz en español *(supuesto)*. |

**Restricciones:**

- **Plazo máximo:** El proyecto debe completarse y entregarse en 12 semanas.
- **Presupuesto tope:** El costo total del proyecto no puede exceder los USD 18 000.
- **Equipo y dedicación:** La VSE dispone de un único equipo de 6 puestos (cubiertos por los 4 integrantes del Grupo 6) y ejecuta solo este proyecto en el periodo.
- **Naturaleza del producto y norma aplicable:** El software no es crítico para la seguridad, pero el proceso debe ajustarse a los requisitos y productos de trabajo del Perfil Básico de la ISO/IEC 29110-5-1-2, protegiendo además la confidencialidad de los datos de los pacientes *(supuesto)*.

**Productos de trabajo:**
- **Enunciado del trabajo [revisado]** (salida de la tarea GP.1.1, elaborado por GP y LT).
- **Plan del proyecto: instrucciones de entrega** (salida de la tarea GP.1.2, definida en la sección 2.6 y acordada con el CL en el [Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md)).
- **Registro de reunión** ([Acta 02](../actas/ACTA-02_2026-11-18_revision-enunciado-y-plan.md), donde consta la revisión y los vacíos detectados).
