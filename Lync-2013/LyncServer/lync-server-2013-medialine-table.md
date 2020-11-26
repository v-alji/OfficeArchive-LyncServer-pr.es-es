---
title: 'Lync Server 2013: Tabla MediaLine'
description: 'Lync Server 2013: tabla MediaLine.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine table
ms:assetid: 414b1d63-ae97-4c27-bac0-c9ad0f808ff0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425920(v=OCS.15)
ms:contentKeyID: 48183956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2acea8e14ba0608d9ebf72a48f888bfc4501fae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425622"
---
# <a name="medialine-table-in-lync-server-2013"></a><span data-ttu-id="98c22-103">Tabla MediaLine en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98c22-103">MediaLine table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98c22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98c22-104">

<span> </span></span></span>

<span data-ttu-id="98c22-105">_**Última modificación del tema:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="98c22-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="98c22-106">Cada registro representa una línea de medios.</span><span class="sxs-lookup"><span data-stu-id="98c22-106">Each record represents one media line.</span></span> <span data-ttu-id="98c22-107">(Una sesión de audio normalmente contiene una línea multimedia de audio.</span><span class="sxs-lookup"><span data-stu-id="98c22-107">(One audio session usually contains one audio media line.</span></span> <span data-ttu-id="98c22-108">Una sesión de audio y vídeo (A/V) normalmente contiene una línea de medio de audio y una línea de medio de vídeo, aunque la sesión podría contener dos líneas de vídeo si se usa un dispositivo de conferencia o si se usa la vista de galería.</span><span class="sxs-lookup"><span data-stu-id="98c22-108">One audio and video (A/V) session usually contains one audio media line and one video media line, although the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98c22-109"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="98c22-110"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="98c22-111"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="98c22-112"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98c22-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-114">datetime</span><span class="sxs-lookup"><span data-stu-id="98c22-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="98c22-115">Primary</span><span class="sxs-lookup"><span data-stu-id="98c22-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="98c22-116">Se hace referencia a ellos desde la <a href="lync-server-2013-session-table.md">tabla sesión en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-116">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-118">int</span><span class="sxs-lookup"><span data-stu-id="98c22-118">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-119">Primary</span><span class="sxs-lookup"><span data-stu-id="98c22-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="98c22-120">Se hace referencia a ellos desde la <a href="lync-server-2013-session-table.md">tabla sesión en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-120">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-121"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-121"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-122">tinyint</span><span class="sxs-lookup"><span data-stu-id="98c22-122">tinyint</span></span></p></td>
<td><p><span data-ttu-id="98c22-123">Primary</span><span class="sxs-lookup"><span data-stu-id="98c22-123">Primary</span></span></p></td>
<td><p><span data-ttu-id="98c22-124">0 es el audio principal, 1 es el vídeo principal y 2 es vídeo panorámico, 3 es uso compartido de aplicaciones y escritorio.</span><span class="sxs-lookup"><span data-stu-id="98c22-124">0 is main audio, 1 is main video, and 2 is panoramic video, 3 is Application/Desktop Sharing.</span></span> <span data-ttu-id="98c22-125">Esta etiqueta debe ser única dentro de una sola sesión.</span><span class="sxs-lookup"><span data-stu-id="98c22-125">This label must be unique within a single session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-126"><strong>ConnectivityIce</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-126"><strong>ConnectivityIce</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-127">tinyint</span><span class="sxs-lookup"><span data-stu-id="98c22-127">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-128">Esta columna está presente pero no se usa en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-128">This column is present but not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="98c22-129">La información sobre la conectividad usada para una línea de medios se captura en las columnas CallerConnectivityICE y CalleeConnectivityICE.</span><span class="sxs-lookup"><span data-stu-id="98c22-129">Information about the connectivity used for a media line is captured in the CallerConnectivityICE and CalleeConnectivityICE columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-130"><strong>CallerIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-130"><strong>CallerIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-131">int</span><span class="sxs-lookup"><span data-stu-id="98c22-131">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-132">Información sobre el proceso de establecimiento de conectividad interactiva (ICE) descrito en marcas de bits.</span><span class="sxs-lookup"><span data-stu-id="98c22-132">Information about Interactive Connectivity Establishment (ICE) process described in bits flags.</span></span> <span data-ttu-id="98c22-133">Para obtener más información, consulte la <em>especificación de protocolo de servidor calidad de la supervisión</em>, disponible para descargar.</span><span class="sxs-lookup"><span data-stu-id="98c22-133">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-134"><strong>CalleeIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-134"><strong>CalleeIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-135">int</span><span class="sxs-lookup"><span data-stu-id="98c22-135">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-136">Igual que CallerIceWarningFlags, pero en el lado del destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-136">Same as CallerIceWarningFlags, but on the callee side.</span></span> <span data-ttu-id="98c22-137">Para obtener más información, consulte la <em>especificación de protocolo de servidor calidad de la supervisión</em>, disponible para descargar.</span><span class="sxs-lookup"><span data-stu-id="98c22-137">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-138"><strong>Seguridad</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-138"><strong>Security</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-139">tinyint</span><span class="sxs-lookup"><span data-stu-id="98c22-139">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-140">Perfil de seguridad en uso.</span><span class="sxs-lookup"><span data-stu-id="98c22-140">The security profile in use.</span></span> <span data-ttu-id="98c22-141">0 es ninguno, 1 es SRTP, 2 es v1.</span><span class="sxs-lookup"><span data-stu-id="98c22-141">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-142"><strong>Transport</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-142"><strong>Transport</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-143">tinyint</span><span class="sxs-lookup"><span data-stu-id="98c22-143">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-144">0 es UDP, 1 es TCP.</span><span class="sxs-lookup"><span data-stu-id="98c22-144">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-145"><strong>CallerIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-145"><strong>CallerIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-146">int</span><span class="sxs-lookup"><span data-stu-id="98c22-146">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-147">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-148">Dirección IP del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-148">IP Address of the caller.</span></span> <span data-ttu-id="98c22-149">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="98c22-149">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-150"><strong>CallerPort</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-150"><strong>CallerPort</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-151">int</span><span class="sxs-lookup"><span data-stu-id="98c22-151">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-152">Puerto usado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-152">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-153"><strong>CallerSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-153"><strong>CallerSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-154">int</span><span class="sxs-lookup"><span data-stu-id="98c22-154">int</span></span></p></td>
<td><p> <span data-ttu-id="98c22-155">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-156">La subred de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="98c22-156">The subnet of the caller.</span></span> <span data-ttu-id="98c22-157">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="98c22-157">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-158"><strong>CallerInside</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-158"><strong>CallerInside</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-159">bit</span><span class="sxs-lookup"><span data-stu-id="98c22-159">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-160">1 significa que la persona que llama está dentro de la red de la empresa, 0 significa que la persona que llama está fuera de la red.</span><span class="sxs-lookup"><span data-stu-id="98c22-160">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-161"><strong>CallerMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-161"><strong>CallerMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-162">int</span><span class="sxs-lookup"><span data-stu-id="98c22-162">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-163">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-164">Dirección Mac de la persona que llama, a la que se hace referencia desde la <a href="lync-server-2013-macaddress-table.md">tabla MacAddress en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-164">Caller’s mac address, referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-165"><strong>CallerRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-165"><strong>CallerRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-166">int</span><span class="sxs-lookup"><span data-stu-id="98c22-166">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-167">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-167">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-168">Dirección IP del servicio perimetral de Lync Server A/V que usa el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-168">IP Address of the Lync Server A/V Edge service used by the caller.</span></span> <span data-ttu-id="98c22-169">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="98c22-169">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-170"><strong>CallerRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-170"><strong>CallerRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-171">int</span><span class="sxs-lookup"><span data-stu-id="98c22-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-172">Puerto usado en el servicio de borde de A/V por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-172">Port used on the A/V Edge service by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-173"><strong>CallerCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-173"><strong>CallerCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-174">int</span><span class="sxs-lookup"><span data-stu-id="98c22-174">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-175">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-176">Dispositivo de captura usado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-176">Capture device used by the caller.</span></span> <span data-ttu-id="98c22-177">Se hace referencia a ellos desde la <a href="lync-server-2013-device-table.md">tabla de dispositivos en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-177">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-178"><strong>CallerRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-178"><strong>CallerRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-179">int</span><span class="sxs-lookup"><span data-stu-id="98c22-179">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-180">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-180">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-181">Dispositivo de representación usado por la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="98c22-181">Render device used by caller.</span></span> <span data-ttu-id="98c22-182">Se hace referencia a ellos desde la <a href="lync-server-2013-device-table.md">tabla de dispositivos en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-182">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-183"><strong>CallerCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-183"><strong>CallerCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-184">int</span><span class="sxs-lookup"><span data-stu-id="98c22-184">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-185">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-186">Controlador para el dispositivo de captura de la persona que llama, al que se hace referencia desde la <a href="lync-server-2013-devicedriver-table.md">tabla DeviceDriver en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-186">Driver for the caller’s capture device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-187"><strong>CallerRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-187"><strong>CallerRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-188">int</span><span class="sxs-lookup"><span data-stu-id="98c22-188">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-189">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-189">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-190">Controlador del dispositivo de representación de la persona que llama, al que se hace referencia desde la <a href="lync-server-2013-devicedriver-table.md">tabla DeviceDriver en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-190">Driver for the caller’s render device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-191"><strong>CallerNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-191"><strong>CallerNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="98c22-192">tinyint</span></span></p></td>
<td><p><span data-ttu-id="98c22-193">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-194">Indica cómo se conectó a la red.</span><span class="sxs-lookup"><span data-stu-id="98c22-194">Indicates how the caller connected to the network.</span></span> <span data-ttu-id="98c22-195">Los valores se obtienen de la <a href="lync-server-2013-networkconnectiondetail-table.md">tabla NetworkConnectionDetail en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-195">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="98c22-196">Los valores típicos son 0 para una conexión cableada ' 1 para una conexión WiFi; y 3 para una conexión Ethernet.</span><span class="sxs-lookup"><span data-stu-id="98c22-196">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-197"><strong>CallerBssid</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-197"><strong>CallerBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-198">int</span><span class="sxs-lookup"><span data-stu-id="98c22-198">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-199">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-200">BSSID del autor de la llamada si se usa una conexión inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="98c22-200">Caller’s BSSID if wireless is used.</span></span> <span data-ttu-id="98c22-201">Se hace referencia desde la <a href="lync-server-2013-macaddress-table.md">tabla MacAddress en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-201">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-202"><strong>CallerVPN</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-202"><strong>CallerVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-203">bit</span><span class="sxs-lookup"><span data-stu-id="98c22-203">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="98c22-204">Vínculo de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="98c22-204">The caller's link.</span></span> <span data-ttu-id="98c22-205">1 es una red privada virtual (VPN) y 0 no es una VPN.</span><span class="sxs-lookup"><span data-stu-id="98c22-205">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-206"><strong>CallerLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-206"><strong>CallerLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-207">decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="98c22-207">decimal(18,0)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="98c22-208">La velocidad del vínculo de red, en bps, para el punto final de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-208">The network link speed, in bps, for the caller's endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-209"><strong>CalleeIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-209"><strong>CalleeIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-210">int</span><span class="sxs-lookup"><span data-stu-id="98c22-210">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-211">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-211">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-212">Dirección IP del receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-212">IP Address of the call receiver.</span></span> <span data-ttu-id="98c22-213">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="98c22-213">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-214"><strong>CalleePort</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-214"><strong>CalleePort</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-215">bit</span><span class="sxs-lookup"><span data-stu-id="98c22-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="98c22-216">Puerto usado por el receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-216">Port used by the call receiver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-217"><strong>CalleeSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-217"><strong>CalleeSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-218">int</span><span class="sxs-lookup"><span data-stu-id="98c22-218">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-219">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-220">Subred del destinatario de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-220">Subnet of callee.</span></span> <span data-ttu-id="98c22-221">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="98c22-221">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-222"><strong>CalleeInside</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-222"><strong>CalleeInside</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-223">bit</span><span class="sxs-lookup"><span data-stu-id="98c22-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-224">1 significa que el receptor de llamadas está dentro de la red empresarial, 0 significa que el receptor de la llamada está fuera de la red.</span><span class="sxs-lookup"><span data-stu-id="98c22-224">1 means call receiver is inside the enterprise network, 0 means the call receiver is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-225"><strong>CalleeMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-225"><strong>CalleeMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-226">int</span><span class="sxs-lookup"><span data-stu-id="98c22-226">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-227">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-227">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-228">Dirección Mac de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-228">Callee Mac address.</span></span> <span data-ttu-id="98c22-229">Se hace referencia a ellos desde la <a href="lync-server-2013-macaddress-table.md">tabla MacAddress en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-229">Referenced from the <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-230"><strong>CalleeRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-230"><strong>CalleeRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-231">int</span><span class="sxs-lookup"><span data-stu-id="98c22-231">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-232">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-232">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-233">Dirección IP del servicio perimetral A/V que usa el receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-233">IP Address of the A/V Edge service used by the call receiver.</span></span> <span data-ttu-id="98c22-234">Para obtener más información, consulte la <a href="lync-server-2013-ipaddress-table.md">tabla IPAddress en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="98c22-234">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-235"><strong>CalleeRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-235"><strong>CalleeRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-236">int</span><span class="sxs-lookup"><span data-stu-id="98c22-236">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-237">Puerto usado en el servicio de borde A/V por el receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-237">Port used on the A/V Edge Service by the call receiver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-238"><strong>CalleeCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-238"><strong>CalleeCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-239">int</span><span class="sxs-lookup"><span data-stu-id="98c22-239">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-240">extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-240">foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-241">Dispositivo de captura usado por el receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-241">Capture device used by the call receiver.</span></span> <span data-ttu-id="98c22-242">Se hace referencia a ellos desde la <a href="lync-server-2013-device-table.md">tabla de dispositivos en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-242">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-243"><strong>CalleeRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-243"><strong>CalleeRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-244">int</span><span class="sxs-lookup"><span data-stu-id="98c22-244">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-245">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-245">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-246">Dispositivo de representación usado por el receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-246">Render device used by the call receiver.</span></span> <span data-ttu-id="98c22-247">Se hace referencia a ellos desde la <a href="lync-server-2013-device-table.md">tabla de dispositivos en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-247">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-248"><strong>CalleeCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-248"><strong>CalleeCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-249">int</span><span class="sxs-lookup"><span data-stu-id="98c22-249">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-250">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-250">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-251">Controlador para el dispositivo de captura del receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-251">Driver for the call receiver’s capture device.</span></span> <span data-ttu-id="98c22-252">Se hace referencia a partir de la <a href="lync-server-2013-devicedriver-table.md">tabla DeviceDriver en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-252">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-253"><strong>CalleeRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-253"><strong>CalleeRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-254">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="98c22-254">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="98c22-255">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-255">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-256">Controlador del dispositivo de representación del receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-256">Driver for the call receiver’s render device.</span></span> <span data-ttu-id="98c22-257">Se hace referencia a partir de la <a href="lync-server-2013-devicedriver-table.md">tabla DeviceDriver en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-257">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-258"><strong>CalleeNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-258"><strong>CalleeNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-259">tinyint</span><span class="sxs-lookup"><span data-stu-id="98c22-259">tinyint</span></span></p></td>
<td><p><span data-ttu-id="98c22-260">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-260">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-261">Indica cómo el destinatario de la llamada está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="98c22-261">Indicates how the callee connected to the network.</span></span> <span data-ttu-id="98c22-262">Los valores se obtienen de la <a href="lync-server-2013-networkconnectiondetail-table.md">tabla NetworkConnectionDetail en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-262">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="98c22-263">Los valores típicos son 0 para una conexión cableada ' 1 para una conexión WiFi; y 3 para una conexión Ethernet.</span><span class="sxs-lookup"><span data-stu-id="98c22-263">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-264"><strong>CalleeBssid</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-264"><strong>CalleeBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-265">int</span><span class="sxs-lookup"><span data-stu-id="98c22-265">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-266">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-266">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-267">BSSID del destinatario de la llamada si se usa la tecnología inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="98c22-267">Callee’s BSSID if wireless is used.</span></span> <span data-ttu-id="98c22-268">Se hace referencia desde la <a href="lync-server-2013-macaddress-table.md">tabla MacAddress en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-268">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-269"><strong>CalleeVPN</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-269"><strong>CalleeVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-270">bit</span><span class="sxs-lookup"><span data-stu-id="98c22-270">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-271">Vínculo del receptor de la llamada; 1 es una red privada virtual (VPN) y 0 no es una VPN.</span><span class="sxs-lookup"><span data-stu-id="98c22-271">The call receiver’s link; 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-272"><strong>CalleeLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-272"><strong>CalleeLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-273">decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="98c22-273">decimal(18,0)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-274">La velocidad del vínculo de red, en bps, para el extremo del receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-274">The network link speed, in bps, for the call receiver’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-275"><strong>ConversationalMOS</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-275"><strong>ConversationalMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-276">decimal (3, 2)</span><span class="sxs-lookup"><span data-stu-id="98c22-276">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-277">OP de banda estrecha de las sesiones de audio (basadas en ambas secuencias de audio).</span><span class="sxs-lookup"><span data-stu-id="98c22-277">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-278"><strong>AppliedBandwidthLimit</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-278"><strong>AppliedBandwidthLimit</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-279">int</span><span class="sxs-lookup"><span data-stu-id="98c22-279">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="98c22-280">Este es el ancho de banda real aplicado a la transmisión de la parte de envío proporcionada, que proporciona varias configuraciones de directiva (TURN, API, SDP, Policy Server, etc.).</span><span class="sxs-lookup"><span data-stu-id="98c22-280">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="98c22-281">Esto no se debe confundir con el ancho de banda efectivo porque puede haber un ancho de banda más bajo según el cálculo de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="98c22-281">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="98c22-282">Básicamente, este es el ancho de banda máximo que la secuencia de envío puede tomar límites de bloqueo impuestas por la estimación del ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="98c22-282">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-283"><strong>AppliedBandwidthSourceKey</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-283"><strong>AppliedBandwidthSourceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-284">smallint</span><span class="sxs-lookup"><span data-stu-id="98c22-284">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="98c22-285">Este es el origen del límite de ancho de banda que se impone.</span><span class="sxs-lookup"><span data-stu-id="98c22-285">This is the source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="98c22-286">Describe dónde viene el límite de ancho de banda ("servidor de directivas", "TURN Server", "Modación", etc.).</span><span class="sxs-lookup"><span data-stu-id="98c22-286">It describes where the bandwidth limit is coming from (“Policy Server”, “TURN Server”, “Modality”, and so on).</span></span> <span data-ttu-id="98c22-287">Se hace referencia a ellos desde la <a href="lync-server-2013-appliedbandwidthsource-table.md">tabla AppliedBandwidthSource en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="98c22-287">Referenced from the <a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-288"><strong>Autor de llamada</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-288"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-289">bit</span><span class="sxs-lookup"><span data-stu-id="98c22-289">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-290">Indica si se recibieron las métricas de la persona que llama; 1 es sí, un valor nulo es no.</span><span class="sxs-lookup"><span data-stu-id="98c22-290">Indicates whether metrics from the caller were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-291"><strong>Destinatario de la llamada</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-291"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-292">bit</span><span class="sxs-lookup"><span data-stu-id="98c22-292">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="98c22-293">Indica si se han recibido métricas del receptor de la llamada; 1 es sí, un valor nulo es no.</span><span class="sxs-lookup"><span data-stu-id="98c22-293">Indicates whether metrics from the call receiver were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-294"><strong>MidCallReport</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-294"><strong>MidCallReport</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-295">bit</span><span class="sxs-lookup"><span data-stu-id="98c22-295">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="98c22-296">Indica si el informe es para una parte de la sesión o para la sesión completa.</span><span class="sxs-lookup"><span data-stu-id="98c22-296">Indicates whether the report is for a portion of the session or for the complete session.</span></span></p>
<p><span data-ttu-id="98c22-297">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-297">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-298"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-298"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-299">bit</span><span class="sxs-lookup"><span data-stu-id="98c22-299">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="98c22-300">Indica si una llamada se ha clasificado como una llamada deficiente (valor de 1) o como una buena llamada (0).</span><span class="sxs-lookup"><span data-stu-id="98c22-300">Indicates whether a call was classified as a poor call (value of 1) or as a good call (0).</span></span></p>
<p><span data-ttu-id="98c22-301">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-302"><strong>CallerConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-302"><strong>CallerConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-303">tinyInt</span><span class="sxs-lookup"><span data-stu-id="98c22-303">tinyInt</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="98c22-304">Indica si la persona que llama se ha conectado a la red mediante el protocolo ICE (establecimiento de conectividad de Internet).</span><span class="sxs-lookup"><span data-stu-id="98c22-304">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="98c22-305">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-305">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-306"><strong>CalleeConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-306"><strong>CalleeConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-307">tinyint</span><span class="sxs-lookup"><span data-stu-id="98c22-307">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="98c22-308">Indica si la persona que llama se ha conectado a la red mediante el protocolo ICE (establecimiento de conectividad de Internet).</span><span class="sxs-lookup"><span data-stu-id="98c22-308">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="98c22-309">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-309">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-310"><strong>CallerReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-310"><strong>CallerReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-311">int</span><span class="sxs-lookup"><span data-stu-id="98c22-311">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-312">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-312">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-313">Dirección IP reflexiva del usuario que realizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-313">Reflexive IP address of the user who placed the call.</span></span> <span data-ttu-id="98c22-314">En las organizaciones que usan NAT (traducción de direcciones de red), la dirección IP reflexiva es la dirección IP del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="98c22-314">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="98c22-315">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-315">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-316"><strong>CallerWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-316"><strong>CallerWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-317">int</span><span class="sxs-lookup"><span data-stu-id="98c22-317">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-318">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-318">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-319">Descripción del dispositivo para el controlador WiFi empleado por el usuario que realizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-319">Device description for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="98c22-320">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-321"><strong>CallerWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-321"><strong>CallerWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-322">int</span><span class="sxs-lookup"><span data-stu-id="98c22-322">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-323">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-323">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-324">Número de versión del controlador WiFi empleado por el usuario que realizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-324">Version number for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="98c22-325">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-326"><strong>CalleReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-326"><strong>CalleReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-327">int</span><span class="sxs-lookup"><span data-stu-id="98c22-327">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-328">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-328">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-329">Dirección IP reflexiva del usuario que recibió la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-329">Reflexive IP address of the user who received the call.</span></span> <span data-ttu-id="98c22-330">En las organizaciones que usan NAT (traducción de direcciones de red), la dirección IP reflexiva es la dirección IP del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="98c22-330">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="98c22-331">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98c22-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-333">int</span><span class="sxs-lookup"><span data-stu-id="98c22-333">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-334">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-334">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-335">Descripción del dispositivo para el controlador WiFi empleado por el usuario que recibió la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-335">Device description for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="98c22-336">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-336">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98c22-337"><strong>CalleeWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="98c22-337"><strong>CalleeWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="98c22-338">int</span><span class="sxs-lookup"><span data-stu-id="98c22-338">int</span></span></p></td>
<td><p><span data-ttu-id="98c22-339">Extranjero</span><span class="sxs-lookup"><span data-stu-id="98c22-339">Foreign</span></span></p></td>
<td><p><span data-ttu-id="98c22-340">Número de versión del controlador WiFi empleado por el usuario que recibió la llamada.</span><span class="sxs-lookup"><span data-stu-id="98c22-340">Version number for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="98c22-341">Esta columna se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c22-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="98c22-342">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98c22-342">


</div>

<span> </span>

</div>

</div>

</span></span></div>

