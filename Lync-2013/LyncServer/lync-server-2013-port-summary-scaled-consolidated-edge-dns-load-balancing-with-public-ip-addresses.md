---
title: 'Lync Server 2013: Resumen de puerto - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP públicas'
description: 'Lync Server 2013: límite consolidado de puertos resumidos, equilibrio de carga DNS con direcciones IP públicas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: f7cbd0f1-841d-4116-8d17-e9d991daa4a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205394(v=OCS.15)
ms:contentKeyID: 48185865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8090435485b4b6a183702a608b139cec91ae26a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446342"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="bc719-103">Resumen de puerto - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc719-103">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc719-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc719-104">

<span> </span></span></span>

<span data-ttu-id="bc719-105">_**Última modificación del tema:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="bc719-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="bc719-106">La funcionalidad del servidor de Lync Server 2013, que se describe en esta arquitectura de escenario, es muy similar a la que se ha implementado en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="bc719-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="bc719-107">La adición más destacada es el puerto **5269 sobre** la entrada TCP para el protocolo de presencia y mensajería extensible (XMPP).</span><span class="sxs-lookup"><span data-stu-id="bc719-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="bc719-108">Lync Server 2013 implementa opcionalmente un proxy XMPP en el servidor perimetral o en el grupo perimetral y el servidor de puerta de enlace XMPP en el servidor front-end o en el grupo front-end.</span><span class="sxs-lookup"><span data-stu-id="bc719-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="bc719-109">Además de IPv4, el servidor EDGE ahora es compatible con IPv6.</span><span class="sxs-lookup"><span data-stu-id="bc719-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="bc719-110">Para mayor claridad, solo se usa IPv4 en los escenarios.</span><span class="sxs-lookup"><span data-stu-id="bc719-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="bc719-111">**Red perimetral empresarial para la tecnología perimetral consolidada, equilibrio de carga DNS con direcciones IP públicas**</span><span class="sxs-lookup"><span data-stu-id="bc719-111">**Enterprise perimeter network for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses**</span></span>

<span data-ttu-id="bc719-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="bc719-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="bc719-113">Detalles de protocolo y puerto</span><span class="sxs-lookup"><span data-stu-id="bc719-113">Port and Protocol Details</span></span>

<span data-ttu-id="bc719-114">Le recomendamos que abra solo los puertos necesarios para admitir la funcionalidad para la que proporciona acceso externo.</span><span class="sxs-lookup"><span data-stu-id="bc719-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="bc719-115">Para que el acceso remoto funcione para cualquier servicio perimetral, es obligatorio que el tráfico SIP pueda fluir de forma bidireccional tal y como se muestra en la cifra de tráfico entrante o saliente.</span><span class="sxs-lookup"><span data-stu-id="bc719-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="bc719-116">En concreto, los mensajes SIP a y desde el servicio perimetral de acceso participan en la mensajería instantánea (mi), presencia, conferencias web, audio/vídeo (A/V) y Federación.</span><span class="sxs-lookup"><span data-stu-id="bc719-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="bc719-117">Resumen del firewall para la tecnología perimetral consolidada, equilibrio de carga DNS con direcciones IP públicas: interfaz externa-nodo 1 y nodo 2 (ejemplo)</span><span class="sxs-lookup"><span data-stu-id="bc719-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc719-118">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="bc719-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="bc719-119">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="bc719-119">Source IP address</span></span></th>
<th><span data-ttu-id="bc719-120">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="bc719-120">Destination IP address</span></span></th>
<th><span data-ttu-id="bc719-121">Notas</span><span class="sxs-lookup"><span data-stu-id="bc719-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc719-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="bc719-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="bc719-123">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-123">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-124">Servicio de proxy XMPP (comparte dirección IP con servicio perimetral de acceso)</span><span class="sxs-lookup"><span data-stu-id="bc719-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="bc719-125">El servicio Proxy XMPP acepta el tráfico de los contactos XMPP en las federaciones XMPP definidas</span><span class="sxs-lookup"><span data-stu-id="bc719-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-126">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="bc719-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="bc719-127">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-128">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-128">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-129">Comprobación y recuperación de CRL o revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="bc719-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-130">Acceso/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="bc719-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="bc719-131">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-132">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-132">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-133">Consulta DNS a través de TCP</span><span class="sxs-lookup"><span data-stu-id="bc719-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-134">Acceso/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="bc719-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="bc719-135">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-135">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-136">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-136">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-137">Consulta DNS a través de UDP</span><span class="sxs-lookup"><span data-stu-id="bc719-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-138">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="bc719-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="bc719-139">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-139">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-140">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-140">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-141">Tráfico SIP de cliente a servidor para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="bc719-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-142">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="bc719-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="bc719-143">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-143">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-144">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-144">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-145">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="bc719-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-146">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="bc719-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="bc719-147">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-147">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-148">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-148">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-149">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="bc719-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-150">Conferencias web/PSOM (TLS) TCP/443</span><span class="sxs-lookup"><span data-stu-id="bc719-150">Web Conferencing/PSOM(TLS)TCP/443</span></span></p></td>
<td><p><span data-ttu-id="bc719-151">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-151">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-152">Dirección IP pública del servicio perimetral de conferencias web del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-152">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-153">Medios de conferencia Web</span><span class="sxs-lookup"><span data-stu-id="bc719-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-154">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="bc719-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="bc719-155">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-155">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-156">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-156">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-157">Necesario para la Federación con socios que ejecutan Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 y Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bc719-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-158">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="bc719-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="bc719-159">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-159">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-160">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-160">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-161">Solo es necesario para la Federación con socios que ejecutan Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="bc719-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-162">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="bc719-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="bc719-163">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-163">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-164">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-165">Necesario solo para la Federación con socios que ejecutan Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="bc719-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-166">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="bc719-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="bc719-167">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-167">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-168">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-168">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-169">Necesario solo para la Federación con socios que ejecutan Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="bc719-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-170">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="bc719-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="bc719-171">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-171">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-172">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-172">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-173">3478 saliente se usa para determinar la versión del servidor perimetral con el que se comunica Lync Server y también para el tráfico de multimedia de un servidor perimetral a un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="bc719-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="bc719-174">Necesario para la Federación con Lync Server 2010, Windows Live Messenger y Office Communications Server 2007 R2, y también si se han implementado varias agrupaciones perimetrales dentro de una empresa.</span><span class="sxs-lookup"><span data-stu-id="bc719-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-175">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="bc719-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="bc719-176">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-176">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-177">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-177">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-178">STUN/TURN negociación de candidatos a través de UDP/3478</span><span class="sxs-lookup"><span data-stu-id="bc719-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-179">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="bc719-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="bc719-180">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-180">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-181">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-181">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-182">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="bc719-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="bc719-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="bc719-184">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="bc719-185">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-185">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-186">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="bc719-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="bc719-187">Resumen del firewall para la tecnología perimetral consolidada, equilibrio de carga DNS con direcciones IP públicas: interfaz interna – nodo 1 y nodo 2 (ejemplo)</span><span class="sxs-lookup"><span data-stu-id="bc719-187">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc719-188">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="bc719-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="bc719-189">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="bc719-189">Source IP address</span></span></th>
<th><span data-ttu-id="bc719-190">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="bc719-190">Destination IP address</span></span></th>
<th><span data-ttu-id="bc719-191">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc719-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc719-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="bc719-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="bc719-193">Cualquiera (se puede definir como la dirección del servidor front-end o la dirección IP del grupo de servidores front-end que ejecuta el servicio de puerta de enlace XMPP)</span><span class="sxs-lookup"><span data-stu-id="bc719-193">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="bc719-194">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-195">Tráfico XMPP saliente del servicio de puerta de enlace XMPP que se ejecuta en el servidor front-end o grupo front-end</span><span class="sxs-lookup"><span data-stu-id="bc719-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="bc719-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="bc719-197">Cualquiera (se puede definir como director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="bc719-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="bc719-198">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-199">Tráfico SIP saliente (del Director, la dirección IP del grupo de directores, el servidor front-end o la dirección IP del grupo de servidores front-end) a la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="bc719-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="bc719-201">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-202">Cualquiera (se puede definir como director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="bc719-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="bc719-203">Tráfico SIP entrante (Director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo front-end) de la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="bc719-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="bc719-205">Cualquiera (se puede definir como la dirección IP del servidor front-end o cada dirección IP del servidor front-end en un grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="bc719-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="bc719-206">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-207">Tráfico de conferencias web desde el servidor front-end o cada servidor front-end si se está en un grupo, a la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="bc719-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="bc719-209">Cualquiera (se puede definir como la dirección IP del servidor front-end, la dirección IP del grupo de servidores front-end o cualquier otro equipo de sucursal o servidor de sucursal con la supervivencia que use este servidor perimetral)</span><span class="sxs-lookup"><span data-stu-id="bc719-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="bc719-210">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-211">Autenticación de usuarios A/V (servicio de autenticación A/V) desde el servidor front-end o la dirección IP del grupo de servidores front-end o cualquier otro dispositivo de sucursal que sea reviviente o con el servidor de sucursal</span><span class="sxs-lookup"><span data-stu-id="bc719-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="bc719-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="bc719-213">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-213">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-214">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-215">Ruta preferida para la transferencia de medios A/V entre usuarios internos y externos, un equipo de sucursal o un servidor de sucursal con la supervivencia</span><span class="sxs-lookup"><span data-stu-id="bc719-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-216">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="bc719-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="bc719-217">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-217">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-218">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-219">Ruta de reserva para la transferencia de medios A/V entre usuarios internos y externos, equipo de sucursal con la supervivencia o servidor de sucursal con la supervivencia, si no se puede establecer la comunicación UDP, se usa TCP para la transferencia de archivos y el uso compartido de escritorio</span><span class="sxs-lookup"><span data-stu-id="bc719-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="bc719-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="bc719-221">Cualquiera (puede definirse como la dirección IP del servidor front-end o el grupo que contiene el almacén de administración central)</span><span class="sxs-lookup"><span data-stu-id="bc719-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="bc719-222">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-223">Replicación de los cambios del almacén de administración central al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="bc719-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="bc719-225">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-225">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-226">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-227">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="bc719-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="bc719-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="bc719-229">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-229">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-230">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-231">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="bc719-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="bc719-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="bc719-233">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-233">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-234">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="bc719-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="bc719-235">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="bc719-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="bc719-236">Resumen del firewall para la Federación</span><span class="sxs-lookup"><span data-stu-id="bc719-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc719-237">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="bc719-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="bc719-238">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="bc719-238">Source IP address</span></span></th>
<th><span data-ttu-id="bc719-239">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="bc719-239">Destination IP address</span></span></th>
<th><span data-ttu-id="bc719-240">Notas</span><span class="sxs-lookup"><span data-stu-id="bc719-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc719-241">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="bc719-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="bc719-242">Dirección IP pública del servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="bc719-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-243">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-243">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-244">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="bc719-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="bc719-245">Resumen del firewall: conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="bc719-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc719-246">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="bc719-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="bc719-247">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="bc719-247">Source IP address</span></span></th>
<th><span data-ttu-id="bc719-248">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="bc719-248">Destination IP address</span></span></th>
<th><span data-ttu-id="bc719-249">Notas</span><span class="sxs-lookup"><span data-stu-id="bc719-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc719-250">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="bc719-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="bc719-251">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="bc719-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="bc719-252">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="bc719-253">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="bc719-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-254">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="bc719-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="bc719-255">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="bc719-256">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="bc719-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="bc719-257">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="bc719-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-258">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="bc719-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="bc719-259">Clientes</span><span class="sxs-lookup"><span data-stu-id="bc719-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="bc719-260">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="bc719-261">Tráfico SIP de cliente a servidor para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="bc719-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-262">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="bc719-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="bc719-263">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="bc719-264">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="bc719-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="bc719-265">Se usa para sesiones de A/V con Windows Live Messenger si está configurada la conectividad de mensajería instantánea pública.</span><span class="sxs-lookup"><span data-stu-id="bc719-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-266">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="bc719-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="bc719-267">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="bc719-268">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="bc719-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="bc719-269">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="bc719-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="bc719-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="bc719-271">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="bc719-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="bc719-272">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="bc719-273">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="bc719-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="bc719-274">Resumen de Firewall para el protocolo de presencia y mensajería extensible</span><span class="sxs-lookup"><span data-stu-id="bc719-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc719-275">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="bc719-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="bc719-276">Origen (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="bc719-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="bc719-277">Destino (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="bc719-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="bc719-278">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc719-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc719-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="bc719-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="bc719-280">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-280">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-281">Dirección IP de la interfaz de servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-282">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="bc719-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="bc719-283">Permite la comunicación con el proxy XMPP del servidor perimetral de socios de XMPP</span><span class="sxs-lookup"><span data-stu-id="bc719-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc719-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="bc719-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="bc719-285">Dirección IP de la interfaz de servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="bc719-286">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-286">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-287">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="bc719-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="bc719-288">Permite la comunicación desde el proxy XMPP del servidor perimetral a socios XMPP de Federación</span><span class="sxs-lookup"><span data-stu-id="bc719-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc719-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="bc719-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="bc719-290">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="bc719-290">Any</span></span></p></td>
<td><p><span data-ttu-id="bc719-291">Cada IP de la interfaz del servidor perimetral interno</span><span class="sxs-lookup"><span data-stu-id="bc719-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="bc719-292">Tráfico de XMPP interno de la puerta de enlace XMPP en el servidor front-end o grupo front-end a la dirección IP interna del servidor perimetral o a la dirección IP interna de cada miembro del grupo perimetral</span><span class="sxs-lookup"><span data-stu-id="bc719-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bc719-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc719-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

