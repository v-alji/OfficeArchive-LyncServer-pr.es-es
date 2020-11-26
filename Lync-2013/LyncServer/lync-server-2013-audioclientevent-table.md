---
title: 'Lync Server 2013: Tabla AudioClientEvent'
description: 'Lync Server 2013: tabla AudioClientEvent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioClientEvent table
ms:assetid: fef73d8f-7261-4e5b-9769-82435b007979
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413086(v=OCS.15)
ms:contentKeyID: 48185967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2200cd9567bdd10ac4ad8f5c269062c2f5614dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438214"
---
# <a name="audioclientevent-table-in-lync-server-2013"></a><span data-ttu-id="7c08f-103">Tabla AudioClientEvent en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c08f-103">AudioClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7c08f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7c08f-104">

<span> </span></span></span>

<span data-ttu-id="7c08f-105">_**Última modificación del tema:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="7c08f-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="7c08f-106">Cada registro contiene un evento de cliente para un punto final en una llamada de audio.</span><span class="sxs-lookup"><span data-stu-id="7c08f-106">Each record contains a client event for one endpoint in an audio call.</span></span> <span data-ttu-id="7c08f-107">Generalmente, una llamada tiene dos registros: uno para el autor de la llamada y otro para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="7c08f-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c08f-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="7c08f-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="7c08f-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="7c08f-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-113">datetime</span><span class="sxs-lookup"><span data-stu-id="7c08f-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="7c08f-114">Primary</span><span class="sxs-lookup"><span data-stu-id="7c08f-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="7c08f-115">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7c08f-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-117">int</span><span class="sxs-lookup"><span data-stu-id="7c08f-117">int</span></span></p></td>
<td><p><span data-ttu-id="7c08f-118">Primary</span><span class="sxs-lookup"><span data-stu-id="7c08f-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="7c08f-119">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7c08f-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="7c08f-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7c08f-122">Primary</span><span class="sxs-lookup"><span data-stu-id="7c08f-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="7c08f-123">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7c08f-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-125">bit</span><span class="sxs-lookup"><span data-stu-id="7c08f-125">bit</span></span></p></td>
<td><p><span data-ttu-id="7c08f-126">Primary</span><span class="sxs-lookup"><span data-stu-id="7c08f-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="7c08f-127">0: datos del destinatario de la llamada</span><span class="sxs-lookup"><span data-stu-id="7c08f-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="7c08f-128">1: datos del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="7c08f-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-129"><strong>NetworkSendQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-129"><strong>NetworkSendQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-130">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-130">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-131">Porcentaje de sesión el evento NetworkSendQuality se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-131">Percentage of session the NetworkSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="7c08f-132">La calidad de la red en términos de vibración o pérdida de paquetes es grave y afecta a la calidad del audio que se envía.</span><span class="sxs-lookup"><span data-stu-id="7c08f-132">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-133"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-133"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-134">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-134">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-135">Porcentaje de sesión el evento ReceiveSendQuality se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-135">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="7c08f-136">La calidad de la red en términos de vibración o pérdida de paquetes es grave y afecta la calidad de audio que se recibe.</span><span class="sxs-lookup"><span data-stu-id="7c08f-136">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-137"><strong>NetworkDelayEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-137"><strong>NetworkDelayEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-138">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-138">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-139">Porcentaje de la sesión el evento de retraso se activó para el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-139">Percentage of session the Delay event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-140">La latencia de la red es grave y afecta a la experiencia al evitar la comunicación interactiva</span><span class="sxs-lookup"><span data-stu-id="7c08f-140">Network latency is severe and impacting the experience by preventing interactive communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-141"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-141"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-142">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-142">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-143">Porcentaje de sesión el evento LowBandwidth se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-143">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-144">El ancho de banda disponible es insuficiente para una experiencia de voz aceptable.</span><span class="sxs-lookup"><span data-stu-id="7c08f-144">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-145"><strong>CPUInsufficientEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-145"><strong>CPUInsufficientEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-146">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-146">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-147">Porcentaje de sesión el evento de CPU insuficiente se activó para el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-147">Percentage of session the insufficient CPU event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-148">No hay suficientes ciclos de CPU para procesar con las aplicaciones y las aplicaciones actuales en uso.</span><span class="sxs-lookup"><span data-stu-id="7c08f-148">There are insufficient CPU cycles for processing with the current modalities and applications in use.</span></span> <span data-ttu-id="7c08f-149">Esto causa distorsiones en el canal de audio.</span><span class="sxs-lookup"><span data-stu-id="7c08f-149">This causes distortions with the audio channel.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-151">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-151">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-152">Porcentaje de sesión el evento DeviceHalfDuplexAEC se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-152">Percentage of session the DeviceHalfDuplexAEC event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-153">Para evitar que se produzca el eco, el sistema se introduce a doble cara.</span><span class="sxs-lookup"><span data-stu-id="7c08f-153">In order to prevent echo, the system has enter half duplex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-155">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-155">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-156">Porcentaje de sesión el evento DeviceRenderNotFunctioning se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-156">Percentage of session the DeviceRenderNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-157">El dispositivo de representación que se usa actualmente para la sesión no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c08f-157">The render device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="7c08f-158">Esto puede dar lugar a problemas de audio unidireccionales.</span><span class="sxs-lookup"><span data-stu-id="7c08f-158">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-160">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-160">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-161">Porcentaje de sesión el evento DeviceCaptureNotFunctioning se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-161">Percentage of session the DeviceCaptureNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-162">El dispositivo de captura usado actualmente para la sesión no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c08f-162">The capture device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="7c08f-163">Esto puede dar lugar a problemas de audio unidireccionales.</span><span class="sxs-lookup"><span data-stu-id="7c08f-163">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-164"><strong>DeviceGlitchesEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-164"><strong>DeviceGlitchesEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-165">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-165">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-166">Porcentaje de sesión el evento DeviceGlitches se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-166">Percentage of session the DeviceGlitches event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-167">Hay problemas graves en la representación de audio que causan distorsiones.</span><span class="sxs-lookup"><span data-stu-id="7c08f-167">There are severe glitches in the rendering of audio which is causing distortions.</span></span> <span data-ttu-id="7c08f-168">Estos problemas pueden estar causados por problemas de controlador, tormentas de llamadas a procedimiento diferidas (DPC) y uso intensivo de la CPU.</span><span class="sxs-lookup"><span data-stu-id="7c08f-168">These glitches can be caused by driver issues, deferred procedure calls (DPC) storm (drivers), and high CPU usage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-169"><strong>DeviceLowSNREventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-169"><strong>DeviceLowSNREventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-170">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-170">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-171">Porcentaje de sesión el evento DeviceLowSNR se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-171">Percentage of session the DeviceLowSNR event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-172">La calidad de la captura es muy mala, ya sea muy ruidosa o el usuario habla demasiado lejos del micrófono.</span><span class="sxs-lookup"><span data-stu-id="7c08f-172">The capture quality is very poor, either very noisy or user is talking too far away from the microphone.</span></span> <span data-ttu-id="7c08f-173">Esto provocará distorsiones.</span><span class="sxs-lookup"><span data-stu-id="7c08f-173">This will cause distortions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-175">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-175">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-176">Porcentaje de sesión el evento DeviceLowSpeechLevel se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-176">Percentage of session the DeviceLowSpeechLevel event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-177">El nivel de voz del usuario es demasiado bajo y el sistema no puede aumentarlo.</span><span class="sxs-lookup"><span data-stu-id="7c08f-177">User‘s speech level is too low and the system cannot increase it any further.</span></span> <span data-ttu-id="7c08f-178">Esto puede causar distorsiones o percibir como audio unidireccional.</span><span class="sxs-lookup"><span data-stu-id="7c08f-178">This can either cause distortions or perceived as one-way audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-179"><strong>DeviceClippingEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-179"><strong>DeviceClippingEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-180">Decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-180">Decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-181">Porcentaje de sesión el evento DeviceClipping se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-181">Percentage of session the DeviceClipping event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="7c08f-182">Cuando los recortes de voz próximos se recortan, el micrófono escucha la distorsión del extremo a causa de la recorte.</span><span class="sxs-lookup"><span data-stu-id="7c08f-182">When near-end speech clips the microphone, far-end hears distortion due to clipping.</span></span> <span data-ttu-id="7c08f-183">Es importante evitar el recorte de micrófono cerca de la final.</span><span class="sxs-lookup"><span data-stu-id="7c08f-183">It is important to avoid near-end microphone clipping.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-184"><strong>DeviceEchoEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-184"><strong>DeviceEchoEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-185">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-185">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-186">Porcentaje de sesión el evento DeviceEchoEvent se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-186">Percentage of session the DeviceEchoEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-187">El dispositivo o el programa de instalación está causando eco más allá de la capacidad del sistema para compensar.</span><span class="sxs-lookup"><span data-stu-id="7c08f-187">Device or setup is causing echo beyond the ability of the system to compensate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-189">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-189">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-190">Porcentaje de sesión el evento DeviceNearEndToEchoRatio se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-190">Percentage of session the DeviceNearEndToEchoRatio event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-191">La voz del usuario es demasiado baja en comparación con el eco que se está capturando y que afecta a la experiencia de los usuarios porque limita lo fácil que es interrumpir a un usuario.</span><span class="sxs-lookup"><span data-stu-id="7c08f-191">The user’s speech is too low compared to the echo being captured which impacts the users experience because it limits how easy it is to interrupt a user.</span></span> <span data-ttu-id="7c08f-192">Reduce el volumen del altavoz, mueve el micrófono cerca de la Talker.</span><span class="sxs-lookup"><span data-stu-id="7c08f-192">Reduce speaker volume, move the microphone closer to the talker.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-193"><strong>DeviceMultipleEndpointsEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-193"><strong>DeviceMultipleEndpointsEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-194">int</span><span class="sxs-lookup"><span data-stu-id="7c08f-194">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7c08f-195">Número de veces durante la sesión el evento DeviceMultipleEndpoints se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-195">Number of times during session the DeviceMultipleEndpoints event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-196">Se detectaron varios puntos de conexión de audio en la misma sesión y el sistema se ha compensado al reducir el volumen de representación.</span><span class="sxs-lookup"><span data-stu-id="7c08f-196">Multiple audio endpoints in the same session detected and the system has compensated by reducing render volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-197"><strong>DeviceHowlingEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-197"><strong>DeviceHowlingEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-198">int</span><span class="sxs-lookup"><span data-stu-id="7c08f-198">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7c08f-199">Número de veces durante la sesión el evento DeviceHowlingEvent se activó por el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-199">Number of times during session the DeviceHowlingEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="7c08f-200">Se detectó un bucle de comentarios de audio (causado por varios puntos de conexión que comparten la ruta de audio).</span><span class="sxs-lookup"><span data-stu-id="7c08f-200">Audio feedback loop detected (caused by multiple endpoints sharing audio path).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c08f-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-202">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-202">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7c08f-203">Porcentaje de sesión el evento DeviceRenderZeroVolume se activó por estar en el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-203">Percentage of session the DeviceRenderZeroVolume event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="7c08f-204">El dispositivo de representación se estableció en un volumen de cero.</span><span class="sxs-lookup"><span data-stu-id="7c08f-204">The render device was set to zero volume.</span></span></p>
<p><span data-ttu-id="7c08f-205">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7c08f-205">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c08f-206"><strong>DeviceRenderMuteEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="7c08f-206"><strong>DeviceRenderMuteEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="7c08f-207">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="7c08f-207">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7c08f-208">Porcentaje de sesión el evento DeviceRenderMute se activó por estar en el estado "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="7c08f-208">Percentage of session the DeviceRenderMute event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="7c08f-209">El dispositivo de representación se ha silenciado.</span><span class="sxs-lookup"><span data-stu-id="7c08f-209">The render device was muted.</span></span></p>
<p><span data-ttu-id="7c08f-210">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7c08f-210">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7c08f-211">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7c08f-211">


</div>

<span> </span>

</div>

</div>

</span></span></div>

