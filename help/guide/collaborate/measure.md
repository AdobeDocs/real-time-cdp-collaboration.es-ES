---
title: Rendimiento de medida
description: Mida el rendimiento de las campañas en diferentes canales. Aprenda a utilizar e interpretar varios informes.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
source-git-commit: e06ee94afdd1edbf86430cbe348dc448419b8f4e
workflow-type: tm+mt
source-wordcount: '2612'
ht-degree: 6%

---

# Rendimiento de medida

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>El área de trabajo **[!UICONTROL Measure]** solo está disponible si el caso de uso **Measurement** se habilitó [durante el proceso de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./manage-projects.md#project-use-cases).

Obtenga información sobre los informes disponibles en Adobe Real-Time CDP Collaboration y comprenda cómo medir y analizar el rendimiento de sus campañas de marketing en varios canales.

## Requisitos previos {#prerequisites}

Para poder acceder a los informes de medición en Collaboration, debe:

* [Conectar](/help/guide/connect/establishing-connections.md) con un colaborador con el caso de uso de **Medición** habilitado
* Colabore en al menos un proyecto con su colaborador. Aprenda a [crear un proyecto](/help/guide/collaborate/manage-projects.md#create-project).
* Ejecute la campaña y asegúrese de que se proporcione un [ID de campaña para la campaña](../collaborate/manage-projects.md#manage-campaign-id):
   * Si es editor, introduzca el ID de campaña vinculado a la campaña del anunciante.
   * Si es anunciante, solicite a su colaborador (editor) que proporcione el ID de campaña. Esto es necesario para [generar informes en el espacio de trabajo de Measure](#create-measurement-report).
* [Cargar datos de medición](/help/guide/setup/onboard-measurement-data.md) en Collaboration si desea [crear informes de atribución](#create-attribution-report).

## Ver informes {#view-reports}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report_campaignID"
>title="ID de campaña"
>abstract="Marcador de posición para añadir información relevante en la interfaz de usuario sobre lo que son los ID de campaña."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report"
>title="ID de campaña"
>abstract="Marcador de posición para añadir información relevante en la interfaz de usuario sobre lo que son los ID de campaña."

Para ver los informes disponibles en la pestaña de medición:

1. Vaya a **[!UICONTROL Colaborar]** > **[!UICONTROL Mis proyectos]**.
2. Para el proyecto deseado y seleccione **[!UICONTROL Ver]**.
3. En el proyecto, seleccione la ficha **[!UICONTROL Medida]**.

Seleccione **[!UICONTROL Ver informe completo]** para acceder a los distintos informes disponibles, que se detallan a continuación.

![Cómo llegar a la ficha de medición en un proyecto.](/help/assets/collaborate/measure/measurement.gif)

### Vista de resumen

La vista de la parte superior de la página en la pestaña de medición muestra un resumen de la campaña con algunos números de alto nivel a los que puede hacer referencia:

**[!UICONTROL Impresiones]**: Número total de veces que se ha mostrado el elemento creativo.
**[!UICONTROL Alcance único]**: El número de identidades individuales que vieron al creativo.
**[!UICONTROL Frecuencia promedio total]**: Se alcanzó el número de impresiones dividido por identidades únicas. Esta figura indica con qué frecuencia se mostraron las identidades del creativo.

![Vista de resumen de campaña](/help/assets/collaborate/measure/campaign-summary.png)

### Métricas a lo largo del tiempo {#metrics-over-time}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measure_metricsovertime"
>title="Métricas a lo largo del tiempo"
>abstract="Utilice la vista de métricas a lo largo del tiempo para comprender la cantidad total de impresiones que se muestran para su creativo durante el periodo de la campaña. Puede seleccionar un máximo de dos dimensiones para mostrarlas en el informe."

Utilice la vista de métricas a lo largo del tiempo para comprender la cantidad total de impresiones que se muestran para su creativo durante el periodo de la campaña. Tenga en cuenta que puede seleccionar un máximo de dos métricas para mostrarlas y analizarlas en el informe.

![Vista de métricas a lo largo del tiempo.](/help/assets/collaborate/measure/metrics-over-time.png)

### Distribución de frecuencia {#frequency-distribution}

Utilice la vista de distribución de frecuencias para comprender el desglose de cuántas impresiones se mostraron a cada usuario único. Esta vista puede ayudarle en campañas futuras a decidir desde qué punto desea comenzar a suprimir audiencias. Por ejemplo, es posible que desee suprimir perfiles que ya han visto un creativo tres veces.

![Vista de distribución de frecuencia.](/help/assets/collaborate/measure/frequency-distribution.gif)

### Métrica por dimensión {#metric-by-dimension}

Analice diferentes métricas, como impresiones, impresiones visibles, alcance único, coste, etc., en el contexto del medio de colocación. Analice qué medio (por ejemplo, streaming móvil, programación de CTV u otros) ofrece los mejores resultados para sus campañas.

![Métrica por dimensión.](/help/assets/collaborate/measure/metric-by-dimension.png)

### Curva de alcance acumulativo {#cumulative-reach-curve}

A medida que la campaña progresaba y el número de impresiones aumentaba, comprenda si el número de usuarios a los que pudo llegar también había aumentado. Un patrón común en las campañas es que después de un punto determinado se llega a una meseta en la que el creativo se muestra a la misma gente una y otra vez. Esta vista puede ayudarle a ajustar la duración de las campañas futuras, en función del momento en que ya no se llegaba a nuevas personas.

![Curva de alcance acumulativa.](/help/assets/collaborate/measure/cumulative-reach-curve.png)

### Impresiones por ubicación {#impressions-by-placement}

Comprenda qué medio está generando impresiones para su creativo. Esto puede ayudarle a decidir dónde invertir su gasto en publicidad en futuras campañas.

![Impresiones por ubicación.](/help/assets/collaborate/measure/impressions-by-placement.png)

### Conversiones acumuladas {#cumulative-conversions}

Esta vista proporciona un desglose detallado de los eventos de conversión que elige medir en formato de tabla. La tabla incluye:

* **Evento de conversión**: Nombre de cada evento de conversión que está rastreando.
* **Recuento de conversiones**: Recuento total de conversiones que se produjeron para cada evento.
* **Ingresos estimados**: Valor estimado atribuido a cada evento de conversión.

Revise esta tabla para evaluar la eficacia de la campaña para impulsar las acciones deseadas.

![Conversiones acumulativas.](/help/assets/collaborate/measure/cumulative-conversions.png)

### Conversiones por día {#conversions-by-day}

Este gráfico proporciona un desglose día a día de las conversiones para cada evento configurado al crear un informe de atribución. Utilice esta vista para descubrir patrones diarios, identificar periodos de actividad de conversión alta o baja y comparar el rendimiento de los distintos eventos de conversión en la cronología de la campaña.

![Conversiones por día.](/help/assets/collaborate/measure/conversions-by-day.gif)

## Crear informe de medición {#create-measurement-report}

En Collaboration, puede crear dos tipos principales de informes de medición:

* **Resumen de campaña**: proporciona métricas de alto nivel como alcance, impresiones, frecuencia promedio y envío por canal, lo que ofrece una visión general rápida del rendimiento general de la campaña.
* **Atribución**: mide cómo las exposiciones de campaña impulsan acciones descendentes como conversiones o compras, lo que le ayuda a comprender la eficacia de la campaña.

Puede ejecutar el informe Resumen de campaña por su cuenta, mientras que el informe Atribución requiere que se seleccionen juntos ambos tipos de informe.

### Crear informe de resumen de campaña {#create-campaign-summary-report}

Tanto los editores como los anunciantes pueden generar **informes de resumen de campaña** para evaluar el rendimiento de la campaña. Use estos informes para obtener información sobre métricas clave como [alcance](#cumulative-reach-curve), [frecuencia](#frequency-distribution) e [impresiones](#impressions-by-placement), y para comprender cómo se entregó la campaña y su impacto general.

Para generar un informe de **Resumen de campaña**, vaya al área de trabajo del proyecto desde el área de trabajo de **[!UICONTROL Collaborator]**. En la ficha **[!UICONTROL Medida]**, seleccione el icono Agregar (![Agregar icono.](/help/assets/icons/plus.png)) y luego seleccione **[!UICONTROL Measure]**.

Si este es su primer informe, también puede seleccionar la opción **[!UICONTROL Ejecutar informe]**.

![La ficha Medida resalta las opciones Ejecutar informe y Medida.](/help/assets/collaborate/measure/run-measure-report.png)

Aparecerá la pantalla **[!UICONTROL Crear informe de medición]** con campos de información y entrada agrupados en las secciones **[!UICONTROL Detalles de facturación]**, **[!UICONTROL Detalles de campaña]** y **[!UICONTROL Detalles del informe]**.

#### Detalles de facturación {#billing-details}

Esta sección explica cómo se utilizan los créditos al generar informes de medición. La responsabilidad crediticia se ha establecido durante la [configuración de la conexión](../connect/establishing-connections.md#credit-split). Antes de ejecutar cualquier informe, asegúrese de revisar y confirmar la configuración de división de crédito y las funciones de creación de informes con su colaborador.

#### Detalles de la campaña {#campaign-details}

En la sección **[!UICONTROL Detalles de la campaña]**, seleccione el **ID del anunciante** apropiado para asociarlo a su informe. Estos nombres o identificadores de anunciantes se agregaron durante [configuración de conexión](../connect/establishing-connections.md#advertiser-names). Si solo se configuró un nombre, aparece de forma predeterminada. Si no se configuró ningún nombre, el campo **[!UICONTROL ID del anunciante (nombre)]** se deshabilita y se rellena previamente con el nombre de la cuenta del anunciante.

![Se deshabilitó la opción Crear informe de medición que muestra la opción ID del anunciante (nombre).](/help/assets/collaborate/measure/advertiser-id.png)

A continuación, seleccione la campaña que desee en el menú desplegable **[!UICONTROL ID de campaña]**. Este menú enumera todos los ID de campaña introducidos por el editor para el proyecto. Si la campaña que necesita no está disponible, [agréguela a la interfaz de usuario](./manage-projects.md#manage-campaign-id) antes de generar el informe.

![Se ha expandido la pantalla Crear informe de medición que muestra el menú desplegable ID de campaña.](/help/assets/collaborate/measure/campaign-id.png)

A continuación, especifique el período que desea que abarque el informe. Seleccione **[!UICONTROL Intervalo de fechas del informe]** y, a continuación, utilice el calendario para elegir las fechas de inicio y finalización.

![La pantalla Crear informe de medición muestra el calendario del intervalo de fechas del informe.](/help/assets/collaborate/measure/report-date-range.png)

#### Detalles del informe {#report-details}

**Fecha de ejecución del informe**

En la sección **[!UICONTROL Detalles del informe]**, elija la fecha en que se debe ejecutar el informe. Seleccione **[!UICONTROL Fecha de ejecución del informe]** y elija la fecha que prefiera en el calendario.

* Si elige la fecha de hoy o una fecha pasada, el informe **Resumen de campaña** se ejecuta inmediatamente.
* Si elige una fecha futura, el informe **Resumen de campaña** está programado para ejecutarse ese día.

![La pantalla Crear informe de medición muestra el calendario de fechas de ejecución del informe.](/help/assets/collaborate/measure/report-run-date.png)

**Tipo de informe**

* Si usted es un anunciante, puede seleccionar el tipo de informe **[!UICONTROL Resumen de campaña]** de entre las opciones disponibles. Solo los anunciantes pueden generar informes de atribución.
* Si usted es un editor, el tipo de informe **[!UICONTROL Resumen de campaña]** está preseleccionado y no se puede cambiar. En este momento, los editores no pueden ejecutar informes de atribución.

![La pantalla Crear informe de medición muestra la opción Resumen de campaña como un tipo de informe preseleccionado e inmodificable.](/help/assets/collaborate/measure/cs-report-type.png)

Finalmente, revisa tu configuración y selecciona **[!UICONTROL Crear]**. El informe de resumen de la campaña se genera inmediatamente si la fecha de ejecución es hoy, antes o en la fecha futura elegida. Puede editar el informe programado antes de su fecha de ejecución. Para obtener instrucciones paso a paso, consulte la sección [Editar informe de medición].

Una vez que esté disponible, podrá ver el informe en cualquier momento en la ficha **[!UICONTROL Measure]** del área de trabajo del proyecto.

![La pantalla Crear informe de medición muestra la información y la opción Crear resaltada.](/help/assets/collaborate/measure/cs-review.png)

### Crear informe de atribución {#create-attribution-report}

Como anunciante, puede generar informes de **Atribución** para evaluar cómo las exposiciones de su campaña contribuyen a resultados clave como suscripciones o compras. Utilice estos informes para comprender las interacciones de los usuarios con su campaña, identificar qué puntos de contacto impulsan el mayor impacto e informar estrategias de marketing más efectivas.

>[!IMPORTANT]
>
> Debe [obtener sus datos de medición](../setup/onboard-measurement-data.md#add-measurement-data) en Collaboration antes de generar informes de atribución.
>![La ficha Medida con los requisitos para los datos de medición y la opción Medida deshabilitada.](/help/assets/collaborate/measure/require-measurement-data.png)

Para generar un informe de **Atribución**, vaya al área de trabajo del proyecto desde el área de trabajo de **[!UICONTROL Collaborator]**. En la ficha **[!UICONTROL Medida]**, seleccione el icono Agregar (![Agregar icono.](/help/assets/icons/plus.png)) y luego seleccione **[!UICONTROL Measure]**.

Si este es su primer informe, también puede seleccionar la opción **[!UICONTROL Ejecutar informe]**.

![La ficha Medida resalta las opciones Ejecutar informe y Medida.](/help/assets/collaborate/measure/run-measure-report-attribution.png)

Aparecerá la pantalla **[!UICONTROL Crear informe de medición]** con campos de información y entrada agrupados en las secciones **[!UICONTROL Detalles de facturación]**, **[!UICONTROL Detalles de campaña]** y **[!UICONTROL Detalles del informe]**.

Lea y siga los pasos de la sección [Crear informe de resumen de campaña](#create-campaign-summary-report) para establecer la siguiente configuración:

* [Detalles de facturación](#billing-details)
* [Detalles de la campaña](#campaign-details)

#### Detalles de los informes de Attribution {#report-details-attribution}

**Fecha de ejecución del informe**

>[!IMPORTANT]
>
> Para los informes de atribución, la fecha de ejecución del informe debe ser una fecha futura y debe producirse al menos un día después de la fecha de finalización del intervalo de fechas del informe más la duración completa de la ventana retrospectiva definida.
> **Fecha de ejecución del informe ≥ fecha de finalización del informe + ventana retrospectiva + 1**
> 
> Por ejemplo, si el intervalo de fechas del informe finaliza el 15 de junio y la ventana retrospectiva es de 14 días, la fecha de ejecución del informe es el 30 de junio o posterior.

En la sección **[!UICONTROL Detalles del informe]**, elija la fecha en que se debe ejecutar el informe. Seleccione **[!UICONTROL Fecha de ejecución del informe]** y elija la fecha que prefiera en el calendario.

**Tipo de informe**

Como anunciante, puede seleccionar **[!UICONTROL Atribución]** como tipo de informe, además de **[!UICONTROL Resumen de campaña]**. Al elegir el informe Atribución, los resultados incluyen tanto métricas de Resumen de campaña estándar como análisis de Atribución detallados, lo que proporciona una vista completa del rendimiento de la campaña.

![La pantalla Crear informe de medición resalta los tipos de informe Resumen de campaña y Atribución seleccionados.](/help/assets/collaborate/measure/attribution-report-type.png)

Cuando selecciona **[!UICONTROL Atribución]** como tipo de informe, aparece una sección de configuración de **[!UICONTROL Atribución]** con la configuración adicional necesaria:

* **Ventana retrospectiva en días**: Define hasta qué punto el informe considera las impresiones de campaña antes de cada conversión. Solo las impresiones dentro de este periodo son elegibles para el crédito de atribución.
* **Eventos de conversión**: Especifica qué acciones de conversión desea medir, por ejemplo, compras o suscripciones. Estos eventos deben configurarse con antelación al [obtener los datos de medición](../setup/onboard-measurement-data.md#add-conversion-event) en Collaboration.

En primer lugar, escriba un valor para la ventana retrospectiva **[!UICONTROL en días]** o ajústelo con las opciones de incremento/disminución.

![La pantalla Crear informe de medición resalta el valor de la ventana Retrospectiva en días.](/help/assets/collaborate/measure/lookback-window-in-days.png)

A continuación, elija hasta **3** eventos de conversión de la lista disponible. Para obtener más información sobre un evento en particular, seleccione el icono **[!UICONTROL i]** para ver sus detalles.

![La pantalla Crear informe de medición resalta los eventos de conversión seleccionados y la información del evento de compra.](/help/assets/collaborate/measure/attribution-conversion-events.png)

Finalmente, revisa tu configuración y selecciona **[!UICONTROL Crear]** para programar el informe. El informe de atribución se generará en la fecha de ejecución especificada. Puede editar el informe programado antes de su fecha de ejecución. Para obtener instrucciones paso a paso, consulte la sección [Editar informe de medición].

Una vez que esté disponible, podrá ver el informe en cualquier momento en la ficha **[!UICONTROL Measure]** del área de trabajo del proyecto.

![La pantalla Crear informe de medición muestra la información y la opción Crear resaltada.](/help/assets/collaborate/measure/attribution-review.png)

## Editar informe de medición {#edit-measurement-report}

>[!IMPORTANT]
>
>Puede editar la configuración de un informe de medición únicamente si está programado para ejecutarse en el futuro. No se puede cambiar la configuración de los informes que ya se han ejecutado.

Actualice la configuración de un informe de medición para asegurarse de que el informe proporcione el análisis correcto de la campaña en un período específico y se ejecute en una fecha deseada.

Para empezar, vaya al espacio de trabajo del informe de medición que desee actualizar. Seleccione el icono de edición (![Editar icono](/help/assets/icons/edit.png)) junto al icono de eliminación.

![Área de trabajo del informe de medición con el icono Editar resaltado.](/help/assets/collaborate/measure/edit-report.png)

>[!TIP]
>
>En la pestaña **[!UICONTROL Measure]**, vaya a la sección del informe que desee editar. Seleccione el icono de edición (![Editar icono](/help/assets/icons/edit.png)) junto a **[!UICONTROL Ver informe completo]** para actualizar su configuración.
>![La ficha Medida resalta el icono Editar dentro de una sección del informe.](/help/assets/collaborate/measure/measure-tab-edit-report.png)

El cuadro de diálogo **[!UICONTROL Editar informe de medición]** aparece con la configuración actual del informe en las secciones siguientes:

* [**Detalles de facturación**](#billing-details): Muestra información sobre los créditos al ejecutar informes de medición. No se requiere ninguna configuración.
* [**Detalles de la campaña**](#campaign-details): muestra la configuración del anunciante, el identificador de campaña, el período de informe y un nombre de informe descriptivo.
* [**Detalles del informe**](#report-details): muestra la configuración del tipo de informe, la fecha de ejecución del informe y las opciones de configuración específicas para los informes de atribución.

![Cuadro de diálogo Editar informe de medición que muestra la configuración actual en las secciones Detalles de facturación, Detalles de campaña y Detalles del informe.](/help/assets/collaborate/measure/edit-measurement-report-dialog.png)

### Editar detalles de la campaña {#edit-campaign-details}

En el cuadro de diálogo **[!UICONTROL Editar informe de medición]**, use los menús desplegables **[!UICONTROL ID del anunciante (nombre)]** e **[!UICONTROL ID de campaña]** para editar el anunciante y el ID de campaña de su informe.

![Se abre el cuadro de diálogo Editar informe de medición que resalta el menú desplegable ID de campaña.](/help/assets/collaborate/measure/edit-campaign-id.png)

A continuación, seleccione **[!UICONTROL Intervalo de fechas del informe]** y use el calendario para cambiar las fechas de inicio y finalización del informe.

![Cuadro de diálogo Editar informe de medición que resalta el calendario del intervalo de fechas del informe abierto.](/help/assets/collaborate/measure/edit-report-date-range.png)

Introduzca un nombre de informe descriptivo actualizado para capturar los cambios recientes. Esto le ayudará a reconocer y buscar este informe en el futuro.

![Cuadro de diálogo Editar informe de medición que resalta el nombre descriptivo del informe actualizado.](/help/assets/collaborate/measure/edit-friendly-report-name.png)

### Editar detalles del informe {#edit-report-details}

Para programar el informe para una fecha diferente, vaya a la sección **[!UICONTROL Detalles del informe]**. Seleccione la opción de fecha de ejecución actual y, a continuación, utilice el calendario para elegir la fecha preferida.

![Cuadro de diálogo Editar informe de medición que resalta el calendario de fechas de ejecución del informe.](/help/assets/collaborate/measure/edit-report-run-date.png)

Como anunciante, tiene la opción de seleccionar o quitar el tipo de informe **[!UICONTROL Atribución]**, además de **[!UICONTROL Resumen de campaña]**. Si elige **[!UICONTROL Atribución]**, su informe de atribución incluye métricas de resumen de campaña estándar y perspectivas de atribución detalladas. Para obtener más información sobre los tipos de informe **Resumen de campaña** y **Atribución**, consulte la sección [Crear informe de medición](#create-measurement-report).

>[!IMPORTANT]
>
>Si usted es **publicador**, el tipo de informe predeterminado es **[!UICONTROL Resumen de campaña]** y no se puede cambiar en este momento.

* Si elige **[!UICONTROL Atribución]** como tipo de informe, debe llenar los campos obligatorios en la sección **[!UICONTROL Atribución]**. Para obtener instrucciones de configuración, consulte la sección [detalles del informe de atribución](#report-details-attribution).
* Si ha configurado anteriormente los ajustes de atribución al crear el informe, puede elegir editar la ventana retrospectiva (medida en días) y seleccionar sobre qué eventos de conversión informar.

Para actualizar la ventana retrospectiva **[!UICONTROL en días]**, escriba un valor numérico o ajústelo con las opciones de incremento o disminución. A continuación, seleccione los eventos de conversión sobre los que desee crear un informe. Puede elegir hasta **3** conversiones de la lista disponible.

![Cuadro de diálogo Editar informe de medición que resalta los eventos de conversión actualizados.](/help/assets/collaborate/measure/edit-conversion-events.png)

Una vez que finalice, revisa las actualizaciones y selecciona **[!UICONTROL Editar]** para aplicar los cambios.

![Cuadro de diálogo Editar informe de medición con la opción Editar resaltada.](/help/assets/collaborate/measure/edit-report-confirm.png)

Un cuadro de diálogo de confirmación confirma que el informe se ha guardado correctamente.

## Eliminar informe de medición {#delete-measurement-report}

Al eliminar un informe de medición en Collaboration, se elimina del sistema de forma permanente. Esta acción no se puede deshacer. Para ello, seleccione el informe que desee eliminar en la ficha **[!UICONTROL Measure]**.

En el área de trabajo del informe de medición, seleccione el icono Eliminar (![Icono Eliminar](/help/assets/common/delete.svg)).

![Área de trabajo del informe de medición con el icono Eliminar resaltado.](/help/assets/collaborate/measure/delete-report.png)

Aparecerá el cuadro de diálogo **[!UICONTROL Eliminar informe]**, que le pedirá que confirme la eliminación. Seleccione **[!UICONTROL Eliminar]**.

![Cuadro de diálogo Eliminar informe con la opción Eliminar resaltada.](/help/assets/collaborate/measure/delete-report-confirm.png)

Un cuadro de diálogo de confirmación confirma que el informe se eliminó correctamente.
