---
title: 'Lync Server 2013: contadores de rendimiento de movilidad'
description: 'Lync Server 2013: contadores de rendimiento de movilidad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility performance counters
ms:assetid: d18ed85a-673d-4695-aa3f-ac83a38ab90a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690046(v=OCS.15)
ms:contentKeyID: 48185441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 922288f6c026f088d651dc61afdcb6ba04fed30a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425559"
---
# <a name="mobility-performance-counters-in-lync-server-2013"></a><span data-ttu-id="754d3-103">Contadores de rendimiento de movilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="754d3-103">Mobility performance counters in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="754d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="754d3-104">

<span> </span></span></span>

<span data-ttu-id="754d3-105">_**Última modificación del tema:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="754d3-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="754d3-106">En las siguientes tablas se enumeran los nombres y descripciones de los contadores de rendimiento que puede usar para supervisar los servidores que ejecutan la API Web de comunicaciones unificadas (UCWA) y el servicio de movilidad de Lync Server 2013 MCX.</span><span class="sxs-lookup"><span data-stu-id="754d3-106">The following tables list the names and descriptions of performance counters that you can use to monitor servers running the Unified Communications Web API (UCWA) and the Lync Server 2013 Mcx Mobility Service.</span></span>

<span data-ttu-id="754d3-107">El nombre de categoría de los contadores de la tabla relativa a UCWA es **LS:WEB – UCWA**.</span><span class="sxs-lookup"><span data-stu-id="754d3-107">The category name for the counters in the UCWA table is **LS:WEB – UCWA**.</span></span>

<span data-ttu-id="754d3-108">El nombre de categoría de los contadores de la tabla relativa al servicio de movilidad Mcx es **LS:WEB - Mobile Communication Service**.</span><span class="sxs-lookup"><span data-stu-id="754d3-108">The category name for the counters in the Mcx Mobility Service table is **LS:WEB - Mobile Communication Service**.</span></span>

<div>

## <a name="performance-counters-for-ucwa"></a><span data-ttu-id="754d3-109">Contadores de rendimiento para UCWA</span><span class="sxs-lookup"><span data-stu-id="754d3-109">Performance Counters for UCWA</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="754d3-110">Contador</span><span class="sxs-lookup"><span data-stu-id="754d3-110">Counter</span></span></th>
<th><span data-ttu-id="754d3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="754d3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="754d3-112">Recuento de aplicaciones activas</span><span class="sxs-lookup"><span data-stu-id="754d3-112">Active Application Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-113">Número actual de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="754d3-113">The current number of applications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-114">Recuento de modalidad de uso compartido de aplicaciones activa</span><span class="sxs-lookup"><span data-stu-id="754d3-114">Active Application Sharing Modality Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-115">Número actual de modalidad de uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="754d3-115">The current number of Application Sharing modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-116">Recuento de modalidad de audio activa</span><span class="sxs-lookup"><span data-stu-id="754d3-116">Active Audio Modality Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-117">Número actual de modalidad de audio</span><span class="sxs-lookup"><span data-stu-id="754d3-117">The current number of Audio modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-118">Recuento de modalidad de colaboración de datos activa</span><span class="sxs-lookup"><span data-stu-id="754d3-118">Active Data Collaboration Modality Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-119">Número actual de modalidad de colaboración de datos</span><span class="sxs-lookup"><span data-stu-id="754d3-119">The current number of Data Collaboration modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-120">Latencia de recuperación de foto de Active Directory (ms)</span><span class="sxs-lookup"><span data-stu-id="754d3-120">Active Directory Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="754d3-121">Contador que refleja el promedio de tiempo (en milisegundos) que se invierte en recuperar una foto de Active Directory</span><span class="sxs-lookup"><span data-stu-id="754d3-121">This counter shows the average time (in milliseconds) to retrieve a photo from active directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-122">Recuento de modalidad de mensajería activa</span><span class="sxs-lookup"><span data-stu-id="754d3-122">Active Messaging Modality Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-123">Número actual de modalidad de mensajería</span><span class="sxs-lookup"><span data-stu-id="754d3-123">The current number of Messaging modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-124">Recuento de modalidad de vídeo panorámico activa</span><span class="sxs-lookup"><span data-stu-id="754d3-124">Active Panoramic Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-125">Número actual de modalidad de vídeo panorámico</span><span class="sxs-lookup"><span data-stu-id="754d3-125">The current number of Panoramic Video modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-126">Recuento de solicitudes GET pendientes activas</span><span class="sxs-lookup"><span data-stu-id="754d3-126">Active Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-127">Número de solicitudes GET pendientes activas actualmente; conexiones largamente mantenidas con el servidor</span><span class="sxs-lookup"><span data-stu-id="754d3-127">The number of currently active pending gets; long-held connections to the server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-128">Recuento de sesiones activas</span><span class="sxs-lookup"><span data-stu-id="754d3-128">Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-129">Número actual de extremos registrados en UCWA por aplicación y total</span><span class="sxs-lookup"><span data-stu-id="754d3-129">The current number of endpoints registered in UCWA per application and total</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-130">Recuento de instancias de usuario activas</span><span class="sxs-lookup"><span data-stu-id="754d3-130">Active User Instance Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-131">Número actual de instancias de usuario</span><span class="sxs-lookup"><span data-stu-id="754d3-131">The current number of user instances</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-132">Instancias de usuario activas sin aplicación</span><span class="sxs-lookup"><span data-stu-id="754d3-132">Active User Instances without Application</span></span></p></td>
<td><p><span data-ttu-id="754d3-133">Número actual de instancias de usuario sin aplicación</span><span class="sxs-lookup"><span data-stu-id="754d3-133">The current number of user instances without application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-134">Recuento de modalidad de vídeo de aplicaciones activa</span><span class="sxs-lookup"><span data-stu-id="754d3-134">Active Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-135">Número actual de modalidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="754d3-135">The current number of Video modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-136">Solicitudes de creación de aplicación recibidas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-136">Application Creation Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-137">Ratio por segundo de solicitudes de creación de aplicación recibidas</span><span class="sxs-lookup"><span data-stu-id="754d3-137">The per second rate of received application creation requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-138">Errores de unión a sesión de MCU de AS</span><span class="sxs-lookup"><span data-stu-id="754d3-138">AS MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-139">Número de errores de unión a sesión de MCU de AS</span><span class="sxs-lookup"><span data-stu-id="754d3-139">The number of AS MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-140">Errores de unión a sesión de MCU de AV</span><span class="sxs-lookup"><span data-stu-id="754d3-140">AV MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-141">Errores de unión a sesión de MCU de AV</span><span class="sxs-lookup"><span data-stu-id="754d3-141">The number of AV MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-142">Tiempo medio de inicio de aplicación (ms)</span><span class="sxs-lookup"><span data-stu-id="754d3-142">Average Application Startup Time (ms)</span></span></p></td>
<td><p><span data-ttu-id="754d3-143">Promedio de tiempo de inicio de la aplicación en milisegundos</span><span class="sxs-lookup"><span data-stu-id="754d3-143">The average application startup time in Milliseconds</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-144">Duración media de sesión (ms)</span><span class="sxs-lookup"><span data-stu-id="754d3-144">Average Lifetime for Session (ms)</span></span></p></td>
<td><p><span data-ttu-id="754d3-145">Duración media de una sesión en milisegundos</span><span class="sxs-lookup"><span data-stu-id="754d3-145">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-146">Errores de unión a sesión de MCU de datos</span><span class="sxs-lookup"><span data-stu-id="754d3-146">Data MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-147">Número de errores de unión a sesión de MCU de datos</span><span class="sxs-lookup"><span data-stu-id="754d3-147">The number of Data MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-148">Latencia de búsqueda de contacto de Exchange (ms)</span><span class="sxs-lookup"><span data-stu-id="754d3-148">Exchange Contact Search Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="754d3-149">Contador que refleja el promedio de tiempo (en milisegundos) que se invierte en buscar un contacto en Exchange</span><span class="sxs-lookup"><span data-stu-id="754d3-149">This counter shows the average time (in milliseconds) to search contact in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-150">Latencia de recuperación de foto HD de Exchange (ms)</span><span class="sxs-lookup"><span data-stu-id="754d3-150">Exchange HD Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="754d3-151">Contador que refleja el promedio de tiempo (en milisegundos) que se invierte en recuperar una foto de Exchange</span><span class="sxs-lookup"><span data-stu-id="754d3-151">This counter shows the average time (in milliseconds) to retrieve a photo from Exchange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-152">Respuestas HTTP 4xx/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-152">HTTP 4xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-153">Ratio por segundo de respuestas con código HTTP 4xx</span><span class="sxs-lookup"><span data-stu-id="754d3-153">The per second rate of responses with HTTP 4xx code</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-154">Respuestas HTTP 5xx/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-154">HTTP 5xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-155">Ratio por segundo de respuestas con código HTTP 5xx</span><span class="sxs-lookup"><span data-stu-id="754d3-155">The per second rate of responses with HTTP 5xx code</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-156">Errores de unión a sesión de MCU de MI</span><span class="sxs-lookup"><span data-stu-id="754d3-156">IM MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-157">Cantidad de errores de unión a sesión de MCU de MI</span><span class="sxs-lookup"><span data-stu-id="754d3-157">The number of IM MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-158">Cantidad de errores de recuperación de foto de Active Directory</span><span class="sxs-lookup"><span data-stu-id="754d3-158">Number of Active Directory Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-159">Cantidad total de errores en recuperar fotos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="754d3-159">The total number of failures to retrieve photos from Active Directory</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-160">Cantidad de errores de búsqueda de contacto</span><span class="sxs-lookup"><span data-stu-id="754d3-160">Number of Contact Search failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-161">Cantidad total de errores de búsqueda de contactos en Exchange</span><span class="sxs-lookup"><span data-stu-id="754d3-161">The total number of failures to search contacts in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-162">Cantidad de errores de deserialización</span><span class="sxs-lookup"><span data-stu-id="754d3-162">Number of Deserialization Failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-163">Cantidad total de errores de deserialización</span><span class="sxs-lookup"><span data-stu-id="754d3-163">The total number of deserialization failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-164">Número de errores de obtención de fotos de alta definición</span><span class="sxs-lookup"><span data-stu-id="754d3-164">Number of HD Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-165">Cantidad total de errores en recuperar fotos HD de Exchange</span><span class="sxs-lookup"><span data-stu-id="754d3-165">The total number of failures to retrieve HD photos from Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-166">Exceso de número máximo de suscripciones por aplicación</span><span class="sxs-lookup"><span data-stu-id="754d3-166">Over The Maximum Subscriptions Per Application</span></span></p></td>
<td><p><span data-ttu-id="754d3-167">Cantidad de solicitudes de suscripción por encima del máximo permitido por aplicación</span><span class="sxs-lookup"><span data-stu-id="754d3-167">The number of Subscription requests over the maximum allowed per application</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-168">Exceso de número máximo de suscripciones por lote</span><span class="sxs-lookup"><span data-stu-id="754d3-168">Over The Maximum Subscriptions Per Batch</span></span></p></td>
<td><p><span data-ttu-id="754d3-169">Cantidad de solicitudes de suscripción por encima del máximo permitido por lote</span><span class="sxs-lookup"><span data-stu-id="754d3-169">The number of Subscription requests over the maximum allowed per batch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-170">Errores de suscripción de presencia</span><span class="sxs-lookup"><span data-stu-id="754d3-170">Presence Subscription Failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-171">Cantidad de errores al suscribir la presencia</span><span class="sxs-lookup"><span data-stu-id="754d3-171">The number of failures to subscribe presence</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-172">Errores de registro de extremos</span><span class="sxs-lookup"><span data-stu-id="754d3-172">Registering Endpoint Failures</span></span></p></td>
<td><p><span data-ttu-id="754d3-173">Cantidad de errores al registrar extremos</span><span class="sxs-lookup"><span data-stu-id="754d3-173">The number of failures to register endpoints</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-174">Solicitudes recibidas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-174">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-175">Ratio por segundo de solicitudes recibidas</span><span class="sxs-lookup"><span data-stu-id="754d3-175">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-176">Solicitudes correctas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-176">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-177">Ratio por segundo de solicitudes correctas (códigos de respuesta HTTP 2xx/3xx)</span><span class="sxs-lookup"><span data-stu-id="754d3-177">The per second rate of successful requests (HTTP 2xx/3xx response codes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-178">Solicitudes de creación de aplicación correctas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-178">Succeeded Create Application Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-179">Ratio por segundo de solicitudes de creación de aplicación correctas</span><span class="sxs-lookup"><span data-stu-id="754d3-179">The per second rate of successful application creation requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-180">Recuento de solicitudes GET pendientes de tiempo agotado</span><span class="sxs-lookup"><span data-stu-id="754d3-180">Timed Out Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-181">Cantidad de solicitudes GET pendientes que han agotado el tiempo</span><span class="sxs-lookup"><span data-stu-id="754d3-181">The number of pending gets that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-182">Total de solicitudes de creación de aplicación recibidas</span><span class="sxs-lookup"><span data-stu-id="754d3-182">Total Application Creation Requests Received</span></span></p></td>
<td><p><span data-ttu-id="754d3-183">Cantidad total de solicitudes de creación de aplicaciones recibido desde que se inició el servicio</span><span class="sxs-lookup"><span data-stu-id="754d3-183">The total number of application creation requests received since the service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-184">Total de respuestas HTTP 4xx</span><span class="sxs-lookup"><span data-stu-id="754d3-184">Total HTTP 4xx Responses</span></span></p></td>
<td><p><span data-ttu-id="754d3-185">Cantidad total de respuestas HTTP 4xx</span><span class="sxs-lookup"><span data-stu-id="754d3-185">The total number of HTTP 4xx responses</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-186">Total de respuestas HTTP 5xx</span><span class="sxs-lookup"><span data-stu-id="754d3-186">Total HTTP 5xx Responses</span></span></p></td>
<td><p><span data-ttu-id="754d3-187">Cantidad total de respuestas HTTP 5xx</span><span class="sxs-lookup"><span data-stu-id="754d3-187">The total number of HTTP 5xx responses</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-188">Solicitudes totales recibidas en el canal de comandos</span><span class="sxs-lookup"><span data-stu-id="754d3-188">Total Requests Received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="754d3-189">Cantidad total de solicitudes recibidas en el canal de comandos</span><span class="sxs-lookup"><span data-stu-id="754d3-189">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-190">Total de solicitudes correctas</span><span class="sxs-lookup"><span data-stu-id="754d3-190">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="754d3-191">Cantidad total de solicitudes correctas</span><span class="sxs-lookup"><span data-stu-id="754d3-191">The total number of requests that succeeded</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-192">Total de sesiones iniciadas</span><span class="sxs-lookup"><span data-stu-id="754d3-192">Total Sessions Initiated</span></span></p></td>
<td><p><span data-ttu-id="754d3-193">Cantidad total de sesiones que se han iniciado desde que se inició el servicio</span><span class="sxs-lookup"><span data-stu-id="754d3-193">The total number of sessions that were initiated since the service was started</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-194">Sesiones totales finalizadas ya que se ha agotado el tiempo de espera de inactividad</span><span class="sxs-lookup"><span data-stu-id="754d3-194">Total Sessions Terminated Because of Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="754d3-195">Cantidad total de sesiones que han finalizado porque se ha agotado el tiempo de espera de inactividad del usuario</span><span class="sxs-lookup"><span data-stu-id="754d3-195">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-196">Total de aplicaciones limitadas</span><span class="sxs-lookup"><span data-stu-id="754d3-196">Total Throttled Applications</span></span></p></td>
<td><p><span data-ttu-id="754d3-197">Cantidad total de aplicaciones limitadas</span><span class="sxs-lookup"><span data-stu-id="754d3-197">The number of throttled applications</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div id="sectionSection1" class="section">

### <a name="performance-counters-for-mcx-mobility-service"></a><span data-ttu-id="754d3-198">Contadores de rendimiento para el servicio de movilidad Mcx</span><span class="sxs-lookup"><span data-stu-id="754d3-198">Performance Counters for Mcx Mobility Service</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="754d3-199">Contador</span><span class="sxs-lookup"><span data-stu-id="754d3-199">Counter</span></span></th>
<th><span data-ttu-id="754d3-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="754d3-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="754d3-201">Duración media de una sesión en milisegundos</span><span class="sxs-lookup"><span data-stu-id="754d3-201">Average Lifetime for a Session in Milliseconds</span></span></p></td>
<td><p><span data-ttu-id="754d3-202">Duración media de una sesión en milisegundos</span><span class="sxs-lookup"><span data-stu-id="754d3-202">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-203">Suscripciones de notificación de inserción actuales</span><span class="sxs-lookup"><span data-stu-id="754d3-203">Current Push Notification Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="754d3-p101">Cantidad actual de suscripciones de notificación de inserción. Esta cantidad representa, junto con el recuento de sesiones actualmente activas, el subconjunto de sesiones actualmente activas que hay registradas para dispositivos Windows Mobile o iPhone.</span><span class="sxs-lookup"><span data-stu-id="754d3-p101">The current number of push notification subscriptions. This number, in conjunction with Currently Active Session Count, represents the subset of currently active sessions that are registered for Windows Mobile or iPhone devices.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-206">Recuento de sondeos de tiempo de espera agotado de red actualmente activa</span><span class="sxs-lookup"><span data-stu-id="754d3-206">Currently Active Network Timeout Poll Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-207">Cantidad de sondeos de red cuyo tiempo de espera se ha agotado</span><span class="sxs-lookup"><span data-stu-id="754d3-207">The number of network polls that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-208">Recuento de sondeos actualmente activos</span><span class="sxs-lookup"><span data-stu-id="754d3-208">Currently Active Poll Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-209">Cantidad de sondeos actualmente activos (conexiones largamente mantenidas con el servidor)</span><span class="sxs-lookup"><span data-stu-id="754d3-209">The number of currently active polls (long-held connections to the server)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-210">Recuento de sesiones actualmente activas</span><span class="sxs-lookup"><span data-stu-id="754d3-210">Currently Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-211">Cantidad actual de extremos registrados en el servicio de movilidad</span><span class="sxs-lookup"><span data-stu-id="754d3-211">Current number of endpoints registered in the Mobility Service</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-212">Recuento de sesiones actualmente activas con suscripciones de presencia activa</span><span class="sxs-lookup"><span data-stu-id="754d3-212">Currently Active Session Count with Active Presence Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="754d3-213">Cantidad de sesiones actualmente activas con suscripciones de presencia activa</span><span class="sxs-lookup"><span data-stu-id="754d3-213">The number of currently active sessions with active presence subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-214">Solicitudes de notificación de inserción erróneas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-214">Push Notification Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-215">Ratio por segundo de notificaciones de inserción erróneas</span><span class="sxs-lookup"><span data-stu-id="754d3-215">The per second rate of failed push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-216">Solicitudes de notificación de inserción correctas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-216">Push Notification Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-217">Ratio por segundo de notificaciones de inserción correctas</span><span class="sxs-lookup"><span data-stu-id="754d3-217">The per second rate of successful push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-218">Solicitudes de notificación de inserción reducidas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-218">Push Notification Requests Throttled/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-219">Ratio por segundo de notificaciones de inserción reducidas</span><span class="sxs-lookup"><span data-stu-id="754d3-219">The per second rate of throttled push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-220">Solicitudes de notificación de inserción/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-220">Push Notification Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-221">Ratio por segundo de notificaciones de inserción enviadas</span><span class="sxs-lookup"><span data-stu-id="754d3-221">The per second rate of sent push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-222">Solicitudes erróneas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-222">Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-223">Ratio por segundo de solicitudes erróneas</span><span class="sxs-lookup"><span data-stu-id="754d3-223">The per second rate of failed requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-224">Solicitudes recibidas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-224">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-225">Ratio por segundo de solicitudes recibidas</span><span class="sxs-lookup"><span data-stu-id="754d3-225">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-226">Solicitudes rechazadas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-226">Requests Rejected/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-227">Ratio por segundo de solicitudes rechazadas</span><span class="sxs-lookup"><span data-stu-id="754d3-227">The per second rate of rejected requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-228">Solicitudes correctas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-228">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-229">Ratio por segundo de solicitudes correctas</span><span class="sxs-lookup"><span data-stu-id="754d3-229">The per second rate of successful requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-230">Solicitudes de inicio de sesión correctas/segundo</span><span class="sxs-lookup"><span data-stu-id="754d3-230">Succeeded Initiate Session Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="754d3-p102">Ratio por segundo de solicitudes Obtener ubicación correctas. Las solicitudes para iniciar una sesión consumen la mayoría de la CPU en el servidor. La carga máxima admitida es 12/segundo. La sostenibilidad depende de otras cargas en el servidor. Iniciar una sesión normalmente significa un inicio de sesión de un usuario que ha tenido la sesión cerrada durante un período prolongado de tiempo.</span><span class="sxs-lookup"><span data-stu-id="754d3-p102">The per second rate of successful Get Location requests. Requests to initiate a session consume the most CPU on the server. Peak supported load is 12/second. Sustainability depends on other loads on the server. Initiate a session typically means a sign-in for a user that has been signed out for an extended period of time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-236">Llamadas de voz entrantes rechazadas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-236">Total Declined Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="754d3-237">Cantidad total de llamadas de voz entrantes que se han rechazado</span><span class="sxs-lookup"><span data-stu-id="754d3-237">The total number of inbound voice calls that were declined</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-238">Llamadas de voz entrantes erróneas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-238">Total Failed Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="754d3-239">Cantidad total de llamadas de voz entrantes erróneas</span><span class="sxs-lookup"><span data-stu-id="754d3-239">The total number of inbound voice calls that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-240">Llamadas de voz salientes erróneas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-240">Total Failed Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="754d3-241">Cantidad total de llamadas de voz salientes erróneas</span><span class="sxs-lookup"><span data-stu-id="754d3-241">The total number of outbound voice calls that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-242">Cantidad de sesiones finalizadas por usuario</span><span class="sxs-lookup"><span data-stu-id="754d3-242">Total number of sessions terminated by user</span></span></p></td>
<td><p><span data-ttu-id="754d3-243">Cantidad de sesiones finalizadas por usuarios</span><span class="sxs-lookup"><span data-stu-id="754d3-243">The total number of sessions terminated by users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-244">Solicitudes de notificación de inserción totales</span><span class="sxs-lookup"><span data-stu-id="754d3-244">Total Push Notification Requests</span></span></p></td>
<td><p><span data-ttu-id="754d3-245">Cantidad total de solicitudes de notificación de inserción</span><span class="sxs-lookup"><span data-stu-id="754d3-245">The total number of push notification requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-246">Solicitudes de notificación de inserción erróneas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-246">Total Push Notification Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="754d3-247">Cantidad total de solicitudes de notificación de inserción erróneas</span><span class="sxs-lookup"><span data-stu-id="754d3-247">The total number of push notification requests that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-248">Solicitudes de notificación de inserción correctas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-248">Total Push Notification Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="754d3-249">Cantidad total de solicitudes de notificación de inserción realizadas correctamente</span><span class="sxs-lookup"><span data-stu-id="754d3-249">The total number of push notification requests that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-250">Solicitudes de notificación de inserción reducidas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-250">Total Push Notification Requests Throttled</span></span></p></td>
<td><p><span data-ttu-id="754d3-251">Cantidad total de solicitudes de notificación de inserción que se han reducido</span><span class="sxs-lookup"><span data-stu-id="754d3-251">The total number of push notification requests that were throttled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-252">Solicitudes erróneas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-252">Total Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="754d3-253">Cantidad total de solicitudes erróneas</span><span class="sxs-lookup"><span data-stu-id="754d3-253">The total number of requests that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-254">Solicitudes totales recibidas en el canal de comandos</span><span class="sxs-lookup"><span data-stu-id="754d3-254">Total Requests received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="754d3-255">Cantidad total de solicitudes recibidas en el canal de comandos</span><span class="sxs-lookup"><span data-stu-id="754d3-255">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-256">Solicitudes rechazadas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-256">Total Requests Rejected</span></span></p></td>
<td><p><span data-ttu-id="754d3-257">Cantidad total de solicitudes que se han rechazado</span><span class="sxs-lookup"><span data-stu-id="754d3-257">The total number of requests that were rejected</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-258">Total de solicitudes correctas</span><span class="sxs-lookup"><span data-stu-id="754d3-258">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="754d3-259">Cantidad total de solicitudes realizadas al servicio de movilidad correctamente</span><span class="sxs-lookup"><span data-stu-id="754d3-259">The total number of requests made to the Mobility Service that succeeded</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-260">Recuento de sesiones iniciadas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-260">Total Session Initiated Count</span></span></p></td>
<td><p><span data-ttu-id="754d3-261">Cantidad total de sesiones que se han iniciado desde que se inició el servicio de movilidad</span><span class="sxs-lookup"><span data-stu-id="754d3-261">The total number of sessions that were initiated since the Mobility Service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-262">Sesiones totales finalizadas ya que se ha agotado el tiempo de espera de inactividad del usuario</span><span class="sxs-lookup"><span data-stu-id="754d3-262">Total Sessions Terminated Because of User Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="754d3-263">Cantidad total de sesiones que han finalizado porque se ha agotado el tiempo de espera de inactividad del usuario</span><span class="sxs-lookup"><span data-stu-id="754d3-263">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d3-264">Llamadas de voz entrantes correctas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-264">Total Successful Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="754d3-265">Cantidad total de llamadas de voz entradas que se han realizado correctamente</span><span class="sxs-lookup"><span data-stu-id="754d3-265">The total number of inbound voice calls that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d3-266">Llamadas de voz salientes correctas totales</span><span class="sxs-lookup"><span data-stu-id="754d3-266">Total Successful Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="754d3-267">Cantidad total de llamadas de voz salientes que se han realizado correctamente</span><span class="sxs-lookup"><span data-stu-id="754d3-267">The total number of outbound voice calls that were successful</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="754d3-268">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="754d3-268">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

