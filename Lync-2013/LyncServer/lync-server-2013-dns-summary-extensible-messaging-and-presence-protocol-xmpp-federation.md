---
title: 'Resumen de DNS: Federación protocolo de presencia y mensajería extensible (XMPP)'
description: 'Resumen de DNS: Federación protocolo de presencia y mensajería extensible (XMPP).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 0f720a2a-8ab5-43cc-882a-ab595ed3cec7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618368(v=OCS.15)
ms:contentKeyID: 49105655
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b8088e30c93faa52c575fefa97e572ed20b6ad9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437738"
---
# <a name="dns-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="41e71-103">Resumen de DNS: Federación protocolo de presencia y mensajería extensible (XMPP) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41e71-103">DNS summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41e71-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41e71-104">

<span> </span></span></span>

<span data-ttu-id="41e71-105">_**Última modificación del tema:** 2014-04-08_</span><span class="sxs-lookup"><span data-stu-id="41e71-105">_**Topic Last Modified:** 2014-04-08_</span></span>

<span data-ttu-id="41e71-106">Para configurar el protocolo de presencia y mensajería extensible (XMPP) para su implementación, debe crear dos registros del sistema de nombres de dominio (DNS) en un servidor DNS externo que resuelva los registros para el servicio perimetral de acceso de su servidor perimetral o de grupo perimetral.</span><span class="sxs-lookup"><span data-stu-id="41e71-106">To configure extensible messaging and presence protocol (XMPP) for your deployment, you create two Domain Name System (DNS) records in an external DNS server that will resolve the records to the Access Edge service of your Edge Server or Edge pool.</span></span>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="41e71-107">Resumen de DNS para el protocolo de presencia y mensajería extensible</span><span class="sxs-lookup"><span data-stu-id="41e71-107">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41e71-108">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="41e71-108">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="41e71-109">FQDN</span><span class="sxs-lookup"><span data-stu-id="41e71-109">FQDN</span></span></th>
<th><span data-ttu-id="41e71-110">Dirección IP/registro de host FQDN</span><span class="sxs-lookup"><span data-stu-id="41e71-110">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="41e71-111">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="41e71-111">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41e71-112">DNS/SRV/5269 externo</span><span class="sxs-lookup"><span data-stu-id="41e71-112">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="41e71-113">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="41e71-113">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="41e71-114">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="41e71-114">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="41e71-115">Interfaz externa de proxy XMPP en el servicio perimetral de acceso o grupo perimetral. Repita el procedimiento según sea necesario para todos los dominios SIP internos con los usuarios habilitados para Lync donde se permite el contacto con los contactos XMPP mediante la configuración de la Directiva de acceso externo a través de una directiva global, una directiva de sitio donde se encuentra el usuario o la Directiva de usuario para el usuario habilitado para Lync.</span><span class="sxs-lookup"><span data-stu-id="41e71-115">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="41e71-116">También se debe configurar un dominio XMPP permitido en la Directiva del socio XMPP federado.</span><span class="sxs-lookup"><span data-stu-id="41e71-116">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="41e71-117">Vea temas en <strong>vea también</strong> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="41e71-117">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41e71-118">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="41e71-118">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="41e71-119">xmpp.contoso.com (por ejemplo)</span><span class="sxs-lookup"><span data-stu-id="41e71-119">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="41e71-120">Dirección IP del servicio perimetral de acceso en el servidor perimetral o grupo perimetral que aloja el proxy XMPP</span><span class="sxs-lookup"><span data-stu-id="41e71-120">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="41e71-121">Señala el servicio perimetral de Access o el grupo de límites que alberga el servicio de proxy XMPP.</span><span class="sxs-lookup"><span data-stu-id="41e71-121">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="41e71-122">Normalmente, el registro SRV que cree apuntará a este registro de host (A o AAAA).</span><span class="sxs-lookup"><span data-stu-id="41e71-122">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="41e71-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="41e71-123">See Also</span></span>


[<span data-ttu-id="41e71-124">Configurar la federación XMPP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41e71-124">Setting up XMPP federation in Lync Server 2013</span></span>](lync-server-2013-setting-up-xmpp-federation.md)  


[<span data-ttu-id="41e71-125">Determinar los requisitos DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41e71-125">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  
  

<span data-ttu-id="41e71-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41e71-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

