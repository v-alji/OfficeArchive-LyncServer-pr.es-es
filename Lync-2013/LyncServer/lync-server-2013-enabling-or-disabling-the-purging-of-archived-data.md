---
title: 'Lync Server 2013: habilitar o deshabilitar la purga de datos archivados'
description: 'Lync Server 2013: habilitar o deshabilitar la purga de datos archivados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling the purging of archived data
ms:assetid: 28cef09f-0970-4fc3-8315-f26689e3e187
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520968(v=OCS.15)
ms:contentKeyID: 48183678
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 442b99e2cfa6db303ca8edd216cbdf3b5c13cea9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428751"
---
# <a name="enabling-or-disabling-the-purging-of-archived-data-in-lync-server-2013"></a><span data-ttu-id="1c025-103">Habilitar o deshabilitar la purga de datos archivados en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c025-103">Enabling or disabling the purging of archived data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c025-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c025-104">

<span> </span></span></span>

<span data-ttu-id="1c025-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="1c025-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="1c025-106">En el panel de control de Lync Server 2013, se usan configuraciones de archivado para habilitar y deshabilitar la purga y configuración de la implementación de la purga.</span><span class="sxs-lookup"><span data-stu-id="1c025-106">In Lync Server 2013 Control Panel, you use Archiving configurations to enable and disable purging and configure how purging is implemented.</span></span> <span data-ttu-id="1c025-107">Esto incluye las siguientes configuraciones de archivado:</span><span class="sxs-lookup"><span data-stu-id="1c025-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="1c025-108">Una configuración global que se crea de forma predeterminada al implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1c025-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="1c025-109">Configuraciones de nivel de sitio y de grupo opcionales que puede crear y usar para especificar cómo se implementa el archivado para grupos o sitios específicos.</span><span class="sxs-lookup"><span data-stu-id="1c025-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="1c025-110">Inicialmente, debe configurar las configuraciones de archivado al implementar el archivado, pero puede cambiar, agregar y eliminar configuraciones después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="1c025-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="1c025-111">Para obtener detalles sobre cómo se implementan las configuraciones de archivado, incluidas las opciones que puede especificar y la jerarquía de las configuraciones de archivado, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="1c025-111">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1c025-112">Para usar el archivado para los usuarios alojados en Lync Server 2013 debe configurar las directivas de archivado para especificar si desea habilitar el archivado de las comunicaciones internas, de las comunicaciones externas o de ambos.</span><span class="sxs-lookup"><span data-stu-id="1c025-112">To use archiving for users who are homed on Lync Server 2013 you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both.</span></span> <span data-ttu-id="1c025-113">De forma predeterminada, el archivado no está habilitado para las comunicaciones internas o externas.</span><span class="sxs-lookup"><span data-stu-id="1c025-113">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="1c025-114">Antes de habilitar el archivado en cualquier directiva, debe especificar las configuraciones de archivado apropiadas para su implementación y, opcionalmente, para determinados sitios y grupos, tal y como se describe en esta sección.</span><span class="sxs-lookup"><span data-stu-id="1c025-114">Prior to enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="1c025-115">Para obtener más información sobre cómo habilitar el archivado, vea <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">configurar y asignar directivas de archivado en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="1c025-115">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="1c025-116">Si decide que después de implementar el archivado desea usar la integración de Microsoft Exchange para almacenar datos y archivos en servidores de Exchange 2013 y todos los usuarios están alojados en los servidores de Exchange 2013, debe quitar la configuración de la base de datos de SQL Server de su topología.</span><span class="sxs-lookup"><span data-stu-id="1c025-116">If you decide after you deploy Archiving that you want to use Microsoft Exchange integration to store archiving data and files on Exchange 2013 servers and all your users are homed on your Exchange 2013 servers, you should remove the SQL Server database configuration from your topology.</span></span> <span data-ttu-id="1c025-117">Para ello, debe usar el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="1c025-117">You must use Topology Builder to do this.</span></span> <span data-ttu-id="1c025-118">Para obtener más información, vea <A href="lync-server-2013-changing-archiving-database-options.md">cambiar las opciones de base de datos de archivado en Lync Server 2013</A> en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="1c025-118">For details, see <A href="lync-server-2013-changing-archiving-database-options.md">Changing Archiving database options in Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-purging-for-archiving"></a><span data-ttu-id="1c025-119">Para habilitar o deshabilitar la depuración para el archivado</span><span class="sxs-lookup"><span data-stu-id="1c025-119">To enable or disable purging for archiving</span></span>

1.  <span data-ttu-id="1c025-120">Desde una cuenta de usuario que se asigne al rol CsArchivingAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="1c025-120">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="1c025-121">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1c025-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="1c025-122">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="1c025-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="1c025-123">En la barra de navegación izquierda, haga clic en **Supervisión y archivado** y, después, en **Configuración de archivado**.</span><span class="sxs-lookup"><span data-stu-id="1c025-123">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="1c025-124">Haga clic en el nombre de la configuración global, de sitio o de grupo adecuada en la lista de configuraciones de archivado; haga clic en **Editar**, en **Mostrar detalles** y, luego, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1c025-124">Click the name of the appropriate global, site, or pool configuration in the list of archiving configurations, click **Edit**, click **Show details**, and then do the following:</span></span>
    
      - <span data-ttu-id="1c025-125">Para habilitar la purga, active la casilla **Habilitar purgado de los datos de archivado** y siga uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="1c025-125">To enable purging, select the **Enable purging of archiving data** check box and then do one of the following:</span></span>
        
          - <span data-ttu-id="1c025-126">Para purgar todos los registros, haga clic en **Purgar los datos de archivado exportados y los datos de archivado almacenados tras la duración máxima (días)** y, luego, especifique la cantidad de días.</span><span class="sxs-lookup"><span data-stu-id="1c025-126">To purge all records, click the **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="1c025-127">Para purgar solo los datos que se han exportado, haga clic en **Purgar solo datos de archivado exportados**.</span><span class="sxs-lookup"><span data-stu-id="1c025-127">To purge only the data that has been exported, click **Purge exported archiving data only**.</span></span>
    
      - <span data-ttu-id="1c025-128">Para deshabilitar la purga, desactive la casilla **Habilitar purgado de los datos de archivado**.</span><span class="sxs-lookup"><span data-stu-id="1c025-128">To disable purging, clear the **Enable purging of archiving data** check box.</span></span>

5.  <span data-ttu-id="1c025-129">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="1c025-129">Click **Commit**.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-the-purging-of-archiving-data-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="1c025-130">Habilitar o deshabilitar la purga de datos de archivado mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1c025-130">Enabling or Disabling the Purging of Archiving Data by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="1c025-131">Habilitar y deshabilitar la purga automática de datos de archivado se puede administrar mediante Windows PowerShell y el cmdlet **set-CsArchivingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="1c025-131">Enabling and disabling the automated purging of archiving data can be managed by using Windows PowerShell and the **Set-CsArchivingConfiguration** cmdlet.</span></span> <span data-ttu-id="1c025-132">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1c025-132">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="1c025-133">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="1c025-133">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-purging-of-all-archiving-data"></a><span data-ttu-id="1c025-134">Para habilitar la purga de todos los datos de archivado</span><span class="sxs-lookup"><span data-stu-id="1c025-134">To enable the purging of all archiving data</span></span>

  - <span data-ttu-id="1c025-135">Para habilitar la purga de todos los datos de archivado, establezca la propiedad **EnablePurging** en true ($true).</span><span class="sxs-lookup"><span data-stu-id="1c025-135">To enable the purging of all archiving data set the **EnablePurging** property to true ($True).</span></span> <span data-ttu-id="1c025-136">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1c025-136">For example:</span></span>
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -EnablePurging $True
    
    <span data-ttu-id="1c025-137">Después de ejecutar este comando, cada día, Lync Server purgará todos los registros de archivado anteriores al valor especificado para la propiedad **KeepArchivingDataForDays** .</span><span class="sxs-lookup"><span data-stu-id="1c025-137">After this command is run, then every day Lync Server will purge all archiving records older than the value specified for the **KeepArchivingDataForDays** property.</span></span>

</div>

<div>

## <a name="to-enable-the-purging-only-of-exported-archiving-data"></a><span data-ttu-id="1c025-138">Para habilitar la purga solamente de datos de archivado exportados</span><span class="sxs-lookup"><span data-stu-id="1c025-138">To enable the purging only of exported archiving data</span></span>

  - <span data-ttu-id="1c025-139">Para limitar la purga a los registros que se han exportado a un archivo de datos (mediante el cmdlet [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) ), también debe establecer la propiedad PurgeExportedArchivesOnly en True ($true).</span><span class="sxs-lookup"><span data-stu-id="1c025-139">To limit purging to archiving records that have been exported to a data file (by using the [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) cmdlet) you must also set the PurgeExportedArchivesOnly property to True ($True).</span></span> <span data-ttu-id="1c025-140">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1c025-140">For example:</span></span>
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -EnablePurging $True -PurgeExportedArchivesOnly $True
    
    <span data-ttu-id="1c025-141">Después de ejecutar este comando, Lync Server solo purgará los registros de archivado que cumplan con dos criterios: 1) son anteriores al valor especificado para la propiedad **KeepArchivingDataForDays** ; y 2) se han exportado con el cmdlet **Export-CsArchivingData** .</span><span class="sxs-lookup"><span data-stu-id="1c025-141">After this command is run, Lync Server will only purge archiving records that meet two criteria: 1) they are older than the value specified for the **KeepArchivingDataForDays** property; and, 2) they have been exported by using the **Export-CsArchivingData** cmdlet.</span></span>

</div>

<div>

## <a name="to-disable-the-purging-of-all-archiving-data"></a><span data-ttu-id="1c025-142">Para deshabilitar la purga de todos los datos de archivado</span><span class="sxs-lookup"><span data-stu-id="1c025-142">To disable the purging of all archiving data</span></span>

  - <span data-ttu-id="1c025-143">Para deshabilitar la purga automática de registros archivados, establezca la propiedad **EnablePurging** en falso ($false).</span><span class="sxs-lookup"><span data-stu-id="1c025-143">To disable the automated purging of archiving records, set the **EnablePurging** property to False ($False).</span></span> <span data-ttu-id="1c025-144">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1c025-144">For example:</span></span>
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -EnablePurging $False

</div>

<span data-ttu-id="1c025-145">Para obtener más información, incluidas opciones adicionales para purgar el archivado de datos, consulte el tema de ayuda sobre el cmdlet [set-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="1c025-145">For more information, including additional options for purging archiving data, see the help topic for the [Set-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1c025-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c025-146">See Also</span></span>


[<span data-ttu-id="1c025-147">Cómo funciona el archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c025-147">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="1c025-148">Configurar y asignar directivas de archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c025-148">Configuring and assigning Archiving policies in Lync Server 2013</span></span>](lync-server-2013-configuring-and-assigning-archiving-policies.md)  
[<span data-ttu-id="1c025-149">Administrar las opciones de configuración de archivado en Lync Server 2013 para su organización, sitios y grupos</span><span class="sxs-lookup"><span data-stu-id="1c025-149">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)  
  

<span data-ttu-id="1c025-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c025-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

