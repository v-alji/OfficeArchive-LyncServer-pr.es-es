---
title: 'Lync Server 2013: tabla UserAgentDef (QoE)'
description: 'Lync Server 2013: tabla UserAgentDef (QoE).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgentDef table (QoE)
ms:assetid: cfd8e3e0-4076-4162-9381-5276da8316d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205259(v=OCS.15)
ms:contentKeyID: 48185394
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8546a33e607524b23755e9abf3edb2d5e2e417d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439047"
---
# <a name="useragentdef-table-qoe-in-lync-server-2013"></a><span data-ttu-id="0dc5c-103">Tabla UserAgentDef (QoE) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0dc5c-103">UserAgentDef table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0dc5c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0dc5c-104">

<span> </span></span></span>

<span data-ttu-id="0dc5c-105">_**Última modificación del tema:** 2014-03-25_</span><span class="sxs-lookup"><span data-stu-id="0dc5c-105">_**Topic Last Modified:** 2014-03-25_</span></span>

<span data-ttu-id="0dc5c-106">La tabla UserAgentDef asigna los identificadores de agente de usuario a los nombres descriptivos del agente.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-106">The UserAgentDef table maps user agent identifiers to the agent’s descriptive names.</span></span> <span data-ttu-id="0dc5c-107">Los agentes de usuario son clientes de software que se usan para conectarse a Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-107">User agents are software clients used to connect to Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0dc5c-108">UAType</span><span class="sxs-lookup"><span data-stu-id="0dc5c-108">UAType</span></span></th>
<th><span data-ttu-id="0dc5c-109">UAName</span><span class="sxs-lookup"><span data-stu-id="0dc5c-109">UAName</span></span></th>
<th><span data-ttu-id="0dc5c-110">UACategory</span><span class="sxs-lookup"><span data-stu-id="0dc5c-110">UACategory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-111">1</span><span class="sxs-lookup"><span data-stu-id="0dc5c-111">1</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-112">MediationServer</span><span class="sxs-lookup"><span data-stu-id="0dc5c-112">MediationServer</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-113">MediationServer</span><span class="sxs-lookup"><span data-stu-id="0dc5c-113">MediationServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-114">2</span><span class="sxs-lookup"><span data-stu-id="0dc5c-114">2</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-115">MCU de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="0dc5c-115">AV-MCU</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-116">MCU de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="0dc5c-116">AV-MCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-117">4</span><span class="sxs-lookup"><span data-stu-id="0dc5c-117">4</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-118">OC</span><span class="sxs-lookup"><span data-stu-id="0dc5c-118">OC</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-119">OC</span><span class="sxs-lookup"><span data-stu-id="0dc5c-119">OC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-120">4,8</span><span class="sxs-lookup"><span data-stu-id="0dc5c-120">8</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-121">OCPhone</span><span class="sxs-lookup"><span data-stu-id="0dc5c-121">OCPhone</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-122">OCPhone</span><span class="sxs-lookup"><span data-stu-id="0dc5c-122">OCPhone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-123">apartado</span><span class="sxs-lookup"><span data-stu-id="0dc5c-123">16</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-124">LMC</span><span class="sxs-lookup"><span data-stu-id="0dc5c-124">LMC</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-125">LMC</span><span class="sxs-lookup"><span data-stu-id="0dc5c-125">LMC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-126">32</span><span class="sxs-lookup"><span data-stu-id="0dc5c-126">32</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-127">DVT</span><span class="sxs-lookup"><span data-stu-id="0dc5c-127">DVT</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-128">DVT</span><span class="sxs-lookup"><span data-stu-id="0dc5c-128">DVT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-129">64</span><span class="sxs-lookup"><span data-stu-id="0dc5c-129">64</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-130">MM</span><span class="sxs-lookup"><span data-stu-id="0dc5c-130">MM</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-131">MM</span><span class="sxs-lookup"><span data-stu-id="0dc5c-131">MM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-132">64</span><span class="sxs-lookup"><span data-stu-id="0dc5c-132">64</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-133">MC</span><span class="sxs-lookup"><span data-stu-id="0dc5c-133">MC</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-134">MM</span><span class="sxs-lookup"><span data-stu-id="0dc5c-134">MM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-135">128</span><span class="sxs-lookup"><span data-stu-id="0dc5c-135">128</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-136">Operador</span><span class="sxs-lookup"><span data-stu-id="0dc5c-136">Attendant</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-137">Operador</span><span class="sxs-lookup"><span data-stu-id="0dc5c-137">Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-138">256</span><span class="sxs-lookup"><span data-stu-id="0dc5c-138">256</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-139">Conferencing_Announcement_Service_1.0</span><span class="sxs-lookup"><span data-stu-id="0dc5c-139">Conferencing_Announcement_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-140">ENTIDAD</span><span class="sxs-lookup"><span data-stu-id="0dc5c-140">CAS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-141">512</span><span class="sxs-lookup"><span data-stu-id="0dc5c-141">512</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-142">Conferencing_Attendant_1.0</span><span class="sxs-lookup"><span data-stu-id="0dc5c-142">Conferencing_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-143">CAA</span><span class="sxs-lookup"><span data-stu-id="0dc5c-143">CAA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-144">512</span><span class="sxs-lookup"><span data-stu-id="0dc5c-144">512</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-145">Conference_Auto_Attendant_1.0</span><span class="sxs-lookup"><span data-stu-id="0dc5c-145">Conference_Auto_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-146">CAA</span><span class="sxs-lookup"><span data-stu-id="0dc5c-146">CAA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-147">1024</span><span class="sxs-lookup"><span data-stu-id="0dc5c-147">1024</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-148">Response_Group_Service</span><span class="sxs-lookup"><span data-stu-id="0dc5c-148">Response_Group_Service</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-149">RGS</span><span class="sxs-lookup"><span data-stu-id="0dc5c-149">RGS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-150">1032</span><span class="sxs-lookup"><span data-stu-id="0dc5c-150">1032</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-151">Call_Park_Service_1.0</span><span class="sxs-lookup"><span data-stu-id="0dc5c-151">Call_Park_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-152">CP</span><span class="sxs-lookup"><span data-stu-id="0dc5c-152">CPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-153">1040</span><span class="sxs-lookup"><span data-stu-id="0dc5c-153">1040</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-154">Response_Group_Service Announcement_Service</span><span class="sxs-lookup"><span data-stu-id="0dc5c-154">Response_Group_Service Announcement_Service</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-155">CUYA</span><span class="sxs-lookup"><span data-stu-id="0dc5c-155">AS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-156">2048</span><span class="sxs-lookup"><span data-stu-id="0dc5c-156">2048</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-157">Microsoft. RTC. Applications. CCS</span><span class="sxs-lookup"><span data-stu-id="0dc5c-157">Microsoft.Rtc.Applications.Ccs</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-158">CCS</span><span class="sxs-lookup"><span data-stu-id="0dc5c-158">CCS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-159">16386</span><span class="sxs-lookup"><span data-stu-id="0dc5c-159">16386</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-160">Notifica</span><span class="sxs-lookup"><span data-stu-id="0dc5c-160">CoMo</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-161">Notifica</span><span class="sxs-lookup"><span data-stu-id="0dc5c-161">CoMo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-162">16387</span><span class="sxs-lookup"><span data-stu-id="0dc5c-162">16387</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-163">CWA</span><span class="sxs-lookup"><span data-stu-id="0dc5c-163">CWA</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-164">CWA</span><span class="sxs-lookup"><span data-stu-id="0dc5c-164">CWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-165">16388</span><span class="sxs-lookup"><span data-stu-id="0dc5c-165">16388</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-166">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="0dc5c-166">InboundRouting</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-167">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="0dc5c-167">InboundRouting</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-168">16389</span><span class="sxs-lookup"><span data-stu-id="0dc5c-168">16389</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-169">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="0dc5c-169">ComoSvc</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-170">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="0dc5c-170">ComoSvc</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-171">16393</span><span class="sxs-lookup"><span data-stu-id="0dc5c-171">16393</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-172">MSExchangeUM</span><span class="sxs-lookup"><span data-stu-id="0dc5c-172">MSExchangeUM</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-173">ExUM</span><span class="sxs-lookup"><span data-stu-id="0dc5c-173">ExUM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-174">16395</span><span class="sxs-lookup"><span data-stu-id="0dc5c-174">16395</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-175">ArchivingAgent</span><span class="sxs-lookup"><span data-stu-id="0dc5c-175">ArchivingAgent</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-176">ARCHAGENT</span><span class="sxs-lookup"><span data-stu-id="0dc5c-176">ARCHAGENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-177">16396</span><span class="sxs-lookup"><span data-stu-id="0dc5c-177">16396</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-178">San</span><span class="sxs-lookup"><span data-stu-id="0dc5c-178">ST</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-179">San</span><span class="sxs-lookup"><span data-stu-id="0dc5c-179">ST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-180">16397</span><span class="sxs-lookup"><span data-stu-id="0dc5c-180">16397</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-181">applicationsharing</span><span class="sxs-lookup"><span data-stu-id="0dc5c-181">applicationsharing</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-182">ASMCU</span><span class="sxs-lookup"><span data-stu-id="0dc5c-182">ASMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-183">16398</span><span class="sxs-lookup"><span data-stu-id="0dc5c-183">16398</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-184">WPLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-184">WPLync</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-185">WPLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-185">WPLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-186">16399</span><span class="sxs-lookup"><span data-stu-id="0dc5c-186">16399</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-187">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-187">iPhoneLync</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-188">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-188">iPhoneLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-189">16400</span><span class="sxs-lookup"><span data-stu-id="0dc5c-189">16400</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-190">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-190">AndroidLync</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-191">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-191">AndroidLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-192">16401</span><span class="sxs-lookup"><span data-stu-id="0dc5c-192">16401</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-193">iPadLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-193">iPadLync</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-194">iPadLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-194">iPadLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-195">16402</span><span class="sxs-lookup"><span data-stu-id="0dc5c-195">16402</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-196">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-196">NokiaLync</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-197">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="0dc5c-197">NokiaLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-198">16403</span><span class="sxs-lookup"><span data-stu-id="0dc5c-198">16403</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-199">LyncImm</span><span class="sxs-lookup"><span data-stu-id="0dc5c-199">LyncImm</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-200">LyncImm</span><span class="sxs-lookup"><span data-stu-id="0dc5c-200">LyncImm</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-201">16404</span><span class="sxs-lookup"><span data-stu-id="0dc5c-201">16404</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-202">INFORMÁTICO</span><span class="sxs-lookup"><span data-stu-id="0dc5c-202">PCS</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-203">INFORMÁTICO</span><span class="sxs-lookup"><span data-stu-id="0dc5c-203">PCS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-204">16405</span><span class="sxs-lookup"><span data-stu-id="0dc5c-204">16405</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-205">LWA</span><span class="sxs-lookup"><span data-stu-id="0dc5c-205">LWA</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-206">LWA</span><span class="sxs-lookup"><span data-stu-id="0dc5c-206">LWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-207">16406</span><span class="sxs-lookup"><span data-stu-id="0dc5c-207">16406</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-208">Access</span><span class="sxs-lookup"><span data-stu-id="0dc5c-208">OWA</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-209">Access</span><span class="sxs-lookup"><span data-stu-id="0dc5c-209">OWA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-210">16407</span><span class="sxs-lookup"><span data-stu-id="0dc5c-210">16407</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-211">AOC</span><span class="sxs-lookup"><span data-stu-id="0dc5c-211">AOC</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-212">AOC</span><span class="sxs-lookup"><span data-stu-id="0dc5c-212">AOC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-213">16408</span><span class="sxs-lookup"><span data-stu-id="0dc5c-213">16408</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-214">GCC</span><span class="sxs-lookup"><span data-stu-id="0dc5c-214">GCC</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-215">GCC</span><span class="sxs-lookup"><span data-stu-id="0dc5c-215">GCC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-216">16409</span><span class="sxs-lookup"><span data-stu-id="0dc5c-216">16409</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-217">IMMCU</span><span class="sxs-lookup"><span data-stu-id="0dc5c-217">IMMCU</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-218">IMMCU</span><span class="sxs-lookup"><span data-stu-id="0dc5c-218">IMMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-219">16410</span><span class="sxs-lookup"><span data-stu-id="0dc5c-219">16410</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-220">XmppTGW</span><span class="sxs-lookup"><span data-stu-id="0dc5c-220">XmppTGW</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-221">XmppGateway</span><span class="sxs-lookup"><span data-stu-id="0dc5c-221">XmppGateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc5c-222">32769</span><span class="sxs-lookup"><span data-stu-id="0dc5c-222">32769</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-223">Puerta</span><span class="sxs-lookup"><span data-stu-id="0dc5c-223">Gateway</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-224">Puerta</span><span class="sxs-lookup"><span data-stu-id="0dc5c-224">Gateway</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc5c-225">32770</span><span class="sxs-lookup"><span data-stu-id="0dc5c-225">32770</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-226">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="0dc5c-226">GatewayMediationServerPair</span></span></p></td>
<td><p><span data-ttu-id="0dc5c-227">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="0dc5c-227">GatewayMediationServerPair</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0dc5c-228">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0dc5c-228">


</div>

<span> </span>

</div>

</div>

</span></span></div>

