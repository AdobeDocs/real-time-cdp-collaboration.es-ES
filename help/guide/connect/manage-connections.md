---
title: Administrar conexiones
description: Obtenga información sobre cómo administrar las conexiones en Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 50120839-4a20-4ec1-8887-9342bd17c52d
source-git-commit: 46d2596bd0ccdc5da32067493968945c61f8acc4
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 1%

---

# Administrar conexiones {#manage-connections}

{{limited-availability-release-note}}

El área de trabajo **[!UICONTROL Mis conexiones]** proporciona una ubicación centralizada para administrar las conexiones. Puede ver las conexiones existentes en la sección **[!UICONTROL Conexiones existentes]** y ver las conexiones que requieran acción en la sección **[!UICONTROL Acción necesaria]**.

## Ver conexión {#view-connection}

Para ver las conexiones existentes, ve al área de trabajo **[!UICONTROL Connect]**. Como editor, se mostrará la conexión existente. Como anunciante, deberías ir a **[!UICONTROL Mis conexiones]**.

![Opción Ver conexión resaltada para una conexión en el área de trabajo Mis conexiones.](/help/assets/connect/manage-connections/view-connection.png){zoomable="yes"}

Aparece el área de trabajo de información general de conexión, que muestra detalles acerca de la conexión y sus proyectos activos. Seleccione **[!UICONTROL Configuración de conexión]** para ver la configuración de conexión.

![La opción de configuración de conexión resaltada en el área de trabajo de información general de conexión.](/help/assets/connect/manage-connections/connection-overview.png){zoomable="yes"}

Aparecerá el espacio de trabajo de configuración de conexión, que muestra los detalles de conexión entre usted y su colaborador. Aquí puede ver todos los ajustes seleccionados durante el proceso de conexión, el estado actual de la conexión, el propietario de la conexión y la información de contacto de su colaborador. Para obtener información sobre la configuración de conexión específica, consulte la guía [configuración de conexión](/help/guide/connect/establishing-connections.md#connection-settings).

![Espacio de trabajo de configuración de conexión que muestra detalles de conexión.](/help/assets/connect/manage-connections/connection-settings.png){zoomable="yes"}

## Eliminar conexión {#delete-connection}

Puede eliminar cualquier conexión con colaboradores con los que no desee seguir trabajando. Para eliminar una conexión, navegue hasta la conexión que desee eliminar y, a continuación, seleccione el icono Eliminar ![icono Eliminar](/help/assets/common/delete.svg) en el área de trabajo de conexión.

![Icono de eliminación resaltado en el área de trabajo de conexión.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

Aparecerá un cuadro de diálogo de confirmación en el que se le pedirá que confirme la eliminación de la conexión. Seleccione **[!UICONTROL Eliminar]** para confirmar la eliminación.

![Cuadro de diálogo de confirmación para eliminar una conexión.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Una vez eliminada la conexión, todos los proyectos existentes en la colaboración se eliminarán de forma permanente y no se recuperarán. La solicitud de conexión permanecerá en estado pendiente en la sección **[!UICONTROL Acción necesaria]** dentro de **[!UICONTROL Mis conexiones]**, pero la conexión y sus configuraciones dejarán de estar activas. Deberá restablecer la conexión si desea volver a conectarse con el colaborador.

## Editar conexión {#edit-connection}

Como propietario de una conexión de colaboración, puede editar la configuración de conexión con su colaborador una vez establecida la conexión. Puede hacer lo siguiente:

* Añadir casos de uso
* Añadir claves de coincidencia. La eliminación de la clave de coincidencia será compatible en el futuro.
* Actualizar permisos de activación de audiencia
* Actualizar configuración de división de crédito

>[!IMPORTANT]
>
>Una vez que se añade un caso de uso o una clave de coincidencia a una conexión, no se puede eliminar.

>[!TIP]
>
>El **propietario** es el colaborador que inicia la conexión al enviar la invitación al **destinatario**. Para obtener más información, consulte la [documentación sobre el establecimiento de conexiones con colaboradores](./establishing-connections.md).

Para editar la configuración de conexión, vaya al área de trabajo de configuración de conexión. Seleccione el icono de tres puntos (![Icono de tres puntos.](/help/assets/icons/more.png)) para ver las acciones disponibles y, a continuación, seleccione **[!UICONTROL Editar]**.

![Espacio de trabajo de configuración de conexión con la opción Editar resaltada.](/help/assets/connect/manage-connections/edit-connection.png){zoomable="yes"}

Aparece un cuadro de diálogo que le solicita que edite y envíe los cambios de configuración para que los revise el colaborador. Seleccione **[!UICONTROL Editar]**.

![Cuadro de diálogo Editar configuración de conexión con la opción Editar resaltada.](/help/assets/connect/manage-connections/edit-connection-settings-dialog.png){zoomable="yes"}

### Editar activación de audiencia {#edit-audience-activation}

La configuración de activación de audiencias determina qué colaborador de la conexión puede activar audiencias en los destinos. Para cambiar esta configuración, seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Activación de audiencia]**.

![Pantalla de edición de la configuración de conexión que muestra la sección de activación de Audiencia y la opción Editar.](/help/assets/connect/manage-connections/edit-audience-activation.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL Activación de audiencia]**, utilice el menú desplegable para actualizar los permisos de activación de audiencia. Puede elegir un solo colaborador o permitir que ambos activen audiencias.

![Se ha expandido el menú desplegable resaltado del cuadro de diálogo de activación de audiencia para actualizar los permisos de activación de audiencia.](/help/assets/connect/manage-connections/audience-activation-dropdown-menu.png){zoomable="yes"}

Una vez finalizado, seleccione **[!UICONTROL Guardar]**.

![Cuadro de diálogo de activación de audiencia que muestra los nuevos permisos de activación de audiencia y la opción Guardar.](/help/assets/connect/manage-connections/audience-activation-dialog.png){zoomable="yes"}

### Añadir casos de uso {#add-use-cases}

En Collaboration, casos de uso como Discover, Activar y Medida determinan qué secciones y funciones del proyecto puede utilizar con su colaborador. Puede agregar casos de uso adicionales a una conexión existente para proyectos futuros. Para obtener más información, vea [casos de uso de colaboración](../overview/use-cases.md).

Para agregar nuevos casos de uso, seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Casos de uso]**.

![La pantalla Editar configuración de conexión resalta la sección Casos de uso y la opción Editar.](/help/assets/connect/manage-connections/edit-use-cases.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL Casos de uso]**, active los nuevos casos de uso que desee agregar, seguidos de **[!UICONTROL Guardar]**.

![El cuadro de diálogo Casos de uso muestra resaltada la opción Guardar.](/help/assets/connect/manage-connections/use-cases-dialog.png){zoomable="yes"}

>[!NOTE]
>
>Cuando [agrega nuevos casos de uso](#add-use-cases), como &quot;Activación de audiencia&quot; o &quot;Medición&quot;, la pantalla Editar configuración de conexión se actualiza para incluir las secciones **[!UICONTROL Activación de audiencia]** y **[!UICONTROL División de crédito]**. Debe configurar las opciones adecuadas para estos nuevos casos de uso. Para obtener más información, consulte las guías de [activación de audiencia](../connect/establishing-connections.md#audience-activation) y [división de crédito](../connect/establishing-connections.md#credit-split).
>
>![La pantalla Editar configuración de conexión muestra las secciones Activación de audiencia y División de crédito después de agregar nuevos casos de uso.](/help/assets/connect/manage-connections/setup-audience-activation-credit-split.png){zoomable="yes"}

### Añadir claves de coincidencia {#add-match-keys}

Solo las claves de coincidencia configuradas en su cuenta y seleccionadas por su colaborador están disponibles para la conexión. Una vez que [agregue nuevas claves de coincidencia a su cuenta](../setup/onboard-account.md#edit-match-keys) y su colaborador también seleccione las mismas claves, puede habilitarlas en sus conexiones existentes.

En la pantalla Editar configuración de conexión, seleccione **[!UICONTROL Editar]** en la sección **[!UICONTROL Claves de coincidencia]**.

![La pantalla Editar configuración de conexión resalta la sección Claves de coincidencia y la opción Editar.](/help/assets/connect/manage-connections/edit-connection-match-keys.png){zoomable="yes"}

Aparece un cuadro de diálogo **[!UICONTROL Claves de coincidencia]** que muestra las claves de coincidencia existentes configuradas para la conexión. Seleccione las claves de coincidencia que desee agregar, seguidas de **[!UICONTROL Guardar]**.

![El cuadro de diálogo Coincidir claves muestra las nuevas claves de coincidencia seleccionadas y la opción Guardar.](/help/assets/connect/manage-connections/connection-match-keys-dialog.png){zoomable="yes"}

### Editar división de crédito {#edit-credit-split}

La configuración de división de crédito especifica qué colaborador es responsable de los costes asociados con cada caso de uso en la conexión. Para actualizar esta configuración, selecciona **[!UICONTROL Editar]** en la sección **[!UICONTROL División de crédito]**.

![La pantalla Editar configuración de conexión resalta la sección División de crédito y la opción Editar.](/help/assets/connect/manage-connections/edit-credit-split.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL División de crédito]**, seleccione la configuración preferida para [!UICONTROL Coincidencia de activación] y [!UICONTROL Medición]. A continuación, seleccione **[!UICONTROL Guardar]** para confirmar.

![Cuadro de diálogo de división de crédito que muestra la configuración de división de crédito y la opción Guardar.](/help/assets/connect/manage-connections/credit-split-dialog.png){zoomable="yes"}

### Revisar y enviar cambios {#review-and-submit-changes}

Cuando termine de editar la configuración de conexión, revise y seleccione **[!UICONTROL Enviar cambios]**. Las actualizaciones de la configuración de conexión se enviarán a su colaborador para que las revise.

![La pantalla Editar configuración de conexión muestra las actualizaciones y la opción Enviar cambios.](/help/assets/connect/manage-connections/review-and-submit-changes.png){zoomable="yes"}

#### Guardar cambios de configuración de conexión como borrador

Puede guardar los cambios de configuración de la conexión como borrador y volver para finalizar la actualización de la configuración de la conexión en cualquier momento.

Para guardar los cambios como borrador, seleccione **[!UICONTROL Cancelar]** junto a **[!UICONTROL Enviar cambios]**. A continuación, en el cuadro de diálogo **[!UICONTROL Cambios no enviados]**, seleccione **[!UICONTROL Continuar más tarde]** para confirmar.

![Pantalla de edición de configuración de conexión.](/help/assets/connect/manage-connections/unsubmitted-changes-dialog.png){zoomable="yes"}

Los cambios se guardarán como borrador. En el área de trabajo de configuración de conexión, puede ver una notificación que indica que hay cambios no enviados. Para hacer más actualizaciones, selecciona **[!UICONTROL Continuar editando]**.

![Notificación en el área de trabajo de configuración de conexión que muestra cambios no enviados pendientes de revisión y envío.](/help/assets/connect/manage-connections/continue-editing-connection.png){zoomable="yes"}
