---
title: 'Lync Server 2013: eliminar una directiva de ubicación'
description: 'Lync Server 2013: eliminar una directiva de ubicación.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting a location policy
ms:assetid: 8ca9ba10-f45f-435a-b39c-519d251e9085
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688125(v=OCS.15)
ms:contentKeyID: 49733724
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88935c00a60de377c9812a4d119708fd610338ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430423"
---
# <a name="deleting-a-location-policy-in-lync-server-2013"></a><span data-ttu-id="4397b-103">Eliminar una directiva de ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4397b-103">Deleting a location policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4397b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4397b-104">

<span> </span></span></span>

<span data-ttu-id="4397b-105">_**Última modificación del tema:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="4397b-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="4397b-106">En Lync Server 2013, puede usar la Directiva de ubicación para aplicar la configuración relacionada con la funcionalidad mejorada de 9-1-1 (E9-1-1) y la configuración de ubicación de los usuarios o los contactos.</span><span class="sxs-lookup"><span data-stu-id="4397b-106">In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts.</span></span> <span data-ttu-id="4397b-107">La Directiva de ubicación determina si un usuario está habilitado para E9-1-1 y, si es así, cuál es el comportamiento de una llamada de emergencia.</span><span class="sxs-lookup"><span data-stu-id="4397b-107">The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call.</span></span> <span data-ttu-id="4397b-108">Por ejemplo, puede usar la política de ubicación para definir qué número constituye una llamada de emergencia (por ejemplo, 911 en los Estados Unidos), si se debe notificar automáticamente la seguridad corporativa y cómo debe dirigirse la llamada.</span><span class="sxs-lookup"><span data-stu-id="4397b-108">For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="4397b-109">Puede configurar directivas de ubicación desde el grupo **configuración de red** en el panel de control de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4397b-109">You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="4397b-110">En el panel de control de Lync Server puede ver, crear, modificar o eliminar directivas de ubicación.</span><span class="sxs-lookup"><span data-stu-id="4397b-110">From Lync Server Control Panel you can view, create, modify, or delete location policies.</span></span> <span data-ttu-id="4397b-111">Use los siguientes procedimientos para eliminar una política de ubicación.</span><span class="sxs-lookup"><span data-stu-id="4397b-111">Use the following procedures delete a location policy.</span></span> <span data-ttu-id="4397b-112">Para obtener más información sobre cómo crear o modificar directivas de ubicación, vea [crear o modificar una directiva de ubicación en Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="4397b-112">For details on creating or modifying location policies, see [Creating or modifying a location policy in Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span></span>

<div>

## <a name="to-delete-a-location-policy"></a><span data-ttu-id="4397b-113">Para eliminar una directiva de ubicación</span><span class="sxs-lookup"><span data-stu-id="4397b-113">To delete a location policy</span></span>

1.  <span data-ttu-id="4397b-114">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="4397b-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4397b-115">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4397b-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4397b-116">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4397b-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4397b-117">En la barra de navegación izquierda, haga clic en **configuración de red** y luego en **Directiva de ubicación**.</span><span class="sxs-lookup"><span data-stu-id="4397b-117">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="4397b-118">En la página **Directiva de ubicación** , seleccione la Directiva de ubicación que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="4397b-118">On the **Location Policy** page, select the location policy that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4397b-119">Puede eliminar más de una política de ubicación a la vez.</span><span class="sxs-lookup"><span data-stu-id="4397b-119">You can delete more than one location policy at a time.</span></span> <span data-ttu-id="4397b-120">Para ello, presione CTRL y seleccione varias directivas mientras mantiene presionada la tecla CTRL.</span><span class="sxs-lookup"><span data-stu-id="4397b-120">To do this, press CTRL and select multiple policies while holding down the CTRL key.</span></span> <span data-ttu-id="4397b-121">O bien, para seleccionar todas las directivas, haga clic en <STRONG>seleccionar todo</STRONG> en el menú <STRONG>edición</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="4397b-121">Or, to select all policies, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="4397b-122">En el menú **Editar** , haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="4397b-122">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="4397b-123">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="4397b-123">Click **OK**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="4397b-124">No se puede eliminar la Directiva de ubicación global.</span><span class="sxs-lookup"><span data-stu-id="4397b-124">You cannot delete the Global location policy.</span></span> <span data-ttu-id="4397b-125">Si intenta eliminar la directiva global, recibirá un mensaje de advertencia y esa Directiva se restablecerá a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="4397b-125">If you attempt to delete the Global policy you will receive a warning message and that policy will be reset to its default values.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4397b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4397b-126">See Also</span></span>


[<span data-ttu-id="4397b-127">Crear o modificar una directiva de ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4397b-127">Creating or modifying a location policy in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-a-location-policy.md)  
[<span data-ttu-id="4397b-128">Ver información de la Directiva de ubicación en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4397b-128">Viewing location policy information in Lync Server 2013</span></span>](lync-server-2013-viewing-location-policy-information.md)  
  

<span data-ttu-id="4397b-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4397b-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

