---
title: 'Lync Server 2013: requisitos DNS para grupos de servidores front-end'
description: 'Lync Server 2013: requisitos DNS para grupos de servidores front-end.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429073"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a><span data-ttu-id="d0899-103">Requisitos DNS para grupos front-end en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0899-103">DNS requirements for Front End pools in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0899-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0899-104">

<span> </span></span></span>

<span data-ttu-id="d0899-105">_**Tema Última modificación:** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="d0899-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="d0899-106">En esta sección se describen los registros del Sistema de nombres de dominio (DNS) necesarios para implementar grupos de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="d0899-106">This section describes the Domain Name System (DNS) records that are required for deployment of Front End pools.</span></span>

<div>

## <a name="dns-records-for-front-end-pools"></a><span data-ttu-id="d0899-107">Registros de DNS para grupos de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="d0899-107">DNS Records for Front End Pools</span></span>

<span data-ttu-id="d0899-108">En la tabla siguiente se especifican los requisitos DNS para una implementación de grupo front-end de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0899-108">The following table specifies DNS requirements for a Lync Server 2013 Front End pool deployment.</span></span>

### <a name="dns-requirements-for-a-front-end-pool"></a><span data-ttu-id="d0899-109">Requisitos de DNS para un grupo de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="d0899-109">DNS Requirements for a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0899-110">Escenario de implementación</span><span class="sxs-lookup"><span data-stu-id="d0899-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="d0899-111">Requisito de DNS</span><span class="sxs-lookup"><span data-stu-id="d0899-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0899-112">Grupo de servidores front-end con varios servidores front-end y un equilibrador de carga de hardware (independientemente de si el equilibrio de carga de DNS también está implementado en este grupo)</span><span class="sxs-lookup"><span data-stu-id="d0899-112">Front End pool with multiple Front End Servers and a hardware load balancer (whether or not DNS load balancing is also deployed on that pool)</span></span></p></td>
<td><p><span data-ttu-id="d0899-113">Al usar el equilibrio de carga DNS y un equilibrador de carga de hardware, debe hospedar (A) registros.</span><span class="sxs-lookup"><span data-stu-id="d0899-113">When using both DNS load balancing and a hardware load balancer, you need to Host (A) records.</span></span> <span data-ttu-id="d0899-114">Cree un registro A interno que resuelva el nombre de dominio completo (FQDN) del grupo front-end para el equilibrio de carga DNS.</span><span class="sxs-lookup"><span data-stu-id="d0899-114">Create an internal A record that resolves the fully qualified domain name (FQDN) of the Front End pool for DNS load balancing.</span></span> <span data-ttu-id="d0899-115">Cree un registro de host interno (A) para los servicios web internos en la dirección IP virtual (VIP) del equilibrador de carga.</span><span class="sxs-lookup"><span data-stu-id="d0899-115">Create an internal host (A) record for the internal Web services to the virtual IP (VIP) address of the load balancer.</span></span> <span data-ttu-id="d0899-116">Debe usar el nombre de los servicios web internos tal como se define en generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="d0899-116">You must use the internal Web services name as defined in Topology Builder.</span></span></p>
<p><span data-ttu-id="d0899-117">Por ejemplo, si usa el equilibrio de carga DNS y el equilibrio de carga de hardware, tendría un registro A para cada servidor front-end en un grupo de servidores para el equilibrio de carga DNS y un registro A para los servicios web internos que apunten a la IP virtual del equilibrador de carga de hardware:</span><span class="sxs-lookup"><span data-stu-id="d0899-117">For example, if you use both DNS load balancing and hardware load balancing, you would have an A record for each Front End Server in a pool for DNS load balancing, and an A record for the internal Web services pointing to the virtual IP of the hardware load balancer:</span></span></p>
<ul>
<li><p><span data-ttu-id="d0899-118">Equilibrio de carga de DNS: Pool01.contoso.net Dirección IP del grupo 10.10.10.5</span><span class="sxs-lookup"><span data-stu-id="d0899-118">DNS load balancing:   Pool01.contoso.net   IP Address of pool   10.10.10.5</span></span></p>
<div>

> [!WARNING]  
> <span data-ttu-id="d0899-119">Cada servidor front-end también tendrá un registro A distinto:</span><span class="sxs-lookup"><span data-stu-id="d0899-119">Each Front End Server will also have a distinct A record:</span></span>


</div>
<ol>
<li><p><span data-ttu-id="d0899-120">FE01.contoso.net 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="d0899-120">FE01.contoso.net    10.10.10.1</span></span></p></li>
<li><p><span data-ttu-id="d0899-121">FE02.contoso.net 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="d0899-121">FE02.contoso.net    10.10.10.2</span></span></p></li>
<li><p><span data-ttu-id="d0899-122">FE03.contoso.net 10.10.10.3</span><span class="sxs-lookup"><span data-stu-id="d0899-122">FE03.contoso.net    10.10.10.3</span></span></p></li>
<li><p><span data-ttu-id="d0899-123">FE04.contoso.net 10.10.10.4</span><span class="sxs-lookup"><span data-stu-id="d0899-123">FE04.contoso.net    10.10.10.4</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="d0899-124">Equilibrio de carga de hardware: WebInternal.contoso.net Dirección IP de HLB VIP 192.168.10.5</span><span class="sxs-lookup"><span data-stu-id="d0899-124">Hardware load balancing:   WebInternal.contoso.net   IP Address of HLB VIP   192.168.10.5</span></span></p></li>
</ul>
<p><span data-ttu-id="d0899-p102">Todo el tráfico, excepto el tráfico HTTP/HTTPS, usará el registro Pool01.contoso.net. El tráfico HTTP/HTTPS utilizará la dirección definida de los servicios web internos, 192.168.10.5.</span><span class="sxs-lookup"><span data-stu-id="d0899-p102">All traffic except for HTTP/HTTPS traffic will use the Pool01.contoso.net record. HTTP/HTTPS traffic will use the defined internal Web services address of 192.168.10.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0899-127">Grupo de servidores front-end con equilibrio de carga de DNS implementado</span><span class="sxs-lookup"><span data-stu-id="d0899-127">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="d0899-128">Un conjunto de registros A internos que resuelven el FQDN del grupo para la dirección IP de cada uno de los servidores del grupo.</span><span class="sxs-lookup"><span data-stu-id="d0899-128">A set of internal A records that resolve the FQDN of the pool to the IP address of each server in the pool.</span></span> <span data-ttu-id="d0899-129">Tiene que haber un registro A para cada servidor del grupo.</span><span class="sxs-lookup"><span data-stu-id="d0899-129">There must one A record for each server in the pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0899-130">Grupo de servidores front-end con equilibrio de carga de DNS implementado</span><span class="sxs-lookup"><span data-stu-id="d0899-130">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="d0899-131">Un conjunto de registros A internos que resuelven el FQDN de cada servidor del grupo en la dirección IP de ese servidor.</span><span class="sxs-lookup"><span data-stu-id="d0899-131">A set of internal A records that resolve the FQDN of each server in the pool to the IP address of that server.</span></span> <span data-ttu-id="d0899-132">Para obtener más información, <a href="lync-server-2013-dns-load-balancing.md">vea Equilibrio de carga DNS en Lync Server 2013</a> en la documentación de planeamiento.</span><span class="sxs-lookup"><span data-stu-id="d0899-132">For details, see <a href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0899-133">Un grupo de servidores front-end con un solo servidor front-end y una base de datos back-end dedicada sin equilibrador de carga</span><span class="sxs-lookup"><span data-stu-id="d0899-133">Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</span></span></p></td>
<td><p><span data-ttu-id="d0899-134">Un registro A interno que resuelve el FQDN del grupo de servidores front-end para la dirección IP del único servidor front-end Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="d0899-134">An internal A record that resolves the FQDN of the Front End pool to the IP address of the single Enterprise Edition Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0899-135">Inicio de sesión de clientes automático</span><span class="sxs-lookup"><span data-stu-id="d0899-135">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="d0899-136">Para cada dominio SIP compatible, un registro SRV para _sipinternaltls._tcp. &lt; dominio &gt; a través del puerto 5061 que se asigna al FQDN del grupo front-end que autentica y redirige las solicitudes de cliente para el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d0899-136">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="d0899-137">Para obtener más información, vea Requisitos DNS para el inicio de sesión automático del cliente <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">en Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="d0899-137">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0899-138">Detección del servicio web de actualización de dispositivos por los dispositivos de comunicaciones unificadas (UC)</span><span class="sxs-lookup"><span data-stu-id="d0899-138">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="d0899-139">Un registro A interno con el nombre ucupdates-r2. &lt; Dominio SIP que se resuelve en la dirección IP del grupo &gt; front-end que hospeda el servicio web de actualización de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d0899-139">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Front End pool that hosts the Device Update Web service.</span></span> <span data-ttu-id="d0899-140">En caso de que se active un dispositivo de UC en el que nunca ningún usuario inició sesión, el registro A permite al dispositivo detectar el grupo de servidores front-end que hospeda el servicio web de actualización de dispositivos y obtener actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="d0899-140">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the Front End pool hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="d0899-141">De lo contrario, los dispositivos obtienen esta información a través del aprovisionamiento en banda la primera vez que un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="d0899-141">Otherwise, devices obtain this information though in-band provisioning the first time a user logs in.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="d0899-142">Si tiene una implementación existente del servicio web de actualización de dispositivos en Lync Server 2010, ya ha creado un registro A interno con el nombre ucupdates. &lt; Dominio SIP &gt; .</span><span class="sxs-lookup"><span data-stu-id="d0899-142">If you have an existing deployment of Device Update Web service in Lync Server 2010, you have already created an internal A record with the name ucupdates.&lt;SIP domain&gt;.</span></span> <span data-ttu-id="d0899-143">Para Microsoft Office Communications Server 2007 R2, debe crear un registro DNS A adicional con el nombre ucupdates-r2. &lt; Dominio SIP &gt; .</span><span class="sxs-lookup"><span data-stu-id="d0899-143">For Microsoft Office Communications Server 2007 R2, you must create an additional DNS A record with the name ucupdates-r2.&lt;SIP domain&gt;.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0899-144">Un proxy inverso compatible con el tráfico HTTP</span><span class="sxs-lookup"><span data-stu-id="d0899-144">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="d0899-145">Un registro A externo que resuelve el FQDN externo de la granja de servidores web en la dirección IP externa del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="d0899-145">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="d0899-146">Los clientes y los dispositivos de UC usan este registro para conectarse al proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="d0899-146">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="d0899-147">Para obtener más información, vea <a href="lync-server-2013-determine-dns-requirements.md">Determinar los requisitos DNS para Lync Server 2013</a> en la documentación de planeamiento.</span><span class="sxs-lookup"><span data-stu-id="d0899-147">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d0899-148">La tabla siguiente muestra un ejemplo de los registros de DNS necesarios para el FQDN interno de la granja de servidores web.</span><span class="sxs-lookup"><span data-stu-id="d0899-148">The following table shows an example of the DNS records required for the internal web farm FQDN.</span></span>

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a><span data-ttu-id="d0899-149">Ejemplo de los registros de DNS para el FQDN interno de la granja de servidores web</span><span class="sxs-lookup"><span data-stu-id="d0899-149">Example DNS Records for Internal Web Farm FQDN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0899-150">FQDN interno de la granja de servidores web</span><span class="sxs-lookup"><span data-stu-id="d0899-150">Internal web farm FQDN</span></span></th>
<th><span data-ttu-id="d0899-151">FQDN del grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="d0899-151">Pool FQDN</span></span></th>
<th><span data-ttu-id="d0899-152">Registro(s) A de DNS</span><span class="sxs-lookup"><span data-stu-id="d0899-152">DNS A record(s)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0899-153">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d0899-153">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d0899-154">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d0899-154">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d0899-155">Registro A de DNS para ee-pool.contoso.com que se resuelve en la dirección VIP del equilibrador de carga que usan los servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="d0899-155">DNS A record for the ee-pool.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p>
<p><span data-ttu-id="d0899-156">Registro A de DNS para webcon.contoso.com que se resuelve en la dirección VIP del equilibrador de carga que usan los servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="d0899-156">DNS A record for webcon.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0899-157">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d0899-157">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d0899-158">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d0899-158">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d0899-159">Registro A de DNS para ee-pool.contoso.com que se resuelve en la dirección IP virtual (VIP) del equilibrador de carga que usan los servidores front-end Enterprise Edition en el grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="d0899-159">DNS A record for ee-pool.contoso.com that resolves to the virtual IP (VIP) address of the load balancer used by the Enterprise Edition Front End Servers in the Front End pool.</span></span></p>
<p><span data-ttu-id="d0899-160">Tenga en cuenta que si usa el equilibrio de carga de DNS en este grupo, su grupo de servidores front-end y la granja de servidores web internos no podrán tener el mismo FQDN.</span><span class="sxs-lookup"><span data-stu-id="d0899-160">Note that if you are using DNS load balancing on this pool, your Front End pool and internal web farm cannot have the same FQDN.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d0899-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0899-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

