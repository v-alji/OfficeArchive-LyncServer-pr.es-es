---
title: 'Lync Server 2013: asignar una directiva de conferencia por usuario'
description: 'Lync Server 2013: asignar una directiva de conferencia por usuario.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user conferencing policy
ms:assetid: 72f12c72-65f7-44fe-ab81-0f57cb2f87d1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521015(v=OCS.15)
ms:contentKeyID: 48184475
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 819d1431a2a7a921ff8c306c47c8b5f86bf5d5bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440517"
---
# <a name="assign-a-per-user-conferencing-policy-in-lync-server-2013"></a><span data-ttu-id="bce56-103">Asignar una directiva de conferencia por usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bce56-103">Assign a per-user conferencing policy in Lync Server 2013</span></span>

 


<span data-ttu-id="bce56-104">La Directiva de conferencia es una de las configuraciones individuales de una cuenta de usuario que puede configurar en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bce56-104">The conferencing policy is one of the individual settings of a user account that you can configure in Lync Server Control Panel.</span></span>

<span data-ttu-id="bce56-105">La implementación de una o más directivas de conferencia por usuario es opcional.</span><span class="sxs-lookup"><span data-stu-id="bce56-105">Deploying one or more per-user conferencing policies is optional.</span></span> <span data-ttu-id="bce56-106">También puede implementar una directiva de conferencia de nivel internacional o una directiva de conferencia de nivel de sitio.</span><span class="sxs-lookup"><span data-stu-id="bce56-106">You can also deploy only a global-level conferencing policy or site-level conferencing policy.</span></span> <span data-ttu-id="bce56-107">Si implementa directivas por usuario, debe asignarlas explícitamente a usuarios, grupos o objetos de contacto.</span><span class="sxs-lookup"><span data-stu-id="bce56-107">If you do deploy per-user policies, you must explicitly assign them to users, groups, or contact objects.</span></span> <span data-ttu-id="bce56-108">Los permisos y derechos de usuario de conferencia se especifican automáticamente de forma predeterminada para los definidos en la Directiva de conferencia global cuando no se ha asignado ninguna directiva específica de nivel de sitio o de usuario.</span><span class="sxs-lookup"><span data-stu-id="bce56-108">Conferencing user rights and permissions automatically default to those defined in the global-level conferencing policy when no specific site-level or per-user policy is assigned.</span></span>

<span data-ttu-id="bce56-109">Después de crear al menos una directiva de conferencia por usuario, use los procedimientos de este tema para asignar la Directiva que especifica los permisos y derechos de usuario que desea que el servidor otorgue a las reuniones organizadas por un usuario en particular.</span><span class="sxs-lookup"><span data-stu-id="bce56-109">After creating at least one per-user conferencing policy, use the procedures in this topic to assign the policy that specifies the user rights and permissions that you want the server to grant to the meetings organized by a particular user.</span></span>

<span data-ttu-id="bce56-110">Para obtener una lista de todas las configuraciones de directiva de conferencia disponibles, consulte [referencia de configuración de directiva de conferencia para Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span><span class="sxs-lookup"><span data-stu-id="bce56-110">For a list of all available conferencing policy settings, see [Conferencing policy settings reference for Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span></span>

<span data-ttu-id="bce56-111">Para obtener más información sobre cómo crear directivas de conferencia, consulte [crear o modificar una directiva de conferencia en Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span><span class="sxs-lookup"><span data-stu-id="bce56-111">For details about creating conferencing policies, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span></span>

## <a name="to-assign-a-per-user-conferencing-policy"></a><span data-ttu-id="bce56-112">Para asignar una directiva de conferencia por usuario</span><span class="sxs-lookup"><span data-stu-id="bce56-112">To assign a per-user conferencing policy</span></span>

1.  <span data-ttu-id="bce56-113">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="bce56-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="bce56-114">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bce56-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="bce56-115">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bce56-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="bce56-116">En la barra de navegación izquierda, haga clic en **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="bce56-116">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="bce56-117">Use uno de los métodos siguientes para encontrar a un usuario:</span><span class="sxs-lookup"><span data-stu-id="bce56-117">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="bce56-118">En el cuadro **Buscar usuarios**, escriba la primera porción del nombre para mostrar, el nombre, los apellidos, el nombre de la cuenta del Administrador de cuentas de seguridad (SAM), la dirección SIP o el identificador uniforme de recursos (URI) de la cuenta de usuario y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="bce56-118">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="bce56-119">Si ha guardado una consulta, haga clic en el icono **Abrir consulta**, use el cuadro de diálogo **Abrir** para recuperar la consulta (un archivo .usf) y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="bce56-119">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="bce56-120">(Opcional) Especificar criterios de búsqueda adicionales para restringir los resultados:</span><span class="sxs-lookup"><span data-stu-id="bce56-120">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="bce56-121">Haga clic en **Agregar filtro**.</span><span class="sxs-lookup"><span data-stu-id="bce56-121">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="bce56-122">Especifique la propiedad de usuario. Para ello, escríbala o haga clic en la flecha de la lista desplegable para seleccionar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bce56-122">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="bce56-123">En la lista desplegable **Igual a**, haga clic en el operador (por ejemplo, **Igual a** o **No igual a**).</span><span class="sxs-lookup"><span data-stu-id="bce56-123">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="bce56-124">En función de la propiedad de usuario que haya seleccionado, especifique los criterios que desee utilizar para filtrar los resultados de búsqueda escribiendo o haciendo clic en la flecha de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="bce56-124">Depending on the user property you selected, enter the criteria you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="bce56-125">Para agregar cláusulas de búsqueda adicionales a la consulta, haga clic en <STRONG>Agregar filtro</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="bce56-125">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

    
    5.  <span data-ttu-id="bce56-126">Haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="bce56-126">Click **Find**.</span></span>

6.  <span data-ttu-id="bce56-127">Haga clic en un usuario en los resultados de búsqueda, haga clic en **Acción** y, a continuación, en **Asignar directivas**.</span><span class="sxs-lookup"><span data-stu-id="bce56-127">Click a user in the search results, click **Action**, and then click **Assign policies**.</span></span>
    

    > [!TIP]  
    > <span data-ttu-id="bce56-128">Si desea que la misma directiva de conferencia por usuario se aplique a varios usuarios, seleccione varios usuarios en los resultados de búsqueda, haga clic en <STRONG>acciones</STRONG>y, a continuación, haga clic en <STRONG>asignar directivas</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="bce56-128">If you want the same per-user conferencing policy to apply to multiple users, select multiple users in the search results, then click <STRONG>Actions</STRONG>, and then click <STRONG>Assign policies</STRONG>.</span></span>



7.  <span data-ttu-id="bce56-129">En **asignar directivas**, en **Directiva de conferencia**, realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="bce56-129">In **Assign Policies**, under **Conferencing policy**, do one of the following:</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="bce56-130">Puesto que existen varias directivas que puede configurar en <STRONG>asignar directivas</STRONG>, <STRONG> &lt; mantener como está &gt; </STRONG> seleccionado de forma predeterminada para todas las directivas del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bce56-130">Because there are multiple policies that you can configure in <STRONG>Assign Policies</STRONG>, <STRONG>&lt;Keep as is&gt;</STRONG> is selected by default for every policy in the dialog box.</span></span> <span data-ttu-id="bce56-131">Para seguir usando la directiva asignada anteriormente al usuario, no efectúe cambios en esta configuración.</span><span class="sxs-lookup"><span data-stu-id="bce56-131">Continue using the policy previously assigned to the user by making no changes to this setting.</span></span>

    
      - <span data-ttu-id="bce56-132">Seleccione esta opción **\<Automatic\>** para permitir que Lync Server 2013 pueda elegir automáticamente la Directiva de nivel global o, si está definida, la Directiva de nivel de sitio.</span><span class="sxs-lookup"><span data-stu-id="bce56-132">Select **\<Automatic\>** to allow Lync Server 2013 to automatically choose either the global-level policy or, if defined, the site-level policy.</span></span>
    
      - <span data-ttu-id="bce56-133">Haga clic en el nombre de una directiva de conferencia por usuario que haya definido previamente en la página **Directiva de conferencia** .</span><span class="sxs-lookup"><span data-stu-id="bce56-133">Click the name of a per-user conferencing policy you previously defined on the **Conferencing Policy** page.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="bce56-134">Para ayudarle a decidir la directiva que desea asignar, tras hacer clic en el nombre de una directiva, haga clic en <STRONG>Ver</STRONG> para ver los derechos y permisos de usuario definidos en la directiva.</span><span class="sxs-lookup"><span data-stu-id="bce56-134">To help you decide the policy you want to assign, after you click a policy name, click <STRONG>View</STRONG> to view the user rights and permissions defined in the policy.</span></span>



8.  <span data-ttu-id="bce56-135">Cuando haya terminado, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="bce56-135">When you are finished, click **OK**.</span></span>

## <a name="assigning-a-per-user-conferencing-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="bce56-136">Asignar una directiva de conferencia de Per-User con cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bce56-136">Assigning a Per-User Conferencing Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="bce56-137">Las directivas de conferencia por usuario se pueden asignar mediante Windows PowerShell y el cmdlet Grant-CsConferencingPolicy.</span><span class="sxs-lookup"><span data-stu-id="bce56-137">Per-user conferencing policies can be assigned by using Windows PowerShell and the Grant-CsConferencingPolicy cmdlet.</span></span> <span data-ttu-id="bce56-138">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bce56-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="bce56-139">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="bce56-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-conferencing-policy-to-a-single-user"></a><span data-ttu-id="bce56-140">Para asignar una directiva de conferencia por usuario a un solo usuario</span><span class="sxs-lookup"><span data-stu-id="bce56-140">To assign a per-user conferencing policy to a single user</span></span>

  - <span data-ttu-id="bce56-141">El comando siguiente asigna la Directiva de conferencia por usuario RedmondConferencingPolicy al usuario Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="bce56-141">The following command assigns the per-user conferencing policy RedmondConferencingPolicy to the user Ken Myer.</span></span>
    
        Grant-CsConferencingPolicy -Identity "Ken Myer" -PolicyName "RedmondConferencingPolicy"

## <a name="to-assign-a-per-user-conferencing-policy-to-multiple-users"></a><span data-ttu-id="bce56-142">Para asignar una directiva de conferencia por usuario a varios usuarios</span><span class="sxs-lookup"><span data-stu-id="bce56-142">To assign a per-user conferencing policy to multiple users</span></span>

  - <span data-ttu-id="bce56-143">Este comando asigna la Directiva de conferencia por usuario HRConferencingPolicy a todos los usuarios que trabajan para el Departamento de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="bce56-143">This command assigns the per-user conferencing policy HRConferencingPolicy to all the users who work for the Human Resources department.</span></span> <span data-ttu-id="bce56-144">Para obtener más información sobre el parámetro LdapFilter que se usa en este comando, consulte la documentación del cmdlet [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="bce56-144">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "Department=Human Resources" | Grant-CsConferencingPolicy -PolicyName "HRConferencingPolicy"

## <a name="to-unassign-a-per-user-conferencing-policy"></a><span data-ttu-id="bce56-145">Para cancelar la asignación de una directiva de conferencia por usuario</span><span class="sxs-lookup"><span data-stu-id="bce56-145">To unassign a per-user conferencing policy</span></span>

  - <span data-ttu-id="bce56-146">El comando siguiente elimina la asignación de cualquier directiva de conferencia por usuario asignada previamente a Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="bce56-146">The following command unassigns any per-user conferencing policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="bce56-147">Después de quitar la asignación de la directiva por usuario, se usará automáticamente la directiva global o la directiva del sitio local, si existe, para administrar a Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="bce56-147">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="bce56-148">La directiva de sitio tiene prioridad sobre la directiva global.</span><span class="sxs-lookup"><span data-stu-id="bce56-148">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsConferencingPolicy -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="bce56-149">Para obtener más información, consulte el tema de ayuda para el cmdlet [Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="bce56-149">For more information, see the help topic for the [Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\)) cmdlet.</span></span>

## <a name="see-also"></a><span data-ttu-id="bce56-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="bce56-150">See Also</span></span>


[<span data-ttu-id="bce56-151">Crear o modificar una directiva de conferencia en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bce56-151">Create or modify a conferencing policy in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-conferencing-policy.md)  


[<span data-ttu-id="bce56-152">Asignación de directivas por usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bce56-152">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)

