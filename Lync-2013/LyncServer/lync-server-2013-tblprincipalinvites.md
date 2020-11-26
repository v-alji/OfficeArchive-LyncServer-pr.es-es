---
title: 'Lync Server 2013: tblPrincipalInvites'
description: 'Lync Server 2013: tblPrincipalInvites'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalInvites
ms:assetid: 548ec156-4d1a-469d-a804-62cff226e5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558650(v=OCS.15)
ms:contentKeyID: 48184141
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30d741864ed2a3cfbec8329215be33c21b3b262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423508"
---
# <a name="tblprincipalinvites-in-lync-server-2013"></a><span data-ttu-id="7d036-103">tblPrincipalInvites en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d036-103">tblPrincipalInvites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d036-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d036-104">

<span> </span></span></span>

<span data-ttu-id="7d036-105">_**Última modificación del tema:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="7d036-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="7d036-106">tblPrincipalInvites contiene invitaciones para todos los usuarios aprovisionados para todos los nodos con la opción de autoinvitar activada.</span><span class="sxs-lookup"><span data-stu-id="7d036-106">tblPrincipalInvites contains invitations for all provisioned users for all nodes with auto-invite on.</span></span>

### <a name="columns"></a><span data-ttu-id="7d036-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="7d036-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d036-108">Columna</span><span class="sxs-lookup"><span data-stu-id="7d036-108">Column</span></span></th>
<th><span data-ttu-id="7d036-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d036-109">Type</span></span></th>
<th><span data-ttu-id="7d036-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d036-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d036-111">prinID</span><span class="sxs-lookup"><span data-stu-id="7d036-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="7d036-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="7d036-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7d036-113">IDENTIFICADOR principal.</span><span class="sxs-lookup"><span data-stu-id="7d036-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d036-114">invID</span><span class="sxs-lookup"><span data-stu-id="7d036-114">invID</span></span></p></td>
<td><p><span data-ttu-id="7d036-115">int, not null</span><span class="sxs-lookup"><span data-stu-id="7d036-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7d036-116">Número secuencial único (por identificador de entidad de identidad) generado desde la tabla tblLastInviteId.</span><span class="sxs-lookup"><span data-stu-id="7d036-116">Unique sequential number (per principal ID) generated from tblLastInviteId table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d036-117">nodeID</span><span class="sxs-lookup"><span data-stu-id="7d036-117">nodeID</span></span></p></td>
<td><p><span data-ttu-id="7d036-118">int, not null</span><span class="sxs-lookup"><span data-stu-id="7d036-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7d036-119">IDENTIFICADOR de nodo (solo salón de chat).</span><span class="sxs-lookup"><span data-stu-id="7d036-119">Node ID (chat room only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d036-120">creado</span><span class="sxs-lookup"><span data-stu-id="7d036-120">createdOn</span></span></p></td>
<td><p><span data-ttu-id="7d036-121">DateTime, not null</span><span class="sxs-lookup"><span data-stu-id="7d036-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="7d036-122">Momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="7d036-122">Time of creation.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="7d036-123">Sus</span><span class="sxs-lookup"><span data-stu-id="7d036-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d036-124">Columna</span><span class="sxs-lookup"><span data-stu-id="7d036-124">Column</span></span></th>
<th><span data-ttu-id="7d036-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d036-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d036-126">&lt;prinID, nodeID&gt;</span><span class="sxs-lookup"><span data-stu-id="7d036-126">&lt;prinID, nodeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="7d036-127">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="7d036-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d036-128">prinID</span><span class="sxs-lookup"><span data-stu-id="7d036-128">prinID</span></span></p></td>
<td><p><span data-ttu-id="7d036-129">Clave externa con la búsqueda en la tabla tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="7d036-129">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d036-130">nodeID</span><span class="sxs-lookup"><span data-stu-id="7d036-130">nodeID</span></span></p></td>
<td><p><span data-ttu-id="7d036-131">Clave externa con la búsqueda en la tabla tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="7d036-131">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7d036-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d036-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

