---
title: 'Lync Server 2013: Administrar la infraestructura de red de Lync Server 2013'
description: 'Lync Server 2013: administración de la infraestructura de red de Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Lync Server 2013 network infrastructure
ms:assetid: cb13456a-8f66-4595-be21-8887f30ad4eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182585(v=OCS.15)
ms:contentKeyID: 48185638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab1b5c6fe52374b012063ac26640e9bb25496ad7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425860"
---
# <a name="managing-the-lync-server-2013-network-infrastructure"></a><span data-ttu-id="380bc-103">Administrar la infraestructura de red de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="380bc-103">Managing the Lync Server 2013 network infrastructure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="380bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="380bc-104">

<span> </span></span></span>

<span data-ttu-id="380bc-105">_**Última modificación del tema:** 2014-02-11_</span><span class="sxs-lookup"><span data-stu-id="380bc-105">_**Topic Last Modified:** 2014-02-11_</span></span>

<span data-ttu-id="380bc-106">Microsoft Lync Server 2013 incluye compatibilidad con control de admisión de llamadas (CAC) y omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="380bc-106">Microsoft Lync Server 2013 includes support for call admission control (CAC) and media bypass.</span></span> <span data-ttu-id="380bc-107">Para implementar estas características, debe configurar una red de regiones, sitios, subredes, etc. que le permitan administrar el ancho de banda en situaciones en las que es necesario restringir las transmisiones de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="380bc-107">To implement these features you must configure a network of regions, sites, subnets, and so on that will allow you to manage bandwidth in situations where audio and video transmissions need to be restricted.</span></span> <span data-ttu-id="380bc-108">También puede usar la tecnología de red de calidad de servicio (QoS) para ofrecer una experiencia de usuario final óptima para las comunicaciones de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="380bc-108">You can also use the Quality of Service (QoS) networking technology to help provide an optimal end-user experience for audio and video communications.</span></span>

<span data-ttu-id="380bc-109">Puede usar el panel de control de Lync Server para configurar y administrar CAC, archivos de omisión y QoS.</span><span class="sxs-lookup"><span data-stu-id="380bc-109">You can use the Lync Server Control Panel to set up and manage CAC, media bypass, and QoS.</span></span> <span data-ttu-id="380bc-110">En los siguientes temas se proporcionan los pasos para realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="380bc-110">The following topics provide steps for how to do this.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="380bc-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="380bc-111">In This Section</span></span>

  - [<span data-ttu-id="380bc-112">Administración de calidad de servicio (QoS) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="380bc-112">Managing Quality of Service (QoS) in Lync Server 2013</span></span>](lync-server-2013-managing-quality-of-service-qos.md)

  - [<span data-ttu-id="380bc-113">Administración del control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="380bc-113">Managing call admission control in Lync Server 2013</span></span>](lync-server-2013-managing-call-admission-control.md)

  - [<span data-ttu-id="380bc-114">Interfaces de red de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="380bc-114">Lync Server 2013 network interfaces</span></span>](lync-server-2013-lync-server-network-interfaces.md)

  - [<span data-ttu-id="380bc-115">Impedir nuevas conexiones a Lync Server 2013 para el mantenimiento del servidor</span><span class="sxs-lookup"><span data-stu-id="380bc-115">Prevent new connections to Lync Server 2013 for server maintenance</span></span>](lync-server-2013-prevent-new-connections-to-lync-server-for-server-maintenance.md)

  - [<span data-ttu-id="380bc-116">Metodología de calidad de llamadas de Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="380bc-116">Lync Call Quality Methodology in Lync Server 2013</span></span>](lync-server-2013-poster-lync-call-quality-methodology.md)

  - [<span data-ttu-id="380bc-117">Indicadores clave de estado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="380bc-117">Key Health Indicators in Lync Server 2013</span></span>](lync-server-2013-poster-key-health-indicators.md)

<span data-ttu-id="380bc-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="380bc-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

