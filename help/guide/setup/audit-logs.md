---
title: Registros de auditoría
description: Obtenga información sobre cómo utilizar la funcionalidad Registros de auditoría en Real-Time CDP Collaboration para rastrear actividades y cambios de usuarios.
audience: admin
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 1%

---

# Registros de auditoría

{{limited-availability-release-note}}

Para aumentar la transparencia y la visibilidad de las actividades realizadas en el sistema, puede auditar la actividad del usuario para varios servicios y funcionalidades en forma de registros de auditoría en Adobe Experience Platform. Estos registros forman una pista de auditoría que puede ayudar a solucionar problemas en Adobe Real-Time CDP Collaboration y ayudar a su empresa a cumplir de forma eficaz con las políticas de administración de datos corporativos y los requisitos regulatorios.

En un sentido básico, un registro de auditoría indica a *quién* realizó *qué* acción y *cuándo*. Cada acción registrada contiene metadatos que indican el tipo de acción, la fecha y la hora, el ID de correo electrónico del usuario que realizó la acción y los atributos adicionales relevantes de ese tipo de acción.

Utilice la funcionalidad de registros de auditoría de Collaboration para rastrear las actividades y los cambios de los usuarios dentro de la plataforma. Esta función está integrada con el servicio de auditoría de Experience Platform y la interfaz de usuario de esta funcionalidad reside en Experience Platform.

![Pantalla de información general de alto nivel sobre la funcionalidad de registros de auditoría.](/help/assets/setup/audit-logs/audit-logs-overview.png)

Para obtener información más completa acerca de los registros de auditoría, visite la [documentación sobre los registros de auditoría de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}.

## Acceder a registros de auditoría

Puede acceder a los registros de auditoría de dos formas, tal como se describe en las secciones siguientes. Ambas opciones muestran una lista de registros de auditoría que capturan varias actividades realizadas en Collaboration.

### Acceso a registros de auditoría desde la interfaz de usuario de Collaboration

1. Vaya a la pestaña **[!UICONTROL Mi actividad]** en el espacio de trabajo **[!UICONTROL Configuración]** de Collaboration.
2. Seleccione el vínculo Experience Platform en el texto de la parte superior de la página.

![Acceder a los registros de auditoría desde la ficha Mi actividad en Collaboration.](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Acceder a los registros de auditoría directamente en la interfaz de usuario de Experience Platform

1. Vaya a [Experience Platform](https://platform.adobe.com/) y seleccione la sección **[!UICONTROL Auditorías]** en el menú de la izquierda. Póngase en contacto con los administradores del sistema de su organización para obtener los permisos necesarios si no puede ver los registros de auditoría.

![Acceder a los registros de auditoría desde Experience Platform.](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## Ver y utilizar registros de auditoría

Para ver los registros de auditoría:

1. Vaya a la sección **[!UICONTROL Auditorías]** en Experience Platform.
2. Use los [filtros](#filter-audit-logs) para reducir los registros según sus criterios.
3. Seleccione una entrada de registro para ver información detallada, incluida la marca de tiempo, el ID de solicitud, los detalles del recurso y el estado de la acción.

![Registro detallado de auditoría](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Actividades capturadas

Los registros de auditoría capturan información detallada sobre las actividades del usuario, incluidas:

* **Marca de tiempo**: La fecha y hora exactas de la acción realizada en formato de mes/día/año hora:minute a.m./p.m.
* **Nombre del recurso**: Nombre del recurso en el que se realizó la acción.
* **Categoría**: Tipo de recurso en el que se realizó la acción.
* **Acción**: la acción específica realizada, como crear o eliminar.
* **Usuario**: La dirección de correo electrónico del usuario que realizó la acción.

Estos registros crean una pista completa de todas las actividades dentro de la instancia de Collaboration, lo que resulta útil para la gobernanza de datos y el cumplimiento de las normativas. Más información sobre [administrar registros de auditoría en la interfaz de usuario](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filtrar registros de auditoría {#filter-audit-logs}

La interfaz de usuario de registros de auditoría proporciona varios filtros para ayudarle a buscar registros específicos:

* **Categoría**: Tipo de recurso en el que se realizó la acción, como Instancia de Collaboration o Invitación a la conexión de Collaboration.
* **Acción**: tipo de acción realizada. Las acciones disponibles dependen de la categoría seleccionada. Por ejemplo, las acciones para la instancia de Collaboration incluyen crear, actualizar y eliminar.
* **ID de solicitud**: Un identificador único para la solicitud.
* **Usuario**: La dirección de correo electrónico del usuario que realizó la acción.
* **Estado**: El estado de la acción, como permitir o denegar.
* **Intervalo de fechas**: El intervalo de fechas para el cual desea ver los registros.

Más información sobre [filtrado de registros de auditoría](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

## Ventajas

Los registros de auditoría proporcionan varios beneficios para las organizaciones que utilizan Collaboration:

* **Control de datos**: Use registros de auditoría para asegurarse de que todas las actividades dentro de la plataforma se rastrean y auditan.
* **Cumplimiento normativo**: La característica proporciona un seguimiento de las actividades de los usuarios para cumplir con los requisitos reglamentarios.
* **Solución de problemas**: los registros de auditoría ayudan a identificar y resolver problemas al proporcionar registros detallados de las acciones del usuario.

## Referencia de categorías y acciones

La siguiente tabla proporciona una referencia de todas las categorías y acciones de Real-Time CDP Collaboration.

![Categorías disponibles resaltadas en los registros de auditoría de Real-Time CDP Collaboration.](/help/assets/setup/audit-logs/available-categories.png)

| Categoría | Acciones | Descripción |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Instancia de Collaboration]** | crear, actualizar, eliminar | Administrar cuentas, incluida la creación, actualización y eliminación de cuentas. Para obtener más información, lee la guía [configuración de tus cuentas](/help/guide/setup/onboard-account.md). |
| **[!UICONTROL Invitación a la conexión de Collaboration]** | crear, actualizar, eliminar, aprobar, rechazar | Administre las invitaciones a conexiones, lo que incluye la creación, actualización, eliminación, aprobación y rechazo de invitaciones. Para obtener más información, lea la guía [establecimiento de conexiones](/help/guide/connect/establishing-connections.md). |
| **[!UICONTROL Conexión de Collaboration]** | crear, actualizar, eliminar, aprobar, rechazar, solicitar aprobación | Administrar conexiones, incluida la creación, actualización, eliminación, aprobación, rechazo y solicitud de aprobación para conexiones. |
| **[!UICONTROL Conexión de datos de Collaboration]** | crear, actualizar, eliminar | Administre las conexiones de datos desde donde obtiene y administre audiencias, incluida la creación, actualización y eliminación de conexiones de datos. Para obtener más información, lea la guía [administración de conexiones de datos](/help/guide/setup/manage-data-connection.md). |
| **[!UICONTROL Entidad de datos de Collaboration]** | crear, actualizar, eliminar | Administrar entidades de datos para Collaboration, incluida la creación, actualización y eliminación de entidades de datos. Las entidades de datos en este contexto hacen referencia a audiencias. Para obtener más información, lea la guía [obtención y administración de audiencias](/help/guide/setup/onboard-audiences.md). |
| **[!UICONTROL Proyecto Collaboration]** | crear, actualizar, eliminar | Administrar proyectos en Collaboration, incluida la creación, actualización y eliminación de proyectos. Para obtener más información, lea la guía [administrar proyectos](/help/guide/collaborate/manage-projects.md). |
| **[!UICONTROL Módulo Collaboration]** | crear, actualizar, eliminar | Administre diferentes módulos dentro de los proyectos, incluida la creación, actualización y eliminación de varios módulos en la interfaz de usuario. Por ejemplo, la capacidad de [activar audiencias](/help/guide/collaborate/activate.md). |

{style="table-layout:auto"}

Al aprovechar la funcionalidad de registros de auditoría, puede mantener un registro claro y detallado de todas las actividades de Collaboration, lo que garantiza la transparencia y la rendición de cuentas.
