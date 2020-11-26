---
title: 'Resumen del certificado: SIP, Federación XMPP y mensajería instantánea pública'
description: 'Resumen del certificado: SIP, Federación XMPP y mensajería instantánea pública.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - SIP, XMPP federation, and public instant messaging
ms:assetid: 933d6351-cfa6-4432-b3ed-1aff3ac92065
ms:mtpsurl: https://technet.microsoft.com/library/JJ618372(v=OCS.15)
ms:contentKeyID: 49105659
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 565d3b935d304aa09588688bd8d71948b1b3ec3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435190"
---
# <a name="certificate-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="6ec31-103">Resumen del certificado: SIP, Federación XMPP y mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ec31-103">Certificate summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ec31-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ec31-104">

<span> </span></span></span>

<span data-ttu-id="6ec31-105">_**Última modificación del tema:** 2013-03-15_</span><span class="sxs-lookup"><span data-stu-id="6ec31-105">_**Topic Last Modified:** 2013-03-15_</span></span>

<span data-ttu-id="6ec31-106">Los certificados que necesita para la Federación con Microsoft Lync Server 2013, Lync Server 2010 y Office Communications Server generalmente se cumplirán con los certificados que configure, solicite y asigne a su servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="6ec31-106">The certificates that you need for federating with Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server will typically be met by the certificates that you configure, request and assign to your Edge Server.</span></span>

<span data-ttu-id="6ec31-107">Los requisitos de certificados para habilitar y establecer comunicaciones con los partners protocolo de presencia y mensajería extensible (XMPP) requieren agregar entradas a los dominios XMPP.</span><span class="sxs-lookup"><span data-stu-id="6ec31-107">Certificate requirements for enabling and establishing communications with extensible messaging and presence protocol (XMPP) partners require addition of entries for your XMPP domains.</span></span> <span data-ttu-id="6ec31-108">El registro que se incluye en el certificado como un nombre alternativo del sujeto (SAN) será el dominio que puede participar en las comunicaciones XMPP.</span><span class="sxs-lookup"><span data-stu-id="6ec31-108">The record that is included on the certificate as a subject alternative name (SAN) will be the domain that can participate in XMPP communications.</span></span> <span data-ttu-id="6ec31-109">El dominio puede ser el dominio de nivel raíz (por ejemplo, contoso.com) Si desea habilitar XMPP para todo el dominio o puede seleccionar dominios secundarios (por ejemplo, corp.contoso.com, finance.contoso.com) si va a habilitar XMPP para un subconjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="6ec31-109">The domain can be the root-level domain (for example, contoso.com) if you want to enable XMPP for your entire domain, or can be selected child domains (for example, corp.contoso.com, finance.contoso.com) if you are enabling XMPP for a subset of users.</span></span>

<span data-ttu-id="6ec31-110">Para configurar certificados para la conectividad de mensajería instantánea pública, tenga en cuenta que no hay nada diferente de otros tipos de Federación SIP o incluso de certificados de servidor perimetral estándar, excepto que America Online (AOL) requiere un certificado o certificados (en el caso de un grupo Edge) para incluir también el EKU de cliente.</span><span class="sxs-lookup"><span data-stu-id="6ec31-110">To configure certificates for public Instant Messaging connectivity, note that there is nothing different from other SIP federation types or even standard Edge Server certificates, except that America Online (AOL) requires a the certificate or certificates (in the case of an Edge pool) to also contain the client EKU.</span></span> <span data-ttu-id="6ec31-111">El EKU de cliente es una adición al certificado y forma parte del certificado público externo que se asigna al servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="6ec31-111">The client EKU is an addition to the certificate, and is part of the external public certificate that is assigned to your Edge Server.</span></span>

<span data-ttu-id="6ec31-112">Para confirmar que ha cumplido los requisitos de certificado correctos para su implementación del servidor perimetral, revise los temas que aparecen en la sección titulada **también**.</span><span class="sxs-lookup"><span data-stu-id="6ec31-112">To confirm that you have met the correct certificate requirements for your Edge Server deployment, review the topics listed in the section titled **See Also**.</span></span>

<div>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ec31-113">Componente</span><span class="sxs-lookup"><span data-stu-id="6ec31-113">Component</span></span></th>
<th><span data-ttu-id="6ec31-114">Nombre del asunto</span><span class="sxs-lookup"><span data-stu-id="6ec31-114">Subject name</span></span></th>
<th><span data-ttu-id="6ec31-115">Nombres alternativos de asunto (SAN)</span><span class="sxs-lookup"><span data-stu-id="6ec31-115">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="6ec31-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ec31-116">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ec31-117">Perimetral de acceso externo</span><span class="sxs-lookup"><span data-stu-id="6ec31-117">External/Access Edge</span></span></p></td>
<td><p><span data-ttu-id="6ec31-118">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6ec31-118">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6ec31-119">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6ec31-119">sip.contoso.com</span></span></p>
<p><span data-ttu-id="6ec31-120">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6ec31-120">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="6ec31-121">contoso.com</span><span class="sxs-lookup"><span data-stu-id="6ec31-121">contoso.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="6ec31-122">Para admitir el espacio de nombres XMPP de contoso.com</span><span class="sxs-lookup"><span data-stu-id="6ec31-122">To support the contoso.com XMPP namespace</span></span>


<p><span data-ttu-id="6ec31-123">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="6ec31-123">sip.fabrikam.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="6ec31-124">Para admitir el espacio de nombres SIP fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="6ec31-124">To support the fabrikam.com SIP namespace</span></span>


<p><span data-ttu-id="6ec31-125">fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="6ec31-125">fabrikam.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="6ec31-126">Para admitir el espacio de nombres XMPP de fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="6ec31-126">To support the fabrikam.com XMPP namespace</span></span>

</td>
<td><p><span data-ttu-id="6ec31-127">El certificado debe ser de una entidad de certificación pública y debe tener el EKU de servidor y el EKU de cliente si se va a implementar la conectividad de mensajería instantánea pública con AOL.</span><span class="sxs-lookup"><span data-stu-id="6ec31-127">The certificate must be from a Public CA, and must have the server EKU and client EKU if public IM connectivity with AOL is to be deployed.</span></span> <span data-ttu-id="6ec31-128">El certificado se asigna a las interfaces del servidor perimetral externo para:</span><span class="sxs-lookup"><span data-stu-id="6ec31-128">The certificate is assigned to the external Edge Server interfaces for:</span></span></p>
<ul>
<li><p><span data-ttu-id="6ec31-129">Servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="6ec31-129">Access Edge service</span></span></p></li>
<li><p><span data-ttu-id="6ec31-130">Servicio perimetral de conferencia web</span><span class="sxs-lookup"><span data-stu-id="6ec31-130">Web Conferencing Edge service</span></span></p></li>
<li><p><span data-ttu-id="6ec31-131">Servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="6ec31-131">A/V Edge service</span></span></p></li>
</ul>



> [!NOTE]
> <span data-ttu-id="6ec31-132">Técnicamente, no se asigna un certificado al borde de A/V.</span><span class="sxs-lookup"><span data-stu-id="6ec31-132">Technically, a certificate is not assigned to the A/V Edge.</span></span> <span data-ttu-id="6ec31-133">La comunicación y la autenticación seguras se administran mediante el servicio de autenticación de retransmisión multimedia (MRAS).</span><span class="sxs-lookup"><span data-stu-id="6ec31-133">Secure communication and authentication is managed by way of the Media Relay Authentication Service (MRAS).</span></span> <span data-ttu-id="6ec31-134">MRAS usa el certificado asignado a la interfaz interna del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="6ec31-134">MRAS uses the certificate assigned to the Edge Server internal interface.</span></span>


<p><span data-ttu-id="6ec31-135">Tenga en cuenta que las redes San se agregan automáticamente al certificado según sus definiciones en el generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="6ec31-135">Note that SANs are automatically added to the certificate based on your definitions in Topology Builder.</span></span> <span data-ttu-id="6ec31-136">Agregue las entradas de SAN según sea necesario para dominios SIP adicionales y otras entradas que necesite admitir.</span><span class="sxs-lookup"><span data-stu-id="6ec31-136">You add SAN entries as needed for additional SIP domains and other entries that you need to support.</span></span> <span data-ttu-id="6ec31-137">El nombre del asunto se replica en el SAN y debe estar presente para que funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ec31-137">The subject name is replicated in the SAN and must be present for correct operation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6ec31-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ec31-138">See Also</span></span>


[<span data-ttu-id="6ec31-139">Configuración XMPP de ejemplo en Lync Server 2013 - Federación XMPP con Google Talk</span><span class="sxs-lookup"><span data-stu-id="6ec31-139">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="6ec31-140">Plan para certificados de servidores perimetrales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ec31-140">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)  
[<span data-ttu-id="6ec31-141">Resumen de certificado - Servidor perimetral consolidado simple con direcciones IP privadas mediante NAT en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ec31-141">Certificate summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-consolidated-edge-with-private-ip-addresses-using-nat.md)  
[<span data-ttu-id="6ec31-142">Resumen de certificado - Perímetro consolidado de equipo único con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ec31-142">Certificate summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-consolidated-edge-with-public-ip-addresses.md)  
[<span data-ttu-id="6ec31-143">Resumen de certificado - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP privadas con NAT en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ec31-143">Certificate summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-dns-load-balancing-private-ip.md)  
[<span data-ttu-id="6ec31-144">Resumen de certificado - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ec31-144">Certificate summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)  
[<span data-ttu-id="6ec31-145">Resumen de certificado - Servidor perimetral consolidado ampliado con equilibradores de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ec31-145">Certificate summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-with-hardware-load-balancers.md)  
  

<span data-ttu-id="6ec31-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ec31-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

