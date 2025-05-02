# Planning_Budgeting

## 📐 High-Level Design Document
A metaphor system architecture diagram with clear modular components (frontend, backend, database, third-party services).
A text explaining the architecture.

### Architecture Diagram

![img.png](img.png)

## 🗂️ Agile Product Backlog
A prioritized list of epics and user stories, organized using user story mapping.
Use Story Points.
### Epics

| ID   | Epic           | Historia de Usuario                                                                                     | Criterios de Aceptación                                                | Prioridad |
| ---- | -------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | --------- |
| US01 | Frontend Web   | Como ciudadano quiero iniciar sesión en la plataforma web para acceder a mis solicitudes y su historial | Valida credenciales, muestra errores, redirige tras autenticación      | Alta      |
| US02 | Frontend Web   | Como ciudadano quiero crear, editar y eliminar solicitudes para reportar problemas                      | Campos requeridos, edición solo si pendiente, confirmación al eliminar | Alta      |
| US03 | Frontend Web   | Como ciudadano quiero consultar el estado de mis solicitudes                                            | Lista de solicitudes con estado, detalles expandibles                  | Alta      |
| US04 | Frontend Web   | Como ciudadano quiero ver un historial de solicitudes                                                   | Filtros por estado y fecha, exportación CSV                            | Media     |
| US05 | Frontend Móvil | Como ciudadano quiero iniciar sesión desde móvil                                                        | Adaptado a pantalla móvil, validación igual que en web                 | Alta      |
| US06 | Frontend Móvil | Como ciudadano quiero crear y editar solicitudes desde mi móvil                                         | Campos requeridos, edición posible, interfaz amigable                  | Alta      |
| US07 | Frontend Móvil | Como ciudadano quiero ver el estado de solicitudes desde móvil                                          | Visualización clara del estado y detalles                              | Media     |
| US08 | Frontend Móvil | Como ciudadano quiero ver el historial desde móvil                                                      | Historial paginado, con filtros                                        | Media     |
| US09 | API Gateway    | Como desarrollador quiero enrutar solicitudes del frontend al backend                                   | Rutas RESTful definidas, autenticación y manejo de errores             | Alta      |
| US10 | Backend Lambda | Como sistema quiero validar usuarios con Cognito y generar tokens                                       | Integración con Cognito, validación JWT                                | Alta      |
| US11 | Backend Lambda | Como sistema quiero registrar solicitudes para que sean atendidas                                       | Almacenar con timestamp, ID único, evento a EventBus                   | Alta      |
| US12 | Backend Lambda | Como administrador quiero asignar solicitudes a departamentos                                           | Permite selección de destino, dispara evento                           | Alta      |
| US13 | Backend Lambda | Como sistema quiero consultar solicitudes históricas del usuario                                        | Consulta paginada, filtrado                                            | Media     |
| US14 | Base de Datos  | Como arquitecto de datos quiero definir el modelo de base                                               | Tablas y relaciones definidas                                          | Alta      |
| US15 | Seguridad      | Como desarrollador quiero usar Cognito para la autenticación                                            | User pool configurado, validación y recuperación                       | Alta      |
| US16 | Seguridad      | Como desarrollador quiero asegurar los tokens y usar certificados HTTPS                                 | JWT firmado, HTTPS activo con Cert Manager                             | Alta      |
| US17 | Integración    | Como sistema quiero emitir eventos cuando se registra una solicitud                                     | Formato JSON, servicios suscritos                                      | Alta      |
| US18 | Observabilidad | Como operador quiero monitorear con CloudWatch para detectar fallos                                     | Métricas por endpoint, alarmas en errores                              | Alta      |
| US19 | Deployment     | Como equipo devops quiero desplegar funciones Lambda con IAM y certificados                             | Despliegue funcional y automatizado                                    | Alta      |


## 💰 Development Budget
Estimate the cost of implementation based on team roles (e.g., frontend/backend devs, QA, PM), hourly rates, and effort
(story points or ideal days).
Present the budget in a simple table with assumptions and ranges.

### Budget Table
#### Supuestos para el cálculo
![img_1.png](img_1.png)

#### Cálculo del esfuerzo por rol
![img_2.png](img_2.png)

Los roles con dedicación parcial (0.5) representan recursos compartidos con otros proyectos o consultores contratados
por tiempo limitado.

#### Presupuesto de desarrollo (COP)
![img_3.png](img_3.png)

#### Presupuesto de Servicios Cloud
![img_4.png](img_4.png)
![img_5.png](img_5.png)