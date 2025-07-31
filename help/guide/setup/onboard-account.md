---
title: Configuración y administración de la cuenta
description: Obtenga información sobre cómo configurar y administrar varios aspectos de su cuenta en Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 608706d00124372ac59209478ab551a3a6ce0226
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 18%

---

# Configuración y administración de la cuenta

{{limited-availability-release-note}}

Obtenga información sobre cómo configurar su cuenta en Real-Time CDP Collaboration para prepararse para conexiones con otros colaboradores. Esta guía trata sobre la configuración inicial de su cuenta, incluyendo la adición de detalles de la cuenta, la selección de claves de coincidencia y la administración de la configuración de su cuenta.

![Espacio de trabajo de instalación que muestra una cuenta configurada.](/help/assets/setup/manage-account/my-account.png){zoomable="yes"}

## Configurar su cuenta {#set-up-account}

Cuando acceda por primera vez a Collaboration, se le pedirá que configure su cuenta. Este es un proceso único que le permite configurar los detalles de la cuenta y las claves de coincidencia. Si esta es la primera cuenta de su organización, se le dirigirá a través del proceso de incorporación inmediatamente, empezando por configurar sus [detalles de cuenta](#set-up-details).

Para agregar organizaciones adicionales, vaya a **[!UICONTROL Configuración]** en el carril izquierdo y seleccione el icono Agregar (![Agregar icono.](/help/assets/icons/plus.png)) en la esquina superior derecha. A continuación, seleccione **[!UICONTROL Cuenta]**.

![Área de trabajo de configuración con la ficha Mi cuenta y la opción Cuenta resaltadas.](/help/assets/setup/manage-account/add-new-account.png){zoomable="yes"}

### Configuración de detalles {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="Correo electrónico de contacto"
>abstract="Proporcione un correo electrónico basado en funciones o en equipos, como **collaboration@yourcompany.com**. No se deben utilizar direcciones de correo electrónico personales o individuales."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="Código de conexión"
>abstract="El código de conexión es un identificador único de su cuenta. Se utiliza para establecer conexiones con otras organizaciones en Real-Time CDP Collaboration."

<!-- Move the above popover to new section for invite on this page when its created -->

Para comenzar a configurar la cuenta, primero debe configurar los detalles de la cuenta. Esto requiere que agregue la siguiente información:

* Agregue un **[!UICONTROL nombre de cuenta]** que represente claramente su marca.
* Agrega una **[!UICONTROL descripción]** sobre tu marca. Esto es opcional, pero ayuda a otros colaboradores a comprender mejor su marca.
* Seleccione su **[!UICONTROL rol]**. Puede seleccionar entre **[!UICONTROL Anunciante]** y **[!UICONTROL Publicador]**. Lea el [documento de flujo de trabajo de extremo a extremo](/help/guide/end-to-end-workflow.md) para ver similitudes y pequeñas diferencias en el flujo de trabajo entre los dos tipos de funciones organizativas.
<!-- The above will need to be updated when I update things for B2B -->
* Seleccione el **[!UICONTROL sector]** de su cuenta. Algunos ejemplos son **[!UICONTROL Retail]**, **[!UICONTROL Telecomunicaciones]** o **[!UICONTROL Servicios financieros]**.
* La **[!UICONTROL región]** se establece automáticamente en función de tu cuenta de Adobe Experience Cloud. Esto no se puede cambiar en ningún momento.
* Agrega un **[!UICONTROL correo electrónico de contacto]** a tu cuenta. Debe ser una dirección de correo electrónico basada en el equipo o en la función. No se deben proporcionar direcciones de correo electrónico personales.
* Sube un **[!UICONTROL logotipo]** para tu cuenta. Actualmente, se admiten imágenes de tipo SVG. Esto es opcional, pero cargar un logotipo ayuda a representar visualmente su marca en la interfaz de Collaboration
* Seleccione una imagen para la imagen del encabezado de la cuenta.

>[!NOTE]
>
>Aunque puede editar la mayoría de estos detalles en cualquier momento, la **[!UICONTROL función]** no se puede editar después de la configuración inicial. Cuando termine, use **[!UICONTROL Siguiente]** para pasar a la página siguiente y seleccionar las claves de coincidencia que desea que use su organización.

![Área de trabajo de configuración de cuenta con la sección Detalles mostrada y la opción Siguiente resaltada.](/help/assets/setup/manage-account/add-account-details.png){zoomable="yes"}

### Configurar claves de coincidencia {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia son identificadores que se utilizan para reconciliar miembros entre los públicos de diferentes fuentes de datos. Incluya cualquier clave de coincidencia con la que pueda trabajar su marca."

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
>Las claves de coincidencia que seleccione durante la configuración de la cuenta determinarán las claves de coincidencia disponibles para las conexiones que cree con otros colaboradores. Aunque puede quitar las claves de coincidencia durante la configuración de la conexión, no puede agregar nuevas claves de coincidencia. Es importante seleccionar **todas** las claves de coincidencia que planea usar en futuras campañas durante la configuración de la cuenta.

Las claves de coincidencia, como las direcciones de correo electrónico, los ID de dispositivo o los ID de cliente, ayudan a los colaboradores a trabajar juntos, ya que permiten una sincronización de datos precisa y centrada en la privacidad, lo que permite una segmentación y medición de audiencias más precisas.

![Diapositiva que muestra los identificadores disponibles para la primera versión de Collaboration.](/help/assets/setup/manage-account/available-identifiers.png)

<!-- Eventually replace this image above to match branding better. -->

Seleccione las claves de coincidencia que desee utilizar para reconciliar perfiles de audiencia. Incluya cualquier clave de coincidencia con la que pueda trabajar. Planifique el futuro y seleccione las claves de coincidencia que prevé utilizar en campañas futuras. Si necesita seleccionar claves de coincidencia adicionales para su cuenta más adelante, puede hacerlo en el flujo de trabajo [editar cuenta](#edit-account).

Seleccione hasta cinco claves de coincidencia que desee utilizar. Posteriormente, al configurar las conexiones, puede quitar las claves de coincidencia no deseadas, pero no puede agregar nuevas.

Existen tres tipos de claves de coincidencia disponibles:

* ID de personas propios
* ID de dispositivos propios
* ID de socios

>[!IMPORTANT]
>
>Actualmente, la única clave de coincidencia admitida es el correo electrónico con hash.

Cuando esté listo, seleccione **[!UICONTROL Completar]** para finalizar el flujo de trabajo de configuración de la organización.

![Se muestra la sección Configurar el área de trabajo de la organización con la sección Coincidir claves.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Editar cuenta {#edit-account}

Después de configurar la cuenta, puede editar ciertos aspectos y detalles de la cuenta en cualquier momento. Para editar tu cuenta, selecciona **[!UICONTROL Editar]** en la sección **[!UICONTROL Mi cuenta]** del área de trabajo **[!UICONTROL Configuración]**.

![Área de trabajo de instalación con la ficha Mi cuenta y la opción Editar resaltadas.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

Ahora puede editar los detalles de su cuenta, con la excepción de **[!UICONTROL Rol]**. Tenga en cuenta que la región se establece automáticamente en función de su cuenta de Adobe Experience Cloud y no se puede cambiar en ningún momento.

![Cuadro de diálogo Editar detalles de la cuenta.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

También puede actualizar las claves de coincidencia que seleccionó inicialmente al incorporar su organización. Seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Claves de coincidencia]** para agregar las claves de coincidencia adicionales que desee.

![Área de trabajo de instalación con la opción Editar resaltada en la sección Claves de coincidencia de la cuenta.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

## Próximos pasos

Una vez configuradas las cuentas, está listo para [originar audiencias](/help/guide/setup/onboard-audiences.md) en Real-Time CDP Collaboration.
