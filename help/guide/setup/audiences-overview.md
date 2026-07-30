---
title: Información general de los públicos
description: Obtenga información acerca de las audiencias en Real-Time CDP Collaboration, incluido de dónde pueden proceder.
audience: admin, publisher
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f7cd44177d60bfd3d3db384f7b1a250ace4c3633
workflow-type: tm+mt
source-wordcount: 707
ht-degree: 5%

---


# Información general de los públicos

{{limited-availability-release-note}}

En Adobe Real-Time CDP Collaboration, las audiencias son grupos de usuarios o clientes que introduce en Collaboration. Después del abastecimiento, las audiencias se pueden usar para detectar superposiciones con colaboradores, activar audiencias y medir el rendimiento de la campaña. Puede obtener audiencias de una variedad de tipos de fuentes, como Adobe Experience Platform, almacenamiento en la nube y sistemas de uso compartido, y flujos de trabajo de carga de archivos, en función de dónde residan ya los datos de su audiencia.

## Qué puede hacer con las audiencias {#audiences-in-collaboration}

Una vez que una audiencia proviene de Collaboration, está disponible para su uso en flujos de trabajo de colaboración admitidos.

Utilice audiencias en Collaboration para lo siguiente:

* Comparación de la audiencia con las audiencias de los colaboradores
* Identificación de superposiciones y oportunidades
* Activar públicos
* Mida los resultados y el rendimiento de la campaña
* Administrar la visibilidad de audiencia y la configuración relacionada

## Cómo encajan las audiencias en Collaboration {#conceptual-diagram}

>[!NOTE]
>
> El diagrama siguiente proporciona una vista de alto nivel de cómo las audiencias de origen se ajustan a Collaboration y se utilizan en los proyectos.

```text
Source → Data connection → Audience → Project
                                         │
                          ┌──────────────┼──────────────┐
                          ▼              ▼              ▼
                      Discover       Activate       Measure
                                         │
                                         ▼
                                    Destination
```

## Conceptos básicos {#core-concepts}

Los siguientes conceptos describen los objetos clave implicados en los flujos de trabajo de colaboración y abastecimiento de audiencia.

**Source**\
El sistema o la ubicación donde se originan los datos de audiencia, como Adobe Experience Platform, una ubicación de almacenamiento en la nube o una carga de archivo.

**Conexión de datos**\
La conexión configurada que utiliza Collaboration para acceder a los datos de audiencia de un origen. Una conexión de datos incluye detalles de configuración específicos del origen, como autenticación, asignación de campos y programación.

**Audiencia**\
Grupo de usuarios o clientes que se ha originado en Collaboration y está disponible para su uso en proyectos.

**Conexión**\
La relación de colaboración entre su organización y otra organización.

**Proyecto**\
Espacio de trabajo en el que los colaboradores utilizan las audiencias para casos de uso admitidos, como descubrimiento, activación y medición.

**Destino**\
La plataforma o el sistema externo al que se envían las audiencias activadas.

**Claves de coincidencia**
Identificadores que utiliza Collaboration para hacer coincidir registros de conjuntos de datos y colaboradores. Las claves de coincidencia admiten flujos de trabajo como superposición de audiencias, activación y medición.

## Ciclo de audiencia {#audience-lifecycle}

En Collaboration, obtiene audiencias a través de conexiones de datos, las administra en **[!UICONTROL Configuración]** y las usa en proyectos para casos de uso admitidos.

1. **Audiencias de Source**: Incluya datos de audiencias en Collaboration mediante una conexión de datos.
2. **Administrar audiencias**: revise y administre los detalles de audiencia, la visibilidad y la configuración relacionada.
3. **Usar audiencias en proyectos**: usa audiencias de origen en proyectos para casos de uso admitidos, como **Discover**, **Activate** y **Measure**.

No todas las audiencias se utilizan en todos los casos de uso. Por ejemplo, una audiencia puede obtenerse y utilizarse para **Discover** sin activarse, o puede usarse en flujos de trabajo de **Measure** sin enviarse a un destino.

Para obtener más información sobre cómo obtener y administrar audiencias, consulte [Source y administrar audiencias](./onboard-audiences.md). Para obtener información acerca de cómo administrar conexiones de datos, consulte [Administrar conexiones de datos](./manage-data-connection.md).

## Procedencia de las audiencias {#supported-sources}

Collaboration admite varios tipos de fuentes de audiencia. El origen que elija determina el flujo de configuración, los requisitos previos, los requisitos de autenticación, el formato de datos, la asignación de campos, el comportamiento de actualización y las opciones de configuración disponibles para introducir audiencias en Collaboration.

* Adobe Experience Platform
* Almacenamiento en la nube, incluidos Amazon S3, Google Cloud Storage y Azure Storage
* Servicios de uso compartido de datos, incluidos Snowflake y Databricks Delta Share
* Adobe Audience Manager
* Carga de archivo CSV

Para obtener una lista de las fuentes admitidas y los pasos de configuración específicos de la fuente, consulte [Resumen de fuentes](./source-overview.md#available-sources).

## De qué están formadas las audiencias {#match-keys}

Las audiencias en RTCDP Collaboration están formadas por claves de coincidencia. Según la configuración de la cuenta, las claves de coincidencia admitidas pueden incluir **ID de persona**, **ID de dispositivo** y **ID de socio**. Las claves de coincidencia admiten flujos de trabajo como **superposición de audiencias**, **activación** y **medición**.

Para obtener más información, consulta [Configurar claves de coincidencia](../setup/onboard-account.md#set-up-match-keys) y [Administrar conexiones de datos](../setup/manage-data-connection.md#match-keys)

## Usar audiencias en proyectos {#audiences-in-projects}

Los proyectos proporcionan el contexto para colaborar con otra organización. Dentro de un proyecto, puede utilizar audiencias para casos de uso de colaboración admitidos:

* **Descubrir**: Compare audiencias y revise perspectivas de superposición. Ver [Superposición de audiencia de detección](../collaborate/discover.md).
* **Activar**: active las audiencias seleccionadas para el uso de la campaña. La activación se inicia desde la ficha [!UICONTROL Activar] del área de trabajo del proyecto y envía audiencias al destino configurado de la conexión. Ver [Activar audiencias](../collaborate/activate.md).
* **Medida**: revise los informes de conversión y envío de la campaña asociados con el proyecto. Ver [Rendimiento de la medida](../collaborate/measure.md).

Para obtener más información sobre cómo crear y administrar proyectos, vea [Crear y administrar proyectos](../collaborate/manage-projects.md). Para obtener información acerca de cómo configurar destinos, vea [Información general sobre destinos](../destinations/overview.md).

## Próximos pasos {#next-steps}

* [Revisar fuentes de audiencia disponibles](./source-overview.md)
* [Source y administración de audiencias](./onboard-audiences.md)
* [Creación y administración de proyectos](../collaborate/manage-projects.md)
* [Detectar superposición de audiencias](../collaborate/discover.md)
* [Activar públicos](../collaborate/activate.md)
* [Rendimiento de medida](../collaborate/measure.md)
* [Información general sobre los destinos](../destinations/overview.md)
