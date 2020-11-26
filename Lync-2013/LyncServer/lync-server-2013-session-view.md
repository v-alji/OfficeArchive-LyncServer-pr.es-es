---
title: 'Lync Server 2013: vista de sesión'
description: 'Lync Server 2013: vista de sesión.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session view
ms:assetid: 49e33f5b-45d0-4146-a5a4-76954d895a98
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688048(v=OCS.15)
ms:contentKeyID: 49733641
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff4bc4abbd55e073006693d28f092f077698ef75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444794"
---
# <a name="session-view-in-lync-server-2013"></a><span data-ttu-id="5d6f8-103">Vista de sesión de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d6f8-103">Session view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d6f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d6f8-104">

<span> </span></span></span>

<span data-ttu-id="5d6f8-105">_**Última modificación del tema:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="5d6f8-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="5d6f8-106">La vista de sesión almacena información sobre las sesiones que tienen registros en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-106">The Session View stores information about sessions that have records in the database.</span></span> <span data-ttu-id="5d6f8-107">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5d6f8-108">Columna</span><span class="sxs-lookup"><span data-stu-id="5d6f8-108">Column</span></span></th>
<th><span data-ttu-id="5d6f8-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5d6f8-109">Data Type</span></span></th>
<th><span data-ttu-id="5d6f8-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="5d6f8-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-111">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="5d6f8-111">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-112">datetime</span><span class="sxs-lookup"><span data-stu-id="5d6f8-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-113">Se hace referencia a ella desde la tabla MediaLine.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-113">Referenced from the MediaLine Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-114">ConferenceURI</span><span class="sxs-lookup"><span data-stu-id="5d6f8-114">ConferenceURI</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-115">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-116">URI de conferencia si se trata de una conferencia o DialogID si se trata de una sesión de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-116">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-117">Correlación</span><span class="sxs-lookup"><span data-stu-id="5d6f8-117">Correlation</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-118">VARCHAR (Max)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-118">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-119">IDENTIFICADOR de correlación de la sesión.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-119">Correlation ID of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-120">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="5d6f8-120">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-121">bit</span><span class="sxs-lookup"><span data-stu-id="5d6f8-121">bit</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-122">Categoría de cuadro de diálogo; 0 ¿se encuentra Lync Server en la pierna del servidor de mediación; 1 es el servidor de mediación para la puerta de la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-122">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-123">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="5d6f8-123">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-124">bit</span><span class="sxs-lookup"><span data-stu-id="5d6f8-124">bit</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-125">Indica si se ha omitido la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-125">Indicates whether or not the call was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-126">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="5d6f8-126">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-127">int</span><span class="sxs-lookup"><span data-stu-id="5d6f8-127">int</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-128">Este campo, si está presente, indica por qué no se omitió una llamada, incluso si los identificadores de omisión coinciden.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-128">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="5d6f8-129">Para Lync Server, solo se define un valor:</span><span class="sxs-lookup"><span data-stu-id="5d6f8-129">For Lync Server, only one value is defined:</span></span></p>
<p><span data-ttu-id="5d6f8-130">0x0001: identificador de omisión desconocido para el adaptador de red predeterminado</span><span class="sxs-lookup"><span data-stu-id="5d6f8-130">0x0001 – Unknown bypass ID for Default network adapter</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="5d6f8-131">StartTime</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-132">datetime</span><span class="sxs-lookup"><span data-stu-id="5d6f8-132">datetime</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-133">Hora de inicio de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-133">Call start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-134">EndTime</span><span class="sxs-lookup"><span data-stu-id="5d6f8-134">EndTime</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-135">datetime</span><span class="sxs-lookup"><span data-stu-id="5d6f8-135">datetime</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-136">Hora de finalización de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-136">Call end time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-137">CallerPool</span><span class="sxs-lookup"><span data-stu-id="5d6f8-137">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-139">FQDN del grupo de llamadas.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-139">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-140">CalleePool</span><span class="sxs-lookup"><span data-stu-id="5d6f8-140">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-142">FQDN del grupo de destinatarios de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-142">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-143">CallerPAI</span><span class="sxs-lookup"><span data-stu-id="5d6f8-143">CallerPAI</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-144">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-144">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-145">URI de identidad afirmada de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-145">Caller’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-146">CalleePAI</span><span class="sxs-lookup"><span data-stu-id="5d6f8-146">CalleePAI</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-148">URI de identidad afirmada de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-148">Callee’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-149">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d6f8-149">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-151">Nombre del punto de conexión de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-151">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-152">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d6f8-152">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-154">Nombre del punto de conexión de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-154">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-155">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="5d6f8-155">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-157">Cadena de agente de usuario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-157">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-158">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="5d6f8-158">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-159">smallint</span><span class="sxs-lookup"><span data-stu-id="5d6f8-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-160">Tipo de agente de usuario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-160">Type of caller’s user agent.</span></span> <span data-ttu-id="5d6f8-161">Para obtener más información, vea la <a href="lync-server-2013-useragent-table.md">tabla UserAgent en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5d6f8-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-162">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="5d6f8-162">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-163">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-164">Categoría del agente de usuario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-164">Category of caller’s user agent.</span></span> <span data-ttu-id="5d6f8-165">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table-qoe.md">tabla UserAgentDef (QoE) en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5d6f8-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-166">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="5d6f8-166">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-168">Cadena de agente de usuario de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-168">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-169">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="5d6f8-169">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-170">smallint</span><span class="sxs-lookup"><span data-stu-id="5d6f8-170">smallint</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-171">Tipo de agente de usuario para el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-171">Type of user agent for the callee.</span></span> <span data-ttu-id="5d6f8-172">Para obtener más información, vea la <a href="lync-server-2013-useragent-table.md">tabla UserAgent en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5d6f8-172">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-173">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="5d6f8-173">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-174">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-174">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-175">Categoría de agente de usuario para el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-175">User agent category for the callee.</span></span> <span data-ttu-id="5d6f8-176">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table-qoe.md">tabla UserAgentDef (QoE) en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5d6f8-176">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-177">CallerURI</span><span class="sxs-lookup"><span data-stu-id="5d6f8-177">CallerURI</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-178">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-178">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-179">URI de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-179">Caller’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d6f8-180">CalleeURI</span><span class="sxs-lookup"><span data-stu-id="5d6f8-180">CalleeURI</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-181">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5d6f8-181">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-182">URI de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-182">Callee’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d6f8-183">CallPrioirty</span><span class="sxs-lookup"><span data-stu-id="5d6f8-183">CallPrioirty</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-184">int</span><span class="sxs-lookup"><span data-stu-id="5d6f8-184">int</span></span></p></td>
<td><p><span data-ttu-id="5d6f8-185">Prioridad de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d6f8-185">Priority of the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5d6f8-186">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d6f8-186">


</div>

<span> </span>

</div>

</div>

</span></span></div>

