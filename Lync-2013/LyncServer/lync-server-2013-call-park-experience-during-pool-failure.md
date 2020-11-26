---
title: 'Lync Server 2013: Experiencia de estacionamiento de llamadas durante un error del grupo de servidores'
description: 'Lync Server 2013: experiencia de estacionamiento de llamadas durante un error de grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park experience during pool failure
ms:assetid: f6303e69-8771-492a-9e8b-c3d7ba231309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205383(v=OCS.15)
ms:contentKeyID: 48185831
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b97a0af13d378b0753979c32b6d5ffe7a525cf0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435701"
---
# <a name="call-park-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="f8b23-103">Experiencia de estacionamiento de llamadas durante un error del grupo de servidores en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8b23-103">Call Park experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8b23-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8b23-104">

<span> </span></span></span>

<span data-ttu-id="f8b23-105">_**Última modificación del tema:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="f8b23-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="f8b23-106">Cuando un grupo front-end no está disponible debido a un incidente no planeado, se desconectan las llamadas que se han detenido pero que aún no se han recuperado.</span><span class="sxs-lookup"><span data-stu-id="f8b23-106">When a Front End pool becomes unavailable due an unplanned incident, calls that have been parked but not yet retrieved are disconnected.</span></span> <span data-ttu-id="f8b23-107">Durante la conmutación por error a un grupo de copia de seguridad, los usuarios se redirigen al grupo de copia de seguridad y están en el modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="f8b23-107">During failover to a backup pool, users are redirected to the backup pool and are in resiliency mode.</span></span> <span data-ttu-id="f8b23-108">Mientras se encuentra en el modo de resistencia, los usuarios no pueden detener las llamadas, pero pueden poner las llamadas en espera y transferirlas.</span><span class="sxs-lookup"><span data-stu-id="f8b23-108">While in resiliency mode, users cannot park calls, but they can place calls on hold and transfer them.</span></span> <span data-ttu-id="f8b23-109">Cuando se completa la conmutación por error, las llamadas se pueden detener de nuevo y recuperar de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="f8b23-109">When failover is complete, calls can again be parked and retrieved as usual.</span></span> <span data-ttu-id="f8b23-110">Durante la conmutación por recuperación, los usuarios no pueden detener las llamadas hasta que no estén fuera del modo de resistencia.</span><span class="sxs-lookup"><span data-stu-id="f8b23-110">During failback, users cannot park calls until they are out of resiliency mode.</span></span>

<span data-ttu-id="f8b23-111">Durante la recuperación de desastres, los usuarios que se han redirigido al grupo de copia de seguridad como parte del proceso de conmutación por error usan la aplicación estacionamiento de llamadas que se implementa en el grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f8b23-111">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park application that is deployed in the backup pool.</span></span> <span data-ttu-id="f8b23-112">Por lo tanto, los usuarios redirigidos al grupo de copias de seguridad usan la configuración de estacionamiento de llamadas que están configurados para la aplicación de estacionamiento de llamada en el grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f8b23-112">Therefore, users who are redirected to the backup pool use the call park settings that are configured for the Call Park application in the backup pool.</span></span>

<span data-ttu-id="f8b23-113">La siguiente tabla resume la experiencia del parque de llamadas a través de las fases de la recuperación de desastres.</span><span class="sxs-lookup"><span data-stu-id="f8b23-113">The following table summarizes the Call Park experience through the phases of disaster recovery.</span></span>

### <a name="user-experience-during-disaster-recovery"></a><span data-ttu-id="f8b23-114">Experiencia del usuario durante la recuperación de desastres</span><span class="sxs-lookup"><span data-stu-id="f8b23-114">User Experience During Disaster Recovery</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8b23-115">Estado de la llamada</span><span class="sxs-lookup"><span data-stu-id="f8b23-115">Call state</span></span></th>
<th><span data-ttu-id="f8b23-116">Cuando se produce una interrupción</span><span class="sxs-lookup"><span data-stu-id="f8b23-116">When outage occurs</span></span></th>
<th><span data-ttu-id="f8b23-117">Durante la conmutación por error</span><span class="sxs-lookup"><span data-stu-id="f8b23-117">During failover</span></span></th>
<th><span data-ttu-id="f8b23-118">Durante la conmutación por recuperación</span><span class="sxs-lookup"><span data-stu-id="f8b23-118">During failback</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8b23-119">Llamada aún no deestacionada</span><span class="sxs-lookup"><span data-stu-id="f8b23-119">Call not yet parked</span></span></p></td>
<td><p><span data-ttu-id="f8b23-120">La llamada permanece conectada, pero no se puede detener.</span><span class="sxs-lookup"><span data-stu-id="f8b23-120">Call remains connected, but cannot be parked.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f8b23-121">Durante la conmutación por error, no se puede detener la llamada cuando los usuarios están en modo de resistencia, pero se pueden suspender y transferir.</span><span class="sxs-lookup"><span data-stu-id="f8b23-121">During failover, call cannot be parked while users are in resiliency mode, but can be put on hold and transferred.</span></span></p></li>
<li><p><span data-ttu-id="f8b23-122">Cuando se complete la conmutación por error, se podrá detener y recuperar la llamada.</span><span class="sxs-lookup"><span data-stu-id="f8b23-122">When failover completes, call can be parked and retrieved.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="f8b23-123">Durante la conmutación por recuperación, la llamada no se puede detener cuando los usuarios tienen el modo de resistencia, pero se pueden suspender y transferir.</span><span class="sxs-lookup"><span data-stu-id="f8b23-123">During failback, call cannot be parked while users are in resiliency mode, but can be put on hold and transferred.</span></span></p></li>
<li><p><span data-ttu-id="f8b23-124">Cuando se complete la conmutación por recuperación, se podrá detener y recuperar la llamada.</span><span class="sxs-lookup"><span data-stu-id="f8b23-124">When failback completes, call can be parked and retrieved.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8b23-125">Llamada estacionada, pero no recuperada aún</span><span class="sxs-lookup"><span data-stu-id="f8b23-125">Call parked, but not yet retrieved</span></span></p></td>
<td><p><span data-ttu-id="f8b23-126">La llamada está desconectada.</span><span class="sxs-lookup"><span data-stu-id="f8b23-126">Call is disconnected.</span></span></p></td>
<td><p><span data-ttu-id="f8b23-127">No hay llamadas en este estado.</span><span class="sxs-lookup"><span data-stu-id="f8b23-127">No calls in this state.</span></span></p></td>
<td><p><span data-ttu-id="f8b23-128">La llamada permanece aparcada.</span><span class="sxs-lookup"><span data-stu-id="f8b23-128">Call remains parked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8b23-129">Ya se ha recuperado una llamada estacionada</span><span class="sxs-lookup"><span data-stu-id="f8b23-129">Parked call already retrieved</span></span></p></td>
<td><p><span data-ttu-id="f8b23-130">La llamada permanece conectada.</span><span class="sxs-lookup"><span data-stu-id="f8b23-130">Call remains connected.</span></span></p></td>
<td><p><span data-ttu-id="f8b23-131">La llamada permanece conectada.</span><span class="sxs-lookup"><span data-stu-id="f8b23-131">Call remains connected.</span></span></p></td>
<td><p><span data-ttu-id="f8b23-132">La llamada permanece conectada.</span><span class="sxs-lookup"><span data-stu-id="f8b23-132">Call remains connected.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f8b23-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8b23-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

