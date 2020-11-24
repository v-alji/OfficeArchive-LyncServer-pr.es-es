---
title: 'Lync Server 2013: tblPrincipalRole'
description: 'Lync Server 2013: tblPrincipalRole'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalRole
ms:assetid: dcd16dc1-a66c-4720-a48f-ec8b28337383
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615039(v=OCS.15)
ms:contentKeyID: 48185597
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f58ffda3136c254ee77f14d33dcb42af5d172c4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398087"
---
# <a name="tblprincipalrole-in-lync-server-2013"></a><span data-ttu-id="54c2d-103">tblPrincipalRole en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54c2d-103">tblPrincipalRole in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54c2d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54c2d-104">

<span> </span></span></span>

<span data-ttu-id="54c2d-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="54c2d-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="54c2d-106">tblPrincipalRole contiene los roles explícitos asignados a los nodos.</span><span class="sxs-lookup"><span data-stu-id="54c2d-106">tblPrincipalRole contains explicit roles assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="54c2d-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="54c2d-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54c2d-108">Columna</span><span class="sxs-lookup"><span data-stu-id="54c2d-108">Column</span></span></th>
<th><span data-ttu-id="54c2d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="54c2d-109">Type</span></span></th>
<th><span data-ttu-id="54c2d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="54c2d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54c2d-111">prinRoleNodeID</span><span class="sxs-lookup"><span data-stu-id="54c2d-111">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="54c2d-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="54c2d-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="54c2d-113">IDENTIFICADOR de nodo al que se aplica el rol.</span><span class="sxs-lookup"><span data-stu-id="54c2d-113">Node ID that the role applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54c2d-114">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="54c2d-114">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="54c2d-115">int, not null</span><span class="sxs-lookup"><span data-stu-id="54c2d-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="54c2d-116">IDENTIFICADOR principal.</span><span class="sxs-lookup"><span data-stu-id="54c2d-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54c2d-117">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="54c2d-117">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="54c2d-118">int, not null</span><span class="sxs-lookup"><span data-stu-id="54c2d-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="54c2d-119">IDENTIFICADOR de tipo de rol (de tblRoleType).</span><span class="sxs-lookup"><span data-stu-id="54c2d-119">Role type ID (from tblRoleType).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54c2d-120">prinRoleUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="54c2d-120">prinRoleUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="54c2d-121">int, not null</span><span class="sxs-lookup"><span data-stu-id="54c2d-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="54c2d-122">IDENTIFICADOR de la entidad de identidad que actualizó por última vez esta entrada.</span><span class="sxs-lookup"><span data-stu-id="54c2d-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="54c2d-123">Sus</span><span class="sxs-lookup"><span data-stu-id="54c2d-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54c2d-124">Columna</span><span class="sxs-lookup"><span data-stu-id="54c2d-124">Column</span></span></th>
<th><span data-ttu-id="54c2d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="54c2d-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54c2d-126">&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</span><span class="sxs-lookup"><span data-stu-id="54c2d-126">&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="54c2d-127">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="54c2d-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54c2d-128">prinRoleNodeID</span><span class="sxs-lookup"><span data-stu-id="54c2d-128">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="54c2d-129">Clave externa con la búsqueda en la tabla tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="54c2d-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54c2d-130">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="54c2d-130">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="54c2d-131">Clave externa con la búsqueda en la tabla tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="54c2d-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54c2d-132">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="54c2d-132">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="54c2d-133">Clave externa con la búsqueda en la tabla tblRoleType. rtypeID.</span><span class="sxs-lookup"><span data-stu-id="54c2d-133">Foreign key with lookup in tblRoleType.rtypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="54c2d-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54c2d-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

