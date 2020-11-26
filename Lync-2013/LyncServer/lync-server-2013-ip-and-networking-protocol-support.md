---
title: 'Lync Server 2013: Compatibilidad con protocolo IP y de red'
description: 'Lync Server 2013: compatibilidad con IP y el protocolo de red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP and networking protocol support
ms:assetid: b0cffb10-3478-445c-89c7-8cb8b5027424
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412848(v=OCS.15)
ms:contentKeyID: 48185128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbd8022dd7197524334e0c70ea0ad875a30446de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426749"
---
# <a name="ip-and-networking-protocol-support-in-lync-server-2013"></a><span data-ttu-id="a85c2-103">Compatibilidad con protocolo IP y de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a85c2-103">IP and networking protocol support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a85c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a85c2-104">

<span> </span></span></span>

<span data-ttu-id="a85c2-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="a85c2-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="a85c2-106">Lync Server 2013 admite los siguientes protocolos de IP y de red:</span><span class="sxs-lookup"><span data-stu-id="a85c2-106">Lync Server 2013 supports the following IP and networking protocols:</span></span>

  - <span data-ttu-id="a85c2-107">**Protocolos IP.**</span><span class="sxs-lookup"><span data-stu-id="a85c2-107">**IP Protocols.**</span></span>   <span data-ttu-id="a85c2-108">Lync Server 2013 admite IP versión 4 (IPv4) o IP versión 6 (IPv6) para la red del servidor.</span><span class="sxs-lookup"><span data-stu-id="a85c2-108">Lync Server 2013 supports either IP version 4 (IPv4) or IP version 6 (IPv6) for the server network.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a85c2-109">Lync Server 2013 puede funcionar en una red con dos pilas IP habilitadas.</span><span class="sxs-lookup"><span data-stu-id="a85c2-109">Lync Server 2013 can function in a network with dual IP stack enabled.</span></span>

    
    </div>

  - <span data-ttu-id="a85c2-110">**Protocolos de transporte SIP.**</span><span class="sxs-lookup"><span data-stu-id="a85c2-110">**SIP Transport Protocols.**</span></span>   <span data-ttu-id="a85c2-111">De forma genérica, SIP puede usar al menos tres tipos de transporte: Protocolo de datagrama de usuario (UDP), protocolo de control de transmisión (TCP) y seguridad de nivel de transporte (TLS).</span><span class="sxs-lookup"><span data-stu-id="a85c2-111">Generically, SIP can use at least three transport types: User Datagram Protocol (UDP), Transmission Control Protocol (TCP), and Transport Layer Security (TLS).</span></span> <span data-ttu-id="a85c2-112">En la configuración de transporte SIP predeterminada, TLS se ejecuta sobre TCP.</span><span class="sxs-lookup"><span data-stu-id="a85c2-112">In the default SIP transport configuration, TLS runs over TCP.</span></span> <span data-ttu-id="a85c2-113">TLS se usa dentro de la red de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a85c2-113">TLS is used within the Lync Server 2013 network.</span></span> <span data-ttu-id="a85c2-114">En el extremo de la red, Lync Server 2013 puede interoperar sobre TCP.</span><span class="sxs-lookup"><span data-stu-id="a85c2-114">At the edge of the network, Lync Server 2013 can interoperate over TCP.</span></span> <span data-ttu-id="a85c2-115">Lync Server 2013 no admite UDP para el transporte SIP porque no cumple con los estándares mínimos de seguridad, confiabilidad y escalabilidad de las comunicaciones empresariales.</span><span class="sxs-lookup"><span data-stu-id="a85c2-115">Lync Server 2013 does not support UDP for SIP transport because it doesn’t meet the minimum standards for enterprise communications security, reliability, and scalability.</span></span> <span data-ttu-id="a85c2-116">Para obtener más información, vea el artículo del blog de NextHop, "to UDP, o not to UDP, que es la pregunta" en [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369) .</span><span class="sxs-lookup"><span data-stu-id="a85c2-116">For details, see the NextHop blog article, "To UDP, or not to UDP, that is the question," at [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a85c2-117">El contenido de los blogs y sus URL están sujetos a cambios sin previo aviso.</span><span class="sxs-lookup"><span data-stu-id="a85c2-117">The content of each blog and its URL are subject to change without notice.</span></span>

    
    <span data-ttu-id="a85c2-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a85c2-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

