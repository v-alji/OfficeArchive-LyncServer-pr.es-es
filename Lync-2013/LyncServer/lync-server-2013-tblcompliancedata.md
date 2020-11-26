---
title: 'Lync Server 2013: tblComplianceData'
description: 'Lync Server 2013: tblComplianceData'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceData
ms:assetid: 05b28f9b-4aba-4b69-ba8d-2ceeb6cbfaac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558606(v=OCS.15)
ms:contentKeyID: 48183308
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c597d67054303de2753182b37419f68051d3af8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444479"
---
# <a name="tblcompliancedata-in-lync-server-2013"></a><span data-ttu-id="26244-103">tblComplianceData en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26244-103">tblComplianceData in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26244-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26244-104">

<span> </span></span></span>

<span data-ttu-id="26244-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="26244-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="26244-106">tblComplianceData contiene los eventos de conformidad que aún no ha procesado el adaptador de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="26244-106">tblComplianceData contains the compliance events that have not been processed by the compliance adapter yet.</span></span>

### <a name="columns"></a><span data-ttu-id="26244-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="26244-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26244-108">Columna</span><span class="sxs-lookup"><span data-stu-id="26244-108">Column</span></span></th>
<th><span data-ttu-id="26244-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="26244-109">Type</span></span></th>
<th><span data-ttu-id="26244-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="26244-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26244-111">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="26244-111">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="26244-112">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="26244-112">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="26244-113">IDENTIFICADOR de evento.</span><span class="sxs-lookup"><span data-stu-id="26244-113">Event ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26244-114">entryDate</span><span class="sxs-lookup"><span data-stu-id="26244-114">entryDate</span></span></p></td>
<td><p><span data-ttu-id="26244-115">smalldatetime, not null</span><span class="sxs-lookup"><span data-stu-id="26244-115">smalldatetime, not null</span></span></p></td>
<td><p><span data-ttu-id="26244-116">Hora de inserción (puede ser muy próxima para cmplType = 9 porque la entrada es solo un marcador de posición en ese caso).</span><span class="sxs-lookup"><span data-stu-id="26244-116">Time of insertion (may be far in the future for cmplType=9 because the entry is just a placeholder in that case).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26244-117">cmplType</span><span class="sxs-lookup"><span data-stu-id="26244-117">cmplType</span></span></p></td>
<td><p><span data-ttu-id="26244-118">int, not null</span><span class="sxs-lookup"><span data-stu-id="26244-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="26244-119">Tipo de evento de conformidad:</span><span class="sxs-lookup"><span data-stu-id="26244-119">Type of compliance event:</span></span></p>
<ul>
<li><p><span data-ttu-id="26244-120">1: chatear</span><span class="sxs-lookup"><span data-stu-id="26244-120">1: Chat</span></span></p></li>
<li><p><span data-ttu-id="26244-121">2: chatear</span><span class="sxs-lookup"><span data-stu-id="26244-121">2: Backchat</span></span></p></li>
<li><p><span data-ttu-id="26244-122">3: descarga de archivos</span><span class="sxs-lookup"><span data-stu-id="26244-122">3: File download</span></span></p></li>
<li><p><span data-ttu-id="26244-123">4: carga de archivos</span><span class="sxs-lookup"><span data-stu-id="26244-123">4: File upload</span></span></p></li>
<li><p><span data-ttu-id="26244-124">9: transferencia provisional de archivos</span><span class="sxs-lookup"><span data-stu-id="26244-124">9: Provisional file transfer</span></span></p></li>
<li><p><span data-ttu-id="26244-125">10: eliminación de chat (con Replace)</span><span class="sxs-lookup"><span data-stu-id="26244-125">10: Chat deletion (with replace)</span></span></p></li>
<li><p><span data-ttu-id="26244-126">11: purgado de chat</span><span class="sxs-lookup"><span data-stu-id="26244-126">11: Chat purging</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26244-127">cmplTime</span><span class="sxs-lookup"><span data-stu-id="26244-127">cmplTime</span></span></p></td>
<td><p><span data-ttu-id="26244-128">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="26244-128">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="26244-129">Marca de tiempo del evento.</span><span class="sxs-lookup"><span data-stu-id="26244-129">Time stamp for the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26244-130">cmplChannelUri</span><span class="sxs-lookup"><span data-stu-id="26244-130">cmplChannelUri</span></span></p></td>
<td><p><span data-ttu-id="26244-131">nvarchar (255), not null</span><span class="sxs-lookup"><span data-stu-id="26244-131">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="26244-132">Identificador uniforme de recursos (URI) del canal.</span><span class="sxs-lookup"><span data-stu-id="26244-132">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26244-133">cmplChatID</span><span class="sxs-lookup"><span data-stu-id="26244-133">cmplChatID</span></span></p></td>
<td><p><span data-ttu-id="26244-134">BIGINT</span><span class="sxs-lookup"><span data-stu-id="26244-134">bigint</span></span></p></td>
<td><p><span data-ttu-id="26244-135">IDENTIFICADOR de chat (corresponde a la tabla tblChat. chatId).</span><span class="sxs-lookup"><span data-stu-id="26244-135">Chat ID (corresponding to tblChat.chatId table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26244-136">cmplUserID</span><span class="sxs-lookup"><span data-stu-id="26244-136">cmplUserID</span></span></p></td>
<td><p><span data-ttu-id="26244-137">int, not null</span><span class="sxs-lookup"><span data-stu-id="26244-137">int, not null</span></span></p></td>
<td><p><span data-ttu-id="26244-138">IDENTIFICADOR principal del póster (correspondiente a la tabla tblPrincipal. prinID).</span><span class="sxs-lookup"><span data-stu-id="26244-138">Principal ID of the poster (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26244-139">cmplUserUri</span><span class="sxs-lookup"><span data-stu-id="26244-139">cmplUserUri</span></span></p></td>
<td><p><span data-ttu-id="26244-140">nvarchar (255), not null</span><span class="sxs-lookup"><span data-stu-id="26244-140">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="26244-141">URI de usuario.</span><span class="sxs-lookup"><span data-stu-id="26244-141">User URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26244-142">cmplMessage</span><span class="sxs-lookup"><span data-stu-id="26244-142">cmplMessage</span></span></p></td>
<td><p><span data-ttu-id="26244-143">nvarchar (Max)</span><span class="sxs-lookup"><span data-stu-id="26244-143">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="26244-144">Mensaje (la codificación depende de cmplType).</span><span class="sxs-lookup"><span data-stu-id="26244-144">Message (encoding depends on cmplType).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="26244-145">Clave</span><span class="sxs-lookup"><span data-stu-id="26244-145">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26244-146">Columna</span><span class="sxs-lookup"><span data-stu-id="26244-146">Column</span></span></th>
<th><span data-ttu-id="26244-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="26244-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26244-148">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="26244-148">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="26244-149">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="26244-149">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="26244-150">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26244-150">


</div>

<span> </span>

</div>

</div>

</span></span></div>

