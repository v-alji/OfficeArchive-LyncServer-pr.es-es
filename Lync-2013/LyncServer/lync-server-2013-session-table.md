---
title: 'Lync Server 2013: Tabla Session'
description: 'Lync Server 2013: tabla de sesiones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session table
ms:assetid: 7f05529c-794d-41ed-bca4-2e85b87b2dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398635(v=OCS.15)
ms:contentKeyID: 48184626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1a52813dfea808253cc934f71a9d4c846c2dbbd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441819"
---
# <a name="session-table-in-lync-server-2013"></a><span data-ttu-id="3a22c-103">Tabla Session en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a22c-103">Session table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3a22c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3a22c-104">

<span> </span></span></span>

<span data-ttu-id="3a22c-105">_**Última modificación del tema:** 2013-09-09_</span><span class="sxs-lookup"><span data-stu-id="3a22c-105">_**Topic Last Modified:** 2013-09-09_</span></span>

<span data-ttu-id="3a22c-106">Cada registro representa una sesión que incluye audio, audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="3a22c-106">Each record represents one session which involves audio or audio and video.</span></span> <span data-ttu-id="3a22c-107">Contiene información general sobre la sesión.</span><span class="sxs-lookup"><span data-stu-id="3a22c-107">It contains overall information about the session.</span></span> <span data-ttu-id="3a22c-108">Una sesión se define como un cuadro de diálogo de protocolo de inicio de sesión (SIP) de audio o vídeo entre dos puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="3a22c-108">A session is defined as an audio or video Session Initiation Protocol (SIP) dialog between two endpoints.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3a22c-109"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="3a22c-110"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="3a22c-111"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="3a22c-112"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-114">datetime</span><span class="sxs-lookup"><span data-stu-id="3a22c-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="3a22c-115">Primary</span><span class="sxs-lookup"><span data-stu-id="3a22c-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="3a22c-116">Se hace referencia a ellos desde la <a href="lync-server-2013-dialog-table.md">tabla de diálogo en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-116">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-118">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-118">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-119">Primary</span><span class="sxs-lookup"><span data-stu-id="3a22c-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="3a22c-120">Se hace referencia a ellos desde la <a href="lync-server-2013-dialog-table.md">tabla de diálogo en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-120">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-121"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-121"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-122">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-122">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-123">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-124">Tecla de conferencia.</span><span class="sxs-lookup"><span data-stu-id="3a22c-124">Conference key.</span></span> <span data-ttu-id="3a22c-125">Se hace referencia a ellos desde la <a href="lync-server-2013-conference-table.md">tabla de conferencia en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-125">Referenced from the <a href="lync-server-2013-conference-table.md">Conference table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-126"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-126"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-127">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-127">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-128">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-129">Clave de correlación.</span><span class="sxs-lookup"><span data-stu-id="3a22c-129">Correlation key.</span></span> <span data-ttu-id="3a22c-130">Se hace referencia a ellos desde la <a href="lync-server-2013-sessioncorrelation-table.md">tabla SessionCorrelation en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-130">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-131"><strong>DialogCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-131"><strong>DialogCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-132">bit</span><span class="sxs-lookup"><span data-stu-id="3a22c-132">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="3a22c-133">Categoría de cuadro de diálogo; 0 ¿se encuentra Lync Server en la pierna del servidor de mediación; 1 es el servidor de mediación para la puerta de la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="3a22c-133">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-134"><strong>MediationServerBypassFlag</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-134"><strong>MediationServerBypassFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-135">bit</span><span class="sxs-lookup"><span data-stu-id="3a22c-135">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3a22c-136">Marcador que indica si la llamada se ha omitido o no.</span><span class="sxs-lookup"><span data-stu-id="3a22c-136">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-137"><strong>MediaBypassWarningFlag</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-137"><strong>MediaBypassWarningFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-138">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3a22c-139">Este campo, si está presente, indica por qué no se omitió una llamada, incluso si los identificadores de omisión coinciden.</span><span class="sxs-lookup"><span data-stu-id="3a22c-139">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="3a22c-140">Para Lync Server, solo se define un valor.</span><span class="sxs-lookup"><span data-stu-id="3a22c-140">For Lync Server, only one value is defined.</span></span></p>
<p><span data-ttu-id="3a22c-141">0x0001: identificador de omisión desconocido para el adaptador de red predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3a22c-141">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-142"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-142"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-143">datetime</span><span class="sxs-lookup"><span data-stu-id="3a22c-143">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="3a22c-144">Hora de inicio de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-144">Call start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-145"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-145"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-146">datetime</span><span class="sxs-lookup"><span data-stu-id="3a22c-146">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="3a22c-147">Hora de finalización de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-147">Call end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-148"><strong>CallerPool</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-148"><strong>CallerPool</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-149">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-149">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-150">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-151">El grupo de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="3a22c-151">The pool of the caller.</span></span> <span data-ttu-id="3a22c-152">Se hace referencia a ella desde la <a href="lync-server-2013-pool-table.md">tabla de grupos en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-152">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-153"><strong>CalleePool</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-153"><strong>CalleePool</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-154">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-154">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-155">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-156">La piscina del receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-156">The pool of the call receiver.</span></span> <span data-ttu-id="3a22c-157">Se hace referencia a ella desde la <a href="lync-server-2013-pool-table.md">tabla de grupos en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-157">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-158"><strong>CalleePAI</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-158"><strong>CalleePAI</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-159">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-159">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-160">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-160">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-161">URI de SIP en la identidad declarada por SIP (PAI) del punto final de recepción.</span><span class="sxs-lookup"><span data-stu-id="3a22c-161">SIP URI in the SIP p-asserted identity (PAI) of the receiving endpoint.</span></span> <span data-ttu-id="3a22c-162">Se hace referencia a ellos desde la <a href="lync-server-2013-user-table.md">tabla de usuario en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-162">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-163"><strong>CallerURI</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-163"><strong>CallerURI</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-164">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-164">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-165">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-165">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-166">URI de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="3a22c-166">Caller’s URI.</span></span> <span data-ttu-id="3a22c-167">Se hace referencia a ellos desde la <a href="lync-server-2013-user-table.md">tabla de usuario en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-167">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-168"><strong>CallerEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-168"><strong>CallerEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-169">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-169">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-170">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-170">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-171">Extremo de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="3a22c-171">Caller’s endpoint.</span></span> <span data-ttu-id="3a22c-172">Se hace referencia a ellos desde la <a href="lync-server-2013-endpoint-table.md">tabla de extremos en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-172">Referenced from the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-173"><strong>CallerUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-173"><strong>CallerUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-174">bit</span><span class="sxs-lookup"><span data-stu-id="3a22c-174">bit</span></span></p></td>
<td><p><span data-ttu-id="3a22c-175">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-176">Agente de usuario del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-176">Caller’s user agent.</span></span> <span data-ttu-id="3a22c-177">Se hace referencia a ella desde la <a href="lync-server-2013-useragent-table.md">tabla UserAgent en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3a22c-177">Referenced from the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-178"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-178"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-179">smallint</span><span class="sxs-lookup"><span data-stu-id="3a22c-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3a22c-180">La prioridad de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-180">The priority of this call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-181"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-181"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-182">bit</span><span class="sxs-lookup"><span data-stu-id="3a22c-182">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3a22c-183">Esta columna ha quedado obsoleta y no se usa en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3a22c-183">This column has been deprecated and is not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="3a22c-184">En su lugar, esta información se notifica en una base de líneas por medios.</span><span class="sxs-lookup"><span data-stu-id="3a22c-184">Instead, this information is reported on a per-media line bases.</span></span> <span data-ttu-id="3a22c-185">Para obtener más información, consulte la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="3a22c-185">Refer to the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-186"><strong>CallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-186"><strong>CallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-187">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-187">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-188">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-189">P-asserted-identidad del usuario que realizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-189">P-Asserted-Identity of the user who placed the call.</span></span> <span data-ttu-id="3a22c-190">La identidad de aserción de P (PAI) se usa para transmitir la verdadera identidad del usuario que realizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-190">The P-Asserted-Identity (PAI) is used to convey the true identity of the user who placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-191"><strong>CalleeEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-191"><strong>CalleeEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-192">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-192">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-193">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-194">Extremo que recibió la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-194">Endpoint that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a22c-195"><strong>CalleeUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-195"><strong>CalleeUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-196">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-196">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-197">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-197">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-198">Agente de usuario empleado por el usuario que recibió la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-198">User agent employed by the user who received the call.</span></span> <span data-ttu-id="3a22c-199">Los agentes de usuario representan el dispositivo de extremo cliente.</span><span class="sxs-lookup"><span data-stu-id="3a22c-199">User agents represent the client endpoint device.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a22c-200"><strong>CalleeUri</strong></span><span class="sxs-lookup"><span data-stu-id="3a22c-200"><strong>CalleeUri</strong></span></span></p></td>
<td><p><span data-ttu-id="3a22c-201">int</span><span class="sxs-lookup"><span data-stu-id="3a22c-201">int</span></span></p></td>
<td><p><span data-ttu-id="3a22c-202">Extranjero</span><span class="sxs-lookup"><span data-stu-id="3a22c-202">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3a22c-203">URI SIP del usuario que recibió la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a22c-203">SIP URI of the user who received the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3a22c-204">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3a22c-204">


</div>

<span> </span>

</div>

</div>

</span></span></div>

