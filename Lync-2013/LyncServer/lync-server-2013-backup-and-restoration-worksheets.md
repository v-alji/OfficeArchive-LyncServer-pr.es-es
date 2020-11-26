---
title: 'Lync Server 2013: realizar copias de seguridad y restaurar hojas de cálculo'
description: 'Lync Server 2013: realizar copias de seguridad y restaurar hojas de cálculo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup and restoration worksheets
ms:assetid: 26c78155-0306-41ac-845b-7ad58000a1d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202169(v=OCS.15)
ms:contentKeyID: 51541460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1713e291ae7132cc96309fa499bd97bf7f4f5016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437962"
---
# <a name="backup-and-restoration-worksheets-for-lync-server-2013"></a><span data-ttu-id="a88dc-103">Copias de seguridad y restauración de hojas de cálculo para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a88dc-103">Backup and restoration worksheets for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a88dc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a88dc-104">

<span> </span></span></span>

<span data-ttu-id="a88dc-105">_**Última modificación del tema:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="a88dc-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="a88dc-106">El plan de copia de seguridad y restauración de la organización debe contener detalles sobre cómo y cuándo se realiza la copia de seguridad de los datos y la configuración.</span><span class="sxs-lookup"><span data-stu-id="a88dc-106">The backup and restoration plan for your organization should contain details about how and when you back up data and settings.</span></span> <span data-ttu-id="a88dc-107">Puede usar las hojas de cálculo que se presentan aquí para ayudarle a documentar esta información para su implementación específica y los requisitos de copia de seguridad y restauración de su organización.</span><span class="sxs-lookup"><span data-stu-id="a88dc-107">You can use the worksheets presented here to help you document this information for your specific deployment and for your organization's backup and restoration requirements.</span></span>

<span data-ttu-id="a88dc-108">Use las siguientes hojas de cálculo para registrar la información que necesita para realizar copias de seguridad y restaurar la información de la base de datos, el almacén de archivos y la configuración de un grupo de servidores de Lync o un servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a88dc-108">Use the following worksheets to record the information that you need to back up and restore database, File Store, and settings information for a Lync Server pool or Standard Edition server.</span></span> <span data-ttu-id="a88dc-109">Mantenga una o más copias de estas hojas de cálculo en un lugar seguro para que sean accesibles si necesita restaurar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a88dc-109">Keep one or more copies of these worksheets in a secure location so that they are readily accessible if you need to restore Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a88dc-110">Las hojas de cálculo de esta sección cubren solo la información necesaria para restaurar los datos y la configuración de las bases de datos y los servidores de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a88dc-110">The worksheets in this section cover only the information that is required to restore the data and settings of Lync Server databases and servers.</span></span> <span data-ttu-id="a88dc-111">Si necesita documentar otra información de restauración, como la información para reinstalar sistemas operativos y otro software, use los planes de implementación de su organización y los planes de copia de seguridad y restauración para cumplir esos requisitos.</span><span class="sxs-lookup"><span data-stu-id="a88dc-111">If you need to document other restoration information, such as the information for reinstalling operating systems and other software, use your organization's deployment plans and backup and restoration plans to address those requirements.</span></span>



</div>

<div>

## <a name="database-backup-and-restoration-worksheet"></a><span data-ttu-id="a88dc-112">Hoja de cálculo de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="a88dc-112">Database Backup and Restoration Worksheet</span></span>

<span data-ttu-id="a88dc-113">Use la tabla siguiente para registrar la información que necesita para realizar copias de seguridad y restaurar las bases de datos de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a88dc-113">Use the following table to record the information that you need to back up and restore Lync Server databases.</span></span>

### <a name="database-information-for-backup-and-restoration"></a><span data-ttu-id="a88dc-114">Información de la base de datos para copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="a88dc-114">Database Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a88dc-115">Database</span><span class="sxs-lookup"><span data-stu-id="a88dc-115">Database</span></span></th>
<th><span data-ttu-id="a88dc-116">Nombre del servidor (FQDN)</span><span class="sxs-lookup"><span data-stu-id="a88dc-116">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="a88dc-117">Programación de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="a88dc-117">Backup schedule</span></span></th>
<th><span data-ttu-id="a88dc-118">Herramienta copia de seguridad de base de datos</span><span class="sxs-lookup"><span data-stu-id="a88dc-118">Database backup tool</span></span></th>
<th><span data-ttu-id="a88dc-119">Conjunto de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="a88dc-119">Backup set</span></span></th>
<th><span data-ttu-id="a88dc-120">Destino de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="a88dc-120">Backup destination</span></span></th>
<th><span data-ttu-id="a88dc-121">Notas</span><span class="sxs-lookup"><span data-stu-id="a88dc-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a88dc-122">Base de datos RTC en el servidor back-end para datos de usuario</span><span class="sxs-lookup"><span data-stu-id="a88dc-122">Rtc database on Back End Server for user data</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="a88dc-123">Cmdlet <strong>Export-CsUserData</strong></span><span class="sxs-lookup"><span data-stu-id="a88dc-123"><strong>Export-CsUserData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="a88dc-124">Denomina</span><span class="sxs-lookup"><span data-stu-id="a88dc-124">Name:</span></span></p>
<p><span data-ttu-id="a88dc-125">Currido</span><span class="sxs-lookup"><span data-stu-id="a88dc-125">Expiration:</span></span></p>
<p>                   </p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a88dc-126">LcsLog (nombre predeterminado) base de datos en el servidor de base de datos de archivado</span><span class="sxs-lookup"><span data-stu-id="a88dc-126">LcsLog (default name) database on Archiving database server</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a88dc-127">Herramienta de administración de SQL Server</span><span class="sxs-lookup"><span data-stu-id="a88dc-127">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="a88dc-128">Denomina</span><span class="sxs-lookup"><span data-stu-id="a88dc-128">Name:</span></span></p>
<p><span data-ttu-id="a88dc-129">Currido</span><span class="sxs-lookup"><span data-stu-id="a88dc-129">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a88dc-130">Base de datos de LcsCdr al supervisar el servidor de base de datos para registros de detalles de llamadas (CDRs)</span><span class="sxs-lookup"><span data-stu-id="a88dc-130">LcsCdr database on Monitoring database server for call detail records (CDRs)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a88dc-131">Herramienta de administración de SQL Server</span><span class="sxs-lookup"><span data-stu-id="a88dc-131">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="a88dc-132">Denomina</span><span class="sxs-lookup"><span data-stu-id="a88dc-132">Name:</span></span></p>
<p><span data-ttu-id="a88dc-133">Currido</span><span class="sxs-lookup"><span data-stu-id="a88dc-133">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a88dc-134">QoEMetrics base de datos de supervisión del servidor de base de datos para los datos de la calidad de la experiencia (QoE)</span><span class="sxs-lookup"><span data-stu-id="a88dc-134">QoEMetrics database on Monitoring database server for Quality of Experience (QoE) data</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a88dc-135">Herramienta de administración de SQL Server</span><span class="sxs-lookup"><span data-stu-id="a88dc-135">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="a88dc-136">Denomina</span><span class="sxs-lookup"><span data-stu-id="a88dc-136">Name:</span></span></p>
<p><span data-ttu-id="a88dc-137">Currido</span><span class="sxs-lookup"><span data-stu-id="a88dc-137">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a88dc-138">Base de datos de chat persistente</span><span class="sxs-lookup"><span data-stu-id="a88dc-138">Persistent Chat Database</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="a88dc-139">Herramienta de administración de SQL Server o cmdlet <strong>Export-CsPersistentChatData</strong></span><span class="sxs-lookup"><span data-stu-id="a88dc-139">SQL Server management tool or <strong>Export-CsPersistentChatData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="a88dc-140">Denomina</span><span class="sxs-lookup"><span data-stu-id="a88dc-140">Name:</span></span></p>
<p><span data-ttu-id="a88dc-141">Currido</span><span class="sxs-lookup"><span data-stu-id="a88dc-141">Expiration:</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a88dc-142">No es necesario realizar copias de seguridad ni restauración de las siguientes bases de datos:</span><span class="sxs-lookup"><span data-stu-id="a88dc-142">No backup or restoration is required of the following databases:</span></span>

  - <span data-ttu-id="a88dc-143">Rtcdyn.</span><span class="sxs-lookup"><span data-stu-id="a88dc-143">Rtcdyn.</span></span> <span data-ttu-id="a88dc-144">Los datos de usuario transitorios de esta base de datos no son necesarios para la restauración de servicio.</span><span class="sxs-lookup"><span data-stu-id="a88dc-144">The transient user data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="a88dc-145">Rtcab.</span><span class="sxs-lookup"><span data-stu-id="a88dc-145">Rtcab.</span></span> <span data-ttu-id="a88dc-146">La base de datos de la libreta de direcciones se vuelve a crear automáticamente desde la lista global de direcciones (GAL) en los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a88dc-146">The Address Book database is automatically recreated from the Global Address List (GAL) in Active Directory Domain Services.</span></span>

  - <span data-ttu-id="a88dc-147">Rgsdyn.</span><span class="sxs-lookup"><span data-stu-id="a88dc-147">Rgsdyn.</span></span> <span data-ttu-id="a88dc-148">Los datos transitorios del servicio de grupo de respuesta de esta base de datos no son necesarios para la restauración de servicio.</span><span class="sxs-lookup"><span data-stu-id="a88dc-148">The transient Response Group service data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="a88dc-149">Cpsdyn.</span><span class="sxs-lookup"><span data-stu-id="a88dc-149">Cpsdyn.</span></span> <span data-ttu-id="a88dc-150">La información dinámica para la aplicación de estacionamiento de llamadas no es necesaria para la restauración del servicio.</span><span class="sxs-lookup"><span data-stu-id="a88dc-150">The dynamic information for the Call Park application is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="a88dc-151">MgcComp.</span><span class="sxs-lookup"><span data-stu-id="a88dc-151">MgcComp.</span></span> <span data-ttu-id="a88dc-152">La base de datos de cumplimiento de la conversación persistente no es necesaria para la restauración de servicio.</span><span class="sxs-lookup"><span data-stu-id="a88dc-152">The compliance database for Persistent Chat is not necessary for restoration of service.</span></span>

</div>

<div>

## <a name="file-store-backup-and-restoration-worksheet"></a><span data-ttu-id="a88dc-153">Hoja de cálculo de copia de seguridad y restauración del almacén de archivos</span><span class="sxs-lookup"><span data-stu-id="a88dc-153">File Store Backup and Restoration Worksheet</span></span>

<span data-ttu-id="a88dc-154">Use la tabla siguiente para registrar la información que necesita para hacer una copia de seguridad de los almacenes de archivos y restaurarlos.</span><span class="sxs-lookup"><span data-stu-id="a88dc-154">Use the following table to record the information that you need to back up and restore the File Stores.</span></span> <span data-ttu-id="a88dc-155">Los almacenes de archivos contienen datos como metadatos de contenido de la reunión, registros de cumplimiento de actualizaciones, registros de actualización de dispositivos y archivos de audio para el grupo de respuesta, las llamadas de estacionamiento y las aplicaciones de anuncios.</span><span class="sxs-lookup"><span data-stu-id="a88dc-155">File Stores contain data such as meeting content metadata, meeting compliance logs, update logs for device updates, and audio files for the Response Group, Call Park, and Announcement applications.</span></span>

### <a name="file-store-information-for-backup-and-restoration"></a><span data-ttu-id="a88dc-156">Información del almacén de archivos para copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="a88dc-156">File Store Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a88dc-157">Contenido</span><span class="sxs-lookup"><span data-stu-id="a88dc-157">Content</span></span></th>
<th><span data-ttu-id="a88dc-158">Nombre del servidor (FQDN)</span><span class="sxs-lookup"><span data-stu-id="a88dc-158">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="a88dc-159">Programación de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="a88dc-159">Backup schedule</span></span></th>
<th><span data-ttu-id="a88dc-160">Herramienta de copia de seguridad del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="a88dc-160">File system backup tool</span></span></th>
<th><span data-ttu-id="a88dc-161">Compartir archivos para realizar una copia de seguridad \*</span><span class="sxs-lookup"><span data-stu-id="a88dc-161">File share to be backed up \*</span></span></th>
<th><span data-ttu-id="a88dc-162">Destino de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="a88dc-162">Backup destination</span></span></th>
<th><span data-ttu-id="a88dc-163">Notas</span><span class="sxs-lookup"><span data-stu-id="a88dc-163">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a88dc-164">Almacén de archivos de Lync Server</span><span class="sxs-lookup"><span data-stu-id="a88dc-164">Lync Server File Store</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="a88dc-165">Herramienta de copia de seguridad estándar, como Robocopy</span><span class="sxs-lookup"><span data-stu-id="a88dc-165">Standard backup tool, such as Robocopy</span></span></p></td>
<td><p><span data-ttu-id="a88dc-166">Servidor de archivos para Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="a88dc-166">On file server for Enterprise Edition.</span></span> <span data-ttu-id="a88dc-167">En Standard Edition de forma predeterminada, para la implementación de Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a88dc-167">On Standard Edition by default, for Standard Edition deployment.</span></span> <span data-ttu-id="a88dc-168">Normalmente, uno por sitio.</span><span class="sxs-lookup"><span data-stu-id="a88dc-168">Typically, one per site.</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a88dc-169">No se debe realizar una copia de seguridad de los archivos llamados <strong>Meeting. Active</strong> .</span><span class="sxs-lookup"><span data-stu-id="a88dc-169">Files named <strong>Meeting.Active</strong> should not be backed up.</span></span> <span data-ttu-id="a88dc-170">Estos archivos están en uso y se bloquean durante la reunión.</span><span class="sxs-lookup"><span data-stu-id="a88dc-170">These files are in use and are locked while a meeting takes place.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="settings-backup-and-restoration-worksheet"></a><span data-ttu-id="a88dc-171">Hoja de cálculo de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="a88dc-171">Settings Backup and Restoration Worksheet</span></span>

<span data-ttu-id="a88dc-172">Use la tabla siguiente para registrar la información que necesita para realizar copias de seguridad y restaurar la configuración.</span><span class="sxs-lookup"><span data-stu-id="a88dc-172">Use the following table to record the information that you need to back up and restore settings.</span></span>

### <a name="settings-information-for-backup-and-restoration"></a><span data-ttu-id="a88dc-173">Información de configuración de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="a88dc-173">Settings Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a88dc-174">Database</span><span class="sxs-lookup"><span data-stu-id="a88dc-174">Database</span></span></th>
<th><span data-ttu-id="a88dc-175">Nombre del servidor (FQDN)</span><span class="sxs-lookup"><span data-stu-id="a88dc-175">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="a88dc-176">Programación de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="a88dc-176">Backup schedule</span></span></th>
<th><span data-ttu-id="a88dc-177">Herramienta de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="a88dc-177">Backup tool</span></span></th>
<th><span data-ttu-id="a88dc-178">Nombre del archivo de configuración (. xml)</span><span class="sxs-lookup"><span data-stu-id="a88dc-178">Configuration file (.xml) name</span></span></th>
<th><span data-ttu-id="a88dc-179">Ubicación de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="a88dc-179">Backup location</span></span></th>
<th><span data-ttu-id="a88dc-180">Notas</span><span class="sxs-lookup"><span data-stu-id="a88dc-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a88dc-181">Base de datos XDS en el almacén de administración central para configuración de topología (global)</span><span class="sxs-lookup"><span data-stu-id="a88dc-181">Xds database in Central Management store for topology configuration (global)</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="a88dc-182">Cmdlet <strong>Export-CsConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="a88dc-182"><strong>Export-CsConfiguration</strong> cmdlet</span></span></p></td>
<td><p>                   </p></td>
<td><p>                    </p></td>
<td><p>                   </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a88dc-183">Base de datos de lis en el almacén central de administración para información de la ubicación E9-1-1 (global)</span><span class="sxs-lookup"><span data-stu-id="a88dc-183">Lis database in Central Management store for E9-1-1 location information (global)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a88dc-184">Cmdlet <strong>Export-CsLisConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="a88dc-184"><strong>Export-CsLisConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a88dc-185">Base de datos RgsConfig en el servidor back-end para la configuración de grupo de respuesta (grupo)</span><span class="sxs-lookup"><span data-stu-id="a88dc-185">RgsConfig database on Back End Server for Response Group configuration (pool)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a88dc-186">Cmdlet <strong>Export-CsRgsConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="a88dc-186"><strong>Export-CsRgsConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
</tbody>
</table><span data-ttu-id="a88dc-187">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a88dc-187">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

