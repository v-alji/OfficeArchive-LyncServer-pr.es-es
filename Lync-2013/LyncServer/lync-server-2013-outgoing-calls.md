---
title: 'Lync Server 2013: Llamadas salientes'
description: 'Lync Server 2013: llamadas salientes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Outgoing calls
ms:assetid: 885ffe6f-cd51-4f21-8d4f-a1ff8d818858
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994049(v=OCS.15)
ms:contentKeyID: 51803960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e14f19dec35a6da47a2ddd62657d5d087a854f16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424838"
---
# <a name="outgoing-calls-in-lync-server-2013"></a><span data-ttu-id="b0f71-103">Llamadas salientes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0f71-103">Outgoing calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0f71-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0f71-104">

<span> </span></span></span>

<span data-ttu-id="b0f71-105">_**Última modificación del tema:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="b0f71-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="b0f71-106">El enrutamiento de llamadas salientes de usuarios habilitados para el enrutamiento de Location-Based se ve afectado por la ubicación de red del extremo del usuario.</span><span class="sxs-lookup"><span data-stu-id="b0f71-106">The routing of outbound calls of users enabled for Location-Based Routing is affected by the network location of the user’s endpoint.</span></span> <span data-ttu-id="b0f71-107">En la tabla siguiente se muestra cómo el enrutamiento de Location-Based afecta al enrutamiento de las llamadas salientes en función de la ubicación del punto de conexión de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b0f71-107">The following table illustrates how Location-Based Routing affects the routing of outbound calls depending on the location of the caller’s endpoint.</span></span>

### <a name="caller-placing-an-outbound-call-to-the-pstn"></a><span data-ttu-id="b0f71-108">El autor de la llamada hace una llamada saliente a la RTC</span><span class="sxs-lookup"><span data-stu-id="b0f71-108">Caller placing an outbound call to the PSTN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b0f71-109">El extremo del usuario se encuentra en un sitio de red habilitado para el enrutamiento basado en ubicación</span><span class="sxs-lookup"><span data-stu-id="b0f71-109">User endpoint located in a network site enabled for Location-Based Routing</span></span></th>
<th><span data-ttu-id="b0f71-110">El extremo del usuario se encuentra en un sitio de red desconocido o no habilitado para el enrutamiento basado en ubicación</span><span class="sxs-lookup"><span data-stu-id="b0f71-110">User endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0f71-111">Autorización de llamadas salientes</span><span class="sxs-lookup"><span data-stu-id="b0f71-111">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="b0f71-112">La llamada se autoriza según la directiva de voz del usuario</span><span class="sxs-lookup"><span data-stu-id="b0f71-112">Call is authorized based on user’s voice policy</span></span></p></td>
<td><p><span data-ttu-id="b0f71-113">La llamada se autoriza según la directiva de voz del usuario</span><span class="sxs-lookup"><span data-stu-id="b0f71-113">Call is authorized based on user’s voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0f71-114">Enrutamiento de llamadas salientes</span><span class="sxs-lookup"><span data-stu-id="b0f71-114">Routing of outbound call</span></span></p></td>
<td><p><span data-ttu-id="b0f71-115">La llamada se redirige según la directiva de enrutamiento de voz del sitio de red</span><span class="sxs-lookup"><span data-stu-id="b0f71-115">Call is routed according to the network site’s voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="b0f71-116">La llamada se redirige según la directiva de voz del usuario y solo a través de troncos no habilitados para el enrutamiento basado en ubicación (si está disponible)</span><span class="sxs-lookup"><span data-stu-id="b0f71-116">Call is routed according to user’s voice policy and only through trunks not enabled for Location-Based Routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="b0f71-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0f71-117">See Also</span></span>


[<span data-ttu-id="b0f71-118">Escenarios para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0f71-118">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="b0f71-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0f71-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

