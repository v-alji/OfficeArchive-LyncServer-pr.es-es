---
title: 'Lync Server 2013: probar el acceso a la aplicación Web'
description: 'Lync Server 2013: Pruebe el acceso a la aplicación Web.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test Web App access
ms:assetid: 17d67ea3-f74d-4952-ac2b-92c0dacc8014
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767944(v=OCS.15)
ms:contentKeyID: 63969584
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc3bbc8008df4fe47fc5a39571356383fe5a6035
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441133"
---
# <a name="test-web-app-access-in-lync-server-2013"></a><span data-ttu-id="07143-103">Probar el acceso a aplicaciones web en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07143-103">Test Web App access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07143-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07143-104">

<span> </span></span></span>

<span data-ttu-id="07143-105">_**Última modificación del tema:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="07143-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07143-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="07143-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="07143-107">Cada mes</span><span class="sxs-lookup"><span data-stu-id="07143-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07143-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="07143-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="07143-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="07143-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07143-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="07143-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="07143-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="07143-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="07143-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsWebApp.</span><span class="sxs-lookup"><span data-stu-id="07143-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsWebApp cmdlet.</span></span> <span data-ttu-id="07143-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07143-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebApp&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="07143-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="07143-114">Description</span></span>

<span data-ttu-id="07143-115">El cmdlet Test-CsWebApp comprueba que los usuarios autenticados pueden unirse a conferencias de Lync Server mediante Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="07143-115">The Test-CsWebApp cmdlet verifies that authenticated users can join Lync Server conferences by using the Lync Web App.</span></span> <span data-ttu-id="07143-116">Al ejecutar el cmdlet, Test-CsWebApp se pone en contacto con el servicio de vales web para obtener vales web para los usuarios especificados.</span><span class="sxs-lookup"><span data-stu-id="07143-116">When you run the cmdlet, Test-CsWebApp contacts the Web Ticket service to obtain web tickets for the specified users.</span></span> <span data-ttu-id="07143-117">Estos vales actúan de manera eficaz como "vales de admisión" en la Conferencia de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="07143-117">These tickets effectively act as ‘admission tickets” to the Lync Server conference.</span></span> <span data-ttu-id="07143-118">Si se pueden recuperar los vales y si los usuarios pueden ser autenticados, Test-CsWebApp se pondrá en contacto con Lync Server e intentará establecer conferencias distintas para la mensajería instantánea, el uso compartido de aplicaciones y la colaboración de datos.</span><span class="sxs-lookup"><span data-stu-id="07143-118">If the tickets can be retrieved, and if the users can be authenticated, Test-CsWebApp will then contact Lync Server and attempt to establish separate conferences for instant messaging, application sharing, and data collaboration.</span></span>

<span data-ttu-id="07143-119">Tenga en cuenta que Test-CsWebApp solo comprueba las API y las conexiones usadas para crear estas conferencias.</span><span class="sxs-lookup"><span data-stu-id="07143-119">Note that Test-CsWebApp just verifies the APIs and connections used to create these conferences.</span></span> <span data-ttu-id="07143-120">El cmdlet está diseñado para comprobar que Lync Web App podría usarse para crear conferencias y unirse a ellas.</span><span class="sxs-lookup"><span data-stu-id="07143-120">The cmdlet is designed to verify that Lync Web App could be used to create and join conferences.</span></span> <span data-ttu-id="07143-121">Sin embargo, en realidad no crea y realiza una conferencia.</span><span class="sxs-lookup"><span data-stu-id="07143-121">However,, it does not actually create and conduct a conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="07143-122">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="07143-122">Running the test</span></span>

<span data-ttu-id="07143-123">El cmdlet Test-CsWebApp se puede ejecutar con un par de cuentas de prueba preconfiguradas o con las cuentas de dos usuarios que están habilitados para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="07143-123">The Test-CsWebApp cmdlet can be run using either a pair of preconfigured test accounts or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="07143-124">Para ejecutar esta comprobación mediante cuentas de prueba, solo tiene que especificar el nombre de dominio completo del grupo de servidores de Lync que se está probando.</span><span class="sxs-lookup"><span data-stu-id="07143-124">To run this check using test accounts, you just have to specify the fully qualified domain name of the Lync Server pool being tested.</span></span> <span data-ttu-id="07143-125">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="07143-125">For example:</span></span>

    Test-CsWebApp -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="07143-126">Para ejecutar esta comprobación con las cuentas de usuario reales, debe crear dos objetos de credenciales de Windows PowerShell (objetos que contengan el nombre y la contraseña de la cuenta) de cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="07143-126">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="07143-127">Después, debe incluir esos objetos de credenciales y las direcciones SIP de las dos cuentas cuando llame a test-CsWebApp:</span><span class="sxs-lookup"><span data-stu-id="07143-127">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsWebApp:</span></span>

    $cred1 = Get-Credential "litwareinc\kenmyer"
    $cred2 = Get-Credential "litwareinc\pilar"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1 -User2SipAddress "sip:pilar@litwareinc.com" -User2Credential $cred2

<span data-ttu-id="07143-128">Para obtener más información, vea el tema de ayuda para el cmdlet [Test-CsWebApp](https://docs.microsoft.com/powershell/module/skype/Test-CsWebApp) .</span><span class="sxs-lookup"><span data-stu-id="07143-128">For more information, see the help topic for the [Test-CsWebApp](https://docs.microsoft.com/powershell/module/skype/Test-CsWebApp) cmdlet.</span></span> <span data-ttu-id="07143-129">Tenga en cuenta que Test-CsWebApp quedó obsoleto para usarse en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="07143-129">Note that Test-CsWebApp was deprecated for use on Lync Server 2013.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="07143-130">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="07143-130">Determining success or failure</span></span>

<span data-ttu-id="07143-131">Si Test-CsWebApp puede unir a los usuarios a sus conferencias, el cmdlet devolverá el resultado de la prueba correcta:</span><span class="sxs-lookup"><span data-stu-id="07143-131">If Test-CsWebApp can join the users to their conferences, the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="07143-132">FQDN de destino:</span><span class="sxs-lookup"><span data-stu-id="07143-132">Target Fqdn :</span></span>

<span data-ttu-id="07143-133">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="07143-133">Result : Success</span></span>

<span data-ttu-id="07143-134">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="07143-134">Latency : 00:00:00</span></span>

<span data-ttu-id="07143-135">Mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="07143-135">Error Message :</span></span>

<span data-ttu-id="07143-136">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="07143-136">Diagnosis :</span></span>

<span data-ttu-id="07143-137">Si los usuarios no pueden unirse a las conferencias necesarias, el resultado de la prueba se marcará como erróneo.</span><span class="sxs-lookup"><span data-stu-id="07143-137">If the users cannot join the necessary conferences then the test result will be marked as Failure.</span></span> <span data-ttu-id="07143-138">Por lo general, Test-CsWebApp también devolverá un mensaje de error y un diagnóstico detallados:</span><span class="sxs-lookup"><span data-stu-id="07143-138">Typically Test-CsWebApp will also report back a detailed error message and diagnosis:</span></span>

<span data-ttu-id="07143-139">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="07143-139">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="07143-140">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="07143-140">Result : Failure</span></span>

<span data-ttu-id="07143-141">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="07143-141">Latency : 00:00:00</span></span>

<span data-ttu-id="07143-142">Mensaje de error: no se recibió respuesta para el servicio Web-Ticket</span><span class="sxs-lookup"><span data-stu-id="07143-142">Error Message : No response received for Web-Ticket service</span></span>

<span data-ttu-id="07143-143">Diagnóstico: la solicitud HTTP no está autorizada con el cliente</span><span class="sxs-lookup"><span data-stu-id="07143-143">Diagnosis : The HTTP request is unauthorized with client</span></span>

<span data-ttu-id="07143-144">esquema de autenticación ' NTLM '.</span><span class="sxs-lookup"><span data-stu-id="07143-144">authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="07143-145">La autenticación</span><span class="sxs-lookup"><span data-stu-id="07143-145">The authentication</span></span>

<span data-ttu-id="07143-146">el encabezado recibido del servidor era ' Negotiate, NTLM '.</span><span class="sxs-lookup"><span data-stu-id="07143-146">header received from the server was 'Negotiate,NTLM'.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="07143-147">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="07143-147">Reasons why the test might have failed</span></span>

<span data-ttu-id="07143-148">Los errores de Test-CsWebApp suelen incluir errores de autenticación de usuario.</span><span class="sxs-lookup"><span data-stu-id="07143-148">Test-CsWebApp failures typically involve user authentication errors.</span></span> <span data-ttu-id="07143-149">Si Test-CsWebApp falla, primero debe comprobar que los usuarios especificados tienen cuentas de usuario válidas y que están habilitados para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="07143-149">If Test-CsWebApp fails, you should first verify that the specified users have valid user accounts and are enabled for Lync Server.</span></span> <span data-ttu-id="07143-150">Puede recuperar información de la cuenta mediante un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="07143-150">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="07143-151">Si la propiedad Enabled no es igual a true o si se produce un error en el comando, significa que el usuario no tiene una cuenta válida de Lync Server. También debe comprobar que las contraseñas proporcionadas al cmdlet son válidas.</span><span class="sxs-lookup"><span data-stu-id="07143-151">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.You should also verify that the passwords that you supplied to the cmdlet are valid.</span></span>

<span data-ttu-id="07143-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07143-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

