---
title: 'Lync Server 2013: Consideraciones técnicas para el enrutamiento basado en ubicación'
description: 'Lync Server 2013: consideraciones técnicas para el enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical considerations for Location-Based Routing
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994027(v=OCS.15)
ms:contentKeyID: 51803936
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54a025af81ab148ad41f95d0a8cf4f900beb7e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423431"
---
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="c7d24-103">Consideraciones técnicas para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7d24-103">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c7d24-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c7d24-104">

<span> </span></span></span>

<span data-ttu-id="c7d24-105">_**Última modificación del tema:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="c7d24-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="c7d24-106">Al planear Location-Based el enrutamiento, debe considerar el impacto en los siguientes escenarios.</span><span class="sxs-lookup"><span data-stu-id="c7d24-106">When planning Location-Based Routing, you should consider the impact to the following scenarios.</span></span>

<div>

## <a name="disaster-recovery"></a><span data-ttu-id="c7d24-107">Recuperación ante desastres</span><span class="sxs-lookup"><span data-stu-id="c7d24-107">Disaster Recovery</span></span>

<span data-ttu-id="c7d24-108">Durante una conmutación por error del repositorio principal a un grupo de copia de seguridad, así como al restaurar las operaciones normales en el grupo principal, el enrutamiento de Location-Based se aplica en todo momento durante un procedimiento de recuperación y desastres.</span><span class="sxs-lookup"><span data-stu-id="c7d24-108">During a failover from the primary pool to a backup pool as well as when restoring normal operations to the primary pool, Location-Based Routing remains enforced at all times during a disaster and recovery procedure.</span></span>

</div>

<div>

## <a name="survivable-branch-appliance"></a><span data-ttu-id="c7d24-109">Aplicación de sucursal con funciones de supervivencia</span><span class="sxs-lookup"><span data-stu-id="c7d24-109">Survivable Branch Appliance</span></span>

<span data-ttu-id="c7d24-110">La configuración del enrutamiento de Location-Based afecta al planeamiento de la ubicación en la que se implementan las puertas de enlace asociadas a los equipos de las sucursales que son revivientes.</span><span class="sxs-lookup"><span data-stu-id="c7d24-110">Configuring Location-Based Routing impacts the planning of where you deploy the gateways associated to your Survivable Branch Appliances.</span></span> <span data-ttu-id="c7d24-111">La puerta de enlace asociada a su SBA debe estar ubicada en el mismo sitio de red que su equipo de sucursal con la supervivencia; de lo contrario, los usuarios alojados en su equipo de sucursal con su supervivencia no podrán realizar llamadas salientes si Location-Based enrutamiento está configurado.</span><span class="sxs-lookup"><span data-stu-id="c7d24-111">The gateway associated to your SBA must be located in the same network site as your Survivable Branch Appliance; otherwise, users homed on your Survivable Branch Appliance will not be permitted to place outbound calls if Location-Based Routing is configured.</span></span> <span data-ttu-id="c7d24-112">Cuando la conexión WAN entre el equipo de la sucursal y el sitio central está inactiva, se exige la aplicación de las restricciones de enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="c7d24-112">When the WAN connection between your Survivable Branch Appliance and the central site is down, Location-Based Routing restrictions remains enforced.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c7d24-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7d24-113">See Also</span></span>


[<span data-ttu-id="c7d24-114">Planificar el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7d24-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="c7d24-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c7d24-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

