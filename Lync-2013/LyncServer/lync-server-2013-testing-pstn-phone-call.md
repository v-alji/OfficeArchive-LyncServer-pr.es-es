---
title: 'Lync Server 2013: prueba de llamadas telefónicas RTC'
description: 'Lync Server 2013: prueba de llamadas telefónicas RTC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call
ms:assetid: dc7d319d-a627-45b6-a978-6111901251e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690133(v=OCS.15)
ms:contentKeyID: 63969656
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b42ea6dd46145961a34386d704f8f44e9b7909ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439768"
---
# <a name="testing-pstn-phone-call-in-lync-server-2013"></a><span data-ttu-id="3b630-103">Prueba de llamadas telefónicas RTC en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b630-103">Testing PSTN phone call in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b630-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b630-104">

<span> </span></span></span>

<span data-ttu-id="3b630-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="3b630-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b630-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="3b630-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="3b630-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="3b630-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b630-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="3b630-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="3b630-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3b630-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b630-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="3b630-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="3b630-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="3b630-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="3b630-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsRegistration.</span><span class="sxs-lookup"><span data-stu-id="3b630-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsRegistration cmdlet.</span></span> <span data-ttu-id="3b630-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3b630-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPstnOutboundCall&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="3b630-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b630-114">Description</span></span>

<span data-ttu-id="3b630-115">El cmdlet Test-CsPstnOutboundCall prueba la posibilidad de que un usuario realice una llamada a un número de teléfono ubicado en la RTC.</span><span class="sxs-lookup"><span data-stu-id="3b630-115">The Test-CsPstnOutboundCall cmdlet tests the ability of a user to make a call to a phone number located on the PSTN.</span></span> <span data-ttu-id="3b630-116">Al ejecutar test-CsPstnOutboundCall, el cmdlet primero intenta registrar el usuario de prueba en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3b630-116">When you run Test-CsPstnOutboundCall, the cmdlet first attempts to log the test user on to Lync Server.</span></span> <span data-ttu-id="3b630-117">Si el inicio de sesión se realiza correctamente, el cmdlet intentará realizar una llamada telefónica en la puerta de enlace PSTN.</span><span class="sxs-lookup"><span data-stu-id="3b630-117">If the logon succeeds, the cmdlet will then try to make a phone call across the PSTN gateway.</span></span> <span data-ttu-id="3b630-118">Esta llamada telefónica se realizará con el plan de marcado, la Directiva de voz y otras directivas y parámetros asignados a la cuenta de prueba.</span><span class="sxs-lookup"><span data-stu-id="3b630-118">This phone call will be made using the dial plan, voice policy, and other policies and settings assigned to the test account.</span></span> <span data-ttu-id="3b630-119">Cuando se responde a la llamada, el cmdlet envía códigos de multifrecuencia de doble tono (DTMF) a través de la red para comprobar la conectividad de los medios.</span><span class="sxs-lookup"><span data-stu-id="3b630-119">When the call is answered, the cmdlet sends dual-tone multi-frequency (DTMF) codes over the network to verify media connectivity.</span></span>

<span data-ttu-id="3b630-120">Al realizar su prueba, Test-CsPstnOutboundCall realizará una llamada real: el teléfono de destino sonará y debe responderse para que la prueba se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="3b630-120">When conducting its test, Test-CsPstnOutboundCall will make an actual phone call: the target phone will ring and must be answered for the test to succeed.</span></span> <span data-ttu-id="3b630-121">Esta llamada también debe ser finalizada manualmente por el administrador.</span><span class="sxs-lookup"><span data-stu-id="3b630-121">This call must also be manually ended by the administrator.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="3b630-122">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="3b630-122">Running the test</span></span>

<span data-ttu-id="3b630-123">El cmdlet Test-CsPstnOutboundCall se puede ejecutar mediante una cuenta de prueba preconfigurada (consulte Configurar cuentas de prueba para ejecutar pruebas de Lync Server) o la cuenta de cualquier usuario que esté habilitado para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3b630-123">The Test-CsPstnOutboundCall cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="3b630-124">Para ejecutar esta comprobación mediante una cuenta de prueba, solo tiene que especificar el FQDN del grupo de Lync Server que se está probando y el número de teléfono RTC al que se llama.</span><span class="sxs-lookup"><span data-stu-id="3b630-124">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the PSTN phone number being called.</span></span> <span data-ttu-id="3b630-125">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3b630-125">For example:</span></span>

    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219"

<span data-ttu-id="3b630-126">Para ejecutar esta comprobación mediante una cuenta de usuario real, primero debe crear un objeto de credenciales de Windows PowerShell que contenga el nombre de la cuenta y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="3b630-126">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="3b630-127">Después debes incluir ese objeto de credenciales y la dirección SIP asignada a la cuenta al llamar a test-CsPstnOutboundCall:</span><span class="sxs-lookup"><span data-stu-id="3b630-127">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsPstnOutboundCall:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="3b630-128">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsPstnOutboundCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall) .</span><span class="sxs-lookup"><span data-stu-id="3b630-128">For more information, see the Help documentation for the [Test-CsPstnOutboundCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="3b630-129">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="3b630-129">Determining success or failure</span></span>

<span data-ttu-id="3b630-130">Si el usuario especificado puede realizar la llamada y se responde a la llamada, recibirá una salida similar a la siguiente y la propiedad result se marcará como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="3b630-130">If the specified user can make the call, and if the call is answered, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="3b630-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3b630-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3b630-132">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="3b630-132">Result : Success</span></span>

<span data-ttu-id="3b630-133">Latencia: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="3b630-133">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="3b630-134">:</span><span class="sxs-lookup"><span data-stu-id="3b630-134">Error :</span></span>

<span data-ttu-id="3b630-135">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="3b630-135">Diagnosis :</span></span>

<span data-ttu-id="3b630-136">Si el usuario especificado no puede hacer la llamada o si la llamada no es contestada, el resultado se mostrará como error y la información adicional se registrará en las propiedades de error y diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="3b630-136">If the specified user can't make the call or if the call is not answered, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="3b630-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3b630-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3b630-138">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="3b630-138">Result : Failure</span></span>

<span data-ttu-id="3b630-139">Latencia: 00:00:0987365</span><span class="sxs-lookup"><span data-stu-id="3b630-139">Latency : 00:00:0987365</span></span>

<span data-ttu-id="3b630-140">Error: 403, prohibido</span><span class="sxs-lookup"><span data-stu-id="3b630-140">Error : 403, Forbidden</span></span>

<span data-ttu-id="3b630-141">Diagnosis: ErrorCode = 12001, Source = ATL-CS-001. litwareinc. com, Reason = User</span><span class="sxs-lookup"><span data-stu-id="3b630-141">Diagnosis : ErrorCode=12001,Source=atl-cs-001.litwareinc.com,Reason=User</span></span>

<span data-ttu-id="3b630-142">La Directiva no contiene uso de la ruta telefónica</span><span class="sxs-lookup"><span data-stu-id="3b630-142">Policy does not contain phone route usage</span></span>

<span data-ttu-id="3b630-143">El resultado anterior indica que no se pudo realizar la prueba porque la Directiva de voz asignada al usuario especificado no incluye un uso de teléfono.</span><span class="sxs-lookup"><span data-stu-id="3b630-143">The previous output states that the test failed because the voice policy assigned to the specified user does not include a phone usage.</span></span> <span data-ttu-id="3b630-144">(Las directivas de voz se asocian con las directivas de voz.</span><span class="sxs-lookup"><span data-stu-id="3b630-144">(Phone usages tie voice policies to voice routes.</span></span> <span data-ttu-id="3b630-145">Sin una directiva de voz y una ruta de voz correspondiente, no puede hacer llamadas a través de la RTC.</span><span class="sxs-lookup"><span data-stu-id="3b630-145">Without both a voice policy and a corresponding voice route you can't make calls over the PSTN.)</span></span>

<span data-ttu-id="3b630-146">Si Test-CsPstnOutboundCall da error, es posible que desee volver a ejecutar la prueba, esta vez incluido el parámetro detallado:</span><span class="sxs-lookup"><span data-stu-id="3b630-146">If Test-CsPstnOutboundCall fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219" -Verbose

<span data-ttu-id="3b630-147">Cuando se incluye el parámetro detallado, Test-CsPstnOutboundCall devolverá una cuenta paso a paso de cada acción que se probó cuando se comprobó la capacidad del usuario especificado para iniciar sesión en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3b630-147">When the Verbose parameter is included, Test-CsPstnOutboundCall will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="3b630-148">Por ejemplo, esta salida indica que hay problemas de red que impiden una conexión con la RTC:</span><span class="sxs-lookup"><span data-stu-id="3b630-148">For example, this output indicates that network problems are preventing a connection with the PSTN:</span></span>

<span data-ttu-id="3b630-149">Establecer videollamadas de audio a ' SIP: + 12065551219@litwareinc. com; User = Phone '.</span><span class="sxs-lookup"><span data-stu-id="3b630-149">Establishing Audio Video call to 'sip:+12065551219@litwareinc.com;user=phone'.</span></span>

<span data-ttu-id="3b630-150">Se ha recibido una respuesta ' una 404 (no se encontró) de la red y se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="3b630-150">An exception 'A 404 (Not Found) response was received from the network and the operation failed.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="3b630-151">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="3b630-151">Reasons why the test might have failed</span></span>

<span data-ttu-id="3b630-152">Estas son algunas de las razones comunes por las que Test-CsPstnOutboundCall puede dar error:</span><span class="sxs-lookup"><span data-stu-id="3b630-152">Here are some common reasons why Test-CsPstnOutboundCall might fail:</span></span>

  - <span data-ttu-id="3b630-153">Ha especificado una cuenta de usuario no válida.</span><span class="sxs-lookup"><span data-stu-id="3b630-153">You specified an invalid user account.</span></span> <span data-ttu-id="3b630-154">Puede comprobar que una cuenta de usuario existe ejecutando un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="3b630-154">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="3b630-155">La cuenta de usuario es válida, pero la cuenta no está habilitada actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3b630-155">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="3b630-156">Para comprobar que una cuenta de usuario está habilitada para Lync Server, ejecute un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="3b630-156">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="3b630-157">Si la propiedad Enabled se establece en false, significa que el usuario no está habilitado actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3b630-157">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="3b630-158">La Directiva de voz asignada al usuario especificado no tiene un uso de RTC válido.</span><span class="sxs-lookup"><span data-stu-id="3b630-158">The voice policy assigned to the specified user does not have a valid PSTN usage.</span></span> <span data-ttu-id="3b630-159">Puede determinar la Directiva de voz asignada a un usuario mediante un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="3b630-159">You can determine the voice policy that is assigned to a user by using a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object VoicePolicy
    
    <span data-ttu-id="3b630-160">Y, después, puede determinar los usos de RTC (si los hay) que se asignan a esa Directiva mediante un comando similar al siguiente, que recupera información sobre la Directiva de voz por usuario RedmondVoicePolicy:</span><span class="sxs-lookup"><span data-stu-id="3b630-160">And then you can determine the PSTN usages (if any) that are assigned to that policy by using a command similar to the following, which retrieves information about the per-user voice policy RedmondVoicePolicy:</span></span>
    
        Get-CsVoicePolicy -Identity "RedmondVoicePolicy"

<span data-ttu-id="3b630-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b630-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

