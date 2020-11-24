---
title: 'Lync Server 2013: Proceso de implementación para el enrutamiento basado en ubicación'
description: 'Lync Server 2013: proceso de implementación para el enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Location-Based Routing
ms:assetid: 9e923e72-83fc-4a4f-8937-28a55739ed3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994055(v=OCS.15)
ms:contentKeyID: 51803966
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2c321d9b0eada6e9501b2ded69120feae36be171
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399569"
---
# <a name="deployment-process-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="ef83d-103">Proceso de implementación para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef83d-103">Deployment process for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef83d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef83d-104">

<span> </span></span></span>

<span data-ttu-id="ef83d-105">_**Última modificación del tema:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="ef83d-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="ef83d-106">Este tema proporciona una descripción general del proceso implicado en la configuración del enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="ef83d-106">This topic provides an overview of the process involved in configuring Location-Based Routing.</span></span> <span data-ttu-id="ef83d-107">Debe implementar Lync Server Enterprise Edition o Standard Edition con telefonía IP empresarial antes de configurar Location-Based enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="ef83d-107">You must deploy Lync Server Enterprise Edition or Standard Edition with Enterprise Voice before you configure Location-Based Routing.</span></span> <span data-ttu-id="ef83d-108">Los componentes que necesita Location-Based enrutamiento ya están instalados y habilitados al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="ef83d-108">The components required by Location-Based Routing are already installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="location-based-routing-deployment-process"></a><span data-ttu-id="ef83d-109">Location-Based proceso de implementación de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="ef83d-109">Location-Based Routing Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef83d-110">Fase</span><span class="sxs-lookup"><span data-stu-id="ef83d-110">Phase</span></span></th>
<th><span data-ttu-id="ef83d-111">Pasos</span><span class="sxs-lookup"><span data-stu-id="ef83d-111">Steps</span></span></th>
<th><span data-ttu-id="ef83d-112">Grupos y roles necesarios</span><span class="sxs-lookup"><span data-stu-id="ef83d-112">Required groups and roles</span></span></th>
<th><span data-ttu-id="ef83d-113">Documentación de implementación</span><span class="sxs-lookup"><span data-stu-id="ef83d-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef83d-114">Implementar la telefonía IP empresarial</span><span class="sxs-lookup"><span data-stu-id="ef83d-114">Deploy Enterprise Voice</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="ef83d-115">Configurar los troncos</span><span class="sxs-lookup"><span data-stu-id="ef83d-115">Configure Trunks</span></span></p></li>
<li><p><span data-ttu-id="ef83d-116">Crear directivas de voz</span><span class="sxs-lookup"><span data-stu-id="ef83d-116">Create Voice Policies</span></span></p></li>
<li><p><span data-ttu-id="ef83d-117">Definir rutas de voz</span><span class="sxs-lookup"><span data-stu-id="ef83d-117">Define Voice Routes</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ef83d-118">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="ef83d-118">CSVoiceAdmins</span></span><br />
<span data-ttu-id="ef83d-119">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef83d-119">CsAdministrator</span></span><br />
<span data-ttu-id="ef83d-120">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef83d-120">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="ef83d-121">Implementación de telefonía IP empresarial</span><span class="sxs-lookup"><span data-stu-id="ef83d-121">Deploying Enterprise Voice</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef83d-122">Comprobar la implementación de telefonía IP empresarial</span><span class="sxs-lookup"><span data-stu-id="ef83d-122">Verify your Enterprise Voice deployment</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef83d-123">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="ef83d-123">CSVoiceAdmins</span></span><br />
<span data-ttu-id="ef83d-124">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef83d-124">CsAdministrator</span></span><br />
<span data-ttu-id="ef83d-125">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef83d-125">CsServerAdministrator</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef83d-126">Configurar regiones, sitios y subredes de redes</span><span class="sxs-lookup"><span data-stu-id="ef83d-126">Configure network regions, sites, and subnets</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="ef83d-127">Crear regiones de red</span><span class="sxs-lookup"><span data-stu-id="ef83d-127">Create network regions</span></span></p></li>
<li><p><span data-ttu-id="ef83d-128">Crear sitios de red</span><span class="sxs-lookup"><span data-stu-id="ef83d-128">Create network sites</span></span></p></li>
<li><p><span data-ttu-id="ef83d-129">Asociar subredes con sitios de red</span><span class="sxs-lookup"><span data-stu-id="ef83d-129">Associates subnets with network sites</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ef83d-130">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="ef83d-130">CSVoiceAdmins</span></span><br />
<span data-ttu-id="ef83d-131">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef83d-131">CsAdministrator</span></span><br />
<span data-ttu-id="ef83d-132">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef83d-132">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="ef83d-133">Acerca de las regiones, sitios y subredes de la red</span><span class="sxs-lookup"><span data-stu-id="ef83d-133">About Network Regions, Sites, and Subnets</span></span><br />
<span data-ttu-id="ef83d-134">Crear o modificar una región de red</span><span class="sxs-lookup"><span data-stu-id="ef83d-134">Create or Modify a Network Region</span></span><br />
<span data-ttu-id="ef83d-135">Crear o modificar un sitio de red</span><span class="sxs-lookup"><span data-stu-id="ef83d-135">Create or Modify a Network Site</span></span><br />
<span data-ttu-id="ef83d-136">Asociar una subred a un sitio de red</span><span class="sxs-lookup"><span data-stu-id="ef83d-136">Associate a Subnet with a Network Site</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef83d-137">Configurar enrutamiento de Location-Based</span><span class="sxs-lookup"><span data-stu-id="ef83d-137">Configure Location-Based Routing</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="ef83d-138">Crear directivas de enrutamiento de voz</span><span class="sxs-lookup"><span data-stu-id="ef83d-138">Create voice routing policies</span></span></p></li>
<li><p><span data-ttu-id="ef83d-139">Definir una configuración troncal separada por tronco</span><span class="sxs-lookup"><span data-stu-id="ef83d-139">Define separate trunk configuration per trunk</span></span></p></li>
<li><p><span data-ttu-id="ef83d-140">Modificar directivas de voz</span><span class="sxs-lookup"><span data-stu-id="ef83d-140">Modify voice policies</span></span></p></li>
<li><p><span data-ttu-id="ef83d-141">Habilitar Location-Based configuración de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="ef83d-141">Enable Location-Based Routing configuration</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ef83d-142">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="ef83d-142">CSVoiceAdmins</span></span><br />
<span data-ttu-id="ef83d-143">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef83d-143">CsAdministrator</span></span><br />
<span data-ttu-id="ef83d-144">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef83d-144">CsServerAdministrator</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="sample-deployment"></a><span data-ttu-id="ef83d-145">Implementación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef83d-145">Sample Deployment</span></span>

<span data-ttu-id="ef83d-146">La siguiente implementación se usa para ilustrar aún más los mecanismos habilitados por Location-Based el enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="ef83d-146">The following deployment is used to illustrate further the mechanisms enabled by Location-Based Routing.</span></span>

<span data-ttu-id="ef83d-147">![e1bd2230-44da-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-b359-24572b6ce02d")</span><span class="sxs-lookup"><span data-stu-id="ef83d-147">![e1bd2230-44da-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-b359-24572b6ce02d")</span></span>

<div>

## <a name="incoming-pstn-calls"></a><span data-ttu-id="ef83d-148">Llamadas RTC entrantes</span><span class="sxs-lookup"><span data-stu-id="ef83d-148">Incoming PSTN calls</span></span>

<span data-ttu-id="ef83d-149">Un administrador puede habilitar el tronco definido para enrutar llamadas a "puerta de enlace del sitio 1" para el enrutamiento de Location-Based y asociar la "puerta de enlace del sitio 1" al sitio 1.</span><span class="sxs-lookup"><span data-stu-id="ef83d-149">An administrator can enable the trunk defined to route calls to “Site 1 Gateway” for Location-Based Routing and associate the “Site 1 Gateway” to site 1.</span></span> <span data-ttu-id="ef83d-150">Una vez habilitadas, las llamadas que se dirigen a través de "puerta de enlace del sitio 1" solo se redirigirán a los usuarios que se encuentren en el sitio 1.</span><span class="sxs-lookup"><span data-stu-id="ef83d-150">Once enabled, calls that are routed through “Site 1 Gateway“ will only be routed to users that are located in site 1.</span></span> <span data-ttu-id="ef83d-151">Todas las llamadas dirigidas a través del "enlace de la puerta de enlace del sitio 1" dirigidas a usuarios de otro sitio, como el sitio 2, se bloquearán para evitar el bypass de llamadas RTC.</span><span class="sxs-lookup"><span data-stu-id="ef83d-151">All calls routed through the “Site 1 Gateway” trunk destined to users in a different site, such as site 2 will be blocked to prevent PSTN toll bypass.</span></span>

<span data-ttu-id="ef83d-152">Todas las llamadas de RTC entrantes a través de "puerta de enlace del sitio 1" solo podrán enrutar a los puntos de conexión que se encuentren en el sitio 1.</span><span class="sxs-lookup"><span data-stu-id="ef83d-152">All incoming PSTN calls through “Site 1 Gateway” will only be allowed to route to endpoints located in site 1.</span></span> <span data-ttu-id="ef83d-153">Por ejemplo, cuando "usuario de Lync 1" se desplaza al sitio 2, todas las llamadas RTC entrantes a través de "puerta de enlace del sitio 1" no se enrutarán a los puntos de conexión de "usuario de Lync 1" ubicados en el sitio 2.</span><span class="sxs-lookup"><span data-stu-id="ef83d-153">For example, when “Lync user 1” travels to site 2, all incoming PSTN calls through “Site 1 Gateway” will not be routed to “Lync user 1” endpoints located in site 2.</span></span> <span data-ttu-id="ef83d-154">La misma regla de enrutamiento se aplica si "Lync User 1" se desplaza a un sitio de red desconocido en el que no se puede determinar la ubicación del usuario.</span><span class="sxs-lookup"><span data-stu-id="ef83d-154">The same routing rule applies if “Lync user 1” travels to an unknown network site where the user’s location can’t be determined.</span></span>

<span data-ttu-id="ef83d-155">En la siguiente tabla se describe la experiencia del usuario de "Lync User 1" en este contexto.</span><span class="sxs-lookup"><span data-stu-id="ef83d-155">The following table outlines the user experience of “Lync user 1” in this context.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ef83d-156">Puntos de conexión del usuario 1 de Lync ubicados en el sitio de red 1</span><span class="sxs-lookup"><span data-stu-id="ef83d-156">Lync user 1 endpoints located in network site 1</span></span></th>
<th><span data-ttu-id="ef83d-157">Puntos de conexión del usuario 1 de Lync ubicados en el sitio de red 2</span><span class="sxs-lookup"><span data-stu-id="ef83d-157">Lync user 1 endpoints located in network site 2</span></span></th>
<th><span data-ttu-id="ef83d-158">Puntos de conexión del usuario 1 de Lync ubicados en un sitio de red desconocido</span><span class="sxs-lookup"><span data-stu-id="ef83d-158">Lync user 1 endpoints located in unknown network site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef83d-159">Llamadas RTC entrantes a usuarios de Lync 1</span><span class="sxs-lookup"><span data-stu-id="ef83d-159">Inbound PSTN calls to Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="ef83d-160">Las llamadas se enrutan a los puntos de conexión de esta ubicación</span><span class="sxs-lookup"><span data-stu-id="ef83d-160">Calls are routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="ef83d-161">Las llamadas no se enrutan a los puntos de conexión de esta ubicación</span><span class="sxs-lookup"><span data-stu-id="ef83d-161">Calls are not routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="ef83d-162">Las llamadas no se enrutan a los puntos de conexión de esta ubicación</span><span class="sxs-lookup"><span data-stu-id="ef83d-162">Calls are not routed to endpoints in this location</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="outgoing-pstn-calls"></a><span data-ttu-id="ef83d-163">Llamadas RTC salientes</span><span class="sxs-lookup"><span data-stu-id="ef83d-163">Outgoing PSTN calls</span></span>

<span data-ttu-id="ef83d-164">Las rutas de voz se mencionan en las dos directivas de voz asignadas directamente a los usuarios y las directivas de enrutamiento de voz asignadas a sitios de red.</span><span class="sxs-lookup"><span data-stu-id="ef83d-164">Voice routes are referenced in both Voice Policies assigned directly to users, and Voice Routing Policies assigned to network sites.</span></span> <span data-ttu-id="ef83d-165">Ambas directivas contienen referencias a rutas, que se pueden usar para enrutar una llamada de otra manera.</span><span class="sxs-lookup"><span data-stu-id="ef83d-165">Both policies contain references to routes, which can be used to route a call differently.</span></span> <span data-ttu-id="ef83d-166">Por ejemplo, un administrador puede definir una directiva de enrutamiento de voz para todos los usuarios ubicados en el sitio de red 1 para enrutar todas las llamadas salientes a través de la "puerta de enlace del sitio 1", mientras que la Directiva de voz de algunos usuarios define una ruta para todas las llamadas salientes a través de la "puerta de enlace del sitio 2".</span><span class="sxs-lookup"><span data-stu-id="ef83d-166">For example, an administrator can define a Voice Routing Policy for all users located in network site 1 to route all outbound calls through the “Site 1 Gateway” while the Voice Policy of some users define a route for all outbound calls through the “Site 2 Gateway”.</span></span> <span data-ttu-id="ef83d-167">Mientras estos usuarios se encuentren en el sitio 1 de la red, sus llamadas salientes se redirigirán a través de la "puerta de enlace del sitio 1".</span><span class="sxs-lookup"><span data-stu-id="ef83d-167">While these users are located in network site 1, their outbound calls will be routed through the “Site 1 Gateway”.</span></span>

<span data-ttu-id="ef83d-168">Cuando un usuario se encuentra en un sitio de red configurado para Location-Based el enrutamiento, la ruta de la Directiva de enrutamiento de voz del sitio de red invalida la ruta de la Directiva de voz del usuario.</span><span class="sxs-lookup"><span data-stu-id="ef83d-168">When a user is located in a network site configured for Location-Based Routing, the network site’s Voice Routing Policy route overrides the user’s Voice Policy route.</span></span> <span data-ttu-id="ef83d-169">Esta regla es particularmente útil para los usuarios que se mueven temporalmente a un sitio diferente.</span><span class="sxs-lookup"><span data-stu-id="ef83d-169">This rule is particularly useful for users that temporarily move to a different site.</span></span> <span data-ttu-id="ef83d-170">En este caso concreto, un usuario siempre usará una puerta de enlace local a su ubicación; Si "el usuario de Lync 3" se encuentra en "sitio 2", todas sus llamadas salientes se enrutarán a través de "puerta de enlace del sitio 2", pero si viajan al sitio 1, todas sus llamadas salientes realizadas mientras está en el sitio 1 se dirigirán a través de la "puerta de enlace del sitio 1".</span><span class="sxs-lookup"><span data-stu-id="ef83d-170">In this particular case a user will always use a gateway that is local to his location; if “Lync user 3” is located at “Site 2”, all his outbound calls will be routed via “Site 2 Gateway”, but if he travels to site 1, all his outbound calls placed while he’s at site 1 will be routed through “Site 1 Gateway”.</span></span>

<span data-ttu-id="ef83d-171">La tabla siguiente muestra la experiencia de usuario del usuario de Lync 1 que realiza una llamada saliente desde los siguientes sitios de red.</span><span class="sxs-lookup"><span data-stu-id="ef83d-171">The following table illustrates the user experience of Lync user 1 placing an outbound call from the following network sites.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ef83d-172">Sitio de red 1</span><span class="sxs-lookup"><span data-stu-id="ef83d-172">Network site 1</span></span></th>
<th><span data-ttu-id="ef83d-173">Sitio de red 2</span><span class="sxs-lookup"><span data-stu-id="ef83d-173">Network site 2</span></span></th>
<th><span data-ttu-id="ef83d-174">Sitio de red desconocido o no habilitado para Location-Based enrutamiento</span><span class="sxs-lookup"><span data-stu-id="ef83d-174">Unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef83d-175">Autorización de llamadas salientes</span><span class="sxs-lookup"><span data-stu-id="ef83d-175">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="ef83d-176">Directiva de voz de usuario 1 de Lync</span><span class="sxs-lookup"><span data-stu-id="ef83d-176">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="ef83d-177">Directiva de voz de usuario 1 de Lync</span><span class="sxs-lookup"><span data-stu-id="ef83d-177">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="ef83d-178">Directiva de voz de usuario 1 de Lync</span><span class="sxs-lookup"><span data-stu-id="ef83d-178">Lync user 1 voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef83d-179">Enrutamiento de llamadas salientes</span><span class="sxs-lookup"><span data-stu-id="ef83d-179">Routing of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="ef83d-180">Directiva de enrutamiento de voz del sitio 1</span><span class="sxs-lookup"><span data-stu-id="ef83d-180">Site 1 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="ef83d-181">Directiva de enrutamiento de voz del sitio 2</span><span class="sxs-lookup"><span data-stu-id="ef83d-181">Site 2 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="ef83d-182">Directiva de voz del usuario y solo en sistemas que no están habilitados para Location-Based enrutamiento</span><span class="sxs-lookup"><span data-stu-id="ef83d-182">User’s voice policy and only to systems not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="call-transfers-and-forwards"></a><span data-ttu-id="ef83d-183">Transferencia de llamadas y reenvíos</span><span class="sxs-lookup"><span data-stu-id="ef83d-183">Call transfers and forwards</span></span>

<span data-ttu-id="ef83d-184">Cuando se transfieren o desvian las llamadas, el enrutamiento de las llamadas se ve afectado por Location-Based enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="ef83d-184">When calls are transferred or forwarded, the routing of calls is affected by Location-Based Routing.</span></span>

<span data-ttu-id="ef83d-185">En la tabla siguiente se muestra cómo el usuario de Lync 1 está transfiriendo o reenviando una llamada RTC a otro usuario de Lync.</span><span class="sxs-lookup"><span data-stu-id="ef83d-185">The following table depicts Lync user 1 transferring or forwarding a PSTN call to another Lync user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef83d-186">El usuario está iniciando la transferencia de llamadas o el reenvío</span><span class="sxs-lookup"><span data-stu-id="ef83d-186">User initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="ef83d-187">Usuario de Lync 2</span><span class="sxs-lookup"><span data-stu-id="ef83d-187">Lync user 2</span></span></th>
<th><span data-ttu-id="ef83d-188">Usuario de Lync 4</span><span class="sxs-lookup"><span data-stu-id="ef83d-188">Lync user 4</span></span></th>
<th><span data-ttu-id="ef83d-189">El usuario de Lync en el sitio de red no está habilitado para el enrutamiento de Location-Based</span><span class="sxs-lookup"><span data-stu-id="ef83d-189">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef83d-190">Usuario de Lync 1</span><span class="sxs-lookup"><span data-stu-id="ef83d-190">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="ef83d-191">Se permite el desvío o la transferencia de la llamada</span><span class="sxs-lookup"><span data-stu-id="ef83d-191">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="ef83d-192">No se permite el desvío ni la transferencia de la llamada</span><span class="sxs-lookup"><span data-stu-id="ef83d-192">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="ef83d-193">No se permite el desvío ni la transferencia de la llamada</span><span class="sxs-lookup"><span data-stu-id="ef83d-193">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="ef83d-194">En la tabla siguiente se muestra cómo el enrutamiento de Location-Based afecta a la forma en que se enruta la llamada en función de la ubicación del usuario de Lync que se está transfiriendo (Lync User 2, Lync User 4, etc.) a un punto final de RTC</span><span class="sxs-lookup"><span data-stu-id="ef83d-194">The following table illustrates how Location-Based Routing affects how the call is routed based on the location of the Lync user being transferred (Lync user 2, Lync user 4, etc) to a PSTN endpoint</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef83d-195">Punto final en el que se transfiere o reenvía una llamada</span><span class="sxs-lookup"><span data-stu-id="ef83d-195">Endpoint where call is transferred or forwarded to</span></span></th>
<th><span data-ttu-id="ef83d-196">Usuario de Lync 2</span><span class="sxs-lookup"><span data-stu-id="ef83d-196">Lync user 2</span></span></th>
<th><span data-ttu-id="ef83d-197">Usuario de Lync 4</span><span class="sxs-lookup"><span data-stu-id="ef83d-197">Lync user 4</span></span></th>
<th><span data-ttu-id="ef83d-198">El usuario de Lync en el sitio de red no está habilitado para el enrutamiento de Location-Based</span><span class="sxs-lookup"><span data-stu-id="ef83d-198">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef83d-199">Extremo de RTC</span><span class="sxs-lookup"><span data-stu-id="ef83d-199">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="ef83d-200">El desvío de llamadas o la transferencia se dirige a través de la Directiva de enrutamiento de voz del sitio 1 y de salida a través de la puerta de enlace del sitio 1</span><span class="sxs-lookup"><span data-stu-id="ef83d-200">Call forward or transfer is routed through site 1 voice routing policy and egress via Site 1 Gateway</span></span></p></td>
<td><p><span data-ttu-id="ef83d-201">El desvío de llamadas o la transferencia se dirige a través de la Directiva de enrutamiento de voz del sitio 2 y de salida a través de la puerta de enlace del sitio 2</span><span class="sxs-lookup"><span data-stu-id="ef83d-201">Call forward or transfer is routed through site 2 voice routing policy and egress via Site 2 Gateway</span></span></p></td>
<td><p><span data-ttu-id="ef83d-202">El desvío de llamadas o la transferencia se dirige a través de la Directiva de voz de usuario de Lync y se salida a través de una puerta de enlace no habilitada para enrutamiento basado en la ubicación (si está disponible)</span><span class="sxs-lookup"><span data-stu-id="ef83d-202">Call forward or transfer is routed through the Lync user voice policy and egress via a gateway not enabled for location-based routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="simultaneous-ringing"></a><span data-ttu-id="ef83d-203">Tono de llamada simultáneo</span><span class="sxs-lookup"><span data-stu-id="ef83d-203">Simultaneous ringing</span></span>

<span data-ttu-id="ef83d-204">Una vez que se configura el enrutamiento basado en la topología de muestra, se aplican las siguientes interacciones.</span><span class="sxs-lookup"><span data-stu-id="ef83d-204">Once location-based routing is configured in the sample topology, the following interactions are enforced.</span></span>

<span data-ttu-id="ef83d-205">En la tabla siguiente se muestra si Location-Based enrutamiento permite llamadas simultáneas para diferentes usuarios de Lync (por ejemplo, usuario de Lync 2, usuario de Lync 4, etc.).</span><span class="sxs-lookup"><span data-stu-id="ef83d-205">The following table illustrates whether Location-Based Routing allows simultaneous ringing for different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef83d-206">Destino de llamada RTC entrante</span><span class="sxs-lookup"><span data-stu-id="ef83d-206">Incoming PSTN call target</span></span></th>
<th><span data-ttu-id="ef83d-207">Usuario de Lync 2</span><span class="sxs-lookup"><span data-stu-id="ef83d-207">Lync user 2</span></span></th>
<th><span data-ttu-id="ef83d-208">Usuario de Lync 4</span><span class="sxs-lookup"><span data-stu-id="ef83d-208">Lync user 4</span></span></th>
<th><span data-ttu-id="ef83d-209">El usuario de Lync en el sitio de red no está habilitado para el enrutamiento de Location-Based</span><span class="sxs-lookup"><span data-stu-id="ef83d-209">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef83d-210">Usuario de Lync 1</span><span class="sxs-lookup"><span data-stu-id="ef83d-210">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="ef83d-211">Se permiten las llamadas simultáneas</span><span class="sxs-lookup"><span data-stu-id="ef83d-211">Simultaneous ring is allowed</span></span></p></td>
<td><p><span data-ttu-id="ef83d-212">No se permiten llamadas simultáneas</span><span class="sxs-lookup"><span data-stu-id="ef83d-212">Simultaneous ring is not allowed</span></span></p></td>
<td><p><span data-ttu-id="ef83d-213">No se permiten llamadas simultáneas</span><span class="sxs-lookup"><span data-stu-id="ef83d-213">Simultaneous ring is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="ef83d-214">En la tabla siguiente se muestra si Location-Based enrutamiento permite hacer llamadas simultáneas a un punto final de RTC de diferentes usuarios de Lync (por ejemplo, usuario de Lync 2, usuario de Lync 4, etc.).</span><span class="sxs-lookup"><span data-stu-id="ef83d-214">The following table illustrates whether Location-Based Routing allows simultaneous ringing to a PSTN endpoint from different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef83d-215">Destino de llamadas simultáneas</span><span class="sxs-lookup"><span data-stu-id="ef83d-215">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="ef83d-216">Usuario de Lync 2</span><span class="sxs-lookup"><span data-stu-id="ef83d-216">Lync user 2</span></span></th>
<th><span data-ttu-id="ef83d-217">Usuario de Lync 4</span><span class="sxs-lookup"><span data-stu-id="ef83d-217">Lync user 4</span></span></th>
<th><span data-ttu-id="ef83d-218">El usuario de Lync en el sitio de red no está habilitado para el enrutamiento de Location-Based</span><span class="sxs-lookup"><span data-stu-id="ef83d-218">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef83d-219">Usuario de Lync 1 teléfono móvil (punto final de la RTC)</span><span class="sxs-lookup"><span data-stu-id="ef83d-219">Lync user 1 mobile phone (PSTN endpoint)</span></span></p></td>
<td><p><span data-ttu-id="ef83d-220">Llamada dirigida a través de la Directiva de enrutamiento de voz del sitio de red 1 y salida a través de la puerta de enlace del sitio 1</span><span class="sxs-lookup"><span data-stu-id="ef83d-220">Call routed through network site 1’s voice routing policy and egress via site 1 gateway</span></span></p></td>
<td><p><span data-ttu-id="ef83d-221">Llamada dirigida a través de la Directiva de enrutamiento de voz del sitio de red 2 y salida a través de la puerta de enlace del sitio 2</span><span class="sxs-lookup"><span data-stu-id="ef83d-221">Call routed through network site 2’s voice routing policy and egress via site 2 gateway</span></span></p></td>
<td><p><span data-ttu-id="ef83d-222">Llamada enrutada a través de la Directiva de voz de la persona que llama y se deshará a través de una puerta de enlace RTC no habilitada para enrutamiento de Location-Based</span><span class="sxs-lookup"><span data-stu-id="ef83d-222">Call routed through the caller voice policy and will egress via a PSTN gateway not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ef83d-223">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef83d-223">See Also</span></span>


[<span data-ttu-id="ef83d-224">Planificar el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef83d-224">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="ef83d-225"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef83d-225"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

