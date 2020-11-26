---
title: 'Lync Server 2013: realizar una llamada de punto a punto de RTC'
description: 'Lync Server 2013: realizar una llamada RTC de par a par.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN peer to peer call
ms:assetid: 7e128eef-9ada-49b4-940f-97d7d13f1e4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690131(v=OCS.15)
ms:contentKeyID: 63969622
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8bf8726c46374e3a799b986e071566d0ae1de138
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439803"
---
# <a name="testing-pstn-peer-to-peer-call-in-lync-server-2013"></a><span data-ttu-id="5e3b7-103">Probar la llamada RTC de par a par en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5e3b7-103">Testing PSTN peer to peer call in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5e3b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5e3b7-104">

<span> </span></span></span>

<span data-ttu-id="5e3b7-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="5e3b7-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e3b7-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="5e3b7-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="5e3b7-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="5e3b7-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3b7-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="5e3b7-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="5e3b7-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5e3b7-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3b7-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="5e3b7-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="5e3b7-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="5e3b7-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsPstnPeerToPeerCall.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPstnPeerToPeerCall cmdlet.</span></span> <span data-ttu-id="5e3b7-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPstnPeerToPeerCall&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="5e3b7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e3b7-114">Description</span></span>

<span data-ttu-id="5e3b7-115">El cmdlet de Test-CsPstnPeerToPeerCall comprueba la capacidad de un par de usuarios de realizar una llamada de punto a punto a través de la puerta de enlace de red telefónica conmutada (RTC).</span><span class="sxs-lookup"><span data-stu-id="5e3b7-115">The Test-CsPstnPeerToPeerCall cmdlet verifies the ability a pair of users has to conduct a peer-to-peer call over the public switched telephone network (PSTN) gateway.</span></span> <span data-ttu-id="5e3b7-116">Al llamar a test-CsPstnPeerToPeerCall, el cmdlet primero intenta iniciar sesión en dos usuarios de prueba en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-116">When you call Test-CsPstnPeerToPeerCall, the cmdlet will first attempt to log on two test users to Lync Server.</span></span> <span data-ttu-id="5e3b7-117">Suponiendo que los inicios de sesión se realicen correctamente, el cmdlet tendrá el intento de usuario 1 de llamar al usuario 2 a través de la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-117">Assuming that the logons succeed, the cmdlet will then have user 1 attempt to call user 2 over the PSTN gateway.</span></span> <span data-ttu-id="5e3b7-118">Test-CsPstnPeerToPeerCall realizará esta llamada con el plan de marcado, la Directiva de voz y otras opciones de configuración y directivas asignadas al usuario de prueba.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-118">Test-CsPstnPeerToPeerCall will make this call using the dial plan, voice policy, and other policy and configuration settings assigned to the test user.</span></span> <span data-ttu-id="5e3b7-119">Si la prueba se reproduce como planeada, el cmdlet comprobará que el usuario 2 pudo contestar la llamada y, a continuación, cerrará la sesión con ambas cuentas de prueba del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-119">If the test goes as planned, the cmdlet will verify that user 2 was able to answer the call, and then log off both test accounts from the system.</span></span>

<span data-ttu-id="5e3b7-120">Test-CsPstnPeerToPeerCall realiza una llamada real, una que comprueba que se puede realizar una conexión y que también transmite códigos de DTMF a través de la red para determinar si los medios se pueden enviar a través de la conexión.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-120">Test-CsPstnPeerToPeerCall makes an actual phone call, one that verifies that a connection can be made and that also transmits DTMF codes over the network to determine whether media can be sent over the connection.</span></span> <span data-ttu-id="5e3b7-121">La llamada es respondida por el propio cmdlet, y no es necesaria la finalización manual de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-121">The call is answered by the cmdlet itself, and no manual termination of the call is necessary.</span></span> <span data-ttu-id="5e3b7-122">(Es decir, nadie debe responder y, a continuación, colgar el teléfono al que se llamó).</span><span class="sxs-lookup"><span data-stu-id="5e3b7-122">(That is, no one must answer and then hang up the phone that was called.)</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="5e3b7-123">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="5e3b7-123">Running the test</span></span>

<span data-ttu-id="5e3b7-124">El cmdlet Test-CsPstnPeerToPeerCall se puede ejecutar con un par de cuentas de prueba preconfiguradas (vea configurar cuentas de prueba para ejecutar pruebas de Lync Server) o las cuentas de dos usuarios que están habilitados para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-124">The Test-CsPstnPeerToPeerCall cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="5e3b7-125">Para ejecutar esta comprobación mediante cuentas de prueba, solo tiene que especificar el FQDN del grupo de servidores de Lync que se está probando.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-125">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="5e3b7-126">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-126">For example:</span></span>

`Test-CsPstnPeerToPeerCall -TargetFqdn "atl-cs-001.litwareinc.com"`

<span data-ttu-id="5e3b7-127">Para ejecutar esta comprobación con las cuentas de usuario reales, debe crear dos objetos de credenciales de Windows PowerShell (objetos que contengan el nombre y la contraseña de la cuenta) de cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-127">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="5e3b7-128">Después, debe incluir esos objetos de credenciales y las direcciones SIP de las dos cuentas cuando llame a test-CsPstnPeerToPeerCall:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-128">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsPstnPeerToPeerCall:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsPstnPeerToPeerCall -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="5e3b7-129">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsPstnPeerToPeerCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnPeerToPeerCall) .</span><span class="sxs-lookup"><span data-stu-id="5e3b7-129">For more information, see the Help documentation for the [Test-CsPstnPeerToPeerCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnPeerToPeerCall) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="5e3b7-130">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="5e3b7-130">Determining success or failure</span></span>

<span data-ttu-id="5e3b7-131">Si los usuarios especificados pueden completar una llamada de punto a punto, recibirá una salida similar a la siguiente, con la propiedad result marcada como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="5e3b7-131">If the specified users can complete a peer-to-peer call, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="5e3b7-132">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5e3b7-132">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="5e3b7-133">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="5e3b7-133">Result : Success</span></span>

<span data-ttu-id="5e3b7-134">Latencia: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="5e3b7-134">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="5e3b7-135">:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-135">Error :</span></span>

<span data-ttu-id="5e3b7-136">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="5e3b7-136">Diagnosis :</span></span>

<span data-ttu-id="5e3b7-137">Si los usuarios especificados no pueden completar una llamada de punto a punto, el resultado se mostrará como error y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-137">If the specified users can't complete a peer-to-peer call, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="5e3b7-138">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5e3b7-138">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="5e3b7-139">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="5e3b7-139">Result : Failure</span></span>

<span data-ttu-id="5e3b7-140">Latencia: 00:00:0182361</span><span class="sxs-lookup"><span data-stu-id="5e3b7-140">Latency : 00:00:0182361</span></span>

<span data-ttu-id="5e3b7-141">Error: 403, prohibido</span><span class="sxs-lookup"><span data-stu-id="5e3b7-141">Error : 403, Forbidden</span></span>

<span data-ttu-id="5e3b7-142">Diagnosis: ErrorCode = 12001, Source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="5e3b7-142">Diagnosis : ErrorCode=12001,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="5e3b7-143">Motivo = la Directiva de usuario no contiene uso de la ruta telefónica</span><span class="sxs-lookup"><span data-stu-id="5e3b7-143">Reason=User Policy does not contain phone route usage</span></span>

<span data-ttu-id="5e3b7-144">El resultado anterior indica que no se pudo realizar la prueba porque la Directiva de voz asignada a al menos uno de los usuarios especificados no incluye un uso de teléfono.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-144">The previous output states that the test failed because the voice policy assigned to at least one of the specified users does not include a phone usage.</span></span> <span data-ttu-id="5e3b7-145">(Las directivas de voz se asocian con las directivas de voz.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-145">(Phone usages tie voice policies to voice routes.</span></span> <span data-ttu-id="5e3b7-146">Sin una directiva de voz y una ruta de voz correspondiente, no puede hacer llamadas a través de la RTC.)</span><span class="sxs-lookup"><span data-stu-id="5e3b7-146">Without both a voice policy and a corresponding voice route, you can't make calls over the PSTN.)</span></span>

<span data-ttu-id="5e3b7-147">Si Test-CsPstnPeerToPeerCall da error, es posible que desee volver a ejecutar la prueba, esta vez incluido el parámetro detallado:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-147">If Test-CsPstnPeerToPeerCall fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPstnPeerToPeerCall -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="5e3b7-148">Cuando se incluye el parámetro detallado, Test-CsPstnPeerToPeerCall devolverá una cuenta paso a paso de cada acción que se probó cuando se comprobó la capacidad del usuario especificado para iniciar sesión en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-148">When the Verbose parameter is included, Test-CsPstnPeerToPeerCall will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="5e3b7-149">Por ejemplo, esta salida indica que hay problemas de red que impiden una conexión con la RTC:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-149">For example, this output indicates that network problems are preventing a connection with the PSTN:</span></span>

<span data-ttu-id="5e3b7-150">Establecer videollamadas de audio a ' SIP: + 12065551219@litwareinc. com; User = Phone '.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-150">Establishing Audio Video call to 'sip:+12065551219@litwareinc.com;user=phone'.</span></span>

<span data-ttu-id="5e3b7-151">Se ha recibido una respuesta ' una 404 (no se encontró) de la red y se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-151">An exception 'A 404 (Not Found) response was received from the network and the operation failed.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="5e3b7-152">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="5e3b7-152">Reasons why the test might have failed</span></span>

<span data-ttu-id="5e3b7-153">Estas son algunas de las razones comunes por las que Test-CsPstnPeerToPeerCall puede dar error:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-153">Here are some common reasons why Test-CsPstnPeerToPeerCall might fail:</span></span>

  - <span data-ttu-id="5e3b7-154">Ha especificado una cuenta de usuario que no es válida.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-154">You specified a user account that is not valid.</span></span> <span data-ttu-id="5e3b7-155">Puede comprobar que una cuenta de usuario existe ejecutando un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-155">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="5e3b7-156">La cuenta de usuario es válida, pero la cuenta no está habilitada actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-156">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="5e3b7-157">Para comprobar que una cuenta de usuario está habilitada para Lync Server, ejecute un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-157">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="5e3b7-158">Si la propiedad Enabled se establece en false, significa que el usuario no está habilitado actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-158">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="5e3b7-159">La Directiva de voz asignada al usuario especificado no tiene un uso de RTC válido.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-159">The voice policy assigned to the specified user does not have a valid PSTN usage.</span></span> <span data-ttu-id="5e3b7-160">Puede determinar la Directiva de voz asignada a un usuario mediante un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-160">You can determine the voice policy that is assigned to a user by using a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object VoicePolicy
    
    <span data-ttu-id="5e3b7-161">Y, después, puede determinar los usos de RTC (si los hay) que se asignan a esa Directiva mediante un comando similar al siguiente, que recupera información sobre la Directiva de voz por usuario RedmondVoicePolicy:</span><span class="sxs-lookup"><span data-stu-id="5e3b7-161">And then you can determine the PSTN usages (if any) that are assigned to that policy by using a command similar to the following, which retrieves information about the per-user voice policy RedmondVoicePolicy:</span></span>
    
        Get-CsVoicePolicy -Identity "RedmondVoicePolicy"

<span data-ttu-id="5e3b7-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5e3b7-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

