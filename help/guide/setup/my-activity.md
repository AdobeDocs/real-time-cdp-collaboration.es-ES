---
title: Rastree su actividad de consumo de crédito
description: Obtenga información sobre cómo rastrear la actividad de consumo de crédito de su organización en Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: b52fd181d80d5a70331571f7a4cbe3e5a7ec1d7c
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 1%

---

# Rastree su actividad de consumo de crédito

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**Período sin sobrecarga de 90 días**: Los clientes de las regiones elegibles se benefician de un período sin sobrecarga de 90 días a partir de la fecha de disponibilidad en su región. Durante este tiempo, los clientes no incurren en cargos por excedentes por exceder su derecho de crédito.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>La tabla de consumo de crédito se redondea al alza y se añade por día para su seguimiento. Las cifras del panel **[!UICONTROL Mi actividad]** representan un consumo de crédito *estimado*. El consumo de crédito *actual* que se usa para la facturación se rastrea en sistemas internos y está disponible bajo pedido. Póngase en contacto con su representante de Adobe para obtener esa información.

Para acceder a tu actividad de consumo de crédito estimado, ve a **[!UICONTROL Configuración]** en la navegación principal y luego selecciona la pestaña **[!UICONTROL Mi actividad]**.

![Mi panel de actividades que muestra detalles de consumo de crédito](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>La vista **[!UICONTROL Mi actividad]** no incluye información sobre acciones del usuario en diferentes partes de la interfaz de usuario de Real-Time Collaboration CDP. Use la funcionalidad [registros de auditoría](/help/guide/setup/audit-logs.md) para obtener esa información.

## Comprender el tablero de actividades {#understand-dashboard}

El panel de actividad muestra una lista completa de todas las operaciones de consumo de crédito dentro de la organización. Cada fila representa una actividad distinta y proporciona información clave sobre el uso del crédito:

>[!NOTE]
>
>Las actividades de **[!UICONTROL Gestión de público]** no están asociadas con otro colaborador, por lo que las columnas **[!UICONTROL ID de conexión]** y **[!UICONTROL nombre de conexión]** de estos tipos de actividad indican un valor de **[!UICONTROL N/A]**.

| Columna | Descripción |
|------------|--------------|
| **[!UICONTROL Fecha]** | La fecha en la que se produjo la actividad, mostrada en formato MM/DD/AAAA. |
| **[!UICONTROL Id. de conexión]** | Un identificador único para cada conexión asociada con una actividad que consume crédito, representada como una cadena alfanumérica. |
| **[!UICONTROL Nombre de conexión]** | El nombre del colaborador asociado con la conexión y la actividad consumidora de crédito. |
| **[!UICONTROL Actividad]** | El tipo de actividad realizada, como **Activación - Coincidencia**, **Activación - Salida** o **Gestión de público**. |
| **[!UICONTROL Entradas procesadas]** | Número total de entradas (por ejemplo, ID o filas) procesadas para la actividad. |
| **[!UICONTROL Créditos totales utilizados]** | Número total de créditos consumidos por la actividad. |
| **[!UICONTROL Mi recurso compartido de crédito]** | La parte de los créditos utilizados para la actividad de su organización. |

{style="table-layout:auto"}

## Tipos de actividades {#types-of-activities}

La columna **[!UICONTROL Actividad]** muestra diferentes tipos de operaciones que consumen crédito.

* **[!UICONTROL Administración de audiencias]**: los créditos se consumen cuando las audiencias se obtienen en Real-Time CDP Collaboration. Los créditos se consumen en función del número de ID (en millones) indexados dentro de Real-Time CDP Collaboration en todas las audiencias y de la frecuencia de esa indexación (diaria, cada tres días o semanal). Para obtener más información, lee la guía [importación y administración de audiencias](/help/guide/setup/onboard-audiences.md).
* **[!UICONTROL Activación - Coincidencia]** - Los créditos se consumen como una función del número de identificadores coincidentes y preparados para la activación. Para obtener más información, lee la guía [activación de audiencias](/help/guide/collaborate/activate.md).
* **[!UICONTROL Activación - Salida]** - Los créditos se consumen como una función del número de ID que se envían a un destino. Esto siempre se carga al colaborador que recibe la audiencia. Para obtener más información, lee la guía [activación de audiencias](/help/guide/collaborate/activate.md).
* **[!UICONTROL Medición]**: ejecute actividades en Real-Time CDP Collaboration para generar informes y perspectivas de rendimiento de campañas. Los créditos se consumen en función del número de filas de los informes de campaña de todas las campañas y de la frecuencia de los informes (diariamente, cada tres días o semanalmente).

## Administrar el consumo de crédito {#manage-credit-consumption}

Para administrar de forma eficaz el consumo de crédito:

1. **Comprenda** el consumo de crédito asociado con cada actividad. Consulte la [descripción del producto de Real-Time CDP Collaboration](https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} para ver una tabla de créditos de colaboración usados por actividad.
2. **Supervisar con regularidad**: compruebe su panel de actividades con frecuencia para comprender los patrones de uso.
3. **Rastrear por conexión**: use el nombre de la conexión para identificar qué asociaciones consumen la mayor cantidad de créditos.

<!--

## Pagination and navigation

The activity list is paginated to improve performance and readability. Use the navigation controls at the bottom of the table to move between pages and adjust how many records you can view at once.

-->
