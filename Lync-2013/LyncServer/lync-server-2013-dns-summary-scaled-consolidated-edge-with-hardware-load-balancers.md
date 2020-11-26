---
title: Resumen DNS - Servidor perimetral consolidado ampliado con equilibradores de carga de hardware
description: 'Resumen DNS: borde consolidado a escala con equilibradores de carga de hardware.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge with hardware load balancers
ms:assetid: 8453297c-da1d-4b9e-a37e-6721458c6feb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398670(v=OCS.15)
ms:contentKeyID: 48184700
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59581f435267a7db607e03a8cbf52d21f70897f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437703"
---
# <a name="dns-summary---scaled-consolidated-edge-with-hardware-load-balancers-in-lync-server-2013"></a><span data-ttu-id="312dd-103">Resumen DNS - Servidor perimetral consolidado ampliado con equilibradores de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="312dd-103">DNS summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="312dd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="312dd-104">

<span> </span></span></span>

<span data-ttu-id="312dd-105">_**Última modificación del tema:** 2013-01-27_</span><span class="sxs-lookup"><span data-stu-id="312dd-105">_**Topic Last Modified:** 2013-01-27_</span></span>

<span data-ttu-id="312dd-106">Los requisitos de registro DNS para el acceso remoto a Lync Server 2013 son bastante sencillos en comparación con los de certificados y puertos.</span><span class="sxs-lookup"><span data-stu-id="312dd-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="312dd-107">Además, muchos registros son opcionales, en función de cómo configure los clientes que ejecutan Lync 2013 y si habilita la Federación.</span><span class="sxs-lookup"><span data-stu-id="312dd-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="312dd-108">Para obtener más información sobre los requisitos de DNS de Lync 2013, consulte [determinar los requisitos de DNS para Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="312dd-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="312dd-109">Para obtener más información sobre cómo configurar la configuración automática de los clientes de Lync 2013, si no se ha configurado el servidor DNS de horizonte dividido, consulte la sección "configuración automática sin DNS de división de datos" en [determinar los requisitos de DNS para Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="312dd-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="312dd-110">La tabla siguiente contiene un resumen de los registros DNS necesarios para admitir la figura de topología de perímetro consolidado escalado (equilibrio de carga de hardware).</span><span class="sxs-lookup"><span data-stu-id="312dd-110">The following table contains a summary of the DNS records that are required to support the Scaled Consolidated Edge Topology (Hardware Load Balanced) figure.</span></span> <span data-ttu-id="312dd-111">Tenga en cuenta que algunos registros DNS solo son necesarios para la configuración automática para clientes de Lync.</span><span class="sxs-lookup"><span data-stu-id="312dd-111">Note that certain DNS records are required only for automatic configuration for Lync clients.</span></span> <span data-ttu-id="312dd-112">Si planea usar objetos de directiva de grupo (GPO) para configurar clientes de Lync, los registros asociados no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="312dd-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="312dd-113">IMPORTANTE: requisitos del adaptador de red del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="312dd-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="312dd-114">Para evitar problemas de enrutamiento, compruebe que hay al menos dos adaptadores de red en los servidores perimetrales y que la puerta de enlace predeterminada solo está configurada en el adaptador de red asociado a la interfaz externa.</span><span class="sxs-lookup"><span data-stu-id="312dd-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="312dd-115">Por ejemplo, tal y como se muestra en el escenario de borde consolidado escalado en el [borde consolidado escalado con equilibradores de carga de hardware en Lync Server 2013](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md), la puerta de enlace predeterminada apunta al firewall externo.</span><span class="sxs-lookup"><span data-stu-id="312dd-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge with hardware load balancers in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md), the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="312dd-116">Puede configurar dos adaptadores de red en cada uno de los servidores perimetrales de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="312dd-116">You can configure two network adapters in each of your Edge Servers as follows:</span></span>

  - <span data-ttu-id="312dd-117">**Adaptador de red 1 (interfaz interna)**</span><span class="sxs-lookup"><span data-stu-id="312dd-117">**Network adapter 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="312dd-118">Interfaz interna con 172.25.33.10 asignado.</span><span class="sxs-lookup"><span data-stu-id="312dd-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="312dd-119">No hay puerta de enlace predeterminada.</span><span class="sxs-lookup"><span data-stu-id="312dd-119">No default gateway.</span></span>
    
    <span data-ttu-id="312dd-120">Asegúrese de que haya una ruta desde la red que contenga la interfaz interna del servidor perimetral a cualquier red que contenga clientes de Lync Server o servidores que ejecuten Lync Server (por ejemplo, de 172.25.33.0 a 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="312dd-120">Ensure there is a route from the network containing the Edge Server internal interface to any networks that contain Lync Server clients or servers running Lync Server (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="312dd-121">**Adaptador de red 2 (interfaz externa)**</span><span class="sxs-lookup"><span data-stu-id="312dd-121">**Network adapter 2 (External Interface)**</span></span>
    
    <span data-ttu-id="312dd-122">Se asignan tres direcciones IP públicas a este adaptador de red, por ejemplo, 131.107.155.10 para el servicio perimetral de acceso, 131.107.155.20 para el servicio perimetral de conferencias web, 131.107.155.30 para el servicio perimetral A/V.</span><span class="sxs-lookup"><span data-stu-id="312dd-122">Three public IP addresses are assigned to this network adapter, for example 131.107.155.10 for Access Edge service, 131.107.155.20 for Web Conferencing Edge service, 131.107.155.30 for A/V Edge service.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="312dd-123">Las direcciones IP que se asignan a las interfaces de red externas reales del servidor perimetral pueden depender del equilibrador de carga de hardware que elija.</span><span class="sxs-lookup"><span data-stu-id="312dd-123">The IP addresses that are assigned to the actual external network interfaces of the Edge Server may depend on which hardware load balancer you choose.</span></span> <span data-ttu-id="312dd-124">Consulte la documentación de su equilibrador de carga de hardware para conocer los requisitos de las direcciones IP reales.</span><span class="sxs-lookup"><span data-stu-id="312dd-124">Refer to the documentation for your hardware load balancer to understand the actual IP address requirements.</span></span><BR><span data-ttu-id="312dd-125">Es posible, aunque no recomendable, usar una única dirección IP para las tres interfaces de servicio perimetral.</span><span class="sxs-lookup"><span data-stu-id="312dd-125">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="312dd-126">Aunque esto sí guarda las direcciones IP, requiere números de Puerto diferentes para cada servicio.</span><span class="sxs-lookup"><span data-stu-id="312dd-126">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="312dd-127">El número de puerto predeterminado es 443/TCP, lo que garantiza que la mayoría de los firewalls remotos permitan el tráfico.</span><span class="sxs-lookup"><span data-stu-id="312dd-127">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="312dd-128">Cambiar los valores del puerto a (por ejemplo) 5061/TCP para el servicio perimetral de acceso, 444/TCP para el servicio perimetral de las conferencias web y 443/TCP para el servicio perimetral a/V puede causar problemas a los usuarios remotos en los que un firewall en el que se encuentra no permite el tráfico a través de 5061/TCP y 444/TCP.</span><span class="sxs-lookup"><span data-stu-id="312dd-128">Changing the port values to (for example) 5061/TCP for the Access Edge service, 444/TCP for the Web Conferencing Edge service and 443/TCP for the A/V Edge service might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="312dd-129">Además, tres direcciones IP distintas hacen que la solución de problemas sea más fácil, ya que es posible filtrar por dirección IP.</span><span class="sxs-lookup"><span data-stu-id="312dd-129">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>
    
    <span data-ttu-id="312dd-130">La dirección IP del servicio perimetral de acceso es principal con la puerta de enlace predeterminada establecida para enrutador orientado a Internet (131.107.155.1).</span><span class="sxs-lookup"><span data-stu-id="312dd-130">Access Edge service IP address is primary with default gateway set to Internet-facing router (131.107.155.1).</span></span>
    
    <span data-ttu-id="312dd-131">Servicio perimetral de conferencias web y direcciones IP del servicio de borde A/V secundarios.</span><span class="sxs-lookup"><span data-stu-id="312dd-131">Web Conferencing Edge service and A/V Edge service IP addresses secondary.</span></span>

<div>


> [!TIP]
> <span data-ttu-id="312dd-132">La configuración del servidor perimetral con dos adaptadores de red es una de dos opciones.</span><span class="sxs-lookup"><span data-stu-id="312dd-132">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="312dd-133">La otra opción es usar un adaptador de red para el lado interno y tres adaptadores de red para el lado externo del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="312dd-133">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="312dd-134">La principal ventaja de esta opción es un adaptador de red distinto por cada servicio de servidor perimetral, así como una recopilación de datos potencialmente más concisa cuando se necesita la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="312dd-134">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-hardware-load-balanced-example"></a><span data-ttu-id="312dd-135">Registros DNS necesarios para el límite consolidado con escala, equilibrio de carga de hardware (ejemplo)</span><span class="sxs-lookup"><span data-stu-id="312dd-135">DNS Records Required for Scaled Consolidated Edge, Hardware Load Balanced (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="312dd-136">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="312dd-136">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="312dd-137">FQDN/registro DNS</span><span class="sxs-lookup"><span data-stu-id="312dd-137">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="312dd-138">Dirección IP/FQDN</span><span class="sxs-lookup"><span data-stu-id="312dd-138">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="312dd-139">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="312dd-139">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="312dd-140">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="312dd-140">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="312dd-141">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="312dd-141">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="312dd-142">131.107.155.10</span><span class="sxs-lookup"><span data-stu-id="312dd-142">131.107.155.10</span></span></p></td>
<td><p><span data-ttu-id="312dd-143">Interfaz externa de servicio perimetral de acceso (contoso).</span><span class="sxs-lookup"><span data-stu-id="312dd-143">Access Edge service external interface (Contoso).</span></span> <span data-ttu-id="312dd-144">Repetir según sea necesario para todos los dominios SIP con usuarios habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="312dd-144">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="312dd-145">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="312dd-145">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="312dd-146">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="312dd-146">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="312dd-147">131.107.155.20</span><span class="sxs-lookup"><span data-stu-id="312dd-147">131.107.155.20</span></span></p></td>
<td><p><span data-ttu-id="312dd-148">Interfaz externa de servicio perimetral de conferencia Web</span><span class="sxs-lookup"><span data-stu-id="312dd-148">Web Conferencing Edge service external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="312dd-149">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="312dd-149">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="312dd-150">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="312dd-150">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="312dd-151">131.107.155.30</span><span class="sxs-lookup"><span data-stu-id="312dd-151">131.107.155.30</span></span></p></td>
<td><p><span data-ttu-id="312dd-152">Interfaz externa de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="312dd-152">A/V Edge service external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="312dd-153">DNS/SRV/443 externo</span><span class="sxs-lookup"><span data-stu-id="312dd-153">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="312dd-154">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="312dd-154">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="312dd-155">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="312dd-155">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="312dd-156">Interfaz externa de servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="312dd-156">Access Edge service external interface.</span></span> <span data-ttu-id="312dd-157">Necesario para que la configuración automática de los clientes de Lync 2013 y Lync 2010 funcione de forma externa.</span><span class="sxs-lookup"><span data-stu-id="312dd-157">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="312dd-158">Repita el procedimiento según sea necesario para todos los dominios SIP con usuarios habilitados para Lync.</span><span class="sxs-lookup"><span data-stu-id="312dd-158">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="312dd-159">DNS externo/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="312dd-159">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="312dd-160">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="312dd-160">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="312dd-161">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="312dd-161">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="312dd-162">Servicio perimetral de acceso SIP interfaz externa necesaria para la detección automática de DNS de los socios federados conocidos como "dominio SIP permitido" (denominado Federación mejorada en versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="312dd-162">SIP Access Edge service external interface Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="312dd-163">Repita el procedimiento según sea necesario para todos los dominios SIP con usuarios habilitados para Lync y los clientes móviles de Microsoft Lync que usan el servicio de notificaciones Push o el servicio de notificaciones push de Apple</span><span class="sxs-lookup"><span data-stu-id="312dd-163">Repeat as necessary for all SIP domains with Lync enabled users and Microsoft Lync Mobile clients that use either the Push Notification Service or the Apple Push Notification service</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="312dd-164">DNS/A interno</span><span class="sxs-lookup"><span data-stu-id="312dd-164">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="312dd-165">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="312dd-165">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="312dd-166">172.25.33.10</span><span class="sxs-lookup"><span data-stu-id="312dd-166">172.25.33.10</span></span></p></td>
<td><p><span data-ttu-id="312dd-167">Interfaz interna de Edge consolidado</span><span class="sxs-lookup"><span data-stu-id="312dd-167">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="312dd-168">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="312dd-168">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

