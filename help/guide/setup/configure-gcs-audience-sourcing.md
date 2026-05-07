---
title: Configurar  [!DNL Google Cloud Storage] para el Abastecimiento de audiencias
description: Aprenda a conectar un contenedor  [!DNL Google Cloud Storage] como fuente de audiencia de autoservicio en Real-Time CDP Collaboration, incluidos los requisitos previos, la autenticación, la asignación de campos, la programación y la validación.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: cb901016a35867be647f165c953f5753eec6dfa5
workflow-type: tm+mt
source-wordcount: '2898'
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

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sourcing_gcs"
>title="Añadir audiencia de Google Cloud Storage"
>abstract="Para conectar su almacenamiento de Google Cloud, autorice al usuario del servicio de Adobe a recuperar sus datos de audiencia para procesarlos. Siga los pasos descritos en Experience League para conceder acceso a Adobe a su almacenamiento en la nube de Google."

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
>Configure la frecuencia de actualización para que coincida o no supere la velocidad a la que se actualizan los datos de audiencia GCS subyacentes. El intervalo mínimo de actualización admitido es de una vez cada seis días. La actualización con más frecuencia que los cambios de datos consume créditos de Collaboration sin producir resultados actualizados. Para supervisar tu uso de crédito, consulta [Rastrear tu actividad de consumo de crédito](./my-activity.md).

![Agregue el flujo de trabajo de audiencia en el paso &quot;Programar&quot;, que muestra la lista desplegable Frecuencia establecida en un intervalo recurrente y un selector de intervalo de fechas de calendario con las fechas de inicio y finalización resaltadas. &quot;Siguiente&quot; está visible en la esquina superior derecha.](../../assets/setup/gcs-audience-sourcing/gcs-schedule-settings.png)

Haga clic en **[!UICONTROL Siguiente]** para continuar.

### Revisión y finalización de la conexión {#review-and-complete}

Revise el resumen de la configuración antes de crear la conexión. La pantalla de resumen muestra las siguientes secciones:

* **[!UICONTROL Conexión de datos]**: las credenciales del contenedor GCS y la ruta de la carpeta que configuró.
* **[!UICONTROL Detalles]**: nombre y descripción opcional de esta conexión de datos.
* **[!UICONTROL Asignación]**: los campos de origen y destino asignados automáticamente.
* **[!UICONTROL Programación]**: La frecuencia de actualización y el intervalo de fechas activo.

![Agregue flujo de trabajo de audiencia en el paso &quot;Revisar&quot;, que muestra un resumen de las secciones de conexión de datos, detalles, asignación y programación con valores configurados, y el botón Completar visible en la esquina superior derecha.](../../assets/setup/gcs-audience-sourcing/gcs-review-summary.png)

Seleccione el icono de lápiz (![Un icono de lápiz.](../../assets/icons/edit.png)) al lado de cualquier sección para volver a ese paso y realizar cambios. Cuando todas las secciones sean correctas, seleccione **[!UICONTROL Completar]**.

Aparece un cuadro de diálogo de confirmación que indica que Collaboration ha creado la conexión de datos y que el abastecimiento de audiencias está en curso.

## Revisar audiencias de origen {#review-sourced-audiences}

Después de completar el asistente de configuración, Collaboration empieza a obtener audiencias del bloque GCS de forma asíncrona. Vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Mis audiencias]** para supervisar el progreso. El abastecimiento no se completa inmediatamente; el tiempo necesario depende del tamaño de los datos y de la frecuencia de actualización configurada.

### Monitorización del progreso de abastecimiento de audiencia {#monitor-sourcing-progress}

Mientras Collaboration recupera sus datos de audiencia, un banner en la parte superior de **[!UICONTROL Mis audiencias]** espacio de trabajo indica que el abastecimiento está en curso. Las audiencias individuales aparecen en la lista solo después de que el abastecimiento se complete para cada audiencia.

![Configure el área de trabajo en la ficha &quot;Mis audiencias&quot; que muestra un titular &quot;Fuente de audiencias en curso&quot; que indica que las audiencias provienen de una conexión de datos de Google Cloud Storage y que la lista de audiencias se muestra a continuación.](../../assets/setup/gcs-audience-sourcing/gcs-sourcing-in-progress.png)

>[!TIP]
>
>El tiempo de obtención de la audiencia varía en función del tamaño de los datos GCS y la frecuencia de actualización configurada. Es posible que los conjuntos de datos más grandes o las programaciones de actualización menos frecuentes tarden más en aparecer en el área de trabajo **[!UICONTROL Mis audiencias]**.

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
* **Una conexión de datos activa por origen:** Solo se admite una conexión de datos activa de [!DNL Google Cloud Storage] a la vez. Si necesita crear audiencias a partir de un bloque diferente, [elimine la conexión existente](./manage-data-connection.md#delete-data-connection) y cree una nueva que apunte al nuevo bloque.
* **Compatibilidad con subcarpetas:** Los archivos de audiencia deben encontrarse directamente en la ruta de acceso de la carpeta especificada. Collaboration no atraviesa subcarpetas dentro de esa ruta.

## Resolución de problemas {#troubleshooting}

Utilice esta sección para resolver los problemas que se producen después de establecer la conexión inicial. Para ver los errores que se producen durante la autenticación, revise las credenciales y los permisos del bloque o póngase en contacto con el administrador.

**Las audiencias no aparecen o el abastecimiento está tardando más de lo esperado**

* El tiempo de abastecimiento se amplía con el volumen de datos y la frecuencia de actualización configurada. Se espera un tiempo de procesamiento prolongado para los conjuntos de datos grandes.
* Si las audiencias no han aparecido en un plazo de 24 horas, confirme que los archivos de audiencia existen en la ruta de carpeta especificada durante la configuración y cumplan con la Especificación del Abastecimiento de audiencias.
* Compruebe la pestaña **[!UICONTROL Mis conexiones de datos]** para ver los indicadores de error en la conexión.
* Si el problema persiste después de completar estos pasos, póngase en contacto con el servicio de atención al cliente de Adobe y proporcione el nombre de la conexión de datos y los detalles del bloque.

**La conexión de datos muestra un estado de error después de haberse realizado correctamente inicialmente**

* Confirme que los permisos y credenciales del contenedor GCS no han cambiado desde que creó la conexión. Cualquier cambio que elimine el acceso de Adobe al bloque provoca que las ejecuciones de abastecimiento posteriores fallen.
* Compruebe que los archivos de audiencia siguen existiendo en la ruta de carpeta configurada y que se ajustan a la Especificación del Abastecimiento de audiencias.
* Si el problema continúa después de confirmar los permisos y la disponibilidad del archivo, [elimine la conexión](./manage-data-connection.md#delete-data-connection) y cree una nueva, o póngase en contacto con el servicio de atención al cliente de Adobe.

**Se producen errores de formato de archivo de audiencia durante una actualización programada**

* Confirme que los archivos actualizados en el bloque cumplen con los requisitos de campo y estructura de columna de la [especificación de fuentes de audiencia](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf).
* Asegúrese de que todos los archivos de la ruta de carpeta configurada utilicen estructuras de columna idénticas. Los archivos de formato mixto en la misma ruta pueden provocar errores de abastecimiento parciales.

## Configurar permisos de [!DNL Google Cloud Storage] {#setup-gcs-permissions}

[!DNL Google Cloud Storage] ofrece una forma segura y escalable de almacenar datos y obtener acceso a ellos en la nube. Para permitir que Adobe lea desde los bloques de GCS, debe configurar los permisos de Identity and Access Management (IAM) y el acceso a la cuenta de servicio adecuados en su cuenta de [!DNL Google Cloud].

### Recopilar información de [!DNL Google Service Account] de Adobe {#collect-account-information}

Para empezar, observe el [!DNL Google Service Account] para Adobe que coincide con su región. Necesitará esta información para conceder acceso a Adobe en pasos posteriores.

| Región | [!DNL Google Service Account] |
| ------------- | --------------- |
| América del Norte | `kk9930000@va3-22da.iam.gserviceaccount.com` |
| EMEA | `kze830000@sfc-eufrankfurt-1-g4a.iam.gserviceaccount.com` |
| Australia | `knhv20000@sfc-au-1-nla.iam.gserviceaccount.com` |

{style="table-layout:auto"}

### Configuración del rol de IAM {#setup-iam-role}

>[!IMPORTANT]
>
>Debe tener privilegios de **Administrador de cuenta** en su cuenta de [!DNL Google Cloud] para completar esta configuración. Si no tiene estos privilegios, póngase en contacto con el administrador antes de continuar.

Siga los pasos a continuación para crear una función IAM personalizada con los permisos necesarios y asignarla a la cuenta de servicio de Adobe. Esto garantiza que Adobe tenga acceso seguro a los datos de audiencia de GCS.

#### Crear función de IAM {#create-iam-role}

En primer lugar, cree una función IAM personalizada en el proyecto [!DNL Google Cloud] con los permisos necesarios para asignarla a Adobe.

En la página **[!DNL IAM & Admin]** de la [[!DNL Google Cloud] consola](https://console.cloud.google.com), vaya a **[!DNL Roles]** y seleccione **[!DNL Create role]**. Rellene la información necesaria, como el título y el ID de la nueva función.

A continuación, agregue los siguientes permisos a la función:

| Permiso | Objetivo |
| ------------- | --------------- |
| `storage.buckets.get` | Leer metadatos de bloque. |
| `storage.objects.get` | Leer datos y metadatos de objetos. |
| `storage.objects.list` | Enumerar objetos en un bloque. |

{style="table-layout:auto"}

Para obtener más información sobre los permisos, consulte [Permisos de GCS IAM](https://cloud.google.com/storage/docs/access-control/iam-permissions). Para obtener instrucciones paso a paso, vea [cómo crear funciones personalizadas](https://docs.cloud.google.com/iam/docs/creating-custom-roles).

#### Asignar la función IAM a Adobe {#assign-role}

A continuación, abra la página [**[!DNL Buckets]**](https://console.cloud.google.com/storage/browser) en [!DNL Google Cloud Console] y seleccione el contenedor que contiene los datos de audiencia.

Vaya a la ficha **[!DNL Permissions]**, elija **[!DNL View by principals]** y, a continuación, seleccione **[!DNL Grant access]**.

En el cuadro de diálogo **[!DNL Add principals]**, agregue la [cuenta del servicio Adobe Google](#collect-account-information) como principal y asigne el rol IAM personalizado que creó anteriormente. Seleccione **[!DNL Save]** para confirmar la instalación.

Adobe ahora tiene acceso seguro a sus datos de audiencia en el bloque GCS seleccionado. Revise [requisitos previos](#prerequisites) adicionales según sea necesario o proceda a [comenzar a obtener audiencias de GCS en Collaboration](#configure-gcs-connection).

#### Recopilar detalles de [!DNL Google Cloud Storage] {#collect-gcs-details}

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
