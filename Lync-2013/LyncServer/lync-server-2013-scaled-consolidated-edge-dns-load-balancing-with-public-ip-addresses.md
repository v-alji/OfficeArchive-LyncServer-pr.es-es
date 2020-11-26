---
title: Perímetro consolidado escalado, equilibrio de carga DNS con direcciones IP públicas
description: Borde consolidado escalado, equilibrio de carga DNS con direcciones IP públicas.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: 2b854f6d-3d3f-4961-a5f8-a03f47740df0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204761(v=OCS.15)
ms:contentKeyID: 48183698
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4d382fe7d25b4fae8c91073451d7d8b4f3f113b5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442075"
---
# <a name="scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="d66e4-103">Perímetro consolidado escalado, equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d66e4-103">Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d66e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d66e4-104">

<span> </span></span></span>

<span data-ttu-id="d66e4-105">_**Última modificación del tema:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="d66e4-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="d66e4-106">En la topología del grupo de servidores perimetrales, dos o más servidores perimetrales se implementan como un grupo de carga equilibrada en la red perimetral del centro de datos.</span><span class="sxs-lookup"><span data-stu-id="d66e4-106">In the Edge Server pool topology, two or more Edge Servers are deployed as a load-balanced pool in the perimeter network of the data center.</span></span> <span data-ttu-id="d66e4-107">El equilibrio de carga del sistema de nombres de dominio (DNS) se usa para el tráfico tanto en la interfaz de borde interno como en la externa.</span><span class="sxs-lookup"><span data-stu-id="d66e4-107">Domain Name System (DNS) load balancing is used for traffic to both the external and internal Edge interfaces.</span></span>

<span data-ttu-id="d66e4-108">Si su organización requiere soporte técnico para más de 15.000 conexiones de cliente del servicio perimetral de acceso, 1.000 conexiones de cliente activas de servicios de conferencias web de Lync Server, o 500 de concurrentes las sesiones de los bordes A/V, y/o la alta disponibilidad del servidor perimetral es importante, esta topología ofrece las ventajas de la escalabilidad y la compatibilidad con la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="d66e4-108">If your organization requires support for more than 15,000 Access Edge service client connections, 1,000 active Lync Server Web Conferencing service client connections, or 500 concurrent A/V Edge sessions, and/or high availability of the Edge Server is important, this topology offers the advantages of scalability and failover support.</span></span>

<span data-ttu-id="d66e4-109">La figura no muestra los directores, un rol de servidor opcional implementado en la red interna entre los servidores perimetrales y los grupos de servidores front-end o el servidor.</span><span class="sxs-lookup"><span data-stu-id="d66e4-109">The figure does not show Directors, an optional server role deployed in the internal network between the Edge Servers and your Front End pools or server.</span></span> <span data-ttu-id="d66e4-110">Para obtener más información sobre la topología para directores, consulte [componentes necesarios para el director de Lync Server 2013](lync-server-2013-components-required-for-the-director.md).</span><span class="sxs-lookup"><span data-stu-id="d66e4-110">For details about the topology for Directors, see [Components required for the Director in Lync Server 2013](lync-server-2013-components-required-for-the-director.md).</span></span> <span data-ttu-id="d66e4-111">La figura representa un único proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="d66e4-111">The figure represents a single reverse proxy.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="d66e4-112">La cifra que se muestra es para la orientación y el direccionamiento IP de ejemplo, pero no tiene la intención de representar los flujos de comunicación reales con el tráfico entrante y saliente correcto.</span><span class="sxs-lookup"><span data-stu-id="d66e4-112">The figure shown is for orientation and example IP addressing, but does not intend to represent actual communication flows with the correct incoming and outgoing traffic.</span></span> <span data-ttu-id="d66e4-113">La figura representa una vista de alto nivel del tráfico posible.</span><span class="sxs-lookup"><span data-stu-id="d66e4-113">The figure represents a high level view of possible traffic.</span></span> <span data-ttu-id="d66e4-114">Los detalles del flujo de tráfico según pertenecen a los puertos entrante (en los que se escuchan) y salientes (a los servidores de destino o a los clientes) se representan en el diagrama de Resumen de puertos en cada escenario.</span><span class="sxs-lookup"><span data-stu-id="d66e4-114">Details for traffic flow as they pertain to incoming (to listening ports) and outgoing (to destination servers or clients) is represented in the Port Summary diagram in each scenario.</span></span> <span data-ttu-id="d66e4-115">Por ejemplo, TCP 443 es realmente entrante (solo para el extremo o proxy inverso) y es solo un flujo bidireccional desde una perspectiva de protocolo (TCP).</span><span class="sxs-lookup"><span data-stu-id="d66e4-115">For example, TCP 443 is actually inbound (to the Edge or reverse proxy) only, and is only a two-way flow from a protocol (TCP) perspective.</span></span> <span data-ttu-id="d66e4-116">Además, la figura muestra la naturaleza del tráfico cuando cambia cuando se produce NAT (traducción de direcciones de red) (la dirección de destino se cambia en entrante; la dirección de origen se cambia en saliente).</span><span class="sxs-lookup"><span data-stu-id="d66e4-116">Additionally, the figure shows the nature of traffic as it changes when NAT (network address translation) occurs (destination address is changed on inbound, source address is changed on outbound).</span></span> <span data-ttu-id="d66e4-117">Ejemplo de firewall externo e interno, y las interfaces de servidor se muestran solo con fines de referencia.</span><span class="sxs-lookup"><span data-stu-id="d66e4-117">Example external and internal firewall, and server interfaces are shown for reference purposes only.</span></span> <span data-ttu-id="d66e4-118">Por último, se muestra ejemplo de puerta de enlace predeterminada y relaciones de ruta, cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="d66e4-118">Finally, example default gateway and route relationships are shown, where applicable.</span></span> <span data-ttu-id="d66e4-119">Observe también que el diagrama usa la zona DNS <EM>. com</EM> para representar la zona DNS externa tanto para el proxy inverso como con los servidores perimetrales, y la zona DNS de <EM>.net</EM> hace referencia a la zona DNS interna.</span><span class="sxs-lookup"><span data-stu-id="d66e4-119">Note also that the diagram uses the <EM>.com</EM> DNS zone to represent the external DNS zone for both reverse proxy and Edge Servers, and the <EM>.net</EM> DNS zone refers to the internal DNS zone.</span></span>



</div>

<span data-ttu-id="d66e4-120">Las novedades de Microsoft Lync Server 2013 son compatibilidad con el direccionamiento IPv6.</span><span class="sxs-lookup"><span data-stu-id="d66e4-120">New to Microsoft Lync Server 2013 is support for IPv6 addressing.</span></span> <span data-ttu-id="d66e4-121">Al igual que con el direccionamiento IPv4, las direcciones IPv6 deben asignarse de forma que las direcciones formen parte del espacio de direcciones IPv6 asignado.</span><span class="sxs-lookup"><span data-stu-id="d66e4-121">Much like IPv4 addressing, IPv6 addresses must be assigned in such a way that the addresses are part of your assigned IPv6 address space.</span></span> <span data-ttu-id="d66e4-122">Las direcciones de este tema solo son por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d66e4-122">The addresses in this topic are for example only.</span></span> <span data-ttu-id="d66e4-123">Debe adquirir direcciones IPv6 que funcionen en su implementación, proporcionar el ámbito correcto y interoperar con direcciones internas y externas.</span><span class="sxs-lookup"><span data-stu-id="d66e4-123">You must acquire IPv6 addresses that will function in your deployment, provide the correct scope and will interoperate with internal and external addressing.</span></span> <span data-ttu-id="d66e4-124">Windows Server proporciona una característica importante para la operación de IPv6 de transición y la comunicación de IPv4 a IPv6 denominada *pila dual*.</span><span class="sxs-lookup"><span data-stu-id="d66e4-124">Windows Server provides a feature that is important to transitional IPv6 operation and IPv4 to IPv6 communication called the *dual stack*.</span></span> <span data-ttu-id="d66e4-125">La pila dual es una pila de red separada y distinta para IPv4 y para IPv6.</span><span class="sxs-lookup"><span data-stu-id="d66e4-125">The dual stack is a separate and distinct network stack for IPv4 and for IPv6.</span></span> <span data-ttu-id="d66e4-126">La pila dual es lo que le permite asignar direcciones IPv4 e IPv6 al mismo tiempo y permite que el servidor se comunique con otros hosts y clientes en función de sus requisitos.</span><span class="sxs-lookup"><span data-stu-id="d66e4-126">The dual stack is what allows you to assign addressing for IPv4 and IPv6 concurrently, and allows the server to communicate with other hosts and clients based on what their requirements are.</span></span>

<span data-ttu-id="d66e4-127">Los tipos de dirección típicos que usará para el direccionamiento IPv6 serán las direcciones globales de IPv6 (similares a las direcciones IPv4 públicas), las direcciones locales IPv6 únicas (similares a los intervalos de direcciones IPv4 privadas) y las direcciones locales del vínculo IPv6 (similares a las direcciones IP privadas automáticas en Windows Server para IPv4).</span><span class="sxs-lookup"><span data-stu-id="d66e4-127">Typical address types that you will use for IPv6 addressing will be the IPv6 global addresses (similar to public IPv4 addresses), IPv6 unique local addresses (similar to the private IPv4 address ranges) and IPv6 link-local addresses (similar to automatic private IP addresses in Windows Server for IPv4)</span></span>

<span data-ttu-id="d66e4-128">Existen tecnologías de traducción de direcciones de red (NAT) para IPv6 que permitirán NAT IPv6 a IPv4 (comúnmente denominado NAT64) y para NAT IPv6 a IPv6 (comúnmente conocido como NAT66).</span><span class="sxs-lookup"><span data-stu-id="d66e4-128">Network address translation technologies (NAT) for IPv6 exist that will allow for NAT IPv6 to IPv4 (commonly referred to as NAT64) and for NAT IPv6 to IPv6 (commonly referred to as NAT66).</span></span> <span data-ttu-id="d66e4-129">La existencia de tecnologías NAT significa que los cinco escenarios presentados para los servidores perimetrales de Lync Server siguen siendo válidos.</span><span class="sxs-lookup"><span data-stu-id="d66e4-129">The existence of NAT technologies means that the five scenarios presented for Lync Server Edge Servers are still valid.</span></span>

<div>


> [!WARNING]
> <span data-ttu-id="d66e4-130">IPv6 es un tema complejo y requiere un cuidadoso planeamiento con el equipo de redes y el proveedor de Internet para garantizar que las direcciones que asigne en el nivel de servidor de Windows y en el nivel de 2013 de Lync Server funcionen de la manera esperada.</span><span class="sxs-lookup"><span data-stu-id="d66e4-130">IPv6 is a complex topic and requires careful planning with your networking team and your Internet provider to ensure that the addresses you assign at the Windows server level and at the Lync Server 2013 level will work as expected.</span></span> <span data-ttu-id="d66e4-131">Vea los vínculos del final de este tema para conocer otros recursos sobre la planeación y el direccionamiento de IPv6.</span><span class="sxs-lookup"><span data-stu-id="d66e4-131">See the links at the end of this topic for additional resources on IPv6 addressing and planning.</span></span>



</div>

<span data-ttu-id="d66e4-132">![7c1e3e6b-9b1b-4ac6-b0e7-9c256dbc2537](images/JJ204761.7c1e3e6b-9b1b-4ac6-b0e7-9c256dbc2537(OCS.15).jpg "7c1e3e6b-9b1b-4ac6-b0e7-9c256dbc2537")</span><span class="sxs-lookup"><span data-stu-id="d66e4-132">![7c1e3e6b-9b1b-4ac6-b0e7-9c256dbc2537](images/JJ204761.7c1e3e6b-9b1b-4ac6-b0e7-9c256dbc2537(OCS.15).jpg "7c1e3e6b-9b1b-4ac6-b0e7-9c256dbc2537")</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="d66e4-133">Si está usando control de admisión de llamadas (CAC), aún debe asignar direcciones IPv4 a la interfaz interna del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="d66e4-133">If you are using Call Admission Control (CAC), you still must assign IPv4 addresses to the Edge Server internal interface.</span></span> <span data-ttu-id="d66e4-134">CAC usa direcciones IPv4 y debe tener disponibles para funcionar.</span><span class="sxs-lookup"><span data-stu-id="d66e4-134">CAC uses IPv4 addresses and must have them available to operate.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d66e4-135">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d66e4-135">In This Section</span></span>

  - [<span data-ttu-id="d66e4-136">Resumen de certificado - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d66e4-136">Certificate summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="d66e4-137">Resumen de puerto - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d66e4-137">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="d66e4-138">Resumen de DNS - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d66e4-138">DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d66e4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d66e4-139">See Also</span></span>


[<span data-ttu-id="d66e4-140">Arquitectura de direccionamiento de IP versión 6</span><span class="sxs-lookup"><span data-stu-id="d66e4-140">IP Version 6 Addressing Architecture</span></span>](https://tools.ietf.org/html/rfc4291)  
[<span data-ttu-id="d66e4-141">Formato de dirección global de unidifusión IPv6</span><span class="sxs-lookup"><span data-stu-id="d66e4-141">IPv6 Global Unicast Address Format</span></span>](https://tools.ietf.org/html/rfc3587)  
[<span data-ttu-id="d66e4-142">Direcciones de unidifusión IPv6 locales únicas</span><span class="sxs-lookup"><span data-stu-id="d66e4-142">Unique Local IPv6 Unicast Addresses</span></span>](https://tools.ietf.org/html/rfc4193)  
  

<span data-ttu-id="d66e4-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d66e4-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

