---
title: Configuración de Adobe Experience Platform como destino
description: Obtenga información sobre cómo configurar y administrar Adobe Experience Platform como destino en Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
source-git-commit: 0dead396657c97cec47ddd64c8ec3c349f541a8f
workflow-type: tm+mt
source-wordcount: '1489'
ht-degree: 11%

---

# Configuración de Adobe Experience Platform como destino

{{limited-availability-release-note}}

Configure este destino para activar audiencias de su proyecto a Adobe Experience Platform. La activación de audiencias en Adobe Experience Platform le permite aprovechar las capacidades de la plataforma para la segmentación de audiencias, el análisis y la activación en varios canales de marketing. Para obtener más información sobre Adobe Experience Platform, consulte la [descripción general de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/home){target="_blank"}.

>[!WARNING]
>
>No se puede actualizar un destino una vez creado. Si necesita cambiar alguna configuración, debe eliminar el destino existente y crear uno nuevo.

## Configurar destino {#configure-destination}

Para configurar Adobe Experience Platform como destino, vaya a **[!UICONTROL Configuración]** y luego seleccione la pestaña **[!UICONTROL Mis destinos]**. Seleccione **[!UICONTROL Configurar]** para Adobe Experience Platform.

![Área de trabajo Mis destinos con la opción de configuración resaltada para el destino de Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

Aparece el flujo de trabajo **[!UICONTROL Crear destino]**.

![Flujo de trabajo Crear destino para Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### Configurar zona protegida {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="Caducidad del público"
>abstract="Período de tiempo después del cual el público ya no estará disponible en Adobe Experience Platform. La caducidad predeterminada es de 30 días, pero se puede establecer en cualquier valor entre 1 y 30 días."

En primer lugar, debe seleccionar la zona protegida a la que se enviarán los datos de audiencia.

>[!IMPORTANT]
>
>Solo puede seleccionar una zona protegida a la que el usuario tenga acceso. De manera predeterminada, todos los usuarios de Collaboration tienen acceso a la zona protegida **Prod**. Para obtener acceso a zonas protegidas adicionales, un administrador debe agregar zonas protegidas adicionales a una función asignada al usuario. Para obtener más información sobre la administración de funciones, consulte la guía [administrar funciones](../permissions/manage-roles.md).

En la sección **[!UICONTROL Configurar zona protegida]**, seleccione la lista desplegable **[!UICONTROL Zona protegida]** o escriba el nombre de una zona protegida.

![Lista desplegable de espacio aislado resaltada en el flujo de trabajo Crear destino.](/help/assets/destinations/adobe-experience-platform/select-sandbox.png)

También puede seleccionar **[!UICONTROL Examinar espacio aislado]** para ver todos los espacios aislados disponibles, así como su **[!UICONTROL Tipo]**, **[!UICONTROL Estado]** y **[!UICONTROL Región]**. Seleccione la zona protegida que desee usar y, a continuación, seleccione **[!UICONTROL Guardar]**.

A continuación, configure **[!UICONTROL Caducidad de audiencia]**. De forma predeterminada, la caducidad de la audiencia se establece en 30 días. Puede elegir establecer la caducidad en cualquier momento entre 1 y 30 días. Una vez superada la fecha de caducidad, la audiencia ya no estará disponible en Adobe Experience Platform.

![La sección Caducidad de audiencia resaltada en el flujo de trabajo Crear destino.](/help/assets/destinations/adobe-experience-platform/audience-expiration.png)

### Crear asignación de activación {#create-activation-mapping}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_matchkeys"
>title="Claves de coincidencia de activación"
>abstract="Las claves de coincidencia de activación se muestran según las claves de coincidencia seleccionadas al crear la organización."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_mapping"
>title="Más información"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Espacios de nombres de destino"
>abstract="Los espacios de nombres de destino especifican a qué espacio de nombres de identidad se asigna la clave de coincidencia en Adobe Experience Platform. Las claves de coincidencia con hash deben asignarse a un espacio de nombres de destino que admita valores con hash."

Todas las claves de coincidencia habilitadas para su cuenta se incluyen en la asignación de activación de forma predeterminada. Si no desea asignar directamente una clave de coincidencia a un área de nombres de destino, puede utilizar la opción de clave vinculada para reemplazarla con una clave de coincidencia diferente. Para obtener más información sobre las claves vinculadas, consulte la [sección siguiente](#linked-keys).

#### Asignar áreas de nombres de destino {#map-target-namespaces}

Para asignar cada clave de coincidencia a un área de nombres de destino, seleccione el campo **[!UICONTROL Áreas de nombres de destino]** junto a la clave de coincidencia. Aparecerá el cuadro de diálogo **[!UICONTROL Seleccionar campo de origen]**. Busque el área de nombres de destinatario en la lista o busque un área de nombres específica. Seleccione el área de nombres de destino que desee usar para la clave de coincidencia y, a continuación, seleccione **[!UICONTROL Seleccionar]**.

>[!IMPORTANT]
>
>Las claves de coincidencia con hash deben asignarse a un área de nombres de destino que admita valores con hash. Por ejemplo, la clave de coincidencia **[!UICONTROL Correo electrónico con hash]** debe asignarse al área de nombres de identidad **[!UICONTROL Correo electrónico(SHA256, en minúsculas)]** en Adobe Experience Platform. No puede asignar la clave de coincidencia **[!UICONTROL Hash email]** al área de nombres de identidad **[!UICONTROL Email]**, ya que este área de nombres no admite valores hash.

![Cuadro de diálogo Seleccionar campo de origen con la opción Seleccionar resaltada..](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

Repita este proceso para cada clave de coincidencia que desee incluir en la asignación de activación. Si no desea incluir una clave de coincidencia, puede eliminarla o utilizar la opción de clave vinculada para reemplazarla con una clave de coincidencia diferente.

#### Claves vinculadas {#linked-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_linked_key"
>title="Clave vinculada"
>abstract="Las claves vinculadas permiten especificar que se debe utilizar una clave de coincidencia diferente en lugar de la clave de coincidencia original durante la activación. Para activar un perfil, debe tener valores tanto para la clave de coincidencia original como para la clave de coincidencia vinculada."

Las claves vinculadas permiten especificar que se debe utilizar una clave de coincidencia diferente en lugar de la clave de coincidencia original durante la activación. Para comprender mejor cómo funcionan las claves vinculadas, vea el siguiente ejemplo:

Un retailer desea enviar los datos que se están activando a Experience Platform a su sistema CRM. Retailer ha habilitado la IP con hash como clave de coincidencia para su cuenta a fin de aumentar la tasa de coincidencia al activar audiencias. Sin embargo, el sistema CRM de retailer no admite IP con hash como área de nombres de identidad, por lo que desean utilizar la clave de coincidencia de ID de CRM en su lugar al activar audiencias en Experience Platform. Retailer puede utilizar la opción de clave vinculada para activar audiencias en Experience Platform mediante un ID de CRM en lugar de una IP con hash.

>[!NOTE]
>
>Para activar un perfil, debe tener valores tanto para la clave de coincidencia original como para la clave de coincidencia vinculada. Por ejemplo, si el ID con hash está vinculado al ID de CRM, un perfil debe tener valores para que se activen el ID con hash y el ID de CRM. Si falta alguno de los valores, el perfil no se activa.

Para usar una clave vinculada, active la opción **[!UICONTROL Clave vinculada]** junto a la clave de coincidencia que desee usar en su lugar. La sección **[!UICONTROL Clave vinculada]** aparece pidiéndole que cree la asignación.

![La opción Clave vinculada y la sección resaltadas en el flujo de trabajo Crear destino.](/help/assets/destinations/adobe-experience-platform/linked-key.png)

Seleccione la **[!UICONTROL clave vinculada]** que desee usar en el menú desplegable. Siguiendo el ejemplo anterior, retailer seleccionaría **[!UICONTROL CRM ID]** como clave vinculada.

![La lista desplegable Clave vinculada resaltada en el flujo de trabajo Crear destino.](/help/assets/destinations/adobe-experience-platform/select-linked-key.png)

A continuación, desea especificar el área de nombres de destino para la clave vinculada si aún no lo ha hecho. Si ya ha seleccionado el área de nombres de destino para la clave de coincidencia en la sección **[!UICONTROL Crear asignación de activación]**, esto se rellenará automáticamente. Si todavía no ha seleccionado un área de nombres de destino para la clave vinculada, puede hacerlo ahora.

Seleccione el campo **[!UICONTROL Áreas de nombres de destino]** junto a la clave vinculada. Aparecerá el cuadro de diálogo **[!UICONTROL Seleccionar campo de origen]**. Busque el área de nombres de destinatario en la lista o busque un área de nombres específica. Seleccione el área de nombres de destino que desee usar para la clave vinculada y, a continuación, seleccione **[!UICONTROL Seleccionar]**.

![Cuadro de diálogo Seleccionar campo de origen.](/help/assets/destinations/adobe-experience-platform/select-linked-key-target-namespace.png)

La clave vinculada ya está configurada.

>[!NOTE]
>
>Solo se puede utilizar un área de nombres de destino de clave vinculada por asignación de activación. Por ejemplo, si vincula un ID con hash a un ID de CRM, al activar la opción de clave vinculada para otro campo, también se vinculará al ID de CRM.

Cuando haya terminado de asignar todas las claves de coincidencia, revise la configuración. La sección **[!UICONTROL Vista previa]** proporciona un resumen de su configuración.

![La sección Vista previa en el flujo de trabajo Crear destino.](/help/assets/destinations/adobe-experience-platform/preview.png)

>[!IMPORTANT]
>
>Actualmente, cada clave de coincidencia se activa en Experience Platform como una audiencia independiente. Por ejemplo, si tiene [!UICONTROL Correo electrónico con hash] y [!UICONTROL Teléfono con hash] como claves de coincidencia, se crearán dos audiencias independientes en Audience Portal cuando se active una audiencia.

Cuando esté satisfecho con la configuración, seleccione **[!UICONTROL Crear destino]**. Aparecerá un mensaje de confirmación que indica que el destino se ha creado correctamente.

## Uso de Adobe Experience Platform como destino

Una vez que hayas configurado Experience Platform como destino, puedes empezar a [activar audiencias](../collaborate/activate.md) en la plataforma a través de tus proyectos. Actualmente, el proceso de activación es un proceso de un solo paso iniciado por el colaborador. Por ejemplo, cuando un anunciante activa una audiencia, se envía al destino preconfigurado del editor (Experience Platform). El editor no necesita realizar ningún paso adicional para enviar la audiencia al destino. Lo mismo ocurre con el patrón de colaboración entre marcas.

>[!IMPORTANT]
>
>Usted **debe** configurar Experience Platform como destino *antes* de que su colaborador active una audiencia. Si el destino no está configurado, la audiencia se le enviará y será visible en la ficha **[!UICONTROL Activar]** dentro de un proyecto, pero no se activará en Experience Platform.

Una vez activada la audiencia, estará disponible en [Audience Portal](#audience-portal) en Experience Platform con Real-Time CDP Collaboration como origen.  Estas audiencias se pueden usar en campañas y participación de clientes.

### Portal de públicos {#audience-portal}

Ahora que ha configurado Adobe Experience Platform como destino, puede ver las audiencias activadas en el Portal de audiencias. Audience Portal es un concentrador central dentro de Adobe Experience Platform que le permite ver y administrar sus audiencias. Audience Portal ahora proporciona Real-Time CDP Collaboration como origen al filtrar las audiencias.

>[!IMPORTANT]
>
>Usted es responsable de aplicar las etiquetas de uso de datos necesarias a las audiencias que active en Adobe Experience Platform. Para obtener más información, consulte la guía [etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

![El portal de audiencia con Real-Time CDP Collaboration como origen en las opciones de filtro.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Para obtener más información sobre Audience Portal, consulte la guía [Información general de Audience Portal](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"}.
