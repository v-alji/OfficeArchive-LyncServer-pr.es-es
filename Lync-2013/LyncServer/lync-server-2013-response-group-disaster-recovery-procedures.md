---
title: 'Lync Server 2013: Procedimientos de recuperación ante desastres del grupo de respuesta'
description: Procedimientos de recuperación ante desastres del grupo de respuesta 2013 de Lync Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group disaster recovery procedures
ms:assetid: b49577b7-0ca3-4f20-b614-f3a2a0046b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205186(v=OCS.15)
ms:contentKeyID: 48185171
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9021fb75c8f937bfd298578a9241d6256d26d85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436303"
---
# <a name="response-group-disaster-recovery-procedures-in-lync-server-2013"></a><span data-ttu-id="0ecfb-103">Procedimientos de recuperación ante desastres del grupo de respuesta en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ecfb-103">Response group disaster recovery procedures in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ecfb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ecfb-104">

<span> </span></span></span>

<span data-ttu-id="0ecfb-105">_**Última modificación del tema:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0ecfb-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0ecfb-106">Durante la fase de conmutación por error de recuperación ante desastres, los grupos de respuesta residen en varios grupos: en el grupo primario (que no está disponible) y en el grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-106">During the failover phase of disaster recovery, the response groups reside in multiple pools: in the primary pool (which is unavailable) and in the backup pool.</span></span> <span data-ttu-id="0ecfb-107">Los grupos de respuesta de ambos grupos tienen el mismo nombre y el mismo propietario (el grupo principal), pero tienen diferentes padres.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-107">The response groups in both pools have the same name and the same owner (the primary pool), but they have different parents.</span></span> <span data-ttu-id="0ecfb-108">Durante este tiempo, los cmdlets del grupo de respuesta funcionan de manera algo diferente.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-108">During this time, Response Group cmdlets work a little differently.</span></span> <span data-ttu-id="0ecfb-109">Asegúrese de usar parámetros según se especifica en el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-109">Be sure to use parameters as specified in the following procedure.</span></span> <span data-ttu-id="0ecfb-110">Para más información sobre cómo funcionan los cmdlets durante la fase de conmutación por error, vea el artículo del blog de NextHop "Lync Server 2013: recuperación de grupos de respuesta durante la recuperación ante desastres" en [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957) .</span><span class="sxs-lookup"><span data-stu-id="0ecfb-110">For details about how cmdlets work during the failover phase, see NextHop blog article "Lync Server 2013: Recovering Response Groups During Disaster Recovery" at [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957).</span></span> <span data-ttu-id="0ecfb-111">Este artículo del blog también se aplica a la versión de lanzamiento de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-111">This blog article also applies to the released version of Lync Server 2013.</span></span>

<span data-ttu-id="0ecfb-112">Siga los pasos que se indican en el siguiente procedimiento para preparar y realizar la recuperación de desastres para el servicio de grupo de respuesta de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-112">Use the steps in the following procedure to prepare for and perform disaster recovery for Lync Server Response Group service.</span></span>

<div>

## <a name="to-fail-over-and-fail-back-response-group"></a><span data-ttu-id="0ecfb-113">Para deshacer la conmutación por error y el grupo de respuesta failback</span><span class="sxs-lookup"><span data-stu-id="0ecfb-113">To fail over and fail back Response Group</span></span>

1.  <span data-ttu-id="0ecfb-114">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="0ecfb-115">Realizar copias de seguridad rutinariamente.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-115">Routinely perform backups.</span></span> <span data-ttu-id="0ecfb-116">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-116">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="0ecfb-117">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-117">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimary.zip"

3.  <span data-ttu-id="0ecfb-118">Durante una interrupción, después de la conmutación por error en el grupo de copias de seguridad, importe los grupos de respuesta al grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-118">During an outage, after failover to the backup pool, import the response groups to the backup pool.</span></span> <span data-ttu-id="0ecfb-119">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-119">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<backup pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="0ecfb-120">Si desea reemplazar la configuración de nivel de aplicación del grupo de copias de seguridad por la configuración del grupo principal, incluya el parámetro – ReplaceExistingSettings.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-120">If you want to replace the application-level settings in the backup pool with the settings from the primary pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="0ecfb-121">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-121">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:backup.contoso.com" -FileName "C:\RgsExportPrimary.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="0ecfb-122">Si no reemplaza la configuración del grupo de copias de seguridad y no se puede recuperar el repositorio principal, se perderá la configuración de la agrupación principal.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-122">If you do not replace the settings in the backup pool and the primary pool can't be recovered, the primary pool settings will be lost.</span></span> <span data-ttu-id="0ecfb-123">Para obtener más información, consulte <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">planeación de la recuperación ante desastres de grupos de respuesta en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-123">For details, see <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">Planning for response group disaster recovery in Lync Server 2013</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="0ecfb-124">Compruebe que la importación se ha realizado correctamente; para ello, muestra los grupos de respuesta importados.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-124">Verify that the import was successful by displaying the imported response groups.</span></span> <span data-ttu-id="0ecfb-125">Los grupos de respuesta importados siguen siendo propiedad del grupo primario.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-125">The imported response groups are still owned by the primary pool.</span></span> <span data-ttu-id="0ecfb-126">Haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-126">Do the following:</span></span>
    
      - <span data-ttu-id="0ecfb-127">Mostrar todos los flujos de trabajo del grupo de copias de seguridad que pertenecen al grupo principal y comprobar que se incluyen todos los flujos de trabajo de grupo primario.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-127">Display all the workflows in the backup pool that are owned by the primary pool, and verify that all the primary pool workflows are included.</span></span> <span data-ttu-id="0ecfb-128">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-128">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0ecfb-129">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-129">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com"
    
      - <span data-ttu-id="0ecfb-130">Muestre todas las colas del grupo de copia de seguridad que pertenecen al grupo principal y compruebe que se incluyen todas las colas de grupo principales.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-130">Display all the queues in the backup pool that are owned by the primary pool, and verify that all the primary pool queues are included.</span></span> <span data-ttu-id="0ecfb-131">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-131">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0ecfb-132">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-132">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="0ecfb-133">Mostrar todos los grupos de agentes del grupo de copias de seguridad que pertenecen al grupo principal y comprobar que se incluyen todos los grupos de agentes de grupo principales.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-133">Display all the agent groups in the backup pool that are owned by the primary pool, and verify that all the primary pool agent groups are included.</span></span> <span data-ttu-id="0ecfb-134">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-134">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0ecfb-135">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-135">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="0ecfb-136">Mostrar todas las horas de actividad en el grupo de copia de seguridad que pertenecen al grupo principal y comprobar que se incluyen todos los horarios de negocio principales de la agrupación.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-136">Display all the hours of business in the backup pool that are owned by the primary pool, and verify that all the primary pool hours of business are included.</span></span> <span data-ttu-id="0ecfb-137">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-137">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0ecfb-138">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-138">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="0ecfb-139">Mostrar todos los conjuntos de días no laborables del grupo de copias de seguridad que pertenecen al grupo principal y comprobar que se incluyen todos los conjuntos de días no laborables de la agrupación principal.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-139">Display all the holiday sets in the backup pool that are owned by the primary pool, and verify that all the primary pool holiday sets are included.</span></span> <span data-ttu-id="0ecfb-140">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-140">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="0ecfb-141">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-141">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
    <span data-ttu-id="0ecfb-142">Como alternativa, puede mostrar todos los grupos de respuesta en el grupo de copias de seguridad, incluidos los que pertenecen al grupo principal y los que pertenecen al grupo de copias de seguridad, con el parámetro – ShowAll en lugar del parámetro – Owner.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-142">Alternatively, you can display all the response groups in the backup pool, including the ones owned by the primary pool and the ones owned by the backup pool by using the –ShowAll parameter instead of the –Owner parameter.</span></span> <span data-ttu-id="0ecfb-143">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-143">For example:</span></span>
    
        Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -ShowAll
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="0ecfb-144">Debe usar el parámetro – ShowAll o el parámetro-Owner.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-144">You must use either the –ShowAll parameter or the –Owner parameter.</span></span> <span data-ttu-id="0ecfb-145">Si no usa ninguno de estos parámetros, los grupos de respuesta que importó al grupo de copias de seguridad no se mostrarán en los resultados devueltos por los cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-145">If you do not use either of these parameters, the response groups that you imported to the backup pool will not be listed in the results returned by the cmdlets.</span></span>

    
    </div>

5.  <span data-ttu-id="0ecfb-146">Verifique que la importación se haya realizado correctamente colocando una llamada a un grupo de respuesta importado y verificando que la llamada se controla correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-146">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

6.  <span data-ttu-id="0ecfb-147">Solicitar agentes que sean miembros de grupos de agentes formales para iniciar sesión en sus grupos de agentes en el grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-147">Request agents who are members of formal agent groups to sign in to their agent groups in the backup pool.</span></span>

7.  <span data-ttu-id="0ecfb-148">Administrar y modificar los grupos de respuesta importados de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-148">Manage and modify the imported response groups as usual.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="0ecfb-149">Mientras los grupos de respuesta están en el grupo de copia de seguridad, necesita usar el shell de administración de Lync Server para administrarlos.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-149">While the response groups are in the backup pool, you need to use Lync Server Management Shell to manage them.</span></span> <span data-ttu-id="0ecfb-150">No puede usar el panel de control de Lync Server para administrar los grupos de respuesta que importó al grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-150">You cannot use Lync Server Control Panel to manage the response groups that you imported to the backup pool.</span></span>

    
    </div>

8.  <span data-ttu-id="0ecfb-151">Una vez que se haya restaurado el grupo principal y se haya completado la conmutación por recuperación, exporte los grupos de respuesta del grupo principal que se importaron al grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-151">After the primary pool is restored and failback is complete, export the primary pool response groups that were imported to the backup pool.</span></span> <span data-ttu-id="0ecfb-152">En la línea de comandos, escriba:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-152">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source ApplicationServer:<backup pool FQDN> -Owner ApplicationServer:<primary pool FQDN> -FileName "<backup path and file name>"

9.  <span data-ttu-id="0ecfb-153">Vuelva a importar los grupos de respuesta al grupo primario.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-153">Import the response groups back to the primary pool.</span></span> <span data-ttu-id="0ecfb-154">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-154">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>"
    
    <span data-ttu-id="0ecfb-155">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-155">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:primary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0ecfb-156">Si reconstruye un grupo durante la recuperación, ya sea con el mismo nombre de dominio completo (FQDN) u otro diferente, debe usar el parámetro – OverwriteOwner.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-156">If you rebuild a pool during recovery, whether with the same or a different fully qualified domain name (FQDN), you need to use the –OverwriteOwner parameter.</span></span> <span data-ttu-id="0ecfb-157">Como regla general, siempre puede usar el parámetro – OverwriteOwner al importar grupos de respuesta al grupo primario.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-157">As a rule of thumb, you can always use the –OverwriteOwner parameter when you import response groups back to the primary pool.</span></span>

    
    </div>
    
    <span data-ttu-id="0ecfb-158">Si implementó un nuevo grupo (con el mismo FQDN u otro diferente) para reemplazar el grupo primario y desea usar la configuración de nivel de aplicación del grupo de copias de seguridad para el nuevo grupo, incluya el parámetro – ReplaceExistingSettings.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-158">If you deployed a new pool (with the same or a different FQDN) to replace the primary pool, and you want to use the application-level settings from the backup pool for the new pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="0ecfb-159">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-159">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<new primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>" -ReplaceExistingSettings
    
    <span data-ttu-id="0ecfb-160">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-160">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:newprimary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="0ecfb-161">Si no quiere reemplazar la configuración de nivel de aplicación y el archivo de audio de música en espera predeterminado para el nuevo grupo con la configuración del grupo de copias de seguridad, el nuevo grupo usará la configuración predeterminada de nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-161">If you don't want to replace the application-level settings and default music-on-hold audio file for the new pool with the settings from the backup pool, the new pool will use the default application-level settings.</span></span>

    
    </div>

10. <span data-ttu-id="0ecfb-162">Compruebe que la importación al grupo primario se ha realizado correctamente mostrando la configuración del grupo de respuesta importado.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-162">Verify that the import back to the primary pool was successful by displaying the imported response group configuration.</span></span> <span data-ttu-id="0ecfb-163">Haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-163">Do the following:</span></span>
    
      - <span data-ttu-id="0ecfb-164">Mostrar todos los flujos de trabajo del grupo principal y comprobar que se incluyen todos los flujos de trabajo importados.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-164">Display all the workflows in the primary pool, and verify that all the imported workflows are included.</span></span> <span data-ttu-id="0ecfb-165">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-165">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0ecfb-166">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-166">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer: primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="0ecfb-167">Muestre todas las colas del grupo principal y compruebe que todas las colas importadas están incluidas.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-167">Display all the queues in the primary pool, and verify that all the imported queues are included.</span></span> <span data-ttu-id="0ecfb-168">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-168">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0ecfb-169">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-169">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="0ecfb-170">Mostrar todos los grupos de agentes en el repositorio principal y comprobar que se incluyen todos los grupos de agentes importados.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-170">Display all the agent groups in the primary pool, and verify that all the imported agent groups are included.</span></span> <span data-ttu-id="0ecfb-171">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-171">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer: <primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0ecfb-172">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-172">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="0ecfb-173">Mostrar todas las horas de actividad en el grupo primario y comprobar que se incluyen todos los horarios de negocios importados.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-173">Display all the hours of business in the primary pool, and verify that all the imported hours of business are included.</span></span> <span data-ttu-id="0ecfb-174">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-174">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0ecfb-175">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-175">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="0ecfb-176">Mostrar todos los conjuntos de días no laborables del repositorio principal y comprobar que están incluidos todos los conjuntos de festividades importados.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-176">Display all the holiday sets in the primary pool, and verify that all the imported holiday sets are included.</span></span> <span data-ttu-id="0ecfb-177">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-177">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="0ecfb-178">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-178">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll

11. <span data-ttu-id="0ecfb-179">Verifique que la importación se haya realizado correctamente colocando una llamada a un grupo de respuesta importado y verificando que la llamada se controla correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-179">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

12. <span data-ttu-id="0ecfb-180">Si lo desea, puede quitar los grupos de respuesta que pertenecen al grupo principal del grupo de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-180">Optionally, remove the response groups owned by the primary pool from the backup pool.</span></span> <span data-ttu-id="0ecfb-181">En la línea de comandos, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-181">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>" -RemoveExportedConfiguration
    
    <span data-ttu-id="0ecfb-182">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0ecfb-182">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimaryUpdated.zip" -RemoveExportedConfiguration
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0ecfb-183">Este paso crea un nuevo archivo con la configuración exportada y, a continuación, lo quita del grupo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0ecfb-183">This step creates a new file with the exported configuration, and then removes it from the backup pool.</span></span>

    
    <span data-ttu-id="0ecfb-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ecfb-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

