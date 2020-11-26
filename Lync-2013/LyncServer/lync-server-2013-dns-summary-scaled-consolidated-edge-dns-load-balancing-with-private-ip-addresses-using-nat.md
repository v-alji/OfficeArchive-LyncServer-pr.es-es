---
title: 'Lync Server 2013: Resumen de DNS - Topologías perimetrales consolidadas escaladas, equilibrio de carga DNS con direcciones IP privadas con NAT'
description: 'Lync Server 2013: el límite consolidado de Resumen de DNS, el equilibrio de carga de DNS con direcciones IP privadas mediante NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: 11bc7b84-91cf-48f9-ad0e-06ad30b46a2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398201(v=OCS.15)
ms:contentKeyID: 48183447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2eef3029323c1c2f798fddc721df832a932524c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437710"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="05a8d-103">Resumen de DNS - Topologías perimetrales consolidadas escaladas, equilibrio de carga DNS con direcciones IP privadas con NAT en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="05a8d-103">DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="05a8d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="05a8d-104">

<span> </span></span></span>

<span data-ttu-id="05a8d-105">_**Última modificación del tema:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="05a8d-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="05a8d-106">Los requisitos de registro DNS para el acceso remoto a Lync Server 2013 son bastante sencillos en comparación con los de certificados y puertos.</span><span class="sxs-lookup"><span data-stu-id="05a8d-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="05a8d-107">Además, muchos registros son opcionales, en función de cómo configure los clientes que ejecutan Lync 2013 y si habilita la Federación.</span><span class="sxs-lookup"><span data-stu-id="05a8d-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="05a8d-108">Para obtener más información sobre los requisitos de DNS de Lync 2013, consulte [determinar los requisitos de DNS para Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="05a8d-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="05a8d-109">Para obtener más información sobre cómo configurar la configuración automática de los clientes de Lync 2013, si no se ha configurado el servidor DNS de horizonte dividido, consulte la sección "configuración automática sin DNS de división de datos" en [determinar los requisitos de DNS para Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="05a8d-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="05a8d-110">La tabla siguiente contiene un resumen de los registros DNS necesarios para admitir la única topología de arista consolidada que se muestra en la ilustración de una única topología de borde consolidado.</span><span class="sxs-lookup"><span data-stu-id="05a8d-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="05a8d-111">Tenga en cuenta que algunos registros DNS solo son necesarios para la configuración automática de clientes de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="05a8d-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="05a8d-112">Si planea usar objetos de directiva de grupo (GPO) para configurar clientes de Lync, los registros asociados no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="05a8d-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="05a8d-113">IMPORTANTE: requisitos del adaptador de red del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="05a8d-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="05a8d-114">Para evitar problemas de enrutamiento, compruebe que hay al menos dos adaptadores de red en los servidores perimetrales y que la puerta de enlace predeterminada solo está configurada en el adaptador de red asociado a la interfaz externa.</span><span class="sxs-lookup"><span data-stu-id="05a8d-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="05a8d-115">Por ejemplo, tal y como se muestra en el escenario de borde consolidado escalado en el modo de [perímetro consolidado, el equilibrio de carga de DNS con direcciones IP privadas usando NAT en Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md), la puerta de enlace predeterminada apunta al firewall externo.</span><span class="sxs-lookup"><span data-stu-id="05a8d-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md), the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="05a8d-116">Puede configurar dos adaptadores de red en cada uno de los servidores perimetrales de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="05a8d-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="05a8d-117">**Adaptador de red 1-nodo 1 (interfaz interna)**</span><span class="sxs-lookup"><span data-stu-id="05a8d-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="05a8d-118">Interfaz interna con 172.25.33.10 asignado.</span><span class="sxs-lookup"><span data-stu-id="05a8d-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="05a8d-119">No hay ninguna puerta de enlace predeterminada definida.</span><span class="sxs-lookup"><span data-stu-id="05a8d-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="05a8d-120">Asegúrese de que haya una ruta desde la red que contenga la interfaz interna perimetral a cualquier red que contenga servidores que ejecuten Lync Server 2013 o clientes de Lync Server 2013 (por ejemplo, de 172.25.33.0 a 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="05a8d-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="05a8d-121">**Adaptador de red 1-nodo 2 (interfaz interna)**</span><span class="sxs-lookup"><span data-stu-id="05a8d-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="05a8d-122">Interfaz interna con 172.25.33.11 asignado.</span><span class="sxs-lookup"><span data-stu-id="05a8d-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="05a8d-123">No hay ninguna puerta de enlace predeterminada definida.</span><span class="sxs-lookup"><span data-stu-id="05a8d-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="05a8d-124">Asegúrese de que haya una ruta desde la red que contenga la interfaz interna perimetral a cualquier red que contenga servidores que ejecuten Lync Server 2013 o clientes de Lync Server 2013 (por ejemplo, de 172.25.33.0 a 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="05a8d-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="05a8d-125">**Adaptador de red 2 nodo 1 (interfaz externa)**</span><span class="sxs-lookup"><span data-stu-id="05a8d-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="05a8d-126">Se asignan tres direcciones IP privadas a este adaptador de red, por ejemplo, 10.45.16.10 para Edge de Access, 10.45.16.20 para Edge de conferencias web, 10.45.16.30 para Edge AV.</span><span class="sxs-lookup"><span data-stu-id="05a8d-126">Three private IP addresses are assigned to this network adapter, for example 10.45.16.10 for Access Edge, 10.45.16.20 for Web Conferencing Edge, 10.45.16.30 for AV Edge.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="05a8d-127">Es posible, aunque no recomendable, usar una única dirección IP para las tres interfaces de servicio perimetral.</span><span class="sxs-lookup"><span data-stu-id="05a8d-127">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="05a8d-128">Aunque esto sí guarda las direcciones IP, requiere números de Puerto diferentes para cada servicio.</span><span class="sxs-lookup"><span data-stu-id="05a8d-128">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="05a8d-129">El número de puerto predeterminado es 443/TCP, lo que garantiza que la mayoría de los firewalls remotos permitan el tráfico.</span><span class="sxs-lookup"><span data-stu-id="05a8d-129">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="05a8d-130">Cambiar los valores del puerto a (por ejemplo) 5061/TCP para el extremo de Access, 444/TCP para el perímetro de la conferencia web y 443/TCP para la periferia AV puede causar problemas a los usuarios remotos en los que un firewall que estén detrás no permite el tráfico por encima de 5061/TCP y 444/TCP.</span><span class="sxs-lookup"><span data-stu-id="05a8d-130">Changing the port values to (for example) 5061/TCP for the Access Edge, 444/TCP for the Web Conferencing Edge and 443/TCP for the AV Edge might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="05a8d-131">Además, tres direcciones IP distintas hacen que la solución de problemas sea más fácil, ya que es posible filtrar por dirección IP.</span><span class="sxs-lookup"><span data-stu-id="05a8d-131">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>
    
    <span data-ttu-id="05a8d-132">La dirección IP pública perimetral de Access es principal con la puerta de enlace predeterminada establecida para el enrutador integrado (10.45.16.1).</span><span class="sxs-lookup"><span data-stu-id="05a8d-132">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="05a8d-133">Las direcciones IP privadas de los bordes de las conferencias web y A/V son direcciones IP adicionales en la sección **avanzadas** de las propiedades del **Protocolo de Internet versión 4 (TCP/IPv4)** y el **Protocolo de Internet versión 6 (TCP/IPv6)** de las **propiedades de conexión de área local** de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="05a8d-133">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

  - <span data-ttu-id="05a8d-134">**Adaptador de red 2 nodo 2 (interfaz externa)**</span><span class="sxs-lookup"><span data-stu-id="05a8d-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="05a8d-135">Se asignan tres direcciones IP privadas a este adaptador de red, por ejemplo, 10.45.16.11 para Edge de Access, 10.45.16.21 para Edge de conferencias web, 10.45.16.31 para Edge AV.</span><span class="sxs-lookup"><span data-stu-id="05a8d-135">Three private IP addresses are assigned to this network adapter, for example 10.45.16.11 for Access Edge, 10.45.16.21 for Web Conferencing Edge, 10.45.16.31 for AV Edge.</span></span>
    
    <span data-ttu-id="05a8d-136">La dirección IP pública perimetral de Access es principal con la puerta de enlace predeterminada establecida para el enrutador integrado (10.45.16.1).</span><span class="sxs-lookup"><span data-stu-id="05a8d-136">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="05a8d-137">Las direcciones IP privadas de los bordes de las conferencias web y A/V son direcciones IP adicionales en la sección **avanzadas** de las propiedades del **Protocolo de Internet versión 4 (TCP/IPv4)** y el **Protocolo de Internet versión 6 (TCP/IPv6)** de las **propiedades de conexión de área local** de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="05a8d-137">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="05a8d-138">La configuración del servidor perimetral con dos adaptadores de red es una de dos opciones.</span><span class="sxs-lookup"><span data-stu-id="05a8d-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="05a8d-139">La otra opción es usar un adaptador de red para el lado interno y tres adaptadores de red para el lado externo del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="05a8d-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="05a8d-140">La principal ventaja de esta opción es un adaptador de red distinto por cada servicio de servidor perimetral, así como una recopilación de datos potencialmente más concisa cuando se necesita la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="05a8d-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-example"></a><span data-ttu-id="05a8d-141">Registros DNS necesarios para el límite consolidado de la escala, el equilibrio de carga de DNS con direcciones IP privadas mediante NAT (ejemplo)</span><span class="sxs-lookup"><span data-stu-id="05a8d-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05a8d-142">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="05a8d-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="05a8d-143">FQDN/registro DNS</span><span class="sxs-lookup"><span data-stu-id="05a8d-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="05a8d-144">Dirección IP/FQDN</span><span class="sxs-lookup"><span data-stu-id="05a8d-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="05a8d-145">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="05a8d-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05a8d-146">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="05a8d-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="05a8d-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-148">131.107.155.10 y 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="05a8d-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="05a8d-149">Interfaz externa de perimetral de acceso (contoso) repite según sea necesario para todos los dominios SIP con usuarios habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="05a8d-149">Access Edge external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05a8d-150">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="05a8d-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="05a8d-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-152">131.107.155.20 y 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="05a8d-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="05a8d-153">Interfaz externa perimetral de conferencia Web</span><span class="sxs-lookup"><span data-stu-id="05a8d-153">Web Conferencing Edge external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05a8d-154">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="05a8d-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="05a8d-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-156">131.107.155.30 y 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="05a8d-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="05a8d-157">Interfaz externa de borde A/V</span><span class="sxs-lookup"><span data-stu-id="05a8d-157">A/V Edge external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05a8d-158">DNS/SRV/443 externo</span><span class="sxs-lookup"><span data-stu-id="05a8d-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="05a8d-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-161">Interfaz externa perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="05a8d-161">Access Edge external interface.</span></span> <span data-ttu-id="05a8d-162">Necesario para que la configuración automática de los clientes de Lync 2013 y Lync 2010 funcione de forma externa.</span><span class="sxs-lookup"><span data-stu-id="05a8d-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="05a8d-163">Repita el procedimiento según sea necesario para todos los dominios SIP con usuarios habilitados para Lync.</span><span class="sxs-lookup"><span data-stu-id="05a8d-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05a8d-164">DNS externo/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="05a8d-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="05a8d-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-167">Interfaz externa perimetral de acceso de SIP.</span><span class="sxs-lookup"><span data-stu-id="05a8d-167">SIP Access Edge external interface.</span></span> <span data-ttu-id="05a8d-168">Necesario para la detección automática de DNS de los socios federados, conocido como "dominio SIP permitido" (denominado Federación mejorada en versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="05a8d-168">Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="05a8d-169">Repetir según sea necesario para todos los dominios SIP con usuarios habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="05a8d-169">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05a8d-170">DNS/A interno</span><span class="sxs-lookup"><span data-stu-id="05a8d-170">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="05a8d-171">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="05a8d-171">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="05a8d-172">172.25.33.10 y 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="05a8d-172">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="05a8d-173">Interfaz interna de Edge consolidado</span><span class="sxs-lookup"><span data-stu-id="05a8d-173">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="05a8d-174">Registros necesarios para la Federación</span><span class="sxs-lookup"><span data-stu-id="05a8d-174">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05a8d-175">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="05a8d-175">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="05a8d-176">FQDN</span><span class="sxs-lookup"><span data-stu-id="05a8d-176">FQDN</span></span></th>
<th><span data-ttu-id="05a8d-177">Dirección IP/registro de host FQDN</span><span class="sxs-lookup"><span data-stu-id="05a8d-177">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="05a8d-178">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="05a8d-178">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05a8d-179">DNS externo/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="05a8d-179">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="05a8d-180">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-180">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-181">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-181">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-182">Interfaz externa perimetral de acceso SIP necesaria para la detección automática de DNS de su Federación a otros posibles socios de Federación, y se conoce como "dominios SIP permitidos" (denominada Federación mejorada en versiones anteriores). Repetir según sea necesario para todos los dominios SIP con usuarios habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="05a8d-182">SIP Access Edge external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="05a8d-183">Este registro SRV es necesario para la movilidad y el centro de enrutamiento de notificaciones push</span><span class="sxs-lookup"><span data-stu-id="05a8d-183">This SRV record is required for mobility and the push notification clearing house</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="05a8d-184">Resumen de DNS: conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="05a8d-184">DNS Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05a8d-185">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="05a8d-185">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="05a8d-186">FQDN/registro DNS</span><span class="sxs-lookup"><span data-stu-id="05a8d-186">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="05a8d-187">Dirección IP/FQDN</span><span class="sxs-lookup"><span data-stu-id="05a8d-187">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="05a8d-188">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="05a8d-188">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05a8d-189">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="05a8d-189">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="05a8d-190">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-190">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-191">Interfaz de servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="05a8d-191">Access Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="05a8d-192">Interfaz externa de perimetral de acceso (contoso) repite según sea necesario para todos los dominios SIP con usuarios habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="05a8d-192">Access Edge external interface (Contoso)Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="05a8d-193">Resumen de DNS para el protocolo de presencia y mensajería extensible</span><span class="sxs-lookup"><span data-stu-id="05a8d-193">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05a8d-194">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="05a8d-194">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="05a8d-195">FQDN</span><span class="sxs-lookup"><span data-stu-id="05a8d-195">FQDN</span></span></th>
<th><span data-ttu-id="05a8d-196">Dirección IP/registro de host FQDN</span><span class="sxs-lookup"><span data-stu-id="05a8d-196">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="05a8d-197">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="05a8d-197">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05a8d-198">DNS/SRV/5269 externo</span><span class="sxs-lookup"><span data-stu-id="05a8d-198">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="05a8d-199">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-199">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-200">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="05a8d-200">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="05a8d-201">Interfaz externa de proxy XMPP en el servicio perimetral de acceso o grupo perimetral. Repita el procedimiento según sea necesario para todos los dominios SIP internos con los usuarios habilitados para Lync donde se permite el contacto con los contactos XMPP mediante la configuración de la Directiva de acceso externo a través de una directiva global, una directiva de sitio donde se encuentra el usuario o la Directiva de usuario para el usuario habilitado para Lync.</span><span class="sxs-lookup"><span data-stu-id="05a8d-201">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="05a8d-202">También se debe configurar un dominio XMPP permitido en la Directiva del socio XMPP federado.</span><span class="sxs-lookup"><span data-stu-id="05a8d-202">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="05a8d-203">Vea temas en <strong>vea también</strong> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="05a8d-203">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05a8d-204">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="05a8d-204">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="05a8d-205">xmpp.contoso.com (por ejemplo)</span><span class="sxs-lookup"><span data-stu-id="05a8d-205">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="05a8d-206">Dirección IP del servicio perimetral de acceso en el servidor perimetral o grupo perimetral que aloja el proxy XMPP</span><span class="sxs-lookup"><span data-stu-id="05a8d-206">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="05a8d-207">Señala el servicio perimetral de Access o el grupo de límites que alberga el servicio de proxy XMPP.</span><span class="sxs-lookup"><span data-stu-id="05a8d-207">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="05a8d-208">Normalmente, el registro SRV que cree apuntará a este registro de host (A o AAAA).</span><span class="sxs-lookup"><span data-stu-id="05a8d-208">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="05a8d-209">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="05a8d-209">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

