---
title: Configurar y administrar destinos de almacenamiento en la nube
description: Obtenga información sobre cómo configurar, ver y eliminar un destino de almacenamiento en la nube en Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 60124235569ca9b17b3bb1cef502d57d39e82e1f
workflow-type: tm+mt
source-wordcount: 885
ht-degree: 2%

---

# Configurar y administrar destinos de almacenamiento en la nube

Use esta guía para configurar, ver y eliminar destinos de almacenamiento en la nube del área de trabajo **[!UICONTROL Activation]**. Utilice la ficha **[!UICONTROL Catálogo]** para configurar destinos, la ficha **[!UICONTROL Destinos]** para administrarlos y la ficha **[!UICONTROL Audiencias activadas]** para revisar las audiencias activadas a los destinos.

Después de configurar un destino, pasa a estar disponible al activar audiencias. Para ver la lista completa de destinos admitidos, consulte la tabla [destinos disponibles](./overview.md#available-destinations).

>[!NOTE]
>
> Esta guía utiliza un destino **[!DNL Amazon S3]** como ejemplo. El flujo de trabajo de configuración guiada se comparte entre los tipos de destino de almacenamiento en la nube admitidos, pero los métodos de autenticación, los campos obligatorios y las capacidades del conector pueden variar. Antes de configurar un destino, revise los [requisitos de destino de almacenamiento en la nube](./cloud-storage-destination-requirements.md), que se vinculan a la documentación de destino de Adobe Experience Platform correspondiente.
>
> Adobe Experience Platform tiene un flujo de trabajo de configuración independiente en Real-Time CDP Collaboration. Para configurarlo, consulte [Configuración de Adobe Experience Platform como destino](./experience-platform.md).

## Requisitos previos {#prerequisites}

Antes de configurar un destino, asegúrese de lo siguiente:

* Tiene acceso al área de trabajo **[!UICONTROL Activation]**.
* Tiene la información de conexión requerida por su proveedor de almacenamiento en la nube.
* Si necesita crear una cuenta, tiene las credenciales o los permisos necesarios.
* Ha revisado los [requisitos para su destino de almacenamiento en la nube](./cloud-storage-destination-requirements.md).

## Configuración de un destino {#configure-destination}

Al configurar un destino, se conecta una cuenta de almacenamiento en la nube de a Real-Time CDP Collaboration y se define cómo se exportan a esta los datos de audiencia.

Vaya a **[!UICONTROL Activación]** > **[!UICONTROL Catálogo]**.

La ficha **[!UICONTROL Catálogo]** muestra los proveedores de destino disponibles. Cada destino aparece como una tarjeta. Según el destino, su tarjeta puede mostrar cuentas y acciones configuradas para ver información adicional.

![La ficha Catálogo muestra las tarjetas de proveedor de destino.](/help/assets/destinations/manage-destinations/destination-provider-catalog.png)

Busque el proveedor de destino que desea configurar y seleccione **[!UICONTROL Configurar]**.

La configuración de destino guiada por la configuración abre y le guía en cuatro pasos: **[!UICONTROL Autenticar]**, **[!UICONTROL Crear destino]**, **[!UICONTROL Asignar campos]** y **[!UICONTROL Revisar]**.

### Autenticar {#authenticate}

El paso **[!UICONTROL Autenticar]** establece una conexión entre Real-Time CDP Collaboration y su cuenta de destino.

Si hay una cuenta disponible, selecciónela en el selector de cuentas. Para crear una cuenta, seleccione **[!UICONTROL Nueva cuenta]**.

Seleccione un método de autenticación y proporcione la información de cuenta requerida. Los métodos y campos de autenticación disponibles dependen del proveedor de destino seleccionado. Para conocer los requisitos específicos del conector, consulte [Requisitos de destino de almacenamiento en la nube](./cloud-storage-destination-requirements.md).

Seleccione **[!UICONTROL Conectarse a Amazon S3]**. Para otros proveedores de destino, el botón muestra el nombre del proveedor correspondiente.

Una vez validada la cuenta correctamente, seleccione **[!UICONTROL Siguiente]**.

![Paso Autenticar que muestra la selección de cuentas y la creación de nuevas cuentas.](/help/assets/destinations/manage-destinations/authenticate-destination-account.png)

### Crear destino {#create-destination}

El paso **[!UICONTROL Crear destino]** define dónde y cómo se envían los archivos de exportación de audiencia.

Introduzca un nombre de destino y complete la configuración de almacenamiento y exportación necesaria. Los campos disponibles dependen del proveedor de destino seleccionado. Para ver las definiciones y los requisitos específicos del conector, consulte la documentación de destino vinculada desde [Requisitos de destino de almacenamiento en la nube](./cloud-storage-destination-requirements.md).

Una vez completados todos los campos obligatorios, seleccione **[!UICONTROL Siguiente]**. La configuración guiada avanza al paso de asignación de campos.

![El paso Crear destino muestra los campos de configuración de destino.](/help/assets/destinations/manage-destinations/configure-new-destination.png)

### Asignar campos {#map-fields}

El paso **[!UICONTROL Asignar campos]** define cómo se asignan las claves de coincidencia de audiencia a los campos de identidad que espera el destino.

A diferencia del flujo de trabajo de destinos estándar de Real-Time CDP, Real-Time CDP Collaboration configura estas asignaciones mientras se crea el destino. Las claves de coincidencia de audiencia aparecen como campos de origen. Asigne cada campo de origen a la identidad de destino correspondiente para que el destino pueda reconocer los identificadores exportados y asociarlos a los usuarios previstos.

Seleccione **[!UICONTROL Agregar campo]** para agregar otra asignación de clave de coincidencia o seleccione el icono Eliminar para quitar una asignación. Revise y configure todas las asignaciones necesarias.

Cuando se completen las asignaciones, seleccione **[!UICONTROL Siguiente]**. La configuración guiada avanza al paso de revisión.

![El paso Asignar campos que muestra la activación coincide con la configuración de asignación de claves.](/help/assets/destinations/manage-destinations/map-destination-fields.png)

### Revisar {#review-destination}

El paso **[!UICONTROL Revisar]** resume la configuración de destino antes de crearla.

Revise la configuración de destino. Para realizar cambios, seleccione el icono de lápiz ![El icono de lápiz.](../../assets/icons/edit.png) para la sección aplicable y actualice la configuración.

Cuando la configuración sea correcta, seleccione **[!UICONTROL Completar]**. El destino se crea y queda disponible para la activación de audiencias.

![El paso Revisar muestra el resumen de la configuración de destino antes de completarse.](/help/assets/destinations/manage-destinations/review-destination-configuration.png)

## Ver destinos configurados {#view-configured-destinations}

Después de configurar un destino, este aparece en el inventario de destino. Desde el inventario, puede revisar su estado y las audiencias activadas.

Vaya a **[!UICONTROL Activación]** > **[!UICONTROL Destinos]**. La ficha **[!UICONTROL Destinos]** muestra una tabla de destinos configurados.

![La ficha Destinos muestra los destinos configurados.](/help/assets/destinations/manage-destinations/configured-destinations-list.png)

## Eliminar un destino {#delete-destination}

Elimine un destino cuando ya no sea necesario para la activación de audiencias. Al eliminar un destino, se elimina del inventario de destinos y se evita que las audiencias se activen en el futuro.

>[!IMPORTANT]
>
>Al eliminar un destino no se eliminan los datos de audiencia que se exportaron anteriormente al mismo. Elimine los datos exportados anteriormente directamente del almacén de datos de destino.

Vaya a **[!UICONTROL Activación]** > **[!UICONTROL Destinos]**.

Busque el destino que desea quitar, seleccione el icono de puntos suspensivos en la columna **[!UICONTROL Acción]** y, a continuación, seleccione **[!UICONTROL Eliminar]**.

![Pestaña Destinos del área de trabajo de activación con el icono de puntos suspensivos y la acción Eliminar resaltados.](/help/assets/destinations/manage-destinations/delete-configured-destination.png)

Aparecerá un cuadro de diálogo de confirmación. Revise el destino que se eliminará y, a continuación, seleccione **[!UICONTROL Eliminar]** para confirmar.

El destino se elimina del inventario de destinos y ya no está disponible para la activación de audiencias.

## Próximos pasos {#next-steps}

Después de configurar un destino, puedes empezar a [activar audiencias](../collaborate/activate.md) dentro de tus proyectos.
