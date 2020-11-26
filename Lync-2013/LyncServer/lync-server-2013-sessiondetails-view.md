---
title: 'Lync Server 2013: vista SessionDetails'
description: 'Lync Server 2013: vista SessionDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails view
ms:assetid: ea328c6f-cf22-48dd-8f7f-f1666c9148c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721924(v=OCS.15)
ms:contentKeyID: 49733859
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c9f657257e54389defb805919be61adbdecad74
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424033"
---
# <a name="sessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="d7267-103">Vista SessionDetails en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7267-103">SessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7267-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7267-104">

<span> </span></span></span>

<span data-ttu-id="d7267-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="d7267-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="d7267-106">La vista SessionDetails almacena información sobre sesiones de punto a punto, que pueden ser una llamada telefónica VoIP-VoIP, una sesión de mensajería instantánea de dos partes u otro tipo de sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-106">The SessionDetails view stores information about peer-to-peer sessions, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="d7267-107">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d7267-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7267-108">Columna</span><span class="sxs-lookup"><span data-stu-id="d7267-108">Column</span></span></th>
<th><span data-ttu-id="d7267-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d7267-109">Data Type</span></span></th>
<th><span data-ttu-id="d7267-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="d7267-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7267-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-112">datetime</span><span class="sxs-lookup"><span data-stu-id="d7267-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="d7267-113">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-113">Time of session request.</span></span> <span data-ttu-id="d7267-114">Se usa en conjunción con SessionIdSeq para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="d7267-115">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en</a> la tabla de 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d7267-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-117">int</span><span class="sxs-lookup"><span data-stu-id="d7267-117">int</span></span></p></td>
<td><p><span data-ttu-id="d7267-118">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-118">ID number to identify the session.</span></span> <span data-ttu-id="d7267-119">Se usa en conjunción con SessionIdTime para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="d7267-120">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-121"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-121"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-122">datetime</span><span class="sxs-lookup"><span data-stu-id="d7267-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="d7267-123">Hora de la primera solicitud de invitación.</span><span class="sxs-lookup"><span data-stu-id="d7267-123">Time of the first INVITE request.</span></span> <span data-ttu-id="d7267-124">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-124">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d7267-125">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="d7267-125">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="d7267-126">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-126">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d7267-127">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="d7267-127">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-128"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-128"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d7267-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d7267-130">Identificador URI del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-130">URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-131"><strong>ToUr</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-131"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-132">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d7267-132">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d7267-133">Identificador URI del usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-133">URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-134"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-134"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-136">Tipo de URI del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-136">Type of URI of the user who started the session.</span></span> <span data-ttu-id="d7267-137">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-137">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-140">Tipo de URI del usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-140">Type of URI of the user who joined the session.</span></span> <span data-ttu-id="d7267-141">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-141">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-142"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-142"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-143">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d7267-143">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d7267-144">Espacio empresarial del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-144">Tenant of the user who started the session.</span></span> <span data-ttu-id="d7267-145">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-146"><strong>ToTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-146"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-147">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-147">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-148">El inquilino del usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-148">The tenant of the user who joined the session.</span></span> <span data-ttu-id="d7267-149">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-149">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-150"><strong>FromEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-150"><strong>FromEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-151">identificador</span><span class="sxs-lookup"><span data-stu-id="d7267-151">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d7267-152">Identificador único del extremo del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-152">Unique identifier of the endpoint of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-153"><strong>ToEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-153"><strong>ToEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-154">identificador</span><span class="sxs-lookup"><span data-stu-id="d7267-154">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d7267-155">Identificador único del extremo del usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-155">Unique identifier of the endpoint of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-156"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-156"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-157">datetime</span><span class="sxs-lookup"><span data-stu-id="d7267-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="d7267-158">Hora de finalización de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-158">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-159"><strong>FromMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-159"><strong>FromMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-160">int</span><span class="sxs-lookup"><span data-stu-id="d7267-160">int</span></span></p></td>
<td><p><span data-ttu-id="d7267-161">Número de mensajes enviados por el usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-161">Number of messages sent by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-162"><strong>ToMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-162"><strong>ToMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-163">int</span><span class="sxs-lookup"><span data-stu-id="d7267-163">int</span></span></p></td>
<td><p><span data-ttu-id="d7267-164">Número de mensajes enviados por el usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-164">Number of messages sent by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-165"><strong>FromClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-165"><strong>FromClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-166">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-166">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-167">Versión del cliente usada por el usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-167">Version of client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-168"><strong>FromClientType</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-168"><strong>FromClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-169">int</span><span class="sxs-lookup"><span data-stu-id="d7267-169">int</span></span></p></td>
<td><p><span data-ttu-id="d7267-170">Cliente usado por el usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-170">Client used by the user who started the session.</span></span> <span data-ttu-id="d7267-171">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table.md">tabla UserAgentDef en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-171">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-172"><strong>FromClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-172"><strong>FromClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-173">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="d7267-173">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="d7267-174">Nombre de la categoría del cliente que ha usado el usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-174">Name of the category of the client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-175"><strong>ToClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-175"><strong>ToClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-176">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-176">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-177">Versión de cliente usada por el usuario que se unió a la sesión</span><span class="sxs-lookup"><span data-stu-id="d7267-177">Version of client used by the user who joined the session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-178"><strong>ToClientType</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-178"><strong>ToClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-179">int</span><span class="sxs-lookup"><span data-stu-id="d7267-179">int</span></span></p></td>
<td><p><span data-ttu-id="d7267-180">Cliente usado por el usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-180">Client used by the user who joined the session.</span></span> <span data-ttu-id="d7267-181">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table.md">tabla UserAgentDef en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-181">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-182"><strong>ToClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-182"><strong>ToClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-183">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="d7267-183">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="d7267-184">Nombre de la categoría del cliente que ha usado el usuario que se unió a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-184">Name of the category of the client used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-185"><strong>TargetUri</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-185"><strong>TargetUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-186">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d7267-186">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d7267-187">URI del usuario de destino de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-187">URI of the target user of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-188"><strong>TargetUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-188"><strong>TargetUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-189">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d7267-189">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d7267-190">Tipo de URI del usuario de destino de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-190">Type of URI of the target user for the session.</span></span> <span data-ttu-id="d7267-191">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-191">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-192"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-192"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-193">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d7267-193">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d7267-194">URI del usuario en cuyo nombre se inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-194">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-195"><strong>OnnnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-195"><strong>OnnnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-197">Tipo de URI del usuario en cuyo nombre se inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-197">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="d7267-198">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-198">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-199"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-199"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-201">Inquilino del usuario cuyo en nombre se ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-201">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="d7267-202">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-202">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-203"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-203"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-204">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d7267-204">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d7267-205">Identificador URI del usuario que remitió la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-205">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-206"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-206"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-207">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-207">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-208">Tipo de URI del usuario que ha remitido la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-208">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="d7267-209">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-209">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-210"><strong>ReferredByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-210"><strong>ReferredByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-211">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-211">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-212">Espacio empresarial del usuario que remitió la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-212">Tenant of the user who referred the session.</span></span> <span data-ttu-id="d7267-213">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-213">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-214"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-214"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-215">VARCHAR (775)</span><span class="sxs-lookup"><span data-stu-id="d7267-215">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="d7267-216">IDENTIFICACIÓN del cuadro de diálogo SIP.</span><span class="sxs-lookup"><span data-stu-id="d7267-216">SIP dialog ID.</span></span> <span data-ttu-id="d7267-217">El formato es:</span><span class="sxs-lookup"><span data-stu-id="d7267-217">The format is:</span></span></p>
<p><span data-ttu-id="d7267-218">cuadro de diálogo; desde: etiqueta; to-Tag</span><span class="sxs-lookup"><span data-stu-id="d7267-218">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-219"><strong>CorrelationId</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-219"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-220">identificador</span><span class="sxs-lookup"><span data-stu-id="d7267-220">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d7267-221">GUID que se usa para correlacionar varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="d7267-221">GUID used to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-222"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-222"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-223">datetime</span><span class="sxs-lookup"><span data-stu-id="d7267-223">datetime</span></span></p></td>
<td><p><span data-ttu-id="d7267-224">Hora del cuadro de diálogo que se ha sustituido por la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-224">Time of the dialog which was replaced by the session.</span></span> <span data-ttu-id="d7267-225">Se usa junto con ReplaceDialogIdSeq para identificar de forma exclusiva un cuadro de diálogo que se reemplaza por la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-225">Used in conjunction with ReplaceDialogIdSeq to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="d7267-226">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-226">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-227"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-227"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-228">int</span><span class="sxs-lookup"><span data-stu-id="d7267-228">int</span></span></p></td>
<td><p><span data-ttu-id="d7267-229">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-229">ID number to identify the session.</span></span> <span data-ttu-id="d7267-230">Se usa junto con ReplaceDialogIdTime para identificar de forma exclusiva un cuadro de diálogo que se reemplaza por la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-230">Used in conjunction with ReplaceDialogIdTime to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="d7267-231">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d7267-231">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-232"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-232"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-233">VARCHAR (775)</span><span class="sxs-lookup"><span data-stu-id="d7267-233">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="d7267-234">IDENTIFICACIÓN del cuadro de diálogo SIP que reemplaza la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-234">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="d7267-235">El formato es:</span><span class="sxs-lookup"><span data-stu-id="d7267-235">The format is:</span></span></p>
<p><span data-ttu-id="d7267-236">cuadro de diálogo; desde: etiqueta; to-Tag</span><span class="sxs-lookup"><span data-stu-id="d7267-236">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-237"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-237"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-238">datetime</span><span class="sxs-lookup"><span data-stu-id="d7267-238">datetime</span></span></p></td>
<td><p><span data-ttu-id="d7267-239">Hora de la respuesta al primer mensaje de invitación.</span><span class="sxs-lookup"><span data-stu-id="d7267-239">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="d7267-240">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d7267-241">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="d7267-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-242"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-242"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-243">int</span><span class="sxs-lookup"><span data-stu-id="d7267-243">int</span></span></p></td>
<td><p><span data-ttu-id="d7267-244">Código de respuesta SIP a la invitación de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-244">SIP response code to the session invitation.</span></span> <span data-ttu-id="d7267-245">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-245">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d7267-246">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="d7267-246">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-247"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-247"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-248">int</span><span class="sxs-lookup"><span data-stu-id="d7267-248">int</span></span></p></td>
<td><p><span data-ttu-id="d7267-249">IDENTIFICACIÓN de diagnóstico capturada de encabezados SIP.</span><span class="sxs-lookup"><span data-stu-id="d7267-249">Diagnostic ID captured from SIP headers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-250"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-250"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-251">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-251">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-252">Tipo de contenido de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-252">Type of content for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-253"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-253"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-254">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-254">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-255">FQDN del servidor front-end que capturó los datos para la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-255">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-256"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-256"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-257">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-257">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-258">FQDN del grupo de servidores que ha capturado los datos de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-258">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-259"><strong>FromEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-259"><strong>FromEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-260">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-260">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-261">FQDN del servidor perimetral usado por el usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-261">FQDN of the Edge server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-262"><strong>ToEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-262"><strong>ToEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-263">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-263">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-264">FQDN del servidor perimetral usado por el usuario que inició la sesión</span><span class="sxs-lookup"><span data-stu-id="d7267-264">FQDN of the Edge server used by the user who started the session</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-265"><strong>IsFromInternal</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-265"><strong>IsFromInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-266">bit</span><span class="sxs-lookup"><span data-stu-id="d7267-266">bit</span></span></p></td>
<td><p><span data-ttu-id="d7267-267">Indica si el usuario que inició la sesión inició sesión en la red interna.</span><span class="sxs-lookup"><span data-stu-id="d7267-267">Indicates whether the user who started the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-268"><strong>IsToInternal</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-268"><strong>IsToInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-269">bit</span><span class="sxs-lookup"><span data-stu-id="d7267-269">bit</span></span></p></td>
<td><p><span data-ttu-id="d7267-270">Indica si el usuario que se unió a la sesión ha iniciado sesión en la red interna.</span><span class="sxs-lookup"><span data-stu-id="d7267-270">Indicates whether the user who joined the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-271"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-271"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-272">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d7267-272">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d7267-273">Prioridad de la llamada de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-273">Call priority of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-274"><strong>FromUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-274"><strong>FromUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-275">smallint</span><span class="sxs-lookup"><span data-stu-id="d7267-275">smallint</span></span></p></td>
<td><p><span data-ttu-id="d7267-276">Indica los atributos del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-276">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="d7267-277">Se permiten las siguientes definiciones de atributo:</span><span class="sxs-lookup"><span data-stu-id="d7267-277">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d7267-278">0x01: integrado con un teléfono de escritorio</span><span class="sxs-lookup"><span data-stu-id="d7267-278">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-279"><strong>ToUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-279"><strong>ToUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-280">smallint</span><span class="sxs-lookup"><span data-stu-id="d7267-280">smallint</span></span></p></td>
<td><p><span data-ttu-id="d7267-281">Indica los atributos del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7267-281">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="d7267-282">Se permiten las siguientes definiciones de atributo:</span><span class="sxs-lookup"><span data-stu-id="d7267-282">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d7267-283">0x01: integrado con un teléfono de escritorio</span><span class="sxs-lookup"><span data-stu-id="d7267-283">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7267-284"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-284"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-285">smallint</span><span class="sxs-lookup"><span data-stu-id="d7267-285">smallint</span></span></p></td>
<td><p><span data-ttu-id="d7267-286">Indica los atributos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d7267-286">Indicates the call attributes.</span></span> <span data-ttu-id="d7267-287">Se permiten las siguientes definiciones de atributo:</span><span class="sxs-lookup"><span data-stu-id="d7267-287">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d7267-288">0x01-reintento de sesión</span><span class="sxs-lookup"><span data-stu-id="d7267-288">0x01 - Retried Session</span></span></p>
<p><span data-ttu-id="d7267-289">0x02: una llamada realizada por el agente en nombre de un grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="d7267-289">0x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7267-290"><strong>Ubicación</strong></span><span class="sxs-lookup"><span data-stu-id="d7267-290"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="d7267-291">VARCHAR (Max)</span><span class="sxs-lookup"><span data-stu-id="d7267-291">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="d7267-292">Ubicación de la llamada de emergencia.</span><span class="sxs-lookup"><span data-stu-id="d7267-292">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d7267-293">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7267-293">


</div>

<span> </span>

</div>

</div>

</span></span></div>

