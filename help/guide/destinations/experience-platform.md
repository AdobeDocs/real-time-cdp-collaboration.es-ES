---
title: Configuración de Adobe Experience Platform como destino
description: Obtenga información sobre cómo configurar y administrar Adobe Experience Platform como destino en Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
source-git-commit: 4ef7f8c7c27935f0e5b3620da63e7129f2714b37
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 11%

---

# Configuración de Adobe Experience Platform como destino

{{limited-availability-release-note}}

Configure este destino para activar audiencias de su proyecto a Adobe Experience Platform. La activación de audiencias en Adobe Experience Platform le permite aprovechar las capacidades de la plataforma para la segmentación de audiencias, el análisis y la activación en varios canales de marketing. Para obtener más información sobre Adobe Experience Platform, consulte la [descripción general de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/home){target="_blank"}.

## Configurar destino {#configure-destination}

Para configurar Adobe Experience Platform como destino, vaya a **[!UICONTROL Configuración]** y luego seleccione la pestaña **[!UICONTROL Destinos]**. Seleccione **[!UICONTROL Configurar]** para Adobe Experience Platform.

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
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Espacios de nombres de destino"
>abstract="Los espacios de nombres de destino especifican a qué espacio de nombres de identidad se asigna la clave de coincidencia en Adobe Experience Platform. Las claves de coincidencia con hash deben asignarse a un espacio de nombres de destino que admita valores con hash."

A continuación, debe crear una asignación de activación para definir cómo se enviarán los datos de audiencia a Adobe Experience Platform. Puede asignar cada [clave de coincidencia](../setup/onboard-account.md#set-up-match-keys) que seleccionó al crear su organización a un área de nombres de destino. Las áreas de nombres de destino especifican a qué [área de nombres de identidad](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} se asignará la clave de coincidencia en Adobe Experience Platform.

>[!IMPORTANT]
>
>Las claves de coincidencia con hash deben asignarse a un área de nombres de destino que admita valores con hash. Por ejemplo, la clave de coincidencia **[!UICONTROL Correo electrónico con hash]** debe asignarse al área de nombres de identidad **[!UICONTROL Correo electrónico(SHA256, en minúsculas)]** en Adobe Experience Platform. No puede asignar la clave de coincidencia **[!UICONTROL Hash email]** al área de nombres de identidad **[!UICONTROL Email]**, ya que este área de nombres no admite valores hash.

Seleccione el campo **[!UICONTROL Áreas de nombres de destino]** junto a cada clave de coincidencia. Aparecerá el cuadro de diálogo **[!UICONTROL Seleccionar campo de origen]**. Busque el área de nombres de destinatario en la lista o busque un área de nombres específica. Seleccione el área de nombres de destino que desee usar para la clave de coincidencia y, a continuación, seleccione **[!UICONTROL Seleccionar]**.

![Cuadro de diálogo Seleccionar campo de origen con la opción Seleccionar resaltada..](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

Cuando hayas terminado de asignar todas las claves de coincidencia, revisa tu configuración y selecciona **[!UICONTROL Crear]** para terminar de crear tu destino.

## Uso de Adobe Experience Platform como destino

Una vez que hayas configurado Adobe Experience Platform como destino, puedes empezar a [activar audiencias](../collaborate/activate.md) en la plataforma a través de tus proyectos. Actualmente, el proceso de activación es un proceso de un solo paso iniciado por el anunciante. Cuando el anunciante activa una audiencia, esta se envía al destino preconfigurado del editor (en este caso, Adobe Experience Platform). El editor no necesita realizar ningún paso adicional para enviar la audiencia al destino.

>[!IMPORTANT]
>
>Usted **debe** configurar Adobe Experience Platform como destino *antes* de que su colaborador active una audiencia. Si el destino no está configurado, la audiencia se le enviará y será visible en la ficha **[!UICONTROL Activar]** dentro de un proyecto, pero no se activará en Adobe Experience Platform.

Una vez activada la audiencia, estará disponible en [Audience Portal](#audience-portal) en Experience Platform con Real-Time CDP Collaboration como origen.  Estas audiencias se pueden usar en campañas y participación de clientes.

### Audience Portal {#audience-portal}

Ahora que ha configurado Adobe Experience Platform como destino, puede ver las audiencias activadas en el Portal de audiencias. Audience Portal es un concentrador central dentro de Adobe Experience Platform que le permite ver y administrar sus audiencias. Audience Portal ahora proporciona Real-Time CDP Collaboration como origen al filtrar las audiencias.

>[!IMPORTANT]
>
>Usted es responsable de aplicar las etiquetas de uso de datos necesarias a las audiencias que active en Adobe Experience Platform. Para obtener más información, consulte la guía [etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

![El portal de audiencia con Real-Time CDP Collaboration como origen en las opciones de filtro.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Para obtener más información sobre Audience Portal, consulte la guía [Información general de Audience Portal](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"}.
