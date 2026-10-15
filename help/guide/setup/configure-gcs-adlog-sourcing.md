---
title: Configurar [!DNL Google Cloud Storage] para el origen de exposición de publicidad
description: Aprenda a conectar un bloque de [!DNL Google Cloud Storage] como origen de registro de anuncios de autoservicio para exposiciones de publicidad en la medición de Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 02f344c9fcfff20c84c2e92b5aa4647829dd5d2f
workflow-type: tm+mt
source-wordcount: '1712'
ht-degree: 3%
---

# Configurar [!DNL Google Cloud Storage] para el origen de exposición de publicidad

Conecte su bloque de [!DNL Google Cloud Storage] (GCS) a Adobe Real-Time CDP Collaboration para generar datos de registro de anuncios para su medición.

El módulo Medición de Real-Time CDP Collaboration conecta los datos de conversión del anunciante con los registros de exposición de anuncios del publicador para ofrecer informes de campaña centrados en la privacidad. Esto agrega una ruta de autoservicio sin código para anunciantes y editores. Puede incluir los registros de exposición (impresión) de anuncios que ya mantiene en [!DNL Google Cloud Storage] en Medición para atribución, sin dependencia de Adobe Experience Platform. Conecta un bloque, confirma que los datos detectados coinciden con el esquema de registro de anuncios que Medición espera y finalizan en minutos.

Los datos no se extraen en el momento de la conexión. El abastecimiento se activa al ejecutar un informe de medición. Para minimizar el almacenamiento, Adobe elimina automáticamente los registros de anuncios de origen después de un periodo de retención de 7 días.

Las reglas de administración y administración de datos para los registros de anuncios procedentes de [!DNL Google Cloud Storage] coinciden con las reglas que se aplican a los datos procedentes de Adobe Experience Platform.

>[!NOTE]
>
>Esta guía describe cómo obtener los registros de anuncios **del anunciante y el publicador** (exposiciones de publicidad) del almacenamiento en la nube. El abastecimiento de datos de conversión desde el almacenamiento en la nube estará disponible próximamente.

## Requisitos previos {#prerequisites}

Complete todos los elementos de esta sección antes de iniciar el flujo de trabajo de configuración. Antes de seguir esta guía, debes haber completado la [incorporación y configuración de la cuenta](./onboard-account.md).

### Acceso y permisos de GCS {#gcs-access-permissions}

Usted o su administrador de [!DNL Google Cloud] deben conceder a Adobe acceso de solo lectura al bloque GCS antes de iniciar el asistente. Para obtener instrucciones paso a paso, consulte [Configurar permisos de Google Cloud Storage](#setup-gcs-permissions).


### Preparar los datos de registro de anuncios {#prepare-adlog-data}

Los archivos de registro de anuncios deben cumplir con el [esquema de registro de anuncios](#ad-log-schema) antes de que comience el abastecimiento. Los requisitos clave incluyen:

* **Formato de archivo:** CSV solamente.
* **Encabezados de columna canónicos:** Los archivos deben utilizar los encabezados de columna canónicos definidos en el [esquema de registro de anuncios](#ad-log-schema). Esta versión no admite la reasignación por columna ni la asignación de esquema automatizada.
* **Campos obligatorios:** Todos los campos obligatorios deben estar presentes, junto con al menos una clave de coincidencia.
* **Hash de clave de coincidencia:** Los valores de hash de clave de coincidencia deben estar en minúscula hexadecimal SHA-256.
* **Coherencia de columna:** Todos los archivos de la ruta de acceso configurada deben compartir un diseño de columna idéntico.
* **Subcarpetas:** Los archivos deben ubicarse directamente en la ruta de acceso especificada. Collaboration no atraviesa las subcarpetas.

## Conexión de registros de publicidad en el asistente {#connect-adlogs}

Siga estos pasos para conectar los registros de anuncios de GCS desde Collaboration.

1. En el área de trabajo **[!UICONTROL Configuración]**, seleccione **[!UICONTROL Mis datos de medición]**, luego seleccione el icono Agregar y elija **[!UICONTROL Datos de medición]**.

   ![El área de trabajo Configuración en la ficha Mis datos de medición, que muestra el icono Agregar y la opción Datos de medición en el menú.](../../assets/setup/gcs-adlog-sourcing/add-measurement-data-entry-point.png){zoomable="yes"}

2. En el flujo de trabajo **[!UICONTROL Agregar datos de medición]**, seleccione **[!UICONTROL Exposiciones de Advertising]** como tipo de datos de medición y, a continuación, seleccione **[!UICONTROL Siguiente]**.

   ![Flujo de trabajo Agregar datos de medición que muestra la selección del tipo de datos de medición, con Advertising Exposure seleccionado.](../../assets/setup/gcs-adlog-sourcing/select-adlog-data-type.png){zoomable="yes"}

3. Para importar sus datos de medición, seleccione **[!UICONTROL Agregar una nueva conexión de datos]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.

   ![Flujo de trabajo Agregar datos de medición que muestra el paso de selección de la conexión de datos, con Agregar una nueva conexión de datos seleccionada.](../../assets/setup/gcs-adlog-sourcing/add-new-data-connection.png){zoomable="yes"}

4. Elija el origen de datos de la nueva conexión de datos: **[!UICONTROL Google Cloud Storage]**. Seleccione **[!UICONTROL Siguiente]**.

   ![Flujo de trabajo Agregar datos de medición que muestra el paso de selección de fuentes de datos, con las opciones Google Cloud Storage, Azure Blob Storage y Azure Data Lake Storage Gen 2 y Google Cloud Storage seleccionado.](../../assets/setup/gcs-adlog-sourcing/gcs-adlog-source-selection.png){zoomable="yes"}

5. Se abre el asistente **[!UICONTROL Agregar conexión de datos]**. En el paso **[!UICONTROL Conectar Google Cloud Storage]**, proporcione **[!UICONTROL Bucket]** y **[!UICONTROL Path]** donde se encuentran los archivos de registro de anuncios. Ambos campos son obligatorios y todos los archivos de la ruta configurada se tratan como un conjunto de datos.

   ![El asistente para agregar conexión de datos en el paso Conectar Google Cloud Storage, que muestra los campos de cubo y ruta de acceso necesarios.](../../assets/setup/gcs-adlog-sourcing/gcs-adlog-connection-details.png){zoomable="yes"}

6. En el paso **[!UICONTROL Nombre y descripción]**, proporcione un **[!UICONTROL nombre de conexión de datos]** necesario y una **[!UICONTROL Descripción]** opcional para la conexión de datos.

   ![Paso Nombre y descripción que muestra los campos Nombre de conexión de datos y Descripción.](../../assets/setup/gcs-adlog-sourcing/gcs-adlog-name-description.png){zoomable="yes"}

7. En el paso **[!UICONTROL Asignar campos]**, obtenga una vista previa de las columnas detectadas para confirmar que el asistente lee los archivos correctos y, a continuación, revise el [esquema de registro de anuncios](#ad-log-schema), que enumera todos los campos que Measurement comprende, qué campos son obligatorios frente a los opcionales y qué columnas detectadas se reconocen como claves de identidad o coincidencia. Este paso es de validación de solo lectura: el sistema confirma que los encabezados requeridos están presentes y le bloquea si falta un campo requerido. En esta versión no hay ninguna reasignación por columna.

   ![El paso Asignar campos muestra la vista previa de las columnas detectadas y la revisión del esquema del registro de anuncios.](../../assets/setup/gcs-adlog-sourcing/gcs-adlog-map-fields.png){zoomable="yes"}

8. En el paso **[!UICONTROL Revisar]**, revise y finalice. La conexión aparece en el área de datos de medición con su estado, que permanece **pendiente** hasta que el primer informe de medición ejecute los datos de origen.

## Funcionamiento del abastecimiento de registros de publicidad {#how-it-works}

El abastecimiento de registro de anuncios de [!DNL Google Cloud Storage] refleja el flujo de alto nivel que se usa para el abastecimiento de audiencias:

1. **Conexión de almacenamiento en la nube:** configura el acceso de solo lectura a un espacio que contiene sus registros de anuncios.
2. **Revisión y validación de esquemas:** el sistema valida los archivos con el esquema de registro de anuncios (comprobaciones de carpetas, archivos y encabezados requeridos; sólo lectura).
3. **Asignación de campos:** los campos de identidad de origen se asignan automáticamente a campos canónicos en función de los nombres de columna canónicos. No hay reasignación manual.
4. **Ingesta y normalización:** eventos se normalizan a una fila por exposición. El abastecimiento de registros de anuncios se inicia al ejecutar un informe de medición.

### Esquema de registro de anuncios (formato CSV canónico) {#ad-log-schema}

Los campos obligatorios deben estar presentes y al menos un campo marcado como **Unir clave (obligatorio)** en la siguiente tabla también debe estar presente. Los valores hash de clave de coincidencia son valores hexadecimales SHA-256 en minúsculas.

| Campo | Tipo de datos | Requerido | Descripción |
| --- | --- | --- | --- |
| `EVENT_DATETIME` | Cadena (ISO 8601) | Requerido | Marca de tiempo del evento |
| `EVENT_ID` | Cadena | Opcional | ID único del evento |
| `EVENT_TYPE` | Cadena (enumeración) | Requerido | Tipo de evento. Uno de `{impression, click}` |
| `HASHED_EMAIL_SHA_256` | Cadena (hexadecimal de 64 caracteres) | Clave de unión (una de ellas obligatoria) | SHA-256 hexadecimal en minúsculas del correo electrónico |
| `HASHED_IPV4_SHA_256` | Cadena (hexadecimal de 64 caracteres) | Clave de unión (una de ellas obligatoria) | SHA-256 hexadecimal en minúsculas de IPv4 |
| `DEVICE_ID` | Cadena (hexadecimal de 64 caracteres) | Clave de unión (una de ellas obligatoria) | ID de publicidad del dispositivo |
| `DEVICE_ID_TYPE` | Cadena (enumeración) | Opcional | Uno de `{idfa, gaid, aaid, rida, afai, msai, vida, lgudid, tifa}` |
| `ECID` | Cadena (hexadecimal de 64 caracteres) | Clave de unión (una de ellas obligatoria) | ECID basado en Demdex |
| `CUSTOM_ID` | Cadena | Opcional | ID persistente de publicador/socio (por ejemplo, PPID, RampID, Core ID) |
| `ADVERTISER_ID` | Cadena | Requerido | Identificador único del anunciante |
| `ADVERTISER_NAME` | Cadena | Opcional | Nombre del anunciante/marca |
| `CAMPAIGN_ID` | Cadena | Requerido | Identificador de campaña específico de la plataforma |
| `CAMPAIGN_NAME` | Cadena | Opcional | Nombre de campaña legible en lenguaje natural |
| `PLACEMENT_ID` | Cadena | Requerido | Identificador único de la ubicación |
| `PLACEMENT_NAME` | Cadena | Opcional | Nombre de ubicación descriptivo |
| `CREATIVE_ID` | Cadena | Opcional | Identificador único del creador de la publicidad |
| `CREATIVE_NAME` | Cadena | Opcional | Nombre creativo legible por un ser humano |
| `AUDIENCE_ID` | Cadena | Opcional | Identificador del segmento de audiencia |
| `AUDIENCE_NAME` | Cadena | Opcional | Nombre de audiencia legible en lenguaje natural |
| `DEVICE_TYPE` | Cadena (enumeración) | Opcional | Uno de `{mobile, desktop, tablet, ctv, dooh, car, in_store, other}` |
| `AD_FORMAT` | Cadena (enumeración) | Opcional | Uno de `{display, video, native, audio, search, commerce, dooh, other}` |
| `SITE_NAME` | Cadena | Opcional | Propiedad de red/sitio/aplicación/editor en la que se produjo la impresión |
| `TEST_GROUP` | Cadena | Opcional | Agrupación para estudios de elevación, ensayos/control, grupos de exclusión |
| `CUSTOM_DIM` | Cadena | Opcional | Dimensión de editor adicional |

{style="table-layout:auto"}

>[!NOTE]
>
>`MATCH_KEY_TYPE` se incluye como un campo opcional en el esquema para que, con el tiempo, se puedan admitir varios tipos de ID en paralelo y la procedencia de clave de coincidencia (correo electrónico, teléfono o CRM) se pueda conservar sin romper el contrato de la versión 1.

### Requisitos de validación (v1) {#validation-requirements}

El sistema valida y registra los datos de origen antes de completar el flujo de trabajo de configuración. Comprobaciones de validación:

* La carpeta de origen debe contener al menos un archivo.
* Los archivos no pueden estar vacíos.
* Deben estar presentes los encabezados de esquema requeridos.
* Se pueden omitir los campos de esquema opcionales.
* Los archivos que solo contienen los campos obligatorios son válidos.

Los errores de validación impiden continuar. El sistema **no** valida tipos de datos, valores de campo, integridad de registros, calidad de datos o asignación de esquema automatizada. La validación se limita a las comprobaciones de carpetas, archivos y encabezados requeridos para esta versión inicial.

## Limitaciones conocidas {#known-limitations}

Tenga en cuenta las siguientes restricciones al configurar y utilizar el abastecimiento de registro de anuncios de [!DNL Google Cloud Storage]:

* **Solo registros de anuncios:** Esta conexión genera registros de anuncios de anunciante o editor (exposiciones de publicidad). Los datos de conversión aún no son compatibles.
* **Fuentes compatibles:** [!DNL Google Cloud Storage] y [!DNL Azure Data Lake Storage] o [!DNL Azure Blob Storage].
* **Formato de archivo:** CSV solamente.
* **Se requieren encabezados canónicos:** No hay reasignación por columna ni asignación inteligente/automatizada en esta versión. Los archivos deben utilizar los nombres de columna canónicos.
* **Sin validación de valor/tipo:** Solo se validan los encabezados de columna requeridos. Inicialmente, es posible que no haya filas de datos.
* **No se puede editar una conexión después de la creación:** Cualquier cambio, incluido el cambio de las claves de coincidencia activas, requiere la creación de una nueva conexión.
* **Un diseño por ruta:** Todos los archivos de la ruta deben compartir un diseño de columna idéntico. Los diseños mixtos pueden provocar errores de abastecimiento parciales.
* **No se han atravesado las subcarpetas:** Los archivos deben sentarse directamente en la ruta de acceso especificada.
* **No hay programación ni retrospectiva en la configuración:** El abastecimiento de registros de anuncios se inicia al ejecutar un informe de medición. Establezca el período retroactivo al configurar el informe.
* **Una conexión de datos de registro de anuncios:** Configure solamente una conexión de datos de registro de anuncios a la vez. Los informes de medición utilizan automáticamente la conexión configurada.

## Resolución de problemas {#troubleshooting}

* **La conexión muestra datos pendientes/no hay datos:** Esto se espera hasta que se ejecute el primer informe de medición. No se obtienen datos en el momento de la conexión.
* **&quot;No se encontraron datos&quot; en el paso de origen:** La carpeta está vacía. Agregue archivos antes de continuar.
* **La vista previa no muestra columnas:** El archivo está presente pero vacío (sin encabezados ni contenido).
* **No se puede obtener la validación posterior:** Falta un encabezado de columna requerido. Confirme que los campos obligatorios y al menos una clave de coincidencia están presentes, utilizando nombres canónicos.
* **Columnas no reconocidas:** Los nombres de columnas no canónicas no se recogen como campos conocidos. Cámbieles el nombre al formato canónico; no hay reasignación en esta versión.
* **Se produce un error en el abastecimiento después de la instalación:** Confirme que el acceso de lectura de Adobe al contenedor no ha cambiado y que los archivos siguen existiendo en la ruta de acceso configurada en formato canónico.
* **El intervalo de fechas del informe no está completamente cubierto:** Recuerde la caducidad automática de datos de 7 días. Es posible que los registros con más de 7 días no estén disponibles para el intervalo solicitado.

## Configurar permisos de [!DNL Google Cloud Storage] {#setup-gcs-permissions}

Para permitir que Adobe lea desde el contenedor GCS, cree una función IAM personalizada con los siguientes permisos:

| Permiso | Objetivo |
| ------------- | --------------- |
| `storage.buckets.get` | Leer metadatos de bloque. |
| `storage.objects.get` | Leer datos y metadatos de objetos. |
| `storage.objects.list` | Enumerar objetos en un bloque. |

{style="table-layout:auto"}

Otorgue esta función personalizada a la cuenta de servicio de Adobe Google de su región (NA, EMEA o Australia). Completar esta configuración requiere privilegios de **administrador de cuenta de Google Cloud**.

## Consideraciones sobre la actualización o migración {#upgrade-migration}

* Los clientes incorporados anteriormente mediante Experience Platform o la configuración asistida por Adobe pueden pasar a la ruta de almacenamiento en la nube de autoservicio. Los informes de medición y flujos existentes no cambiarán.
* Las claves de coincidencia presentes en los archivos de registro de publicidad deben habilitarse para la cuenta de Collaboration, al igual que con el abastecimiento de audiencias.
* Las reglas de gobernanza y gestión de datos coinciden con los datos procedentes de Experience Platform.

## Próximos pasos {#next-steps}

Una vez finalizado el abastecimiento, los registros de anuncios están disponibles para los informes de medición.

Para ver otros métodos de obtención de exposición a la publicidad, consulte [Configuración del almacenamiento de Azure para la obtención de exposición a la publicidad](./configure-azure-adlog-sourcing.md).
