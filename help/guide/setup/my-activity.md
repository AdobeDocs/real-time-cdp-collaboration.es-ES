---
title: Rastrear la actividad de consumo de crédito
description: Descubre cómo realizar el seguimiento de la actividad de consumo de crédito de tu organización en Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: 4fc9b4e814f7392e1dfdb5847b7189d7d6e21702
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 7%

---

# Rastrear la actividad de consumo de crédito {#track-credit-consumption-activity}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_my_activity"
>title="Más información"
>abstract=""

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**Período de no sobrecarga de 90 días**: los clientes de las regiones elegibles se benefician de un período de no sobrecarga de 90 días a partir de la fecha de disponibilidad en su región. Durante este tiempo, los clientes no incurren en cargos por excedente por exceder sus derechos de crédito.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>El cuadro de consumo del crédito se redondea al alza y se agrega por días para su seguimiento. Las cifras del panel **[!UICONTROL Mi actividad]** representan un consumo de crédito *estimado*. El *consumo real* de crédito utilizado para la facturación se rastrea en los sistemas internos y está disponible para usted cuando lo solicite. Póngase en contacto con su representante de Adobe para obtener esa información.

Para acceder a tu actividad de consumo de crédito estimada, ve a **[!UICONTROL Configuración]** en la navegación principal y luego selecciona la pestaña **[!UICONTROL Mi actividad]**.

![El panel Mi actividad muestra los detalles de consumo de crédito](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>La vista **[!UICONTROL Mi actividad]** no incluye información sobre las acciones del usuario en diferentes partes de la interfaz de usuario de colaboración. Use la funcionalidad de [registros de auditoría](/help/guide/setup/audit-logs.md) para obtener esa información.

## Comprensión del panel de actividad {#understand-dashboard}

El panel de actividad muestra una lista completa de todas las operaciones que consumen créditos en su cuenta. Cada fila representa una actividad distinta y proporciona información clave sobre el uso del crédito:

>[!NOTE]
>
>Las actividades de **[!UICONTROL Audience Management]** no están asociadas a otro colaborador, por lo que las columnas **[!UICONTROL Connection ID]** y **[!UICONTROL Connection name]** de estos tipos de actividad indican un valor **[!UICONTROL -]**.

| Columna | Descripción |
|------------|--------------|
| **[!UICONTROL Fecha]** | La fecha en que se produjo la actividad, que se muestra en formato MM/DD/AAAA. |
| **[!UICONTROL Id. de conexión]** | Un identificador único para cada conexión asociada a una actividad que consume créditos, representado como una cadena alfanumérica. |
| **[!UICONTROL Nombre de conexión]** | El nombre del colaborador asociado con la conexión y la actividad que consume créditos. |
| **[!UICONTROL Actividad]** | El tipo de actividad realizada, como **Activación - Coincidencia**, **Activación - Salida** o **Administración de audiencia**. |
| **[!UICONTROL Entradas procesadas]** | Número total de entradas (por ejemplo, ID o filas) procesadas para la actividad. |
| **[!UICONTROL Créditos totales utilizados]** | Número total de créditos consumidos por la actividad. |
| **[!UICONTROL Mi cuota de crédito]** | La parte de los créditos utilizados en la actividad de su cuenta. |

{style="table-layout:auto"}

## Tipos de actividades {#types-of-activities}

La columna **[!UICONTROL Actividad]** muestra diferentes tipos de operaciones que consumen crédito.

* **[!UICONTROL Gestión de público]**: Los créditos se consumen cuando las audiencias se obtienen en Collaboration. Los créditos se consumen en función del número de ID (en millones) indexados dentro de Collaboration en todas las audiencias y de la frecuencia de esa indexación (diaria, cada tres días o semanal). Para obtener más información, lea la guía [obtención y administración de audiencias](/help/guide/setup/onboard-audiences.md).
* **[!UICONTROL Activación - Coincidencia]** - Los créditos se consumen como una función del número de ID coincidentes y preparados para la activación. Para obtener más información, lee la guía [activación de audiencias](/help/guide/collaborate/activate.md).
* **[!UICONTROL Activación - Salida]** - Los créditos se consumen como una función del número de ID que se envían a un destino. Esto siempre se carga al colaborador que recibe la audiencia. Para obtener más información, lee la guía [activación de audiencias](/help/guide/collaborate/activate.md).
* **[!UICONTROL Medición]**: ejecute actividades en Collaboration para generar informes y perspectivas de rendimiento de campañas. Los créditos se consumen en función del número de filas de los informes de campaña de todas las campañas y la frecuencia de los informes (diariamente, cada tres días o semanalmente).

## Administrar el consumo de crédito {#manage-credit-consumption}

Para administrar de forma eficaz el consumo de crédito:

1. **Comprenda** el consumo de crédito asociado con cada actividad. Consulte la [descripción del producto de Collaboration](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} para ver una tabla de créditos usados por actividad.
2. **Supervisar con regularidad**: compruebe su panel de actividades con frecuencia para comprender los patrones de uso.
3. **Rastrear por conexión**: use el nombre de la conexión para identificar qué conexiones consumen la mayor cantidad de créditos.
