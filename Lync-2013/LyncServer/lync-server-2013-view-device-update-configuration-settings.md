---
title: 'Lync Server 2013: Ver las opciones de configuración de la actualización de dispositivos'
description: 'Lync Server 2013: ver la configuración de la actualización de dispositivos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Device Update configuration settings
ms:assetid: aa6a70a9-bd77-4606-b797-ea6a3bab9cf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994059(v=OCS.15)
ms:contentKeyID: 51803970
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e686562d99da679149b6b977bd3cb9feb5c9a7fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443352"
---
# <a name="view-device-update-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="adfda-103">Ver las opciones de configuración de la actualización de dispositivos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="adfda-103">View Device Update configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="adfda-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="adfda-104">

<span> </span></span></span>

<span data-ttu-id="adfda-105">_**Última modificación del tema:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="adfda-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="adfda-106">Puede ver las opciones de configuración del servicio de actualización de dispositivos mediante el shell de administración de Lync Server y el cmdlet **Get-CsDeviceUpdateConfiguration** , que puede ejecutar desde el shell de administración de lync Server 2013 o desde una sesión remota de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="adfda-106">You can view the Device Update Service configuration settings by using Lync Server Management Shell and the **Get-CsDeviceUpdateConfiguration** cmdlet, which you can run from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="adfda-107">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="adfda-107">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>


  - <span data-ttu-id="adfda-108">Para ver información sobre todas las rutas de voz, escriba el siguiente comando en el shell de administración de Lync Server y presione ENTRAR:</span><span class="sxs-lookup"><span data-stu-id="adfda-108">To view information about all your voice routes, type the following command in the Lync Server Management Shell and press Enter:</span></span>
    
        Get-CsDeviceUpdateConfiguration
    
    <span data-ttu-id="adfda-109">Este comando devolverá información similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="adfda-109">This command returns information similar to the following:</span></span>
    
        Identity               : Global
        ValidLogFileTypes      : {Watson, Config, Diaglog, CELog}
        ValidLogFileExtensions : {.dmp, .clg, .clg1, .clg2...}
        MaxLogFileSize         : 1024000
        MaxLogCacheLimit       : 512000
        LogCleanUpInterval     : 10.00:00:00
        LogFlushInterval       : 00:05:00
        LogCleanUpTimeOfDay    :

</div>

<span data-ttu-id="adfda-110">Para obtener más información sobre este cmdlet, consulte el tema de ayuda en [obtener-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsDeviceUpdateConfiguration).</span><span class="sxs-lookup"><span data-stu-id="adfda-110">For details about this cmdlet, see Help topic at [Get-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsDeviceUpdateConfiguration).</span></span>

<span data-ttu-id="adfda-111"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="adfda-111"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

