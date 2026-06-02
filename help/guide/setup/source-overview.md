---
title: Información general de fuentes
description: Obtenga información acerca de los conectores de origen en Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
source-git-commit: 07666bc6d001e602c270a611ad1da3ea5f301dbd
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 6%

---

# Información general de fuentes

En Adobe Real-Time CDP Collaboration, una fuente (o conexión de datos) es de donde provienen los datos de audiencia. Puede conectarse a varios tipos de fuentes, como aplicaciones de Adobe, almacenamiento basado en la nube o archivos de su sistema local, para [crear y administrar audiencias](./onboard-audiences.md) para sus proyectos de Collaboration. Durante el flujo de trabajo de fuentes de audiencia, puede elegir y configurar su fuente preferida según las necesidades de su organización.

## Conectar un origen {#connect-a-source}

Para conectar un origen, debe introducir el flujo de trabajo de abastecimiento. En primer lugar, vaya a la ficha **[!UICONTROL Mis audiencias]** en el área de trabajo **[!UICONTROL Configuración]**.

Seleccione el icono de agregar (![Agregar icono.](/help/assets/icons/plus.png)) y, a continuación, seleccione **[!UICONTROL Audiencia]** para iniciar el flujo de trabajo de abastecimiento.

![Área de trabajo de Mis audiencias con la opción Agregar y las opciones de Audiencias resaltadas.](/help/assets/setup/add-manage-audiences/add-audiences.png)

Durante el flujo de trabajo, se le pedirá que seleccione un origen para añadir una nueva conexión de datos. La fuente que elija determina cómo se llevan los datos de audiencia a Collaboration. Consulte la tabla [orígenes disponibles](#available-sources) para obtener una lista de todos los orígenes admitidos.

![Espacio de trabajo Agregar audiencias con la opción Agregar una nueva conexión de datos resaltada.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

Después de seleccionar un origen, el flujo de trabajo le guía a través de los pasos de configuración específicos de la conexión, incluida la autenticación, la asignación de campos, la programación y la selección de audiencias.

### Fuentes disponibles {#available-sources}

Las siguientes fuentes están disponibles en Collaboration. Para ver la guía de abastecimiento paso a paso para ese origen, seleccione el nombre del origen en la tabla siguiente. Si está interesado en un origen que no está disponible actualmente, póngase en contacto con su representante de Adobe.

| Fuente | Descripción | Disponibilidad |
| --- | --- | --- |
| [Adobe Experience Platform](./onboard-audiences.md) | Incluya audiencias de la instancia de Experience Platform conectada y reutilice los segmentos de clientes existentes. | Disponible |
| [Amazon S3](./configure-aws-s3-audience-sourcing.md) | Conecte los bloques de S3 para obtener grandes conjuntos de datos de origen desde su infraestructura en la nube. | Disponible |
| [[!DNL Snowflake]](./configure-snowflake-audience-sourcing.md) | Conecte su [!DNL Snowflake Secure Data Share] para incorporar conjuntos de datos de audiencia a gran escala. | Disponible |
| [[!DNL Google Cloud Storage]](./configure-gcs-audience-sourcing.md) | Conecte los bloques de GCS para introducir los datos de audiencia almacenados en su entorno [!DNL Google Cloud]. | Disponible |
| [Carga de archivo CSV](./upload-csv-audience-sourcing.md) | Cargue un archivo CSV con formato directamente desde el sistema local. | Disponible |
| Adobe Audience Manager | Incluya segmentos de Audience Manager existentes en sus proyectos de Collaboration. | *Próximamente* |
| [!DNL Azure Blob Storage] | Conecte los contenedores de [!DNL Azure Blob Storage] para obtener conjuntos de datos de origen desde el entorno de [!DNL Microsoft Azure]. | *Próximamente* |
| [!DNL Azure Data Lake Storage] | Conecte su cuenta de [!DNL Azure Data Lake Storage Gen 2] para introducir los datos de audiencia almacenados en su repositorio de datos de [!DNL Azure]. | *Próximamente* |

{style="table-layout:auto"}

## Próximos pasos

Después de conectar una fuente e incorporar las audiencias, puede ver detalles, actualizar configuraciones o eliminar fuentes existentes. Para obtener más información, consulte la guía [Administrar conexiones de datos](./manage-data-connection.md).
