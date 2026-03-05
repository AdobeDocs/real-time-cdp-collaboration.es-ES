---
title: Administrar conexiones de datos
description: Obtenga información sobre cómo administrar conexiones de datos, incluidas claves de coincidencia, programación, casos de uso y filtrado de audiencias en Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: 4bfa57ba36336dd835551fb846f1d567d6830bf9
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 5%

---

# Administrar conexiones de datos

{{limited-availability-release-note}}

## Información general

Utilice conexiones de datos en Real-Time CDP Collaboration para obtener audiencias de varias plataformas. Obtenga información sobre cómo administrar las claves de coincidencia y programar la actualización de datos para las conexiones de datos existentes. Además, podrá filtrar audiencias por atributos diferentes para obtener perspectivas más granulares.

## Ver conexiones de datos

Para ver las conexiones de datos existentes, vaya a **[!UICONTROL Configuración]** y, a continuación, seleccione la pestaña **[!UICONTROL Mis conexiones de datos]**. Se muestran todas las conexiones de datos actuales, con una breve descripción general de cada conexión. Para obtener una vista completa de la información de una conexión de datos, incluidas sus claves de coincidencia, detalles de programación y audiencias, seleccione **[!UICONTROL Ver conexión de datos]** en la conexión correspondiente.

![Configurar el área de trabajo con la vista de la ficha Mis conexiones de datos mostrada y resaltada.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Claves de coincidencia {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia determinan cómo coincidirán los datos de diferentes fuentes. Las claves de coincidencia que se muestran a continuación son los campos de destino a los que asignó los campos de origen."

Las claves de coincidencia son los campos de destino a los que [asignó los campos de origen](./onboard-audiences.md#map-fields). Para obtener más información sobre cómo funcionan las claves de coincidencia, consulte la guía [claves de coincidencia](./onboard-account.md#set-up-match-keys).

![Espacio de trabajo de conexiones de datos con la sección Claves de coincidencia resaltada.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Programación {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Programación"
>abstract="Vea los detalles de programación de la conexión de datos y edite las configuraciones si es necesario."

Ver y administrar la configuración de programación de las conexiones de datos. La programación determina la frecuencia con la que se actualiza la audiencia.

Después de crear una conexión de datos, puede actualizar su frecuencia de actualización, fecha de inicio y fecha de finalización directamente desde la sección **[!UICONTROL Programando]** del área de trabajo de conexión de datos.

>[!NOTE]
>
>Cuando se obtienen audiencias de Adobe Experience Platform, estas están disponibles en un plazo de 24 horas tras establecer la conexión de datos. Después del abastecimiento inicial, los datos de audiencia se actualizan según la frecuencia definida.

Para obtener más información sobre la programación, consulte la [sección de programación](/help/guide/setup/onboard-audiences.md#schedule) en la guía para configurar audiencias.

![Espacio de trabajo de una conexión de datos con la sección Programación resaltada.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Editar conexión de datos {#edit-data-connection}

Lea las siguientes secciones para aprender a actualizar las claves de coincidencia y la configuración de programación de una conexión de datos existente.

### Editar claves de coincidencia {#edit-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_edit_measurement_data_connection_enrichment"
>title="Enriquecimiento"
>abstract="No se admite desactivar el enriquecimiento. En su lugar, puede cambiar las claves de unión de enriquecimiento."
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

Una vez finalizada la asignación de campos, revisa las actualizaciones y selecciona **[!UICONTROL Confirmar]** para aplicar los cambios.

![Cuadro de diálogo Coincidir claves que muestra la asignación de campo actualizada con la opción Confirmar resaltada.](/help/assets/setup/manage-data-connection/review-and-confirm.png){zoomable="yes"}

Un cuadro de diálogo de confirmación confirma que las claves de coincidencia se actualizaron correctamente.

### Editar programación {#edit-scheduling}

Después de crear una conexión de datos, puede actualizar su frecuencia de actualización, fecha de inicio y fecha de finalización directamente desde la sección **[!UICONTROL Programando]** del área de trabajo de conexión de datos.

Puede editar la frecuencia de una conexión de datos existente para controlar mejor la frecuencia con la que se actualizan las audiencias. Para editar la programación, selecciona **[!UICONTROL Editar]** en la conexión de datos de la tarjeta de programación.

![La sección Programación con la opción Editar resaltada.](/help/assets/setup/manage-data-connection/edit-scheduling.png){zoomable="yes"}

Aparece un cuadro de diálogo de confirmación que explica que cualquier cambio en la conexión de datos se aplicará a todas las audiencias asociadas. Seleccione **[!UICONTROL Aceptar]** para confirmar. Puede optar por omitir esta confirmación en el futuro.

![Cuadro de diálogo de confirmación que muestra que cualquier cambio en la conexión de datos se aplicará a todas las audiencias asociadas.](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL Programación]**, seleccione el menú desplegable para actualizar la **[!UICONTROL Frecuencia]**. Configure la frecuencia de actualización para que se ejecute a diario o cada dos a seis días.

![El cuadro de diálogo Programación con el menú desplegable Frecuencia se ha expandido para mostrar las opciones de frecuencia de actualización de audiencia.](../../assets/setup/manage-data-connection/edit-frequency.png){zoomable="yes"}

A continuación, seleccione **[!UICONTROL Intervalo de fecha]** si desea actualizar el período durante el cual se rellenan y actualizan las audiencias.

![El cuadro de diálogo Programación que muestra el menú desplegable Intervalo de fechas se ha expandido para editar las fechas de inicio y finalización de la población y actualización de la audiencia.](../../assets/setup/manage-data-connection/edit-date-range.png){zoomable="yes"}

Cuando termines, revisa las actualizaciones y selecciona **[!UICONTROL Guardar]** para aplicar los cambios.

![Cuadro de diálogo Programación que resalta las actualizaciones y la opción Guardar.](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes"}

## Eliminar conexión de datos

Al eliminar una conexión de datos, se eliminarán todas las audiencias subyacentes, la configuración asociada y el uso en Collaboration. Esta acción no se puede deshacer.

Para eliminar una conexión de datos existente, seleccione el icono Eliminar (![Eliminar icono](/help/assets/common/delete.svg)) en el área de trabajo de una conexión de datos individual.

![Área de trabajo de conexiones de datos con la opción de eliminación resaltada.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

Aparecerá un cuadro de diálogo de confirmación. Seleccione **[!UICONTROL Eliminar]** para finalizar la eliminación de la conexión de datos.

![Cuadro de diálogo Eliminar conexión de datos con la opción Eliminar resaltada.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Administrar audiencias {#manage-audiences}

En la parte inferior del espacio de trabajo se muestra una lista de audiencias adjuntas a la conexión de datos. La lista muestra una breve descripción general de cada audiencia, incluido su estado, origen y acceso a la conexión. Para editar las categorías de audiencia, el acceso a conexiones o la visibilidad de metadatos de una audiencia, seleccione el nombre de la audiencia. Para obtener una guía completa sobre cómo administrar una audiencia, consulte la guía [ver audiencias individuales](./onboard-audiences.md#view-individual-audiences).

![Espacio de trabajo de conexiones de datos con las audiencias resaltadas.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Próximos pasos

Después de administrar las conexiones de datos, puede [descubrir superposiciones](/help/guide/collaborate/discover.md) entre sus audiencias y las audiencias que su colaborador ha hecho reconocibles.
