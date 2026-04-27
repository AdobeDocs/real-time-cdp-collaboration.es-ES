---
title: Información general sobre Conexiones
description: Obtenga información sobre las conexiones en Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 419dde94-fee2-4dc1-b25d-cf79b7e57ec0
TQID: https://experienceleague.adobe.com/ZF3bqoR0XRv2G7abRULz1ElRgk5xLCZySHylrqzPqg0
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 803
ht-degree: 2%

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

Once the connection settings are accepted, the connection is established, and collaborators are ready to [create a project](/help/guide/collaborate/manage-projects.md#create-project) to begin collaborating on campaigns.

## Brand-to-brand connection {#brand-to-brand-connection}

![High-level diagram of the brand-to-brand connection process.](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>The term **brand** is used to refer a company or brand outside of Collaboration. The term **collaborator** refers to any account that can form a connection in Collaboration, regardless of whether they are an advertiser or a publisher.

In the brand-to-brand pattern, two brands that have communicated outside of the product can connect directly in Collaboration using a [private connection invite](#private-connection-invite). A brand can be either an advertiser or a publisher. This pattern is particularly useful for brands that may not fit the traditional advertiser-publisher model, such as two advertisers or two publishers.

To begin, a collaborator sends a private connection invite to another collaborator. The recipient reviews the invite and accepts it, allowing the owner to propose connection settings. Once the recipient accepts the connection settings, the connection is established, and both collaborators can start working together on projects.

### High-level overview

>[!TIP]
>
>When discussing the connection process, there will be a distinction between the **owner** and the **recipient**. The owner is the collaborator who initiates the connection by sending the invite, while the recipient is the collaborator who receives and reviews the invite.

The connection process between two brands involves several steps. Before the connection process begins, a few prerequisites must be met:

1. Two brands communicate outside of the product to discuss the potential connection.
1. The brands [create accounts](/help/guide/setup/onboard-account.md) in Collaboration if they haven&#39;t already, being sure to select the appropriate role type (advertiser or publisher).

Once the prerequisites are met, the connection process can begin. The following steps outline the process:

1. [Send private connection invite](./establishing-connections.md#private-connection-invite): One collaborator sends a private connection invite to another collaborator.
2. [Accept private connection invite](./establishing-connections.md#accept-invite): The recipient reviews and accepts the private connection invite.
3. [Configure connection settings](./establishing-connections.md#configure-connection-settings): The owner configures the connection settings and sends them to the recipient for review and acceptance.
4. [Confirm connection settings](./establishing-connections.md#review-connection-settings): The recipient reviews the connection settings and either accepts or rejects them.

Once the connection settings are accepted, the connection is established, and collaborators are ready to [create a project](/help/guide/collaborate/manage-projects.md#create-project) to begin collaborating on campaigns.

## Advertiser-to-advertising-platform connection {#advertiser-to-advertising-platform-connection}

The advertiser-to-advertising-platform connection process allows advertisers to connect with third-party advertising platforms, such as Amazon Marketing Cloud (AMC), to enhance their marketing capabilities.

### High-level overview

The connection process between an advertiser and an advertising platform involves several steps. Before the connection process begins, ensure you have an active account with the advertising platform and are approved to use their services. The following steps outline the connection process:

1. [Discover advertising platforms](./discover-collaborators.md): The advertiser identifies potential advertising platforms to collaborate with.
2. [Connect to advertising platform](./advertising-platforms/overview.md#advertising-platforms-overview): The advertiser initiates the connection process by selecting the advertising platform they want to connect with and follows the prompts to authenticate and authorize the connection.
