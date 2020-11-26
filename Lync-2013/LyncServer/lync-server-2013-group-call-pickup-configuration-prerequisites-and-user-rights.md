---
title: Requisitos previos y derechos de usuario para la configuración de la llamada grupal
description: Requisitos previos y derechos de usuario para la configuración de la llamada grupal.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group Call Pickup configuration prerequisites and user rights
ms:assetid: 8757b1d3-751d-49c3-b1b8-b678f663f18e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945641(v=OCS.15)
ms:contentKeyID: 51541495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74d2a758b7199634e14ee387d2554b30bf2ae8d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427876"
---
# <a name="group-call-pickup-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a><span data-ttu-id="4d18c-103">Requisitos previos y derechos de usuario para la configuración de la llamada grupal en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d18c-103">Group Call Pickup configuration prerequisites and user rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d18c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d18c-104">

<span> </span></span></span>

<span data-ttu-id="4d18c-105">_**Última modificación del tema:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="4d18c-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="4d18c-106">La recogida de llamada grupal es una característica de administración de llamadas que se instala de forma predeterminada al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="4d18c-106">Group Call Pickup is a call management feature that is installed by default when you deploy Enterprise Voice.</span></span> <span data-ttu-id="4d18c-107">En este tema se describe lo que debe tener en cuenta antes de poder configurar la recogida de llamadas grupales y los derechos de usuario que necesita para realizar las tareas de configuración.</span><span class="sxs-lookup"><span data-stu-id="4d18c-107">This topic describes what you need to have in place before you can configure Group Call Pickup and the user rights that you need to perform configuration tasks.</span></span>

<span data-ttu-id="4d18c-108">En esta sección se presupone que ha leído la documentación de planificación relacionada con la recogida de llamadas grupales (consulte [planificación de la recogida de llamadas grupales en Lync Server 2013](lync-server-2013-planning-for-group-call-pickup.md)).</span><span class="sxs-lookup"><span data-stu-id="4d18c-108">This section assumes that you have read the planning documentation related to Group Call Pickup (see [Planning for Group Call Pickup in Lync Server 2013](lync-server-2013-planning-for-group-call-pickup.md)).</span></span>

<div>

## <a name="group-call-pickup-configuration-prerequisites"></a><span data-ttu-id="4d18c-109">Requisitos previos de configuración de la llamada grupal</span><span class="sxs-lookup"><span data-stu-id="4d18c-109">Group Call Pickup Configuration Prerequisites</span></span>

<span data-ttu-id="4d18c-110">La recogida de llamadas grupales requiere los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="4d18c-110">Group Call Pickup requires the following components:</span></span>

  - <span data-ttu-id="4d18c-111">Servicio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4d18c-111">Application service</span></span>

  - <span data-ttu-id="4d18c-112">Aplicación de estacionamiento de llamadas</span><span class="sxs-lookup"><span data-stu-id="4d18c-112">Call Park application</span></span>

<span data-ttu-id="4d18c-113">Estos componentes se instalan automáticamente al implementar la telefonía IP empresarial.</span><span class="sxs-lookup"><span data-stu-id="4d18c-113">These components are installed automatically when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="group-call-pickup-configuration-user-rights"></a><span data-ttu-id="4d18c-114">Configuración de la recogida de llamada grupal derechos de usuario</span><span class="sxs-lookup"><span data-stu-id="4d18c-114">Group Call Pickup Configuration User Rights</span></span>

<span data-ttu-id="4d18c-115">Use las siguientes herramientas administrativas para configurar la recogida de llamadas grupales:</span><span class="sxs-lookup"><span data-stu-id="4d18c-115">You use the following administrative tools to configure Group Call Pickup:</span></span>

  - <span data-ttu-id="4d18c-116">Shell de administración de Communications Server</span><span class="sxs-lookup"><span data-stu-id="4d18c-116">Lync Server Management Shell</span></span>

  - <span data-ttu-id="4d18c-117">Herramienta del kit de recursos de SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="4d18c-117">SEFAUtil resource kit tool</span></span>

<span data-ttu-id="4d18c-118">Use el shell de administración de Lync Server para crear y administrar grupos de recogida de llamadas en la tabla de llamadas en órbita de estacionamiento.</span><span class="sxs-lookup"><span data-stu-id="4d18c-118">Use Lync Server Management Shell to create and manage call pickup groups in the Call Park orbit table.</span></span> <span data-ttu-id="4d18c-119">Use la herramienta del kit de recursos de SEFAUtil para asignar un grupo de recogida de llamadas y habilitar la recogida de llamadas grupales para los usuarios o para deshabilitar la recogida de llamadas grupales para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="4d18c-119">Use the SEFAUtil resource kit tool to assign a call pickup group and enable Group Call Pickup for users or to disable Group Call Pickup for users.</span></span>

<span data-ttu-id="4d18c-120">La configuración de la recogida de llamadas de grupo requiere cualquiera de los siguientes roles administrativos, en función de la tarea:</span><span class="sxs-lookup"><span data-stu-id="4d18c-120">Configuring Group Call Pickup requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="4d18c-121">**CsVoiceAdministrator:** Esta función de administrador puede crear, configurar y administrar todas las configuraciones y directivas relacionadas con las voz.</span><span class="sxs-lookup"><span data-stu-id="4d18c-121">**CsVoiceAdministrator:** This administrator role can create, configure, and manage all voice-related settings and policies.</span></span>

  - <span data-ttu-id="4d18c-122">**CsUserAdministrator:** Este rol de administrador puede habilitar la recogida de llamadas grupales para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="4d18c-122">**CsUserAdministrator:** This administrator role can enable Group Call Pickup for users.</span></span> <span data-ttu-id="4d18c-123">Esta función de administrador también tiene acceso de vista de solo lectura a todas las configuraciones de voz.</span><span class="sxs-lookup"><span data-stu-id="4d18c-123">This administrator role also has read-only view access to all voice configurations.</span></span>

  - <span data-ttu-id="4d18c-124">**CsServerAdministrator:** Esta función de administrador puede administrar, supervisar y solucionar problemas de servidores y servicios.</span><span class="sxs-lookup"><span data-stu-id="4d18c-124">**CsServerAdministrator:** This administrator role can manage, monitor, and troubleshoot servers and services.</span></span>

  - <span data-ttu-id="4d18c-125">**CsAdministrator:** Esta función de administrador puede realizar todas las tareas de CsVoiceAdministrator, CsServerAdministrator y CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="4d18c-125">**CsAdministrator:** This administrator role can perform all of the tasks of CsVoiceAdministrator, CsServerAdministrator, and CsUserAdministrator.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="4d18c-126">Para obtener más información sobre los derechos administrativos, consulte <A href="lync-server-2013-planning-for-role-based-access-control.md">planificación de control de acceso basado en roles en Lync Server 2013</A> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="4d18c-126">For details about administrative rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4d18c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d18c-127">See Also</span></span>


[<span data-ttu-id="4d18c-128">Implementación de telefonía IP empresarial en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d18c-128">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="4d18c-129">Planeamiento de las características de administración de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d18c-129">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="4d18c-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d18c-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

