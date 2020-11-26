---
title: 'Lync Server 2013: Configurar el enrutamiento basado en ubicación'
description: 'Lync Server 2013: configuración del enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Location-Based Routing
ms:assetid: 63cdc474-e80f-43b1-a237-9d9ed673300a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994036(v=OCS.15)
ms:contentKeyID: 51803946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 080c2a3a82a8714fc35ce882b0c6cb1630552f27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433045"
---
# <a name="configuring-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="3194f-103">Configurar el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3194f-103">Configuring Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3194f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3194f-104">

<span> </span></span></span>

<span data-ttu-id="3194f-105">_**Última modificación del tema:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="3194f-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="3194f-106">Lync Server 2013 CU1, el enrutamiento de Location-Based es una característica de telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="3194f-106">Lync Server 2013 CU1, Location-Based Routing is a feature of Enterprise Voice.</span></span> <span data-ttu-id="3194f-107">Location-Based el enrutamiento es una característica de administración de llamadas que controla cómo Lync Server 2013 CU1 dirige las llamadas.</span><span class="sxs-lookup"><span data-stu-id="3194f-107">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="3194f-108">Aplica restricciones sobre si las llamadas se pueden enrutar a destinos de PBX o RTC en función de la ubicación de la persona que llama de Lync.</span><span class="sxs-lookup"><span data-stu-id="3194f-108">It enforces restrictions on whether calls can be routed to PBX or PSTN destinations based on the Lync caller’s location.</span></span> <span data-ttu-id="3194f-109">El enrutamiento de Location-Based aplica las reglas de autorización de llamadas a llamadas RTC en función de la ubicación de red de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="3194f-109">Location-Based Routing applies call authorization rules to PSTN calls based on the caller’s network location.</span></span> <span data-ttu-id="3194f-110">La ubicación de la persona que llama se determina en función del sitio de red asociado a la subred de red en la que está conectada la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="3194f-110">The caller’s location is determined based on the network site associated with the network subnet the caller is connected on.</span></span> <span data-ttu-id="3194f-111">Para configurar el enrutamiento de Location-Based es necesario implementar primero la telefonía IP empresarial y, a continuación, configurar regiones, sitios y subredes de la red.</span><span class="sxs-lookup"><span data-stu-id="3194f-111">Configuring Location-Based Routing requires first deploying Enterprise Voice, then configuring network regions, sites and subnets.</span></span> <span data-ttu-id="3194f-112">Esto configura la base para habilitar el enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="3194f-112">This sets up the foundation for enabling Location-Based Routing.</span></span>

<span data-ttu-id="3194f-113">Antes de implementar Location-Based enrutamiento, primero debe implementar Enterprise Voice y configurar regiones y sitios de red, y asociar subredes de red a los sitios de red.</span><span class="sxs-lookup"><span data-stu-id="3194f-113">Before deploying Location-Based Routing, you must first deploy Enterprise Voice, and configure network regions, sites, and associate network subnets to your network sites.</span></span> <span data-ttu-id="3194f-114">Una vez completado, puede configurar el enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="3194f-114">Once completed, you can configure Location-Based Routing.</span></span> <span data-ttu-id="3194f-115">Para conocer los pasos sobre cómo configurar regiones de red, sitios y subredes, consulte [implementar características avanzadas de telefonía empresarial en Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span><span class="sxs-lookup"><span data-stu-id="3194f-115">For steps on how to configure network regions, sites and subnets, see [Deploying advanced Enterprise Voice features in Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span></span>

<span data-ttu-id="3194f-116">Esta sección le guiará a través de la configuración de Location-Based enrutamiento con el ejemplo siguiente como ilustración.</span><span class="sxs-lookup"><span data-stu-id="3194f-116">This section guides you through the configuration of Location-Based Routing using the following example as illustration.</span></span>

<span data-ttu-id="3194f-117">![Ejemplo de enrutamiento basado en la ubicación de voz empresarial](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Ejemplo de enrutamiento basado en la ubicación de voz empresarial")</span><span class="sxs-lookup"><span data-stu-id="3194f-117">![Enterprise Voice location-based routing example](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Enterprise Voice location-based routing example")</span></span>

  
<span data-ttu-id="3194f-118">En la tabla siguiente se representan los usuarios definidos en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3194f-118">The following table represents the users defined in this example.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3194f-119">Tipo de extremo</span><span class="sxs-lookup"><span data-stu-id="3194f-119">Endpoint type</span></span></th>
<th><span data-ttu-id="3194f-120">Ubicación</span><span class="sxs-lookup"><span data-stu-id="3194f-120">Location</span></span></th>
<th><span data-ttu-id="3194f-121">Usuarios</span><span class="sxs-lookup"><span data-stu-id="3194f-121">Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3194f-122">Lync</span><span class="sxs-lookup"><span data-stu-id="3194f-122">Lync</span></span></p></td>
<td><p><span data-ttu-id="3194f-123">Oficina corporativa de Delhi</span><span class="sxs-lookup"><span data-stu-id="3194f-123">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="3194f-124">DE-LYNC-1, DE-LYNC-2, DE-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="3194f-124">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3194f-125">Lync</span><span class="sxs-lookup"><span data-stu-id="3194f-125">Lync</span></span></p></td>
<td><p><span data-ttu-id="3194f-126">Oficina corporativa de Hyderabad</span><span class="sxs-lookup"><span data-stu-id="3194f-126">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="3194f-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="3194f-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3194f-128">Lync</span><span class="sxs-lookup"><span data-stu-id="3194f-128">Lync</span></span></p></td>
<td><p><span data-ttu-id="3194f-129">Desconocido (es decir, Hotel)</span><span class="sxs-lookup"><span data-stu-id="3194f-129">Unknown (i.e. hotel)</span></span></p></td>
<td><p><span data-ttu-id="3194f-130">UNK-LYNC-1</span><span class="sxs-lookup"><span data-stu-id="3194f-130">UNK-LYNC-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3194f-131">PBX</span><span class="sxs-lookup"><span data-stu-id="3194f-131">PBX</span></span></p></td>
<td><p><span data-ttu-id="3194f-132">Oficina corporativa de Delhi</span><span class="sxs-lookup"><span data-stu-id="3194f-132">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="3194f-133">DEL-PBX-1, DEL-PBX-2</span><span class="sxs-lookup"><span data-stu-id="3194f-133">DEL-PBX-1, DEL-PBX-2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3194f-134">PBX</span><span class="sxs-lookup"><span data-stu-id="3194f-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="3194f-135">Oficina corporativa de Hyderabad</span><span class="sxs-lookup"><span data-stu-id="3194f-135">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="3194f-136">HYD-PBX-1, HYD-PBX-2</span><span class="sxs-lookup"><span data-stu-id="3194f-136">HYD-PBX-1, HYD-PBX-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3194f-137">RTC</span><span class="sxs-lookup"><span data-stu-id="3194f-137">PSTN</span></span></p></td>
<td><p><span data-ttu-id="3194f-138">Reconoce</span><span class="sxs-lookup"><span data-stu-id="3194f-138">Unknown</span></span></p></td>
<td><p><span data-ttu-id="3194f-139">PSTN-1, PSTN-2, PSTN-3</span><span class="sxs-lookup"><span data-stu-id="3194f-139">PSTN-1, PSTN-2, PSTN-3</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="3194f-140">La tabla siguiente representa los sistemas que se muestran en este entorno de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3194f-140">The following table represents the systems illustrated in this example environment.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3194f-141">Sistemas</span><span class="sxs-lookup"><span data-stu-id="3194f-141">System</span></span></th>
<th><span data-ttu-id="3194f-142">Ubicación</span><span class="sxs-lookup"><span data-stu-id="3194f-142">Location</span></span></th>
<th><span data-ttu-id="3194f-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="3194f-143">Name</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3194f-144">Grupo de 2013 de Lync Server CU1</span><span class="sxs-lookup"><span data-stu-id="3194f-144">Lync Server 2013 CU1 pool</span></span></p></td>
<td><p><span data-ttu-id="3194f-145">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="3194f-145">any</span></span></p></td>
<td><p><span data-ttu-id="3194f-146">LS-PL1</span><span class="sxs-lookup"><span data-stu-id="3194f-146">LS-PL1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3194f-147">Lync Server 2013 CU1, servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="3194f-147">Lync Server 2013 CU1, Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="3194f-148">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="3194f-148">any</span></span></p></td>
<td><p><span data-ttu-id="3194f-149">MS-PL1</span><span class="sxs-lookup"><span data-stu-id="3194f-149">MS-PL1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3194f-150">Puerta de enlace PSTN 1</span><span class="sxs-lookup"><span data-stu-id="3194f-150">PSTN gateway 1</span></span></p></td>
<td><p><span data-ttu-id="3194f-151">Delhi</span><span class="sxs-lookup"><span data-stu-id="3194f-151">Delhi</span></span></p></td>
<td><p><span data-ttu-id="3194f-152">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="3194f-152">DEL-GW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3194f-153">Puerta de enlace PSTN 2</span><span class="sxs-lookup"><span data-stu-id="3194f-153">PSTN gateway 2</span></span></p></td>
<td><p><span data-ttu-id="3194f-154">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="3194f-154">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="3194f-155">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="3194f-155">HYD-GW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3194f-156">PBX 1</span><span class="sxs-lookup"><span data-stu-id="3194f-156">PBX 1</span></span></p></td>
<td><p><span data-ttu-id="3194f-157">Delhi</span><span class="sxs-lookup"><span data-stu-id="3194f-157">Delhi</span></span></p></td>
<td><p><span data-ttu-id="3194f-158">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="3194f-158">DEL-PBX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3194f-159">PBX 2</span><span class="sxs-lookup"><span data-stu-id="3194f-159">PBX 2</span></span></p></td>
<td><p><span data-ttu-id="3194f-160">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="3194f-160">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="3194f-161">RED PBX ROJA</span><span class="sxs-lookup"><span data-stu-id="3194f-161">RED-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="3194f-162">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3194f-162">In This Section</span></span>

  - [<span data-ttu-id="3194f-163">Configurar la telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3194f-163">Configuring Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-configuring-enterprise-voice.md)

  - [<span data-ttu-id="3194f-164">Implementar regiones, sitios y subredes de la red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3194f-164">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-deploying-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="3194f-165">Habilitar el enrutamiento de Location-Based en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3194f-165">Enabling Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-enabling-location-based-routing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3194f-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="3194f-166">See Also</span></span>


[<span data-ttu-id="3194f-167">Implementación de características avanzadas de telefonía empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3194f-167">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)  
  

<span data-ttu-id="3194f-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3194f-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

