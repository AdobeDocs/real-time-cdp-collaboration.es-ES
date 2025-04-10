---
title: Incorporación y administración de la organización
description: Aprenda a incorporar y administrar varios aspectos de su organización en Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 1%

---

# Incorporación y administración de la organización

{{limited-availability-release-note}}

Aprenda a incorporar su organización en Real-Time CDP Collaboration y a administrar varios aspectos de su compañía. Esta página describe los pasos para incorporar una organización a Adobe Real-Time CDP Collaboration, incluida la configuración de las claves de coincidencia, las identidades preferidas y más opciones.

![Página de instalación](/help/assets/setup/manage-organization/my-organization.png)

## Configuración inicial de la organización

Primero debe configurar su organización y los detalles de la organización. Vaya a **[!UICONTROL Configuración]** en el carril izquierdo, seleccione el símbolo **+** en la esquina superior derecha y seleccione **[!UICONTROL Cuenta]**.

>[!TIP]
>
>Después de configurar una cuenta inicial con la que trabajar, puede usar la misma flujo de trabajo para configurar cuentas adicionales dentro de la misma organización.

![Seleccione Cuenta para agregar nueva organización a CDP en tiempo real Colaboración](/help/assets/setup/manage-organization/add-new-account.png)

El flujo de trabajo para configurar la organización incluye las dos páginas siguientes:

* [Detalles de configuración](#set-up-details)
* [Configuración de las claves de coincidencia](#set-up-match-keys)

>[!IMPORTANT]
>
>Las *claves* de coincidencia que seleccione a nivel de organización se filtrarán al nivel](/help/guide/collaborate/manage-projects.md) de [proyecto en la colaboración entre anunciantes y editores. En el nivel de proyecto, usted puede eliminar cualquier clave de coincidencia, pero *no* puede agregar ninguna clave adicional que no se haya seleccionado en el nivel de organización en esta pantalla.

### Configuración de detalles {#set-up-details}

![Los detalles y pasos de casos de uso para configurar una organización](/help/assets/setup/manage-organization/add-organization-details.png)

1. Añada un **[!UICONTROL nombre de organización]** para su compañía.
2. añadir un **[!UICONTROL Descripción]** sobre su compañía.
3. Seleccione el función ]**de la**[!UICONTROL  empresa. Puede seleccionar entre **[!UICONTROL Anunciante]** y **[!UICONTROL Publicador]**. Lea el [documento de flujo de trabajo de extremo a extremo](/help/guide/end-to-end-workflow.md) para ver similitudes y pequeñas diferencias en el flujo de trabajo entre los dos tipos de funciones organizativas.
4. Seleccione el **[!UICONTROL sector]** de su organización. Algunos ejemplos son **[!UICONTROL Retail]**, **[!UICONTROL Telecomunicaciones]** o **[!UICONTROL Servicios financieros]**.
5. Seleccione la **[!UICONTROL región]** de su organización. En la versión actual del producto, **[!UICONTROL Norteamérica]** es la selección predeterminada preestablecida.
6. <span class="preview"> de sólo editor</span>: al configurar una organización de editor, debe leer y reconocer que los anunciantes del catálogo de editores podrán detectarlo.
   ![Mensaje de inclusión específico del publicador.](/help/assets/setup/manage-organization/publisher-specific-optin-message.png)
7. Cargue un **[!UICONTROL logotipo]** para su compañía. Actualmente, se admiten imágenes de tipo SVG.
8. Seleccione una imagen para la imagen del encabezado de la empresa.

Cuando esté satisfecho con su selección, use **[!UICONTROL Siguiente]** para continuar a la página siguiente y seleccionar las claves de coincidencia que su organización debería usar.

### Configuración de claves de coincidencia {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia son identificadores que sirven para reconciliar miembros entre audiencias de distintos orígenes de datos. Incluya cualquier clave de coincidencia con la que pueda trabajar el compañía."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="ID de personas de origen"
>abstract="Los identificadores de personas de origen, como direcciones correo electrónico o números de teléfono con hash, están conectados directamente a un perfil individual. Los ID admitidos actualmente son correos electrónicos y números de teléfono con hash."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="ID de dispositivos propios"
>abstract="Los ID de dispositivos de origen, como ECID o direcciones IP, se conectan directamente a los dispositivos, que pueden compartirse entre varias personas. IPv4 es el único ID de dispositivo de origen compatible actualmente."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="ID de socios admitidos"
>abstract="Los ID de socio asociados con perfiles amplían el alcance a un perfil determinado."

Las claves coincidentes, como las direcciones de correo electrónico, los ID de dispositivos o los ID de clientes, ayudan a los anunciantes y editores a trabajar juntos al permitir una sincronización de datos precisa y compatible con la privacidad, lo que permite una direccionamiento y medición de audiencia más precisas.

![Diapositiva que muestra los identificadores disponibles para la primera versión de Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Seleccione las claves de coincidencia que desee utilizar para reconciliar a los miembros de las audiencias de editor y anunciante. Incluya cualquier clave de coincidencia con la que pueda trabajar su compañía. Planifique el futuro y seleccione las claves de coincidencia que prevé utilizar en futuras campañas de editor-anunciante. Si necesita seleccionar claves de coincidencia adicionales para su organización, también puede hacerlo más adelante, en el flujo de trabajo [editar organización](#edit-organization).

![Paso de selección de claves coincidentes.](/help/assets/setup/manage-organization/add-organization-match-keys.png)

Seleccione hasta cinco claves de coincidencia que desee utilizar. Posteriormente, al configurar las conexiones, puede quitar las claves de coincidencia no deseadas, pero no puede agregar nuevas. Defina el umbral de recuento de identidades (recuento mínimo) para cada clave de coincidencia seleccionada. Las claves de coincidencia con menos del recuento mínimo no aparecerán en los desgloses de identidad para algunos casos de uso.

Las claves de coincidencia disponibles en la colaboración de CDP en tiempo real pueden ser de tres tipos:

* ID de personas de origen
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

![Editar control de organización resaltado.](/help/assets/setup/manage-organization/edit-organization.png)

En este punto, puede actualizar el nombre de la organización, la descripción, el logotipo y la imagen del perfil de la organización.

![Opciones editables para organizaciones.](/help/assets/setup/manage-organization/editable-options.png)

También puede actualizar las claves de coincidencia seleccionadas inicialmente al incorporar su organización, así como el umbral mínimo de identidades correspondientes a claves de coincidencia para que sean visibles y utilizables en superposiciones de audiencias y otras áreas de producto. Seleccione **[!UICONTROL Editar]** en la ficha **[!UICONTROL Claves de coincidencia]** para agregar las claves de coincidencia adicionales que desee o actualizar los umbrales de identidad.

![Editar claves de coincidencia](/help/assets/setup/manage-organization/edit-match-keys.png)

## Pasos siguientes

Después de configurar su organización, está listo para [importar audiencias](/help/guide/setup/onboard-audiences.md) en Real-Time CDP Collaboration.
