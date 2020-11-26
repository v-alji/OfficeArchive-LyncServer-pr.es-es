---
title: 'Lync Server 2013: probar las conferencias de audio de terceros'
description: 'Lync Server 2013: prueba de las conferencias de audio de terceros.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing third-party audio conferencing
ms:assetid: 0428eb2f-a5ce-47e5-9ea4-383965dfc1e4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727299(v=OCS.15)
ms:contentKeyID: 63969576
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f009d95834768d8a4e6619a79ff1f3be0a2b92bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440958"
---
# <a name="testing-third-party-audio-conferencing-in-lync-server-2013"></a><span data-ttu-id="b9978-103">Prueba de conferencias de audio de terceros en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b9978-103">Testing third-party audio conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b9978-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b9978-104">

<span> </span></span></span>

<span data-ttu-id="b9978-105">_**Última modificación del tema:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="b9978-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9978-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="b9978-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="b9978-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="b9978-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9978-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="b9978-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="b9978-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b9978-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9978-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="b9978-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="b9978-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="b9978-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="b9978-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsAudioConferencingProvider.</span><span class="sxs-lookup"><span data-stu-id="b9978-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAudioConferencingProvider cmdlet.</span></span> <span data-ttu-id="b9978-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b9978-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAudioConferencingProvider&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b9978-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9978-114">Description</span></span>

<span data-ttu-id="b9978-115">Estos proveedores son organizaciones de terceros que suministran servicios de audioconferencia a organizaciones.</span><span class="sxs-lookup"><span data-stu-id="b9978-115">An audio conferencing provider is a third-party company that provides organizations with conferencing services.</span></span> <span data-ttu-id="b9978-116">Entre otras cosas, los proveedores de audioconferencia permiten a los usuarios que no se encuentran en la oficina, y que no están conectados a la red corporativa o Internet, participar en la parte de audio de una conferencia o una reunión.</span><span class="sxs-lookup"><span data-stu-id="b9978-116">Among other things, audio conferencing providers enable users located off site, and not connected to the corporate network or the Internet, to participate in the audio portion of a conference or meeting.</span></span> <span data-ttu-id="b9978-117">Los proveedores de servicios de audioconferencia suelen ofrecer servicios de alta calidad, como la traducción en vivo, la transcripción y la asistencia del operador Live por Conferencia.</span><span class="sxs-lookup"><span data-stu-id="b9978-117">Audio conferencing providers often provide high-end services such as live translation, transcription, and live per-conference operator assistance.</span></span>

<span data-ttu-id="b9978-118">El cmdlet **Test-CsAudioConferencingProvider** se usa para comprobar que un usuario puede establecer una conexión con su proveedor de servicios de audioconferencia.</span><span class="sxs-lookup"><span data-stu-id="b9978-118">The **Test-CsAudioConferencingProvider** cmdlet is used to verify that a user is able to make a connection to his or her audio conferencing provider.</span></span> <span data-ttu-id="b9978-119">Tenga en cuenta que este cmdlet puede ejecutarse de una de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="b9978-119">Note that this cmdlet can be run in one of two ways.</span></span> <span data-ttu-id="b9978-120">Muchos administradores usarán los cmdlets de CsHealthMonitoringConfiguration para configurar los usuarios de prueba para cada uno de sus grupos de registradores.</span><span class="sxs-lookup"><span data-stu-id="b9978-120">Many administrators will use the CsHealthMonitoringConfiguration cmdlets to set up test users for each of their Registrar pools.</span></span> <span data-ttu-id="b9978-121">Estos usuarios de prueba representan un par de cuentas de usuario preconfiguradas para su uso con transacciones sintéticas.</span><span class="sxs-lookup"><span data-stu-id="b9978-121">These test users represent a pair of user accounts that have been preconfigured for use with synthetic transactions.</span></span> <span data-ttu-id="b9978-122">(Normalmente, son cuentas de prueba y no cuentas que pertenecen a usuarios reales). Si los usuarios de prueba están configurados para un grupo, los administradores pueden ejecutar el cmdlet **Test-CsAudioConferencingProvider** en ese grupo sin tener que especificar la identidad de (y proporcionar las credenciales para) la cuenta de usuario implicada en la prueba.</span><span class="sxs-lookup"><span data-stu-id="b9978-122">(Typically these are test accounts and not accounts that belong to actual users.) If test users are configured for a pool, administrators can run the **Test-CsAudioConferencingProvider** cmdlet against that pool without having to specify the identity of (and supply the credentials for) the user account involved in the test.</span></span>

<span data-ttu-id="b9978-123">Como alternativa, los administradores pueden ejecutar el cmdlet **Test-CsAudioConferencingProvider** con una cuenta de usuario real.</span><span class="sxs-lookup"><span data-stu-id="b9978-123">Alternatively, administrators can run the **Test-CsAudioConferencingProvider** cmdlet using an actual user account.</span></span> <span data-ttu-id="b9978-124">Si decide realizar la prueba usando una cuenta de usuario real, tendrá que proporcionar el nombre de inicio de sesión y la contraseña de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="b9978-124">If you decide to conduct the test using an actual user account you will need to supply the logon name and password for that account.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b9978-125">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="b9978-125">Running the test</span></span>

<span data-ttu-id="b9978-126">El ejemplo 1 comprueba si un usuario de prueba definido para el grupo atl-cs-001.litwareinc.com puede conectarse a su proveedor de servicios de audioconferencia.</span><span class="sxs-lookup"><span data-stu-id="b9978-126">Example 1 checks to see if a test user defined for the pool atl-cs-001.litwareinc.com is able to connect to his or her audio conferencing provider.</span></span> <span data-ttu-id="b9978-127">Este comando requiere que se defina al menos un usuario de prueba para el grupo.</span><span class="sxs-lookup"><span data-stu-id="b9978-127">This command requires that at least one test user be defined for the pool.</span></span> <span data-ttu-id="b9978-128">Si no se han definido usuarios de prueba para atl-cs-001.litwareinc.com, el comando fallará; Esto se debe a que el cmdlet **Test-CsAudioConferencingProvider** no sabrá qué usuario debe emplear en la prueba.</span><span class="sxs-lookup"><span data-stu-id="b9978-128">If no test users have been defined for atl-cs-001.litwareinc.com, then the command will fail; that's because the **Test-CsAudioConferencingProvider** cmdlet will not know which user to employ in the test.</span></span> <span data-ttu-id="b9978-129">Si no ha definido usuarios de prueba para un grupo, debe incluir el parámetro UserSipAddress y las credenciales de la cuenta de usuario que debe usar el comando al comprobar la conexión con un proveedor de servicios de audioconferencia.</span><span class="sxs-lookup"><span data-stu-id="b9978-129">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user account that the command should employ when verifying the connection with an audio conferencing provider.</span></span>

    Test-CsAudioConferencingProvider -TargetFqdn atl-cs-001.litwareinc.com 

<span data-ttu-id="b9978-130">Los comandos que se muestran en el ejemplo 2 prueban la capacidad de un usuario específico (litwareinc \\ kenmyer) para conectarse a su proveedor de servicios de audioconferencia.</span><span class="sxs-lookup"><span data-stu-id="b9978-130">The commands shown in Example 2 test the ability of a specific user (litwareinc\\kenmyer) to connect to his audio conferencing provider.</span></span> <span data-ttu-id="b9978-131">Para ello, el primer comando del ejemplo usa el cmdlet Get-Credential para crear un objeto de credenciales de la interfaz de línea de comandos de Windows PowerShell que contiene el nombre y la contraseña del usuario Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="b9978-131">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credentials object containing the name and password of the user Ken Myer.</span></span> <span data-ttu-id="b9978-132">(Dado que el nombre de inicio de sesión litwareinc kenmyer se ha \\ incluido como parámetro, el cuadro de diálogo solicitud de credenciales de Windows PowerShell solo requiere que el administrador escriba la contraseña de la cuenta de Ken Myer). El objeto de credenciales resultante se almacena en una variable denominada $credential.</span><span class="sxs-lookup"><span data-stu-id="b9978-132">(Because the logon name litwareinc\\kenmyer has been included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Ken Myer account.) The resulting credentials object is stored in a variable named $credential.</span></span>

<span data-ttu-id="b9978-133">El segundo comando comprueba entonces si este usuario puede conectarse a su proveedor de servicios de audioconferencia.</span><span class="sxs-lookup"><span data-stu-id="b9978-133">The second command then checks to see if this user can connect to his audio conferencing provider.</span></span> <span data-ttu-id="b9978-134">Para llevar a cabo esta tarea, se llama al cmdlet Test-CsAudioConferencingProvider, junto con tres parámetros: TargetFqdn (el FQDN del grupo de servidores de registrar); UserCredential (el objeto de Windows PowerShell que contiene las credenciales de usuario de Ken Myer); y UserSipAddress (la dirección SIP correspondiente a las credenciales de usuario suministradas).</span><span class="sxs-lookup"><span data-stu-id="b9978-134">To carry out this task, the Test-CsAudioConferencingProvider cmdlet is called, along with three parameters: TargetFqdn (the FQDN of the Registrar pool); UserCredential (the Windows PowerShell object containing Ken Myer's user credentials); and UserSipAddress (the SIP address corresponding to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer" 
    Test-CsAudioConferencingProvider -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b9978-135">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="b9978-135">Determining success or failure</span></span>

<span data-ttu-id="b9978-136">Si el proveedor de servicios de audioconferencia está configurado correctamente, recibirá una salida similar a la siguiente, con la propiedad result marcada como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="b9978-136">If the audio conferencing provider is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="b9978-137">FQDN de destino: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b9978-137">Target Fqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="b9978-138">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="b9978-138">Result : Success</span></span>

<span data-ttu-id="b9978-139">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b9978-139">Latency : 00:00:00</span></span>

<span data-ttu-id="b9978-140">Mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="b9978-140">Error Message :</span></span>

<span data-ttu-id="b9978-141">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="b9978-141">Diagnosis :</span></span>

<span data-ttu-id="b9978-142">Si el usuario especificado no puede iniciar sesión o cerrar sesión, el resultado se mostrará como un **error** y se registrará información adicional en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="b9978-142">If the specified user can't log on or log off, the Result will be shown as a **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="b9978-143">FQDN de destino: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b9978-143">Target Fqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="b9978-144">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="b9978-144">Result : Failure</span></span>

<span data-ttu-id="b9978-145">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b9978-145">Latency : 00:00:00</span></span>

<span data-ttu-id="b9978-146">Mensaje de error: 10060, error al intentar la conexión porque la persona conectada</span><span class="sxs-lookup"><span data-stu-id="b9978-146">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="b9978-147">no respondió correctamente después de un período de tiempo, o</span><span class="sxs-lookup"><span data-stu-id="b9978-147">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="b9978-148">error en la conexión establecida porque el host conectado tiene</span><span class="sxs-lookup"><span data-stu-id="b9978-148">established connection failed because connected host has</span></span>

<span data-ttu-id="b9978-149">Error al responder \[ 2001:4898: E8: f39e: 5c9a: ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="b9978-149">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="b9978-150">Excepción interna: error en el intento de conexión porque el</span><span class="sxs-lookup"><span data-stu-id="b9978-150">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="b9978-151">la parte conectada no respondió correctamente después de un período de</span><span class="sxs-lookup"><span data-stu-id="b9978-151">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="b9978-152">hora o error de conexión establecida porque el host conectado</span><span class="sxs-lookup"><span data-stu-id="b9978-152">time, or established connection failed because connected host</span></span>

<span data-ttu-id="b9978-153">Error al responder</span><span class="sxs-lookup"><span data-stu-id="b9978-153">has failed to respond</span></span>

<span data-ttu-id="b9978-154">\[2001:4898: E8: f39e: 5c9a: ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="b9978-154">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="b9978-155">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="b9978-155">Diagnosis :</span></span>

<span data-ttu-id="b9978-156">Por ejemplo, la salida anterior incluye la nota "la persona conectada no respondió correctamente" que normalmente indica que hay un problema con el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="b9978-156">For example, the previous output includes the note “the connected party did not properly respond” That typically indicates a problem with the Edge Server.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b9978-157">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="b9978-157">Reasons why the test might have failed</span></span>

<span data-ttu-id="b9978-158">Estas son algunas de las razones comunes por las que **Test-CsAudioConferencingProvider** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="b9978-158">Here are some common reasons why **Test-CsAudioConferencingProvider** might fail:</span></span>

  - <span data-ttu-id="b9978-159">Se proporcionó un valor de parámetro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="b9978-159">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="b9978-160">Tal y como se muestra en el ejemplo anterior, los parámetros opcionales deben estar configurados correctamente o no se puede realizar la prueba.</span><span class="sxs-lookup"><span data-stu-id="b9978-160">As shown in the previous example, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="b9978-161">Vuelva a ejecutar el comando sin los parámetros opcionales y vea si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="b9978-161">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="b9978-162">Observe que la prueba se producirá un error si el usuario empleado por el cmdlet **Test-CsAudioConferencingProvider** no ha sido asignado a un proveedor de servicios de audioconferencia.</span><span class="sxs-lookup"><span data-stu-id="b9978-162">Note that the test will fail if the user employed by the **Test-CsAudioConferencingProvider** cmdlet has not been assigned an audio conferencing provider.</span></span>

  - <span data-ttu-id="b9978-163">Este comando fallará si el servidor perimetral está mal configurado o aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="b9978-163">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

<span data-ttu-id="b9978-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b9978-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

