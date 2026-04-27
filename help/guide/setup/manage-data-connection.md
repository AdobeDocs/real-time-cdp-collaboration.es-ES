---
title: Administrar conexiones de datos
description: Learn how to manage data connections, including match keys, scheduling, use cases, and audience filtering in Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
TQID: https://experienceleague.adobe.com/QvkEpR1fJMZ5BXrucAzEtxFNSfSMS-2hIZvMSg63ySE
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1179
ht-degree: 6%

---

# Administrar conexiones de datos

{{limited-availability-release-note}}

## Información general

Use data connections in Real-Time CDP Collaboration to source audiences from various platforms. Learn how to manage match keys and schedule data refreshing for your existing data connections. Additionally, you&#39;ll be able to filter audiences by different attributes for more granular insights.

>[!NOTE]
>
>To create a new data connection, see [Add and manage audiences](./onboard-audiences.md).

## View data connections

To view existing data connections, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My data connections]** tab. All your current data connection are displayed, showing a brief overview for each connection. For a complete view of a data connection&#39;s information, including its match keys, scheduling details, and audiences, select **[!UICONTROL View data connection]** on the corresponding connection.

![Setup workspace with My data connections tab view displayed and highlighted.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Claves de coincidencia {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia determinan cómo coincidirán los datos de diferentes fuentes. Las claves de coincidencia que se muestran a continuación son los campos de destino a los que asignó los campos de origen."

Match keys are the target fields you [mapped your source fields to](./onboard-audiences.md#map-fields). To learn more about how match keys work, see the [match keys](./onboard-account.md#set-up-match-keys) guide.

![A data connections workspace with the Match keys section highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Programación {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Programación"
>abstract="View the scheduling details for your data connection, and edit the configurations if required."

View and manage the scheduling settings for your data connections. Scheduling determines how often the audience is refreshed.

After a data connection is created, you can update its refresh frequency, start date, and end date directly from the **[!UICONTROL Scheduling]** section of the data connection workspace.

>[!NOTE]
>
>When sourcing audiences from Adobe Experience Platform, audiences become available within 24 hours after the data connection is established. After the initial sourcing, audience data refreshes according to the defined frequency.

For more information on scheduling, see the [scheduling section](/help/guide/setup/onboard-audiences.md#schedule) in the guide to configuring audiences.

![A data connection&#39;s workspace with the Scheduling section highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Editar conexión de datos {#edit-data-connection}

Read the following sections to learn how to update the match keys and scheduling settings of an existing data connection.

### Editar claves de coincidencia {#edit-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_edit_measurement_data_connection_enrichment"
>title="Enriquecimiento"
>abstract="Turning off enrichment is not supported. You can change the enrichment join keys instead."
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-manage-dataconnections" text="Enriquecimiento"

>[!IMPORTANT]
>
>Antes de editar las claves de coincidencia para una conexión de datos, tenga en cuenta lo siguiente:
>
>* Solo se pueden utilizar claves de coincidencia configuradas para su cuenta en las conexiones de datos.
>* En este momento, puede agregar claves de coincidencia adicionales a una conexión de datos, pero una vez que una clave de coincidencia está habilitada, no se puede eliminar.

Seleccione **[!UICONTROL Editar]** de la sección **[!UICONTROL Claves de coincidencia]**.

![La sección Claves de coincidencia con la opción Editar resaltada.](/help/assets/setup/manage-data-connection/edit-match-keys.png){zoomable="yes"}

Aparece un cuadro de diálogo de confirmación que explica que cualquier cambio en la conexión de datos se aplicará a todas las audiencias asociadas. Seleccione **[!UICONTROL Aceptar]** para confirmar. Puede optar por omitir esta confirmación en el futuro.

![Cuadro de diálogo de confirmación que muestra que cualquier cambio en la conexión de datos se aplicará a todas las audiencias asociadas.](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

En el diálogo **[!UICONTROL Claves de coincidencia]**, puede ver las asignaciones existentes entre los campos de origen y sus campos de destino correspondientes (claves de coincidencia). Puede editar una clave de coincidencia actualizando el campo de origen asignado o agregar filas de campo de asignación adicionales para rellenar nuevas claves de coincidencia.

![Cuadro de diálogo Asignar claves que muestra las asignaciones existentes entre los campos de origen y los campos de destino correspondientes.](/help/assets/setup/manage-data-connection/match-keys-dialog.png){zoomable="yes"}

#### Añadir claves de coincidencia {#add-match-keys}

Seleccione **[!UICONTROL Agregar campo]** para agregar una nueva fila de campo.

![Después de seleccionar Agregar campo, el cuadro de diálogo Asignar claves muestra un nuevo campo de asignación vacío listo para la entrada.](/help/assets/setup/manage-data-connection/add-new-field.png){zoomable="yes"}

A continuación, seleccione el campo de origen vacío. El cuadro de diálogo **[!UICONTROL Seleccionar campo de origen]** aparece con las opciones **[!UICONTROL Áreas de nombres de identidad]** y **[!UICONTROL Atributos de perfil]**. Puede filtrar la lista y buscar el campo de origen deseado con la opción de búsqueda.

Elija el campo de origen que desee, seguido de **[!UICONTROL Seleccionar]**.

![Cuadro de diálogo Seleccionar campo de origen con la opción GAID seleccionada.](/help/assets/setup/manage-data-connection/select-source-field.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL Claves de coincidencia]**, utilice el menú desplegable para asignar el nuevo campo de origen a un campo de destino. Todos los campos de destino disponibles son las claves de coincidencia configuradas para la cuenta de Collaborator. Si no ves el campo de destino que necesitas, [edita las claves de coincidencia](./onboard-account.md#edit-match-keys) de tu cuenta para agregarlo.

Utilice la opción **[!UICONTROL Aplicar transformación]** si desea crear un campo sin hash con un campo de destino con hash, por ejemplo, al asignar un campo de origen de correo electrónico de texto sin formato al campo de destino **[!UICONTROL Correo electrónico con hash]**.

![Menú desplegable que muestra todos los campos de destino disponibles para asignar con el nuevo campo de origen.](/help/assets/setup/manage-data-connection/select-target-field.png){zoomable="yes"}

After you finish mapping fields, review your updates and select **[!UICONTROL Confirm]** to apply the changes.

![The Match keys dialog showing the updated field mapping with the Confirm option highlighted.](/help/assets/setup/manage-data-connection/review-and-confirm.png){zoomable="yes"}

A confirmation dialog confirms that the match keys were updated successfully.

### Edit scheduling {#edit-scheduling}

After a data connection is created, you can update its refresh frequency, start date, and end date directly from the **[!UICONTROL Scheduling]** section of the data connection workspace.

You can edit the frequency of an existing data connection to better control how often audiences are refreshed. To edit the schedule, select **[!UICONTROL Edit]** from within the data connection in the scheduling card.

![The Scheduling section with the Edit option highlighted.](/help/assets/setup/manage-data-connection/edit-scheduling.png){zoomable="yes"}

A confirmation dialog appears, explaining that any changes to the data connection will apply to all associated audiences. Select **[!UICONTROL OK]** to confirm. You can choose to skip this confirmation in the future.

![Confirmation dialog showing that any changes to the data connection will apply to all associated audiences.](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

In the **[!UICONTROL Scheduling]** dialog, select the dropdown menu to update the **[!UICONTROL Frequency]**. Set the refresh frequency to run daily or every two to six days.

![The Scheduling dialog with the Frequency dropdown expanded to display audience refresh frequency options.](../../assets/setup/manage-data-connection/edit-frequency.png){zoomable="yes"}

Next, select **[!UICONTROL Date range]** if you want to update the period during which audiences are populated and refreshed.

![The Scheduling dialog showing the Date range dropdown expanded to edit the start and end dates for audience population and refresh.](../../assets/setup/manage-data-connection/edit-date-range.png){zoomable="yes"}

When you&#39;re done, review the updates and select **[!UICONTROL Save]** to apply your changes.

![The Scheduling dialog highlighting the updates and Save option.](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes"}

## Eliminar conexión de datos

Deleting a data connection will remove all underlying audiences, associated settings, and usage across Collaboration. Esta acción no se puede deshacer.

To delete an existing data connection, select the delete icon (![Delete icon](/help/assets/common/delete.svg)) within an individual data connection&#39;s workspace.

![A data connections workspace with the delete option highlighted.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

A confirmation dialogue will appear. Select **[!UICONTROL Delete]** to finish deleting the data connection.

![The Delete data connection dialog with the Delete option highlighted.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Administrar audiencias {#manage-audiences}

En la parte inferior del espacio de trabajo se muestra una lista de audiencias adjuntas a la conexión de datos. La lista muestra una breve descripción general de cada audiencia, incluido su estado, origen y acceso a la conexión. Para editar las categorías de audiencia, el acceso a conexiones o la visibilidad de metadatos de una audiencia, seleccione el nombre de la audiencia. Para obtener una guía completa sobre cómo administrar una audiencia, consulte la guía [ver audiencias individuales](./onboard-audiences.md#view-individual-audiences).

![Espacio de trabajo de conexiones de datos con las audiencias resaltadas.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Próximos pasos

Después de administrar las conexiones de datos, puede [descubrir superposiciones](/help/guide/collaborate/discover.md) entre sus audiencias y las audiencias que su colaborador ha hecho reconocibles.
