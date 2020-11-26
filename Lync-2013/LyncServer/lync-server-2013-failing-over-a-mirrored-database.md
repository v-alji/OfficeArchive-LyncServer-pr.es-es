---
title: 'Lync Server 2013: Conmutación por error de una base de datos reflejada'
description: 'Lync Server 2013: error en una base de datos reflejada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over a mirrored database
ms:assetid: 70185476-e3d4-440a-9316-fa24b226343e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204991(v=OCS.15)
ms:contentKeyID: 48184450
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc7c401157c79762f674721ca717296c0fe502db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428296"
---
# <a name="failing-over-a-mirrored-database-in-lync-server-2013"></a><span data-ttu-id="cbe12-103">Conmutación por error de una base de datos reflejada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cbe12-103">Failing over a mirrored database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cbe12-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cbe12-104">

<span> </span></span></span>

<span data-ttu-id="cbe12-105">_**Última modificación del tema:** 2014-03-14_</span><span class="sxs-lookup"><span data-stu-id="cbe12-105">_**Topic Last Modified:** 2014-03-14_</span></span>

<span data-ttu-id="cbe12-106">Si ha configurado la base de datos back-end para usar el reflejo sincronizado con un testigo, la conmutación por error es automática.</span><span class="sxs-lookup"><span data-stu-id="cbe12-106">If you have configured your back-end database to use synchronized mirroring with a witness, failover is automatic.</span></span> <span data-ttu-id="cbe12-107">Si ha configurado el reflejo sincronizado sin un testigo, puede usar los siguientes procedimientos para realizar la conmutación por error y la recuperación de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cbe12-107">If you have configured synchronized mirroring without a witness, you can use the following procedures to failover and failback your database.</span></span> <span data-ttu-id="cbe12-108">También puede usar estos procedimientos para realizar un failover manual de las bases de datos y hacer un failback, incluso si ha configurado un testigo.</span><span class="sxs-lookup"><span data-stu-id="cbe12-108">You can also use these procedures to manually failover and failback your databases even if you have configured a witness.</span></span>

<div>

## <a name="to-fail-over-your-back-end-database"></a><span data-ttu-id="cbe12-109">Para conmutar por error a la base de datos back-end</span><span class="sxs-lookup"><span data-stu-id="cbe12-109">To fail over your back-end database</span></span>

1.  <span data-ttu-id="cbe12-110">Antes de realizar la conmutación por error, determine qué base de datos back-end es el principal y cuál es el reflejo; para ello, escriba el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cbe12-110">Before failing over, determine which back-end database is the principal and which is the mirror by typing the following cmdlet:</span></span>
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType User

2.  <span data-ttu-id="cbe12-111">Si el almacén de administración central está hospedado en este grupo, escriba el siguiente cmdlet para determinar cuál es el principal y cuál es el reflejo del almacén central de administración:</span><span class="sxs-lookup"><span data-stu-id="cbe12-111">If the Central Management store is hosted in this pool, type the following cmdlet to determine which is the principal and which is the mirror for the Central Management store:</span></span>
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt

3.  <span data-ttu-id="cbe12-112">Realice la conmutación por error de la base de datos de usuario:</span><span class="sxs-lookup"><span data-stu-id="cbe12-112">Perform the failover of the user database:</span></span>
    
      - <span data-ttu-id="cbe12-113">Si el principal ha fallado y se está produciendo un error en el reflejo, escriba:</span><span class="sxs-lookup"><span data-stu-id="cbe12-113">If the primary has failed and you are failing over to the mirror, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal mirror -Verbose
    
      - <span data-ttu-id="cbe12-114">Si el reflejo ha fallado y se está conmutando por error al principal, escriba:</span><span class="sxs-lookup"><span data-stu-id="cbe12-114">If the mirror has failed and you are failing over to the primary, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal primary -Verbose

4.  <span data-ttu-id="cbe12-115">Si el grupo hospeda el servidor de administración central, realice la conmutación por error del almacén de administración central.</span><span class="sxs-lookup"><span data-stu-id="cbe12-115">If the pool hosts the Central Management Server, perform the failover of the Central Management store.</span></span>
    
      - <span data-ttu-id="cbe12-116">Si el principal ha fallado y se está produciendo un error en el reflejo, escriba:</span><span class="sxs-lookup"><span data-stu-id="cbe12-116">If the primary has failed and you are failing over to the mirror, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal mirror -Verbose
    
      - <span data-ttu-id="cbe12-117">Si el reflejo ha fallado y se está conmutando por error al principal, escriba:</span><span class="sxs-lookup"><span data-stu-id="cbe12-117">If the mirror has failed and you are failing over to the primary, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal primary -Verbose

<span data-ttu-id="cbe12-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cbe12-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

