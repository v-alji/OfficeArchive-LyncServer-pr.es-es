---
title: 'Lync Server 2013: cmdlets de administración de usuarios'
description: 'Lync Server 2013: cmdlets de administración de usuarios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User management cmdlets
ms:assetid: 85312f3f-28e8-421c-b94c-e6ead1f5f755
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398677(v=OCS.15)
ms:contentKeyID: 48184702
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b94f2b48017fd29fa7a5a814da8a3c80d8f57968
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440776"
---
# <a name="user-management-cmdlets-in-lync-server-2013"></a><span data-ttu-id="71ccf-103">Cmdlets de administración de usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71ccf-103">User management cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71ccf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71ccf-104">

<span> </span></span></span>

<span data-ttu-id="71ccf-105">_**Última modificación del tema:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="71ccf-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="71ccf-106">Los cmdlets de administración de usuarios incluidos en Microsoft Lync Server 2013 le permiten habilitar, deshabilitar y modificar cuentas de usuario de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71ccf-106">The user management cmdlets included in Microsoft Lync Server 2013 allow you to enable, disable, and modify Lync Server user accounts.</span></span>

<div>

## <a name="user-management-cmdlets"></a><span data-ttu-id="71ccf-107">Cmdlets de administración de usuarios</span><span class="sxs-lookup"><span data-stu-id="71ccf-107">User Management Cmdlets</span></span>

<span data-ttu-id="71ccf-108">La mayoría de las tareas de administración que se aplican a los usuarios y las cuentas de usuario se pueden realizar en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71ccf-108">Most management tasks that apply to users and user accounts can be performed from the Lync Server Control Panel.</span></span> <span data-ttu-id="71ccf-109">Las excepciones principales son los cmdlets que se utilizan en los proveedores de servicios de audioconferencia.</span><span class="sxs-lookup"><span data-stu-id="71ccf-109">The primary exceptions are the cmdlets that deal with audio conferencing providers.</span></span> <span data-ttu-id="71ccf-110">Las tareas de administración de usuarios se pueden realizar con cmdlets desde el shell de administración de Lync Server o desde una secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="71ccf-110">User management tasks can be performed using cmdlets from the Lync Server Management Shell or from within a script.</span></span> <span data-ttu-id="71ccf-111">Mediante un script, puede automatizar determinadas tareas.</span><span class="sxs-lookup"><span data-stu-id="71ccf-111">By using a script, you can automate certain tasks.</span></span> <span data-ttu-id="71ccf-112">A continuación se muestra una lista de cmdlets que se relacionan directamente con la administración de usuarios y cuentas de usuario:</span><span class="sxs-lookup"><span data-stu-id="71ccf-112">The following is a list of cmdlets that relate directly to managing users and user accounts:</span></span>

  - <span></span>  
    [<span data-ttu-id="71ccf-113">Get-CsAdContact</span><span class="sxs-lookup"><span data-stu-id="71ccf-113">Get-CsAdContact</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAdContact)

<!-- end list -->

  - <span></span>  
    [<span data-ttu-id="71ccf-114">Get-CsAdUser</span><span class="sxs-lookup"><span data-stu-id="71ccf-114">Get-CsAdUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAdUser)

<!-- end list -->

  - [<span data-ttu-id="71ccf-115">Get-CsClientAccessLicense</span><span class="sxs-lookup"><span data-stu-id="71ccf-115">Get-CsClientAccessLicense</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsClientAccessLicense)

<!-- end list -->

  - [<span data-ttu-id="71ccf-116">Get-CsEffectivePolicy</span><span class="sxs-lookup"><span data-stu-id="71ccf-116">Get-CsEffectivePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsEffectivePolicy)

<!-- end list -->

  - [<span data-ttu-id="71ccf-117">Invoke-CsUcsRollback</span><span class="sxs-lookup"><span data-stu-id="71ccf-117">Invoke-CsUcsRollback</span></span>](https://docs.microsoft.com/powershell/module/skype/Invoke-CsUcsRollback)

<!-- end list -->

  - [<span data-ttu-id="71ccf-118">Debug-CsUnifiedContactStore</span><span class="sxs-lookup"><span data-stu-id="71ccf-118">Debug-CsUnifiedContactStore</span></span>](https://docs.microsoft.com/powershell/module/skype/Debug-CsUnifiedContactStore)

  - [<span data-ttu-id="71ccf-119">Test-CsUnifiedContactStore</span><span class="sxs-lookup"><span data-stu-id="71ccf-119">Test-CsUnifiedContactStore</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsUnifiedContactStore)

<!-- end list -->

  - <span></span>  
    [<span data-ttu-id="71ccf-120">Disable-CsUser</span><span class="sxs-lookup"><span data-stu-id="71ccf-120">Disable-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Disable-CsUser)

  - <span></span>  
    [<span data-ttu-id="71ccf-121">Enable-CsUser</span><span class="sxs-lookup"><span data-stu-id="71ccf-121">Enable-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Enable-CsUser)

  - <span></span>  
    [<span data-ttu-id="71ccf-122">Get-CsUser</span><span class="sxs-lookup"><span data-stu-id="71ccf-122">Get-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUser)

  - <span></span>  
    [<span data-ttu-id="71ccf-123">Mover-CsUser</span><span class="sxs-lookup"><span data-stu-id="71ccf-123">Move-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Move-CsUser)

  - <span></span>  
    [<span data-ttu-id="71ccf-124">Set-CsUser</span><span class="sxs-lookup"><span data-stu-id="71ccf-124">Set-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUser)

<!-- end list -->

  - <span></span>  
    [<span data-ttu-id="71ccf-125">Get-CsUserAcp</span><span class="sxs-lookup"><span data-stu-id="71ccf-125">Get-CsUserAcp</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserAcp)

  - <span></span>  
    [<span data-ttu-id="71ccf-126">Remove-CsUserAcp</span><span class="sxs-lookup"><span data-stu-id="71ccf-126">Remove-CsUserAcp</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsUserAcp)

  - <span></span>  
    [<span data-ttu-id="71ccf-127">Set-CsUserAcp</span><span class="sxs-lookup"><span data-stu-id="71ccf-127">Set-CsUserAcp</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUserAcp)

  - <span></span>  
    [<span data-ttu-id="71ccf-128">Test-CsAudioConferencingProvider</span><span class="sxs-lookup"><span data-stu-id="71ccf-128">Test-CsAudioConferencingProvider</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAudioConferencingProvider)

<!-- end list -->

  - <span></span>  
    [<span data-ttu-id="71ccf-129">Get-CsUserPoolInfo</span><span class="sxs-lookup"><span data-stu-id="71ccf-129">Get-CsUserPoolInfo</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserPoolInfo)

<!-- end list -->

  - [<span data-ttu-id="71ccf-130">Get-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="71ccf-130">Get-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserServicesPolicy)

  - [<span data-ttu-id="71ccf-131">Grant-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="71ccf-131">Grant-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsUserServicesPolicy)

  - [<span data-ttu-id="71ccf-132">New-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="71ccf-132">New-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsUserServicesPolicy)

  - [<span data-ttu-id="71ccf-133">Remove-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="71ccf-133">Remove-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsUserServicesPolicy)

  - [<span data-ttu-id="71ccf-134">Set-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="71ccf-134">Set-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUserServicesPolicy)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="71ccf-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="71ccf-135">See Also</span></span>


[<span data-ttu-id="71ccf-136">Blog de Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="71ccf-136">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="71ccf-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71ccf-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

