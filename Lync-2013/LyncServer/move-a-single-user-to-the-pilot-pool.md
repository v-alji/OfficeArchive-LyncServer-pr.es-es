---
title: Mover un solo usuario a la agrupación piloto
description: Mover un solo usuario a la agrupación piloto.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move a single user to the pilot pool
ms:assetid: e9de81a8-40dd-4446-81e7-a2b810eaea50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205401(v=OCS.15)
ms:contentKeyID: 48185905
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5f7396ed2d92c7015f01ff6cd6e90fd3998219d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398639"
---
# <a name="move-a-single-user-to-the-pilot-pool"></a><span data-ttu-id="d8d64-103">Mover un solo usuario a la agrupación piloto</span><span class="sxs-lookup"><span data-stu-id="d8d64-103">Move a single user to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8d64-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8d64-104">

<span> </span></span></span>

<span data-ttu-id="d8d64-105">_**Última modificación del tema:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="d8d64-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="d8d64-106">Puede mover un usuario de su grupo de 2010 de Lync Server a su grupo de pruebas piloto de Lync Server 2013 mediante el panel de control de Lync Server 2013 o el shell de administración de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d8d64-106">You can move a user from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="d8d64-107">En el ejemplo siguiente, en la columna registrar grupo, **pool01.contoso.net** es el grupo de servidores de Lync Server 2010 y todos los seis de estos usuarios están conectados a este grupo.</span><span class="sxs-lookup"><span data-stu-id="d8d64-107">In the example below, in the Registrar pool column, **pool01.contoso.net** is the Lync Server 2010 pool, and all six of these users are connected to this pool.</span></span> <span data-ttu-id="d8d64-108">Use los procedimientos siguientes para mover un usuario a su grupo de servidores de Lync Server 2013 con el panel de control de Lync Server 2013 y el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d8d64-108">Use the following procedures to move a user to your Lync Server 2013 pool using Lync Server 2013 Control Panel and Lync Server Management Shell.</span></span>

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="d8d64-109">Para mover un usuario mediante el panel de control de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8d64-109">To move a user by using the Lync Server 2013 Control Panel</span></span>

<span data-ttu-id="d8d64-110">**Lista de usuarios en el panel de control de Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="d8d64-110">**List of users in the Lync Server 2013 Control Panel**</span></span>

<span data-ttu-id="d8d64-111">![Panel de control de Lync Server, cuadro de diálogo mover usuario](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Panel de control de Lync Server, cuadro de diálogo mover usuario")</span><span class="sxs-lookup"><span data-stu-id="d8d64-111">![Lync Server Control Panel, Move User dialog](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Lync Server Control Panel, Move User dialog")</span></span>

1.  <span data-ttu-id="d8d64-112">Inicie sesión en el servidor front-end con una cuenta que sea miembro del grupo RTCUniversalServerAdmins o miembro del rol administrativo CsAdministrator o CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d8d64-112">Log on to the Front End Server with an account that is a member of the RTCUniversalServerAdmins group or a member of the CsAdministrator or CsUserAdministrator administrative role.</span></span>

2.  <span data-ttu-id="d8d64-113">Abra el **Panel de control de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="d8d64-113">Open **Lync Server Control Panel**.</span></span>

3.  <span data-ttu-id="d8d64-114">Haga clic en **Usuarios**, haga clic en Buscar y, posteriormente, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="d8d64-114">Click **Users**, click Search, and then click **Find**.</span></span>

4.  <span data-ttu-id="d8d64-115">Seleccione el usuario que desea mover al grupo de servidores de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d8d64-115">Select a user that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="d8d64-116">En este ejemplo, moveremos a Sara Davis.</span><span class="sxs-lookup"><span data-stu-id="d8d64-116">In this example, we will move user Sara Davis.</span></span>

5.  <span data-ttu-id="d8d64-117">En el menú **Acción**, seleccione **Mover usuarios seleccionados a grupo**.</span><span class="sxs-lookup"><span data-stu-id="d8d64-117">On the **Action** menu, select **Move selected users to pool**.</span></span>

6.  <span data-ttu-id="d8d64-118">En la lista desplegable, seleccione el grupo de 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d8d64-118">From the drop-down list, select the Lync Server 2013 pool.</span></span>

7.  <span data-ttu-id="d8d64-119">Haga clic en **Acción** y, posteriormente, haga clic en **Mover usuarios seleccionados a grupo**.</span><span class="sxs-lookup"><span data-stu-id="d8d64-119">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="d8d64-120">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d8d64-120">Click **OK**.</span></span>
    
    <span data-ttu-id="d8d64-121">![Cuadro de diálogo mover usuarios, conjunto de registradores de destino](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Cuadro de diálogo mover usuarios, conjunto de registradores de destino")</span><span class="sxs-lookup"><span data-stu-id="d8d64-121">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

8.  <span data-ttu-id="d8d64-122">Compruebe que la columna del **Grupo registrador** del usuario contiene ahora el grupo de servidores de Lync Server 2013, lo que indica que el usuario se ha movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8d64-122">Verify that the **Registrar pool** column for the user now contains the Lync Server 2013 pool, which indicates that the user has been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="d8d64-123">Para mover un usuario mediante el shell de administración de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8d64-123">To move a user by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="d8d64-124">Abra el shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d8d64-124">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="d8d64-125">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="d8d64-125">At the command line, type the following:</span></span>
    
        Move-CsUser -Identity "David Pelton" -Target "pool02.contoso.net"

3.  <span data-ttu-id="d8d64-126">A continuación, en la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8d64-126">Next, at the command line, type the following:</span></span>
    
        Get-CsUser -Identity "David Pelton"

4.  <span data-ttu-id="d8d64-127">La identidad de **RegistrarPool** apunta ahora al grupo de servidores de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="d8d64-127">The **RegistrarPool** identity now points to the Lync Server 2013 pool.</span></span> <span data-ttu-id="d8d64-128">La presencia de esta identidad confirma que el usuario se movió correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8d64-128">The presence of this identity confirms that the user has been successfully moved.</span></span>
    
    <span data-ttu-id="d8d64-129">![Resultado de Get-CsUser cmdlet con el filtro Identity](images/JJ205401.bc5d4672-8068-4475-b882-dbd305c801a9(OCS.15).jpg "Resultado de Get-CsUser cmdlet con el filtro Identity")</span><span class="sxs-lookup"><span data-stu-id="d8d64-129">![Output from Get-CsUser cmdlet with Identity filter](images/JJ205401.bc5d4672-8068-4475-b882-dbd305c801a9(OCS.15).jpg "Output from Get-CsUser cmdlet with Identity filter")</span></span>  
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d8d64-130">Para obtener detalles sobre el cmdlet <STRONG>Get-CsUser</STRONG> , ejecute: <STRONG>Get-Help Get-CsUser-Detailed</STRONG></span><span class="sxs-lookup"><span data-stu-id="d8d64-130">For details about the <STRONG>Get-CsUser</STRONG> cmdlet, run: <STRONG>Get-Help Get-CsUser –Detailed</STRONG></span></span>

    
    <span data-ttu-id="d8d64-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8d64-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

