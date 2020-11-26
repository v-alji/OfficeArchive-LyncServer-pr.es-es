---
title: 'Lync Server 2013: probar la configuración de la base de datos'
description: 'Lync Server 2013: prueba de la configuración de la base de datos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing database configuration
ms:assetid: 60f7fcd2-5efe-4791-b159-b0f9bf39a41b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727307(v=OCS.15)
ms:contentKeyID: 63969606
ms.date: 07/07/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b9f88eee99c4a2d523cc84df401dcc1d7b9fe59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441042"
---
# <a name="testing-database-configuration-in-lync-server-2013"></a><span data-ttu-id="a9a40-103">Prueba de la configuración de bases de datos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9a40-103">Testing database configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a9a40-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a9a40-104">

<span> </span></span></span>

<span data-ttu-id="a9a40-105">_**Última modificación del tema:** 2016-07-07_</span><span class="sxs-lookup"><span data-stu-id="a9a40-105">_**Topic Last Modified:** 2016-07-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9a40-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="a9a40-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="a9a40-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="a9a40-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9a40-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="a9a40-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="a9a40-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a9a40-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9a40-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="a9a40-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="a9a40-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins y deben tener privilegios de administrador en SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a9a40-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group, and need to have Administrator privileges on the SQL server.</span></span></p>
<p><span data-ttu-id="a9a40-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe asignar un rol de RBAC que tenga permiso para ejecutar el cmdlet <strong>Test-CsDatabase</strong> .</span><span class="sxs-lookup"><span data-stu-id="a9a40-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsDatabase</strong> cmdlet.</span></span> <span data-ttu-id="a9a40-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a9a40-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDatabase&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="a9a40-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9a40-114">Description</span></span>

<span data-ttu-id="a9a40-115">El cmdlet **Test-CsDatabase** comprueba la conectividad a una o varias bases de datos de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a9a40-115">The **Test-CsDatabase** cmdlet verifies connectivity to one or more Lync Server 2013 databases.</span></span> <span data-ttu-id="a9a40-116">Cuando se ejecuta, el cmdlet **Test-CsDatabase** lee la topología de Lync Server, intenta conectarse a las bases de datos relevantes y, después, informa del éxito o error de cada intento.</span><span class="sxs-lookup"><span data-stu-id="a9a40-116">When run, the **Test-CsDatabase** cmdlet reads the Lync Server topology, attempts to connect to relevant databases, and then reports back the success or failure of each try.</span></span> <span data-ttu-id="a9a40-117">Si se puede establecer una conexión, el cmdlet también devolverá información como el nombre de la base de datos, la información de la versión de SQL Server y la ubicación de cualquier base de datos reflejada instalada.</span><span class="sxs-lookup"><span data-stu-id="a9a40-117">If a connection can be made, the cmdlet will also report back such information as the database name, SQL Server version information, and the location of any installed mirror databases.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="a9a40-118">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="a9a40-118">Running the test</span></span>

<span data-ttu-id="a9a40-119">El comando que se muestra en el ejemplo 1 comprueba la configuración de la base de datos de administración central.</span><span class="sxs-lookup"><span data-stu-id="a9a40-119">The command shown in Example 1 verifies the configuration of the Central Management database.</span></span>

    Test-CsDatabase -CentralManagementDatabase

<span data-ttu-id="a9a40-120">El ejemplo 2 verifica todas las bases de datos de Lync Server instaladas en el equipo atl-sql-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="a9a40-120">Example 2 verifies all the Lync Server databases installed on the computer atl-sql-001.litwareinc.com.</span></span>

    Test-CsDatabase -ConfiguredDatabases -SqlServerFqdn "atl-sql-001.litwareinc.com"

<span data-ttu-id="a9a40-121">En el ejemplo 3, la comprobación se realiza solo para la base de datos de archivado instalada en el equipo atl-sql-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="a9a40-121">In Example 3, verification is performed only for the Archiving database installed on the computer atl-sql-001.litwareinc.com.</span></span> <span data-ttu-id="a9a40-122">Ten en cuenta que el parámetro SqlInstanceName se incluye para especificar la instancia de SQL Server (Archinst) donde se encuentra la base de datos de archivado.</span><span class="sxs-lookup"><span data-stu-id="a9a40-122">Note that the SqlInstanceName parameter is included to specify the SQL Server instance (Archinst) where the Archiving database is located.</span></span>

    Test-CsDatabase -DatabaseType "Archiving" -SqlServerFqdn "atl-sql-001.litwareinc.com" -SqlInstanceName "archinst"

<span data-ttu-id="a9a40-123">El comando que se muestra en el ejemplo 4 comprueba las bases de datos instaladas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="a9a40-123">The command shown in Example 4 verifies the databases installed on the local computer.</span></span>

    Test-CsDatabase -LocalService

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="a9a40-124">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="a9a40-124">Determining success or failure</span></span>

<span data-ttu-id="a9a40-125">Si la conectividad de la base de datos está configurada correctamente, recibirá un resultado similar a este, con la propiedad Success marcada como **true**:</span><span class="sxs-lookup"><span data-stu-id="a9a40-125">If database connectivity is configured correctly, you'll receive output similar to this, with the Succeed property marked as **True**:</span></span>

<span data-ttu-id="a9a40-126">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a9a40-126">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="a9a40-127">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="a9a40-127">SqlInstanceName : rtc</span></span>

<span data-ttu-id="a9a40-128">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="a9a40-128">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="a9a40-129">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="a9a40-129">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="a9a40-130">NombreBasededatos: XDS</span><span class="sxs-lookup"><span data-stu-id="a9a40-130">DatabaseName : xds</span></span>

<span data-ttu-id="a9a40-131">Orígenes</span><span class="sxs-lookup"><span data-stu-id="a9a40-131">DataSource :</span></span>

<span data-ttu-id="a9a40-132">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="a9a40-132">SQLServerVersion :</span></span>

<span data-ttu-id="a9a40-133">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="a9a40-133">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="a9a40-134">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="a9a40-134">InstalledVersion :</span></span>

<span data-ttu-id="a9a40-135">Correcta: verdadero</span><span class="sxs-lookup"><span data-stu-id="a9a40-135">Succeed : True</span></span>

<span data-ttu-id="a9a40-136">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a9a40-136">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="a9a40-137">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="a9a40-137">SqlInstanceName : rtc</span></span>

<span data-ttu-id="a9a40-138">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="a9a40-138">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="a9a40-139">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="a9a40-139">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="a9a40-140">NombreBasededatos: Lis</span><span class="sxs-lookup"><span data-stu-id="a9a40-140">DatabaseName : lis</span></span>

<span data-ttu-id="a9a40-141">Orígenes</span><span class="sxs-lookup"><span data-stu-id="a9a40-141">DataSource :</span></span>

<span data-ttu-id="a9a40-142">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="a9a40-142">SQLServerVersion :</span></span>

<span data-ttu-id="a9a40-143">ExpectedVersion: 3.1.1</span><span class="sxs-lookup"><span data-stu-id="a9a40-143">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="a9a40-144">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="a9a40-144">InstalledVersion :</span></span>

<span data-ttu-id="a9a40-145">Correcta: verdadero</span><span class="sxs-lookup"><span data-stu-id="a9a40-145">Succeed : True</span></span>

<span data-ttu-id="a9a40-146">Si la base de datos está configurada correctamente pero aún disponible, el campo Success se mostrará como **false** y se proporcionarán más advertencias e información:</span><span class="sxs-lookup"><span data-stu-id="a9a40-146">If the database is configured correctly but still available, the Succeed field will be shown as **False**, and additional warnings and information will be provided:</span></span>

<span data-ttu-id="a9a40-147">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a9a40-147">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="a9a40-148">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="a9a40-148">SqlInstanceName : rtc</span></span>

<span data-ttu-id="a9a40-149">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="a9a40-149">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="a9a40-150">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="a9a40-150">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="a9a40-151">NombreBasededatos: XDS</span><span class="sxs-lookup"><span data-stu-id="a9a40-151">DatabaseName : xds</span></span>

<span data-ttu-id="a9a40-152">Orígenes</span><span class="sxs-lookup"><span data-stu-id="a9a40-152">DataSource :</span></span>

<span data-ttu-id="a9a40-153">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="a9a40-153">SQLServerVersion :</span></span>

<span data-ttu-id="a9a40-154">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="a9a40-154">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="a9a40-155">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="a9a40-155">InstalledVersion :</span></span>

<span data-ttu-id="a9a40-156">Correcta: falso</span><span class="sxs-lookup"><span data-stu-id="a9a40-156">Succeed : False</span></span>

<span data-ttu-id="a9a40-157">SqlServerFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a9a40-157">SqlServerFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a9a40-158">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="a9a40-158">SqlInstanceName : rtc</span></span>

<span data-ttu-id="a9a40-159">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="a9a40-159">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="a9a40-160">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="a9a40-160">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="a9a40-161">NombreBasededatos: Lis</span><span class="sxs-lookup"><span data-stu-id="a9a40-161">DatabaseName : lis</span></span>

<span data-ttu-id="a9a40-162">Orígenes</span><span class="sxs-lookup"><span data-stu-id="a9a40-162">DataSource :</span></span>

<span data-ttu-id="a9a40-163">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="a9a40-163">SQLServerVersion :</span></span>

<span data-ttu-id="a9a40-164">ExpectedVersion: 3.1.1</span><span class="sxs-lookup"><span data-stu-id="a9a40-164">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="a9a40-165">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="a9a40-165">InstalledVersion :</span></span>

<span data-ttu-id="a9a40-166">Correcta: falso</span><span class="sxs-lookup"><span data-stu-id="a9a40-166">Succeed : False</span></span>

<span data-ttu-id="a9a40-167">ADVERTENCIA: Test-CsDatabase detectó errores.</span><span class="sxs-lookup"><span data-stu-id="a9a40-167">WARNING: Test-CsDatabase encountered errors.</span></span> <span data-ttu-id="a9a40-168">Consultar el archivo de registro para obtener un</span><span class="sxs-lookup"><span data-stu-id="a9a40-168">Consult the log file for a</span></span>

<span data-ttu-id="a9a40-169">Análisis detallado y asegurarse de que se solucionan todos los errores (2) y las advertencias (0)</span><span class="sxs-lookup"><span data-stu-id="a9a40-169">detailed analysis, and to make sure that all errors (2) and warnings (0) are addressed</span></span>

<span data-ttu-id="a9a40-170">antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="a9a40-170">before continuing.</span></span>

<span data-ttu-id="a9a40-171">ADVERTENCIA: puede encontrar resultados detallados en</span><span class="sxs-lookup"><span data-stu-id="a9a40-171">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="a9a40-172">"C: \\ usuarios \\ probando \\ AppData \\ local \\ temporal \\ 2 \\ prueba-CsDatabase-b18d488a-8044-4679-bbf2-</span><span class="sxs-lookup"><span data-stu-id="a9a40-172">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsDatabase-b18d488a-8044-4679-bbf2-</span></span>

<span data-ttu-id="a9a40-173">04d593cce8e6.html ".</span><span class="sxs-lookup"><span data-stu-id="a9a40-173">04d593cce8e6.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="a9a40-174">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="a9a40-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="a9a40-175">Estas son algunas de las razones comunes por las que **Test-CsDatabase** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="a9a40-175">Here are some common reasons why **Test-CsDatabase** might fail:</span></span>

  - <span data-ttu-id="a9a40-176">Se proporcionó un valor de parámetro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="a9a40-176">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="a9a40-177">Si se usa, los parámetros opcionales deben estar configurados correctamente o se producirá un error en la prueba.</span><span class="sxs-lookup"><span data-stu-id="a9a40-177">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="a9a40-178">Vuelva a ejecutar el comando sin los parámetros opcionales y vea si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a9a40-178">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="a9a40-179">Este comando fallará si la base de datos no está configurada correctamente o aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="a9a40-179">This command will fail if the database is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a9a40-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9a40-180">See Also</span></span>


[<span data-ttu-id="a9a40-181">Get-CsDatabaseMirrorState</span><span class="sxs-lookup"><span data-stu-id="a9a40-181">Get-CsDatabaseMirrorState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDatabaseMirrorState)  
[<span data-ttu-id="a9a40-182">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="a9a40-182">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="a9a40-183">Get-CsUserDatabaseState</span><span class="sxs-lookup"><span data-stu-id="a9a40-183">Get-CsUserDatabaseState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserDatabaseState)  
  

<span data-ttu-id="a9a40-184"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a9a40-184"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

