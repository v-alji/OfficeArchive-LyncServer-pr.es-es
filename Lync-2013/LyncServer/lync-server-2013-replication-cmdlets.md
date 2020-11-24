---
title: 'Lync Server 2013: cmdlets de replicación'
description: 'Lync Server 2013: cmdlets de replicación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Replication cmdlets
ms:assetid: e0c49601-d2a3-45a1-b05c-26c7ff820708
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415677(v=OCS.15)
ms:contentKeyID: 48185527
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b253176101de61a07630ec141a318dd114776392
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399815"
---
# <a name="replication-cmdlets-in-lync-server-2013"></a><span data-ttu-id="70f15-103">Cmdlets de replicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70f15-103">Replication cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70f15-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70f15-104">

<span> </span></span></span>

<span data-ttu-id="70f15-105">_**Última modificación del tema:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="70f15-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="70f15-106">Los cmdlets de replicación proporcionan una manera de supervisar y administrar la replicación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="70f15-106">The replication cmdlets provide a way for you to both monitor and manage Lync Server replication.</span></span> <span data-ttu-id="70f15-107">Puede usar estos cmdlets para configurar las opciones de replicación; para supervisar el progreso de la replicación; y para forzar manualmente la replicación en un servidor.</span><span class="sxs-lookup"><span data-stu-id="70f15-107">You can use these cmdlets to configure replication settings; to monitor replication progress; and to manually force replication on a server.</span></span>

<div>

## <a name="replication-cmdlets"></a><span data-ttu-id="70f15-108">Cmdlets de replicación</span><span class="sxs-lookup"><span data-stu-id="70f15-108">Replication Cmdlets</span></span>

<span data-ttu-id="70f15-109">A continuación se muestra una lista de cmdlets que se relacionan directamente con la administración de la replicación:</span><span class="sxs-lookup"><span data-stu-id="70f15-109">The following is a list of cmdlets that relate directly to managing replication:</span></span>

<span data-ttu-id="70f15-110">**La replicación**</span><span class="sxs-lookup"><span data-stu-id="70f15-110">**Replication**</span></span>

  - <span></span>  
    <span data-ttu-id="70f15-111">[Debug-CsInterPoolReplication](https://technet.microsoft.com/library/JJ619185(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="70f15-111">[Debug-CsInterPoolReplication](https://technet.microsoft.com/library/JJ619185(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="70f15-112">[Invoke-CsManagementStoreReplication](https://technet.microsoft.com/library/Gg413060(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="70f15-112">[Invoke-CsManagementStoreReplication](https://technet.microsoft.com/library/Gg413060(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="70f15-113">[Get-CsManagementStoreReplicationStatus](https://technet.microsoft.com/library/Gg399052(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="70f15-113">[Get-CsManagementStoreReplicationStatus](https://technet.microsoft.com/library/Gg399052(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="70f15-114">[Enable-CsReplica](https://technet.microsoft.com/library/Gg425965(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="70f15-114">[Enable-CsReplica](https://technet.microsoft.com/library/Gg425965(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="70f15-115">[Test-CsReplica](https://technet.microsoft.com/library/JJ205289(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="70f15-115">[Test-CsReplica](https://technet.microsoft.com/library/JJ205289(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="70f15-116">[Get-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398548(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="70f15-116">[Get-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398548(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="70f15-117">[Nuevo: CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg399059(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="70f15-117">[New-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg399059(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="70f15-118">[Remove-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg425738(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="70f15-118">[Remove-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg425738(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="70f15-119">[Set-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398540(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="70f15-119">[Set-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398540(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="70f15-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="70f15-120">See Also</span></span>


[<span data-ttu-id="70f15-121">Blog de Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="70f15-121">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="70f15-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70f15-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

