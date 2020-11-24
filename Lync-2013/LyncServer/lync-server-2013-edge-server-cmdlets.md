---
title: 'Lync Server 2013: cmdlets de servidor perimetral'
description: 'Lync Server 2013: cmdlets de servidor perimetral.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edge Server cmdlets
ms:assetid: 1a5427f4-a0d1-4652-8135-91333158ffc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415635(v=OCS.15)
ms:contentKeyID: 48183534
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b73172331ddcde76672cccda682669f71dd7262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397896"
---
# <a name="edge-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="9eeca-103">Cmdlets de servidor perimetral en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9eeca-103">Edge Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9eeca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9eeca-104">

<span> </span></span></span>

<span data-ttu-id="9eeca-105">_**Última modificación del tema:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="9eeca-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="9eeca-106">Los servidores perimetrales le ofrecen una manera de ampliar las funciones de Microsoft Lync Server 2013 a las personas que no han iniciado sesión en su red interna.</span><span class="sxs-lookup"><span data-stu-id="9eeca-106">Edge Servers provide a way for you to extend the capabilities of Microsoft Lync Server 2013 to people who are not logged on to your internal network.</span></span> <span data-ttu-id="9eeca-107">Por ejemplo, si tiene usuarios remotos (autenticados) que inician sesión en Lync Server 2013 a través de Internet, en lugar de hacerlo a través de la red interna, tendrá que configurar un servidor perimetral que ejecute el servicio perimetral de acceso de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9eeca-107">For example, if you have remote users -- authenticated users who log on to Lync Server 2013 over the Internet rather than through the internal network -- you will need to set up an Edge Server that runs the Lync Server Access Edge service.</span></span> <span data-ttu-id="9eeca-108">Además, se necesitan servidores perimetrales si desea establecer la Federación con otra organización o si desea conceder a los usuarios el derecho de comunicarse con las personas que tienen cuentas con un servicio de mensajería instantánea pública, como Yahoo \! , AOL o MSN.</span><span class="sxs-lookup"><span data-stu-id="9eeca-108">Additionally, Edge Servers are required if you want to establish federation with another organization or if you want to give your users the right to communicate with people who have accounts with a public instant messaging service such as Yahoo\!, AOL, or MSN.</span></span>

<div>


> [!IMPORTANT]
> <UL>
> <LI>
> <P><span data-ttu-id="9eeca-109">A partir del 1 de septiembre de 2012, la licencia de suscripción de usuario de conectividad de mensajería instantánea pública de Microsoft Lync ("PIC USL") ya no está disponible para la compra de contratos nuevos o de renovación.</span><span class="sxs-lookup"><span data-stu-id="9eeca-109">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="9eeca-110">Los clientes con licencias activas podrán seguir federando a Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9eeca-110">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="9eeca-111">Messenger hasta que se cierre la fecha del servicio.</span><span class="sxs-lookup"><span data-stu-id="9eeca-111">Messenger until the service shut down date.</span></span> <span data-ttu-id="9eeca-112">Una fecha de fin de vida de junio de 2014 para AOL y Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9eeca-112">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="9eeca-113">ha sido anunciado.</span><span class="sxs-lookup"><span data-stu-id="9eeca-113">has been announced.</span></span> <span data-ttu-id="9eeca-114">Para obtener más información, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">compatibilidad de la conectividad de mensajería instantánea pública en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9eeca-114">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="9eeca-115">El PIC USL es una licencia por usuario por mes de suscripción que es necesaria para que Lync Server o Office Communications Server se federe con Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9eeca-115">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="9eeca-116">Mensajería.</span><span class="sxs-lookup"><span data-stu-id="9eeca-116">Messenger.</span></span> <span data-ttu-id="9eeca-117">La capacidad de Microsoft para proporcionar este servicio está supeditada al soporte de Yahoo!, el contrato subyacente para el que se está pospuesto.</span><span class="sxs-lookup"><span data-stu-id="9eeca-117">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="9eeca-118">Más que nunca, Lync es una herramienta eficaz para la conexión entre organizaciones y con personas de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="9eeca-118">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="9eeca-119">La Federación con Windows Live Messenger no requiere licencias adicionales para usuarios y dispositivos más allá de la CAL de Lync Standard.</span><span class="sxs-lookup"><span data-stu-id="9eeca-119">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="9eeca-120">La Federación de Skype se agrega a esta lista, lo que permite a los usuarios de Lync llegar a cientos de millones de personas con la mensajería instantánea y la voz.</span><span class="sxs-lookup"><span data-stu-id="9eeca-120">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

<div>

## <a name="edge-server-cmdlets"></a><span data-ttu-id="9eeca-121">Cmdlets de servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="9eeca-121">Edge Server Cmdlets</span></span>

<span data-ttu-id="9eeca-122">A continuación se muestra una lista de cmdlets que se relacionan directamente con la administración de servidores perimetrales:</span><span class="sxs-lookup"><span data-stu-id="9eeca-122">The following is a list of cmdlets that relate directly to managing Edge Servers:</span></span>

<span data-ttu-id="9eeca-123">**Servidor perimetral**</span><span class="sxs-lookup"><span data-stu-id="9eeca-123">**Edge Server**</span></span>

  - <span></span>  
    <span data-ttu-id="9eeca-124">[Get-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9eeca-124">[Get-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="9eeca-125">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9eeca-125">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="9eeca-126">[Get-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9eeca-126">[Get-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="9eeca-127">[Nuevo: CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9eeca-127">[New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="9eeca-128">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9eeca-128">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="9eeca-129">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9eeca-129">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="9eeca-130">[Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9eeca-130">[Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="9eeca-131">[Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9eeca-131">[Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9eeca-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9eeca-132">See Also</span></span>


[<span data-ttu-id="9eeca-133">Blog de Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeca-133">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="9eeca-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9eeca-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

