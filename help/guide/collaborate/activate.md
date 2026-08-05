---
title: Activar públicos
description: Obtenga información sobre cómo enviar audiencias a colaboradores y activar manualmente las audiencias recibidas a destinos en Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
TQID: https://experienceleague.adobe.com/bfPHtcW8Mf6RhIlg5fKcJmPSEKDyAODjbNRJ5D3SMkQ
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 87a7ddb5b6ef1661e347a3dd7842523639d54859
workflow-type: tm+mt
source-wordcount: 1589
ht-degree: 3%

---

# Activar públicos

Use la ficha **[!UICONTROL Activar]** de un proyecto para enviar audiencias a su colaborador, revisar las audiencias recibidas de su colaborador y activar las audiencias recibidas para enviarlas a un destino configurado. Para configurar y administrar destinos desde el área de trabajo **[!UICONTROL Activation]** de nivel superior, consulte la [descripción general de destinos](../destinations/overview.md).

>[!IMPORTANT]
>
>La ficha **[!UICONTROL Activar]** solo está disponible si el caso de uso **Activación de audiencias** se habilitó [durante el proceso de conexión](../connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte [Administrar proyectos](./manage-projects.md#project-use-cases).

Use la [pestaña Discover](./discover.md) para identificar las audiencias que mejor se ajustan a su campaña y luego envíelas a su colaborador. El colaborador receptor selecciona un destino configurado y programa la audiencia recibida para su activación.

Enviar y activar son acciones independientes. El envío proporciona a su colaborador acceso a una audiencia. A continuación, el colaborador receptor selecciona un destino y activa manualmente la audiencia recibida.

Las secciones y acciones disponibles dependen de si la organización envía o recibe audiencias en el proyecto. La ficha **[!UICONTROL Activar]** contiene las siguientes secciones:

| Sección | Descripción |
|---|---|
| **[!UICONTROL Se enviaron las audiencias a [colaborador]]** | Audiencias que ha enviado a su colaborador. |
| **[!UICONTROL Audiencias recibidas]** | Audiencias que le ha enviado su colaborador y que están disponibles para su activación. |
| **[!UICONTROL Audiencias activadas]** | Audiencias recibidas que ha activado a un destino. |

![La pestaña Activar a nivel de proyecto con recuentos de resumen en las secciones superior y audiencias enviadas y recibidas y audiencias activadas expandidas. Cada sección muestra recuentos de estado y una tabla de detalles de audiencia.](/help/assets/collaborate/activate/activate-dashboard.png)

## Requisitos previos {#prerequisites}

Antes de enviar o activar audiencias, asegúrese de lo siguiente:

- Las audiencias provienen de y están disponibles para su envío. Para obtener más información, consulte [Source y administrar audiencias](../setup/onboard-audiences.md).
- Si necesita activar las audiencias recibidas, debe configurarse como mínimo un destino. Para obtener más información, consulte la [descripción general de destinos](../destinations/overview.md).

## Enviar públicos {#send-audiences}

Envíe una audiencia para que su colaborador tenga acceso a ella. Después de enviar la audiencia, esta aparece en la sección **[!UICONTROL Audiencias enviadas al colaborador]&rbrack;** y en la sección **[!UICONTROL Audiencias recibidas]** del colaborador.&lbrack;

Vaya a **[!UICONTROL Colaborar]**, abra un proyecto y seleccione la ficha **[!UICONTROL Activar]**.

En la sección **[!UICONTROL Audiencias enviadas a [colaborador]]**, seleccione el icono de agregar (![Agregar icono.](/help/assets/icons/plus.png)). Si no se han enviado audiencias, selecciona **[!UICONTROL Enviar audiencia]** en la pantalla vacía.

![La pestaña Activar a nivel de proyecto cuando no se han enviado audiencias. El mensaje para mostrar vacío explica que no ha enviado ninguna audiencia y muestra el botón Enviar audiencia.](/help/assets/collaborate/activate/activate-new-audiences.png)

Se abre el flujo de trabajo **[!UICONTROL Enviar audiencias]**. Use el selector de audiencia para encontrar una audiencia o seleccione **[!UICONTROL Examinar audiencias]** para comparar las audiencias disponibles.

>[!IMPORTANT]
>
>Solo las audiencias con más de 1000 identidades superpuestas están disponibles para la activación. Si la superposición de audiencias está cerca del umbral de identidad de 1000, puede producirse un error de activación.

![Flujo de trabajo Enviar audiencias con un selector de audiencia y un botón Examinar audiencias. El flujo de trabajo permite que el remitente elija una audiencia antes de configurar las claves de coincidencia y la configuración de acceso.](/help/assets/collaborate/activate/audience-activation.png)

En el cuadro de diálogo **[!UICONTROL Examinar audiencias]**, revise **[!UICONTROL Recuento de identidades]**, **[!UICONTROL Identidades superpuestas]** y **[!UICONTROL Superposición %]** para cada audiencia.

![El cuadro de diálogo Examinar audiencias enumera las audiencias disponibles con su recuento de identidades, recuento de identidades superpuesto y porcentaje de superposición.](/help/assets/collaborate/activate/browse-audiences.png)

>[!IMPORTANT]
>
>Si una audiencia utiliza varias claves de coincidencia, cada clave de coincidencia seleccionada debe alcanzar el umbral de superposición requerido. Use la [pestaña Discover](./discover.md) para confirmar que la audiencia cumple los requisitos de superposición antes de enviarla.

Seleccione la audiencia que desee enviar y, a continuación, seleccione **[!UICONTROL Guardar]**.

La audiencia seleccionada aparece en el flujo de trabajo con su identidad e información de superposición.

![Flujo de trabajo Enviar audiencias con una audiencia seleccionada que muestra su recuento de identidades, recuento de identidades superpuesto, porcentaje de superposición, claves de coincidencia y opción Editar claves de coincidencia.](/help/assets/collaborate/activate/audience-selected.png)

### Editar claves de coincidencia {#edit-match-keys}

Utilice las claves de coincidencia configuradas para la conexión de colaborador o elimine las claves de coincidencia que no se apliquen a la audiencia.

Seleccione **[!UICONTROL Editar claves de coincidencia]** en la audiencia seleccionada.

![La audiencia seleccionada en el flujo de trabajo Enviar audiencias con la opción Editar claves de coincidencia resaltada.](/help/assets/collaborate/activate/edit-match-keys.png)

Aparecerá el cuadro de diálogo **[!UICONTROL Editar claves de coincidencia]**. Desactive las claves de coincidencia que no desee usar y, a continuación, seleccione **[!UICONTROL Guardar]**.

>[!NOTE]
>
>Debe permanecer seleccionada al menos una clave de coincidencia.

![Cuadro de diálogo Editar claves de coincidencia con controles de alternancia para las claves de coincidencia disponibles a través de la conexión de colaborador y un botón Guardar.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Configuración del acceso a audiencias {#configure-audience-access}

Configure cómo se envía la audiencia y cuánto tiempo puede acceder a ella su colaborador.

Utilice el control **[!UICONTROL Duración del acceso]** para seleccionar una de las opciones siguientes:

- **[!UICONTROL Enviar ahora (solo una vez)]**: Envíe la audiencia una vez. El colaborador receptor puede activarlo una vez.
- **[!UICONTROL Programar envío recurrente de audiencia]**: Actualice la audiencia durante un período de acceso especificado. Utilice el control **[!UICONTROL Intervalo de fechas]** para seleccionar las fechas de inicio y finalización.

![El paso Duración del acceso en el flujo de trabajo Enviar audiencias con opciones para enviar la audiencia una vez o programar un envío recurrente de la audiencia. La opción recurrente muestra los controles de fecha para definir el período de acceso.](/help/assets/collaborate/activate/activation-frequency.png)

Una vez completada la configuración de audiencia y acceso, seleccione **[!UICONTROL Enviar]**.

La audiencia aparece en la sección **[!UICONTROL Audiencias enviadas al [colaborador]]**. Su colaborador puede revisarlo en la sección **[!UICONTROL Audiencias recibidas]**.

## Ver audiencias enviadas {#view-sent-audiences}

Utilice la sección **[!UICONTROL Audiencias enviadas a [colaborador]]** para revisar las audiencias que ha enviado y supervisar su estado de acceso actual.

Cada audiencia enviada muestra la siguiente información:

| Columna | Descripción |
|---|---|
| **[!UICONTROL Nombre de audiencia]** | Nombre de la audiencia enviada. |
| **[!UICONTROL Estado]** | El estado de acceso actual de la audiencia. |
| **[!UICONTROL Recuento de identidad]** | Número de identidades de la audiencia. |
| **[!UICONTROL Identidades superpuestas]** | Número de identidades que se superponen con el inventario del colaborador. |
| **[!UICONTROL Creado]** | La fecha y la hora en que se envió la audiencia por primera vez. |
| **[!UICONTROL Último envío]** | La fecha y la hora en que los datos de audiencia se enviaron más recientemente a su colaborador. |
| **[!UICONTROL Duración del acceso]** | La configuración de acceso establecida cuando se envió la audiencia. |
| **[!UICONTROL Claves coincidentes]** | Las claves de coincidencia utilizadas al enviar la audiencia. |

### Eliminar una audiencia enviada {#delete-sent-audience}

Elimine una audiencia enviada para eliminarla de la lista de audiencias enviadas y revoque el acceso de su colaborador.

Seleccione el icono de eliminación (![Eliminar icono.](/help/assets/icons/delete.png)) junto a la audiencia en la sección **[!UICONTROL Audiencias enviadas a [colaborador]]**.

![La sección Audiencias enviadas con el icono de eliminación mostrado junto a una fila de audiencia.](/help/assets/collaborate/activate/delete-sent-audiences.png)

Aparecerá un cuadro de diálogo de confirmación. Seleccione **[!UICONTROL Eliminar]** para confirmar.

![Cuadro de diálogo de confirmación de eliminación de audiencia enviada que explica que se eliminará la audiencia y que el colaborador perderá el acceso, con los botones Cancelar y Eliminar.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

La audiencia se elimina de la sección y el colaborador pierde el acceso a ella.

## Ver audiencias recibidas {#received-audiences}

Utilice la sección **[!UICONTROL Audiencias recibidas]** para revisar las audiencias que le ha enviado su colaborador. Una audiencia recibida debe activarse manualmente antes de enviar sus datos a un destino.

Cada audiencia recibida muestra la siguiente información:

| Columna | Descripción |
|---|---|
| **[!UICONTROL Nombre de audiencia]** | Nombre de la audiencia recibida. |
| **[!UICONTROL Estado]** | El estado de acceso actual de la audiencia. |
| **[!UICONTROL Recuento de identidad]** | Número de identidades de la audiencia. |
| **[!UICONTROL Identidades superpuestas]** | El número de identidades que se superponen con el inventario. |
| **[!UICONTROL Última ejecución de flujo de datos]** | La fecha y la hora de la ejecución del flujo de datos más reciente para la audiencia. |
| **[!UICONTROL Duración del acceso]** | La configuración de acceso configurada por el colaborador que envió la audiencia. |
| **[!UICONTROL Claves coincidentes]** | Las claves de coincidencia utilizadas para la audiencia. |

![La sección Audiencias recibidas con recuentos de público activos y caducados. Cada fila de audiencia muestra su nombre, estado, información de identidad, última ejecución del flujo de datos, duración del acceso, claves de coincidencia y un icono de agregar que se utilizó para iniciar la activación.](/help/assets/collaborate/activate/received-audiences-section.png)

### Activar una audiencia recibida {#activate-received-audience}

Active una audiencia recibida para enviar sus datos a uno de los destinos configurados.

En la sección **[!UICONTROL Audiencias recibidas]**, seleccione el icono Agregar (![Agregar icono.](/help/assets/icons/plus.png)) junto a la audiencia que desea activar.

Aparecerá el cuadro de diálogo **[!UICONTROL Activar audiencia]**.

Use **[!UICONTROL Destino]** para seleccionar el destino que recibe los datos de audiencia. Si la lista de destinos está vacía, configure un destino antes de continuar. Para obtener instrucciones, consulte la [descripción general de destinos](../destinations/overview.md).

Use **[!UICONTROL Fecha]** para seleccionar la fecha en la que se ejecutará la activación y, a continuación, seleccione **[!UICONTROL Activar]**.

![El cuadro de diálogo Activar audiencia se abrió desde una audiencia recibida. El cuadro de diálogo contiene un menú desplegable Destino para seleccionar un destino configurado, un campo Fecha con un control de calendario y los botones Cancelar y Activar.](/help/assets/collaborate/activate/activate-received-audience.png)

El cuadro de diálogo se cierra y la activación aparece en la sección **[!UICONTROL Audiencias activadas]**. La audiencia recibida permanecerá disponible en la sección **[!UICONTROL Audiencias recibidas]** mientras su acceso permanezca activo.

## Ver audiencias activadas {#activated-audiences}

Utilice la sección **[!UICONTROL Audiencias activadas]** para confirmar qué audiencias recibidas se han activado y revisar su destino y estado de envío.

Cada audiencia activada muestra la siguiente información:

| Columna | Descripción |
|---|---|
| **[!UICONTROL Nombre de audiencia]** | Nombre de la audiencia activada. |
| **[!UICONTROL Estado]** | El estado de activación actual. |
| **[!UICONTROL Recuento activado]** | El número de identidades activadas en el destino. |
| **[!UICONTROL Última actualización]** | La fecha y la hora en que se actualizó la audiencia activada más recientemente. |
| **[!UICONTROL Destino]** | Destino que recibe los datos de audiencia. |
| **[!UICONTROL Frecuencia]** | La frecuencia de activación. Las activaciones manuales se muestran **[!UICONTROL Una vez]**. |
| **[!UICONTROL Fecha]** | La fecha en la que se ejecuta la activación. |
| **[!UICONTROL Claves coincidentes]** | Las claves de coincidencia incluidas en la audiencia activada. |

![La sección Audiencias activadas con recuentos de activación activos, archivados y pausados. Cada fila muestra el nombre de la audiencia, el estado, el recuento activado, la fecha de la última actualización, el destino, la frecuencia, la fecha de activación, las claves de coincidencia y un icono de eliminación.](/help/assets/collaborate/activate/activated-audiences-section.png)

### Eliminar una audiencia activada {#delete-activated-audience}

Elimine una audiencia activada para eliminar la activación de la sección **[!UICONTROL Audiencias activadas]**.

Seleccione el icono de eliminación (![Eliminar icono.](/help/assets/icons/delete.png)) junto a la audiencia activada.

Aparecerá un cuadro de diálogo de confirmación. Seleccione **[!UICONTROL Eliminar]** para confirmar.

![Cuadro de diálogo de confirmación de eliminación de audiencia activada que explica que la audiencia se eliminará de la lista de audiencias activadas y que se podrá activar de nuevo más tarde, con los botones Cancelar y Eliminar.](/help/assets/collaborate/activate/delete-activated-audience-confirmation.png)

La activación se elimina de la lista. Puede volver a activar la audiencia recibida mientras su acceso permanezca activo.

## Próximos pasos {#next-steps}

Después de enviar o activar audiencias, monitorice su estado en las secciones **[!UICONTROL Audiencias enviadas a [colaboradores]]** y **[!UICONTROL Audiencias activadas]**. Una vez finalizadas las campañas, trabaje con el equipo de ingeniería y habilitación de Adobe para cargar los datos de medición y ver los [informes de medición](./measure.md) correspondientes.
