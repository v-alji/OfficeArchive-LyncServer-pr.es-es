---
title: 'Lync Server 2013: capacidad de probar la conexión a un dominio federado'
description: 'Lync Server 2013: capacidad de prueba para conectarse a un dominio federado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to connect to a federated domain
ms:assetid: d8ccfade-ef54-47a4-9f87-36213a635ce5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743840(v=OCS.15)
ms:contentKeyID: 63969653
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf1f5bdef66d34b9ca2e39797df0b4ad32d9afde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441140"
---
# <a name="testing-ability-to-connect-to-a-federated-domain-from-lync-server-2013"></a><span data-ttu-id="19018-103">Capacidad de prueba para conectarse a un dominio federado desde Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19018-103">Testing ability to connect to a federated domain from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19018-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19018-104">

<span> </span></span></span>

<span data-ttu-id="19018-105">_**Última modificación del tema:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="19018-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19018-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="19018-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="19018-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="19018-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19018-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="19018-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="19018-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="19018-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19018-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="19018-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="19018-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="19018-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="19018-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsFederatedPartner.</span><span class="sxs-lookup"><span data-stu-id="19018-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsFederatedPartner cmdlet.</span></span> <span data-ttu-id="19018-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="19018-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsFederatedPartner&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="19018-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="19018-114">Description</span></span>

<span data-ttu-id="19018-115">Test-CsFederatedPartner verifica su capacidad para conectarse al dominio de un socio federado.</span><span class="sxs-lookup"><span data-stu-id="19018-115">Test-CsFederatedPartner verifies your ability to connect to the domain of a federated partner.</span></span> <span data-ttu-id="19018-116">Para comprobar la conectividad a un dominio, ese dominio debe aparecer en la colección de dominios permitidos (federados).</span><span class="sxs-lookup"><span data-stu-id="19018-116">To verify the connectivity to a domain, that domain must be listed in the collection of allowed (federated) domains.</span></span> <span data-ttu-id="19018-117">Puede recuperar una lista de los dominios en la lista de dominios permitidos con este comando:</span><span class="sxs-lookup"><span data-stu-id="19018-117">You can retrieve a list of the domains on your allowed domains list by using this command:</span></span>

    Get-CsAllowedDomain

<span data-ttu-id="19018-118">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) .</span><span class="sxs-lookup"><span data-stu-id="19018-118">For more information, see the Help documentation for the [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="19018-119">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="19018-119">Running the test</span></span>

<span data-ttu-id="19018-120">El cmdlet Test-FederatedPartner requiere dos datos: el FQDN de su servidor perimetral y el FQDN del socio federado.</span><span class="sxs-lookup"><span data-stu-id="19018-120">The Test-FederatedPartner cmdlet requires two pieces of information: the FQDN of your Edge Server and the FQDN of the federated partner.</span></span> <span data-ttu-id="19018-121">Por ejemplo, este comando prueba la capacidad de conectar con el dominio contoso.com:</span><span class="sxs-lookup"><span data-stu-id="19018-121">For example, this command tests the ability to connect to the domain contoso.com:</span></span>

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"

<span data-ttu-id="19018-122">Este comando le permite probar las conexiones a todos los dominios que se encuentran en la lista de dominios permitidos:</span><span class="sxs-lookup"><span data-stu-id="19018-122">This command enables you to test the connections to all the domains currently on your allowed domains list:</span></span>

    Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Identity}

<span data-ttu-id="19018-123">Para obtener más información, consulte la documentación de ayuda del cmdlet [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) .</span><span class="sxs-lookup"><span data-stu-id="19018-123">For more information, see the Help documentation for the [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="19018-124">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="19018-124">Determining success or failure</span></span>

<span data-ttu-id="19018-125">Si se puede contactar con el dominio especificado, recibirá una salida similar a la siguiente, con la propiedad result marcada como **correcta:**</span><span class="sxs-lookup"><span data-stu-id="19018-125">If the specified domain can be contacted, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="19018-126">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="19018-126">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="19018-127">Resultado: éxito</span><span class="sxs-lookup"><span data-stu-id="19018-127">Result : Success</span></span>

<span data-ttu-id="19018-128">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="19018-128">Latency : 00:00:00</span></span>

<span data-ttu-id="19018-129">:</span><span class="sxs-lookup"><span data-stu-id="19018-129">Error :</span></span>

<span data-ttu-id="19018-130">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="19018-130">Diagnosis :</span></span>

<span data-ttu-id="19018-131">Si no se puede contactar con el dominio especificado, el resultado se mostrará como erróneo y la información adicional se registrará en las propiedades de diagnóstico y errores:</span><span class="sxs-lookup"><span data-stu-id="19018-131">If the specified domain cannot be contacted, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="19018-132">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="19018-132">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="19018-133">Resultado: error</span><span class="sxs-lookup"><span data-stu-id="19018-133">Result : Failure</span></span>

<span data-ttu-id="19018-134">Latencia: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="19018-134">Latency : 00:00:00</span></span>

<span data-ttu-id="19018-135">Error: 504, tiempo de espera del servidor</span><span class="sxs-lookup"><span data-stu-id="19018-135">Error : 504, Server time-out</span></span>

<span data-ttu-id="19018-136">Diagnosis: ErrorCode = 2, Source = ATL-CS-001. litwareinc. com, razón = ver</span><span class="sxs-lookup"><span data-stu-id="19018-136">Diagnosis : ErrorCode=2, Source=atl-cs-001.litwareinc.com,Reason=See</span></span>

<span data-ttu-id="19018-137">código de respuesta y frase de motivo.</span><span class="sxs-lookup"><span data-stu-id="19018-137">response code and reason phrase.</span></span>

<span data-ttu-id="19018-138">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="19018-138">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="19018-139">Por ejemplo, la salida anterior indica que no se pudo realizar la prueba debido a un error de tiempo de espera del servidor.</span><span class="sxs-lookup"><span data-stu-id="19018-139">For example, the previous output states that the test failed because of a server time-out error.</span></span> <span data-ttu-id="19018-140">Normalmente, esto indica problemas de conectividad de red o problemas para ponerse en contacto con el servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="19018-140">This typically indicates either network connectivity problems or problems contacting the Edge Server.</span></span>

<span data-ttu-id="19018-141">Si Test-CsFederatedPartner da error, es posible que desee volver a ejecutar la prueba, esta vez incluido el parámetro detallado:</span><span class="sxs-lookup"><span data-stu-id="19018-141">If Test-CsFederatedPartner fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com" -Verbose

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="19018-142">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="19018-142">Reasons why the test might have failed</span></span>

<span data-ttu-id="19018-143">Estas son algunas de las razones comunes por las que Test-CsFederatedPartner puede dar error:</span><span class="sxs-lookup"><span data-stu-id="19018-143">Here are some common reasons why Test-CsFederatedPartner might fail:</span></span>

  - <span data-ttu-id="19018-144">Es posible que el servidor perimetral no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="19018-144">The Edge Server might not be available.</span></span> <span data-ttu-id="19018-145">Puede usar los FQDN de los servidores perimetrales con este comando:</span><span class="sxs-lookup"><span data-stu-id="19018-145">You can the FQDNs of your Edge Servers by using this command:</span></span>
    
        Get-CsService -EdgeServer | Select-Object PoolFqdn
    
    <span data-ttu-id="19018-146">Después, puede hacer ping a cada servidor perimetral para comprobar que se puede tener acceso a él a través de la red.</span><span class="sxs-lookup"><span data-stu-id="19018-146">You can then ping each Edge Server to verify that it can be accessed over the network.</span></span> <span data-ttu-id="19018-147">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="19018-147">For example:</span></span>
    
        ping atl-edge-001.litwareinc.com

  - <span data-ttu-id="19018-148">Es posible que el dominio especificado no aparezca en la lista de dominios permitidos.</span><span class="sxs-lookup"><span data-stu-id="19018-148">The specified domain might not be listed on the allowed domains list.</span></span> <span data-ttu-id="19018-149">Para comprobar los dominios que se han agregado a la lista de dominios permitidos, use este comando:</span><span class="sxs-lookup"><span data-stu-id="19018-149">To verify the domains that were added to the allowed domains list, use this command:</span></span>
    
        Get-CsAllowedDomain
    
    <span data-ttu-id="19018-150">Si desea ver una lista de los dominios con los que los usuarios no pueden comunicarse, use este comando:</span><span class="sxs-lookup"><span data-stu-id="19018-150">If you’d like to see a list of domains that users were blocked from communicating with, then use this command:</span></span>
    
        Get-CsBlockedDomain

<span data-ttu-id="19018-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19018-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

