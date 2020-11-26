---
title: 'Lync Server 2013: informe de la lista de llamadas'
description: 'Lync Server 2013: informe de la lista de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call List Report
ms:assetid: 9739f9f0-7a37-4844-91d5-f089d2011013
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615020(v=OCS.15)
ms:contentKeyID: 48184921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5b08d4c5f3011facc9cd8d4f6b2800638f3cc896
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435757"
---
# <a name="call-list-report-in-lync-server-2013"></a><span data-ttu-id="91cae-103">Informe de la lista de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91cae-103">Call List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91cae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91cae-104">

<span> </span></span></span>

<span data-ttu-id="91cae-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="91cae-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="91cae-106">El informe de lista de llamadas proporciona métricas relativas a la calidad de la experiencia para las llamadas individuales realizadas y recibidas en su organización.</span><span class="sxs-lookup"><span data-stu-id="91cae-106">The Call List Report provides Quality of Experience (QoE) metrics for individual calls made and received in your organization.</span></span> <span data-ttu-id="91cae-107">Tenga en cuenta que las métricas reales que se incluyan dependerán de cómo obtenga acceso al informe de lista de llamadas.</span><span class="sxs-lookup"><span data-stu-id="91cae-107">Note that the actual metrics reported will depend on how you access the Call List report.</span></span> <span data-ttu-id="91cae-108">Por ejemplo, si abre el informe desde el [Informe de dispositivos en Lync Server 2013](lync-server-2013-device-report.md), verá las métricas como las siguientes, métricas que también se notifican en el informe de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="91cae-108">For example, if you open the report from the [Device Report in Lync Server 2013](lync-server-2013-device-report.md), you'll see metrics such as the following, metrics that are also reported on the Device Report:</span></span>

  - <span data-ttu-id="91cae-109">Micrófono del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="91cae-109">Caller's microphone</span></span>

  - <span data-ttu-id="91cae-110">Altavoz del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="91cae-110">Caller's speaker</span></span>

  - <span data-ttu-id="91cae-111">Micrófono del destinatario de la llamada</span><span class="sxs-lookup"><span data-stu-id="91cae-111">Callee's microphone</span></span>

  - <span data-ttu-id="91cae-112">Altavoz del destinatario de la llamada</span><span class="sxs-lookup"><span data-stu-id="91cae-112">Callee's speaker</span></span>

  - <span data-ttu-id="91cae-113">Relación de tiempo de conmutación de voz</span><span class="sxs-lookup"><span data-stu-id="91cae-113">Ratio of voice switch time</span></span>

<span data-ttu-id="91cae-114">Sin embargo, si abre el informe de la lista de llamadas desde el [Informe de ubicación en Lync Server 2013](lync-server-2013-location-report.md), no verá ninguna de esas métricas; en su lugar, verás métricas como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="91cae-114">However, if you open the Call List Report from the [Location Report in Lync Server 2013](lync-server-2013-location-report.md), you won't see any of those metrics; instead, you'll see metrics like these:</span></span>

  - <span data-ttu-id="91cae-115">Recorrido de ida y vuelta (ms)</span><span class="sxs-lookup"><span data-stu-id="91cae-115">Round trip (ms)</span></span>

  - <span data-ttu-id="91cae-116">Degradación (MOS)</span><span class="sxs-lookup"><span data-stu-id="91cae-116">Degradation (MOS)</span></span>

  - <span data-ttu-id="91cae-117">Pérdida de paquetes</span><span class="sxs-lookup"><span data-stu-id="91cae-117">Packet loss</span></span>

  - <span data-ttu-id="91cae-118">Vibración (ms)</span><span class="sxs-lookup"><span data-stu-id="91cae-118">Jitter (ms)</span></span>

<span data-ttu-id="91cae-p102">Esas son las métricas incluidas en el informe de ubicaciones. No obstante, siempre puede hacer clic en la métrica Detalles, en el informe de lista de llamadas, para obtener información completa sobre la calidad de la experiencia de cualquier llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-p102">Those are the metrics reported on the Location Report. However, from the Call List Report you can always click the Detail metric to provide complete QoE information for any call.</span></span>

<div>

## <a name="accessing-the-call-list-report"></a><span data-ttu-id="91cae-121">Acceso al informe de lista de llamadas</span><span class="sxs-lookup"><span data-stu-id="91cae-121">Accessing the Call List Report</span></span>

<span data-ttu-id="91cae-122">El informe de lista de llamadas es accesible desde cualquiera de los siguientes informes:</span><span class="sxs-lookup"><span data-stu-id="91cae-122">The Call List Report can be accessed from any of the following reports:</span></span>

  - <span data-ttu-id="91cae-123">El [Informe de ubicación en Lync Server 2013](lync-server-2013-location-report.md) (haciendo clic en el volumen de la llamada o en la métrica de porcentaje de llamada deficiente)</span><span class="sxs-lookup"><span data-stu-id="91cae-123">The [Location Report in Lync Server 2013](lync-server-2013-location-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="91cae-124">El [Informe del dispositivo en Lync Server 2013](lync-server-2013-device-report.md) (haciendo clic en el volumen de la llamada o en la métrica de porcentaje de llamada deficiente)</span><span class="sxs-lookup"><span data-stu-id="91cae-124">The [Device Report in Lync Server 2013](lync-server-2013-device-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="91cae-125">El [informe Resumen de calidad de medios en Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (haciendo clic en el volumen de la llamada o en la métrica de porcentaje de llamada deficiente)</span><span class="sxs-lookup"><span data-stu-id="91cae-125">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="91cae-126">El [Informe rendimiento del servidor de Lync Server 2013](lync-server-2013-server-performance-report.md) (haciendo clic en el volumen de la llamada o en la métrica de porcentaje de llamada deficiente)</span><span class="sxs-lookup"><span data-stu-id="91cae-126">The [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

<span data-ttu-id="91cae-127">Desde el informe de la lista de llamadas puede acceder al [Informe de detalles de llamadas en Lync Server 2013](lync-server-2013-call-detail-report.md) haciendo clic en la métrica de detalles.</span><span class="sxs-lookup"><span data-stu-id="91cae-127">From within the Call List Report you can access the [Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) by clicking the Detail metric.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-list-report"></a><span data-ttu-id="91cae-128">Optimización del uso del informe de lista de llamadas</span><span class="sxs-lookup"><span data-stu-id="91cae-128">Making the Best Use of the Call List Report</span></span>

<span data-ttu-id="91cae-129">Si no recuerda qué miden algunas de las métricas del informe de lista de llamadas (por ejemplo, Relación de tiempo de conmutación de voz), mantenga el mouse sobre la etiqueta de la métrica y aparecerá una información sobre la herramienta con una breve descripción de la métrica.</span><span class="sxs-lookup"><span data-stu-id="91cae-129">If you can't remember what some of the Call List Report metrics (such as Ratio voice switch time) actually measure, hold your mouse over the metric label; a tool tip will then appear giving you a brief description of the metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="91cae-130">Filtros</span><span class="sxs-lookup"><span data-stu-id="91cae-130">Filters</span></span>

<span data-ttu-id="91cae-p103">Ninguno. No se puede filtrar el informe de lista de llamadas.</span><span class="sxs-lookup"><span data-stu-id="91cae-p103">None. You cannot filter the Call List Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="91cae-133">Métricas</span><span class="sxs-lookup"><span data-stu-id="91cae-133">Metrics</span></span>

<span data-ttu-id="91cae-134">En la siguiente tabla se detalla la información facilitada en el informe de lista de llamadas para cada llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-134">The following table lists the information provided in the Call List Report for each call.</span></span>

### <a name="call-list-report-metrics"></a><span data-ttu-id="91cae-135">Métricas del informe de lista de llamadas</span><span class="sxs-lookup"><span data-stu-id="91cae-135">Call List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91cae-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="91cae-136">Name</span></span></th>
<th><span data-ttu-id="91cae-137">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="91cae-137">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="91cae-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="91cae-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91cae-139"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-139"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-140">No</span><span class="sxs-lookup"><span data-stu-id="91cae-140">No</span></span></p></td>
<td><p><span data-ttu-id="91cae-141">Al hacer clic en este elemento, el informe muestra información adicional sobre la llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-141">When you click this item, the report shows additional information on the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91cae-142"><strong>Autor de llamada</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-142"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-143">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-143">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-144">Dirección SIP de la persona que inició la llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-144">SIP address of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91cae-145"><strong>Destinatario de la llamada</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-145"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-146">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-146">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-147">Dirección SIP de la persona que recibió la llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-147">SIP address of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91cae-148"><strong>Hora de inicio</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-148"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-149">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-149">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-150">Fecha y hora en que se inició la llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-150">Date and time that the call started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91cae-151"><strong>Hora de finalización</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-151"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-152">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-152">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-153">Fecha y hora en que finalizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-153">Date and time that the call ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91cae-154"><strong>Agente de usuario de autor de la llamada</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-154"><strong>Caller user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-155">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-155">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-156">Software utilizado por el extremo de la persona que inició la llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-156">Software used by the endpoint of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91cae-157"><strong>Agente de usuario de destinatario de la llamada</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-157"><strong>Callee user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-158">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-158">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-159">Software utilizado por el extremo de la persona que recibió la llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-159">Software used by the endpoint of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91cae-160"><strong>Recorrido de ida y vuelta (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-160"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-161">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-161">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-p104">Tiempo medio (en milisegundos) necesario para que un paquete de protocolo de transporte en tiempo real (RTP) llegue a otro extremo y vuelva. Los tiempos de ida y vuelta de 100 milisegundos o menos se consideran de calidad aceptable.</span><span class="sxs-lookup"><span data-stu-id="91cae-p104">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="91cae-p105">Los valores elevados en los tiempos del recorrido de ida y vuelta pueden deberse a que se trata de enrutamientos de llamadas internacionales, una configuración incorrecta del enrutamiento o a la sobrecarga en el servidor multimedia y causan dificultades en las conversaciones de audio bidireccionales en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="91cae-p105">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91cae-166"><strong>Degradación (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-166"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-167">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-167">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-168">Cantidad media de degradación de la puntuación de opinión media (MOS) experimentada durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-168">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="91cae-169">Los valores de degradación oscilan entre un mínimo de 0,0 y un máximo de 5,0.</span><span class="sxs-lookup"><span data-stu-id="91cae-169">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="91cae-170">Un valor de 0,5 o menos constituye una degradación aceptable.</span><span class="sxs-lookup"><span data-stu-id="91cae-170">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="91cae-171">Históricamente, las puntuaciones de opinión media se calculaban haciendo que los usuarios puntuaran la calidad de una llamada en una escala del 1 al 5.</span><span class="sxs-lookup"><span data-stu-id="91cae-171">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="91cae-172">En Lync Server, Lync Server usa un conjunto de algoritmos para predecir cómo los usuarios habrían calificado una llamada.</span><span class="sxs-lookup"><span data-stu-id="91cae-172">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="91cae-p107">Los valores altos de degradación pueden ser producto de la congestión, falta de ancho de banda, congestión o interferencias en una conexión inalámbrica, o la sobrecarga de un servidor multimedia o servidor de extremo. Una degradación alta causa la distorsión o la pérdida del audio.</span><span class="sxs-lookup"><span data-stu-id="91cae-p107">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91cae-175"><strong>Pérdida de paquetes</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-175"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-176">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-p108">Tasa media de pérdida de paquetes RTP. Se habla de pérdida de paquetes cuando los paquetes RTP, un protocolo que se usa para transmitir audio y vídeo a través de Internet, no llegan a su destino. Una tasa alta de pérdida suele deberse a la congestión, falta de ancho de banda, congestión o interferencias en una conexión inalámbrica, o la sobrecarga de un servidor multimedia. Generalmente, la pérdida de paquetes da lugar a la pérdida o la distorsión del audio.</span><span class="sxs-lookup"><span data-stu-id="91cae-p108">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91cae-180"><strong>Vibración</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-180"><strong>Jitter</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-181">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-181">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-182">Valor medio de las vibraciones detectadas entre la llagada de paquetes RTP.</span><span class="sxs-lookup"><span data-stu-id="91cae-182">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="91cae-183">(La vibración es una medida de la &quot; irregularidad &quot; de una llamada). Los valores de vibración elevada suelen estar causados por una congestión o un servidor multimedia sobrecargado y tienen como resultado una distorsión o pérdida de audio.</span><span class="sxs-lookup"><span data-stu-id="91cae-183">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91cae-184"><strong>Tasa de recuperación de muestras ocultas</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-184"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-185">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-p110">Tasa media de muestras de audio ocultas respecto a la cantidad total de muestras. Una muestra de audio oculta es una técnica que se emplea para suavizar la transición brusca que normalmente supondría la pérdida de paquetes de red. Los valores elevados indican niveles igualmente elevados de aplicación de ocultación de pérdidas a causa de la pérdida de paquetes o de las vibraciones, y dan lugar a la distorsión o pérdida del audio.</span><span class="sxs-lookup"><span data-stu-id="91cae-p110">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91cae-188"><strong>Tasa de recuperación de muestras extendidas</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-188"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-189">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-189">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-p111">Tasa media de muestras de audio extendidas respecto a la cantidad total de muestras. El audio extendido es el audio que se expande para ayudar a mantener el nivel de calidad de la llamada cuando se detecta la pérdida de paquetes en la red. Los valores elevados indican un grado igualmente elevado de extensión de las muestras a causa de las vibraciones, y dan lugar a un audio robótico o distorsionado.</span><span class="sxs-lookup"><span data-stu-id="91cae-p111">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91cae-192"><strong>Tasa de recuperación de muestras comprimidas</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-192"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-193">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-193">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-p112">Tasa media de muestras de audio comprimidas respecto a la cantidad total de muestras. El audio comprimido es el audio que se comprime para ayudar a mantener el nivel de calidad de la llamada cuando se detecta la pérdida de paquetes en la red. Los valores altos indican un elevado grado de compresión de las muestras a causa de las vibraciones y las consecuencias son un audio acelerado o distorsionado.</span><span class="sxs-lookup"><span data-stu-id="91cae-p112">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91cae-196"><strong>Conectividad</strong></span><span class="sxs-lookup"><span data-stu-id="91cae-196"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="91cae-197">Sí</span><span class="sxs-lookup"><span data-stu-id="91cae-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="91cae-p113">Tipo de vínculo de comunicación inalámbrica. Normalmente es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="91cae-p113">Type of wireless communication link. Typically, this is one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91cae-200">Retransmisión</span><span class="sxs-lookup"><span data-stu-id="91cae-200">Relay</span></span></p></li>
<li><p><span data-ttu-id="91cae-201">Directo</span><span class="sxs-lookup"><span data-stu-id="91cae-201">Direct</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="91cae-202">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91cae-202">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

