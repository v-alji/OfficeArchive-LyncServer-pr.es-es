---
title: 'Lync Server 2013: probar el enrutamiento de llamadas de teléfono RTC'
description: 'Lync Server 2013: probar el enrutamiento de llamadas de teléfono RTC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call routing
ms:assetid: 301dd44d-03e9-41cd-9722-54e00365aa45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727302(v=OCS.15)
ms:contentKeyID: 63969598
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da931b43176932a9b6781fa27318e83e6994548c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440993"
---
# <a name="testing-pstn-phone-call-routing-in-lync-server-2013"></a><span data-ttu-id="f135d-103">Probar el enrutamiento de llamadas de teléfono RTC en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f135d-103">Testing PSTN phone call routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f135d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f135d-104">

<span> </span></span></span>

<span data-ttu-id="f135d-105">_**Última modificación del tema:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="f135d-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f135d-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="f135d-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="f135d-107">Cada día</span><span class="sxs-lookup"><span data-stu-id="f135d-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f135d-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="f135d-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="f135d-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f135d-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f135d-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="f135d-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="f135d-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f135d-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="f135d-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe asignar un rol de RBAC que tenga permiso para ejecutar el cmdlet <strong>Test-CsInterTrunkRouting</strong> .</span><span class="sxs-lookup"><span data-stu-id="f135d-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsInterTrunkRouting</strong> cmdlet.</span></span> <span data-ttu-id="f135d-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f135d-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsInterTrunkRouting&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="f135d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f135d-114">Description</span></span>

<span data-ttu-id="f135d-115">El cmdlet **Test-CsInterTrunkRouting** verifica que las llamadas se puedan enrutar desde un SIP a otro.</span><span class="sxs-lookup"><span data-stu-id="f135d-115">The **Test-CsInterTrunkRouting** cmdlet verifies that calls can be routed from one SIP to another.</span></span> <span data-ttu-id="f135d-116">Para ello, el cmdlet recibe un número de teléfono y una configuración de tronco.</span><span class="sxs-lookup"><span data-stu-id="f135d-116">To do this, the cmdlet is given a phone number and a trunk configuration.</span></span> <span data-ttu-id="f135d-117">**Prueba-CsInterTrunkRouting** notificará las rutas de coincidencia y los usos de RTC que coincidan con el número especificado.</span><span class="sxs-lookup"><span data-stu-id="f135d-117">**Test-CsInterTrunkRouting** will then report back matching routes and matching PSTN usages for the specified number.</span></span> <span data-ttu-id="f135d-118">Tenga en cuenta que las llamadas pueden enrutarse entre líneas troncales solo si estas líneas tienen un patrón de número que coincide con el número telefónico especificado y solo si las líneas troncales comparten por lo menos un uso de RTC.</span><span class="sxs-lookup"><span data-stu-id="f135d-118">Note that calls can be routed between trunks only if the trunks have a number pattern that matches the specified phone number and only if the trunks share at least one PSTN usage.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="f135d-119">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="f135d-119">Running the test</span></span>

<span data-ttu-id="f135d-120">Los comandos que se muestran a continuación devuelven las rutas correspondientes y los usos de teléfono coincidentes que permiten a los usuarios llamar al número de teléfono 1-206-555-1219 con la configuración del tronco para el sitio de Redmond.</span><span class="sxs-lookup"><span data-stu-id="f135d-120">The commands shown below return the matching routes and matching phone usages that enable users to call the phone number 1-206-555-1219 using the trunk configuration settings for the Redmond site.</span></span>

    $trunk = Get-CsTrunkConfiguration -Identity "site:Redmond"
    
    Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219" -TrunkConfiguration $trunk

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="f135d-121">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="f135d-121">Determining success or failure</span></span>

<span data-ttu-id="f135d-122">Si las llamadas se pueden desviar de un SIP a otro, recibirás un resultado similar a este:</span><span class="sxs-lookup"><span data-stu-id="f135d-122">If calls can be routed from one SIP to another, you'll receive output similar to this:</span></span>

<span data-ttu-id="f135d-123">FirstMatchingRoute MatchingUsage MatchingRoutes</span><span class="sxs-lookup"><span data-stu-id="f135d-123">FirstMatchingRoute MatchingUsage MatchingRoutes</span></span>

<span data-ttu-id="f135d-124">\------------------ ------------- --------------</span><span class="sxs-lookup"><span data-stu-id="f135d-124">\------------------ ------------- --------------</span></span>

<span data-ttu-id="f135d-125">RedmondRoute LocalUsage {RedmondRoute}</span><span class="sxs-lookup"><span data-stu-id="f135d-125">RedmondRoute LocalUsage {RedmondRoute}</span></span>

<span data-ttu-id="f135d-126">Si la prueba no se completó correctamente, recibirá un resultado similar a este:</span><span class="sxs-lookup"><span data-stu-id="f135d-126">If the test did not succeed, you'll receive output similar to this:</span></span>

<span data-ttu-id="f135d-127">Test-CsInterTrunkRouting: no se puede procesar la transformación de argumentos en el parámetro</span><span class="sxs-lookup"><span data-stu-id="f135d-127">Test-CsInterTrunkRouting : Cannot process argument transformation on parameter</span></span>

<span data-ttu-id="f135d-128">'TrunkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="f135d-128">'TrunkConfiguration'.</span></span> <span data-ttu-id="f135d-129">TrunkConfigurationsetting (parámetro) no válido.</span><span class="sxs-lookup"><span data-stu-id="f135d-129">Invalid TrunkConfigurationsetting (parameter).</span></span> <span data-ttu-id="f135d-130">Especificar un</span><span class="sxs-lookup"><span data-stu-id="f135d-130">Specify a</span></span>

<span data-ttu-id="f135d-131">configuración válida (parámetro) y, a continuación, inténtalo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="f135d-131">valid setting (parameter) and then try again.</span></span>

<span data-ttu-id="f135d-132">En la línea: 1 carácter: 79</span><span class="sxs-lookup"><span data-stu-id="f135d-132">At line:1 char:79</span></span>

<span data-ttu-id="f135d-133">\+ Test-CsInterTrunkRouting-TargetNumber "Tel: + 12065551219"</span><span class="sxs-lookup"><span data-stu-id="f135d-133">\+ Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219"</span></span>

<span data-ttu-id="f135d-134">\-TrunkConfiguration $t...</span><span class="sxs-lookup"><span data-stu-id="f135d-134">\-TrunkConfiguration $t ...</span></span>

\+

~~

<span data-ttu-id="f135d-135">\+ CategoryInfo: InvalidData: (:) \[ Prueba-CsInterTrunkRouting \] , par</span><span class="sxs-lookup"><span data-stu-id="f135d-135">\+ CategoryInfo : InvalidData: (:) \[Test-CsInterTrunkRouting\], Par</span></span>

<span data-ttu-id="f135d-136">ameterBindingArgumentTransformationException</span><span class="sxs-lookup"><span data-stu-id="f135d-136">ameterBindingArgumentTransformationException</span></span>

<span data-ttu-id="f135d-137">\+ FullyQualifiedErrorId: ParameterArgumentTransformationError, Microsoft. R</span><span class="sxs-lookup"><span data-stu-id="f135d-137">\+ FullyQualifiedErrorId : ParameterArgumentTransformationError,Microsoft.R</span></span>

<span data-ttu-id="f135d-138">CT. Management. Voice. cmdlets. TestOcsInterTrunkRoutingCmdlet</span><span class="sxs-lookup"><span data-stu-id="f135d-138">tc.Management.Voice.Cmdlets.TestOcsInterTrunkRoutingCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="f135d-139">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="f135d-139">Reasons why the test might have failed</span></span>

<span data-ttu-id="f135d-140">Estas son algunas de las razones comunes por las que **Test-CsInterTrunkRouting** podría fallar:</span><span class="sxs-lookup"><span data-stu-id="f135d-140">Here are some common reasons why **Test-CsInterTrunkRouting** might fail:</span></span>

  - <span data-ttu-id="f135d-141">Ha especificado parámetros no válidos.</span><span class="sxs-lookup"><span data-stu-id="f135d-141">You specified invalid parameters.</span></span> <span data-ttu-id="f135d-142">Es posible que el tronco no esté configurado correctamente y que el número de destino especificado sea incorrecto o no válido.</span><span class="sxs-lookup"><span data-stu-id="f135d-142">The trunk might not yet be correctly configured and the specified target number might be incorrect or invalid.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f135d-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="f135d-143">See Also</span></span>


[<span data-ttu-id="f135d-144">Get-CsTrunk</span><span class="sxs-lookup"><span data-stu-id="f135d-144">Get-CsTrunk</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunk)  
[<span data-ttu-id="f135d-145">Get-CsTrunkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f135d-145">Get-CsTrunkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration)  
  

<span data-ttu-id="f135d-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f135d-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

