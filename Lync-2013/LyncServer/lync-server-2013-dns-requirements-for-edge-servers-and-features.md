---
title: 'Lync Server 2013: requisitos de DNS para servidores perimetrales y características'
description: 'Lync Server 2013: requisitos de DNS para servidores perimetrales y características.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Edge Servers and features
ms:assetid: e3bf05c8-96fb-4dd2-acb1-f0d141c9e2ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721912(v=OCS.15)
ms:contentKeyID: 49733846
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9bcfd00080e765924eecc3138bc3d552ce331b63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399744"
---
# <a name="dns-requirements-for-edge-servers-and-features-in-lync-server-2013"></a><span data-ttu-id="d22e0-103">Requisitos de DNS para los servidores perimetrales y las características de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d22e0-103">DNS requirements for Edge Servers and features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d22e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d22e0-104">

<span> </span></span></span>

<span data-ttu-id="d22e0-105">_**Última modificación del tema:** 2014-04-08_</span><span class="sxs-lookup"><span data-stu-id="d22e0-105">_**Topic Last Modified:** 2014-04-08_</span></span>

<span data-ttu-id="d22e0-106">Los servidores perimetrales de Lync Server 2013, los grupos perimetrales y los proxies inversos tienen requisitos específicos para los registros del sistema de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="d22e0-106">Lync Server 2013 Edge Servers, Edge pools, and reverse proxies have specific requirements for Domain Name System (DNS) records.</span></span> <span data-ttu-id="d22e0-107">En Lync Server 2013 cuando se usan IPv4 e IPv6, debe planear los registros A y AAAA del host.</span><span class="sxs-lookup"><span data-stu-id="d22e0-107">In Lync Server 2013 when IPv4 and IPv6 are in use, you must plan for both host A and AAAA records.</span></span>

<span data-ttu-id="d22e0-108">Los temas siguientes definen el uso de registros DNS para la planificación de su implementación:</span><span class="sxs-lookup"><span data-stu-id="d22e0-108">The topics listed below define the use of DNS records for your deployment planning:</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d22e0-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d22e0-109">In This Section</span></span>

  - [<span data-ttu-id="d22e0-110">Resumen DNS - Servidor perimetral consolidado simple con dirección IP privada mediante NAT en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d22e0-110">DNS summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-dns-summary-single-consolidated-edge-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="d22e0-111">Resumen DNS - Servidor perimetral consolidado simple con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d22e0-111">DNS summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="d22e0-112">Resumen de DNS - Topologías perimetrales consolidadas escaladas, equilibrio de carga DNS con direcciones IP privadas con NAT en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d22e0-112">DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="d22e0-113">Resumen de DNS - Servidor perimetral consolidado ampliado, equilibrio de carga DNS con direcciones IP públicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d22e0-113">DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="d22e0-114">Resumen DNS - Servidor perimetral consolidado ampliado con equilibradores de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d22e0-114">DNS summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-with-hardware-load-balancers.md)

  - [<span data-ttu-id="d22e0-115">Resumen DNS - Proxy inverso en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d22e0-115">DNS summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-dns-summary-reverse-proxy.md)

  - [<span data-ttu-id="d22e0-116">Resumen DNS: SIP, Federación XMPP y mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d22e0-116">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-dns-summary-sip-xmpp-federation-and-public-instant-messaging.md)

<span data-ttu-id="d22e0-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d22e0-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

