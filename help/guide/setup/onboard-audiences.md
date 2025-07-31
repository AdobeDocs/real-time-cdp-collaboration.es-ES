---
title: Source y administración de audiencias
description: Obtenga información sobre cómo crear y administrar audiencias en Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: 608706d00124372ac59209478ab551a3a6ce0226
workflow-type: tm+mt
source-wordcount: '2897'
ht-degree: 18%

---

# Source y administración de audiencias

{{limited-availability-release-note}}

Las audiencias son grupos específicos de usuarios o clientes segmentados según varios atributos. Esto permite a los colaboradores colaborar en marketing segmentado y experiencias personalizadas para lograr campañas publicitarias más eficaces. Esta guía explica cómo crear audiencias en Real-Time CDP Collaboration, ver el panel de audiencias y administrar audiencias individuales.

>[!BEGINSHADEBOX]

Lo que encontrará en esta página de documentación:

* [Audiencias de Source en Collaboration](#source-audiences)
* [Panel de vista de públicos](#view-audiences-dashboard)
* [Ver audiencias individuales](#view-individual-audiences)

>[!ENDSHADEBOX]

## Audiencias de Source en Collaboration {#source-audiences}

>[!IMPORTANT]
>
>Para las audiencias de origen, el usuario debe asignarse a una función que contenga dos permisos de Administración de perfiles: **[!UICONTROL Ver perfiles]** y **[!UICONTROL Ver segmentos]**. Para obtener información sobre cómo asignar los permisos necesarios, consulte la guía [obtención de audiencias](../permissions/overview.md#audience-sourcing) en permisos.

Para poder activar audiencias con colaboradores y ejecutar cálculos de superposición, las audiencias deben proceder de Collaboration. Para crear audiencias de origen, siga los pasos de flujo de trabajo de la sección siguiente.

En la ficha **[!UICONTROL Mis audiencias]** del área de trabajo **[!UICONTROL Configuración]**, seleccione el icono Agregar (![Agregar icono.](/help/assets/icons/plus.png)) y luego seleccione **[!UICONTROL Audiencia]**. Si esta es su primera audiencia, también puede seleccionar la opción **[!UICONTROL Agregar]**.

![Área de trabajo de Mis audiencias con la opción Agregar y las opciones de Audiencias resaltadas.](/help/assets/setup/add-manage-audiences/add-audiences.png)

### Seleccionar conexión de datos {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Acción de marketing"
>abstract="<p>Utilice acciones de marketing para controlar qué datos del público se importarán a Real-Time CDP Collaboration desde Experience Platform. La acción de marketing <strong>Colaboración de datos</strong> admite las etiquetas de uso de datos C4, C5 y C9. La acción de marketing <strong>Ciencia de datos</strong> admite la etiqueta de uso de datos C9.</p> <p> <ul><li> Con la casilla de verificación <em>habilitada</em>, cualquier dato marcado con las etiquetas llamadas arriba en Experience Platform se excluye y <strong>no</strong> se incorpora a Real-Time CDP Collaboration.</li><li> Con la casilla de verificación <em>deshabilitada</em>, no hay restricciones en los datos de Experience Platform que se pueden importar a Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=es" text="Información general sobre las etiquetas de uso de datos"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=es" text="Glosario de etiquetas de uso de datos"

>[!IMPORTANT]
>
>Después de establecer en la primera conexión de datos e importar la primera audiencia, puede importar varias audiencias desde la conexión de datos existente. Al agregar audiencias adicionales, empezará desde el paso [seleccionar audiencia](#select-audiences), ya que la conexión de datos ya se ha establecido.

Una conexión de datos es la fuente de datos desde la que se obtienen las audiencias. Actualmente, la única conexión de datos admitida es Adobe Experience Platform.

Cualquier configuración, como la programación, que configure para la conexión de datos se aplica a todas las audiencias procedentes de esta conexión de datos.

>[!TIP]
>
>Hay un flujo de trabajo independiente en el que puede ver y editar las conexiones de datos. Para obtener más información, consulte la guía [administración de conexiones de datos](/help/guide/setup/manage-data-connection.md).

Para empezar a agregar su conexión de datos, seleccione **[!UICONTROL Agregar una nueva conexión de datos]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.

![Espacio de trabajo Agregar audiencias con la opción Agregar una nueva conexión de datos resaltada.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

#### Seleccionar fuente de datos

A continuación, elegirá el origen de la conexión de datos. Las fuentes disponibles incluyen:

* **Adobe Experience Platform**: selecciona esta opción para traer tus audiencias desde Adobe Experience Platform.
* **Archivo CSV** (versión futura): cargue un archivo CSV que contenga los datos de su audiencia para introducir datos de forma rápida y directa.
* **Amazon Web Service** (versión futura): conéctese a su almacenamiento de Amazon S3 para obtener datos de audiencia directamente desde sus bloques de S3.
* **Snowflake** (versión futura): Use su almacén de datos de Snowflake para extraer datos de audiencia sin problemas.
* **Google Cloud Platform** (versión futura): conéctese a su almacenamiento de Google Cloud para obtener datos de audiencia directamente de sus bloques de GCS.

Seleccione su fuente de datos y luego seleccione **[!UICONTROL Siguiente]**.

![Espacio de trabajo Agregar audiencias con la opción Adobe Experience Platform resaltada.](/help/assets/setup/add-manage-audiences/select-data-connection-source.png)

#### Selección de zona protegida

Después de seleccionar la fuente de datos, debe seleccionar la zona protegida que incluye las audiencias que desea utilizar en Collaboration. Seleccione la zona protegida de la lista de zonas protegidas disponibles y, a continuación, seleccione **[!UICONTROL Siguiente]**

![Espacio de trabajo Agregar audiencias con una zona protegida seleccionada.](/help/assets/setup/add-manage-audiences/select-sandbox.png)

#### Política de gobernanza y acciones de cumplimiento {#governance-policy-and-enforcement-actions}

A continuación, debe asegurarse de que las acciones de marketing correctas se establecen en los datos de origen. También debe dar su consentimiento para que los datos procedentes de Experience Platform se utilicen para la colaboración de datos.

Utilice acciones de marketing para controlar qué datos de audiencia introducir en Collaboration desde Experience Platform. La acción de marketing **[!UICONTROL Colaboración de datos]** admite las etiquetas de uso de datos C4, C5 y C9. La acción de marketing **[!UICONTROL Ciencia de datos]** admite la etiqueta de uso de datos C9.

Obtenga más información sobre las [etiquetas de uso de datos C4, C5 y C9](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* Si la casilla de verificación está ***habilitada***, se excluirán todos los datos etiquetados en Experience Platform como se describió anteriormente y **no** se incluirán en Collaboration.
* Con la casilla de verificación ***deshabilitada***, no hay restricciones en los datos procedentes de Experience Platform.

Obtenga más información sobre las etiquetas de uso de datos en la documentación de Experience Platform:

* [Información general sobre las etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Glosario de etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Además, debe seleccionar las reglas de consentimiento que se aplicarán a los datos que se obtienen en Collaboration.

![Espacio de trabajo Agregar audiencias en la sección Directiva de administración y acciones de cumplimiento.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

Una vez que haya seleccionado las acciones de marketing y las reglas de consentimiento, seleccione **[!UICONTROL Siguiente]** para continuar con el paso siguiente. Aparecerá un cuadro de diálogo de confirmación en el que se le pedirá que acepte los términos. Seleccione la casilla de verificación y, a continuación, seleccione **[!UICONTROL Aceptar]** para confirmar.

![Cuadro de diálogo Directiva de gobernanza y acciones de aplicación con la casilla de verificación y la opción Aceptar resaltadas.](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png)

### Proporcionar detalles

A continuación, proporcione un nombre y una descripción para la conexión de datos. Esta información le ayudará a identificar la conexión de datos más adelante.

![El área de trabajo Agregar audiencias tiene la opción de proporcionar un nombre y una descripción.](/help/assets/setup/add-manage-audiences/data-connection-details.png)

### Asignar campos {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Campos de origen"
>abstract="Los campos de origen son espacios de nombres de identidad y atributos de la implementación de Experience Platform. Puede asignarlos a los campos de destino definidos en Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Campos de destino"
>abstract="Actualmente, los correos electrónicos con hash son las únicas claves de coincidencia admitidas."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Aplicar transformación"
>abstract="Al importar campos *sin hash* desde su origen, utilice esta opción para que Collaboration aplique el hash y transforme los campos sin formato en campos con hash."

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

A continuación, seleccione los campos de origen para asignarlos a los campos de destino en Collaboration.

![Espacio de trabajo Agregar audiencias con la opción de asignar campos de origen a campos de destino.](/help/assets/setup/add-manage-audiences/add-map-fields.png)

>[!TIP]
>
>Puede asignar varios campos de origen al mismo campo de destino. Por ejemplo, si tiene direcciones de correo electrónico en dos campos distintos en Experience Platform, puede asignar cada uno de ellos al campo de destino **[!UICONTROL Correo electrónico con hash]** como dos filas independientes.

>[!BEGINSHADEBOX]

**[!UICONTROL Los campos de Source]** son áreas de nombres y atributos de identidad de Experience Platform. Así es como existen las identidades en la plataforma desde la que obtiene datos. Los campos de Source se asignan a los campos de destino definidos en Collaboration.

**[!UICONTROL Campos de destino]** indican cómo se hace referencia a las identidades en Collaboration. Actualmente, los correos electrónicos con hash son las únicas claves de coincidencia admitidas.

Utilice la opción **[!UICONTROL Aplicar transformación]** al importar *campos sin hash* desde su origen. En este caso, Collaboration aplica el hash y transforma los campos. El algoritmo hash utilizado por Adobe es SHA256.

>[!ENDSHADEBOX]

Seleccione el campo de origen vacío junto al campo de destino. Aparecerá el cuadro de diálogo **[!UICONTROL Seleccionar campo de origen]**. Seleccione entre las opciones **[!UICONTROL Áreas de nombres de identidad]** y **[!UICONTROL Atributos de perfil]** para encontrar el campo de origen deseado y, a continuación, seleccione el campo en la lista. También puede utilizar la opción de búsqueda para encontrar el campo deseado.

![Cuadro de diálogo Seleccionar campo de origen con las opciones de correo electrónico mostradas.](/help/assets/setup/add-manage-audiences/select-source-field.png)

Para administrar varios campos de correo electrónico, asigne el campo de origen de correo electrónico sin hash con **[!UICONTROL Aplicar transformación]**.

![Espacio de trabajo Agregar audiencias con los campos de origen de correo electrónico asignados al campo de destino, con la opción Aplicar transformación activada para uno.](/help/assets/setup/add-manage-audiences/apply-transformation.png)

Siga agregando pares de asignación según sea necesario y, a continuación, seleccione **[!UICONTROL Siguiente]**.

### Programación {#schedule}

A continuación, programe cuándo comenzar y terminar de rellenar las audiencias. La audiencia se actualizará según esta programación.

![Espacio de trabajo Agregar audiencia con las opciones de programación mostradas.](/help/assets/setup/add-manage-audiences/audience-scheduling.png)

>[!IMPORTANT]
>
>Ajustar la frecuencia de las actualizaciones de audiencias ayudará a administrar la [actividad de crédito de Gestión de público](/help/guide/setup/my-activity.md#types-of-activities), que se calcula por actualización de audiencia. La selección de una frecuencia mayor puede afectar a la actualización de los datos disponibles para los informes de detección de audiencias y la activación de audiencias.

Seleccione la frecuencia de actualización de la audiencia en el menú desplegable **[!UICONTROL Frecuencia]**.

![Espacio de trabajo de programación Agregar audiencias con la lista desplegable Frecuencia abierta.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png)

A continuación, seleccione **[!UICONTROL Intervalo de fecha]**. La fecha de inicio es la fecha en la que la audiencia empezará a rellenarse con perfiles y la fecha de finalización es cuando la audiencia dejará de actualizarse.

![Espacio de trabajo de programación Agregar audiencias con la opción Intervalo de fechas mostrada.](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png)

>[!IMPORTANT]
>
>Después de la fecha de finalización en el intervalo de fechas, todas las audiencias procedentes de esta conexión de datos dejarán de actualizarse. Para renovar la conexión, sigue la guía [administrar conexión de datos](/help/guide/setup/manage-data-connection.md).

### Seleccionar públicos {#select-audiences}

Después de seleccionar la fuente de audiencia, elegirá las audiencias específicas que desea incluir. Utilice las opciones de búsqueda y filtro para encontrar las audiencias relevantes de la fuente de datos. Seleccione las audiencias que desee y luego seleccione **[!UICONTROL Siguiente]**.

![Espacio de trabajo Agregar audiencias con una lista de audiencias disponibles.](/help/assets/setup/add-manage-audiences/select-audience.png)

### Revisión

Revise todas las configuraciones y ajustes de antes de finalizar la adición de audiencias. Asegúrese de que todos los detalles sean correctos y, a continuación, seleccione **[!UICONTROL Completar]** para finalizar la creación de la conexión de datos.

![Espacio de trabajo Agregar audiencias con todas las configuraciones seleccionadas mostradas.](/help/assets/setup/add-manage-audiences/review-connection.png)

## Panel de vista de públicos {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Identidades que faltan"
>abstract="El recuento de identidades estará disponible tras la siguiente actualización de la conexión de datos siguiendo la programación configurada. La actualización inicial suele producirse en las 24 horas siguientes al establecimiento de la conexión de datos. Las actualizaciones continuas seguirán la programación configurada."

Después de obtener audiencias, el área de trabajo **[!UICONTROL Mis audiencias]** muestra todas las audiencias que provienen actualmente de Collaboration.

Cada audiencia contiene una descripción general de la siguiente información:

| Elemento | Descripción |
|----------|---------|
| **[!UICONTROL Identidades]** | Indica el número de identidades presentes en esta audiencia. Tenga en cuenta que si el mismo perfil tiene dos o más identidades y estas identidades se utilizan como claves de coincidencia en el proyecto, el perfil aparecerá dos veces en el recuento. |
| **[!UICONTROL Estado]** | Indica si la audiencia está activa y si se puede utilizar en proyectos. El estado **[!UICONTROL Pendiente]** indica que la audiencia se ha originado recientemente y que las identidades aún no se han rellenado. Las audiencias de origen se rellenarán con perfiles después de la actualización inicial, que generalmente se produce dentro de las 24 horas siguientes a la configuración de la conexión de datos. |
| **[!UICONTROL Source]** | Indica el origen de la audiencia. En la versión actual de Collaboration, Experience Platform es la única fuente compatible. |
| **[!UICONTROL Conexión de datos]** | La conexión de datos desde la que se origina la audiencia. Puede seleccionar el nombre para ver la conexión de datos. |
| **[!UICONTROL Acceso a la conexión]** | Define si la audiencia es pública o privada. Las audiencias públicas se pueden descubrir en los informes de superposición y se pueden activar dentro de un proyecto. |
| **[!UICONTROL Creado]** | Indica cuándo se originó la audiencia inicialmente en Collaboration. |
| **[!UICONTROL Última actualización]** | Indica la última fecha y hora en que la audiencia se actualizó en Collaboration. Esto no hace referencia a la última actualización de la audiencia, sino a la última modificación de la configuración o los metadatos de la audiencia. |

![Área de trabajo de Mi audiencia que muestra todas las audiencias de origen.](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

Para realizar acciones rápidas en una audiencia, seleccione los puntos suspensivos **...** junto al nombre de la audiencia. Las opciones disponibles son las siguientes:

* **[!UICONTROL Editar categorías]** le permite agregar diferentes etiquetas de categoría a la audiencia. Para obtener más información, consulte la sección [categorías](#categories) a continuación.
* **[!UICONTROL Eliminar]** eliminará la audiencia de la conexión de datos.

![Área de trabajo Mis audiencias con el menú de los tres puntos abierto y las opciones Editar categorías y Eliminar resaltadas.](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png)

## Ver audiencias individuales {#view-individual-audiences}

Para ver más información y editar las configuraciones de una audiencia individual, selecciona la audiencia en el espacio de trabajo **[!UICONTROL Mis audiencias]**. El espacio de trabajo de audiencia muestra información detallada sobre la audiencia seleccionada, incluidos detalles, identidades, categorías, acceso a conexiones y configuración de visibilidad de metadatos.

### Detalles de público

Se muestra la siguiente información para cada audiencia individual:

| Elemento | Descripción |
|----------|---------|
| **[!UICONTROL Estado]** | Indica si la audiencia está activa y si se puede utilizar en proyectos. |
| **[!UICONTROL Source]** | Indica el origen de la audiencia. En la versión actual de Collaboration, Experience Platform es la única fuente compatible. |
| **[!UICONTROL Conexión de datos]** | La conexión de datos desde la que se origina la audiencia. |
| **[!UICONTROL Última actualización]** | Indica la última fecha y hora en que la audiencia se actualizó en Collaboration. Esto no hace referencia a la última actualización de la audiencia, sino a la última modificación de la configuración o los metadatos de la audiencia |
| **[!UICONTROL Última actualización por]** | Indica el usuario que actualizó la audiencia por última vez. |
| **[!UICONTROL Creado]** | Indica cuándo se originó la audiencia inicialmente en Collaboration. |
| **[!UICONTROL Creado por]** | Indica el usuario que originó la audiencia en Collaboration. |

![Espacio de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details.png)

Además, los siguientes controles están disponibles en el espacio de trabajo de audiencia:

* **[!UICONTROL Eliminar]**: elimine la audiencia de su conexión de datos.
* **[!UICONTROL Editar]**: edite el nombre o la descripción de la audiencia.

![Espacio de trabajo de una audiencia individual con la opción Editar y eliminar resaltada.](/help/assets/setup/add-manage-audiences/audience-details-edit-delete.png)

A continuación, puede actualizar las secciones siguientes en el espacio de trabajo de la audiencia:

* [Identidades](#identities)
* [Categorías](#categories)
* [Acceso a la conexión](#connection-access)
* [Visibilidad de los metadatos](#metadata-visibility)

### Identidades {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identidades"
>abstract="Obtenga una vista desglosada de las identidades que componen este público, así como un recuento total de los perfiles con las identidades respectivas."

La sección **[!UICONTROL Identidades]** indica el número de perfiles presentes en la audiencia con cualquiera de las identidades seleccionadas al obtener la audiencia. La sección también contiene un desglose de identidades para que pueda saber qué identidades conforman la mayor parte de la población de audiencia.

![La sección Identidades del espacio de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

### Categorías {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Categorías"
>abstract="Etiquete sus públicos para facilitar la organización, el filtrado y la recuperación. Puede etiquetar un público con varias categorías y, a continuación, puede utilizar estas etiquetas de categoría para filtrar los públicos que desee en otras áreas del producto."

Para facilitar la organización, el filtrado y la recuperación de audiencias, puede etiquetar sus audiencias. Puede etiquetar una audiencia con varias categorías y, a continuación, puede usar estas etiquetas de categoría para filtrar las audiencias que desee en el área de producto [Discover](/help/guide/collaborate/discover.md) al ejecutar informes de superposición de audiencias.

Para agregar categorías, seleccione la opción **[!UICONTROL Editar]** en la sección **[!UICONTROL Categorías]**.

![La sección Categorías del espacio de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details-categories.png)

Aparecerá el cuadro de diálogo **[!UICONTROL Categorías]**, que le permitirá seleccionar las categorías que desee agregar a la audiencia. Para seleccionar una categoría individual, marque la casilla que hay junto al nombre de la categoría.

![Cuadro de diálogo Categorías con las categorías disponibles mostradas.](/help/assets/setup/add-manage-audiences/audience-details-categories-select.png)

### Acceso a la conexión {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Acceso a la conexión"
>abstract="<p>Los públicos pueden ser de tres tipos: públicos, privados y personalizados.</p><p> Su disponibilidad para usarlos en proyectos con los colaboradores difiere según la configuración de acceso a la conexión. Siempre puede cambiar el acceso a la conexión de privado a público, pero no puede volver a cambiar esa configuración cuando un público se haya compartido con los colaboradores.</p>"

La disponibilidad de una audiencia para su uso en proyectos con colaboradores difiere según la configuración de acceso a la conexión. En la sección **[!UICONTROL Acceso a la conexión]**, puede seleccionar si la audiencia debe ser privada o pública. Las audiencias públicas se pueden utilizar y detectar en conexiones.

Para actualizar el acceso a la conexión de la audiencia, seleccione la opción **[!UICONTROL Editar]** en la sección **[!UICONTROL Acceso a la conexión]**.

![La sección de acceso a la conexión del área de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png)

Aparecerá el cuadro de diálogo **[!UICONTROL Acceso a conexión]**, con tres opciones de acceso a conexión disponibles:

* **[!UICONTROL Audiencia privada]**. Estas audiencias *no* están disponibles para su uso en informes de superposición o para su activación en conexiones con colaboradores. Aunque las audiencias no están disponibles para que los colaboradores las vean o utilicen, la población de las audiencias sigue contribuyendo a la población total en la vista **[!UICONTROL Todas las audiencias]** en la sección [comparar audiencias](/help/guide/collaborate/discover.md#compare-audiences). Cambie la configuración a pública o personalizada para utilizar las audiencias en conexiones con los colaboradores.
* **[!UICONTROL Público]**. Estas audiencias están disponibles para usarlas en informes de superposición y para activarlas en conexiones con cualquier colaborador.
* **[!UICONTROL Audiencia personalizada]**. Estas audiencias están disponibles para usarlas en informes de superposición y solo para activarlas en conexiones especificadas. Aunque las audiencias no están disponibles para que los colaboradores las vean o utilicen, la población de las audiencias sigue contribuyendo a la población total en la vista **[!UICONTROL Todas las audiencias]** en la sección [comparar audiencias](/help/guide/collaborate/discover.md#compare-audiences).

Seleccione la opción de acceso a la conexión que desee y, a continuación, seleccione **[!UICONTROL Guardar]** para aplicar los cambios.

![Cuadro de diálogo de acceso a la conexión con las opciones disponibles mostradas.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

>[!IMPORTANT]
>
>Independientemente del estado del acceso (público, privado o personalizado), la población de cualquier audiencia contribuye a la población de **[!UICONTROL Todas las audiencias]** en la sección **[!UICONTROL Comparar audiencias]** dentro de un proyecto.

La disponibilidad de la audiencia para su uso en proyectos con colaboradores difiere según la configuración de acceso a la conexión. Siempre puede cambiar la conexión de acceso de privada a pública, pero no puede volver a cambiar esa configuración una vez que se activa una audiencia.

### Visibilidad de los metadatos {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Visibilidad de los metadatos"
>abstract="<p>Indica qué metadatos del público son visibles para otros colaboradores antes de que se conecten con usted o dentro de las vistas del proyecto.</p> <p> **Recuento de identidades** controla si su colaborador puede ver los recuentos de identidades de sus públicos cuando visualiza los informes de superposición en la pestaña de detección. **% de solapamiento de público** controla si los colaboradores pueden descubrir los porcentajes de solapamiento entre sus públicos y los suyos."

>[!NOTE]
>
>Si su colaborador tiene todas las audiencias definidas como privadas, la sección **[!UICONTROL Audiencias relevantes]** de un proyecto en el área de trabajo **[!UICONTROL Discover]** estará en blanco. Para obtener más información, lea la guía [Discover](/help/guide/collaborate/discover.md#relevant-audiences).

La visibilidad de los metadatos indica la visibilidad de los metadatos de una audiencia para otros colaboradores antes de que se conecten con usted o en diferentes vistas de proyecto. Para actualizar la visibilidad de los metadatos de la audiencia, seleccione la opción **[!UICONTROL Editar]** en la sección **[!UICONTROL Visibilidad de los metadatos]**.

![La sección de visibilidad de metadatos del espacio de trabajo de una audiencia individual.](/help/assets/setup/add-manage-audiences/audience-details-metadata.png)

Aparece el cuadro de diálogo **[!UICONTROL Visibilidad de metadatos]**, que le permite configurar las opciones de visibilidad de la audiencia. Hay dos ajustes de visibilidad de metadatos que puede configurar para cada audiencia:

**[!UICONTROL Mostrar recuento de identidades]**: esta opción controla si el colaborador puede ver los recuentos de identidades de las audiencias al [ver informes de superposición en la ficha de detección](/help/guide/collaborate/discover.md#discover-overlaps) dentro de un proyecto.

**[!UICONTROL Mostrar superposición de audiencias %]**: esta opción controla si los colaboradores pueden [descubrir porcentajes de superposición](/help/guide/collaborate/discover.md#compare-audiences) entre sus audiencias y las suyas.

![Cuadro de diálogo de visibilidad de metadatos con las opciones disponibles mostradas.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

## Próximos pasos

Después de obtener audiencias, es hora de descubrir editores con los que [conectar](/help/guide/connect/establishing-connections.md) para colaborar en proyectos.
