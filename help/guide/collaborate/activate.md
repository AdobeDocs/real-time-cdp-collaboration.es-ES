---
title: Activar públicos
description: Obtenga información sobre cómo activar audiencias en Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: afe8560a12017c6b993f93cde8636288aa6e4991
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 2%

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
>Al activar audiencias en las que se utilizan varias claves de coincidencia, si una (o más) clave de coincidencia no se superpone, no se contabiliza la audiencia o cae por debajo del umbral, toda la activación falla. Asegúrese de que las audiencias se superpongan lo suficiente y cumplan el umbral mínimo de 1000 ID en todas las claves de coincidencia antes de activarlas.

Seleccione la audiencia que desea activar en las campañas y luego seleccione **[!UICONTROL Guardar]**. La audiencia ahora se muestra y puede ver **[!UICONTROL Recuento de identidades]**, **[!UICONTROL identidades superpuestas]** y **[!UICONTROL Superposición %]** para la audiencia seleccionada.

![Flujo de trabajo de activación de audiencia con la audiencia seleccionada mostrada.](/help/assets/collaborate/activate/audience-selected.png)

### Editar claves de coincidencia {#edit-match-keys}

A continuación, puede editar las claves de coincidencia de la audiencia seleccionando **[!UICONTROL Editar claves de coincidencia]** dentro de la audiencia seleccionada. Estas opciones se heredan de las selecciones de claves de coincidencia cuando se configuró inicialmente la conexión entre colaboradores. Puede eliminar las claves de coincidencia seleccionadas si no se aplican a una campaña específica, pero no puede añadir nuevas claves de coincidencia.

![Flujo de trabajo de activación de audiencia con la opción Editar claves de coincidencia resaltada.](/help/assets/collaborate/activate/edit-match-keys.png)

Se abre el cuadro de diálogo **[!UICONTROL Editar claves de coincidencia]**, donde puede desactivar las claves de coincidencia que no desee usar. Seleccione **[!UICONTROL Guardar]** para guardar los cambios.

>[!NOTE]
>
>Se debe seleccionar al menos una clave de coincidencia. En la versión actual, las únicas claves de coincidencia disponibles son **[!UICONTROL Correo electrónico con hash]**, por lo que no puede eliminar esta clave de coincidencia.

![Cuadro de diálogo Editar claves de coincidencia en el flujo de trabajo de activación de Audience.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Establecer frecuencia de actualización de audiencia {#set-audience-refresh-frequency}

Finalmente, establezca la frecuencia y el intervalo de fechas deseados para que la audiencia se actualice. En la versión actual, la única opción de frecuencia admitida es **[!UICONTROL Una vez]**. La frecuencia **[!UICONTROL Una vez]** significa que las audiencias se activan una sola vez y no se actualizan. La opción **[!UICONTROL Date]** se rellena automáticamente con la fecha actual.

![Flujo de trabajo de activación de audiencia con la sección Frecuencia resaltada.](/help/assets/collaborate/activate/audience-frequency.png)

Cuando esté satisfecho con las selecciones, seleccione **[!UICONTROL Activar]** para completar el flujo de trabajo.

## Activar tablero {#activate-dashboard}

En la pestaña **[!UICONTROL Activar]**, puedes ver todas las audiencias que se enviaron a tu colaborador, así como todas las audiencias que tu colaborador activó en tu destino.

![El panel Activar muestra las secciones Audiencias enviadas y Audiencias activadas.](/help/assets/collaborate/activate/activate-dashboard.png)

## Ver audiencias enviadas {#view-sent-audiences}

En la sección **[!UICONTROL Audiencias enviadas al colaborador]**, se enumerarán todas las audiencias que haya enviado. Actualmente, las audiencias se envían automáticamente al destino configurado del colaborador después de enviarlas. En la vista de su colaborador, estas audiencias se muestran en la sección **[!UICONTROL Audiencias activadas]**.

Dentro de cada audiencia enviada, puede ver las siguientes métricas:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Nombre]** | Nombre de la audiencia. |
| **[!UICONTROL Estado]** | El estado de la audiencia enviada. |
| **[!UICONTROL Recuento de identidades]** | Número de identidades de la audiencia. |
| **[!UICONTROL Identidades superpuestas]** | El número de identidades superpuestas entre esta audiencia y la población total de perfiles en el inventario del colaborador. |
| **[!UICONTROL Creado]** | La fecha en la que se envió inicialmente la audiencia. |
| **[!UICONTROL Último envío]** | La fecha en la que la audiencia se envió por última vez a su colaborador. |
| **[!UICONTROL Claves coincidentes]** | Indica la clave de coincidencia utilizada para la audiencia. |

## Ver audiencias activadas {#view-activated-audiences}

En la sección **[!UICONTROL Audiencias activadas]** puede ver todas las audiencias que se han activado en su destino.

Dentro de cada audiencia activada, puede ver las siguientes métricas:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Nombre]** | Nombre de la audiencia. |
| **[!UICONTROL Estado]** | El estado de la audiencia activada. |
| **[!UICONTROL Recuento de identidades]** | El número de identidades activadas, en función de las identidades superpuestas cuando el colaborador envió la audiencia. |
| **[!UICONTROL Creado]** | La fecha en la que se activó la audiencia. |
| **[!UICONTROL Última actualización]** | La fecha en la que se actualizó la audiencia por última vez, según la programación de actualización elegida durante la activación. |
| **[!UICONTROL Destino]** | El destino en el que se activó la audiencia. |
| **[!UICONTROL Claves coincidentes]** | Indica la clave de coincidencia utilizada para la audiencia. |

## Eliminar audiencias enviadas {#delete-sent-audiences}

Puede eliminar las audiencias enviadas que ya no desee activar. Cuando elimina una audiencia enviada, se elimina de la sección **[!UICONTROL Audiencias enviadas a]** y ya no se activa en el destino de su colaborador.

Para eliminar una audiencia enviada, seleccione el icono **[!UICONTROL Eliminar]** (![Eliminar.](/help/assets/icons/delete.png)) junto a la audiencia en la sección **[!UICONTROL Audiencias enviadas a]**.

![Opción Eliminar en la sección Audiencias enviadas a.](/help/assets/collaborate/activate/delete-sent-audiences.png)

Se abrirá un cuadro de diálogo de confirmación en el que se le pedirá que confirme la eliminación. Seleccione **[!UICONTROL Eliminar]** para confirmar.

![Cuadro de diálogo de confirmación de eliminación.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

## Próximos pasos {#next-steps}

Después de activar audiencias y ejecutar campañas, trabaje con el equipo de ingeniería y habilitación de Adobe para cargar datos de medición y ver los [informes de medición](/help/guide/collaborate/measure.md) correspondientes.
