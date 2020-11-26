---
title: 'Lync Server 2013: Acerca de las regiones de red, sitios y subredes'
description: 'Lync Server 2013: acerca de las regiones, sitios y subredes de la red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: About network regions, sites, and subnets
ms:assetid: 6662123a-d011-408c-a290-92b2a8589943
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398467(v=OCS.15)
ms:contentKeyID: 48184335
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3c7f660f3c72003527e0721c3f9702865e9b9b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439523"
---
# <a name="about-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="28423-103">Acerca de las regiones de red, sitios y subredes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="28423-103">About network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28423-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28423-104">

<span> </span></span></span>

<span data-ttu-id="28423-105">_**Última modificación del tema:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="28423-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="28423-106">Las características avanzadas de voz empresarial descritas en esta sección comparten ciertos requisitos de configuración para regiones de red, sitios de red y subredes.</span><span class="sxs-lookup"><span data-stu-id="28423-106">The advanced Enterprise Voice features described in this section share certain configuration requirements for network regions, network sites, and subnets.</span></span> <span data-ttu-id="28423-107">Por ejemplo, las tres características avanzadas requieren que cada subred de su topología esté asociada a un sitio de *red* específico, y cada sitio de red debe estar asociado a una *región de red*.</span><span class="sxs-lookup"><span data-stu-id="28423-107">For example, all three advanced features require that each subnet in your topology be associated with a specific *network site*, and each network site must be associated with a *network region*.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="28423-108">Antes de comenzar con la configuración de red de control de admisión de llamadas, E9-1-1 o omisión de medios, asegúrese de que ha revisado información adicional sobre la configuración de red en el tema <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">configuración de red para características avanzadas de telefonía por voz de Lync Server 2013</A> en la documentación de planificación.</span><span class="sxs-lookup"><span data-stu-id="28423-108">Before you begin network configuration for call admission control, E9-1-1, or media bypass, make sure that you reviewed additional information about network settings in the <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Network settings for the advanced Enterprise Voice features in Lync Server 2013</A> topic in the Planning documentation.</span></span> <span data-ttu-id="28423-109">Para obtener información sobre la configuración de red principalmente sobre el control de admisión de llamadas, vea también <A href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">definir los requisitos para el control de admisión de llamadas en Lync Server 2013</A> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="28423-109">For details about network configuration primarily about call admission control, also see <A href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<span data-ttu-id="28423-110">El control de admisión de llamadas y E9-1-1 tienen requisitos de configuración adicionales para los sitios de red:</span><span class="sxs-lookup"><span data-stu-id="28423-110">Call admission control and E9-1-1 have additional configuration requirements for network sites:</span></span>

  - <span data-ttu-id="28423-111">El control de admisión de llamadas requiere que se especifique un   *perfil de directiva de ancho de banda* para cada uno de los sitios restringidos con limitaciones de ancho de banda WAN.</span><span class="sxs-lookup"><span data-stu-id="28423-111">Call admission control requires that a *bandwidth policy profile* be specified for each site that is constrained by WAN bandwidth limitations.</span></span> <span data-ttu-id="28423-112">Si planea implementar el control de admisión de llamadas, debe [crear perfiles de directiva de ancho de banda en Lync Server 2013 antes de](lync-server-2013-create-bandwidth-policy-profiles.md) configurar los sitios de red.</span><span class="sxs-lookup"><span data-stu-id="28423-112">If you plan to deploy call admission control, you must [Create bandwidth policy profiles in Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md) before you configure your network sites.</span></span>

  - <span data-ttu-id="28423-113">E9-1-1 requiere que se especifique una *directiva de ubicación* para cada uno de los sitios.</span><span class="sxs-lookup"><span data-stu-id="28423-113">E9-1-1 requires that a *location policy* be specified for each site.</span></span> <span data-ttu-id="28423-114">Si tiene previsto implementar E9-1-1, debe [crear directivas de ubicación en Lync Server 2013](lync-server-2013-create-location-policies.md) antes de configurar los sitios de red.</span><span class="sxs-lookup"><span data-stu-id="28423-114">If you plan to deploy E9-1-1, you must [Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md) before you configure your network sites.</span></span>

<div>

## <a name="create-or-modify-network-regions-network-sites-and-subnets"></a><span data-ttu-id="28423-115">Crear o modificar regiones de red, sitios de red y subredes</span><span class="sxs-lookup"><span data-stu-id="28423-115">Create or Modify Network Regions, Network Sites, and Subnets</span></span>

<span data-ttu-id="28423-116">En los siguientes temas se proporcionan pasos para crear o modificar regiones de red y sitios de red, y para asociar subredes a sitios de red.</span><span class="sxs-lookup"><span data-stu-id="28423-116">The following topics provide steps to create or modify network regions and network sites, and to associate subnets with network sites.</span></span> <span data-ttu-id="28423-117">Estos temas no son específicos de ninguna característica avanzada empresarial de voz en particular.</span><span class="sxs-lookup"><span data-stu-id="28423-117">These topics are not specific to any particular advanced Enterprise Voice feature.</span></span>

  - [<span data-ttu-id="28423-118">Crear o modificar una región de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="28423-118">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)

  - [<span data-ttu-id="28423-119">Crear o modificar un sitio de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="28423-119">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)

  - [<span data-ttu-id="28423-120">Asociar una subred a un sitio de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="28423-120">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)

<span data-ttu-id="28423-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28423-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

