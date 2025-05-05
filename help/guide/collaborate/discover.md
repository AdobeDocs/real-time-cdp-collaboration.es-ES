---
title: Descubra superposiciones y compare audiencias
description: Descubra las superposiciones entre las audiencias de y de sus colaboradores. Descubra las mejores audiencias para usar en sus campañas.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 24%

---

# Descubra superposiciones y compare audiencias

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>El área de trabajo **[!UICONTROL Discover]** solo está disponible si el caso de uso **Detección de audiencias** se habilitó [durante el proceso de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./manage-projects.md#project-use-cases).

Después de [crear un proyecto](/help/guide/collaborate/manage-projects.md) en un espacio de colaboración entre un anunciante y un editor, ahora puedes comparar tus audiencias con las de tu colaborador. De este modo, puede descubrir superposiciones entre audiencias y obtener perspectivas desglosadas por claves de coincidencia o identidades. Esto ayuda a los anunciantes a decidir qué audiencias compartir con los editores para su activación.

>[!IMPORTANT]
>
>Cualquier [boceto de datos](/help/guide/glossary.md#sketches) que no se actualice o actualice se eliminará pasados 7 días. Cuando esto sucede, las cifras mostradas en los distintos informes de superposición de esta página se reducen a cero y el uso compartido de audiencias deja de estar disponible para estas audiencias caducadas. Los bocetos de datos se actualizan automáticamente para las audiencias con una [programación de actualización activa](/help/guide/setup/onboard-audiences.md#schedule).

![Detectar superposiciones](/help/assets/collaborate/discover-overlaps/discover-overlaps.png)

Las claves de coincidencia utilizadas para detectar y comparar audiencias se establecen al [conectar con un editor](/help/guide/connect/establishing-connections.md#connection-settings). Para cambiar los porcentajes de superposición indicados como preparación para la ejecución de campañas, puede quitar las claves de coincidencia, pero no puede agregar nuevas claves de coincidencia en este momento. Para ello, vaya a la [configuración de conexión](/help/guide/connect/establishing-connections.md#connection-settings) entre los colaboradores.

![Editar pantalla de claves de coincidencia](/help/assets/collaborate/discover-overlaps/edit-match-keys.png)

## Requisitos previos {#prerequisites}

Para utilizar completamente la funcionalidad de la ficha **[!UICONTROL Discover]** del flujo de trabajo **[!UICONTROL Colaborar]**, ya ha hecho lo siguiente:

* [Audiencias importadas](/help/guide/setup/onboard-audiences.md)
* [Conectado](/help/guide/connect/establishing-connections.md) con un anunciante o editor deseado con el caso de uso de **descubrimiento de audiencias** habilitado
* [Creó un proyecto](/help/guide/collaborate/manage-projects.md) entre usted y un colaborador

Una vez cumplidos los requisitos previos mencionados, puede empezar a explorar y comparar la superposición entre las audiencias de y de su colaborador.

## Comparar públicos {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Comparar públicos"
>abstract="Descubra los solapamientos entre sus públicos y los de de su colaborador. Puede ajustar la configuración en el selector desplegable para detectar los solapamientos entre uno o varios de sus públicos y uno o varios públicos de su colaborador."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Su recuento de identidades"
>abstract="El número de perfiles con esa identidad seleccionada que forman parte de su público seleccionado"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Recuento de identidades del colaborador"
>abstract="El número de perfiles con esa identidad seleccionada que forman parte del público seleccionado de su colaborador"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Recuento de identidades solapadas"
>abstract="El número de perfiles con esa identidad seleccionada que están presentes tanto en su público como en el de su colaborador"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Porcentaje de identidades solapadas"
>abstract="El porcentaje de perfiles que se solapan entre el público seleccionado por usted y el seleccionado por su colaborador."

Utilice la tarjeta Comparar audiencias para obtener información enriquecida sobre la superposición entre las audiencias de y de su colaborador. Puede seleccionar comparar cualquiera de las siguientes combinaciones de audiencias:

* Una de las audiencias de se compara con una de las audiencias de su colaborador
* Una de las audiencias frente a todas las audiencias de los colaboradores
* Todas las audiencias se comparan con las de los colaboradores
* Todas las audiencias de con todas las audiencias de los colaboradores

La información mostrada está relacionada con lo siguiente:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Recuento de identidades]** (suyos) | El número de perfiles con una identidad seleccionada que forman parte de la audiencia seleccionada. |
| **[!UICONTROL Recuento de identidades]** (su colaborador) | El número de perfiles con una identidad seleccionada que forman parte de la audiencia seleccionada del colaborador. |
| **[!UICONTROL Identidades superpuestas]** | El número de perfiles con una identidad seleccionada que están presentes tanto en la audiencia de como en la de su colaborador. |
| **[!UICONTROL Porcentaje de superposición]** | El porcentaje de perfiles que se solapan entre el público seleccionado por usted y el seleccionado por su colaborador. |
| **[!UICONTROL Desglose de identidades por clave de coincidencia]** | En función de las claves de coincidencia que usted y su colaborador hayan acordado para el proyecto, visualice la composición de las identidades en los cálculos de superposición por claves de coincidencia individuales. |

{style="table-layout:auto"}

>[!TIP]
>
>Es posible que la cifra de porcentaje de superposición no siempre esté disponible para todas las audiencias. La visibilidad del indicador de porcentaje de superposición depende de la configuración que el colaborador elija para una audiencia en la [sección de visibilidad de metadatos](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Públicos relevantes {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Públicos relevantes"
>abstract="En función de los porcentajes de solapamiento, estos públicos del publicador pueden ser adecuados para su campaña. <br><br> <b>El recuento de identidades</b> es el tamaño de público del publicador. <br><br> <b>Identidades solapadas</b> representa el solapamiento entre el público del publicador recomendado y todos los públicos del anunciante. <br><br> El <b>% de solapamiento</b> representa el número de identidades solapadas dividido por el tamaño de <i>todos</i> los públicos del anunciante."

La vista **[!UICONTROL Audiencias relevantes]** del módulo **[!UICONTROL Discover]** proporciona una lista revisada de las cinco audiencias principales en función del porcentaje de superposición. Esta función le ayuda a identificar rápidamente las audiencias con la mayor superposición con los datos actuales, lo que le permite segmentar las campañas de forma más eficaz.

* **[!UICONTROL Recuento de identidad]** es el tamaño de audiencia del editor.
* **[!UICONTROL Identidades superpuestas]** representa la superposición entre la audiencia del editor recomendado y todas las audiencias del anunciante.
* **[!UICONTROL Superposición %]** representa el número de identidades superpuestas dividido por el tamaño de *todas* las audiencias del anunciante.

![Vista de audiencias relevantes](/help/assets/collaborate/discover-overlaps/relevant-audiences-highlighted.png)

## Detecctar solapamientos {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Detectar solapamientos con públicos individuales"
>abstract="Obtenga información sobre la población de este público y sus superposiciones con el universo de identidades del colaborador."

![Detectar superposiciones con distintas vistas de audiencias](/help/assets/collaborate/discover-overlaps/discover-overlaps-cards-view.png)

Obtenga amplia información sobre cualquiera de las audiencias de su colaborador y vea información de superposición comparando estas audiencias con todo el recuento de población en todas las audiencias o con audiencias específicas suyas.

>[!TIP]
>
>Es posible que algunos de los números indicados en la captura de pantalla no estén siempre disponibles para todas las audiencias. Su visibilidad depende de la configuración que el colaborador elija para una audiencia en la [sección de visibilidad de metadatos](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Pasos siguientes

Después de explorar y descubrir las audiencias que deseas, es hora de [compartir](/help/guide/collaborate/share.md) las audiencias que se deben usar en las campañas con el editor.
