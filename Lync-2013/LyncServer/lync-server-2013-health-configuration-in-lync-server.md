---
title: 'Lync Server 2013: configuración de estado en Lync Server'
description: 'Lync Server 2013: configuración de estado en Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Health configuration in Lync Server 2013
ms:assetid: c00a8c8e-c2d2-4557-8c42-211c7cc96550
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205234(v=OCS.15)
ms:contentKeyID: 48185305
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 999a6d5401cb34382a4120f9255c91c846f72422
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427652"
---
# <a name="health-configuration-in-lync-server-2013"></a><span data-ttu-id="a5534-103">Configuración de mantenimiento de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5534-103">Health configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5534-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5534-104">

<span> </span></span></span>

<span data-ttu-id="a5534-105">_**Última modificación del tema:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="a5534-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="a5534-106">Entre los distintos sitios web, los artículos de Microsoft Knowledge base y las herramientas del kit de recursos de Lync Server, los administradores que encuentren problemas al ejecutar Lync Server nunca están lejos de una forma de resolver esos problemas.</span><span class="sxs-lookup"><span data-stu-id="a5534-106">Between various websites, Microsoft Knowledge Base articles, and Lync Server Resource Kit tools, administrators who encounter problems when running Lync Server are never far from a way to solve those problems.</span></span>

<span data-ttu-id="a5534-107">Obviamente, no hay ninguna manera de garantizar que nunca se produzcan problemas con Lync Server 2013 porque Lync Server puede verse afectado por muchos factores, como el bloqueo de red y los errores de hardware, que el producto no puede controlar.</span><span class="sxs-lookup"><span data-stu-id="a5534-107">Obviously there is no way to guarantee that you will never encounter problems with Lync Server 2013 because Lync Server can be affected by many things—like network crashes and hardware failures—that the product itself cannot control.</span></span> <span data-ttu-id="a5534-108">Al implementar la supervisión de estado, los administradores pueden identificar posibles problemas antes de que se conviertan en problemas reales.</span><span class="sxs-lookup"><span data-stu-id="a5534-108">By implementing health monitoring, administrators can identify potential problems before they turn into actual problems.</span></span> <span data-ttu-id="a5534-109">Por ejemplo, los administradores pueden usar la supervisión de Lync Server para identificar tendencias y tendencias.</span><span class="sxs-lookup"><span data-stu-id="a5534-109">For example, administrators can use Lync Server monitoring to identify trends and tendencies.</span></span> <span data-ttu-id="a5534-110">Por ejemplo, es posible que un aumento sostenido de la cantidad de conferencias de audio y vídeo sugiera una necesidad de añadir capacidad antes de que el sistema se sobrecargue.</span><span class="sxs-lookup"><span data-stu-id="a5534-110">For example, a steady increase in the number of audio/video conferences might suggest a need to add capacity before the system becomes overloaded.</span></span>

<span data-ttu-id="a5534-111">De forma similar, los administradores pueden usar System Center Operations Manager para realizar tareas como emitir alertas en tiempo real cuando se produzcan eventos específicos y ejecutar transacciones sintéticas que prueben proactivamente el sistema.</span><span class="sxs-lookup"><span data-stu-id="a5534-111">In a similar fashion, administrators can use System Center Operations Manager to do such things as issue real-time alerts when specified events occur, and to run synthetic transactions that proactively test the system.</span></span> <span data-ttu-id="a5534-112">Las transacciones sintéticas se usan en Lync Server para comprobar que los usuarios pueden completar correctamente tareas comunes como iniciar sesión en el sistema, intercambiar mensajes instantáneos o hacer llamadas a un teléfono que se encuentra en la red de telefonía pública conmutada (RTC).</span><span class="sxs-lookup"><span data-stu-id="a5534-112">Synthetic transactions are used in Lync Server to verify that users are able to successfully complete common tasks such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="a5534-113">Por ejemplo, la ejecución periódica de estas pruebas puede alertarle de posibles problemas con los usuarios que inicien sesión en Lync Server y le dará la oportunidad de corregir el problema antes de que su equipo de soporte se desborde con llamadas de los usuarios que no pueden establecer una conexión.</span><span class="sxs-lookup"><span data-stu-id="a5534-113">For example, periodically running these tests can alert you to potential problems with users logging on to Lync Server, and give you a chance to correct the problem before your support team is flooded with calls from users unable to make a connection.</span></span> <span data-ttu-id="a5534-114">Al usar System Center Operations Manager para ejecutar estas transacciones sintéticas, los administradores pueden supervisar de forma rutinaria su implementación de Lync Server continuamente durante 24 horas cada día, sin tener que hacer mucho más allá de responder a las alertas que se puedan emitir.</span><span class="sxs-lookup"><span data-stu-id="a5534-114">By using System Center Operations Manager to run these synthetic transactions, administrators can routinely monitor their deployment of Lync Server continuously for 24 hours every day without having to do much of anything beyond responding to any alerts that might be issued.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a5534-115">Para Lync Server 2013, el módulo de administración de System Center Operations Manager también puede detectar problemas "externos" que pueden afectar negativamente a Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a5534-115">For Lync Server 2013, the Management Pack for System Center Operations Manager is also able to detect "external" issues that can adversely affect Lync Server.</span></span> <span data-ttu-id="a5534-116">Por ejemplo, se puede notificar a los administradores si los servicios de información de Internet (IIS) se desconectan, los recursos del sistema en un equipo de Lync Server caen por debajo de una cantidad determinada o un equipo de Lync Server experimenta un error de hardware.</span><span class="sxs-lookup"><span data-stu-id="a5534-116">For example, administrators can be notified if Internet Information Services (IIS) goes offline, system resources on a Lync Server computer fall below a specified amount, or a Lync Server computer experiences a hardware failure.</span></span>



</div>

<span data-ttu-id="a5534-117">La configuración de mantenimiento de Lync Server 2013 se basa en System Center Operations Manager y en el uso de los paquetes de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a5534-117">Health configuration in Lync Server 2013 is built around System Center Operations Manager and the use of Lync Server Management Packs.</span></span> <span data-ttu-id="a5534-118">Estos paquetes de administración incluyen varias características y mejoras nuevas, entre las que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="a5534-118">These Management Packs include a number of new features and enhancements, including:</span></span>

  - <span data-ttu-id="a5534-119">**Disponibilidad de escenario desde cualquier ubicación.**</span><span class="sxs-lookup"><span data-stu-id="a5534-119">**Scenario availability from any location.**</span></span> <span data-ttu-id="a5534-120">El paquete de administración de Lync Server 2010 presentó el concepto de supervisión de la disponibilidad del escenario del usuario final con transacciones sintéticas.</span><span class="sxs-lookup"><span data-stu-id="a5534-120">The Lync Server 2010 Management Pack introduced the concept of monitoring end user scenario availability with synthetic transactions.</span></span> <span data-ttu-id="a5534-121">En Lync Server 2013, estos agentes tienen más transacciones sintéticas y se pueden ejecutar desde una amplia variedad de ubicaciones dentro de la empresa, desde ubicaciones geográficas remotas fuera de la empresa, con dispositivos de sucursales y con implementaciones de Lync Server 2010 para agregar cobertura a implementaciones de borde heredado.</span><span class="sxs-lookup"><span data-stu-id="a5534-121">In Lync Server 2013, these agents have more synthetic transactions and can be run from a variety of locations inside the enterprise, from remote geographic locations outside of the enterprise, against branch office appliances and against Lync Server 2010 deployments to add coverage to legacy Edge deployments.</span></span>

  - <span data-ttu-id="a5534-122">**Registros de transacciones sintéticos.**</span><span class="sxs-lookup"><span data-stu-id="a5534-122">**Synthetic transaction logs.**</span></span> <span data-ttu-id="a5534-123">Cuando se produce un error en una transacción sintética, los administradores tienen acceso a los registros HTML para determinar qué ha fallado.</span><span class="sxs-lookup"><span data-stu-id="a5534-123">When a synthetic transaction fails, administrators have access to HTML logs to help determine what failed.</span></span> <span data-ttu-id="a5534-124">Esto incluye comprender qué acción ha fallado, la latencia de cada acción, la línea de comandos que se usa para ejecutar la prueba y el error encontrado.</span><span class="sxs-lookup"><span data-stu-id="a5534-124">This includes understanding which action failed, the latency of each action, the command-line used to run the test, and the error that was encountered.</span></span>

  - <span data-ttu-id="a5534-125">**Mayor cobertura de la confiabilidad de las llamadas.**</span><span class="sxs-lookup"><span data-stu-id="a5534-125">**Increased call reliability coverage.**</span></span> <span data-ttu-id="a5534-126">El paquete de administración de Lync Server 2010 introdujo alertas de confiabilidad para detectar problemas de conectividad graves que afectan a las llamadas de audio de los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="a5534-126">The Lync Server 2010 Management Pack introduced call reliability alerting to detect severe connectivity issues that affect the audio calls of end users.</span></span> <span data-ttu-id="a5534-127">Los módulos de administración de Lync Server 2013 agregan cobertura para la mensajería instantánea de punto a punto (mi) y otras características de conferencia básicas para maximizar la cobertura y reducir el ruido.</span><span class="sxs-lookup"><span data-stu-id="a5534-127">The Lync Server 2013 Management Packs add coverage for peer-to-peer instant messaging (IM) and other basic conferencing features to maximize coverage while reducing noise.</span></span>

  - <span data-ttu-id="a5534-128">**Supervisión de dependencias.**</span><span class="sxs-lookup"><span data-stu-id="a5534-128">**Dependency monitoring.**</span></span> <span data-ttu-id="a5534-129">Los escenarios de Lync Server pueden fallar debido a una variedad de factores externos como IIS desconectado, recursos de memoria y CPU limitados, y problemas de disco.</span><span class="sxs-lookup"><span data-stu-id="a5534-129">Lync Server scenarios can fail due to a variety of external factors such as IIS being offline, limited CPU and memory resources, and disk issues.</span></span> <span data-ttu-id="a5534-130">Los nuevos paquetes de administración comprueban varias dependencias críticas para garantizar que los administradores sean conscientes de su impacto.</span><span class="sxs-lookup"><span data-stu-id="a5534-130">The new management packs check several critical dependencies to ensure administrators are aware of their impact.</span></span>

  - <span data-ttu-id="a5534-131">**Informes mejorados.**</span><span class="sxs-lookup"><span data-stu-id="a5534-131">**Enhanced reporting.**</span></span> <span data-ttu-id="a5534-132">Un conjunto de informes para ayudar a los administradores a calcular la disponibilidad de escenarios, planear la capacidad y ver qué componentes experimentan la mayoría de los problemas.</span><span class="sxs-lookup"><span data-stu-id="a5534-132">A set of reports to help administrators estimate scenario availability, plan for capacity, and see which components are experiencing the most issues.</span></span>

<span data-ttu-id="a5534-133">Los paquetes de administración también incluyen una variedad de características para ayudar a detectar y diagnosticar proporcionar visibilidad en tiempo real del estado de la implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a5534-133">The Management Packs also include a variety of features to help detect and diagnose provide real-time visibility into the health your Lync Server deployment.</span></span> <span data-ttu-id="a5534-134">Estas características se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a5534-134">These features are listed in the following table.</span></span>

### <a name="management-pack-features"></a><span data-ttu-id="a5534-135">Características del paquete de administración</span><span class="sxs-lookup"><span data-stu-id="a5534-135">Management Pack Features</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5534-136">Característica</span><span class="sxs-lookup"><span data-stu-id="a5534-136">Feature</span></span></th>
<th><span data-ttu-id="a5534-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5534-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5534-138">Transacciones sintéticas</span><span class="sxs-lookup"><span data-stu-id="a5534-138">Synthetic Transactions</span></span></p></td>
<td><p><span data-ttu-id="a5534-139">Cmdlets de Windows PowerShell que se pueden ejecutar desde varias ubicaciones para garantizar que los usuarios finales, como el inicio de sesión, la presencia, la mensajería instantánea y las conferencias, estén disponibles para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="a5534-139">Windows PowerShell cmdlets that can be run from various locations to ensure that end user scenarios such as sign-in, presence, IM, and conferencing are readily available to end users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5534-140">Alertas de confiabilidad de llamadas</span><span class="sxs-lookup"><span data-stu-id="a5534-140">Call Reliability Alerts</span></span></p></td>
<td><p><span data-ttu-id="a5534-141">Consultas de base de datos para registros de detalles de llamadas (CDR).</span><span class="sxs-lookup"><span data-stu-id="a5534-141">Database queries for Call Detail Records (CDR).</span></span> <span data-ttu-id="a5534-142">Estos registros los escriben los servidores front-end para reflejar si los usuarios finales podían conectarse a una llamada o por qué se terminó una llamada.</span><span class="sxs-lookup"><span data-stu-id="a5534-142">These records are written by Front End Servers to reflect whether end users were able to connect to a call or why a call was terminated.</span></span> <span data-ttu-id="a5534-143">Estas consultas tienen como resultado alertas que indican si una amplia variedad de usuarios finales experimentan problemas de conectividad para las llamadas de par a par o para la funcionalidad de conferencia básica.</span><span class="sxs-lookup"><span data-stu-id="a5534-143">These queries result in alerts that indicate when a wide range of end users are experiencing connectivity issues for peer-to-peer calls or basic conferencing functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5534-144">Alertas de calidad multimedia</span><span class="sxs-lookup"><span data-stu-id="a5534-144">Media Quality Alerts</span></span></p></td>
<td><p><span data-ttu-id="a5534-145">Consultas de base de datos que tienen los informes de calidad de la experiencia (QoE) publicados por los clientes al final de cada llamada.</span><span class="sxs-lookup"><span data-stu-id="a5534-145">Database queries that look at Quality of Experience (QoE) reports published by clients at the end of each call.</span></span> <span data-ttu-id="a5534-146">Estas consultas generan alertas que indican escenarios en los que es probable que los usuarios experimenten una calidad de medios deficiente durante las llamadas y conferencias.</span><span class="sxs-lookup"><span data-stu-id="a5534-146">These queries result in alerts that pinpoint scenarios where users are likely to be experiencing poor media quality during calls and conferences.</span></span> <span data-ttu-id="a5534-147">Los datos se basan en métricas clave como la latencia y pérdida de paquetes, métricas que se sabe que contribuyen directamente a la calidad de las llamadas.</span><span class="sxs-lookup"><span data-stu-id="a5534-147">The data is built upon key metrics such as packet latency and loss, metrics that are known to directly contribute to call quality.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5534-148">Estado del componente</span><span class="sxs-lookup"><span data-stu-id="a5534-148">Component Health</span></span></p></td>
<td><p><span data-ttu-id="a5534-149">Los componentes de servidor individuales generan alertas mediante registros de eventos y contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a5534-149">Individual server components raise alerts by using event logs and performance counters.</span></span> <span data-ttu-id="a5534-150">Estas alertas indican condiciones de error que pueden afectar gravemente a uno o más escenarios de usuario final.</span><span class="sxs-lookup"><span data-stu-id="a5534-150">These alerts indicate failure conditions that can severely impact one or more end user scenarios.</span></span> <span data-ttu-id="a5534-151">Estas alertas también pueden indicar diversas condiciones de error, como servicios que no se ejecutan, tarifas elevadas de errores, latencia de mensajes de alta latencia o problemas de conectividad.</span><span class="sxs-lookup"><span data-stu-id="a5534-151">These alerts can also indicate a variety of other failure conditions, including services not running, high failure rates, high message latency, or connectivity issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5534-152">Estado de dependencia</span><span class="sxs-lookup"><span data-stu-id="a5534-152">Dependency Health</span></span></p></td>
<td><p><span data-ttu-id="a5534-153">Pueden producirse errores por una variedad de razones externas.</span><span class="sxs-lookup"><span data-stu-id="a5534-153">Failures can occur for a variety of external reasons.</span></span> <span data-ttu-id="a5534-154">Los paquetes de administración ahora supervisan y recopilan datos para algunas de las dependencias externas críticas que pueden indicar problemas graves, como la disponibilidad de IIS, el uso de CPU y de memoria de servidores y procesos, y las métricas de disco.</span><span class="sxs-lookup"><span data-stu-id="a5534-154">The management packs now monitor and collect data for some of the critical external dependencies that might indicate severe issues, including IIS availability, CPU and memory usage of servers and processes, and disk metrics.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5534-155">Las alertas emitidas por el sistema se han clasificado en tres categorías generales:</span><span class="sxs-lookup"><span data-stu-id="a5534-155">The alerts issued by the system have been classified into three general categories:</span></span>

  - <span data-ttu-id="a5534-156">**Alertas de alta prioridad.**</span><span class="sxs-lookup"><span data-stu-id="a5534-156">**High-priority Alerts.**</span></span> <span data-ttu-id="a5534-157">Estas alertas indican condiciones que provocarán interrupciones de servicio para grupos grandes de usuarios.</span><span class="sxs-lookup"><span data-stu-id="a5534-157">These alerts indicate conditions that will cause service outages for large groups of users.</span></span> <span data-ttu-id="a5534-158">Por ejemplo, un error de un componente en un solo equipo no es una alerta de alta prioridad porque Lync Server 2013 tiene características de alta disponibilidad integradas.</span><span class="sxs-lookup"><span data-stu-id="a5534-158">For example, a component failure on a single machine is not a high-priority alert because Lync Server 2013 has built-in high availability features.</span></span> <span data-ttu-id="a5534-159">En su lugar, las alertas de alta prioridad representan problemas lo suficientemente graves como para reactivar a los administradores durante la noche.</span><span class="sxs-lookup"><span data-stu-id="a5534-159">Instead, high-priority alerts represent problems serious enough “to wake up administrators at night.”</span></span> <span data-ttu-id="a5534-160">Las interrupciones detectadas por transacciones sintéticas y servicios sin conexión (por ejemplo, audioconferencias/videoconferencias) se califican como alertas de alta prioridad.</span><span class="sxs-lookup"><span data-stu-id="a5534-160">Outages detected by synthetic transactions and offline services (for example, audio/video conferencing) qualify as high-priority alerts.</span></span>

  - <span data-ttu-id="a5534-161">**Alertas de prioridad media.**.</span><span class="sxs-lookup"><span data-stu-id="a5534-161">**Medium-priority alerts.**.</span></span> <span data-ttu-id="a5534-162">Estas alertas indican condiciones que afectan a un subconjunto de usuarios o indican una degradación de la calidad de las llamadas.</span><span class="sxs-lookup"><span data-stu-id="a5534-162">These alerts indicate conditions that affect a subset of users or indicate call quality degradation.</span></span> <span data-ttu-id="a5534-163">Esto incluye problemas como errores de componentes, latencia en el establecimiento de la llamada o disminución de la calidad de audio en la llamada.</span><span class="sxs-lookup"><span data-stu-id="a5534-163">That includes problems such as component failures, latency in call establishment, or degraded audio quality in call.</span></span> <span data-ttu-id="a5534-164">Las alertas de esta categoría están con estado e indican el estado actual del problema.</span><span class="sxs-lookup"><span data-stu-id="a5534-164">Alerts in this category are stateful and indicate the current status of the issue.</span></span> <span data-ttu-id="a5534-165">Por ejemplo, supongamos que los tiempos de establecimiento de llamadas superan el umbral de alerta.</span><span class="sxs-lookup"><span data-stu-id="a5534-165">For example, suppose your call establishment times exceed the alert threshold.</span></span> <span data-ttu-id="a5534-166">Si los tiempos de establecimiento de la llamada vuelven a normal, estas alertas se resolverán automáticamente en System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="a5534-166">If call establishment times return to normal, these alerts will be auto-resolved in System Center Operations Manager.</span></span> <span data-ttu-id="a5534-167">La expectativa de estas alertas es que un administrador las verá en el mismo día laborable.</span><span class="sxs-lookup"><span data-stu-id="a5534-167">The expectation for these alerts is that an administrator will look at them on the same business day.</span></span>

  - <span data-ttu-id="a5534-168">**Otras alertas.**</span><span class="sxs-lookup"><span data-stu-id="a5534-168">**Other alerts.**</span></span> <span data-ttu-id="a5534-169">Son alertas de componentes que pueden afectar a un usuario específico o a un subconjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="a5534-169">These are alerts from components that might affect a specific user or subset of users.</span></span> <span data-ttu-id="a5534-170">Por ejemplo, es posible que el servicio de libreta de direcciones no pueda analizar la entrada de Active Directory de un usuario dado.</span><span class="sxs-lookup"><span data-stu-id="a5534-170">For example, perhaps the Address Book service could not parse the Active Directory entry of a given user.</span></span> <span data-ttu-id="a5534-171">La expectativa de estas alertas es que los administradores las recibirán cuando tengan tiempo disponible.</span><span class="sxs-lookup"><span data-stu-id="a5534-171">The expectation for these alerts is that administrators will get to them when they have time available.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a5534-172">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a5534-172">In This Section</span></span>

  - [<span data-ttu-id="a5534-173">Configuración de Lync Server 2013 para que funcione con System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="a5534-173">Configuring Lync Server 2013 to work with System Center Operations Manager</span></span>](lync-server-2013-configuring-lync-server-to-work-with-system-center-operations-manager.md)

  - [<span data-ttu-id="a5534-174">Usar el registro avanzado para transacciones sintéticas en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5534-174">Using rich logging for synthetic transactions in Lync Server 2013</span></span>](lync-server-2013-using-rich-logging-for-synthetic-transactions.md)

  - [<span data-ttu-id="a5534-175">Uso de Microsoft SQL Server 2008 R2 como base de datos de System Center Operations Manager para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5534-175">Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database for Lync Server 2013</span></span>](lync-server-2013-using-microsoft-sql-server-2008-r2-as-your-system-center-operations-manager-database.md)

<span data-ttu-id="a5534-176"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5534-176"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

