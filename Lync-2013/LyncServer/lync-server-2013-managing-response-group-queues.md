---
title: 'Lync Server 2013: administración de colas de grupos de respuesta'
description: 'Lync Server 2013: administración de colas de grupos de respuesta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Response Group queues
ms:assetid: 1e91720c-ab67-4dfb-b30c-0ef2a8012310
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520960(v=OCS.15)
ms:contentKeyID: 48183576
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a46359df874ee375b8b0b8fdd6ee7ed4f879b31e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437262"
---
# <a name="managing-response-group-queues-in-lync-server-2013"></a><span data-ttu-id="b0617-103">Administrar colas de grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0617-103">Managing Response Group queues in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0617-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0617-104">

<span> </span></span></span>

<span data-ttu-id="b0617-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="b0617-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="b0617-106">Las colas contienen llamadas a un grupo de respuesta hasta que un agente responde a la llamada.</span><span class="sxs-lookup"><span data-stu-id="b0617-106">Queues hold calls to a response group until an agent answers the call.</span></span> <span data-ttu-id="b0617-107">Cuando administra una cola, asigna uno o varios grupos de agentes a la cola y especifica la configuración de la cola, como el número de llamadas que la cola puede mantener antes de realizar una acción de desbordamiento y el período de tiempo durante el que una llamada espera un agente antes de realizar una acción de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b0617-107">When you manage a queue, you assign one or more agent groups to the queue and specify queue settings, such as the number of calls that the queue can hold before performing an overflow action and the length of time that a call waits for an agent before performing a time-out action.</span></span> <span data-ttu-id="b0617-108">Cuando la aplicación de grupo de respuesta busca un agente disponible, busca en los grupos de agentes en el orden en que se enumeren.</span><span class="sxs-lookup"><span data-stu-id="b0617-108">When the Response Group application searches for an available agent, it searches agent groups in the order that you list them.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b0617-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b0617-109">In This Section</span></span>

  - [<span data-ttu-id="b0617-110">Crear o modificar una cola en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0617-110">Create or modify a queue in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-queue.md)

  - [<span data-ttu-id="b0617-111">Eliminar una cola de grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0617-111">Delete a Response Group queue in Lync Server 2013</span></span>](lync-server-2013-delete-a-response-group-queue.md)

<span data-ttu-id="b0617-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0617-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

