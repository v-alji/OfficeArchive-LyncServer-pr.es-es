---
title: 'Lync Server 2013: crear una configuración de archivado para administrar el archivado de grupos o sitios específicos'
description: 'Lync Server 2013: crear una configuración de archivado para administrar el archivado de determinados sitios o grupos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving configuration to manage Archiving for specific sites or pools
ms:assetid: c5c864a6-96c7-4bbb-ab7c-61eb1744246c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205251(v=OCS.15)
ms:contentKeyID: 48185361
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ab19f2d8900693ef0fcb14d8f6d862b22c355bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431536"
---
# <a name="creating-an-archiving-configuration-in-lync-server-2013-to-manage-archiving-for-specific-sites-or-pools"></a><span data-ttu-id="67703-103">Creación de una configuración de archivado en Lync Server 2013 para administrar el archivado de sitios o grupos específicos</span><span class="sxs-lookup"><span data-stu-id="67703-103">Creating an Archiving configuration in Lync Server 2013 to manage Archiving for specific sites or pools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67703-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67703-104">

<span> </span></span></span>

<span data-ttu-id="67703-105">_**Última modificación del tema:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="67703-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="67703-106">En el panel de control de Lync Server 2013, use las configuraciones de archivado para controlar cómo se implementa el archivado en su implementación.</span><span class="sxs-lookup"><span data-stu-id="67703-106">In Lync Server 2013 Control Panel, you use Archiving configurations to control how archiving is implemented in your deployment.</span></span> <span data-ttu-id="67703-107">Esto incluye las siguientes configuraciones de archivado:</span><span class="sxs-lookup"><span data-stu-id="67703-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="67703-108">Una configuración global que se crea de forma predeterminada al implementar Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="67703-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="67703-109">Configuraciones de nivel de sitio y de grupo opcionales que puede crear y usar para especificar cómo se implementa el archivado para grupos o sitios específicos.</span><span class="sxs-lookup"><span data-stu-id="67703-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="67703-110">Inicialmente, debe configurar las configuraciones de archivado al implementar el archivado, pero puede cambiar, agregar y eliminar configuraciones después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="67703-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="67703-111">Para obtener detalles sobre cómo se implementan las configuraciones de archivado, incluidas las opciones que puede especificar y la jerarquía de las configuraciones de archivado, consulte [Cómo funciona el archivado en Lync Server 2013](lync-server-2013-how-archiving-works.md) en la documentación de planeación, la documentación de implementación o la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="67703-111">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="67703-112">Para usar el archivado, debe configurar las directivas de archivado para especificar si desea habilitar el archivado de las comunicaciones internas, de las comunicaciones externas o de ambos para los usuarios alojados en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="67703-112">To use archiving, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both for users homed on Lync Server 2013.</span></span> <span data-ttu-id="67703-113">De forma predeterminada, el archivado no está habilitado para las comunicaciones internas o externas.</span><span class="sxs-lookup"><span data-stu-id="67703-113">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="67703-114">Antes de habilitar el archivado en cualquier directiva, debe especificar las configuraciones de archivado apropiadas para su implementación y, opcionalmente, para determinados sitios y grupos, tal y como se describe en esta sección.</span><span class="sxs-lookup"><span data-stu-id="67703-114">Before enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="67703-115">Para obtener más información sobre cómo habilitar el archivado, vea <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">configurar y asignar directivas de archivado en Lync Server 2013</A> en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="67703-115">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="67703-116">Si decide que después de implementar el archivado desea usar la integración de Microsoft Exchange para almacenar datos y archivos en servidores de Exchange 2013 y todos los usuarios están alojados en los servidores de Exchange 2013, debe quitar la configuración de la base de datos de SQL Server de su topología.</span><span class="sxs-lookup"><span data-stu-id="67703-116">If you decide after you deploy Archiving that you want to use Microsoft Exchange integration to store archiving data and files on Exchange 2013 servers and all your users are homed on your Exchange 2013 servers, you should remove the SQL Server database configuration from your topology.</span></span> <span data-ttu-id="67703-117">Para ello, debe usar el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="67703-117">You must use Topology Builder to do this.</span></span> <span data-ttu-id="67703-118">Para obtener más información, vea <A href="lync-server-2013-changing-archiving-database-options.md">cambiar las opciones de base de datos de archivado en Lync Server 2013</A> en la documentación de operaciones.</span><span class="sxs-lookup"><span data-stu-id="67703-118">For details, see <A href="lync-server-2013-changing-archiving-database-options.md">Changing Archiving database options in Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-configuration-for-a-site-or-pool"></a><span data-ttu-id="67703-119">Para crear una configuración de archivado para un sitio o grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="67703-119">To create an archiving configuration for a site or pool</span></span>

1.  <span data-ttu-id="67703-120">Desde una cuenta de usuario que se asigne al rol CsArchivingAdministrator o CsAdministrator, inicie sesión en cualquier equipo en la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="67703-120">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="67703-121">Abra una ventana del explorador y, a continuación, escriba la dirección URL del administrador para abrir el panel de control de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="67703-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="67703-122">Para obtener más información sobre los diferentes métodos que puede usar para iniciar el panel de control de Lync Server, consulte [abrir las herramientas administrativas 2013 de Lync Server](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="67703-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="67703-123">En la barra de navegación izquierda, haga clic en **Supervisión y archivado** y, después, en **Configuración de archivado**.</span><span class="sxs-lookup"><span data-stu-id="67703-123">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="67703-124">En la página **Configuración de archivado**, haga clic en **Nuevo** y haga una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="67703-124">On the **Archiving Configuration** page, click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="67703-125">Para crear una configuración de archivado de sitio, haga clic en **configuración del sitio** y, a continuación, en **seleccionar un sitio**, seleccione el sitio que se va a configurar para el archivado.</span><span class="sxs-lookup"><span data-stu-id="67703-125">To create a site archiving configuration, click **Site Configuration** and then, in **Select a site**, select the site to be configured for archiving.</span></span>
    
      - <span data-ttu-id="67703-126">Para crear una configuración de archivado de grupo, haga clic en **configuración del grupo** y, a continuación, en **seleccionar un grupo** de servidores, seleccione el grupo de servidores que se va a configurar para el archivado.</span><span class="sxs-lookup"><span data-stu-id="67703-126">To create a pool archiving configuration, click **Pool Configuration** and then, in **Select a pool**, select the pool to be configured for archiving.</span></span>

5.  <span data-ttu-id="67703-127">En **Nueva configuración de archivado**, vaya al cuadro de lista desplegable **Configuración de archivado** y siga uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="67703-127">In **New Archiving Setting**, in the **Archiving setting** drop-down list box, do one of the following:</span></span>
    
      - <span data-ttu-id="67703-128">Para habilitar el archivado solo para las sesiones de mensajería instantánea (MI), haga clic en **Archivar sesiones de mensajería instantánea (MI)**.</span><span class="sxs-lookup"><span data-stu-id="67703-128">To enable archiving only for instant messaging (IM) sessions, click **Archive IM sessions**.</span></span>
    
      - <span data-ttu-id="67703-129">Para habilitar el archivado tanto para las sesiones de mensajería instantánea (MI) como para las conferencias web, haga clic en **Archivar sesiones de mensajería instantánea (MI) y conferencias web**.</span><span class="sxs-lookup"><span data-stu-id="67703-129">To enable archiving for both IM sessions and web conferences, click **Archive IM and web conferencing sessions**.</span></span>
    
      - <span data-ttu-id="67703-130">A fin de deshabilitar el archivado de la directiva, haga clic en **Deshabilitar archivado**.</span><span class="sxs-lookup"><span data-stu-id="67703-130">To disable archiving for the policy, click **Disable archiving**.</span></span>

6.  <span data-ttu-id="67703-131">Además, en **Nueva configuración de archivado**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="67703-131">Also in **New Archiving Setting**, do the following:</span></span>
    
      - <span data-ttu-id="67703-132">Para bloquear la actividad cuando el archivado no está disponible, active la casilla **Bloquear sesiones de mensajería instantánea (MI) o de conferencias web si no se pueden archivar**.</span><span class="sxs-lookup"><span data-stu-id="67703-132">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="67703-133">Para usar Microsoft Exchange Server para almacenar datos de archivado, haga clic en la casilla de verificación **integración con Microsoft Exchange** .</span><span class="sxs-lookup"><span data-stu-id="67703-133">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="67703-134">Para habilitar la purga de datos, active la casilla **Habilitar purgado de los datos de archivado** y realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="67703-134">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="67703-135">Para especificar la purga al transcurrir una cantidad de días determinada, haga clic en **Purgar los datos de archivado exportados y los datos de archivado almacenados tras la duración máxima (días)** y especifique la cantidad de días.</span><span class="sxs-lookup"><span data-stu-id="67703-135">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="67703-136">Para limitar la purga de los datos de archivado que se han exportado, haga clic en **Purgar solo datos de archivado exportados**.</span><span class="sxs-lookup"><span data-stu-id="67703-136">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

7.  <span data-ttu-id="67703-137">Haga clic en **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="67703-137">Click **Commit**.</span></span>

</div>

<div>

## <a name="creating-archiving-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="67703-138">Creación de parámetros de configuración de archivado mediante cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="67703-138">Creating Archiving Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="67703-139">Los valores de configuración de archivado se pueden crear con Windows PowerShell y el cmdlet New-CsArchivingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="67703-139">Archiving configuration settings can be created by using Windows PowerShell and the New-CsArchivingConfiguration cmdlet.</span></span> <span data-ttu-id="67703-140">Este cmdlet se puede ejecutar desde el shell de administración de Lync Server 2013 o desde una sesión remota de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="67703-140">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="67703-141">Para obtener más información sobre cómo usar Windows PowerShell remoto para conectarse a Lync Server, consulte el artículo del blog de Lync Server de Windows PowerShell "Inicio rápido: administrar Microsoft Lync Server 2010 mediante PowerShell remoto" en [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="67703-141">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-collection-of-archiving-configuration-settings-for-a-site"></a><span data-ttu-id="67703-142">Para crear una nueva colección de parámetros de configuración de archivado para un sitio</span><span class="sxs-lookup"><span data-stu-id="67703-142">To create a new collection of archiving configuration settings for a site</span></span>

  - <span data-ttu-id="67703-143">El comando siguiente crea una colección de opciones de configuración de archivado para el sitio de Redmond:</span><span class="sxs-lookup"><span data-stu-id="67703-143">The following command creates a new collection of archiving configuration settings for the Redmond site:</span></span>
    
        New-CsArchivingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-collection-of-archiving-configuration-settings-that-only-allow-im-archiving"></a><span data-ttu-id="67703-144">Para crear una nueva colección de opciones de configuración de archivado que solo permitan el archivado de mensajes instantáneos</span><span class="sxs-lookup"><span data-stu-id="67703-144">To create a new collection of archiving configuration settings that only allow IM archiving</span></span>

  - <span data-ttu-id="67703-145">Dado que, en el comando anterior, no se especificaron parámetros (además del parámetro de identidad obligatorio), la nueva colección de valores de configuración usará los valores predeterminados para todas sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="67703-145">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties.</span></span> <span data-ttu-id="67703-146">Para crear una configuración que use otros valores de propiedad, basta con incluir el parámetro y el valor correspondiente adecuados.</span><span class="sxs-lookup"><span data-stu-id="67703-146">To create settings that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="67703-147">Por ejemplo, para crear una colección de opciones de configuración de archivado que permitan el archivado de sesiones de mensajería instantánea, de forma predeterminada, use únicamente un comando como este:</span><span class="sxs-lookup"><span data-stu-id="67703-147">For example, to create a collection of archiving configuration settings that, by default, allow archiving of instant messaging sessions, only use a command like this:</span></span>
    
        New-CsArchivingConfiguration -Identity "site:Redmond" -EnableArchiving "ImOnly"

</div>

<div>

## <a name="to-specify-multiple-property-values-when-creating-archiving-configuration-settings"></a><span data-ttu-id="67703-148">Para especificar varios valores de propiedad al crear parámetros de configuración de archivado</span><span class="sxs-lookup"><span data-stu-id="67703-148">To specify multiple property values when creating archiving configuration settings</span></span>

  - <span data-ttu-id="67703-p108">Puede incluir varios parámetros para modificar varios valores de propiedad. Por ejemplo, este comando define la nueva configuración para archivar las sesiones de mensajería instantánea y bloquear la mensajería instantánea si el servicio de archivado no está disponible:</span><span class="sxs-lookup"><span data-stu-id="67703-p108">Multiple property values can be modified by including multiple parameters. For example, this command configures the new settings to archive instant messaging sessions and to block instant messaging of the archiving service is not available:</span></span>
    
        New-CsArchivingConfiguration -Identity "site:Redmond" -EnableArchiving "ImOnly" -BlockOnArchiveFailure $True

</div>

<span data-ttu-id="67703-151">Para obtener más información, vea el tema de ayuda sobre el cmdlet [New-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsArchivingConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="67703-151">For more information, see the help topic for the [New-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsArchivingConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="67703-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="67703-152">See Also</span></span>


[<span data-ttu-id="67703-153">Cómo funciona el archivado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67703-153">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="67703-154">Administrar las opciones de configuración de archivado en Lync Server 2013 para su organización, sitios y grupos</span><span class="sxs-lookup"><span data-stu-id="67703-154">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)  
  

<span data-ttu-id="67703-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67703-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

