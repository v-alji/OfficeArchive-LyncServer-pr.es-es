---
title: 'Lync Server 2013: pruebas de chat persistente'
description: 'Lync Server 2013: pruebas de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing persistent chat
ms:assetid: d351b6f2-bc31-42e0-9e8d-c347713d6b4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727313(v=OCS.15)
ms:contentKeyID: 63969651
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8b1dc4eef1870f1287dacdc1852ab1e24edd169
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441000"
---
# <a name="testing-persistent-chat-in-lync-server-2013"></a><span data-ttu-id="19ed1-103">Prueba de la conversación persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19ed1-103">Testing persistent chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19ed1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19ed1-104">

<span> </span></span></span>

<span data-ttu-id="19ed1-105">_**Última modificación del tema:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="19ed1-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19ed1-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="19ed1-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="19ed1-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="19ed1-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19ed1-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="19ed1-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="19ed1-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="19ed1-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19ed1-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="19ed1-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="19ed1-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="19ed1-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="19ed1-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe asignar un rol de RBAC que tenga permiso para ejecutar el cmdlet <strong>Test-CsPersistentChatMessage</strong> .</span><span class="sxs-lookup"><span data-stu-id="19ed1-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsPersistentChatMessage</strong> cmdlet.</span></span> <span data-ttu-id="19ed1-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="19ed1-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPersistentChatMessage&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="19ed1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="19ed1-114">Description</span></span>

<span data-ttu-id="19ed1-115">El cmdlet **Test-CsPersistentChatMessage** verifica que un par de usuarios de prueba puedan intercambiar mensajes con el servicio de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="19ed1-115">The **Test-CsPersistentChatMessage** cmdlet verifies that a pair of test users can exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="19ed1-116">Para ello, el cmdlet registra los dos usuarios en Lync Server 2013, conecta los usuarios a un salón de chat persistente, intercambia un par de mensajes y, a continuación, sale del salón de chat y cierra la sesión de los dos usuarios.</span><span class="sxs-lookup"><span data-stu-id="19ed1-116">To do this, the cmdlet logs the two users on to Lync Server 2013, connects the users to a persistent Chat room, exchanges a pair of messages, then exits the chat room and logs off the two users.</span></span> <span data-ttu-id="19ed1-117">Observe que las llamadas a este cmdlet fallarán si no ha creado ningún salón de chat o si las dos cuentas de usuario de prueba no tienen asignada una directiva de chat persistente que les proporcione acceso al servicio de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="19ed1-117">Note that calls to this cmdlet will fail if you have not created any chat rooms or if the two test user accounts are not assigned a Persistent Chat policy that gives them access to the Persistent Chat service.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="19ed1-118">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="19ed1-118">Running the test</span></span>

<span data-ttu-id="19ed1-119">Los comandos que se muestran en el siguiente ejemplo prueban la capacidad de un par de usuarios (litwareinc \\ Pilar y litwareinc \\ kenmyer) para iniciar sesión en Lync Server 2013 y, a continuación, intercambiar mensajes con el servicio de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="19ed1-119">The commands shown in the following example test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to log on to Lync Server 2013 and then exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="19ed1-120">Para ello, el primer comando del ejemplo usa el cmdlet **Get-Credential** para crear un objeto de credencial de interfaz de línea de comandos de Windows PowerShell que contiene el nombre y la contraseña del usuario Pilar Ackerman.</span><span class="sxs-lookup"><span data-stu-id="19ed1-120">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="19ed1-121">(Como el nombre de inicio de sesión, litwareinc \\ pilar, se incluyó como parámetro, el cuadro de diálogo solicitud de credenciales de Windows PowerShell solo requiere que el administrador escriba la contraseña de la cuenta de Pilar Ackerman). El objeto de credenciales resultante se almacena en una variable llamada $cred 1.</span><span class="sxs-lookup"><span data-stu-id="19ed1-121">(Because the logon name, litwareinc\\pilar, was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credentials object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="19ed1-122">El segundo comando hace lo mismo, pero esta vez devuelve un objeto de credenciales para la cuenta Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="19ed1-122">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="19ed1-123">Con los objetos de credenciales a mano, el tercer comando determina si estos dos usuarios pueden iniciar sesión en Lync Server 2013 y intercambiar mensajes con el chat persistente.</span><span class="sxs-lookup"><span data-stu-id="19ed1-123">With the credential objects in hand, the third command determines whether these two users can log on to Lync Server 2013 and exchange messages using Persistent Chat.</span></span> <span data-ttu-id="19ed1-124">Para realizar esta tarea, se llama al cmdlet **Test-CsPersistentChatMessage** con los siguientes parámetros: TargetFqdn (el FQDN del grupo de servidores de registrar); SenderSipAddress (dirección SIP del primer usuario de prueba); SenderCredential (el objeto de Windows PowerShell que contiene las credenciales de este mismo usuario); ReceiverSipAddress (la dirección SIP del otro usuario de prueba); y ReceiverCredential (el objeto de Windows PowerShell que contiene las credenciales del otro usuario de prueba).</span><span class="sxs-lookup"><span data-stu-id="19ed1-124">To perform this task, the **Test-CsPersistentChatMessage** cmdlet is called using the following parameters: TargetFqdn (the FQDN of the Registrar pool); SenderSipAddress (the SIP address for the first test user); SenderCredential (the Windows PowerShell object that contains the credentials for this same user); ReceiverSipAddress (the SIP address for the other test user); and ReceiverCredential (the Windows PowerShell object that contains the credentials for the other test user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsPersistentChatMessage -TargetFqdn atl-persistentchat-001.litwareinc.com -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $cred1 -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -ReceiverCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="19ed1-125">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="19ed1-125">Determining success or failure</span></span>

<span data-ttu-id="19ed1-126">Si el usuario especificado tiene una directiva de ubicación válida, recibirá una salida similar a la siguiente, con la propiedad result marcada como **correcta**:</span><span class="sxs-lookup"><span data-stu-id="19ed1-126">If the specified user has a valid location policy, then you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="19ed1-127">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="19ed1-127">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="19ed1-128">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="19ed1-128">Result : Success</span></span>

<span data-ttu-id="19ed1-129">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="19ed1-129">Latency : 00:00:00</span></span>

<span data-ttu-id="19ed1-130">Mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="19ed1-130">Error Message :</span></span>

<span data-ttu-id="19ed1-131">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="19ed1-131">Diagnosis :</span></span>

<span data-ttu-id="19ed1-132">Si los usuarios especificados no pueden intercambiar mensajes con el servicio de chat persistente, el resultado se mostrará como **error** y la información adicional se registrará en las propiedades de error y diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="19ed1-132">If the specified users can't exchange messages using the Persistent Chat service, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="19ed1-133">ADVERTENCIA: no se pudo leer el número de puerto del registrador para el nombre completo</span><span class="sxs-lookup"><span data-stu-id="19ed1-133">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="19ed1-134">nombre de dominio (FQDN).</span><span class="sxs-lookup"><span data-stu-id="19ed1-134">domain name (FQDN).</span></span> <span data-ttu-id="19ed1-135">Usando el número de puerto predeterminado del registrador.</span><span class="sxs-lookup"><span data-stu-id="19ed1-135">Using default Registrar port number.</span></span> <span data-ttu-id="19ed1-136">Excepción</span><span class="sxs-lookup"><span data-stu-id="19ed1-136">Exception:</span></span>

<span data-ttu-id="19ed1-137">System. InvalidOperationException: no se encontró ningún clúster coincidente en la topología.</span><span class="sxs-lookup"><span data-stu-id="19ed1-137">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="19ed1-138">en</span><span class="sxs-lookup"><span data-stu-id="19ed1-138">at</span></span>

<span data-ttu-id="19ed1-139">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="19ed1-139">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="19ed1-140">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="19ed1-140">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="19ed1-141">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="19ed1-141">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="19ed1-142">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="19ed1-142">Result : Failure</span></span>

<span data-ttu-id="19ed1-143">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="19ed1-143">Latency : 00:00:00</span></span>

<span data-ttu-id="19ed1-144">Mensaje de error: 10060, error al intentar la conexión porque la persona conectada</span><span class="sxs-lookup"><span data-stu-id="19ed1-144">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="19ed1-145">no respondió correctamente después de un período de tiempo, o</span><span class="sxs-lookup"><span data-stu-id="19ed1-145">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="19ed1-146">error en la conexión establecida porque el host conectado tiene</span><span class="sxs-lookup"><span data-stu-id="19ed1-146">established connection failed because connected host has</span></span>

<span data-ttu-id="19ed1-147">Error al responder \[ 2001:4898: E8: f39e: 5c9a: ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="19ed1-147">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="19ed1-148">Excepción interna: error en el intento de conexión porque el</span><span class="sxs-lookup"><span data-stu-id="19ed1-148">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="19ed1-149">la parte conectada no respondió correctamente después de un período de</span><span class="sxs-lookup"><span data-stu-id="19ed1-149">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="19ed1-150">hora o error de conexión establecida porque el host conectado</span><span class="sxs-lookup"><span data-stu-id="19ed1-150">time, or established connection failed because connected host</span></span>

<span data-ttu-id="19ed1-151">Error al responder</span><span class="sxs-lookup"><span data-stu-id="19ed1-151">has failed to respond</span></span>

<span data-ttu-id="19ed1-152">\[2001:4898: E8: f39e: 5c9a: ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="19ed1-152">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="19ed1-153">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="19ed1-153">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="19ed1-154">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="19ed1-154">Reasons why the test might have failed</span></span>

<span data-ttu-id="19ed1-155">Estas son algunas de las razones comunes por las que **Test-CsPersistentChatMessage** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="19ed1-155">Here are some common reasons why **Test-CsPersistentChatMessage** might fail:</span></span>

  - <span data-ttu-id="19ed1-156">Se proporcionó un valor de parámetro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="19ed1-156">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="19ed1-157">Es posible que las cuentas de prueba necesarias no existan o se hayan creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="19ed1-157">The required test accounts may not exist or have been correctly created.</span></span>

  - <span data-ttu-id="19ed1-158">Es posible que se haya producido un problema de red que ocasionó un retraso inesperado en el que se agotó la prueba.</span><span class="sxs-lookup"><span data-stu-id="19ed1-158">There may have been a network issue causing an unexpected delay which timed out the test.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="19ed1-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="19ed1-159">See Also</span></span>


[<span data-ttu-id="19ed1-160">Grant-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="19ed1-160">Grant-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsPersistentChatPolicy)  
[<span data-ttu-id="19ed1-161">New-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="19ed1-161">New-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsPersistentChatPolicy)  
[<span data-ttu-id="19ed1-162">Set-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="19ed1-162">Set-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsPersistentChatPolicy)  
  

<span data-ttu-id="19ed1-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19ed1-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

