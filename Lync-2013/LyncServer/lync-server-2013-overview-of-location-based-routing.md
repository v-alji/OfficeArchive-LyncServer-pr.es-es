---
title: 'Lync Server 2013: información general sobre el enrutamiento de Location-Based'
description: 'Lync Server 2013: información general sobre el enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399678"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a>Información general sobre el enrutamiento de Location-Based en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2013-02-21_

El enrutamiento basado en ubicación introduce un nuevo conjunto de reglas que modifica el enrutamiento de llamadas RTC nacionales e internacionales para evitar que se omitan los números de pago. El enrutamiento basado en ubicación proporciona la flexibilidad para delimitar estas reglas solo a regiones específicas, a puertas de enlace específicas o a un conjunto específico de usuarios.

Los siguientes escenarios ilustran los tipos principales de restricciones Location-Based el enrutamiento puede exigir:

  - Llamadas de salida: el enrutamiento de Location-Based puede exigir llamadas salientes a salidas de una puerta de enlace RTC que se encuentra en la misma región, en la que el autor de la llamada impide la omisión de llamadas RTC, lo que evita que se produzcan salidas de una puerta de enlace RTC ubicada en otra región, como la persona que llama.

  - Llamadas de entrada: el enrutamiento de Location-Based puede evitar las llamadas RTC entrantes para llamar a puntos de conexión de Lync si el enrutamiento de la puerta de enlace RTC la llamada entrante no se encuentra en la misma región que el usuario llamado Lync.

  - Regiones desconocidas: el enrutamiento de Location-Based restringe las llamadas a través de la RTC entrantes y salientes a los usuarios que se encuentran en ubicaciones indeterminadas (es decir, los usuarios remotos se conectan desde Internet o se encuentran en regiones desconocidas).

  - Regiones internacionales: el enrutamiento de Location-Based exige el enrutamiento de llamadas salientes a través de puertas de enlace RTC internacionales Si no se puede encontrar una puerta de enlace local a la ubicación del usuario.

<div>

## <a name="see-also"></a>Vea también


[Planificar el enrutamiento basado en ubicación en Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

