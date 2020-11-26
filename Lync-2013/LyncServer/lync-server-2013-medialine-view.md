---
title: 'Lync Server 2013: vista MediaLine'
description: 'Lync Server 2013: vista MediaLine.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine view
ms:assetid: 132eca13-8913-4218-9eff-4960ced8c3dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687972(v=OCS.15)
ms:contentKeyID: 49733560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c61fcc15b46958622e6cddd66427255a6def154
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445949"
---
# <a name="medialine-view-in-lync-server-2013"></a><span data-ttu-id="ebfe1-103">Vista MediaLine en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebfe1-103">MediaLine view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ebfe1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ebfe1-104">

<span> </span></span></span>

<span data-ttu-id="ebfe1-105">_**Última modificación del tema:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="ebfe1-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="ebfe1-106">La vista MediaLine almacena información acerca de cada línea de medios de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-106">The MediaLine View stores information about each media line in the database.</span></span> <span data-ttu-id="ebfe1-107">Una sesión de audio normalmente contiene una línea multimedia de audio.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-107">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="ebfe1-108">Una sesión de audio y vídeo (A/V) normalmente contiene una línea de medio de audio y una línea de medio de vídeo; sin embargo, la sesión podría contener dos líneas multimedia de vídeo si se usa un dispositivo de conferencia o si se usa la vista de galería.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-108">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span> <span data-ttu-id="ebfe1-109">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebfe1-110">Columna</span><span class="sxs-lookup"><span data-stu-id="ebfe1-110">Column</span></span></th>
<th><span data-ttu-id="ebfe1-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ebfe1-111">Data Type</span></span></th>
<th><span data-ttu-id="ebfe1-112">sobre</span><span class="sxs-lookup"><span data-stu-id="ebfe1-112">details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-113">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="ebfe1-113">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-114">datetime</span><span class="sxs-lookup"><span data-stu-id="ebfe1-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-115">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-116">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="ebfe1-116">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-117">int</span><span class="sxs-lookup"><span data-stu-id="ebfe1-117">int</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-118">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-118">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-119">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="ebfe1-119">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-120">tinyint</span><span class="sxs-lookup"><span data-stu-id="ebfe1-120">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-121">Se hace referencia a ellos desde la <a href="lync-server-2013-medialine-table.md">tabla MediaLine en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-121">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-122">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="ebfe1-122">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-123">int</span><span class="sxs-lookup"><span data-stu-id="ebfe1-123">int</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-124">Información sobre el proceso de establecimiento de conectividad interactiva (ICE) descrito en indicadores de bits para la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-124">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="ebfe1-125">Para obtener más información, consulte la especificación de protocolo de servidor de supervisión de la calidad de la experiencia.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-125">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-126">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="ebfe1-126">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-127">int</span><span class="sxs-lookup"><span data-stu-id="ebfe1-127">int</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-128">Información sobre el proceso de establecimiento de conectividad interactiva (ICE) descrito en marcas de bits para el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-128">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="ebfe1-129">Para obtener más información, consulte la especificación de protocolo de servidor de supervisión de la calidad de la experiencia.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-129">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-130">Seguridad</span><span class="sxs-lookup"><span data-stu-id="ebfe1-130">Security</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-131">tinyint</span><span class="sxs-lookup"><span data-stu-id="ebfe1-131">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-132">Perfil de seguridad en uso.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-132">Security profile in use.</span></span> <span data-ttu-id="ebfe1-133">0 es ninguno, 1 es SRTP, 2 es v1.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-133">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-134">Transport</span><span class="sxs-lookup"><span data-stu-id="ebfe1-134">Transport</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-135">tinyint</span><span class="sxs-lookup"><span data-stu-id="ebfe1-135">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-136">Tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-136">Transport type.</span></span> <span data-ttu-id="ebfe1-137">0 es UDP, 1 es TCP.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-137">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-138">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="ebfe1-138">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-139">var (50)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-139">var(50)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-140">Dirección IP del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-140">IP address of the caller.</span></span> <span data-ttu-id="ebfe1-141">Puede ser una dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-141">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-142">CallerPort</span><span class="sxs-lookup"><span data-stu-id="ebfe1-142">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-143">int</span><span class="sxs-lookup"><span data-stu-id="ebfe1-143">int</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-144">Puerto usado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-144">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-145">CallerInside</span><span class="sxs-lookup"><span data-stu-id="ebfe1-145">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-146">bit</span><span class="sxs-lookup"><span data-stu-id="ebfe1-146">bit</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-147">Indica si el autor de la llamada está dentro de la red de la organización.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-147">Indicates whether or not the caller is inside the organization network.</span></span> <span data-ttu-id="ebfe1-148">1 significa que la persona que llama está dentro de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-148">1 means that the caller is inside the enterprise network.</span></span> <span data-ttu-id="ebfe1-149">0 significa que la persona que llama está fuera de la red.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-149">0 means that the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-150">CallerMacAddress</span><span class="sxs-lookup"><span data-stu-id="ebfe1-150">CallerMacAddress</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-151">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-151">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-152">Dirección MAC de la interfaz de red que llama.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-152">MAC address of network interface used by caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-153">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="ebfe1-153">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-154">var (50)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-154">var(50)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-155">Dirección IP del servicio perimetral A/V que usa el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-155">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="ebfe1-156">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ebfe1-156">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-157">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="ebfe1-157">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-158">int</span><span class="sxs-lookup"><span data-stu-id="ebfe1-158">int</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-159">Puerto usado en el servicio perimetral A/V usado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-159">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-160">CallerReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="ebfe1-160">CallerReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-161">var (50)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-161">var(50)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-162">Dirección IP de la persona que llama según el servicio perimetral de A/V.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-162">Caller’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="ebfe1-163">Esta dirección puede ser diferente de la CallerIPAddr si el cliente se encuentra detrás de un NAT, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-163">This address may be different that the CallerIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-164">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="ebfe1-164">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-165">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-165">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-166">Nombre del dispositivo de captura del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-166">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-167">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="ebfe1-167">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-168">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-168">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-169">Nombre del dispositivo de representación del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-169">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-170">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="ebfe1-170">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-171">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-171">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-172">Nombre del controlador del dispositivo de captura del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-172">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-173">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="ebfe1-173">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-174">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-174">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-175">Nombre del controlador del dispositivo de representación del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-175">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-176">CallerWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="ebfe1-176">CallerWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-177">VARCHAR (256</span><span class="sxs-lookup"><span data-stu-id="ebfe1-177">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-178">Descripción del controlador WIFI del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-178">Caller’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-179">CallerWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="ebfe1-179">CallerWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-180">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-180">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-181">Versión del controlador WIFI del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-181">Caller’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-182">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="ebfe1-182">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-183">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-183">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-184">Detalles de la conexión de red de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-184">Details of caller’s network connection.</span></span> <span data-ttu-id="ebfe1-185">Para obtener más información, consulte la <a href="lync-server-2013-networkconnectiondetail-table.md">tabla NetworkConnectionDetail en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ebfe1-185">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-186">CallerBssid</span><span class="sxs-lookup"><span data-stu-id="ebfe1-186">CallerBssid</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-187">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-187">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-188">Identificador del conjunto de servicios básicos usado por las personas que llaman conexión WiFi.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-188">Basic Service Set Identifier used by callers WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-189">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="ebfe1-189">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-190">bit</span><span class="sxs-lookup"><span data-stu-id="ebfe1-190">bit</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-191">Indica si la persona que llama se ha conectado a través de una red privada virtual.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-191">Indicates whether the caller connected over a virtual private network.</span></span> <span data-ttu-id="ebfe1-192">1 es una red privada virtual (VPN) y 0 no es una VPN.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-192">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-193">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="ebfe1-193">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-194">var (50)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-194">var(50)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-195">Dirección IP del destinatario.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-195">IP address of the callee.</span></span> <span data-ttu-id="ebfe1-196">Puede ser una dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-196">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-197">CalleePort</span><span class="sxs-lookup"><span data-stu-id="ebfe1-197">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-198">int</span><span class="sxs-lookup"><span data-stu-id="ebfe1-198">int</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-199">Puerto usado por el destinatario.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-199">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-200">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="ebfe1-200">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-201">bit</span><span class="sxs-lookup"><span data-stu-id="ebfe1-201">bit</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-202">Indica si el destinatario de la llamada está dentro de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-202">Indicates whether the callee is inside the enterprise network.</span></span> <span data-ttu-id="ebfe1-203">1 significa que el destinatario de la llamada está dentro de la red de la empresa, 0 significa que el destinatario de la llamada está fuera de la red.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-203">1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-204">CalleeMacAddress</span><span class="sxs-lookup"><span data-stu-id="ebfe1-204">CalleeMacAddress</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-205">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-205">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-206">Dirección MAC de la interfaz de red que usa el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-206">MAC address of network interface used by callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-207">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="ebfe1-207">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-208">var (50)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-208">var(50)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-209">Dirección IP del servicio perimetral A/V que usa el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-209">IP Address of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="ebfe1-210">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ebfe1-210">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-211">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="ebfe1-211">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-212">int</span><span class="sxs-lookup"><span data-stu-id="ebfe1-212">int</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-213">Puerto usado en el servicio de borde A/V que usa el destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-213">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-214">CalleeReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="ebfe1-214">CalleeReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-215">var (50)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-215">var(50)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-216">Dirección IP del destinatario de la llamada tal y como lo indica el servicio A/V Edge.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-216">Callee’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="ebfe1-217">Esta dirección puede ser diferente de la CalleeIPAddr si el cliente se encuentra detrás de un NAT, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-217">This address may be different that the CalleeIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-218">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="ebfe1-218">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-219">var (50)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-219">var(50)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-220">Nombre del dispositivo de captura de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-220">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-221">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="ebfe1-221">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-222">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-222">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-223">Nombre del dispositivo de representación de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-223">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-224">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="ebfe1-224">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-225">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-225">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-226">Nombre del controlador del dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-226">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-227">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="ebfe1-227">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-228">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-228">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-229">Nombre del controlador del dispositivo de representación de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-229">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-230">CalleeWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="ebfe1-230">CalleeWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-231">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-231">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-232">Descripción del controlador WIFI de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-232">Callee’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-233">CalleeWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="ebfe1-233">CalleeWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-234">VARCHAR (256</span><span class="sxs-lookup"><span data-stu-id="ebfe1-234">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-235">Versión del controlador WIFI de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-235">Callee’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-236">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="ebfe1-236">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-237">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-237">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-238">Detalles de la conexión de red de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-238">Details of callee’s network connection.</span></span> <span data-ttu-id="ebfe1-239">Para obtener más información, consulte la <a href="lync-server-2013-networkconnectiondetail-table.md">tabla NetworkConnectionDetail en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ebfe1-239">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-240">CalleeBssid</span><span class="sxs-lookup"><span data-stu-id="ebfe1-240">CalleeBssid</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-241">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-241">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-242">Identificador del conjunto de servicios básicos usado por la conexión WiFi de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-242">Basic Service Set Identifier used by callee’s WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-243">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="ebfe1-243">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-244">bit</span><span class="sxs-lookup"><span data-stu-id="ebfe1-244">bit</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-245">Indica si el destinatario de la llamada se conecta a través de una red privada virtual.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-245">Indicates whether the callee connected over a virtual private network.</span></span> <span data-ttu-id="ebfe1-246">1 es una red privada virtual (VPN) y 0 no es una VPN.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-246">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-247">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="ebfe1-247">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-248">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-248">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-249">OP de banda estrecha de las sesiones de audio (basadas en ambas secuencias de audio).</span><span class="sxs-lookup"><span data-stu-id="ebfe1-249">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-250">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="ebfe1-250">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-251">int</span><span class="sxs-lookup"><span data-stu-id="ebfe1-251">int</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-252">Este es el ancho de banda real que se aplica a la transmisión de la parte de envío proporcionada, dadas varias configuraciones de directiva (TURN, API, SDP, Policy Server, etc.).</span><span class="sxs-lookup"><span data-stu-id="ebfe1-252">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, etc.).</span></span> <span data-ttu-id="ebfe1-253">Esto no debe confundirse con el ancho de banda efectivo porque puede haber un ancho de banda más bajo en función de la estimación del ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-253">This should not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="ebfe1-254">Básicamente, este es el ancho de banda máximo que la secuencia de envío puede tomar límites de bloqueo impuestas por la estimación del ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-254">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-255">AppliedBandwidthSource</span><span class="sxs-lookup"><span data-stu-id="ebfe1-255">AppliedBandwidthSource</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-256">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="ebfe1-256">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-257">Origen del límite de ancho de banda que se impone.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-257">Source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="ebfe1-258">Describe de dónde viene el límite de ancho de banda (por ejemplo, "servidor de directivas", "convertir servidor" o "modalidad de moda").</span><span class="sxs-lookup"><span data-stu-id="ebfe1-258">It describes where the bandwidth limit is coming from (for example, “Policy Server”, “TURN Server”, or “Modality”).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-259">Autor de llamada</span><span class="sxs-lookup"><span data-stu-id="ebfe1-259">Caller</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-260">bit</span><span class="sxs-lookup"><span data-stu-id="ebfe1-260">bit</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-261">Indica si se recibieron las métricas de la persona que llama; 1 es sí, 0 es no.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-261">Indicates whether metrics from the caller were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-262">Destinatario de la llamada</span><span class="sxs-lookup"><span data-stu-id="ebfe1-262">Callee</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-263">bit</span><span class="sxs-lookup"><span data-stu-id="ebfe1-263">bit</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-264">Indica si se han recibido métricas del receptor de la llamada; 1 es sí, 0 es no.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-264">Indicates whether metrics from the call receiver were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-265">MidCallReport</span><span class="sxs-lookup"><span data-stu-id="ebfe1-265">MidCallReport</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-266">bit</span><span class="sxs-lookup"><span data-stu-id="ebfe1-266">bit</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-267">Indica si el informe es para una parte de la llamada o para la llamada completa.</span><span class="sxs-lookup"><span data-stu-id="ebfe1-267">Indicates whether the report is for a portion of the call or for the complete call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-268">ClassifiedPoorCall</span><span class="sxs-lookup"><span data-stu-id="ebfe1-268">ClassifiedPoorCall</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-269">bit</span><span class="sxs-lookup"><span data-stu-id="ebfe1-269">bit</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-270">Indica si una llamada se ha clasificado como una llamada deficiente (1) o como una buena llamada (0).</span><span class="sxs-lookup"><span data-stu-id="ebfe1-270">Indicates whether a call was classified as a poor call (1) or as a good call (0).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebfe1-271">CallerConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="ebfe1-271">CallerConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-272">tinyint</span><span class="sxs-lookup"><span data-stu-id="ebfe1-272">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-273">Indica si la persona que llama se ha conectado a la red mediante el protocolo ICE (establecimiento de conectividad de Internet).</span><span class="sxs-lookup"><span data-stu-id="ebfe1-273">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebfe1-274">CalleeConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="ebfe1-274">CalleeConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-275">tinyint</span><span class="sxs-lookup"><span data-stu-id="ebfe1-275">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ebfe1-276">Indica si el usuario ha sido llamado conectado a la red mediante el protocolo ICE (establecimiento de conectividad de Internet).</span><span class="sxs-lookup"><span data-stu-id="ebfe1-276">Indicates whether the user called connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ebfe1-277">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ebfe1-277">


</div>

<span> </span>

</div>

</div>

</span></span></div>

