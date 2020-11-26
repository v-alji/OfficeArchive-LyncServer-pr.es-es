---
title: 'Lync Server 2013: cambios realizados por Grant-CsSetupPermission'
description: 'Lync Server 2013: cambios realizados por Grant-CsSetupPermission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsSetupPermission
ms:assetid: c5801f48-14e3-4fdd-8f14-d52e7af07a57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205250(v=OCS.15)
ms:contentKeyID: 48185360
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2a9156c977c993dd32e38fc6816bd08d3f65c1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435071"
---
# <a name="changes-made-by-grant-cssetuppermission-in-lync-server-2013"></a><span data-ttu-id="46acd-103">Cambios realizados por Grant-CsSetupPermission en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46acd-103">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46acd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46acd-104">

<span> </span></span></span>

<span data-ttu-id="46acd-105">_**Última modificación del tema:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="46acd-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="46acd-106">Para delegar la configuración, puede conceder permisos al grupo universal RTCUniversalServerAdmins de una unidad organizativa de Active Directory específica, lo que permite a los miembros del grupo RTCUniversalServerAdmins de esa OU instalar Lync Server 2013 en el dominio especificado sin ser miembros del grupo administradores de dominio.</span><span class="sxs-lookup"><span data-stu-id="46acd-106">To delegate setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="46acd-107">El cmdlet **Grant-CsSetupPermission** concede los permisos de grupo RTCUniversalServerAdmins en una unidad organizativa, como se especifica en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="46acd-107">The **Grant-CsSetupPermission** cmdlet grants the RTCUniversalServerAdmins group permissions on an OU, as specified in the following table:</span></span>

### <a name="permissions-granted-to-objects-in-the-ou"></a><span data-ttu-id="46acd-108">Permisos otorgados a objetos de la OU</span><span class="sxs-lookup"><span data-stu-id="46acd-108">Permissions granted to Objects in the OU</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46acd-109">Los permisos se aplican a:</span><span class="sxs-lookup"><span data-stu-id="46acd-109">Permissions apply to:</span></span></th>
<th><span data-ttu-id="46acd-110">Los permisos concedidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="46acd-110">Permissions granted are:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46acd-111">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="46acd-111">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="46acd-112">Acceso especial:</span><span class="sxs-lookup"><span data-stu-id="46acd-112">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-113">Leer servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="46acd-113">Read servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="46acd-114">Escribir servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="46acd-114">Write servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="46acd-115">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="46acd-115">Delete tree</span></span></p></li>
<li><p><span data-ttu-id="46acd-116">Replicar cambios de directorio</span><span class="sxs-lookup"><span data-stu-id="46acd-116">Replicating directory changes</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46acd-117">Objetos serviceConnectionPoint descendientes</span><span class="sxs-lookup"><span data-stu-id="46acd-117">Descendant serviceConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="46acd-118">Acceso especial:</span><span class="sxs-lookup"><span data-stu-id="46acd-118">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-119">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-119">Read permissions</span></span></p></li>
<li><p><span data-ttu-id="46acd-120">Permisos de escritura</span><span class="sxs-lookup"><span data-stu-id="46acd-120">Write permissions</span></span></p></li>
<li><p><span data-ttu-id="46acd-121">Crear elemento secundario</span><span class="sxs-lookup"><span data-stu-id="46acd-121">Create child</span></span></p></li>
<li><p><span data-ttu-id="46acd-122">Eliminar hijo</span><span class="sxs-lookup"><span data-stu-id="46acd-122">Delete child</span></span></p></li>
<li><p><span data-ttu-id="46acd-123">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="46acd-123">List contents</span></span></p></li>
<li><p><span data-ttu-id="46acd-124">Write (propiedad)</span><span class="sxs-lookup"><span data-stu-id="46acd-124">Write property</span></span></p></li>
<li><p><span data-ttu-id="46acd-125">Propiedad de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-125">Read property</span></span></p></li>
<li><p><span data-ttu-id="46acd-126">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="46acd-126">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46acd-127">Objetos descendientes msRTCSIP-Server</span><span class="sxs-lookup"><span data-stu-id="46acd-127">Descendant msRTCSIP-Server objects</span></span></p></td>
<td><p><span data-ttu-id="46acd-128">Acceso especial:</span><span class="sxs-lookup"><span data-stu-id="46acd-128">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-129">Write (propiedad)</span><span class="sxs-lookup"><span data-stu-id="46acd-129">Write property</span></span></p></li>
<li><p><span data-ttu-id="46acd-130">Propiedad de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-130">Read property</span></span></p></li>
<li><p><span data-ttu-id="46acd-131">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="46acd-131">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46acd-132">Objetos descendientes msRTCSIP-webcomponents</span><span class="sxs-lookup"><span data-stu-id="46acd-132">Descendant msRTCSIP-WebComponents objects</span></span></p></td>
<td><p><span data-ttu-id="46acd-133">Acceso especial:</span><span class="sxs-lookup"><span data-stu-id="46acd-133">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-134">Write (propiedad)</span><span class="sxs-lookup"><span data-stu-id="46acd-134">Write property</span></span></p></li>
<li><p><span data-ttu-id="46acd-135">Propiedad de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-135">Read property</span></span></p></li>
<li><p><span data-ttu-id="46acd-136">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="46acd-136">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46acd-137">Objetos descendientes msRTCSIP-MCU</span><span class="sxs-lookup"><span data-stu-id="46acd-137">Descendant msRTCSIP-MCU objects</span></span></p></td>
<td><p><span data-ttu-id="46acd-138">Acceso especial:</span><span class="sxs-lookup"><span data-stu-id="46acd-138">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-139">Write (propiedad)</span><span class="sxs-lookup"><span data-stu-id="46acd-139">Write property</span></span></p></li>
<li><p><span data-ttu-id="46acd-140">Propiedad de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-140">Read property</span></span></p></li>
<li><p><span data-ttu-id="46acd-141">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="46acd-141">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46acd-142">Objetos descendientes msRTCSIP-MediationServer</span><span class="sxs-lookup"><span data-stu-id="46acd-142">Descendant msRTCSIP-MediationServer objects</span></span></p></td>
<td><p><span data-ttu-id="46acd-143">Acceso especial:</span><span class="sxs-lookup"><span data-stu-id="46acd-143">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-144">Write (propiedad)</span><span class="sxs-lookup"><span data-stu-id="46acd-144">Write property</span></span></p></li>
<li><p><span data-ttu-id="46acd-145">Propiedad de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-145">Read property</span></span></p></li>
<li><p><span data-ttu-id="46acd-146">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="46acd-146">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46acd-147">Objetos descendientes msRTCSIP-ApplicationServer</span><span class="sxs-lookup"><span data-stu-id="46acd-147">Descendant msRTCSIP-ApplicationServer objects</span></span></p></td>
<td><p><span data-ttu-id="46acd-148">Acceso especial:</span><span class="sxs-lookup"><span data-stu-id="46acd-148">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-149">Write (propiedad)</span><span class="sxs-lookup"><span data-stu-id="46acd-149">Write property</span></span></p></li>
<li><p><span data-ttu-id="46acd-150">Propiedad de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-150">Read property</span></span></p></li>
<li><p><span data-ttu-id="46acd-151">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="46acd-151">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46acd-152">Objetos descendientes msRTCSIP-punto de la</span><span class="sxs-lookup"><span data-stu-id="46acd-152">Descendant msRTCSIP-ConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="46acd-153">Acceso especial:</span><span class="sxs-lookup"><span data-stu-id="46acd-153">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-154">Write (propiedad)</span><span class="sxs-lookup"><span data-stu-id="46acd-154">Write property</span></span></p></li>
<li><p><span data-ttu-id="46acd-155">Propiedad de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-155">Read property</span></span></p></li>
<li><p><span data-ttu-id="46acd-156">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="46acd-156">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46acd-157">Objetos de equipo descendientes</span><span class="sxs-lookup"><span data-stu-id="46acd-157">Descendant Computer objects</span></span></p></td>
<td><p><span data-ttu-id="46acd-158">Acceso especial para serviceConnectionPoint:</span><span class="sxs-lookup"><span data-stu-id="46acd-158">Special access for serviceConnectionPoint:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-159">Crear objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="46acd-159">Create child objects</span></span></p></li>
<li><p><span data-ttu-id="46acd-160">Eliminar objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="46acd-160">Delete child objects</span></span></p></li>
<li><p><span data-ttu-id="46acd-161">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="46acd-161">Delete tree</span></span></p></li>
</ul>
<p><span data-ttu-id="46acd-162">Acceso especial para información pública:</span><span class="sxs-lookup"><span data-stu-id="46acd-162">Special access for public information:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-163">Propiedad de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-163">Read property</span></span></p></li>
</ul>
<p><span data-ttu-id="46acd-164">Acceso especial para el nombre de host DNS:</span><span class="sxs-lookup"><span data-stu-id="46acd-164">Special access for DNS host name:</span></span></p>
<ul>
<li><p><span data-ttu-id="46acd-165">Propiedad de lectura</span><span class="sxs-lookup"><span data-stu-id="46acd-165">Read property</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="46acd-166">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46acd-166">


</div>

<span> </span>

</div>

</div>

</span></span></div>

