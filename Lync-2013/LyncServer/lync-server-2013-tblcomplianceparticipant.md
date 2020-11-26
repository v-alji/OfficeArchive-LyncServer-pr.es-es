---
title: 'Lync Server 2013: tblComplianceParticipant'
description: 'Lync Server 2013: tblComplianceParticipant'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceParticipant
ms:assetid: 5d7e0dea-74f7-46d1-badf-b94abc8f066d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558655(v=OCS.15)
ms:contentKeyID: 48184262
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1385b0a635f003a72de93f10f72642314ad7ebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444458"
---
# <a name="tblcomplianceparticipant-in-lync-server-2013"></a><span data-ttu-id="b6b31-103">tblComplianceParticipant en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6b31-103">tblComplianceParticipant in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6b31-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6b31-104">

<span> </span></span></span>

<span data-ttu-id="b6b31-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="b6b31-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="b6b31-106">tblComplianceParticipant contiene los participantes actuales por canal y por servidor.</span><span class="sxs-lookup"><span data-stu-id="b6b31-106">tblComplianceParticipant contains the current participants per channel and per server.</span></span>

### <a name="columns"></a><span data-ttu-id="b6b31-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="b6b31-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6b31-108">Columna</span><span class="sxs-lookup"><span data-stu-id="b6b31-108">Column</span></span></th>
<th><span data-ttu-id="b6b31-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6b31-109">Type</span></span></th>
<th><span data-ttu-id="b6b31-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6b31-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6b31-111">channelUri</span><span class="sxs-lookup"><span data-stu-id="b6b31-111">channelUri</span></span></p></td>
<td><p><span data-ttu-id="b6b31-112">nvarchar (255), not null</span><span class="sxs-lookup"><span data-stu-id="b6b31-112">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="b6b31-113">Identificador uniforme de recursos (URI) del canal.</span><span class="sxs-lookup"><span data-stu-id="b6b31-113">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b31-114">Iddeusuario</span><span class="sxs-lookup"><span data-stu-id="b6b31-114">userId</span></span></p></td>
<td><p><span data-ttu-id="b6b31-115">int, not null</span><span class="sxs-lookup"><span data-stu-id="b6b31-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="b6b31-116">IDENTIFICADOR principal del participante (correspondiente a la tabla tblPrincipal. prinID).</span><span class="sxs-lookup"><span data-stu-id="b6b31-116">Principal ID of the participant (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b31-117">joinedAt</span><span class="sxs-lookup"><span data-stu-id="b6b31-117">joinedAt</span></span></p></td>
<td><p><span data-ttu-id="b6b31-118">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="b6b31-118">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="b6b31-119">Marca de tiempo del evento de Unión.</span><span class="sxs-lookup"><span data-stu-id="b6b31-119">Time stamp of the joining event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b31-120">partedAt</span><span class="sxs-lookup"><span data-stu-id="b6b31-120">partedAt</span></span></p></td>
<td><p><span data-ttu-id="b6b31-121">BIGINT</span><span class="sxs-lookup"><span data-stu-id="b6b31-121">bigint</span></span></p></td>
<td><p><span data-ttu-id="b6b31-122">NULL si el participante aún se ha unido.</span><span class="sxs-lookup"><span data-stu-id="b6b31-122">Null if participant is still joined.</span></span> <span data-ttu-id="b6b31-123">Marca de tiempo del canal dejando el evento si no es NULL.</span><span class="sxs-lookup"><span data-stu-id="b6b31-123">The time stamp of the channel leaving event if not null.</span></span></p>
<p><span data-ttu-id="b6b31-124">Estas entradas se eliminan en algún momento cuando todos los traductores procesan el evento.</span><span class="sxs-lookup"><span data-stu-id="b6b31-124">These entries are eventually removed when all translators process the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b31-125">userUri</span><span class="sxs-lookup"><span data-stu-id="b6b31-125">userUri</span></span></p></td>
<td><p><span data-ttu-id="b6b31-126">nvarchar (255), not null</span><span class="sxs-lookup"><span data-stu-id="b6b31-126">nvarchar(255), not null</span></span></p></td>
<td><p><span data-ttu-id="b6b31-127">URI de usuario.</span><span class="sxs-lookup"><span data-stu-id="b6b31-127">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6b31-128">serverID</span><span class="sxs-lookup"><span data-stu-id="b6b31-128">serverID</span></span></p></td>
<td><p><span data-ttu-id="b6b31-129">int</span><span class="sxs-lookup"><span data-stu-id="b6b31-129">int</span></span></p></td>
<td><p><span data-ttu-id="b6b31-130">Identidad del servidor (como en la tabla tblServerIdentity. serverID).</span><span class="sxs-lookup"><span data-stu-id="b6b31-130">Server identity (as in tblServerIdentity.serverID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6b31-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6b31-131">sessionId</span></span></p></td>
<td><p><span data-ttu-id="b6b31-132">BIGINT</span><span class="sxs-lookup"><span data-stu-id="b6b31-132">bigint</span></span></p></td>
<td><p><span data-ttu-id="b6b31-133">Sesión de servidor.</span><span class="sxs-lookup"><span data-stu-id="b6b31-133">Server session.</span></span> <span data-ttu-id="b6b31-134">Este es un número aleatorio generado cada vez que se inicia un servicio de chat.</span><span class="sxs-lookup"><span data-stu-id="b6b31-134">This is a random number generated each time a Chat service starts.</span></span> <span data-ttu-id="b6b31-135">Se usa para diferenciar las sesiones con el fin de identificar a los participantes huérfanos.</span><span class="sxs-lookup"><span data-stu-id="b6b31-135">It is used to differentiate sessions for the purpose of identifying orphaned participants.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="b6b31-136">Clave</span><span class="sxs-lookup"><span data-stu-id="b6b31-136">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6b31-137">Columna</span><span class="sxs-lookup"><span data-stu-id="b6b31-137">Column</span></span></th>
<th><span data-ttu-id="b6b31-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6b31-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6b31-139">&lt;channelUri, userId, joinedAt&gt;</span><span class="sxs-lookup"><span data-stu-id="b6b31-139">&lt;channelUri, userId, joinedAt&gt;</span></span></p></td>
<td><p><span data-ttu-id="b6b31-140">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="b6b31-140">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b6b31-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6b31-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

