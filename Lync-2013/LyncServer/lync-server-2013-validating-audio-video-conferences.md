---
title: 'Lync Server 2013: validación de conferencias de audio o vídeo'
description: 'Lync Server 2013: validación de conferencias de audio o vídeo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating audio/video conferences
ms:assetid: 6c8c422a-d501-42cb-820b-b002f9b2250b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720915(v=OCS.15)
ms:contentKeyID: 63969615
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad12611e928a64b934252ec21c18b98366e0912b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443492"
---
# <a name="validating-audiovideo-conferences-in-lync-server-2013"></a><span data-ttu-id="ce6a9-103">Validación de conferencias de audio o vídeo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce6a9-103">Validating audio/video conferences in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce6a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce6a9-104">

<span> </span></span></span>

<span data-ttu-id="ce6a9-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="ce6a9-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce6a9-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="ce6a9-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="ce6a9-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="ce6a9-107">Daily</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce6a9-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="ce6a9-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="ce6a9-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ce6a9-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce6a9-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="ce6a9-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="ce6a9-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="ce6a9-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsAVConference.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAVConference cmdlet.</span></span> <span data-ttu-id="ce6a9-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAVConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="ce6a9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce6a9-114">Description</span></span>

<span data-ttu-id="ce6a9-115">El cmdlet Test-CsAVConference comprueba si dos usuarios de prueba pueden participar en una conferencia de audio o vídeo (A/V).</span><span class="sxs-lookup"><span data-stu-id="ce6a9-115">The Test-CsAVConference cmdlet checks whether two test users can participate in an audio/video (A/V) conference.</span></span> <span data-ttu-id="ce6a9-116">Cuando se ejecuta el cmdlet, los dos usuarios inician sesión en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-116">When the cmdlet runs, the two users are logged on to the system.</span></span> <span data-ttu-id="ce6a9-117">Una vez que se hayan conectado correctamente, el primer usuario crea una conferencia a/V y, a continuación, espera a que el segundo usuario se una a la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-117">After they face successfully logged on, the first user creates an A/V conference, and then waits for the second user to join that conference.</span></span> <span data-ttu-id="ce6a9-118">Después de un breve intercambio de datos, se elimina la Conferencia y se desconectan las dos pruebas de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-118">After a brief exchange of data, the conference is deleted and the two tests users are logged off.</span></span>

<span data-ttu-id="ce6a9-119">Tenga en cuenta que Test-CsAVConference no realiza una conferencia A/V real entre los dos usuarios de prueba.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-119">Note that Test-CsAVConference does not conduct an actual A/V conference between the two test users.</span></span> <span data-ttu-id="ce6a9-120">En su lugar, el cmdlet verifica que los dos usuarios pueden hacer todas las conexiones necesarias para llevar a cabo una conferencia.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-120">Instead, the cmdlet verifies that the two users can make all the connections necessary to conduct such a conference.</span></span>

<span data-ttu-id="ce6a9-121">Puede encontrar más ejemplos de este comando en [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference).</span><span class="sxs-lookup"><span data-stu-id="ce6a9-121">Further examples for this command can be found at [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference).</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="ce6a9-122">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="ce6a9-122">Running the test</span></span>

<span data-ttu-id="ce6a9-123">El cmdlet Test-CsAVConference se puede ejecutar con un par de cuentas de prueba preconfiguradas (vea configurar cuentas de prueba para ejecutar pruebas de Lync Server) o las cuentas de dos usuarios que están habilitados para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-123">The Test-CsAVConference cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="ce6a9-124">Para ejecutar esta comprobación mediante cuentas de prueba, solo tiene que especificar el FQDN del grupo de servidores de Lync que se está probando.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-124">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="ce6a9-125">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-125">For example:</span></span>

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="ce6a9-126">Para ejecutar esta comprobación con las cuentas de usuario reales, debe crear dos objetos de credenciales de Windows PowerShell (objetos que contengan el nombre y la contraseña de la cuenta) de cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-126">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="ce6a9-127">Después, debe incluir esos objetos de credenciales y las direcciones SIP de las dos cuentas cuando llaman a test-CsAVConference:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-127">You must then include those credentials objects and the SIP addresses of the two accounts when they call Test-CsAVConference:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="ce6a9-128">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference) .</span><span class="sxs-lookup"><span data-stu-id="ce6a9-128">For more information, see the Help documentation for the [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="ce6a9-129">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="ce6a9-129">Determining Success or Failure</span></span>

<span data-ttu-id="ce6a9-130">Si los usuarios especificados pueden completar correctamente una conferencia A/V, recibirá una salida similar a la siguiente, con la propiedad result marcada como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="ce6a9-130">If the specified users can successfully complete an A/V conference, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="ce6a9-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ce6a9-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ce6a9-132">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="ce6a9-132">Result : Success</span></span>

<span data-ttu-id="ce6a9-133">Latencia: 00:00:02.6841765</span><span class="sxs-lookup"><span data-stu-id="ce6a9-133">Latency : 00:00:02.6841765</span></span>

<span data-ttu-id="ce6a9-134">:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-134">Error :</span></span>

<span data-ttu-id="ce6a9-135">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ce6a9-135">Diagnosis :</span></span>

<span data-ttu-id="ce6a9-136">Si los usuarios no pueden completar la Conferencia, el resultado se mostrará como error y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-136">If the users can not complete the conference, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="ce6a9-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ce6a9-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ce6a9-138">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="ce6a9-138">Result : Failure</span></span>

<span data-ttu-id="ce6a9-139">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ce6a9-139">Latency : 00:00:00</span></span>

<span data-ttu-id="ce6a9-140">Error: 404, no se encontró</span><span class="sxs-lookup"><span data-stu-id="ce6a9-140">Error : 404, Not Found</span></span>

<span data-ttu-id="ce6a9-141">Diagnosis: ErrorCode = 4005, Source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="ce6a9-141">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="ce6a9-142">Motivo = URI de destino no habilitado para SIP o no</span><span class="sxs-lookup"><span data-stu-id="ce6a9-142">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="ce6a9-143">condiciones.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-143">exist.</span></span>

<span data-ttu-id="ce6a9-144">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="ce6a9-144">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="ce6a9-145">Por ejemplo, la salida anterior indica que la prueba no se realizó correctamente porque al menos una de las dos cuentas de usuario no era válida, ya sea porque la cuenta no existe o porque la cuenta no se ha habilitado para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-145">For example, the previous output states that the test failed because at least one of the two user accounts was not valid, either because the account does not exist or because the account has not been enabled for Lync Server.</span></span> <span data-ttu-id="ce6a9-146">Puede comprobar la existencia de las dos cuentas de prueba y si se han habilitado para Lync Server ejecutando un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-146">You can verify the existence of the two test accounts, and whether they were enabled for Lync Server, by running a command similar to the following:</span></span>

    "sip:kenmyer@litwareinc.com","sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, enabled

<span data-ttu-id="ce6a9-147">Si Test-CsAVConference da error, es posible que desee volver a ejecutar la prueba, esta vez incluido el parámetro detallado:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-147">If Test-CsAVConference fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="ce6a9-148">Cuando se incluye el parámetro detallado Test-CsAVConference se devolverá una cuenta paso a paso de cada acción que haya probado cuando haya comprobado la posibilidad de que los usuarios especificados participen en una conferencia antivirus.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-148">When the Verbose parameter is included Test-CsAVConference will return a step-by-step account of each action it tried when it checked the ability of the specified users to participate in an AV conference.</span></span> <span data-ttu-id="ce6a9-149">Por ejemplo, supongamos que la prueba falla y recibe el siguiente diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-149">For example, suppose that your test fails and you receive the following Diagnosis:</span></span>

<span data-ttu-id="ce6a9-150">ErrorCode = 1008, Source = accessproxy. litwareinc. com, causa = no se puede resolver el registro SRV de DNS</span><span class="sxs-lookup"><span data-stu-id="ce6a9-150">ErrorCode=1008,Source=accessproxy.litwareinc.com,Reason=Unable to resolve DNS SRV record</span></span>

<span data-ttu-id="ce6a9-151">Si vuelve a ejecutar la prueba con el parámetro verbose, la información devuelta incluirá una salida similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-151">If you rerun the test using the Verbose parameter, the step-by-step information returned will include output similar to this:</span></span>

<span data-ttu-id="ce6a9-152">VERBOse: actividad ' Register ' iniciada.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-152">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="ce6a9-153">Enviando solicitud de registro:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-153">Sending Registration request:</span></span>

<span data-ttu-id="ce6a9-154">FQDN de destino = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ce6a9-154">Target Fqdn = atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ce6a9-155">Dirección SIP del usuario = sip:davidlongmire@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ce6a9-155">User Sip Address = sip:davidlongmire@litwareinc.com</span></span>

<span data-ttu-id="ce6a9-156">Registrar puerto = 5061.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-156">Registrar Port = 5061.</span></span>

<span data-ttu-id="ce6a9-157">El tipo de autenticación "de confianza" está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-157">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="ce6a9-158">Actividad ' Register ' iniciada.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-158">'Register' activity started.</span></span>

<span data-ttu-id="ce6a9-159">Enviando solicitud de registro:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-159">Sending Registration request:</span></span>

<span data-ttu-id="ce6a9-160">FQDN de destino = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ce6a9-160">Target Fqdn = atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ce6a9-161">Dirección SIP del usuario = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ce6a9-161">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="ce6a9-162">Registrar puerto = 5061.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-162">Registrar Port = 5061.</span></span>

<span data-ttu-id="ce6a9-163">El tipo de autenticación "de confianza" está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-163">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="ce6a9-164">Excepción ' el punto de conexión no se pudo registrar.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-164">An exception 'The endpoint was unable to register.</span></span> <span data-ttu-id="ce6a9-165">Consulte ErrorCode por razones específicas. '</span><span class="sxs-lookup"><span data-stu-id="ce6a9-165">See the ErrorCode for specific reason.'</span></span> <span data-ttu-id="ce6a9-166">durante el flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="ce6a9-166">occurred during Workflow</span></span>

<span data-ttu-id="ce6a9-167">La última línea de la salida indica que el usuario sip:kenmyer@litwareinc.com no se pudo registrar con Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-167">The last line in that output indicates that the user sip:kenmyer@litwareinc.com was unable to register with Lync Server.</span></span> <span data-ttu-id="ce6a9-168">Eso significa que debe comprobar que la dirección SIP sip:kenmyer@litwareinc.com es válida y que el usuario asociado está habilitado para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-168">That means that you should verify that the SIP address sip:kenmyer@litwareinc.com is valid, and that the associated user is enabled for Lync Server.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="ce6a9-169">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="ce6a9-169">Reasons why the test might have failed</span></span>

<span data-ttu-id="ce6a9-170">Estas son algunas de las razones comunes por las que Test-CsAVConference puede dar error:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-170">Here are some common reasons why Test-CsAVConference might fail:</span></span>

  - <span data-ttu-id="ce6a9-171">Ha especificado una cuenta de usuario que no es válida.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-171">You specified a user account that is not valid.</span></span> <span data-ttu-id="ce6a9-172">Puede comprobar que una cuenta de usuario existe ejecutando un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-172">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="ce6a9-173">La cuenta de usuario es válida, pero la cuenta no está habilitada actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-173">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="ce6a9-174">Para comprobar que una cuenta de usuario está habilitada para Lync Server, ejecute un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="ce6a9-174">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="ce6a9-175">Si la propiedad Enabled se establece en false, significa que el usuario no está habilitado actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce6a9-175">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="ce6a9-176"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce6a9-176"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

