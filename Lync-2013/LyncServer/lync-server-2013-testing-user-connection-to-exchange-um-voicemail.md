---
title: 'Lync Server 2013: probar la conexión del usuario para intercambiar el buzón de voz de mensajería unificada'
description: 'Lync Server 2013: probar la conexión del usuario para intercambiar el buzón de voz de mensajería unificada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user connection to Exchange UM voicemail
ms:assetid: 574da104-8823-4061-9fb6-353639f1884d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727305(v=OCS.15)
ms:contentKeyID: 63969604
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b887b5b0df02a5864e0a39f2b62893d20105a86a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439719"
---
# <a name="testing-user-connection-to-exchange-um-voicemail-in-lync-server-2013"></a><span data-ttu-id="391d3-103">Probar la conexión de usuario para intercambiar el buzón de voz de mensajería unificada en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="391d3-103">Testing user connection to Exchange UM voicemail in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="391d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="391d3-104">

<span> </span></span></span>

<span data-ttu-id="391d3-105">_**Última modificación del tema:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="391d3-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="391d3-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="391d3-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="391d3-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="391d3-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="391d3-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="391d3-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="391d3-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="391d3-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="391d3-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="391d3-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="391d3-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="391d3-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="391d3-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe asignar un rol de RBAC que tenga permiso para ejecutar el cmdlet <strong>Test-CsExUMVoiceMail</strong> .</span><span class="sxs-lookup"><span data-stu-id="391d3-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExUMVoiceMail</strong> cmdlet.</span></span> <span data-ttu-id="391d3-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="391d3-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExUMVoiceMail&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="391d3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="391d3-114">Description</span></span>

<span data-ttu-id="391d3-115">El cmdlet **Test-CsExUMVoiceMail** permite a los administradores comprobar que un usuario puede obtener acceso y usar el servicio de mensajería unificada de Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="391d3-115">The **Test-CsExUMVoiceMail** cmdlet enables administrators to verify that a user can access and use the Microsoft Exchange Server 2013 unified messaging service.</span></span> <span data-ttu-id="391d3-116">Para ello, el cmdlet se conecta al servicio de mensajería unificada y deja un correo de voz en el buzón especificado.</span><span class="sxs-lookup"><span data-stu-id="391d3-116">To do this, the cmdlet connects to the unified messaging service and leaves a voice mail in the specified mailbox.</span></span> <span data-ttu-id="391d3-117">Puede ser un correo de voz suministrado por el sistema o puede ser un. WAV que haya grabado usted mismo.</span><span class="sxs-lookup"><span data-stu-id="391d3-117">This can be a system-supplied voice mail, or it can be a custom .WAV file that you have recorded yourself.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="391d3-118">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="391d3-118">Running the test</span></span>

<span data-ttu-id="391d3-119">En el siguiente ejemplo se prueba la Conectividad del correo de voz de mensajería unificada de Exchange para el grupo atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="391d3-119">The following example tests Exchange Unified Messaging voice mail connectivity for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="391d3-120">Este comando solo funcionará si se definieron usuarios de prueba para el grupo atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="391d3-120">This command will work only if test users were defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="391d3-121">De ser así, el comando determinará si el primer usuario de prueba puede usar el correo de voz de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="391d3-121">If they have, then the command will determine whether the first test user can use Unified Messaging voice mail.</span></span> <span data-ttu-id="391d3-122">Si no se han configurado los usuarios de prueba para el grupo, el comando fallará.</span><span class="sxs-lookup"><span data-stu-id="391d3-122">If test users were not configured for the pool then the command will fail.</span></span>

    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" 

<span data-ttu-id="391d3-123">Los comandos que aparecen en el siguiente ejemplo de prueba de la Conectividad del correo de voz de mensajería unificada de Exchange para el usuario litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="391d3-123">The commands shown in the next example test Exchange Unified Messaging voice mail connectivity for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="391d3-124">Para ello, el primer comando del ejemplo usa el cmdlet **Get-Credential** para crear un objeto de credenciales de la interfaz de línea de comandos de Windows PowerShell para el usuario litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="391d3-124">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credentials object for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="391d3-125">Tenga en cuenta que debe proporcionar la contraseña de esta cuenta para crear un objeto de credenciales válido y asegurarse de que el cmdlet **Test-CsExUMVoiceMail** puede ejecutar su comprobación.</span><span class="sxs-lookup"><span data-stu-id="391d3-125">Note that you must supply the password for this account to create a valid credentials object and to ensure that the **Test-CsExUMVoiceMail** cmdlet can run its check.</span></span>

<span data-ttu-id="391d3-126">El segundo comando del ejemplo usa el objeto de credenciales proporcionado ($x) y la dirección SIP del usuario litwareinc \\ kenmyer para determinar si este usuario puede conectarse al correo de voz de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="391d3-126">The second command in the example uses the supplied credentials object ($x) and the SIP address of the user litwareinc\\kenmyer to determine whether or this user can connect to Exchange Unified Messaging voice mail.</span></span>

    $credential = Get-Credential "litwareinc\pilar" 
    
    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $credential 

<span data-ttu-id="391d3-127">El comando que se muestra en el ejemplo siguiente es una variación del comando que se muestra en el ejemplo 1; en este caso, se incluye el parámetro OutLoggerVariable para generar un registro detallado de cada paso realizado por la **CsExUMVoiceMail de prueba** cmdletand el éxito o el fracaso de cada uno de estos pasos.</span><span class="sxs-lookup"><span data-stu-id="391d3-127">The command shown in the next example is a variation of the command shown in Example 1; in this case, the OutLoggerVariable parameter is included to generate a detailed log of every step done by the **Test-CsExUMVoiceMail** cmdletand the success or failure of each of those steps.</span></span> <span data-ttu-id="391d3-128">Para ello, se agrega el parámetro OutLoggerVariable junto al valor de parámetro ExumText; Esto provoca que la información de registro detallada se almacene en una variable denominada $ExumTest.</span><span class="sxs-lookup"><span data-stu-id="391d3-128">To do this, the OutLoggerVariable parameter is added alongside the parameter value ExumText; that causes detailed logging information to be stored in a variable named $ExumTest.</span></span> <span data-ttu-id="391d3-129">En el último comando del ejemplo, el método ToXML () se usa para convertir la información de registro a formato XML.</span><span class="sxs-lookup"><span data-stu-id="391d3-129">In the final command in the example, the ToXML() method is used to convert the log information to XML format.</span></span> <span data-ttu-id="391d3-130">Esos datos XML se escriben en un archivo denominado C: \\ Logs \\VoicemailTest.xml con el cmdlet Out-File.</span><span class="sxs-lookup"><span data-stu-id="391d3-130">That XML data is then written to a file that is named C:\\Logs\\VoicemailTest.xml by using the Out-File cmdlet.</span></span>

    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -OutLoggerVariable VoicemailTest 
     
    $VoicemailTest.ToXML() | Out-File C:\Logs\VoicemailTest.xml

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="391d3-131">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="391d3-131">Determining success or failure</span></span>

<span data-ttu-id="391d3-132">Si la integración de Exchange se ha configurado correctamente, recibirá un resultado similar a este, con la propiedad result marcada como **correcta**:</span><span class="sxs-lookup"><span data-stu-id="391d3-132">If Exchange integration is correctly configured, you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="391d3-133">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="391d3-133">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="391d3-134">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="391d3-134">Result : Success</span></span>

<span data-ttu-id="391d3-135">Latencia: 00:00:02.9911345</span><span class="sxs-lookup"><span data-stu-id="391d3-135">Latency : 00:00:02.9911345</span></span>

<span data-ttu-id="391d3-136">Mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="391d3-136">Error Message :</span></span>

<span data-ttu-id="391d3-137">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="391d3-137">Diagnosis :</span></span>

<span data-ttu-id="391d3-138">Si el usuario especificado no puede conectarse al buzón de voz, el resultado se mostrará como **error** y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="391d3-138">If the specified user can't connect to voicemail, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="391d3-139">ADVERTENCIA: no se pudo leer el número de puerto del registrador para el nombre completo</span><span class="sxs-lookup"><span data-stu-id="391d3-139">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="391d3-140">nombre de dominio (FQDN).</span><span class="sxs-lookup"><span data-stu-id="391d3-140">domain name (FQDN).</span></span> <span data-ttu-id="391d3-141">Usando el número de puerto predeterminado del registrador.</span><span class="sxs-lookup"><span data-stu-id="391d3-141">Using default Registrar port number.</span></span> <span data-ttu-id="391d3-142">Excepción</span><span class="sxs-lookup"><span data-stu-id="391d3-142">Exception:</span></span>

<span data-ttu-id="391d3-143">System. InvalidOperationException: no se encontró ningún clúster coincidente en la topología.</span><span class="sxs-lookup"><span data-stu-id="391d3-143">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="391d3-144">en</span><span class="sxs-lookup"><span data-stu-id="391d3-144">at</span></span>

<span data-ttu-id="391d3-145">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="391d3-145">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="391d3-146">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="391d3-146">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="391d3-147">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="391d3-147">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="391d3-148">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="391d3-148">Result : Failure</span></span>

<span data-ttu-id="391d3-149">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="391d3-149">Latency : 00:00:00</span></span>

<span data-ttu-id="391d3-150">Mensaje de error: 10060, error al intentar la conexión porque la persona conectada</span><span class="sxs-lookup"><span data-stu-id="391d3-150">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="391d3-151">no respondió correctamente después de un período de tiempo, o</span><span class="sxs-lookup"><span data-stu-id="391d3-151">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="391d3-152">error en la conexión establecida porque el host conectado tiene</span><span class="sxs-lookup"><span data-stu-id="391d3-152">established connection failed because connected host has</span></span>

<span data-ttu-id="391d3-153">Error al responder 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="391d3-153">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="391d3-154">Excepción interna: error en el intento de conexión porque el</span><span class="sxs-lookup"><span data-stu-id="391d3-154">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="391d3-155">la parte conectada no respondió correctamente después de un período de</span><span class="sxs-lookup"><span data-stu-id="391d3-155">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="391d3-156">hora o error de conexión establecida porque el host conectado</span><span class="sxs-lookup"><span data-stu-id="391d3-156">time, or established connection failed because connected host</span></span>

<span data-ttu-id="391d3-157">Error al responder 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="391d3-157">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="391d3-158">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="391d3-158">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="391d3-159">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="391d3-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="391d3-160">Estas son algunas de las razones comunes por las que **Test-CsExUMVoiceMail** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="391d3-160">Here are some common reasons why **Test-CsExUMVoiceMail** might fail:</span></span>

  - <span data-ttu-id="391d3-161">Se proporcionó un valor de parámetro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="391d3-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="391d3-162">Si se usa, los parámetros opcionales deben estar configurados correctamente o se producirá un error en la prueba.</span><span class="sxs-lookup"><span data-stu-id="391d3-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="391d3-163">Vuelva a ejecutar el comando sin los parámetros opcionales y vea si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="391d3-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="391d3-164">Este comando fallará si el servidor de Exchange está mal configurado o aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="391d3-164">This command will fail if the Exchange Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="391d3-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="391d3-165">See Also</span></span>


[<span data-ttu-id="391d3-166">Test-CsExUMConnectivity</span><span class="sxs-lookup"><span data-stu-id="391d3-166">Test-CsExUMConnectivity</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExUMConnectivity)  
  

<span data-ttu-id="391d3-167"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="391d3-167"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

