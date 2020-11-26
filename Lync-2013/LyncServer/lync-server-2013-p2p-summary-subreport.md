---
title: 'Lync Server 2013: subinforme del Resumen P2P'
description: 'Lync Server 2013: subinforme del Resumen P2P.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: P2P Summary Subreport
ms:assetid: fc36185a-3cc5-4167-8c93-8a755fa75ac7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205416(v=OCS.15)
ms:contentKeyID: 48185950
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eda51e76c4ed7b62535a2a2e4ab52982aa6381f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424705"
---
# <a name="p2p-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="703fc-103">Informe de Resumen de P2P en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="703fc-103">P2P Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="703fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="703fc-104">

<span> </span></span></span>

<span data-ttu-id="703fc-105">_**Última modificación del tema:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="703fc-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="703fc-106">El Subinforme de resumen de P2P ofrecer una vista general de todas las sesiones de comunicación de punto a punto que han presentado error.</span><span class="sxs-lookup"><span data-stu-id="703fc-106">The P2P Summary Subreport provides an overall view of your failed peer-to-peer communication sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="703fc-107">Filtros</span><span class="sxs-lookup"><span data-stu-id="703fc-107">Filters</span></span>

<span data-ttu-id="703fc-p101">Los filtros ofrecen el medio para devolver un conjunto de datos más específico o para ver los datos devueltos de diferentes formas. La tabla siguiente muestra los filtros que se pueden utilizar con el Subinforme de resumen de P2P.</span><span class="sxs-lookup"><span data-stu-id="703fc-p101">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-filters"></a><span data-ttu-id="703fc-110">Filtros del Subinforme de resumen de P2P</span><span class="sxs-lookup"><span data-stu-id="703fc-110">P2P Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="703fc-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="703fc-111">Name</span></span></th>
<th><span data-ttu-id="703fc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="703fc-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="703fc-113"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="703fc-113"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="703fc-p102">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="703fc-p102">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="703fc-116">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="703fc-116">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="703fc-p103">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="703fc-p103">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="703fc-119">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="703fc-119">7/7/2012</span></span></p>
<p><span data-ttu-id="703fc-120">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="703fc-120">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="703fc-121">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="703fc-121">7/3/2012</span></span></p>
<p><span data-ttu-id="703fc-122">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="703fc-122">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="703fc-123"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="703fc-123"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="703fc-p104">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización tal como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="703fc-p104">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="703fc-126">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="703fc-126">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="703fc-p105">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="703fc-p105">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="703fc-129">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="703fc-129">7/7/2012</span></span></p>
<p><span data-ttu-id="703fc-130">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="703fc-130">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="703fc-131">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="703fc-131">7/3/2012</span></span></p>
<p><span data-ttu-id="703fc-132">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="703fc-132">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="703fc-133"><strong>Grupo de servidores</strong></span><span class="sxs-lookup"><span data-stu-id="703fc-133"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="703fc-p106">Nombre de dominio completo (FQDN) del grupo de registradores o servidor perimetral. Puede seleccionar un grupo individual o hacer clic en <strong>[Todos]</strong> para ver los datos de todos los grupos. Esta lista desplegable se rellena automáticamente en función de los registros de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="703fc-p106">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="703fc-137">Métricas</span><span class="sxs-lookup"><span data-stu-id="703fc-137">Metrics</span></span>

<span data-ttu-id="703fc-138">En la tabla siguiente se muestra la información recogida en el Subinforme de resumen de P2P.</span><span class="sxs-lookup"><span data-stu-id="703fc-138">The following table lists the information provided in the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-metrics"></a><span data-ttu-id="703fc-139">Métricas del Subinforme de resumen de P2P</span><span class="sxs-lookup"><span data-stu-id="703fc-139">P2P Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="703fc-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="703fc-140">Name</span></span></th>
<th><span data-ttu-id="703fc-141">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="703fc-141">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="703fc-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="703fc-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="703fc-143"><strong>Total de sesiones</strong></span><span class="sxs-lookup"><span data-stu-id="703fc-143"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="703fc-144">No</span><span class="sxs-lookup"><span data-stu-id="703fc-144">No</span></span></p></td>
<td><p><span data-ttu-id="703fc-145">Cantidad total de sesiones, incluidas las sesiones correctas, las sesiones con errores (tanto esperados como inesperados) y las sesiones sin categoría.</span><span class="sxs-lookup"><span data-stu-id="703fc-145">Total number of sessions, including successful sessions, failed sessions (both expected failures and unexpected failures), and uncategorized sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="703fc-146"><strong>Porcentaje de errores</strong></span><span class="sxs-lookup"><span data-stu-id="703fc-146"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="703fc-147">No</span><span class="sxs-lookup"><span data-stu-id="703fc-147">No</span></span></p></td>
<td><p><span data-ttu-id="703fc-148">Porcentaje de las sesiones punto a punto con errores.</span><span class="sxs-lookup"><span data-stu-id="703fc-148">Percentage of peer-to-peer sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="703fc-149"><strong>Sesiones por modalidad</strong></span><span class="sxs-lookup"><span data-stu-id="703fc-149"><strong>Sessions by Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="703fc-150">No</span><span class="sxs-lookup"><span data-stu-id="703fc-150">No</span></span></p></td>
<td><p><span data-ttu-id="703fc-151">Cantidad total de sesiones agrupadas por modalidad (por ejemplo, mensajería instantánea).</span><span class="sxs-lookup"><span data-stu-id="703fc-151">Total number of sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="703fc-152"><strong>Porcentaje de errores por modalidad</strong></span><span class="sxs-lookup"><span data-stu-id="703fc-152"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="703fc-153">No</span><span class="sxs-lookup"><span data-stu-id="703fc-153">No</span></span></p></td>
<td><p><span data-ttu-id="703fc-154">Cantidad total de sesiones con error agrupadas por modalidad (por ejemplo, mensajería instantánea).</span><span class="sxs-lookup"><span data-stu-id="703fc-154">Total number of failed sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="703fc-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="703fc-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

