---
title: 'Lync Server 2013: eliminar una directiva de conferencia existente'
description: 'Lync Server 2013: eliminar una directiva de conferencia existente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing conferencing policy
ms:assetid: 709ed771-790f-4bf1-a4de-b37ca5168688
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688089(v=OCS.15)
ms:contentKeyID: 49733688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b64e51acc6e6dc91b938244da28057b01957069
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430507"
---
# <a name="delete-an-existing-conferencing-policy-in-lync-server-2013"></a><span data-ttu-id="5604c-103">Eliminar una directiva de conferencia existente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5604c-103">Delete an existing conferencing policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5604c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5604c-104">

<span> </span></span></span>

<span data-ttu-id="5604c-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="5604c-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="5604c-106">Siga estos pasos para eliminar una directiva de conferencia de nivel de usuario o de sitio.</span><span class="sxs-lookup"><span data-stu-id="5604c-106">Follow these steps to delete a user-level or a site-level conferencing policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5604c-107">No puede eliminar la Directiva de conferencia global.</span><span class="sxs-lookup"><span data-stu-id="5604c-107">You cannot delete the global conferencing policy.</span></span>



</div>

<div>

## <a name="to-delete-a-site-or-user-conferencing-policy"></a><span data-ttu-id="5604c-108">Para eliminar un sitio o una directiva de conferencia de usuario</span><span class="sxs-lookup"><span data-stu-id="5604c-108">To delete a site or user conferencing policy</span></span>

1.  <span data-ttu-id="5604c-109">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="5604c-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5604c-110">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5604c-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5604c-111">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5604c-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5604c-112">En la barra de navegación izquierda, haga clic en **Conferencia** y, a continuación, en **Directiva de conferencia**.</span><span class="sxs-lookup"><span data-stu-id="5604c-112">In the left navigation bar, click **Conferencing** and then click **Conferencing Policy**.</span></span>

4.  <span data-ttu-id="5604c-113">En la lista de directivas de conferencia, haga clic en la directiva de usuario o en el sitio que desea eliminar, haga clic en **Editar** y, después, en **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="5604c-113">In the list of conferencing policies, click the site or user policy that you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-conferencing-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="5604c-114">Quitar directivas de conferencia con cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5604c-114">Removing Conferencing Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="5604c-115">Puede eliminar directivas de conferencia con el shell de administración de Lync Server y el cmdlet **Remove-CsConferencingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="5604c-115">You can delete conferencing policies by using Lync Server Management Shell and the **Remove-CsConferencingPolicy** cmdlet.</span></span> <span data-ttu-id="5604c-116">Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5604c-116">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="5604c-117">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="5604c-117">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-conferencing-policy"></a><span data-ttu-id="5604c-118">Para quitar una directiva de conferencia especificada</span><span class="sxs-lookup"><span data-stu-id="5604c-118">To remove a specified conferencing policy</span></span>

  - <span data-ttu-id="5604c-119">El comando siguiente quita la directiva de conferencia con el valor de identidad RedmondConferencingPolicy:</span><span class="sxs-lookup"><span data-stu-id="5604c-119">The following command removes the conferencing policy with the Identity RedmondConferencingPolicy:</span></span>
    
        Remove-CsConferencingPolicy -Identity "RedmondConferencingPolicy"

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-policies-applied-to-the-per-user-scope"></a><span data-ttu-id="5604c-120">Para quitar todas las directivas de conferencia que se aplican al ámbito de cada usuario</span><span class="sxs-lookup"><span data-stu-id="5604c-120">To remove all of the conferencing policies applied to the per-user scope</span></span>

  - <span data-ttu-id="5604c-121">El siguiente comando quita todas las directivas de conferencia configuradas en el ámbito de cada usuario:</span><span class="sxs-lookup"><span data-stu-id="5604c-121">The following command removes all the conferencing policies configured at the per-user scope:</span></span>
    
        Get-CsConferencingPolicy -Filter "tag:*" | Remove-CsConferencingPolicy

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-polices-that-allow-recording-by-external-users"></a><span data-ttu-id="5604c-122">Para quitar todas las directivas de conferencia que permiten la grabación de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="5604c-122">To remove all of the conferencing polices that allow recording by external users</span></span>

  - <span data-ttu-id="5604c-123">El siguiente comando elimina las directivas de conferencia que permiten a los usuarios externos grabar la Conferencia:</span><span class="sxs-lookup"><span data-stu-id="5604c-123">The following command deletes any conferencing policies that allow external users to record the conference:</span></span>
    
        Get-CsConferencingPolicy | Where-Object {$_.AllowExternalUsersToRecordMeetings -eq $True} | Remove-CsConferencingPolicy

</div>

<span data-ttu-id="5604c-124">Para obtener más información, consulte [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy).</span><span class="sxs-lookup"><span data-stu-id="5604c-124">For details, see [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy).</span></span>

<span data-ttu-id="5604c-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5604c-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

