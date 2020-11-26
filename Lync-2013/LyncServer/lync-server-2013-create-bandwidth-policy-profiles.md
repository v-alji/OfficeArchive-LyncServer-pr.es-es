---
title: 'Lync Server 2013: crear perfiles de directiva de ancho de banda'
description: 'Lync Server 2013: crear perfiles de directiva de ancho de banda.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create bandwidth policy profiles
ms:assetid: a71881ef-b04a-465e-9abb-0577bfd182f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412785(v=OCS.15)
ms:contentKeyID: 48185086
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9646657c84806bff8caef3352774cdc5ddeab862
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431984"
---
# <a name="create-bandwidth-policy-profiles-in-lync-server-2013"></a><span data-ttu-id="dc202-103">Crear perfiles de directiva de ancho de banda en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc202-103">Create bandwidth policy profiles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc202-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc202-104">

<span> </span></span></span>

<span data-ttu-id="dc202-105">_**Última modificación del tema:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="dc202-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="dc202-p101">Las *directivas de ancho de banda* definen limitaciones en el uso de ancho de banda para las modalidades de audio y vídeo en tiempo real. Las directivas de ancho de banda se aplican a los *perfiles de directiva de ancho de banda*, que pueden aplicarse a varios sitios de red para el control de admisión de llamadas.</span><span class="sxs-lookup"><span data-stu-id="dc202-p101">*Bandwidth policies* define limitations on bandwidth usage for real-time audio and video modalities. Bandwidth policies are applied to *bandwidth policy profiles*, which can be applied to multiple network sites for call admission control.</span></span>

<span data-ttu-id="dc202-108">Para obtener instrucciones sobre qué límites de ancho de banda debe establecer en su implementación CAC, consulte [definir los requisitos para el control de admisión de llamadas en Lync Server 2013](lync-server-2013-defining-your-requirements-for-call-admission-control.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="dc202-108">For guidelines about what bandwidth limits you should set in your CAC deployment, see [Defining your requirements for call admission control in Lync Server 2013](lync-server-2013-defining-your-requirements-for-call-admission-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="dc202-109">Para obtener más información sobre cómo trabajar con directivas de ancho de banda y perfiles de Directiva, consulte la documentación del shell de administración de Lync Server para los siguientes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="dc202-109">For details about working with bandwidth policies and policy profiles, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="dc202-110">New-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="dc202-110">New-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkBandwidthPolicyProfile)

  - [<span data-ttu-id="dc202-111">Get-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="dc202-111">Get-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile)

  - [<span data-ttu-id="dc202-112">Set-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="dc202-112">Set-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkBandwidthPolicyProfile)

  - [<span data-ttu-id="dc202-113">Remove-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="dc202-113">Remove-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkBandwidthPolicyProfile)

<span data-ttu-id="dc202-114">Las directivas de ejemplo creadas en el procedimiento siguiente definen límites para el tráfico de audio global, sesiones de audio individuales, el tráfico de vídeo global y sesiones de vídeo individuales.</span><span class="sxs-lookup"><span data-stu-id="dc202-114">The example policies created in the following procedure set limits for overall audio traffic, individual audio sessions, overall video traffic, and individual video sessions.</span></span> <span data-ttu-id="dc202-115">Por ejemplo, el perfil de directiva de ancho de banda del vínculo de 5 MB \_ establece los siguientes límites:</span><span class="sxs-lookup"><span data-stu-id="dc202-115">For example, the 5Mb\_Link bandwidth policy profile sets the following limits:</span></span>

  - <span data-ttu-id="dc202-116">Límite de audio: 2.000 kbps</span><span class="sxs-lookup"><span data-stu-id="dc202-116">Audio Limit: 2,000 kbps</span></span>

  - <span data-ttu-id="dc202-117">Límite de sesión de audio: 200 kbps</span><span class="sxs-lookup"><span data-stu-id="dc202-117">Audio Session Limit: 200 kbps</span></span>

  - <span data-ttu-id="dc202-118">Límite de vídeo: 1.400 kbps</span><span class="sxs-lookup"><span data-stu-id="dc202-118">Video Limit: 1,400 kbps</span></span>

  - <span data-ttu-id="dc202-119">Límite de sesión de vídeo: 700 kbps</span><span class="sxs-lookup"><span data-stu-id="dc202-119">Video Session Limit: 700 kbps</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="dc202-p103">El valor de Límite de sesión de audio es 40 kbps. El valor de Límite de sesión de vídeo es 100 kbps.</span><span class="sxs-lookup"><span data-stu-id="dc202-p103">The minimum Audio Session Limit value is 40 kbps. The minimum Video Session Limit value is 100 kbps.</span></span>



</div>

<div>

## <a name="to-create-bandwidth-policy-profiles-by-using-management-shell"></a><span data-ttu-id="dc202-122">Para crear perfiles de directiva de ancho de banda mediante el shell de administración</span><span class="sxs-lookup"><span data-stu-id="dc202-122">To create bandwidth policy profiles by using Management Shell</span></span>

1.  <span data-ttu-id="dc202-123">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="dc202-123">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="dc202-124">Para cada perfil de directiva de ancho de banda que quiera crear, ejecute el cmdlet New-CsNetworkBandwidthPolicyProfile.</span><span class="sxs-lookup"><span data-stu-id="dc202-124">For each bandwidth policy profile that you want to create, run the New-CsNetworkBandwidthPolicyProfile cmdlet.</span></span> <span data-ttu-id="dc202-125">Por ejemplo, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="dc202-125">For example, run:</span></span>
    
       ```powershell
        New-CsNetworkBandwidthPolicyProfile -Identity 5Mb_Link -Description "BW profile for 5Mb links" -AudioBWLimit 2000 -AudioBWSessionLimit 200 -VideoBWLimit 1400  -VideoBWSessionLimit 700
       ```
    
       ```powershell
        New-CsNetworkBandwidthPolicyProfile -Identity 10Mb_Link -Description "BW profile for 10Mb links" -AudioBWLimit 4000 -AudioBWSessionLimit 200 -VideoBWLimit 2800 -VideoBWSessionLimit 700
       ```
    
       ```powershell
        New-CsNetworkBandwidthPolicyProfile -Identity 50Mb_Link -Description "BW profile for 50Mb links" -AudioBWLimit 20000 -AudioBWSessionLimit 200 -VideoBWLimit 14000 -VideoBWSessionLimit 700
       ```
    
       ```powershell
        New-CsNetworkBandwidthPolicyProfile -Identity 25Mb_Link -Description "BW profile for 25Mb links" -AudioBWLimit 10000 -AudioBWSessionLimit 200 -VideoBWLimit 7000 -VideoBWSessionLimit 700
       ```

</div>

<div>

## <a name="to-create-bandwidth-policy-profiles-by-using-lync-server-control-panel"></a><span data-ttu-id="dc202-126">Para crear perfiles de directiva de ancho de banda mediante el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="dc202-126">To create bandwidth policy profiles by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="dc202-127">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dc202-127">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="dc202-128">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="dc202-128">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="dc202-129">En la barra de navegación izquierda, haga clic en **Configuración de red**.</span><span class="sxs-lookup"><span data-stu-id="dc202-129">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="dc202-130">Haga clic en el botón de navegación **Perfil de directiva**.</span><span class="sxs-lookup"><span data-stu-id="dc202-130">Click the **Policy Profile** navigation button.</span></span>

4.  <span data-ttu-id="dc202-131">Haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="dc202-131">Click **New**.</span></span>

5.  <span data-ttu-id="dc202-132">En la página **Nuevo perfil de directiva**, haga clic en **Nombre** y escriba un nombre para el perfil de directiva de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="dc202-132">On the **New Policy Profile** page, click **Name** and then type a name for the bandwidth policy profile.</span></span>

6.  <span data-ttu-id="dc202-133">Haga clic en **Límite de audio** y escriba el número máximo de kbps que se deben permitir para todas las sesiones de audio combinadas.</span><span class="sxs-lookup"><span data-stu-id="dc202-133">Click **Audio limit**, and then type in the maximum number of kbps to allow for all audio sessions combined.</span></span>

7.  <span data-ttu-id="dc202-134">Haga clic en **Límite de sesión de audio** y escriba el número máximo de kbps que se deben permitir para cada sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="dc202-134">Click **Audio session limit**, and then type in the maximum number of kbps to allow for each individual audio session.</span></span>

8.  <span data-ttu-id="dc202-135">Haga clic en **Límite de vídeo** y escriba el número máximo de kbps que se deben permitir para todas las sesiones de vídeo combinadas.</span><span class="sxs-lookup"><span data-stu-id="dc202-135">Click **Video limit**, and then type in the maximum number of kbps to allow for all video sessions combined.</span></span>

9.  <span data-ttu-id="dc202-136">Haga clic en **Límite de sesión de vídeo** y escriba el número máximo de kbps que se deben permitir para cada sesión de vídeo.</span><span class="sxs-lookup"><span data-stu-id="dc202-136">Click **Video session limit**, and then type in the maximum number of kbps to allow for each individual video session.</span></span>

10. <span data-ttu-id="dc202-137">Si lo desea, haga clic en **Descripción** y escriba información adicional para describir este perfil de directiva de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="dc202-137">Optionally, click **Description**, and then type additional information to describe this bandwidth policy profile.</span></span>

11. <span data-ttu-id="dc202-138">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="dc202-138">Click **Commit**.</span></span>

12. <span data-ttu-id="dc202-139">Para terminar de crear perfiles de directiva de ancho de banda para su topología, repita los pasos del 4 al 11 con la configuración para otros perfiles de directiva de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="dc202-139">To finish creating bandwidth policy profiles for your topology, repeat steps 4 through 11 with settings for other bandwidth policy profiles.</span></span>

<span data-ttu-id="dc202-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc202-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

