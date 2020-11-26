---
title: 'Lync Server 2013: compatibilidad con múltiples troncales'
description: 'Lync Server 2013: compatibilidad con múltiples enlaces.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Multiple trunk support
ms:assetid: a1309c09-ad9a-4c54-9650-4e3f5b2a4a00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205127(v=OCS.15)
ms:contentKeyID: 48184948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3bbabb90405b3fdae47a59ba8a0798743943216d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425206"
---
# <a name="multiple-trunk-support-in-lync-server-2013"></a><span data-ttu-id="8cdc3-103">Compatibilidad con varios troncales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8cdc3-103">Multiple trunk support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8cdc3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8cdc3-104">

<span> </span></span></span>

<span data-ttu-id="8cdc3-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="8cdc3-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="8cdc3-106">La funcionalidad de Lync Server 2013 admite varias asociaciones entre puertas de enlace y servidores de mediación.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-106">Lync Server 2013 functionality supports multiple associations between gateways and Mediation Servers.</span></span> <span data-ttu-id="8cdc3-107">Estas asociaciones se realizan mediante la definición de un tronco, que es una asociación lógica entre un grupo de servidores de mediación y una puerta de enlace de red de telefonía pública conmutada (RTC), controlador de borde de sesión (SBC) o IP-PBX.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-107">These associations are made by defining a trunk, which is a logical association between a Mediation Server pool and a public switched telephone network (PSTN) gateway, Session Border Controller (SBC), or IP-PBX.</span></span> <span data-ttu-id="8cdc3-108">Use el generador de topología para asociar puertas de enlace con servidores de mediación (es decir, troncos).</span><span class="sxs-lookup"><span data-stu-id="8cdc3-108">Use the Topology Builder to associate gateways with Mediation Servers (that is, trunks).</span></span>

  - <span data-ttu-id="8cdc3-109">Para asignar o quitar un tronco en Lync Server 2013, primero debe definir un tronco en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-109">To assign or remove a trunk in Lync Server 2013, you must first define a trunk in Topology Builder.</span></span> <span data-ttu-id="8cdc3-110">Un tronco consiste en la siguiente Asociación: nombre de dominio completo (FQDN) de Media Server, el puerto de escucha del servidor de mediación, el FQDN de la puerta de enlace y el puerto de escucha de la puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-110">A trunk consists of the following association: Mediation Server fully qualified domain name (FQDN), the Mediation Server listening port, the gateway FQDN, and the gateway listening port.</span></span>

  - <span data-ttu-id="8cdc3-111">Para configurar varios troncos, puede crear varias asociaciones entre la misma puerta de enlace y el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-111">To configure multiple trunks, you can create multiple associations between the same gateway and the Mediation Server.</span></span> <span data-ttu-id="8cdc3-112">Esto proporciona resistencia adicional a la infraestructura de telefonía IP empresarial, que es especialmente útil en escenarios de interoperabilidad de la intercambiación privada (PBX).</span><span class="sxs-lookup"><span data-stu-id="8cdc3-112">This provides additional resiliency to the Enterprise Voice infrastructure, which is especially useful in private branch exchange (PBX) interoperational scenarios.</span></span>

<span data-ttu-id="8cdc3-113">Cuando se define un tronco, debe estar asociado con una ruta.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-113">When a trunk is defined, it must be associated to a route.</span></span> <span data-ttu-id="8cdc3-114">Para asociar un tronco a una ruta, defina un nombre simple para el tronco en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-114">To associate a trunk to a route, you define a simple name for the trunk in Topology Builder.</span></span> <span data-ttu-id="8cdc3-115">Este nombre simple se usa como el nombre del tronco en el panel de control de Lync Server, donde los troncos se pueden asociar a rutas.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-115">This simple name is used as the trunk name in the Lync Server Control Panel, where trunks can be associated with routes.</span></span> <span data-ttu-id="8cdc3-116">El nombre de tronco simple se usa como nombre de la puerta de enlace desde el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-116">The simple trunk name is used as the gateway name from the Lync Server Management Shell.</span></span>

    New-CsVoiceRoute -Identity <RouteId> -NumberPattern <String> -PstnUsages @{add="<UsageString>"} -PstnGatewayList @{add="<TrunkSimpleName>"}

<span data-ttu-id="8cdc3-117">El administrador debe seleccionar un tronco predeterminado asociado a un servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-117">The administrator must select a default trunk associated with a Mediation Server.</span></span> <span data-ttu-id="8cdc3-118">En el generador de topología, haga clic con el botón secundario en el servidor de mediación asociado y luego haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-118">From the Topology Builder, right-click the associated Mediation Server, and then click **Properties**.</span></span> <span data-ttu-id="8cdc3-119">Especificar la puerta de enlace predeterminada para el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-119">Specify the default gateway for the Mediation Server.</span></span>

<span data-ttu-id="8cdc3-120">En el siguiente diagrama se muestran los diversos troncos que se definen para cada servidor de mediación y puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="8cdc3-120">The following diagram illustrates the multiple trunks that are defined for each Mediation Server and gateway.</span></span>

<span data-ttu-id="8cdc3-121">**Enrutamiento de troncal M-N**</span><span class="sxs-lookup"><span data-stu-id="8cdc3-121">**M-N Trunk Routing**</span></span>

<span data-ttu-id="8cdc3-122">![Varias asignaciones de tronco.](images/JJ205127.c61cd9a7-d8d9-4e02-83b9-ab62519a48c4(OCS.15).jpg "Varias asignaciones de tronco.")</span><span class="sxs-lookup"><span data-stu-id="8cdc3-122">![Multiple trunk assignments.](images/JJ205127.c61cd9a7-d8d9-4e02-83b9-ab62519a48c4(OCS.15).jpg "Multiple trunk assignments.")</span></span>

<span data-ttu-id="8cdc3-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8cdc3-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

