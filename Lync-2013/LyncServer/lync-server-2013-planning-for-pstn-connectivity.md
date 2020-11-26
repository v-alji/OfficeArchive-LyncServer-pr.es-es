---
title: 'Lync Server 2013: planificación de la conectividad RTC'
description: 'Lync Server 2013: planificación de la conectividad RTC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for PSTN connectivity
ms:assetid: 280f684a-740a-443d-8ecf-574241382a42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425749(v=OCS.15)
ms:contentKeyID: 48183684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45c0df6aa6dc9d9cc8522223056f1834849e6ddb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424439"
---
# <a name="planning-for-pstn-connectivity-in-lync-server-2013"></a><span data-ttu-id="778ee-103">Planificación de la conectividad RTC en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="778ee-103">Planning for PSTN connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="778ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="778ee-104">

<span> </span></span></span>

<span data-ttu-id="778ee-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="778ee-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="778ee-106">Una solución VoIP empresarial necesita proporcionar llamadas entrantes y salientes a la red telefónica conmutada (RTC) sin que la calidad de servicio (QoS) se vea afectada.</span><span class="sxs-lookup"><span data-stu-id="778ee-106">An enterprise-grade VoIP solution must provide for calls to and from the public switched telephone network (PSTN) without any decline in Quality of Service (QoS).</span></span> <span data-ttu-id="778ee-107">Los usuarios que realicen y reciban llamadas no deben ser conscientes de la tecnología subyacente: desde el punto de vista del usuario, una llamada entre la infraestructura de telefonía IP empresarial y la RTC debe parecer simplemente otra llamada telefónica.</span><span class="sxs-lookup"><span data-stu-id="778ee-107">Users who place and receive calls should not be aware of the underlying technology: from the user's perspective, a call between the Enterprise Voice infrastructure and the PSTN should seem like just another phone call.</span></span>

<span data-ttu-id="778ee-108">Lync Server 2013 proporciona conectividad RTC confiable y escalable con las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="778ee-108">Lync Server 2013 provides reliable, scalable PSTN connectivity by using the following options:</span></span>

  - <span data-ttu-id="778ee-109">**Troncos SIP** a un proveedor de servicios de telefonía por Internet (ITSP)</span><span class="sxs-lookup"><span data-stu-id="778ee-109">**SIP trunks** to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="778ee-110">**Conexiones SIP directas** a una puerta de enlace RTC</span><span class="sxs-lookup"><span data-stu-id="778ee-110">**Direct SIP connections** to a PSTN gateway</span></span>

  - <span data-ttu-id="778ee-111">**Conexiones SIP directas** a una PBX</span><span class="sxs-lookup"><span data-stu-id="778ee-111">**Direct SIP connections** to a PBX</span></span>

<span data-ttu-id="778ee-112">Según cuál sea el tamaño, la cobertura geográfica y la infraestructura de voz existente de una organización, es posible usar una, dos o todas estas opciones en diversas ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="778ee-112">Depending on its size, geographic coverage, and existing voice infrastructure, an enterprise may use one, two, or even all three of these options at various locations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="778ee-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="778ee-113">In This Section</span></span>

  - [<span data-ttu-id="778ee-114">Troncalización SIP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="778ee-114">SIP trunking in Lync Server 2013</span></span>](lync-server-2013-sip-trunking.md)

  - [<span data-ttu-id="778ee-115">Conexiones SIP directas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="778ee-115">Direct SIP connections in Lync Server 2013</span></span>](lync-server-2013-direct-sip-connections.md)

  - [<span data-ttu-id="778ee-116">M:N troncal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="778ee-116">M:N trunk in Lync Server 2013</span></span>](lync-server-2013-m-n-trunk.md)

  - [<span data-ttu-id="778ee-117">Reglas de traducción en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="778ee-117">Translation rules in Lync Server 2013</span></span>](lync-server-2013-translation-rules.md)

  - [<span data-ttu-id="778ee-118">Planeación del enrutamiento de voz saliente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="778ee-118">Planning outbound voice routing in Lync Server 2013</span></span>](lync-server-2013-planning-outbound-voice-routing.md)

<span data-ttu-id="778ee-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="778ee-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

