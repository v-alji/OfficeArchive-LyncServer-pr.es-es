---
title: 'Lync Server 2013: información general sobre la omisión de medios'
description: 'Lync Server 2013: información general sobre la omisión de medios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of media bypass
ms:assetid: 9ea090b3-f607-46f7-97dd-2510052524e5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412740(v=OCS.15)
ms:contentKeyID: 48184924
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3859c41a01ae5e7f1100a6872fd4e6747f45dbd8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399677"
---
# <a name="overview-of-media-bypass-in-lync-server-2013"></a><span data-ttu-id="864a3-103">Información general sobre la omisión de elementos multimedia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="864a3-103">Overview of media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="864a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="864a3-104">

<span> </span></span></span>

<span data-ttu-id="864a3-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="864a3-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="864a3-106">La omisión de elementos multimedia es útil cuando desea minimizar el número de servidores de mediación implementados.</span><span class="sxs-lookup"><span data-stu-id="864a3-106">Media bypass is useful when you want to minimize the number of Mediation Servers deployed.</span></span> <span data-ttu-id="864a3-107">Normalmente, un grupo de servidores de mediación se implementará en un sitio central y controlará las puertas de enlace en los sitios de sucursales.</span><span class="sxs-lookup"><span data-stu-id="864a3-107">Typically, a Mediation Server pool will be deployed at a central site, and it will control gateways at branch sites.</span></span> <span data-ttu-id="864a3-108">Habilitar la omisión de medios permite que las llamadas de la red telefónica conmutada (RTC) desde clientes en sitios de sucursal se dirijan directamente a través de las puertas de enlace a esos sitios.</span><span class="sxs-lookup"><span data-stu-id="864a3-108">Enabling media bypass allows media for public switched telephone network (PSTN) calls from clients at branch sites to flow directly through the gateways at those sites.</span></span> <span data-ttu-id="864a3-109">Las directivas de llamadas salientes de Lync Server 2013 y de Enterprise Voice deben configurarse correctamente para que las llamadas RTC de clientes de un sitio de sucursal se enruten a la puerta de enlace adecuada.</span><span class="sxs-lookup"><span data-stu-id="864a3-109">Lync Server 2013 outbound call routes and Enterprise Voice policies must be properly configured so that PSTN calls from clients at a branch site are routed to the appropriate gateway.</span></span>

<span data-ttu-id="864a3-p102">Las redes Wi-Fi suelen tener más pérdidas de paquetes que las redes por cable. En general, las puertas de enlace no pueden asumir la recuperación de la pérdida de paquetes. Por lo tanto, antes de decidir si necesitas habilitar la omisión de medios para una subred inalámbrica, te recomendamos evaluar la calidad de una red Wi-Fi. La reducción de latencia presenta una contrapartida respecto a la recuperación de la pérdida de paquetes que también necesitas tener en cuenta. RTAudio, un códec disponible para llamadas que no omiten el servidor de mediación, es más apropiado para la gestión de la pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="864a3-p102">Wi-Fi networks typically experience more packet loss than wired networks. Recovery from this packet loss is not typically something that can be accommodated by gateways. Therefore, we recommend that you evaluate the quality of a Wi-Fi network before determining whether bypass should be enabled for a wireless subnet. There is a tradeoff in latency reduction versus recovery from packet loss to consider, as well. RTAudio, a codec which is available for calls that do not bypass the Mediation Server, is better suited for handling packet loss.</span></span>

<span data-ttu-id="864a3-115">Una vez que la estructura de telefonía empresarial está en vigor, la planeación de la omisión de elementos multimedia es sencilla.</span><span class="sxs-lookup"><span data-stu-id="864a3-115">After your Enterprise Voice structure is in place, planning for media bypass is straightforward.</span></span>

  - <span data-ttu-id="864a3-116">Si tienes una topología centralizada sin vínculos WAN a sitios de sucursal, puedes habilitar la omisión de medios global porque no se necesita control de ajustes.</span><span class="sxs-lookup"><span data-stu-id="864a3-116">If you have a centralized topology without WAN links to branch sites, you can enable global media bypass, because fine-tuned control is unnecessary.</span></span>

  - <span data-ttu-id="864a3-117">Si tienes una topología distribuida compuesta de una o más regiones de red y sus sitios de sucursal afiliados, determina los aspectos siguientes:</span><span class="sxs-lookup"><span data-stu-id="864a3-117">If you have a distributed topology that consists of one or more network regions and their affiliated branch sites, determine the following:</span></span>
    
      - <span data-ttu-id="864a3-118">Si los componentes del mismo nivel del servidor de mediación pueden asumir las capacidades que se requieren para la omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="864a3-118">Whether your Mediation Server peers are able to support the capabilities required for media bypass.</span></span>
    
      - <span data-ttu-id="864a3-119">Los sitios de cada región de red que están bien conectados.</span><span class="sxs-lookup"><span data-stu-id="864a3-119">Which sites in each network region are well-connected.</span></span>
    
      - <span data-ttu-id="864a3-120">La combinación de la omisión de medios y el servicio de control de admisión de llamadas que es apropiada para la red.</span><span class="sxs-lookup"><span data-stu-id="864a3-120">Which combination of media bypass and call admission control is appropriate for your network.</span></span>

<span data-ttu-id="864a3-p103">Al habilitar la omisión de medios, se genera automáticamente un identificador de omisión único para una región de red y para todos los sitios de red que no tengan restricciones de ancho de banda en dicha región. A los sitios con restricciones de ancho de banda dentro de la región y a los sitios conectados a la región a través de vínculos WAN con restricciones de ancho de banda se les asignan sus propios identificadores de omisión únicos.</span><span class="sxs-lookup"><span data-stu-id="864a3-p103">When you enable media bypass, a unique bypass ID is automatically generated for a network region, and for all network sites without bandwidth constraints within that region. Sites with bandwidth constraints within the region and sites connected to the region over WAN links with bandwidth constraints are each assigned their own unique bypass IDs.</span></span>

<span data-ttu-id="864a3-123">Cuando un usuario realiza una llamada a la RTC, el servidor de mediación compara el identificador de omisión de la subred del cliente con el identificador de omisión de la subred de la puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="864a3-123">When a user makes a call to the PSTN, the Mediation Server compares the bypass ID of the client subnet with the bypass ID of the gateway subnet.</span></span> <span data-ttu-id="864a3-124">Si los dos identificadores de omisión coinciden, se usará la omisión de medios para la llamada.</span><span class="sxs-lookup"><span data-stu-id="864a3-124">If the two bypass IDs match, media bypass is used for the call.</span></span> <span data-ttu-id="864a3-125">Si los identificadores de omisión no coinciden, el medio para la llamada debe fluir por el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="864a3-125">If the bypass IDs do not match, media for the call must flow through the Mediation Server.</span></span>

<span data-ttu-id="864a3-126">Cuando un usuario recibe una llamada de la RTC, el cliente del usuario compara su identificador de omisión con el de la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="864a3-126">When a user receives a call from the PSTN, the user’s client compares its bypass ID to that of the PSTN gateway.</span></span> <span data-ttu-id="864a3-127">Si los dos identificadores de omisión coinciden, los medios fluyen directamente de la puerta de enlace al cliente, omitiendo el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="864a3-127">If the two bypass IDs match, media flows directly from the gateway to the client, bypassing the Mediation Server.</span></span>

<span data-ttu-id="864a3-128">Solo los clientes y dispositivos de Lync 2010 o superior admiten interacciones de omisión de contenido multimedia con un servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="864a3-128">Only Lync 2010 or above clients and devices support media bypass interactions with a Mediation Server.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="864a3-p106">Además de habilitar la omisión de medios de manera global, necesitas habilitar la omisión de medios en cada tronco RTC de forma individual. Si la omisión se habilita globalmente, pero no se habilita en un determinado tronco RTC, no se invocará la omisión de medios en ninguna de las llamadas en las que intervenga ese tronco RTC. Asimismo, si la omisión de medios se define en <STRONG>Usar información de región y sitio</STRONG>, todas las subredes que se pueden redirigir necesitan asociarse con los sitios en los que se ubican. Si en un sitio hay subredes que se pueden redirigir en las que no se desea habilitar la omisión, dichas subredes necesitan agruparse en un sitio nuevo antes de habilitar la omisión de medios. Esta acción asegurará que las subredes que no se pueden redirigir tengan asignado un identificador de omisión diferente.</span><span class="sxs-lookup"><span data-stu-id="864a3-p106">In addition to enabling media bypass globally, you must enable media bypass individually on each PSTN trunk. If bypass is enabled globally, but is not enabled for a particular PSTN trunk, media bypass will not be invoked for any calls involving that PSTN trunk. In addition, when media bypass is set to <STRONG>Use Site and Region Information</STRONG>, you must associate all routable subnets with the sites in which they are located. If there are routable subnets within a site for which bypass is not wanted, these subnets should be grouped within a new site before you enable media bypass. Doing so will assure that the unroutable subnets are assigned a different bypass ID.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="864a3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="864a3-134">See Also</span></span>


[<span data-ttu-id="864a3-135">Modos de omisión de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="864a3-135">Media bypass modes in Lync Server 2013</span></span>](lync-server-2013-media-bypass-modes.md)  
[<span data-ttu-id="864a3-136">Omisión de medios y control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="864a3-136">Media bypass and call admission control in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-call-admission-control.md)  
[<span data-ttu-id="864a3-137">Requisitos técnicos para la omisión de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="864a3-137">Technical requirements for media bypass in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-media-bypass.md)  
  

<span data-ttu-id="864a3-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="864a3-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

