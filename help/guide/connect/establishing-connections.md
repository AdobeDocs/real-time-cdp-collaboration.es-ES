---
title: Conectar con anunciantes o editores
description: Después de descubrir colaboradores potenciales, aprenda a establecer conexiones y a comenzar a colaborar en proyectos.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: cc74b26091a4f764e200c9cae91316492874551a
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 12%

---

# Conectar con anunciantes o editores

{{limited-availability-release-note}}

El establecimiento de una conexión entre dos partes de una colaboración (por lo general, un anunciante y un editor) es el requisito previo en Real-Time CDP Collaboration para que las compañías trabajen juntas en campañas. Los editores y anunciantes pueden configurar conexiones. Cualquiera de las partes que inicie la conexión será posteriormente el *propietario de la conexión*.

## Flujo de trabajo de alto nivel

En un nivel superior, para establecer una conexión entre un anunciante y un editor, el flujo de trabajo tiene el siguiente aspecto:

1. El anunciante [explora a los editores y descubre](/help/guide/connect/discover-publishers.md) uno con el que les gustaría trabajar
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

En este punto, la invitación no está disponible y puede obtener una vista previa de la configuración de conexión, pero no puede editarla. Puede ver la invitación pendiente en la ficha **[!UICONTROL Mis conexiones]**. El estado de la conexión es **[!UICONTROL Se envió la invitación]**.

![Se ha enviado una invitación pendiente al editor que aparece en la vista Mis conexiones.](/help/assets/connect/establish-connection/pending-invite-sent.png){zoomable="yes"}

Una vez que el colaborador acepta la invitación, puede configurar los ajustes de conexión y enviarlos al colaborador para que los revise y acepte.

## Configuración de la conexión {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Casos de uso"
>abstract="Los casos de uso se rellenan previamente con todas las opciones. Puede editar los casos de uso antes de enviar la configuración de conexión."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia se rellenan previamente con las seleccionadas en el nivel de organización. Puede desactivar cualquier clave de coincidencia que no desee utilizar en esta conexión."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="Pago dividido"
>abstract="Esta sección determina quién paga las actividades correspondientes dentro de Real-Time CDP Collaboration. Actualmente, solo se puede configurar el caso de uso compartido de públicos."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Uso compartido de audiencias"
>abstract="El uso compartido de públicos es la actividad que una parte realiza al solicitar que su socio de colaboración active sus datos coincidentes."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Medición"
>abstract="Este caso de uso le permite ejecutar actividades en Real-Time CDP Collaboration para generar informes de rendimiento e información de la campaña."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Acuerdo legal"
>abstract="Compruebe que existe un acuerdo de uso compartido de datos entre las dos partes."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Nombres de anunciantes"
>abstract="<p>Configuración opcional. Indica el nombre y el ID con los que el editor conoce al anunciante.</p><p>El nombre del anunciante que agregue aquí se rellenará previamente en el paso Crear proyecto.</p><ul><li>Si el publicador configuró varios nombres, seleccione uno de la lista.</li><li>Si solo se configura un nombre, se preselecciona automáticamente.</li><li>Si no se configuran nombres, el campo se rellena previamente con el nombre de cuenta del anunciante de Real-Time CDP Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Crear un proyecto"

Una vez enviada la invitación, puede obtener una vista previa de la configuración de conexión. La invitación debe ser aceptada antes de que pueda finalizar la configuración de la conexión.

![Vista de configuración de conexión en estado de vista previa.](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

Una vez que su colaborador ha aceptado la conexión, puede empezar a configurar los ajustes de conexión para la conexión. La configuración de conexión define los términos de su colaboración, como los casos de uso que realizará conjuntamente, las claves de coincidencia que utilizará en los proyectos, etc.

Para establecer y compartir la configuración de conexión con tu colaborador, ve a **[!UICONTROL Mis conexiones]**. Para cualquier conexión con el estado **[!UICONTROL Pendiente]**, puede seleccionar **[!UICONTROL Configurar conexión]** para configurar las opciones de conexión.

![Se resaltó la vista Mis conexiones con una conexión pendiente y su opción Configurar conexión.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

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

+++Nombres del anunciante

Como editor que trabaja en la configuración de conexión, puede seleccionar agregar en sus sistemas cualquier nombre de anunciante por el que conozca al anunciante. Como editor, puede agregar varios nombres de anunciante a una conexión, por ejemplo, en casos en los que el anunciante con el que trabaja tenga presencia en varias regiones geográficas. Más adelante en el proceso, al [crear un proyecto](/help/guide/collaborate/manage-projects.md#create-project) en el que colaborar, usted o su colaborador podrán seleccionar el nombre del anunciante que se asociará con el proyecto.

![Agregar modal de nombres de anunciante.](/help/assets/connect/establish-connection/add-advertiser-names-modal.png)

Así funciona la selección de nombre del anunciante al crear un proyecto:

1. **Sin conjunto de nombres de anunciante**: Si no se agregan nombres de anunciante, Real-Time CDP Collaboration usa de manera predeterminada el nombre del anunciante como nombre del anunciante.
2. **Un conjunto de nombres de anunciante**: Si se agrega un solo nombre de anunciante, Real-Time CDP Collaboration lo usará automáticamente como nombre de anunciante para el proyecto.
3. **Conjunto de varios nombres de anunciante**: Si se agrega más de un nombre de anunciante, usted o su colaborador pueden seleccionar cualquiera de los nombres proporcionados al crear el proyecto.

![Nombres de anunciantes.](/help/assets/connect/establish-connection/advertiser-names.png)

+++

Una vez que haya hecho su selección, seleccione **[!UICONTROL Enviar]** para enviar la configuración sugerida a su colaborador para que la revise.

Si recibe la configuración de conexión propuesta de su colaborador, puede **[!UICONTROL Aceptar]** o **[!UICONTROL Rechazar]** dicha configuración. Antes de aceptar la configuración de conexión, debe reconocer y confirmar que existe un acuerdo legal entre usted y el colaborador. Si está rechazando la configuración de conexión, póngase en contacto con su colaborador fuera del producto y hable de cómo deben revisar la configuración de conexión para que usted la acepte.

## Eliminación de conexiones {#delete-connections}

Puede eliminar cualquier conexión con colaboradores con los que no desee seguir trabajando. Para eliminar conexiones existentes:

1. Vaya a **[!UICONTROL Conectar]** > **[!UICONTROL Mis conexiones]**.
2. Seleccione **[!UICONTROL Ver conexión]** en la tarjeta de conexión para tener acceso a la conexión que desea eliminar.
3. Seleccione el icono de eliminación ![icono de eliminación](/help/assets/common/delete.svg) para que aparezca el cuadro de diálogo de confirmación de eliminación de conexión.
   ![Icono de eliminación de conexión resaltado.](/help/assets/connect/establish-connection/delete-icon-highlighted.png){zoomable="yes"}
4. Confirme la eliminación seleccionando **[!UICONTROL Eliminar]**.
   ![Cuadro de diálogo para confirmar la eliminación de una conexión. ](/help/assets/connect/establish-connection/delete-connection-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Una vez eliminada la conexión, ya no estará conectado con el colaborador y todos los proyectos existentes que formen parte de la colaboración se eliminarán de forma permanente y no se recuperarán.

## Pasos siguientes

Después de establecer una conexión con su colaborador, usted y su colaborador ahora pueden [crear proyectos](/help/guide/collaborate/manage-projects.md#create-project).
