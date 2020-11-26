---
title: 'Lync Server 2013: eliminar un grupo de agentes'
description: 'Lync Server 2013: eliminar un grupo de agentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an agent group
ms:assetid: df385fd1-62f4-42b7-a349-4eb38dea50c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182597(v=OCS.15)
ms:contentKeyID: 48185670
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dded2db0957e37a624d7e8bf3a06e102f8d35cad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430647"
---
# <a name="delete-an-agent-group-in-lync-server-2013"></a><span data-ttu-id="e2b46-103">Eliminar un grupo de agentes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2b46-103">Delete an agent group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e2b46-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e2b46-104">

<span> </span></span></span>

<span data-ttu-id="e2b46-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="e2b46-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="e2b46-106">Use uno de los procedimientos siguientes para eliminar un grupo de agentes.</span><span class="sxs-lookup"><span data-stu-id="e2b46-106">Use one of the following procedures to delete an agent group.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-an-agent-group"></a><span data-ttu-id="e2b46-107">Para usar el panel de control de Lync Server para eliminar un grupo de agentes</span><span class="sxs-lookup"><span data-stu-id="e2b46-107">To use Lync Server Control Panel to delete an agent group</span></span>

1.  <span data-ttu-id="e2b46-108">Inicie sesión como miembro del grupo RTCUniversalServerAdmins o como miembro de uno de los roles administrativos predefinidos que admiten el Grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2b46-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="e2b46-109">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e2b46-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e2b46-110">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e2b46-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e2b46-111">En la barra de navegación izquierda, haga clic en **Grupos de respuesta** y, a continuación, haga clic en **Grupo**.</span><span class="sxs-lookup"><span data-stu-id="e2b46-111">In the left navigation bar, click **Response Groups**, and then click **Group**.</span></span>

4.  <span data-ttu-id="e2b46-112">En la página **grupos de respuesta** , escriba todo o parte del nombre del grupo de agentes que desea eliminar en el campo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e2b46-112">On the **Response Groups** page, type all or part of the name of the agent group that you want to delete in the search field.</span></span>

5.  <span data-ttu-id="e2b46-113">En la lista resultante, haga clic en el grupo que desea eliminar, haga clic en **Editar** y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="e2b46-113">In the resulting list, click the group that you want to delete, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="e2b46-114">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e2b46-114">Click **OK**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-an-agent-group"></a><span data-ttu-id="e2b46-115">Para usar Windows PowerShell para eliminar un grupo de agentes</span><span class="sxs-lookup"><span data-stu-id="e2b46-115">To use Windows PowerShell to delete an agent group</span></span>

1.  <span data-ttu-id="e2b46-116">Inicie sesión como miembro del grupo RTCUniversalServerAdmins o como miembro de uno de los roles administrativos predefinidos que admiten el Grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2b46-116">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="e2b46-117">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e2b46-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e2b46-118">En la línea de comandos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="e2b46-118">At the command line, run:</span></span>
    
        Get-CsRgsAgentGroup -Identity <Application Server service> -Name "<name of agent group>" | Remove-CsRgsAgentGroup
    
    <span data-ttu-id="e2b46-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e2b46-119">For example:</span></span>
    
        Get-CsRgsAgentGroup -Identity service:ApplicationServer:redmond.contoso.com -Name "Human Resources" | Remove-CsRgsAgentGroup

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e2b46-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2b46-120">See Also</span></span>


[<span data-ttu-id="e2b46-121">Crear o modificar un grupo de agentes en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2b46-121">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  


[<span data-ttu-id="e2b46-122">Remove-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="e2b46-122">Remove-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsRgsAgentGroup)  
[<span data-ttu-id="e2b46-123">Get-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="e2b46-123">Get-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsAgentGroup)  
  

<span data-ttu-id="e2b46-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e2b46-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

