---
title: Configurar  [!DNL Snowflake] para el Abastecimiento de audiencias
description: Aprenda a configurar y conectar su  [!DNL Snowflake Secure Data Share] fuente de datos de autoservicio para ingerir datos de audiencia en Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 517a28afc83b0e1b4a9e64fa53eb90e0ad5541e9
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 2%

---

# Configurar [!DNL Snowflake] para el abastecimiento de audiencia

Aprenda a configurar y conectar su [!DNL Snowflake Secure Data Share] en la interfaz de usuario de Adobe Real-Time CDP Collaboration a los datos de audiencia de origen para la activación y el análisis de superposición.

## Información general {#overview}

[!DNL Snowflake] es una de las opciones compatibles para obtener datos de audiencia de origen en Collaboration. Otros métodos disponibles incluyen el abastecimiento de audiencias de [Experience Platform](./onboard-audiences.md), la conexión de un [[!DNL AWS S3] contenedor](./configure-aws-s3-audience-sourcing.md) o la carga de un [archivo CSV](./upload-csv-audience-sourcing.md).

Siga los pasos a continuación para conectar su [!DNL Snowflake Secure Data Share] y obtener sus datos de audiencia en Collaboration. Una vez completada la configuración, puede revisar, activar y administrar las audiencias de origen para sus proyectos de colaboración.

## Requisitos previos {#prerequisites}

Antes de configurar la conexión de [!DNL Snowflake], asegúrese de cumplir los siguientes requisitos previos:

* Ha creado un [!DNL Snowflake Share] y ha configurado los permisos necesarios en su cuenta de [!DNL Snowflake] para conceder acceso a Adobe a su [!DNL Snowflake Secure Data Share].
* Tiene preparados los siguientes [!DNL Snowflake Share] valores:

   * **Nombre para compartir**
   * **Identificador de cuenta**
   * **Esquema**
   * **Ver**

* Los datos de audiencia de [!DNL Snowflake Secure Data Share] deben cumplir los requisitos de formato descritos en la guía [Especificación de fuentes de audiencia (v1.2)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf).
* Todas las claves de coincidencia del archivo de audiencia [!DNL Snowflake] también deben habilitarse para la cuenta de Collaboration. Aprenda a [habilitar las claves de coincidencia](./onboard-account.md#set-up-match-keys) o a [agregar nuevas claves de coincidencia](./onboard-account.md#edit-match-keys) a su cuenta.

## Configurar su conexión de [!DNL Snowflake] {#configure-snowflake-connection}

En la ficha **[!UICONTROL Mis audiencias]** del área de trabajo **[!UICONTROL Configuración]**, seleccione el icono de agregar (![Agregar icono.](/help/assets/icons/plus.png)) y luego seleccione **[!UICONTROL Audiencia]**.

Si esta es su primera audiencia, también puede seleccionar la opción **[!UICONTROL Agregar audiencia]**.

![Se muestra la ficha Mis audiencias en el área de trabajo de configuración con el icono Agregar y la opción Agregar audiencia.](../../assets/setup/snowflake-audience-sourcing/add-audience.png)

Aparecerá el flujo de trabajo Añadir audiencia. Seleccione **[!UICONTROL Agregar una nueva conexión de datos]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.

![Espacio de trabajo Agregar audiencias con la opción Agregar una nueva conexión de datos resaltada.](../../assets/setup/snowflake-audience-sourcing/add-data-connection.png){zoomable="yes"}

### Seleccione [!DNL Snowflake] como conexión de datos {#select-snowflake}

A continuación, selecciona **[!UICONTROL Snowflake]** como conexión de datos, seguido de **[!UICONTROL Siguiente]**.

![La pantalla de selección de conexión de datos con [!DNL Snowflake] está disponible como opción seleccionable.](../../assets/setup/snowflake-audience-sourcing/select-snowflake-data-connection.png)

### Revisar archivo de audiencia {#review-audience-file}

Aparecerá un cuadro de diálogo en el que se explicarán los requisitos de [!DNL Snowflake Share] y del archivo de audiencia [!DNL Snowflake] para poder iniciar el abastecimiento. Asegúrese de que su [!DNL Snowflake Share] se haya creado con el nombre de recurso compartido, el identificador de cuenta, el esquema y la vista correctos. Para confirmar que los datos de audiencias tienen el formato y la estructura correctos para su uso en Collaboration, consulte la guía **[[!UICONTROL Especificación de fuentes de audiencias]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)**.

Una vez finalizado, seleccione **[!UICONTROL Iniciar incorporación]**.

![Prepare su [!DNL Snowflake Share] para el cuadro de diálogo de incorporación con un vínculo a las especificaciones de fuentes de audiencias.](../../assets/setup/snowflake-audience-sourcing/prepare-snowflake-share-onboarding-dialog.png)

### Autenticar la conexión [!DNL Snowflake Share] {#authenticate-snowflake-share-connection}

En este paso, debe proporcionar las credenciales de [!DNL Snowflake Share] necesarias para conectar su [!DNL Snowflake Share] a Collaboration:

| Campo | Descripción | Ejemplo |
|--------------------|-------------|------------------------------|
| Compartir nombre | El nombre de su [!DNL Snowflake Share]. | `ADOBE_DATA_SHARE` |
| Identificador de cuenta | El identificador único de su cuenta de Snowflake. | `CUSTOMER_ORG.CUSTOMER_SNOWFLAKE_ACCOUNT` |
| Esquema | El esquema de su [!DNL Snowflake Share] que contiene sus datos de audiencia. | `CUSTOMER_SCHEMA` |
| Ver | El conjunto de datos real del que Collaboration extrae datos de audiencia. | `SECURE_VIEW_FOR_ADOBE` |

{style="table-layout:auto"}

Después de escribir todas las credenciales necesarias, seleccione **[!UICONTROL Siguiente]**.

![Se rellenó el formulario de conexión [!DNL Snowflake Share] con los campos Compartir nombre, Identificador de cuenta, Esquema y Ver, y se resaltó el botón Siguiente.](../../assets/setup/snowflake-audience-sourcing/snowflake-authentication-credentials-form.png)

Aparece un cuadro de diálogo de confirmación en la parte inferior de la página siguiente, que confirma que su [!DNL Snowflake Share] se ha conectado correctamente a Collaboration.

![Un cuadro de diálogo de confirmación confirma que la conexión [!DNL Snowflake Share] se estableció correctamente.](../../assets/setup/snowflake-audience-sourcing/snowflake-share-connection-established.png)

### Nombre y descripción {#provide-name-description}

En la vista **[!UICONTROL Proporcionar detalles]**, escriba un nombre descriptivo y una descripción opcional para la conexión de datos de [!DNL Snowflake]. Cuando termine, seleccione **[!UICONTROL Siguiente]**.

![La pantalla Proporcionar detalles muestra el nombre y la descripción de la conexión de datos, con el botón Siguiente resaltado.](../../assets/setup/snowflake-audience-sourcing/provide-name-description.png)

### Asignar campos {#map-fields}

La pantalla **[!UICONTROL Mapping]** es de solo lectura en este momento. No se pueden agregar, eliminar ni aplicar transformaciones. Collaboration asigna automáticamente los campos de identidad de origen de los datos de [!DNL Snowflake Share] a los campos de destino según la **[especificación de fuentes de audiencia (v1.2)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)**.

Confirme visualmente los campos asignados y seleccione **[!UICONTROL Siguiente]** para continuar. También puede obtener una vista previa de datos de ejemplo de su [!DNL Snowflake Share] con la opción **[!UICONTROL Vista previa de datos de origen]**.

![La pantalla Asignar campos muestra los campos de origen y destino asignados automáticamente, con las opciones Vista previa de datos de origen y Siguiente resaltadas.](../../assets/setup/snowflake-audience-sourcing/map-fields-screen.png)

Cuando elige obtener una vista previa, aparece el cuadro de diálogo **[!UICONTROL [!DNL Snowflake Share]vista previa de datos]** con datos de ejemplo mostrados en formato de tabla. Revise esto y luego seleccione **[!UICONTROL Cerrar]**.

El cuadro de diálogo de vista previa de datos de ![[!DNL Snowflake Share] muestra los datos de ejemplo de su [!DNL Snowflake Share] y la opción Cerrar resaltada.](../../assets/setup/snowflake-audience-sourcing/preview-source-data.png)

<!-- NOTE: Manual mapping will be available in the future. -->
<!-- In the **[!UICONTROL Map fields]** screen, you can use the **[!UICONTROL Source field]** and **[!UICONTROL Target field]** dropdowns to update the auto-mapped fields, or include additional fields with the **[!UICONTROL Add field]** option. Once finished, select **[!UICONTROL Next]**. -->

<!-- ![The Map fields screen showing the mapped fields with the Next option highlighted.](../../assets/setup/snowflake-audience-sourcing/map-fields.png) -->

### Frecuencia de actualización de programación e intervalo de fechas {#refresh-frequency-date-range}

A continuación, en la vista **[!UICONTROL Programar]**, utilice el menú desplegable para seleccionar la frecuencia de actualización entre uno y seis días. A continuación, utilice el icono de calendario para especificar las fechas de inicio y finalización de la audiencia de abastecimiento.

>[!IMPORTANT]
>
>Para administrar los créditos de Collaboration de manera efectiva, configure la frecuencia de actualización para que coincida o no exceda la frecuencia de actualización de los datos de [!DNL Snowflake] subyacentes. El intervalo mínimo de actualización admitido es de una vez cada seis días.

![La pantalla Programar resalta la frecuencia de actualización y las configuraciones del intervalo de fechas, así como la opción Siguiente.](../../assets/setup/snowflake-audience-sourcing/refresh-frequency-date-range.png)

### Revisión y finalización de la conexión {#review-and-complete}

Por último, revise los ajustes de configuración en la pantalla de resumen. Esta vista contiene un resumen de las secciones siguientes:

* **[!UICONTROL Conexión de datos]**: muestra el nombre del recurso compartido, el identificador de cuenta, el esquema y la vista de su [!DNL Snowflake Share].
* **[!UICONTROL Detalles]**: muestra el nombre y la descripción opcional de la conexión de datos para ayudar a identificarla más adelante.
* **[!UICONTROL Asignación]**: Muestra cómo se asignan los campos de origen del archivo de audiencia a los campos de destino utilizados en Collaboration.
* **[!UICONTROL Programación]**: Muestra la frecuencia con la que la conexión actualiza los datos de audiencia y el intervalo de fechas activo para el abastecimiento.

Seleccione el icono de lápiz (![Editar icono](/help/assets/icons/edit.png)) si necesita editar una sección. Seleccione **[!UICONTROL Completar]** para confirmar todas las secciones.

![La pantalla Revisar muestra un resumen de la conexión de datos, los detalles, la asignación y la configuración de programación, con la opción Completar resaltada.](../../assets/setup/snowflake-audience-sourcing/review-settings.png)

Un cuadro de diálogo de confirmación confirma que la conexión de datos se creó correctamente y que el abastecimiento de audiencia está en curso.

## Revisar audiencias de origen {#review-sourced-audiences}

Una vez completada la configuración, Collaboration empieza a obtener audiencias de su [!DNL Snowflake Share]. Si el abastecimiento de la audiencia está en curso, se muestra un banner en la parte superior de la vista.

![La pestaña Mis audiencias muestra el banner Fuente de audiencias en curso.](../../assets/setup/snowflake-audience-sourcing/audience-sourcing-in-progress.png)

>[!TIP]
>
>El tiempo de obtención de la audiencia varía según el tamaño de los datos de [!DNL Snowflake] y la frecuencia de actualización que haya configurado. Es posible que los conjuntos de datos más grandes o las programaciones de actualización menos frecuentes tarden más en aparecer en el área de trabajo **[!UICONTROL Mis audiencias]**.

Cuando finalice el abastecimiento, las audiencias estarán disponibles en la pestaña **[!UICONTROL Mis audiencias]** con las mismas características e información que las audiencias que provienen de Experience Platform.

![La ficha Mis audiencias muestra una lista de audiencias de origen en la vista tabular.](../../assets/setup/snowflake-audience-sourcing/snowflake-audience-list.png)

En la vista de cuadrícula o en la vista de tabla, seleccione un elemento de fila o **[!UICONTROL Ver audiencia]** para ver una descripción general de una audiencia específica. Muestra el estado de la audiencia, el origen y el nombre de la conexión de datos, junto con paneles detallados para **[!UICONTROL Identidades]**, **[!UICONTROL Categorías]**, **[!UICONTROL Acceso a la conexión]** y **[!UICONTROL Visibilidad de los metadatos]**. Consulte [cómo ver una audiencia individual](./onboard-audiences.md#view-individual-audiences) para obtener más información.

Utilice esta vista para confirmar los ajustes de configuración de audiencia y visibilidad antes de utilizar la audiencia en proyectos de colaboración.

## Ver su conexión de datos de [!DNL Snowflake] {#view-snowflake-connection}

La conexión [!DNL Snowflake] que acaba de agregar está disponible de inmediato en la ficha **[!UICONTROL Mis conexiones de datos]**. El origen de la audiencia se muestra como [!UICONTROL [!DNL Snowflake]].

Su conexión de datos de [!DNL Snowflake] incluye la misma funcionalidad y detalles que otras conexiones de datos de audiencia. Más información acerca de [cómo ver y administrar conexiones de datos](../setup/manage-data-connection.md).

![La ficha Mis conexiones de datos muestra la conexión de datos [!DNL Snowflake] con la información de estado de abastecimiento.](../../assets/setup/snowflake-audience-sourcing/data-connection-tab-snowflake.png)

## Próximos pasos {#next-steps}

Ahora ha configurado y conectado correctamente su [!DNL Snowflake] como origen de datos en Collaboration. Una vez finalizado el abastecimiento, puedes [crear proyectos de colaboración](../collaborate/manage-projects.md), [activar audiencias](../collaborate/activate.md), [revisar superposiciones y perspectivas](../collaborate/measure.md) y [administrar tu configuración de audiencia y visibilidad](./onboard-audiences.md).

Para obtener información sobre otros métodos de abastecimiento de audiencia, consulte la siguiente documentación:

* [Configurar  [!DNL Amazon S3] para el abastecimiento de audiencias](./configure-aws-s3-audience-sourcing.md)
* [Audiencias de Source de Experience Platform](./onboard-audiences.md)
* [Cargar archivo CSV para el abastecimiento de audiencias](./upload-csv-audience-sourcing.md)
