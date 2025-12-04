---
title: Administrar funciones mediante Permisos
description: Comprenda todos los recursos de funciones disponibles que proporcionan acceso a diferentes componentes dentro de la interfaz de usuario de Real-Time CDP Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 59cf5bf2-421b-4ebc-beab-30eafb098649
source-git-commit: 1f825bb4a81dbf65c43ddadcfd444923a37a906e
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 1%

---

# Administrar funciones {#manage-roles}

{{limited-availability-release-note}}

Para administrar el acceso de usuarios a diferentes componentes de la interfaz de usuario de Adobe Real-Time CDP Collaboration, un [administrador](./manage-user-access.md#system-admin-gain-access) puede definir y asignar funciones. Las funciones definen el acceso que un administrador o usuario tiene a [recursos](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/home#permissions){target="_blank"} en su organización. Esta guía proporciona información sobre las funciones estándar que se proporcionan en Real-Time CDP Collaboration, así como los permisos individuales que se pueden asignar a las funciones personalizadas.

Para empezar a administrar funciones, un administrador deberá tener acceso al producto Experience Platform. Para obtener información sobre cómo obtener acceso administrativo o sobre cómo obtener acceso a Experience Platform, lea la guía [administrar el acceso de usuario](./manage-user-access.md#manage-user-access-through-permissions).

## Funciones estándar {#standard-roles}

Se le han proporcionado dos funciones estándar que rellenan dos casos de uso comunes de control de acceso. Son funciones de &quot;solo lectura&quot;, lo que significa que no se pueden personalizar.

| Nombre de la función | Descripción de función | Permisos |
| --- | --- | --- |
| Collaboration Managers | Es un permiso de acceso completo que contiene los 15 permisos. Esto permite al usuario leer, crear y editar todos los datos. También proporciona acceso a la zona protegida **[!UICONTROL Prod]** en Experience Platform, lo que le permite importar audiencias en Real-Time CDP Collaboration. | Todos de la tabla siguiente. |
| Visores de Collaboration | Es un permiso de acceso de solo lectura. Un usuario puede leer y descubrir datos, actividades, conexiones y mucho más. También proporciona acceso a la zona protegida **[!UICONTROL Prod]** en Experience Platform, lo que le permite importar audiencias en Real-Time CDP Collaboration. | Todos los permisos de lectura de la tabla siguiente. |

{style="table-layout:auto"}

## Crear funciones de acceso específicas {#specific-access-roles}

Es probable que desee crear funciones adicionales para proporcionar distintos niveles de acceso a distintos usuarios. Al crear funciones, puede administrar diferentes niveles de acceso seleccionando permisos específicos en el recurso **[!UICONTROL Colaboraciones]**. Para aprender a crear y administrar roles, consulte la guía [roles](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/roles#create-new-role){target="_blank"}.

>[!NOTE]
> Para obtener acceso a Collaboration, un usuario debe tener acceso a la zona protegida **[!UICONTROL Prod]** en Adobe Experience Platform. Para que un usuario tenga acceso a esta zona protegida, debe asignársele un rol que contenga el permiso **[!UICONTROL Prod]** en el recurso **[!UICONTROL Sandboxes]**.

A continuación, se muestra una lista de los permisos disponibles en el recurso de colaboraciones:

| Permiso de alto nivel | Descripción |
| --- | --- |
| Administrar instancias de Collaboration | Ver, crear, actualizar y eliminar las instancias de colaboración de una organización. Descubra las instancias de colaboración de otras organizaciones. |
| Leer instancias de Collaboration | Lea las instancias de colaboración de una organización y descubra las instancias de colaboración de otras organizaciones. |
| Administrar invitaciones de conexión | Vea, cree y elimine invitaciones a conexiones iniciadas por su organización. Aceptar y rechazar la invitación de conexión iniciada por otras organizaciones. |
| Leer invitaciones de conexión | Ver invitaciones de conexión. |
| Administrar conexiones de Collaboration | Un colaborador puede ver, crear y actualizar la configuración, así como enviar y eliminar conexiones. |
| Leer conexiones de Collaboration | Ver conexiones. |
| Administrar datos de audiencia | Incorporar y descubrir audiencias. Actualice las audiencias públicas, privadas y personalizadas y administre la configuración de metadatos del inventario de audiencias. |
| Leer datos de audiencias | Leer y descubrir audiencias. |
| Administrar datos de medición | Incorpore, actualice y elimine datos de medición. |
| Leer datos de medición | Leer datos de medición. |
| Administrar proyectos | Ver, crear, actualizar y eliminar proyectos para cualquiera de las actividades de detección, activación y medición. |
| Leer proyectos | Ver proyectos para cualquiera de las actividades de detección, activación y medición. |
| Leer actividades de usuario | Actividades de usuario de lectura. |
| Exportar actividades de usuario | Exportar actividades de usuario. |
| Leer supervisión de crédito de Collaboration | Supervisión del crédito a nivel de organización e instancia. |

{style="table-layout:auto"}

## Próximos pasos

Después de crear las funciones que definen el acceso a Collaboration, [debe asignar las funciones](./manage-user-access.md#assign-a-role) a los administradores y a los usuarios. Consulte la guía [administrar permisos para una función](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/permissions) para obtener una descripción general completa de la administración de funciones.
