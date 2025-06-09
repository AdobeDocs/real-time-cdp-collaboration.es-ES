---
title: Activar públicos
description: Obtenga información sobre cómo activar audiencias en Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: f19aff1b7d10a446dd209721e7a6fdf537c9d63e
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# Activar públicos

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>El área de trabajo **[!UICONTROL Activar]** solo está disponible si el caso de uso **Activación de audiencias** se habilitó [durante el proceso de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./manage-projects.md#project-use-cases).

La activación de audiencias permite activar audiencias en campañas. El proceso de actividad es una colaboración entre anunciantes y editores. Después de [descubrir las mejores audiencias para tu campaña](./discover.md), las audiencias podrán activar las audiencias segmentadas. Las audiencias activadas se envían al destino preconfigurado del editor, como Adobe Experience Platform, para su uso en campañas. Para obtener más información sobre la configuración de destinos, consulte la guía [descripción general de destinos](../destinations/overview.md).

>[!IMPORTANT]
>
>Actualmente, cuando los anunciantes activan audiencias, se activan automáticamente en el destino configurado por el editor para su organización. El editor **debe** configurar un destino *antes de* que el anunciante active una audiencia. Si no se configura ningún destino, la audiencia se envía al editor, pero no se puede activar en ninguna campaña.

## Activar nuevas audiencias

Para empezar a activar audiencias, ve a la pestaña **[!UICONTROL Activar]** del área de trabajo del proyecto.

Seleccione el icono de agregar (![Agregar icono.](/help/assets/icons/plus.png)) o la opción **[!UICONTROL Activar audiencia]** si no se han enviado audiencias anteriores para su activación.

![El área de trabajo de activación en un proyecto sin audiencias agregadas.](/help/assets/collaborate/activate/activate-new-audiences.png)

Se abre el flujo de trabajo activar audiencias, donde puede seleccionar la audiencia que desea enviar a su colaborador. Utilice el menú desplegable para seleccionar una audiencia o buscar una audiencia específica. Para ver más información sobre las audiencias antes de realizar la selección, selecciona **[!UICONTROL Examinar audiencias]**

![Flujo de trabajo de activación de audiencia con las opciones desplegables y Examinar audiencias resaltadas.](/help/assets/collaborate/activate/audience-activation.png)

En **[!UICONTROL Examinar audiencias]**, puede ver **[!UICONTROL Recuento de identidades]**, **[!UICONTROL Identidades superpuestas]** y **[!UICONTROL Superposición %]** para cada audiencia.

![Cuadro de diálogo Examinar audiencias que muestra las audiencias disponibles.](/help/assets/collaborate/activate/browse-audiences.png)

Seleccione la audiencia que desea activar en las campañas y luego seleccione **[!UICONTROL Guardar]**. La audiencia ahora se muestra y puede ver **[!UICONTROL Recuento de identidades]**, **[!UICONTROL identidades superpuestas]** y **[!UICONTROL Superposición %]** para la audiencia seleccionada.

![Flujo de trabajo de activación de audiencia con la audiencia seleccionada mostrada.](/help/assets/collaborate/activate/audience-selected.png)

### Editar claves de coincidencia

A continuación, puede editar las claves de coincidencia de la audiencia seleccionando **[!UICONTROL Editar claves de coincidencia]** dentro de la audiencia seleccionada. Estas opciones se heredan de las selecciones de claves de coincidencia cuando se configuró inicialmente la conexión entre colaboradores. Puede eliminar las claves de coincidencia seleccionadas si no se aplican a una campaña específica, pero no puede añadir nuevas claves de coincidencia.

![Flujo de trabajo de activación de audiencia con la opción Editar claves de coincidencia resaltada.](/help/assets/collaborate/activate/edit-match-keys.png)

Se abre el cuadro de diálogo **[!UICONTROL Editar claves de coincidencia]**, donde puede desactivar las claves de coincidencia que no desee usar. Seleccione **[!UICONTROL Guardar]** para guardar los cambios.

>[!NOTE]
>
>Se debe seleccionar al menos una clave de coincidencia. En la versión actual, las únicas claves de coincidencia disponibles son **[!UICONTROL Correo electrónico con hash]**, por lo que no puede eliminar esta clave de coincidencia.

![Cuadro de diálogo Editar claves de coincidencia en el flujo de trabajo de activación de Audience.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Establecer frecuencia e intervalo de actualización de audiencia

Finalmente, establezca la frecuencia y el intervalo de fechas deseados para que la audiencia se actualice. En la versión actual, la única opción de frecuencia admitida es **[!UICONTROL Una vez]**. La frecuencia **[!UICONTROL Una vez]** significa que las audiencias se activan una sola vez y no se actualizan. La opción **[!UICONTROL Date]** se rellena automáticamente con la fecha actual.

![Flujo de trabajo de activación de audiencia con la sección Frecuencia resaltada.](/help/assets/collaborate/activate/audience-frequency.png)

Cuando esté satisfecho con las selecciones, seleccione **[!UICONTROL Activar]** para completar el flujo de trabajo. La audiencia ahora está activada y puede verla en la ficha **[!UICONTROL Activar]**. También estará disponible para sus colaboradores en la pestaña **[!UICONTROL Activar]**, donde podrán usarlo en campañas.

Puede editar el nombre o el icono de edición de la audiencia (icono ![Lápiz).](/help/assets/icons/edit.png)) o desactivar la audiencia seleccionando **[!UICONTROL Desactivar]**.

![Pestaña Activar con la audiencia activada en pantalla y las opciones Editar y Desactivar resaltadas.](/help/assets/collaborate/activate/edit-activate-audience.png)

## Ver audiencias activadas

En la ficha **[!UICONTROL Activar]**, tanto los editores como los anunciantes pueden ver las audiencias que están activadas actualmente. Actualmente, las audiencias se envían automáticamente al destino configurado del editor después de que el anunciante las active.

![Información general de la ficha Activar, que muestra una audiencia activada.](/help/assets/collaborate/activate/activate-overview.png)

Dentro de cada audiencia activada, puede ver las siguientes métricas:

| Métrica | Descripción |
|---------|----------|
| **[!UICONTROL Identidades activadas]** | Indica el número de identidades activadas dentro de la audiencia. |
| **[!UICONTROL Identidades superpuestas]** | Indica la cantidad de identidades superpuestas entre esta audiencia y la población total de perfiles en el inventario del colaborador. |
| **[!UICONTROL Desglose de clave de coincidencia]** | Muestra el recuento de identidades de cada identidad utilizada en la audiencia. Por ejemplo, un recuento total de identidades de 500 000 usuarios puede constar de 400 000 usuarios que no escriben la identidad de correo electrónico con hash y 100 000 usuarios que no escriben una identidad de ID móvil. Tenga en cuenta que, en el ejemplo descrito aquí, la misma persona podría estar presente en la audiencia dos veces con sus identidades de correo electrónico e ID móvil. |

## Pasos siguientes {#next-steps}

Después de activar los datos y ejecutar las campañas, colabore con el equipo de ingeniería y habilitación de Adobe para cargar los datos de medición y ver los [informes de medición](/help/guide/collaborate/measure.md) correspondientes.
