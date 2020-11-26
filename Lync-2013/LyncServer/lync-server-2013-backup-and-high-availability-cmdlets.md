---
title: 'Lync Server 2013: cmdlets de copia de seguridad y alta disponibilidad'
description: 'Lync Server 2013: cmdlets de copia de seguridad y alta disponibilidad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup and high availability cmdlets
ms:assetid: 5aff41a3-7a0e-4c51-9d5f-7f08e36bf046
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204925(v=OCS.15)
ms:contentKeyID: 48184236
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d455f25e7a5a816f42d9df58c886429c96208acd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438004"
---
# <a name="backup-and-high-availability-cmdlets-in-lync-server-2013"></a><span data-ttu-id="3fa9c-103">Cmdlets de copia de seguridad y alta disponibilidad en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fa9c-103">Backup and high availability cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fa9c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fa9c-104">

<span> </span></span></span>

<span data-ttu-id="3fa9c-105">_**Última modificación del tema:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="3fa9c-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="3fa9c-106">Los cmdlets de copia de seguridad y de alta disponibilidad permiten a los administradores administrar las capacidades de la copia de seguridad de la agrupación, la restauración y la alta disponibilidad introducidas en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3fa9c-106">The backup and high availability cmdlets enable administrators to manage the pool backup, restore, and high availability capabilities introduced in Microsoft Lync Server 2013.</span></span>

<div>

## <a name="backup-and-high-availability-cmdlets"></a><span data-ttu-id="3fa9c-107">Cmdlets de alta disponibilidad y copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="3fa9c-107">Backup and High Availability Cmdlets</span></span>

<span data-ttu-id="3fa9c-108">A continuación se muestra una lista de cmdlets que se relacionan directamente con la copia de seguridad y la configuración de la topología de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="3fa9c-108">The following is a list of cmdlets that relate directly to backing up and configuring the availability of your Lync Server topology:</span></span>

<span data-ttu-id="3fa9c-109">**Cmdlets de alta disponibilidad y copia de seguridad**</span><span class="sxs-lookup"><span data-stu-id="3fa9c-109">**Backup and High Availability Cmdlets**</span></span>

  - <span data-ttu-id="3fa9c-110">[Get-CsBackupServiceConfiguration](https://technet.microsoft.com/library/JJ205087(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-110">[Get-CsBackupServiceConfiguration](https://technet.microsoft.com/library/JJ205087(v=OCS.15))</span></span>

  - <span data-ttu-id="3fa9c-111">[Remove-CsBackupServiceConfiguration](https://technet.microsoft.com/library/JJ204903(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-111">[Remove-CsBackupServiceConfiguration](https://technet.microsoft.com/library/JJ204903(v=OCS.15))</span></span>

  - <span data-ttu-id="3fa9c-112">[Set-CsBackupServiceConfiguration](https://technet.microsoft.com/library/JJ205006(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-112">[Set-CsBackupServiceConfiguration](https://technet.microsoft.com/library/JJ205006(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-113">[Get-CsBackupServiceStatus](https://technet.microsoft.com/library/JJ205032(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-113">[Get-CsBackupServiceStatus](https://technet.microsoft.com/library/JJ205032(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-114">[Invoke-CsBackupServiceSync](https://technet.microsoft.com/library/JJ205374(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-114">[Invoke-CsBackupServiceSync](https://technet.microsoft.com/library/JJ205374(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-115">[Debug-CsIntraPoolReplication](https://technet.microsoft.com/library/JJ205103(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-115">[Debug-CsIntraPoolReplication](https://technet.microsoft.com/library/JJ205103(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-116">[Backup-CsPool](https://technet.microsoft.com/library/JJ204955(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-116">[Backup-CsPool](https://technet.microsoft.com/library/JJ204955(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-117">[Get-CsPoolBackupRelationship](https://technet.microsoft.com/library/JJ204745(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-117">[Get-CsPoolBackupRelationship](https://technet.microsoft.com/library/JJ204745(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-118">[Get-CsPoolFabricState](https://technet.microsoft.com/library/JJ619188(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-118">[Get-CsPoolFabricState](https://technet.microsoft.com/library/JJ619188(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-119">[Invoke-CsPoolFailBack](https://technet.microsoft.com/library/JJ204873(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-119">[Invoke-CsPoolFailBack](https://technet.microsoft.com/library/JJ204873(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-120">[Invoke-CsPoolFailOver](https://technet.microsoft.com/library/JJ205189(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-120">[Invoke-CsPoolFailOver](https://technet.microsoft.com/library/JJ205189(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-121">[Get-CsPoolUpgradeReadinessState](https://technet.microsoft.com/library/JJ204689(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-121">[Get-CsPoolUpgradeReadinessState](https://technet.microsoft.com/library/JJ204689(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-122">[Invoke-CsStorageServiceFlush](https://technet.microsoft.com/library/JJ619175(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-122">[Invoke-CsStorageServiceFlush](https://technet.microsoft.com/library/JJ619175(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-123">[Sync-CsUserData](https://technet.microsoft.com/library/JJ205242(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-123">[Sync-CsUserData](https://technet.microsoft.com/library/JJ205242(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="3fa9c-124">[Remove-CsUserStoreBackupData](https://technet.microsoft.com/library/JJ205003(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3fa9c-124">[Remove-CsUserStoreBackupData](https://technet.microsoft.com/library/JJ205003(v=OCS.15))</span></span>

<span data-ttu-id="3fa9c-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fa9c-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

