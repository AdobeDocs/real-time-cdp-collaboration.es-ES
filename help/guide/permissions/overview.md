---
title: Información general de control de acceso
description: Obtenga información sobre cómo obtener acceso a Adobe Real-Time Customer Data Platform (CDP) Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: af48f5ea-8258-42a6-a39e-f4a4ca5b4a69
source-git-commit: 1f825bb4a81dbf65c43ddadcfd444923a37a906e
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 2%

---

# Información general sobre el control de acceso

{{limited-availability-release-note}}

>[!IMPORTANT]
>
> Si es un usuario final que desea acceder a Adobe Real-Time CDP Collaboration, póngase en contacto con el administrador del sistema o del producto para comprobar el acceso existente. Si no sabe quién es el administrador del sistema, póngase en contacto con su representante de Adobe.

El control de acceso para Adobe Real-Time CDP Collaboration se proporciona a través de Admin Console y los permisos en [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}. En esta guía, aprenderá a darse acceso a sí mismo o a otros miembros de su equipo, según su caso de uso.

## Jerarquía de control de acceso {#hierarchy}

Para configurar el control de acceso a Collaboration, **debe** tener privilegios de administrador de sistemas o productos. Un administrador del sistema no tiene restricciones y se aprovisiona durante el proceso de incorporación. Mientras tanto, un administrador de productos puede proporcionar funciones administrativas para todos los productos a los que se les ha asignado. Un administrador del sistema debe otorgar acceso administrativo y de producto a un administrador de productos.

En estas guías se describe la configuración del acceso para administradores del sistema, administradores de productos y usuarios finales. Consulte la tabla siguiente para comprender la diferencia clave entre las funciones.

| Función | Descripción |
| --- | --- |
| Administrador del sistema | El superusuario de la organización. Pueden realizar todas las tareas administrativas en Admin Console y tienen permisos para delegar funciones administrativas a otros usuarios. |
| Administrador de productos | Administra los productos asignados a ellos y todas las funciones administrativas asociadas, como agregar usuarios a organizaciones, agregar o eliminar usuarios de perfiles de productos y agregar o eliminar otros administradores de productos de un producto. |
| Usuario final | Los usuarios de su organización que utilizan los productos. |

{style="table-layout:auto"}

Para obtener más información sobre las funciones administrativas, visite el [Centro de ayuda de Adobe](https://helpx.adobe.com/enterprise/using/admin-roles.html).

>[!TIP]
>
>El uso de **administradores** en estas guías hará referencia a **administradores de sistemas y productos**.

## Productos adicionales {#products}

Antes de que puedas dar acceso a Collaboration, necesitarás acceso a varios productos, según tu [caso de uso](#use-cases). Las guías de control de acceso pueden funcionar a través de varias interfaces de usuario a medida que avanza, cada una con un propósito específico dentro del proceso de configuración de acceso. Consulte la tabla siguiente para comprender mejor para qué se utilizará cada producto.

| Producto | Usos |
| --- | --- |
| [Admin Console](https://adminconsole.adobe.com/) | Los administradores utilizan esto para asignar a los usuarios acceso de producto o administrador. |
| [Permisos](https://experience.adobe.com/) | Los administradores utilizan esta opción para asignar funciones de administrador o de usuario final. |
| [Experience Platform](https://platform.adobe.com/) | Los administradores y los usuarios finales deben tener acceso al producto de Experience Platform para asignarlos a funciones. |

## Por dónde empezar {#use-cases}

Ahora que tiene una comprensión más profunda de las funciones de usuario y administración, así como de los diferentes productos de Experience Cloud, puede empezar a dar acceso a Collaboration. Existen dos factores principales que influyen en los pasos que debe seguir:

- si asigna acceso de administrador o de usuario final
- si los usuarios ya tienen acceso al producto Experience Platform

Consulte el gráfico siguiente para determinar quién es necesario para configurar los privilegios y dónde comenzar en función del caso de uso del control de acceso. **Asegúrese de seguir el tutorial hasta el final de la guía desde el lugar de inicio.**

>[!TIP]
>
> Un superusuario hace referencia al nivel más alto de acceso que obtiene el administrador del sistema. Un superusuario puede realizar todas las tareas administrativas y la funcionalidad del usuario. Un administrador del sistema no tiene la funcionalidad del producto lista para usar y debe concederse el acceso adecuado, como se muestra en el gráfico siguiente.

| Ejemplo de uso | Función requerida | Por dónde empezar |
| --- | --- | --- |
| Superusuario sin acceso a producto de Experience Platform existente. | Un administrador del sistema. | [Configurar el acceso de administrador de productos](./manage-user-access.md#admin-access) |
| Superusuario para un administrador de sistema de Experience Platform existente **con** acceso a la interfaz de usuario de Experience Platform. | Un administrador del sistema. | [Configurar el acceso a Collaboration](./manage-user-access.md#RTCDP-collab-access) |
| Superusuario para un administrador de sistema de Experience Platform existente **sin** acceso a la interfaz de usuario de Experience Platform. | Un administrador del sistema. | [Configurar el acceso de administrador de productos](./manage-user-access.md#admin-access) |
| Privilegios de administrador de productos y acceso a Collaboration para un nuevo administrador de productos. | Un administrador del sistema. | [Configurar el acceso de administrador de productos](./manage-user-access.md#admin-access) |
| Acceso a Collaboration para un administrador de productos de Experience Platform existente **con** acceso a la interfaz de usuario de Experience Platform. | Un administrador de sistemas o productos. | [Configurar el acceso a Collaboration](./manage-user-access.md#RTCDP-collab-access) |
| Acceso a Collaboration para un administrador de productos de Experience Platform existente **sin** acceso a la interfaz de usuario de Experience Platform. | Un administrador de sistemas o productos. | [Configurar el acceso de los usuarios](./manage-user-access.md#user-access) |
| Acceso a Collaboration para un nuevo usuario final. | Un administrador de sistemas o productos. | [Configurar el acceso de los usuarios](./manage-user-access.md#user-access) |
| Acceso a Collaboration para un usuario existente con acceso a Experience Platform. | Un administrador de sistemas o productos. | [Configurar el acceso a Collaboration](./manage-user-access.md#RTCDP-collab-access) |

{style="table-layout:auto"}

## Permisos adicionales

Una vez que haya obtenido acceso a Collaboration, es posible que necesite algunos permisos de Experience Platform adicionales para una funcionalidad específica.

### Fuentes de audiencia {#audience-sourcing}

Para poder empezar a enviar audiencias a los colaboradores, debe convertir las audiencias en origen en Collaboration. Actualmente, la única conexión de datos de autoservicio compatible para importar audiencias es Experience Platform. Para empezar, los usuarios que administren la incorporación a la audiencia deberán tener asignada una función que contenga los siguientes permisos de recurso de **[!UICONTROL Administración de perfiles]**:

| Permiso | Descripción |
| ---- | ---- |
| [!UICONTROL Ver segmentos] | Permite al usuario ver la lista de audiencias disponibles en una zona protegida. |
| [!UICONTROL Ver perfiles] | Permite al usuario ver los campos disponibles para su asignación a campos de colaboración. |

A continuación, puede ver una función de ejemplo con los permisos anteriores añadidos. Para obtener más información sobre cómo crear o asignar funciones, consulte la guía [administrar funciones](./manage-roles.md).

![Espacio de trabajo de recursos en Permisos con los permisos Ver segmentos y Ver perfiles agregados al recurso Administración de perfiles.](../../assets/permissions/sample-audience-role.png)

>[!NOTE]
>
>Los usuarios pueden trabajar con audiencias dentro de Collaboration después de haber obtenido datos sin ninguno de los permisos anteriores.

## Próximos pasos

Una vez que haya determinado por dónde empezar, siga el vínculo de su caso de uso para comenzar a configurar el acceso. Si desea obtener más información sobre cómo configurar el acceso a Collaboration como administrador además de estos casos de uso, consulte la guía [administrar el acceso de usuario](manage-user-access.md). Para obtener más información sobre las funciones y su función en la configuración del acceso a varios componentes de Collaboration, consulte la guía [administrar funciones](manage-roles.md).
