---
title: 'Lync Server 2013: Escalabilidad'
description: Lync Server 2013 escalabilidad.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scalability
ms:assetid: 46fa0cb5-1507-4a12-ad3f-ba64585e2dc4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417160(v=OCS.15)
ms:contentKeyID: 48183995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28cd5820755ffd1eb863ed6f2369b5756a7ae3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442120"
---
# <a name="scalability-with-lync-server-2013"></a><span data-ttu-id="e79cb-103">Escalabilidad con Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e79cb-103">Scalability with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e79cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e79cb-104">

<span> </span></span></span>

<span data-ttu-id="e79cb-105">_**Última modificación del tema:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="e79cb-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="e79cb-106">Lync Server se ofrece en dos ediciones Enterprise Edition y Standard.</span><span class="sxs-lookup"><span data-stu-id="e79cb-106">Lync Server is offered in two editions, Enterprise Edition and Standard Edition.</span></span> <span data-ttu-id="e79cb-107">Las diferentes ediciones están pensadas principalmente para diferentes tamaños de organizaciones.</span><span class="sxs-lookup"><span data-stu-id="e79cb-107">The different editions are intended primarily for different sizes of organizations.</span></span> <span data-ttu-id="e79cb-108">Como se muestra en la tabla siguiente, ambas ediciones admiten toda la funcionalidad de todas las cargas de trabajo, excepto para la alta disponibilidad y la recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="e79cb-108">As shown in the following table, both editions support all functionality in all workloads, except for high availability and disaster recovery.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e79cb-109">Característica</span><span class="sxs-lookup"><span data-stu-id="e79cb-109">Feature</span></span></th>
<th><span data-ttu-id="e79cb-110">¿Es compatible con Enterprise Edition?</span><span class="sxs-lookup"><span data-stu-id="e79cb-110">Supported in Enterprise Edition?</span></span></th>
<th><span data-ttu-id="e79cb-111">¿Compatible con Standard Edition?</span><span class="sxs-lookup"><span data-stu-id="e79cb-111">Supported in Standard Edition?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e79cb-112">Mensajería instantánea (mi) y presencia</span><span class="sxs-lookup"><span data-stu-id="e79cb-112">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="e79cb-113">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-113">Yes</span></span></p></td>
<td><p><span data-ttu-id="e79cb-114">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-114">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e79cb-115">Conferencias</span><span class="sxs-lookup"><span data-stu-id="e79cb-115">Conferencing</span></span></p></td>
<td><p><span data-ttu-id="e79cb-116">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-116">Yes</span></span></p></td>
<td><p><span data-ttu-id="e79cb-117">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-117">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e79cb-118">Conferencia A/V</span><span class="sxs-lookup"><span data-stu-id="e79cb-118">A/V conferencing</span></span></p></td>
<td><p><span data-ttu-id="e79cb-119">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-119">Yes</span></span></p></td>
<td><p><span data-ttu-id="e79cb-120">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e79cb-121">Conferencia de acceso telefónico local</span><span class="sxs-lookup"><span data-stu-id="e79cb-121">Dial-in conferencing</span></span></p></td>
<td><p><span data-ttu-id="e79cb-122">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-122">Yes</span></span></p></td>
<td><p><span data-ttu-id="e79cb-123">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-123">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e79cb-124">Telefonía IP empresarial</span><span class="sxs-lookup"><span data-stu-id="e79cb-124">Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="e79cb-125">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-125">Yes</span></span></p></td>
<td><p><span data-ttu-id="e79cb-126">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-126">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e79cb-127">Virtualización</span><span class="sxs-lookup"><span data-stu-id="e79cb-127">Virtualization</span></span></p></td>
<td><p><span data-ttu-id="e79cb-128">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-128">Yes</span></span></p></td>
<td><p><span data-ttu-id="e79cb-129">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-129">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e79cb-130">Alta disponibilidad, failover y recuperación ante desastres</span><span class="sxs-lookup"><span data-stu-id="e79cb-130">High availability, failover, and disaster recovery</span></span></p></td>
<td><p><span data-ttu-id="e79cb-131">Sí</span><span class="sxs-lookup"><span data-stu-id="e79cb-131">Yes</span></span></p></td>
<td><p><span data-ttu-id="e79cb-132">No</span><span class="sxs-lookup"><span data-stu-id="e79cb-132">No</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e79cb-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e79cb-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

