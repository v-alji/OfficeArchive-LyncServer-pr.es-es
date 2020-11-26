---
title: 'Lync Server 2013: tblLastInviteId'
description: 'Lync Server 2013: tblLastInviteId'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblLastInviteId
ms:assetid: 222b3508-5963-4ddc-b4f3-e8412767e61b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558625(v=OCS.15)
ms:contentKeyID: 48183608
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5a13cfc7edc29ea20c95f7f4d587b0cfb84eb73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444423"
---
# <a name="tbllastinviteid-in-lync-server-2013"></a><span data-ttu-id="c0524-103">tblLastInviteId en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0524-103">tblLastInviteId in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0524-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0524-104">

<span> </span></span></span>

<span data-ttu-id="c0524-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="c0524-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="c0524-106">tblLastInviteId contiene el último identificador de invitación generado (y usado en la tabla tblPrincipalInvites) para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="c0524-106">tblLastInviteId contains the last invite ID that was generated (and used in the tblPrincipalInvites table) for each user.</span></span>

### <a name="columns"></a><span data-ttu-id="c0524-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="c0524-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0524-108">Columna</span><span class="sxs-lookup"><span data-stu-id="c0524-108">Column</span></span></th>
<th><span data-ttu-id="c0524-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0524-109">Type</span></span></th>
<th><span data-ttu-id="c0524-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0524-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0524-111">prinID</span><span class="sxs-lookup"><span data-stu-id="c0524-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="c0524-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="c0524-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="c0524-113">IDENTIFICADOR principal.</span><span class="sxs-lookup"><span data-stu-id="c0524-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0524-114">lastInviteID</span><span class="sxs-lookup"><span data-stu-id="c0524-114">lastInviteID</span></span></p></td>
<td><p><span data-ttu-id="c0524-115">int, not null</span><span class="sxs-lookup"><span data-stu-id="c0524-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="c0524-116">Último ID de invitación usado.</span><span class="sxs-lookup"><span data-stu-id="c0524-116">Last used invite ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="c0524-117">Sus</span><span class="sxs-lookup"><span data-stu-id="c0524-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0524-118">Columna</span><span class="sxs-lookup"><span data-stu-id="c0524-118">Column</span></span></th>
<th><span data-ttu-id="c0524-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0524-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0524-120">prinID</span><span class="sxs-lookup"><span data-stu-id="c0524-120">prinID</span></span></p></td>
<td><p><span data-ttu-id="c0524-121">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="c0524-121">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0524-122">prinID</span><span class="sxs-lookup"><span data-stu-id="c0524-122">prinID</span></span></p></td>
<td><p><span data-ttu-id="c0524-123">Clave externa con la búsqueda en la tabla tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="c0524-123">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="c0524-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0524-124">See Also</span></span>


[<span data-ttu-id="c0524-125">tblPrincipalInvites en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0524-125">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)  
  

<span data-ttu-id="c0524-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0524-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

