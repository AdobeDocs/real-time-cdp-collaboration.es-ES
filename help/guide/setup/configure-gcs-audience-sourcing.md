---
title: Configurar  [!DNL Google Cloud Storage] para el Abastecimiento de audiencias
description: Aprenda a conectar un contenedor  [!DNL Google Cloud Storage] como fuente de audiencia de autoservicio en Real-Time CDP Collaboration, incluidos los requisitos previos, la autenticación, la asignación de campos, la programación y la validación.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 4f7cb15ab5747a50d42188d03bc352c1fb05263b
workflow-type: tm+mt
source-wordcount: '2858'
ht-degree: 2%

---


# Configurar [!DNL Google Cloud Storage] para el abastecimiento de audiencia

Siga los pasos de esta guía para conectar su bloque de [!DNL Google Cloud Storage] (GCS) a Adobe Real-Time CDP Collaboration y comenzar a obtener datos de audiencia de origen a través de la interfaz de usuario.

Conecte un bloque GCS a Collaboration para introducir datos de audiencia de origen directamente sin soporte de ingeniería. Una vez conectada, Collaboration obtiene las audiencias de su bloque en una programación recurrente y las pone a disposición para la activación y el análisis de superposición dentro de sus proyectos de colaboración. Abastecer las audiencias es un paso necesario para poder activarlas o utilizarlas en análisis de superposición con colaboradores.

Esta guía cubre el flujo de trabajo de configuración completo: preparación de requisitos previos, autenticación del bloque GCS, revisión de campos de identidad asignados automáticamente, programación de la actualización de datos y confirmación de que el abastecimiento se ha completado correctamente.

Las audiencias provenientes de [!DNL Google Cloud Storage] siguen las mismas reglas de gobernanza y administración de datos que las audiencias provenientes de Adobe Experience Platform.

Otros métodos de obtención disponibles incluyen [Experience Platform](./onboard-audiences.md), [Amazon S3](./configure-aws-s3-audience-sourcing.md), [Snowflake](./configure-snowflake-audience-sourcing.md) y [carga de archivo CSV](./upload-csv-audience-sourcing.md).

## Requisitos previos {#prerequisites}

Complete todos los elementos de esta sección antes de iniciar el flujo de trabajo de configuración. Los requisitos previos incompletos son el motivo más común por el que la configuración falla o las audiencias no aparecen después del abastecimiento. Antes de seguir esta guía, debes haber completado la [incorporación y configuración de la cuenta](./onboard-account.md).

Algunos pasos de esta sección requieren la acción de un administrador de [!DNL Google Cloud]. Si usted no es el administrador de [!DNL Google Cloud] de su organización, identifique a la persona adecuada antes de comenzar.

### Acceso y permisos de GCS {#gcs-access-permissions}

Antes de continuar, confirme lo siguiente con su administrador de [!DNL Google Cloud]:

* Se han concedido a Adobe los permisos necesarios para autenticarse en el bloque GCS y leer archivos de audiencia. Para obtener instrucciones paso a paso, consulte la [sección de configuración de permisos](#setup-gcs-permissions).
* El abastecimiento de audiencia [!DNL Google Cloud Storage] está disponible en su región. La disponibilidad varía según la región (NA, EMEA, ANZ). Si el abastecimiento de GCS aún no está disponible en su región, póngase en contacto con su representante de cuentas de Adobe para confirmar una cronología.

### Preparación de los datos de audiencia {#prepare-audience-data}

Los archivos de audiencia deben cumplir con la **[Especificación de fuentes de audiencia (v1.2)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)** antes de que comience el abastecimiento. Revise la especificación para la definición de esquema completa y los ejemplos de nivel de campo. Los requisitos clave incluyen:

* **Formato de archivo:** CSV, con comas como delimitadores de campo y barras verticales (`|`) como separadores de varios valores dentro de un solo campo.
* **Campos obligatorios:** Cada registro debe incluir una columna `AUDIENCE_ID` y al menos una columna de clave de coincidencia admitida.
* **Claves de coincidencia admitidas:** `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, `ADFIXUS_ID`.
* **Requisitos de hash:** Todos los valores de clave de coincidencia deben estar recortados, en minúsculas y con hash SHA256 antes de la carga. Collaboration no hash ni normaliza los datos antes de la ingesta.
* **Coherencia de columna:** Si el bloque contiene varios archivos de audiencia, todos los archivos deben utilizar estructuras de columna idénticas.

Todas las claves de coincidencia presentes en los archivos de audiencia también deben habilitarse para la cuenta de Collaboration. Para agregar o habilitar claves de coincidencia, consulte [Configurar claves de coincidencia](./onboard-account.md#set-up-match-keys).

### Valores necesarios antes de comenzar {#required-values}

Tenga preparados los siguientes valores antes de iniciar el asistente de configuración.

| Valor | Descripción |
| --- | --- |
| **[!UICONTROL Cubo]** | Nombre del bloque [!DNL Google Cloud Storage] que contiene los archivos de audiencia. |
| **[!UICONTROL Ruta]** | Prefijo de ruta de acceso dentro del bloque donde se almacenan los archivos de audiencia (por ejemplo, `sourcing/testdata/path1/`). |

## Configurar su conexión de [!DNL Google Cloud Storage] {#configure-gcs-connection}

El flujo de trabajo de configuración es un asistente de varios pasos dentro del área de trabajo **[!UICONTROL Setup]**. Complete cada paso de forma secuencial. Puede volver a cualquier paso con el icono de lápiz de la pantalla de revisión final antes de crear la conexión.

### Añadir una nueva conexión de datos {#add-data-connection}

En la ficha **[!UICONTROL Mis audiencias]** del área de trabajo **[!UICONTROL Configuración]**, seleccione el icono de agregar (![Agregar icono.](/help/assets/icons/plus.png)) y luego seleccione **[!UICONTROL Audiencia]**.

Si esta es su primera audiencia, también puede seleccionar la opción **[!UICONTROL Agregar]**.

![Se muestra la ficha Mis audiencias en el área de trabajo de configuración con el icono Agregar y la opción Agregar audiencia.](../../assets/setup/add-manage-audiences/add-audiences.png)

Aparecerá el flujo de trabajo Añadir audiencia. Seleccione **[!UICONTROL Agregar una nueva conexión de datos]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.

![Espacio de trabajo Agregar audiencias con la opción Agregar una nueva conexión de datos resaltada.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Seleccionar [!DNL Google Cloud Storage] como origen de datos {#select-gcs}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sourcing_specifications_gcs"
>title="Preparar los datos para la incorporación"
>abstract="Lea la guía de especificación de fuentes de audiencias para aprender a dar formato y estructurar los datos de audiencia de Google Cloud Storage para Collaboration."
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-audience-sourcing" text="Consulte la guía de especificación del Abastecimiento de audiencias"

La pantalla de selección de fuentes de datos enumera todos los tipos de conexión disponibles. Seleccione **[!UICONTROL Google Cloud Storage]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.

![Flujo de trabajo Agregar audiencia que muestra la pantalla de selección de fuentes de datos con Google Cloud Storage seleccionado y Siguiente resaltado.](../../assets/setup/gcs-audience-sourcing/gcs-data-source-selection.png)

Aparece un cuadro de diálogo de requisitos previos en el que se describen los pasos de configuración necesarios (por ejemplo, la configuración del contenedor GCS y la asignación de funciones IAM) y se indica que los datos deben cumplir con la **[[!UICONTROL especificación de fuentes de audiencias]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)**. Seleccione **[!UICONTROL Iniciar incorporación]** para confirmar el cumplimiento antes de continuar.

![Los requisitos previos de la lista modal &quot;Prepare your GCS bucket for onboarding&quot; (Prepare your GCS bucket for onboarding), entre los que se incluyen la creación de un bucket GCS, la configuración del acceso IAM para Adobe y el cumplimiento de la Especificación de Abastecimiento de Audiencia, con las opciones Cancelar e &quot;Iniciar la incorporación&quot;.](../../assets/setup/gcs-audience-sourcing/gcs-onboarding-prerequisites-dialog.png)

### Escriba los detalles de conexión de [!DNL Google Cloud Storage] {#authenticate-gcs-connection}

Proporcione los detalles necesarios para permitir que Collaboration acceda a su espacio de [!DNL Google Cloud Storage]. Después de especificar la información requerida, seleccione **[!UICONTROL Siguiente]**.

| Campo | Descripción |
| --- | --- |
| **[!UICONTROL Cubo]** | Nombre de su cubo de [!DNL Google Cloud Storage]. Consulte [Valores necesarios antes de comenzar](#required-values). |
| **[!UICONTROL Ruta]** | El prefijo de ruta dentro del bloque en el que se almacenan los archivos de audiencia. |

![Flujo de trabajo Agregar audiencia que muestra el formulario de autenticación de Google Cloud Storage con campos de nombre de contenedor y ruta de acceso a la carpeta, y el botón Siguiente disponible.](../../assets/setup/gcs-audience-sourcing/gcs-data-connection-authentication.png)

### Confirmar el consentimiento y el reconocimiento de uso de datos {#confirm-consent}

Debe confirmar que las exclusiones de consentimiento se han eliminado de los datos de audiencia para que Collaboration pueda procesarlos. Si no está seguro de si sus datos cumplen con este requisito, revise la guía de [directiva de gobernanza y acciones de aplicación](./onboard-audiences.md#governance-policy-and-enforcement-actions) antes de continuar. Seleccione la casilla de verificación de confirmación y, a continuación, seleccione **[!UICONTROL Aceptar]** para continuar.

### Proporcionar detalles de conexión {#provide-connection-details}

Escriba un nombre y una descripción opcional para esta conexión de datos. El nombre que proporcione aparecerá en la ficha **[!UICONTROL Mis conexiones de datos]** y le ayudará a distinguir esta fuente si administra varias conexiones de datos.

* **[!UICONTROL Nombre de conexión de datos]** (obligatorio)
* **[!UICONTROL Descripción de la conexión de datos]** (opcional).

Haga clic en **[!UICONTROL Siguiente]** para continuar.

![Agregue flujo de trabajo de audiencia en el paso &quot;Proporcionar detalles&quot; que muestra campos para el nombre de la conexión de datos y la descripción de la conexión de datos rellenados con valores de ejemplo, con &quot;Siguiente&quot; visible en la esquina superior derecha.](../../assets/setup/gcs-audience-sourcing/gcs-provide-details.png)

### Revisar los campos de identidad asignados automáticamente {#auto-mapped-fields}

La pantalla **[!UICONTROL Mapping]** es de solo lectura. Collaboration asigna automáticamente los campos de identidad de origen de los archivos de audiencia a los campos de destino en función de los nombres de columna definidos en la Especificación de fuentes de audiencia. No puede agregar, quitar ni aplicar transformaciones a campos asignados en esta fase.

>[!TIP]
>
>Seleccione **[!UICONTROL Vista previa de datos de origen]** para revisar una muestra de sus datos de audiencia en formato tabular y, a continuación, seleccione **[!UICONTROL Cerrar]** para volver a la pantalla de asignación.

![Cuadro de diálogo &quot;Vista previa de datos GCS&quot; que muestra una tabla de datos de audiencia de ejemplo con columnas como AUDIENCE_ID y HASHED_EMAIL_SHA_256, y un botón Cerrar en la esquina inferior derecha.](../../assets/setup/gcs-audience-sourcing/gcs-data-preview.png){zoomable="yes"}

Confirme que las asignaciones mostradas reflejen los campos de los archivos de audiencia. Si no lo hacen, detenga y corrija los archivos para que se ajusten a la [especificación de fuentes de audiencias](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf) antes de continuar. Haga clic en **[!UICONTROL Siguiente]** para continuar.

![Agregue el flujo de trabajo de audiencia en el paso &quot;Asignar campos&quot; que muestra los campos de origen asignados automáticamente (AUDIENCE\_ID y HASHED\_EMAIL\_SHA\_256) a los campos de identidad de destino, con la opción &quot;Previsualizar datos de origen&quot; visible y el botón Siguiente en la esquina superior derecha.](../../assets/setup/gcs-audience-sourcing/gcs-mapping-auto-fields.png)

### Programar actualización de datos {#schedule-data-refresh}

En la vista **[!UICONTROL Programación]**, establezca la frecuencia con la que Collaboration recupera los datos de audiencia actualizados de su bloque GCS y defina el intervalo de fechas activo para el abastecimiento.

Utilice el menú desplegable **[!UICONTROL Frecuencia]** para seleccionar la frecuencia con la que Collaboration recupera los datos de audiencia actualizados de su bloque GCS. Los intervalos disponibles van de **[!UICONTROL Diario]** a **[!UICONTROL Cada 6 días]**.

Escriba un intervalo de fechas en el campo de entrada o seleccione el icono de calendario para establecer las fechas de **[!UICONTROL inicio]** y **[!UICONTROL fin]** para el período de abastecimiento activo. Cuando se llega a la fecha de finalización, el abastecimiento cesa y las audiencias de origen anterior caducan y dejan de estar disponibles para su uso en proyectos de colaboración.

>[!IMPORTANT]
>
>Configure la frecuencia de actualización para que coincida o no supere la velocidad a la que se actualizan los datos de audiencia GCS subyacentes. El intervalo mínimo de actualización admitido es de una vez cada seis días. Refreshing more frequently than your data changes consumes Collaboration credits without producing updated results. To monitor your credit usage, see [Track your credit consumption activity](./my-activity.md).

![Add audience workflow on the &quot;Schedule&quot; step showing the Frequency dropdown set to a recurring interval and a calendar date range selector with start and end dates highlighted. &quot;Next&quot; is visible in the top-right corner.](../../assets/setup/gcs-audience-sourcing/gcs-schedule-settings.png)

Haga clic en **[!UICONTROL Siguiente]** para continuar.

### Review and complete the connection {#review-and-complete}

Review the configuration summary before creating the connection. The summary screen displays the following sections:

* **[!UICONTROL Data connection]**: The GCS bucket credentials and folder path you configured.
* **[!UICONTROL Details]**: The name and optional description of this data connection.
* **[!UICONTROL Mapping]**: The auto-mapped source and target identity fields.
* **[!UICONTROL Schedule]**: The refresh frequency and active date range.

![Add audience workflow on the &quot;Review&quot; step showing a summary of the data connection, details, mapping, and schedule sections with configured values, and the Complete button visible in the top-right corner.](../../assets/setup/gcs-audience-sourcing/gcs-review-summary.png)

Select the pencil icon (![A pencil icon.](../../assets/icons/edit.png)) next to any section to return to that step and make changes. When all sections are correct, select **[!UICONTROL Complete]**.

A confirmation dialog appears, indicating that Collaboration created the data connection and that audience sourcing is in progress.

## Review sourced audiences {#review-sourced-audiences}

After you complete the configuration wizard, Collaboration begins sourcing audiences from your GCS bucket asynchronously. Navigate to **[!UICONTROL Setup]** > **[!UICONTROL My audiences]** to monitor progress. Sourcing does not complete immediately; the time required depends on the size of your data and the configured refresh frequency.

### Monitor audience sourcing progress {#monitor-sourcing-progress}

While Collaboration is retrieving your audience data, a banner at the top of the **[!UICONTROL My audiences]** workspace indicates that sourcing is in progress. Individual audiences appear in the list only after sourcing completes for each audience.

![Setup workspace on the &quot;My audiences&quot; tab showing an &quot;Audience sourcing in progress&quot; banner indicating that audiences are being sourced from a Google Cloud Storage data connection, with the audience list displayed below.](../../assets/setup/gcs-audience-sourcing/gcs-sourcing-in-progress.png)

>[!TIP]
>
>Audience sourcing time varies based on the size of your GCS data and the refresh frequency you configured. Es posible que los conjuntos de datos más grandes o las programaciones de actualización menos frecuentes tarden más en aparecer en el área de trabajo **[!UICONTROL Mis audiencias]**.

### Ver detalles de la audiencia de origen {#view-audience-details}

Una vez finalizado el abastecimiento, las audiencias de [!DNL Google Cloud Storage] aparecerán en la pestaña **[!UICONTROL Mis audiencias]** junto con las audiencias procedentes de otras conexiones. Seleccione un elemento de fila o **[!UICONTROL Ver audiencia]** para abrir la vista de detalles de una audiencia específica.

![La ficha &quot;Mis audiencias&quot; del área de trabajo de configuración muestra una tabla de audiencias, incluida una procedente de Google Cloud Storage, con casillas de verificación y acciones de fila seleccionables disponibles.](../../assets/setup/gcs-audience-sourcing/gcs-audience-list-view.png)

La vista de detalles muestra el estado de la audiencia, el origen y el nombre de la conexión de datos, junto con los siguientes paneles:

* **[!UICONTROL Identidades]**: El recuento total de identidades y el desglose de la audiencia, una vez que los datos estén disponibles.
* **[!UICONTROL Categorías]**: Cualquier etiqueta aplicada para organizar o filtrar la audiencia.
* **[!UICONTROL Acceso a la conexión]**: Indica si la audiencia es privada, pública o compartida con colaboradores específicos.
* **[!UICONTROL Visibilidad de metadatos]**: Qué información de audiencia (como recuento de identidades, porcentaje de superposición e índice) es visible para los colaboradores.

![Vista de detalles de audiencia individual que muestra el estado: Activo, el sistema de origen y el nombre de la conexión de datos en la parte superior, con cuatro paneles a continuación: Identidades que muestran el recuento y el desglose de identidades, Categorías que muestran etiquetas aplicadas, Acceso a la conexión que muestra el tipo de audiencia y la visibilidad, y Visibilidad de metadatos que muestra la configuración del recuento de identidades, el porcentaje de superposición y el índice de audiencia.](../../assets/setup/gcs-audience-sourcing/gcs-audience-details.png)

Revise esta configuración antes de usar la audiencia en un proyecto de colaboración. Para actualizar categorías, acceso a conexiones o visibilidad de metadatos, consulte [Ver y administrar audiencias individuales](./onboard-audiences.md#view-individual-audiences).

### Editar configuración de audiencia {#edit-audience-settings}

Puede editar metadatos de audiencia directamente desde la vista de lista **[!UICONTROL Mis audiencias]** sin abrir la vista de detalles. Seleccione la casilla de verificación de una audiencia para mostrar la barra de herramientas de acciones y, a continuación, seleccione una acción: **[!UICONTROL Editar visibilidad de metadatos]**, **[!UICONTROL Editar acceso a la conexión]**, **[!UICONTROL Editar nombre y descripción]**, **[!UICONTROL Editar categorías]** o **[!UICONTROL Eliminar]**.

![La vista de lista Mis audiencias muestra dos audiencias, una proveniente de Adobe Experience Platform y otra de Google Cloud Storage, con una fila seleccionada mediante una casilla de verificación, que muestra una barra de herramientas inferior con opciones para Editar visibilidad de metadatos, Editar acceso de conexión, Editar nombre y descripción, Editar categorías y Eliminar.](../../assets/setup/gcs-audience-sourcing/gcs-audience-list-view-edit-options.png)

### Vea su conexión de datos GCS {#view-gcs-connection}

Para revisar o administrar la propia conexión, incluidas sus claves de coincidencia y la programación, vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Mis conexiones de datos]**. Su nueva conexión GCS está disponible inmediatamente allí. El origen de la audiencia se muestra como **[!UICONTROL Google Cloud Storage]**.

## Limitaciones conocidas {#known-limitations}

Tenga en cuenta las siguientes restricciones al configurar y utilizar el abastecimiento de audiencia [!DNL Google Cloud Storage]:

* **Restricciones de clave de coincidencia:** Una vez habilitada una clave de coincidencia para una conexión de datos, no se puede quitar. Puede agregar claves de coincidencia a una conexión existente, pero no puede deshabilitarlas ni eliminarlas. Para cambiar las claves de coincidencia activas, debe [eliminar la conexión de datos](./manage-data-connection.md#delete-data-connection) y crear una nueva.
* **One active data connection per source:** Only one active [!DNL Google Cloud Storage] data connection is supported at a time. If you need to source audiences from a different bucket, [delete the existing connection](./manage-data-connection.md#delete-data-connection) and create a new one pointing to the new bucket.
* **Subfolder support:** Audience files must be located directly within the specified folder path. Collaboration does not traverse subfolders within that path.

## Resolución de problemas {#troubleshooting}

Use this section to resolve issues that occur after you establish the initial connection. For errors that occur during authentication, review your credentials and bucket permissions, or contact your administrator.

**Audiences are not appearing or sourcing is taking longer than expected**

* Sourcing time scales with data volume and the configured refresh frequency. Extended processing time is expected for large datasets.
* If audiences have not appeared within 24 hours, confirm that your audience files exist at the folder path you specified during setup and comply with the Audience Sourcing Specification.
* Check the **[!UICONTROL My data connections]** tab for error indicators on the connection.
* If the issue persists after completing these steps, contact Adobe customer support and provide the data connection name and bucket details.

**The data connection shows a failed status after initially succeeding**

* Confirm that the GCS bucket permissions and credentials have not changed since you created the connection. Any change that removes Adobe&#39;s access to the bucket causes subsequent sourcing runs to fail.
* Verify that audience files still exist at the configured folder path and conform to the Audience Sourcing Specification.
* If the issue persists after confirming permissions and file availability, [delete the connection](./manage-data-connection.md#delete-data-connection) and create a new one, or contact Adobe customer support.

**Audience file format errors occur during a scheduled refresh**

* Confirm that updated files in the bucket comply with the column structure and field requirements in the [Audience Sourcing Specification](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf).
* Ensure all files in the configured folder path use identical column structures. Mixed-format files in the same path can cause partial sourcing failures.

## Set up [!DNL Google Cloud Storage] permissions {#setup-gcs-permissions}

[!DNL Google Cloud Storage] provides a secure, scalable way to store and access your data in the cloud. To allow Adobe to read from your GCS buckets, you must configure the appropriate Identity and Access Management (IAM) permissions and service account access in your [!DNL Google Cloud] account.

### Collect Adobe&#39;s [!DNL Google Service Account] information {#collect-account-information}

To get started, note the [!DNL Google Service Account] for Adobe that matches your region. You will need this information to grant Adobe access in later steps.

| Región | [!DNL Google Service Account] |
| ------------- | --------------- |
| América del Norte | `kk9930000@va3-22da.iam.gserviceaccount.com` |
| EMEA | `kze830000@sfc-eufrankfurt-1-g4a.iam.gserviceaccount.com` |
| Australia | `knhv20000@sfc-au-1-nla.iam.gserviceaccount.com` |

{style="table-layout:auto"}

### Set up IAM role {#setup-iam-role}

>[!IMPORTANT]
>
>You must have **Account Admin** privileges in your [!DNL Google Cloud] account to complete this setup. If you do not have these privileges, contact your administrator before proceeding.

Follow the steps below to create a custom IAM role with the necessary permissions and assign it to the Adobe service account. This ensures Adobe has secure access to your GCS audience data.

#### Create IAM role {#create-iam-role}

First, create a custom IAM role in your [!DNL Google Cloud] project with the necessary permissions to assign to Adobe.

In the **[!DNL IAM & Admin]** page of the [[!DNL Google Cloud] Console](https://console.cloud.google.com), navigate to **[!DNL Roles]** and select **[!DNL Create role]**. Fill in the required information such as the title and ID for your new role.

Then add the following permissions to the role:

| Permiso | Objetivo |
| ------------- | --------------- |
| `storage.buckets.get` | Read bucket metadata. |
| `storage.objects.get` | Read object data and metadata. |
| `storage.objects.list` | List objects in a bucket. |

{style="table-layout:auto"}

For more information on permissions, see [GCS IAM permissions](https://cloud.google.com/storage/docs/access-control/iam-permissions). For step-by-step instructions, see [how to create custom roles](https://docs.cloud.google.com/iam/docs/creating-custom-roles).

#### Assign IAM role to Adobe {#assign-role}

Next, open the [**[!DNL Buckets]**&#x200B;page](https://console.cloud.google.com/storage/browser) in the [!DNL Google Cloud Console] and select the bucket that contains your audience data.

Navigate to the **[!DNL Permissions]** tab, choose **[!DNL View by principals]**, and then select **[!DNL Grant access]**.

In the **[!DNL Add principals]** dialog, add the [Adobe Google Service Account](#collect-account-information) as the principal and assign the custom IAM role you created earlier. Select **[!DNL Save]** to confirm the setup.

Adobe now has secure access your audience data in the selected GCS bucket. Review any additional [prerequisites](#prerequisites) as needed, or proceed to [begin sourcing audiences from GCS into Collaboration](#configure-gcs-connection).

#### Collect [!DNL Google Cloud Storage] details {#collect-gcs-details}

Finalmente, reúna los detalles de su cubo GCS como se muestra en la tabla siguiente. Necesitará esta información para configurar la conexión entre su GCS y Collaboration.

| Campo | Descripción | Ejemplo |
|------ |------------ |-------- |
| [!DNL Bucket] | El nombre exacto del bloque [!DNL Google Cloud Storage] que contiene los archivos de audiencia. | `customer-data-bucket` |
| [!DNL Path] | El prefijo de ruta dentro del bloque en el que se almacenan los archivos de audiencia. Debe finalizar con `/` para leer todos los archivos. | `sourcing/testdata/path1/` |

{style="table-layout:auto"}

## Próximos pasos {#next-steps}

Ha configurado [!DNL Google Cloud Storage] como origen de datos en Collaboration. Una vez finalizado el abastecimiento, las audiencias estarán disponibles en el espacio de trabajo de **[!UICONTROL Mis audiencias]** y listas para usarse en proyectos de colaboración.

Desde ahí, puede realizar lo siguiente:

* [Creación y administración de proyectos de colaboración](../collaborate/manage-projects.md)
* [Activación de audiencias dentro de un proyecto](../collaborate/activate.md)
* [Revisión de superposiciones y medición del rendimiento](../collaborate/measure.md)
* [Administrar la configuración y visibilidad de la audiencia](./onboard-audiences.md#view-individual-audiences)
* [Administrar las claves de coincidencia y la programación de esta conexión de datos](./manage-data-connection.md)

Para ver otros métodos de obtención de audiencias, consulte:

* [Configurar  [!DNL Amazon S3] para el abastecimiento de audiencias](./configure-aws-s3-audience-sourcing.md)
* [Configurar  [!DNL Snowflake] para el abastecimiento de audiencias](./configure-snowflake-audience-sourcing.md)
* [Audiencias de Source de Experience Platform](./onboard-audiences.md)
* [Cargar un archivo CSV para el abastecimiento de audiencias](./upload-csv-audience-sourcing.md)
