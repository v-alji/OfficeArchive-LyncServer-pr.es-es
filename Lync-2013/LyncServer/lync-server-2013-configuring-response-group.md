---
title: 'Lync Server 2013: Configurar grupos de respuesta'
description: 'Lync Server 2013: configuración del grupo de respuesta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Response Group
ms:assetid: c56db929-cb21-4af0-be3f-c8f807b78a5a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205249(v=OCS.15)
ms:contentKeyID: 48185359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92674bb971ec5216051d75d788dc58b9c7ca641c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432691"
---
# <a name="configuring-response-group-in-lync-server-2013"></a><span data-ttu-id="b7e39-103">Configurar grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-103">Configuring Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7e39-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7e39-104">

<span> </span></span></span>

<span data-ttu-id="b7e39-105">_**Última modificación del tema:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="b7e39-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="b7e39-106">El grupo de respuesta es una característica de voz de empresa que enruta y pone en cola las llamadas entrantes a grupos de personas, denominados *agentes*, como un servicio de asistencia o un servicio de asistencia al cliente.</span><span class="sxs-lookup"><span data-stu-id="b7e39-106">Response Group is an Enterprise Voice feature that routes and queues incoming calls to groups of people, called *agents*, such as a help desk or a customer service desk.</span></span>

<span data-ttu-id="b7e39-107">Los componentes que requiere el grupo de respuesta se instalan y se habilitan automáticamente en el servidor front-end o el servidor Standard Edition al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="b7e39-107">The components that Response Group requires are installed and enabled automatically on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="b7e39-108">Para que los usuarios puedan disponer de un grupo de respuesta, debe configurar grupos de agentes, después colas y, por último, flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b7e39-108">To make Response Group available to users, you must configure agent groups, then queues, and then workflows.</span></span> <span data-ttu-id="b7e39-109">Además, un administrador de grupo de respuesta puede delegar la configuración de un flujo de trabajo existente a un administrador de grupo de respuesta, que podrá modificar y volver a configurar el flujo de trabajo y sus grupos de agentes y colas relacionados.</span><span class="sxs-lookup"><span data-stu-id="b7e39-109">Additionally, a Response Group Administrator can delegate configuration of an existing workflow to a Response Group Manager, who can then modify and reconfigure the workflow and its associated agent groups and queues.</span></span>

<span data-ttu-id="b7e39-110">Esta sección le guiará a través de la configuración del grupo de respuesta 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b7e39-110">This section guides you through the configuration of Lync Server 2013 Response Group.</span></span> <span data-ttu-id="b7e39-111">Se supone que ya ha leído las secciones de planificación relacionadas con el grupo de respuesta y ha implementado un servidor Enterprise Edition o un servidor Standard Edition con telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="b7e39-111">It assumes that you have already read the planning sections related to Response Group and have deployed an Enterprise Edition server or a Standard Edition server with Enterprise Voice.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="b7e39-112">Para obtener detalles acerca de la creación de un grupo de respuesta mediante el shell de administración de Lync Server, incluido un script de ejemplo, consulte "crear su primer grupo de respuesta con el shell de administración de Lync Server" en <A href="https://go.microsoft.com/fwlink/p/?linkid=204108">https://go.microsoft.com/fwlink/p/?linkId=204108</A> .</span><span class="sxs-lookup"><span data-stu-id="b7e39-112">For details about creating a Response Group by using Lync Server Management Shell, including a sample script, see "Creating Your First Response Group Using Lync Server Management Shell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=204108">https://go.microsoft.com/fwlink/p/?linkId=204108</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b7e39-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b7e39-113">In This Section</span></span>

  - [<span data-ttu-id="b7e39-114">Permisos y requisitos previos de configuración de grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-114">Response Group configuration permissions and prerequisites in Lync Server 2013</span></span>](lync-server-2013-response-group-configuration-permissions-and-prerequisites.md)

  - [<span data-ttu-id="b7e39-115">Proceso de implementación para un grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-115">Deployment process for Response Group in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-response-group.md)

  - [<span data-ttu-id="b7e39-116">Resumen de escenarios de creación de flujo de trabajo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-116">Overview of workflow creation scenarios in Lync Server 2013</span></span>](lync-server-2013-overview-of-workflow-creation-scenarios.md)

  - [<span data-ttu-id="b7e39-117">Crear grupos de agentes de grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-117">Create Response Group agent groups Lync Server 2013</span></span>](lync-server-2013-create-response-group-agent-groups.md)

  - [<span data-ttu-id="b7e39-118">Crear colas de grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-118">Create Response Group queues in Lync Server 2013</span></span>](lync-server-2013-create-response-group-queues.md)

  - [<span data-ttu-id="b7e39-119">Faculta Definir las horas de trabajo del grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-119">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)

  - [<span data-ttu-id="b7e39-120">Faculta Definir conjuntos de días festivos de grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-120">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)

  - [<span data-ttu-id="b7e39-121">Crear flujos de trabajo de grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-121">Create Response Group workflows in Lync Server 2013</span></span>](lync-server-2013-create-response-group-workflows.md)

  - [<span data-ttu-id="b7e39-122">Faculta Comprobar la implementación de grupos de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-122">(Optional) Verify Response Group deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-response-group-deployment.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b7e39-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7e39-123">See Also</span></span>


[<span data-ttu-id="b7e39-124">Planeamiento de las características de administración de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7e39-124">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="b7e39-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7e39-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

