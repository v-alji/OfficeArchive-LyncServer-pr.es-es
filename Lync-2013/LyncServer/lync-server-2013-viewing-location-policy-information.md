---
title: 'Lync Server 2013: visualización de la información de directiva de ubicación'
description: 'Lync Server 2013: visualización de la información de directiva de ubicación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing location policy information
ms:assetid: 14e41bcb-ea0a-49c2-99b3-1f61fc34416d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520954(v=OCS.15)
ms:contentKeyID: 48183489
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fecc5de5fb71014a1641038e9e09afba0e90cdb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443961"
---
# <a name="viewing-location-policy-information-in-lync-server-2013"></a><span data-ttu-id="831c5-103">Ver información de la Directiva de ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="831c5-103">Viewing location policy information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="831c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="831c5-104">

<span> </span></span></span>

<span data-ttu-id="831c5-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="831c5-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="831c5-106">En Lync Server 2013, puede usar la Directiva de ubicación para aplicar la configuración relacionada con la funcionalidad mejorada de 9-1-1 (E9-1-1) y la configuración de ubicación de los usuarios o los contactos.</span><span class="sxs-lookup"><span data-stu-id="831c5-106">In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts.</span></span> <span data-ttu-id="831c5-107">La Directiva de ubicación determina si un usuario está habilitado para E9-1-1 y, si es así, cuál es el comportamiento de una llamada de emergencia.</span><span class="sxs-lookup"><span data-stu-id="831c5-107">The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call.</span></span> <span data-ttu-id="831c5-108">Por ejemplo, puede usar la política de ubicación para definir qué número constituye una llamada de emergencia (por ejemplo, 911 en los Estados Unidos), si se debe notificar automáticamente la seguridad corporativa y cómo debe dirigirse la llamada.</span><span class="sxs-lookup"><span data-stu-id="831c5-108">For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="831c5-109">Puede configurar directivas de ubicación desde el grupo **configuración de red** en el panel de control de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="831c5-109">You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="831c5-110">En el panel de control de Lync Server puede ver, crear, modificar o eliminar directivas de ubicación.</span><span class="sxs-lookup"><span data-stu-id="831c5-110">From Lync Server Control Panel you can view, create, modify, or delete location policies.</span></span> <span data-ttu-id="831c5-111">Use el procedimiento siguiente para ver información sobre las directivas de ubicación.</span><span class="sxs-lookup"><span data-stu-id="831c5-111">Use the following procedure to view information about location policies.</span></span> <span data-ttu-id="831c5-112">Para obtener más información sobre cómo crear o modificar directivas de ubicación, vea [crear o modificar una directiva de ubicación en Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="831c5-112">For details on creating or modifying location policies, see [Creating or modifying a location policy in Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span></span>

<div>

## <a name="to-view-information-about-a-location-policy"></a><span data-ttu-id="831c5-113">Para ver información sobre una directiva de ubicación</span><span class="sxs-lookup"><span data-stu-id="831c5-113">To view information about a location policy</span></span>

1.  <span data-ttu-id="831c5-114">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="831c5-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="831c5-115">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="831c5-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="831c5-116">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="831c5-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="831c5-117">En la barra de navegación izquierda, haga clic en **configuración de red** y luego en **Directiva de ubicación**.</span><span class="sxs-lookup"><span data-stu-id="831c5-117">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="831c5-118">En la página **Directiva de ubicación** , seleccione la Directiva de ubicación que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="831c5-118">On the **Location Policy** page, select the location policy that you want to modify.</span></span>

5.  <span data-ttu-id="831c5-119">En el menú **Editar**, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="831c5-119">On the **Edit** menu, click **Show details**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="831c5-120">Solo puede ver información sobre una política de ubicación a la vez.</span><span class="sxs-lookup"><span data-stu-id="831c5-120">You can only view information about one location policy at a time.</span></span>

    
    </div>

<span data-ttu-id="831c5-121">De forma predeterminada, existe una única directiva, denominada global, que no se puede eliminar ni cambiar de nombre.</span><span class="sxs-lookup"><span data-stu-id="831c5-121">A single policy, called Global, exists by default and cannot be deleted or renamed.</span></span> <span data-ttu-id="831c5-122">Sin embargo, puede modificar la directiva global.</span><span class="sxs-lookup"><span data-stu-id="831c5-122">However, you can modify the Global policy.</span></span> <span data-ttu-id="831c5-123">Esta Directiva se aplicará a todos los usuarios y contactos, a menos que cree directivas de sitio o directivas por usuario.</span><span class="sxs-lookup"><span data-stu-id="831c5-123">This policy will apply to all users and contacts, unless you create site policies or per-user policies.</span></span> <span data-ttu-id="831c5-124">Las directivas por usuario deben aplicarse a usuarios específicos.</span><span class="sxs-lookup"><span data-stu-id="831c5-124">Per-user policies must be applied to specific users.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="831c5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="831c5-125">See Also</span></span>


[<span data-ttu-id="831c5-126">Crear o modificar una directiva de ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="831c5-126">Creating or modifying a location policy in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-a-location-policy.md)  
[<span data-ttu-id="831c5-127">Crear directivas de ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="831c5-127">Create location policies in Lync Server 2013</span></span>](lync-server-2013-create-location-policies.md)  
[<span data-ttu-id="831c5-128">Crear o modificar un sitio de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="831c5-128">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)  


[<span data-ttu-id="831c5-129">Nuevo: CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="831c5-129">New-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy)  
[<span data-ttu-id="831c5-130">Set-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="831c5-130">Set-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy)  
[<span data-ttu-id="831c5-131">Remove-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="831c5-131">Remove-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsLocationPolicy)  
[<span data-ttu-id="831c5-132">Get-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="831c5-132">Get-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsLocationPolicy)  
  

<span data-ttu-id="831c5-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="831c5-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

