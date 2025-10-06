---
title: Amazon Marketing Cloud
description: Obtenga información acerca de la colaboración con Amazon Marketing Cloud en Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 57b847c25edbf88f4708bda74be41fe6141472a7
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 20%

---

# Amazon Marketing Cloud

{{limited-availability-release-note}}

Después de establecer una conexión con [!DNL Amazon Marketing Cloud] ([!DNL AMC]), los anunciantes pueden [crear un proyecto](../manage-projects.md#create-project) para colaborar con [!DNL AMC] a fin de aprovechar sus capacidades de análisis avanzadas. Después de crear un proyecto, puede usar la sección **[!UICONTROL Discover]** para comparar la información de audiencias y descubrir audiencias relevantes para sus campañas.

>[!IMPORTANT]
>
>Los únicos casos de uso admitidos con [!DNL AMC] son **Detección de audiencias** y **Medición**. En este momento, solamente la sección **[!UICONTROL Discover]** está disponible en su proyecto con [!DNL AMC].

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
>abstract="El número de ID que la resolución de identidad de Amazon pudo resolver con los datos de su público."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="ID expuestos a anuncios solapados"
>abstract="Representa el número de &#39;ID resueltos&#39; del público cargado que también se han expuesto en un anuncio a través de Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="% de solapamiento"
>abstract="La proporción de &#39;ID resueltos&#39; que se han expuesto a un anuncio a través de Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Desglose por producto publicitario de Amazon"
>abstract="Desglose de los “ID expuestos a anuncios solapados” a través de Amazon Ads Sponsor Product o Amazon Ads DSP."

En la sección **[!UICONTROL Discover]**, puedes comparar tu audiencia AMC con todos los consumidores a los que han llegado tus Amazon Ads. También puede ver los segmentos de segmentación de Amazon con los que la audiencia tiene la mayor superposición, teniendo en cuenta solo las impresiones de DSP (estos segmentos solo pueden segmentarse en DSP).

>[!IMPORTANT]
>
>Los datos de audiencias se procesan a partir de las audiencias cargadas en su cuenta de [!DNL Amazon Ads]. Para obtener información sobre cómo enviar y usar la función Destinos de Experience Platform para enviar tus audiencias a tu cuenta de [!DNL Amazon Ads], lee la guía de conexión de [Amazon Ads](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/catalog/advertising/amazon-ads).

![Sección Discover en un proyecto con Amazon Marketing Cloud.](/help/assets/collaborate/advertising-platforms/amc-discover.png){zoomable="yes"}

### Comparar públicos {#compare-audiences}

La sección **[!UICONTROL Comparar audiencias]** proporciona información sobre cómo la audiencia de [!DNL AMC] se superpone con los consumidores a los que llegan los anuncios de Amazon. En la sección **[!UICONTROL Comparar audiencias]**, puede ver las siguientes métricas:

| Métrica | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID resueltos] | El número de identificadores [!DNL Amazon’s Identity Resolution] se pudo resolver con sus datos de audiencia. |
| [!UICONTROL ID expuestos y superpuestos] | El número de [!UICONTROL ID resueltos] de la audiencia cargada que también se expusieron a un anuncio a través de [!DNL Amazon Ads]. |
| [!UICONTROL Superposición %] | La proporción de [!UICONTROL ID resueltos] que se han expuesto a un anuncio a través de [!DNL Amazon Ads]. |
| [!UICONTROL Desglose por producto de anuncios de Amazon] | Desglose de [!UICONTROL ID superpuestos y expuestos] alcanzados por [!UICONTROL producto patrocinado] o [!UICONTROL DSP]. Cada uno se representa como un porcentaje individual del número total de ID expuestos a publicidad. Dado que un ID puede pertenecer tanto a [!UICONTROL Productos patrocinados] como a [!UICONTROL DSP], es posible que los porcentajes no sumen el 100%. |


### Públicos relevantes {#relevant-audiences}

La sección **[!UICONTROL Audiencias relevantes]** proporciona información sobre [!DNL Amazon] segmentos de segmentación, o audiencias, con las que la audiencia tiene la mayor superposición, teniendo en cuenta solo las impresiones de DSP (estos segmentos solo se pueden segmentar en DSP). Puede alternar entre todas las audiencias relevantes y, dentro de cada sección, puede ver las siguientes métricas:

| Métrica | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID resueltos] | El número de identificadores [!DNL Amazon’s Identity Resolution] se pudo resolver con sus datos de audiencia. |
| [!UICONTROL ID expuestos y superpuestos] | Representa el número de [!UICONTROL ID resueltos] de la audiencia cargada que también se expusieron a un anuncio a través de [!DNL Amazon Ads]. Esto solo tiene en cuenta las impresiones de DSP. |
| [!UICONTROL Superposición %] | La proporción de [!UICONTROL ID resueltos] que se han expuesto a un anuncio a través de [!DNL Amazon Ads]. |
| [!UICONTROL Categorías] | La categoría o categorías a las que pertenece la audiencia. Una audiencia puede pertenecer a varias categorías. |

### Detectar superposiciones con [!DNL Amazon Marketing Cloud] {#discover-overlaps}

La sección **[!UICONTROL Detectar superposiciones con Amazon Marketing Cloud]** proporciona información sobre cómo las audiencias se superponen con [!DNL Amazon] segmentos de segmentación o audiencias. Puede ver las métricas siguientes:

| Métrica | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID resueltos] | El número de identificadores [!DNL Amazon’s Identity Resolution] se pudo resolver con sus datos de audiencia. |
| [!UICONTROL ID expuestos y superpuestos] | Representa el número de [!UICONTROL ID resueltos] de la audiencia cargada que también se expusieron a un anuncio a través de [!DNL Amazon Ads]. Esto solo tiene en cuenta las impresiones de DSP. |
| [!UICONTROL Superposición %] | La proporción de [!UICONTROL ID resueltos] que se han expuesto a un anuncio a través de [!DNL Amazon Ads]. |