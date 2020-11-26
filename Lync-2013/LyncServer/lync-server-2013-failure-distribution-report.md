---
title: 'Lync Server 2013: informe de distribución de errores'
description: 'Lync Server 2013: informe de distribución de errores.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure Distribution Report
ms:assetid: 365c7beb-24d4-40f5-92e7-4978b9688916
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558635(v=OCS.15)
ms:contentKeyID: 48183849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5a87f779f87d6b7002fa108f1969c33739eed9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428219"
---
# <a name="failure-distribution-report-in-lync-server-2013"></a><span data-ttu-id="24e39-103">Informe de distribución de errores en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24e39-103">Failure Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24e39-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24e39-104">

<span> </span></span></span>

<span data-ttu-id="24e39-105">_**Última modificación del tema:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="24e39-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="24e39-106">El Informe de distribución de errores clasifica las sesiones con error en las categorías siguientes:</span><span class="sxs-lookup"><span data-stu-id="24e39-106">The Failure Distribution Report ranks failed sessions in the following categories:</span></span>

  - <span data-ttu-id="24e39-107">Principales motivos de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="24e39-107">Top diagnostic reasons</span></span>

  - <span data-ttu-id="24e39-108">Principales modalidades</span><span class="sxs-lookup"><span data-stu-id="24e39-108">Top modalities</span></span>

  - <span data-ttu-id="24e39-109">Principales grupos de servidores</span><span class="sxs-lookup"><span data-stu-id="24e39-109">Top pools</span></span>

  - <span data-ttu-id="24e39-110">Principales fuentes</span><span class="sxs-lookup"><span data-stu-id="24e39-110">Top sources</span></span>

  - <span data-ttu-id="24e39-111">Principales componentes</span><span class="sxs-lookup"><span data-stu-id="24e39-111">Top components</span></span>

  - <span data-ttu-id="24e39-112">Principales remitentes</span><span class="sxs-lookup"><span data-stu-id="24e39-112">Top from users</span></span>

  - <span data-ttu-id="24e39-113">Principales destinatarios</span><span class="sxs-lookup"><span data-stu-id="24e39-113">Top to users</span></span>

  - <span data-ttu-id="24e39-114">Agentes de usuarios de origen principales</span><span class="sxs-lookup"><span data-stu-id="24e39-114">Top from user agents</span></span>

<span data-ttu-id="24e39-p101">Puede usar estas categorías para determinar dónde se está produciendo exactamente el problema y, en determinados casos, por qué se está produciendo el problema. Por ejemplo, supongamos que ha registrado 242 sesiones de audio/vídeo con error en un día determinado. El Informe de distribución de errores puede mostrar que 237 de dichas sesiones con error tuvieron lugar en el grupo de Dublín. Esto supone un buen punto de partida para el seguimiento y el diagnóstico de las causas de dichos errores. Si hace clic en el grupo de Dublín en la categoría **Grupos principales**, verá un Informe de distribución de errores solo para dicho grupo. Desde ahí, podrá comenzar a analizar las razones por las que el grupo de Dublín tenía tantos problemas.</span><span class="sxs-lookup"><span data-stu-id="24e39-p101">You can use these categories to determine exactly where a problem is occurring and, in some cases, why the problem is occurring. For example, suppose you recorded 242 failed audio/video sessions during a given day. If you look at the Failure Distribution Report, it might show that 237 of those failed sessions took place in your Dublin pool. That gives you a good place to start when it comes to tracking down and diagnosing the causes behind those failures. If you click on the Dublin pool under the **Top pools** category, you will see a Failure Distribution Report just for that pool. You can then begin analyzing why the Dublin pool was experiencing so many difficulties.</span></span>

<div>

## <a name="viewing-the-failure-distribution-report"></a><span data-ttu-id="24e39-121">Visualización del Informe de distribución de errores</span><span class="sxs-lookup"><span data-stu-id="24e39-121">Viewing the Failure Distribution Report</span></span>

<span data-ttu-id="24e39-122">Puede tener acceso al Informe de distribución de errores desde cualquiera de los informes siguientes haciendo clic en la métrica **Volumen de errores esperados** o **Volumen de errores inesperados**:</span><span class="sxs-lookup"><span data-stu-id="24e39-122">You can access the Failure Distribution Report from any of the following reports by clicking either the **Expected failure volume** or the **Unexpected failure volume** metric:</span></span>

  - [<span data-ttu-id="24e39-123">Informe de errores principales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24e39-123">Top Failures Report in Lync Server 2013</span></span>](lync-server-2013-top-failures-report.md)

  - [<span data-ttu-id="24e39-124">Informe de diagnóstico de conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24e39-124">Conference Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-conference-diagnostic-report.md)

  - [<span data-ttu-id="24e39-125">Informe de diagnóstico de actividad de punto a punto en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24e39-125">Peer-to-Peer Activity Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)

<span data-ttu-id="24e39-126">En el informe de distribución de errores, puede hacer clic en cualquiera de las siguientes métricas para ver el [Informe de la lista de errores en Lync Server 2013](lync-server-2013-failure-list-report.md):</span><span class="sxs-lookup"><span data-stu-id="24e39-126">From the Failure Distribution Report, you can click any of the following metrics to view the [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md):</span></span>

  - <span data-ttu-id="24e39-127">Principales motivos del diagnóstico (sesiones)</span><span class="sxs-lookup"><span data-stu-id="24e39-127">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="24e39-128">Principales modalidades (sesiones)</span><span class="sxs-lookup"><span data-stu-id="24e39-128">Top modalities (sessions)</span></span>

  - <span data-ttu-id="24e39-129">Principales grupos de servidores (sesiones)</span><span class="sxs-lookup"><span data-stu-id="24e39-129">Top pools (sessions)</span></span>

  - <span data-ttu-id="24e39-130">Principales orígenes (sesiones)</span><span class="sxs-lookup"><span data-stu-id="24e39-130">Top sources (sessions)</span></span>

  - <span data-ttu-id="24e39-131">Principales componentes (sesiones)</span><span class="sxs-lookup"><span data-stu-id="24e39-131">Top components (sessions)</span></span>

  - <span data-ttu-id="24e39-132">Principales remitentes (sesiones)</span><span class="sxs-lookup"><span data-stu-id="24e39-132">Top from users (sessions)</span></span>

  - <span data-ttu-id="24e39-133">Principales destinatarios (sesiones)</span><span class="sxs-lookup"><span data-stu-id="24e39-133">Top to users (sessions)</span></span>

  - <span data-ttu-id="24e39-134">Principales agentes de remitente (sesiones)</span><span class="sxs-lookup"><span data-stu-id="24e39-134">Top from user agents (sessions)</span></span>

</div>

<div>

## <a name="using-the-failure-distribution-report"></a><span data-ttu-id="24e39-135">Uso del Informe de distribución de errores</span><span class="sxs-lookup"><span data-stu-id="24e39-135">Using the Failure Distribution Report</span></span>

<span data-ttu-id="24e39-p102">Dependiendo del tamaño de su monitor y de la resolución de la pantalla, es posible que algunos de los datos del Informe de distribución de errores aparezcan truncados. Esto se produce, sobre todo, en métricas como, por ejemplo, las de los agentes de usuarios que tienen etiquetas muy largas. Por ejemplo, es posible que un agente de usuario con el nombre "UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)" solo se muestre de forma parcial en la pantalla:</span><span class="sxs-lookup"><span data-stu-id="24e39-p102">Depending on your monitor size and screen resolution, it's possible that some of the data shown in the Failure Distribution Report might be truncated when you view it onscreen. This is especially true for metrics such as user agents, which can have very long labels. For example, a user agent with a name like "UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)" might only partially appear onscreen:</span></span>

<span data-ttu-id="24e39-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span><span class="sxs-lookup"><span data-stu-id="24e39-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span></span>

<span data-ttu-id="24e39-140">Afortunadamente, basta con mantener el mouse sobre el valor truncado para ver la etiqueta completa.</span><span class="sxs-lookup"><span data-stu-id="24e39-140">Fortunately, you can see the entire label simply by holding your mouse over the truncated value.</span></span>

<span data-ttu-id="24e39-p103">Una métrica interesante que puede filtrar con el Informe de distribución de errores es la del Id. de diagnóstico. Si se muestra el mismo Id. de diagnóstico en otros informes, podrá filtrar dicho Id. de diagnóstico en el Informe de distribución de errores y obtener una vista detallada del lugar exacto y la frecuencia con la que se ha informado de dicho Id. en la sesión con errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-p103">One interesting metric that you can filter on by using the Failure Distribution Report is Diagnostic ID. If you see the same Diagnostic ID cropping up in other reports you can filter on that ID in the Failure Distribution Report and get a very detailed look at exactly where, and how often, that ID has been reported during a failed session.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="24e39-143">Filtros</span><span class="sxs-lookup"><span data-stu-id="24e39-143">Filters</span></span>

<span data-ttu-id="24e39-p104">Los filtros se emplean para recuperar un conjunto de datos más específico o para ver los datos devueltos de diferentes formas. Por ejemplo, el informe de distribución de errores le permite filtrar por tipo de actividad (sesión de punto a punto o sesión de conferencias) o por el Id. de diagnóstico que contenía cada sesión con errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Failed Distribution Report enables you to filter on such things as the activity type (peer-to-peer session or conferencing session) or by the diagnostic ID that accompanied each failed session.</span></span>

<span data-ttu-id="24e39-146">La siguiente tabla muestra los filtros que puede utilizar con el informe de resumen de conferencia.</span><span class="sxs-lookup"><span data-stu-id="24e39-146">The following table lists the filters that you can use with the Failure Distribution Report.</span></span>

### <a name="failure-distribution-report-filters"></a><span data-ttu-id="24e39-147">Filtros de informes de distribución de errores</span><span class="sxs-lookup"><span data-stu-id="24e39-147">Failure Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e39-148">Nombre</span><span class="sxs-lookup"><span data-stu-id="24e39-148">Name</span></span></th>
<th><span data-ttu-id="24e39-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e39-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e39-150"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-p105">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="24e39-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="24e39-153">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="24e39-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="24e39-p106">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="24e39-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="24e39-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="24e39-156">7/7/2012</span></span></p>
<p><span data-ttu-id="24e39-157">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="24e39-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="24e39-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="24e39-158">7/3/2012</span></span></p>
<p><span data-ttu-id="24e39-159">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="24e39-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-160"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-p107">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="24e39-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="24e39-163">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="24e39-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="24e39-p108">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="24e39-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="24e39-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="24e39-166">7/7/2012</span></span></p>
<p><span data-ttu-id="24e39-167">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="24e39-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="24e39-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="24e39-168">7/3/2012</span></span></p>
<p><span data-ttu-id="24e39-169">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="24e39-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-170"><strong>Grupo de servidores</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-170"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-p109">Nombre de dominio completo (FQDN) del grupo de registradores o servidor perimetral. Puede seleccionar un grupo individual o hacer clic en <strong>[Todos]</strong> para ver los datos de todos los grupos. Esta lista desplegable se rellena automáticamente en función de los registros de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="24e39-p109">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-174"><strong>Tipo de actividad</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-174"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-p110">Tipo de actividad para filtrar. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="24e39-p110">Type of activity to filter on. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="24e39-177">[Todas]</span><span class="sxs-lookup"><span data-stu-id="24e39-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="24e39-178">Punto a punto</span><span class="sxs-lookup"><span data-stu-id="24e39-178">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="24e39-179">Una conferencia</span><span class="sxs-lookup"><span data-stu-id="24e39-179">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-180"><strong>Categoría de sesión</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-180"><strong>Session category</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-p111">Indica si la actividad correspondiente se desarrolló correctamente o causó errores. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="24e39-p111">Indicates whether the activity in question succeeded or failed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="24e39-183">[Todas]</span><span class="sxs-lookup"><span data-stu-id="24e39-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="24e39-184">Correcto</span><span class="sxs-lookup"><span data-stu-id="24e39-184">Success</span></span></p></li>
<li><p><span data-ttu-id="24e39-185">Error esperado</span><span class="sxs-lookup"><span data-stu-id="24e39-185">Expected failure</span></span></p></li>
<li><p><span data-ttu-id="24e39-186">Error inesperado</span><span class="sxs-lookup"><span data-stu-id="24e39-186">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="24e39-187">Un &quot; error esperado &quot; es un error que se espera que suceda.</span><span class="sxs-lookup"><span data-stu-id="24e39-187">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="24e39-188">Por ejemplo, si un usuario ha establecido su estado en No molestar, se espera que las llamadas a ese usuario no se realicen.</span><span class="sxs-lookup"><span data-stu-id="24e39-188">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="24e39-189">Un &quot; error inesperado &quot; es un error que se produce en lo que parecería ser un sistema saludable en otro caso.</span><span class="sxs-lookup"><span data-stu-id="24e39-189">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="24e39-190">Por ejemplo, una llamada no tendría que finalizarse si el autor de la llamada está en espera.</span><span class="sxs-lookup"><span data-stu-id="24e39-190">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="24e39-191">De ser así, tal cosa se identificaría como un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="24e39-191">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-192"><strong>Id. de diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-192"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-p113">Identificador único (con formato de encabezado de ms-diagnostics) adjunto a un mensaje SIP que a menudo aporta información útil para solucionar errores. Los encabezados de diagnóstico son opcionales (es posible que haya sesiones SIP que no incluyan estos encabezados) y los identificadores de diagnóstico se notifican únicamente para las sesiones que tienen problemas de algún tipo.</span><span class="sxs-lookup"><span data-stu-id="24e39-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="24e39-195">Métricas para motivos del diagnóstico destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-195">Metrics for Top Diagnostic Reasons</span></span>

<span data-ttu-id="24e39-196">La siguiente tabla enumera la información proporcionada en el informe de distribución de errores basándose en el Id. de diagnóstico que aparece con mayor frecuencia.</span><span class="sxs-lookup"><span data-stu-id="24e39-196">The following table lists the information provided in the Failure Distribution Report based on the most frequently reported diagnostic ID.</span></span>

### <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="24e39-197">Métricas para motivos del diagnóstico destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-197">Metrics for Top Diagnostic Reasons</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e39-198">Nombre</span><span class="sxs-lookup"><span data-stu-id="24e39-198">Name</span></span></th>
<th><span data-ttu-id="24e39-199">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="24e39-199">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="24e39-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e39-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e39-201"><strong>Clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-201"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-202">No</span><span class="sxs-lookup"><span data-stu-id="24e39-202">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-p114">Clasificación relativa de sesiones con errores basándose en los Id. de diagnóstico. El Id. de diagnóstico es un identificador único (con el formato de un encabezado de diagnóstico MS) adjunto a un mensaje SIP que suele proporcionar información útil para resolver errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-p114">Relative ranking of failed sessions based on diagnostic IDs. The diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-205"><strong>Principales motivos de diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-205"><strong>Top diagnostic reasons</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-206">No</span><span class="sxs-lookup"><span data-stu-id="24e39-206">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-207">Id. de diagnóstico generado en una sesión.</span><span class="sxs-lookup"><span data-stu-id="24e39-207">Diagnostic ID generated in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-208"><strong>Sesiones</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-208"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-209">No</span><span class="sxs-lookup"><span data-stu-id="24e39-209">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-210">Cantidad total de sesiones con errores en las que generó el Id. de diagnóstico especificado.</span><span class="sxs-lookup"><span data-stu-id="24e39-210">Total number of failed sessions where the specified diagnostic ID was generated.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-modalities"></a><span data-ttu-id="24e39-211">Métricas para modalidades destacadas</span><span class="sxs-lookup"><span data-stu-id="24e39-211">Metrics for Top Modalities</span></span>

<span data-ttu-id="24e39-212">La siguiente tabla enumera la información proporcionada en el informe de distribución de errores basándose en las modalidades de sesiones que experimentaron más errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-212">The following table lists the information provided in the Failure Distribution Report based on the session modalities that experienced the most failures.</span></span>

### <a name="metrics-for-top-modalities"></a><span data-ttu-id="24e39-213">Métricas para modalidades destacadas</span><span class="sxs-lookup"><span data-stu-id="24e39-213">Metrics for Top Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e39-214">Nombre</span><span class="sxs-lookup"><span data-stu-id="24e39-214">Name</span></span></th>
<th><span data-ttu-id="24e39-215">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="24e39-215">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="24e39-216">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e39-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e39-217"><strong>Clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-217"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-218">No</span><span class="sxs-lookup"><span data-stu-id="24e39-218">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-219">Clasificación relativa de sesiones con errores basándose en los tipos de sesiones (por ejemplo, una conferencia de audio o vídeo o una sesión de transferencia de archivos de punto a punto).</span><span class="sxs-lookup"><span data-stu-id="24e39-219">Relative ranking based of failed session based on session type (for example, an audio/video conference or a peer-to-peer file transfer session).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-220"><strong>Principales modalidades</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-220"><strong>Top modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-221">No</span><span class="sxs-lookup"><span data-stu-id="24e39-221">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-222">Tipo de sesión.</span><span class="sxs-lookup"><span data-stu-id="24e39-222">Session type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-223"><strong>Sesiones</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-223"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-224">No</span><span class="sxs-lookup"><span data-stu-id="24e39-224">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-225">Cantidad total de sesiones con errores en las que aparece la modalidad especificada.</span><span class="sxs-lookup"><span data-stu-id="24e39-225">Total number of failed sessions involving the specified modality.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-pools"></a><span data-ttu-id="24e39-226">Métricas para grupos destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-226">Metrics for Top Pools</span></span>

<span data-ttu-id="24e39-227">La siguiente tabla enumera la información proporcionada en el informe de distribución de errores basándose en los grupos de servidores que experimentaron más errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-227">The following table lists the information provided in the Failure Distribution Report based on the pools that experienced the most failures.</span></span>

### <a name="metrics-for-top-pools"></a><span data-ttu-id="24e39-228">Métricas para grupos destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-228">Metrics for Top Pools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e39-229">Nombre</span><span class="sxs-lookup"><span data-stu-id="24e39-229">Name</span></span></th>
<th><span data-ttu-id="24e39-230">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="24e39-230">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="24e39-231">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e39-231">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e39-232"><strong>Clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-232"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-233">No</span><span class="sxs-lookup"><span data-stu-id="24e39-233">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-234">Clasificación relativa de las sesiones erróneas basadas en el grupo de registradores o el servidor perimetral donde se realizó la sesión.</span><span class="sxs-lookup"><span data-stu-id="24e39-234">Relative ranking of failed sessions based on the Registrar pool or Edge Server where the session was conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-235"><strong>Principales grupos de servidores</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-235"><strong>Top pools</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-236">No</span><span class="sxs-lookup"><span data-stu-id="24e39-236">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-237">Nombre del grupo de registradores o del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="24e39-237">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-238"><strong>Sesiones</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-238"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-239">No</span><span class="sxs-lookup"><span data-stu-id="24e39-239">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-240">Número total de sesiones erróneas por grupo de registradores o servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="24e39-240">Total number of failed sessions per Registrar pool or Edge Server.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-sources"></a><span data-ttu-id="24e39-241">Métricas para fuentes destacadas</span><span class="sxs-lookup"><span data-stu-id="24e39-241">Metrics for Top Sources</span></span>

<span data-ttu-id="24e39-242">La siguiente tabla enumera la información proporcionada en el informe de distribución de errores basándose en los equipos que experimentaron más errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-242">The following table lists the information provided in the Failure Distribution Report based on the computers that experienced the most failures.</span></span>

### <a name="metrics-for-top-sources"></a><span data-ttu-id="24e39-243">Métricas para fuentes destacadas</span><span class="sxs-lookup"><span data-stu-id="24e39-243">Metrics for Top Sources</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e39-244">Nombre</span><span class="sxs-lookup"><span data-stu-id="24e39-244">Name</span></span></th>
<th><span data-ttu-id="24e39-245">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="24e39-245">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="24e39-246">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e39-246">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e39-247"><strong>Clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-247"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-248">No</span><span class="sxs-lookup"><span data-stu-id="24e39-248">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-249">Clasificación relativa de sesiones con errores por equipo.</span><span class="sxs-lookup"><span data-stu-id="24e39-249">Relative ranking failed sessions per computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-250"><strong>Principales fuentes</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-250"><strong>Top sources</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-251">No</span><span class="sxs-lookup"><span data-stu-id="24e39-251">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-252">Nombre del equipo que participó en la sesión con errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-252">Name of the computer involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-253"><strong>Sesiones</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-253"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-254">No</span><span class="sxs-lookup"><span data-stu-id="24e39-254">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-255">Cantidad total de sesiones con errores por equipo.</span><span class="sxs-lookup"><span data-stu-id="24e39-255">Total number of failed sessions per computer.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-components"></a><span data-ttu-id="24e39-256">Métricas para componentes destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-256">Metrics for Top Components</span></span>

<span data-ttu-id="24e39-257">En la tabla siguiente se enumera la información proporcionada en el informe de distribución de errores en función de los componentes de Microsoft Lync Server 2010 que experimentaron la mayoría de los errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-257">The following table lists the information provided in the Failure Distribution Report based on the Microsoft Lync Server 2010 components that experienced the most failures.</span></span>

### <a name="metrics-for-top-components"></a><span data-ttu-id="24e39-258">Métricas para componentes destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-258">Metrics for Top Components</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e39-259">Nombre</span><span class="sxs-lookup"><span data-stu-id="24e39-259">Name</span></span></th>
<th><span data-ttu-id="24e39-260">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="24e39-260">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="24e39-261">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e39-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e39-262"><strong>Clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-262"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-263">No</span><span class="sxs-lookup"><span data-stu-id="24e39-263">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-264">Clasificación relativa de las sesiones fallidas basadas en el componente de Lync Server 2010 (por ejemplo, ExumRouting, GroupChat o MediationServer).</span><span class="sxs-lookup"><span data-stu-id="24e39-264">Relative ranking of failed sessions based on Lync Server 2010 component (for example, ExumRouting, GroupChat, or MediationServer).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-265"><strong>Principales componentes</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-265"><strong>Top components</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-266">No</span><span class="sxs-lookup"><span data-stu-id="24e39-266">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-267">Nombre del componente que participó en la sesión con errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-267">Name of the component involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-268"><strong>Sesiones</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-268"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-269">No</span><span class="sxs-lookup"><span data-stu-id="24e39-269">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-270">Cantidad total de sesiones con errores por componente.</span><span class="sxs-lookup"><span data-stu-id="24e39-270">Total number of failed sessions per component.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-from-users"></a><span data-ttu-id="24e39-271">Métricas para usuarios destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-271">Metrics for Top From Users</span></span>

<span data-ttu-id="24e39-272">La siguiente tabla enumera la información proporcionada en el informe de distribución de errores basándose en los usuarios que experimentaron más errores al intentar llamar a otra persona (denominados remitentes).</span><span class="sxs-lookup"><span data-stu-id="24e39-272">The following table lists the information provided in the Failure Distribution Report based on users who experienced the most failures when they tried to call someone else (known as "From" users).</span></span>

### <a name="metrics-for-top-from-users"></a><span data-ttu-id="24e39-273">Métricas para usuarios destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-273">Metrics for Top From Users</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e39-274">Nombre</span><span class="sxs-lookup"><span data-stu-id="24e39-274">Name</span></span></th>
<th><span data-ttu-id="24e39-275">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="24e39-275">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="24e39-276">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e39-276">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e39-277"><strong>Clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-277"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-278">No</span><span class="sxs-lookup"><span data-stu-id="24e39-278">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-279">Clasificación relativa de sesiones con errores basándose en el usuario invitado a unirse a la sesión.</span><span class="sxs-lookup"><span data-stu-id="24e39-279">Relative ranking of failed sessions based on the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-280"><strong>Principales remitentes</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-280"><strong>Top from users</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-281">No</span><span class="sxs-lookup"><span data-stu-id="24e39-281">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-282">Dirección SIP del usuario invitado a unirse a la sesión.</span><span class="sxs-lookup"><span data-stu-id="24e39-282">SIP address of the user invited to join the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-283"><strong>Sesiones</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-283"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-284">No</span><span class="sxs-lookup"><span data-stu-id="24e39-284">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-285">Cantidad total de sesiones con error por usuario.</span><span class="sxs-lookup"><span data-stu-id="24e39-285">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-to-users"></a><span data-ttu-id="24e39-286">Métricas para principales destinatarios</span><span class="sxs-lookup"><span data-stu-id="24e39-286">Metrics for Top To Users</span></span>

<span data-ttu-id="24e39-287">La siguiente tabla enumera la información proporcionada en el informe de distribución de errores basándose en los usuarios que experimentaron más errores cuando otro usuario intentó llamarlos (denominados destinatarios).</span><span class="sxs-lookup"><span data-stu-id="24e39-287">The following table lists the information provided in the Failure Distribution Report based on the users who experienced the most failures when another user tried to call them (known as "To" users).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e39-288">Nombre</span><span class="sxs-lookup"><span data-stu-id="24e39-288">Name</span></span></th>
<th><span data-ttu-id="24e39-289">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="24e39-289">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="24e39-290">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e39-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e39-291"><strong>Clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-291"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-292">No</span><span class="sxs-lookup"><span data-stu-id="24e39-292">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-293">Clasificación relativa de sesiones con errores basándose en el usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="24e39-293">Relative ranking of failed sessions based on the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-294"><strong>Principales destinatarios</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-294"><strong>Top to users</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-295">No</span><span class="sxs-lookup"><span data-stu-id="24e39-295">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-296">Dirección SIP del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="24e39-296">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-297"><strong>Sesiones</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-297"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-298">No</span><span class="sxs-lookup"><span data-stu-id="24e39-298">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-299">Cantidad total de sesiones con error por usuario.</span><span class="sxs-lookup"><span data-stu-id="24e39-299">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-user-agents"></a><span data-ttu-id="24e39-300">Métricas para agentes de usuario destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-300">Metrics for Top User Agents</span></span>

<span data-ttu-id="24e39-301">La siguiente tabla enumera la información proporcionada en el informe de distribución de errores basándose en el software extremo que experimentó más errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-301">The following table lists the information provided in the Failure Distribution Report based on the endpoint software that experienced the most failures.</span></span>

### <a name="metrics-for-top-user-agents"></a><span data-ttu-id="24e39-302">Métricas para agentes de usuario destacados</span><span class="sxs-lookup"><span data-stu-id="24e39-302">Metrics for Top User Agents</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e39-303">Nombre</span><span class="sxs-lookup"><span data-stu-id="24e39-303">Name</span></span></th>
<th><span data-ttu-id="24e39-304">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="24e39-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="24e39-305">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e39-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24e39-306"><strong>Clasificación</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-306"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-307">No</span><span class="sxs-lookup"><span data-stu-id="24e39-307">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-p115">Clasificación relativa de sesiones con errores basándose en el agente de usuario (software) que participa en la sesión. Por ejemplo: RTCC/4.0.0.0 Enrutamiento de entrada/4.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="24e39-p115">Relative ranking of failed sessions based on the user agent (software) involved in the session. For example: RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24e39-310"><strong>Principales agentes de usuario</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-310"><strong>Top user agents</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-311">No</span><span class="sxs-lookup"><span data-stu-id="24e39-311">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-312">Nombre del agente de usuario que participó en la sesión con errores.</span><span class="sxs-lookup"><span data-stu-id="24e39-312">Name of the user agent involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24e39-313"><strong>Sesiones</strong></span><span class="sxs-lookup"><span data-stu-id="24e39-313"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="24e39-314">No</span><span class="sxs-lookup"><span data-stu-id="24e39-314">No</span></span></p></td>
<td><p><span data-ttu-id="24e39-315">Cantidad total de sesiones con errores por agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="24e39-315">Total number of failed sessions per user agent.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="24e39-316">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24e39-316">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

