---
title: Manage roles through Permissions
description: Understand all available role resources that provide access to different components within the Real-Time CDP Collaboration UI.
audience: admin
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 59cf5bf2-421b-4ebc-beab-30eafb098649
TQID: https://experienceleague.adobe.com/dB7nEQtEGG8PvCSE7eDDelH-ml2EhKOQ8ovvGXG1Ejg
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 623
ht-degree: 3%

---

# Administrar funciones {#manage-roles}

{{limited-availability-release-note}}

To manage user access to different components of the Adobe Real-Time CDP Collaboration UI, an [administrator](./manage-user-access.md#system-admin-gain-access) can define and assign roles. Roles define the access that an administrator or user has to [resources](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions){target="_blank"} in your organization. This guide will provide information on the standard roles provided in Real-Time CDP Collaboration, as well as the individual permissions you that can be assign to custom roles.

To begin managing roles, an administrator will need access to the Experience Platform product. For information on gaining administrative access, or on gaining access to Experience Platform, read the [manage user access](./manage-user-access.md#manage-user-access-through-permissions) guide.

## Standard roles {#standard-roles}

There are two standard roles provided to you that fill two common access control use cases. These are &quot;read only&quot; roles meaning they cannot be customized.

| Nombre de la función | Role description | Permisos |
| --- | --- | --- |
| Collaboration Managers | This is all-access permission, containing all 15 permissions. This allows the user to read, create, and edit all data. It also provides access to the **[!UICONTROL Prod]** sandbox in Experience Platform, allowing you to import audiences into Real-Time CDP Collaboration. | All from the table below. |
| Collaboration Viewers | This is a read-only access permission. A user can read and discover data, activities, connections, and more. It also provides access to the **[!UICONTROL Prod]** sandbox in Experience Platform, allowing you to import audiences into Real-Time CDP Collaboration. | All read permissions from the table below. |

{style="table-layout:auto"}

## Create specific access roles {#specific-access-roles}

Es probable que desee crear funciones adicionales para proporcionar distintos niveles de acceso a distintos usuarios. Al crear funciones, puede administrar diferentes niveles de acceso seleccionando permisos específicos en el recurso **[!UICONTROL Colaboraciones]**. Para aprender a crear y administrar roles, consulte la guía [roles](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/roles#create-new-role){target="_blank"}.

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
| Leer datos de audiencias | Read and discover audiences. |
| Manage Measurement Data | Onboard, update, and delete measurement data. |
| Read Measurement Data | Read measurement data. |
| Manage Projects | View, create, update, and delete projects for any of the discover, activate, and measurement activities. |
| Read Projects | View projects for any of the discover, activate, and measurement activities. |
| Read User Activities | Read user activities. |
| Export User Activities | Export user activities. |
| Read Collaboration Credit Monitoring | Credit monitoring at the organization and instance level. |

{style="table-layout:auto"}

## Próximos pasos

After creating roles that define access to Collaboration, you&#39;ll need to [assign the roles](./manage-user-access.md#assign-a-role) to administrators and users. Refer to the [manage permissions for a role](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) guide for a complete overview of managing roles.
