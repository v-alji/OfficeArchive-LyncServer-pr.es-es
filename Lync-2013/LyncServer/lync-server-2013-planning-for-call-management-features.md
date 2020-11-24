---
title: 'Lync Server 2013: planeamiento de características de administración de llamadas'
description: 'Lync Server 2013: planeamiento de características de administración de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for call management features
ms:assetid: 5f557345-5a04-45d6-b274-c02dbfe41b33
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398421(v=OCS.15)
ms:contentKeyID: 48184298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec990aad40baf33365e92e78ee8071216a2add1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397878"
---
# <a name="planning-for-call-management-features-in-lync-server-2013"></a><span data-ttu-id="8e7c5-103">Planeamiento de las características de administración de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e7c5-103">Planning for call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e7c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e7c5-104">

<span> </span></span></span>

<span data-ttu-id="8e7c5-105">_**Última modificación del tema:** 2012-12-17_</span><span class="sxs-lookup"><span data-stu-id="8e7c5-105">_**Topic Last Modified:** 2012-12-17_</span></span>

<span data-ttu-id="8e7c5-106">Las características de administración de llamadas de telefonía de empresa controlan cómo se enrutan y responden las llamadas entrantes.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="8e7c5-107">Lync Server 2013 ofrece las siguientes características de administración de llamadas:</span><span class="sxs-lookup"><span data-stu-id="8e7c5-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="8e7c5-108">**Estacionamiento de llamadas**:   permite a los usuarios de voz estacionar temporalmente una llamada y recuperarla más tarde desde el mismo teléfono o desde otro.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-108">**Call Park**:   Enables voice users to temporarily park a call and then pick it up from the same or another phone.</span></span>

  - <span data-ttu-id="8e7c5-109">**Atención de llamadas grupales**:   permite a los usuarios de voz atender llamadas que suenan para otros usuarios de voz asignados a grupos de atención de llamadas.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-109">**Group Pickup**:   Enables voice users to pick up calls that are ringing for other voice users who are assigned to call pickup groups.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e7c5-110">La recopilación grupal es nueva con las actualizaciones acumulativas para Lync Server 2013: febrero de 2013.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-110">Group Pickup is new with Cumulative Updates for Lync Server 2013: February 2013.</span></span>

    
    </div>

  - <span data-ttu-id="8e7c5-111">**Grupo de respuesta**:   enruta las llamadas entrantes a grupos de agentes mediante preguntas y respuestas de respuesta interactiva de voz (IVR) o grupos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-111">**Response Group**:   Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="8e7c5-112">**Anuncio:**    Reproduce un mensaje para las llamadas realizadas a un número no asignado o enruta la llamada en otro lugar, o ambas.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-112">**Announcement:**    Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="8e7c5-113">Si desea implementar Telefonía IP empresarial, puede optar por implementar cualquiera de estas características de administración de llamadas, implementarlas todas o no implementar ninguna.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-113">If you plan to deploy Enterprise Voice, you can choose to implement any or all of these call management features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8e7c5-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8e7c5-114">In This Section</span></span>

  - [<span data-ttu-id="8e7c5-115">Planear el estacionamiento de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e7c5-115">Planning for Call Park in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-park.md)

  - [<span data-ttu-id="8e7c5-116">Planificación de la recogida de llamadas grupales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e7c5-116">Planning for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-planning-for-group-call-pickup.md)

  - [<span data-ttu-id="8e7c5-117">Planificar para grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e7c5-117">Planning for response groups in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-groups.md)

  - [<span data-ttu-id="8e7c5-118">Planear los anuncios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e7c5-118">Planning for announcements in Lync Server 2013</span></span>](lync-server-2013-planning-for-announcements.md)

<span data-ttu-id="8e7c5-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e7c5-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

