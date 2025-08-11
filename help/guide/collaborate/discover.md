---
title: Descubra superposiciones y compare audiencias
description: Descubra las superposiciones entre las audiencias de y de sus colaboradores. Descubra las mejores audiencias para usar en sus campañas.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: 7fef1c490c2b980fa823c9ec75ba158568b11988
workflow-type: tm+mt
source-wordcount: '2068'
ht-degree: 12%

---

# Descubra superposiciones y compare audiencias

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>El área de trabajo **[!UICONTROL Discover]** solo está disponible si el caso de uso **Detección de audiencias** se habilitó [durante el proceso de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./manage-projects.md#project-use-cases).

Después de [crear un proyecto](/help/guide/collaborate/manage-projects.md), puedes comparar tus audiencias con las de tus colaboradores. Esto le ayuda a identificar audiencias relevantes para las campañas y a decidir cuáles enviar a los colaboradores para su activación.

>[!IMPORTANT]
>
>Cualquier [boceto de datos](/help/guide/glossary.md#sketches) que no se actualice o actualice se eliminará pasados 7 días. Cuando esto sucede, las cifras mostradas en los distintos informes de superposición de esta página se reducen a cero y el uso compartido de audiencias deja de estar disponible para estas audiencias caducadas. Los bocetos de datos se actualizan automáticamente para las audiencias con una [programación de actualización activa](/help/guide/setup/onboard-audiences.md#schedule).

Las claves de coincidencia utilizadas para detectar y comparar audiencias se han configurado [durante el proceso de conexión](/help/guide/connect/establishing-connections.md#connection-settings). Las claves de coincidencia se utilizan para calcular la superposición entre las audiencias y se pueden activar y desactivar. Para editar las claves de coincidencia, seleccione la opción **[!UICONTROL Editar claves de coincidencia]**.

![Espacio de trabajo de la ficha Descubrimiento, que muestra las perspectivas de Audiencia.](/help/assets/collaborate/discover/discover-overview.png)

Se abre el cuadro de diálogo **[!UICONTROL Editar claves de coincidencia]**, donde puede desactivar las claves de coincidencia que no desee usar. Seleccione **[!UICONTROL Guardar]** para guardar los cambios.

![Cuadro de diálogo Editar claves de coincidencia en el área de trabajo de Discover.](/help/assets/collaborate/discover/edit-match-keys.png)

## Requisitos previos {#prerequisites}

Para empezar a usar la ficha **[!UICONTROL Discover]** en el proyecto, debes tener:

* [Audiencias de origen](/help/guide/setup/onboard-audiences.md) en su cuenta
* [Conectado](/help/guide/connect/establishing-connections.md) con un colaborador con el caso de uso de **descubrimiento de audiencias** habilitado
* [Creó un proyecto](/help/guide/collaborate/manage-projects.md) entre usted y un colaborador

Una vez cumplidos estos requisitos previos, puede empezar a explorar y comparar las superposiciones entre usted y las audiencias de su colaborador.

## Comparar públicos {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Comparar públicos"
>abstract="Descubra los solapamientos entre sus públicos y los de de su colaborador. Puede ajustar la configuración en el selector desplegable para detectar los solapamientos entre uno o varios de sus públicos y uno o varios públicos de su colaborador."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Su recuento de identidades"
>abstract="El número de ID únicos dentro del público seleccionado, en función de las claves de coincidencia que usted y su colaborador hayan acordado para el proyecto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Recuento de identidades del colaborador"
>abstract="El número de ID únicos dentro del público de su colaborador, según las claves de coincidencia que usted y su colaborador hayan acordado para el proyecto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Recuento de identidades solapadas"
>abstract="El número de ID únicos que están presentes tanto en el público del usuario como en la del colaborador, según las claves de coincidencia que el usuario y el colaborador hayan acordado para el proyecto."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Porcentaje de identidades solapadas"
>abstract="El porcentaje de perfiles que se solapan entre el público seleccionado por usted y el seleccionado por su colaborador."

Utilice la sección de comparación de audiencias para obtener información enriquecida sobre la superposición entre las audiencias de y de su colaborador. Para cambiar la selección de audiencias, usa el selector desplegable en la parte superior de la sección **[!UICONTROL Comparar audiencias]**. Puede seleccionar una o todas las audiencias y una o todas las audiencias de su colaborador para compararlas entre sí.

![El área de trabajo de Discover con el selector de audiencia resaltado en la sección Comparar audiencias.](/help/assets/collaborate/discover/compare-audiences-selector.png)

En la sección de comparación de audiencias, puede ver las siguientes métricas, que se basan en las claves de coincidencia que usted y su colaborador acordaron para el proyecto:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Recuento de identidades]** (suyos) | El número de ID únicos dentro de las audiencias seleccionadas. |
| **[!UICONTROL Recuento de identidades]** (su colaborador) | El número de ID únicos dentro de la audiencia de su colaborador. |
| **[!UICONTROL Identidades superpuestas]** | El número de ID únicos que están presentes en la audiencia del usuario y en la del colaborador. |
| **[!UICONTROL Superposición %]** | El porcentaje de perfiles que se solapan entre el público seleccionado por usted y el seleccionado por su colaborador. |
| **[!UICONTROL Índice de audiencia]** | Una puntuación que indica la intensidad con la que una audiencia se relaciona con otra en función de los recuentos y superposiciones de audiencias subyacentes. Para obtener más información sobre el significado de las puntuaciones, lea la sección [puntuación del índice de audiencia](#audience-index-score). Las puntuaciones del índice de audiencia no están disponibles al compararlas con la línea de base de su colaborador (todas las audiencias). |
| **[!UICONTROL Desglose de identidades por clave de coincidencia]** | El desglose de identidades para cada clave de coincidencia elegida en el proyecto, en función de las audiencias seleccionadas para cada colaborador. |

{style="table-layout:auto"}

>[!NOTE]
>
>Es posible que la cifra de porcentaje de superposición y la puntuación del índice de audiencia no estén siempre disponibles para todas las audiencias. La visibilidad del porcentaje de superposición y la puntuación del índice de audiencia depende de la configuración que el colaborador elija para una audiencia en la [sección de visibilidad de metadatos](/help/guide/setup/onboard-audiences.md#metadata-visibility).

Si su colaborador no ha activado el índice de audiencia ni el porcentaje de superposición, la audiencia no tendrá disponibles datos de comparación.

## Públicos relevantes {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Públicos relevantes"
>abstract="En funció de los porcentajes de solapamiento, estos públicos pueden ser adecuados para su campaña. <br><br> El <b>El recuento de identidades</b> es el tamaño de público del colaborador. <br><br> <b>Identidades solapadas</b> representa el solapamiento entre el público recomendado y todos los públicos. <br><br> El <b>% de solapamiento</b> representa el número de identidades solapadas dividido por el tamaño de <i>todos</i> los públicos."

La sección **[!UICONTROL Audiencias relevantes]** de la pestaña **[!UICONTROL Descubrir]** proporciona una lista revisada de las cinco audiencias principales en función del porcentaje de superposición entre la audiencia de su colaborador y todas sus audiencias. Esta función le ayuda a identificar rápidamente las audiencias con la mayor superposición, lo que le permite segmentar sus campañas de forma más eficaz. Cambie entre las audiencias relevantes mediante los selectores de página en la parte superior derecha de la sección.

![Espacio de trabajo de Discover con la sección Audiencias relevantes resaltada.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>La visibilidad de las audiencias del colaborador depende de la configuración que el colaborador elija para una audiencia en la [sección de acceso a la conexión](/help/guide/setup/onboard-audiences.md#connection-access) y en la [sección de visibilidad de metadatos](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si el colaborador ha establecido todas las audiencias como privadas, esta sección no mostrará ninguna audiencia.

La sección **[!UICONTROL Audiencias relevantes]** muestra la siguiente información para cada audiencia recomendada:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Recuento de identidades]** | El número de ID únicos dentro de la audiencia. |
| **[!UICONTROL Identidades superpuestas]** | El número de ID únicos que se superponen entre la audiencia recomendada y todas las audiencias. |
| **[!UICONTROL Superposición %]** | El porcentaje de identidades superpuestas entre la audiencia recomendada y todas las audiencias. |
| **[!UICONTROL Índice de audiencia]** | Una puntuación que indica la intensidad con la que una audiencia se relaciona con otra en función de los recuentos y superposiciones de audiencias subyacentes. Para obtener más información sobre el significado de las puntuaciones, lea la sección [puntuación del índice de audiencia](#audience-index-score). |
| **[!UICONTROL Categorías de audiencia]** | Las categorías que el colaborador ha asignado a la audiencia. |
| **[!UICONTROL Claves coincidentes]** | Las claves de coincidencia que el colaborador seleccionó para la audiencia. |

{style="table-layout:auto"}

Si la puntuación del índice de audiencia está habilitada para cualquiera de las audiencias de su colaborador, las audiencias relevantes se basarán en la puntuación del índice de audiencia y no se incluirán las audiencias en las que no se haya habilitado el índice de audiencia. Las audiencias relevantes basadas en la puntuación del índice de audiencia se ordenan de modo que se muestre primero la puntuación de índice más alta. Si el índice de audiencia no está habilitado para ninguna de las audiencias de su colaborador, las audiencias relevantes se basarán en el porcentaje de superposición.

## Detecctar solapamientos {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Detectar solapamientos con públicos individuales"
>abstract="Obtenga información sobre las superposiciones entre sus públicos y los de su colaborador."

Descubra superposiciones para obtener información sobre cómo se comparan las audiencias con las de sus colaboradores. De forma predeterminada, esta sección compara todas las audiencias con las de cada colaborador. Utilice el control de paginación situado en la parte inferior de la sección para navegar por las audiencias disponibles.

![Área de trabajo de Discover con la sección Superposiciones de detección resaltada.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>La visibilidad de las audiencias del colaborador depende de la configuración que el colaborador elija para una audiencia en la [sección de acceso a la conexión](/help/guide/setup/onboard-audiences.md#connection-access) y en la [sección de visibilidad de metadatos](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si el colaborador ha establecido todas las audiencias como privadas, esta sección no mostrará ninguna audiencia.

Si el colaborador no ha activado el índice de audiencia o el porcentaje de superposición, la audiencia no se muestra.

Para cambiar tu selección de audiencia, selecciona **[!UICONTROL Cambiar audiencia]**.

![Espacio de trabajo de Discover con la opción Cambiar audiencia resaltada.](/help/assets/collaborate/discover/change-audience.png)

Se abre el cuadro de diálogo **[!UICONTROL Cambiar audiencia]**, donde puede seleccionar una audiencia específica para compararla con las audiencias de su colaborador. Seleccione las audiencias que desee o borre las selecciones para seleccionar todas las audiencias y luego seleccione **[!UICONTROL Guardar]**.

![Cuadro de diálogo Cambiar audiencia en el área de trabajo de Discover.](/help/assets/collaborate/discover/change-audience-selection.png)

Una vez que haya seleccionado las audiencias que desee, la sección **[!UICONTROL Detectar superposiciones]** muestra la siguiente información para cada audiencia:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Recuento de identidades]** | El número de ID únicos dentro de la audiencia. |
| **[!UICONTROL Identidades superpuestas]** | El número de ID únicos que se superponen entre la audiencia recomendada y todas las audiencias. |
| **[!UICONTROL Superposición %]** | El porcentaje de identidades superpuestas entre la audiencia recomendada y todas las audiencias. |
| **[!UICONTROL Índice de audiencia]** | Una puntuación que indica la intensidad con la que una audiencia se relaciona con otra en función de los recuentos y superposiciones de audiencias subyacentes. Para obtener más información sobre el significado de las puntuaciones, lea la sección [puntuación del índice de audiencia](#audience-index-score). |
| **[!UICONTROL Categorías de audiencia]** | Las categorías que el colaborador ha asignado a la audiencia. |
| **[!UICONTROL Claves coincidentes]** | Las claves de coincidencia que el colaborador seleccionó para la audiencia. |

{style="table-layout:auto"}

## Puntuación del índice de audiencia {#audience-index-score}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_audience_index_score"
>title="Puntuación del índice de audiencia"
>abstract="Las puntuaciones del índice de audiencia son una métrica con matices que muestra en qué medida una audiencia se relaciona con otra en función de los recuentos de audiencias subyacentes y las superposiciones. La puntuación del índice sin procesar se traduce en bandas de relevancia, que categorizan las puntuaciones del índice de audiencia de muy baja a muy alta. Esto le permite evaluar rápidamente la solidez de la relación entre la audiencia y la audiencia del colaborador."

Las puntuaciones del índice de audiencia son una métrica con matices que muestra en qué medida una audiencia se relaciona con otra en función de los recuentos de audiencias subyacentes y las superposiciones. Esto le ayuda a contextualizar las perspectivas de audiencia e identificar audiencias de alto potencial para la prospección y la segmentación de campañas.

La puntuación del índice se calcula mediante la fórmula siguiente:

![Fórmula para calcular la puntuación de índice.](/help/assets/collaborate/discover/index-score-formula.png)

Imaginen que un fabricante de automóviles quiere hacer una campaña publicitaria con un gran editor de CTV para un nuevo modelo de SUV. El fabricante de automóviles tiene datos sobre quién posee actualmente un modelo similar y quiere utilizarlo para encontrar perspectivas adicionales para convertirlos en clientes. El fabricante de automóviles mira a las audiencias del editor de CTV para encontrar una audiencia relevante que coincida estrechamente con los actuales propietarios de SUV.

![El anunciante del coche frente a las audiencias del editor de CTV.](/help/assets/collaborate/discover/audience-index-score-example.png)

Se realizan cálculos de puntuación del índice que se pueden utilizar para determinar el éxito probable de la campaña:

| Audiencia del editor de CTV | Fórmula | Puntuación de índice (i) | Interpretación |
|------------------------|-------------|----------------|----------------|
| Línea base (todas las audiencias) | ((1,3 M / 1,3 M) / (50 M / 50 M)) * 100 | 100 | Sirve como línea de base con la que se comparan las demás audiencias de su colaborador. |
| Observadores de atracones | ((500 k / 1,3 M) / (20 M / 50 M)) * 100 | 96 | Al segmentar esta audiencia, tiene un 4 % menos de probabilidades de llegar a los propietarios de todoterrenos en comparación con la línea de base. |
| Amantes de la comedia | ((200 k / 1,3 M) / (6 M / 50 M)) * 100 | 128 | Al segmentar esta audiencia, tiene un 28 % más de probabilidades de llegar a los propietarios de todoterrenos en comparación con la línea de base. |
| Hombres 25-34 | ((700 k / 1,3 M) / (12 M / 50 M)) * 100 | 224 | Al segmentar esta audiencia, tiene un 124 % más de probabilidades de llegar a los propietarios de todoterrenos en comparación con la línea de base. |
| Entusiastas de la tecnología | ((500 k / 1,3 M) / (8 M / 50 M)) * 100 | 240 | Al segmentar esta audiencia, tiene un 140 % más de probabilidades de llegar a los propietarios de todoterrenos en comparación con la línea de base. |

{style="table-layout:auto"}

Para comprender mejor cómo afectarán las puntuaciones del índice a la campaña, se proporcionan bandas de relevancia junto con las puntuaciones.

### Bandas de relevancia {#audience-index-relevance-bands}

Para facilitar la comparación entre distintas audiencias y campañas, Collaboration convierte las puntuaciones de índice en bandas de relevancia (de muy baja a muy alta). Esto le permite evaluar rápidamente la solidez de la relación entre la audiencia y la audiencia del colaborador.

| Puntuación de índice (i) | Banda de relevancia | Descripción |
|---------|----------|-----------|
| i &lt; 60 | Muy baja | La superposición es mucho menos frecuente en la audiencia de destino que en la de destino, lo que indica una relación muy débil. Es mucho menos probable que los clientes que utilizan esta audiencia lleguen a su audiencia objetivo. |
| 60 &lt; i &lt; 80 | Bajo | La superposición es algo menos prevalente en la audiencia de destino en comparación con la audiencia, lo que sugiere una relación débil. Es menos probable que los clientes que utilizan esta audiencia lleguen a su audiencia objetivo. |
| 80 &lt; i &lt; 120 | Medio | La superposición tiene la misma prevalencia en la audiencia de destino que en la audiencia, lo que indica una relación típica. Los clientes que utilizan esta audiencia tienen una probabilidad media de llegar a su audiencia objetivo. |
| 120 &lt; i &lt; 140 | Alto | La superposición es más frecuente en la audiencia de destino que en la de destino, lo que muestra una fuerte relación. Es más probable que los clientes que utilizan esta audiencia lleguen a su audiencia objetivo. |
| i > 140 | Muy alta | La superposición es mucho más frecuente en la audiencia de destino que en la de destino, lo que refleja una relación muy sólida. Es mucho más probable que los clientes que utilizan esta audiencia lleguen a su audiencia objetivo. |

{style="table-layout:auto"}

Dentro de la sección Discover superposiciones, la puntuación del índice de audiencia mostrará la banda de relevancia junto a la puntuación. La puntuación estará codificada por colores para indicar la banda de relevancia, lo que facilita la identificación de la fuerza de la relación de un vistazo. Las bandas de muy baja y baja relevancia se muestran en naranja, bandas de relevancia media en negro y bandas de relevancia alta y muy alta en verde.

## Próximos pasos

Después de explorar y descubrir las audiencias deseadas, es hora de [activar](/help/guide/collaborate/activate.md) las audiencias que se deben usar en las campañas.
