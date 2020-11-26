---
title: 'Lync Server 2013: copia de seguridad y restauración de Lync Server'
description: 'Lync Server 2013: copia de seguridad y restauración de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up and restoring Lync Server 2013
ms:assetid: 07dc1f5e-af66-4e18-bf39-881dceff8bc3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202160(v=OCS.15)
ms:contentKeyID: 51541443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1a7024b2264fb895d1562a6da0775f9397644b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438144"
---
# <a name="backing-up-and-restoring-lync-server-2013"></a><span data-ttu-id="ec39d-103">Copia de seguridad y restauración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec39d-103">Backing up and restoring Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec39d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec39d-104">

<span> </span></span></span>

<span data-ttu-id="ec39d-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ec39d-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ec39d-106">En esta sección, encontrarás los procedimientos recomendados para realizar copias de seguridad de los datos de Lync Server 2013 y de restaurarlos si tienes un error.</span><span class="sxs-lookup"><span data-stu-id="ec39d-106">In this section, you’ll find the best practices for backing up your Lync Server 2013 data, and for restoring it if you have a failure.</span></span> <span data-ttu-id="ec39d-107">Estas prácticas recomendadas se aplican a las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="ec39d-107">These best practices apply to the following situations:</span></span>

  - <span data-ttu-id="ec39d-108">Un grupo de servidores de Lync completo de cualquier tipo (servidor front-end, servidor perimetral, servidor de mediación, servidor de chat persistente o director) o un servidor individual de uno de estos grupos.</span><span class="sxs-lookup"><span data-stu-id="ec39d-108">An entire Lync Server pool of any type (Front End Server, Edge Server, Mediation Server, Persistent Chat Server, or Director), or an individual server in one of these pools.</span></span>

  - <span data-ttu-id="ec39d-109">El servidor de administración central</span><span class="sxs-lookup"><span data-stu-id="ec39d-109">The Central Management Server</span></span>

  - <span data-ttu-id="ec39d-110">Un servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="ec39d-110">A Standard Edition server</span></span>

  - <span data-ttu-id="ec39d-111">Un servidor de back-end Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="ec39d-111">An Enterprise Edition Back End Server</span></span>

  - <span data-ttu-id="ec39d-112">Un almacén de archivos</span><span class="sxs-lookup"><span data-stu-id="ec39d-112">A File Store</span></span>

  - <span data-ttu-id="ec39d-113">Una base de datos de archivado, una base de datos de supervisión o una base de datos de chat persistente</span><span class="sxs-lookup"><span data-stu-id="ec39d-113">An Archiving database, Monitoring database, or Persistent Chat database</span></span>

<span data-ttu-id="ec39d-114">Esta sección no incluye información sobre cómo restaurar todo un sitio o para desarrollar un sitio en espera.</span><span class="sxs-lookup"><span data-stu-id="ec39d-114">This section does not include information about restoring an entire site or for developing a standby site.</span></span> <span data-ttu-id="ec39d-115">Para obtener información sobre cómo desarrollar una solución de recuperación ante desastres con grupos front-end emparejados, vea [planear la alta disponibilidad y la recuperación ante desastres en Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="ec39d-115">For details about developing a disaster recovery solution with paired Front End pools, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span> <span data-ttu-id="ec39d-116">Este es el método recomendado para planear la recuperación de desastres.</span><span class="sxs-lookup"><span data-stu-id="ec39d-116">This is the recommended method for planning for disaster recovery.</span></span>

<span data-ttu-id="ec39d-117">Si ha implementado agrupaciones front-end emparejadas, si uno de estos grupos tiene errores y se vuelve irrecuperable, puede restaurar este grupo con un nuevo nombre de dominio completo (FQDN) de su grupo emparejado.</span><span class="sxs-lookup"><span data-stu-id="ec39d-117">If you have deployed paired Front End pools, if one of these pools fails and becomes unrecoverable, you can restore this pool with a new fully qualified domain name (FQDN) from its paired pool.</span></span> <span data-ttu-id="ec39d-118">Para obtener más información sobre los pasos necesarios para realizar esta recuperación, consulte [conmutación por error de un grupo en Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span><span class="sxs-lookup"><span data-stu-id="ec39d-118">For details on the steps to perform this recovery, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="ec39d-119">Además, si posteriormente desea volver a crear un grupo con errores e irrecuperables que formaba parte de un par front-end, puede seguir los pasos que se indican en [realizar una conmutación por error de la agrupación de front-end ABC en Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).</span><span class="sxs-lookup"><span data-stu-id="ec39d-119">Additionally, if you later want to recreate a failed and unrecoverable pool that was part of a Front End pair, you can use the steps in [Performing an ABC Front End pool failover in Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).</span></span>

<span data-ttu-id="ec39d-120">La metodología descrita en este documento implica consideraciones especiales durante la fase de planificación.</span><span class="sxs-lookup"><span data-stu-id="ec39d-120">The methodology described in this document involves special considerations during the planning phase.</span></span> <span data-ttu-id="ec39d-121">Para obtener más información, consulte [establecer un plan de copia de seguridad y restauración para Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span><span class="sxs-lookup"><span data-stu-id="ec39d-121">For details, see [Establishing a backup and restoration plan for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ec39d-122">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ec39d-122">In This Section</span></span>

  - [<span data-ttu-id="ec39d-123">Prepararse para la copia de seguridad y restauración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec39d-123">Preparing for Lync Server 2013 backup and restoration</span></span>](lync-server-2013-preparing-for-lync-server-backup-and-restoration.md)

  - [<span data-ttu-id="ec39d-124">Copia de seguridad de datos y configuración en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec39d-124">Backing up data and settings in Lync Server 2013</span></span>](lync-server-2013-backing-up-data-and-settings.md)

  - [<span data-ttu-id="ec39d-125">Restauración de datos y configuración en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec39d-125">Restoring data and settings in Lync Server 2013</span></span>](lync-server-2013-restoring-data-and-settings.md)

  - [<span data-ttu-id="ec39d-126">Copias de seguridad y restauración de hojas de cálculo para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec39d-126">Backup and restoration worksheets for Lync Server 2013</span></span>](lync-server-2013-backup-and-restoration-worksheets.md)

<span data-ttu-id="ec39d-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec39d-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

