---
title: 'Lync Server 2013: vista AudioStreamDetail'
description: 'Lync Server 2013: vista AudioStreamDetail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStreamDetail view
ms:assetid: b6a435b3-103c-41c4-96ed-33c3784534c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721859(v=OCS.15)
ms:contentKeyID: 49733792
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92c4c9bbb4f126e242e28d835222f6ba2af89d8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438165"
---
# <a name="audiostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="b1dd4-103">Vista AudioStreamDetail en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1dd4-103">AudioStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1dd4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1dd4-104">

<span> </span></span></span>

<span data-ttu-id="b1dd4-105">_**Última modificación del tema:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="b1dd4-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="b1dd4-106">La vista AudioStreamDetail almacena información acerca de cada secuencia de audio de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-106">The AudioStreamDetail View stores information about each audio stream in the database.</span></span> <span data-ttu-id="b1dd4-107">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1dd4-108">Columna</span><span class="sxs-lookup"><span data-stu-id="b1dd4-108">Column</span></span></th>
<th><span data-ttu-id="b1dd4-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b1dd4-109">Data Type</span></span></th>
<th><span data-ttu-id="b1dd4-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="b1dd4-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="b1dd4-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-112">datetime</span><span class="sxs-lookup"><span data-stu-id="b1dd4-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-113">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="b1dd4-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-115">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-115">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-116">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-117">StreamId</span><span class="sxs-lookup"><span data-stu-id="b1dd4-117">StreamId</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-118">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-118">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-119">IDENTIFICADOR exclusivo dentro de una línea de medios.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-119">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-120">StartTime</span><span class="sxs-lookup"><span data-stu-id="b1dd4-120">StartTime</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-121">datetime</span><span class="sxs-lookup"><span data-stu-id="b1dd4-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-122">Hora de inicio de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-122">Start time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-123">EndTime</span><span class="sxs-lookup"><span data-stu-id="b1dd4-123">EndTime</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-124">datetime</span><span class="sxs-lookup"><span data-stu-id="b1dd4-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-125">Hora de finalización de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-125">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-126">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="b1dd4-126">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-127">bit</span><span class="sxs-lookup"><span data-stu-id="b1dd4-127">bit</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-128">Categoría de cuadro de diálogo: 0 es el servidor de Lync para el servidor de mediación; 1 es el servidor de mediación para la puerta de la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-128">Dialog category: 0 is the Lync Server to Mediation Server leg; 1 is the Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-129">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="b1dd4-129">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-130">bit</span><span class="sxs-lookup"><span data-stu-id="b1dd4-130">bit</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-131">Marcador que indica si la llamada se ha omitido o no.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-131">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-132">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="b1dd4-132">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-133">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-133">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-134">Si está presente, indica por qué no se omitió una llamada aunque los identificadores de omisión coincidan.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-134">If present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="b1dd4-135">Solo se define un valor:</span><span class="sxs-lookup"><span data-stu-id="b1dd4-135">Only one value is defined:</span></span></p>
<p><span data-ttu-id="b1dd4-136">0x0001: identificador de omisión desconocido para el adaptador de red predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-136">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-137">CallPriority</span><span class="sxs-lookup"><span data-stu-id="b1dd4-137">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-138">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-138">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-139">Prioridad de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-139">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-140">CallerPool</span><span class="sxs-lookup"><span data-stu-id="b1dd4-140">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-142">FQDN del grupo de llamadas.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-142">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-143">CalleePool</span><span class="sxs-lookup"><span data-stu-id="b1dd4-143">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-144">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-144">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-145">FQDN del grupo de destinatarios de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-145">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-146">Autor de llamada</span><span class="sxs-lookup"><span data-stu-id="b1dd4-146">Caller</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-148">URI de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-148">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-149">Destinatario de la llamada</span><span class="sxs-lookup"><span data-stu-id="b1dd4-149">Callee</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-150">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-150">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-151">URI de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-151">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-152">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="b1dd4-152">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-154">Cadena de agente de usuario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-154">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-155">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="b1dd4-155">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-156">smallint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-156">smallint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-157">Tipo del agente de usuario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-157">Type of the caller’s user agent.</span></span> <span data-ttu-id="b1dd4-158">Para obtener más información, vea la <a href="lync-server-2013-useragent-table.md">tabla UserAgent en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-158">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-159">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="b1dd4-159">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-160">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-160">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-161">Categoría del agente de usuario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-161">Category of the caller’s user agent.</span></span> <span data-ttu-id="b1dd4-162">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table-qoe.md">tabla UserAgentDef (QoE) en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-162">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-163">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="b1dd4-163">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-164">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-164">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-165">Cadena de agente de usuario de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-165">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-166">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="b1dd4-166">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-167">smallint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-167">smallint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-168">Tipo de agente de usuario del destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-168">Type of callee’s user agent.</span></span> <span data-ttu-id="b1dd4-169">Para obtener más información, vea la <a href="lync-server-2013-useragent-table.md">tabla UserAgent en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-169">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-170">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="b1dd4-170">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-171">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-171">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-172">Categoría del agente de usuario del destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-172">Category of callee’s user agent.</span></span> <span data-ttu-id="b1dd4-173">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table-qoe.md">tabla UserAgentDef (QoE) en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-173">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-174">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-174">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-176">Nombre del punto de conexión de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-176">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-177">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-177">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-179">Nombre del extremo de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-179">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-180">CallerOS</span><span class="sxs-lookup"><span data-stu-id="b1dd4-180">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-181">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="b1dd4-181">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-182">Sistema operativo (SO) del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-182">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-183">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="b1dd4-183">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-184">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="b1dd4-184">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-185">Sistema operativo (SO) del extremo de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-185">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-186">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="b1dd4-186">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-187">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="b1dd4-187">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-188">Nombre de la CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-188">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-189">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="b1dd4-189">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-190">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="b1dd4-190">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-191">Nombre de la CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-191">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-192">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="b1dd4-192">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-193">smallint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-193">smallint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-194">Número de núcleos de CPU en el extremo de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-194">Number of CPU cores in the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-195">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="b1dd4-195">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-196">smallint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-196">smallint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-197">Número de núcleos de la CPU en el punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-197">Number of CPU cores in the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-198">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="b1dd4-198">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-199">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-199">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-200">Velocidad del procesador de CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-200">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-201">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="b1dd4-201">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-202">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-202">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-203">Velocidad del procesador de CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-203">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-204">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="b1dd4-204">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-206">Indica si el sistema de la persona que llama se está ejecutando en un entorno virtualizado.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-206">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="b1dd4-207">Para obtener más información, consulte la <a href="lync-server-2013-endpoint-table.md">tabla de extremos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-207">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-208">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="b1dd4-208">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-209">tinyint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-209">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-210">Indica si el sistema de la persona que llama se está ejecutando en un entorno virtualizado.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-210">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="b1dd4-211">Para obtener más información, consulte la <a href="lync-server-2013-endpoint-table.md">tabla de extremos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-211">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-212">CorrelationKey</span><span class="sxs-lookup"><span data-stu-id="b1dd4-212">CorrelationKey</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b1dd4-213">Clave de correlación.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-213">Correlation key.</span></span> <span data-ttu-id="b1dd4-214">Se hace referencia a ellos desde la <a href="lync-server-2013-sessioncorrelation-table.md">tabla SessionCorrelation en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-214">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-215">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="b1dd4-215">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-216">tinyint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-216">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-217">Información sobre la ruta multimedia, como Direct o retransmitida.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-217">Information about the media path, such as direct or relayed.</span></span> <span data-ttu-id="b1dd4-218">Para obtener más información, consulte la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-218">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-219">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="b1dd4-219">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-220">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-220">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-221">Información sobre el proceso de establecimiento de conectividad interactiva (ICE) descrito en indicadores de bits para la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-221">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="b1dd4-222">Para obtener más información, consulte la especificación de protocolo de servidor de supervisión de la calidad de la experiencia.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-222">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-223">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="b1dd4-223">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-224">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-224">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-225">Información sobre el proceso de establecimiento de conectividad interactiva (ICE) descrito en marcas de bits para el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-225">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="b1dd4-226">Para obtener más información, consulte la especificación de protocolo de servidor de supervisión de la calidad de la experiencia.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-226">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-227">Transport</span><span class="sxs-lookup"><span data-stu-id="b1dd4-227">Transport</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-228">tinyint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-228">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-229">Tipo de transporte: 0 es UDP, 1 es TCP.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-229">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-230">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="b1dd4-230">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-232">Dirección IP del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-232">IP address of the caller.</span></span> <span data-ttu-id="b1dd4-233">Puede ser una dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-234">CallerPort</span><span class="sxs-lookup"><span data-stu-id="b1dd4-234">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-235">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-235">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-236">Puerto usado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-236">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-237">CallerInside</span><span class="sxs-lookup"><span data-stu-id="b1dd4-237">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-238">bit</span><span class="sxs-lookup"><span data-stu-id="b1dd4-238">bit</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-239">Indica si la persona que llama está dentro de la red de intervalos: 1 significa que la persona que llama está dentro de la red de la empresa, 0 significa que la persona que llama está fuera de la red.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-239">Indicates whether the caller is inside the interval network: 1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-240">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="b1dd4-240">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-241">var (50)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-241">var(50)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-242">Dirección IP del destinatario.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-242">IP address of the callee.</span></span> <span data-ttu-id="b1dd4-243">Puede ser una dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-243">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-244">CalleePort</span><span class="sxs-lookup"><span data-stu-id="b1dd4-244">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-245">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-245">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-246">Puerto usado por el destinatario.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-246">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-247">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="b1dd4-247">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-248">bit</span><span class="sxs-lookup"><span data-stu-id="b1dd4-248">bit</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-249">Indica si el destinatario de la llamada está dentro de la red de intervalos: 1 significa que el destinatario de la llamada está dentro de la red de la empresa, 0 significa que el destinatario de la llamada está fuera de la red.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-249">Indicates whether the callee is inside the interval network: 1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-250">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="b1dd4-250">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-251">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="b1dd4-251">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-252">Nombre del sitio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-252">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-253">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="b1dd4-253">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-254">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="b1dd4-254">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-255">Nombre del país o de la región del sitio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-255">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-256">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="b1dd4-256">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-257">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="b1dd4-257">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-258">Nombre del sitio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-258">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-259">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="b1dd4-259">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-260">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="b1dd4-260">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-261">Nombre del país o región del sitio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-261">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-262">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="b1dd4-262">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-263">var (50)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-263">var(50)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-264">Dirección IP del servicio perimetral A/V que usa el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-264">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="b1dd4-265">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-265">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-266">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="b1dd4-266">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-267">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-267">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-268">Puerto usado en el servicio perimetral A/V usado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-268">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-269">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="b1dd4-269">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-270">var (50)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-270">var(50)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-271">Clave de dirección IP del servicio perimetral A/V que usa el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-271">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="b1dd4-272">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-272">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-273">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="b1dd4-273">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-274">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-274">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-275">Puerto usado en el servicio de borde A/V que usa el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-275">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-276">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="b1dd4-276">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-277">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-277">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-278">Nombre del dispositivo de captura del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-278">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-279">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="b1dd4-279">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-280">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-280">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-281">Nombre del dispositivo de representación del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-281">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-282">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="b1dd4-282">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-283">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-283">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-284">Nombre del controlador del dispositivo de captura del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-284">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-285">CallerRenderDriver</span><span class="sxs-lookup"><span data-stu-id="b1dd4-285">CallerRenderDriver</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-286">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-286">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-287">Nombre del controlador del dispositivo de representación del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-287">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-288">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="b1dd4-288">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-289">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-289">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-290">Nombre del dispositivo de captura de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-290">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-291">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="b1dd4-291">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-292">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-292">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-293">Nombre del dispositivo de representación de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-293">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-294">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="b1dd4-294">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-295">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-295">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-296">Nombre del controlador del dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-296">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-297">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="b1dd4-297">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-298">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-298">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-299">Nombre del controlador del dispositivo de representación de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-299">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-300">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="b1dd4-300">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-302">Tipo de conexión de red de la persona que llama: 0 es con cable, 1 es inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-302">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-303">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="b1dd4-303">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-304">bit</span><span class="sxs-lookup"><span data-stu-id="b1dd4-304">bit</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-305">Indica si la persona que llama se conecta a través de una red privada virtual: 1 es una red privada virtual (VPN), 0 no es una VPN.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-305">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-306">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="b1dd4-306">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-307">decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-307">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-308">Velocidad de vínculo de red para el punto final de la llamada en bps.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-308">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-309">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="b1dd4-309">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-310">tinyint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-310">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-311">Tipo de conexión de red de la persona que llama: 0 es con cable, 1 es inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-311">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-312">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="b1dd4-312">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-313">bit</span><span class="sxs-lookup"><span data-stu-id="b1dd4-313">bit</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-314">Indica si la persona que llama se conecta a través de una red privada virtual: 1 es una red privada virtual (VPN), 0 no es una VPN.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-314">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-315">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="b1dd4-315">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-316">decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-316">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-317">Velocidad de vínculo de red para el punto final de la persona que llama en bps.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-317">Network link speed for the callee's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-318">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="b1dd4-318">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-319">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-319">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-320">OP de banda estrecha de las sesiones de audio (basadas en ambas secuencias de audio).</span><span class="sxs-lookup"><span data-stu-id="b1dd4-320">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-321">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="b1dd4-321">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-322">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-322">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-323">El ancho de banda real aplicado a la transmisión de la parte de envío dada proporciona varias configuraciones de directiva (TURN, API, SDP, Policy Server, etc.).</span><span class="sxs-lookup"><span data-stu-id="b1dd4-323">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="b1dd4-324">Esto no se debe confundir con el ancho de banda efectivo porque puede haber un ancho de banda más bajo según el cálculo de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-324">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="b1dd4-325">Básicamente, este es el ancho de banda máximo que la secuencia de envío puede tomar límites de bloqueo impuestas por la estimación del ancho de banda</span><span class="sxs-lookup"><span data-stu-id="b1dd4-325">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-326">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="b1dd4-326">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-327">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-327">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-328">Vibración de red media de las estadísticas del Protocolo de control de tiempo real (RTCP).</span><span class="sxs-lookup"><span data-stu-id="b1dd4-328">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-329">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="b1dd4-329">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-330">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-330">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-331">Vibración máxima de la red durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-331">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-332">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="b1dd4-332">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-333">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-333">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-334">Tasa promedio de pérdida de paquetes durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-334">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-335">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="b1dd4-335">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-336">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-336">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-337">Pérdida máxima de paquetes observadas durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-337">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-338">BurstDensity</span><span class="sxs-lookup"><span data-stu-id="b1dd4-338">BurstDensity</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-339">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-339">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-340">Densidad promedio de pérdida de paquetes durante las ráfagas de pérdidas durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-340">Average density of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-341">BurstDuration</span><span class="sxs-lookup"><span data-stu-id="b1dd4-341">BurstDuration</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-342">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-342">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-343">Duración media de pérdida de paquetes durante ráfagas de pérdidas durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-343">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-344">BurstGapDensity</span><span class="sxs-lookup"><span data-stu-id="b1dd4-344">BurstGapDensity</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-345">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-345">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-346">Densidad media de pérdida de paquetes entre ráfagas de pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-346">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-347">BurstGapDuration</span><span class="sxs-lookup"><span data-stu-id="b1dd4-347">BurstGapDuration</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-348">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-348">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-349">Duración media de los huecos entre las ráfagas de pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-349">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-350">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="b1dd4-350">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-351">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-351">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-352">Recuento de paquetes de la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-352">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-353">Ancho de banda más</span><span class="sxs-lookup"><span data-stu-id="b1dd4-353">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-354">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-354">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-355">Cálculo de ancho de banda para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-355">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-356">DegradationAvg</span><span class="sxs-lookup"><span data-stu-id="b1dd4-356">DegradationAvg</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-357">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-357">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-358">Degradación de MOS de red para toda la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-358">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="b1dd4-359">El intervalo está comprendido entre 0,0 y 5,0.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-359">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="b1dd4-360">Esta métrica muestra el monto que se redujo en el MOS de red debido a la vibración y a la pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-360">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="b1dd4-361">Para una calidad aceptable, debe ser menor que 0,5.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-361">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-362">DegradationMax</span><span class="sxs-lookup"><span data-stu-id="b1dd4-362">DegradationMax</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-363">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-363">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-364">La degradación de OP máxima de red durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-364">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-365">DegradationJitterAvg</span><span class="sxs-lookup"><span data-stu-id="b1dd4-365">DegradationJitterAvg</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-366">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-366">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-367">Degradación de MOS de red causada por vibración.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-367">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-368">DegradationPacketLossAvg</span><span class="sxs-lookup"><span data-stu-id="b1dd4-368">DegradationPacketLossAvg</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-369">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-369">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-370">Degradación de MOS de red causada por pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-370">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-371">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="b1dd4-371">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-372">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-372">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-373">El códec de audio usado para la llamada, al que se hace referencia desde la <a href="lync-server-2013-payloaddescription-table.md">tabla PayloadDescription en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-373">The audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-374">AudioSampleRate</span><span class="sxs-lookup"><span data-stu-id="b1dd4-374">AudioSampleRate</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-375">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-375">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-376">Frecuencia de muestreo de la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-376">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-377">CallerSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-377">CallerSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-378">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-378">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-379">Nivel posterior de señal de audio de control de ganancia analógica para el audio enviado por la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-379">Post-Analog Gain Control audio signal level for the audio the caller sent.</span></span> <span data-ttu-id="b1dd4-380">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-380">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b1dd4-381">Para obtener una calidad aceptable, debe tener al menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-381">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="b1dd4-382">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-382">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-383">CallerRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-383">CallerRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-384">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-384">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-385">Nivel de señal de audio del audio recibido por la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-385">Audio signal level for the audio the caller received.</span></span> <span data-ttu-id="b1dd4-386">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-386">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b1dd4-387">Para obtener una calidad aceptable, debe tener al menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-387">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="b1dd4-388">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-388">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-389">CallerSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-389">CallerSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-390">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-390">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-391">El nivel de ruido de audio de control de ganancia posterior analógico para el audio enviado por la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-391">Post-Analog Gain Control audio noise level for the audio the caller sent.</span></span> <span data-ttu-id="b1dd4-392">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-392">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b1dd4-393">Para obtener una calidad aceptable, debe ser menor que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-393">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="b1dd4-394">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-394">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-395">CallerRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-395">CallerRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-396">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-396">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-397">El nivel de ruido de audio de control de ganancia posterior analógico para el audio recibido por la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-397">Post-Analog Gain Control audio noise level for the audio the caller received.</span></span> <span data-ttu-id="b1dd4-398">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-398">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b1dd4-399">Para obtener una calidad aceptable, debe ser menor que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-399">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="b1dd4-400">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-400">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-401">CallerEchoReturn</span><span class="sxs-lookup"><span data-stu-id="b1dd4-401">CallerEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-402">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-402">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-403">Return echo Return Enhancement para la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-403">Echo Return Loss Enhancement for the caller.</span></span> <span data-ttu-id="b1dd4-404">La unidad para esta métrica es dB.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-404">The unit for this metric is dB.</span></span> <span data-ttu-id="b1dd4-405">Los valores más bajos representan menos eco.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-405">Lower values represent less echo.</span></span> <span data-ttu-id="b1dd4-406">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-406">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-407">CallerSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="b1dd4-407">CallerSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-408">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-408">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-409">Promedio de problemas por cinco minutos para la representación del altavoz de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-409">Average glitches per five minutes for the caller’s loudspeaker rendering.</span></span> <span data-ttu-id="b1dd4-410">Para obtener una buena calidad, debe ser inferior a un período de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-410">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="b1dd4-411">No se han notificado por servidores de conferencia A/V, servidores de mediación o teléfonos IP.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-411">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-412">CallerMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="b1dd4-412">CallerMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-413">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-413">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-414">Promedio de problemas por cinco minutos para la captura de micrófono de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-414">Average glitches per five minutes for the caller’s microphone capture.</span></span> <span data-ttu-id="b1dd4-415">Para obtener una buena calidad, debe ser inferior a uno por cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-415">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="b1dd4-416">No se han notificado por servidores de conferencia A/V, servidores de mediación o teléfonos IP.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-416">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-417">CallerTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="b1dd4-417">CallerTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-418">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-418">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-419">Tasa de desplazamiento del reloj del dispositivo de la persona que llama, en relación con el reloj de la CPU.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-419">Caller’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-420">CallerTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="b1dd4-420">CallerTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-421">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-421">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-422">Velocidad de desplazamiento del reloj del dispositivo de altavoz del autor de la llamada, relativa al reloj de la CPU.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-422">Caller’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-423">CallerTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="b1dd4-423">CallerTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-424">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-424">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-425">Error de marca de tiempo de captura de micrófono promedio, en milisegundos, en los últimos 20 segundos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-425">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-426">CallerTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="b1dd4-426">CallerTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-427">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-427">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-428">Promedio del error de marca de tiempo de la secuencia de representación de altavoces de la persona que llama, en milisegundos, en los últimos 20 segundos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-428">Average of the caller’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-429">CallerVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="b1dd4-429">CallerVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-430">smallint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-430">smallint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-431">El cambio de voz es un modo de dúplex medio con una capacidad de interrupción reducida.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-431">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="b1dd4-432">Para obtener más información, consulte la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-432">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-433">CallerEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="b1dd4-433">CallerEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-434">tinyint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-434">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-435">Causas de un evento de Eco para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-435">Causes of an echo event for the caller.</span></span> <span data-ttu-id="b1dd4-436">Para obtener más información, consulte la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-436">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-437">CallerEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="b1dd4-437">CallerEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-438">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-438">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-439">Porcentaje de tiempo en que se detecta eco en el flujo de captura de micrófono de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-439">Percentage of time when echo is detected in the caller’s microphone capture stream.</span></span> <span data-ttu-id="b1dd4-440">Si se usa un auricular, el valor debe ser bajo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-440">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-441">CallerEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="b1dd4-441">CallerEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-442">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-442">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-443">Porcentaje de tiempo durante el que se detecta eco en el flujo enviado de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-443">Percentage of time when echo is detected in the caller’s sent stream.</span></span> <span data-ttu-id="b1dd4-444">Porcentaje de eco alto en secuencias de envío indica una pérdida de eco.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-444">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-445">CallerRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-445">CallerRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-446">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-446">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-447">Nivel de señal recibido en el servidor de mediación de la puerta de enlace para el audio de la persona que llama; Esto solo se aplica al servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-447">Received signal level on the Mediation Server from the Gateway for the caller’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="b1dd4-448">La unidad de esta métrica es dBoV.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-448">The unit of this metric is dBoV.</span></span> <span data-ttu-id="b1dd4-449">Para obtener una buena calidad, el rango aceptable debe ser de-30 a-18 dBoV.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-449">For good quality, the acceptable range should be -30 to -18 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-450">CallerRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-450">CallerRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-451">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-451">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-452">Nivel de señal recibido en el servidor de mediación de la puerta de enlace para el audio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-452">Received signal level on the Mediation Server from the Gateway for the caller’s audio.</span></span> <span data-ttu-id="b1dd4-453">Esto solo se aplica al servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-453">This applies only to the Mediation Server.</span></span> <span data-ttu-id="b1dd4-454">La unidad de esta métrica es dBoV.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-454">The unit of this metric is dBoV.</span></span> <span data-ttu-id="b1dd4-455">Para obtener una buena calidad, el rango aceptable debe ser menor que-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-455">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-456">CallerRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="b1dd4-456">CallerRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-457">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-457">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-458">Control automático de ganancia (AGC) en el servidor de mediación aplicado al audio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-458">Automatic gain control (AGC) on the Mediation Server side applied to the caller’s audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-459">CallerInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="b1dd4-459">CallerInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-460">float</span><span class="sxs-lookup"><span data-stu-id="b1dd4-460">float</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-461">Cuadrado principal raíz (RMS) de la señal entrante al autor de la llamada durante los primeros 30 segundos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-461">Root mean square (RMS) of the incoming signal to the caller for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-462">CalleeSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-462">CalleeSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-463">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-463">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-464">Representa el nivel de señal de audio de control de ganancia posterior analógico para el audio que envió el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-464">Represents the Post-Analog Gain Control audio signal level for the audio the callee sent.</span></span> <span data-ttu-id="b1dd4-465">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-465">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b1dd4-466">Para obtener una calidad aceptable, debe tener al menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-466">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="b1dd4-467">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-467">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-468">CalleeRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-468">CalleeRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-469">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-469">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-470">Nivel de señal de audio del audio recibido por el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-470">Audio signal level for the audio the callee received.</span></span> <span data-ttu-id="b1dd4-471">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-471">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b1dd4-472">Para obtener una calidad aceptable, debe tener al menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-472">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="b1dd4-473">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-473">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-474">CalleeSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-474">CalleeSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-475">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-475">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-476">El nivel de ruido de audio de control de ganancia posterior analógico para el audio que envió el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-476">Post-Analog Gain Control audio noise level for the audio the callee sent.</span></span> <span data-ttu-id="b1dd4-477">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-477">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b1dd4-478">Para obtener una calidad aceptable, debe ser menor que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-478">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="b1dd4-479">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-479">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-480">CalleeRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-480">CalleeRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-481">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-481">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-482">El nivel de ruido de audio de control de ganancia posterior analógico para el audio recibido.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-482">Post-Analog Gain Control audio noise level for the audio the callee received.</span></span> <span data-ttu-id="b1dd4-483">La unidad para esta métrica es dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-483">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b1dd4-484">Para obtener una calidad aceptable, debe ser menor que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-484">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="b1dd4-485">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-485">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-486">CalleeEchoReturn</span><span class="sxs-lookup"><span data-stu-id="b1dd4-486">CalleeEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-487">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-487">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-488">Return echo Return Enhancement para el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-488">Echo Return Loss Enhancement for the callee.</span></span> <span data-ttu-id="b1dd4-489">La unidad para esta métrica es dB.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-489">The unit for this metric is dB.</span></span> <span data-ttu-id="b1dd4-490">Los valores más bajos representan menos eco.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-490">Lower values represent less echo.</span></span> <span data-ttu-id="b1dd4-491">El servidor de conferencia A/V o los teléfonos IP no han informado de esta métrica.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-491">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-492">CalleeSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="b1dd4-492">CalleeSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-493">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-493">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-494">Promedio de problemas por cinco minutos para la representación del altavoz de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-494">Average glitches per five minutes for the callee’s loudspeaker rendering.</span></span> <span data-ttu-id="b1dd4-495">Para obtener una buena calidad, debe ser inferior a un período de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-495">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="b1dd4-496">No se han notificado por servidores de conferencia A/V, servidores de mediación o teléfonos IP.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-496">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-497">CalleeMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="b1dd4-497">CalleeMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-498">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-498">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-499">Promedio de problemas por cinco minutos para la captura de micrófono de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-499">Average glitches per five minutes for the callee’s microphone capture.</span></span> <span data-ttu-id="b1dd4-500">Para obtener una buena calidad, debe ser inferior a uno por cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-500">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="b1dd4-501">No se han notificado por servidores de conferencia A/V, servidores de mediación o teléfonos IP.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-501">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-502">CalleeTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="b1dd4-502">CalleeTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-503">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-503">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-504">Tasa de desplazamiento del reloj del dispositivo de micrófono del destinatario, relativa al reloj de la CPU.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-504">Callee’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-505">CalleeTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="b1dd4-505">CalleeTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-506">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-506">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-507">Tasa de desplazamiento del reloj del dispositivo de altavoz de la llamada, relativa al reloj de la CPU.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-507">Callee’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-508">CalleeTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="b1dd4-508">CalleeTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-509">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-509">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-510">Error de marca de tiempo de captura de micrófono promedio, en milisegundos, en los últimos 20 segundos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-510">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-511">CalleeTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="b1dd4-511">CalleeTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-512">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-512">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-513">Promedio del error de marca de tiempo del altavoz del destinatario de la llamada, en milisegundos, en los últimos 20 segundos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-513">Average of the callee’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-514">CalleeVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="b1dd4-514">CalleeVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-515">smallint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-515">smallint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-516">El cambio de voz es un modo de dúplex medio con una capacidad de interrupción reducida.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-516">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="b1dd4-517">Para obtener más información, consulte la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-517">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-518">CalleeEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="b1dd4-518">CalleeEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-519">tinyint</span><span class="sxs-lookup"><span data-stu-id="b1dd4-519">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-520">Causas de un evento de Eco para el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-520">Causes of an echo event for the callee.</span></span> <span data-ttu-id="b1dd4-521">Para obtener más información, consulte la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b1dd4-521">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-522">CalleeEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="b1dd4-522">CalleeEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-523">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-523">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-524">Porcentaje de tiempo durante el que se detecta eco en el flujo de captura de micrófono de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-524">Percentage of time when echo is detected in the callee’s microphone capture stream.</span></span> <span data-ttu-id="b1dd4-525">Si se usa un auricular, el valor debe ser bajo.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-525">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-526">CalleeEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="b1dd4-526">CalleeEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-527">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-527">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-528">Porcentaje de tiempo durante el que se detecta eco en el flujo enviado de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-528">Percentage of time when echo is detected in the callee’s sent stream.</span></span> <span data-ttu-id="b1dd4-529">Porcentaje de eco alto en secuencias de envío indica una pérdida de eco.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-529">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-530">CalleeRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-530">CalleeRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-531">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-531">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-532">Nivel de señal recibido en el servidor de mediación de la puerta de enlace para el audio de la persona que llama; Esto solo se aplica al servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-532">Received signal level on the Mediation Server from the Gateway for the callee’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="b1dd4-533">La unidad de esta métrica es dBoV.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-533">The unit of this metric is dBoV.</span></span> <span data-ttu-id="b1dd4-534">Para obtener una buena calidad, el rango aceptable debe ser [-30 a-18] dBoV.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-534">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-535">CalleeRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="b1dd4-535">CalleeRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-536">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-536">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-537">Nivel de señal recibido en el servidor de mediación de la puerta de enlace para el audio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-537">Received signal level on the Mediation Server from the Gateway for the callee’s audio.</span></span> <span data-ttu-id="b1dd4-538">Esto solo se aplica al servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-538">This applies only to the Mediation Server.</span></span> <span data-ttu-id="b1dd4-539">La unidad de esta métrica es dBoV.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-539">The unit of this metric is dBoV.</span></span> <span data-ttu-id="b1dd4-540">Para obtener una buena calidad, el rango aceptable debe ser menor que-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-540">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-541">CalleeRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="b1dd4-541">CalleeRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-542">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-542">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-543">Control automático de ganancia (AGC) en el servidor de mediación aplicado al audio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-543">Automatic gain control (AGC) on the Mediation Server side applied to the callee’s audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-544">CalleeInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="b1dd4-544">CalleeInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-545">float</span><span class="sxs-lookup"><span data-stu-id="b1dd4-545">float</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-546">Cuadrado de la media raíz (RMS) de la señal entrante para el destinatario durante los primeros 30 segundos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-546">Root mean square (RMS) of the incoming signal to the callee for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-547">RatioConcealedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="b1dd4-547">RatioConcealedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-548">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-548">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-549">Relación media entre las muestras ocultas generadas por la corrección de audio a muestras típicas.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-549">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-550">RatioStretchedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="b1dd4-550">RatioStretchedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-551">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-551">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-552">Relación media de muestras extendidas generadas por la recuperación de audio a muestras típicas.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-552">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-553">RatioCompressedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="b1dd4-553">RatioCompressedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-554">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-554">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-555">Relación media de muestras comprimidas generadas por la corrección de audio a muestras típicas.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-555">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-556">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="b1dd4-556">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-557">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-557">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-558">Tiempo de ida y vuelta de las estadísticas de RTCP.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-558">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-559">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="b1dd4-559">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-560">int</span><span class="sxs-lookup"><span data-stu-id="b1dd4-560">int</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-561">Tiempo máximo de ida y vuelta para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-561">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-562">OverallAvgNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="b1dd4-562">OverallAvgNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-563">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-563">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-564">MOS de red de banda ancha promedio para la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-564">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="b1dd4-565">Esta métrica depende de la pérdida del paquete, de la vibración y del códec usado.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-565">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="b1dd4-566">El intervalo está comprendido entre 1,0 y 5,0.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-566">Range is 1.0 to 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-567">OverallMinNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="b1dd4-567">OverallMinNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-568">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-568">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-569">MOS de red de banda ancha mínima para la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-569">Minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-570">SendListenMOS</span><span class="sxs-lookup"><span data-stu-id="b1dd4-570">SendListenMOS</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-571">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-571">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-572">Puntuación de MOS de escucha de banda ancha prevista para el audio enviado, incluyendo el nivel de voz, el nivel de ruido y las características del dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-572">Average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-573">SendListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="b1dd4-573">SendListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-574">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-574">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-575">SendListenMOS mínimo para la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-575">Minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-576">RecvListenMOS</span><span class="sxs-lookup"><span data-stu-id="b1dd4-576">RecvListenMOS</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-577">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-577">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-578">Puntuación de MOS de escucha de banda ancha prevista para el audio recibido de la red, incluido el nivel de voz, nivel de ruido, códec, condiciones de red y características de dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-578">Average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-579">RecvListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="b1dd4-579">RecvListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-580">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="b1dd4-580">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-581">RecvListenMOS mínimo para la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-581">Minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1dd4-582">AudioFECUsed</span><span class="sxs-lookup"><span data-stu-id="b1dd4-582">AudioFECUsed</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-583">bit</span><span class="sxs-lookup"><span data-stu-id="b1dd4-583">bit</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-584">Indica si se usó el audio FEC para la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-584">Indicates whether audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1dd4-585">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="b1dd4-585">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-586">bit</span><span class="sxs-lookup"><span data-stu-id="b1dd4-586">bit</span></span></p></td>
<td><p><span data-ttu-id="b1dd4-587">Indica la dirección de la información identificada por p; 1 significa que la dirección de la transmisión es de la persona que llama al destinatario de la llamada. 0 significa que la dirección de la transmisión es de la persona que llama a la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="b1dd4-587">Indicates direction of the p-asserted identify information; 1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b1dd4-588">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1dd4-588">


</div>

<span> </span>

</div>

</div>

</span></span></div>

