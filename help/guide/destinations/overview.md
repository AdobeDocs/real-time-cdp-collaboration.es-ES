---
title: Resumen de destinos
description: Obtenga información sobre los destinos en Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
source-git-commit: 4ef7f8c7c27935f0e5b3620da63e7129f2714b37
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 6%

---

# Información general sobre los destinos

{{limited-availability-release-note}}

Los destinos son integraciones que se utilizan para enviar audiencias de destino a plataformas externas. Estas integraciones le permiten activar audiencias en varios canales y plataformas de marketing para utilizarlas en campañas y participación de clientes.

Los colaboradores pueden configurar destinos para enviar audiencias a plataformas externas, como Adobe Experience Platform, para usarlas en campañas. Los colaboradores pueden [activar audiencias dentro de un proyecto](../collaborate/activate.md), que se envían al destino configurado de su conexión. La activación puede realizarla el colaborador en función de la configuración de activación de audiencia [configurada en la conexión](/help/guide/connect/establishing-connections.md#configure-connection-settings).

>[!IMPORTANT]
>
>Actualmente, cuando los colaboradores activan audiencias dentro de un proyecto, se envían automáticamente al destino configurado de su conexión. Usted **debe** configurar un destino antes de que su colaborador pueda activar audiencias dentro de un proyecto.

## Configuración de destinos {#configure-destinations}

Para configurar un destino, ve a **[!UICONTROL Configuración]** y luego selecciona la pestaña **[!UICONTROL Mis destinos]**. Aquí puede ver todos los destinos disponibles.

>[!NOTE]
>
> Actualmente, solo Adobe Experience Platform está disponible como destino de autoservicio en Collaboration. Si le interesa configurar un destino como Amazon S3 o Snowflake, póngase en contacto con su representante de Adobe.

![La ficha Mis destinos del área de trabajo de instalación muestra los destinos disponibles.](/help/assets/destinations/overview/my-destinations-overview.png)

Para comenzar a configurar un destino, selecciona la opción **[!UICONTROL Configurar]** en el destino que elijas. Para obtener información sobre cómo configurar destinos específicos, consulte las guías de la tabla [destinos disponibles](#available-destinations).

![Área de trabajo Mis destinos con la opción de configuración resaltada para el destino de Adobe Experience Platform.](/help/assets/destinations/overview/my-destinations-set-up.png)

### Destinos disponibles {#available-destinations}

Los siguientes destinos están disponibles para su configuración en Collaboration. Para ver la guía de configuración de ese destino, seleccione el nombre del destino en la tabla siguiente. Si le interesa configurar un destino que no está disponible actualmente, póngase en contacto con su representante de Adobe.

| Destino | Disponibilidad |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Disponible |
| Amazon S3 | Muy pronto. |
| Snowflake | Muy pronto. |
| Almacenamiento en la nube de Google | Muy pronto. |
| Azure Blob Storage | Muy pronto. |

## Próximos pasos

Una vez que hayas configurado el destino, puedes empezar a [activar audiencias de destino](../collaborate/activate.md) dentro de tus proyectos.
