---
title: 'Lync Server 2013: cambios de esquema en Lync Server 2013'
description: 'Lync Server 2013: cambios de esquema en Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema changes in Lync Server 2013
ms:assetid: d760cb93-77d4-4d64-adb7-416b808f36f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398944(v=OCS.15)
ms:contentKeyID: 48185575
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e914de48ace80fd2611f2d05b092894b11c534a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444927"
---
# <a name="schema-changes-in-lync-server-2013"></a><span data-ttu-id="ebab3-103">Cambios de esquema en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebab3-103">Schema changes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ebab3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ebab3-104">

<span> </span></span></span>

<span data-ttu-id="ebab3-105">_**Última modificación del tema:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="ebab3-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="ebab3-106">Antes de implementar y ejecutar Lync Server 2013, debe preparar el esquema para preparar los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ebab3-106">Before you deploy and operate Lync Server 2013, you must prepare Active Directory Domain Services by extending the schema.</span></span> <span data-ttu-id="ebab3-107">Las extensiones de esquema agregan las clases y los atributos requeridos por Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ebab3-107">The schema extensions add the classes and attributes that are required by Lync Server 2013.</span></span>

<span data-ttu-id="ebab3-108">Lync Server 2013 requiere varias clases y atributos nuevos y modifica algunas clases y atributos existentes.</span><span class="sxs-lookup"><span data-stu-id="ebab3-108">Lync Server 2013 requires several new classes and attributes and modifies some existing classes and attributes.</span></span> <span data-ttu-id="ebab3-109">Además, la información de configuración para Lync Server 2013 se almacena en el almacén de administración central, en lugar de en AD DS, como en versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="ebab3-109">In addition, much configuration information for Lync Server 2013 is stored in the Central Management store instead of in AD DS as in previous versions.</span></span> <span data-ttu-id="ebab3-110">La siguiente información se almacena aún en AD DS en Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="ebab3-110">The following information is still stored in AD DS in Lync Server 2013:</span></span>

  - <span data-ttu-id="ebab3-111">**Extensiones de esquema**:</span><span class="sxs-lookup"><span data-stu-id="ebab3-111">**Schema extensions**:</span></span>
    
      - <span data-ttu-id="ebab3-112">Extensiones de objetos de usuario</span><span class="sxs-lookup"><span data-stu-id="ebab3-112">User object extensions</span></span>
    
      - <span data-ttu-id="ebab3-113">Extensiones para las clases de Office Communications Server 2007 y Office Communications Server 2007 R2 para mantener la compatibilidad con versiones anteriores compatibles</span><span class="sxs-lookup"><span data-stu-id="ebab3-113">Extensions for Office Communications Server 2007 and Office Communications Server 2007 R2 classes to maintain backward compatibility with supported previous versions</span></span>

<!-- end list -->

  - <span data-ttu-id="ebab3-114">**Datos** (almacenados en el esquema extendido de Lync Server y en las clases de esquema existentes):</span><span class="sxs-lookup"><span data-stu-id="ebab3-114">**Data** (stored in Lync Server extended schema and in existing schema classes):</span></span>
    
      - <span data-ttu-id="ebab3-115">Identificador uniforme de recursos (URI) SIP de usuario y otra configuración de usuario</span><span class="sxs-lookup"><span data-stu-id="ebab3-115">User SIP Uniform Resource Identifier (URI) and other user settings</span></span>
    
      - <span data-ttu-id="ebab3-116">Objetos de contacto para aplicaciones como el operador de conferencia y el grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="ebab3-116">Contact objects for applications such as Response Group and Conferencing Attendant</span></span>
    
      - <span data-ttu-id="ebab3-117">Puntero al almacén de administración central</span><span class="sxs-lookup"><span data-stu-id="ebab3-117">A pointer to the Central Management store</span></span>
    
      - <span data-ttu-id="ebab3-118">Cuenta de autenticación Kerberos (un objeto de equipo opcional)</span><span class="sxs-lookup"><span data-stu-id="ebab3-118">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="ebab3-119">En este tema se describen los cambios de esquema de Active Directory que necesita Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ebab3-119">This topic describes the Active Directory schema changes required by Lync Server 2013.</span></span> <span data-ttu-id="ebab3-120">No se describen los cambios de esquema introducidos por versiones anteriores de Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="ebab3-120">It does not describe schema changes that were introduced by previous versions of Office Communications Server.</span></span> <span data-ttu-id="ebab3-121">Para obtener una lista de las clases y sus descripciones, vea [clases y descripciones de esquemas en Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="ebab3-121">For a list of classes and their descriptions, see [Schema classes and descriptions in Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span></span> <span data-ttu-id="ebab3-122">Para obtener una lista de atributos y sus descripciones, consulte [atributos y descripciones del esquema en Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="ebab3-122">For a list of attributes and their descriptions, see [Schema attributes and descriptions in Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span></span> <span data-ttu-id="ebab3-123">Para obtener una lista de las clases con los atributos que pueden contener, consulte [atributos de esquema por clase en Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span><span class="sxs-lookup"><span data-stu-id="ebab3-123">For a list of classes with the attributes they may contain, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span>

<span data-ttu-id="ebab3-124">El prefijo msRTCSIP identifica clases y atributos específicos de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ebab3-124">The msRTCSIP prefix identifies classes and attributes that are specific to Lync Server.</span></span>

<div>

## <a name="new-active-directory-attributes"></a><span data-ttu-id="ebab3-125">Nuevos atributos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="ebab3-125">New Active Directory Attributes</span></span>

<span data-ttu-id="ebab3-126">En la siguiente tabla se describen los atributos de Active Directory agregados por Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ebab3-126">The following table describes the Active Directory attributes that are added by Lync Server 2013.</span></span>

### <a name="attributes-added-by-lync-server-2013"></a><span data-ttu-id="ebab3-127">Atributos agregados por Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebab3-127">Attributes Added by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebab3-128">Atributo</span><span class="sxs-lookup"><span data-stu-id="ebab3-128">Attribute</span></span></th>
<th><span data-ttu-id="ebab3-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebab3-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebab3-130">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="ebab3-130">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="ebab3-131">Este atributo de valor múltiple contiene los identificadores para las directivas de retención que se aplican al usuario.</span><span class="sxs-lookup"><span data-stu-id="ebab3-131">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="ebab3-132">Las directivas de retención mantienen los elementos del buzón de correo para el usuario durante el período de espera.</span><span class="sxs-lookup"><span data-stu-id="ebab3-132">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="ebab3-133">Este atributo se comparte con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="ebab3-133">This attribute is shared with Exchange 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebab3-134">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="ebab3-134">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="ebab3-135">Este es el identificador de grupo de enrutamiento SIP.</span><span class="sxs-lookup"><span data-stu-id="ebab3-135">This is the SIP routing group ID.</span></span> <span data-ttu-id="ebab3-136">Los usuarios del mismo grupo se registrarán en el mismo servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="ebab3-136">Users in the same group will register to the same Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebab3-137">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="ebab3-137">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="ebab3-138">Este atributo se usa para almacenar el back-end de SQL Server reflejado usado por el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="ebab3-138">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="modified-active-directory-classes"></a><span data-ttu-id="ebab3-139">Clases de Active Directory modificadas</span><span class="sxs-lookup"><span data-stu-id="ebab3-139">Modified Active Directory Classes</span></span>

<span data-ttu-id="ebab3-140">En la siguiente tabla se describen las clases de Active Directory que modifica Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ebab3-140">The following table describes the Active Directory classes that are modified by Lync Server 2013.</span></span>

### <a name="classes-modified-by-lync-server-2013"></a><span data-ttu-id="ebab3-141">Clases modificadas por Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebab3-141">Classes Modified by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebab3-142">Las</span><span class="sxs-lookup"><span data-stu-id="ebab3-142">Class</span></span></th>
<th><span data-ttu-id="ebab3-143">Cambio</span><span class="sxs-lookup"><span data-stu-id="ebab3-143">Change</span></span></th>
<th><span data-ttu-id="ebab3-144">Clase o atributo</span><span class="sxs-lookup"><span data-stu-id="ebab3-144">Class or Attribute</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebab3-145">Usuario</span><span class="sxs-lookup"><span data-stu-id="ebab3-145">User</span></span></p></td>
<td><p><span data-ttu-id="ebab3-146">Agregar: mayContain</span><span class="sxs-lookup"><span data-stu-id="ebab3-146">add: mayContain</span></span></p>
<p><span data-ttu-id="ebab3-147">Agregar: mayContain</span><span class="sxs-lookup"><span data-stu-id="ebab3-147">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="ebab3-148">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="ebab3-148">ProxyAddresses</span></span></p>
<p><span data-ttu-id="ebab3-149">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="ebab3-149">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebab3-150">Con</span><span class="sxs-lookup"><span data-stu-id="ebab3-150">Contact</span></span></p></td>
<td><p><span data-ttu-id="ebab3-151">Agregar: mayContain</span><span class="sxs-lookup"><span data-stu-id="ebab3-151">add: mayContain</span></span></p>
<p><span data-ttu-id="ebab3-152">Agregar: mayContain</span><span class="sxs-lookup"><span data-stu-id="ebab3-152">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="ebab3-153">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="ebab3-153">ProxyAddresses</span></span></p>
<p><span data-ttu-id="ebab3-154">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="ebab3-154">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebab3-155">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="ebab3-155">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="ebab3-156">Agregar: mayContain</span><span class="sxs-lookup"><span data-stu-id="ebab3-156">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="ebab3-157">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="ebab3-157">msExchUserHoldPolicies</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebab3-158">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="ebab3-158">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="ebab3-159">Agregar: mayContain</span><span class="sxs-lookup"><span data-stu-id="ebab3-159">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="ebab3-160">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="ebab3-160">msRTCSIP-MirrorBackEndServer</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ebab3-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ebab3-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

