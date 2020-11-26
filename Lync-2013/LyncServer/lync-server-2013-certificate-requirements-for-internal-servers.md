---
title: 'Lync Server 2013: Requisitos de certificado para Servidores internos'
description: 'Lync Server 2013: requisitos de certificado para servidores internos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for internal servers
ms:assetid: 0444cdbd-538c-43b1-b9a1-9d7d6cf818d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398094(v=OCS.15)
ms:contentKeyID: 48183270
ms.date: 02/17/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc1a627dd762c849b848087a96e00e19d320ef01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435358"
---
# <a name="certificate-requirements-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="b9fab-103">Requisitos de certificado para Servidores internos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b9fab-103">Certificate requirements for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b9fab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b9fab-104">

<span> </span></span></span>

<span data-ttu-id="b9fab-105">_**Última modificación del tema:** 2017-02-17_</span><span class="sxs-lookup"><span data-stu-id="b9fab-105">_**Topic Last Modified:** 2017-02-17_</span></span>

<span data-ttu-id="b9fab-106">Los servidores internos que ejecutan Lync Server y que requieren certificados incluyen el servidor Standard Edition, el servidor front-end Enterprise Edition, el servidor de mediación y el director.</span><span class="sxs-lookup"><span data-stu-id="b9fab-106">Internal servers that are running Lync Server and that require certificates include Standard Edition server, Enterprise Edition Front End Server, Mediation Server, and Director.</span></span> <span data-ttu-id="b9fab-107">En la tabla siguiente se muestran los requisitos de certificados para estos servidores.</span><span class="sxs-lookup"><span data-stu-id="b9fab-107">The following table shows the certificate requirements for these servers.</span></span> <span data-ttu-id="b9fab-108">Puede usar el Asistente para certificados de Lync Server para solicitar estos certificados.</span><span class="sxs-lookup"><span data-stu-id="b9fab-108">You can use the Lync Server certificate wizard to request these certificates.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="b9fab-109">Los certificados comodín son compatibles con los nombres alternativos de asunto asociados con las direcciones URL simples del grupo de servidores front-end, del servidor front-end o del director.</span><span class="sxs-lookup"><span data-stu-id="b9fab-109">Wildcard certificates are supported for the subject alternative names associated with the simple URLs on the Front End pool, Front End Server, or Director.</span></span> <span data-ttu-id="b9fab-110">Para obtener más información acerca de la compatibilidad con certificados comodín, consulte <A href="lync-server-2013-wildcard-certificate-support.md">compatibilidad de certificados comodín en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="b9fab-110">For details about wildcard certificate support, see <A href="lync-server-2013-wildcard-certificate-support.md">Wildcard certificate support in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="b9fab-111">Aunque se recomienda una entidad de certificación (CA) interna de empresa para los servidores internos, también puede usar una CA pública.</span><span class="sxs-lookup"><span data-stu-id="b9fab-111">Although an internal enterprise certification authority (CA) is recommended for internal servers, you can also use a public CA.</span></span> <span data-ttu-id="b9fab-112">Para obtener una lista de las entidades emisoras de certificados públicas que proporcionan certificados que cumplen con los requisitos específicos para certificados de comunicaciones unificadas (UC) y que se han asociado con Microsoft para garantizar que funcionan con el Asistente para certificados de Lync Server, consulte el artículo 929395 de Microsoft Knowledge base, "asociados de certificados de comunicaciones unificadas para Exchange Server y Communications Server" en [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834) .</span><span class="sxs-lookup"><span data-stu-id="b9fab-112">For a list of public CAs that provide certificates that comply with specific requirements for unified communications (UC) certificates and have partnered with Microsoft to ensure they work with the Lync Server Certificate Wizard, see article Microsoft Knowledge Base 929395, "Unified Communications Certificate Partners for Exchange Server and for Communications Server," at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834).</span></span>

<span data-ttu-id="b9fab-113">La comunicación con otras aplicaciones y servidores, como Exchange 2013, requiere un certificado que sea compatible con otras aplicaciones y productos.</span><span class="sxs-lookup"><span data-stu-id="b9fab-113">Communication with other applications and servers, such as Exchange 2013, requires a certificate that is supported by the other applications and products.</span></span> <span data-ttu-id="b9fab-114">Para la versión 2013, Lync Server 2013 y otros productos de Microsoft Server, incluidos Exchange 2013 y SharePoint Server, admiten el protocolo de autorización abierta (OAuth) para la autenticación y la autorización de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="b9fab-114">For the 2013 release, Lync Server 2013 and other Microsoft server products, including Exchange 2013 and SharePoint Server, support the Open Authorization (OAuth) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="b9fab-115">Para obtener más información, vea [administrar la autenticación de servidor a servidor (OAuth) y las aplicaciones de socios en Lync server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) en la documentación de implementación o en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="b9fab-115">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="b9fab-116">Para las conexiones de clientes que ejecutan el sistema operativo Windows 7, el sistema operativo Windows Server 2008, el sistema operativo Windows Server 2008 R2, el sistema operativo Windows Vista y Microsoft Lync Phone Edition, Lync Server 2013 incluye compatibilidad con (pero no requiere) certificados firmados con la función de hash criptográfica SHA-256.</span><span class="sxs-lookup"><span data-stu-id="b9fab-116">For connections from clients running Windows 7 operating system, Windows Server 2008 operating system, Windows Server 2008 R2 operating system, Windows Vista operating system, and Microsoft Lync Phone Edition, Lync Server 2013 includes support for (but does not require) certificates signed using the SHA-256 cryptographic hash function.</span></span> <span data-ttu-id="b9fab-117">Para admitir el acceso externo mediante SHA-256, un certificado externo es emitido por una entidad de certificación pública con SHA-256.</span><span class="sxs-lookup"><span data-stu-id="b9fab-117">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>

<span data-ttu-id="b9fab-118">En las tablas siguientes se muestran los requisitos de los certificados por función del servidor para los servidores front-end y los servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="b9fab-118">The following tables show certificate requirements by server role for Front End pools and Standard Edition servers.</span></span> <span data-ttu-id="b9fab-119">Todos son certificados de servidor web estándar, clave privada, no exportable.</span><span class="sxs-lookup"><span data-stu-id="b9fab-119">All these are standard web server certificates, private key, non-exportable.</span></span>

<span data-ttu-id="b9fab-120">Tenga en cuenta que el uso mejorado de clave (EKU) del servidor se configura automáticamente cuando usa el Asistente para certificados para solicitar certificados.</span><span class="sxs-lookup"><span data-stu-id="b9fab-120">Note that server enhanced key usage (EKU) is automatically configured when you use the certificate wizard to request certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b9fab-121">Cada nombre descriptivo de certificado debe ser único en el almacén de equipos.</span><span class="sxs-lookup"><span data-stu-id="b9fab-121">Each certificate Friendly Name must be unique in the computer store.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="b9fab-122">Si ha configurado sipinternal.contoso.com o sipexternal.contoso.com en su DNS, tendrá que agregarlos en el nombre alternativo de asunto del certificado.</span><span class="sxs-lookup"><span data-stu-id="b9fab-122">If you have configured sipinternal.contoso.com or sipexternal.contoso.com in your DNS, you will need to add them in the certificate’s Subject Alternative Name.</span></span>



</div>

### <a name="certificates-for-standard-edition-server"></a><span data-ttu-id="b9fab-123">Certificados para un servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="b9fab-123">Certificates for Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9fab-124">Certificado</span><span class="sxs-lookup"><span data-stu-id="b9fab-124">Certificate</span></span></th>
<th><span data-ttu-id="b9fab-125">Nombre del asunto/nombre común</span><span class="sxs-lookup"><span data-stu-id="b9fab-125">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="b9fab-126">Nombre alternativo de sujeto</span><span class="sxs-lookup"><span data-stu-id="b9fab-126">Subject alternative name</span></span></th>
<th><span data-ttu-id="b9fab-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9fab-127">Example</span></span></th>
<th><span data-ttu-id="b9fab-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9fab-128">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9fab-129">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b9fab-129">Default</span></span></p></td>
<td><p><span data-ttu-id="b9fab-130">Nombre de dominio completo (FQDN) del grupo</span><span class="sxs-lookup"><span data-stu-id="b9fab-130">Fully qualified domain name (FQDN) of the pool</span></span></p></td>
<td><p><span data-ttu-id="b9fab-131">FQDN del grupo y el FQDN del servidor</span><span class="sxs-lookup"><span data-stu-id="b9fab-131">FQDN of the pool and the FQDN of the server</span></span></p>
<p><span data-ttu-id="b9fab-132">Si hay varios dominios SIP y está habilitada la configuración automática de los clientes, el Asistente para certificados detectará y agregará los FQDN de todos los dominios SIP admitidos.</span><span class="sxs-lookup"><span data-stu-id="b9fab-132">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="b9fab-133">Si este grupo de servidores es el servidor de inicio automático de sesión de los clientes y se requiere una correspondencia exacta del sistema de nombres de dominio (DNS) en la directiva del grupo, necesitará también entradas para sip.sipdomain (para cada uno de los dominios SIP que tenga).</span><span class="sxs-lookup"><span data-stu-id="b9fab-133">If this pool is the auto-logon server for clients and strict Domain Name System (DNS) matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="b9fab-134">SN=se01.contoso.com; SAN=se01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-134">SN=se01.contoso.com; SAN=se01.contoso.com</span></span></p>
<p><span data-ttu-id="b9fab-135">Si este grupo de servidores es el servidor de inicio automático de sesión de los clientes y se requiere una correspondencia exacta de DNS en la directiva del grupo, necesitará también SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-135">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="b9fab-136">En el servidor Standard Edition, el FQDN del servidor es el mismo que el FQDN del grupo.</span><span class="sxs-lookup"><span data-stu-id="b9fab-136">On Standard Edition server, the server FQDN is the same as the pool FQDN.</span></span></p>
<p><span data-ttu-id="b9fab-137">El asistente detecta todos los dominios SIP especificados durante la instalación y los agrega automáticamente al nombre alternativo de sujeto.</span><span class="sxs-lookup"><span data-stu-id="b9fab-137">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="b9fab-138">También puede usar este certificado para la autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="b9fab-138">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9fab-139">Web interno</span><span class="sxs-lookup"><span data-stu-id="b9fab-139">Web internal</span></span></p></td>
<td><p><span data-ttu-id="b9fab-140">FQDN del servidor</span><span class="sxs-lookup"><span data-stu-id="b9fab-140">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="b9fab-141">Cada uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b9fab-141">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="b9fab-142">FQDN web interno (que es igual que el FQDN del servidor)</span><span class="sxs-lookup"><span data-stu-id="b9fab-142">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="b9fab-143">URL sencilla de reunión</span><span class="sxs-lookup"><span data-stu-id="b9fab-143">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="b9fab-144">URL sencilla de marcado</span><span class="sxs-lookup"><span data-stu-id="b9fab-144">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-145">URL sencilla de administración</span><span class="sxs-lookup"><span data-stu-id="b9fab-145">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-146">O bien, una entrada comodín para las direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="b9fab-146">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b9fab-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="b9fab-148">Con un certificado de comodín:</span><span class="sxs-lookup"><span data-stu-id="b9fab-148">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="b9fab-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="b9fab-150">No puede invalidar el FQDN de la web interna en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="b9fab-150">You cannot override the Internal web FQDN in Topology Builder.</span></span></p>
<p><span data-ttu-id="b9fab-151">Si tiene varias direcciones URL simples, debe incluirlas como nombres alternativos de asunto.</span><span class="sxs-lookup"><span data-stu-id="b9fab-151">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="b9fab-152">Las entradas de comodín se admiten para las entradas de direcciones URL sencillas.</span><span class="sxs-lookup"><span data-stu-id="b9fab-152">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9fab-153">Web externo</span><span class="sxs-lookup"><span data-stu-id="b9fab-153">Web external</span></span></p></td>
<td><p><span data-ttu-id="b9fab-154">FQDN del servidor</span><span class="sxs-lookup"><span data-stu-id="b9fab-154">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="b9fab-155">Cada uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b9fab-155">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="b9fab-156">FQDN web externo</span><span class="sxs-lookup"><span data-stu-id="b9fab-156">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="b9fab-157">URL sencilla de marcado</span><span class="sxs-lookup"><span data-stu-id="b9fab-157">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-158">Direcciones URL sencillas de reunión por dominio SIP</span><span class="sxs-lookup"><span data-stu-id="b9fab-158">Meet simple URLs per SIP domain</span></span></p></li>
<li><p><span data-ttu-id="b9fab-159">O bien, una entrada comodín para las direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="b9fab-159">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b9fab-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="b9fab-161">Con un certificado de comodín:</span><span class="sxs-lookup"><span data-stu-id="b9fab-161">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="b9fab-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="b9fab-163">Si tiene varias direcciones URL simples, debe incluirlas como nombres alternativos de asunto.</span><span class="sxs-lookup"><span data-stu-id="b9fab-163">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="b9fab-164">Las entradas de comodín se admiten para las entradas de direcciones URL sencillas.</span><span class="sxs-lookup"><span data-stu-id="b9fab-164">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-front-end-server-in-a-front-end-pool"></a><span data-ttu-id="b9fab-165">Certificados para el servidor front-end en un grupo de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="b9fab-165">Certificates for Front End Server in a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9fab-166">Certificado</span><span class="sxs-lookup"><span data-stu-id="b9fab-166">Certificate</span></span></th>
<th><span data-ttu-id="b9fab-167">Nombre del asunto/nombre común</span><span class="sxs-lookup"><span data-stu-id="b9fab-167">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="b9fab-168">Nombre alternativo de sujeto</span><span class="sxs-lookup"><span data-stu-id="b9fab-168">Subject alternative name</span></span></th>
<th><span data-ttu-id="b9fab-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9fab-169">Example</span></span></th>
<th><span data-ttu-id="b9fab-170">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9fab-170">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9fab-171">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b9fab-171">Default</span></span></p></td>
<td><p><span data-ttu-id="b9fab-172">FQDN del grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="b9fab-172">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="b9fab-173">FQDN del grupo y FQDN del servidor.</span><span class="sxs-lookup"><span data-stu-id="b9fab-173">FQDN of the pool and FQDN of the server.</span></span></p>
<p><span data-ttu-id="b9fab-174">Si hay varios dominios SIP y está habilitada la configuración automática de los clientes, el Asistente para certificados detectará y agregará los FQDN de todos los dominios SIP admitidos.</span><span class="sxs-lookup"><span data-stu-id="b9fab-174">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="b9fab-175">Si este grupo es el servidor de inicio de sesión automático para clientes y se requiere coincidencia de DNS estricta en la Directiva de grupo, también necesitarás entradas para SIP. sipdomain (para cada dominio SIP que tengas).</span><span class="sxs-lookup"><span data-stu-id="b9fab-175">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="b9fab-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com </span><span class="sxs-lookup"><span data-stu-id="b9fab-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com</span></span></p>
<p><span data-ttu-id="b9fab-177">Si este grupo de servidores es el servidor de inicio automático de sesión de los clientes y se requiere una correspondencia exacta de DNS en la directiva del grupo, necesitará también SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-177">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="b9fab-178">El asistente detecta todos los dominios SIP especificados durante la instalación y los agrega automáticamente al nombre alternativo de sujeto.</span><span class="sxs-lookup"><span data-stu-id="b9fab-178">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="b9fab-179">También puede usar este certificado para la autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="b9fab-179">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9fab-180">Interno de la web</span><span class="sxs-lookup"><span data-stu-id="b9fab-180">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="b9fab-181">FQDN del grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="b9fab-181">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="b9fab-182">Cada uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b9fab-182">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="b9fab-183">FQDN web interno (que NO es el mismo que el FQDN del servidor)</span><span class="sxs-lookup"><span data-stu-id="b9fab-183">Internal web FQDN (which is NOT the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="b9fab-184">FQDN del servidor</span><span class="sxs-lookup"><span data-stu-id="b9fab-184">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="b9fab-185">FQDN del grupo de Lync</span><span class="sxs-lookup"><span data-stu-id="b9fab-185">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="b9fab-186">URL sencilla de reunión</span><span class="sxs-lookup"><span data-stu-id="b9fab-186">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="b9fab-187">URL sencilla de marcado</span><span class="sxs-lookup"><span data-stu-id="b9fab-187">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-188">URL sencilla de administración</span><span class="sxs-lookup"><span data-stu-id="b9fab-188">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-189">O bien, una entrada comodín para las direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="b9fab-189">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b9fab-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="b9fab-191">Con un certificado de comodín:</span><span class="sxs-lookup"><span data-stu-id="b9fab-191">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="b9fab-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="b9fab-193">Si tiene varias direcciones URL simples, debe incluirlas como nombres alternativos de asunto.</span><span class="sxs-lookup"><span data-stu-id="b9fab-193">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="b9fab-194">Las entradas de comodín se admiten para las entradas de direcciones URL sencillas.</span><span class="sxs-lookup"><span data-stu-id="b9fab-194">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9fab-195">Web externo</span><span class="sxs-lookup"><span data-stu-id="b9fab-195">Web external</span></span></p></td>
<td><p><span data-ttu-id="b9fab-196">FQDN del grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="b9fab-196">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="b9fab-197">Cada uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b9fab-197">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="b9fab-198">FQDN web externo</span><span class="sxs-lookup"><span data-stu-id="b9fab-198">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="b9fab-199">URL sencilla de marcado</span><span class="sxs-lookup"><span data-stu-id="b9fab-199">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-200">URL sencilla de administración</span><span class="sxs-lookup"><span data-stu-id="b9fab-200">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-201">O bien, una entrada comodín para las direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="b9fab-201">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b9fab-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="b9fab-203">Con un certificado de comodín:</span><span class="sxs-lookup"><span data-stu-id="b9fab-203">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="b9fab-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="b9fab-205">Si tiene varias direcciones URL simples, debe incluirlas como nombres alternativos de asunto.</span><span class="sxs-lookup"><span data-stu-id="b9fab-205">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="b9fab-206">Las entradas de comodín se admiten para las entradas de direcciones URL sencillas.</span><span class="sxs-lookup"><span data-stu-id="b9fab-206">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-director"></a><span data-ttu-id="b9fab-207">Certificados para Director</span><span class="sxs-lookup"><span data-stu-id="b9fab-207">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9fab-208">Certificado</span><span class="sxs-lookup"><span data-stu-id="b9fab-208">Certificate</span></span></th>
<th><span data-ttu-id="b9fab-209">Nombre del asunto/nombre común</span><span class="sxs-lookup"><span data-stu-id="b9fab-209">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="b9fab-210">Nombre alternativo de sujeto</span><span class="sxs-lookup"><span data-stu-id="b9fab-210">Subject alternative name</span></span></th>
<th><span data-ttu-id="b9fab-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9fab-211">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9fab-212">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b9fab-212">Default</span></span></p></td>
<td><p><span data-ttu-id="b9fab-213">FQDN del grupo de directores</span><span class="sxs-lookup"><span data-stu-id="b9fab-213">FQDN of the Director pool</span></span></p></td>
<td><p><span data-ttu-id="b9fab-214">FQDN del Director, FQDN del grupo de directores</span><span class="sxs-lookup"><span data-stu-id="b9fab-214">FQDN of the Director, FQDN of the Director pool</span></span></p>
<p><span data-ttu-id="b9fab-215">Si este grupo es el servidor de inicio de sesión automático para clientes y se requiere coincidencia de DNS estricta en la Directiva de grupo, también necesitarás entradas para SIP. sipdomain (para cada dominio SIP que tengas).</span><span class="sxs-lookup"><span data-stu-id="b9fab-215">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="b9fab-216">SN = dir-pool.contoso.com; SAN = dir-pool.contoso.com; SAN = dir01. contoso. com</span><span class="sxs-lookup"><span data-stu-id="b9fab-216">SN=dir-pool.contoso.com; SAN=dir-pool.contoso.com; SAN=dir01.contoso.com</span></span></p>
<p><span data-ttu-id="b9fab-217">Si este grupo de directores es el servidor de inicio de sesión automático para clientes y se requiere una coincidencia de DNS estricta en la Directiva de grupo, también necesita SAN = SIP. contoso. com; SAN = SIP. fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="b9fab-217">If this Director pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9fab-218">Interno de la web</span><span class="sxs-lookup"><span data-stu-id="b9fab-218">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="b9fab-219">FQDN del servidor</span><span class="sxs-lookup"><span data-stu-id="b9fab-219">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="b9fab-220">Cada uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b9fab-220">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="b9fab-221">FQDN web interno (que es igual que el FQDN del servidor)</span><span class="sxs-lookup"><span data-stu-id="b9fab-221">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="b9fab-222">FQDN del servidor</span><span class="sxs-lookup"><span data-stu-id="b9fab-222">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="b9fab-223">FQDN del grupo de Lync</span><span class="sxs-lookup"><span data-stu-id="b9fab-223">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="b9fab-224">URL sencilla de reunión</span><span class="sxs-lookup"><span data-stu-id="b9fab-224">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="b9fab-225">URL sencilla de marcado</span><span class="sxs-lookup"><span data-stu-id="b9fab-225">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-226">URL sencilla de administración</span><span class="sxs-lookup"><span data-stu-id="b9fab-226">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-227">O bien, una entrada comodín para las direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="b9fab-227">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b9fab-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="b9fab-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9fab-230">Web externo</span><span class="sxs-lookup"><span data-stu-id="b9fab-230">Web external</span></span></p></td>
<td><p><span data-ttu-id="b9fab-231">FQDN del servidor</span><span class="sxs-lookup"><span data-stu-id="b9fab-231">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="b9fab-232">Cada uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b9fab-232">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="b9fab-233">FQDN web externo</span><span class="sxs-lookup"><span data-stu-id="b9fab-233">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="b9fab-234">URL sencilla de marcado</span><span class="sxs-lookup"><span data-stu-id="b9fab-234">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-235">URL sencilla de administración</span><span class="sxs-lookup"><span data-stu-id="b9fab-235">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="b9fab-236">O bien, una entrada comodín para las direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="b9fab-236">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b9fab-237">El FQDN de la web externa del Director debe ser diferente del de la aplicación front end o del servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="b9fab-237">The Director external web FQDN must be different from the Front End pool or Front End Server.</span></span></p>
<p><span data-ttu-id="b9fab-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="b9fab-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9fab-240">Si tiene un grupo de servidores de mediación independiente, cada uno de los servidores de mediación de cada uno necesita los certificados enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b9fab-240">If you have a stand-alone Mediation Server pool, the Mediation Servers in it each need the certificates listed in the following table.</span></span> <span data-ttu-id="b9fab-241">Si Collocate el servidor de mediación con los servidores front-end, los certificados que figuran en la tabla "certificados para el servidor front-end en la agrupación front end" anteriormente en este tema son suficientes.</span><span class="sxs-lookup"><span data-stu-id="b9fab-241">If you collocate Mediation Server with the Front End Servers, the certificates listed in the “Certificates for Front End Server in Front End Pool” table earlier in this topic are sufficient.</span></span>

### <a name="certificates-for-stand-alone-mediation-server"></a><span data-ttu-id="b9fab-242">Certificados para el servidor de mediación independiente</span><span class="sxs-lookup"><span data-stu-id="b9fab-242">Certificates for Stand-alone Mediation Server</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9fab-243">Certificado</span><span class="sxs-lookup"><span data-stu-id="b9fab-243">Certificate</span></span></th>
<th><span data-ttu-id="b9fab-244">Nombre del asunto/nombre común</span><span class="sxs-lookup"><span data-stu-id="b9fab-244">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="b9fab-245">Nombre alternativo de sujeto</span><span class="sxs-lookup"><span data-stu-id="b9fab-245">Subject alternative name</span></span></th>
<th><span data-ttu-id="b9fab-246">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9fab-246">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9fab-247">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b9fab-247">Default</span></span></p></td>
<td><p><span data-ttu-id="b9fab-248">FQDN del grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="b9fab-248">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="b9fab-249">FQDN del grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="b9fab-249">FQDN of the pool</span></span></p>
<p><span data-ttu-id="b9fab-250">FQDN del servidor miembro del grupo</span><span class="sxs-lookup"><span data-stu-id="b9fab-250">FQDN of pool member server</span></span></p></td>
<td><p><span data-ttu-id="b9fab-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="b9fab-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-survivable-branch-appliance"></a><span data-ttu-id="b9fab-252">Certificados para la aplicación de rama superviviente</span><span class="sxs-lookup"><span data-stu-id="b9fab-252">Certificates for Survivable Branch Appliance</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9fab-253">Certificado</span><span class="sxs-lookup"><span data-stu-id="b9fab-253">Certificate</span></span></th>
<th><span data-ttu-id="b9fab-254">Nombre del asunto/nombre común</span><span class="sxs-lookup"><span data-stu-id="b9fab-254">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="b9fab-255">Nombre alternativo de sujeto</span><span class="sxs-lookup"><span data-stu-id="b9fab-255">Subject alternative name</span></span></th>
<th><span data-ttu-id="b9fab-256">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9fab-256">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9fab-257">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="b9fab-257">Default</span></span></p></td>
<td><p><span data-ttu-id="b9fab-258">FQDN de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b9fab-258">FQDN of the appliance</span></span></p></td>
<td><p><span data-ttu-id="b9fab-259">SIP. &lt; sipdomain &gt; (necesita una entrada por cada dominio SIP)</span><span class="sxs-lookup"><span data-stu-id="b9fab-259">SIP.&lt;sipdomain&gt; (need one entry per SIP domain)</span></span></p></td>
<td><p><span data-ttu-id="b9fab-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="b9fab-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="b9fab-261">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9fab-261">See Also</span></span>


[<span data-ttu-id="b9fab-262">Compatibilidad de certificado de comodín en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b9fab-262">Wildcard certificate support in Lync Server 2013</span></span>](lync-server-2013-wildcard-certificate-support.md)  
  

<span data-ttu-id="b9fab-263"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b9fab-263"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

