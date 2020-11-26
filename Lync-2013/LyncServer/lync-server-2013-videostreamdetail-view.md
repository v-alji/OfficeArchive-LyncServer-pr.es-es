---
title: 'Lync Server 2013: vista VideoStreamDetail'
description: 'Lync Server 2013: vista VideoStreamDetail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStreamDetail view
ms:assetid: ec8c45e1-307d-40ec-a75e-6083306105f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721928(v=OCS.15)
ms:contentKeyID: 49733863
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3f420c292627d15fd0d54f2eba01c565a49a72d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443429"
---
# <a name="videostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="34ba8-103">Vista VideoStreamDetail en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34ba8-103">VideoStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34ba8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34ba8-104">

<span> </span></span></span>

<span data-ttu-id="34ba8-105">_**Última modificación del tema:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="34ba8-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="34ba8-106">La vista VideoStreamDetail almacena información acerca de cada secuencia de vídeo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="34ba8-106">The VideoStreamDetail View stores information about each video stream in the database.</span></span> <span data-ttu-id="34ba8-107">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34ba8-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34ba8-108">Columna</span><span class="sxs-lookup"><span data-stu-id="34ba8-108">Column</span></span></th>
<th><span data-ttu-id="34ba8-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="34ba8-109">Data Type</span></span></th>
<th><span data-ttu-id="34ba8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="34ba8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="34ba8-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="34ba8-112">datetime</span><span class="sxs-lookup"><span data-stu-id="34ba8-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="34ba8-113">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="34ba8-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="34ba8-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="34ba8-115">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-115">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-116">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="34ba8-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-117">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="34ba8-117">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="34ba8-118">tinyint</span><span class="sxs-lookup"><span data-stu-id="34ba8-118">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-119">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="34ba8-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-120">StreamId</span><span class="sxs-lookup"><span data-stu-id="34ba8-120">StreamId</span></span></p></td>
<td><p><span data-ttu-id="34ba8-121">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-121">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-122">IDENTIFICADOR exclusivo dentro de una línea de medios.</span><span class="sxs-lookup"><span data-stu-id="34ba8-122">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-123">StartTime</span><span class="sxs-lookup"><span data-stu-id="34ba8-123">StartTime</span></span></p></td>
<td><p><span data-ttu-id="34ba8-124">datetime</span><span class="sxs-lookup"><span data-stu-id="34ba8-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="34ba8-125">Hora de inicio de la sesión.</span><span class="sxs-lookup"><span data-stu-id="34ba8-125">Start time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-126">EndTime</span><span class="sxs-lookup"><span data-stu-id="34ba8-126">EndTime</span></span></p></td>
<td><p><span data-ttu-id="34ba8-127">datetime</span><span class="sxs-lookup"><span data-stu-id="34ba8-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="34ba8-128">Hora de finalización de la sesión.</span><span class="sxs-lookup"><span data-stu-id="34ba8-128">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-129">CallPriority</span><span class="sxs-lookup"><span data-stu-id="34ba8-129">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="34ba8-130">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-130">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-131">Prioridad de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-131">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-132">CallerPool</span><span class="sxs-lookup"><span data-stu-id="34ba8-132">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="34ba8-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-134">FQDN del grupo de llamadas.</span><span class="sxs-lookup"><span data-stu-id="34ba8-134">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-135">CalleePool</span><span class="sxs-lookup"><span data-stu-id="34ba8-135">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="34ba8-136">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-136">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-137">FQDN del grupo de destinatarios de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-137">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-138">Autor de llamada</span><span class="sxs-lookup"><span data-stu-id="34ba8-138">Caller</span></span></p></td>
<td><p><span data-ttu-id="34ba8-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="34ba8-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-140">URI de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-140">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-141">Destinatario de la llamada</span><span class="sxs-lookup"><span data-stu-id="34ba8-141">Callee</span></span></p></td>
<td><p><span data-ttu-id="34ba8-142">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="34ba8-142">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-143">URI de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-143">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-144">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="34ba8-144">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="34ba8-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-146">Cadena de agente de usuario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-146">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-147">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="34ba8-147">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="34ba8-148">smallint</span><span class="sxs-lookup"><span data-stu-id="34ba8-148">smallint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-149">Tipo de agente de usuario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-149">Type of caller’s user agent.</span></span> <span data-ttu-id="34ba8-150">Para obtener más información, vea la <a href="lync-server-2013-useragent-table.md">tabla UserAgent en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34ba8-150">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-151">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="34ba8-151">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="34ba8-152">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="34ba8-152">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-153">Categoría del agente de usuario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-153">Category of caller’s user agent.</span></span> <span data-ttu-id="34ba8-154">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table-qoe.md">tabla UserAgentDef (QoE) en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34ba8-154">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-155">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="34ba8-155">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="34ba8-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-157">Cadena de agente de usuario de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-157">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-158">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="34ba8-158">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="34ba8-159">smallint</span><span class="sxs-lookup"><span data-stu-id="34ba8-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-160">Tipo de agente de usuario del destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-160">Type of callee’s user agent.</span></span> <span data-ttu-id="34ba8-161">Para obtener más información, vea la <a href="lync-server-2013-useragent-table.md">tabla UserAgent en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34ba8-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-162">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="34ba8-162">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="34ba8-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="34ba8-163">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-164">Categoría del agente de usuario del destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-164">Category of callee’s user agent.</span></span> <span data-ttu-id="34ba8-165">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table-qoe.md">tabla UserAgentDef (QoE) en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34ba8-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-166">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="34ba8-166">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-168">Nombre del punto de conexión de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-168">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-169">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="34ba8-169">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-171">Nombre del extremo de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-171">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-172">CallerOS</span><span class="sxs-lookup"><span data-stu-id="34ba8-172">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="34ba8-173">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="34ba8-173">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-174">Sistema operativo (SO) del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-174">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-175">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="34ba8-175">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="34ba8-176">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="34ba8-176">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-177">Sistema operativo (SO) del extremo de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-177">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-178">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="34ba8-178">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="34ba8-179">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="34ba8-179">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-180">Nombre de la CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-180">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-181">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="34ba8-181">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="34ba8-182">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="34ba8-182">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-183">Nombre de la CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-183">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-184">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="34ba8-184">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="34ba8-185">smallint</span><span class="sxs-lookup"><span data-stu-id="34ba8-185">smallint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-186">Número de núcleos de CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-186">Number of CPU cores of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-187">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="34ba8-187">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="34ba8-188">smallint</span><span class="sxs-lookup"><span data-stu-id="34ba8-188">smallint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-189">Número de núcleos de CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-189">Number of CPU cores of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-190">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="34ba8-190">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="34ba8-191">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-191">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-192">Velocidad del procesador de CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-192">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-193">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="34ba8-193">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="34ba8-194">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-194">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-195">Velocidad del procesador de CPU del punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-195">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-196">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="34ba8-196">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="34ba8-197">tinyint</span><span class="sxs-lookup"><span data-stu-id="34ba8-197">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-198">Indica si el sistema de la persona que llama se está ejecutando en un entorno virtualizado.</span><span class="sxs-lookup"><span data-stu-id="34ba8-198">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="34ba8-199">Para obtener más información, consulte la <a href="lync-server-2013-endpoint-table.md">tabla de extremos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34ba8-199">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-200">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="34ba8-200">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="34ba8-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="34ba8-201">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-202">Indica si el sistema de la persona que llama se está ejecutando en un entorno virtualizado.</span><span class="sxs-lookup"><span data-stu-id="34ba8-202">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="34ba8-203">Para obtener más información, consulte la <a href="lync-server-2013-endpoint-table.md">tabla de extremos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34ba8-203">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-204">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="34ba8-204">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="34ba8-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="34ba8-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-206">Información sobre la ruta multimedia, como Direct o retransmitida.</span><span class="sxs-lookup"><span data-stu-id="34ba8-206">Information about media path, such as direct or relayed.</span></span> <span data-ttu-id="34ba8-207">Para obtener más información, consulte la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34ba8-207">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-208">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="34ba8-208">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="34ba8-209">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-209">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-210">Información sobre el proceso de establecimiento de conectividad interactiva (ICE) descrito en indicadores de bits para la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-210">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="34ba8-211">Para obtener más información, consulte la especificación de protocolo de servidor de supervisión de la calidad de la experiencia.</span><span class="sxs-lookup"><span data-stu-id="34ba8-211">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-212">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="34ba8-212">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="34ba8-213">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-213">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-214">Información sobre el proceso de establecimiento de conectividad interactiva (ICE) descrito en marcas de bits para el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-214">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="34ba8-215">Para obtener más información, consulte la especificación de protocolo de servidor de supervisión de la calidad de la experiencia.</span><span class="sxs-lookup"><span data-stu-id="34ba8-215">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-216">Transport</span><span class="sxs-lookup"><span data-stu-id="34ba8-216">Transport</span></span></p></td>
<td><p><span data-ttu-id="34ba8-217">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-217">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-218">Tipo de transporte: 0 es UDP, 1 es TCP.</span><span class="sxs-lookup"><span data-stu-id="34ba8-218">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-219">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="34ba8-219">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="34ba8-220">var (50)</span><span class="sxs-lookup"><span data-stu-id="34ba8-220">var(50)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-221">Dirección IP del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-221">IP address of the caller.</span></span> <span data-ttu-id="34ba8-222">Puede ser una dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="34ba8-222">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-223">CallerPort</span><span class="sxs-lookup"><span data-stu-id="34ba8-223">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="34ba8-224">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-224">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-225">Puerto usado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-225">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-226">CallerInside</span><span class="sxs-lookup"><span data-stu-id="34ba8-226">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="34ba8-227">bit</span><span class="sxs-lookup"><span data-stu-id="34ba8-227">bit</span></span></p></td>
<td><p><span data-ttu-id="34ba8-228">Indica si la persona que llama está dentro de la red de la organización.</span><span class="sxs-lookup"><span data-stu-id="34ba8-228">Indicates whether the caller is inside the organization network.</span></span> <span data-ttu-id="34ba8-229">1 significa que la persona que llama está dentro de la red de la empresa, 0 significa que la persona que llama está fuera de la red.</span><span class="sxs-lookup"><span data-stu-id="34ba8-229">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-230">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="34ba8-230">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="34ba8-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="34ba8-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-232">Dirección IP del destinatario.</span><span class="sxs-lookup"><span data-stu-id="34ba8-232">IP address of the callee.</span></span> <span data-ttu-id="34ba8-233">Puede ser una dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="34ba8-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-234">CalleePort</span><span class="sxs-lookup"><span data-stu-id="34ba8-234">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="34ba8-235">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-235">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-236">Puerto usado por el destinatario.</span><span class="sxs-lookup"><span data-stu-id="34ba8-236">Port used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-237">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="34ba8-237">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="34ba8-238">bit</span><span class="sxs-lookup"><span data-stu-id="34ba8-238">bit</span></span></p></td>
<td><p><span data-ttu-id="34ba8-239">Indica si la persona que llama está dentro de la red de la organización. 1 significa que el destinatario de la llamada está dentro de la red de la empresa, 0 significa que el destinatario de la llamada está fuera de la red.</span><span class="sxs-lookup"><span data-stu-id="34ba8-239">Indicates whether the caller is inside the organization network.1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-240">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="34ba8-240">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="34ba8-241">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="34ba8-241">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-242">Nombre del sitio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-242">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-243">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="34ba8-243">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="34ba8-244">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="34ba8-244">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-245">Nombre del país o de la región del sitio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-245">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-246">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="34ba8-246">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="34ba8-247">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="34ba8-247">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-248">Nombre del sitio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-248">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-249">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="34ba8-249">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="34ba8-250">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="34ba8-250">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-251">Nombre del país o región del sitio de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-251">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-252">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="34ba8-252">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="34ba8-253">var (50)</span><span class="sxs-lookup"><span data-stu-id="34ba8-253">var(50)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-254">Dirección IP del servicio perimetral A/V que usa el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-254">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="34ba8-255">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34ba8-255">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-256">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="34ba8-256">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="34ba8-257">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-257">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-258">Puerto en el servicio perimetral A/V usado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-258">Port on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-259">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="34ba8-259">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="34ba8-260">var (50)</span><span class="sxs-lookup"><span data-stu-id="34ba8-260">var(50)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-261">Clave de dirección IP del servicio perimetral A/V que usa el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-261">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="34ba8-262">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34ba8-262">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-263">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="34ba8-263">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="34ba8-264">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-264">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-265">Puerto del servicio perimetral A/V usado por el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-265">Port on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-266">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="34ba8-266">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="34ba8-267">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-267">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-268">Nombre del dispositivo de captura del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-268">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-269">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="34ba8-269">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="34ba8-270">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-270">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-271">Nombre del dispositivo de representación del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-271">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-272">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="34ba8-272">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="34ba8-273">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-273">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-274">Nombre del controlador del dispositivo de captura del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-274">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-275">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="34ba8-275">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="34ba8-276">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-276">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-277">Nombre del controlador del dispositivo de representación del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-277">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-278">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="34ba8-278">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="34ba8-279">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-279">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-280">Nombre del dispositivo de captura de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-280">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-281">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="34ba8-281">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="34ba8-282">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-282">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-283">Nombre del dispositivo de representación de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-283">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-284">CalleCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="34ba8-284">CalleCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="34ba8-285">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-285">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-286">Nombre del controlador del dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="34ba8-286">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-287">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="34ba8-287">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="34ba8-288">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="34ba8-288">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-289">Nombre del controlador del dispositivo de representación de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-289">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-290">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="34ba8-290">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="34ba8-291">tinyint</span><span class="sxs-lookup"><span data-stu-id="34ba8-291">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-292">Tipo de conexión de red de la persona que llama: 0 es con cable, 1 es inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="34ba8-292">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-293">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="34ba8-293">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="34ba8-294">bit</span><span class="sxs-lookup"><span data-stu-id="34ba8-294">bit</span></span></p></td>
<td><p><span data-ttu-id="34ba8-295">Indica si el autor de la llamada se ha conectado a través de una red privada virtual.</span><span class="sxs-lookup"><span data-stu-id="34ba8-295">Indicates whether or not the caller connected over a virtual private network.</span></span> <span data-ttu-id="34ba8-296">1 es una red privada virtual (VPN) y 0 no es una VPN.</span><span class="sxs-lookup"><span data-stu-id="34ba8-296">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-297">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="34ba8-297">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="34ba8-298">decimal (18;)</span><span class="sxs-lookup"><span data-stu-id="34ba8-298">decimal(18,)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-299">Velocidad de vínculo de red para el punto final de la llamada en bps.</span><span class="sxs-lookup"><span data-stu-id="34ba8-299">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-300">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="34ba8-300">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="34ba8-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="34ba8-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34ba8-302">Tipo de conexión de red de la persona que llama: 0 es con cable, 1 es inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="34ba8-302">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-303">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="34ba8-303">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="34ba8-304">bit</span><span class="sxs-lookup"><span data-stu-id="34ba8-304">bit</span></span></p></td>
<td><p><span data-ttu-id="34ba8-305">Indica si el destinatario de la llamada se conecta a través de una red privada virtual.</span><span class="sxs-lookup"><span data-stu-id="34ba8-305">Indicates whether or not the callee connected over a virtual private network.</span></span> <span data-ttu-id="34ba8-306">1 es una red privada virtual (VPN) y 0 no es una VPN.</span><span class="sxs-lookup"><span data-stu-id="34ba8-306">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-307">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="34ba8-307">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="34ba8-308">decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="34ba8-308">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-309">Velocidad de vínculo de red del extremo de la persona que llama (en bps).</span><span class="sxs-lookup"><span data-stu-id="34ba8-309">Network link speed for the callee’s endpoint (in bps).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-310">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="34ba8-310">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="34ba8-311">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="34ba8-311">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-312">OP de banda estrecha de las sesiones de audio (basadas en ambas secuencias de audio).</span><span class="sxs-lookup"><span data-stu-id="34ba8-312">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-313">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="34ba8-313">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="34ba8-314">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-314">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-315">El ancho de banda real aplicado a la transmisión de la parte de envío dada proporciona varias configuraciones de directiva (TURN, API, SDP, Policy Server, etc.).</span><span class="sxs-lookup"><span data-stu-id="34ba8-315">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="34ba8-316">Esto no se debe confundir con el ancho de banda efectivo porque puede haber un ancho de banda más bajo según el cálculo de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="34ba8-316">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="34ba8-317">Básicamente, este es el ancho de banda máximo que la secuencia de envío puede tomar límites de bloqueo impuestas por la estimación del ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="34ba8-317">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-318">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="34ba8-318">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="34ba8-319">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-319">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-320">Vibración de red media de las estadísticas del Protocolo de control de tiempo real (RTCP).</span><span class="sxs-lookup"><span data-stu-id="34ba8-320">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-321">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="34ba8-321">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="34ba8-322">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-322">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-323">Vibración máxima de la red durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-323">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-324">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="34ba8-324">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="34ba8-325">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-325">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-326">Tiempo de ida y vuelta de las estadísticas de RTCP.</span><span class="sxs-lookup"><span data-stu-id="34ba8-326">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-327">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="34ba8-327">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="34ba8-328">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-328">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-329">Tiempo máximo de ida y vuelta para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="34ba8-329">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-330">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="34ba8-330">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="34ba8-331">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="34ba8-331">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-332">Tasa promedio de pérdida de paquetes durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-332">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-333">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="34ba8-333">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="34ba8-334">decimal (4,5)</span><span class="sxs-lookup"><span data-stu-id="34ba8-334">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-335">Pérdida máxima de paquetes observadas durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-335">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-336">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="34ba8-336">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="34ba8-337">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-337">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-338">Recuento de paquetes para la secuencia de vídeo (Protocolo de transporte en tiempo real, RTP).</span><span class="sxs-lookup"><span data-stu-id="34ba8-338">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-339">Ancho de banda más</span><span class="sxs-lookup"><span data-stu-id="34ba8-339">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="34ba8-340">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-340">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-341">Cálculo de ancho de banda para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="34ba8-341">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-342">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="34ba8-342">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="34ba8-343">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-343">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-344">Códec de audio usado para la llamada, al que se hace referencia desde la <a href="lync-server-2013-payloaddescription-table.md">tabla PayloadDescription en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="34ba8-344">Audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-345">Resolución de la</span><span class="sxs-lookup"><span data-stu-id="34ba8-345">VideoResolution</span></span></p></td>
<td><p><span data-ttu-id="34ba8-346">carácter (9)</span><span class="sxs-lookup"><span data-stu-id="34ba8-346">char(9)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-347">Resolución del vídeo en píxeles ancho multiplicado por píxeles alto.</span><span class="sxs-lookup"><span data-stu-id="34ba8-347">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="34ba8-348">Se ha notificado como una cadena.</span><span class="sxs-lookup"><span data-stu-id="34ba8-348">Reported as a string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-349">VideoBitRateAvg</span><span class="sxs-lookup"><span data-stu-id="34ba8-349">VideoBitRateAvg</span></span></p></td>
<td><p><span data-ttu-id="34ba8-350">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-350">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-351">Promedio de velocidad de bits de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="34ba8-351">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-352">InboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="34ba8-352">InboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="34ba8-353">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="34ba8-353">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-354">Velocidad de fotogramas de video recibido.</span><span class="sxs-lookup"><span data-stu-id="34ba8-354">Frame rate of video received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-355">OutboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="34ba8-355">OutboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="34ba8-356">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="34ba8-356">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-357">Velocidad de fotogramas enviada.</span><span class="sxs-lookup"><span data-stu-id="34ba8-357">Frame rate of video sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-358">ViideoBitRateMax</span><span class="sxs-lookup"><span data-stu-id="34ba8-358">ViideoBitRateMax</span></span></p></td>
<td><p><span data-ttu-id="34ba8-359">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-359">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-360">Máxima tasa de bits de vídeo durante la sesión de video.</span><span class="sxs-lookup"><span data-stu-id="34ba8-360">Maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-361">Tasa</span><span class="sxs-lookup"><span data-stu-id="34ba8-361">VideoPacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="34ba8-362">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="34ba8-362">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-363">Velocidad a la que se han perdido paquetes de video.</span><span class="sxs-lookup"><span data-stu-id="34ba8-363">Rate at which video packets were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-364">VideoFrameLossRate</span><span class="sxs-lookup"><span data-stu-id="34ba8-364">VideoFrameLossRate</span></span></p></td>
<td><p><span data-ttu-id="34ba8-365">decimal (9.4)</span><span class="sxs-lookup"><span data-stu-id="34ba8-365">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-366">Porcentaje de fotogramas de video totales que se pierden.</span><span class="sxs-lookup"><span data-stu-id="34ba8-366">Percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-367">VideoFEC</span><span class="sxs-lookup"><span data-stu-id="34ba8-367">VideoFEC</span></span></p></td>
<td><p><span data-ttu-id="34ba8-368">bit</span><span class="sxs-lookup"><span data-stu-id="34ba8-368">bit</span></span></p></td>
<td><p><span data-ttu-id="34ba8-369">No usado.</span><span class="sxs-lookup"><span data-stu-id="34ba8-369">Not used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-370">VideoAllocateBWAvg</span><span class="sxs-lookup"><span data-stu-id="34ba8-370">VideoAllocateBWAvg</span></span></p></td>
<td><p><span data-ttu-id="34ba8-371">int</span><span class="sxs-lookup"><span data-stu-id="34ba8-371">int</span></span></p></td>
<td><p><span data-ttu-id="34ba8-372">Cantidad promedio de ancho de banda asignado para el vídeo.</span><span class="sxs-lookup"><span data-stu-id="34ba8-372">Average amount of bandwidth allocated for video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ba8-373">Media</span><span class="sxs-lookup"><span data-stu-id="34ba8-373">VideoLocalFrameLossPercentageAvg</span></span></p></td>
<td><p><span data-ttu-id="34ba8-374">decimal (9.4)</span><span class="sxs-lookup"><span data-stu-id="34ba8-374">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="34ba8-375">Porcentaje de fotogramas de video totales que se han perdido.</span><span class="sxs-lookup"><span data-stu-id="34ba8-375">Percentage of total video frames that were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34ba8-376">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="34ba8-376">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="34ba8-377">bit</span><span class="sxs-lookup"><span data-stu-id="34ba8-377">bit</span></span></p></td>
<td><p><span data-ttu-id="34ba8-378">Dirección de la secuencia para la información de identidad declarada en p.</span><span class="sxs-lookup"><span data-stu-id="34ba8-378">Stream direction for p-asserted identity information.</span></span> <span data-ttu-id="34ba8-379">1 significa que la dirección de la transmisión es de la persona que llama al destinatario de la llamada. 0 significa que la dirección de la transmisión es de la persona que llama a la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="34ba8-379">1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="34ba8-380">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34ba8-380">


</div>

<span> </span>

</div>

</div>

</span></span></div>

