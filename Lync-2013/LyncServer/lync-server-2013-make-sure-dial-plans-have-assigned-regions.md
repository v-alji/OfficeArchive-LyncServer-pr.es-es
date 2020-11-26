---
title: 'Lync Server 2013: Asegurarse de que los planes de marcado tienen regiones asignadas'
description: 'Lync Server 2013: Asegúrese de que los planes de marcado tienen regiones asignadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Make sure dial plans have assigned regions
ms:assetid: 3da3a907-0dbf-4440-b12f-370f94dd4c17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425903(v=OCS.15)
ms:contentKeyID: 48183937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c055eda221bc03de449631ba38483165a8621773
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426154"
---
# <a name="make-sure-dial-plans-lync-server-2013-have-assigned-regions"></a><span data-ttu-id="ac00f-103">Asegúrese de que los planes de marcado de Lync Server 2013 tienen regiones asignadas</span><span class="sxs-lookup"><span data-stu-id="ac00f-103">Make sure dial plans Lync Server 2013 have assigned regions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac00f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac00f-104">

<span> </span></span></span>

<span data-ttu-id="ac00f-105">_**Última modificación del tema:** 2010-11-02_</span><span class="sxs-lookup"><span data-stu-id="ac00f-105">_**Topic Last Modified:** 2010-11-02_</span></span>

<span data-ttu-id="ac00f-106">Los planes de marcado que se usan para las conferencias de acceso telefónico local necesitan tener una **región de conferencia de acceso telefónico local** especificada para asociar los números de acceso de las conferencias de acceso telefónico local con el plan de marcado adecuado.</span><span class="sxs-lookup"><span data-stu-id="ac00f-106">Dial plans that are used for dial-in conferencing need to have a **Dial-in conferencing region** specified to associate dial-in conferencing access numbers with the appropriate dial plan.</span></span> <span data-ttu-id="ac00f-107">Al configurar un plan de marcado, especifica la región de conferencia de acceso telefónico local que se aplica a ese plan de marcado.</span><span class="sxs-lookup"><span data-stu-id="ac00f-107">When you set up a dial plan, you specify the dial-in conferencing region that applies to that dial plan.</span></span> <span data-ttu-id="ac00f-108">Después, cuando cree el número de acceso telefónico local, seleccione las regiones que asocian el número de acceso con los planes de marcado adecuados.</span><span class="sxs-lookup"><span data-stu-id="ac00f-108">Then, when you create the dial-in access number, you select the regions that associate the access number with the appropriate dial plans.</span></span>

<span data-ttu-id="ac00f-109">Como es importante especificar una región para todos los planes de marcado, le recomendamos que use este procedimiento para comprobar que todos los planes de marcado tienen regiones.</span><span class="sxs-lookup"><span data-stu-id="ac00f-109">Because it important to specify a region for all dial plans, we recommend that you use this procedure to verify that all dial plans have regions.</span></span> <span data-ttu-id="ac00f-110">Este paso es opcional.</span><span class="sxs-lookup"><span data-stu-id="ac00f-110">This step is optional.</span></span>

<span data-ttu-id="ac00f-111">Use el cmdlet **Get-CsDialPlan** para comprobar si la región está configurada para todos los planes de marcado de conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="ac00f-111">Use the **Get-CsDialPlan** cmdlet to verify whether the region is set for all dial-in conferencing dial plans.</span></span> <span data-ttu-id="ac00f-112">Si a los planes de marcado les falta la región, puede usar el cmdlet **Set-CsDialPlan** para establecer la región.</span><span class="sxs-lookup"><span data-stu-id="ac00f-112">If the region is missing from dial plans, you can use the **Set-CsDialPlan** cmdlet to set the region.</span></span> <span data-ttu-id="ac00f-113">También puede usar el panel de control de Lync Server para actualizar la región en los planes de marcado existentes.</span><span class="sxs-lookup"><span data-stu-id="ac00f-113">You can also use Lync Server Control Panel to update the region in existing dial plans.</span></span> <span data-ttu-id="ac00f-114">Para obtener más información sobre el uso del panel de control de Lync Server, vea [modificar un plan de marcado en Lync server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="ac00f-114">For details about using Lync Server Control Panel, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

<div>

## <a name="to-verify-whether-dial-plans-have-the-region-property-set"></a><span data-ttu-id="ac00f-115">Para comprobar si se ha establecido la propiedad Región en los planes de marcado</span><span class="sxs-lookup"><span data-stu-id="ac00f-115">To verify whether dial plans have the region property set</span></span>

1.  <span data-ttu-id="ac00f-116">Inicie sesión en el equipo como miembro del grupo RTCUniversalServerAdmins o como miembro del rol **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** o **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="ac00f-116">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="ac00f-117">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="ac00f-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ac00f-118">Ejecute los siguientes comandos en símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="ac00f-118">Run the following at the command prompt:</span></span>
    
        Get-CsDialPlan [-Identity <Identifier of the dial plans to be retrieved>]
    
    <span data-ttu-id="ac00f-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ac00f-119">For example:</span></span>
    
        Get-CsDialPlan
    
    <span data-ttu-id="ac00f-120">En este ejemplo, se devuelven todos los planes de marcado configurados para la organización.</span><span class="sxs-lookup"><span data-stu-id="ac00f-120">In this example, all the dial plans configured for your organization are returned.</span></span>

4.  <span data-ttu-id="ac00f-121">Revise los planes de marcado devueltos para identificar si a alguno le falta la región de conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="ac00f-121">Review the returned dial plans to identify any that are missing the dial-in conferencing region.</span></span> <span data-ttu-id="ac00f-122">Para obtener más información, consulte la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ac00f-122">For details, see the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-set-the-region-property-for-a-dial-plan"></a><span data-ttu-id="ac00f-123">Para establecer la propiedad Región en un plan de marcado</span><span class="sxs-lookup"><span data-stu-id="ac00f-123">To set the region property for a dial plan</span></span>

1.  <span data-ttu-id="ac00f-124">Inicie sesión en el equipo como miembro del grupo RTCUniversalServerAdmins o como miembro del rol **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** o **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="ac00f-124">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="ac00f-125">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="ac00f-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ac00f-126">Para los planes de marcado a los que les falte la región de conferencias de acceso telefónico local, ejecute:</span><span class="sxs-lookup"><span data-stu-id="ac00f-126">For any dial plans that are missing the dial-in conferencing region, run:</span></span>
    
        Set-CsDialPlan [-Identity <Identity of the dial plan to be modified>] -DialinConferencingRegion "<new region>"
    
    <span data-ttu-id="ac00f-127">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ac00f-127">For example:</span></span>
    
        Set-CsDialPlan -Identity Redmond -DialinConferencingRegion "US West Coast"
    
    <span data-ttu-id="ac00f-128">En este ejemplo, se modifica el plan de marcado con la Identity de Redmond para establecer la propiedad DialinConferencingRegion en "Costa oeste de EE. UU.".</span><span class="sxs-lookup"><span data-stu-id="ac00f-128">In this example, the dial plan with the Identity of Redmond is modified to set the DialinConferencingRegion property to "US West Coast".</span></span> <span data-ttu-id="ac00f-129">Para obtener más información, consulte la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ac00f-129">For details, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="ac00f-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac00f-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

