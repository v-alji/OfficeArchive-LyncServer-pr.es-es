---
title: Configurar las opciones globales del desvío de medios para usar información de sitio y región
description: Configure la configuración global de omisión de medios para usar la información del sitio y la región.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media bypass global settings to use site and region information
ms:assetid: 0a21cdf1-f350-49da-b346-70806f256bea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398150(v=OCS.15)
ms:contentKeyID: 48183360
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a65dcec966030262d6d0fb5530b94f2411003c7a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433965"
---
# <a name="configure-media-bypass-global-settings-in-lync-server-2013-to-use-site-and-region-information"></a><span data-ttu-id="e396d-103">Configure media bypass global settings in Lync Server 2013 to use site and region information</span><span class="sxs-lookup"><span data-stu-id="e396d-103">Configure media bypass global settings in Lync Server 2013 to use site and region information</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e396d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e396d-104">

<span> </span></span></span>

<span data-ttu-id="e396d-105">_**Última modificación del tema:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="e396d-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="e396d-106">En este tema se supone que ya ha configurado la omisión de medios para cualquier conexión troncal desde el servidor de mediación a un interlocutor (una puerta de enlace de red telefónica conmutada (RTC), un IP-PBX o un controlador de borde de sesión (SBC) en un proveedor de servicios de telefonía por Internet</span><span class="sxs-lookup"><span data-stu-id="e396d-106">This topic assumes that you have already configured media bypass for any trunk connections from the Mediation Server to a peer (a public switched telephone network (PSTN) gateway, an IP-PBX, or a Session Border Controller (SBC) at an Internet Telephony Service Provider (ITSP) for a specific site or service for which you want media to bypass the Mediation Server.</span></span><BR><span data-ttu-id="e396d-107">En este tema también se da por sentado que ha definido todos los sitios centrales y sucursales en el generador de topologías de forma que coincidan con la región de red, el sitio de red y la configuración de subred que ha realizado según los pasos de <A href="lync-server-2013-create-or-modify-a-network-region.md">crear o modificar una región de red en Lync server 2013</A>, <A href="lync-server-2013-create-or-modify-a-network-site.md">crear o modificar un sitio de red en Lync Server 2013</A>y <A href="lync-server-2013-associate-a-subnet-with-a-network-site.md">asociar una 2013 subred</A></span><span class="sxs-lookup"><span data-stu-id="e396d-107">This topic also assumes that you have defined all central sites and branch sites in Topology Builder in a way that matches the network region, network site, and subnet configuration that you performed according to the steps in <A href="lync-server-2013-create-or-modify-a-network-region.md">Create or modify a network region in Lync Server 2013</A>, <A href="lync-server-2013-create-or-modify-a-network-site.md">Create or modify a network site in Lync Server 2013</A>, and <A href="lync-server-2013-associate-a-subnet-with-a-network-site.md">Associate a subnet with a network site in Lync Server 2013</A>.</span></span> <span data-ttu-id="e396d-108">Si no coinciden, la omisión de elementos multimedia no se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="e396d-108">If they do not match, then media bypass will not succeed.</span></span>



</div>

<span data-ttu-id="e396d-109">Además de habilitar la omisión de medios para conexiones troncales individuales asociadas con un mismo nivel, también debe establecer la configuración global.</span><span class="sxs-lookup"><span data-stu-id="e396d-109">In addition to enabling media bypass for individual trunk connections associated with a peer, you must also configure global settings.</span></span> <span data-ttu-id="e396d-110">Si usa los pasos de este tema para configurar las opciones globales de omisión de medios, se supone que una o ambas de las siguientes situaciones afectan a la configuración:</span><span class="sxs-lookup"><span data-stu-id="e396d-110">If you use the steps in this topic to configure global settings for media bypass, the assumption is that one or both of the following situations affects your configuration:</span></span>

  - <span data-ttu-id="e396d-111">*No* tiene buena conectividad entre los puntos de conexión de Lync Server y los elementos del mismo nivel para los que configuró el bypass de medios en la conexión troncal.</span><span class="sxs-lookup"><span data-stu-id="e396d-111">You *do not* have good connectivity between Lync Server endpoints and any peers for which you configured media bypass on the trunk connection.</span></span>

  - <span data-ttu-id="e396d-112">Control de admisión de llamadas (CAC) para la administración del ancho de banda está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e396d-112">Call admission control (CAC) for bandwidth management is enabled.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="e396d-113">Para obtener más información sobre las consideraciones para el control de admisión de llamadas y para la omisión de medios, consulte la sección "control de admisión de conexiones RTC" en servidor de omisión y mediación de <A href="lync-server-2013-media-bypass-and-mediation-server.md">multimedia en Lync server 2013</A> en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="e396d-113">For details about the considerations for both call admission control and media bypass, see the "Call Admission Control of PSTN Connections" section in <A href="lync-server-2013-media-bypass-and-mediation-server.md">Media bypass and Mediation Server in Lync Server 2013</A> in the Planning documentation.</span></span>

    
    </div>

<span data-ttu-id="e396d-p103">La información de región de red y sitio de red se comparte entre las características de Enterprise Voice avanzadas del control de admisión de llamadas y el desvío de medios cuando ambos están habilitados. Por consiguiente, si ya ha configurado el control de admisión de llamadas, no es necesario que realice el siguiente procedimiento para editar la información de región y sitio específica para la omisión de medios. Siga los pasos de este procedimiento si todavía no ha configurado los sitios y regiones de red para el control de admisión de llamadas y desea cambiar las opciones del omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="e396d-p103">Network region and network site information is shared between call admission control and media bypass advanced Enterprise Voice features when both are enabled. Therefore, if you have already configured call admission control, you are not required to use the following procedure to edit the site and region information specifically for media bypass. Follow the steps in this procedure if you have not yet configured network regions and sites for call admission control, and you want to change media bypass settings.</span></span>

<span data-ttu-id="e396d-117">O bien, siga estos pasos si desea usar la información del sitio y de la región para tomar la decisión de omisión, pero no tiene la intención de habilitar el control de admisión de llamadas.</span><span class="sxs-lookup"><span data-stu-id="e396d-117">Or, follow these steps if you want to use site and region information in making the bypass decision, but have no intention of enabling call admission control.</span></span> <span data-ttu-id="e396d-118">En tal caso, los vínculos con restricciones de ancho de banda seguirán representados mediante directivas de intersitio de red, tal y como se describe en [crear directivas entre sitios de red en Lync Server 2013](lync-server-2013-create-network-intersite-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e396d-118">In such a case, bandwidth restricted links will still need to be represented through network intersite policies, as described in [Create network intersite policies in Lync Server 2013](lync-server-2013-create-network-intersite-policies.md).</span></span> <span data-ttu-id="e396d-119">Las restricciones de ancho de banda reales no son tan importantes en este caso, porque el control de admisión de llamadas no se ha habilitado.</span><span class="sxs-lookup"><span data-stu-id="e396d-119">The actual bandwidth constraints are not as important in this case, because call admission control has not been enabled.</span></span> <span data-ttu-id="e396d-120">En su lugar, estos vínculos se usan para particionar subredes para especificar aquellas que no tienen límites de ancho de banda y que pueden, por consiguiente, emplear omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="e396d-120">Instead, these links are used to partition subnets to specify those that have no bandwidth limits and can, therefore, employ media bypass.</span></span> <span data-ttu-id="e396d-121">Tenga en cuenta que esto también es cierto cuando ambos están habilitados el control de admisión de llamadas y los medios.</span><span class="sxs-lookup"><span data-stu-id="e396d-121">Note that this is also true when call admission control and media bypass are both enabled.</span></span>

<span data-ttu-id="e396d-122">Además, para que el omisión funcione correctamente, es necesario que haya coherencia entre un sitio definido en el generador de topologías y que se defina al configurar las regiones de red y los sitios de red.</span><span class="sxs-lookup"><span data-stu-id="e396d-122">Furthermore, for bypass to work properly there must be consistency between a site as defined in Topology Builder and as it is defined when you configure network regions and network sites.</span></span> <span data-ttu-id="e396d-123">Por ejemplo, si tiene un sitio de sucursal que ha definido en el generador de topología y tiene una puerta de enlace RTC implementada, ese sitio de sucursal debe estar configurado con una directiva de telefonía IP empresarial que permita a los usuarios de la sucursal enrutar sus llamadas RTC a través de la puerta de enlace PSTN en el sitio de la sucursal.</span><span class="sxs-lookup"><span data-stu-id="e396d-123">For example, if you have a branch site that you defined in Topology Builder as having only a PSTN gateway deployed, then that branch site must be configured with an Enterprise Voice policy that enables branch site users to have their PSTN calls routed through the PSTN gateway at the branch site.</span></span>

<div>

## <a name="to-configure-site-and-region-information-for-media-bypass"></a><span data-ttu-id="e396d-124">Configurar la información de sitio y región para el desvío de medios</span><span class="sxs-lookup"><span data-stu-id="e396d-124">To Configure Site and Region Information for Media Bypass</span></span>

1.  <span data-ttu-id="e396d-125">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e396d-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e396d-126">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e396d-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="e396d-127">En la barra de navegación izquierda, haga clic en **Configuración de red**.</span><span class="sxs-lookup"><span data-stu-id="e396d-127">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="e396d-128">Haga doble clic en la configuración **Global** de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e396d-128">Double-click the **Global** configuration in the table.</span></span>

4.  <span data-ttu-id="e396d-129">En la página **Editar configuración global**, seleccione la casilla **Habilitar omisión de medios**.</span><span class="sxs-lookup"><span data-stu-id="e396d-129">On the **Edit Global Setting** page, select the **Enable media bypass** check box.</span></span>

5.  <span data-ttu-id="e396d-130">Haga clic en **Usar la configuración de sitios y regiones**.</span><span class="sxs-lookup"><span data-stu-id="e396d-130">Click **Use sites and region configuration**.</span></span>

6.  <span data-ttu-id="e396d-131">Si es necesario, seleccione la casilla **Habilitar omisión para sitios sin asignar**.</span><span class="sxs-lookup"><span data-stu-id="e396d-131">If necessary, select the **Enable bypass for non-mapped sites** check box.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="e396d-p107">Seleccione esta casilla solamente si dispone de uno o más sitios grandes asociados a la misma región que no tengan restricciones de ancho de banda (por ejemplo, un sitio central grande) y si dispone también de algunas sucursales asociadas con la misma región que no tienen restricciones de ancho de banda. Cuando habilita la omisión para sitios sin asignar, la configuración se simplifica ya que solo especifica subredes asociadas con las sucursales, en lugar de tener que especificar todas las subredes asociadas a todos los sitios. Se recomienda no activar esta casilla si se ha habilitado el control de admisión de llamadas.</span><span class="sxs-lookup"><span data-stu-id="e396d-p107">Select this check box only if you have one or more large sites associated with the same region that do not have bandwidth constraints (for example, a large central site), but you also have some branch sites associated with the same region that do have bandwidth constraints. When you enable bypass for non-mapped sites, configuration is streamlined in that you specify only the subnets associated with the branch sites, rather than needing to specify all subnets associated with all sites. We recommend that you do not select this check box if call admission control is enabled.</span></span>

    
    </div>

7.  <span data-ttu-id="e396d-135">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="e396d-135">Click **Commit**.</span></span>

<span data-ttu-id="e396d-136">A continuación, agregue subredes al sitio de red, como se describe en [asociar subredes con sitios de red para evitar contenido multimedia en Lync Server 2013](lync-server-2013-associate-subnets-with-network-sites-for-media-bypass.md).</span><span class="sxs-lookup"><span data-stu-id="e396d-136">Next, add subnets to the network site, as described in [Associate subnets with network sites for media bypass in Lync Server 2013](lync-server-2013-associate-subnets-with-network-sites-for-media-bypass.md).</span></span> <span data-ttu-id="e396d-137">(Los procedimientos reales para asociar subredes con sitios de red se describen en [asociar una subred con un sitio de red en Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md)). Una vez que haya asociado todas las subredes a los sitios de red, se completará la implementación de omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="e396d-137">(The actual procedures for associating subnets with network sites are described in [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).) After you associate all subnets with network sites, media bypass deployment is complete.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="e396d-138">Si todavía no ha creado regiones de red y sitios de red, deberá crearlos en primer lugar para poder continuar con la implementación de la omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="e396d-138">If you have not already created network regions and network sites, you must first create those before you can proceed with media bypass deployment.</span></span> <span data-ttu-id="e396d-139">Para obtener más información, vea <A href="lync-server-2013-create-or-modify-a-network-region.md">crear o modificar una región de red en Lync server 2013</A> y <A href="lync-server-2013-create-or-modify-a-network-site.md">crear o modificar un sitio de red en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e396d-139">For details, see <A href="lync-server-2013-create-or-modify-a-network-region.md">Create or modify a network region in Lync Server 2013</A> and <A href="lync-server-2013-create-or-modify-a-network-site.md">Create or modify a network site in Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e396d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e396d-140">See Also</span></span>


[<span data-ttu-id="e396d-141">Asociar subredes con sitios de red para evitar contenido multimedia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e396d-141">Associate subnets with network sites for media bypass in Lync Server 2013</span></span>](lync-server-2013-associate-subnets-with-network-sites-for-media-bypass.md)  
  

<span data-ttu-id="e396d-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e396d-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

