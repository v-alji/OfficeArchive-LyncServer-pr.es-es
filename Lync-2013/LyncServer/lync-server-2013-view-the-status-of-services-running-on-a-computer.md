---
title: 'Lync Server 2013: ver el estado de los servicios que se ejecutan en un equipo'
description: 'Lync Server 2013: ver el estado de los servicios que se ejecutan en un equipo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View the status of services running on a computer
ms:assetid: f41918e7-4c02-431e-840a-88a1f36ae499
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182606(v=OCS.15)
ms:contentKeyID: 48185804
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22aeb13f2beb5d3b0ee5eec8109eceeb14e40213
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399198"
---
# <a name="view-the-status-of-services-running-on-a-computer-in-lync-server-2013"></a><span data-ttu-id="fb2b6-103">Ver el estado de los servicios que se ejecutan en un equipo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb2b6-103">View the status of services running on a computer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb2b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb2b6-104">

<span> </span></span></span>

<span data-ttu-id="fb2b6-105">_**Última modificación del tema:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="fb2b6-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="fb2b6-106">Puede usar el panel de control de Lync Server 2013 para ver todos los servicios que se están ejecutando en un equipo específico de su topología de Lync Server y ver el estado de cada servicio.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-106">You can use Lync Server 2013 Control Panel to view all the services that are running on a specific computer in your Lync Server topology and see the status of each service.</span></span>

<div>

## <a name="to-view-the-status-of-services-running-on-a-computer"></a><span data-ttu-id="fb2b6-107">Para ver el estado de los servicios que se ejecutan en un equipo</span><span class="sxs-lookup"><span data-stu-id="fb2b6-107">To view the status of services running on a computer</span></span>

1.  <span data-ttu-id="fb2b6-108">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fb2b6-109">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="fb2b6-110">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fb2b6-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="fb2b6-111">En la barra de navegación izquierda, haga clic en **topología**.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-111">In the left navigation bar, click **Topology**.</span></span>

4.  <span data-ttu-id="fb2b6-112">En la página **Estado** , ordene o busque la lista, según sea necesario, para buscar el equipo que le interesa y, a continuación, haga clic en el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-112">On the **Status** page, sort or search the list, as required, to find the computer you’re interested in, and then click the computer name.</span></span>

5.  <span data-ttu-id="fb2b6-113">Siga uno de estos pasos:</span><span class="sxs-lookup"><span data-stu-id="fb2b6-113">Do any of the following:</span></span>
    
      - <span data-ttu-id="fb2b6-114">Para ver el estado más reciente de los servicios que se ejecutan en el equipo, haga clic en **obtener estado del servicio**.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-114">To see the latest status of services running on the computer, click **Get service status**.</span></span>
    
      - <span data-ttu-id="fb2b6-115">Para ver una lista de los servicios específicos que se ejecutan en el equipo y el estado de cada servicio, haga clic en **propiedades** y, a continuación, haga clic en **cerrar** para volver a la lista.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-115">To see a list of specific services running on the computer and the status of each service, click **Properties**, and then click **Close** to return to the list.</span></span>

</div>

<div>

## <a name="viewing-service-status-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="fb2b6-116">Ver el estado del servicio con cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb2b6-116">Viewing Service Status by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="fb2b6-117">También puede ver el estado del servicio con Windows PowerShell y el cmdlet **Get-CsWindowsService** .</span><span class="sxs-lookup"><span data-stu-id="fb2b6-117">You can also view service status by using Windows PowerShell and the **Get-CsWindowsService** cmdlet.</span></span> <span data-ttu-id="fb2b6-118">Puede ejecutar este cmdlet desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-118">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="fb2b6-119">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="fb2b6-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-service-status"></a><span data-ttu-id="fb2b6-120">Para ver el estado del servicio</span><span class="sxs-lookup"><span data-stu-id="fb2b6-120">To view service status</span></span>

  - <span data-ttu-id="fb2b6-121">Para ver el estado del servicio en un equipo, escriba un comando similar al siguiente en el shell de administración de Lync Server y, a continuación, presione ENTRAR:</span><span class="sxs-lookup"><span data-stu-id="fb2b6-121">To view service status on a computer, type a command similar to the following in the Lync Server Management Shell and then press Enter:</span></span>
    
        Get-CsWindowsService -ComputerName atl-cs-001.litwareinc.com | Select-Object RoleName, Status
    
    <span data-ttu-id="fb2b6-122">Este comando devolverá información similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb2b6-122">This command returns information similar to the following:</span></span>
    
        RoleName                                  Status
        --------                                  ------
        {W3SVC}                                   Running
        {CentralManagement}                       Running
        {ClsAgent}                                Running
        {Registrar, UserServer, EdgeServer}       Running
        {ApplicationServer}                       Running
        {ConferencingServer}                      Running
        {MediationServer}                         Running

</div>

<span data-ttu-id="fb2b6-123">Para obtener más información, vea [Get-CsWindowsService](https://docs.microsoft.com/powershell/module/skype/Get-CsWindowsService).</span><span class="sxs-lookup"><span data-stu-id="fb2b6-123">For details, see [Get-CsWindowsService](https://docs.microsoft.com/powershell/module/skype/Get-CsWindowsService).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fb2b6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb2b6-124">See Also</span></span>


[<span data-ttu-id="fb2b6-125">Administrar dispositivos, teléfonos y aplicaciones cliente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb2b6-125">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="fb2b6-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb2b6-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

