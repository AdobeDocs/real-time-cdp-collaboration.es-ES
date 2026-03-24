---
title: Configure and manage your account
description: Learn how to configure and manage various aspects of your account in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: be7078b16d8126a80cced0a3a8328b465b6ec245
workflow-type: tm+mt
source-wordcount: '1393'
ht-degree: 13%

---

# Configure and manage your account

{{limited-availability-release-note}}

Learn how to set up your account in Real-Time CDP Collaboration to prepare for connections with other collaborators. This guide covers the initial setup of your account, including adding account details, selecting match keys, and managing your account&#39;s settings.

![](/help/assets/setup/manage-account/my-account.png){zoomable="yes"}

## Set up your account {#set-up-account}

[&#128279;](#set-up-details)

**&#x200B;**![](/help/assets/icons/plus.png)**&#x200B;**

![](/help/assets/setup/manage-account/add-new-account.png){zoomable="yes"}

### Configuración de detalles {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="Correo electrónico de contacto"
>abstract="Proporcione un correo electrónico basado en funciones o en equipos, como **collaboration@yourcompany.com**. No se deben utilizar direcciones de correo electrónico personales o individuales."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="Código de conexión"
>abstract="El código de conexión es un identificador único de su cuenta. Se utiliza para establecer conexiones con otras organizaciones en Real-Time CDP Collaboration."

To begin configuring your account, you must first set up the account details. This requires you to add the following information:

* **&#x200B;**
* **&#x200B;**
* **&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;[&#128279;](/help/guide/overview/roles.md)
* **&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**
* **&#x200B;**
* **&#x200B;**
* **&#x200B;**
* Select an image for your account header picture.

>[!NOTE]
>
>**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/manage-account/add-account-details.png){zoomable="yes"}

### Configurar claves de coincidencia {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia son identificadores que se utilizan para reconciliar perfiles de públicos de diferentes fuentes de datos. Incluya cualquier clave de coincidencia con la que pueda trabajar su marca."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_setup_match_keys"
>title="claves de coincidencia"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="ID de personas propios"
>abstract="Los ID de personas propios, como las direcciones de correo electrónico, los números de teléfono con hash, o los ID de CRM, están conectados directamente a un perfil individual."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="ID de dispositivos propios"
>abstract="Los ID de dispositivos propios, como las direcciones ECID o IP, se conectan directamente a los dispositivos, que pueden compartirse entre varias personas."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="ID de socios compatibles"
>abstract="Los ID de socio son identificadores proporcionados por socios externos para la reconciliación de públicos. Los ID de socio no están conectados directamente a un perfil individual."

![](/help/assets/setup/manage-account/match-keys.png){zoomable="yes"}

>[!IMPORTANT]
>
>[&#128279;](../connect/establishing-connections.md#connection-settings)**&#x200B;**

[&#128279;](./onboard-audiences.md#map-fields)

[&#128279;](#edit-account)

#### Claves de coincidencia admitidas {#supported-match-keys}

Collaboration supports three types of match keys: first-party people IDs, first-party device IDs, and partner IDs. All match keys must meet the following requirements:

* **&#x200B;**&#x200B;**&#x200B;**
* **&#x200B;**
* If you provide hashed values that use uppercase characters, Collaboration automatically converts them to lowercase.
* **&#x200B;**&#x200B;**&#x200B;**&#x200B;[&#128279;](./manage-data-connection.md#match-keys)

##### ID de personas propios

First-party people IDs are directly connected to an individual profile. Currently supported IDs are:

* **&#x200B;**
* **&#x200B;**
* **&#x200B;**
* **&#x200B;**
<!-- * **[!UICONTROL Custom ID]**: Custom identifiers -->

##### ID de dispositivos propios

First-party device IDs are identifiers connected to a specific device. Currently supported IDs are:

* **&#x200B;**
* **&#x200B;**
* **&#x200B;**

##### ID de socios

Los ID de socio son identificadores proporcionados por socios externos para la reconciliación de públicos. 

* **&#x200B;**

>[!NOTE]
>
>[!DNL AdFixus]&#x200B;**&#x200B;**

**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/manage-account/adfixus-settings.png){zoomable="yes"}

**&#x200B;**

![](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Edit account {#edit-account}

After setting up your account, you can edit the details and match keys at anytime.

### Editar detalles {#edit-details}

**&#x200B;**

**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

**&#x200B;**

![](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

### Editar claves de coincidencia {#edit-match-keys}

You can also update the match keys that you initially selected when creating your account. These match keys will determine the match keys available to future connections.

**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**

>[!IMPORTANT]
>
>[&#128279;](../glossary.md#sketches) [&#128279;](./manage-data-connection.md#scheduling)
>
>At this time, match keys cannot be removed once added to your account.

![](/help/assets/setup/manage-account/match-key-dialog.png){zoomable="yes"}

A success dialog confirms that your account&#39;s match keys are updated successfully.

![](/help/assets/setup/manage-account/match-key-updated-successfully.png){zoomable="yes"}

## Próximos pasos

[&#128279;](/help/guide/setup/onboard-audiences.md)
