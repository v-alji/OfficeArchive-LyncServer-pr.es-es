---
title: 'Lync Server 2013: Elección de una topología'
description: 'Lync Server 2013: elección de una topología.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Choosing a topology
ms:assetid: 23f2aeb6-fed9-4349-8fba-dcbf18ee4b04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425716(v=OCS.15)
ms:contentKeyID: 48183634
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01ded739c3c5e4e0bd8c0f25f3f0fe8ff1f350b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434912"
---
# <a name="choosing-a-topology-in-lync-server-2013"></a><span data-ttu-id="5245e-103">Elección de una topología en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5245e-103">Choosing a topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span data-ttu-id="5245e-104">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="5245e-104">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="5245e-105">Al elegir una topología, puede usar una de las siguientes opciones de topología compatibles:</span><span class="sxs-lookup"><span data-stu-id="5245e-105">When you choose a topology, you can use one the following supported topology options:</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="5245e-106">A menos que se indique lo contrario, si tiene experiencia con Microsoft Lync Server 2010, verá que la guía se encuentra en gran medida.</span><span class="sxs-lookup"><span data-stu-id="5245e-106">Unless otherwise noted, if you have experience with Microsoft Lync Server 2010, you will find the guidance here is largely unchanged.</span></span>



</div>

  - [<span data-ttu-id="5245e-107">Servidor perimetral consolidado simple con direcciones IP privadas y NAT en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5245e-107">Single consolidated edge with private IP addresses and NAT in Lync Server 2013</span></span>](lync-server-2013-single-consolidated-edge-with-private-ip-addresses-and-nat.md)

  - [<span data-ttu-id="5245e-108">Topología perimetral consolidada de un solo equipo con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5245e-108">Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="5245e-109">Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP privadas mediante NAT en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5245e-109">Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="5245e-110">Perímetro consolidado escalado, equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5245e-110">Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="5245e-111">Servidor perimetral consolidado ampliado con equilibradores de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5245e-111">Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md)

<div>


> [!IMPORTANT]
> <span data-ttu-id="5245e-p101">La interfaz perimetral interna y la interfaz perimetral externa necesitan usar el mismo tipo de equilibrio de carga. No puede usar equilibrio de carga de DNS en una interfaz perimetral y equilibrio de carga de hardware en la otra interfaz perimetral.</span><span class="sxs-lookup"><span data-stu-id="5245e-p101">The internal Edge interface and external Edge interface must use the same type of load balancing. You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span>



</div>

<span data-ttu-id="5245e-114">En la siguiente tabla se resumen las funciones disponibles en las topologías de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5245e-114">The following table summarizes the functionality available with the supported Microsoft Lync Server 2013 topologies.</span></span> <span data-ttu-id="5245e-115">Los encabezados de columna indican la funcionalidad disponible para una opción de configuración de borde determinada.</span><span class="sxs-lookup"><span data-stu-id="5245e-115">The column headings indicate the functionality available for a given Edge configuration option.</span></span> <span data-ttu-id="5245e-116">Con la opción de borde escalado (carga equilibrada de DNS) como ejemplo, puede ver que admite alta disponibilidad, puede usar direcciones IP privadas no enrutables (con NAT) o direcciones IP públicas enrutables asignadas a las interfaces externas de borde y reduce el costo porque no se requiere un equilibrador de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="5245e-116">Using the Scaled Edge (DNS load balanced) option as an example, you can see that it supports high availability, can use non-routable private IP addresses (with NAT) or routable public IP addresses assigned to the Edge external interfaces, and reduces cost because a hardware load balancer is not required.</span></span>

<span data-ttu-id="5245e-117">Escenarios de conmutación por error perimetral compatibles con el equilibrio de carga de DNS son sesiones de punto a punto entre Lync, sesiones de conferencia de Lync, sesiones entre usuarios de Skype empresarial, Office 365 y Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5245e-117">Edge failover scenarios supported with DNS Load Balancing are Lync-to-Lync point-to-point sessions, Lync conferencing sessions, Lync-to-PSTN sessions, Office 365, and Microsoft 365.</span></span> <span data-ttu-id="5245e-118">Los escenarios de failover perimetral que no se beneficien del equilibrio de carga de DNS son el failover de la mensajería unificada de Exchange de los usuarios remotos (anteriores a Exchange 2010 SP1), la conectividad de mensajería instantánea pública (mi) y la Federación con servidores que ejecutan Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="5245e-118">Edge failover scenarios that do not benefit from DNS Load Balancing are failover for remote user Exchange Unified Messaging (UM) (prior to Exchange 2010 SP1), public instant messaging (IM) connectivity, and federation with servers running Office Communications Server.</span></span>

### <a name="summary-of-edge-server-topology-options"></a><span data-ttu-id="5245e-119">Resumen de las opciones de topología de servidores perimetrales</span><span class="sxs-lookup"><span data-stu-id="5245e-119">Summary of Edge Server Topology Options</span></span>

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
<th><span data-ttu-id="5245e-120">Topología</span><span class="sxs-lookup"><span data-stu-id="5245e-120">Topology</span></span></th>
<th><span data-ttu-id="5245e-121">Alta disponibilidad</span><span class="sxs-lookup"><span data-stu-id="5245e-121">High availability</span></span></th>
<th><span data-ttu-id="5245e-122">Se requieren registros DNS adicionales adicionales para el servidor perimetral externo en el grupo Edge</span><span class="sxs-lookup"><span data-stu-id="5245e-122">Additional DNS A records required for external Edge Server in the Edge pool</span></span></th>
<th><span data-ttu-id="5245e-123">Conmutación por error de borde para sesiones de Lync a Lync</span><span class="sxs-lookup"><span data-stu-id="5245e-123">Edge Failover for Lync-to-Lync sessions</span></span></th>
<th><span data-ttu-id="5245e-124">Conmutación por error de Edge para sesiones de Federación de Lync EUM/PIC/OCS</span><span class="sxs-lookup"><span data-stu-id="5245e-124">Edge Failover for Lync-to-Lync EUM/PIC/OCS Federation sessions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5245e-125">Un solo lado con NAT</span><span class="sxs-lookup"><span data-stu-id="5245e-125">Single Edge using NAT</span></span></p></td>
<td><p><span data-ttu-id="5245e-126">No</span><span class="sxs-lookup"><span data-stu-id="5245e-126">No</span></span></p></td>
<td><p><span data-ttu-id="5245e-127">No</span><span class="sxs-lookup"><span data-stu-id="5245e-127">No</span></span></p></td>
<td><p><span data-ttu-id="5245e-128">No</span><span class="sxs-lookup"><span data-stu-id="5245e-128">No</span></span></p></td>
<td><p><span data-ttu-id="5245e-129">No</span><span class="sxs-lookup"><span data-stu-id="5245e-129">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5245e-130">Un solo lado con IP pública</span><span class="sxs-lookup"><span data-stu-id="5245e-130">Single Edge using Public IP</span></span></p></td>
<td><p><span data-ttu-id="5245e-131">No</span><span class="sxs-lookup"><span data-stu-id="5245e-131">No</span></span></p></td>
<td><p><span data-ttu-id="5245e-132">No</span><span class="sxs-lookup"><span data-stu-id="5245e-132">No</span></span></p></td>
<td><p><span data-ttu-id="5245e-133">No</span><span class="sxs-lookup"><span data-stu-id="5245e-133">No</span></span></p></td>
<td><p><span data-ttu-id="5245e-134">No</span><span class="sxs-lookup"><span data-stu-id="5245e-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5245e-135">Borde escalado (equilibrio de carga de DNS) con NAT</span><span class="sxs-lookup"><span data-stu-id="5245e-135">Scaled Edge (DNS Load Balanced) using NAT</span></span></p></td>
<td><p><span data-ttu-id="5245e-136">Sí</span><span class="sxs-lookup"><span data-stu-id="5245e-136">Yes</span></span></p></td>
<td><p><span data-ttu-id="5245e-137">Sí</span><span class="sxs-lookup"><span data-stu-id="5245e-137">Yes</span></span></p></td>
<td><p><span data-ttu-id="5245e-138">Sí</span><span class="sxs-lookup"><span data-stu-id="5245e-138">Yes</span></span></p></td>
<td><p>*</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5245e-139">Borde escalado (DNS carga equilibrada) mediante IP pública</span><span class="sxs-lookup"><span data-stu-id="5245e-139">Scaled Edge (DNS Load Balanced) using Public IP</span></span></p></td>
<td><p><span data-ttu-id="5245e-140">Sí</span><span class="sxs-lookup"><span data-stu-id="5245e-140">Yes</span></span></p></td>
<td><p><span data-ttu-id="5245e-141">Sí</span><span class="sxs-lookup"><span data-stu-id="5245e-141">Yes</span></span></p></td>
<td><p><span data-ttu-id="5245e-142">Sí</span><span class="sxs-lookup"><span data-stu-id="5245e-142">Yes</span></span></p></td>
<td><p>*</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5245e-143">Carga de hardware perimetral con escala equilibrada)</span><span class="sxs-lookup"><span data-stu-id="5245e-143">Scaled Edge Hardware load balanced)</span></span></p></td>
<td><p><span data-ttu-id="5245e-144">Sí</span><span class="sxs-lookup"><span data-stu-id="5245e-144">Yes</span></span></p></td>
<td><p><span data-ttu-id="5245e-145">No (un registro A DNS por VIP)</span><span class="sxs-lookup"><span data-stu-id="5245e-145">No (one DNS A record per VIP)</span></span></p></td>
<td><p><span data-ttu-id="5245e-146">Sí</span><span class="sxs-lookup"><span data-stu-id="5245e-146">Yes</span></span></p></td>
<td><p><span data-ttu-id="5245e-147">Sí</span><span class="sxs-lookup"><span data-stu-id="5245e-147">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5245e-148">\**\**• La conmutación por error de la conectividad de mensajería instantánea pública (mi) y la Federación con servidores que ejecutan Office Communications Server no está disponible con el equilibrio de carga de DNS.</span><span class="sxs-lookup"><span data-stu-id="5245e-148">\**\** _ Failover for public instant messaging (IM) connectivity, and federation with servers running Office Communications Server is not available with DNS load balancing.</span></span> <span data-ttu-id="5245e-149">Mensajería unificada de Exchange (usuario remoto) la conmutación por error con el equilibrio de carga de DNS requiere Exchange Server 2010 SP1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5245e-149">Exchange UM (remote user) failover using DNS load balancing requires Exchange Server 2010 SP1 or newer.</span></span>



> [!NOTE]
> <span data-ttu-id="5245e-150">Las topologías de borde y borde simple (equilibrio de carga de DNS) pueden usar:</span><span class="sxs-lookup"><span data-stu-id="5245e-150">Single Edge and Scaled Edge (DNS load balanced) topologies can use:</span></span>
> <ul><li><p><span data-ttu-id="5245e-151">Direcciones IP públicas enrutables</span><span class="sxs-lookup"><span data-stu-id="5245e-151">Routable public IP addresses</span></span></p></li>
> <li><p><span data-ttu-id="5245e-152">Dirección IP privada no enrutable si se usa la traducción de direcciones de red (NAT) simétrica</span><span class="sxs-lookup"><span data-stu-id="5245e-152">Non-routable private IP address if symmetric network address translation (NAT) is used</span></span></p></li>
>
> <ul><li> <span data-ttu-id="5245e-153">Si usa una dirección IP pública o una dirección IP privada con NAT, seguirá usando el mismo número de direcciones IP basadas en la elección de configuración en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="5245e-153">If you use public IP address or private IP address with NAT, you will still use the same number of IP addresses based on your configuration choice in Topology Builder.</span></span> <span data-ttu-id="5245e-154">Puede configurar el servidor perimetral para usar una única dirección IP con puertos distintos por servicio o usar direcciones IP distintas por cada servicio, pero use el mismo puerto (de forma predeterminada, TCP 443).</span><span class="sxs-lookup"><span data-stu-id="5245e-154">You can configure the Edge Server to use a single IP address with distinct ports per service, or use distinct IP addresses per service, but use the same port (by default, TCP 443).</span></span></li></ul>>
> <span data-ttu-id="5245e-155">Si decide usar direcciones IP privadas no enrutables con NAT:</span><span class="sxs-lookup"><span data-stu-id="5245e-155">If you decide to use non-routable private IP addresses with NAT:</span></span>
> <ul><li><p><span data-ttu-id="5245e-156">Debe usar direcciones IP privadas enrutables en las tres interfaces externas</span><span class="sxs-lookup"><span data-stu-id="5245e-156">You must use routable private IP addresses on all three external interfaces</span></span></p></li>
> <li><p><span data-ttu-id="5245e-157">Debe configurar NAT simétrico para el tráfico entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="5245e-157">You must configure symmetric NAT for incoming and outgoing traffic</span></span></p></li></ul>>
> <span data-ttu-id="5245e-158">La topología de borde con escala (equilibrio de carga de hardware) debe usar direcciones IP públicas.</span><span class="sxs-lookup"><span data-stu-id="5245e-158">Scaled Edge (hardware load balanced) topology must use public IP addresses.</span></span>



<span data-ttu-id="5245e-159">Lync Server 2013 admite la colocación de interfaces externas de acceso, conferencia web y borde A/V detrás de un enrutador o firewall que realice la traducción de direcciones de red (NAT) para topologías de servidores perimetrales únicos y escalables.</span><span class="sxs-lookup"><span data-stu-id="5245e-159">Lync Server 2013 supports placing Access, Web Conferencing, and A/V Edge external interfaces behind a router or firewall that performs network address translation (NAT) for both single and scaled consolidated Edge Server topologies.</span></span>

<span data-ttu-id="5245e-160">El uso de NAT para todas las interfaces externas de borde requiere el uso del equilibrio de carga de DNS.</span><span class="sxs-lookup"><span data-stu-id="5245e-160">Using NAT for all Edge external interfaces requires the use of DNS load balancing.</span></span> <span data-ttu-id="5245e-161">En comparación con el uso de equilibradores de carga de hardware, el uso del equilibrio de carga de DNS sin NAT le permite reducir el número de direcciones IP públicas por servidor perimetral en un grupo de límites, tal y como se describe en la siguiente lista:</span><span class="sxs-lookup"><span data-stu-id="5245e-161">When compared to using hardware load balancers, using DNS load balancing without NAT allows you to reduce the number of public IP address per Edge Server in an Edge pool as described in the following list:</span></span>

  - <span data-ttu-id="5245e-162">Lync Server 2013 el límite consolidado escalado (DNS Load balanceed) requiere tres direcciones IP públicas para cada servidor perimetral de un grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="5245e-162">Lync Server 2013 Scaled Consolidated Edge (DNS load balanced) Requires three public IP addresses for each Edge Server in an Edge pool.</span></span>

  - <span data-ttu-id="5245e-163">Lync Server 2013 el borde consolidado escalado (equilibrio de carga de hardware) requiere tres direcciones IP públicas para las direcciones IP virtuales virtuales (un requisito de tiempo que no aumenta a medida que se agregan más servidores perimetrales al grupo) además de tres direcciones IP públicas por servidor perimetral en un grupo.</span><span class="sxs-lookup"><span data-stu-id="5245e-163">Lync Server 2013 Scaled Consolidated Edge (hardware load balanced) Requires three public IP address for load balancer virtual IP addresses (one time requirement that does not increment as more Edge Servers are added to the pool) plus three public IP addresses per Edge Server in a pool.</span></span>

### <a name="ip-address-requirements-for-scaled-consolidated-edge-ip-address-per-role"></a><span data-ttu-id="5245e-164">Requisitos de dirección IP para el límite consolidado escalado (dirección IP por función)</span><span class="sxs-lookup"><span data-stu-id="5245e-164">IP Address Requirements for Scaled Consolidated Edge (IP Address per role)</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5245e-165">Número de servidores perimetrales por grupo</span><span class="sxs-lookup"><span data-stu-id="5245e-165">Number of Edge Servers per pool</span></span></th>
<th><span data-ttu-id="5245e-166">Número de direcciones IP requeridas Lync Server 2013 (equilibrio de carga DNS)</span><span class="sxs-lookup"><span data-stu-id="5245e-166">Number of required IP addresses Lync Server 2013 (DNS load balanced)</span></span></th>
<th><span data-ttu-id="5245e-167">Número de direcciones IP requeridas Lync Server 2013 (equilibrio de carga de hardware)</span><span class="sxs-lookup"><span data-stu-id="5245e-167">Number of required IP addresses Lync Server 2013 (hardware load balanced)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5245e-168">2</span><span class="sxs-lookup"><span data-stu-id="5245e-168">2</span></span></p></td>
<td><p><span data-ttu-id="5245e-169">6</span><span class="sxs-lookup"><span data-stu-id="5245e-169">6</span></span></p></td>
<td><p><span data-ttu-id="5245e-170">3 (1 por VIP) + 6</span><span class="sxs-lookup"><span data-stu-id="5245e-170">3 (1 per VIP) + 6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5245e-171">3</span><span class="sxs-lookup"><span data-stu-id="5245e-171">3</span></span></p></td>
<td><p><span data-ttu-id="5245e-172">99,999</span><span class="sxs-lookup"><span data-stu-id="5245e-172">9</span></span></p></td>
<td><p><span data-ttu-id="5245e-173">3 (1 por VIP) + 9</span><span class="sxs-lookup"><span data-stu-id="5245e-173">3 (1 per VIP) + 9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5245e-174">4</span><span class="sxs-lookup"><span data-stu-id="5245e-174">4</span></span></p></td>
<td><p><span data-ttu-id="5245e-175">2007</span><span class="sxs-lookup"><span data-stu-id="5245e-175">12</span></span></p></td>
<td><p><span data-ttu-id="5245e-176">3 (1 por VIP) + 12</span><span class="sxs-lookup"><span data-stu-id="5245e-176">3 (1 per VIP) + 12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5245e-177">5</span><span class="sxs-lookup"><span data-stu-id="5245e-177">5</span></span></p></td>
<td><p><span data-ttu-id="5245e-178">4,5</span><span class="sxs-lookup"><span data-stu-id="5245e-178">15</span></span></p></td>
<td><p><span data-ttu-id="5245e-179">3 (1 por VIP) + 15</span><span class="sxs-lookup"><span data-stu-id="5245e-179">3 (1 per VIP) + 15</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="ip-address-requirements-for-scaled-consolidated-edge-single-ip-address-for-all-roles"></a><span data-ttu-id="5245e-180">Requisitos de dirección IP para arista consolidada escalada (dirección IP única para todas las funciones)</span><span class="sxs-lookup"><span data-stu-id="5245e-180">IP Address Requirements for Scaled Consolidated Edge (Single IP address for all roles)</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5245e-181">Número de servidores perimetrales por grupo</span><span class="sxs-lookup"><span data-stu-id="5245e-181">Number of Edge Servers per pool</span></span></th>
<th><span data-ttu-id="5245e-182">Número de direcciones IP requeridas Lync Server 2013 (equilibrio de carga DNS)</span><span class="sxs-lookup"><span data-stu-id="5245e-182">Number of required IP addresses Lync Server 2013 (DNS load balanced)</span></span></th>
<th><span data-ttu-id="5245e-183">Número de direcciones IP requeridas Lync Server 2013 (equilibrio de carga de hardware)</span><span class="sxs-lookup"><span data-stu-id="5245e-183">Number of required IP addresses Lync Server 2013 (hardware load balanced)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5245e-184">2</span><span class="sxs-lookup"><span data-stu-id="5245e-184">2</span></span></p></td>
<td><p><span data-ttu-id="5245e-185">2</span><span class="sxs-lookup"><span data-stu-id="5245e-185">2</span></span></p></td>
<td><p><span data-ttu-id="5245e-186">1 (1 por VIP) + 2</span><span class="sxs-lookup"><span data-stu-id="5245e-186">1 (1 per VIP) + 2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5245e-187">3</span><span class="sxs-lookup"><span data-stu-id="5245e-187">3</span></span></p></td>
<td><p><span data-ttu-id="5245e-188">3</span><span class="sxs-lookup"><span data-stu-id="5245e-188">3</span></span></p></td>
<td><p><span data-ttu-id="5245e-189">1 (1 por VIP) + 3</span><span class="sxs-lookup"><span data-stu-id="5245e-189">1 (1 per VIP) + 3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5245e-190">4</span><span class="sxs-lookup"><span data-stu-id="5245e-190">4</span></span></p></td>
<td><p><span data-ttu-id="5245e-191">4</span><span class="sxs-lookup"><span data-stu-id="5245e-191">4</span></span></p></td>
<td><p><span data-ttu-id="5245e-192">1 (1 por VIP) + 4</span><span class="sxs-lookup"><span data-stu-id="5245e-192">1 (1 per VIP) + 4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5245e-193">5</span><span class="sxs-lookup"><span data-stu-id="5245e-193">5</span></span></p></td>
<td><p><span data-ttu-id="5245e-194">5</span><span class="sxs-lookup"><span data-stu-id="5245e-194">5</span></span></p></td>
<td><p><span data-ttu-id="5245e-195">1 (1 por VIP) + 5</span><span class="sxs-lookup"><span data-stu-id="5245e-195">1 (1 per VIP) + 5</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5245e-196">Los principales puntos de decisiones para la selección de topología son la alta disponibilidad y el equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="5245e-196">The primary decision points for topology selection are high availability and load balancing.</span></span> <span data-ttu-id="5245e-197">El requisito de alta disponibilidad puede influir en la decisión de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="5245e-197">The requirement for high availability can influence the load balancing decision.</span></span>

  - <span data-ttu-id="5245e-198">_ *Alta disponibilidad*\* si necesita una alta disponibilidad, implemente al menos dos servidores perimetrales en un grupo.</span><span class="sxs-lookup"><span data-stu-id="5245e-198">_ *High availability*\*   If you need high availability, deploy at least two Edge Servers in a pool.</span></span> <span data-ttu-id="5245e-199">Un único grupo de borde soportará hasta doce servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="5245e-199">A single Edge pool will support up to twelve Edge Servers.</span></span> <span data-ttu-id="5245e-200">Si se requiere más capacidad, puede implementar varias agrupaciones perimetrales.</span><span class="sxs-lookup"><span data-stu-id="5245e-200">If more capacity is required, you can deploy multiple Edge pools.</span></span> <span data-ttu-id="5245e-201">Como regla general, el 10% de una base de usuarios determinada necesitará acceso externo.</span><span class="sxs-lookup"><span data-stu-id="5245e-201">As a general rule, 10% of a given user base will need external access.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="5245e-202">El generador de topología le permitirá configurar hasta veinte servidores perimetrales en un único Pool perimetral.</span><span class="sxs-lookup"><span data-stu-id="5245e-202">Topology Builder will allow you to configure up to twenty Edge Servers in a single Edge pool.</span></span> <span data-ttu-id="5245e-203">La cantidad máxima admitida y probada de servidores perimetrales en un grupo es de doce y el creador de topologías que permite un número mayor de doce no se debe interpretar como compatibilidad implícita para más de doce servidores perimetrales en un solo grupo de borde.</span><span class="sxs-lookup"><span data-stu-id="5245e-203">The tested and supported maximum number of Edge Servers in a pool is twelve and Topology Builder allowing for a number larger than twelve should not be construed as implied support for more than twelve Edge Servers in a single Edge pool.</span></span>

    
    </div>

  - <span data-ttu-id="5245e-204">**Equilibrio de carga de hardware**   El equilibrio de carga de hardware es compatible con el equilibrio de carga de servidores perimetrales de Lync Server 2013 al usar direcciones IP enrutables públicas para las interfaces externas de Edge.</span><span class="sxs-lookup"><span data-stu-id="5245e-204">**Hardware load balancing**   Hardware load balancing is supported for load balancing Lync Server 2013 Edge Servers when using publicly routable IP addresses for the Edge external interfaces.</span></span> <span data-ttu-id="5245e-205">Por ejemplo, usaría este enfoque en situaciones en las que se necesita la conmutación por error para cualquiera de las siguientes aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="5245e-205">For example, you would use this approach in situations where failover is required for any of the following applications:</span></span>
    
      - <span data-ttu-id="5245e-206">Conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="5245e-206">Public IM connectivity</span></span>
    
      - <span data-ttu-id="5245e-207">Federación con empresas que ejecutan Microsoft Office Communications Server 2007 o Microsoft Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="5245e-207">Federation with companies running Microsoft Office Communications Server 2007 or Microsoft Office Communications Server 2007 R2</span></span>
    
      - <span data-ttu-id="5245e-208">Acceso externo a la mensajería unificada de Exchange 2007 o UM de Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="5245e-208">External access to Exchange 2007 Unified Messaging (UM) or Exchange 2010 UM</span></span>
        
        <div>
        

        > [!IMPORTANT]
        > <span data-ttu-id="5245e-209">El equilibrio de carga de DNS para Exchange 2010 SP1 y versiones posteriores es compatible con la mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5245e-209">DNS load balancing for Exchange 2010 SP1 and newer is supported for Exchange UM.</span></span>

        
        </div>
    
    <span data-ttu-id="5245e-210">Estas tres aplicaciones seguirán funcionando, pero no son conscientes del equilibrio de carga de DNS y solo se conectarán al primer servidor perimetral del grupo.</span><span class="sxs-lookup"><span data-stu-id="5245e-210">These three applications will continue to operate, but they are not DNS load balancing aware and will only connect to the first Edge Server in the pool.</span></span> <span data-ttu-id="5245e-211">Si el servidor no está disponible, se producirá un error en la conexión.</span><span class="sxs-lookup"><span data-stu-id="5245e-211">If that server is unavailable, the connection will fail.</span></span> <span data-ttu-id="5245e-212">Por ejemplo, si se implementan varios servidores perimetrales en un grupo para controlar la carga de tráfico federada, solo un proxy de acceso realmente recibe tráfico mientras otros están inactivos.</span><span class="sxs-lookup"><span data-stu-id="5245e-212">For example, if multiple Edge Servers are deployed in a pool to handle the federated traffic load, only one access proxy actually receives traffic while the others are idle.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="5245e-213">Se recomienda usar el equilibrio de carga de DNS si está en la Federación con empresas que usan Lync Server 2010 y Office 365 o Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5245e-213">Using DNS load balancing is recommended if you are federating with companies using Lync Server 2010 and Office 365 or Microsoft 365.</span></span> <span data-ttu-id="5245e-214">Tenga en cuenta que se produce un importante impacto en el rendimiento si la mayoría de los socios federados usan Office Communications Server 2007 u Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="5245e-214">Be aware that there are significant performance impacts if most of your federated partners are using Office Communications Server 2007 or Office Communications Server 2007 R2.</span></span>



<span data-ttu-id="5245e-215"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5245e-215"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

