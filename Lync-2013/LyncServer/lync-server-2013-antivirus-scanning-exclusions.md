---
title: 'Lync Server 2013: Exclusiones de la detección de virus'
description: 'Lync Server 2013: exclusiones de detección de antivirus.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Antivirus scanning exclusions for Lync Server 2013
ms:assetid: 71e1f1cc-2d16-4111-9864-9276bf24dfe0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440138(v=OCS.15)
ms:contentKeyID: 57793042
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20c395f529cad91993d003efdeb231bd66f4b9bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440664"
---
# <a name="antivirus-scanning-exclusions-for-lync-server-2013"></a><span data-ttu-id="d4f02-103">Exclusiones de la detección de virus para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4f02-103">Antivirus scanning exclusions for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4f02-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4f02-104">

<span> </span></span></span>

<span data-ttu-id="d4f02-105">_**Última modificación del tema:** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="d4f02-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="d4f02-106">Para asegurarse de que el detector de virus no interfiere con el funcionamiento de Lync Server 2013, debe excluir los procesos y directorios específicos de cada rol de servidor o servidor de Lync Server 2013 en el que se ejecute un detector de virus.</span><span class="sxs-lookup"><span data-stu-id="d4f02-106">To ensure that the antivirus scanner does not interfere with the operation of Lync Server 2013, you must exclude specific processes and directories for each Lync Server 2013 server or server role on which you run an antivirus scanner.</span></span> <span data-ttu-id="d4f02-107">Es necesario excluir los siguientes procesos y directorios:</span><span class="sxs-lookup"><span data-stu-id="d4f02-107">The following processes and directories should be excluded:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d4f02-108">Las ubicaciones de carpetas y archivos que se enumeran a continuación son las ubicaciones predeterminadas de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d4f02-108">Folder and file locations listed below are the default locations for Lync Server 2013.</span></span> <span data-ttu-id="d4f02-109">Si no usó los valores predeterminados para algunas ubicaciones, excluya esas ubicaciones especificadas para su organización en lugar de las ubicaciones predeterminadas especificadas en este tema.</span><span class="sxs-lookup"><span data-stu-id="d4f02-109">For any locations for which you did not use the default, exclude the locations you specified for your organization instead of the default locations specified in this topic.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d4f02-110">Tenga en cuenta que es posible que algunos programas antivirus necesiten rutas de acceso absolutas (no relativas) para su lista de exclusión.</span><span class="sxs-lookup"><span data-stu-id="d4f02-110">Please note that some antivirus programs may need absolute, not relative paths, for their exclusion list.</span></span>



</div>

  - <span data-ttu-id="d4f02-111">Procesos de 2013 de Lync Server:</span><span class="sxs-lookup"><span data-stu-id="d4f02-111">Lync Server 2013 processes:</span></span>
    
      - <span data-ttu-id="d4f02-112">ABServer.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-112">ABServer.exe</span></span>
    
      - <span data-ttu-id="d4f02-113">AcpMcuSvc.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-113">AcpMcuSvc.exe</span></span>
    
      - <span data-ttu-id="d4f02-114">ASMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-114">ASMCUSvc.exe</span></span>
    
      - <span data-ttu-id="d4f02-115">AVMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-115">AVMCUSvc.exe</span></span>
    
      - <span data-ttu-id="d4f02-116">ChannelService.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-116">ChannelService.exe</span></span>
    
      - <span data-ttu-id="d4f02-117">ClsAgent.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-117">ClsAgent.exe</span></span>
    
      - <span data-ttu-id="d4f02-118">ComplianceService.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-118">ComplianceService.exe</span></span>
    
      - <span data-ttu-id="d4f02-119">DataMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-119">DataMCUSvc.exe</span></span>
    
      - <span data-ttu-id="d4f02-120">DataProxy.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-120">DataProxy.exe</span></span>
    
      - <span data-ttu-id="d4f02-121">FileTransferAgent.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-121">FileTransferAgent.exe</span></span>
    
      - <span data-ttu-id="d4f02-122">IMMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-122">IMMCUSvc.exe</span></span>
    
      - <span data-ttu-id="d4f02-123">LysSvc.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-123">LysSvc.exe</span></span>
    
      - <span data-ttu-id="d4f02-124">MasterReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-124">MasterReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="d4f02-125">MediaRelaySvc.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-125">MediaRelaySvc.exe</span></span>
    
      - <span data-ttu-id="d4f02-126">MediationServerSvc.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-126">MediationServerSvc.exe</span></span>
    
      - <span data-ttu-id="d4f02-127">MRASSvc.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-127">MRASSvc.exe</span></span>
    
      - <span data-ttu-id="d4f02-128">OcsAppServerHost.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-128">OcsAppServerHost.exe</span></span>
    
      - <span data-ttu-id="d4f02-129">ReplicaReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-129">ReplicaReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="d4f02-130">ReplicationApp.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-130">ReplicationApp.exe</span></span>
    
      - <span data-ttu-id="d4f02-131">RtcHost.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-131">RtcHost.exe</span></span>
    
      - <span data-ttu-id="d4f02-132">RTCSrv.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-132">RTCSrv.exe</span></span>
    
      - <span data-ttu-id="d4f02-133">XmppProxy.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-133">XmppProxy.exe</span></span>
    
      - <span data-ttu-id="d4f02-134">XmppTGW.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-134">XmppTGW.exe</span></span>

  - <span data-ttu-id="d4f02-135">Procesos del servicio de host de Windows Fabric:</span><span class="sxs-lookup"><span data-stu-id="d4f02-135">Windows Fabric Host Service processes:</span></span>
    
      - <span data-ttu-id="d4f02-136">Fabric.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-136">Fabric.exe</span></span>
    
      - <span data-ttu-id="d4f02-137">FabricDCA.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-137">FabricDCA.exe</span></span>
    
      - <span data-ttu-id="d4f02-138">FabricHost.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-138">FabricHost.exe</span></span>

  - <span data-ttu-id="d4f02-139">Procesos de IIS:</span><span class="sxs-lookup"><span data-stu-id="d4f02-139">IIS processes:</span></span>
    
      - <span data-ttu-id="d4f02-140">% SystemRoot% \\ system32 \\ Inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-140">%systemroot%\\system32\\inetsrv\\w3wp.exe</span></span>
    
      - <span data-ttu-id="d4f02-141">% SystemRoot% \\ SysWOW64 \\ Inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-141">%systemroot%\\SysWOW64\\inetsrv\\w3wp.exe</span></span>

  - <span data-ttu-id="d4f02-142">Procesos del back-end de SQL Server:</span><span class="sxs-lookup"><span data-stu-id="d4f02-142">SQL Server Back-End processes:</span></span>
    
      - <span data-ttu-id="d4f02-143">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. Binn de MSSQLSERVER de MSSQLSERVER \\ \\ \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-143">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.MSSQLSERVER\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="d4f02-144">% ProgramFiles% \\ Microsoft SQL Server \\ MSRS11. \\Papelera de Reporting Services de MSSQLSERVER \\ \\ \\ReportingServicesService.exe</span><span class="sxs-lookup"><span data-stu-id="d4f02-144">%ProgramFiles%\\Microsoft SQL Server\\MSRS11.MSSQLSERVER\\Reporting Services\\ReportServer\\Bin\\ReportingServicesService.exe</span></span>
    
      - <span data-ttu-id="d4f02-145">% ProgramFiles% \\ Microsoft SQL Server \\ MSAS11.MSMDSrv.exe de la \\ bandeja OLAP de MSSQLServer \\ \\</span><span class="sxs-lookup"><span data-stu-id="d4f02-145">%ProgramFiles%\\Microsoft SQL Server\\MSAS11.MSSQLSERVER\\OLAP\\Bin\\MSMDSrv.exe</span></span>

  - <span data-ttu-id="d4f02-146">Procesos del front-end de SQL Server:</span><span class="sxs-lookup"><span data-stu-id="d4f02-146">SQL Server Front-End processes:</span></span>
    
      - <span data-ttu-id="d4f02-147">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. \\ \\SQLServr.exe Binn de LYNCLOCAL MSSQL \\</span><span class="sxs-lookup"><span data-stu-id="d4f02-147">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.LYNCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="d4f02-148">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. \\ \\SQLServr.exe Binn de RTCLOCAL MSSQL \\</span><span class="sxs-lookup"><span data-stu-id="d4f02-148">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.RTCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>

  - <span data-ttu-id="d4f02-149">Directorios y archivos:</span><span class="sxs-lookup"><span data-stu-id="d4f02-149">Directories and files:</span></span>
    
      - <span data-ttu-id="d4f02-150">archivos de registro de% SystemRoot% \\ system32 \\</span><span class="sxs-lookup"><span data-stu-id="d4f02-150">%systemroot%\\System32\\LogFiles</span></span>
    
      - <span data-ttu-id="d4f02-151">archivos de registro de% SystemRoot% \\ SysWow64 \\</span><span class="sxs-lookup"><span data-stu-id="d4f02-151">%systemroot%\\SysWow64\\LogFiles</span></span>
    
      - <span data-ttu-id="d4f02-152">% SystemRoot% \\ Microsoft.net del \\ ensamblado \\ GAC \_ MSIL</span><span class="sxs-lookup"><span data-stu-id="d4f02-152">%systemroot%\\Microsoft.NET\\assembly\\GAC\_MSIL</span></span>
    
      - <span data-ttu-id="d4f02-153">% programfiles% \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4f02-153">%programfiles%\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="d4f02-154">Archivos comunes de% ProgramFiles% \\ \\ Microsoft Lync Server 2013 \\ nodo de monitor</span><span class="sxs-lookup"><span data-stu-id="d4f02-154">%programfiles%\\Common Files\\Microsoft Lync Server 2013\\Watcher Node</span></span>
    
      - <span data-ttu-id="d4f02-155">Archivos comunes de% ProgramFiles% \\ \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4f02-155">%programfiles%\\Common Files\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="d4f02-156">% SystemDrive% \\ RtcReplicaRoot</span><span class="sxs-lookup"><span data-stu-id="d4f02-156">%SystemDrive%\\RtcReplicaRoot</span></span>
    
      - <span data-ttu-id="d4f02-157">Almacén de recurso compartido de archivos (especificado en el Generador de topologías).</span><span class="sxs-lookup"><span data-stu-id="d4f02-157">File share store (specified in Topology Builder).</span></span> <span data-ttu-id="d4f02-158">Los almacenes de archivos se especifican en el Generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="d4f02-158">File stores are specified in Topology Builder.</span></span>
    
      - <span data-ttu-id="d4f02-159">Datos y archivos de registro de SQL Server, incluidos los relacionados con la base de datos back-end, el almacén de usuarios, el almacén de archivado, el almacén de supervisión y el almacén de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d4f02-159">SQL Server data and log files, including those for the back-end database, user store, archiving store, monitoring store, and application store.</span></span> <span data-ttu-id="d4f02-160">Las bases de datos y los archivos de registro se pueden especificar en el Generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="d4f02-160">Database and log files can be specified in Topology Builder.</span></span> <span data-ttu-id="d4f02-161">Para obtener detalles sobre los archivos de datos y de registro de cada base de datos, incluidos los nombres predeterminados, consulte ubicación de los [archivos de registro y datos de SQL Server para Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="d4f02-161">For details about the data and log files for each database, including default names, see [SQL Server data and log file placement for Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="d4f02-162">Los datos y archivos de registro de SQL Server, incluidos los de la base de datos front-end, la tienda Lync y la tienda RtcDatabase.</span><span class="sxs-lookup"><span data-stu-id="d4f02-162">SQL Server data and log files, including those for the Front-end database, Lync store, and RtcDatabase store.</span></span> <span data-ttu-id="d4f02-163">Normalmente se encuentran debajo de% UnidadLocal% \\ CSData.</span><span class="sxs-lookup"><span data-stu-id="d4f02-163">They are normally under %localdrive%\\CSData.</span></span>

<span data-ttu-id="d4f02-164"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4f02-164"></div>

<span> </span>

</div>

</div>

</span></span></div>

