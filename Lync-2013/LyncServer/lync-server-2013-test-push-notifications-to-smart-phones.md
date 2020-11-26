---
title: 'Lync Server 2013: probar las notificaciones de inserción en teléfonos inteligentes'
description: 'Lync Server 2013: Pruebe las notificaciones de inserción en teléfonos inteligentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test push notifications to smart phones
ms:assetid: 8f5ca7d1-1ccb-4cb0-b417-730559e79b6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767948(v=OCS.15)
ms:contentKeyID: 63969626
ms.date: 03/15/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b92ef444a5331c9a673fd2db506631554e96eea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441231"
---
# <a name="test-push-notifications-to-smart-phones-in-lync-server-2013"></a><span data-ttu-id="f5bd7-103">Probar las notificaciones Push a Smart Phone en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f5bd7-103">Test push notifications to smart phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f5bd7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f5bd7-104">

<span> </span></span></span>

<span data-ttu-id="f5bd7-105">_**Última modificación del tema:** 2017-03-15_</span><span class="sxs-lookup"><span data-stu-id="f5bd7-105">_**Topic Last Modified:** 2017-03-15_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5bd7-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="f5bd7-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="f5bd7-107">Cada mes</span><span class="sxs-lookup"><span data-stu-id="f5bd7-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5bd7-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="f5bd7-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="f5bd7-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f5bd7-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5bd7-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="f5bd7-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="f5bd7-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="f5bd7-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsMcxPushNotification.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxPushNotification cmdlet.</span></span> <span data-ttu-id="f5bd7-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxPushNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="f5bd7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5bd7-114">Description</span></span>

<span data-ttu-id="f5bd7-115">El servicio de notificaciones push (servicio de notificaciones push de Apple y servicio de notificaciones push de Microsoft) puede enviar notificaciones sobre eventos como nuevos mensajes instantáneos o un nuevo correo de voz a dispositivos móviles como iPhone y Windows Phone, incluso si el cliente Lync en esos dispositivos está suspendido o se está ejecutando en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-115">The push notification service (Apple Push Notification Service and Microsoft Push Notification Service) can send notifications about events such as new instant messages or new voice mail to mobile devices such as iPhones and Windows Phones, even if the Lync client on those devices is currently suspended or running in the background.</span></span> <span data-ttu-id="f5bd7-116">El servicio de notificaciones push es un servicio basado en la nube que se ejecuta en servidores de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-116">The push notification service is a cloud-based service that is running on Microsoft servers.</span></span> <span data-ttu-id="f5bd7-117">Para aprovechar las notificaciones push, debe poder conectarse a la conexión de notificaciones Push y autenticarla en él.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-117">In order to take advantage of push notifications, you must be able to connect to, and be authenticated by, the push notification clearinghouse.</span></span> <span data-ttu-id="f5bd7-118">El cmdlet Test-CsMcxPushNotification permite a los administradores comprobar que las solicitudes de notificaciones de inserción se pueden enrutar a través del servidor perimetral al centro de notificaciones Push.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-118">The Test-CsMcxPushNotification cmdlet enables administrators to verify that push notification requests can be routed through your Edge server to the push notification clearinghouse.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="f5bd7-119">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="f5bd7-119">Running the test</span></span>

<span data-ttu-id="f5bd7-120">Para probar el servicio de notificaciones de inserción, llama al cmdlet Test-CsMcxPushNotification.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-120">To test the push notification service, call the Test-CsMcxPushNotification cmdlet.</span></span> <span data-ttu-id="f5bd7-121">Asegúrese de especificar el nombre de dominio completo del servidor perimetral:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-121">Make sure that you specify the fully qualified domain name of your Edge server:</span></span>

    Test-CsMcxPushNotification -AccessEdgeFqdn "atl-edge-001.litwareinc.com"

<span data-ttu-id="f5bd7-122">Para obtener más información, vea el tema de ayuda para el cmdlet [Test-CsMcxPushNotification](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification) .</span><span class="sxs-lookup"><span data-stu-id="f5bd7-122">For more information, see the help topic for the [Test-CsMcxPushNotification](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="f5bd7-123">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="f5bd7-123">Determining success or failure</span></span>

<span data-ttu-id="f5bd7-124">Si Test-CsMcxPushNotification se ejecuta correctamente, el cmdlet devolverá el resultado de la prueba correcta:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-124">If Test-CsMcxPushNotification succeeds the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="f5bd7-125">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="f5bd7-125">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="f5bd7-126">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="f5bd7-126">Result : Success</span></span>

<span data-ttu-id="f5bd7-127">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f5bd7-127">Latency : 00:00:00</span></span>

<span data-ttu-id="f5bd7-128">:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-128">Error :</span></span>

<span data-ttu-id="f5bd7-129">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="f5bd7-129">Diagnosis :</span></span>

<span data-ttu-id="f5bd7-130">Si Test-CsMcxPushNotification no puede conectarse al centro de notificaciones push, el cmdlet normalmente no devolverá un resultado de prueba de error.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-130">If Test-CsMcxPushNotification is unable to connect to the push notification clearinghouse the cmdlet will typically not return a test result of Failure.</span></span> <span data-ttu-id="f5bd7-131">En su lugar, el comando fallará por completo.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-131">Instead the command will usually fail completely.</span></span> <span data-ttu-id="f5bd7-132">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-132">For example:</span></span>

<span data-ttu-id="f5bd7-133">Test-CsMcxPushNotification: se ha recibido una respuesta 504 (tiempo de espera del servidor) de la red y se ha producido un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-133">Test-CsMcxPushNotification : A 504 (Server time-out) response was received from the network and the operation failed.</span></span> <span data-ttu-id="f5bd7-134">Para obtener más información, consulta los detalles de la excepción.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-134">See the exception details for more information.</span></span>

<span data-ttu-id="f5bd7-135">En la línea: 1 carácter: 27</span><span class="sxs-lookup"><span data-stu-id="f5bd7-135">At line:1 char:27</span></span>

<span data-ttu-id="f5bd7-136">\+Test-CsMcxPushNotification \< \< \< \< AccessEdgeFqdn lyncedge.mydomain.com</span><span class="sxs-lookup"><span data-stu-id="f5bd7-136">\+ Test-CsMcxPushNotification \<\<\<\< -AccessEdgeFqdn lyncedge.mydomain.com</span></span>

<span data-ttu-id="f5bd7-137">\+ CategoryInfo: OperationStopped: (:) \[ Prueba-CsMcxPushNotification \] , FailureResponseException</span><span class="sxs-lookup"><span data-stu-id="f5bd7-137">\+ CategoryInfo : OperationStopped: (:) \[Test-CsMcxPushNotification\], FailureResponseException</span></span>

<span data-ttu-id="f5bd7-138">\+ FullyQualifiedErrorId: WorkflowNotCompleted, Microsoft. RTC. Management. SyntheticTransactions. TestMcxPushNotificationCmdlet</span><span class="sxs-lookup"><span data-stu-id="f5bd7-138">\+ FullyQualifiedErrorId : WorkflowNotCompleted,Microsoft.Rtc.Management.SyntheticTransactions.TestMcxPushNotificationCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="f5bd7-139">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="f5bd7-139">Reasons why the test might have failed</span></span>

<span data-ttu-id="f5bd7-140">Si se produce un error en el servicio de notificaciones Push que normalmente indica problemas de comunicación con el servidor perimetral o problemas de comunicación con el centro de enrutamiento de notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-140">If the push notification service fails that usually indicates either problems communicating with your Edge server, or problems communicating with the Push Notification Clearing House.</span></span> <span data-ttu-id="f5bd7-141">Si experimenta problemas al ejecutar test-CsMcxPushNotification, lo primero que debe hacer es comprobar que el servidor perimetral funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-141">If you encounter problems when you run Test-CsMcxPushNotification, the first thing that you should do is verify that your Edge server is working correctly.</span></span> <span data-ttu-id="f5bd7-142">Una forma de hacerlo es usar el cmdlet Test-CsAVEdgeConnectivity:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-142">One way to do that is to use the Test-CsAVEdgeConnectivity cmdlet:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsAVEdgeConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="f5bd7-143">Esta comprobación comprueba que un usuario especificado puede conectarse al servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-143">This check verifies that a specified user can connect to the Edge server.</span></span>

<span data-ttu-id="f5bd7-144">Si el servidor perimetral parece funcionar correctamente, eso a menudo significa que no puede conectarse al centro de notificaciones Push.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-144">If the Edge server seems to be working correctly, that often means that you are unable to connect to the push notification clearinghouse.</span></span> <span data-ttu-id="f5bd7-145">A su vez, eso significa que no ha configurado el URI de Clearinghouse correctamente o que no tiene un registro SRV de DNS que apunte a esta dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-145">In turn, that typically means that you either have not configured the clearinghouse URI correctly or that you do not have a DNS SRV record that points to this URL.</span></span> <span data-ttu-id="f5bd7-146">Puede comprobar que el URI está configurado con el valor correcto (sip:push@push.lync.com) ejecutando este comando:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-146">You can verify that the URI is set to the correct value (sip:push@push.lync.com) by running this command:</span></span>

    Get-CsMcxConfiguration

<span data-ttu-id="f5bd7-147">Si la propiedad PushNotificationProxyUri se establece en un valor distinto de sip:push@push.lync.com, puede corregir ese problema mediante el cmdlet Set-McxConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-147">If the PushNotificationProxyUri property is set to anything other than sip:push@push.lync.com then you can correct that problem by using the Set-McxConfiguration cmdlet.</span></span> <span data-ttu-id="f5bd7-148">Por ejemplo, este comando establece correctamente el URI en toda la organización:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-148">For example, this command correctly sets the URI throughout your organization:</span></span>

    Get-CsMcxConfiguration | Set-CsMcxConfiguration -PushNotificationProxyUri "sip:push@push.lync.com"

<span data-ttu-id="f5bd7-149">Para obtener más información, consulte el tema de ayuda para el cmdlet [set-CsMcxConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsMcxConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="f5bd7-149">For more information, see the help topic for the [Set-CsMcxConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsMcxConfiguration) cmdlet.</span></span>

<span data-ttu-id="f5bd7-150">Si el URI está configurado correctamente, el siguiente paso debe ser comprobar que tiene un registro SRV de DNS que se resuelve en el dominio SIP y en el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-150">If the URI is configured correctly, your next step should be to verify that you have a DNS SRV record that resolves to your SIP domain and your Edge server.</span></span> <span data-ttu-id="f5bd7-151">Para obtener más información sobre cómo configurar estos registros, vea el tema de ayuda sobre los requisitos de DNS para la movilidad.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-151">For more information about how to configure these records, see the help topic DNS Requirements for Mobility.</span></span> <span data-ttu-id="f5bd7-152">Tenga en cuenta que el siguiente mensaje de error suele indicar un problema con los registros DNS:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-152">Note that the following error message usually indicates a problem with DNS records:</span></span>

<span data-ttu-id="f5bd7-153">Se ha recibido una respuesta 504 (tiempo de espera del servidor) de la red y se ha producido un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-153">A 504 (Server time-out) response was received from the network and the operation failed.</span></span> <span data-ttu-id="f5bd7-154">Para obtener más información, consulta los detalles de la excepción.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-154">See the exception details for more information.</span></span>

<span data-ttu-id="f5bd7-155">También es posible que Test-CsMcxConfiguration falle con este mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-155">It’s also possible that Test-CsMcxConfiguration will fail with this error message:</span></span>

<span data-ttu-id="f5bd7-156">Test-CsMcxPushNotification: se rechazó la solicitud de notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-156">Test-CsMcxPushNotification : Push Notification request was rejected.</span></span>

<span data-ttu-id="f5bd7-157">En la línea: 1 carácter: 27</span><span class="sxs-lookup"><span data-stu-id="f5bd7-157">At line:1 char:27</span></span>

<span data-ttu-id="f5bd7-158">\+ Test-CsMcxPushNotification \<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="f5bd7-158">\+ Test-CsMcxPushNotification \<\<\<\<</span></span>

<span data-ttu-id="f5bd7-159">\+ CategoryInfo: OperationStopped: (:) \[ Prueba-CsMcxPushNotification \] , SyntheticTransactionException</span><span class="sxs-lookup"><span data-stu-id="f5bd7-159">\+ CategoryInfo : OperationStopped: (:) \[Test-CsMcxPushNotification\], SyntheticTransactionException</span></span>

<span data-ttu-id="f5bd7-160">\+ FullyQualifiedErrorId: WorkflowNotCompleted, Microsoft. RTC. Management. SyntheticTransactions. TestMcxPushNotificationCmdlet</span><span class="sxs-lookup"><span data-stu-id="f5bd7-160">\+ FullyQualifiedErrorId : WorkflowNotCompleted,Microsoft.Rtc.Management.SyntheticTransactions.TestMcxPushNotificationCmdlet</span></span>

<span data-ttu-id="f5bd7-161">El mensaje "se rechazó la solicitud de notificación de inserción" suele ocurrir si ha habilitado el filtrado de URL y está bloqueando los prefijos http: y https:.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-161">The “Push notification request was rejected” message typically occurs if you have enabled URL filtering and are blocking the http: and https: prefixes.</span></span> <span data-ttu-id="f5bd7-162">Puede determinar qué prefijos se están bloqueando mediante un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-162">You can determine which prefixes are being blocked by using a command similar to the following:</span></span>

```PowerShell 
 (Get-CsImFilterConfiguration -Identity Global).Prefixes
```

<span data-ttu-id="f5bd7-163">Si http: o https: aparecen en los resultados, debe eliminarlos de la lista de prefijos bloqueados para que las notificaciones de inserción funcionen.</span><span class="sxs-lookup"><span data-stu-id="f5bd7-163">If http: or https: appear in the results, you must remove them from the blocked prefix list for push notifications to work.</span></span> <span data-ttu-id="f5bd7-164">Esto se puede hacer con comandos similares a estos:</span><span class="sxs-lookup"><span data-stu-id="f5bd7-164">That can be done by using commands similar to these:</span></span>

    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="http:"}
    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="https:"}

<span data-ttu-id="f5bd7-165">Para obtener más información, consulte el tema de ayuda para el cmdlet [set-CsImFilterConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsImFilterConfiguration).</span><span class="sxs-lookup"><span data-stu-id="f5bd7-165">For more information, see the help topic for the [Set-CsImFilterConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsImFilterConfiguration)cmdlet.</span></span>

<span data-ttu-id="f5bd7-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f5bd7-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

