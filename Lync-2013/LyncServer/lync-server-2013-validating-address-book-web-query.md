---
title: 'Lync Server 2013: validación de la consulta Web de la libreta de direcciones'
description: 'Lync Server 2013: validación de la consulta Web de la libreta de direcciones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating address book web query
ms:assetid: e6ae0a5a-e131-4cfe-9a33-6e611831072d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720925(v=OCS.15)
ms:contentKeyID: 63969662
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e73c39fc33f8d1851fc89d277333a94aaa137790
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438907"
---
# <a name="validating-address-book-web-query-in-lync-server-2013"></a><span data-ttu-id="f3654-103">Validación de la consulta Web de la libreta de direcciones en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3654-103">Validating address book web query in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3654-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3654-104">

<span> </span></span></span>

<span data-ttu-id="f3654-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="f3654-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3654-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="f3654-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="f3654-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="f3654-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3654-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="f3654-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="f3654-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3654-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3654-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="f3654-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="f3654-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f3654-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="f3654-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsAddressBookWebQuery.</span><span class="sxs-lookup"><span data-stu-id="f3654-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAddressBookWebQuery cmdlet.</span></span> <span data-ttu-id="f3654-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f3654-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAddressBookWebQuery&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="f3654-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3654-114">Description</span></span>

<span data-ttu-id="f3654-115">El cmdlet Test-CsAddressBookWebQuery permite a los administradores comprobar que los usuarios pueden usar el servicio de consultas Web de la libreta de direcciones para buscar un contacto específico.</span><span class="sxs-lookup"><span data-stu-id="f3654-115">The Test-CsAddressBookWebQuery cmdlet enables administrators to verify that users can use the Address Book Web Query service to search for a specific contact.</span></span> <span data-ttu-id="f3654-116">Al ejecutar el cmdlet, Test-CsAddressBookWebQuery se conectará primero con el servicio de vales web para que se autentique.</span><span class="sxs-lookup"><span data-stu-id="f3654-116">When you run the cmdlet, Test-CsAddressBookWebQuery will first connect to the Web Ticket service to be authenticated.</span></span> <span data-ttu-id="f3654-117">Si la autenticación se realiza correctamente, el cmdlet se conectará al servicio de consulta Web de la libreta de direcciones y buscará el contacto especificado.</span><span class="sxs-lookup"><span data-stu-id="f3654-117">If authentication is successful, the cmdlet will then connect to the Address Book Web Query service and search for the specified contact.</span></span> <span data-ttu-id="f3654-118">Si se encuentra ese contacto, el cmdlet intentará devolver esa información al equipo local.</span><span class="sxs-lookup"><span data-stu-id="f3654-118">If that contact is found, the cmdlet will attempt to return that information to the local computer.</span></span> <span data-ttu-id="f3654-119">La prueba se marcará como correcta solo si se pueden completar todos los pasos.</span><span class="sxs-lookup"><span data-stu-id="f3654-119">The test will be marked a success only if all those steps can be completed.</span></span>

<span data-ttu-id="f3654-120">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) .</span><span class="sxs-lookup"><span data-stu-id="f3654-120">For more information, see the Help documentation for the [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="f3654-121">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="f3654-121">Running the test</span></span>

<span data-ttu-id="f3654-122">El cmdlet Test-CsAddressBookWebQuery se puede ejecutar mediante una cuenta de prueba preconfigurada (consulte Configurar cuentas de prueba para ejecutar pruebas de Lync Server) o la cuenta de cualquier usuario que esté habilitado para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3654-122">The Test-CsAddressBookWebQuery cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="f3654-123">Para ejecutar esta comprobación mediante una cuenta de prueba, solo tiene que especificar el FQDN del grupo de servidores de Lync y la dirección SIP del usuario que actúa como destino de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f3654-123">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool and the SIP address of the user acting as the target of the search.</span></span> <span data-ttu-id="f3654-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f3654-124">For example:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com"

<span data-ttu-id="f3654-125">Para ejecutar esta comprobación mediante una cuenta de usuario real, debe crear un objeto de credenciales de Windows PowerShell que contenga un nombre de usuario y una contraseña válidos.</span><span class="sxs-lookup"><span data-stu-id="f3654-125">To run this check using an actual user account, you must create a Windows PowerShell credentials object that contains a valid user name and password.</span></span> <span data-ttu-id="f3654-126">Después debes incluir ese objeto de credenciales y la dirección SIP asignada a la cuenta cuando el código llama a test-CsAddressBookWebQuery:</span><span class="sxs-lookup"><span data-stu-id="f3654-126">You must then include that credentials object and the SIP address assigned to the account when the code calls Test-CsAddressBookWebQuery:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="f3654-127">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) .</span><span class="sxs-lookup"><span data-stu-id="f3654-127">For more information, see the Help documentation for the [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="f3654-128">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="f3654-128">Determining success or failure</span></span>

<span data-ttu-id="f3654-129">Si el usuario especificado puede conectarse al servicio de libreta de direcciones y recuperar la dirección de usuario de destino, devolverá un resultado similar a este, con la propiedad result marcada como correcta:</span><span class="sxs-lookup"><span data-stu-id="f3654-129">If the specified user can connect to the Address Book Service and retrieve the targeted user address, you'll return output similar to this with the Result property marked as Success:</span></span>

<span data-ttu-id="f3654-130">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="f3654-130">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="f3654-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="f3654-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="f3654-132">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="f3654-132">Result : Success</span></span>

<span data-ttu-id="f3654-133">Latencia: 00:00:06.2611356</span><span class="sxs-lookup"><span data-stu-id="f3654-133">Latency : 00:00:06.2611356</span></span>

<span data-ttu-id="f3654-134">:</span><span class="sxs-lookup"><span data-stu-id="f3654-134">Error :</span></span>

<span data-ttu-id="f3654-135">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="f3654-135">Diagnosis :</span></span>

<span data-ttu-id="f3654-136">Si el usuario especificado no se puede conectar o si la dirección de usuario de destino no se puede recuperar, el resultado se mostrará como error y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="f3654-136">If the specified user can't connect or if the target user address cannot be retrieved, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="f3654-137">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="f3654-137">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="f3654-138">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="f3654-138">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="f3654-139">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="f3654-139">Result : Failure</span></span>

<span data-ttu-id="f3654-140">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f3654-140">Latency : 00:00:00</span></span>

<span data-ttu-id="f3654-141">Error: error en la solicitud de servicio Web de libreta de direcciones con código de respuesta</span><span class="sxs-lookup"><span data-stu-id="f3654-141">Error : Address Book Web service request has failed with response code</span></span>

<span data-ttu-id="f3654-142">NoEntryFound.</span><span class="sxs-lookup"><span data-stu-id="f3654-142">NoEntryFound.</span></span>

<span data-ttu-id="f3654-143">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="f3654-143">Diagnosis :</span></span>

<span data-ttu-id="f3654-144">La salida anterior indica que no se pudo realizar la prueba porque no se pudo encontrar el usuario de destino.</span><span class="sxs-lookup"><span data-stu-id="f3654-144">The previous output states that the test failed because the target user couldn't be found.</span></span> <span data-ttu-id="f3654-145">Puede determinar si se ha pasado o no una dirección SIP válida a Test-CsAddressBookWebQuery ejecutando un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3654-145">You can determine whether or not a valid SIP address was passed to Test-CsAddressBookWebQuery by running a command similar to the following:</span></span>

    Get-CsUser | Where-Object {$_.SipAddress -eq "sip:davidlongmire@litwareinc.com"

<span data-ttu-id="f3654-146">Si Test-CsAddressBookWebQuery da error, es posible que desee volver a ejecutar la prueba, esta vez incluido el parámetro detallado:</span><span class="sxs-lookup"><span data-stu-id="f3654-146">If Test-CsAddressBookWebQuery fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -Verbose

<span data-ttu-id="f3654-147">Cuando se incluye el parámetro detallado, Test-CsAddressBookWebQuery devolverá una cuenta paso a paso de cada acción que intentó realizar al comprobar la capacidad del usuario especificado para iniciar sesión en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3654-147">When the Verbose parameter is included, Test-CsAddressBookWebQuery will return a step-by-step account of each action it tried while checking the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="f3654-148">Por ejemplo, esta salida indica que Test-CsAddressBookWebQuery pudo conectarse al servicio de libreta de direcciones, pero no pudo encontrar la dirección SIP de destino:</span><span class="sxs-lookup"><span data-stu-id="f3654-148">For example, this output indicates that Test-CsAddressBookWebQuery was able to connect to the Address Book Service, but was not able to locate the target SIP address:</span></span>

<span data-ttu-id="f3654-149">Actividad ' QueryAddressBookWebService ' iniciada.</span><span class="sxs-lookup"><span data-stu-id="f3654-149">'QueryAddressBookWebService' activity started.</span></span>

<span data-ttu-id="f3654-150">Llamar al servicio de consultas Web de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f3654-150">Calling Address Book Web Query Service.</span></span> <span data-ttu-id="f3654-151">DIRECCIÓN URL DE ABWS =</span><span class="sxs-lookup"><span data-stu-id="f3654-151">ABWS URL =</span></span>

https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc

<span data-ttu-id="f3654-152">Excepción de consulta de la libreta de direcciones: error en la solicitud de servicio Web de libreta de direcciones con código de respuesta NoEntryFound.</span><span class="sxs-lookup"><span data-stu-id="f3654-152">Address book query exception : Address Book Web service request has failed with response code NoEntryFound.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="f3654-153">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="f3654-153">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="f3654-154">Estas son algunas de las razones comunes por las que Test-CsAddressBookWebQuery puede dar error:</span><span class="sxs-lookup"><span data-stu-id="f3654-154">Here are some common reasons why Test-CsAddressBookWebQuery might fail:</span></span>

  - <span data-ttu-id="f3654-155">Ha especificado una cuenta de usuario no válida.</span><span class="sxs-lookup"><span data-stu-id="f3654-155">You specified an invalid user account.</span></span> <span data-ttu-id="f3654-156">Puede comprobar que una cuenta de usuario existe ejecutando un comando similar a este:</span><span class="sxs-lookup"><span data-stu-id="f3654-156">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="f3654-157">La cuenta de usuario es válida, pero la cuenta no está habilitada actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3654-157">The user account is valid, but the account is not currently enabled for Lync Server.</span></span> <span data-ttu-id="f3654-158">Para comprobar que se ha habilitado una cuenta de usuario para Lync Server, ejecute un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3654-158">To verify that a user account has been enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="f3654-159">Si la propiedad Enabled se establece en false, significa que el usuario no está habilitado actualmente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3654-159">If the Enabled property is set to False that means that the user is not currently enabled for Lync Server.</span></span>

  - <span data-ttu-id="f3654-160">Es posible que el usuario de destino no esté en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f3654-160">The target user might not be in the Address Book.</span></span>

  - <span data-ttu-id="f3654-161">Es posible que la libreta de direcciones no se haya actualizado completamente y se haya replicado.</span><span class="sxs-lookup"><span data-stu-id="f3654-161">The Address Book might not have fully updated and replicated.</span></span> <span data-ttu-id="f3654-162">Puede forzar una actualización de todos los servidores de la libreta de direcciones de su organización ejecutando el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="f3654-162">You can force an update of all the Address Book Servers in your organization by running the following command:</span></span>
    
        Update-CsAddressBook

<span data-ttu-id="f3654-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3654-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

