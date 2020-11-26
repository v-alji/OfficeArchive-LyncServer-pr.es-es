---
title: 'Lync Server 2013: Configuración de troncos'
description: 'Lync Server 2013: configuración de troncos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring trunks
ms:assetid: 0c339511-a185-484e-94f0-dbe918b7e48a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398170(v=OCS.15)
ms:contentKeyID: 48183389
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07d9503cd38419a7145796a6edf8484a14cdeb53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432467"
---
# <a name="configuring-trunks-in-lync-server-2013"></a><span data-ttu-id="75b22-103">Configuración de troncos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-103">Configuring trunks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75b22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75b22-104">

<span> </span></span></span>

<span data-ttu-id="75b22-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="75b22-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="75b22-106">Como parte de la implementación de telefonía IP empresarial, puede configurar un tronco entre un servidor de mediación y uno o más de los siguientes elementos para proporcionar conectividad de red telefónica conmutada (RTC) pública para los clientes y dispositivos de voz de su organización:</span><span class="sxs-lookup"><span data-stu-id="75b22-106">As part of Enterprise Voice deployment, you can configure a trunk between a Mediation Server and one or more of the following peers to provide public switched telephone network (PSTN) connectivity for Enterprise Voice clients and devices in your organization:</span></span>

  - <span data-ttu-id="75b22-107">Conexión basada en troncos SIP para un proveedor de servicio s de telefonía</span><span class="sxs-lookup"><span data-stu-id="75b22-107">SIP trunk connection to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="75b22-108">Puerta de enlace RTC</span><span class="sxs-lookup"><span data-stu-id="75b22-108">PSTN gateway</span></span>

  - <span data-ttu-id="75b22-109">Central de conmutación (PBX)</span><span class="sxs-lookup"><span data-stu-id="75b22-109">Private branch exchange (PBX)</span></span>

<span data-ttu-id="75b22-110">Para obtener más información, consulte [planificación de la conectividad RTC en Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="75b22-110">For details, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) in the Planning documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="75b22-111">Antes de comenzar con la configuración troncal, verifique que se haya creado la topología y que el servidor de mediación y sus pares se hayan configurado y asociado entre sí.</span><span class="sxs-lookup"><span data-stu-id="75b22-111">Before you begin trunk configuration, verify that the topology has been created and that the Mediation Server and its peer have been configured and associated with one another.</span></span> <span data-ttu-id="75b22-112">Para obtener más información, vea <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">definir una puerta de enlace en el generador de topologías de Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="75b22-112">For details, see <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Define a gateway in Topology Builder in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="75b22-113">Como parte de la configuración troncal, puede habilitar la característica de omisión de medios de Lync Server 2013, que permite a los medios omitir el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="75b22-113">As a part of trunk configuration, you can enable the Lync Server 2013 media bypass feature, which enables media to bypass the Mediation Server.</span></span> <span data-ttu-id="75b22-114">Los troncos se pueden configurar con o sin omisión de medios habilitados, pero le recomendamos encarecidamente que lo habilite.</span><span class="sxs-lookup"><span data-stu-id="75b22-114">Trunks can be configured either with or without media bypass enabled, but we strongly recommend that you enable it.</span></span> <span data-ttu-id="75b22-115">Para obtener más información, consulte <A href="lync-server-2013-planning-for-media-bypass.md">planificación de la omisión de medios en Lync Server 2013</A> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="75b22-115">For details, see <A href="lync-server-2013-planning-for-media-bypass.md">Planning for media bypass in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="75b22-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="75b22-116">In This Section</span></span>

  - [<span data-ttu-id="75b22-117">Compatibilidad con varios troncales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-117">Multiple trunk support in Lync Server 2013</span></span>](lync-server-2013-multiple-trunk-support.md)

  - [<span data-ttu-id="75b22-118">Enrutamiento entre troncales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-118">Inter-trunk routing in Lync Server 2013</span></span>](lync-server-2013-inter-trunk-routing.md)

  - [<span data-ttu-id="75b22-119">Ver la información de configuración troncal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-119">View trunk configuration information in Lync Server 2013</span></span>](lync-server-2013-view-trunk-configuration-information.md)

  - [<span data-ttu-id="75b22-120">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-120">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)

  - [<span data-ttu-id="75b22-121">Configurar un tronco sin omisión de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-121">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)

  - [<span data-ttu-id="75b22-122">Crear una nueva colección de opciones de configuración de troncal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-122">Create a new collection of trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-a-new-collection-of-trunk-configuration-settings.md)

  - [<span data-ttu-id="75b22-123">Eliminar una colección existente de parámetros de configuración del tronco de SIP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-123">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="75b22-124">Modificar la configuración de los enlaces de SIP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-124">Modify SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-modify-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="75b22-125">Probar la configuración del tronco del SIP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-125">Test SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-test-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="75b22-126">Ver información sobre los troncos SIP individuales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-126">View information about individual SIP trunks in Lync Server 2013</span></span>](lync-server-2013-view-information-about-individual-sip-trunks.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="75b22-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="75b22-127">See Also</span></span>


[<span data-ttu-id="75b22-128">Definir una puerta de enlace en el generador de topología de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-128">Define a gateway in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-define-a-gateway-in-topology-builder.md)  


[<span data-ttu-id="75b22-129">Planificación de la conectividad RTC en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-129">Planning for PSTN connectivity in Lync Server 2013</span></span>](lync-server-2013-planning-for-pstn-connectivity.md)  
[<span data-ttu-id="75b22-130">Planificar la omisión de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b22-130">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="75b22-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75b22-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

