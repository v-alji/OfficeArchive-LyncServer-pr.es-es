---
title: 'Lync Server 2013: probar la activación del servicio y los permisos de grupo'
description: 'Lync Server 2013: probar la activación del servicio y los permisos de grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing service activation and group permissions
ms:assetid: 2c59e603-ba85-40ba-91a7-51c6fd39472e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743833(v=OCS.15)
ms:contentKeyID: 63969594
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 116cf939f3110616ce395eb14c7945890bdb89b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440986"
---
# <a name="testing-service-activation-and-group-permissions-in-lync-server-2013"></a><span data-ttu-id="372c4-103">Probar la activación de servicios y los permisos de grupo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="372c4-103">Testing service activation and group permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="372c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="372c4-104">

<span> </span></span></span>

<span data-ttu-id="372c4-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="372c4-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="372c4-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="372c4-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="372c4-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="372c4-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="372c4-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="372c4-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="372c4-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="372c4-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="372c4-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="372c4-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="372c4-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="372c4-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="372c4-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="372c4-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsTopology cmdlet.</span></span> <span data-ttu-id="372c4-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="372c4-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsTopology&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="372c4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="372c4-114">Description</span></span>

<span data-ttu-id="372c4-115">El cmdlet Test-CsTopology le permite comprobar si Lync Server 2013 está funcionando correctamente en un ámbito global.</span><span class="sxs-lookup"><span data-stu-id="372c4-115">The Test-CsTopology cmdlet enables you to verify that Lync Server 2013 is functioning correctly at a global scope.</span></span> <span data-ttu-id="372c4-116">De forma predeterminada, el cmdlet comprueba toda la infraestructura de Lync Server, verifica que los servicios necesarios se estén ejecutando y que se hayan establecido los permisos adecuados para estos servicios y para los grupos de seguridad universal que se crean al instalar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="372c4-116">By default, the cmdlet checks your whole Lync Server infrastructure, verifying that the required services are running and that the appropriate permissions are set for these services and for the universal security groups that are created when you install Lync Server.</span></span>

<span data-ttu-id="372c4-117">Además de comprobar la validez de la instalación de Lync Server, Test-CsTopology también le permite comprobar la validez de un servicio específico.</span><span class="sxs-lookup"><span data-stu-id="372c4-117">In addition to verifying the validity of the Lync Server installation, Test-CsTopology also lets you check the validity of a specific service.</span></span> <span data-ttu-id="372c4-118">Por ejemplo, este comando comprueba el estado del servidor de conferencia A/V en el grupo atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="372c4-118">For example, this command checks the state of the A/V Conferencing Server on the pool atl-cs-001.litwareinc.com:</span></span>

    Test-CsTopology -Service "ConferencingServer:atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="372c4-119">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="372c4-119">Running the test</span></span>

<span data-ttu-id="372c4-120">De forma predeterminada, Test-CsTopology muestra muy pocos resultados en pantalla.</span><span class="sxs-lookup"><span data-stu-id="372c4-120">By default, Test-CsTopology displays very little output on-screen.</span></span> <span data-ttu-id="372c4-121">En su lugar, la información devuelta por el cmdlet se escribe en un archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="372c4-121">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="372c4-122">El parámetro de informe le permite especificar una ruta de acceso y un nombre de archivo para el archivo HTML generado por test-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="372c4-122">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsTopology.</span></span> <span data-ttu-id="372c4-123">Si no incluye el parámetro de informe, el archivo HTML se guardará automáticamente en la carpeta usuarios y recibirá un nombre parecido a este: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span><span class="sxs-lookup"><span data-stu-id="372c4-123">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="372c4-124">El siguiente comando de ejemplo se ejecuta Test-CsTopology y guarda el resultado en un archivo denominado C: \\ Logs \\ComputerTest.html:</span><span class="sxs-lookup"><span data-stu-id="372c4-124">The following sample command runs Test-CsTopology and saves the output to a file that is named C:\\Logs\\ComputerTest.html:</span></span>

    Test-CsTopology -Report "C:\Logs\ComputerTest.html" -Verbose

<span data-ttu-id="372c4-125">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) .</span><span class="sxs-lookup"><span data-stu-id="372c4-125">For more information, see the Help documentation for the [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="372c4-126">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="372c4-126">Determining success or failure</span></span>

<span data-ttu-id="372c4-127">A diferencia de la mayoría de los cmdlets de prueba, Test-CsTopology informa de que ha tenido éxito o ha fallado.</span><span class="sxs-lookup"><span data-stu-id="372c4-127">Unlike most of the test cmdlets, Test-CsTopology does report back Success or Failure.</span></span> <span data-ttu-id="372c4-128">En parte, esto se debe a la gran cantidad de comprobaciones de comprobación que el cmdlet debe hacer cada vez que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="372c4-128">In part, that’s due to the large number of verification checks that the cmdlet must make every time that it runs.</span></span> <span data-ttu-id="372c4-129">En su lugar, los datos se guardan en un informe HTML que se puede ver en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="372c4-129">Instead, data is saved to an HTML report that can then be viewed by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="372c4-130">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="372c4-130">Reasons why the test might have failed</span></span>

<span data-ttu-id="372c4-131">Estas son algunas de las razones comunes por las que Test-CsTopology puede dar error:</span><span class="sxs-lookup"><span data-stu-id="372c4-131">Here are some common reasons why Test-CsTopology might fail:</span></span>

  - <span data-ttu-id="372c4-132">Es posible que la replicación no esté actualizada en el equipo de prueba.</span><span class="sxs-lookup"><span data-stu-id="372c4-132">Replication might not be up-to-date on the test computer.</span></span> <span data-ttu-id="372c4-133">Para comprobar el estado de replicación actual de un equipo, ejecute el cmdlet Get-CsManagementStoreReplicationStatus:</span><span class="sxs-lookup"><span data-stu-id="372c4-133">You can check the current replication status for a computer by running the Get-CsManagementStoreReplicationStatus cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="372c4-134">Si el estado de replicación no está actualizado, puede forzar la replicación de forma manual con un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="372c4-134">If the replication status is not up-to-date, you can manually force replication to occur by using a command similar to this:</span></span>
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - <span data-ttu-id="372c4-135">Es posible que se deba habilitar la topología.</span><span class="sxs-lookup"><span data-stu-id="372c4-135">The topology might have to be enabled.</span></span> <span data-ttu-id="372c4-136">Si cambia la topología de Lync Server (cambios que pueden afectar al equipo local), debe habilitar la nueva topología.</span><span class="sxs-lookup"><span data-stu-id="372c4-136">If you change the Lync Server topology (changes that might affect the local computer), then you must enable the new topology.</span></span> <span data-ttu-id="372c4-137">Puede habilitar la topología en cualquier momento ejecutando este comando:</span><span class="sxs-lookup"><span data-stu-id="372c4-137">You can enable the topology at any time by running this command:</span></span>
    
        Enable-CsTopology

<span data-ttu-id="372c4-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="372c4-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

