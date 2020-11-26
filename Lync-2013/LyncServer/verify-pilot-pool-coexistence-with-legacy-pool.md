---
title: Comprobar la coexistencia del grupo de servidores piloto con el grupo de servidores heredado
description: Comprobar coexistencia de grupo piloto con grupo heredado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify pilot pool coexistence with legacy pool
ms:assetid: fe7e14bb-c7eb-4719-b154-009e99360520
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205420(v=OCS.15)
ms:contentKeyID: 48185964
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b910939b59fdaed6df32ae504eb2719435a0161e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440188"
---
# <a name="verify-pilot-pool-coexistence-with-legacy-pool"></a><span data-ttu-id="7bf5e-103">Comprobar la coexistencia del grupo de servidores piloto con el grupo de servidores heredado</span><span class="sxs-lookup"><span data-stu-id="7bf5e-103">Verify pilot pool coexistence with legacy pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7bf5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7bf5e-104">

<span> </span></span></span>

<span data-ttu-id="7bf5e-105">_**Última modificación del tema:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="7bf5e-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="7bf5e-106">Después de implementar el grupo piloto, debe comprobar la coexistencia de las dos agrupaciones mediante las herramientas administrativas para ver la información del grupo.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-106">After you deploy the pilot pool, you need to verify the coexistence of the two pools by using the administrative tools to view the pool information.</span></span> <span data-ttu-id="7bf5e-107">Para los grupos de 2013 y los grupos heredados de Lync Server, debe usar las herramientas del panel de control y del generador de topologías de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-107">For the Lync Server 2013 pools and legacy pools, you must use the Lync Server 2013 Control Panel and Topology Builder tools.</span></span>

<div>

## <a name="verify-that-lync-server-2013-services-have-started"></a><span data-ttu-id="7bf5e-108">Comprobar que los servicios de Lync Server 2013 se han iniciado</span><span class="sxs-lookup"><span data-stu-id="7bf5e-108">Verify that Lync Server 2013 services have started</span></span>

1.  <span data-ttu-id="7bf5e-109">En el servidor front-end de Lync Server 2013, vaya al \\ subprograma Servicios de herramientas administrativas.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-109">From the Lync Server 2013 Front End Server, navigate to the Administrative Tools\\Services applet.</span></span>

2.  <span data-ttu-id="7bf5e-110">Compruebe que se están ejecutando los siguientes servicios en el servidor front-end:</span><span class="sxs-lookup"><span data-stu-id="7bf5e-110">Verify that the following services are running on the Front End Server:</span></span>

<span data-ttu-id="7bf5e-111">**Servicios de Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="7bf5e-111">**Lync Server 2013 services**</span></span>

<span data-ttu-id="7bf5e-112">![Lista de servicios de Lync Server iniciada](images/JJ205420.cfff9385-6bf6-461c-982c-e727c9f20b70(OCS.15).png "Lista de servicios de Lync Server iniciada")</span><span class="sxs-lookup"><span data-stu-id="7bf5e-112">![List of Lync Server Services Started](images/JJ205420.cfff9385-6bf6-461c-982c-e727c9f20b70(OCS.15).png "List of Lync Server Services Started")</span></span>

</div>

<div>

## <a name="open-the-lync-server-2013-control-panel"></a><span data-ttu-id="7bf5e-113">Abrir el panel de control de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7bf5e-113">Open the Lync Server 2013 Control Panel</span></span>

<span data-ttu-id="7bf5e-114">Desde el servidor front-end de su implementación de Lync Server 2013, abra el panel de control de Lync Server 2013 y seleccione el grupo de servidores de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-114">From the Front End Server in your Lync Server 2013 deployment, open the Lync Server 2013 Control Panel and select the Lync Server 2010 pool.</span></span> <span data-ttu-id="7bf5e-115">Repita el procedimiento para abrir el grupo de servidores de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-115">Repeat the procedure to open the Lync Server 2013 pool.</span></span>

<span data-ttu-id="7bf5e-116">**Abrir el panel de control de Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="7bf5e-116">**Open Lync Server 2013 Control Panel**</span></span>

<span data-ttu-id="7bf5e-117">![Cuadro de diálogo Seleccionar dirección URL](images/JJ205420.b1f8e650-9c3c-4563-a403-5069f198342f(OCS.15).png "Cuadro de diálogo Seleccionar dirección URL")</span><span class="sxs-lookup"><span data-stu-id="7bf5e-117">![Select URL dialog box](images/JJ205420.b1f8e650-9c3c-4563-a403-5069f198342f(OCS.15).png "Select URL dialog box")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="7bf5e-118">En Lync Server 2013, debe actualizar Silverlight a la versión 5 antes de usar el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-118">On Lync Server 2013, you must upgrade Silverlight to Silverlight version 5 prior to using the Lync Server Control Panel.</span></span>



</div>

<span data-ttu-id="7bf5e-119">Esta topología incluye ahora los roles de servidor de Lync Server 2010 y Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-119">This topology now includes Lync Server 2010 and Lync Server 2013 server roles.</span></span>

<span data-ttu-id="7bf5e-120">**Página de topología del panel de control 2013 de Lync Server**</span><span class="sxs-lookup"><span data-stu-id="7bf5e-120">**Lync Server 2013 Control Panel Topology page**</span></span>

<span data-ttu-id="7bf5e-121">![Panel de control de Lync Server-página de topología](images/JJ205420.4ed1cc7a-cb3e-42f6-82e2-6d4d71d19352(OCS.15).jpg "Panel de control de Lync Server-página de topología")</span><span class="sxs-lookup"><span data-stu-id="7bf5e-121">![Lync Server Control Panel - Topology page](images/JJ205420.4ed1cc7a-cb3e-42f6-82e2-6d4d71d19352(OCS.15).jpg "Lync Server Control Panel - Topology page")</span></span>

</div>

<div>

## <a name="dont-attempt-to-open-the-topology-in-lync-server-2010-topology-builder"></a><span data-ttu-id="7bf5e-122">No intente abrir la topología en el generador de topología de Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7bf5e-122">Don’t attempt to open the topology in Lync Server 2010 Topology Builder</span></span>

<span data-ttu-id="7bf5e-123">Si intenta abrir la topología con el generador de topología de Lync Server 2010, encontrará el error siguiente.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-123">If you attempt to open the topology using Lync Server 2010 Topology Builder, you will encounter the error below.</span></span> <span data-ttu-id="7bf5e-124">La topología solo se puede ver con el generador de topología de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-124">The topology can only be viewed using Lync Server 2013 Topology Builder.</span></span> <span data-ttu-id="7bf5e-125">El generador de topología de Lync Server 2013 debe usarse para crear grupos para Lync Server 2013 y Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="7bf5e-125">The Lync Server 2013 Topology Builder must be used to create pools for both Lync Server 2013 and Lync Server 2010.</span></span>

<span data-ttu-id="7bf5e-126">**Mensaje de error del generador de topología 2010 de Lync Server**</span><span class="sxs-lookup"><span data-stu-id="7bf5e-126">**Lync Server 2010 Topology Builder error message**</span></span>

<span data-ttu-id="7bf5e-127">![Error de acoplamiento de MMC del generador de topología de Lync Server](images/JJ205420.f6666343-c348-4d81-ae0e-6ba5a44e16c4(OCS.15).png "Error de acoplamiento de MMC del generador de topología de Lync Server")</span><span class="sxs-lookup"><span data-stu-id="7bf5e-127">![Lync Server Topology Builder MMC Snap Error](images/JJ205420.f6666343-c348-4d81-ae0e-6ba5a44e16c4(OCS.15).png "Lync Server Topology Builder MMC Snap Error")</span></span>

<span data-ttu-id="7bf5e-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7bf5e-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

