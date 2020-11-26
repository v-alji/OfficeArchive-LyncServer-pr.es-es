---
title: 'Lync Server 2013: tblPrincipal'
description: 'Lync Server 2013: tblPrincipal'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipal
ms:assetid: 79a24502-b4ce-41f0-8979-8caddf535338
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558667(v=OCS.15)
ms:contentKeyID: 48184571
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f07b37ac4c8ceed5c044b5c263eeee6370adfdc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444416"
---
# <a name="tblprincipal-in-lync-server-2013"></a><span data-ttu-id="4f0be-103">tblPrincipal enn Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f0be-103">tblPrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4f0be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4f0be-104">

<span> </span></span></span>

<span data-ttu-id="4f0be-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="4f0be-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="4f0be-106">tblPrincipal contiene todos los principales, incluidos los usuarios, las carpetas y los grupos.</span><span class="sxs-lookup"><span data-stu-id="4f0be-106">tblPrincipal contains all principals, including users, folders, and groups.</span></span>

### <a name="columns"></a><span data-ttu-id="4f0be-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="4f0be-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f0be-108">Columna</span><span class="sxs-lookup"><span data-stu-id="4f0be-108">Column</span></span></th>
<th><span data-ttu-id="4f0be-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f0be-109">Type</span></span></th>
<th><span data-ttu-id="4f0be-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f0be-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-111">prinID</span><span class="sxs-lookup"><span data-stu-id="4f0be-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="4f0be-112">int, not null</span><span class="sxs-lookup"><span data-stu-id="4f0be-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="4f0be-113">IDENTIFICADOR principal.</span><span class="sxs-lookup"><span data-stu-id="4f0be-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-114">prinGuid</span><span class="sxs-lookup"><span data-stu-id="4f0be-114">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="4f0be-115">GUID, not null</span><span class="sxs-lookup"><span data-stu-id="4f0be-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="4f0be-116">GUID principal.</span><span class="sxs-lookup"><span data-stu-id="4f0be-116">Principal GUID.</span></span> <span data-ttu-id="4f0be-117">Esto se usa ampliamente como una clave principal alternativa porque su significado pasa a ser el espacio de servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4f0be-117">This is broadly used as an alternate primary key because its meaning crosses over into the Active Directory Domain Services space.</span></span> <span data-ttu-id="4f0be-118">(El GUID de un principal en caché es igual al GUID de objeto de Active Directory correspondiente).</span><span class="sxs-lookup"><span data-stu-id="4f0be-118">(The GUID for a cached principal is equal to the corresponding Active Directory object GUID.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-119">prinUri</span><span class="sxs-lookup"><span data-stu-id="4f0be-119">prinUri</span></span></p></td>
<td><p><span data-ttu-id="4f0be-120">nvarchar (256), not null</span><span class="sxs-lookup"><span data-stu-id="4f0be-120">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="4f0be-121">URI principal.</span><span class="sxs-lookup"><span data-stu-id="4f0be-121">Principal URI.</span></span> <span data-ttu-id="4f0be-122">El esquema SIP se usa para los usuarios y el mA-GRP se usa para casi todos los demás.</span><span class="sxs-lookup"><span data-stu-id="4f0be-122">The SIP scheme is used for users, and ma-grp is used for almost everything else.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-123">prinName</span><span class="sxs-lookup"><span data-stu-id="4f0be-123">prinName</span></span></p></td>
<td><p><span data-ttu-id="4f0be-124">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="4f0be-124">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="4f0be-125">Nombre común.</span><span class="sxs-lookup"><span data-stu-id="4f0be-125">Common name.</span></span> <span data-ttu-id="4f0be-126">Solo se usan los tipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="4f0be-126">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-127">prinDisplayName</span><span class="sxs-lookup"><span data-stu-id="4f0be-127">prinDisplayName</span></span></p></td>
<td><p><span data-ttu-id="4f0be-128">Nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="4f0be-128">Nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="4f0be-129">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="4f0be-129">Display name.</span></span> <span data-ttu-id="4f0be-130">Solo se usan los tipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="4f0be-130">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-131">prinCompanyName</span><span class="sxs-lookup"><span data-stu-id="4f0be-131">prinCompanyName</span></span></p></td>
<td><p><span data-ttu-id="4f0be-132">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="4f0be-132">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="4f0be-133">Nombre de la empresa.</span><span class="sxs-lookup"><span data-stu-id="4f0be-133">Company name.</span></span> <span data-ttu-id="4f0be-134">Solo se usan los tipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="4f0be-134">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-135">prinEmail</span><span class="sxs-lookup"><span data-stu-id="4f0be-135">prinEmail</span></span></p></td>
<td><p><span data-ttu-id="4f0be-136">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="4f0be-136">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="4f0be-137">Correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4f0be-137">Email.</span></span> <span data-ttu-id="4f0be-138">Solo se usan los tipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="4f0be-138">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-139">prinADPath</span><span class="sxs-lookup"><span data-stu-id="4f0be-139">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="4f0be-140">nvarchar (384)</span><span class="sxs-lookup"><span data-stu-id="4f0be-140">nvarchar (384)</span></span></p></td>
<td><p><span data-ttu-id="4f0be-141">Nombre de dominio del objeto de Active Directory del que el principal es una versión almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="4f0be-141">Domain name of the Active Directory object that the principal is a cached version of.</span></span> <span data-ttu-id="4f0be-142">Puede ser null para los tipos que no son objetos de Active Directory (como usuarios del sistema).</span><span class="sxs-lookup"><span data-stu-id="4f0be-142">Can be Null for types that are not Active Directory objects (such as system users).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-143">prinADUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4f0be-143">prinADUserPrincipalName</span></span></p></td>
<td><p><span data-ttu-id="4f0be-144">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="4f0be-144">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="4f0be-145">Nombre principal de usuario (UPN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="4f0be-145">User’s user principal name (UPN).</span></span> <span data-ttu-id="4f0be-146">Solo lo usan los tipos de usuario normales.</span><span class="sxs-lookup"><span data-stu-id="4f0be-146">Used only by regular user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-147">prinDisabled</span><span class="sxs-lookup"><span data-stu-id="4f0be-147">prinDisabled</span></span></p></td>
<td><p><span data-ttu-id="4f0be-148">smallint, not null</span><span class="sxs-lookup"><span data-stu-id="4f0be-148">smallint, not null</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4f0be-149">0: la principal está activa.</span><span class="sxs-lookup"><span data-stu-id="4f0be-149">0: Principal is active.</span></span></p></li>
<li><p><span data-ttu-id="4f0be-150">1: la entidad de la identidad está deshabilitada porque las funciones SIP del usuario están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="4f0be-150">1: Principal is disabled because user’s SIP capabilities are disabled.</span></span></p></li>
<li><p><span data-ttu-id="4f0be-151">2: se eliminó el capital porque el objeto de AD asociado se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="4f0be-151">2: Principal is deleted because associated AD object has been deleted.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-152">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="4f0be-152">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="4f0be-153">smallint, not null</span><span class="sxs-lookup"><span data-stu-id="4f0be-153">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="4f0be-154">Tipo principal (de la tabla tblPrincipalType).</span><span class="sxs-lookup"><span data-stu-id="4f0be-154">Principal type (from tblPrincipalType table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-155">prinPoolID</span><span class="sxs-lookup"><span data-stu-id="4f0be-155">prinPoolID</span></span></p></td>
<td><p><span data-ttu-id="4f0be-156">ENT</span><span class="sxs-lookup"><span data-stu-id="4f0be-156">Int</span></span></p></td>
<td><p><span data-ttu-id="4f0be-157">Asignación de grupo de Lync para la entidad de identidad.</span><span class="sxs-lookup"><span data-stu-id="4f0be-157">Lync pool assignment for the principal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-158">prinPolicyID</span><span class="sxs-lookup"><span data-stu-id="4f0be-158">prinPolicyID</span></span></p></td>
<td><p><span data-ttu-id="4f0be-159">ENT</span><span class="sxs-lookup"><span data-stu-id="4f0be-159">Int</span></span></p></td>
<td><p><span data-ttu-id="4f0be-160">Valor de la Directiva del servidor de chat persistente para usuario, si la Directiva de tipo de etiqueta está presente.</span><span class="sxs-lookup"><span data-stu-id="4f0be-160">Persistent Chat Server policy value for user, if tag type policy is present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-161">prinAddedBy</span><span class="sxs-lookup"><span data-stu-id="4f0be-161">prinAddedBy</span></span></p></td>
<td><p><span data-ttu-id="4f0be-162">int</span><span class="sxs-lookup"><span data-stu-id="4f0be-162">int</span></span></p></td>
<td><p><span data-ttu-id="4f0be-163">IDENTIFICADOR principal del creador.</span><span class="sxs-lookup"><span data-stu-id="4f0be-163">Principal ID of the creator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-164">prinAddedOn</span><span class="sxs-lookup"><span data-stu-id="4f0be-164">prinAddedOn</span></span></p></td>
<td><p><span data-ttu-id="4f0be-165">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="4f0be-165">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="4f0be-166">Marca de tiempo de la hora de creación.</span><span class="sxs-lookup"><span data-stu-id="4f0be-166">Time stamp for the creation time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-167">prinUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="4f0be-167">prinUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="4f0be-168">int</span><span class="sxs-lookup"><span data-stu-id="4f0be-168">int</span></span></p></td>
<td><p><span data-ttu-id="4f0be-169">IDENTIFICADOR de la entidad de identidad que la actualizó por última vez.</span><span class="sxs-lookup"><span data-stu-id="4f0be-169">ID of the principal that last updated this.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-170">prinUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="4f0be-170">prinUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="4f0be-171">BIGINT, not null</span><span class="sxs-lookup"><span data-stu-id="4f0be-171">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="4f0be-172">Marca de tiempo de la última actualización.</span><span class="sxs-lookup"><span data-stu-id="4f0be-172">Time stamp for the last update.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-173">prinVerifiedOn</span><span class="sxs-lookup"><span data-stu-id="4f0be-173">prinVerifiedOn</span></span></p></td>
<td><p><span data-ttu-id="4f0be-174">DateTime, not null</span><span class="sxs-lookup"><span data-stu-id="4f0be-174">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="4f0be-175">Fecha y hora de la última actualización de sincronización de Active Directory para la entidad de identidad.</span><span class="sxs-lookup"><span data-stu-id="4f0be-175">Date and time of the last Active Directory Sync refresh for the principal.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="4f0be-176">Sus</span><span class="sxs-lookup"><span data-stu-id="4f0be-176">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f0be-177">Columna</span><span class="sxs-lookup"><span data-stu-id="4f0be-177">Column</span></span></th>
<th><span data-ttu-id="4f0be-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f0be-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f0be-179">prinID</span><span class="sxs-lookup"><span data-stu-id="4f0be-179">prinID</span></span></p></td>
<td><p><span data-ttu-id="4f0be-180">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="4f0be-180">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f0be-181">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="4f0be-181">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="4f0be-182">Clave externa con la búsqueda en la tabla tblPrincipalType. ptypeID.</span><span class="sxs-lookup"><span data-stu-id="4f0be-182">Foreign key with lookup in tblPrincipalType.ptypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4f0be-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4f0be-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

