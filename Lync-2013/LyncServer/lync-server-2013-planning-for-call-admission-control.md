---
title: 'Lync Server 2013: Planear el control de admisión de llamadas'
description: 'Lync Server 2013: planificación de control de admisión de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for call admission control (CAC)
ms:assetid: ca367138-adf5-4119-bc40-5ddf335ed22f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398842(v=OCS.15)
ms:contentKeyID: 48185652
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: afbc3ca411fcf0a3a1c869a23cddccdb87f09ed6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437045"
---
# <a name="planning-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="ddd0f-103">Planear el control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddd0f-103">Planning for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ddd0f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ddd0f-104">

<span> </span></span></span>

<span data-ttu-id="ddd0f-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="ddd0f-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="ddd0f-106">En el caso de las aplicaciones de comunicaciones unificadas (UC) que se basan en IP, como la telefonía, el vídeo y el uso compartido de aplicaciones, generalmente no se considera que el ancho de banda disponible de las redes empresariales sea un factor limitador dentro de entornos LAN.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-106">For unified communications (UC) applications that are IP-based, such as telephony, video, and application sharing, the available bandwidth of enterprise networks is not generally considered to be a limiting factor within LAN environments.</span></span> <span data-ttu-id="ddd0f-107">Sin embargo, en los vínculos WAN que conectan sitios entre sí, el ancho de banda de red puede restringirse.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-107">However, on WAN links that interconnect sites, network bandwidth can be limited.</span></span> <span data-ttu-id="ddd0f-108">Cuando un flujo de tráfico de red sobrescribirá un vínculo WAN, se usarán mecanismos actuales como colas, almacenamiento en búfer y descartar paquetes para resolver la congestión.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-108">When an influx of network traffic oversubscribes a WAN link, current mechanisms such as queuing, buffering, and packet dropping are used to resolve the congestion.</span></span> <span data-ttu-id="ddd0f-109">El tráfico adicional se retrasa generalmente hasta que la red se acelera o, si es necesario, se pierde el tráfico.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-109">The extra traffic is typically delayed until the network congestion eases or, if necessary, the traffic is dropped.</span></span> <span data-ttu-id="ddd0f-110">Para el tráfico de datos convencionales en estas situaciones, el cliente receptor puede recuperarse.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-110">For conventional data traffic in such situations, the receiving client can recover.</span></span> <span data-ttu-id="ddd0f-111">Para el tráfico en tiempo real, como las comunicaciones unificadas, la congestión de red no se puede resolver de esta manera, porque el tráfico de comunicaciones unificadas es sensible a la latencia y a la pérdida de paquetes.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-111">For real-time traffic such as unified communications, network congestion cannot be resolved in this manner, because the unified communications traffic is sensitive to both latency and packet loss.</span></span> <span data-ttu-id="ddd0f-112">La congestión de la WAN puede dar lugar a una experiencia de calidad deficiente para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-112">Congestion on the WAN can result in a poor Quality of Experience (QoE) for users.</span></span> <span data-ttu-id="ddd0f-113">Para el tráfico en tiempo real en condiciones congestionadas, es mejor denegar las llamadas que proporcionar conexiones de baja calidad.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-113">For real-time traffic in congested conditions, it is better to deny calls than to provide connections with poor quality.</span></span>

<span data-ttu-id="ddd0f-114">El servicio de control de admisión de llamadas (CAC) determina si hay suficiente ancho de banda de red para establecer una sesión en tiempo real con una calidad aceptable.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-114">Call admission control (CAC) determines whether there is sufficient network bandwidth to establish a real-time session of acceptable quality.</span></span> <span data-ttu-id="ddd0f-115">En Lync Server 2013, CAC controla el tráfico en tiempo real solo para audio y vídeo, pero no afecta al tráfico de datos.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-115">In Lync Server 2013, CAC controls real-time traffic only for audio and video, but it does not affect data traffic.</span></span> <span data-ttu-id="ddd0f-116">Si la ruta de acceso de WAN predeterminada no tiene el ancho de banda necesario, CAC puede intentar redirigir la llamada a través de una ruta de acceso de Internet o a través de la red telefónica conmutada (RTC).</span><span class="sxs-lookup"><span data-stu-id="ddd0f-116">If the default WAN path does not have the required bandwidth, CAC can attempt to route the call through an Internet path or the public switched telephone network (PSTN).</span></span> <span data-ttu-id="ddd0f-117">CAC solo está disponible en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-117">CAC is available only in Lync Server.</span></span>

<span data-ttu-id="ddd0f-118">En esta sección se describen las funciones del servicio de control de admisión de llamadas y explica cómo planificar para CAC.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-118">This section describes the call admission control functionality and explains how to plan for CAC.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ddd0f-119">Lync Server tiene tres características avanzadas de Enterprise Voice: control de admisión de llamadas (CAC), servicios de emergencia (E9-1-1) y omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-119">Lync Server has three advanced Enterprise Voice features: call admission control (CAC), emergency services (E9-1-1), and media bypass.</span></span> <span data-ttu-id="ddd0f-120">Para obtener una descripción general de la información de planeación común para estas tres características, consulte <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">configuración de red para las características de telefonía avanzada empresarial de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ddd0f-120">For an overview of planning information that is common to all three of these features, see <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Network settings for the advanced Enterprise Voice features in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ddd0f-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ddd0f-121">In This Section</span></span>

  - [<span data-ttu-id="ddd0f-122">Información general sobre el control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddd0f-122">Overview of call admission control in Lync Server 2013</span></span>](lync-server-2013-overview-of-call-admission-control.md)

  - [<span data-ttu-id="ddd0f-123">Definición de los requisitos de la organización para el servicio de control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddd0f-123">Defining your requirements for call admission control in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-call-admission-control.md)

  - [<span data-ttu-id="ddd0f-124">Ejemplo: recopilar los requisitos para el control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddd0f-124">Example: Gathering your requirements for call admission control in Lync Server 2013</span></span>](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md)

  - [<span data-ttu-id="ddd0f-125">Componentes y topologías para CAC en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddd0f-125">Components and topologies for CAC in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-cac.md)

  - [<span data-ttu-id="ddd0f-126">Procedimientos recomendados para el servicio de control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddd0f-126">Best practices for call admission control in Lync Server 2013</span></span>](lync-server-2013-best-practices-for-call-admission-control.md)

  - [<span data-ttu-id="ddd0f-127">Lista de comprobación para la implementación del control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddd0f-127">Deployment checklist for call admission control in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-call-admission-control.md)

<span data-ttu-id="ddd0f-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ddd0f-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

