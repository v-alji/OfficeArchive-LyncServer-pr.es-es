---
title: 'Lync Server 2013: informe de rendimiento del servidor'
description: 'Lync Server 2013: informe de rendimiento del servidor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server Performance Report
ms:assetid: 942bb39a-1790-498e-9d99-8f6ce2d155c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615018(v=OCS.15)
ms:contentKeyID: 48184879
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aed9b3b9eeec4487dce4d401df0d70ffba89677b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441882"
---
# <a name="server-performance-report-in-lync-server-2013"></a><span data-ttu-id="47795-103">Informe de rendimiento del servidor en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47795-103">Server Performance Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47795-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47795-104">

<span> </span></span></span>

<span data-ttu-id="47795-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="47795-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="47795-106">El informe rendimiento del servidor proporciona una lista de servidores de Microsoft Lync Server 2013 que han experimentado el mayor porcentaje de llamadas inadecuadas.</span><span class="sxs-lookup"><span data-stu-id="47795-106">The Server Performance Report provides a list of Microsoft Lync Server 2013 servers that have experienced the highest-percentage of poor calls.</span></span> <span data-ttu-id="47795-107">El informe desglosa los servidores por tipo de servidor y notifica diferentes estadísticas para los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="47795-107">The report breaks down servers by server type, reporting separate statistics for the following types:</span></span>

  - <span data-ttu-id="47795-108">Servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="47795-108">Mediation Server</span></span>

  - <span data-ttu-id="47795-109">Servidor de conferencia A/V</span><span class="sxs-lookup"><span data-stu-id="47795-109">A/V Conferencing Server</span></span>

  - <span data-ttu-id="47795-110">Servidor perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="47795-110">A/V Edge Server</span></span>

  - <span data-ttu-id="47795-111">Puerta de enlace (servidor de mediación)</span><span class="sxs-lookup"><span data-stu-id="47795-111">Gateway (Mediation Server)</span></span>

  - <span data-ttu-id="47795-112">Puerta de enlace (desvío del servidor de mediación)</span><span class="sxs-lookup"><span data-stu-id="47795-112">Gateway (Mediation Server bypass)</span></span>

  - <span data-ttu-id="47795-113">Vídeo (incluye métricas de vídeo para servidores de conferencia A/V y servidores perimetrales A/V)</span><span class="sxs-lookup"><span data-stu-id="47795-113">Video (including video metrics for A/V Conferencing servers and A/V Edge servers)</span></span>

  - <span data-ttu-id="47795-114">Uso compartido de aplicaciones (incluye métricas de uso compartido de aplicaciones para servidores de conferencia A/V y servidores perimetrales A/V)</span><span class="sxs-lookup"><span data-stu-id="47795-114">Application Sharing (including application sharing metrics for A/V Conferencing servers and A/V Edge servers)</span></span>

<span data-ttu-id="47795-p102">Es importante recordar que la clasificación mostrada en este informe es una clasificación relativa. Por ejemplo, supongamos que el servidor con el peor rendimiento tuvo una llamada deficiente entre las 1000 llamadas realizadas. Eso supone un porcentaje más que aceptable del 0,1 %. Pero, si es el servidor de peor rendimiento (es decir, todos los demás servidores tienen un porcentaje de llamadas deficientes incluso inferior al 0,1 %), aparecerá en el informe de rendimiento del servidor.</span><span class="sxs-lookup"><span data-stu-id="47795-p102">It’s important to note that the ranking shown in this report as relative rankings. For example, suppose your worst-performing server had one poor call among its 1,000 placed calls. That's a more-than-acceptable percentage of .1%. However, if that's the worst-performing server you have (that is, if all your other servers have a poor call percentage even lower than .1%), then that server will still appear on the Server Performance Report.</span></span>

<div>

## <a name="accessing-the-server-performance-report"></a><span data-ttu-id="47795-119">Acceso al informe de rendimiento del servidor</span><span class="sxs-lookup"><span data-stu-id="47795-119">Accessing the Server Performance Report</span></span>

<span data-ttu-id="47795-120">El informe de acceso del servidor es accesible desde la página principal de informes de supervisión.</span><span class="sxs-lookup"><span data-stu-id="47795-120">The Server Performance Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="47795-121">Puede explorar en profundidad el [Informe de la lista de llamadas en Lync Server 2013](lync-server-2013-call-list-report.md) haciendo clic en cualquiera de las siguientes métricas:</span><span class="sxs-lookup"><span data-stu-id="47795-121">You can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="47795-122">Volumen de llamadas</span><span class="sxs-lookup"><span data-stu-id="47795-122">Call volume</span></span>

  - <span data-ttu-id="47795-123">Porcentaje de llamadas deficientes</span><span class="sxs-lookup"><span data-stu-id="47795-123">Poor call percentage</span></span>

<span data-ttu-id="47795-124">Además, puede navegar hasta el informe de tendencias de calidad de medios del servidor haciendo clic en las métricas siguientes:</span><span class="sxs-lookup"><span data-stu-id="47795-124">In addition, you can drill down to the Server Media Quality Trend Report by clicking the following metric:</span></span>

  - <span data-ttu-id="47795-125">Tendencia</span><span class="sxs-lookup"><span data-stu-id="47795-125">Trend</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-server-performance-report"></a><span data-ttu-id="47795-126">Uso óptimo del informe de rendimiento del servidor</span><span class="sxs-lookup"><span data-stu-id="47795-126">Making the Best Use of the Server Performance Report</span></span>

<span data-ttu-id="47795-p104">El informe de rendimiento del servidor ofrece varias maneras de filtrar los datos; por ejemplo, puede filtrar por tipo de red (llamadas realizadas desde una conexión cableada frente a las llamadas realizadas desde una conexión inalámbrica) y tipo de acceso (llamadas realizadas desde dentro del firewall frente a las llamadas realizadas desde fuera del firewall). Para ver el informe de rendimiento del servidor, es buena idea utilizar estos filtros. Por ejemplo, supongamos que tiene un servidor de mediación con un porcentaje de llamadas deficientes del 3,24 %. Si solo consulta las llamadas inalámbricas, el mismo servidor podría tener un porcentaje de llamadas deficientes cercano al 20 %. Eso significa que el servidor tenía dificultades con las llamadas inalámbricas, un problema que quedó oculto en parte porque el servidor no tenía problemas con las llamadas cableadas.</span><span class="sxs-lookup"><span data-stu-id="47795-p104">The Server Performance Report provides a number of ways to filter data; for example, you can filter on network type (calls made from a wired connection vs. calls made from a wireless connection) and access type (calls made from inside the firewall vs. calls made from outside the firewall). It's a good idea when viewing the server performance report to make use of these filters. For example, suppose you have a Mediation Server that has a poor call percentage of 3.24%. If you look solely at wireless calls, that same server might have a poor call percentage approaching 20%. That means that the server was having difficulty with wireless calls, a problem that is partially obscured because the server was not having problems with wired calls.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="47795-132">Filtros</span><span class="sxs-lookup"><span data-stu-id="47795-132">Filters</span></span>

<span data-ttu-id="47795-p105">Los filtros constituyen un modo de obtener un conjunto de datos más acorde con lo que se busca o para ver los datos devueltos de diversas formas. Por ejemplo, el informe de rendimiento del servidor permite realizar tareas como filtrar los datos devueltos por el tipo de servidor o por el tipo de red (con cable o inalámbrica). También se puede elegir cómo agrupar los datos. En este caso, las llamadas se agrupan por hora, día, semana o mes.</span><span class="sxs-lookup"><span data-stu-id="47795-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Server Performance Report enables you to do such things as filter the returned data by server type or by network type (that is, wired or wireless). You can also choose how data should be grouped. In this case, data is grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="47795-137">En la siguiente tabla se muestran los filtros que se pueden usar en el informe de rendimiento del servidor.</span><span class="sxs-lookup"><span data-stu-id="47795-137">The following table lists the filters that you can use with the Server Performance Report.</span></span>

### <a name="server-performance-report-filters"></a><span data-ttu-id="47795-138">Filtros del informe de rendimiento del servidor</span><span class="sxs-lookup"><span data-stu-id="47795-138">Server Performance Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47795-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="47795-139">Name</span></span></th>
<th><span data-ttu-id="47795-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="47795-140">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47795-141"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="47795-141"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-p106">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="47795-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="47795-144">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="47795-144">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="47795-p107">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="47795-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="47795-147">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="47795-147">7/7/2012</span></span></p>
<p><span data-ttu-id="47795-148">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="47795-148">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="47795-149">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="47795-149">7/3/2012</span></span></p>
<p><span data-ttu-id="47795-150">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="47795-150">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-151"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="47795-151"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-p108">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="47795-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="47795-154">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="47795-154">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="47795-p109">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="47795-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="47795-157">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="47795-157">7/7/2012</span></span></p>
<p><span data-ttu-id="47795-158">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="47795-158">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="47795-159">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="47795-159">7/3/2012</span></span></p>
<p><span data-ttu-id="47795-160">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="47795-160">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-161"><strong>Tipo de servidor</strong></span><span class="sxs-lookup"><span data-stu-id="47795-161"><strong>Server type</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-p110">Indica el tipo de servidor cuyo rendimiento necesita notificarse. Seleccione una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="47795-p110">Indicates the type of server whose performance should be reported. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="47795-164">[Todas]</span><span class="sxs-lookup"><span data-stu-id="47795-164">[All]</span></span></p></li>
<li><p><span data-ttu-id="47795-165">Servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="47795-165">Mediation Server</span></span></p></li>
<li><p><span data-ttu-id="47795-166">Servidor de conferencia A/V</span><span class="sxs-lookup"><span data-stu-id="47795-166">A/V Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="47795-167">Servidor perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="47795-167">A/V Edge Server</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-168"><strong>Superior N</strong></span><span class="sxs-lookup"><span data-stu-id="47795-168"><strong>Top N</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-p111">Indica la cantidad de servidores (en función de su escaso porcentaje de llamadas) que se va a mostrar en cada categoría. Por ejemplo, si selecciona <strong>5</strong>, aparecerán los cinco servidores con peor rendimiento. Seleccione una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="47795-p111">Indicates the number of servers (based on their poor call percentage) to be displayed in each category. For example, if you select <strong>5</strong> then the five poorest-performing servers are displayed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="47795-172">[Todas]</span><span class="sxs-lookup"><span data-stu-id="47795-172">[All]</span></span></p></li>
<li><p><span data-ttu-id="47795-173">5</span><span class="sxs-lookup"><span data-stu-id="47795-173">5</span></span></p></li>
<li><p><span data-ttu-id="47795-174">base10</span><span class="sxs-lookup"><span data-stu-id="47795-174">10</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-175"><strong>Tipo de acceso</strong></span><span class="sxs-lookup"><span data-stu-id="47795-175"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-p112">Indica si el cliente había iniciado sesión en la red interna o en la externa cuando se realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="47795-p112">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="47795-178">[Todas]</span><span class="sxs-lookup"><span data-stu-id="47795-178">[All]</span></span></p></li>
<li><p><span data-ttu-id="47795-179">Interno</span><span class="sxs-lookup"><span data-stu-id="47795-179">Internal</span></span></p></li>
<li><p><span data-ttu-id="47795-180">Externo</span><span class="sxs-lookup"><span data-stu-id="47795-180">External</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-181"><strong>Tipo de red</strong></span><span class="sxs-lookup"><span data-stu-id="47795-181"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-p113">Indica el tipo de red al que estaba conectado el cliente cuando realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="47795-p113">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="47795-184">[Todas]</span><span class="sxs-lookup"><span data-stu-id="47795-184">[All]</span></span></p></li>
<li><p><span data-ttu-id="47795-185">Cableada</span><span class="sxs-lookup"><span data-stu-id="47795-185">Wired</span></span></p></li>
<li><p><span data-ttu-id="47795-186">Inalámbrica</span><span class="sxs-lookup"><span data-stu-id="47795-186">Wireless</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-187"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="47795-187"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-p114">Indica si un cliente externo estaba utilizando una conexión de red privada virtual (VPN) cuando se realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="47795-p114">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="47795-190">[Todas]</span><span class="sxs-lookup"><span data-stu-id="47795-190">[All]</span></span></p></li>
<li><p><span data-ttu-id="47795-191">VPN</span><span class="sxs-lookup"><span data-stu-id="47795-191">VPN</span></span></p></li>
<li><p><span data-ttu-id="47795-192">Distinto de VPN</span><span class="sxs-lookup"><span data-stu-id="47795-192">Non-VPN</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="47795-193">Métricas</span><span class="sxs-lookup"><span data-stu-id="47795-193">Metrics</span></span>

<span data-ttu-id="47795-194">En la tabla siguiente se muestra la información que recoge el informe de rendimiento del servidor.</span><span class="sxs-lookup"><span data-stu-id="47795-194">The following table lists the information provided in the Server Performance Report.</span></span>

### <a name="server-performance-report-metrics-audio-call-summary"></a><span data-ttu-id="47795-195">Métricas del informe de rendimiento del servidor: resumen de llamadas de audio</span><span class="sxs-lookup"><span data-stu-id="47795-195">Server Performance Report Metrics: Audio Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47795-196">Nombre</span><span class="sxs-lookup"><span data-stu-id="47795-196">Name</span></span></th>
<th><span data-ttu-id="47795-197">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="47795-197">Can Sort On</span></span></th>
<th><span data-ttu-id="47795-198">Descripción</span><span class="sxs-lookup"><span data-stu-id="47795-198">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47795-199"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="47795-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-200">No</span><span class="sxs-lookup"><span data-stu-id="47795-200">No</span></span></p></td>
<td><p><span data-ttu-id="47795-201">Nombre/dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="47795-201">Name/IP address of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-202"><strong>Volumen de llamadas</strong></span><span class="sxs-lookup"><span data-stu-id="47795-202"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-203">No</span><span class="sxs-lookup"><span data-stu-id="47795-203">No</span></span></p></td>
<td><p><span data-ttu-id="47795-204">Cantidad total de llamadas realizadas.</span><span class="sxs-lookup"><span data-stu-id="47795-204">Total number of calls made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-205"><strong>Porcentaje de llamadas deficientes</strong></span><span class="sxs-lookup"><span data-stu-id="47795-205"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-206">No</span><span class="sxs-lookup"><span data-stu-id="47795-206">No</span></span></p></td>
<td><p><span data-ttu-id="47795-p115">Cantidad total de llamadas clasificadas como deficientes. Una llamada deficiente es aquella durante la que al menos uno de los valores medidos supera el valor permitido, por ejemplo, una llamada con un exceso de vibraciones.</span><span class="sxs-lookup"><span data-stu-id="47795-p115">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-209"><strong>Recorrido de ida y vuelta (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-209"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-210">Sí</span><span class="sxs-lookup"><span data-stu-id="47795-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="47795-p116">Tiempo medio (en milisegundos) necesario para que un paquete de protocolo de transporte en tiempo real (RTP) llegue a otro extremo y vuelva. Los tiempos de ida y vuelta de 100 milisegundos o menos se consideran de calidad aceptable.</span><span class="sxs-lookup"><span data-stu-id="47795-p116">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="47795-p117">Los valores elevados en los tiempos del recorrido de ida y vuelta pueden deberse a que se trata de enrutamientos de llamadas internacionales, una configuración incorrecta del enrutamiento o a la sobrecarga en el servidor de medios y causan dificultades en las conversaciones de audio en tiempo real bidireccionales.</span><span class="sxs-lookup"><span data-stu-id="47795-p117">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-215"><strong>Degradación (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-215"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-216">Sí</span><span class="sxs-lookup"><span data-stu-id="47795-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="47795-217">Cantidad media de degradación de la puntuación de opinión media (MOS) experimentada durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="47795-217">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="47795-218">Los valores de degradación oscilan entre un mínimo de 0,0 y un máximo de 5,0.</span><span class="sxs-lookup"><span data-stu-id="47795-218">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="47795-219">Un valor de 0,5 o menos constituye una degradación aceptable.</span><span class="sxs-lookup"><span data-stu-id="47795-219">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="47795-220">Históricamente, las puntuaciones de opinión media se calculaban haciendo que los usuarios puntuaran la calidad de una llamada en una escala del 1 al 5.</span><span class="sxs-lookup"><span data-stu-id="47795-220">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="47795-221">En Lync Server, el servidor de supervisión usa un conjunto de algoritmos para predecir cómo los usuarios habrían calificado una llamada.</span><span class="sxs-lookup"><span data-stu-id="47795-221">In Lync Server, the Monitoring Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="47795-p119">Los valores altos de degradación pueden ser producto de la congestión, falta de ancho de banda, congestión o interferencias en una conexión inalámbrica, o la sobrecarga de un servidor multimedia o servidor de extremo. Una degradación alta causa la distorsión o la pérdida del audio.</span><span class="sxs-lookup"><span data-stu-id="47795-p119">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-224"><strong>Pérdida de paquetes</strong></span><span class="sxs-lookup"><span data-stu-id="47795-224"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-225">Sí</span><span class="sxs-lookup"><span data-stu-id="47795-225">Yes</span></span></p></td>
<td><p><span data-ttu-id="47795-p120">Tasa media de pérdida de paquetes RTP (se habla de pérdida de paquetes cuando los paquetes RTP, un protocolo utilizado para transmitir audio y vídeo a través de Internet, no llegan a su destino). Una tasa alta de pérdida se suele deber a la congestión, falta de ancho de banda, congestión o interferencias en una conexión inalámbrica o la sobrecarga de un servidor de medios. Generalmente, la pérdida de paquetes da lugar a la pérdida o la distorsión del audio.</span><span class="sxs-lookup"><span data-stu-id="47795-p120">Average rate of real-time transport protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-229"><strong>Vibración (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-229"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-230">Sí</span><span class="sxs-lookup"><span data-stu-id="47795-230">Yes</span></span></p></td>
<td><p><span data-ttu-id="47795-231">Valor medio de las vibraciones detectadas entre la llagada de paquetes RTP.</span><span class="sxs-lookup"><span data-stu-id="47795-231">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="47795-232">(La vibración es una medida de la &quot; irregularidad &quot; de una llamada). Los valores de vibración elevada suelen estar causados por una congestión o un servidor multimedia sobrecargado y tienen como resultado una distorsión o pérdida de audio.</span><span class="sxs-lookup"><span data-stu-id="47795-232">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-233"><strong>Tasa de recuperación de muestras ocultas</strong></span><span class="sxs-lookup"><span data-stu-id="47795-233"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-234">Sí</span><span class="sxs-lookup"><span data-stu-id="47795-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="47795-p122">Tasa media de muestras de audio ocultas respecto a la cantidad total de muestras. Una muestra de audio oculta es una técnica que se emplea para suavizar la transición brusca que normalmente supondría la pérdida de paquetes de red. Los valores elevados indican niveles igualmente elevados de aplicación de ocultación de pérdidas a causa de la pérdida de paquetes o de las vibraciones, y dan lugar a la distorsión o pérdida del audio.</span><span class="sxs-lookup"><span data-stu-id="47795-p122">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-237"><strong>Tasa de recuperación de muestras extendidas</strong></span><span class="sxs-lookup"><span data-stu-id="47795-237"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-238">Sí</span><span class="sxs-lookup"><span data-stu-id="47795-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="47795-p123">Tasa media de muestras de audio extendidas respecto a la cantidad total de muestras. El audio extendido es el audio que se expande para ayudar a mantener el nivel de calidad de la llamada cuando se detecta la pérdida de paquetes en la red. Los valores elevados indican un grado igualmente elevado de extensión de las muestras a causa de las vibraciones, y dan lugar a un audio robótico o distorsionado.</span><span class="sxs-lookup"><span data-stu-id="47795-p123">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-241"><strong>Tasa de recuperación de muestras comprimidas</strong></span><span class="sxs-lookup"><span data-stu-id="47795-241"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-242">Sí</span><span class="sxs-lookup"><span data-stu-id="47795-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="47795-p124">Tasa media de muestras de audio comprimidas respecto a la cantidad total de muestras. El audio comprimido es el audio que se comprime para ayudar a mantener el nivel de calidad de la llamada cuando se detecta la pérdida de paquetes en la red. Los valores altos indican un elevado grado de compresión de las muestras a causa de las vibraciones y las consecuencias son un audio acelerado o distorsionado.</span><span class="sxs-lookup"><span data-stu-id="47795-p124">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="server-performance-report-metrics-video-call-summary"></a><span data-ttu-id="47795-245">Métricas del informe de rendimiento del servidor: resumen de llamadas de vídeo</span><span class="sxs-lookup"><span data-stu-id="47795-245">Server Performance Report Metrics: Video Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47795-246">Nombre</span><span class="sxs-lookup"><span data-stu-id="47795-246">Name</span></span></th>
<th><span data-ttu-id="47795-247">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="47795-247">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="47795-248">Descripción</span><span class="sxs-lookup"><span data-stu-id="47795-248">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47795-249"><strong>Tipo de llamada/tipo de extremo</strong></span><span class="sxs-lookup"><span data-stu-id="47795-249"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-250">No</span><span class="sxs-lookup"><span data-stu-id="47795-250">No</span></span></p></td>
<td><p><span data-ttu-id="47795-p125">Cuando se hace clic en este elemento, el informe muestra información detallada sobre las llamadas de ese tipo. Los tipos de llamadas son:</span><span class="sxs-lookup"><span data-stu-id="47795-p125">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="47795-253">Llamadas de punto a punto de UC</span><span class="sxs-lookup"><span data-stu-id="47795-253">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="47795-254">Sesiones de conferencia de UC</span><span class="sxs-lookup"><span data-stu-id="47795-254">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="47795-255">Sesiones de conferencia de RTC</span><span class="sxs-lookup"><span data-stu-id="47795-255">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="47795-256">Llamadas RTC: desvío de medios</span><span class="sxs-lookup"><span data-stu-id="47795-256">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="47795-257">Llamadas RTC (sin desvío): sección de UC</span><span class="sxs-lookup"><span data-stu-id="47795-257">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="47795-258">Llamadas RTC (sin desvío): sección de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="47795-258">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="47795-259">Otros tipos de llamada</span><span class="sxs-lookup"><span data-stu-id="47795-259">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-260"><strong>Volumen de llamadas</strong></span><span class="sxs-lookup"><span data-stu-id="47795-260"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-261">No</span><span class="sxs-lookup"><span data-stu-id="47795-261">No</span></span></p></td>
<td><p><span data-ttu-id="47795-262">Cantidad total de llamadas por tipo.</span><span class="sxs-lookup"><span data-stu-id="47795-262">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-263"><strong>Porcentaje de llamadas deficientes</strong></span><span class="sxs-lookup"><span data-stu-id="47795-263"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-264">No</span><span class="sxs-lookup"><span data-stu-id="47795-264">No</span></span></p></td>
<td><p><span data-ttu-id="47795-p126">Cantidad total de llamadas clasificadas como deficientes. Una llamada deficiente es aquella durante la que al menos uno de los valores medidos supera el valor permitido, por ejemplo, una llamada con un exceso de vibraciones.</span><span class="sxs-lookup"><span data-stu-id="47795-p126">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-267"><strong>Volumen de llamadas (llamada inalámbrica)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-267"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-268">No</span><span class="sxs-lookup"><span data-stu-id="47795-268">No</span></span></p></td>
<td><p><span data-ttu-id="47795-269">Cantidad total de llamadas que ha empleado una conexión inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="47795-269">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-270"><strong>Volumen de llamadas (llamada VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-270"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-271">No</span><span class="sxs-lookup"><span data-stu-id="47795-271">No</span></span></p></td>
<td><p><span data-ttu-id="47795-272">Cantidad total de llamadas que ha empleado una conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="47795-272">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-273"><strong>Volumen de llamadas (llamada externa)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-273"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-274">No</span><span class="sxs-lookup"><span data-stu-id="47795-274">No</span></span></p></td>
<td><p><span data-ttu-id="47795-275">Cantidad de llamadas que ha empleado una conexión externa, es decir, una conexión fuera de la red interna.</span><span class="sxs-lookup"><span data-stu-id="47795-275">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-276"><strong>Velocidad de bits media (Kbits/s)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-276"><strong>Avg bit-rate (Kbits/s)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-277">No</span><span class="sxs-lookup"><span data-stu-id="47795-277">No</span></span></p></td>
<td><p><span data-ttu-id="47795-278">Velocidad de bits de vídeo media (en kilobits por segundo).</span><span class="sxs-lookup"><span data-stu-id="47795-278">Average video bit rate (in kilobits per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-279"><strong>% de velocidad de bits baja</strong></span><span class="sxs-lookup"><span data-stu-id="47795-279"><strong>Low bit-rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-280">No</span><span class="sxs-lookup"><span data-stu-id="47795-280">No</span></span></p></td>
<td><p><span data-ttu-id="47795-281">Porcentaje de la llamada con una velocidad de bits baja.</span><span class="sxs-lookup"><span data-stu-id="47795-281">Percentage of the call where the bit rate was low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-282"><strong>Pérdida de paquetes de salida</strong></span><span class="sxs-lookup"><span data-stu-id="47795-282"><strong>Outbound packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-283">No</span><span class="sxs-lookup"><span data-stu-id="47795-283">No</span></span></p></td>
<td><p><span data-ttu-id="47795-p127">Pérdida de paquetes de salida del Protocolo de transporte en tiempo real (RTP). (La pérdida de paquetes se produce cuando los paquetes de RTP, un protocolo usado para transmitir audio y vídeo a través de Internet, no llegan a su destino). Las altas tasas de pérdidas suelen estar causadas por congestión, falta de ancho de banda, congestión inalámbrica o interferencias, o un servidor de medios sobrecargado. La pérdida de paquetes suele producir distorsión o pérdida de audio.</span><span class="sxs-lookup"><span data-stu-id="47795-p127">Real-Time Transport Protocol (RTP) packet loss for outbound packets. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-287"><strong>% fotogramas congelados</strong></span><span class="sxs-lookup"><span data-stu-id="47795-287"><strong>Frozen frame %</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-288">No</span><span class="sxs-lookup"><span data-stu-id="47795-288">No</span></span></p></td>
<td><p><span data-ttu-id="47795-p128">Porcentaje de fotogramas "congelados". En un fotograma congelado, el vídeo detiene su avance mientras que la parte de audio de la llamada continúa.</span><span class="sxs-lookup"><span data-stu-id="47795-p128">Percentage of “frozen” frames. In a frozen frame, the video stops advancing while the audio portion of the call continues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-291"><strong>Velocidad de fotogramas media de salida</strong></span><span class="sxs-lookup"><span data-stu-id="47795-291"><strong>Outbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-292">No</span><span class="sxs-lookup"><span data-stu-id="47795-292">No</span></span></p></td>
<td><p><span data-ttu-id="47795-293">Velocidad de fotogramas media para las transmisiones de salida durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="47795-293">Average frame rate for outbound transmissions during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-294"><strong>Velocidad de fotogramas media de entrada</strong></span><span class="sxs-lookup"><span data-stu-id="47795-294"><strong>Inbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-295">No</span><span class="sxs-lookup"><span data-stu-id="47795-295">No</span></span></p></td>
<td><p><span data-ttu-id="47795-296">Velocidad de fotogramas media para las transmisiones de entrada durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="47795-296">Average frame rate for incoming transmissions during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-297"><strong>% de velocidad de fotogramas baja de entrada</strong></span><span class="sxs-lookup"><span data-stu-id="47795-297"><strong>Inbound low frame rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-298">No</span><span class="sxs-lookup"><span data-stu-id="47795-298">No</span></span></p></td>
<td><p><span data-ttu-id="47795-299">Porcentaje de la llamada con una velocidad de bits baja para el vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="47795-299">Percentage of the call where the bit rate for incoming video was low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-300"><strong>% de estado del cliente</strong></span><span class="sxs-lookup"><span data-stu-id="47795-300"><strong>Client health %</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="47795-301">Indica el estado relativo del dispositivo cliente durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="47795-301">Indicates the relative health of the client device during the call.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="server-performance-report-metrics-application-sharing-call-summary"></a><span data-ttu-id="47795-302">Métricas del informe de rendimiento del servidor: resumen de llamadas de uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="47795-302">Server Performance Report Metrics: Application Sharing Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47795-303">Nombre</span><span class="sxs-lookup"><span data-stu-id="47795-303">Name</span></span></th>
<th><span data-ttu-id="47795-304">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="47795-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="47795-305">Descripción</span><span class="sxs-lookup"><span data-stu-id="47795-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47795-306"><strong>Tipo de llamada/tipo de extremo</strong></span><span class="sxs-lookup"><span data-stu-id="47795-306"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-307">No</span><span class="sxs-lookup"><span data-stu-id="47795-307">No</span></span></p></td>
<td><p><span data-ttu-id="47795-p129">Cuando se hace clic en este elemento, el informe muestra información detallada sobre las llamadas de ese tipo. Los tipos de llamadas son:</span><span class="sxs-lookup"><span data-stu-id="47795-p129">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="47795-310">Llamadas de punto a punto de UC</span><span class="sxs-lookup"><span data-stu-id="47795-310">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="47795-311">Sesiones de conferencia de UC</span><span class="sxs-lookup"><span data-stu-id="47795-311">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="47795-312">Sesiones de conferencia de RTC</span><span class="sxs-lookup"><span data-stu-id="47795-312">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="47795-313">Llamadas RTC: desvío de medios</span><span class="sxs-lookup"><span data-stu-id="47795-313">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="47795-314">Llamadas RTC (sin desvío): sección de UC</span><span class="sxs-lookup"><span data-stu-id="47795-314">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="47795-315">Llamadas RTC (sin desvío): sección de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="47795-315">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="47795-316">Otros tipos de llamada</span><span class="sxs-lookup"><span data-stu-id="47795-316">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-317"><strong>Volumen de llamadas</strong></span><span class="sxs-lookup"><span data-stu-id="47795-317"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-318">No</span><span class="sxs-lookup"><span data-stu-id="47795-318">No</span></span></p></td>
<td><p><span data-ttu-id="47795-319">Cantidad total de llamadas por tipo.</span><span class="sxs-lookup"><span data-stu-id="47795-319">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-320"><strong>Porcentaje de llamadas deficientes</strong></span><span class="sxs-lookup"><span data-stu-id="47795-320"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-321">No</span><span class="sxs-lookup"><span data-stu-id="47795-321">No</span></span></p></td>
<td><p><span data-ttu-id="47795-p130">Cantidad total de llamadas clasificadas como deficientes. Una llamada deficiente es aquella durante la que al menos uno de los valores medidos supera el valor permitido, por ejemplo, una llamada con un exceso de vibraciones.</span><span class="sxs-lookup"><span data-stu-id="47795-p130">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-324"><strong>Volumen de llamadas (llamada inalámbrica)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-324"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-325">No</span><span class="sxs-lookup"><span data-stu-id="47795-325">No</span></span></p></td>
<td><p><span data-ttu-id="47795-326">Cantidad total de llamadas que ha empleado una conexión inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="47795-326">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-327"><strong>Volumen de llamadas (llamada VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-327"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-328">No</span><span class="sxs-lookup"><span data-stu-id="47795-328">No</span></span></p></td>
<td><p><span data-ttu-id="47795-329">Cantidad total de llamadas que ha empleado una conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="47795-329">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-330"><strong>Volumen de llamadas (llamada externa)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-330"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-331">No</span><span class="sxs-lookup"><span data-stu-id="47795-331">No</span></span></p></td>
<td><p><span data-ttu-id="47795-332">Cantidad de llamadas que ha empleado una conexión externa, es decir, una conexión fuera de la red interna.</span><span class="sxs-lookup"><span data-stu-id="47795-332">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-333"><strong>Vibración (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="47795-333"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-334">No</span><span class="sxs-lookup"><span data-stu-id="47795-334">No</span></span></p></td>
<td><p><span data-ttu-id="47795-335">Valor medio de las vibraciones detectadas entre la llagada de paquetes RTP.</span><span class="sxs-lookup"><span data-stu-id="47795-335">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="47795-336">(La vibración es una medida de la &quot; irregularidad &quot; de una llamada). Los valores de vibración elevada suelen estar causados por una congestión o un servidor multimedia sobrecargado y tienen como resultado una distorsión o pérdida de audio.</span><span class="sxs-lookup"><span data-stu-id="47795-336">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-337"><strong>Unidireccional relativo medio</strong></span><span class="sxs-lookup"><span data-stu-id="47795-337"><strong>Avg. relative one way</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-338">No</span><span class="sxs-lookup"><span data-stu-id="47795-338">No</span></span></p></td>
<td><p><span data-ttu-id="47795-p132">Retraso unidireccional relativo medio entre dos extremos de medios. Es una medición de la latencia de un solo salto.</span><span class="sxs-lookup"><span data-stu-id="47795-p132">Average relative one-way delay between two media endpoints. This is a single-hop latency measure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47795-341"><strong>Latencia media de procesamiento de iconos RDP</strong></span><span class="sxs-lookup"><span data-stu-id="47795-341"><strong>Avg. RDP tile processing latency</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-342">No</span><span class="sxs-lookup"><span data-stu-id="47795-342">No</span></span></p></td>
<td><p><span data-ttu-id="47795-p133">Latencia media de procesamiento de iconos RDP en el servidor de conferencias AS durante el transcurso de la sesión de visualización. Esta métrica no incluye la latencia de red. Una media alta refleja un retraso mayor en la experiencia de visualización. Un servidor de conferencias sobrecargado podría experimentar una media mayor de retrasos.</span><span class="sxs-lookup"><span data-stu-id="47795-p133">The average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session. This metric does not cover network latency. A high average reflects a longer delay in the viewing experience. An overloaded conferencing server may experience higher average delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47795-347"><strong>% total de iconos dañados</strong></span><span class="sxs-lookup"><span data-stu-id="47795-347"><strong>Total spoiled tile %</strong></span></span></p></td>
<td><p><span data-ttu-id="47795-348">No</span><span class="sxs-lookup"><span data-stu-id="47795-348">No</span></span></p></td>
<td><p><span data-ttu-id="47795-349">Porcentaje total de iconos RDP dañados.</span><span class="sxs-lookup"><span data-stu-id="47795-349">Total percentage of spoiled RDP tiles.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="47795-350">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47795-350">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

