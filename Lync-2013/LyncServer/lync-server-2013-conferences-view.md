---
title: 'Lync Server 2013: vista conferencias'
description: 'Lync Server 2013: vista conferencias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences view
ms:assetid: c0e5c4db-c135-401f-9296-e9a49f6499a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721871(v=OCS.15)
ms:contentKeyID: 49733803
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee7fbb7c839c351fc9c81716a5800a678980549
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434427"
---
# <a name="conferences-view-in-lync-server-2013"></a><span data-ttu-id="543c8-103">Vista conferencias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="543c8-103">Conferences view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="543c8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="543c8-104">

<span> </span></span></span>

<span data-ttu-id="543c8-105">_**Última modificación del tema:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="543c8-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="543c8-106">La vista conferencias almacena información sobre las conferencias.</span><span class="sxs-lookup"><span data-stu-id="543c8-106">The Conferences View stores information about the conferences.</span></span> <span data-ttu-id="543c8-107">Esta vista se presentó en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="543c8-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="543c8-108">Columna</span><span class="sxs-lookup"><span data-stu-id="543c8-108">Column</span></span></th>
<th><span data-ttu-id="543c8-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="543c8-109">Data Type</span></span></th>
<th><span data-ttu-id="543c8-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="543c8-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="543c8-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-112">datetime</span><span class="sxs-lookup"><span data-stu-id="543c8-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="543c8-113">Hora de la solicitud de sesión.</span><span class="sxs-lookup"><span data-stu-id="543c8-113">Time of session request.</span></span> <span data-ttu-id="543c8-114">Se usa en conjunción con SessionIdSeq para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="543c8-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="543c8-115">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="543c8-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="543c8-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-117">int</span><span class="sxs-lookup"><span data-stu-id="543c8-117">int</span></span></p></td>
<td><p><span data-ttu-id="543c8-118">Número de identificación para identificar la sesión.</span><span class="sxs-lookup"><span data-stu-id="543c8-118">ID number to identify the session.</span></span> <span data-ttu-id="543c8-119">Se usa en conjunción con SessionIdTime para identificar de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="543c8-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="543c8-120">Para obtener más información, vea la <a href="lync-server-2013-dialogs-table.md">tabla cuadros de diálogo en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="543c8-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="543c8-121"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-121"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-122">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="543c8-122">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="543c8-123">URI de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="543c8-123">URI for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="543c8-124"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-124"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="543c8-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="543c8-126">Tipo de URI de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="543c8-126">Type of the conference URI.</span></span> <span data-ttu-id="543c8-127">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="543c8-127">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="543c8-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-129">identificador</span><span class="sxs-lookup"><span data-stu-id="543c8-129">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="543c8-130">Se usa para conferencias periódicas.</span><span class="sxs-lookup"><span data-stu-id="543c8-130">Used for recurring conferences.</span></span> <span data-ttu-id="543c8-131">Cada instancia de una conferencia periódica tiene el mismo ConferenceUri pero un ConfInstance diferente.</span><span class="sxs-lookup"><span data-stu-id="543c8-131">Each instance of a recurring conference has the same ConferenceUri but a different ConfInstance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="543c8-132"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-132"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-133">datetime</span><span class="sxs-lookup"><span data-stu-id="543c8-133">datetime</span></span></p></td>
<td><p><span data-ttu-id="543c8-134">Hora de inicio de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="543c8-134">Starting time for the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="543c8-135"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-135"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-136">datetime</span><span class="sxs-lookup"><span data-stu-id="543c8-136">datetime</span></span></p></td>
<td><p><span data-ttu-id="543c8-137">Hora de finalización de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="543c8-137">Ending time for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="543c8-138"><strong>OrganizerUri</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-138"><strong>OrganizerUri</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="543c8-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="543c8-140">Identificador URI del usuario que organizó la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="543c8-140">URI of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="543c8-141"><strong>OrganizerType</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-141"><strong>OrganizerType</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="543c8-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="543c8-143">Tipo de URI del usuario que organizó la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="543c8-143">Type of URI of the user who organized the conference.</span></span> <span data-ttu-id="543c8-144">Para obtener más información, consulte la <a href="lync-server-2013-uritypes-table.md">tabla UriTypes en Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="543c8-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="543c8-145"><strong>OrganizerTenant</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-145"><strong>OrganizerTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-146">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="543c8-146">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="543c8-147">Espacio empresarial del usuario que organizó la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="543c8-147">Tenant of the user who organized the conference.</span></span> <span data-ttu-id="543c8-148">Para obtener más información, consulte la <a href="lync-server-2013-tenants-table.md">tabla de inquilinos de Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="543c8-148">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="543c8-149"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-149"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="543c8-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="543c8-151">Nombre de dominio completo del grupo que ha hospedado la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="543c8-151">Fully qualified domain name of the pool that hosted the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="543c8-152"><strong>Fdisableautoindexingonschemaupdate</strong></span><span class="sxs-lookup"><span data-stu-id="543c8-152"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="543c8-153">smallint</span><span class="sxs-lookup"><span data-stu-id="543c8-153">smallint</span></span></p></td>
<td><p><span data-ttu-id="543c8-154">Máscara de bits que contiene atributos de conferencia.</span><span class="sxs-lookup"><span data-stu-id="543c8-154">Bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="543c8-155">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="543c8-155">Possible values are:</span></span></p>
<p><span data-ttu-id="543c8-156">0X01: transacción sintética</span><span class="sxs-lookup"><span data-stu-id="543c8-156">0X01 – Synthetic Transaction</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="543c8-157">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="543c8-157">


</div>

<span> </span>

</div>

</div>

</span></span></div>

