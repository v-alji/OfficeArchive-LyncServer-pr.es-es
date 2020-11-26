---
title: 'Lync Server 2013: transferencias de llamadas consultiva y enrutamiento de Location-Based'
description: 'Lync Server 2013: transferencias de llamadas consultiva y enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426557"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a><span data-ttu-id="fc90b-103">Location-Based el enrutamiento y las transferencias de llamadas Consultiva en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc90b-103">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc90b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc90b-104">

<span> </span></span></span>

<span data-ttu-id="fc90b-105">_**Última modificación del tema:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="fc90b-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="fc90b-106">Además de exigir Location-Based el enrutamiento a las reuniones de Lync, la aplicación de conferencia de enrutamiento de Location-Based exige Location-Based restricciones de enrutamiento en las transferencias de llamadas Consultiva que se salida a puntos de conexión RTC.</span><span class="sxs-lookup"><span data-stu-id="fc90b-106">In addition to enforcing Location-Based Routing to Lync meetings, the Location-Based Routing Conferencing application enforces Location-Based Routing restrictions on consultative call transfers that egress to PSTN endpoints.</span></span> <span data-ttu-id="fc90b-107">Una transferencia de llamadas Consultiva es una llamada establecida entre dos partes cuando una de las partes la transfiere a un nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="fc90b-107">A consultative call transfer is a call established between two parties where one of the parties transfers the call to a new user.</span></span> <span data-ttu-id="fc90b-108">Por ejemplo, un punto final de RTC llama al usuario A (llamada de Lync).</span><span class="sxs-lookup"><span data-stu-id="fc90b-108">For example, a PSTN endpoint calls user A (Lync callee).</span></span> <span data-ttu-id="fc90b-109">El usuario A determina que el usuario de RTC debe reenviarse al usuario B (usuario de Lync).</span><span class="sxs-lookup"><span data-stu-id="fc90b-109">User A determines the PSTN user should be forwarded to user B (Lync user).</span></span> <span data-ttu-id="fc90b-110">El usuario A coloca la llamada con el usuario de la RTC en espera y llama al usuario B. el usuario B acepta hablar con el usuario de la RTC.</span><span class="sxs-lookup"><span data-stu-id="fc90b-110">User A places the call with the PSTN user on hold, and calls user B. User B agrees to talk to the PSTN user.</span></span> <span data-ttu-id="fc90b-111">El usuario A transfiere la llamada en espera al usuario B.</span><span class="sxs-lookup"><span data-stu-id="fc90b-111">User A transfers the call on-hold to user B.</span></span>

<span data-ttu-id="fc90b-112">**Flujo de llamadas de transferencia de llamada de consulta**</span><span class="sxs-lookup"><span data-stu-id="fc90b-112">**Consultative call transfer call flow**</span></span>

<span data-ttu-id="fc90b-113">![Enrutamiento basado en ubicación para diagrama de conferencias](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Enrutamiento basado en ubicación para diagrama de conferencias")</span><span class="sxs-lookup"><span data-stu-id="fc90b-113">![Location-based routing for conferencing diagram](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Location-based routing for conferencing diagram")</span></span>

<span data-ttu-id="fc90b-114">Cuando un usuario habilitado para Location-Based el enrutamiento inicia una llamada Consultiva de un extremo de RTC (tal como se muestra en la ilustración anterior), se crean dos llamadas activas, una llamada entre el usuario de la RTC y el usuario de Lync A y la otra entre el usuario de Lync A y el usuario B de Lync. la aplicación de conferencia de enrutamiento de Location-Based exige el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="fc90b-114">When a user enabled for Location-Based Routing initiates a consultative call transfer of a PSTN endpoint (as shown in the preceding figure), this creates two active calls, one call between the PSTN user and Lync user A, and the other between Lync user A and Lync user B. the following behavior is enforced by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="fc90b-115">Si el enrutamiento de troncal del SIP la llamada RTC está autorizada para redirigir la llamada RTC al sitio de red donde se encuentra el usuario de Lync B (es decir, el destino de transferencia), se permitirá la transferencia de llamadas; de lo contrario, la transferencia de llamadas Consultiva se bloqueará.</span><span class="sxs-lookup"><span data-stu-id="fc90b-115">If the SIP trunk routing the PSTN call is authorized to re-route the PSTN call to the network site where Lync user B (i.e. transfer target) is located,, then the call transfer will be allowed; otherwise, the consultative call transfer will be blocked.</span></span> <span data-ttu-id="fc90b-116">Esta autorización se realiza en función de si la ubicación de la entidad transferida es el mismo sitio de red que el tronco SIP que está redirigiendo la llamada activa al extremo de RTC.</span><span class="sxs-lookup"><span data-stu-id="fc90b-116">This authorization is performed based on the transferred party’s location being in the same network site as the SIP trunk that is routing the active call to the PSTN endpoint.</span></span>

  - <span data-ttu-id="fc90b-117">Si el enrutamiento de tronco del SIP la llamada RTC entrante no está autorizada para enrutar llamadas al sitio de red en el que se encuentra la entidad transferida (usuario de Lync B) o la parte transferida se encuentra en un sitio de red desconocido, se bloqueará la transferencia de la llamada Consultiva al extremo de la RTC (el destino de la transferencia de llamadas).</span><span class="sxs-lookup"><span data-stu-id="fc90b-117">If the SIP trunk routing the inbound PSTN call is not authorized to route calls to the network site where the transferred party (Lync user B) is located or the transferred party is located in an unknown network site, then the consultative call transfer to the PSTN endpoint (i.e. call transfer target) will be blocked.</span></span>

<span data-ttu-id="fc90b-118">En la tabla siguiente se describe cómo se aplican Location-Based restricciones de enrutamiento en la aplicación Location-Based enrutamiento de conferencia para las transferencias de llamadas Consultiva.</span><span class="sxs-lookup"><span data-stu-id="fc90b-118">The following table describes how Location-Based Routing restrictions are applied by the Location-Based Routing Conferencing application for consultative call transfers.</span></span> <span data-ttu-id="fc90b-119">A pesar de que los extremos de PBX no están directamente asociados con un sitio de red, el tronco SIP al cual está conectado la PBX se puede asignar a un sitio de red.</span><span class="sxs-lookup"><span data-stu-id="fc90b-119">Although PBX endpoints are not directly associated with a network site, the SIP trunk the PBX is connected to can be assigned a network site.</span></span> <span data-ttu-id="fc90b-120">Por lo tanto, el extremo de PBX se puede asociar indirectamente con el sitio de red.</span><span class="sxs-lookup"><span data-stu-id="fc90b-120">Therefore, the PBX endpoint can be indirectly associated with a network site.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc90b-121">Sitio de red de la entidad de origen de la transferencia de la llamada</span><span class="sxs-lookup"><span data-stu-id="fc90b-121">Network site of call transferred party</span></span></p></td>
<td><p><span data-ttu-id="fc90b-122">Sitio de red del destino de la transferencia de la llamada</span><span class="sxs-lookup"><span data-stu-id="fc90b-122">Network site of call transfer target</span></span></p></td>
<td><p><span data-ttu-id="fc90b-123">Comportamiento</span><span class="sxs-lookup"><span data-stu-id="fc90b-123">Behavior</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc90b-124">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="fc90b-124">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="fc90b-125">Usuario de Lync en el mismo sitio de red (es decir, sitio 1)</span><span class="sxs-lookup"><span data-stu-id="fc90b-125">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="fc90b-126">Se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-126">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc90b-127">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="fc90b-127">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="fc90b-128">Usuario de Lync en diferentes sitios de red (p. ej., sitio 2)</span><span class="sxs-lookup"><span data-stu-id="fc90b-128">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="fc90b-129">No se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-129">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc90b-130">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="fc90b-130">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="fc90b-131">Usuario de Lync en un sitio de red desconocido</span><span class="sxs-lookup"><span data-stu-id="fc90b-131">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="fc90b-132">No se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-132">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc90b-133">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="fc90b-133">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="fc90b-134">Usuario federado de Lync</span><span class="sxs-lookup"><span data-stu-id="fc90b-134">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="fc90b-135">No se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-135">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc90b-136">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="fc90b-136">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="fc90b-137">Extremo de PBX en el mismo sitio (es decir, el sitio 1)</span><span class="sxs-lookup"><span data-stu-id="fc90b-137">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="fc90b-138">Se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-138">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc90b-139">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="fc90b-139">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="fc90b-140">Extremo de PBX en un sitio diferente (es decir, el sitio 2)</span><span class="sxs-lookup"><span data-stu-id="fc90b-140">PBX endpoint in a different sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="fc90b-141">No se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-141">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc90b-142">Extremo de PBX en el mismo sitio (es decir, el sitio 1)</span><span class="sxs-lookup"><span data-stu-id="fc90b-142">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="fc90b-143">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="fc90b-143">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="fc90b-144">Se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-144">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc90b-145">Extremo de PBX en un sitio diferente (es decir, el sitio 2)</span><span class="sxs-lookup"><span data-stu-id="fc90b-145">PBX endpoint in a different site (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="fc90b-146">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="fc90b-146">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="fc90b-147">No se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-147">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc90b-148">Extremo de PBX en cualquier sitio</span><span class="sxs-lookup"><span data-stu-id="fc90b-148">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="fc90b-149">Usuario de Lync en el mismo sitio de red (es decir, sitio 1)</span><span class="sxs-lookup"><span data-stu-id="fc90b-149">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="fc90b-150">Se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-150">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc90b-151">Extremo de PBX en cualquier sitio</span><span class="sxs-lookup"><span data-stu-id="fc90b-151">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="fc90b-152">Usuario de Lync en diferentes sitios de red (p. ej., sitio 2)</span><span class="sxs-lookup"><span data-stu-id="fc90b-152">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="fc90b-153">Se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-153">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc90b-154">Extremo de PBX en cualquier sitio</span><span class="sxs-lookup"><span data-stu-id="fc90b-154">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="fc90b-155">Usuario de Lync en un sitio de red desconocido</span><span class="sxs-lookup"><span data-stu-id="fc90b-155">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="fc90b-156">Se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-156">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc90b-157">Extremo de PBX en cualquier sitio</span><span class="sxs-lookup"><span data-stu-id="fc90b-157">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="fc90b-158">Usuario federado de Lync</span><span class="sxs-lookup"><span data-stu-id="fc90b-158">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="fc90b-159">Se permitirá la transferencia de consulta</span><span class="sxs-lookup"><span data-stu-id="fc90b-159">Consultative transfer will be allowed</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fc90b-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc90b-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

