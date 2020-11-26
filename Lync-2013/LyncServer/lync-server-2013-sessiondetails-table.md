---
title: 'Lync Server 2013: Tabla SessionDetails'
description: 'Lync Server 2013: tabla SessionDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails table
ms:assetid: 783d2508-e31f-4b54-be0c-63aa5ec21c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398589(v=OCS.15)
ms:contentKeyID: 48184559
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd927f784fb0f2a835c896824105fe8bb112c7a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444780"
---
# <a name="sessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="be54a-103">Tabla SessionDetails en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be54a-103">SessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be54a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be54a-104">

<span> </span></span></span>

<span data-ttu-id="be54a-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="be54a-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="be54a-106">Cada registro representa una sesión de punto a punto, que puede ser una llamada telefónica VoIP-VoIP, una sesión de mensajería instantánea de dos partes u otro tipo de sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-106">Each record represents one peer-to-peer session, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="be54a-107">Puede realizar una combinación de tabla con la [tabla multimedia en Lync Server 2013](lync-server-2013-media-table.md) para buscar los detalles de cada elemento multimedia implicado en esta sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-107">You can perform a table join with the [Media table in Lync Server 2013](lync-server-2013-media-table.md) to find the details of each media involved in this session.</span></span>

<span data-ttu-id="be54a-108">Observe que los campos IsUser1IntegratedWithDeskPhone y IsUser2IntegratedWithDeskPhone se han quitado de la tabla SessionDetails que se usa en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="be54a-108">Note that the IsUser1IntegratedWithDeskPhone and the IsUser2IntegratedWithDeskPhone fields have been dropped from the SessionDetails table used in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be54a-109">Columna</span><span class="sxs-lookup"><span data-stu-id="be54a-109">Column</span></span></th>
<th><span data-ttu-id="be54a-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="be54a-110">Data Type</span></span></th>
<th><span data-ttu-id="be54a-111">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="be54a-111">Key/Index</span></span></th>
<th><span data-ttu-id="be54a-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="be54a-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be54a-113"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-113"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-114">datetime</span><span class="sxs-lookup"><span data-stu-id="be54a-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="be54a-115">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-116">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-116">Time of session request.</span></span> <span data-ttu-id="be54a-117">Se usa en conjunción con <strong>SessionIdSeq</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-117">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="be54a-118">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-118">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-119"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-119"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-120">int</span><span class="sxs-lookup"><span data-stu-id="be54a-120">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-121">Principal, extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-121">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-122">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-122">ID number to identify the session.</span></span> <span data-ttu-id="be54a-123">Se usa junto con <strong>SessionIdTime</strong> para identificar de forma única una sesión. \* para obtener más información, consulta la <a href="lync-server-2013-dialogs-table.md">tabla de cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-123">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.\* See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-124"><strong>CorrelationId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-124"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-125">identificador</span><span class="sxs-lookup"><span data-stu-id="be54a-125">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-126">Un GUID para correlacionar varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="be54a-126">A GUID to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-127"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-127"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-128">datetime</span><span class="sxs-lookup"><span data-stu-id="be54a-128">datetime</span></span></p></td>
<td><p><span data-ttu-id="be54a-129">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-130">Número de identificación para identificar el cuadro de diálogo que se reemplazó por la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="be54a-130">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="be54a-131">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-131">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-132"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-132"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-133">int</span><span class="sxs-lookup"><span data-stu-id="be54a-133">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-134">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-135">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-135">ID number to identify the session.</span></span> <span data-ttu-id="be54a-136">Se usa junto con <strong>ReplacesDialogIdTime</strong> para identificar de forma única una sesión que se reemplaza por esta sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-136">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="be54a-137">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-137">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-138"><strong>User1Id</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-138"><strong>User1Id</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-139">int</span><span class="sxs-lookup"><span data-stu-id="be54a-139">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-140">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-140">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-141">IDENTIFICADOR de un usuario de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-141">ID of one user in the session.</span></span> <span data-ttu-id="be54a-142">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-142">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-143"><strong>User2Id</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-143"><strong>User2Id</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-144">int</span><span class="sxs-lookup"><span data-stu-id="be54a-144">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-145">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-146">IDENTIFICADOR del otro usuario de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-146">ID of the other user in the session.</span></span> <span data-ttu-id="be54a-147">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-147">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-148"><strong>User1EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-148"><strong>User1EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-149">Identificador</span><span class="sxs-lookup"><span data-stu-id="be54a-149">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-150">GUID que identifica el extremo utilizado por el primer usuario de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-150">GUID that identifies the endpoint used by the first user in the session.</span></span></p>
<p><span data-ttu-id="be54a-151">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="be54a-151">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-152"><strong>User2EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-152"><strong>User2EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-153">Identificador</span><span class="sxs-lookup"><span data-stu-id="be54a-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-154">GUID que identifica el extremo usado por el segundo usuario de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-154">GUID that identifies the endpoint used by the second user in the session.</span></span></p>
<p><span data-ttu-id="be54a-155">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="be54a-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-156"><strong>TargetUserId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-156"><strong>TargetUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-157">int</span><span class="sxs-lookup"><span data-stu-id="be54a-157">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-158">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-158">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-159">El URI del usuario original para la solicitud SIP.</span><span class="sxs-lookup"><span data-stu-id="be54a-159">The original To user URI in the SIP request.</span></span> <span data-ttu-id="be54a-160">para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-160">see the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-161"><strong>SessionStartedById</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-161"><strong>SessionStartedById</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-162">int</span><span class="sxs-lookup"><span data-stu-id="be54a-162">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-163">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-164">IDENTIFICADOR del usuario que inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-164">ID of the user who started the session.</span></span> <span data-ttu-id="be54a-165">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-165">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-166"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-166"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-167">int</span><span class="sxs-lookup"><span data-stu-id="be54a-167">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-168">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-168">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-169">Indica el identificador del usuario de la persona que llama en nombre.</span><span class="sxs-lookup"><span data-stu-id="be54a-169">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="be54a-170">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-170">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-171"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-171"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-172">int</span><span class="sxs-lookup"><span data-stu-id="be54a-172">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-173">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-173">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-174">IDENTIFICADOR del usuario al que hace referencia la llamada.</span><span class="sxs-lookup"><span data-stu-id="be54a-174">ID of the user by who the call is referred.</span></span> <span data-ttu-id="be54a-175">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-175">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-176"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-176"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-177">int</span><span class="sxs-lookup"><span data-stu-id="be54a-177">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-178">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-178">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-179">IDENTIFICADOR del servidor front-end usado para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-179">ID of the front-end server used for this session.</span></span> <span data-ttu-id="be54a-180">Para obtener más información, consulte la <a href="lync-server-2013-servers-table.md">tabla servidores en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-180">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-181"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-181"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-182">int</span><span class="sxs-lookup"><span data-stu-id="be54a-182">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-183">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-183">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-184">IDENTIFICADOR del grupo en el que se capturó la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-184">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="be54a-185">Para obtener más información, consulte la <a href="lync-server-2013-pools-table.md">tabla de grupos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-185">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-186"><strong>ContentTypeID</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-186"><strong>ContentTypeID</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-187">int</span><span class="sxs-lookup"><span data-stu-id="be54a-187">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-188">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-189">Tipo de contenido usado en la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-189">Content type used in the session.</span></span> <span data-ttu-id="be54a-190">Para obtener más información, consulte la <a href="lync-server-2013-contenttypes-table.md">tabla contentTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-190">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-191"><strong>User1ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-191"><strong>User1ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-192">int</span><span class="sxs-lookup"><span data-stu-id="be54a-192">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-193">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-194">Versión de cliente usada por el usuario1.</span><span class="sxs-lookup"><span data-stu-id="be54a-194">Client version used by User1.</span></span> <span data-ttu-id="be54a-195">Para obtener más información, consulte la <a href="lync-server-2013-clientversions-table.md">tabla ClientVersions en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-195">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-196"><strong>User2ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-196"><strong>User2ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-197">int</span><span class="sxs-lookup"><span data-stu-id="be54a-197">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-198">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-198">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-199">Versión de cliente usada por usuario2.</span><span class="sxs-lookup"><span data-stu-id="be54a-199">Client version used by User2.</span></span> <span data-ttu-id="be54a-200">Para obtener más información, consulte la <a href="lync-server-2013-clientversions-table.md">tabla ClientVersions en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-200">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-201"><strong>User1EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-201"><strong>User1EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-202">int</span><span class="sxs-lookup"><span data-stu-id="be54a-202">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-203">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-203">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-204">Servidor perimetral usado por el usuario1.</span><span class="sxs-lookup"><span data-stu-id="be54a-204">Edge Server used by User1.</span></span> <span data-ttu-id="be54a-205">Para obtener más información, consulte la <a href="lync-server-2013-edgeservers-table.md">tabla EdgeServers en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-205">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-206"><strong>User2EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-206"><strong>User2EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-207">int</span><span class="sxs-lookup"><span data-stu-id="be54a-207">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-208">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-208">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-209">Servidor perimetral usado por usuario2.</span><span class="sxs-lookup"><span data-stu-id="be54a-209">Edge Server used by User2.</span></span> <span data-ttu-id="be54a-210">Para obtener más información, consulte la <a href="lync-server-2013-edgeservers-table.md">tabla EdgeServers en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-210">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-211"><strong>IsUser1Internal</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-211"><strong>IsUser1Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-212">bit</span><span class="sxs-lookup"><span data-stu-id="be54a-212">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-213">Si user1 está conectado desde interno o no.</span><span class="sxs-lookup"><span data-stu-id="be54a-213">Whether User1 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-214"><strong>IsUser2Internal</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-214"><strong>IsUser2Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-215">bit</span><span class="sxs-lookup"><span data-stu-id="be54a-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-216">Si usuario2 está conectado desde interno o no.</span><span class="sxs-lookup"><span data-stu-id="be54a-216">Whether User2 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-217"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-217"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-218">datetime</span><span class="sxs-lookup"><span data-stu-id="be54a-218">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-219">La hora de la primera solicitud de invitación.</span><span class="sxs-lookup"><span data-stu-id="be54a-219">The time of the first INVITE request.</span></span> <span data-ttu-id="be54a-220">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-220">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="be54a-221">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="be54a-221">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="be54a-222">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-222">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="be54a-223">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="be54a-223">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-224"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-224"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-225">datetime</span><span class="sxs-lookup"><span data-stu-id="be54a-225">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-226">La hora de la respuesta al primer mensaje de invitación.</span><span class="sxs-lookup"><span data-stu-id="be54a-226">The time of the response to the first INVITE message.</span></span> <span data-ttu-id="be54a-227">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-227">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="be54a-228">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="be54a-228">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-229"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-229"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-230">int</span><span class="sxs-lookup"><span data-stu-id="be54a-230">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-231">Código de respuesta SIP a la invitación de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-231">SIP response code to the session invitation.</span></span> <span data-ttu-id="be54a-232">Por lo general, este campo se rellena con los datos generados desde el mensaje de invitación inicial de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-232">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="be54a-233">Si no hay ningún mensaje de invitación, el campo se rellena con la fecha y la hora del primer mensaje SIP pertinente (BYE, cancelar, mensaje o información).</span><span class="sxs-lookup"><span data-stu-id="be54a-233">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-234"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-234"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-235">int</span><span class="sxs-lookup"><span data-stu-id="be54a-235">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-236">IDENTIFICACIÓN de diagnóstico capturada del encabezado de SIP.</span><span class="sxs-lookup"><span data-stu-id="be54a-236">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-237"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-237"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-238">int</span><span class="sxs-lookup"><span data-stu-id="be54a-238">int</span></span></p></td>
<td><p><span data-ttu-id="be54a-239">Extranjero</span><span class="sxs-lookup"><span data-stu-id="be54a-239">Foreign</span></span></p></td>
<td><p><span data-ttu-id="be54a-240">Prioridad de la llamada.</span><span class="sxs-lookup"><span data-stu-id="be54a-240">Call priority.</span></span> <span data-ttu-id="be54a-241">Para obtener más información, consulte la <a href="lync-server-2013-callpriorities-table.md">tabla CallPriorities en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="be54a-241">See the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-242"><strong>User1MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-242"><strong>User1MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-243">int</span><span class="sxs-lookup"><span data-stu-id="be54a-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-244">Número de mensajes enviados por el usuario1 durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-244">Number of messages sent by User1 during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-245"><strong>User2MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-245"><strong>User2MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-246">int</span><span class="sxs-lookup"><span data-stu-id="be54a-246">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-247">Número de mensajes enviados por usuario2 durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-247">Number of messages sent by User2 during the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-248"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-248"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-249">datetime</span><span class="sxs-lookup"><span data-stu-id="be54a-249">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-250">Hora de finalización de la sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-250">Time at the end of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-251"><strong>MediaTypes</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-251"><strong>MediaTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-252">int</span><span class="sxs-lookup"><span data-stu-id="be54a-252">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-253">Un conjunto de bits que indica el tipo de medio de esta sesión.</span><span class="sxs-lookup"><span data-stu-id="be54a-253">A bit set that indicates the media type of this session.</span></span> <span data-ttu-id="be54a-254">En la lista se muestran las definiciones de los tipos:</span><span class="sxs-lookup"><span data-stu-id="be54a-254">Listed are the definitions of the types:</span></span></p>
<h3 id="section-1"> </h3>
<div>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be54a-255">MI</span><span class="sxs-lookup"><span data-stu-id="be54a-255">IM</span></span></p></td>
<td><p><span data-ttu-id="be54a-256">1</span><span class="sxs-lookup"><span data-stu-id="be54a-256">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-257">FILE_TRANSFER</span><span class="sxs-lookup"><span data-stu-id="be54a-257">FILE_TRANSFER</span></span></p></td>
<td><p><span data-ttu-id="be54a-258">2</span><span class="sxs-lookup"><span data-stu-id="be54a-258">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-259">REMOTE_ASSISTANCE</span><span class="sxs-lookup"><span data-stu-id="be54a-259">REMOTE_ASSISTANCE</span></span></p></td>
<td><p><span data-ttu-id="be54a-260">4</span><span class="sxs-lookup"><span data-stu-id="be54a-260">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-261">APP_SHARING</span><span class="sxs-lookup"><span data-stu-id="be54a-261">APP_SHARING</span></span></p></td>
<td><p><span data-ttu-id="be54a-262">4,8</span><span class="sxs-lookup"><span data-stu-id="be54a-262">8</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-263">AUDIO</span><span class="sxs-lookup"><span data-stu-id="be54a-263">AUDIO</span></span></p></td>
<td><p><span data-ttu-id="be54a-264">apartado</span><span class="sxs-lookup"><span data-stu-id="be54a-264">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-265">CÁMARA</span><span class="sxs-lookup"><span data-stu-id="be54a-265">VIDEO</span></span></p></td>
<td><p><span data-ttu-id="be54a-266">32</span><span class="sxs-lookup"><span data-stu-id="be54a-266">32</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-267">APP_INVITE</span><span class="sxs-lookup"><span data-stu-id="be54a-267">APP_INVITE</span></span></p></td>
<td><p><span data-ttu-id="be54a-268">64</span><span class="sxs-lookup"><span data-stu-id="be54a-268">64</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-269"><strong>User1Flag</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-269"><strong>User1Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-270">smallint</span><span class="sxs-lookup"><span data-stu-id="be54a-270">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-271">Un conjunto de bits que indica los atributos del Usuario1.</span><span class="sxs-lookup"><span data-stu-id="be54a-271">A bit set that indicates the User1 attributes.</span></span> <span data-ttu-id="be54a-272">Se muestran las siguientes definiciones de atributos:</span><span class="sxs-lookup"><span data-stu-id="be54a-272">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="be54a-273">0x01: integrado con un teléfono de escritorio</span><span class="sxs-lookup"><span data-stu-id="be54a-273">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-274"><strong>User2Flag</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-274"><strong>User2Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-275">smallint</span><span class="sxs-lookup"><span data-stu-id="be54a-275">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-276">Un conjunto de bits que indica los atributos de usuario2.</span><span class="sxs-lookup"><span data-stu-id="be54a-276">A bit set that indicates the User2 attributes.</span></span> <span data-ttu-id="be54a-277">Se muestran las siguientes definiciones de atributos:</span><span class="sxs-lookup"><span data-stu-id="be54a-277">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="be54a-278">0x01: integrado con un teléfono de escritorio</span><span class="sxs-lookup"><span data-stu-id="be54a-278">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be54a-279"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-279"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-280">smallint</span><span class="sxs-lookup"><span data-stu-id="be54a-280">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-281">Un conjunto de bits que indica los atributos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="be54a-281">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="be54a-282">Se muestran las siguientes definiciones de atributos:</span><span class="sxs-lookup"><span data-stu-id="be54a-282">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="be54a-283">0x01-reintento de sesión</span><span class="sxs-lookup"><span data-stu-id="be54a-283">0x01 - Retried Session</span></span></p></li>
<li><p><span data-ttu-id="be54a-284">0x02: una llamada realizada por el agente en nombre de un grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="be54a-284">0x02 - A call made by agent on behalf of a response group</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be54a-285"><strong>Procesar</strong></span><span class="sxs-lookup"><span data-stu-id="be54a-285"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="be54a-286">bit</span><span class="sxs-lookup"><span data-stu-id="be54a-286">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be54a-287">Para uso interno del servicio de supervisión.</span><span class="sxs-lookup"><span data-stu-id="be54a-287">For internal use by the Monitoring service.</span></span></p>
<p><span data-ttu-id="be54a-288">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="be54a-288">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be54a-289">\* Para la mayoría de las sesiones, SessionIdSeq tendrá el valor 1.</span><span class="sxs-lookup"><span data-stu-id="be54a-289">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="be54a-290">Si varias sesiones comienzan exactamente al mismo tiempo, la SessionIdSeq para una será 1, la otra será 2, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="be54a-290">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="be54a-291"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be54a-291"></div>

<span> </span>

</div>

</div>

</span></span></div>

