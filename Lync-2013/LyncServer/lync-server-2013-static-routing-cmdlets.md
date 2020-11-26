---
title: 'Lync Server 2013: cmdlets de enrutamiento estáticos'
description: 'Lync Server 2013: cmdlets de enrutamiento estáticos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Static routing cmdlets
ms:assetid: 71d5e0cd-8412-4383-818a-95b851a4da4b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416492(v=OCS.15)
ms:contentKeyID: 48184496
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33fd251f63111cebb9297287252e666a7e10f0e1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423690"
---
# <a name="static-routing-cmdlets-in-lync-server-2013"></a><span data-ttu-id="bbf21-103">Cmdlets de enrutamiento estático en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bbf21-103">Static routing cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bbf21-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bbf21-104">

<span> </span></span></span>

<span data-ttu-id="bbf21-105">_**Última modificación del tema:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="bbf21-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="bbf21-106">Con las rutas estáticas, los administradores pueden predeterminar las rutas de red tomadas por los mensajes SIP.</span><span class="sxs-lookup"><span data-stu-id="bbf21-106">With static routes, administrators can predetermine the network routes taken by SIP messages.</span></span> <span data-ttu-id="bbf21-107">Cuando un servidor recibe un mensaje, el servidor comprueba la dirección del mensaje y, a continuación, reenvía el mensaje al servidor del próximo salto preconfigurado por un administrador.</span><span class="sxs-lookup"><span data-stu-id="bbf21-107">When a message is received by a server, the server checks the message address and then forwards the message to the next hop server preconfigured by an administrator.</span></span> <span data-ttu-id="bbf21-108">Si se configuran correctamente, las rutas estáticas ayudan a asegurar la entrega precisa y puntual de los mensajes sin apenas sobrecargar los servidores.</span><span class="sxs-lookup"><span data-stu-id="bbf21-108">If configured correctly, static routes help ensure timely, and accurate, delivery of messages, and with minimal overheard placed on servers.</span></span>

<div>

## <a name="static-routing-cmdlets"></a><span data-ttu-id="bbf21-109">Cmdlets de enrutamiento estático</span><span class="sxs-lookup"><span data-stu-id="bbf21-109">Static Routing Cmdlets</span></span>

<span data-ttu-id="bbf21-110">A menos que el personal de soporte técnico de Microsoft lo indique de otra manera, las rutas estáticas configuradas para Microsoft Lync Server 2013 deberían crearse con el cmdlet [New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="bbf21-110">Unless otherwise instructed by Microsoft support personnel, static routes configured for Microsoft Lync Server 2013 should be created using the [New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15)) cmdlet.</span></span> <span data-ttu-id="bbf21-111">Después de crear una ruta, puede usar los cmdlets de CsStaticRoutingConfiguration para agregar esa ruta a una colección de enrutamiento estático.</span><span class="sxs-lookup"><span data-stu-id="bbf21-111">After a route has been created, you can then use the CsStaticRoutingConfiguration cmdlets to add that route to a static routing collection.</span></span>

<span data-ttu-id="bbf21-112">**Enrutamiento estático**</span><span class="sxs-lookup"><span data-stu-id="bbf21-112">**Static Routing**</span></span>

  - <span></span>  
    <span data-ttu-id="bbf21-113">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-113">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="bbf21-114">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-114">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="bbf21-115">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-115">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="bbf21-116">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-116">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-117">[New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-117">[New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-118">[Get-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-118">[Get-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="bbf21-119">[Nuevo: CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-119">[New-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="bbf21-120">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-120">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="bbf21-121">[Set-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-121">[Set-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-122">[Nuevo: CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-122">[New-CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-123">[Nuevo: CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-123">[New-CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-124">[Nuevo: CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-124">[New-CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-125">[Nuevo: CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-125">[New-CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-126">[Nuevo: CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-126">[New-CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-127">[Nuevo: CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-127">[New-CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-128">[Nuevo: CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-128">[New-CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="bbf21-129">[Nuevo: CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="bbf21-129">[New-CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bbf21-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbf21-130">See Also</span></span>


[<span data-ttu-id="bbf21-131">Blog de Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="bbf21-131">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="bbf21-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bbf21-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

