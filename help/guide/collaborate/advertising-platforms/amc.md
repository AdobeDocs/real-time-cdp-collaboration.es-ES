---
title: Amazon Marketing Cloud
description: Learn about collaborating with Amazon Marketing Cloud in Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 1a1b8fec-384b-465f-832d-0772c518fdf1
TQID: https://experienceleague.adobe.com/jNTQWEaUuuvgqKboJWsUH4XoKStP49nB0GLUSze0eXw
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2: id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 665
ht-degree: 22%

---

# Amazon Marketing Cloud

{{limited-availability-release-note}}

After forming a connection with [!DNL Amazon Marketing Cloud] ([!DNL AMC]), advertisers can [create a project](../manage-projects.md#create-project) to collaborate with [!DNL AMC] to leverage its advanced analytics capabilities. After creating a project, you can use the **[!UICONTROL Discover]** section to compare audience insights and discover relevant audiences for your campaigns.

>[!IMPORTANT]
>
>The only use cases supported with [!DNL AMC] are **Audience discovery** and **Measurement**. Currently, only the **[!UICONTROL Discover]** section is available within your project with [!DNL AMC].

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

In the **[!UICONTROL Discover]** section, you can compare your AMC audience to all consumers reached by your Amazon Ads. You can also view Amazon targeting segments that your audience has the highest overlaps with, considering only DSP impressions (these segments can only be targeted in the DSP).

>[!IMPORTANT]
>
>Audience data is processed from the audiences uploaded to your [!DNL Amazon Ads] account. To learn how send use Experience Platform&#39;s Destinations feature to send yours audiences to your [!DNL Amazon Ads] account, read the [Amazon Ads connection](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/amazon-ads) guide.

![The Discover section in a project with Amazon Marketing Cloud.](/help/assets/collaborate/advertising-platforms/amc-discover.png){zoomable="yes"}

### Comparar públicos {#compare-audiences}

The **[!UICONTROL Compare audiences]** section provides insights into how your [!DNL AMC] audience overlaps with consumers reached by your Amazon Ads. Within the **[!UICONTROL Compare audiences]** section, you can view the following metrics:

| Métrica | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL Resolved IDs] | The number of IDs [!DNL Amazon’s Identity Resolution] was able to resolve using your audience data. |
| [!UICONTROL Overlapping ad exposed IDs] | The number of [!UICONTROL Resolved IDs] from the uploaded audience that have also been exposed to an ad via [!DNL Amazon Ads]. |
| [!UICONTROL Superposición %] | The proportion of [!UICONTROL Resolved IDs] that have been exposed to an ad via [!DNL Amazon Ads]. |
| [!UICONTROL Breakdown by Amazon ad product] | Breakdown of [!UICONTROL Overlapping ad exposed IDs] reached by either [!UICONTROL Sponsored Product] and/or [!UICONTROL DSP]. Each is represented as an individual percentage from total number of ad exposed IDs. Since an ID can belong to both [!UICONTROL Sponsored Products] and [!UICONTROL DSP], the percentages may not sum to 100%. |


### Públicos relevantes {#relevant-audiences}

The **[!UICONTROL Relevant audiences]** section provides insights into [!DNL Amazon] targeting segments, or audiences, that your audience has the highest overlaps with, considering only DSP impressions (these segments can only be targeted in the DSP). Puede alternar entre todas las audiencias relevantes y, dentro de cada sección, puede ver las siguientes métricas:

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
