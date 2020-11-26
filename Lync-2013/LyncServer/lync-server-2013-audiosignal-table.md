---
title: 'Lync Server 2013: Tabla AudioSignal'
description: 'Lync Server 2013: tabla AudioSignal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioSignal table
ms:assetid: 0013c8c6-cdf9-4d70-bc2a-cddd1560f66b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398064(v=OCS.15)
ms:contentKeyID: 48183217
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82f3b3119eaccfe56c4706cff07469bc3434461f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438213"
---
# <a name="audiosignal-table-in-lync-server-2013"></a><span data-ttu-id="afd0b-103">Tabla AudioSignal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="afd0b-103">AudioSignal table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="afd0b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="afd0b-104">

<span> </span></span></span>

<span data-ttu-id="afd0b-105">_**Última modificación del tema:** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="afd0b-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="afd0b-106">Cada registro representa las métricas de señal de audio de un extremo.</span><span class="sxs-lookup"><span data-stu-id="afd0b-106">Each record represents audio signal metrics for one endpoint.</span></span> <span data-ttu-id="afd0b-107">Normalmente, cada llamada tiene dos registros, uno para la persona que llama y el otro es para el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="afd0b-107">Usually, each call has two records, one is for caller, and one is for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="afd0b-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="afd0b-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="afd0b-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="afd0b-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-113">datetime</span><span class="sxs-lookup"><span data-stu-id="afd0b-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="afd0b-114">Primary</span><span class="sxs-lookup"><span data-stu-id="afd0b-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="afd0b-115">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="afd0b-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-117">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-117">int</span></span></p></td>
<td><p><span data-ttu-id="afd0b-118">Primary</span><span class="sxs-lookup"><span data-stu-id="afd0b-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="afd0b-119">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="afd0b-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="afd0b-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="afd0b-122">Primary</span><span class="sxs-lookup"><span data-stu-id="afd0b-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="afd0b-123">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="afd0b-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-125">bit</span><span class="sxs-lookup"><span data-stu-id="afd0b-125">bit</span></span></p></td>
<td><p><span data-ttu-id="afd0b-126">Primary</span><span class="sxs-lookup"><span data-stu-id="afd0b-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="afd0b-127">0: datos del destinatario de la llamada</span><span class="sxs-lookup"><span data-stu-id="afd0b-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="afd0b-128">1: datos del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="afd0b-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-129"><strong>SendSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-129"><strong>SendSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-130">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-130">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-131">Representa el nivel de señal de audio de control de ganancia posterior analógico.</span><span class="sxs-lookup"><span data-stu-id="afd0b-131">Represents the Post-Analog Gain Control audio signal level.</span></span> <span data-ttu-id="afd0b-132">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="afd0b-132">The unit for this metric is dBmo.</span></span> <span data-ttu-id="afd0b-133">Para obtener una calidad aceptable, debe tener al menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="afd0b-133">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="afd0b-134">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="afd0b-134">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-135"><strong>RecvSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-135"><strong>RecvSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-136">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-136">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-137">Consulta SendSignalLevel.</span><span class="sxs-lookup"><span data-stu-id="afd0b-137">See SendSignalLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-138"><strong>SendNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-138"><strong>SendNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-139">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-139">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-140">Representa el nivel de ruido de audio del control de ganancia posterior analógico.</span><span class="sxs-lookup"><span data-stu-id="afd0b-140">Represents the Post-Analog Gain Control audio noise level.</span></span> <span data-ttu-id="afd0b-141">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="afd0b-141">The unit for this metric is dBmo.</span></span> <span data-ttu-id="afd0b-142">Para obtener una calidad aceptable, debe ser menor que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="afd0b-142">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="afd0b-143">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="afd0b-143">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-144"><strong>RecvNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-144"><strong>RecvNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-145">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-145">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-146">Consulta SendNoiseLevel.</span><span class="sxs-lookup"><span data-stu-id="afd0b-146">See SendNoiseLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-147"><strong>EchoReturn</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-147"><strong>EchoReturn</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-148">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-148">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-149">Métrica de mejora de pérdida de eco.</span><span class="sxs-lookup"><span data-stu-id="afd0b-149">Echo Return Loss Enhancement metric.</span></span> <span data-ttu-id="afd0b-150">La unidad para esta métrica es dB.</span><span class="sxs-lookup"><span data-stu-id="afd0b-150">The unit for this metric is dB.</span></span> <span data-ttu-id="afd0b-151">Los valores más bajos representan menos eco.</span><span class="sxs-lookup"><span data-stu-id="afd0b-151">Lower values represent less echo.</span></span> <span data-ttu-id="afd0b-152">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="afd0b-152">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-153"><strong>AudioSpeakerGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-153"><strong>AudioSpeakerGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-154">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-154">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-155">Promedio de problemas por cinco minutos para el procesamiento de altavoz.</span><span class="sxs-lookup"><span data-stu-id="afd0b-155">Average glitches per five minutes for the loudspeaker rendering.</span></span> <span data-ttu-id="afd0b-156">Para obtener una buena calidad, debe ser inferior a un período de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="afd0b-156">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="afd0b-157">No se han notificado por servidores de conferencia A/V, servidores de mediación o teléfonos IP.</span><span class="sxs-lookup"><span data-stu-id="afd0b-157">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-158"><strong>AudioMicGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-158"><strong>AudioMicGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-159">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-159">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-160">Promedio de problemas por cinco minutos para la captura del micrófono.</span><span class="sxs-lookup"><span data-stu-id="afd0b-160">Average glitches per five minutes for the microphone capture.</span></span> <span data-ttu-id="afd0b-161">Para obtener una buena calidad, debe ser inferior a uno por cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="afd0b-161">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="afd0b-162">No se han notificado por servidores de conferencia A/V, servidores de mediación o teléfonos IP.</span><span class="sxs-lookup"><span data-stu-id="afd0b-162">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-163"><strong>AudioTimestampDriftRateMic</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-163"><strong>AudioTimestampDriftRateMic</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-164">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="afd0b-164">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-165">Velocidad de desplazamiento del reloj del dispositivo de micrófono, relativa al reloj de la CPU.</span><span class="sxs-lookup"><span data-stu-id="afd0b-165">Microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-166"><strong>AudioTimestampDriftRateSpk</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-166"><strong>AudioTimestampDriftRateSpk</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-167">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="afd0b-167">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-168">Velocidad de desplazamiento del reloj del dispositivo de altavoz, relativa al reloj de la CPU.</span><span class="sxs-lookup"><span data-stu-id="afd0b-168">Speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-169"><strong>AudioTimestampErrorMicMs</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-169"><strong>AudioTimestampErrorMicMs</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-170">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="afd0b-170">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-171">Velocidad de desplazamiento del reloj del dispositivo de altavoz, relativa al reloj de la CPU.</span><span class="sxs-lookup"><span data-stu-id="afd0b-171">Speaker device clock drift rate, relative to CPU clock.</span></span></p>
<p><span data-ttu-id="afd0b-172">Error de marca de tiempo de captura de micrófono promedio, en milisegundos, en los últimos 20 segundos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="afd0b-172">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-173"><strong>AudioTimestampErrorSpkMs</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-173"><strong>AudioTimestampErrorSpkMs</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-174">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="afd0b-174">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-175">El altavoz promedio representa el error de marca de tiempo de la secuencia, en milisegundos, en los últimos 20 segundos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="afd0b-175">Average speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-176"><strong>VsEntryCauses</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-176"><strong>VsEntryCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-177">smallint</span><span class="sxs-lookup"><span data-stu-id="afd0b-177">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-178">El cambio de voz es un modo de dúplex medio con una capacidad de interrupción reducida.</span><span class="sxs-lookup"><span data-stu-id="afd0b-178">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="afd0b-179">Causas de la entrada de conmutación de voz:</span><span class="sxs-lookup"><span data-stu-id="afd0b-179">Causes of voice switch entry:</span></span></p>
<p><span data-ttu-id="afd0b-180">ENTER_VS_BADTS 0x01</span><span class="sxs-lookup"><span data-stu-id="afd0b-180">ENTER_VS_BADTS 0x01</span></span></p>
<p><span data-ttu-id="afd0b-181">ENTER_VS_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="afd0b-181">ENTER_VS_ECHO 0x02</span></span></p>
<p><span data-ttu-id="afd0b-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span><span class="sxs-lookup"><span data-stu-id="afd0b-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span></span></p>
<p><span data-ttu-id="afd0b-183">ENTER_VS_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="afd0b-183">ENTER_VS_DNLP 0x08</span></span></p>
<p><span data-ttu-id="afd0b-184">La causa puede ser una combinación de estas causas individuales.</span><span class="sxs-lookup"><span data-stu-id="afd0b-184">The cause can be a combination of those individual causes.</span></span> <span data-ttu-id="afd0b-185">RegKey solo puede habilitar ENTER_VS_FORCEORCONVERGENCE para fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="afd0b-185">ENTER_VS_FORCEORCONVERGENCE can only be enabled by regkey for test purpose.</span></span></p>
<p><span data-ttu-id="afd0b-186">El tipo de datos de esta columna se modificó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afd0b-186">The data type for this column was changed in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-187"><strong>EchoEventCauses</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-187"><strong>EchoEventCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-188">tinyint</span><span class="sxs-lookup"><span data-stu-id="afd0b-188">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-189">Causas de un evento de eco:</span><span class="sxs-lookup"><span data-stu-id="afd0b-189">Causes of an echo event:</span></span></p>
<p><span data-ttu-id="afd0b-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span><span class="sxs-lookup"><span data-stu-id="afd0b-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span></span></p>
<p><span data-ttu-id="afd0b-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="afd0b-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span></span></p>
<p><span data-ttu-id="afd0b-192">ECHO_EVENT_ANLP 0x04</span><span class="sxs-lookup"><span data-stu-id="afd0b-192">ECHO_EVENT_ANLP 0x04</span></span></p>
<p><span data-ttu-id="afd0b-193">ECHO_EVENT_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="afd0b-193">ECHO_EVENT_DNLP 0x08</span></span></p>
<p><span data-ttu-id="afd0b-194">ECHO_EVENT_MIC_CLIPPING 0x10</span><span class="sxs-lookup"><span data-stu-id="afd0b-194">ECHO_EVENT_MIC_CLIPPING 0x10</span></span></p>
<p><span data-ttu-id="afd0b-195">ECHO_EVENT_BAD_STATE 0x20</span><span class="sxs-lookup"><span data-stu-id="afd0b-195">ECHO_EVENT_BAD_STATE 0x20</span></span></p>
<p><span data-ttu-id="afd0b-196">La causa puede ser una combinación de estas causas individuales.</span><span class="sxs-lookup"><span data-stu-id="afd0b-196">The cause can be a combination of those individual causes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-197"><strong>EchoPercentMicIn</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-197"><strong>EchoPercentMicIn</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-198">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="afd0b-198">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-p109">Porcentaje de tiempo para la detección del eco en la secuencia de captura del micrófono. En general, los valores son bajos para auriculares, y altos para altavoces de teléfono o independientes. En el caso de dispositivos que son compatibles con la cancelación del eco acústico incorporada, los valores altos indican filtraciones de eco. En otros dispositivos, esta métrica no debe utilizarse para evaluar la calidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="afd0b-p109">Percentage of time when echo was detected in the microphone capture stream. Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers. For devices that support on-board acoustic echo cancellation, high values indicate echo leak. For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-203"><strong>EchoPercentSend</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-203"><strong>EchoPercentSend</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-204">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="afd0b-204">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="afd0b-205">Porcentaje de tiempo durante el que se detecta eco en el flujo enviado.</span><span class="sxs-lookup"><span data-stu-id="afd0b-205">Percentage of time when echo is detected in sent stream.</span></span> <span data-ttu-id="afd0b-206">Porcentaje de eco alto en secuencias de envío indica una pérdida de eco.</span><span class="sxs-lookup"><span data-stu-id="afd0b-206">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-207"><strong>RxAGCSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-207"><strong>RxAGCSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-208">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-208">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-209">Nivel de señal recibido en el servidor de mediación de la puerta de enlace; Esto solo se aplica al servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="afd0b-209">Received signal level on the Mediation Server from the Gateway; this applies only to the Mediation Server.</span></span> <span data-ttu-id="afd0b-210">La unidad de esta métrica es dBoV.</span><span class="sxs-lookup"><span data-stu-id="afd0b-210">The unit of this metric is dBoV.</span></span> <span data-ttu-id="afd0b-211">Para obtener una buena calidad, el rango aceptable debe ser [-30 a-18] dBoV.</span><span class="sxs-lookup"><span data-stu-id="afd0b-211">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-212"><strong>RxAGCNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-212"><strong>RxAGCNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-213">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-213">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-214">Nivel de señal recibido en el servidor de mediación de la puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="afd0b-214">Received signal level on the Mediation Server from the Gateway.</span></span> <span data-ttu-id="afd0b-215">Esto solo se aplica al servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="afd0b-215">This applies only to the Mediation Server.</span></span> <span data-ttu-id="afd0b-216">La unidad de esta métrica es dBoV.</span><span class="sxs-lookup"><span data-stu-id="afd0b-216">The unit of this metric is dBoV.</span></span> <span data-ttu-id="afd0b-217">Para obtener una buena calidad, el rango aceptable debe ser menor que-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="afd0b-217">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-218"><strong>RxAvgAGCGain</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-218"><strong>RxAvgAGCGain</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-219">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-219">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-220">Control automático de ganancia (AGC) en el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="afd0b-220">Automatic gain control (AGC) on the Mediation Server side.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-221"><strong>InitialSignalLevelRMS</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-221"><strong>InitialSignalLevelRMS</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-222">float</span><span class="sxs-lookup"><span data-stu-id="afd0b-222">float</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="afd0b-223">El cuadrado de la media raíz (RMS) de la señal entrante de hasta los primeros 30 segundos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="afd0b-223">The root mean square (RMS) of the incoming signal of up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-224"><strong>RecvSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-224"><strong>RecvSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-225">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-225">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="afd0b-226">Nivel de señal como recibido en el canal 1.</span><span class="sxs-lookup"><span data-stu-id="afd0b-226">Signal level as received on channel 1.</span></span></p>
<p><span data-ttu-id="afd0b-227">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afd0b-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-228"><strong>RecvSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-228"><strong>RecvSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-229">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="afd0b-230">Nivel de señal como recibido en el canal 2.</span><span class="sxs-lookup"><span data-stu-id="afd0b-230">Signal level as received on channel 2.</span></span></p>
<p><span data-ttu-id="afd0b-231">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afd0b-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-232"><strong>RecvNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-232"><strong>RecvNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-233">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="afd0b-234">Nivel de ruido recibido en el canal 1.</span><span class="sxs-lookup"><span data-stu-id="afd0b-234">Noise level as received on channel 1.</span></span></p>
<p><span data-ttu-id="afd0b-235">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afd0b-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-236"><strong>RecvNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-236"><strong>RecvNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-237">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="afd0b-238">Nivel de ruido recibido en el canal 2.</span><span class="sxs-lookup"><span data-stu-id="afd0b-238">Noise level as received on channel 2.</span></span></p>
<p><span data-ttu-id="afd0b-239">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afd0b-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-240"><strong>SendSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-240"><strong>SendSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-241">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="afd0b-242">Nivel de señal enviado en el canal 1.</span><span class="sxs-lookup"><span data-stu-id="afd0b-242">Signal level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="afd0b-243">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afd0b-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-244"><strong>SendSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-244"><strong>SendSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-245">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-245">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="afd0b-246">Nivel de señal enviado en el canal 2.</span><span class="sxs-lookup"><span data-stu-id="afd0b-246">Signal level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="afd0b-247">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afd0b-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afd0b-248"><strong>SendNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-248"><strong>SendNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-249">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-249">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="afd0b-250">Nivel de ruido enviado en el canal 1.</span><span class="sxs-lookup"><span data-stu-id="afd0b-250">Noise level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="afd0b-251">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afd0b-251">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afd0b-252"><strong>SendNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="afd0b-252"><strong>SendNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="afd0b-253">int</span><span class="sxs-lookup"><span data-stu-id="afd0b-253">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="afd0b-254">Nivel de ruido enviado en el canal 2.</span><span class="sxs-lookup"><span data-stu-id="afd0b-254">Noise level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="afd0b-255">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afd0b-255">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="afd0b-256">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="afd0b-256">


</div>

<span> </span>

</div>

</div>

</span></span></div>

