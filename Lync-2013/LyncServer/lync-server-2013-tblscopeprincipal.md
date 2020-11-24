---
title: 'Lync Server 2013: tblScopePrincipal'
description: 'Lync Server 2013: tblScopePrincipal'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblScopePrincipal
ms:assetid: 422d6c7f-7ba7-4dd4-bacc-95ace47959ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558639(v=OCS.15)
ms:contentKeyID: 48184009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63315f8525e5c2f05fe54a0f9ed9e8a97b9e8bce
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398069"
---
# <a name="tblscopeprincipal-in-lync-server-2013"></a><span data-ttu-id="2bc2e-103">tblScopePrincipal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2bc2e-103">tblScopePrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2bc2e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2bc2e-104">

<span> </span></span></span>

<span data-ttu-id="2bc2e-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="2bc2e-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="2bc2e-106">tblScopePrincipal contiene ámbitos asignados a los nodos.</span><span class="sxs-lookup"><span data-stu-id="2bc2e-106">tblScopePrincipal contains scopes assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="2bc2e-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="2bc2e-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bc2e-108">Columna</span><span class="sxs-lookup"><span data-stu-id="2bc2e-108">Column</span></span></th>
<th><span data-ttu-id="2bc2e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bc2e-109">Type</span></span></th>
<th><span data-ttu-id="2bc2e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bc2e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bc2e-111">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="2bc2e-111">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="2bc2e-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-113">IDENTIFICADOR de nodo al que se aplica el ámbito.</span><span class="sxs-lookup"><span data-stu-id="2bc2e-113">Node ID that the scope applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bc2e-114">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="2bc2e-114">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-115">int, not null</span><span class="sxs-lookup"><span data-stu-id="2bc2e-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-116">IDENTIFICADOR principal.</span><span class="sxs-lookup"><span data-stu-id="2bc2e-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bc2e-117">scopeIsDenied</span><span class="sxs-lookup"><span data-stu-id="2bc2e-117">scopeIsDenied</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-118">bit, not null</span><span class="sxs-lookup"><span data-stu-id="2bc2e-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-119">Verdadero si el tipo de ámbito es denegar; False si la opción permitir.</span><span class="sxs-lookup"><span data-stu-id="2bc2e-119">True if type of scope is Deny; False if Allow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bc2e-120">scopeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="2bc2e-120">scopeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-121">int, not null</span><span class="sxs-lookup"><span data-stu-id="2bc2e-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-122">IDENTIFICADOR de la entidad de identidad que actualizó por última vez esta entrada.</span><span class="sxs-lookup"><span data-stu-id="2bc2e-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="2bc2e-123">Sus</span><span class="sxs-lookup"><span data-stu-id="2bc2e-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bc2e-124">Columna</span><span class="sxs-lookup"><span data-stu-id="2bc2e-124">Column</span></span></th>
<th><span data-ttu-id="2bc2e-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bc2e-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bc2e-126">&lt;scopeNodeID, scopePrinID&gt;</span><span class="sxs-lookup"><span data-stu-id="2bc2e-126">&lt;scopeNodeID, scopePrinID&gt;</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-127">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="2bc2e-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bc2e-128">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="2bc2e-128">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-129">Clave externa con la búsqueda en la tabla tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="2bc2e-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bc2e-130">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="2bc2e-130">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="2bc2e-131">Clave externa con la búsqueda en la tabla tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="2bc2e-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2bc2e-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2bc2e-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

