---
title: Resumen de puerto - Perímetro consolidado de equipo único con direcciones IP públicas
description: 'Resumen de puertos: un solo borde consolidado con direcciones IP públicas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with public IP addresses
ms:assetid: 28407acc-8b92-4f78-875c-fd6b4323b602
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204756(v=OCS.15)
ms:contentKeyID: 48183685
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82ab2d89404fb174994d8e5b798f64bb68768326
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424261"
---
# <a name="port-summary---single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="32982-103">Resumen de puerto - Perímetro consolidado de equipo único con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32982-103">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32982-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32982-104">

<span> </span></span></span>

<span data-ttu-id="32982-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="32982-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="32982-106">La funcionalidad del servidor de Lync Server 2013, que se describe en esta arquitectura de escenario, es muy similar a la que se ha implementado en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="32982-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="32982-107">La adición más destacada es el puerto **5269 sobre** la entrada TCP para el protocolo de presencia y mensajería extensible (XMPP).</span><span class="sxs-lookup"><span data-stu-id="32982-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="32982-108">Lync Server 2013 implementa opcionalmente un proxy XMPP en el servidor perimetral o en el grupo perimetral y el servidor de puerta de enlace XMPP en el servidor front-end o en el grupo front-end.</span><span class="sxs-lookup"><span data-stu-id="32982-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span> <span data-ttu-id="32982-109">La información de planeación del proxy inverso y la Federación se encuentra en [escenarios de inverso de proxy en Lync server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) , así como en la [planeación de la Federación de SIP, la Federación de XMPP y la mensajería instantánea pública en las secciones de Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="32982-109">Planning information for the reverse proxy and federation are found in [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) and [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) sections, respectively.</span></span>

<span data-ttu-id="32982-110">Además de IPv4, el servidor EDGE ahora es compatible con IPv6.</span><span class="sxs-lookup"><span data-stu-id="32982-110">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="32982-111">Para mayor claridad, solo se usa IPv4 en los escenarios.</span><span class="sxs-lookup"><span data-stu-id="32982-111">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="32982-112">**Red perimetral empresarial para un solo borde consolidado con direccionamiento IP público**</span><span class="sxs-lookup"><span data-stu-id="32982-112">**Enterprise perimeter network for single consolidated edge with public IP addressing**</span></span>

<span data-ttu-id="32982-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="32982-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="32982-114">Detalles de protocolo y puerto</span><span class="sxs-lookup"><span data-stu-id="32982-114">Port and Protocol Details</span></span>

<span data-ttu-id="32982-115">Le recomendamos que abra solo los puertos necesarios para admitir la funcionalidad para la que proporciona acceso externo.</span><span class="sxs-lookup"><span data-stu-id="32982-115">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="32982-116">Para que el acceso remoto funcione para cualquier servicio perimetral, es obligatorio que el tráfico SIP pueda fluir de forma bidireccional tal y como se muestra en la cifra de tráfico entrante o saliente.</span><span class="sxs-lookup"><span data-stu-id="32982-116">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bidirectionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="32982-117">En concreto, los mensajes SIP a y desde el servicio perimetral de acceso participan en la mensajería instantánea (mi), presencia, conferencias web, audio/vídeo (A/V) y Federación.</span><span class="sxs-lookup"><span data-stu-id="32982-117">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-external-interface"></a><span data-ttu-id="32982-118">Resumen del firewall para un solo borde consolidado con direcciones IP públicas: interfaz externa</span><span class="sxs-lookup"><span data-stu-id="32982-118">Firewall Summary for Single Consolidated Edge with Public IP Addresses: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32982-119">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="32982-119">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="32982-120">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="32982-120">Source IP address</span></span></th>
<th><span data-ttu-id="32982-121">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="32982-121">Destination IP address</span></span></th>
<th><span data-ttu-id="32982-122">Notas</span><span class="sxs-lookup"><span data-stu-id="32982-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32982-123">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="32982-123">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="32982-124">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-124">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-125">Servicio de proxy XMPP (comparte dirección IP con servicio perimetral de acceso)</span><span class="sxs-lookup"><span data-stu-id="32982-125">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="32982-126">El servicio Proxy XMPP acepta el tráfico de los contactos XMPP en las federaciones XMPP definidas</span><span class="sxs-lookup"><span data-stu-id="32982-126">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-127">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="32982-127">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="32982-128">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-128">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-129">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-129">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-130">Comprobación y recuperación de CRL o revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="32982-130">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-131">Acceso/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="32982-131">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="32982-132">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-132">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-133">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-133">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-134">Consulta DNS a través de TCP</span><span class="sxs-lookup"><span data-stu-id="32982-134">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-135">Acceso/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="32982-135">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="32982-136">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-136">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-137">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-137">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-138">Consulta DNS a través de UDP</span><span class="sxs-lookup"><span data-stu-id="32982-138">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-139">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="32982-139">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="32982-140">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-140">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-141">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-141">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-142">Tráfico SIP de cliente a servidor para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="32982-142">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-143">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="32982-143">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="32982-144">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-144">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-145">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-145">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-146">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="32982-146">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-147">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="32982-147">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="32982-148">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-148">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-149">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-149">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-150">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="32982-150">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-151">Conferencias web/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="32982-151">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="32982-152">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-152">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-153">Dirección IP pública del servicio perimetral de conferencias web del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-153">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-154">Medios de conferencia Web</span><span class="sxs-lookup"><span data-stu-id="32982-154">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-155">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="32982-155">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="32982-156">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-156">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-157">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-157">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-158">Necesario para la Federación con socios que ejecutan Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 y Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="32982-158">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-159">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="32982-159">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="32982-160">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-160">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-161">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-161">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-162">Necesario solo para la Federación con socios que ejecutan Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="32982-162">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-163">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="32982-163">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="32982-164">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-164">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-165">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-165">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-166">Solo es necesario para la Federación con socios que ejecutan Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="32982-166">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-167">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="32982-167">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="32982-168">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-168">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-169">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-169">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-170">Solo es necesario para la Federación con socios que ejecutan Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="32982-170">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-171">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="32982-171">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="32982-172">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-172">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-173">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-173">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-174">3478 saliente se usa para determinar la versión del servidor perimetral con el que se comunica Lync Server y también para el tráfico de multimedia de un servidor perimetral a un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="32982-174">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="32982-175">Necesario para la Federación con Lync Server 2010, Windows Live Messenger y Office Communications Server 2007 R2, y también si se han implementado varias agrupaciones perimetrales dentro de una empresa.</span><span class="sxs-lookup"><span data-stu-id="32982-175">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-176">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="32982-176">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="32982-177">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-177">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-178">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-178">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-179">STUN/TURN negociación de candidatos a través de UDP/3478</span><span class="sxs-lookup"><span data-stu-id="32982-179">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-180">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="32982-180">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="32982-181">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-181">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-182">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-182">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-183">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="32982-183">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-184">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="32982-184">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="32982-185">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-185">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-186">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-186">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-187">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="32982-187">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-internal-interface"></a><span data-ttu-id="32982-188">Resumen del firewall para un solo borde consolidado con direcciones IP públicas: interfaz interna</span><span class="sxs-lookup"><span data-stu-id="32982-188">Firewall Summary for Single Consolidated Edge with Public IP Addresses: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32982-189">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="32982-189">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="32982-190">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="32982-190">Source IP address</span></span></th>
<th><span data-ttu-id="32982-191">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="32982-191">Destination IP address</span></span></th>
<th><span data-ttu-id="32982-192">Comentarios</span><span class="sxs-lookup"><span data-stu-id="32982-192">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32982-193">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="32982-193">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="32982-194">Cualquiera (puede definirse como IP de servidor Standard Edition, dirección IP del servidor Standard Edition o dirección IP del grupo de servidores que ejecuta el servicio de puerta de enlace XMPP)</span><span class="sxs-lookup"><span data-stu-id="32982-194">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="32982-195">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-195">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-196">Tráfico XMPP saliente del servicio de puerta de enlace XMPP que se ejecuta en el servidor front-end o grupo front-end</span><span class="sxs-lookup"><span data-stu-id="32982-196">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-197">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="32982-197">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="32982-198">Cualquiera (se puede definir como director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="32982-198">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="32982-199">IP del servidor perimetral o grupo que contiene la interfaz interna</span><span class="sxs-lookup"><span data-stu-id="32982-199">Edge Server IP, or pool that holds the internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-200">Tráfico SIP saliente (del Director, la dirección IP del grupo de directores, el servidor front-end o la dirección IP del grupo de servidores front-end) a la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-200">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-201">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="32982-201">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="32982-202">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-203">Cualquiera (se puede definir como director, dirección IP del grupo de directores, servidor front-end o dirección de grupo frontal)</span><span class="sxs-lookup"><span data-stu-id="32982-203">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool address)</span></span></p></td>
<td><p><span data-ttu-id="32982-204">Tráfico SIP entrante (Director, dirección IP del grupo de directores, servidor front-end o dirección IP del grupo front-end) de la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-204">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-205">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="32982-205">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="32982-206">Cualquiera (se puede definir como la dirección IP del servidor front-end o cada dirección IP del servidor front-end en un grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="32982-206">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="32982-207">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-207">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-208">Tráfico de conferencias web desde el servidor front-end o cada servidor front-end si se está en un grupo, a la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-208">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-209">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="32982-209">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="32982-210">Cualquiera (se puede definir como la dirección IP del servidor front-end, la dirección IP del grupo de servidores front-end o cualquier otro equipo de sucursal o servidor de sucursal con la supervivencia que use este servidor perimetral)</span><span class="sxs-lookup"><span data-stu-id="32982-210">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="32982-211">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-211">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-212">Autenticación de usuarios A/V (servicio de autenticación A/V) desde el servidor front-end o la dirección IP del grupo de servidores front-end o cualquier otro dispositivo de sucursal que sea reviviente o con el servidor de sucursal</span><span class="sxs-lookup"><span data-stu-id="32982-212">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-213">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="32982-213">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="32982-214">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-214">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-215">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-215">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-216">Ruta preferida para la transferencia de medios A/V entre usuarios internos y externos, un equipo de sucursal o un servidor de sucursal con la supervivencia</span><span class="sxs-lookup"><span data-stu-id="32982-216">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-217">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="32982-217">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="32982-218">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-218">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-219">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-219">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-220">Ruta de reserva para la transferencia de medios A/V entre usuarios internos y externos, equipo de sucursal con la supervivencia o servidor de sucursal con la supervivencia, si no se puede establecer la comunicación UDP, se usa TCP para la transferencia de archivos y el uso compartido de escritorio</span><span class="sxs-lookup"><span data-stu-id="32982-220">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-221">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="32982-221">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="32982-222">Cualquiera (puede definirse como la dirección IP del servidor front-end o el grupo que contiene el almacén de administración central)</span><span class="sxs-lookup"><span data-stu-id="32982-222">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="32982-223">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-223">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-224">Replicación de los cambios del almacén de administración central al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-224">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-225">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="32982-225">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="32982-226">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-226">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-227">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-227">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-228">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="32982-228">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-229">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="32982-229">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="32982-230">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-230">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-231">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-231">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-232">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="32982-232">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-233">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="32982-233">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="32982-234">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-234">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-235">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="32982-235">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="32982-236">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="32982-236">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="32982-237">Resumen del firewall para la Federación</span><span class="sxs-lookup"><span data-stu-id="32982-237">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32982-238">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="32982-238">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="32982-239">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="32982-239">Source IP address</span></span></th>
<th><span data-ttu-id="32982-240">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="32982-240">Destination IP address</span></span></th>
<th><span data-ttu-id="32982-241">Notas</span><span class="sxs-lookup"><span data-stu-id="32982-241">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32982-242">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="32982-242">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="32982-243">Dirección IP pública del servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="32982-243">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-244">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-244">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-245">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="32982-245">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="32982-246">Resumen del firewall: conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="32982-246">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32982-247">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="32982-247">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="32982-248">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="32982-248">Source IP address</span></span></th>
<th><span data-ttu-id="32982-249">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="32982-249">Destination IP address</span></span></th>
<th><span data-ttu-id="32982-250">Notas</span><span class="sxs-lookup"><span data-stu-id="32982-250">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32982-251">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="32982-251">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="32982-252">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="32982-252">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="32982-253">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-253">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="32982-254">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="32982-254">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-255">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="32982-255">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="32982-256">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="32982-257">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="32982-257">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="32982-258">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="32982-258">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-259">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="32982-259">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="32982-260">Clientes</span><span class="sxs-lookup"><span data-stu-id="32982-260">Clients</span></span></p></td>
<td><p><span data-ttu-id="32982-261">Servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-261">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="32982-262">Tráfico SIP de cliente a servidor para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="32982-262">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-263">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="32982-263">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="32982-264">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-264">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="32982-265">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="32982-265">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="32982-266">Se usa para sesiones de A/V con Windows Live Messenger si está configurada la conectividad de mensajería instantánea pública.</span><span class="sxs-lookup"><span data-stu-id="32982-266">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-267">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="32982-267">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="32982-268">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-268">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="32982-269">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="32982-269">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="32982-270">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="32982-270">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-271">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="32982-271">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="32982-272">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="32982-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="32982-273">Servidor perimetral A/V servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-273">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="32982-274">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="32982-274">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="32982-275">Resumen de Firewall para el protocolo de presencia y mensajería extensible</span><span class="sxs-lookup"><span data-stu-id="32982-275">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32982-276">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="32982-276">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="32982-277">Origen (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="32982-277">Source (IP address)</span></span></th>
<th><span data-ttu-id="32982-278">Destino (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="32982-278">Destination (IP address)</span></span></th>
<th><span data-ttu-id="32982-279">Comentarios</span><span class="sxs-lookup"><span data-stu-id="32982-279">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32982-280">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="32982-280">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="32982-281">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-281">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-282">Dirección IP de la interfaz de servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-282">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-283">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="32982-283">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="32982-284">Permite la comunicación con el proxy XMPP del servidor perimetral de socios de XMPP</span><span class="sxs-lookup"><span data-stu-id="32982-284">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32982-285">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="32982-285">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="32982-286">Dirección IP de la interfaz de servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-286">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="32982-287">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-287">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-288">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="32982-288">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="32982-289">Permite la comunicación desde el proxy XMPP del servidor perimetral a socios XMPP de Federación</span><span class="sxs-lookup"><span data-stu-id="32982-289">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32982-290">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="32982-290">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="32982-291">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="32982-291">Any</span></span></p></td>
<td><p><span data-ttu-id="32982-292">Cada IP de la interfaz del servidor perimetral interno</span><span class="sxs-lookup"><span data-stu-id="32982-292">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="32982-293">Tráfico de XMPP interno de la puerta de enlace XMPP en el servidor front-end o grupo front-end a la dirección IP interna del servidor perimetral o a la dirección IP interna de cada miembro del grupo perimetral</span><span class="sxs-lookup"><span data-stu-id="32982-293">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="32982-294">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32982-294">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

