---
title: Resumen de puerto - Servidor perimetral consolidado ampliado con equilibradores de carga de hardware
description: 'Resumen de puertos: borde consolidado a escala con equilibradores de carga de hardware.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge with hardware load balancers
ms:assetid: 91213b1e-f875-464b-83e8-fe3a351595a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398739(v=OCS.15)
ms:contentKeyID: 48184841
ms.date: 04/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a03acb3644d83669bcf0065ebb20c526ef5fa32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424319"
---
# <a name="port-summary---scaled-consolidated-edge-with-hardware-load-balancers-in-lync-server-2013"></a><span data-ttu-id="f8a92-103">Resumen de puerto - Servidor perimetral consolidado ampliado con equilibradores de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8a92-103">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8a92-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8a92-104">

<span> </span></span></span>

<span data-ttu-id="f8a92-105">_**Última modificación del tema:** 2015-04-27_</span><span class="sxs-lookup"><span data-stu-id="f8a92-105">_**Topic Last Modified:** 2015-04-27_</span></span>

<span data-ttu-id="f8a92-106">La funcionalidad del servidor de Lync Server 2013, que se describe en esta arquitectura de escenario, es muy similar a la que se ha implementado en Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="f8a92-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="f8a92-107">La adición más destacada es el puerto **5269 sobre** la entrada TCP para el protocolo de presencia y mensajería extensible (XMPP).</span><span class="sxs-lookup"><span data-stu-id="f8a92-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="f8a92-108">Lync Server 2013 implementa opcionalmente un proxy XMPP en el servidor perimetral o en el grupo perimetral y el servidor de puerta de enlace XMPP en el servidor front-end o en el grupo front-end.</span><span class="sxs-lookup"><span data-stu-id="f8a92-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="f8a92-109">Además de IPv4, el servidor EDGE ahora es compatible con IPv6.</span><span class="sxs-lookup"><span data-stu-id="f8a92-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="f8a92-110">Para mayor claridad, solo se usa IPv4 en los escenarios.</span><span class="sxs-lookup"><span data-stu-id="f8a92-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="f8a92-111">**Borde consolidado escalado mediante el equilibrio de carga de hardware**</span><span class="sxs-lookup"><span data-stu-id="f8a92-111">**Scaled Consolidated Edge using Hardware Load Balancing**</span></span>

<span data-ttu-id="f8a92-112">![Protocolos y puertos de la red perimetral de servidores perimetrales](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Protocolos y puertos de la red perimetral de servidores perimetrales")</span><span class="sxs-lookup"><span data-stu-id="f8a92-112">![Edge Server Perimeter Network ports and protocols](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Edge Server Perimeter Network ports and protocols")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="f8a92-113">Detalles de protocolo y puerto</span><span class="sxs-lookup"><span data-stu-id="f8a92-113">Port and Protocol Details</span></span>

<span data-ttu-id="f8a92-114">Le recomendamos que abra solo los puertos necesarios para admitir la funcionalidad para la que proporciona acceso externo.</span><span class="sxs-lookup"><span data-stu-id="f8a92-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="f8a92-115">Para que el acceso remoto funcione para cualquier servicio perimetral, es obligatorio que el tráfico SIP pueda fluir de forma bidireccional tal y como se muestra en la cifra de tráfico entrante o saliente.</span><span class="sxs-lookup"><span data-stu-id="f8a92-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="f8a92-116">En concreto, los mensajes SIP a y desde el servicio perimetral de acceso participan en la mensajería instantánea (mi), presencia, conferencias web, audio/vídeo (A/V) y Federación.</span><span class="sxs-lookup"><span data-stu-id="f8a92-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="f8a92-117">Resumen del firewall para el perímetro consolidado con escala, equilibrio de carga de hardware: interfaz externa-nodo 1 y nodo 2 (ejemplo)</span><span class="sxs-lookup"><span data-stu-id="f8a92-117">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8a92-118">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="f8a92-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="f8a92-119">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="f8a92-119">Source IP address</span></span></th>
<th><span data-ttu-id="f8a92-120">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="f8a92-120">Destination IP address</span></span></th>
<th><span data-ttu-id="f8a92-121">Notas</span><span class="sxs-lookup"><span data-stu-id="f8a92-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-122">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="f8a92-122">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="f8a92-123">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-123">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-124">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-124">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-125">Comprobación y recuperación de CRL o revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="f8a92-125">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-126">Acceso/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="f8a92-126">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="f8a92-127">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-128">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-128">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-129">Consulta DNS a través de TCP</span><span class="sxs-lookup"><span data-stu-id="f8a92-129">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-130">Acceso/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="f8a92-130">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="f8a92-131">Dirección IP pública del servicio perimetral de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-132">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-132">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-133">Consulta DNS a través de UDP</span><span class="sxs-lookup"><span data-stu-id="f8a92-133">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-134">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="f8a92-134">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="f8a92-135">Dirección IP del servicio Edge del servidor perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="f8a92-135">Edge Server A/V Edge service IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-136">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-136">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-137">Necesario para la Federación con socios que ejecutan Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 y Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f8a92-137">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-138">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="f8a92-138">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="f8a92-139">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-139">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-140">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-140">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-141">Solo es necesario para la Federación con socios que ejecutan Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="f8a92-141">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-142">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="f8a92-142">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="f8a92-143">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-143">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-144">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-144">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-145">Necesario solo para la Federación con socios que ejecutan Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="f8a92-145">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-146">A/V/RTP/UDP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="f8a92-146">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="f8a92-147">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-147">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-148">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-148">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-149">Necesario solo para la Federación con socios que ejecutan Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="f8a92-149">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-150">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="f8a92-150">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="f8a92-151">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-151">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-152">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-152">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-153">3478 saliente se usa para determinar la versión del servidor perimetral con el que se comunica Lync Server y también para el tráfico de multimedia de un servidor perimetral a un servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="f8a92-153">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="f8a92-154">Necesario para la Federación con Lync Server 2010, Windows Live Messenger y Office Communications Server 2007 R2, y también si se han implementado varias agrupaciones perimetrales dentro de una empresa.</span><span class="sxs-lookup"><span data-stu-id="f8a92-154">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-155">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="f8a92-155">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="f8a92-156">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-156">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-157">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-157">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-158">STUN/TURN negociación de candidatos a través de UDP/3478</span><span class="sxs-lookup"><span data-stu-id="f8a92-158">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-159">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-159">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="f8a92-160">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-160">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-161">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-161">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-162">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-162">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-163">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-163">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="f8a92-164">Dirección IP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-165">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-165">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-166">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-166">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-node-1-and-node-2"></a><span data-ttu-id="f8a92-167">Resumen del firewall para el perímetro consolidado con escala, equilibrio de carga de hardware: nodo 1 de interfaz interna y nodo 2</span><span class="sxs-lookup"><span data-stu-id="f8a92-167">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Node 1 and Node 2</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8a92-168">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="f8a92-168">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="f8a92-169">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="f8a92-169">Source IP address</span></span></th>
<th><span data-ttu-id="f8a92-170">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="f8a92-170">Destination IP address</span></span></th>
<th><span data-ttu-id="f8a92-171">Notas</span><span class="sxs-lookup"><span data-stu-id="f8a92-171">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-172">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="f8a92-172">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="f8a92-173">Cualquiera (se puede definir como la dirección del servidor front-end o la dirección IP virtual del grupo de servidores front-end que ejecuta el servicio de puerta de enlace XMPP)</span><span class="sxs-lookup"><span data-stu-id="f8a92-173">Any (can be defined as Front End Server address, or Front End pool virtual IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-174">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-174">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-175">Tráfico XMPP saliente del servicio de puerta de enlace XMPP que se ejecuta en el servidor front-end o grupo front-end</span><span class="sxs-lookup"><span data-stu-id="f8a92-175">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-176">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="f8a92-176">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="f8a92-177">Cualquiera (puede definirse como la IP o el grupo de servidores front-end Server que contiene el almacén central de administración)</span><span class="sxs-lookup"><span data-stu-id="f8a92-177">Any (can be defined as the Front End Server server IP or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-178">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-178">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-179">Replicación de los cambios del almacén de administración central al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-179">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-180">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="f8a92-180">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="f8a92-181">Any (se puede definir como IP de Director, IP de servidor front end o IP virtual de grupo)</span><span class="sxs-lookup"><span data-stu-id="f8a92-181">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-182">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-182">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-183">Tráfico de conferencias web de la implementación interna a la interfaz de servidor perimetral interno</span><span class="sxs-lookup"><span data-stu-id="f8a92-183">Web conferencing traffic from Internal deployment to Internal Edge Server interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-184">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="f8a92-184">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="f8a92-185">Any (se puede definir como IP de Director, IP de servidor front end o IP virtual de grupo)</span><span class="sxs-lookup"><span data-stu-id="f8a92-185">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-186">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-186">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-187">Ruta preferida para la transferencia de medios A/V entre usuarios internos y externos, un equipo de sucursal o un servidor de sucursal con la supervivencia</span><span class="sxs-lookup"><span data-stu-id="f8a92-187">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-188">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-188">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="f8a92-189">Any (se puede definir como IP de Director, IP de servidor front end o IP virtual de grupo)</span><span class="sxs-lookup"><span data-stu-id="f8a92-189">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-190">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-190">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-191">Ruta de reserva para la transferencia de medios A/V entre usuarios internos y externos, equipo de sucursal con la supervivencia o servidor de sucursal con la supervivencia, si no se puede establecer la comunicación UDP, se usa TCP para la transferencia de archivos y el uso compartido de escritorio</span><span class="sxs-lookup"><span data-stu-id="f8a92-191">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-192">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="f8a92-192">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="f8a92-193">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-193">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-194">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-195">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="f8a92-195">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-196">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="f8a92-196">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="f8a92-197">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-197">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-198">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-199">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="f8a92-199">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-200">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="f8a92-200">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="f8a92-201">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-201">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-202">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-203">Controlador de servicio de registro centralizado con el shell de administración de Lync Server y los cmdlets del servicio de registro centralizado, la línea de comandos de ClsController (ClsController.exe) o los comandos del agente (ClsAgent.exe) y la colección de registros</span><span class="sxs-lookup"><span data-stu-id="f8a92-203">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f8a92-204">Los equilibradores de carga de hardware tienen requisitos específicos cuando se implementan para proporcionar disponibilidad y equilibrio de carga para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f8a92-204">Hardware load balancers have specific requirements when deployed to provide availability and load balancing for Lync Server.</span></span> <span data-ttu-id="f8a92-205">Los requisitos se definen en la siguiente ilustración y tablas.</span><span class="sxs-lookup"><span data-stu-id="f8a92-205">The requirements are defined in the following figure and tables.</span></span> <span data-ttu-id="f8a92-206">Los proveedores de terceros pueden usar terminología diferente para los requisitos que se definen aquí.</span><span class="sxs-lookup"><span data-stu-id="f8a92-206">Third party vendors may use different terminology for the requirements defined here.</span></span> <span data-ttu-id="f8a92-207">Será necesario asignar los requisitos de Lync Server a las características y opciones de configuración proporcionadas por el proveedor de equilibrador de carga del hardware.</span><span class="sxs-lookup"><span data-stu-id="f8a92-207">It will be necessary to map the requirements of Lync Server to the features and configuration options provided by your hardware load balancer vendor.</span></span>

<span data-ttu-id="f8a92-208">Al configurar equilibradores de carga de hardware, tenga en cuenta los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="f8a92-208">When configuring hardware load balancers, consider the following requirements:</span></span>

  - <span data-ttu-id="f8a92-209">La traducción de direcciones de red de origen (SNAT) se puede configurar en el equilibrio de carga de hardware (HLB) para el servicio perimetral de Access y el servicio perimetral de conferencia Web</span><span class="sxs-lookup"><span data-stu-id="f8a92-209">Source Network Address Translation (SNAT) can be configured on the hardware load balancer (HLB) for Access Edge service and Web Conferencing Edge service</span></span>

  - <span data-ttu-id="f8a92-210">SNAT no se puede configurar en el servicio perimetral A/V: el servicio perimetral A/V debe responder con la dirección real del servidor, no con la IP virtual de HLB (VIP), para un recorrido simple de UDP sobre NAT (STUN)/Traversal mediante la opción de retransmisión NAT (TURN)/Federation (FAPAGAR) para funcionar correctamente</span><span class="sxs-lookup"><span data-stu-id="f8a92-210">SNAT cannot be configured on the A/V Edge service– the A/V Edge service must respond with the real server address, not the HLB virtual IP (VIP), for simple traversal of UDP over NAT (STUN)/traversal using relay NAT (TURN)/federation TURN (FTURN) to work properly</span></span>
    
      - <span data-ttu-id="f8a92-211">Si el cliente envía una solicitud al HLB, la respuesta debe devolverse a la dirección VIP de HLB.</span><span class="sxs-lookup"><span data-stu-id="f8a92-211">If the client sends a request to the HLB, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="f8a92-212">Si el cliente envía una solicitud al borde, la respuesta debe volver de la IP de borde.</span><span class="sxs-lookup"><span data-stu-id="f8a92-212">If the client sends a request to the Edge, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="f8a92-213">Las direcciones IP públicas se usan en cada interfaz de servidor y en los VIP de la HLB, y los requisitos de dirección IP pública son N + 1, donde hay una dirección IP pública para cada interfaz de servidor real y otra para cada VIP de HLB.</span><span class="sxs-lookup"><span data-stu-id="f8a92-213">Public IP addresses are used on each server interface and on the VIPs of the HLB, and your public IP address requirements are N+1, where there is a public IP address for each real server interface and one for each HLB VIP.</span></span> <span data-ttu-id="f8a92-214">Cuando tiene dos servidores perimetrales en el grupo, se producen 9 direcciones IP públicas, donde 3 se usan para los VIP de HLB y una para cada interfaz de servidor perimetral (un total de seis para los servidores)</span><span class="sxs-lookup"><span data-stu-id="f8a92-214">Where you have 2 Edge servers in the pool, this results in 9 public IP addresses, where 3 are used for the HLB VIPs, and one for each Edge server interface (a total of six for the servers)</span></span>

  - <span data-ttu-id="f8a92-215">Para el servicio perimetral de Access y el servicio perimetral de conferencias web, (y uso de NAT en la HLB) el cliente se conecta a la dirección VIP, la VIP cambia la dirección IP de origen del cliente a su propia dirección IP.</span><span class="sxs-lookup"><span data-stu-id="f8a92-215">For the Access Edge service and Web Conferencing Edge service, (and using NAT on the HLB) the client contacts the VIP, the VIP changes the source IP address from the client to its own IP address.</span></span> <span data-ttu-id="f8a92-216">La interfaz de servidor dirige la dirección de remite a la dirección VIP, la VIP cambia la dirección de origen de la dirección IP de la interfaz del servidor y envía el paquete al cliente.</span><span class="sxs-lookup"><span data-stu-id="f8a92-216">The server interface addresses the return address to the VIP, the VIP changes the source address from the server interface IP address and sends the packet to the client</span></span>

  - <span data-ttu-id="f8a92-217">Para el servicio perimetral A/V, la dirección VIP no debe cambiar la dirección IP de origen, y la dirección del servidor real se devuelve directamente al cliente; no puede configurar NAT en el HLB para el tráfico audiovisual</span><span class="sxs-lookup"><span data-stu-id="f8a92-217">For the A/V Edge service, the VIP must NOT change the source IP address, and the real server address is returned to the client directly – you cannot configure NAT on the HLB for AV traffic</span></span>
    
      - <span data-ttu-id="f8a92-218">Si el cliente envía una solicitud a la dirección VIP de HLB, la respuesta debe regresar a la HLB VIP</span><span class="sxs-lookup"><span data-stu-id="f8a92-218">If the client sends a request to the HLB VIP, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="f8a92-219">Si el cliente envía una solicitud a la IP de borde, la respuesta debe devolverse a la IP de borde.</span><span class="sxs-lookup"><span data-stu-id="f8a92-219">If the client sends a request to the Edge IP, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="f8a92-220">Para AV, el firewall externo retendrá la dirección IP pública real del servidor para todos los paquetes</span><span class="sxs-lookup"><span data-stu-id="f8a92-220">For AV, the external firewall will retain the real server public IP address for all packets</span></span>

  - <span data-ttu-id="f8a92-221">Una vez que se haya establecido, la comunicación entre el cliente y el servicio perimetral a/V es al servidor real, no a la HLB</span><span class="sxs-lookup"><span data-stu-id="f8a92-221">Once established, client to A/V Edge service communication is to the real server, not the HLB</span></span>

  - <span data-ttu-id="f8a92-222">El borde interno de los servidores internos y los clientes debe enrutarse y se establecen rutas persistentes para todas las redes internas que hospedan servidores o clientes.</span><span class="sxs-lookup"><span data-stu-id="f8a92-222">Internal edge to internal servers and clients must be routed, and persistent routes are set for all internal networks that host servers or clients</span></span>

  - <span data-ttu-id="f8a92-223">La dirección VIP del servicio perimetral de acceso de HLB actuará como puerta de enlace predeterminada para cada interfaz de servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="f8a92-223">The HLB Access Edge service VIP will act as the default gateway for each Edge server interface</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="f8a92-224">Para obtener más información sobre el planeamiento y la funcionalidad de NAT, consulte <A href="lync-server-2013-hardware-load-balancer-requirements.md">requisitos del equilibrador de carga de hardware para Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f8a92-224">For further information on NAT planning and functionality, please refer to <A href="lync-server-2013-hardware-load-balancer-requirements.md">Hardware load balancer requirements for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="f8a92-225">![Detalles de puertos y protocolos de servidores perimetrales](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Detalles de puertos y protocolos de servidores perimetrales")</span><span class="sxs-lookup"><span data-stu-id="f8a92-225">![Edge Server ports and protocols details](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Edge Server ports and protocols details")</span></span>

### <a name="external-port-settings-required-for-scaled-consolidated-edge-hardware-load-balanced-external-interface-virtual-ips"></a><span data-ttu-id="f8a92-226">Configuración de puertos externos necesaria para el perímetro consolidado con escala, equilibrio de carga de hardware: IPs virtual de interfaz externa</span><span class="sxs-lookup"><span data-stu-id="f8a92-226">External Port Settings Required for Scaled Consolidated Edge, Hardware Load Balanced: External Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8a92-227">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="f8a92-227">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="f8a92-228">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="f8a92-228">Source IP address</span></span></th>
<th><span data-ttu-id="f8a92-229">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="f8a92-229">Destination IP address</span></span></th>
<th><span data-ttu-id="f8a92-230">Notas</span><span class="sxs-lookup"><span data-stu-id="f8a92-230">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-231">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="f8a92-231">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="f8a92-232">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-232">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-233">Servicio de proxy XMPP (comparte dirección IP con servicio perimetral de acceso)</span><span class="sxs-lookup"><span data-stu-id="f8a92-233">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-234">El servicio Proxy XMPP acepta el tráfico de los contactos XMPP en las federaciones XMPP definidas</span><span class="sxs-lookup"><span data-stu-id="f8a92-234">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-235">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="f8a92-235">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="f8a92-236">Servicio de proxy XMPP (comparte dirección IP con servicio perimetral de acceso)</span><span class="sxs-lookup"><span data-stu-id="f8a92-236">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-237">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-237">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-238">El servicio Proxy XMPP envía tráfico a los contactos XMPP en las federaciones XMPP definidas</span><span class="sxs-lookup"><span data-stu-id="f8a92-238">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-239">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-239">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="f8a92-240">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-240">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-241">Dirección VIP pública de servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="f8a92-241">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-242">Tráfico SIP de cliente a servidor para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="f8a92-242">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-243">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="f8a92-243">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="f8a92-244">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-244">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-245">Dirección VIP pública de servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="f8a92-245">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-246">Señalización SIP, Federación y conectividad de mensajería instantánea pública con SIP</span><span class="sxs-lookup"><span data-stu-id="f8a92-246">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-247">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="f8a92-247">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="f8a92-248">Dirección VIP pública de servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="f8a92-248">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-249">Socio federado</span><span class="sxs-lookup"><span data-stu-id="f8a92-249">Federated partner</span></span></p></td>
<td><p><span data-ttu-id="f8a92-250">Señalización SIP, Federación y conectividad de mensajería instantánea pública con SIP</span><span class="sxs-lookup"><span data-stu-id="f8a92-250">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-251">Conferencias web/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-251">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="f8a92-252">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-252">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-253">Dirección VIP pública del servicio perimetral de conferencias web del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-253">Edge Server Web Conferencing Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-254">Medios de conferencia Web</span><span class="sxs-lookup"><span data-stu-id="f8a92-254">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-255">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="f8a92-255">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="f8a92-256">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-256">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-257">Dirección VIP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-257">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-258">STUN/TURN negociación de candidatos a través de UDP/3478</span><span class="sxs-lookup"><span data-stu-id="f8a92-258">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-259">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-259">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="f8a92-260">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-260">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-261">Dirección VIP pública del servicio perimetral A/V del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-261">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="f8a92-262">STUN/TURN negociación de candidatos por TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-262">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-virtual-ips"></a><span data-ttu-id="f8a92-263">Resumen del firewall para la tecnología perimetral consolidada con escala, equilibrio de carga de hardware: interfaz IP virtual interna</span><span class="sxs-lookup"><span data-stu-id="f8a92-263">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8a92-264">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="f8a92-264">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="f8a92-265">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="f8a92-265">Source IP address</span></span></th>
<th><span data-ttu-id="f8a92-266">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="f8a92-266">Destination IP address</span></span></th>
<th><span data-ttu-id="f8a92-267">Notas</span><span class="sxs-lookup"><span data-stu-id="f8a92-267">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-268">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="f8a92-268">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="f8a92-269">Cualquiera (se puede definir como director, dirección IP virtual del grupo de directores, servidor front-end o dirección IP virtual del grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="f8a92-269">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-270">Interfaz VIP interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-270">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-271">Tráfico SIP saliente (de Director, grupo de directores, dirección IP virtual, servidor front-end o dirección IP virtual del grupo de servidores front-end) hasta VIP interna</span><span class="sxs-lookup"><span data-stu-id="f8a92-271">Outbound SIP traffic (from Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)to Internal Edge VIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-272">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="f8a92-272">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="f8a92-273">Interfaz VIP interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-273">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-274">Cualquiera (se puede definir como director, dirección IP virtual del grupo de directores, servidor front-end o dirección IP virtual del grupo de servidores front-end)</span><span class="sxs-lookup"><span data-stu-id="f8a92-274">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-275">Tráfico SIP entrante (Director, grupo de directores, dirección IP virtual, servidor front-end o dirección IP virtual del grupo de servidores front-end) de la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f8a92-275">Inbound SIP traffic (to Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-276">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="f8a92-276">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="f8a92-277">Cualquiera (se puede definir como la dirección IP del servidor front-end, la dirección IP del grupo de servidores front-end o cualquier otro equipo de sucursal o servidor de sucursal con la supervivencia que use este servidor perimetral)</span><span class="sxs-lookup"><span data-stu-id="f8a92-277">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="f8a92-278">Interfaz VIP interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-278">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-279">Autenticación de usuarios A/V (servicio de autenticación A/V) desde el servidor front-end o la dirección IP del grupo de servidores front-end o cualquier otro dispositivo de sucursal que sea reviviente o con el servidor de sucursal</span><span class="sxs-lookup"><span data-stu-id="f8a92-279">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-280">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="f8a92-280">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="f8a92-281">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-281">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-282">Interfaz VIP interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-282">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-283">Ruta preferida para la transferencia de medios A/V entre usuarios internos y externos</span><span class="sxs-lookup"><span data-stu-id="f8a92-283">Preferred path for A/V media transfer between internal and external users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a92-284">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-284">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="f8a92-285">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-285">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-286">Interfaz VIP interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-286">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-287">Ruta de reserva para la transferencia de medios A/V entre usuarios internos y externos si no se puede establecer la comunicación UDP, se usa TCP para la transferencia de archivos y el uso compartido de escritorio</span><span class="sxs-lookup"><span data-stu-id="f8a92-287">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a92-288">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="f8a92-288">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="f8a92-289">Interfaz VIP interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="f8a92-289">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="f8a92-290">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f8a92-290">Any</span></span></p></td>
<td><p><span data-ttu-id="f8a92-291">Ruta de reserva para la transferencia de medios A/V entre usuarios internos y externos si no se puede establecer la comunicación UDP, se usa TCP para la transferencia de archivos y el uso compartido de escritorio</span><span class="sxs-lookup"><span data-stu-id="f8a92-291">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f8a92-292">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8a92-292">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

