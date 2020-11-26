---
title: 'Lync Server 2013: requisitos para el enrutamiento de Location-Based para conferencias'
description: 'Lync Server 2013: requisitos para el enrutamiento de Location-Based para conferencias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442666"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="c0831-103">Requisitos para Location-Based el enrutamiento de conferencias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0831-103">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0831-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0831-104">

<span> </span></span></span>

<span data-ttu-id="c0831-105">_**Última modificación del tema:** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="c0831-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="c0831-106">A continuación se indican los requisitos necesarios para la instalación y configuración de la aplicación de conferencia de enrutamiento de Location-Based:</span><span class="sxs-lookup"><span data-stu-id="c0831-106">The following are the requirements needed for the installation and configuration of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="c0831-107">La actualización acumulativa 2 de Lync Server 2013 debe implementarse en todos los servidores o grupos de servidores de su topología.</span><span class="sxs-lookup"><span data-stu-id="c0831-107">Lync Server 2013 Cumulative Update 2 must be deployed on all servers or pools in your topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c0831-108">Si un servidor de Lync o un grupo de servidores de su topología no tienen instalado la actualización acumulativa 2 o posterior de Lync Server 2013, no se puede garantizar la aplicación de Location-Based el enrutamiento de las reuniones de Lync.</span><span class="sxs-lookup"><span data-stu-id="c0831-108">If a Lync server or pool in your topology does not have Lync Server 2013 Cumulative Update 2 or higher installed, then enforcement of Location-Based Routing of Lync meetings cannot be guaranteed.</span></span>



</div>

  - <span data-ttu-id="c0831-109">Lync Server 2013 Location-Based el enrutamiento es un requisito previo para Location-Based aplicación de conferencia de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="c0831-109">Lync Server 2013 Location-Based Routing is a pre-requisite for Location-Based Routing Conferencing application.</span></span> <span data-ttu-id="c0831-110">Para obtener más información sobre cómo configurar Lync Server 2013 Location-Based enrutamiento, consulte [configuring Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="c0831-110">For further information on configuring Lync Server 2013 Location-Based Routing, please refer to [Configuring Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

  - <span data-ttu-id="c0831-111">Los requisitos de Location-Based aplicación de conferencia de enrutamiento son los mismos que se incluyen en el enrutamiento de Lync Server 2013 Location-Based.</span><span class="sxs-lookup"><span data-stu-id="c0831-111">Requirements of Location-Based Routing Conferencing application are the same as the requirements for Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="c0831-112">Para obtener más información, consulte [planeamiento de Location-Based enrutamiento](lync-server-2013-planning-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="c0831-112">For more information, please refer to [Planning for Location-Based Routing](lync-server-2013-planning-for-location-based-routing.md).</span></span>

<div>

## <a name="supported-servers"></a><span data-ttu-id="c0831-113">Servidores compatibles</span><span class="sxs-lookup"><span data-stu-id="c0831-113">Supported Servers</span></span>

<span data-ttu-id="c0831-114">La aplicación de conferencia de Location-Based enrutamiento requiere que la actualización acumulativa 2 de Lync Server 2013 se implemente en todos los grupos de Front-End y servidores Standard Edition de su topología.</span><span class="sxs-lookup"><span data-stu-id="c0831-114">The Location-Based Routing Conferencing application requires that Lync Server 2013 Cumulative Update 2 is deployed on all Front-End pools and Standard Edition Servers in your topology.</span></span> <span data-ttu-id="c0831-115">Si la actualización acumulativa 2 de Lync Server 2013 no está instalada en algunos servidores de Lync de su topología, Location-Based restricciones de enrutamiento no se pueden aplicar completamente en las reuniones de Lync ni en las transferencias de llamadas Consultiva.</span><span class="sxs-lookup"><span data-stu-id="c0831-115">If Lync Server 2013 Cumulative Update 2 is not installed on some Lync Servers in your topology, Location-Based Routing restrictions cannot be fully enforced on Lync meetings and consultative call transfers.</span></span>

<span data-ttu-id="c0831-116">En la siguiente tabla se identifica la combinación de las versiones y los roles de servidor que admiten Location-Based enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="c0831-116">The following table identifies the combination of server roles and versions that support Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0831-117">Versión del grupo de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="c0831-117">Front-End Pool version</span></span></p></td>
<td><p><span data-ttu-id="c0831-118">Versión del servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="c0831-118">Mediation Server version</span></span></p></td>
<td><p><span data-ttu-id="c0831-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="c0831-119">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0831-120">Actualización acumulativa 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0831-120">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c0831-121">Actualización acumulativa 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0831-121">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c0831-122">Sí</span><span class="sxs-lookup"><span data-stu-id="c0831-122">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0831-123">Actualización acumulativa 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0831-123">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c0831-124">Actualización acumulativa 1 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0831-124">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="c0831-125">No</span><span class="sxs-lookup"><span data-stu-id="c0831-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0831-126">Actualización acumulativa 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0831-126">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c0831-127">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="c0831-127">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="c0831-128">No</span><span class="sxs-lookup"><span data-stu-id="c0831-128">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0831-129">Actualización acumulativa 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0831-129">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="c0831-130">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="c0831-130">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="c0831-131">No</span><span class="sxs-lookup"><span data-stu-id="c0831-131">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0831-132">Actualización acumulativa 1 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0831-132">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="c0831-133">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c0831-133">Any</span></span></p></td>
<td><p><span data-ttu-id="c0831-134">No</span><span class="sxs-lookup"><span data-stu-id="c0831-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0831-135">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="c0831-135">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="c0831-136">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c0831-136">Any</span></span></p></td>
<td><p><span data-ttu-id="c0831-137">No</span><span class="sxs-lookup"><span data-stu-id="c0831-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0831-138">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="c0831-138">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="c0831-139">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c0831-139">Any</span></span></p></td>
<td><p><span data-ttu-id="c0831-140">No</span><span class="sxs-lookup"><span data-stu-id="c0831-140">No</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a><span data-ttu-id="c0831-141">Clientes compatibles</span><span class="sxs-lookup"><span data-stu-id="c0831-141">Supported Clients</span></span>

<span data-ttu-id="c0831-142">Los clientes de Lync que admiten el enrutamiento Location-Based de reuniones de Lync son los mismos clientes que admiten el enrutamiento de Lync Server 2013 Location-Based.</span><span class="sxs-lookup"><span data-stu-id="c0831-142">The Lync clients that support Location-Based Routing of Lync meetings are the same clients that support Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="c0831-143">Para obtener más información, consulte [compatibilidad de servidor y cliente para Location-Based enrutamiento](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="c0831-143">For more information, please refer to [Client and Server Support for Location-Based Routing](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span></span>

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a><span data-ttu-id="c0831-144">Requisitos del servidor de mediación para las transferencias de llamadas Consultiva</span><span class="sxs-lookup"><span data-stu-id="c0831-144">Mediation Server Requirements for Consultative Call Transfers</span></span>

<span data-ttu-id="c0831-145">La aplicación de conferencia de Location-Based enrutamiento requiere la implementación de servidores de mediación independientes para exigir Location-Based restricciones de enrutamiento en las transferencias de llamadas Consultiva.</span><span class="sxs-lookup"><span data-stu-id="c0831-145">The Location-Based Routing Conferencing application requires deploying stand-alone Mediation Servers in order to enforce Location-Based Routing restrictions on consultative call transfers.</span></span>

<span data-ttu-id="c0831-146">Para exigir Location-Based el enrutamiento de las transferencias de llamadas Consultiva, el servidor de mediación debe estar asociado solo con un servidor de mediación del mismo nivel (por ejemplo, PBX, puerta de enlace SIP, etc.) en las regiones de red en las que se requiere Location-Based enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="c0831-146">To enforce Location-Based Routing of consultative call transfers, the Mediation Server must be associated with only one Mediation Server peer (i.e. PBX, SIP gateway, etc) in network regions where Location-Based Routing is required.</span></span> <span data-ttu-id="c0831-147">Si se implementan pares de servidores de mediación adicionales en la misma región de red, el servidor de mediación del mismo nivel debe estar asociado a un servidor de mediación diferente.</span><span class="sxs-lookup"><span data-stu-id="c0831-147">If additional Mediation Server peers are deployed in the same network region, the Mediation Server peer must be associated with a different Mediation Server .</span></span> <span data-ttu-id="c0831-148">Este requisito se detalla de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c0831-148">This Requirement is detailed as follows:</span></span>

  - <span data-ttu-id="c0831-149">Servidor de mediación único para los interlocutores de varios servidores de mediación cuando una transferencia de llamada Consultiva se dirige a un servidor de mediación del mismo nivel a través de un servidor de mediación que está configurado con varios troncos SIP para varios interlocutores (es decir, PBX y puertas de enlace), la transferencia de llamadas Consultiva está bloqueada a través de otros troncos SIP.</span><span class="sxs-lookup"><span data-stu-id="c0831-149">Single Mediation Server per multiple Mediation Server peers When a consultative call transfer is routed to a Mediation Server peer through a Mediation Server that’s configured with multiple SIP trunks to multiple peers (i.e. PBXs and gateways), the consultative call transfer is blocked to prevent PSTN toll bypass if the consultative call transfer is permitted through some SIP trunks but disallowed through other SIP trunks.</span></span>
    
    <span data-ttu-id="c0831-150">Por ejemplo, en el caso de un único servidor de mediación que atienda un servidor de mediación de puerta de enlace RTC y un servidor de mediación de PBX, se observará el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="c0831-150">For example, in the case of a single Mediation Server servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="c0831-151">Cuando un usuario de Lync de un sitio determinado (por ejemplo, el sitio 1) intenta transferir una llamada con un punto final de la RTC a un usuario de Lync desde un sitio diferente (por ejemplo, el sitio 2) a través de una transferencia Consultiva, la llamada no se permitirá para evitar la omisión de llamadas RTC.</span><span class="sxs-lookup"><span data-stu-id="c0831-151">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="c0831-152">Cuando un usuario de Lync de un sitio determinado (por ejemplo, el sitio 1) intenta transferir una llamada con un extremo de PBX en el mismo sitio (sitio 1) a un usuario de Lync desde un sitio diferente (por ejemplo, el sitio 2) a través de una transferencia Consultiva, la llamada no se permitirá incluso si no se produce ninguna incumplimiento en la posible omisión de llamadas RTC.</span><span class="sxs-lookup"><span data-stu-id="c0831-152">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed even if it doesn’t incur in potential PSTN toll bypassing.</span></span>

  - <span data-ttu-id="c0831-153">Servidores de mediación independientes por servidor de mediación del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="c0831-153">Separate Mediation Servers per Mediation Server peer</span></span>
    
    <span data-ttu-id="c0831-154">Cuando una transferencia Consultiva se dirige a un interlocutor de servidor de mediación, la transferencia Consultiva se evaluará en relación con el servidor de mediación que atendida el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="c0831-154">When a consultative transfer is targeted at a Mediation Server Peer, the consultative transfer will be evaluated against the single Mediation Server Peer serviced by the Mediation Server.</span></span> <span data-ttu-id="c0831-155">La llamada no se permitirá o se autorizará en función de su potencial de incurrir en una omisión de peaje de RTC, independientemente del resto de los servidores de mediación del sitio que sean atendidas por servidores de mediación independientes.</span><span class="sxs-lookup"><span data-stu-id="c0831-155">The call will be disallowed or allowed based in its potential to incur in PSTN toll bypass regardless of all other Mediations Server Peers in the site as they’re serviced by separate Mediation Servers.</span></span>
    
    <span data-ttu-id="c0831-156">Por ejemplo, en el caso de un servidor de mediación independiente que está atendiendo a un servidor de mediación de puerta de enlace RTC y un servidor de mediación de PBX, se observará el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="c0831-156">For example, in the case of a separate Mediation Servers servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="c0831-157">Cuando un usuario de Lync de un sitio determinado (por ejemplo, el sitio 1) intenta transferir una llamada con un punto final de la RTC a un usuario de Lync desde un sitio diferente (por ejemplo, el sitio 2) a través de una transferencia Consultiva, la llamada no se permitirá para evitar la omisión de llamadas RTC.</span><span class="sxs-lookup"><span data-stu-id="c0831-157">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="c0831-158">Cuando un usuario de Lync de un sitio determinado (es decir, el sitio 1) intenta transferir una llamada con un extremo de PBX en el mismo sitio (sitio 1) a un usuario de Lync desde un sitio diferente (por ejemplo, el sitio 2) a través de la transferencia Consultiva, la llamada se permitirá porque no se produce en la posible omisión de llamadas RTC.</span><span class="sxs-lookup"><span data-stu-id="c0831-158">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be allowed as it doesn’t incur in potential PSTN toll bypassing.</span></span>

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a><span data-ttu-id="c0831-159">Funciones no compatibles con la aplicación de conferencia de enrutamiento de Location-Based</span><span class="sxs-lookup"><span data-stu-id="c0831-159">Capabilities Not Supported by the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="c0831-160">Las siguientes características no son compatibles con la aplicación Location-Based de conferencia de enrutamiento:</span><span class="sxs-lookup"><span data-stu-id="c0831-160">The following capabilities are not supported by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="c0831-161">Conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="c0831-161">Dial-in conferencing.</span></span> <span data-ttu-id="c0831-162">No se puede aplicar el enrutamiento Location-Based para las conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="c0831-162">Location-Based Routing cannot be enforced for Dial-in conferencing.</span></span> <span data-ttu-id="c0831-163">Las solicitudes de acceso telefónico a una conferencia determinada no estarán limitadas por el enrutamiento del Location-Based incluso si el organizador de la Conferencia es un usuario de Lync habilitado para Location-Based el enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="c0831-163">Any dial-in request to a given conference will not be restricted by Location-Based Routing even if the conference organizer is a Lync user enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="c0831-164">Se recomienda no suministrar números de acceso a la Conferencia en regiones donde sea necesario exigir Location-Based restricciones de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="c0831-164">It’s recommended not to provision conferencing access numbers in regions where Location-Based Routing restrictions need to be enforced.</span></span>

<span data-ttu-id="c0831-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0831-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

