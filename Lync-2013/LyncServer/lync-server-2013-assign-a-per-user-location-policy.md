---
title: 'Lync Server 2013: asignar una directiva de ubicación por usuario'
description: 'Lync Server 2013: asignar una directiva de ubicación para cada usuario.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user location policy
ms:assetid: 343f2de3-a0ae-4403-8456-6e520b579d32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520974(v=OCS.15)
ms:contentKeyID: 48183794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81631740e0a6c908c392ccacb6b37d7033d9224c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443219"
---
# <a name="assign-a-per-user-location-policy-in-lync-server-2013"></a><span data-ttu-id="d4e2f-103">Asignar una directiva de ubicación por usuario en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4e2f-103">Assign a per-user location policy in Lync Server 2013</span></span>

 


<span data-ttu-id="d4e2f-104">La Directiva de ubicación es una de las configuraciones individuales de una cuenta de usuario que puede configurar en el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-104">The location policy is one of the individual settings of a user account that you can configure in the Lync Server Control Panel.</span></span>

<span data-ttu-id="d4e2f-105">Implementar una o más directivas de ubicación para cada usuario es opcional.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-105">Deploying one or more per-user location policies is optional.</span></span> <span data-ttu-id="d4e2f-106">También puede implementar una directiva de ubicación global o una directiva de ubicación de nivel de subred.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-106">You can also deploy only a global-level location policy or subnet-level location policy.</span></span> <span data-ttu-id="d4e2f-107">Si implementa directivas por usuario, es preciso que las asigne explícitamente a un objeto de usuario, grupo o contacto.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-107">If you do deploy per-user policies, you must explicitly assign them to users, groups, or contact object.</span></span> <span data-ttu-id="d4e2f-108">La configuración mejorada de 9-1-1 (E9-1-1) se asigna de forma predeterminada a los valores definidos en la Directiva de ubicación global cuando no se ha asignado ninguna directiva específica de subred o de usuario.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-108">Enhanced 9-1-1 (E9-1-1) settings automatically default to those defined in the global-level location policy when no specific subnet-level or per-user policy is assigned.</span></span>

<span data-ttu-id="d4e2f-109">Después de crear al menos una directiva de ubicación por usuario, use los procedimientos de este tema para asignar a la Directiva que especifica la configuración que quiere que el servidor aplique para las llamadas de emergencia realizadas por un usuario en particular.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-109">After creating at least one per-user location policy, use the procedures in this topic to assign to the policy that specifies the settings that you want the server to apply for emergency calls placed by a particular user.</span></span>

<span data-ttu-id="d4e2f-110">Para obtener una lista de todas las opciones de configuración de la Directiva de ubicación disponibles, consulte [definir la Directiva de ubicación de Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="d4e2f-110">For a list of all available location policy settings, see [Defining the location policy for Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span></span>

<span data-ttu-id="d4e2f-111">Para obtener detalles sobre la creación de directivas de ubicación, consulte [crear directivas de ubicación en Lync Server 2013](lync-server-2013-create-location-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d4e2f-111">For details about creating location policies, see [Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md).</span></span>

## <a name="to-assign-a-per-user-location-policy-with-the-lync-server-control-panel"></a><span data-ttu-id="d4e2f-112">Para asignar una directiva de ubicación por usuario con el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="d4e2f-112">To assign a per-user location policy with the Lync Server Control Panel</span></span>

1.  <span data-ttu-id="d4e2f-113">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d4e2f-114">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d4e2f-115">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d4e2f-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d4e2f-116">En la barra de navegación izquierda, haga clic en **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-116">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="d4e2f-117">Use uno de los métodos siguientes para encontrar a un usuario:</span><span class="sxs-lookup"><span data-stu-id="d4e2f-117">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="d4e2f-118">En el cuadro **Buscar usuarios**, escriba la primera porción del nombre para mostrar, el nombre, los apellidos, el nombre de la cuenta del Administrador de cuentas de seguridad (SAM), la dirección SIP o el identificador uniforme de recursos (URI) de la cuenta de usuario y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-118">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="d4e2f-119">Si ha guardado una consulta, haga clic en el icono **Abrir consulta**, use el cuadro de diálogo **Abrir** para recuperar la consulta (un archivo .usf) y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-119">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="d4e2f-120">(Opcional) Especificar criterios de búsqueda adicionales para restringir los resultados:</span><span class="sxs-lookup"><span data-stu-id="d4e2f-120">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="d4e2f-121">Haga clic en **Agregar filtro**.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-121">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="d4e2f-122">Especifique la propiedad de usuario. Para ello, escríbala o haga clic en la flecha de la lista desplegable para seleccionar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-122">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="d4e2f-123">En la lista desplegable **Igual a**, haga clic en el operador (por ejemplo, **Igual a** o **No igual a**).</span><span class="sxs-lookup"><span data-stu-id="d4e2f-123">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="d4e2f-124">En función de la propiedad de usuario que haya seleccionado, especifique los criterios que desee utilizar para filtrar los resultados de búsqueda escribiendo o haciendo clic en la flecha de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-124">Depending on the user property you selected, enter the criteria you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="d4e2f-125">Para agregar cláusulas de búsqueda adicionales a la consulta, haga clic en <STRONG>Agregar filtro</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-125">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

    
    5.  <span data-ttu-id="d4e2f-126">Haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-126">Click **Find**.</span></span>

6.  <span data-ttu-id="d4e2f-127">Haga clic en un usuario en los resultados de búsqueda, haga clic en **Acción** y, a continuación, en **Asignar directivas**.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-127">Click a user in the search results, click **Action**, and then click **Assign policies**.</span></span>
    

    > [!TIP]  
    > <span data-ttu-id="d4e2f-128">Si desea aplicar la misma directiva de ubicación por usuario a varios usuarios, seleccione varios usuarios en los resultados de búsqueda, haga clic en <STRONG>acciones</STRONG>y, a continuación, haga clic en <STRONG>asignar directivas</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-128">If you want the same per-user location policy to apply to multiple users, select multiple users in the search results, then click <STRONG>Actions</STRONG>, and then click <STRONG>Assign policies</STRONG>.</span></span>



7.  <span data-ttu-id="d4e2f-129">En **asignar directivas**, en **Directiva de ubicación**, realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="d4e2f-129">In **Assign Policies**, under **Location policy**, do one of the following:</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="d4e2f-130">Puesto que existen varias directivas que puede configurar mediante el cuadro de diálogo <STRONG>asignar directivas</STRONG> , la opción <STRONG> &lt; &gt; mantener</STRONG> está seleccionada de forma predeterminada para todas las directivas del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-130">Because there are multiple policies that you can configure by using the <STRONG>Assign Policies</STRONG> dialog box, <STRONG>&lt;Keep as is&gt;</STRONG> is selected by default for every policy in the dialog box.</span></span> <span data-ttu-id="d4e2f-131">Para seguir usando la directiva asignada anteriormente al usuario, no efectúe cambios en esta configuración.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-131">Continue using the policy previously assigned to the user by making no changes to this setting.</span></span>

    
      - <span data-ttu-id="d4e2f-132">Permita Lync Server 2013 para elegir automáticamente la Directiva de nivel global o, si está definida, la Directiva de nivel de subred.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-132">Allow Lync Server 2013 to automatically choose either the global-level policy or, if defined, the subnet-level policy.</span></span>
    
      - <span data-ttu-id="d4e2f-133">Haga clic en el nombre de una directiva de ubicación por usuario que haya definido previamente ejecutando el cmdlet **New-CsLocationPolicy** .</span><span class="sxs-lookup"><span data-stu-id="d4e2f-133">Click the name of a per-user location policy you previously defined by running the **New-CsLocationPolicy** cmdlet.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="d4e2f-134">Para ayudarle a decidir la Directiva que desea asignar, después de hacer clic en un nombre de Directiva, haga clic en <STRONG>Ver</STRONG> para ver los derechos de usuario y permisos definidos en la Directiva.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-134">To help you decide the policy that you want to assign, after you click a policy name, click <STRONG>View</STRONG> to view the user rights and permissions defined in the policy.</span></span>



8.  <span data-ttu-id="d4e2f-135">Cuando haya terminado, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-135">When you are finished, click **OK**.</span></span>

## <a name="assigning-a-per-user-location-policy-by-using-lync-server-management-shell-cmdlets"></a><span data-ttu-id="d4e2f-136">Asignar una directiva de ubicación de Per-User mediante los cmdlets del shell de administración de Lync Server</span><span class="sxs-lookup"><span data-stu-id="d4e2f-136">Assigning a Per-User Location Policy by Using Lync Server Management Shell Cmdlets</span></span>

<span data-ttu-id="d4e2f-137">Puede asignar directivas de ubicación por usuario mediante el cmdlet Grant-CsLocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-137">You can assign per-user location policies by using the Grant-CsLocationPolicy cmdlet.</span></span> <span data-ttu-id="d4e2f-138">Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-138">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d4e2f-139">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="d4e2f-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-location-policy-to-a-single-user"></a><span data-ttu-id="d4e2f-140">Para asignar una directiva de ubicación por usuario a un solo usuario</span><span class="sxs-lookup"><span data-stu-id="d4e2f-140">To assign a per-user location policy to a single user</span></span>

  - <span data-ttu-id="d4e2f-141">El comando siguiente asigna la Directiva de ubicación por usuario RedmondLocationPolicy al usuario Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-141">The following command assigns the per-user location policy RedmondLocationPolicy to the user Ken Myer.</span></span>
    
        Grant-CsLocationPolicy -Identity "Ken Myer" -PolicyName "RedmondLocationPolicy"

## <a name="to-assign-a-per-user-location-policy-to-multiple-users"></a><span data-ttu-id="d4e2f-142">Para asignar una directiva de ubicación por usuario a varios usuarios</span><span class="sxs-lookup"><span data-stu-id="d4e2f-142">To assign a per-user location policy to multiple users</span></span>

  - <span data-ttu-id="d4e2f-143">Este comando asigna la Directiva de ubicación por usuario AccountingDepartmentLocationPolicy a todos los usuarios que trabajan para el Departamento de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-143">This command assigns the per-user location policy AccountingDepartmentLocationPolicy to all the users who work for the Accounting department.</span></span> <span data-ttu-id="d4e2f-144">Para obtener más información sobre el parámetro LdapFilter que se usa en este comando, consulte la documentación del cmdlet [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="d4e2f-144">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "Department=Accounting" | Grant-CsLocationPolicy -PolicyName "AccountingDepartmentLocationPolicy"

## <a name="to-unassign-a-per-user-location-policy"></a><span data-ttu-id="d4e2f-145">Para cancelar la asignación de una directiva de ubicación por usuario</span><span class="sxs-lookup"><span data-stu-id="d4e2f-145">To unassign a per-user location policy</span></span>

  - <span data-ttu-id="d4e2f-146">El comando siguiente elimina la asignación de cualquier directiva de ubicación por usuario asignada previamente a Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-146">The following command unassigns any per-user location policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="d4e2f-147">Después de quitar la asignación de la directiva por usuario, se usará automáticamente la directiva global o la directiva del sitio local, si existe, para administrar a Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-147">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="d4e2f-148">La directiva de sitio tiene prioridad sobre la directiva global.</span><span class="sxs-lookup"><span data-stu-id="d4e2f-148">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsLocationPolicy -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="d4e2f-149">Para obtener más información, consulte el tema de ayuda para el cmdlet [Grant-CsLocationPolicy](https://technet.microsoft.com/library/gg413049\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="d4e2f-149">For more information, see the help topic for the [Grant-CsLocationPolicy](https://technet.microsoft.com/library/gg413049\(v=ocs.15\)) cmdlet.</span></span>

