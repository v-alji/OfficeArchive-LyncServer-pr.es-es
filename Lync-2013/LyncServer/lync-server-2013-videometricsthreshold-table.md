---
title: 'Lync Server 2013: tabla VideoMetricsThreshold'
description: 'Lync Server 2013: tabla VideoMetricsThreshold.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoMetricsThreshold table
ms:assetid: 2e2f4711-35ba-48c6-b15b-5aba61c4eb75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204778(v=OCS.15)
ms:contentKeyID: 48183736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 93cdd6fb4c3c54ac1470499490f36fee87ba283d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438872"
---
# <a name="videometricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="b356d-103">Tabla VideoMetricsThreshold en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b356d-103">VideoMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b356d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b356d-104">

<span> </span></span></span>

<span data-ttu-id="b356d-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="b356d-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="b356d-106">La tabla VideoMetricsThreshold contiene valores óptimos y aceptables para la medición de la calidad de la medición que se usa con las videollamadas.</span><span class="sxs-lookup"><span data-stu-id="b356d-106">The VideoMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with video calls.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b356d-107"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="b356d-108"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="b356d-109"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="b356d-110"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b356d-111"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-111"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-112">int</span><span class="sxs-lookup"><span data-stu-id="b356d-112">int</span></span></p></td>
<td><p><span data-ttu-id="b356d-113">Primary</span><span class="sxs-lookup"><span data-stu-id="b356d-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="b356d-114">Tipo de llamada que se realizó.</span><span class="sxs-lookup"><span data-stu-id="b356d-114">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b356d-115"><strong>VideoPostFECPLROptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-115"><strong>VideoPostFECPLROptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-116">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-116">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-117">El valor predeterminado es 0,05.</span><span class="sxs-lookup"><span data-stu-id="b356d-117">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b356d-118"><strong>VideoPostFECPLRAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-118"><strong>VideoPostFECPLRAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-119">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-119">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-120">El valor predeterminado es 0,10.</span><span class="sxs-lookup"><span data-stu-id="b356d-120">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b356d-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-122">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-122">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-123">El valor predeterminado es 5,0.</span><span class="sxs-lookup"><span data-stu-id="b356d-123">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b356d-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-125">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-125">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-126">El valor predeterminado es 10,0.</span><span class="sxs-lookup"><span data-stu-id="b356d-126">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b356d-127"><strong>RecvFrameRateAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-127"><strong>RecvFrameRateAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-128">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="b356d-128">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-129">El valor predeterminado es 12,0000.</span><span class="sxs-lookup"><span data-stu-id="b356d-129">The default value is 12.0000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b356d-130"><strong>RecvFramerateAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-130"><strong>RecvFramerateAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-131">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="b356d-131">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-132">El valor predeterminado es 7,0000.</span><span class="sxs-lookup"><span data-stu-id="b356d-132">The default value is 7.0000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b356d-133"><strong>LowFrameRateCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-133"><strong>LowFrameRateCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-134">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-134">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-135">El valor predeterminado es 5,0.</span><span class="sxs-lookup"><span data-stu-id="b356d-135">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b356d-136"><strong>LowFrameRateCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-136"><strong>LowFrameRateCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-137">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-137">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-138">El valor predeterminado es 10,0/</span><span class="sxs-lookup"><span data-stu-id="b356d-138">The default value is 10.0/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b356d-139"><strong>LowResolutionCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-139"><strong>LowResolutionCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-140">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-140">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-141">El valor predeterminado es 5,0.</span><span class="sxs-lookup"><span data-stu-id="b356d-141">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b356d-142"><strong>LowResolutionCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-142"><strong>LowResolutionCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-143">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-143">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-144">El valor predeterminado es 10,0.</span><span class="sxs-lookup"><span data-stu-id="b356d-144">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b356d-145"><strong>VideoPacketLossRateOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-145"><strong>VideoPacketLossRateOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-146">foat</span><span class="sxs-lookup"><span data-stu-id="b356d-146">foat</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-147">El valor predeterminado es 0,05.</span><span class="sxs-lookup"><span data-stu-id="b356d-147">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b356d-148"><strong>VideoPacketLossRateAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-148"><strong>VideoPacketLossRateAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-149">float</span><span class="sxs-lookup"><span data-stu-id="b356d-149">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-150">El valor predeterminado es 0,10.</span><span class="sxs-lookup"><span data-stu-id="b356d-150">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b356d-151"><strong>VideoFrameRateAvgOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-151"><strong>VideoFrameRateAvgOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-152">float</span><span class="sxs-lookup"><span data-stu-id="b356d-152">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-153">El valor predeterminado es 12.</span><span class="sxs-lookup"><span data-stu-id="b356d-153">The default value is 12.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b356d-154"><strong>VideoFrameRateAvgAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-154"><strong>VideoFrameRateAvgAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-155">float</span><span class="sxs-lookup"><span data-stu-id="b356d-155">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-156">El valor predeterminado es 7.</span><span class="sxs-lookup"><span data-stu-id="b356d-156">The default value is 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b356d-157"><strong>DynamicCapabilityPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-157"><strong>DynamicCapabilityPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-158">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-158">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-159">El valor predeterminado es 5,00.</span><span class="sxs-lookup"><span data-stu-id="b356d-159">The default value is 5.00.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b356d-160"><strong>DynamicCapabilityPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b356d-160"><strong>DynamicCapabilityPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b356d-161">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b356d-161">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b356d-162">El valor predeterminado es 10,00.</span><span class="sxs-lookup"><span data-stu-id="b356d-162">The default value is 10.00.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b356d-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b356d-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

