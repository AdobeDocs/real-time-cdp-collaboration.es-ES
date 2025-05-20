---
title: Importar y administrar audiencias
description: Obtenga información sobre cómo importar y administrar audiencias en Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: 8fca38c8125cefae9fe52ecd168e3d0ff20f2936
workflow-type: tm+mt
source-wordcount: '2685'
ht-degree: 24%

---

# Importar y administrar audiencias

{{limited-availability-release-note}}

Las audiencias son grupos específicos de usuarios o clientes segmentados según varios atributos. Esto permite a los anunciantes y editores colaborar en marketing dirigido y experiencias personalizadas para campañas publicitarias más efectivas.

Utilice esta página como referencia para comprender todas las métricas relevantes que puede ver relacionadas con sus audiencias, así como los pasos del flujo de trabajo para importar una audiencia en Adobe Real-Time CDP Collaboration.

>[!TIP]
>
>Use la información de esta pantalla para obtener toda la información que necesita sobre sus audiencias y las [pantallas de detección y superposición](/help/guide/collaborate/discover.md) para obtener información sobre cuál de sus audiencias funcionaría mejor para los distintos tipos de campañas, en comparación con el inventario de editores.

>[!BEGINSHADEBOX]

Lo que encontrará en esta página de documentación:

* [Importación de audiencias en Real-Time CDP Collaboration](#import-audiences)
* [Panel de vista de públicos](#view-audiences-dashboard)
* [Ver audiencias individuales](#view-individual-audiences)

>[!ENDSHADEBOX]

## Importación de audiencias en Real-Time CDP Collaboration {#import-audiences}

>[!IMPORTANT]
>
>Para importar audiencias, el usuario debe estar asignado a una función que contenga dos permisos de Administración de perfiles: Ver perfiles y Ver segmentos. Para obtener información sobre cómo asignar los permisos necesarios, consulte la guía [importación de audiencias](../permissions/overview.md#audience-importation).

Para poder compartir audiencias con colaboradores y ejecutar cálculos de superposición, es necesario importar las audiencias a Real-Time CDP Collaboration. Para importar audiencias, siga los pasos de flujo de trabajo de la sección siguiente.

![Mis audiencias se mostraron en pantalla antes de que se agregaran audiencias a la organización.](/help/assets/setup/add-manage-audiences/org-without-audiences-added.png)

En la ficha **[!UICONTROL Mis audiencias]**, seleccione el símbolo Más **+** y seleccione **Audiencia**.

### Seleccionar conexión de datos {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Acción de marketing"
>abstract="<p>Utilice acciones de marketing para controlar qué datos del público se importarán a Real-Time CDP Collaboration desde Experience Platform. La acción de marketing <strong>Colaboración de datos</strong> admite las etiquetas de uso de datos C4, C5 y C9. La acción de marketing <strong>Ciencia de datos</strong> admite la etiqueta de uso de datos C9.</p> <p> <ul><li> Con la casilla de verificación <em>habilitada</em>, cualquier dato marcado con las etiquetas llamadas arriba en Experience Platform se excluye y <strong>no</strong> se incorpora a Real-Time CDP Collaboration.</li><li> Con la casilla de verificación <em>deshabilitada</em>, no hay restricciones en los datos de Experience Platform que se pueden importar a Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=es" text="Información general sobre las etiquetas de uso de datos"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=es" text="Glosario de etiquetas de uso de datos"

>[!IMPORTANT]
>
>Después de conectarse a la primera conexión de datos e importar la primera audiencia, puede seleccionar importar varias audiencias desde esta conexión de datos existente. En este caso, el flujo de trabajo le llevará directamente al paso [seleccionar audiencia](#select-audience), ya que toda la información de requisitos previos de los demás pasos se importará desde la conexión existente.

Las conexiones de datos son el origen de los datos desde los que se importan las audiencias a Real-Time CDP Collaboration. En la primera versión de Real-Time CDP Collaboration, la única conexión de datos compatible es Adobe Experience Platform.

Cualquier configuración, como la asignación de identidad o la programación, que configure para la conexión de datos se aplica a todas las audiencias importadas desde esta conexión de datos.

>[!TIP]
>
>Hay un flujo de trabajo independiente en el que siempre puede ver y editar todas las conexiones de datos que añadió en este paso. Más información sobre [administrar conexiones de datos](/help/guide/setup/manage-data-connection.md).

![Seleccione la pantalla de origen de la audiencia que muestra las opciones de AEP RTCDP, archivo CSV, Amazon S3 y Snowflake.](/help/assets/setup/add-manage-audiences/Step-Select-Audience-Source.png)

#### Seleccionar fuente de datos

En este paso, elegirá la fuente de los datos de audiencia. Las fuentes disponibles incluyen:

* **Adobe Experience Platform**: seleccione esta opción para traer sus audiencias desde Adobe Experience Platform Real-Time CDP.
* **Archivo CSV** (versión futura): cargue un archivo CSV que contenga los datos de su audiencia para introducir datos de forma rápida y directa.
* **Amazon Web Service** (versión futura): conéctese a su almacenamiento de Amazon S3 para importar datos de audiencia directamente desde sus bloques de S3.
* **Snowflake** (versión futura): Use su almacén de datos de Snowflake para extraer datos de audiencia sin problemas.

#### Selección de zona protegida

Después de seleccionar **Adobe Experience Platform** como fuente de datos, debe seleccionar la zona protegida que incluye las audiencias que va a importar.

![Seleccionar zona protegida para importar audiencias](/help/assets/setup/add-manage-audiences/import-audiences-select-sandbox.png)

Seleccione **[!UICONTROL Siguiente]** después de seleccionar la zona protegida deseada.

#### Política de gobernanza y acciones de cumplimiento {#governance-policy-and-enforcement-actions}

A continuación, debe asegurarse de que las acciones de marketing correctas se establecen en los datos importados. También debe dar su consentimiento para que los datos importados de Real-Time CDP se utilicen para la colaboración de datos.

Utilice acciones de marketing para controlar qué datos del público se importarán a Real-Time CDP Collaboration desde Experience Platform. La acción de marketing **Colaboración de datos** admite las etiquetas de uso de datos C4, C5 y C9. La acción de marketing **Ciencia de datos** admite la etiqueta de uso de datos C9.

Obtenga más información sobre las [etiquetas de uso de datos C4, C5 y C9](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* Con la casilla de verificación *habilitada*, cualquier dato marcado con las etiquetas llamadas arriba en Experience Platform se excluye y *no* se incorpora a Real-Time CDP Collaboration.
* Con la casilla de verificación *deshabilitada*, no hay restricciones en los datos de Experience Platform que se pueden importar a Real-Time CDP Collaboration.

Obtenga más información sobre las etiquetas de uso de datos en la documentación de Experience Platform:

* [Información general sobre las etiquetas de uso de datos](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Glosario de etiquetas de uso de datos](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target="_blank"}

![Acciones de marketing necesarias para la colaboración de datos.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

### Proporcionar detalles

A continuación, proporcione un nombre y una descripción para que pueda reconocer esta conexión de datos en el futuro.

<!--

>[!IMPORTANT]
>
>Note a difference in terminology where the sandbox selected from Real-Time CDP is considered a dataset in the UI in Real-Time CDP Collaboration.

-->

### Asignar campos {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Campos de origen"
>abstract="Los campos de origen son espacios de nombres de identidad y atributos de la implementación existente de Real-Time CDP. Puede asignarlos a los campos de destino definidos en Real-Time CDP Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Campos de destino"
>abstract="Los campos de destino corresponden a las claves de coincidencia seleccionadas al incorporar la empresa. Actualmente, los correos electrónicos con hash son las únicas claves de coincidencia admitidas."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Aplicar transformación"
>abstract="Al importar campos *sin hash* desde su origen, utilice esta opción para que Real-Time CDP Collaboration aplique el hash y transforme los campos sin formato en campos con hash."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="Espacios de nombres de identidad"
>abstract="Seleccione un espacio de nombres de identidad del espacio de nombres de identidad estándar y personalizados disponibles en su organización de Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=es#standard" text="Espacios de nombres estándar y de identidad de Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="Atributos de perfil"
>abstract="Seleccione atributos del esquema de unión para la clase de perfil en Experience Platform. Esta vista muestra los atributos que están presentes en el esquema de unión y pertenecen a la clase de perfil individual XDM."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=es" text="Esquema de unión en Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Espacios de nombres de destino"
>abstract="Se rellenará con una descripción adecuada."

![Pantalla Asignar campos que muestra los campos de origen asignados a los campos de destino.](/help/assets/setup/add-manage-audiences/Step-Map-Fields.png)

En el paso Asignar campos, puede seleccionar cómo se debe asignar cualquier campo de identidad para los perfiles introducidos desde la conexión de datos a las claves de coincidencia seleccionadas en su organización.

>[!TIP]
>
>Puede asignar varios campos de origen al mismo campo de destino. Por ejemplo, si tiene direcciones de correo electrónico en dos campos distintos en Experience Platform, puede asignar ambos al campo de destino **[!UICONTROL Correo electrónico con hash]** como dos filas independientes.

>[!BEGINSHADEBOX]

**[!UICONTROL Campos de Source]** indican cómo se hace referencia a las identidades en el origen desde el que se importan los datos.

**[!UICONTROL Campos de destino]** indican cómo se hace referencia a las identidades en Real-Time CDP Collaboration. Los valores que puede seleccionar aquí corresponden a las claves de coincidencia configuradas en el flujo de trabajo de incorporación de la empresa.

Utilice la opción **[!UICONTROL Aplicar transformación]** al importar *campos sin hash* desde su origen. En este caso, Real-Time CDP Collaboration aplica el hash y transforma los campos. El algoritmo hash utilizado por Adobe es SHA256.

>[!ENDSHADEBOX]

Agregue todos los pares de asignación que necesite y seleccione **[!UICONTROL Siguiente]** para continuar con el paso siguiente.

<!--

In this step, you can also add any identity crosswalks that you would like to use.

Identity crosswalks will be supported after the beta release.

#### Add identity crosswalk

Use identity crosswalks to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. 

TODO add GIF Identity crosswalks screen showing a list of available identity crosswalks with details.

Select **[!UICONTROL Add identity crosswalk]** to see a screen where you can choose from various identity crosswalks that you have previously [imported into Real-Time CDP Collaboration](/help/guide/setup/identity-crosswalk.md#import-crosswalk). Each entry includes details such as the table name, type, description, and creation date.

After selecting the desired crosswalk, use a source field join key to map to the crosswalk table join key. 

>[!NOTE]
>
>After selecting an identity crosswalk, the **[!UICONTROL Add identity crosswalk]** control is greyed out. 

For further reading about identity crosswalks, refer to the [glossary](/help/guide/glossary.md).

-->


<!-- will uncomment this part when Manage use cases part becomes available

### Manage use cases {#manage-use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_usecases"
>title="Use cases for identities"
>abstract="This control is disabled in the initial release of Real-Time CDP Collaboration"

![Manage use cases screen.](/help/assets/setup/add-manage-audiences/Step-manage-use-cases.png)

For every identity selected in the mapping step, select the use cases that you can use the identity for. Available use cases are: 

* Discover
* Share
* Activate
* Measure

Note that this control is disabled in the initial release of Real-Time CDP Collaboration.

After selecting the desired use cases for each identity, proceed to the next step. 

-->›

### Programación {#schedule}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="Caducidad del público"
>abstract="Próximamente se darán detalles sobre la caducidad del público."

Programe cuándo comenzar y finalizar la cumplimentación y actualización de las audiencias. El abono a audiencia se actualizará según esta programación.

![Pantalla de programación que muestra las fechas de inicio y finalización para rellenar las audiencias.](/help/assets/setup/add-manage-audiences/Step-Schedule.png)

Seleccione la frecuencia de actualización de las audiencias. Las opciones disponibles tienen una frecuencia de actualización de entre uno y seis días.

>[!IMPORTANT]
>
>Ajustar la frecuencia de las actualizaciones de audiencias ayudará a administrar la [actividad de crédito de Gestión de público](/help/guide/setup/my-activity.md#types-of-activities), que se calcula por actualización de pertenencia a audiencias. El impacto de esto puede ser que haya menos datos nuevos disponibles para los informes de descubrimiento de audiencias y para el uso compartido y la activación de audiencias.

![Pantalla de programación que muestra diferentes intervalos de frecuencia para actualizar la pertenencia a audiencias.](/help/assets/setup/add-manage-audiences/Step-Schedule-Set-Frequency.png)

>[!IMPORTANT]
>
>Después de la fecha de finalización en el intervalo de fechas, todas las audiencias importadas desde esta conexión de datos dejarán de actualizarse. Para renovar la conexión, ve a [Administrar conexión de datos](/help/guide/setup/manage-data-connection.md) y establece una nueva fecha de finalización.

### Seleccionar públicos {#select-audience}

Después de seleccionar la fuente de audiencia, elegirá las audiencias específicas que desea incluir. Utilice las opciones de búsqueda y filtrado de la página para encontrar las audiencias relevantes de la fuente de datos seleccionada.

![La pantalla Seleccionar audiencia muestra una lista de audiencias disponibles con casillas de verificación para seleccionarlas.](/help/assets/setup/add-manage-audiences/Step-Select-Audience.png)

### Revisar

Revise todas las configuraciones y ajustes de antes de finalizar la adición de audiencias. Asegúrese de que todos los detalles sean correctos y seleccione **[!UICONTROL Completar]** para finalizar el proceso.

## Panel de vista de públicos {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Identidades que faltan"
>abstract="El recuento de identidades estará disponible tras la siguiente actualización de la conexión de datos siguiendo la programación configurada. La actualización inicial suele producirse en las 24 horas siguientes al establecimiento de la conexión de datos. Las actualizaciones continuas seguirán la programación configurada. "

Después de importar audiencias en Real-Time CDP Collaboration, puede obtener información sobre ellas en una vista de panel. La vista predeterminada de la página **[!UICONTROL Mis audiencias]** muestra todas las audiencias que su organización ha importado actualmente a Real-Time CDP Collaboration.

![Página de información general de audiencias que muestra todas las audiencias importadas por un anunciante](/help/assets/setup/add-manage-audiences/audiences-overview.png)

Puede ver la siguiente información relevante sobre cada audiencia:

| Elemento | Descripción |
|----------|---------|
| **[!UICONTROL Identidades]** | Indica el número de identidades presentes en esta audiencia. Tenga en cuenta que si el mismo perfil tiene dos o más identidades y estas identidades se utilizan como claves de coincidencia en el proyecto, el perfil aparecerá dos veces en el recuento. |
| **[!UICONTROL Estado]** | Indica si la audiencia está activa y si se puede utilizar en proyectos. El estado Pendiente indica que la audiencia se ha importado recientemente y que los miembros de la audiencia aún no se han completado. Las audiencias importadas se rellenarán con perfiles después de la siguiente actualización de la conexión de datos según la programación configurada. La actualización inicial suele producirse en un plazo de 24 horas tras la configuración de la conexión de datos                                         . |
| **[!UICONTROL Source]** | Indica la fuente desde la que se importó esta audiencia. En la versión actual de Real-Time CDP Collaboration, Adobe Experience Platform es la única fuente compatible. |
| **[!UICONTROL Conexión de datos]** | Más información detallada acerca de desde dónde se importó esta audiencia. Por ejemplo, al importar audiencias desde el origen de Experience Platform, los entornos limitados individuales a los que su organización tiene acceso se consideran las conexiones de datos. |
| **[!UICONTROL Acceso a la conexión]** | Define si esta audiencia es privada o pública. Las audiencias públicas se pueden detectar en informes de superposición y compartir con colaboradores. |
| **[!UICONTROL Creado]** | Indica cuándo se importó esta audiencia a Real-Time CDP Collaboration. |
| **[!UICONTROL Última actualización]** | Indica la última fecha y hora en que se actualizó cualquier aspecto de esta audiencia. |

Seleccione **[!UICONTROL Administrar conexiones de datos]** para ver y editar todas las conexiones de datos que haya configurado.
Seleccione los elipsis y **[!UICONTROL Delete]** para eliminar la audiencia.
Seleccione los puntos suspensivos y **[!UICONTROL Editar categorías]** para agregar distintas etiquetas de categoría a la audiencia. Obtenga más información en la sección [categorías](/#categories) a continuación.
Seleccione el nombre de la audiencia para inspeccionar o editar audiencias individuales.

## Ver audiencias individuales {#view-individual-audiences}

La vista de audiencia revela más información sobre su audiencia.

![Ver e inspeccionar audiencia individual.](/help/assets/setup/add-manage-audiences/view-inspect-audience.png)

Las métricas que puede ver en esta pantalla se describen a continuación:

| Elemento | Descripción |
|----------|---------|
| **[!UICONTROL Estado]** | Indica si la audiencia está activa y si se puede utilizar en proyectos. |
| **[!UICONTROL Source]** | Indica la fuente desde la que se importó esta audiencia. En la versión actual de Real-Time CDP Collaboration, Adobe Experience Platform es la única fuente compatible. |
| **[!UICONTROL Conexión de datos]** | Más información detallada acerca de desde dónde se importó esta audiencia. Por ejemplo, al importar audiencias desde el origen de Experience Platform, los entornos limitados individuales a los que su organización tiene acceso se consideran las conexiones de datos. |
| **[!UICONTROL Última actualización]** | Indica la última fecha y hora en que se actualizó cualquier aspecto de esta audiencia. |
| **[!UICONTROL Última actualización por]** | Indica el usuario que actualizó esta audiencia por última vez. |
| **[!UICONTROL Creado]** | Indica cuándo se importó esta audiencia a Real-Time CDP Collaboration. |
| **[!UICONTROL Creado por]** | Indica el usuario que importó la audiencia en Real-Time CDP Collaboration. |


Puede utilizar otros dos controles en la página para editar o eliminar audiencias:

* **[!UICONTROL Eliminar]**: elimine la audiencia de su inventario
* **[!UICONTROL Editar]**: edite los metadatos de la audiencia como su nombre o descripción.

![Ver e inspeccionar audiencia individual.](/help/assets/setup/add-manage-audiences/audiences-edit-delete-controls.png)

A continuación, encontrará más información acerca de la audiencia, que se puede editar parcialmente en los widgets:

![Ver e inspeccionar audiencia individual.](/help/assets/setup/add-manage-audiences/audiences-further-info-boxes.png)

* [Identidades](#identities)
* [Categorías](#categories)
* [Acceso a la conexión](#connection-access)
* [Visibilidad de los metadatos](#metadata-visibility)

### Identidades {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identidades"
>abstract="Obtenga una vista desglosada de las identidades que componen este público, así como un recuento total de los perfiles con las identidades respectivas."

Esta sección indica el número de perfiles presentes en la audiencia con cualquiera de las identidades especificadas al importar las audiencias. La sección también contiene un desglose de identidades para que pueda saber qué identidades conforman la mayor parte de la población de audiencia.

### Categorías {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Categorías"
>abstract="Etiquete sus públicos para facilitar la organización, el filtrado y la recuperación. Puede etiquetar un público con varias categorías y, a continuación, puede utilizar estas etiquetas de categoría para filtrar los públicos que desee en otras áreas del producto."

Para facilitar la organización, el filtrado y la recuperación de audiencias, puede etiquetar sus audiencias. Puede etiquetar una audiencia con varias categorías y, a continuación, puede usar estas etiquetas de categoría para filtrar las audiencias que desee en el área de producto [Discover](/help/guide/collaborate/discover.md) al ejecutar informes de superposición de audiencias.

### Acceso a la conexión {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Acceso a la conexión"
>abstract="<p>Los públicos pueden ser de tres tipos: públicos, privados y personalizados.</p><p> Su disponibilidad para usarlos en proyectos con los colaboradores difiere según la configuración de acceso a la conexión. Siempre puede cambiar el acceso a la conexión de privado a público, pero no puede volver a cambiar esa configuración cuando un público se ha compartido con los colaboradores.</p>"

Seleccione si la audiencia debe ser privada para usted o utilizable y detectable en las conexiones. Las tres opciones disponibles son:

* **[!UICONTROL Público]**. Estas audiencias están disponibles para su uso en informes de superposición y para compartir y activar conexiones con cualquier colaborador.
* **[!UICONTROL Audiencia privada]**. Estas audiencias *no* están disponibles para su uso en informes de superposición y para compartirlas y activarlas en conexiones con colaboradores. Aunque no está disponible para que los colaboradores la vean o usen, la población de esta audiencia sigue contribuyendo a la población total en la vista **[!UICONTROL Todas las audiencias]** en la sección [Discover y superpone](/help/guide/collaborate/discover.md#compare-audiences). Cambie la configuración a pública o personalizada para utilizar las audiencias en conexiones con los colaboradores.
* **[!UICONTROL Audiencia personalizada]**. Estas audiencias están disponibles para usarlas en informes de superposición y para compartirlas y activarlas únicamente en conexiones especificadas. Aunque no está disponible para que todos los colaboradores la vean o usen, la población de esta audiencia sigue contribuyendo a la población total en la vista **[!UICONTROL Todas las audiencias]** en la sección [Discover y superpone](/help/guide/collaborate/discover.md).

>[!IMPORTANT]
>
>Independientemente del estado del acceso (público, privado o personalizado), la población de cualquier audiencia contribuye a la población de **[!UICONTROL Todas las audiencias]** en la vista de análisis de superposición de Audience Discovery. <br> ![La audiencia de **Todas las audiencias** generada por el sistema en el análisis de superposición de detección de audiencias incluye audiencias con todos los estados de acceso a la conexión (pública, privada o personalizada).](/help/assets/setup/add-manage-audiences/all-audiences-view.png "La audiencia **Todas las audiencias** generada por el sistema en el análisis de superposición **Detección de audiencias** incluye audiencias con todos los estados de acceso a la conexión (pública, privada, personalizada)."){width="100" zoomable="yes"}

La disponibilidad de la audiencia para su uso en proyectos con colaboradores difiere según la configuración de acceso a la conexión. Siempre puede cambiar el acceso a la conexión de privado a público, pero no puede volver a cambiar esa configuración cuando un público se ha compartido con los colaboradores.

### Visibilidad de los metadatos {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Visibilidad de los metadatos"
>abstract="<p>Indica qué información de metadatos del público es visible para otras organizaciones antes de conectarse con su organización. </p> <p> **Recuento de identidades** controla si su socio puede ver los recuentos de identidades de sus públicos cuando visualiza los informes de superposición en la pestaña de detección. **% de solapamiento de público** controla si los colaboradores pueden descubrir los porcentajes de solapamiento entre sus públicos y los suyos."

>[!NOTE]
>
>Si su colaborador tiene todas las audiencias definidas como privadas, la vista **[!UICONTROL Audiencias relevantes]** en las perspectivas de audiencia estará en blanco. [Más información](/help/guide/collaborate/discover.md#relevant-audiences).

Indica qué información de los metadatos de audiencia es visible para otras organizaciones antes de conectarse con su organización o en diferentes vistas de proyecto.

**[!UICONTROL Mostrar recuento de identidad]**: esta opción controla si tu pareja puede ver los recuentos de identidad de tus audiencias al [ver informes de superposición en la pestaña de detección](/help/guide/collaborate/discover.md#discover-overlaps).

![Imágenes en paralelo con la opción Mostrar recuento de identidades no seleccionada y seleccionada.](/help/assets/setup/add-manage-audiences/show-identity-count.png)

**[!UICONTROL Mostrar superposición de audiencias %]**: cuando se establece en true, los colaboradores pueden [descubrir porcentajes de superposición](/help/guide/collaborate/discover.md#compare-audiences) entre sus audiencias y la audiencia que le pertenece. Por ejemplo, en la grabación siguiente, la audiencia `agora-advertiser-aud3` tiene esta configuración establecida en true y un colaborador puede ver porcentajes de superposición con esa audiencia. La audiencia `agora-advertiser-aud1` tiene esta configuración establecida en false, por lo que el colaborador no puede ver porcentajes de superposición.

![Porcentaje de superposición de audiencia para dos audiencias diferentes.](/help/assets/setup/add-manage-audiences/audience-overlap-percentage.gif)

## Pasos siguientes

Después de importar audiencias, usa la sección [Conectar](/help/guide/connect/establishing-connections.md) para descubrir editores con los que conectarte y comenzar a colaborar en proyectos.
