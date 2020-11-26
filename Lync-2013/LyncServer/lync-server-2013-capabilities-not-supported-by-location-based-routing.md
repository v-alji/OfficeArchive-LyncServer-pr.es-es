---
title: 'Lync Server 2013: Capacidades no compatibles con el enrutamiento basado en ubicación'
description: 'Lync Server 2013: las funciones no son compatibles con el enrutamiento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capabilities not supported by Location-Based Routing
ms:assetid: c3d54953-a7d6-4465-a6c3-ae411b2d8ea9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994071(v=OCS.15)
ms:contentKeyID: 51803982
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf9cd03a8cbdd50e136605c4f172598b2ad3f523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435610"
---
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="8d276-103">Capacidades no compatibles con el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d276-103">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d276-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d276-104">

<span> </span></span></span>

<span data-ttu-id="8d276-105">_**Última modificación del tema:** 2014-03-12_</span><span class="sxs-lookup"><span data-stu-id="8d276-105">_**Topic Last Modified:** 2014-03-12_</span></span>

<span data-ttu-id="8d276-106">El enrutamiento de Location-Based no se aplica a los siguientes tipos de interacciones.</span><span class="sxs-lookup"><span data-stu-id="8d276-106">Location-Based Routing does not apply to the following types of interactions.</span></span> <span data-ttu-id="8d276-107">Location-Based el enrutamiento no se aplica cuando los puntos de conexión de Lync interactúan con puntos de conexión RTC mediante estas características.</span><span class="sxs-lookup"><span data-stu-id="8d276-107">Location-Based Routing is not enforced when Lync endpoints interact with PSTN endpoints using these capabilities.</span></span>

  - <span data-ttu-id="8d276-108">Marcación RTC para conferencias</span><span class="sxs-lookup"><span data-stu-id="8d276-108">PSTN dial-in to conferences</span></span>

  - <span data-ttu-id="8d276-109">Llamadas RTC entrantes y salientes a través del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="8d276-109">Incoming and outgoing PSTN calls through Response Group</span></span>

  - <span data-ttu-id="8d276-110">Estacionamiento o recuperación de llamadas RTC a través del estacionamiento de llamadas</span><span class="sxs-lookup"><span data-stu-id="8d276-110">Call park or retrieval of PSTN calls through Call Park</span></span>

  - <span data-ttu-id="8d276-111">Llamadas RTC entrantes al servicio de anuncio</span><span class="sxs-lookup"><span data-stu-id="8d276-111">Incoming PSTN calls to Announcement Service</span></span>

  - <span data-ttu-id="8d276-112">Llamadas RTC entrantes recuperadas a través de la atención de llamadas de grupo</span><span class="sxs-lookup"><span data-stu-id="8d276-112">Incoming PSTN calls retrieved via Group Call Pickup</span></span>

<span data-ttu-id="8d276-113">Para exigir Location-Based reglas de enrutamiento a los tipos de interacciones de la siguiente lista, debe habilitar el enrutamiento de Location-Based para las conferencias:</span><span class="sxs-lookup"><span data-stu-id="8d276-113">To enforce Location-Based Routing rules to the types of interactions in the following list, you must enable Location-Based Routing for Conferencing:</span></span>

  - <span data-ttu-id="8d276-114">Iniciar llamadas RTC desde una conferencia</span><span class="sxs-lookup"><span data-stu-id="8d276-114">PSTN dial-out from conferences</span></span>

  - <span data-ttu-id="8d276-115">Escalaciones desde conversaciones de audio de punto a punto a conferencias en las que participen extremos de RTC</span><span class="sxs-lookup"><span data-stu-id="8d276-115">Escalations from peer-to-peer audio conversations to conferencing involving PSTN endpoints</span></span>

  - <span data-ttu-id="8d276-116">Transferencias de consulta con extremos de RTC</span><span class="sxs-lookup"><span data-stu-id="8d276-116">Consultative transfers involving PSTN endpoints</span></span>

<span data-ttu-id="8d276-117">Para habilitar el enrutamiento de Location-Based para conferencias, consulte [enrutamiento basado en ubicación para conferencias en Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="8d276-117">To enable Location-Based Routing for Conferencing, see [Location-Based Routing for conferencing in Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="8d276-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d276-118">See Also</span></span>


[<span data-ttu-id="8d276-119">Planificar el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d276-119">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="8d276-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d276-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

