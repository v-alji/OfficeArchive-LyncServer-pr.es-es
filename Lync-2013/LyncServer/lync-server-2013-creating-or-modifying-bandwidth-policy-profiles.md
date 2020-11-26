---
title: 'Lync Server 2013: crear o modificar perfiles de directiva de ancho de banda'
description: 'Lync Server 2013: crear o modificar perfiles de directiva de ancho de banda.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying bandwidth policy profiles
ms:assetid: 08a2e18f-9b0d-4a2f-aa14-13bbf79ec745
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520945(v=OCS.15)
ms:contentKeyID: 48183336
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de8450cf8f4da53bf4a7e096fd7618b7fc6d055b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431452"
---
# <a name="creating-or-modifying-bandwidth-policy-profiles-in-lync-server-2013"></a><span data-ttu-id="085ba-103">Crear o modificar perfiles de directiva de ancho de banda en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="085ba-103">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="085ba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="085ba-104">

<span> </span></span></span>

<span data-ttu-id="085ba-105">_**Última modificación del tema:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="085ba-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="085ba-106">Como parte de control de admisión de llamadas (CAC), se usa una directiva de ancho de banda para definir limitaciones de ancho de banda para determinadas modalidades.</span><span class="sxs-lookup"><span data-stu-id="085ba-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="085ba-107">En Microsoft Lync Server 2013, solo se pueden asignar limitaciones de ancho de banda a las modalidades de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="085ba-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="085ba-108">Puede establecer limitaciones generales de ancho de banda y limitaciones de sesión.</span><span class="sxs-lookup"><span data-stu-id="085ba-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="085ba-109">Puede usar el panel de control de Lync Server para crear, modificar o eliminar un perfil de contenedor para estas directivas.</span><span class="sxs-lookup"><span data-stu-id="085ba-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="085ba-110">Cada perfil de directiva de ancho de banda se puede asociar a uno o varios sitios de red.</span><span class="sxs-lookup"><span data-stu-id="085ba-110">Each bandwidth policy profile can be associated with one or more network sites.</span></span> <span data-ttu-id="085ba-111">Use los procedimientos siguientes para crear o modificar un perfil de directiva de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="085ba-111">Use the following procedures to create or modify a bandwidth policy profile.</span></span> <span data-ttu-id="085ba-112">Para eliminar un perfil de directiva de ancho de banda, consulte [eliminar perfiles de directiva de ancho de banda de red en Lync Server 2013](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="085ba-112">To delete a bandwidth policy profile, see [Deleting network bandwidth policy profiles in Lync Server 2013](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)</span></span>

<div>

## <a name="to-create-a-new-bandwidth-policy-profile"></a><span data-ttu-id="085ba-113">Para crear un nuevo perfil de directiva de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="085ba-113">To create a new bandwidth policy profile</span></span>

1.  <span data-ttu-id="085ba-114">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="085ba-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="085ba-115">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="085ba-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="085ba-116">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="085ba-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="085ba-117">En la barra de navegación izquierda, haga clic en **configuración de red** y, después, en Directiva de **ancho de banda**.</span><span class="sxs-lookup"><span data-stu-id="085ba-117">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="085ba-118">En la página **Directiva de ancho de banda** , haga clic en **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="085ba-118">On the **Bandwidth Policy** page, click **New**.</span></span>

5.  <span data-ttu-id="085ba-119">En **nuevo perfil de directiva de ancho de banda**, escriba un nombre en el campo **nombre** .</span><span class="sxs-lookup"><span data-stu-id="085ba-119">In **New Bandwidth Policy Profile**, type a name in the **Name** field.</span></span> <span data-ttu-id="085ba-120">Este nombre debe ser único entre todos los perfiles de directiva de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="085ba-120">This name must be unique among all bandwidth policy profiles.</span></span>

6.  <span data-ttu-id="085ba-121">En el campo **límite de audio** , escriba un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="085ba-121">In the **Audio limit** field, type a numeric value.</span></span> <span data-ttu-id="085ba-122">Este valor es la cantidad máxima de ancho de banda que se asignará a todas las conexiones de audio, expresadas en kbps.</span><span class="sxs-lookup"><span data-stu-id="085ba-122">This value is the maximum amount of bandwidth to allocate for all audio connections, expressed in kbps.</span></span>

7.  <span data-ttu-id="085ba-123">Escriba un valor numérico en el campo límite de la **sesión de audio** .</span><span class="sxs-lookup"><span data-stu-id="085ba-123">Enter a numeric value in the **Audio session limit** field.</span></span> <span data-ttu-id="085ba-124">Este valor es la cantidad máxima de ancho de banda que se asignará a una conexión de audio individual, expresada en kbps.</span><span class="sxs-lookup"><span data-stu-id="085ba-124">This value is the maximum amount of bandwidth to allocate for an individual audio connection, expressed in kbps.</span></span> <span data-ttu-id="085ba-125">Este valor debe ser 40 o superior.</span><span class="sxs-lookup"><span data-stu-id="085ba-125">This value must be 40 or higher.</span></span>

8.  <span data-ttu-id="085ba-126">Escriba un valor numérico en el campo **límite de video** .</span><span class="sxs-lookup"><span data-stu-id="085ba-126">Enter a numeric value in the **Video limit** field.</span></span> <span data-ttu-id="085ba-127">Este valor es la cantidad máxima de ancho de banda que se asignará a todas las conexiones de vídeo, expresadas en kbps.</span><span class="sxs-lookup"><span data-stu-id="085ba-127">This value is the maximum amount of bandwidth to allocate for all video connections, expressed in kbps.</span></span>

9.  <span data-ttu-id="085ba-128">Escriba un valor numérico en el campo límite de la **sesión de vídeo** .</span><span class="sxs-lookup"><span data-stu-id="085ba-128">Enter a numeric value in the **Video session limit** field.</span></span> <span data-ttu-id="085ba-129">Este valor es la cantidad máxima de ancho de banda que se asignará a una conexión de video individual, expresada en kbps.</span><span class="sxs-lookup"><span data-stu-id="085ba-129">This value is the maximum amount of bandwidth to allocate for an individual video connection, expressed in kbps.</span></span> <span data-ttu-id="085ba-130">Este valor debe ser 100 o superior.</span><span class="sxs-lookup"><span data-stu-id="085ba-130">This value must be 100 or higher.</span></span>

10. <span data-ttu-id="085ba-131">Faculta Escriba un valor en el campo **Descripción** para proporcionar más información sobre este perfil de directiva de ancho de banda que no se puede expresar solo con el nombre.</span><span class="sxs-lookup"><span data-stu-id="085ba-131">(Optional) Type a value in the **Description** field to provide more information about this bandwidth policy profile that cannot be expressed by the name alone.</span></span>

11. <span data-ttu-id="085ba-132">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="085ba-132">Click **Commit**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="085ba-133">La creación de un nuevo perfil de directiva de ancho de banda no aplica automáticamente restricciones de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="085ba-133">Creating a new bandwidth policy profile does not automatically enforce bandwidth restrictions.</span></span> <span data-ttu-id="085ba-134">Primero debe asociar el perfil de directiva con un sitio.</span><span class="sxs-lookup"><span data-stu-id="085ba-134">You must first associate the policy profile with a site.</span></span> <span data-ttu-id="085ba-135">Para obtener más información sobre cómo asociar un perfil de directiva con un sitio, vea <A href="lync-server-2013-creating-or-modifying-network-sites.md">crear o modificar sitios de red en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="085ba-135">For details about how to associate a policy profile with a site, see <A href="lync-server-2013-creating-or-modifying-network-sites.md">Creating or modifying network sites in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-a-bandwidth-policy-profile"></a><span data-ttu-id="085ba-136">Para modificar un perfil de directiva de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="085ba-136">To modify a bandwidth policy profile</span></span>

1.  <span data-ttu-id="085ba-137">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="085ba-137">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="085ba-138">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="085ba-138">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="085ba-139">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="085ba-139">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="085ba-140">En la barra de navegación izquierda, haga clic en **configuración de red** y, después, en Directiva de **ancho de banda**.</span><span class="sxs-lookup"><span data-stu-id="085ba-140">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="085ba-141">En la página **Directiva de ancho de banda** , haga clic en el perfil de directiva de ancho de banda que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="085ba-141">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to modify.</span></span>

5.  <span data-ttu-id="085ba-142">En el menú **Editar**, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="085ba-142">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="085ba-143">En la página **Editar perfil de directiva de ancho de banda** , modifique los campos según sea necesario (para obtener información detallada, consulte la sección "para crear un perfil de directiva de ancho de banda" anteriormente en este tema).</span><span class="sxs-lookup"><span data-stu-id="085ba-143">On the **Edit Bandwidth Policy Profile** page, modify the fields as necessary (for details, see the "To create a bandwidth policy profile" section earlier in this topic).</span></span>

7.  <span data-ttu-id="085ba-144">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="085ba-144">Click **Commit**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="085ba-145">Al modificar el perfil de directiva de ancho de banda, se actualizarán inmediatamente las limitaciones de ancho de banda de todos los sitios de red asociados a este perfil de directiva de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="085ba-145">When you modify the bandwidth policy profile, it will immediately update the bandwidth limitations of all network sites associated with this bandwidth policy profile.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="085ba-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="085ba-146">See Also</span></span>


[<span data-ttu-id="085ba-147">Eliminar perfiles de directiva de ancho de banda de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="085ba-147">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)  


[<span data-ttu-id="085ba-148">Configurar el control de admisión de llamadas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="085ba-148">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="085ba-149">New-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="085ba-149">New-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkBandwidthPolicyProfile)  
[<span data-ttu-id="085ba-150">Set-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="085ba-150">Set-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkBandwidthPolicyProfile)  
[<span data-ttu-id="085ba-151">Get-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="085ba-151">Get-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile)  
  

<span data-ttu-id="085ba-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="085ba-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

