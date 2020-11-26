---
title: 'Lync Server 2013: configuración de la recogida de llamadas grupales'
description: 'Lync Server 2013: configuración de la recogida de llamadas grupales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Group Call Pickup
ms:assetid: b4b0a9a0-91c6-43a5-9e2b-a086caeb3f94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945645(v=OCS.15)
ms:contentKeyID: 51541505
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff6be1ea20a98cfaf2addf32c7767940b420c5c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433034"
---
# <a name="configuring-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="da3b6-103">Configuración de la recogida de llamadas grupales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da3b6-103">Configuring Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da3b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da3b6-104">

<span> </span></span></span>

<span data-ttu-id="da3b6-105">_**Última modificación del tema:** 2013-02-01_</span><span class="sxs-lookup"><span data-stu-id="da3b6-105">_**Topic Last Modified:** 2013-02-01_</span></span>

<span data-ttu-id="da3b6-106">Actualización acumulativa para Lync Server 2013: febrero de 2013 presenta la recogida de llamadas grupales como una nueva característica de voz empresarial.</span><span class="sxs-lookup"><span data-stu-id="da3b6-106">Cumulative update for Lync Server 2013: February 2013 introduces Group Call Pickup as a new Enterprise Voice feature.</span></span> <span data-ttu-id="da3b6-107">La recopilación de la llamada grupal permite que los usuarios recojan llamadas que están sonando por otro usuario marcando un número de grupo de recogida de llamadas.</span><span class="sxs-lookup"><span data-stu-id="da3b6-107">Group Call Pickup lets users pick up calls that are ringing for another user by dialing a call pickup group number.</span></span>

<span data-ttu-id="da3b6-108">Los componentes que usa la recogida de llamadas grupales se instalan y se habilitan automáticamente en el servidor front-end o el servidor Standard Edition al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="da3b6-108">The components that Group Call Pickup uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="da3b6-109">Sin embargo, debe configurar la recogida de llamadas de grupo antes de que esté disponible para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="da3b6-109">However, you must configure Group Call Pickup before it is available to users.</span></span>

<span data-ttu-id="da3b6-110">Esta sección le guiará a través de la configuración de la recogida de llamadas grupales.</span><span class="sxs-lookup"><span data-stu-id="da3b6-110">This section guides you through the configuration of Group Call Pickup.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="da3b6-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="da3b6-111">In This Section</span></span>

[<span data-ttu-id="da3b6-112">Requisitos previos y derechos de usuario para la configuración de la llamada grupal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da3b6-112">Group Call Pickup configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-group-call-pickup-configuration-prerequisites-and-user-rights.md)

[<span data-ttu-id="da3b6-113">Proceso de implementación para la recogida de llamadas grupales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da3b6-113">Deployment process for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-group-call-pickup.md)

[<span data-ttu-id="da3b6-114">Deploy the SEFAUtil tool in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da3b6-114">Deploy the SEFAUtil tool in Lync Server 2013</span></span>](lync-server-2013-deploy-the-sefautil-tool.md)

[<span data-ttu-id="da3b6-115">Configurar números de grupo de recogida de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da3b6-115">Configure call pickup group numbers in Lync Server 2013</span></span>](lync-server-2013-configure-call-pickup-group-numbers.md)

[<span data-ttu-id="da3b6-116">Habilitar la recogida de llamadas grupales para los usuarios en Lync Server 2013 y asignar un número de grupo</span><span class="sxs-lookup"><span data-stu-id="da3b6-116">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</span></span>](lync-server-2013-enable-group-call-pickup-for-users-and-assign-a-group-number.md)

[<span data-ttu-id="da3b6-117">Comunicar las tareas de recogida de llamadas grupales a los usuarios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da3b6-117">Communicate Group Call Pickup assignments to users in Lync Server 2013</span></span>](lync-server-2013-communicate-group-call-pickup-assignment-to-users.md)

[<span data-ttu-id="da3b6-118">Faculta Comprobar la implementación de la llamada grupal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da3b6-118">(Optional) Verify the Group Call Pickup deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-the-group-call-pickup-deployment.md)

<span data-ttu-id="da3b6-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da3b6-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

