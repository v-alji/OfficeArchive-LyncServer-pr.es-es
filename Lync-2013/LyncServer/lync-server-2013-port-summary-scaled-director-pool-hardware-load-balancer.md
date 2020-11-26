---
title: 'Lync Server 2013: Resumen de puerto - Grupo de director escalado, equilibrador de carga de hardware'
description: 'Lync Server 2013: Grupo de directores de nivel de Resumen de puerto, equilibrador de carga de hardware.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled Director pool, hardware load balancer
ms:assetid: 6ae2f4ac-5b64-4e45-8253-133308f5812d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204983(v=OCS.15)
ms:contentKeyID: 48184434
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10bfb3a3ad3a38b6cb0e46414bf22deecc71d7b5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442799"
---
# <a name="port-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="4ef2e-103">Resumen de puerto - Grupo de director escalado, equilibrador de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4ef2e-103">Port summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ef2e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ef2e-104">

<span> </span></span></span>

<span data-ttu-id="4ef2e-105">_**Última modificación del tema:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="4ef2e-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="4ef2e-106">Los requisitos de puerto de Firewall para un grupo de directores consisten en los puertos que se usan para establecer comunicación con el director desde la interfaz interna del servidor perimetral o la interfaz interna del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-106">Firewall port requirements for a Director pool consist of the ports that are used to establish communication with the Director from the internal interface of the Edge Server or internal-facing interface of the reverse proxy.</span></span> <span data-ttu-id="4ef2e-107">Microsoft Lync Server 2013 espera de forma predeterminada que los puertos HTTP/TCP 8080 y HTTPS/TCP 4443 se abran desde el proxy inverso al Director, así como el servidor front-end y el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="4ef2e-108">Además, debe haber comunicación del Protocolo de inicio de sesión (SIP) desde la interfaz interna del servidor perimetral al Director y al grupo de servidores front-end y front-end.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="4ef2e-109">El protocolo SIP usa SIP/MTLS/TCP 5061 del servidor perimetral al grupo front-end y al servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="4ef2e-110">También se debe crear una regla que permita la comunicación SIP/MTLS/TCP 5061 desde el director, el grupo de servidores front-end y el servidor front-end a la interfaz interna del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="4ef2e-111">Puertos y protocolos de directores para definiciones de Firewall</span><span class="sxs-lookup"><span data-stu-id="4ef2e-111">Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ef2e-112">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="4ef2e-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="4ef2e-113">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="4ef2e-113">Source IP address</span></span></th>
<th><span data-ttu-id="4ef2e-114">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="4ef2e-114">Destination IP address</span></span></th>
<th><span data-ttu-id="4ef2e-115">Notas</span><span class="sxs-lookup"><span data-stu-id="4ef2e-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ef2e-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="4ef2e-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-117">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="4ef2e-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-118">Director VIP de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="4ef2e-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-119">Inicialmente recibido por el lado externo del proxy inverso, la comunicación se envía al Director HLB VIP y los servicios Web de los servidores front-end</span><span class="sxs-lookup"><span data-stu-id="4ef2e-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ef2e-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="4ef2e-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-121">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="4ef2e-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-122">Director VIP de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="4ef2e-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-123">Inicialmente recibido por el lado externo del proxy inverso, la comunicación se envía al Director HLB VIP y los servicios Web de los servidores front-end</span><span class="sxs-lookup"><span data-stu-id="4ef2e-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ef2e-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="4ef2e-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-125">Director</span><span class="sxs-lookup"><span data-stu-id="4ef2e-125">Director</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-126">Servidor front-end o grupo front-end</span><span class="sxs-lookup"><span data-stu-id="4ef2e-126">Front End Server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-127">Comunicación entre servidores entre el director HLB VIP y los servidores front-end</span><span class="sxs-lookup"><span data-stu-id="4ef2e-127">Inter-server communication between the Director HLB VIP and the Front End Servers</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ef2e-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="4ef2e-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-129">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="4ef2e-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-130">Director VIP de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="4ef2e-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-131">El director proporciona servicios web a clientes externos y internos.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ef2e-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="4ef2e-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-133">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="4ef2e-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-134">Director VIP de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="4ef2e-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-135">El director proporciona servicios web a clientes externos y internos.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ef2e-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="4ef2e-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-137">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="4ef2e-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-138">Director VIP de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="4ef2e-138">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-139">Comunicación SIP desde el servidor perimetral al Director y a los servidores de aplicaciones para el usuario.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-139">SIP communication from the Edge Server to the Director, and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ef2e-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="4ef2e-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-141">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="4ef2e-141">Any</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-142">Director</span><span class="sxs-lookup"><span data-stu-id="4ef2e-142">Director</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-143">Controlador de servicio de registro centralizado (ClsController.exe) o comandos del agente (ClsAgent.exe) y colección de registros</span><span class="sxs-lookup"><span data-stu-id="4ef2e-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ef2e-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="4ef2e-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-145">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="4ef2e-145">Any</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-146">Director</span><span class="sxs-lookup"><span data-stu-id="4ef2e-146">Director</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-147">Controlador de servicio de registro centralizado (ClsController.exe) o comandos del agente (ClsAgent.exe) y colección de registros</span><span class="sxs-lookup"><span data-stu-id="4ef2e-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ef2e-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="4ef2e-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-149">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="4ef2e-149">Any</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-150">Director</span><span class="sxs-lookup"><span data-stu-id="4ef2e-150">Director</span></span></p></td>
<td><p><span data-ttu-id="4ef2e-151">Controlador de servicio de registro centralizado (ClsController.exe) o comandos del agente (ClsAgent.exe) y colección de registros</span><span class="sxs-lookup"><span data-stu-id="4ef2e-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4ef2e-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ef2e-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

