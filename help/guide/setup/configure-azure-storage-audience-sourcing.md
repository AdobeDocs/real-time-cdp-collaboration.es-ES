---
title: Audiencias de Source del almacenamiento  [!DNL Azure] en Real-Time CDP Collaboration
description: Datos de audiencia de origen de Source del almacenamiento de Azure Blob o del almacenamiento de Azure Data Lake Gen2 en Real-Time CDP Collaboration.
keywords: Real-Time CDP Collaboration; abastecimiento de audiencia; [!DNL Azure Blob Storage]; [!DNL Azure Data Lake Storage] Gen2
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 3b62837cecf6cf7c288ce1633d43312ff6a92664
workflow-type: tm+mt
source-wordcount: '2050'
ht-degree: 3%

---

# Audiencias de Source desde el almacenamiento de Azure

Conecte [!DNL Azure Blob Storage] o [!DNL Azure Data Lake Storage] (ADLS) Gen2 a Adobe Real-Time CDP Collaboration para obtener datos de audiencia de origen para la activación y el análisis de superposición.

Use esta guía para crear una conexión de datos [!DNL Azure] reutilizable y ejecutar una importación única desde la ubicación de almacenamiento configurada. Antes de empezar, confirme que los archivos de audiencia cumplen con la [especificación de fuentes de audiencias](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1_3.pdf). Concederá acceso de lectura a Adobe a su almacenamiento de Azure durante el proceso de configuración.

## Elija su tipo de origen [!DNL Azure] {#choose-source-type}

Collaboration admite dos opciones de ingesta de [!DNL Azure]. Utilice la tabla siguiente para elegir la ruta de la guía que coincida con la ubicación de los archivos de audiencia.

| | **[!DNL Azure Blob Storage]** | **[!DNL Azure Data Lake Storage]Gen2** |
|---|---|---|
| **Usar cuando** | Los archivos están en un **contenedor** de blob estándar en una cuenta de almacenamiento (no se requiere un área de nombres jerárquica). | Los archivos están en un **sistema de archivos** en una cuenta de almacenamiento con **área de nombres jerárquica habilitada (ADLS Gen2)**. |
| **Opción Source en Collaboration** | **[!DNL Azure Blob Storage]** | **[!DNL Azure Data Lake Storage]Gen2** |
| **Campos obligatorios en Collaboration** | Cuenta de almacenamiento, **[!UICONTROL Contenedor]**, **[!UICONTROL Ruta]** | Cuenta de almacenamiento, **[!UICONTROL Contenedor]** (sistema de archivos ADLS Gen2), **[!UICONTROL Ruta]** |
| **Sección de permisos** | [[!DNL Azure Blob] permisos](#set-up-azure-blob-storage-permissions) | [[!DNL Azure Data Lake Storage] Permisos Gen2](#set-up-adls-gen2-permissions) |

Solo puede configurar **un tipo de origen por conexión de datos**. Para crear el origen de [!DNL Blob] y ADLS, cree conexiones de datos independientes.

## Requisitos previos {#prerequisites}

Antes de seguir esta guía, complete la [incorporación y configuración de la cuenta](./onboard-account.md). A continuación, complete los requisitos previos en esta sección antes de iniciar el flujo de trabajo de configuración.

Algunos pasos requieren la acción de un administrador de **[!DNL Azure]**. Si usted no es el administrador de [!DNL Azure] de su organización, identifique a la persona adecuada antes de comenzar.

### Acceso y permisos de [!DNL Azure] {#azure-access-and-permissions}

Antes de configurar la conexión en Collaboration, usted o el administrador de [!DNL Azure] deben otorgar acceso de lectura a Adobe al contenedor de almacenamiento o al sistema de archivos ADLS Gen2 que contiene los archivos de audiencia. Una vez completada la configuración de permisos, el flujo de trabajo de configuración de Collaboration valida el acceso durante el paso **[!UICONTROL Consentimiento]**.

### Preparación de los datos de audiencia {#prepare-audience-data}

Los archivos de audiencia deben cumplir con la **[Especificación de fuentes de audiencia (v1.2)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1_3.pdf)** antes de que comience el abastecimiento.

Los requisitos clave incluyen:

* **Formato de archivo:** CSV, con comas como delimitadores de campo y barras verticales (`|`) como separadores de varios valores dentro de un solo campo.
* **Campos obligatorios:** Cada registro debe incluir una columna `AUDIENCE_ID` y al menos una columna de clave de coincidencia admitida.
* **Claves de coincidencia admitidas:** `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, `ADFIXUS_ID`.
* **Requisitos de hash:** Todos los valores de clave de coincidencia deben estar recortados, en minúsculas y con hash SHA256 antes de la carga. Collaboration no hash ni normaliza los datos antes de la ingesta.
* **Coherencia de columna:** Todos los archivos de la ruta de acceso configurada deben utilizar estructuras de columna idénticas.

Todas las claves de coincidencia presentes en los archivos de audiencia también deben habilitarse para la cuenta de Collaboration. Consulte [Configurar claves de coincidencia](https://experienceleague.adobe.com/es/docs/real-time-cdp-collaboration/using/setup/onboard-account#set-up-match-keys) para obtener instrucciones.

>[!IMPORTANT]
>
> Las claves de coincidencia habilitadas para una conexión de datos no se pueden quitar una vez creada la conexión. Para cambiar el conjunto activo de claves de coincidencia, debe eliminar la conexión y crear una nueva. Confirme la configuración completa de la clave de coincidencia antes de iniciar el flujo de trabajo de configuración.

### Valores necesarios antes de comenzar {#values-required}

Tenga preparados los siguientes valores antes de iniciar el flujo de trabajo de configuración.

| Valor | Descripción | Ejemplo de almacenamiento de Azure Blob | Ejemplo de ADLS Gen2 |
| ------------------- | ------------------------ | -------------------------------------- | -------------------------------------- |
| **Cuenta de almacenamiento** | Nombre de la cuenta de almacenamiento de [!DNL Azure] que hospeda los archivos de audiencia. | `customerdatastore` | `datalake-prod` |
| **Contenedor** | Para [!DNL Azure Blob Storage], el contenedor de almacenamiento que contiene los archivos de audiencia. Para [!DNL Azure Data Lake Storage] Gen2, ingrese el nombre del sistema de archivos ADLS Gen2 en el campo **[!UICONTROL Contenedor]**. | `audience-ingest` | `audiences` |
| **Ruta** | Ruta de la carpeta dentro del contenedor o sistema de archivos que contiene los archivos de audiencia que se van a introducir. Collaboration solo ingiere archivos directamente en la ruta configurada y no ingiere archivos de subcarpetas anidadas. | `sourcing/audiences/path1/` | `sourcing/inbound/` |
| **Id. de inquilino** | El id. de inquilino de Microsoft Entra asociado con su cuenta de almacenamiento [!DNL Azure]. | `00000000-0000-0000-0000-000000000000` | `00000000-0000-0000-0000-000000000000` |

## Configurar permisos de [!DNL Azure] {#set-up-azure-permissions}

Complete los pasos de esta sección para preparar su entorno de [!DNL Azure]. Adobe requiere acceso de lectura al contenedor de almacenamiento para que el flujo de trabajo de configuración de Collaboration pueda establecer una conexión. Este trabajo se realiza en el portal [!DNL Azure] y es posible que el administrador [!DNL Azure] deba completarlo.

Después de completar esta sección, procede a [Configurar tu [!DNL Azure] conexión](#configure-your-azure-connection).

### Obtener el identificador principal de servicio [!DNL Azure] de Adobe {#obtain-principal-identifier}

Antes de completar los pasos de asignación de funciones que se indican a continuación, póngase en contacto con el equipo de su cuenta de Adobe para obtener el identificador principal de servicio [!DNL Azure] para su región (Norteamérica, EMEA o Australia y Nueva Zelanda). Utilizará este identificador para otorgar acceso de lectura a Adobe a su almacenamiento.

### Configurar permisos de [!DNL Azure Blob Storage] {#set-up-azure-blob-storage-permissions}

>[!IMPORTANT]
>
> Necesita permiso para asignar funciones en la cuenta o el contenedor de almacenamiento (por ejemplo, **Propietario** o **Administrador de acceso de usuario** o equivalente).

1. En el [[!DNL Azure] portal](https://portal.azure.com/), abra la cuenta de almacenamiento, vaya a **[!UICONTROL Contenedores]** y seleccione el contenedor que contiene los archivos de audiencia.
2. Seleccione **[!DNL Access control (IAM)]** y luego seleccione **[!DNL Add role assignment]**.
3. Asigne el rol **[!DNL Storage Blob Data Reader]** al principal de Adobe en el ámbito del contenedor.
4. Seleccione **Guardar**.

### Configuración de permisos de ADLS Gen2 {#set-up-adls-gen2-permissions}

Para conexiones ADLS Gen2, el campo **[!UICONTROL Container]** en Collaboration corresponde al sistema de archivos ADLS Gen2 en [!DNL Azure]. Utilice el sistema de archivos que contiene los archivos de audiencia.

Antes de asignar permisos, confirme que la cuenta de almacenamiento tiene **área de nombres jerárquica habilitada** y que las reglas de firewall o de extremo privado permiten el acceso a Adobe.

1. En el [[!DNL Azure] portal](https://portal.azure.com/), abra la cuenta de almacenamiento que contiene su sistema de archivos ADLS Gen2.
2. Abra el sistema de archivos que contiene los archivos de audiencia.
3. Seleccione **[!UICONTROL Control de acceso (IAM)]** y, a continuación, seleccione **[!UICONTROL Agregar asignación de rol]**.
4. Asigne el rol **[!DNL Storage Blob Data Reader]** al principal de Adobe en el ámbito del sistema de archivos o directorio.
5. Seleccione **[!UICONTROL Guardar]**.

Después de completar la configuración de permisos para tu tipo de origen, continúa con [Configurar tu [!DNL Azure] conexión](#configure-your-azure-connection).

## Configurar su conexión de [!DNL Azure] {#configure-your-azure-connection}

Use el flujo de trabajo de configuración de Collaboration para validar los detalles de almacenamiento de [!DNL Azure], confirmar el acceso a Adobe, revisar los campos de identidad asignados automáticamente y crear la conexión de datos.

### Añadir una nueva conexión de datos {#add-new-data-connection}

Vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Mis audiencias]** y, a continuación, seleccione el icono Agregar (![El icono Agregar.](/help/assets/icons/plus.png)) y elija **[!UICONTROL Audiencia]**.

![La vista Mis audiencias que muestra la opción Agregar audiencia utilizada para crear una nueva audiencia o conexión de datos.](../../assets/setup/azure-sourcing/my-audiences-add-audience-entry-point.png){zoomable="yes"}

Aparece el flujo de trabajo **[!UICONTROL Agregar audiencia]**. Seleccione **[!UICONTROL Agregar una nueva conexión de datos]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.

![La vista Mis audiencias que muestra la opción Agregar nueva conexión de datos seleccionada y Siguiente resaltada.](../../assets/setup/azure-sourcing/add-new-data-connection.png){zoomable="yes"}

### Seleccione su origen de datos [!DNL Azure] {#select-azure-data-source}

Seleccione **[!UICONTROL Azure Blob Storage]** o **[!UICONTROL Azure Data Lake Storage Gen2]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.

![El flujo de trabajo Agregar audiencia muestra [!DNL Azure Blob Storage] seleccionado como tipo de conexión de datos y los pasos de incorporación Credenciales, Consentimiento, Asignación de campos y Revisión.](../../assets/setup/azure-sourcing/azure-source-selection-step.png){zoomable="yes"}

Continúe con los pasos restantes para validar la conexión de Azure, confirmar el acceso de Adobe, revisar las asignaciones de campos y crear la conexión de datos.

### Introducir credenciales de conexión {#enter-connection-credentials}

En el paso **[!UICONTROL Credenciales]**, proporcione la información necesaria para tener acceso a la ubicación de almacenamiento [!DNL Azure].

| Campo | Descripción |
|---|---|
| **[!UICONTROL Cuenta de almacenamiento]** | La cuenta de almacenamiento de [!DNL Azure] que contiene los archivos de audiencia. |
| **[!UICONTROL Contenedor]** | El contenedor de almacenamiento o el sistema de archivos ADLS Gen2 que contiene los archivos de audiencia. |
| **[!UICONTROL Ruta]** | Ruta de la carpeta dentro del contenedor en el que se almacenan los archivos de audiencia. |
| **[!UICONTROL Id. de inquilino]** | El identificador de inquilino [!DNL Azure] asociado con su cuenta de almacenamiento. |

Después de especificar los valores requeridos, selecciona **[!UICONTROL Conectarse a Azure]**.

Un mensaje de confirmación indica que la conexión se ha establecido correctamente. Haga clic en **[!UICONTROL Siguiente]** para continuar.

![El paso de credenciales muestra los campos Cuenta de almacenamiento, Contenedor, Ruta de acceso e Id. de inquilino completados con un mensaje de confirmación Conectado a [!DNL Azure].](../../assets/setup/azure-sourcing/azure-credentials-step.png){zoomable="yes"}

### Conceder acceso a Adobe a su almacenamiento de [!DNL Azure] {#grant-adobe-access}

En el paso **[!UICONTROL Consentimiento]**, Collaboration valida los permisos de [!DNL Azure] que configuró anteriormente.

Seleccione el icono de inicio junto a **[!UICONTROL URL de consentimiento]** para abrir el flujo de trabajo de autorización en [!DNL Azure]. Inicie sesión con una cuenta que tenga permiso para conceder consentimiento para la ubicación de almacenamiento y, a continuación, complete las solicitudes de autorización de Azure que conceden a Adobe acceso a la ubicación de almacenamiento configurada. Una vez completada la autorización, vuelva a Collaboration y seleccione **[!UICONTROL Confirmar consentimiento]** para validar el acceso de Adobe.

>[!NOTE]
>
>[!DNL Azure] asignaciones de rol pueden tardar varios minutos en propagarse. Si la validación del consentimiento no se realiza correctamente de inmediato, espere unos minutos, confirme que la entidad de seguridad de servicio de Adobe tiene la asignación de funciones necesaria e inténtelo de nuevo.

Cuando la validación del consentimiento se realiza correctamente, aparece el mensaje de confirmación **[!UICONTROL Consentimiento concedido]**. Haga clic en **[!UICONTROL Siguiente]** para continuar.

![Paso de consentimiento que muestra una dirección URL de consentimiento, el identificador de aplicación \[!DNL Azure\] y un mensaje de confirmación de consentimiento concedido.](../../assets/setup/azure-sourcing/azure-consent-granted-step.png){zoomable="yes"}

### Revisar asignaciones de campo {#review-field-mappings}

En el paso **[!UICONTROL Asignación de campos]**, Collaboration asigna automáticamente los campos de identidad admitidos de los archivos de origen.

No se requiere ninguna configuración manual.

>[!IMPORTANT]
>
> Collaboration asigna automáticamente los campos de identidad en función de la especificación de fuente de audiencias. Si las asignaciones mostradas son incorrectas, actualice los archivos de origen antes de completar el flujo de trabajo de incorporación.

Revise las asignaciones mostradas y confirme que los campos de origen coinciden con las columnas de identidad de los archivos de audiencia. Haga clic en **[!UICONTROL Siguiente]** para continuar.

![Paso de asignación de campos que muestra los campos de origen asignados automáticamente y los campos de identidad de destino sin necesidad de configuración manual.](../../assets/setup/azure-sourcing/azure-field-mapping-step.png){zoomable="yes"}

### Revisión y finalización de la conexión {#review-and-complete}

En el paso **[!UICONTROL Revisar]**, compruebe la cuenta de almacenamiento, el contenedor, la ruta de origen, el identificador de inquilino y las asignaciones de campos.

La página de revisión también indica que el flujo de trabajo actual [!DNL Azure] realiza una única ejecución de abastecimiento y no configura una programación recurrente.

Cuando la configuración sea correcta, seleccione **[!UICONTROL Completar]**.

![El paso Revisar muestra detalles de conexión, asignaciones de campos y un mensaje que indica que la importación de audiencias es una importación única sin programación configurada.](../../assets/setup/azure-sourcing/azure-review-connection-step.png){zoomable="yes"}

## Confirmar la conexión y monitorizar las audiencias de origen {#confirm-connection-and-monitor-audiences}

Después de seleccionar **[!UICONTROL Completar]**, Collaboration crea la conexión de datos y lo desplaza a **[!UICONTROL Configuración]** > **[!UICONTROL Mis conexiones de datos]**.

### Confirme que la conexión se ha creado. {#confirm-connection-created}

La tarjeta de conexión de **[!UICONTROL Mis conexiones de datos]** confirma que la conexión se creó correctamente. La tarjeta muestra el tipo de origen (**[!UICONTROL Azure Blob Storage]** o **[!UICONTROL Azure Data Lake Storage] Gen2**), la fecha de creación, las claves de coincidencia, el recuento de público y el estado de conexión actual.

![La vista Mis conexiones de datos muestra una tarjeta de conexión [!DNL Azure Blob Storage] recién creada con detalles de conexión, claves de coincidencia, recuento de público e información de estado.](../../assets/setup/azure-sourcing/azure-data-connection-card.png){zoomable="yes"}

### Ver audiencias de origen {#view-sourced-audiences}

Una vez creada la conexión, Collaboration empieza a obtener audiencias automáticamente desde la ubicación [!DNL Azure] configurada. Vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Mis audiencias]** para supervisar el progreso de abastecimiento y revisar las audiencias de origen.

Las audiencias de origen aparecen en la tabla **[!UICONTROL Mis audiencias]**. Utilice el estado de la audiencia, el recuento de identidades, el origen, la conexión de datos y la fecha de la última actualización para confirmar que las audiencias esperadas provienen de su conexión de [!DNL Azure].

>[!TIP]
>
>El tiempo de obtención varía según el volumen de datos. Si las audiencias no han aparecido pasadas 24 horas, consulte [Solución de problemas](#troubleshooting).

![La ficha Mis audiencias del área de trabajo de configuración con una nueva audiencia resaltada en la tabla.](../../assets/setup/azure-sourcing/view-sourced-audiences.png)

## Limitaciones conocidas {#known-limitations}

Revise las siguientes limitaciones antes de crear o administrar una conexión de datos de Azure.

* **Restricciones de clave de coincidencia:** Las claves de coincidencia no se pueden quitar de una conexión existente. Para cambiar las claves de coincidencia activas, elimine la conexión y cree una nueva.
* **Una conexión activa por tipo de origen de [!DNL Azure]:** Puede tener una conexión Blob activa y una conexión ADLS Gen2 activa por cuenta. Para cambiar la ubicación de almacenamiento, elimine la conexión existente y cree una nueva.
* **Compatibilidad con subcarpetas:** Collaboration solo ingiere archivos directamente bajo la ruta de acceso configurada. No ingiere archivos de subcarpetas anidadas.
* **Tipos de origen independientes:** Blob y ADLS Gen2 son conexiones distintas; no mezcle la configuración entre ellos en una sola ejecución del asistente.

## Resolución de problemas {#troubleshooting}

### Las audiencias no aparecen o el abastecimiento es lento {#audiences-not-appearing}

Si las audiencias de origen no aparecen después de crear la conexión, complete las siguientes acciones.

* Confirme que los archivos de audiencia existen directamente en la ruta configurada y cumplen con la Especificación del Abastecimiento de audiencias.
* Compruebe si hay errores en **[!UICONTROL Mis conexiones de datos]**.
* Póngase en contacto con el servicio de asistencia de Adobe e indique el nombre de la conexión, la cuenta de almacenamiento y los detalles del contenedor si los problemas persisten pasadas 24 horas.

### Las audiencias se originan, pero muestran cero o identidades inesperadas {#zero-identities}

Si las audiencias aparecen después del origen, pero los recuentos de identidad son cero o inferiores a lo esperado, complete las siguientes acciones.

* Compruebe que todos los valores clave de coincidencia de los archivos de audiencia estén recortados, en minúsculas y con hash SHA256 antes de la carga. Collaboration no hash ni normaliza los datos de ingesta.
* Confirme que las claves de coincidencia presentes en los archivos estén habilitadas para su cuenta de Collaboration. Ver [Configurar claves de coincidencia](https://experienceleague.adobe.com/es/docs/real-time-cdp-collaboration/using/setup/onboard-account#set-up-match-keys).

### Error de conexión después del éxito inicial {#connection-failed}

Utilice estas comprobaciones cuando una conexión se haya creado correctamente pero más tarde introduzca un estado de error.

* Compruebe que la asignación de rol RBAC [!DNL Azure] del principal de Adobe no se quitó ni se estrechó.
* Confirme que los archivos siguen existiendo en la ruta y que coinciden con la especificación.

### Errores de importación o formato {#format-errors}

Utilice estas comprobaciones cuando falle el abastecimiento debido a problemas de estructura de archivos, hash o formato de columna.

* Asegúrese de que todos los archivos mantienen la misma estructura de columnas y reglas de hash que la ingesta inicial.

## Próximos pasos {#next-steps}

Una vez finalizado el abastecimiento, las audiencias estarán disponibles en **[!UICONTROL Mis audiencias]** para los flujos de trabajo de activación, análisis de superposición y medición. Para activar audiencias de origen con colaboradores, consulte [Activar audiencias](../collaborate/activate.md).

Otros métodos de abastecimiento disponibles incluyen Experience Platform, [!DNL Amazon S3], [!DNL Google Cloud Storage], [!DNL Snowflake] y la carga de archivos CSV. Para ver otros métodos de obtención de audiencias, consulte:

* [Configuración de Google Cloud Storage para el abastecimiento de audiencias](./configure-gcs-audience-sourcing.md)
* [Configuración de Snowflake para el abastecimiento de audiencias](./configure-snowflake-audience-sourcing.md)
* [Configuración de AWS S3 para el abastecimiento de audiencias](./configure-aws-s3-audience-sourcing.md)
* [Audiencias de Source de Experience Platform](./onboard-audiences.md)
* [Cargar un archivo CSV para el abastecimiento de audiencias](./upload-csv-audience-sourcing.md)
