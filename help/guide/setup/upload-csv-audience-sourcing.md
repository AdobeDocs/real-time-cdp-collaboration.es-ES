---
title: Cargar archivo CSV para el abastecimiento de audiencias
description: Obtenga información sobre cómo cargar el archivo CSV como fuente de datos de autoservicio para introducir datos de audiencia en Real-Time CDP Collaboration.
source-git-commit: 96d3f87cedcfde73ce01c2b53c0b2ce4365fd277
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 0%

---

# Cargar archivo CSV para el abastecimiento de audiencias

Esta guía proporciona los pasos para cargar un archivo CSV en la interfaz de usuario de Adobe Real-Time CDP Collaboration para obtener los datos de audiencia y utilizarlos en proyectos de colaboración.

## Información general {#overview}

La carga de archivos CSV es un método para obtener datos de audiencia de origen para proyectos de colaboración. Esta es una alternativa a [conectar tu AWS S3 bucket](./configure-aws-s3-audience-sourcing.md) o [obtener audiencias de Experience Platform](./onboard-audiences.md).

Siga este flujo de trabajo para cargar un archivo CSV que contenga los datos de audiencia en el origen y administrar audiencias de origen en Collaboration. Puede asignar campos de identidad para la activación y el análisis de superposición. Una vez que se carga y procesa el archivo, la audiencia de origen queda disponible en el área de trabajo de **[!UICONTROL Mis audiencias]**, donde puede revisar, activar y administrar sus proyectos de colaboración.

>[!IMPORTANT]
>
>* Las audiencias que se obtuvieron mediante la carga de CSV están disponibles durante **7 días**. Después de este periodo, la audiencia caduca y debe volver a cargarse para usarla en sus proyectos de colaboración.
>
>* En este momento puede cargar un archivo CSV por sesión. Para añadir audiencias adicionales, complete de nuevo el flujo de trabajo de carga para cada archivo de origen que desee.

## Requisitos previos {#prerequisites}

Antes de cargar archivos CSV para el abastecimiento de audiencias, asegúrese de lo siguiente:

* Incorporación de la cuenta completada en Real-Time CDP Collaboration. Consulte [Incorporar su cuenta](./onboard-account.md) para obtener instrucciones paso a paso.
* Los permisos necesarios para agregar audiencias en su organización.
* Un archivo CSV que contiene los datos de audiencia con campos de identidad como correo electrónico o teléfono.

## Cargar un archivo CSV {#upload-csv-file}

En la ficha **[!UICONTROL Mis audiencias]** del área de trabajo **[!UICONTROL Configuración]**, seleccione el icono Agregar (![Agregar icono.](/help/assets/icons/plus.png)) y luego seleccione **[!UICONTROL Audiencia]**.

Si esta es su primera audiencia, también puede seleccionar la opción **[!UICONTROL Agregar]**.

![Se muestra la ficha Mis audiencias en el área de trabajo de configuración con el icono Agregar y la opción Agregar audiencia.](../../assets/setup/add-manage-audiences/add-audiences.png)

Aparecerá el flujo de trabajo Añadir audiencia. Seleccione **[!UICONTROL Agregar una nueva conexión de datos]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.

![Espacio de trabajo Agregar audiencias con la opción Agregar una nueva conexión de datos resaltada.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Seleccione Archivo CSV como conexión de datos {#select-csv-file}

Seleccione **[!UICONTROL Archivo CSV]** como conexión de datos, seguido de **[!UICONTROL Siguiente]**.

![La pantalla de selección de conexión de datos con el archivo CSV está disponible como opción seleccionable.](../../assets/setup/csv-audience-sourcing/select-csv-data-connection.png)

### Seleccionar archivo {#select-file}

Elija **[!UICONTROL Seleccionar del equipo]** para cargar un archivo CSV desde el sistema local. También puede arrastrar y soltar el archivo CSV que desee cargar en el panel [!UICONTROL Arrastrar y soltar un archivo CSV].

>[!IMPORTANT]
>
>Solo se admiten archivos CSV. El tamaño máximo de archivo es de **2 GB**.

![Seleccione un archivo CSV que contenga datos de audiencia de su sistema local.](../../assets/setup/csv-audience-sourcing/select-file.png)

Una vez cargada, la interfaz de usuario muestra un resumen que incluye el número de columnas, un recuento de filas estimado, la estructura del archivo y una vista previa de las primeras 10 filas de datos.

Revisa el resumen y luego selecciona **[!UICONTROL Siguiente]**.

![Obtenga una vista previa de los datos de audiencia de ejemplo desde el archivo CSV.](../../assets/setup/csv-audience-sourcing/preview-sample-data.png)

#### Reemplazar archivo {#replace-file}

Si necesita cargar un archivo CSV diferente, elija **[!UICONTROL Reemplazar archivo]** y seleccione el nuevo archivo. A continuación, la interfaz se actualiza para mostrar un resumen actualizado de los nuevos datos.

Después de revisar el resumen revisado, seleccione **[!UICONTROL Siguiente]**.

![Seleccione la opción Reemplazar archivo para cargar un archivo CSV diferente.](../../assets/setup/csv-audience-sourcing/replace-file.png)

### Confirmar confirmación de consentimiento {#confirm-consent}

Antes de continuar, debe reconocer que las exclusiones de consentimiento se han eliminado de los datos de audiencia. Collaboration requiere datos de audiencia limpios sin usuarios que se hayan excluido del uso compartido de datos.

Marque la casilla de confirmación seguida de **[!UICONTROL OK]** para confirmar. A continuación, se cierra el cuadro de diálogo y se continúa con la pantalla Asignar campos.

![El cuadro de diálogo de confirmación de exclusión de consentimiento que requiere confirmación antes de continuar.](../../assets/setup/csv-audience-sourcing/consent-optout-acknowledgment.png)

### Asignar campos de identidad de origen {#map-fields}

La asignación de campos determina cómo Collaboration utiliza los datos de audiencia para la activación y el análisis de superposición. En la pantalla **[!UICONTROL Asignar campos]**, utilice los menús desplegables para asignar cada campo de identidad de origen del archivo CSV al campo de destino adecuado en Collaboration.

Si necesita detalles adicionales sobre un campo de destino, incluido el tipo de datos o la descripción, seleccione **[!UICONTROL Detalles de campos de destino]** para obtener más información.

![Menú desplegable para asignar un campo de identidad de origen desde los datos de audiencia CSV al campo de destino en Collaboration.](../../assets/setup/csv-audience-sourcing/map-fields.png)

A continuación, revise los campos asignados y seleccione **[!UICONTROL Siguiente]**.

![Pantalla de asignación de campos que muestra los campos de identidad de origen y destino asignados.](../../assets/setup/csv-audience-sourcing/confirm-mapped-fields.png)

### Revisión y finalización de la carga {#review-and-complete}

La pantalla **[!UICONTROL Revisar]** aparece con un resumen de la configuración de audiencia del archivo CSV. Revise la información de las secciones siguientes:

* **[!UICONTROL Información de archivo]**: muestra el nombre de archivo, el número de columnas y el recuento estimado de filas.
* **[!UICONTROL Asignación]**: detalla cómo se asignan los campos de origen del archivo de audiencia cargado (por ejemplo, `email`) a los campos de destino utilizados en Collaboration (por ejemplo, correo electrónico con hash).

Seleccione el icono de lápiz si necesita editar una sección. Seleccione **[!UICONTROL Completar]** para confirmar todas las secciones.

![Revise el resumen de la configuración de carga, incluida la información del archivo CSV y los detalles de asignación de campos.](../../assets/setup/csv-audience-sourcing/review-upload-summary.png)

Aparecerá una barra de progreso debajo de las secciones de resumen para indicar el progreso de carga. Una vez finalizada la carga, un cuadro de diálogo de confirmación confirma que se ha creado la audiencia CSV y que el abastecimiento de audiencias está en curso.

![Después de cargar el archivo, aparece un cuadro de diálogo de confirmación que indica que se creó la audiencia CSV y que el abastecimiento de la audiencia está en curso.](../../assets/setup/csv-audience-sourcing/upload-success-sourcing-in-progress.png)

## Revisar audiencias de origen {#review-sourced-audiences}

Después de cargar el archivo CSV, Collaboration empieza a obtener audiencias a partir del archivo. Este proceso puede tardar varios minutos. Cuando finalice el abastecimiento, las audiencias estarán disponibles en la pestaña **[!UICONTROL Mis audiencias]** con las mismas características e información que las audiencias que provienen de Experience Platform.

![La pestaña Audiencias muestra una lista de audiencias de origen en la vista de cuadrícula.](../../assets/setup/csv-audience-sourcing/csv-audiences-list.png)

En la vista de cuadrícula o en la vista de tabla, seleccione un elemento de fila o **[!UICONTROL Ver audiencia]** para ver una descripción general de una audiencia específica. Muestra el estado de la audiencia, el origen y el nombre de la conexión de datos, junto con paneles detallados para:

**[!UICONTROL Identidades]**: muestra el recuento y el desglose de identidades totales cuando los datos están disponibles.
**[!UICONTROL Categorías]**: muestra todas las etiquetas utilizadas para organizar o filtrar la audiencia.
**[!UICONTROL Acceso a la conexión]**: Muestra si la audiencia es privada, pública o compartida con colaboradores específicos.
**[!UICONTROL Visibilidad de metadatos]**: Muestra qué información de audiencia (como recuento de identidades, porcentaje de superposición e índice) es visible para los colaboradores.

Utilice esta vista para confirmar los ajustes de configuración de audiencia y visibilidad antes de utilizar la audiencia en proyectos de colaboración. Para obtener más información, vea [cómo ver una audiencia individual](./onboard-audiences.md#view-individual-audiences).

## Próximos pasos {#next-steps}

Ahora ha cargado correctamente el archivo CSV en Collaboration. Una vez finalizado el abastecimiento, puede:

* Cree proyectos de colaboración con las audiencias de origen. Ver [Descubrir audiencias](../../guide/collaborate/discover.md).
* Activar audiencias en destinos conectados. Ver [Activar audiencias](../../guide/collaborate/activate.md).
* Revise la superposición de audiencias y las perspectivas. Ver [Medir el rendimiento de la campaña](../../guide/collaborate/measure.md).
* Administre la configuración y visibilidad de su audiencia. Ver [Source y administrar audiencias](./onboard-audiences.md).

Para obtener información acerca de otros métodos de obtención de audiencias, consulte [Configuración de AWS S3 para la obtención de audiencias](./configure-aws-s3-audience-sourcing.md) o [Audiencias de Source de Experience Platform](./onboard-audiences.md).
