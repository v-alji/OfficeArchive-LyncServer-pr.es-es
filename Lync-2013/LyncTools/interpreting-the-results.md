---
title: Interpretación de los resultados
description: Interpretación de los resultados.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Interpreting the Results
ms:assetid: dd7f199f-7075-4d88-bb84-49a7e05eb593
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945608(v=OCS.15)
ms:contentKeyID: 51541433
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8342a1ec1e15e42852fc5293f87342e98587a60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443177"
---
# <a name="interpreting-the-results"></a><span data-ttu-id="a68af-103">Interpretación de los resultados</span><span class="sxs-lookup"><span data-stu-id="a68af-103">Interpreting the Results</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a68af-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a68af-104">

<span> </span></span></span>

<span data-ttu-id="a68af-105">_**Última modificación del tema:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="a68af-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="a68af-106">La herramienta Lync Server 2013 stress and Performance (LyncPerfTool.exe) tiene muchos contadores que puede usar para comprender lo que hace el cliente y si se están encontrando problemas.</span><span class="sxs-lookup"><span data-stu-id="a68af-106">The Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) has many counters that you can use to understand what the client is doing and whether it is encountering issues.</span></span>

<div>

## <a name="client-counters"></a><span data-ttu-id="a68af-107">Contadores de cliente</span><span class="sxs-lookup"><span data-stu-id="a68af-107">Client Counters</span></span>

<span data-ttu-id="a68af-108">Cada instancia de LyncPerfTool.exe que se está ejecutando tiene una instancia independiente de los contadores.</span><span class="sxs-lookup"><span data-stu-id="a68af-108">Each instance of LyncPerfTool.exe that is running has a separate instance of the counters.</span></span> <span data-ttu-id="a68af-109">Cada instancia se denomina mediante su identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="a68af-109">Each instance is named by its process ID.</span></span>

<span data-ttu-id="a68af-110">Si los clientes están sobrecargados, pueden producirse problemas.</span><span class="sxs-lookup"><span data-stu-id="a68af-110">If the clients are overloaded, issues can occur.</span></span> <span data-ttu-id="a68af-111">Para evitar estos problemas, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a68af-111">To prevent these issues, do the following:</span></span>

1.  <span data-ttu-id="a68af-112">Supervise la CPU y el uso de memoria en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="a68af-112">Monitor the CPU and the memory usage on the client computers.</span></span> <span data-ttu-id="a68af-113">Si la CPU es sistemática por encima del 90 por ciento, reduzca el número de usuarios.</span><span class="sxs-lookup"><span data-stu-id="a68af-113">If the CPU is consistently above 90 percent, reduce the number of users.</span></span>

2.  <span data-ttu-id="a68af-114">Si el tamaño de la memoria es alto, puede tener problemas si el archivo de paginación no es lo suficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="a68af-114">If the memory footprint is high, you could run into issues if the page file is not big enough.</span></span> <span data-ttu-id="a68af-115">Compruebe que el cargo de asignación no haya alcanzado el límite en el equipo.</span><span class="sxs-lookup"><span data-stu-id="a68af-115">Verify that the Commit Charge is not hitting the limit on the computer.</span></span> <span data-ttu-id="a68af-116">Si se encuentran límites de memoria, considere la posibilidad de aumentar el tamaño del archivo de paginación o reducir el número de usuarios.</span><span class="sxs-lookup"><span data-stu-id="a68af-116">If you are running into memory limits, consider increasing the page file size or reducing the number of users</span></span>

<span data-ttu-id="a68af-117">En las siguientes tablas se enumeran los contadores de rendimiento de LyncPerfTool clave.</span><span class="sxs-lookup"><span data-stu-id="a68af-117">The following tables list the key LyncPerfTool performance counters.</span></span>

<span data-ttu-id="a68af-118">**Información general**</span><span class="sxs-lookup"><span data-stu-id="a68af-118">**General Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-119"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-119"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-120"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-120"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-121">Tiempo invertido en minutos</span><span class="sxs-lookup"><span data-stu-id="a68af-121">Time Spent in Minutes</span></span></p></td>
<td><p><span data-ttu-id="a68af-122">Tiempo transcurrido desde que se inició el proceso.</span><span class="sxs-lookup"><span data-stu-id="a68af-122">Time spent since the process was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-123">Puntos de conexión activos</span><span class="sxs-lookup"><span data-stu-id="a68af-123">Active Endpoints</span></span></p></td>
<td><p><span data-ttu-id="a68af-124">Número de puntos finales conectados actualmente al servidor.</span><span class="sxs-lookup"><span data-stu-id="a68af-124">Number of endpoints currently connected to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-125">Inicios de sesión erróneos</span><span class="sxs-lookup"><span data-stu-id="a68af-125">Failed Logons</span></span></p></td>
<td><p><span data-ttu-id="a68af-126">Número total de errores de inicio de sesión de extremo.</span><span class="sxs-lookup"><span data-stu-id="a68af-126">Total number of endpoint sign-in failures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-127">Intentos de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="a68af-127">Logon Attempts</span></span></p></td>
<td><p><span data-ttu-id="a68af-128">Número total de intentos de inicio de sesión de punto final.</span><span class="sxs-lookup"><span data-stu-id="a68af-128">Total number of endpoint sign-in attempts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-129">Puntos de conexión desconectados</span><span class="sxs-lookup"><span data-stu-id="a68af-129">Endpoints Disconnected</span></span></p></td>
<td><p><span data-ttu-id="a68af-130">Número total de puntos de conexión que se han desconectado.</span><span class="sxs-lookup"><span data-stu-id="a68af-130">Total number of endpoints that have been disconnected.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-131">**Información de presencia**</span><span class="sxs-lookup"><span data-stu-id="a68af-131">**Presence Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-132"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-132"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-133"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-133"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-134">Llamadas de SetPresence</span><span class="sxs-lookup"><span data-stu-id="a68af-134">SetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="a68af-135">Número total de intentos de cambio de presencia.</span><span class="sxs-lookup"><span data-stu-id="a68af-135">Total number of presence change attempts.</span></span> <span data-ttu-id="a68af-136">Para los distintos tipos de cambios de presencia, vea el contador de rendimiento llamadas de SetPresence (tipo de presencia).</span><span class="sxs-lookup"><span data-stu-id="a68af-136">For different types of presence changes, see the SetPresence (Presence Type) Calls Performance Counter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-137">NNN respuestas para SetPresence</span><span class="sxs-lookup"><span data-stu-id="a68af-137">NNN Responses for SetPresence</span></span></p></td>
<td><p><span data-ttu-id="a68af-138">Número total de los códigos de respuesta nnn recibidos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="a68af-138">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-139">Llamadas a GetPresence</span><span class="sxs-lookup"><span data-stu-id="a68af-139">GetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="a68af-140">Número total de intentos de solicitud de presencia.</span><span class="sxs-lookup"><span data-stu-id="a68af-140">Total number of get presence request attempts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-141">NNN respuestas para GetPresence</span><span class="sxs-lookup"><span data-stu-id="a68af-141">NNN Responses for GetPresence</span></span></p></td>
<td><p><span data-ttu-id="a68af-142">Número total de los códigos de respuesta nnn recibidos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="a68af-142">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-143">**Información del servicio de libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="a68af-143">**Address Book service Information**</span></span>

<span data-ttu-id="a68af-144">Esta categoría incluye los contadores usados para supervisar las solicitudes de servicio de descargas de archivos del servicio de libreta de direcciones (ABS) y la libreta de direcciones web de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a68af-144">This category includes counters used to monitor Address Book service (ABS) file downloads and Address Book Web Query service requests.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-145"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-145"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-146"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-146"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-147">Intento de descarga de archivos completo/Delta de ABS</span><span class="sxs-lookup"><span data-stu-id="a68af-147">ABS Full/Delta File Downloads Attempted</span></span></p></td>
<td><p><span data-ttu-id="a68af-148">Número total de solicitudes de descarga de archivos completas o delta intentadas.</span><span class="sxs-lookup"><span data-stu-id="a68af-148">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-149">Descarga de archivo completo/Delta de ABS correctamente</span><span class="sxs-lookup"><span data-stu-id="a68af-149">ABS Full/Delta File Downloads Succeeded</span></span></p></td>
<td><p><span data-ttu-id="a68af-150">Número total de solicitudes de descarga de archivos completas o delta intentadas.</span><span class="sxs-lookup"><span data-stu-id="a68af-150">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-151">Contadores relacionados con el servicio de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="a68af-151">Address Book Web Query service related counters</span></span></p></td>
<td><p><span data-ttu-id="a68af-152">Descarga de archivos de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a68af-152">Address book file download related counters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-153">Intentos de llamadas de ABS WS</span><span class="sxs-lookup"><span data-stu-id="a68af-153">ABS WS Calls attempted</span></span></p></td>
<td><p><span data-ttu-id="a68af-154">Número total de solicitudes de servicio de consulta Web de la libreta de direcciones intentadas.</span><span class="sxs-lookup"><span data-stu-id="a68af-154">Total number of Address Book Web Query service requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-155">Llamadas ABS WS correctas</span><span class="sxs-lookup"><span data-stu-id="a68af-155">ABS WS Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="a68af-156">Número total de solicitudes de servicio de consulta Web de la libreta de direcciones que devolvieron un código de respuesta correcto.</span><span class="sxs-lookup"><span data-stu-id="a68af-156">Total number of Address Book Web Query service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-157">Error en las llamadas de ABS WS</span><span class="sxs-lookup"><span data-stu-id="a68af-157">ABS WS Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="a68af-158">Número total de solicitudes de servicio de consulta Web de la libreta de direcciones que devolvieron un código de respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="a68af-158">Total number of Address Book Web Query service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-159">**Información de la lista de distribución (DL)**</span><span class="sxs-lookup"><span data-stu-id="a68af-159">**Distribution List (DL) Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-160"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-160"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-161"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-161"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-162">Llamadas intentadas</span><span class="sxs-lookup"><span data-stu-id="a68af-162">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="a68af-163">Número total de solicitudes de servicio Web de expansión de la lista de distribución (DLX) intentadas.</span><span class="sxs-lookup"><span data-stu-id="a68af-163">Total number of distribution list expansion (DLX) web service requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-164">Llamadas correctas</span><span class="sxs-lookup"><span data-stu-id="a68af-164">Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="a68af-165">Número total de solicitudes de servicio Web de DLX que devolvieron un código de respuesta satisfactorio.</span><span class="sxs-lookup"><span data-stu-id="a68af-165">Total number of DLX web service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-166">Error en las llamadas</span><span class="sxs-lookup"><span data-stu-id="a68af-166">Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="a68af-167">Número total de solicitudes de servicio Web de DLX que devolvieron un código de respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="a68af-167">Total number of DLX web service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-168">**Información básica de VoIP**</span><span class="sxs-lookup"><span data-stu-id="a68af-168">**VoIP Basic Information**</span></span>

<span data-ttu-id="a68af-169">Los contadores de rendimiento que aparecen a continuación indican números para todas las llamadas de voz a través de IP (VoIP), incluidas las llamadas a servidor de mediación, el servidor de conferencia a/V, el servidor perimetral, la aplicación de grupo de respuesta y el operador automático de conferencia, cuando se habilitan estos escenarios.</span><span class="sxs-lookup"><span data-stu-id="a68af-169">The performance counters listed below report numbers for all Voice over IP (VoIP) calls, including calls to Mediation Server, A/V Conferencing Server, Edge Server, Response Group application, and Conference Auto Attendant, when these scenarios are enabled.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-170"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-170"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-171"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-171"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-172">Llamadas activas</span><span class="sxs-lookup"><span data-stu-id="a68af-172">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="a68af-173">Número total de llamadas de voz entrantes y salientes actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="a68af-173">Total number of incoming/outgoing voice calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-174">Llamadas finalizadas</span><span class="sxs-lookup"><span data-stu-id="a68af-174">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="a68af-175">Número total de llamadas de voz entrantes y salientes que ya han finalizado.</span><span class="sxs-lookup"><span data-stu-id="a68af-175">Total number of incoming/outgoing voice calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-176">Llamadas rechazadas</span><span class="sxs-lookup"><span data-stu-id="a68af-176">Calls Declined</span></span></p></td>
<td><p><span data-ttu-id="a68af-177">Número total de llamadas de voz entrantes rechazadas.</span><span class="sxs-lookup"><span data-stu-id="a68af-177">Total number of incoming voice calls declined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-178">Intentos de llamadas entrantes y salientes</span><span class="sxs-lookup"><span data-stu-id="a68af-178">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="a68af-179">Número total de llamadas de voz entrantes y salientes intentadas.</span><span class="sxs-lookup"><span data-stu-id="a68af-179">Total number of incoming/outgoing voice calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-180">Llamadas entrantes y salientes establecidas</span><span class="sxs-lookup"><span data-stu-id="a68af-180">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="a68af-181">Número total de llamadas de voz entrantes y salientes establecidas.</span><span class="sxs-lookup"><span data-stu-id="a68af-181">Total number of incoming/outgoing voice calls established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-182">Llamadas recibidas NNN</span><span class="sxs-lookup"><span data-stu-id="a68af-182">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="a68af-183">Número total de los códigos de respuesta nnn recibidos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="a68af-183">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-184">Tasa de transferencia de VoIP (%)</span><span class="sxs-lookup"><span data-stu-id="a68af-184">VoIP Pass Rate (%)</span></span></p></td>
<td><p><span data-ttu-id="a68af-185">Llamadas totales establecidas/llamadas totales realizadas.</span><span class="sxs-lookup"><span data-stu-id="a68af-185">Total calls established/Total calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-186">**Información de llamada del servicio de grupo de respuesta**</span><span class="sxs-lookup"><span data-stu-id="a68af-186">**Response Group service Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-187"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-187"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-188"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-188"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-189">Llamadas activas</span><span class="sxs-lookup"><span data-stu-id="a68af-189">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="a68af-190">Número total de llamadas activas a la aplicación de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a68af-190">Total number of active calls to the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-191">Llamadas intentadas</span><span class="sxs-lookup"><span data-stu-id="a68af-191">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="a68af-192">Número total de intentos de llamada.</span><span class="sxs-lookup"><span data-stu-id="a68af-192">Total number of calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-193">**Información de la llamada de mensajería instantánea (mi)**</span><span class="sxs-lookup"><span data-stu-id="a68af-193">**Instant Messaging (IM) Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-194"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-194"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-195"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-195"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-196">Llamadas activas</span><span class="sxs-lookup"><span data-stu-id="a68af-196">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="a68af-197">Número total de llamadas entrantes y salientes de mensajería instantánea en curso.</span><span class="sxs-lookup"><span data-stu-id="a68af-197">Total number of ongoing incoming/outgoing instant messaging calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-198">Llamadas finalizadas</span><span class="sxs-lookup"><span data-stu-id="a68af-198">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="a68af-199">Número total de llamadas de mensajería instantánea entrantes o salientes que ya han finalizado.</span><span class="sxs-lookup"><span data-stu-id="a68af-199">Total number of incoming/outgoing instant messaging calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-200">Llamadas recibidas NNN</span><span class="sxs-lookup"><span data-stu-id="a68af-200">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="a68af-201">Número total de los códigos de respuesta nnn recibidos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="a68af-201">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-202">Mensajes INSTANTÁNEos recibidos/enviados</span><span class="sxs-lookup"><span data-stu-id="a68af-202">IM Messages Received/Sent</span></span></p></td>
<td><p><span data-ttu-id="a68af-203">Número total de mensajes recibidos o enviados para todas las sesiones.</span><span class="sxs-lookup"><span data-stu-id="a68af-203">Total number of messages received or sent for all sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-204">Intentos de llamadas entrantes y salientes</span><span class="sxs-lookup"><span data-stu-id="a68af-204">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="a68af-205">Número total de intentos de llamadas entrantes y salientes de mensajes instantáneos.</span><span class="sxs-lookup"><span data-stu-id="a68af-205">Total number of incoming/outgoing instant messaging calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-206">Llamadas entrantes y salientes establecidas</span><span class="sxs-lookup"><span data-stu-id="a68af-206">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="a68af-207">Número total de llamadas de mensajes instantáneos entrantes o salientes que se han establecido.</span><span class="sxs-lookup"><span data-stu-id="a68af-207">Total number of incoming/outgoing instant message calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-208">**Información de llamadas de uso compartido de aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="a68af-208">**App Sharing Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-209"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-209"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-210"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-210"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-211">Llamadas activas</span><span class="sxs-lookup"><span data-stu-id="a68af-211">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="a68af-212">Número total de llamadas de uso compartido de aplicaciones entrantes y salientes en curso.</span><span class="sxs-lookup"><span data-stu-id="a68af-212">Total number of ongoing incoming/outgoing application sharing calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-213">Llamadas finalizadas</span><span class="sxs-lookup"><span data-stu-id="a68af-213">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="a68af-214">Número total de llamadas de uso compartido de aplicaciones entrantes o salientes que ya se han finalizado.</span><span class="sxs-lookup"><span data-stu-id="a68af-214">Total number of incoming/outgoing application sharing calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-215">Llamadas recibidas NNN</span><span class="sxs-lookup"><span data-stu-id="a68af-215">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="a68af-216">Número total de los códigos de respuesta nnn recibidos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="a68af-216">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-217">Intentos de llamadas entrantes y salientes</span><span class="sxs-lookup"><span data-stu-id="a68af-217">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="a68af-218">Número total de llamadas de uso compartido de aplicaciones entrantes o salientes.</span><span class="sxs-lookup"><span data-stu-id="a68af-218">Total number of incoming/outgoing application sharing calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-219">Llamadas entrantes y salientes establecidas</span><span class="sxs-lookup"><span data-stu-id="a68af-219">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="a68af-220">Número total de llamadas de uso compartido de aplicaciones entrantes o salientes establecidas.</span><span class="sxs-lookup"><span data-stu-id="a68af-220">Total number of incoming/outgoing application sharing calls established.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-221">**Información de la llamada de CAA**</span><span class="sxs-lookup"><span data-stu-id="a68af-221">**CAA Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-222"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-222"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-223"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-223"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-224">Llamadas activas</span><span class="sxs-lookup"><span data-stu-id="a68af-224">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="a68af-225">Número total de llamadas de red telefónica conmutada (RTC) entrantes y salientes actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="a68af-225">Total number of incoming/outgoing public switched telephone network (PSTN) calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-226">Llamadas finalizadas</span><span class="sxs-lookup"><span data-stu-id="a68af-226">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="a68af-227">Número total de llamadas RTC entrantes y salientes que ya se han finalizado.</span><span class="sxs-lookup"><span data-stu-id="a68af-227">Total number of incoming/outgoing PSTN calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-228">Intentos de llamadas entrantes y salientes</span><span class="sxs-lookup"><span data-stu-id="a68af-228">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="a68af-229">Número total de intentos de llamadas RTC entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="a68af-229">Total number of incoming/outgoing PSTN calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-230">Llamadas entrantes y salientes establecidas</span><span class="sxs-lookup"><span data-stu-id="a68af-230">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="a68af-231">Número total de llamadas RTC entrantes y salientes establecidas.</span><span class="sxs-lookup"><span data-stu-id="a68af-231">Total number of incoming/outgoing PSTN calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-232">**Información sobre la Conferencia**</span><span class="sxs-lookup"><span data-stu-id="a68af-232">**Conference Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-233"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-233"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-234"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-234"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-235">Conferencias de mensajería instantánea activas</span><span class="sxs-lookup"><span data-stu-id="a68af-235">Active Instant Messaging Conferences</span></span></p></td>
<td><p><span data-ttu-id="a68af-236">Número total de conferencias de mensajería instantánea en curso.</span><span class="sxs-lookup"><span data-stu-id="a68af-236">Total number of ongoing instant messaging conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-237">Conferencias de audio y vídeo activas</span><span class="sxs-lookup"><span data-stu-id="a68af-237">Active Audio/Video Conferences</span></span></p></td>
<td><p><span data-ttu-id="a68af-238">Número total de conferencias de audio o vídeo (A/V) en curso.</span><span class="sxs-lookup"><span data-stu-id="a68af-238">Total number of ongoing audio/video (A/V) conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-239">Conferencias de uso compartido de aplicaciones activas</span><span class="sxs-lookup"><span data-stu-id="a68af-239">Active Application Sharing Conferences</span></span></p></td>
<td><p><span data-ttu-id="a68af-240">Número total de conferencias de uso compartido de aplicaciones en curso.</span><span class="sxs-lookup"><span data-stu-id="a68af-240">Total number of ongoing application sharing conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-241">Número de participantes</span><span class="sxs-lookup"><span data-stu-id="a68af-241">Number of Participants</span></span></p></td>
<td><p><span data-ttu-id="a68af-242">Número total de participantes actualmente conectados a conferencias.</span><span class="sxs-lookup"><span data-stu-id="a68af-242">Total number of participants currently connected to conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a68af-243">Error de programación en Conferencia</span><span class="sxs-lookup"><span data-stu-id="a68af-243">Conference Schedule Failure</span></span></p></td>
<td><p><span data-ttu-id="a68af-244">Número total de errores al intentar programar una conferencia.</span><span class="sxs-lookup"><span data-stu-id="a68af-244">Total number of failures while trying to schedule a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-245">Error al unirse a la Conferencia</span><span class="sxs-lookup"><span data-stu-id="a68af-245">Join Conference Failure</span></span></p></td>
<td><p><span data-ttu-id="a68af-246">Número total de errores al intentar conectarse a una conferencia.</span><span class="sxs-lookup"><span data-stu-id="a68af-246">Total number of failures while trying to connect to a conference.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a68af-247">**Contadores de cliente de UCWA**</span><span class="sxs-lookup"><span data-stu-id="a68af-247">**UCWA Client Counters**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a68af-248"><strong>Contador de rendimiento</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-248"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="a68af-249"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="a68af-249"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a68af-250">Número total de combinaciones de IMMCU correctas</span><span class="sxs-lookup"><span data-stu-id="a68af-250">Total Number of IMMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="a68af-251">Número total de conferencias de mensajería instantánea combinadas.</span><span class="sxs-lookup"><span data-stu-id="a68af-251">Total number of instant messaging conferences joined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a68af-252">Número total de combinaciones de DMCU correctas</span><span class="sxs-lookup"><span data-stu-id="a68af-252">Total Number of DMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="a68af-253">Número total de conferencias A/V combinadas.</span><span class="sxs-lookup"><span data-stu-id="a68af-253">Total number of A/V conferences joined.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a68af-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a68af-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

