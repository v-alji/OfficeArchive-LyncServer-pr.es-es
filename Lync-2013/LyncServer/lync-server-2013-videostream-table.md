---
title: 'Lync Server 2013: Tabla VideoStream'
description: 'Lync Server 2013: tabla de Videostream.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStream table
ms:assetid: 4275ede7-5467-4a97-b8c8-a4b00917bf32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425928(v=OCS.15)
ms:contentKeyID: 48184014
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d741478e1f6290685181bff471f143e41ce9ca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444129"
---
# <a name="videostream-table-in-lync-server-2013"></a><span data-ttu-id="6dccc-103">Tabla VideoStream en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6dccc-103">VideoStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6dccc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6dccc-104">

<span> </span></span></span>

<span data-ttu-id="6dccc-105">_**Última modificación del tema:** 2013-12-13_</span><span class="sxs-lookup"><span data-stu-id="6dccc-105">_**Topic Last Modified:** 2013-12-13_</span></span>

<span data-ttu-id="6dccc-106">Cada registro representa una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6dccc-106">Each record represents one video stream.</span></span> <span data-ttu-id="6dccc-107">Una línea de medios de vídeo suele contener dos secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6dccc-107">One video media line usually contains two video streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dccc-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="6dccc-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="6dccc-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="6dccc-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-113">datetime</span><span class="sxs-lookup"><span data-stu-id="6dccc-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="6dccc-114">Primary</span><span class="sxs-lookup"><span data-stu-id="6dccc-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="6dccc-115">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="6dccc-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-117">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-117">int</span></span></p></td>
<td><p><span data-ttu-id="6dccc-118">Primary</span><span class="sxs-lookup"><span data-stu-id="6dccc-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="6dccc-119">R al que se hace referencia en la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="6dccc-119">R Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="6dccc-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="6dccc-122">Primary</span><span class="sxs-lookup"><span data-stu-id="6dccc-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="6dccc-123">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="6dccc-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-125">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-125">int</span></span></p></td>
<td><p><span data-ttu-id="6dccc-126">Primary</span><span class="sxs-lookup"><span data-stu-id="6dccc-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="6dccc-127">IDENTIFICADOR exclusivo dentro de una línea de medios.</span><span class="sxs-lookup"><span data-stu-id="6dccc-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-128"><strong>VideoPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-128"><strong>VideoPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-129">smallint</span><span class="sxs-lookup"><span data-stu-id="6dccc-129">smallint</span></span></p></td>
<td><p><span data-ttu-id="6dccc-130">Externo, principal</span><span class="sxs-lookup"><span data-stu-id="6dccc-130">Foreign, Primary</span></span></p></td>
<td><p><span data-ttu-id="6dccc-131">Descripción de la carga.</span><span class="sxs-lookup"><span data-stu-id="6dccc-131">Payload description.</span></span> <span data-ttu-id="6dccc-132">Para obtener más información, consulte la <a href="lync-server-2013-payloaddescription-table.md">tabla PayloadDescription en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6dccc-132">See the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-134">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-134">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-135">Vibración de red media de las estadísticas del Protocolo de control de tiempo real (RTCP).</span><span class="sxs-lookup"><span data-stu-id="6dccc-135">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-136"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-136"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-137">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-137">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-138">Vibración máxima de red durante la sesión de video.</span><span class="sxs-lookup"><span data-stu-id="6dccc-138">Maximum network jitter during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-139"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-139"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-140">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-140">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-141">Tiempo de ida y vuelta de las estadísticas de RTCP.</span><span class="sxs-lookup"><span data-stu-id="6dccc-141">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-142"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-142"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-143">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-143">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-144">Tiempo máximo de ida y vuelta para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6dccc-144">Maximum round trip time for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-145"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-145"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-146">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="6dccc-146">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-147">Tasa promedio de pérdida de paquetes durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="6dccc-147">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-148"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-148"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-149">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="6dccc-149">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-150">Pérdida máxima de paquetes observadas durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="6dccc-150">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-151"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-151"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-152">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-152">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-153">Recuento de paquetes para la secuencia de vídeo (Protocolo de transporte en tiempo real, RTP).</span><span class="sxs-lookup"><span data-stu-id="6dccc-153">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-154"><strong>Ancho de banda más</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-154"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-155">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-155">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-156">Cálculo de ancho de banda para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6dccc-156">Bandwidth estimates for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-157"><strong>Resolución de la</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-157"><strong>VideoResolution</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-158">carácter (9)</span><span class="sxs-lookup"><span data-stu-id="6dccc-158">char(9)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-159">Resolución del vídeo en píxeles ancho multiplicado por píxeles alto.</span><span class="sxs-lookup"><span data-stu-id="6dccc-159">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="6dccc-160">Se ha notificado como una cadena.</span><span class="sxs-lookup"><span data-stu-id="6dccc-160">Reported as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-161"><strong>VideoBitRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-161"><strong>VideoBitRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-162">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-162">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-163">Promedio de velocidad de bits de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6dccc-163">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-164"><strong>InboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-164"><strong>InboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-165">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="6dccc-165">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-166">La velocidad de fotogramas de vídeo recibida.</span><span class="sxs-lookup"><span data-stu-id="6dccc-166">The video frame rate received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-167"><strong>OutboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-167"><strong>OutboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-168">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="6dccc-168">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-169">La velocidad de fotogramas de vídeo enviada.</span><span class="sxs-lookup"><span data-stu-id="6dccc-169">The video frame rate sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-170"><strong>VideoBitRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-170"><strong>VideoBitRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-171">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-172">La máxima tasa de bits de vídeo durante la sesión de video.</span><span class="sxs-lookup"><span data-stu-id="6dccc-172">The maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-173"><strong>VideoFrameLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-173"><strong>VideoFrameLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-174">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="6dccc-174">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-175">El porcentaje de fotogramas de video totales que se pierden.</span><span class="sxs-lookup"><span data-stu-id="6dccc-175">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-176"><strong>VideoFEC</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-176"><strong>VideoFEC</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-177">bit</span><span class="sxs-lookup"><span data-stu-id="6dccc-177">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-178">No disponible.</span><span class="sxs-lookup"><span data-stu-id="6dccc-178">Not available.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-179"><strong>Media</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-180">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="6dccc-180">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-181">El porcentaje de fotogramas de video totales que se pierden.</span><span class="sxs-lookup"><span data-stu-id="6dccc-181">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-182"><strong>CIFQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-182"><strong>CIFQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-183">tinyint</span><span class="sxs-lookup"><span data-stu-id="6dccc-183">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-184">El porcentaje de la llamada que se encontraba en la resolución de formato de intercambio común (CIF).</span><span class="sxs-lookup"><span data-stu-id="6dccc-184">The percentage of the call that was at the Common Interchange Format (CIF) resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-185"><strong>VGAQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-185"><strong>VGAQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-186">tinyint</span><span class="sxs-lookup"><span data-stu-id="6dccc-186">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-187">El porcentaje de la llamada que se mostraba en la resolución VGA.</span><span class="sxs-lookup"><span data-stu-id="6dccc-187">The percentage of the call that was at VGA resolution.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-188"><strong>HD720QualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-188"><strong>HD720QualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="6dccc-189">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-190">El porcentaje de la llamada que se encontraba en la resolución de HD720.</span><span class="sxs-lookup"><span data-stu-id="6dccc-190">The percentage of the call that was at HD720 resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-191"><strong>NoneDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-191"><strong>NoneDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="6dccc-192">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-193">Porcentaje de la duración de la llamada sin colocación de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6dccc-193">Percentage of call duration with no frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-194"><strong>BDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-194"><strong>BDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-195">tinyint</span><span class="sxs-lookup"><span data-stu-id="6dccc-195">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-196">Porcentaje de la duración de la llamada con la caída de fotograma B.</span><span class="sxs-lookup"><span data-stu-id="6dccc-196">Percentage of call duration with B frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-197"><strong>BPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-197"><strong>BPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-198">tinyint</span><span class="sxs-lookup"><span data-stu-id="6dccc-198">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-199">Porcentaje de la duración de la llamada con fotograma de fotograma BP.</span><span class="sxs-lookup"><span data-stu-id="6dccc-199">Percentage of call duration with BP frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-200"><strong>BPSPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-200"><strong>BPSPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="6dccc-201">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-202">Porcentaje de la duración de la llamada con el fotograma BPSP.</span><span class="sxs-lookup"><span data-stu-id="6dccc-202">Percentage of call duration with BPSP frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-203"><strong>BPSPIDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-203"><strong>BPSPIDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-204">tinyint</span><span class="sxs-lookup"><span data-stu-id="6dccc-204">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-205">Porcentaje de la duración de la llamada con el fotograma BPSPI.</span><span class="sxs-lookup"><span data-stu-id="6dccc-205">Percentage of call duration with BPSPI frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-206"><strong>Entrada</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-206"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-207">bit</span><span class="sxs-lookup"><span data-stu-id="6dccc-207">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-208">Se reciben los datos de la secuencia del lado del destinatario.</span><span class="sxs-lookup"><span data-stu-id="6dccc-208">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-209"><strong>Saliente</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-209"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-210">bit</span><span class="sxs-lookup"><span data-stu-id="6dccc-210">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-211">Se reciben los datos de la secuencia en el lado del remitente.</span><span class="sxs-lookup"><span data-stu-id="6dccc-211">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-212"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-212"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-213">bit</span><span class="sxs-lookup"><span data-stu-id="6dccc-213">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6dccc-214">1 significa que la dirección de la transmisión es de la persona que llama a la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="6dccc-214">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="6dccc-215">0 significa que la dirección de la transmisión es de la persona que llama a la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="6dccc-215">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-216"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-216"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-217">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-217">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-218">Indica el porcentaje de la hora en que la llamada se encontraba en un estado de congestión de pérdida.</span><span class="sxs-lookup"><span data-stu-id="6dccc-218">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="6dccc-219">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-219">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-220"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-220"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-221">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-221">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-222">Indica el porcentaje de la llamada durante el cual la congestión fue causada por la llegada demorada de los paquetes de red.</span><span class="sxs-lookup"><span data-stu-id="6dccc-222">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="6dccc-223">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-223">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-224"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-224"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-225">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-225">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-226">Indica el porcentaje de la hora en que la llamada compite en los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="6dccc-226">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="6dccc-227">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-228"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-228"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-229">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-230">Cantidad mínima de estimación del ancho de banda medido durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="6dccc-230">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="6dccc-231">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-232"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-232"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-233">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-234">Cantidad máxima de estimación del ancho de banda medido durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="6dccc-234">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="6dccc-235">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-236"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-236"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-237">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-238">Desviación estándar de la estimación del ancho de banda medida durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="6dccc-238">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="6dccc-239">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-240"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-240"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-241">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-242">Cantidad promedio de estimación del ancho de banda medido durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="6dccc-242">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="6dccc-243">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-244"><strong>LowBandwidthForMultiview</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-244"><strong>LowBandwidthForMultiview</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-245">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-245">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-246">Porcentaje de la llamada en la que el punto de conexión determinó que la conexión de red no pudo admitir el vídeo de vista.</span><span class="sxs-lookup"><span data-stu-id="6dccc-246">Percentage of the call where the endpoint determined that the network connection could not support multiview video.</span></span></p>
<p><span data-ttu-id="6dccc-247">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-248"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-248"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-249">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-249">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-250">Cantidad total de latencia unidireccional.</span><span class="sxs-lookup"><span data-stu-id="6dccc-250">Total amount of one-way latency.</span></span> <span data-ttu-id="6dccc-251">Latencia unidireccional relativa mide el retraso entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-251">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="6dccc-252">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-253"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-253"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-254">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-255">Cantidad promedio de latencia unidireccional.</span><span class="sxs-lookup"><span data-stu-id="6dccc-255">Average amount of one-way latency.</span></span> <span data-ttu-id="6dccc-256">Latencia unidireccional relativa mide el retraso entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-256">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="6dccc-257">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-257">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-258"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-258"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-259">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-259">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-260">Cantidad máxima de latencia unidireccional.</span><span class="sxs-lookup"><span data-stu-id="6dccc-260">Maximum amount of one-way latency.</span></span> <span data-ttu-id="6dccc-261">Latencia unidireccional relativa mide el retraso entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-261">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="6dccc-262">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-262">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-263"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-263"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-264">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-264">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-265">Total de repeticiones de ráfagas unidireccionales.</span><span class="sxs-lookup"><span data-stu-id="6dccc-265">Total one-way burst occurrences.</span></span> <span data-ttu-id="6dccc-266">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="6dccc-266">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="6dccc-267">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-267">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6dccc-268">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-269"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-269"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-270">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-271">Densidad de ráfaga unidireccional total.</span><span class="sxs-lookup"><span data-stu-id="6dccc-271">Total one-way burst density.</span></span> <span data-ttu-id="6dccc-272">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="6dccc-272">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="6dccc-273">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-273">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6dccc-274">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-274">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-275"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-275"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-276">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-276">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-277">Total de duración de ráfaga unidireccional.</span><span class="sxs-lookup"><span data-stu-id="6dccc-277">Total one-way burst duration.</span></span> <span data-ttu-id="6dccc-278">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="6dccc-278">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="6dccc-279">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-279">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6dccc-280">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-281"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-281"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-282">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-282">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-283">Total de repeticiones de intervalos unidireccionales.</span><span class="sxs-lookup"><span data-stu-id="6dccc-283">Total one-way gap occurrences.</span></span> <span data-ttu-id="6dccc-284">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante; los huecos indican retrasos entre estas ráfagas.</span><span class="sxs-lookup"><span data-stu-id="6dccc-284">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="6dccc-285">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-285">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6dccc-286">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-286">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-287"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-287"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-288">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-288">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-289">Densidad de brechas en un camino total.</span><span class="sxs-lookup"><span data-stu-id="6dccc-289">Total one-way gap density.</span></span> <span data-ttu-id="6dccc-290">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante; los huecos indican retrasos entre estas ráfagas.</span><span class="sxs-lookup"><span data-stu-id="6dccc-290">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="6dccc-291">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-291">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6dccc-292">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-292">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-293"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-293"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-294">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-294">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-295">Duración del intervalo unidireccional total.</span><span class="sxs-lookup"><span data-stu-id="6dccc-295">Total one-way gap duration.</span></span> <span data-ttu-id="6dccc-296">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante; los huecos indican retrasos entre estas ráfagas.</span><span class="sxs-lookup"><span data-stu-id="6dccc-296">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="6dccc-297">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-297">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="6dccc-298">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-298">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-299"><strong>Tasa</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-299"><strong>VideoPacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-300">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="6dccc-300">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-301">Velocidad a la que se han perdido paquetes de video.</span><span class="sxs-lookup"><span data-stu-id="6dccc-301">Rate at which video packets were lost.</span></span></p>
<p><span data-ttu-id="6dccc-302">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-302">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-303"><strong>VideoAllocateBWAvg</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-303"><strong>VideoAllocateBWAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-304">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-304">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-305">Cantidad promedio de ancho de banda asignado para el vídeo.</span><span class="sxs-lookup"><span data-stu-id="6dccc-305">Average amount of bandwidth allocated for video.</span></span></p>
<p><span data-ttu-id="6dccc-306">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-306">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-307"><strong>SendCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-307"><strong>SendCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-308">smallint</span><span class="sxs-lookup"><span data-stu-id="6dccc-308">smallint</span></span></p></td>
<td><p><span data-ttu-id="6dccc-309">Extranjero</span><span class="sxs-lookup"><span data-stu-id="6dccc-309">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6dccc-310">Tipo de códecs de vídeo usados por el remitente.</span><span class="sxs-lookup"><span data-stu-id="6dccc-310">Type of video codecs used by the sender.</span></span> <span data-ttu-id="6dccc-311">Para obtener más información, consulte la <a href="lync-server-2013-codecdescription-table.md">tabla CodecDescription en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6dccc-311">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="6dccc-312">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-312">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-313"><strong>SendResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-313"><strong>SendResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-314">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-314">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-315">Ancho de resolución usado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="6dccc-315">Resolution width used by the sender.</span></span></p>
<p><span data-ttu-id="6dccc-316">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-316">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-317"><strong>SendResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-317"><strong>SendResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-318">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-318">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-319">Alto de resolución usado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="6dccc-319">Resolution height used by the sender.</span></span></p>
<p><span data-ttu-id="6dccc-320">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-321"><strong>SendFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-321"><strong>SendFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-322">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-322">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-323">Promedio de transmisión de velocidad de fotogramas de vídeo utilizada por el remitente.</span><span class="sxs-lookup"><span data-stu-id="6dccc-323">Average video frame rate transmission used by the sender.</span></span></p>
<p><span data-ttu-id="6dccc-324">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-324">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-325"><strong>SendBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-325"><strong>SendBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-326">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-327">La tasa de bits máxima para el remitente.</span><span class="sxs-lookup"><span data-stu-id="6dccc-327">Maximum bit rate for the sender.</span></span></p>
<p><span data-ttu-id="6dccc-328">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-328">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-329"><strong>SendBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-329"><strong>SendBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-330">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-330">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-331">Promedio de velocidad de bits del remitente.</span><span class="sxs-lookup"><span data-stu-id="6dccc-331">Average bit rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-332"><strong>SendVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-332"><strong>SendVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-333">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-333">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-334">Número máximo de transmisiones de vídeo usadas por el remitente.</span><span class="sxs-lookup"><span data-stu-id="6dccc-334">Maximum number of video streams used by the sender.</span></span></p>
<p><span data-ttu-id="6dccc-335">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-336"><strong>RecvCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-336"><strong>RecvCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-337">smallint</span><span class="sxs-lookup"><span data-stu-id="6dccc-337">smallint</span></span></p></td>
<td><p><span data-ttu-id="6dccc-338">Extranjero</span><span class="sxs-lookup"><span data-stu-id="6dccc-338">Foreign</span></span></p></td>
<td><p><span data-ttu-id="6dccc-339">Códigos de vídeo usados por el destinatario.</span><span class="sxs-lookup"><span data-stu-id="6dccc-339">Video codes used by the receiver.</span></span> <span data-ttu-id="6dccc-340">Para obtener más información, consulte la <a href="lync-server-2013-codecdescription-table.md">tabla CodecDescription en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6dccc-340">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="6dccc-341">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-342"><strong>RecvResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-342"><strong>RecvResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-343">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-343">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-344">Ancho de resolución usado por el receptor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-344">Resolution width used by the receiver.</span></span></p>
<p><span data-ttu-id="6dccc-345">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-345">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-346"><strong>RecvResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-346"><strong>RecvResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-347">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-347">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-348">Alto de resolución usado por el receptor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-348">Resolution height used by the receiver.</span></span></p>
<p><span data-ttu-id="6dccc-349">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-349">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-350"><strong>Media</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-350"><strong>RecvFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-351">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-351">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-352">Promedio de velocidad de fotogramas de video usada por el receptor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-352">Average video frame rate used by the receiver.</span></span></p>
<p><span data-ttu-id="6dccc-353">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-353">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-354"><strong>RecvBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-354"><strong>RecvBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-355">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-355">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-356">La velocidad de bits máxima para el receptor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-356">Maximum bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="6dccc-357">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-357">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-358"><strong>RecvBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-358"><strong>RecvBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-359">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-359">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-360">Promedio de velocidad de bits para el receptor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-360">Average bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="6dccc-361">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-361">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-362"><strong>RecvVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-362"><strong>RecvVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-363">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-363">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-364">Máximo de transmisiones de vídeo para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="6dccc-364">Maximum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="6dccc-365">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-365">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-366"><strong>RecvVideoStreamsMin</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-366"><strong>RecvVideoStreamsMin</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-367">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-367">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-368">Las transmisiones de video mínimas para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="6dccc-368">Minimum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="6dccc-369">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-369">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-370"><strong>RecvVideoStreamsMode</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-370"><strong>RecvVideoStreamsMode</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-371">int</span><span class="sxs-lookup"><span data-stu-id="6dccc-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-372">Modo de vídeo (por ejemplo, Galería o un único flujo) para el receptor.</span><span class="sxs-lookup"><span data-stu-id="6dccc-372">Video mode (for example, gallery or single stream) for the receiver.</span></span></p>
<p><span data-ttu-id="6dccc-373">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-373">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-374"><strong>Tasa</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-374"><strong>VideoPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-375">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-375">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-376">Tasa de pérdida de paquetes después de aplicar la corrección de errores de reenvío.</span><span class="sxs-lookup"><span data-stu-id="6dccc-376">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="6dccc-377">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-377">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-378"><strong>Porcentaje</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-378"><strong>DynamicCapabilityPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-379">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-379">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-380">Porcentaje de tiempo que el indicador de capacidad dinámica estaba activo.</span><span class="sxs-lookup"><span data-stu-id="6dccc-380">Percentage of time that the dynamic capability flag was active.</span></span></p>
<p><span data-ttu-id="6dccc-381">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-381">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-382"><strong>ResolutionMin</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-382"><strong>ResolutionMin</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-383">carácter (9)</span><span class="sxs-lookup"><span data-stu-id="6dccc-383">char(9)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-384">Resolución mínima medida durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="6dccc-384">Minimum resolution measured during the call.</span></span></p>
<p><span data-ttu-id="6dccc-385">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-385">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-386"><strong>LowBitRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-386"><strong>LowBitRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-387">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-387">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-388">Porcentaje de la llamada por debajo del umbral de baja velocidad de bits (70 kilobits por segundo).</span><span class="sxs-lookup"><span data-stu-id="6dccc-388">Percentage of the call below the low bit rate threshold (70 kilobits per second).</span></span></p>
<p><span data-ttu-id="6dccc-389">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-389">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-390"><strong>Porcentaje</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-390"><strong>LowFrameRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-391">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-391">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-392">Porcentaje de la llamada por debajo del umbral de baja velocidad de fotogramas (7,5 fotogramas por segundo, entrada).</span><span class="sxs-lookup"><span data-stu-id="6dccc-392">Percentage of the call below the low frame rate threshold (7.5 frames per second, inbound).</span></span></p>
<p><span data-ttu-id="6dccc-393">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-393">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-394"><strong>Porcentaje</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-394"><strong>LowResolutionCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-395">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-396">Porcentaje de la llamada que se produjo en la resolución más baja.</span><span class="sxs-lookup"><span data-stu-id="6dccc-396">Percentage of the call that occurred at the lowest resolution.</span></span></p>
<p><span data-ttu-id="6dccc-397">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-397">This column was introduced in Microsoft Lync Server 2013.</span></span></p>
<p><span data-ttu-id="6dccc-398">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-398">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dccc-399"><strong>DurationSeconds</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-399"><strong>DurationSeconds</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-400">float</span><span class="sxs-lookup"><span data-stu-id="6dccc-400">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-401">Duración de la llamada en segundos.</span><span class="sxs-lookup"><span data-stu-id="6dccc-401">Length of the call in seconds.</span></span></p>
<p><span data-ttu-id="6dccc-402">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-402">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dccc-403"><strong>IsAggregatedData</strong></span><span class="sxs-lookup"><span data-stu-id="6dccc-403"><strong>IsAggregatedData</strong></span></span></p></td>
<td><p><span data-ttu-id="6dccc-404">bit</span><span class="sxs-lookup"><span data-stu-id="6dccc-404">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6dccc-405">Indica si los datos se han agregado desde varias llamadas.</span><span class="sxs-lookup"><span data-stu-id="6dccc-405">Indicates whether the data has been aggregated from multiple calls.</span></span></p>
<p><span data-ttu-id="6dccc-406">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dccc-406">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6dccc-407">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6dccc-407">


</div>

<span> </span>

</div>

</div>

</span></span></div>

