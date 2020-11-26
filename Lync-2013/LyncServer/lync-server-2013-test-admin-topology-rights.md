---
title: 'Lync Server 2013: derechos de topología de administración de pruebas'
description: 'Lync Server 2013: derechos de topología de administración de pruebas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test admin topology rights
ms:assetid: 0c03b7fd-449a-47ad-8263-ce811164cbce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767943(v=OCS.15)
ms:contentKeyID: 63969575
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22d713297d0e944c7acbc5efcb11b21ea1b26639
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441280"
---
# <a name="test-admin-topology-rights-in-lync-server-2013"></a><span data-ttu-id="5ca66-103">Probar los derechos de topología de administración en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ca66-103">Test admin topology rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5ca66-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5ca66-104">

<span> </span></span></span>

<span data-ttu-id="5ca66-105">_**Última modificación del tema:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="5ca66-105">_**Topic Last Modified:** 2016-12-08_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ca66-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="5ca66-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="5ca66-107">Después de la implementación inicial de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5ca66-107">After initial Lync Server deployment.</span></span> <span data-ttu-id="5ca66-108">Según sea necesario, si surgen problemas relacionados con los permisos.</span><span class="sxs-lookup"><span data-stu-id="5ca66-108">As needed if permission-related issues arise.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ca66-109">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="5ca66-109">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="5ca66-110">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ca66-110">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ca66-111">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="5ca66-111">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="5ca66-112">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="5ca66-112">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="5ca66-113">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsSetupPermission.</span><span class="sxs-lookup"><span data-stu-id="5ca66-113">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="5ca66-114">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5ca66-114">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsSetupPermission&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="5ca66-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ca66-115">Description</span></span>

<span data-ttu-id="5ca66-116">De forma predeterminada, solo los administradores de dominio pueden habilitar una topología de Lync Server y realizar cambios importantes en la infraestructura de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5ca66-116">By default, only domain administrators can enable a Lync Server topology and make large changes to the Lync Server infrastructure.</span></span> <span data-ttu-id="5ca66-117">Esto no será un problema siempre que los administradores de dominio y los administradores de Lync Server sean uno y el mismo. En muchas organizaciones, los administradores de Lync Server no mantienen derechos administrativos en todo el dominio.</span><span class="sxs-lookup"><span data-stu-id="5ca66-117">This won't be a problem as long as your domain administrators and your Lync Server administrators are one and the same.In many organizations Lync Server administrators do not hold administrative rights to the whole domain.</span></span> <span data-ttu-id="5ca66-118">De forma predeterminada, eso significa que estos administradores (definidos como miembros del grupo RTCUniversalServerAdmins) no pueden hacer cambios en la topología de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5ca66-118">By default, that means that these administrators (defined as members of the RTCUniversalServerAdmins group) can't make Lync Server topology changes.</span></span> <span data-ttu-id="5ca66-119">Para conceder a los miembros del grupo RTCUniversalServerAdmins el derecho de realizar cambios de topología, debe asignar los permisos necesarios de Active Directory mediante el cmdlet [Grant-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission) .</span><span class="sxs-lookup"><span data-stu-id="5ca66-119">To give members of the RTCUniversalServerAdmins group the right to make topology changes, you must assign the required Active Directory permissions by using the [Grant-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission) cmdlet.</span></span>

<span data-ttu-id="5ca66-120">El cmdlet Test-CsSetupPermission comprueba que los permisos necesarios para instalar Lync Server o uno de sus componentes están configurados en el contenedor de Active Directory especificado.</span><span class="sxs-lookup"><span data-stu-id="5ca66-120">The Test-CsSetupPermission cmdlet verifies that the required permissions that are needed to install Lync Server or one of its components are configured on the specified Active Directory container.</span></span> <span data-ttu-id="5ca66-121">Si no se asignan los permisos, puede ejecutar el cmdlet Grant-CsSetupPermission para conceder a los miembros del grupo RTCUniversalServerAdmins el derecho de instalar y habilitar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5ca66-121">If the permissions are not assigned, you can then run the Grant-CsSetupPermission cmdlet to give members of the RTCUniversalServerAdmins group the right to install and enable Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5ca66-122">Para obtener una lista detallada de los permisos asignados por Grant-CsSetupPermission, consulte la entrada de blog <A href="https://blogs.technet.com/b/jenstr/archive/2011/02/07/grant-cssetuppermission-and-grant-csoupermission.aspx">Grant-CsSetupPermission y Grant-CsOUPermission</A>.</span><span class="sxs-lookup"><span data-stu-id="5ca66-122">For a detailed list of permissions assigned by Grant-CsSetupPermission, see the blog post <A href="https://blogs.technet.com/b/jenstr/archive/2011/02/07/grant-cssetuppermission-and-grant-csoupermission.aspx">Grant-CsSetupPermission and Grant-CsOUPermission</A>.</span></span>



</div>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="5ca66-123">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="5ca66-123">Running the test</span></span>

<span data-ttu-id="5ca66-124">Para determinar si los permisos de configuración se asignan a un contenedor de Active Directory, llame al cmdlet Test-CsSetupPermission.</span><span class="sxs-lookup"><span data-stu-id="5ca66-124">To determine whether setup permissions are assigned for an Active Directory container, call the Test-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="5ca66-125">Especifique el nombre distintivo del contenedor que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="5ca66-125">Specify the distinguished name of the container to be checked.</span></span> <span data-ttu-id="5ca66-126">Por ejemplo, este comando comprueba los permisos de configuración en el contenedor ou = CsServers, DC = litwareinc, DC = com:</span><span class="sxs-lookup"><span data-stu-id="5ca66-126">For example, this command verifies setup permissions on the container ou=CsServers,dc=litwareinc,dc=com:</span></span>

    Test-CsSetupPermission -ComputerOU "ou=CsServers,dc=litwareinc,dc=com"

<span data-ttu-id="5ca66-127">Para obtener más información, vea el tema de ayuda para el cmdlet [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) .</span><span class="sxs-lookup"><span data-stu-id="5ca66-127">For more information, see the help topic for the [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="5ca66-128">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="5ca66-128">Determining success or failure</span></span>

<span data-ttu-id="5ca66-129">Si Test-CsSetupPermission determina que los permisos necesarios ya se han establecido en un contenedor de Active Directory, el cmdlet devolverá el valor true:</span><span class="sxs-lookup"><span data-stu-id="5ca66-129">If Test-CsSetupPermission determines that the required permissions have already been set on an Active Directory container then the cmdlet will return the value True:</span></span>

<span data-ttu-id="5ca66-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5ca66-130">True</span></span>

<span data-ttu-id="5ca66-131">Si no se establecen permisos, Test-CsSetupPermission devolverá el valor false.</span><span class="sxs-lookup"><span data-stu-id="5ca66-131">If permissions are not set, Test-CsSetupPermission will return the value False.</span></span> <span data-ttu-id="5ca66-132">Ten en cuenta que este valor normalmente se incluirá en muchos mensajes de advertencia.</span><span class="sxs-lookup"><span data-stu-id="5ca66-132">Note that this value will typically be enclosed in many warning messages.</span></span> <span data-ttu-id="5ca66-133">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5ca66-133">For example:</span></span>

<span data-ttu-id="5ca66-134">ADVERTENCIA: entrada de control de acceso (ACE) ATL-CS-001 \\ RTCUniversalServerAdmins; Permitir ExtendedRight; Nada Nada 1131f6aa-9c07-11d1-f79f-00c04fc2dcd2</span><span class="sxs-lookup"><span data-stu-id="5ca66-134">WARNING: Access control entry (ACE) atl-cs-001\\RTCUniversalServerAdmins; Allow; ExtendedRight; None; None; 1131f6aa-9c07-11d1-f79f-00c04fc2dcd2</span></span>

<span data-ttu-id="5ca66-135">ADVERTENCIA: las entradas de control de acceso (ACE) del objeto "CN = Computers, DC = litwareinc, DC = com" no están listas.</span><span class="sxs-lookup"><span data-stu-id="5ca66-135">WARNING: The access control entries (ACEs) on the object "CN=Computers,DC=litwareinc,DC=com" are not ready.</span></span>

<span data-ttu-id="5ca66-136">Falso</span><span class="sxs-lookup"><span data-stu-id="5ca66-136">False</span></span>

<span data-ttu-id="5ca66-137">ADVERTENCIA: el procesamiento de "prueba-CsSetupPermission" se completó con advertencias.</span><span class="sxs-lookup"><span data-stu-id="5ca66-137">WARNING: "Test-CsSetupPermission" processing has completed with warnings.</span></span> <span data-ttu-id="5ca66-138">durante esta ejecución, se grabaron "2" advertencias.</span><span class="sxs-lookup"><span data-stu-id="5ca66-138">"2" warnings were recorded during this run.</span></span>

<span data-ttu-id="5ca66-139">ADVERTENCIA: los resultados detallados se encuentran en "C: \\ users \\ admin \\ \\ local \\ temp \\Test-CsSetupPermission-1da99ba6-abe2-45e4-8b16-dfd244763118.html".</span><span class="sxs-lookup"><span data-stu-id="5ca66-139">WARNING: Detailed results can be found at "C:\\Users\\Admin\\AppData\\Local\\Temp\\Test-CsSetupPermission-1da99ba6-abe2-45e4-8b16-dfd244763118.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="5ca66-140">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="5ca66-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="5ca66-141">Aunque hay raras excepciones, si Test-CsSetupPermission se produce un error que normalmente significa que los permisos de configuración no se asignan al contenedor de Active Directory especificado.</span><span class="sxs-lookup"><span data-stu-id="5ca66-141">Although there are rare exceptions, if Test-CsSetupPermission fails that typically means that setup permissions are not assigned for the specified Active Directory container.</span></span> <span data-ttu-id="5ca66-142">Esos permisos se pueden asignar mediante el cmdlet Grant-CsSetupPermission.</span><span class="sxs-lookup"><span data-stu-id="5ca66-142">Those permissions can be assigned by using the Grant-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="5ca66-143">Por ejemplo, este comando concede permisos de configuración al contenedor Computers del dominio litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="5ca66-143">For example, this command grants setup permissions to the Computers container in the domain litwareinc.com:</span></span>

    Grant-CsSetupPermission -ComputerOU "cn=Computers,dc=litwareinc,dc=com"

<span data-ttu-id="5ca66-144">Para obtener más información, vea el tema de ayuda para el cmdlet [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) .</span><span class="sxs-lookup"><span data-stu-id="5ca66-144">For more information, see the help topic for the [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet.</span></span>

<span data-ttu-id="5ca66-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5ca66-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

