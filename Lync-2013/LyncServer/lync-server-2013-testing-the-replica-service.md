---
title: 'Lync Server 2013: probar el servicio de réplicas'
description: 'Lync Server 2013: prueba del servicio de réplicas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the replica service
ms:assetid: 4ff2cc91-0036-4c5a-9792-7bf43d8ce18d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727303(v=OCS.15)
ms:contentKeyID: 63969600
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a61751b95115da3d6519f20f52262b7159ffcbfe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440979"
---
# <a name="testing-the-replica-service-in-lync-server-2013"></a><span data-ttu-id="b2429-103">Probar el servicio de réplicas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2429-103">Testing the replica service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2429-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2429-104">

<span> </span></span></span>

<span data-ttu-id="b2429-105">_**Última modificación del tema:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="b2429-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2429-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="b2429-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="b2429-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="b2429-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2429-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="b2429-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="b2429-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b2429-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2429-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="b2429-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="b2429-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="b2429-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="b2429-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe asignar un rol de RBAC que tenga permiso para ejecutar el cmdlet <strong>Test-CsReplica</strong> .</span><span class="sxs-lookup"><span data-stu-id="b2429-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsReplica</strong> cmdlet.</span></span> <span data-ttu-id="b2429-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b2429-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsReplica&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b2429-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2429-114">Description</span></span>

<span data-ttu-id="b2429-115">El cmdlet **Test-CsReplica** verifica que el servicio de réplica de Lync Server 2013 se esté ejecutando en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="b2429-115">The **Test-CsReplica** cmdlet verifies that the Lync Server 2013 replica service is running on the local computer.</span></span> <span data-ttu-id="b2429-116">El cmdlet **Test-CsReplica** realiza estas tareas como:</span><span class="sxs-lookup"><span data-stu-id="b2429-116">The **Test-CsReplica** cmdlet performs such tasks as:</span></span>

  - <span data-ttu-id="b2429-117">comprobar el estado del agente de replicación y los servicios de agente de registro centralizados</span><span class="sxs-lookup"><span data-stu-id="b2429-117">checking the status of the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="b2429-118">comprobando que los puertos necesarios se abrieron en el Firewall de Windows</span><span class="sxs-lookup"><span data-stu-id="b2429-118">verifying that the required ports were opened in the Windows Firewall</span></span>

  - <span data-ttu-id="b2429-119">asegurándose de que existen los grupos de seguridad de Active Directory y de equipo local necesarios.</span><span class="sxs-lookup"><span data-stu-id="b2429-119">making sure that the necessary Active Directory and local computer security groups exist.</span></span>

<span data-ttu-id="b2429-120">Ten en cuenta que este cmdlet debe ejecutarse de forma local.</span><span class="sxs-lookup"><span data-stu-id="b2429-120">Note that this cmdlet must be run locally.</span></span> <span data-ttu-id="b2429-121">Es decir, debe ejecutarse en el mismo equipo en el que se ejecuta el servicio de réplicas.</span><span class="sxs-lookup"><span data-stu-id="b2429-121">That is, it must be run on the same computer where the replica service is running.</span></span> <span data-ttu-id="b2429-122">No hay opciones para ejecutar el cmdlet **Test-CsReplica** en un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="b2429-122">There are no options for running the **Test-CsReplica** cmdlet against a remote server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b2429-123">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="b2429-123">Running the test</span></span>

<span data-ttu-id="b2429-124">El comando que se muestra en el ejemplo 1 prueba el servicio de réplica de 2013 de Lync Server en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="b2429-124">The command shown in Example 1 tests the Lync Server 2013 replica service on the local computer.</span></span> <span data-ttu-id="b2429-125">En este ejemplo, el parámetro verbose se usa para garantizar que se muestra en pantalla la información sobre la prueba, incluido el error eventual o el éxito de la prueba y la ubicación del informe generado por la prueba.</span><span class="sxs-lookup"><span data-stu-id="b2429-125">In this example the Verbose parameter is used to guarantee that information about the test – including the eventual failure or success of the test and the location of the report generated by the test – is displayed on screen.</span></span>

    Test-CsReplica -Verbose

<span data-ttu-id="b2429-126">El ejemplo 2 es una variación del comando que se muestra en el ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="b2429-126">Example 2 is a variation of the command shown in Example 1.</span></span> <span data-ttu-id="b2429-127">En este caso, el parámetro de informe se incluye para especificar una ruta de acceso y un nombre de carpeta para el informe generado por la prueba.</span><span class="sxs-lookup"><span data-stu-id="b2429-127">In this case, the Report parameter is included to specify a folder path and name for the report generated by the test.</span></span> <span data-ttu-id="b2429-128">Si no especifica una ruta de acceso al informe, se le proporcionará un nombre generado automáticamente de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b2429-128">If you do not specify a report path the report will be given an auto-generated name similar to this:</span></span>

<span data-ttu-id="b2429-129">C: \\ Administrador de usuarios \\ . litwareinc \\ AppData \\ local \\ temporal \\ 1 \\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span><span class="sxs-lookup"><span data-stu-id="b2429-129">C:\\Users\\Administrator.Litwareinc\\AppData\\Local\\Temp\\1\\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span></span>

    Test-CsReplica -Verbose -Report C:\Logs\ReplicaTest.html

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b2429-130">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="b2429-130">Determining success or failure</span></span>

<span data-ttu-id="b2429-131">Inserte el cuerpo de la sección aquí.</span><span class="sxs-lookup"><span data-stu-id="b2429-131">Insert section body here.</span></span>

<span data-ttu-id="b2429-132">VERBOse: crear un nuevo archivo de registro "C: \\ usuarios \\ probando \\ AppData \\ \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml temporal local \\ ".</span><span class="sxs-lookup"><span data-stu-id="b2429-132">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="b2429-133">VERBOse: crear un nuevo archivo de registro "C: \\ usuarios \\ probando \\ AppData \\ \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml temporal local \\ ".</span><span class="sxs-lookup"><span data-stu-id="b2429-133">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="b2429-134">VERBOse: el procesamiento de "prueba-CsReplica" se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2429-134">VERBOSE: "Test-CsReplica" processing has completed successfully.</span></span>

<span data-ttu-id="b2429-135">VERBOse puede encontrar los resultados detallados en "C: \\ usuarios \\ prueban \\ AppData \\ local \\ temp \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span><span class="sxs-lookup"><span data-stu-id="b2429-135">VERBOSE: Detailed results can be found at "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="b2429-136">VERBOse: crear un nuevo archivo de registro</span><span class="sxs-lookup"><span data-stu-id="b2429-136">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="b2429-137">"C: \\ usuarios \\ prueba \\ AppData \\ local \\ temporal \\ 2 \\ prueba-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="b2429-137">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="b2429-138">d3bd0e4a083.xml ".</span><span class="sxs-lookup"><span data-stu-id="b2429-138">d3bd0e4a083.xml".</span></span>

<span data-ttu-id="b2429-139">VERBOse: crear un nuevo archivo de registro</span><span class="sxs-lookup"><span data-stu-id="b2429-139">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="b2429-140">"C: \\ usuarios \\ prueba \\ AppData \\ local \\ temporal \\ 2 \\ prueba-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="b2429-140">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="b2429-141">d3bd0e4a083.html ".</span><span class="sxs-lookup"><span data-stu-id="b2429-141">d3bd0e4a083.html".</span></span>

<span data-ttu-id="b2429-142">ADVERTENCIA: error de Test-CsReplica.</span><span class="sxs-lookup"><span data-stu-id="b2429-142">WARNING: Test-CsReplica failed.</span></span>

<span data-ttu-id="b2429-143">ADVERTENCIA: puede encontrar resultados detallados en</span><span class="sxs-lookup"><span data-stu-id="b2429-143">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="b2429-144">"C: \\ usuarios \\ prueba \\ AppData \\ local \\ temporal \\ 2 \\ prueba-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="b2429-144">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="b2429-145">d3bd0e4a083.html ".</span><span class="sxs-lookup"><span data-stu-id="b2429-145">d3bd0e4a083.html".</span></span>

<span data-ttu-id="b2429-146">Test-CsReplica: error al ejecutar el comando: el acceso al registro solicitado no es</span><span class="sxs-lookup"><span data-stu-id="b2429-146">Test-CsReplica : Command execution failed: Requested registry access is not</span></span>

<span data-ttu-id="b2429-147">tienen.</span><span class="sxs-lookup"><span data-stu-id="b2429-147">allowed.</span></span>

<span data-ttu-id="b2429-148">En la línea: 1 carácter: 1</span><span class="sxs-lookup"><span data-stu-id="b2429-148">At line:1 char:1</span></span>

<span data-ttu-id="b2429-149">\+ Test-CsReplica: detallado</span><span class="sxs-lookup"><span data-stu-id="b2429-149">\+ Test-CsReplica -Verbose</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="b2429-150">\+ CategoryInfo: InvalidOperation: (:) \[ Prueba-CsReplica \] , seguridad</span><span class="sxs-lookup"><span data-stu-id="b2429-150">\+ CategoryInfo : InvalidOperation: (:) \[Test-CsReplica\], Security</span></span>

<span data-ttu-id="b2429-151">Excepción</span><span class="sxs-lookup"><span data-stu-id="b2429-151">Exception</span></span>

<span data-ttu-id="b2429-152">\+ FullyQualifiedErrorId: ProcessingFailed, Microsoft. RTC. Management. deploy</span><span class="sxs-lookup"><span data-stu-id="b2429-152">\+ FullyQualifiedErrorId : ProcessingFailed,Microsoft.Rtc.Management.Deploy</span></span>

<span data-ttu-id="b2429-153">asignaciones. TestReplicaCmdlet</span><span class="sxs-lookup"><span data-stu-id="b2429-153">ment.TestReplicaCmdlet</span></span>

<span data-ttu-id="b2429-154">Prueba de PS C: \\ usuarios \\\></span><span class="sxs-lookup"><span data-stu-id="b2429-154">PS C:\\Users\\Testing\></span></span>

<span data-ttu-id="b2429-155">PS C: \\ usuarios \\ probando \> Test-CsUcwaConference-TargetFqdn "LyncTest. SelfHost. Corp. M</span><span class="sxs-lookup"><span data-stu-id="b2429-155">PS C:\\Users\\Testing\> Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.M</span></span>

<span data-ttu-id="b2429-156">icrosoft.com "</span><span class="sxs-lookup"><span data-stu-id="b2429-156">icrosoft.com"</span></span>

<span data-ttu-id="b2429-157">ADVERTENCIA: no se pudo leer el número de puerto del registrador para el nombre completo</span><span class="sxs-lookup"><span data-stu-id="b2429-157">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="b2429-158">nombre de dominio (FQDN).</span><span class="sxs-lookup"><span data-stu-id="b2429-158">domain name (FQDN).</span></span> <span data-ttu-id="b2429-159">Usando el número de puerto predeterminado del registrador.</span><span class="sxs-lookup"><span data-stu-id="b2429-159">Using default Registrar port number.</span></span> <span data-ttu-id="b2429-160">Excepción</span><span class="sxs-lookup"><span data-stu-id="b2429-160">Exception:</span></span>

<span data-ttu-id="b2429-161">System. InvalidOperationException: no se encontró ningún clúster coincidente en la topología.</span><span class="sxs-lookup"><span data-stu-id="b2429-161">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="b2429-162">en</span><span class="sxs-lookup"><span data-stu-id="b2429-162">at</span></span>

<span data-ttu-id="b2429-163">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="b2429-163">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="b2429-164">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="b2429-164">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="b2429-165">Test-CsUcwaConference: no hay ningún usuario de prueba asignado para</span><span class="sxs-lookup"><span data-stu-id="b2429-165">Test-CsUcwaConference : There is no test user assigned for</span></span>

<span data-ttu-id="b2429-166">\[LyncTest.SelfHost.Corp.Microsoft.com \] .</span><span class="sxs-lookup"><span data-stu-id="b2429-166">\[LyncTest.SelfHost.Corp.Microsoft.com\].</span></span> <span data-ttu-id="b2429-167">Comprobar la configuración del usuario de prueba.</span><span class="sxs-lookup"><span data-stu-id="b2429-167">Verify test user configuration.</span></span>

<span data-ttu-id="b2429-168">En la línea: 1 carácter: 1</span><span class="sxs-lookup"><span data-stu-id="b2429-168">At line:1 char:1</span></span>

<span data-ttu-id="b2429-169">\+ Test-CsUcwaConference TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="b2429-169">\+ Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="b2429-170">\+ CategoryInfo: ResourceUnavailable: (:) \[ Prueba-CsUcwaConference\]</span><span class="sxs-lookup"><span data-stu-id="b2429-170">\+ CategoryInfo : ResourceUnavailable: (:) \[Test-CsUcwaConference\]</span></span>

<span data-ttu-id="b2429-171">, InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="b2429-171">, InvalidOperationException</span></span>

<span data-ttu-id="b2429-172">\+ FullyQualifiedErrorId: NotFoundTestUsers, Microsoft. RTC. Management. sintetizador</span><span class="sxs-lookup"><span data-stu-id="b2429-172">\+ FullyQualifiedErrorId : NotFoundTestUsers,Microsoft.Rtc.Management.Synth</span></span>

<span data-ttu-id="b2429-173">eticTransactions.TestUcwaConferenceCmdlet</span><span class="sxs-lookup"><span data-stu-id="b2429-173">eticTransactions.TestUcwaConferenceCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b2429-174">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="b2429-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="b2429-175">Estas son algunas de las razones comunes por las que **Test-CsReplica** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="b2429-175">Here are some common reasons why **Test-CsReplica** might fail:</span></span>

  - <span data-ttu-id="b2429-176">Es posible que haya un problema mayor con el agente de replicación y los servicios de agente de registro centralizados</span><span class="sxs-lookup"><span data-stu-id="b2429-176">There may be a larger problem with the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="b2429-177">Es posible que los puertos necesarios no estén abiertos en el Firewall de Windows</span><span class="sxs-lookup"><span data-stu-id="b2429-177">The required ports may not be open in the Windows Firewall</span></span>

  - <span data-ttu-id="b2429-178">Es posible que los grupos de seguridad de Active Directory y equipos locales necesarios no existan</span><span class="sxs-lookup"><span data-stu-id="b2429-178">The necessary Active Directory and local computer security groups may not exist</span></span>

<span data-ttu-id="b2429-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2429-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

