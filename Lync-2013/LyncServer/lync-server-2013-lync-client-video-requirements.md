---
title: 'Lync Server 2013: requisitos de vídeo de cliente de Lync'
description: 'Lync Server 2013: requisitos de vídeo de cliente de Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync client video requirements
ms:assetid: 8f68f4c2-3194-487c-bd2f-fbe71ba8ad70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688132(v=OCS.15)
ms:contentKeyID: 49733731
ms.date: 01/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea1d4a993650ec8102d8b66ea5aa936ad1613f20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426441"
---
# <a name="lync-client-video-requirements-for-lync-server-2013"></a><span data-ttu-id="8195f-103">Requisitos de vídeo de cliente de Lync para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8195f-103">Lync client video requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8195f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8195f-104">

<span> </span></span></span>

<span data-ttu-id="8195f-105">_**Última modificación del tema:** 2016-01-29_</span><span class="sxs-lookup"><span data-stu-id="8195f-105">_**Topic Last Modified:** 2016-01-29_</span></span>

<span data-ttu-id="8195f-106">Esta sección describe la compatibilidad de hardware de vídeo para las videollamadas de Lync 2013 y describe cómo determinar la calidad de video prevista para varias configuraciones de equipos, tabletas y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="8195f-106">This section describes video hardware support for Lync 2013 video calls and describes how to determine the expected video quality for various computer, tablet, and mobile device configurations.</span></span>

<div>

## <a name="windows-desktop-and-tablet-video-requirements-and-capabilities"></a><span data-ttu-id="8195f-107">Requisitos y capacidades de vídeo y escritorio de Windows</span><span class="sxs-lookup"><span data-stu-id="8195f-107">Windows Desktop and Tablet Video Requirements and Capabilities</span></span>

<span data-ttu-id="8195f-108">Lync 2013 incluye aceleración de hardware para la codificación y descodificación de video basadas en el estándar de codificación de video de H. 264/MPEG-4, parte 10.</span><span class="sxs-lookup"><span data-stu-id="8195f-108">Lync 2013 introduces hardware acceleration for video encoding and decoding based on the H.264/MPEG-4 Part 10 Advanced Video Coding standard.</span></span> <span data-ttu-id="8195f-109">Esta característica permite a los equipos con menores velocidades de reloj de CPU codificar y descodificar vídeo de mayor resolución.</span><span class="sxs-lookup"><span data-stu-id="8195f-109">This feature allows computers with lower CPU clock speeds to encode and decode higher resolution video.</span></span> <span data-ttu-id="8195f-110">Los requisitos de hardware de vídeo varían en función de la configuración del equipo y de la resolución de vídeo que se desea.</span><span class="sxs-lookup"><span data-stu-id="8195f-110">Video hardware requirements vary depending on the computer configuration and the video resolution wanted.</span></span>

<div>

## <a name="video-hardware-requirements"></a><span data-ttu-id="8195f-111">Requisitos de hardware de vídeo</span><span class="sxs-lookup"><span data-stu-id="8195f-111">Video Hardware Requirements</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8195f-112">Característica</span><span class="sxs-lookup"><span data-stu-id="8195f-112">Feature</span></span></th>
<th><span data-ttu-id="8195f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8195f-113">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8195f-114">Descodificación H.264 acelerada por hardware mediante DirectX Video Acceleration (DXVA)</span><span class="sxs-lookup"><span data-stu-id="8195f-114">Hardware accelerated H.264 decoding using DirectX Video Acceleration (DXVA)</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8195f-115">La tarjeta gráfica necesita admitir DirectX 9.0 y necesita exponer el modo de descodificación DXVA2_ModeH264_VLD_NoFGT.</span><span class="sxs-lookup"><span data-stu-id="8195f-115">Graphics card must support DirectX 9.0 and must expose the DXVA2_ModeH264_VLD_NoFGT decoding mode.</span></span></p></li>
<li><p><span data-ttu-id="8195f-116">Necesita estar instalado el controlador de la tarjeta gráfica más reciente.</span><span class="sxs-lookup"><span data-stu-id="8195f-116">The latest graphics card driver must be installed.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="8195f-117">Para obtener más información sobre los modos de descodificación, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A> .</span><span class="sxs-lookup"><span data-stu-id="8195f-117">For details about decoding modes, see <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A>.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8195f-118">Codificación H.264 acelerada por hardware: requisitos del conjunto de chips</span><span class="sxs-lookup"><span data-stu-id="8195f-118">Hardware accelerated H.264 encoding: Chipset Requirements</span></span></p></td>
<td><p><span data-ttu-id="8195f-119">Se admiten las siguientes soluciones de codificación de vídeo acelerada por hardware Intel:</span><span class="sxs-lookup"><span data-stu-id="8195f-119">The following Intel hardware accelerated video encoding solutions are supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="8195f-120">Los chipsets Intel HD de segunda y tercera generación 2000, 2500, 3000 y 4000 (o versiones posteriores) con codificadores de vídeo de hardware integrados.</span><span class="sxs-lookup"><span data-stu-id="8195f-120">Second and third generation Intel HD Graphics 2000, 2500, 3000, and 4000 chipsets (or later versions) with integrated hardware video encoders.</span></span> <span data-ttu-id="8195f-121">Se requiere la instalación del controlador Intel HD Graphics 15.28.9.2884 o el controlador más reciente que contenga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8195f-121">Installation of the Intel HD Graphics driver 15.28.9.2884 or the latest driver containing the following is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="8195f-122">Controlador de pantalla 9.17.10.2884 o el controlador más reciente</span><span class="sxs-lookup"><span data-stu-id="8195f-122">Display driver 9.17.10.2884 or the latest driver</span></span></p></li>
<li><p><span data-ttu-id="8195f-123">Hardware media foundation transform (HMFT) versión 3.12.10.31 o el HMFT más reciente</span><span class="sxs-lookup"><span data-stu-id="8195f-123">Hardware media foundation transform (HMFT) version 3.12.10.31 or the latest HMFT</span></span></p></li>
</ul></li>
</ul>
<p><span data-ttu-id="8195f-124">Se admiten las siguientes soluciones de codificación de vídeo acelerado por hardware AMD (requiere actualizaciones de CU1 para Lync Server 2013):</span><span class="sxs-lookup"><span data-stu-id="8195f-124">The following AMD hardware accelerated video encoding solutions are supported (requires CU1 Updates for Lync Server 2013):</span></span></p>
<ul>
<li><p><span data-ttu-id="8195f-p103">AMD Video Codec Engine, que está disponible en varias tarjetas de gráficos independientes y en unidades de procesamiento acelerado integrado de procesadores acelerados de la serie AMD A. El controlador de AMD Video Codec Engine 9.12.0.0 o superior necesita estar instalado.</span><span class="sxs-lookup"><span data-stu-id="8195f-p103">AMD Video Codec Engine, which is available in several discrete graphics cards and in integrated accelerated processing units of AMD A-Series Accelerated Processors. The AMD Video Codec Engine driver 9.12.0.0 or higher must be installed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8195f-127">Codificación H.264 acelerada por hardware: requisitos de la cámara</span><span class="sxs-lookup"><span data-stu-id="8195f-127">Hardware accelerated H.264 encoding: Camera Requirements</span></span></p></td>
<td><p><span data-ttu-id="8195f-128">Cámaras de vídeo USB con codificador de hardware H.264 integrado que cumplan la especificación USB Video Class (UVC) versión 1.5.</span><span class="sxs-lookup"><span data-stu-id="8195f-128">USB video cameras with integrated H.264 hardware encoder that conforms to the USB Video Class (UVC) specification version 1.5.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="8195f-129">Lync 2013 admite cámaras UVC 1,5 con Windows 8 o Windows 8,1, que incluye compatibilidad con UVC 1,5.</span><span class="sxs-lookup"><span data-stu-id="8195f-129">Lync 2013 supports UVC 1.5 cameras with Windows 8 or Windows 8.1, which includes support for UVC 1.5.</span></span> <span data-ttu-id="8195f-130">Dado que Windows 7 no incluye compatibilidad con UVC 1,5, Lync 2013 trata las cámaras de UVC 1,5 como cámaras normales sin compatibilidad con la codificación de hardware.</span><span class="sxs-lookup"><span data-stu-id="8195f-130">Because Windows 7 does not include support for UVC 1.5, Lync 2013 treats UVC 1.5 cameras as regular cameras with no hardware encoding support.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="determining-h264-video-encoding-and-decoding-capabilities"></a><span data-ttu-id="8195f-131">Determinación de las capacidades de codificación y descodificación de video H. 264</span><span class="sxs-lookup"><span data-stu-id="8195f-131">Determining H.264 Video Encoding and Decoding Capabilities</span></span>

<span data-ttu-id="8195f-132">Por lo general, son cuatro los factores principales que determinan la capacidad máxima de codificación y descodificación de una configuración de equipo determinada:</span><span class="sxs-lookup"><span data-stu-id="8195f-132">Generally, there are four major factors that determine the maximum encoding and decoding capability of a particular computer configuration:</span></span>

  - <span data-ttu-id="8195f-133">Compatibilidad para descodificación acelerada por hardware mediante DXVA</span><span class="sxs-lookup"><span data-stu-id="8195f-133">Support for hardware accelerated decoding by using DXVA</span></span>

  - <span data-ttu-id="8195f-134">Compatibilidad para codificación acelerada por hardware</span><span class="sxs-lookup"><span data-stu-id="8195f-134">Support for hardware accelerated encoding</span></span>

  - <span data-ttu-id="8195f-135">Número de núcleos físicos</span><span class="sxs-lookup"><span data-stu-id="8195f-135">Number of physical cores</span></span>

  - <span data-ttu-id="8195f-136">Evaluación de la experiencia de Windows (WEI)</span><span class="sxs-lookup"><span data-stu-id="8195f-136">Windows Experience Index (WEI)</span></span>

<span data-ttu-id="8195f-137">La Herramienta de evaluación del sistema de Windows (WinSAT) determina la WEI.</span><span class="sxs-lookup"><span data-stu-id="8195f-137">The Windows System Assessment Tool (WinSAT) determines the WEI.</span></span> <span data-ttu-id="8195f-138">Cuando ejecuta la herramienta WinSAT, genera un documento XML formal de evaluación en el equipo en el directorio% WINDIR% \\ Performance WinSAT de la \\ tienda de \\ almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="8195f-138">When you run the WinSAT tool, it generates a Formal.Assessment XML document on the computer in the %windir%\\Performance\\WinSAT\\DataStore directory.</span></span> <span data-ttu-id="8195f-139">Este archivo XML contiene las siguientes dos puntuaciones que son especialmente importantes para determinar la capacidad de codificación y descodificación:</span><span class="sxs-lookup"><span data-stu-id="8195f-139">This XML file contains the following two scores that are of particular importance for determining encoding and decoding capabilities:</span></span>

  - <span data-ttu-id="8195f-140">VideoEncodeScore indica la capacidad de codificación de vídeo basada en software del equipo.</span><span class="sxs-lookup"><span data-stu-id="8195f-140">The VideoEncodeScore indicates the software-based video encoding capability of the computer.</span></span>

  - <span data-ttu-id="8195f-141">El valor de GraphicsScore indica la capacidad de codificación acelerada por hardware del equipo.</span><span class="sxs-lookup"><span data-stu-id="8195f-141">The GraphicsScore value indicates the hardware accelerated encoding capability of the computer.</span></span>

<span data-ttu-id="8195f-p106">Las siguientes tres tablas explican la capacidad máxima de codificación y descodificación de diferentes tipos de PC en función de la aceleración de hardware que admitan. Para resoluciones de 640 x 360 y superiores, la velocidad de fotogramas máxima admitida es de 30 fotogramas por segundo (fps). Para resoluciones inferiores a 640 x 360, la velocidad de fotogramas máxima admitida es de 15 fps.</span><span class="sxs-lookup"><span data-stu-id="8195f-p106">The following three tables explain the maximum encoding and decoding capability for different PC types depending on what hardware acceleration they support. For resolutions of 640x360 and higher, the maximum supported frame rate is 30 frames per second (fps). For resolutions lower than 640x360, the maximum supported frame rate is 15 fps.</span></span>

### <a name="computer-without-dxva-and-without-hardware-accelerated-encoder"></a><span data-ttu-id="8195f-145">Equipo sin DXVA y sin codificador acelerado por hardware</span><span class="sxs-lookup"><span data-stu-id="8195f-145">Computer Without DXVA And Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8195f-146">Resolución del codificador habilitado</span><span class="sxs-lookup"><span data-stu-id="8195f-146">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="8195f-147">Resolución del descodificador habilitado</span><span class="sxs-lookup"><span data-stu-id="8195f-147">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="8195f-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="8195f-148">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8195f-149">424 x 240</span><span class="sxs-lookup"><span data-stu-id="8195f-149">424x240</span></span></p></td>
<td><p><span data-ttu-id="8195f-150">424 x 240 (640 x 360 a 15 fps para escenarios solo de recepción)</span><span class="sxs-lookup"><span data-stu-id="8195f-150">424x240 (640x360 at 15fps for receive only scenarios)</span></span></p></td>
<td><p><span data-ttu-id="8195f-151">1 núcleo y VideoEncodeScore ≥4.0</span><span class="sxs-lookup"><span data-stu-id="8195f-151">1 Core and VideoEncodeScore ≥ 4.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8195f-152">640 x 360</span><span class="sxs-lookup"><span data-stu-id="8195f-152">640x360</span></span></p></td>
<td><p><span data-ttu-id="8195f-153">640 x 360</span><span class="sxs-lookup"><span data-stu-id="8195f-153">640x360</span></span></p></td>
<td><p><span data-ttu-id="8195f-154">2 núcleos y VideoEncodeScore ≥4.5</span><span class="sxs-lookup"><span data-stu-id="8195f-154">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8195f-155">640 x 360</span><span class="sxs-lookup"><span data-stu-id="8195f-155">640x360</span></span></p></td>
<td><p><span data-ttu-id="8195f-156">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="8195f-156">1280x720</span></span></p></td>
<td><p><span data-ttu-id="8195f-157">2 núcleos y VideoEncodeScore ≥4.5</span><span class="sxs-lookup"><span data-stu-id="8195f-157">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8195f-158">640 x 360</span><span class="sxs-lookup"><span data-stu-id="8195f-158">640x360</span></span></p></td>
<td><p><span data-ttu-id="8195f-159">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-159">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-160">4 núcleos y VideoEncodeScore ≥4.5</span><span class="sxs-lookup"><span data-stu-id="8195f-160">4 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8195f-161">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="8195f-161">1280x720</span></span></p></td>
<td><p><span data-ttu-id="8195f-162">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="8195f-162">1280x720</span></span></p></td>
<td><p><span data-ttu-id="8195f-163">4 núcleos y VideoEncodeScore ≥7.3</span><span class="sxs-lookup"><span data-stu-id="8195f-163">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8195f-164">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="8195f-164">1280x720</span></span></p></td>
<td><p><span data-ttu-id="8195f-165">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-165">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-166">4 núcleos y VideoEncodeScore ≥7.3</span><span class="sxs-lookup"><span data-stu-id="8195f-166">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8195f-167">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-167">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-168">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-168">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-169">N/D</span><span class="sxs-lookup"><span data-stu-id="8195f-169">N/A</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="computer-with-dxva-but-without-hardware-accelerated-encoder"></a><span data-ttu-id="8195f-170">Equipo con DXVA pero sin codificador acelerado por hardware</span><span class="sxs-lookup"><span data-stu-id="8195f-170">Computer With DXVA But Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8195f-171">Resolución del codificador habilitado</span><span class="sxs-lookup"><span data-stu-id="8195f-171">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="8195f-172">Resolución del descodificador habilitado</span><span class="sxs-lookup"><span data-stu-id="8195f-172">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="8195f-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="8195f-173">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8195f-174">424 x 240</span><span class="sxs-lookup"><span data-stu-id="8195f-174">424x240</span></span></p></td>
<td><p><span data-ttu-id="8195f-175">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-175">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-176">1 núcleo y VideoEncodeScore ≥3.0</span><span class="sxs-lookup"><span data-stu-id="8195f-176">1 Core and VideoEncodeScore ≥ 3.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8195f-177">640 x 360</span><span class="sxs-lookup"><span data-stu-id="8195f-177">640x360</span></span></p></td>
<td><p><span data-ttu-id="8195f-178">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-178">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-179">2 núcleos y VideoEncodeScore ≥4.5</span><span class="sxs-lookup"><span data-stu-id="8195f-179">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8195f-180">960 x 540</span><span class="sxs-lookup"><span data-stu-id="8195f-180">960x540</span></span></p></td>
<td><p><span data-ttu-id="8195f-181">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-181">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-182">2 núcleos y VideoEncodeScore ≥6.0</span><span class="sxs-lookup"><span data-stu-id="8195f-182">2 Cores and VideoEncodeScore ≥ 6.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8195f-183">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="8195f-183">1280x720</span></span></p></td>
<td><p><span data-ttu-id="8195f-184">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-184">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-185">4 núcleos y VideoEncodeScore ≥6.7</span><span class="sxs-lookup"><span data-stu-id="8195f-185">4 Cores and VideoEncodeScore ≥ 6.7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8195f-186">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-186">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-187">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-187">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-188">4 núcleos y VideoEncodeScore ≥8.2</span><span class="sxs-lookup"><span data-stu-id="8195f-188">4 Cores and VideoEncodeScore ≥ 8.2</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="8195f-p107">La puntuación de WinSAT en Windows 7 está limitada a un máximo de 7,9. Por lo tanto, la capacidad de codificación de un equipo sin un codificador acelerado por hardware solo se puede lograr en Windows 8 o Windows 8.1, donde la puntuación máxima de WinSAT es de 9,9.</span><span class="sxs-lookup"><span data-stu-id="8195f-p107">The WinSAT score on Windows 7 is limited to a maximum of 7.9. Therefore, the encoding capability for a computer without a hardware accelerated encoder can only be achieved on Windows 8 or Windows 8.1, where the maximum WinSAT score is 9.9.</span></span>



</div>

### <a name="computer-with-dxva-and-with-intel-hd-graphics-hardware-accelerated-encoder"></a><span data-ttu-id="8195f-191">Equipo con DXVA y con codificador acelerado por hardware Intel HD Graphics</span><span class="sxs-lookup"><span data-stu-id="8195f-191">Computer With DXVA And With Intel HD Graphics Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8195f-192">Resolución del codificador habilitado</span><span class="sxs-lookup"><span data-stu-id="8195f-192">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="8195f-193">Resolución del descodificador habilitado</span><span class="sxs-lookup"><span data-stu-id="8195f-193">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="8195f-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="8195f-194">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8195f-195">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="8195f-195">1280x720</span></span></p></td>
<td><p><span data-ttu-id="8195f-196">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-196">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-197">Todos los modelos de Intel HD Graphics de segunda y tercera generación</span><span class="sxs-lookup"><span data-stu-id="8195f-197">All 2nd and 3rd generation Intel HD Graphics</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8195f-198">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-198">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-199">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="8195f-199">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="8195f-200">Todos los modelos de Intel HD Graphics de segunda y tercera generación y GraphicsScore ≥5.0</span><span class="sxs-lookup"><span data-stu-id="8195f-200">2nd and 3rd generation Intel HD Graphics and GraphicsScore ≥ 5.0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="mobile-device-video-capabilities"></a><span data-ttu-id="8195f-201">Capacidades de vídeo de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="8195f-201">Mobile Device Video Capabilities</span></span>

<span data-ttu-id="8195f-202">En la tabla siguiente se describen las capacidades máximas de vídeo para dispositivos móviles compatibles.</span><span class="sxs-lookup"><span data-stu-id="8195f-202">The following table describes the maximum video capabilities for supported mobile devices.</span></span> <span data-ttu-id="8195f-203">Para obtener más información sobre la compatibilidad de dispositivos móviles, vea [planificación de clientes móviles en Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span><span class="sxs-lookup"><span data-stu-id="8195f-203">For more information about mobile device support, see [Planning for mobile clients in Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8195f-204">Característica</span><span class="sxs-lookup"><span data-stu-id="8195f-204">Feature</span></span></th>
<th><span data-ttu-id="8195f-205">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="8195f-205">Windows Phone</span></span></th>
<th><span data-ttu-id="8195f-206">iPhone</span><span class="sxs-lookup"><span data-stu-id="8195f-206">iPhone</span></span></th>
<th><span data-ttu-id="8195f-207">iPad</span><span class="sxs-lookup"><span data-stu-id="8195f-207">iPad</span></span></th>
<th><span data-ttu-id="8195f-208">Android</span><span class="sxs-lookup"><span data-stu-id="8195f-208">Android</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8195f-209">Resolución máxima de codificación H.264</span><span class="sxs-lookup"><span data-stu-id="8195f-209">H.264 encoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="8195f-210">VGA</span><span class="sxs-lookup"><span data-stu-id="8195f-210">VGA</span></span></p></td>
<td><p><span data-ttu-id="8195f-211">QVGA: iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="8195f-211">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="8195f-212">VGA: iPhone 5</span><span class="sxs-lookup"><span data-stu-id="8195f-212">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="8195f-213">720p: iPhone 5S y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8195f-213">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="8195f-214">VGA: iPad 2 y versiones posteriores/iPad mini 1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8195f-214">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="8195f-215">720p: iPad Air/iPad mini 2/iPad Pro y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8195f-215">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="8195f-216">Hasta VGA según el modelo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8195f-216">Up to VGA depending on device model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8195f-217">Resolución máxima de descodificación H.264</span><span class="sxs-lookup"><span data-stu-id="8195f-217">H.264 decoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="8195f-218">VGA</span><span class="sxs-lookup"><span data-stu-id="8195f-218">VGA</span></span></p></td>
<td><p><span data-ttu-id="8195f-219">QVGA: iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="8195f-219">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="8195f-220">VGA: iPhone 5</span><span class="sxs-lookup"><span data-stu-id="8195f-220">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="8195f-221">720p: iPhone 5S y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8195f-221">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="8195f-222">VGA: iPad 2 y versiones posteriores/iPad mini 1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8195f-222">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="8195f-223">720p: iPad Air/iPad mini 2/iPad Pro y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8195f-223">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="8195f-224">Hasta VGA según el modelo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8195f-224">Up to VGA depending on device model</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8195f-225">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8195f-225">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

