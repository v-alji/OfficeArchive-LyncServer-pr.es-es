---
title: 'Lync Server 2013: informe de errores principales'
description: 'Lync Server 2013: informe de errores principales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Top Failures Report
ms:assetid: 438942e2-580a-4b67-9d42-f116111fb26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558640(v=OCS.15)
ms:contentKeyID: 48184021
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 768c9a99916dece9eb76877b0cd65b057697ff95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440916"
---
# <a name="top-failures-report-in-lync-server-2013"></a><span data-ttu-id="b24eb-103">Informe de errores principales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b24eb-103">Top Failures Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b24eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b24eb-104">

<span> </span></span></span>

<span data-ttu-id="b24eb-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="b24eb-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="b24eb-p101">El Informe de errores principales proporciona una presentación de los errores más frecuentes y las tendencias en el tiempo. Los errores se basan en una combinación de las dos métricas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p101">The Top Failures Report provides a look at the most-commonly reported failures and their trends over time. Failures are based on a combination of the following two metrics:</span></span>

  - <span data-ttu-id="b24eb-p102">**Id. de diagnóstico**. Identificador único (en forma de un encabezado de ms-diagnostics) que se adjunta a un mensaje SIP. Los Id. de diagnóstico proporcionan información útil para la solución de problemas relacionados con la llamada.</span><span class="sxs-lookup"><span data-stu-id="b24eb-p102">**Diagnostic ID**. Unique identifier (in the form of an ms-diagnostics header) that is attached to a SIP message. Diagnostic IDs provide information useful in troubleshooting call-related problems.</span></span>

  - <span data-ttu-id="b24eb-111">**Código de respuesta**.</span><span class="sxs-lookup"><span data-stu-id="b24eb-111">**Response code**.</span></span> <span data-ttu-id="b24eb-112">Los códigos de respuesta se usan en las sesiones de comunicación SIP para responder a solicitudes SIP.</span><span class="sxs-lookup"><span data-stu-id="b24eb-112">Response codes are used in SIP communication sessions to respond to SIP requests.</span></span> <span data-ttu-id="b24eb-113">Por ejemplo, supongamos que Ken envía la solicitud INVITE a Pilar Ackerman (es decir, supongamos que Ken Myer llama Pilar Ackerman).</span><span class="sxs-lookup"><span data-stu-id="b24eb-113">For example, suppose Ken sends the INVITE request to Pilar Ackerman (that is, suppose Ken Myer calls Pilar Ackerman).</span></span> <span data-ttu-id="b24eb-114">Si Pilar responde, su teléfono le enviará el código de respuesta 200 (OK), indicando al teléfono de Ken que Pilar ha respondido.</span><span class="sxs-lookup"><span data-stu-id="b24eb-114">If Pilar answers, her phone will send the response code 200 (OK), letting Ken's phone know that Pilar has answered.</span></span> <span data-ttu-id="b24eb-115">El informe de errores principales solo incluye códigos de respuesta que se enviaron en respuesta a un error de llamada. Lync Server no realiza un seguimiento de todos los códigos de respuesta emitidos durante el transcurso de una llamada.</span><span class="sxs-lookup"><span data-stu-id="b24eb-115">The Top Failures Report only includes response codes that were sent in response to a call failure; Lync Server does not keep track of all the response codes issued during the course of a call.</span></span>

<span data-ttu-id="b24eb-116">No solo se proporciona información de la cantidad total de sesiones donde se produjo un error, sino también de la cantidad total de usuarios a los que afectó el error.</span><span class="sxs-lookup"><span data-stu-id="b24eb-116">Information is reported not only for the total number of sessions where a failure occurred but also for the total number of users who were impacted by the failure.</span></span>

<div>

## <a name="accessing-the-top-failures-report"></a><span data-ttu-id="b24eb-117">Acceso al Informe de errores principales</span><span class="sxs-lookup"><span data-stu-id="b24eb-117">Accessing the Top Failures Report</span></span>

<span data-ttu-id="b24eb-118">Desde la página Informes supervisión se obtiene acceso al Informe de errores principales.</span><span class="sxs-lookup"><span data-stu-id="b24eb-118">The Top Failures Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="b24eb-119">Al hacer clic en la métrica de sesiones notificadas, se abrirá el [Informe de distribución de errores en Lync Server 2013](lync-server-2013-failure-distribution-report.md).</span><span class="sxs-lookup"><span data-stu-id="b24eb-119">Clicking the Reported sessions metric will take you to the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md).</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-top-failures-report"></a><span data-ttu-id="b24eb-120">Hacer el mejor uso del Informe de errores principales</span><span class="sxs-lookup"><span data-stu-id="b24eb-120">Making the Best Use of the Top Failures Report</span></span>

<span data-ttu-id="b24eb-p105">El Informe de errores principales es inusual en un sentido: le permite filtrar a la vez hasta 5 Id. de diagnóstico. (Normalmente solo se filtra por un elemento cada vez, como una dirección SIP de usuario). Para filtrar por varios Id. de diagnóstico, simplemente introduzca cada Id. en el cuadro Id. de diagnóstico, separe los identificadores con comas. (Si desea, puede dejar un espacio en blanco después de cada coma). Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p105">The Top Failures Report is unusual in one regard: it allows you to filter on as many as 5 diagnostic IDs at once. (Typically you can only filter on one item – such as one user SIP address – at a time.) To filter on multiple diagnostic IDs, simply enter each ID in the Diagnostic IDs box, separating the IDs by using commas. (If you want to, you can leave a blank space after each comma.) For example:</span></span>

<span data-ttu-id="b24eb-124">1011, 2412, 1033, 52116, 1008</span><span class="sxs-lookup"><span data-stu-id="b24eb-124">1011, 2412, 1033, 52116, 1008</span></span>

<span data-ttu-id="b24eb-125">Haga eso y solo aparecerán las llamadas erróneas que notificaron al menos uno de esos cinco Id. de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="b24eb-125">Do that, and only failed calls that reported at least one of those five diagnostic IDs will be displayed.</span></span>

<span data-ttu-id="b24eb-p106">Si coloca el mouse sobre un código de respuesta verá una información sobre herramientas que le indica el significado del código de respuesta en cuestión. Por ejemplo, si coloca el mouse sobre el código de respuesta 486 verá este mensaje:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p106">If you hold your mouse over a Response code you'll see a tooltip that tells you what the Response code in question means. For example, if you hold the mouse over the Response code 486 you'll see this message:</span></span>

<span data-ttu-id="b24eb-128">No disponible aquí.</span><span class="sxs-lookup"><span data-stu-id="b24eb-128">Busy Here.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="b24eb-129">Filtros</span><span class="sxs-lookup"><span data-stu-id="b24eb-129">Filters</span></span>

<span data-ttu-id="b24eb-p107">Los filtros se emplean para recuperar un conjunto de datos más específico o para ver los datos devueltos de diferentes formas. Por ejemplo, el informe de errores más comunes le permite filtrar los datos en función de aspectos tales como el tipo de actividad (sesión punto a punto o sesión de conferencia) o por el código de respuesta SIP que acompañó a la sesión fallida. Es posible también elegir la forma en la que los datos necesitan agruparse. En este caso, los usos se agrupan por hora, día, semana o mes.</span><span class="sxs-lookup"><span data-stu-id="b24eb-p107">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Top Failures Report enables you to filter the returned data based on such things as the activity type (peer-to-peer session or conferencing session) or by the SIP response code that accompanied the failed session. You can also choose how data should be grouped. In this case, usages are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="b24eb-134">La siguiente tabla muestra los filtros que puede utilizar con el informe de errores más comunes.</span><span class="sxs-lookup"><span data-stu-id="b24eb-134">The following table lists the filters that you can use with the Top Failures Report.</span></span>

### <a name="top-failures-report-filters"></a><span data-ttu-id="b24eb-135">Filtros del informe de errores más comunes</span><span class="sxs-lookup"><span data-stu-id="b24eb-135">Top Failures Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b24eb-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="b24eb-136">Name</span></span></th>
<th><span data-ttu-id="b24eb-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="b24eb-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b24eb-138"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-138"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-p108">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p108">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="b24eb-141">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="b24eb-141">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="b24eb-p109">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p109">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="b24eb-144">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="b24eb-144">7/7/2012</span></span></p>
<p><span data-ttu-id="b24eb-145">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="b24eb-145">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="b24eb-146">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="b24eb-146">7/3/2012</span></span></p>
<p><span data-ttu-id="b24eb-147">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="b24eb-147">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24eb-148"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-148"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-p110">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p110">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="b24eb-151">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="b24eb-151">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="b24eb-p111">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p111">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="b24eb-154">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="b24eb-154">7/7/2012</span></span></p>
<p><span data-ttu-id="b24eb-155">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="b24eb-155">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="b24eb-156">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="b24eb-156">7/3/2012</span></span></p>
<p><span data-ttu-id="b24eb-157">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="b24eb-157">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24eb-158"><strong>Tipo de actividad</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-158"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-p112">Tipo de actividad. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p112">Type of activity. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="b24eb-161">[Todas]</span><span class="sxs-lookup"><span data-stu-id="b24eb-161">[All]</span></span></p></li>
<li><p><span data-ttu-id="b24eb-162">Punto a punto</span><span class="sxs-lookup"><span data-stu-id="b24eb-162">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="b24eb-163">Una conferencia</span><span class="sxs-lookup"><span data-stu-id="b24eb-163">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24eb-164"><strong>Modalidad</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-164"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-165">En este momento, la única opción disponible es <strong>[Todos]</strong>.</span><span class="sxs-lookup"><span data-stu-id="b24eb-165">At this time the only option available is <strong>[All]</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24eb-166"><strong>Grupo de servidores</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-166"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-p113">Nombre de dominio completo (FQDN) del grupo de registradores o servidor perimetral. Puede seleccionar un grupo individual o hacer clic en <strong>[Todos]</strong> para ver los datos de todos los grupos. Esta lista desplegable se rellena automáticamente en función de los registros de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b24eb-p113">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24eb-170"><strong>Categoría</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-170"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-p114">Tipo de error. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p114">Type of failure experienced. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="b24eb-173">Error esperado e inesperado</span><span class="sxs-lookup"><span data-stu-id="b24eb-173">Both expected and unexpected failure</span></span></p></li>
<li><p><span data-ttu-id="b24eb-174">Error inesperado</span><span class="sxs-lookup"><span data-stu-id="b24eb-174">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="b24eb-175">Un &quot; error esperado &quot; es un error que se espera que suceda.</span><span class="sxs-lookup"><span data-stu-id="b24eb-175">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="b24eb-176">Por ejemplo, si un usuario ha establecido su estado en No molestar, se espera que las llamadas a ese usuario no se realicen.</span><span class="sxs-lookup"><span data-stu-id="b24eb-176">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="b24eb-177">Un &quot; error inesperado &quot; es un error que se produce en lo que parecería ser un sistema saludable en otro caso.</span><span class="sxs-lookup"><span data-stu-id="b24eb-177">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="b24eb-178">Por ejemplo, una llamada no tendría que finalizarse si el autor de la llamada está en espera.</span><span class="sxs-lookup"><span data-stu-id="b24eb-178">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="b24eb-179">De ser así, tal cosa se identificaría como un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b24eb-179">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24eb-180"><strong>Código de respuesta</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-180"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-p116">Código de respuesta SIP enviado cuando la conferencia ha fallado. Escriba el código de respuesta en su totalidad, como por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b24eb-p116">SIP response code sent when the conference failed. Enter the entire response code For example:</span></span></p>
<p><span data-ttu-id="b24eb-183">400</span><span class="sxs-lookup"><span data-stu-id="b24eb-183">400</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24eb-184"><strong>Id. de diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-184"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-p117">Identificador único (con formato de encabezado de ms-diagnostics) adjunto a un mensaje SIP que a menudo aporta información útil para solucionar errores. Los encabezados de diagnóstico son opcionales (es posible que haya sesiones SIP que no incluyan estos encabezados) y los identificadores de diagnóstico se notifican únicamente para las sesiones que tienen problemas de algún tipo.</span><span class="sxs-lookup"><span data-stu-id="b24eb-p117">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="b24eb-187">Métricas</span><span class="sxs-lookup"><span data-stu-id="b24eb-187">Metrics</span></span>

<span data-ttu-id="b24eb-188">En la tabla siguiente se muestra la información que recoge el informe de errores más comunes.</span><span class="sxs-lookup"><span data-stu-id="b24eb-188">The following table lists the information provided in the Top Failures Report.</span></span>

### <a name="top-failures-report-metrics"></a><span data-ttu-id="b24eb-189">Métricas del informe de errores más comunes</span><span class="sxs-lookup"><span data-stu-id="b24eb-189">Top Failures Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b24eb-190">Nombre</span><span class="sxs-lookup"><span data-stu-id="b24eb-190">Name</span></span></th>
<th><span data-ttu-id="b24eb-191">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="b24eb-191">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="b24eb-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="b24eb-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b24eb-193"><strong>Clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-193"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-194">Sí</span><span class="sxs-lookup"><span data-stu-id="b24eb-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="b24eb-195">Clasificación relativa basada en la cantidad de sesiones de las que se informa.</span><span class="sxs-lookup"><span data-stu-id="b24eb-195">Relative rank based on the number of reported sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24eb-196"><strong>Sesiones notificadas</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-196"><strong>Reported sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-197">Sí</span><span class="sxs-lookup"><span data-stu-id="b24eb-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="b24eb-198">Cantidad total de sesiones con error basadas en el Id. de diagnóstico y en el código de respuesta SIP.</span><span class="sxs-lookup"><span data-stu-id="b24eb-198">Total number of failed sessions based on diagnostic ID and SIP response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24eb-199"><strong>Usuarios afectados</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-199"><strong>Users impacted</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-200">Sí</span><span class="sxs-lookup"><span data-stu-id="b24eb-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="b24eb-201">Cantidad total de usuarios afectados por la sesión con error.</span><span class="sxs-lookup"><span data-stu-id="b24eb-201">Total number of users affected by the failed session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b24eb-202"><strong>Información del error</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-202"><strong>Failure information</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-203">No</span><span class="sxs-lookup"><span data-stu-id="b24eb-203">No</span></span></p></td>
<td><p><span data-ttu-id="b24eb-204">Información detallada sobre el error, incluido el Id. de diagnóstico, el código de respuesta SIP y la descripción de los motivos por los que se produjo un error en la sesión.</span><span class="sxs-lookup"><span data-stu-id="b24eb-204">Detailed information about the failure, including diagnostic ID, SIP response code, and description of why the session failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b24eb-205"><strong>Tendencia en el pasado</strong></span><span class="sxs-lookup"><span data-stu-id="b24eb-205"><strong>Trend in the past</strong></span></span></p></td>
<td><p><span data-ttu-id="b24eb-206">No</span><span class="sxs-lookup"><span data-stu-id="b24eb-206">No</span></span></p></td>
<td><p><span data-ttu-id="b24eb-207">Gráfico de sesiones con error a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="b24eb-207">Graphs failed sessions over time.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b24eb-208">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b24eb-208">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

