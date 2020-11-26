---
title: 'Lync Server 2013: requisitos de copia de seguridad y restauración: herramientas y permisos'
description: 'Lync Server 2013: requisitos de copia de seguridad y restauración: herramientas y permisos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: tools and permissions'
ms:assetid: 35ec2e33-f33e-4f84-9e64-6550fd78aa52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202171(v=OCS.15)
ms:contentKeyID: 51541465
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36327d1214854586b44024f126bbd87acad6c4b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437983"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-tools-and-permissions"></a><span data-ttu-id="21f51-103">Requisitos de copia de seguridad y restauración en Lync Server 2013: herramientas y permisos</span><span class="sxs-lookup"><span data-stu-id="21f51-103">Backup and restoration requirements in Lync Server 2013: tools and permissions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="21f51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="21f51-104">

<span> </span></span></span>

<span data-ttu-id="21f51-105">_**Última modificación del tema:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="21f51-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="21f51-106">En este tema se identifican las herramientas que puede usar para realizar copias de seguridad y restaurar Lync Server 2013, los permisos que necesita y si puede ejecutar comandos de forma remota o local.</span><span class="sxs-lookup"><span data-stu-id="21f51-106">This topic identifies the tools that you can use to back up and restore Lync Server 2013, the permissions that you need, and whether you can run commands remotely or locally.</span></span> <span data-ttu-id="21f51-107">En concreto, este tema se centra en las herramientas que se proporcionan con Lync Server para realizar copias de seguridad y restauraciones.</span><span class="sxs-lookup"><span data-stu-id="21f51-107">Specifically, this topic focuses on tools that are provided with Lync Server for backup and restoration.</span></span>

<div>

## <a name="backups"></a><span data-ttu-id="21f51-108">Copias</span><span class="sxs-lookup"><span data-stu-id="21f51-108">Backups</span></span>

<span data-ttu-id="21f51-109">Para hacer una copia de seguridad de Lync Server, use las herramientas identificadas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="21f51-109">To back up Lync Server, use the tools identified in the following table.</span></span> <span data-ttu-id="21f51-110">Todos los comandos necesarios para realizar copias de seguridad de Lync Server se pueden ejecutar en secuencias de comandos y se pueden ejecutar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="21f51-110">All the commands that you need to back up Lync Server can be scripted and can be run remotely.</span></span>

### <a name="tools-for-backing-up-lync-server"></a><span data-ttu-id="21f51-111">Herramientas para realizar copias de seguridad de Lync Server</span><span class="sxs-lookup"><span data-stu-id="21f51-111">Tools for Backing Up Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21f51-112">Para hacer una copia de seguridad:</span><span class="sxs-lookup"><span data-stu-id="21f51-112">To back up this:</span></span></th>
<th><span data-ttu-id="21f51-113">Use esta herramienta o cmdlet:</span><span class="sxs-lookup"><span data-stu-id="21f51-113">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21f51-114">Datos de configuración de topología (XDS. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-114">Topology configuration data (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="21f51-115">Export-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="21f51-115">Export-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21f51-116">Datos del servicio de información de ubicación (E9-1-1) (LIS. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-116">Location information service (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="21f51-117">Export-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="21f51-117">Export-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21f51-118">Datos de configuración del grupo de respuesta (RgsConfig. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-118">Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="21f51-119">Export-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="21f51-119">Export-CsRgsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21f51-120">Datos de usuario persistentes (base de datos Rtcxds. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-120">Persistent user data (Rtcxds.mdf database)</span></span></p>
<p><span data-ttu-id="21f51-121">Identificadores de conferencia</span><span class="sxs-lookup"><span data-stu-id="21f51-121">Conference IDs</span></span></p></td>
<td><p><span data-ttu-id="21f51-122">Export-CsUserData</span><span class="sxs-lookup"><span data-stu-id="21f51-122">Export-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><ul>
<li><p><span data-ttu-id="21f51-123">Base de datos de archivado (LcsLog. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-123">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="21f51-124">Supervisión de la base de datos de registros de detalles de llamadas (LcsCDR. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-124">Monitoring call detail record database (LcsCDR.mdf)</span></span></p></li>
<li><p><span data-ttu-id="21f51-125">Supervisión de la base de datos de QoE (QoEMetrics. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-125">Monitoring QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21f51-126">Herramienta de base de datos de SQL Server, como SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="21f51-126">SQL Server database tool, such as SQL Server Management Studio</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21f51-127">Base de datos de chat persistente (MGC. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-127">Persistent Chat database (Mgc.mdf)</span></span></p></td>
<td><p><span data-ttu-id="21f51-128">Procedimientos de copia de seguridad de SQL Server o Export-CsPersistentChatData.</span><span class="sxs-lookup"><span data-stu-id="21f51-128">SQL Server backup procedures or Export-CsPersistentChatData.</span></span> <span data-ttu-id="21f51-129">Export-CsPersistentChatData exporta datos de chat persistentes como un archivo.</span><span class="sxs-lookup"><span data-stu-id="21f51-129">Export-CsPersistentChatData exports Persistent Chat data as a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21f51-130">Todos los almacenes de archivos: almacén de archivos de Lync Server, almacén de archivos de archivado</span><span class="sxs-lookup"><span data-stu-id="21f51-130">All file stores: Lync Server file store, Archiving file store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="21f51-131">No se debe realizar una copia de seguridad de los archivos llamados <STRONG>Meeting. Active</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="21f51-131">Files named <STRONG>Meeting.Active</STRONG> should not be backed up.</span></span> <span data-ttu-id="21f51-132">Estos archivos están en uso y se bloquean durante la reunión.</span><span class="sxs-lookup"><span data-stu-id="21f51-132">These files are in use and locked while a meeting takes place.</span></span>


</div></td>
<td><p><span data-ttu-id="21f51-133">Herramienta estándar de administración del sistema de archivos, como Robocopy.</span><span class="sxs-lookup"><span data-stu-id="21f51-133">Standard file system management tool, such as Robocopy.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="restoration"></a><span data-ttu-id="21f51-134">Restablecimiento</span><span class="sxs-lookup"><span data-stu-id="21f51-134">Restoration</span></span>

<span data-ttu-id="21f51-135">Para restaurar Lync Server, use las herramientas de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="21f51-135">To restore Lync Server, use the tools in the following table.</span></span> <span data-ttu-id="21f51-136">Todos los comandos que necesita para restaurar Lync Server se pueden incluir en secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="21f51-136">All the commands that you need to restore Lync Server can be scripted.</span></span> <span data-ttu-id="21f51-137">Algunas pueden ejecutarse de forma remota, pero otras personas deben ejecutarse de forma local, como se especifica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="21f51-137">Some can be run remotely, but others need to be run locally, as specified in the following table.</span></span>

### <a name="tools-for-restoring-lync-server"></a><span data-ttu-id="21f51-138">Herramientas para restaurar Lync Server</span><span class="sxs-lookup"><span data-stu-id="21f51-138">Tools for Restoring Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21f51-139">Para ello, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="21f51-139">To do this:</span></span></th>
<th><span data-ttu-id="21f51-140">Use esta herramienta o cmdlet:</span><span class="sxs-lookup"><span data-stu-id="21f51-140">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21f51-141">Crear un equipo nuevo o limpio</span><span class="sxs-lookup"><span data-stu-id="21f51-141">Build a new or clean computer</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="21f51-142">Software de instalación del sistema operativo Windows</span><span class="sxs-lookup"><span data-stu-id="21f51-142">Windows operating system installation software</span></span></p></li>
<li><p><span data-ttu-id="21f51-143">Software de instalación de SQL Server</span><span class="sxs-lookup"><span data-stu-id="21f51-143">SQL Server installation software</span></span></p></li>
<li><p><span data-ttu-id="21f51-144">Complemento certificados de Microsoft Management Console (MMC), si se restauran certificados con una clave privada exportable</span><span class="sxs-lookup"><span data-stu-id="21f51-144">Certificates Microsoft Management Console (MMC) snap-in, if restoring certificates with an exportable private key</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21f51-145">Restaurar datos del almacén de archivos</span><span class="sxs-lookup"><span data-stu-id="21f51-145">Restore file store data</span></span></p></td>
<td><p><span data-ttu-id="21f51-146">Herramienta estándar de administración del sistema de archivos, como Robocopy</span><span class="sxs-lookup"><span data-stu-id="21f51-146">Standard file system management tool, such as Robocopy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21f51-147">Vuelva a crear bases de datos vacías y establezca los permisos para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="21f51-147">Recreate empty databases and set permissions for the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="21f51-148">Almacén de administración central</span><span class="sxs-lookup"><span data-stu-id="21f51-148">Central Management store</span></span></p></li>
<li><p><span data-ttu-id="21f51-149">Servidor back-end</span><span class="sxs-lookup"><span data-stu-id="21f51-149">Back End Server</span></span></p></li>
<li><p><span data-ttu-id="21f51-150">Base de datos de supervisión</span><span class="sxs-lookup"><span data-stu-id="21f51-150">Monitoring database</span></span></p></li>
<li><p><span data-ttu-id="21f51-151">Base de datos de archivado</span><span class="sxs-lookup"><span data-stu-id="21f51-151">Archiving database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21f51-152">Install-CSDatabase</span><span class="sxs-lookup"><span data-stu-id="21f51-152">Install-CsDatabase</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21f51-153">Restaurar el puntero de servicios de dominio de Active Directory al almacén de administración central</span><span class="sxs-lookup"><span data-stu-id="21f51-153">Restore the Active Directory Domain Services pointer to the Central Management store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="21f51-154">Si pierde el punto de conexión de servicio en cualquier momento, puede volver a ejecutar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f51-154">If you lose the service connection point at any time, you can rerun this cmdlet.</span></span>


</div></td>
<td><p><span data-ttu-id="21f51-155">Set-CsConfigurationStoreLocation</span><span class="sxs-lookup"><span data-stu-id="21f51-155">Set-CsConfigurationStoreLocation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21f51-156">Importar la topología, las directivas y las opciones de configuración en el almacén de administración central (XDS. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-156">Import the topology, policies, and configuration settings to the Central Management store (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="21f51-157">Import-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="21f51-157">Import-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21f51-158">Publicar y habilitar la topología</span><span class="sxs-lookup"><span data-stu-id="21f51-158">Publish and enable the topology</span></span></p></td>
<td><p><span data-ttu-id="21f51-159">Generador de topologías</span><span class="sxs-lookup"><span data-stu-id="21f51-159">Topology Builder</span></span></p>
<p><span data-ttu-id="21f51-160">ni</span><span class="sxs-lookup"><span data-stu-id="21f51-160">-or-</span></span></p>
<p><span data-ttu-id="21f51-161">Publish-CsTopology y Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="21f51-161">Publish-CsTopology and Enable-CsTopology</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21f51-162">Habilitar la última topología Publicada</span><span class="sxs-lookup"><span data-stu-id="21f51-162">Enable the last published topology</span></span></p></td>
<td><p><span data-ttu-id="21f51-163">Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="21f51-163">Enable-CsTopology</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21f51-164">Reinstalar los componentes de Lync Server</span><span class="sxs-lookup"><span data-stu-id="21f51-164">Reinstall Lync Server components</span></span></p></td>
<td><p><span data-ttu-id="21f51-165">Instalación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="21f51-165">Lync Server Setup</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="21f51-166">Se encuentra en la carpeta o el medio de instalación de Lync Server en \setup\amd64\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="21f51-166">Located in the Lync Server installation folder or media at \setup\amd64\Setup.exe.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21f51-167">Restaurar datos de ubicación (E9-1-1) (LIS. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-167">Restore location information (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="21f51-168">Import-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="21f51-168">Import-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21f51-169">Restaurar datos de usuario persistentes (Rtcxds. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-169">Restore persistent user data (Rtcxds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="21f51-170">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="21f51-170">Import-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21f51-171">Restaurar datos de configuración de grupo de respuesta (RgsConfig. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-171">Restore Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="21f51-172">Import-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="21f51-172">Import-CsRgsConfiguration</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="21f51-173">Si la configuración se está restaurando en un grupo recién implementado que no tiene datos de grupo de respuesta en la base de datos, debe usar la opción – OverwriteOwner.</span><span class="sxs-lookup"><span data-stu-id="21f51-173">If the configuration is being restored in a newly deployed pool that has no Response Group data in the database, then you should use the –OverwriteOwner option.</span></span> <span data-ttu-id="21f51-174">Use esta opción incluso si los datos que se están restaurando están en un grupo con el mismo nombre de dominio completo (FQDN).</span><span class="sxs-lookup"><span data-stu-id="21f51-174">Use this option even if the data being restored is in a pool with the same fully qualified domain name (FQDN).</span></span> <span data-ttu-id="21f51-175">De lo contrario, la importación no se realizará correctamente, debido a los objetos de contacto de los grupos de respuesta que ya existen en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="21f51-175">Otherwise, the import will not succeed, due to the contact objects to the Response Groups already existing in Active Directory.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21f51-176">Restaure las siguientes bases de datos:</span><span class="sxs-lookup"><span data-stu-id="21f51-176">Restore the following databases:</span></span></p>
<ul>
<li><p><span data-ttu-id="21f51-177">Base de datos de archivado (LcsLog. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-177">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="21f51-178">Supervisar bases de datos: base de datos de registros de detalles de llamadas (LcsCDR. MDF) y base de datos de QoE (QoEMetrics. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-178">Monitoring databases: call detail record database (LcsCDR.mdf) and QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21f51-179">Herramientas de administración de bases de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="21f51-179">SQL Server database management tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21f51-180">Base de datos de chat persistente (MGS. MDF)</span><span class="sxs-lookup"><span data-stu-id="21f51-180">Persistent Chat database (Mgs.mdf)</span></span></p></td>
<td><p><span data-ttu-id="21f51-181">Procedimientos de restauración de SQL Server o Import-CsPersistentChatData.</span><span class="sxs-lookup"><span data-stu-id="21f51-181">SQL Server restore procedures or Import-CsPersistentChatData.</span></span> <span data-ttu-id="21f51-182">Puede usar Import-CsPersistentChatData con un archivo creado por Export-CsPersistentChatData y los datos se importarán a la base de datos de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="21f51-182">You can use Import-CsPersistentChatData with a file created by Export-CsPersistentChatData, and the data will be imported into the Persistent Chat database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="required-permissions"></a><span data-ttu-id="21f51-183">Permisos necesarios</span><span class="sxs-lookup"><span data-stu-id="21f51-183">Required Permissions</span></span>

<span data-ttu-id="21f51-184">Los usuarios deben ser miembros del grupo **RTCUniversalServerAdmins** para poder ejecutar todos los comandos que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="21f51-184">Users must be a member of the **RTCUniversalServerAdmins** group to perform all the commands described in this topic.</span></span> <span data-ttu-id="21f51-185">La mayoría de los comandos de copia de seguridad y restauración no admiten el control de acceso basado en roles (RBAC).</span><span class="sxs-lookup"><span data-stu-id="21f51-185">Most backup and restore commands do not support role-based access control (RBAC).</span></span> <span data-ttu-id="21f51-186">Dos excepciones son los cmdlets de chat persistentes Export-CsPersistentChatData y Import-CsPersistentChatData, que debe ejecutar un usuario que sea miembro del grupo CsPersistentChatAdministrator.</span><span class="sxs-lookup"><span data-stu-id="21f51-186">Two exceptions are the Persistent Chat cmdlets Export-CsPersistentChatData and Import-CsPersistentChatData, which must be run by a user who is a member of the CsPersistentChatAdministrator group.</span></span> <span data-ttu-id="21f51-187">Para ejecutar el Asistente para la implementación de Lync Server, un usuario también debe ser miembro del grupo de administradores locales.</span><span class="sxs-lookup"><span data-stu-id="21f51-187">To run Lync Server Deployment Wizard, a user must also be a member of the Local Adminstrators group.</span></span>

<span data-ttu-id="21f51-188"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="21f51-188"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

