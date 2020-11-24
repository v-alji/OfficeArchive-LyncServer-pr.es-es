---
title: 'Lync Server 2013: Componentes necesarios para el acceso de usuarios externos'
description: 'Lync Server 2013: componentes necesarios para el acceso de usuarios externos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components required for external user access
ms:assetid: 2d0f9817-14e7-4109-95dc-62420e3c29e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425779(v=OCS.15)
ms:contentKeyID: 48183711
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d75ef0c7f2000353a35acefa0b177c90bdcc879b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398531"
---
# <a name="components-required-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="172a9-103">Componentes necesarios para el acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="172a9-103">Components required for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="172a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="172a9-104">

<span> </span></span></span>

<span data-ttu-id="172a9-105">_**Última modificación del tema:** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="172a9-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="172a9-106">La mayoría de los componentes perimetrales se implementan en una red perimetral.</span><span class="sxs-lookup"><span data-stu-id="172a9-106">Most Edge components are deployed in a perimeter network.</span></span> <span data-ttu-id="172a9-107">Los siguientes componentes forman la topología perimetral de la red perimetral.</span><span class="sxs-lookup"><span data-stu-id="172a9-107">The following components make up the edge topology of the perimeter network.</span></span> <span data-ttu-id="172a9-108">Excepto donde se indique lo contrario, los componentes forman parte de los [escenarios para el acceso de usuarios externos en Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) y en la red perimetral.</span><span class="sxs-lookup"><span data-stu-id="172a9-108">Except where noted, the components are part of the [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) and are in the perimeter network.</span></span> <span data-ttu-id="172a9-109">Los componentes perimetrales engloban los siguientes:</span><span class="sxs-lookup"><span data-stu-id="172a9-109">Edge components include the following:</span></span>

  - <span data-ttu-id="172a9-110">Edge Servers</span><span class="sxs-lookup"><span data-stu-id="172a9-110">Edge Servers</span></span>

  - <span data-ttu-id="172a9-111">Reverse proxies</span><span class="sxs-lookup"><span data-stu-id="172a9-111">Reverse proxies</span></span>

  - <span data-ttu-id="172a9-112">Firewalls</span><span class="sxs-lookup"><span data-stu-id="172a9-112">Firewalls</span></span>

  - <span data-ttu-id="172a9-113">Directores (opcional y, lógicamente, ubicado en la red interna)</span><span class="sxs-lookup"><span data-stu-id="172a9-113">Directors (optional, and logically located on the internal network)</span></span>

  - <span data-ttu-id="172a9-114">Equilibrio de carga para topologías perimetrales escaladas (equilibrio de carga de DNS o un equilibrador de carga de hardware)</span><span class="sxs-lookup"><span data-stu-id="172a9-114">Load balancing for Scaled Edge Topologies (either DNS load balancing or a hardware load balancer)</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="172a9-p102">No se admite el uso del equilibrio de carga de DNS en una interfaz y del equilibrio de carga de hardware en otra. Necesita utilizar el equilibrio de carga de hardware o de DNS en ambas interfaces.</span><span class="sxs-lookup"><span data-stu-id="172a9-p102">Using DNS load balancing on one interface and hardware load balancing on the other is not supported. You must use hardware load balancing for both interfaces or DNS load balancing for both.</span></span>

    
    </div>

<div>

## <a name="edge-servers"></a><span data-ttu-id="172a9-117">Servidores perimetrales</span><span class="sxs-lookup"><span data-stu-id="172a9-117">Edge Servers</span></span>

<span data-ttu-id="172a9-118">Los servidores perimetrales envían y reciben tráfico de red para los servicios ofrecidos por los usuarios externos en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="172a9-118">The Edge Servers send and receive network traffic for the services offered by internal deployment by external users.</span></span> <span data-ttu-id="172a9-119">El servidor perimetral ejecuta los siguientes servicios:</span><span class="sxs-lookup"><span data-stu-id="172a9-119">The Edge Server runs the following services:</span></span>

  - <span data-ttu-id="172a9-120">**Servicio perimetral de acceso**   El servicio perimetral de acceso proporciona un único punto de conexión de confianza para el tráfico de protocolo de inicio de sesión entrante y saliente (SIP).</span><span class="sxs-lookup"><span data-stu-id="172a9-120">**Access Edge service**   The Access Edge service provides a single, trusted connection point for both outbound and inbound Session Initiation Protocol (SIP) traffic.</span></span>

  - <span data-ttu-id="172a9-121">**Servicio perimetral de conferencias web**   El servicio perimetral de conferencias web permite a los usuarios externos unirse a reuniones hospedadas en la implementación interna de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="172a9-121">**Web Conferencing Edge service**   The Web Conferencing Edge service enables external users to join meetings that are hosted on your internal Lync Server 2013 deployment.</span></span>

  - <span data-ttu-id="172a9-122">**Servicio perimetral A/V**   El servicio Edge de A/V hace que el audio, el vídeo, el uso compartido de aplicaciones y la transferencia de archivos estén disponibles para los usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="172a9-122">**A/V Edge service**   The A/V Edge service makes audio, video, application sharing, and file transfer available to external users.</span></span> <span data-ttu-id="172a9-123">Los usuarios pueden agregar audio y vídeo a las reuniones que incluyen participantes externos, y pueden comunicarse con audio o video directamente con un usuario externo en sesiones punto a punto.</span><span class="sxs-lookup"><span data-stu-id="172a9-123">Your users can add audio and video to meetings that include external participants, and they can communicate using audio and/or video directly with an external user in point-to-point sessions.</span></span> <span data-ttu-id="172a9-124">El servicio perimetral A/V también proporciona compatibilidad con el uso compartido de escritorio y la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="172a9-124">The A/V Edge service also provides support for desktop sharing and file transfer.</span></span>

  - <span data-ttu-id="172a9-125">**Servicio de proxy XMPP**   El servicio de proxy XMPP acepta y envía mensajes de protocolo de presencia y mensajería extensible (XMPP) a los socios de XMPP federados configurados.</span><span class="sxs-lookup"><span data-stu-id="172a9-125">**XMPP Proxy service**   The XMPP Proxy service accepts and sends extensible messaging and presence protocol (XMPP) messages to and from configured XMPP Federated partners.</span></span>

<span data-ttu-id="172a9-126">Los usuarios externos autorizados pueden tener acceso a los servidores perimetrales para conectarse a la implementación interna de Lync Server 2013, pero los servidores perimetrales no proporcionan medios para ningún otro tipo de acceso a la red interna.</span><span class="sxs-lookup"><span data-stu-id="172a9-126">Authorized external users can access the Edge Servers in order to connect to your internal Lync Server 2013 deployment, but the Edge Servers do not provide a means for any other access to the internal network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="172a9-127">Los servidores perimetrales se implementan para proporcionar conexiones para clientes de Lync habilitados y otros servidores Microsoft Edge (como en los escenarios de Federación).</span><span class="sxs-lookup"><span data-stu-id="172a9-127">Edge servers are deployed to provide connections for enabled Lync clients and other Microsoft Edge servers (as in federation scenarios).</span></span> <span data-ttu-id="172a9-128">No están diseñados para permitir conexiones de otros tipos de clientes o servidores de punto final.</span><span class="sxs-lookup"><span data-stu-id="172a9-128">They are not designed to allow connections from other end point client or server types.</span></span> <span data-ttu-id="172a9-129">El servidor de puerta de enlace XMPP puede implementarse para permitir conexiones con socios XMPP configurados.</span><span class="sxs-lookup"><span data-stu-id="172a9-129">The XMPP Gateway server can be deployed to allow connections with configured XMPP partners.</span></span> <span data-ttu-id="172a9-130">El servidor perimetral y la puerta de enlace XMPP solo admiten conexiones de punto final de estos tipos de Federación y cliente.</span><span class="sxs-lookup"><span data-stu-id="172a9-130">The Edge server and XMPP Gateway can only support end point connections from these client and federation types.</span></span>



</div>

</div>

<div>

## <a name="reverse-proxy"></a><span data-ttu-id="172a9-131">Proxy inverso</span><span class="sxs-lookup"><span data-stu-id="172a9-131">Reverse Proxy</span></span>

<span data-ttu-id="172a9-132">El proxy inverso es necesario para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="172a9-132">The reverse proxy is required for the following:</span></span>

  - <span data-ttu-id="172a9-133">Para permitir que los usuarios se conecten a reuniones o conferencias de acceso telefónico local con direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="172a9-133">To allow users to connect to meetings or dial-in conferences using simple URLs</span></span>

  - <span data-ttu-id="172a9-134">Para permitir que los usuarios externos descarguen contenido de la reunión</span><span class="sxs-lookup"><span data-stu-id="172a9-134">To enable external users to download meeting content</span></span>

  - <span data-ttu-id="172a9-135">Para permitir a los usuarios externos expandir grupos de distribución</span><span class="sxs-lookup"><span data-stu-id="172a9-135">To enable external users to expand distribution groups</span></span>

  - <span data-ttu-id="172a9-136">Para permitir que el usuario obtenga un certificado basado en el usuario para la autenticación basada en certificados de cliente</span><span class="sxs-lookup"><span data-stu-id="172a9-136">To allow the user to obtain a user-based certificate for client certificate based authentication</span></span>

  - <span data-ttu-id="172a9-137">Para permitir que los usuarios remotos descarguen archivos desde el servidor de la libreta de direcciones o para enviar consultas al servicio de consulta Web de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="172a9-137">To enable remote users to download files from the Address Book Server or to submit queries to the Address Book Web Query service</span></span>

  - <span data-ttu-id="172a9-138">Para permitir que los usuarios remotos obtengan actualizaciones del software del cliente y del dispositivo</span><span class="sxs-lookup"><span data-stu-id="172a9-138">To enable remote users to obtain updates to client and device software</span></span>

  - <span data-ttu-id="172a9-139">Para habilitar dispositivos móviles para detectar automáticamente los servidores front-end que ofrecen servicios de movilidad</span><span class="sxs-lookup"><span data-stu-id="172a9-139">To enable mobile devices to automatically discover Front End Servers offering mobility services</span></span>

  - <span data-ttu-id="172a9-140">Para habilitar las notificaciones de inserción en dispositivos móviles desde Microsoft 365, Office 365 o los servicios de notificaciones push de Apple</span><span class="sxs-lookup"><span data-stu-id="172a9-140">To enable push notifications to mobile devices from the Microsoft 365, Office 365, or Apple push notification services</span></span>

<span data-ttu-id="172a9-141">Para obtener más información relacionada con los proxies inversos y los requisitos que deben cumplir los proxies inversos, consulte los detalles de [los requisitos de configuración para el proxy inverso en Lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="172a9-141">For additional information related to reverse proxies and the requirements that reverse proxies must meet, see the details in [Configuration requirements for reverse proxy in Lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="172a9-142">Los usuarios externos no necesitan una conexión de red privada virtual (VPN) a la organización para poder participar en las comunicaciones con Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="172a9-142">External users do not need a virtual private network (VPN) connection to your organization in order to participate in communications using Lync Server 2013.</span></span> <span data-ttu-id="172a9-143">Si ha implementado tecnología VPN en su organización y los usuarios usan la VPN para Lync, el tráfico multimedia (como las videoconferencias) puede verse afectado negativamente.</span><span class="sxs-lookup"><span data-stu-id="172a9-143">If you have implemented VPN technology in your organization and your users use the VPN for Lync, media traffic (such as video conferencing) can be adversely affected.</span></span> <span data-ttu-id="172a9-144">Debe considerar proporcionar un medio para que el tráfico de medios se conecte directamente con el servicio perimetral de AV y omita la red privada virtual.</span><span class="sxs-lookup"><span data-stu-id="172a9-144">You should consider providing a means for media traffic to connect to the AV Edge service directly and bypass the VPN.</span></span> <span data-ttu-id="172a9-145">Para obtener más información, vea el artículo del blog de NextHop, "habilitar medios de Lync para eludir un túnel VPN" en <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A> .</span><span class="sxs-lookup"><span data-stu-id="172a9-145">For details, see the NextHop Blog article, “Enabling Lync Media to Bypass a VPN Tunnel,” at <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A>.</span></span>



</div>

</div>

<div>

## <a name="firewall"></a><span data-ttu-id="172a9-146">Firewall</span><span class="sxs-lookup"><span data-stu-id="172a9-146">Firewall</span></span>

<span data-ttu-id="172a9-147">Puede implementar su topología perimetral solo con un firewall externo o con firewalls externos e internos.</span><span class="sxs-lookup"><span data-stu-id="172a9-147">You can deploy your edge topology with only an external firewall or both external and internal firewalls.</span></span> <span data-ttu-id="172a9-148">Las arquitecturas de escenario incluyen dos firewalls.</span><span class="sxs-lookup"><span data-stu-id="172a9-148">The scenario architectures include two firewalls.</span></span> <span data-ttu-id="172a9-149">El uso de dos firewalls es el método recomendado, ya que garantiza el enrutamiento estricto desde un perímetro de red al otro y protege la implementación interna detrás de dos niveles de Firewall.</span><span class="sxs-lookup"><span data-stu-id="172a9-149">Using two firewalls is the recommended approach because it ensures strict routing from one network edge to the other, and it protects your internal deployment behind two levels of firewall.</span></span>

</div>

<div>

## <a name="director"></a><span data-ttu-id="172a9-150">Director</span><span class="sxs-lookup"><span data-stu-id="172a9-150">Director</span></span>

<span data-ttu-id="172a9-151">Un director es un rol de servidor independiente y opcional de Lync Server 2013 que no aloja cuentas de usuario o proporciona servicios de presencia o de conferencia.</span><span class="sxs-lookup"><span data-stu-id="172a9-151">A Director is a separate, optional server role in Lync Server 2013 that does not home user accounts, or provide presence or conferencing services.</span></span> <span data-ttu-id="172a9-152">Actúa como un servidor interno del próximo salto al que un servidor perimetral enruta el tráfico SIP entrante destinado a los servidores internos.</span><span class="sxs-lookup"><span data-stu-id="172a9-152">It serves as an internal next hop server to which an Edge Server routes inbound SIP traffic destined for internal servers.</span></span> <span data-ttu-id="172a9-153">El director preautentica las solicitudes entrantes y las redirige al grupo de servidores o al grupo de servidores principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="172a9-153">The Director preauthenticates inbound requests and redirects them to the user’s home pool or server.</span></span> <span data-ttu-id="172a9-154">Al autenticar en el director, puede colocar solicitudes de cuentas de usuario desconocidas para la implementación.</span><span class="sxs-lookup"><span data-stu-id="172a9-154">By preauthenticating at the Director, you can drop requests from user accounts that are unknown to the deployment.</span></span>

<span data-ttu-id="172a9-155">Un director ayuda a aislar servidores Standard Edition y servidores de aplicaciones para el usuario de las agrupaciones front end de Enterprise Edition de tráfico malintencionado, como ataques de denegación de servicio (DoS).</span><span class="sxs-lookup"><span data-stu-id="172a9-155">A Director helps insulate Standard Edition servers and Front End Servers in Enterprise Edition Front End pools from malicious traffic such as denial-of-service (DoS) attacks.</span></span> <span data-ttu-id="172a9-156">Si la red se inunda con tráfico externo no válido en tal ataque, el tráfico termina en el director.</span><span class="sxs-lookup"><span data-stu-id="172a9-156">If the network is flooded with invalid external traffic in such an attack, the traffic ends at the Director.</span></span> <span data-ttu-id="172a9-157">Para obtener más información sobre el uso de los directores, consulte [escenarios del Director de Lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span><span class="sxs-lookup"><span data-stu-id="172a9-157">For details about the use of Directors, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="172a9-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="172a9-158">See Also</span></span>


[<span data-ttu-id="172a9-159">Requisitos del equilibrador de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="172a9-159">Hardware load balancer requirements for Lync Server 2013</span></span>](lync-server-2013-hardware-load-balancer-requirements.md)  
  

<span data-ttu-id="172a9-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="172a9-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

