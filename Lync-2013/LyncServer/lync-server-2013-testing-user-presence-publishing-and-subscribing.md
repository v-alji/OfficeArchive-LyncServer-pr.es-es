---
title: 'Lync Server 2013: prueba de la publicación de presencia de usuario y suscripción'
description: 'Lync Server 2013: prueba de la publicación de presencia de usuario y suscripción.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user presence publishing and subscribing
ms:assetid: 27694c71-8e63-4aa4-b49f-fa06ccb81949
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743832(v=OCS.15)
ms:contentKeyID: 63969587
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90913f270fbd034ca4d2ea7cf3b93c255fc95c66
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439718"
---
# <a name="testing-user-presence-publishing-and-subscribing-in-lync-server-2013"></a><span data-ttu-id="864b0-103">Probar la publicación de presencia de usuarios y la suscripción en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="864b0-103">Testing user presence publishing and subscribing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="864b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="864b0-104">

<span> </span></span></span>

<span data-ttu-id="864b0-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="864b0-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="864b0-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="864b0-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="864b0-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="864b0-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="864b0-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="864b0-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="864b0-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="864b0-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="864b0-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="864b0-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="864b0-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="864b0-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="864b0-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsPresence.</span><span class="sxs-lookup"><span data-stu-id="864b0-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPresence cmdlet.</span></span> <span data-ttu-id="864b0-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="864b0-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPresence&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="864b0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="864b0-114">Description</span></span>

<span data-ttu-id="864b0-115">Test-CsPresence se usa para determinar si un par de usuarios de prueba pueden iniciar sesión en Lync Server y, a continuación, intercambiar información de presencia.</span><span class="sxs-lookup"><span data-stu-id="864b0-115">Test-CsPresence is used to determine whether a pair of test users can log on to Lync Server and then exchange presence information.</span></span> <span data-ttu-id="864b0-116">Para ello, el cmdlet registra primero los dos usuarios en el sistema.</span><span class="sxs-lookup"><span data-stu-id="864b0-116">To do this, the cmdlet first logs the two users on to the system.</span></span> <span data-ttu-id="864b0-117">Si se ejecutan ambos inicios de sesión, el primer usuario de prueba le pedirá que reciba la información de presencia del segundo usuario.</span><span class="sxs-lookup"><span data-stu-id="864b0-117">If both logons succeed, the first test user then asks to receive presence information from the second user.</span></span> <span data-ttu-id="864b0-118">El segundo usuario publica esta información y Test-CsPresence verifica que la información se haya transmitido correctamente al primer usuario.</span><span class="sxs-lookup"><span data-stu-id="864b0-118">The second user publishes this information, and Test-CsPresence verifies that the information was successfully transmitted to the first user.</span></span> <span data-ttu-id="864b0-119">Después del intercambio de información de presencia, se cerrará la sesión de los dos usuarios de prueba en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="864b0-119">After the exchange of presence information, the two test users are then logged off from Lync Server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="864b0-120">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="864b0-120">Running the test</span></span>

<span data-ttu-id="864b0-121">El cmdlet Test-CsPresence se puede ejecutar con un par de cuentas de prueba preconfiguradas (vea configurar cuentas de prueba para ejecutar pruebas de Lync Server) o las cuentas de dos usuarios que están habilitados para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="864b0-121">The Test-CsPresence cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="864b0-122">Para ejecutar esta comprobación mediante cuentas de prueba, solo tiene que especificar el FQDN del grupo de servidores de Lync que se está probando.</span><span class="sxs-lookup"><span data-stu-id="864b0-122">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="864b0-123">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="864b0-123">For example:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="864b0-124">Para ejecutar esta comprobación con las cuentas de usuario reales, debe crear dos objetos de credenciales de Windows PowerShell (objetos que contengan el nombre y la contraseña de la cuenta) de cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="864b0-124">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="864b0-125">Después, debe incluir esos objetos de credenciales y las direcciones SIP de las dos cuentas cuando llame a test-CsPresence:</span><span class="sxs-lookup"><span data-stu-id="864b0-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsPresence:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -PublisherSipAddress "sip:kenmyer@litwareinc.com" -PublisherCredential $credential1 -SubscriberSipAddress "sip:davidlongmire@litwareinc.com" -SubscriberCredential $credential2

<span data-ttu-id="864b0-126">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) .</span><span class="sxs-lookup"><span data-stu-id="864b0-126">For more information, see the Help documentation for the [Test-CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="864b0-127">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="864b0-127">Determining success or failure</span></span>

<span data-ttu-id="864b0-128">Si los usuarios especificados pueden intercambiar información de presencia, recibirá un resultado similar a este, con la propiedad result marcada como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="864b0-128">If the specified users can exchange presence information, then you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="864b0-129">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="864b0-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="864b0-130">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="864b0-130">Result : Success</span></span>

<span data-ttu-id="864b0-131">Latencia: 00:00:06.3280315</span><span class="sxs-lookup"><span data-stu-id="864b0-131">Latency : 00:00:06.3280315</span></span>

<span data-ttu-id="864b0-132">:</span><span class="sxs-lookup"><span data-stu-id="864b0-132">Error :</span></span>

<span data-ttu-id="864b0-133">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="864b0-133">Diagnosis :</span></span>

<span data-ttu-id="864b0-134">Si los dos usuarios no pueden intercambiar información de presencia, el resultado se mostrará como error y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="864b0-134">If the two users can't exchange presence information, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="864b0-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="864b0-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="864b0-136">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="864b0-136">Result : Failure</span></span>

<span data-ttu-id="864b0-137">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="864b0-137">Latency : 00:00:00</span></span>

<span data-ttu-id="864b0-138">Error: 404, no se encontró</span><span class="sxs-lookup"><span data-stu-id="864b0-138">Error : 404, Not Found</span></span>

<span data-ttu-id="864b0-139">Diagnosis: ErrorCode = 4005, Source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="864b0-139">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="864b0-140">Motivo = URI de destino no habilitado para SIP o no</span><span class="sxs-lookup"><span data-stu-id="864b0-140">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="864b0-141">condiciones.</span><span class="sxs-lookup"><span data-stu-id="864b0-141">exist.</span></span>

<span data-ttu-id="864b0-142">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="864b0-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="864b0-143">Por ejemplo, la salida anterior indica que la prueba no se realizó correctamente porque al menos una de las dos cuentas de usuario no es válida: la cuenta no existe o no se ha habilitado para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="864b0-143">For example, the previous output states that the test failed because at least one of the two user accounts is not valid: either the account does not exist or it has not been enabled for Lync Server.</span></span> <span data-ttu-id="864b0-144">Puede comprobar que las cuentas existen y determinar si están habilitadas para Lync Server ejecutando un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="864b0-144">You can verify that the accounts exist, and determine whether they are enabled for Lync Server, by running a command similar to this:</span></span>

    "sip:kenmyer@litwareinc.com", "sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="864b0-145">Si Test-CsPresence da error, es posible que desee volver a ejecutar la prueba, esta vez incluido el parámetro detallado:</span><span class="sxs-lookup"><span data-stu-id="864b0-145">If Test-CsPresence fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="864b0-146">Cuando se incluye el parámetro detallado, Test-CsPresence devolverá una cuenta paso a paso de cada acción que se probó cuando se comprobó la capacidad del usuario especificado para iniciar sesión en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="864b0-146">When the Verbose parameter is included, Test-CsPresence will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="864b0-147">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="864b0-147">For example:</span></span>

<span data-ttu-id="864b0-148">Acceso a la solicitud de registro contra desconocido</span><span class="sxs-lookup"><span data-stu-id="864b0-148">Registration Request hit against Unknown</span></span>

<span data-ttu-id="864b0-149">Actividad ' Register ' completada en ' 0,0345791 ' s.</span><span class="sxs-lookup"><span data-stu-id="864b0-149">'Register' activity completed in '0.0345791' secs.</span></span>

<span data-ttu-id="864b0-150">Actividad ' SelfSubscribeActivity ' iniciada.</span><span class="sxs-lookup"><span data-stu-id="864b0-150">'SelfSubscribeActivity' activity started.</span></span>

<span data-ttu-id="864b0-151">Actividad ' SelfSubscribeActivity ' completada en ' 0,0041174 ' s.</span><span class="sxs-lookup"><span data-stu-id="864b0-151">'SelfSubscribeActivity' activity completed in '0.0041174' secs.</span></span>

<span data-ttu-id="864b0-152">Actividad ' SubscribePresence ' iniciada.</span><span class="sxs-lookup"><span data-stu-id="864b0-152">'SubscribePresence' activity started.</span></span>

<span data-ttu-id="864b0-153">Actividad ' SubscribePresence ' completada en ' 0,0038764 ' s.</span><span class="sxs-lookup"><span data-stu-id="864b0-153">'SubscribePresence' activity completed in '0.0038764' secs.</span></span>

<span data-ttu-id="864b0-154">Actividad ' PublishPresence ' iniciada.</span><span class="sxs-lookup"><span data-stu-id="864b0-154">'PublishPresence' activity started.</span></span>

<span data-ttu-id="864b0-155">No se recibe una notificación de presencia de excepción en un lapso de 25 segundos.</span><span class="sxs-lookup"><span data-stu-id="864b0-155">An exception 'Presence notification is not received within 25 secs.'</span></span> <span data-ttu-id="864b0-156">se ha producido ruing flujo de trabajo Microsoft. RTC. SyntheticTransactions. flujos de trabajo. STPresenceWorkflow.</span><span class="sxs-lookup"><span data-stu-id="864b0-156">occurred ruing Workflow Microsoft.Rtc.SyntheticTransactions.Workflows.STPresenceWorkflow execution.</span></span>

<span data-ttu-id="864b0-157">El hecho de que la notificación de presencia no se haya recibido en 25 segundos podría indicar que hay problemas de red que impiden que se intercambie la información.</span><span class="sxs-lookup"><span data-stu-id="864b0-157">The fact that the presence notification was not received within 25 seconds might indicate that network issues are preventing information from being exchanged.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="864b0-158">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="864b0-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="864b0-159">Estas son algunas de las razones comunes por las que Test-CsPresence puede dar error:</span><span class="sxs-lookup"><span data-stu-id="864b0-159">Here are some common reasons why Test-CsPresence might fail:</span></span>

  - <span data-ttu-id="864b0-160">Ha especificado una cuenta de usuario incorrecta.</span><span class="sxs-lookup"><span data-stu-id="864b0-160">You specified an incorrect user account.</span></span> <span data-ttu-id="864b0-161">Puede comprobar que una cuenta de usuario existe ejecutando un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="864b0-161">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="864b0-162">La cuenta de usuario es válida, pero la cuenta no está habilitada actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="864b0-162">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="864b0-163">Para comprobar que una cuenta de usuario está habilitada para Lync Server, ejecute un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="864b0-163">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="864b0-164">Si la propiedad Enabled se establece en false, significa que el usuario no está habilitado actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="864b0-164">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="864b0-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="864b0-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

