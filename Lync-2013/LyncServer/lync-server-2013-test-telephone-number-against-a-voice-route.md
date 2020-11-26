---
title: 'Lync Server 2013: probar el número de teléfono en una ruta de voz'
description: 'Lync Server 2013: Pruebe el número de teléfono en una ruta de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test telephone number against a voice route
ms:assetid: 9a77ed6d-9394-4bef-9344-3d91b6959b97
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725211(v=OCS.15)
ms:contentKeyID: 63969631
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 789f4a538a992a72abf61f4c1fbdb98370f2e643
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444241"
---
# <a name="test-telephone-number-against-a-voice-route-in-lync-server-2013"></a><span data-ttu-id="99182-103">Probar el número de teléfono en una ruta de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99182-103">Test telephone number against a voice route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99182-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99182-104">

<span> </span></span></span>

<span data-ttu-id="99182-105">_**Última modificación del tema:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="99182-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99182-106">Programación de verificación</span><span class="sxs-lookup"><span data-stu-id="99182-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="99182-107">Cada mes</span><span class="sxs-lookup"><span data-stu-id="99182-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99182-108">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="99182-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="99182-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="99182-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99182-110">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="99182-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="99182-111">Al ejecutarse de forma local con el shell de administración de Lync Server, los usuarios deben ser miembros del grupo de seguridad RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="99182-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="99182-112">Cuando se ejecuta con una instancia remota de Windows PowerShell, a los usuarios se les debe haber asignado un rol de RBAC que tenga permiso para ejecutar el cmdlet Test-CsVoiceRoute.</span><span class="sxs-lookup"><span data-stu-id="99182-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceRoute cmdlet.</span></span> <span data-ttu-id="99182-113">Para ver una lista de todos los roles de RBAC que pueden usar este cmdlet, ejecute el siguiente comando en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="99182-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceRoute&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="99182-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="99182-114">Description</span></span>

<span data-ttu-id="99182-115">Las rutas de voz funcionan conjuntamente con directivas de voz para ayudar a dirigir llamadas de voz empresariales a la red RTC.</span><span class="sxs-lookup"><span data-stu-id="99182-115">Voice routes work together with voice policies to help route Enterprise Voice calls to the PSTN network.</span></span> <span data-ttu-id="99182-116">Cada ruta de voz incluye una expresión regular (un patrón de número) que identifica los números de teléfono que se redirigirán a través de una ruta de voz determinada: la ruta podrá controlar cualquier número de teléfono que coincida con esta expresión regular.</span><span class="sxs-lookup"><span data-stu-id="99182-116">Each voice route includes a regular expression (a number pattern) that identifies the phone numbers that will be routed through a given voice route: the route will be able to handle any phone numbers that match this regular expression.</span></span> <span data-ttu-id="99182-117">Por ejemplo, una ruta de voz puede tener una expresión regular que le permite controlar cualquier número de 10 dígitos.</span><span class="sxs-lookup"><span data-stu-id="99182-117">For example, a voice route might have a regular expression that enables it to handle any 10-digit number.</span></span> <span data-ttu-id="99182-118">Eso significa que la ruta podría controlar un número de teléfono como este:</span><span class="sxs-lookup"><span data-stu-id="99182-118">That means the route would be able to handle a phone number such as this:</span></span>

  - <span data-ttu-id="99182-119">2065551219</span><span class="sxs-lookup"><span data-stu-id="99182-119">2065551219</span></span>

<span data-ttu-id="99182-120">La ruta no podría controlar ninguno de los dos números siguientes, ninguno de los cuales tiene 10 dígitos:</span><span class="sxs-lookup"><span data-stu-id="99182-120">The route would not be able to handle either of the following two numbers, neither of which has 10 digits:</span></span>

  - <span data-ttu-id="99182-121">5551219</span><span class="sxs-lookup"><span data-stu-id="99182-121">5551219</span></span>

  - <span data-ttu-id="99182-122">12065551219</span><span class="sxs-lookup"><span data-stu-id="99182-122">12065551219</span></span>

<span data-ttu-id="99182-123">El cmdlet Test-CsVoiceRoute comprueba si una ruta de voz determinada puede enrutar un número de teléfono especificado.</span><span class="sxs-lookup"><span data-stu-id="99182-123">The Test-CsVoiceRoute cmdlet verifies whether a given voice route can route a specified phone number.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="99182-124">Ejecutar la prueba</span><span class="sxs-lookup"><span data-stu-id="99182-124">Running the test</span></span>

<span data-ttu-id="99182-125">Comprobar la capacidad de una ruta de voz para enrutar un número de teléfono especificado es un proceso de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="99182-125">Verifying the ability of a voice route to route a specified phone number is a two-step process.</span></span> <span data-ttu-id="99182-126">Primero tiene que usar el cmdlet Get-CsVoiceRoute para devolver una instancia de esa ruta de voz y, a continuación, debe usar el cmdlet de Test-CsVoiceRoute para comprobar la capacidad de esa ruta para controlar el número de teléfono de destino.</span><span class="sxs-lookup"><span data-stu-id="99182-126">First you have to use the Get-CsVoiceRoute cmdlet to return an instance of that voice route, and then you have to use the Test-CsVoiceRoute cmdlet to verify the ability of that route to handle the target phone number.</span></span> <span data-ttu-id="99182-127">Por ejemplo, este comando comprueba si la ruta de voz RedmondVoiceRoute puede enrutar el número de teléfono 2065551219:</span><span class="sxs-lookup"><span data-stu-id="99182-127">For example, this command verifies whether the RedmondVoiceRoute voice route can route the phone number 2065551219:</span></span>

`Get-CsVoiceRoute -Identity "RedmondVoiceRoute" | Test-CsVoiceRoute -TargetNumber "2065551219"`

<span data-ttu-id="99182-128">Ten en cuenta que el número de teléfono debe escribirse tal como espera que los usuarios marquen ese número.</span><span class="sxs-lookup"><span data-stu-id="99182-128">Note that the phone number should be typed as you expect users to dial that number.</span></span> <span data-ttu-id="99182-129">Por ejemplo, si no espera que los usuarios incluyan el prefijo internacional y el código de área al marcar, entonces use una sintaxis similar a esta:</span><span class="sxs-lookup"><span data-stu-id="99182-129">For example, if you do not expect users to include the country code and area code when dialing, then use syntax similar to this:</span></span>

`-TargetNumber "5551219"`

<span data-ttu-id="99182-130">En este caso, el número de destino deja el prefijo internacional y el código de área.</span><span class="sxs-lookup"><span data-stu-id="99182-130">In this case, the target number leaves out both the country code and the area code.</span></span>

<span data-ttu-id="99182-131">Para usar un solo comando para probar todas las rutas de voz con un número de destino especificado, use una sintaxis como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="99182-131">To use a single command to test all the voice routes against a specified target number, use syntax such as the following:</span></span>

`Get-CsVoiceRoute | Test-CsVoiceRoute -TargetNumber "2065551219"`

<span data-ttu-id="99182-132">Para obtener más información, consulte la documentación de ayuda del cmdlet Test-CsVoiceRoute.</span><span class="sxs-lookup"><span data-stu-id="99182-132">For more information, see the Help documentation for the Test-CsVoiceRoute cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="99182-133">Determinar el éxito o el fracaso</span><span class="sxs-lookup"><span data-stu-id="99182-133">Determining success or failure</span></span>

<span data-ttu-id="99182-134">Si la ruta de voz puede enrutar el número de teléfono de destino, el cmdlet Test-CsVoiceRoute solo devuelve el valor true:</span><span class="sxs-lookup"><span data-stu-id="99182-134">If the voice route can route the target phone number the Test-CsVoiceRoute cmdlet just returns the value True:</span></span>

<span data-ttu-id="99182-135">MatchesPattern</span><span class="sxs-lookup"><span data-stu-id="99182-135">MatchesPattern</span></span>

\--------------

<span data-ttu-id="99182-136">Verdadero</span><span class="sxs-lookup"><span data-stu-id="99182-136">True</span></span>

<span data-ttu-id="99182-137">Eso significa que Route puede administrar números similares al número de destino.</span><span class="sxs-lookup"><span data-stu-id="99182-137">That means that route can handle numbers similar to the target number.</span></span> <span data-ttu-id="99182-138">Si la ruta de voz no puede controlar el número de destino, Test-CsVoiceRoute devuelve el valor falso:</span><span class="sxs-lookup"><span data-stu-id="99182-138">If the voice route is can't handle the target number then Test-CsVoiceRoute returns the value False:</span></span>

<span data-ttu-id="99182-139">MatchesPattern</span><span class="sxs-lookup"><span data-stu-id="99182-139">MatchesPattern</span></span>

\--------------

<span data-ttu-id="99182-140">Falso</span><span class="sxs-lookup"><span data-stu-id="99182-140">False</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="99182-141">Razones por las que se ha producido un error en la prueba</span><span class="sxs-lookup"><span data-stu-id="99182-141">Reasons why the test might have failed</span></span>

<span data-ttu-id="99182-142">Al probar las rutas de voz, "error" es un término relativo.</span><span class="sxs-lookup"><span data-stu-id="99182-142">When testing voice routes, “failure” is a relative term.</span></span> <span data-ttu-id="99182-143">En este caso, no significa que la ruta esté de alguna manera "dañada", sino que simplemente significa que la ruta no puede controlar el número de destino.</span><span class="sxs-lookup"><span data-stu-id="99182-143">In this case, it doesn’t mean that the route is somehow “broken;” instead, it just means that the route can't handle the target number.</span></span> <span data-ttu-id="99182-144">Esto puede deberse a que la ruta de voz no se ha configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="99182-144">That could be because the voice route was configured incorrectly.</span></span> <span data-ttu-id="99182-145">También podría significar que la ruta nunca estaba destinada a tratar números usando este patrón.</span><span class="sxs-lookup"><span data-stu-id="99182-145">It could also mean that the route was never intended to handle numbers using this pattern.</span></span> <span data-ttu-id="99182-146">Por ejemplo, si no deseas enrutar llamadas a otros países a través de una ruta determinada, la ruta podría estar configurada para rechazar todos los números de teléfono que incluyan un prefijo internacional.</span><span class="sxs-lookup"><span data-stu-id="99182-146">For example, if you do not want to route calls to other countries over a given route that route might be configured to reject all phone numbers that include a country code.</span></span> <span data-ttu-id="99182-147">Si Test-CsVoiceRoute devuelve false cuando se espera que devuelva true, compruebe que escribió el número de destino correctamente.</span><span class="sxs-lookup"><span data-stu-id="99182-147">If Test-CsVoiceRoute returns False when you expected it to return True, verify that you typed the target number in correctly.</span></span> <span data-ttu-id="99182-148">Si lo hizo, use un comando similar a este para ver la NumberPattern configurada para la ruta:</span><span class="sxs-lookup"><span data-stu-id="99182-148">If you did, then use a command similar to this one to view the NumberPattern configured for the route:</span></span>

`Get-CsVoiceRoute -Identity "RedmondVoiceRoute" | Select-Object NumberPattern`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="99182-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="99182-149">See Also</span></span>


[<span data-ttu-id="99182-150">Prueba-CsVoiceRoute</span><span class="sxs-lookup"><span data-stu-id="99182-150">Test-CsVoiceRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceRoute)  
  

<span data-ttu-id="99182-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99182-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

