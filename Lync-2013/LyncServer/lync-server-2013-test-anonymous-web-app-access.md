---
title: 'Lync Server 2013: probar el acceso anónimo a aplicaciones Web'
description: 'Lync Server 2013: Pruebe el acceso anónimo a la aplicación Web.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test anonymous Web App access
ms:assetid: 92f691cd-e05e-4bab-beb5-251d4b837a19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767949(v=OCS.15)
ms:contentKeyID: 63969630
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c33840912fefcaeef069e14773cfefd0834a8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441273"
---
# <a name="test-anonymous-web-app-access-in-lync-server-2013"></a><span data-ttu-id="91035-103">Probar el acceso anónimo a aplicaciones web en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91035-103">Test anonymous Web App access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91035-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91035-104">

<span> </span></span></span>

<span data-ttu-id="91035-105">_**Última modificación del tema:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="91035-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91035-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="91035-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="91035-107">Cada mes</span><span class="sxs-lookup"><span data-stu-id="91035-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91035-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="91035-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="91035-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="91035-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91035-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="91035-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="91035-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="91035-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="91035-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsWebAppAnonymous.</span><span class="sxs-lookup"><span data-stu-id="91035-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsWebAppAnonymous cmdlet.</span></span> <span data-ttu-id="91035-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91035-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebAppAnonymous&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="91035-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="91035-114">Description</span></span>

<span data-ttu-id="91035-115">El cmdlet Test-CsWebAppAnonymous comprueba que un usuario anónimo puede unirse a conferencias de Lync Server mediante Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="91035-115">The Test-CsWebAppAnonymous cmdlet verifies that an anonymous user can join Lync Server conferences by using the Lync Web App.</span></span> <span data-ttu-id="91035-116">Al ejecutar el cmdlet, Test-CsWebAppAnonymous se pone en contacto con el servicio de vales web para obtener un vale web para el usuario anónimo.</span><span class="sxs-lookup"><span data-stu-id="91035-116">When you run the cmdlet, Test-CsWebAppAnonymous contacts the Web Ticket service to obtain a web ticket for the anonymous user.</span></span> <span data-ttu-id="91035-117">Si el cmdlet consigue obtener este vale, Test-CsWebAppAnonymous se pondrá en contacto con Lync Server e intentará establecer conferencias independientes para la mensajería instantánea, el uso compartido de aplicaciones y la colaboración de datos.</span><span class="sxs-lookup"><span data-stu-id="91035-117">If the cmdlet succeeds in obtaining this ticket, Test-CsWebAppAnonymous will then contact Lync Server and attempt to establish separate conferences for instant messaging, application sharing, and data collaboration.</span></span>

<span data-ttu-id="91035-118">Tenga en cuenta que Test-CsWebAppAnonymous solo comprueba las API y las conexiones usadas para crear estas conferencias.</span><span class="sxs-lookup"><span data-stu-id="91035-118">Note that Test-CsWebAppAnonymous only verifies the APIs and connections used to create these conferences.</span></span> <span data-ttu-id="91035-119">En realidad, el cmdlet no crea ni dirige ninguna Conferencia.</span><span class="sxs-lookup"><span data-stu-id="91035-119">The cmdlet does not actually create and conduct any conferences.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="91035-120">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="91035-120">Running the test</span></span>

<span data-ttu-id="91035-121">El cmdlet Test-CsWebAppAnonymous se puede ejecutar con un par de cuentas de prueba preconfiguradas o con las cuentas de dos usuarios que están habilitados para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91035-121">The Test-CsWebAppAnonymous cmdlet can be run using either a pair of preconfigured test accounts or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="91035-122">Para ejecutar esta comprobación mediante cuentas de prueba, solo tiene que especificar el nombre de dominio completo del grupo de servidores de Lync que se está probando.</span><span class="sxs-lookup"><span data-stu-id="91035-122">To run this check using test accounts, you just have to specify the fully qualified domain name of the Lync Server pool being tested.</span></span> <span data-ttu-id="91035-123">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="91035-123">For example:</span></span>

    Test-CsWebAppAnonymous -TargetFqdn atl-cs-001.litwareinc.com

<span data-ttu-id="91035-124">Para ejecutar esta comprobación con las cuentas de usuario reales, debe crear dos objetos de credenciales del shell de administración de Lync Server (objetos que contengan el nombre y la contraseña de la cuenta) de cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="91035-124">To run this check using actual user accounts, you must create two Lync Server Management Shell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="91035-125">Después, debe incluir esos objetos de credenciales y las direcciones SIP de las dos cuentas cuando llame a test-CsWebAppAnonymous:</span><span class="sxs-lookup"><span data-stu-id="91035-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsWebAppAnonymous:</span></span>

    $cred1 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1

<span data-ttu-id="91035-126">Para obtener más información, consulte el tema de ayuda para el cmdlet Test-CsWebAppAnonymous.</span><span class="sxs-lookup"><span data-stu-id="91035-126">For more information, see the help topic for the Test-CsWebAppAnonymous cmdlet.</span></span> <span data-ttu-id="91035-127">Tenga en cuenta que Test-CsWebAppAnonymous está en desuso para su uso en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="91035-127">Note that Test-CsWebAppAnonymous is deprecated for use on Lync Server 2013.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="91035-128">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="91035-128">Determining success or failure</span></span>

<span data-ttu-id="91035-129">Si Test-CsWebAppAnonymous puede unir al usuario anónimo a su conferencia, el cmdlet devolverá el resultado de la prueba correcto:</span><span class="sxs-lookup"><span data-stu-id="91035-129">If Test-CsWebAppAnonymous can join the anonymous user to his or her conferences, the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="91035-130">FQDN de destino:</span><span class="sxs-lookup"><span data-stu-id="91035-130">Target Fqdn :</span></span>

<span data-ttu-id="91035-131">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="91035-131">Result : Success</span></span>

<span data-ttu-id="91035-132">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="91035-132">Latency : 00:00:00</span></span>

<span data-ttu-id="91035-133">Mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="91035-133">Error Message :</span></span>

<span data-ttu-id="91035-134">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="91035-134">Diagnosis :</span></span>

<span data-ttu-id="91035-135">Si el usuario anónimo no puede unirse a las conferencias necesarias, el resultado de la prueba se marcará como erróneo.</span><span class="sxs-lookup"><span data-stu-id="91035-135">If the anonymous user can't join the necessary conferences then the test result will be marked as Failure.</span></span> <span data-ttu-id="91035-136">Por lo general, Test-CsWebAppAnonymous también devolverá un mensaje de error y un diagnóstico detallados:</span><span class="sxs-lookup"><span data-stu-id="91035-136">Typically Test-CsWebAppAnonymous will also report back a detailed error message and diagnosis:</span></span>

<span data-ttu-id="91035-137">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="91035-137">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="91035-138">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="91035-138">Result : Failure</span></span>

<span data-ttu-id="91035-139">Latencia: 00:00:05.9746266</span><span class="sxs-lookup"><span data-stu-id="91035-139">Latency : 00:00:05.9746266</span></span>

<span data-ttu-id="91035-140">Mensaje de error: no se recibió respuesta para el servicio Web-Ticket</span><span class="sxs-lookup"><span data-stu-id="91035-140">Error Message : No response received for Web-Ticket service</span></span>

<span data-ttu-id="91035-141">Diagnóstico: la solicitud HTTP no está autorizada con el cliente</span><span class="sxs-lookup"><span data-stu-id="91035-141">Diagnosis : The HTTP request is unauthorized with client</span></span>

<span data-ttu-id="91035-142">esquema de autenticación ' NTLM '.</span><span class="sxs-lookup"><span data-stu-id="91035-142">authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="91035-143">La autenticación</span><span class="sxs-lookup"><span data-stu-id="91035-143">The authentication</span></span>

<span data-ttu-id="91035-144">el encabezado recibido del servidor era ' Negotiate, NTLM '.</span><span class="sxs-lookup"><span data-stu-id="91035-144">header received from the server was 'Negotiate,NTLM'.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="91035-145">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="91035-145">Reasons why the test might have failed</span></span>

<span data-ttu-id="91035-146">Los errores de Test-CsWebAppAnonymous suelen girar en relación con errores de autenticación de usuario: debe ejecutar la prueba con una cuenta de usuario válida, aunque el cmdlet está comprobando la capacidad de un usuario anónimo para conectarse a Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91035-146">Test-CsWebAppAnonymous failures usually revolve around user authentication errors: you must run the test using a valid user account even though the cmdlet is checking the ability of an anonymous user to connect to Lync Server.</span></span> <span data-ttu-id="91035-147">Si Test-CsWebAppAnonymous da error, debe comprobar que el usuario especificado tiene una cuenta de usuario válida de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91035-147">If Test-CsWebAppAnonymous fails, you should verify that the specified user has valid a Lync Server user account.</span></span> <span data-ttu-id="91035-148">Puede recuperar la información de la cuenta de Lync Server mediante un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="91035-148">You can retrieve Lync Server account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="91035-149">Si la propiedad Enabled no es igual a true o si se produce un error en el comando, significa que el usuario no tiene una cuenta válida de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91035-149">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.</span></span>

<span data-ttu-id="91035-150">También debe comprobar que la contraseña que proporcionó al ejecutar el cmdlet es una contraseña válida.</span><span class="sxs-lookup"><span data-stu-id="91035-150">You should also verify that the password that you supplied when you run the cmdlet is a valid password.</span></span>

<span data-ttu-id="91035-151">Los problemas de configuración con Office Web Apps Server también pueden hacer que Test-CsWebAppAnonymous no se realice correctamente; Esto suele ser el caso si recibe el siguiente diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="91035-151">Configuration problems with Office Web Apps Server can also cause Test-CsWebAppAnonymous to fail; that will often be the case if you receive the following diagnosis:</span></span>

<span data-ttu-id="91035-152">La solicitud HTTP no está autorizada con el esquema de autenticación de cliente ' NTLM '.</span><span class="sxs-lookup"><span data-stu-id="91035-152">The HTTP request is unauthorized with client authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="91035-153">El encabezado de autenticación recibido desde el servidor era ' Negotiate, NTLM '.</span><span class="sxs-lookup"><span data-stu-id="91035-153">The authentication header received from the server was 'Negotiate,NTLM'.</span></span>

<span data-ttu-id="91035-154">Para obtener más información sobre cómo diagnosticar y resolver problemas de Office Web Apps Server, consulte el blog de las aplicaciones de correo de Office [Web Apps server 2013: los equipos se muestran siempre como en mal estado](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy).</span><span class="sxs-lookup"><span data-stu-id="91035-154">For more information on diagnosing and resolving Office Web Apps Server problems see the blog post [Office Web Apps Server 2013 - machines are always reported as Unhealthy](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy).</span></span>

<span data-ttu-id="91035-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91035-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

