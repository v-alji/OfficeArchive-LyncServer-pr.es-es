---
title: 'Lync Server 2013: ejecutar la ruta de voz casos de prueba'
description: 'Lync Server 2013: ejecutar la ruta de voz de casos de prueba.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Run voice routing test cases
ms:assetid: fb4d32df-b9ea-4944-8cd7-a6102c78c465
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413068(v=OCS.15)
ms:contentKeyID: 48185948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e521216a12fba6b78913e7f4a79432809bb6e252
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398165"
---
# <a name="run-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="d5e5e-103">Ejecutar los casos de prueba de enrutamiento de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5e5e-103">Run voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5e5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5e5e-104">

<span> </span></span></span>

<span data-ttu-id="d5e5e-105">_**Última modificación del tema:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="d5e5e-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="d5e5e-106">Puede ejecutar todos los casos de prueba en el conjunto de casos de prueba de enrutamiento de voz, o bien puede ejecutar uno o varios casos de prueba seleccionados.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-106">You can run all of the test cases in your voice routing test case suite, or you can run one or more selected test cases.</span></span>

<div>

## <a name="to-run-all-voice-routing-test-cases"></a><span data-ttu-id="d5e5e-107">Para ejecutar todos los casos de prueba de enrutamiento de voz</span><span class="sxs-lookup"><span data-stu-id="d5e5e-107">To run all voice routing test cases</span></span>

1.  <span data-ttu-id="d5e5e-108">Inicie sesión en el equipo como miembro del grupo RTCUniversalServerAdmins o como miembro del rol CsVoiceAdministrator, CsServerAdministrator o CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-108">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="d5e5e-109">Para obtener más información, consulte [permisos de configuración de delegación en Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d5e5e-109">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="d5e5e-110">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d5e5e-111">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d5e5e-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d5e5e-112">En la barra de navegación izquierda, haga clic en **enrutamiento de voz** y luego en **probar enrutamiento de voz**.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-112">In the left navigation bar, click **Voice Routing** and then click **Test Voice Routing**.</span></span>

4.  <span data-ttu-id="d5e5e-113">En la página **probar enrutamiento de voz** , haga clic en **acción** y, a continuación, en **ejecutar todo**.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-113">On the **Test Voice Routing** page, click **Action** and then click **Run all**.</span></span>
    
    <span data-ttu-id="d5e5e-114">El estado de paso o error de cada caso de prueba se muestra en la columna **correcto o error** .</span><span class="sxs-lookup"><span data-stu-id="d5e5e-114">The pass or fail status of each test case is shown in the **Pass/fail** column.</span></span> <span data-ttu-id="d5e5e-115">Si aún no se ha ejecutado un caso de prueba, se muestra N/A en la columna **correcto o error** .</span><span class="sxs-lookup"><span data-stu-id="d5e5e-115">If a test case has not yet been run, N/A is shown in the **Pass/fail** column.</span></span>

5.  <span data-ttu-id="d5e5e-116">Faculta Para ver los resultados detallados de cada caso de prueba, haga doble clic en el nombre del caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-116">(Optional) To see detailed results for each test case, double-click the test case name.</span></span> <span data-ttu-id="d5e5e-117">Los resultados se muestran en el área sombreada en el lado derecho de la página **Editar caso de prueba** :</span><span class="sxs-lookup"><span data-stu-id="d5e5e-117">Results are shown in the shaded area on the right side of the **Edit Test Case** page:</span></span>
    
    1.  <span data-ttu-id="d5e5e-118">**Resultado de la prueba:** Estado general de paso o error de la ejecución del caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-118">**Test result:** Overall pass or fail status of the test case run.</span></span>
    
    2.  <span data-ttu-id="d5e5e-119">**Regla de normalización:** La primera regla de normalización seleccionada en el plan de marcado para este caso de prueba que coincide con el número marcado (el valor del campo **número para probar** ).</span><span class="sxs-lookup"><span data-stu-id="d5e5e-119">**Normalization rule:** The first normalization rule in the dial plan selected for this test case that matches the dialed number (the value in the **Number to test** field).</span></span>
    
    3.  <span data-ttu-id="d5e5e-120">**Número normalizado:** El valor del número marcado después de que la regla de normalización la haya traducido.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-120">**Normalized number:** The value of the dialed number after the normalization rule has translated it.</span></span>
    
    4.  <span data-ttu-id="d5e5e-121">**Primer uso de la RTC:** El primer registro de uso de la red telefónica conmutada (RTC) en la Directiva de voz seleccionada para este caso de prueba que coincide con el número marcado.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-121">**First PSTN usage:** The first public switched telephone network (PSTN) usage record in the voice policy selected for this test case that matches the dialed number.</span></span>
    
    5.  <span data-ttu-id="d5e5e-122">**Primera ruta:** La primera ruta de voz del primer registro de uso de RTC que coincide con el número marcado.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-122">**First route:** The first voice route in the first PSTN usage record that matches the dialed number.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="d5e5e-123">El <STRONG>registro de uso de RTC esperado</STRONG> y los campos de <STRONG>ruta previstos</STRONG> son opcionales en la configuración del caso de prueba de enrutamiento de voz.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-123">The <STRONG>Expected PSTN usage record</STRONG> and <STRONG>Expected route</STRONG> fields are optional in voice routing test case configuration.</span></span> <span data-ttu-id="d5e5e-124">Si el caso de prueba no especifica estos valores, el campo correspondiente en los resultados de la prueba estará vacío.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-124">If the test case does not specify these values, the corresponding field in the test results will be empty.</span></span>

        
        </div>

</div>

<div>

## <a name="to-run-one-or-more-selected-voice-routing-test-cases"></a><span data-ttu-id="d5e5e-125">Para ejecutar uno o varios casos de prueba de enrutamiento de voz seleccionados</span><span class="sxs-lookup"><span data-stu-id="d5e5e-125">To run one or more selected voice routing test cases</span></span>

1.  <span data-ttu-id="d5e5e-126">Inicie sesión en el equipo como miembro del grupo RTCUniversalServerAdmins o como miembro del rol CsVoiceAdministrator, CsServerAdministrator o CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-126">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="d5e5e-127">Para obtener más información, consulte [permisos de configuración de delegación en Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d5e5e-127">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="d5e5e-128">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-128">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d5e5e-129">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d5e5e-129">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d5e5e-130">En la barra de navegación izquierda, haga clic en **enrutamiento de voz** y, a continuación, en **probar enrutamiento de voz**.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-130">In the left navigation bar, click **Voice Routing**, and then click **Test Voice Routing**.</span></span>

4.  <span data-ttu-id="d5e5e-131">En la página **probar enrutamiento de voz** , haga clic en los nombres de los casos de prueba que desee ejecutar.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-131">On the **Test Voice Routing** page, click the names of the test cases that you want to run.</span></span>

5.  <span data-ttu-id="d5e5e-132">En el menú **acción** , haga clic en **Ejecutar seleccionado**.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-132">On the **Action** menu, click **Run selected**.</span></span>
    
    <span data-ttu-id="d5e5e-133">El estado de paso o error de cada caso de prueba se muestra en la columna **correcto o error** .</span><span class="sxs-lookup"><span data-stu-id="d5e5e-133">The pass or fail status of each test case is shown in the **Pass/fail** column.</span></span> <span data-ttu-id="d5e5e-134">Si aún no se ha ejecutado un caso de prueba, se muestra N/A en la columna **correcto o error** .</span><span class="sxs-lookup"><span data-stu-id="d5e5e-134">If a test case has not yet been run, N/A is shown in the **Pass/fail** column.</span></span>

6.  <span data-ttu-id="d5e5e-135">Faculta Para ver los resultados detallados de cada caso de prueba, haga doble clic en el nombre del caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-135">(Optional) To see detailed results for each test case, double-click the test case name.</span></span> <span data-ttu-id="d5e5e-136">Los resultados se muestran en el área sombreada en el lado derecho de la página **Editar caso de prueba** :</span><span class="sxs-lookup"><span data-stu-id="d5e5e-136">Results are shown in the shaded area on the right side of the **Edit Test Case** page:</span></span>
    
    1.  <span data-ttu-id="d5e5e-137">**Resultado de la prueba:** Estado general de paso o error de la ejecución del caso de prueba.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-137">**Test result:** Overall pass or fail status of the test case run.</span></span>
    
    2.  <span data-ttu-id="d5e5e-138">**Regla de normalización:** La primera regla de normalización seleccionada en el plan de marcado para este caso de prueba que coincide con el número marcado (el valor del campo **número para probar** ).</span><span class="sxs-lookup"><span data-stu-id="d5e5e-138">**Normalization rule:** The first normalization rule in the dial plan selected for this test case that matches the dialed number (the value in the **Number to test** field).</span></span>
    
    3.  <span data-ttu-id="d5e5e-139">**Número normalizado:** El valor del número marcado después de que la regla de normalización la haya traducido.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-139">**Normalized number:** The value of the dialed number after the normalization rule has translated it.</span></span>
    
    4.  <span data-ttu-id="d5e5e-140">**Primer uso de la RTC:** El primer registro de uso de RTC de la Directiva de voz seleccionada para este caso de prueba que coincide con el número marcado.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-140">**First PSTN usage:** The first PSTN usage record in the voice policy selected for this test case that matches the dialed number.</span></span>
    
    5.  <span data-ttu-id="d5e5e-141">**Primera ruta:** La primera ruta de voz del primer registro de uso de RTC que coincide con el número marcado.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-141">**First route:** The first voice route in the first PSTN usage record that matches the dialed number.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="d5e5e-142">El <STRONG>registro de uso de RTC esperado</STRONG> y los campos de <STRONG>ruta previstos</STRONG> son opcionales en la configuración del caso de prueba de enrutamiento de voz.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-142">The <STRONG>Expected PSTN usage record</STRONG> and <STRONG>Expected route</STRONG> fields are optional in voice routing test case configuration.</span></span> <span data-ttu-id="d5e5e-143">Si el caso de prueba no especifica estos valores, el campo correspondiente en los resultados de la prueba estará vacío.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-143">If the test case does not specify these values, the corresponding field in the test results will be empty.</span></span>

        
        </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d5e5e-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5e5e-144">See Also</span></span>


[<span data-ttu-id="d5e5e-145">Probar el enrutamiento de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5e5e-145">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
[<span data-ttu-id="d5e5e-146">Ejecución de pruebas de enrutamiento de voz en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5e5e-146">Running voice routing tests in Lync Server 2013</span></span>](lync-server-2013-running-voice-routing-tests.md)  
  

<span data-ttu-id="d5e5e-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5e5e-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

