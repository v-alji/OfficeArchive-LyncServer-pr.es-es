---
title: 'Lync Server 2013: Administrar grupos de respuesta durante un desastre'
description: 'Lync Server 2013: administración de grupos de respuesta durante un desastre.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing response groups during a disaster
ms:assetid: 9f14e677-7be8-4f08-88ba-444ec2148ce8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688154(v=OCS.15)
ms:contentKeyID: 49733757
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16018f170395e4657daf4405798be05c6da62581
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446067"
---
# <a name="managing-response-groups-in-lync-server-2013-during-a-disaster"></a><span data-ttu-id="23491-103">Administrar grupos de respuesta durante un desastre en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23491-103">Managing response groups in Lync Server 2013 during a disaster</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23491-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23491-104">

<span> </span></span></span>

<span data-ttu-id="23491-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="23491-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="23491-106">Lync Server 2013 admite la ejecución de grupos de respuesta en el grupo de copia de seguridad durante la recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="23491-106">Lync Server 2013 supports running response groups in the backup pool during disaster recovery.</span></span> <span data-ttu-id="23491-107">En esta sección se describe cómo planear los grupos de respuesta durante una interrupción, cómo funcionan los grupos de respuesta durante la interrupción y los pasos necesarios para la conmutación por error y los grupos de respuesta con conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="23491-107">This section describes how to plan for response groups during an outage, how response groups work during the outage, and the steps required to fail over and fail back response groups.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="23491-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="23491-108">In This Section</span></span>

  - [<span data-ttu-id="23491-109">Planeamiento de recuperación ante desastres del grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23491-109">Planning for response group disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-group-disaster-recovery.md)

  - [<span data-ttu-id="23491-110">Experiencia de grupo de respuesta durante errores del grupo de servidores en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23491-110">Response group experience in Lync Server 2013 during pool failure</span></span>](lync-server-2013-response-group-experience-during-pool-failure.md)

  - [<span data-ttu-id="23491-111">Procedimientos de recuperación ante desastres del grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23491-111">Response group disaster recovery procedures in Lync Server 2013</span></span>](lync-server-2013-response-group-disaster-recovery-procedures.md)

<span data-ttu-id="23491-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23491-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

