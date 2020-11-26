---
title: 'Lync Server 2013: Resumen de DNS - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP públicas'
description: 'Lync Server 2013: el límite consolidado de Resumen de DNS, el equilibrio de carga DNS con direcciones IP públicas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: dc8f096a-a0a4-4f71-8930-88ff8fc089d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205319(v=OCS.15)
ms:contentKeyID: 48185594
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca88043b76365508ea00ca840e9a9fdcb0e270be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429017"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="5c767-103">Resumen de DNS - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c767-103">DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c767-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c767-104">

<span> </span></span></span>

<span data-ttu-id="5c767-105">_**Última modificación del tema:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="5c767-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="5c767-106">Los requisitos de registro DNS para el acceso remoto a Lync Server 2013 son bastante sencillos en comparación con los de certificados y puertos.</span><span class="sxs-lookup"><span data-stu-id="5c767-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="5c767-107">Además, muchos registros son opcionales, en función de cómo configure los clientes que ejecutan Lync 2013 y si habilita la Federación.</span><span class="sxs-lookup"><span data-stu-id="5c767-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="5c767-108">Para obtener más información sobre los requisitos de DNS de Lync 2013, consulte [determinar los requisitos de DNS para Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5c767-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="5c767-109">Para obtener más información sobre cómo configurar la configuración automática de los clientes de Lync 2013, si no se ha configurado el servidor DNS de horizonte dividido, consulte la sección "configuración automática sin DNS de división de datos" en [determinar los requisitos de DNS para Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5c767-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="5c767-110">La tabla siguiente contiene un resumen de los registros DNS necesarios para admitir la única topología de arista consolidada que se muestra en la ilustración de una única topología de borde consolidado.</span><span class="sxs-lookup"><span data-stu-id="5c767-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="5c767-111">Tenga en cuenta que algunos registros DNS solo son necesarios para la configuración automática de clientes de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="5c767-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="5c767-112">Si planea usar objetos de directiva de grupo (GPO) para configurar clientes de Lync, los registros asociados no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="5c767-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="5c767-113">IMPORTANTE: requisitos del adaptador de red del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="5c767-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="5c767-114">Para evitar problemas de enrutamiento, compruebe que hay al menos dos adaptadores de red en los servidores perimetrales y que la puerta de enlace predeterminada solo está configurada en el adaptador de red asociado a la interfaz externa.</span><span class="sxs-lookup"><span data-stu-id="5c767-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="5c767-115">Por ejemplo, tal y como se muestra en el escenario de borde consolidado escalado en el [nivel perimetral consolidado, el equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) , la puerta de enlace predeterminada apunta al firewall externo.</span><span class="sxs-lookup"><span data-stu-id="5c767-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) , the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="5c767-116">Puede configurar dos adaptadores de red en cada uno de los servidores perimetrales de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5c767-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="5c767-117">**Adaptador de red 1-nodo 1 (interfaz interna)**</span><span class="sxs-lookup"><span data-stu-id="5c767-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="5c767-118">Interfaz interna con 172.25.33.10 asignado.</span><span class="sxs-lookup"><span data-stu-id="5c767-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="5c767-119">No hay ninguna puerta de enlace predeterminada definida.</span><span class="sxs-lookup"><span data-stu-id="5c767-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="5c767-120">Asegúrese de que haya una ruta desde la red que contenga la interfaz interna perimetral a cualquier red que contenga servidores que ejecuten Lync Server 2013 o clientes de Lync Server 2013 (por ejemplo, de 172.25.33.0 a 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="5c767-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="5c767-121">**Adaptador de red 1-nodo 2 (interfaz interna)**</span><span class="sxs-lookup"><span data-stu-id="5c767-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="5c767-122">Interfaz interna con 172.25.33.11 asignado.</span><span class="sxs-lookup"><span data-stu-id="5c767-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="5c767-123">No hay ninguna puerta de enlace predeterminada definida.</span><span class="sxs-lookup"><span data-stu-id="5c767-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="5c767-124">Asegúrese de que haya una ruta desde la red que contenga la interfaz interna perimetral a cualquier red que contenga servidores que ejecuten Lync Server 2013 o clientes de Lync Server 2013 (por ejemplo, de 172.25.33.0 a 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="5c767-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="5c767-125">**Adaptador de red 2 nodo 1 (interfaz externa)**</span><span class="sxs-lookup"><span data-stu-id="5c767-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="5c767-126">Se asignan tres direcciones IP privadas a este adaptador de red, por ejemplo, 131.107.155.10 para el servicio perimetral de acceso, 131.107.155.20 para el servicio perimetral de conferencias web, 131.107.155.30 para el servicio perimetral A/V.</span><span class="sxs-lookup"><span data-stu-id="5c767-126">Three private IP addresses are assigned to this network adapter, for example 131.107.155.10 for Access Edge service, 131.107.155.20 for Web Conferencing Edge service, 131.107.155.30 for A/V Edge service.</span></span>
    
    <span data-ttu-id="5c767-127">La dirección IP pública del servicio perimetral de acceso es principal con la puerta de enlace predeterminada establecida para el enrutador público (131.107.155.1).</span><span class="sxs-lookup"><span data-stu-id="5c767-127">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="5c767-128">Servicio perimetral de conferencias web y direcciones IP privadas de servicio perimetral A/V son direcciones IP adicionales en la sección **avanzadas** de las propiedades del **Protocolo de Internet versión 4 (TCP/IPv4)** y el **Protocolo de Internet versión 6 (TCP/IPv6)** de las **propiedades de conexión de área local** de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5c767-128">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5c767-129">Es posible, aunque no recomendable, usar una única dirección IP para las tres interfaces de servicio perimetral.</span><span class="sxs-lookup"><span data-stu-id="5c767-129">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="5c767-130">Aunque esto sí guarda las direcciones IP, requiere números de Puerto diferentes para cada servicio.</span><span class="sxs-lookup"><span data-stu-id="5c767-130">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="5c767-131">El número de puerto predeterminado es 443/TCP, lo que garantiza que la mayoría de los firewalls remotos permitan el tráfico.</span><span class="sxs-lookup"><span data-stu-id="5c767-131">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="5c767-132">Cambiar los valores del puerto a (por ejemplo) 5061/TCP para el servicio perimetral de acceso, 444/TCP para el servicio perimetral de las conferencias web y 443/TCP para el servicio perimetral a/V puede causar problemas a los usuarios remotos en los que un firewall en el que se encuentra no permite el tráfico a través de 5061/TCP y 444/TCP.</span><span class="sxs-lookup"><span data-stu-id="5c767-132">Changing the port values to (for example) 5061/TCP for the Access Edge service, 444/TCP for the Web Conferencing Edge service and 443/TCP for the A/V Edge service might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="5c767-133">Además, tres direcciones IP distintas hacen que la solución de problemas sea más fácil, ya que es posible filtrar por dirección IP.</span><span class="sxs-lookup"><span data-stu-id="5c767-133">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>

  - <span data-ttu-id="5c767-134">**Adaptador de red 2 nodo 2 (interfaz externa)**</span><span class="sxs-lookup"><span data-stu-id="5c767-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="5c767-135">Se asignan tres direcciones IP privadas a este adaptador de red, por ejemplo, 131.107.155.11 para el servicio perimetral de acceso, 131.107.155.21 para el servicio perimetral de conferencias web, 131.107.155.31 para el servicio perimetral A/V.</span><span class="sxs-lookup"><span data-stu-id="5c767-135">Three private IP addresses are assigned to this network adapter, for example 131.107.155.11 for Access Edge service, 131.107.155.21 for Web Conferencing Edge service, 131.107.155.31 for A/V Edge service.</span></span>
    
    <span data-ttu-id="5c767-136">La dirección IP pública del servicio perimetral de acceso es principal con la puerta de enlace predeterminada establecida para el enrutador público (131.107.155.1).</span><span class="sxs-lookup"><span data-stu-id="5c767-136">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="5c767-137">Servicio perimetral de conferencias web y direcciones IP privadas de servicio perimetral A/V son direcciones IP adicionales en la sección **avanzadas** de las propiedades del **Protocolo de Internet versión 4 (TCP/IPv4)** y el **Protocolo de Internet versión 6 (TCP/IPv6)** de las **propiedades de conexión de área local** de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5c767-137">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="5c767-138">La configuración del servidor perimetral con dos adaptadores de red es una de dos opciones.</span><span class="sxs-lookup"><span data-stu-id="5c767-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="5c767-139">La otra opción es usar un adaptador de red para el lado interno y tres adaptadores de red para el lado externo del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="5c767-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="5c767-140">La principal ventaja de esta opción es un adaptador de red distinto por cada servicio de servidor perimetral, así como una recopilación de datos potencialmente más concisa cuando se necesita la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="5c767-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-example"></a><span data-ttu-id="5c767-141">Registros DNS necesarios para el límite consolidado de la escala, el equilibrio de carga DNS con direcciones IP públicas (ejemplo)</span><span class="sxs-lookup"><span data-stu-id="5c767-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c767-142">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="5c767-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="5c767-143">FQDN/registro DNS</span><span class="sxs-lookup"><span data-stu-id="5c767-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="5c767-144">Dirección IP/FQDN</span><span class="sxs-lookup"><span data-stu-id="5c767-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="5c767-145">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="5c767-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c767-146">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="5c767-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5c767-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-148">131.107.155.10 y 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="5c767-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="5c767-149">Interfaz externa de servicio perimetral de acceso (contoso) Repita según sea necesario para todos los dominios SIP con usuarios habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="5c767-149">Access Edge service external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c767-150">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="5c767-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5c767-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-152">131.107.155.20 y 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="5c767-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="5c767-153">Interfaz externa de servicio perimetral de conferencia Web</span><span class="sxs-lookup"><span data-stu-id="5c767-153">Web Conferencing Edge service external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c767-154">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="5c767-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5c767-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-156">131.107.155.30 y 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="5c767-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="5c767-157">Interfaz externa de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="5c767-157">A/V Edge service external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c767-158">DNS/SRV/443 externo</span><span class="sxs-lookup"><span data-stu-id="5c767-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="5c767-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-161">Interfaz externa de servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="5c767-161">Access Edge service external interface.</span></span> <span data-ttu-id="5c767-162">Necesario para que la configuración automática de los clientes de Lync 2013 y Lync 2010 funcione de forma externa.</span><span class="sxs-lookup"><span data-stu-id="5c767-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="5c767-163">Repita el procedimiento según sea necesario para todos los dominios SIP con usuarios habilitados para Lync.</span><span class="sxs-lookup"><span data-stu-id="5c767-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c767-164">DNS externo/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="5c767-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="5c767-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-167">Servicio perimetral de acceso interfaz externa necesaria para la detección automática de DNS de los socios federados conocidos como "dominio SIP permitido" (denominado Federación mejorada en versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="5c767-167">Access Edge service external interface Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="5c767-168">Repetir según sea necesario para todos los dominios SIP con usuarios habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="5c767-168">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c767-169">DNS/A interno</span><span class="sxs-lookup"><span data-stu-id="5c767-169">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5c767-170">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="5c767-170">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="5c767-171">172.25.33.10 y 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="5c767-171">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="5c767-172">Interfaz interna de Edge consolidado</span><span class="sxs-lookup"><span data-stu-id="5c767-172">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="5c767-173">Registros necesarios para la Federación</span><span class="sxs-lookup"><span data-stu-id="5c767-173">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c767-174">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="5c767-174">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="5c767-175">FQDN</span><span class="sxs-lookup"><span data-stu-id="5c767-175">FQDN</span></span></th>
<th><span data-ttu-id="5c767-176">Dirección IP/registro de host FQDN</span><span class="sxs-lookup"><span data-stu-id="5c767-176">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="5c767-177">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="5c767-177">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c767-178">DNS externo/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="5c767-178">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="5c767-179">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-179">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-180">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-180">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-181">Servicio perimetral de acceso SIP interfaz externa necesaria para la detección automática de DNS de su Federación a otros potenciales socios de Federación, y se conoce como "dominios SIP permitidos" (denominada Federación mejorada en versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="5c767-181">SIP Access Edge service external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="5c767-182">Repita el procedimiento según sea necesario para todos los dominios SIP con usuarios habilitados para Lync y los clientes móviles de Microsoft Lync que usan el servicio de notificaciones Push o el servicio de notificaciones push de Apple</span><span class="sxs-lookup"><span data-stu-id="5c767-182">Repeat as necessary for all SIP domains with Lync enabled users and Microsoft Lync Mobile clients that use either the Push Notification Service or the Apple Push Notification service</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="5c767-183">Resumen de DNS para el protocolo de presencia y mensajería extensible</span><span class="sxs-lookup"><span data-stu-id="5c767-183">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c767-184">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="5c767-184">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="5c767-185">FQDN</span><span class="sxs-lookup"><span data-stu-id="5c767-185">FQDN</span></span></th>
<th><span data-ttu-id="5c767-186">Dirección IP/registro de host FQDN</span><span class="sxs-lookup"><span data-stu-id="5c767-186">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="5c767-187">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="5c767-187">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c767-188">DNS/SRV/5269 externo</span><span class="sxs-lookup"><span data-stu-id="5c767-188">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="5c767-189">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-189">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-190">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5c767-190">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5c767-191">Interfaz externa de proxy XMPP en el servicio perimetral de acceso o grupo perimetral. Repita el procedimiento según sea necesario para todos los dominios SIP internos con los usuarios habilitados para Lync donde se permite el contacto con los contactos XMPP mediante la configuración de la Directiva de acceso externo a través de una directiva global, una directiva de sitio donde se encuentra el usuario o la Directiva de usuario para el usuario habilitado para Lync.</span><span class="sxs-lookup"><span data-stu-id="5c767-191">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="5c767-192">También se debe configurar un dominio XMPP permitido en la Directiva del socio XMPP federado.</span><span class="sxs-lookup"><span data-stu-id="5c767-192">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="5c767-193">Vea temas en <strong>vea también</strong> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5c767-193">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c767-194">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="5c767-194">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5c767-195">xmpp.contoso.com (por ejemplo)</span><span class="sxs-lookup"><span data-stu-id="5c767-195">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="5c767-196">Dirección IP del servicio perimetral de acceso en el servidor perimetral o grupo perimetral que aloja el proxy XMPP</span><span class="sxs-lookup"><span data-stu-id="5c767-196">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="5c767-197">Señala el servicio perimetral de Access o el grupo de límites que alberga el servicio de proxy XMPP.</span><span class="sxs-lookup"><span data-stu-id="5c767-197">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="5c767-198">Normalmente, el registro SRV que cree apuntará a este registro de host (A o AAAA).</span><span class="sxs-lookup"><span data-stu-id="5c767-198">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5c767-199">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c767-199">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

