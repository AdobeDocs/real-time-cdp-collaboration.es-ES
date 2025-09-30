---
title: Flujo de trabajo de extremo a extremo
description: Comprenda el flujo de trabajo completo del uso de Real-Time CDP Collaboration en función de su patrón de colaboración.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
source-git-commit: 36f43d9d34ce7851a1c7093e0891f9c87e56387c
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 0%

---

# Flujo de trabajo de extremo a extremo

{{limited-availability-release-note}}

En Adobe Real-Time CDP Collaboration, el flujo de trabajo completo varía en función del patrón de colaboración que elija. El flujo de trabajo describe los pasos necesarios para configurar y ejecutar un proyecto de colaboración, desde la creación de cuentas y el abastecimiento de audiencias hasta la formación de conexiones y la creación de proyectos. Comprender este flujo de trabajo es esencial para aprovechar de forma eficaz las capacidades de la plataforma con el fin de lograr sus objetivos de marketing.

## Introducción

Antes de empezar, asegúrese de tener una comprensión sólida de estos conceptos clave:

- **patrones de Collaboration**: estos patrones definen cómo trabajan juntos los colaboradores. Hay dos patrones distintos: [anunciante a editor](./collaboration-patterns.md#advertiser-to-publisher) y [marca a marca](./collaboration-patterns.md#brand-to-brand).
- **Funciones de cuenta**: Las funciones de cuenta determinan las capacidades dentro de la plataforma. Deben coincidir con los objetivos, la marca y las metas de su organización. Hay dos funciones de cuenta: [anunciante](./roles.md#advertiser) y [publicador](./roles.md#publisher).
- **Casos de uso**: Los casos de uso definen las formas de aprovechar Collaboration para lograr sus objetivos de marketing. Hay tres casos de uso de colaboración: [Discover](./use-cases.md#discover), [Activate](./use-cases.md#activate) y [Measure](./use-cases.md#measure).

En esta guía se utilizan tres simuladores de colaborador para ilustrar el flujo de trabajo de extremo a extremo:

- **[!UICONTROL Luma]**: Una marca de ropa deportiva. Es un anunciante que quiere llegar a audiencias específicas a través de campañas de marketing dirigidas.
- **[!UICONTROL Tubo de TV]**: Un proveedor de transmisión digital. Es un editor que proporciona datos de audiencia para que los utilicen los anunciantes.
- **[!UICONTROL Ropa Fit]**: Otra marca de ropa deportiva. Es el segundo anunciante que desea colaborar para compartir datos de audiencia y perspectivas para mejorar los esfuerzos de marketing.

## Flujo de trabajo de anunciante a editor {#advertiser-to-publisher-workflow}

[!UICONTROL Luma], una empresa minorista deportiva, quiere establecer una conexión con [!UICONTROL TV Tube], un proveedor de streaming digital, para llegar a audiencias específicas a través de campañas de marketing dirigidas.

Para empezar, [!UICONTROL Luma] necesita [crear una cuenta](../setup/onboard-account.md) con la función de anunciante, mientras que [!UICONTROL TV Tube] crea una cuenta con la función de publicador.

Después de establecer sus cuentas, tanto [!UICONTROL Luma] como [!UICONTROL TV Tube] deben [crear una conexión de datos y audiencias de origen](../setup/onboard-audiences.md). Solo [!UICONTROL TV Tube] activará audiencias para campañas de marketing, por lo que necesitan [configurar un destino](../setup/manage-destinations.md).

Una vez que ambos colaboradores tengan sus cuentas configuradas, están listos para [formar una conexión](../connect/establishing-connections.md) dentro de la plataforma. [!UICONTROL Luma] usa la función [descubrir colaboradores](../connect/discover-collaborators.md) para encontrar [!UICONTROL TV Tube] e iniciar una solicitud de conexión. Después de que [!UICONTROL TV Tube] acepte la solicitud de conexión, [!UICONTROL Luma] configura la configuración de conexión para definir cómo se realiza la colaboración. [!UICONTROL TV Tube] acepta la solicitud de conexión para establecer un vínculo seguro entre las dos marcas.

Una vez establecida la conexión, [!UICONTROL Luma] [crea un proyecto](../collaborate/manage-projects.md) para iniciar su colaboración con [!UICONTROL TV Tube]. Durante la configuración del proyecto, eligen los casos de uso de colaboración que mejor se ajustan a sus objetivos: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md) y [Measure](../collaborate/measure.md).

[!UICONTROL Luma] aprovecha el caso de uso [Discover](../collaborate/discover.md) para obtener información sobre los datos de audiencia de [!UICONTROL TV Tube]. Una vez que [!UICONTROL Luma] ha identificado los segmentos de audiencia objetivo, [activan](../collaborate/activate.md) estas audiencias.

Después de activar las audiencias, [!UICONTROL TV Tube] ejecuta campañas de marketing dirigidas y carga datos en [Measure](../collaborate/measure.md) para evaluar la eficacia de su campaña.

## Flujo de trabajo de marca a marca {#brand-to-brand-workflow}

[!UICONTROL Fit Apparel], una marca de ropa deportiva, quiere colaborar con [!UICONTROL Luma], otra marca de ropa deportiva, para compartir datos de audiencia y perspectivas con el fin de mejorar los esfuerzos de marketing.

Después de establecer sus cuentas, tanto [!UICONTROL Fit Apparel] como [!UICONTROL Luma] necesitan [crear una conexión de datos y audiencias de origen](../setup/onboard-audiences.md). Tanto [!UICONTROL Fit Apparel] como [!UICONTROL Luma] activarán audiencias para las campañas de marketing, por lo que ambos deberán [configurar un destino](../setup/manage-destinations.md).

Después de obtener sus audiencias, [!UICONTROL Fit Apparel] y [!UICONTROL Luma] [forman una conexión](../connect/establishing-connections.md) dentro de la plataforma para compartir datos de audiencia de forma segura. Para ello, deben utilizar la característica [invitación a la conexión privada](../connect/establishing-connections.md#private-connection-invite). [!UICONTROL Luma] comparte su código de conexión con [!UICONTROL Fit Apparel], que lo usa para iniciar una solicitud de conexión. Después de que [!UICONTROL Luma] acepte la solicitud de conexión, [!UICONTROL Fit Apparel] configura las opciones de conexión para definir cómo colaborarán. En la configuración, [!UICONTROL Ajustar ropa] especifica que ambos colaboradores pueden activar audiencias para campañas de marketing. Para completar la conexión, [!UICONTROL Luma] acepta la solicitud para establecer un vínculo seguro entre las dos marcas.

Una vez establecida la conexión, [!UICONTROL Fit Apparel] [crea un proyecto](../collaborate/manage-projects.md) para iniciar su colaboración con [!UICONTROL Luma]. Durante la configuración del proyecto, eligen los casos de uso de colaboración que mejor se ajustan a sus objetivos: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md) y [Measure](../collaborate/measure.md).

[!UICONTROL Fit Apparel] y [!UICONTROL Luma] pueden usar el caso de uso [Discover](../collaborate/discover.md) para obtener información sobre los datos de audiencia de cada uno. Una vez que han identificado segmentos de audiencia valiosos, [activan](../collaborate/activate.md) las audiencias que han elegido para las campañas de marketing.

Finalmente, después de ejecutar sus campañas, ambas marcas cargan datos en [Measure](../collaborate/measure.md) para evaluar los resultados y la efectividad de su colaboración.
