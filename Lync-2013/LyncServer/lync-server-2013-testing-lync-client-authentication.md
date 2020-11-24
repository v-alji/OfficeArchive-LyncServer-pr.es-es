---
title: 'Lync Server 2013: comprobación de la autenticación de clientes de Lync'
description: 'Lync Server 2013: comprobación de la autenticación de clientes de Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Client authentication
ms:assetid: e22114cb-4456-4e5f-93ab-51592c4a8209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689120(v=OCS.15)
ms:contentKeyID: 63969659
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03694b7fd56d7847d8d493304b97af335d2a5b4d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398940"
---
# <a name="testing-lync-client-authentication-in-lync-server-2013"></a><span data-ttu-id="0b66f-103">Prueba de la autenticación de clientes de Lync en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b66f-103">Testing Lync Client authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b66f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b66f-104">

<span> </span></span></span>

<span data-ttu-id="0b66f-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="0b66f-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b66f-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="0b66f-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="0b66f-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="0b66f-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b66f-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="0b66f-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="0b66f-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0b66f-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b66f-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="0b66f-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="0b66f-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="0b66f-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="0b66f-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsClientAuth.</span><span class="sxs-lookup"><span data-stu-id="0b66f-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="0b66f-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="0b66f-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsClientAuth&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="0b66f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b66f-114">Description</span></span>

<span data-ttu-id="0b66f-115">El cmdlet Test-CsClientAuth le permite determinar si un usuario puede iniciar sesión en el servidor de Lync con un certificado de cliente, puede ejecutar el cmdlet Test-CsClientAuth.</span><span class="sxs-lookup"><span data-stu-id="0b66f-115">The Test-CsClientAuth cmdlet enables you to determine whether a user can log on to the Lync Server by using a client certificate, you can run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="0b66f-116">Después de llamar a test-CsClientAuth, el cmdlet se pondrá en contacto con el servicio de aprovisionamiento de certificados y descargará una copia de todos los certificados de cliente del usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="0b66f-116">After calling Test-CsClientAuth, the cmdlet will contact the certificate provisioning service and download a copy of any client certificates for the specified user.</span></span> <span data-ttu-id="0b66f-117">Si se puede encontrar y descargar un certificado de cliente, Test-CsClientAuth intentará iniciar sesión con ese certificado.</span><span class="sxs-lookup"><span data-stu-id="0b66f-117">If a client certificate can be found and downloaded, Test-CsClientAuth will then attempt to log on by using that certificate.</span></span> <span data-ttu-id="0b66f-118">Si el inicio de sesión se realiza correctamente, Test-CsClientAuth cerrará sesión e informará de que la prueba se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b66f-118">If logon succeeds, Test-CsClientAuth will log off and report that the test succeeded.</span></span> <span data-ttu-id="0b66f-119">Si un certificado no se puede encontrar o descargar, o si el cmdlet no puede iniciar sesión con ese certificado, Test-CsClientAuth notificará que se produjo un error en la prueba.</span><span class="sxs-lookup"><span data-stu-id="0b66f-119">If a certificate cannot be found or downloaded, or if the cmdlet is unable to logon using that certificate, then Test-CsClientAuth will report that the test failed.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="0b66f-120">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="0b66f-120">Running the test</span></span>

<span data-ttu-id="0b66f-121">El cmdlet Test-CsClientAuth se ejecuta con la cuenta de cualquier usuario que esté habilitado para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0b66f-121">The Test-CsClientAuth cmdlet is run by using the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="0b66f-122">Para ejecutar esta comprobación mediante una cuenta de usuario real, primero debe crear un objeto de credenciales de Windows PowerShell que contenga el nombre de la cuenta y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="0b66f-122">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="0b66f-123">Después, debes incluir ese objeto de credenciales y la dirección SIP asignada a la cuenta cuando el sistema llame test-CsClientAuth:</span><span class="sxs-lookup"><span data-stu-id="0b66f-123">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsClientAuth:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="0b66f-124">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsClientAuth](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) .</span><span class="sxs-lookup"><span data-stu-id="0b66f-124">For more information, see the Help documentation for the [Test-CsClientAuth](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="0b66f-125">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="0b66f-125">Determining success or failure</span></span>

<span data-ttu-id="0b66f-126">Si el usuario especificado puede iniciar sesión en Lync Server con un certificado de cliente, recibirá una salida similar a la siguiente y la propiedad result se marcará como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="0b66f-126">If the specified user can log on to Lync Server by using a client certificate, you will receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="0b66f-127">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="0b66f-127">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="0b66f-128">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="0b66f-128">Result : Success</span></span>

<span data-ttu-id="0b66f-129">Latencia: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="0b66f-129">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="0b66f-130">:</span><span class="sxs-lookup"><span data-stu-id="0b66f-130">Error :</span></span>

<span data-ttu-id="0b66f-131">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="0b66f-131">Diagnosis :</span></span>

<span data-ttu-id="0b66f-132">Si el usuario especificado no puede iniciar sesión, el resultado se mostrará como error y se registrará información adicional en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="0b66f-132">If the specified user can not log on, the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="0b66f-133">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="0b66f-133">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="0b66f-134">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="0b66f-134">Result : Failure</span></span>

<span data-ttu-id="0b66f-135">Latencia: 00:00:03.3645259</span><span class="sxs-lookup"><span data-stu-id="0b66f-135">Latency : 00:00:03.3645259</span></span>

<span data-ttu-id="0b66f-136">Error: no se pudo descargar un certificado CS para el usuario dado.</span><span class="sxs-lookup"><span data-stu-id="0b66f-136">Error : Could not download a CS Certificate for the given user.</span></span> <span data-ttu-id="0b66f-137">Comprobar si</span><span class="sxs-lookup"><span data-stu-id="0b66f-137">Check if</span></span>

<span data-ttu-id="0b66f-138">el URI y las credenciales proporcionados son correctos.</span><span class="sxs-lookup"><span data-stu-id="0b66f-138">provided uri and credentials are correct.</span></span>

<span data-ttu-id="0b66f-139">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="0b66f-139">Diagnosis :</span></span>

<span data-ttu-id="0b66f-140">Por ejemplo, la salida anterior indica que se produjo un error en la prueba porque no se encontró un certificado de cliente válido para el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="0b66f-140">For example, the previous output states that the test failed because a valid client certificate couldn't be located for the specified user.</span></span> <span data-ttu-id="0b66f-141">Puede devolver una lista de los certificados de cliente emitidos para un usuario ejecutando un comando de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="0b66f-141">You can return a list of the client certificates issued to a user by running a command as follows:</span></span>

    Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="0b66f-142">Si Test-CsClientAuth da error, es posible que desee volver a ejecutar la prueba, esta vez incluido el parámetro detallado:</span><span class="sxs-lookup"><span data-stu-id="0b66f-142">If Test-CsClientAuth fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential -Verbose

<span data-ttu-id="0b66f-143">Cuando se incluye el parámetro detallado, Test-CsClientAuth devolverá una cuenta paso a paso de cada acción que se probó cuando se comprobó la capacidad del usuario especificado para iniciar sesión en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0b66f-143">When the Verbose parameter is included, Test-CsClientAuth will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="0b66f-144">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0b66f-144">For example:</span></span>

<span data-ttu-id="0b66f-145">Intentando descargar un certificado CS para el usuario: kenmyer@litwareinc.com Endpoint: STEpid</span><span class="sxs-lookup"><span data-stu-id="0b66f-145">Trying to download a CS certificate for User : kenmyer@litwareinc.com endpoint : STEpid</span></span>

<span data-ttu-id="0b66f-146">Dirección URL del servicio Web: https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="0b66f-146">Web Service url : https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span></span>

<span data-ttu-id="0b66f-147">No se pudo descargar un certificado CS del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="0b66f-147">Could not download a CS certificate from web service.</span></span>

<span data-ttu-id="0b66f-148">Si</span><span class="sxs-lookup"><span data-stu-id="0b66f-148">CHECK:</span></span>

<span data-ttu-id="0b66f-149">\- La dirección URL del servicio web es válida y los servicios web son funcionales</span><span class="sxs-lookup"><span data-stu-id="0b66f-149">\- Web service url is valid and the web services are functional</span></span>

<span data-ttu-id="0b66f-150">\-Si usas PhoneNo \\ \\ PIN para autenticar, asegúrate de que coincidan con el URI de usuario.</span><span class="sxs-lookup"><span data-stu-id="0b66f-150">\- If using PhoneNo\\\\Pin to authenticate, make sure they match the user uri</span></span>

<span data-ttu-id="0b66f-151">\- Si usa NTLM \\ Kerberos auth, asegúrese de que ha proporcionado credenciales válidas</span><span class="sxs-lookup"><span data-stu-id="0b66f-151">\- If using NTLM\\Kerberos auth, make sure you provided valid credentials</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="0b66f-152">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="0b66f-152">Reasons why the test might have failed</span></span>

<span data-ttu-id="0b66f-153">Estas son algunas de las razones comunes por las que Test-CsClientAuth puede dar error:</span><span class="sxs-lookup"><span data-stu-id="0b66f-153">Here are some common reasons why Test-CsClientAuth might fail:</span></span>

  - <span data-ttu-id="0b66f-154">Ha especificado una cuenta de usuario que no es válida.</span><span class="sxs-lookup"><span data-stu-id="0b66f-154">You specified a user account that was not valid.</span></span> <span data-ttu-id="0b66f-155">Puede comprobar que una cuenta de usuario existe ejecutando un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="0b66f-155">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="0b66f-156">La cuenta de usuario es válida, pero la cuenta no está habilitada actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0b66f-156">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="0b66f-157">Para comprobar que una cuenta de usuario está habilitada para Lync Server, ejecute un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="0b66f-157">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="0b66f-158">Si la propiedad Enabled se establece en false, significa que el usuario no está habilitado actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0b66f-158">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="0b66f-159">Es posible que el usuario de prueba no tenga un certificado de cliente válido.</span><span class="sxs-lookup"><span data-stu-id="0b66f-159">The test user might not have a valid client certificate.</span></span> <span data-ttu-id="0b66f-160">Puede devolver información acerca de los certificados de cliente asignados a un usuario mediante un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="0b66f-160">You can return information about the client certificates assigned to a user by using a command similar to this:</span></span>
    
        Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="0b66f-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b66f-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

