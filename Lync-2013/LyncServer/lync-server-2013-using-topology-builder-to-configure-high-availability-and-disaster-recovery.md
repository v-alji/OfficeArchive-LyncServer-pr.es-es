---
title: Usar Topology Builder para configurar la alta disponibilidad y la recuperación ante desastres
description: Usar el generador de topología para configurar la alta disponibilidad y la recuperación ante desastres.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Topology Builder to configure high availability and disaster recovery
ms:assetid: abc1a25d-1f5e-46ef-91d2-0144fc847206
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205172(v=OCS.15)
ms:contentKeyID: 48185113
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04764a58ac3ae1bbe0df97aadeabb03158ce8100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400116"
---
# <a name="using-topology-builder-to-configure-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="2495d-103">Usar Topology Builder para configurar la alta disponibilidad y la recuperación ante desastres en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2495d-103">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2495d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2495d-104">

<span> </span></span></span>

<span data-ttu-id="2495d-105">_**Última modificación del tema:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="2495d-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="2495d-106">Siga los pasos que se indican en el generador de topología para configurar la alta disponibilidad y la recuperación ante desastres para el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="2495d-106">Perform the following steps within Topology Builder to configure high availability and disaster recovery for Persistent Chat Server.</span></span>

1.  <span data-ttu-id="2495d-107">Agregue las bases de datos reflejadas y de trasvase de registros que SQL Server almacena.</span><span class="sxs-lookup"><span data-stu-id="2495d-107">Add the mirror databases and the log shipping secondary database SQL Server stores.</span></span>

2.  <span data-ttu-id="2495d-108">Edite las propiedades del servicio del servidor de chat persistentes en:</span><span class="sxs-lookup"><span data-stu-id="2495d-108">Edit the Persistent Chat Server service properties to:</span></span>
    
    1.  <span data-ttu-id="2495d-109">Habilite la creación de reflejo para la base de datos principal.</span><span class="sxs-lookup"><span data-stu-id="2495d-109">Enable mirroring for the primary database.</span></span>
    
    2.  <span data-ttu-id="2495d-110">Agregue el almacén de SQL Server de reflejo principal.</span><span class="sxs-lookup"><span data-stu-id="2495d-110">Add the primary mirror SQL Server store.</span></span>
    
    3.  <span data-ttu-id="2495d-111">Habilite la base de datos de trasvase de registros de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2495d-111">Enable the SQL Server Log Shipping database.</span></span>
    
    4.  <span data-ttu-id="2495d-112">Agregue el almacén de SQL Server secundario de trasvase de registros de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2495d-112">Add the SQL Server Log Shipping secondary SQL Server store.</span></span>
    
    5.  <span data-ttu-id="2495d-113">Agregue el reflejo de la tienda SQL Server para la base de datos secundaria.</span><span class="sxs-lookup"><span data-stu-id="2495d-113">Add the SQL Server store mirror for the secondary database.</span></span>
    
    6.  <span data-ttu-id="2495d-114">Publique la topología.</span><span class="sxs-lookup"><span data-stu-id="2495d-114">Publish the topology.</span></span>

<span data-ttu-id="2495d-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2495d-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

