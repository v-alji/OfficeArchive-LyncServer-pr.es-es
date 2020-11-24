---
title: 'Resumen de puertos: SIP, Federación XMPP y mensajería instantánea pública'
description: 'Resumen de puertos: SIP, Federación XMPP y mensajería instantánea pública.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - SIP, XMPP federation, and public instant messaging
ms:assetid: ab05bdd6-e9b0-4b1b-9dd9-29ab88e8befe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618373(v=OCS.15)
ms:contentKeyID: 49105660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c58dbf7bdd56b4678d56f96a11332219bb40c17
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398172"
---
# <a name="port-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="a4855-103">Resumen de puertos: SIP, Federación XMPP y mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4855-103">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a4855-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a4855-104">

<span> </span></span></span>

<span data-ttu-id="a4855-105">_**Última modificación del tema:** 2013-03-15_</span><span class="sxs-lookup"><span data-stu-id="a4855-105">_**Topic Last Modified:** 2013-03-15_</span></span>

<span data-ttu-id="a4855-106">Los requisitos de puertos, protocolos y firewalls para la Federación con Microsoft Lync Server 2013, Lync Server 2010 y Office Communications Server son similares a los del servidor perimetral implementado.</span><span class="sxs-lookup"><span data-stu-id="a4855-106">Port, protocol and firewall requirements for federation with Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server are similar to those for the deployed Edge Server.</span></span> <span data-ttu-id="a4855-107">Los clientes inician la comunicación con el servicio perimetral de acceso a través de TLS/SIP/TCP 443.</span><span class="sxs-lookup"><span data-stu-id="a4855-107">Clients initiate communication with the Access Edge service over TLS/SIP/TCP 443.</span></span> <span data-ttu-id="a4855-108">Sin embargo, los socios federados iniciarán las comunicaciones con el servicio perimetral de acceso a través de MTLS/SIP/TCP 5061.</span><span class="sxs-lookup"><span data-stu-id="a4855-108">Federated partners however, will initiate communications to the Access Edge service over MTLS/SIP/TCP 5061.</span></span>

<span data-ttu-id="a4855-109">Para configurar el firewall para los puertos y protocolos necesarios para admitir la conectividad de mensajería instantánea pública, primero tenga en cuenta que los SIP/MTLS/TCP 5061 son bidireccionales para tener en cuenta la capacidad de los contactos en el proveedor de mi pública para ponerse en contacto con los clientes de Lync o para que Lync pueda comunicarse con los contactos públicos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="a4855-109">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="a4855-110">Windows Live Messenger puede participar en comunicaciones de audio y vídeo con clientes de Lync.</span><span class="sxs-lookup"><span data-stu-id="a4855-110">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="a4855-111">Esto cuenta con una configuración de protocolo y un puerto de Firewall muy similar que normalmente tendría en el firewall para admitir clientes de Lync como usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="a4855-111">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="a4855-112">Más que nunca, Lync es una herramienta eficaz para la conexión entre organizaciones y con personas de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="a4855-112">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="a4855-113">La Federación con Windows Live Messenger no requiere licencias de usuario o de dispositivo adicionales aparte de la licencia de acceso de cliente (CAL) de Lync.</span><span class="sxs-lookup"><span data-stu-id="a4855-113">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="a4855-114">La Federación de Skype se agrega a esta lista, lo que permite a los usuarios de Lync llegar a cientos de millones de personas con la mensajería instantánea y la voz.</span><span class="sxs-lookup"><span data-stu-id="a4855-114">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="a4855-115">La Federación con los contactos de los clientes de Messenger terminará oficialmente el 15 de marzo de 2013, excepto en el caso de China continental.</span><span class="sxs-lookup"><span data-stu-id="a4855-115">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="a4855-116">Skype se convertirá en el cliente de Federación para los usuarios federados que antes usaban Messenger.</span><span class="sxs-lookup"><span data-stu-id="a4855-116">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<span data-ttu-id="a4855-117">Los puertos y protocolos definidos para el proxy protocolo de presencia y mensajería extensible (XMPP) implementado en el servidor perimetral permiten las comunicaciones del socio XMPP federado hasta el servidor perimetral, y también permiten la comunicación desde el servidor perimetral al socio XMPP federado.</span><span class="sxs-lookup"><span data-stu-id="a4855-117">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="a4855-118">Una regla también se define en el Firewall de orientación interna desde el servidor front-end o el grupo front-end hasta el servidor perimetral o el grupo Edge.</span><span class="sxs-lookup"><span data-stu-id="a4855-118">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary---sip-federation"></a><span data-ttu-id="a4855-119">Resumen del firewall: Federación SIP</span><span class="sxs-lookup"><span data-stu-id="a4855-119">Firewall Summary - SIP Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4855-120">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="a4855-120">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="a4855-121">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="a4855-121">Source IP address</span></span></th>
<th><span data-ttu-id="a4855-122">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="a4855-122">Destination IP address</span></span></th>
<th><span data-ttu-id="a4855-123">Notas</span><span class="sxs-lookup"><span data-stu-id="a4855-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4855-124">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="a4855-124">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="a4855-125">Dirección IP pública del servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="a4855-125">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="a4855-126">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="a4855-126">Any</span></span></p></td>
<td><p><span data-ttu-id="a4855-127">Para conectividad de mensajería instantánea pública y federada con SIP</span><span class="sxs-lookup"><span data-stu-id="a4855-127">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="a4855-128">Resumen del firewall: conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="a4855-128">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4855-129">Función/protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="a4855-129">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="a4855-130">Dirección IP de origen</span><span class="sxs-lookup"><span data-stu-id="a4855-130">Source IP address</span></span></th>
<th><span data-ttu-id="a4855-131">Dirección IP de destino</span><span class="sxs-lookup"><span data-stu-id="a4855-131">Destination IP address</span></span></th>
<th><span data-ttu-id="a4855-132">Notas</span><span class="sxs-lookup"><span data-stu-id="a4855-132">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4855-133">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="a4855-133">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="a4855-134">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="a4855-134">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="a4855-135">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="a4855-135">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="a4855-136">Para la conectividad de mensajería instantánea pública y federada que usan SIP.</span><span class="sxs-lookup"><span data-stu-id="a4855-136">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4855-137">Acceso/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="a4855-137">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="a4855-138">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="a4855-138">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="a4855-139">Partners de conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="a4855-139">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="a4855-140">Para la conectividad de mensajería instantánea pública y federada que usan SIP.</span><span class="sxs-lookup"><span data-stu-id="a4855-140">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4855-141">Acceso/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="a4855-141">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="a4855-142">Clientes</span><span class="sxs-lookup"><span data-stu-id="a4855-142">Clients</span></span></p></td>
<td><p><span data-ttu-id="a4855-143">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="a4855-143">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="a4855-144">Tráfico SIP de cliente a servidor para el acceso de usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="a4855-144">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4855-145">A/V/RTP/TCP/50000-59.999 SESIONES</span><span class="sxs-lookup"><span data-stu-id="a4855-145">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="a4855-146">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="a4855-146">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="a4855-147">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="a4855-147">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="a4855-148">Se usa para sesiones de A/V con Windows Live Messenger si está configurada la conectividad de mensajería instantánea pública.</span><span class="sxs-lookup"><span data-stu-id="a4855-148">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4855-149">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="a4855-149">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="a4855-150">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="a4855-150">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="a4855-151">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="a4855-151">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="a4855-152">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="a4855-152">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4855-153">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="a4855-153">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="a4855-154">Clientes de Live Messenger</span><span class="sxs-lookup"><span data-stu-id="a4855-154">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="a4855-155">Interfaz de acceso al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="a4855-155">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="a4855-156">Necesario para la conectividad de mensajería instantánea pública con Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="a4855-156">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary---extensible-messaging-and-presence-protocol-xmpp"></a><span data-ttu-id="a4855-157">Resumen de Firewall: Protocolo de presencia y mensajería extensible (XMPP)</span><span class="sxs-lookup"><span data-stu-id="a4855-157">Firewall Summary - Extensible Messaging and Presence Protocol (XMPP)</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4855-158">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="a4855-158">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="a4855-159">Origen (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="a4855-159">Source (IP address)</span></span></th>
<th><span data-ttu-id="a4855-160">Destino (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="a4855-160">Destination (IP address)</span></span></th>
<th><span data-ttu-id="a4855-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4855-161">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4855-162">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="a4855-162">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="a4855-163">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="a4855-163">Any</span></span></p></td>
<td><p><span data-ttu-id="a4855-164">Dirección IP de la interfaz de servicio perimetral de Access</span><span class="sxs-lookup"><span data-stu-id="a4855-164">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="a4855-165">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="a4855-165">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="a4855-166">Permite la comunicación con el proxy XMPP del servidor perimetral de socios de XMPP</span><span class="sxs-lookup"><span data-stu-id="a4855-166">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4855-167">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="a4855-167">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="a4855-168">Dirección IP de la interfaz de servicio perimetral de Access</span><span class="sxs-lookup"><span data-stu-id="a4855-168">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="a4855-169">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="a4855-169">Any</span></span></p></td>
<td><p><span data-ttu-id="a4855-170">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="a4855-170">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="a4855-171">Permite la comunicación desde el proxy XMPP del servidor perimetral a socios XMPP de Federación</span><span class="sxs-lookup"><span data-stu-id="a4855-171">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4855-172">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="a4855-172">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="a4855-173">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="a4855-173">Any</span></span></p></td>
<td><p><span data-ttu-id="a4855-174">IP de la interfaz del servidor perimetral interno</span><span class="sxs-lookup"><span data-stu-id="a4855-174">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="a4855-175">Tráfico de XMPP interno de la puerta de enlace XMPP del servidor front-end o del grupo front-end al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="a4855-175">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a4855-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4855-176">See Also</span></span>


[<span data-ttu-id="a4855-177">Escenarios para el acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4855-177">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="a4855-178">Determinar los requisitos de los puertos y el firewall de A/V externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4855-178">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  


[<span data-ttu-id="a4855-179">Administrar socios federados XMPP para su organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4855-179">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="a4855-180"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a4855-180"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

