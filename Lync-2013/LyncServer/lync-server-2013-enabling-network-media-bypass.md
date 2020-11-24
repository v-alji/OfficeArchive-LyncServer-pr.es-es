---
title: 'Lync Server 2013: habilitar la omisión de medios de red'
description: 'Lync Server 2013: habilitar la omisión de medios de red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling network media bypass
ms:assetid: 95c4fa06-49d3-41ac-acdc-7dcda66e5508
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182552(v=OCS.15)
ms:contentKeyID: 48184846
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1218376903aa42e1ea55205e3a9e8d16aade9a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399281"
---
# <a name="enabling-network-media-bypass-in-lync-server-2013"></a><span data-ttu-id="42b50-103">Habilitar el omisión de medios de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42b50-103">Enabling network media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42b50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42b50-104">

<span> </span></span></span>

<span data-ttu-id="42b50-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="42b50-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="42b50-106">La configuración de omisión de medios se aplica globalmente en una implementación de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="42b50-106">Media bypass settings apply globally across a Microsoft Lync Server 2013 deployment.</span></span> <span data-ttu-id="42b50-107">La omisión de medios permite que las llamadas omitan el servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="42b50-107">Media bypass allows calls to bypass the Mediation Server.</span></span> <span data-ttu-id="42b50-108">Para obtener información sobre Cuándo usar la omisión de medios, consulte [planificación de la omisión de medios en Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) en la sección planificación.</span><span class="sxs-lookup"><span data-stu-id="42b50-108">For details about when to use Media bypass, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning section.</span></span>

<span data-ttu-id="42b50-109">Puede habilitar y configurar la omisión de medios en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="42b50-109">You can enable and configure media bypass from the Lync Server Control Panel.</span></span>

<div>

## <a name="to-enable-and-configure-media-bypass"></a><span data-ttu-id="42b50-110">Para habilitar y configurar la omisión de medios</span><span class="sxs-lookup"><span data-stu-id="42b50-110">To enable and configure media bypass</span></span>

1.  <span data-ttu-id="42b50-111">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="42b50-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="42b50-112">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="42b50-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="42b50-113">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="42b50-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="42b50-114">En la barra de navegación izquierda, haga clic en **configuración de red** y, después, en **global**.</span><span class="sxs-lookup"><span data-stu-id="42b50-114">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="42b50-115">En la página **global** , haga clic en la configuración **global** .</span><span class="sxs-lookup"><span data-stu-id="42b50-115">On the **Global** page, click the **Global** configuration.</span></span> <span data-ttu-id="42b50-116">Siempre hay una sola configuración y siempre se denomina global.</span><span class="sxs-lookup"><span data-stu-id="42b50-116">There is always only one configuration, and it is always named Global.</span></span>

5.  <span data-ttu-id="42b50-117">En el menú **Editar** , haga clic en **Ver detalles**.</span><span class="sxs-lookup"><span data-stu-id="42b50-117">On the **Edit** menu, click **View details**.</span></span>

6.  <span data-ttu-id="42b50-118">En la página **Editar configuración global** , haga clic en la casilla de verificación **Habilitar omisión de medios** .</span><span class="sxs-lookup"><span data-stu-id="42b50-118">On the **Edit Global Setting** page, click the **Enable media bypass** check box.</span></span>

7.  <span data-ttu-id="42b50-119">Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="42b50-119">Select one of the following options:</span></span>
    
      - <span data-ttu-id="42b50-120">**Omitir siempre**   Seleccione esta opción para intentar la omisión de medios en todas las llamadas.</span><span class="sxs-lookup"><span data-stu-id="42b50-120">**Always bypass**   Select this option to attempt media bypass on all calls.</span></span> <span data-ttu-id="42b50-121">Esta opción no estará disponible si el control de admisión de llamada (CAC) está habilitado.</span><span class="sxs-lookup"><span data-stu-id="42b50-121">This option will be unavailable if call admission control (CAC) is enabled.</span></span> <span data-ttu-id="42b50-122">Si CAC no está habilitado, seleccione esta opción en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="42b50-122">If CAC is not enabled, select this option in the following situations:</span></span>
        
          - <span data-ttu-id="42b50-123">No es necesario el control del ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="42b50-123">There is no need for bandwidth control.</span></span>
        
          - <span data-ttu-id="42b50-124">No es necesario que la configuración específica determine Cuándo debe pasar el bypass.</span><span class="sxs-lookup"><span data-stu-id="42b50-124">There is no need for fine-grained configuration to determine when bypass should happen.</span></span>
        
          - <span data-ttu-id="42b50-125">Hay conectividad completa entre las puertas de enlace y los clientes.</span><span class="sxs-lookup"><span data-stu-id="42b50-125">There is full connectivity between gateways and clients.</span></span>
    
      - <span data-ttu-id="42b50-126">**Usar configuración de sitios y regiones**   Si CAC está habilitado, esta opción está seleccionada de forma predeterminada y no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="42b50-126">**Use sites and region configuration**   If CAC is enabled, this option is selected by default and cannot be changed.</span></span> <span data-ttu-id="42b50-127">Cuando esta opción está seleccionada, se usarán regiones y sitios de configuración de red para determinar cuándo es posible la omisión de medios.</span><span class="sxs-lookup"><span data-stu-id="42b50-127">When this option is selected, network configuration sites and regions will be used to determine when media bypass is possible.</span></span> <span data-ttu-id="42b50-128">Si selecciona esta opción, puede habilitar el omisión de sitios que no están asignados.</span><span class="sxs-lookup"><span data-stu-id="42b50-128">If you select this option, you can choose to enable bypass for sites that are not mapped.</span></span> <span data-ttu-id="42b50-129">Haga clic en la casilla **de verificación Habilitar el omisión de sitios no asignados** solo si tiene uno o varios sitios grandes asociados a la misma región que no tienen restricciones de ancho de banda (por ejemplo, un sitio central grande) y también tiene algunos sitios de rama asociados a la misma región que tienen restricciones de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="42b50-129">Click the **Enable bypass for non-mapped sites** check box only if you have one or more large sites associated with the same region that do not have bandwidth constraints (for example, a large central site) and you also have some branch sites associated with the same region that do have bandwidth constraints.</span></span> <span data-ttu-id="42b50-130">Cuando habilita el bypass para sitios no asignados, la configuración se simplifica porque especifica solo las subredes asociadas a las sucursales en lugar de tener que especificar todas las subredes asociadas a todos los sitios.</span><span class="sxs-lookup"><span data-stu-id="42b50-130">When you enable bypass for non-mapped sites, configuration is streamlined because you specify only the subnets associated with the branch sites rather than needing to specify all subnets associated with all sites.</span></span> <span data-ttu-id="42b50-131">Le recomendamos que no active la casilla **Habilitar omisión para sitios no asignados** si CAC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="42b50-131">We recommend that you do not select the **Enable bypass for non-mapped sites** check box if CAC is enabled.</span></span>

8.  <span data-ttu-id="42b50-132">Haga clic en **confirmar** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="42b50-132">Click **Commit** to save your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="42b50-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="42b50-133">See Also</span></span>


[<span data-ttu-id="42b50-134">Deshabilitar la omisión de medios de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42b50-134">Disabling network media bypass in Lync Server 2013</span></span>](lync-server-2013-disabling-network-media-bypass.md)  


[<span data-ttu-id="42b50-135">Opciones de omisión de multimedia global en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42b50-135">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  


[<span data-ttu-id="42b50-136">Planificar la omisión de medios en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42b50-136">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="42b50-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42b50-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

