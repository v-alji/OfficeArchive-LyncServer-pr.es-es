---
title: 'Lync Server 2013: ver actualizaciones de software para dispositivos de su organización'
description: 'Lync Server 2013: vea las actualizaciones de software para los dispositivos de su organización.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View software updates for devices in your organization
ms:assetid: d2cca12b-ed43-4e1f-90ab-d14bca8b482c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182592(v=OCS.15)
ms:contentKeyID: 48185418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 833ab25315847b760271c63bbfca3ba8357e41c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399210"
---
# <a name="view-software-updates-for-devices-in-lync-server-2013"></a><span data-ttu-id="0981f-103">Ver actualizaciones de software para dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0981f-103">View software updates for devices in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0981f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0981f-104">

<span> </span></span></span>

<span data-ttu-id="0981f-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0981f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0981f-106">Con Lync Server 2013, puede usar el servicio Web de actualización de dispositivos para ver y administrar las actualizaciones de software para los dispositivos de su organización.</span><span class="sxs-lookup"><span data-stu-id="0981f-106">With Lync Server 2013, you use Device Update Web service to view and manage software updates for your organization’s devices.</span></span> <span data-ttu-id="0981f-107">Estas actualizaciones están disponibles en archivos. cab (Cabinet) del sitio web de soporte técnico de Microsoft en [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) .</span><span class="sxs-lookup"><span data-stu-id="0981f-107">These updates are available in .cab (cabinet) files from the Microsoft Support website at [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091).</span></span> <span data-ttu-id="0981f-108">Una vez que haya descargado el archivo. cab, ejecute el cmdlet **Import-CSDeviceUpdate** para importar las reglas de actualización del dispositivo desde el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="0981f-108">After you download the .cab file, run the **Import-CSDeviceUpdate** cmdlet to import the device update rules from the .cab file.</span></span> <span data-ttu-id="0981f-109">Para obtener más información sobre el cmdlet **Import-CSDeviceUpdate** , consulte [Import-CSDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) en la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0981f-109">For details about the **Import-CSDeviceUpdate** cmdlet, see [Import-CsDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) in the Lync Server Management Shell documentation.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="0981f-110">Antes de implementar una nueva actualización de su organización, compruebe que funciona correctamente en un dispositivo de prueba.</span><span class="sxs-lookup"><span data-stu-id="0981f-110">Before deploying a new update to your organization, verify that it functions correctly on a test device.</span></span>



</div>

<div>

## <a name="to-view-software-updates-for-uc-devices"></a><span data-ttu-id="0981f-111">Para ver las actualizaciones de software para los dispositivos de comunicaciones unificadas</span><span class="sxs-lookup"><span data-stu-id="0981f-111">To view software updates for UC devices</span></span>

1.  <span data-ttu-id="0981f-112">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="0981f-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0981f-113">En el sitio web de soporte técnico de Microsoft [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) , descargue el archivo. cab en una ubicación en un equipo de Lync Server 2013 (por ejemplo, las actualizaciones de C: \\ \\UCUpdates.cab).</span><span class="sxs-lookup"><span data-stu-id="0981f-113">From the Microsoft Support website at [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091), download the .cab file to a location on a Lync Server 2013 computer (for example, C:\\Updates\\UCUpdates.cab).</span></span>

3.  <span data-ttu-id="0981f-114">Importar las reglas de actualización de dispositivos del archivo C: \\ updates \\UCUpdates.cab mediante la ejecución de uno de los siguientes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0981f-114">Import the device update rules from the C:\\Updates\\UCUpdates.cab file by running one of the following cmdlets:</span></span>
    
      - <span data-ttu-id="0981f-115">Si el archivo. cab se encuentra en el mismo equipo que el que está ejecutando el servicio que se va a actualizar (servicio: Redmond-websvc-2), ejecute el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0981f-115">If the .cab file is located on the same computer as the one running the service to be updated (service:Redmond-websvc-2), run the following cmdlet:</span></span>
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-2 -FileName C:\Updates\UCUpdates.cab
    
      - <span data-ttu-id="0981f-116">Si el archivo. cab se encuentra en un equipo diferente del que está ejecutando el servicio que se va a actualizar (servicio: Redmond-websvc-3), ejecute el siguiente cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0981f-116">If the .cab file is located on a different computer than the one running the service to be updated (service:Redmond-websvc-3), run the following cmdlet:</span></span>
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-3 -ByteInput C:\Updates\UCUpdates.cab

4.  <span data-ttu-id="0981f-117">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0981f-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0981f-118">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0981f-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

5.  <span data-ttu-id="0981f-119">En la barra de navegación izquierda, haga clic en **clientes** y, a continuación, en **actualización de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="0981f-119">In the left navigation bar, click **Clients**, and then click **Device Update**.</span></span>

6.  <span data-ttu-id="0981f-120">En la página **actualización de dispositivo** , haga clic en una actualización de la lista y, a continuación, siga uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="0981f-120">On the **Device Update** page, click an update in the list, and then do one of the following:</span></span>
    
      - <span data-ttu-id="0981f-121">**Cancelar una actualización pendiente.**</span><span class="sxs-lookup"><span data-stu-id="0981f-121">**Cancel a pending update.**</span></span> <span data-ttu-id="0981f-122">Para evitar que la actualización seleccionada se implemente en los dispositivos de su organización, haga clic en el menú **acción** y, a continuación, haga clic en **Cancelar actualizaciones pendientes**.</span><span class="sxs-lookup"><span data-stu-id="0981f-122">To prevent the selected update from being deployed to your organization’s devices, click the **Action** menu, and then click **Cancel pending updates**.</span></span>
    
      - <span data-ttu-id="0981f-123">**Aprobar una actualización.**</span><span class="sxs-lookup"><span data-stu-id="0981f-123">**Approve an update.**</span></span> <span data-ttu-id="0981f-124">Para permitir que la actualización seleccionada se implemente en los dispositivos de su organización, haga clic en el menú **acción** y, a continuación, haga clic en **aprobar**.</span><span class="sxs-lookup"><span data-stu-id="0981f-124">To allow the selected update to be deployed to your organization’s devices, click the **Action** menu, and then click **Approve**.</span></span>
    
      - <span data-ttu-id="0981f-125">**Restaurar una actualización.**</span><span class="sxs-lookup"><span data-stu-id="0981f-125">**Restore an update.**</span></span> <span data-ttu-id="0981f-126">Para permitir que se implemente una actualización aprobada previamente en los dispositivos de su organización, haga clic en el menú **acción** y, a continuación, haga clic en **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="0981f-126">To allow a previously approved update to be deployed to your organization’s devices, click the **Action** menu, and then click **Restore**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0981f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0981f-127">See Also</span></span>


[<span data-ttu-id="0981f-128">Administrar dispositivos, teléfonos y aplicaciones cliente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0981f-128">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="0981f-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0981f-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

