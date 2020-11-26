---
title: 'Lync Server 2013: Resumen de puerto - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP privadas mediante NAT'
description: 'Lync Server 2013: límite consolidado de puertos resumidos, equilibrio de carga de DNS con direcciones IP privadas mediante NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: a296c2af-54d4-4b4f-9795-9191baf688cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412756(v=OCS.15)
ms:contentKeyID: 48184955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e0402b6682e86e5edf263fca78dfbe0f8fa070b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424289"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="c57b3-103">Resumen de puerto - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP privadas mediante NAT en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c57b3-103">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c57b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c57b3-104">

<span> </span></span></span>

<span data-ttu-id="c57b3-105">_**Última modificación del tema:** 2012-12-04_</span><span class="sxs-lookup"><span data-stu-id="c57b3-105">_**Topic Last Modified:** 2012-12-04_</span></span>

<span data-ttu-id="c57b3-106">La funcionalidad del servidor de Lync Server 2013, que se describe en esta arquitectura de escenario, es muy similar a la que se ha implementado en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c57b3-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="c57b3-107">La adición más destacada es el puerto **5269 sobre** la entrada TCP para el protocolo de presencia y mensajería extensible (XMPP).</span><span class="sxs-lookup"><span data-stu-id="c57b3-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="c57b3-108">Lync Server 2013 implementa opcionalmente un proxy XMPP en el servidor perimetral o en el grupo perimetral y el servidor de puerta de enlace XMPP en el servidor front-end o en el grupo front-end.</span><span class="sxs-lookup"><span data-stu-id="c57b3-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="c57b3-109">Además de IPv4, el servidor EDGE ahora es compatible con IPv6.</span><span class="sxs-lookup"><span data-stu-id="c57b3-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="c57b3-110">Para mayor claridad, solo se usa IPv4 en los escenarios.</span><span class="sxs-lookup"><span data-stu-id="c57b3-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="c57b3-111">**Red perimetral empresarial para el perímetro consolidado con direcciones IP privadas mediante NAT**</span><span class="sxs-lookup"><span data-stu-id="c57b3-111">**Enterprise perimeter network for scaled consolidated edge with private IP addresses using NAT**</span></span>

<span data-ttu-id="c57b3-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="c57b3-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="c57b3-113">Detalles de protocolo y puerto</span><span class="sxs-lookup"><span data-stu-id="c57b3-113">Port and Protocol Details</span></span>

<span data-ttu-id="c57b3-114">Le recomendamos que abra solo los puertos necesarios para admitir la funcionalidad para la que proporciona acceso externo.</span><span class="sxs-lookup"><span data-stu-id="c57b3-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="c57b3-115">Para que el acceso remoto funcione para cualquier servicio perimetral, es obligatorio que el tráfico SIP pueda fluir de forma bidireccional tal y como se muestra en la cifra de tráfico entrante o saliente.</span><span class="sxs-lookup"><span data-stu-id="c57b3-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="c57b3-116">En concreto, los mensajes SIP a y desde el servicio perimetral de acceso participan en la mensajería instantánea (mi), presencia, conferencias web, audio/vídeo (A/V) y Federación.</span><span class="sxs-lookup"><span data-stu-id="c57b3-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="c57b3-117">Resumen de Firewall para Edge consolidado, equilibrio de carga de DNS con direcciones IP privadas mediante NAT: interfaz externa-nodo 1 y nodo 2 (ejemplo)</span><span class="sxs-lookup"><span data-stu-id="c57b3-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c57b3-118">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="c57b3-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="c57b3-119">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="c57b3-119">Source IP address</span></span></th>
<th><span data-ttu-id="c57b3-120">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="c57b3-120">Destination IP address</span></span></th>
<th><span data-ttu-id="c57b3-121">Notas</span><span class="sxs-lookup"><span data-stu-id="c57b3-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="c57b3-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="c57b3-123">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-123">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-124">Servicio de proxy XMPP (comparte dirección IP con servicio perimetral de acceso)</span><span class="sxs-lookup"><span data-stu-id="c57b3-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="c57b3-125">El servicio Proxy XMPP acepta el tráfico de los contactos XMPP en las federaciones XMPP definidas</span><span class="sxs-lookup"><span data-stu-id="c57b3-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-126">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="c57b3-126">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="c57b3-127">Servicio de proxy XMPP (comparte dirección IP con servicio perimetral de acceso)</span><span class="sxs-lookup"><span data-stu-id="c57b3-127">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="c57b3-128">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-128">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-129">El servicio Proxy XMPP envía tráfico a los contactos XMPP en las federaciones XMPP definidas</span><span class="sxs-lookup"><span data-stu-id="c57b3-129">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-130">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="c57b3-130">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="c57b3-131">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-132">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-132">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-133">Comprobación y recuperación de CRL o revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="c57b3-133">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-134">Acceso/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="c57b3-134">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="c57b3-135">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-136">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-136">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-137">Consulta DNS a través de TCP</span><span class="sxs-lookup"><span data-stu-id="c57b3-137">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-138">Acceso/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="c57b3-138">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="c57b3-139">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-139">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-140">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-140">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-141">Consulta DNS a través de UDP</span><span class="sxs-lookup"><span data-stu-id="c57b3-141">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-142">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="c57b3-142">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="c57b3-143">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-143">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-144">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-145">Tráfico SIP de cliente a servidor para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="c57b3-145">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-146">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="c57b3-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="c57b3-147">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-147">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-148">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-148">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-149">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="c57b3-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-150">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="c57b3-150">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="c57b3-151">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-151">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-152">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-152">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-153">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="c57b3-153">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-154">Conferencias web/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="c57b3-154">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="c57b3-155">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-155">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-156">Servicio perimetral de conferencias web del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-156">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-157">Medios de conferencia Web</span><span class="sxs-lookup"><span data-stu-id="c57b3-157">Web Conferencing media</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-158">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="c57b3-158">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="c57b3-159">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-160">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-160">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-161">Necesario para la Federación con socios que ejecutan Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 y Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c57b3-161">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-162">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="c57b3-162">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="c57b3-163">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-163">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-164">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-164">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-165">Solo es necesario para la Federación con socios que ejecutan Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="c57b3-165">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-166">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="c57b3-166">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="c57b3-167">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-167">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-168">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-169">Necesario solo para la Federación con socios que ejecutan Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="c57b3-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-170">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="c57b3-170">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="c57b3-171">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-171">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-172">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-172">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-173">Necesario solo para la Federación con socios que ejecutan Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="c57b3-173">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-174">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="c57b3-174">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="c57b3-175">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-175">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-176">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-176">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-177">3478 saliente se usa para determinar la versión del servidor perimetral con el que se comunica Lync Server y también para el tráfico de multimedia de un servidor perimetral a un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="c57b3-177">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="c57b3-178">Necesario para la Federación con Lync Server 2010, Windows Live Messenger y Office Communications Server 2007 R2, y también si se han implementado varias agrupaciones perimetrales dentro de una empresa.</span><span class="sxs-lookup"><span data-stu-id="c57b3-178">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-179">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="c57b3-179">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="c57b3-180">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-180">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-181">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-182">STUN/TURN negociación de candidatos a través de UDP/3478</span><span class="sxs-lookup"><span data-stu-id="c57b3-182">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="c57b3-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="c57b3-184">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-184">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-185">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-185">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-186">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="c57b3-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-187">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="c57b3-187">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="c57b3-188">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-188">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-189">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-189">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-190">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="c57b3-190">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="c57b3-191">Resumen de Firewall para Edge consolidado con escala, equilibrio de carga de DNS con direcciones IP privadas mediante NAT: interfaz interna-nodo 1 y nodo 2 (ejemplo)</span><span class="sxs-lookup"><span data-stu-id="c57b3-191">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c57b3-192">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="c57b3-192">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="c57b3-193">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="c57b3-193">Source IP address</span></span></th>
<th><span data-ttu-id="c57b3-194">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="c57b3-194">Destination IP address</span></span></th>
<th><span data-ttu-id="c57b3-195">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c57b3-195">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-196">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="c57b3-196">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="c57b3-197">Cualquiera (se puede definir como la dirección del servidor front-end o la dirección IP del grupo de servidores front-end que ejecuta el servicio de puerta de enlace XMPP)</span><span class="sxs-lookup"><span data-stu-id="c57b3-197">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="c57b3-198">Dirección IP de la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-198">Edge Server internal interface IP address</span></span></p></td>
<td><p><span data-ttu-id="c57b3-199">Tráfico XMPP saliente del servicio de puerta de enlace XMPP que se ejecuta en el servidor front-end o grupo front-end</span><span class="sxs-lookup"><span data-stu-id="c57b3-199">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="c57b3-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="c57b3-201">Cualquiera (se puede definir como director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="c57b3-201">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="c57b3-202">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-203">Tráfico SIP saliente (del Director, la dirección IP del grupo de directores, el servidor front-end o la dirección IP del grupo de servidores front-end) a la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-203">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-204">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="c57b3-204">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="c57b3-205">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-205">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-206">Cualquiera (se puede definir como director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="c57b3-206">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="c57b3-207">Tráfico SIP entrante (Director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo front-end) de la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-207">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-208">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="c57b3-208">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="c57b3-209">Cualquiera (se puede definir como la dirección IP del servidor front-end o cada dirección IP del servidor front-end en un grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="c57b3-209">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="c57b3-210">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-211">Tráfico de conferencias web desde el servidor front-end o cada servidor front-end si se está en un grupo, a la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-211">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-212">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="c57b3-212">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="c57b3-213">Cualquiera (se puede definir como la dirección IP del servidor front-end, la dirección IP del grupo de servidores front-end o cualquier otro equipo de sucursal o servidor de sucursal con la supervivencia que use este servidor perimetral)</span><span class="sxs-lookup"><span data-stu-id="c57b3-213">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="c57b3-214">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-215">Autenticación de usuarios A/V (servicio de autenticación A/V) desde el servidor front-end o la dirección IP del grupo de servidores front-end o cualquier otro dispositivo de sucursal que sea reviviente o con el servidor de sucursal</span><span class="sxs-lookup"><span data-stu-id="c57b3-215">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-216">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="c57b3-216">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="c57b3-217">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-217">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-218">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-219">Ruta preferida para la transferencia de medios A/V entre usuarios internos y externos, un equipo de sucursal o un servidor de sucursal con la supervivencia</span><span class="sxs-lookup"><span data-stu-id="c57b3-219">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-220">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="c57b3-220">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="c57b3-221">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-221">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-222">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-223">Ruta de reserva para la transferencia de medios A/V entre usuarios internos y externos, equipo de sucursal con la supervivencia o servidor de sucursal con la supervivencia, si no se puede establecer la comunicación UDP, se usa TCP para la transferencia de archivos y el uso compartido de escritorio</span><span class="sxs-lookup"><span data-stu-id="c57b3-223">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-224">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="c57b3-224">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="c57b3-225">Cualquiera (puede definirse como la dirección IP del servidor front-end o el grupo que contiene el almacén de administración central)</span><span class="sxs-lookup"><span data-stu-id="c57b3-225">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="c57b3-226">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-227">Replicación de los cambios del almacén de administración central al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-227">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-228">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="c57b3-228">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="c57b3-229">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-229">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-230">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-231">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="c57b3-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-232">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="c57b3-232">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="c57b3-233">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-233">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-234">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-235">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="c57b3-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-236">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="c57b3-236">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="c57b3-237">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-237">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-238">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="c57b3-238">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="c57b3-239">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="c57b3-239">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="c57b3-240">Resumen del firewall para la Federación</span><span class="sxs-lookup"><span data-stu-id="c57b3-240">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c57b3-241">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="c57b3-241">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="c57b3-242">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="c57b3-242">Source IP address</span></span></th>
<th><span data-ttu-id="c57b3-243">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="c57b3-243">Destination IP address</span></span></th>
<th><span data-ttu-id="c57b3-244">Notas</span><span class="sxs-lookup"><span data-stu-id="c57b3-244">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-245">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="c57b3-245">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="c57b3-246">Dirección IP pública del servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="c57b3-246">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="c57b3-247">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-247">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-248">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="c57b3-248">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="c57b3-249">Resumen del firewall: conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="c57b3-249">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c57b3-250">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="c57b3-250">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="c57b3-251">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="c57b3-251">Source IP address</span></span></th>
<th><span data-ttu-id="c57b3-252">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="c57b3-252">Destination IP address</span></span></th>
<th><span data-ttu-id="c57b3-253">Notas</span><span class="sxs-lookup"><span data-stu-id="c57b3-253">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-254">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="c57b3-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="c57b3-255">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="c57b3-255">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="c57b3-256">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-257">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="c57b3-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-258">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="c57b3-258">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="c57b3-259">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-259">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-260">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="c57b3-260">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="c57b3-261">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="c57b3-261">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-262">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="c57b3-262">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="c57b3-263">Clientes</span><span class="sxs-lookup"><span data-stu-id="c57b3-263">Clients</span></span></p></td>
<td><p><span data-ttu-id="c57b3-264">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-264">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-265">Tráfico SIP de cliente a servidor para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="c57b3-265">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-266">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="c57b3-266">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="c57b3-267">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-268">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="c57b3-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="c57b3-269">Se usa para sesiones de A/V con Windows Live Messenger si está configurada la conectividad de mensajería instantánea pública.</span><span class="sxs-lookup"><span data-stu-id="c57b3-269">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="c57b3-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="c57b3-271">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-271">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-272">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="c57b3-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="c57b3-273">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="c57b3-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-274">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="c57b3-274">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="c57b3-275">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="c57b3-275">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="c57b3-276">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-276">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="c57b3-277">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="c57b3-277">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="c57b3-278">Resumen de Firewall para el protocolo de presencia y mensajería extensible</span><span class="sxs-lookup"><span data-stu-id="c57b3-278">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c57b3-279">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="c57b3-279">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="c57b3-280">Origen (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="c57b3-280">Source (IP address)</span></span></th>
<th><span data-ttu-id="c57b3-281">Destino (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="c57b3-281">Destination (IP address)</span></span></th>
<th><span data-ttu-id="c57b3-282">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c57b3-282">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-283">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="c57b3-283">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="c57b3-284">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-284">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-285">Dirección IP de la interfaz de servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="c57b3-286">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="c57b3-286">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="c57b3-287">Permite la comunicación con el proxy XMPP del servidor perimetral de socios de XMPP</span><span class="sxs-lookup"><span data-stu-id="c57b3-287">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57b3-288">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="c57b3-288">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="c57b3-289">Dirección IP de la interfaz de servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-289">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="c57b3-290">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-290">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-291">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="c57b3-291">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="c57b3-292">Permite la comunicación desde el proxy XMPP del servidor perimetral a socios XMPP de Federación</span><span class="sxs-lookup"><span data-stu-id="c57b3-292">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57b3-293">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="c57b3-293">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="c57b3-294">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c57b3-294">Any</span></span></p></td>
<td><p><span data-ttu-id="c57b3-295">Cada IP de la interfaz del servidor perimetral interno</span><span class="sxs-lookup"><span data-stu-id="c57b3-295">Each internal Edge Server interface IP</span></span></p></td>
<td><p><span data-ttu-id="c57b3-296">Tráfico de XMPP interno de la puerta de enlace XMPP en el servidor front-end o grupo front-end a la dirección IP interna del servidor perimetral o a la dirección IP interna de cada miembro del grupo perimetral</span><span class="sxs-lookup"><span data-stu-id="c57b3-296">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c57b3-297">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c57b3-297">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

