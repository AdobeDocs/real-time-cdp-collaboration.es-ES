---
title: 'Activar audiencias directamente (1P Audience Activation): Beta'
description: Obtenga información sobre cómo activar audiencias propias o compartidas de origen sin un proyecto, seleccionar un destino, revisar asignaciones de campos y establecer una programación de activación.
badgeBeta: label="Beta" type="Informative"
source-git-commit: 5f823194a18468b9205f64853551719ae8a3752f
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 1%
---

# Activar audiencias directamente (1P Audience Activation) {#activate-audiences-directly}

Utilice la activación directa de audiencias de origen (1P) en [!DNL Adobe Real-Time CDP Collaboration] para enviar audiencias a un destino sin crear un proyecto. Active las audiencias que posea o que haya compartido con usted para uso propio.

Comience desde un destino configurado o **[!UICONTROL audiencias activadas]**, luego seleccione audiencias y establezca la programación de activación.

Para enviar y activar audiencias a través de un proyecto de colaboración, consulte [Enviar y activar audiencias en un proyecto](/help/guide/collaborate/activate.md).

## Acceso de audiencia para activación {#audience-access-for-activation}

Compruebe la fuente de audiencia para determinar si necesita una concesión antes de la activación.

| Origen de público | Requisito de acceso |
| --- | --- |
| Sus propias audiencias | Las audiencias son suyas. |
| Audiencias compartidas con usted | Necesita una concesión activa con permiso de activación directa. El proveedor conserva la propiedad. |

{style="table-layout:auto"}

Una concesión de audiencia virtual le permite acceder a una audiencia compartida por referencia sin mover sus datos. A continuación, puede activar la audiencia para enviar sus datos al destino seleccionado.

Para obtener detalles acerca de las concesiones y los controles de proveedor, consulte [Acceso de audiencia virtual (concesiones de audiencia)](/help/guide/setup/virtual-audience-access.md).

## Requisitos previos {#prerequisites}

Antes de empezar, confirme que dispone de lo siguiente:

* Una audiencia suya o compartida a través de una subvención de origen (1P) válida.
* Un destino configurado que controla y que admite la activación directa.
* Al menos una asignación de campo de clave de coincidencia para el destino.

Para activar una audiencia compartida, confirme que su concesión activa con ámbito de conexión cumple las [condiciones de idoneidad](#check-shared-audience-access). Use el área de trabajo **[!UICONTROL Activation]**. No necesita un proyecto.

### Idoneidad de audiencia compartida {#check-shared-audience-access}

La concesión debe cumplir cada condición para admitir la activación directa.

| Requisito | Condición |
| --- | --- |
| Permiso de audiencia | La concesión incluye el permiso de activación directa. |
| Duración del acceso | La concesión está activa, ya sea de forma indefinida o dentro del intervalo de fechas especificado. |

{style="table-layout:auto"}

El permiso independiente **[!UICONTROL Generar nueva audiencia]** le permite usar una audiencia compartida para la creación de audiencias de cohorte. No necesita este permiso para la activación directa.

### Asignaciones de campos de destino {#review-destination-field-mappings}

La activación directa utiliza las asignaciones de clave de coincidencia configuradas para su destino. No se seleccionan las claves de coincidencia durante la activación.

Para configurar destinos, consulte [información general de destinos](../destinations/overview.md).

## Iniciar activación directa {#start-direct-activation}

Comience desde un destino configurado o desde la lista de audiencias activadas. Los destinos de Adobe Experience Platform no admiten la activación de origen.

### Empezar desde un destino {#start-from-a-destination}

Para abrir el flujo de trabajo con un destino seleccionado, comience desde ese destino configurado. En primer lugar, abra el área de trabajo **[!UICONTROL Activation]** y seleccione **[!UICONTROL Destinos]**.

A continuación, seleccione **[!UICONTROL Activar audiencias]** de las acciones para el destino que desee usar.

El flujo de trabajo se abre con el destino seleccionado. Luego continúa con [Configurar la activación](#configure-the-activation).

### Empezar desde audiencias activadas {#start-from-activated-audiences}

Para elegir un destino en el flujo de trabajo, comience desde la lista de audiencias activadas. En primer lugar, abra el área de trabajo **[!UICONTROL Activation]** y seleccione **[!UICONTROL Audiencias activadas]**.

A continuación, inicie el flujo de trabajo seleccionando **[!UICONTROL Activar audiencia]** en la página o el icono de agregar (![Agregar una activación de audiencia.](/help/assets/icons/plus.png)) y luego **[!UICONTROL Activar audiencia]**.

El flujo de trabajo se abre sin seleccionar ningún destino. Luego continúa con [Configurar la activación](#configure-the-activation).

## Configuración de la activación {#configure-the-activation}

Seleccione una audiencia por activación de entre sus propias audiencias o audiencias compartidas con usted. Utilice el destino preseleccionado o elija un destino configurado si no hay ninguno seleccionado. El flujo de trabajo aplica las [asignaciones existentes](#review-destination-field-mappings) configuradas para ese destino.

Elija cuándo ejecutar la activación y revise la audiencia, el destino y la programación seleccionados antes de enviarlos.

## Acceso a cambios y ejecuciones programadas {#access-changes-and-scheduled-runs}

Active una audiencia compartida solo mientras el proveedor conceda permisos de acceso.

| Cambio de acceso | Efecto |
| --- | --- |
| La subvención caduca | El sistema procesa la caducidad cada hora. El destinatario pierde el acceso a la audiencia virtual una vez procesada la caducidad. |
| El proveedor anula la concesión | El destinatario pierde el acceso a la audiencia virtual inmediatamente. |
| Se ejecuta una activación programada | El sistema comprueba la concesión. Las audiencias con concesiones revocadas o caducadas no pueden activarse. |

{style="table-layout:auto"}

La caducidad o revocación no elimina los datos de audiencia ya entregados a un destino.

## Próximos pasos {#next-steps}

Después de activar las audiencias, utilice estas guías para administrar destinos o conexiones de colaboradores.

* [Configuración y administración de destinos](/help/guide/destinations/manage-destinations.md)
* [Administrar conexiones de colaborador](/help/guide/connect/manage-connections.md)
