---
title: 'Lync Server 2013: tblPrincipalMemberDifference'
description: 'Lync Server 2013: tblPrincipalMemberDifference'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMemberDifference
ms:assetid: 0b94f555-6888-4fe0-a048-4660a2513276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558612(v=OCS.15)
ms:contentKeyID: 48183379
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce7c770a6fed02dc27d2493816fae58943d391a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398117"
---
# <a name="tblprincipalmemberdifference-in-lync-server-2013"></a><span data-ttu-id="a2d7d-103">tblPrincipalMemberDifference en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2d7d-103">tblPrincipalMemberDifference in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2d7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2d7d-104">

<span> </span></span></span>

<span data-ttu-id="a2d7d-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="a2d7d-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="a2d7d-106">tblPrincipalMemberDifference contiene cambios de pertenencia a grupos (miembros agregados y eliminados) que aún no han procesado los pasos de sincronización de servicios de dominio de Active Directory más recientes.</span><span class="sxs-lookup"><span data-stu-id="a2d7d-106">tblPrincipalMemberDifference contains group membership changes (both added and removed members) that have not yet been processed by the later Active Directory Domain Services Sync steps.</span></span>

### <a name="columns"></a><span data-ttu-id="a2d7d-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="a2d7d-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a2d7d-108">Columna</span><span class="sxs-lookup"><span data-stu-id="a2d7d-108">Column</span></span></th>
<th><span data-ttu-id="a2d7d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2d7d-109">Type</span></span></th>
<th><span data-ttu-id="a2d7d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2d7d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2d7d-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="a2d7d-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="a2d7d-112">GUID, not null</span><span class="sxs-lookup"><span data-stu-id="a2d7d-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="a2d7d-113">GUID principal del grupo que cambió.</span><span class="sxs-lookup"><span data-stu-id="a2d7d-113">Principal GUID of the group that changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2d7d-114">memberADPath</span><span class="sxs-lookup"><span data-stu-id="a2d7d-114">memberADPath</span></span></p></td>
<td><p><span data-ttu-id="a2d7d-115">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="a2d7d-115">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="a2d7d-116">Nombre distintivo del miembro.</span><span class="sxs-lookup"><span data-stu-id="a2d7d-116">Distinguished name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2d7d-117">memberRemoved</span><span class="sxs-lookup"><span data-stu-id="a2d7d-117">memberRemoved</span></span></p></td>
<td><p><span data-ttu-id="a2d7d-118">bit, not null</span><span class="sxs-lookup"><span data-stu-id="a2d7d-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="a2d7d-119">False si se agregó el miembro.</span><span class="sxs-lookup"><span data-stu-id="a2d7d-119">False if the member was added.</span></span> <span data-ttu-id="a2d7d-120">True si se ha quitado el miembro.</span><span class="sxs-lookup"><span data-stu-id="a2d7d-120">True if the member was removed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="a2d7d-121">Clave</span><span class="sxs-lookup"><span data-stu-id="a2d7d-121">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a2d7d-122">Columna</span><span class="sxs-lookup"><span data-stu-id="a2d7d-122">Column</span></span></th>
<th><span data-ttu-id="a2d7d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2d7d-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2d7d-124">&lt;prinGuid, memberADPath&gt;</span><span class="sxs-lookup"><span data-stu-id="a2d7d-124">&lt;prinGuid, memberADPath&gt;</span></span></p></td>
<td><p><span data-ttu-id="a2d7d-125">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="a2d7d-125">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a2d7d-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2d7d-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

