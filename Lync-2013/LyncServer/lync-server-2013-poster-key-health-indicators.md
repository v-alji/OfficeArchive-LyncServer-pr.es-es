---
title: 'Lync Server 2013: póster: indicadores clave de estado'
description: 'Lync Server 2013: cartel: indicadores clave de estado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Poster: Key Health Indicators'
ms:assetid: 8367dccf-adaa-4a0b-a4ed-bc9570cc5e24
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn593599(v=OCS.15)
ms:contentKeyID: 61084873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9962d1764d5d2c664bb8415261344d9b48c81149
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424240"
---
# <a name="key-health-indicators-in-lync-server-2013"></a><span data-ttu-id="32356-103">Indicadores clave de estado en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32356-103">Key Health Indicators in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32356-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32356-104">

<span> </span></span></span>

<span data-ttu-id="32356-105">_**Última modificación del tema:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="32356-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="32356-106">Este artículo es un complemento de los [indicadores clave de estado: la base para mantener el póster de los servidores de Lync en buen estado](https://go.microsoft.com/fwlink/?linkid=391838) , que puede descargar desde el centro de descarga.</span><span class="sxs-lookup"><span data-stu-id="32356-106">This article is a companion to the [Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers](https://go.microsoft.com/fwlink/?linkid=391838) poster, which you can download from the Download Center.</span></span>

<span data-ttu-id="32356-107">![Póster que describe la solución de problemas con datos de KHI](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Póster que describe la solución de problemas con datos de KHI")</span><span class="sxs-lookup"><span data-stu-id="32356-107">![Poster describing troubleshooting using KHI data](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Poster describing troubleshooting using KHI data")</span></span>

<span data-ttu-id="32356-108">Puede usar este póster para obtener información sobre los indicadores clave de estado (KHIs), los contadores de rendimiento con umbrales destinados a revelar problemas de experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="32356-108">You can use this poster to learn about Key Health Indicators (KHIs), performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="32356-109">La recopilación de datos de KHI suele ser el primer paso para implementar la metodología de calidad de las llamadas (CQM), que se centra en garantizar una experiencia de audio de calidad para los usuarios de Lync.</span><span class="sxs-lookup"><span data-stu-id="32356-109">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="32356-110">Si tienes preguntas sobre cómo usar CQM, puedes enviar tus preguntas a cqmfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="32356-110">If you have questions about how to use CQM, you can submit your questions to cqmfeedback@microsoft.com.</span></span>

<span data-ttu-id="32356-111">En el póster se explican las siguientes áreas:</span><span class="sxs-lookup"><span data-stu-id="32356-111">The poster explains the following areas:</span></span>

  - <span data-ttu-id="32356-112">¿Qué son los indicadores de estado clave?</span><span class="sxs-lookup"><span data-stu-id="32356-112">What are Key Health Indicators?</span></span>

  - <span data-ttu-id="32356-113">Para recopilar datos de KHI</span><span class="sxs-lookup"><span data-stu-id="32356-113">To Collect KHI Data</span></span>

  - <span data-ttu-id="32356-114">Flujo de corrección para todos los roles de servidor</span><span class="sxs-lookup"><span data-stu-id="32356-114">Remediation Flow for all Server Roles</span></span>

  - <span data-ttu-id="32356-115">Glosario</span><span class="sxs-lookup"><span data-stu-id="32356-115">Glossary</span></span>

  - <span data-ttu-id="32356-116">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="32356-116">Front-end Servers</span></span>

  - <span data-ttu-id="32356-117">Servidores SQL back-end</span><span class="sxs-lookup"><span data-stu-id="32356-117">Backend SQL Servers</span></span>

  - <span data-ttu-id="32356-118">Servidores de mediación</span><span class="sxs-lookup"><span data-stu-id="32356-118">Mediation Servers</span></span>

  - <span data-ttu-id="32356-119">Servidores perimetrales</span><span class="sxs-lookup"><span data-stu-id="32356-119">Edge Servers</span></span>

<span id="WhatIs"></span>

<div>

## <a name="what-are-key-health-indicators"></a><span data-ttu-id="32356-120">¿Qué son los indicadores de estado clave?</span><span class="sxs-lookup"><span data-stu-id="32356-120">What are Key Health Indicators?</span></span>

<span data-ttu-id="32356-121">Los indicadores de estado de clave son contadores de rendimiento con umbrales destinados a revelar problemas de experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="32356-121">Key Health Indicators are performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="32356-122">La recopilación de datos de KHI suele ser el primer paso para implementar la metodología de calidad de las llamadas (CQM), que se centra en garantizar una experiencia de audio de calidad para los usuarios de Lync.</span><span class="sxs-lookup"><span data-stu-id="32356-122">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="32356-123">KHIs se usan además de las soluciones de supervisión estándar de Lync (por ejemplo, System Center Operations Manager, transacciones sintéticas, servidor de supervisión) y no en lugar de esas soluciones.</span><span class="sxs-lookup"><span data-stu-id="32356-123">KHIs are used in addition to standard Lync Monitoring Solutions (e.g. System Center Operations Manager, Synthetic Transactions, Monitoring Server) and not instead of those solutions.</span></span>

<span data-ttu-id="32356-124">Recopilar los contadores de rendimiento de KHI y rellenar la hoja de cálculo KHI que acompaña a la guía de redes para crear un cuadro de mandos que le ayudará a determinar el estado del servidor de una implementación de Lync.</span><span class="sxs-lookup"><span data-stu-id="32356-124">Collect the KHI performance counters and populate the KHI spreadsheet accompanying the Networking Guide to produce a scorecard that will help you determine the server health of a Lync deployment.</span></span> <span data-ttu-id="32356-125">Una vez que se haya rellenado, le guiará para reparar el entorno y le dará información adicional a otros participantes.</span><span class="sxs-lookup"><span data-stu-id="32356-125">Once populated, it guides you in repairing the environment and gives additional insight to other stakeholders.</span></span> <span data-ttu-id="32356-126">Evalúe KHIs cada mes e incorpórelo a cualquier proceso operativo en curso de implementación.</span><span class="sxs-lookup"><span data-stu-id="32356-126">Evaluate KHIs on a monthly basis and incorporate them into any deployment’s ongoing operational processes.</span></span>

<span data-ttu-id="32356-127">Descargue la [Guía de redes de Lync Server](https://go.microsoft.com/fwlink/p/?linkid=390677) para ver la lista completa de KHIs y para obtener las hojas de cálculo relacionadas.</span><span class="sxs-lookup"><span data-stu-id="32356-127">Download the [Lync Server Networking Guide](https://go.microsoft.com/fwlink/p/?linkid=390677) to see the full list of KHIs and to get the related spreadsheets.</span></span>

</div>

<span id="ToCollect"></span>

<div>

## <a name="to-collect-khi-data"></a><span data-ttu-id="32356-128">Para recopilar datos de KHI</span><span class="sxs-lookup"><span data-stu-id="32356-128">To Collect KHI Data</span></span>

1.  <span data-ttu-id="32356-129">Ejecute el script KHI que se incluye con la guía de redes de Lync Server en cada servidor de Lync.</span><span class="sxs-lookup"><span data-stu-id="32356-129">Run the KHI script included with the Lync Server Networking Guide on each Lync Server.</span></span> <span data-ttu-id="32356-130">Esto creará un recopilador de datos dentro del monitor de rendimiento y le dará el nombre KHI.</span><span class="sxs-lookup"><span data-stu-id="32356-130">This will create a Data Collector inside of Performance Monitor and name it KHI.</span></span> <span data-ttu-id="32356-131">De forma predeterminada, los datos se sondearán cada 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="32356-131">By default, data will be polled every 15 seconds.</span></span>

2.  <span data-ttu-id="32356-132">Antes de iniciar el día hábil de la empresa, vaya a cada servidor de Lync e inicie el recopilador de datos de KHI.</span><span class="sxs-lookup"><span data-stu-id="32356-132">Before the start of your company's business day, go to each Lync Server and start the KHI Data Collector.</span></span>

3.  <span data-ttu-id="32356-133">Al final de ese día, detenga el recopilador de datos de KHI y copie los datos en una ubicación central.</span><span class="sxs-lookup"><span data-stu-id="32356-133">At the end of that day, stop the KHI Data Collector and copy the data to a central location.</span></span>

4.  <span data-ttu-id="32356-134">Después de usar Monitor de rendimiento para rellenar la hoja de cálculo KHI incluida en la descarga de la guía de redes de Lync Server, compare los resultados con los destinos recomendados.</span><span class="sxs-lookup"><span data-stu-id="32356-134">After using Performance Monitor to fill in the KHI spreadsheet included with the Lync Server Networking Guide download, compare the results to the recommended targets.</span></span>

</div>

<span id="Remidiation"></span>

<div>

## <a name="remediation-flow-for-all-server-roles"></a><span data-ttu-id="32356-135">Flujo de corrección para todos los roles de servidor</span><span class="sxs-lookup"><span data-stu-id="32356-135">Remediation Flow for all Server Roles</span></span>

<span data-ttu-id="32356-136">Para cada servidor de la implementación de Lync, primero Compruebe que el estado del componente y el rendimiento del sistema del servidor están en el nivel deseado o por encima de él.</span><span class="sxs-lookup"><span data-stu-id="32356-136">For each server in your Lync implementation, begin by verifying that the server’s component health and system performance is at or above the desired level.</span></span> <span data-ttu-id="32356-137">Solo después de eso debería consultar los indicadores relacionados con el rol del servidor en la implementación general de Lync.</span><span class="sxs-lookup"><span data-stu-id="32356-137">Only after that should you look at the indicators relating to the server’s role in the overall Lync implementation.</span></span>

<span data-ttu-id="32356-138">Comienza con la recopilación de datos de rendimiento de KHI para todos los servidores.</span><span class="sxs-lookup"><span data-stu-id="32356-138">Begin by collecting KHI Performance Data for all servers.</span></span> <span data-ttu-id="32356-139">Para cada uno de los roles del sistema (los detalles tratados más adelante en este documento) determine si los componentes básicos del sistema cumplen los objetivos recomendados.</span><span class="sxs-lookup"><span data-stu-id="32356-139">For each of the system roles (details discussed later in this document) determine whether the basic system components meet the recommended targets.</span></span> <span data-ttu-id="32356-140">Si no es así, corrija el rendimiento del sistema y vuelva a recopilar datos de KHI y asegúrese de que el estado del sistema antes de ver las métricas específicas de la función del servidor en la implementación de Lync.</span><span class="sxs-lookup"><span data-stu-id="32356-140">If they do not, remediate the system performance then re-collect KHI data and ensure system health before looking at the metrics specific to the server’s role in the Lync implementation.</span></span> <span data-ttu-id="32356-141">El estado del componente para todos los roles se define como sigue:</span><span class="sxs-lookup"><span data-stu-id="32356-141">Component health for all roles is defined as:</span></span>

  - <span data-ttu-id="32356-142">Uso de la CPU \< 80%</span><span class="sxs-lookup"><span data-stu-id="32356-142">CPU Utilization \< 80%</span></span>

  - <span data-ttu-id="32356-143">Promedio de escrituras en disco: \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="32356-143">Avg. Disk Write \< 10 ms</span></span>

  - <span data-ttu-id="32356-144">Disco de lectura promedio: \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="32356-144">Avg. Disk Read \< 10 ms</span></span>

  - <span data-ttu-id="32356-145">Memoria disponible \> 20% de sistema total MB</span><span class="sxs-lookup"><span data-stu-id="32356-145">Available memory \>20% System Total MB</span></span>

  - <span data-ttu-id="32356-146">Longitud de cola de red \< 2</span><span class="sxs-lookup"><span data-stu-id="32356-146">Network Queue Length \< 2</span></span>

  - <span data-ttu-id="32356-147">Paquetes descartados (o fuera) = 0</span><span class="sxs-lookup"><span data-stu-id="32356-147">Discarded Packets (in / out) = 0</span></span>

</div>

<span id="Glossary"></span>

<div>

## <a name="glossary"></a><span data-ttu-id="32356-148">Glosario</span><span class="sxs-lookup"><span data-stu-id="32356-148">Glossary</span></span>

<span data-ttu-id="32356-149">Los siguientes términos y acrónimos se usan en este póster:</span><span class="sxs-lookup"><span data-stu-id="32356-149">The following terms and acronyms are used in this poster:</span></span>

<span data-ttu-id="32356-150">Como la unidad de control de varios puntos de la MCU = uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="32356-150">AS MCU = Application Sharing Multi-point Control Unit</span></span>

<span data-ttu-id="32356-151">CABLE MCU = audio/video MCU</span><span class="sxs-lookup"><span data-stu-id="32356-151">AV MCU = Audio/Video MCU</span></span>

<span data-ttu-id="32356-152">MI MCU = mensajería instantánea MCU</span><span class="sxs-lookup"><span data-stu-id="32356-152">IM MCU = Instant Messaging MCU</span></span>

<span data-ttu-id="32356-153">UCWA = API Web de comunicaciones unificadas</span><span class="sxs-lookup"><span data-stu-id="32356-153">UCWA = Unified Communications Web API</span></span>

<span data-ttu-id="32356-154">Borde AV = recorrido de audio o vídeo vía borde</span><span class="sxs-lookup"><span data-stu-id="32356-154">AV Edge = Traversal of audio/video via edge</span></span>

<span data-ttu-id="32356-155">Autenticación AV = autenticación de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="32356-155">AV Auth = Audio/Video Authentication</span></span>

<span data-ttu-id="32356-156">SIP Stack = contiene la implementación de SIP principal de Lync</span><span class="sxs-lookup"><span data-stu-id="32356-156">SIP Stack = Contains Lync’s core SIP implementation</span></span>

<span data-ttu-id="32356-157">Proxy de datos = usado para conferencias perimetrales</span><span class="sxs-lookup"><span data-stu-id="32356-157">Data Proxy = Used for edge conferencing</span></span>

<span data-ttu-id="32356-158">LySS = servicio de almacenamiento de Lync</span><span class="sxs-lookup"><span data-stu-id="32356-158">LySS = Lync Storage Service</span></span>

</div>

<span id="Front"></span>

<div>

## <a name="front-end-servers"></a><span data-ttu-id="32356-159">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="32356-159">Front-end Servers</span></span>

<span data-ttu-id="32356-160">Los siguientes destinos KHI recomendados son específicos de los servidores front-end, además del estado básico de los componentes:</span><span class="sxs-lookup"><span data-stu-id="32356-160">The following recommended KHI targets are specific to front-end servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32356-161">Área funcional</span><span class="sxs-lookup"><span data-stu-id="32356-161">Functional area</span></span></th>
<th><span data-ttu-id="32356-162">Métricas de destino</span><span class="sxs-lookup"><span data-stu-id="32356-162">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32356-163">AS/AV/MENSAJERÍA INSTANTÁNEA MCU</span><span class="sxs-lookup"><span data-stu-id="32356-163">AS/AV/IM MCU</span></span></p></td>
<td><p><span data-ttu-id="32356-164">Estado de mantenimiento MCU &lt; 2</span><span class="sxs-lookup"><span data-stu-id="32356-164">MCU Health State &lt;2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32356-165">Componentes Web</span><span class="sxs-lookup"><span data-stu-id="32356-165">Web Components</span></span></p></td>
<td><p><span data-ttu-id="32356-166">Tiempo de espera de anuncio de expansión de lista de distribución &lt; 0</span><span class="sxs-lookup"><span data-stu-id="32356-166">Distribution List expansion AD timeouts &lt;0</span></span></p>
<p><span data-ttu-id="32356-167">Errores de ABWQ = 0</span><span class="sxs-lookup"><span data-stu-id="32356-167">ABWQ failures = 0</span></span></p>
<p><span data-ttu-id="32356-168">Errores de LIS = 0</span><span class="sxs-lookup"><span data-stu-id="32356-168">LIS failures = 0</span></span></p>
<p><span data-ttu-id="32356-169">Errores de autenticación &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="32356-169">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="32356-170">Solicitudes ASP.NET V4 rechazadas = 0</span><span class="sxs-lookup"><span data-stu-id="32356-170">ASP.NET v4 Requests Rejected = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32356-171">Pila SIP</span><span class="sxs-lookup"><span data-stu-id="32356-171">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="32356-172">Promedio de procesamiento de mensajes entrantes de &lt; 1 s</span><span class="sxs-lookup"><span data-stu-id="32356-172">Avg. Incoming Message Processing &lt; 1 sec</span></span></p>
<p><span data-ttu-id="32356-173">Respuestas entrantes quitadas &lt; 1/s solicitudes entrantes descartadas &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="32356-173">Incoming Responses Dropped &lt; 1/sec Incoming Requests Dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="32356-174">Latencia de cola &lt; 100 ms</span><span class="sxs-lookup"><span data-stu-id="32356-174">Queue Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="32356-175">Latencia del procedimiento almacenado &lt; 100 ms</span><span class="sxs-lookup"><span data-stu-id="32356-175">Sproc Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="32356-176">Solicitudes limitadas = 0</span><span class="sxs-lookup"><span data-stu-id="32356-176">Throttled Requests = 0</span></span></p>
<p><span data-ttu-id="32356-177">Errores de autenticación &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="32356-177">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="32356-178">Se agotó el tiempo de espera de los mensajes entrantes &lt; 2</span><span class="sxs-lookup"><span data-stu-id="32356-178">Incoming Messages Timed Out &lt; 2</span></span></p>
<p><span data-ttu-id="32356-179">Promedio de mensajes entrantes en espera &lt; 1 s</span><span class="sxs-lookup"><span data-stu-id="32356-179">Avg. Incoming Message Hold &lt; 1 sec</span></span></p>
<p><span data-ttu-id="32356-180">Conexiones controladas por flujo &lt; 2</span><span class="sxs-lookup"><span data-stu-id="32356-180">Flow Controlled Connections &lt; 2</span></span></p>
<p><span data-ttu-id="32356-181">Retraso de cola de salida promedio &lt; 2 s</span><span class="sxs-lookup"><span data-stu-id="32356-181">Avg. Out Queue Delay &lt; 2 sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32356-182">LySS</span><span class="sxs-lookup"><span data-stu-id="32356-182">LySS</span></span></p></td>
<td><p><span data-ttu-id="32356-183">% de espacio usado por la base de BD de servicio de almacenamiento &lt; 80</span><span class="sxs-lookup"><span data-stu-id="32356-183">% of space used by Storage Service DB &lt; 80</span></span></p>
<p><span data-ttu-id="32356-184"># de errores de replicación de réplica = 0</span><span class="sxs-lookup"><span data-stu-id="32356-184"># of replica replication failures = 0</span></span></p>
<p><span data-ttu-id="32356-185"># eventos de pérdida de datos = 0</span><span class="sxs-lookup"><span data-stu-id="32356-185"># of data loss events = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32356-186">SQL</span><span class="sxs-lookup"><span data-stu-id="32356-186">SQL</span></span></p></td>
<td><p><span data-ttu-id="32356-187">Esperanza de vida de la página &gt; 300 s</span><span class="sxs-lookup"><span data-stu-id="32356-187">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="32356-188">Solicitudes de lotes/s &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="32356-188">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="BackEnd"></span>

<div>

## <a name="backend-sql-servers"></a><span data-ttu-id="32356-189">Servidores SQL back-end</span><span class="sxs-lookup"><span data-stu-id="32356-189">Backend SQL Servers</span></span>

<span data-ttu-id="32356-190">Los siguientes destinos KHI recomendados son específicos de los servidores SQL Server además del estado básico de los componentes:</span><span class="sxs-lookup"><span data-stu-id="32356-190">The following recommended KHI targets are specific to SQL servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32356-191">Área funcional</span><span class="sxs-lookup"><span data-stu-id="32356-191">Functional area</span></span></th>
<th><span data-ttu-id="32356-192">Métricas de destino</span><span class="sxs-lookup"><span data-stu-id="32356-192">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32356-193">SQL</span><span class="sxs-lookup"><span data-stu-id="32356-193">SQL</span></span></p></td>
<td><p><span data-ttu-id="32356-194">Esperanza de vida de la página &gt; 300 s</span><span class="sxs-lookup"><span data-stu-id="32356-194">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="32356-195">Solicitudes de lotes/s &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="32356-195">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Mediation"></span>

<div>

## <a name="mediation-servers"></a><span data-ttu-id="32356-196">Servidores de mediación</span><span class="sxs-lookup"><span data-stu-id="32356-196">Mediation Servers</span></span>

<span data-ttu-id="32356-197">Los siguientes destinos KHI recomendados son específicos de los servidores de mediación, además del estado básico de los componentes:</span><span class="sxs-lookup"><span data-stu-id="32356-197">The following recommended KHI targets are specific to mediation servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32356-198">Área funcional</span><span class="sxs-lookup"><span data-stu-id="32356-198">Functional area</span></span></th>
<th><span data-ttu-id="32356-199">Métricas de destino</span><span class="sxs-lookup"><span data-stu-id="32356-199">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32356-200">Servicio servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="32356-200">Mediation Server Service</span></span></p></td>
<td><p><span data-ttu-id="32356-201">Índice de error de llamada de carga = 0</span><span class="sxs-lookup"><span data-stu-id="32356-201">Load Call Failure Index = 0</span></span></p>
<p><span data-ttu-id="32356-202">Llamadas fallidas debido al proxy &lt; 10</span><span class="sxs-lookup"><span data-stu-id="32356-202">Failed Calls due to Proxy &lt;10</span></span></p>
<p><span data-ttu-id="32356-203">Llamadas fallidas debido a la puerta de enlace &lt; 10</span><span class="sxs-lookup"><span data-stu-id="32356-203">Failed Calls due to Gateway &lt;10</span></span></p>
<p><span data-ttu-id="32356-204">Llamadas (dentro o salida) rechazadas = 0</span><span class="sxs-lookup"><span data-stu-id="32356-204">Calls (in or out) rejected = 0</span></span></p>
<p><span data-ttu-id="32356-205">Candidatos a medios ausentes = 0</span><span class="sxs-lookup"><span data-stu-id="32356-205">Media Candidates missing = 0</span></span></p>
<p><span data-ttu-id="32356-206">Errores de comprobación de conectividad de medios = 0</span><span class="sxs-lookup"><span data-stu-id="32356-206">Media Connectivity Check Failures = 0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Edge"></span>

<div>

## <a name="edge-servers"></a><span data-ttu-id="32356-207">Servidores perimetrales</span><span class="sxs-lookup"><span data-stu-id="32356-207">Edge Servers</span></span>

<span data-ttu-id="32356-208">Los siguientes destinos KHI recomendados son específicos de los servidores perimetrales además del estado básico de los componentes:</span><span class="sxs-lookup"><span data-stu-id="32356-208">The following recommended KHI targets are specific to edge servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32356-209">Área funcional</span><span class="sxs-lookup"><span data-stu-id="32356-209">Functional area</span></span></th>
<th><span data-ttu-id="32356-210">Métricas de destino</span><span class="sxs-lookup"><span data-stu-id="32356-210">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32356-211">Autenticación de AV</span><span class="sxs-lookup"><span data-stu-id="32356-211">AV Auth</span></span></p></td>
<td><p><span data-ttu-id="32356-212">Solicitudes erróneas &lt; 20/s</span><span class="sxs-lookup"><span data-stu-id="32356-212">Bad Requests &lt; 20/sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32356-213">Borde AV</span><span class="sxs-lookup"><span data-stu-id="32356-213">AV Edge</span></span></p></td>
<td><p><span data-ttu-id="32356-214">Errores de auth. &lt; 20/s</span><span class="sxs-lookup"><span data-stu-id="32356-214">Auth. Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="32356-215">Errores de asignación de &lt; 20/s</span><span class="sxs-lookup"><span data-stu-id="32356-215">Allocation Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="32356-216">Paquetes descartados &lt; 300/s</span><span class="sxs-lookup"><span data-stu-id="32356-216">Packets Dropped &lt;300/sec</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32356-217">Proxy de datos</span><span class="sxs-lookup"><span data-stu-id="32356-217">Data Proxy</span></span></p></td>
<td><p><span data-ttu-id="32356-218">Conexiones de servidor limitado &lt; 3</span><span class="sxs-lookup"><span data-stu-id="32356-218">Throttled Server connections &lt; 3</span></span></p>
<p><span data-ttu-id="32356-219">El sistema está limitando &lt; 1</span><span class="sxs-lookup"><span data-stu-id="32356-219">System is Throttling &lt;1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32356-220">Pila SIP</span><span class="sxs-lookup"><span data-stu-id="32356-220">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="32356-221">Descartar conexiones por límite &lt; 1</span><span class="sxs-lookup"><span data-stu-id="32356-221">Connections over limit dropped &lt; 1</span></span></p>
<p><span data-ttu-id="32356-222">Se agotó el tiempo de espera de envíos &lt; 10</span><span class="sxs-lookup"><span data-stu-id="32356-222">Sends timed out &lt;10</span></span></p>
<p><span data-ttu-id="32356-223">Conexiones controladas por flujo &lt; 100</span><span class="sxs-lookup"><span data-stu-id="32356-223">Flow Controlled Connections &lt;100</span></span></p>
<p><span data-ttu-id="32356-224">Solicitudes entrantes descartadas &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="32356-224">Incoming requests dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="32356-225">Promedio de procesamiento de mensajes &lt; 3 por segundo</span><span class="sxs-lookup"><span data-stu-id="32356-225">Avg. Message Processing &lt; 3 sec</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="32356-226">Vea también</span><span class="sxs-lookup"><span data-stu-id="32356-226">See Also</span></span>


[<span data-ttu-id="32356-227">Guía de redes de Lync Server</span><span class="sxs-lookup"><span data-stu-id="32356-227">Lync Server Networking Guide</span></span>](https://go.microsoft.com/fwlink/p/?linkid=390677)  
[<span data-ttu-id="32356-228">Indicadores clave de estado: la base para mantener los servidores de Lync en buen estado</span><span class="sxs-lookup"><span data-stu-id="32356-228">Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers</span></span>](https://go.microsoft.com/fwlink/?linkid=391838)  
[<span data-ttu-id="32356-229">Metodología de calidad de llamadas de Lync</span><span class="sxs-lookup"><span data-stu-id="32356-229">Lync Call Quality Methodology</span></span>](https://go.microsoft.com/fwlink/?linkid=391841)  
  

<span data-ttu-id="32356-230"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32356-230"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

