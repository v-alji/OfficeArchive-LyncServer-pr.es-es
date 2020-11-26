---
title: 'Lync Server 2013: tblPrincipalAffiliations'
description: 'Lync Server 2013: tblPrincipalAffiliations'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalAffiliations
ms:assetid: 45fd8484-5837-44d2-85bb-45c83546607c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558642(v=OCS.15)
ms:contentKeyID: 48183993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c373147a58300e64f22e60e989a777c59b2653
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441371"
---
# <a name="tblprincipalaffiliations-in-lync-server-2013"></a><span data-ttu-id="fdf10-103">tblPrincipalAffiliations en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fdf10-103">tblPrincipalAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fdf10-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fdf10-104">

<span> </span></span></span>

<span data-ttu-id="fdf10-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="fdf10-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="fdf10-106">tblPrincipalAffiliations contiene las afiliaciones principales que describen las pertenencias en ubicaciones, incluidos los grupos de seguridad de los servicios de dominio de Active Directory, en contenedores de Active Directory, en dominios.</span><span class="sxs-lookup"><span data-stu-id="fdf10-106">tblPrincipalAffiliations contains the principal affiliations that describe memberships in locations, including Active Directory Domain Services security groups, in Active Directory containers, in domains.</span></span>

### <a name="columns"></a><span data-ttu-id="fdf10-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="fdf10-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fdf10-108">Columna</span><span class="sxs-lookup"><span data-stu-id="fdf10-108">Column</span></span></th>
<th><span data-ttu-id="fdf10-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdf10-109">Type</span></span></th>
<th><span data-ttu-id="fdf10-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdf10-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdf10-111">principalID</span><span class="sxs-lookup"><span data-stu-id="fdf10-111">principalID</span></span></p></td>
<td><p><span data-ttu-id="fdf10-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="fdf10-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="fdf10-113">IDENTIFICADOR de la entidad de identidad afiliada.</span><span class="sxs-lookup"><span data-stu-id="fdf10-113">ID of the affiliated principal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdf10-114">affiliationID</span><span class="sxs-lookup"><span data-stu-id="fdf10-114">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="fdf10-115">int, not null</span><span class="sxs-lookup"><span data-stu-id="fdf10-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="fdf10-116">IDENTIFICADOR de la identidad que representa la afiliación.</span><span class="sxs-lookup"><span data-stu-id="fdf10-116">ID of the principal representing the affiliation.</span></span> <span data-ttu-id="fdf10-117">Cada principal (excepto los tipos de usuario del sistema) tiene también una afiliación propia.</span><span class="sxs-lookup"><span data-stu-id="fdf10-117">Each principal (except system-user-types) has a self-affiliation as well.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdf10-118">clasificación</span><span class="sxs-lookup"><span data-stu-id="fdf10-118">index</span></span></p></td>
<td><p><span data-ttu-id="fdf10-119">int, not null</span><span class="sxs-lookup"><span data-stu-id="fdf10-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="fdf10-120">Clasificación.</span><span class="sxs-lookup"><span data-stu-id="fdf10-120">Index.</span></span> <span data-ttu-id="fdf10-121">El valor de las afiliaciones automáticas es de-1 y para las otras afiliaciones que aumenta secuencialmente de 1 en cada &lt; principalID, affiliationId &gt; bucket.</span><span class="sxs-lookup"><span data-stu-id="fdf10-121">The value for self-affiliations is -1, and for the other affiliations it increases sequentially from 1 within each &lt;principalID, affiliationId&gt; bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdf10-122">updatedBy</span><span class="sxs-lookup"><span data-stu-id="fdf10-122">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="fdf10-123">int, not null</span><span class="sxs-lookup"><span data-stu-id="fdf10-123">int, not null</span></span></p></td>
<td><p><span data-ttu-id="fdf10-124">Principal que realizó la actualización más reciente.</span><span class="sxs-lookup"><span data-stu-id="fdf10-124">Principal that did the latest update.</span></span> <span data-ttu-id="fdf10-125">Esto suele ser 1, que significa sincronización de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fdf10-125">This is usually 1, which means Active Directory Sync.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="fdf10-126">Sus</span><span class="sxs-lookup"><span data-stu-id="fdf10-126">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fdf10-127">Columnas</span><span class="sxs-lookup"><span data-stu-id="fdf10-127">Columns</span></span></th>
<th><span data-ttu-id="fdf10-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdf10-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdf10-129">&lt;principalID, Indice, affiliationID&gt;</span><span class="sxs-lookup"><span data-stu-id="fdf10-129">&lt;principalID, index, affiliationID&gt;</span></span></p></td>
<td><p><span data-ttu-id="fdf10-130">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="fdf10-130">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdf10-131">principalID</span><span class="sxs-lookup"><span data-stu-id="fdf10-131">principalID</span></span></p></td>
<td><p><span data-ttu-id="fdf10-132">Clave externa con la búsqueda en la tabla tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="fdf10-132">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdf10-133">affiliationID</span><span class="sxs-lookup"><span data-stu-id="fdf10-133">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="fdf10-134">Clave externa con la búsqueda en la tabla tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="fdf10-134">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fdf10-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fdf10-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

