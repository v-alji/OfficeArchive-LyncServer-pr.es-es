---
title: 'Lync Server 2013: subinforme del Resumen de la Conferencia'
description: 'Lync Server 2013: subinforme del Resumen de la Conferencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Summary Subreport
ms:assetid: 2fc1d2bf-34f5-4093-a6e2-250ec1f1b004
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204779(v=OCS.15)
ms:contentKeyID: 48183742
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0612ce1adb8a6b0fdea5e3bf70b88346f7c08044
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434490"
---
# <a name="conference-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="ac035-103">Informe subinforme Resumen de la Conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac035-103">Conference Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac035-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac035-104">

<span> </span></span></span>

<span data-ttu-id="ac035-105">_**Última modificación del tema:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="ac035-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="ac035-p101">El Subinforme de resumen de conferencia proporciona información general de sesiones de conferencia fallidas. Estas sesiones fallidas se dividen además por tipo de sesión: sesiones de foco y sesiones MCU.</span><span class="sxs-lookup"><span data-stu-id="ac035-p101">The Conference Summary Subreport provides an overall view of failed conference sessions. These failed sessions are further broken down by session type: Focus sessions and MCU sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="ac035-108">Filtros</span><span class="sxs-lookup"><span data-stu-id="ac035-108">Filters</span></span>

<span data-ttu-id="ac035-p102">Los filtros se emplean para recuperar un conjunto de datos más específico o para ver los datos devueltos de diferentes formas. En la tabla siguiente, se muestran los filtros que se pueden utilizar en el Subinforme de resumen de conferencia.</span><span class="sxs-lookup"><span data-stu-id="ac035-p102">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-filters"></a><span data-ttu-id="ac035-111">Filtros del Subinforme de resumen de conferencia</span><span class="sxs-lookup"><span data-stu-id="ac035-111">Conference Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac035-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac035-112">Name</span></span></th>
<th><span data-ttu-id="ac035-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac035-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac035-114"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-114"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-p103">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ac035-p103">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="ac035-117">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="ac035-117">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ac035-p104">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="ac035-p104">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ac035-120">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ac035-120">7/7/2012</span></span></p>
<p><span data-ttu-id="ac035-121">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="ac035-121">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ac035-122">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ac035-122">7/3/2012</span></span></p>
<p><span data-ttu-id="ac035-123">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="ac035-123">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac035-124"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-124"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-p105">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ac035-p105">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="ac035-127">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="ac035-127">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ac035-p106">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="ac035-p106">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ac035-130">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ac035-130">7/7/2012</span></span></p>
<p><span data-ttu-id="ac035-131">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="ac035-131">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ac035-132">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ac035-132">7/3/2012</span></span></p>
<p><span data-ttu-id="ac035-133">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="ac035-133">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac035-134"><strong>Grupo de servidores</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-134"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-p107">Nombre de dominio completo (FQDN) del grupo de registradores o servidor perimetral. Puede seleccionar un grupo individual o hacer clic en <strong>[Todos]</strong> para ver los datos de todos los grupos. Esta lista desplegable se rellena automáticamente en función de los registros de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ac035-p107">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="ac035-138">Métricas</span><span class="sxs-lookup"><span data-stu-id="ac035-138">Metrics</span></span>

<span data-ttu-id="ac035-139">La siguiente tabla contiene la información que recoge el Subinforme de resumen de conferencia.</span><span class="sxs-lookup"><span data-stu-id="ac035-139">The following table lists the information provided in the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-metrics"></a><span data-ttu-id="ac035-140">Métricas del Subinforme de resumen de conferencia</span><span class="sxs-lookup"><span data-stu-id="ac035-140">Conference Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac035-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac035-141">Name</span></span></th>
<th><span data-ttu-id="ac035-142">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="ac035-142">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ac035-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac035-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac035-144"><strong>Total de conferencias</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-144"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-145">No</span><span class="sxs-lookup"><span data-stu-id="ac035-145">No</span></span></p></td>
<td><p><span data-ttu-id="ac035-146">Cantidad total de conferencias que ha tenido lugar.</span><span class="sxs-lookup"><span data-stu-id="ac035-146">Total number of conferences held.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac035-147"><strong>Total de sesiones de conferencias</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-147"><strong>Total conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-148">No</span><span class="sxs-lookup"><span data-stu-id="ac035-148">No</span></span></p></td>
<td><p><span data-ttu-id="ac035-p108">Cantidad total de sesiones de conferencia. Una única conferencia puede tener varias sesiones; por ejemplo, una conferencia podría incluir tanto una sesión de foco como una sesión MCU.</span><span class="sxs-lookup"><span data-stu-id="ac035-p108">Total number of conference sessions. A single conference can have multiple sessions; for example, a conference might include both a Focus session and an MCU session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac035-151"><strong>Porcentaje de errores de sesión generales</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-151"><strong>Overall session failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-152">No</span><span class="sxs-lookup"><span data-stu-id="ac035-152">No</span></span></p></td>
<td><p><span data-ttu-id="ac035-153">Porcentaje de todas las conferencias fallidas.</span><span class="sxs-lookup"><span data-stu-id="ac035-153">Percentage of all conferences that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac035-154"><strong>Sesiones de foco</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-154"><strong>Focus sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-155">No</span><span class="sxs-lookup"><span data-stu-id="ac035-155">No</span></span></p></td>
<td><p><span data-ttu-id="ac035-156">Cantidad total de sesiones de foco.</span><span class="sxs-lookup"><span data-stu-id="ac035-156">Total number of Focus sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac035-157"><strong>Porcentaje de errores de foco</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-157"><strong>Focus failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-158">No</span><span class="sxs-lookup"><span data-stu-id="ac035-158">No</span></span></p></td>
<td><p><span data-ttu-id="ac035-159">Porcentaje de sesiones de foco fallidas.</span><span class="sxs-lookup"><span data-stu-id="ac035-159">Percentage of Focus sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac035-160">Sesiones MCU</span><span class="sxs-lookup"><span data-stu-id="ac035-160">MCU sessions</span></span></p></td>
<td><p><span data-ttu-id="ac035-161">No</span><span class="sxs-lookup"><span data-stu-id="ac035-161">No</span></span></p></td>
<td><p><span data-ttu-id="ac035-162">Cantidad total de sesiones MCU.</span><span class="sxs-lookup"><span data-stu-id="ac035-162">Total number of MCU sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac035-163"><strong>Porcentaje de errores de MCU</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-163"><strong>MCU failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-164">No</span><span class="sxs-lookup"><span data-stu-id="ac035-164">No</span></span></p></td>
<td><p><span data-ttu-id="ac035-165">Porcentaje de sesiones MCU fallidas.</span><span class="sxs-lookup"><span data-stu-id="ac035-165">Percentage of MCU sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac035-166"><strong>Sesiones MCU por modalidad</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-166"><strong>MCU sessions by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-167">No</span><span class="sxs-lookup"><span data-stu-id="ac035-167">No</span></span></p></td>
<td><p><span data-ttu-id="ac035-168">Cantidad total de sesiones MCU, agrupadas por modalidad (por ejemplo, conferencia de mensajería instantánea).</span><span class="sxs-lookup"><span data-stu-id="ac035-168">Total number of MCU sessions, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac035-169"><strong>Porcentaje de errores por modalidad</strong></span><span class="sxs-lookup"><span data-stu-id="ac035-169"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="ac035-170">No</span><span class="sxs-lookup"><span data-stu-id="ac035-170">No</span></span></p></td>
<td><p><span data-ttu-id="ac035-171">Porcentaje de sesiones MCU fallidas, agrupadas por modalidad (por ejemplo, conferencia de mensajería instantánea).</span><span class="sxs-lookup"><span data-stu-id="ac035-171">Percentage of MCU sessions that failed, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ac035-172">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac035-172">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

