---
title: Rastree su actividad de consumo de crédito
description: Obtenga información sobre cómo rastrear la actividad de consumo de crédito de su organización en Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: 1e8c2fdb3294111562f206ac141cfa39d5193c6c
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 1%

---

# Rastree su actividad de consumo de crédito

{{limited-availability-release-note}}

Use la pestaña **[!UICONTROL Mi actividad]** para monitorizar y rastrear el consumo de crédito estimado de su organización en todas las actividades de colaboración. Esta función proporciona información detallada sobre cómo se utilizan los créditos en diferentes conexiones y actividades, lo que le ayuda a administrar sus recursos de forma eficaz.

>[!IMPORTANT]
>
>La tabla de consumo de crédito se redondea al alza y se añade por día para su seguimiento. Las cifras del panel **[!UICONTROL Mi actividad]** representan un consumo de crédito *estimado*. El consumo de crédito *actual* que se usa para la facturación se rastrea en sistemas internos y está disponible bajo pedido. Póngase en contacto con su representante de Adobe para obtener esa información.

Para acceder a tu actividad de consumo de crédito estimado, ve a **[!UICONTROL Configuración]** en la navegación principal y luego selecciona la pestaña **[!UICONTROL Mi actividad]**.

![Mi panel de actividades que muestra detalles de consumo de crédito](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>La vista **[!UICONTROL Mi actividad]** no incluye información sobre acciones del usuario en diferentes partes de la interfaz de usuario de Real-Time Collaboration CDP. Use la funcionalidad [registros de auditoría](/help/guide/setup/audit-logs.md) para obtener esa información.

## Comprender el tablero de actividades

El panel de actividad muestra una lista completa de todas las operaciones de consumo de crédito dentro de la organización. Cada fila representa una actividad distinta y proporciona información clave sobre el uso del crédito:

>[!NOTE]
>
>Las actividades de **[!UICONTROL Gestión de público]** no están asociadas con otro colaborador, por lo que las columnas **[!UICONTROL ID de conexión]** y **[!UICONTROL nombre de conexión]** de estos tipos de actividad indican un valor de **[!UICONTROL N/A]**.

| Columna | Descripción |
|--------|-------------|
| **[!UICONTROL Fecha]** | La fecha en la que se produjo la actividad, mostrada en formato MM/DD/AAAA. |
| **[!UICONTROL Id. de conexión]** | Un identificador único para cada conexión asociada con una actividad que consume crédito, representada como una cadena alfanumérica. |
| **[!UICONTROL Nombre de conexión]** | El nombre del colaborador asociado con la conexión y la actividad consumidora de crédito. |
| **[!UICONTROL Actividad]** | El tipo de actividad realizada, como **Activación - Uso compartido**, **Activación - Salida** o **Gestión de público**. |
| **[!UICONTROL Créditos totales utilizados]** | Número total de créditos consumidos por la actividad. |
| **[!UICONTROL Mi recurso compartido de crédito]** | La parte de los créditos utilizados para la actividad de su organización. |

{style="table-layout:auto"}

## Tipos de actividades {#types-of-activities}

La columna **[!UICONTROL Actividad]** muestra diferentes tipos de operaciones que consumen crédito.

* **[!UICONTROL Administración de audiencias]**: los créditos se consumen cuando las audiencias se importan en Real-Time CDP Collaboration. Los créditos se consumen en función del número de ID (en millones) indexados dentro de Real-Time CDP Collaboration en todas las audiencias y de la frecuencia de esa indexación (diaria, cada tres días o semanalmente) durante todo el periodo de facturación. Más información sobre [importación y administración de audiencias](/help/guide/setup/onboard-audiences.md).
* **[!UICONTROL Activación - Uso compartido]**: los créditos se consumen como una función del número de ID activados desde Real-Time CDP Collaboration durante el período de facturación. Obtenga más información sobre [compartir](/help/guide/collaborate/share.md) y [activar audiencias](/help/guide/collaborate/activate.md) en Real-Time CDP Collaboration.
* **[!UICONTROL Activación - Salida]** - Los créditos se consumen como una función del número de ID activados desde Real-Time CDP Collaboration durante el período de facturación. Obtenga más información sobre [compartir](/help/guide/collaborate/share.md) y [activar audiencias](/help/guide/collaborate/activate.md) en Real-Time CDP Collaboration.


<!--

**[!UICONTROL Audience Overlaps]** – Credits are consumed as a function of the number of matched IDs across 2 or more shared audiences throughout the billing period. Read more about [audience overlaps in the discover tab](/help/guide/collaborate/discover.md).

Collaboration Measurement – Credits are consumed as a function of the number of rows existing in campaign reports across all campaigns, and the frequency of that reporting (daily, every three days, or weekly).

-->


## Administrar el consumo de crédito {#manage-credit-consumption}

Para administrar de forma eficaz el consumo de crédito:

1. **Comprenda** el consumo de crédito asociado con cada actividad. Consulte la [descripción del producto de Real-Time CDP Collaboration](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} para ver una tabla de créditos de colaboración usados por actividad.
2. **Supervisar con regularidad**: compruebe su panel de actividades con frecuencia para comprender los patrones de uso.
3. **Rastrear por conexión**: use el nombre de la conexión para identificar qué asociaciones consumen la mayor cantidad de créditos.

<!--

## Pagination and navigation

The activity list is paginated to improve performance and readability. Use the navigation controls at the bottom of the table to move between pages and adjust how many records you can view at once.

-->
