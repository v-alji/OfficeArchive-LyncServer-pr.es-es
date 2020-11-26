---
title: 'Lync Server 2013: implementar características de administración de llamadas'
description: 'Lync Server 2013: implementar características de administración de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying call management features
ms:assetid: 1667cfe4-76fa-4e10-91bb-b3efbedbf759
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204706(v=OCS.15)
ms:contentKeyID: 48183504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa89b75dbcae9de1069daf99986076b66e0411cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430073"
---
# <a name="deploying-call-management-features-in-lync-server-2013"></a><span data-ttu-id="9fb2f-103">Implementar características de administración de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fb2f-103">Deploying call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9fb2f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9fb2f-104">

<span> </span></span></span>

<span data-ttu-id="9fb2f-105">_**Última modificación del tema:** 2012-12-18_</span><span class="sxs-lookup"><span data-stu-id="9fb2f-105">_**Topic Last Modified:** 2012-12-18_</span></span>

<span data-ttu-id="9fb2f-106">Las características de administración de llamadas de telefonía de empresa controlan cómo se enrutan y responden las llamadas entrantes.</span><span class="sxs-lookup"><span data-stu-id="9fb2f-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="9fb2f-107">Lync Server 2013 ofrece las siguientes características de administración de llamadas:</span><span class="sxs-lookup"><span data-stu-id="9fb2f-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="9fb2f-108">**Parque de llamadas:** Permite a los usuarios de voz detener temporalmente una llamada y, a continuación, recogerla desde el mismo teléfono u otro teléfono.</span><span class="sxs-lookup"><span data-stu-id="9fb2f-108">**Call Park:** Enables voice users to temporarily park a call and then pick it up from the same phone or another phone.</span></span>

  - <span data-ttu-id="9fb2f-109">**Recogida de grupos:** Permite a los usuarios contestar las llamadas hechas a otro usuario que se asigna a un grupo de recogida marcando el número de grupo de recogida de llamadas.</span><span class="sxs-lookup"><span data-stu-id="9fb2f-109">**Group Pickup:** Enables users to answer calls made to another user who is assigned to a pickup group by dialing the call pickup group number.</span></span>

  - <span data-ttu-id="9fb2f-110">**Grupo de respuesta:** Enruta las llamadas entrantes a grupos de agentes mediante el uso de grupos de extensiones o preguntas y respuestas interactivas de respuesta de voz (IVR).</span><span class="sxs-lookup"><span data-stu-id="9fb2f-110">**Response Group:** Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="9fb2f-111">**Anuncio:** Reproduce un mensaje para las llamadas realizadas a un número no asignado o enruta la llamada en otro lugar, o ambas.</span><span class="sxs-lookup"><span data-stu-id="9fb2f-111">**Announcement:** Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="9fb2f-112">En esta sección se describe cómo configurar estas características de administración de llamadas durante una implementación de telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="9fb2f-112">This section describes how to configure these call management features during an Enterprise Voice deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9fb2f-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9fb2f-113">In This Section</span></span>

  - [<span data-ttu-id="9fb2f-114">Configurar el estacionamiento de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fb2f-114">Configuring Call Park in Lync Server 2013</span></span>](lync-server-2013-configuring-call-park.md)

  - [<span data-ttu-id="9fb2f-115">Configuración de la recogida de llamadas grupales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fb2f-115">Configuring Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-configuring-group-call-pickup.md)

  - [<span data-ttu-id="9fb2f-116">Configurar grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fb2f-116">Configuring Response Group in Lync Server 2013</span></span>](lync-server-2013-configuring-response-group.md)

  - [<span data-ttu-id="9fb2f-117">Configuración de anuncios para números sin asignar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fb2f-117">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>](lync-server-2013-configuring-announcements-for-unassigned-numbers.md)

<span data-ttu-id="9fb2f-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9fb2f-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

