---
title: Compartir públicos
description: Aprenda a compartir audiencias con sus colaboradores para campañas publicitarias.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0fdf0598-89c9-452d-a2e3-ce868df0b9d2
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 1%

---

# Compartir públicos

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>El área de trabajo **[!UICONTROL Compartir]** solo está disponible si el caso de uso de **Compartir audiencias y activación** se habilitó [durante el proceso de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./manage-projects.md#project-use-cases).

Como anunciante, aprenda a compartir audiencias con sus editores para que puedan ejecutar campañas. Si su colaboración ha habilitado el caso de uso **Detectar audiencias**, comience ejecutando informes de superposición en la [pestaña de detección](/help/guide/collaborate/discover.md) para identificar las mejores audiencias para compartir.

## Compartir nuevas audiencias

Para empezar a compartir audiencias, vaya a la pestaña **[!UICONTROL Compartir]** del área de trabajo del proyecto. Solo **las organizaciones de anunciantes** pueden compartir audiencias para campañas. En esta pestaña, puede revisar y administrar las audiencias compartidas.

Seleccione el **símbolo más (+)** o la opción **[!UICONTROL Compartir audiencia]** si no se han compartido audiencias anteriores, para iniciar el proceso de uso compartido de audiencias.

![Vista predeterminada sin audiencias compartidas.](/help/assets/collaborate/share/share-new-audiences.png)

Aparece un nuevo panel, donde puede seleccionar las audiencias que desea compartir con su colaborador.

![Compartir nuevo flujo de trabajo de audiencias.](/help/assets/collaborate/share/share-audiences-workflow.png)

### Seleccionar audiencias para compartir

En la ventana de selección de audiencias, puede buscar audiencias específicas para compartir introduciendo el nombre de la audiencia en la barra de búsqueda. Seleccione **[!UICONTROL Examinar audiencias]** y use las opciones de ordenación disponibles para encontrar las audiencias exactas que necesita.

![Examinar la vista de audiencias con las audiencias seleccionadas.](/help/assets/collaborate/share/browse-audiences-view.png)

### Editar claves de coincidencia y definir opciones de segmentación

Después de seleccionar las audiencias que desea compartir, ahora puede seleccionar otras opciones de configuración para la actividad de uso compartido.

![Editar claves de coincidencia y seleccionar o suprimir selector resaltado](/help/assets/collaborate/share/match-keys-and-targeting.png)

Seleccione **[!UICONTROL Editar claves de coincidencia]** para indicar qué claves de coincidencia se deben usar para las identidades en la audiencia. Estas opciones se heredan de la configuración seleccionada cuando se configuró inicialmente la conexión entre colaboradores. Puede eliminar las claves de coincidencia seleccionadas en ese momento si no se aplican a esta campaña específica, pero no puede añadir nuevas claves de coincidencia en este momento.

![Editar claves de coincidencia.](/help/assets/collaborate/share/update-match-keys.png)

Para cada audiencia, seleccione si desea que los miembros de esa audiencia se segmenten o se supriman en la campaña. Los perfiles suprimidos específicamente no formarán parte de la audiencia activada por el editor.

### Establecer frecuencia e intervalo de actualización de audiencia

Finalmente, establezca la frecuencia y el intervalo de fechas deseados para la actualización de la audiencia. Los modos actualmente admitidos para la actualización de audiencias son **[!UICONTROL Una vez]** y **[!UICONTROL Diario]**.

Al seleccionar **[!UICONTROL Una vez]**, la pertenencia a la audiencia no se actualiza durante toda la campaña. Al seleccionar **[!UICONTROL Diario]**, la pertenencia a la audiencia se actualiza una vez al día durante toda la campaña.

![Opciones de frecuencia resaltadas.](/help/assets/collaborate/share/audience-refresh-frequency.png)

Cuando esté satisfecho con las selecciones, seleccione **[!UICONTROL Compartir]** para completar el flujo de trabajo.

>[!SUCCESS]
>
>Ahora puede ver una nueva actividad para compartir audiencias en la pestaña **[!UICONTROL Compartir]**. Si lo desea, puede volver atrás y editar cualquiera de las selecciones realizadas.

## Ver audiencias compartidas actualmente

En la ficha **[!UICONTROL Compartir]**, puede ver las audiencias que están compartiendo actualmente los colaboradores, agrupadas en actividades de uso compartido de audiencias.

![Información general sobre la ficha para compartir.](/help/assets/collaborate/share/share-tab-overview.png)

<!--

The banner at the top of the page shows figures across all audience sharing activities. 

![The hero banner in the sharing tab.](/help/assets/collaborate/share/share-hero-banner.png)


|Metric | Description |
|---------|----------|
| **[!UICONTROL Shared audiences]** | Indicates the number of audiences shared between collaborators in this project, across all audience sharing modules. |
| **[!UICONTROL Estimated addressable reach]** | Indicates the approximate number of profiles that you can reach across all the audiences that are currently shared in the project. [TODO: ADD INFORMATION ABOUT HOW THIS IS CALCULATED] |
| **[!UICONTROL Target identities]** | The number of identities across all audiences shared in this project for which you selected to target the profiles. |
| **[!UICONTROL Suppress identities]** | The number of identities across all audiences shared in this project for which you selected to suppress the profiles and thereby not target them in campaigns. |

-->

Dentro de cada actividad de uso compartido de audiencias, puede obtener información sobre cada audiencia compartida.

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Recuento de identidades]** | Indica el número de perfiles en todas las identidades vinculadas a esta audiencia, según la última evaluación del recuento de identidades. Estos números se actualizan cada 24 horas. |
| **[!UICONTROL Identidades superpuestas]** | Indica la cantidad de identidades superpuestas entre los miembros de esta audiencia y la población total de perfiles en el inventario del colaborador. |
| **[!UICONTROL Desglose de clave de coincidencia]** | Muestra el recuento de identidades de cada identidad utilizada en la audiencia. Por ejemplo, un recuento total de identidades de 500 000 usuarios puede constar de 400 000 usuarios que no escriben la identidad de correo electrónico con hash y 100 000 usuarios que no escriben una identidad de ID móvil. Tenga en cuenta que, en el ejemplo descrito aquí, la misma persona podría estar presente en la audiencia dos veces con sus identidades de correo electrónico e ID móvil. |
| **[!UICONTROL Objetivo]** | **[!UICONTROL Suprimir]** o **[!UICONTROL Destino]**. Indica si los miembros de una audiencia deben segmentarse o excluirse de las campañas. |

La página también proporciona controles para **[!UICONTROL Pausar el uso compartido]** y **[!UICONTROL Editar audiencias]**.

## Editar públicos {#edit-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_share_edit_audiences_usecases"
>title="Segmentación o supresión de casos de uso"
>abstract="<p>Seleccione **Target** si quiere que los perfiles de la audiencia se muestren como anuncios en la campaña.</p> <p>Seleccione **Suprimir** si desea excluir los perfiles de la audiencia de los mensajes de la campaña.</p>"

Seleccione **[!UICONTROL Editar audiencias]** para cambiar qué audiencias se comparten en un módulo de uso compartido de audiencias, así como para cambiar varias configuraciones relacionadas con cómo se comparten las audiencias.

![Vista del modal de edición de audiencias](/help/assets/collaborate/share/edit-audiences-modal.png)

<!--

Search for audiences that you want to add to the sharing module. 

For each audience, you can select whether you'd like to target or suppress those profiles in campaigns. 

To remove an audience from the sharing module, select the trash can icon [TODO: add spectrum icon and folder].

Select how often you would like the audience membership to be refreshed and the date range within which you want the membership of the audience to be refreshed. 

TODO: are there any limitations for frequency in the M1 release?

-->

## Pasos siguientes

Una vez que el editor reciba las audiencias compartidas, ahora las [activará](/help/guide/collaborate/activate.md) en campañas de publicidad digital.
