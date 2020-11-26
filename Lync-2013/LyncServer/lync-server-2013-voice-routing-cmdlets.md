---
title: 'Lync Server 2013: cmdlets de enrutamiento de voz'
description: 'Lync Server 2013: cmdlets de enrutamiento de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Voice routing cmdlets
ms:assetid: 8f05b25e-cc62-4d85-a5d8-4ed56f28dfbf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416494(v=OCS.15)
ms:contentKeyID: 48184821
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b895eb84bccea6fcb014e61d5609b45c8c14d4cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440384"
---
# <a name="voice-routing-cmdlets-in-lync-server-2013"></a><span data-ttu-id="1bf45-103">Cmdlets de enrutamiento de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1bf45-103">Voice routing cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1bf45-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1bf45-104">

<span> </span></span></span>

<span data-ttu-id="1bf45-105">_**Última modificación del tema:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="1bf45-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="1bf45-106">Las rutas de voz contienen instrucciones que indican a Microsoft Lync Server 2013 cómo enrutar las llamadas de los usuarios de voz de empresa a números de teléfono de la red de telefonía pública conmutada (RTC) o de una central de conmutación (PBX).</span><span class="sxs-lookup"><span data-stu-id="1bf45-106">Voice routes contain instructions that tell Microsoft Lync Server 2013 how to route calls from Enterprise Voice users to phone numbers on the public switched telephone network (PSTN) or a private branch exchange (PBX).</span></span>

<div>

## <a name="voice-routing-cmdlets"></a><span data-ttu-id="1bf45-107">Cmdlets de enrutamiento de voz</span><span class="sxs-lookup"><span data-stu-id="1bf45-107">Voice Routing Cmdlets</span></span>

<span data-ttu-id="1bf45-108">Use los siguientes cmdlets para configurar las rutas de voz.</span><span class="sxs-lookup"><span data-stu-id="1bf45-108">Use the following cmdlets to configure voice routes.</span></span>

<span data-ttu-id="1bf45-109">**Enrutamiento de voz**</span><span class="sxs-lookup"><span data-stu-id="1bf45-109">**Voice Routing**</span></span>

  - <span></span>  
    <span data-ttu-id="1bf45-110">[Get-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg425851(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-110">[Get-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg425851(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="1bf45-111">[Nuevo: CsRoutingConfiguration](https://technet.microsoft.com/library/Gg399056(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-111">[New-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg399056(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="1bf45-112">[Remove-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg398643(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-112">[Remove-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg398643(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="1bf45-113">[Set-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg412811(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-113">[Set-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg412811(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="1bf45-114">[Get-CsVoiceRoute](https://technet.microsoft.com/library/Gg425926(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-114">[Get-CsVoiceRoute](https://technet.microsoft.com/library/Gg425926(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="1bf45-115">[Nuevo: CsVoiceRoute](https://technet.microsoft.com/library/Gg398197(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-115">[New-CsVoiceRoute](https://technet.microsoft.com/library/Gg398197(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="1bf45-116">[Remove-CsVoiceRoute](https://technet.microsoft.com/library/Gg398468(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-116">[Remove-CsVoiceRoute](https://technet.microsoft.com/library/Gg398468(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="1bf45-117">[Set-CsVoiceRoute](https://technet.microsoft.com/library/Gg412893(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-117">[Set-CsVoiceRoute](https://technet.microsoft.com/library/Gg412893(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="1bf45-118">[Prueba-CsVoiceRoute](https://technet.microsoft.com/library/Gg425873(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-118">[Test-CsVoiceRoute](https://technet.microsoft.com/library/Gg425873(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="1bf45-119">[Get-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ204940(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-119">[Get-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ204940(v=OCS.15))</span></span>

  - <span data-ttu-id="1bf45-120">[Grant-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ205141(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-120">[Grant-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ205141(v=OCS.15))</span></span>

  - <span data-ttu-id="1bf45-121">[New-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ205135(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-121">[New-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ205135(v=OCS.15))</span></span>

  - <span data-ttu-id="1bf45-122">[Remove-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ204799(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-122">[Remove-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ204799(v=OCS.15))</span></span>

  - <span data-ttu-id="1bf45-123">[Set-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ205313(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-123">[Set-CsVoiceRoutingPolicy](https://technet.microsoft.com/library/JJ205313(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="1bf45-124">[Get-CsPstnUsage](https://technet.microsoft.com/library/Gg412734(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-124">[Get-CsPstnUsage](https://technet.microsoft.com/library/Gg412734(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="1bf45-125">[Set-CsPstnUsage](https://technet.microsoft.com/library/Gg399069(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1bf45-125">[Set-CsPstnUsage](https://technet.microsoft.com/library/Gg399069(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1bf45-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bf45-126">See Also</span></span>


[<span data-ttu-id="1bf45-127">Cmdlets de telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1bf45-127">Enterprise Voice cmdlets in Lync Server 2013</span></span>](lync-server-2013-enterprise-voice-cmdlets.md)  
[<span data-ttu-id="1bf45-128">Cmdlets de conectividad RTC en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1bf45-128">PSTN connectivity cmdlets in Lync Server 2013</span></span>](lync-server-2013-pstn-connectivity-cmdlets.md)  


[<span data-ttu-id="1bf45-129">Blog de Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="1bf45-129">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="1bf45-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1bf45-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

