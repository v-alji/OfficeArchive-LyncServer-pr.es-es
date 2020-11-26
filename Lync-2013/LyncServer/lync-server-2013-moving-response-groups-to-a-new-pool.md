---
title: 'Lync Server 2013: mover grupos de respuesta a un grupo nuevo'
description: 'Lync Server 2013: mover grupos de respuesta a un grupo nuevo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Moving response groups to a new pool
ms:assetid: da0db765-41e5-430b-b5a7-5418ec5ff2a7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205298(v=OCS.15)
ms:contentKeyID: 48185538
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b696963a28abbcd258f53fae12c3e281efa6ae4d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425269"
---
# <a name="moving-response-groups-to-a-new-pool-in-lync-server-2013"></a><span data-ttu-id="76ee0-103">Mover grupos de respuesta a un grupo nuevo en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76ee0-103">Moving response groups to a new pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76ee0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76ee0-104">

<span> </span></span></span>

<span data-ttu-id="76ee0-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="76ee0-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="76ee0-106">Lync Server 2013 introduce nuevos cmdlets que permiten mover grupos de respuesta de un grupo a otro, incluso cuando el nombre de dominio completo (FQDN) es diferente.</span><span class="sxs-lookup"><span data-stu-id="76ee0-106">Lync Server 2013 introduces new cmdlet support for moving response groups from one pool to another pool, even when the fully qualified domain name (FQDN) is different.</span></span>

<span data-ttu-id="76ee0-107">Siga los pasos que se indican en el siguiente procedimiento para mover grupos de respuesta de un grupo de servidores front-end a otro grupo de servidores front-end con un FQDN diferente.</span><span class="sxs-lookup"><span data-stu-id="76ee0-107">Use the steps in the following procedure to move response groups from one Front End pool to another Front End pool with a different FQDN.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="76ee0-108">En un entorno de coexistencia, solo puede mover grupos de respuesta entre &nbsp; grupos front-end de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="76ee0-108">In a coexistence environment, you can move response groups only between Lync Server 2013&nbsp;Front End pools.</span></span>



</div>

<div>

## <a name="to-move-response-groups-to-a-pool-with-a-different-fqdn"></a><span data-ttu-id="76ee0-109">Para mover grupos de respuesta a un grupo con un FQDN diferente</span><span class="sxs-lookup"><span data-stu-id="76ee0-109">To move response groups to a pool with a different FQDN</span></span>

1.  <span data-ttu-id="76ee0-110">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="76ee0-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="76ee0-111">Exporte los grupos de respuesta en el grupo de origen.</span><span class="sxs-lookup"><span data-stu-id="76ee0-111">Export the response groups in the source pool.</span></span> <span data-ttu-id="76ee0-112">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="76ee0-112">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<source FQDN>" -FileName "<export file name>"
    
    <span data-ttu-id="76ee0-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76ee0-113">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:source.contoso.com" -FileName "C:\RgsExportSource.zip"
    
    <span data-ttu-id="76ee0-114">Para quitar los grupos de respuesta del grupo de origen durante la exportación, incluya el parámetro – RemoveExportedConfiguration.</span><span class="sxs-lookup"><span data-stu-id="76ee0-114">To remove the response groups from the source pool during the export, include the –RemoveExportedConfiguration parameter.</span></span> <span data-ttu-id="76ee0-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76ee0-115">For example:</span></span>
    
        Export-CsRgsConfiguration -Source ApplicationServer:source.contoso.com -FileName "C:\RgsExportSource.zip" -RemoveExportedConfiguration

3.  <span data-ttu-id="76ee0-116">Importe los grupos de respuesta al grupo de destino y asigne el grupo de destino como nuevo propietario.</span><span class="sxs-lookup"><span data-stu-id="76ee0-116">Import the response groups to the destination pool and assign the destination pool as the new owner.</span></span> <span data-ttu-id="76ee0-117">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="76ee0-117">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<destination pool>" -FileName "<export file name>" -OverwriteOwner
    
    <span data-ttu-id="76ee0-118">Si también desea copiar la configuración del nivel de aplicación del grupo de respuesta del grupo de origen al grupo de destino, incluya el parámetro – ReplaceExistingRgsSettings.</span><span class="sxs-lookup"><span data-stu-id="76ee0-118">If you also want to copy the Response Group application-level settings from the source pool to the destination pool, include the –ReplaceExistingRgsSettings parameter.</span></span> <span data-ttu-id="76ee0-119">Solo puede definir un conjunto de opciones de configuración de la aplicación por grupo.</span><span class="sxs-lookup"><span data-stu-id="76ee0-119">You can define only one set of application-level settings per pool.</span></span> <span data-ttu-id="76ee0-120">Si copia la configuración de nivel de aplicación del grupo de origen en el grupo de destino, la configuración del grupo de origen reemplaza la configuración del grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="76ee0-120">If you copy the application-level settings from the source pool to the destination pool, the settings from the source pool replace the settings for the destination pool.</span></span> <span data-ttu-id="76ee0-121">Si no copia la configuración de nivel de aplicación del grupo de origen, la configuración existente del grupo de destino se aplicará a los grupos de respuesta importados.</span><span class="sxs-lookup"><span data-stu-id="76ee0-121">If you do not copy the application-level settings from the source pool, the existing settings from the destination pool apply to the imported response groups.</span></span>
    
    <span data-ttu-id="76ee0-122">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76ee0-122">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:destination.contoso.com" -FileName "C:\RgsExportSource.zip" -OverwriteOwner -ReplaceExistingRgsSettings
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="76ee0-123">La configuración de nivel de aplicación incluye la configuración predeterminada de música en espera, el archivo de audio de música activada predeterminada, el período de gracia de timbre de timbre y la configuración de contexto de llamada.</span><span class="sxs-lookup"><span data-stu-id="76ee0-123">Application-level settings include the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span> <span data-ttu-id="76ee0-124">Para ver estas opciones de configuración, ejecute el cmdlet <STRONG>Get-CsRgsConfiguration</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="76ee0-124">To view these configuration settings, run the <STRONG>Get-CsRgsConfiguration</STRONG> cmdlet.</span></span> <span data-ttu-id="76ee0-125">Para obtener más información sobre este cmdlet, vea <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration">Get-CsRgsConfiguration</A>.</span><span class="sxs-lookup"><span data-stu-id="76ee0-125">For details about this cmdlet, see <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration">Get-CsRgsConfiguration</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="76ee0-126">Para comprobar que la importación se ha realizado correctamente, muestre la configuración del grupo de respuesta importado de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="76ee0-126">Verify that the import was successful by displaying the imported response group configuration by doing the following:</span></span>
    
      - <span data-ttu-id="76ee0-127">Compruebe que se importaron todos los flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="76ee0-127">Verify that all the workflows were imported.</span></span> <span data-ttu-id="76ee0-128">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="76ee0-128">At the command line, type the following:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<destination pool FQDN>"
    
      - <span data-ttu-id="76ee0-129">Compruebe que se han importado todas las colas.</span><span class="sxs-lookup"><span data-stu-id="76ee0-129">Verify that all the queues were imported.</span></span> <span data-ttu-id="76ee0-130">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="76ee0-130">At the command line, type the following:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<destination pool FQDN>"
    
      - <span data-ttu-id="76ee0-131">Verifique que se hayan importado todos los grupos de agentes.</span><span class="sxs-lookup"><span data-stu-id="76ee0-131">Verify that all the agent groups were imported.</span></span> <span data-ttu-id="76ee0-132">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="76ee0-132">At the command line, type the following:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<destination pool FQDN>"
    
      - <span data-ttu-id="76ee0-133">Verifique que se hayan importado todas las horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="76ee0-133">Verify that all the hours of business were imported.</span></span> <span data-ttu-id="76ee0-134">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="76ee0-134">At the command line, type the following:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<destination pool FQDN>" 
    
      - <span data-ttu-id="76ee0-135">Verifique que se hayan importado todos los conjuntos de días festivos.</span><span class="sxs-lookup"><span data-stu-id="76ee0-135">Verify that all the holiday sets were imported.</span></span> <span data-ttu-id="76ee0-136">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="76ee0-136">At the command line, type the following:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<destination pool FQDN>" 

5.  <span data-ttu-id="76ee0-137">Verifique que la importación se haya realizado correctamente colocando una llamada a uno de los grupos de respuesta y verificando que la llamada se controla correctamente.</span><span class="sxs-lookup"><span data-stu-id="76ee0-137">Verify that the import was successful by placing a call to one of the response groups and verifying that the call is handled correctly.</span></span>

6.  <span data-ttu-id="76ee0-138">Solicitar agentes que sean miembros de grupos de agentes formales para iniciar sesión en sus grupos de agentes en el grupo de servidores de destino.</span><span class="sxs-lookup"><span data-stu-id="76ee0-138">Request agents who are members of formal agent groups to sign in to their agent groups in the destination pool.</span></span>

7.  <span data-ttu-id="76ee0-139">Si no ha quitado previamente grupos de respuesta del grupo de origen, quite los grupos de respuesta del grupo de origen.</span><span class="sxs-lookup"><span data-stu-id="76ee0-139">If you did not previously remove response groups from the source pool, remove the response groups from the source pool.</span></span> <span data-ttu-id="76ee0-140">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="76ee0-140">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<source pool FQDN> -RemoveExportedConfiguration -FileName "<temporary export file name>"
    
    <span data-ttu-id="76ee0-141">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76ee0-141">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:source.contoso.com" -RemoveExportedConfiguration -FileName "C:\TempRGsConfiguration.zip"

<span data-ttu-id="76ee0-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76ee0-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

