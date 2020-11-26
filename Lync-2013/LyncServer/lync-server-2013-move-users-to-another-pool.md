---
title: 'Lync Server 2013: mover usuarios a otro grupo'
description: 'Lync Server 2013: mover usuarios a otro grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move users to another pool
ms:assetid: e7b4968c-0e9d-4d56-b5f1-9edf0f7206f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182600(v=OCS.15)
ms:contentKeyID: 48185879
ms.date: 02/09/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 21012e0df7567a79bca018d194878c85b8653ae4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425286"
---
# <a name="move-users-to-another-pool-in-lync-server-2013"></a><span data-ttu-id="15934-103">Mover usuarios a otro grupo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15934-103">Move users to another pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15934-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15934-104">

<span> </span></span></span>

<span data-ttu-id="15934-105">_**Última modificación del tema:** 2018-02-09_</span><span class="sxs-lookup"><span data-stu-id="15934-105">_**Topic Last Modified:** 2018-02-09_</span></span>

<span data-ttu-id="15934-106">Puede usar el panel de control de Lync Server para asignar usuarios a un servidor o grupo de servidores específico.</span><span class="sxs-lookup"><span data-stu-id="15934-106">You can use Lync Server Control Panel to assign users to a specific server or pool.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="15934-107">El traslado de todos los usuarios existentes de un grupo de origen que ejecute Lync Server 2010 o una versión anterior a un grupo de destino de Lync Server 2013 en un entorno de Active Directory complejo puede ralentizar la replicación de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="15934-107">Moving all existing users from a source pool that is running Lync Server 2010 or earlier to a Lync Server 2013 destination pool in a complex Active Directory environment might result in slower Active Directory replication.</span></span> <span data-ttu-id="15934-108">Para evitar esto, puede usar filtros de búsqueda para mover usuarios de grupos que ejecuten Lync Server 2010 o una versión anterior por separado, o bien puede usar el shell de administración de Lync Server para mover usuarios con cmdlets.</span><span class="sxs-lookup"><span data-stu-id="15934-108">To avoid this, you can use search filters to move users from pools that are running Lync Server 2010 or earlier separately, or you can use Lync Server Management Shell to move users with cmdlets.</span></span> <span data-ttu-id="15934-109">Además, la funcionalidad de filtro funciona con usuarios de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="15934-109">Also, the filter functionality works with Lync Server 2013 users.</span></span>



</div>

<div>

## <a name="to-move-selected-users-to-a-different-server-or-pool"></a><span data-ttu-id="15934-110">Para mover los usuarios seleccionados a otro servidor o grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="15934-110">To move selected users to a different server or pool</span></span>

1.  <span data-ttu-id="15934-111">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="15934-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="15934-112">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="15934-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="15934-113">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="15934-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="15934-114">En la barra de navegación izquierda, haga clic en **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="15934-114">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="15934-115">En el cuadro **Buscar usuarios** , escriba todas o la primera parte del nombre para mostrar, el nombre, el apellido, el nombre de cuenta del administrador de cuentas de seguridad (SAM), la dirección SIP o el identificador uniforme de recursos (URI) de la cuenta de usuario que desee y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="15934-115">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want, and then click **Find**.</span></span>

5.  <span data-ttu-id="15934-116">En la tabla, seleccione un usuario o usuarios específicos de la lista.</span><span class="sxs-lookup"><span data-stu-id="15934-116">In the table, select a specific user or users in the list.</span></span>

6.  <span data-ttu-id="15934-117">En el menú **acción** , haga clic en **mover los usuarios seleccionados al grupo**.</span><span class="sxs-lookup"><span data-stu-id="15934-117">On the **Action** menu, click **Move selected users to pool**.</span></span>

7.  <span data-ttu-id="15934-118">En **mover usuarios**, seleccione el grupo al que desea mover los usuarios en el **grupo de registrador de destinos**.</span><span class="sxs-lookup"><span data-stu-id="15934-118">In **Move Users**, select the pool that you want to move the users to in **Destination registrar pool**.</span></span>

8.  <span data-ttu-id="15934-119">Faculta Si el servidor de destino o el grupo de servidores no están disponibles, active la casilla **forzar** .</span><span class="sxs-lookup"><span data-stu-id="15934-119">(Optional) If the destination server or pool is unavailable, select the **Force** check box.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="15934-120">Si selecciona <STRONG>Force</STRONG>, la cuenta de usuario se mueve, pero los datos de usuario asociados tales conferencias y contactos programados no se mueven.</span><span class="sxs-lookup"><span data-stu-id="15934-120">If you select <STRONG>Force</STRONG>, the user account is moved, but associated user data such scheduled conferences and contacts is not moved.</span></span>

    
    </div>

</div>

<div>

## <a name="to-move-all-users-from-one-server-or-pool-to-a-different-server-or-pool"></a><span data-ttu-id="15934-121">Para mover todos los usuarios de un servidor o grupo de servidores a otro servidor o grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="15934-121">To move all users from one server or pool to a different server or pool</span></span>

1.  <span data-ttu-id="15934-122">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="15934-122">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="15934-123">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="15934-123">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="15934-124">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="15934-124">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="15934-125">En la barra de navegación izquierda, haga clic en **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="15934-125">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="15934-126">En el menú **acción** , haga clic en **mover todos los usuarios al grupo**.</span><span class="sxs-lookup"><span data-stu-id="15934-126">On the **Action** menu, click **Move all users to pool**.</span></span>

5.  <span data-ttu-id="15934-127">En **mover usuarios**, seleccione el grupo que contiene las cuentas de usuario que desea mover en el **grupo de registrador de origen**.</span><span class="sxs-lookup"><span data-stu-id="15934-127">In **Move Users**, select the pool that contains the user accounts that you want to move in **Source registrar pool**.</span></span>

6.  <span data-ttu-id="15934-128">En **grupo de registradores de destino**, seleccione el grupo al que desea mover a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="15934-128">In **Destination registrar pool**, select the pool that you want to move the users to.</span></span>

7.  <span data-ttu-id="15934-129">Faculta Si el servidor de destino o el grupo de servidores no están disponibles, active la casilla **forzar** .</span><span class="sxs-lookup"><span data-stu-id="15934-129">(Optional) If the destination server or pool is unavailable, select the **Force** check box.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="15934-130">Si selecciona <STRONG>Force</STRONG>, la cuenta de usuario se mueve, pero los datos de usuario asociados tales conferencias y contactos programados no se mueven.</span><span class="sxs-lookup"><span data-stu-id="15934-130">If you select <STRONG>Force</STRONG>, the user account is moved, but associated user data such scheduled conferences and contacts is not moved.</span></span>

    
    </div>

</div>

<div>

## <a name="to-move-users-from-one-pool-to-a-different-pool-by-using-a-filter"></a><span data-ttu-id="15934-131">Para mover los usuarios de un grupo a otro mediante un filtro</span><span class="sxs-lookup"><span data-stu-id="15934-131">To move users from one pool to a different pool by using a filter</span></span>

1.  <span data-ttu-id="15934-132">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="15934-132">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="15934-133">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="15934-133">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="15934-134">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="15934-134">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="15934-135">En la barra de navegación izquierda, haga clic en **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="15934-135">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="15934-136">En **búsqueda de usuario**, haga clic en **Buscar** y, a continuación, haga clic en **Agregar filtro**.</span><span class="sxs-lookup"><span data-stu-id="15934-136">In **User Search**, click **Search**, and then click **Add Filter**.</span></span>

5.  <span data-ttu-id="15934-137">En los criterios de búsqueda, seleccione **registrar grupo**, seleccione **igual a**, seleccione **FQDN del grupo actual** y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="15934-137">In the Search criteria, select **Registrar Pool**, select **Equal to**, select **Current Pool FQDN**, and then click **Find**.</span></span>

6.  <span data-ttu-id="15934-138">En el menú **acción** , haga clic en **mover todos los usuarios al grupo**.</span><span class="sxs-lookup"><span data-stu-id="15934-138">On the **Action** menu, click **Move all users to pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="15934-139">Cuando se aplica un filtro a un conjunto de usuarios existente, la opción <STRONG>mover todos los usuarios al grupo</STRONG> se encuentra en el contexto del subconjunto filtrado de usuarios, no de <STRONG><EM>todos</EM></STRONG> los usuarios posibles.</span><span class="sxs-lookup"><span data-stu-id="15934-139">When a filter is applied to an existing set of users, the option <STRONG>Move all users to pool</STRONG> is in the context of the filtered subset of users, not <STRONG><EM>all</EM></STRONG> possible users.</span></span>

    
    </div>

7.  <span data-ttu-id="15934-140">En **mover usuarios**, seleccione el grupo que contiene las cuentas de usuario que desea mover en el **grupo de registrador de origen**.</span><span class="sxs-lookup"><span data-stu-id="15934-140">In **Move Users**, select the pool that contains the user accounts that you want to move in **Source registrar pool**.</span></span>

8.  <span data-ttu-id="15934-141">En **grupo de registradores de destino**, seleccione el grupo al que desea mover los usuarios.</span><span class="sxs-lookup"><span data-stu-id="15934-141">In **Destination registrar pool**, select the pool where you want to move the users.</span></span>

9.  <span data-ttu-id="15934-142">Faculta Si el servidor de destino o el grupo de servidores no están disponibles, active la casilla **forzar** .</span><span class="sxs-lookup"><span data-stu-id="15934-142">(Optional) If the destination server or pool is unavailable, select the **Force** check box.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="15934-143">Si selecciona <STRONG>Force</STRONG>, la cuenta de usuario se mueve, pero los datos de usuario asociados tales conferencias y contactos programados no se mueven.</span><span class="sxs-lookup"><span data-stu-id="15934-143">If you select <STRONG>Force</STRONG>, the user account is moved, but associated user data such scheduled conferences and contacts is not moved.</span></span>

    
    </div>

</div>

<div>

## <a name="to-move-users-from-one-pool-to-another-using-windows-powershell-cmdlets"></a><span data-ttu-id="15934-144">Para mover usuarios de un grupo a otro mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="15934-144">To move users from one pool to another using Windows PowerShell cmdlets</span></span>

1.  <span data-ttu-id="15934-145">En función de cómo ejecute los comandos de Windows PowerShell (es decir, de forma local o remota), tendrá que iniciar sesión como miembro de las funciones administrativas correctas de Lync Server 2013 de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="15934-145">Depending on how you run Windows PowerShell commands (that is, locally or remotely), you need to log on as a member of the correct Lync Server 2013 administrative roles as follows:</span></span>
    
    1.  <span data-ttu-id="15934-146">Si está ejecutando los comandos en el equipo local (por ejemplo, inicia sesión directamente en un servidor de aplicaciones para el usuario): inicie sesión en el equipo donde está instalado el shell de administración de Lync Server como miembro del grupo RTCUniversalServerAdmins o con los derechos de usuario necesarios, tal como se describe en [permisos de configuración de delegado en Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="15934-146">If you are running the commands on the local machine (for example, you log on directly to a Front End Server): Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>
    
    2.  <span data-ttu-id="15934-147">Si ejecuta los comandos de forma remota en otro equipo (por ejemplo, inicia sesión en el equipo y ejecuta los comandos de forma remota en un servidor front-end Standard Edition): desde una cuenta de usuario asignada al rol CsUserAdministrator o al rol CsAdministrator, inicie sesión en cualquier equipo de su implementación interna.</span><span class="sxs-lookup"><span data-stu-id="15934-147">If you are running the commands remotely on another computer (for example, you log on to your computer and run the commands remotely on a Standard Edition Front End Server): From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="15934-148">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="15934-148">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="15934-149">Para mover usuarios individuales, use el cmdlet Move-CsUser de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="15934-149">To move single users, use the Move-CsUser cmdlet as follows:</span></span>
    
        Move-CsUser -Identity "Pilar Ackerman" -Target "pool01.contoso.net"
    
    <span data-ttu-id="15934-150">Donde el usuario debe mover es el usuario Pilar Ackerman, y el usuario se moverá de su grupo local asignado a la agrupación pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="15934-150">Where the user to move is the user Pilar Ackerman, and the user will be moved from their currently assigned home pool to the pool pool01.contoso.net</span></span>

4.  <span data-ttu-id="15934-151">Para mover un gran número de usuarios, use filtros con el cmdlet **Get-CsUser** y pase el conjunto de usuarios resultante a **Move-CsUser**:</span><span class="sxs-lookup"><span data-stu-id="15934-151">To move a large number of users, use filters with the **Get-CsUser** cmdlet and pass the resulting set of users to **Move-CsUser**:</span></span>
    
        Get-CsUser -Filter {RegistrarPool -eq "CurrentPoolFqdn"} | Move-CsUser -Target "TargetPoolFQDN"
    
    <span data-ttu-id="15934-152">Los comandos combinados de **Get-CsUser** y **Move-CsUser** pueden dar lugar a esto:</span><span class="sxs-lookup"><span data-stu-id="15934-152">The combined commands of the **Get-CsUser** and **Move-CsUser** might result in this:</span></span>
    
        Get-CsUser -Filter {RegistrarPool -eq "pool02.contoso.net"} | Move-CsUser -Target "pool01.contoso.net"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="15934-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="15934-153">See Also</span></span>


[<span data-ttu-id="15934-154">Modificar las propiedades de la cuenta de usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15934-154">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)  
  

<span data-ttu-id="15934-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15934-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

