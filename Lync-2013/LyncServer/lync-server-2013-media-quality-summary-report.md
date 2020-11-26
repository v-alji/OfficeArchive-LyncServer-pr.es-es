---
title: 'Lync Server 2013: informe Resumen de calidad de medios'
description: 'Lync Server 2013: informe Resumen de calidad de medios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Summary Report
ms:assetid: 8bd59ad6-3087-49c8-b692-5573fe2ffcd8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615012(v=OCS.15)
ms:contentKeyID: 48184776
ms.date: 06/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2616b7e3cdea9df7b004745a5c407188870903c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446049"
---
# <a name="media-quality-summary-report-in-lync-server-2013"></a><span data-ttu-id="f4aa0-103">Informe Resumen de calidad de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4aa0-103">Media Quality Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f4aa0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f4aa0-104">

<span> </span></span></span>

<span data-ttu-id="f4aa0-105">_**Última modificación del tema:** 2016-06-29_</span><span class="sxs-lookup"><span data-stu-id="f4aa0-105">_**Topic Last Modified:** 2016-06-29_</span></span>

<span data-ttu-id="f4aa0-106">El Informe de resumen de calidad de medios es, quizás, la mejor opción para analizar la calidad de las llamadas en su organización: este informe proporciona métricas de llamadas de calidad de la experiencia (QoE) detalladas y desglosadas en las siguientes categorías:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-106">The Media Quality Summary Report is perhaps your best bet for analyzing call quality in your organization: this report provides detailed Quality of Experience (QoE) call metrics broken down into the following categories:</span></span>

  - <span data-ttu-id="f4aa0-107">Llamadas de par a par de UC (como una llamada de Microsoft Lync 2013 a Microsoft Lync 2013)</span><span class="sxs-lookup"><span data-stu-id="f4aa0-107">UC Peer to Peer Calls (such as a Microsoft Lync 2013 to Microsoft Lync 2013 call)</span></span>

  - <span data-ttu-id="f4aa0-108">Sesiones de conferencia de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-108">UC Conference Sessions</span></span>

  - <span data-ttu-id="f4aa0-109">Sesiones de conferencia de RTC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-109">PSTN Conference Sessions</span></span>

  - <span data-ttu-id="f4aa0-110">Llamadas RTC: desvío de medios</span><span class="sxs-lookup"><span data-stu-id="f4aa0-110">PSTN Calls: Media Bypass</span></span>

  - <span data-ttu-id="f4aa0-111">Llamadas RTC (sin desvío): sección de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-111">PSTN Calls (Non-Bypass): UC Leg</span></span>

  - <span data-ttu-id="f4aa0-112">Llamadas RTC (sin desvío): sección de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="f4aa0-112">PSTN Calls (Non-Bypass): Gateway Leg</span></span>

  - <span data-ttu-id="f4aa0-113">Otros tipos de llamada</span><span class="sxs-lookup"><span data-stu-id="f4aa0-113">Other Call Types</span></span>

<span data-ttu-id="f4aa0-114">Al abrir el informe por primera vez, se ve la información de resumen de cada una de estas categorías.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-114">When you first open the report, you see summary information for each of these categories.</span></span> <span data-ttu-id="f4aa0-115">Sin salir del informe, puede expandir cada categoría para ver subcategorías, como las llamadas realizadas desde Office Communicator 2007 R2 a Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-115">Without leaving the report, you can expand each category to look at subcategories such as calls made from Office Communicator 2007 R2 to Lync 2013.</span></span> <span data-ttu-id="f4aa0-116">A su vez, puede profundizar en esas subcategorías para ver detalles sobre cada llamada realizada dentro de esa subcategoría.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-116">In turn, you can then drill down into these subcategories to see details about each call made within that subcategory.</span></span>

<span data-ttu-id="f4aa0-117">En Microsoft Lync Server 2013, el informe Resumen de la calidad de medios también divide los datos en tres tipos de llamadas: llamadas de audio, videollamadas y llamadas de uso compartido de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-117">In Microsoft Lync Server 2013 the Media Quality Summary Report further breaks the data down into three call types: audio calls, video calls, and application sharing calls.</span></span> <span data-ttu-id="f4aa0-118">Cada tipo de llamada tiene su propia sección en el informe y su propio conjunto personalizado de métricas de llamada.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-118">Each call type has its own section in the report, and its own custom set of call metrics.</span></span>

<span data-ttu-id="f4aa0-119">El Informe de resumen de calidad de medios también permite aplicar filtros para poder comparar la calidad de las llamadas: llamadas por cable frente a inalámbricas, llamadas internas frente a externas y llamadas de VPN frente a llamadas distintas de VPN.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-119">The Media Quality Summary Report also allows you to apply filters that enable you to compare the call quality of wired calls vs. wireless calls, internal calls vs. external calls, and VPN calls vs. non-VPN calls.</span></span>

<div>

## <a name="accessing-the-media-quality-summary-report"></a><span data-ttu-id="f4aa0-120">Acceso al Informe de resumen de calidad de medios</span><span class="sxs-lookup"><span data-stu-id="f4aa0-120">Accessing the Media Quality Summary Report</span></span>

<span data-ttu-id="f4aa0-121">Al Informe de resumen de calidad de medios se obtiene acceso desde la página principal de Informes de supervisión.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-121">The Media Quality Summary Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="f4aa0-122">Puede explorar en profundidad el [Informe de la lista de llamadas en Lync Server 2013](lync-server-2013-call-list-report.md) haciendo clic en cualquiera de las siguientes métricas:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-122">You can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="f4aa0-123">Volumen de llamadas</span><span class="sxs-lookup"><span data-stu-id="f4aa0-123">Call volume</span></span>

  - <span data-ttu-id="f4aa0-124">Porcentaje de llamadas deficientes</span><span class="sxs-lookup"><span data-stu-id="f4aa0-124">Poor call percentage</span></span>

<span data-ttu-id="f4aa0-125">Además, puede obtener acceso al Informe de resumen de calidad de medios haciendo clic en cualquiera de las siguientes métricas de llamadas de audio:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-125">In addition, you can access the Media Quality Metrics Distribution Report by clicking any of the following audio call metrics:</span></span>

  - <span data-ttu-id="f4aa0-126">Recorrido de ida y vuelta (ms)</span><span class="sxs-lookup"><span data-stu-id="f4aa0-126">Round trip (ms)</span></span>

  - <span data-ttu-id="f4aa0-127">Degradación (MOS)</span><span class="sxs-lookup"><span data-stu-id="f4aa0-127">Degradation (MOS)</span></span>

  - <span data-ttu-id="f4aa0-128">Pérdida de paquetes</span><span class="sxs-lookup"><span data-stu-id="f4aa0-128">Packet loss</span></span>

  - <span data-ttu-id="f4aa0-129">Vibración (ms)</span><span class="sxs-lookup"><span data-stu-id="f4aa0-129">Jitter (ms)</span></span>

  - <span data-ttu-id="f4aa0-130">Tasa de recuperación de muestras ocultas</span><span class="sxs-lookup"><span data-stu-id="f4aa0-130">Healer concealed ratio</span></span>

  - <span data-ttu-id="f4aa0-131">Tasa de recuperación de muestras extendidas</span><span class="sxs-lookup"><span data-stu-id="f4aa0-131">Healer stretched ratio</span></span>

  - <span data-ttu-id="f4aa0-132">Tasa de recuperación de muestras comprimidas</span><span class="sxs-lookup"><span data-stu-id="f4aa0-132">Healer compressed ratio</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="f4aa0-133">Filtros</span><span class="sxs-lookup"><span data-stu-id="f4aa0-133">Filters</span></span>

<span data-ttu-id="f4aa0-p104">Los filtros se emplean para recuperar un conjunto de datos más específico o para ver los datos devueltos de diferentes formas. Por ejemplo, el informe de resumen de calidad de los medios permite filtrar los datos devueltos por el tipo de acceso (acceso interno o externo) o por tipo de conexión de red (cableada o inalámbrica). También se puede elegir cómo agrupar los datos. En este caso, las llamadas se agrupan por hora, día, semana o mes.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Media Quality Summary Report enables you to filter the returned data by such things as access type (that is, interval access vs. external access) or by wired/wireless network connection. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="f4aa0-138">En la tabla siguiente se muestran los filtros que se pueden utilizar en el informe de resumen de calidad de los medios.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-138">The following table lists the filters that you can use with the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-filters"></a><span data-ttu-id="f4aa0-139">Filtros del informe de resumen de calidad de los medios</span><span class="sxs-lookup"><span data-stu-id="f4aa0-139">Media Quality Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4aa0-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4aa0-140">Name</span></span></th>
<th><span data-ttu-id="f4aa0-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4aa0-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-142"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-142"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p105">Fecha y hora de inicio del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de inicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="f4aa0-145">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-145">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="f4aa0-p106">Si no escribe una hora de inicio, el informe se iniciará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="f4aa0-148">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="f4aa0-148">7/7/2012</span></span></p>
<p><span data-ttu-id="f4aa0-149">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="f4aa0-149">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="f4aa0-150">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="f4aa0-150">7/3/2012</span></span></p>
<p><span data-ttu-id="f4aa0-151">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-151">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-152"><strong>Hasta</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-152"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p107">Fecha y hora de finalización del intervalo de tiempo. Para ver los datos por horas, escriba la fecha y hora de finalización como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="f4aa0-155">7/7/2012 1:00 P.M.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-155">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="f4aa0-p108">Si no escribe una hora de finalización, el informe finalizará automáticamente a las 12:00 del día especificado. Para ver los datos por día, escriba solo la fecha:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="f4aa0-158">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="f4aa0-158">7/7/2012</span></span></p>
<p><span data-ttu-id="f4aa0-159">Para verlos por semanas o por meses, escriba una fecha que caiga en cualquier punto de la semana o del mes que desee ver (no es necesario escribir el primer día de la semana o del mes):</span><span class="sxs-lookup"><span data-stu-id="f4aa0-159">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="f4aa0-160">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="f4aa0-160">7/3/2012</span></span></p>
<p><span data-ttu-id="f4aa0-161">Las semanas siempre van del domingo al sábado.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-161">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-162"><strong>Tipo de acceso</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-162"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p109">Indica si el cliente había iniciado sesión en la red interna o en la externa cuando se realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p109">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f4aa0-165">[Todas]</span><span class="sxs-lookup"><span data-stu-id="f4aa0-165">[All]</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-166">Interno</span><span class="sxs-lookup"><span data-stu-id="f4aa0-166">Internal</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-167">Externo</span><span class="sxs-lookup"><span data-stu-id="f4aa0-167">External</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-168"><strong>Tipo de red</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-168"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p110">Indica el tipo de red al que estaba conectado el cliente cuando realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p110">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f4aa0-171">[Todas]</span><span class="sxs-lookup"><span data-stu-id="f4aa0-171">[All]</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-172">Cableada</span><span class="sxs-lookup"><span data-stu-id="f4aa0-172">Wired</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-173">Inalámbrica</span><span class="sxs-lookup"><span data-stu-id="f4aa0-173">Wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-174"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-174"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p111">Indica si un cliente externo estaba utilizando una conexión de red privada virtual (VPN) cuando se realizó la llamada. Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p111">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f4aa0-177">[Todas]</span><span class="sxs-lookup"><span data-stu-id="f4aa0-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-178">VPN</span><span class="sxs-lookup"><span data-stu-id="f4aa0-178">VPN</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-179">Distinto de VPN</span><span class="sxs-lookup"><span data-stu-id="f4aa0-179">Non-VPN</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="f4aa0-180">Métricas</span><span class="sxs-lookup"><span data-stu-id="f4aa0-180">Metrics</span></span>

<span data-ttu-id="f4aa0-181">En la tabla siguiente se muestra la información que recoge el informe de resumen de calidad de los medios.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-181">The following table lists the information provided in the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-metrics-audio-call-summary"></a><span data-ttu-id="f4aa0-182">Métricas del Informe de resumen de calidad de medios: resumen de llamadas de audio</span><span class="sxs-lookup"><span data-stu-id="f4aa0-182">Media Quality Summary Report Metrics: Audio Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4aa0-183">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4aa0-183">Name</span></span></th>
<th><span data-ttu-id="f4aa0-184">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="f4aa0-184">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f4aa0-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4aa0-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-186"><strong>Tipo de llamada/tipo de extremo</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-186"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-187">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-187">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p112">Cuando se hace clic en este elemento, el informe muestra información detallada sobre las llamadas de ese tipo. Los tipos de llamadas son:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p112">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="f4aa0-190">Llamadas de punto a punto de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-190">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-191">Sesiones de conferencia de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-191">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-192">Sesiones de conferencia de RTC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-192">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-193">Llamadas RTC: desvío de medios</span><span class="sxs-lookup"><span data-stu-id="f4aa0-193">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-194">Llamadas RTC (sin desvío): sección de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-194">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-195">Llamadas RTC (sin desvío): sección de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="f4aa0-195">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-196">Otros tipos de llamada</span><span class="sxs-lookup"><span data-stu-id="f4aa0-196">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-197"><strong>Volumen de llamadas</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-197"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-198">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-198">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-199">Cantidad total de llamadas por tipo.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-199">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-200"><strong>Porcentaje de llamadas deficientes</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-200"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-201">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-201">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p113">Cantidad total de llamadas clasificadas como deficientes. Una llamada deficiente es aquella durante la que al menos uno de los valores medidos supera el valor permitido, por ejemplo, una llamada con un exceso de vibraciones.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p113">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-204"><strong>Volumen de llamadas (llamada inalámbrica)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-204"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-205">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-205">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-206">Cantidad total de llamadas que ha empleado una conexión inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-206">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-207"><strong>Volumen de llamadas (llamada VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-207"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-208">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-208">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-209">Cantidad total de llamadas que ha empleado una conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-209">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-210"><strong>Volumen de llamadas (llamada externa)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-210"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-211">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-211">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-212">Cantidad de llamadas que ha empleado una conexión externa, es decir, una conexión fuera de la red interna.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-212">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-213"><strong>Recorrido de ida y vuelta (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-213"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-214">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-214">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p114">Tiempo medio (en milisegundos) necesario para que un paquete de protocolo de transporte en tiempo real (RTP) llegue a otro extremo y vuelva. Los tiempos de ida y vuelta de 100 milisegundos o menos se consideran de calidad aceptable.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p114">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="f4aa0-p115">Los valores elevados en los tiempos del recorrido de ida y vuelta pueden deberse a que se trata de enrutamientos de llamadas internacionales, una configuración incorrecta del enrutamiento o a la sobrecarga en el servidor multimedia y causan dificultades en las conversaciones de audio bidireccionales en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p115">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-219"><strong>Degradación (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-219"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-220">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-220">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-221">Cantidad media de degradación de la puntuación de opinión media (MOS) experimentada durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-221">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="f4aa0-222">Los valores de degradación oscilan entre un mínimo de 0,0 y un máximo de 5,0.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-222">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="f4aa0-223">Un valor de 0,5 o menos constituye una degradación aceptable.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-223">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="f4aa0-224">Históricamente, las puntuaciones de opinión media se calculaban haciendo que los usuarios puntuaran la calidad de una llamada en una escala del 1 al 5.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-224">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="f4aa0-225">En Lync Server, Lync Server usa un conjunto de algoritmos para predecir cómo los usuarios habrían calificado una llamada.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-225">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="f4aa0-p117">Los valores altos de degradación pueden ser producto de la congestión, falta de ancho de banda, congestión o interferencias en una conexión inalámbrica, o la sobrecarga de un servidor multimedia o servidor de extremo. Una degradación alta causa la distorsión o la pérdida del audio.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p117">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-228"><strong>Pérdida de paquetes</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-228"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-229">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-229">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p118">Tasa media de pérdida de paquetes RTP. Se habla de pérdida de paquetes cuando los paquetes RTP, un protocolo que se usa para transmitir audio y vídeo a través de Internet, no llegan a su destino. Una tasa alta de pérdida suele deberse a la congestión, falta de ancho de banda, congestión o interferencias en una conexión inalámbrica, o la sobrecarga de un servidor multimedia. Generalmente, la pérdida de paquetes da lugar a la pérdida o la distorsión del audio.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p118">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-233"><strong>Vibración (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-233"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-234">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-234">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-235">Valor medio de las vibraciones detectadas entre la llagada de paquetes RTP.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-235">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="f4aa0-236">(La vibración es una medida de la &quot; irregularidad &quot; de una llamada). Los valores de vibración elevada suelen estar causados por una congestión o un servidor multimedia sobrecargado y tienen como resultado una distorsión o pérdida de audio.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-236">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-237"><strong>Tasa de recuperación de muestras ocultas</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-237"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-238">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-238">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p120">Tasa media de muestras de audio ocultas respecto a la cantidad total de muestras. Una muestra de audio oculta es una técnica que se emplea para suavizar la transición brusca que normalmente supondría la pérdida de paquetes de red. Los valores elevados indican niveles igualmente elevados de aplicación de ocultación de pérdidas a causa de la pérdida de paquetes o de las vibraciones, y dan lugar a la distorsión o pérdida del audio.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p120">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-241"><strong>Tasa de recuperación de muestras extendidas</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-241"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-242">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-242">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p121">Tasa media de muestras de audio extendidas respecto a la cantidad total de muestras. El audio extendido es el audio que se expande para ayudar a mantener el nivel de calidad de la llamada cuando se detecta la pérdida de paquetes en la red. Los valores elevados indican un grado igualmente elevado de extensión de las muestras a causa de las vibraciones, y dan lugar a un audio robótico o distorsionado.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p121">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-245"><strong>Tasa de recuperación de muestras comprimidas</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-245"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-246">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-246">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p122">Tasa media de muestras de audio comprimidas respecto a la cantidad total de muestras. El audio comprimido es el audio que se comprime para ayudar a mantener el nivel de calidad de la llamada cuando se detecta la pérdida de paquetes en la red. Los valores altos indican un elevado grado de compresión de las muestras a causa de las vibraciones y las consecuencias son un audio acelerado o distorsionado.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p122">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-video-call-summary"></a><span data-ttu-id="f4aa0-249">Métricas del Informe de resumen de calidad de medios: resumen de videollamadas</span><span class="sxs-lookup"><span data-stu-id="f4aa0-249">Media Quality Summary Report Metrics: Video Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4aa0-250">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4aa0-250">Name</span></span></th>
<th><span data-ttu-id="f4aa0-251">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="f4aa0-251">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f4aa0-252">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4aa0-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-253"><strong>Tipo de llamada/tipo de extremo</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-253"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-254">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-254">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p123">Cuando se hace clic en este elemento, el informe muestra información detallada sobre las llamadas de ese tipo. Los tipos de llamadas son:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p123">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="f4aa0-257">Llamadas de punto a punto de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-257">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-258">Sesiones de conferencia de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-258">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-259">Sesiones de conferencia de RTC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-259">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-260">Llamadas RTC: desvío de medios</span><span class="sxs-lookup"><span data-stu-id="f4aa0-260">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-261">Llamadas RTC (sin desvío): sección de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-261">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-262">Llamadas RTC (sin desvío): sección de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="f4aa0-262">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-263">Otros tipos de llamada</span><span class="sxs-lookup"><span data-stu-id="f4aa0-263">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-264"><strong>Volumen de llamadas</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-264"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-265">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-265">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-266">Cantidad total de llamadas por tipo.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-266">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-267"><strong>Porcentaje de llamadas deficientes</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-267"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-268">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-268">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p124">Cantidad total de llamadas clasificadas como deficientes. Una llamada deficiente es aquella durante la que al menos uno de los valores medidos supera el valor permitido, por ejemplo, una llamada con un exceso de vibraciones.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p124">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-271"><strong>Volumen de llamadas (llamada inalámbrica)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-271"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-272">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-272">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-273">Cantidad total de llamadas que ha empleado una conexión inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-273">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-274"><strong>Volumen de llamadas (llamada VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-274"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-275">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-275">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-276">Cantidad total de llamadas que ha empleado una conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-276">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-277"><strong>Volumen de llamadas (llamada externa)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-277"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-278">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-278">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-279">Cantidad de llamadas que ha empleado una conexión externa, es decir, una conexión fuera de la red interna.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-279">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-280"><strong>Velocidad de bits media (Kbits/s)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-280"><strong>Avg bit-rate (Kbits/s)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-281">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-281">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-282">Velocidad de bits de vídeo media (en kilobits por segundo).</span><span class="sxs-lookup"><span data-stu-id="f4aa0-282">Average video bit rate (in kilobits per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-283"><strong>% de velocidad de bits baja</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-283"><strong>Low bit-rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-284">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-284">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-285">Porcentaje de la llamada con una velocidad de bits baja.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-285">Percentage of the call where the bit rate was low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-286"><strong>Pérdida de paquetes de salida</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-286"><strong>Outbound packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-287">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-287">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p125">Pérdida de paquetes del Protocolo de transporte en tiempo real (RTP) correspondiente a los paquetes salientes (se habla de pérdida de paquetes cuando los paquetes RTP, un protocolo que se usa para transmitir audio y vídeo a través de Internet, no llegan a su destino). Una tasa alta de pérdida se suele deber a la congestión, la falta de ancho de banda, la congestión o las interferencias en una conexión inalámbrica o la sobrecarga de un servidor de medios. Generalmente, la pérdida de paquetes da lugar a la pérdida o la distorsión del audio.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p125">Real-Time Transport Protocol (RTP) packet loss for outbound packets. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-291"><strong>% fotogramas congelados</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-291"><strong>Frozen frame %</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-292">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-292">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p126">Porcentaje de fotogramas "congelados". En un fotograma congelado, el vídeo detiene su avance mientras que la parte de audio de la llamada continúa.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p126">Percentage of “frozen” frames. In a frozen frame, the video stops advancing while the audio portion of the call continues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-295"><strong>Velocidad de fotogramas media de salida</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-295"><strong>Outbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-296">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-296">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-297">Velocidad de fotogramas media para las transmisiones de salida durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-297">Average frame rate for outbound transmissions during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-298"><strong>Velocidad de fotogramas media de entrada</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-298"><strong>Inbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-299">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-299">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-300">Velocidad de fotogramas media para las transmisiones de entrada durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-300">Average frame rate for incoming transmissions during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-301"><strong>% de velocidad de fotogramas baja de entrada</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-301"><strong>Inbound low frame rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-302">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-302">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-303">Porcentaje de la llamada con una velocidad de bits baja para el vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-303">Percentage of the call where the bit rate for incoming video was low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-304"><strong>% de estado del cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-304"><strong>Client health %</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f4aa0-305">Indica el estado relativo del dispositivo cliente durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-305">Indicates the relative health of the client device during the call.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-application-sharing-call-summary"></a><span data-ttu-id="f4aa0-306">Métricas del Informe de resumen de calidad de medios: resumen de llamadas de uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f4aa0-306">Media Quality Summary Report Metrics: Application Sharing Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4aa0-307">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4aa0-307">Name</span></span></th>
<th><span data-ttu-id="f4aa0-308">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="f4aa0-308">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f4aa0-309">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4aa0-309">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-310"><strong>Tipo de llamada/tipo de extremo</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-310"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-311">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-311">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p127">Cuando se hace clic en este elemento, el informe muestra información detallada sobre las llamadas de ese tipo. Los tipos de llamadas son:</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p127">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="f4aa0-314">Llamadas de punto a punto de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-314">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-315">Sesiones de conferencia de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-315">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-316">Sesiones de conferencia de RTC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-316">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-317">Llamadas RTC: desvío de medios</span><span class="sxs-lookup"><span data-stu-id="f4aa0-317">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-318">Llamadas RTC (sin desvío): sección de UC</span><span class="sxs-lookup"><span data-stu-id="f4aa0-318">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-319">Llamadas RTC (sin desvío): sección de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="f4aa0-319">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="f4aa0-320">Otros tipos de llamada</span><span class="sxs-lookup"><span data-stu-id="f4aa0-320">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-321"><strong>Volumen de llamadas</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-321"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-322">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-322">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-323">Cantidad total de llamadas por tipo.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-323">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-324"><strong>Porcentaje de llamadas deficientes</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-324"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-325">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-325">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p128">Cantidad total de llamadas clasificadas como deficientes. Una llamada deficiente es aquella durante la que al menos uno de los valores medidos supera el valor permitido, por ejemplo, una llamada con un exceso de vibraciones.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p128">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-328"><strong>Volumen de llamadas (llamada inalámbrica)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-328"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-329">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-329">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-330">Cantidad total de llamadas que ha empleado una conexión inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-330">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-331"><strong>Volumen de llamadas (llamada VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-331"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-332">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-332">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-333">Cantidad total de llamadas que ha empleado una conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-333">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-334"><strong>Volumen de llamadas (llamada externa)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-334"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-335">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-335">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-336">Cantidad de llamadas que ha empleado una conexión externa, es decir, una conexión fuera de la red interna.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-336">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-337"><strong>Vibración (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-337"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-338">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-338">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-339">Valor medio de las vibraciones detectadas entre la llagada de paquetes RTP.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-339">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="f4aa0-340">(La vibración es una medida de la &quot; irregularidad &quot; de una llamada). Los valores de vibración elevada suelen estar causados por una congestión o un servidor multimedia sobrecargado y tienen como resultado una distorsión o pérdida de audio.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-340">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-341"><strong>Unidireccional relativo medio</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-341"><strong>Avg. relative one way</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-342">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-342">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p130">Retraso unidireccional relativo medio entre dos extremos de medios. Es una medición de la latencia de un solo salto.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p130">Average relative one-way delay between two media endpoints. This is a single-hop latency measure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4aa0-345"><strong>Latencia media de procesamiento de iconos RDP</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-345"><strong>Avg. RDP tile processing latency</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-346">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-346">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-p131">La latencia media de procesamiento de iconos RDP en el servidor de conferencias AS durante el transcurso de la sesión de visualización. Una media alta refleja un retraso mayor en la experiencia de visualización e incluye latencia de red. Un servidor de conferencias sobrecargado podría experimentar una media mayor de retrasos.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-p131">The average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session. A high average reflects a longer delay in the viewing experience, and includes network latency. An overloaded conferencing server may experience higher average delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4aa0-350"><strong>% total de iconos dañados</strong></span><span class="sxs-lookup"><span data-stu-id="f4aa0-350"><strong>Total spoiled tile %</strong></span></span></p></td>
<td><p><span data-ttu-id="f4aa0-351">No</span><span class="sxs-lookup"><span data-stu-id="f4aa0-351">No</span></span></p></td>
<td><p><span data-ttu-id="f4aa0-352">Porcentaje total de iconos RDP dañados.</span><span class="sxs-lookup"><span data-stu-id="f4aa0-352">Total percentage of spoiled RDP tiles.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f4aa0-353">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f4aa0-353">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

