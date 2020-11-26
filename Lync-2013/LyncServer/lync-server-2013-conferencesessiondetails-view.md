---
title: 'Lync Server 2013: vista ConferenceSessionDetails'
description: 'Lync Server 2013: vista ConferenceSessionDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails view
ms:assetid: 5858c84d-baed-421d-ad1d-3726e150e256
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688066(v=OCS.15)
ms:contentKeyID: 49733660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1c62f020413efecdbc0f909618256ccc7308d4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434399"
---
# <a name="conferencesessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="85107-103">Vista ConferenceSessionDetails en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85107-103">ConferenceSessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85107-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85107-104">

<span> </span></span></span>

<span data-ttu-id="85107-105">_**Última modificación del tema:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="85107-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="85107-106">La vista ConferenceSessionDetails almacena información sobre las sesiones de varias partes.</span><span class="sxs-lookup"><span data-stu-id="85107-106">The ConferenceSessionDetails view stores information about multiparty sessions.</span></span> <span data-ttu-id="85107-107">Cada registro representa una sesión de conferencia, que puede ser la sesión con el foco o la sesión con un servidor de conferencia específico.</span><span class="sxs-lookup"><span data-stu-id="85107-107">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span> <span data-ttu-id="85107-108">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85107-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85107-109">Columna</span><span class="sxs-lookup"><span data-stu-id="85107-109">Column</span></span></th>
<th><span data-ttu-id="85107-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="85107-110">Data Type</span></span></th>
<th><span data-ttu-id="85107-111">Detalles</span><span class="sxs-lookup"><span data-stu-id="85107-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85107-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="85107-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-113">datetime</span><span class="sxs-lookup"><span data-stu-id="85107-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="85107-114">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-114">Time of session request.</span></span> <span data-ttu-id="85107-115">Se usa en conjunción con SessionIdSeq para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-115">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="85107-116">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="85107-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-118">int</span><span class="sxs-lookup"><span data-stu-id="85107-118">int</span></span></p></td>
<td><p><span data-ttu-id="85107-119">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-119">ID number to identify the session.</span></span> <span data-ttu-id="85107-120">Se usa en conjunción con SessionIdTime para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-120">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="85107-121">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-122"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="85107-122"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-123">datetime</span><span class="sxs-lookup"><span data-stu-id="85107-123">datetime</span></span></p></td>
<td><p><span data-ttu-id="85107-124">Hora de la primera solicitud de invitación.</span><span class="sxs-lookup"><span data-stu-id="85107-124">Time of the first INVITE request.</span></span> <span data-ttu-id="85107-125">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-125">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="85107-126">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="85107-126">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-127"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="85107-127"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-128">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="85107-128">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="85107-129">URI de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="85107-129">URI of the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-130"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="85107-130"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-131">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-131">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-132">URI de tipo de conferencia.</span><span class="sxs-lookup"><span data-stu-id="85107-132">Type of conference URI.</span></span> <span data-ttu-id="85107-133">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-133">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-134"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="85107-134"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-135">identificador</span><span class="sxs-lookup"><span data-stu-id="85107-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="85107-136">Identificador que diferencia entre instancias de conferencias periódicas.</span><span class="sxs-lookup"><span data-stu-id="85107-136">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="85107-137">Cada instancia de conferencia periódica tiene el mismo ConferenceURI pero un valor diferente de ConfInstance.</span><span class="sxs-lookup"><span data-stu-id="85107-137">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-138"><strong>McuConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="85107-138"><strong>McuConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="85107-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="85107-140">URI del servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="85107-140">URI of the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-141"><strong>McuConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="85107-141"><strong>McuConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-143">Tipo de URI del servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="85107-143">Type of conferencing server URI.</span></span> <span data-ttu-id="85107-144">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-145"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="85107-145"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-146">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="85107-146">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="85107-147">URI del usuario implicado en la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-147">URI of the user involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-148"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="85107-148"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-149">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-149">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-150">Tipo de URI del usuario que formaba parte de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-150">Type of URI of the user whose was part of the session.</span></span> <span data-ttu-id="85107-151">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-151">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-152"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="85107-152"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-154">Espacio empresarial del usuario que formaba parte de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-154">Tenant of the user whose was part of the session.</span></span> <span data-ttu-id="85107-155">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-155">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-156"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="85107-156"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-157">identificador</span><span class="sxs-lookup"><span data-stu-id="85107-157">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="85107-158">Identificador único del usuario que forma parte de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-158">Unique identifier of the user whose was part of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-159"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="85107-159"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-160">datetime</span><span class="sxs-lookup"><span data-stu-id="85107-160">datetime</span></span></p></td>
<td><p><span data-ttu-id="85107-161">Hora de finalización de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-161">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-162"><strong>ConferenceClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="85107-162"><strong>ConferenceClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-163">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-163">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-164">Versión del servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="85107-164">Version of conference server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-165"><strong>ConferenceClientType</strong></span><span class="sxs-lookup"><span data-stu-id="85107-165"><strong>ConferenceClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-166">int</span><span class="sxs-lookup"><span data-stu-id="85107-166">int</span></span></p></td>
<td><p><span data-ttu-id="85107-167">Tipo de servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="85107-167">Type of conference server.</span></span> <span data-ttu-id="85107-168">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table.md">tabla UserAgentDef en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-168">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-169"><strong>ConferenceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="85107-169"><strong>ConferenceCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-170">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="85107-170">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="85107-171">Categoría servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="85107-171">Conference server category.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-172"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="85107-172"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-173">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-173">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-174">Versión del cliente utilizada por el usuario que participó en la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-174">Version of client used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-175"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="85107-175"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-176">int</span><span class="sxs-lookup"><span data-stu-id="85107-176">int</span></span></p></td>
<td><p><span data-ttu-id="85107-177">Cliente usado por el usuario que participó en la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-177">Client used by the user who participated in the session.</span></span> <span data-ttu-id="85107-178">Para obtener más información, consulte la <a href="lync-server-2013-useragentdef-table.md">tabla UserAgentDef en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-178">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-179"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="85107-179"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-180">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="85107-180">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="85107-181">Nombre de la categoría del cliente que ha usado el usuario que forma parte de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-181">Name of the category of the client used by the user who was part of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-182"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="85107-182"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-183">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="85107-183">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="85107-184">URI del usuario en cuyo nombre se inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-184">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-185"><strong>OnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="85107-185"><strong>OnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-186">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-186">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-187">Tipo de URI del usuario en cuyo nombre se inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-187">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="85107-188">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-188">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-189"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="85107-189"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-190">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-190">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-191">Inquilino del usuario cuyo en nombre se ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-191">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="85107-192">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-192">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-193"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="85107-193"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-194">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="85107-194">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="85107-195">Identificador URI del usuario que remitió la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-195">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-196"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="85107-196"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-197">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-197">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-198">Tipo de URI del usuario que ha remitido la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-198">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="85107-199">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-199">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-200"><strong>ReferredByUriTenant</strong></span><span class="sxs-lookup"><span data-stu-id="85107-200"><strong>ReferredByUriTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-201">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-201">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-202">Espacio empresarial del usuario que remitió la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-202">Tenant of the user who referred the session.</span></span> <span data-ttu-id="85107-203">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-203">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-204"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="85107-204"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-205">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="85107-205">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="85107-206">IDENTIFICACIÓN del cuadro de diálogo SIP.</span><span class="sxs-lookup"><span data-stu-id="85107-206">SIP dialog ID.</span></span> <span data-ttu-id="85107-207">El formato es</span><span class="sxs-lookup"><span data-stu-id="85107-207">The format is</span></span></p>
<p><span data-ttu-id="85107-208">:d ialog; de-etiqueta; to-Tag</span><span class="sxs-lookup"><span data-stu-id="85107-208">:dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-209"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="85107-209"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-210">datetime</span><span class="sxs-lookup"><span data-stu-id="85107-210">datetime</span></span></p></td>
<td><p><span data-ttu-id="85107-211">Número de identificación para identificar el cuadro de diálogo que se reemplazó por la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="85107-211">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="85107-212">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-212">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-213"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="85107-213"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-214">int</span><span class="sxs-lookup"><span data-stu-id="85107-214">int</span></span></p></td>
<td><p><span data-ttu-id="85107-215">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-215">ID number to identify the session.</span></span> <span data-ttu-id="85107-216">Se usa junto con ReplaceDialogIdTime para identificar de forma única una sesión que se reemplaza por esta sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-216">Used in conjunction with ReplaceDialogIdTime to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="85107-217">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="85107-217">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-218"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="85107-218"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-219">VARCHAR (775)</span><span class="sxs-lookup"><span data-stu-id="85107-219">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="85107-220">IDENTIFICACIÓN del cuadro de diálogo SIP que reemplaza la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-220">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="85107-221">El formato de es:</span><span class="sxs-lookup"><span data-stu-id="85107-221">The format of the is:</span></span></p>
<p><span data-ttu-id="85107-222">cuadro de diálogo; desde: etiqueta; to-Tag</span><span class="sxs-lookup"><span data-stu-id="85107-222">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-223"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="85107-223"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-224">bit</span><span class="sxs-lookup"><span data-stu-id="85107-224">bit</span></span></p></td>
<td><p><span data-ttu-id="85107-225">Indica si la sesión ha sido iniciada por el servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="85107-225">Indicates whether the session was started by the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-226"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="85107-226"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-227">bit</span><span class="sxs-lookup"><span data-stu-id="85107-227">bit</span></span></p></td>
<td><p><span data-ttu-id="85107-228">Indica si el servidor de conferencia finalizó la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-228">Indicates whether the session was ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-229"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="85107-229"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-230">bit</span><span class="sxs-lookup"><span data-stu-id="85107-230">bit</span></span></p></td>
<td><p><span data-ttu-id="85107-231">Indica si el usuario ha iniciado sesión en la red interna.</span><span class="sxs-lookup"><span data-stu-id="85107-231">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="85107-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-233">datetime</span><span class="sxs-lookup"><span data-stu-id="85107-233">datetime</span></span></p></td>
<td><p><span data-ttu-id="85107-234">Hora de la respuesta al primer mensaje de invitación.</span><span class="sxs-lookup"><span data-stu-id="85107-234">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="85107-235">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="85107-236">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="85107-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-237"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="85107-237"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-238">int</span><span class="sxs-lookup"><span data-stu-id="85107-238">int</span></span></p></td>
<td><p><span data-ttu-id="85107-239">Código de respuesta SIP a la invitación de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-239">SIP response code to the session invitation.</span></span> <span data-ttu-id="85107-240">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="85107-241">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="85107-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-242"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="85107-242"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-243">int</span><span class="sxs-lookup"><span data-stu-id="85107-243">int</span></span></p></td>
<td><p><span data-ttu-id="85107-244">IDENTIFICADOR de diagnóstico capturado de los encabezados de SIP de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-244">Diagnostic ID captured from session SIP headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-245"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="85107-245"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-246">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-246">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-247">Tipo de contenido de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-247">Content type for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-248"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="85107-248"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-249">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-249">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-250">FQDN del servidor front-end que capturó los datos para la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-250">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-251"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="85107-251"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-252">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-252">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-253">FQDN del grupo de servidores que ha capturado los datos de la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-253">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-254"><strong>MediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="85107-254"><strong>MediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-255">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-255">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-256">Servidor de mediación usado por el usuario que participó en la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-256">Mediation Server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-257"><strong>Puerta</strong></span><span class="sxs-lookup"><span data-stu-id="85107-257"><strong>Gateway</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-258">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-258">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-259">Puerta de enlace usada por el usuario que participó la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-259">Gateway used by the user who participated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-260"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="85107-260"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-261">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="85107-261">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="85107-262">FQDN del servidor perimetral usado por el usuario que participó en la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-262">FQDN of the Edge server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85107-263"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="85107-263"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-264">smallint</span><span class="sxs-lookup"><span data-stu-id="85107-264">smallint</span></span></p></td>
<td><p><span data-ttu-id="85107-265">Indica los atributos del usuario que participó en la sesión.</span><span class="sxs-lookup"><span data-stu-id="85107-265">Indicates the attributes of the user who participated in the session.</span></span> <span data-ttu-id="85107-266">Se permiten las siguientes definiciones de atributos:</span><span class="sxs-lookup"><span data-stu-id="85107-266">The following attribute definitions allowed:</span></span></p>
<p><span data-ttu-id="85107-267">0x01: integrado con un teléfono de escritorio</span><span class="sxs-lookup"><span data-stu-id="85107-267">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85107-268"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="85107-268"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="85107-269">smallint</span><span class="sxs-lookup"><span data-stu-id="85107-269">smallint</span></span></p></td>
<td><p><span data-ttu-id="85107-270">Indica los atributos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="85107-270">Indicates the call attributes.</span></span> <span data-ttu-id="85107-271">Se permiten las siguientes definiciones de atributo:</span><span class="sxs-lookup"><span data-stu-id="85107-271">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="85107-272">0x01-reintento Session0</span><span class="sxs-lookup"><span data-stu-id="85107-272">0x01 - Retried Session0</span></span></p>
<p><span data-ttu-id="85107-273">x02: una llamada realizada por el agente en nombre de un grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="85107-273">x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="85107-274">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85107-274">


</div>

<span> </span>

</div>

</div>

</span></span></div>

