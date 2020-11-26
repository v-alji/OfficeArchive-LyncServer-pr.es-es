---
title: 'Lync Server 2013: crear una directiva de archivado para habilitar o deshabilitar el archivado de las comunicaciones internas o externas de determinados sitios o usuarios'
description: 'Lync Server 2013: crear una directiva de archivado para habilitar o deshabilitar el archivado de las comunicaciones internas o externas de determinados sitios o usuarios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431991"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a><span data-ttu-id="fccf2-103">Crear una directiva de archivado en Lync Server 2013 para habilitar o deshabilitar el archivado de las comunicaciones internas o externas para usuarios o sitios específicos</span><span class="sxs-lookup"><span data-stu-id="fccf2-103">Creating an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for specific sites or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fccf2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fccf2-104">

<span> </span></span></span>

<span data-ttu-id="fccf2-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="fccf2-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="fccf2-106">En Lync Server 2013, se usan directivas para habilitar y deshabilitar el archivado de comunicaciones internas y comunicaciones externas para usuarios alojados en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fccf2-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="fccf2-107">Esto incluye las siguientes directivas de archivado:</span><span class="sxs-lookup"><span data-stu-id="fccf2-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="fccf2-108">Una directiva global que se crea de forma predeterminada al implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fccf2-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="fccf2-109">Directivas opcionales a nivel de sitio y de usuario que puede crear y usar para especificar cómo se implementa el archivado para usuarios o sitios específicos.</span><span class="sxs-lookup"><span data-stu-id="fccf2-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="fccf2-110">Inicialmente, debe configurar las directivas de archivado al implementar el archivado, pero puede cambiar, agregar y eliminar directivas después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="fccf2-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="fccf2-111">En el panel de control de Lync Server 2013, puede usar la página **Directiva de archivado** del grupo **archivado y supervisión** para administrar directivas a nivel global, nivel de sitio y nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="fccf2-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="fccf2-112">Si integra el almacenamiento de Lync Server con el almacenamiento de Exchange 2013, las directivas de usuario de Exchange tienen prioridad sobre las directivas de archivado de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fccf2-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="fccf2-113">Para obtener más información sobre cómo se implementan las directivas, incluida la jerarquía de directivas, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="fccf2-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="fccf2-114">Para controlar la implementación de archivado, debe especificar las opciones para archivar las configuraciones, por ejemplo, si desea archivar la mensajería instantánea o la Conferencia, el uso del modo crítico y las opciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="fccf2-114">To control the implementation of Archiving, you must specify options in Archiving configurations, such as whether to archive IM or conferencing, the use of critical mode, and purging options.</span></span> <span data-ttu-id="fccf2-115">De forma predeterminada, no se habilita ninguna opción en la configuración global de archivado ni en ninguna configuración de archivado de sitios o grupos.</span><span class="sxs-lookup"><span data-stu-id="fccf2-115">By default no options are enabled in the global Archiving configuration or any site or pool Archiving configuration.</span></span> <span data-ttu-id="fccf2-116">Debe especificar todas las opciones apropiadas en las configuraciones de archivado antes de habilitar el archivado de las comunicaciones internas o externas en las directivas de archivado.</span><span class="sxs-lookup"><span data-stu-id="fccf2-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving for internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="fccf2-117">Para obtener más información, vea <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">administrar las opciones de configuración de archivado en Lync Server 2013 para su organización, sitios y grupos</A> en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="fccf2-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span><BR><span data-ttu-id="fccf2-118">Si habilitó la integración de Microsoft Exchange para su implementación, las directivas de Exchange controlan si el archivado está habilitado para los usuarios que están alojados en Exchange 2013 y si sus buzones se ponen en espera In-Place.</span><span class="sxs-lookup"><span data-stu-id="fccf2-118">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="fccf2-119">Para obtener más información, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configurar directivas para archivar en Lync Server 2013 al usar la integración de Exchange Server</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="fccf2-119">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a><span data-ttu-id="fccf2-120">Para crear una directiva de archivado para un sitio o usuarios</span><span class="sxs-lookup"><span data-stu-id="fccf2-120">To create an archiving policy for a site or users</span></span>

1.  <span data-ttu-id="fccf2-121">Desde una cuenta de usuario que se asigne al rol CsArchivingAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="fccf2-121">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fccf2-122">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fccf2-122">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="fccf2-123">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fccf2-123">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="fccf2-124">En la barra de navegación izquierda, haga clic en **Supervisión y archivado** y, después, en **Directiva de archivado**.</span><span class="sxs-lookup"><span data-stu-id="fccf2-124">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="fccf2-125">Haga clic en **Nuevo** y, luego, siga uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="fccf2-125">Click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="fccf2-126">Para crear una directiva de archivado de nivel de sitio, haga clic en **Directiva del sitio** y, a continuación, en **seleccionar un sitio**, haga clic en el sitio al que se va a aplicar la Directiva.</span><span class="sxs-lookup"><span data-stu-id="fccf2-126">To create a site-level archiving policy, click **Site policy** and then, in **Select a site**, click the site to which the policy is to be applied.</span></span>
    
      - <span data-ttu-id="fccf2-127">Para crear una directiva de archivado de usuario, haga clic en **Directiva de usuario**.</span><span class="sxs-lookup"><span data-stu-id="fccf2-127">To create a user-level archiving policy, click **User policy**.</span></span>

5.  <span data-ttu-id="fccf2-128">En **Directiva de archivado nueva**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fccf2-128">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="fccf2-129">En **Nombre**, especifique un nombre para la nueva directiva (por ejemplo, externalContoso).</span><span class="sxs-lookup"><span data-stu-id="fccf2-129">In **Name**, specify a name for the new policy (for example, externalContoso).</span></span>
    
      - <span data-ttu-id="fccf2-130">En **Descripción**, proporcione información detallada sobre la función de la directiva (por ejemplo, directiva de archivado de usuarios externos para Contoso).</span><span class="sxs-lookup"><span data-stu-id="fccf2-130">In **Description**, provide details about what the policy is (for example, External user archiving policy for Contoso).</span></span>
    
      - <span data-ttu-id="fccf2-131">Para controlar el archivado de comunicaciones con usuarios internos, active o desactive la casilla **Archivar comunicaciones internas**.</span><span class="sxs-lookup"><span data-stu-id="fccf2-131">To control archiving of communications with internal users, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="fccf2-132">Para controlar el archivado de comunicaciones externas, active o desactive la casilla **Archivar comunicaciones externas**.</span><span class="sxs-lookup"><span data-stu-id="fccf2-132">To control archiving of communications with external users, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="fccf2-133">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="fccf2-133">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="fccf2-134">La configuración de una directiva de usuario únicamente se aplica a los usuarios y grupos de usuarios específicos a los que aplica la directiva.</span><span class="sxs-lookup"><span data-stu-id="fccf2-134">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="fccf2-135">Para obtener más información, consulte <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">aplicar una directiva de archivado a los usuarios en Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="fccf2-135">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="fccf2-136">Creación de una directiva de archivado mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fccf2-136">Creating an Archiving Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="fccf2-137">Las directivas de archivado se pueden crear con Windows PowerShell y el cmdlet **Remove-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="fccf2-137">Archiving policies can be created by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="fccf2-138">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fccf2-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="fccf2-139">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="fccf2-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a><span data-ttu-id="fccf2-140">Para crear una nueva Directiva de archivado en el ámbito del sitio</span><span class="sxs-lookup"><span data-stu-id="fccf2-140">To create a new archiving policy at the site scope</span></span>

  - <span data-ttu-id="fccf2-141">Este comando crea una directiva de archivado para el sitio Redmond:</span><span class="sxs-lookup"><span data-stu-id="fccf2-141">This command creates a new archiving policy for the Redmond site:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a><span data-ttu-id="fccf2-142">Para crear una nueva Directiva de archivado en el ámbito de cada usuario</span><span class="sxs-lookup"><span data-stu-id="fccf2-142">To create a new archiving policy at the per-user scope</span></span>

  - <span data-ttu-id="fccf2-143">Para crear una nueva Directiva de archivado en el ámbito de cada usuario, simplemente especifique una identidad única al crear la Directiva:</span><span class="sxs-lookup"><span data-stu-id="fccf2-143">To create a new archiving policy at the per-user scope, simply specify a unique Identity when creating the policy:</span></span>
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a><span data-ttu-id="fccf2-144">Para crear una directiva de archivado que permita el archivado de sesiones de comunicaciones internas</span><span class="sxs-lookup"><span data-stu-id="fccf2-144">To create a new archiving policy that enables archiving of internal communication sessions</span></span>

  - <span data-ttu-id="fccf2-145">Ya que no se especifican parámetros (excepto el parámetro obligatorio Identity) en los comandos anteriores, las nuevas directivas usarán los valores predeterminados para todas sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="fccf2-145">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding commands, the new policies will use the default values for all their properties.</span></span> <span data-ttu-id="fccf2-146">Para crear directivas que usen otros valores de propiedades, basta con incluir el parámetro y el valor de parámetro correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fccf2-146">To create policies that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="fccf2-147">Por ejemplo, para crear una directiva de archivado que permita el archivado de sesiones de mensajería instantánea interna, use un comando como este:</span><span class="sxs-lookup"><span data-stu-id="fccf2-147">For example, to create an archiving policy that permits archiving of internal instant messaging sessions use a command like this:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="fccf2-148">Para crear una directiva de archivado que permita el archivado de sesiones de comunicaciones tanto internas como externas</span><span class="sxs-lookup"><span data-stu-id="fccf2-148">To create a new archiving policy that enables archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="fccf2-149">Con la inclusión de varios parámetros se pueden cambiar varios valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="fccf2-149">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="fccf2-150">Por ejemplo, este comando configura la nueva Directiva para archivar las sesiones de mensajería instantánea internas y externas:</span><span class="sxs-lookup"><span data-stu-id="fccf2-150">For example, this command configures the new policy to archiving both internal and external instant messaging sessions:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

<span data-ttu-id="fccf2-151">Para obtener más información, vea el tema de ayuda sobre el cmdlet [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="fccf2-151">For more information, see the help topic for the [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fccf2-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="fccf2-152">See Also</span></span>


[<span data-ttu-id="fccf2-153">Administrar el archivado de comunicaciones internas y externas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fccf2-153">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="fccf2-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fccf2-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

