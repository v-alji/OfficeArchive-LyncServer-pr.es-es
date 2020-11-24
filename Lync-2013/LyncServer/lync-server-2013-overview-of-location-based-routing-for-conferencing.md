---
title: 'Lync Server 2013: información general sobre el enrutamiento de Location-Based para conferencias'
description: 'Lync Server 2013: información general sobre el enrutamiento de Location-Based para conferencias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing for conferencing
ms:assetid: 8b86740e-db95-4304-bb83-64d0cbb91d47
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362815(v=OCS.15)
ms:contentKeyID: 56335084
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a8fe9cdf4a797243c3ec04b3466011f374fb0d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399683"
---
# <a name="overview-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="5caec-103">Información general sobre el enrutamiento de Location-Based para conferencias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5caec-103">Overview of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5caec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5caec-104">

<span> </span></span></span>

<span data-ttu-id="5caec-105">_**Última modificación del tema:** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="5caec-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="5caec-106">La aplicación Location-Based enrutamiento de conferencias proporciona a las conferencias de Lync un mecanismo para la prevención de la omisión de llamadas RTC.</span><span class="sxs-lookup"><span data-stu-id="5caec-106">The Location-Based Routing Conferencing application provides to Lync Conferences a mechanism for the prevention of PSTN toll bypass.</span></span> <span data-ttu-id="5caec-107">La aplicación supervisa las conferencias activas y aplica Location-Based restricciones de enrutamiento en función de la ubicación de los usuarios de Lync que participan.</span><span class="sxs-lookup"><span data-stu-id="5caec-107">The application monitors active conferences and enforces Location-Based Routing restrictions based on the location of the Lync users participating.</span></span>

<span data-ttu-id="5caec-108">La aplicación Location-Based de conferencia de enrutamiento determina si se debe exigir Location-Based el enrutamiento en una reunión de Lync si se cumplen los criterios siguientes:</span><span class="sxs-lookup"><span data-stu-id="5caec-108">The Location-Based Routing Conferencing application determines whether Location-Based Routing is to be enforced on a Lync meeting if the following criteria are met:</span></span>

  - <span data-ttu-id="5caec-109">El organizador de la reunión está habilitado para Location-Based enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5caec-109">The meeting organizer is enabled for Location-Based Routing.</span></span> <span data-ttu-id="5caec-110">Location-Based restricciones de enrutamiento solo se aplicarán a conferencias organizadas por usuarios que están habilitados para Location-Based el enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5caec-110">Location-Based Routing restrictions will be applied only to conferences that are organized by users who are enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="5caec-111">Al menos uno de los participantes de la reunión es un extremo de RTC.</span><span class="sxs-lookup"><span data-stu-id="5caec-111">At least one meeting participant is a PSTN endpoint.</span></span> <span data-ttu-id="5caec-112">Location-Based las restricciones de enrutamiento solo se aplican a las conferencias que incluyen puntos de conexión RTC.</span><span class="sxs-lookup"><span data-stu-id="5caec-112">Location-Based Routing restrictions are applicable only for conferences that include PSTN endpoints.</span></span>

  - <span data-ttu-id="5caec-113">El sitio de red donde se utiliza la puerta de enlace RTC para conectar la conferencia con la RTC se encuentra (al igual que los sitios de red) en la ubicación desde donde se conectan los organizadores y los participantes.</span><span class="sxs-lookup"><span data-stu-id="5caec-113">The network site where the PSTN gateway used to bridge the conference to the PSTN is located as well as the network sites where the organizers and participants are connecting from.</span></span>

<span data-ttu-id="5caec-114">La aplicación de conferencia de Location-Based enrutamiento impide la participación de los usuarios de Lync y los puntos finales de RTC de distintos sitios de red en la misma conferencia.</span><span class="sxs-lookup"><span data-stu-id="5caec-114">The Location-Based Routing Conferencing application prevents the participation of Lync users and PSTN endpoints from different network sites to the same conference.</span></span> <span data-ttu-id="5caec-115">Si el organizador de una reunión está habilitado para Location-Based enrutamiento, la aplicación de conferencias aplicará las siguientes restricciones:</span><span class="sxs-lookup"><span data-stu-id="5caec-115">If the organizer of a meeting is enabled for Location-Based Routing, the Conferencing application enforces the following restrictions:</span></span>

  - <span data-ttu-id="5caec-116">Los puntos de conexión que pueden unirse a una reunión de Lync dependen de los puntos de conexión que ya se hayan unido a la Conferencia, y esta restricción se ajusta como puntos de conexión Unidos y los puntos de conexión nuevos se unen a la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="5caec-116">The endpoints that can join a Lync meeting depend on the endpoints that already joined the conference, and this restriction adjusts as joined endpoints leave and new endpoints join the conference.</span></span> <span data-ttu-id="5caec-117">Si los organizadores y los participantes se unen a una reunión de Lync desde el mismo sitio de red, se permite la combinación de un punto final de RTC, otro participante del mismo sitio de red, otro participante de un sitio de red diferente o de un participante de un sitio de red desconocido.</span><span class="sxs-lookup"><span data-stu-id="5caec-117">If organizers and participants are joining a Lync meeting from the same network site, then a PSTN endpoint, another participant from the same network site, another participant from a different network site or a participant from an unknown network site are allowed to join.</span></span>

  - <span data-ttu-id="5caec-118">Si organizadores y participantes se unen a la reunión desde diferentes sitios de red o sitios de red desconocidos, no se permite la entrada a la reunión de un extremo de RTC, si la llamada de RTC entra de un tronco SIP habilitado para el enrutamiento basado en ubicación.</span><span class="sxs-lookup"><span data-stu-id="5caec-118">If organizers and participants are joining the meeting from different or unknown network sites, a PSTN endpoint is not allowed to join the meeting if the PSTN call ingresses from a SIP trunk enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="5caec-119">Si todos los organizadores y participantes se unen a la reunión desde el mismo sitio de red y hay participantes que se unen a la misma reunión de la RTC, no se permite unirse a la reunión con un punto de conexión de Lync desde un sitio de red diferente.</span><span class="sxs-lookup"><span data-stu-id="5caec-119">If organizers and participants are all joining the meeting from the same network site and there are participants joining the same meeting from the PSTN, a Lync endpoint from a different network site is not allowed to join the meeting.</span></span>

<span data-ttu-id="5caec-120">En la tabla siguiente se resumen las restricciones de enrutamiento Location-Based las conferencias.</span><span class="sxs-lookup"><span data-stu-id="5caec-120">These conferencing Location-Based Routing restrictions are summarized in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5caec-121">Usuario(s) en una conferencia en un momento determinado</span><span class="sxs-lookup"><span data-stu-id="5caec-121">User(s) in a conference at any given point</span></span></p></td>
<td><p><span data-ttu-id="5caec-122">Usuarios(s) con permiso para unirse a la conferencia</span><span class="sxs-lookup"><span data-stu-id="5caec-122">User(s) allowed to join the conference</span></span></p></td>
<td><p><span data-ttu-id="5caec-123">Usuarios(s) sin permiso para unirse a la conferencia</span><span class="sxs-lookup"><span data-stu-id="5caec-123">User(s) not allowed to join the conference</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caec-124">Usuarios del cliente de VoIP de Lync desde un único sitio de red</span><span class="sxs-lookup"><span data-stu-id="5caec-124">Lync VoIP client user(s) from a single network site</span></span></p></td>
<td><p><span data-ttu-id="5caec-125">Usuario de cliente de VoIP de Lync desde el mismo sitio de red</span><span class="sxs-lookup"><span data-stu-id="5caec-125">Lync VoIP client user from the same network site</span></span></p>
<p><span data-ttu-id="5caec-126">Usuario de cliente de VoIP de Lync desde un sitio de red diferente</span><span class="sxs-lookup"><span data-stu-id="5caec-126">Lync VoIP client user from a different network site</span></span></p>
<p><span data-ttu-id="5caec-127">Usuario de cliente de VoIP de Lync desde un sitio de red desconocido</span><span class="sxs-lookup"><span data-stu-id="5caec-127">Lync VoIP client user from an unknown network site</span></span></p>
<p><span data-ttu-id="5caec-128">Usuario del cliente VoIP de Lync federado</span><span class="sxs-lookup"><span data-stu-id="5caec-128">Federated Lync VoIP client user</span></span></p>
<p><span data-ttu-id="5caec-129">Usuario que se une desde un extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="5caec-129">User joining from a PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="5caec-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5caec-130">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caec-131">Usuarios del cliente de VoIP de Lync desde un sitio de red desconocido</span><span class="sxs-lookup"><span data-stu-id="5caec-131">Lync VoIP client user(s) from an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="5caec-132">Usuario de cliente de VoIP de Lync desde cualquier sitio</span><span class="sxs-lookup"><span data-stu-id="5caec-132">Lync VoIP client user from any site</span></span></p>
<p><span data-ttu-id="5caec-133">Usuario de cliente de VoIP de Lync desde un sitio desconocido</span><span class="sxs-lookup"><span data-stu-id="5caec-133">Lync VoIP client user from an unknown site</span></span></p>
<p><span data-ttu-id="5caec-134">Usuario del cliente VoIP de Lync federado</span><span class="sxs-lookup"><span data-stu-id="5caec-134">Federated Lync VoIP client user</span></span></p></td>
<td><p><span data-ttu-id="5caec-135">Usuario que se une a través de un extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="5caec-135">User joining via a PSTN endpoint</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caec-136">Usuarios de Lync VoIP clientes de diferentes sitios de red</span><span class="sxs-lookup"><span data-stu-id="5caec-136">Lync VoIP client users from different network sites</span></span></p></td>
<td><p><span data-ttu-id="5caec-137">Usuario de cliente de VoIP de Lync desde cualquier sitio de red</span><span class="sxs-lookup"><span data-stu-id="5caec-137">Lync VoIP client user from any network site</span></span></p>
<p><span data-ttu-id="5caec-138">Usuario de cliente de VoIP de Lync desde un sitio de red desconocido</span><span class="sxs-lookup"><span data-stu-id="5caec-138">Lync VoIP client user from an unknown network site</span></span></p>
<p><span data-ttu-id="5caec-139">Usuario del cliente VoIP de Lync federado</span><span class="sxs-lookup"><span data-stu-id="5caec-139">Federated Lync VoIP client user</span></span></p></td>
<td><p><span data-ttu-id="5caec-140">Usuario que se une a través de un extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="5caec-140">User joining via a PSTN endpoint</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caec-141">Usuarios del cliente de VoIP de Lync desde un único sitio de red y usuarios que se unen desde un punto final de RTC</span><span class="sxs-lookup"><span data-stu-id="5caec-141">Lync VoIP client user(s) from a single network site and users joining from a PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="5caec-142">Usuario de cliente de VoIP de Lync desde el mismo sitio de red</span><span class="sxs-lookup"><span data-stu-id="5caec-142">Lync VoIP client user from the same network site</span></span></p></td>
<td><p><span data-ttu-id="5caec-143">Usuario de cliente de VoIP de Lync desde un sitio de red diferente</span><span class="sxs-lookup"><span data-stu-id="5caec-143">Lync VoIP client user from a different network site</span></span></p>
<p><span data-ttu-id="5caec-144">Usuario de cliente de VoIP de Lync desde un sitio de red desconocido</span><span class="sxs-lookup"><span data-stu-id="5caec-144">Lync VoIP client user from an unknown network site</span></span></p>
<p><span data-ttu-id="5caec-145">Usuario del cliente VoIP de Lync federado</span><span class="sxs-lookup"><span data-stu-id="5caec-145">Federated Lync VoIP client user</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5caec-146">A continuación se muestran características adicionales de la aplicación de conferencia de enrutamiento de Location-Based:</span><span class="sxs-lookup"><span data-stu-id="5caec-146">The following are additional characteristics of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="5caec-147">Cuando un usuario no puede unirse a una conferencia determinada Location-Based restricciones de enrutamiento, se rechazarán las llamadas de los usuarios a la Conferencia y su cliente de Lync informará que la llamada no se completó o finalizó.</span><span class="sxs-lookup"><span data-stu-id="5caec-147">When a user is not allowed to join a conference given Location-Based Routing restrictions, the users call to the conference will be rejected and his Lync Client will report that the call was not completed or has ended.</span></span>

  - <span data-ttu-id="5caec-148">Un punto final de RTC que se une a una conferencia con Location-Based las fuerzas de enrutamiento no se verá restringido para unirse a la Conferencia, independientemente de su estado, si el punto de conexión se une a través de un tronco que no está habilitado para el enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="5caec-148">A PSTN endpoint joining a conference with Location-Based Routing enforcements will not be restricted to join the conference regardless of its state if the endpoint joins via a trunk that is not enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="5caec-149">Un sistema PBX conectado a un servidor de mediación a través de un tronco de SIP que no esté de salida las llamadas a la RTC tendrán las mismas fuerzas que los usuarios de Lync que se encuentren en el mismo sitio de red en el que se define el tronco del SIP.</span><span class="sxs-lookup"><span data-stu-id="5caec-149">A PBX system connected to a Mediations Server over a SIP trunk that does not egress calls to the PSTN will have the same enforcements as Lync users located in the same network site where the SIP trunk is defined.</span></span> <span data-ttu-id="5caec-150">Por ejemplo, un punto final de RTC podrá unirse a una conferencia con un usuario de PBX y un usuario de Lync si se encuentran en el mismo sitio de red; de lo contrario, el punto final de RTC no podrá unirse a la Conferencia si el usuario de PBX se encuentra en otro sitio de red que el usuario de Lync.</span><span class="sxs-lookup"><span data-stu-id="5caec-150">For example, a PSTN endpoint will be able to join a conference with a PBX user and a Lync user if they are located in the same network site; otherwise, the PSTN endpoint will not be allowed to join the conference if the PBX user is in a different network site than the Lync user.</span></span>

<span data-ttu-id="5caec-151"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5caec-151"></div>

<span> </span>

</div>

</div>

</span></span></div>

