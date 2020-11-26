---
title: 'Lync Server 2013: Capacidades no compatibles con el enrutamiento basado en ubicación'
description: 'Lync Server 2013: las funciones no son compatibles con el enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capabilities not supported by Location-Based Routing
ms:assetid: c3d54953-a7d6-4465-a6c3-ae411b2d8ea9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994071(v=OCS.15)
ms:contentKeyID: 51803982
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf9cd03a8cbdd50e136605c4f172598b2ad3f523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435610"
---
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a>Capacidades no compatibles con el enrutamiento basado en ubicación en Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Última modificación del tema:** 2014-03-12_

El enrutamiento de Location-Based no se aplica a los siguientes tipos de interacciones. Location-Based el enrutamiento no se aplica cuando los puntos de conexión de Lync interactúan con puntos de conexión RTC mediante estas características.

  - Marcación RTC para conferencias

  - Llamadas RTC entrantes y salientes a través del grupo de respuesta

  - Estacionamiento o recuperación de llamadas RTC a través del estacionamiento de llamadas

  - Llamadas RTC entrantes al servicio de anuncio

  - Llamadas RTC entrantes recuperadas a través de la atención de llamadas de grupo

Para exigir Location-Based reglas de enrutamiento a los tipos de interacciones de la siguiente lista, debe habilitar el enrutamiento de Location-Based para las conferencias:

  - Iniciar llamadas RTC desde una conferencia

  - Escalaciones desde conversaciones de audio de punto a punto a conferencias en las que participen extremos de RTC

  - Transferencias de consulta con extremos de RTC

Para habilitar el enrutamiento de Location-Based para conferencias, consulte [enrutamiento basado en ubicación para conferencias en Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).

<div>

## <a name="see-also"></a>Vea también


[Planificar el enrutamiento basado en ubicación en Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

