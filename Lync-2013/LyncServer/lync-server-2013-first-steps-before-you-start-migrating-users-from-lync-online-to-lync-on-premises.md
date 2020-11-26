---
title: 'Lync Server 2013: primeros pasos antes de empezar a migrar usuarios de Lync Online a Lync local'
description: 'Lync Server 2013: primeros pasos antes de empezar a migrar usuarios de Lync Online a Lync local.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: First steps before you start migrating users from Lync Online to Lync on-premises
ms:assetid: 98245b04-ded4-4186-8da3-ba1c554b5c39
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689118(v=OCS.15)
ms:contentKeyID: 62258123
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 408820e461c0a9f7c0beaaaae3a502802048d3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428121"
---
# <a name="first-steps-before-you-start-migrating-users-from-lync-online-to-lync-on-premises-in-lync-server-2013"></a><span data-ttu-id="f2613-103">Primeros pasos antes de empezar a migrar usuarios de Lync Online a Lync local en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2613-103">First steps before you start migrating users from Lync Online to Lync on-premises in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2613-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2613-104">

<span> </span></span></span>

<span data-ttu-id="f2613-105">_**Última modificación del tema:** 2014-05-08_</span><span class="sxs-lookup"><span data-stu-id="f2613-105">_**Topic Last Modified:** 2014-05-08_</span></span>

<span data-ttu-id="f2613-106">Antes de empezar a mover usuarios de Lync Online a su entorno local, compruebe que se cumplen todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2613-106">Before you start moving Lync Online users to your on-premises environment, check that all of the following are true:</span></span>

  - <span data-ttu-id="f2613-107">El entorno local de Lync Server debe implementarse y validarse por completo.</span><span class="sxs-lookup"><span data-stu-id="f2613-107">Your Lync Server on-premises environment must be fully deployed and validated.</span></span> <span data-ttu-id="f2613-108">Para obtener más información, consulte [implementar Lync Server 2013](lync-server-2013-deploying-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="f2613-108">For more information, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md).</span></span>

  - <span data-ttu-id="f2613-109">El inquilino de Lync Online debe estar configurado para el acceso remoto de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f2613-109">Your Lync Online tenant must be configured for remote PowerShell Access.</span></span>
    
    <span data-ttu-id="f2613-110">Para ello, primero Instale el módulo Lync Online para Windows PowerShell, que puede obtener aquí: [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911) .</span><span class="sxs-lookup"><span data-stu-id="f2613-110">To do this, first install the Lync Online module for Windows PowerShell, which you can get here: [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911).</span></span>
    
    <span data-ttu-id="f2613-111">Después de instalar el módulo, puede establecer una sesión remota escribiendo los cmdlets siguientes en el shell de administración de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="f2613-111">After you install the module, you can establish a remote session by typing the following cmdlets in the Lync Server Management Shell:</span></span>
    
       ```PowerShell
        Import-Module LyncOnlineConnector
       ```  
    
       ```PowerShell
        $cred = Get-Credential
       ``` 
    
       ```PowerShell
        $CSSession = New-CsOnlineSession -Credential $cred
       ```
    
       ```PowerShell
        Import-PSSession $CSSession -AllowClobber
       ```
    
    <span data-ttu-id="f2613-112">Para obtener más información sobre cómo establecer una sesión PowerShell remota con Lync Online, consulte [conectarse a Lync Online mediante Windows PowerShell](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="f2613-112">For more information about how to establish a remote PowerShell session with Lync Online, see [Connecting to Lync Online by using Windows PowerShell](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>
  
    <span data-ttu-id="f2613-113">Para obtener más información sobre el uso del módulo de PowerShell Lync Online, vea [usar Windows PowerShell para administrar Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="f2613-113">For more information about using the Lync Online PowerShell module, see [Using Windows PowerShell to manage Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

  - <span data-ttu-id="f2613-114">Su Lync Online debe estar configurado para el espacio de direcciones SIP compartido.</span><span class="sxs-lookup"><span data-stu-id="f2613-114">Your Lync Online must be configured for Shared SIP Address Space.</span></span> <span data-ttu-id="f2613-115">Para ello, inicie en primer lugar una sesión remota de PowerShell con Lync Online.</span><span class="sxs-lookup"><span data-stu-id="f2613-115">To do this, first start a remote Powershell session with Lync Online.</span></span> <span data-ttu-id="f2613-116">Luego, ejecute el cmdlet siguiente:</span><span class="sxs-lookup"><span data-stu-id="f2613-116">Then run the following cmdlet:</span></span>
    
        Set-CsTenantFederationConfiguration -SharedSipAddressSpace $True

<span data-ttu-id="f2613-117">Una vez que haya terminado estos pasos, puede pasar a [migrar usuarios de Lync Online a Lync local en Lync Server 2013](lync-server-2013-migrating-lync-online-users-to-lync-on-premises.md).</span><span class="sxs-lookup"><span data-stu-id="f2613-117">After you’ve finished these steps, you can move on to [Migrating Lync Online users to Lync on-premises in Lync Server 2013](lync-server-2013-migrating-lync-online-users-to-lync-on-premises.md).</span></span>

<span data-ttu-id="f2613-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2613-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

