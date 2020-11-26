---
title: 'Lync Server 2013: informe de voz y vídeo de punto a punto'
description: 'Lync Server 2013: informe de voz y vídeo de punto a punto.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Voice and Video Report
ms:assetid: e17c36b5-5a2f-4673-9696-3b2d31c2bb2f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615040(v=OCS.15)
ms:contentKeyID: 48185535
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43041926b3d6b57508b6ee4c53ca9cb055bcb348
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424698"
---
# <a name="peer-to-peer-voice-and-video-report-in-lync-server-2013"></a><span data-ttu-id="ceefb-103">Informe de voz y vídeo de punto a punto en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ceefb-103">Peer-to-Peer Voice and Video Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ceefb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ceefb-104">

<span> </span></span></span>

<span data-ttu-id="ceefb-105">_**Última modificación del tema:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="ceefb-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="ceefb-p101">El Informe de voz y vídeo punto a punto da una visión detallada de la distribución de las llamadas de voz y de las videollamadas en un período de tiempo especificado (por ejemplo, llamadas por hora o llamadas por día). El informe también da la opción de visualizar todas las llamadas de voz y videollamadas que se efectuaron, o de visualizar únicamente las llamadas correctas o las erróneas. Los informes muestran la información de las llamadas desglosadas en las agrupaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p101">The Peer-to-Peer Voice and Video Report provides a detailed look at the distribution of voice and video calls over a specified period of time (for example, calls per hour or calls per day). The report also gives you the option of viewing all the voice and video calls that were made, or of viewing only the successful or failed calls. The reports shows call information broken down into the following groupings:</span></span>

  - <span data-ttu-id="ceefb-109">Llamadas por grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="ceefb-109">Calls per pool</span></span>

  - <span data-ttu-id="ceefb-110">Llamadas por tipo de llamada (por ejemplo, una llamada de Lync a Lync, una llamada de Lync a una persona en la red RTC)</span><span class="sxs-lookup"><span data-stu-id="ceefb-110">Calls per call type (for example, a Lync to Lync call vs. a Lync call to a person on the PSTN network)</span></span>

  - <span data-ttu-id="ceefb-111">Llamadas por tipo de acceso (los usuarios que iniciaron sesión en la red interna comparados con los usuarios que iniciaron sesión en la red externa)</span><span class="sxs-lookup"><span data-stu-id="ceefb-111">Calls per access type (users logged on to the internal network vs. users logged on to the external network)</span></span>

  - <span data-ttu-id="ceefb-112">Llamadas por servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="ceefb-112">Calls per Mediation Server</span></span>

<div>

## <a name="to-access-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="ceefb-113">Para obtener acceso al informe de voz y vídeo punto a punto</span><span class="sxs-lookup"><span data-stu-id="ceefb-113">To access the peer-to-peer voice and video report</span></span>

<span data-ttu-id="ceefb-114">Obtenga acceso al informe de voz y vídeo punto a punto abriendo el Informe de resumen de actividad punto a punto y haciendo clic en una de las métricas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ceefb-114">You can access the Peer-to-Peer Voice and Video Report only by opening the Peer-to-Peer Activity Summary Report and then clicking any of the following metrics:</span></span>

  - <span data-ttu-id="ceefb-115">Total de sesiones de audio punto a punto</span><span class="sxs-lookup"><span data-stu-id="ceefb-115">Total peer-to-peer audio sessions</span></span>

  - <span data-ttu-id="ceefb-116">Total de minutos de audio punto a punto</span><span class="sxs-lookup"><span data-stu-id="ceefb-116">Total peer-to-peer audio minutes</span></span>

  - <span data-ttu-id="ceefb-117">Total de sesiones de vídeo punto a punto</span><span class="sxs-lookup"><span data-stu-id="ceefb-117">Total peer-to-peer video sessions</span></span>

  - <span data-ttu-id="ceefb-118">Total de minutos de vídeo punto a punto</span><span class="sxs-lookup"><span data-stu-id="ceefb-118">Total peer-to-peer video minutes</span></span>

</div>

<div>

## <a name="to-make-the-best-use-of-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="ceefb-119">Para sacar el máximo provecho del informe de voz y vídeo punto a punto</span><span class="sxs-lookup"><span data-stu-id="ceefb-119">To make the best use of the peer-to-peer voice and video report</span></span>

<span data-ttu-id="ceefb-p102">Existen varias formas de filtrar el informe de voz y vídeo punto a punto. No obstante, normalmente esas opciones de filtrado están ocultas a la vista. Para ver las opciones de filtrado que tiene disponibles, haga clic en el botón **Mostrar u ocultar parámetros** en la esquina superior derecha de la ventana del informe.</span><span class="sxs-lookup"><span data-stu-id="ceefb-p102">There are a number of ways you can filter the Peer-to-Peer Voice and Video Report. However, those filtering options are hidden from view by default. To view the filtering options available to you, click **Show/Hide Parameters** button in the upper-right corner of the Report window.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="ceefb-123">Filtros</span><span class="sxs-lookup"><span data-stu-id="ceefb-123">Filters</span></span>

<span data-ttu-id="ceefb-p103">Los filtros se emplean para recuperar un conjunto de datos más específico o para ver los datos de diferentes formas. En la siguiente tabla se enumeran los filtros que puede utilizar con el informe de voz y vídeo punto a punto.</span><span class="sxs-lookup"><span data-stu-id="ceefb-p103">Filters provide a way for you to return a more finely targeted set of data or to view the data in different ways. The following table lists the filters that you can use with the Peer-to-Peer Voice and Video Report.</span></span>

### <a name="peer-to-peer-voice-and-video-report-filters"></a><span data-ttu-id="ceefb-126">Filtros del informe de voz y vídeo punto a punto</span><span class="sxs-lookup"><span data-stu-id="ceefb-126">Peer-to-peer voice and video report filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ceefb-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceefb-127">Name</span></span></th>
<th><span data-ttu-id="ceefb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceefb-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-129"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-129"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-p104">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p104">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="ceefb-132">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="ceefb-132">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ceefb-p105">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ceefb-135">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ceefb-135">7/7/2012</span></span></p>
<p><span data-ttu-id="ceefb-136">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="ceefb-136">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ceefb-137">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ceefb-137">7/3/2012</span></span></p>
<p><span data-ttu-id="ceefb-138">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="ceefb-138">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ceefb-139"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-139"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-p106">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p106">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="ceefb-142">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="ceefb-142">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ceefb-p107">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ceefb-145">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ceefb-145">7/7/2012</span></span></p>
<p><span data-ttu-id="ceefb-146">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="ceefb-146">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ceefb-147">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ceefb-147">7/3/2012</span></span></p>
<p><span data-ttu-id="ceefb-148">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="ceefb-148">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-149"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-149"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-p108">Intervalo de tiempo. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ceefb-152">Cada hora (se puede ver un máximo de 25 horas)</span><span class="sxs-lookup"><span data-stu-id="ceefb-152">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ceefb-153">Cada día (se puede ver un máximo de 31 días)</span><span class="sxs-lookup"><span data-stu-id="ceefb-153">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ceefb-154">Cada semana (se puede ver un máximo de 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="ceefb-154">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ceefb-155">Cada mes (se puede ver un máximo de 12 meses)</span><span class="sxs-lookup"><span data-stu-id="ceefb-155">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="ceefb-156">Si las fechas de inicio y finalización superan la cantidad máxima de valores permitidos para el intervalo seleccionado, solo se mostrará la cantidad máxima de valores (comenzando en la fecha de inicio).</span><span class="sxs-lookup"><span data-stu-id="ceefb-156">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="ceefb-157">Por ejemplo, si selecciona el intervalo diario con una fecha de inicio de 7/7/2012 y una fecha de finalización de 2/28/2012, los datos se muestran para los días 8/7/2012 12:00 A.M. a 9/7/2012 12:00 A.M. (es decir, un total de 31 días de datos).</span><span class="sxs-lookup"><span data-stu-id="ceefb-157">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ceefb-158"><strong>Tipo de medio</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-158"><strong>Media type</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-p110">Indica el tipo de medio utilizado en la sesión. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p110">Indicates the type of media used in the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ceefb-161">Both</span><span class="sxs-lookup"><span data-stu-id="ceefb-161">Both</span></span></p></li>
<li><p><span data-ttu-id="ceefb-162">Audio</span><span class="sxs-lookup"><span data-stu-id="ceefb-162">Audio</span></span></p></li>
<li><p><span data-ttu-id="ceefb-163">Vídeo</span><span class="sxs-lookup"><span data-stu-id="ceefb-163">Video</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-164"><strong>Disposición de llamada</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-164"><strong>Call disposition</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-p111">Indica el resultado de la sesión. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p111">Indicates the success or failure of the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ceefb-167">[Todas]</span><span class="sxs-lookup"><span data-stu-id="ceefb-167">[All]</span></span></p></li>
<li><p><span data-ttu-id="ceefb-168">Llamadas correctas</span><span class="sxs-lookup"><span data-stu-id="ceefb-168">Success Calls</span></span></p></li>
<li><p><span data-ttu-id="ceefb-169">Llamadas con error</span><span class="sxs-lookup"><span data-stu-id="ceefb-169">Failed Calls</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ceefb-170"><strong>Informe por</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-170"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-p112">Indica los valores a utilizar en el informe. Seleccione una opción de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p112">Indicates the values to be used in the report. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ceefb-173">Recuento de sesiones</span><span class="sxs-lookup"><span data-stu-id="ceefb-173">Session count</span></span></p></li>
<li><p><span data-ttu-id="ceefb-174">Minutos de la llamada</span><span class="sxs-lookup"><span data-stu-id="ceefb-174">Call minutes</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="ceefb-175">Métricas de actividad de voz y vídeo punto a punto por grupo</span><span class="sxs-lookup"><span data-stu-id="ceefb-175">Metrics for peer-to-peer voice and video activity by Pool</span></span>

<span data-ttu-id="ceefb-176">En la siguiente tabla se enumera la información provista en el Informe de voz y vídeo punto a punto para cada grupo.</span><span class="sxs-lookup"><span data-stu-id="ceefb-176">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each pool.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="ceefb-177">Métricas de actividad de voz y vídeo punto a punto por grupo</span><span class="sxs-lookup"><span data-stu-id="ceefb-177">Metrics for peer-to-peer voice and video activity by pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ceefb-178">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceefb-178">Name</span></span></th>
<th><span data-ttu-id="ceefb-179">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="ceefb-179">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ceefb-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceefb-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-181"><strong>Grupo de servidores</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-181"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-182">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-182">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-183">Nombre del grupo de registradores o del servidor perimetral usado para la llamada.</span><span class="sxs-lookup"><span data-stu-id="ceefb-183">Name of the Registrar pool or Edge Server used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ceefb-184"><strong>Fecha y hora</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-184"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-185">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-185">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-186">Fecha/hora en que se produjo la llamada.</span><span class="sxs-lookup"><span data-stu-id="ceefb-186">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-187"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-187"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-188">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-188">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-189">Cantidad total de sesiones o recuento total de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ceefb-189">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="ceefb-190">Métricas de actividad de voz y vídeo punto a punto por tipo de llamada</span><span class="sxs-lookup"><span data-stu-id="ceefb-190">Metrics for peer-to-peer voice and video activity by call type</span></span>

<span data-ttu-id="ceefb-191">En la siguiente tabla se enumera la información proporcionada en el Informe de voz y vídeo punto a punto para cada tipo de llamada realizada.</span><span class="sxs-lookup"><span data-stu-id="ceefb-191">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each type of call that was made.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="ceefb-192">Métricas de actividad de voz y vídeo punto a punto por tipo de llamada</span><span class="sxs-lookup"><span data-stu-id="ceefb-192">Metrics for peer-to-peer voice and video activity by call type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ceefb-193">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceefb-193">Name</span></span></th>
<th><span data-ttu-id="ceefb-194">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="ceefb-194">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ceefb-195">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceefb-195">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-196"><strong>Tipo de llamada</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-196"><strong>Call type</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-197">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-197">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-p113">Indica el tipo de llamada que se realizó. Los valores son uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p113">Indicates the type of call that was made. Values are one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ceefb-200">UC-a-UC</span><span class="sxs-lookup"><span data-stu-id="ceefb-200">UC-to-UC</span></span></p></li>
<li><p><span data-ttu-id="ceefb-201">UC-a-PSTN</span><span class="sxs-lookup"><span data-stu-id="ceefb-201">UC-to-PSTN</span></span></p></li>
<li><p><span data-ttu-id="ceefb-202">PSTN-a-UC</span><span class="sxs-lookup"><span data-stu-id="ceefb-202">PSTN-to-UC</span></span></p></li>
<li><p><span data-ttu-id="ceefb-203">PSTN-a-PSTN</span><span class="sxs-lookup"><span data-stu-id="ceefb-203">PSTN-to-PSTN</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ceefb-204"><strong>Fecha y hora</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-204"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-205">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-205">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-206">Fecha/hora en que se produjo la llamada.</span><span class="sxs-lookup"><span data-stu-id="ceefb-206">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-207"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-207"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-208">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-208">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-209">Cantidad total de sesiones o recuento total de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ceefb-209">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="ceefb-210">Métricas de actividad de voz y vídeo punto a punto por tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="ceefb-210">Metrics for peer-to-peer voice and video activity by access type</span></span>

<span data-ttu-id="ceefb-211">En la siguiente tabla se enumera la información proporcionada en el Informe de voz y vídeo punto a punto para cada tipo de acceso a la red.</span><span class="sxs-lookup"><span data-stu-id="ceefb-211">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each network access type.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="ceefb-212">Métricas de actividad de voz y vídeo punto a punto por tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="ceefb-212">Metrics for peer-to-peer voice and video activity by access type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ceefb-213">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceefb-213">Name</span></span></th>
<th><span data-ttu-id="ceefb-214">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="ceefb-214">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ceefb-215">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceefb-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-216"><strong>Tipo de actividad</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-216"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-217">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-217">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-p114">Indica si los clientes habían iniciado sesión en la red interna o en la externa cuando se realizó la llamada. Generalmente, los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ceefb-p114">Indicates whether the clients were logged on to the internal network or the external network when the call was placed. Values are typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ceefb-220">Interna</span><span class="sxs-lookup"><span data-stu-id="ceefb-220">Internal</span></span></p></li>
<li><p><span data-ttu-id="ceefb-221">Externa</span><span class="sxs-lookup"><span data-stu-id="ceefb-221">External</span></span></p></li>
<li><p><span data-ttu-id="ceefb-222">Mixta</span><span class="sxs-lookup"><span data-stu-id="ceefb-222">Mixed</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ceefb-223"><strong>Fecha y hora</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-223"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-224">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-224">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-225">Fecha/hora en que se produjo la llamada.</span><span class="sxs-lookup"><span data-stu-id="ceefb-225">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-226"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-226"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-227">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-227">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-228">Cantidad total de sesiones o recuento total de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ceefb-228">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="ceefb-229">Métricas de actividad de voz y vídeo punto a punto por servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="ceefb-229">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<span data-ttu-id="ceefb-230">En la siguiente tabla se enumera la información proporcionada en el informe de voz y vídeo de punto a punto para cada servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="ceefb-230">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each Mediation Server.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="ceefb-231">Métricas de actividad de voz y vídeo punto a punto por servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="ceefb-231">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ceefb-232">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceefb-232">Name</span></span></th>
<th><span data-ttu-id="ceefb-233">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="ceefb-233">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ceefb-234">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceefb-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-235"><strong>Servidor de mediación</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-235"><strong>Mediation Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-236">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-236">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-237">Nombre del servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="ceefb-237">Name of the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ceefb-238"><strong>Fecha y hora</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-238"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-239">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-239">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-240">Fecha/hora en que se produjo la llamada.</span><span class="sxs-lookup"><span data-stu-id="ceefb-240">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ceefb-241"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="ceefb-241"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="ceefb-242">No</span><span class="sxs-lookup"><span data-stu-id="ceefb-242">No</span></span></p></td>
<td><p><span data-ttu-id="ceefb-243">Cantidad total de sesiones o recuento total de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ceefb-243">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ceefb-244">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ceefb-244">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

