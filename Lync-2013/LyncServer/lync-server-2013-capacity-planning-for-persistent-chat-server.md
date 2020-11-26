---
title: 'Lync Server 2013: Planeación de capacidad para el servidor de chat persistente'
description: 'Lync Server 2013: Planeación de capacidad para el servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Persistent Chat Server
ms:assetid: 7a850cd5-c789-4795-a8ff-083be21ae784
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615006(v=OCS.15)
ms:contentKeyID: 48184580
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f78f9f3666fb272b808ef36da2d3010f451d0079
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435561"
---
# <a name="capacity-planning-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="130c2-103">Planificación de capacidad para el servidor de chat persistente en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="130c2-103">Capacity planning for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="130c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="130c2-104">

<span> </span></span></span>

<span data-ttu-id="130c2-105">_**Última modificación del tema:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="130c2-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="130c2-106">El servidor de chat persistente puede llevar a cabo una conversación en tiempo real con varios usuarios que puede persistir para una recuperación y búsqueda futura.</span><span class="sxs-lookup"><span data-stu-id="130c2-106">Persistent Chat Server can perform multi-user real-time chat that can persist for future retrieval and search.</span></span> <span data-ttu-id="130c2-107">A diferencia de la mensajería instantánea (mi) grupal que se guarda en el buzón de un usuario si está configurado el historial de conversaciones, una sesión de servidor de chat persistente permanece abierta más tiempo y el contenido se guarda en un servidor, junto con los mensajes, archivos, direcciones URL y otros datos que forman parte de una conversación en curso.</span><span class="sxs-lookup"><span data-stu-id="130c2-107">Unlike group instant messaging (IM) that is saved in a user’s mailbox if conversation history is configured, a Persistent Chat Server session stays open longer, and the content is saved on a server, along with the messages, files, URLs, and other data that are part of an ongoing conversation.</span></span>

<span data-ttu-id="130c2-108">El plan de capacidad es una parte importante de la preparación para implementar un servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="130c2-108">Capacity planning is an important part of preparing to deploy Persistent Chat Server.</span></span> <span data-ttu-id="130c2-109">Este tema proporciona detalles sobre las topologías de servidores de chat persistentes compatibles y las tablas de planeación de capacidad que puede usar para determinar la mejor configuración para su implementación.</span><span class="sxs-lookup"><span data-stu-id="130c2-109">This topic provides details about supported Persistent Chat Server topologies and capacity planning tables that you can use to determine the best configuration for your deployment.</span></span> <span data-ttu-id="130c2-110">También se describe cómo administrar mejor las implementaciones del servidor de chat persistentes que requieren mayor capacidad en horas punta.</span><span class="sxs-lookup"><span data-stu-id="130c2-110">It also describes how to best manage Persistent Chat Server deployments that require greater capacity at peak times.</span></span>

<span data-ttu-id="130c2-111">Para descargar el servidor de chat persistente, consulte "servidor de chat persistente de Microsoft Lync Server 13" en [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539) .</span><span class="sxs-lookup"><span data-stu-id="130c2-111">To download Persistent Chat Server, see "Microsoft Lync Server 13 Persistent Chat Server" at [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539).</span></span>

<span data-ttu-id="130c2-112">Para obtener más información sobre cómo instalar el servidor de chat persistente, consulte [instalar el servidor de chat persistente en Lync server 2013](lync-server-2013-installing-persistent-chat-server.md) y [configurar el servidor de chat persistente en Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md) en la documentación de implementación.</span><span class="sxs-lookup"><span data-stu-id="130c2-112">For details about installing Persistent Chat Server, see [Installing Persistent Chat Server in Lync Server 2013](lync-server-2013-installing-persistent-chat-server.md) and [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="130c2-113">Las herramientas de soporte técnico, como la herramienta de planeación de Lync Server, pueden ayudarle aún más para planear la capacidad.</span><span class="sxs-lookup"><span data-stu-id="130c2-113">Support tools, such as Lync Server Planning Tool, can further assist you with capacity planning.</span></span> <span data-ttu-id="130c2-114">Para obtener más información sobre la herramienta de planeación, consulte [comenzar el proceso de planeación de Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="130c2-114">For details about the Planning Tool, see [Beginning the planning process for Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) in the Planning documentation.</span></span>

<div>

## <a name="persistent-chat-server-supported-topologies"></a><span data-ttu-id="130c2-115">Topologías compatibles con el servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="130c2-115">Persistent Chat Server Supported Topologies</span></span>

<span data-ttu-id="130c2-116">Puede implementar un servidor de chat persistente en grupos de un solo servidor o de varios servidores, y con topología de un único grupo o de varios grupos.</span><span class="sxs-lookup"><span data-stu-id="130c2-116">You can deploy Persistent Chat Server in single-server or multiple-server pools, and with single-pool or multiple-pool topology.</span></span>

<span data-ttu-id="130c2-117">También se admite el servidor de chat persistente en el servidor Standard Edition para nuevas implementaciones de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="130c2-117">We now also support Persistent Chat Server on Standard Edition server for new Lync Server 2013 deployments.</span></span> <span data-ttu-id="130c2-118">Sin embargo, el rendimiento y la escala se verán afectados, y dado que no hay una opción de alta disponibilidad para esta nueva implementación, esperamos que use esto principalmente para fines de pruebas de concepto, evaluación, etc.</span><span class="sxs-lookup"><span data-stu-id="130c2-118">However, performance and scale will be affected, and because there is no high availability option for this new deployment, we expect you to use this primarily for the purposes of proof of concept, evaluation, and so on.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="130c2-119">Para obtener más información sobre las dos topologías, vea <A href="lync-server-2013-planning-for-persistent-chat-server.md">planear el servidor de chat persistente en Lync server 2013</A> en la documentación de implementación y en <A href="lync-server-2013-deploying-persistent-chat-server.md">implementar el servidor de chat persistente en Lync Server 2013</A> .</span><span class="sxs-lookup"><span data-stu-id="130c2-119">For additional details about both topologies, see <A href="lync-server-2013-planning-for-persistent-chat-server.md">Planning for Persistent Chat Server in Lync Server 2013</A> in this documentation set and <A href="lync-server-2013-deploying-persistent-chat-server.md">Deploying Persistent Chat Server in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="single-server-topology"></a><span data-ttu-id="130c2-120">Topología Single-Server</span><span class="sxs-lookup"><span data-stu-id="130c2-120">Single-Server Topology</span></span>

<span data-ttu-id="130c2-121">La configuración mínima y la implementación más sencilla para el servidor de chat persistente es una topología única de servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="130c2-121">The minimum configuration and simplest deployment for Persistent Chat Server is a single Persistent Chat Server Front End Server topology.</span></span> <span data-ttu-id="130c2-122">Esta implementación requiere un único servidor que ejecute el servidor de chat persistente (que, opcionalmente, ejecuta el servicio de cumplimiento, si el cumplimiento está habilitado), un servidor que hospede tanto la base de datos de SQL Server como la de la base de datos de SQL Server para almacenar los datos de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="130c2-122">This deployment requires a single server that runs Persistent Chat Server (which optionally runs the Compliance service, if compliance is enabled), a server that hosts both the SQL Server database, and if compliance is required, the SQL Server database to store the compliance data.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="130c2-123">No puede agregar servidores adicionales a un grupo de servidores de chat persistente que se inicie como una implementación de servidor único en el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="130c2-123">You cannot add additional servers to a Persistent Chat Server pool that is started as a single-server deployment in Topology Builder.</span></span> <span data-ttu-id="130c2-124">Le recomendamos que use la topología del grupo de varios servidores, incluso si está usando un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="130c2-124">We recommend using the multiple-server pool topology, even if you’re using a single server.</span></span> <span data-ttu-id="130c2-125">De esta manera, podrás agregar más servidores más adelante, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="130c2-125">This is so that you’ll be able to add more servers later, if it's necessary.</span></span> 


</div>

<span data-ttu-id="130c2-126">La siguiente ilustración muestra todos los componentes obligatorios y opcionales de una topología para un único servidor de usuario de chat persistente con cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="130c2-126">The following figure shows all required and optional components of a topology for a single Persistent Chat Server Front End Server with compliance.</span></span>

<span data-ttu-id="130c2-127">**Servidor único de chat persistente**</span><span class="sxs-lookup"><span data-stu-id="130c2-127">**Single Persistent Chat Server**</span></span>

<span data-ttu-id="130c2-128">![Topología de servidor único con servicio de cumplimiento](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "Topología de servidor único con servicio de cumplimiento")</span><span class="sxs-lookup"><span data-stu-id="130c2-128">![Single server topology with Compliance service](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "Single server topology with Compliance service")</span></span>

</div>

<div>

## <a name="multiple-server-topology"></a><span data-ttu-id="130c2-129">Topología Multiple-Server</span><span class="sxs-lookup"><span data-stu-id="130c2-129">Multiple-Server Topology</span></span>

<span data-ttu-id="130c2-130">Para proporcionar mayor capacidad y confiabilidad, puede implementar una topología de varios servidores, como se describe en [planear el servidor de chat persistente en Lync server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="130c2-130">To provide greater capacity and reliability, you can deploy a multiple-server topology, as described in [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span></span> <span data-ttu-id="130c2-131">La topología de varios servidores puede incluir hasta cuatro equipos activos que ejecutan el servidor de chat persistente (la alta disponibilidad y las configuraciones de recuperación ante desastres permiten hasta ocho, pero solo cuatro pueden estar activos y los cuatro restantes en espera).</span><span class="sxs-lookup"><span data-stu-id="130c2-131">The multiple-server topology can include as many as four active computers running Persistent Chat Server (high availability and disaster recovery configurations will allow up to eight, but only four can be active and the remaining four on standby).</span></span> <span data-ttu-id="130c2-132">Cada servidor puede admitir hasta 20.000 usuarios simultáneos, para un total de 80.000 usuarios simultáneos conectados a un grupo de servidores de chat persistente con 4 servidores.</span><span class="sxs-lookup"><span data-stu-id="130c2-132">Each server can support as many as 20,000 concurrent users, for a total of 80,000 concurrent users connected to a Persistent Chat Server pool with 4 servers.</span></span> <span data-ttu-id="130c2-133">Una topología de varios servidores es la misma que la topología de servidor único, excepto en que varios servidores hospedan un servidor de chat persistente y pueden escalar más alto.</span><span class="sxs-lookup"><span data-stu-id="130c2-133">A multiple-server topology is the same as the single-server topology except that multiple servers host Persistent Chat Server, and can scale higher.</span></span> <span data-ttu-id="130c2-134">Varios equipos que ejecutan el servidor de chat persistente deben residir en el mismo dominio de servicios de dominio de Active Directory que Lync Server y el servicio de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="130c2-134">Multiple computers running Persistent Chat Server should reside in the same Active Directory Domain Services domain as Lync Server and the Compliance service.</span></span>

<span data-ttu-id="130c2-135">La siguiente ilustración muestra todos los componentes de una topología de varios servidores con varios equipos que ejecutan un servidor de chat persistente, el servicio de cumplimiento opcional y una base de datos de cumplimiento independiente.</span><span class="sxs-lookup"><span data-stu-id="130c2-135">The following figure shows all the components of a multiple-server topology with multiple computers running Persistent Chat Server, the optional Compliance service, and a separate compliance database.</span></span>

<span data-ttu-id="130c2-136">**Varios servidores de chat persistentes**</span><span class="sxs-lookup"><span data-stu-id="130c2-136">**Multiple Persistent Chat Servers**</span></span>

<span data-ttu-id="130c2-137">![Topología de varios servidores](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "Topología de varios servidores")</span><span class="sxs-lookup"><span data-stu-id="130c2-137">![Multiple server topology](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "Multiple server topology")</span></span>

<span data-ttu-id="130c2-138">En una implementación de servidor de chat persistente de cuatro servidores, en la que los usuarios de 80.000 pueden iniciar sesión y usar la conversación de forma permanente, la carga se distribuye uniformemente en 20.000 usuarios por servidor.</span><span class="sxs-lookup"><span data-stu-id="130c2-138">In a four-server Persistent Chat Server deployment, where 80,000 users can be simultaneously signed in to and using Persistent Chat, the load is distributed evenly at 20,000 users per server.</span></span> <span data-ttu-id="130c2-139">Si un servidor no está disponible, los usuarios que estén conectados a él perderán el acceso al servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="130c2-139">If one server becomes unavailable, the users who are connected to that server will lose their access to Persistent Chat Server.</span></span> <span data-ttu-id="130c2-140">Los usuarios desconectados se transferirán automáticamente a los servidores restantes hasta que se restaure el servidor que no se encuentra disponible.</span><span class="sxs-lookup"><span data-stu-id="130c2-140">The disconnected users will be automatically transferred to the remaining servers until the unavailable server is restored.</span></span> <span data-ttu-id="130c2-141">En función de la cantidad de tráfico de chat persistente en la red, esta transferencia puede demorar unos minutos o más.</span><span class="sxs-lookup"><span data-stu-id="130c2-141">Depending on the amount of Persistent Chat traffic on the network, this transfer can take a few minutes or longer.</span></span> <span data-ttu-id="130c2-142">Como es posible que cada uno de los servidores restantes aloje hasta 30.000 usuarios, le recomendamos que restaure el servidor no disponible lo antes posible para evitar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="130c2-142">Because each of the remaining servers might be hosting as many as 30,000 users, we recommend that you restore the unavailable server as quickly as possible to avoid performance issues.</span></span> <span data-ttu-id="130c2-143">De lo contrario, puede hacer que otro servidor de chat persistente esté disponible con el generador de topologías o el cmdlet de Windows PowerShell **set-CsPersistentChatActiveServer**.</span><span class="sxs-lookup"><span data-stu-id="130c2-143">Otherwise, you can make another Persistent Chat Server available by using the Topology Builder or the Windows PowerShell cmdlet, **set-CsPersistentChatActiveServer**.</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-server-capacity-planning"></a><span data-ttu-id="130c2-144">Planificación de capacidad del servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="130c2-144">Persistent Chat Server Capacity Planning</span></span>

<span data-ttu-id="130c2-145">Las siguientes tablas pueden ayudarle con la planificación de capacidad de un servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="130c2-145">The following tables can help you with capacity planning for Persistent Chat Server.</span></span> <span data-ttu-id="130c2-146">Modelan cómo afectan las capacidades de capacidad a cambiar la configuración del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="130c2-146">They model how changing various Persistent Chat Server settings affect capacity capabilities.</span></span>

<div>

## <a name="planning-your-maximum-capacity-for-persistent-chat-server"></a><span data-ttu-id="130c2-147">Planificación de su capacidad máxima para el servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="130c2-147">Planning Your Maximum Capacity for Persistent Chat Server</span></span>

<span data-ttu-id="130c2-148">Usa la siguiente tabla de muestra para determinar la cantidad de usuarios que podrás admitir.</span><span class="sxs-lookup"><span data-stu-id="130c2-148">Use the following sample table to determine the number of users you will be able to support.</span></span>

### <a name="persistent-chat-server-pool-maximum-capacity-sample"></a><span data-ttu-id="130c2-149">Muestra de capacidad máxima del grupo de servidores de chat persistente</span><span class="sxs-lookup"><span data-stu-id="130c2-149">Persistent Chat Server pool Maximum Capacity Sample</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="130c2-150">Instancias activas del servicio de chat persistente</span><span class="sxs-lookup"><span data-stu-id="130c2-150">Active Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="130c2-151"><em>4</em></span><span class="sxs-lookup"><span data-stu-id="130c2-151"><em>4</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-152">Instancias del servicio de chat persistentes</span><span class="sxs-lookup"><span data-stu-id="130c2-152">Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="130c2-153"><em>8 (4 debe estar inactivo; solo un máximo de 4 puede estar activo)</em></span><span class="sxs-lookup"><span data-stu-id="130c2-153"><em>8 (4 must be inactive; only a maximum of 4 can be active)</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-154">Usuarios activos conectados</span><span class="sxs-lookup"><span data-stu-id="130c2-154">Active users connected</span></span></p></td>
<td><p><span data-ttu-id="130c2-155"><em>80,000</em></span><span class="sxs-lookup"><span data-stu-id="130c2-155"><em>80,000</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-156">Cantidad total de usuarios aprovisionados</span><span class="sxs-lookup"><span data-stu-id="130c2-156">Total provisioned users</span></span></p></td>
<td><p><span data-ttu-id="130c2-157">150,000</span><span class="sxs-lookup"><span data-stu-id="130c2-157">150,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-158">Cantidad de extremos</span><span class="sxs-lookup"><span data-stu-id="130c2-158">Number of endpoints</span></span></p></td>
<td><p><span data-ttu-id="130c2-159">120,000</span><span class="sxs-lookup"><span data-stu-id="130c2-159">120,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="130c2-160">En el ejemplo anterior, el plan es compatible con el número máximo de usuarios que permite el servidor de chat persistente: cuatro servidores/instancias del servicio de chat persistente (pueden tener cuatro servidores más pasivos con servidor de chat persistente para una alta disponibilidad y recuperación ante desastres) y 20.000 usuarios por servidor, para un total de 80.000 usuarios activos.</span><span class="sxs-lookup"><span data-stu-id="130c2-160">In the preceding sample, the plan is to support the maximum number of users that Persistent Chat Server allows: four servers/instances of the Persistent Chat service (can have four more passive servers running Persistent Chat Server for high availability and disaster recovery) and 20,000 users per server, for a total of 80,000 active users.</span></span>

</div>

<div>

## <a name="capacity-planning-for-managing-persistent-chat-room-access"></a><span data-ttu-id="130c2-161">Planificación de capacidad para administrar el acceso permanente al salón de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-161">Capacity Planning for Managing Persistent Chat Room Access</span></span>

<span data-ttu-id="130c2-162">La siguiente tabla de ejemplo puede ayudarle a planear la administración del acceso permanente al salón de chat en un grupo de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="130c2-162">The following sample table can help you plan for managing Persistent Chat room access in a Persistent Chat Server pool.</span></span>

### <a name="managing-chat-room-access-sample"></a><span data-ttu-id="130c2-163">Ejemplo de administración de acceso al salón de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-163">Managing Chat Room Access Sample</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="130c2-164">Salones de chat pequeños</span><span class="sxs-lookup"><span data-stu-id="130c2-164">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="130c2-165">Salones de chat medianos</span><span class="sxs-lookup"><span data-stu-id="130c2-165">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="130c2-166">Salones de chat grandes</span><span class="sxs-lookup"><span data-stu-id="130c2-166">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="130c2-167">Total</span><span class="sxs-lookup"><span data-stu-id="130c2-167">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="130c2-168">Tamaño de los salones de chat (cantidad de usuarios conectados)</span><span class="sxs-lookup"><span data-stu-id="130c2-168">Size of chat rooms (number of users connected)</span></span></p></td>
<td><p><span data-ttu-id="130c2-169">30 por salón</span><span class="sxs-lookup"><span data-stu-id="130c2-169">30 per room</span></span></p></td>
<td><p><span data-ttu-id="130c2-170">150 por salón</span><span class="sxs-lookup"><span data-stu-id="130c2-170">150 per room</span></span></p></td>
<td><p><span data-ttu-id="130c2-171">16 000 por salón</span><span class="sxs-lookup"><span data-stu-id="130c2-171">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-172">Salones de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-172">Chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-173">32,000</span><span class="sxs-lookup"><span data-stu-id="130c2-173">32,000</span></span></p></td>
<td><p><span data-ttu-id="130c2-174">1,067</span><span class="sxs-lookup"><span data-stu-id="130c2-174">1,067</span></span></p></td>
<td><p><span data-ttu-id="130c2-175">base10</span><span class="sxs-lookup"><span data-stu-id="130c2-175">10</span></span></p></td>
<td><p><span data-ttu-id="130c2-176">33,077</span><span class="sxs-lookup"><span data-stu-id="130c2-176">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-177">% de salones que son auditorios</span><span class="sxs-lookup"><span data-stu-id="130c2-177">% of rooms that are auditorium</span></span></p></td>
<td><p><span data-ttu-id="130c2-178">1 %</span><span class="sxs-lookup"><span data-stu-id="130c2-178">1%</span></span></p></td>
<td><p><span data-ttu-id="130c2-179">1 %</span><span class="sxs-lookup"><span data-stu-id="130c2-179">1%</span></span></p></td>
<td><p><span data-ttu-id="130c2-180">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-180">50%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-181">% de salones que están abiertos</span><span class="sxs-lookup"><span data-stu-id="130c2-181">% of rooms that are open</span></span></p></td>
<td><p><span data-ttu-id="130c2-182">3%</span><span class="sxs-lookup"><span data-stu-id="130c2-182">3%</span></span></p></td>
<td><p><span data-ttu-id="130c2-183">3%</span><span class="sxs-lookup"><span data-stu-id="130c2-183">3%</span></span></p></td>
<td><p><span data-ttu-id="130c2-184">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-184">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-185">Salones abiertos (ninguna pertenencia explícita)</span><span class="sxs-lookup"><span data-stu-id="130c2-185">Open rooms (no explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="130c2-186">960</span><span class="sxs-lookup"><span data-stu-id="130c2-186">960</span></span></p></td>
<td><p><span data-ttu-id="130c2-187">32</span><span class="sxs-lookup"><span data-stu-id="130c2-187">32</span></span></p></td>
<td><p><span data-ttu-id="130c2-188">5</span><span class="sxs-lookup"><span data-stu-id="130c2-188">5</span></span></p></td>
<td><p><span data-ttu-id="130c2-189">997</span><span class="sxs-lookup"><span data-stu-id="130c2-189">997</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-190">Salones no abiertos (salones regulares con pertenencia explícita)</span><span class="sxs-lookup"><span data-stu-id="130c2-190">Non-open rooms (regular rooms with explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="130c2-191">31,040</span><span class="sxs-lookup"><span data-stu-id="130c2-191">31,040</span></span></p></td>
<td><p><span data-ttu-id="130c2-192">1.035</span><span class="sxs-lookup"><span data-stu-id="130c2-192">1.035</span></span></p></td>
<td><p><span data-ttu-id="130c2-193">5</span><span class="sxs-lookup"><span data-stu-id="130c2-193">5</span></span></p></td>
<td><p><span data-ttu-id="130c2-194">32,080</span><span class="sxs-lookup"><span data-stu-id="130c2-194">32,080</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-195">Salones de auditorio (entrada de moderadores adicionales)</span><span class="sxs-lookup"><span data-stu-id="130c2-195">Auditorium rooms (additional presenters entry)</span></span></p></td>
<td><p><span data-ttu-id="130c2-196">,0</span><span class="sxs-lookup"><span data-stu-id="130c2-196">0</span></span></p></td>
<td><p><span data-ttu-id="130c2-197">32</span><span class="sxs-lookup"><span data-stu-id="130c2-197">32</span></span></p></td>
<td><p><span data-ttu-id="130c2-198">5</span><span class="sxs-lookup"><span data-stu-id="130c2-198">5</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-199">Salones administrados por pertenencia directa</span><span class="sxs-lookup"><span data-stu-id="130c2-199">Rooms managed by direct membership</span></span></p></td>
<td><p><span data-ttu-id="130c2-200">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-200">50%</span></span></p></td>
<td><p><span data-ttu-id="130c2-201">10%</span><span class="sxs-lookup"><span data-stu-id="130c2-201">10%</span></span></p></td>
<td><p><span data-ttu-id="130c2-202">0%</span><span class="sxs-lookup"><span data-stu-id="130c2-202">0%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-203">Salones administrados por grupos de usuarios</span><span class="sxs-lookup"><span data-stu-id="130c2-203">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="130c2-204">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-204">50%</span></span></p></td>
<td><p><span data-ttu-id="130c2-205">90%</span><span class="sxs-lookup"><span data-stu-id="130c2-205">90%</span></span></p></td>
<td><p><span data-ttu-id="130c2-206">100%</span><span class="sxs-lookup"><span data-stu-id="130c2-206">100%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-207">Grupos de usuarios en la lista de pertenencia de cada salón de chat para los salones abiertos (no especificado explícitamente)</span><span class="sxs-lookup"><span data-stu-id="130c2-207">User groups in each chat room's membership list for open rooms (not specified explicitly)</span></span></p></td>
<td><p><span data-ttu-id="130c2-208">,0</span><span class="sxs-lookup"><span data-stu-id="130c2-208">0</span></span></p></td>
<td><p><span data-ttu-id="130c2-209">,0</span><span class="sxs-lookup"><span data-stu-id="130c2-209">0</span></span></p></td>
<td><p><span data-ttu-id="130c2-210">,0</span><span class="sxs-lookup"><span data-stu-id="130c2-210">0</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-211">Usuarios en la lista de pertenencia de cada salón de chat para los salones no abiertos</span><span class="sxs-lookup"><span data-stu-id="130c2-211">Users in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-212">0,30</span><span class="sxs-lookup"><span data-stu-id="130c2-212">30</span></span></p></td>
<td><p><span data-ttu-id="130c2-213">150</span><span class="sxs-lookup"><span data-stu-id="130c2-213">150</span></span></p></td>
<td><p><span data-ttu-id="130c2-214">16,000</span><span class="sxs-lookup"><span data-stu-id="130c2-214">16,000</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-215">Grupos de usuarios en la lista de pertenencia de cada salón de chat para los salones no abiertos</span><span class="sxs-lookup"><span data-stu-id="130c2-215">User groups in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-216">3</span><span class="sxs-lookup"><span data-stu-id="130c2-216">3</span></span></p></td>
<td><p><span data-ttu-id="130c2-217">5</span><span class="sxs-lookup"><span data-stu-id="130c2-217">5</span></span></p></td>
<td><p><span data-ttu-id="130c2-218">base10</span><span class="sxs-lookup"><span data-stu-id="130c2-218">10</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-219">Usuarios y grupos de usuarios en la lista del administrador de cada salón de chat (para salones abiertos y no abiertos)</span><span class="sxs-lookup"><span data-stu-id="130c2-219">Users and user groups in each chat room's manager list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="130c2-220">6</span><span class="sxs-lookup"><span data-stu-id="130c2-220">6</span></span></p></td>
<td><p><span data-ttu-id="130c2-221">6</span><span class="sxs-lookup"><span data-stu-id="130c2-221">6</span></span></p></td>
<td><p><span data-ttu-id="130c2-222">6</span><span class="sxs-lookup"><span data-stu-id="130c2-222">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-223">Usuarios y grupos de usuarios en la lista de moderadores de cada salón de chat de auditorio (para salones abiertos y no abiertos)</span><span class="sxs-lookup"><span data-stu-id="130c2-223">Users and user groups in each auditorium chat room's presenters list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="130c2-224">6</span><span class="sxs-lookup"><span data-stu-id="130c2-224">6</span></span></p></td>
<td><p><span data-ttu-id="130c2-225">6</span><span class="sxs-lookup"><span data-stu-id="130c2-225">6</span></span></p></td>
<td><p><span data-ttu-id="130c2-226">6</span><span class="sxs-lookup"><span data-stu-id="130c2-226">6</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-227">Entidades de pertenencia basadas en usuarios en todos los salones no abiertos</span><span class="sxs-lookup"><span data-stu-id="130c2-227">User-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-228">465,600</span><span class="sxs-lookup"><span data-stu-id="130c2-228">465,600</span></span></p></td>
<td><p><span data-ttu-id="130c2-229">15,520</span><span class="sxs-lookup"><span data-stu-id="130c2-229">15,520</span></span></p></td>
<td><p>-</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-230">Entidades de pertenencia basadas en grupos de usuarios en todos los salones no abiertos</span><span class="sxs-lookup"><span data-stu-id="130c2-230">User-group-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-231">46,560</span><span class="sxs-lookup"><span data-stu-id="130c2-231">46,560</span></span></p></td>
<td><p><span data-ttu-id="130c2-232">4656</span><span class="sxs-lookup"><span data-stu-id="130c2-232">4656</span></span></p></td>
<td><p><span data-ttu-id="130c2-233">50</span><span class="sxs-lookup"><span data-stu-id="130c2-233">50</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-234">Entidades basadas en usuarios y grupos de usuarios en todos los salones de chat de auditorio</span><span class="sxs-lookup"><span data-stu-id="130c2-234">Users and user groups based entities across all auditorium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-235">,0</span><span class="sxs-lookup"><span data-stu-id="130c2-235">0</span></span></p></td>
<td><p><span data-ttu-id="130c2-236">192</span><span class="sxs-lookup"><span data-stu-id="130c2-236">192</span></span></p></td>
<td><p><span data-ttu-id="130c2-237">50</span><span class="sxs-lookup"><span data-stu-id="130c2-237">50</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-238">Entidades de administradores basadas en usuarios y grupos de usuarios en todas las listas de administrador de salones de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-238">Users and user groups based manager entities across all chat rooms manager lists</span></span></p></td>
<td><p><span data-ttu-id="130c2-239">192,000</span><span class="sxs-lookup"><span data-stu-id="130c2-239">192,000</span></span></p></td>
<td><p><span data-ttu-id="130c2-240">6,400</span><span class="sxs-lookup"><span data-stu-id="130c2-240">6,400</span></span></p></td>
<td><p><span data-ttu-id="130c2-241">60</span><span class="sxs-lookup"><span data-stu-id="130c2-241">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-242">Usuarios activos por salón de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-242">Active users per chat room</span></span></p></td>
<td><p><span data-ttu-id="130c2-243"><em>0,30</em></span><span class="sxs-lookup"><span data-stu-id="130c2-243"><em>30</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-244"><em>150</em></span><span class="sxs-lookup"><span data-stu-id="130c2-244"><em>150</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-245"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="130c2-245"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-246">Salones de chat por usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-246">Chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-247"><em>2007</em></span><span class="sxs-lookup"><span data-stu-id="130c2-247"><em>12</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-248"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="130c2-248"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-249"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="130c2-249"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-250"><em>apartado</em></span><span class="sxs-lookup"><span data-stu-id="130c2-250"><em>16</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-251">Grupos de usuarios en la lista de pertenencia de cada salón de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-251">User groups in each chat room’s membership list</span></span></p></td>
<td><p><span data-ttu-id="130c2-252"><em>base10</em></span><span class="sxs-lookup"><span data-stu-id="130c2-252"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-253"><em>base10</em></span><span class="sxs-lookup"><span data-stu-id="130c2-253"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-254"><em>4,5</em></span><span class="sxs-lookup"><span data-stu-id="130c2-254"><em>15</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-255">Salones administrados por grupos de usuarios</span><span class="sxs-lookup"><span data-stu-id="130c2-255">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="130c2-256"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="130c2-256"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-257"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="130c2-257"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-258"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="130c2-258"><em>50%</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-259">Entidades de pertenencia basadas en grupos de usuarios en todos los salones de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-259">User-group-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-260">155,200</span><span class="sxs-lookup"><span data-stu-id="130c2-260">155,200</span></span></p></td>
<td><p><span data-ttu-id="130c2-261">5173</span><span class="sxs-lookup"><span data-stu-id="130c2-261">5173</span></span></p></td>
<td><p><span data-ttu-id="130c2-262">68</span><span class="sxs-lookup"><span data-stu-id="130c2-262">68</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-263">Entidades de pertenencia basadas en usuarios en todos los salones de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-263">User-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-264">465,600</span><span class="sxs-lookup"><span data-stu-id="130c2-264">465,600</span></span></p></td>
<td><p><span data-ttu-id="130c2-265">77,600</span><span class="sxs-lookup"><span data-stu-id="130c2-265">77,600</span></span></p></td>
<td><p><span data-ttu-id="130c2-266">72,000</span><span class="sxs-lookup"><span data-stu-id="130c2-266">72,000</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-267">Usuarios y grupos de usuarios en las listas de administradores, moderadores y ámbitos de cada salón de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-267">Users and user groups in each chat room's manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="130c2-268">6</span><span class="sxs-lookup"><span data-stu-id="130c2-268">6</span></span></p></td>
<td><p><span data-ttu-id="130c2-269">6</span><span class="sxs-lookup"><span data-stu-id="130c2-269">6</span></span></p></td>
<td><p><span data-ttu-id="130c2-270">6</span><span class="sxs-lookup"><span data-stu-id="130c2-270">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-271">Usuarios y grupos de usuarios en las listas de administradores, moderadores y ámbitos de todos los salones de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-271">Users and user groups across all chat rooms' manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="130c2-272">192,000</span><span class="sxs-lookup"><span data-stu-id="130c2-272">192,000</span></span></p></td>
<td><p><span data-ttu-id="130c2-273">6400</span><span class="sxs-lookup"><span data-stu-id="130c2-273">6400</span></span></p></td>
<td><p><span data-ttu-id="130c2-274">60</span><span class="sxs-lookup"><span data-stu-id="130c2-274">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-275">Entradas de control de acceso</span><span class="sxs-lookup"><span data-stu-id="130c2-275">Access control entries</span></span></p></td>
<td><p><span data-ttu-id="130c2-276">704,160</span><span class="sxs-lookup"><span data-stu-id="130c2-276">704,160</span></span></p></td>
<td><p><span data-ttu-id="130c2-277">26,768</span><span class="sxs-lookup"><span data-stu-id="130c2-277">26,768</span></span></p></td>
<td><p><span data-ttu-id="130c2-278">160</span><span class="sxs-lookup"><span data-stu-id="130c2-278">160</span></span></p></td>
<td><p><span data-ttu-id="130c2-279">731,088</span><span class="sxs-lookup"><span data-stu-id="130c2-279">731,088</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-280">Máximo de entradas de control de acceso</span><span class="sxs-lookup"><span data-stu-id="130c2-280">Maximum access control entries</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="130c2-281">2,000,000</span><span class="sxs-lookup"><span data-stu-id="130c2-281">2,000,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="130c2-282">En el ejemplo anterior, al implementar los servidores de chat persistentes de acuerdo con las pautas recomendadas, pueden administrar hasta 80.000 usuarios activos en un grupo de cuatro servidores con la compatibilidad habilitada.</span><span class="sxs-lookup"><span data-stu-id="130c2-282">In the preceding sample, when you deploy the Persistent Chat Servers according to the recommended guidelines, they can handle up to 80,000 active users across a four-server pool with compliance enabled.</span></span>

<span data-ttu-id="130c2-283">Esta muestra representa los salones de chat clasificados como pequeños (30 usuarios activos en un momento dado), medianos (150 usuarios activos) y grandes (16 000 usuarios activos).</span><span class="sxs-lookup"><span data-stu-id="130c2-283">This sample shows chat rooms categorized as small (30 active users at any given time), medium (150 active users), and large (16,000 active users).</span></span> <span data-ttu-id="130c2-284">El número de salones de chat con un tamaño determinado se calcula en función del número total de:</span><span class="sxs-lookup"><span data-stu-id="130c2-284">The number of chat rooms of a certain size is computed based on the total number of:</span></span>

  - <span data-ttu-id="130c2-285">Usuarios activos en el sistema</span><span class="sxs-lookup"><span data-stu-id="130c2-285">Active users in the system</span></span>

  - <span data-ttu-id="130c2-286">Usuarios activos en los salones de chat del tamaño correspondiente</span><span class="sxs-lookup"><span data-stu-id="130c2-286">Active users in chat rooms of the given size</span></span>

  - <span data-ttu-id="130c2-287">Salones de chat del tamaño correspondiente a los que se una un solo usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-287">Chat rooms of the given size that a single user joins</span></span>

<span data-ttu-id="130c2-p111">Para cada salón de chat, la tabla de planificación de la capacidad anterior especifica la cantidad de entradas de control de acceso asociadas al salón de chat, incluidas las entradas asignadas directamente al salón de chat. Puedes controlar el acceso a salones de chat individuales al utilizar listas de control de acceso (ACL). También puedes controlar el acceso en cuanto a la categoría. En una ACL, una entrada de control de acceso individual puede corresponder a un grupo de usuarios (por ejemplo, un grupo de seguridad, una lista de distribución o a un solo usuario). Puedes definir las entradas de control de acceso de los administradores, los moderadores y los miembros de los salones de chat.</span><span class="sxs-lookup"><span data-stu-id="130c2-p111">For each chat room, the preceding capacity planning table specifies the number of access control entries that are associated with the chat room, including entries that are assigned directly to the chat room. You can control access to individual chat rooms by using access control lists (ACLs). You can also control access at the category level. In an ACL, an individual access control entry can be either a user group—for example, a security group, a distribution list, or a single user. You can define access control entries for chat room managers, presenters, and members.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="130c2-p112">A la hora de planificar tu estrategia para administrar los salones de chat, ten en cuenta que la cantidad total de entradas de control de acceso permitida es 2 millones. Si las entradas de control de acceso que calcules superan los 2 millones, el rendimiento del servidor puede disminuir en gran medida. Para evitar este problema, siempre que sea posible, asegúrate de que las entradas de control de acceso sean grupos de usuarios, en lugar de usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="130c2-p112">In planning your strategy for managing chat rooms, keep in mind that the total number of allowed access control entries is 2 million. If the calculated access control entries exceed 2 million, server performance could degrade significantly. To avoid this issue, whenever possible, be sure that your access control entries are user groups instead of individual users.</span></span>



</div>

</div>

<div>

## <a name="capacity-planning-for-managing-chat-room-access-by-invitation"></a><span data-ttu-id="130c2-296">Planificación de capacidad para administrar el acceso al salón de chat mediante una invitación</span><span class="sxs-lookup"><span data-stu-id="130c2-296">Capacity Planning for Managing Chat Room Access by Invitation</span></span>

<span data-ttu-id="130c2-297">Puede usar la siguiente tabla de planeación de capacidad para comprender el número de invitaciones que el servidor de chat persistente crea y almacena en la base de datos de chat persistente cuando está configurada para enviar invitaciones.</span><span class="sxs-lookup"><span data-stu-id="130c2-297">You can use the following capacity planning table to understand the number of invitations that Persistent Chat Server creates and stores in the Persistent Chat database when it is configured to send invitations.</span></span> <span data-ttu-id="130c2-298">Para administrar las invitaciones de la categoría, use la página **configuración de categoría de salón de chat** en el panel de control de Lync Server, o bien use el cmdlet de Windows PowerShell **set-csPersistentChatCategory**.</span><span class="sxs-lookup"><span data-stu-id="130c2-298">You manage invitations on the Category by using the **Chat Room Category settings** page in the Lync Server Control Panel, or by using the Windows PowerShell cmdlet, **set-csPersistentChatCategory**.</span></span> <span data-ttu-id="130c2-299">Puede administrar invitaciones en un salón de chat (en función de lo que permita la categoría) mediante la página de **Administración de salas** iniciada desde el cliente Lync, o mediante un cmdlet de Windows PowerShell, **set-csPersistentChatRoom**.</span><span class="sxs-lookup"><span data-stu-id="130c2-299">You can manage invitations on a chat room (in line with what the category allows) by using the **Room Management** page launched from the Lync client, or by using a Windows PowerShell cmdlet, **set-csPersistentChatRoom**.</span></span>

<span data-ttu-id="130c2-300">Los datos de muestra de la siguiente tabla presuponen que, en la página **Configuración de salones de chat** para el 50 % de los salones de chat, la opción **Invitaciones** se ha configurado como **Sí**.</span><span class="sxs-lookup"><span data-stu-id="130c2-300">The sample data in the following table assumes that, on the **Chat room settings** page for 50 percent of all chat rooms, the **Invitations** option is set to **Yes**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="130c2-301">Si el valor calculado para la cantidad de invitaciones que el servidor genera supera 1 millón, el rendimiento del servidor puede disminuir en gran medida.</span><span class="sxs-lookup"><span data-stu-id="130c2-301">If the calculated value for the number of invitations that is generated by the server exceeds 1 million, server performance could degrade significantly.</span></span> <span data-ttu-id="130c2-302">Para evitar este problema, asegúrese de minimizar la cantidad de salones de chat configurados para enviar invitaciones o restringir el número de usuarios que pueden unirse a salones de chat que se han configurado para enviar invitaciones.</span><span class="sxs-lookup"><span data-stu-id="130c2-302">To avoid this issue, be sure that you minimize the number of chat rooms that are configured to send invitations or restrict the number of users who can join chat rooms that have been configured to send invitations.</span></span>



</div>

### <a name="chat-room-access-by-invitation-sample"></a><span data-ttu-id="130c2-303">Acceso a salón de chat por muestra de invitación</span><span class="sxs-lookup"><span data-stu-id="130c2-303">Chat Room Access by Invitation Sample</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="130c2-304">Salones de chat pequeños</span><span class="sxs-lookup"><span data-stu-id="130c2-304">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="130c2-305">Salones de chat medianos</span><span class="sxs-lookup"><span data-stu-id="130c2-305">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="130c2-306">Salones de chat grandes</span><span class="sxs-lookup"><span data-stu-id="130c2-306">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="130c2-307">Total</span><span class="sxs-lookup"><span data-stu-id="130c2-307">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="130c2-308">Usuarios que pueden tener acceso a salones de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-308">Users who can access chat room</span></span></p></td>
<td><p><span data-ttu-id="130c2-309">30 por salón</span><span class="sxs-lookup"><span data-stu-id="130c2-309">30 per room</span></span></p></td>
<td><p><span data-ttu-id="130c2-310">150 por salón</span><span class="sxs-lookup"><span data-stu-id="130c2-310">150 per room</span></span></p></td>
<td><p><span data-ttu-id="130c2-311">16 000 por salón</span><span class="sxs-lookup"><span data-stu-id="130c2-311">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-312">Porcentaje de salones que disponen de invitaciones</span><span class="sxs-lookup"><span data-stu-id="130c2-312">Percentage of rooms that have invitations</span></span></p></td>
<td><p><span data-ttu-id="130c2-313">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-313">50%</span></span></p></td>
<td><p><span data-ttu-id="130c2-314">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-314">50%</span></span></p></td>
<td><p><span data-ttu-id="130c2-315">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-315">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-316">Salones de chat configurados para enviar invitaciones</span><span class="sxs-lookup"><span data-stu-id="130c2-316">Chat rooms configured to send invitations</span></span></p></td>
<td><p><span data-ttu-id="130c2-317"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="130c2-317"><em>16,000</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-318"><em>533</em></span><span class="sxs-lookup"><span data-stu-id="130c2-318"><em>533</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-319"><em>5</em></span><span class="sxs-lookup"><span data-stu-id="130c2-319"><em>5</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-320">Usuarios que pueden acceder al salón de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-320">Users who can access the chat room</span></span></p></td>
<td><p><span data-ttu-id="130c2-321"><em>60</em></span><span class="sxs-lookup"><span data-stu-id="130c2-321"><em>60</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-322"><em>225</em></span><span class="sxs-lookup"><span data-stu-id="130c2-322"><em>225</em></span></span></p></td>
<td><p><span data-ttu-id="130c2-323"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="130c2-323"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-324">Invitaciones generadas por el servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="130c2-324">Invitations generated by Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="130c2-325">960,000</span><span class="sxs-lookup"><span data-stu-id="130c2-325">960,000</span></span></p></td>
<td><p><span data-ttu-id="130c2-326">120,000</span><span class="sxs-lookup"><span data-stu-id="130c2-326">120,000</span></span></p></td>
<td><p><span data-ttu-id="130c2-327">80,000</span><span class="sxs-lookup"><span data-stu-id="130c2-327">80,000</span></span></p></td>
<td><p><span data-ttu-id="130c2-328">1,160,000</span><span class="sxs-lookup"><span data-stu-id="130c2-328">1,160,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-329">Cantidad máxima de invitaciones permitidas</span><span class="sxs-lookup"><span data-stu-id="130c2-329">Maximum allowable number of invitations</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="130c2-330">2,000,000</span><span class="sxs-lookup"><span data-stu-id="130c2-330">2,000,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-331">Modelo 1: Inicio con la cantidad esperada de mensajes por salón por día</span><span class="sxs-lookup"><span data-stu-id="130c2-331">Model 1 - Start with expected number of messages per room per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-332">Tasa de chats por salón (por día)</span><span class="sxs-lookup"><span data-stu-id="130c2-332">Chat Rate Per Room (per day)</span></span></p></td>
<td><p><span data-ttu-id="130c2-333">50</span><span class="sxs-lookup"><span data-stu-id="130c2-333">50</span></span></p></td>
<td><p><span data-ttu-id="130c2-334">500</span><span class="sxs-lookup"><span data-stu-id="130c2-334">500</span></span></p></td>
<td><p><span data-ttu-id="130c2-335">100</span><span class="sxs-lookup"><span data-stu-id="130c2-335">100</span></span></p></td>
<td><p><span data-ttu-id="130c2-336">650</span><span class="sxs-lookup"><span data-stu-id="130c2-336">650</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-337">Tasa de chats (por segundo) en todos los salones</span><span class="sxs-lookup"><span data-stu-id="130c2-337">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-338">55.56</span><span class="sxs-lookup"><span data-stu-id="130c2-338">55.56</span></span></p></td>
<td><p><span data-ttu-id="130c2-339">18.52</span><span class="sxs-lookup"><span data-stu-id="130c2-339">18.52</span></span></p></td>
<td><p><span data-ttu-id="130c2-340">0.03</span><span class="sxs-lookup"><span data-stu-id="130c2-340">0.03</span></span></p></td>
<td><p><span data-ttu-id="130c2-341">74</span><span class="sxs-lookup"><span data-stu-id="130c2-341">74</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-342">Modelo 2: Inicio con la cantidad de mensajes publicados por usuario por día</span><span class="sxs-lookup"><span data-stu-id="130c2-342">Model 2 - Start with number of messages posted per user per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-343">Tasa de chats por usuario por día</span><span class="sxs-lookup"><span data-stu-id="130c2-343">Chat rate per user per day</span></span></p></td>
<td><p><span data-ttu-id="130c2-344">4,5</span><span class="sxs-lookup"><span data-stu-id="130c2-344">15</span></span></p></td>
<td><p><span data-ttu-id="130c2-345">5</span><span class="sxs-lookup"><span data-stu-id="130c2-345">5</span></span></p></td>
<td><p><span data-ttu-id="130c2-346">0.1</span><span class="sxs-lookup"><span data-stu-id="130c2-346">0.1</span></span></p></td>
<td><p><span data-ttu-id="130c2-347">veinte</span><span class="sxs-lookup"><span data-stu-id="130c2-347">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-348">Tasa de chats por salón (por día)</span><span class="sxs-lookup"><span data-stu-id="130c2-348">Chat rate per room (per day)</span></span></p></td>
<td><p><span data-ttu-id="130c2-349">38</span><span class="sxs-lookup"><span data-stu-id="130c2-349">38</span></span></p></td>
<td><p><span data-ttu-id="130c2-350">375</span><span class="sxs-lookup"><span data-stu-id="130c2-350">375</span></span></p></td>
<td><p><span data-ttu-id="130c2-351">800</span><span class="sxs-lookup"><span data-stu-id="130c2-351">800</span></span></p></td>
<td><p><span data-ttu-id="130c2-352">1,213</span><span class="sxs-lookup"><span data-stu-id="130c2-352">1,213</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-353">Tasa de chats (por segundo) en todos los salones</span><span class="sxs-lookup"><span data-stu-id="130c2-353">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-354">41.67</span><span class="sxs-lookup"><span data-stu-id="130c2-354">41.67</span></span></p></td>
<td><p><span data-ttu-id="130c2-355">13.89</span><span class="sxs-lookup"><span data-stu-id="130c2-355">13.89</span></span></p></td>
<td><p><span data-ttu-id="130c2-356">0.28</span><span class="sxs-lookup"><span data-stu-id="130c2-356">0.28</span></span></p></td>
<td><p><span data-ttu-id="130c2-357">56</span><span class="sxs-lookup"><span data-stu-id="130c2-357">56</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="130c2-358">Modelo de usuario de rendimiento del servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="130c2-358">Persistent Chat Server Performance User Model</span></span>

<span data-ttu-id="130c2-359">En la siguiente tabla se describe el modelo de usuario para el servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="130c2-359">The following table describes the user model for Persistent Chat Server.</span></span> <span data-ttu-id="130c2-360">Constituye la base de los requisitos de planificación de la capacidad y representa una organización típica con 80 000 usuarios simultáneos, en cuatro servidores.</span><span class="sxs-lookup"><span data-stu-id="130c2-360">It provides the basis for the capacity planning requirements and represents a typical organization with 80,000 concurrent users on four servers.</span></span>

### <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="130c2-361">Modelo de usuario de rendimiento del servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="130c2-361">Persistent Chat Server Performance User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="130c2-362">Cantidad de usuarios activos conectados</span><span class="sxs-lookup"><span data-stu-id="130c2-362">Number of active users connected</span></span></p></td>
<td><p><span data-ttu-id="130c2-363">80,000</span><span class="sxs-lookup"><span data-stu-id="130c2-363">80,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-364">Número de instancias de servicio del servidor de chat persistentes</span><span class="sxs-lookup"><span data-stu-id="130c2-364">Number of Persistent Chat Server service instances</span></span></p></td>
<td><p><span data-ttu-id="130c2-365">4</span><span class="sxs-lookup"><span data-stu-id="130c2-365">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-366">Tamaño de salones de chat pequeños</span><span class="sxs-lookup"><span data-stu-id="130c2-366">Size of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-367">30 usuarios</span><span class="sxs-lookup"><span data-stu-id="130c2-367">30 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-368">Tamaño de salones de chat medianos</span><span class="sxs-lookup"><span data-stu-id="130c2-368">Size of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-369">150 usuarios</span><span class="sxs-lookup"><span data-stu-id="130c2-369">150 users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-370">Tamaño de salones de chat grandes</span><span class="sxs-lookup"><span data-stu-id="130c2-370">Size of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-371">16 000 usuarios</span><span class="sxs-lookup"><span data-stu-id="130c2-371">16,000 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-372">Cantidad total de salones de chat</span><span class="sxs-lookup"><span data-stu-id="130c2-372">Total number of chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-373">33,077</span><span class="sxs-lookup"><span data-stu-id="130c2-373">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-374">Cantidad de salones de chat pequeños</span><span class="sxs-lookup"><span data-stu-id="130c2-374">Number of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-375">32,000</span><span class="sxs-lookup"><span data-stu-id="130c2-375">32,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-376">Cantidad de salones de chat medianos</span><span class="sxs-lookup"><span data-stu-id="130c2-376">Number of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-377">1,067</span><span class="sxs-lookup"><span data-stu-id="130c2-377">1,067</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-378">Cantidad de salones de chat grandes</span><span class="sxs-lookup"><span data-stu-id="130c2-378">Number of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-379">base10</span><span class="sxs-lookup"><span data-stu-id="130c2-379">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-380">Cantidad total de salones de chat por usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-380">Total number of chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-381">apartado</span><span class="sxs-lookup"><span data-stu-id="130c2-381">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-382">Cantidad de salones de chat pequeños por usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-382">Number of small chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-383">2007</span><span class="sxs-lookup"><span data-stu-id="130c2-383">12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-384">Cantidad de salones de chat medianos por usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-384">Number of medium chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-385">2</span><span class="sxs-lookup"><span data-stu-id="130c2-385">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-386">Cantidad de salones de chat grandes por usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-386">Number of large chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-387">2</span><span class="sxs-lookup"><span data-stu-id="130c2-387">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-388">Cantidad de salones a los que se han unido por usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-388">Number of rooms joined per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-389">veinticuatro</span><span class="sxs-lookup"><span data-stu-id="130c2-389">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-390">Tasa máxima de uniones</span><span class="sxs-lookup"><span data-stu-id="130c2-390">Peak join rate</span></span></p></td>
<td><p><span data-ttu-id="130c2-391">10/segundo</span><span class="sxs-lookup"><span data-stu-id="130c2-391">10/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-392">Tasa de chats total</span><span class="sxs-lookup"><span data-stu-id="130c2-392">Total chat rate</span></span></p></td>
<td><p><span data-ttu-id="130c2-393">24/segundo</span><span class="sxs-lookup"><span data-stu-id="130c2-393">24/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-394">Tasa de chats en salones de chat pequeños</span><span class="sxs-lookup"><span data-stu-id="130c2-394">Chat rate for small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-395">22.22/second</span><span class="sxs-lookup"><span data-stu-id="130c2-395">22.22/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-396">Tasa de chats en salones de chat medianos</span><span class="sxs-lookup"><span data-stu-id="130c2-396">Chat rate for medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-397">1.67/second</span><span class="sxs-lookup"><span data-stu-id="130c2-397">1.67/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-398">Tasa de chats en salones de chat grandes</span><span class="sxs-lookup"><span data-stu-id="130c2-398">Chat rate for large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="130c2-399">~0.15/second</span><span class="sxs-lookup"><span data-stu-id="130c2-399">~0.15/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-400">Porcentaje de salones de chat configurados con invitaciones</span><span class="sxs-lookup"><span data-stu-id="130c2-400">Percentage of chat rooms configured for invitations</span></span></p></td>
<td><p><span data-ttu-id="130c2-401">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-401">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-402">Porcentaje de pertenencia directa</span><span class="sxs-lookup"><span data-stu-id="130c2-402">Percentage of direct memberships</span></span></p></td>
<td><p><span data-ttu-id="130c2-403">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-403">50%</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-404">Porcentaje de pertenencia de grupo</span><span class="sxs-lookup"><span data-stu-id="130c2-404">Percentage of group memberships</span></span></p></td>
<td><p><span data-ttu-id="130c2-405">50%</span><span class="sxs-lookup"><span data-stu-id="130c2-405">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-406">Número promedio de afiliaciones antecesoras en servicios de dominio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="130c2-406">Average number of ancestor affiliations in Active Directory Domain Services</span></span></p></td>
<td><p><span data-ttu-id="130c2-407">100 - 200</span><span class="sxs-lookup"><span data-stu-id="130c2-407">100 - 200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-408">Cantidad de contactos suscritos por usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-408">Number of subscribed contacts per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-409">80</span><span class="sxs-lookup"><span data-stu-id="130c2-409">80</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-410">Cantidad promedio de extremos por usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-410">Average number of endpoints per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-411">1.5</span><span class="sxs-lookup"><span data-stu-id="130c2-411">1.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-412">Cantidad promedio de salones de chat visibles por extremo</span><span class="sxs-lookup"><span data-stu-id="130c2-412">Average number of visible chat rooms per endpoint</span></span></p></td>
<td><p><span data-ttu-id="130c2-413">1.5</span><span class="sxs-lookup"><span data-stu-id="130c2-413">1.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-414">Cantidad promedio de salones de chat visibles por usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-414">Average number of visible chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-415">2,25 (50% para 1 salón y 50% para 2 salones); hasta 6 salones abiertos, uno por monitor</span><span class="sxs-lookup"><span data-stu-id="130c2-415">2.25 (50% for 1 room and 50% for 2 rooms); Up to 6 rooms open, one per monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-416">Cantidad de participantes sondeados por intervalo</span><span class="sxs-lookup"><span data-stu-id="130c2-416">Number of participants polled per interval</span></span></p></td>
<td><p><span data-ttu-id="130c2-417">25 por salón de chat visible</span><span class="sxs-lookup"><span data-stu-id="130c2-417">25 per visible chat room</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-418">Longitud del intervalo de sondeo</span><span class="sxs-lookup"><span data-stu-id="130c2-418">Length of polling interval</span></span></p></td>
<td><p><span data-ttu-id="130c2-419">5 minutos</span><span class="sxs-lookup"><span data-stu-id="130c2-419">5 minutes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-420">Cantidad de participantes sondeados por segundo</span><span class="sxs-lookup"><span data-stu-id="130c2-420">Number of participants polled per second</span></span></p></td>
<td><p><span data-ttu-id="130c2-421">15,000</span><span class="sxs-lookup"><span data-stu-id="130c2-421">15,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130c2-422">Cantidad de cambios de presencia por hora y usuario</span><span class="sxs-lookup"><span data-stu-id="130c2-422">Number of presence changes per hour per user</span></span></p></td>
<td><p><span data-ttu-id="130c2-423">6</span><span class="sxs-lookup"><span data-stu-id="130c2-423">6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130c2-424">Cantidad de cambios de presencia por segundo</span><span class="sxs-lookup"><span data-stu-id="130c2-424">Number of presence changes per second</span></span></p></td>
<td><p><span data-ttu-id="130c2-425">133.33</span><span class="sxs-lookup"><span data-stu-id="130c2-425">133.33</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="130c2-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="130c2-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

