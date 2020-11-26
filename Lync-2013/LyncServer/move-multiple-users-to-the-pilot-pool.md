---
title: Mover varios usuarios a la agrupación piloto
description: Mover varios usuarios a la agrupación piloto.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move multiple users to the pilot pool
ms:assetid: 90d0590c-922c-4933-b778-9dd850b59310
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205096(v=OCS.15)
ms:contentKeyID: 48184838
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 121509fbad863b0ce2d6cc9c7e9afaef360e2eb6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438507"
---
# <a name="move-multiple-users-to-the-pilot-pool"></a><span data-ttu-id="cf959-103">Mover varios usuarios a la agrupación piloto</span><span class="sxs-lookup"><span data-stu-id="cf959-103">Move multiple users to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf959-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf959-104">

<span> </span></span></span>

<span data-ttu-id="cf959-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="cf959-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="cf959-106">Puede mover varios usuarios de su grupo de 2010 de Lync Server a su grupo piloto de Lync Server 2013 con el panel de control de Lync Server 2013 o el shell de administración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf959-106">You can move multiple users from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="cf959-107">Para mover varios usuarios con el panel de control de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf959-107">To move multiple users by using the Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="cf959-108">Abra el **Panel de control de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="cf959-108">Open **Lync Server Control Panel**.</span></span>

2.  <span data-ttu-id="cf959-109">Haga clic en **Usuarios**, haga clic en Buscar y, posteriormente, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="cf959-109">Click **Users**, click Search, and then click **Find**.</span></span>

3.  <span data-ttu-id="cf959-110">Seleccione dos usuarios que desee mover al grupo de servidores de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf959-110">Select two users that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="cf959-111">En este ejemplo, se moverán los usuarios Chen Yang y Claus Hansen.</span><span class="sxs-lookup"><span data-stu-id="cf959-111">In this example, we will move users Chen Yang and Claus Hansen.</span></span>
    
    <span data-ttu-id="cf959-112">![Mover usuarios a un grupo de registros específico](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Mover usuarios a un grupo de registros específico")</span><span class="sxs-lookup"><span data-stu-id="cf959-112">![Move users to specific register pool](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Move users to specific register pool")</span></span>  

4.  <span data-ttu-id="cf959-113">En el menú **acción** , seleccione **mover usuarios seleccionados al grupo**.</span><span class="sxs-lookup"><span data-stu-id="cf959-113">From the **Action** menu, select **Move selected users to pool**.</span></span>

5.  <span data-ttu-id="cf959-114">En la lista desplegable, seleccione el grupo de 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cf959-114">From the drop-down list, select the Lync Server 2013 pool.</span></span>

6.  <span data-ttu-id="cf959-115">Haga clic en **Acción** y, posteriormente, haga clic en **Mover usuarios seleccionados a grupo**.</span><span class="sxs-lookup"><span data-stu-id="cf959-115">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="cf959-116">Haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="cf959-116">Click OK.</span></span>
    
    <span data-ttu-id="cf959-117">![Cuadro de diálogo mover usuarios, conjunto de registradores de destino](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Cuadro de diálogo mover usuarios, conjunto de registradores de destino")</span><span class="sxs-lookup"><span data-stu-id="cf959-117">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

7.  <span data-ttu-id="cf959-118">Compruebe que la columna del **Grupo registrador** de los usuarios contiene ahora el grupo de servidores de Lync Server 2013, lo que indica que los usuarios se movieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="cf959-118">Verify that the **Registrar pool** column for the users now contains the Lync Server 2013 pool, which indicates that the users have been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="cf959-119">Para mover varios usuarios con el shell de administración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf959-119">To move multiple users by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="cf959-120">Abra el shell de administración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf959-120">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="cf959-121">En la línea de comandos, escriba lo siguiente y reemplace **user1** y **user2** por los nombres de usuario específicos que desea mover y reemplazar **\_ FQDN de grupo** con el nombre del grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="cf959-121">At the command line, type the following and replace **User1** and **User2** with specific user names you want to move and replace **pool\_FQDN** with the name of the destination pool.</span></span> <span data-ttu-id="cf959-122">En este ejemplo, moveremos a los usuarios Hao Chen y Katie Katie.</span><span class="sxs-lookup"><span data-stu-id="cf959-122">In this example we will move users Hao Chen and Katie Jordan.</span></span>
    
        Get-CsUser -Filter {DisplayName -eq "User1" -or DisplayName - eq "User2"} | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="cf959-123">![Ejemplo de cmdlet de Get-CsUser de PowerShell](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Ejemplo de cmdlet de Get-CsUser de PowerShell")</span><span class="sxs-lookup"><span data-stu-id="cf959-123">![Example of PowerShell Get-CsUser cmdlet](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Example of PowerShell Get-CsUser cmdlet")</span></span>  

3.  <span data-ttu-id="cf959-124">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cf959-124">At the command line, type the following</span></span>
    
        Get-CsUser -Identity "User1"

4.  <span data-ttu-id="cf959-125">La identidad del **grupo de registradores** debe apuntar ahora al grupo que especificó como **\_ FQDN del grupo** en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="cf959-125">The **Registrar Pool** identity should now point to the pool you specified as **pool\_FQDN** in the previous step.</span></span> <span data-ttu-id="cf959-126">La presencia de esta identidad confirma que el usuario se movió correctamente.</span><span class="sxs-lookup"><span data-stu-id="cf959-126">The presence of this identity confirms that the user has been successfully moved.</span></span> <span data-ttu-id="cf959-127">Repita el paso para verificar que se ha movido **usuario2** .</span><span class="sxs-lookup"><span data-stu-id="cf959-127">Repeat step to verify **User2** has been moved.</span></span>
    
    <span data-ttu-id="cf959-128">![Resultado del cmdlet Get-UsUser de identidad de PowerShell](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Resultado del cmdlet Get-UsUser de identidad de PowerShell")</span><span class="sxs-lookup"><span data-stu-id="cf959-128">![Output of PowerShell Get-UsUser -Identity cmdlet](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Output of PowerShell Get-UsUser -Identity  cmdlet")</span></span>  

</div>

<div>

## <a name="to-move-all-users-at-the-same-time-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="cf959-129">Para mover todos los usuarios al mismo tiempo mediante el shell de administración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf959-129">To move all users at the same time by using the Lync Server 2013 Management Shell</span></span>

<span data-ttu-id="cf959-130">En este ejemplo, todos los usuarios han sido devueltos al grupo de servidores de Lync Server 2010 (pool01.contoso.net).</span><span class="sxs-lookup"><span data-stu-id="cf959-130">In this example, all users have been returned to the Lync Server 2010 pool (pool01.contoso.net).</span></span> <span data-ttu-id="cf959-131">Con el shell de administración de Lync Server 2013, se moverán todos los usuarios al mismo tiempo al grupo de servidores de Lync Server 2013 (pool02.contoso.net).</span><span class="sxs-lookup"><span data-stu-id="cf959-131">Using the Lync Server 2013 Management Shell, we will move all users at the same time to the Lync Server 2013 pool (pool02.contoso.net).</span></span>

1.  <span data-ttu-id="cf959-132">Abra el **Shell de administración de Lync Server 2013**.</span><span class="sxs-lookup"><span data-stu-id="cf959-132">Open the **Lync Server 2013 Management Shell**.</span></span>

2.  <span data-ttu-id="cf959-133">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="cf959-133">At the command line, type the following:</span></span>
    
        Get-CsUser -OnLyncServer | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="cf959-134">![Cmdlet de PowerShell y resultados en el shell de administración](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "Cmdlet de PowerShell y resultados en el shell de administración")</span><span class="sxs-lookup"><span data-stu-id="cf959-134">![PowerShell cmdlet and results in Management Shell](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "PowerShell cmdlet and results in Management Shell")</span></span>  

3.  <span data-ttu-id="cf959-135">A continuación, ejecute **Get-CsUser** para uno de los usuarios de la prueba piloto.</span><span class="sxs-lookup"><span data-stu-id="cf959-135">Next, run **Get-CsUser** for one of the pilot users.</span></span>
    
        Get-CsUser -Identity "Hao Chen"

4.  <span data-ttu-id="cf959-136">La identidad del **grupo de registradores** de cada usuario apunta ahora al grupo que especificó como "FQDN del grupo \_ " en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="cf959-136">The **Registrar Pool** identity for each user now points to the pool you specified as “pool\_FQDN” in the previous step.</span></span> <span data-ttu-id="cf959-137">La presencia de esta identidad confirma que el usuario se movió correctamente.</span><span class="sxs-lookup"><span data-stu-id="cf959-137">The presence of this identity confirms that the user has been successfully moved.</span></span>

5.  <span data-ttu-id="cf959-138">Además, podemos ver la lista de usuarios en el panel de control de Lync Server 2013 y comprobar que el valor del grupo de registradores apunta al grupo de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf959-138">Additionally, we can view the list of users in the Lync Server 2013 Control Panel and verify that the Registrar Pool value now points to the Lync Server 2013 pool.</span></span>
    
    <span data-ttu-id="cf959-139">![Lista de usuarios del panel de control de Lync Server 2013](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Lista de usuarios del panel de control de Lync Server 2013")</span><span class="sxs-lookup"><span data-stu-id="cf959-139">![Lync Server 2013 Control Panel user list](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Lync Server 2013 Control Panel user list")</span></span>  

<span data-ttu-id="cf959-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf959-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

