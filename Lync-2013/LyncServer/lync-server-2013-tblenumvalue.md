---
title: 'Lync Server 2013: tblEnumValue'
description: 'Lync Server 2013: tblEnumValue'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumValue
ms:assetid: a33df20c-d19d-4f5c-b012-29dab8fb9200
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615025(v=OCS.15)
ms:contentKeyID: 48185040
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 159f90bb96c367fcb3e11725a582a9993080d3fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444451"
---
# <a name="tblenumvalue-in-lync-server-2013"></a><span data-ttu-id="01469-103">tblEnumValue en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01469-103">tblEnumValue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01469-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01469-104">

<span> </span></span></span>

<span data-ttu-id="01469-105">_**Última modificación del tema:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="01469-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="01469-106">tblEnumValue es una tabla codificada que contiene los valores de visibilidad y comportamiento de los atributos que se usan en la tabla de nodos.</span><span class="sxs-lookup"><span data-stu-id="01469-106">tblEnumValue is a hardcoded table that contains the Visibility and Behavior values of the attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="01469-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="01469-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01469-108">Columna</span><span class="sxs-lookup"><span data-stu-id="01469-108">Column</span></span></th>
<th><span data-ttu-id="01469-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="01469-109">Type</span></span></th>
<th><span data-ttu-id="01469-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="01469-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01469-111">valueID</span><span class="sxs-lookup"><span data-stu-id="01469-111">valueID</span></span></p></td>
<td><p><span data-ttu-id="01469-112">smallint, not null</span><span class="sxs-lookup"><span data-stu-id="01469-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="01469-113">IDENTIFICADOR del valor.</span><span class="sxs-lookup"><span data-stu-id="01469-113">ID of the value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01469-114">attributeID</span><span class="sxs-lookup"><span data-stu-id="01469-114">attributeID</span></span></p></td>
<td><p><span data-ttu-id="01469-115">smallint, not null</span><span class="sxs-lookup"><span data-stu-id="01469-115">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="01469-116">IDENTIFICADOR del atributo.</span><span class="sxs-lookup"><span data-stu-id="01469-116">ID of the attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01469-117">attributeValue</span><span class="sxs-lookup"><span data-stu-id="01469-117">attributeValue</span></span></p></td>
<td><p><span data-ttu-id="01469-118">nvarchar (256), not null</span><span class="sxs-lookup"><span data-stu-id="01469-118">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="01469-119">Nombre del valor.</span><span class="sxs-lookup"><span data-stu-id="01469-119">Name of the value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="01469-120">Sus</span><span class="sxs-lookup"><span data-stu-id="01469-120">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01469-121">Columna</span><span class="sxs-lookup"><span data-stu-id="01469-121">Column</span></span></th>
<th><span data-ttu-id="01469-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="01469-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01469-123">valueID</span><span class="sxs-lookup"><span data-stu-id="01469-123">valueID</span></span></p></td>
<td><p><span data-ttu-id="01469-124">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="01469-124">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01469-125">attributeID</span><span class="sxs-lookup"><span data-stu-id="01469-125">attributeID</span></span></p></td>
<td><p><span data-ttu-id="01469-126">Clave externa con la búsqueda en la tabla tblEnumAttribute. attributeID.</span><span class="sxs-lookup"><span data-stu-id="01469-126">Foreign key with lookup in tblEnumAttribute.attributeID table.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="01469-127">Valores de tabla</span><span class="sxs-lookup"><span data-stu-id="01469-127">Table Values</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01469-128">valueID</span><span class="sxs-lookup"><span data-stu-id="01469-128">valueID</span></span></th>
<th><span data-ttu-id="01469-129">attributeID</span><span class="sxs-lookup"><span data-stu-id="01469-129">attributeID</span></span></th>
<th><span data-ttu-id="01469-130">attributeValue</span><span class="sxs-lookup"><span data-stu-id="01469-130">attributeValue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01469-131">2</span><span class="sxs-lookup"><span data-stu-id="01469-131">2</span></span></p></td>
<td><p><span data-ttu-id="01469-132">1</span><span class="sxs-lookup"><span data-stu-id="01469-132">1</span></span></p></td>
<td><p><span data-ttu-id="01469-133">private</span><span class="sxs-lookup"><span data-stu-id="01469-133">private</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01469-134">3</span><span class="sxs-lookup"><span data-stu-id="01469-134">3</span></span></p></td>
<td><p><span data-ttu-id="01469-135">1</span><span class="sxs-lookup"><span data-stu-id="01469-135">1</span></span></p></td>
<td><p><span data-ttu-id="01469-136">ID</span><span class="sxs-lookup"><span data-stu-id="01469-136">scope</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01469-137">4</span><span class="sxs-lookup"><span data-stu-id="01469-137">4</span></span></p></td>
<td><p><span data-ttu-id="01469-138">2</span><span class="sxs-lookup"><span data-stu-id="01469-138">2</span></span></p></td>
<td><p><span data-ttu-id="01469-139">normal</span><span class="sxs-lookup"><span data-stu-id="01469-139">normal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01469-140">5</span><span class="sxs-lookup"><span data-stu-id="01469-140">5</span></span></p></td>
<td><p><span data-ttu-id="01469-141">2</span><span class="sxs-lookup"><span data-stu-id="01469-141">2</span></span></p></td>
<td><p><span data-ttu-id="01469-142">Audi</span><span class="sxs-lookup"><span data-stu-id="01469-142">auditorium</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01469-143">6</span><span class="sxs-lookup"><span data-stu-id="01469-143">6</span></span></p></td>
<td><p><span data-ttu-id="01469-144">1</span><span class="sxs-lookup"><span data-stu-id="01469-144">1</span></span></p></td>
<td><p><span data-ttu-id="01469-145">volver</span><span class="sxs-lookup"><span data-stu-id="01469-145">open</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="01469-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="01469-146">See Also</span></span>


[<span data-ttu-id="01469-147">tblNode en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01469-147">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="01469-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01469-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

