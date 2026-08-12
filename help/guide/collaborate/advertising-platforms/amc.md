---
title: Amazon Marketing Cloud
description: Obtenga información acerca de la colaboración con Amazon Marketing Cloud en Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 1a1b8fec-384b-465f-832d-0772c518fdf1
TQID: https://experienceleague.adobe.com/jNTQWEaUuuvgqKboJWsUH4XoKStP49nB0GLUSze0eXw
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: b29c92fa411198ec4e9a0a493c91ee302a327697
workflow-type: tm+mt
source-wordcount: 699
ht-degree: 11%

---

# Amazon Marketing Cloud

{{limited-availability-release-note}}

Después de establecer una conexión con [!DNL Amazon Marketing Cloud] ([!DNL AMC]), los anunciantes pueden [crear un proyecto](../manage-projects.md#create-project) para colaborar con [!DNL AMC]. Se admiten dos casos de uso en un proyecto [!DNL AMC]: **Detección de audiencias** con la sección **[!UICONTROL Discover]** y **Medición** con la ficha **[!UICONTROL Medida]**.

## Descubrir {#discover}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="Comparar públicos"
>abstract="Compare su público con todos los consumidores a los que llegan sus anuncios de Amazon."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="Públicos relevantes"
>abstract="Segmentos a los que se dirige Amazon en los que su público tiene el mayor solapamiento teniendo en cuenta solo las impresiones de DSP (estos segmentos solo se pueden dirigir en DSP)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="ID resueltos"
>abstract="El número de ID que la resolución de identidad de Amazon pudo resolver con sus datos de audiencia."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="ID expuestos a anuncios solapados"
>abstract="Representa el número de &quot;ID resueltos&quot; de la audiencia cargada que también se han expuesto a un anuncio a través de Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="% de solapamiento"
>abstract="La proporción de &quot;ID resueltos&quot; que se han expuesto a un anuncio a través de Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Desglose por producto publicitario de Amazon"
>abstract="Desglose de &quot;ID superpuestos y expuestos&quot; alcanzados por el producto patrocinado por Amazon Ads o por Amazon Ads DSP."

En la sección **[!UICONTROL Discover]**, puedes comparar tu audiencia AMC con todos los consumidores a los que han llegado tus Amazon Ads. También puede ver los segmentos de segmentación de Amazon con los que la audiencia tiene la mayor superposición, teniendo en cuenta solo las impresiones de DSP (estos segmentos solo pueden segmentarse en DSP).

>[!IMPORTANT]
>
>Los datos de audiencias se procesan a partir de las audiencias cargadas en su cuenta de [!DNL Amazon Ads]. Para obtener información sobre cómo enviar y usar la función Destinos de Experience Platform para enviar tus audiencias a tu cuenta de [!DNL Amazon Ads], lee la guía de conexión de [Amazon Ads](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/catalog/advertising/amazon-ads).

![Sección Discover en un proyecto con Amazon Marketing Cloud.](/help/assets/collaborate/advertising-platforms/amc-discover.png){zoomable="yes"}

### Comparar públicos {#compare-audiences}

La sección **[!UICONTROL Comparar audiencias]** proporciona información sobre cómo la audiencia de [!DNL AMC] se superpone con los consumidores a los que llegan los anuncios de Amazon. En la sección **[!UICONTROL Comparar audiencias]**, puede ver las siguientes métricas:

| Métrica | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID resueltos] | El número de identificadores [!DNL Amazon's Identity Resolution] se pudo resolver con sus datos de audiencia. |
| [!UICONTROL ID expuestos y superpuestos] | El número de [!UICONTROL ID resueltos] de la audiencia cargada que también se expusieron a un anuncio a través de [!DNL Amazon Ads]. |
| [!UICONTROL Superposición %] | La proporción de [!UICONTROL ID resueltos] que se han expuesto a un anuncio a través de [!DNL Amazon Ads]. |
| [!UICONTROL Desglose por producto de anuncios de Amazon] | Desglose de [!UICONTROL ID superpuestos y expuestos] alcanzados por [!UICONTROL producto patrocinado] o [!UICONTROL DSP]. Cada uno se representa como un porcentaje individual del número total de ID expuestos a publicidad. Dado que un ID puede pertenecer tanto a [!UICONTROL Productos patrocinados] como a [!UICONTROL DSP], es posible que los porcentajes no sumen el 100%. |


### Públicos relevantes {#relevant-audiences}

La sección **[!UICONTROL Audiencias relevantes]** proporciona información sobre [!DNL Amazon] segmentos de segmentación, o audiencias, con las que la audiencia tiene la mayor superposición, teniendo en cuenta solo las impresiones de DSP (estos segmentos solo se pueden segmentar en DSP). Puede alternar entre todas las audiencias relevantes y, dentro de cada sección, puede ver las siguientes métricas:

| Métrica | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID resueltos] | El número de identificadores [!DNL Amazon's Identity Resolution] se pudo resolver con sus datos de audiencia. |
| [!UICONTROL ID expuestos y superpuestos] | Representa el número de [!UICONTROL ID resueltos] de la audiencia cargada que también se expusieron a un anuncio a través de [!DNL Amazon Ads]. Esto solo tiene en cuenta las impresiones de DSP. |
| [!UICONTROL Superposición %] | La proporción de [!UICONTROL ID resueltos] que se han expuesto a un anuncio a través de [!DNL Amazon Ads]. |
| [!UICONTROL Categorías] | La categoría o categorías a las que pertenece la audiencia. Una audiencia puede pertenecer a varias categorías. |

### Detectar superposiciones con [!DNL Amazon Marketing Cloud] {#discover-overlaps}

La sección **[!UICONTROL Detectar superposiciones con Amazon Marketing Cloud]** proporciona información sobre cómo las audiencias se superponen con [!DNL Amazon] segmentos de segmentación o audiencias. Puede ver las métricas siguientes:

| Métrica | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID resueltos] | El número de identificadores [!DNL Amazon's Identity Resolution] se pudo resolver con sus datos de audiencia. |
| [!UICONTROL ID expuestos y superpuestos] | Representa el número de [!UICONTROL ID resueltos] de la audiencia cargada que también se expusieron a un anuncio a través de [!DNL Amazon Ads]. Esto solo tiene en cuenta las impresiones de DSP. |
| [!UICONTROL Superposición %] | La proporción de [!UICONTROL ID resueltos] que se han expuesto a un anuncio a través de [!DNL Amazon Ads]. |

## Medida {#measure}

La pestaña **[!UICONTROL Measure]** está disponible cuando la instancia [!DNL AMC] contiene ID de campaña. Cuando crea un proyecto, Real-Time CDP Collaboration ejecuta consultas en segundo plano con los datos de [!DNL AMC] para rellenar la sección [!UICONTROL Discover] y las listas de eventos de conversión y campaña utilizadas para configurar los informes de medición.

Para obtener instrucciones paso a paso sobre cómo crear e interpretar [!DNL AMC] informes de medición, lea la guía [crear informes de medición AMC](./amc-measure.md).
