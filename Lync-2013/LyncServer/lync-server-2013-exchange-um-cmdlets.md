---
title: 'Lync Server 2013: cmdlets de mensajería unificada de Exchange'
description: 'Lync Server 2013: cmdlets de mensajería unificada de Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exchange UM cmdlets
ms:assetid: 32922b9f-590d-41cc-ba57-9ed5f1caa814
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415642(v=OCS.15)
ms:contentKeyID: 48183786
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 272e791969508b488efb0aaa2db10fb645ddd81c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428401"
---
# <a name="exchange-um-cmdlets-in-lync-server-2013"></a><span data-ttu-id="e7172-103">Cmdlets de mensajería unificada de Exchange en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7172-103">Exchange UM cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e7172-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e7172-104">

<span> </span></span></span>

<span data-ttu-id="e7172-105">_**Última modificación del tema:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="e7172-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="e7172-106">Microsoft Lync Server 2013 funciona junto con la mensajería unificada de Exchange (UM) para implementar el acceso de operador automático y suscriptor para el correo de voz hospedado.</span><span class="sxs-lookup"><span data-stu-id="e7172-106">Microsoft Lync Server 2013 works together with Exchange Unified Messaging (UM) to implement Auto Attendant and Subscriber Access for hosted voice mail.</span></span> <span data-ttu-id="e7172-107">Estas características se pueden administrar mediante cmdlets en el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e7172-107">These features can be managed through cmdlets in the Lync Server Management Shell.</span></span>

<div>

## <a name="exchange-um-cmdlets"></a><span data-ttu-id="e7172-108">Cmdlets de mensajería unificada de Exchange</span><span class="sxs-lookup"><span data-stu-id="e7172-108">Exchange UM Cmdlets</span></span>

<span data-ttu-id="e7172-109">Los siguientes cmdlets se pueden usar para administrar la mensajería unificada de Exchange</span><span class="sxs-lookup"><span data-stu-id="e7172-109">The following cmdlets can be used to manage Exchange UM</span></span>

<span data-ttu-id="e7172-110">**Mensajería unificada de Exchange**</span><span class="sxs-lookup"><span data-stu-id="e7172-110">**Exchange UM**</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-111">[Get-CsExUmContact](https://technet.microsoft.com/library/Gg412725(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-111">[Get-CsExUmContact](https://technet.microsoft.com/library/Gg412725(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-112">[Move-CsExUmContact](https://technet.microsoft.com/library/Gg425842(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-112">[Move-CsExUmContact](https://technet.microsoft.com/library/Gg425842(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-113">[New-CsExUmContact](https://technet.microsoft.com/library/Gg398139(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-113">[New-CsExUmContact](https://technet.microsoft.com/library/Gg398139(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-114">[Remove-CsExUmContact](rehttps://technet.microsoft.com/library/Gg425842(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-114">[Remove-CsExUmContact](rehttps://technet.microsoft.com/library/Gg425842(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-115">[Set-CsExUmContact](https://technet.microsoft.com/library/Gg412944(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-115">[Set-CsExUmContact](https://technet.microsoft.com/library/Gg412944(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="e7172-116">[Test-CsExStorageConnectivity](https://technet.microsoft.com/library/JJ204740(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-116">[Test-CsExStorageConnectivity](https://technet.microsoft.com/library/JJ204740(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="e7172-117">[Test-CsExStorageNotification](https://technet.microsoft.com/library/JJ205331(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-117">[Test-CsExStorageNotification](https://technet.microsoft.com/library/JJ205331(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="e7172-118">[Test-CsExUMConnectivity](https://technet.microsoft.com/library/JJ204784(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-118">[Test-CsExUMConnectivity](https://technet.microsoft.com/library/JJ204784(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="e7172-119">[Test-CsExUMVoiceMail](https://technet.microsoft.com/library/JJ205058(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-119">[Test-CsExUMVoiceMail](https://technet.microsoft.com/library/JJ205058(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="e7172-120">[Get-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398348(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-120">[Get-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398348(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-121">[Grant-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg412829(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-121">[Grant-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg412829(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-122">[Nuevo: CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398653(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-122">[New-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398653(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-123">[Remove-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398211(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-123">[Remove-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398211(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-124">[Set-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg412722(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-124">[Set-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg412722(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="e7172-125">[Get-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg425732(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-125">[Get-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg425732(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-126">[Nuevo: CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg425849(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-126">[New-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg425849(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-127">[Remove-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg398573(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-127">[Remove-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg398573(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="e7172-128">[Set-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg412948(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="e7172-128">[Set-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg412948(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e7172-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7172-129">See Also</span></span>


[<span data-ttu-id="e7172-130">Blog de Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7172-130">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="e7172-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e7172-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

