---
title: 'Lync Server 2013: Planificar el enrutamiento basado en ubicación'
description: 'Lync Server 2013: planeamiento de enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Location-Based Routing
ms:assetid: bb035924-6b52-4f0f-8e05-b76864fb9ef3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994068(v=OCS.15)
ms:contentKeyID: 51803979
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 894a596e998fe07b97ad7911441eced670ba85b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442953"
---
# <a name="planning-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="0b982-103">Planificar el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-103">Planning for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b982-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b982-104">

<span> </span></span></span>

<span data-ttu-id="0b982-105">_**Última modificación del tema:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="0b982-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="0b982-106">La información de este tema se refiere a las actualizaciones acumulativas de Lync Server 2013: febrero de 2013.</span><span class="sxs-lookup"><span data-stu-id="0b982-106">The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>

<span data-ttu-id="0b982-107">Location-Based el enrutamiento permite restringir el enrutamiento de llamadas entre puntos de conexión VoIP y puntos de conexión RTC en función de la ubicación de las partes en la llamada.</span><span class="sxs-lookup"><span data-stu-id="0b982-107">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="0b982-108">Location-Based el enrutamiento es parte de la infraestructura de telefonía IP empresarial de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0b982-108">Location-Based Routing is part of the Lync Server 2013 Enterprise Voice infrastructure.</span></span> <span data-ttu-id="0b982-109">Location-Based el enrutamiento es una característica de administración de llamadas que controla cómo Lync Server 2013 CU1 dirige las llamadas.</span><span class="sxs-lookup"><span data-stu-id="0b982-109">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="0b982-110">Aplica reglas de autorización de llamadas si las llamadas se pueden enrutar a puntos de conexión PBX o RTC en función de la ubicación geográfica de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="0b982-110">It enforces call authorization rules on whether calls can be routed to PBX or PSTN endpoints based on the Lync caller’s geographic location.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0b982-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="0b982-111">In This Section</span></span>

  - [<span data-ttu-id="0b982-112">Información general sobre el enrutamiento de Location-Based en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-112">Overview of Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing.md)

  - [<span data-ttu-id="0b982-113">Instrucciones para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-113">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)

  - [<span data-ttu-id="0b982-114">Escenarios para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-114">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)

  - [<span data-ttu-id="0b982-115">Consideraciones técnicas para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-115">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-technical-considerations-for-location-based-routing.md)

  - [<span data-ttu-id="0b982-116">Compatibilidad de cliente y servidor para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-116">Client and server support for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-client-and-server-support-for-location-based-routing.md)

  - [<span data-ttu-id="0b982-117">Capacidades no compatibles con el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-117">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-capabilities-not-supported-by-location-based-routing.md)

  - [<span data-ttu-id="0b982-118">Proceso de implementación para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-118">Deployment process for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-location-based-routing.md)

  - [<span data-ttu-id="0b982-119">Enrutamiento basado en la ubicación de las conferencias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-119">Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-for-conferencing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0b982-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b982-120">See Also</span></span>


[<span data-ttu-id="0b982-121">Planificación de telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b982-121">Planning for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice.md)  
  

<span data-ttu-id="0b982-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b982-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

