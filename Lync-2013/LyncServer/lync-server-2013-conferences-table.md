---
title: 'Lync Server 2013: Tabla Conferences'
description: 'Lync Server 2013: tabla conferencias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences table
ms:assetid: c3da6271-b3c6-4898-894f-10456ec794d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412964(v=OCS.15)
ms:contentKeyID: 48185340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e0d8c61e795dc0c8f9843b871d7e4efd1bec571
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399383"
---
# <a name="conferences-table-in-lync-server-2013"></a><span data-ttu-id="4c718-103">Tabla Conferences en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c718-103">Conferences table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c718-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c718-104">

<span> </span></span></span>

<span data-ttu-id="4c718-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="4c718-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="4c718-106">Cada registro de esta tabla contiene detalles de llamadas sobre una conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-106">Each record in this table contains call details about one conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c718-107">Columna</span><span class="sxs-lookup"><span data-stu-id="4c718-107">Column</span></span></th>
<th><span data-ttu-id="4c718-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4c718-108">Data Type</span></span></th>
<th><span data-ttu-id="4c718-109">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="4c718-109">Key/Index</span></span></th>
<th><span data-ttu-id="4c718-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="4c718-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c718-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-112">datetime</span><span class="sxs-lookup"><span data-stu-id="4c718-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="4c718-113">Primary</span><span class="sxs-lookup"><span data-stu-id="4c718-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="4c718-114">Hora en que el agente CDR capturó la solicitud de conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-114">Time that the conference request was captured by the CDR agent.</span></span> <span data-ttu-id="4c718-115">Solo se usa como clave principal para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-115">Used only as a primary key to uniquely identify a conference instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c718-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-117">int</span><span class="sxs-lookup"><span data-stu-id="4c718-117">int</span></span></p></td>
<td><p><span data-ttu-id="4c718-118">Primary</span><span class="sxs-lookup"><span data-stu-id="4c718-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="4c718-119">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="4c718-119">ID number to identify the session.</span></span> <span data-ttu-id="4c718-120">Se usa junto con <strong>SessionIdTime</strong> para identificar de forma exclusiva una instancia de conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c718-121"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-121"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-122">int</span><span class="sxs-lookup"><span data-stu-id="4c718-122">int</span></span></p></td>
<td><p><span data-ttu-id="4c718-123">Extranjero</span><span class="sxs-lookup"><span data-stu-id="4c718-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="4c718-124">URI de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-124">Conference URI.</span></span> <span data-ttu-id="4c718-125">Para obtener más información, consulte la <a href="lync-server-2013-conferenceuris-table.md">tabla ConferenceUris en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4c718-125">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c718-126"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-126"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-127">identificador</span><span class="sxs-lookup"><span data-stu-id="4c718-127">uniqueidentifier</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4c718-128">Útil para las conferencias recurrentes; cada instancia de una conferencia periódica tiene el mismo <strong>ConferenceUri</strong>, pero tendrá un <strong>ConfInstance</strong>diferente.</span><span class="sxs-lookup"><span data-stu-id="4c718-128">Useful for recurring conferences; each instance of a recurring conference has the same <strong>ConferenceUri</strong>, but will have a different <strong>ConfInstance</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c718-129"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-129"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-130">datetime</span><span class="sxs-lookup"><span data-stu-id="4c718-130">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4c718-131">Hora de inicio de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-131">Conference start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c718-132"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-132"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-133">datetime</span><span class="sxs-lookup"><span data-stu-id="4c718-133">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4c718-134">Hora de inicio de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-134">Conference start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c718-135"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-135"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-136">int</span><span class="sxs-lookup"><span data-stu-id="4c718-136">int</span></span></p></td>
<td><p><span data-ttu-id="4c718-137">Extranjero</span><span class="sxs-lookup"><span data-stu-id="4c718-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="4c718-138">Número de identificación para identificar el grupo en el que se capturó la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-138">ID number to identify the pool in which the conference was captured.</span></span> <span data-ttu-id="4c718-139">Para obtener más información, consulte la <a href="lync-server-2013-pools-table.md">tabla de grupos en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4c718-139">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c718-140"><strong>OrganizerId</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-140"><strong>OrganizerId</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-141">ENT</span><span class="sxs-lookup"><span data-stu-id="4c718-141">Int</span></span></p></td>
<td><p><span data-ttu-id="4c718-142">Extranjero</span><span class="sxs-lookup"><span data-stu-id="4c718-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="4c718-143">Número de identificación para identificar el URI del organizador de esta conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-143">ID number to identify the organizer URI of this conference.</span></span> <span data-ttu-id="4c718-144">Para obtener más información, consulte la <a href="lync-server-2013-users-table.md">tabla usuarios en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4c718-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c718-145"><strong>Fdisableautoindexingonschemaupdate</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-145"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-146">smallint</span><span class="sxs-lookup"><span data-stu-id="4c718-146">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4c718-147">Máscara de bits que contiene atributos de conferencia.</span><span class="sxs-lookup"><span data-stu-id="4c718-147">A bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="4c718-148">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="4c718-148">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="4c718-149">0X01</span><span class="sxs-lookup"><span data-stu-id="4c718-149">0X01</span></span></p></li>
<li><p><span data-ttu-id="4c718-150">Sintética</span><span class="sxs-lookup"><span data-stu-id="4c718-150">Synthetic</span></span></p></li>
<li><p><span data-ttu-id="4c718-151">Transaccional</span><span class="sxs-lookup"><span data-stu-id="4c718-151">Transaction</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c718-152"><strong>Procesar</strong></span><span class="sxs-lookup"><span data-stu-id="4c718-152"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="4c718-153">bit</span><span class="sxs-lookup"><span data-stu-id="4c718-153">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4c718-154">Campo interno usado por el servicio de supervisión.</span><span class="sxs-lookup"><span data-stu-id="4c718-154">Internal field used by the Monitoring service.</span></span></p>
<p><span data-ttu-id="4c718-155">Este campo se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4c718-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4c718-156">\* Para la mayoría de las sesiones, SessionIdSeq tendrá el valor 1.</span><span class="sxs-lookup"><span data-stu-id="4c718-156">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="4c718-157">Si dos sesiones comienzan exactamente al mismo tiempo, la SessionIdSeq para uno será 1, y la otra será 2, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="4c718-157">If two sessions start at exactly the same time, the SessionIdSeq for one will be 1, and for the other will be 2, and so on.</span></span>

<span data-ttu-id="4c718-158"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c718-158"></div>

<span> </span>

</div>

</div>

</span></span></div>

