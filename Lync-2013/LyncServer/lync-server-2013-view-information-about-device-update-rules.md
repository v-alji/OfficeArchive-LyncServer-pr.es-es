---
title: 'Lync Server 2013: ver información sobre las reglas de actualización de dispositivos'
description: 'Lync Server 2013: ver información sobre las reglas de actualización de dispositivos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View information about Device Update rules
ms:assetid: d6677ca4-024b-4816-8511-8d7630788107
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994077(v=OCS.15)
ms:contentKeyID: 51803988
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4aecfd0dd778b576ea4a672e550f9e27d7ca463e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446300"
---
# <a name="view-information-about-device-update-rules-in-lync-server-2013"></a><span data-ttu-id="7075c-103">Ver información sobre las reglas de actualización de dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7075c-103">View information about Device Update rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7075c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7075c-104">

<span> </span></span></span>

<span data-ttu-id="7075c-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="7075c-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="7075c-106">Ver detalles sobre las reglas de actualización de dispositivos que ya se han importado, incluido el tipo, modelo y la marca de los dispositivos a los que se aplica la actualización; la versión y el tipo de actualización; y la configuración regional y de grupo para la actualización.</span><span class="sxs-lookup"><span data-stu-id="7075c-106">View details about device update rules that have already been imported, including the type, model, and brand of devices the update applies to; version and type of update; and locale and pool for the update.</span></span> <span data-ttu-id="7075c-107">La información está disponible para todas las reglas importadas de actualización de dispositivos: las que están pendientes de aprobación, las que se han implementado (aprobadas), las que se han recuperado y las que ha decidido no usar (restablecer).</span><span class="sxs-lookup"><span data-stu-id="7075c-107">Information is available for all imported device update rules—those that are pending approval, deployed (approved), recalled (restored), and those you’ve decided not to use (reset).</span></span> <span data-ttu-id="7075c-108">Obtenga acceso a esta información en el panel de control de Lync Server o en Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7075c-108">Access this information from either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7075c-109">Para obtener más información sobre cómo importar, aprobar, restablecer, restaurar y quitar reglas, consulte los temas que aparecen en las <A href="lync-server-2013-device-update-rules.md">reglas de actualización de dispositivos en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7075c-109">For details about how to import, approve, reset, restore, and remove rules, see the topics listed at <A href="lync-server-2013-device-update-rules.md">Device Update rules in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-view-device-update-rules-by-using-lync-server-control-panel"></a><span data-ttu-id="7075c-110">Para ver las reglas de actualización de dispositivos mediante el panel de control de Lync Server</span><span class="sxs-lookup"><span data-stu-id="7075c-110">To view device update rules by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="7075c-111">Desde una cuenta de usuario que se asigne al rol CsUserAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="7075c-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7075c-112">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7075c-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7075c-113">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7075c-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7075c-114">En la barra de navegación izquierda, haga clic en **clientes** y, a continuación, haga clic en el botón de navegación de **actualización de dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="7075c-114">In the left navigation bar, click **Clients**, and then click the **Device Update** navigation button.</span></span> <span data-ttu-id="7075c-115">Las reglas importadas se muestran en la página de **actualización del dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="7075c-115">Imported rules are listed on the **Device Update** page.</span></span>

</div>

<div>

## <a name="viewing-device-update-rules-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="7075c-116">Visualización de las reglas de actualización de dispositivos mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7075c-116">Viewing Device Update Rules by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="7075c-117">La información detallada sobre todas las reglas de actualización de dispositivos también se puede ver con Windows PowerShell y el cmdlet **Get-CsDeviceUpdateRule** .</span><span class="sxs-lookup"><span data-stu-id="7075c-117">Detailed information about all your device update rules can also be viewed by using Windows PowerShell and the **Get-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="7075c-118">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7075c-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7075c-119">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="7075c-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>

## <a name="to-view-all-your-device-update-rules"></a><span data-ttu-id="7075c-120">Para ver todas las reglas de actualización de dispositivos</span><span class="sxs-lookup"><span data-stu-id="7075c-120">To view all your device update rules</span></span>

  - <span data-ttu-id="7075c-121">El siguiente comando devuelve información acerca de todas las reglas de actualización de dispositivos configuradas para su uso en su organización:</span><span class="sxs-lookup"><span data-stu-id="7075c-121">The following command returns information about all the device updates rules configured for use in your organization:</span></span>
    
        Get-CsDeviceUpdateRule
    
    <span data-ttu-id="7075c-122">El comando devuelve información similar a la siguiente para cada una de las reglas de actualización de su dispositivo:</span><span class="sxs-lookup"><span data-stu-id="7075c-122">The command returns information similar to the following for each of your device update rules:</span></span>
    
        Identity        : Service:WebServer:pool0.vdomain.com/2de8cbf6-9441-4f61-b755-1e4bef1effde
        Id              : 2de8cbf6-9441-4f61-b755-1e4bef1effde
        DeviceType      : UCPhone
        Brand           : Microsoft
        Model           : CPE
        Revision        : A
        Locale          : ENU
        UpdateType      : CPE
        ApprovedVersion :
        RestoreVersion  :
        PendingVersion  : 4.0.7577.4066

</div>

<div>

## <a name="to-view-all-the-device-update-rules-on-a-specific-web-server"></a><span data-ttu-id="7075c-123">Para ver todas las reglas de actualización de dispositivos en un servidor Web específico</span><span class="sxs-lookup"><span data-stu-id="7075c-123">To view all the device update rules on a specific web server</span></span>

  - <span data-ttu-id="7075c-124">Para ver las reglas de actualización de dispositivos en un equipo específico, use el parámetro filter seguido de la identidad del servidor y el carácter comodín ( \* ).</span><span class="sxs-lookup"><span data-stu-id="7075c-124">To view the device update rules on a specific computer, use the Filter parameter followed by the server Identity and the wildcard character (\*).</span></span> <span data-ttu-id="7075c-125">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7075c-125">For example:</span></span>
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*"

</div>

<span data-ttu-id="7075c-126">Para obtener más información, vea el tema de ayuda sobre el cmdlet [Get-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Get-CsDeviceUpdateRule) .</span><span class="sxs-lookup"><span data-stu-id="7075c-126">For details, see the Help topic for the [Get-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Get-CsDeviceUpdateRule) cmdlet.</span></span>

<span data-ttu-id="7075c-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7075c-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

