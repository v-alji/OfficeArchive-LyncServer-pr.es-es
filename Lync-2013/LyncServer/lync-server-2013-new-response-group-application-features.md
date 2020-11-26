---
title: 'Lync Server 2013: Nuevas funciones de las aplicaciones de grupo de respuesta'
description: 'Lync Server 2013: nuevas características de la aplicación de grupo de respuesta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Response Group application features
ms:assetid: 569544b4-fa97-429b-97e6-568afab6c19b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398373(v=OCS.15)
ms:contentKeyID: 48184196
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 191d3867758da427ade3470e78abfd417f6f00de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424999"
---
# <a name="new-response-group-application-features-in-lync-server-2013"></a><span data-ttu-id="e0fe4-103">Nuevas funciones de las aplicaciones de grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0fe4-103">New Response Group application features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0fe4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0fe4-104">

<span> </span></span></span>

<span data-ttu-id="e0fe4-105">_**Última modificación del tema:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="e0fe4-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="e0fe4-106">Con la aplicación de grupo de respuesta, puede enrutar y poner en cola las llamadas entrantes a personas designadas para fines especiales, como el servicio de atención al cliente, una asistencia interna o asistencia telefónica general para un departamento.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-106">With the Response Group application, you can route and queue incoming calls to designated persons for special purposes, such as customer service, an internal help desk, or general telephone support for a department.</span></span>

<span data-ttu-id="e0fe4-107">Las siguientes características de la aplicación de grupo de respuesta son nuevas en Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="e0fe4-107">The following Response Group application features are new in Lync Server 2013:</span></span>

  - <span data-ttu-id="e0fe4-108">**Rol de administrador**</span><span class="sxs-lookup"><span data-stu-id="e0fe4-108">**Manager role**</span></span>
    
    <span data-ttu-id="e0fe4-109">Lync Server 2013 introduce un nuevo rol de administrador de grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-109">Lync Server 2013 introduces a new Response Group Manager role.</span></span> <span data-ttu-id="e0fe4-110">Ahora hay dos roles de administración para los grupos de respuesta: administrador de grupo de respuesta y administrador del grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-110">Now there are two management roles for response groups: Response Group Manager and Response Group Administrator.</span></span> <span data-ttu-id="e0fe4-111">Mientras que los administradores de grupos de respuesta aún pueden configurar cualquier elemento para cualquier grupo de respuesta, los administradores solo pueden configurar determinados elementos, solo para los grupos de respuesta de los que son propietarios.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-111">While Response Group Administrators can still configure any element for any response group, Managers can configure only certain elements, only for response groups they own.</span></span>
    
    <span data-ttu-id="e0fe4-112">Esta mejora en el modelo de administración beneficia la escalabilidad de grupos de respuesta, especialmente para escenarios de implementación grandes.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-112">This improvement in the administration model benefits Response Group scalability, especially for large deployment scenarios.</span></span>

  - <span data-ttu-id="e0fe4-113">**Alta disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="e0fe4-113">**High availability**</span></span>
    
    <span data-ttu-id="e0fe4-114">La compatibilidad de alta disponibilidad para la aplicación de grupo de respuesta, en forma de reflejo de SQL Server, está habilitada como parte de la configuración general e implementación de la alta disponibilidad de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-114">High availability support for the Response Group application, in the form of SQL Server mirroring, is enabled as part of the overall configuration and deployment of high availability for Lync Server 2013.</span></span> <span data-ttu-id="e0fe4-115">Si configura para alta disponibilidad y pierde conectividad con el servidor back-end principal, la funcionalidad de grupo de respuesta no se ve afectada por el uso del servidor de servicios de fondo reflejado.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-115">If you configure for high availability and lose connectivity to the primary back-end server, Response Group functionality is not affected by leveraging the mirrored back-end server.</span></span>
    
    <span data-ttu-id="e0fe4-116">La compatibilidad con el reflejo de SQL Server para la aplicación de grupo de respuesta no se puede habilitar o configurar individualmente fuera de la configuración general de alta disponibilidad de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-116">Support for SQL Server mirroring for the Response Group application can’t be individually enabled or configured outside of the overall Lync Server 2013 high availability configuration.</span></span>

  - <span data-ttu-id="e0fe4-117">**Recuperación ante desastres**</span><span class="sxs-lookup"><span data-stu-id="e0fe4-117">**Disaster recovery**</span></span>
    
    <span data-ttu-id="e0fe4-118">La compatibilidad de recuperación ante desastres para la aplicación de grupo de respuesta está habilitada como parte de la configuración e implementación de las agrupaciones frontales emparejadas, que forman parte de la configuración general de recuperación ante desastres de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-118">Disaster recovery support for the Response Group application is enabled as part of the configuration and deployment of the paired Front End pools, which are part of the overall Lync Server 2013 disaster recovery configuration.</span></span> <span data-ttu-id="e0fe4-119">Además, los cmdlets de importación y exportación de grupos de respuesta admiten el proceso de conmutación por error para el grupo de copia de seguridad y el proceso de recuperación tras error al grupo principal o a un grupo nuevo.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-119">In addition, Response Group import and export cmdlets support the failover process to the backup pool and the failback process to the primary pool or to a new pool.</span></span> <span data-ttu-id="e0fe4-120">Si se produce una interrupción en el grupo principal, los grupos de respuesta pueden conmutar por error al grupo de copias de seguridad y, después, devolver el error al grupo principal o a un nuevo grupo cuando haya finalizado la interrupción.</span><span class="sxs-lookup"><span data-stu-id="e0fe4-120">If an outage occurs in the primary pool, response groups can be failed over to the backup pool, and then failed back to the primary pool or to a new pool when the outage is over.</span></span>

<div id="sectionSection0" class="section">

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e0fe4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0fe4-121">See Also</span></span>


[<span data-ttu-id="e0fe4-122">Planificar para grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0fe4-122">Planning for response groups in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-groups.md)  
  

<span data-ttu-id="e0fe4-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0fe4-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

