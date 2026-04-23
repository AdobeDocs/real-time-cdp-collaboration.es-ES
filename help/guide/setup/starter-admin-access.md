---
title: 'Configurar el acceso de administrador para la incorporación de Collaboration [!DNL Starter] '
description: Obtenga información sobre cómo configurar el acceso de administrador para Adobe Real-Time CDP Collaboration [!DNL Starter] mediante Admin Console en Adobe Experience Cloud.
audience: users invited to Real-Time CDP Collaboration [!DNL Starter]
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 7b5aa5e2-1238-4a0b-be20-becfe6c9e0b7
source-git-commit: db4cc34592e49254163d7db54f93238146ce72a4
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 3%

---

# Configurar el acceso de administrador para la incorporación de Collaboration [!DNL Starter]

Como el primer usuario de su organización en acceder a Adobe Experience Platform a través de Collaboration [!DNL Starter], usted es responsable de configurar y administrar el acceso para su equipo. Debe concederse los permisos de administrador y usuario necesarios para empezar a trabajar en Real-Time CDP Collaboration. Lea esta guía para aprender a configurar el acceso necesario en Admin Console para poder administrar permisos para colaboraciones en la interfaz de permisos.

## Requisitos previos {#prerequisites}

Antes de continuar, asegúrese de lo siguiente:

* Ha aceptado la invitación de su socio de Collaboration con licencia. Para obtener más información acerca de los requisitos de invitación, consulte la [descripción general de Collaboration [!DNL Starter] 2&rbrace;.](../overview/starter-overview.md#prerequisites)
* Revisó y firmó los términos y condiciones de Collaboration.
* Se ha recibido el correo electrónico de bienvenida de Adobe y se ha completado la creación de la cuenta por primera vez.

## Configuración del acceso {#setup-access}

Cuando se crea su cuenta de Adobe a través del flujo de trabajo [!DNL Starter], se le asigna automáticamente la función de administrador del sistema. Esto le permite administrar los usuarios y el acceso a los productos en Admin Console. Sin embargo, todavía no tiene acceso a **[!UICONTROL Permisos]**, que es necesario para administrar el acceso de Collaboration.

Use Admin Console para concederse **acceso de administrador de productos** a Experience Platform y **acceso de usuario** a productos de Experience Platform para obtener **[!UICONTROL permisos]**.

Para obtener más información sobre las funciones y los productos en Experience Cloud, lea la [descripción general del control de acceso](../permissions/overview.md).

>[!TIP]
>
>A lo largo de esta guía, un **administrador** hará referencia a **administradores de sistemas y productos**.

### Configuración del acceso de administrador de productos {#configure-product-admin-access}

Lea esta sección para concederse privilegios de administrador para comenzar a configurar el acceso para Collaboration [!DNL Starter].

#### Acceso a Admin Console {#access-admin-console}

Para empezar, inicia sesión en [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} con tus credenciales. Puede ver una lista de los productos disponibles en la sección **[!UICONTROL Acceso rápido]**. Seleccione **[!UICONTROL Admin Console]**.

![Página principal de Adobe Experience Cloud con Admin Console resaltado.](../../assets/setup/starter/admin-access/select-admin-console.png){zoomable="yes"}

#### Acceso al panel de producto de Adobe Experience Platform {#access-adobe-experience-platform}

El área de trabajo [Admin Console](https://adminconsole.adobe.com/) se abre en una nueva pestaña. Seleccione **[!UICONTROL Adobe Experience Platform]** de la lista **[!UICONTROL Productos]** en **[!UICONTROL Productos y servicios]**.

![espacio de trabajo de Admin Console con el producto Adobe Experience Platform resaltado.](../../assets/setup/starter/admin-access/admin-console-workspace.png){zoomable="yes"}

#### Añadir administrador de productos {#add-product-admin}

En el panel de producto de **[!UICONTROL Adobe Experience Platform]**, vaya a la pestaña **[!UICONTROL Administradores]**. Luego selecciona **[!UICONTROL Agregar administrador]**.

![Tablero de producto de Adobe Experience Platform con la ficha Administradores y la opción Agregar administrador resaltada.](../../assets/setup/starter/admin-access/add-admin.png){zoomable="yes"}

Escriba su dirección de correo electrónico o nombre de usuario en el cuadro de diálogo **[!UICONTROL Agregar administradores de productos]** y, a continuación, seleccione la cuenta correcta en el menú desplegable. Una vez finalizado, seleccione **[!UICONTROL Guardar]**.

![El cuadro de diálogo Agregar administradores de productos muestra la información de su cuenta y la opción Guardar resaltada.](../../assets/setup/starter/admin-access/add-product-admin.png){zoomable="yes"}

Ahora es administrador de productos y puede agregar usuarios u otros administradores al producto desde Admin Console. A continuación, concédase acceso de usuario al producto Experience Platform para acceder y realizar funciones en Permisos.

### Configuración del acceso de usuarios {#configure-user-access}

Para administrar permisos de Collaboration, debe tener **acceso de usuario** al producto, además del acceso de administrador. El acceso de usuario lo puede configurar un administrador de sistemas o de productos.

>[!TIP]
>
>Si está siguiendo los pasos de la sección anterior, ya debería estar en el tablero de productos **[!UICONTROL Adobe Experience Platform]** dentro de Admin Console. Desde aquí, proceda a [agregarse como usuario](#add-user).

Para comenzar a configurar el acceso de usuario, complete los siguientes pasos:

1. [Acceder a Admin Console desde la página principal de Adobe Experience Cloud](#access-admin-console).
2. [Vaya al panel de producto de Adobe Experience Platform](#access-adobe-experience-platform).

#### Añadir usuario al producto {#add-user}

Ahora se encuentra en el tablero de producto **[!UICONTROL Adobe Experience Platform]**. Vaya a la ficha **[!UICONTROL Usuarios]** y, a continuación, seleccione **[!UICONTROL Agregar usuarios]**.

![Tablero de producto de Adobe Experience Platform con la ficha Usuarios y la opción Agregar usuarios resaltada.](../../assets/setup/starter/admin-access/add-user.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Agregar usuarios a este producto]**, en el que se le pedirá que escriba su nombre, grupo de usuarios o dirección de correo electrónico. Rellene los valores y, a continuación, seleccione su cuenta de la lista desplegable.

![Agregar usuarios a este cuadro de diálogo de productos muestra la información de su cuenta y la opción Productos resaltada.](../../assets/setup/starter/admin-access/add-users-to-product.png){zoomable="yes"}

A continuación, seleccione el icono de agregar ![Agregar icono](../../assets/icons/plus.png) en **[!UICONTROL Productos]**.

Aparecerá un cuadro de diálogo con una lista de [perfiles de producto](https://helpx.adobe.com/es/enterprise/using/manage-product-profiles.html) disponibles. Seleccione **[!UICONTROL AEP-Default-All-Users]** y **[!UICONTROL Acceso predeterminado a todas las aplicaciones de producción]**. Luego selecciona **[!UICONTROL Aplicar]**.

El cuadro de diálogo ![Seleccionar perfiles de producto muestra los perfiles de producto seleccionados y la opción Aplicar resaltada.](../../assets/setup/starter/admin-access/select-product-profiles.png){zoomable="yes"}

Finalmente, selecciona **[!UICONTROL Guardar]** para finalizar la adición de un nuevo usuario al producto.

![Agregar usuarios al cuadro de diálogo de este producto con la opción Guardar resaltada.](../../assets/setup/starter/admin-access/save-user.png){zoomable="yes"}

Cuando tenga acceso de usuario, vuelva a [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}. Confirme que **[!UICONTROL Permisos]** y **[!UICONTROL Real-Time CDP Collaboration]** están disponibles en **[!UICONTROL Acceso rápido]**.

![Pantalla de inicio de Adobe Experience Cloud que muestra los permisos y Real-Time CDP Collaboration enumerados en Acceso rápido y resaltados.](../../assets/setup/starter/admin-access/permissions-collaboration-available.png){zoomable="yes"}

>[!TIP]
>
>Si **[!UICONTROL Permisos]** y **[!UICONTROL Real-Time CDP Collaboration]** no aparecen en **[!UICONTROL Acceso rápido]**, intente cerrar la sesión y volver a iniciarla.

## Próximos pasos {#next-steps}

Ahora cuenta con **acceso de administrador** y **acceso de usuario** para introducir permisos en los que puede definir funciones, asignar permisos específicos y administrar el acceso de usuario para las características y los recursos de Collaboration. Para obtener instrucciones paso a paso, consulte la [Guía de controles de permisos](./starter-permission-controls.md).
