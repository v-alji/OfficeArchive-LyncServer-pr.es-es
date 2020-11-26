---
title: 'Lync Server 2013: pruebas de uso compartido en conferencias'
description: 'Lync Server 2013: pruebas de uso compartido en conferencias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing sharing in conferences
ms:assetid: e6021d70-6ed9-414d-954c-06eef397dc1a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727314(v=OCS.15)
ms:contentKeyID: 63969660
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e569a97d102664b64c201af9b60061813df69ef5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439754"
---
# <a name="testing-sharing-in-conferences-in-lync-server-2013"></a><span data-ttu-id="c526a-103">Pruebas de uso compartido en conferencias en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c526a-103">Testing sharing in conferences in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c526a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c526a-104">

<span> </span></span></span>

<span data-ttu-id="c526a-105">_**Última modificación del tema:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="c526a-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c526a-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="c526a-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c526a-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="c526a-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c526a-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="c526a-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c526a-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c526a-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c526a-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="c526a-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c526a-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="c526a-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="c526a-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe asignar un rol de RBAC que tenga permiso para ejecutar el cmdlet <strong>Test-CsDataConference</strong> .</span><span class="sxs-lookup"><span data-stu-id="c526a-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsDataConference</strong> cmdlet.</span></span> <span data-ttu-id="c526a-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c526a-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDataConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c526a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c526a-114">Description</span></span>

<span data-ttu-id="c526a-115">En Lync Server 2013, una conferencia de datos es cualquier conferencia en la que se usen actividades de colaboración, como pizarras o anotaciones.</span><span class="sxs-lookup"><span data-stu-id="c526a-115">In Lync Server 2013, a data conference is any conference where collaborative activities such as whiteboarding or annotations are used.</span></span> <span data-ttu-id="c526a-116">El cmdlet **Test-CsDataConference** le permite comprobar que un par de usuarios pueden participar en una conferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="c526a-116">The **Test-CsDataConference** cmdlet enables you to verify that a pair of users are able to take part in a data conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c526a-117">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="c526a-117">Running the test</span></span>

<span data-ttu-id="c526a-118">El comando que se muestra en el ejemplo 1 comprueba que una conferencia de datos se puede llevar a cabo en el grupo atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="c526a-118">The command shown in Example 1 verifies that a data conference can be conducted on the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="c526a-119">Este comando supone que ha configurado un par de usuarios de prueba para el grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="c526a-119">This command assumes that you have configured a pair of test users for the specified pool.</span></span> <span data-ttu-id="c526a-120">Si no existen esos usuarios de prueba, el comando fallará.</span><span class="sxs-lookup"><span data-stu-id="c526a-120">If no such test users exist, the command will fail.</span></span>

    Test-CsDataConference -TargetFqdn "atl-cs-001.litwareinc.com" 

<span data-ttu-id="c526a-121">Los comandos que se muestran en el ejemplo 2 prueban la capacidad de un par de usuarios (litwareinc \\ Pilar y litwareinc \\ kenmyer) para iniciar sesión en Lync Server 2013 y, a continuación, realizar una conferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="c526a-121">The commands shown in Example 2 test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to log on to Lync Server 2013 and then conduct a data conference.</span></span> <span data-ttu-id="c526a-122">Para ello, el primer comando del ejemplo usa el cmdlet **Get-Credential** para crear un objeto de credencial de interfaz de línea de comandos de Windows PowerShell que contiene el nombre y la contraseña del usuario Pilar Ackerman.</span><span class="sxs-lookup"><span data-stu-id="c526a-122">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object containing the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="c526a-123">(Como el nombre de inicio de sesión, litwareinc \\ pilar, se ha incluido como parámetro, el cuadro de diálogo solicitud de credenciales de Windows PowerShell solo requiere que el administrador escriba la contraseña de la cuenta de Pilar Ackerman). El objeto de credencial resultante se almacena en una variable llamada $cred 1.</span><span class="sxs-lookup"><span data-stu-id="c526a-123">(Because the logon name, litwareinc\\pilar, has been included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credential object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="c526a-124">El segundo comando hace lo mismo, pero esta vez devuelve un objeto de credenciales para la cuenta Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="c526a-124">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="c526a-125">Con los objetos de credenciales a mano, el tercer comando determina si estos dos usuarios pueden iniciar sesión en Lync Server 2013 y realizar una conferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="c526a-125">With the credential objects in hand, the third command determines whether or not these two users can log on to Lync Server 2013 and conduct a data conference.</span></span> <span data-ttu-id="c526a-126">Para llevar a cabo esta tarea, se llama al cmdlet **Test-CsDataConference** , junto con los siguientes parámetros: TargetFqdn (el FQDN del grupo de servidores de registrar); SenderSipAddress (dirección SIP del primer usuario de prueba); SenderCredential (el objeto de Windows PowerShell que contiene las credenciales para este mismo usuario); ReceiverSipAddress (la dirección SIP del otro usuario de prueba); y ReceiverCredential (el objeto de Windows PowerShell que contiene las credenciales del otro usuario de prueba).</span><span class="sxs-lookup"><span data-stu-id="c526a-126">To carry out this task, the **Test-CsDataConference** cmdlet is called, along with the following parameters: TargetFqdn (the FQDN of the Registrar pool); SenderSipAddress (the SIP address for the first test user); SenderCredential (the Windows PowerShell object containing the credentials for this same user); ReceiverSipAddress (the SIP address for the other test user); and ReceiverCredential (the Windows PowerShell object containing the credentials for the other test user).</span></span>

    $credential1 = Get-Credential "litwareinc\pilar" 
    $credential2 = Get-Credential "litwareinc\kenmyer" 
    Test-CsDataConference -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -ReceiverCredential $credential2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c526a-127">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="c526a-127">Determining success or failure</span></span>

<span data-ttu-id="c526a-128">Si la Conferencia de datos se ha configurado correctamente, recibirá un resultado similar a este, con la propiedad result marcada como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="c526a-128">If data conferencing is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="c526a-129">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c526a-129">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c526a-130">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="c526a-130">Result : Success</span></span>

<span data-ttu-id="c526a-131">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c526a-131">Latency : 00:00:00</span></span>

<span data-ttu-id="c526a-132">Mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="c526a-132">Error Message :</span></span>

<span data-ttu-id="c526a-133">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c526a-133">Diagnosis :</span></span>

<span data-ttu-id="c526a-134">Si los usuarios especificados no pueden usar el uso compartido de datos, el resultado se mostrará como **error** y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="c526a-134">If the specified users can't use data sharing, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="c526a-135">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c526a-135">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c526a-136">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="c526a-136">Result : Failure</span></span>

<span data-ttu-id="c526a-137">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c526a-137">Latency : 00:00:00</span></span>

<span data-ttu-id="c526a-138">Mensaje de error: 10060, error al intentar la conexión porque la persona conectada</span><span class="sxs-lookup"><span data-stu-id="c526a-138">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="c526a-139">no respondió correctamente después de un período de tiempo, o</span><span class="sxs-lookup"><span data-stu-id="c526a-139">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="c526a-140">error en la conexión establecida porque el host conectado tiene</span><span class="sxs-lookup"><span data-stu-id="c526a-140">established connection failed because connected host has</span></span>

<span data-ttu-id="c526a-141">Error al responder \[ 2001:4898: E8: f39e: 5c9a: ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="c526a-141">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="c526a-142">Excepción interna: error en el intento de conexión porque el</span><span class="sxs-lookup"><span data-stu-id="c526a-142">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="c526a-143">la parte conectada no respondió correctamente después de un período de</span><span class="sxs-lookup"><span data-stu-id="c526a-143">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="c526a-144">hora o error de conexión establecida porque el host conectado</span><span class="sxs-lookup"><span data-stu-id="c526a-144">time, or established connection failed because connected host</span></span>

<span data-ttu-id="c526a-145">Error al responder</span><span class="sxs-lookup"><span data-stu-id="c526a-145">has failed to respond</span></span>

<span data-ttu-id="c526a-146">\[2001:4898: E8: f39e: 5c9a: ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="c526a-146">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="c526a-147">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c526a-147">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c526a-148">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="c526a-148">Reasons why the test might have failed</span></span>

<span data-ttu-id="c526a-149">Estas son algunas de las razones comunes por las que **Test-CsDataConference** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="c526a-149">Here are some common reasons why **Test-CsDataConference** might fail:</span></span>

  - <span data-ttu-id="c526a-150">Se proporcionó un valor de parámetro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="c526a-150">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="c526a-151">Si se usa, los parámetros opcionales deben estar configurados correctamente o se producirá un error en la prueba.</span><span class="sxs-lookup"><span data-stu-id="c526a-151">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="c526a-152">Vuelva a ejecutar el comando sin los parámetros opcionales y vea si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c526a-152">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="c526a-153">La posibilidad de llevar a cabo una conferencia de datos depende de la Directiva de conferencia que se haya asignado al usuario que organizó la Conferencia (en el caso del cmdlet **Test-CsDataConference** , que es el "remitente").</span><span class="sxs-lookup"><span data-stu-id="c526a-153">The ability to conduct a data conference depends on the conferencing policy that has been assigned to the user who organized the conference (in the case of the **Test-CsDataConference** cmdlet, that is the "sender").</span></span> <span data-ttu-id="c526a-154">Si el organizador no puede incluir actividades de colaboración en su reunión (por ejemplo, si su Directiva de conferencia tiene la propiedad EnableDataCollaboration establecida en falso), el cmdlet **Test-CsDataConference** se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="c526a-154">If the organizer is not allowed to include collaborative activities in his or her meeting (for example, if his or her conferencing policy has the EnableDataCollaboration property set to False) then the **Test-CsDataConference** cmdlet will fail.</span></span>

  - <span data-ttu-id="c526a-155">Este comando fallará si el servidor perimetral está mal configurado o aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="c526a-155">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

<span data-ttu-id="c526a-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c526a-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

