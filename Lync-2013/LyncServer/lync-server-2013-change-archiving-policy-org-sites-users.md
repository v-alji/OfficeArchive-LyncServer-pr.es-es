---
title: 'Lync Server 2013: cambio de una directiva de archivado para habilitar o deshabilitar el archivado de comunicaciones internas o externas para la organización, los sitios o los usuarios'
description: 'Lync Server 2013: cambiar una directiva de archivado para habilitar o deshabilitar el archivado de las comunicaciones internas o externas para la organización, los sitios o los usuarios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing an Archiving policy to enable or disable Archiving of internal or external communications for your organization, sites, or users
ms:assetid: b85dc3fb-8ebd-4e3c-ac90-fc79270ac867
ms:mtpsurl: https://technet.microsoft.com/library/Gg182576(v=OCS.15)
ms:contentKeyID: 48185234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee24f3d72e447a778d434994dff1795baa04d420
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435183"
---
# <a name="changing-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-your-organization-sites-or-users"></a><span data-ttu-id="6f094-103">Cambiar una directiva de archivado en Lync Server 2013 para habilitar o deshabilitar el archivado de comunicaciones internas o externas para la organización, los sitios o los usuarios</span><span class="sxs-lookup"><span data-stu-id="6f094-103">Changing an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for your organization, sites, or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f094-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f094-104">

<span> </span></span></span>

<span data-ttu-id="6f094-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="6f094-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="6f094-106">En Lync Server 2013, se usan directivas para habilitar y deshabilitar el archivado de comunicaciones internas y comunicaciones externas para usuarios alojados en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6f094-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="6f094-107">Esto incluye las siguientes directivas de archivado:</span><span class="sxs-lookup"><span data-stu-id="6f094-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="6f094-108">Una directiva global que se crea de forma predeterminada al implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6f094-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="6f094-109">Directivas opcionales a nivel de sitio y de usuario que puede crear y usar para especificar cómo se implementa el archivado para usuarios o sitios específicos.</span><span class="sxs-lookup"><span data-stu-id="6f094-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="6f094-110">Inicialmente, debe configurar las directivas de archivado al implementar el archivado, pero puede cambiar, agregar y eliminar directivas después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="6f094-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="6f094-111">En el panel de control de Lync Server 2013, puede usar la página **Directiva de archivado** del grupo **archivado y supervisión** para administrar directivas a nivel global, nivel de sitio y nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="6f094-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="6f094-112">Si integra el almacenamiento de Lync Server con el almacenamiento de Exchange 2013, las directivas de usuario de Exchange tienen prioridad sobre las directivas de archivado de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6f094-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="6f094-113">Para obtener más información sobre cómo se implementan las directivas, incluida la jerarquía de directivas, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="6f094-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6f094-114">Si habilitó la integración de Microsoft Exchange para su implementación, las directivas de Exchange controlan si el archivado está habilitado para los usuarios que están alojados en Exchange 2013 y si sus buzones se ponen en espera In-Place.</span><span class="sxs-lookup"><span data-stu-id="6f094-114">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="6f094-115">Para obtener más información, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configurar directivas para archivar en Lync Server 2013 al usar la integración de Exchange Server</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="6f094-115">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="6f094-116">Debe especificar todas las opciones apropiadas en las configuraciones de archivado antes de habilitar el archivado.</span><span class="sxs-lookup"><span data-stu-id="6f094-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="6f094-117">Para obtener más información, vea <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">administrar las opciones de configuración de archivado en Lync Server 2013 para su organización, sitios y grupos</A> en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="6f094-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-change-an-archiving-policy"></a><span data-ttu-id="6f094-118">Para cambiar una directiva de archivado</span><span class="sxs-lookup"><span data-stu-id="6f094-118">To change an archiving policy</span></span>

1.  <span data-ttu-id="6f094-119">Desde una cuenta de usuario que se asigne al rol CsArchivingAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="6f094-119">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="6f094-120">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6f094-120">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6f094-121">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6f094-121">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6f094-122">En la barra de navegación izquierda, haga clic en **Supervisión y archivado** y, después, en **Directiva de archivado**.</span><span class="sxs-lookup"><span data-stu-id="6f094-122">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="6f094-123">En la lista de directivas, siga uno de estos pasos:</span><span class="sxs-lookup"><span data-stu-id="6f094-123">In the list of policies, do one of the following:</span></span>
    
      - <span data-ttu-id="6f094-124">Para cambiar la directiva de toda la implementación, haga clic en **Global** en la lista de directivas, y luego haga clic en **Editar** y en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="6f094-124">To change the policy for your entire deployment, click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="6f094-125">Para cambiar la directiva de un solo sitio, haga clic en el nombre del sitio en la lista de directivas, y luego haga clic en **Editar** y en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="6f094-125">To change the policy for a single site, click the site name in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="6f094-126">Para cambiar la directiva de solo usuario o grupo de usuarios, haga clic en el nombre del usuario o del grupo de usuarios en la lista de directivas, y luego haga clic en **Editar** y en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="6f094-126">To change the policy for a single user or user group, click the user or user group name in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="6f094-127">En la página **Editar directiva de archivado**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6f094-127">On the **Edit Archiving Policy** page, do the following:</span></span>
    
      - <span data-ttu-id="6f094-128">Para habilitar o deshabilitar el archivado interno para la directiva, active o desactive la casilla **Archivar comunicaciones internas**.</span><span class="sxs-lookup"><span data-stu-id="6f094-128">To enable or disable internal archiving for the policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="6f094-129">Para habilitar o deshabilitar el archivado externo para la directiva, active o desactiva la casilla **Archivar comunicaciones externas**.</span><span class="sxs-lookup"><span data-stu-id="6f094-129">To enable or disable external archiving for the policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="6f094-130">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="6f094-130">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="6f094-131">La configuración de una directiva de usuario únicamente se aplica a los usuarios y grupos de usuarios específicos a los que aplica la directiva.</span><span class="sxs-lookup"><span data-stu-id="6f094-131">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="6f094-132">Para obtener más información, consulte <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">aplicar una directiva de archivado a los usuarios en Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="6f094-132">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="enabling-and-disabling-archiving-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="6f094-133">Habilitar y deshabilitar el archivado mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f094-133">Enabling and Disabling Archiving by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="6f094-134">El archivado se puede habilitar y deshabilitar (en sesiones de comunicación internas y externas) mediante el cmdlet **set-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="6f094-134">Archiving can be enabled and disabled (for both internal and external communication sessions) by using the **Set-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="6f094-135">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6f094-135">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="6f094-136">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="6f094-136">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-archiving-of-internal-communication-sessions"></a><span data-ttu-id="6f094-137">Para habilitar el archivado de sesiones de comunicación interna</span><span class="sxs-lookup"><span data-stu-id="6f094-137">To enable the archiving of internal communication sessions</span></span>

  - <span data-ttu-id="6f094-138">Para habilitar el archivado de sesiones de comunicación interna, establece el valor de la propiedad **ArchiveInternal** en True ($true).</span><span class="sxs-lookup"><span data-stu-id="6f094-138">To enable archiving of internal communication sessions, set the value of the **ArchiveInternal** property to True ($True).</span></span> <span data-ttu-id="6f094-139">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6f094-139">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-external-communication-sessions"></a><span data-ttu-id="6f094-140">Para habilitar el archivado de sesiones de comunicación externa</span><span class="sxs-lookup"><span data-stu-id="6f094-140">To enable the archiving of external communication sessions</span></span>

  - <span data-ttu-id="6f094-141">Para habilitar el archivado de sesiones de comunicación externa, establece el valor de la propiedad **ArchiveExternal** en True ($true).</span><span class="sxs-lookup"><span data-stu-id="6f094-141">To enable archiving of external communication sessions, set the value of the **ArchiveExternal** property to True ($True).</span></span> <span data-ttu-id="6f094-142">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6f094-142">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveExternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="6f094-143">Para habilitar el archivado tanto en sesiones de comunicación internas como externas</span><span class="sxs-lookup"><span data-stu-id="6f094-143">To enable the archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="6f094-144">Para habilitar el archivado de las sesiones de comunicaciones internas y externas, establezca las propiedades **ArchiveInternal** y **ArchiveExternal** en true:</span><span class="sxs-lookup"><span data-stu-id="6f094-144">To enable archiving of both internal and external communications sessions, set both the **ArchiveInternal** and the **ArchiveExternal** properties to True:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

</div>

<div>

## <a name="to-disable-archiving"></a><span data-ttu-id="6f094-145">Para deshabilitar el archivado</span><span class="sxs-lookup"><span data-stu-id="6f094-145">To disable archiving</span></span>

  - <span data-ttu-id="6f094-146">Para deshabilitar el archivado por completo, establezca las propiedades **ArchiveInternal** y **ArchiveExternal** en falso ($false).</span><span class="sxs-lookup"><span data-stu-id="6f094-146">To disable archiving altogether, set both the **ArchiveInternal** and **ArchiveExternal** properties to False ($False).</span></span> <span data-ttu-id="6f094-147">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6f094-147">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $False -ArchiveExternal $False

</div>

<span data-ttu-id="6f094-148">Para obtener más información, consulte el tema de ayuda para el cmdlet [set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="6f094-148">For more information, see the help topic for the [Set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6f094-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f094-149">See Also</span></span>


[<span data-ttu-id="6f094-150">Administrar el archivado de comunicaciones internas y externas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f094-150">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="6f094-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f094-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

