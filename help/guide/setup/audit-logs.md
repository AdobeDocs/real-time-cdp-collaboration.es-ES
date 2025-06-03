---
title: Registros de auditoría
description: Obtenga información sobre cómo utilizar la funcionalidad Registros de auditoría en Real-Time CDP Collaboration para rastrear actividades y cambios de usuarios.
audience: admin
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 1%

---

# Registros de auditoría

{{limited-availability-release-note}}

Para aumentar la transparencia y la visibilidad de las actividades realizadas en el sistema, puede auditar la actividad del usuario para varios servicios y funcionalidades en forma de registros de auditoría en Adobe Real-Time Customer Data Platform (CDP). Estos registros forman una pista de auditoría que puede ayudar a solucionar problemas en Real-Time CDP Collaboration y ayudar a su empresa a cumplir de forma eficaz con las políticas de administración de datos corporativos y los requisitos regulatorios.

En un sentido básico, un registro de auditoría indica a *quién* realizó *qué* acción y *cuándo*. Cada acción registrada contiene metadatos que indican el tipo de acción, la fecha y la hora, el ID de correo electrónico del usuario que realizó la acción y los atributos adicionales relevantes de ese tipo de acción.

Utilice la funcionalidad de registros de auditoría de Real-Time CDP Collaboration para rastrear las actividades y los cambios de los usuarios dentro de la plataforma. Esta función está integrada con el servicio de auditoría de Adobe Experience Platform y la interfaz de usuario de esta funcionalidad reside en Experience Platform.

![Pantalla de información general de alto nivel sobre la funcionalidad de registros de auditoría](/help/assets/setup/audit-logs/audit-logs-overview.png)

Para obtener información más completa acerca de los registros de auditoría, visite la [Documentación de registros de auditoría de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}.

## Acceder a registros de auditoría

Puede acceder a los registros de auditoría de dos formas, tal como se describe en las secciones siguientes. Ambas opciones muestran una lista de registros de auditoría que capturan varias actividades realizadas dentro de la interfaz de usuario de Real-Time CDP Collaboration

### Acceso a registros de auditoría desde la interfaz de usuario de Real-Time CDP Collaboration

1. Vaya a la pestaña **[!UICONTROL Mi actividad]** de la interfaz de usuario de Real-Time CDP Collaboration.
2. Seleccione el vínculo Experience Platform en el texto de la interfaz de usuario en la parte superior de la página.

![Acceder a registros de auditoría desde la interfaz de usuario de Real-Time CDP Collaboration](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Acceder a los registros de auditoría directamente en la interfaz de usuario de Experience Platform

1. Vaya a la interfaz de usuario de Adobe Experience Platform y seleccione la sección **[!UICONTROL Auditorías]** en el menú de la izquierda. Póngase en contacto con los administradores del sistema de su organización para obtener los permisos necesarios si no puede ver los registros de auditoría.

![Acceder a registros de auditoría desde la interfaz de usuario de Experience Platform](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## Ver y utilizar registros de auditoría

Para ver los registros de auditoría:

1. Vaya a la sección **[!UICONTROL Auditorías]** en la interfaz de usuario de Adobe Experience Platform.
2. Utilice los filtros para reducir los registros en función de sus criterios.
3. Seleccione una entrada de registro para ver información detallada, incluida la marca de tiempo, el ID de solicitud, los detalles del recurso y el estado de la acción.

![Registro detallado de auditoría](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Actividades capturadas

Los registros de auditoría capturan información detallada sobre las actividades del usuario, incluidas:

* **Id. de usuario**: El identificador del usuario que realizó la acción.
* **Acción**: Tipo de acción realizada (por ejemplo, crear, actualizar, eliminar).
* **Recurso**: El recurso que se modificó o creó.
* **Marca de tiempo**: Hora a la que se realizó la acción.

Estos registros crean una pista completa de todas las actividades dentro de la instancia de Real-Time CDP Collaboration, lo que resulta útil para la gobernanza de datos y el cumplimiento de las normativas. Más información sobre [administrar registros de auditoría en la interfaz de usuario](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filtrar registros de auditoría

La interfaz de usuario de registros de auditoría proporciona varios filtros para ayudarle a buscar registros específicos:

* **Categoría**: Hace referencia al tipo de recurso (por ejemplo: instancia de colaboración, conexión, proyecto).
* **Acción**: tipo de acción realizada (por ejemplo: crear, eliminar, actualizar).
* **ID de solicitud**: Un identificador único para la solicitud.
* **Correo electrónico del usuario**: La dirección de correo electrónico del usuario que realizó la acción.
* **Estado**: El estado de la acción (por ejemplo: permitido, denegado).
* **Intervalo de fechas**: El intervalo de fechas para el cual desea ver los registros.

Más información sobre [filtrado de registros de auditoría](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

### Ejemplo de uso

Los registros de auditoría se generan y se muestran en la interfaz de usuario de auditorías de Experience Platform cuando se realizan acciones en la interfaz de usuario de Real-Time CDP Collaboration, como administrar audiencias, ampliar invitaciones a conexiones, crear proyectos, etc. Por ejemplo, las operaciones para crear o actualizar partes de un proyecto se capturan como se muestra a continuación:

![Ejemplo de registros de auditoría generados al crear y actualizar partes de un proyecto.](/help/assets/setup/audit-logs/create-project-audits.png)

## Ventajas

Comprenda algunas de las ventajas de utilizar los registros de auditoría:

* **Control de datos**: Use registros de auditoría para asegurarse de que todas las actividades dentro de la plataforma se rastrean y auditan.
* **Cumplimiento normativo**: La característica proporciona un seguimiento de las actividades de los usuarios para cumplir con los requisitos reglamentarios.
* **Solución de problemas**: los registros de auditoría ayudan a identificar y resolver problemas al proporcionar registros detallados de las acciones del usuario.

## Referencia de categorías y acciones

La siguiente tabla proporciona una referencia de todas las categorías y acciones de Real-Time CDP Collaboration.

![Categorías disponibles resaltadas en los registros de auditoría de Real-Time CDP Collaboration.](/help/assets/setup/audit-logs/available-categories.png)

| Categoría | Acciones | Descripción |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Instancia de Collaboration]** | crear, actualizar, eliminar | Administrar cuentas de organización, incluida la creación, actualización y eliminación de organizaciones. Más información sobre [configuración de organizaciones](/help/guide/setup/onboard-organization.md). |
| **[!UICONTROL Invitación a la conexión de Collaboration]** | crear, actualizar, eliminar, aprobar, rechazar | Administre las invitaciones a conexiones, lo que incluye la creación, actualización, eliminación, aprobación y rechazo de invitaciones. Más información sobre [invitaciones de conexión](/help/guide/connect/establishing-connections.md). |
| **[!UICONTROL Conexión de Collaboration]** | crear, actualizar, eliminar, aprobar, rechazar, solicitar aprobación | Administrar conexiones de colaboración, incluida la creación, actualización, eliminación, aprobación, rechazo y solicitud de aprobación para conexiones. |
| **[!UICONTROL Conexión de datos de Collaboration]** | crear, actualizar, eliminar | Administrar conexiones de datos para colaborar en la importación y administración de audiencias, incluida la creación, actualización y eliminación de conexiones de datos. Más información sobre [administrar conexiones de datos](/help/guide/setup/manage-data-connection.md). |
| **[!UICONTROL Entidad de datos de Collaboration]** | crear, actualizar, eliminar | Administrar entidades de datos para la colaboración, incluida la creación, actualización y eliminación de entidades de datos. Las entidades de datos en este contexto hacen referencia a audiencias. Más información sobre [importación y administración de audiencias](/help/guide/setup/onboard-audiences.md). |
| **[!UICONTROL Proyecto Collaboration]** | crear, actualizar, eliminar | Administrar proyectos en colaboración, incluida la creación, actualización y eliminación de proyectos. Más información sobre [administrar proyectos](/help/guide/collaborate/manage-projects.md). |
| **[!UICONTROL Módulo Collaboration]** | crear, actualizar, eliminar | Administre diferentes módulos dentro de los proyectos de colaboración, incluida la creación, actualización y eliminación de varios módulos en la interfaz de usuario. Por ejemplo, la capacidad de [compartir audiencias](/help/guide/collaborate/share.md). |

{style="table-layout:auto"}

Al aprovechar la funcionalidad de registros de auditoría, puede mantener un registro claro y detallado de todas las actividades dentro de la instancia de Real-Time CDP Collaboration, lo que garantiza la transparencia y la rendición de cuentas.
