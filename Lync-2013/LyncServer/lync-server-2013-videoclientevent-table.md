---
title: 'Lync Server 2013: Tabla VideoClientEvent'
description: 'Lync Server 2013: tabla VideoClientEvent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoClientEvent table
ms:assetid: e8ab963b-fe1d-45b3-b9bd-66a5f44c1629
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399039(v=OCS.15)
ms:contentKeyID: 48185891
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae73ac2548e838241febe60a2d31f80983b01de5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399996"
---
# <a name="videoclientevent-table-in-lync-server-2013"></a><span data-ttu-id="32d71-103">Tabla VideoClientEvent en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32d71-103">VideoClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32d71-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32d71-104">

<span> </span></span></span>

<span data-ttu-id="32d71-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="32d71-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="32d71-106">Cada registro contiene un evento de cliente para un punto final en una videollamada.</span><span class="sxs-lookup"><span data-stu-id="32d71-106">Each record contains client event for one endpoint in a video call.</span></span> <span data-ttu-id="32d71-107">Generalmente, una llamada tiene dos registros: uno para el autor de la llamada y otro para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="32d71-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32d71-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="32d71-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="32d71-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="32d71-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32d71-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="32d71-113">datetime</span><span class="sxs-lookup"><span data-stu-id="32d71-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="32d71-114">Primary</span><span class="sxs-lookup"><span data-stu-id="32d71-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="32d71-115">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="32d71-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32d71-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="32d71-117">int</span><span class="sxs-lookup"><span data-stu-id="32d71-117">int</span></span></p></td>
<td><p><span data-ttu-id="32d71-118">Primary</span><span class="sxs-lookup"><span data-stu-id="32d71-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="32d71-119">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="32d71-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32d71-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="32d71-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="32d71-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="32d71-122">Primary</span><span class="sxs-lookup"><span data-stu-id="32d71-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="32d71-123">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="32d71-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32d71-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="32d71-125">bit</span><span class="sxs-lookup"><span data-stu-id="32d71-125">bit</span></span></p></td>
<td><p><span data-ttu-id="32d71-126">Primary</span><span class="sxs-lookup"><span data-stu-id="32d71-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="32d71-127">0: datos del destinatario de la llamada</span><span class="sxs-lookup"><span data-stu-id="32d71-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="32d71-128">1: datos del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="32d71-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32d71-129"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-129"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="32d71-130">Porcentaje de sesión el evento LowBandwidth se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="32d71-130">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="32d71-131">El ancho de banda disponible es insuficiente para una experiencia de voz aceptable.</span><span class="sxs-lookup"><span data-stu-id="32d71-131">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32d71-132"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="32d71-132"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="32d71-133">Porcentaje de sesión el evento ReceiveSendQuality se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="32d71-133">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="32d71-134">La calidad de la red en términos de vibración o pérdida de paquetes es grave y afecta la calidad de audio que se recibe.</span><span class="sxs-lookup"><span data-stu-id="32d71-134">Network quality in terms of jitter or packet loss is severe and impacts the quality of audio being received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="32d71-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32d71-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

