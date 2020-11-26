---
title: 'Lync Server 2013: cmdlets de topología'
description: 'Lync Server 2013: cmdlets de topología.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topology cmdlets
ms:assetid: 3ed739a7-d58d-475d-8240-fa8d2c6dc7e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415648(v=OCS.15)
ms:contentKeyID: 48183942
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f77febaa3beb4acc25bc5bc54dd0d5585fe18fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444143"
---
# <a name="topology-cmdlets-jn-lync-server-2013"></a><span data-ttu-id="76439-103">Cmdlets de topología Jn Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76439-103">Topology cmdlets jn Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76439-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76439-104">

<span> </span></span></span>

<span data-ttu-id="76439-105">_**Última modificación del tema:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="76439-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="76439-106">Muchos de los cmdlets de topología incluidos en Microsoft Lync Server 2013 están diseñados para su uso con la configuración y el generador de topología; por eso, hay varios cmdlets de topología que los administradores suelen llamar directamente.</span><span class="sxs-lookup"><span data-stu-id="76439-106">Many of the topology cmdlets included in Microsoft Lync Server 2013 are designed for use with Setup and Topology Builder; because of that, there are a number of topology cmdlets that administrators will rarely call directly.</span></span> <span data-ttu-id="76439-107">Sin embargo, habrá ocasiones en que los administradores necesiten usar estos cmdlets; por ejemplo, después de crear nuevas cuentas Kerberos, debe ejecutar el cmdlet [enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15)) para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="76439-107">However, there will be times when administrators will be required to use these cmdlets; for example, after creating new Kerberos accounts you must run the [Enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15)) cmdlet to cause the changes to take effect.</span></span> <span data-ttu-id="76439-108">Además, es probable que los administradores ejecuten cmdlets como [Test-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15)) y [Test-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15)) para asegurarse de que Lync Server 2013 se haya instalado correctamente y de que funcione de la manera esperada.</span><span class="sxs-lookup"><span data-stu-id="76439-108">In addition, administrators will likely run cmdlets such as [Test-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15)) and [Test-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15)) to help ensure that Lync Server 2013 has been correctly installed and is working as expected.</span></span>

<div>

## <a name="topology-cmdlets"></a><span data-ttu-id="76439-109">Cmdlets de topología</span><span class="sxs-lookup"><span data-stu-id="76439-109">Topology Cmdlets</span></span>

<span data-ttu-id="76439-110">A continuación se muestra una lista de cmdlets que se relacionan directamente con la administración de la topología de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="76439-110">The following is a list of cmdlets that relate directly managing your Lync Server topology:</span></span>

<span data-ttu-id="76439-111">**Topología**</span><span class="sxs-lookup"><span data-stu-id="76439-111">**Topology**</span></span>

  - <span></span>  
    <span data-ttu-id="76439-112">[Get-CsPool](https://technet.microsoft.com/library/Gg398992(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-112">[Get-CsPool](https://technet.microsoft.com/library/Gg398992(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="76439-113">[Get-CsSite](https://technet.microsoft.com/library/Gg398185(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-113">[Get-CsSite](https://technet.microsoft.com/library/Gg398185(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="76439-114">[Set-CsSite](https://technet.microsoft.com/library/Gg413023(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-114">[Set-CsSite](https://technet.microsoft.com/library/Gg413023(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="76439-115">[Enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-115">[Enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="76439-116">[Get-CsTopology](https://technet.microsoft.com/library/Gg412824(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-116">[Get-CsTopology](https://technet.microsoft.com/library/Gg412824(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="76439-117">[Publicar-CsTopology](https://technet.microsoft.com/library/Gg398953(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-117">[Publish-CsTopology](https://technet.microsoft.com/library/Gg398953(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="76439-118">[Prueba-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-118">[Test-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="76439-119">[Exportar-CsConfiguration](https://technet.microsoft.com/library/Gg398627(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-119">[Export-CsConfiguration](https://technet.microsoft.com/library/Gg398627(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="76439-120">[Importar-CsConfiguration](https://technet.microsoft.com/library/Gg398800(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-120">[Import-CsConfiguration](https://technet.microsoft.com/library/Gg398800(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="76439-121">[Get-CsServerVersion](https://technet.microsoft.com/library/Gg398470(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-121">[Get-CsServerVersion](https://technet.microsoft.com/library/Gg398470(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="76439-122">[Disable-CsComputer](https://technet.microsoft.com/library/Gg399023(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-122">[Disable-CsComputer](https://technet.microsoft.com/library/Gg399023(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="76439-123">[Enable-CsComputer](https://technet.microsoft.com/library/Gg412815(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-123">[Enable-CsComputer](https://technet.microsoft.com/library/Gg412815(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="76439-124">[Get-CsComputer](https://technet.microsoft.com/library/Gg425959(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-124">[Get-CsComputer](https://technet.microsoft.com/library/Gg425959(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="76439-125">[Prueba-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-125">[Test-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="76439-126">[Get-CsNetworkInterface](https://technet.microsoft.com/library/Gg398121(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="76439-126">[Get-CsNetworkInterface](https://technet.microsoft.com/library/Gg398121(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="76439-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="76439-127">See Also</span></span>


[<span data-ttu-id="76439-128">Blog de Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="76439-128">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="76439-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76439-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

