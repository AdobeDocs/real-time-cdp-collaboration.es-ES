---
title: Creación de audiencias de expansión en Expandir
description: Aprenda a crear audiencias de expansión a partir de una audiencia semilla con la población de audiencias de un colaborador en Adobe Real-Time CDP Collaboration.
source-git-commit: 88cd685742a4d85850cbf732ef93ab215287c22a
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 1%
---
# Creación de audiencias de expansión en Expandir

Use la ficha **[!UICONTROL Expand]** en un proyecto para crear una audiencia de expansión a partir de una de sus audiencias. Collaboration utiliza la población de audiencias de su colaborador para encontrar perfiles similares a su audiencia semilla, lo que le ayuda a alcanzar nuevos clientes potenciales sin exponer los datos de audiencia subyacentes de su colaborador. La audiencia de expansión resultante se envía a su colaborador para su activación.

## Requisitos previos {#prerequisites}

Antes de usar la ficha **[!UICONTROL Expand]**, debería tener:

* [Se originó](/help/guide/setup/onboard-audiences.md) al menos una audiencia para usarla como audiencia semilla
* [Conectado](/help/guide/connect/establishing-connections.md) con un colaborador
* [Creó un proyecto](/help/guide/collaborate/manage-projects.md) con ese colaborador
* Si está recibiendo una audiencia de expansión, un [destino](/help/guide/destinations/overview.md) configurado para recibir audiencias activadas

## Expandir información general {#expand-overview}

Vaya a **[!UICONTROL Colaborar]** > **[!UICONTROL Mis proyectos]**, abra un proyecto y seleccione la ficha **[!UICONTROL Expandir]**.

La página **[!UICONTROL Expand]** muestra las audiencias de expansión creadas para este colaborador y la opción de crear una nueva.

![La pestaña Expandir que muestra la tabla de audiencias de expansión con las columnas Nombre, Estado, Tamaño del modelo, Alcance de audiencia y Última actualización.](/help/assets/collaborate/expand/expand-overview.png){zoomable="yes"}

La tabla **[!UICONTROL Audiencias de expansión]** enumera todas las audiencias de expansión creadas en el proyecto:

| Columna | Descripción |
|---|---|
| **[!UICONTROL Nombre]** | Nombre de la audiencia de expansión. El valor predeterminado es el nombre de la audiencia semilla hasta que se edite. |
| **[!UICONTROL Estado]** | El estado actual de la audiencia de expansión. Consulte [estado de audiencia de expansión](#expansion-audience-status) para obtener más información. |
| **[!UICONTROL Tamaño de modelo]** | El tamaño de la audiencia de expansión generada. No está disponible hasta que el modelo termina de procesarse. |
| **[!UICONTROL Alcance de audiencia]** | La configuración de alcance de audiencia que se utiliza para la audiencia de expansión. |
| **[!UICONTROL Última actualización]** | Fecha y hora en que se actualizó la audiencia de expansión por última vez. |

{style="table-layout:auto"}

### Estado de audiencia de expansión {#expansion-audience-status}

Una audiencia de expansión se desplaza por los siguientes estados:

| Estado | Descripción |
|---|---|
| **[!UICONTROL Procesando]** | El modelo de expansión sigue generando la audiencia de expansión. |
| **[!UICONTROL Borrador]** | El modelo ha finalizado y la audiencia de expansión está lista para que la revise y la envíe a su colaborador. |
| **[!UICONTROL Activo]** | Ha enviado la audiencia de expansión a su colaborador. |

{style="table-layout:auto"}

>[!NOTE]
>
>El estado no se actualiza en tiempo real. Vuelva a abrir o actualice la ficha **[!UICONTROL Expandir]** para ver el estado más reciente.

## Creación de una audiencia de expansión {#create-expansion-audience}

Para crear una nueva audiencia de expansión, seleccione el icono Agregar (![Agregar icono.](/help/assets/icons/plus.png)) en la página **[!UICONTROL Expand]** y, a continuación, seleccione **[!UICONTROL Crear una audiencia expandida]**.


Aparecerá el cuadro de diálogo **[!UICONTROL Generar una audiencia de expansión]**. Complete todos los campos para generar la audiencia de expansión.

![Cuadro de diálogo Generar expansión de audiencia con los campos Audiencia semilla, Alcance de audiencia, Clave de coincidencia y Miembros de la audiencia semilla.](/help/assets/collaborate/expand/generate-expansion-audience-dialog.png){zoomable="yes"}

### Selección de la audiencia semilla {#select-seed-audience}

Seleccione una de sus propias audiencias en el menú desplegable **[!UICONTROL Seleccionar la audiencia semilla]**. Collaboration utiliza esta audiencia como base para encontrar perfiles similares en la población de colaboradores.

![Campo de audiencia semilla en el cuadro de diálogo Generar expansión de audiencia.](/help/assets/collaborate/expand/select-seed-audience.png){zoomable="yes"}

### Seleccione una clave de coincidencia {#select-match-key}

Habilite una clave de coincidencia para la audiencia de expansión. No puede habilitar más de uno.

| ID de persona | ID de dispositivo |
|---|---|
| **[!UICONTROL Correo electrónico con hash]** | **[!UICONTROL IPv4 con hash]** |
| **[!UICONTROL Teléfono con hash]** | **[!UICONTROL GAID]** |
| **[!UICONTROL ID de fidelización]** | **[!UICONTROL IDFA]** |
| **[!UICONTROL ID de CRM]** | **[!UICONTROL ID de Demdex]** |

{style="table-layout:auto"}

>[!NOTE]
>
>Si la audiencia semilla no incluye una clave de coincidencia determinada, esa opción aparece deshabilitada y no se puede seleccionar.

![La sección Clave de coincidencia del cuadro de diálogo Generar expansión de audiencia con las opciones de clave de coincidencia disponibles.](/help/assets/collaborate/expand/select-match-key.png){zoomable="yes"}

### Seleccione el alcance de la audiencia {#select-audience-reach}

Utilice el menú desplegable **[!UICONTROL Alcance de la audiencia]** para equilibrar la similitud con la audiencia semilla y el alcance general. Seleccione **[!UICONTROL Equilibrado]** para obtener un punto medio entre la similitud con su audiencia semilla y el alcance general.

![El campo Alcance de audiencia en el cuadro de diálogo Generar expansión de audiencia con la opción Equilibrada seleccionada y el texto de descripción debajo.](/help/assets/collaborate/expand/select-audience-reach.png){zoomable="yes"}

### Incluir o excluir la audiencia semilla {#include-exclude-seed-audience}

Utilice los botones de opción **[!UICONTROL Audiencia semilla]** para elegir si la audiencia semilla original se incluye en la audiencia de expansión final o se excluye de ella.

![Campo Miembros de la audiencia semilla en el cuadro de diálogo Generar expansión de audiencia con los botones de opción Sí y No.](/help/assets/collaborate/expand/include-exclude-seed-audience.png){zoomable="yes"}

### Generación de la audiencia de expansión {#generate-expansion-audience}

Una vez completados todos los campos, seleccione **[!UICONTROL Generar audiencia de expansión]**. Un mensaje de confirmación confirma que Collaboration está creando la audiencia de expansión y que puedes seguir su progreso en la página **[!UICONTROL Expand]**.

## Revisión y envío de una audiencia de expansión {#review-send-expansion-audience}

Una vez que el estado de una audiencia de expansión se actualice a **[!UICONTROL Borrador]**, seleccione su nombre en la tabla **[!UICONTROL Audiencias de expansión]** para abrirlo.

![La audiencia de expansiónPágina de detalles que muestra los metadatos de audiencia, el tamaño del modelo, el tamaño de la audiencia semilla y el botón Enviar.](/help/assets/collaborate/expand/expansion-audience-detail.png){zoomable="yes"}

Desde esta vista, puede:

* Editar el nombre de la audiencia de expansión
* Ver la fecha y hora de creación
* Comparar el tamaño de la audiencia semilla con el tamaño de la audiencia de expansión generado
* Revise la clave de coincidencia utilizada para generar la audiencia

Cuando esté listo, seleccione **[!UICONTROL Enviar al socio]** para enviar la audiencia de expansión a su colaborador. La audiencia permanece en estado **[!UICONTROL Borrador]** hasta que la envíes y luego se actualiza a **[!UICONTROL Activo]**.

>[!NOTE]
>
>Si el colaborador no tiene un destino configurado, **[!UICONTROL Enviar al asociado]** no está disponible. En un mensaje se explica que el colaborador debe configurar primero un destino.

>[!IMPORTANT]
>
>Una audiencia de expansión caduca siete días después de generarse si no se envía a su colaborador.

## Recepción y activación de una audiencia de expansión {#receive-activate-expansion-audience}

Cuando envía una audiencia de expansión, Collaboration la envía a su colaborador según la configuración de activación configurada para la conexión:

* Si **activación automática** está habilitada, Collaboration activa la audiencia de expansión automáticamente en el destino configurado del colaborador y aparece en su [pestaña Activar](./activate.md#activated-audiences).
<!-- Beta release: automatic activation is the only available activation setting. Uncomment the manual activation guidance below when manual activation is introduced with the GA release. -->
<!-- * If **manual activation** is enabled, the expansion audience appears in your collaborator's [Received audiences](./activate.md#received-audiences) section of the **[!UICONTROL Activate]** tab, and your collaborator must manually activate it. -->

## Próximos pasos

Una vez que envíe la audiencia de expansión, use [Discover tab](./discover.md) para compararla con otras audiencias, o [Activate tab](./activate.md) para rastrear su activación.
