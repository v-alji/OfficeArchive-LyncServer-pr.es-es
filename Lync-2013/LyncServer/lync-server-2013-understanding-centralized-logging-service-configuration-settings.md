---
title: Descripción de las opciones de configuración del servicio de registro centralizado
description: Descripción de las opciones de configuración del servicio de registro centralizado.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding Centralized Logging Service configuration settings
ms:assetid: 3c34e600-0b91-43dc-b4cc-90b6a70ee12e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688029(v=OCS.15)
ms:contentKeyID: 49733619
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f99dbffe15c4b3f0dc13d231c3a2732a8554397
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399497"
---
# <a name="understanding-centralized-logging-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="370b7-103">Descripción de la configuración del servicio de registro centralizado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="370b7-103">Understanding Centralized Logging Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="370b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="370b7-104">

<span> </span></span></span>

<span data-ttu-id="370b7-105">_**Última modificación del tema:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="370b7-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="370b7-106">El servicio de registro centralizado está configurado para definir qué debe recopilar el servicio de registro, cómo se recopila, de dónde se recopilará y de cuál es la configuración de registro.</span><span class="sxs-lookup"><span data-stu-id="370b7-106">The Centralized Logging Service is configured to define what the logging service is intended to collect, how it collects, where it will collect from, and what the log settings are.</span></span> <span data-ttu-id="370b7-107">Define estas configuraciones de modo global (es decir, para toda la implementación) o para un sitio (es decir, para un sitio específico de la implementación).</span><span class="sxs-lookup"><span data-stu-id="370b7-107">You define these settings globally (that is, for the entire deployment) or for a site (that is, a named site in your deployment).</span></span> <span data-ttu-id="370b7-108">Cualquier registro que defina utilizará la configuración apropiada de la identidad que utiliza para iniciar, detener, vaciar y buscar registros.</span><span class="sxs-lookup"><span data-stu-id="370b7-108">Any logging that you define will use the settings that are appropriate for the identity that you use for commands to start, stop, flush, and search logs.</span></span>

<div>

## <a name="to-display-the-current-centralized-logging-service-configuration"></a><span data-ttu-id="370b7-109">Para mostrar la configuración del servicio de registro centralizado actual</span><span class="sxs-lookup"><span data-stu-id="370b7-109">To display the current Centralized Logging Service configuration</span></span>

1.  <span data-ttu-id="370b7-110">Inicie el shell de administración de Lync Server: haga clic en **Inicio**, seleccione **todos los programas**, **Microsoft Lync Server 2013** y, a continuación, haga clic en **Shell de administración de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="370b7-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="370b7-111">Escriba lo siguiente en un símbolo de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="370b7-111">Type the following at a command-line prompt:</span></span>
    
        Get-CsClsConfiguration
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="370b7-112">Puede restringir o expandir el ámbito de los parámetros de configuración devueltos por la definición de <CODE>-Identity</CODE> un ámbito, como "sitio: Redmond" para devolver solo el CsClsConfiguration del sitio Redmond.</span><span class="sxs-lookup"><span data-stu-id="370b7-112">You can narrow or expand the scope of the configuration settings that are returned by defining <CODE>-Identity</CODE> and a scope, such as "Site:Redmond" to return only the CsClsConfiguration for the site Redmond.</span></span> <span data-ttu-id="370b7-113">Si desea detalles sobre una parte determinada de la configuración, puede canalizar la salida en otro cmdlet de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="370b7-113">If you want details about a given portion of the configuration, you can pipe the output into another Windows PowerShell cmdlet.</span></span> <span data-ttu-id="370b7-114">Por ejemplo, para obtener detalles sobre los escenarios definidos en la configuración del sitio "Redmond", escriba lo siguiente: <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span><span class="sxs-lookup"><span data-stu-id="370b7-114">For example, to get details about the scenarios defined in the configuration for site "Redmond", type: <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span></span>

    
    </div>
    
    <span data-ttu-id="370b7-115">![Salida de ejemplo de Get-CsClsConfiguration.](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Salida de ejemplo de Get-CsClsConfiguration.")</span><span class="sxs-lookup"><span data-stu-id="370b7-115">![Sample output from Get-CsClsConfiguration.](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Sample output from Get-CsClsConfiguration.")</span></span>
    
    <span data-ttu-id="370b7-116">El resultado del cmdlet muestra la configuración actual del servicio de registro centralizado.</span><span class="sxs-lookup"><span data-stu-id="370b7-116">The result from the cmdlet displays the current configuration of the Centralized Logging Service.</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="370b7-117">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="370b7-117">Configuration Setting</span></span></th>
    <th><span data-ttu-id="370b7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="370b7-118">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="370b7-119"><strong>Identity</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-119"><strong>Identity</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-p103">Identifica el ámbito y el nombre de esta configuración. Hay solamente una configuración global y una configuración por sitio.</span><span class="sxs-lookup"><span data-stu-id="370b7-p103">Identifies the scope and name for this configuration. There is only one Global configuration, and one configuration per site.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="370b7-122"><strong>Scenarios</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-122"><strong>Scenarios</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-123">Listado de todos los escenarios que se definen para esta configuración.</span><span class="sxs-lookup"><span data-stu-id="370b7-123">Listing of all scenarios that are defined for this configuration.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="370b7-124"><strong>SearchTerms</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-124"><strong>SearchTerms</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-125">Términos de búsqueda definidos para la configuración.</span><span class="sxs-lookup"><span data-stu-id="370b7-125">Defined search terms for the configuration.</span></span> <span data-ttu-id="370b7-126">Office 365 o Microsoft 365, no implementaciones locales.</span><span class="sxs-lookup"><span data-stu-id="370b7-126">Office 365 or Microsoft 365, not on-premises deployments.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="370b7-127"><strong>SecurityGroups</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-127"><strong>SecurityGroups</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-128">Grupos de seguridad definidos que controlan quiénes (es decir, qué miembros de los grupos de seguridad) pueden ver equipos basados en el sitio en el que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="370b7-128">Defined security groups that control who (that is, members of the security groups) can see computers based on the site they are located in.</span></span> <span data-ttu-id="370b7-129">Sitio, en este contexto, es el sitio definido en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="370b7-129">Site, in this context, is the site as defined in Topology Builder.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="370b7-130"><strong>Regions</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-130"><strong>Regions</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-131">Las regiones definidas se utilizan para recopilar SecurityGroups en una región, por ejemplo EMEA.</span><span class="sxs-lookup"><span data-stu-id="370b7-131">Defined regions are used to collect SecurityGroups into a region, for example EMEA.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="370b7-132"><strong>EtlFileFolder</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-132"><strong>EtlFileFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-133">Ruta de acceso definida a la ubicación donde se escriben los archivos de registro en los equipos.</span><span class="sxs-lookup"><span data-stu-id="370b7-133">Defined path to the location where log files are written on computers.</span></span> <span data-ttu-id="370b7-134">CLSAgent escribe los archivos de registro y se ejecuta en el contexto del servicio de red.</span><span class="sxs-lookup"><span data-stu-id="370b7-134">CLSAgent writes the log files and runs under the context of the Network Service.</span></span> <span data-ttu-id="370b7-135">En este caso,% TEMP% se expande a%WINDIR%\ServiceProfiles\NetworkService\AppData\Local</span><span class="sxs-lookup"><span data-stu-id="370b7-135">In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="370b7-136"><strong>EtlFileRolloverSizeMB</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-136"><strong>EtlFileRolloverSizeMB</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-p107">El parámetro indica el tamaño máximo del archivo de registro antes de que se cree un archivo de registro de seguimiento de eventos (.etl). Un nuevo archivo de registro se crea cuando se alcanza el tamaño definido, incluso si aún no se ha alcanzado el tiempo máximo establecido en EtlFileRolloverMinutes.</span><span class="sxs-lookup"><span data-stu-id="370b7-p107">The parameter indicates the maximum size of the log file before a new event trace log (.etl) file is created. A new log file is created when the defined size is reached even if the maximum time set in EtlFileRolloverMinutes has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="370b7-139"><strong>EtlFileRolloverMinutes</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-139"><strong>EtlFileRolloverMinutes</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-p108">Cantidad máxima definida de tiempo, en minutos, que puede durar un registro antes de que se cree un nuevo archivo .etl. Un nuevo archivo de registro se crea cuando expira el tiempo definido incluso si aún no se ha alcanzado el tamaño máximo establecido en EtlFileRolloverSizeMB.</span><span class="sxs-lookup"><span data-stu-id="370b7-p108">Defined maximum amount of time, in minutes, that a log can elapse before a new .etl file is created. A new log file is created when the timer expires even if the maximum size set in EtlFileRolloverSizeMB has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="370b7-142"><strong>TmfFileSearchPath</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-142"><strong>TmfFileSearchPath</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-143">Ubicación en la que se buscarán archivos con formato de mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="370b7-143">Location to search for the trace message format files.</span></span> <span data-ttu-id="370b7-144">Los archivos de formato de mensaje de seguimiento se usan para convertir los archivos binarios en un formato legible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="370b7-144">The trace message format files are used to convert the binary files into a human readable format.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="370b7-145"><strong>CacheFileLocalFolders</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-145"><strong>CacheFileLocalFolders</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-p110">Ruta de acceso definida de la ubicación en la que se escriben los archivos caché en los equipos. CLSAgent escribe los archivos caché y se ejecuta en el contexto del servicio de red. En este caso, %TEMP% se expande a %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local. De manera predeterminada, los archivos caché y los archivos de registro se escriben en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="370b7-p110">Defined path to the location where cache files are written on computers. CLSAgent writes the cache files and runs under the context of the Network Service. In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local. By default, cache files and log files are written to the same directory.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="370b7-150"><strong>CacheFileNetworkFolder</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-150"><strong>CacheFileNetworkFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-151">Puede definir una ruta de acceso de convención de nomenclatura universal (UNC) para recibir los archivos caché durante las operaciones de registro.</span><span class="sxs-lookup"><span data-stu-id="370b7-151">You can define a universal naming convention (UNC) path to receive the cache files during logging operations.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="370b7-152"><strong>CacheFileLocalRetentionPeriod</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-152"><strong>CacheFileLocalRetentionPeriod</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-153">Definido como el tiempo máximo, en días, que se pueden retener los archivos caché.</span><span class="sxs-lookup"><span data-stu-id="370b7-153">Defined as the maximum time, in days, that cache files are retained.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="370b7-154"><strong>CacheFileMaxDiskUsage</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-154"><strong>CacheFileMaxDiskUsage</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-155">Definido como el porcentaje de espacio en disco que pueden utilizar los archivos caché.</span><span class="sxs-lookup"><span data-stu-id="370b7-155">Defined as the percentage of disk space that can be used by the cache files.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="370b7-156"><strong>ComponentThrottleLimit</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-156"><strong>ComponentThrottleLimit</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-157">Definido como la cantidad máxima de seguimientos por segundo que puede producir un componente antes de que se active el limitador de aceleración automático.</span><span class="sxs-lookup"><span data-stu-id="370b7-157">Defined as the maximum number of traces per second that a component can produce before the automatic throttle limiter is triggered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="370b7-158"><strong>ComponentThrottleSample</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-158"><strong>ComponentThrottleSample</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-159">Cantidad de veces en 60 segundos que puede excederse el ComponentThrottleLimit.</span><span class="sxs-lookup"><span data-stu-id="370b7-159">Number of times in 60 seconds that the ComponentThrottleLimit can be exceeded.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="370b7-160"><strong>MinimumClsAgentServiceVersion</strong></span><span class="sxs-lookup"><span data-stu-id="370b7-160"><strong>MinimumClsAgentServiceVersion</strong></span></span></p></td>
    <td><p><span data-ttu-id="370b7-161">La versión mínima del CLSAgent que se permite ejecutar.</span><span class="sxs-lookup"><span data-stu-id="370b7-161">The minimum version of the CLSAgent allowed to run.</span></span> <span data-ttu-id="370b7-162">Este elemento está pensado para Office 365 o Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="370b7-162">This element is intended for Office 365 or Microsoft 365.</span></span></p></td>
    </tr>
    </tbody>
    </table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="370b7-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="370b7-163">See Also</span></span>


[<span data-ttu-id="370b7-164">Información general sobre el servicio de registro centralizado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="370b7-164">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)  


<span data-ttu-id="370b7-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="370b7-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span></span>  
<span data-ttu-id="370b7-166">[Remove-CsClsConfiguration](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="370b7-166">[Remove-CsClsConfiguration](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span></span>  
<span data-ttu-id="370b7-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="370b7-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span></span>  
<span data-ttu-id="370b7-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="370b7-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span></span>  
  

<span data-ttu-id="370b7-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="370b7-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

