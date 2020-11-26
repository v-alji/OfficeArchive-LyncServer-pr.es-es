---
title: 'Lync Server 2013: crear o modificar subredes de red'
description: 'Lync Server 2013: crear o modificar subredes de red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify network subnets
ms:assetid: 1ba8c4e3-fbc7-4758-88ac-d651fef17bed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520957(v=OCS.15)
ms:contentKeyID: 48183548
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37695707bf39b10c351a4990b132c9799406f9c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431655"
---
# <a name="create-or-modify-network-subnets-in-lync-server-2013"></a><span data-ttu-id="33075-103">Crear o modificar subredes de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33075-103">Create or modify network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="33075-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="33075-104">

<span> </span></span></span>

<span data-ttu-id="33075-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="33075-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="33075-106">Una subred de red debe estar asociada a un sitio de red para determinar la ubicación geográfica del host que pertenece a esta subred.</span><span class="sxs-lookup"><span data-stu-id="33075-106">A network subnet must be associated with a network site for the purposes of determining the geographic location of the host belonging to this subnet.</span></span> <span data-ttu-id="33075-107">Puede usar el panel de control de Lync Server para configurar subredes.</span><span class="sxs-lookup"><span data-stu-id="33075-107">You can use Lync Server Control Panel to configure subnets.</span></span> <span data-ttu-id="33075-108">En el panel de control de Lync Server, puede crear, modificar o eliminar una subred de red.</span><span class="sxs-lookup"><span data-stu-id="33075-108">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="33075-109">Para más información sobre cómo eliminar subredes de red, vea [eliminar subredes de red en Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="33075-109">For details about deleting network subnets, see [Deleting network subnets in Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span></span>

<span data-ttu-id="33075-110">En la mayoría de las implementaciones de Microsoft Lync Server 2013 donde se implementa control de admisión de llamadas (CAC), generalmente habrá un gran número de subredes.</span><span class="sxs-lookup"><span data-stu-id="33075-110">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="33075-111">Por ello, suele ser mejor configurar las subredes desde el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="33075-111">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="33075-112">Desde allí puedes llamar a **New-CsNetworkSubnet** junto con el cmdlet **Import-CSV** de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33075-112">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="33075-113">Al usar estos cmdlets juntos, puede leer la configuración de la subred de un archivo de valores separados por comas (. csv) y crear varias subredes al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="33075-113">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="33075-114">Para obtener ejemplos de cómo crear subredes a partir de un archivo. csv, consulte [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="33075-114">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-create-a-network-subnet"></a><span data-ttu-id="33075-115">Para crear una subred de red</span><span class="sxs-lookup"><span data-stu-id="33075-115">To create a network subnet</span></span>

1.  <span data-ttu-id="33075-116">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="33075-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="33075-117">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="33075-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="33075-118">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="33075-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="33075-119">En la barra de navegación izquierda, haga clic en **configuración de red** y, después, en **subred**.</span><span class="sxs-lookup"><span data-stu-id="33075-119">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="33075-120">En la página **subred** , haga clic en **nueva**.</span><span class="sxs-lookup"><span data-stu-id="33075-120">On the **Subnet** page, click **New**.</span></span>

5.  <span data-ttu-id="33075-121">En **nueva subred**, escriba un valor en el campo **ID de subred** .</span><span class="sxs-lookup"><span data-stu-id="33075-121">In **New Subnet**, enter a value in the **Subnet ID** field.</span></span> <span data-ttu-id="33075-122">Debe ser una dirección IP (por ejemplo, 174.11.12.0) y debe ser la primera dirección del intervalo de direcciones IP definido por la subred.</span><span class="sxs-lookup"><span data-stu-id="33075-122">This must be an IP address (for example, 174.11.12.0), and it must be the first address in the IP address range defined by the subnet.</span></span>

6.  <span data-ttu-id="33075-123">En el campo **máscara** , escriba un valor numérico comprendido entre 1 y 32.</span><span class="sxs-lookup"><span data-stu-id="33075-123">In the **Mask** field, enter a numeric value from 1 through 32.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="33075-124">Este valor es la máscara de red que se aplicará a la subred que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="33075-124">This value is the bitmask that is to be applied to the subnet being created.</span></span>

    
    </div>

7.  <span data-ttu-id="33075-125">En **identificador de sitio de red**, seleccione el sitio al que pertenece esta subred.</span><span class="sxs-lookup"><span data-stu-id="33075-125">In **Network site ID**, select the site to which this subnet belongs.</span></span>

8.  <span data-ttu-id="33075-126">Faculta Escriba un valor en el campo **Descripción** para proporcionar más información sobre esta subred que no puede expresarse solo por el nombre.</span><span class="sxs-lookup"><span data-stu-id="33075-126">(Optional) Type a value in the **Description** field to provide more information about this subnet that cannot be expressed by the name alone.</span></span>

9.  <span data-ttu-id="33075-127">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="33075-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-subnet"></a><span data-ttu-id="33075-128">Para modificar una subred de red</span><span class="sxs-lookup"><span data-stu-id="33075-128">To modify a network subnet</span></span>

1.  <span data-ttu-id="33075-129">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="33075-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="33075-130">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="33075-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="33075-131">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="33075-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="33075-132">En la barra de navegación izquierda, haga clic en **configuración de red** y, después, en **subred**.</span><span class="sxs-lookup"><span data-stu-id="33075-132">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="33075-133">En la página **subred** , haga clic en la subred que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="33075-133">On the **Subnet** page, click the subnet that you want to modify.</span></span>

5.  <span data-ttu-id="33075-134">En el menú **Editar**, haga clic en **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="33075-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="33075-135">En la página **Editar subred** , puede modificar la máscara de máscara, el sitio de red asociado o la descripción.</span><span class="sxs-lookup"><span data-stu-id="33075-135">On the **Edit Subnet** page, you can modify the bitmask, associated network site, or description.</span></span> <span data-ttu-id="33075-136">Si modifica la máscara de subred, tenga en cuenta que el identificador de subred debe ser la primera dirección del intervalo de direcciones IP definido por la subred.</span><span class="sxs-lookup"><span data-stu-id="33075-136">If you modify the bitmask, keep in mind that the Subnet ID must still be the first address in the IP address range defined by the subnet.</span></span>

7.  <span data-ttu-id="33075-137">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="33075-137">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="33075-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="33075-138">See Also</span></span>


[<span data-ttu-id="33075-139">Eliminar subredes de la red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33075-139">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  


[<span data-ttu-id="33075-140">Acerca de las regiones de red, sitios y subredes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33075-140">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)  


[<span data-ttu-id="33075-141">New-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="33075-141">New-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)  
[<span data-ttu-id="33075-142">Set-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="33075-142">Set-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSubnet)  
[<span data-ttu-id="33075-143">Remove-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="33075-143">Remove-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSubnet)  
[<span data-ttu-id="33075-144">Get-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="33075-144">Get-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet)  
  

<span data-ttu-id="33075-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="33075-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

