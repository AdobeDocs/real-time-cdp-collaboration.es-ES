---
title: Conéctate con anunciantes o editores
description: Después de descubrir posibles colaboradores, aprende a establecer conexiones y inicio colaborar en proyectos.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: 81cedb2a06d930734b1f97304de82d450c06bf79
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 1%

---

# Conectar con anunciantes o editores

{{limited-availability-release-note}}

Establecer una conexión entre dos partes de un colaboración (más comúnmente un anunciante y un publicador) es el requisito previo en la colaboración de CDP en tiempo real para las empresas que trabajan juntas en campañas. Tanto los editores como los anunciantes pueden establecer conexiones. La parte que inicie la conexión será después la *conexión propietario*.

## flujo de trabajo de alto nivel

En un nivel alto, para establecer una conexión entre un anunciante y un publicador, el flujo de trabajo se ve gustar abajo:

1. El anunciante [busca en los editores y descubre uno con el](/help/guide/connect/discover-publishers.md) que gustar trabajar
2. El anunciante envía una invitación de conexión.
3. El editor acepta la invitación.
4. El anunciante envía la configuración de conexión, incluidas las claves de coincidencia y otras. Esta configuración de conexión representa los términos internos del producto de colaboración.
5. El editor acepta la configuración de conexión. Si lo desea, el editor puede rechazar la configuración de conexión inicial y solicitar que el anunciante envíe la configuración de conexión revisada.

![Diagrama de alto nivel del proceso de conexión anunciante-editor.](/help/assets/connect/establish-connection/advertiser-publisher-connection-process.png){zoomable="yes"}

Una vez completados los elementos anteriores, los colaboradores pueden [crear un proyecto](/help/guide/collaborate/manage-projects.md#create-project) para [ejecutar informes de superposición](/help/guide/collaborate/discover.md) y poner en marcha campañas publicitarias.

>[!IMPORTANT]
>
>Una vez establecida la conexión entre dos colaboradores, la configuración de conexión ya no se puede revisar.

## Enviar invitación {#send-invite}

Para configurar una conexión, selecciona **[!UICONTROL Conectar]** al examinar el inventario de editores en la pantalla Detectar editores.

![Selector de conexión](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

En este punto, la invitación ha salido y puede previsualización la configuración de conexión, pero no puede editarla. Puede vista la invitación pendiente en el **[!UICONTROL pestaña Mis conexiones]** . El estado de la conexión es **[!UICONTROL Invitación enviada]**.

![Se ha enviado una invitación pendiente al editor que aparece en la vista Mis conexiones.](/help/assets/connect/establish-connection/pending-invite-sent.png){zoomable="yes"}

Una vez que el colaborador acepta la invitación, puede configurar los ajustes de conexión y enviarlos al colaborador para que los revise y acepte.

## Configuración de conexión {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Casos de uso"
>abstract="Los casos de uso se rellenan previamente con todas las opciones. Puede editar los casos de uso antes de enviar la configuración de conexión."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia se rellenan previamente con las que ha seleccionado a nivel de organización. Puede desactivar cualquier clave de coincidencia que no desee utilizar en este contexto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="División de crédito"
>abstract="Esta sección determina quién paga las actividades correspondientes dentro de Real-Time CDP Collaboration. Actualmente, solo se puede configurar el caso de uso compartido de audiencia."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Uso compartido de audiencias"
>abstract="Compartir audiencias es la actividad que una parte realiza al solicitar que su socio de colaboración active sus datos coincidentes."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Acuerdo legal"
>abstract="Compruebe que existe un acuerdo de uso compartido de datos entre las dos partes."

Una vez enviada la invitación, puede obtener una vista previa de la configuración de conexión. La invitación debe ser aceptada antes de que pueda finalizar la configuración de la conexión.

![Vista de configuración de conexión en estado de vista previa.](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

Una vez que su colaborador ha aceptado la conexión, puede empezar a configurar los ajustes de conexión para la conexión. La configuración de conexión define los términos de su colaboración, como los casos de uso que realizará conjuntamente, las claves de coincidencia que utilizará en los proyectos, etc.

Para establecer y compartir la configuración de conexión con tu colaborador, ve a **[!UICONTROL Mis conexiones]**. Para cualquier conexión con el estado **[!UICONTROL Pendiente]**, puede seleccionar **[!UICONTROL Configurar conexión]** para configurar las opciones de conexión.

![La vista Mis conexiones con una conexión pendiente y su opción Configuración de conexión resaltada.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Puede editar y definir los campos siguientes:

![Configurar vista de conexión](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++Casos de uso

Los casos de uso se rellenan previamente con todos los casos de uso disponibles. Puede elegir los casos de uso que usará su conexión seleccionando **[!UICONTROL Editar]** y desactivando los casos de uso que no desee. Los casos de uso seleccionados afectarán a las vistas y opciones que estén [disponibles en sus proyectos](../collaborate/manage-projects.md#project-use-cases).

![Casos de uso](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Claves coincidentes

Las claves de coincidencia se rellenan previamente con las que [seleccionó en el nivel organizativo](/help/guide/setup/onboard-organization.md#set-up-match-keys). Puede desactivar cualquier clave de coincidencia que no desee utilizar en esta conexión, pero no puede añadir ninguna clave de coincidencia que no estuviera seleccionada al configurar la organización.

![Claves coincidentes](/help/assets/connect/establish-connection/match-keys.png)

+++

+++División de crédito

Utilice la sección de división de crédito para determinar cuál de las dos partes colaboradoras cubrirá los costes de las actividades.

![División de crédito](/help/assets/connect/establish-connection/edit-billing-ownership.png)

+++

+++Acuerdos

Antes de continuar con esta conexión, debe reconocer que existe un acuerdo de uso compartido de datos entre las dos partes.

![Acuerdos legales.](/help/assets/connect/establish-connection/legal-agreement.png)

+++

Después de realizar la selección, seleccione **[!UICONTROL Enviar]** para enviar la configuración sugerida a su colaborador para su revisión.

Si su colaborador le propone una configuración de conexión, puede **[!UICONTROL aceptar]** o **[!UICONTROL rechazar]** dicha configuración. Antes de aceptar la configuración de conexión, debe reconocer y confirmar que existe un acuerdo legal entre usted y el colaborador. Si está rechazando la configuración de conexión, póngase en contacto con su colaborador fuera del producto y hable de cómo deben revisar la configuración de conexión para que usted la acepte.

## Eliminación de conexiones {#delete-connections}

Puede eliminar cualquier conexión con colaboradores con los que no desee seguir trabajando. Para eliminar conexiones existentes:

1. Vaya a **[!UICONTROL Conectar]** > **[!UICONTROL Mis conexiones]**.
2. Seleccione **[!UICONTROL Ver conexión]** en el tarjeta de conexión para acceder a la conexión que desea eliminar.
3. Seleccione el icono ![](/help/assets/common/delete.svg) de eliminación para que aparezca el cuadro de diálogo de confirmación de conexión de eliminación.
   ![Eliminar icono de conexión resaltado.](/help/assets/connect/establish-connection/delete-icon-highlighted.png){zoomable="yes"}
4. Confirme la eliminación seleccionando **[!UICONTROL Eliminar]**.
   ![Diálogo para confirmar la eliminación de una conexión. ](/help/assets/connect/establish-connection/delete-connection-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Una vez eliminada la conexión, ya no estará conectado con el colaborador y todos los proyectos existentes que formen parte de la colaboración se eliminarán de forma permanente y no se recuperarán.

## Pasos siguientes

Después de establecer una conexión con su colaborador, usted y su colaborador ahora pueden [crear proyectos](/help/guide/collaborate/manage-projects.md#create-project).
