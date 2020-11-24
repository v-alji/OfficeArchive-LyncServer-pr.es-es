---
title: 'Lync Server 2013: configurar los números del grupo de recogida de llamadas'
description: 'Lync Server 2013: configurar los números del grupo de recogida de llamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure call pickup group numbers
ms:assetid: 5cc67f0b-d70d-446a-8db1-befda8671121
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945631(v=OCS.15)
ms:contentKeyID: 51541479
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ddffae2e385ce6c3fd7a700a9b94a89b1b6679f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397961"
---
# <a name="configure-call-pickup-group-numbers-in-lync-server-2013"></a><span data-ttu-id="6e72d-103">Configurar números de grupo de recogida de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e72d-103">Configure call pickup group numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e72d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e72d-104">

<span> </span></span></span>

<span data-ttu-id="6e72d-105">_**Última modificación del tema:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="6e72d-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="6e72d-106">La recogida de llamadas grupales se basa en la aplicación de estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="6e72d-106">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="6e72d-107">Al implementar la recogida de llamadas grupales, debe configurar la tabla de llamadas en órbita con los rangos de números de teléfono que se designan como números de grupo de recogida de llamadas.</span><span class="sxs-lookup"><span data-stu-id="6e72d-107">When you deploy Group Call Pickup, you configure the call park orbit table with ranges of phone numbers that are designated as call pickup group numbers.</span></span> <span data-ttu-id="6e72d-108">Estos números de grupo son los números que los usuarios marcan para atender las llamadas que están sonando para otro usuario.</span><span class="sxs-lookup"><span data-stu-id="6e72d-108">These group numbers are the numbers that users dial to pick up calls that are ringing for another user.</span></span>

<span data-ttu-id="6e72d-109">Al igual que sucede con los números de órbita de estacionamiento de llamadas, los números de grupo de atención a llamadas deben ser extensiones virtuales que no tengan asignado ningún usuario o teléfono.</span><span class="sxs-lookup"><span data-stu-id="6e72d-109">Like call park orbit numbers, call pickup group numbers need to be virtual extensions that have no user or phone assigned to them.</span></span> <span data-ttu-id="6e72d-110">Cada grupo de servidores front-end en el que se implementa la recogida de llamadas grupales puede tener uno o más intervalos de números de grupo de recogida de llamadas.</span><span class="sxs-lookup"><span data-stu-id="6e72d-110">Each Front End pool where you deploy Group Call Pickup can have one or more ranges of call pickup group numbers.</span></span> <span data-ttu-id="6e72d-111">Los intervalos de números de grupo deben ser únicos globalmente en la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6e72d-111">The group number ranges must be globally unique across the Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6e72d-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6e72d-112">In This Section</span></span>

[<span data-ttu-id="6e72d-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e72d-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-group-call-pickup-number-range.md)

<span data-ttu-id="6e72d-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e72d-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

