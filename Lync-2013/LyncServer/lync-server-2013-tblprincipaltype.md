---
title: 'Lync Server 2013: tblPrincipalType'
description: 'Lync Server 2013: tblPrincipalType'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalType
ms:assetid: 32e1c1d6-80f4-4624-bf4e-b4c77d3982fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558633(v=OCS.15)
ms:contentKeyID: 48183787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba0f607d4499b54b16d7ecf8a4e7de603e874788
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398075"
---
# <a name="tblprincipaltype-in-lync-server-2013"></a><span data-ttu-id="af567-103">tblPrincipalType en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af567-103">tblPrincipalType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af567-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af567-104">

<span> </span></span></span>

<span data-ttu-id="af567-105">_**Última modificación del tema:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="af567-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="af567-106">tblPrincipalType contiene tipos de principales para categorizar lo que hay en la tabla tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="af567-106">tblPrincipalType contains principal types to categorize what is in the tblPrincipal table.</span></span>

### <a name="columns"></a><span data-ttu-id="af567-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="af567-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af567-108">Columna</span><span class="sxs-lookup"><span data-stu-id="af567-108">Column</span></span></th>
<th><span data-ttu-id="af567-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="af567-109">Type</span></span></th>
<th><span data-ttu-id="af567-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="af567-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af567-111">ptypeID</span><span class="sxs-lookup"><span data-stu-id="af567-111">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="af567-112">smallint, not null</span><span class="sxs-lookup"><span data-stu-id="af567-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="af567-113">IDENTIFICADOR de tipo de entidad de identidad.</span><span class="sxs-lookup"><span data-stu-id="af567-113">Principal type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af567-114">ptypeDesc</span><span class="sxs-lookup"><span data-stu-id="af567-114">ptypeDesc</span></span></p></td>
<td><p><span data-ttu-id="af567-115">nvarchar (256), not null</span><span class="sxs-lookup"><span data-stu-id="af567-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="af567-116">Descripción del tipo.</span><span class="sxs-lookup"><span data-stu-id="af567-116">Description of the type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af567-117">ptypeIsSystemUser</span><span class="sxs-lookup"><span data-stu-id="af567-117">ptypeIsSystemUser</span></span></p></td>
<td><p><span data-ttu-id="af567-118">bit, not null</span><span class="sxs-lookup"><span data-stu-id="af567-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="af567-119">True si el tipo corresponde a las entidades de identidad que se usan para fines internos.</span><span class="sxs-lookup"><span data-stu-id="af567-119">True if the type corresponds to the principals that are used for internal purposes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af567-120">ptypeIsUser</span><span class="sxs-lookup"><span data-stu-id="af567-120">ptypeIsUser</span></span></p></td>
<td><p><span data-ttu-id="af567-121">bit, not null</span><span class="sxs-lookup"><span data-stu-id="af567-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="af567-122">True si el tipo es un tipo de usuario.</span><span class="sxs-lookup"><span data-stu-id="af567-122">True if the type is a user type.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="af567-123">Clave</span><span class="sxs-lookup"><span data-stu-id="af567-123">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af567-124">Columna</span><span class="sxs-lookup"><span data-stu-id="af567-124">Column</span></span></th>
<th><span data-ttu-id="af567-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="af567-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af567-126">ptypeID</span><span class="sxs-lookup"><span data-stu-id="af567-126">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="af567-127">Clave principal.</span><span class="sxs-lookup"><span data-stu-id="af567-127">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="principal-values"></a><span data-ttu-id="af567-128">Valores principales</span><span class="sxs-lookup"><span data-stu-id="af567-128">Principal Values</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af567-129">ID</span><span class="sxs-lookup"><span data-stu-id="af567-129">ID</span></span></th>
<th><span data-ttu-id="af567-130">Rol</span><span class="sxs-lookup"><span data-stu-id="af567-130">Role</span></span></th>
<th><span data-ttu-id="af567-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="af567-131">Description</span></span></th>
<th><span data-ttu-id="af567-132">Usuario</span><span class="sxs-lookup"><span data-stu-id="af567-132">User</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af567-133">1</span><span class="sxs-lookup"><span data-stu-id="af567-133">1</span></span></p></td>
<td><p><span data-ttu-id="af567-134">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="af567-134">Any</span></span></p></td>
<td><p><span data-ttu-id="af567-135">Entidad de identidad genérica con un tipo no conocido.</span><span class="sxs-lookup"><span data-stu-id="af567-135">Generic principal with no known type.</span></span> <span data-ttu-id="af567-136">No se usa en la tabla tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="af567-136">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af567-137">2</span><span class="sxs-lookup"><span data-stu-id="af567-137">2</span></span></p></td>
<td><p><span data-ttu-id="af567-138">AnyUser</span><span class="sxs-lookup"><span data-stu-id="af567-138">AnyUser</span></span></p></td>
<td><p><span data-ttu-id="af567-139">Identidad genérica del tipo de usuario.</span><span class="sxs-lookup"><span data-stu-id="af567-139">Generic principal of user type.</span></span> <span data-ttu-id="af567-140">No se usa en la tabla tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="af567-140">Not used in tblPrincipal table.</span></span></p></td>
<td><p><span data-ttu-id="af567-141">Sí</span><span class="sxs-lookup"><span data-stu-id="af567-141">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af567-142">3</span><span class="sxs-lookup"><span data-stu-id="af567-142">3</span></span></p></td>
<td><p><span data-ttu-id="af567-143">AnyGroup</span><span class="sxs-lookup"><span data-stu-id="af567-143">AnyGroup</span></span></p></td>
<td><p><span data-ttu-id="af567-144">Principal genérico con semántica de grupo.</span><span class="sxs-lookup"><span data-stu-id="af567-144">Generic principal with group semantic.</span></span> <span data-ttu-id="af567-145">No se usa en la tabla tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="af567-145">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af567-146">4</span><span class="sxs-lookup"><span data-stu-id="af567-146">4</span></span></p></td>
<td><p><span data-ttu-id="af567-147">SystemUser</span><span class="sxs-lookup"><span data-stu-id="af567-147">SystemUser</span></span></p></td>
<td><p><span data-ttu-id="af567-148">Principal utilizado internamente por el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="af567-148">Principal used internally by Persistent Chat Server.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af567-149">5</span><span class="sxs-lookup"><span data-stu-id="af567-149">5</span></span></p></td>
<td><p><span data-ttu-id="af567-150">Usuario</span><span class="sxs-lookup"><span data-stu-id="af567-150">User</span></span></p></td>
<td><p><span data-ttu-id="af567-151">Usuario normal.</span><span class="sxs-lookup"><span data-stu-id="af567-151">Regular user.</span></span></p></td>
<td><p><span data-ttu-id="af567-152">Sí</span><span class="sxs-lookup"><span data-stu-id="af567-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af567-153">4,8</span><span class="sxs-lookup"><span data-stu-id="af567-153">8</span></span></p></td>
<td><p><span data-ttu-id="af567-154">Clona</span><span class="sxs-lookup"><span data-stu-id="af567-154">DC</span></span></p></td>
<td><p><span data-ttu-id="af567-155">Controlador de dominio de servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="af567-155">Active Directory Domain Services domain controller.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af567-156">99,999</span><span class="sxs-lookup"><span data-stu-id="af567-156">9</span></span></p></td>
<td><p><span data-ttu-id="af567-157">Mesa</span><span class="sxs-lookup"><span data-stu-id="af567-157">Group</span></span></p></td>
<td><p><span data-ttu-id="af567-158">Grupo de seguridad de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="af567-158">Active Directory security group.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af567-159">base10</span><span class="sxs-lookup"><span data-stu-id="af567-159">10</span></span></p></td>
<td><p><span data-ttu-id="af567-160">Carpeta</span><span class="sxs-lookup"><span data-stu-id="af567-160">Folder</span></span></p></td>
<td><p><span data-ttu-id="af567-161">Contenedor de Active Directory o unidad de organización.</span><span class="sxs-lookup"><span data-stu-id="af567-161">Active Directory container or organizational unit.</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="af567-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="af567-162">See Also</span></span>


[<span data-ttu-id="af567-163">tblPrincipal enn Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af567-163">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)  
  

<span data-ttu-id="af567-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af567-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

