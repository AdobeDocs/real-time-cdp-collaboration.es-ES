---
title: Creación de informes de medición de Amazon Marketing Cloud
description: Obtenga información sobre cómo crear e interpretar informes de medición para campañas de Amazon Marketing Cloud en Real-Time CDP Collaboration.
audience: advertiser
keywords: AMC, Amazon Marketing Cloud, informes de medición, resumen de campaña, atribución, Real-Time CDP Collaboration
solution: Real-Time Customer Data Platform Collaboration
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 944914557c10b43abbe4915e061c219aca9f783f
workflow-type: tm+mt
source-wordcount: '1574'
ht-degree: 6%

---


# Crear [!DNL Amazon Marketing Cloud] informes de medición {#amc-measurement-reports}

{{limited-availability-release-note}}

Use la ficha **[!UICONTROL Medida]** en un proyecto de [!DNL Amazon Marketing Cloud] ([!DNL AMC]) para revisar el alcance de audiencia, la frecuencia y los resultados de conversión. Después de crear un proyecto AMC, cree informes de medición para las campañas que ya se han ejecutado con los datos disponibles en su instancia de [!DNL AMC].

>[!IMPORTANT]
>
>La pestaña **[!UICONTROL Measure]** muestra &quot;No hay datos de medición disponibles&quot; hasta que se completen las consultas de configuración de datos en segundo plano. Este proceso puede tardar hasta 24 horas. Si el mensaje persiste pasadas 24 horas, consulte la sección [Solución de problemas](#troubleshooting).


## Creación de un informe {#create-report}

Para crear un informe de medición de [!DNL AMC], siga los pasos de [Crear informe de resumen de campaña](../measure.md#create-campaign-summary-report-create-campaign-summary-report).

![Formulario del informe de medición que muestra los campos ID del anunciante, ID de campaña desplegable, Intervalo de fechas del informe, Fecha de ejecución del informe, Nombre del informe y Tipo de informe.](../../../assets/collaborate/advertising-platforms/create-measurement-report.png){zoomable="yes"}

### Detalles de la campaña {#campaign}

El **[!UICONTROL ID del anunciante]** identifica la cuenta [!DNL Amazon Advertising] asociada con la instancia [!DNL AMC]. [!DNL AMC] utiliza este contexto de cuenta para recuperar campañas de medición.

La lista **[!UICONTROL Campaign ID]** se rellena automáticamente con las campañas disponibles en la instancia [!DNL AMC] conectada. Una campaña solo aparece si se encuentra dentro de la ventana retrospectiva de detección predeterminada y tiene suficientes usuarios únicos para satisfacer el umbral mínimo de agregación de [!DNL AMC]. Seleccione la campaña cuya actividad [!DNL Amazon Ads] desee medir.

Si la campaña que necesita no aparece en la lista, compruebe que pertenece a la cuenta conectada de [!DNL Amazon Ads] y revise [Solución de problemas](#troubleshooting). Para obtener más información sobre el umbral, consulte la [documentación sobre el umbral de agregación AMC](https://advertising.amazon.com/API/docs/en-us/guides/amazon-marketing-cloud/aggregation-threshold).

#### Intervalo de fechas, fecha de ejecución y nombre del informe {#dates}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_report_date_range"
>title="Intervalo de fecha"
>abstract="Establezca las fechas de inicio y finalización de los datos de campaña para incluirlos en el informe. El intervalo de fechas está limitado a una ventana retrospectiva de 365 días con un intervalo máximo de 90 días. Solo puede informar sobre campañas anteriores."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_report_run_date"
>title="Fecha de ejecución"
>abstract="Fecha en la que se ejecuta el informe. Debe ser al menos un día después de la fecha de finalización del informe y puede tardar hasta 46 días en el futuro."

>[!NOTE]
>
>Solo puede informar sobre campañas que ya se hayan ejecutado.

Establezca el **[!UICONTROL intervalo de fechas del informe]** en el período en el que se ejecutó la campaña [!DNL AMC] seleccionada. [!DNL AMC] admite una ventana retrospectiva de 365 días con un lapso máximo de 90 días.

Establezca **[!UICONTROL Fecha de ejecución del informe]**. Es la fecha en la que se ejecuta el informe. La fecha de ejecución debe ser al menos un día después de la fecha de finalización del informe y puede ser hasta 46 días en el futuro. Para obtener el conjunto completo de restricciones de fecha, vea [AMC constraint reference](#constraints).

>[!TIP]
>
>En el caso de los informes de atribución en los que el intervalo de fechas se encuentra dentro de los 30 días de la fecha actual, establezca la fecha de ejecución 30 días en el futuro para garantizar que todas las conversiones dentro de la ventana retrospectiva fija de 30 días se hayan capturado antes de que se ejecute el informe.

#### Tipo de informe {#report-type}

Todos los informes de [!DNL AMC] incluyen **[!UICONTROL Resumen de campaña]**. Opcionalmente, puede incluir datos de **[!UICONTROL Atribución]** para medir si las impresiones de campaña tuvieron como resultado acciones del cliente, como compras o registros, en un período de 30 días después de la exposición del anuncio. La atribución requiere que los eventos de conversión relevantes estén disponibles en la instancia [!DNL AMC]. Para las campañas centradas en el alcance o la concienciación, **[!UICONTROL Campaign summary]** proporciona las métricas de entrega que necesita.

| Tipo de informe | Descripción |
| --- | --- |
| **[!UICONTROL Resumen de campaña]** | Proporciona métricas de alcance, frecuencia e impresión para la campaña seleccionada. Siempre incluido. |
| **[!UICONTROL Atribución]** | Agrega datos de conversión al informe. Solo está disponible si existen eventos de conversión en su instancia de [!DNL AMC]. Consulte [Eventos de conversión](#conversion-events). |

#### Eventos de conversión (solo atribución) {#conversion-events}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_attribution_lookback_period"
>title="Período retrospectivo de atribución"
>abstract="AMC aplica un período fijo de atribución de 30 días: las conversiones que se producen hasta 30 días después de la última impresión pueden atribuirse a impresiones dentro del intervalo de fechas del informe. Este valor no se puede editar; programe la fecha de ejecución del informe al menos 30 días después del final del intervalo para garantizar que se capturan todas las conversiones aptas."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_conversion_events"
>title="Eventos de conversión"
>abstract="Seleccione hasta tres eventos de conversión para incluirlos en el informe de atribución. Los eventos disponibles se detectan automáticamente desde la instancia de [!DNL AMC]. Si no aparece ningún evento, es posible que la instancia de [!DNL AMC] no tenga ningún evento de conversión registrado y la atribución no estará disponible."

>[!NOTE]
>
>Los datos de atribución requieren que se configuren eventos de conversión en la instancia [!DNL AMC]. Si [!UICONTROL Atribución] no está disponible o no se seleccionó, omita esta sección y seleccione **[!UICONTROL Crear]** para enviar el formulario.

Para los informes de [!UICONTROL Attribution], [!DNL AMC] aplica una ventana retrospectiva de atribución de 30 días fija. Esta configuración no se puede ajustar.

![La sección Eventos de conversión del formulario de informe de medición está en estado activo y muestra el campo de ventana retrospectiva establecido en 30 días y la lista de selección múltiple Eventos de conversión con eventos disponibles.](../../../assets/collaborate/advertising-platforms/conversion-events-active.png){zoomable="yes"}

Los eventos de conversión representan acciones de clientes in situ rastreadas por [!DNL Amazon Ads], como una compra, la adición a una lista de deseos, la acción del carro de compras o la vista de detalles del producto. Los informes de atribución admiten hasta tres eventos. Seleccione los eventos que se alinean con los resultados de la campaña que desea medir. Si la opción [!UICONTROL Atribución] no está disponible, consulte [Solución de problemas](#troubleshooting).

Después de crear el informe, aparece en la ficha **[!UICONTROL Measure]** con un estado programado o pendiente. En la fecha de ejecución configurada, [!DNL AMC] procesa la consulta del informe y devuelve los resultados en un plazo de 24 horas.

![La pestaña Medida muestra una tarjeta de informe de medición recién creada con un indicador de estado programado, el nombre del informe, la fecha de ejecución y el tipo de informe visibles.](../../../assets/collaborate/advertising-platforms/measurement-report-pending.png){zoomable="yes"}


## Ver un informe {#view-report}

Una vez que se ha ejecutado un informe, los resultados están disponibles en la ficha **[!UICONTROL Measure]** del proyecto [!DNL AMC]. Busque el informe y seleccione **[!UICONTROL Ver informe completo]** para revisar los resultados.

![La ficha Medida de un proyecto [!DNL AMC] muestra una tarjeta de informe completada con la fecha de ejecución, el tipo de informe y el botón Ver informe completo resaltado.](../../../assets/collaborate/advertising-platforms/view-full-report.png){zoomable="yes"}

El informe muestra los resultados disponibles para el tipo de informe seleccionado. Los informes **[!UICONTROL Resumen de campaña]** muestran los resultados de la entrega de la campaña de Amazon seleccionada.

![Visualizaciones de resumen de campaña que muestran totales de resumen, distribución de impresiones, distribución de frecuencia, curva de alcance e impresiones por ubicación.](../../../assets/collaborate/advertising-platforms/campaign-summary-widgets.png){zoomable="yes"}

Los informes que incluyen **[!UICONTROL Atribución]** también muestran la actividad de conversión asociada con los eventos de conversión de Amazon Ads seleccionados.


![Las visualizaciones de atribución que muestran conversiones acumulativas y gráficos de conversiones por día.](../../../assets/collaborate/advertising-platforms/attribution-report-conversion-widgets.png){zoomable="yes"}

Para obtener más información sobre cómo interpretar los resultados del informe, vea [Medir el rendimiento](../measure.md#view-reports-view-reports).

## [!DNL AMC] restricciones de referencia {#constraints}

Las siguientes restricciones se aplican a todos los [!DNL AMC] informes de medición.

| Restricción | Valor |
| --- | --- |
| Inicio del intervalo de fechas del informe más temprano | 365 días antes de la fecha actual |
| Fin del último intervalo de fechas del informe | 45 días después de la fecha actual. Utilícelo para preconfigurar un informe para una campaña que aún se está ejecutando y que finalizará en los próximos 45 días; el informe se ejecuta automáticamente en la fecha de ejecución programada después de que finalice la campaña. |
| Intervalo máximo de fechas del informe | 90 días |
| Ventana retrospectiva de atribución | 30 días (fijos para [!DNL AMC]) |
| Fecha de ejecución mínima | Al menos 1 día después de la fecha de finalización del informe |
| Fecha de ejecución máxima | 46 días en el futuro |
| Número máximo de eventos de conversión por informe | 3 |
| Selección de campaña | Campaña única por informe |
| Edición de informes | No disponible. Se conserva el informe existente. [Crear un nuevo informe](#create-report) cuando se requieran cambios |

## Resolución de problemas {#troubleshooting}

**No hay datos de medición disponibles**

La pestaña **[!UICONTROL Measure]** muestra &quot;No hay datos de medición disponibles&quot; hasta que se hayan completado las consultas de configuración de datos en segundo plano activadas al crear el proyecto. Esto puede tardar hasta 24 horas. Si el mensaje &quot;No hay datos de medición disponibles&quot; persiste después de 24 horas, compruebe que la instancia de [!DNL AMC] tenga campañas que se hayan ejecutado en los últimos tres meses, ya que esta es la ventana retrospectiva predeterminada que se utiliza durante la detección de campañas. Si existen campañas aptas y el mensaje persiste, comprueba el estado de la campaña en tu [cuenta de Amazon Ads](https://advertising.amazon.com/sign-in){target="_blank"}.

**No aparecen campañas en la lista desplegable [!UICONTROL ID de campaña]**

Las campañas pueden estar ausentes incluso cuando la pestaña **[!UICONTROL Measure]** esté visible. [!DNL AMC] aplica un umbral mínimo de usuario a los datos de campaña. Las campañas que no alcanzan el umbral de usuarios únicos mínimos se excluyen y las consultas de informes no arrojarán resultados. Compruebe que las campañas de las que desea informar tienen suficiente alcance. Para obtener detalles sobre los umbrales de agregación de [!DNL AMC], consulte la [documentación sobre el umbral de agregación AMC](https://advertising.amazon.com/API/docs/en-us/guides/amazon-marketing-cloud/aggregation-threshold){target="_blank"}.

**Los resultados no son visibles después de la fecha de ejecución**

Espere hasta 24 horas después de la fecha programada de ejecución de [!DNL AMC] para procesar las consultas del informe y devolver los resultados. Si el informe permanece pendiente después de ese período, compruebe que la fecha de ejecución haya pasado y que el estado del informe ya no aparezca como pendiente.

**Los eventos de conversión no están disponibles y [!UICONTROL La atribución] está atenuada**

Esto puede ocurrir por tres razones:

1. **El seguimiento de conversión no está habilitado.** Es posible que la cuenta del anunciante [!DNL AMC] no tenga configurado el seguimiento de conversiones. Vaya a su [cuenta de Amazon Ads](https://advertising.amazon.com/sign-in){target="_blank"} y compruebe que se está realizando un seguimiento de los eventos de conversión de las campañas relevantes.
2. **No se registraron eventos de conversión.** Incluso con el seguimiento habilitado, es posible que la instancia de [!DNL AMC] aún no haya registrado ningún evento de conversión.
3. **Umbral de agregación no alcanzado.** [!DNL AMC] aplica un umbral mínimo a los datos de conversión. Si un tipo de evento de conversión no tiene un número suficiente de ocurrencias, no se devolverá y no aparecerá en la lista.

**Las conversiones aparecen por debajo de lo esperado**

Si la fecha de ejecución del informe es anterior en menos de 30 días al final del intervalo de fechas, es posible que [!DNL AMC] no haya capturado todas las conversiones dentro de la ventana de atribución. [Cree un nuevo informe](#create-report) con una fecha de ejecución al menos 30 días después de que finalice el intervalo de fechas.

## Próximos pasos {#next-steps}

Use los resultados del informe para evaluar el rendimiento de la campaña e informar la planificación de campañas futuras en [!DNL Amazon Advertising]. Por ejemplo, puede ajustar la segmentación, suprimir las audiencias sobreexpuestas identificadas en la distribución de frecuencias o reasignar el gasto a ubicaciones de alto rendimiento. Para analizar una campaña o un período de informe diferente, cree otro informe de medición con la configuración adecuada.

Para obtener una descripción general de todas las capacidades de colaboración de [!DNL AMC] disponibles, consulte [[!DNL Amazon Marketing Cloud]](./amc.md).
