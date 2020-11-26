---
title: 'Lync Server 2013: dependencias operativas'
description: 'Lync Server 2013: dependencias operativas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operational dependencies
ms:assetid: 450b6be2-7fb3-47d7-8b0b-c05faa331e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720559(v=OCS.15)
ms:contentKeyID: 63969597
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e240981f5dfded7c27f123c8483794ea3ffedff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445298"
---
# <a name="operational-dependencies-in-lync-server-2013"></a><span data-ttu-id="a921e-103">Dependencias operativas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a921e-103">Operational dependencies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a921e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a921e-104">

<span> </span></span></span>

<span data-ttu-id="a921e-105">_**Última modificación del tema:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="a921e-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="a921e-106">La arquitectura de referencia que se describe en este documento le ayudará a asegurarse de que tiene una implementación de Lync Server 2013 que no solo escala a los requisitos de la organización, sino que está diseñado según las prácticas recomendadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a921e-106">The Reference Architecture discussed in this document will help ensure that you have a Lync Server 2013 deployment that not only scales to the organization’s requirements but is architected as per Microsoft best practices.</span></span> <span data-ttu-id="a921e-107">Asegúrese de que la implementación de Lync Server 2013 es un servicio dinámico y, al igual que cualquier otro servicio de la empresa, aún requiere supervisión y administración proactiva para mantener un alto nivel de disponibilidad de servicio y calidad de servicio para la empresa.</span><span class="sxs-lookup"><span data-stu-id="a921e-107">Be that as it may the Lync Server 2013 implementation is a dynamic service and like any other service in the enterprise still requires monitoring and proactive management to maintain high level of service availability and service quality to the business.</span></span>

<span data-ttu-id="a921e-108">Puesto que Lync Server 2013 se hace profundamente ingranulario en las empresas cotidianas de la organización, es importante que el servicio se administre mediante una administración de nivel de servicio precisa y tangible.</span><span class="sxs-lookup"><span data-stu-id="a921e-108">As Lync Server 2013 becomes deeply ingrained in the organization’s everyday business it is important that the service be managed by accurate and tangible service level management.</span></span> <span data-ttu-id="a921e-109">La arquitectura del sistema de Lync puede ser compleja y muy integrada, y para mantener la administración del nivel de servicio eficaz y establecer SLAs para Lync Server 2013 es fundamental comprender las dependencias del sistema en otras plataformas y servidores.</span><span class="sxs-lookup"><span data-stu-id="a921e-109">The Lync system architecture can become complex and very integrated and in order to maintain effective service level management and establish SLAs for Lync Server 2013 it becomes critical to understand the system’s dependencies on other platforms and servers.</span></span> <span data-ttu-id="a921e-110">Igualmente importante es anotar qué servicios empresariales, como las aplicaciones integradas de voz y comunicaciones, se convierten en dependientes en Lync.</span><span class="sxs-lookup"><span data-stu-id="a921e-110">Equally important is to note which business services, such as voice and UC integrated applications, become dependent on Lync.</span></span>

<span data-ttu-id="a921e-111">Lync Server 2013 debe establecerse con todas las dependencias mencionadas.</span><span class="sxs-lookup"><span data-stu-id="a921e-111">Lync Server 2013 must be established noting all the said dependencies.</span></span> <span data-ttu-id="a921e-112">El mapa de servicio le permitirá formular un SLA entre Lync y su servicio dependiente y proporcionar un lugar de inicio para la negociación de SLA.</span><span class="sxs-lookup"><span data-stu-id="a921e-112">The service map will allow you to formulate a SLA between Lync and its dependent service and provide a starting place for SLA negotiation.</span></span>

<span data-ttu-id="a921e-113">En la siguiente tabla se enumeran los servicios de dependencia típicos para una infraestructura de Lync.</span><span class="sxs-lookup"><span data-stu-id="a921e-113">The following table lists the typical dependency services for a Lync infrastructure.</span></span> <span data-ttu-id="a921e-114">Cada una de estas tecnologías debe tener su propia supervisión proactiva.</span><span class="sxs-lookup"><span data-stu-id="a921e-114">Each of these technologies should have its own proactive monitoring.</span></span>

### <a name="typical-dependency-services"></a><span data-ttu-id="a921e-115">Servicios de dependencia típicos</span><span class="sxs-lookup"><span data-stu-id="a921e-115">Typical dependency services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a921e-116">Servicio de dependencia</span><span class="sxs-lookup"><span data-stu-id="a921e-116">Dependency Service</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a921e-117">Sistemas operativos</span><span class="sxs-lookup"><span data-stu-id="a921e-117">Operating systems</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a921e-118">Hardware de servidor</span><span class="sxs-lookup"><span data-stu-id="a921e-118">Server Hardware</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-119">Active Directory</span><span class="sxs-lookup"><span data-stu-id="a921e-119">Active Directory</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a921e-120">Infraestructura de clave pública</span><span class="sxs-lookup"><span data-stu-id="a921e-120">Public Key Infrastructure</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-121">Servicio de nombres de dominio</span><span class="sxs-lookup"><span data-stu-id="a921e-121">Domain Naming Service</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a921e-122">Servicios de bases de datos</span><span class="sxs-lookup"><span data-stu-id="a921e-122">Database Services</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-123">Servicios de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="a921e-123">Storage Services</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a921e-124">Administración del sistema: supervisión y distribución</span><span class="sxs-lookup"><span data-stu-id="a921e-124">System Management – Monitoring and distribution</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-125">Servicios de seguridad: antivirus</span><span class="sxs-lookup"><span data-stu-id="a921e-125">Security Services - Antivirus</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a921e-126">Infraestructura de red-Internet</span><span class="sxs-lookup"><span data-stu-id="a921e-126">Network Infrastructure - Internet</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-127">Infraestructura de red: interna (LAN/WAN)</span><span class="sxs-lookup"><span data-stu-id="a921e-127">Network Infrastructure – Internal (LAN/WAN)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a921e-128">Infraestructura de telefonía: IP-PBX y puertas de enlace</span><span class="sxs-lookup"><span data-stu-id="a921e-128">Telephony Infrastructure – IP-PBX and Gateways</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-129">Servicios en la nube</span><span class="sxs-lookup"><span data-stu-id="a921e-129">Cloud Services</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a921e-130">Se supone que la organización se ha consolidado en el ejercicio de las funciones básicas de administración del nivel de servicio, como la administración de cambios, incidentes y versiones, según lo prescribe el MOF.</span><span class="sxs-lookup"><span data-stu-id="a921e-130">It is assumed that the organization is operationally mature in exercising basic service level management functions such as change, incident and release management as prescribed by the MOF.</span></span> <span data-ttu-id="a921e-131">Las soluciones de Lync deben ser adoptadas por estas funciones y están sujetas a los mismos procesos de administración operativos.</span><span class="sxs-lookup"><span data-stu-id="a921e-131">The Lync solution should be adopted by these functions and become subject to the same operational management processes.</span></span>

<span data-ttu-id="a921e-132">Partiendo de la información obtenida anteriormente, ahora tenemos una mayor comprensión de lo que puede afectar al servicio Lync en la empresa.</span><span class="sxs-lookup"><span data-stu-id="a921e-132">Building on the information obtained above we now have a greater understanding of what can impact the Lync service in the enterprise.</span></span> <span data-ttu-id="a921e-133">Para garantizar la calidad y disponibilidad del servicio de Lync Server 2013, las siguientes herramientas de supervisión deben acompañar a la implementación de arquitectura de referencia:</span><span class="sxs-lookup"><span data-stu-id="a921e-133">To help ensure Lync Server 2013 service availability and quality, the following monitoring tools must accompany the reference architecture deployment:</span></span>

### <a name="monitoring-tools"></a><span data-ttu-id="a921e-134">Herramientas de supervisión</span><span class="sxs-lookup"><span data-stu-id="a921e-134">Monitoring tools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a921e-135">Componente</span><span class="sxs-lookup"><span data-stu-id="a921e-135">Component</span></span></th>
<th><span data-ttu-id="a921e-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="a921e-136">Description</span></span></th>
<th><span data-ttu-id="a921e-137">Sitio aplicable</span><span class="sxs-lookup"><span data-stu-id="a921e-137">Applicable Site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a921e-138">Servidor de supervisión de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a921e-138">Lync Server 2013 Monitoring Server</span></span></p></td>
<td><p><span data-ttu-id="a921e-139">Implemente al menos un rol de servidor de supervisión de Lync Server 2013 por sitio central y configure la calidad de la experiencia (QoE).</span><span class="sxs-lookup"><span data-stu-id="a921e-139">Deploy at least one Lync Server 2013 Monitoring Server role per Central site and configure Quality of Experience (QoE) Reporting Pack.</span></span></p>
<p><span data-ttu-id="a921e-140">Para obtener más información, consulte la documentación de implementación de Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="a921e-140">Refer to the Lync Server 2013 Deployment documentation for further details:</span></span></p>
<p><span data-ttu-id="a921e-141"><a href="lync-server-2013-deploying-monitoring.md">Implementación de la supervisión en Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a921e-141"><a href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="a921e-142">Sitios centrales</span><span class="sxs-lookup"><span data-stu-id="a921e-142">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="a921e-143">Tethering cada grupo a su instancia más cercana de la función de servidor de supervisión.</span><span class="sxs-lookup"><span data-stu-id="a921e-143">Tether each pool to its nearest instance of the Monitoring Server role.</span></span></p></td>
<td><p><span data-ttu-id="a921e-144">Sitios centrales</span><span class="sxs-lookup"><span data-stu-id="a921e-144">Central sites</span></span></p>
<p><span data-ttu-id="a921e-145">Sitios de sucursales</span><span class="sxs-lookup"><span data-stu-id="a921e-145">Branch sites</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-146">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="a921e-146">System Center Operations Manager 2012</span></span></p></td>
<td><p><span data-ttu-id="a921e-147">System Center Operations Manager 2012 con el módulo de administración de Microsoft Lync Server 2013 (MP) importado.</span><span class="sxs-lookup"><span data-stu-id="a921e-147">System Center Operations Manager 2012 with the Microsoft Lync Server 2013 Management Pack (MP) imported.</span></span></p>
<p><span data-ttu-id="a921e-148">El módulo de administración implementa la instrumentación tradicional basada en el registro de eventos y en el contador de rendimiento, así como la habilitación de la instrumentación recién disponible en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a921e-148">The Management Pack implements traditional Event Log and Performance counter based instrumentation is utilized as well as enabling newly available instrumentation in Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="a921e-149">Sitios centrales</span><span class="sxs-lookup"><span data-stu-id="a921e-149">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="a921e-150">Asegúrese de que el descubrimiento central para descubrir los roles y componentes que es necesario supervisar se completa automáticamente según un script de detección central que lee el documento de topología publicado en la base de datos de administración central.</span><span class="sxs-lookup"><span data-stu-id="a921e-150">Make sure that Central Discovery to discovery of roles and components that need to be monitored are automatically completed based on a central discovery script that reads the topology document published in Central Management Database.</span></span></p></td>
<td><p><span data-ttu-id="a921e-151">Sitio central</span><span class="sxs-lookup"><span data-stu-id="a921e-151">Central Site</span></span></p>
<p><span data-ttu-id="a921e-152">Sitio de sucursal</span><span class="sxs-lookup"><span data-stu-id="a921e-152">Branch Site</span></span></p>
<p><span data-ttu-id="a921e-153">Sitio perimetral</span><span class="sxs-lookup"><span data-stu-id="a921e-153">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="a921e-154">Implemente agentes de System Center Operations Manager 2007 en todos los servidores implementados que ejecuten Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a921e-154">Deploy System Centre Operations Manager 2007 agents to all deployed servers running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="a921e-155">Sitio central</span><span class="sxs-lookup"><span data-stu-id="a921e-155">Central Site</span></span></p>
<p><span data-ttu-id="a921e-156">Sitio de sucursal</span><span class="sxs-lookup"><span data-stu-id="a921e-156">Branch Site</span></span></p>
<p><span data-ttu-id="a921e-157">Sitio perimetral</span><span class="sxs-lookup"><span data-stu-id="a921e-157">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="a921e-158">Asegúrese de que las alertas prioritarias están configuradas para notificaciones:</span><span class="sxs-lookup"><span data-stu-id="a921e-158">Make sure Prioritized Alerts are configured for notification:</span></span></p>
<p><span data-ttu-id="a921e-159">Alertas de prioridad alta</span><span class="sxs-lookup"><span data-stu-id="a921e-159">High Priority Alerts</span></span></p>
<p><span data-ttu-id="a921e-160">Alertas de prioridad media</span><span class="sxs-lookup"><span data-stu-id="a921e-160">Medium Priority Alerts</span></span></p>
<p><span data-ttu-id="a921e-161">Otras alertas.</span><span class="sxs-lookup"><span data-stu-id="a921e-161">Other Alerts.</span></span></p></td>
<td><p><span data-ttu-id="a921e-162">Sitio central</span><span class="sxs-lookup"><span data-stu-id="a921e-162">Central Site</span></span></p>
<p><span data-ttu-id="a921e-163">Sitio de sucursal</span><span class="sxs-lookup"><span data-stu-id="a921e-163">Branch Site</span></span></p>
<p><span data-ttu-id="a921e-164">Sitio perimetral</span><span class="sxs-lookup"><span data-stu-id="a921e-164">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="a921e-165">Configure la supervisión de puertos para su implementación.</span><span class="sxs-lookup"><span data-stu-id="a921e-165">Configure Port monitoring for your deployment.</span></span></p></td>
<td><p><span data-ttu-id="a921e-166">Sitio central</span><span class="sxs-lookup"><span data-stu-id="a921e-166">Central Site</span></span></p>
<p><span data-ttu-id="a921e-167">Sitio de sucursal</span><span class="sxs-lookup"><span data-stu-id="a921e-167">Branch Site</span></span></p>
<p><span data-ttu-id="a921e-168">Sitio perimetral</span><span class="sxs-lookup"><span data-stu-id="a921e-168">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="a921e-169">Configurar la supervisión de URL para la implementación</span><span class="sxs-lookup"><span data-stu-id="a921e-169">Configure URL monitoring for your deployment</span></span></p></td>
<td><p><span data-ttu-id="a921e-170">Sitio central</span><span class="sxs-lookup"><span data-stu-id="a921e-170">Central Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-171">Integración de Lync y System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="a921e-171">Lync and System Center Operations Manager integration</span></span></p></td>
<td><p><span data-ttu-id="a921e-172">Implementar la confiabilidad de las llamadas y la calidad de los medios MonitoringCall la fiabilidad y la supervisión de la calidad de los medios use el equipo servidor de supervisión como nodo de monitor para supervisar la confiabilidad de las llamadas y la calidad de los medios de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a921e-172">Deploy Call Reliability and Media Quality MonitoringCall reliability and media quality monitoring use the Monitoring Server computer as their watcher node to monitor call reliability and media quality of Lync Server.</span></span> <span data-ttu-id="a921e-173">Estas dos características consultan las bases de datos del servidor de supervisión para realizar análisis.</span><span class="sxs-lookup"><span data-stu-id="a921e-173">Both of these features query the Monitoring Server databases to do analysis.</span></span></p></td>
<td><p><span data-ttu-id="a921e-174">Sitio central</span><span class="sxs-lookup"><span data-stu-id="a921e-174">Central Site</span></span></p>
<p><span data-ttu-id="a921e-175">Sitio de sucursal</span><span class="sxs-lookup"><span data-stu-id="a921e-175">Branch Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="a921e-176">Garantizar que los umbrales de advertencia de calidad de medios se hayan configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a921e-176">Ensure Media Quality warning thresholds are accurately configured.</span></span> <span data-ttu-id="a921e-177">En la tabla siguiente se indican los resultados de opinión medios máximos de la red por códec.</span><span class="sxs-lookup"><span data-stu-id="a921e-177">The following table indicates the maximum Network Mean Opinion Scores by Codec.</span></span> <span data-ttu-id="a921e-178">En la producción, estas puntuaciones deben vigilarse durante un período establecido y los umbrales aceptables se deben establecer en función de las puntuaciones de NMOS específicas de la organización.</span><span class="sxs-lookup"><span data-stu-id="a921e-178">In production these scores should be monitored for a set period and acceptable thresholds must be established based on the organization specific NMOS scores.</span></span></p></td>
<td><p><span data-ttu-id="a921e-179">Sitio central</span><span class="sxs-lookup"><span data-stu-id="a921e-179">Central Site</span></span></p>
<p><span data-ttu-id="a921e-180">Sitio de sucursal</span><span class="sxs-lookup"><span data-stu-id="a921e-180">Branch Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-181">Monitor de transacción sintética de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a921e-181">Lync Server 2013 Synthetic Transaction Watcher</span></span></p></td>
<td><p><span data-ttu-id="a921e-182">Implementar un servidor de Lync dedicado para que sea un monitor de transacciones sintéticos.</span><span class="sxs-lookup"><span data-stu-id="a921e-182">Deploy a dedicated Lync Server to be a synthetic transaction watcher.</span></span></p>
<p><span data-ttu-id="a921e-183">Las transacciones sintéticas son cmdlets de Lync Server 2013 de Windows PowerShell que el módulo de administración desencadena automáticamente en un intervalo predefinido.</span><span class="sxs-lookup"><span data-stu-id="a921e-183">Synthetic transactions are Lync Server 2013 Windows PowerShell cmdlets that are automatically triggered by the management pack on a predefined interval.</span></span> <span data-ttu-id="a921e-184">Se ejecutan en un nodo de monitor de transacciones sintéticos, que es un servidor designado por el administrador responsable de detectar y ejecutar STs para cada grupo.</span><span class="sxs-lookup"><span data-stu-id="a921e-184">These are executed on a synthetic transaction watcher node which is an administrator designated server responsible for discovery and execution of STs for each pool.</span></span></p>
<p><span data-ttu-id="a921e-185">No se recomienda usar un servidor de Microsoft Lync Server 2013 existente como nodo de supervisor de transacciones sintéticos.</span><span class="sxs-lookup"><span data-stu-id="a921e-185">We do not recommend that you use an existing Microsoft Lync Server 2013 server as a synthetic transaction watcher node.</span></span> <span data-ttu-id="a921e-186">Esto se debe a los requisitos de uso intensivo de CPU y memoria para ejecutar STs.</span><span class="sxs-lookup"><span data-stu-id="a921e-186">This is due to the high CPU/memory usage requirements for running STs.</span></span> <span data-ttu-id="a921e-187">Use un nuevo equipo servidor (o un servidor virtual) para el nodo Monitor de transacciones sintéticos.</span><span class="sxs-lookup"><span data-stu-id="a921e-187">Use a new server computer (or a virtual server) for the synthetic transaction watcher node.</span></span></p></td>
<td><p><span data-ttu-id="a921e-188">Sitio central</span><span class="sxs-lookup"><span data-stu-id="a921e-188">Central Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="a921e-189">Implementación del nodo de monitor de transacciones sintéticas.</span><span class="sxs-lookup"><span data-stu-id="a921e-189">Deploying synthetic transactions watcher node.</span></span></p>
<p><span data-ttu-id="a921e-190">Consulte el documento MonitoringCS_withSCOM.docx de la documentación de UCTAP Connect.</span><span class="sxs-lookup"><span data-stu-id="a921e-190">Refer to the MonitoringCS_withSCOM.docx document from UCTAP connect documentation.</span></span></p></td>
<td><p><span data-ttu-id="a921e-191">Sitio central</span><span class="sxs-lookup"><span data-stu-id="a921e-191">Central Site</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="maximum-network-mos-scores-per-codec"></a><span data-ttu-id="a921e-192">Puntuaciones de OP de red máxima por códec</span><span class="sxs-lookup"><span data-stu-id="a921e-192">Maximum Network MOS scores per codec</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a921e-193">Escenario</span><span class="sxs-lookup"><span data-stu-id="a921e-193">Scenario</span></span></th>
<th><span data-ttu-id="a921e-194">Códec</span><span class="sxs-lookup"><span data-stu-id="a921e-194">Codec</span></span></th>
<th><span data-ttu-id="a921e-195">NMOS máx</span><span class="sxs-lookup"><span data-stu-id="a921e-195">Max NMOS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a921e-196">UC-llamadas UC</span><span class="sxs-lookup"><span data-stu-id="a921e-196">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="a921e-197">RTAudio WB</span><span class="sxs-lookup"><span data-stu-id="a921e-197">RTAudio WB</span></span></p></td>
<td><p><span data-ttu-id="a921e-198">4,10</span><span class="sxs-lookup"><span data-stu-id="a921e-198">4.10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a921e-199">UC-llamadas UC</span><span class="sxs-lookup"><span data-stu-id="a921e-199">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="a921e-200">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="a921e-200">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="a921e-201">2,95</span><span class="sxs-lookup"><span data-stu-id="a921e-201">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-202">Llamada de conferencia</span><span class="sxs-lookup"><span data-stu-id="a921e-202">Conference call</span></span></p></td>
<td><p><span data-ttu-id="a921e-203">Siren</span><span class="sxs-lookup"><span data-stu-id="a921e-203">Siren</span></span></p></td>
<td><p><span data-ttu-id="a921e-204">3,72</span><span class="sxs-lookup"><span data-stu-id="a921e-204">3.72</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a921e-205">UC-llamada RTC</span><span class="sxs-lookup"><span data-stu-id="a921e-205">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="a921e-206">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="a921e-206">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="a921e-207">2,95</span><span class="sxs-lookup"><span data-stu-id="a921e-207">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a921e-208">UC-llamada RTC</span><span class="sxs-lookup"><span data-stu-id="a921e-208">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="a921e-209">G-711</span><span class="sxs-lookup"><span data-stu-id="a921e-209">G-711</span></span></p></td>
<td><p><span data-ttu-id="a921e-210">3,61</span><span class="sxs-lookup"><span data-stu-id="a921e-210">3.61</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a921e-211">Antes y después de las actividades de supervisión proactivas anteriores, las tareas de mantenimiento deben ejecutarse para sitios centrales, perimetrales y de sucursales en una periodicidad diaria, semanal y mensual, según se define en la guía de operaciones de Lync RA.</span><span class="sxs-lookup"><span data-stu-id="a921e-211">Over and above the previous pro-active monitoring activities, maintenance tasks should be executed for Central, Edge and Branch sites on a recurring daily, weekly and monthly basis as defined in the Lync RA Operations Guide.</span></span>

<span data-ttu-id="a921e-212"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a921e-212"></div>

<span> </span>

</div>

</div>

</span></span></div>

