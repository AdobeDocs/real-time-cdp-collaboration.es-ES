---
title: Incorporación y administración de la organización
description: Aprenda a incorporar y administrar varios aspectos de su organización en Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 860138b95abc4d6af94bbbf722cf498463570c1b
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 16%

---

# Incorporar y administrar su organización

{{limited-availability-release-note}}

Aprenda a incorporar su organización en Real-Time CDP Collaboration y a administrar varios aspectos de su compañía. Esta página describe los pasos para incorporar una organización a Adobe Real-Time CDP Collaboration, incluida la configuración de las claves de coincidencia, las identidades preferidas y más opciones.

![Espacio de trabajo de configuración de la organización que muestra su configuración actual.](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## Configuración inicial de la organización

Primero debe configurar su organización y los detalles de la organización. Si esta es su primera organización, se le dirigirá a través del proceso de incorporación inmediatamente, empezando por configurar sus [detalles de cuenta](#set-up-details).

Para agregar organizaciones adicionales, vaya a **[!UICONTROL Configuración]** en el carril izquierdo y seleccione el icono Agregar (![Agregar icono.](/help/assets/icons/plus.png)) en la esquina superior derecha. A continuación, seleccione **[!UICONTROL Cuenta]**.

![Área de trabajo de configuración con la opción Cuenta resaltada.](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

### Configuración de detalles {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="Correo electrónico de contacto"
>abstract="Proporcione un correo electrónico basado en funciones o en equipos, como `collaboration@yourcompany.com`. No se deben utilizar direcciones de correo electrónico personales o individuales."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="Código de conexión"
>abstract="El código de conexión es un identificador único para su organización. Se utiliza para establecer conexiones con otras organizaciones en Real-Time CDP Collaboration."

<!-- Move the above to new section for invite on this page when its created -->

Para comenzar a incorporar su organización, primero debe configurar los detalles de la organización. Esto requiere que agregue la siguiente información:

* Añada un **[!UICONTROL nombre de organización]** para su compañía.
* Agrega una **[!UICONTROL descripción]** sobre tu compañía.
* Seleccione su **[!UICONTROL rol de compañía]**. Puede seleccionar entre **[!UICONTROL Anunciante]** y **[!UICONTROL Publicador]**. Lea el [documento de flujo de trabajo de extremo a extremo](/help/guide/end-to-end-workflow.md) para ver similitudes y pequeñas diferencias en el flujo de trabajo entre los dos tipos de funciones organizativas.
* Seleccione el **[!UICONTROL sector]** de su organización. Algunos ejemplos son **[!UICONTROL Retail]**, **[!UICONTROL Telecomunicaciones]** o **[!UICONTROL Servicios financieros]**.
* Seleccione la **[!UICONTROL región]** de su organización. En la versión actual del producto, **[!UICONTROL Norteamérica]** es la selección predeterminada preestablecida.
* Agregue un **[!UICONTROL correo electrónico de contacto]** para su organización. Debe ser una dirección de correo electrónico basada en el equipo o en la función. No se deben proporcionar direcciones de correo electrónico personales.
* Cargue un **[!UICONTROL logotipo]** para su compañía. Actualmente, se admiten imágenes de tipo SVG.
* Seleccione una imagen para la imagen del encabezado de la empresa.

>[!NOTE]
>
>Aunque puede editar la mayoría de estos detalles en cualquier momento, **[!UICONTROL Role]** y **[!UICONTROL Region]** no se pueden editar después de la configuración inicial.

![Configuración del área de trabajo de la organización con la sección Detalles mostrada.](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

Cuando termine, use **[!UICONTROL Siguiente]** para pasar a la página siguiente y seleccionar las claves de coincidencia que desea que use su organización.

### Configurar claves de coincidencia {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia son identificadores que se utilizan para reconciliar miembros entre los públicos de diferentes fuentes de datos. Incluya cualquier clave de coincidencia con la que pueda trabajar su compañía."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="ID de personas propios"
>abstract="Los ID de personas propios, como las direcciones de correo electrónico con hash o los números de teléfono, están conectados directamente a un perfil individual. Los ID admitidos actualmente son correos electrónicos con hash y números de teléfono."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="ID de dispositivos propios"
>abstract="Los ID de dispositivos propios, como las direcciones ECID o IP, se conectan directamente a los dispositivos, que pueden compartirse entre varias personas. IPv4 es el único ID de dispositivo propio compatible actualmente."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="ID de socios compatibles"
>abstract="Los ID de socio asociados con perfiles amplían el alcance a un perfil determinado."

>[!IMPORTANT]
>
>Las claves de coincidencia que seleccione durante la configuración de la organización determinarán las claves de coincidencia disponibles para las conexiones que cree con otras organizaciones. Aunque puede quitar las claves de coincidencia durante la configuración de la conexión, no puede agregar nuevas claves de coincidencia más adelante. Es importante seleccionar todas las claves de coincidencia que planea utilizar en futuras campañas durante la configuración de la organización.

Las claves de coincidencia, como las direcciones de correo electrónico, los ID de dispositivo o los ID de cliente, ayudan a los anunciantes y editores a trabajar juntos, ya que permiten una sincronización de datos precisa y centrada en la privacidad, lo que permite una segmentación y medición de audiencias más precisas.

![Diapositiva que muestra los identificadores disponibles para la primera versión de Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Seleccione las claves de coincidencia que desee utilizar para reconciliar a los miembros de las audiencias de editor y anunciante. Incluya cualquier clave de coincidencia con la que pueda trabajar su compañía. Planifique el futuro y seleccione las claves de coincidencia que prevé utilizar en futuras campañas de editor-anunciante. Si necesita seleccionar claves de coincidencia adicionales para su organización, también puede hacerlo más adelante, en el flujo de trabajo [editar organización](#edit-organization).

![Se muestra la sección Configurar el área de trabajo de la organización con la sección Coincidir claves.](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

Seleccione hasta cinco claves de coincidencia que desee utilizar. Posteriormente, al configurar las conexiones, puede quitar las claves de coincidencia no deseadas, pero no puede agregar nuevas.

Las claves de coincidencia disponibles en Real-Time CDP Collaboration pueden ser de tres tipos:

* ID de personas propios
* ID de dispositivos propios
* ID de socios

Las claves de coincidencia disponibles para la primera versión de Real-Time CDP Collaboration son:

* Correo electrónico con hash

Cuando esté listo, seleccione **[!UICONTROL Completar]** para finalizar el flujo de trabajo de configuración de la organización.

## Editar organización {#edit-organization}

Después de configurar inicialmente la organización, puede editar en cualquier momento ciertos aspectos y detalles de la organización. Para editar tu organización, selecciona **[!UICONTROL Editar]** en la sección **[!UICONTROL Mi organización]** del área de trabajo **[!UICONTROL Configuración]**.

![Área de trabajo de instalación con la ficha Mi organización y la opción Editar resaltadas.](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

Ahora puede editar los detalles de su organización, excepto la **[!UICONTROL función]** y la **[!UICONTROL región]**.

![Cuadro de diálogo Editar detalles de la organización.](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

También puede actualizar las claves de coincidencia que seleccionó inicialmente al incorporar su organización. Seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Claves de coincidencia]** para agregar las claves de coincidencia adicionales que desee.

![Área de trabajo de instalación con la opción Editar resaltada en la sección Claves de coincidencia de la organización.](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## Pasos siguientes

Después de configurar su organización, está listo para [importar audiencias](/help/guide/setup/onboard-audiences.md) en Real-Time CDP Collaboration.
