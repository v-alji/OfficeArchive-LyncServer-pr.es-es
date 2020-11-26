---
title: 'Lync Server 2013: administración de control de admisión de llamadas'
description: 'Lync Server 2013: administración de control de admisión de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing call admission control
ms:assetid: b0bd4783-6f47-408d-b010-2e30f9bc1770
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721851(v=OCS.15)
ms:contentKeyID: 49733784
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a1c01bff6d1dce48dea314b6704cc0f5ff7d6b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425965"
---
# <a name="managing-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="27d0a-103">Administración del control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-103">Managing call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27d0a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27d0a-104">

<span> </span></span></span>

<span data-ttu-id="27d0a-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="27d0a-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="27d0a-106">El control de admisión de llamadas (CAC) determina, en base al ancho de banda de la red disponible, si está permitido establecer sesiones de comunicación en tiempo real, como son las llamadas de voz o vídeo.</span><span class="sxs-lookup"><span data-stu-id="27d0a-106">Call admission control (CAC) determines, based on available network bandwidth, whether to allow real-time communications sessions such as voice or video calls to be established.</span></span> <span data-ttu-id="27d0a-107">Use los procedimientos siguientes para administrar las distintas características de CAC para el entorno de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="27d0a-107">Use the following procedures to manage different CAC features for your Lync Server 2013 environment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="27d0a-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="27d0a-108">In This Section</span></span>

  - [<span data-ttu-id="27d0a-109">Habilitar el control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-109">Enabling call admission control in Lync Server 2013</span></span>](lync-server-2013-enabling-call-admission-control.md)

  - [<span data-ttu-id="27d0a-110">Administrar perfiles de directiva de ancho de banda de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-110">Managing network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-managing-network-bandwidth-policy-profiles.md)

  - [<span data-ttu-id="27d0a-111">Regiones de red de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-111">Network regions in Lync Server 2013</span></span>](lync-server-2013-network-regions.md)

  - [<span data-ttu-id="27d0a-112">Rutas de la región de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-112">Network region routes in Lync Server 2013</span></span>](lync-server-2013-network-region-routes.md)

  - [<span data-ttu-id="27d0a-113">Control de admisión de llamadas para sitios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-113">Call admission control for sites in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-for-sites.md)

  - [<span data-ttu-id="27d0a-114">Habilitar y deshabilitar la omisión de elementos multimedia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-114">Enabling and disabling media bypass in Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-media-bypass.md)

  - [<span data-ttu-id="27d0a-115">Vincular regiones de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-115">Linking network regions in Lync Server 2013</span></span>](lync-server-2013-linking-network-regions.md)

  - [<span data-ttu-id="27d0a-116">Administración de subredes de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-116">Managing network subnets in Lync Server 2013</span></span>](lync-server-2013-managing-network-subnets.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="27d0a-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="27d0a-117">See Also</span></span>


[<span data-ttu-id="27d0a-118">Información general sobre el control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27d0a-118">Overview of call admission control in Lync Server 2013</span></span>](lync-server-2013-overview-of-call-admission-control.md)  
  

<span data-ttu-id="27d0a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27d0a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

