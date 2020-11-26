---
title: 'Lync Server 2013: informe de diagnóstico'
description: 'Lync Server 2013: informe de diagnóstico.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Diagnostic Report
ms:assetid: b389dbd9-f2e8-4184-93d0-2e504796ac16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615445(v=OCS.15)
ms:contentKeyID: 48185159
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 198b836437285b464ba9172e59c9a60ed0a53b65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429307"
---
# <a name="diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="c8b44-103">Informe de diagnóstico en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8b44-103">Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c8b44-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c8b44-104">

<span> </span></span></span>

<span data-ttu-id="c8b44-105">_**Última modificación del tema:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="c8b44-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="c8b44-106">El informe de diagnóstico ofrece información de diagnóstico y solución de problemas para las sesiones con errores.</span><span class="sxs-lookup"><span data-stu-id="c8b44-106">The Diagnostic Report provides diagnostic and troubleshooting information for a failed session.</span></span> <span data-ttu-id="c8b44-107">Esta información incluye el identificador de diagnóstico y el encabezado de diagnóstico que se notificaron cuando se produjo el error en la sesión.</span><span class="sxs-lookup"><span data-stu-id="c8b44-107">This information includes both the Diagnostic ID and the Diagnostic header that were reported when the session failed.</span></span> <span data-ttu-id="c8b44-108">El identificador de diagnóstico es un identificador único (con formato de encabezado ms-diagnostics) que se adjunta a un mensaje SIP, mientras que el encabezado de diagnóstico proporciona una descripción que acompaña al identificador de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="c8b44-108">The Diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) that gets attached to a SIP message, while the Diagnostic header provides an accompanying description for the Diagnostic ID.</span></span> <span data-ttu-id="c8b44-109">El informe también puede contener detalles valiosos sobre la solución de problemas conocidos por el componente del informe.</span><span class="sxs-lookup"><span data-stu-id="c8b44-109">The report might also contain valuable troubleshooting details that are known by the reporting component.</span></span> <span data-ttu-id="c8b44-110">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c8b44-110">For example:</span></span>

  - <span data-ttu-id="c8b44-p102">El código de causa proporcionado por la puerta de enlace RTC que generó el error. Cuando una llamada saliente presenta errores en la red RTC, se genera automáticamente un código de causa ISUP (ISDN User Part). Por ejemplo, una puerta de enlace RTC puede enviar un código de causa 34 para indicar que no hay ningún canal o circuito disponible para completar la llamada.</span><span class="sxs-lookup"><span data-stu-id="c8b44-p102">The cause code provided by the PSTN gateway that generated the failure. When an outgoing call fails on the PSTN network, an ISDN User Part (ISUP) cause code is automatically generated. For example, a PSTN gateway might send cause code 34 to indicate that no circuit or channel was available for completing the call.</span></span>

  - <span data-ttu-id="c8b44-114">Errores de Winsock, puerto y FQDN del mismo nivel para detectar errores de conectividad.</span><span class="sxs-lookup"><span data-stu-id="c8b44-114">Peer FQDN, port, and Winsock errors for connectivity failures.</span></span>

  - <span data-ttu-id="c8b44-p103">Comprobación de nombres para detectar errores de resolución DNS. La resolución DNS tiene lugar cada vez que un cliente establece contacto con un servidor de nombres y solicita la dirección IP correspondiente al nombre de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c8b44-p103">Names being looked up for DNS resolution failures. DNS resolution takes place any time a client contacts a name server and requests the IP address that corresponds to specified device name.</span></span>

<div>

## <a name="accessing-the-diagnostic-report"></a><span data-ttu-id="c8b44-117">Obtener acceso al informe de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c8b44-117">Accessing the Diagnostic Report</span></span>

<span data-ttu-id="c8b44-118">Para acceder al informe de diagnóstico, haga clic en la métrica informe de diagnóstico (detalles) en el [informe detallado de sesión de punto a punto de Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) o en el informe detalles de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="c8b44-118">The Diagnostic Report can be accessed by clicking the Diagnostic Report (Detail) metric on either the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) or the Conference Detail Report.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="c8b44-119">Filtros</span><span class="sxs-lookup"><span data-stu-id="c8b44-119">Filters</span></span>

<span data-ttu-id="c8b44-p104">Ninguno. No se puede filtrar el informe de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="c8b44-p104">None. You cannot filter the Diagnostic Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="c8b44-122">Métricas</span><span class="sxs-lookup"><span data-stu-id="c8b44-122">Metrics</span></span>

<span data-ttu-id="c8b44-123">En la siguiente tabla se detalla la información proporcionada en el informe de diagnóstico para cada sesión.</span><span class="sxs-lookup"><span data-stu-id="c8b44-123">The following table lists the information provided in the Diagnostic Report for each session.</span></span>

### <a name="diagnostic-report-metrics"></a><span data-ttu-id="c8b44-124">Métricas del informe de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c8b44-124">Diagnostic Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c8b44-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="c8b44-125">Name</span></span></th>
<th><span data-ttu-id="c8b44-126">¿Se pueden ordenar los datos por este elemento?</span><span class="sxs-lookup"><span data-stu-id="c8b44-126">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c8b44-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8b44-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8b44-128"><strong>Hora del informe</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-128"><strong>Report time</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-129">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-129">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-130">Fecha y hora en que se registró el informe.</span><span class="sxs-lookup"><span data-stu-id="c8b44-130">Date and time that the report was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b44-131"><strong>Código de respuesta</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-131"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-132">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-132">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-133">Código de respuesta SIP enviado cuando se produjo un error en la sesión.</span><span class="sxs-lookup"><span data-stu-id="c8b44-133">SIP response code sent when the session failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8b44-134"><strong>Tipo de solicitud</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-134"><strong>Request type</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-135">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-135">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-p105">Tipo de solicitud SIP que presentó errores. Por ejemplo, INVITE, BYE o SERVICE.</span><span class="sxs-lookup"><span data-stu-id="c8b44-p105">SIP request type that failed. For example, INVITE, BYE, or SERVICE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b44-138"><strong>Origen</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-138"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-139">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-139">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-140">Origen del error.</span><span class="sxs-lookup"><span data-stu-id="c8b44-140">Source of the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8b44-141"><strong>URI de remitente</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-141"><strong>From user URI</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-142">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-142">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-143">Dirección SIP del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="c8b44-143">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b44-144"><strong>Agente de remitente</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-144"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-145">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-145">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-146">Software usado por el extremo del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="c8b44-146">Software used by the endpoint of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8b44-147"><strong>Id. de diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-147"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-148">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-148">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-149">Identificador único (con formato de encabezado de ms-diagnostics) adjunto a un mensaje SIP que a menudo aporta información útil para solucionar errores.</span><span class="sxs-lookup"><span data-stu-id="c8b44-149">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b44-150"><strong>Tipo de contenido</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-150"><strong>Content type</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-151">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-151">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-p106">Tipo de contenido multimedia que presentó errores. Un ejemplo de tipo de contenido habitual es Application/sdp. Session Description Protocol (SDP) es un protocolo estándar de Internet que se usa para anuncios e invitaciones de sesiones, y otras formas de iniciar sesiones multimedia.</span><span class="sxs-lookup"><span data-stu-id="c8b44-p106">Type of media content that failed. For example, a common content type is Application/sdp. Session Description Protocol (SDP) is a standard Internet protocol used for session announcements, session invitations, and other forms of multimedia session initiation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8b44-155"><strong>Aplicación</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-155"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-156">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-156">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-157">Aplicación a la que corresponde el error.</span><span class="sxs-lookup"><span data-stu-id="c8b44-157">Application involved in the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b44-158"><strong>URI de destinatario</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-158"><strong>To user URI</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-159">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-159">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-160">Dirección SIP del usuario invitado a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c8b44-160">SIP address of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8b44-161">Tiempo en unirse a conferencia (ms)</span><span class="sxs-lookup"><span data-stu-id="c8b44-161">Conference join times (ms)</span></span></p></td>
<td><p><span data-ttu-id="c8b44-162">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-162">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-163">Cantidad de tiempo (en milisegundos) que tardó el usuario en unirse a la conferencia.</span><span class="sxs-lookup"><span data-stu-id="c8b44-163">Amount of time (in milliseconds) it took for the user to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8b44-164"><strong>Encabezado de diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="c8b44-164"><strong>Diagnostic header</strong></span></span></p></td>
<td><p><span data-ttu-id="c8b44-165">No</span><span class="sxs-lookup"><span data-stu-id="c8b44-165">No</span></span></p></td>
<td><p><span data-ttu-id="c8b44-166">Descripción del identificador de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="c8b44-166">Diagnostic ID description.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8b44-167">Puede encontrar una lista de errores de diagnóstico en la [Página de encabezado de MS-Diagnostics](https://msdn.microsoft.com/library/gg132446\(v=office.12\).aspx).</span><span class="sxs-lookup"><span data-stu-id="c8b44-167">A list of diagnostic errors can be found on the [Ms-Diagnostics Header page](https://msdn.microsoft.com/library/gg132446\(v=office.12\).aspx).</span></span>

<span data-ttu-id="c8b44-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c8b44-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

