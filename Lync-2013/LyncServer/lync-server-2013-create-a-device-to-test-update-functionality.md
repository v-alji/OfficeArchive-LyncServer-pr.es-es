---
title: 'Lync Server 2013: crear un dispositivo para probar la funcionalidad de actualización'
description: 'Lync Server 2013: cree un dispositivo para probar la funcionalidad de actualización.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a device to test update functionality
ms:assetid: ce509fd1-17b3-4b78-b269-fe5d06fe2e1d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182587(v=OCS.15)
ms:contentKeyID: 48185466
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d45d8970dc72abc8ea6095c879272394e34c54d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432243"
---
# <a name="create-a-device-to-test-update-functionality-in-lync-server-2013"></a><span data-ttu-id="8c773-103">Crear un dispositivo para probar la funcionalidad de actualización en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c773-103">Create a device to test update functionality in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c773-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c773-104">

<span> </span></span></span>

<span data-ttu-id="8c773-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="8c773-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="8c773-106">Puede agregar un dispositivo de prueba a la página **Dispositivo de prueba** y, luego, usar este dispositivo para comprobar la funcionalidad de las actualizaciones nuevas antes de implementarlas en los dispositivos de producción.</span><span class="sxs-lookup"><span data-stu-id="8c773-106">You can add a test device to the **Test Device** page and then use this device to verify the functionality of new updates before deploying the updates to production devices.</span></span> <span data-ttu-id="8c773-107">Puede probar un dispositivo de forma global (en todo el entorno de Lync Server) o dentro de un solo sitio.</span><span class="sxs-lookup"><span data-stu-id="8c773-107">You can test a device globally (throughout your entire Lync Server environment) or within a single site.</span></span> <span data-ttu-id="8c773-108">Un dispositivo de prueba se identifica por su dirección Media Access Control (MAC) o número de serie.</span><span class="sxs-lookup"><span data-stu-id="8c773-108">You identify a test device by its Media Access Control (MAC) address or serial number.</span></span> <span data-ttu-id="8c773-109">Cuando agregue un dispositivo, aparecerá en la lista de la página **probar dispositivo** del panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8c773-109">When you add a device, it appears in the list on the **Test Device** page of the Lync Server Control Panel.</span></span>

<div>

## <a name="to-add-a-test-device"></a><span data-ttu-id="8c773-110">Para agregar un dispositivo de prueba</span><span class="sxs-lookup"><span data-stu-id="8c773-110">To add a test device</span></span>

1.  <span data-ttu-id="8c773-111">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8c773-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8c773-112">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8c773-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="8c773-113">En la barra de navegación izquierda, haga clic en **clientes** y, a continuación, haga clic en **probar dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="8c773-113">In the left navigation bar, click **Clients**, and then click **Test Device**.</span></span>

3.  <span data-ttu-id="8c773-114">Haga clic en **nuevo** y, a continuación, en **dispositivo de prueba global** o **dispositivo de prueba del sitio**.</span><span class="sxs-lookup"><span data-stu-id="8c773-114">Click **New**, and then click either **Global test device** or **Site test device**.</span></span>

4.  <span data-ttu-id="8c773-115">Realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="8c773-115">Do one of the following:</span></span>
    
      - <span data-ttu-id="8c773-116">Si hizo clic en **dispositivo de prueba global**, vaya al siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="8c773-116">If you clicked **Global test device**, skip to the next step.</span></span>
    
      - <span data-ttu-id="8c773-117">Si hizo clic en **dispositivo de prueba de sitio**, seleccione un sitio de la lista de sitios disponibles y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8c773-117">If you clicked **Site test device**, select a site from the list of available sites, and then click **OK**.</span></span>

5.  <span data-ttu-id="8c773-118">En **nuevo dispositivo de prueba**, escriba un nombre para el dispositivo en **nombre del dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="8c773-118">In **New Test Device**, type a name for the device in **Device name**.</span></span>

6.  <span data-ttu-id="8c773-119">En **tipo de identificador**, haga clic en **dirección Mac** o en **número de serie**.</span><span class="sxs-lookup"><span data-stu-id="8c773-119">Under **Identifier type**, click either **MAC address** or **Serial number**.</span></span>

7.  <span data-ttu-id="8c773-120">En el cuadro **identificador único** , escriba la dirección Mac o el número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c773-120">In the **Unique identifier** box, type the MAC address or serial number of the device.</span></span>

8.  <span data-ttu-id="8c773-121">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="8c773-121">Click **Commit**.</span></span>

</div>

<div>

## <a name="creating-test-devices-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="8c773-122">Creación de dispositivos de prueba con cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c773-122">Creating Test Devices by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="8c773-123">Los dispositivos de prueba se pueden crear con Windows PowerShell y el cmdlet New-CsTestDevice.</span><span class="sxs-lookup"><span data-stu-id="8c773-123">Test devices can be created by using Windows PowerShell and the New-CsTestDevice cmdlet.</span></span> <span data-ttu-id="8c773-124">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c773-124">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="8c773-125">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="8c773-125">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<span data-ttu-id="8c773-126">Al crear dispositivos de prueba con este cmdlet, debe hacer dos cosas:</span><span class="sxs-lookup"><span data-stu-id="8c773-126">When creating test devices using this cmdlet, you must do two things:</span></span>

  - <span data-ttu-id="8c773-127">Especifique MACAddress o SerialNumber como IdentifierType.</span><span class="sxs-lookup"><span data-stu-id="8c773-127">Specify either MACAddress or SerialNumber as the IdentifierType.</span></span>

  - <span data-ttu-id="8c773-128">Incluir el ámbito al especificar la identidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c773-128">Include the scope when specifying the device Identity.</span></span> <span data-ttu-id="8c773-129">Para crear un nuevo dispositivo en el ámbito global use una sintaxis similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="8c773-129">To create a new device at the global scope use syntax similar to this:</span></span>
    
        -Identity "global/WindowsPhone"
    
    <span data-ttu-id="8c773-130">Para crear un dispositivo de prueba en el ámbito de sitio, use una sintaxis similar a esta:</span><span class="sxs-lookup"><span data-stu-id="8c773-130">To create a test device at the site scope use syntax similar to this:</span></span>
    
        -Identity "site:Redmond/WindowsPhone"

<div>

## <a name="to-create-a-test-device-by-using-the-mac-address"></a><span data-ttu-id="8c773-131">Para crear un dispositivo de prueba con la dirección MAC</span><span class="sxs-lookup"><span data-stu-id="8c773-131">To create a test device by using the MAC address</span></span>

  - <span data-ttu-id="8c773-132">Este comando crea un dispositivo de prueba en el ámbito global y usa la dirección MAC como IdentifierType:</span><span class="sxs-lookup"><span data-stu-id="8c773-132">This command creates a test device at the global scope, and using the MAC address as the IdentifierType:</span></span>
    
        New-CsTestDevice -Identity "global/WindowsPhone" -IdentifierType "MACAddress" -Identifier "01:02:03:04:05:06"

</div>

<div>

## <a name="to-create-a-test-device-by-using-the-serial-number"></a><span data-ttu-id="8c773-133">Para crear un dispositivo de prueba con el número de serie</span><span class="sxs-lookup"><span data-stu-id="8c773-133">To create a test device by using the serial number</span></span>

  - <span data-ttu-id="8c773-134">Este comando crea un nuevo dispositivo de prueba en el ámbito del sitio (para el sitio de Redmond) y usa el número de serie como IdentifierType:</span><span class="sxs-lookup"><span data-stu-id="8c773-134">This command creates a new test device at the site scope (for the Redmond site) and uses the serial number as the IdentifierType:</span></span>
    
        New-CsTestDevice -Identity "site:Redmond/WindowsPhone" -IdentifierType "SerialNumber" -Identifier "01ABC5419JKR55T"

</div>

<span data-ttu-id="8c773-135">Para obtener más información, vea el tema de ayuda sobre el cmdlet [New-CsTestDevice](https://docs.microsoft.com/powershell/module/skype/New-CsTestDevice) .</span><span class="sxs-lookup"><span data-stu-id="8c773-135">For more information, see the help topic for the [New-CsTestDevice](https://docs.microsoft.com/powershell/module/skype/New-CsTestDevice) cmdlet.</span></span>

<span data-ttu-id="8c773-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c773-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

