---
title: Información general sobre Conexiones
description: Obtenga información sobre las conexiones en Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 5c08738cdc8e1e208203ee1f9a1cf1891b5b07cb
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 0%

---

# Información general sobre Conexiones

{{limited-availability-release-note}}

Para que los colaboradores puedan trabajar juntos en las campañas, deben establecer una conexión. Esta conexión les permite activar audiencias, crear proyectos y ejecutar informes sobre el rendimiento de la campaña.

Las conexiones se establecen en función del patrón de colaboración elegido. Collaboration admite tres patrones de colaboración clave: anunciante a editor, marca a marca y anunciante a plataforma de publicidad. Para obtener más información sobre estos patrones, consulte la guía [patrones de colaboración](/help/guide/overview/collaboration-patterns.md).

Para aprender a establecer una conexión, lea la sección siguiente que corresponde a su patrón de colaboración:

- [Conexión de anunciante a editor](#advertiser-to-publisher-connection)
- [Conexión entre marcas](#brand-to-brand-connection)
- [Conexión entre anunciante y plataforma de publicidad](#advertiser-to-advertising-platform-connection)

## Conexión de anunciante a editor {#advertiser-to-publisher-connection}

![Diagrama de alto nivel del proceso de conexión anunciante-editor.](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

En el patrón de anunciante a editor, un anunciante descubre un publicador con el que desea trabajar a través del área de trabajo de **[!UICONTROL Discover publicadores]** y envía una invitación de conexión. A continuación, el editor revisa la invitación y la acepta, lo que permite al anunciante proponer la configuración de conexión. Una vez que el editor acepta la configuración de conexión, esta se establece y ambos colaboradores pueden empezar a trabajar juntos en los proyectos.

### Información general de alto nivel

Para establecer una conexión entre un anunciante y un editor, se deben seguir los siguientes pasos:

1. [Descubrir editores](./discover-collaborators.md): El anunciante identifica editores potenciales con los que colaborar.
2. [Enviar invitación](./establishing-connections.md#send-invite): El anunciante envía una invitación de conexión al editor seleccionado.
3. [Aceptar invitación](./establishing-connections.md#accept-invite): El editor revisa y acepta la invitación.
4. [Configurar opciones de conexión](./establishing-connections.md#configure-connection-settings): el anunciante configura las opciones de conexión y las envía al editor para que las revise.
5. [Confirmar configuración de conexión](./establishing-connections.md#review-connection-settings): el editor revisa la configuración de conexión y la acepta o la rechaza. Si se acepta, se establece la conexión. Si se rechaza, el publicador puede proporcionar comentarios sobre las revisiones fuera del producto. El anunciante puede revisar la configuración y reenviarla para su revisión.

Una vez aceptada la configuración de conexión, se establece la conexión y los colaboradores están listos para [crear un proyecto](/help/guide/collaborate/manage-projects.md#create-project) para comenzar a colaborar en las campañas.

## Conexión entre marcas {#brand-to-brand-connection}

![Diagrama de alto nivel del proceso de conexión de marca a marca.](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>El término **brand** se usa para referirse a una compañía o marca fuera de Collaboration. El término **colaborador** hace referencia a cualquier cuenta que pueda formar una conexión en Collaboration, independientemente de si es un anunciante o un editor.

En el patrón de marca a marca, dos marcas que se han comunicado fuera del producto pueden conectarse directamente en Collaboration mediante una [invitación de conexión privada](#private-connection-invite). Una marca puede ser un anunciante o un editor. Este patrón es especialmente útil para marcas que pueden no ajustarse al modelo tradicional de anunciante-editor, como dos anunciantes o dos editores.

Para empezar, un colaborador envía una invitación de conexión privada a otro colaborador. El destinatario revisa la invitación y la acepta, lo que permite al propietario proponer la configuración de conexión. Una vez que el destinatario acepta la configuración de conexión, esta se establece y ambos colaboradores pueden empezar a trabajar juntos en los proyectos.

### Información general de alto nivel

>[!TIP]
>
>Al discutir el proceso de conexión, habrá una distinción entre **propietario** y **destinatario**. El propietario es el colaborador que inicia la conexión enviando la invitación, mientras que el destinatario es el colaborador que recibe y revisa la invitación.

El proceso de conexión entre dos marcas implica varios pasos. Antes de que comience el proceso de conexión, se deben cumplir algunos requisitos previos:

1. Dos marcas se comunican fuera del producto para discutir la posible conexión.
1. Las marcas [crean cuentas](/help/guide/setup/onboard-account.md) en Collaboration si aún no lo han hecho, asegurándose de seleccionar el tipo de rol apropiado (anunciante o editor).

Una vez cumplidos los requisitos previos, puede comenzar el proceso de conexión. Los siguientes pasos describen el proceso:

1. [Enviar invitación a una conexión privada](./establishing-connections.md#private-connection-invite): Un colaborador envía una invitación a otra conexión privada.
2. [Aceptar invitación a conexión privada](./establishing-connections.md#accept-invite): El destinatario revisa y acepta la invitación a conexión privada.
3. [Configurar opciones de conexión](./establishing-connections.md#configure-connection-settings): El propietario configura las opciones de conexión y las envía al destinatario para que las revise y las acepte.
4. [Confirmar configuración de conexión](./establishing-connections.md#review-connection-settings): El destinatario revisa la configuración de conexión y la acepta o la rechaza.

Una vez aceptada la configuración de conexión, se establece la conexión y los colaboradores están listos para [crear un proyecto](/help/guide/collaborate/manage-projects.md#create-project) para comenzar a colaborar en las campañas.

## Conexión entre anunciante y plataforma de publicidad {#advertiser-to-advertising-platform-connection}

El proceso de conexión de anunciante a plataforma de publicidad permite a los anunciantes conectarse con plataformas de publicidad de terceros, como Amazon Marketing Cloud (AMC), para mejorar sus capacidades de marketing.

### Información general de alto nivel

El proceso de conexión entre un anunciante y una plataforma publicitaria implica varios pasos. Antes de que comience el proceso de conexión, asegúrese de que tiene una cuenta activa con la plataforma de publicidad y de que está aprobado para utilizar sus servicios. Los siguientes pasos describen el proceso de conexión:

1. [Descubre plataformas publicitarias](./discover-collaborators.md): El anunciante identifica posibles plataformas publicitarias con las que colaborar.
2. [Conectarse a la plataforma de publicidad](./advertising-platforms/overview.md#advertising-platforms-overview): El anunciante inicia el proceso de conexión al seleccionar la plataforma de publicidad con la que desea conectarse y sigue las indicaciones para autenticar y autorizar la conexión.
