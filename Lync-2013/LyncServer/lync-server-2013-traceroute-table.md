---
title: 'Lync Server 2013: tabla TraceRoute'
description: 'Lync Server 2013: tabla TraceRoute.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TraceRoute table
ms:assetid: b9493cef-6ece-4f13-bf68-dbf132aab4f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205205(v=OCS.15)
ms:contentKeyID: 48185242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af33e572065fbab1eaaaef684997e7f95edaed9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440839"
---
# <a name="traceroute-table-in-lync-server-2013"></a><span data-ttu-id="9af35-103">Tabla TraceRoute en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9af35-103">TraceRoute table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9af35-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9af35-104">

<span> </span></span></span>

<span data-ttu-id="9af35-105">_**Última modificación del tema:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="9af35-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="9af35-106">La tabla TraceRoute contiene información de enrutamiento de las llamadas.</span><span class="sxs-lookup"><span data-stu-id="9af35-106">The TraceRoute table contains routing information from calls.</span></span> <span data-ttu-id="9af35-107">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9af35-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9af35-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="9af35-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="9af35-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="9af35-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9af35-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9af35-113">datetime</span><span class="sxs-lookup"><span data-stu-id="9af35-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="9af35-114">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="9af35-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9af35-115">Fecha y hora en que comenzó la llamada.</span><span class="sxs-lookup"><span data-stu-id="9af35-115">Date and time that the call began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9af35-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9af35-117">int</span><span class="sxs-lookup"><span data-stu-id="9af35-117">int</span></span></p></td>
<td><p><span data-ttu-id="9af35-118">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="9af35-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9af35-119">Identificador único que se usa para distinguir entre varias llamadas que podrían haber comenzado en la misma fecha y al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="9af35-119">Unique identifier used to distinguish between multiple calls that might have begun on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9af35-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="9af35-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="9af35-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9af35-122">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="9af35-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9af35-123">Representa el tipo de línea de vídeo que se usa en la llamada.</span><span class="sxs-lookup"><span data-stu-id="9af35-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="9af35-124">Los valores permitidos son:</span><span class="sxs-lookup"><span data-stu-id="9af35-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9af35-125">0: audio</span><span class="sxs-lookup"><span data-stu-id="9af35-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="9af35-126">1: vídeo</span><span class="sxs-lookup"><span data-stu-id="9af35-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="9af35-127">2-video panorámico</span><span class="sxs-lookup"><span data-stu-id="9af35-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="9af35-128">3: uso compartido de aplicaciones y escritorio</span><span class="sxs-lookup"><span data-stu-id="9af35-128">3 – Application/Desktop sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9af35-129"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-129"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="9af35-130">bit</span><span class="sxs-lookup"><span data-stu-id="9af35-130">bit</span></span></p></td>
<td><p><span data-ttu-id="9af35-131">Primary</span><span class="sxs-lookup"><span data-stu-id="9af35-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="9af35-132">Extremo que hizo la llamada.</span><span class="sxs-lookup"><span data-stu-id="9af35-132">Endpoint that placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9af35-133"><strong>Únicos</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-133"><strong>Hop</strong></span></span></p></td>
<td><p><span data-ttu-id="9af35-134">int</span><span class="sxs-lookup"><span data-stu-id="9af35-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9af35-135">Salto de red/</span><span class="sxs-lookup"><span data-stu-id="9af35-135">Network hop/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9af35-136"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-136"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="9af35-137">int</span><span class="sxs-lookup"><span data-stu-id="9af35-137">int</span></span></p></td>
<td><p><span data-ttu-id="9af35-138">Extranjero</span><span class="sxs-lookup"><span data-stu-id="9af35-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9af35-139">Identificador único de la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="9af35-139">Unique identifier for the IP address.</span></span> <span data-ttu-id="9af35-140">La información de la dirección IP se almacena en la <a href="lync-server-2013-ipaddress-table.md">tabla direcciónIP de Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="9af35-140">IP address information is stored in the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9af35-141"><strong>RTT</strong></span><span class="sxs-lookup"><span data-stu-id="9af35-141"><strong>RTT</strong></span></span></p></td>
<td><p><span data-ttu-id="9af35-142">int</span><span class="sxs-lookup"><span data-stu-id="9af35-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9af35-143">Tiempo de ida y vuelta.</span><span class="sxs-lookup"><span data-stu-id="9af35-143">Roundtrip time.</span></span> <span data-ttu-id="9af35-144">El tiempo de ida y vuelta mide la cantidad de tiempo que se tarda en llegar un paquete de voz a su destino y, a continuación, se envía una notificación de que se ha recibido.</span><span class="sxs-lookup"><span data-stu-id="9af35-144">The roundtrip time measures the amount of time it takes for a voice packet to reach its destination and then send back notification that it was received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9af35-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9af35-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

