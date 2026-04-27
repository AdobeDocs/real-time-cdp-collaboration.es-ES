---
title: Source y administración de audiencias
description: Obtenga información sobre cómo crear y administrar audiencias en Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
TQID: https://experienceleague.adobe.com/aGnYCTj23Tth2Hbq1Y-ALmFPVa36vKCYWXVu3-8wf0Q
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 3680
ht-degree: 18%

---

# Source y administración de audiencias

{{limited-availability-release-note}}

Las audiencias son grupos específicos de usuarios o clientes segmentados según varios atributos. Esto permite a los colaboradores colaborar en marketing segmentado y experiencias personalizadas para lograr campañas publicitarias más eficaces. Esta guía explica cómo crear audiencias en Real-Time CDP Collaboration, ver el panel de audiencias y administrar audiencias individuales.

## Audiencias de Source en Collaboration {#source-audiences}

>[!IMPORTANT]
>
>Para las audiencias de origen, el usuario debe asignarse a una función que contenga dos permisos de Administración de perfiles: **[!UICONTROL Ver perfiles]** y **[!UICONTROL Ver segmentos]**. Para obtener información sobre cómo asignar los permisos necesarios, consulte la guía [obtención de audiencias](../permissions/overview.md#audience-sourcing) en permisos.

Para poder activar audiencias con colaboradores y ejecutar cálculos de superposición, las audiencias deben proceder de Collaboration. Para crear audiencias de origen, siga los pasos de flujo de trabajo de la sección siguiente.

En la ficha **[!UICONTROL Mis audiencias]** del área de trabajo **[!UICONTROL Configuración]**, seleccione el icono de agregar (![Agregar icono.](/help/assets/icons/plus.png)) y luego seleccione **[!UICONTROL Audiencia]**. Si esta es su primera audiencia, también puede seleccionar la opción **[!UICONTROL Agregar]**.

![Área de trabajo de Mis audiencias con la opción Agregar y las opciones de Audiencias resaltadas.](/help/assets/setup/add-manage-audiences/add-audiences.png){zoomable="yes"}

### Seleccionar conexión de datos {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Acción de marketing"
>abstract="<p>Utilice acciones de marketing para controlar qué datos del público se importarán a Real-Time CDP Collaboration desde Experience Platform. La acción de marketing <strong>Colaboración de datos</strong> admite las etiquetas de uso de datos C4, C5 y C9. La acción de marketing <strong>Ciencia de datos</strong> admite la etiqueta de uso de datos C9.</p> <p> <ul><li> Con la casilla de verificación <em>habilitada</em>, cualquier dato marcado con las etiquetas llamadas arriba en Experience Platform se excluye y <strong>no</strong> se incorpora a Real-Time CDP Collaboration.</li><li> Con la casilla de verificación <em>deshabilitada</em>, no hay restricciones en los datos de Experience Platform que se pueden importar a Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=es" text="Información general sobre las etiquetas de uso de datos"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=es" text="Glosario de etiquetas de uso de datos"

>[!IMPORTANT]
>
>Después de establecer en la primera conexión de datos y obtener la primera audiencia, puede obtener varias audiencias a partir de la conexión de datos existente. Al agregar audiencias adicionales, empezará desde el paso [seleccionar audiencia](#select-audiences), ya que la conexión de datos ya se ha establecido.

Una conexión de datos es la fuente desde la que se introducen audiencias en Collaboration. Los orígenes admitidos son Adobe Experience Platform, carga de archivo CSV, [!DNL Amazon S3], [!DNL Snowflake] y [!DNL Google Cloud Storage], cada uno con su propio flujo de trabajo.

Las secciones siguientes describen cómo seleccionar **Adobe Experience Platform** y completar los pasos específicos de Experience Platform (simulación de pruebas, administración y consentimiento). Si elige CSV, [!DNL Amazon S3], [!DNL Snowflake] o [!DNL Google Cloud Storage], use la guía vinculada en [Seleccionar origen de datos](#select-data-source) para esa opción.

Cualquier configuración que establezca para una conexión de datos de Experience Platform se aplicará a todas las audiencias procedentes de esa conexión.

>[!TIP]
>
>Hay un flujo de trabajo independiente en el que puede ver y editar las conexiones de datos. For more information, follow the [managing data connections](/help/guide/setup/manage-data-connection.md) guide.

To begin adding your data connection, select **[!UICONTROL Add a new data connection]** and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Add a new data connection option highlighted.](/help/assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

#### Select data source

Next, you&#39;ll choose the source for your data connection. The available sources include:

* **Adobe Experience Platform**: Select this option to bring in your audiences from Adobe Experience Platform.
* **CSV File**: Upload a CSV file containing your audience data for quick and straightforward data ingestion. Refer to the [Upload CSV file for audience sourcing](./upload-csv-audience-sourcing.md) guide to get started.
* **Amazon Web Services**: Connect to your Amazon S3 storage to source audience data directly from your S3 buckets. See the [Configure AWS S3 for audience sourcing](./configure-aws-s3-audience-sourcing.md) guide for step-by-step instructions.
* **Snowflake**: Use your Snowflake data warehouse to pull in audience data seamlessly. Refer to the [Configure [!DNL Snowflake] for audience sourcing](./configure-snowflake-audience-sourcing.md) guide.
* **Google Cloud Storage**: Connect to your GCS buckets to source audience data. See the [Configure GCS for audience sourcing](./configure-gcs-audience-sourcing.md) guide for step-by-step instructions.

Select your data source and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Adobe Experience Platform option highlighted.](/help/assets/setup/add-manage-audiences/select-data-connection-source.png){zoomable="yes"}

#### Selección de zona protegida

After selecting your data source, you must select the sandbox that includes the audiences that you want to use for Collaboration. Select the sandbox from the list of available sandboxes and then select **[!UICONTROL Next]**

![The Add audiences workspace with a sandbox selected.](/help/assets/setup/add-manage-audiences/select-sandbox.png){zoomable="yes"}

#### Política de gobernanza y acciones de cumplimiento {#governance-policy-and-enforcement-actions}

Next, you must make sure that the correct marketing actions are set on the sourced data. You are also required to provide consent for data sourced from Experience Platform to be used for data collaboration.

Use marketing actions to control which audience data to bring into Collaboration from Experience Platform. La acción de marketing **[!UICONTROL Colaboración de datos]** admite las etiquetas de uso de datos C4, C5 y C9. La acción de marketing **[!UICONTROL Ciencia de datos]** admite la etiqueta de uso de datos C9.

Read more about the [C4, C5, and C9 data usage labels](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* When the checkbox is ***enabled***, any data labeled in Experience Platform as described above is excluded and **not** brought into Collaboration.
* Con la casilla de verificación ***deshabilitada***, no hay restricciones en los datos procedentes de Experience Platform.

Obtenga más información sobre las etiquetas de uso de datos en la documentación de Experience Platform:

* [Información general sobre las etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Glosario de etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Además, debe seleccionar las reglas de consentimiento que se aplicarán a los datos que se obtienen en Collaboration.

![Espacio de trabajo Agregar audiencias en la sección Directiva de administración y acciones de cumplimiento.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png){zoomable="yes"}

Una vez que haya seleccionado las acciones de marketing y las reglas de consentimiento, seleccione **[!UICONTROL Siguiente]** para continuar con el paso siguiente. Aparecerá un cuadro de diálogo de confirmación en el que se le pedirá que acepte los términos. Seleccione la casilla de verificación y, a continuación, seleccione **[!UICONTROL Aceptar]** para confirmar.

![Cuadro de diálogo Directiva de gobernanza y acciones de aplicación con la casilla de verificación y la opción Aceptar resaltadas.](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png){zoomable="yes"}

### Proporcionar detalles

A continuación, proporcione un nombre y una descripción para la conexión de datos. Esta información le ayudará a identificar la conexión de datos más adelante.

![El área de trabajo Agregar audiencias tiene la opción de proporcionar un nombre y una descripción.](/help/assets/setup/add-manage-audiences/data-connection-details.png){zoomable="yes"}

### Asignar campos {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Campos de origen"
>abstract="Los campos de origen son espacios de nombres de identidad y atributos de la implementación de Experience Platform. Puede asignarlos a los campos de destino definidos en Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Campos de destino"
>abstract="Los campos de destino son las claves de coincidencia seleccionadas durante la configuración de la cuenta. De forma predeterminada, todas las claves de coincidencia seleccionadas están disponibles."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Aplicar transformación"
>abstract="Al importar campos *sin hash* desde su origen, utilice esta opción para que Collaboration aplique el hash y transforme los campos sin formato en campos con hash."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="Espacios de nombres de identidad"
>abstract="Seleccione un espacio de nombres de identidad del espacio de nombres de identidad estándar y personalizados disponibles en su organización de Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=es#standard" text="Espacios de nombres estándar y de identidad de Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="Atributos de perfil"
>abstract="Seleccione atributos del esquema de unión para la clase de perfil en Experience Platform. Esta vista muestra los atributos que están presentes en el esquema de unión y pertenecen a la clase de perfil individual XDM."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=es" text="Esquema de unión en Experience Platform"

A continuación, seleccione los campos de origen para asignarlos a los campos de destino en Collaboration. Los campos de destino disponibles se basarán en las claves de coincidencia seleccionadas durante la configuración de la cuenta.

>[!IMPORTANT]
>
>Actualmente, no se pueden editar conexiones de datos para incluir nuevos campos de asignación. Si agrega nuevas claves de coincidencia a su cuenta después de crear la conexión de datos, deberá crear una nueva conexión de datos para asignarla a ellas.

![Espacio de trabajo Agregar audiencias con la opción de asignar campos de origen a campos de destino.](/help/assets/setup/add-manage-audiences/add-map-fields.png){zoomable="yes"}

>[!TIP]
>
>Puede asignar varios campos de origen al mismo campo de destino. Por ejemplo, si tiene direcciones de correo electrónico en dos campos distintos en Experience Platform, puede asignar cada uno de ellos al campo de destino **[!UICONTROL Correo electrónico con hash]** como dos filas independientes. Utilice la opción **[!UICONTROL Agregar campo]** para agregar filas de asignación adicionales.

>[!BEGINSHADEBOX]

**[!UICONTROL Los campos de Source]** son áreas de nombres y atributos de identidad de Experience Platform. Estas incluyen áreas de nombres de identidad [standard](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=es#standard){target="_blank"} y [custom](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#create-namespaces){target="_blank"}. También incluyen atributos de perfil que están presentes en el [esquema de unión](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=es){target="_blank"} y pertenecen a la clase XDM Individual Profile.

Los campos de Source se asignan a los campos de destino definidos en Collaboration.

**[!UICONTROL Campos de destino]** indican cómo se hace referencia a las identidades en Collaboration. Los campos de destino son las claves de coincidencia seleccionadas durante la configuración de la cuenta. De forma predeterminada, todas las claves de coincidencia seleccionadas están disponibles.

Utilice la opción **[!UICONTROL Aplicar transformación]** cuando esté suministrando *campos sin hash* a campos con hash. Collaboration will apply the hashing and transform the fields. The hashing algorithm used by Adobe is SHA256.

>[!ENDSHADEBOX]

To begin mapping fields, select the empty source field next to the target field. The **[!UICONTROL Select source field]** dialog will appear. Select between the **[!UICONTROL Identity namespaces]** and **[!UICONTROL Profile attributes]** options to find the desired source field and then select the field from the list. You can also make use of the search option to find the desired field.

![The Select source field dialog with the email options displayed.](/help/assets/setup/add-manage-audiences/select-source-field.png){zoomable="yes"}

To handle sourcing a non-hashed field to a hashed target field, use the **[!UICONTROL Apply transformation]** option. For example, to add a second email field, select the **[!UICONTROL Add field]** option to to add a new row, then select **[!UICONTROL Hashed email]** for the target field. Select a non-hashed email source field, and then select **[!UICONTROL Apply transformation]**.

![The Add audiences workspace with the email source fields mapped to the target field, with Apply transformation toggled on for one.](/help/assets/setup/add-manage-audiences/apply-transformation.png){zoomable="yes"}

Continue adding mapping pairs for each target field. If you don&#39;t wish to use a match key, you can remove it using the delete (![Delete icon](/help/assets/icons/delete.png)) icon next to the field. If match key is removed, you will not be able to use it when sourcing any audiences from the connection.

![The Add audiences workspace with the Delete option beside a target field highlighted.](/help/assets/setup/add-manage-audiences/remove-target-field.png){zoomable="yes"}

When you&#39;re finished mapping fields, select **[!UICONTROL Next]** to continue.

![The Add audiences workspace with the map fields filled in and the Next option highlighted.](/help/assets/setup/add-manage-audiences/confirm-field-mapping.png){zoomable="yes"}

### Programación {#schedule}

Next, schedule when to start and end populating the audiences. The audience will be refreshed according to this schedule.

![The Add audience workspace with the scheduling options displayed.](/help/assets/setup/add-manage-audiences/audience-scheduling.png){zoomable="yes"}

>[!IMPORTANT]
>
>Adjusting the frequency of audience updates will help manage the [Audience Management credit activity](/help/guide/setup/my-activity.md#types-of-activities), which is calculated per audience refresh. Selecting a higher frequency can impact of the freshness of the data available for audience discover reports and audience activation.

Select the frequency of the audience refresh from the **[!UICONTROL Frequency]** dropdown.

![The Add audiences scheduling workspace with the Frequency dropdown open.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png){zoomable="yes"}

Next, select the **[!UICONTROL Date range]**. La fecha de inicio es la fecha en la que la audiencia empezará a rellenarse con perfiles y la fecha de finalización es cuando la audiencia dejará de actualizarse.

![Espacio de trabajo de programación Agregar audiencias con la opción Intervalo de fechas mostrada.](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png){zoomable="yes"}

>[!IMPORTANT]
>
>Después de la fecha de finalización en el intervalo de fechas, todas las audiencias procedentes de esta conexión de datos dejarán de actualizarse. Para renovar la conexión, sigue la guía [administrar conexión de datos](/help/guide/setup/manage-data-connection.md).

### Seleccionar públicos {#select-audiences}

Después de seleccionar la fuente de audiencia, elegirá las audiencias específicas que desea incluir. Utilice las opciones de búsqueda y filtro para encontrar las audiencias relevantes de su conexión de datos. Seleccione las audiencias que desee y luego seleccione **[!UICONTROL Siguiente]**.

![Espacio de trabajo Agregar audiencias con una lista de audiencias disponibles.](/help/assets/setup/add-manage-audiences/select-audience.png){zoomable="yes"}

### Revisar

Revise todas las configuraciones y ajustes de antes de finalizar la adición de audiencias. Asegúrese de que todos los detalles sean correctos y, a continuación, seleccione **[!UICONTROL Completar]** para finalizar la creación de la conexión de datos.

![Espacio de trabajo Agregar audiencias con todas las configuraciones seleccionadas mostradas.](/help/assets/setup/add-manage-audiences/review-connection.png){zoomable="yes"}

## Panel de control de vista de públicos {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Identidades que faltan"
>abstract="El recuento de identidades estará disponible tras la siguiente actualización de la conexión de datos siguiendo la programación configurada. La actualización inicial suele producirse en las 24 horas siguientes al establecimiento de la conexión de datos. Las actualizaciones continuas seguirán la programación configurada."

Después de obtener audiencias, el área de trabajo **[!UICONTROL Mis audiencias]** muestra todas las audiencias que provienen actualmente de Collaboration.

![Área de trabajo Mis audiencias que muestra todas las audiencias de origen.](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

Cada audiencia contiene una descripción general de la siguiente información:

| Elemento | Descripción |
|----------|---------|
| **[!UICONTROL Nombre]** | Nombre de la audiencia. |
| **[!UICONTROL Identidades]** | Indica el número de identidades presentes en esta audiencia. Tenga en cuenta que si el mismo perfil tiene dos o más identidades y estas identidades se utilizan como claves de coincidencia en el proyecto, el perfil aparecerá dos veces en el recuento. |
| **[!UICONTROL Estado]** | Indica si la audiencia está activa y si se puede utilizar en proyectos. El estado **[!UICONTROL Pendiente]** indica que la audiencia se ha originado recientemente y que las identidades aún no se han rellenado. Las audiencias de origen se rellenarán con perfiles después de la actualización inicial, que generalmente se produce dentro de las 24 horas siguientes a la configuración de la conexión de datos. |
| **[!UICONTROL Source]** | Indica el origen de la audiencia. En la versión actual de Collaboration, Experience Platform es la única fuente compatible. |
| **[!UICONTROL Conexión de datos]** | La conexión de datos desde la que se origina la audiencia. Puede seleccionar el nombre para ver la conexión de datos. |
| **[!UICONTROL Acceso a la conexión]** | Define si la audiencia es pública o privada. Las audiencias públicas se pueden descubrir en los informes de superposición y se pueden activar dentro de un proyecto. |
| **[!UICONTROL Creado]** | Indica cuándo se originó la audiencia inicialmente en Collaboration. |
| **[!UICONTROL Última actualización]** | Indica la última fecha y hora en que la audiencia se actualizó en Collaboration. Esto no hace referencia a la última actualización de la audiencia, sino a la última modificación de la configuración o los metadatos de la audiencia. |

![Área de trabajo de Mi audiencia que muestra todas las audiencias de origen.](/help/assets/setup/add-manage-audiences/audiences-workspace.png){zoomable="yes"}

Para realizar acciones rápidas en una audiencia, seleccione los puntos suspensivos **...** junto al nombre de la audiencia. Las opciones disponibles son las siguientes:

* **[!UICONTROL Editar categorías]** le permite agregar diferentes etiquetas de categoría a la audiencia. Para obtener más información, consulte la sección [categorías](#categories) a continuación.
* **[!UICONTROL Eliminar]** eliminará la audiencia de la conexión de datos.

![Área de trabajo Mis audiencias con el menú de los tres puntos abierto y las opciones Editar categorías y Eliminar resaltadas.](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png){zoomable="yes"}

## Ver audiencias individuales {#view-individual-audiences}

Para ver y actualizar la información de una audiencia individual, seleccione la audiencia en el área de trabajo **[!UICONTROL Mis audiencias]**. El espacio de trabajo de audiencia muestra información detallada sobre la audiencia seleccionada, incluidos detalles, identidades, categorías, acceso a conexiones y configuración de visibilidad de metadatos.

### Detalles de público

Se muestra la siguiente información para cada audiencia individual:

| Elemento | Descripción |
|----------|---------|
| **[!UICONTROL Estado]** | Indica si la audiencia está activa y si se puede utilizar en proyectos. |
| **[!UICONTROL Source]** | Indica el origen de la audiencia. En la versión actual de Collaboration, Experience Platform es la única fuente compatible. |
| **[!UICONTROL Conexión de datos]** | La conexión de datos desde la que se origina la audiencia. |
| **[!UICONTROL Última actualización]** | Indica la última fecha y hora en que la audiencia se actualizó en Collaboration. Esto no hace referencia a la última actualización de la audiencia, sino a la última modificación de la configuración o los metadatos de la audiencia |
| **[!UICONTROL Última actualización por]** | Indica el usuario que actualizó la audiencia por última vez. |
| **[!UICONTROL Creado]** | Indica cuándo se originó la audiencia inicialmente en Collaboration. |
| **[!UICONTROL Creado por]** | Indica el usuario que originó la audiencia en Collaboration. |

![Espacio de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details.png){zoomable="yes"}

#### Identidades {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identidades"
>abstract="Una vista desglosada de las identidades que componen este público separadas por una clave de coincidencia."

La sección **[!UICONTROL Identidades]** indica la cantidad de identidades presentes en la audiencia. La sección también contiene un desglose de identidades por clave de coincidencia para ayudarle a comprender la composición de la audiencia.

![La sección Identidades del espacio de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details-identities.png){zoomable="yes"}

Al pasar el ratón por encima de las secciones individuales del desglose de claves de coincidencia, se proporciona un recuento de identidad preciso para la clave correspondiente.

![La sección Identidades del espacio de trabajo de una audiencia individual con un desglose de clave de coincidencia.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

#### Categorías {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Categorías"
>abstract="Etiquete sus públicos para facilitar la organización, el filtrado y la recuperación. Puede etiquetar un público con varias categorías y, a continuación, puede utilizar estas etiquetas de categoría para filtrar los públicos que desee en otras áreas del producto."

Para facilitar la organización, el filtrado y la recuperación de audiencias, puede etiquetar sus audiencias. Puede etiquetar una audiencia con varias categorías y, a continuación, puede usar estas etiquetas de categoría para filtrar las audiencias que desee en el área de producto [Discover](/help/guide/collaborate/discover.md) al ejecutar informes de superposición de audiencias.

Para agregar categorías, seleccione la opción **[!UICONTROL Editar]** en la sección **[!UICONTROL Categorías]**.

![La sección Categorías del espacio de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details-categories.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Categorías]**, que le permitirá seleccionar las categorías que desee agregar a la audiencia. Para seleccionar una categoría individual, marque la casilla que hay junto al nombre de la categoría.


#### Acceso a la conexión {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Acceso a la conexión"
>abstract="<p>Los públicos pueden ser de tres tipos: públicos, privados y personalizados.</p><p> Su disponibilidad para el uso en proyectos con los colaboradores difiere según la configuración de acceso a la conexión.</p>"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_access"
>title="Más información"
>abstract=""

La disponibilidad de una audiencia para su uso en proyectos con colaboradores difiere según la configuración de acceso a la conexión. En la sección **[!UICONTROL Acceso a la conexión]**, puede seleccionar si la audiencia debe ser privada, pública o solo disponible para conexiones específicas. Las audiencias públicas se pueden utilizar y detectar en conexiones.

Para actualizar el acceso a la conexión de la audiencia, seleccione la opción **[!UICONTROL Editar]** en la sección **[!UICONTROL Acceso a la conexión]**.

![La sección de acceso a la conexión del área de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Acceso a conexión]**, con tres opciones de acceso a conexión disponibles:

* **[!UICONTROL Audiencia privada]**. Estas audiencias *no* están disponibles para su uso en informes de superposición o para su activación en conexiones con colaboradores. Aunque las audiencias no están disponibles para que los colaboradores las vean o utilicen, la población de las audiencias sigue contribuyendo a la población total en la vista **[!UICONTROL Todas las audiencias]** en la sección [comparar audiencias](/help/guide/collaborate/discover.md#compare-audiences). Cambie la configuración a pública o personalizada para utilizar las audiencias en conexiones con los colaboradores.
* **[!UICONTROL Público]**. Estas audiencias están disponibles para usarlas en informes de superposición y para activarlas en conexiones con cualquier colaborador.
* **[!UICONTROL Audiencia personalizada]**. Estas audiencias están disponibles para usarlas en informes de superposición y solo para activarlas en conexiones especificadas. Aunque las audiencias no están disponibles para que los colaboradores las vean o utilicen, la población de las audiencias sigue contribuyendo a la población total en la vista **[!UICONTROL Todas las audiencias]** en la sección [comparar audiencias](/help/guide/collaborate/discover.md#compare-audiences).

Seleccione la opción de acceso a la conexión que desee y, a continuación, seleccione **[!UICONTROL Guardar]** para aplicar los cambios.

![Cuadro de diálogo de acceso a la conexión con las opciones disponibles mostradas.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png){zoomable="yes"}

>[!IMPORTANT]
>
>Independientemente del estado del acceso (público, privado o personalizado), la población de cualquier audiencia contribuye a la población de **[!UICONTROL Todas las audiencias]** en la sección **[!UICONTROL Comparar audiencias]** dentro de un proyecto.

La disponibilidad de la audiencia para su uso en proyectos con colaboradores difiere según la configuración de acceso a la conexión.

#### Visibilidad de los metadatos {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Visibilidad de los metadatos"
>abstract="<p>Indica qué metadatos del público son visibles para otros colaboradores antes de que se conecten con usted o dentro de las vistas del proyecto.</p> <p> **Recuento de identidad** controla si su colaborador puede ver los recuentos de identidad de sus públicos cuando visualiza los informes de superposición en la pestaña de detección.</p><p> El **Porcentaje de solapamiento de público** controla si los colaboradores pueden descubrir los porcentajes de solapamiento entre sus públicos y los suyos.</p><p> **[!UICONTROL Índice de público]** controla si los colaboradores pueden ver el índice de público dentro de un proyecto. Esta funcionalidad solo está disponible cuando tiene tres o más públicos activos.</p> <br> Para que la configuración de visibilidad de metadatos surta efecto, el público debe establecerse en público o personalizado."

>[!NOTE]
>
>Si su colaborador tiene todas las audiencias definidas como privadas, la sección **[!UICONTROL Audiencias relevantes]** de un proyecto en el área de trabajo **[!UICONTROL Discover]** estará en blanco. Para obtener más información, lea la guía [Discover](/help/guide/collaborate/discover.md#relevant-audiences).

La visibilidad de los metadatos indica la visibilidad de los metadatos de una audiencia para otros colaboradores antes de que se conecten con usted o en diferentes vistas de proyecto. Para actualizar la visibilidad de los metadatos de la audiencia, seleccione la opción **[!UICONTROL Editar]** en la sección **[!UICONTROL Visibilidad de los metadatos]**.

![La sección de visibilidad de metadatos del espacio de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details-metadata-visibility.png){zoomable="yes"}

Aparece el cuadro de diálogo **[!UICONTROL Visibilidad de metadatos]**, que le permite configurar las opciones de visibilidad de la audiencia. Hay dos ajustes de visibilidad de metadatos que puede configurar para cada audiencia:

**[!UICONTROL Mostrar recuento de identidades]**: esta opción controla si el colaborador puede ver los recuentos de identidades de las audiencias al [ver informes de superposición en la ficha de detección](/help/guide/collaborate/discover.md#discover-overlaps) dentro de un proyecto.

**[!UICONTROL Mostrar superposición de audiencias %]**: esta opción controla si los colaboradores pueden [descubrir porcentajes de superposición](/help/guide/collaborate/discover.md#compare-audiences) entre sus audiencias y las suyas.

**[!UICONTROL Índice de audiencia]**: cuando se establece en true, los colaboradores pueden ver [índice de audiencia](/help/guide/collaborate/discover.md#audience-index-score) dentro de un proyecto. Esta funcionalidad solo está disponible cuando tiene tres o más públicos activos.

>[!NOTE]
>
>Para que la configuración de visibilidad de los metadatos surta efecto, la audiencia debe configurarse como pública o personalizada.

![Cuadro de diálogo de visibilidad de metadatos con las opciones disponibles mostradas.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png){zoomable="yes"}

## Editar varias audiencias {#edit-audiences}

Desde el panel de audiencias, puede editar varias audiencias a la vez. Para ello, seleccione las audiencias que desee editar seleccionando los cuadros junto a sus nombres. Una vez seleccionadas las audiencias, puede realizar acciones con las opciones disponibles en el menú de edición.

![Área de trabajo Mis audiencias con dos audiencias seleccionadas y el menú de edición resaltado.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit.png)

### Visibilidad de metadatos de edición masiva {#bulk-edit-metadata-visibility}

Con las audiencias seleccionadas en el panel de audiencias, seleccione **[!UICONTROL Editar visibilidad de metadatos]** en el menú de edición.

![Área de trabajo de Mis audiencias con la opción Editar visibilidad de metadatos resaltada.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-metadata.png)

Aparece el cuadro de diálogo **[!UICONTROL Visibilidad de metadatos]**, que le permite configurar las opciones de visibilidad de las audiencias seleccionadas. De forma predeterminada, no se selecciona ninguna de las opciones. Elige las opciones que deseas aplicar a todas las audiencias seleccionadas y luego selecciona **[!UICONTROL Guardar]**.

![Cuadro de diálogo de visibilidad de metadatos con las opciones disponibles mostradas.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

### Acceso a conexión de edición masiva {#bulk-edit-connection-access}

Con las audiencias seleccionadas en el panel de audiencias, seleccione **[!UICONTROL Editar acceso a conexión]** del menú de edición.

![Área de trabajo de Mis audiencias con la opción de acceso Editar conexión resaltada.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-connection-access.png)

Aparecerá el cuadro de diálogo **[!UICONTROL Acceso a la conexión]**, que le permitirá configurar los ajustes de acceso para las audiencias seleccionadas. De manera predeterminada, se seleccionará la opción **[!UICONTROL Audiencia privada]**. Elige las opciones que deseas aplicar a todas las audiencias seleccionadas y luego selecciona **[!UICONTROL Guardar]**.

![Cuadro de diálogo de acceso a la conexión con las opciones disponibles mostradas.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

### Edición masiva de nombres y descripciones de audiencias {#bulk-edit-audience-names-descriptions}

Con las audiencias seleccionadas en el panel de audiencias, seleccione **[!UICONTROL Editar nombre y descripción]** en el menú de edición.

![Área de trabajo de Mis audiencias con la opción Editar nombre y descripción resaltada.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description.png)

Aparecerá el cuadro de diálogo **[!UICONTROL Nombre y descripción]**, que le permitirá configurar el nombre y la descripción de cada audiencia seleccionada. De forma predeterminada, se muestran los nombres y las descripciones actuales de cada audiencia. Realice los cambios y seleccione **[!UICONTROL Guardar]**.

![Cuadro de diálogo Nombre y descripción con las opciones disponibles mostradas.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description-dialog.png)

### Editar categorías de forma masiva {#bulk-edit-categories}

Con las audiencias seleccionadas en el panel de audiencias, seleccione **[!UICONTROL Editar categorías]** en el menú de edición.

![Área de trabajo Mis audiencias con la opción Editar categorías resaltada.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories.png)

Aparece el cuadro de diálogo **[!UICONTROL Categorías]**, que le permite configurar las categorías para cada audiencia seleccionada. De forma predeterminada, no se seleccionará ninguna categoría. Para seleccionar una categoría, primero seleccione la categoría principal y luego seleccione las subcategorías que desee incluir. Realice los cambios y seleccione **[!UICONTROL Guardar]**.

![Cuadro de diálogo Categorías con las opciones disponibles mostradas.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories-dialog.png)

## Próximos pasos

Después de obtener audiencias, es hora de descubrir colaboradores con los que [conectar](/help/guide/connect/establishing-connections.md) para colaborar en proyectos.
