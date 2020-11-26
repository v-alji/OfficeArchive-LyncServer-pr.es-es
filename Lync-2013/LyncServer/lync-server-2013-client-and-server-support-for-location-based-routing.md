---
title: 'Lync Server 2013: Compatibilidad de cliente y servidor para el enrutamiento basado en ubicación'
description: 'Lync Server 2013: compatibilidad del cliente y el servidor con el enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client and server support for Location-Based Routing
ms:assetid: 26c2ca3d-026d-4dd7-94fa-15ebb4406953
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994024(v=OCS.15)
ms:contentKeyID: 51803933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20dca7444f58ee62dbc36edbb7d9e1c976a97807
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434903"
---
# <a name="client-and-server-support-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="54172-103">Compatibilidad de cliente y servidor para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54172-103">Client and server support for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54172-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54172-104">

<span> </span></span></span>

<span data-ttu-id="54172-105">_**Última modificación del tema:** 2013-06-18_</span><span class="sxs-lookup"><span data-stu-id="54172-105">_**Topic Last Modified:** 2013-06-18_</span></span>

<span data-ttu-id="54172-106">El enrutamiento de Location-Based es exigido por Lync Server.</span><span class="sxs-lookup"><span data-stu-id="54172-106">Location-Based Routing is enforced by Lync Server.</span></span> <span data-ttu-id="54172-107">Lync Server puede identificar los sitios de red desde los que se conectan los usuarios dentro de la red corporativa.</span><span class="sxs-lookup"><span data-stu-id="54172-107">Lync Server can identify the network sites where users are connecting from within the corporate network.</span></span> <span data-ttu-id="54172-108">Dado que los usuarios remotos están fuera de la red corporativa, su ubicación se considera como desconocida.</span><span class="sxs-lookup"><span data-stu-id="54172-108">Since remote users are outside the corporate network, their location is considered to be unknown.</span></span>

<div>

## <a name="lync-server-support"></a><span data-ttu-id="54172-109">Soporte técnico de Lync Server</span><span class="sxs-lookup"><span data-stu-id="54172-109">Lync Server Support</span></span>

<span data-ttu-id="54172-110">Location-Based enrutamiento requiere que Lync Server 2013 CU1 se implemente en todos los grupos de servidores front-end y servidores Standard Edition en una topología determinada.</span><span class="sxs-lookup"><span data-stu-id="54172-110">Location-Based Routing requires that Lync Server 2013 CU1 is deployed on all Front End pools and Standard Edition servers in a given topology.</span></span> <span data-ttu-id="54172-111">Si Lync Server 2013 CU1 no está instalado en algunos componentes de Lync de la topología, no se pueden aplicar las restricciones de enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="54172-111">If Lync Server 2013 CU1 is not installed on certain Lync components in the topology, Location-Based Routing restrictions cannot be fully enforced.</span></span>

<span data-ttu-id="54172-112">En la siguiente tabla se identifica la combinación de las versiones y los roles de servidor que se admiten para Location-Based el enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="54172-112">The following table identifies the combination of server roles and versions that is supported for Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54172-113">Versión del grupo</span><span class="sxs-lookup"><span data-stu-id="54172-113">Pool version</span></span></th>
<th><span data-ttu-id="54172-114">Versión del servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="54172-114">Mediation Server version</span></span></th>
<th><span data-ttu-id="54172-115">Compatible</span><span class="sxs-lookup"><span data-stu-id="54172-115">Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54172-116">Lync Server 2013, actualización acumulativa de febrero 2013</span><span class="sxs-lookup"><span data-stu-id="54172-116">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="54172-117">Lync Server 2013, actualización acumulativa de febrero 2013</span><span class="sxs-lookup"><span data-stu-id="54172-117">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="54172-118">sí</span><span class="sxs-lookup"><span data-stu-id="54172-118">yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54172-119">Lync Server 2013, actualización acumulativa de febrero 2013</span><span class="sxs-lookup"><span data-stu-id="54172-119">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="54172-120">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54172-120">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="54172-121">no</span><span class="sxs-lookup"><span data-stu-id="54172-121">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54172-122">Lync Server 2013, actualización acumulativa de febrero 2013</span><span class="sxs-lookup"><span data-stu-id="54172-122">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="54172-123">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="54172-123">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="54172-124">no</span><span class="sxs-lookup"><span data-stu-id="54172-124">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54172-125">Lync Server 2013, actualización acumulativa de febrero 2013</span><span class="sxs-lookup"><span data-stu-id="54172-125">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="54172-126">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="54172-126">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="54172-127">no</span><span class="sxs-lookup"><span data-stu-id="54172-127">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54172-128">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54172-128">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="54172-129">cualquiera</span><span class="sxs-lookup"><span data-stu-id="54172-129">any</span></span></p></td>
<td><p><span data-ttu-id="54172-130">no</span><span class="sxs-lookup"><span data-stu-id="54172-130">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54172-131">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="54172-131">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="54172-132">cualquiera</span><span class="sxs-lookup"><span data-stu-id="54172-132">any</span></span></p></td>
<td><p><span data-ttu-id="54172-133">no</span><span class="sxs-lookup"><span data-stu-id="54172-133">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54172-134">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="54172-134">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="54172-135">cualquiera</span><span class="sxs-lookup"><span data-stu-id="54172-135">any</span></span></p></td>
<td><p><span data-ttu-id="54172-136">no</span><span class="sxs-lookup"><span data-stu-id="54172-136">no</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="54172-137">Compatibilidad con clientes de Lync</span><span class="sxs-lookup"><span data-stu-id="54172-137">Lync Client Support</span></span>

<span data-ttu-id="54172-138">La siguiente tabla identifica los clientes que admite el enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="54172-138">The following table identifies the clients that Location-Based Routing supports.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54172-139">Tipo de cliente</span><span class="sxs-lookup"><span data-stu-id="54172-139">Client type</span></span></th>
<th><span data-ttu-id="54172-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="54172-140">Supported</span></span></th>
<th><span data-ttu-id="54172-141">Detalles</span><span class="sxs-lookup"><span data-stu-id="54172-141">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54172-142">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="54172-142">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="54172-143">sí</span><span class="sxs-lookup"><span data-stu-id="54172-143">yes</span></span></p></td>
<td><p><span data-ttu-id="54172-144">Incluidas las actualizaciones acumulativas de Lync 2013 de febrero de 2013</span><span class="sxs-lookup"><span data-stu-id="54172-144">Including Lync 2013 February 2013 Cumulative Update</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54172-145">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="54172-145">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="54172-146">sí</span><span class="sxs-lookup"><span data-stu-id="54172-146">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54172-147">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="54172-147">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="54172-148">no</span><span class="sxs-lookup"><span data-stu-id="54172-148">no</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54172-149">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="54172-149">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="54172-150">sí</span><span class="sxs-lookup"><span data-stu-id="54172-150">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54172-151">Lync Attendant</span><span class="sxs-lookup"><span data-stu-id="54172-151">Lync Attendant</span></span></p></td>
<td><p><span data-ttu-id="54172-152">sí</span><span class="sxs-lookup"><span data-stu-id="54172-152">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54172-153">Lync para Windows 8</span><span class="sxs-lookup"><span data-stu-id="54172-153">Lync for Windows 8</span></span></p></td>
<td><p><span data-ttu-id="54172-154">no</span><span class="sxs-lookup"><span data-stu-id="54172-154">no</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54172-155">Lync Mobile 2013</span><span class="sxs-lookup"><span data-stu-id="54172-155">Lync Mobile 2013</span></span></p></td>
<td><p><span data-ttu-id="54172-156">no</span><span class="sxs-lookup"><span data-stu-id="54172-156">no</span></span></p></td>
<td><p><span data-ttu-id="54172-157">VoIP debe estar deshabilitado para los clientes de Lync Mobile 2013 si lo usan los usuarios con el enrutamiento Location-Based habilitado.</span><span class="sxs-lookup"><span data-stu-id="54172-157">VoIP must be disabled for Lync Mobile 2013 clients if used by users with Location-Based Routing enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54172-158">Lync Mobile 2010</span><span class="sxs-lookup"><span data-stu-id="54172-158">Lync Mobile 2010</span></span></p></td>
<td><p><span data-ttu-id="54172-159">sí</span><span class="sxs-lookup"><span data-stu-id="54172-159">yes</span></span></p></td>
<td> </td>
</tr>
</tbody>
</table>

  

<div>


> [!NOTE]  
> <span data-ttu-id="54172-160">Para deshabilitar VoIP para Lync Mobile 2013 clientes, asigne una directiva de movilidad con la configuración, audio/vídeo IP, deshabilitado para todos los usuarios habilitados para el enrutamiento basado en la ubicación.</span><span class="sxs-lookup"><span data-stu-id="54172-160">To disable VoIP for Lync Mobile 2013 clients, assign a mobility policy with the setting, IP Audio/Video, disabled for all users enabled for Location Based Routing.</span></span> <span data-ttu-id="54172-161">Para obtener más detalles sobre la directiva de movilidad, mira <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span><span class="sxs-lookup"><span data-stu-id="54172-161">For more details about mobility policy, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="54172-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="54172-162">See Also</span></span>


[<span data-ttu-id="54172-163">Planificar el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54172-163">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="54172-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54172-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

