---
title: Cálculo de recuentos y porcentajes de superposición
description: Descubra cómo se calculan los recuentos y porcentajes de superposición en diversas áreas de Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilidad limitada" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 23dc33af83366806f7d99161b4b713a33daeec76
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 6%

---


# Cálculo de recuentos y porcentajes de superposición

En Adobe Real-Time CDP Collaboration, comprender la superposición de audiencias es crucial para optimizar las estrategias de marketing y garantizar una colaboración eficaz entre anunciantes y editores. En este documento se explica cómo se calculan los recuentos y porcentajes de superposición en diversas áreas de producto mediante datos de ejemplo.

## Datos de muestra: recuento de identidades

### Suposiciones con fines de cálculo

Para este ejemplo, supongamos que:

* El anunciante tiene tres audiencias (A1, A2, A3).
* El editor tiene tres audiencias (P1, P2, P3).
* Todas las identidades clave de coincidencia son mutuamente excluyentes en todas las audiencias.

>[!NOTE]
>
>En realidad, habría cierta superposición entre las identidades de clave de coincidencia de cada audiencia, pero para simplificar, este ejemplo supone que son exclusivas en este caso.

### Audiencias del anunciante

| Audiencias del anunciante | A1 | A2 | A3 | TODAS |
|----------------------|------|------|------|------|
| Identidades de correo electrónico con hash | 300K | 450K | 250K | 1 M |
| Identidades de ID de Liveramp | 500K | 200K | 700K | 1,4 M |
| Recuento total de identidades | 800K | 650K | 950K | 2,4 M |

### Audiencias del editor

| Audiencias del editor | P1 | P2 | P3 | TODAS |
|---------------------|------|------|------|------|
| Identidades de correo electrónico con hash | 150K | 600K | 550K | 1,3 M |
| Identidades de ID de Liveramp | 400K | 350K | 100K | 850K |
| Recuento total de identidades | 550K | 950K | 800K | 2,3 M |

## Cálculo de recuentos y porcentajes de superposición

### Datos de muestra: recuento de superposiciones

#### Cada anunciante frente a cada publicador

|                     | A1 - P1 | A2 - P2 | A3 - P3 |
|---------------------|---------|---------|---------|
| Superposición por correo electrónico con hash | 100K | 300K | 150K |
| Superposición por ID de Liveramp | 200K | 150K | 50K |
| Superposición total | 300K | 450K | 200K |

#### Cada anunciante frente a TODO el editor

|                     | A1 - P TODO | A2 - P TODO | A3 - P ALL |
|---------------------|------------|------------|------------|
| Superposición por correo electrónico con hash | 250K | 400K | 200K |
| Superposición por ID de Liveramp | 350K | 150K | 230K |
| Superposición total | 600K | 550K | 430K |

#### Todos los anunciantes frente a Todos los editores

|                     | TODO A - P1 | A TODO - P2 | A ALL - P3 |
|---------------------|------------|------------|------------|
| Superposición por correo electrónico con hash | 120K | 530K | 200K |
| Superposición por ID de Liveramp | 350K | 330K | 50K |
| Superposición total | 470K | 860K | 250K |

#### Todos los anunciantes frente a TODOS los editores

|                     | A TODO - P TODO |
|---------------------|---------------|
| Superposición por correo electrónico con hash | 850K |
| Superposición por ID de Liveramp | 730K |
| Superposición total | 1,58 M |

## Módulo Discover

El módulo **[!UICONTROL Discover]** de Adobe Real-Time CDP Collaboration proporciona información valiosa sobre tus datos de audiencia. Si se comprenden las superposiciones de audiencias, se pueden identificar posibles oportunidades de colaboración entre editores y anunciantes. La sección **[!UICONTROL Información de audiencia]** del módulo **[!UICONTROL Discover]** le ayuda a analizar los recuentos y porcentajes de superposición entre distintas audiencias.

![El módulo de detección del flujo de trabajo de colaboración.](/help/assets/reference/overlap-calculations/discover-module-overlap-calculations.png)

Vea a continuación cálculos y fórmulas de ejemplo para varios escenarios de superposición.

### Todas las audiencias de anunciante y todas las audiencias de editor

| Audiencias del anunciante | Audiencias del editor | Recuento de identidades (A) | Identidades superpuestas (B) | Porcentaje de superposición | Desglose de claves de coincidencias | Porcentaje de desglose de claves coincidentes |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| TODAS | TODAS | Recuento total de identidades de TODAS las audiencias de anunciante <br> Recuento de identidades = 1M + 1,4M = 2,4M | Superposición total entre TODAS las audiencias de anunciante y TODAS las audiencias de publicador para todas las claves de coincidencia <br> Identidades superpuestas = 1,58 M | Porcentaje de identidades superpuestas sobre el recuento total de identidades de TODAS las audiencias de anunciante <br> % de superposición = (B / A) * 100 = (1,58 M / 2,4 M) * 100 = 65,83 % <br> Porcentaje de superposición = 65,83 % | Identidades superpuestas por clave de coincidencia <br> Superposición por correo electrónico con hash = 850K <br> Superposición por ID de Liveramp = 730K | Porcentaje de superposición de clave de coincidencia sobre el total de identidades superpuestas <br> Porcentaje de clave de coincidencia para correo electrónico con hash = (850K / 1,58M) * 100 = 53,8% <br> para Liveramp Id = (730K / 1,58M) * 100 = 46,2% |

### Todas las audiencias de anunciantes y una audiencia de editor

| Audiencias del anunciante | Audiencias del editor | Recuento de identidades (A) | Identidades superpuestas (B) | Porcentaje de superposición | Desglose de claves de coincidencias | Porcentaje de desglose de claves coincidentes |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| TODAS | 1 P2 | Recuento total de identidades de todas las audiencias del anunciante <br> Recuento de identidades = 1M + 1,4M = 2,4M | Superposición total entre TODAS las audiencias de anunciante y la audiencia de editor seleccionada P2 para todas las claves de coincidencia <br> Identidades superpuestas = 860K | Porcentaje de identidades superpuestas sobre el recuento total de identidades de TODAS las audiencias de anunciante <br> % de superposición = (B / A) * 100 = (860K / 2,4M) * 100 = 35,83 % <br> Porcentaje de superposición = 35,83 % | Identidades superpuestas por clave de coincidencia <br> Superposición por correo electrónico con hash = 530K <br> Superposición por ID de Liveramp = 330K | Porcentaje de superposición de clave de coincidencia sobre el total de identidades superpuestas <br> Porcentaje de clave de coincidencia para correo electrónico con hash = (530K / 860K) * 100 = 61,62% <br> para Liveramp Id = (330K / 860K) * 100 = 38,38% |

### Una audiencia de anunciante y todas las audiencias de editor

| Audiencias del anunciante | Audiencias del editor | Recuento de identidades (A) | Identidades superpuestas (B) | Porcentaje de superposición | Desglose de claves de coincidencias | Porcentaje de desglose de claves coincidentes |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A1 | TODAS | Recuento total de identidades de la audiencia seleccionada por el anunciante A1 <br> Recuento de identidades = 300K + 500K = 800K | Superposición total entre la audiencia del anunciante A1 y TODAS las audiencias del publicador para todas las claves de coincidencia <br> Identidades superpuestas = 600K | Porcentaje de identidades superpuestas sobre el recuento de identidades de la audiencia seleccionada por el anunciante (A1) <br> % de superposición = (B / A) * 100 = (600K / 800K) * 100 = 75 % <br> Porcentaje de superposición = 75 % | Identidades superpuestas por clave de coincidencia <br> Superposición por correo electrónico con hash = 250K <br> Superposición por ID de Liveramp = 350K | Porcentaje de superposición de clave de coincidencia sobre el total de identidades superpuestas <br> Porcentaje de clave de coincidencia para correo electrónico con hash = (250K / 600K) * 100 = 41,67% <br> para Liveramp Id = (350K / 600K) * 100 = 58,33% |

### Una audiencia de anunciante y una audiencia de editor

| Audiencias del anunciante | Audiencias del editor | Recuento de identidades (A) | Identidades superpuestas (B) | Porcentaje de superposición | Desglose de claves de coincidencias | Porcentaje de desglose de claves coincidentes |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A2 | 1 P2 | Recuento total de identidades de la audiencia seleccionada por el anunciante A2 <br> Recuento de identidades = 450K + 200K = 650K | Superposición total entre la audiencia de anunciante A2 seleccionada y la audiencia de publicador P2 seleccionada para todas las claves de coincidencia <br> Identidades superpuestas = 450K | Porcentaje de identidades superpuestas sobre el recuento de identidades de mi audiencia seleccionada (A2) <br> % de superposición = (B / A) * 100 = (450 000 / 650 000) * 100 = 69,23 % <br> Porcentaje de superposición = 69,23 % | Identidades superpuestas por clave de coincidencia <br> Superposición por correo electrónico con hash = 300 K <br> Superposición por ID de Liveramp = 150 K | Porcentaje de superposición de clave de coincidencia sobre el total de identidades superpuestas <br> Porcentaje de clave de coincidencia para correo electrónico con hash = (300K / 450K) * 100 = 66,67% <br> para Liveramp Id = (150K / 450K) * 100 = 33,33% |
