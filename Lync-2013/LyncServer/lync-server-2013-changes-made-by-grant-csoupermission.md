---
title: 'Lync Server 2013: cambios realizados por Grant-CsOUPermission'
description: 'Lync Server 2013: cambios realizados por Grant-CsOUPermission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsOUPermission
ms:assetid: d744d352-1ad9-4447-8e2b-28e768d2ed1b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205310(v=OCS.15)
ms:contentKeyID: 48185564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10d3db0e9dde380628690bc016e2b4bd2ec85b54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435057"
---
# <a name="changes-made-by-grant-csoupermission-in-lync-server-2013"></a><span data-ttu-id="5b20d-103">Cambios realizados por Grant-CsOUPermission en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b20d-103">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b20d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b20d-104">

<span> </span></span></span>

<span data-ttu-id="5b20d-105">_**Última modificación del tema:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="5b20d-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="5b20d-106">Para delegar la administración de Lync Server 2013, puede Agregar permisos a unidades organizativas (OU) especificadas de modo que los miembros de los grupos RTC universales creados por la preparación del bosque puedan tener acceso a las unidades organizativas sin ser miembros del grupo administradores de dominio.</span><span class="sxs-lookup"><span data-stu-id="5b20d-106">To delegate Lync Server 2013 administration, you can add permissions to specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access the OUs without being members of the Domain Admins group.</span></span>

<span data-ttu-id="5b20d-107">El cmdlet **Grant-CsOuPermission** otorga permisos a objetos en la ou especificada, tal como se especifica en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="5b20d-107">The **Grant-CsOuPermission** cmdlet grants permissions to objects in the specified OU as specified in the following tables.</span></span>

<div>

## <a name="granting-permission-for-user-objects"></a><span data-ttu-id="5b20d-108">Conceder permisos a los objetos de usuario</span><span class="sxs-lookup"><span data-stu-id="5b20d-108">Granting Permission for User Objects</span></span>

<span data-ttu-id="5b20d-109">Al ejecutar el cmdlet **Grant-CsOuPermission** para objetos de usuario en una unidad organizativa, se conceden permisos a los grupos como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b20d-109">When you run the **Grant-CsOuPermission** cmdlet for User objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-user-objects"></a><span data-ttu-id="5b20d-110">Permisos otorgados para objetos de usuario</span><span class="sxs-lookup"><span data-stu-id="5b20d-110">Permissions Granted for User Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b20d-111">Mesa</span><span class="sxs-lookup"><span data-stu-id="5b20d-111">Group</span></span></th>
<th><span data-ttu-id="5b20d-112">Permiso</span><span class="sxs-lookup"><span data-stu-id="5b20d-112">Permission</span></span></th>
<th><span data-ttu-id="5b20d-113">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="5b20d-113">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-114">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="5b20d-114">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="5b20d-115">Replicar cambios de directorio</span><span class="sxs-lookup"><span data-stu-id="5b20d-115">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="5b20d-116">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-116">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-117">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-117">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-118">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-118">List contents</span></span></p>
<p><span data-ttu-id="5b20d-119">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-119">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-120">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-120">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-121">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-121">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-122">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-122">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-123">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-123">List contents</span></span></p>
<p><span data-ttu-id="5b20d-124">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-124">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-125">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-125">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-126">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-126">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-127">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-127">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-128">Leer RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-128">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-129">Leer RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-129">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-130">Leer RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-130">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-131">Public-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-131">Read Public-Information</span></span></p>
<p><span data-ttu-id="5b20d-132">General-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-132">Read General-Information</span></span></p>
<p><span data-ttu-id="5b20d-133">Leer las restricciones de la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="5b20d-133">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-134">Objetos de usuario descendientes</span><span class="sxs-lookup"><span data-stu-id="5b20d-134">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-135">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="5b20d-135">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="5b20d-136">Escribir RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-136">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-137">Escribir msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="5b20d-137">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="5b20d-138">Escribir RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-138">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-139">Escribir RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-139">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-140">Escribir proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="5b20d-140">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="5b20d-141">Objetos de usuario descendientes</span><span class="sxs-lookup"><span data-stu-id="5b20d-141">Descendant User objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-computer-objects"></a><span data-ttu-id="5b20d-142">Concesión de permisos para objetos de equipo</span><span class="sxs-lookup"><span data-stu-id="5b20d-142">Granting Permission for Computer Objects</span></span>

<span data-ttu-id="5b20d-143">Al ejecutar el cmdlet **Grant-CsOuPermission** para objetos de equipo en una unidad organizativa, se conceden permisos a los grupos como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b20d-143">When you run the **Grant-CsOuPermission** cmdlet for Computer objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-computer-objects"></a><span data-ttu-id="5b20d-144">Permisos otorgados para objetos de equipo</span><span class="sxs-lookup"><span data-stu-id="5b20d-144">Permissions Granted for Computer Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b20d-145">Mesa</span><span class="sxs-lookup"><span data-stu-id="5b20d-145">Group</span></span></th>
<th><span data-ttu-id="5b20d-146">Permiso</span><span class="sxs-lookup"><span data-stu-id="5b20d-146">Permission</span></span></th>
<th><span data-ttu-id="5b20d-147">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="5b20d-147">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-148">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="5b20d-148">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="5b20d-149">Replicar cambios de directorio</span><span class="sxs-lookup"><span data-stu-id="5b20d-149">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="5b20d-150">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-150">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-151">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-151">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-152">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-152">List contents</span></span></p>
<p><span data-ttu-id="5b20d-153">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-153">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-154">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-154">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-155">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-155">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-156">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-156">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-157">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-157">List contents</span></span></p>
<p><span data-ttu-id="5b20d-158">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-158">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-159">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-159">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-160">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-160">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-161">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-161">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-162">Public-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-162">Read Public-Information</span></span></p>
<p><span data-ttu-id="5b20d-163">Lectura validada: nombre-DNS-host</span><span class="sxs-lookup"><span data-stu-id="5b20d-163">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="5b20d-164">Objetos de equipo descendientes</span><span class="sxs-lookup"><span data-stu-id="5b20d-164">Descendant Computer objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-165">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="5b20d-165">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="5b20d-166">Public-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-166">Read Public-Information</span></span></p>
<p><span data-ttu-id="5b20d-167">Lectura validada: nombre-DNS-host</span><span class="sxs-lookup"><span data-stu-id="5b20d-167">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="5b20d-168">Objetos de equipo descendientes</span><span class="sxs-lookup"><span data-stu-id="5b20d-168">Descendant Computer objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-contact-or-appcontact-objects"></a><span data-ttu-id="5b20d-169">Concesión de permisos para objetos de contacto o de AppContact</span><span class="sxs-lookup"><span data-stu-id="5b20d-169">Granting Permission for Contact or AppContact Objects</span></span>

<span data-ttu-id="5b20d-170">Al ejecutar el cmdlet **Grant-CsOuPermission** para objetos de contacto o objetos de AppContact en una unidad organizativa, se conceden permisos a los grupos como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b20d-170">When you run the **Grant-CsOuPermission** cmdlet for Contact objects or AppContact objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-contact-or-appcontact-objects"></a><span data-ttu-id="5b20d-171">Permisos concedidos para objetos de contacto o AppContact</span><span class="sxs-lookup"><span data-stu-id="5b20d-171">Permissions Granted for Contact or AppContact Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b20d-172">Mesa</span><span class="sxs-lookup"><span data-stu-id="5b20d-172">Group</span></span></th>
<th><span data-ttu-id="5b20d-173">Permiso</span><span class="sxs-lookup"><span data-stu-id="5b20d-173">Permission</span></span></th>
<th><span data-ttu-id="5b20d-174">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="5b20d-174">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-175">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="5b20d-175">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="5b20d-176">Replicar cambios de directorio</span><span class="sxs-lookup"><span data-stu-id="5b20d-176">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="5b20d-177">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-177">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-178">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-178">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-179">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-179">List contents</span></span></p>
<p><span data-ttu-id="5b20d-180">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-180">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-181">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-181">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-182">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-182">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-183">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-183">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-184">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-184">List contents</span></span></p>
<p><span data-ttu-id="5b20d-185">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-185">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-186">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-186">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-187">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-187">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-188">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-188">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-189">Leer RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-189">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-190">Leer RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-190">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-191">Leer RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-191">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-192">Public-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-192">Read Public-Information</span></span></p>
<p><span data-ttu-id="5b20d-193">General-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-193">Read General-Information</span></span></p>
<p><span data-ttu-id="5b20d-194">Personal-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-194">Read Personal-Information</span></span></p>
<p><span data-ttu-id="5b20d-195">Leer las restricciones de la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="5b20d-195">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-196">Objetos de contacto descendiente</span><span class="sxs-lookup"><span data-stu-id="5b20d-196">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-197">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="5b20d-197">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="5b20d-198">Escribir RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-198">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-199">Escribir otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="5b20d-199">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="5b20d-200">Escribir displayName</span><span class="sxs-lookup"><span data-stu-id="5b20d-200">Write displayName</span></span></p>
<p><span data-ttu-id="5b20d-201">Escribir Descripción</span><span class="sxs-lookup"><span data-stu-id="5b20d-201">Write description</span></span></p>
<p><span data-ttu-id="5b20d-202">Escribir telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="5b20d-202">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="5b20d-203">Escribir msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="5b20d-203">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="5b20d-204">Escribir RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-204">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-205">Escribir RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-205">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-206">Escribir proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="5b20d-206">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="5b20d-207">Objetos de contacto descendiente</span><span class="sxs-lookup"><span data-stu-id="5b20d-207">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-device-objects"></a><span data-ttu-id="5b20d-208">Conceder permisos a objetos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5b20d-208">Granting Permission for Device Objects</span></span>

<span data-ttu-id="5b20d-209">Al ejecutar el cmdlet **Grant-CsOuPermission** en una unidad organizativa, se conceden permisos a los grupos, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b20d-209">When you run the **Grant-CsOuPermission** cmdlet for Device objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-device-objects"></a><span data-ttu-id="5b20d-210">Permisos concedidos para objetos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5b20d-210">Permissions Granted for Device Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b20d-211">Mesa</span><span class="sxs-lookup"><span data-stu-id="5b20d-211">Group</span></span></th>
<th><span data-ttu-id="5b20d-212">Permiso</span><span class="sxs-lookup"><span data-stu-id="5b20d-212">Permission</span></span></th>
<th><span data-ttu-id="5b20d-213">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="5b20d-213">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-214">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="5b20d-214">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="5b20d-215">Replicar cambios de directorio</span><span class="sxs-lookup"><span data-stu-id="5b20d-215">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="5b20d-216">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-216">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-217">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-217">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-218">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-218">List contents</span></span></p>
<p><span data-ttu-id="5b20d-219">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-219">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-220">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-220">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-221">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-221">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-222">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-222">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-223">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-223">List contents</span></span></p>
<p><span data-ttu-id="5b20d-224">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-224">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-225">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-225">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-226">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-226">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-227">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-227">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-228">Leer RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-228">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-229">Leer RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-229">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-230">Leer RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-230">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-231">Public-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-231">Read Public-Information</span></span></p>
<p><span data-ttu-id="5b20d-232">Personal-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-232">Read Personal-Information</span></span></p>
<p><span data-ttu-id="5b20d-233">General-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-233">Read General-Information</span></span></p>
<p><span data-ttu-id="5b20d-234">Leer las restricciones de la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="5b20d-234">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-235">Objetos de contacto descendiente</span><span class="sxs-lookup"><span data-stu-id="5b20d-235">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-236">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="5b20d-236">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="5b20d-237">Crear elemento secundario</span><span class="sxs-lookup"><span data-stu-id="5b20d-237">Create child</span></span></p>
<p><span data-ttu-id="5b20d-238">Eliminar hijo</span><span class="sxs-lookup"><span data-stu-id="5b20d-238">Delete child</span></span></p>
<p><span data-ttu-id="5b20d-239">Eliminar árbol</span><span class="sxs-lookup"><span data-stu-id="5b20d-239">Delete tree</span></span></p></td>
<td><p><span data-ttu-id="5b20d-240">Con</span><span class="sxs-lookup"><span data-stu-id="5b20d-240">Contact</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-241">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="5b20d-241">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="5b20d-242">Escribir displayName</span><span class="sxs-lookup"><span data-stu-id="5b20d-242">Write displayName</span></span></p>
<p><span data-ttu-id="5b20d-243">Escribir Descripción</span><span class="sxs-lookup"><span data-stu-id="5b20d-243">Write description</span></span></p>
<p><span data-ttu-id="5b20d-244">Escribir telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="5b20d-244">Write telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="5b20d-245">Objetos de usuario descendientes</span><span class="sxs-lookup"><span data-stu-id="5b20d-245">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-246">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="5b20d-246">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="5b20d-247">Escribir RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-247">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-248">Escribir otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="5b20d-248">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="5b20d-249">Escribir displayName</span><span class="sxs-lookup"><span data-stu-id="5b20d-249">Write displayName</span></span></p>
<p><span data-ttu-id="5b20d-250">Escribir Descripción</span><span class="sxs-lookup"><span data-stu-id="5b20d-250">Write description</span></span></p>
<p><span data-ttu-id="5b20d-251">Escribir telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="5b20d-251">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="5b20d-252">Escribir msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="5b20d-252">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="5b20d-253">Escribir RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-253">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-254">Escribir RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-254">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-255">Escribir proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="5b20d-255">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="5b20d-256">Objetos de contacto descendiente</span><span class="sxs-lookup"><span data-stu-id="5b20d-256">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-inetorgperson-objects"></a><span data-ttu-id="5b20d-257">Conceder permisos a objetos InetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="5b20d-257">Granting Permission for InetOrgPerson Objects</span></span>

<span data-ttu-id="5b20d-258">Al ejecutar el cmdlet **Grant-CsOuPermission** para los objetos InetOrgPerson de una unidad organizativa, se conceden permisos a los grupos como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b20d-258">When you run the **Grant-CsOuPermission** cmdlet for InetOrgPerson objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-inetorgperson-objects"></a><span data-ttu-id="5b20d-259">Permisos otorgados a los objetos InetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="5b20d-259">Permissions Granted for InetOrgPerson Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b20d-260">Mesa</span><span class="sxs-lookup"><span data-stu-id="5b20d-260">Group</span></span></th>
<th><span data-ttu-id="5b20d-261">Permiso</span><span class="sxs-lookup"><span data-stu-id="5b20d-261">Permission</span></span></th>
<th><span data-ttu-id="5b20d-262">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="5b20d-262">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-263">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="5b20d-263">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="5b20d-264">Replicar cambios de directorio</span><span class="sxs-lookup"><span data-stu-id="5b20d-264">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="5b20d-265">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-265">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-266">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-266">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-267">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-267">List contents</span></span></p>
<p><span data-ttu-id="5b20d-268">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-268">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-269">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-269">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-270">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-270">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-271">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-271">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-272">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="5b20d-272">List contents</span></span></p>
<p><span data-ttu-id="5b20d-273">Leer todas las propiedades</span><span class="sxs-lookup"><span data-stu-id="5b20d-273">Read all properties</span></span></p>
<p><span data-ttu-id="5b20d-274">Permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-274">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-275">Solo este objeto</span><span class="sxs-lookup"><span data-stu-id="5b20d-275">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b20d-276">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="5b20d-276">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="5b20d-277">Leer RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-277">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-278">Leer RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-278">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-279">Leer RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-279">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-280">Personal-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-280">Read Personal-Information</span></span></p>
<p><span data-ttu-id="5b20d-281">Public-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-281">Read Public-Information</span></span></p>
<p><span data-ttu-id="5b20d-282">General-Information de lectura</span><span class="sxs-lookup"><span data-stu-id="5b20d-282">Read General-Information</span></span></p>
<p><span data-ttu-id="5b20d-283">Leer las restricciones de la cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="5b20d-283">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="5b20d-284">Objetos descendientes de inetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="5b20d-284">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b20d-285">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="5b20d-285">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="5b20d-286">Escribir RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-286">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-287">Escribir RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-287">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-288">Escribir RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="5b20d-288">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="5b20d-289">Escribir proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="5b20d-289">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="5b20d-290">Objetos descendientes de inetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="5b20d-290">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5b20d-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b20d-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

