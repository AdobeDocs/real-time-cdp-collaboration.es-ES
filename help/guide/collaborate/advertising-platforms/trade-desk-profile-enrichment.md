---
title: Enriquecer perfiles con señales de medios de pago de [!DNL The Trade Desk] (Alpha)
description: Obtenga información sobre cómo exportar atributos de enriquecimiento de medios de pago, ingerir el CSV enviado y actualizar perfiles de origen para la creación y personalización de audiencias.
audience: advertiser
hide: true
badge: Alpha
source-git-commit: d090aff6ea091f60c9b3bbaf2ca72fcf8017d7d1
workflow-type: tm+mt
source-wordcount: '1484'
ht-degree: 1%
---

# Enriquecimiento del perfil de la Trade Desk (Alpha)

Utilice la fuente de datos de registro de impresión de flujo de datos de evento sin procesar (REDS) de [!DNL The Trade Desk] para exportar atributos de enriquecimiento y contexto de medios de pago a sus perfiles de origen.

Una vez que el archivo CSV llegue a su destino de exportación [!DNL Amazon S3], ingréselo en [!DNL Adobe Real-Time CDP]. En esta versión, la exportación del archivo no actualiza automáticamente los perfiles ni activa las experiencias. El enriquecimiento automatizado de perfiles de nuevo a [!DNL Adobe Real-Time CDP] será una característica de una versión posterior.

La exposición de publicidad añade contexto a los perfiles de los clientes. No confirma la participación, la intención de compra ni los intereses a largo plazo.

## Preparación para el enriquecimiento {#prepare-for-enrichment}

Antes de comenzar, colabore con su administrador, equipo de medios y equipo de datos para asegurarse de que dispone de lo siguiente:

* Acceso a [!DNL Adobe Real-Time CDP Collaboration] y un acuerdo de participación firmado.
* Se completó una carta de acceso con [!DNL The Trade Desk] para autorizar el aprovisionamiento de fuentes REDS.
* Audiencias de origen disponibles en [!DNL Adobe Real-Time CDP Collaboration] que utilizan direcciones de correo electrónico con hash o números de teléfono con hash. En esta versión no se admiten otros identificadores.
* Un destino [!DNL Amazon S3] configurado para recibir la salida de enriquecimiento.
* Proceso para introducir el archivo enviado en [!DNL Adobe Real-Time CDP].

### Autorizar la fuente de origen {#authorize-source-feed}

Complete la carta de acceso proporcionada por [!DNL The Trade Desk] para autorizar a [!DNL The Trade Desk] a enviar registros REDS directamente a Adobe.

[!DNL The Trade Desk] aprovisiona la fuente de origen y Adobe configura el acceso y la ingesta. Antes de crear un proyecto, confirme que la conexión está activa y que la fuente está lista.

Después del procesamiento, el archivo de salida de enriquecimiento llega al destino de exportación.

### Preparar la ingesta descendente {#prepare-downstream-ingestion}

Después de la entrega, pídale al administrador de [!DNL Adobe Real-Time CDP] o al equipo de soporte técnico que introduzcan el archivo.

## Conexión y creación de proyectos {#connect-create-projects}

Complete la carta de acceso del cuadro de diálogo de conexión y guarde su ID de socio. Espere a que Adobe confirme la recepción de los registros de REDS antes de crear un proyecto. La creación de un proyecto inicia el trabajo de enriquecimiento, que requiere su ID de socio y los registros.

### Conexión con el socio {#connect-partner}

Conéctese a [!DNL The Trade Desk] y agregue la información de su anunciante:

1. En **[!UICONTROL Connect]**, abra **[!UICONTROL Discover colaboradores]**.
1. Busque [!DNL The Trade Desk].
   ![El catálogo de colaboradores enumera [!DNL The Trade Desk] y su opción [!UICONTROL Conectar].](../../../assets/collaborate/advertising-platforms/discover-collaborators-trade-desk.png){zoomable="yes"}
1. Seleccione **[!UICONTROL Conectar]** para [!DNL The Trade Desk] y siga las instrucciones del cuadro de diálogo de conexión.
   ![El cuadro de diálogo de conexión explica la autorización de REDS y la configuración del ID de socio para [!DNL The Trade Desk].](../../../assets/collaborate/advertising-platforms/trade-desk-connection-instructions.png){zoomable="yes"}
1. Una vez que la conexión esté activa, abra **[!UICONTROL Configuración de la conexión]**. En **[!UICONTROL Información del anunciante]**, selecciona **[!UICONTROL Editar]** para actualizar la información existente o **[!UICONTROL Agregar]** para escribir información nueva.
   ![La configuración de conexión activa muestra [!UICONTROL Información del anunciante] y el control [!UICONTROL Editar].](../../../assets/collaborate/advertising-platforms/trade-desk-connection-settings.png){zoomable="yes"}
1. Escriba su ID de socio y su nombre en **[!UICONTROL ID de socio]** y **[!UICONTROL nombre de socio]**; a continuación, seleccione **[!UICONTROL Guardar]**. Encuentre su ID de socio en su cuenta de [!DNL The Trade Desk] en **[!UICONTROL Identificadores de puestos]**.
   ![El cuadro de diálogo de información del anunciante tiene los campos ID de socio y nombre de socio necesarios, así como un control [!UICONTROL Guardar].](../../../assets/collaborate/advertising-platforms/trade-desk-advertiser-partner-info-dialog.png){zoomable="yes"}

Una vez que la conexión esté activa y guarde la información del anunciante, espere a que se confirme que Adobe ha recibido los registros de REDS. A continuación, cree un proyecto.

### Crear un proyecto {#create-project}

Cree un proyecto para la conexión:

1. En **[!UICONTROL Colaborar]**, seleccione **[!UICONTROL Mis proyectos]**.
1. Seleccione **[!UICONTROL Crear un proyecto]** o el icono de agregar (![Agregar un proyecto.](/help/assets/icons/plus.png)).
1. En **[!UICONTROL Crear proyecto]**, seleccione [!DNL The Trade Desk] de **[!UICONTROL Colaborador]**.
   ![El formulario [!UICONTROL Crear proyecto] enumera [!DNL The Trade Desk] e incluye el nombre del proyecto, la descripción y los campos de imagen.](../../../assets/collaborate/advertising-platforms/trade-desk-create-project.png){zoomable="yes"}
1. Escriba un **[!UICONTROL nombre de proyecto]** y **[!UICONTROL descripción]**, y después elija una imagen para identificar el proyecto.
1. Seleccione **[!UICONTROL Crear]**.

Para administrar proyectos en general, consulte la [Guía de creación y administración de proyectos](/help/guide/collaborate/manage-projects.md).

## Seleccionar y exportar atributos {#select-export-attributes}

Exporte atributos de enriquecimiento del proyecto:

<!-- TODO: Replace the destination screenshot with one showing the [!UICONTROL Export Attributes] action. -->

1. Abra el proyecto y seleccione **[!UICONTROL Enrich]**.
1. Revise los valores de cobertura de cada atributo para comprender la disponibilidad de la señal.
1. Seleccione los atributos que desee utilizar para el enriquecimiento.
   ![La página [!UICONTROL Enrich] agrupa las señales seleccionables por categoría y muestra los valores de cobertura.](../../../assets/collaborate/advertising-platforms/enrich-attribute-selection.png){zoomable="yes"}
1. Seleccione el destino de exportación [!DNL Amazon S3] configurado para la salida de enriquecimiento. Para configurar un destino, consulte [Configurar y administrar destinos de almacenamiento en la nube](/help/guide/destinations/manage-destinations.md).
   <!-- ![The [!UICONTROL Choose a destination] screen lists a destination and the [!UICONTROL Export Attributes] action.](../../../assets/collaborate/advertising-platforms/enrich-choose-destination.png){zoomable="yes"} -->
1. Revise los atributos y el destino seleccionados y, a continuación, seleccione **[!UICONTROL Exportar atributos]**.
   <!-- ![The destination screen confirms that enrichment has started.](../../../assets/collaborate/advertising-platforms/enrich-request-confirmation.png){zoomable="yes"} -->

Al enviar una exportación, se inicia la entrega si el destino está configurado correctamente. Verifique que la entrega de archivos se haya realizado correctamente fuera de [!DNL Adobe Real-Time CDP Collaboration].

Adobe procesa los atributos de enriquecimiento cuando crea un proyecto y luego semanalmente. Cada ejecución usa los últimos 90 días de los datos de [!DNL The Trade Desk] disponibles. Cada exportación incluye los atributos seleccionados de la ejecución completada más reciente. Para exportar atributos actualizados, solicite otra exportación una vez finalizada una ejecución posterior.

### Señales de ampliación disponibles {#available-signals}

Seleccione entre 18 señales depuradas en cuatro categorías. No se admiten expresiones de enriquecimiento personalizadas.

| Categoría | Señal | Descripción |
| --- | --- | --- |
| Núcleo | [!UICONTROL Última fecha de exposición] | La fecha en la que se expuso una identidad más recientemente a un anuncio. |
| Núcleo | [!UICONTROL Recuento de exposición] | Una categoría de frecuencia de exposición, en lugar de un recuento de impresiones sin procesar. |
| Núcleo | [!UICONTROL Prospección y redireccionamiento] | Clasificación deducida de la exposición como prospección o remarketing. |
| Núcleo | [!UICONTROL Se muestra la categoría del producto] | Una categoría deducida para los productos promocionados en los anuncios. |
| Núcleo | [!UICONTROL Canal de inventario dominante] | El canal de inventario principal asociado con la exposición de publicidad. |
| Núcleo | [!UICONTROL Tipo de dispositivo dominante] | El tipo de dispositivo principal asociado con la exposición del anuncio. |
| Geografía | [!UICONTROL Ciudad] | Información de la ciudad derivada del contexto publicitario, no una ubicación verificada. |
| Geografía | [!UICONTROL Región / Estado] | Información de región o estado del contexto publicitario. |
| Geografía | [!UICONTROL DMA] | Información de área de mercado designada (DMA) derivada del contexto publicitario. |
| Televisión conectada (CTV) | [!UICONTROL CTV expuesto] | Exposición de anuncios en un dispositivo de televisión conectado. |
| Televisión conectada (CTV) | [!UICONTROL Visor de flujo en directo] | Exposición de anuncios en el inventario de flujo en directo, no prueba de visualización o participación. |
| Televisión conectada (CTV) | [!UICONTROL PMP / exposición premium] | Mercado privado (PMP) o exposición de contrato privado, no inventario de primas verificado de forma independiente. |
| Afinidad del contenido | [!UICONTROL Transmisión por televisión conectada] | Exposición de publicidad asociada al contenido de streaming. |
| Afinidad del contenido | [!UICONTROL Jugador] | Exposición de publicidad asociada a contenido, sitios o aplicaciones de juegos. |
| Afinidad del contenido | [!UICONTROL Aficionado a los deportes] | Exposición de publicidad asociada a contenido deportivo, sitios o aplicaciones. |
| Afinidad del contenido | [!UICONTROL Seguidor de noticias] | Exposición de publicidad asociada a contenido de noticias, sitios o aplicaciones. |
| Afinidad del contenido | [!UICONTROL Amante de la música] | Exposición de publicidad asociada a contenido de música, sitios o aplicaciones. |
| Afinidad del contenido | [!UICONTROL Género de contenido] | El género de contenido asociado con la exposición de publicidad. |

Las señales geográficas describen el contexto publicitario en lugar de una casa verificada o una ubicación actual. Las señales de afinidad del contenido no confirman los intereses ni las preferencias personales. Es posible que algunos atributos no contengan valores cuando la información de origen no está disponible.

### Cobertura de atributo {#attribute-coverage}

La cobertura describe la frecuencia con la que los registros procesados incluyen un valor de atributo. Para las señales sí/no, como **[!UICONTROL CTV expuesto]**, la cobertura cuenta los registros con un valor verdadero. La cobertura no indica tasas de coincidencia de identidad ni la proporción de perfiles de origen que recibirán un atributo.

La coincidencia de identidad, la disponibilidad de la señal de origen y la ingesta afectan a las actualizaciones de perfil. La cobertura no confirma la finalización de la exportación ni las actualizaciones del perfil.

### Ámbito del flujo de trabajo {#workflow-scope}

Utilice el catálogo depurado para enriquecer los datos de [!DNL The Trade Desk]. No puede exportar registros sin procesar ni crear expresiones de atributo personalizadas. No se admiten otras integraciones de plataforma del lado de la demanda (DSP) y plataforma del lado de la oferta (SSP).

Este flujo de trabajo no admite el descubrimiento de oportunidades de enriquecimiento, el análisis de superposición de audiencias o la medición de atribución e incrementalidad.

## Ingesta y validación de resultados {#ingest-validate-results}

Después de la entrega, pídale al administrador de [!DNL Adobe Real-Time CDP] o al equipo de soporte técnico que introduzcan el archivo.

### Archivo de salida {#output-file}

La exportación envía un archivo CSV al destino configurado [!DNL Amazon S3].

<!-- 
TODO: replace this placeholder with the engineering-confirmed output specification:
* Required hashing and normalization for each identifier, including whether email requires SHA-256 after trimming and lowercasing.
* Exact CSV headers, the file naming pattern, and the delivery bucket and path.
* Each identifier column in the delivered file and the identity namespace to map that column to during ingestion.
Do not treat example formats or supported input match keys as confirmed output requirements.
-->

Compruebe la exportación de forma independiente de las actualizaciones de perfil:

1. Confirme que el archivo CSV ha llegado a la ubicación [!DNL Amazon S3] deseada.
1. Compruebe que el archivo contiene los identificadores esperados y los atributos seleccionados.
1. Introduzca el archivo utilizando las asignaciones de identidad y esquema confirmadas para la zona protegida y el conjunto de datos de destino.
1. Revise los resultados de la ingesta y compruebe que una muestra de perfiles esperados contenga los atributos de enriquecimiento.

La exportación de un archivo no confirma que la ingesta haya actualizado los perfiles. Introduzca cada exportación posterior por separado para actualizar los perfiles.

## Solución de problemas de enriquecimiento {#troubleshoot-enrichment}

Utilice estas comprobaciones para solucionar problemas de datos de origen, exportación e ingesta:

| Problema | Qué comprobar |
| --- | --- |
| La conexión de **[!UICONTROL Enrich]** no está disponible | Solicite al administrador que confirme la conexión y el acceso al proyecto. Confirme que la configuración de la fuente de origen haya finalizado. |
| No hay ningún destino de exportación disponible | Pida al administrador que confirme que hay un destino configurado y disponible para la salida de enriquecimiento. |
| Un atributo tiene una cobertura limitada | Revise la disponibilidad de los datos de origen con su equipo de medios. No interprete la cobertura como una tasa de coincidencia de perfil. |
| Se solicitó una exportación, pero no hay ningún archivo presente | Compruebe el destino deseado con su equipo de datos. El envío de la solicitud no confirma la entrega. |
| Un archivo enviado no tiene perfiles actualizados | Revise los resultados de la ingesta y confirme las asignaciones de identidad y esquema. La exportación y la ingesta son operaciones independientes. |
| No se puede solicitar una exportación | Seleccione al menos un atributo y un destino. Si una exportación ya se está procesando, espere hasta que termine antes de solicitar otra. |
| La cobertura es alta, pero pocos perfiles reciben atributos | La cobertura no es una tasa de coincidencia de identidad. Confirme que la fuente de origen esté lista, que la audiencia utilice claves de coincidencia admitidas y que la asignación de identidad sea correcta durante la ingesta. |
| No aparecen atributos ni cobertura después de crear un proyecto | La configuración del proyecto se soluciona al crearlo. Si Adobe no hubiera recibido los registros de REDS de [!DNL The Trade Desk] en ese momento, el proyecto no podrá usarlos más adelante. Una vez que Adobe confirme la recepción de los registros, cree un nuevo proyecto. |
| Los perfiles tienen los atributos, pero una audiencia o experiencia no los refleja | Compruebe las reglas de evaluación de audiencia, identidad, consentimiento y segmentación de experiencias descendentes. |

## Próximos pasos {#next-steps}

Después de ingerir y validar los atributos, genere audiencias en [!DNL Adobe Real-Time CDP] combinando señales de enriquecimiento con datos de origen. Para obtener más información, consulte la [guía del Generador de audiencias](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-builder){target="_blank"}.

Para activar audiencias para destinos, personalización o recorridos de clientes, consulta la [guía de activación de audiencias](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activation-overview){target="_blank"}.
