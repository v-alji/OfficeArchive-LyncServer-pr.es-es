---
title: 'Lync Server 2013: cambios realizados por la preparación del dominio'
description: 'Lync Server 2013: cambios realizados por la preparación del dominio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by domain preparation
ms:assetid: 9191221e-6166-4c2b-837e-fa73d90fdf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398742(v=OCS.15)
ms:contentKeyID: 48184845
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26400bd1c72c6ae3b8dc1f2d2d8f6c6906b80595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435120"
---
# <a name="changes-made-by-domain-preparation-in-lync-server-2013"></a><span data-ttu-id="7c018-103">Cambios realizados por la preparación del dominio en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c018-103">Changes made by domain preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7c018-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7c018-104">

<span> </span></span></span>

<span data-ttu-id="7c018-105">_**Última modificación del tema:** 2010-10-18_</span><span class="sxs-lookup"><span data-stu-id="7c018-105">_**Topic Last Modified:** 2010-10-18_</span></span>

<span data-ttu-id="7c018-106">En la siguiente tabla se enumeran las entradas de control de acceso (ACE) que crea la preparación del dominio en la raíz del dominio.</span><span class="sxs-lookup"><span data-stu-id="7c018-106">The following table lists the access control entries (ACEs) that domain preparation creates on the domain root.</span></span> <span data-ttu-id="7c018-107">A menos que se indique lo contrario, se heredan todas las ACE.</span><span class="sxs-lookup"><span data-stu-id="7c018-107">All ACEs are inherited unless otherwise noted.</span></span>

<div id="sectionSection0" class="section">

### <a name="aces-added-to-domain-root"></a><span data-ttu-id="7c018-108">Entradas ACE agregadas a la raíz del dominio</span><span class="sxs-lookup"><span data-stu-id="7c018-108">ACEs Added to Domain Root</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c018-109">ENTRADA</span><span class="sxs-lookup"><span data-stu-id="7c018-109">ACE</span></span></th>
<th><span data-ttu-id="7c018-110">RTCUniversal-UserReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="7c018-110">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="7c018-111">RTCUniversal-ServerReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="7c018-111">RTCUniversal-ServerReadOnly-Group</span></span></th>
<th><span data-ttu-id="7c018-112">RTCUniversal-UserAdmins</span><span class="sxs-lookup"><span data-stu-id="7c018-112">RTCUniversal-UserAdmins</span></span></th>
<th><span data-ttu-id="7c018-113">RTCHSUniversal-Services</span><span class="sxs-lookup"><span data-stu-id="7c018-113">RTCHSUniversal-Services</span></span></th>
<th><span data-ttu-id="7c018-114">Authenticated-Users</span><span class="sxs-lookup"><span data-stu-id="7c018-114">Authenticated-Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c018-115">Leer contenedor (no heredado)</span><span class="sxs-lookup"><span data-stu-id="7c018-115">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="7c018-116"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-116"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-117"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-117"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-118">No</span><span class="sxs-lookup"><span data-stu-id="7c018-118">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-119">No</span><span class="sxs-lookup"><span data-stu-id="7c018-119">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-120">No</span><span class="sxs-lookup"><span data-stu-id="7c018-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c018-121">Leer usuario de la PropertySet de la cuenta de usuario-restricciones</span><span class="sxs-lookup"><span data-stu-id="7c018-121">Read User PropertySet User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="7c018-122"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-122"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-123">No</span><span class="sxs-lookup"><span data-stu-id="7c018-123">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-124">No</span><span class="sxs-lookup"><span data-stu-id="7c018-124">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-125">No</span><span class="sxs-lookup"><span data-stu-id="7c018-125">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-126">No</span><span class="sxs-lookup"><span data-stu-id="7c018-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c018-127">Leer el Personal-Information de usuario PropertySet</span><span class="sxs-lookup"><span data-stu-id="7c018-127">Read User PropertySet Personal-Information</span></span></p></td>
<td><p><span data-ttu-id="7c018-128"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-128"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-129">No</span><span class="sxs-lookup"><span data-stu-id="7c018-129">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-130">No</span><span class="sxs-lookup"><span data-stu-id="7c018-130">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-131">No</span><span class="sxs-lookup"><span data-stu-id="7c018-131">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-132">No</span><span class="sxs-lookup"><span data-stu-id="7c018-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c018-133">Leer el General-Information de usuario PropertySet</span><span class="sxs-lookup"><span data-stu-id="7c018-133">Read User PropertySet General-Information</span></span></p></td>
<td><p><span data-ttu-id="7c018-134"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-134"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-135">No</span><span class="sxs-lookup"><span data-stu-id="7c018-135">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-136">No</span><span class="sxs-lookup"><span data-stu-id="7c018-136">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-137">No</span><span class="sxs-lookup"><span data-stu-id="7c018-137">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-138">No</span><span class="sxs-lookup"><span data-stu-id="7c018-138">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c018-139">Leer el Public-Information de usuario PropertySet</span><span class="sxs-lookup"><span data-stu-id="7c018-139">Read User PropertySet Public-Information</span></span></p></td>
<td><p><span data-ttu-id="7c018-140"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-140"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-141">No</span><span class="sxs-lookup"><span data-stu-id="7c018-141">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-142">No</span><span class="sxs-lookup"><span data-stu-id="7c018-142">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-143">No</span><span class="sxs-lookup"><span data-stu-id="7c018-143">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-144">No</span><span class="sxs-lookup"><span data-stu-id="7c018-144">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c018-145">Leer el RTCUserSearchProperty-Set de usuario PropertySet</span><span class="sxs-lookup"><span data-stu-id="7c018-145">Read User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="7c018-146"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-146"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-147">No</span><span class="sxs-lookup"><span data-stu-id="7c018-147">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-148">No</span><span class="sxs-lookup"><span data-stu-id="7c018-148">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-149">No</span><span class="sxs-lookup"><span data-stu-id="7c018-149">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-150"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-150"><strong>Yes</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c018-151">Leer el usuario PropertySet RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="7c018-151">Read User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="7c018-152"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-152"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-153">No</span><span class="sxs-lookup"><span data-stu-id="7c018-153">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-154">No</span><span class="sxs-lookup"><span data-stu-id="7c018-154">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-155">No</span><span class="sxs-lookup"><span data-stu-id="7c018-155">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-156">No</span><span class="sxs-lookup"><span data-stu-id="7c018-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c018-157">Proxy-Addresses de propiedad de usuario de escritura</span><span class="sxs-lookup"><span data-stu-id="7c018-157">Write User Property Proxy-Addresses</span></span></p></td>
<td><p><span data-ttu-id="7c018-158">No</span><span class="sxs-lookup"><span data-stu-id="7c018-158">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-159">No</span><span class="sxs-lookup"><span data-stu-id="7c018-159">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-160"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-160"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-161">No</span><span class="sxs-lookup"><span data-stu-id="7c018-161">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-162">No</span><span class="sxs-lookup"><span data-stu-id="7c018-162">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c018-163">Escribe el usuario PropertySet RTCUserSearchProperty-Set</span><span class="sxs-lookup"><span data-stu-id="7c018-163">Write User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="7c018-164">No</span><span class="sxs-lookup"><span data-stu-id="7c018-164">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-165">No</span><span class="sxs-lookup"><span data-stu-id="7c018-165">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-166"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-166"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-167">No</span><span class="sxs-lookup"><span data-stu-id="7c018-167">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-168">No</span><span class="sxs-lookup"><span data-stu-id="7c018-168">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c018-169">Escribir el usuario PropertySet RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="7c018-169">Write User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="7c018-170">No</span><span class="sxs-lookup"><span data-stu-id="7c018-170">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-171">No</span><span class="sxs-lookup"><span data-stu-id="7c018-171">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-172"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-172"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-173">No</span><span class="sxs-lookup"><span data-stu-id="7c018-173">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-174">No</span><span class="sxs-lookup"><span data-stu-id="7c018-174">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c018-175">Lea el complemento de DS-replicación-obtener-cambios de todos los objetos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="7c018-175">Read PropertySet DS-Replication-Get-Changes of all Active Directory objects</span></span></p></td>
<td><p><span data-ttu-id="7c018-176">No</span><span class="sxs-lookup"><span data-stu-id="7c018-176">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-177">No</span><span class="sxs-lookup"><span data-stu-id="7c018-177">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-178">No</span><span class="sxs-lookup"><span data-stu-id="7c018-178">No</span></span></p></td>
<td><p><span data-ttu-id="7c018-179"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-179"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-180">No</span><span class="sxs-lookup"><span data-stu-id="7c018-180">No</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7c018-181">En la tabla siguiente se enumeran las ACE que crea el dominio de preparación en los tres contenedores integrados: usuarios, equipos y controladores de dominio.</span><span class="sxs-lookup"><span data-stu-id="7c018-181">The following table lists the ACEs that domain preparation creates in the three built-in containers: Users, Computers, and Domain Controllers.</span></span> <span data-ttu-id="7c018-182">A menos que se indique lo contrario, se heredan todas las ACE.</span><span class="sxs-lookup"><span data-stu-id="7c018-182">All ACEs are inherited unless otherwise noted.</span></span>

### <a name="aces-added-to-built-in-containers"></a><span data-ttu-id="7c018-183">Entradas ACE agregadas a contenedores integrados</span><span class="sxs-lookup"><span data-stu-id="7c018-183">ACEs Added to Built-in Containers</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c018-184">ENTRADA</span><span class="sxs-lookup"><span data-stu-id="7c018-184">ACE</span></span></th>
<th><span data-ttu-id="7c018-185">RTCUniversal-UserReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="7c018-185">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="7c018-186">RTCUniversal-ServerReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="7c018-186">RTCUniversal-ServerReadOnly-Group</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c018-187">Leer contenedor (no heredado)</span><span class="sxs-lookup"><span data-stu-id="7c018-187">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="7c018-188"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-188"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="7c018-189"><strong>Sí</strong></span><span class="sxs-lookup"><span data-stu-id="7c018-189"><strong>Yes</strong></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7c018-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7c018-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

