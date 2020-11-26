---
title: Excepciones IPsec de Lync Server 2013
description: Excepciones IPsec de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPsec exceptions
ms:assetid: 241f1eca-6f2f-44de-90b1-2cb659cbe27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425719(v=OCS.15)
ms:contentKeyID: 48183627
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b01264171592ec352b778e1aa7eee5861801991
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426728"
---
# <a name="ipsec-exceptions-in-lync-server-2013"></a><span data-ttu-id="efcda-103">Excepciones de IPsec en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="efcda-103">IPsec exceptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="efcda-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="efcda-104">

<span> </span></span></span>

<span data-ttu-id="efcda-105">_**Última modificación del tema:** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="efcda-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="efcda-106">En el caso de redes empresariales en las que se ha implementado la seguridad de protocolo de Internet (consulte IETF RFC 4301-4309), debe deshabilitarse IPsec en el rango de puertos que se usan para la entrega de video de audio, vídeo y panorámica.</span><span class="sxs-lookup"><span data-stu-id="efcda-106">For enterprise networks where Internet Protocol security (IPsec) (see IETF RFC 4301-4309) has been deployed, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span> <span data-ttu-id="efcda-107">Esta recomendación se fundamenta en la necesidad de evitar retrasos en la asignación de los puertos de medios por la negociación de IPsec.</span><span class="sxs-lookup"><span data-stu-id="efcda-107">The recommendation is motivated by the need to avoid any delay in the allocation of media ports due to IPsec negotiation.</span></span>

<span data-ttu-id="efcda-108">En la siguiente tabla se detalla la configuración de las excepciones de IPsec recomendadas.</span><span class="sxs-lookup"><span data-stu-id="efcda-108">The following table explains the recommended IPsec exception settings.</span></span>

### <a name="recommended-ipsec-exceptions"></a><span data-ttu-id="efcda-109">Excepciones de IPsec recomendadas</span><span class="sxs-lookup"><span data-stu-id="efcda-109">Recommended IPsec Exceptions</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="efcda-110">Nombre de regla</span><span class="sxs-lookup"><span data-stu-id="efcda-110">Rule name</span></span></th>
<th><span data-ttu-id="efcda-111">IP de origen</span><span class="sxs-lookup"><span data-stu-id="efcda-111">Source IP</span></span></th>
<th><span data-ttu-id="efcda-112">IP de destino</span><span class="sxs-lookup"><span data-stu-id="efcda-112">Destination IP</span></span></th>
<th><span data-ttu-id="efcda-113">Protocolo</span><span class="sxs-lookup"><span data-stu-id="efcda-113">Protocol</span></span></th>
<th><span data-ttu-id="efcda-114">Puerto de origen</span><span class="sxs-lookup"><span data-stu-id="efcda-114">Source port</span></span></th>
<th><span data-ttu-id="efcda-115">Puerto de destino</span><span class="sxs-lookup"><span data-stu-id="efcda-115">Destination port</span></span></th>
<th><span data-ttu-id="efcda-116">Requisito de autenticación</span><span class="sxs-lookup"><span data-stu-id="efcda-116">Authentication Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efcda-117">Servidor perimetral A/V interno entrante</span><span class="sxs-lookup"><span data-stu-id="efcda-117">A/V Edge Server Internal Inbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-118">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-118">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-119">Servidor perimetral A/V interno</span><span class="sxs-lookup"><span data-stu-id="efcda-119">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="efcda-120">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-120">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-121">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-121">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-122">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-122">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-123">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-123">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcda-124">Servidor perimetral A/V externo entrante</span><span class="sxs-lookup"><span data-stu-id="efcda-124">A/V Edge Server External Inbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-125">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-125">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-126">Servidor perimetral A/V externo</span><span class="sxs-lookup"><span data-stu-id="efcda-126">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="efcda-127">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-127">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-128">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-128">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-129">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-129">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-130">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-130">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcda-131">Servidor perimetral A/V interno saliente</span><span class="sxs-lookup"><span data-stu-id="efcda-131">A/V Edge Server Internal Outbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-132">Servidor perimetral A/V interno</span><span class="sxs-lookup"><span data-stu-id="efcda-132">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="efcda-133">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-133">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-134">&amp;TCP UDP</span><span class="sxs-lookup"><span data-stu-id="efcda-134">UDP &amp; TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-135">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-135">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-136">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-136">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-137">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-137">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcda-138">Servidor perimetral A/V externo saliente</span><span class="sxs-lookup"><span data-stu-id="efcda-138">A/V Edge Server External Outbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-139">Servidor perimetral A/V externo</span><span class="sxs-lookup"><span data-stu-id="efcda-139">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="efcda-140">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-140">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-141">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-141">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-142">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-142">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-143">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-143">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-144">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-144">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcda-145">Servidor de mediación entrante</span><span class="sxs-lookup"><span data-stu-id="efcda-145">Mediation Server Inbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-146">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-146">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-147">Servidores</span><span class="sxs-lookup"><span data-stu-id="efcda-147">Mediation</span></span></p>
<p><span data-ttu-id="efcda-148">de mediación</span><span class="sxs-lookup"><span data-stu-id="efcda-148">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="efcda-149">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-149">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-150">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-150">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-151">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-151">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-152">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-152">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcda-153">Servidor de mediación saliente</span><span class="sxs-lookup"><span data-stu-id="efcda-153">Mediation Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-154">Servidores</span><span class="sxs-lookup"><span data-stu-id="efcda-154">Mediation</span></span></p>
<p><span data-ttu-id="efcda-155">de mediación</span><span class="sxs-lookup"><span data-stu-id="efcda-155">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="efcda-156">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-156">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-157">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-157">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-158">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-158">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-159">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-159">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-160">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-160">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcda-161">Operador de conferencia entrante</span><span class="sxs-lookup"><span data-stu-id="efcda-161">Conferencing Attendant Inbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-162">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-162">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-163">Servidor front-end que ejecuta operador de conferencia</span><span class="sxs-lookup"><span data-stu-id="efcda-163">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="efcda-164">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-164">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-165">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-165">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-166">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-166">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-167">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-167">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcda-168">Operador de conferencia saliente</span><span class="sxs-lookup"><span data-stu-id="efcda-168">Conferencing Attendant Outbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-169">Servidor front-end que ejecuta operador de conferencia</span><span class="sxs-lookup"><span data-stu-id="efcda-169">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="efcda-170">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-170">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-171">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-171">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-172">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-172">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-173">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-173">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-174">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-174">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcda-175">Servidor de conferencia A/V entrante</span><span class="sxs-lookup"><span data-stu-id="efcda-175">A/V Conferencing Inbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-176">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-176">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-177">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="efcda-177">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="efcda-178">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-178">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-179">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-179">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-180">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-180">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-181">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-181">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcda-182">Salida de conferencia A/V</span><span class="sxs-lookup"><span data-stu-id="efcda-182">A/V Conferencing Outbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-183">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="efcda-183">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="efcda-184">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-184">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-185">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-185">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-186">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-186">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-187">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-187">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-188">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-188">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcda-189">Exchange entrante</span><span class="sxs-lookup"><span data-stu-id="efcda-189">Exchange Inbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-190">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-190">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-191">Mensajería unificada de Exchange</span><span class="sxs-lookup"><span data-stu-id="efcda-191">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="efcda-192">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-192">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-193">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-193">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-194">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-194">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-195">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-195">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcda-196">Servidores de aplicaciones compartidas entrantes</span><span class="sxs-lookup"><span data-stu-id="efcda-196">Application Sharing Servers Inbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-197">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-197">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-198">Servidores de aplicaciones compartidas</span><span class="sxs-lookup"><span data-stu-id="efcda-198">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="efcda-199">TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-199">TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-200">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-200">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-201">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-201">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-202">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-202">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcda-203">Servidor de aplicaciones compartidas saliente</span><span class="sxs-lookup"><span data-stu-id="efcda-203">Application Sharing Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-204">Servidores de aplicaciones compartidas</span><span class="sxs-lookup"><span data-stu-id="efcda-204">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="efcda-205">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-205">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-206">TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-206">TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-207">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-207">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-208">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-208">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-209">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-209">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcda-210">Exchange saliente</span><span class="sxs-lookup"><span data-stu-id="efcda-210">Exchange Outbound</span></span></p></td>
<td><p><span data-ttu-id="efcda-211">Mensajería unificada de Exchange</span><span class="sxs-lookup"><span data-stu-id="efcda-211">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="efcda-212">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-212">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-213">UDP y TCP</span><span class="sxs-lookup"><span data-stu-id="efcda-213">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="efcda-214">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-214">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-215">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-215">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-216">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-216">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcda-217">Clientes</span><span class="sxs-lookup"><span data-stu-id="efcda-217">Clients</span></span></p></td>
<td><p><span data-ttu-id="efcda-218">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-218">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-219">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-219">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-220">UDP</span><span class="sxs-lookup"><span data-stu-id="efcda-220">UDP</span></span></p></td>
<td><p><span data-ttu-id="efcda-221">Intervalo de puertos de medios especificado</span><span class="sxs-lookup"><span data-stu-id="efcda-221">Specified media port range</span></span></p></td>
<td><p><span data-ttu-id="efcda-222">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="efcda-222">Any</span></span></p></td>
<td><p><span data-ttu-id="efcda-223">No autenticar</span><span class="sxs-lookup"><span data-stu-id="efcda-223">Do not authenticate</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="efcda-224">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="efcda-224">


</div>

<span> </span>

</div>

</div>

</span></span></div>

