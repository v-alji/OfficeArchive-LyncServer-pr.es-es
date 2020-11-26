---
title: 'Lync Server 2013: capacidad de pruebas para usar la expansión de grupos'
description: 'Lync Server 2013: prueba de la capacidad de usar la expansión de grupos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to employ group expansion
ms:assetid: 9b0fc954-6f9c-411a-ab32-94ebabc42de2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743836(v=OCS.15)
ms:contentKeyID: 63969634
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6267bc2099fc420c5c57e1ef80f4bf4491334938
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441112"
---
# <a name="testing-ability-to-employ-group-expansion-in-lync-server-2013"></a><span data-ttu-id="ab4d0-103">Capacidad de pruebas para emplear la expansión de grupos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab4d0-103">Testing ability to employ group expansion in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab4d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab4d0-104">

<span> </span></span></span>

<span data-ttu-id="ab4d0-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="ab4d0-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab4d0-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="ab4d0-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="ab4d0-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="ab4d0-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab4d0-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="ab4d0-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="ab4d0-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab4d0-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab4d0-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="ab4d0-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="ab4d0-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="ab4d0-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsGroupExpansion.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupExpansion cmdlet.</span></span> <span data-ttu-id="ab4d0-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupExpansion&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="ab4d0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab4d0-114">Description</span></span>

<span data-ttu-id="ab4d0-115">El cmdlet Test-CsGroupExpansion le permite determinar si la expansión de grupo funciona en su organización.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-115">The Test-CsGroupExpansion cmdlet lets you determine whether group expansion is working within your organization.</span></span> <span data-ttu-id="ab4d0-116">Cuando la expansión de grupo está habilitada, los usuarios configuran grupos de distribución como un contacto.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-116">When group expansion is enabled, users configure distribution groups as a contact.</span></span> <span data-ttu-id="ab4d0-117">Eso significa que los usuarios pueden enviar el mismo mensaje instantáneo a todos los miembros del grupo si dirigen el mensaje al grupo en lugar de a los miembros individuales de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-117">That means that those users can then send the same instant message to all the group members by addressing the message to the group instead of to individual members of that group.</span></span> <span data-ttu-id="ab4d0-118">La expansión grupal te permite ver de forma rápida y sencilla a todos los miembros del grupo y su estado actual.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-118">Group expansion enables you to quickly and easily view all the group members and their current status.</span></span>

<span data-ttu-id="ab4d0-119">Con el cmdlet Test-CsGroupExpansion, puede especificar un grupo de distribución de Active Directory mediante la dirección de correo electrónico del grupo.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-119">With the Test-CsGroupExpansion cmdlet, you specify an Active Directory distribution group by using the group’s email address.</span></span> <span data-ttu-id="ab4d0-120">Test-CsGroupExpansion usa la expansión de grupo para recuperar la pertenencia a grupos y comparar la lista recuperada con la pertenencia de la dirección de correo electrónico del grupo que proporcionó.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-120">Test-CsGroupExpansion then uses group expansion to retrieve the group membership and compare the retrieved list to the membership of the group email address that you supplied.</span></span> <span data-ttu-id="ab4d0-121">Si las dos listas coinciden, la expansión del grupo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-121">If the two lists match, then group expansion is working correctly.</span></span> <span data-ttu-id="ab4d0-122">Tenga en cuenta que puede probar la expansión de grupos de dos maneras: probando el servicio o probando el servicio web asociado.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-122">Note that you can test group expansion in two ways: by testing the service itself or by testing the associated web service.</span></span>

<span data-ttu-id="ab4d0-123">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="ab4d0-123">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="ab4d0-124">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="ab4d0-124">Running the test</span></span>

<span data-ttu-id="ab4d0-125">El cmdlet Test-CsGroupExpansion se puede ejecutar mediante una cuenta de prueba preconfigurada (consulte Configurar cuentas de prueba para ejecutar pruebas de Lync Server) o la cuenta de cualquier usuario que se haya habilitado para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-125">The Test-CsGroupExpansion cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who was enabled for Lync Server.</span></span> <span data-ttu-id="ab4d0-126">Para ejecutar esta comprobación mediante una cuenta de prueba, solo tiene que especificar el FQDN del grupo de servidores de Lync que se está probando y la dirección de correo electrónico de un grupo de distribución válido.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-126">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the email address for a valid distribution group.</span></span> <span data-ttu-id="ab4d0-127">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-127">For example:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com"

<span data-ttu-id="ab4d0-128">Para ejecutar esta comprobación mediante una cuenta de usuario real, primero debe crear un objeto de credenciales de Lync Server que contenga el nombre y la contraseña de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-128">To run this check using an actual user account, you must first create a Lync Server credentials object that contains the account name and password.</span></span> <span data-ttu-id="ab4d0-129">Después, debes incluir ese objeto de credenciales y la dirección SIP asignada a la cuenta cuando el sistema llame test-CsGroupExpansion:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-129">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsGroupExpansion:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="ab4d0-130">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="ab4d0-130">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="ab4d0-131">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="ab4d0-131">Determining success or failure</span></span>

<span data-ttu-id="ab4d0-132">Si el usuario especificado puede usar la expansión de grupo, recibirá una salida similar a la siguiente, con la propiedad result marcada como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="ab4d0-132">If the specified user can use group expansion, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="ab4d0-133">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="ab4d0-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="ab4d0-134">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ab4d0-134">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ab4d0-135">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="ab4d0-135">Result : Success</span></span>

<span data-ttu-id="ab4d0-136">Latencia: 00:00:01.1234976</span><span class="sxs-lookup"><span data-stu-id="ab4d0-136">Latency : 00:00:01.1234976</span></span>

<span data-ttu-id="ab4d0-137">:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-137">Error :</span></span>

<span data-ttu-id="ab4d0-138">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ab4d0-138">Diagnosis :</span></span>

<span data-ttu-id="ab4d0-139">Si el usuario especificado no puede usar la expansión de grupo, el resultado se mostrará como error y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-139">If the specified user can't use group expansion, then the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="ab4d0-140">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="ab4d0-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="ab4d0-141">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ab4d0-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ab4d0-142">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="ab4d0-142">Result : Failure</span></span>

<span data-ttu-id="ab4d0-143">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ab4d0-143">Latency : 00:00:00</span></span>

<span data-ttu-id="ab4d0-144">:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-144">Error :</span></span>

<span data-ttu-id="ab4d0-145">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ab4d0-145">Diagnosis :</span></span>

<span data-ttu-id="ab4d0-146">Test-CsGroupExpansion: el punto de conexión no se pudo registrar.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-146">Test-CsGroupExpansion : The endpoint was unable to register.</span></span> <span data-ttu-id="ab4d0-147">Consulte ErrorCode por razones específicas.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-147">See the ErrorCode for specific reason.</span></span>

<span data-ttu-id="ab4d0-148">El resultado anterior indica que no se pudo realizar la prueba porque el usuario especificado no se pudo registrar en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-148">The previous output states that the test failed because the specified user was unable to register with Lync Server.</span></span> <span data-ttu-id="ab4d0-149">Esto suele ocurrir si la cuenta de prueba no existe o no ha habilitado para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-149">This will typically occur if the test account does not exist or has not enabled for Lync Server.</span></span> <span data-ttu-id="ab4d0-150">Puede comprobar que la cuenta existe y determinar si la cuenta se ha habilitado para nm-OCS-14-3rd ejecutando un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-150">You can verify that the account exists, and determine whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to the following:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

<span data-ttu-id="ab4d0-151">Si Test-CsGroupExpansion da error, es posible que desee volver a ejecutar la prueba, esta vez incluido el parámetro detallado:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-151">If Test-CsGroupExpansion fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -Verbose

<span data-ttu-id="ab4d0-152">Cuando se incluye el parámetro detallado Test-CsGroupExpansion se devolverá una cuenta paso a paso de cada acción que haya probado cuando haya comprobado la capacidad del usuario especificado para iniciar sesión en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-152">When the Verbose parameter is included Test-CsGroupExpansion will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="ab4d0-153">Por ejemplo, este resultado indica que no se pudo encontrar el grupo de distribución especificado:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-153">For example, this output indicates that the specified distribution group couldn't be found:</span></span>

<span data-ttu-id="ab4d0-154">Intentando obtener vale Web.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-154">Trying to get web ticket.</span></span>

<span data-ttu-id="ab4d0-155">Dirección URL del servicio Web: https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="ab4d0-155">Web Service url : https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="ab4d0-156">Uso de NTLM/Kerb auth.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-156">Using NTLM/Kerb auth.</span></span>

<span data-ttu-id="ab4d0-157">GetWebTicketActivity completado.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-157">GetWebTicketActivity completed.</span></span>

<span data-ttu-id="ab4d0-158">Actividad ' VerifyDistributionList ' iniciada.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-158">'VerifyDistributionList' activity started.</span></span>

<span data-ttu-id="ab4d0-159">El estado de respuesta del servicio Web de DLX es: NotFound.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-159">DLX Web Service Response Status is: NotFound.</span></span>

<span data-ttu-id="ab4d0-160">Actividad ' VerifyDistributionList ' completada en ' 0,2597923 ' s.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-160">'VerifyDistributionList' activity completed in '0.2597923' secs.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="ab4d0-161">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="ab4d0-161">Reasons why the test might have failed</span></span>

<span data-ttu-id="ab4d0-162">Estas son algunas de las razones comunes por las que Test-CsGroupExpansion puede dar error:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-162">Here are some common reasons why Test-CsGroupExpansion might fail:</span></span>

  - <span data-ttu-id="ab4d0-163">Ha especificado una cuenta de usuario no válida.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-163">You specified an invalid user account.</span></span> <span data-ttu-id="ab4d0-164">Puede comprobar que una cuenta de usuario existe ejecutando un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-164">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="ab4d0-165">La cuenta de usuario es válida, pero la cuenta no está habilitada actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-165">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="ab4d0-166">Para comprobar que una cuenta de usuario se ha habilitado para Lync Server, ejecute un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-166">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="ab4d0-167">Si la propiedad Enabled se establece en false, significa que el usuario no está habilitado actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-167">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="ab4d0-168">Es posible que la expansión del grupo esté deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-168">Group expansion might be disabled.</span></span> <span data-ttu-id="ab4d0-169">Es posible desactivar la expansión de grupos.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-169">It is possible to turn off group expansion.</span></span> <span data-ttu-id="ab4d0-170">Si se ha deshabilitado la expansión de grupos, el cmdlet Test-CsGroupExpansion producirá un error.</span><span class="sxs-lookup"><span data-stu-id="ab4d0-170">If group expansion was disabled then the Test-CsGroupExpansion cmdlet will fail.</span></span> <span data-ttu-id="ab4d0-171">Para determinar si la expansión de grupo está habilitada, use un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="ab4d0-171">To determine whether group expansion is enabled, use a command similar to this:</span></span>
    
        Get-CsWebServiceConfiguration | Select-Object Identity, EnableGroupExpansion

<span data-ttu-id="ab4d0-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab4d0-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

