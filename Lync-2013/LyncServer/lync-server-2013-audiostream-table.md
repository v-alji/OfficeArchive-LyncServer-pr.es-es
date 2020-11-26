---
title: 'Lync Server 2013: Tabla AudioStream'
description: 'Lync Server 2013: tabla AudioStream.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStream table
ms:assetid: 49ccbbc3-2f73-45fc-80a6-e612535cbc10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425961(v=OCS.15)
ms:contentKeyID: 48184077
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af2e622e14c54fa4f9a6313e1b0dae8f2483132
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438179"
---
# <a name="audiostream-table-in-lync-server-2013"></a><span data-ttu-id="57790-103">Tabla AudioStream en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57790-103">AudioStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57790-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57790-104">

<span> </span></span></span>

<span data-ttu-id="57790-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="57790-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="57790-106">Cada registro representa una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="57790-106">Each record represents one audio stream.</span></span> <span data-ttu-id="57790-107">Una línea de medios de audio normalmente contiene dos secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="57790-107">One audio media line usually contains two audio streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57790-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="57790-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="57790-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="57790-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="57790-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="57790-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="57790-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="57790-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57790-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="57790-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-113">datetime</span><span class="sxs-lookup"><span data-stu-id="57790-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="57790-114">Primary</span><span class="sxs-lookup"><span data-stu-id="57790-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="57790-115">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="57790-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="57790-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-117">int</span><span class="sxs-lookup"><span data-stu-id="57790-117">int</span></span></p></td>
<td><p><span data-ttu-id="57790-118">Primary</span><span class="sxs-lookup"><span data-stu-id="57790-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="57790-119">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="57790-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="57790-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="57790-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="57790-122">Primary</span><span class="sxs-lookup"><span data-stu-id="57790-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="57790-123">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="57790-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="57790-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-125">int</span><span class="sxs-lookup"><span data-stu-id="57790-125">int</span></span></p></td>
<td><p><span data-ttu-id="57790-126">Primary</span><span class="sxs-lookup"><span data-stu-id="57790-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="57790-127">IDENTIFICADOR exclusivo dentro de una línea de medios.</span><span class="sxs-lookup"><span data-stu-id="57790-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-128"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="57790-128"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-129">int</span><span class="sxs-lookup"><span data-stu-id="57790-129">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-130">Vibración de red media de las estadísticas del Protocolo de control de tiempo real (RTCP).</span><span class="sxs-lookup"><span data-stu-id="57790-130">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-131"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="57790-131"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-132">int</span><span class="sxs-lookup"><span data-stu-id="57790-132">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-133">Vibración máxima de la red durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-133">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-134"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="57790-134"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-135">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="57790-135">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-136">Tasa promedio de pérdida de paquetes durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-136">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-137"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="57790-137"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-138">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="57790-138">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-139">Pérdida máxima de paquetes observadas durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-139">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-140"><strong>BurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="57790-140"><strong>BurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-141">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="57790-141">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-142">Densidad promedio de pérdida de paquetes durante las ráfagas de pérdidas durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-142">Average density of packet Loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-143"><strong>BurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="57790-143"><strong>BurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-144">int</span><span class="sxs-lookup"><span data-stu-id="57790-144">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-145">Duración media de pérdida de paquetes durante ráfagas de pérdidas durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-145">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-146"><strong>BurstGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="57790-146"><strong>BurstGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-147">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="57790-147">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-148">Densidad media de pérdida de paquetes entre ráfagas de pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="57790-148">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-149"><strong>BurstGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="57790-149"><strong>BurstGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-150">int</span><span class="sxs-lookup"><span data-stu-id="57790-150">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-151">Duración media de los huecos entre las ráfagas de pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="57790-151">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-152"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="57790-152"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-153">ENT</span><span class="sxs-lookup"><span data-stu-id="57790-153">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-154">Recuento de paquetes de la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="57790-154">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-155"><strong>Ancho de banda más</strong></span><span class="sxs-lookup"><span data-stu-id="57790-155"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-156">ENT</span><span class="sxs-lookup"><span data-stu-id="57790-156">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-157">Cálculo de ancho de banda para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="57790-157">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-158"><strong>DegradationAvg</strong></span><span class="sxs-lookup"><span data-stu-id="57790-158"><strong>DegradationAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-159">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-159">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-160">Degradación de MOS de red para toda la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-160">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="57790-161">El intervalo está comprendido entre 0,0 y 5,0.</span><span class="sxs-lookup"><span data-stu-id="57790-161">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="57790-162">Esta métrica muestra el monto que se redujo en el MOS de red debido a la vibración y a la pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="57790-162">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="57790-163">Para una calidad aceptable, debe ser menor que 0,5.</span><span class="sxs-lookup"><span data-stu-id="57790-163">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-164"><strong>DegradationMax</strong></span><span class="sxs-lookup"><span data-stu-id="57790-164"><strong>DegradationMax</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-165">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-165">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-166">La degradación de OP máxima de red durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-166">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-167"><strong>DegradationJitterAvg</strong></span><span class="sxs-lookup"><span data-stu-id="57790-167"><strong>DegradationJitterAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-168">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-168">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-169">Degradación de MOS de red causada por vibración.</span><span class="sxs-lookup"><span data-stu-id="57790-169">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-170"><strong>DegradationPacketLossAvg</strong></span><span class="sxs-lookup"><span data-stu-id="57790-170"><strong>DegradationPacketLossAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-171">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-171">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-172">Degradación de MOS de red causada por pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="57790-172">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-173"><strong>AudioPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="57790-173"><strong>AudioPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-174">int</span><span class="sxs-lookup"><span data-stu-id="57790-174">int</span></span></p></td>
<td><p><span data-ttu-id="57790-175">Extranjero</span><span class="sxs-lookup"><span data-stu-id="57790-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="57790-176">El códec de audio usado para la llamada, al que se hace referencia desde la tabla PayloadDescription.</span><span class="sxs-lookup"><span data-stu-id="57790-176">The audio Codec used for the call, referenced from PayloadDescription Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-177"><strong>AudioSampleRate</strong></span><span class="sxs-lookup"><span data-stu-id="57790-177"><strong>AudioSampleRate</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-178">int</span><span class="sxs-lookup"><span data-stu-id="57790-178">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-179">Frecuencia de muestreo de la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="57790-179">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-180"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="57790-180"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-181">int</span><span class="sxs-lookup"><span data-stu-id="57790-181">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-182">Tiempo de ida y vuelta de las estadísticas de RTCP.</span><span class="sxs-lookup"><span data-stu-id="57790-182">Round trip time from RTCP statistics.</span></span> <span data-ttu-id="57790-183">Para obtener una calidad aceptable, debe ser inferior a 100 $.</span><span class="sxs-lookup"><span data-stu-id="57790-183">For acceptable quality this should be less than 100ms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-184"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="57790-184"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-185">int</span><span class="sxs-lookup"><span data-stu-id="57790-185">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-186">Tiempo máximo de ida y vuelta para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="57790-186">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-187"><strong>OverallAvgNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="57790-187"><strong>OverallAvgNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-188">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-188">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-189">MOS de red de banda ancha promedio para la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-189">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="57790-190">Esta métrica depende de la pérdida del paquete, de la vibración y del códec usado.</span><span class="sxs-lookup"><span data-stu-id="57790-190">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="57790-191">El rango es de [1,0 a 5,0].</span><span class="sxs-lookup"><span data-stu-id="57790-191">Range is [1.0 to 5.0].</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-192"><strong>OverallMinNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="57790-192"><strong>OverallMinNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-193">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-193">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-194">MOS de red de banda ancha mínima para la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-194">The minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-195"><strong>SendListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="57790-195"><strong>SendListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-196">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-196">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-197">La puntuación media de escucha de banda ancha prevista para el audio enviado, incluyendo el nivel de voz, el nivel de ruido y las características del dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="57790-197">The average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-198"><strong>SendListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="57790-198"><strong>SendListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-199">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-199">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-200">El SendListenMOS mínimo para la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-200">The minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-201"><strong>RecvListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="57790-201"><strong>RecvListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-202">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-202">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-203">La puntuación media de escucha de banda ancha prevista para el audio recibido de la red, incluido el nivel de voz, el nivel de ruido, el códec, las condiciones de la red y las características del dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="57790-203">The average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-204"><strong>RecvListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="57790-204"><strong>RecvListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-205">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="57790-205">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-206">El RecvListenMOS mínimo para la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-206">The minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-207"><strong>AudioFECUsed</strong></span><span class="sxs-lookup"><span data-stu-id="57790-207"><strong>AudioFECUsed</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-208">bit</span><span class="sxs-lookup"><span data-stu-id="57790-208">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-209">Marca que indica si se usó el audio FEC para la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-209">Flag indicating if audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-210"><strong>RatioConcealedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="57790-210"><strong>RatioConcealedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-211">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="57790-211">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-212">Relación media entre las muestras ocultas generadas por la corrección de audio a muestras típicas.</span><span class="sxs-lookup"><span data-stu-id="57790-212">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-213"><strong>RatioStretchedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="57790-213"><strong>RatioStretchedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-214">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="57790-214">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-215">Relación media de muestras extendidas generadas por la recuperación de audio a muestras típicas.</span><span class="sxs-lookup"><span data-stu-id="57790-215">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-216"><strong>RatioCompressedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="57790-216"><strong>RatioCompressedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-217">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="57790-217">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-218">Relación media de muestras comprimidas generadas por la corrección de audio a muestras típicas.</span><span class="sxs-lookup"><span data-stu-id="57790-218">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-219"><strong>Entrada</strong></span><span class="sxs-lookup"><span data-stu-id="57790-219"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-220">bit</span><span class="sxs-lookup"><span data-stu-id="57790-220">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-221">Se reciben los datos de la secuencia del lado del destinatario.</span><span class="sxs-lookup"><span data-stu-id="57790-221">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-222"><strong>Saliente</strong></span><span class="sxs-lookup"><span data-stu-id="57790-222"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-223">bit</span><span class="sxs-lookup"><span data-stu-id="57790-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-224">Se reciben los datos de la secuencia en el lado del remitente.</span><span class="sxs-lookup"><span data-stu-id="57790-224">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-225"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="57790-225"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-226">bit</span><span class="sxs-lookup"><span data-stu-id="57790-226">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="57790-227">1 significa que la dirección de la transmisión es de la persona que llama al destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-227">1 means the stream direction is from the caller to the callee.</span></span></p>
<p><span data-ttu-id="57790-228">0 significa que la dirección de la transmisión es de la persona que llama a la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="57790-228">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-229"><strong>JitterInterArrivalSD</strong></span><span class="sxs-lookup"><span data-stu-id="57790-229"><strong>JitterInterArrivalSD</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-230">float</span><span class="sxs-lookup"><span data-stu-id="57790-230">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-231">Desviación estándar para las horas de llegada de la vibración.</span><span class="sxs-lookup"><span data-stu-id="57790-231">Standard deviation for jitter arrival times.</span></span></p>
<p><span data-ttu-id="57790-232">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-232">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-233"><strong>ConcealRatioMax</strong></span><span class="sxs-lookup"><span data-stu-id="57790-233"><strong>ConcealRatioMax</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-234">float</span><span class="sxs-lookup"><span data-stu-id="57790-234">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-235">Relación máxima de paquetes ocultos por el Healer.</span><span class="sxs-lookup"><span data-stu-id="57790-235">Maximum ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="57790-236">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-236">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-237"><strong>ConcealRatioSD</strong></span><span class="sxs-lookup"><span data-stu-id="57790-237"><strong>ConcealRatioSD</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-238">float</span><span class="sxs-lookup"><span data-stu-id="57790-238">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-239">Desviación estándar para la proporción de paquetes ocultos por el Healer.</span><span class="sxs-lookup"><span data-stu-id="57790-239">Standard deviation for the ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="57790-240">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-240">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-241"><strong>HealerPacketDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="57790-241"><strong>HealerPacketDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-242">float</span><span class="sxs-lookup"><span data-stu-id="57790-242">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-243">Proporción de paquetes descartados por el healro comparado con el número total de paquetes recibidos.</span><span class="sxs-lookup"><span data-stu-id="57790-243">Ratio of packets dropped by the healer compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="57790-244">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-244">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-245"><strong>HealerFECPacketUsedRatio</strong></span><span class="sxs-lookup"><span data-stu-id="57790-245"><strong>HealerFECPacketUsedRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-246">float</span><span class="sxs-lookup"><span data-stu-id="57790-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-247">Relación entre los paquetes de corrección de errores de reenvío en comparación con el número total de paquetes recibidos.</span><span class="sxs-lookup"><span data-stu-id="57790-247">Ratio of used forward error correction packets compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="57790-248">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-248">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-249"><strong>MaxCompressedSamples</strong></span><span class="sxs-lookup"><span data-stu-id="57790-249"><strong>MaxCompressedSamples</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-250">float</span><span class="sxs-lookup"><span data-stu-id="57790-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-251">Número máximo de paquetes de audio que el Healer ha comprimido.</span><span class="sxs-lookup"><span data-stu-id="57790-251">Maximum number of audio packets that were compressed by the healer.</span></span></p>
<p><span data-ttu-id="57790-252">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-253"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="57790-253"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-254">float</span><span class="sxs-lookup"><span data-stu-id="57790-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-255">Indica el porcentaje de la hora en que la llamada se encontraba en un estado de congestión de pérdida.</span><span class="sxs-lookup"><span data-stu-id="57790-255">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="57790-256">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-256">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-257"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="57790-257"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-258">float</span><span class="sxs-lookup"><span data-stu-id="57790-258">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-259">Indica el porcentaje de la llamada durante el cual la congestión fue causada por la llegada demorada de los paquetes de red.</span><span class="sxs-lookup"><span data-stu-id="57790-259">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="57790-260">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-260">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-261"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="57790-261"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-262">float</span><span class="sxs-lookup"><span data-stu-id="57790-262">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-263">Indica el porcentaje de la hora en que la llamada compite en los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="57790-263">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="57790-264">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-264">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-265"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="57790-265"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-266">int</span><span class="sxs-lookup"><span data-stu-id="57790-266">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-267">Cantidad mínima de estimación del ancho de banda medido durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-267">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="57790-268">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-269"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="57790-269"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-270">int</span><span class="sxs-lookup"><span data-stu-id="57790-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-271">Cantidad máxima de estimación del ancho de banda medido durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-271">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="57790-272">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-272">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-273"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="57790-273"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-274">int</span><span class="sxs-lookup"><span data-stu-id="57790-274">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-275">Desviación estándar de la estimación del ancho de banda medida durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-275">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="57790-276">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-276">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-277"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="57790-277"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-278">int</span><span class="sxs-lookup"><span data-stu-id="57790-278">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-279">Cantidad promedio de estimación del ancho de banda medido durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="57790-279">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="57790-280">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-281"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="57790-281"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-282">float</span><span class="sxs-lookup"><span data-stu-id="57790-282">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-283">Cantidad total de latencia unidireccional.</span><span class="sxs-lookup"><span data-stu-id="57790-283">Total amount of one-way latency.</span></span> <span data-ttu-id="57790-284">Latencia unidireccional relativa mide el retraso entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57790-284">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="57790-285">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-285">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-286"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="57790-286"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-287">float</span><span class="sxs-lookup"><span data-stu-id="57790-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-288">Cantidad promedio de latencia unidireccional.</span><span class="sxs-lookup"><span data-stu-id="57790-288">Average amount of one-way latency.</span></span> <span data-ttu-id="57790-289">Latencia unidireccional relativa mide el retraso entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57790-289">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="57790-290">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-290">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-291"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="57790-291"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-292">float</span><span class="sxs-lookup"><span data-stu-id="57790-292">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-293">Cantidad máxima de latencia unidireccional.</span><span class="sxs-lookup"><span data-stu-id="57790-293">Maximum amount of one-way latency.</span></span> <span data-ttu-id="57790-294">Latencia unidireccional relativa mide el retraso entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57790-294">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="57790-295">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-295">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-296"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="57790-296"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-297">int</span><span class="sxs-lookup"><span data-stu-id="57790-297">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-298">Total de repeticiones de ráfagas unidireccionales.</span><span class="sxs-lookup"><span data-stu-id="57790-298">Total one-way burst occurrences.</span></span> <span data-ttu-id="57790-299">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="57790-299">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="57790-300">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57790-300">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="57790-301">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-302"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="57790-302"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-303">float</span><span class="sxs-lookup"><span data-stu-id="57790-303">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-304">Densidad de ráfaga unidireccional total.</span><span class="sxs-lookup"><span data-stu-id="57790-304">Total one-way burst density.</span></span> <span data-ttu-id="57790-305">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="57790-305">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="57790-306">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57790-306">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="57790-307">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-307">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-308"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="57790-308"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-309">float</span><span class="sxs-lookup"><span data-stu-id="57790-309">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-310">Total de duración de ráfaga unidireccional.</span><span class="sxs-lookup"><span data-stu-id="57790-310">Total one-way burst duration.</span></span> <span data-ttu-id="57790-311">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="57790-311">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="57790-312">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57790-312">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="57790-313">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-313">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-314"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="57790-314"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-315">int</span><span class="sxs-lookup"><span data-stu-id="57790-315">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-316">Total de repeticiones de intervalos unidireccionales.</span><span class="sxs-lookup"><span data-stu-id="57790-316">Total one-way gap occurrences.</span></span> <span data-ttu-id="57790-317">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante; los huecos indican retrasos entre estas ráfagas.</span><span class="sxs-lookup"><span data-stu-id="57790-317">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="57790-318">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57790-318">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="57790-319">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-319">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-320"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="57790-320"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-321">float</span><span class="sxs-lookup"><span data-stu-id="57790-321">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-322">Densidad de brechas en un camino total.</span><span class="sxs-lookup"><span data-stu-id="57790-322">Total one-way gap density.</span></span> <span data-ttu-id="57790-323">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante; los huecos indican retrasos entre estas ráfagas.</span><span class="sxs-lookup"><span data-stu-id="57790-323">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="57790-324">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57790-324">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="57790-325">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-326"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="57790-326"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-327">float</span><span class="sxs-lookup"><span data-stu-id="57790-327">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-328">Duración del intervalo unidireccional total.</span><span class="sxs-lookup"><span data-stu-id="57790-328">Total one-way gap duration.</span></span> <span data-ttu-id="57790-329">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante; los huecos indican retrasos entre estas ráfagas.</span><span class="sxs-lookup"><span data-stu-id="57790-329">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="57790-330">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57790-330">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="57790-331">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-332"><strong>DecodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="57790-332"><strong>DecodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-333">float</span><span class="sxs-lookup"><span data-stu-id="57790-333">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-334">Porcentaje de la llamada descodificada como estéreo.</span><span class="sxs-lookup"><span data-stu-id="57790-334">Percentage of the call decoded as stereo.</span></span></p>
<p><span data-ttu-id="57790-335">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-336"><strong>AecRenderStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="57790-336"><strong>AecRenderStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-337">float</span><span class="sxs-lookup"><span data-stu-id="57790-337">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-338">Porcentaje de la llamada representada como estéreo por el cancelador de eco acústico.</span><span class="sxs-lookup"><span data-stu-id="57790-338">Percentage of the call rendered as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="57790-339">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-339">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-340"><strong>AudioPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="57790-340"><strong>AudioPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-341">float</span><span class="sxs-lookup"><span data-stu-id="57790-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-342">Tasa de pérdida de paquetes después de aplicar la corrección de errores de reenvío.</span><span class="sxs-lookup"><span data-stu-id="57790-342">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="57790-343">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-343">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57790-344"><strong>EncodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="57790-344"><strong>EncodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-345">float</span><span class="sxs-lookup"><span data-stu-id="57790-345">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-346">Porcentaje de la llamada codificada como estéreo.</span><span class="sxs-lookup"><span data-stu-id="57790-346">Percentage of the call encoded as stereo.</span></span></p>
<p><span data-ttu-id="57790-347">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-347">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57790-348"><strong>AecCaptureStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="57790-348"><strong>AecCaptureStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="57790-349">float</span><span class="sxs-lookup"><span data-stu-id="57790-349">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="57790-350">Porcentaje de la llamada capturada como estéreo por el cancelador de eco acústico.</span><span class="sxs-lookup"><span data-stu-id="57790-350">Percentage of the call captured as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="57790-351">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57790-351">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="57790-352">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57790-352">


</div>

<span> </span>

</div>

</div>

</span></span></div>

