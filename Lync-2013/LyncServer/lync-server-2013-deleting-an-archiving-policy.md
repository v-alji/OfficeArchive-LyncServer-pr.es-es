---
title: 'Lync Server 2013: eliminar una directiva de archivado'
description: 'Lync Server 2013: eliminar una directiva de archivado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an Archiving policy
ms:assetid: 4739a691-41cc-4128-8bb8-6d5a4c02107a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520989(v=OCS.15)
ms:contentKeyID: 48184043
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ecf465a62cf8f54777b03a1634d9a95f1b565c9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430367"
---
# <a name="deleting-an-archiving-policy-in-lync-server-2013"></a><span data-ttu-id="49d47-103">Eliminar una directiva de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49d47-103">Deleting an Archiving policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49d47-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49d47-104">

<span> </span></span></span>

<span data-ttu-id="49d47-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="49d47-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="49d47-106">Puede eliminar una directiva de usuario o una directiva de sitio.</span><span class="sxs-lookup"><span data-stu-id="49d47-106">You can delete a user policy or site policy.</span></span> <span data-ttu-id="49d47-107">No se puede quitar la directiva global.</span><span class="sxs-lookup"><span data-stu-id="49d47-107">The global policy cannot be removed.</span></span> <span data-ttu-id="49d47-108">Si intenta eliminar la directiva global, Lync Server 2013 restablece automáticamente la Directiva a los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="49d47-108">If you try to delete the global policy, Lync Server 2013 automatically resets the policy to the default values.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49d47-109">Si habilitó la integración de Microsoft Exchange para su implementación, las directivas de Exchange controlan si el archivado está habilitado para los usuarios que están alojados en Exchange 2013 y si sus buzones se ponen en espera In-Place.</span><span class="sxs-lookup"><span data-stu-id="49d47-109">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="49d47-110">Para obtener más información, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configurar directivas para archivar en Lync Server 2013 al usar la integración de Exchange Server</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="49d47-110">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-delete-a-user-or-site-policy-for-archiving"></a><span data-ttu-id="49d47-111">Para eliminar un usuario o una directiva de sitio para archivar</span><span class="sxs-lookup"><span data-stu-id="49d47-111">To delete a user or site policy for archiving</span></span>

1.  <span data-ttu-id="49d47-112">Desde una cuenta de usuario que se asigne al rol CsArchivingAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="49d47-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="49d47-113">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="49d47-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="49d47-114">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="49d47-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="49d47-115">En la barra de navegación izquierda, haga clic en **Supervisión y archivado** y, después, en **Directiva de archivado**.</span><span class="sxs-lookup"><span data-stu-id="49d47-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="49d47-116">En la lista de directivas de archivado, haga clic en la directiva de usuario o sitio que desea eliminar, haga clic en **Editar** y, luego, en **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="49d47-116">In the list of archiving policies, click the user or site policy that you want to delete, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="49d47-117">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="49d47-117">Click **Commit**.</span></span>

</div>

<div>

## <a name="removing-archiving-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="49d47-118">Quitar directivas de archivado mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="49d47-118">Removing Archiving Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="49d47-119">Las directivas de archivado se pueden eliminar mediante Windows PowerShell y el cmdlet **Remove-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="49d47-119">Archiving policies can be deleted by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="49d47-120">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="49d47-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="49d47-121">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="49d47-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-archiving-policy"></a><span data-ttu-id="49d47-122">Para quitar una directiva de archivado especificada</span><span class="sxs-lookup"><span data-stu-id="49d47-122">To remove a specified archiving policy</span></span>

  - <span data-ttu-id="49d47-123">A modo de ejemplo, **Remove-CsArchivingPolicy** elimina la Directiva con el sitio de identidad: Redmond.</span><span class="sxs-lookup"><span data-stu-id="49d47-123">As an example, **Remove-CsArchivingPolicy** deletes the policy with the Identity site:Redmond.</span></span> <span data-ttu-id="49d47-124">Tenga en cuenta que, cuando se elimina una directiva configurada en el ámbito del sitio, los usuarios administrados previamente por la Directiva del sitio se regirán automáticamente por la Directiva de archivado global.</span><span class="sxs-lookup"><span data-stu-id="49d47-124">Note that, when a policy configured at the site scope is deleted, users previously managed by the site policy will automatically be governed by the global archiving policy instead.</span></span> <span data-ttu-id="49d47-125">El siguiente comando quita el archivado aplicado al sitio de Redmond:</span><span class="sxs-lookup"><span data-stu-id="49d47-125">The following command removes the archiving applied to the Redmond site:</span></span>
    
        Remove-CsArchivingPolicy -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-applied-to-the-per-user-scope"></a><span data-ttu-id="49d47-126">Para quitar todas las directivas de archivado aplicadas al ámbito de cada usuario</span><span class="sxs-lookup"><span data-stu-id="49d47-126">To remove all the archiving policies applied to the per-user scope</span></span>

  - <span data-ttu-id="49d47-127">Este comando quita todas las directivas de archivado aplicadas al ámbito de cada usuario:</span><span class="sxs-lookup"><span data-stu-id="49d47-127">This command removes all the archiving policies applied to the per-user scope:</span></span>
    
        Get-CsArchivingPolicy -Filter "tag:*" | Remove-CsArchivingPolicy

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-that-disable-internal-archiving"></a><span data-ttu-id="49d47-128">Para quitar todas las directivas de archivado que deshabilitan el archivado interno</span><span class="sxs-lookup"><span data-stu-id="49d47-128">To remove all the archiving policies that disable internal archiving</span></span>

  - <span data-ttu-id="49d47-129">Este comando quita todas las directivas de archivado donde se deshabilitó el archivado interno:</span><span class="sxs-lookup"><span data-stu-id="49d47-129">This command removes all the archiving policies where internal archiving has been disabled:</span></span>
    
        Get-CsArchivingPolicy | Where-Object {$_.ArchiveInternal -eq $False} | Remove-CsArchivingPolicy

</div>

<span data-ttu-id="49d47-130">Para obtener más información, consulte el tema de ayuda para el cmdlet [Remove-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="49d47-130">For more information, see the help topic for the [Remove-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="49d47-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="49d47-131">See Also</span></span>


[<span data-ttu-id="49d47-132">Administrar el archivado de comunicaciones internas y externas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49d47-132">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="49d47-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49d47-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

