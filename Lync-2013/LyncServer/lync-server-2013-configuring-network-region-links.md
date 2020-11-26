---
title: 'Lync Server 2013: configuración de vínculos de región de red'
description: 'Lync Server 2013: configuración de vínculos de región de red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring network region links
ms:assetid: 952bc93e-e6aa-4539-85c7-2b15f14eb382
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182551(v=OCS.15)
ms:contentKeyID: 48184829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b92593f3b8fcd5fe3307a9c193ed7cddcf6dfce0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432929"
---
# <a name="configuring-network-region-links-in-lync-server-2013"></a><span data-ttu-id="79bef-103">Configuración de vínculos de regiones de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79bef-103">Configuring network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79bef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79bef-104">

<span> </span></span></span>

<span data-ttu-id="79bef-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="79bef-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="79bef-106">Puede configurar vínculos entre dos regiones de red como parte de control de admisión de llamadas (CAC).</span><span class="sxs-lookup"><span data-stu-id="79bef-106">You can configure links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="79bef-107">Las regiones dentro de una red están vinculadas a través de la conectividad de red de área extensa (WAN).</span><span class="sxs-lookup"><span data-stu-id="79bef-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="79bef-108">Puede usar el panel de control de Lync Server para definir un vínculo entre dos regiones de red y establecer las limitaciones de ancho de banda en las conexiones de audio y vídeo entre estas regiones.</span><span class="sxs-lookup"><span data-stu-id="79bef-108">You can use the Lync Server Control Panel to define a link between two network regions and set the bandwidth limitations on audio and video connections between these regions.</span></span> <span data-ttu-id="79bef-109">Para más información sobre cómo eliminar un vínculo de región de red existente, vea [eliminar vínculos de región de red en Lync Server 2013](lync-server-2013-deleting-network-region-links.md).</span><span class="sxs-lookup"><span data-stu-id="79bef-109">For details about deleting an existing network region link, see [Deleting network region links in Lync Server 2013](lync-server-2013-deleting-network-region-links.md).</span></span>

<div>

## <a name="to-create-a-network-region-link"></a><span data-ttu-id="79bef-110">Para crear un vínculo a región de red</span><span class="sxs-lookup"><span data-stu-id="79bef-110">To create a network region link</span></span>

1.  <span data-ttu-id="79bef-111">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="79bef-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="79bef-112">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="79bef-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="79bef-113">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="79bef-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="79bef-114">En la barra de navegación izquierda, haga clic en **configuración de red** y, a continuación, en **vínculo de región**.</span><span class="sxs-lookup"><span data-stu-id="79bef-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="79bef-115">En la página vínculo de la **región** , haga clic en **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="79bef-115">On the **Region Link** page, click **New**.</span></span>

5.  <span data-ttu-id="79bef-116">En el **vínculo nueva región**, escriba un valor en el campo **nombre** .</span><span class="sxs-lookup"><span data-stu-id="79bef-116">In **New Region Link**, type a value in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="79bef-117">Este valor debe ser único dentro de la implementación de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="79bef-117">This value must be unique within your Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="79bef-118">En la lista desplegable **región de red \# 1** , seleccione una de las dos regiones para vincular.</span><span class="sxs-lookup"><span data-stu-id="79bef-118">From the **Network region \#1** drop-down list, select one of the two regions to be linked.</span></span>

7.  <span data-ttu-id="79bef-119">En la lista desplegable **región de red \# 2** , seleccione la otra región que desea vincular.</span><span class="sxs-lookup"><span data-stu-id="79bef-119">From the **Network region \#2** drop-down list, select the other region to be linked.</span></span> <span data-ttu-id="79bef-120">Esta región debe ser diferente de la región seleccionada para la región de red \# 1.</span><span class="sxs-lookup"><span data-stu-id="79bef-120">This region must be different from the region selected for Network region \#1.</span></span>

8.  <span data-ttu-id="79bef-121">Faculta Si desea colocar limitaciones de ancho de banda en las llamadas de audio o vídeo entre estas regiones, seleccione un perfil de directiva de ancho de banda en la lista desplegable **Directiva de ancho de banda** .</span><span class="sxs-lookup"><span data-stu-id="79bef-121">(Optional) If you want to place bandwidth limitations on audio or video calls between these regions, select a bandwidth policy profile from the **Bandwidth policy** drop-down list.</span></span>

9.  <span data-ttu-id="79bef-122">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="79bef-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-region-link"></a><span data-ttu-id="79bef-123">Para modificar un vínculo de región de red</span><span class="sxs-lookup"><span data-stu-id="79bef-123">To modify a network region link</span></span>

1.  <span data-ttu-id="79bef-124">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="79bef-124">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="79bef-125">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="79bef-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="79bef-126">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="79bef-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="79bef-127">En la barra de navegación izquierda, haga clic en **configuración de red** y, a continuación, en **vínculo de región**.</span><span class="sxs-lookup"><span data-stu-id="79bef-127">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="79bef-128">En la página vínculo de la **región** , haga clic en el vínculo de la región que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="79bef-128">On the **Region Link** page, click the region link that you want to modify.</span></span>

5.  <span data-ttu-id="79bef-129">En el menú **Editar**, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="79bef-129">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="79bef-130">En el **vínculo editar región**, puede modificar las regiones vinculadas o el perfil de directiva de ancho de banda para este vínculo.</span><span class="sxs-lookup"><span data-stu-id="79bef-130">In **Edit Region Link**, you can modify the regions that are linked or the bandwidth policy profile for this link.</span></span>

7.  <span data-ttu-id="79bef-131">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="79bef-131">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="79bef-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="79bef-132">See Also</span></span>


[<span data-ttu-id="79bef-133">Eliminar vínculos de regiones de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79bef-133">Deleting network region links in Lync Server 2013</span></span>](lync-server-2013-deleting-network-region-links.md)  


[<span data-ttu-id="79bef-134">New-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="79bef-134">New-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegionLink)  
[<span data-ttu-id="79bef-135">Set-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="79bef-135">Set-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegionLink)  
[<span data-ttu-id="79bef-136">Remove-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="79bef-136">Remove-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegionLink)  
[<span data-ttu-id="79bef-137">Get-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="79bef-137">Get-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)  
  

<span data-ttu-id="79bef-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79bef-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
