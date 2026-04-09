---
title: Administrar conexiones de datos de medición
description: Obtenga información sobre cómo administrar conexiones de datos de medición, incluidos detalles y claves de coincidencia en Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 494277f421606eda62b74c254f1fdd29b22e3473
workflow-type: tm+mt
source-wordcount: '1338'
ht-degree: 4%

---

# Administrar conexiones de datos de medición

{{limited-availability-release-note}}

## Información general

Utilice conexiones de datos de medición en Real-Time CDP Collaboration para obtener los datos de conversión de varias plataformas. Obtenga información sobre cómo administrar detalles y claves de coincidencia para las conexiones de datos existentes.

## Ver conexiones de datos de medición {#view-measurement-data-connections}

Puede ver los detalles de cualquier conexión de datos de medición existente, incluido cómo se originan los datos de conversión, qué claves de coincidencia están en uso y todos los eventos de conversión vinculados a la conexión.

En el área de trabajo **[!UICONTROL Configuración]**, vaya a la ficha **[!UICONTROL Mis conexiones de datos]**. Todas las conexiones de datos de medición actuales se muestran en la sección **[!UICONTROL Medición]** de la vista tabular o de cuadrícula. Seleccione **[!UICONTROL Ver conexión de datos]** en la tarjeta de conexión correspondiente o seleccione el nombre de la conexión de datos en la vista de tabla para abrir su área de trabajo y ver todos los detalles.

![La pestaña Mis conexiones de datos resalta una tarjeta de conexión de datos de medición y la opción Ver conexión de datos.](/help/assets/setup/manage-measurement-data-connection/view-measurement-data-connection.png){zoomable="yes"}

### Detalles de conexión de datos de medición {#measurement-data-connection-details}

En esta sección, puede ver los siguientes detalles de la conexión de datos:

| Campo | Descripción |
|-------------------|-------------|
| Estado | El estado actual de la conexión de datos de medición, por ejemplo, **[!UICONTROL Activo]**. |
| Fuente | La plataforma o el sistema que proporciona los datos de medición para esta conexión. |
| Zona protegida | Nombre de la zona protegida en la que se ha configurado la conexión de datos de medición. |
| Conjunto de datos | Nombre del conjunto de datos utilizado para obtener datos de medición en la conexión. |
| Última actualización | La marca de tiempo de la actualización más reciente de la conexión de datos de medición. |
| Última actualización de | Usuario que modificó por última vez la conexión de datos de medición. |
| Creado | La marca de tiempo cuando se creó la conexión de datos de medición. |
| Creado por | Usuario que creó originalmente la conexión de datos de medición. |

{style="table-layout:auto"}

### Claves de coincidencia {#match-keys}

Las claves de coincidencia son los campos de destino a los que asignó los campos de origen al [obtener los datos de medición](./onboard-measurement-data.md). Para obtener más información sobre cómo funcionan las claves de coincidencia, consulte la guía [claves de coincidencia](./onboard-account.md#set-up-match-keys).

![Área de trabajo de conexión de datos de medición con la sección Claves de coincidencia resaltada.](/help/assets/setup/manage-measurement-data-connection/view-match-keys.png){zoomable="yes"}

### Eventos de conversión {#conversion-events}

En la parte inferior del espacio de trabajo se muestra una lista de los eventos de conversión adjuntos a la conexión de datos. La lista muestra una breve descripción general de cada evento, incluido su estado, tipo de conversión y origen. Puede seleccionar el nombre del evento para ver y editar sus configuraciones o quitar el evento de conversión con la opción Eliminar (![Icono Eliminar](/help/assets/common/delete.svg)). Para obtener una guía completa sobre cómo administrar un evento de conversión, consulte la guía [agregar y administrar datos de medición](./onboard-measurement-data.md).

![Área de trabajo de conexión de datos de medición con la sección de eventos de conversión resaltada.](/help/assets/setup/manage-measurement-data-connection/view-conversion-events.png){zoomable="yes"}

## Editar conexión de datos de medición {#edit-measurement-data-connection}

Puede actualizar los detalles y las claves de coincidencia de una conexión de datos de medición existente en cualquier momento para garantizar que los informes y análisis sean precisos. Para empezar, vaya a la pestaña **[!UICONTROL Mis conexiones de datos]** y seleccione la conexión de datos de medición que desee editar. Esto abre el espacio de trabajo de conexión de datos, donde puede seguir los pasos a continuación para realizar los cambios necesarios.

### Editar nombre y descripción {#edit-name-and-description}

Para actualizar el nombre y la descripción de la conexión de datos, seleccione el icono de edición (![Editar icono](/help/assets/icons/edit.png)) junto al nombre de la conexión actual.

![Área de trabajo de conexión de datos de medición que resalta el icono Editar junto al nombre de la conexión de datos.](/help/assets/setup/manage-measurement-data-connection/edit-name-description.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL Editar conexión de datos]**, actualice los campos con los valores deseados y, a continuación, seleccione **[!UICONTROL Guardar]** para aplicar los cambios.

![Cuadro de diálogo Editar conexión de datos con la opción Guardar resaltada.](/help/assets/setup/manage-measurement-data-connection/edit-name-description-dialog.png){zoomable="yes"}

Aparecerá un cuadro de diálogo de confirmación para confirmar que los detalles se han actualizado correctamente.

### Editar claves de coincidencia {#edit-match-keys}

>[!IMPORTANT]
>
>Antes de editar las claves de coincidencia para una conexión de datos, tenga en cuenta lo siguiente:
>
>* Solo se pueden utilizar claves de coincidencia configuradas para su cuenta en las conexiones de datos.
>* En este momento, puede agregar claves de coincidencia adicionales a una conexión de datos, pero una vez que una clave de coincidencia está habilitada, no se puede eliminar.

En el área de trabajo de conexión de datos, seleccione **[!UICONTROL Editar]** en el panel **[!UICONTROL Claves de coincidencia]**.

![La sección Claves de coincidencia con la opción Editar resaltada.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys.png){zoomable="yes"}

Aparece un cuadro de diálogo de confirmación que explica que cualquier cambio en la conexión de datos se aplicará a todas las conversiones asociadas. Seleccione **[!UICONTROL Aceptar]** para confirmar. Puede optar por omitir esta confirmación en el futuro.

![Cuadro de diálogo de confirmación que muestra que cualquier cambio en la conexión de datos se aplicará a todas las conversiones asociadas.](/help/assets/setup/manage-measurement-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL Claves de coincidencia]**, puede revisar la configuración de enriquecimiento y ver las asignaciones actuales entre los campos de origen y los campos de destino (claves de coincidencia).

![Cuadro de diálogo Asignar claves que muestra la configuración de enriquecimiento y las asignaciones existentes entre los campos de origen y los campos de destino correspondientes.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys-dialog.png){zoomable="yes"}

#### Enriquecimiento {#enrichment}

Si el enriquecimiento no estaba habilitado al [obtener sus datos de medición](./onboard-measurement-data.md), tiene la opción de enriquecer su conjunto de datos de evento con atributos del perfil del cliente en tiempo real. Tenga en cuenta que una vez activado el enriquecimiento para los datos de medición, no se puede desactivar. Puede seguir actualizando las claves de combinación de enriquecimiento según sea necesario.

Cuando habilita el enriquecimiento en el cuadro de diálogo **[!UICONTROL Claves de coincidencia]**, la interfaz de usuario se amplía para mostrar más opciones de configuración en la sección **[!UICONTROL Enriquecimiento de los datos de evento con ID de perfiles]**.

Seleccione la opción **[!UICONTROL clave de combinación de campos Source]**.

![Se resaltó el cuadro de diálogo Coincidir claves con la opción de clave de combinación de campos de Source.](../../assets/setup/manage-measurement-data-connection/enrich-event-data.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL clave de combinación de campos de Source]**, elija el campo de origen, seguido de **[!UICONTROL Seleccionar]**.

![Cuadro de diálogo de clave de combinación de campos de Source que resalta el campo de origen seleccionado y la opción Siguiente.](../../assets/setup/manage-measurement-data-connection/source-field-join-key-dialog.png){zoomable="yes"}

A continuación, seleccione la opción **[!UICONTROL Clave de unión de perfil]**. En el cuadro de diálogo **[!UICONTROL Clave de unión de perfil]**, seleccione el campo de perfil de la lista. Puede utilizar la opción Buscar para encontrar el campo deseado. A continuación, elija **[!UICONTROL Seleccionar]** para confirmar.

![Cuadro de diálogo Clave de unión de perfil que resalta el campo de perfil seleccionado y la opción Seleccionar.](../../assets/setup/manage-measurement-data-connection/profile-join-key-dialog.png){zoomable="yes"}

#### Editar una asignación {#edit-mapping}

Para editar una clave de coincidencia existente, actualice su campo de origen y de destino asociados en el cuadro de diálogo **[!UICONTROL Claves de coincidencia]**. Si desea incluir una nueva clave de coincidencia, seleccione **[!UICONTROL Agregar campo]**. Esto crea una fila vacía en la que se puede definir una asignación adicional entre los campos de origen y destino.

![Después de seleccionar Agregar campo, el cuadro de diálogo Asignar claves muestra una nueva fila de asignación vacía lista para la entrada.](/help/assets/setup/manage-measurement-data-connection/add-new-field.png){zoomable="yes"}

A continuación, seleccione el campo de origen vacío. El cuadro de diálogo **[!UICONTROL Seleccionar campo de origen]** aparece con una lista de campos de origen disponibles agrupados en opciones como **[!UICONTROL Áreas de nombres de identidad]** y **[!UICONTROL Atributos de perfil]**. Puede filtrar la lista y buscar el campo de origen deseado con la opción de búsqueda.

Elija el campo de origen que desee, seguido de **[!UICONTROL Seleccionar]**.

![El cuadro de diálogo Seleccionar campo de origen resalta la opción Buscar, el campo Origen del teléfono y la opción Seleccionar.](/help/assets/setup/manage-measurement-data-connection/select-source-field.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL Claves de coincidencia]**, utilice el menú desplegable para asignar el nuevo campo de origen a un campo de destino. Todos los campos de destino disponibles son las claves de coincidencia configuradas para la cuenta de Collaborator. Si no ves el campo de destino que necesitas, [edita las claves de coincidencia](./onboard-account.md#edit-match-keys) de tu cuenta para agregarlo.

Utilice la opción **[!UICONTROL Aplicar transformación]** si desea crear un campo sin hash con un campo de destino con hash, por ejemplo, al asignar un campo de origen de teléfono de texto sin formato al campo de destino **[!UICONTROL Teléfono con hash]**.

![Menú desplegable que muestra todos los campos de destino disponibles para asignar con el nuevo campo de origen.](/help/assets/setup/manage-measurement-data-connection/target-field-dropdown.png){zoomable="yes"}

Una vez finalizada la asignación de campos, revisa las actualizaciones y selecciona **[!UICONTROL Confirmar]** para aplicar los cambios.

![Cuadro de diálogo Coincidir claves que muestra la asignación de campo actualizada con la opción Confirmar resaltada.](/help/assets/setup/manage-measurement-data-connection/confirm-edit-match-keys.png){zoomable="yes"}

Un cuadro de diálogo de confirmación confirma que las claves de coincidencia se actualizaron correctamente.

## Eliminar conexión de datos

Al eliminar una conexión de datos, se eliminarán todas las conversiones subyacentes, la configuración asociada y el uso en Collaboration. Esta acción no se puede deshacer.

Para eliminar una conexión de datos existente, seleccione el icono Eliminar (![Eliminar icono](/help/assets/common/delete.svg)) en el área de trabajo de una conexión de datos individual.

![Área de trabajo de conexiones de datos con la opción de eliminación resaltada.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection.png){zoomable="yes"}

Aparecerá un cuadro de diálogo de confirmación. Seleccione **[!UICONTROL Eliminar]** para finalizar la eliminación de la conexión de datos.

![Cuadro de diálogo Eliminar conexión de datos con la opción Eliminar resaltada.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection-confirm.png){zoomable="yes"}

Un cuadro de diálogo de confirmación confirma que la conexión de datos se eliminó correctamente.

## Próximos pasos {#next-steps}

Después de administrar las conexiones de datos de medición, puede:

* Añada más eventos de conversión vinculados a su conexión de datos según sea necesario. Para ver los pasos detallados, lea la documentación [agregar y administrar datos de medición](./onboard-measurement-data.md).
* Genere informes de medición para obtener información sobre el rendimiento y el impacto de su campaña. Para obtener más información sobre los tipos de informes disponibles y cómo crearlos, consulte la guía [medir el rendimiento](/help/guide/collaborate/measure.md).
