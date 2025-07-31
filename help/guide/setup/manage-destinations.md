---
title: Configuración y administración de destinos
description: Obtenga información sobre cómo configurar y administrar destinos en Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b4b26761-46ac-420f-b9f7-6e829d67aec9
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 1%

---

# Configuración y administración de destinos

{{limited-availability-release-note}}

Los destinos son integraciones que se utilizan para enviar audiencias de destino a plataformas externas. Estas integraciones le permiten activar audiencias en varios canales y plataformas de marketing para utilizarlas en campañas y participación de clientes.

Los colaboradores pueden configurar destinos para enviar audiencias a plataformas externas, como Adobe Experience Platform, para usarlas en campañas. Los colaboradores pueden [activar audiencias dentro de un proyecto](../collaborate/activate.md), que se envían al destino configurado de su conexión. La activación puede realizarla el colaborador en función de la configuración de activación de audiencia [configurada en la conexión](/help/guide/connect/establishing-connections.md#configure-connection-settings).

![La ficha Mis destinos del área de trabajo de instalación muestra destinos de Adobe Experience Platform activos.](/help/assets/setup/manage-destinations/my-destinations-overview.png)

Para obtener más información sobre los destinos, consulte la guía [descripción general de destinos](../destinations/overview.md).

## Configuración de destinos {#configure-destinations}

Los destinos están configurados en la sección **[!UICONTROL Configuración]** de Collaboration. Para configurar un destino, ve a **[!UICONTROL Configuración]** y luego selecciona la pestaña **[!UICONTROL Mis destinos]**. Aquí puede ver todos los destinos disponibles.

>[!IMPORTANT]
>
>Para configurar y administrar destinos, el usuario debe tener una función con el permiso **Administrar datos de audiencia** asignado. Para obtener más información sobre la administración de funciones, consulte la guía [administrar funciones](../permissions/manage-roles.md).

![La ficha Mis destinos del área de trabajo de instalación muestra los destinos disponibles.](/help/assets/setup/manage-destinations/my-destinations.png)

El proceso de configuración de destinos depende del destino que esté configurando. Consulte el catálogo [destinos disponibles](../destinations/overview.md#available-destinations) para ver los destinos disponibles y sus guías de configuración.

>[!NOTE]
>
>Actualmente, solo Adobe Experience Platform está disponible como destino de autoservicio en Real-Time CDP Collaboration. Si le interesa configurar un destino diferente, póngase en contacto con su representante de Adobe.

## Eliminar destinos {#delete-destinations}

Al eliminar un destino, se elimina de la cuenta, se eliminan del destino las audiencias enviadas anteriormente y se impide que se envíen audiencias futuras a ese destino.

Para eliminar un destino, vaya a la ficha **[!UICONTROL Mis destinos]** en la sección **[!UICONTROL Configuración]**. Seleccione la opción **[!UICONTROL Delete]** para el destino que desee eliminar.

![Área de trabajo Mis destinos con la opción Eliminar resaltada para el destino Adobe Experience Platform.](/help/assets/setup/manage-destinations/delete-destination.png)

Aparecerá un cuadro de diálogo de confirmación, en el que puede confirmar que desea eliminar el destino. Seleccione **[!UICONTROL Eliminar]** para eliminar el destino.

![Cuadro de diálogo Eliminar destino con la opción Eliminar resaltada.](/help/assets/setup/manage-destinations/delete-destination-confirmation.png)

## Próximos pasos

Una vez configurado el destino, puede empezar a colaborar en sus conexiones para [activar audiencias de destino](../collaborate/activate.md) en sus proyectos.
