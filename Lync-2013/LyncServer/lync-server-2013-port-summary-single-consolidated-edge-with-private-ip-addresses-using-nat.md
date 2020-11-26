---
title: Resumen de puerto - Perímetro consolidado de un solo equipo con direcciones IP privadas mediante NAT
description: 'Resumen de puertos: un solo borde consolidado con direcciones IP privadas con NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with private IP addresses using NAT
ms:assetid: 3c1a389f-5f42-4719-a05b-e0b84aa3eb9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425891(v=OCS.15)
ms:contentKeyID: 48183877
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3fc182b9fbbd24d589feb7f73e3c0086fa23152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424299"
---
# <a name="port-summary---single-consolidated-edge-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="cb67b-103">Resumen de puerto - Perímetro consolidado de un solo equipo con direcciones IP privadas mediante NAT en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb67b-103">Port summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb67b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb67b-104">

<span> </span></span></span>

<span data-ttu-id="cb67b-105">_**Última modificación del tema:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="cb67b-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="cb67b-106">La funcionalidad del servidor de Lync Server 2013, que se describe en esta arquitectura de escenario, es muy similar a la que se ha implementado en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="cb67b-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="cb67b-107">La adición más destacada es el puerto **5269 sobre** la entrada TCP para el protocolo de presencia y mensajería extensible (XMPP).</span><span class="sxs-lookup"><span data-stu-id="cb67b-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="cb67b-108">Lync Server 2013 implementa opcionalmente un proxy XMPP en el servidor perimetral o en el grupo perimetral y el servidor de puerta de enlace XMPP en el servidor front-end o en el grupo front-end.</span><span class="sxs-lookup"><span data-stu-id="cb67b-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="cb67b-109">Además de IPv4, el servidor EDGE ahora es compatible con IPv6.</span><span class="sxs-lookup"><span data-stu-id="cb67b-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="cb67b-110">Para mayor claridad, solo se usa IPv4 en los escenarios.</span><span class="sxs-lookup"><span data-stu-id="cb67b-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="cb67b-111">**Perímetro de red para un único servidor consolidado con direccionamiento IP privado con NAT**</span><span class="sxs-lookup"><span data-stu-id="cb67b-111">**Network Perimeter for a Single Consolidated Edge Server with Private IP Addressing Using NAT**</span></span>

<span data-ttu-id="cb67b-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="cb67b-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="cb67b-113">Detalles de protocolo y puerto</span><span class="sxs-lookup"><span data-stu-id="cb67b-113">Port and Protocol Details</span></span>

<span data-ttu-id="cb67b-114">Le recomendamos que abra solo los puertos necesarios para admitir la funcionalidad para la que proporciona acceso externo.</span><span class="sxs-lookup"><span data-stu-id="cb67b-114">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="cb67b-115">Para que el acceso remoto funcione para cualquier servicio perimetral, es obligatorio que el tráfico SIP pueda fluir de forma bidireccional tal y como se muestra en la cifra de tráfico entrante o saliente.</span><span class="sxs-lookup"><span data-stu-id="cb67b-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="cb67b-116">En concreto, los mensajes SIP a y desde el servicio perimetral de acceso participan en la mensajería instantánea (mi), presencia, conferencias web, audio/vídeo (A/V) y Federación.</span><span class="sxs-lookup"><span data-stu-id="cb67b-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V), and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-external-interface"></a><span data-ttu-id="cb67b-117">Resumen del firewall para un solo borde consolidado con direcciones IP privadas que usan NAT: interfaz externa</span><span class="sxs-lookup"><span data-stu-id="cb67b-117">Firewall Summary for Single Consolidated Edge with Private IP Addresses using NAT: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb67b-118">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="cb67b-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cb67b-119">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="cb67b-119">Source IP address</span></span></th>
<th><span data-ttu-id="cb67b-120">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="cb67b-120">Destination IP address</span></span></th>
<th><span data-ttu-id="cb67b-121">Notas</span><span class="sxs-lookup"><span data-stu-id="cb67b-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="cb67b-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="cb67b-123">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-123">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-124">Servicio de proxy XMPP (comparte dirección IP con servicio perimetral de acceso)</span><span class="sxs-lookup"><span data-stu-id="cb67b-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="cb67b-125">El servicio Proxy XMPP acepta el tráfico de los contactos XMPP en las federaciones XMPP definidas</span><span class="sxs-lookup"><span data-stu-id="cb67b-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-126">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="cb67b-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="cb67b-127">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-127">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-128">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-128">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-129">Comprobación y recuperación de CRL o revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="cb67b-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-130">Acceso/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="cb67b-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="cb67b-131">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-132">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-132">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-133">Consulta DNS a través de TCP</span><span class="sxs-lookup"><span data-stu-id="cb67b-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-134">Acceso/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="cb67b-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="cb67b-135">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-136">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-136">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-137">Consulta DNS a través de UDP</span><span class="sxs-lookup"><span data-stu-id="cb67b-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-138">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="cb67b-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="cb67b-139">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-139">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-140">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-140">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-141">Tráfico SIP de cliente a servidor para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="cb67b-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-142">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="cb67b-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cb67b-143">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-143">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-144">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-145">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="cb67b-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-146">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="cb67b-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cb67b-147">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-147">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-148">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-148">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-149">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="cb67b-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-150">Conferencias web/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="cb67b-150">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="cb67b-151">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-151">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-152">Servicio perimetral de conferencias web del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-152">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-153">Medios de conferencia Web</span><span class="sxs-lookup"><span data-stu-id="cb67b-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-154">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="cb67b-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="cb67b-155">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-155">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-156">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-156">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-157">Necesario para la Federación con socios que ejecutan Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 y Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cb67b-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-158">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="cb67b-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="cb67b-159">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-160">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-160">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-161">Solo es necesario para la Federación con socios que ejecutan Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="cb67b-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-162">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="cb67b-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="cb67b-163">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-163">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-164">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-164">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-165">Necesario solo para la Federación con socios que ejecutan Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="cb67b-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-166">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="cb67b-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="cb67b-167">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-167">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-168">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-169">Necesario solo para la Federación con socios que ejecutan Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="cb67b-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-170">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="cb67b-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="cb67b-171">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-171">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-172">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-172">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-173">3478 saliente se usa para determinar la versión del servidor perimetral con el que se comunica Lync Server y también para el tráfico de multimedia de un servidor perimetral a un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="cb67b-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="cb67b-174">Necesario para la Federación con Lync Server 2010, Windows Live Messenger y Office Communications Server 2007 R2, y también si se han implementado varias agrupaciones perimetrales dentro de una empresa.</span><span class="sxs-lookup"><span data-stu-id="cb67b-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-175">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="cb67b-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="cb67b-176">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-176">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-177">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-177">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-178">STUN/TURN negociación de candidatos a través de UDP/3478</span><span class="sxs-lookup"><span data-stu-id="cb67b-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-179">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="cb67b-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="cb67b-180">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-180">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-181">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-182">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="cb67b-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="cb67b-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="cb67b-184">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-185">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-185">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-186">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="cb67b-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-internal-interface"></a><span data-ttu-id="cb67b-187">Resumen del firewall para un solo borde consolidado con direcciones IP privadas que usan NAT: interfaz interna</span><span class="sxs-lookup"><span data-stu-id="cb67b-187">Firewall Summary for Single Consolidated Edge with Private IP Addresses Using NAT: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb67b-188">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="cb67b-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cb67b-189">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="cb67b-189">Source IP address</span></span></th>
<th><span data-ttu-id="cb67b-190">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="cb67b-190">Destination IP address</span></span></th>
<th><span data-ttu-id="cb67b-191">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb67b-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="cb67b-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="cb67b-193">Cualquiera (puede definirse como IP de servidor Standard Edition, dirección IP del servidor Standard Edition o dirección IP del grupo de servidores que ejecuta el servicio de puerta de enlace XMPP)</span><span class="sxs-lookup"><span data-stu-id="cb67b-193">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="cb67b-194">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-195">Tráfico XMPP saliente del servicio de puerta de enlace XMPP que se ejecuta en el servidor front-end o grupo front-end</span><span class="sxs-lookup"><span data-stu-id="cb67b-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="cb67b-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cb67b-197">Cualquiera (se puede definir como director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="cb67b-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="cb67b-198">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-199">Tráfico SIP saliente (del Director, la dirección IP del grupo de directores, el servidor front-end o la dirección IP del grupo de servidores front-end) a la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="cb67b-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cb67b-201">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-202">Cualquiera (se puede definir como director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="cb67b-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="cb67b-203">Tráfico SIP entrante (Director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo front-end) de la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="cb67b-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="cb67b-205">Cualquiera (se puede definir como la dirección IP del servidor front-end o cada dirección IP del servidor front-end en un grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="cb67b-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="cb67b-206">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-207">Tráfico de conferencias web desde el servidor front-end o cada servidor front-end si se está en un grupo, a la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="cb67b-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="cb67b-209">Cualquiera (se puede definir como la dirección IP del servidor front-end, la dirección IP del grupo de servidores front-end o cualquier otro equipo de sucursal o servidor de sucursal con la supervivencia que use este servidor perimetral)</span><span class="sxs-lookup"><span data-stu-id="cb67b-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="cb67b-210">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-211">Autenticación de usuarios A/V (servicio de autenticación A/V) desde el servidor front-end o la dirección IP del grupo de servidores front-end o cualquier otro dispositivo de sucursal que sea reviviente o con el servidor de sucursal</span><span class="sxs-lookup"><span data-stu-id="cb67b-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="cb67b-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="cb67b-213">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-213">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-214">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-215">Ruta preferida para la transferencia de medios A/V entre usuarios internos y externos, un equipo de sucursal o un servidor de sucursal con la supervivencia</span><span class="sxs-lookup"><span data-stu-id="cb67b-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-216">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="cb67b-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="cb67b-217">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-217">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-218">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-219">Ruta de reserva para la transferencia de medios A/V entre usuarios internos y externos, equipo de sucursal con la supervivencia o servidor de sucursal con la supervivencia, si no se puede establecer la comunicación UDP, se usa TCP para la transferencia de archivos y el uso compartido de escritorio</span><span class="sxs-lookup"><span data-stu-id="cb67b-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="cb67b-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="cb67b-221">Cualquiera (puede definirse como la dirección IP del servidor front-end o el grupo que contiene el almacén de administración central)</span><span class="sxs-lookup"><span data-stu-id="cb67b-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="cb67b-222">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-223">Replicación de los cambios del almacén de administración central al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="cb67b-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="cb67b-225">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-225">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-226">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-227">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="cb67b-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="cb67b-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="cb67b-229">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-229">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-230">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-231">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="cb67b-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="cb67b-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="cb67b-233">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-233">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-234">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="cb67b-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="cb67b-235">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="cb67b-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="cb67b-236">Resumen del firewall para la Federación</span><span class="sxs-lookup"><span data-stu-id="cb67b-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb67b-237">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="cb67b-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cb67b-238">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="cb67b-238">Source IP address</span></span></th>
<th><span data-ttu-id="cb67b-239">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="cb67b-239">Destination IP address</span></span></th>
<th><span data-ttu-id="cb67b-240">Notas</span><span class="sxs-lookup"><span data-stu-id="cb67b-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-241">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="cb67b-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cb67b-242">Dirección IP pública del servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="cb67b-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="cb67b-243">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-243">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-244">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="cb67b-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="cb67b-245">Resumen del firewall: conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="cb67b-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb67b-246">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="cb67b-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cb67b-247">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="cb67b-247">Source IP address</span></span></th>
<th><span data-ttu-id="cb67b-248">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="cb67b-248">Destination IP address</span></span></th>
<th><span data-ttu-id="cb67b-249">Notas</span><span class="sxs-lookup"><span data-stu-id="cb67b-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-250">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="cb67b-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cb67b-251">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="cb67b-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="cb67b-252">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-253">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="cb67b-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-254">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="cb67b-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cb67b-255">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-256">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="cb67b-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="cb67b-257">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="cb67b-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-258">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="cb67b-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="cb67b-259">Clientes</span><span class="sxs-lookup"><span data-stu-id="cb67b-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="cb67b-260">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-261">Tráfico SIP de cliente a servidor para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="cb67b-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-262">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="cb67b-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="cb67b-263">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-264">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="cb67b-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="cb67b-265">Se usa para sesiones de A/V con Windows Live Messenger si está configurada la conectividad de mensajería instantánea pública.</span><span class="sxs-lookup"><span data-stu-id="cb67b-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-266">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="cb67b-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="cb67b-267">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-268">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="cb67b-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="cb67b-269">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="cb67b-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="cb67b-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="cb67b-271">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="cb67b-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="cb67b-272">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="cb67b-273">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="cb67b-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="cb67b-274">Resumen de Firewall para el protocolo de presencia y mensajería extensible</span><span class="sxs-lookup"><span data-stu-id="cb67b-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb67b-275">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="cb67b-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cb67b-276">Origen (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="cb67b-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="cb67b-277">Destino (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="cb67b-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="cb67b-278">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb67b-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="cb67b-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="cb67b-280">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-280">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-281">Dirección IP de la interfaz de servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="cb67b-282">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="cb67b-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="cb67b-283">Permite la comunicación con el proxy XMPP del servidor perimetral de socios de XMPP</span><span class="sxs-lookup"><span data-stu-id="cb67b-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb67b-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="cb67b-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="cb67b-285">Dirección IP de la interfaz de servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="cb67b-286">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-286">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-287">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="cb67b-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="cb67b-288">Permite la comunicación desde el proxy XMPP del servidor perimetral a socios XMPP de Federación</span><span class="sxs-lookup"><span data-stu-id="cb67b-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb67b-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="cb67b-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="cb67b-290">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cb67b-290">Any</span></span></p></td>
<td><p><span data-ttu-id="cb67b-291">Cada IP de la interfaz del servidor perimetral interno</span><span class="sxs-lookup"><span data-stu-id="cb67b-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="cb67b-292">Tráfico de XMPP interno de la puerta de enlace XMPP en el servidor front-end o grupo front-end a la dirección IP interna del servidor perimetral o a la dirección IP interna de cada miembro del grupo perimetral</span><span class="sxs-lookup"><span data-stu-id="cb67b-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cb67b-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb67b-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

