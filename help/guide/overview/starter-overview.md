---
title: Información general sobre RTCDP Collaboration Starter
description: Descubra cómo Adobe Real-Time CDP Collaboration Starter le ayuda a ampliar y mejorar la colaboración centrada en la privacidad con un socio con licencia sin requerir su propia licencia completa de Real-Time CDP.
audience: publisher, advertiser, invited users to Real-Time CDP Collaboration Starter
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 7ae0bd3d-eee9-48c0-9f18-a56033fee52d
source-git-commit: d0d854f73fa835984e5cff5207ce3e01297c8deb
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 5%

---

# Información general de Adobe Real-Time CDP Collaboration [!DNL Starter]

Use Adobe Real-Time CDP Collaboration [!DNL Starter] para colaborar con un socio con licencia en proyectos de datos centrados en la privacidad. No necesita su propia licencia de Collaboration para participar.

Su socio con licencia le invita a Collaboration y utiliza sus créditos para financiar sus flujos de trabajo conjuntos, tanto en patrones de anunciante a editor como de marca a marca. Para obtener más información sobre estos patrones y cómo funcionan, lee las guías de [patrones de colaboración](./collaboration-patterns.md) y [flujo de trabajo de extremo a extremo](./end-to-end-workflow.md).

Como usuario [!DNL Starter] invitado, puede:

* Incorporar y administrar datos de colaboración en una cuenta de [!DNL Starter].
* Source y mantener audiencias para utilizarlas en proyectos conjuntos.
* Obtenga información sobre las superposiciones de audiencias con su socio para admitir una segmentación y una medición de campañas eficaces.
* Active audiencias y compártalas con su socio para la activación y participación conjunta de campañas.

## Requisitos previos {#prerequisites}

Para empezar a usar Collaboration [!DNL Starter], asegúrese de que su organización y su socio con licencia estén ubicados en la misma región. Debe ser invitado por un socio que posea una licencia de Real-Time CDP Prime, Ultimate o Collaboration.

Para iniciar la invitación, proporcione la siguiente información a su socio con licencia:

* Nombre de contacto
* Correo electrónico de contacto
* Compañía
* Función (Anunciante/Publicador): Anunciante
* Industria

Después de recibir y aceptar la invitación, su organización debe revisar y firmar un pedido de ventas sin costo con Adobe para tener acceso a Collaboration [!DNL Starter]. Para obtener más información sobre el proceso de invitación, consulte la guía [invitar a un colaborador a Collaboration [!DNL Starter]](../connect/establishing-connections.md#invite-non-licensed-collaborator).

## Mecanismos de protección {#guardrails}

Lea la siguiente tabla para comprender las protecciones clave que se aplican a su cuenta de [!DNL Starter]. Estos incluyen límites en el abastecimiento de audiencias, volumen de datos, frecuencia de actualización, superposiciones de audiencias y capacidades de activación.

| Barrera | Descripción |
|----------| ------------|
| Origen de público | Puede llevar datos de audiencia a Collaboration con **[!DNL Amazon S3]** como origen. Para obtener instrucciones paso a paso, consulte [cómo configurar [!DNL Amazon S3] para el abastecimiento de audiencias](../setup/configure-aws-s3-audience-sourcing.md). |
| Público | Su cuenta de [!DNL Starter] tiene derecho a un máximo de:<ul><li>10 audiencias procedentes de un bloque de [!DNL AWS S3]</li><li>50 millones de identidades totales (calculadas mediante el número de filas en los datos de audiencia)</li><li>1 actualización por audiencia cada 6 días</li></ul> |
| Superposiciones de audiencias y perspectivas | No hay límite de uso en cuanto a la frecuencia con la que se pueden ejecutar superposiciones de audiencias y perspectivas entre audiencias. Aprenda a [descubrir superposiciones y comparar audiencias](../collaborate/discover.md). |
| Activation | Como usuario de [!DNL Starter], solo puede activar y compartir audiencias con el socio que le invitó. La configuración de destinos para plataformas externas no está disponible. Más información sobre [activar tus audiencias](../collaborate/activate.md). |

{style="table-layout:auto"}

## Introducción {#getting-started}

Una vez que [acepte su invitación y acepte los términos](../connect/establishing-connections.md#accept-invitation-sign-terms), inicie sesión en [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} con sus credenciales. Antes de poder usar Collaboration, se debe otorgar a su cuenta el acceso y las funciones correspondientes.

Use este flujo de trabajo para configurar su cuenta de [!DNL Starter] y comenzar a colaborar con su socio.

### Configuración del acceso de administrador {#setup-admin-access}

En primer lugar, use el área de trabajo **Acceso de administrador** para concederse el acceso necesario. Esto garantiza que tenga derechos administrativos y acceso de usuario a los productos de Experience Platform. Para ver los pasos detallados sobre cómo configurar el acceso inicial, consulte las [instrucciones de acceso de administrador](../setup/starter-admin-access.md).

Una vez finalizado, debería ver **[!UICONTROL Permisos]**, **[!UICONTROL Experience Platform]** y **[!UICONTROL Real-Time CDP Collaboration]** en la sección **[!UICONTROL Acceso rápido]** de la página principal de [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}.

![Espacio de trabajo de Adobe Experience Cloud que muestra permisos, Experience Platform y Real-Time CDP Collaboration después de configurar el acceso de administrador de productos.](/help/assets/overview/starter/setup-admin-access.png){zoomable="yes"}

Para obtener más información sobre las funciones de acceso y los distintos productos de Adobe Experience Cloud, lea la [descripción general del control de acceso](../permissions/overview.md).

### Configure los permisos {#configure-permissions}

Ahora que tiene privilegios de administrador, puede asignarse funciones y permisos a sí mismo y a otros usuarios de su organización. Este paso es necesario para poder acceder a Real-Time CDP Collaboration o permitir que otros lo utilicen. Para obtener instrucciones detalladas, consulte [cómo configurar los permisos](../setup/starter-permission-controls.md). Para obtener más información sobre las diferentes funciones y permisos disponibles en Collaboration, consulte la documentación de [administrar funciones](../permissions/manage-roles.md).

Una vez asignados los roles y los permisos, confirme que puede acceder a Collaboration. Vaya a [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} y seleccione **[!UICONTROL Real-Time CDP Collaboration]** en la sección **[!UICONTROL Acceso rápido]**. Esto abre el área de trabajo **[!UICONTROL Adobe Real-Time CDP Collaboration]**, donde puede empezar a usar las características de Collaboration.

### Configuración de conexiones {#set-up-connections}

A continuación, siga los pasos de las siguientes guías para configurar la conexión y comenzar a colaborar con su socio:

* [Configurar su cuenta de Collaboration](../setup/onboard-account.md)
* [Establezca una conexión con su colaborador invitado](../connect/overview.md)
* [Cree un nuevo proyecto y empiece a colaborar con su socio](../collaborate/overview.md)

### Comprender el uso del crédito {#understand-credit-usage}

Todas las actividades de Collaboration [!DNL Starter] utilizan créditos. Sin embargo, como usuario invitado, no es necesario que compre o administre estos créditos. El colaborador que le ha invitado cubre todo el uso del crédito asociado con sus actividades. Para obtener más información, consulte la [documentación sobre uso y consumo de crédito en Collaboration [!DNL Starter]](../setup/starter-credit-usage.md).

## Próximos pasos {#next-steps}

Ahora ha completado la configuración inicial y ha configurado su organización para una colaboración segura. A continuación, explore los siguientes recursos para obtener más información sobre el abastecimiento de audiencias y los diferentes casos de uso de proyectos dentro de Collaboration:

* [Source y administración de audiencias](../setup/onboard-audiences.md)
* [Casos de uso del proyecto](../collaborate/overview.md#project-use-cases):
   * [Descubra superposiciones y compare audiencias](../collaborate/discover.md)
   * [Activar públicos](../collaborate/activate.md)
   * [Medir el rendimiento de la campaña](../collaborate/measure.md)
