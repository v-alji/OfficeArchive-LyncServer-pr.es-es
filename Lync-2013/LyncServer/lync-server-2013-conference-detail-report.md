---
title: 'Lync Server 2013: informe detallado de la Conferencia'
description: 'Lync Server 2013: informe detallado de la Conferencia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Detail Report
ms:assetid: 1d61cd81-dcfe-40b4-9a41-a73b038bc216
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204728(v=OCS.15)
ms:contentKeyID: 48183565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07c50b545f4a9ee3308a840fc2aa5a15e617a5bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398519"
---
# <a name="conference-detail-report-in-lync-server-2013"></a><span data-ttu-id="4f634-103">Informe detallado de la Conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f634-103">Conference Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4f634-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4f634-104">

<span> </span></span></span>

<span data-ttu-id="4f634-105">_**Última modificación del tema:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="4f634-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="4f634-p101">El Informe de detalles de conferencia proporciona información detallada sobre todos los usuarios que participaron en una conferencia. Por ejemplo, puede ver información como la fecha y hora en que un usuario se conectó a la conferencia, la fecha y hora en la que el usuario se desconectó de la conferencia y el agente del usuario del extremo que se utilizó para conectar a ese usuario a la conferencia. También puede ver información sobre el rol del usuario en cada conferencia (por ejemplo, moderador o asistente). Quizás lo más importante, puede ver rápidamente qué usuarios se conectan satisfactoriamente y finalizan la conferencia y qué usuarios no pudieron conectarse satisfactoriamente ni finalizar la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-p101">The Conference Detail Report provides detailed information about all the users who participated in a conference. For example, you can see such information as the date and time that a user joined the conference, the date and time that the user left the conference, and the user agent of the endpoint that was used to connect that user to the conference. You can also see information the user's role in each conference (for example, Presenter or Attendee). Perhaps most important, you get quickly see which users successfully join and complete the conference, and which users were not able to successfully join and complete the conference.</span></span>

<div>

## <a name="accessing-the-conference-detail-report"></a><span data-ttu-id="4f634-110">Acceso al Informe de detalles de conferencia</span><span class="sxs-lookup"><span data-stu-id="4f634-110">Accessing the Conference Detail Report</span></span>

<span data-ttu-id="4f634-111">Es posible obtener acceso al Informe de detalles de conferencia a partir de los siguientes informes:</span><span class="sxs-lookup"><span data-stu-id="4f634-111">The Conference Detail Report can be accessed from the following reports:</span></span>

  - <span data-ttu-id="4f634-112">El [Informe de control de admisión de llamadas en Lync Server 2013](lync-server-2013-call-admission-control-report.md) (al hacer clic en la métrica de detalle de una conferencia)</span><span class="sxs-lookup"><span data-stu-id="4f634-112">The [Call Admission Control Report in Lync Server 2013](lync-server-2013-call-admission-control-report.md) (by clicking the Detail metric for a conference)</span></span>

  - <span data-ttu-id="4f634-113">El [informe lista de errores de Lync Server 2013](lync-server-2013-failure-list-report.md) (al hacer clic en la métrica de la Conferencia)</span><span class="sxs-lookup"><span data-stu-id="4f634-113">The [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md) (by clicking the Conference metric)</span></span>

  - <span data-ttu-id="4f634-114">[Informe de actividad de usuario en Lync Server 2013](lync-server-2013-user-activity-report.md) (al hacer clic en la métrica de URI de la Conferencia)</span><span class="sxs-lookup"><span data-stu-id="4f634-114">The [User Activity Report in Lync Server 2013](lync-server-2013-user-activity-report.md) (by clicking the Conference URI metric)</span></span>

<span data-ttu-id="4f634-115">En el informe de detalles de la Conferencia, puede acceder al [Informe de diagnóstico en Lync Server 2013](lync-server-2013-diagnostic-report.md) haciendo clic en la métrica de informe de diagnóstico (detalles).</span><span class="sxs-lookup"><span data-stu-id="4f634-115">From the Conference Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Detail) metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="4f634-116">Filtros</span><span class="sxs-lookup"><span data-stu-id="4f634-116">Filters</span></span>

<span data-ttu-id="4f634-p102">Ninguno. No se puede filtrar el Informe de detalles de conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-p102">None. You cannot filter on the Conference Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="4f634-119">Métricas</span><span class="sxs-lookup"><span data-stu-id="4f634-119">Metrics</span></span>

<span data-ttu-id="4f634-120">La siguiente tabla muestra la información brindada en la sección Información de conferencia del Informe de detalles de conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-120">The following table lists the information provided in the Conference Information section of the Conference Detail Report.</span></span>

### <a name="conference-information-metrics"></a><span data-ttu-id="4f634-121">Métricas de Información de conferencia</span><span class="sxs-lookup"><span data-stu-id="4f634-121">Conference Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f634-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f634-122">Name</span></span></th>
<th><span data-ttu-id="4f634-123">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="4f634-123">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4f634-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f634-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f634-125"><strong>URI de conferencia</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-125"><strong>Conference URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-p103">URI asignado a la conferencia. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4f634-p103">URI assigned to the conference. For example:</span></span></p>
<p><span data-ttu-id="4f634-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span><span class="sxs-lookup"><span data-stu-id="4f634-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f634-129"><strong>FQDN del grupo de servidores</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-129"><strong>Pool FQDN</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-130">Nombre de dominio completo del grupo de registrador o servidor perimetral involucrado en una sesión.</span><span class="sxs-lookup"><span data-stu-id="4f634-130">Fully-qualified domain name of the Registrar pool or Edge Server involved in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f634-131"><strong>Hora de inicio</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-131"><strong>Start time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-132">Fecha y hora en que comenzó la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-132">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f634-133"><strong>Organizador</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-133"><strong>Organizer</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-134">Dirección SIP del usuario que organizó la conferencia</span><span class="sxs-lookup"><span data-stu-id="4f634-134">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f634-135"><strong>Hora de finalización</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-135"><strong>End time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-136">Fecha y hora en que la conferencia finalizó.</span><span class="sxs-lookup"><span data-stu-id="4f634-136">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f634-137">La siguiente tabla muestra la información brindada en la sección Participación de conferencia del Informe de detalles de conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-137">The following table lists the information provided in the Conference Participation Section of the Conference Detail Report.</span></span>

### <a name="conference-participation-metrics"></a><span data-ttu-id="4f634-138">Métricas de Participación de conferencia</span><span class="sxs-lookup"><span data-stu-id="4f634-138">Conference Participation Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f634-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f634-139">Name</span></span></th>
<th><span data-ttu-id="4f634-140">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="4f634-140">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4f634-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f634-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f634-142"><strong>Usuario</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-142"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-143">Dirección SIP del usuario que participó en la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-143">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f634-144"><strong>Rol</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-144"><strong>Role</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-145">Rol (por ejemplo, Moderador) que ocupó el participante de la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-145">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f634-146"><strong>Conectividad</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-146"><strong>Connectivity</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-147">Conectividad de red (normalmente Desde conexión interna o Desde conexión externa) del participante.</span><span class="sxs-lookup"><span data-stu-id="4f634-147">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f634-148">Hora de conexión</span><span class="sxs-lookup"><span data-stu-id="4f634-148">Join time</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-149">Fecha y hora en que el participante se unió a la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-149">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f634-150"><strong>Hora de desconexión</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-150"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-151">Fecha y hora en que el participante abandonó la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-151">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f634-152"><strong>Agente de usuario</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-152"><strong>User agent</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-153">Identificador del software del extremo del participante.</span><span class="sxs-lookup"><span data-stu-id="4f634-153">Identifier for the software used by the participant’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f634-154"><strong>Informes de diagnósticos</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-154"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-p104">Proporciona información de diagnóstico y resolución de problemas. Por ejemplo, códigos de respuesta SIP, encabezados de diagnóstico, horarios de conexión a conferencias e identificadores de diagnóstico para sesiones fallidas.</span><span class="sxs-lookup"><span data-stu-id="4f634-p104">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f634-157">En la tabla siguiente se enumera la información proporcionada en la sección modalidades de conferencia del informe detalles de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-157">The following table lists the information provided in the Conference Modalities section of the Conference Detail Report.</span></span>

### <a name="conference-modalities-metrics"></a><span data-ttu-id="4f634-158">Métricas de Modalidades de conferencia</span><span class="sxs-lookup"><span data-stu-id="4f634-158">Conference Modalities Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f634-159">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f634-159">Name</span></span></th>
<th><span data-ttu-id="4f634-160">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="4f634-160">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4f634-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f634-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f634-162"><strong>Usuario</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-162"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-163">Dirección SIP del usuario que participó en la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-163">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f634-164"><strong>Hora de conexión</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-164"><strong>Join time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-165">Fecha y hora en que el participante se unió a la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-165">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f634-166"><strong>Hora de desconexión</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-166"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-167">Fecha y hora en que un participante abandonó la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-167">Date and time that a participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f634-168"><strong>URI del servidor de conferencia</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-168"><strong>Conferencing server URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-169">URI para el servidor de conferencia utilizado en la conferencia.</span><span class="sxs-lookup"><span data-stu-id="4f634-169">URI for the Conferencing server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f634-170"><strong>Informes de diagnósticos</strong></span><span class="sxs-lookup"><span data-stu-id="4f634-170"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4f634-p105">Proporciona información de diagnóstico y resolución de problemas. Por ejemplo, códigos de respuesta SIP, encabezados de diagnóstico, horarios de conexión a conferencias e identificadores de diagnóstico para sesiones fallidas.</span><span class="sxs-lookup"><span data-stu-id="4f634-p105">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4f634-173">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4f634-173">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

