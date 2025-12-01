---
title: Configuración de permisos de AWS para el abastecimiento de audiencias
description: Aprenda a configurar los permisos de AWS Identity and Access Management (IAM) para conceder a Adobe acceso seguro de solo lectura a su  [!DNL Amazon S3] bloque para el abastecimiento de audiencias en Real-Time CDP Collaboration.
source-git-commit: 73f11b7341cf94540dc01f8803291f6dc3cd5038
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 1%

---

# Configuración de permisos de AWS para el abastecimiento de audiencias

Utilice esta guía para configurar las políticas y funciones de AWS Identity and Access Management (IAM) que otorgan a Adobe acceso seguro de solo lectura a su bloque de Amazon S3. Este acceso permite a Real-Time CDP Collaboration obtener audiencias a partir del compartimento de S3.

## Requisitos previos {#prerequisites}

Antes de continuar, confirme que cumple los siguientes requisitos y que tiene acceso a la información necesaria.

### Permisos de AWS necesarios

Para completar esta configuración, su cuenta debe tener acceso de administrador de AWS. El acceso de administrador garantiza que pueda crear y administrar las políticas y funciones de IAM necesarias para autorizar el acceso de Adobe a su compartimento de S3. Si no tiene privilegios de administrador, póngase en contacto con el administrador de AWS antes de continuar.

### Información requerida

A medida que avance en los pasos siguientes, tenga en cuenta la siguiente información. Estos detalles se utilizan en la [[!DNL Amazon S3] guía de la interfaz de usuario de abastecimiento de audiencia](./configure-aws-s3-audience-sourcing.md).

* Nombre del contenedor de S3 donde se almacenan los archivos de audiencia.
* La ruta de la carpeta (prefijo) con la que se encuentran los archivos de audiencia.
* El nombre del recurso de Amazon (ARN) para su rol de IAM recién creado, por ejemplo: `arn:aws:s3:::my-company-data/audience-files/`

>[!TIP]
>
>Un Nombre de recurso de Amazon (ARN) identifica de forma exclusiva los recursos de AWS, como bloques de S3 y funciones de IAM. Utilice el siguiente formato para especificar el bloque y la ruta de carpeta opcional:
>
>```
>arn:aws:s3:::<bucket-name>/<optional-folder-path>
>```

## Crear una directiva IAM {#create-policy}

Para comenzar la configuración, primero cree una directiva de IAM que conceda **acceso de solo lectura** a su espacio de S3. Esta directiva permite a Adobe leer los archivos necesarios para el abastecimiento de audiencias, pero no concede permisos de escritura o eliminación.

Abra [AWS Management Console](https://aws.amazon.com/console/) y vaya a **[!DNL IAM]** > **[!DNL Policies]** > **[!DNL Create policy]**.

En el espacio de trabajo de la directiva Crear de AWS, seleccione la pestaña **JSON** y pegue la siguiente directiva de ejemplo.

>[!NOTE]
>
>Reemplace `<Your AWS ARN for bucket folder path>` y `<Your AWS ARN for bucket>` por sus ARN S3 específicos. Al especificar la ruta de la carpeta del contenedor, incluya `/*` al final del ARN (por ejemplo, `arn:aws:s3:::my-company-data/audience-files/*`). Esto garantiza que Adobe tenga acceso a todos los archivos y subcarpetas de la ruta de carpeta especificada.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket",
        "s3:GetBucketLocation"
      ],
      "Resource": "<Your AWS ARN for bucket folder path>"
    },
    {
      "Sid": "Statement2",
      "Effect": "Allow",
      "Action": [
        "s3:ListBucket"
      ],
      "Resource": "<Your AWS ARN for bucket>"
    }
  ]
}
```

Revise la configuración de directiva y seleccione **[!DNL Create policy]**. Registre el nombre de la directiva para utilizarlo en un paso posterior.

>[!TIP]
>
>Para encontrar el nombre del contenedor y la ruta de la carpeta, abra **Amazon S3 Management Console**. En la página **Bloques**, seleccione el nombre del bloque para abrirlo. La vista **Objetos** muestra sus archivos y carpetas, y la ruta de acceso situada en la parte superior de la página muestra la ruta de acceso de la carpeta actual.

## Crear una función de IAM {#create-role}

A continuación, cree una función IAM y establezca la función IAM de Real-Time CDP Collaboration AWS como **entidad de confianza**. Esto permite a los servicios de Adobe asumir la función y leer de forma segura los datos de audiencia de S3.

En la ficha **[!DNL IAM]** de la consola de administración de Amazon S3, vaya a **[!DNL Roles]** > **[!DNL Create role]**.

En [!DNL Step 1] del flujo de trabajo [!DNL Create role], en la sección **[!DNL Trusted entity type]**, seleccione **[!DNL Custom trust policy]**. A continuación, en el editor **[!DNL Custom trust policy]**, pegue el siguiente ejemplo y reemplace `<Adobe IAM Role ARN>` por el valor de su región.

* El ARN de la función de Adobe IAM adecuado para su región:

| Región | ARN de la función Adobe IAM |
|---------|-------------------|
| América del Norte | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-va6-role` |
| Australia | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-aus3-role` |
| EMEA | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-deu1-role` |

Un ejemplo de directiva de confianza:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Principal": {
        "AWS": "<Adobe IAM Role ARN>"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

Revise la directiva y seleccione **Siguiente** para continuar.

En la sección [!DNL Step 2] **[!DNL Add permissions]** del flujo de trabajo [!DNL Create role], busque y adjunte la directiva IAM que creó [anteriormente](#create-policy). Seleccione la directiva seguida por **[!DNL Next]** para continuar con [!DNL Step 3].

En la sección [!DNL Step 3] **[!DNL Name review, and create - Role details]**, proporcione un nombre de rol (por ejemplo, `s3-iam-role`) y una descripción opcional.

Esta página muestra la directiva de entidad de confianza, el resumen de la directiva de permisos y cualquier etiqueta que haya agregado para la organización interna y el seguimiento.

Finalmente, seleccione **Crear rol** para confirmar la configuración.

>[!IMPORTANT]
>
>Debe registrar el Nombre del recurso de Amazon (ARN) después de crear la función. Deberá proporcionar el ARN de la función IAM durante el paso **Autenticar la conexión S3** en el flujo de trabajo [Configuración de AWS S3 para el abastecimiento de audiencias](./configure-aws-s3-audience-sourcing.md).

## Próximos pasos {#next-steps}

Esta configuración concede a Adobe acceso de solo lectura a su bloque S3 y establece una conexión de confianza con la función IAM de Adobe.

A continuación, continúe con [Configuración de AWS S3 para el abastecimiento de audiencias](./configure-aws-s3-audience-sourcing.md) para conectar su compartimento de S3 a Collaboration.

Para obtener más información sobre las audiencias de abastecimiento, consulte [Source y administrar audiencias](./onboard-audiences.md).
