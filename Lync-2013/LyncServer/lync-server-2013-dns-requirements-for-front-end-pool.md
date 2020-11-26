---
title: 'Lync Server 2013: Requisitos de DNS para el grupo de servidores front-end'
description: 'Lync Server 2013: requisitos de DNS para el grupo de servidores front-end.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pool
ms:assetid: 02d2aa6b-9e01-437b-a2df-00590280150d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398082(v=OCS.15)
ms:contentKeyID: 48183249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bfce90eccb8c8dff94d4122c96c4ca68ea9150f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437829"
---
# <a name="dns-requirements-for-front-end-pool-in-lync-server-2013"></a><span data-ttu-id="ae6d5-103">Requisitos de DNS para el grupo de servidores front-end en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae6d5-103">DNS requirements for Front End pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae6d5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae6d5-104">

<span> </span></span></span>

<span data-ttu-id="ae6d5-105">_**Última modificación del tema:** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="ae6d5-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="ae6d5-106">Para completar correctamente este procedimiento, debe haber iniciado sesión en el servidor o dominio como miembro del grupo administradores de dominio o en miembro del grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="ae6d5-107">Debe configurar los registros de sistema de nombres de dominio (DNS) necesarios antes de publicar su topología en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-107">You need to configure the required Domain Name System (DNS) records prior to publishing your topology in Topology Builder.</span></span> <span data-ttu-id="ae6d5-108">Además, algunos de los nombres de dominio completos (FQDN) que se usan en la configuración de una implementación de Lync Server 2013 son lógicos y no FQDN de servidor físico, por lo que es necesaria una configuración DNS adicional antes de la publicación.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-108">Additionally, some of the fully qualified domain names (FQDNs) used in the configuration of a Lync Server 2013 deployment are logical and not physical server FQDNs, so additional DNS configuration is required prior to publishing.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="ae6d5-109">Lync Server 2013 no admite dominios con etiqueta única.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-109">Lync Server 2013 does not support single-labeled domains.</span></span> <span data-ttu-id="ae6d5-110">Por ejemplo, un bosque con un dominio raíz denominado <STRONG>contoso. local</STRONG> es compatible, pero no se admite un dominio raíz denominado <STRONG>local</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ae6d5-110">For example, a forest with a root domain named <STRONG>contoso.local</STRONG> is supported, but a root domain named <STRONG>local</STRONG> is not supported.</span></span> <span data-ttu-id="ae6d5-111">Para obtener más información, consulte el artículo 300684 de Microsoft Knowledge base, "información sobre la configuración de Windows para dominios con nombres DNS de etiqueta única", en <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp ; kbid = 300684</A>.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-111">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=300684</A>.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ae6d5-112">El nombre que especifique debe ser idéntico al nombre de equipo configurado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-112">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="ae6d5-113">De forma predeterminada, el nombre de equipo de un equipo que no está unido a un dominio es un nombre corto, no un FQDN.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-113">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="ae6d5-114">El Generador de topologías usa nombres de dominio completos, no nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-114">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="ae6d5-115"><STRONG>Use solo caracteres estándar</STRONG> (incluidos A-z, a-z, 0-9 y guiones) al asignar FQDN de los servidores que ejecutan Lync Server, servidores perimetrales y grupos.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-115"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your servers running Lync Server, Edge Servers, and pools.</span></span> <span data-ttu-id="ae6d5-116">No utilice caracteres Unicode ni de subrayado.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-116">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="ae6d5-117">A menudo, los caracteres no estándar de un FQDN no son admitidos por el DNS externo y las entidades de certificación públicas (CA) (cuando se debe asignar el FQDN al SN en el certificado).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-117">Nonstandard characters in an FQDN are often not supported by external DNS and public certification authorities (CAs) (when the FQDN must be assigned to the SN in the certificate).</span></span>



</div>

<span data-ttu-id="ae6d5-118">Antes de operar la topología después de haberla implementado, asegúrese de crear los siguientes registros de Active Directory y DNS (según las necesidades de características específicas que determinen):</span><span class="sxs-lookup"><span data-stu-id="ae6d5-118">Prior to operating the topology after it has been deployed, ensure that the following Active Directory and DNS records are created (as your needs for specific features dictate):</span></span>

  - <span data-ttu-id="ae6d5-119">Cada rol de servidor que existirá en la topología se publica como un objeto de Active Directory (una vez que se une el equipo con el dominio).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-119">Each server role that will exist in the topology is published as an Active Directory object (joining the computer to the domain will accomplish this).</span></span>

  - <span data-ttu-id="ae6d5-120">Existe un registro A de DNS para cada servidor.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-120">A DNS A Record exists for each server.</span></span>

  - <span data-ttu-id="ae6d5-121">Existe un registro SRV de DNS para cada dominio SIP si piensa usar el inicio de sesión automático para clientes en forma de \_ sipinternaltls \_ TCP. \<SIP domain\> .</span><span class="sxs-lookup"><span data-stu-id="ae6d5-121">A DNS SRV Record exists for each SIP domain if you plan to use automatic logon for clients in the form of \_sipinternaltls\_tcp.\<SIP domain\>.</span></span> <span data-ttu-id="ae6d5-122">Si va a usar la configuración manual para clientes, este registro no es necesario.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-122">If you will use manual configuration for clients, this record is not necessary.</span></span>

  - <span data-ttu-id="ae6d5-123">Un registro A de DNS para cada dirección URL simple configurada, de la que normalmente hay cuatro: reunirse, marcación, LWA y programador.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-123">A DNS A Record for each configured simple URL, of which there are typically four: meet, dialin, lwa, and scheduler.</span></span> <span data-ttu-id="ae6d5-124">Además, existe la dirección URL simple de administrador, que es una dirección URL especial para el acceso al panel de control de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-124">Additionally, there is the admin simple URL which is a special URL for access to the Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="ae6d5-125">El servidor que ejecuta SQL Server debe estar unido al dominio y ser accesible desde el equipo desde el que se está publicando el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-125">The server running SQL Server must be joined to the domain, and reachable by the computer that Topology Builder is publishing from.</span></span>

<span data-ttu-id="ae6d5-126">La tabla sigue las arquitecturas de referencia presentadas en la sección de planificación.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-126">The table follows the reference architectures presented in the Planning section.</span></span> <span data-ttu-id="ae6d5-127">Para obtener más información, vea [escenarios de acceso de usuarios externos en Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-127">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) in the Planning documentation.</span></span>

<div id="sectionSection0" class="section">

### <a name="dns-records-required-for-the-front-end-pool"></a><span data-ttu-id="ae6d5-128">Registros DNS necesarios para el grupo de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="ae6d5-128">DNS Records Required for the Front End pool</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae6d5-129">Ubicación</span><span class="sxs-lookup"><span data-stu-id="ae6d5-129">Location</span></span></th>
<th><span data-ttu-id="ae6d5-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae6d5-130">Type</span></span></th>
<th><span data-ttu-id="ae6d5-131">FQDN</span><span class="sxs-lookup"><span data-stu-id="ae6d5-131">FQDN</span></span></th>
<th><span data-ttu-id="ae6d5-132">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="ae6d5-132">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae6d5-133">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-133">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-134">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-134">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-135">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ae6d5-135">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-136">Pool01 (equilibrio de carga de DNS).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-136">Pool01 (DNS load balancing).</span></span> <span data-ttu-id="ae6d5-137">Requiere un registro DNS A para la dirección IP de cada servidor front-end dentro del grupo, que se asigna al FQDN del grupo.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-137">Requires a DNS A record for the IP address of each Front End Server within the pool, mapping to the pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae6d5-138">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-138">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-139">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-139">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-140">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ae6d5-140">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-141">Pool01 (IP virtual (VIP) de equilibrador de carga de hardware).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-141">Pool01 (virtual IP (VIP) of hardware load balancer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae6d5-142">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-142">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-143">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-143">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-144">fe01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ae6d5-144">fe01.contoso.net</span></span></p>
<p><span data-ttu-id="ae6d5-145">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ae6d5-145">fe02.contoso.net</span></span></p>
<p><span data-ttu-id="ae6d5-146">fe03.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ae6d5-146">fe03.contoso.net</span></span></p>
<p><span data-ttu-id="ae6d5-147">…</span><span class="sxs-lookup"><span data-stu-id="ae6d5-147">…</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-148">Servidor front-end de Pool01 (nodo 1).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-148">Pool01 Front End Server (NODE 1).</span></span></p>
<p><span data-ttu-id="ae6d5-149">Servidor front-end Pool01 (nodo 2).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-149">Pool01 Front End Server (NODE 2).</span></span></p>
<p><span data-ttu-id="ae6d5-150">Servidor front-end Pool01 (nodo 3).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-150">Pool01 Front End Server (NODE 3).</span></span></p>
<p><span data-ttu-id="ae6d5-151">…</span><span class="sxs-lookup"><span data-stu-id="ae6d5-151">…</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae6d5-152">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-152">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-153">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-153">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-154">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ae6d5-154">fe02.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-155">Servidor front-end Pool01 (nodo 2).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-155">Pool01 Front End Server (NODE 2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae6d5-156">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-156">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-157">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-157">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-158">lsweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ae6d5-158">lsweb.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-159">Pool01 (VIP) para el tráfico web entre clientes y servidores.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-159">Pool01 (VIP) for client-to-server web traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae6d5-160">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-160">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-161">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-161">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-162">sqlbe.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ae6d5-162">sqlbe.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-163">Servidor de Pool01 back end con SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-163">Pool01 Back End Server running SQL Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae6d5-164">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-164">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-165">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-165">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-167">Necesario para Lync Phone Edition o el inicio de sesión automático de clientes sin registros SRV de DNS y para una coincidencia de dominios estricta.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-167">Required for Lync Phone Edition, or automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="ae6d5-168">No se requiere en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-168">Not required in all cases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae6d5-169">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-169">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-170">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-170">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-171">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-171">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-172">Supone que se trata de un segundo dominio SIP.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-172">Assumes a second SIP domain.</span></span> <span data-ttu-id="ae6d5-173">Necesario para Lync Phone Edition, el inicio de sesión automático de clientes sin los registros SRV de DNS y para la coincidencia estricta de dominios.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-173">Required for Lync Phone Edition, automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="ae6d5-174">No se requiere en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-174">Not required in all cases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae6d5-175">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-175">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-176">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-176">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-177">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-177">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-178">Dirección URL simple para conferencias de acceso telefónico local publicadas internamente: el servidor front-end (o director, si está instalado) responde a consultas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-178">Simple URL for dial-in conferencing published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae6d5-179">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-179">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-180">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-180">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-181">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-181">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-182">Dirección URL simple para conferencias publicadas internamente: el servidor front-end (o director, si está instalado) responde a consultas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-182">Simple URL for conferences published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae6d5-183">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-183">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-184">A</span><span class="sxs-lookup"><span data-stu-id="ae6d5-184">A</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-185">admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-185">admin.contoso.com</span></span></p>
<p><span data-ttu-id="ae6d5-186">administradores</span><span class="sxs-lookup"><span data-stu-id="ae6d5-186">admin</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-187">Registro opcional, dirección URL simple para Lync Server 2013 panel de control publicado internamente: el servidor front-end (o director, si está instalado) responde a consultas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-187">Optional record, simple URL for Lync Server 2013 Control Panel published internally - Front End Server (or Director, if installed) responds to simple URL queries.</span></span> <span data-ttu-id="ae6d5-188">Se recomienda usar solo el nombre de host (sin nombre de dominio).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-188">Host name only (no domain name) is recommended.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="ae6d5-189">VIP = dirección IP virtual de equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="ae6d5-189">VIP = Virtual IP address for hardware load balancer</span></span>



</div>

</div>

<div>

## <a name="dns-srv-records-for-the-front-end-pool"></a><span data-ttu-id="ae6d5-190">Registros SRV de DNS para el grupo de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="ae6d5-190">DNS SRV Records for the Front End pool</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae6d5-191">Ubicación</span><span class="sxs-lookup"><span data-stu-id="ae6d5-191">Location</span></span></th>
<th><span data-ttu-id="ae6d5-192">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae6d5-192">Type</span></span></th>
<th><span data-ttu-id="ae6d5-193">FQDN</span><span class="sxs-lookup"><span data-stu-id="ae6d5-193">FQDN</span></span></th>
<th><span data-ttu-id="ae6d5-194">FQDN de destino</span><span class="sxs-lookup"><span data-stu-id="ae6d5-194">Target FQDN</span></span></th>
<th><span data-ttu-id="ae6d5-195">Puerto</span><span class="sxs-lookup"><span data-stu-id="ae6d5-195">Port</span></span></th>
<th><span data-ttu-id="ae6d5-196">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="ae6d5-196">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae6d5-197">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-197">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-198">SRV</span><span class="sxs-lookup"><span data-stu-id="ae6d5-198">SRV</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-199">_sipinternaltls _sipinternaltls._tcp. contoso. com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-199">_sipinternaltls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-200">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-200">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-201">5061</span><span class="sxs-lookup"><span data-stu-id="ae6d5-201">5061</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-202">Necesario para que la configuración automática de los clientes de Lync 2013 funcione internamente.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-202">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae6d5-203">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-203">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-204">SRV</span><span class="sxs-lookup"><span data-stu-id="ae6d5-204">SRV</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-205">_sipinternaltls _sipinternaltls._tcp. fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-205">_sipinternaltls._tcp.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-206">pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-206">pool01.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-207">5061</span><span class="sxs-lookup"><span data-stu-id="ae6d5-207">5061</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-208">Necesario para que la configuración automática de los clientes de Lync 2013 funcione internamente.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-208">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae6d5-209">DNS interno</span><span class="sxs-lookup"><span data-stu-id="ae6d5-209">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-210">SRV</span><span class="sxs-lookup"><span data-stu-id="ae6d5-210">SRV</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-211">_ntp _ntp._udp. contoso. com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-211">_ntp._udp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-212">dc01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae6d5-212">dc01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-213">123</span><span class="sxs-lookup"><span data-stu-id="ae6d5-213">123</span></span></p></td>
<td><p><span data-ttu-id="ae6d5-214">El origen de protocolo de tiempo de red (NTP) es necesario para los dispositivos que ejecutan Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-214">Network Time Protocol (NTP) source required for devices running Lync Phone Edition.</span></span> <span data-ttu-id="ae6d5-215">Internamente, debe apuntar al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-215">Internally, this should point to the domain controller.</span></span> <span data-ttu-id="ae6d5-216">Si el controlador de dominio no está definido, intentará usar el servidor NTP time.windows.com.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-216">If the domain controller is not defined, it will try to use the NTP server time.windows.com.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ae6d5-217">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae6d5-217">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

