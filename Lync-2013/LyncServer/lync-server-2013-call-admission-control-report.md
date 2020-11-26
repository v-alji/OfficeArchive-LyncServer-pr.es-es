---
title: 'Lync Server 2013: informe de control de admisión de llamadas'
description: 'Lync Server 2013: informe de control de admisión de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Admission Control Report
ms:assetid: ea4b0c9f-7f93-4b8a-b901-01e1636c44fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615043(v=OCS.15)
ms:contentKeyID: 48185933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8764e51603e7097095894bc1230c2a2bb1126b9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435785"
---
# <a name="call-admission-control-report-in-lync-server-2013"></a><span data-ttu-id="f53b0-103">Informe de control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f53b0-103">Call Admission Control Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f53b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f53b0-104">

<span> </span></span></span>

<span data-ttu-id="f53b0-105">_**Última modificación del tema:** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="f53b0-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="f53b0-106">El Informe de control de admisión de llamadas ofrece información sobre las sesiones de punto a punto y de conferencia que se han llevado a cabo con restricciones definidas por el Control de admisión de llamadas.</span><span class="sxs-lookup"><span data-stu-id="f53b0-106">The Call Admission Control Report provides information about peer-to-peer and conferencing sessions that were conducted under restrictions set in place by Call Admission Control.</span></span> <span data-ttu-id="f53b0-107">El control de admisión de llamadas, presentado en Microsoft Lync Server 2010, proporciona a los administradores una manera de permitir (o no permitir) sesiones de comunicación basadas en restricciones de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="f53b0-107">Call Admission Control, introduced in Microsoft Lync Server 2010, provides a way for administrators to allow (or not allow) communication sessions based on bandwidth constraints.</span></span> <span data-ttu-id="f53b0-108">Por ejemplo, los administradores pueden crear directivas que impongan un límite a la cantidad de ancho de banda disponible para las llamadas de voz y vídeo.</span><span class="sxs-lookup"><span data-stu-id="f53b0-108">For example, administrators can create policies that impose a limit on the amount of bandwidth available for voice and video calls.</span></span> <span data-ttu-id="f53b0-109">Si se alcanza ese límite de ancho de banda, no se podrán realizar nuevas llamadas de voz o vídeo hasta que finalice alguna de las llamadas en curso y se liberen los recursos de red necesarios.</span><span class="sxs-lookup"><span data-stu-id="f53b0-109">If that bandwidth limit has been reached, then no new voice or video calls can be placed until one of the current calls has ended and freed up the required network resources.</span></span>

<div>

## <a name="accessing-the-call-admission-control-report"></a><span data-ttu-id="f53b0-110">Acceso al Informe de control de admisión de llamadas</span><span class="sxs-lookup"><span data-stu-id="f53b0-110">Accessing the Call Admission Control Report</span></span>

<span data-ttu-id="f53b0-p102">Al Informe de control de admisión de llamadas se obtiene acceso desde la página de inicio de Informes de supervisión. Desde el Informe de control de admisión de llamadas, puede obtener acceso a cualquiera de los informes siguientes:</span><span class="sxs-lookup"><span data-stu-id="f53b0-p102">The Call Admission Control Report is accessed from the Monitoring Reports home page. From the Call Admission Control Report you can drill down to either of the following reports:</span></span>

  - <span data-ttu-id="f53b0-113">Informe de detalles de conferencia: para obtener acceso a este informe, hada clic en la métrica Detalles desde una sesión de conferencia.</span><span class="sxs-lookup"><span data-stu-id="f53b0-113">Conference Detail Report – To access this report, click the Details metric from a conference session.</span></span>

  - <span data-ttu-id="f53b0-114">Informe de detalles de sesiones punto a punto: para obtener acceso a este informe, haga clic en la métrica Detalles desde una sesión punto a punto.</span><span class="sxs-lookup"><span data-stu-id="f53b0-114">Peer-to-Peer Session Detail Report – To access this report, click the Details metric for a peer-to-peer session.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-admission-control-report"></a><span data-ttu-id="f53b0-115">Cómo hacer el mejor uso del Informe de control de admisión de llamadas</span><span class="sxs-lookup"><span data-stu-id="f53b0-115">Making the Best Use of the Call Admission Control Report</span></span>

<span data-ttu-id="f53b0-p103">Para obtener una lista de las llamadas que no se han podido completar correctamente porque el ancho de banda no era suficiente, seleccione Llamadas rechazadas por el control de admisión de llamadas en la lista desplegable Categoría de llamada. La mayoría de las llamadas devueltas presentarán seguramente el identificador de diagnóstico 5:</span><span class="sxs-lookup"><span data-stu-id="f53b0-p103">To get a list of calls that failed because of insufficient bandwidth, select Calls rejected because of call admission control from the Call category dropdown list. Most of the returned calls will likely have a diagnostic ID of 5:</span></span>

<span data-ttu-id="f53b0-p104">Ancho de banda insuficiente para establecer la sesión. Intente volver a enrutar la llamada a través de RTC.</span><span class="sxs-lookup"><span data-stu-id="f53b0-p104">Insufficient bandwidth to establish session. Attempt PSTN re-route.</span></span>

<span data-ttu-id="f53b0-120">Este mensaje indica que las limitaciones del Control de admisión de llamadas impidió que la llamada se realizara en la red VoIP.</span><span class="sxs-lookup"><span data-stu-id="f53b0-120">That indicates that Call Admission Control limitations were preventing the call from being made on the VoIP network.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="f53b0-121">Filtros</span><span class="sxs-lookup"><span data-stu-id="f53b0-121">Filters</span></span>

<span data-ttu-id="f53b0-p105">Los filtros se emplean para recuperar un conjunto de datos más específico o para ver los datos devueltos de diferentes formas. Por ejemplo, el Informe de control de admisión de llamadas le permite filtrar llamadas por el usuario que inicia la llamada o por el usuario que recibe la llamada. También puede elegir cómo agrupar los datos. En este caso, las llamadas se agrupan por hora, día, semana o mes.</span><span class="sxs-lookup"><span data-stu-id="f53b0-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Admission Control Report enables you to filter calls by the user who initiated the call or by the user who was being called. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="f53b0-126">En la tabla siguiente se muestran los filtros que se pueden utilizar con el Informe de control de admisión de llamadas.</span><span class="sxs-lookup"><span data-stu-id="f53b0-126">The following table lists the filters that you can use with the Call Admission Control Report.</span></span>

### <a name="call-admission-control-report-filters"></a><span data-ttu-id="f53b0-127">Filtros del Informe de control de admisión de llamadas</span><span class="sxs-lookup"><span data-stu-id="f53b0-127">Call Admission Control Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f53b0-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="f53b0-128">Name</span></span></th>
<th><span data-ttu-id="f53b0-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="f53b0-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-130"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-130"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-p106">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f53b0-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="f53b0-133">7/17/12012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="f53b0-133">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="f53b0-p107">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="f53b0-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="f53b0-136">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="f53b0-136">7/17/12012</span></span></p>
<p><span data-ttu-id="f53b0-137">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="f53b0-137">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="f53b0-138">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="f53b0-138">7/13/2012</span></span></p>
<p><span data-ttu-id="f53b0-139">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="f53b0-139">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-140"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-140"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-p108">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f53b0-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="f53b0-143">7/17/12012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="f53b0-143">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="f53b0-p109">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="f53b0-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="f53b0-146">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="f53b0-146">7/17/12012</span></span></p>
<p><span data-ttu-id="f53b0-147">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="f53b0-147">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="f53b0-148">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="f53b0-148">7/13/2012</span></span></p>
<p><span data-ttu-id="f53b0-149">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="f53b0-149">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-150"><strong>Grupo de servidores</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-150"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-p110">Nombre de dominio completo (FQDN) del grupo de registradores o servidor perimetral. Puede seleccionar un grupo individual o hacer clic en <strong>[Todos]</strong> para ver los datos de todos los grupos. Esta lista desplegable se rellena automáticamente en función de los registros de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f53b0-p110">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-154"><strong>Tipo de actividad</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-154"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-p111">Tipo de actividad. Seleccione una de las siguientes actividades:</span><span class="sxs-lookup"><span data-stu-id="f53b0-p111">Type of activity. Select one of the following activities:</span></span></p>
<ul>
<li><p><span data-ttu-id="f53b0-157">[Todas]</span><span class="sxs-lookup"><span data-stu-id="f53b0-157">[All]</span></span></p></li>
<li><p><span data-ttu-id="f53b0-158">Punto a punto</span><span class="sxs-lookup"><span data-stu-id="f53b0-158">Peer-to-Peer</span></span></p></li>
<li><p><span data-ttu-id="f53b0-159">Una conferencia</span><span class="sxs-lookup"><span data-stu-id="f53b0-159">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-160"><strong>Categoría de llamada</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-160"><strong>Call category</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-p112">Indica el motivo por el que se usó el control de admisión de llamadas para la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="f53b0-p112">Indicates the reason that CAC was used for the call. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f53b0-163">[Todas]</span><span class="sxs-lookup"><span data-stu-id="f53b0-163">[All]</span></span></p></li>
<li><p><span data-ttu-id="f53b0-164">Llamada rechazada por el control de admisión de llamadas</span><span class="sxs-lookup"><span data-stu-id="f53b0-164">Call rejected because of call admission control</span></span></p></li>
<li><p><span data-ttu-id="f53b0-165">Llamadas que se han vuelto a enrutar a través de RTC por el control de admisión de llamadas</span><span class="sxs-lookup"><span data-stu-id="f53b0-165">Calls rerouted through PSTN because of call admission control</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="f53b0-166">Métricas de las sesiones punto a punto</span><span class="sxs-lookup"><span data-stu-id="f53b0-166">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="f53b0-167">En la siguiente tabla se muestra la información proporcionada por el Informe del control de admisión de llamadas para las sesiones punto a punto (es decir, sesiones entre solo dos participantes).</span><span class="sxs-lookup"><span data-stu-id="f53b0-167">The following table lists the information provided in the Call Admission Control Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="f53b0-168">Métricas de las sesiones punto a punto</span><span class="sxs-lookup"><span data-stu-id="f53b0-168">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f53b0-169">Nombre</span><span class="sxs-lookup"><span data-stu-id="f53b0-169">Name</span></span></th>
<th><span data-ttu-id="f53b0-170">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="f53b0-170">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f53b0-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="f53b0-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-172"><strong>Detalle</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-172"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-173">No</span><span class="sxs-lookup"><span data-stu-id="f53b0-173">No</span></span></p></td>
<td><p><span data-ttu-id="f53b0-174">Cuando se hace clic en este elemento, el informe muestra un informe detallado de sesión punto a punto de la sesión específica.</span><span class="sxs-lookup"><span data-stu-id="f53b0-174">When you click this item, the report shows you a Peer-to-Peer Session Detail Report for the specified session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-175"><strong>Remitente</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-175"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-176">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-177">Dirección SIP del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="f53b0-177">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-178"><strong>Destinatario</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-178"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-179">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-179">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-180">Dirección SIP del usuario al que se invitó a unirse a la sesión.</span><span class="sxs-lookup"><span data-stu-id="f53b0-180">SIP address of the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-181"><strong>Modalidades</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-181"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-182">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-182">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-183">Modalidades de comunicación (como audio y vídeo) que se usaron durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="f53b0-183">Communication modalities (such as audio and video) that were used during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-184"><strong>Hora de invitación</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-184"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-185">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-186">Fecha y hora en que se envió al remitente la invitación a la sesión inicial.</span><span class="sxs-lookup"><span data-stu-id="f53b0-186">Date and time the initial session invitation was sent to the From user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-187"><strong>Tiempo de respuesta</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-187"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-188">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-188">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-189">Fecha y hora en que se recibió la aceptación de la invitación.</span><span class="sxs-lookup"><span data-stu-id="f53b0-189">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-190"><strong>Hora de finalización</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-190"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-191">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-191">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-192">Fecha y hora en que finalizó la sesión.</span><span class="sxs-lookup"><span data-stu-id="f53b0-192">Date and time that the session ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-193"><strong>Id. de diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-193"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-194">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-p113">Identificador único (con formato de encabezado de ms-diagnostics) adjunto a un mensaje SIP que a menudo aporta información útil para solucionar errores. Los encabezados de diagnóstico son opcionales (es posible que haya sesiones SIP que no incluyan estos encabezados) y los identificadores de diagnóstico se notifican únicamente para las sesiones que tienen problemas de algún tipo.</span><span class="sxs-lookup"><span data-stu-id="f53b0-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="f53b0-197">Métricas de las sesiones de conferencia</span><span class="sxs-lookup"><span data-stu-id="f53b0-197">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="f53b0-198">En la siguiente tabla se muestra información proporcionada en el Informe de control de admisión de llamadas para las sesiones de conferencia (es decir, sesiones con tres o más participantes).</span><span class="sxs-lookup"><span data-stu-id="f53b0-198">The following table lists the information provided in the Call Admission Control Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="f53b0-199">Métricas de las sesiones de conferencia</span><span class="sxs-lookup"><span data-stu-id="f53b0-199">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f53b0-200">Nombre</span><span class="sxs-lookup"><span data-stu-id="f53b0-200">Name</span></span></th>
<th><span data-ttu-id="f53b0-201">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="f53b0-201">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f53b0-202">Descripción</span><span class="sxs-lookup"><span data-stu-id="f53b0-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-203"><strong>URI de conferencia</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-203"><strong>Conference URI</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-204">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-204">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-p114">Identificador único de la conferencia. Cuando se hace clic en este elemento, el informe muestra los participantes individuales de la conferencia.</span><span class="sxs-lookup"><span data-stu-id="f53b0-p114">Unique identifier for the conference. When you click this item, the report shows the individual conference participants.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-207"><strong>Organizador</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-207"><strong>Organizer</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-208">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-209">Dirección SIP del usuario que organizó la conferencia</span><span class="sxs-lookup"><span data-stu-id="f53b0-209">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-210"><strong>Grupo de servidores</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-210"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-211">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-211">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-212">Servidor perimetral usado en la conferencia.</span><span class="sxs-lookup"><span data-stu-id="f53b0-212">Edge Server used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-213"><strong>Hora de inicio</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-213"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-214">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-215">Fecha y hora en que comenzó la conferencia.</span><span class="sxs-lookup"><span data-stu-id="f53b0-215">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-216"><strong>Hora de finalización</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-216"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-217">Sí</span><span class="sxs-lookup"><span data-stu-id="f53b0-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="f53b0-218">Fecha y hora en que la conferencia finalizó.</span><span class="sxs-lookup"><span data-stu-id="f53b0-218">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="f53b0-219">Métricas de participantes en conferencias individuales</span><span class="sxs-lookup"><span data-stu-id="f53b0-219">Metrics for Individual Conference Participants</span></span>

<span data-ttu-id="f53b0-220">En la siguiente tabla se muestra la información proporcionada en el Informe de control de admisión de llamadas sobre participantes en conferencias individuales.</span><span class="sxs-lookup"><span data-stu-id="f53b0-220">The following table lists the information provided in the Call Admission Control Report for individual conference participants.</span></span>

### <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="f53b0-221">Métricas de participantes en conferencias individuales</span><span class="sxs-lookup"><span data-stu-id="f53b0-221">Metrics for Individual Conference Participants</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f53b0-222">Nombre</span><span class="sxs-lookup"><span data-stu-id="f53b0-222">Name</span></span></th>
<th><span data-ttu-id="f53b0-223">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="f53b0-223">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f53b0-224">Descripción</span><span class="sxs-lookup"><span data-stu-id="f53b0-224">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-225"><strong>Rol</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-225"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-226">No</span><span class="sxs-lookup"><span data-stu-id="f53b0-226">No</span></span></p></td>
<td><p><span data-ttu-id="f53b0-227">Rol (por ejemplo, Moderador) que ocupó el participante de la conferencia.</span><span class="sxs-lookup"><span data-stu-id="f53b0-227">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-228"><strong>Participante</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-228"><strong>Participant</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-229">No</span><span class="sxs-lookup"><span data-stu-id="f53b0-229">No</span></span></p></td>
<td><p><span data-ttu-id="f53b0-230">Dirección SIP del participante de la conferencia.</span><span class="sxs-lookup"><span data-stu-id="f53b0-230">SIP address of the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-231"><strong>Conectividad</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-231"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-232">No</span><span class="sxs-lookup"><span data-stu-id="f53b0-232">No</span></span></p></td>
<td><p><span data-ttu-id="f53b0-233">Conectividad de red (normalmente Desde conexión interna o Desde conexión externa) del participante.</span><span class="sxs-lookup"><span data-stu-id="f53b0-233">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-234"><strong>Modalidad</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-234"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-235">No</span><span class="sxs-lookup"><span data-stu-id="f53b0-235">No</span></span></p></td>
<td><p><span data-ttu-id="f53b0-236">Tipo de conferencia (por ejemplo, conferencia A/V).</span><span class="sxs-lookup"><span data-stu-id="f53b0-236">Conference type (for example, A/V conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-237"><strong>Hora de conexión</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-237"><strong>Join time</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-238">No</span><span class="sxs-lookup"><span data-stu-id="f53b0-238">No</span></span></p></td>
<td><p><span data-ttu-id="f53b0-239">Fecha y hora en que el participante se unió a la conferencia.</span><span class="sxs-lookup"><span data-stu-id="f53b0-239">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53b0-240"><strong>Hora de desconexión</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-240"><strong>Leave time</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-241">No</span><span class="sxs-lookup"><span data-stu-id="f53b0-241">No</span></span></p></td>
<td><p><span data-ttu-id="f53b0-242">Fecha y hora en que el participante abandonó la conferencia.</span><span class="sxs-lookup"><span data-stu-id="f53b0-242">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f53b0-243"><strong>Id. de diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="f53b0-243"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="f53b0-244">No</span><span class="sxs-lookup"><span data-stu-id="f53b0-244">No</span></span></p></td>
<td><p><span data-ttu-id="f53b0-p115">Identificador único (con formato de encabezado de ms-diagnostics) adjunto a un mensaje SIP que a menudo aporta información útil para solucionar errores. Los encabezados de diagnóstico son opcionales (es posible que haya sesiones SIP que no incluyan estos encabezados) y los identificadores de diagnóstico se notifican únicamente para las sesiones que tienen problemas de algún tipo.</span><span class="sxs-lookup"><span data-stu-id="f53b0-p115">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f53b0-247">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f53b0-247">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

