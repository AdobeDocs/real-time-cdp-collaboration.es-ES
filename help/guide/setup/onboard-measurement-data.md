---
title: Adición y administración de datos de medición
description: Aprenda a añadir datos de medición a Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 739d31b9-3f00-477d-b6be-995c7767c6ca
TQID: https://experienceleague.adobe.com/uJgTdRoA4K-Y-Me287MRvI5-jmuW2glaigB8JMAtME4
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 2720
ht-degree: 4%

---

# Adición y administración de datos de medición {#add-and-manage-measurement-data}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_onboard_measurement_data"
>title="Más información"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_data_target_fields"
>title="Campos de destino"
>abstract="Marcador de posición de los campos de destino de medición."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_data_source_fields"
>title="Campos de origen"
>abstract="Marcador de posición de los campos de origen de medición."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_measurement_mapping_source_fields"
>title="Asignar campos de origen"
>abstract="Marcador de posición de los campos de origen de medición."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_measurement_mapping_target_fields"
>title="Asignar campos de destino"
>abstract="Marcador de posición los campos de destino de medición."

{{limited-availability-release-note}}

Este documento describe los pasos para agregar datos de medición de campañas a Adobe Real-Time CDP Collaboration. Los editores pueden trabajar con los equipos de Adobe para cargar los datos de medición de campañas. Una vez que los datos se hayan cargado y procesado, tanto el editor como el anunciante podrán ver [informes de medición de campañas](/help/guide/collaborate/measure.md).

## Añadir datos de medición {#add-measurement-data}

Como anunciante, puede cargar en Collaboration los datos de medición que contengan eventos de conversión para utilizarlos en informes de medición de campañas. Los datos de conversión suelen incluir campos como identificadores de usuario (por ejemplo, correo electrónico con hash o ID de dispositivo), marca de tiempo del evento de conversión y detalles específicos del evento de conversión, como compra o registro.

Para obtener datos de medición de origen, vaya a la ficha **[!UICONTROL Mis datos de medición]** en el área de trabajo **[!UICONTROL Configuración]**. Seleccione el icono de agregar (![Agregar icono.](/help/assets/icons/plus.png)) y luego seleccione **[!UICONTROL Datos de medición]**.

Si estos son sus primeros datos de medición, también puede seleccionar la opción **[!UICONTROL Agregar]**.

![Pestaña de datos Mi medida con las opciones Agregar y Datos de medida resaltadas.](../../assets/setup/add-manage-measurement-data/add-measurement-data.png){zoomable="yes"}

Aparece la pantalla **[!UICONTROL Agregar datos de medición]**, que muestra un resumen de los pasos para obtener datos de medición. Seleccione **[!UICONTROL Iniciar incorporación]**.

![La pantalla Agregar datos de medición muestra un resumen de los pasos para obtener los datos de medición y la opción Iniciar incorporación está resaltada.](../../assets/setup/add-manage-measurement-data/add-measurement-data-screen.png){zoomable="yes"}

### Conexión de datos y detalles {#data-connection-and-details}

En este paso, debe configurar la conexión de datos y especificar los detalles de los datos de medición.

#### Seleccionar tipo de datos de medición {#select-measurement-data-type}

El tipo de datos de medición define el tipo de eventos que se llevan a cabo para la medición de campañas. Actualmente, el tipo compatible son los datos de conversión.

Seleccione **[!UICONTROL Datos de conversión]** como tipo de datos de medición, seguido de **[!UICONTROL Siguiente]**.

![La conexión de datos y el paso de detalles resaltan el tipo de datos de medición y la opción Siguiente.](../../assets/setup/add-manage-measurement-data/select-measurement-data-type.png){zoomable="yes"}

#### Seleccionar conexión de datos {#select-data-connection}

Una conexión de datos es la fuente desde la que se obtienen los datos de medición en Collaboration. Una vez establecida la conexión de datos inicial y obtenido el primer conjunto de datos de medición, puede seguir obteniendo datos de medición adicionales mediante la misma conexión de datos.

Para agregar una conexión de datos, seleccione **[!UICONTROL Agregar una nueva conexión de datos]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.

![El paso de conexión de datos y detalles resalta la opción Agregar una nueva conexión de datos y la opción Siguiente.](../../assets/setup/add-manage-measurement-data/select-measurement-data-connection.png){zoomable="yes"}

#### Seleccionar fuente de datos {#select-data-source}

Next, choose the source for your data connection. At this time, Adobe Experience Platform is the only supported data source.

Select your data source, then select **[!UICONTROL Next]**.

![The Data connection and details step highlighting the Adobe Experience Platform option and the Next option.](../../assets/setup/add-manage-measurement-data/select-measurement-data-source.png){zoomable="yes"}

#### Selección de zona protegida {#select-sandbox}

Select the sandbox that includes the measurement data that you want to use for Collaboration campaign measurement reports. Choose the sandbox from the list of available sandboxes and then select **[!UICONTROL Next]**.

![The Data connection and details step highlighting the Prod sandbox and the Next option.](../../assets/setup/add-manage-measurement-data/select-sandbox.png){zoomable="yes"}

#### Select measurement dataset {#select-measurement-dataset}

A list of datasets in the selected sandbox appears. Select a dataset as your measurement data, then select **[!UICONTROL Next]**. You can use the Search option to filter and find the preferred dataset.

![The Data connection and details step highlighting the Search option, the Example Event Data Dataset, and the Next option.](../../assets/setup/add-manage-measurement-data/select-measurement-dataset.png){zoomable="yes"}

#### Provide name and details {#provide-name-and-details}

Next, provide a name and a description for your data connection. This information will help you identify the data connection later on.

![The Data connection and details step with the option to provide a name and description.](../../assets/setup/add-manage-measurement-data/data-connection-name-details.png){zoomable="yes"}

### Asignación {#mapping}

The next step is to map fields from your measurement data to the corresponding target fields used in Collaboration. You can also choose to enrich your event dataset with attributes from Real‑Time Customer Profile by mapping join keys, and use these attributes to break down measurement reports.

#### Enrich event data {#enrich-event-data}

To enrich your event data, select the **[!UICONTROL Source field join key]** option.

![The Mapping screen with the Source field join key option highlighted.](../../assets/setup/add-manage-measurement-data/select-source-field-join-key.png){zoomable="yes"}

In the **[!UICONTROL Source field join key]** dialog, choose the source field, followed by **[!UICONTROL Select]**.

![The Source field join key dialog highlighting the Source field and the Next option.](../../assets/setup/add-manage-measurement-data/source-field-join-key-dialog.png){zoomable="yes"}

Next, select the **[!UICONTROL Profile join key]** option. In the **[!UICONTROL Profile join key]** dialog, select the profile field from the list. Puede utilizar la opción Buscar para encontrar el campo deseado. A continuación, elija **[!UICONTROL Seleccionar]** para confirmar.

![El cuadro de diálogo Clave de unión de perfil que resalta la clave de búsqueda, el campo de perfil seleccionado y la opción Siguiente.](../../assets/setup/add-manage-measurement-data/profile-join-key-dialog.png){zoomable="yes"}

#### Asignación de campos {#mapping-fields}

Para empezar a asignar campos de origen de los datos de medición a los campos de destino en Collaboration, seleccione el campo de origen vacío en la pantalla **[!UICONTROL Mapping]**.

![Pantalla de asignación con el campo de origen vacío resaltado.](../../assets/setup/add-manage-measurement-data/mapping-screen.png){zoomable="yes"}

Aparece el cuadro de diálogo **[!UICONTROL Seleccionar campo de origen]**, que muestra una lista de los campos de origen disponibles agrupados en opciones como **[!UICONTROL Área de nombres de identidad]** y **[!UICONTROL Esquema de evento]**. Puede utilizar la opción de búsqueda para filtrar y encontrar el campo de origen de la lista.

Elija el campo de origen que desee, seguido de **[!UICONTROL Seleccionar]**.

![El cuadro de diálogo Seleccionar campo de origen resalta el campo de origen Correos electrónicos y la opción Seleccionar.](../../assets/setup/add-manage-measurement-data/select-source-field-dialog.png){zoomable="yes"}

A continuación, utilice el menú desplegable para asignar el campo de origen seleccionado a un campo de destino adecuado. Todos los campos de destino disponibles son las [claves de coincidencia configuradas para su cuenta de Collaborator](./onboard-account.md#set-up-match-keys).

![Menú desplegable que muestra todos los campos de destino disponibles para asignar con el campo de origen seleccionado.](../../assets/setup/add-manage-measurement-data/select-target-field-dropdown.png){zoomable="yes"}

Puede agregar o quitar filas de asignación según sea necesario. Si necesita asignar un campo de origen sin hash a un campo de destino con hash (por ejemplo, asignar un correo electrónico de texto sin hash a [!UICONTROL Correo electrónico con hash]), use la opción **[!UICONTROL Aplicar transformación]** para aplicar el hash requerido.

Cuando haya terminado, revise los campos asignados y las claves de unión si el enriquecimiento está habilitado. A continuación, seleccione **[!UICONTROL Siguiente]**.

![Pantalla de asignación que muestra los campos asignados, las claves de combinación (cuando el enriquecimiento está habilitado) y la opción Siguiente resaltada.](../../assets/setup/add-manage-measurement-data/review-mapping.png){zoomable="yes"}

### Administrar el consentimiento {#manage-consent}

Antes de continuar, debe reconocer que el uso de datos en Collaboration cumple con las políticas de gobernanza de datos de Real-Time CDP. Todos los datos deben filtrarse previamente de acuerdo con los requisitos de consentimiento o cualquier política de consentimiento personalizada aplicable, por lo que no se requiere ningún procesamiento adicional.

Para confirmar tu confirmación, selecciona **[!UICONTROL Siguiente]**.

![La pantalla Administrar consentimiento que requiere confirmación con la opción Siguiente resaltada.](../../assets/setup/add-manage-measurement-data/manage-consent.png){zoomable="yes"}

Si [habilita el enriquecimiento de perfiles durante el paso de asignación](#enrich-event-data), puede configurar directivas de consentimiento a partir de una lista de opciones predefinidas. Esto incluye:

* **Acciones de marketing**: utilice estas acciones de marketing para controlar qué datos de audiencia se incluirán en Collaboration desde Experience Platform.
* **Reglas de consentimiento**: seleccione las reglas de consentimiento que se aplicarán a los datos que se originan en Collaboration.
* **Audiencia**: use el filtro de audiencia para incluir o excluir perfiles de audiencia para el consentimiento.

>[!NOTE]
>
>**[!UICONTROL Data Collaboration]** admite las etiquetas de uso de datos C4, C5 y C9, mientras que **[!UICONTROL Data Science]** solo admite C9. Obtenga más información sobre las etiquetas de uso de datos en la documentación de Experience Platform:
>
>* [Información general sobre las etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/overview){target="_blank"}
>* [Glosario](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Seleccione la configuración preferida y luego seleccione **[!UICONTROL Siguiente]**.

![La pantalla Administrar consentimiento muestra las opciones de configuración de consentimiento cuando el enriquecimiento de perfil está habilitado, con la opción Siguiente resaltada.](../../assets/setup/add-manage-measurement-data/manage-consent-configuration-options.png){zoomable="yes"}

Antes de continuar, debe confirmar y aceptar los términos del cuadro de diálogo **[!UICONTROL Directiva de gobernanza y acciones de aplicación]**. Seleccione la casilla de verificación, seguida de **[!UICONTROL Aceptar]**.

![El cuadro de diálogo Directiva de gobernanza y acciones de aplicación que muestra la casilla de verificación y la opción Aceptar resaltada.](../../assets/setup/add-manage-measurement-data/governance-policy-enforcement-actions-dialog.png){zoomable="yes"}

#### Filtro de público {#audience-filter}

Para incluir o excluir determinados perfiles de audiencia para el consentimiento, utilice el menú desplegable **[!UICONTROL Filtro de audiencia]**. Una vez que seleccione este filtro, la interfaz de usuario se actualizará para mostrar la opción **[!UICONTROL Examinar audiencias]**. Seleccionar **[!UICONTROL audiencias de exploración]**.

![La pantalla Administrar consentimiento que muestra la opción Examinar audiencias después de seleccionar el filtro de audiencia.](../../assets/setup/add-manage-measurement-data/browse-audiences.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Seleccionar audiencias]**. Elija una audiencia de la lista, seguida de **[!UICONTROL Select]**.

![El cuadro de diálogo Seleccionar audiencias resalta la audiencia seleccionada y la opción Seleccionar.](../../assets/setup/add-manage-measurement-data/select-audiences-dialog.png){zoomable="yes"}

La audiencia elegida aparece ahora, con la opción de eliminarla si es necesario. Revisa tu configuración de consentimiento y, a continuación, selecciona **[!UICONTROL Siguiente]**.

![La pantalla Administrar consentimiento resalta la audiencia seleccionada para el consentimiento y la opción Siguiente.](../../assets/setup/add-manage-measurement-data/audience-for-consent.png){zoomable="yes"}

### Añadir evento de conversión {#add-conversion-event}

A continuación, defina los eventos de conversión que desea que midan el impacto de sus campañas en, por ejemplo, visitas al sitio, registros o compras completadas. Puede especificar hasta **3** eventos de conversión distintos para la medición.

Proporcione el nombre del evento de conversión y, a continuación, utilice el menú desplegable para seleccionar el tipo de conversión.

![Se ha expandido la pantalla Agregar evento de conversión que resalta el menú desplegable de tipo de conversión.](../../assets/setup/add-manage-measurement-data/conversion-type-dropdown.png){zoomable="yes"}

Puede introducir un valor para la conversión o dejarlo vacío si no desea asignar un valor en este momento.

![La pantalla Agregar evento de conversión resalta la opción Valor de conversión.](../../assets/setup/add-manage-measurement-data/conversion-value.png){zoomable="yes"}

A continuación, debe especificar la clave de duplicación para indicar qué filas del conjunto de datos de evento pertenecen al mismo evento de conversión subyacente (por ejemplo, la misma marca de tiempo durante un proceso de registro). This prevents counting the same conversion multiple times in measurement reports. To do this, select **[!UICONTROL Duplication key]**. In the **[!UICONTROL Duplication key]** dialog, find and choose the key, followed by **[!UICONTROL Select]**.

![The Duplication key dialog showing the selected key and the Select option.](../../assets/setup/add-manage-measurement-data/duplication-key-dialog.png){zoomable="yes"}

After specifying the duplication key, you can add up to **5** conditions to include only relevant rows from the event dataset for the conversion. Choose to apply all or any of these conditions.

Select **[!UICONTROL Add condition]**, then select the condition option.

![The Add conversion event screen highlighting the condition option after selecting Add condition option.](../../assets/setup/add-manage-measurement-data/add-condition.png){zoomable="yes"}

In the **[!UICONTROL Select source field]** dialog, find and choose a source field for the condition rule, followed by **[!UICONTROL Select]**.

![The Select source field dialog highlighting the Event Type field and the Select option.](../../assets/setup/add-manage-measurement-data/select-condition-field.png){zoomable="yes"}

Use the dropdown menu to select a logic operator, then enter the value for the confition rule.

![The Add conversion event screen highlighting the dropdown for logic operator and the Value option.](../../assets/setup/add-manage-measurement-data/logic-operator-dropdown.png){zoomable="yes"}

To add another conversion event, select **[!UICONTROL Add conversion]**. You can include up to **3** conversion events in total. Once finished, review the conversion configurations and select **[!UICONTROL Next]**.

![The Add conversion event screen showing the conversion event configurations and the Next option highlighted.](../../assets/setup/add-manage-measurement-data/add-conversion-event.png){zoomable="yes"}

### Revisar {#review}

The **[!UICONTROL Review]** screen appears with a summary of measurement data settings. Review and ensure all the information are correct. If you need to change any section, use the **[!UICONTROL Edit]** option.

Finally, select **[!UICONTROL Complete]** to finish adding your measurement data.

![The Review screen showing a summary of measurement data settings and the Complete option highlighted.](../../assets/setup/add-manage-measurement-data/review-measurement-data.png){zoomable="yes"}

A confirmation dialog confirms that your measurement data was created successfully. You can see the new conversion events configured from your measurement data in the **[!UICONTROL My measurement data]** workspace.

![My measurement data workspace showing a list of conversion events configured from your measurement data.](../../assets/setup/add-manage-measurement-data/conversion-event-list.png){zoomable="yes"}

When in grid view or table view, select a row item or the **[!UICONTROL View conversion]** option within an event card to see an overview of a specific conversion event. It displays the event&#39;s status, source, and data connection name, along with detailed panels for:

* **[!UICONTROL Conversion details]**: Displays key information about the conversion, including its type, the duplication key used to identify unique events, and the assigned conversion value (if specified).
* **[!UICONTROL Conditions]**: Displays the condition rules applied to this conversion event.

![The Overview screen displaying the details for a conversion event.](../../assets/setup/add-manage-measurement-data/conversion-event-overview.png){zoomable="yes"}

## Edit measurement data {#edit-measurement-data}

After sourcing your measurement data, you can edit the details and condition rules of a conversion event at anytime.

From the **[!UICONTROL My measurement data]** tab, select the ellipsis option (![More icon](/help/assets/icons/more.png)) within the relevant conversion event card. Then select **[!UICONTROL View conversion]** from the dropdown menu to open the detailed page for that conversion event.

![My measurement data tab with the ellipsis menu open and the View conversion option highlighted.](/help/assets/setup/add-manage-measurement-data/conversion-event-list.png){zoomable="yes"}

### Editar nombre y descripción {#edit-name-and-description}

To update the event&#39;s name and description, select the edit icon (![Edit icon](/help/assets/icons/edit.png)) at the top right of the page.

![The Site Visit event page with the Edit icon on the top right highlighted.](/help/assets/setup/add-manage-measurement-data/edit-name-description.png){zoomable="yes"}

In the **[!UICONTROL Edit name and description]** dialog, update the fields with the desired values, then select **[!UICONTROL Save]** to apply your changes.

![The Edit name and description dialog with the Save option highlighted.](/help/assets/setup/add-manage-measurement-data/edit-name-description-dialog.png){zoomable="yes"}

A confirmation dialog appears to confirm that the details are successfully updated.

### Editar detalles de la conversión {#edit-conversion-details}

You can update the following conversion details of the event:

| Campo | Descripción |
|-------------------|-------------|
| Tipo de conversión | The category of the conversion event, such as a site visit, purchase, or sign-up. |
| Clave de duplicación | Identifier for rows in the event dataset belonging to the same conversion event (for example, same timestamp). Prevents duplicate counts. |
| Valor de conversión | The value associated with each conversion. |

{style="table-layout:auto"}

To start editing, select **[!UICONTROL Edit]** within the **[!UICONTROL Conversion details]** panel.

![The Site Visit event page highlighting the Edit option within the Conversion details panel.](/help/assets/setup/add-manage-measurement-data/edit-conversion-details.png){zoomable="yes"}

In the **[!UICONTROL Edit conversion details]** dialog, use the dropdown menu to update the conversion type. You can enter a value for the conversion, or leave it empty if you do not wish to assign a value. To edit the duplication key, select the existing key option.

![The Edit conversion details dialog with the Example Person ID option highlighted.](/help/assets/setup/add-manage-measurement-data/edit-conversion-details-dialog.png){zoomable="yes"}

The **[!UICONTROL Duplication key]** dialog displays a list of available fields grouped under options such as **[!UICONTROL Identity namespace]** and **[!UICONTROL Event schema]**. Find and choose the desired key, followed by **[!UICONTROL Select]**.

![The Duplication key dialog showing the chosen key and the Select option.](../../assets/setup/add-manage-measurement-data/edit-duplication-key-dialog.png){zoomable="yes"}

Once finished, review the updates and select **[!UICONTROL Save]** to apply your changes.

![The Edit conversion details dialog with the Save option highlighted.](/help/assets/setup/add-manage-measurement-data/edit-conversion-details-save.png){zoomable="yes"}

A confirmation dialog appears to confirm that the details are successfully updated.

### Editar condiciones {#edit-conditions}

Condition rules specify which data rows from your event dataset are included as conversions. Update these rules as needed to ensure your measurement reflects only the most relevant data for your analysis.

To edit conditions, select **[!UICONTROL Edit]** within the **[!UICONTROL Conditions]** panel.

![The Site Visit event page highlighting the Edit option within the Conditions panel.](/help/assets/setup/add-manage-measurement-data/edit-conditions.png){zoomable="yes"}

In the **[!UICONTROL Edit conversion rules]** dialog, you can view the current details of all conditions. Select an existing condition option to update its details including source field, logic rule and value.

![The Edit conversion rules dialog highlighting the options to edit source field, logic rule and value of an exisiting condition.](/help/assets/setup/add-manage-measurement-data/edit-exisiting-condition.png){zoomable="yes"}

To include additional conversion rules, select **[!UICONTROL Add condition]**. Then select the new empty condition option.

![The Edit conversion rules dialog showing the new empty condition option after selecting the Add condition option.](/help/assets/setup/add-manage-measurement-data/edit-conversion-rules-add-condition.png){zoomable="yes"}

In the **[!UICONTROL Select source field]** dialog, you can see available fields grouped under options such as **[!UICONTROL Identity namespace]** and **[!UICONTROL Event schema]**. Select the appropriate field you want to use for your condition, then choose **[!UICONTROL Select]**. You can use the **[!UICONTROL Search]** option to quickly find your preferred field.

![The Select source field dialog showing the chosen field and the Select option.](../../assets/setup/add-manage-measurement-data/edit-condition-source-key.png){zoomable="yes"}

Next, use the dropdown menu to select a logic operator from the available list and enter a value for the condition.

![The Edit conversion rules dialog highlighting the logic dropdown menu.](../../assets/setup/add-manage-measurement-data/edit-condition-logic-dropdown.png){zoomable="yes"}

Use **[!UICONTROL Include all conditions]** if all specified conditions are required for each conversion, or use **[!UICONTROL Include any of the conditions]** to allow conversions that match at least one condition. When you finish updating, review and select **[!UICONTROL Save]** to apply the changes.

![The Edit conversion rules dialog with the Save option highlighted.](/help/assets/setup/add-manage-measurement-data/edit-conversion-rules-save.png){zoomable="yes"}

Aparecerá un cuadro de diálogo de confirmación para confirmar que los detalles se han actualizado correctamente.

## Eliminar datos de medición {#delete-measurement-data}

Al eliminar los datos de medición, se eliminan permanentemente del proyecto el evento de conversión asociado y todos los detalles de medición vinculados. Cualquier informe de medición que dependa de este evento perderá las métricas de conversión correspondientes y ya no se podrá actualizar. Esta acción no se puede deshacer.

Para eliminar un evento de conversión existente, vaya a la ficha **[!UICONTROL Mis datos de medición]** en el área de trabajo **[!UICONTROL Configuración]**. En la vista de cuadrícula, seleccione **[!UICONTROL Eliminar]** en la tarjeta de evento correspondiente. En la vista de tabla, seleccione el icono de eliminación (![Eliminar icono](/help/assets/common/delete.svg)) junto al nombre del evento.

![La pestaña Mis datos de medición resalta la opción Eliminar en una fila de eventos de conversión.](/help/assets/setup/add-manage-measurement-data/delete-measurement-data.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Eliminar medición]**, que le pedirá que confirme la eliminación del evento. Seleccione **[!UICONTROL Eliminar]**.

![Cuadro de diálogo Eliminar medición con la opción Eliminar resaltada.](/help/assets/setup/add-manage-measurement-data/delete-measurement-dialog.png){zoomable="yes"}

Aparecerá un cuadro de diálogo de confirmación para confirmar que el evento de conversión se ha eliminado correctamente.

## Próximos pasos {#next-steps}

Ha completado el abastecimiento de los datos de medición en Collaboration. Como anunciante, ahora puede crear informes de atribución para explorar cómo las campañas generan conversiones y miden el impacto general. Si es editor, solicite a su colaborador que genere un informe de atribución para sus campañas. Para obtener instrucciones detalladas, consulte la guía [Crear informe de atribución](../collaborate/measure.md#create-attribution-report).
