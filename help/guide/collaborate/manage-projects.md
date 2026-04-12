---
title: Creación y administración de proyectos
description: Obtenga información sobre cómo crear y administrar proyectos en Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: ae492846-bc0a-4422-86ca-577bcc1fa60c
source-git-commit: 0cf888e36ffc4730fc8de4d8adccae0e0fc2caa8
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 13%

---

# Creación y administración de proyectos

{{limited-availability-release-note}}

Los proyectos son la pieza central del flujo de trabajo en Adobe Real-Time CDP Collaboration. Después de conectar con los colaboradores, cree un proyecto para ejecutar cálculos de superposición de audiencias y descubrir audiencias relevantes para las campañas.

>[!TIP]
>
>Los proyectos deben asociarse generalmente a una sola campaña.

![Panel de colaboración que muestra todos los proyectos actuales.](/help/assets/collaborate/manage-view-projects/projects-overview-page.png){zoomable="yes"}

Puede utilizar filtros para ver únicamente los proyectos que ha iniciado con ciertos colaboradores, como se muestra a continuación:

![Vista filtrada de proyectos con un solo colaborador.](/help/assets/collaborate/manage-view-projects/filtered-project-view.png){zoomable="yes"}

## Crear proyecto {#create-project}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_create_project_advertisername_amc"
>title="Nombre del anunciante (Amazon Marketing Cloud)"
>abstract="Para las conexiones de Amazon Marketing Cloud (AMC), este campo representa la instancia de AMC a la que tiene acceso su inicio de sesión en Amazon Ads. No refleja el nombre de un anunciante. Si la instancia necesaria no aparece en la lista, póngase en contacto con el administrador de Amazon Marketing Cloud para solicitar acceso."

Para crear un proyecto, primero debe [establecer una conexión](/help/guide/connect/establishing-connections.md) con un colaborador. Una vez establecida la conexión, puede crear un proyecto con ese colaborador.

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_projects_advertisername"
>title="Nombre del anunciante"
>abstract="Seleccione el nombre del anunciante en el menú desplegable. El editor preconfigura las opciones en la configuración de conexión para garantizar la compatibilidad con sus sistemas."

Vaya a **[!UICONTROL Colaborar]** y luego a **[!UICONTROL Mis proyectos]**. Si este es su primer proyecto, puede seleccionar **[!UICONTROL Crear un proyecto]**. De lo contrario, puede seleccionar el icono Agregar (![Agregar icono.](/help/assets/icons/plus.png)) para crear un nuevo proyecto en cualquier momento.

![Seleccione el símbolo más o cree un proyecto para configurar un nuevo proyecto.](/help/assets/collaborate/manage-view-projects/create-project.png){zoomable="yes"}

Aparecerá el cuadro de diálogo **[!UICONTROL Crear proyecto]**. Seleccione el **[!UICONTROL colaborador]** con el que está creando el proyecto a través de la lista desplegable. Si eres editor y estableces nombres de anunciante durante la configuración de la conexión, puedes seleccionar **[!UICONTROL Nombre del anunciante]**.

>[!NOTE]
>
> Si ha configurado un solo nombre de anunciante en la configuración de conexión, aparecerá de forma predeterminada. Si no se configuró ningún nombre de anunciante, el **[!UICONTROL Nombre]** del anunciante se preseleccionará como **[!UICONTROL Nombre del anunciante]**.

![Cuadro de diálogo Crear proyecto con el colaborador seleccionado y el nombre del anunciante resaltado.](/help/assets/collaborate/manage-view-projects/create-project-advertiser-names.png){zoomable="yes"}

A continuación, agrega un **[!UICONTROL nombre de proyecto]** y **[!UICONTROL Descripción]** para tu proyecto. A continuación, seleccione una imagen para representar el proyecto. Esta imagen ayuda a distinguir el proyecto en la página de información general del proyecto. Una vez que hayas terminado, selecciona **[!UICONTROL Crear]** para crear el proyecto.

![Opciones requeridas para configurar un nuevo proyecto](/help/assets/collaborate/manage-view-projects/create-project-required-info.png){zoomable="yes"}

Ahora puede ver el nuevo proyecto, sus detalles y las secciones disponibles en función de los casos de uso seleccionados durante la configuración de la conexión.

![Espacio de trabajo de descripción general del proyecto.](/help/assets/collaborate/manage-view-projects/project-overview.png){zoomable="yes"}

## Administrar ID de campaña {#manage-campaign-id}

Un **identificador de campaña** vincula el proyecto con una campaña específica y es necesario para [generar informes de medición](./measure.md#create-measurement-report). Puede añadir varios ID de campaña a un proyecto si ejecuta varias campañas con el mismo colaborador. Todas estas campañas están disponibles para su selección en los informes.

- **Publicadores**: escriba o actualice los identificadores de campaña y los nombres asociados en la interfaz de usuario de Collaboration antes de ejecutar los informes.
- **Anunciantes**: Solicite a su colaborador (editor) que agregue los identificadores de campaña según sea necesario.

Para agregar o actualizar las ID de campaña, vaya al área de trabajo **[!UICONTROL Colaborar]** y, a continuación, seleccione **[!UICONTROL Ver]** en la tarjeta de proyecto correspondiente.

![Área de trabajo de colaboración que resalta la opción Ver en una tarjeta de proyecto.](/help/assets/collaborate/manage-view-projects/view-project.png){zoomable="yes"}

El área de trabajo **[!UICONTROL Información general del proyecto]** correspondiente aparece con una sección **[!UICONTROL Nombre e ID de campaña]** que enumera todas las campañas vinculadas al proyecto. Si aún no ha agregado una campaña, seleccione **[!UICONTROL Agregar]**. Si ya hay campañas presentes, selecciona **[!UICONTROL Editar]** para actualizar los detalles o agregar más.

![Área de trabajo de información general del proyecto que muestra la sección ID de campaña y nombre con la opción Editar resaltada.](/help/assets/collaborate/manage-view-projects/edit-campaign-id.png){zoomable="yes"}

En el cuadro de diálogo **[!UICONTROL Nombre e ID de campaña]**, seleccione **[!UICONTROL Agregar ID de campaña]** para agregar una nueva fila donde pueda introducir los detalles de la campaña.

![El cuadro de diálogo ID de campaña y nombre muestra la fila de campaña vacía después de seleccionar la opción Agregar ID de campaña.](/help/assets/collaborate/manage-view-projects/add-campaign-row.png){zoomable="yes"}

Proporcione el **[!UICONTROL ID de campaña]** y **[!UICONTROL nombre de campaña]**, y luego seleccione **[!UICONTROL Guardar]**.

![El cuadro de diálogo ID. y nombre de campaña que muestra los detalles de la nueva campaña y la opción Guardar resaltada.](/help/assets/collaborate/manage-view-projects/save-campaign-id.png){zoomable="yes"}

Compruebe la sección **[!UICONTROL Nombre e ID de campaña]** para ver sus campañas más recientes y los cambios recientes. Ahora puede utilizar los nuevos ID de campaña para generar informes de medición.

![Área de trabajo de información general del proyecto que muestra la sección de nombre e ID de campaña actualizada.](/help/assets/collaborate/manage-view-projects/view-updated-campaigns.png){zoomable="yes"}
