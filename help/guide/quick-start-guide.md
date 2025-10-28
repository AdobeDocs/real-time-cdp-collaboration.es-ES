---
title: Guía de inicio rápido de Real-Time CDP Collaboration
description: Obtenga información sobre cómo incorporar su organización en Real-Time CDP Collaboration, incluida la configuración de funciones y organizaciones, el abastecimiento de audiencias, la activación y la medición. Esta guía ayuda a los colaboradores a configurar las opciones de conexión para empezar a utilizar sus audiencias de forma segura y eficaz.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
source-git-commit: 9355535e067afeedff33f5c6468bc6fcb1f58e08
workflow-type: tm+mt
source-wordcount: '1394'
ht-degree: 0%

---

# Guía de inicio rápido de Real-Time CDP Collaboration

{{limited-availability-release-note}}

Comience a usar Real-Time CDP Collaboration configurando su organización, obteniendo audiencias y habilitando la activación y medición centradas en la privacidad.

## Requisitos previos

Antes de empezar, asegúrese de que dispone de lo siguiente:

- Licencia de Real-Time CDP Collaboration activa.
- [Acceso de administrador de sistema o producto a Adobe Experience Platform](./permissions/overview.md).
- [Acceso aprovisionado para usuarios finales](./permissions/manage-user-access.md).
- [Roles creados para su organización y asignados a usuarios](./permissions/manage-roles.md).
- Acceso a recursos de promoción de la marca, como el nombre, el logotipo y el banner de su organización.
- Una [estrategia de clave de coincidencia definida](./setup/onboard-account.md#set-up-match-keys)
- (Opcional) Acceso a una fuente en la nube compatible (Amazon S3 o Snowflake) si no utiliza Experience Platform para la gestión de público.

## Paso 1: completar la configuración basada en funciones {#complete-role-based-setup}

Las funciones de acceso de su organización determinan lo que los usuarios pueden ver y hacer en Collaboration. Antes de continuar, asegúrese de que los permisos basados en funciones están correctamente configurados para garantizar el acceso y la visibilidad adecuados en la plataforma.

**Recursos:**

- [Documentación de acceso de usuario](./permissions/manage-user-access.md)
- [Documentación de configuración de rol](./permissions/manage-roles.md)


Vea este vídeo para aprender a asignar acceso y permisos de producto para Collaboration mediante Admin Console y Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452216/?learn=on&enablevpops)

## Paso 2: Configurar su cuenta de Collaboration {#set-up-your-account}

Para poder crear audiencias de origen, debe configurar la cuenta en Collaboration. Esto determina cómo aparece y a qué se puede acceder en la interfaz.

Si no tiene el acceso necesario, vuelva al paso 1 o póngase en contacto con el administrador de su organización para que le ayude a completar esta configuración.

Defina la función de su cuenta en Collaboration, proporcione recursos de promoción de la marca y configure las claves de coincidencia para alinear las audiencias entre conexiones.

>[!NOTE]
>
>Puede crear una o varias cuentas (como anunciante y editor) durante la configuración. Algunos campos, como los recursos de personalización de marca y el correo electrónico de contacto, se pueden actualizar más adelante en el área de trabajo **[!UICONTROL Configuración]**.

- **Asignar un rol** - Determina si su cuenta es un anunciante o un editor. Su función define qué capacidades tiene en Collaboration. Para obtener más información sobre cómo afectan las funciones al flujo de trabajo de colaboración, consulte la guía [funciones](./overview/roles.md).
- **Recursos de promoción de la marca** - Agregue lo siguiente a su cuenta:
   - Nombre de cuenta (máximo 100 caracteres)
   - Descripción (máximo de 1000 caracteres)
   - Logotipo (SVG &lt;20 KB, idealmente cuadrado)

>[!NOTE]
>
>Si va a crear una cuenta de publicador y desea que sea visible públicamente en el catálogo de conexiones de Collaboration, póngase en contacto con el representante de la cuenta de Adobe. Las cuentas de Publisher requieren un banner de marca personalizado (JPG 2688x1536); este archivo se puede compartir directamente con el representante.

- **Correo electrónico de contacto**: proporcione un correo electrónico empresarial para que lo utilicen los colaboradores después de establecer una conexión.
- **Configurar claves de coincidencia**: seleccione los identificadores utilizados para la coincidencia de audiencias.

Para obtener más información sobre la configuración inicial de la cuenta, incluido cómo definir funciones, cargar recursos de promoción de la marca y configurar claves de coincidencia, consulte la guía [configuración inicial de la cuenta](./setup/onboard-account.md#initial-account-setup){target="_blank"}.

Vea este vídeo para obtener una guía paso a paso de la configuración de un anunciante, incluida la creación de cuentas, la promoción de la marca y la configuración de claves de coincidencia.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Paso 3: Audiencias de Source (desde Experience Platform o una fuente de nube) {#source-audiences}

Una vez creada la cuenta y configuradas las claves de personalización de marca y de coincidencia, está listo para empezar a obtener audiencias. Elija uno de los siguientes métodos de abastecimiento en función de sus necesidades comerciales y de su almacén de datos.

### Opción A: Source de Experience Platform

[Use Collaboration para vincular una zona protegida que contenga audiencias](./setup/onboard-audiences.md). Utilice este método de autoservicio para hacer referencia a segmentos de audiencia existentes desde su instancia de Experience Platform.

#### Configuración de audiencias

Configure cómo se preparan, comparan y controlan las audiencias para su uso en conexiones.

- **Seleccionar audiencias** *(solo Experience Platform)*: elija segmentos de audiencia con identificadores admitidos.
- **Asignar claves de coincidencia** - Alinear campos de audiencia con las claves de coincidencia configuradas.
- **Aplicar transformaciones**: utilice valores de texto sin formato hash (por ejemplo, correo electrónico) si es necesario.
- **Actualizaciones de programación**: defina la frecuencia de actualización (por ejemplo, diaria).
- **Configurar la configuración de consentimiento** - Determine qué perfiles cumplen los requisitos para ser incluidos en las conexiones seleccionando un modo de consentimiento: Opt-in, Opt-out o none.

>[!NOTE]
>
>Puede añadir o quitar audiencias y actualizar la programación de actualización directamente en Collaboration. Para cambiar otras configuraciones, como las claves de coincidencia o el modo de consentimiento, debe eliminar y volver a crear la conexión de datos.

>[!IMPORTANT]
>
>**Número máximo de audiencias por rol de colaborador:**
>
>- **Anunciantes** pueden obtener hasta 25 audiencias.
>- **Los editores** pueden obtener hasta 250 audiencias (cada una con un mínimo de 1.000 ID).

>[!IMPORTANT]
>
>**Requisitos de clave de coincidencia:**
>
>Todas las claves de coincidencia deben estar **recortadas**, **en minúsculas**
>&#x200B;>Las claves de coincidencia con hash deben ser **SHA256-hashed**.\
>Si proporciona valores hash con caracteres en mayúsculas, Collaboration los convierte automáticamente a minúsculas.\
>Si su origen contiene **identificadores de texto sin formato**, use la opción **[!UICONTROL Aplicar transformación]** para aplicar el hash. Esta opción solo está disponible cuando obtiene audiencias de Experience Platform y no es compatible con fuentes basadas en la nube.
>
>Para obtener más información, consulte la sección [asignar campos](./setup/onboard-audiences.md#map-fields) de la guía de origen y administración de audiencias.

Para ver una introducción completa sobre cómo crear audiencias con Collaboration, vea el siguiente vídeo.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

También puede ver el documento sobre [audiencias de abastecimiento en Collaboration](./setup/onboard-audiences.md#source-and-manage-audiences).

### Opción B: Source desde Snowflake o Amazon S3

Para configurar una fuente de nube (por ejemplo, [!DNL AWS S3] o [!DNL Snowflake]), prepare los datos de audiencia con la siguiente [especificación de audiencia PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.1.pdf). Una vez finalizado, o si tiene alguna pregunta, póngase en contacto con el representante de su cuenta de Adobe para finalizar la configuración. Este método no es de autoservicio y requiere la asistencia de Adobe.

<!-- Add in the below in final draft: 

To configure a cloud source, such as [!DNL Snowflake] or [!DNL AWS S3], prepare your audience data using the [Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.1)

[!DNL AWS S3] can now be configured as a self-service source. For setup instructions, see the [AWS S3 sourcing guide](./setup/configure-aws-s3-audience-sourcing.md)

If you are using [!DNL Snowflake], or other cloud service provider, contact your Adobe account representative to finalize the setup. -->

>[!IMPORTANT]
>
>Los archivos de audiencia basados en la nube deben seguir el esquema requerido descrito en la Especificación de audiencias de PDF. Los archivos deben incluir identificadores hash (SHA256 en minúsculas), campos de metadatos requeridos como `segment_name` y `activation_id`, y usar formatos compatibles como CSV o Parquet. Adobe no normaliza los datos antes de la activación. El TTL se aplica en función de la duración de la audiencia.
>
>Todas las audiencias del archivo cargado tienen un origen completo en este momento. La configuración de [visibilidad de la audiencia](/help/guide/setup/onboard-audiences.md#metadata-visibility) determina si los colaboradores pueden ver la audiencia y se administra mediante la interfaz de usuario de Collaboration.

## Paso 4: Activar audiencias (en Experience Platform o en un destino de nube) {#activate-audiences}

A continuación, active las audiencias en su instancia de Experience Platform o en un destino de nube.

### Opción A: Activar en Experience Platform

Complete los siguientes pasos descritos en la guía [configurar Adobe Experience Platform como destino](/help/guide/destinations/experience-platform.md).

- **Crear un destino**: use la interfaz de usuario para configurar un destino de Experience Platform (nivel de zona protegida).
- **Asignar claves de coincidencia** - Seleccione el identificador (por ejemplo, `hashedEmail`).
- **Definir TTL** - Establecer caducidad (de 1 a 30 días).
- **Verificar en el portal de audiencia**: una vez que un colaborador le envíe una audiencia, compruebe que aparece en el portal de audiencia bajo el origen &quot;[!UICONTROL Real-Time CDP Collaboration]&quot;.

### Opción B: Activar en la nube

Para configurar un destino de nube (por ejemplo, [!DNL AWS S3] o [!DNL Snowflake]), póngase en contacto con el representante de su cuenta de Adobe para iniciar el proceso de configuración. Según el destino en la nube, deberá proporcionar detalles de destino en la nube, como la ruta del archivo, las credenciales, los localizadores de cuentas, etc. Una vez que se proporcione la información necesaria, Adobe configurará el destino de la nube.

Los datos de audiencia enviados a un destino de nube siguen un esquema predefinido. Para obtener una descripción detallada de los campos y el formato requeridos, descargue la [Guía de Collaboration Audience Activation](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

## Paso 5: Configurar la medición (opcional) {#set-up-measurement}

>[!AVAILABILITY]
>
>Esta característica está en **beta** y está disponible en exclusiva para los clientes del programa de disponibilidad limitada. Póngase en contacto con su representante de Adobe para solicitar acceso.

>[!IMPORTANT]
>
>El área de trabajo **[!UICONTROL Measure]** solo está disponible si el caso de uso **[!UICONTROL Measurement]** se habilitó [durante el proceso de conexión](./connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./collaborate/manage-projects.md#project-use-cases).

Collaboration ofrece una variedad de informes para analizar el alcance, la frecuencia y la eficacia de las campañas. Mientras que el espacio de trabajo **[!UICONTROL Measure]** está disponible en la interfaz de usuario, la funcionalidad completa de creación de informes puede requerir la habilitación del servidor.

Para aprender a ver e interpretar los informes de medición, consulte la [Guía de medición](./collaborate/measure.md). Abarca la atribución, las métricas de resumen de la campaña y los paneles, como las curvas de alcance y la distribución de frecuencias.

<!-- 
Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."

### Configure measurement workflow

Collaboration supports two measurement workflows:

- **Attribution using Adobe Experience Platform datasets**
- **Campaign summary using only partner-provided data**

Choose the appropriate workflow below based on your campaign measurement goals.

#### Option A: Attribution using Experience Platform datasets

Use this workflow to measure conversion activity using datasets stored in Experience Platform.

1. **Create a measurement data connection**
   - Select the dataset that contains your conversion events.
   - Map identity fields from your dataset to the match keys used in Collaboration.
   - Manage consent and governance settings.
   - Define one or more conversion events to measure.
   - Review and confirm your setup.

2. **Run a measurement report**
   - Go to the **[!UICONTROL Measure]** workspace within the associated project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Attribution]** as the report type.
   - Select the defined conversion event(s).
   - Submit the report. It will run on the specified date and populate within 24 hours.

#### Option B: Campaign summary using partner-provided data

Use this workflow to generate campaign summary insights based on advertiser-supplied identifiers (for example, campaign ID).

1. **Set up the connection**
   - In the connection settings, ensure **[!UICONTROL Measurement]** is selected as a use case.
   - Create a project under the connection with **[!UICONTROL Measurement]** as an activity.

2. **Provide campaign context**
   - Input required campaign identifiers (for example, **Campaign ID**) for the partner to reference.
   - Align with your partner on campaign scope and reporting timeline.

3. **Run a measurement report**
   - Navigate to the **[!UICONTROL Measure]** workspace within the project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Campaign summary]** as the report type.
   - Submit the report. It will run on the selected date and populate within 24 hours. 
-->

## Paso 6: Conexión con colaboradores {#connect-with-collaborators}

Una vez completada la configuración, su organización ya está lista para conectarse con los colaboradores enviando o aceptando invitaciones y enviando la configuración del proyecto para su aprobación. Este proceso de conexión implica enviar o recibir invitaciones, revisar y enviar la configuración de conexión (como casos de uso y consumo de crédito) y confirmar la conexión.

Como anunciante, usa el espacio de trabajo **[!UICONTROL Connect]** del menú de navegación de la izquierda para buscar editores disponibles. Alternativamente, los colaboradores pueden conectarse entre sí directamente a través de [invitaciones de conexión privada](./connect/establishing-connections.md#private-connection-invite){target="_blank"}.

>[!NOTE]
>
>Actualmente, solo los anunciantes pueden examinar a los editores. Los editores no pueden examinar ni iniciar conexiones con anunciantes.

Para obtener una descripción general de este flujo, consulte la [guía de establecimiento de conexiones](./connect/establishing-connections.md){target="_blank"}. Para obtener una descripción general visual del proceso de conexión, incluidos los colaboradores de exploración y la administración de la configuración de conexión, vea el vídeo [configuración de cuenta del anunciante](https://experienceleague.adobe.com/es/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Próximos pasos

Ahora ha completado la configuración inicial y ha configurado su organización para una colaboración segura. A continuación, explore los siguientes recursos para comprender mejor la activación, la medición y la gobernanza de datos:

- [Documentación del flujo de trabajo de activación de audiencia](./collaborate/activate.md)
- [Casos de uso de medición](./collaborate/measure.md)
- [Prácticas recomendadas de administración de Collaboration](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
