---
title: Administrar conexiones de datos
description: Aprenda a administrar las conexiones de datos, incluidas las claves de coincidencia, la programación, los casos de uso y el filtrado de audiencia en Real-Time CDP Collaboration
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

Utilice las conexiones de datos en Real-Time CDP Collaboration para importar audiencias de diversas fuentes. Aprenda a administrar claves de coincidencia y programar importaciones de datos para sus conexiones de datos existentes. Además, podrá filtrar audiencias por diferentes atributos para obtener información más granular.

Antes de administrar sus conexiones de datos aquí, inicialmente debe configurarlas durante el flujo de trabajo de incorporación audiencia[](./onboard-audiences.md). Esto garantizará que las fuentes de datos correctas estén conectadas para su uso en Real-Time CDP Collaboration.

## Ver conexiones de datos

>[!IMPORTANT]
>
>Actualmente, la eliminación de una conexión de datos no se admite en la interfaz de usuario de colaboración de CDP en tiempo real. Para eliminar una conexión de datos, póngase en contacto con su representante de Adobe o [cree un ticket](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=open-ticket#support){target="_blank"} con el servicio de atención al cliente.

Para vista las conexiones de datos existentes, vaya a **[!UICONTROL Configuración > Mis audiencias]** y seleccione **[!UICONTROL Administrar]** conexiones ]**de**[!UICONTROL  datos.

![Instale espacio de trabajo con la opción Administrar conexiones de datos resaltada.](/help/assets/setup/manage-data-connection/manage-data-connection-highlighted.png){zoomable="yes"}

Esto brinda una vista de todas sus conexiones de datos configuradas actualmente, con información sobre el número de audiencias en cada una de ellas, el origen de la conexión de datos y más. Seleccione **[!UICONTROL Ver conexión]** de datos para vista información sobre las claves de coincidencia, la programación y las audiencias que forman parte de esta conexión de datos.

![Administre las conexiones de datos espacio de trabajo con una Ver de conexiones de datos resaltadas. ](/help/assets/setup/manage-data-connection/view-data-connection-highlighted.png){zoomable="yes"}

### Claves de coincidencia {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Claves de coincidencia"
>abstract="Las claves de coincidencia determinan cómo se emparejarán los datos de diferentes fuentes. Elija las claves de coincidencia que sean más relevantes para sus casos de uso y directrices de privacidad."

Las claves de coincidencia son identificadores que sirven para reconciliar miembros entre audiencias de distintos orígenes de datos. Las claves de coincidencia disponibles incluyen:

- **correo electrónico con hash**

No puede editar las claves de coincidencia utilizadas en esta conexión de datos.

![Se espacio de trabajo una conexión de datos con la sección Claves de coincidencia resaltada.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Programación {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Programación"
>abstract="Este vista muestra las opciones de programación que seleccionó inicialmente para la conexión de datos."

No puede editar las opciones de programación que seleccionó inicialmente para la conexión de datos. Para obtener más información acerca de las opciones de programación, vista la [sección](/help/guide/setup/onboard-audiences.md#schedule) de programación del documento de importación flujo de trabajo audiencia.

![Un espacio de trabajo de conexiones de datos con la sección Programación resaltada.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Administrar audiencias {#manage-audiences}

Al ver el lista de audiencias desde la conexión de datos, puede seleccionar vista las audiencias, editar sus categorías o eliminarlas de la conexión de datos.

![Una conexión de datos espacio de trabajo con las audiencias resaltadas.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Pasos siguientes

Después de administrar sus conexiones de datos, puede [descubrir superposiciones](/help/guide/collaborate/discover.md) entre sus audiencias y las audiencias que su colaborador ha hecho detectables.
