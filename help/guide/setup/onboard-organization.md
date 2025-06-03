---
title: Incorporación y administración de la organización
description: Aprenda a incorporar y administrar varios aspectos de su organización en Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 19%

---

# Incorporación y administración de la organización

{{limited-availability-release-note}}

Aprenda a incorporar su organización en Real-Time CDP Collaboration y a administrar varios aspectos de su compañía. Esta página describe los pasos para incorporar una organización a Adobe Real-Time CDP Collaboration, incluida la configuración de las claves de coincidencia, las identidades preferidas y más opciones.

![Página de instalación](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## Configuración inicial de la organización

Primero debe configurar su organización y los detalles de la organización. Vaya a **[!UICONTROL Configuración]** en el carril izquierdo, seleccione el símbolo **+** en la esquina superior derecha y seleccione **[!UICONTROL Cuenta]**.

>[!TIP]
>
>Después de configurar una cuenta inicial para trabajar con, puede utilizar el mismo flujo de trabajo para configurar cuentas adicionales dentro de la misma organización.

![Seleccione la cuenta para agregar una nueva organización a Real-Time CDP Collaboration](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

El flujo de trabajo para configurar su organización incluye las dos páginas siguientes:

* [Configuración de detalles](#set-up-details)
* [Configurar claves de coincidencia](#set-up-match-keys)

>[!IMPORTANT]
>
>Las *claves de coincidencia* que seleccione en el nivel de organización se filtrarán al [nivel de proyecto](/help/guide/collaborate/manage-projects.md) en colaboración entre anunciantes y editores. En el nivel de proyecto, usted puede eliminar cualquier clave de coincidencia, pero *no* puede agregar ninguna clave adicional que no se haya seleccionado en el nivel de organización en esta pantalla.

### Configuración de detalles {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="Correo electrónico de contacto"
>abstract="Proporcione un correo electrónico basado en roles o en equipos, como `collaboration@yourcompany.com`. No se deben utilizar direcciones de correo electrónico personales o individuales."

![Los detalles y pasos de casos de uso para configurar una organización](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

1. Añada un **[!UICONTROL nombre de organización]** para su compañía.
2. Agrega una **[!UICONTROL descripción]** sobre tu compañía.
3. Seleccione su **[!UICONTROL rol de compañía]**. Puede seleccionar entre **[!UICONTROL Anunciante]** y **[!UICONTROL Publicador]**. Lea el [documento de flujo de trabajo de extremo a extremo](/help/guide/end-to-end-workflow.md) para ver similitudes y pequeñas diferencias en el flujo de trabajo entre los dos tipos de funciones organizativas.
4. Seleccione el **[!UICONTROL sector]** de su organización. Algunos ejemplos son **[!UICONTROL Retail]**, **[!UICONTROL Telecomunicaciones]** o **[!UICONTROL Servicios financieros]**.
5. Seleccione la **[!UICONTROL región]** de su organización. En la versión actual del producto, **[!UICONTROL Norteamérica]** es la selección predeterminada preestablecida.
6. Agregue un **[!UICONTROL correo electrónico de contacto]** para su organización. Debe ser una dirección de correo electrónico basada en el equipo o en la función. No se deben proporcionar direcciones de correo electrónico personales.
7. Cargue un **[!UICONTROL logotipo]** para su compañía. Actualmente, se admiten imágenes de tipo SVG.
8. Seleccione una imagen para la imagen del encabezado de la empresa.

Cuando esté satisfecho con su selección, use **[!UICONTROL Siguiente]** para continuar a la página siguiente y seleccionar las claves de coincidencia que su organización debería usar.

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

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_matchkeys"
>title="Claves de coincidencia de activación"
>abstract="Las claves de coincidencia de activación se muestran según las claves de coincidencia seleccionadas por su organización."

Las claves de coincidencia, como las direcciones de correo electrónico, los ID de dispositivo o los ID de cliente, ayudan a los anunciantes y editores a trabajar juntos, ya que permiten una sincronización de datos precisa y centrada en la privacidad, lo que permite una segmentación y medición de audiencias más precisas.

![Diapositiva que muestra los identificadores disponibles para la primera versión de Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Seleccione las claves de coincidencia que desee utilizar para reconciliar a los miembros de las audiencias de editor y anunciante. Incluya cualquier clave de coincidencia con la que pueda trabajar su compañía. Planifique el futuro y seleccione las claves de coincidencia que prevé utilizar en futuras campañas de editor-anunciante. Si necesita seleccionar claves de coincidencia adicionales para su organización, también puede hacerlo más adelante, en el flujo de trabajo [editar organización](#edit-organization).

![Paso de selección de claves coincidentes.](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

Seleccione hasta cinco claves de coincidencia que desee utilizar. Posteriormente, al configurar las conexiones, puede quitar las claves de coincidencia no deseadas, pero no puede agregar nuevas.

Las claves de coincidencia disponibles en Real-Time CDP Collaboration pueden ser de tres tipos:

* ID de personas propios
* ID de dispositivos propios
* ID de socios

Las claves de coincidencia disponibles para la primera versión de Real-Time CDP Collaboration son:

* Correo electrónico con hash

<!--

not available in the Limited GA release

* Hashed phone
* IPv4

-->

Cuando esté listo, seleccione **[!UICONTROL Completar]** para finalizar el flujo de trabajo de configuración de la organización.

## Editar organización {#edit-organization}

Después de configurar inicialmente la organización, puede editar en cualquier momento ciertos aspectos y detalles de la organización. Para editar tu organización, selecciona **[!UICONTROL Editar]** en la vista **[!UICONTROL Mi organización]**.

![Editar control de organización resaltado.](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

En este punto, puede actualizar el nombre de la organización, la descripción, el logotipo y la imagen del perfil de la organización.

![Opciones editables para organizaciones.](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

También puede actualizar las claves de coincidencia seleccionadas inicialmente al incorporar su organización, así como el umbral mínimo de identidades correspondientes a claves de coincidencia para que sean visibles y utilizables en superposiciones de audiencias y otras áreas de producto. Seleccione **[!UICONTROL Editar]** en la ficha **[!UICONTROL Claves de coincidencia]** para agregar las claves de coincidencia adicionales que desee o actualizar los umbrales de identidad.

![Editar claves de coincidencia](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## Pasos siguientes

Después de configurar su organización, está listo para [importar audiencias](/help/guide/setup/onboard-audiences.md) en Real-Time CDP Collaboration.
