---
title: 'Lync Server 2013: tabla AppSharingMetricsThreshold'
description: 'Lync Server 2013: tabla AppSharingMetricsThreshold.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingMetricsThreshold table
ms:assetid: 782cfab9-01a6-4843-aea1-28f47b0b51f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205018(v=OCS.15)
ms:contentKeyID: 48184556
ms.date: 12/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 092c7d08026e6b736b81043a71b4ecaabc4d5f1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439875"
---
# <a name="appsharingmetricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="e040e-103">Tabla AppSharingMetricsThreshold en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e040e-103">AppSharingMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e040e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e040e-104">

<span> </span></span></span>

<span data-ttu-id="e040e-105">_**Última modificación del tema:** 2015-12-08_</span><span class="sxs-lookup"><span data-stu-id="e040e-105">_**Topic Last Modified:** 2015-12-08_</span></span>

<span data-ttu-id="e040e-106">La tabla AppSharingMetricsThreshold contiene valores óptimos y aceptables para las métricas de la calidad de la experiencia que se usan con el uso compartido de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e040e-106">The AppSharingMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with application sharing.</span></span> <span data-ttu-id="e040e-107">Estos umbrales se usan para determinar si la experiencia de uso compartido de aplicaciones se debe clasificar como mala.</span><span class="sxs-lookup"><span data-stu-id="e040e-107">These thresholds are used to determine if the application sharing experience should be classified as poor.</span></span>

<span data-ttu-id="e040e-108">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e040e-109"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="e040e-110"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="e040e-111"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="e040e-112"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e040e-113"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-113"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-114">int</span><span class="sxs-lookup"><span data-stu-id="e040e-114">int</span></span></p></td>
<td><p><span data-ttu-id="e040e-115">Primary</span><span class="sxs-lookup"><span data-stu-id="e040e-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="e040e-116">Tipo de llamada que se realizó.</span><span class="sxs-lookup"><span data-stu-id="e040e-116">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e040e-117"><strong>AppliedBandwidthLimitOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-117"><strong>AppliedBandwidthLimitOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-118">int</span><span class="sxs-lookup"><span data-stu-id="e040e-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-119">Límite de ancho de banda óptimo para compartir aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e040e-119">Optimal bandwidth limitation for application sharing.</span></span> <span data-ttu-id="e040e-120">El valor predeterminado es 1 millón.</span><span class="sxs-lookup"><span data-stu-id="e040e-120">The default value is 1000000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e040e-121"><strong>AppliedBandwidthLimitAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-121"><strong>AppliedBandwidthLimitAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-122">int</span><span class="sxs-lookup"><span data-stu-id="e040e-122">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-123">Limitación de ancho de banda aceptable para el uso compartido de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e040e-123">Acceptable bandwidth limitation for application sharing.</span></span> <span data-ttu-id="e040e-124">El valor predeterminado es 500000.</span><span class="sxs-lookup"><span data-stu-id="e040e-124">The default value is 500000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e040e-125"><strong>SpoiledTilePercentTotalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-125"><strong>SpoiledTilePercentTotalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-126">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="e040e-126">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-127">Tasa de porcentaje óptima para los mosaicos "estropeados" para clasificar la calidad de uso compartido de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e040e-127">Optimal percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="e040e-128">Este valor es el porcentaje del contenido del que el que comparte no ha podido comunicarse con el visor.</span><span class="sxs-lookup"><span data-stu-id="e040e-128">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="e040e-129">El contenido puede ser descartado (o estropeado) cuando el compartidor descarta los mosaicos del origen de los gráficos o los mosaicos de ASMCU descarta los mosaicos del compartidor, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e040e-129">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="e040e-130">El valor predeterminado es 11 por ciento.</span><span class="sxs-lookup"><span data-stu-id="e040e-130">The default value is 11 percent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e040e-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-132">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="e040e-132">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-133">tasa porcentual de cceptable para los cuadros "estropeados" para clasificar la calidad de uso compartido de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e040e-133">cceptable percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="e040e-134">Este valor es el porcentaje del contenido del que el que comparte no ha podido comunicarse con el visor.</span><span class="sxs-lookup"><span data-stu-id="e040e-134">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="e040e-135">El contenido puede ser descartado (o estropeado) cuando el compartidor descarta los mosaicos del origen de los gráficos o los mosaicos de ASMCU descarta los mosaicos del compartidor, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e040e-135">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="e040e-136">El valor predeterminado es 36 por ciento.</span><span class="sxs-lookup"><span data-stu-id="e040e-136">The default value is 36 percent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e040e-137"><strong>JitterInterArrivalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-137"><strong>JitterInterArrivalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-138">int</span><span class="sxs-lookup"><span data-stu-id="e040e-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-139">Esta columna no se usa en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-139">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e040e-140"><strong>JitterInterArrivalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-140"><strong>JitterInterArrivalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-141">int</span><span class="sxs-lookup"><span data-stu-id="e040e-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-142">Esta columna no se usa en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-142">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e040e-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-144">float</span><span class="sxs-lookup"><span data-stu-id="e040e-144">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-145">Esta columna no se usa en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-145">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e040e-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-147">float</span><span class="sxs-lookup"><span data-stu-id="e040e-147">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-148">Esta columna no se usa en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-148">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e040e-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-150">float</span><span class="sxs-lookup"><span data-stu-id="e040e-150">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-151">Esta columna no se usa en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-151">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e040e-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-153">float</span><span class="sxs-lookup"><span data-stu-id="e040e-153">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-154">Esta columna no se usa en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-154">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e040e-155"><strong>RelativeOneWayAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-155"><strong>RelativeOneWayAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-156">float</span><span class="sxs-lookup"><span data-stu-id="e040e-156">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-157">Valor óptimo para el retraso relativo relativo entre los dos extremos multimedia implicados en el uso compartido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e040e-157">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="e040e-158">Es una medición de la latencia de un solo salto.</span><span class="sxs-lookup"><span data-stu-id="e040e-158">This is a single-hop latency measure.</span></span> <span data-ttu-id="e040e-159">El valor predeterminado es 1,0 segundos.</span><span class="sxs-lookup"><span data-stu-id="e040e-159">The default value is 1.0 seconds.</span></span></p>
<p><span data-ttu-id="e040e-160">La columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-160">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e040e-161"><strong>RelativeOneWayAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-161"><strong>RelativeOneWayAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-162">float</span><span class="sxs-lookup"><span data-stu-id="e040e-162">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-163">Valor óptimo para el retraso relativo relativo entre los dos extremos multimedia implicados en el uso compartido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e040e-163">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="e040e-164">Es una medición de la latencia de un solo salto.</span><span class="sxs-lookup"><span data-stu-id="e040e-164">This is a single-hop latency measure.</span></span> <span data-ttu-id="e040e-165">El valor predeterminado es 1,75 segundos.</span><span class="sxs-lookup"><span data-stu-id="e040e-165">The default value is 1.75 seconds.</span></span></p>
<p><span data-ttu-id="e040e-166">La columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-166">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e040e-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-168">float</span><span class="sxs-lookup"><span data-stu-id="e040e-168">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-169">Valor óptimo de la latencia media de procesamiento de mosaicos RDP en el servidor de conferencia como durante la duración de la sesión de visualización.</span><span class="sxs-lookup"><span data-stu-id="e040e-169">Optimal value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="e040e-170">Latencia es la diferencia horaria entre cuando el fotograma inicial está codificado en el servidor (compartidor o MCU, según el escenario) y se descodifica el mismo fotograma de inicio en el visor.</span><span class="sxs-lookup"><span data-stu-id="e040e-170">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="e040e-171">Una media alta refleja un retraso mayor en la experiencia de visualización.</span><span class="sxs-lookup"><span data-stu-id="e040e-171">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="e040e-172">Un servidor de conferencias sobrecargado podría experimentar una media mayor de retrasos.</span><span class="sxs-lookup"><span data-stu-id="e040e-172">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="e040e-173">El valor predeterminado es 200ms.</span><span class="sxs-lookup"><span data-stu-id="e040e-173">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="e040e-174">La columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-174">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e040e-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e040e-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e040e-176">float</span><span class="sxs-lookup"><span data-stu-id="e040e-176">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e040e-177">Valor aceptable de la latencia media de procesamiento de mosaicos RDP en el servidor de conferencia como durante la duración de la sesión de visualización.</span><span class="sxs-lookup"><span data-stu-id="e040e-177">Acceptable value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="e040e-178">Latencia es la diferencia horaria entre cuando el fotograma inicial está codificado en el servidor (compartidor o MCU, según el escenario) y se descodifica el mismo fotograma de inicio en el visor.</span><span class="sxs-lookup"><span data-stu-id="e040e-178">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="e040e-179">Una media alta refleja un retraso mayor en la experiencia de visualización.</span><span class="sxs-lookup"><span data-stu-id="e040e-179">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="e040e-180">Un servidor de conferencias sobrecargado podría experimentar una media mayor de retrasos.</span><span class="sxs-lookup"><span data-stu-id="e040e-180">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="e040e-181">El valor predeterminado es 200ms.</span><span class="sxs-lookup"><span data-stu-id="e040e-181">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="e040e-182">La columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e040e-182">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e040e-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e040e-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

