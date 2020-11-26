---
title: 'Lync Server 2013: Tabla ConferenceSessionDetails'
description: 'Lync Server 2013: tabla ConferenceSessionDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails table
ms:assetid: 9eae6a54-69fd-4966-aa17-7ecee1297ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412741(v=OCS.15)
ms:contentKeyID: 48184925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d101eb1607e366ab814e60acaeee80820fe87c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434420"
---
# <a name="conferencesessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="f22f0-103">Tabla ConferenceSessionDetails en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f22f0-103">ConferenceSessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f22f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f22f0-104">

<span> </span></span></span>

<span data-ttu-id="f22f0-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="f22f0-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="f22f0-106">Cada registro representa una sesión de conferencia, que puede ser la sesión con el foco o la sesión con un servidor de conferencia específico.</span><span class="sxs-lookup"><span data-stu-id="f22f0-106">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f22f0-107">Columna</span><span class="sxs-lookup"><span data-stu-id="f22f0-107">Column</span></span></th>
<th><span data-ttu-id="f22f0-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f22f0-108">Data Type</span></span></th>
<th><span data-ttu-id="f22f0-109">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="f22f0-109">Key/Index</span></span></th>
<th><span data-ttu-id="f22f0-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="f22f0-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-112">Fechas</span><span class="sxs-lookup"><span data-stu-id="f22f0-112">Datetime</span></span></p></td>
<td><p><span data-ttu-id="f22f0-113">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-114">Hora de la solicitud de sesión; se usa junto con <strong>SessionIdSeq</strong> para identificar de forma exclusiva una sesión de conferencia.</span><span class="sxs-lookup"><span data-stu-id="f22f0-114">Time of session request; used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="f22f0-115">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-117">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-117">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-118">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-119">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-119">ID number to identify the session.</span></span> <span data-ttu-id="f22f0-120">Se usa junto con <strong>SessionIdTime</strong> para identificar de forma exclusiva una sesión de conferencia.</span><span class="sxs-lookup"><span data-stu-id="f22f0-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="f22f0-121">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-122"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-122"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-123">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-123">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-124">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-125">Centrar el URI de conferencia relacionado con esta sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-125">Focus conference URI related to this session.</span></span> <span data-ttu-id="f22f0-126">Para obtener más información, consulte la <a href="lync-server-2013-conferenceuris-table.md">tabla ConferenceUris en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-126">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="f22f0-127">Este URI es un URI de conferencia basado en el foco.</span><span class="sxs-lookup"><span data-stu-id="f22f0-127">This URI is a Focus-based conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-129">Identificador</span><span class="sxs-lookup"><span data-stu-id="f22f0-129">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-130">Identificador que diferencia entre instancias de conferencias periódicas.</span><span class="sxs-lookup"><span data-stu-id="f22f0-130">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="f22f0-131">Cada instancia de conferencia periódica tiene el mismo ConferenceURI pero un valor diferente de ConfInstance.</span><span class="sxs-lookup"><span data-stu-id="f22f0-131">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p>
<p><span data-ttu-id="f22f0-132">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f22f0-132">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-133"><strong>McuConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-133"><strong>McuConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-134">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-134">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-135">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-135">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-136">URI de conferencia del servidor de conferencia relacionado con esta sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-136">Conferencing server conference URI related to this session.</span></span> <span data-ttu-id="f22f0-137">Para obtener más información, consulte la <a href="lync-server-2013-conferenceuris-table.md">tabla ConferenceUris en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-137">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="f22f0-138">Este URI es el URI de conferencia basado en el servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="f22f0-138">This URI is the conferencing server-based conference URI.</span></span> <span data-ttu-id="f22f0-139">Para sesiones de conferencia focalizadas, esta columna será nula.</span><span class="sxs-lookup"><span data-stu-id="f22f0-139">For Focus conference sessions, this column will be null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-140"><strong>Iddeusuario</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-140"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-141">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-141">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-142">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-143">IDENTIFICADOR de un usuario en la sesión de conferencia.</span><span class="sxs-lookup"><span data-stu-id="f22f0-143">ID of one user in the conference session.</span></span> <span data-ttu-id="f22f0-144">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-145"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-145"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-146">identificador</span><span class="sxs-lookup"><span data-stu-id="f22f0-146">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-147">Un GUID para identificar la instancia de Endpoint.</span><span class="sxs-lookup"><span data-stu-id="f22f0-147">A GUID to identify the instance of endpoint.</span></span> <span data-ttu-id="f22f0-148">Por ejemplo, si un usuario inicia sesión en diferentes equipos con la misma cuenta, cada equipo tendrá un identificador de extremo diferente.</span><span class="sxs-lookup"><span data-stu-id="f22f0-148">For example, if one user logs on to different machines with the same account, then each machine will have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-149"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-149"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-150">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-150">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-151">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-151">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-152">Indica el identificador del usuario de la persona que llama en nombre.</span><span class="sxs-lookup"><span data-stu-id="f22f0-152">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="f22f0-153">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-153">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-154"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-154"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-155">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-155">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-156">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-157">IDENTIFICADOR del usuario al que hace referencia la llamada.</span><span class="sxs-lookup"><span data-stu-id="f22f0-157">ID of the user by who the call is referred.</span></span> <span data-ttu-id="f22f0-158">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-158">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-159"><strong>UserClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-159"><strong>UserClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-160">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-160">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-161">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-162">Versión del cliente usada por el usuario de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="f22f0-162">Client version used by the conference user.</span></span> <span data-ttu-id="f22f0-163">Para obtener más información, consulte la <a href="lync-server-2013-clientversions-table.md">tabla ClientVersions en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-164"><strong>ConfClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-164"><strong>ConfClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-165">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-165">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-166">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-166">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-167">Versión de cliente usada por el servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="f22f0-167">Client version used by the conference server.</span></span> <span data-ttu-id="f22f0-168">Para obtener más información, consulte la <a href="lync-server-2013-clientversions-table.md">tabla ClientVersions en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-168">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-169"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-169"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-170">datetime</span><span class="sxs-lookup"><span data-stu-id="f22f0-170">datetime</span></span></p></td>
<td><p><span data-ttu-id="f22f0-171">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-171">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-172">Número de identificación para identificar el cuadro de diálogo que se reemplazó por la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="f22f0-172">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="f22f0-173">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-173">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-174"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-174"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-175">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-175">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-176">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-176">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-177">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-177">ID number to identify the session.</span></span> <span data-ttu-id="f22f0-178">Se usa junto con <strong>ReplacesDialogIdTime</strong> para identificar de forma única una sesión que se reemplaza por esta sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-178">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="f22f0-179">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-179">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-180"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-180"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-181">bit</span><span class="sxs-lookup"><span data-stu-id="f22f0-181">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-182">Indica si la sesión ha sido iniciada por el servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="f22f0-182">Indicates if the session started by the conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-183"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-183"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-184">bit</span><span class="sxs-lookup"><span data-stu-id="f22f0-184">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-185">Indica si la sesión finalizó por el servidor de conferencia.</span><span class="sxs-lookup"><span data-stu-id="f22f0-185">Indicates if the session ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-186"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-186"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-187">bit</span><span class="sxs-lookup"><span data-stu-id="f22f0-187">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-188">Si el usuario ha iniciado sesión en un interno o no.</span><span class="sxs-lookup"><span data-stu-id="f22f0-188">Whether user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-189"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-189"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-190">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-190">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-191">Código de respuesta del Protocolo de inicio de sesión (SIP) a la invitación de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-191">Session Initiation Protocol (SIP) response code to the session invitation.</span></span> <span data-ttu-id="f22f0-192">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-192">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="f22f0-193">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="f22f0-193">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-194"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-194"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-195">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-195">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-196">IDENTIFICACIÓN de diagnóstico capturada del encabezado de SIP.</span><span class="sxs-lookup"><span data-stu-id="f22f0-196">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-197"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-197"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-198">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-198">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-199">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-200">IDENTIFICADOR del servidor front-end usado para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-200">ID of the front-end server used for this session.</span></span> <span data-ttu-id="f22f0-201">Para obtener más información, consulte la <a href="lync-server-2013-servers-table.md">tabla servidores en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-201">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-202"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-202"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-203">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-203">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-204">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-204">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-205">IDENTIFICADOR del grupo en el que se capturó la sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-205">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="f22f0-206">Para obtener más información, consulte la <a href="lync-server-2013-pools-table.md">tabla de grupos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-206">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-207"><strong>MediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-207"><strong>MediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-208">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-208">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-209">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-209">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-210">El servidor de mediación que usa la llamada.</span><span class="sxs-lookup"><span data-stu-id="f22f0-210">The Mediation Server the call is using.</span></span> <span data-ttu-id="f22f0-211">Para obtener más información, consulte la <a href="lync-server-2013-mediationservers-table.md">tabla MediationServers en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-211">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-212"><strong>GatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-212"><strong>GatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-213">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-213">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-214">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-214">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-215">La puerta de enlace que usa la llamada.</span><span class="sxs-lookup"><span data-stu-id="f22f0-215">The gateway the call is using.</span></span> <span data-ttu-id="f22f0-216">Para obtener más información, consulte la <a href="lync-server-2013-gateways-table.md">tabla de puertas de enlace en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-216">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-217"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-217"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-218">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-218">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-219">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-220">El servidor perimetral que usa la llamada.</span><span class="sxs-lookup"><span data-stu-id="f22f0-220">The Edge Server the call is using.</span></span> <span data-ttu-id="f22f0-221">Para obtener más información, consulte la <a href="lync-server-2013-edgeservers-table.md">tabla EdgeServers en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-221">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-222"><strong>ContentTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-222"><strong>ContentTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-223">int</span><span class="sxs-lookup"><span data-stu-id="f22f0-223">int</span></span></p></td>
<td><p><span data-ttu-id="f22f0-224">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-224">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-225">Tipo de contenido usado en la sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-225">Content type used in the session.</span></span> <span data-ttu-id="f22f0-226">Para obtener más información, consulte la <a href="lync-server-2013-contenttypes-table.md">tabla contentTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f22f0-226">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-227"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-227"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-228">datetime</span><span class="sxs-lookup"><span data-stu-id="f22f0-228">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-229">La hora de la primera solicitud de invitación.</span><span class="sxs-lookup"><span data-stu-id="f22f0-229">The time of the first INVITE request.</span></span> <span data-ttu-id="f22f0-230">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-230">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="f22f0-231">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="f22f0-231">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-233">datetime</span><span class="sxs-lookup"><span data-stu-id="f22f0-233">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-234">Hora de la primera respuesta del SIP.</span><span class="sxs-lookup"><span data-stu-id="f22f0-234">Time of the first SIP RESPONSE.</span></span> <span data-ttu-id="f22f0-235">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="f22f0-236">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="f22f0-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-237"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-237"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-238">datetime</span><span class="sxs-lookup"><span data-stu-id="f22f0-238">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-239">La hora de finalización de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f22f0-239">The time when the session is ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-240"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-240"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-241">tinyint</span><span class="sxs-lookup"><span data-stu-id="f22f0-241">tinyint</span></span></p></td>
<td><p><span data-ttu-id="f22f0-242">Extranjero</span><span class="sxs-lookup"><span data-stu-id="f22f0-242">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f22f0-243">Contiene el valor de tipo URI de MCU de la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f22f0-243">Contains the MCU URI type value from the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a>.</span></span> <span data-ttu-id="f22f0-244">Este campo se usa para mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="f22f0-244">This field is used for improving query performance.</span></span></p>
<p><span data-ttu-id="f22f0-245">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f22f0-245">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22f0-246"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-246"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-247">smallint</span><span class="sxs-lookup"><span data-stu-id="f22f0-247">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-248">Un conjunto de bits que indica los atributos de usuario.</span><span class="sxs-lookup"><span data-stu-id="f22f0-248">A bit set that indicates the user attributes.</span></span> <span data-ttu-id="f22f0-249">Se muestran las siguientes definiciones de atributos:</span><span class="sxs-lookup"><span data-stu-id="f22f0-249">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="f22f0-250">Integrado con un teléfono de escritorio: 1</span><span class="sxs-lookup"><span data-stu-id="f22f0-250">Integrated with desktop phone - 1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22f0-251"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="f22f0-251"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="f22f0-252">smallint</span><span class="sxs-lookup"><span data-stu-id="f22f0-252">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f22f0-253">Un conjunto de bits que indica los atributos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f22f0-253">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="f22f0-254">Se muestran las siguientes definiciones de atributos:</span><span class="sxs-lookup"><span data-stu-id="f22f0-254">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="f22f0-255">Reintento de sesión: 1</span><span class="sxs-lookup"><span data-stu-id="f22f0-255">Retried Session - 1</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f22f0-256">\* Para la mayoría de las sesiones, SessionIdSeq tendrá el valor 1.</span><span class="sxs-lookup"><span data-stu-id="f22f0-256">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="f22f0-257">Si varias sesiones comienzan exactamente al mismo tiempo, la SessionIdSeq para una será 1, la otra será 2, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="f22f0-257">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="f22f0-258"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f22f0-258"></div>

<span> </span>

</div>

</div>

</span></span></div>

