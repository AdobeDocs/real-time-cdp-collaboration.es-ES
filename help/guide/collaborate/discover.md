---
title: Descubra superposiciones y compare audiencias
description: Descubra las superposiciones entre las audiencias de y de sus colaboradores. Descubra las mejores audiencias para usar en sus campañas.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: 92702e8dd596dc6249a7240f0e3b57b661905c30
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 11%

---

# Descubra superposiciones y compare audiencias

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>El área de trabajo **[!UICONTROL Discover]** solo está disponible si el caso de uso **Detección de audiencias** se habilitó [durante el proceso de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./manage-projects.md#project-use-cases).

Después de [crear un proyecto](/help/guide/collaborate/manage-projects.md), puedes comparar tus audiencias con las de tus colaboradores. Esto le ayuda a identificar audiencias relevantes para las campañas y a decidir cuáles enviar a los editores para que las activen.

>[!IMPORTANT]
>
>Cualquier [boceto de datos](/help/guide/glossary.md#sketches) que no se actualice o actualice se eliminará pasados 7 días. Cuando esto sucede, las cifras mostradas en los distintos informes de superposición de esta página se reducen a cero y el uso compartido de audiencias deja de estar disponible para estas audiencias caducadas. Los bocetos de datos se actualizan automáticamente para las audiencias con una [programación de actualización activa](/help/guide/setup/onboard-audiences.md#schedule).

Las claves de coincidencia utilizadas para detectar y comparar audiencias se han configurado [durante el proceso de conexión](/help/guide/connect/establishing-connections.md#connection-settings). Las claves de coincidencia se utilizan para calcular la superposición entre las audiencias y se pueden activar y desactivar. Para editar las claves de coincidencia, seleccione la opción **[!UICONTROL Editar claves de coincidencia]**. Esta

![Espacio de trabajo de la ficha Descubrimiento, que muestra las perspectivas de Audiencia.](/help/assets/collaborate/discover/discover-overview.png)

Se abre el cuadro de diálogo **[!UICONTROL Editar claves de coincidencia]**, donde puede desactivar las claves de coincidencia que no desee usar. Seleccione **[!UICONTROL Guardar]** para guardar los cambios.

![Cuadro de diálogo Editar claves de coincidencia en el área de trabajo de Discover.](/help/assets/collaborate/discover/edit-match-keys.png)

## Requisitos previos {#prerequisites}

Para empezar a usar la ficha **[!UICONTROL Discover]** en el proyecto, debes tener:

* [Audiencias importadas](/help/guide/setup/onboard-audiences.md) en su organización
* [Conectado](/help/guide/connect/establishing-connections.md) con un colaborador con el caso de uso de **descubrimiento de audiencias** habilitado
* [Creó un proyecto](/help/guide/collaborate/manage-projects.md) entre usted y un colaborador

Una vez cumplidos estos requisitos previos, puede empezar a explorar y comparar la superposición entre usted y las audiencias de su colaborador.

## Comparar públicos {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Comparar públicos"
>abstract="Descubra los solapamientos entre sus públicos y los de de su colaborador. Puede ajustar la configuración en el selector desplegable para detectar los solapamientos entre uno o varios de sus públicos y uno o varios públicos de su colaborador."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Su recuento de identidades"
>abstract="El número de ID únicos dentro de la audiencia seleccionada, en función de las claves de coincidencia que usted y su colaborador acordaron para el proyecto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Recuento de identidades del colaborador"
>abstract="El número de ID únicos dentro de la audiencia de su colaborador, según las claves de coincidencia que usted y su colaborador acordaron para el proyecto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Recuento de identidades solapadas"
>abstract="El número de ID únicos que están presentes en la audiencia del usuario y la del colaborador, según las claves de coincidencia que el usuario y el colaborador acordaron para el proyecto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Porcentaje de identidades solapadas"
>abstract="Porcentaje de identidades superpuestas entre usted y la audiencia seleccionada del colaborador."

Utilice la sección de comparación de audiencias para obtener información enriquecida sobre la superposición entre las audiencias de y de su colaborador. Para cambiar la selección de audiencias, usa el selector desplegable en la parte superior de la sección **[!UICONTROL Comparar audiencias]**. Puede seleccionar una o todas las audiencias y una o todas las audiencias de su colaborador para compararlas entre sí.

![El área de trabajo de Discover con el selector de audiencia resaltado en la sección Comparar audiencias.](/help/assets/collaborate/discover/compare-audiences-selector.png)

En la sección de comparación de audiencias, puede ver las siguientes métricas, que se basan en las claves de coincidencia que usted y su colaborador acordaron para el proyecto:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Recuento de identidades]** (suyos) | El número de ID únicos dentro de las audiencias seleccionadas. |
| **[!UICONTROL Recuento de identidades]** (su colaborador) | El número de ID únicos dentro de la audiencia de su colaborador. |
| **[!UICONTROL Identidades superpuestas]** | El número de ID únicos que están presentes en la audiencia del usuario y en la del colaborador. |
| **[!UICONTROL Superposición %]** | El porcentaje de perfiles que se solapan entre el público seleccionado por usted y el seleccionado por su colaborador. |
| **[!UICONTROL Desglose de identidades por clave de coincidencia]** | El desglose de identidades para cada clave de coincidencia elegida en el proyecto, en función de las audiencias seleccionadas para cada colaborador. |

{style="table-layout:auto"}

>[!TIP]
>
>Es posible que la cifra de porcentaje de superposición no siempre esté disponible para todas las audiencias. La visibilidad del indicador de porcentaje de superposición depende de la configuración que el colaborador elija para una audiencia en la [sección de visibilidad de metadatos](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Públicos relevantes {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Públicos relevantes"
>abstract="En función de los porcentajes de solapamiento, estos públicos del publicador pueden ser adecuados para su campaña. <br><br> <b>El recuento de identidades</b> es el tamaño de público del publicador. <br><br> <b>Identidades solapadas</b> representa el solapamiento entre el público del publicador recomendado y todos los públicos del anunciante. <br><br> El <b>% de solapamiento</b> representa el número de identidades solapadas dividido por el tamaño de <i>todos</i> los públicos del anunciante."

La sección **[!UICONTROL Audiencias relevantes]** de la pestaña **[!UICONTROL Descubrir]** proporciona una lista revisada de las cinco audiencias principales en función del porcentaje de superposición entre la audiencia de su colaborador y todas sus audiencias. Esta función le ayuda a identificar rápidamente las audiencias con la mayor superposición, lo que le permite segmentar sus campañas de forma más eficaz. Cambie entre las audiencias relevantes mediante los selectores de página en la parte superior derecha de la sección.

![Espacio de trabajo de Discover con la sección Audiencias relevantes resaltada.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>La visibilidad de las audiencias del colaborador depende de la configuración que el colaborador elija para una audiencia en la [sección de visibilidad de metadatos](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si el colaborador ha establecido todas las audiencias como privadas, esta sección no mostrará ninguna audiencia.

La sección **[!UICONTROL Audiencias relevantes]** muestra la siguiente información para cada audiencia recomendada:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Recuento de identidades]** | Nombre ID únicos dentro de la audiencia. |
| **[!UICONTROL Identidades superpuestas]** | El número de ID únicos que se superponen entre la audiencia recomendada y todas las audiencias. |
| **[!UICONTROL Superposición %]** | El porcentaje de identidades superpuestas entre la audiencia recomendada y todas las audiencias. |
| **[!UICONTROL Categorías de audiencia]** | Las categorías que el colaborador ha asignado a la audiencia. |
| **[!UICONTROL Claves coincidentes]** | Las claves de coincidencia que el colaborador seleccionó para la audiencia. |

{style="table-layout:auto"}

>[!NOTE]
>
>La visibilidad de las audiencias del colaborador depende de la configuración que el colaborador elija para una audiencia en la [sección de visibilidad de metadatos](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si el colaborador ha establecido todas las audiencias como privadas, esta sección no mostrará ninguna audiencia.

## Detecctar solapamientos {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Detectar solapamientos con públicos individuales"
>abstract="Obtenga información sobre las superposiciones entre sus audiencias y las audiencias de su colaborador."

Descubra superposiciones para obtener información sobre cómo se comparan las audiencias con las de sus colaboradores. De forma predeterminada, esta sección compara todas las audiencias con las de cada colaborador. Utilice el control de paginación situado en la parte inferior de la sección para navegar por las audiencias disponibles.

![Área de trabajo de Discover con la sección Superposiciones de detección resaltada.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>La visibilidad de las audiencias del colaborador depende de la configuración que el colaborador elija para una audiencia en la [sección de visibilidad de metadatos](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si el colaborador ha establecido todas las audiencias como privadas, esta sección no mostrará ninguna audiencia.

Para cambiar tu selección de audiencia, selecciona **[!UICONTROL Cambiar audiencia]**.

![Espacio de trabajo de Discover con la opción Cambiar audiencia resaltada.](/help/assets/collaborate/discover/change-audience.png)

Se abre el cuadro de diálogo **[!UICONTROL Cambiar audiencia]**, en el que puede comparar una audiencia específica con las audiencias de su colaborador. Seleccione las audiencias que desee o borre las selecciones para seleccionar todas las audiencias y luego seleccione **[!UICONTROL Guardar]**.

![Cuadro de diálogo Cambiar audiencia en el área de trabajo de Discover.](/help/assets/collaborate/discover/change-audience-selection.png)

Una vez que haya seleccionado las audiencias que desee, la sección **[!UICONTROL Detectar superposiciones]** muestra la siguiente información para cada audiencia:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Recuento de identidades]** | Nombre ID únicos dentro de la audiencia. |
| **[!UICONTROL Identidades superpuestas]** | El número de ID únicos que se superponen entre la audiencia recomendada y todas las audiencias. |
| **[!UICONTROL Superposición %]** | El porcentaje de identidades superpuestas entre la audiencia recomendada y todas las audiencias. |
| **[!UICONTROL Categorías de audiencia]** | Las categorías que el colaborador ha asignado a la audiencia. |
| **[!UICONTROL Claves coincidentes]** | Las claves de coincidencia que el colaborador seleccionó para la audiencia. |

{style="table-layout:auto"}

## Pasos siguientes

Después de explorar y descubrir las audiencias deseadas, es hora de [activar](/help/guide/collaborate/activate.md) las audiencias que se deben usar en las campañas.
