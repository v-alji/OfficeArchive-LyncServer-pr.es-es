---
title: 'Lync Server 2013: Crear o modificar un sitio de red'
description: 'Lync Server 2013: crear o modificar un sitio de red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a network site
ms:assetid: 14e24856-9996-4da4-9f31-300940bdf5aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398218(v=OCS.15)
ms:contentKeyID: 48183488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4db9080f866becfcb94972787e099a69eac28c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431795"
---
# <a name="create-or-modify-a-network-site-in-lync-server-2013"></a><span data-ttu-id="91ef3-103">Crear o modificar un sitio de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91ef3-103">Create or modify a network site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91ef3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91ef3-104">

<span> </span></span></span>

<span data-ttu-id="91ef3-105">_**Última modificación del tema:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="91ef3-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="91ef3-106">Control de admisión de llamadas (CAC), E9-1-1 y las implementaciones por omisión de multimedia se basan en la configuración de los *sitios de red* que se definen dentro y siempre están asociados con una región de red.</span><span class="sxs-lookup"><span data-stu-id="91ef3-106">Call admission control (CAC), E9-1-1, and media bypass deployments rely on the configuration of *network sites* which are defined within and always associated with a network region.</span></span> <span data-ttu-id="91ef3-107">Un sitio de red representa una ubicación de sucursal, un conjunto de edificios o un campus.</span><span class="sxs-lookup"><span data-stu-id="91ef3-107">A network site represents a branch office location, a set of buildings, or a campus.</span></span> <span data-ttu-id="91ef3-108">Los sitios de red representan colecciones de subredes con un ancho de banda similar.</span><span class="sxs-lookup"><span data-stu-id="91ef3-108">Network sites represent collections of subnets with similar bandwidth.</span></span>

<span data-ttu-id="91ef3-109">Use los procedimientos siguientes para crear o modificar sitios de red.</span><span class="sxs-lookup"><span data-stu-id="91ef3-109">Use the following procedures to create or modify network sites.</span></span> <span data-ttu-id="91ef3-110">Por ejemplo, si ya ha creado sitios de red para una característica de voz, no es necesario crear sitios de red nuevos; otras características de voz usarán esos mismos sitios.</span><span class="sxs-lookup"><span data-stu-id="91ef3-110">For example, if you have already created network sites for one Voice feature, you do not need to create new network sites; other Voice features will use those same sites.</span></span> <span data-ttu-id="91ef3-111">Con todo, puede que sea necesario modificar una definición de sitio de red existente para aplicar una configuración específica de una característica.</span><span class="sxs-lookup"><span data-stu-id="91ef3-111">You may, however, need to modify an existing network site definition to apply feature-specific settings.</span></span> <span data-ttu-id="91ef3-112">Así, si ha creado un sitio de red para E9-1-1, deberá modificar el sitio de red durante la implementación de un control de admisión de llamadas con objeto de aplicar un perfil de directiva de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="91ef3-112">For example, if you created a network site for E9-1-1, you need to modify the network site during deployment of call admission control to apply a bandwidth policy profile.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="91ef3-113">En el lugar donde estén, puede encontrar ejemplos y requisitos específicos para los sitios de red como pertenecen a una característica avanzada de voz en la documentación de implementación de cada característica:</span><span class="sxs-lookup"><span data-stu-id="91ef3-113">Where they exist, you can find specific examples and requirements for network sites as they pertain to an advanced Voice feature in the Deployment documentation for each feature:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="91ef3-114"><A href="lync-server-2013-configure-network-sites-for-cac.md">Configurar sitios de red para CAC en Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="91ef3-114"><A href="lync-server-2013-configure-network-sites-for-cac.md">Configure network sites for CAC in Lync Server 2013</A></span></span></P></LI></UL>



</div>

<span data-ttu-id="91ef3-115">Para obtener más información sobre cómo trabajar con sitios de red, consulte la documentación del shell de administración de Lync Server para los siguientes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="91ef3-115">For details about working with network sites, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="91ef3-116">New-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="91ef3-116">New-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite)

  - [<span data-ttu-id="91ef3-117">Get-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="91ef3-117">Get-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite)

  - [<span data-ttu-id="91ef3-118">Set-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="91ef3-118">Set-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSite)

  - [<span data-ttu-id="91ef3-119">Remove-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="91ef3-119">Remove-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSite)

<div>

## <a name="create-a-network-site"></a><span data-ttu-id="91ef3-120">Crear un sitio de red</span><span class="sxs-lookup"><span data-stu-id="91ef3-120">Create a Network Site</span></span>

<span data-ttu-id="91ef3-121">Cree una región de red que pueda usar el control de admisión de llamadas, el E9-1-1 o la omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="91ef3-121">Create a network region that can be used by call admission control, E9-1-1, or media bypass.</span></span>

<div>

## <a name="to-create-a-network-site-by-using-management-shell"></a><span data-ttu-id="91ef3-122">Para crear un sitio de red mediante el shell de administración</span><span class="sxs-lookup"><span data-stu-id="91ef3-122">To create a network site by using Management Shell</span></span>

1.  <span data-ttu-id="91ef3-123">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-123">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="91ef3-124">Ejecute el cmdlet New-CsNetworkSite para crear sitios de red:</span><span class="sxs-lookup"><span data-stu-id="91ef3-124">Run the New-CsNetworkSite cmdlet to create network sites:</span></span>
    
        New-CsNetworkSite -NetworkSiteID <string>
    
    <span data-ttu-id="91ef3-125">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="91ef3-125">For example:</span></span>
    
        New-CsNetworkSite -NetworkSiteID Chicago -Description "Corporate headquarters"-NetworkRegionID NorthAmerica
    
    <span data-ttu-id="91ef3-126">En este ejemplo, ha creado un sitio de red denominado “Chicago” que se encuentra en la región de red “NorthAmerica”.</span><span class="sxs-lookup"><span data-stu-id="91ef3-126">In this example, you created a network site called “Chicago” that is in the “NorthAmerica” network region.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="91ef3-127">Esta región de red ya debe existir para que este comando se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="91ef3-127">The NorthAmerica network region must already exist for this command to run successfully.</span></span>

    
    </div>

3.  <span data-ttu-id="91ef3-128">Para terminar de crear sitios de red en su topología, repita el paso 2 con la configuración pertinente del resto de sitios.</span><span class="sxs-lookup"><span data-stu-id="91ef3-128">To finish creating network sites for your topology, repeat step 2 with settings for other sites.</span></span>

</div>

<div>

## <a name="to-create-a-network-site-by-using-lync-server-control-panel"></a><span data-ttu-id="91ef3-129">Para crear un sitio de red con el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="91ef3-129">To create a network site by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="91ef3-130">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91ef3-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="91ef3-131">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="91ef3-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="91ef3-132">En la barra de navegación izquierda, haga clic en **Configuración de red**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-132">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="91ef3-133">Haga clic en el botón de navegación **Sitio**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-133">Click the **Site** navigation button.</span></span>

4.  <span data-ttu-id="91ef3-134">Haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-134">Click **New**.</span></span>

5.  <span data-ttu-id="91ef3-135">En la página **Nuevo sitio**, haga clic en **Nombre** y, a continuación, escriba un nombre para el sitio de red.</span><span class="sxs-lookup"><span data-stu-id="91ef3-135">On the **New Site** page, click **Name** and then type a name for the network site.</span></span>

6.  <span data-ttu-id="91ef3-136">Haga clic en **Región** y, a continuación, en una región de la lista.</span><span class="sxs-lookup"><span data-stu-id="91ef3-136">Click **Region**, and then click a region in the list.</span></span>

7.  <span data-ttu-id="91ef3-137">Si lo desea, también puede hacer clic en **Directiva de ancho de banda** y hacer clic en una directiva de ancho de banda de la lista.</span><span class="sxs-lookup"><span data-stu-id="91ef3-137">Optionally, click **Bandwidth policy**, and then click a bandwidth policy in the list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="91ef3-138">Las directivas de ancho de banda solo son necesarias cuando se implementa el control de admisión de llamadas en el sitio.</span><span class="sxs-lookup"><span data-stu-id="91ef3-138">Bandwidth policy is required only if you deploy call admission control at the site.</span></span>

    
    </div>

8.  <span data-ttu-id="91ef3-139">Si lo desea, también puede hacer clic en **Directiva de ubicación** y hacer clic en una directiva de ubicación de la lista.</span><span class="sxs-lookup"><span data-stu-id="91ef3-139">Optionally, click **Location policy**, and then click a location policy in the list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="91ef3-140">Las directivas de ubicación solo son necesarias cuando se implementa E9-1-1 en el sitio.</span><span class="sxs-lookup"><span data-stu-id="91ef3-140">Location policy is required only if you deploy E9-1-1 at the site.</span></span>

    
    </div>

9.  <span data-ttu-id="91ef3-141">Si lo desea, también puede hacer clic en **Descripción** y aportar más información que describa este sitio de red.</span><span class="sxs-lookup"><span data-stu-id="91ef3-141">Optionally, click **Description**, and then type additional information to describe this network site.</span></span>

10. <span data-ttu-id="91ef3-142">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-142">Click **Commit**.</span></span>

11. <span data-ttu-id="91ef3-143">Para terminar de crear sitios de red en su topología, repita los pasos 4 a 10 con la configuración pertinente del resto de sitios.</span><span class="sxs-lookup"><span data-stu-id="91ef3-143">To finish creating network sites for your topology, repeat steps 4 through 10 with settings for other sites.</span></span>

</div>

</div>

<div>

## <a name="modify-a-network-site"></a><span data-ttu-id="91ef3-144">Modificar un sitio de red</span><span class="sxs-lookup"><span data-stu-id="91ef3-144">Modify a Network Site</span></span>

<span data-ttu-id="91ef3-145">Modificar una región de red que puede ser usada por control de admisión de llamadas, E9-1-1 o por omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="91ef3-145">Modify a network region that can be used by call admission control, E9-1-1, or media bypass.</span></span>

<div>

## <a name="to-modify-a-network-site"></a><span data-ttu-id="91ef3-146">Para modificar un sitio de red</span><span class="sxs-lookup"><span data-stu-id="91ef3-146">To modify a network site</span></span>

1.  <span data-ttu-id="91ef3-147">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="91ef3-148">Ejecute el cmdlet Set-CsNetworkSite para modificar sitios de red:</span><span class="sxs-lookup"><span data-stu-id="91ef3-148">Run the Set-CsNetworkSite cmdlet to modify network sites:</span></span>
    
        Set-CsNetworkSite -Identity <string>
    
    <span data-ttu-id="91ef3-149">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="91ef3-149">For example:</span></span>
    
        Set-CsNetworkSite -Identity Albuquerque -NetworkRegionID NorthAmerica
    
    <span data-ttu-id="91ef3-p104">En este ejemplo, el sitio denominado “Albuquerque” se traslada a la región de red “NorthAmerica”. Para modificar la configuración de sitio de red a fin de implementar el control de admisión de llamadas, E9-1-1 o el desvío de medios, cambie la configuración del sitio de red ejecutando el cmdlet Set-CsNetworkSite con los parámetros BWPolicyProfileID o LocationPolicy respectivamente.</span><span class="sxs-lookup"><span data-stu-id="91ef3-p104">In this example, the site called “Albuquerque” is moved to the “NorthAmerica” network region. To modify the network site configuration to deploy call admission control, E9-1-1, or media bypass, modify the network site settings by running the Set-CsNetworkSite cmdlet with the BWPolicyProfileID or LocationPolicy parameter, respectively.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="91ef3-p105">En el caso del desvío de medios, existe un parámetro BypassID, si bien se recomienda encarecidamente no invalidar automáticamente los identificadores de desvío generados. No es necesario especificar más parámetros para configurar un sitio de red para el desvío de medios.</span><span class="sxs-lookup"><span data-stu-id="91ef3-p105">Although the BypassID parameter exists for media bypass, we strongly recommend that you do not override automatically generated bypass IDs. You do not need to specify additional parameters to configure a network site for media bypass.</span></span>

    
    </div>

3.  <span data-ttu-id="91ef3-154">Para terminar de modificar sitios de red en su topología, repita el paso 2 con la configuración pertinente del resto de sitios.</span><span class="sxs-lookup"><span data-stu-id="91ef3-154">To finish modifying network sites for your topology, repeat step 2 with settings for other sites.</span></span>

</div>

<div>

## <a name="to-modify-a-network-site-by-using-lync-server-control-panel"></a><span data-ttu-id="91ef3-155">Para modificar un sitio de red mediante el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="91ef3-155">To modify a network site by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="91ef3-156">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91ef3-156">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="91ef3-157">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="91ef3-157">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="91ef3-158">En la barra de navegación izquierda, haga clic en **Configuración de red**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-158">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="91ef3-159">Haga clic en el botón de navegación **Sitio**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-159">Click the **Site** navigation button.</span></span>

4.  <span data-ttu-id="91ef3-160">En la tabla, haga clic en el sitio de red que desee modificar.</span><span class="sxs-lookup"><span data-stu-id="91ef3-160">In the table, click the network site that you want to modify.</span></span>

5.  <span data-ttu-id="91ef3-161">Haga clic en **Editar** y, a continuación, en **Mostrar detalles…**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-161">Click **Edit**, and then click **Show details…**.</span></span>

6.  <span data-ttu-id="91ef3-162">En la página **Modificar sitio**, cambie los valores de la configuración del sitio de red según proceda.</span><span class="sxs-lookup"><span data-stu-id="91ef3-162">On the **Edit Site** page, change the values for this network site’s settings as appropriate.</span></span>

7.  <span data-ttu-id="91ef3-163">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-163">Click **Commit**.</span></span>

8.  <span data-ttu-id="91ef3-164">Para terminar de modificar sitios de red, repita los pasos 4 a 7 con la configuración pertinente del resto de sitios.</span><span class="sxs-lookup"><span data-stu-id="91ef3-164">To finish modify network sites, repeat steps 4 through 7 with settings for other sites.</span></span>

<span data-ttu-id="91ef3-165"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91ef3-165"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

