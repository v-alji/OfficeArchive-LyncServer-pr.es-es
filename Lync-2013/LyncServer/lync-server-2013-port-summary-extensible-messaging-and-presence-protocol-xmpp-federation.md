---
title: 'Resumen de puertos: Federación protocolo de presencia y mensajería extensible (XMPP)'
description: 'Resumen de puertos: Federación protocolo de presencia y mensajería extensible (XMPP).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary -  Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 62e98fab-7add-4983-a3fa-dbe74e1c3849
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618371(v=OCS.15)
ms:contentKeyID: 49105658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9508bc8b9fbcca6fb6a37478def258a9fa52c373
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442806"
---
# <a name="port-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="f9d78-103">Resumen de puertos: Federación protocolo de presencia y mensajería extensible (XMPP) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9d78-103">Port summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9d78-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9d78-104">

<span> </span></span></span>

<span data-ttu-id="f9d78-105">_**Última modificación del tema:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="f9d78-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="f9d78-106">Los puertos y protocolos definidos para el proxy protocolo de presencia y mensajería extensible (XMPP) implementado en el servidor perimetral permiten las comunicaciones del socio XMPP federado hasta el servidor perimetral, y también permiten la comunicación desde el servidor perimetral al socio XMPP federado.</span><span class="sxs-lookup"><span data-stu-id="f9d78-106">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="f9d78-107">Una regla también se define en el Firewall de orientación interna desde el servidor front-end o el grupo front-end hasta el servidor perimetral o el grupo Edge.</span><span class="sxs-lookup"><span data-stu-id="f9d78-107">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="f9d78-108">Resumen de Firewall para el protocolo de presencia y mensajería extensible</span><span class="sxs-lookup"><span data-stu-id="f9d78-108">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9d78-109">Protocolo/TCP o UDP/puerto</span><span class="sxs-lookup"><span data-stu-id="f9d78-109">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="f9d78-110">Origen (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="f9d78-110">Source (IP address)</span></span></th>
<th><span data-ttu-id="f9d78-111">Destino (dirección IP)</span><span class="sxs-lookup"><span data-stu-id="f9d78-111">Destination (IP address)</span></span></th>
<th><span data-ttu-id="f9d78-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9d78-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9d78-113">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="f9d78-113">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="f9d78-114">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f9d78-114">Any</span></span></p></td>
<td><p><span data-ttu-id="f9d78-115">Dirección IP de la interfaz de servicio perimetral de Access</span><span class="sxs-lookup"><span data-stu-id="f9d78-115">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="f9d78-116">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="f9d78-116">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="f9d78-117">Permite la comunicación con el proxy XMPP del servidor perimetral de socios de XMPP</span><span class="sxs-lookup"><span data-stu-id="f9d78-117">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9d78-118">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="f9d78-118">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="f9d78-119">Dirección IP de la interfaz de servicio perimetral de Access</span><span class="sxs-lookup"><span data-stu-id="f9d78-119">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="f9d78-120">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f9d78-120">Any</span></span></p></td>
<td><p><span data-ttu-id="f9d78-121">Puerto de comunicación de servidor a servidor estándar para XMPP.</span><span class="sxs-lookup"><span data-stu-id="f9d78-121">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="f9d78-122">Permite la comunicación desde el proxy XMPP del servidor perimetral a socios XMPP de Federación</span><span class="sxs-lookup"><span data-stu-id="f9d78-122">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9d78-123">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="f9d78-123">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="f9d78-124">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="f9d78-124">Any</span></span></p></td>
<td><p><span data-ttu-id="f9d78-125">IP de la interfaz del servidor perimetral interno</span><span class="sxs-lookup"><span data-stu-id="f9d78-125">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="f9d78-126">Tráfico de XMPP interno de la puerta de enlace XMPP del servidor front-end o del grupo front-end al servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="f9d78-126">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f9d78-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9d78-127">See Also</span></span>


[<span data-ttu-id="f9d78-128">Configuración XMPP de ejemplo en Lync Server 2013 - Federación XMPP con Google Talk</span><span class="sxs-lookup"><span data-stu-id="f9d78-128">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="f9d78-129">Administrar socios federados XMPP para su organización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9d78-129">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="f9d78-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9d78-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

