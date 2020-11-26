---
title: 'Lync Server 2013: informe Resumen de la Conferencia'
description: 'Lync Server 2013: informe Resumen de la Conferencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Summary Report
ms:assetid: 62f54812-5700-45a3-8526-8f58b0f77fbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558656(v=OCS.15)
ms:contentKeyID: 48184299
ms.date: 09/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d9c0b8ad7280d2c7336282c14f46e6b5d6a1aec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434497"
---
# <a name="conference-summary-report-in-lync-server-2013"></a><span data-ttu-id="fb0fe-103">Informe de Resumen de conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb0fe-103">Conference Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb0fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb0fe-104">

<span> </span></span></span>

<span data-ttu-id="fb0fe-105">_**Última modificación del tema:** 2014-09-03_</span><span class="sxs-lookup"><span data-stu-id="fb0fe-105">_**Topic Last Modified:** 2014-09-03_</span></span>

<span data-ttu-id="fb0fe-106">El informe de resumen de conferencia ofrece una vista general de las sesiones de conferencia en línea.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-106">The Conference Summary Report provides an overall view of your online conferencing sessions.</span></span> <span data-ttu-id="fb0fe-107">Una conferencia suele implicar a más de 2 usuarios y requiere el uso de los servicios de conferencia de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-107">A conference typically involves more than 2 users and requires the use of Microsoft Lync Server 2013 conferencing services.</span></span> <span data-ttu-id="fb0fe-108">Por comparación, una sesión de punto a punto normalmente implica solo 2 usuarios y no requiere el uso de los servicios de conferencia de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-108">By comparison, a peer-to-peer session typically involves just 2 users and does not require the use of Lync Server's conferencing services.</span></span> <span data-ttu-id="fb0fe-109">Las actividades de punto a punto se notifican en el [Informe de Resumen de actividad punto a punto de Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md).</span><span class="sxs-lookup"><span data-stu-id="fb0fe-109">Peer-to-peer activities are reported on the [Peer-to-Peer Activity Summary Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md).</span></span>

<span data-ttu-id="fb0fe-110">El informe Resumen de la Conferencia no solo le indica el número de conferencias que se han mantenido durante un período de tiempo determinado (cada hora, diariamente, semanalmente, mensualmente), pero también le indica el número total de personas que participaron en esas conferencias, así como el número total de organizadores de conferencia únicos.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-110">The Conference Summary Report not only tells you how many conferences were held during a given time period (hourly, daily, weekly, monthly) but also tells you the total number of people who took part in those conferences, and the total number of unique conference organizers.</span></span>

<span data-ttu-id="fb0fe-111">Un organizador "único" es cualquier persona que programe al menos una conferencia.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-111">A "unique” organizer is anyone who schedules at least one conference.</span></span> <span data-ttu-id="fb0fe-112">Por ejemplo, si Pilar Ackerman programa una conferencia, cuenta como un único organizador.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-112">For example, if Pilar Ackerman schedules one conference she counts as one unique organizer.</span></span> <span data-ttu-id="fb0fe-113">Si Ken Myer programa conferencias de 148, también cuenta como un único organizador.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-113">If Ken Myer schedules 148 conferences he, too counts as one unique organizer.</span></span> <span data-ttu-id="fb0fe-114">Por ejemplo, la siguiente tabla muestra ocho conferencias programadas, pero solo tres organizadores únicos (Ken Myer, Pilar Ackerman y David AHS).</span><span class="sxs-lookup"><span data-stu-id="fb0fe-114">For example, the table below shows 8 conferences scheduled, but just three unique organizers (Ken Myer, Pilar Ackerman, and David Ahs).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb0fe-115">Organizador de la conferencia</span><span class="sxs-lookup"><span data-stu-id="fb0fe-115">Conference Organizer</span></span></th>
<th><span data-ttu-id="fb0fe-116">Fecha de la conferencia</span><span class="sxs-lookup"><span data-stu-id="fb0fe-116">Conference Date</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-117">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="fb0fe-117">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-118">7/7/2012 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-118">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-119">David Ahs</span><span class="sxs-lookup"><span data-stu-id="fb0fe-119">David Ahs</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-120">7/7/2012 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-120">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-121">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="fb0fe-121">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-122">7/7/2012 11:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-122">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-123">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="fb0fe-123">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-124">7/7/2012 11:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-124">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-125">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="fb0fe-125">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-126">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-126">7/7/2012 1:00 PM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-127">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="fb0fe-127">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-128">7/7/2012 2:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-128">7/7/2012 2:00 PM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-129">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="fb0fe-129">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-130">7/2/2012 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-130">7/2/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-131">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="fb0fe-131">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-132">7/2/2012 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-132">7/2/2012 10:00 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fb0fe-133">El informe de resumen de conferencia también indica la cantidad de conferencias que incluyeron audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-133">The Conference Summary Report also indicates how many conferences included audio and/or video.</span></span>

<div>

## <a name="accessing-the-conference-summary-report"></a><span data-ttu-id="fb0fe-134">Acceso al informe de resumen de conferencia</span><span class="sxs-lookup"><span data-stu-id="fb0fe-134">Accessing the Conference Summary Report</span></span>

<span data-ttu-id="fb0fe-p103">Puede obtener acceso al informe de resumen de conferencia desde la página principal de informes de supervisión. Para llegar hasta dicho informe, necesitará hacer clic en las siguientes métricas:</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p103">The Conference Summary Report is accessed from the Monitoring Reports home page. You can drill down to the Conference Activity report by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="fb0fe-137">Total de conferencias</span><span class="sxs-lookup"><span data-stu-id="fb0fe-137">Total conferences</span></span>

  - <span data-ttu-id="fb0fe-138">Total de participantes</span><span class="sxs-lookup"><span data-stu-id="fb0fe-138">Total participants</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-summary-report"></a><span data-ttu-id="fb0fe-139">Usar el informe de resumen de conferencia de la mejor forma posible</span><span class="sxs-lookup"><span data-stu-id="fb0fe-139">Making the Best Use of the Conference Summary Report</span></span>

<span data-ttu-id="fb0fe-140">Los valores totales de la mayoría de las métricas que se usan en el informe de Resumen de conferencia se pueden encontrar en la parte inferior del informe; Desplácese hacia abajo para ver valores como el número total de conferencias mantenidas durante el período de tiempo especificado y el número total de personas que participaron en esas conferencias.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-140">Total values for most of the metrics used on the Conference Summary Report can be found at the bottom of the report; scroll down to see values such as the total number of conferences held during the specified time period, and the total number of people who participated in those conferences.</span></span> <span data-ttu-id="fb0fe-141">Una métrica que no se totaliza en la parte inferior del informe es un total de organizadores únicos de conferencia.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-141">One metric that is not totaled at the bottom of the report is Total unique conference organizers.</span></span> <span data-ttu-id="fb0fe-142">¿Por qué no?</span><span class="sxs-lookup"><span data-stu-id="fb0fe-142">Why not?</span></span> <span data-ttu-id="fb0fe-143">He aquí una de las razones.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-143">Here’s one reason.</span></span> <span data-ttu-id="fb0fe-144">Supongamos que está buscando un mes de datos.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-144">Suppose you are looking at a month's worth of data.</span></span> <span data-ttu-id="fb0fe-145">El día 1 tenía 34 organizadores únicos de conferencia; el día 2 tenía 27 organizadores únicos de conferencia.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-145">On day 1 you had 34 unique conference organizers; on day 2 you had 27 unique conference organizers.</span></span> <span data-ttu-id="fb0fe-146">¿Eso significa que tenía 61 organizadores únicos para esos dos días?</span><span class="sxs-lookup"><span data-stu-id="fb0fe-146">Does that mean you had 61 unique conference organizers for those two days?</span></span> <span data-ttu-id="fb0fe-147">No necesariamente.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-147">Not necessarily.</span></span> <span data-ttu-id="fb0fe-148">Después de todo, las 27 personas que organizaron las conferencias en el día 2 pueden ser entre las 34 personas que organizón las conferencias en el día 1.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-148">After all, all 27 people who organized conferences on day 2 might be among the 34 people who organized conferences on day 1.</span></span> <span data-ttu-id="fb0fe-149">Por ejemplo, en este informe simple, tenga en cuenta que Ken Myer y Pilar Ackerman las conferencias programadas en 7/7/2012 y en 7/2/2012:</span><span class="sxs-lookup"><span data-stu-id="fb0fe-149">For example, in this simple report, note that Ken Myer and Pilar Ackerman scheduled conferences both on 7/7/2012 and on 7/2/2012:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb0fe-150">Organizador de la conferencia</span><span class="sxs-lookup"><span data-stu-id="fb0fe-150">Conference Organizer</span></span></th>
<th><span data-ttu-id="fb0fe-151">Fecha de la conferencia</span><span class="sxs-lookup"><span data-stu-id="fb0fe-151">Conference Date</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-152">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="fb0fe-152">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-153">7/7/2012 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-153">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-154">David Ahs</span><span class="sxs-lookup"><span data-stu-id="fb0fe-154">David Ahs</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-155">7/7/2012 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-155">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-156">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="fb0fe-156">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-157">7/7/2012 11:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-157">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-158">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="fb0fe-158">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-159">7/7/2012 11:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-159">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-160">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="fb0fe-160">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-161">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-161">7/7/2012 1:00 PM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-162">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="fb0fe-162">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-163">7/7/2012 2:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-163">7/7/2012 2:00 PM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-164">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="fb0fe-164">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-165">7/2/2012 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-165">7/2/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-166">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="fb0fe-166">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-167">7/2/2012 10:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-167">7/2/2012 10:00 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fb0fe-168">Para componerse una mejor idea de la cantidad total de usuarios distintos que ha organizado conferencias, cambie el intervalo temporal (por ejemplo, consulte los datos por mes en lugar de por día).</span><span class="sxs-lookup"><span data-stu-id="fb0fe-168">To get a better idea of the total number of unique users who organized conferences, change your time interval; for example, look at the data by month instead of by day.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="fb0fe-169">Filtros</span><span class="sxs-lookup"><span data-stu-id="fb0fe-169">Filters</span></span>

<span data-ttu-id="fb0fe-p105">Los filtros se emplean para recuperar un conjunto de datos más específico o para ver los datos devueltos de diferentes formas. Por ejemplo, el informe de resumen de conferencia le permite elegir cómo agrupar los datos. En este caso, las conferencias se agrupan por hora, día, semana o mes.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Conference Summary Report enables you to choose how data should be grouped. In this case, conferences grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="fb0fe-173">La siguiente tabla muestra los filtros que puede utilizar con el informe de resumen de conferencia.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-173">The following table lists the filters that you can use with the Conference Summary Report.</span></span>

### <a name="conference-summary-report-filters"></a><span data-ttu-id="fb0fe-174">Filtros del informe de resumen de conferencia</span><span class="sxs-lookup"><span data-stu-id="fb0fe-174">Conference Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb0fe-175">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb0fe-175">Name</span></span></th>
<th><span data-ttu-id="fb0fe-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb0fe-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-177"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-177"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-p106">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="fb0fe-180">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-180">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="fb0fe-p107">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="fb0fe-183">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="fb0fe-183">7/7/2012</span></span></p>
<p><span data-ttu-id="fb0fe-184">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="fb0fe-184">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="fb0fe-185">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="fb0fe-185">7/3/2012</span></span></p>
<p><span data-ttu-id="fb0fe-186">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-186">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-187"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-187"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-p108">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="fb0fe-190">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-190">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="fb0fe-p109">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="fb0fe-193">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="fb0fe-193">7/7/2012</span></span></p>
<p><span data-ttu-id="fb0fe-194">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="fb0fe-194">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="fb0fe-195">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="fb0fe-195">7/3/2012</span></span></p>
<p><span data-ttu-id="fb0fe-196">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-196">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-197"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-197"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-p110">Intervalo de tiempo. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p110">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb0fe-200">Cada hora (se puede ver un máximo de 25 horas)</span><span class="sxs-lookup"><span data-stu-id="fb0fe-200">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="fb0fe-201">Cada día (se puede ver un máximo de 31 días)</span><span class="sxs-lookup"><span data-stu-id="fb0fe-201">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="fb0fe-202">Cada semana (se puede ver un máximo de 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="fb0fe-202">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="fb0fe-203">Cada mes (se puede ver un máximo de 12 meses)</span><span class="sxs-lookup"><span data-stu-id="fb0fe-203">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="fb0fe-204">Si las fechas de inicio y finalización superan la cantidad máxima de valores permitidos para el intervalo seleccionado, solo se mostrará la cantidad máxima de valores (comenzando en la fecha de inicio).</span><span class="sxs-lookup"><span data-stu-id="fb0fe-204">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="fb0fe-205">Por ejemplo, si selecciona el intervalo diario con una fecha de inicio de 7/7/2012 y una fecha de finalización de 2/28/2012, los datos se muestran para los días 8/7/2012 12:00 A.M. a 9/7/2012 12:00 A.M. (es decir, un total de 31 días de datos).</span><span class="sxs-lookup"><span data-stu-id="fb0fe-205">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="fb0fe-206">Métricas</span><span class="sxs-lookup"><span data-stu-id="fb0fe-206">Metrics</span></span>

<span data-ttu-id="fb0fe-207">La siguiente tabla incluye la información que ofrece el informe de resumen de conferencia.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-207">The following table the information provided by the Conferences Summary Report.</span></span>

### <a name="conference-summary-report-metrics"></a><span data-ttu-id="fb0fe-208">Métricas del informe de resumen de conferencia</span><span class="sxs-lookup"><span data-stu-id="fb0fe-208">Conference Summary Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb0fe-209">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb0fe-209">Name</span></span></th>
<th><span data-ttu-id="fb0fe-210">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="fb0fe-210">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="fb0fe-211">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb0fe-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-212"><strong>Cada hora</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-212"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="fb0fe-213"><strong>Cada día</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-213"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="fb0fe-214"><strong>Cada semana</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-214"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="fb0fe-215"><strong>Cada mes</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-215"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-216">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-216">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-217">Indica el intervalo temporal que ha seleccionado en la barra de herramientas para filtros.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-217">Indicates the time interval that you selected on the filter toolbar.</span></span> <span data-ttu-id="fb0fe-218">Cuando corresponda, podrá hacer clic en un intervalo temporal determinado para ver información detallada para dicho intervalo.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-218">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="fb0fe-219">Por ejemplo, si está usando el intervalo diario y hace clic en 7/7/2012, verá un desglose por hora de actividad de registro de usuario para esa fecha.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-219">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-220"><strong>Total de conferencias</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-220"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-221">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-221">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-p113">Cantidad total de conferencias (independientemente del tipo de conferencia) celebradas. Al hacer clic en este elemento, el informe le muestra el informe de actividad de conferencia del periodo de tiempo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p113">Total number of conferences (regardless of conference type) that were held. When you click this item, the report shows you the Conference Activity Report for the selected time period.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-224"><strong>Total de participantes</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-224"><strong>Total participants</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-225">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-225">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-p114">Cantidad total de personas que participaron en las conferencias. Al hacer clic en este elemento, el informe le muestra el informe de actividad de conferencia del periodo de tiempo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p114">Total number of people who took part in the conferences. When you click this item, the report shows you the Conference Activity Report for the selected time period.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-228"><strong>Media de participantes por conferencia</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-228"><strong>Average participants per conference</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-229">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-229">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-p115">Cantidad media de participantes que participaron en una conferencia en concreto. Se calcula dividiendo la cantidad total de conferencias por la cantidad total de participantes.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p115">Average number of people who took part in a given conference. Determined by dividing the total conferences by the total participants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-232"><strong>Cantidad total de conferencias A/V</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-232"><strong>Total A/V conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-233">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-233">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-234">Cantidad total de conferencias que incluían audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-234">Total number of conferences that included audio or video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-235"><strong>Total de minutos de conferencia A/V</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-235"><strong>Total A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-236">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-236">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-237">Cantidad total de minutos dedicados a conferencias de audio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-237">Total number of minutes devoted to audio/video conferencing.</span></span></p>
<p><span data-ttu-id="fb0fe-238">La métrica total de minutos de conferencia A/V resume todos los tipos de conferencias de audio y vídeo, entre los que se incluyen: conferencias A/V; Conferencias de mensajería instantánea; conferencias de uso compartido de aplicaciones; conferencias de datos; y conferencias de RTC.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-238">The Total A/V conference minutes metric summarizes all the audio/visual conference types, including: A/V conferences; IM conferences; app sharing conferences; data conferences; and PSTN conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-239"><strong>Total de minutos de participantes en conferencia A/V</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-239"><strong>Total A/V conference participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-240">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-240">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-p116">Cantidad total de minutos de los participantes dedicados a conferencias de audio/vídeo. Por ejemplo, supongamos que un usuario participa 5 minutos en una conferencia de audio/vídeo y un segundo usuario participa 3 minutos en la misma conferencia. Esto hace un total de 8 minutos de los participantes: 5 minutos más 3 minutos.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p116">Total number of participant minutes devoted to audio/video conferencing. For example, suppose one user spends 5 minutes in an audio/video conference and a second user spends 3 minutes in that same conference. That makes a total of 8 participant minutes: 5 minutes plus 3 minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-244"><strong>Cantidad media de minutos en conferencias A/V</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-244"><strong>Average A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-245">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-245">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-246">Cantidad media de minutos por conferencia de audio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-246">Average number of minutes per audio/video conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0fe-247"><strong>Cantidad total de organizadores únicos de conferencias</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-247"><strong>Total number of unique organizers of conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-248">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-248">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-p117">Cantidad total de usuarios que organizaron al menos una conferencia. Los usuarios que organizaron más de una conferencia se cuentan como un único organizador, al igual que ocurre con los usuarios que solo organizaron una única conferencia.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-p117">Total number of users who organized at least one conference. Users who organized more than one conference are counted as one unique organizer, just like users who only organized a single conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0fe-251"><strong>Cantidad total de mensajes de conferencias</strong></span><span class="sxs-lookup"><span data-stu-id="fb0fe-251"><strong>Total conference messages</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0fe-252">No</span><span class="sxs-lookup"><span data-stu-id="fb0fe-252">No</span></span></p></td>
<td><p><span data-ttu-id="fb0fe-253">Cantidad total de mensajes instantáneos enviados durante las conferencias.</span><span class="sxs-lookup"><span data-stu-id="fb0fe-253">Total number of instant messages sent during the conferences.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fb0fe-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb0fe-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

