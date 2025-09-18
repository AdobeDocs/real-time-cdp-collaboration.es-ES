---
title: Establecimiento de conexiones
description: Después de descubrir colaboradores potenciales, aprenda a establecer conexiones y a comenzar a colaborar en proyectos.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: 899b6c2a0111ccaebbaf2818772e1d743d6de914
workflow-type: tm+mt
source-wordcount: '3400'
ht-degree: 6%

---

# Establecimiento de conexiones {#establishing-connections}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="Comparar públicos"
>abstract="Compare su audiencia con todos los consumidores a los que llegan sus anuncios de Amazon."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="Públicos relevantes"
>abstract="Segmentos de segmentación de Amazon en los que la audiencia tiene la mayor superposición teniendo en cuenta solo las impresiones de DSP (estos segmentos solo pueden segmentarse en DSP)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="ID resueltos"
>abstract="El número de ID que la resolución de identidad de Amazon pudo resolver con sus datos de audiencia."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="ID superpuestos y expuestos"
>abstract="Representa el número de &quot;ID resueltos&quot; de la audiencia cargada que también se han expuesto a un anuncio a través de Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="% de solapamiento"
>abstract="La proporción de &quot;ID resueltos&quot; que se han expuesto a un anuncio a través de Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Desglose por Amazon y producto"
>abstract="Desglose de los &quot;ID superpuestos y expuestos&quot; alcanzados por el producto patrocinado por Amazon Ads o por Amazon Ads DSP."

{{limited-availability-release-note}}

Para que los colaboradores puedan trabajar juntos en las campañas, deben establecer una conexión. Esta conexión les permite activar audiencias, crear proyectos y ejecutar informes sobre el rendimiento de la campaña.

Las conexiones se establecen en función del patrón de colaboración elegido. Collaboration admite dos patrones de colaboración clave: de anunciante a editor y de marca a marca. Para obtener más información sobre estos patrones, consulte la guía [casos de uso](/help/guide/overview/use-cases.md).

Para aprender a establecer una conexión, lea la sección siguiente que corresponde a su patrón de colaboración:

- [Conexión de anunciante a editor](#advertiser-to-publisher-connection)
- [Conexión entre marcas](#brand-to-brand-connection)

## Conexión de anunciante a editor {#advertiser-to-publisher-connection}

![Diagrama de alto nivel del proceso de conexión anunciante-editor.](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

En el patrón de anunciante a editor, un anunciante descubre un publicador con el que desea trabajar a través del área de trabajo de **[!UICONTROL Discover publicadores]** y envía una invitación de conexión. A continuación, el editor revisa la invitación y la acepta, lo que permite al anunciante proponer la configuración de conexión. Una vez que el editor acepta la configuración de conexión, esta se establece y ambos colaboradores pueden empezar a trabajar juntos en los proyectos.

### Información general de alto nivel

Para establecer una conexión entre un anunciante y un editor, se deben seguir los siguientes pasos:

1. [Descubrir editores](#discover-publishers): El anunciante identifica editores potenciales con los que colaborar.
1. [Enviar invitación](#send-invite): El anunciante envía una invitación de conexión al editor seleccionado.
1. [Aceptar invitación](#accept-invite): El editor revisa y acepta la invitación.
1. [Configurar opciones de conexión](#configure-connection-settings): el anunciante configura las opciones de conexión y las envía al editor para que las revise.
1. [Confirmar configuración de conexión](#establish-connection): el editor revisa la configuración de conexión y la acepta o la rechaza. Si se acepta, se establece la conexión. Si se rechaza, el publicador puede proporcionar comentarios sobre las revisiones fuera del producto. El anunciante puede revisar la configuración y reenviarla para su revisión.

Una vez aceptada la configuración de conexión, se establece la conexión y los colaboradores están listos para [crear un proyecto](/help/guide/collaborate/manage-projects.md#create-project) para comenzar a colaborar en las campañas.

## Conexión entre marcas {#brand-to-brand-connection}

![Diagrama de alto nivel del proceso de conexión de marca a marca.](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>El término **brand** se usa para referirse a una compañía o marca fuera de Collaboration. El término **colaborador** hace referencia a cualquier cuenta que pueda formar una conexión en Collaboration, independientemente de si es un anunciante o un editor.

En el patrón de marca a marca, dos marcas que se han comunicado fuera del producto pueden conectarse directamente en Collaboration mediante una [invitación de conexión privada](#private-connection-invite). Una marca puede ser un anunciante o un editor. Este patrón es especialmente útil para marcas que pueden no ajustarse al modelo tradicional de anunciante-editor, como dos anunciantes o dos editores.

Para empezar, un colaborador envía una invitación de conexión privada a otro colaborador. El destinatario revisa la invitación y la acepta, lo que permite al propietario proponer la configuración de conexión. Una vez que el destinatario acepta la configuración de conexión, esta se establece y ambos colaboradores pueden empezar a trabajar juntos en los proyectos.

### Información general de alto nivel

>[!TIP]
>
>Al discutir el proceso de conexión, habrá una distinción entre **propietario** y **destinatario**. El propietario es el colaborador que inicia la conexión enviando la invitación, mientras que el destinatario es el colaborador que recibe y revisa la invitación.

El proceso de conexión entre dos marcas implica varios pasos. Antes de que comience el proceso de conexión, se deben cumplir algunos requisitos previos:

1. Dos marcas se comunican fuera del producto para discutir la posible conexión.
1. Las marcas [crean cuentas](/help/guide/setup/onboard-account.md) en Collaboration si aún no lo han hecho, asegurándose de seleccionar el tipo de rol apropiado (anunciante o editor).

   Una vez cumplidos los requisitos previos, puede comenzar el proceso de conexión. Los siguientes pasos describen el proceso:

1. [Enviar invitación a una conexión privada](#send-private-connection-invite): Un colaborador envía una invitación a otra conexión privada.
1. [Aceptar invitación a conexión privada](#accept-private-connection-invite): El destinatario revisa y acepta la invitación a conexión privada.
1. [Configurar opciones de conexión](#configure-connection-settings): El propietario configura las opciones de conexión y las envía al destinatario para que las revise y las acepte.
1. [Confirmar configuración de conexión](#establish-connection): El destinatario revisa la configuración de conexión y la acepta o la rechaza.

Una vez aceptada la configuración de conexión, se establece la conexión y los colaboradores están listos para [crear un proyecto](/help/guide/collaborate/manage-projects.md#create-project) para comenzar a colaborar en las campañas.

## Conectar {#connect}

El área de trabajo **[!UICONTROL Connect]** es donde puedes administrar tus conexiones con los colaboradores, enviar invitaciones de conexión y donde los anunciantes pueden examinar el directorio del editor. El espacio de trabajo de se divide en dos pestañas principales:

### Descubrir editores {#discover-publishers}

>[!IMPORTANT]
>
>Solo los anunciantes pueden descubrir editores mediante el espacio de trabajo **[!UICONTROL Discover publishers]**. Para obtener más información sobre cómo conectar con colaboradores independientemente de su función, lea la sección [conexión de marca a marca](#brand-to-brand-connection).

Para descubrir editores, ve al espacio de trabajo de **[!UICONTROL Discover publishers]** en la pestaña **[!UICONTROL Connect]**. Aquí puede examinar la lista de editores disponibles mediante los controles de paginación situados en la parte inferior del espacio de trabajo. Para obtener más información sobre el área de trabajo de **[!UICONTROL Discover publishers]**, consulte la guía [Discover publishers](/help/guide/connect/discover-publishers.md).

![El área de trabajo de Discover publishers muestra una lista de editores disponibles.](/help/assets/connect/establish-connection/discover-publishers.png){zoomable="yes"}

### Enviar invitación {#send-invite}

>[!IMPORTANT]
>
>En esta sección se describe el proceso por el que los anunciantes envían invitaciones de conexión a los editores a través del espacio de trabajo **[!UICONTROL Discover publishers]**. Para obtener información sobre cómo formar conexiones entre marcas independientemente de sus funciones, lea la sección [conexión de marca a marca](#brand-to-brand-connection) o visite la sección [invitación de conexión privada](#private-connection-invite).

Una vez que haya identificado un editor con el que desee colaborar, seleccione la opción **[!UICONTROL Conectar]** en la tarjeta de editor. Esta acción inicia el proceso de conexión.

![La opción Conectar resaltada en un editor específico del área de trabajo de Discover publishers.](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

Aparece un cuadro de diálogo que le solicita que envíe una invitación de conexión al editor. Seleccione **[!UICONTROL Enviar invitación]** para continuar.

![Cuadro de diálogo Enviar invitación de conexión con el botón Enviar invitación resaltado.](/help/assets/connect/establish-connection/send-connection-invite-dialog.png){zoomable="yes"}

>[!NOTE]
>
>Si desea conectarse con un editor con el que se ha comunicado fuera del producto, puede utilizar la opción de invitación de conexión privada. Para obtener más información, consulte la sección [invitación a una conexión privada](#private-connection-invite).

La invitación pendiente se muestra en la ficha **[!UICONTROL Mis conexiones]** de la sección **[!UICONTROL Acción necesaria]**. El estado de la conexión aparece como **[!UICONTROL Invitación enviada]**. Puede obtener una vista previa de la configuración de conexión seleccionando **[!UICONTROL Vista previa de la conexión]**, pero no podrá editarla hasta que el editor acepte la invitación.

![La conexión pendiente se muestra en el área de trabajo Mis conexiones en la sección Acción necesaria.](/help/assets/connect/establish-connection/preview-connection.png){zoomable="yes"}

### Invitación de conexión privada {#private-connection-invite}

Las invitaciones a conexiones privadas le permiten conectarse con colaboradores con los que se ha comunicado fuera del producto mediante **[!UICONTROL Conectar código]**. Para formar una conexión privada, debes obtener el **[!UICONTROL código Connect]** del colaborador con el que deseas conectarte fuera del producto. A continuación, puede usar este código para enviar una invitación de conexión privada al colaborador en el área de trabajo **[!UICONTROL Connect]**.

#### Código de conexión {#connect-code}

Para poder enviar una invitación a una conexión privada, el colaborador que quieras debe proporcionarte su **[!UICONTROL código de conexión]** único. Para buscar y copiar tu **[!UICONTROL código Connect]**, ve a la ficha **[!UICONTROL Mi cuenta]** en el área de trabajo de **[!UICONTROL Configuración]**. El **[!UICONTROL código Connect]** se muestra en los detalles de la cuenta.

![La ficha Mi cuenta del área de trabajo de instalación con el código de Connect resaltado.](/help/assets/connect/establish-connection/connect-code.png){zoomable="yes"}

Seleccione el icono de copiar (![icono de copiar](/help/assets/icons/copy.png)) junto al **[!UICONTROL código de conexión]** para copiarlo en el portapapeles. A continuación, puede compartir este código con su colaborador fuera del producto.

![Código de conexión con el icono de copia resaltado.](/help/assets/connect/establish-connection/copy-connect-code.png){zoomable="yes"}

##### Actualización del código de conexión {#refresh-connect-code}

Puedes actualizar tu **[!UICONTROL código Connect]** en cualquier momento. Al actualizar el código, se genera un nuevo código único que puede compartir con los colaboradores. Esto resulta útil si desea invalidar el código anterior por motivos de seguridad. Cualquier conexión establecida con el código antiguo permanecerá activa, pero los nuevos colaboradores deberán utilizar el nuevo código para conectarse con usted.

>[!IMPORTANT]
>
>Si actualiza tu **[!UICONTROL código de conexión]** durante una invitación pendiente, es posible que no se acepte la invitación. Si actualiza el código, es posible que el colaborador tenga que reenviar la invitación de conexión privada utilizando el nuevo código.

Para actualizar tu **[!UICONTROL código Connect]**, selecciona el icono de actualización (![icono de actualización](/help/assets/icons/refresh.png)) junto al **[!UICONTROL código Connect]**.

![Código de conexión con el icono de actualización resaltado.](/help/assets/connect/establish-connection/refresh-connect-code.png){zoomable="yes"}

>[!IMPORTANT]
>
>Las cuentas creadas antes de que se introdujera la característica **[!UICONTROL Connect code]** no tendrán un código de conexión generado y el campo de conexión se mostrará como **[!UICONTROL No disponible]**. Utilice la opción de actualización para generar un nuevo código de conexión.

#### Enviar invitación de conexión privada {#send-private-connection-invite}

Una vez que tengas el **[!UICONTROL código Connect]** de tu colaborador, puedes enviar una invitación a una conexión privada. Para ello, vaya al área de trabajo **[!UICONTROL Connect]** y seleccione el icono de signo más (![icono de signo más](/help/assets/icons/plus.png)) en la esquina superior derecha.

![Icono de signo más resaltado en el área de trabajo de Connect.](/help/assets/connect/establish-connection/private-connection-invite.png){zoomable="yes"}

Aparece el cuadro de diálogo **[!UICONTROL Conectar]**, que le solicita que escriba el **[!UICONTROL código de conexión]** del colaborador con el que desea conectarse. Pegue el código en el campo de texto y seleccione **[!UICONTROL Continuar]** para continuar.

![Se ha rellenado el cuadro de diálogo Conectar con el campo Código de conexión y se ha resaltado la opción Continuar.](/help/assets/connect/establish-connection/private-connection-invite-connect.png){zoomable="yes"}

El cuadro de diálogo **[!UICONTROL Conectar]** mostrará el colaborador con el que está asociado el código, lo que le permitirá confirmar que se está conectando con el colaborador correcto. Si el colaborador es correcto, seleccione **[!UICONTROL Conectar]** para enviar la invitación de conexión privada.

![Cuadro de diálogo Conectar con los detalles del colaborador mostrados y la opción Conectar resaltada.](/help/assets/connect/establish-connection/private-connection-invite-connect-confirm.png){zoomable="yes"}

### Aceptar invitación {#accept-invite}

>[!TIP]
>
>Al discutir el proceso de conexión, habrá una distinción entre **propietario** y **destinatario**. El propietario es el colaborador que inicia la conexión enviando la invitación, mientras que el destinatario es el colaborador que recibe y revisa la invitación.

Para que el propietario pueda establecer la configuración de conexión, el destinatario debe aceptar la invitación de conexión. Para ello, vaya al área de trabajo **[!UICONTROL Connect]** y busque la conexión pendiente en la sección **[!UICONTROL Acción necesaria]**. El estado de la conexión aparece como **[!UICONTROL Invitación recibida]**. Seleccione **[!UICONTROL Aceptar]** para aceptar la invitación.

![Se muestra la conexión pendiente en la sección Acción necesaria del área de trabajo Conectar con la opción Aceptar resaltada.](/help/assets/connect/establish-connection/accept-connection.png){zoomable="yes"}

El cuadro de diálogo le pedirá que acepte la invitación. Seleccione **[!UICONTROL Aceptar invitación]** para continuar.

![Cuadro de diálogo Aceptar invitación a la conexión con la opción Aceptar invitación resaltada.](/help/assets/connect/establish-connection/accept-connection-invite.png){zoomable="yes"}

El estado de la conexión cambia a **[!UICONTROL Pendiente]**. El propietario ahora puede establecer la configuración de conexión.

### Configurar opciones de conexión {#configure-connection-settings}

La configuración de conexión define los términos entre dos colaboradores. Esta configuración incluye casos de uso, claves de coincidencia, división de crédito y acuerdos legales. Los colaboradores que se conectan con anunciantes también pueden agregar nombres de anunciantes a la configuración de conexión, que se utilizará al crear proyectos.

Una vez que el destinatario acepta la invitación, el propietario puede configurar los ajustes de conexión. Para ello, vaya a **[!UICONTROL Mis conexiones]** y busque la conexión pendiente en la sección **[!UICONTROL Acción necesaria]**. Seleccione **[!UICONTROL Configurar conexión]** para establecer la configuración de conexión.

![El área de trabajo Connect con la opción Set up connection resaltada en la sección Action required.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Aparecerá el área de trabajo de configuración de conexión, que le permitirá configurar las distintas opciones de configuración de la conexión.

![Espacio de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/connection-set-up.png){zoomable="yes"}

#### Configuración de conexión {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Casos de uso"
>abstract="Los casos de uso se rellenan previamente con todas las opciones. Puede editar los casos de uso antes de enviar la configuración de conexión."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia se rellenan previamente con claves de coincidencia comunes que usted y su colaborador han seleccionado en el nivel de cuenta. Puede desactivar cualquier clave de coincidencia que no desee utilizar en esta conexión."
>additional-url="https://experienceleague.adobe.com/es/docs/real-time-cdp-collaboration/using/setup/onboard-account#set-up-match-keys" text="Claves de coincidencia de cuenta"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="División de crédito"
>abstract="Esta sección determina quién paga las actividades correspondientes dentro de Collaboration. "

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Uso compartido de públicos"
>abstract="Los créditos de activación del público se consumen en función del número de ID coincidentes preparados para la activación."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Medición"
>abstract="Ejecutar actividades para generar informes y análisis sobre el rendimiento de las campañas. Los créditos se consumen en función del número de filas de los informes de campaña de todas las campañas y la frecuencia de los informes (diariamente, cada tres días o semanalmente)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Nombres de anunciantes"
>abstract="<p>Configuración opcional. Indica el nombre y el ID mediante los cuales el editor conoce al anunciante.</p><p>El nombre del anunciante que añada aquí se rellenará previamente en el paso de creación del proyecto.</p><ul><li>Si el editor configuró varios nombres, seleccione uno de la lista.</li><li>Si solo se ha configurado un nombre, se seleccionará automáticamente de antemano.</li><li>Si no se han configurado nombres, el campo se rellenará previamente con el nombre de cuenta del anunciante de Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/es/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Crear un proyecto"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_activation"
>title="Activación del público"
>abstract="La activación del público permite seleccionar qué colaborador puede iniciar la activación del público."

Puede configurar las siguientes opciones de conexión:

##### Activación del público {#audience-activation}

>[!IMPORTANT]
>
>Cualquier conexión creada antes de que se introdujera la característica **[!UICONTROL activación de audiencia]** tendrá automáticamente la configuración de activación de audiencia establecida en el propietario de la conexión. Si deseas permitir que ambos colaboradores activen audiencias, necesitarás [eliminar tu conexión actual](#delete-connections) y crear una nueva con la configuración actualizada.

La activación de audiencias permite seleccionar qué colaborador puede activar audiencias dentro de la conexión. La activación de audiencias solo será una opción si se selecciona el caso de uso **[!UICONTROL Activación de audiencias]**. Si elige quitar el caso de uso durante el proceso de conexión, la configuración de activación de audiencia se eliminará de la configuración de conexión. Para obtener más información acerca de la activación de audiencias, consulte la guía [activar](/help/guide/collaborate/activate.md).

Para configurar la activación de audiencia, seleccione **[!UICONTROL Configurar]** en la sección **[!UICONTROL Activación de audiencia]**. Utilice el menú desplegable para especificar qué colaborador puede activar audiencias. Puede elegir un solo colaborador o permitir que ambos activen audiencias.

![Cuadro de diálogo de activación de Audiencia con opciones en el área de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/audience-activation.png){zoomable="yes"}

Cuando termines, selecciona **[!UICONTROL Guardar]** para guardar los cambios.

![Cuadro de diálogo de activación de Audiencia con la opción Guardar en el área de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/audience-activation-confirm.png){zoomable="yes"}

##### Casos de uso {#use-cases}

Los casos de uso se rellenan automáticamente con todas las opciones disponibles. Los casos de uso seleccionados determinan qué vistas y opciones están disponibles en sus proyectos. Para obtener más información, lea la guía [casos de uso del proyecto](/help/guide/collaborate/manage-projects.md#project-use-cases).

Para personalizar los casos de uso, seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Casos de uso]** y desactive los que no desee incluir en ningún proyecto con su colaborador. Cuando termines, selecciona **[!UICONTROL Guardar]** para guardar los cambios.

![La configuración de casos de uso en el área de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

##### Claves de coincidencia {#match-keys}

>[!IMPORTANT]
>
>Al activar audiencias en las que se utilizan varias claves de coincidencia, si una (o más) clave de coincidencia no se superpone, no se contabiliza la audiencia o cae por debajo del umbral, toda la activación falla. Asegúrese de que las audiencias se superpongan lo suficiente y cumplan el umbral mínimo de 1000 ID en todas las claves de coincidencia antes de activarlas.

Las claves de coincidencia se rellenan automáticamente con las claves de coincidencia comunes que usted y su colaborador seleccionaron al [configurar sus cuentas](/help/guide/setup/onboard-account.md#set-up-match-keys). Solo aparecerán las claves de coincidencia que usted y el colaborador seleccionado **y** tengan en común.

![Área de trabajo de configuración de conexión con la sección Claves de coincidencia resaltada que muestra las claves de coincidencia comunes.](/help/assets/connect/establish-connection/auto-populated-match-keys.png){zoomable="yes"}

Cuando el propietario de la conexión está configurando la configuración de conexión, puede [editar las claves de coincidencia de la cuenta](../setup/onboard-account.md#edit-match-keys) para incluir claves de coincidencia adicionales. Después de activar más claves de coincidencia en la configuración de la cuenta, dichas claves de coincidencia estarán disponibles para activarse en la configuración de conexión si su colaborador también las ha seleccionado. Las claves de coincidencia agregadas una vez iniciado el proceso de conexión no se rellenarán automáticamente y deben activarse manualmente.

Para personalizar las claves de coincidencia, seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Claves de coincidencia]** y desactive las claves de coincidencia que no desee usar en esta conexión. Cuando termines, selecciona **[!UICONTROL Guardar]** para guardar los cambios.

![Se abre el área de trabajo de configuración de conexión con el cuadro de diálogo de sección Claves de coincidencia que muestra una clave de coincidencia desactivada.](/help/assets/connect/establish-connection/additional-match-key-selected.png){zoomable="yes"}

>[!IMPORTANT]
>
>Una vez que el colaborador haya aceptado la configuración de conexión, las claves de coincidencia se bloquearán y no se podrán cambiar.

##### División de crédito {#credit-split}

Utilice la sección de división de crédito para determinar cuál de las dos partes colaboradoras cubrirá los costes de las actividades. Las opciones de división de crédito están determinadas por los casos de uso seleccionados para la conexión. Aunque el caso de uso **[!UICONTROL Medición]** requiere que una parte cubra los costos, el caso de uso **[!UICONTROL Activación - Coincidencia]** proporciona una opción adicional para que cada parte cubra sus propios costos. Para obtener información sobre el desglose de costos, lea la guía [tipos de actividades de crédito](/help/guide/setup/my-activity.md#types-of-activities).

>[!NOTE]
>
>Audiencia: la salida siempre está cubierta por el colaborador que recibe la audiencia, por lo que no se requiere ninguna selección.

Para configurar la división de crédito, seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL División de crédito]**. A continuación, puede seleccionar las opciones adecuadas para cada caso de uso. Cuando termines, selecciona **[!UICONTROL Guardar]** para guardar los cambios.

![Cuadro de diálogo de división de crédito con opciones en el área de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}

##### Nombres de anunciantes {#advertiser-names}

>[!NOTE]
>
>Esta opción puede aparecer durante la configuración de la conexión o la revisión de la configuración de la conexión, según el usuario que inicie la conexión.

Si es un editor que establece una conexión con un anunciante, puede elegir agregar nombres de anunciantes en la configuración de conexión. Esto le permite agregar varios nombres por los que el anunciante es conocido por usted en sus sistemas. Esto resulta especialmente útil si el anunciante tiene presencia en varias regiones geográficas o si se les conoce por nombres diferentes en contextos diferentes. Posteriormente, al crear un proyecto, puede seleccionar el nombre del anunciante adecuado en la lista de nombres configurados en la configuración de conexión.

![Nombres del anunciante en el área de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/advertiser-names.png){zoomable="yes"}

Para agregar nombres de anunciantes, seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Nombres de anunciantes]**. A continuación, puede escribir el **[!UICONTROL ID del anunciante]** que el anunciante conoce como en su sistema, y un **[!UICONTROL nombre del anunciante]** para asociarlo a ese ID en Collaboration. Puede agregar varios nombres de anunciantes seleccionando la opción **[!UICONTROL Agregar]**.

![Cuadro de diálogo Nombres del anunciante con opciones en el área de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/advertiser-names-dialog.png){zoomable="yes"}

Cuando termines, selecciona **[!UICONTROL Guardar]** para guardar los cambios.

Al crear un proyecto, el nombre del anunciante se rellena previamente en función de la siguiente configuración establecida durante la conexión    :

1. **Sin conjunto de nombres de anunciante**: Si no se agregan nombres de anunciante, Collaboration usa de manera predeterminada el nombre del anunciante como nombre del anunciante.
2. **Un conjunto de nombres de anunciante**: Si se agrega un solo nombre de anunciante, Collaboration lo usará automáticamente como nombre de anunciante para el proyecto.
3. **Conjunto de varios nombres de anunciante**: Si se agrega más de un nombre de anunciante, usted o su colaborador pueden seleccionar cualquiera de los nombres proporcionados al crear el proyecto.

>[!NOTE]
>
> Una vez enviada la configuración de conexión, ya no puede añadir ni editar nombres de anunciantes.

![Se ha completado el área de trabajo de configuración de conexión con la sección Nombres de anunciantes.](/help/assets/connect/establish-connection/add-advertiser-names.png)

Una vez que haya realizado sus selecciones, seleccione **[!UICONTROL Enviar]** para enviar la configuración sugerida al destinatario para que la revise.

### Revisar configuración de conexión {#review-connection-settings}

A continuación, el destinatario debe revisar la configuración de conexión propuesta por el propietario. El destinatario puede hacerlo navegando a la ficha **[!UICONTROL Mis conexiones]** en el área de trabajo de **[!UICONTROL Connect]**. La conexión se mostrará en la sección **[!UICONTROL Acción necesaria]**. Seleccione **[!UICONTROL Revisar configuración de conexión]** para revisar la configuración de conexión propuesta.

![Se resaltó el área de trabajo Mis conexiones con la opción Revisar configuración de conexión.](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

Revise la configuración que ha propuesto el colaborador. Puede aceptar o rechazar la configuración de conexión. Si rechaza la configuración de conexión, deberá comunicarse con el colaborador acerca de los cambios que desee realizar fuera del producto. La información de contacto del colaborador se muestra en la sección **[!UICONTROL Contacto]** del área de trabajo de configuración de conexión. El propietario puede revisar la configuración de conexión y reenviarla para su revisión.

![Espacio de trabajo de configuración de conexión con la opción Aceptar y rechazar resaltada.](/help/assets/connect/establish-connection/accept-connection-settings.png){zoomable="yes"}

Además, si es un editor que se conecta con un anunciante, ahora puede agregar nombres de anunciantes en la configuración de conexión. Para obtener más información sobre este proceso, consulte la sección [configuración de conexión](#connection-settings).

>[!NOTE]
>
> Una vez que haya aceptado la configuración de conexión, ya no podrá agregar ni editar nombres de anunciantes.

A continuación, seleccione **[!UICONTROL Aceptar]** para continuar con la conexión. El estado de la conexión cambiará a **[!UICONTROL Activa]** y ahora podrá empezar a colaborar en proyectos.

## Eliminación de conexiones {#delete-connections}

Puede eliminar cualquier conexión con colaboradores con los que no desee seguir trabajando. Para eliminar las conexiones existentes, ve a **[!UICONTROL Connect]**. Como editor, se mostrará la conexión existente. Como anunciante, deberías ir a **[!UICONTROL Mis conexiones]**.

Seleccione **[!UICONTROL Ver conexión]** en la tarjeta de conexión que desee eliminar.

![La opción Ver conexión resaltada en la vista Mis conexiones.](/help/assets/connect/establish-connection/delete-view-connection.png){zoomable="yes"}

Seleccione el icono de eliminación ![eliminar icono](/help/assets/common/delete.svg) en el área de trabajo de conexión para eliminar la conexión.

![Icono de eliminación resaltado en el área de trabajo de conexión.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

Aparecerá un cuadro de diálogo de confirmación en el que se le pedirá que confirme la eliminación de la conexión. Seleccione **[!UICONTROL Eliminar]** para confirmar la eliminación.

![Cuadro de diálogo de confirmación para eliminar una conexión.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Una vez eliminada la conexión, todos los proyectos existentes en la colaboración se eliminarán de forma permanente y no se recuperarán. La solicitud de conexión permanecerá en un estado pendiente, pero la conexión y sus configuraciones dejarán de estar activas. Deberá restablecer la conexión si desea volver a conectarse con el colaborador.

## Próximos pasos

Después de establecer una conexión con su colaborador, usted y su colaborador ahora pueden [crear proyectos](/help/guide/collaborate/manage-projects.md#create-project).
