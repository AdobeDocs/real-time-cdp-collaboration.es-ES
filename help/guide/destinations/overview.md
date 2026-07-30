---
title: Resumen de destinos
description: Obtenga información sobre los destinos en Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
TQID: https://experienceleague.adobe.com/1VvnSt3Z65dfQBfXnjJJi3H0Oj9BxFStexq3icVKxkY
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7ab1bc21a4d644e2e6a481d8de594d6a509a92a5
workflow-type: tm+mt
source-wordcount: 273
ht-degree: 11%

---

# Información general sobre los destinos

{{limited-availability-release-note}}

>[!NOTE]
>
>Esta página cubre los destinos en los que las audiencias están activadas **para**, como las plataformas de almacenamiento en la nube. Para activar audiencias **en un colaborador** dentro de un proyecto compartido, consulte la guía [activar audiencias](/help/guide/collaborate/activate.md).

Los destinos son integraciones que se utilizan para enviar audiencias de destino a plataformas externas. Estas integraciones le permiten activar audiencias en varios canales y plataformas de marketing para utilizarlas en campañas y participación de clientes.

Los colaboradores pueden configurar destinos para enviar audiencias a plataformas externas, como Adobe Experience Platform o una plataforma de almacenamiento en la nube, para usarlas en campañas. Los colaboradores pueden [activar audiencias dentro de un proyecto](../collaborate/activate.md), que se envían al destino configurado de su conexión. La activación puede realizarla el colaborador en función de la configuración de activación de audiencia [configurada en la conexión](/help/guide/connect/establishing-connections.md#configure-connection-settings).

>[!IMPORTANT]
>
>Actualmente, cuando los colaboradores activan audiencias dentro de un proyecto, se envían automáticamente al destino configurado de su conexión. Usted **debe** configurar un destino antes de que su colaborador pueda activar audiencias dentro de un proyecto.

## Destinos disponibles {#available-destinations}

Los siguientes destinos están disponibles para su configuración en Collaboration. Para ver la guía de configuración de ese destino, seleccione el nombre del destino en la tabla siguiente.

| Destino | Disponibilidad |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Disponible |
| [[!DNL Amazon S3]](./manage-destinations.md) | Disponible |
| [[!DNL Snowflake]](./manage-destinations.md) | Disponible |
| [[!DNL Google Cloud Storage]](./manage-destinations.md) | Disponible |
| [[!DNL Azure Blob Storage]](./manage-destinations.md) | Disponible |
| [[!DNL SFTP]](./manage-destinations.md) | Disponible |
| [[!DNL Data Landing Zone]](./manage-destinations.md) | Disponible |

>[!NOTE]
>
>**[!DNL Google Cloud Storage]** en esta tabla hace referencia a **destinos** (donde Collaboration envía audiencias durante la activación). Para **obtener audiencias de** un bloque GCS en el área de trabajo **[!UICONTROL Configuración]**, consulte [Configurar GCS para el abastecimiento de audiencias](../setup/configure-gcs-audience-sourcing.md).

## Próximos pasos

Para configurar un destino, consulte la guía [configurar y administrar un destino](./manage-destinations.md). Una vez que hayas configurado el destino, puedes empezar a [activar audiencias de destino](../collaborate/activate.md) dentro de tus proyectos.
