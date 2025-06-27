---
title: Conectar con anunciantes o editores
description: Después de descubrir colaboradores potenciales, aprenda a establecer conexiones y a comenzar a colaborar en proyectos.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: 3615d969ff6e0ff95304a02346845909f3f8258c
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 16%

---

# Conectar con anunciantes o editores

{{limited-availability-release-note}}

Para que los colaboradores (normalmente un anunciante y un editor) puedan trabajar juntos en las campañas, deben establecer una conexión. Esta conexión les permite activar audiencias, crear proyectos y ejecutar informes sobre el rendimiento de la campaña.

## Flujo de trabajo de alto nivel

Para establecer una conexión entre un anunciante y un editor, se requieren los siguientes pasos:

1. El anunciante [explora a los editores y descubre](/help/guide/connect/discover-publishers.md) uno con el que les gustaría trabajar.
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

![Panel de conexión con la opción Conectar resaltada en un editor específico.](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

Una vez enviada la invitación, puede obtener una vista previa de la configuración de conexión, pero no editarla. Ver invitaciones pendientes en la ficha **[!UICONTROL Mis conexiones]**. El estado de la conexión aparece como **[!UICONTROL Invitación enviada]**.

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
>abstract="Esta sección determina quién paga las actividades correspondientes dentro de Real-Time CDP Collaboration. "

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Uso compartido de audiencias"
>abstract="Los créditos de activación del público se consumen en función del número de ID coincidentes preparados para la activación."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Medición"
>abstract="Ejecutar actividades para generar informes y análisis sobre el rendimiento de las campañas. Los créditos se consumen en función del número de filas de los informes de campaña de todas las campañas y la frecuencia de los informes (diariamente, cada tres días o semanalmente)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Acuerdo legal"
>abstract="Compruebe que existe un acuerdo de uso compartido de datos entre las dos partes."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Nombres de anunciantes"
>abstract="<p>Configuración opcional. Indica el nombre y el ID mediante los cuales el editor conoce al anunciante.</p><p>El nombre del anunciante que añada aquí se rellenará previamente en el paso de creación del proyecto.</p><ul><li>Si el editor configuró varios nombres, seleccione uno de la lista.</li><li>Si solo se ha configurado un nombre, se seleccionará automáticamente de antemano.</li><li>Si no se han configurado nombres, el campo se rellenará previamente con el nombre de cuenta del anunciante de Real-Time CDP Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/es/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Crear un proyecto"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_activation"
>title="Activación del público"
>abstract="La activación del público permite seleccionar qué colaborador puede iniciar la activación del público."

<!-- Move and update the above popover when bidirectional is active. -->

Una vez enviada la invitación, puede obtener una vista previa de la configuración de conexión. La invitación debe ser aceptada antes de que pueda finalizar la configuración de la conexión.

![Vista de configuración de conexión en estado de vista previa.](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

### Configuración de conexión del anunciante {#advertiser-connection-settings}

Una vez que el colaborador haya aceptado la conexión, configure los parámetros de conexión. Esta configuración define los términos de colaboración, incluidos los casos de uso en los que trabajará, las claves de coincidencia para proyectos y otras configuraciones.

Para empezar, vaya a **[!UICONTROL Mis conexiones]**. Para cualquier conexión con el estado **[!UICONTROL Pendiente]**, puede seleccionar **[!UICONTROL Configurar conexión]** para configurar las opciones de conexión.

![Se resaltó el área de trabajo Mis conexiones con una conexión pendiente y su opción Configurar conexión.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Puede editar y definir los campos siguientes:

![Espacio de trabajo de configuración de conexión antes de que se rellene.](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++Casos de uso

Los casos de uso se rellenan previamente con todas las opciones disponibles. Para personalizarlos, seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Casos de uso]** y desactive los que no desee. Los casos de uso seleccionados determinan qué vistas y opciones están [disponibles en sus proyectos](../collaborate/manage-projects.md#project-use-cases).

![La configuración de casos de uso en el área de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Claves coincidentes

Las claves de coincidencia se rellenan previamente con las que seleccionaste al [configurar tu organización](/help/guide/setup/onboard-organization.md#set-up-match-keys). Puede desactivar cualquier clave de coincidencia que no desee utilizar, pero no puede añadir claves de coincidencia que no se seleccionaron durante la configuración de la organización.

![La configuración de la clave Match en el área de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/match-keys.png){zoomable="yes"}

+++

+++División de crédito

Utilice la sección de división de crédito para determinar cuál de las dos partes colaboradoras cubrirá los costes de las actividades. Las opciones de división de crédito están determinadas por los casos de uso seleccionados para la conexión. Aunque el caso de uso **[!UICONTROL Medición]** requiere que una parte cubra los costos, el caso de uso **[!UICONTROL Activación - Coincidencia]** proporciona una opción adicional para que cada parte cubra sus propios costos. Para obtener información sobre el desglose de costos, lea la guía [tipos de actividades de crédito](/help/guide/setup/my-activity.md#types-of-activities).

>[!NOTE]
>
>Audiencia: la salida siempre está cubierta por el colaborador que recibe la audiencia, por lo que no se requiere ninguna selección.

![Cuadro de diálogo de división de crédito con opciones en el área de trabajo de conexión.](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}
+++

+++Acuerdos

Antes de continuar con esta conexión, debe reconocer que existe un acuerdo de uso compartido de datos entre las dos partes.

![La sección Acuerdo legal se resalta y se confirma en el área de trabajo de conexión.](/help/assets/connect/establish-connection/legal-agreement.png){zoomable="yes"}

+++

Una vez que haya realizado sus selecciones, seleccione **[!UICONTROL Enviar]** para enviar la configuración sugerida a su colaborador para que la revise.

### Configuración de conexión del publicador {#publisher-connection-settings}

A continuación, el publicador debe revisar la configuración de conexión y aceptarla o rechazarla. Para revisar la configuración de conexión, vaya a **[!UICONTROL Mis conexiones]** y seleccione **[!UICONTROL Revisar configuración de conexión]** en la tarjeta de conexión.

![La opción Revisar configuración de conexión resaltada en la vista Mis conexiones.](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

Revise la configuración que ha propuesto el colaborador. Antes de aceptar la configuración de conexión, debe reconocer que existe un acuerdo legal entre usted y el colaborador. Además, puede agregar en sus sistemas cualquier nombre de anunciante por el cual conozca al anunciante.

![Espacio de trabajo de configuración de conexión con la configuración propuesta de las secciones Nombres de colaboradores y Anunciantes y Acuerdos resaltadas.](/help/assets/connect/establish-connection/publisher-connection-settings.png){zoomable="yes"}

+++Nombres del anunciante

Como editor que trabaja en la configuración de conexión, puede seleccionar agregar en sus sistemas cualquier nombre de anunciante por el que conozca al anunciante. Como editor, puede agregar varios nombres de anunciante a una conexión, por ejemplo, en casos en los que el anunciante con el que trabaja tenga presencia en varias regiones geográficas. Más adelante en el proceso, al [crear un proyecto](/help/guide/collaborate/manage-projects.md#create-project) en el que colaborar, usted o su colaborador podrán seleccionar el nombre del anunciante que se asociará con el proyecto.

![Cuadro de diálogo Nombres del anunciante en el área de trabajo de configuración de conexión.](/help/assets/connect/establish-connection/add-advertiser-names-modal.png)

Así funciona la selección de nombre del anunciante al crear un proyecto:

1. **Sin conjunto de nombres de anunciante**: Si no se agregan nombres de anunciante, Real-Time CDP Collaboration usa de manera predeterminada el nombre del anunciante como nombre del anunciante.
2. **Un conjunto de nombres de anunciante**: Si se agrega un solo nombre de anunciante, Real-Time CDP Collaboration lo usará automáticamente como nombre de anunciante para el proyecto.
3. **Conjunto de varios nombres de anunciante**: Si se agrega más de un nombre de anunciante, usted o su colaborador pueden seleccionar cualquiera de los nombres proporcionados al crear el proyecto.

![Se ha completado el área de trabajo de configuración de conexión con la sección Nombres de anunciantes.](/help/assets/connect/establish-connection/advertiser-names.png)

+++

>[!NOTE]
>
> Una vez que haya aceptado la configuración de conexión, ya no podrá agregar ni editar nombres de anunciantes.

Si está satisfecho con la configuración de conexión propuesta, seleccione **[!UICONTROL Aceptar]** para establecer la conexión. Si desea solicitar cambios en la configuración de conexión, seleccione **[!UICONTROL Rechazar]**. A continuación, el colaborador puede revisar la configuración de conexión y reenviarla para su revisión.

## Eliminación de conexiones {#delete-connections}

Puede eliminar cualquier conexión con colaboradores con los que no desee seguir trabajando. Para eliminar las conexiones existentes, ve a **[!UICONTROL Connect]**. Los anunciantes deberían navegar a **[!UICONTROL Mis conexiones]**. Seleccione **[!UICONTROL Ver conexión]** en la tarjeta de conexión para abrir la conexión que desea eliminar.

![La opción Ver conexión resaltada en la vista Mis conexiones.](/help/assets/connect/establish-connection/delete-view-connection.png){zoomable="yes"}

Seleccione el icono de eliminación ![eliminar icono](/help/assets/common/delete.svg) en el área de trabajo de conexión para eliminar la conexión.

![Icono de eliminación resaltado en el área de trabajo de conexión.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

Aparecerá un cuadro de diálogo de confirmación en el que se le pedirá que confirme la eliminación de la conexión. Seleccione **[!UICONTROL Eliminar]** para confirmar la eliminación.

![Cuadro de diálogo de confirmación para eliminar una conexión.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Una vez eliminada la conexión, ya no estará conectado con el colaborador y todos los proyectos existentes que formen parte de la colaboración se eliminarán de forma permanente y no se recuperarán.

## Pasos siguientes

Después de establecer una conexión con su colaborador, usted y su colaborador ahora pueden [crear proyectos](/help/guide/collaborate/manage-projects.md#create-project).
