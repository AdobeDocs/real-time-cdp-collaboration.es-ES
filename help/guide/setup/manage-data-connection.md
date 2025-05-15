---
title: Administrar conexiones de datos
description: Obtenga información sobre cómo administrar conexiones de datos, incluidas claves de coincidencia, programación, casos de uso y filtrado de audiencias en Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: 8d620828bb0fb0bf116396f884b1bbd35d7c5d69
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 16%

---

# Administrar conexiones de datos

{{limited-availability-release-note}}

## Información general

Utilice conexiones de datos en Real-Time CDP Collaboration para importar audiencias de varias fuentes. Obtenga información sobre cómo administrar las claves de coincidencia y programar las importaciones de datos para las conexiones de datos existentes. Además, podrá filtrar audiencias por atributos diferentes para obtener perspectivas más granulares.

## Ver conexiones de datos

Para ver las conexiones de datos existentes, vaya a **[!UICONTROL Configuración]** y, a continuación, seleccione la pestaña **[!UICONTROL Mis conexiones de datos]**. Se muestran todas las conexiones de datos actuales, con una breve descripción general de cada conexión. Para obtener una vista completa de la información de una conexión de datos, incluidas sus claves de coincidencia, detalles de programación y audiencias, seleccione **[!UICONTROL Ver conexión de datos]** en la conexión correspondiente.

![Configurar el área de trabajo con la vista de la ficha Mis conexiones de datos mostrada y resaltada.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Claves de coincidencia {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia determinan cómo se compararán los datos de diferentes fuentes. Elija las claves de coincidencia más relevantes para sus casos de uso y directrices de privacidad."

Las claves de coincidencia son identificadores que se utilizan para reconciliar miembros entre los públicos de diferentes fuentes de datos. No puede editar las claves de coincidencia seleccionadas inicialmente para la conexión de datos.

Las claves de coincidencia disponibles incluyen:

- **Correo electrónico con hash**

![Espacio de trabajo de conexiones de datos con la sección Claves de coincidencia resaltada.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Programación {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Programación"
>abstract="Esta vista muestra las opciones de programación seleccionadas inicialmente para la conexión de datos."

No puede editar las opciones de programación seleccionadas inicialmente para la conexión de datos. Para obtener más información acerca de las opciones de programación, vea la [sección de programación](/help/guide/setup/onboard-audiences.md#schedule) en el documento de flujo de trabajo de importación de audiencia.

![Área de trabajo de conexiones de datos con la sección Programación resaltada.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Eliminar conexión de datos

Al eliminar una conexión de datos, se eliminarán todas las audiencias subyacentes, la configuración asociada y el uso en toda la plataforma. Esta acción no se puede deshacer.

Para eliminar una conexión de datos existente, seleccione el icono Eliminar (![Eliminar icono](/help/assets/common/delete.svg)) en el área de trabajo de una conexión de datos individual.

![Área de trabajo de conexiones de datos con la opción de eliminación resaltada.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

Aparecerá un cuadro de diálogo de confirmación. Seleccione **[!UICONTROL Eliminar]** para finalizar la eliminación de la conexión de datos.

![Cuadro de diálogo Eliminar conexión de datos con la opción Eliminar resaltada.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Administrar audiencias {#manage-audiences}

En la parte inferior del espacio de trabajo se muestra una lista de audiencias adjuntas a la conexión de datos. La lista muestra una breve descripción general de cada audiencia, incluido su estado, origen y acceso a la conexión. Para editar las categorías de audiencia, el acceso a conexiones o la visibilidad de metadatos de una audiencia, seleccione el nombre de la audiencia. Para obtener una guía completa sobre cómo administrar una audiencia, consulte la guía [ver audiencias individuales](./onboard-audiences.md#view-individual-audiences).

![Espacio de trabajo de conexiones de datos con las audiencias resaltadas.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Pasos siguientes

Después de administrar las conexiones de datos, puede [descubrir superposiciones](/help/guide/collaborate/discover.md) entre sus audiencias y las audiencias que su colaborador ha hecho reconocibles.
