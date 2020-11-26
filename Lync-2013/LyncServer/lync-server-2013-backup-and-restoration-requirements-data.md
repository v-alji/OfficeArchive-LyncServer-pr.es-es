---
title: 'Lync Server 2013: requisitos de copia de seguridad y restauración: datos'
description: 'Lync Server 2013: requisitos de copia de seguridad y restauración: datos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: data'
ms:assetid: ecfb8e4d-cb4f-476d-9772-4486bd683c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202194(v=OCS.15)
ms:contentKeyID: 51541526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e135f09706d31ff3f0efa54c8687546de9fab78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437990"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-data"></a><span data-ttu-id="ef6da-103">Requisitos de copia de seguridad y restauración en Lync Server 2013: datos</span><span class="sxs-lookup"><span data-stu-id="ef6da-103">Backup and restoration requirements in Lync Server 2013: data</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef6da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef6da-104">

<span> </span></span></span>

<span data-ttu-id="ef6da-105">_**Última modificación del tema:** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="ef6da-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="ef6da-106">Lync Server usa la configuración y la información de configuración que se almacenan en bases de datos y datos que se almacenan en bases de datos y almacenes de archivos.</span><span class="sxs-lookup"><span data-stu-id="ef6da-106">Lync Server uses settings and configuration information that are stored in databases, and data that is stored in databases and file stores.</span></span> <span data-ttu-id="ef6da-107">En este tema se describen los datos de los que debe hacer una copia de seguridad para poder restaurar el servicio si su organización sufre un error o una interrupción, y también identifica los datos y componentes usados por Lync Server que necesita para hacer una copia de seguridad por separado.</span><span class="sxs-lookup"><span data-stu-id="ef6da-107">This topic describes the data that you need to back up to be able to restore service if your organization experiences a failure or outage, and also identifies the data and components used by Lync Server that you need to back up separately.</span></span>

<div>

## <a name="settings-and-configuration-requirements"></a><span data-ttu-id="ef6da-108">Requisitos de configuración y configuración</span><span class="sxs-lookup"><span data-stu-id="ef6da-108">Settings and Configuration Requirements</span></span>

<span data-ttu-id="ef6da-109">Este tema incluye procedimientos para realizar copias de seguridad y restaurar la configuración y la información de configuración necesarias para la recuperación del servicio de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-109">This topic includes procedures for backing up and restoring the settings and configuration information that is required for recovery of Lync Server service.</span></span> <span data-ttu-id="ef6da-110">La información de configuración se encuentra en el almacén central de administración o en otra base de datos back-end o en un servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="ef6da-110">The configuration information is located in the Central Management store or on another back-end database or on Standard Edition server.</span></span>

<span data-ttu-id="ef6da-111">La siguiente tabla identifica la configuración y la información de configuración que necesita para realizar copias de seguridad y restaurar.</span><span class="sxs-lookup"><span data-stu-id="ef6da-111">The following table identifies the settings and configuration information that you need to back up and restore.</span></span>

### <a name="settings-and-configuration-data"></a><span data-ttu-id="ef6da-112">Datos de configuración y configuración</span><span class="sxs-lookup"><span data-stu-id="ef6da-112">Settings and Configuration Data</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef6da-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ef6da-113">Type of data</span></span></th>
<th><span data-ttu-id="ef6da-114">Donde se almacena</span><span class="sxs-lookup"><span data-stu-id="ef6da-114">Where stored</span></span></th>
<th><span data-ttu-id="ef6da-115">Descripción/Cuándo hacer una copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="ef6da-115">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef6da-116">Información de configuración de topología</span><span class="sxs-lookup"><span data-stu-id="ef6da-116">Topology configuration information</span></span></p></td>
<td><p><span data-ttu-id="ef6da-117">Tienda de administración central (base de datos: XDS. MDF)</span><span class="sxs-lookup"><span data-stu-id="ef6da-117">Central Management store (database: Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ef6da-118">Topología, Directiva y parámetros de configuración.</span><span class="sxs-lookup"><span data-stu-id="ef6da-118">Topology, policy, and configuration settings.</span></span></p>
<p><span data-ttu-id="ef6da-119">Haga una copia de seguridad de las copias de seguridad periódicas y después use los cmdlets o el panel de control de Lync Server para modificar su configuración o directivas.</span><span class="sxs-lookup"><span data-stu-id="ef6da-119">Back up with your regular backups and after you use Lync Server Control Panel or cmdlets to modify your configuration or policies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef6da-120">Información de ubicación</span><span class="sxs-lookup"><span data-stu-id="ef6da-120">Location information</span></span></p></td>
<td><p><span data-ttu-id="ef6da-121">Almacén de administración central (base de datos: Lis. MDF)</span><span class="sxs-lookup"><span data-stu-id="ef6da-121">Central Management store (database: Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ef6da-122">Información de configuración de Enterprise Voice Enhanced 9-1-1 (E9-1-1).</span><span class="sxs-lookup"><span data-stu-id="ef6da-122">Enterprise Voice Enhanced 9-1-1 (E9-1-1) configuration information.</span></span> <span data-ttu-id="ef6da-123">Generalmente, esta información es estática.</span><span class="sxs-lookup"><span data-stu-id="ef6da-123">This information is generally static.</span></span></p>
<p><span data-ttu-id="ef6da-124">Haga una copia de seguridad de sus copias de seguridad periódicas.</span><span class="sxs-lookup"><span data-stu-id="ef6da-124">Back up with your regular backups.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef6da-125">Información de configuración del grupo de respuesta</span><span class="sxs-lookup"><span data-stu-id="ef6da-125">Response Group configuration information</span></span></p></td>
<td><p><span data-ttu-id="ef6da-126">Servidor back-end o servidor Standard Edition (base de datos: RgsConfig. MDF)</span><span class="sxs-lookup"><span data-stu-id="ef6da-126">Back End Server or Standard Edition server (database: RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ef6da-127">Grupos de agentes de grupo de respuesta, colas y flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ef6da-127">Response Group agent groups, queues, and workflows.</span></span></p>
<p><span data-ttu-id="ef6da-128">Haga una copia de seguridad de sus copias de seguridad periódicas y después agregue o cambie los grupos de agentes, las colas o los flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ef6da-128">Back up with your regular backups and after you add or change agent groups, queues, or workflows.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="data-requirements"></a><span data-ttu-id="ef6da-129">Requisitos de datos</span><span class="sxs-lookup"><span data-stu-id="ef6da-129">Data Requirements</span></span>

<span data-ttu-id="ef6da-130">A continuación se muestra una lista de los datos de Lync Server que necesita para realizar una copia de seguridad de modo que pueda restaurar el servicio Lync Server en caso de que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="ef6da-130">Here is a list of the Lync Server data that you need to back up so that you can restore Lync Server service in the event of a failure.</span></span>

<span data-ttu-id="ef6da-131">Tenga en cuenta que algunos tipos de datos no son necesarios para la recuperación.</span><span class="sxs-lookup"><span data-stu-id="ef6da-131">Note that some types of data are not required for recovery.</span></span> <span data-ttu-id="ef6da-132">Este tema no contiene procedimientos para realizar copias de seguridad de estos tipos de datos, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ef6da-132">This topic does not contain procedures for backing up these types of data, which include the following:</span></span>

  - <span data-ttu-id="ef6da-133">Datos de usuario transitorios, como puntos finales y suscripciones, servidores de conferencia activos y Estados de conferencia transitorios (base de datos: RtcDyn. MDF)</span><span class="sxs-lookup"><span data-stu-id="ef6da-133">Transient user data, such as endpoints and subscriptions, active conferencing servers, and transient conferencing states (database: RtcDyn.mdf)</span></span>

  - <span data-ttu-id="ef6da-134">Datos de la libreta de direcciones (bases de datos: Rtcab. MDF y Rtcab1. MDF).</span><span class="sxs-lookup"><span data-stu-id="ef6da-134">Address Book data (databases: Rtcab.mdf and Rtcab1.mdf).</span></span> <span data-ttu-id="ef6da-135">La base de datos de la libreta de direcciones se regenera automáticamente desde los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ef6da-135">The Address Book database is regenerated automatically from Active Directory Domain Services.</span></span>

  - <span data-ttu-id="ef6da-136">Información dinámica para la aplicación de estacionamiento de llamadas (base de datos: CpsDyn. MDF)</span><span class="sxs-lookup"><span data-stu-id="ef6da-136">Dynamic information for the Call Park application (database: CpsDyn.mdf)</span></span>

  - <span data-ttu-id="ef6da-137">Datos de grupo de respuesta transitorios, como el estado de inicio de sesión del agente y la información de llamada en espera (base de datos: RgsDyn. MDF)</span><span class="sxs-lookup"><span data-stu-id="ef6da-137">Transient Response Group data, such as agent sign-in state and call waiting information (database: RgsDyn.mdf)</span></span>

  - <span data-ttu-id="ef6da-138">La base de datos de cumplimiento para una conversación persistente (base de datos: MgcComp. MDF).</span><span class="sxs-lookup"><span data-stu-id="ef6da-138">The compliance database for Persistent Chat (database: MgcComp.mdf).</span></span> <span data-ttu-id="ef6da-139">Si tiene habilitada la compatibilidad de chat persistente, la información de la base de datos de cumplimiento persistente de chat es transitoria siempre que tenga un adaptador configurado para leer la información de la base de datos y convertirla a un formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="ef6da-139">If you have Persistent Chat compliance enabled, the information in the Persistent Chat Compliance database is transient as long as you have an adapter configured to read information from the database and convert it to an alternate format.</span></span> <span data-ttu-id="ef6da-140">Por lo tanto, la base de datos de cumplimiento para chat persistente se considera transitoria.</span><span class="sxs-lookup"><span data-stu-id="ef6da-140">Hence the compliance database for Persistent Chat is considered transient.</span></span>
    
    <span data-ttu-id="ef6da-141">Lync Server 2013 el servidor de chat persistente se distribuye con un adaptador XML.</span><span class="sxs-lookup"><span data-stu-id="ef6da-141">Lync Server 2013 Persistent Chat Server ships with an XML adapter.</span></span> <span data-ttu-id="ef6da-142">También puede instalar adaptadores personalizados que toman estos datos y los mueven a otros orígenes, como archivos hospedados de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef6da-142">You can also install custom adapters that take this data and move it to other sources, such as Exchange Hosted Archives.</span></span>

<span data-ttu-id="ef6da-143">La siguiente tabla identifica los datos que necesita para realizar copias de seguridad y restaurar.</span><span class="sxs-lookup"><span data-stu-id="ef6da-143">The following table identifies the data that you need to back up and restore.</span></span>

### <a name="data-stored-in-databases"></a><span data-ttu-id="ef6da-144">Datos almacenados en bases de datos</span><span class="sxs-lookup"><span data-stu-id="ef6da-144">Data Stored in Databases</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef6da-145">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ef6da-145">Type of data</span></span></th>
<th><span data-ttu-id="ef6da-146">Donde se almacena</span><span class="sxs-lookup"><span data-stu-id="ef6da-146">Where stored</span></span></th>
<th><span data-ttu-id="ef6da-147">Descripción/Cuándo hacer una copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="ef6da-147">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef6da-148">Datos de usuario persistentes</span><span class="sxs-lookup"><span data-stu-id="ef6da-148">Persistent user data</span></span></p></td>
<td><p><span data-ttu-id="ef6da-149">Servidor back-end o servidor Standard Edition (base de datos: RTCXDS. MDF)</span><span class="sxs-lookup"><span data-stu-id="ef6da-149">Back End Server or Standard Edition server (database: RTCXDS.mdf)</span></span></p></td>
<td><p><span data-ttu-id="ef6da-150">Derechos de usuario, listas de contactos de usuarios, datos de servidores o agrupaciones, conferencias programadas, etc.</span><span class="sxs-lookup"><span data-stu-id="ef6da-150">User rights, user Contacts lists, server or pool data, scheduled conferences, and so on.</span></span> <span data-ttu-id="ef6da-151">Los datos de este usuario no incluyen contenido cargado en una conferencia.</span><span class="sxs-lookup"><span data-stu-id="ef6da-151">This user data does not include content uploaded to a conference.</span></span></p>
<p><span data-ttu-id="ef6da-152">Haga una copia de seguridad de sus copias de seguridad periódicas.</span><span class="sxs-lookup"><span data-stu-id="ef6da-152">Back up with your regular backups.</span></span> <span data-ttu-id="ef6da-153">Esta información es dinámica, pero la pérdida de actualizaciones no es catastrófica para Lync Server si necesita restaurar la última copia de seguridad normal.</span><span class="sxs-lookup"><span data-stu-id="ef6da-153">This information is dynamic, but the loss of updates is not catastrophic to Lync Server if you need to restore to your last regular backup.</span></span> <span data-ttu-id="ef6da-154">Si las listas de contactos son críticas para su organización, puede realizar copias de seguridad de estos datos con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="ef6da-154">If Contacts lists are critical to your organization, you can back up this data more frequently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef6da-155">Archivar datos</span><span class="sxs-lookup"><span data-stu-id="ef6da-155">Archiving data</span></span></p></td>
<td><p><span data-ttu-id="ef6da-156">Base de datos de archivado (base de datos: LcsLog. MDF)</span><span class="sxs-lookup"><span data-stu-id="ef6da-156">Archiving database (database: LcsLog.mdf)</span></span></p>
<p><span data-ttu-id="ef6da-157">Estos datos pueden almacenarse en Exchange 2013, si ha habilitado la opción de integración de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef6da-157">This data may be stored on Exchange 2013, if you have enabled the Microsoft Exchange integration option.</span></span> <span data-ttu-id="ef6da-158">De lo contrario, estos datos se guardan en una base de datos de archivado de Lync Server, que se puede colocar con otra base de datos de Lync Server o independiente en un servidor de base de datos independiente.</span><span class="sxs-lookup"><span data-stu-id="ef6da-158">Otherwise, this data is kept in a Lync Server Archiving database, which may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="ef6da-159">Mensajería instantánea (mi) y contenido de la reunión.</span><span class="sxs-lookup"><span data-stu-id="ef6da-159">Instant messaging (IM) and meeting content.</span></span></p>
<p><span data-ttu-id="ef6da-160">Esta información no es crítica para Lync Server, pero puede ser fundamental para su organización con fines normativos.</span><span class="sxs-lookup"><span data-stu-id="ef6da-160">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="ef6da-161">Determine la programación de la copia de seguridad según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ef6da-161">Determine your back up schedule accordingly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef6da-162">Supervisión de datos</span><span class="sxs-lookup"><span data-stu-id="ef6da-162">Monitoring data</span></span></p></td>
<td><p><span data-ttu-id="ef6da-163">Supervisar bases de datos (LcsCDR. MDF y QoeMetrics. MDF)</span><span class="sxs-lookup"><span data-stu-id="ef6da-163">Monitoring databases (LcsCDR.mdf and QoeMetrics.mdf)</span></span></p>
<p><span data-ttu-id="ef6da-164">Estas bases de datos pueden estar colocadas con otra base de datos de Lync Server o independiente en un servidor de base de datos independiente.</span><span class="sxs-lookup"><span data-stu-id="ef6da-164">These databases may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="ef6da-165">Registros de detalles de llamadas (LcsCDR. MDF) y métricas de la calidad de la experiencia (QoE) (QoeMetrics. MDF).</span><span class="sxs-lookup"><span data-stu-id="ef6da-165">Call detail records (LcsCDR.mdf) and Quality of Experience (QoE) metrics (QoeMetrics.mdf).</span></span></p>
<p><span data-ttu-id="ef6da-166">Los registros de detalles de llamadas son dinámicos y pueden ser esenciales para tu empresa.</span><span class="sxs-lookup"><span data-stu-id="ef6da-166">Call detail records are dynamic and may be critical to your business.</span></span> <span data-ttu-id="ef6da-167">Determine la programación de la copia de seguridad teniendo en cuenta si necesita estos registros por razones normativas.</span><span class="sxs-lookup"><span data-stu-id="ef6da-167">Determine your back up schedule by considering whether you need these records for regulatory reasons.</span></span></p>
<p><span data-ttu-id="ef6da-168">La calidad de la experiencia de la información es dinámica.</span><span class="sxs-lookup"><span data-stu-id="ef6da-168">Quality of experience information is dynamic.</span></span> <span data-ttu-id="ef6da-169">La pérdida de los datos de la calidad de la calidad no es crítica para el funcionamiento de Lync Server, pero puede ser crítico para su empresa.</span><span class="sxs-lookup"><span data-stu-id="ef6da-169">Loss of QoE data is not critical for the operation of Lync Server, but it may be critical to your business.</span></span> <span data-ttu-id="ef6da-170">Determine la programación de la copia de seguridad en función de la importancia de esta información para su organización.</span><span class="sxs-lookup"><span data-stu-id="ef6da-170">Determine your back up schedule based on how critical this information is to your organization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef6da-171">Datos de chat persistente</span><span class="sxs-lookup"><span data-stu-id="ef6da-171">Persistent Chat data</span></span></p></td>
<td><p><span data-ttu-id="ef6da-172">Base de datos de chat persistente (MGD. MDF).</span><span class="sxs-lookup"><span data-stu-id="ef6da-172">Persistent Chat database (mgd.mdf).</span></span></p>
<p><span data-ttu-id="ef6da-173">Esta base de datos puede estar colocada con otra base de datos de Lync Server o independiente en un servidor de base de datos independiente.</span><span class="sxs-lookup"><span data-stu-id="ef6da-173">This database may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="ef6da-174">Los datos de chat persistentes son contenido de chat real que se publican en salones de chat.</span><span class="sxs-lookup"><span data-stu-id="ef6da-174">Persistent Chat Data is actual chat content being posted in chat rooms.</span></span> <span data-ttu-id="ef6da-175">Estos datos son a menudo críticos para la empresa.</span><span class="sxs-lookup"><span data-stu-id="ef6da-175">This data is often business critical.</span></span></p>
<p><span data-ttu-id="ef6da-176">Puede optar por usar la copia de seguridad de SQL Server o exportar la base de datos con el cmdlet <strong>Export-CsPersistentChatData</strong> que se proporciona en Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-176">You can choose to use SQL Server backup, or export the database by using the <strong>Export-CsPersistentChatData</strong> cmdlet that is provided in Lync Server.</span></span> <span data-ttu-id="ef6da-177">Para recuperar los datos, puede importar y restaurar la base de datos hasta el momento de la última copia de seguridad completa, lo que significa que no puede restaurar la base de datos hasta el momento del error.</span><span class="sxs-lookup"><span data-stu-id="ef6da-177">For recovery of the data, you can import and restore the database to the point of the last full backup, which means you cannot restore the database to the point of failure.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="file-store-data-requirements"></a><span data-ttu-id="ef6da-178">Requisitos de datos del almacén de archivos</span><span class="sxs-lookup"><span data-stu-id="ef6da-178">File Store Data Requirements</span></span>

<span data-ttu-id="ef6da-179">En una implementación de Enterprise Edition, el almacén de archivos de Lync Server suele encontrarse en un servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="ef6da-179">In an Enterprise Edition deployment, the Lync Server file store is typically located on a file server.</span></span> <span data-ttu-id="ef6da-180">En una implementación de Standard Edition, el almacén de archivos de Lync Server se encuentra de forma predeterminada en el servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="ef6da-180">In a Standard Edition deployment, the Lync Server file store is located by default on the Standard Edition server.</span></span> <span data-ttu-id="ef6da-181">Normalmente, hay un almacén de archivos de Lync Server compartido para un sitio.</span><span class="sxs-lookup"><span data-stu-id="ef6da-181">Typically, there is one Lync Server file store that is shared for a site.</span></span> <span data-ttu-id="ef6da-182">El almacén de archivos de chat persistente usa el mismo recurso compartido de archivos que el almacén de archivos de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-182">The Persistent Chat file store uses the same file share as the Lync Server file store.</span></span>

<span data-ttu-id="ef6da-183">Las ubicaciones del almacén de archivos se identifican como \\ \\ \\ nombres de recursos compartidos del servidor.</span><span class="sxs-lookup"><span data-stu-id="ef6da-183">File store locations are identified as \\\\server\\share name.</span></span> <span data-ttu-id="ef6da-184">Para buscar las ubicaciones específicas de los almacenes de archivos, abra el generador de topologías y mire en el nodo **almacenes de archivos** .</span><span class="sxs-lookup"><span data-stu-id="ef6da-184">To find the specific locations of your file stores, open Topology Builder and look in the **File stores** node.</span></span>

<span data-ttu-id="ef6da-185">La siguiente tabla identifica los almacenes de archivos que necesita para realizar copias de seguridad y restaurar.</span><span class="sxs-lookup"><span data-stu-id="ef6da-185">The following table identifies the file stores you need to back up and restore.</span></span>

### <a name="file-stores"></a><span data-ttu-id="ef6da-186">Almacenes de archivos</span><span class="sxs-lookup"><span data-stu-id="ef6da-186">File Stores</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef6da-187">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ef6da-187">Type of data</span></span></th>
<th><span data-ttu-id="ef6da-188">Donde se almacena</span><span class="sxs-lookup"><span data-stu-id="ef6da-188">Where stored</span></span></th>
<th><span data-ttu-id="ef6da-189">Descripción/Cuándo hacer una copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="ef6da-189">Description / when to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef6da-190">Almacén de archivos de Lync Server</span><span class="sxs-lookup"><span data-stu-id="ef6da-190">Lync Server file store</span></span></p></td>
<td><p><span data-ttu-id="ef6da-191">Normalmente, en un servidor de archivos, un clúster de archivos o un servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="ef6da-191">Typically on a file server, file cluster, or a Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="ef6da-192">Contenido de la reunión, metadatos de contenido, reuniones registros de cumplimiento, archivos de datos de aplicaciones, archivos de actualización para actualizaciones de dispositivos, archivos de audio para el grupo de respuesta, detener la llamada y aplicaciones de presentación, y archivos publicados en salones de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="ef6da-192">Meeting content, meeting content metadata, meeting compliance logs, application data files, update files for device updates, audio files for Response Group, Call Park, and Announcement applications, and files posted into Persistent Chat rooms.</span></span></p>
<p><span data-ttu-id="ef6da-193">Haga una copia de seguridad de sus copias de seguridad periódicas.</span><span class="sxs-lookup"><span data-stu-id="ef6da-193">Back up with your regular backups.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="additional-backup-requirements"></a><span data-ttu-id="ef6da-194">Requisitos de copia de seguridad adicionales</span><span class="sxs-lookup"><span data-stu-id="ef6da-194">Additional Backup Requirements</span></span>

<span data-ttu-id="ef6da-195">Para garantizar su capacidad de restaurar los servicios de Lync Server en el caso de que se produzca un error, debe hacer una copia de seguridad de algunos componentes necesarios que no forman parte de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-195">To help ensure your ability to restore Lync Server services in the event of a failure, you must back up some necessary components that are not part of Lync Server itself.</span></span> <span data-ttu-id="ef6da-196">Los siguientes componentes no se incluyen en la copia de seguridad ni se restauran como parte del proceso de copia de seguridad y restauración de Lync Server descrito en este documento:</span><span class="sxs-lookup"><span data-stu-id="ef6da-196">The following components are not backed up or restored as part of the Lync Server backup and restoration process described in this document:</span></span>

  - <span data-ttu-id="ef6da-197">**Servicios de dominio de Active Directory**   Debe hacer una copia de seguridad de AD DS con las herramientas de Active Directory al mismo tiempo que realiza una copia de seguridad de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-197">**Active Directory Domain Services**   You need to back up AD DS by using Active Directory tools at the same time that you back up Lync Server.</span></span> <span data-ttu-id="ef6da-198">Es importante mantener AD DS sincronizado con Lync Server, para evitar problemas que se pueden producir cuando Lync Server espera objetos de contacto que no coinciden con los de AD DS.</span><span class="sxs-lookup"><span data-stu-id="ef6da-198">It is important to keep AD DS synchronized with Lync Server, to avoid problems that can occur when Lync Server expects contact objects that do not match those in AD DS.</span></span> <span data-ttu-id="ef6da-199">AD DS almacena los siguientes valores de configuración usados por Lync Server:</span><span class="sxs-lookup"><span data-stu-id="ef6da-199">AD DS stores the following settings which are used by Lync Server:</span></span>
    
      - <span data-ttu-id="ef6da-200">URI del SIP del usuario y otra configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ef6da-200">User SIP URI and other user settings.</span></span>
    
      - <span data-ttu-id="ef6da-201">Objetos de contacto para aplicaciones como el grupo de respuesta y el operador de conferencia.</span><span class="sxs-lookup"><span data-stu-id="ef6da-201">Contact objects for applications such as Response Group and Conferencing Attendant.</span></span>
    
      - <span data-ttu-id="ef6da-202">Puntero al almacén de administración central.</span><span class="sxs-lookup"><span data-stu-id="ef6da-202">A pointer to the Central Management Store.</span></span>
    
      - <span data-ttu-id="ef6da-203">Cuenta de autenticación Kerberos (un objeto de equipo opcional) y grupos de seguridad de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-203">Kerberos Authentication Account (an optional computer object) and Lync Server security groups.</span></span>
    
    <span data-ttu-id="ef6da-204">Para obtener detalles sobre cómo realizar copias de seguridad y restaurar AD DS en Windows Server 2008, consulte "Guía paso a paso de copia de seguridad y recuperación de AD DS" en [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105) .</span><span class="sxs-lookup"><span data-stu-id="ef6da-204">For details about backing up and restoring AD DS in Windows Server 2008, see "AD DS Backup and Recovery Step-by-Step Guide" at [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105).</span></span>

  - <span data-ttu-id="ef6da-205">**Entidad de certificación y certificados**   Use la Directiva de su organización para hacer una copia de seguridad de su entidad de certificación (CA) y certificados.</span><span class="sxs-lookup"><span data-stu-id="ef6da-205">**Certification authority and certificates**   Use your organization's policy for backing up your certification authority (CA) and certificates.</span></span> <span data-ttu-id="ef6da-206">Si utiliza claves privadas exportables, puede hacer una copia de seguridad del certificado y de la clave privada y, a continuación, exportarlos si usa los procedimientos de este documento para restaurar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-206">If you use exportable private keys, you can back up the certificate and the private key, and then export them if you use the procedures in this document to restore Lync Server.</span></span> <span data-ttu-id="ef6da-207">Si usa una CA interna, puede volver a inscribirse si necesita restaurar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-207">If you use an internal CA, you can re-enroll if you need to restore Lync Server.</span></span> <span data-ttu-id="ef6da-208">Es importante que mantenga la clave privada en una ubicación segura donde estará disponible si se produce un error en un equipo.</span><span class="sxs-lookup"><span data-stu-id="ef6da-208">It is important that you retain the private key in a secure location where it will be available if a computer fails.</span></span>

  - <span data-ttu-id="ef6da-209">**System Center Operations Manager**   Si usa Microsoft System Center Operations Manager (anteriormente Microsoft Operations Manager) para supervisar la implementación de Lync Server, puede hacer una copia de seguridad de los datos que crea mientras está supervisando Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-209">**System Center Operations Manager**   If you use Microsoft System Center Operations Manager (formerly Microsoft Operations Manager) to monitor your Lync Server deployment, you can optionally back up the data it creates while it is monitoring Lync Server.</span></span> <span data-ttu-id="ef6da-210">Use el proceso de copia de seguridad estándar de SQL Server para realizar copias de seguridad de los archivos de System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="ef6da-210">Use your standard SQL Server backup process to back up System Center Operations Manager files.</span></span> <span data-ttu-id="ef6da-211">Estos archivos no se restauran durante la recuperación.</span><span class="sxs-lookup"><span data-stu-id="ef6da-211">These files are not restored during recovery.</span></span>

  - <span data-ttu-id="ef6da-212">**Configuración de puerta de enlace de red de telefonía pública conmutada (RTC)**   Si usa dispositivos de voz de empresa o de sucursal con supervivencia, tendrá que realizar una copia de seguridad de la configuración de la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="ef6da-212">**Public switched telephone network (PSTN) gateway configuration**   If you use Enterprise Voice or Survivable Branch Appliances, you need to back up the PSTN gateway configuration.</span></span> <span data-ttu-id="ef6da-213">Consulte a su proveedor para obtener detalles sobre cómo realizar copias de seguridad y restaurar las configuraciones de puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="ef6da-213">See your vendor for details about backing up and restoring PSTN gateway configurations.</span></span>

  - <span data-ttu-id="ef6da-214">**Versiones coexistentes de Lync Server o de Office Communications Server**   Si su implementación de Lync Server 2013 coexiste con Lync Server 2010 o una versión anterior de Office Communications Server, no puede usar los procedimientos de este documento para realizar una copia de seguridad de la versión anterior o restaurarla.</span><span class="sxs-lookup"><span data-stu-id="ef6da-214">**Coexisting versions of Lync Server or Office Communications Server**   If your Lync Server 2013 deployment coexists with Lync Server 2010 or an earlier version of Office Communications Server, you can’t use the procedures in this document for backing up or restoring the earlier version.</span></span> <span data-ttu-id="ef6da-215">En su lugar, debe usar los procedimientos de copia de seguridad y restauración documentados específicamente para su versión anterior.</span><span class="sxs-lookup"><span data-stu-id="ef6da-215">Instead, you must use the backup and restoration procedures documented specifically for your earlier version.</span></span> <span data-ttu-id="ef6da-216">Para obtener detalles sobre cómo realizar copias de seguridad y restaurar Lync Server 2010, consulte [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span><span class="sxs-lookup"><span data-stu-id="ef6da-216">For details about backing up and restoring Lync Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span></span> <span data-ttu-id="ef6da-217">Para obtener más información sobre cómo realizar copias de seguridad y restaurar Microsoft Office Communications Server 2007 R2, consulte [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162) .</span><span class="sxs-lookup"><span data-stu-id="ef6da-217">For details about backing up and restoring Microsoft Office Communications Server 2007 R2, see [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162).</span></span>

  - <span data-ttu-id="ef6da-218">**Información de infraestructura**   Debe realizar una copia de seguridad de la infraestructura, como la configuración del firewall, la configuración del equilibrio de carga, la configuración de los servicios de Internet Information Server (IIS), los registros del sistema de nombres de dominio (DNS) y las direcciones IP, y la configuración del Protocolo de configuración dinámica de host (DHCP).</span><span class="sxs-lookup"><span data-stu-id="ef6da-218">**Infrastructure information**   You need to back up information about your infrastructure, such as your firewall configuration, load balancing configuration, Internet Information Services (IIS) configuration, Domain Name System (DNS) records and IP addresses, and Dynamic Host Configuration Protocol (DHCP) configuration.</span></span> <span data-ttu-id="ef6da-219">Para obtener detalles sobre cómo realizar una copia de seguridad de estos componentes, consulte a sus respectivos proveedores.</span><span class="sxs-lookup"><span data-stu-id="ef6da-219">For details about backing up these components, check with their respective vendors.</span></span>

  - <span data-ttu-id="ef6da-220">**Mensajería unificada de Microsoft Exchange y Exchange (UM)**   Realice una copia de seguridad y restaure Microsoft Exchange y Exchange UM tal como se describe en la documentación de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef6da-220">**Microsoft Exchange and Exchange Unified Messaging (UM)**   Backup and restore Microsoft Exchange and Exchange UM as described in the Microsoft Exchange documentation.</span></span> <span data-ttu-id="ef6da-221">Para obtener detalles sobre cómo realizar copias de seguridad y restaurar Exchange Server 2013, consulte [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384) .</span><span class="sxs-lookup"><span data-stu-id="ef6da-221">For details about backing up and restoring Exchange Server 2013, see [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384).</span></span> <span data-ttu-id="ef6da-222">Para obtener detalles sobre cómo realizar copias de seguridad y restaurar Exchange Server 2010, consulte [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179) .</span><span class="sxs-lookup"><span data-stu-id="ef6da-222">For details about backing up and restoring Exchange Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179).</span></span>
    
    <span data-ttu-id="ef6da-223">Tenga en cuenta que Lync Server 2013 introduce la posibilidad de disponer de listas de contactos de usuarios, fotos de usuarios de alta definición y archivado de datos almacenados en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="ef6da-223">Note that Lync Server 2013 introduces the ability to have user contact lists, high definition user photos, and archiving data stored in Exchange 2013.</span></span> <span data-ttu-id="ef6da-224">Consulte la siguiente lista para ver cómo hacer una copia de seguridad de estos tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="ef6da-224">See the following list to see how to back up these types of data:</span></span>
    
      - <span data-ttu-id="ef6da-225">Se realiza una copia de seguridad de las **fotos de alta definición** como parte de la copia de seguridad de Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-225">**High definition photos** are backed up as part of the Exchange Server backup.</span></span>
    
      - <span data-ttu-id="ef6da-226">El **almacén de contactos unificado** se introdujo en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef6da-226">**Unified contact store** is introduced in Lync Server 2013.</span></span> <span data-ttu-id="ef6da-227">El almacén de contactos unificado permite a los usuarios mantener toda la información de contacto en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="ef6da-227">Unified contact store enables users to keep all their contact information in Exchange 2013.</span></span>
        
        <span data-ttu-id="ef6da-228">Debe asegurarse de que las copias de seguridad están actualizadas para los usuarios en cuanto a si sus contactos de usuario se almacenan en el almacenamiento de contactos unificado o en el servidor back-end de Lync.</span><span class="sxs-lookup"><span data-stu-id="ef6da-228">You should make sure that backups are up-to-date for users in terms of whether their user contacts are stored in the unified contact store or on the Lync Back End Server.</span></span> <span data-ttu-id="ef6da-229">Los siguientes escenarios muestran dónde migrar contactos de usuario al almacén de contactos unificado puede causar problemas para el proceso de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="ef6da-229">The following scenarios illustrate where migrating user contacts to the unified contact store can cause issues for the backup and restore process.</span></span>
        
        <span data-ttu-id="ef6da-230">**Escenario 1:** Los contactos de usuario se migran al almacén de contactos unificado y se realiza una restauración desde una copia de seguridad de Lync Server realizada antes de la migración de los contactos de usuario.</span><span class="sxs-lookup"><span data-stu-id="ef6da-230">**Scenario 1:** User contacts are migrated to the unified contact store, and a restore is performed from a Lync Server backup taken prior to the migration of user contacts.</span></span> <span data-ttu-id="ef6da-231">En este escenario, el usuario tendrá un estado de contactos anticuados durante un día hasta que la tarea de migración de Lync Server comience a migrar los contactos de los usuarios a Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef6da-231">In this scenario, the user will have a state of outdated contacts for up to one day until Lync Server Migration Task begins migrating user contacts to Exchange.</span></span> <span data-ttu-id="ef6da-232">(Tenga en cuenta que, dado que los contactos del usuario se han migrado previamente al almacén de contactos unificado, se usará la información de contacto de Exchange).</span><span class="sxs-lookup"><span data-stu-id="ef6da-232">(Note that because the user contacts were previously migrated to the unified contact store, the Exchange contact information will be used).</span></span> <span data-ttu-id="ef6da-233">No es necesario que intervenga el administrador en este escenario.</span><span class="sxs-lookup"><span data-stu-id="ef6da-233">No administrator intervention is needed in this scenario.</span></span>
        
        <span data-ttu-id="ef6da-234">**Escenario 2:** Los contactos de usuario se almacenaron anteriormente en el almacén de contactos unificados, pero después se deshicieron.</span><span class="sxs-lookup"><span data-stu-id="ef6da-234">**Scenario 2:** User contacts were previously stored in the unified contact store, but then rolled back.</span></span> <span data-ttu-id="ef6da-235">Una restauración se realiza desde una copia de seguridad de Lync Server realizada cuando los contactos del usuario se almacenaron en el almacén de contactos unificado.</span><span class="sxs-lookup"><span data-stu-id="ef6da-235">A restore is performed from a Lync Server backup taken when the user contacts were stored in the unified contact store.</span></span> <span data-ttu-id="ef6da-236">En este escenario, un mensaje de error de `Error: Incorrect Exchange Version` los registros del cliente o del servidor Lyss puede indicar que se trata de un problema.</span><span class="sxs-lookup"><span data-stu-id="ef6da-236">In this scenario, an error message of `Error: Incorrect Exchange Version` in the client or Lyss server logs may indicate this as an issue.</span></span> <span data-ttu-id="ef6da-237">El usuario podrá obtener acceso a su lista de contactos en Lync 2013 directamente desde Exchange, pero el estado del cliente no coincidirá con el estado del servidor de Lync.</span><span class="sxs-lookup"><span data-stu-id="ef6da-237">The user will be able to access their contact list in Lync 2013 directly from Exchange, but client’s state will not match the Lync Server state.</span></span> <span data-ttu-id="ef6da-238">Para corregir este error, un administrador tendrá que ejecutar los cmdlets **Invoke-CsUCSRollback** para los usuarios afectados.</span><span class="sxs-lookup"><span data-stu-id="ef6da-238">To fix this, an administrator will need to run the **Invoke-CsUCSRollback** cmdlets for the affected users.</span></span>
    
      - <span data-ttu-id="ef6da-239">El **archivado de datos** puede almacenarse en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="ef6da-239">**Archiving Data** can be stored in Exchange 2013.</span></span> <span data-ttu-id="ef6da-240">Esta información no es crítica para Lync Server, pero puede ser fundamental para su organización con fines normativos.</span><span class="sxs-lookup"><span data-stu-id="ef6da-240">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="ef6da-241">Si los datos de archivado se almacenan en Exchange y son esenciales para su organización, siga los procedimientos de copia de seguridad y restauración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef6da-241">If archiving data is stored in Exchange and is critical to your organization, then follow Exchange backup and restore procedures.</span></span> <span data-ttu-id="ef6da-242">Tenga en cuenta que los datos de archivado almacenados en Exchange no se pueden volver a mover a Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef6da-242">Note that archiving data stored in Exchange cannot be moved back to Lync Server.</span></span> <span data-ttu-id="ef6da-243">Además, no hay ninguna manera de mover los datos que ya están almacenados en la base de datos de archivado de Lync a Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef6da-243">Additionally, there is no way to move data already stored in the Lync archiving database to Exchange.</span></span>

<span data-ttu-id="ef6da-244"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef6da-244"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

