---
title: Configuración y administración de la cuenta
description: Obtenga información sobre cómo configurar y administrar varios aspectos de su cuenta en Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 0dead396657c97cec47ddd64c8ec3c349f541a8f
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 14%

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

Para comenzar a configurar la cuenta, primero debe configurar los detalles de la cuenta. Esto requiere que agregue la siguiente información:

* Agregue un **[!UICONTROL nombre de cuenta]** que represente claramente su marca.
* Agrega una **[!UICONTROL descripción]** sobre tu marca. Esto es opcional, pero ayuda a otros colaboradores a comprender mejor su marca.
* Seleccione su **[!UICONTROL rol]**. Puede seleccionar entre **[!UICONTROL Anunciante]** y **[!UICONTROL Publicador]**. Lea la guía [funciones](/help/guide/overview/roles.md) para ver similitudes y pequeñas diferencias en el flujo de trabajo entre los dos tipos de funciones de cuenta.
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
>abstract="Las claves de coincidencia son identificadores que se utilizan para reconciliar perfiles de públicos de diferentes fuentes de datos. Incluya cualquier clave de coincidencia con la que pueda trabajar su marca."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_setup_match_keys"
>title="claves de coincidencia"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="ID de personas propios"
>abstract="Los ID de personas propios, como las direcciones de correo electrónico, los números de teléfono con hash, o los ID de CRM, están conectados directamente a un perfil individual. "

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="ID de dispositivos propios"
>abstract="Los ID de dispositivos propios, como las direcciones ECID o IP, se conectan directamente a los dispositivos, que pueden compartirse entre varias personas. IPv4 es el único ID de dispositivo propio compatible actualmente."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="ID de socios compatibles"
>abstract="Los ID de socio son identificadores proporcionados por socios externos para la reconciliación de públicos. Los ID de socio no están conectados directamente a un perfil individual."

![Claves de coincidencia admitidas.](/help/assets/setup/manage-account/match-keys.png){zoomable="yes"}

>[!IMPORTANT]
>
>Las claves de coincidencia que seleccione durante la configuración de la cuenta determinarán las claves de coincidencia disponibles en las conexiones. Aunque puede [eliminar las claves de coincidencia no deseadas](../connect/establishing-connections.md#connection-settings) durante la configuración de la conexión, las claves de coincidencia no se pueden agregar después de establecer una conexión. Es importante que seleccione **todas** las claves de coincidencia que planea usar en futuras campañas durante la configuración de la cuenta.

Las claves de coincidencia ayudan a los colaboradores a trabajar juntos ya que permiten una sincronización de datos precisa y centrada en la privacidad, lo que permite una segmentación y medición de audiencias más precisas. Las claves de coincidencia seleccionadas durante la configuración de la cuenta determinarán qué claves de coincidencia están disponibles en conexiones futuras. También se usan para [asignar campos](./onboard-audiences.md#map-fields) desde la conexión de datos a los campos de destino en Collaboration al obtener audiencias.

Seleccione las claves de coincidencia que desee utilizar para reconciliar perfiles de audiencia. Planifique el futuro e incluya cualquier clave de coincidencia con la que pueda trabajar y anticipar su uso en campañas futuras. Si necesita seleccionar claves de coincidencia adicionales para su cuenta más adelante, puede hacerlo en el flujo de trabajo [editar cuenta](#edit-account). Sin embargo, las claves de coincidencia agregadas después de la configuración inicial no estarán disponibles para su uso en conexiones existentes.

#### Claves de coincidencia admitidas {#supported-match-keys}

Collaboration admite tres tipos de claves de coincidencia: ID de personas de origen, ID de dispositivos de origen e ID de socios. Todas las claves de coincidencia deben cumplir los siguientes requisitos:

* Las claves de coincidencia deben estar **recortadas**, **en minúsculas**
* Las claves de coincidencia con hash deben ser **SHA256-hashed**.
* Si proporciona valores hash con caracteres en mayúsculas, Collaboration los convierte automáticamente a minúsculas.
* Si el origen contiene **identificadores de texto sin formato**, use la opción **[!UICONTROL Aplicar transformación]** durante la configuración de la conexión de datos [para aplicar el hash. &#x200B;](./manage-data-connection.md#match-keys) Esta opción solo está disponible cuando obtiene audiencias de Experience Platform y no es compatible con fuentes basadas en la nube.

##### ID de personas propios

Los ID de personas de origen están conectados directamente a un perfil individual. Los ID admitidos actualmente son:

* **[!UICONTROL Correo electrónico con hash]**
* **[!UICONTROL Teléfono con hash]**
* **[!UICONTROL ID de CRM]**
* **[!UICONTROL ID de fidelización]**
<!-- * **[!UICONTROL Custom ID]**: Custom identifiers -->

##### ID de dispositivos propios

Los ID de dispositivos de origen son identificadores conectados a un dispositivo específico. Los ID admitidos actualmente son:

* **[!UICONTROL IPv4 con hash]**: Direcciones IPv4 con hash

##### ID de socios

Los ID de socio son identificadores proporcionados por socios externos para la reconciliación de públicos. Los ID admitidos actualmente son:

* **[!UICONTROL Id. Adfixus]**

>[!NOTE]
>
>La integración de Adobe con [!DNL Adfixus] asigna los [!UICONTROL identificadores de archivo adjunto] únicos para cada cuenta a un formato común codificado en Adobe. Estas asignaciones se utilizan para identificar superposiciones entre colaboradores. Al activar audiencias con **[!UICONTROL Id. de prefijo]**, se usan los identificadores originales. El formato con codificación Adobe nunca abandona Collaboration.

Al seleccionar **[!UICONTROL ID de prefijo]**, deberá proporcionar el ID correspondiente de su socio externo en la sección **[!UICONTROL Credenciales de cuenta]**. Esta opción solo estará disponible *después de que* active **[!UICONTROL Adfixus ID]**. Introduzca su ID de Adfixus en el campo **[!UICONTROL ID de cuenta]**, asegurándose de comprobar el valor para comprobar su precisión.

![El cuadro de diálogo Coincidir claves con el identificador de Adfixus está activado y la sección Credenciales de cuenta resaltada.](/help/assets/setup/manage-account/adfixus-settings.png){zoomable="yes"}

Una vez que haya seleccionado todas las claves de coincidencia deseadas, seleccione **[!UICONTROL Completar]** para finalizar el flujo de trabajo de configuración de la cuenta.

![Área de trabajo Configurar cuenta con la sección Claves de coincidencia mostrada.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Editar cuenta {#edit-account}

Después de configurar la cuenta, puede editar los detalles y las claves de coincidencia en cualquier momento.

### Editar detalles {#edit-details}

Puede editar la mayoría de los detalles de su cuenta en cualquier momento, excepto la **[!UICONTROL Función]**. La región se establece automáticamente en función de su cuenta de Adobe Experience Cloud y no se puede cambiar.

Para editar tu cuenta, selecciona **[!UICONTROL Editar]** en la sección **[!UICONTROL Mi cuenta]** del área de trabajo **[!UICONTROL Configurar]**.

![Área de trabajo de instalación con la ficha Mi cuenta y la opción Editar resaltadas.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

Ahora puede editar los detalles de su cuenta. Actualice los campos que desee cambiar y, a continuación, seleccione **[!UICONTROL Guardar]** para confirmar los cambios.

![Cuadro de diálogo Editar detalles de la cuenta.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

### Editar claves de coincidencia {#edit-match-keys}

>[!IMPORTANT]
>
>La edición de las claves de coincidencia no afectará a las conexiones existentes. Una vez establecida una conexión, se corrigen las claves de coincidencia seleccionadas durante la configuración de la conexión. Es importante que seleccione **todas** las claves de coincidencia que planea usar en futuras campañas durante la configuración de la cuenta.

También puede actualizar las claves de coincidencia que seleccionó inicialmente al crear su cuenta. Estas claves de coincidencia determinarán las claves de coincidencia disponibles para conexiones futuras.

Seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Claves de coincidencia]**.

![Área de trabajo de instalación con la opción Editar resaltada en la sección Claves de coincidencia de la cuenta.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Claves de coincidencia]**. Activa y desactiva cualquier clave de coincidencia, o actualiza tu **[!UICONTROL ID de cuenta]** para tus [!UICONTROL ID de Adfixus] y, a continuación, selecciona **[!UICONTROL Guardar]** para confirmar los cambios.

>[!IMPORTANT]
>
>Si cambia su [!UICONTROL Id. de Adfixus], no se almacenará en déclencheur una actualización de [boceto de datos](../glossary.md#sketches) para las conexiones de datos existentes mediante la clave de coincidencia. Una vez que se hayan esbozado los datos, cualquier cambio en su [!UICONTROL ID de Adfixus] no se reflejará hasta que se actualice la próxima audiencia según la configuración de [programación de conexión de datos](./manage-data-connection.md#scheduling). Si necesita realizar cambios antes de la próxima actualización, puede eliminar y volver a crear la conexión de datos.

![Cuadro de diálogo Coincidir claves con la opción Guardar resaltada.](/help/assets/setup/manage-account/match-key-dialog.png){zoomable="yes"}

## Próximos pasos

Una vez configuradas las cuentas, está listo para [originar audiencias](/help/guide/setup/onboard-audiences.md) en Real-Time CDP Collaboration.
