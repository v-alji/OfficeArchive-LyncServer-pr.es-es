---
title: 'Lync Server 2013: eliminar subredes de red'
description: 'Lync Server 2013: eliminar subredes de red.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network subnets
ms:assetid: c1850f38-40a3-48c9-b6f1-f181c5e63b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721873(v=OCS.15)
ms:contentKeyID: 49733806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6635ec99b68c4ceb10d1cda343fef35c951bf152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430283"
---
# <a name="deleting-network-subnets-in-lync-server-2013"></a><span data-ttu-id="ff1c4-103">Eliminar subredes de la red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff1c4-103">Deleting network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff1c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff1c4-104">

<span> </span></span></span>

<span data-ttu-id="ff1c4-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ff1c4-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ff1c4-106">Puede usar el procedimiento siguiente para eliminar una subred.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-106">You can use the following procedure to delete a subnet.</span></span> <span data-ttu-id="ff1c4-107">En el panel de control de Lync Server, puede crear, modificar o eliminar una subred de red.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-107">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="ff1c4-108">Para obtener más información sobre cómo crear o modificar subredes de red, consulte [crear o modificar subredes de red en Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="ff1c4-108">For details on creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span></span>

<span data-ttu-id="ff1c4-109">En la mayoría de las implementaciones de Microsoft Lync Server 2013 donde se implementa control de admisión de llamadas (CAC), generalmente habrá un gran número de subredes.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-109">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="ff1c4-110">Por ello, suele ser mejor configurar las subredes desde el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-110">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="ff1c4-111">Desde allí puedes llamar a **New-CsNetworkSubnet** junto con el cmdlet **Import-CSV** de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-111">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="ff1c4-112">Al usar estos cmdlets juntos, puede leer la configuración de la subred de un archivo de valores separados por comas (. csv) y crear varias subredes al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-112">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="ff1c4-113">Para obtener ejemplos de cómo crear subredes a partir de un archivo. csv, consulte [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="ff1c4-113">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-delete-a-network-subnet"></a><span data-ttu-id="ff1c4-114">Para eliminar una subred de red</span><span class="sxs-lookup"><span data-stu-id="ff1c4-114">To delete a network subnet</span></span>

1.  <span data-ttu-id="ff1c4-115">Desde una cuenta de usuario que sea miembro del grupo RTCUniversalServerAdmins (o que tenga derechos de usuario equivalentes), o esté asignada al rol CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ff1c4-116">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ff1c4-117">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ff1c4-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ff1c4-118">En la barra de navegación izquierda, haga clic en **configuración de red** y, después, en **subred**.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-118">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="ff1c4-119">En la página **subred** , haga clic en la subred que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-119">On the **Subnet** page, click the subnet that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ff1c4-120">Puede eliminar más de una subred a la vez.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-120">You can delete more than one subnet at a time.</span></span> <span data-ttu-id="ff1c4-121">Para ello, presione CTRL y seleccione varias subredes mientras mantiene presionada la tecla CTRL.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-121">To do this, press CTRL and select multiple subnets while holding down the CTRL key.</span></span> <span data-ttu-id="ff1c4-122">O bien, para seleccionar todas las subredes, haga clic en <STRONG>seleccionar todo</STRONG> en el menú <STRONG>edición</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ff1c4-122">Or, to select all subnets, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="ff1c4-123">En el menú **Editar** , haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="ff1c4-124">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ff1c4-124">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ff1c4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff1c4-125">See Also</span></span>


[<span data-ttu-id="ff1c4-126">Crear o modificar subredes de red en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff1c4-126">Create or modify network subnets in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-network-subnets.md)  
  

<span data-ttu-id="ff1c4-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff1c4-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

