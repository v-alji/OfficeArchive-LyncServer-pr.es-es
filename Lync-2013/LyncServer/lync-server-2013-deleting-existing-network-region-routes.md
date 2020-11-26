---
title: 'Lync Server 2013: eliminar rutas de región de red existentes'
description: 'Lync Server 2013: eliminar rutas de región de red existentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network region routes
ms:assetid: 6256ff80-5f1e-48b4-928b-24aeb3c1a0e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688074(v=OCS.15)
ms:contentKeyID: 49733669
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c2501dc3f4ed88a56e9f591e3af11a673046280a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430339"
---
# <a name="deleting-existing-network-region-routes-in-lync-server-2013"></a><span data-ttu-id="9aff3-103">Eliminar las rutas de la región de red existente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aff3-103">Deleting existing network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9aff3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9aff3-104">

<span> </span></span></span>

<span data-ttu-id="9aff3-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9aff3-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9aff3-106">Cada región dentro de una configuración de control de admisión de llamadas (CAC) debe tener alguna forma de tener acceso a todas las demás regiones.</span><span class="sxs-lookup"><span data-stu-id="9aff3-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="9aff3-107">Aunque los vínculos de región establecen limitaciones de ancho de banda en las conexiones entre las regiones y también representan los vínculos físicos, una ruta determina qué ruta de acceso vinculada pasará la conexión de una región a otra.</span><span class="sxs-lookup"><span data-stu-id="9aff3-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="9aff3-108">Puede usar el panel de control de Lync Server para configurar las rutas de la región de red.</span><span class="sxs-lookup"><span data-stu-id="9aff3-108">You can use Lync Server Control Panel to configure network region routes.</span></span> <span data-ttu-id="9aff3-109">En el panel de control de Lync Server, puede crear, modificar o eliminar una ruta de región de red.</span><span class="sxs-lookup"><span data-stu-id="9aff3-109">From Lync Server Control Panel, you can create, modify, or delete a network region route.</span></span> <span data-ttu-id="9aff3-110">Use este tema para eliminar las rutas de la región de red existentes.</span><span class="sxs-lookup"><span data-stu-id="9aff3-110">Use this topic to delete existing network region routes.</span></span> <span data-ttu-id="9aff3-111">Para obtener detalles sobre cómo crear o modificar rutas de regiones de red, vea [crear o modificar rutas de región de red en Lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span><span class="sxs-lookup"><span data-stu-id="9aff3-111">For details about creating or modifying network region routes, see [Creating or modifying network region routes in Lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span></span>

<div>

## <a name="to-delete-a-network-region-route"></a><span data-ttu-id="9aff3-112">Para eliminar una ruta de región de red</span><span class="sxs-lookup"><span data-stu-id="9aff3-112">To delete a network region route</span></span>

1.  <span data-ttu-id="9aff3-113">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="9aff3-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9aff3-114">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9aff3-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9aff3-115">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9aff3-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9aff3-116">En la barra de navegación izquierda, haga clic en **configuración de red** y luego en **ruta de región**.</span><span class="sxs-lookup"><span data-stu-id="9aff3-116">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="9aff3-117">En la página Ruta de la **región** , haga clic en la ruta de la región que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="9aff3-117">On the **Region Route** page, click the region route that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9aff3-118">Puede eliminar más de una ruta de región a la vez.</span><span class="sxs-lookup"><span data-stu-id="9aff3-118">You can delete more than one region route at a time.</span></span> <span data-ttu-id="9aff3-119">Para ello, presione CTRL y seleccione varias rutas de región mientras mantiene presionada la tecla CTRL.</span><span class="sxs-lookup"><span data-stu-id="9aff3-119">To do this, press CTRL and select multiple region routes while holding down the CTRL key.</span></span> <span data-ttu-id="9aff3-120">O bien, para seleccionar todas las rutas de la región, haga clic en <STRONG>seleccionar todo</STRONG> en el menú <STRONG>edición</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="9aff3-120">Or, to select all region routes, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="9aff3-121">En el menú **Editar** , haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="9aff3-121">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="9aff3-122">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9aff3-122">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9aff3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aff3-123">See Also</span></span>


[<span data-ttu-id="9aff3-124">Crear o modificar rutas de región de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aff3-124">Creating or modifying network region routes in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-region-routes.md)  


<span data-ttu-id="9aff3-125">[Configurar una ruta de región de red](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="9aff3-125">[Configure a Network Region Route](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span></span>  


[<span data-ttu-id="9aff3-126">New-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="9aff3-126">New-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterRegionRoute)  
[<span data-ttu-id="9aff3-127">Set-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="9aff3-127">Set-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterRegionRoute)  
[<span data-ttu-id="9aff3-128">Remove-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="9aff3-128">Remove-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterRegionRoute)  
[<span data-ttu-id="9aff3-129">Get-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="9aff3-129">Get-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterRegionRoute)  
  

<span data-ttu-id="9aff3-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9aff3-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

