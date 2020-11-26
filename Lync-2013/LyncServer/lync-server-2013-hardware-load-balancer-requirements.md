---
title: 'Lync Server 2013: Requisitos del equilibrador de carga de hardware'
description: Requisitos del equilibrador de carga de hardware de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware load balancer requirements
ms:assetid: 32891268-2059-43d0-adf4-af4ff1e9ce66
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ656815(v=OCS.15)
ms:contentKeyID: 49287208
ms.date: 05/11/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69cbf79c1fd7551dfd428c23ed22c924d0805c43
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427722"
---
# <a name="hardware-load-balancer-requirements-for-lync-server-2013"></a><span data-ttu-id="93a5b-103">Requisitos del equilibrador de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93a5b-103">Hardware load balancer requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93a5b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93a5b-104">

<span> </span></span></span>

<span data-ttu-id="93a5b-105">_**Última modificación del tema:** 2015-05-11_</span><span class="sxs-lookup"><span data-stu-id="93a5b-105">_**Topic Last Modified:** 2015-05-11_</span></span>

<span data-ttu-id="93a5b-106">La topología de borde consolidado de Lync Server 2013 escalada está optimizada para el equilibrio de carga de DNS para implementaciones nuevas que se federan principalmente con otras organizaciones que usan Lync Server.</span><span class="sxs-lookup"><span data-stu-id="93a5b-106">The Lync Server 2013 scaled consolidated Edge topology is optimized for DNS load balancing for new deployments federating primarily with other organizations using Lync Server.</span></span> <span data-ttu-id="93a5b-107">Si se requiere una alta disponibilidad para cualquiera de los siguientes escenarios, se debe usar un equilibrador de carga de hardware en los grupos de servidores perimetrales para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="93a5b-107">If high availability is required for any of the following scenarios, a hardware load balancer must be used on Edge Server pools for the following:</span></span>

  - <span data-ttu-id="93a5b-108">Federación con organizaciones que usan Office Communications Server 2007 R2 u Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="93a5b-108">Federation with organizations using Office Communications Server 2007 R2 or Office Communications Server 2007</span></span>

  - <span data-ttu-id="93a5b-109">Mensajería unificada de Exchange para usuarios remotos que usan la mensajería unificada de Exchange antes de Exchange 2010 con SP1</span><span class="sxs-lookup"><span data-stu-id="93a5b-109">Exchange UM for remote users using Exchange UM prior to Exchange 2010 with SP1</span></span>

  - <span data-ttu-id="93a5b-110">Conectividad con usuarios de mensajería instantánea (MI) pública</span><span class="sxs-lookup"><span data-stu-id="93a5b-110">Connectivity to public IM users</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="93a5b-p102">No se admite el uso del equilibrio de carga de DNS en una interfaz y del equilibrio de carga de hardware en otra. Necesita utilizar el equilibrio de carga de hardware o de DNS en ambas interfaces.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p102">Using DNS load balancing on one interface and hardware load balancing on the other is not supported. You must use hardware load balancing for both interfaces or DNS load balancing for both.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="93a5b-p103">Si usa un equilibrador de carga de hardware, el equilibrador de carga que se haya implementado para las conexiones con la red interna necesitará configurarse para que solo equilibre la carga del tráfico de los servidores que ejecuten el servicio perimetral de acceso y el servicio perimetral A/V. No puede equilibrar la carga del tráfico al servicio perimetral de conferencia web interno o al servicio proxy XMPP interno.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p103">If you are using a hardware load balancer, the load balancer deployed for connections with the internal network must be configured to load balance only the traffic to servers running the Access Edge service and the A/V Edge service. It cannot load balance the traffic to the internal Web Conferencing Edge service or the internal XMPP Proxy service.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="93a5b-115">El NAT de Return de servidor directo (DSR) no es compatible con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93a5b-115">The direct server return (DSR) NAT is not supported with Lync Server 2013.</span></span>



</div>

<span data-ttu-id="93a5b-116">Para determinar si su equilibrador de carga de hardware admite las características necesarias para Lync Server 2013, consulte "Lync Server 2010 de equilibrador de carga" en [https://go.microsoft.com/fwlink/p/?linkId=202452](https://go.microsoft.com/fwlink/p/?linkid=202452) .</span><span class="sxs-lookup"><span data-stu-id="93a5b-116">To determine whether your hardware load balancer supports the necessary features required by Lync Server 2013, see "Lync Server 2010 Load Balancer Partners" at [https://go.microsoft.com/fwlink/p/?linkId=202452](https://go.microsoft.com/fwlink/p/?linkid=202452).</span></span>

<div>

## <a name="hardware-load-balancer-requirements-for-edge-servers-running-the-av-edge-service"></a><span data-ttu-id="93a5b-117">Requisitos de equilibrador de carga de hardware para servidores perimetrales que ejecutan el servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="93a5b-117">Hardware Load Balancer Requirements for Edge Servers Running the A/V Edge Service</span></span>

<span data-ttu-id="93a5b-118">Estos son los requisitos del equilibrador de carga de hardware para los servidores perimetrales que ejecutan el servicio perimetral A/V:</span><span class="sxs-lookup"><span data-stu-id="93a5b-118">Following are the hardware load balancer requirements for Edge Servers running the A/V Edge service:</span></span>

  - <span data-ttu-id="93a5b-p104">Deshabilitar el algoritmo de Nagle de TCP para los puertos 443 internos y externos. El algoritmo de Nagle es el proceso de combinación de varios paquetes pequeños en un único paquete más grande para obtener una transmisión más eficiente.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p104">Turn off TCP nagling for both internal and external ports 443. Nagling is the process of combining several small packets into a single, larger packet for more efficient transmission.</span></span>

  - <span data-ttu-id="93a5b-121">Deshabilitar el algoritmo de Nagle de TCP para el intervalo de puertos externos de 50 000 a 59 999.</span><span class="sxs-lookup"><span data-stu-id="93a5b-121">Turn off TCP nagling for external port range 50,000 – 59,999.</span></span>

  - <span data-ttu-id="93a5b-122">No utilizar NAT en el firewall interno o externo.</span><span class="sxs-lookup"><span data-stu-id="93a5b-122">Do not use NAT on the internal or external firewall.</span></span>

  - <span data-ttu-id="93a5b-123">La interfaz interna de Edge debe estar en una red diferente a la de la interfaz externa del servidor perimetral y el enrutamiento entre ellas debe estar deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="93a5b-123">The edge internal interface must be on a different network than the Edge Server external interface and routing between them must be disabled.</span></span>

  - <span data-ttu-id="93a5b-124">La interfaz externa del servidor perimetral que ejecuta el servicio de borde A/V debe usar direcciones IP enrutables públicamente y sin traducción de NAT o puerto en ninguna de las direcciones IP externas de Edge.</span><span class="sxs-lookup"><span data-stu-id="93a5b-124">The external interface of the Edge Server running the A/V Edge Service must use publicly routable IP addresses and no NAT or port translation on any of the edge external IP addresses.</span></span>

</div>

<div>

## <a name="hardware-load-balancer-requirements"></a><span data-ttu-id="93a5b-125">Requisitos del equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="93a5b-125">Hardware Load Balancer Requirements</span></span>

<span data-ttu-id="93a5b-126">Los requisitos de afinidad basados en cookies se reducen enormemente en Lync Server 2013 para servicios Web.</span><span class="sxs-lookup"><span data-stu-id="93a5b-126">Cookie-based affinity requirements are greatly reduced in Lync Server 2013 for Web services.</span></span> <span data-ttu-id="93a5b-127">Si implementa Lync Server 2013 y no va a conservar ninguno de los servidores front-end de Lync Server 2010 ni los grupos front-end, no necesita persistencia basada en cookies.</span><span class="sxs-lookup"><span data-stu-id="93a5b-127">If you are deploying Lync Server 2013 and will not retain any Lync Server 2010 Front End Servers or Front End pools, you do not need cookie-based persistence.</span></span> <span data-ttu-id="93a5b-128">Sin embargo, si conservará de forma temporal o permanente los servidores front-end de Lync Server 2010 o las agrupaciones front end, seguirá usando la persistencia basada en cookies a medida que se implemente y se configure para Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="93a5b-128">However, if you will temporarily or permanently retain any Lync Server 2010 Front End Servers or Front End pools, you still use cookie-based persistence as it is deployed and configured for Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="93a5b-129"><STRONG>La utilización de la afinidad basada en cookies pese a que su implementación no la necesite</STRONG> no tiene repercusiones.</span><span class="sxs-lookup"><span data-stu-id="93a5b-129"><STRONG>If you decide to use cookie-based affinity even though your deployment does not require it</STRONG>, there is no negative impact to doing so.</span></span>



</div>

<span data-ttu-id="93a5b-130">Para las implementaciones que **no utilizarán** la afinidad basada en cookies:</span><span class="sxs-lookup"><span data-stu-id="93a5b-130">For deployments that **will not use** cookie-based affinity:</span></span>

  - <span data-ttu-id="93a5b-p106">En la regla de publicación del proxy inverso para el puerto 4443, establezca **Reenviar encabezado de host** en True. Esto garantizará que se reenviará la dirección URL original.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p106">On the reverse proxy publishing rule for port 4443, set **Forward host header** to True. This will ensure that the original URL is forwarded.</span></span>

<span data-ttu-id="93a5b-133">Para las implementaciones que **utilizarán** la afinidad basada en cookies:</span><span class="sxs-lookup"><span data-stu-id="93a5b-133">For deployments that **will use** cookie-based affinity:</span></span>

  - <span data-ttu-id="93a5b-p107">En la regla de publicación del proxy inverso para el puerto 4443, establezca **Reenviar encabezado de host** en True. Esto garantizará que se reenviará la dirección URL original.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p107">On the reverse proxy publishing rule for port 4443, set **Forward host header** to True. This will ensure that the original URL is forwarded.</span></span>

  - <span data-ttu-id="93a5b-136">La cookie del equilibrador de carga de hardware NO NECESITA estar marcada como httpOnly</span><span class="sxs-lookup"><span data-stu-id="93a5b-136">Hardware load balancer cookie MUST NOT be marked httpOnly</span></span>

  - <span data-ttu-id="93a5b-137">La cookie del equilibrador de carga de hardware NO NECESITA tener tiempo de expiración</span><span class="sxs-lookup"><span data-stu-id="93a5b-137">Hardware load balancer cookie MUST NOT have an expiration time</span></span>

  - <span data-ttu-id="93a5b-138">La cookie del equilibrador de carga de hardware NECESITA tener el nombre **MS-WSMAN** (este es el valor esperado por los servicios web y no puede modificarse)</span><span class="sxs-lookup"><span data-stu-id="93a5b-138">Hardware load balancer cookie MUST be named **MS-WSMAN** (This is the value that the Web services expect, and cannot be changed)</span></span>

  - <span data-ttu-id="93a5b-p108">La cookie del equilibrador de carga de hardware NECESITA estar establecida en cada respuesta HTTP para la que la solicitud HTTP entrante no tenía una cookie, independientemente de si una respuesta HTTP anterior en la misma conexión TCP ya había obtenido una cookie. Si el equilibrador de carga optimiza la inserción de cookies para que solo ocurra una vez por conexión TCP, la optimización NO NECESITA usarse.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p108">Hardware load balancer cookie MUST be set in every HTTP response for which the incoming HTTP request did not have a cookie, regardless of whether a previous HTTP response on that same TCP connection had already obtained a cookie. If the load balancer optimizes cookie insert to only occur once per TCP connection, that optimization MUST NOT be used</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="93a5b-141">Las configuraciones típicas de equilibrado de carga de hardware usan afinidad de dirección de origen y 20 minutos de duración de la sesión TCP, lo cual es adecuado para clientes de Lync Server y Lync 2013 porque se mantiene el estado de la sesión a través del uso del cliente o la interacción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="93a5b-141">Typical hardware load balancer configurations use source-address affinity and a 20 min. TCP session lifetime, which is fine for Lync Server and Lync 2013 clients because session state is maintained through client usage and/or and application interaction.</span></span>



</div>

<span data-ttu-id="93a5b-142">Si se implementan dispositivos móviles, es preciso que el equilibrador de carga de hardware pueda equilibrar la carga de una solicitud individual dentro de una sesión TCP (de hecho, necesita poder equilibrar la carga de una solicitud individual basada en la dirección IP de destino).</span><span class="sxs-lookup"><span data-stu-id="93a5b-142">If you are deploying mobile devices, your hardware load balancer must be able to load balance individual request within a TCP session (in effect, you must be able to load balance an individual request based on the target IP address).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="93a5b-p109">Los equilibradores de carga de hardware F5 tienen una característica llamada OneConnect que asegura que cada solicitud dentro de una conexión TCP tenga carga equilibrada individualmente. Si va a implementar dispositivos móviles, asegúrese de que su proveedor del equilibrador de carga de hardware admita la misma función. Las últimas aplicaciones móviles que utilizan Apple iOS requieren la versión 1.2 de la seguridad de la capa de transporte (TLS). Para ellos, F5 proporciona una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p109">F5 hardware load balancers have a feature called OneConnect that ensures each request within a TCP connection is individually load balanced. If you are deploying mobile devices, ensure your hardware load balancer vendor supports the same functionality. The latest Apple iOS mobile apps require Transport Layer Security (TLS) version 1.2. F5 provides specific settings for this.</span></span><BR><span data-ttu-id="93a5b-147">Para obtener detalles sobre los equilibradores de carga de hardware de terceros, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=230700">https://go.microsoft.com/fwlink/p/?linkId=230700</A></span><span class="sxs-lookup"><span data-stu-id="93a5b-147">For details on third party hardware load balancers, see <A href="https://go.microsoft.com/fwlink/p/?linkid=230700">https://go.microsoft.com/fwlink/p/?linkId=230700</A></span></span>



</div>

<span data-ttu-id="93a5b-148">A continuación, se muestran los requisitos del equilibrador de carga de hardware para los servicios web del grupo de servidores front-end y de directores:</span><span class="sxs-lookup"><span data-stu-id="93a5b-148">Following are the hardware load balancer requirements for Director and Front End pool Web Services:</span></span>

  - <span data-ttu-id="93a5b-149">Para los VIP de servicios Web internos, establezca \_ la persistencia de la dirección de origen (puerto interno 80, 443) en el equilibrador de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="93a5b-149">For internal Web Services VIPs, set Source\_addr persistence (internal port 80, 443) on the hardware load balancer.</span></span> <span data-ttu-id="93a5b-150">Para Lync Server 2013, la persistencia de la dirección de origen \_ significa que siempre se envían varias conexiones provenientes de una única dirección IP a un servidor para mantener el estado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="93a5b-150">For Lync Server 2013, Source\_addr persistence means that multiple connections coming from a single IP address are always sent to one server to maintain session state.</span></span>

  - <span data-ttu-id="93a5b-151">Use un tiempo de espera de inactividad de TCP de 1800 segundos.</span><span class="sxs-lookup"><span data-stu-id="93a5b-151">Use TCP idle timeout of 1800 seconds.</span></span>

  - <span data-ttu-id="93a5b-p111">En el firewall entre el proxy inverso y el equilibrador de carga de hardware del grupo de servidores del próximo salto, cree una regla que permita el tráfico https: en el puerto 4443, desde el proxy inverso al equilibrador de carga de hardware. El equilibrador de carga de hardware necesita configurarse para que escuche los puertos 80, 443 y 4443.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p111">On the firewall between the reverse proxy and the next hop pool’s hardware load balancer, create a rule to allow https: traffic on port 4443, from the reverse proxy to the hardware load balancer. The hardware load balancer must be configured to listen on ports 80, 443, and 4443.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="93a5b-154">Para obtener más lecturas sobre la configuración del equilibrador de carga de hardware, consulte <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Resumen de puerto: borde consolidado escalado con equilibradores de carga de hardware de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="93a5b-154">For further reading on configuration of the hardware load balancer, please review <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="summary-of-hardware-load-balancer-affinity-requirements"></a><span data-ttu-id="93a5b-155">Resumen de los requisitos de afinidad del equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="93a5b-155">Summary of Hardware Load Balancer Affinity Requirements</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93a5b-156">Ubicación de cliente/usuario</span><span class="sxs-lookup"><span data-stu-id="93a5b-156">Client/user location</span></span></th>
<th><span data-ttu-id="93a5b-157">Requisitos de afinidad del FQDN de servicios web externos</span><span class="sxs-lookup"><span data-stu-id="93a5b-157">External web services FQDN affinity requirements</span></span></th>
<th><span data-ttu-id="93a5b-158">Requisitos de afinidad del FQDN de servicios web internos</span><span class="sxs-lookup"><span data-stu-id="93a5b-158">Internal web services FQDN affinity requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93a5b-159">Lync Web App (usuarios internos y externos)</span><span class="sxs-lookup"><span data-stu-id="93a5b-159">Lync Web App (internal and external users)</span></span></p>
<p><span data-ttu-id="93a5b-160">Dispositivo móvil (usuarios internos y externos)</span><span class="sxs-lookup"><span data-stu-id="93a5b-160">Mobile device (internal and external users)</span></span></p></td>
<td><p><span data-ttu-id="93a5b-161">Sin afinidad</span><span class="sxs-lookup"><span data-stu-id="93a5b-161">No affinity</span></span></p></td>
<td><p><span data-ttu-id="93a5b-162">Afinidad de direcciones de origen</span><span class="sxs-lookup"><span data-stu-id="93a5b-162">Source address affinity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93a5b-163">Lync Web App (solo usuarios externos)</span><span class="sxs-lookup"><span data-stu-id="93a5b-163">Lync Web App (external users only)</span></span></p>
<p><span data-ttu-id="93a5b-164">Dispositivo móvil (usuarios internos y externos)</span><span class="sxs-lookup"><span data-stu-id="93a5b-164">Mobile device (internal and external users)</span></span></p></td>
<td><p><span data-ttu-id="93a5b-165">Sin afinidad</span><span class="sxs-lookup"><span data-stu-id="93a5b-165">No affinity</span></span></p></td>
<td><p><span data-ttu-id="93a5b-166">Afinidad de direcciones de origen</span><span class="sxs-lookup"><span data-stu-id="93a5b-166">Source address affinity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93a5b-167">Lync Web App (solo para usuarios internos)</span><span class="sxs-lookup"><span data-stu-id="93a5b-167">Lync Web App (internal users only)</span></span></p>
<p><span data-ttu-id="93a5b-168">Dispositivo móvil (no implementado)</span><span class="sxs-lookup"><span data-stu-id="93a5b-168">Mobile device (not deployed)</span></span></p></td>
<td><p><span data-ttu-id="93a5b-169">Sin afinidad</span><span class="sxs-lookup"><span data-stu-id="93a5b-169">No affinity</span></span></p></td>
<td><p><span data-ttu-id="93a5b-170">Afinidad de direcciones de origen</span><span class="sxs-lookup"><span data-stu-id="93a5b-170">Source address affinity</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="port-monitoring-for-hardware-load-balancers"></a><span data-ttu-id="93a5b-171">Supervisión de puertos para los equilibradores de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="93a5b-171">Port Monitoring for Hardware Load Balancers</span></span>

<span data-ttu-id="93a5b-172">Es necesario definir la supervisión de puertos en los equilibradores de carga de hardware para determinar cuándo determinados servicios dejan de estar disponibles por errores de comunicaciones o de hardware.</span><span class="sxs-lookup"><span data-stu-id="93a5b-172">You define port monitoring on the hardware load balancers to determine when specific services are no longer available due to hardware or communications failure.</span></span> <span data-ttu-id="93a5b-173">Por ejemplo, si se detiene el servicio servidor front-end (RTCSRV) porque se produce un error en el servidor front-end o en la agrupación front end, la supervisión de HLB también debe dejar de recibir tráfico en los servicios Web.</span><span class="sxs-lookup"><span data-stu-id="93a5b-173">For example, if the Front End Server service (RTCSRV) stops because the Front End Server or Front End pool fails, the HLB monitoring should also stop receiving traffic on the Web Services.</span></span> <span data-ttu-id="93a5b-174">La supervisión de puertos en ECH tiene que implementarse para supervisar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="93a5b-174">You implement port monitoring on the HLB to monitor the following:</span></span>

### <a name="front-end-server-user-pool--hlb-internal-interface"></a><span data-ttu-id="93a5b-175">Grupo de usuarios del servidor front-end – interfaz interna de HLB</span><span class="sxs-lookup"><span data-stu-id="93a5b-175">Front End Server User Pool – HLB Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93a5b-176">Puerto/IP virtual</span><span class="sxs-lookup"><span data-stu-id="93a5b-176">Virtual IP/Port</span></span></th>
<th><span data-ttu-id="93a5b-177">Puerto de nodo</span><span class="sxs-lookup"><span data-stu-id="93a5b-177">Node Port</span></span></th>
<th><span data-ttu-id="93a5b-178">Monitor/máquina de nodo</span><span class="sxs-lookup"><span data-stu-id="93a5b-178">Node Machine/Monitor</span></span></th>
<th><span data-ttu-id="93a5b-179">Perfil de persistencia</span><span class="sxs-lookup"><span data-stu-id="93a5b-179">Persistence Profile</span></span></th>
<th><span data-ttu-id="93a5b-180">Notas</span><span class="sxs-lookup"><span data-stu-id="93a5b-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93a5b-181">&lt;&gt;Web del Grupo: int_mco_443_vs</span><span class="sxs-lookup"><span data-stu-id="93a5b-181">&lt;pool&gt;web-int_mco_443_vs</span></span></p>
<p><span data-ttu-id="93a5b-182">443</span><span class="sxs-lookup"><span data-stu-id="93a5b-182">443</span></span></p></td>
<td><p><span data-ttu-id="93a5b-183">443</span><span class="sxs-lookup"><span data-stu-id="93a5b-183">443</span></span></p></td>
<td><p><span data-ttu-id="93a5b-184">Front-end</span><span class="sxs-lookup"><span data-stu-id="93a5b-184">Front End</span></span></p>
<p><span data-ttu-id="93a5b-185">5061</span><span class="sxs-lookup"><span data-stu-id="93a5b-185">5061</span></span></p></td>
<td><p><span data-ttu-id="93a5b-186">Origen</span><span class="sxs-lookup"><span data-stu-id="93a5b-186">Source</span></span></p></td>
<td><p><span data-ttu-id="93a5b-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="93a5b-187">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93a5b-188">&lt;&gt;Web del Grupo: int_mco_80_vs</span><span class="sxs-lookup"><span data-stu-id="93a5b-188">&lt;pool&gt;web-int_mco_80_vs</span></span></p>
<p><span data-ttu-id="93a5b-189">80</span><span class="sxs-lookup"><span data-stu-id="93a5b-189">80</span></span></p></td>
<td><p><span data-ttu-id="93a5b-190">80</span><span class="sxs-lookup"><span data-stu-id="93a5b-190">80</span></span></p></td>
<td><p><span data-ttu-id="93a5b-191">Front-end</span><span class="sxs-lookup"><span data-stu-id="93a5b-191">Front End</span></span></p>
<p><span data-ttu-id="93a5b-192">5061</span><span class="sxs-lookup"><span data-stu-id="93a5b-192">5061</span></span></p></td>
<td><p><span data-ttu-id="93a5b-193">Origen</span><span class="sxs-lookup"><span data-stu-id="93a5b-193">Source</span></span></p></td>
<td><p><span data-ttu-id="93a5b-194">HTTP</span><span class="sxs-lookup"><span data-stu-id="93a5b-194">HTTP</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="front-end-server-user-pool--hlb-external-interface"></a><span data-ttu-id="93a5b-195">Grupo de usuarios del servidor front-end: HLB externa</span><span class="sxs-lookup"><span data-stu-id="93a5b-195">Front End Server User Pool – HLB External Interface</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93a5b-196">Puerto/IP virtual</span><span class="sxs-lookup"><span data-stu-id="93a5b-196">Virtual IP/Port</span></span></th>
<th><span data-ttu-id="93a5b-197">Puerto de nodo</span><span class="sxs-lookup"><span data-stu-id="93a5b-197">Node Port</span></span></th>
<th><span data-ttu-id="93a5b-198">Monitor/máquina de nodo</span><span class="sxs-lookup"><span data-stu-id="93a5b-198">Node Machine/Monitor</span></span></th>
<th><span data-ttu-id="93a5b-199">Perfil de persistencia</span><span class="sxs-lookup"><span data-stu-id="93a5b-199">Persistence Profile</span></span></th>
<th><span data-ttu-id="93a5b-200">Notas</span><span class="sxs-lookup"><span data-stu-id="93a5b-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93a5b-201">&lt;web_mco_443_vs de grupo &gt;</span><span class="sxs-lookup"><span data-stu-id="93a5b-201">&lt;pool&gt;web_mco_443_vs</span></span></p>
<p><span data-ttu-id="93a5b-202">443</span><span class="sxs-lookup"><span data-stu-id="93a5b-202">443</span></span></p></td>
<td><p><span data-ttu-id="93a5b-203">4443</span><span class="sxs-lookup"><span data-stu-id="93a5b-203">4443</span></span></p></td>
<td><p><span data-ttu-id="93a5b-204">Front-end</span><span class="sxs-lookup"><span data-stu-id="93a5b-204">Front End</span></span></p>
<p><span data-ttu-id="93a5b-205">5061</span><span class="sxs-lookup"><span data-stu-id="93a5b-205">5061</span></span></p></td>
<td><p><span data-ttu-id="93a5b-206">Ninguno</span><span class="sxs-lookup"><span data-stu-id="93a5b-206">None</span></span></p></td>
<td><p><span data-ttu-id="93a5b-207">HTTPS</span><span class="sxs-lookup"><span data-stu-id="93a5b-207">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93a5b-208">&lt;web_mco_80_vs de grupo &gt;</span><span class="sxs-lookup"><span data-stu-id="93a5b-208">&lt;pool&gt;web_mco_80_vs</span></span></p>
<p><span data-ttu-id="93a5b-209">80</span><span class="sxs-lookup"><span data-stu-id="93a5b-209">80</span></span></p></td>
<td><p><span data-ttu-id="93a5b-210">8080</span><span class="sxs-lookup"><span data-stu-id="93a5b-210">8080</span></span></p></td>
<td><p><span data-ttu-id="93a5b-211">Front-end</span><span class="sxs-lookup"><span data-stu-id="93a5b-211">Front End</span></span></p>
<p><span data-ttu-id="93a5b-212">5061</span><span class="sxs-lookup"><span data-stu-id="93a5b-212">5061</span></span></p></td>
<td><p><span data-ttu-id="93a5b-213">Ninguno</span><span class="sxs-lookup"><span data-stu-id="93a5b-213">None</span></span></p></td>
<td><p><span data-ttu-id="93a5b-214">HTTP</span><span class="sxs-lookup"><span data-stu-id="93a5b-214">HTTP</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="93a5b-215">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93a5b-215">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

