---
title: 'Lync Server 2013: tblPrincipalMeta'
description: 'Lync Server 2013: tblPrincipalMeta'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMeta
ms:assetid: 808490d4-7d6d-47a2-b8af-b5940d47073b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615009(v=OCS.15)
ms:contentKeyID: 48184648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 899fd1e450dac52afa56c1ee1de86da82b2db309
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398106"
---
# <a name="tblprincipalmeta-in-lync-server-2013"></a><span data-ttu-id="7c7b3-103">tblPrincipalMeta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c7b3-103">tblPrincipalMeta in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7c7b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7c7b3-104">

<span> </span></span></span>

<span data-ttu-id="7c7b3-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="7c7b3-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="7c7b3-106">tblPrincipalMeta contiene las entidades de identidad que deben actualizarse desde los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-106">tblPrincipalMeta contains the principals that have to be refreshed from Active Directory Domain Services.</span></span>

### <a name="columns"></a><span data-ttu-id="7c7b3-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="7c7b3-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c7b3-108">Columna</span><span class="sxs-lookup"><span data-stu-id="7c7b3-108">Column</span></span></th>
<th><span data-ttu-id="7c7b3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c7b3-109">Type</span></span></th>
<th><span data-ttu-id="7c7b3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c7b3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c7b3-111">prinID</span><span class="sxs-lookup"><span data-stu-id="7c7b3-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="7c7b3-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-113">IDENTIFICADOR principal.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7b3-114">prinAffiliationsDirty</span><span class="sxs-lookup"><span data-stu-id="7c7b3-114">prinAffiliationsDirty</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-115">bit, not null</span><span class="sxs-lookup"><span data-stu-id="7c7b3-115">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-116">True si es necesario actualizar las afiliaciones principales.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-116">True if principal affiliations have to be refreshed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7b3-117">prinAttributesDirty</span><span class="sxs-lookup"><span data-stu-id="7c7b3-117">prinAttributesDirty</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-118">bit, not null</span><span class="sxs-lookup"><span data-stu-id="7c7b3-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-119">True si es necesario actualizar los atributos de principal.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-119">True if principal attributes have to be refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7b3-120">prinDeleted</span><span class="sxs-lookup"><span data-stu-id="7c7b3-120">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-121">bit, not null</span><span class="sxs-lookup"><span data-stu-id="7c7b3-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-122">True si el principal se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-122">True if the principal has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7b3-123">tryCount</span><span class="sxs-lookup"><span data-stu-id="7c7b3-123">tryCount</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-124">int</span><span class="sxs-lookup"><span data-stu-id="7c7b3-124">int</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-125">Número de intentos de actualizar el principal de AD DS que se ha producido hasta el momento.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-125">Number of attempts to refresh the principal from AD DS that have happened so far.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7b3-126">lastTry</span><span class="sxs-lookup"><span data-stu-id="7c7b3-126">lastTry</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-127">datetime</span><span class="sxs-lookup"><span data-stu-id="7c7b3-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-128">Marca de tiempo del último intento de actualizar la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-128">Time stamp from the latest attempt to refresh the principal.</span></span> <span data-ttu-id="7c7b3-129">Puede ser null si aún no se ha intentado ninguna actualización.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-129">Can be null if no refresh has been attempted yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7b3-130">nextTry</span><span class="sxs-lookup"><span data-stu-id="7c7b3-130">nextTry</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-131">datetime</span><span class="sxs-lookup"><span data-stu-id="7c7b3-131">datetime</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-132">Marca de tiempo de la siguiente actualización programada.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-132">Time stamp for the next scheduled refresh.</span></span> <span data-ttu-id="7c7b3-133">Puede ser null si no se ha programado ninguna actualización adicional.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-133">Can be null if no further refresh has been scheduled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="7c7b3-134">Sus</span><span class="sxs-lookup"><span data-stu-id="7c7b3-134">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c7b3-135">Columna</span><span class="sxs-lookup"><span data-stu-id="7c7b3-135">Column</span></span></th>
<th><span data-ttu-id="7c7b3-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c7b3-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c7b3-137">prinID</span><span class="sxs-lookup"><span data-stu-id="7c7b3-137">prinID</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-138">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-138">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7b3-139">prinID</span><span class="sxs-lookup"><span data-stu-id="7c7b3-139">prinID</span></span></p></td>
<td><p><span data-ttu-id="7c7b3-140">Clave externa con la búsqueda en la tabla tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="7c7b3-140">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7c7b3-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7c7b3-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

