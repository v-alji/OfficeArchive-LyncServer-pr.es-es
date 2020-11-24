---
title: 'Lync Server 2013: Tabla VoipDetails'
description: 'Lync Server 2013: tabla VoipDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoipDetails table
ms:assetid: 74ffbb71-569b-4018-be1f-4db2bbafcf36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398566(v=OCS.15)
ms:contentKeyID: 48184522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f23d991c1d577a15717de2572d744e1b65ba6bab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397889"
---
# <a name="voipdetails-table-in-lync-server-2013"></a><span data-ttu-id="a6acd-103">Tabla VoipDetails en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6acd-103">VoipDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6acd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6acd-104">

<span> </span></span></span>

<span data-ttu-id="a6acd-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="a6acd-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="a6acd-106">Cada registro representa una llamada de fiesta de 1 2 en la que al menos un usuario es un usuario de VoIP.</span><span class="sxs-lookup"><span data-stu-id="a6acd-106">Each record represents one two-party call in which at least one user is a VoIP user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6acd-107">Columna</span><span class="sxs-lookup"><span data-stu-id="a6acd-107">Column</span></span></th>
<th><span data-ttu-id="a6acd-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a6acd-108">Data Type</span></span></th>
<th><span data-ttu-id="a6acd-109">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="a6acd-109">Key/Index</span></span></th>
<th><span data-ttu-id="a6acd-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="a6acd-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6acd-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-112">datetime</span><span class="sxs-lookup"><span data-stu-id="a6acd-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="a6acd-113">Primary</span><span class="sxs-lookup"><span data-stu-id="a6acd-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="a6acd-114">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="a6acd-114">Time of session request.</span></span> <span data-ttu-id="a6acd-115">Se usa en conjunción con <strong>SessionIdSeq</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="a6acd-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="a6acd-116">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6acd-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-118">int</span><span class="sxs-lookup"><span data-stu-id="a6acd-118">int</span></span></p></td>
<td><p><span data-ttu-id="a6acd-119">Primary</span><span class="sxs-lookup"><span data-stu-id="a6acd-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="a6acd-120">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="a6acd-120">ID number to identify the session.</span></span> <span data-ttu-id="a6acd-121">Se usa en conjunción con <strong>SessionIdTime</strong> para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="a6acd-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="a6acd-122">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6acd-123"><strong>FromNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-123"><strong>FromNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-124">int</span><span class="sxs-lookup"><span data-stu-id="a6acd-124">int</span></span></p></td>
<td><p><span data-ttu-id="a6acd-125">Extranjero</span><span class="sxs-lookup"><span data-stu-id="a6acd-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6acd-126"><strong>PhoneId</strong> de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="a6acd-126"><strong>PhoneId</strong> of the caller.</span></span> <span data-ttu-id="a6acd-127">Para obtener más información, consulte la <a href="lync-server-2013-phones-table.md">tabla teléfonos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-127">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="a6acd-128">Si no es NULL y <strong>FromGatewayId</strong> no es null, la persona que llama era un usuario de la RTC.</span><span class="sxs-lookup"><span data-stu-id="a6acd-128">If not NULL and <strong>FromGatewayId</strong> is not NULL, then the caller was a PSTN user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6acd-129"><strong>ConnectedNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-129"><strong>ConnectedNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-130">int</span><span class="sxs-lookup"><span data-stu-id="a6acd-130">int</span></span></p></td>
<td><p><span data-ttu-id="a6acd-131">Extranjero</span><span class="sxs-lookup"><span data-stu-id="a6acd-131">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6acd-132"><strong>PhoneId</strong> del receptor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a6acd-132"><strong>PhoneId</strong> of the call receiver.</span></span> <span data-ttu-id="a6acd-133">Para obtener más información, consulte la <a href="lync-server-2013-phones-table.md">tabla teléfonos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-133">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="a6acd-134">Si no es NULL y <strong>ToGatewayId</strong> no es null, el receptor de la llamada fue un usuario de la RTC.</span><span class="sxs-lookup"><span data-stu-id="a6acd-134">If not NULL and <strong>ToGatewayId</strong> is not NULL, then the call receiver was a PSTN user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6acd-135"><strong>FromMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-135"><strong>FromMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-136">int</span><span class="sxs-lookup"><span data-stu-id="a6acd-136">int</span></span></p></td>
<td><p><span data-ttu-id="a6acd-137">Extranjero</span><span class="sxs-lookup"><span data-stu-id="a6acd-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6acd-138">El servidor de mediación del que procede la llamada.</span><span class="sxs-lookup"><span data-stu-id="a6acd-138">The Mediation Server the call is coming from.</span></span> <span data-ttu-id="a6acd-139">Para obtener más información, consulte la <a href="lync-server-2013-mediationservers-table.md">tabla MediationServers en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-139">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6acd-140"><strong>ToMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-140"><strong>ToMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-141">int</span><span class="sxs-lookup"><span data-stu-id="a6acd-141">int</span></span></p></td>
<td><p><span data-ttu-id="a6acd-142">Extranjero</span><span class="sxs-lookup"><span data-stu-id="a6acd-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6acd-143">El servidor de mediación llamado es el.</span><span class="sxs-lookup"><span data-stu-id="a6acd-143">The Mediation Server called is going to.</span></span> <span data-ttu-id="a6acd-144">Para obtener más información, consulte la <a href="lync-server-2013-mediationservers-table.md">tabla MediationServers en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-144">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6acd-145"><strong>FromGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-145"><strong>FromGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-146">int</span><span class="sxs-lookup"><span data-stu-id="a6acd-146">int</span></span></p></td>
<td><p><span data-ttu-id="a6acd-147">Extranjero</span><span class="sxs-lookup"><span data-stu-id="a6acd-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6acd-148">Puerta de enlace de la cual procede la llamada.</span><span class="sxs-lookup"><span data-stu-id="a6acd-148">Gateway the call is coming from.</span></span> <span data-ttu-id="a6acd-149">Para obtener más información, consulte la <a href="lync-server-2013-gateways-table.md">tabla de puertas de enlace en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-149">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6acd-150"><strong>ToGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-150"><strong>ToGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-151">int</span><span class="sxs-lookup"><span data-stu-id="a6acd-151">int</span></span></p></td>
<td><p><span data-ttu-id="a6acd-152">Extranjero</span><span class="sxs-lookup"><span data-stu-id="a6acd-152">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6acd-153">Puerta de enlace a la que va la llamada.</span><span class="sxs-lookup"><span data-stu-id="a6acd-153">Gateway the call is going to.</span></span> <span data-ttu-id="a6acd-154">Para obtener más información, consulte la <a href="lync-server-2013-gateways-table.md">tabla de puertas de enlace en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-154">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6acd-155"><strong>DisconnectedbyURIId</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-155"><strong>DisconnectedbyURIId</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-156">int</span><span class="sxs-lookup"><span data-stu-id="a6acd-156">int</span></span></p></td>
<td><p><span data-ttu-id="a6acd-157">Extranjero</span><span class="sxs-lookup"><span data-stu-id="a6acd-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6acd-158">URI del usuario que desconectó la llamada, si el usuario tiene un URI.</span><span class="sxs-lookup"><span data-stu-id="a6acd-158">URI of the user who disconnected the call, if the user has a URI.</span></span> <span data-ttu-id="a6acd-159">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-159">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6acd-160"><strong>DisconnectedbyPhoneId</strong></span><span class="sxs-lookup"><span data-stu-id="a6acd-160"><strong>DisconnectedbyPhoneId</strong></span></span></p></td>
<td><p><span data-ttu-id="a6acd-161">int</span><span class="sxs-lookup"><span data-stu-id="a6acd-161">int</span></span></p></td>
<td><p><span data-ttu-id="a6acd-162">Extranjero</span><span class="sxs-lookup"><span data-stu-id="a6acd-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6acd-163">El identificador del teléfono que desconectó la llamada se desconectó de un teléfono.</span><span class="sxs-lookup"><span data-stu-id="a6acd-163">ID of the phone that disconnected the call was disconnected from a phone.</span></span> <span data-ttu-id="a6acd-164">Para obtener más información, consulte la <a href="lync-server-2013-phones-table.md">tabla teléfonos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a6acd-164">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a6acd-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6acd-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

