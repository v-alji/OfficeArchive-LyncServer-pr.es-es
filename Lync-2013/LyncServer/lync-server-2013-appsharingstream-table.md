---
title: 'Lync Server 2013: tabla AppSharingStream'
description: 'Lync Server 2013: tabla AppSharingStream.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingStream table
ms:assetid: 391490cb-d7b8-44ca-b4d1-429600da909c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204808(v=OCS.15)
ms:contentKeyID: 48183852
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b530af5b489e090e5d0d00fbb01b2b950bafbe5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440559"
---
# <a name="appsharingstream-table-in-lync-server-2013"></a><span data-ttu-id="ffeac-103">Tabla AppSharingStream en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ffeac-103">AppSharingStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffeac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffeac-104">

<span> </span></span></span>

<span data-ttu-id="ffeac-105">_**Última modificación del tema:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="ffeac-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="ffeac-106">La tabla AppSharingStream contiene métricas de experiencia de calidad para las secuencias de red que se usan para compartir aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ffeac-106">The AppSharingStream table contains Quality of Experience metrics for the network streams used for application sharing.</span></span> <span data-ttu-id="ffeac-107">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ffeac-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffeac-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="ffeac-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="ffeac-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="ffeac-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-113">Fechas</span><span class="sxs-lookup"><span data-stu-id="ffeac-113">dateTime</span></span></p></td>
<td><p><span data-ttu-id="ffeac-114">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="ffeac-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ffeac-115">Fecha y hora en que comenzó la sesión.</span><span class="sxs-lookup"><span data-stu-id="ffeac-115">Date and time that the session started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-117">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-117">int</span></span></p></td>
<td><p><span data-ttu-id="ffeac-118">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="ffeac-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ffeac-119">Identificador secuencial que se usa para diferenciar las sesiones que comenzaron en la misma fecha y al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-119">Sequential identifier used to distinguish between sessions that started on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="ffeac-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ffeac-122">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="ffeac-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ffeac-123">Representa el tipo de línea de vídeo que se usa en la llamada.</span><span class="sxs-lookup"><span data-stu-id="ffeac-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="ffeac-124">Los valores permitidos son:</span><span class="sxs-lookup"><span data-stu-id="ffeac-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ffeac-125">0: audio</span><span class="sxs-lookup"><span data-stu-id="ffeac-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="ffeac-126">1: vídeo</span><span class="sxs-lookup"><span data-stu-id="ffeac-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="ffeac-127">2-video panorámico</span><span class="sxs-lookup"><span data-stu-id="ffeac-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="ffeac-128">3: uso compartido de aplicaciones y escritorio</span><span class="sxs-lookup"><span data-stu-id="ffeac-128">3 –Application/Desktop Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-129"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-129"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-130">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-130">int</span></span></p></td>
<td><p><span data-ttu-id="ffeac-131">Primary</span><span class="sxs-lookup"><span data-stu-id="ffeac-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="ffeac-132">Identificador único de la secuencia de uso compartido de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ffeac-132">Unique identifier of the application sharing stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-134">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-135">Valor medio de las vibraciones detectadas entre la llagada de paquetes RTP.</span><span class="sxs-lookup"><span data-stu-id="ffeac-135">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="ffeac-136">(La vibración es una medida de la &quot; irregularidad &quot; de una llamada). Los valores de vibración elevada suelen estar causados por una congestión o un servidor multimedia sobrecargado y tienen como resultado una distorsión o pérdida de audio.</span><span class="sxs-lookup"><span data-stu-id="ffeac-136">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-137"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-137"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-138">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-139">Vibración máxima detectada entre las llegadas al paquete RTP.</span><span class="sxs-lookup"><span data-stu-id="ffeac-139">Maximum jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="ffeac-140">(La vibración es una medida de la &quot; irregularidad &quot; de una llamada). Los valores de vibración elevada suelen estar causados por una congestión o un servidor multimedia sobrecargado y tienen como resultado una distorsión o pérdida de audio.</span><span class="sxs-lookup"><span data-stu-id="ffeac-140">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-141"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-141"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-142">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-p105">Tiempo medio (en milisegundos) necesario para que un paquete de protocolo de transporte en tiempo real (RTP) llegue a otro extremo y vuelva. Los tiempos de ida y vuelta de 200 milisegundos o menos se consideran de calidad aceptable.</span><span class="sxs-lookup"><span data-stu-id="ffeac-p105">Average amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="ffeac-p106">Los valores elevados en los tiempos del recorrido de ida y vuelta pueden deberse a que se trata de enrutamientos de llamadas internacionales, una configuración incorrecta del enrutamiento o a la sobrecarga en el servidor de medios y causan dificultades en las conversaciones de audio en tiempo real bidireccionales.</span><span class="sxs-lookup"><span data-stu-id="ffeac-p106">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-147"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-147"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-148">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-148">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-149">Cantidad máxima de (en milisegundos) requerida para que un paquete de protocolo de transporte de Real-Time viaje a otro extremo y después de nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-149">Maximum amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back.</span></span> <span data-ttu-id="ffeac-150">Los tiempos de ida y vuelta de 200 milisegundos o menos se consideran de calidad aceptable.</span><span class="sxs-lookup"><span data-stu-id="ffeac-150">Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="ffeac-p108">Los valores elevados en los tiempos del recorrido de ida y vuelta pueden deberse a que se trata de enrutamientos de llamadas internacionales, una configuración incorrecta del enrutamiento o a la sobrecarga en el servidor de medios y causan dificultades en las conversaciones de audio en tiempo real bidireccionales.</span><span class="sxs-lookup"><span data-stu-id="ffeac-p108">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-153"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-153"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-154">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-154">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-p109">Tasa media de pérdida de paquetes RTP (se habla de pérdida de paquetes cuando los paquetes RTP, un protocolo utilizado para transmitir audio y vídeo a través de Internet, no llegan a su destino). Una tasa alta de pérdida se suele deber a la congestión, falta de ancho de banda, congestión o interferencias en una conexión inalámbrica o la sobrecarga de un servidor de medios. Generalmente, la pérdida de paquetes da lugar a la pérdida o la distorsión del audio.</span><span class="sxs-lookup"><span data-stu-id="ffeac-p109">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-158"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-158"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-159">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-159">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-160">Frecuencia máxima de pérdida de paquetes de protocolo de transporte de Real-Time (RTP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-160">Maximum rate of Real-Time Transport Protocol (RTP) packet loss.</span></span> <span data-ttu-id="ffeac-161">(La pérdida de paquetes se produce cuando los paquetes RTP, un protocolo usado para transmitir audio y vídeo a través de Internet, no pudo alcanzar su destino). Las tarifas de pérdida elevada suelen ser causadas por la congestión; falta de ancho de banda; disgestión o interferencias inalámbricas; o un servidor multimedia sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="ffeac-161">(Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server.</span></span> <span data-ttu-id="ffeac-162">Generalmente, la pérdida de paquetes da lugar a la pérdida o la distorsión del audio.</span><span class="sxs-lookup"><span data-stu-id="ffeac-162">Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-163"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-163"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-164">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-164">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-165">Número de paquetes enviados.</span><span class="sxs-lookup"><span data-stu-id="ffeac-165">Number of packets sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-166"><strong>Ancho de banda más</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-166"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-167">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-167">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-168">Ancho de banda de unidireccional Estimado disponible al final de la sesión.</span><span class="sxs-lookup"><span data-stu-id="ffeac-168">Estimated one-way bandwidth available at the end of the session.</span></span> <span data-ttu-id="ffeac-169">Se notifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-169">Reported in bits per second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-170"><strong>AppSharingPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-170"><strong>AppSharingPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-171">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-171">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-172">Descripción de la carga de uso compartido de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ffeac-172">Description of the application sharing payload.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-173"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-173"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-174">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-174">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-175">Cantidad total de latencia unidireccional.</span><span class="sxs-lookup"><span data-stu-id="ffeac-175">Total amount of one-way latency.</span></span> <span data-ttu-id="ffeac-176">Latencia unidireccional relativa mide el retraso entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-176">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-177"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-177"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-178">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-178">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-179">Cantidad promedio de latencia unidireccional.</span><span class="sxs-lookup"><span data-stu-id="ffeac-179">Average amount of one-way latency.</span></span> <span data-ttu-id="ffeac-180">Latencia unidireccional relativa mide el retraso entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-180">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-181"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-181"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-182">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-182">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-183">Cantidad máxima de latencia unidireccional.</span><span class="sxs-lookup"><span data-stu-id="ffeac-183">Maximum amount of one-way latency.</span></span> <span data-ttu-id="ffeac-184">Latencia unidireccional relativa mide el retraso entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-184">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-185"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-185"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-186">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-187">Total de repeticiones de ráfagas unidireccionales.</span><span class="sxs-lookup"><span data-stu-id="ffeac-187">Total one-way burst occurrences.</span></span> <span data-ttu-id="ffeac-188">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="ffeac-188">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ffeac-189">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-189">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-190"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-190"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-191">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-191">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-192">Densidad de ráfaga unidireccional total.</span><span class="sxs-lookup"><span data-stu-id="ffeac-192">Total one-way burst density.</span></span> <span data-ttu-id="ffeac-193">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="ffeac-193">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ffeac-194">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-194">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-195"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-195"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-196">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-196">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-197">Total de duración de ráfaga unidireccional.</span><span class="sxs-lookup"><span data-stu-id="ffeac-197">Total one-way burst duration.</span></span> <span data-ttu-id="ffeac-198">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="ffeac-198">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ffeac-199">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-199">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-200"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-200"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-201">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-201">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-202">Total de repeticiones de intervalos unidireccionales.</span><span class="sxs-lookup"><span data-stu-id="ffeac-202">Total one-way gap occurrences.</span></span> <span data-ttu-id="ffeac-203">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante; los huecos indican retrasos entre estas ráfagas.</span><span class="sxs-lookup"><span data-stu-id="ffeac-203">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ffeac-204">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-204">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-205"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-205"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-206">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-206">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-207">Densidad de brechas en un camino total.</span><span class="sxs-lookup"><span data-stu-id="ffeac-207">Total one-way gap density.</span></span> <span data-ttu-id="ffeac-208">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante; los huecos indican retrasos entre estas ráfagas.</span><span class="sxs-lookup"><span data-stu-id="ffeac-208">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ffeac-209">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-209">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-210"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-210"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-211">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-211">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-212">Duración del intervalo unidireccional total.</span><span class="sxs-lookup"><span data-stu-id="ffeac-212">Total one-way gap duration.</span></span> <span data-ttu-id="ffeac-213">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante; los huecos indican retrasos entre estas ráfagas.</span><span class="sxs-lookup"><span data-stu-id="ffeac-213">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ffeac-214">Esta medida mide el flujo de datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-214">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-215"><strong>ApplicationSharingType</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-215"><strong>ApplicationSharingType</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-216">varChar (256)</span><span class="sxs-lookup"><span data-stu-id="ffeac-216">varChar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-217">Función de aplicación (persona que comparte o visor) y tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="ffeac-217">Application role (Sharer or Viewer) and content type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-218"><strong>RDPTileProcessingLatencyTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-218"><strong>RDPTileProcessingLatencyTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-219">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-219">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-220">Tiempo total de procesamiento para los mosaicos del Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-220">Total processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ffeac-221">Un total más alto iguala a un retraso más largo en la experiencia de visualización.</span><span class="sxs-lookup"><span data-stu-id="ffeac-221">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-222"><strong>RDPTileProcessingLatencyAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-222"><strong>RDPTileProcessingLatencyAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-223">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-223">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-224">Tiempo promedio de procesamiento para los mosaicos del Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-224">Average processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ffeac-225">Un total más alto iguala a un retraso más largo en la experiencia de visualización.</span><span class="sxs-lookup"><span data-stu-id="ffeac-225">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-226"><strong>RDPTileProcessingLatencyMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-226"><strong>RDPTileProcessingLatencyMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-227">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-227">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-228">Tiempo máximo de procesamiento para los mosaicos del Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-228">Maximum processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ffeac-229">Un total más alto iguala a un retraso más largo en la experiencia de visualización.</span><span class="sxs-lookup"><span data-stu-id="ffeac-229">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-231">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-231">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-232">Repeticiones de ráfagas en el tiempo de procesamiento de los mosaicos del Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-232">Burst occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ffeac-233">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="ffeac-233">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-235">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-235">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-236">Densidad de ráfaga en el tiempo de procesamiento de los mosaicos del Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-236">Burst density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ffeac-237">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="ffeac-237">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-239">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-239">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-240">Duración de ráfagas en el tiempo de procesamiento de los mosaicos del Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-240">Burst duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ffeac-241">Una transmisión "por ráfagas" es una transmisión en la que los datos fluyen en ráfagas imprevisibles en lugar de un flujo constante.</span><span class="sxs-lookup"><span data-stu-id="ffeac-241">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-243">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-244">Repeticiones de huecos en el tiempo de procesamiento de los mosaicos del Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-244">Gap occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-246">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-247">Densidad de brechas en el tiempo de procesamiento de los mosaicos del Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-247">Gap density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ffeac-248">La densidad de huecos bajos corresponde a una mejor experiencia de visualización.</span><span class="sxs-lookup"><span data-stu-id="ffeac-248">Low gap density equates to a better viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-250">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-251">Duración del hueco en el tiempo de procesamiento de los mosaicos del Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="ffeac-251">Gap duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ffeac-252">Las duraciones cortas equivalen a una mejor experiencia de visualización.</span><span class="sxs-lookup"><span data-stu-id="ffeac-252">Short gap durations equate to a better viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-253"><strong>CaptureTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-253"><strong>CaptureTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-254">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-255">Tasa total de mosaicos capturados (en mosaicos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ffeac-255">Total rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-256"><strong>CaptureTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-256"><strong>CaptureTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-257">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-257">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-258">Velocidad promedio de los mosaicos capturados (en mosaicos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ffeac-258">Average rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-259"><strong>CaptureTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-259"><strong>CaptureTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-260">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-260">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-261">Frecuencia máxima de mosaicos capturados (en mosaicos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ffeac-261">Maximum rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-262"><strong>CaptureTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-262"><strong>CaptureTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-263">en t</span><span class="sxs-lookup"><span data-stu-id="ffeac-263">in t</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-264">Repeticiones de ráfaga en la tasa de mosaicos capturados (en mosaicos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ffeac-264">Burst occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-265"><strong>CaptureTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-265"><strong>CaptureTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-266">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-266">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-267">Densidad de ráfaga en la tasa de mosaicos capturados (en mosaicos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ffeac-267">Burst density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-268"><strong>CaptureTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-268"><strong>CaptureTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-269">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-269">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-270">Duración de ráfaga en la tasa de mosaicos capturados (en mosaicos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ffeac-270">Burst duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-271"><strong>CaptureTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-271"><strong>CaptureTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-272">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-272">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-273">Repeticiones de huecos en la tasa de mosaicos capturados (en mosaicos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ffeac-273">Gap occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-274"><strong>CaptureTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-274"><strong>CaptureTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-275">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-275">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-276">Densidad de huecos en la tasa de mosaicos capturados (en mosaicos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ffeac-276">Gap density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-277"><strong>CaptureTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-277"><strong>CaptureTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-278">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-278">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-279">Duración del hueco en la tasa de mosaicos capturados (en mosaicos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ffeac-279">Gap duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-280"><strong>SpoiledTilePercentTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-280"><strong>SpoiledTilePercentTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-281">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-281">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-282">Porcentaje total del contenido que no se ha podido alcanzar con el visor, pero que se ha descartado y ha sido reemplazado por contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-282">Total percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-283"><strong>SpoiledTilePercentAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-283"><strong>SpoiledTilePercentAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-284">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-284">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-285">Porcentaje medio del contenido que no se ha encontrado en el visor pero que se ha descartado y se ha reemplazado por contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-285">Average percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-286"><strong>SpoiledTilePercentMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-286"><strong>SpoiledTilePercentMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-287">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-288">Porcentaje máximo del contenido que no se ha podido alcanzar con el visor, pero que se descartó y se sobrescribió por contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-288">Maximum percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-290">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-290">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-291">Repeticiones de ráfagas para el contenido que no se ha podido alcanzar con el visor, pero que se han descartado y reemplazado por contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-291">Burst occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-292"><strong>SpoiledTilePercentBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-292"><strong>SpoiledTilePercentBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-293">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-293">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-294">Densidad de ráfaga para el contenido que no se ha podido alcanzar con el visor, pero se ha descartado y ha sido reemplazado por contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-294">Burst density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-295"><strong>SpoiledTilePercentBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-295"><strong>SpoiledTilePercentBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-296">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-296">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-297">Duración de ráfaga para el contenido que no se ha podido alcanzar con el visor, pero se ha descartado y ha sido reemplazado por contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-297">Burst duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-298"><strong>SpoiledTilePercentGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-298"><strong>SpoiledTilePercentGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-299">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-299">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-300">Las repeticiones de huecos para el contenido que no se ha podido alcanzar con el visor pero se han descartado y reemplazado por contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-300">Gap occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-301"><strong>SpoiledTilePercentGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-301"><strong>SpoiledTilePercentGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-302">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-302">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-303">Densidad de brechas para el contenido que no se ha podido alcanzar con el visor, pero que se descartó y sobrescribe por contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-303">Gap density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-304"><strong>SpoiledTilePercentGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-304"><strong>SpoiledTilePercentGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-305">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-305">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-306">El intervalo de tiempo para el contenido que no se ha podido alcanzar con el visor, se ha descartado y ha sido reemplazado por contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffeac-306">Gap duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-307"><strong>ScrapingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-307"><strong>ScrapingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-308">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-308">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-309">Número total de fotogramas descartados de la fuente de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffeac-309">Total number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-310"><strong>ScrapingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-310"><strong>ScrapingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-311">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-311">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-312">Número promedio de fotogramas descartados del origen de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffeac-312">Average number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-313"><strong>ScrapingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-313"><strong>ScrapingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-314">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-314">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-315">Número máximo de fotogramas descartados del origen de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffeac-315">Maximum number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-317">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-317">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-318">Repeticiones de ráfagas en los fotogramas descartados de la fuente de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffeac-318">Burst occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-319"><strong>ScrapingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-319"><strong>ScrapingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-320">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-320">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-321">Densidad de ráfaga en las tramas descartadas de la fuente de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffeac-321">Burst density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-322"><strong>ScrapingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-322"><strong>ScrapingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-323">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-323">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-324">Duración de ráfaga en las tramas descartadas del origen de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffeac-324">Burst duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-325"><strong>ScrapingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-325"><strong>ScrapingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-326">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-327">Repeticiones de huecos en los fotogramas descartados del origen de los gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffeac-327">Gap occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-328"><strong>ScrapingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-328"><strong>ScrapingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-329">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-329">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-330">Densidad de huecos en los fotogramas descartados del origen de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffeac-330">Gap density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-331"><strong>ScrapingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-331"><strong>ScrapingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-332">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-332">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-333">Duración del hueco en los fotogramas descartados del origen de los gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffeac-333">Gap duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-334"><strong>IncomingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-334"><strong>IncomingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-335">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-335">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-336">Total de la velocidad de fotogramas entrantes recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-336">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-337"><strong>IncomingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-337"><strong>IncomingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-338">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-338">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-339">Promedio de velocidad de fotogramas entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-339">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-340"><strong>IncomingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-340"><strong>IncomingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-341">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-342">Cantidad máxima de mosaico entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-342">Maximum incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-343"><strong>IncomingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-343"><strong>IncomingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-344">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-344">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-345">Repeticiones de ráfaga en la tasa de mosaico entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-345">Burst occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-346"><strong>IncomingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-346"><strong>IncomingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-347">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-347">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-348">Densidad de ráfaga en la tasa de icono entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-348">Burst density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-349"><strong>IncomingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-349"><strong>IncomingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-350">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-350">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-351">Duración de ráfaga en la tasa de mosaico entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-351">Burst duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-352"><strong>IncomingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-352"><strong>IncomingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-353">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-353">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-354">Las repeticiones de huecos de la velocidad de los mosaicos entrantes recibidas por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-354">Gap occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-355"><strong>IncomingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-355"><strong>IncomingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-356">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-356">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-357">Densidad de hueco en la tasa de mosaico entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-357">Gap density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-358"><strong>IncomingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-358"><strong>IncomingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-359">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-359">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-360">Duración del intervalo en la tasa de mosaico entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-360">Gap duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-361"><strong>IncomingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-361"><strong>IncomingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-362">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-362">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-363">Total de la velocidad de fotogramas entrantes recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-363">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-364"><strong>IncomingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-364"><strong>IncomingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-365">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-365">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-366">Promedio de velocidad de fotogramas entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-366">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-367"><strong>IncomingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-367"><strong>IncomingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-368">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-368">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-369">Cantidad máxima de fotogramas entrantes recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-369">Maximum incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-370"><strong>IncomingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-370"><strong>IncomingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-371">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-372">Repeticiones de ráfagas en la velocidad de fotogramas entrantes recibidas por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-372">Burst occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-373"><strong>IncomingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-373"><strong>IncomingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-374">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-374">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-375">Densidad de ráfaga en la velocidad de fotogramas entrantes recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-375">Burst density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-376"><strong>IncomingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-376"><strong>IncomingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-377">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-377">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-378">La duración de la ráfaga en la velocidad de fotogramas entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-378">Burst duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-379"><strong>IncomingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-379"><strong>IncomingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-380">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-380">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-381">Las repeticiones de huecos de la velocidad de fotogramas entrantes recibidas por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-381">Gap occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-382"><strong>IncomingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-382"><strong>IncomingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-383">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-383">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-384">Densidad de huecos en la velocidad de fotogramas entrante recibida por el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-384">Gap density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-385"><strong>IncomingFrameRateDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-385"><strong>IncomingFrameRateDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-386">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-386">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-387">Duración del hueco en la velocidad de fotogramas entrante que recibió el visor.</span><span class="sxs-lookup"><span data-stu-id="ffeac-387">Gap duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-388"><strong>OutgoingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-388"><strong>OutgoingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-389">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-389">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-390">Intervalo total de los mosaicos salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-390">Total outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-391"><strong>OutgoingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-391"><strong>OutgoingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-392">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-392">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-393">Promedio de la velocidad de los iconos salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-393">Average outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-394"><strong>OutgoingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-394"><strong>OutgoingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-395">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-396">Velocidad máxima de los iconos salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-396">Maximum outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-397"><strong>OutgoingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-397"><strong>OutgoingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-398">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-398">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-399">Repeticiones de ráfaga en la tasa del mosaico saliente para el remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-399">Burst occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-400"><strong>OutgoingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-400"><strong>OutgoingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-401">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-401">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-402">Densidad de ráfaga en la tasa del mosaico saliente para el remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-402">Burst density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-403"><strong>OutgoingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-403"><strong>OutgoingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-404">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-404">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-405">Duración de ráfaga en la tasa del mosaico saliente para el remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-405">Burst duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-406"><strong>OutgoingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-406"><strong>OutgoingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-407">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-407">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-408">Repeticiones de huecos en la tasa de mosaico saliente para el remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-408">Gap occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-409"><strong>OutgoingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-409"><strong>OutgoingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-410">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-410">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-411">Densidad de hueco en la tasa de mosaico saliente para el remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-411">Gap density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-412"><strong>OutgoingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-412"><strong>OutgoingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-413">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-413">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-414">Duración del hueco en la tasa del mosaico saliente para el remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-414">Gap duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-415"><strong>OutgoingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-415"><strong>OutgoingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-416">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-416">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-417">Total de la velocidad de los fotogramas salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-417">Total outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-418"><strong>OutgoingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-418"><strong>OutgoingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-419">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-419">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-420">promedio de velocidad de fotograma saliente para el remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-420">average outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-421"><strong>OutgoingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-421"><strong>OutgoingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-422">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-422">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-423">Velocidad máxima de los fotogramas salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-423">Maximum outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-425">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-425">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-426">Repeticiones de ráfagas en la velocidad de fotogramas salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-426">Burst occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-427"><strong>OutgoingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-427"><strong>OutgoingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-428">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-428">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-429">Densidad de ráfagas en la velocidad de fotogramas salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-429">Burst density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-430"><strong>OutgoingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-430"><strong>OutgoingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-431">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-431">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-432">Duración de ráfaga en la velocidad de fotogramas salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-432">Burst duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-433"><strong>OutgoingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-433"><strong>OutgoingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-434">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-434">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-435">Repeticiones de huecos en la velocidad de fotogramas salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-435">Gap occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-436"><strong>OutgoingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-436"><strong>OutgoingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-437">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-437">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-438">Densidad de huecos en la velocidad de fotogramas salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-438">Gap density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-439"><strong>OutgoingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-439"><strong>OutgoingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-440">float</span><span class="sxs-lookup"><span data-stu-id="ffeac-440">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-441">Duración del hueco en la velocidad de fotogramas salientes del remitente.</span><span class="sxs-lookup"><span data-stu-id="ffeac-441">Gap duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-442"><strong>AverageRectangleHeight</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-442"><strong>AverageRectangleHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-443">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-443">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-444">Promedio de altura de la resolución de video, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ffeac-444">Average video resolution height, in pixels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-445"><strong>AverageRectangleWidth</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-445"><strong>AverageRectangleWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-446">int</span><span class="sxs-lookup"><span data-stu-id="ffeac-446">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-447">Promedio de ancho de resolución de video, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ffeac-447">Average video resolution width, in pixels.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-448"><strong>Entrada</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-448"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-449">bit</span><span class="sxs-lookup"><span data-stu-id="ffeac-449">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-450">Promedio de velocidad de fotogramas (en fotogramas por segundo) para transfronterizas entrantes.</span><span class="sxs-lookup"><span data-stu-id="ffeac-450">Average frame rate (in frames per second) for inbound transmissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffeac-451"><strong>Saliente</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-451"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-452">bit</span><span class="sxs-lookup"><span data-stu-id="ffeac-452">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-453">Promedio de velocidad de fotogramas (en fotogramas por segundo) para transfronterizas salientes.</span><span class="sxs-lookup"><span data-stu-id="ffeac-453">Average frame rate (in frames per second) for outbound transmissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffeac-454"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="ffeac-454"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="ffeac-455">bit</span><span class="sxs-lookup"><span data-stu-id="ffeac-455">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ffeac-456">1 significa que la dirección de la transmisión es de la persona que llama a la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ffeac-456">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="ffeac-457">0 significa que la dirección de la transmisión es de la persona que llama a la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="ffeac-457">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ffeac-458">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffeac-458">


</div>

<span> </span>

</div>

</div>

</span></span></div>

