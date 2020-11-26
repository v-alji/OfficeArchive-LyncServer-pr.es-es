---
title: 'Lync Server 2013: Resumen del puerto - Director único'
description: 'Lync Server 2013: Resumen de puertos-un único Director.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single Director
ms:assetid: 079c1414-723f-4499-b7d4-a0d7121c1626
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204648(v=OCS.15)
ms:contentKeyID: 48183322
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a46e394121dbc7dd6158016d39511e9487cec1ff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436982"
---
# <a name="port-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="45c22-103">Resumen del puerto - Director único en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="45c22-103">Port summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45c22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45c22-104">

<span> </span></span></span>

<span data-ttu-id="45c22-105">_**Última modificación del tema:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="45c22-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="45c22-106">Los requisitos del puerto de Firewall para un único Director son los puertos que se usan para establecer comunicación con el director desde la interfaz interna o la red interna del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="45c22-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="45c22-107">Microsoft Lync Server 2013 espera de forma predeterminada que los puertos HTTP/TCP 8080 y HTTPS/TCP 4443 se abran desde el proxy inverso al Director, así como el servidor front-end y el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="45c22-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="45c22-108">Además, debe haber comunicación del Protocolo de inicio de sesión (SIP) desde la interfaz interna del servidor perimetral al Director y al grupo de servidores front-end y front-end.</span><span class="sxs-lookup"><span data-stu-id="45c22-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="45c22-109">El protocolo SIP usa SIP/MTLS/TCP 5061 del servidor perimetral al grupo front-end y al servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="45c22-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="45c22-110">También se debe crear una regla que permita la comunicación SIP/MTLS/TCP 5061 desde el director, el grupo de servidores front-end y el servidor front-end a la interfaz interna del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="45c22-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="45c22-111">Puertos y protocolos de un solo Director para definiciones de Firewall</span><span class="sxs-lookup"><span data-stu-id="45c22-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45c22-112">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="45c22-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="45c22-113">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="45c22-113">Source IP address</span></span></th>
<th><span data-ttu-id="45c22-114">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="45c22-114">Destination IP address</span></span></th>
<th><span data-ttu-id="45c22-115">Notas</span><span class="sxs-lookup"><span data-stu-id="45c22-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45c22-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="45c22-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="45c22-117">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="45c22-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="45c22-118">Director</span><span class="sxs-lookup"><span data-stu-id="45c22-118">Director</span></span></p></td>
<td><p><span data-ttu-id="45c22-119">Inicialmente recibido por el lado externo del proxy inverso, la comunicación se envía al Director y a los servicios Web de servidor front-end</span><span class="sxs-lookup"><span data-stu-id="45c22-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45c22-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="45c22-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="45c22-121">Interfaz interna de proxy invertida</span><span class="sxs-lookup"><span data-stu-id="45c22-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="45c22-122">Director</span><span class="sxs-lookup"><span data-stu-id="45c22-122">Director</span></span></p></td>
<td><p><span data-ttu-id="45c22-123">Inicialmente recibido por el lado externo del proxy inverso, la comunicación se envía al Director y a los servicios Web de servidor front-end</span><span class="sxs-lookup"><span data-stu-id="45c22-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45c22-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="45c22-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="45c22-125">Director</span><span class="sxs-lookup"><span data-stu-id="45c22-125">Director</span></span></p></td>
<td><p><span data-ttu-id="45c22-126">Servidor front-end o grupo front-end</span><span class="sxs-lookup"><span data-stu-id="45c22-126">Front End server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="45c22-127">Comunicación entre servidores entre el director y el servidor front-end</span><span class="sxs-lookup"><span data-stu-id="45c22-127">Inter-server communication between the Director and the Front End Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45c22-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="45c22-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="45c22-129">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="45c22-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="45c22-130">Servicios Web de Director</span><span class="sxs-lookup"><span data-stu-id="45c22-130">Director web services</span></span></p></td>
<td><p><span data-ttu-id="45c22-131">El director proporciona servicios web a clientes internos y externos.</span><span class="sxs-lookup"><span data-stu-id="45c22-131">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45c22-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="45c22-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="45c22-133">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="45c22-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="45c22-134">Servicios Web de Director</span><span class="sxs-lookup"><span data-stu-id="45c22-134">Director web services</span></span></p></td>
<td><p><span data-ttu-id="45c22-135">El director proporciona servicios web a clientes internos y externos.</span><span class="sxs-lookup"><span data-stu-id="45c22-135">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45c22-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="45c22-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="45c22-137">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="45c22-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="45c22-138">Director</span><span class="sxs-lookup"><span data-stu-id="45c22-138">Director</span></span></p></td>
<td><p><span data-ttu-id="45c22-139">Comunicación SIP desde el servidor perimetral al Director y al servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="45c22-139">SIP communication from the Edge Server to the Director, and the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45c22-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="45c22-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="45c22-141">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="45c22-141">Any</span></span></p></td>
<td><p><span data-ttu-id="45c22-142">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="45c22-142">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="45c22-143">Controlador de servicio de registro centralizado (ClsController.exe) o comandos del agente (ClasAgent.exe) y colección de registros</span><span class="sxs-lookup"><span data-stu-id="45c22-143">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45c22-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="45c22-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="45c22-145">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="45c22-145">Any</span></span></p></td>
<td><p><span data-ttu-id="45c22-146">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="45c22-146">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="45c22-147">Controlador de servicio de registro centralizado (ClsController.exe) o comandos del agente (ClasAgent.exe) y colección de registros</span><span class="sxs-lookup"><span data-stu-id="45c22-147">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45c22-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="45c22-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="45c22-149">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="45c22-149">Any</span></span></p></td>
<td><p><span data-ttu-id="45c22-150">Interfaz interna de Edge Server</span><span class="sxs-lookup"><span data-stu-id="45c22-150">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="45c22-151">Controlador de servicio de registro centralizado (ClsController.exe) o comandos del agente (ClasAgent.exe) y colección de registros</span><span class="sxs-lookup"><span data-stu-id="45c22-151">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="45c22-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45c22-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

