---
title: Activar públicos
description: Obtenga información sobre cómo activar audiencias en Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
TQID: https://experienceleague.adobe.com/bfPHtcW8Mf6RhIlg5fKcJmPSEKDyAODjbNRJ5D3SMkQ
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1016
ht-degree: 8%

---

# Activar públicos

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>El área de trabajo **[!UICONTROL Activar]** solo está disponible si el caso de uso **Activación de audiencias** se habilitó [durante el proceso de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./manage-projects.md#project-use-cases).

La activación de audiencias permite activar audiencias para utilizarlas en campañas. La activación puede realizarla el colaborador en función de la configuración de activación de audiencia [configurada en la conexión](/help/guide/connect/establishing-connections.md#configure-connection-settings). Después de [descubrir las mejores audiencias para tu campaña](./discover.md), actívalas para que estén disponibles para su uso. Al activar una audiencia, se envía al destino preconfigurado del colaborador, como Adobe Experience Platform, donde está disponible para su uso en campañas. Para obtener más información sobre la configuración de destinos, consulte la guía [descripción general de destinos](../destinations/overview.md).

## Activar nuevas audiencias {#activate-new-audiences}

Para empezar a activar audiencias, ve a la pestaña **[!UICONTROL Activar]** del área de trabajo del proyecto.

>[!IMPORTANT]
>
>**Antes de que** pueda activar una audiencia, su colaborador **debe** configurar un destino. Al activar una audiencia, esta se envía automáticamente al destino configurado del colaborador. Si no se configura ningún destino, no se pueden activar las audiencias.
>
>![Activa el espacio de trabajo cuando el colaborador no tiene ningún destino configurado.](/help/assets/collaborate/activate/no-destination-configured.png)

Seleccione el icono de agregar (![Agregar icono.](/help/assets/icons/plus.png)) o la opción **[!UICONTROL Activar audiencia]** si no se han enviado audiencias anteriores para su activación.

![El área de trabajo de activación en un proyecto sin audiencias agregadas.](/help/assets/collaborate/activate/activate-new-audiences.png)

Se abre el flujo de trabajo activar audiencias, donde puede seleccionar la audiencia que desea enviar a su colaborador. Utilice el menú desplegable para seleccionar una audiencia o buscar una audiencia específica. Para ver más información sobre las audiencias antes de realizar la selección, selecciona **[!UICONTROL Examinar audiencias]**

![Flujo de trabajo de activación de audiencia con las opciones desplegables y Examinar audiencias resaltadas.](/help/assets/collaborate/activate/audience-activation.png)

En **[!UICONTROL Examinar audiencias]**, puede ver **[!UICONTROL Recuento de identidades]**, **[!UICONTROL Identidades superpuestas]** y **[!UICONTROL Superposición %]** para cada audiencia.

![Cuadro de diálogo Examinar audiencias que muestra las audiencias disponibles.](/help/assets/collaborate/activate/browse-audiences.png)

>[!IMPORTANT]
>
>Al activar audiencias en las que se utilizan varias claves de coincidencia, si una (o más) clave de coincidencia no se superpone, no hay recuentos de público o cae por debajo del umbral, toda la activación falla. Asegúrese de que las audiencias se superpongan lo suficiente y cumplan el umbral mínimo de 1000 ID en todas las claves de coincidencia antes de activarlas.

Seleccione la audiencia que desea activar en las campañas y luego seleccione **[!UICONTROL Guardar]**. La audiencia ahora se muestra y puede ver **[!UICONTROL Recuento de identidades]**, **[!UICONTROL identidades superpuestas]** y **[!UICONTROL Superposición %]** para la audiencia seleccionada.

![The Audience activation workflow with the selected audience displayed.](/help/assets/collaborate/activate/audience-selected.png)

### Editar claves de coincidencia {#edit-match-keys}

Next, you can edit the audience&#39;s match keys by selecting **[!UICONTROL Edit match keys]** within the select audience. These options are inherited from your match key selections when the connection between collaborators was initially set up. You can remove match keys that were selected if they don&#39;t apply to a specific campaign, but you cannot add new match keys.

![The Audience activation workflow with the Edit match keys option highlighted.](/help/assets/collaborate/activate/edit-match-keys.png)

Se abre el cuadro de diálogo **[!UICONTROL Editar claves de coincidencia]**, donde puede desactivar las claves de coincidencia que no desee usar. Seleccione **[!UICONTROL Guardar]** para guardar los cambios.

>[!NOTE]
>
>At least one match key must be selected. In the current release, the only match keys available is **[!UICONTROL Hashed email]**, so you cannot remove this match key.

![The Edit match keys dialog in the Audiece activation workflow.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Set audience refresh frequency {#set-audience-refresh-frequency}

Finally, set the desired frequency and date range for the audience to refresh. In the current release, the only supported frequency option is **[!UICONTROL Once]**. The **[!UICONTROL Once]** frequency means the audiences are activated a single time and are not refreshed. The **[!UICONTROL Date]** option is auto-populated with the current date.

![The Audience activation workflow with the Frequency section highlighted.](/help/assets/collaborate/activate/audience-frequency.png)

When satisfied with your selections, select **[!UICONTROL Activate]** to complete the workflow.

## Activate dashboard {#activate-dashboard}

In the **[!UICONTROL Activate]** tab, you can view all audiences sent to your collaborator, as well as all audiences your collaborator has activated to your destination.

![The Activate dashboard showing the Sent audiences and Activated audiences sections.](/help/assets/collaborate/activate/activate-dashboard.png)

## View sent audiences {#view-sent-audiences}

In the **[!UICONTROL Sent audiences to]** collaborator section, all the audiences you&#39;ve sent will be listed. Currently, audiences are automatically sent to your collaborator&#39;s configured destination after you&#39;ve sent them. In your collaborator&#39;s view, these audiences are displayed in the **[!UICONTROL Activated audiences]** section.

Within each sent audience, you can see the following metrics:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Nombre]** | The name of the audience. |
| **[!UICONTROL Estado]** | The status of the sent audience. |
| **[!UICONTROL Recuento de identidad]** | The number of identities in the audience. |
| **[!UICONTROL Identidades superpuestas]** | The number of overlapping identities between this audience and the total population of profiles across the collaborator&#39;s inventory. |
| **[!UICONTROL Creado]** | The date when the audience was initially sent. |
| **[!UICONTROL Last sent]** | The date when the audience was last sent to your collaborator. |
| **[!UICONTROL Claves coincidentes]** | Indicates the match key used for the audience. |

## View activated audiences {#view-activated-audiences}

In the **[!UICONTROL Activated audiences]** section, you can see all the audiences that have been activated to your destination.

Within each activated audience, you can see the following metrics:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Nombre]** | The name of the audience. |
| **[!UICONTROL Estado]** | The status of the activated audience. |
| **[!UICONTROL Recuento de identidad]** | The number of identities that were activated, based off the overlapping identities when your collaborator sent the audience. |
| **[!UICONTROL Creado]** | The date when the audience was activated. |
| **[!UICONTROL Last refreshed]** | The date when the audience was last refreshed, based on the refresh schedule chosen during activation. |
| **[!UICONTROL Destino]** | The destination where the audience was activated to. |
| **[!UICONTROL Claves coincidentes]** | Indicates the match key used for the audience. |

## Delete sent audiences {#delete-sent-audiences}

You can delete sent audiences that you no longer want to activate. When you delete a sent audience, it is removed from the **[!UICONTROL Sent audiences to]** section, and it will no longer be activated to your collaborator&#39;s destination.

To delete a sent audience, select the **[!UICONTROL Delete]** icon (![Delete icon.](/help/assets/icons/delete.png)) next to the audience in the **[!UICONTROL Sent audiences to]** section.

![The Delete option in the Sent audiences to section.](/help/assets/collaborate/activate/delete-sent-audiences.png)

A confirmation dialog opens, asking you to confirm the deletion. Seleccione **[!UICONTROL Eliminar]** para confirmar.

![The Delete confirmation dialog.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

## Próximos pasos {#next-steps}

Después de activar audiencias y ejecutar campañas, trabaje con el equipo de ingeniería y habilitación de Adobe para cargar datos de medición y ver los [informes de medición](/help/guide/collaborate/measure.md) correspondientes.
