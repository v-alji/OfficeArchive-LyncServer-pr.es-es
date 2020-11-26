---
title: 'Lync Server 2013: Omisión de medios y servidor de mediación'
description: 'Lync Server 2013: servidor de mediación y omisión de medios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media bypass and Mediation Server
ms:assetid: 8ed35f95-05cd-4b5d-8470-442d2323df71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398719(v=OCS.15)
ms:contentKeyID: 48184774
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebb005d3d52fa9e5a38fdf56a65dfcbd73616d87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425706"
---
# <a name="media-bypass-and-mediation-server-in-lync-server-2013"></a><span data-ttu-id="81d16-103">Omisión de medios y servidor de mediación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="81d16-103">Media bypass and Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="81d16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="81d16-104">

<span> </span></span></span>

<span data-ttu-id="81d16-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="81d16-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="81d16-106">La omisión de multimedia es una función de Lync Server que permite a un administrador configurar el enrutamiento de llamadas para que fluya directamente entre el extremo de usuario y la puerta de enlace de red telefónica conmutada (RTC) sin atravesar el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="81d16-106">Media bypass is a Lync Server capability that enables an administrator to configure call routing to flow directly between the user endpoint and the public switched telephone network (PSTN) gateway without traversing the Mediation Server.</span></span> <span data-ttu-id="81d16-107">La omisión de medios mejora la calidad de las llamadas al reducir la latencia, la traducción innecesaria, la posibilidad de pérdida de paquetes y la cantidad de puntos posibles de error.</span><span class="sxs-lookup"><span data-stu-id="81d16-107">Media bypass improves call quality by reducing latency, unnecessary translation, possibility of packet loss, and the number of potential points of failure.</span></span> <span data-ttu-id="81d16-108">Cuando un sitio remoto sin un servidor de mediación se conecta a un sitio central mediante uno o varios vínculos WAN con ancho de banda restringido, la omisión de medios disminuye el requisito de ancho de banda al permitir que los medios de un cliente en un sitio remoto fluyan directamente a su puerta de enlace local sin tener que transmitir primero a través del vínculo WAN a un servidor de mediación en el sitio Esta reducción en el procesamiento de medios también complementa la capacidad del servidor de mediación de controlar varias puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="81d16-108">Where a remote site without a Mediation Server is connected to a central site by one or more WAN links with constrained bandwidth, media bypass lowers the bandwidth requirement by enabling media from a client at a remote site to flow directly to its local gateway without first having to flow across the WAN link to a Mediation Server at the central site and back.This reduction in media processing also complements the Mediation Server’s ability to control multiple gateways.</span></span>

<span data-ttu-id="81d16-p102">La omisión de medios y el servicio de control de admisión de llamadas (CAC) se excluyen mutuamente. Si se usa la omisión de medios en una llamada, no se aplicará el CAC en esa llamada. Se asume que no hay vínculos relacionados con la llamada que tengan restringido el ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="81d16-p102">Media bypass and call admission control (CAC) are mutually exclusive. If media bypass is employed for a call, CAC is not performed for that call. The assumption is that there are no links with constrained bandwidth involved in the call.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="81d16-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="81d16-112">See Also</span></span>


[<span data-ttu-id="81d16-113">Control de admisión de llamadas y servidor de mediación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="81d16-113">Call admission control and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-and-mediation-server.md)  


[<span data-ttu-id="81d16-114">Planificar la omisión de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="81d16-114">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="81d16-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="81d16-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

