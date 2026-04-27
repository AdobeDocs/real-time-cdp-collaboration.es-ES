---
title: Administrar el acceso de los usuarios mediante permisos
description: Administre los permisos y el acceso de los usuarios a diferentes componentes de la interfaz de usuario de Real-Time CDP Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0155f6a6-5e67-4415-af96-1848345842e4
TQID: https://experienceleague.adobe.com/uPFss3qIstJmeVFF1YpQQJ0V848SiDEfy6BYyEcgPZw
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1406
ht-degree: 3%

---

# Administrar el acceso de los usuarios mediante permisos {#manage-user-access}

{{limited-availability-release-note}}

Administre permisos y acceso de usuarios a componentes individuales dentro de Adobe Real-Time CDP Collaboration a través de la interfaz de Experience Cloud [Permissions](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/browse){target="_blank"}. Los permisos permiten a los administradores de sistemas y productos definir [roles](./manage-roles.md) para administrar el acceso de los usuarios a características y recursos específicos.

## Configuración del acceso a los permisos {#permissions-access}

Para acceder a los permisos, debe tener acceso de administrador de producto y de usuario al producto de Adobe Experience Platform. Se requiere un administrador del sistema para configurar los privilegios de administrador de productos, mientras que un administrador del sistema o de productos puede configurar los privilegios de usuario. Para obtener más información sobre las funciones administrativas, lea la guía [jerarquía de control de acceso](./overview.md#hierarchy).

>[!TIP]
>
>A lo largo de esta guía, un **administrador** hará referencia a **administradores de sistemas y productos**.

### Administradores del sistema: configurar el acceso de administrador de productos {#admin-access}

Conceda a un administrador de productos de usuario acceso para proporcionarle funciones administrativas dentro del producto de Experience Platform mediante los siguientes pasos:

>[!IMPORTANT]
>
>Como administrador del sistema, tiene acceso predeterminado a productos específicos de Experience Cloud, como Adobe Admin Console. Sin embargo, para utilizar Permisos, es necesario que se proporcione a sí mismo un acceso de administrador y usuario del producto de Experience Platform. Siga la guía paso a paso que se muestra a continuación para concederse acceso como administrador del sistema.

Inicie sesión en [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} con sus credenciales. La vista Inicio se muestra con una lista de los productos disponibles en la sección **[!UICONTROL Acceso rápido]**. Seleccione **[!UICONTROL Admin Console]**.

![Vista de inicio de Experience Cloud con Admin Console resaltado.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

Se muestra el panel de información general de [Adobe Admin Console](https://adminconsole.adobe.com/). Seleccione **[!UICONTROL Adobe Experience Platform]** de la lista **[!UICONTROL Productos]** en **[!UICONTROL Productos y servicios]**.

![Panel de información general de Admin Console con el producto Adobe Experience Platform resaltado.](../../assets/permissions/admin-console.png){zoomable="yes"}

Se muestra el panel de Adobe Experience Platform. Seleccione la ficha **[!UICONTROL Administradores]** y luego seleccione **[!UICONTROL Agregar administrador]**.

![Tablero de producto de Adobe Experience Platform con la ficha Administradores seleccionada y Agregar administrador resaltado.](../../assets/permissions/add-admin.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Agregar administradores de productos]**. Introduzca el correo electrónico o el nombre de usuario en el campo de texto **[!UICONTROL Correo electrónico o nombre de usuario]** y, a continuación, seleccione la cuenta correcta en el menú desplegable. Seleccione **[!UICONTROL Guardar]** para finalizar la adición del usuario como administrador de productos.

![Cuadro de diálogo Agregar administradores de productos con información de usuarios completada y la opción Guardar seleccionada.](../../assets/permissions/add-product-administrators.png){zoomable="yes"}

El usuario ahora tiene privilegios de administrador de productos y puede realizar funciones administrativas, como agregar usuarios u otros administradores, al producto en Admin Console. A continuación, necesitará el acceso de usuario al producto de Experience Platform para acceder y realizar funciones dentro de Permisos.

### Administradores: configurar el acceso de los usuarios a Experience Platform {#user-access}

Ahora que ha concedido al administrador de productos acceso, debe proporcionarle acceso de usuario al producto de Experience Platform. Como parte de las configuraciones de acceso, asignará al usuario [perfiles de producto](https://helpx.adobe.com/es/enterprise/using/manage-product-profiles.html) específicos.

>[!TIP]
>
>Si está siguiendo los pasos de la sección anterior, ya estará dentro del producto de Adobe Experience Platform y puede omitir el primer paso.

Vaya a [Admin Console](https://adminconsole.adobe.com/){target="_blank"} y seleccione **[!UICONTROL Adobe Experience Platform]** de la lista **[!UICONTROL Productos]** en **[!UICONTROL Productos y servicios]**.

![Vista de inicio de Experience Cloud con Admin Console resaltado.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

Seleccione la ficha **[!UICONTROL Usuarios]** y luego seleccione **[!UICONTROL Agregar usuarios]**.

![Tablero de producto de Adobe Experience Platform con la ficha Usuarios seleccionada y Agregar usuarios resaltada.](../../assets/permissions/add-users.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Agregar usuarios a este producto]**. Escriba el nombre o el correo electrónico del usuario en el campo de texto **[!UICONTROL Nombre, grupo de usuarios o dirección de correo electrónico]** y, a continuación, seleccione la cuenta correcta en el menú desplegable. A continuación, seleccione la opción de adición **[!UICONTROL Productos]**.

![Cuadro de diálogo Agregar usuarios a este producto con información de usuarios rellenada y la opción Agregar productos seleccionada.](../../assets/permissions/add-users-to-product.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Seleccionar perfiles de producto]**. Seleccione **[!UICONTROL AEP-Default-All-Users]** y **[!UICONTROL Acceso predeterminado a todas las aplicaciones de producción]** y, a continuación, seleccione **[!UICONTROL Aplicar]**.

![El cuadro de diálogo Seleccionar perfiles de producto con las opciones AEP-Default-All-Users y Default Production All Access seleccionadas y Aplicar resaltadas.](../../assets/permissions/select-product-profiles.png){zoomable="yes"}

Confirme que la información es correcta y, a continuación, seleccione **[!UICONTROL Guardar]**.

![Cuadro de diálogo Agregar usuarios a productos con la información de los usuarios y los perfiles de producto mostrados y el cuadro de diálogo Guardar resaltado.](../../assets/permissions/save-selections.png){zoomable="yes"}

El usuario ahora debe tener acceso de administrador de productos y productos a Experience Platform, lo que le permitirá acceder a los permisos. A continuación, debe asignar al usuario dos funciones fundamentales para que tenga acceso a la interfaz de usuario de Experience Platform.

### Administradores: configurar el acceso a la IU de Experience Platform {#product-access}

En Real-Time CDP Collaboration, los administradores y los usuarios finales trabajarán con datos de Experience Platform, como audiencias y registros de auditoría. Estos datos se mantienen en instancias de Experience Platform denominadas zonas protegidas. Para garantizar que los usuarios puedan interactuar con estos datos, debe asignar [funciones predeterminadas](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#default-roles){target="_blank"} al usuario.

Para empezar, ve a [Adobe Experience Cloud](https://experience.adobe.com/). Ahora debería ver **[!UICONTROL Experience Platform]** y **[!UICONTROL Permisos]** dentro de **[!UICONTROL Acceso rápido]**.

![Vista de inicio de Experience Cloud con Experience Platform y permisos resaltados.](../../assets/permissions/experience-cloud-products.png){zoomable="yes"}

>[!NOTE]
>
> Los productos pueden tardar varios minutos en obtener acceso a y recibirá un correo electrónico que le avisará de que ha recibido acceso. Si no ve Experience Platform o Permisos en Adobe Experience Cloud después de recibir el correo electrónico, cierre la sesión y vuelva a iniciarla en la cuenta.

En este momento, ahora puede obtener acceso a **[!UICONTROL Permisos]**. Si intentas acceder a **[!UICONTROL Experience Platform]**, recibirás una advertencia avisando que no hay zonas protegidas habilitadas, como se muestra a continuación. Para resolver esto, debe asignar las funciones predeterminadas al usuario. Para empezar, seleccione **[!UICONTROL Permisos]**.

![Vista de inicio de Experience Cloud con una advertencia y Permisos resaltados.](../../assets/permissions/experience-cloud-warning.png){zoomable="yes"}

Se mostrará el panel **[!UICONTROL Permisos]**. Seleccione **Usuarios** en el panel izquierdo y, a continuación, seleccione el nombre del usuario.

![Panel de permisos con el área de trabajo Usuarios mostrado y un usuario resaltado.](../../assets/permissions/permissions-user.png){zoomable="yes"}

Seleccione la ficha **[!UICONTROL Roles]** y luego seleccione **[!UICONTROL Agregar roles]**.

![Espacio de trabajo del usuario con la ficha Roles mostrada y Agregar roles resaltados.](../../assets/permissions/user-roles.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Agregar roles]**. Seleccione **[!UICONTROL Acceso predeterminado a todos los equipos de producción]** y **[!UICONTROL Administradores de espacio aislado]** y, a continuación, seleccione **[!UICONTROL Guardar]**.

![Se seleccionó el cuadro de diálogo Agregar roles con los administradores de acceso y de zona protegida de producción predeterminada y se resaltó Guardar.](../../assets/permissions/add-roles.png){zoomable="yes"}

Ahora tiene acceso a Experience Platform y a Permisos. In the final step, you&#39;ll grant access to Real-Time CDP Collaboration.

### Administradores: configurar el acceso a Real-Time CDP Collaboration {#RTCDP-collaboration-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_permissions"
>title="guía de administración de acceso de usuarios"
>abstract=""

To grant users access to Collaboration, you&#39;ll use an access control concept called roles. Roles define the level of access a administrator or user has to [resources](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions) in your organization.

When configuring individual access to Collaboration, you&#39;ll assign users&#39; roles containing permissions from the Collaborations resource. You can use the [manage roles](./manage-roles.md) guide to find out information on:

- the [two standard roles](./manage-roles.md#standard-roles) and the levels of access they grant to Collaboration
- creating [custom roles](./manage-roles.md#specific-access-roles) using the Collaboration resource
- the list of permissions included in the Collaborations resource

>[!NOTE]
>
>Additionally, a user must be assigned to a role containing the **[!UICONTROL Prod]** permission in the **[!UICONTROL Sandboxes]** resources. Both standard roles contain this permission. If you choose to assign a user a custom role instead of a standard role, you must ensure one of the roles they are assigned to contain this permission.

Once you&#39;ve chosen or created a role that encompasses the level of access your user needs, you need to assign the user to that role.

#### Assign a role

You may assign multiple roles to a single user or assign multiple users to a single role. The first case was covered earlier when [assigning the default roles](#product-access) to give a user access to Experience Platform. In the next steps, you&#39;ll assign users directly to the role you&#39;ve selected.

In **[!UICONTROL Permissions]** select **[!UICONTROL Roles]** from the left panel and then select your role from the list.

![The Permissions dashboard with the Roles workspace displayed and a role highlighted.](../../assets/permissions/select-role.png){zoomable="yes"}

The role&#39;s detail page displays. Select the **[!UICONTROL Users]** tab and then select **[!UICONTROL Add Users]**.

![The role&#39;s detail workspace with the Users tab displayed and Add Users highlighted.](../../assets/permissions/role-users.png){zoomable="yes"}

The **[!UICONTROL Add Users]** dialog appears. Select the user(s) from the list and then select **[!UICONTROL Save]**.

![The Add Users dialog with a user select and the Save option highlighted.](../../assets/permissions/add-users-to-role.png){zoomable="yes"}

The user should now see **[!UICONTROL RTCDP Collaboration]** listed as a product under **[!UICONTROL Quick Access]** in Experience Cloud.

![Experience Cloud con RTCDP Collaboration destacado en Acceso rápido](../../assets/permissions/rtcdp-experience-cloud.png)

## Pasos siguientes

Ahora que los usuarios tienen acceso a Real-Time CDP Collaboration, pueden empezar a utilizar el producto. Para obtener más información sobre el producto en su conjunto, lea la [guía de información general](../home.md).
