---
title: 'Lync Server 2013: Resumen de puerto - Carga equilibrada DNS y HLB'
description: 'Lync Server 2013: Resumen de puertos: DNS y carga equilibrada de HLB.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - DNS and HLB load balanced
ms:assetid: b07c37e4-820e-46ee-a678-1da95d1b87af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205179(v=OCS.15)
ms:contentKeyID: 48185149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be2e8204e792fd9c4718cb9171e90784af2d0104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424341"
---
# <a name="port-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="832f1-103">Resumen de puerto - Carga equilibrada DNS y HLB en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="832f1-103">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="832f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="832f1-104">

<span> </span></span></span>

<span data-ttu-id="832f1-105">_**Última modificación del tema:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="832f1-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="832f1-106">Los requisitos del puerto de Firewall para un único Director son los puertos que se usan para establecer comunicación con el director desde la interfaz interna o la red interna del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="832f1-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="832f1-107">Microsoft Lync Server 2013 espera de forma predeterminada que los puertos HTTP/TCP 8080 y HTTPS/TCP 4443 se abran desde el proxy inverso al Director, así como el servidor front-end y el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="832f1-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="832f1-108">Además, debe haber comunicación del Protocolo de inicio de sesión (SIP) desde la interfaz interna del servidor perimetral al Director y al grupo de servidores front-end y front-end.</span><span class="sxs-lookup"><span data-stu-id="832f1-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="832f1-109">El protocolo SIP usa SIP/MTLS/TCP 5061 del servidor perimetral al grupo front-end y al servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="832f1-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="832f1-110">También se debe crear una regla que permita la comunicación SIP/MTLS/TCP 5061 desde el director, el grupo de servidores front-end y el servidor front-end a la interfaz interna del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="832f1-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="832f1-111">Puertos y protocolos de un solo Director para definiciones de Firewall</span><span class="sxs-lookup"><span data-stu-id="832f1-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="832f1-112">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="832f1-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="832f1-113">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="832f1-113">Source IP address</span></span></th>
<th><span data-ttu-id="832f1-114">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="832f1-114">Destination IP address</span></span></th>
<th><span data-ttu-id="832f1-115">Notas</span><span class="sxs-lookup"><span data-stu-id="832f1-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="832f1-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="832f1-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="832f1-117">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="832f1-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="832f1-118">Director VIP de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="832f1-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="832f1-119">Inicialmente recibido por el lado externo del proxy inverso, la comunicación se envía al Director HLB VIP y los servicios Web de servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="832f1-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="832f1-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="832f1-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="832f1-121">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="832f1-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="832f1-122">Director VIP de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="832f1-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="832f1-123">Inicialmente recibido por el lado externo del proxy inverso, la comunicación se envía al Director HLB VIP y los servicios Web de servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="832f1-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="832f1-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="832f1-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="832f1-125">Director</span><span class="sxs-lookup"><span data-stu-id="832f1-125">Director</span></span></p></td>
<td><p><span data-ttu-id="832f1-126">Grupo de servidores front-end o servidor front-end</span><span class="sxs-lookup"><span data-stu-id="832f1-126">Front End pool or Front End Server</span></span></p></td>
<td><p><span data-ttu-id="832f1-127">Comunicación entre servidores entre el director HLB VIP y el servidor front-end o front-end.</span><span class="sxs-lookup"><span data-stu-id="832f1-127">Inter-server communication between the Director HLB VIP and the Front End Server or Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="832f1-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="832f1-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="832f1-129">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="832f1-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="832f1-130">Director VIP de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="832f1-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="832f1-131">El director proporciona servicios web a clientes externos y internos.</span><span class="sxs-lookup"><span data-stu-id="832f1-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="832f1-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="832f1-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="832f1-133">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="832f1-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="832f1-134">Director VIP de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="832f1-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="832f1-135">El director proporciona servicios web a clientes externos y internos.</span><span class="sxs-lookup"><span data-stu-id="832f1-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="832f1-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="832f1-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="832f1-137">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="832f1-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="832f1-138">Director</span><span class="sxs-lookup"><span data-stu-id="832f1-138">Director</span></span></p></td>
<td><p><span data-ttu-id="832f1-139">Comunicación SIP desde el servidor perimetral al Director, así como a los servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="832f1-139">SIP communication from the Edge Server to the Director, as well as the Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="832f1-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="832f1-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="832f1-141">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="832f1-141">Any</span></span></p></td>
<td><p><span data-ttu-id="832f1-142">Director</span><span class="sxs-lookup"><span data-stu-id="832f1-142">Director</span></span></p></td>
<td><p><span data-ttu-id="832f1-143">Controlador de servicio de registro centralizado (ClsController.exe) o comandos del agente (ClsAgent.exe) y colección de registros</span><span class="sxs-lookup"><span data-stu-id="832f1-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="832f1-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="832f1-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="832f1-145">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="832f1-145">Any</span></span></p></td>
<td><p><span data-ttu-id="832f1-146">Director</span><span class="sxs-lookup"><span data-stu-id="832f1-146">Director</span></span></p></td>
<td><p><span data-ttu-id="832f1-147">Controlador de servicio de registro centralizado (ClsController.exe) o comandos del agente (ClsAgent.exe) y colección de registros</span><span class="sxs-lookup"><span data-stu-id="832f1-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="832f1-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="832f1-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="832f1-149">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="832f1-149">Any</span></span></p></td>
<td><p><span data-ttu-id="832f1-150">Director</span><span class="sxs-lookup"><span data-stu-id="832f1-150">Director</span></span></p></td>
<td><p><span data-ttu-id="832f1-151">Controlador de servicio de registro centralizado (ClsController.exe) o comandos del agente (ClsAgent.exe) y colección de registros</span><span class="sxs-lookup"><span data-stu-id="832f1-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="832f1-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="832f1-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

