---
title: 'Lync Server 2013: eliminar un intervalo de números sin asignar'
description: 'Lync Server 2013: eliminar un intervalo de números sin asignar.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an unassigned number range
ms:assetid: a8141bfb-b94d-4d0f-a7a9-2e60d10b103a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182565(v=OCS.15)
ms:contentKeyID: 48185090
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 977cae1432c43a7df33e26597efdb364a7fbea08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430493"
---
# <a name="delete-an-unassigned-number-range-in-lync-server-2013"></a><span data-ttu-id="3826c-103">Eliminar un intervalo numérico sin asignar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3826c-103">Delete an unassigned number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3826c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3826c-104">

<span> </span></span></span>

<span data-ttu-id="3826c-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="3826c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="3826c-106">Use uno de los procedimientos siguientes para eliminar un intervalo de números sin asignar para los anuncios.</span><span class="sxs-lookup"><span data-stu-id="3826c-106">Use one of the following procedures to delete an unassigned number range for Announcements.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-an-unassigned-number-range"></a><span data-ttu-id="3826c-107">Para usar el panel de control de Lync Server para eliminar un intervalo de números sin asignar</span><span class="sxs-lookup"><span data-stu-id="3826c-107">To use Lync Server Control Panel to delete an unassigned number range</span></span>

1.  <span data-ttu-id="3826c-108">Inicie sesión en el equipo como miembro del grupo RTCUniversalServerAdmins o como miembro del rol CsVoiceAdministrator, CsServerAdministrator o CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="3826c-108">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="3826c-109">Para obtener más información, consulte [permisos de configuración de delegación en Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="3826c-109">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="3826c-110">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3826c-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3826c-111">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3826c-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3826c-112">En la barra de navegación izquierda, haga clic en **Características de voz** y, a continuación, en **Número sin asignar**.</span><span class="sxs-lookup"><span data-stu-id="3826c-112">In the left navigation bar, click **Voice Features** and then click **Unassigned Number**.</span></span>

4.  <span data-ttu-id="3826c-113">En la página **Número sin asignar**, en el campo de búsqueda, escriba la totalidad o parte del nombre del intervalo del número sin asignar que desee eliminar.</span><span class="sxs-lookup"><span data-stu-id="3826c-113">On the **Unassigned Number** page, in the search field, type all or part of the name of the unassigned number range you want to delete.</span></span>

5.  <span data-ttu-id="3826c-114">En la lista resultante de intervalos numéricos, haga clic en el nombre, en **Editar** y, a continuación, en **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="3826c-114">In the resulting list of number ranges, click the name, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="3826c-115">Haga clic en **Confirmar todo**.</span><span class="sxs-lookup"><span data-stu-id="3826c-115">Click **Commit all**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-an-unassigned-number-range"></a><span data-ttu-id="3826c-116">Para usar Windows PowerShell para eliminar un intervalo de números no asignado</span><span class="sxs-lookup"><span data-stu-id="3826c-116">To use Windows PowerShell to delete an unassigned number range</span></span>

1.  <span data-ttu-id="3826c-117">Inicie sesión en el equipo donde está instalado el shell de administración de Lync Server como miembro del grupo RTCUniversalServerAdmins o con los derechos de usuario necesarios, tal y como se describe en [permisos de configuración de delegado en Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="3826c-117">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="3826c-118">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="3826c-118">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="3826c-119">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3826c-119">At the command line, type:</span></span>
    
        Remove-CsUnassignedNumber -Identity "<name of unassigned number range>" 
    
    <span data-ttu-id="3826c-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3826c-120">For example:</span></span>
    
        Remove-CsUnassignedNumber -Identity "Unassigned range 1"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3826c-121">Para obtener más información sobre más opciones, consulte <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span><span class="sxs-lookup"><span data-stu-id="3826c-121">For details about more options, see <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3826c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="3826c-122">See Also</span></span>


[<span data-ttu-id="3826c-123">Crear o modificar un intervalo numérico sin asignar en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3826c-123">Create or modify an unassigned number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-unassigned-number-range.md)  


[<span data-ttu-id="3826c-124">Remove-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="3826c-124">Remove-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsUnassignedNumber)  
[<span data-ttu-id="3826c-125">Get-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="3826c-125">Get-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUnassignedNumber)  
  

<span data-ttu-id="3826c-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3826c-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

