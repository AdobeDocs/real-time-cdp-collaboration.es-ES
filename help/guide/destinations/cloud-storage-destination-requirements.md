---
title: Requisitos de conexión de destino
description: Revise la información de conexión necesaria para configurar los destinos admitidos en Real-Time CDP Collaboration.
audience: admin, publisher
source-git-commit: c84582bb81289ce761c664af7db177535ff00a00
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%

---

# Requisitos de conexión de destino

Antes de configurar un destino en Real-Time CDP Collaboration, obtenga las credenciales y la información de conexión que requiera el proveedor de destino.

Esta página resume los métodos de autenticación disponibles en Collaboration. Para obtener instrucciones sobre cómo crear credenciales, asignar permisos, configurar el acceso a la red o preparar el sistema de destino, consulte la documentación de destino de Adobe Experience Platform vinculada.

>[!NOTE]
>
>La documentación de Adobe Experience Platform vinculada describe el flujo de trabajo de destino estándar. Es posible que algunos pasos, campos u opciones no se apliquen al configurar el destino en Real-Time CDP Collaboration.

## Resumen de los requisitos {#requirements-at-a-glance}

| Destino | Método de autenticación o conexión | Preparar antes de empezar | Requisitos detallados |
|---|---|---|---|
| [!DNL Amazon S3] | Clave de acceso y clave secreta, o función asumida | Par de claves de acceso a AWS o ARN de la función IAM; información de bloque y carpeta | [[!DNL Amazon S3] documentación de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3) |
| SFTP | Contraseña o clave SSH | Dominio del servidor, puerto, nombre de usuario, credencial de autenticación y ruta de carpeta | [Documentación de destino SFTP](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp) |
| [!DNL Azure Blob Storage] | Cadena de conexión | Cadena de conexión de almacenamiento de Azure, contenedor e información de carpeta | [[!DNL Azure Blob Storage] documentación de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob) |
| [!DNL Google Cloud Storage] | ID de clave de acceso y clave de acceso secreta | [!DNL Google Cloud Storage] credenciales de interoperabilidad, espacio e información de carpeta | [[!DNL Google Cloud Storage] documentación de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage) |
| [!DNL Snowflake Batch] | Compartir datos de [!DNL Snowflake] | [!DNL Snowflake]: id. de cuenta, región, estado de vínculo privado y acceso a listados privados | [[!DNL Snowflake Batch] documentación de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch) |
| [!DNL Data Landing Zone] | No se requiere autenticación independiente | Ruta de la carpeta de destino y preferencias de salida de archivo | [[!DNL Data Landing Zone] documentación de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone) |

## Notas del conector {#connector-notes}

Revise los siguientes métodos de autenticación específicos del conector y las diferencias del flujo de trabajo antes de configurar un destino.

### [!DNL Amazon S3] {#amazon-s3}

Collaboration admite la autenticación de **[!UICONTROL Clave de acceso]** y **[!UICONTROL Función asumida]**. La autenticación de clave de acceso requiere una clave de acceso y una clave de acceso secreta. La autenticación de la función asumida requiere el ARN de una función de AWS IAM que Adobe puede asumir.

Para obtener la configuración de credenciales, funciones y permisos, consulte [Autenticar con el [!DNL Amazon S3] destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#authenticate).

### SFTP {#sftp}

Collaboration admite **[!UICONTROL SFTP con contraseña]** y **[!UICONTROL SFTP con autenticación de clave SSH]**. Ambos métodos requieren el dominio del servidor, el puerto y el nombre de usuario. El puerto toma el valor predeterminado de `22`.

Para conocer los requisitos de formato, servidor, red y lista de permitidos de la clave SSH, consulte [Información de autenticación SFTP](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp#authentication-information).

### [!DNL Azure Blob Storage] {#azure-blob-storage}

Collaboration se autentica en [!DNL Azure Blob Storage] mediante una cadena de conexión de cuenta de almacenamiento.

Para obtener instrucciones sobre cómo obtener la cadena de conexión y asignar permisos de almacenamiento, consulte [Autenticar con el [!DNL Azure Blob Storage] destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob#authenticate).

### [!DNL Google Cloud Storage] {#google-cloud-storage}

Collaboration requiere un id. de clave de acceso [!DNL Google Cloud Storage] y una clave de acceso secreta generadas a través de la configuración de interoperabilidad de [!DNL Google Cloud Storage].

Para conocer los requisitos de generación de credenciales y permisos de bloque, consulte [Autenticar con el [!DNL Google Cloud Storage] destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage#authenticate).

### [!DNL Snowflake Batch] {#snowflake-batch}

[!DNL Snowflake Batch] utiliza el uso compartido de datos de [!DNL Snowflake] en lugar de exportar archivos al almacenamiento administrado por el cliente. En Collaboration, no hay ningún paso de autenticación independiente. Introduzca el ID de cuenta de Snowflake, la región, el estado de vínculo privado y la confirmación de propiedad de la cuenta durante la creación del destino.

Para conocer los requisitos para la preparación de cuentas y las listas privadas, consulte [[!DNL Snowflake Batch] documentación de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch).

### [!DNL Data Landing Zone] {#data-landing-zone}

[!DNL Data Landing Zone] está aprovisionado por Adobe y no requiere un paso de autenticación independiente en Collaboration. Durante la creación del destino, especifique la ruta de la carpeta de destino y la configuración de salida del archivo.

Para obtener información sobre el acceso a [!DNL Data Landing Zone] aprovisionado por AWS, vea [Autenticar en la zona de aterrizaje de datos aprovisionada por AWS](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone#authenticate-dlz-aws).

## Próximos pasos {#next-steps}

Después de obtener la información de conexión necesaria, [configure y administre un destino](./manage-destinations.md).
