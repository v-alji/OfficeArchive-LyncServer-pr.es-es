---
title: 'Lync Server 2013: posibilidad de probar los mensajes instantáneos de los usuarios móviles'
description: 'Lync Server 2013: posibilidad de que los usuarios móviles puedan intercambiar mensajes instantáneos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test mobile users' ability to exchange instant messages
ms:assetid: a78a048f-d413-4bee-8626-d62b8b74f811
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767950(v=OCS.15)
ms:contentKeyID: 63969638
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 675bbeff93fed374d950b2efbdf15b4ea246f861
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444262"
---
# <a name="test-mobile-users-ability-to-exchange-instant-messages-in-lync-server-2013"></a><span data-ttu-id="42540-103">Probar la capacidad de los usuarios móviles para intercambiar mensajes instantáneos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42540-103">Test mobile users' ability to exchange instant messages in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42540-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42540-104">

<span> </span></span></span>

<span data-ttu-id="42540-105">_**Última modificación del tema:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="42540-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42540-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="42540-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="42540-107">Cada mes</span><span class="sxs-lookup"><span data-stu-id="42540-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42540-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="42540-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="42540-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="42540-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42540-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="42540-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="42540-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="42540-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="42540-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsMcxP2PIM.</span><span class="sxs-lookup"><span data-stu-id="42540-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxP2PIM cmdlet.</span></span> <span data-ttu-id="42540-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="42540-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxP2PIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="42540-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="42540-114">Description</span></span>

<span data-ttu-id="42540-115">El servicio de movilidad permite que los usuarios de dispositivos móviles realicen estas acciones como:</span><span class="sxs-lookup"><span data-stu-id="42540-115">The Mobility Service enables mobile device users to do such things as:</span></span>

1.  <span data-ttu-id="42540-116">Intercambia mensajes instantáneos e información de presencia.</span><span class="sxs-lookup"><span data-stu-id="42540-116">Exchange instant messages and presence information.</span></span>

2.  <span data-ttu-id="42540-117">Almacene y recupere el correo de voz internamente en lugar de con su proveedor de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="42540-117">Store and retrieve voice mail internally instead of with their wireless provider.</span></span>

3.  <span data-ttu-id="42540-118">Aproveche las capacidades de Lync Server, como las llamadas a través del trabajo y las conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="42540-118">Take advantage of Lync Server capabilities such as Call via Work and dial-out conferencing.</span></span>

<span data-ttu-id="42540-119">El cmdlet Test-CsMxcP2PIM ofrece una manera rápida y sencilla de comprobar que los usuarios pueden usar el servicio de movilidad para intercambiar mensajes instantáneos.</span><span class="sxs-lookup"><span data-stu-id="42540-119">The Test-CsMxcP2PIM cmdlet provides a quick and easy way to verify that users can use the Mobility Service to exchange instant messages.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="42540-120">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="42540-120">Running the test</span></span>

<span data-ttu-id="42540-121">Para ejecutar esta prueba, debe crear dos objetos de credenciales de Windows PowerShell (objetos que contengan el nombre y la contraseña de la cuenta) de cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="42540-121">To run this test, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="42540-122">Después, debe incluir esos objetos de credenciales y las direcciones SIP de las dos cuentas cuando llame a test-CsMcxP2PIM:</span><span class="sxs-lookup"><span data-stu-id="42540-122">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsMcxP2PIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\pilar"
    
    Test-CsMcxP2PIM -TargetFqdn "atl-cs-001.litwareinc.com" -Authentication Negotiate -SenderSipAddres "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:packerman@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="42540-123">Para obtener más información, vea el tema de ayuda para el cmdlet [Test-CsMcxP2PIM](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM) .</span><span class="sxs-lookup"><span data-stu-id="42540-123">For more information, see the help topic for the [Test-CsMcxP2PIM](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="42540-124">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="42540-124">Determining success or failure</span></span>

<span data-ttu-id="42540-125">Si los dos usuarios de prueba pueden intercambiar mensajes instantáneos con el servicio de movilidad, Test-CsMcxP2PIM devolverá el resultado de la prueba correcto:</span><span class="sxs-lookup"><span data-stu-id="42540-125">If the two test users can exchange instant messages by using the mobility service then Test-CsMcxP2PIM will return test result Success:</span></span>

<span data-ttu-id="42540-126">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="42540-126">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="42540-127">URI de destino: http://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="42540-127">Target Uri : http://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="42540-128">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="42540-128">Result : Success</span></span>

<span data-ttu-id="42540-129">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="42540-129">Latency : 00:00:00</span></span>

<span data-ttu-id="42540-130">Mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="42540-130">Error Message :</span></span>

<span data-ttu-id="42540-131">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="42540-131">Diagnosis :</span></span>

<span data-ttu-id="42540-132">Si se produce un error en la prueba, el resultado se establecerá en error y aparecerá un mensaje de error detallado y un diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="42540-132">If the test fails then the Result will be set to Failure and a detailed error message and diagnosis will be displayed:</span></span>

<span data-ttu-id="42540-133">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="42540-133">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="42540-134">URI de destino: https://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="42540-134">Target Uri : https://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="42540-135">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="42540-135">Result : Failure</span></span>

<span data-ttu-id="42540-136">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="42540-136">Latency : 00:00:00</span></span>

<span data-ttu-id="42540-137">Mensaje de error: no se recibió ninguna respuesta para el servicio Web-Ticket.</span><span class="sxs-lookup"><span data-stu-id="42540-137">Error Message : No response received for Web-Ticket service.</span></span>

<span data-ttu-id="42540-138">Excepción interna: la solicitud HHTP no está autorizada con</span><span class="sxs-lookup"><span data-stu-id="42540-138">Inner Exception:The HHTP request is unauthorized with</span></span>

<span data-ttu-id="42540-139">esquema de negociación de cliente ' NTLM '.</span><span class="sxs-lookup"><span data-stu-id="42540-139">client negotiation scheme 'Ntlm'.</span></span> <span data-ttu-id="42540-140">La autenticación</span><span class="sxs-lookup"><span data-stu-id="42540-140">The authentication</span></span>

<span data-ttu-id="42540-141">el encabezado recibido del servidor era ' Negotiate, NTLM '.</span><span class="sxs-lookup"><span data-stu-id="42540-141">header received from the server was 'Negotiate,NTLM'.</span></span>

<span data-ttu-id="42540-142">Excepción interna: el servidor remoto devolvió un error:</span><span class="sxs-lookup"><span data-stu-id="42540-142">Inner Exception:The remote server returned an error:</span></span>

<span data-ttu-id="42540-143">(401) no autorizado.</span><span class="sxs-lookup"><span data-stu-id="42540-143">(401) Unauthorized.</span></span>

<span data-ttu-id="42540-144">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="42540-144">Diagnosis :</span></span>

<span data-ttu-id="42540-145">Diagnosis interior: X-MS-Server-Fqdb: ATL-CS-</span><span class="sxs-lookup"><span data-stu-id="42540-145">Inner Diagnosis:X-MS-server-Fqdb : atl-cs-</span></span>

<span data-ttu-id="42540-146">001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="42540-146">001.litwareinc.com</span></span>

<span data-ttu-id="42540-147">Cache-Control: privado</span><span class="sxs-lookup"><span data-stu-id="42540-147">Cache-Control : private</span></span>

<span data-ttu-id="42540-148">Tipo de contenido: text/html; charset = utf-8.</span><span class="sxs-lookup"><span data-stu-id="42540-148">Content-Type : text/html; charset=utf-8.</span></span>

<span data-ttu-id="42540-149">Servidor: Microsoft-IIS/8.5</span><span class="sxs-lookup"><span data-stu-id="42540-149">Server : Microsoft-IIS/8.5</span></span>

<span data-ttu-id="42540-150">WWW-Authenticate: Negotiate, NTLM</span><span class="sxs-lookup"><span data-stu-id="42540-150">WWW-Authenticate : Negotiate,NTLM</span></span>

<span data-ttu-id="42540-151">Alimentado por X: ASP.NET</span><span class="sxs-lookup"><span data-stu-id="42540-151">X-Powered-By : ASP.NET</span></span>

<span data-ttu-id="42540-152">Opciones de tipo de contenido X: nosniffing</span><span class="sxs-lookup"><span data-stu-id="42540-152">X-Content-Type-Options : nosniff</span></span>

<span data-ttu-id="42540-153">Fecha: miércoles, 28 de mayo de 2014 19:16:05 GMT</span><span class="sxs-lookup"><span data-stu-id="42540-153">Date : Wed, 28 May 2014 19:16:05 GMT</span></span>

<span data-ttu-id="42540-154">Longitud del contenido: 6305</span><span class="sxs-lookup"><span data-stu-id="42540-154">Content-Length : 6305</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="42540-155">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="42540-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="42540-156">Si Test-CsMcxP2PIM no supera el primer paso debe ser comprobar que el servicio de movilidad está funcionando.</span><span class="sxs-lookup"><span data-stu-id="42540-156">If Test-CsMcxP2PIM fails your first step should be to verify that the mobility service is up and running.</span></span> <span data-ttu-id="42540-157">Esto se puede realizar con un explorador Web para comprobar que se puede acceder a la dirección URL del servicio de movilidad de su grupo de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="42540-157">That can be done by using a web browser to verify that the mobility service URL for your Lync Server pool can be accessed.</span></span> <span data-ttu-id="42540-158">Por ejemplo, este comando comprueba la dirección URL del grupo atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="42540-158">For example, this command verifies the URL for the pool atl-cs-001.litwareinc.com:</span></span>

    https://atl-cs-001.litwareinc.com/mcx/mcxservice.svc

<span data-ttu-id="42540-159">Si el servicio de movilidad parece estar ejecutándose, compruebe que los dos usuarios de prueba tengan cuentas válidas de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="42540-159">If the mobility service seems to be running then verify that your two test users have valid Lync Server accounts.</span></span> <span data-ttu-id="42540-160">Puede recuperar información de la cuenta mediante un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="42540-160">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="42540-161">Si la propiedad Enabled no es igual a true o si se produce un error en el comando, significa que el usuario no tiene una cuenta válida de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="42540-161">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.</span></span>

<span data-ttu-id="42540-162">También debe comprobar que el usuario está habilitado para la movilidad.</span><span class="sxs-lookup"><span data-stu-id="42540-162">You should also verify that the user is enabled for mobility.</span></span> <span data-ttu-id="42540-163">Para ello, primero determine la Directiva de movilidad que está asignada a la cuenta:</span><span class="sxs-lookup"><span data-stu-id="42540-163">To do that, first determine the mobility policy that is assigned to the account:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object MobilityPolicy

<span data-ttu-id="42540-164">Una vez que conozca el nombre de la Directiva, use el cmdlet Get-CsMobilityPolicy para comprobar que la Directiva en cuestión (por ejemplo, RedmondMobilityPolicy) tiene la propiedad EnableMobility establecida en true:</span><span class="sxs-lookup"><span data-stu-id="42540-164">After you know the policy name, use the Get-CsMobilityPolicy cmdlet to verify that the policy in question (for example, RedmondMobilityPolicy) has the EnableMobility property set to True:</span></span>

    Get-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

<span data-ttu-id="42540-165">Si recibe un mensaje de error con encabezados de autenticación, eso a menudo significa que no ha especificado una cuenta de usuario válida.</span><span class="sxs-lookup"><span data-stu-id="42540-165">If you receive an error message with authentication headers, that often means that you have not specified a valid user account.</span></span> <span data-ttu-id="42540-166">Compruebe el nombre de usuario y la contraseña y, a continuación, vuelva a intentar la prueba.</span><span class="sxs-lookup"><span data-stu-id="42540-166">Verify the user name and password and then try the test again.</span></span> <span data-ttu-id="42540-167">Si estás convencido de que la cuenta de usuario es válida, usa el cmdlet Get-CsWebServiceConfiguration y verifica el valor de la propiedad UseWindowsAuth.</span><span class="sxs-lookup"><span data-stu-id="42540-167">If you are convinced that the user account is valid, then use the Get-CsWebServiceConfiguration cmdlet and check the value of the UseWindowsAuth property.</span></span> <span data-ttu-id="42540-168">Que le indicará qué métodos de autenticación están habilitados en su organización. Para obtener más información sobre cómo solucionar problemas del servicio de movilidad, vea la [solución de problemas de la conectividad de movilidad de Lync externa](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span><span class="sxs-lookup"><span data-stu-id="42540-168">That will tell you which authentication methods are enabled in your organization.For more tips about how to troubleshoot the mobility service, see the blog post [Troubleshooting External Lync Mobility Connectivity Issues Step-by-Step](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span></span>

<span data-ttu-id="42540-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42540-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

