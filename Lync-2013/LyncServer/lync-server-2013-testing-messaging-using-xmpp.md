---
title: 'Lync Server 2013: probar la mensajería mediante XMPP'
description: 'Lync Server 2013: probar la mensajería con XMPP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing messaging using XMPP
ms:assetid: ae5305ba-e5fc-4ca0-a805-872b4ebaf981
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727312(v=OCS.15)
ms:contentKeyID: 63969641
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06faeae0a6104351f9102de31c76b2424a140deb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441007"
---
# <a name="testing-messaging-using-xmpp-in-lync-server-2013"></a><span data-ttu-id="4811f-103">Probar la mensajería con XMPP en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4811f-103">Testing messaging using XMPP in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4811f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4811f-104">

<span> </span></span></span>

<span data-ttu-id="4811f-105">_**Última modificación del tema:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="4811f-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4811f-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="4811f-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="4811f-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="4811f-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4811f-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="4811f-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="4811f-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4811f-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4811f-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="4811f-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="4811f-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="4811f-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="4811f-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe asignar un rol de RBAC que tenga permiso para ejecutar el cmdlet <strong>Test-CsXmppIM</strong> .</span><span class="sxs-lookup"><span data-stu-id="4811f-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsXmppIM</strong> cmdlet.</span></span> <span data-ttu-id="4811f-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="4811f-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsXmppIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="4811f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4811f-114">Description</span></span>

<span data-ttu-id="4811f-115">El protocolo de presencia y mensajería extensible (XMPP) es un protocolo de comunicaciones estándar (basado en XML) que se usa para enviar mensajes a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="4811f-115">The Extensible Messaging and Presence Protocol (XMPP) is a standard communications protocol (based on XML) used for sending messages across the Internet.</span></span> <span data-ttu-id="4811f-116">XMPP se llamaba originalmente Jabber y es compatible con varias aplicaciones de mensajería y comunicaciones de Internet, como Google Talk y la conversación de Facebook.</span><span class="sxs-lookup"><span data-stu-id="4811f-116">XMPP was originally named Jabber, and is supported by several Internet messaging and communication applications, such as Google Talk and Facebook Chat.</span></span> <span data-ttu-id="4811f-117">El cmdlet **Test-CsXmppIM** verifica que un usuario puede intercambiar mensajes instantáneos con un usuario en una red XMPP.</span><span class="sxs-lookup"><span data-stu-id="4811f-117">The **Test-CsXmppIM** cmdlet verifies that a user can exchange instant messages with a user on an XMPP network.</span></span> <span data-ttu-id="4811f-118">Tenga en cuenta que, para que esta prueba se realice correctamente, debe tener una dirección SIP válida para el usuario de XMPP, y esa dirección SIP debe estar en una red que se haya configurado como socio XMPP autorizado.</span><span class="sxs-lookup"><span data-stu-id="4811f-118">Note that, for this test to succeed, you must have a valid SIP address for the XMPP user, and that SIP address must be on a network that was configured as an allowed XMPP partner.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="4811f-119">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="4811f-119">Running the test</span></span>

<span data-ttu-id="4811f-120">En el ejemplo siguiente se comprueban las capacidades de mensajería instantánea de XMPP para el grupo atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="4811f-120">The following example verifies the XMPP instant messaging capabilities for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="4811f-121">Este comando solo funciona si se han definido usuarios de prueba para el grupo atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="4811f-121">This command will work only if test users are defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="4811f-122">De ser así, el comando determinará si el primer usuario de prueba puede enviar un mensaje instantáneo XMPP a un usuario que tenga la dirección SIP adelaney@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="4811f-122">If they have, then the command will determine whether the first test user can send an XMPP instant message to a user who has the SIP address adelaney@contoso.com.</span></span>

<span data-ttu-id="4811f-123">Si no se definen los usuarios de prueba, el comando fallará porque no sabrá en qué usuario iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="4811f-123">If test users are not defined, then the command will fail because it won't know which user to log on as.</span></span> <span data-ttu-id="4811f-124">Si no ha definido usuarios de prueba para un grupo, debe incluir el parámetro UserSipAddress y las credenciales del usuario que debe usar el comando al intentar iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="4811f-124">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user who the command should use when trying to log on.</span></span>

    Test-CsXmppIM -TargetFqdn "atl-cs-001.litwareinc.com" -Receiver "adelany@contoso.com"

<span data-ttu-id="4811f-125">Los comandos que se muestran en el siguiente ejemplo prueban la capacidad de un usuario específico (litwareinc \\ Pilar) para iniciar sesión y enviar un mensaje instantáneo XMPP a la adelaney@contoso.com de usuario.</span><span class="sxs-lookup"><span data-stu-id="4811f-125">The commands shown in the next example test the ability of a specific user (litwareinc\\pilar) to log on to send an XMPP instant message to the user adelaney@contoso.com.</span></span> <span data-ttu-id="4811f-126">Para ello, el primer comando del ejemplo usa el cmdlet Get-Credential para crear un objeto de credencial de interfaz de línea de comandos de Windows PowerShell que contiene el nombre y la contraseña del usuario Pilar Ackerman.</span><span class="sxs-lookup"><span data-stu-id="4811f-126">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="4811f-127">(Como el nombre de inicio de sesión litwareinc \\ Pilar se incluyó como parámetro, el cuadro de diálogo solicitud de credenciales de Windows PowerShell solo requiere que el administrador escriba la contraseña de la cuenta de Pilar Ackerman). El objeto de credencial resultante se almacena en una variable llamada $cred 1.</span><span class="sxs-lookup"><span data-stu-id="4811f-127">(Because the logon name litwareinc\\pilar was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credential object is then stored in a variable named $cred1.</span></span>

<span data-ttu-id="4811f-128">El segundo comando comprueba si este usuario puede iniciar sesión en el grupo atl-cs-001.litwareinc.com y enviar el mensaje instantáneo XMPP.</span><span class="sxs-lookup"><span data-stu-id="4811f-128">The second command then checks whether this user can log on to the pool atl-cs-001.litwareinc.com and send the XMPP instant message.</span></span> <span data-ttu-id="4811f-129">Para ejecutar esta tarea, se llama al cmdlet **Test-CsXmppIm** , junto con cuatro parámetros: TargetFqdn (el FQDN del grupo de servidores de registrar); Receptor (la dirección SIP del usuario al que se dirige el mensaje); UserCredential (el objeto de Windows PowerShell que contiene las credenciales de usuario de Pilar Ackerman); y UserSipAddress (la dirección SIP que corresponde a las credenciales de usuario suministradas).</span><span class="sxs-lookup"><span data-stu-id="4811f-129">To run this task, the **Test-CsXmppIm** cmdlet is called, together with four parameters: TargetFqdn (the FQDN of the Registrar pool); Receiver (the SIP address of the user the message is being addressed to); UserCredential (the Windows PowerShell object that contains Pilar Ackerman’s user credentials); and UserSipAddress (the SIP address that corresponds to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsXmppIM -TargetFqdn "atl-cs-001.litwareinc.com" -Receiver "adelany@contoso.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="4811f-130">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="4811f-130">Determining success or failure</span></span>

<span data-ttu-id="4811f-131">Si la mensajería instantánea XMPP está configurada correctamente, recibirá una salida similar a la siguiente, con la propiedad result marcada como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="4811f-131">If XMPP instant messaging is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="4811f-132">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4811f-132">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4811f-133">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="4811f-133">Result : Success</span></span>

<span data-ttu-id="4811f-134">Latencia: 00:00:02.5361946</span><span class="sxs-lookup"><span data-stu-id="4811f-134">Latency : 00:00:02.5361946</span></span>

<span data-ttu-id="4811f-135">Mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="4811f-135">Error Message :</span></span>

<span data-ttu-id="4811f-136">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="4811f-136">Diagnosis :</span></span>

<span data-ttu-id="4811f-137">Si los usuarios especificados no pueden usar la mensajería instantánea de XMPP, el resultado se mostrará como **error** y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="4811f-137">If the specified users can't use XMPP instant messaging, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="4811f-138">ADVERTENCIA: no se pudo leer el número de puerto del registrador para el nombre completo</span><span class="sxs-lookup"><span data-stu-id="4811f-138">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="4811f-139">nombre de dominio (FQDN).</span><span class="sxs-lookup"><span data-stu-id="4811f-139">domain name (FQDN).</span></span> <span data-ttu-id="4811f-140">Usando el número de puerto predeterminado del registrador.</span><span class="sxs-lookup"><span data-stu-id="4811f-140">Using default Registrar port number.</span></span> <span data-ttu-id="4811f-141">Excepción</span><span class="sxs-lookup"><span data-stu-id="4811f-141">Exception:</span></span>

<span data-ttu-id="4811f-142">System. InvalidOperationException: no se encontró ningún clúster coincidente en la topología.</span><span class="sxs-lookup"><span data-stu-id="4811f-142">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="4811f-143">en</span><span class="sxs-lookup"><span data-stu-id="4811f-143">at</span></span>

<span data-ttu-id="4811f-144">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="4811f-144">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="4811f-145">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="4811f-145">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="4811f-146">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4811f-146">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4811f-147">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="4811f-147">Result : Failure</span></span>

<span data-ttu-id="4811f-148">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4811f-148">Latency : 00:00:00</span></span>

<span data-ttu-id="4811f-149">Mensaje de error: 10060, error al intentar la conexión porque la persona conectada</span><span class="sxs-lookup"><span data-stu-id="4811f-149">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="4811f-150">no respondió correctamente después de un período de tiempo, o</span><span class="sxs-lookup"><span data-stu-id="4811f-150">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="4811f-151">error en la conexión establecida porque el host conectado tiene</span><span class="sxs-lookup"><span data-stu-id="4811f-151">established connection failed because connected host has</span></span>

<span data-ttu-id="4811f-152">Error al responder 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="4811f-152">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="4811f-153">Excepción interna: error en el intento de conexión porque el</span><span class="sxs-lookup"><span data-stu-id="4811f-153">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="4811f-154">la parte conectada no respondió correctamente después de un período de</span><span class="sxs-lookup"><span data-stu-id="4811f-154">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="4811f-155">hora o error de conexión establecida porque el host conectado</span><span class="sxs-lookup"><span data-stu-id="4811f-155">time, or established connection failed because connected host</span></span>

<span data-ttu-id="4811f-156">Error al responder 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="4811f-156">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="4811f-157">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="4811f-157">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="4811f-158">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="4811f-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="4811f-159">Estas son algunas de las razones comunes por las que **Test-CsXmppIM** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="4811f-159">Here are some common reasons why **Test-CsXmppIM** might fail:</span></span>

  - <span data-ttu-id="4811f-160">Se proporcionó un valor de parámetro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="4811f-160">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="4811f-161">Si se usa, los parámetros opcionales deben estar configurados correctamente o se producirá un error en la prueba.</span><span class="sxs-lookup"><span data-stu-id="4811f-161">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="4811f-162">Vuelva a ejecutar el comando sin los parámetros opcionales y vea si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4811f-162">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="4811f-163">Este comando fallará si la configuración de la puerta de enlace XMPP no se ha configurado correctamente o si aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="4811f-163">This command will fail if XMPP gateway configuration is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4811f-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="4811f-164">See Also</span></span>


[<span data-ttu-id="4811f-165">Set-CsXmppGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="4811f-165">Set-CsXmppGatewayConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsXmppGatewayConfiguration)  
  

<span data-ttu-id="4811f-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4811f-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

