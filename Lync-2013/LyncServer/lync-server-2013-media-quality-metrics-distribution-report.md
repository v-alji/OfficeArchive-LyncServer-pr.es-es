---
title: 'Lync Server 2013: informe de distribución de métricas de calidad media'
description: 'Lync Server 2013: informe de distribución de métricas de calidad media.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Metrics Distribution Report
ms:assetid: d07996e6-b0a5-4ff8-9512-ab707762b4e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205262(v=OCS.15)
ms:contentKeyID: 48185409
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: def56580477dadf989268e1fc24fcec7776c00d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399695"
---
# <a name="the-media-quality-metrics-distribution-report-in-lync-server-2013"></a><span data-ttu-id="5edee-103">El informe de distribución de métricas de calidad media en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5edee-103">The Media Quality Metrics Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5edee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5edee-104">

<span> </span></span></span>

<span data-ttu-id="5edee-105">_**Última modificación del tema:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="5edee-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="5edee-p101">El Informe de distribución de métricas de calidad de medios permite ver un gráfico que muestra los valores de distribución de una métrica de calidad de experiencia como la vibración o la pérdida de paquetes. Por ejemplo, supongamos que los usuarios realizan un total de 10 llamadas telefónicas. Estas 10 llamadas telefónicas tienen los siguientes tiempos de ida y vuelta:</span><span class="sxs-lookup"><span data-stu-id="5edee-p101">The Media Quality Metrics Distribution Report enables you to see a graph that shows the distribution values for a Quality of Experience metric such as jitter or packet loss. For example, suppose your users make a total of 10 phone calls; those 10 calls report the following roundtrip times:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5edee-108">Número de llamada</span><span class="sxs-lookup"><span data-stu-id="5edee-108">Call Number</span></span></th>
<th><span data-ttu-id="5edee-109">Tiempo de ida y vuelta (milisegundos)</span><span class="sxs-lookup"><span data-stu-id="5edee-109">Roundtrip Time (milliseconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5edee-110">1</span><span class="sxs-lookup"><span data-stu-id="5edee-110">1</span></span></p></td>
<td><p><span data-ttu-id="5edee-111">50</span><span class="sxs-lookup"><span data-stu-id="5edee-111">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5edee-112">2</span><span class="sxs-lookup"><span data-stu-id="5edee-112">2</span></span></p></td>
<td><p><span data-ttu-id="5edee-113">50</span><span class="sxs-lookup"><span data-stu-id="5edee-113">50</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5edee-114">3</span><span class="sxs-lookup"><span data-stu-id="5edee-114">3</span></span></p></td>
<td><p><span data-ttu-id="5edee-115">50</span><span class="sxs-lookup"><span data-stu-id="5edee-115">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5edee-116">4</span><span class="sxs-lookup"><span data-stu-id="5edee-116">4</span></span></p></td>
<td><p><span data-ttu-id="5edee-117">50</span><span class="sxs-lookup"><span data-stu-id="5edee-117">50</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5edee-118">5</span><span class="sxs-lookup"><span data-stu-id="5edee-118">5</span></span></p></td>
<td><p><span data-ttu-id="5edee-119">50</span><span class="sxs-lookup"><span data-stu-id="5edee-119">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5edee-120">6</span><span class="sxs-lookup"><span data-stu-id="5edee-120">6</span></span></p></td>
<td><p><span data-ttu-id="5edee-121">50</span><span class="sxs-lookup"><span data-stu-id="5edee-121">50</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5edee-122">7</span><span class="sxs-lookup"><span data-stu-id="5edee-122">7</span></span></p></td>
<td><p><span data-ttu-id="5edee-123">50</span><span class="sxs-lookup"><span data-stu-id="5edee-123">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5edee-124">4,8</span><span class="sxs-lookup"><span data-stu-id="5edee-124">8</span></span></p></td>
<td><p><span data-ttu-id="5edee-125">4550</span><span class="sxs-lookup"><span data-stu-id="5edee-125">4550</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5edee-126">99,999</span><span class="sxs-lookup"><span data-stu-id="5edee-126">9</span></span></p></td>
<td><p><span data-ttu-id="5edee-127">50</span><span class="sxs-lookup"><span data-stu-id="5edee-127">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5edee-128">base10</span><span class="sxs-lookup"><span data-stu-id="5edee-128">10</span></span></p></td>
<td><p><span data-ttu-id="5edee-129">50</span><span class="sxs-lookup"><span data-stu-id="5edee-129">50</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5edee-130">El promedio de esos tiempos de ida y vuelta es de 500 milisegundos (5000 dividido entre 10).</span><span class="sxs-lookup"><span data-stu-id="5edee-130">The average for those roundtrip times is 500 milliseconds (5000 divided by 10).</span></span> <span data-ttu-id="5edee-131">500 milisegundos es un tiempo de ida y vuelta extremadamente grande; como resultado, puede creer que tiene un problema grave con la congestión de la red.</span><span class="sxs-lookup"><span data-stu-id="5edee-131">Five hundred milliseconds is an extremely large roundtrip time; as a result, you might believe that you have a serious problem with network congestion.</span></span> <span data-ttu-id="5edee-132">(Los tiempos de ida y vuelta largos suelen ser el resultado de las redes sobrecargadas).</span><span class="sxs-lookup"><span data-stu-id="5edee-132">(Long roundtrip times are typically the result of overloaded networks.)</span></span>

<span data-ttu-id="5edee-133">En realidad, por supuesto, el 90% de tus llamadas ha sido un excelente tiempo de ida y vuelta; simplemente tenías una llamada incorrecta que sesgaba los resultados totales.</span><span class="sxs-lookup"><span data-stu-id="5edee-133">In reality, of course, 90% of your calls had excellent round trip times; you merely had one bad call that skewed the overall results.</span></span> <span data-ttu-id="5edee-134">Si solo miras el tiempo medio de ida y vuelta, puedes pasar a una conclusión muy incorrecta.</span><span class="sxs-lookup"><span data-stu-id="5edee-134">If you only look at the average roundtrip time you might jump to a very wrong conclusion.</span></span>

<span data-ttu-id="5edee-p104">Con el informe de distribución de métricas de calidad de medios le será más fácil evitar llegar a conclusiones erróneas, ya que muestra una distribución gráfica de una métrica especificada (como el tiempo de ida y vuelta). Con estos gráficos le resultará más fácil ver que tiene nueve llamadas buenas y una llamada muy mala. Probablemente querrá seguir investigando esa única llamada, pero el hecho de que 9 de las 10 llamadas fueran muy buenas sugiere que no hay ningún motivo para efectuar ningún cambio drástico en la red, al menos no en este momento.</span><span class="sxs-lookup"><span data-stu-id="5edee-p104">The Media Quality Metrics Distribution Report helps you avoid jumping to wrong conclusions by showing you a graphical distribution of a specified metric (such as round trip time). These graphs can help make it clear that you had nine very good calls and one very bad call. Admittedly, you might still want to further investigate that one call; however, the fact that 9 out of the 10 calls were very good suggests that there is no reason to make any drastic changes to your network, at least not at this point in time.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="5edee-138">Filtros</span><span class="sxs-lookup"><span data-stu-id="5edee-138">Filters</span></span>

<span data-ttu-id="5edee-p105">Los filtros se emplean para recuperar un conjunto de datos más específico o para ver los datos devueltos de diferentes formas. En la tabla siguiente, se muestran los filtros que se pueden utilizar en el informe de distribución de métricas de calidad de medios.</span><span class="sxs-lookup"><span data-stu-id="5edee-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Media Quality Metrics Distribution Report.</span></span>

### <a name="media-quality-metrics-distribution-report-filters"></a><span data-ttu-id="5edee-141">Filtros del informe de distribución de métricas de calidad de medios</span><span class="sxs-lookup"><span data-stu-id="5edee-141">Media Quality Metrics Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5edee-142">Nombre</span><span class="sxs-lookup"><span data-stu-id="5edee-142">Name</span></span></th>
<th><span data-ttu-id="5edee-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="5edee-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5edee-144"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="5edee-144"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="5edee-p106">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="5edee-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="5edee-147">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="5edee-147">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="5edee-p107">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="5edee-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="5edee-150">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="5edee-150">7/7/2012</span></span></p>
<p><span data-ttu-id="5edee-151">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="5edee-151">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="5edee-152">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="5edee-152">7/3/2012</span></span></p>
<p><span data-ttu-id="5edee-153">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="5edee-153">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5edee-154"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="5edee-154"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="5edee-p108">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="5edee-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="5edee-157">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="5edee-157">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="5edee-p109">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="5edee-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="5edee-160">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="5edee-160">7/7/2012</span></span></p>
<p><span data-ttu-id="5edee-161">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="5edee-161">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="5edee-162">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="5edee-162">7/3/2012</span></span></p>
<p><span data-ttu-id="5edee-163">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="5edee-163">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5edee-164"><strong>Mínimo en eje x</strong></span><span class="sxs-lookup"><span data-stu-id="5edee-164"><strong>Minimum in x axis</strong></span></span></p></td>
<td><p><span data-ttu-id="5edee-165">Valor mínimo que se visualizará en el eje X del gráfico.</span><span class="sxs-lookup"><span data-stu-id="5edee-165">Lowest value to be displayed on the X axis of the graph.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5edee-166"><strong>Máximo en eje x</strong></span><span class="sxs-lookup"><span data-stu-id="5edee-166"><strong>Maximum in x axis</strong></span></span></p></td>
<td><p><span data-ttu-id="5edee-167">Valor máximo que se visualizará en el eje X del gráfico.</span><span class="sxs-lookup"><span data-stu-id="5edee-167">Highest value to be displayed on the X axis of the graph.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5edee-168"><strong>Tipo de acceso</strong></span><span class="sxs-lookup"><span data-stu-id="5edee-168"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="5edee-p110">Indica si el cliente había iniciado sesión en la red interna o en la externa cuando se realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="5edee-p110">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="5edee-171">[Todas]</span><span class="sxs-lookup"><span data-stu-id="5edee-171">[All]</span></span></p></li>
<li><p><span data-ttu-id="5edee-172">Interno</span><span class="sxs-lookup"><span data-stu-id="5edee-172">Internal</span></span></p></li>
<li><p><span data-ttu-id="5edee-173">Externo</span><span class="sxs-lookup"><span data-stu-id="5edee-173">External</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5edee-174"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="5edee-174"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="5edee-p111">Indica si un cliente externo estaba utilizando una conexión de red privada virtual (VPN) cuando se realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="5edee-p111">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="5edee-177">[Todas]</span><span class="sxs-lookup"><span data-stu-id="5edee-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="5edee-178">VPN</span><span class="sxs-lookup"><span data-stu-id="5edee-178">VPN</span></span></p></li>
<li><p><span data-ttu-id="5edee-179">Distinto de VPN</span><span class="sxs-lookup"><span data-stu-id="5edee-179">Non-VPN</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5edee-180"><strong>Tipo de red</strong></span><span class="sxs-lookup"><span data-stu-id="5edee-180"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="5edee-p112">Indica el tipo de red al que estaba conectado el cliente cuando realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="5edee-p112">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="5edee-183">[Todas]</span><span class="sxs-lookup"><span data-stu-id="5edee-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="5edee-184">Cableada</span><span class="sxs-lookup"><span data-stu-id="5edee-184">Wired</span></span></p></li>
<li><p><span data-ttu-id="5edee-185">Inalámbrica</span><span class="sxs-lookup"><span data-stu-id="5edee-185">Wireless</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="5edee-186">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5edee-186">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

