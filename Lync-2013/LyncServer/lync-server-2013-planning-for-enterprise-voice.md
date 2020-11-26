---
title: 'Lync Server 2013: planificación de telefonía IP empresarial'
description: 'Lync Server 2013: planificación de telefonía IP empresarial.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Enterprise Voice
ms:assetid: fd8d5867-0ac9-47f8-94f0-1c3ee5e25575
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413081(v=OCS.15)
ms:contentKeyID: 48185959
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4dfa0d91fe8270e49524d648ef403cd69ede2407
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424586"
---
# <a name="planning-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="30d38-103">Planificación de telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-103">Planning for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30d38-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30d38-104">

<span> </span></span></span>

<span data-ttu-id="30d38-105">_**Última modificación del tema:** 2013-11-01_</span><span class="sxs-lookup"><span data-stu-id="30d38-105">_**Topic Last Modified:** 2013-11-01_</span></span>

<span data-ttu-id="30d38-106">El proceso de implementación de telefonía IP empresarial depende de la topología, la infraestructura y la funcionalidad de telefonía IP de empresa que desee admitir.</span><span class="sxs-lookup"><span data-stu-id="30d38-106">The deployment process for Enterprise Voice depends on your existing topology, infrastructure, and the Enterprise Voice functionality that you want to support.</span></span> <span data-ttu-id="30d38-107">Los procedimientos necesarios dependerán de las características que seleccione, pero también es preciso tener en cuenta otros aspectos de la planeación que se necesitan realizar en un nivel más específico.</span><span class="sxs-lookup"><span data-stu-id="30d38-107">The required procedures will depend on what features you choose, but there are other planning considerations that you must make at a high level.</span></span>

<span data-ttu-id="30d38-108">En general, hay que tener en cuenta el tipo y la cantidad de sitios que se quiere implementar, así como sus ubicaciones geográficas, el volumen de llamadas de cada sitio, las clases de vínculos de red que conectan sitios, si se quiere proporcionar redundancia y conmutación por error para la función de voz en cada sitio y, asimismo, si se quiere usar el equipo de PBX existente.</span><span class="sxs-lookup"><span data-stu-id="30d38-108">In general, consider the type and number of sites that you want to deploy and their geographical locations, the call volume at each site, the types of network links that connect sites, whether you want to provide redundancy and failover for voice functionality for each site, and whether you want to use existing PBX equipment.</span></span> <span data-ttu-id="30d38-109">Hay ciertas consideraciones, como la alta disponibilidad, que debe tener en cuenta al planear el software de comunicaciones de Lync Server como un todo.</span><span class="sxs-lookup"><span data-stu-id="30d38-109">There are certain considerations, such as high availability, that you should consider when you plan for Lync Server  communications software as a whole.</span></span> <span data-ttu-id="30d38-110">Estas consideraciones se tratan en los distintos temas de esta sección.</span><span class="sxs-lookup"><span data-stu-id="30d38-110">These considerations are discussed in topics throughout this section, as needed.</span></span>

<div>

## <a name="planning-considerations"></a><span data-ttu-id="30d38-111">Consideraciones de planeación</span><span class="sxs-lookup"><span data-stu-id="30d38-111">Planning Considerations</span></span>

<span data-ttu-id="30d38-112">Para conocer las decisiones de planeación relacionadas con la implementación de una funcionalidad de telefonía empresarial determinada o un componente o escenario de implementación, consulte los temas de esta sección.</span><span class="sxs-lookup"><span data-stu-id="30d38-112">For planning decisions that pertain to the deployment of a particular Enterprise Voice capability or deployment scenario or component, consult the topics in this section.</span></span>

  - [<span data-ttu-id="30d38-113">Definición de los requisitos para la telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-113">Defining your requirements for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-enterprise-voice.md)

  - [<span data-ttu-id="30d38-114">Estimar el uso de voz y el tráfico para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-114">Estimating voice usage and traffic for Lync Server 2013</span></span>](lync-server-2013-estimating-voice-usage-and-traffic.md)

  - [<span data-ttu-id="30d38-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md)

  - [<span data-ttu-id="30d38-116">Components required for Enterprise Voice in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-116">Components required for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-components-required-for-enterprise-voice.md)

  - [<span data-ttu-id="30d38-117">Planear la resistencia de la telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-117">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="30d38-118">Planear la integración de la mensajería unificada de Exchange en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-118">Planning for Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-planning-for-exchange-unified-messaging-integration.md)

  - [<span data-ttu-id="30d38-119">Planear el control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-119">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="30d38-120">Planeación de los servicios de emergencia (E9-1-1) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-120">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="30d38-121">Planificar la omisión de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-121">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

  - [<span data-ttu-id="30d38-122">Planificación de líneas telefónicas privadas con Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-122">Planning for private telephone lines with Lync Server 2013</span></span>](lync-server-2013-planning-for-private-telephone-lines.md)

  - [<span data-ttu-id="30d38-123">Planificar el enrutamiento basado en ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-123">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)

  - [<span data-ttu-id="30d38-124">Planear la resistencia de la telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-124">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="30d38-125">Instrucciones para la implementación de la telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-125">Deployment guidelines for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-enterprise-voice.md)

  - [<span data-ttu-id="30d38-126">Información general sobre el proceso de implementación para telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-126">Deployment process overview for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-process-overview-for-enterprise-voice.md)

  - [<span data-ttu-id="30d38-127">Mover usuarios a telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-127">Moving users to Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-moving-users-to-enterprise-voice.md)

  - [<span data-ttu-id="30d38-128">Herramienta de diagnóstico de PRELLAMADA de Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30d38-128">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>](lync-server-2013-lync-precall-diagnostics-tool.md)

<span data-ttu-id="30d38-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30d38-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

