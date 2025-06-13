---
title: Rendimiento de medida
description: Mida el rendimiento de las campañas en diferentes canales. Aprenda a utilizar e interpretar varios informes.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
source-git-commit: b52fd181d80d5a70331571f7a4cbe3e5a7ec1d7c
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 18%

---

# Rendimiento de medida

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>El área de trabajo **[!UICONTROL Measure]** solo está disponible si el caso de uso **Measurement** se habilitó [durante el proceso de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./manage-projects.md#project-use-cases).

Obtenga información sobre los informes disponibles en Real-Time CDP Collaboration y comprenda cómo medir y analizar el rendimiento de sus campañas de marketing en varios canales.

## Requisitos previos

Antes de poder acceder a los informes de medición en Real-Time CDP Collaboration, ya ha hecho lo siguiente:

* [Se conectó](/help/guide/connect/establishing-connections.md) con un anunciante o editor deseado con el caso de uso de **Medición** habilitado y comenzó a colaborar en [proyectos](/help/guide/collaborate/manage-projects.md)
* Ejecute una campaña y [cargó datos de medición](/help/guide/setup/onboard-measurement-data.md) en Real-Time CDP Collaboration.

<!--

## Create a report {#create-report}

Hidden until functionality is live. At that point, move the contextualhelp from below into this section. 

The syntax rtcdp_collaboration_measurement_create_report is currently implemented in the UI. However, a preference would be to imlement the other contextualhelp ID from below instead, since that explicitly includes campaignID in the syntax. Need to sync up with UI team. More details in CORE-116991.

-->

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

## Pasos siguientes

![Detectar, activar y medir anunciantes.](/help/assets/end-to-end-workflow/discover-activate-measure.png)

En el espíritu de la ciclicidad de la imagen anterior, use las perspectivas que obtuvo al ver los informes para planificar su próxima campaña. Como anunciante, si es necesario, vuelva para descubrir diferentes editores y ejecute superposiciones para descubrir diferentes audiencias para sus próximas campañas.
