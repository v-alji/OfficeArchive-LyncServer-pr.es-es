---
title: 'Lync Server 2013: Ubicación del usuario'
description: 'Lync Server 2013: Ubicación del usuario.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User's location
ms:assetid: ce57941d-086b-448e-8ada-c7d636a2a1c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994073(v=OCS.15)
ms:contentKeyID: 51803984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a92ec780809cdb3e1ee582ce6c348c884bbb5890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439173"
---
# <a name="users-location-in-lync-server-2013"></a><span data-ttu-id="901e3-103">Ubicación del usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="901e3-103">User's location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="901e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="901e3-104">

<span> </span></span></span>

<span data-ttu-id="901e3-105">_**Última modificación del tema:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="901e3-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="901e3-106">El enrutamiento de Location-Based aprovecha las mismas regiones, sitios y subredes de la red que se definen en Lync Server usado por E9-1-1, CAC y media bypass para aplicar restricciones de enrutamiento de llamadas para evitar la omisión de llamadas RTC.</span><span class="sxs-lookup"><span data-stu-id="901e3-106">Location-Based Routing leverages the same network regions, sites and subnets as defined in Lync Server used by E9-1-1, CAC and Media Bypass to apply call routing restrictions to prevent PSTN toll bypass.</span></span> <span data-ttu-id="901e3-107">La ubicación de un usuario viene determinada por la subred IP de los puntos de conexión de Lync del usuario.</span><span class="sxs-lookup"><span data-stu-id="901e3-107">A user’s location is determined by the IP subnet of the user’s Lync endpoint(s) are connected from.</span></span> <span data-ttu-id="901e3-108">Cada subred IP está asociada a un sitio de red, y los sitios de red se agrupan en regiones de red definidas por el administrador.</span><span class="sxs-lookup"><span data-stu-id="901e3-108">Each IP subnet is associated to a network site, which are aggregated into network regions defined by the administrator.</span></span> <span data-ttu-id="901e3-109">El enrutamiento basado en ubicación se aplica en función del sitio de red del usuario.</span><span class="sxs-lookup"><span data-stu-id="901e3-109">Location-Based Routing is enforced based on the user’s network site.</span></span>

<span data-ttu-id="901e3-110">Location-Based las reglas de enrutamiento se aplican por sitio de red, lo que significa que se aplicará a todos los puntos de conexión habilitados para Location-Based enrutamiento que se encuentren en el mismo sitio de red.</span><span class="sxs-lookup"><span data-stu-id="901e3-110">Location-Based Routing rules are applied on a per network site basis, meaning that a given set of rules will be applied to all endpoints enabled for Location-Based Routing that are located within the same network site.</span></span> <span data-ttu-id="901e3-111">Los administradores pueden aplicar el enrutamiento basado en ubicación a los sitios de red que lo necesiten.</span><span class="sxs-lookup"><span data-stu-id="901e3-111">Administrators can apply Location-Based Routing to network sites that require it.</span></span>

<span data-ttu-id="901e3-112">Se pueden definir directivas de enrutamiento de voz en cada sitio de red, para que todos los usuarios ubicados en el sitio de red utilicen una puerta de enlace RTC concreta para llamar a números de teléfono de RTC.</span><span class="sxs-lookup"><span data-stu-id="901e3-112">Voice routing policies can be defined on a per network site basis to define a particular PSTN gateway that should be used by all users located in the network site to call PSTN phone numbers.</span></span> <span data-ttu-id="901e3-113">Dichas directivas de enrutamiento de voz tendrán prioridad sobre el enrutamiento definido por la Directiva de voz del usuario cuando el usuario se encuentre en un sitio de red habilitado para Location-Based enrutamiento y evitará el enrutamiento de llamadas a través de puertas de enlace RTC habilitadas para Location-Based enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="901e3-113">Such voice routing policies will take precedence over the routing defined by the user’s voice policy when the user is located in a network site enabled for Location-Based Routing, and it will prevent the routing of calls via other PSTN gateways that are enabled for Location-Based Routing.</span></span> <span data-ttu-id="901e3-114">Cuando un usuario de Lync realiza una llamada RTC, la Directiva de voz del usuario determina si el usuario puede tener autorización para realizar la llamada.</span><span class="sxs-lookup"><span data-stu-id="901e3-114">When a Lync user places a PSTN call, the user’s voice policy determines whether the user can be authorized to place the call.</span></span> <span data-ttu-id="901e3-115">Si la Directiva de voz del usuario permite al usuario realizar la llamada, el enrutamiento de Location-Based determina qué puerta de enlace RTC debe salir de la llamada.</span><span class="sxs-lookup"><span data-stu-id="901e3-115">If the user’s voice policy allows the user to place the call, Location-Based Routing determines which PSTN gateway the call should egress from.</span></span> <span data-ttu-id="901e3-116">Location-Based enrutamiento realiza esta determinación en función de la ubicación del usuario.</span><span class="sxs-lookup"><span data-stu-id="901e3-116">Location-Based Routing makes this determination based on the user’s location.</span></span>

<span data-ttu-id="901e3-117">La ubicación de un usuario se puede clasificar de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="901e3-117">A user location can be categorized in the following ways:</span></span>

  - <span data-ttu-id="901e3-118">El usuario se encuentra en un sitio de red conocido habilitado para Location-Based enrutamiento y su número de realizado (marcado directo) termina en una puerta de enlace RTC situada en el mismo sitio de red (es decir, Office).</span><span class="sxs-lookup"><span data-stu-id="901e3-118">The user is located in a known network site enabled for Location-Based Routing and his DID (Direct Inward Dial) number terminates on a PSTN gateway placed in the same network site (i.e. office).</span></span> <span data-ttu-id="901e3-119">El enrutamiento de las llamadas salientes se realizará a través de la directiva de enrutamiento de voz del sitio de red en el que está ubicado el usuario.</span><span class="sxs-lookup"><span data-stu-id="901e3-119">The routing of outbound calls will be through the voice routing policy of the network site in which the user is located.</span></span> <span data-ttu-id="901e3-120">Las llamadas de RTC entrantes que reciba el usuario se redirigirán a los extremos ubicados en el mismo sitio de red que la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="901e3-120">Incoming PSTN calls to the user are routed to endpoints that are located in the same network site as the PSTN gateway.</span></span>

  - <span data-ttu-id="901e3-p105">El usuario está ubicado en un sitio de red conocido y diferente del sitio de red donde se encuentra la puerta de enlace RTC (es decir, el usuario viajó a otra oficina de la compañía). El enrutamiento de las llamadas salientes utilizará la directiva de enrutamiento de voz del sitio de red en el que está ubicado el usuario. Las llamadas de RTC entrantes que reciba el usuario no se redirigirán a los extremos ubicados en sitios diferentes del de la puerta de enlace RTC, para evitar que se omitan los números de pago de RTC.</span><span class="sxs-lookup"><span data-stu-id="901e3-p105">The user is located in a known network site that is in different from the network site where the PSTN gateway is located. (i.e. the user traveled to another corporate office). The routing of outbound calls will be using the voice routing policy of the network site in which the user is located. Incoming PSTN calls to the user will not be routed to endpoints that are located in different sites than the PSTN gateway to prevent PSTN toll bypassing.</span></span>

  - <span data-ttu-id="901e3-125">Cuando un usuario se encuentra en un sitio de red desconocido para la implementación de Lync Server, el enrutamiento de las llamadas salientes se basará en la Directiva de voz asignada al usuario a las puertas de enlace RTC no enlazadas a las restricciones de enrutamiento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="901e3-125">When a user is located in a network site that is unknown to the Lync Server deployment, the routing of outbound calls will be based on the voice policy assigned to the user to PSTN gateways not bound to Location-Based Routing restrictions.</span></span> <span data-ttu-id="901e3-126">Las llamadas de RTC entrantes no se redirigirán a los extremos ubicados en sitios de red desconocidos, para evitar que se omitan los números de pago de RTC.</span><span class="sxs-lookup"><span data-stu-id="901e3-126">Incoming PSTN calls will not be routed to endpoints that are located in unknown network sites to prevent PSTN toll bypassing.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="901e3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="901e3-127">See Also</span></span>


[<span data-ttu-id="901e3-128">Instrucciones para el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="901e3-128">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)  
  

<span data-ttu-id="901e3-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="901e3-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

