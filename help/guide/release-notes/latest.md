---
title: Últimas notas de la versión de Real-Time CDP Collaboration
description: Siga las últimas versiones de Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
source-git-commit: 36f43d9d34ce7851a1c7093e0891f9c87e56387c
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 2%

---

# Últimas notas de la versión de Real-Time CDP Collaboration

{{limited-availability-release-note}}

**Última actualización**: agosto de 2025.

Estas notas de la versión abarcan la funcionalidad incluida en Adobe Real-Time CDP Collaboration. Las versiones de Collaboration funcionan con un modelo de entrega continua, que permite una cadencia de versión mensual aproximada. Estas notas de la versión se actualizan con frecuencia, por lo que asegúrese de consultarlas regularmente.

## Agosto de 2025 {#august-2025}

Real-Time CDP Collaboration ya está disponible para los clientes de **Canadá**. Está disponible automáticamente para los clientes de Real-Time CDP Prime y Ultimate en estas regiones.

* Collaboration ahora admite las [claves de coincidencia](../setup/onboard-account.md#supported-match-keys) siguientes:
   * Correo electrónico con hash
   * Número de teléfono con hash
   * ID de CRM
   * ID de lealtad
   * IPv4 con hash
   * ID de AdFixus
* Ahora hay disponibles varias claves de coincidencia en Collaboration, lo que le permite ampliar el tamaño de la audiencia y mejorar las tasas de coincidencia. Se pueden utilizar varias claves de coincidencia al obtener audiencias, establecer conexiones y activar audiencias. Para obtener más información sobre cómo usar varias claves de coincidencia, lee las guías [configurar claves de coincidencia](../setup/onboard-account.md) y [obtención de audiencias](../setup/onboard-audiences.md#map-fields).

>[!IMPORTANT]
>
>Al activar audiencias en las que se utilizan varias claves de coincidencia, si una (o más) clave de coincidencia no se superpone, no se contabiliza la audiencia o cae por debajo del umbral, toda la activación falla. Asegúrese de que las audiencias se superpongan lo suficiente y cumplan el umbral mínimo de 1000 ID en todas las claves de coincidencia antes de activarlas.

* El destino de Adobe Experience Platform ahora admite la activación de audiencias con varias claves de coincidencia. Además, ahora puede utilizar una clave vinculada al configurar la asignación de destino para especificar qué clave de coincidencia se envía durante la activación. Para obtener más información, lee la guía [Experience Platform destination](../destinations/experience-platform.md#linked-keys).
* Los colaboradores ahora pueden editar varias audiencias a la vez. Ahora puede editar metadatos de audiencia, acceso de conexión, nombres, descripciones y categorías para varias audiencias mediante la herramienta de edición masiva. Para obtener más información sobre cómo editar audiencias, lee la guía [administrar audiencias](../setup/onboard-audiences.md#edit-audiences).

## Julio de 2025 {#july-2025}

Real-time CDP Collaboration ahora admite la colaboración de marca a marca. Los colaboradores ahora pueden formar conexiones, independientemente de si son anunciantes o editores. Esto ofrece oportunidades de colaboración más flexibles y permite a las marcas aprovechar los datos y las perspectivas de cada una. Para obtener más información sobre las diferencias entre la colaboración de marca a marca y la colaboración de anunciante a editor, lee la guía [patrones de colaboración](../overview/collaboration-patterns.md).

* Los colaboradores ahora pueden conectarse entre sí usando [invitaciones a conexiones privadas](../connect/establishing-connections.md#private-connection-invites). Comparta el código de conexión único de su cuenta con un colaborador que luego pueda utilizarlo para conectarse directamente con usted. Esta es una característica central de la colaboración de marca a marca, que permite a los colaboradores establecer conexiones más allá de los anunciantes que exploran el directorio **[!UICONTROL Discover colaboradores]**.
* [Los destinos de autoservicio](../setup/manage-destinations.md) ya están disponibles tanto para anunciantes como para editores.
* La activación de audiencia ya está disponible para ambos colaboradores en una conexión, independientemente de su [rol de cuenta](../overview/roles.md). La configuración de activación de audiencias se establece al [establecer conexiones](../connect/establishing-connections.md#configure-connection-settings), lo que le permite especificar qué colaborador puede activar audiencias. Para obtener más información acerca de la activación de audiencias, lea la guía [activar audiencias](../collaborate/activate.md).
* El caso de uso **[!UICONTROL Activar]** se ha reconfigurado para admitir la colaboración de marca a marca. La ficha **[!UICONTROL Activar]** de un proyecto ahora muestra las audiencias que se han enviado a su colaborador y las que su colaborador ha activado en su destino. Para obtener más información, lee la guía [activar audiencias](../collaborate/activate.md). <br> ![El panel Activar con las secciones Audiencias enviadas a y Audiencias activadas.](/help/assets/release-notes/2025/activate-dashboard.png){zoomable="yes"}
* Las puntuaciones del índice de audiencia ahora están disponibles en la pestaña **[!UICONTROL Discover]** de un proyecto. La puntuación del índice de audiencia mide en qué medida una audiencia coincide con la audiencia de su colaborador. Esta puntuación se calcula en función de los recuentos y superposiciones de audiencias subyacentes. Para obtener más información sobre las puntuaciones de índice de audiencia, lea la guía [puntuación de índice de audiencia](../collaborate/discover.md#audience-index-score).

## Mayo de 2025 {#may-2025}

* Real-Time CDP Collaboration ya está disponible para los clientes de **Australia** y **Nueva Zelanda**. Está disponible automáticamente para los clientes de Real-Time CDP Prime y Ultimate en estas regiones.
* Real-Time CDP Collaboration ahora ofrece [destinos de autoservicio](../setup/manage-destinations.md) a través de la ficha **[!UICONTROL Mis destinos]** en la sección **[!UICONTROL Configuración]**. Los destinos le permiten activar audiencias en plataformas de terceros, como redes de publicidad o plataformas de administración de datos, para llegar a sus clientes a través de varios canales. Actualmente, solo se admiten destinos de Adobe Experience Platform. Si le interesa configurar un destino diferente, póngase en contacto con su representante de Adobe. Para obtener más información sobre los destinos, lea la guía [descripción general de destinos](../destinations/overview.md).
   * Los destinos también agregan compatibilidad para ver audiencias de Collaboration en [Adobe Experience Platform audience portal](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences).
* Ahora puede editar la frecuencia de actualización de audiencia para conexiones de datos existentes en Collaboration. Actualmente, puede elegir actualizar las audiencias diariamente o cada dos a seis días. Para obtener más información sobre cómo editar la frecuencia de actualización de la audiencia, lea la guía [administrar conexiones de datos](../setup/manage-data-connection.md#scheduling).
* Las divisiones de crédito entre colaboradores ahora se establecen para cada caso de uso seleccionado dentro de la conexión. Puede establecer diferentes reglas de consumo de crédito para cada caso de uso para controlar mejor cómo se utilizan los créditos. Para obtener más información acerca de la funcionalidad de división de crédito, lee la guía [configuración de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre cómo se consumen los créditos, lea la guía [tipos de actividades de crédito](../setup/my-activity.md#types-of-activities). <br> ![Pantalla de configuración de conexión que muestra la funcionalidad de división de crédito.](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* Los editores ahora pueden establecer nombres e ID de anunciantes antes de aceptar la configuración de conexión de un anunciante. Los editores pueden establecer nombres e ID que se alineen con sus sistemas internos, que pueden ser diferentes de los nombres e ID del anunciante. Para obtener más información sobre cómo agregar nombres e ID de anunciantes, lee la guía [configuración de conexión](../connect/establishing-connections.md#connection-settings.md). <br> ![Pantalla de configuración de conexión que muestra los nombres e ID del anunciante de configuración del publicador.](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## Abril de 2025 {#april-2025}

* Se ha agregado una nueva columna **[!UICONTROL Entradas procesadas]** a la tabla de actividad de consumo de crédito. Esta columna muestra el número total de entradas (por ejemplo, ID o filas) procesadas para cada actividad. [Más información](/help/guide/setup/my-activity.md#inputs-processed). <br> ![Columna de entradas procesadas resaltada en Mi vista de actividad.](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* Se ha añadido una nueva opción de correo electrónico de contacto a la creación de cuentas. Esto ayuda a los colaboradores de los socios a ponerse en contacto con usted según sea necesario durante el proceso de conexión. [Más información](../setup/onboard-account.md).

## Marzo de 2025 {#march-2025}

* Al [obtener audiencias](/help/guide/setup/onboard-audiences.md) en Collaboration, ahora puede establecer una frecuencia de actualización de audiencia de **cada uno a seis días** para administrar mejor la [actividad de crédito de Gestión de público](/help/guide/setup/my-activity.md#types-of-activities). Para obtener más información, lea la guía [administrar audiencias](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences). <br> ![Pantalla de programación que muestra diferentes intervalos de frecuencia para actualizar el abono a audiencia.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png "Pantalla de programación que muestra diferentes intervalos de frecuencia para actualizar la pertenencia a audiencias."){width="250" align="center" zoomable="yes"}
* Al establecer una conexión con un colaborador, ahora puede seleccionar entre **casos de uso** predefinidos. El caso de uso seleccionado determina qué secciones de proyecto y qué funcionalidad del producto están disponibles. Para obtener más información, lea la guía [administrar proyectos](/help/guide/collaborate/manage-projects.md#project-use-cases).
   * *Medición* habilita la sección del proyecto **Medida**.
   * *Detección de audiencias* habilita la sección del proyecto **Discover**.
   * *Activación de audiencia* habilita **Activar** secciones de proyecto <br>
* Ahora puede eliminar conexiones con colaboradores con los que ya no desea trabajar. Para aprender a eliminar conexiones, lea la guía [eliminar conexiones](/help/guide/connect/establishing-connections.md#delete-connections).

## Febrero de 2025 {#february-2025}

Adobe Real-Time CDP Collaboration, creado específicamente para permitir a anunciantes y editores descubrir, activar y medir audiencias de alto valor sin cookies de terceros, ahora está disponible de forma general en Estados Unidos.

### Introducción

1. **Configuración de acceso**: Los administradores del sistema configuran los permisos de acceso para los usuarios. Para obtener más información sobre cómo configurar los permisos de acceso, lea la guía [administrar el acceso de usuario](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access).
2. **Conectar fuentes de datos**: audiencias de Source para usar en Collaboration. Para empezar a obtener audiencias, lea la guía [origen y administrar audiencias](/help/guide/setup/onboard-audiences.md).
3. **Establecer conexiones**: Empiece a colaborar con anunciantes o editores de confianza. Para obtener más información acerca de cómo formar conexiones, lea la guía [establecer conexiones](/help/guide/connect/establishing-connections.md).
4. **Descubrir y activar**: Cree proyectos para identificar audiencias valiosas que activar en las campañas. Para obtener más información sobre cómo crear proyectos, lee la guía [administrar proyectos](/help/guide/collaborate/manage-projects.md).

### Disponibilidad

* Actualmente, Adobe Real-Time CDP Collaboration solo está disponible para los clientes de EE. UU.
* Está disponible automáticamente para los clientes de Adobe Real-Time CDP Prime y Ultimate

Para obtener más información, lea:

* [Información general de Collaboration](/help/guide/home.md)
* [Flujo de trabajo de extremo a extremo](/help/guide/overview/end-to-end-workflow.md)
* [Resumen de permisos](/help/guide/permissions/overview.md)
