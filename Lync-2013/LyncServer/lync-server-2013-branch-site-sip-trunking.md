---
title: 'Lync Server 2013: Troncalización SIP de sitio de sucursal'
description: 'Lync Server 2013: Troncalización SIP de sitio de sucursal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Branch site SIP trunking
ms:assetid: c4d9dfcd-8baa-41ea-9677-48b0e429429d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412974(v=OCS.15)
ms:contentKeyID: 48185350
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33e408a462c21ffa6df6e6a2aee50d7b87dca1f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435946"
---
# <a name="branch-site-sip-trunking-in-lync-server-2013"></a><span data-ttu-id="2ab23-103">Branch site SIP trunking in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ab23-103">Branch site SIP trunking in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ab23-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ab23-104">

<span> </span></span></span>

<span data-ttu-id="2ab23-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="2ab23-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="2ab23-106">En algunos casos, es posible que necesites implementar el troncal de SIP distribuido en los sitios de sucursales seleccionados.</span><span class="sxs-lookup"><span data-stu-id="2ab23-106">In some cases, you may need to implement distributed SIP trunking at selected branch sites.</span></span> <span data-ttu-id="2ab23-107">Para determinar si es necesario un tronco de SIP para un sitio de sucursal, revise la información en [cómo implementar la Troncalización SIP en Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span><span class="sxs-lookup"><span data-stu-id="2ab23-107">To determine whether a SIP trunk is needed for a branch site, review the information in [How do I implement SIP trunking in Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span></span>

<span data-ttu-id="2ab23-108">Para obtener más información sobre las opciones de topología compatibles para implementar los troncos SIP en sitios de sucursales, consulte [soluciones de resistencia de sitio de sucursal en Lync Server 2013](lync-server-2013-branch-site-resiliency-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="2ab23-108">For details about the supported topology options for deploying SIP trunks in branch sites, see [Branch-site resiliency solutions in Lync Server 2013](lync-server-2013-branch-site-resiliency-solutions.md).</span></span>

<div>

## <a name="example-branch-site-sip-trunk-requirements-analysis"></a><span data-ttu-id="2ab23-109">Ejemplo de análisis de requisitos de un tronco SIP de sitio de sucursal</span><span class="sxs-lookup"><span data-stu-id="2ab23-109">Example Branch Site SIP Trunk Requirements Analysis</span></span>

<span data-ttu-id="2ab23-110">Si decide implementar un tronco SIP de sitio de sucursal, debe realizar un análisis de costos específico del sitio.</span><span class="sxs-lookup"><span data-stu-id="2ab23-110">When you decide to deploy a branch site SIP trunk, you need to perform a site-specific cost analysis.</span></span> <span data-ttu-id="2ab23-111">Por ejemplo, una empresa que tiene un sitio central en Redmond, Washington y un sitio de sucursal en Nueva York debe realizar un análisis para determinar si implementar un tronco SIP desde el sitio de Nueva York a un proveedor de servicios locales.</span><span class="sxs-lookup"><span data-stu-id="2ab23-111">For example, an enterprise that has a central site in Redmond, Washington, and a branch site in New York, should do an analysis to determine whether to implement a SIP trunk from the New York site to a local service provider.</span></span>

<span data-ttu-id="2ab23-112">Para determinar si un tronco SIP distribuido en Nueva York es rentable, identifica qué números de llamada directa a la extensión (DID) usarán el tronco SIP y analiza la cantidad de llamadas que Nueva York realiza a áreas que no sean Redmond (425).</span><span class="sxs-lookup"><span data-stu-id="2ab23-112">To determine whether a distributed SIP trunk in New York is cost-effective, identify which Direct Inward Dialing (DID) numbers will use the SIP trunk, and analyze the number of calls New York makes to areas other than Redmond (425).</span></span> <span data-ttu-id="2ab23-113">Puede haber finalizado el sitio de la sucursal en el sitio central.</span><span class="sxs-lookup"><span data-stu-id="2ab23-113">You can have DID termination for the branch site at the central site.</span></span> <span data-ttu-id="2ab23-114">Por ejemplo, el sitio central de Redmond puede hospedar números para el sitio de sucursal de Nueva York.</span><span class="sxs-lookup"><span data-stu-id="2ab23-114">For example, the Redmond central site can host DID numbers for the New York branch site.</span></span> <span data-ttu-id="2ab23-115">Si el precio de la implementación de un tronco de SIP distribuido es menor que el precio de esas llamadas, considere la posibilidad de implementar un tronco del SIP en el sitio de la sucursal de Nueva York.</span><span class="sxs-lookup"><span data-stu-id="2ab23-115">If the cost of implementing a distributed SIP trunk is less than the cost of those calls, consider implementing a SIP trunk at the New York branch site.</span></span>

</div>

<div>

## <a name="other-branch-site-sip-trunk-requirements"></a><span data-ttu-id="2ab23-116">Otros requisitos de un tronco SIP de sitio de sucursal</span><span class="sxs-lookup"><span data-stu-id="2ab23-116">Other Branch Site SIP Trunk Requirements</span></span>

<span data-ttu-id="2ab23-117">La elección entre implementar un tronco SIP en lugar de una puerta de enlace se basa en la diferencia entre las tarifas de la red telefónica conmutada (RTC) de larga distancia de cada opción.</span><span class="sxs-lookup"><span data-stu-id="2ab23-117">The choice between a deploying a SIP trunk instead of a gateway is based on the difference between the public switched telephone network (PSTN) long distance toll charges of each option.</span></span> <span data-ttu-id="2ab23-118">Si implementa un tronco SIP de sitio de sucursal, también necesita determinar los requisitos de resistencia y ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="2ab23-118">If you deploy a branch site SIP trunk, you also need to determine your resiliency and bandwidth requirements.</span></span> <span data-ttu-id="2ab23-119">Si el vínculo entre el sitio de la sucursal y el sitio central es resistente y tiene suficiente ancho de banda, puede implementar un tronco SIP o una puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="2ab23-119">If the link between your branch site and central site is resilient and has sufficient bandwidth, you can deploy a SIP trunk or a gateway.</span></span> <span data-ttu-id="2ab23-120">No es necesario implementar una aplicación de rama que sea superviviente en el sitio de la sucursal.</span><span class="sxs-lookup"><span data-stu-id="2ab23-120">You do not need to deploy a Survivable Branch Appliance at the branch site.</span></span> <span data-ttu-id="2ab23-121">Si el vínculo entre el sitio de la sucursal y el sitio central no es resistente, implemente un dispositivo de sucursal con la supervivencia o implemente un servidor de sucursal que sea reviviente con una puerta de enlace o un tronco SIP en el sitio de la sucursal.</span><span class="sxs-lookup"><span data-stu-id="2ab23-121">If the link between your branch site and central site is not resilient, deploy a Survivable Branch Appliance, or deploy a Survivable Branch Server with either a gateway or SIP trunk at the branch site.</span></span>

<span data-ttu-id="2ab23-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ab23-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

