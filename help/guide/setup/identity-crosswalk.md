---
title: Cruces de identidades
description: Conozca todo acerca de los pasos transversales de identidad en Real-Time CDP Collaboration, incluyendo cómo traer pasos transversales de identidad de diferentes fuentes y cómo administrar los pasos transversales de identidad
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hidefromtoc: true
hide: true
exl-id: a51f112d-3da7-4482-a24a-6d9f269d28d1
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 22%

---

# Cruces de identidades

{{limited-availability-release-note}}

Conozca todo acerca de los cruces de identidad en Real-Time CDP Collaboration, incluyendo cómo traer cruces de identidad desde diferentes fuentes, y cómo administrar los cruces de identidad.

Los pasos cruzados de identidad facilitan la vinculación segura y compatible con la privacidad de las identidades de los clientes en varios conjuntos de datos y plataformas. Al utilizar identificadores hash, Real-Time CDP Collaboration garantiza que los usuarios puedan sincronizar y reconciliar identidades sin exponer información de identificación personal (PII). Esto permite obtener una vista unificada del cliente para mejorar la colaboración y las iniciativas de marketing segmentadas.

<!--
In Real-Time CDP Collaboration, use identity crosswalks alongside your audiences by [TODO] insert material here. 
-->


Como primer paso, debe importar pasos transversales de identidad en Real-Time CDP Collaboration. Para importar cruces de identidad en Real-Time CDP Collaboration, lea la siguiente sección:

>[!NOTE]
>
>En la versión beta de Real-Time CDP Collaboration, puede importar pasos de identidad de sus conjuntos de datos en Real-Time CDP. Habrá más opciones disponibles en versiones posteriores.

## Importación de pasos de identidad en Real-Time CDP Collaboration {#import-crosswalk}

Vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Cruces de identidad]**, seleccione el símbolo Más **+** y seleccione **[!UICONTROL Cruce de identidad]**

![Grabación de cómo llegar a la pantalla para agregar cruces de identidad](/help/assets/setup/identity-crosswalks/import-identity-crosswalk.gif)

### Seleccionar fuente de cruce

Seleccione una fuente desde la que vaya a importar el cruce de identidades. En la primera versión de Real-Time CDP Collaboration, Experience Platform es la única fuente compatible para importar pasos cruzados.

>[!TIP]
>
>Los cruces peatonales que está importando desde Experience Platform se denominan *conjuntos de datos* en Platform.

Después de seleccionar Experience Platform como fuente de tus pasos peatonales, selecciona la [zona protegida de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/sandbox/home) desde la cual estás importando el paso peatonal de identidad.

![Registro de cómo seleccionar un origen de paso de peatones](/help/assets/setup/identity-crosswalks/select-crosswalk-source.gif)

### Seleccionar cruce

Después de seleccionar Experience Platform como fuente de sus pasos peatonales,

### Proporcionar detalles

Proporcione un nombre y una descripción para el cruce de identidades que está importando en el producto.

### Seleccionar clave de unión {#select-join-key}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_crosswalk_join_key"
>title="Clave de unión"
>abstract="Una clave de unión es un identificador único que se utiliza para hacer coincidir y vincular registros en diferentes conjuntos de datos. Garantiza que los datos de varias fuentes se puedan asociar con precisión a la misma persona o entidad. Cualquiera de los encabezados de columna del cruce seleccionado puede servir como clave de unión."

Una clave de unión es un identificador único que se utiliza para hacer coincidir y vincular registros en diferentes conjuntos de datos. Garantiza que los datos de varias fuentes se puedan asociar con precisión a la misma persona o entidad. Al seleccionar la clave de unión adecuada, puede combinar y reconciliar datos de forma eficaz, lo que mejora la precisión y exhaustividad de las campañas.

Cualquiera de los encabezados de columna del cruce seleccionado puede servir como clave de unión.

Seleccione la clave de unión que desee para la tabla de cruce y seleccione **[!UICONTROL Siguiente]** para continuar con el paso siguiente.

### Revisar

Revise cualquiera de las selecciones de las pantallas anteriores. Cuando esté satisfecho con la selección, seleccione **[!UICONTROL Siguiente]** para completar el flujo de trabajo.

## Pasos siguientes

Después de aprender a importar pasos de identidad en Real-Time CDP, puede ver todos los pasos de identidad que ha agregado hasta ahora a Real-Time CDP Collaboration. Ahora también puede utilizar los pasos de identidad que ha importado al importar audiencias en Real-Time CDP Collaboration.
