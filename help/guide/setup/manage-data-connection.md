---
title: Administrar conexiones de datos
description: Obtenga información sobre cómo administrar conexiones de datos, incluidas claves de coincidencia, programación, casos de uso y filtrado de audiencias en Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 4%

---

# Administrar conexiones de datos

{{limited-availability-release-note}}

## Información general

Utilice conexiones de datos en Real-Time CDP Collaboration para importar audiencias de varias fuentes. Obtenga información sobre cómo administrar las claves de coincidencia y programar las importaciones de datos para las conexiones de datos existentes. Además, podrá filtrar audiencias por atributos diferentes para obtener perspectivas más granulares.

Antes de administrar las conexiones de datos aquí, debe configurarlas inicialmente durante el [flujo de trabajo de incorporación de audiencias](./onboard-audiences.md). Esto garantizará que las fuentes de datos correctas estén conectadas para su uso en Real-Time CDP Collaboration.

## Ver conexiones de datos

>[!IMPORTANT]
>
>En este momento no se admite la eliminación de una conexión de datos en la interfaz de usuario de Real-Time CDP Collaboration. Para eliminar una conexión de datos, comuníquese con su representante de Adobe o [cree un ticket de atención al cliente](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=open-ticket#support){target="_blank"}.

Para ver las conexiones de datos existentes, vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Mis audiencias]** y seleccione **[!UICONTROL Administrar conexiones de datos]**.

![Espacio de trabajo de instalación con Administrar conexiones de datos resaltadas.](/help/assets/setup/manage-data-connection/manage-data-connection-highlighted.png){zoomable="yes"}

Esto abre una vista de todas las conexiones de datos configuradas actualmente, con información sobre la cantidad de audiencias en cada una de ellas, el origen de la conexión de datos y más. Seleccione **[!UICONTROL Ver conexión de datos]** para ver información sobre las claves de coincidencia, la programación y las audiencias que forman parte de esta conexión de datos.

![Administrar área de trabajo de conexiones de datos con conexiones Ver conexiones de datos resaltadas. ](/help/assets/setup/manage-data-connection/view-data-connection-highlighted.png){zoomable="yes"}

### Claves de coincidencia {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia determinan cómo se compararán los datos de diferentes fuentes. Elija las claves de coincidencia más relevantes para sus casos de uso y directrices de privacidad."

Las claves de coincidencia son identificadores utilizados para reconciliar miembros entre audiencias de diferentes fuentes de datos. Las claves de coincidencia disponibles incluyen:

- **Correo electrónico con hash**

No puede editar las claves de coincidencia utilizadas en esta conexión de datos.

![Espacio de trabajo de conexiones de datos con la sección Claves de coincidencia resaltada.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Programación {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Programación"
>abstract="Esta vista muestra las opciones de programación seleccionadas inicialmente para la conexión de datos."

No puede editar las opciones de programación seleccionadas inicialmente para la conexión de datos. Para obtener más información acerca de las opciones de programación, vea la [sección de programación](/help/guide/setup/onboard-audiences.md#schedule) en el documento de flujo de trabajo de importación de audiencia.

![Área de trabajo de conexiones de datos con la sección Programación resaltada.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Administrar audiencias {#manage-audiences}

Al ver la lista de audiencias desde la conexión de datos, puede seleccionar ver las audiencias, editar sus categorías o eliminarlas de la conexión de datos.

![Espacio de trabajo de conexiones de datos con las audiencias resaltadas.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Pasos siguientes

Después de administrar las conexiones de datos, puede [descubrir superposiciones](/help/guide/collaborate/discover.md) entre sus audiencias y las audiencias que su colaborador ha hecho reconocibles.
