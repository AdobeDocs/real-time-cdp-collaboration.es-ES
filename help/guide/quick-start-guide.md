---
title: Real-Time CDP Collaboration Quick Start & Setup Guide
description: Obtenga información sobre cómo configurar Real-Time CDP Collaboration, configurar funciones y cuentas, públicos de origen, activar datos y conectarse con socios de forma segura.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/es/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
TQID: https://experienceleague.adobe.com/rhIArZZm0Thkj3E-qiHtVHO6qxpr1vd-Qs4hWt4tf1U
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1417
ht-degree: 4%

---

# Real-Time CDP Collaboration quick start guide

{{limited-availability-release-note}}

Get started with Real-Time CDP Collaboration by configuring your organization, sourcing audiences, and enabling privacy-focused activation and measurement.

## Requisitos previos

Before you begin, ensure you have the following:

- An active Real-Time CDP Collaboration license.
- [System or product administrator access to Adobe Experience Platform](./permissions/overview.md).
- [Access provisioned for end users](./permissions/manage-user-access.md).
- [Roles created for your organization and assigned to users](./permissions/manage-roles.md).
- Access to branding assets, such as your organization&#39;s name, logo, and banner.
- A [defined match key strategy](./setup/onboard-account.md#set-up-match-keys)
- (Optional) Access to a supported cloud source (Amazon S3, Google Cloud Storage, or Snowflake) if you&#39;re not using Experience Platform for audience management.

## Step 1: Complete role-based setup {#complete-role-based-setup}

Your organization&#39;s access roles determine what users can see and do in Collaboration. Before proceeding, make sure role-based permissions are set up correctly to ensure appropriate access and visibility in the platform.

**Resources:**

- [User Access Documentation](./permissions/manage-user-access.md)
- [Role Setup Documentation](./permissions/manage-roles.md)


Watch this video to learn how to assign product access and permissions for Collaboration using the Admin Console and Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452233/?captions=spa&learn=on&enablevpops)

## Step 2: Set up your Collaboration account {#set-up-your-account}

Before you can source audiences, you must configure your account in Collaboration. This governs how you appear and what you have access to in the interface.

If you don&#39;t have the necessary access, please refer back to step 1 or contact your organization&#39;s administrator for help completing this setup.

Define your account&#39;s role in Collaboration, provide branding assets, and configure match keys to align audiences across connections.

>[!NOTE]
>
>You can create one or more accounts (such as advertiser and a publisher) during setup. Certain fields, like branding assets and contact email, can be updated later in the **[!UICONTROL Settings]** workspace.

- **Assign a role** – Determines whether your account is an advertiser or a publisher. Your role defines which capabilities you have in Collaboration. To learn more about how roles impact the collaboration workflow, see the [roles](./overview/roles.md) guide.
- **Branding assets** – Add the following to your account:
   - Account name (max 100 characters)
   - Description (max 1,000 characters)
   - Logo (SVG &lt;20KB, ideally square)

>[!NOTE]
>
>If you&#39;re creating a publisher account and would like to be publicly visible in Collaboration&#39;s connections catalog, please contact your Adobe account representative. Publisher accounts require a custom brand banner (JPG 2688x1536); this file can be shared directly with your representative.

- **Contact email** – Provide a business email for collaborators to use after a connection is established.
- **Configure match keys** – Select the identifiers used for audience matching.

To learn more about initial account setup, including how to define roles, upload branding assets, and configure match keys, see the [initial account setup](./setup/onboard-account.md#initial-account-setup){target="_blank"} guide.

Watch this video for a step-by-step walkthrough of an advertiser setup, including account creation, branding, and match key configuration.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Step 3: Source audiences (from Experience Platform or a cloud source) {#source-audiences}

Once your account is created and your branding and match keys are configured, you&#39;re ready to begin sourcing audiences. Choose one of the following sourcing methods based on your data store and business needs.

### Option A: Source from Experience Platform

[Use Collaboration to link a sandbox that contains audiences](./setup/onboard-audiences.md). Use this self-service method to reference existing audience segments from within your Experience Platform instance.

#### Configure audiences

Configure how audiences are prepared, matched, and governed for use in connections.

- **Select audiences** *(Experience Platform only)* – Choose audience segments with supported identifiers.
- **Map match keys** – Align audience fields with the configured match keys.
- **Apply transformations** – Hash plaintext values (for example, email) if needed.
- **Schedule refreshes** – Define update frequency (for example, daily).
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
>Las claves de coincidencia con hash deben ser **SHA256-hashed**.\
>Si proporciona valores hash con caracteres en mayúsculas, Collaboration los convierte automáticamente a minúsculas.\
>Si su origen contiene **identificadores de texto sin formato**, use la opción **[!UICONTROL Aplicar transformación]** para aplicar el hash. Esta opción solo está disponible cuando obtiene audiencias de Experience Platform y no es compatible con fuentes basadas en la nube.
>
>Para obtener más información, consulte la sección [asignar campos](./setup/onboard-audiences.md#map-fields) de la guía de origen y administración de audiencias.

Para ver una introducción completa sobre cómo crear audiencias con Collaboration, vea el siguiente vídeo.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

También puede ver el documento sobre [audiencias de abastecimiento en Collaboration](./setup/onboard-audiences.md#source-and-manage-audiences).

### Opción B: Source desde Snowflake, Amazon S3 o Google Cloud Storage

Para configurar una fuente de nube, como [!DNL Snowflake], [!DNL Amazon S3] o [!DNL Google Cloud Storage], prepare los datos de audiencia con la [especificación de audiencia PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)

Puede configurar [!DNL Amazon S3], [!DNL Google Cloud Storage] o [!DNL Snowflake] como orígenes de datos de autoservicio. Para obtener instrucciones de configuración, consulte la [guía de abastecimiento de Amazon S3](./setup/configure-aws-s3-audience-sourcing.md), la [guía de abastecimiento de GCS](./setup/configure-gcs-audience-sourcing.md) o la [guía de abastecimiento de Snowflake](./setup/configure-snowflake-audience-sourcing.md).

Para otros proveedores de servicios en la nube, póngase en contacto con el representante de su cuenta de Adobe para finalizar la configuración.

>[!IMPORTANT]
>
>Los archivos de audiencia basados en la nube deben seguir el esquema requerido descrito en la Especificación de audiencias de PDF. Los archivos deben incluir identificadores hash (SHA256 en minúsculas), campos de metadatos requeridos como `segment_name` y `activation_id`, y usar formatos compatibles como CSV o Parquet. Adobe no normaliza los datos antes de la activación. El TTL se aplica en función de la duración de la audiencia.
>
>Todas las audiencias del archivo cargado tienen un origen completo en este momento. The [audience visibility setting](/help/guide/setup/onboard-audiences.md#metadata-visibility) determines whether your collaborators can view your audience and is managed through the Collaboration UI.

## Step 4: Activate audiences (to Experience Platform or a cloud destination) {#activate-audiences}

Next, activate audiences to either your Experience Platform instance or a cloud destination.

### Option A: Activate to Experience Platform

Complete the following steps outlined in the [configure Adobe Experience Platform as a destination](/help/guide/destinations/experience-platform.md) guide.

- **Create a destination** – Use the UI to set up an Experience Platform destination (sandbox-level).
- **Map match keys** – Select the identifier (e.g., `hashedEmail`).
- **Define TTL** – Set expiration (1–30 days).
- **Verify in Audience Portal** – Once a collaborator sends you an audience, verify that it appears in the Audience Portal under the origin &quot;[!UICONTROL Real-Time CDP Collaboration].&quot;

### Option B: Activate to cloud

To configure a cloud destination (for example, [!DNL AWS S3] or [!DNL Snowflake]), contact your Adobe account representative to initiate the setup process. Depending on the cloud destination, you will need to provide cloud destination details such as file path, credentials, account locators etc. Once required information is provided, Adobe will configure the cloud destination setup.

Audience data sent to a cloud destination follows a predefined schema. For a detailed description of the required fields and format, download the [Collaboration Audience Activation Guide](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

## Step 5: Set up measurement (optional) {#set-up-measurement}

>[!IMPORTANT]
>
>The **[!UICONTROL Measure]** workspace is only available if the **[!UICONTROL Measurement]** use case was enabled [during the connection process](./connect/establishing-connections.md#connection-settings). Para obtener más información sobre los casos de uso, consulte la guía [administrar proyectos](./collaborate/manage-projects.md#project-use-cases).

Collaboration offers a variety of reports to analyze campaign reach, frequency, and effectiveness. While the **[!UICONTROL Measure]** workspace is available in the UI, full reporting functionality may require backend enablement.

To learn how to view and interpret measurement reports, see the [Measurement guide](./collaborate/measure.md). It covers attribution, campaign summary metrics, and dashboards such as reach curves and frequency distribution.

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

## Step 6: Connect with collaborators {#connect-with-collaborators}

With setup complete, your organization is now ready to connect with collaborators by sending or accepting invitations and submitting project settings for approval. This connection process involves sending or receiving invitations, reviewing and submitting connection settings (such as use cases and credit consumption), and confirming the connection.

As an advertiser, use the **[!UICONTROL Connect]** workspace from the left navigation menu to browse available publishers. Alternatively, collaborators may connect with each other directly through [private connection invitations](./connect/establishing-connections.md#private-connection-invite){target="_blank"}.

>[!NOTE]
>
>Actualmente, solo los anunciantes pueden examinar a los editores. Los editores no pueden examinar ni iniciar conexiones con anunciantes.

Para obtener una descripción general de este flujo, consulte la [guía de establecimiento de conexiones](./connect/establishing-connections.md){target="_blank"}. Para obtener una descripción general visual del proceso de conexión, incluidos los colaboradores de exploración y la administración de la configuración de conexión, vea el vídeo [configuración de cuenta del anunciante](https://experienceleague.adobe.com/es/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Próximos pasos

Ahora ha completado la configuración inicial y ha configurado su organización para una colaboración segura. A continuación, explore los siguientes recursos para comprender mejor la activación, la medición y la gobernanza de datos:

- [Documentación del flujo de trabajo de activación de audiencia](./collaborate/activate.md)
- [Casos de uso de medición](./collaborate/measure.md)
- [Prácticas recomendadas de administración de Collaboration](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
