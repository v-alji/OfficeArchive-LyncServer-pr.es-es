---
title: 'Lync Server 2013: Tono de llamada simultáneo'
description: 'Lync Server 2013: llamadas simultáneas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Simultaneous ringing
ms:assetid: df02f919-4d50-4832-9300-6c51f8b4fc56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994079(v=OCS.15)
ms:contentKeyID: 51803990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 595c8c1d4ce105e2189002f18733ffae92cff8bf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423823"
---
# <a name="simultaneous-ringing-in-lync-server-2013"></a><span data-ttu-id="2a4de-103">Tono de llamada simultáneo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2a4de-103">Simultaneous ringing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a4de-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a4de-104">

<span> </span></span></span>

<span data-ttu-id="2a4de-105">_**Última modificación del tema:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="2a4de-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="2a4de-106">Cuando la persona llamada tiene habilitado el timbre simultáneo, Location-Based el enrutamiento analiza la ubicación de la persona que llama y los puntos finales de las partes a las que se llama para determinar si se debe distribuir la llamada.</span><span class="sxs-lookup"><span data-stu-id="2a4de-106">When the called party has simultaneous ringing enabled, Location-Based Routing analyzes the location of the calling party and the endpoints of the called parties to determine whether the call should be routed.</span></span>

<span data-ttu-id="2a4de-107">En la siguiente tabla se muestra un usuario con la configuración de llamadas simultáneas habilitada y el destino de llamadas simultáneas es un usuario en el mismo sitio de red, en un sitio de red diferente o en un sitio de red desconocido.</span><span class="sxs-lookup"><span data-stu-id="2a4de-107">The following table illustrates a user configured with simultaneous ringing, and the simultaneous ringing target is a user in the same network site, in a different network site, or in an unknown network site.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a4de-108">Llamada RTC entrante para</span><span class="sxs-lookup"><span data-stu-id="2a4de-108">Incoming PSTN call for</span></span></th>
<th><span data-ttu-id="2a4de-109">Ubicado en el mismo sitio de red que el destinatario</span><span class="sxs-lookup"><span data-stu-id="2a4de-109">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="2a4de-110">Ubicado en un sitio de red distinto del sitio del destinatario</span><span class="sxs-lookup"><span data-stu-id="2a4de-110">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="2a4de-111">Se encuentra en un sitio de red desconocido o no está habilitado para Location-Based enrutamiento</span><span class="sxs-lookup"><span data-stu-id="2a4de-111">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a4de-112">Usuario de Lync</span><span class="sxs-lookup"><span data-stu-id="2a4de-112">Lync user</span></span></p></td>
<td><p><span data-ttu-id="2a4de-113">Llamadas simultáneas permitidas</span><span class="sxs-lookup"><span data-stu-id="2a4de-113">Simultaneous ring allowed</span></span></p></td>
<td><p><span data-ttu-id="2a4de-114">Llamadas simultáneas no permitidas</span><span class="sxs-lookup"><span data-stu-id="2a4de-114">Simultaneous ring not allowed</span></span></p></td>
<td><p><span data-ttu-id="2a4de-115">Llamadas simultáneas no permitidas</span><span class="sxs-lookup"><span data-stu-id="2a4de-115">Simultaneous ring not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="2a4de-116">En la tabla siguiente se muestra una llamada de un usuario de Lync (es decir, el autor de la llamada de Lync) en el mismo sitio de red, en un sitio de red diferente o desde un sitio de red desconocido.</span><span class="sxs-lookup"><span data-stu-id="2a4de-116">The following table illustrates a call from a Lync user (i.e. Lync caller) in the same network site, in a different network site, or from an unknown network site.</span></span> <span data-ttu-id="2a4de-117">El destinatario de la llamada tiene un punto final de la RTC (por ejemplo, teléfono móvil) configurado como un objetivo de llamada simultánea.</span><span class="sxs-lookup"><span data-stu-id="2a4de-117">The callee has a PSTN endpoint (i.e. cellphone) configured as a simultaneous ring target.</span></span> <span data-ttu-id="2a4de-118">En este caso, el enrutamiento de Location-Based determinará si la llamada debe dirigirse al destino simultáneo (por ejemplo, teléfono móvil) del destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2a4de-118">In this scenario, Location-Based Routing will determine whether the call should be routed to the simultaneous ring target (i.e. cellphone) of the callee or not.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a4de-119">Destino de llamadas simultáneas</span><span class="sxs-lookup"><span data-stu-id="2a4de-119">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="2a4de-120">Ubicado en el mismo sitio de red que el destinatario</span><span class="sxs-lookup"><span data-stu-id="2a4de-120">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="2a4de-121">Ubicado en un sitio de red distinto del sitio del destinatario</span><span class="sxs-lookup"><span data-stu-id="2a4de-121">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="2a4de-122">Se encuentra en un sitio de red desconocido o no está habilitado para Location-Based enrutamiento</span><span class="sxs-lookup"><span data-stu-id="2a4de-122">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a4de-123">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="2a4de-123">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2a4de-124">Llamadas simultáneas permitidas a través de la directiva del enrutamiento de voz del sitio del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="2a4de-124">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="2a4de-125">Llamadas simultáneas permitidas a través de la directiva del enrutamiento de voz del sitio del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="2a4de-125">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="2a4de-126">Llamadas simultáneas permitidas a través de la directiva del enrutamiento de voz del autor de la llamada para troncos no habilitados para el enrutamiento basado en ubicación</span><span class="sxs-lookup"><span data-stu-id="2a4de-126">Simultaneous ring allowed through the caller’s voice policy to trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="2a4de-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a4de-127">See Also</span></span>


[<span data-ttu-id="2a4de-128">Escenarios para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2a4de-128">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="2a4de-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a4de-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

