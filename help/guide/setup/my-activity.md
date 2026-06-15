---
title: Rastrear la actividad de consumo de crédito
description: Obtenga información sobre cómo ver la cartera de crédito de su organización y rastrear la actividad de consumo de crédito en Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
TQID: https://experienceleague.adobe.com/hDvkKFUCBYvsX8wntcYFrL6qZTxOo5CZOWAbxNwk7mw
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 681f4af47a58a2ce66b25b09d793d0b5b127df39
workflow-type: tm+mt
source-wordcount: 726
ht-degree: 22%

---

# Rastrear la actividad de consumo de crédito {#track-credit-consumption-activity}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_my_activity"
>title="Más información"
>abstract=""

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**Período sin sobrecarga de 90 días**: Los clientes de las regiones elegibles se benefician de un período sin sobrecarga de 90 días a partir de la fecha de disponibilidad en su región. Durante este tiempo, los clientes no incurren en cargos por excedentes por exceder su derecho de crédito.

>[!ENDSHADEBOX]

Para acceder a tu cartera de crédito y a tu actividad de consumo de crédito, ve a **[!UICONTROL Configuración]** en la navegación principal y, a continuación, selecciona la pestaña **[!UICONTROL Mi actividad]**.

![La pestaña Mi actividad muestra la cartera de crédito con los créditos aprovisionados, los créditos consumidos, los créditos disponibles y la tabla de actividad de consumo de crédito.](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>La vista **[!UICONTROL Mi actividad]** no incluye las acciones del usuario desde otras áreas de la interfaz de Real-Time CDP Collaboration. Use la funcionalidad [registros de auditoría](/help/guide/setup/audit-logs.md) para obtener esa información.

## Comprender la vista de Mi actividad {#understand-dashboard}

Usa la vista **[!UICONTROL Mi actividad]** para supervisar el uso de tu crédito y revisar las actividades que consumen créditos. La vista incluye la cartera de crédito y una tabla de actividades.

La Cartera de Crédito muestra los créditos aprovisionados, los créditos consumidos y los créditos disponibles.

| Métrica | Descripción |
|---------|-------------|
| **[!UICONTROL Créditos aprovisionados]** | El número de créditos aprovisionados para su cuenta. |
| **[!UICONTROL Créditos consumidos]** | El número de créditos consumidos por su cuenta en la última actualización diaria. |
| **[!UICONTROL Créditos disponibles]** | El número de créditos disponibles en su cuenta, calculados a partir de los créditos aprovisionados menos los créditos consumidos. |

{style="table-layout:auto"}

En la tabla de actividad se muestran los registros de consumo de crédito diario por fecha, tipo de actividad, entradas procesadas y créditos utilizados:

>[!NOTE]
>
>Las actividades de **[!UICONTROL Gestión de público]** no están asociadas con otro colaborador, por lo que las columnas **[!UICONTROL ID de conexión]** y **[!UICONTROL nombre de conexión]** de estos tipos de actividad muestran un valor de **[!UICONTROL -]**.

| Columna | Descripción |
|------------|--------------|
| **[!UICONTROL Fecha]** | La fecha en la que se produjo la actividad, mostrada en formato MM/DD/AAAA. |
| **[!UICONTROL Id. de conexión]** | Un identificador único para cada conexión asociada con una actividad que consume crédito, representada como una cadena alfanumérica. |
| **[!UICONTROL Nombre de conexión]** | El nombre del colaborador asociado con la conexión y la actividad consumidora de crédito. |
| **[!UICONTROL Actividad]** | El tipo de actividad realizada, como **[!UICONTROL Activación - Acceso de audiencia (una vez)]**, **[!UICONTROL Activación - Acceso de audiencia (recurrente)]**, **[!UICONTROL Activación - Salida de audiencia (una vez)]**, **[!UICONTROL Activación - Salida de audiencia (recurrente)]** o **[!UICONTROL Gestión de audiencia]**. |
| **[!UICONTROL Entradas procesadas]** | Número total de entradas (por ejemplo, ID o filas) procesadas para la actividad. |
| **[!UICONTROL Créditos totales utilizados]** | Créditos totales consumidos por la actividad. |
| **[!UICONTROL Mi cuota de crédito]** | La parte de los créditos utilizados en la actividad de su cuenta. |

{style="table-layout:auto"}

## Tipos de actividades {#types-of-activities}

La columna **[!UICONTROL Actividad]** muestra diferentes tipos de operaciones que consumen crédito.

* **[!UICONTROL Gestión de público]**: Los créditos se consumen cuando las audiencias se obtienen en Collaboration. Los créditos se consumen en función del número de ID indexados dentro de Collaboration en todas las audiencias y de la frecuencia de dicha indexación, como diaria, cada tres días o semanal. Para obtener más información, lea la guía [obtención y administración de audiencias](/help/guide/setup/onboard-audiences.md).
* **[!UICONTROL Activación - Acceso de audiencia (una vez)]**: los créditos se consumen cuando el acceso de audiencia se procesa una vez a través del flujo de trabajo de activación. Para obtener más información, lee la guía [activación de audiencias](/help/guide/collaborate/activate.md).
* **[!UICONTROL Activación - Acceso de audiencia (recurrente)]**: los créditos se consumen cuando el acceso de audiencia se procesa en una programación recurrente a través del flujo de trabajo de activación. Para obtener más información, lee la guía [activación de audiencias](/help/guide/collaborate/activate.md).
* **[!UICONTROL Activación - Salida de audiencia (una vez)]**: los créditos se consumen cuando la salida de audiencia a un destino se procesa una vez a través del flujo de trabajo de activación. Esta actividad se carga al colaborador que recibe la audiencia. Para obtener más información, lee la guía [activación de audiencias](/help/guide/collaborate/activate.md).
* **[!UICONTROL Activación - Salida de audiencia (recurrente)]**: los créditos se consumen cuando la salida de la audiencia a un destino se procesa en una programación recurrente a través del flujo de trabajo de activación. Esta actividad se carga al colaborador que recibe la audiencia. Para obtener más información, lee la guía [activación de audiencias](/help/guide/collaborate/activate.md).
* **[!UICONTROL Medición]**: Los créditos se consumen al generar informes de rendimiento de campañas y perspectivas en Collaboration. Los créditos se consumen en función del número de filas de los informes de campaña de todas las campañas y de la frecuencia de los informes, como diario, cada tres días o semanalmente.

## Administrar el consumo de crédito {#manage-credit-consumption}

Para administrar de forma eficaz el consumo de crédito:

1. **Comprenda** el consumo de crédito asociado con cada actividad. Consulte la [descripción del producto de Collaboration](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} para ver una tabla de créditos usados por actividad.
2. **Monitorizar el uso con regularidad**: revise los créditos disponibles y la tabla de actividades para comprender los patrones de uso en la administración de audiencias, el acceso a audiencias, la salida de audiencias y las actividades de medición.
3. **Rastrear por conexión**: use el nombre de la conexión para identificar qué conexiones consumen la mayor cantidad de créditos.
