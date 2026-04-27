---
title: Rendimiento de medida
description: Mida el rendimiento de las campañas en diferentes canales. Aprenda a utilizar e interpretar varios informes.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
TQID: https://experienceleague.adobe.com/pr-qF4sd-NHd55kxh1dCstHRnVCUEhIvtv-47-ljiu4
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 2612
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
**[!UICONTROL Total average frequency]**: The number of impressions divided by unique identities reached. This figure indicates how often every identity was displayed the creative.

![Campaign summary view](/help/assets/collaborate/measure/campaign-summary.png)

### Métricas a lo largo del tiempo {#metrics-over-time}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measure_metricsovertime"
>title="Métricas a lo largo del tiempo"
>abstract="Utilice la vista de métricas a lo largo del tiempo para comprender la cantidad total de impresiones que se muestran para su creativo durante el periodo de la campaña. Puede seleccionar un máximo de dos dimensiones para mostrarlas en el informe."

Utilice la vista de métricas a lo largo del tiempo para comprender la cantidad total de impresiones que se muestran para su creativo durante el periodo de la campaña. Note that you can select a maximum of two metrics to display and analyze in the report.

![Metrics over time view.](/help/assets/collaborate/measure/metrics-over-time.png)

### Distribución de frecuencia {#frequency-distribution}

Use the frequency distribution view to understand the breakdown of how many impressions were shown to each unique user. This view can help you in future campaigns to decide as of which point you want to start suppressing audiences. For example, you may want to suppress profiles who have already seen a creative three times.

![Frequency distribution view.](/help/assets/collaborate/measure/frequency-distribution.gif)

### Métrica por dimensión {#metric-by-dimension}

Analyze different metrics like impressions, viewable impressions, unique reach, cost, and more in the context of the placement medium. Analyze which medium (for example mobile streaming, CTV programmatic, or others) are driving the best results for your campaigns.

![Metric by dimension.](/help/assets/collaborate/measure/metric-by-dimension.png)

### Curva de alcance acumulativo {#cumulative-reach-curve}

As the campaign progressed and the number of impressions went up, understand whether the number of users that you were able to reach has also grown. A common pattern in campaigns is that after a certain point a plateau is reached where the creative is displayed to the same people over and over again. This view can help you adjust the length of future campaigns, depending on the moment that new people were not being reached anymore.

![Cumulative reach curve.](/help/assets/collaborate/measure/cumulative-reach-curve.png)

### Impresiones por ubicación {#impressions-by-placement}

Understand which medium is driving impressions for your creative. This can help you decide where to invest your ad spend in future campaigns.

![Impressions by placement.](/help/assets/collaborate/measure/impressions-by-placement.png)

### Conversiones acumuladas {#cumulative-conversions}

This view provides a detailed breakdown of the conversion events you choose to measure in a tabular format. The table includes:

* **Conversion event**: Name of each conversion event you are tracking.
* **Conversion count**: Total count of conversions that occurred for each event.
* **Estimated revenue**: Estimated value attributed to each conversion event.

Review this table to evaluate the effectiveness of your campaign in driving the desired actions.

![Cumulative conversions.](/help/assets/collaborate/measure/cumulative-conversions.png)

### Conversiones por día {#conversions-by-day}

This chart provides a day-by-day breakdown of conversions for each event set up when you create an Attribution report. Use this view to uncover daily patterns, identify periods of high or low conversion activity, and compare how different conversion events perform across your campaign timeline.

![Conversions by day.](/help/assets/collaborate/measure/conversions-by-day.gif)

## Crear informe de medición {#create-measurement-report}

In Collaboration, you can create two main types of measurement reports:

* **Campaign Summary**: Provides high-level metrics such as reach, impressions, average frequency, and delivery by channel, giving a quick overview of overall campaign performance.
* **Attribution**: Measures how campaign exposures drive downstream actions like conversions or purchases, helping you understand campaign effectiveness.

You can run Campaign Summary report on its own, while Attribution report requires both report types to be selected together.

### Create campaign summary report {#create-campaign-summary-report}

Both publishers and advertisers can generate **Campaign Summary** reports to evaluate campaign performance. Use these reports to gain insights into key metrics such as [reach](#cumulative-reach-curve), [frequency](#frequency-distribution), and [impressions](#impressions-by-placement), and understand how your campaign was delivered and its overall impact.

To generate a **Campaign Summary** report, navigate to the project workspace from the **[!UICONTROL Collaborator]** workspace. From the **[!UICONTROL Measure]** tab, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Measure]**.

If this is your first report, you may also select the **[!UICONTROL Run report]** option.

![The Measure tab highlighting the Run report option and the Measure option.](/help/assets/collaborate/measure/run-measure-report.png)

The **[!UICONTROL Create measurement report]** screen appears with information and input fields grouped under **[!UICONTROL Billing details]**, **[!UICONTROL Campaign details]**, and **[!UICONTROL Report details]** sections.

#### Detalles de facturación {#billing-details}

This section explains how credits are used when generating measurement reports. Credit responsibility is established during [connection setup](../connect/establishing-connections.md#credit-split). Before running any reports, make sure to review and confirm the credit split settings and reporting roles with your collaborator.

#### Detalles de la campaña {#campaign-details}

In the **[!UICONTROL Campaign details]** section, select the appropriate **Advertiser ID** to associate with your report. These advertiser names or IDs were added during [connection setup](../connect/establishing-connections.md#advertiser-names). If only one name was configured, it appears by default. If no name was set up, the **[!UICONTROL Advertiser ID (Name)]** field is disabled and prefilled with the advertiser account name.

![The Create measurement report screen showing the Advertiser ID (Name) option disabled.](/help/assets/collaborate/measure/advertiser-id.png)

Then, select the desired campaign from the **[!UICONTROL Campaign ID]** dropdown menu. This menu lists all campaign IDs entered by the publisher for your project. If the campaign you need isn&#39;t available, [add it in the UI](./manage-projects.md#manage-campaign-id) before generating the report.

![The Create measurement report screen showing the Campaign ID dropdown menu expanded.](/help/assets/collaborate/measure/campaign-id.png)

Next, specify the period you want the report to cover. Select **[!UICONTROL Report date range]**, then use the calendar to choose the start and end dates.

![The Create measurement report screen showing the Report date range calendar.](/help/assets/collaborate/measure/report-date-range.png)

#### Detalles del informe {#report-details}

**Report run date**

In the **[!UICONTROL Report details]** section, choose the date on which the report should run. Select **[!UICONTROL Report run date]** and choose your preferred date from the calendar.

* If you choose today&#39;s date or a date in the past, the **Campaign Summary** report runs right away.
* If you choose a future date, the **Campaign Summary** report is scheduled to run on that day.

![The Create measurement report screen showing the Report run date calendar.](/help/assets/collaborate/measure/report-run-date.png)

**Report type**

* If you&#39;re an advertiser, you can select the **[!UICONTROL Campaign summary]** report type from the available options. Only advertisers can generate attribution reports.
* If you&#39;re a publisher, the **[!UICONTROL Campaign summary]** report type is preselected and cannot be changed. At this time, publishers cannot run attribution reports.

![The Create measurement report screen showing the Campaign summary option as a preselected and unchangable report type.](/help/assets/collaborate/measure/cs-report-type.png)

Finally, review your settings and select **[!UICONTROL Create]**. Your campaign summary report generates immediately if the run date is today or earlier, or on the chosen future date. You can edit the scheduled report before its run date. For step-by-step instructions, refer to the [Edit measurement report] section.

Once available, you can view your report at any time in the **[!UICONTROL Measure]** tab within your project workspace.

![The Create measurement report screen showing the information and the Create option highlighted.](/help/assets/collaborate/measure/cs-review.png)

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

* **Lookback window in days**: Defines how far back the report considers campaign impressions before each conversion. Only impressions within this period are eligible for attribution credit.
* **Conversion events**: Specifies which conversion actions you want to measure, for example, purchases or sign-ups. These events must be set up in advance when you [source your measurement data](../setup/onboard-measurement-data.md#add-conversion-event) into Collaboration.

First, enter a value for the **[!UICONTROL Lookback window in days]** field, or adjust it with the increment/decrement options.

![The Create measurement report screen highlighting the value for Lookback window in days.](/help/assets/collaborate/measure/lookback-window-in-days.png)

Next, choose up to **3** conversion events from the available list. For more information about a particular event, select the **[!UICONTROL i]** icon to view its details.

![The Create measurement report screen highlighting the selected conversion events and the information of the Purchase event.](/help/assets/collaborate/measure/attribution-conversion-events.png)

Finally, review your settings and select **[!UICONTROL Create]** to schedule the report. Your attribution report will be generated on the specified run date. You can edit the scheduled report before its run date. For step-by-step instructions, refer to the [Edit measurement report] section.

Once available, you can view your report at any time in the **[!UICONTROL Measure]** tab within your project workspace.

![The Create measurement report screen showing the information and the Create option highlighted.](/help/assets/collaborate/measure/attribution-review.png)

## Editar informe de medición {#edit-measurement-report}

>[!IMPORTANT]
>
>You can edit the settings of a measurement report only if it is scheduled to run in the future. For reports that have already been executed, settings cannot be changed.

Update a measurement report settings to ensure the report provides the correct analysis of your campaign within a specific period and runs on a desired date.

To begin, navigate to the workspace of the measurement report you want to update. Select the edit icon (![Edit icon](/help/assets/icons/edit.png)) next to the delete icon.

![The measurement report workspace with the Edit icon highlighted.](/help/assets/collaborate/measure/edit-report.png)

>[!TIP]
>
>In the **[!UICONTROL Measure]** tab, navigate to the report section you wish to edit. Select the edit icon (![Edit icon](/help/assets/icons/edit.png)) next to **[!UICONTROL View full report]** to update its settings.
>![The Measure tab highlighting the Edit icon within a report section.](/help/assets/collaborate/measure/measure-tab-edit-report.png)

The **[!UICONTROL Edit measurement report]** dialog appears with the current settings of the report in the following sections:

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
