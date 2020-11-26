---
title: 'Lync Server 2013: puertos y protocolos para servidores internos'
description: 'Lync Server 2013: puertos y protocolos para servidores internos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Ports and protocols for internal servers
ms:assetid: c94063f1-e802-4a61-be90-022fc185335e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398833(v=OCS.15)
ms:contentKeyID: 48185402
ms.date: 04/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7d8f12c78c5dec5caacaeb1156f4d228b7cd591
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424250"
---
# <a name="ports-and-protocols-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="8ef6c-103">Puertos y protocolos para servidores internos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ef6c-103">Ports and protocols for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ef6c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ef6c-104">

<span> </span></span></span>

<span data-ttu-id="8ef6c-105">_**Última modificación del tema:** 2016-04-06_</span><span class="sxs-lookup"><span data-stu-id="8ef6c-105">_**Topic Last Modified:** 2016-04-06_</span></span>

<span data-ttu-id="8ef6c-106">En esta sección se resumen los puertos y protocolos usados por servidores, equilibradores de carga y clientes en una implementación de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-106">This section summarizes the ports and protocols used by servers, load balancers, and clients in a Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8ef6c-107">Los clientes de Lync y Communicator, cuando participan en una sola comunicación, se suelen denominar de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-107">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="8ef6c-108">Técnicamente, los dos clientes se comunican en una conversación de una en una, con la unidad de control multipunto de mensajería instantánea (IMMCU) en el medio.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-108">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="8ef6c-109">El IMMCU es un componente de servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-109">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="8ef6c-110">La colocación de IMMCU en el flujo de trabajo de comunicaciones requerido permite la grabación de detalles de llamadas y otras características que permite el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-110">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="8ef6c-111">La comunicación es de un puerto de origen dinámico en el cliente al puerto del servidor front-end TLS/TCP/5061 (asumiendo el uso de la seguridad de la capa de transporte recomendada).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-111">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="8ef6c-112">Por diseño, la comunicación de punto a punto (así como la de mensajería instantánea de varios participantes) solo es posible cuando Lync Server y IMMCU está activo y disponible.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-112">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="8ef6c-113">Detalles de protocolo y puerto</span><span class="sxs-lookup"><span data-stu-id="8ef6c-113">Port and Protocol Details</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8ef6c-114">El Firewall de Windows debe estar ejecutándose antes de iniciar los servicios de Lync Server en un servidor, porque es cuando Lync Server abre los puertos necesarios en el firewall.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-114">Windows Firewall must be running before you start the Lync Server services on a server, because that is when Lync Server opens the required ports in the firewall.</span></span>



</div>

<span data-ttu-id="8ef6c-115">Para obtener más información sobre la configuración del firewall para los componentes de Edge, consulte [determinar el firewall externo a/V y los requisitos de puerto para Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-115">For details about firewall configuration for edge components, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

<span data-ttu-id="8ef6c-116">En la tabla siguiente se enumeran los puertos que debe abrir en cada rol del servidor interno.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-116">The following table lists the ports that need to be open on each internal server role.</span></span>

### <a name="required-server-ports-by-server-role"></a><span data-ttu-id="8ef6c-117">Puertos de servidor obligatorios (por rol de servidor)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-117">Required Server Ports (by Server Role)</span></span>

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
<th><span data-ttu-id="8ef6c-118">Rol de servidor</span><span class="sxs-lookup"><span data-stu-id="8ef6c-118">Server role</span></span></th>
<th><span data-ttu-id="8ef6c-119">Nombre de servicio</span><span class="sxs-lookup"><span data-stu-id="8ef6c-119">Service name</span></span></th>
<th><span data-ttu-id="8ef6c-120">Puerto</span><span class="sxs-lookup"><span data-stu-id="8ef6c-120">Port</span></span></th>
<th><span data-ttu-id="8ef6c-121">Protocolo</span><span class="sxs-lookup"><span data-stu-id="8ef6c-121">Protocol</span></span></th>
<th><span data-ttu-id="8ef6c-122">Notas</span><span class="sxs-lookup"><span data-stu-id="8ef6c-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-123">Todos los servidores</span><span class="sxs-lookup"><span data-stu-id="8ef6c-123">All Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-124">Explorador SQL</span><span class="sxs-lookup"><span data-stu-id="8ef6c-124">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-125">1434</span><span class="sxs-lookup"><span data-stu-id="8ef6c-125">1434</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-126">UDP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-126">UDP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-127">Explorador SQL para la copia replicada local de la base de datos del almacén central de administración.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-127">SQL Browser for the local replicated copy of the Central Management Store database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-128">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-128">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-129">Servicio de Front-End de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-129">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-130">5060</span><span class="sxs-lookup"><span data-stu-id="8ef6c-130">5060</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-131">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-131">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-132">Opcionalmente lo usan los servidores Standard Edition y front-end para rutas estáticas a servicios de confianza, como los servidores de control remoto de llamadas.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-132">Optionally used by Standard Edition servers and Front End Servers for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-133">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-133">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-134">Servicio de Front-End de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-134">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-135">5061</span><span class="sxs-lookup"><span data-stu-id="8ef6c-135">5061</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-136">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-136">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-137">Lo usan los servidores Standard Edition y los grupos de servidores front-end para todas las comunicaciones SIP internas entre los servidores (MTLS), para las comunicaciones SIP entre el cliente y el servidor (TLS) y para las comunicaciones SIP entre los servidores front-end y los servidores de mediación (MTLS).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-137">Used by Standard Edition servers and Front End pools for all internal SIP communications between servers (MTLS), for SIP communications between Server and Client (TLS) and for SIP communications between Front End Servers and Mediation Servers (MTLS).</span></span> <span data-ttu-id="8ef6c-138">También se usa para comunicaciones con el servidor de supervisión.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-138">Also used for communications with Monitoring Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-139">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-139">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-140">Servicio de Front-End de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-140">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-141">444</span><span class="sxs-lookup"><span data-stu-id="8ef6c-141">444</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-142">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-142">HTTPS</span></span></p>
<p><span data-ttu-id="8ef6c-143">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-143">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-144">Se usa para la comunicación HTTPS entre el foco (el componente de Lync Server que administra el estado de la Conferencia) y los servidores individuales.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-144">Used for HTTPS communication between the Focus (the Lync Server component that manages conference state) and the individual servers.</span></span></p>
<p><span data-ttu-id="8ef6c-145">Este puerto también se usa para la comunicación TCP entre los equipos de las sucursales y los servidores de aplicaciones para el usuario.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-145">This port is also used for TCP communication between Survivable Branch Appliances and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-146">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-146">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-147">Servicio de Front-End de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-147">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-148">135</span><span class="sxs-lookup"><span data-stu-id="8ef6c-148">135</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-149">DCOM y llamada a procedimiento remoto (RPC)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-149">DCOM and remote procedure call (RPC)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-150">Se usa para operaciones basadas en DCOM, como la migración de los usuarios, la sincronización del replicador de usuarios y la sincronización de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-150">Used for DCOM based operations such as Moving Users, User Replicator Synchronization, and Address Book Synchronization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-151">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-151">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-152">Servicio de conferencia de mensajería instantánea de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-152">Lync Server IM Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-153">5062</span><span class="sxs-lookup"><span data-stu-id="8ef6c-153">5062</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-154">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-154">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-155">Se usa para las solicitudes SIP entrantes de las conferencias de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-155">Used for incoming SIP requests for instant messaging (IM) conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-156">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-156">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-157">Servicio de conferencias web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-157">Lync Server Web Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-158">8057</span><span class="sxs-lookup"><span data-stu-id="8ef6c-158">8057</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-159">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-159">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-160">Se usa para escuchar las conexiones del Modelo de objetos compartidos persistentes (PSOM) desde un cliente.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-160">Used to listen for Persistent Shared Object Model (PSOM) connections from client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-161">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-161">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-162">Servicio de compatibilidad con conferencias web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-162">Lync Server Web Conferencing Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-163">8058</span><span class="sxs-lookup"><span data-stu-id="8ef6c-163">8058</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-164">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-164">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-165">Se usa para escuchar conexiones persistentes del modelo de objetos compartidos (PSOM) desde el cliente de Live Meeting y las versiones anteriores de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-165">Used to listen for Persistent Shared Object Model (PSOM) connections from the Live Meeting client and previous versions of Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-166">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-166">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-167">Servicio de conferencia de audio y vídeo de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-167">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-168">5063</span><span class="sxs-lookup"><span data-stu-id="8ef6c-168">5063</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-169">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-169">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-170">Se usa para las solicitudes SIP entrantes de las conferencias de audio y vídeo (A/V).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-170">Used for incoming SIP requests for audio/video (A/V) conferencing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-171">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-171">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-172">Servicio de conferencia de audio y vídeo de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-172">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-173">57501-65535</span><span class="sxs-lookup"><span data-stu-id="8ef6c-173">57501-65535</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-174">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-174">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-175">Intervalo de puertos de medios que se usa para conferencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-175">Media port range used for video conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-176">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-176">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-177">Servicio de compatibilidad Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-177">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-178">80</span><span class="sxs-lookup"><span data-stu-id="8ef6c-178">80</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-179">HTTP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-179">HTTP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-180">Se usa para la comunicación entre los servidores front-end y los FQDN (direcciones URL que usan los componentes web de IIS) cuando no se usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-180">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components) when HTTPS is not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-181">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-181">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-182">Servicio de compatibilidad Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-182">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-183">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-183">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-184">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-184">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-185">Se usa para la comunicación entre los servidores front-end y los FQDN de la granja de servidores web (direcciones URL que usan los componentes web de IIS).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-185">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-186">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-186">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-187">Servicio de compatibilidad Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-187">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-188">8080</span><span class="sxs-lookup"><span data-stu-id="8ef6c-188">8080</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-189">TCP y HTTP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-189">TCP and HTTP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-190">Lo usan los componentes web para acceso externo.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-190">Used by web components for external access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-191">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-191">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-192">Componente de servidor web</span><span class="sxs-lookup"><span data-stu-id="8ef6c-192">Web server component</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-193">4443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-193">4443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-194">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-194">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-195">Comunicaciones entre grupos de HTTPS (desde proxy inverso) y HTTPS front-end para el inicio de sesión con detección automática.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-195">HTTPS (from Reverse Proxy) and HTTPS Front End inter-pool communications for Autodiscover sign-in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-196">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-196">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-197">Componente de servidor web</span><span class="sxs-lookup"><span data-stu-id="8ef6c-197">Web server component</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-198">8060</span><span class="sxs-lookup"><span data-stu-id="8ef6c-198">8060</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-199">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-199">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-200">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-200">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-201">Componente de servidor web</span><span class="sxs-lookup"><span data-stu-id="8ef6c-201">Web server component</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-202">8061</span><span class="sxs-lookup"><span data-stu-id="8ef6c-202">8061</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-203">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-203">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-204">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-204">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-205">Componente de servicios de movilidad</span><span class="sxs-lookup"><span data-stu-id="8ef6c-205">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-206">5086</span><span class="sxs-lookup"><span data-stu-id="8ef6c-206">5086</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-207">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-207">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-208">Puerto SIP que usan los procesos internos de los servicios de movilidad</span><span class="sxs-lookup"><span data-stu-id="8ef6c-208">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-209">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-209">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-210">Componente de servicios de movilidad</span><span class="sxs-lookup"><span data-stu-id="8ef6c-210">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-211">5087</span><span class="sxs-lookup"><span data-stu-id="8ef6c-211">5087</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-212">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-212">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-213">Puerto SIP que usan los procesos internos de los servicios de movilidad</span><span class="sxs-lookup"><span data-stu-id="8ef6c-213">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-214">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-214">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-215">Componente de servicios de movilidad</span><span class="sxs-lookup"><span data-stu-id="8ef6c-215">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-216">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-216">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-217">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-217">HTTPS</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-218">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-218">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-219">Servicio del operador de conferencias de Lync Server (Conferencia de acceso telefónico local)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-219">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-220">5064</span><span class="sxs-lookup"><span data-stu-id="8ef6c-220">5064</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-221">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-221">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-222">Se usa para las solicitudes SIP entrantes de las conferencias de acceso telefónico local.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-222">Used for incoming SIP requests for dial-in conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-223">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-223">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-224">Servicio del operador de conferencias de Lync Server (Conferencia de acceso telefónico local)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-224">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-225">5072</span><span class="sxs-lookup"><span data-stu-id="8ef6c-225">5072</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-226">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-226">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-227">Se usa para las solicitudes SIP entrantes para operadores (llamar en conferencia).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-227">Used for incoming SIP requests for Attendant (dial in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-228">Servidores front-end que también ejecutan un servidor de mediación combinado</span><span class="sxs-lookup"><span data-stu-id="8ef6c-228">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-229">Servicio de mediación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-229">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-230">5070</span><span class="sxs-lookup"><span data-stu-id="8ef6c-230">5070</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-231">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-231">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-232">Lo usa el servidor de mediación para solicitudes entrantes desde el servidor front-end al servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-232">Used by the Mediation Server for incoming requests from the Front End Server to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-233">Servidores front-end que también ejecutan un servidor de mediación combinado</span><span class="sxs-lookup"><span data-stu-id="8ef6c-233">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-234">Servicio de mediación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-234">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-235">5067</span><span class="sxs-lookup"><span data-stu-id="8ef6c-235">5067</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-236">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-236">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-237">Se usa para solicitudes SIP entrantes desde la puerta de enlace RTC al servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-237">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-238">Servidores front-end que también ejecutan un servidor de mediación combinado</span><span class="sxs-lookup"><span data-stu-id="8ef6c-238">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-239">Servicio de mediación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-239">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-240">5068</span><span class="sxs-lookup"><span data-stu-id="8ef6c-240">5068</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-241">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-241">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-242">Se usa para solicitudes SIP entrantes desde la puerta de enlace RTC al servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-242">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-243">Servidores front-end que también ejecutan un servidor de mediación combinado</span><span class="sxs-lookup"><span data-stu-id="8ef6c-243">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-244">Servicio de mediación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-244">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-245">5081</span><span class="sxs-lookup"><span data-stu-id="8ef6c-245">5081</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-246">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-246">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-247">Se usa para solicitudes SIP salientes desde el servidor de mediación a la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-247">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-248">Servidores front-end que también ejecutan un servidor de mediación combinado</span><span class="sxs-lookup"><span data-stu-id="8ef6c-248">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-249">Servicio de mediación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-249">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-250">5082</span><span class="sxs-lookup"><span data-stu-id="8ef6c-250">5082</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-251">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-251">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-252">Se usa para solicitudes SIP salientes desde el servidor de mediación a la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-252">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-253">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-253">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-254">Servicio de uso compartido de aplicaciones de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-254">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-255">5065</span><span class="sxs-lookup"><span data-stu-id="8ef6c-255">5065</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-256">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-256">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-257">Se usa para las solicitudes de escucha SIP entrantes para compartir las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-257">Used for incoming SIP listening requests for application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-258">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-258">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-259">Servicio de uso compartido de aplicaciones de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-259">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-260">49152-65535</span><span class="sxs-lookup"><span data-stu-id="8ef6c-260">49152-65535</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-261">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-261">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-262">Intervalo de puertos de medios que se usa para compartir aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-262">Media port range used for application sharing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-263">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-263">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-264">Servicio de anuncios de conferencias de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-264">Lync Server Conferencing Announcement service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-265">5073</span><span class="sxs-lookup"><span data-stu-id="8ef6c-265">5073</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-266">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-266">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-267">Se usa para las solicitudes SIP entrantes para el servicio de anuncios de conferencias de Lync Server (es decir, para conferencias de acceso telefónico local).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-267">Used for incoming SIP requests for the Lync Server Conferencing Announcement service (that is, for dial-in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-268">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-268">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-269">Servicio de estacionamiento de llamadas de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-269">Lync Server Call Park service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-270">5075</span><span class="sxs-lookup"><span data-stu-id="8ef6c-270">5075</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-271">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-271">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-272">Se usa para las solicitudes SIP entrantes de la aplicación Estacionamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-272">Used for incoming SIP requests for the Call Park application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-273">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-273">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-274">Servicio de prueba de audio de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-274">Lync Server Audio Test service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-275">5076</span><span class="sxs-lookup"><span data-stu-id="8ef6c-275">5076</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-276">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-276">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-277">Se usa para las solicitudes SIP entrantes del servicio de prueba de audio.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-277">Used for incoming SIP requests for the Audio Test service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-278">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-278">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-279">No aplicable</span><span class="sxs-lookup"><span data-stu-id="8ef6c-279">Not applicable</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-280">5066</span><span class="sxs-lookup"><span data-stu-id="8ef6c-280">5066</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-281">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-281">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-282">Se usa para la puerta de enlace 9-1-1 mejorado (E9-1-1) saliente.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-282">Used for outbound Enhanced 9-1-1 (E9-1-1) gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-283">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-283">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-284">Servicio de grupo de respuesta de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-284">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-285">5071</span><span class="sxs-lookup"><span data-stu-id="8ef6c-285">5071</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-286">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-286">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-287">Se usa para las solicitudes SIP entrantes de la aplicación Grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-287">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-288">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-288">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-289">Servicio de grupo de respuesta de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-289">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-290">8404</span><span class="sxs-lookup"><span data-stu-id="8ef6c-290">8404</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-291">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-291">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-292">Se usa para las solicitudes SIP entrantes de la aplicación Grupo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-292">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-293">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-293">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-294">Servicio de directiva de ancho de banda de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-294">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-295">5080</span><span class="sxs-lookup"><span data-stu-id="8ef6c-295">5080</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-296">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-296">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-297">Lo usa el servicio de directiva de ancho de banda del tráfico TURN perimetral A/V para el servicio de control de admisión de llamadas.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-297">Used for call admission control by the Bandwidth Policy service for A/V Edge TURN traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-298">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-298">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-299">Servicio de directiva de ancho de banda de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-299">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-300">448</span><span class="sxs-lookup"><span data-stu-id="8ef6c-300">448</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-301">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-301">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-302">Usado por el servicio de directivas de ancho de banda de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-302">Used for call admission control by the Lync Server Bandwidth Policy Service.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-303">Servidores front-end en los que reside el almacén de administración central</span><span class="sxs-lookup"><span data-stu-id="8ef6c-303">Front End Servers where the Central Management store resides</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-304">Servicio agente de replicación maestra de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-304">Lync Server Master Replicator Agent service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-305">445</span><span class="sxs-lookup"><span data-stu-id="8ef6c-305">445</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-306">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-306">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-307">Se usa para insertar los datos de configuración desde el almacén de administración central en servidores que ejecutan Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-307">Used to push configuration data from the Central Management store to servers running Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-308">Todos los servidores</span><span class="sxs-lookup"><span data-stu-id="8ef6c-308">All Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-309">Explorador SQL</span><span class="sxs-lookup"><span data-stu-id="8ef6c-309">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-310">1434</span><span class="sxs-lookup"><span data-stu-id="8ef6c-310">1434</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-311">UDP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-311">UDP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-312">Explorador SQL para la copia replicada local de los datos del almacén central de administración en la instancia local de SQL Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-312">SQL Browser for local replicated copy of Central Management store data in local SQL Server instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-313">Todos los usuarios internos</span><span class="sxs-lookup"><span data-stu-id="8ef6c-313">All internal servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-314">Varios</span><span class="sxs-lookup"><span data-stu-id="8ef6c-314">Various</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-315">49152-57500</span><span class="sxs-lookup"><span data-stu-id="8ef6c-315">49152-57500</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-316">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-316">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-317">El intervalo de puertos de medios se usa para audioconferencias en todos los servidores internos.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-317">Media port range used for audio conferencing on all internal servers.</span></span> <span data-ttu-id="8ef6c-318">Usado por todos los servidores que terminan audio: servidores front-end (para el servicio del operador de conferencias de Lync Server, servicio de anuncios de conferencias de Lync Server y el servicio de audioconferencias de audio y vídeo de Lync) y servidor de mediación.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-318">Used by all servers that terminate audio: Front End Servers (for Lync Server Conferencing Attendant service, Lync Server Conferencing Announcement service, and Lync Server Audio/Video Conferencing service), and Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-319">Servidores de Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="8ef6c-319">Office Web Apps Servers</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8ef6c-320">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-320">443</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8ef6c-321">Usado por Lync Server 2013 para conectarse a Office Web Apps Server.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-321">Used by Lync Server 2013 to connect to Office Web Apps Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-322">Directores</span><span class="sxs-lookup"><span data-stu-id="8ef6c-322">Directors</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-323">Servicio de Front-End de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-323">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-324">5060</span><span class="sxs-lookup"><span data-stu-id="8ef6c-324">5060</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-325">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-325">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-326">Se usa opcionalmente para rutas estáticas a servicios de confianza, como los servidores de control remoto de llamadas.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-326">Optionally used for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-327">Directores</span><span class="sxs-lookup"><span data-stu-id="8ef6c-327">Directors</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-328">Servicio de Front-End de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-328">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-329">444</span><span class="sxs-lookup"><span data-stu-id="8ef6c-329">444</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-330">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-330">HTTPS</span></span></p>
<p><span data-ttu-id="8ef6c-331">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-331">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-332">Comunicación entre servidores front-end y Director.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-332">Inter-server communication between Front End and Director.</span></span> <span data-ttu-id="8ef6c-333">Además, la publicación de certificados de cliente (a servidores de aplicaciones para el usuario) o la validación si el certificado de cliente ya se ha publicado.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-333">Additionally, client certificate publish (to Front End Servers) or validate if the client certificate has already been published.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-334">Directores</span><span class="sxs-lookup"><span data-stu-id="8ef6c-334">Directors</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-335">Servicio de compatibilidad Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-335">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-336">80</span><span class="sxs-lookup"><span data-stu-id="8ef6c-336">80</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-337">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-337">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-p105">Se usa para la comunicación inicial desde los Directores a los FQDN de la granja de servidores web (direcciones URL que usan los componentes web de IIS). En condiciones normales, cambiará a tráfico HTTPS a través del puerto 443 y el tipo de protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-p105">Used for initial communication from Directors to the web farm FQDNs (the URLs used by IIS web components). In normal operation, will switch to HTTPS traffic, using port 443 and protocol type TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-340">Directores</span><span class="sxs-lookup"><span data-stu-id="8ef6c-340">Directors</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-341">Servicio de compatibilidad Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-341">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-342">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-342">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-343">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-343">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-344">Se usa para la comunicación desde los Directores a los FQDN de la granja de servidores web (direcciones URL que usan los componentes web de IIS).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-344">Used for communication from Directors to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-345">Directores</span><span class="sxs-lookup"><span data-stu-id="8ef6c-345">Directors</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-346">Servicio de Front-End de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-346">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-347">5061</span><span class="sxs-lookup"><span data-stu-id="8ef6c-347">5061</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-348">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-348">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-349">Se usa para comunicaciones internas entre servidores y para conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-349">Used for internal communications between servers and for client connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-350">Servidores de mediación</span><span class="sxs-lookup"><span data-stu-id="8ef6c-350">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-351">Servicio de mediación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-351">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-352">5070</span><span class="sxs-lookup"><span data-stu-id="8ef6c-352">5070</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-353">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-353">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-354">Lo usa el servidor de mediación para solicitudes entrantes desde el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-354">Used by the Mediation Server for incoming requests from the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-355">Servidores de mediación</span><span class="sxs-lookup"><span data-stu-id="8ef6c-355">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-356">Servicio de mediación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-356">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-357">5067</span><span class="sxs-lookup"><span data-stu-id="8ef6c-357">5067</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-358">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-358">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-359">Se usa para solicitudes SIP entrantes desde la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-359">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-360">Servidores de mediación</span><span class="sxs-lookup"><span data-stu-id="8ef6c-360">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-361">Servicio de mediación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-361">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-362">5068</span><span class="sxs-lookup"><span data-stu-id="8ef6c-362">5068</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-363">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-363">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-364">Se usa para solicitudes SIP entrantes desde la puerta de enlace RTC.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-364">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-365">Servidores de mediación</span><span class="sxs-lookup"><span data-stu-id="8ef6c-365">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-366">Servicio de mediación de Lync Server</span><span class="sxs-lookup"><span data-stu-id="8ef6c-366">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-367">5070</span><span class="sxs-lookup"><span data-stu-id="8ef6c-367">5070</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-368">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-368">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-369">Se usa para solicitudes SIP desde los servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-369">Used for SIP requests from the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-370">Servidor front-end de chat persistente</span><span class="sxs-lookup"><span data-stu-id="8ef6c-370">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-371">SIP de chat persistente</span><span class="sxs-lookup"><span data-stu-id="8ef6c-371">Persistent Chat SIP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-372">5041</span><span class="sxs-lookup"><span data-stu-id="8ef6c-372">5041</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-373">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-373">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-374">Servidor front-end de chat persistente</span><span class="sxs-lookup"><span data-stu-id="8ef6c-374">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-375">Windows Communication Foundation (WCF) de chat persistente</span><span class="sxs-lookup"><span data-stu-id="8ef6c-375">Persistent Chat Windows Communication Foundation (WCF)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-376">881</span><span class="sxs-lookup"><span data-stu-id="8ef6c-376">881</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-377">TCP (TLS) y TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-377">TCP (TLS) and TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-378">Servidor front-end de chat persistente</span><span class="sxs-lookup"><span data-stu-id="8ef6c-378">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-379">Servicio de transferencia de archivos de chat persistente</span><span class="sxs-lookup"><span data-stu-id="8ef6c-379">Persistent Chat File Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-380">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-380">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-381">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-381">TCP (TLS)</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="8ef6c-382">Algunos escenarios de control remoto de llamadas requieren una conexión entre el servidor front-end o el Director y la PBX.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-382">Some remote call control scenarios require a TCP connection between the Front End Server or Director and the PBX.</span></span> <span data-ttu-id="8ef6c-383">Aunque Lync Server ya no usa el puerto TCP 5060, durante la implementación de control remoto de llamadas, se crea una configuración de servidor de confianza, que asocia el FQDN del servidor de línea RCC con el puerto TCP que usará el servidor o director de front-end para conectarse al sistema PBX.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-383">Although Lync Server no longer uses TCP port 5060, during remote call control deployment you create a trusted server configuration, which associates the RCC Line Server FQDN with the TCP port that the Front End Server or Director will use to connect to the PBX system.</span></span> <span data-ttu-id="8ef6c-384">Para obtener más información, vea el cmdlet <STRONG>CsTrustedApplicationComputer</STRONG> en la documentación del shell de administración de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-384">For details, see the <STRONG>CsTrustedApplicationComputer</STRONG> cmdlet in the Lync Server Management Shell documentation.</span></span>



</div>

<span data-ttu-id="8ef6c-385">Para los grupos que solo usan equilibrio de carga de hardware (no equilibrio de carga de DNS), en la siguiente tabla se muestran los puertos que necesitan para abrir los equilibradores de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-385">For your pools that use only hardware load balancing (not DNS load balancing), the following table shows the ports that need to open the hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-only-hardware-load-balancing"></a><span data-ttu-id="8ef6c-386">Puertos del equilibrador de carga de hardware si solo usa equilibrio de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="8ef6c-386">Hardware Load Balancer Ports if Using Only Hardware Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ef6c-387">Equilibrador de carga</span><span class="sxs-lookup"><span data-stu-id="8ef6c-387">Load Balancer</span></span></th>
<th><span data-ttu-id="8ef6c-388">Puerto</span><span class="sxs-lookup"><span data-stu-id="8ef6c-388">Port</span></span></th>
<th><span data-ttu-id="8ef6c-389">Protocolo</span><span class="sxs-lookup"><span data-stu-id="8ef6c-389">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-390">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-390">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-391">5061</span><span class="sxs-lookup"><span data-stu-id="8ef6c-391">5061</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-392">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-392">TCP (TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-393">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-393">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-394">444</span><span class="sxs-lookup"><span data-stu-id="8ef6c-394">444</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-395">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-395">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-396">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-396">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-397">135</span><span class="sxs-lookup"><span data-stu-id="8ef6c-397">135</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-398">DCOM y llamada a procedimiento remoto (RPC)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-398">DCOM and remote procedure call (RPC)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-399">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-399">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-400">80</span><span class="sxs-lookup"><span data-stu-id="8ef6c-400">80</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-401">HTTP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-401">HTTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-402">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-402">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-403">8080</span><span class="sxs-lookup"><span data-stu-id="8ef6c-403">8080</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-404">TCP, Recuperación cliente y dispositivo del certificado raíz del servidor de front-end, clientes y dispositivos autenticados por NTLM</span><span class="sxs-lookup"><span data-stu-id="8ef6c-404">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-405">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-405">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-406">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-406">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-407">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-407">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-408">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-408">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-409">4443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-409">4443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-410">HTTPS (desde proxy inverso)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-410">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-411">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-411">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-412">5072</span><span class="sxs-lookup"><span data-stu-id="8ef6c-412">5072</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-413">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-413">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-414">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-414">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-415">5073</span><span class="sxs-lookup"><span data-stu-id="8ef6c-415">5073</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-416">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-416">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-417">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-417">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-418">5075</span><span class="sxs-lookup"><span data-stu-id="8ef6c-418">5075</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-419">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-419">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-420">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-420">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-421">5076</span><span class="sxs-lookup"><span data-stu-id="8ef6c-421">5076</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-422">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-422">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-423">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-423">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-424">5071</span><span class="sxs-lookup"><span data-stu-id="8ef6c-424">5071</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-425">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-425">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-426">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-426">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-427">5080</span><span class="sxs-lookup"><span data-stu-id="8ef6c-427">5080</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-428">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-428">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-429">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-429">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-430">448</span><span class="sxs-lookup"><span data-stu-id="8ef6c-430">448</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-431">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-431">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-432">Equilibrador de carga del servidor de mediación</span><span class="sxs-lookup"><span data-stu-id="8ef6c-432">Mediation Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-433">5070</span><span class="sxs-lookup"><span data-stu-id="8ef6c-433">5070</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-434">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-434">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-435">Equilibrador de carga del servidor front-end (si el grupo también ejecuta el servidor de mediación)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-435">Front End Server load balancer (if the pool also runs Mediation Server)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-436">5070</span><span class="sxs-lookup"><span data-stu-id="8ef6c-436">5070</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-437">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-437">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-438">Equilibrador de carga del Director</span><span class="sxs-lookup"><span data-stu-id="8ef6c-438">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-439">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-439">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-440">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-440">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-441">Equilibrador de carga del Director</span><span class="sxs-lookup"><span data-stu-id="8ef6c-441">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-442">444</span><span class="sxs-lookup"><span data-stu-id="8ef6c-442">444</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-443">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-443">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-444">Equilibrador de carga del Director</span><span class="sxs-lookup"><span data-stu-id="8ef6c-444">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-445">5061</span><span class="sxs-lookup"><span data-stu-id="8ef6c-445">5061</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-446">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-446">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-447">Equilibrador de carga del Director</span><span class="sxs-lookup"><span data-stu-id="8ef6c-447">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-448">4443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-448">4443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-449">HTTPS (desde proxy inverso)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-449">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8ef6c-p107">Los grupos de servidores front-end y de Directores que usan equilibrio de carga de DNS también deben tener implementado un equilibrador de carga de hardware. En la siguiente tabla se muestran los puertos que se deben abrir en estos equilibradores de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-p107">Your Front End pools and Director pools that use DNS load balancing also must have a hardware load balancer deployed. The following table shows the ports that need to be open on these hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-dns-load-balancing"></a><span data-ttu-id="8ef6c-452">Puertos del equilibrador de carga de hardware si usa equilibrio de carga de DNS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-452">Hardware Load Balancer Ports if Using DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ef6c-453">Equilibrador de carga</span><span class="sxs-lookup"><span data-stu-id="8ef6c-453">Load Balancer</span></span></th>
<th><span data-ttu-id="8ef6c-454">Puerto</span><span class="sxs-lookup"><span data-stu-id="8ef6c-454">Port</span></span></th>
<th><span data-ttu-id="8ef6c-455">Protocolo</span><span class="sxs-lookup"><span data-stu-id="8ef6c-455">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-456">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-456">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-457">80</span><span class="sxs-lookup"><span data-stu-id="8ef6c-457">80</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-458">HTTP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-458">HTTP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-459">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-459">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-460">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-460">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-461">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-461">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-462">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-462">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-463">8080</span><span class="sxs-lookup"><span data-stu-id="8ef6c-463">8080</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-464">TCP, Recuperación cliente y dispositivo del certificado raíz del servidor de front-end, clientes y dispositivos autenticados por NTLM</span><span class="sxs-lookup"><span data-stu-id="8ef6c-464">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-465">Equilibrador de carga del servidor front-end</span><span class="sxs-lookup"><span data-stu-id="8ef6c-465">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-466">4443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-466">4443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-467">HTTPS (desde proxy inverso)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-467">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-468">Equilibrador de carga del Director</span><span class="sxs-lookup"><span data-stu-id="8ef6c-468">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-469">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-469">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-470">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ef6c-470">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-471">Equilibrador de carga del Director</span><span class="sxs-lookup"><span data-stu-id="8ef6c-471">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-472">4443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-472">4443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-473">HTTPS (desde proxy inverso)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-473">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="required-client-ports"></a><span data-ttu-id="8ef6c-474">Puertos de cliente necesarios</span><span class="sxs-lookup"><span data-stu-id="8ef6c-474">Required Client Ports</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ef6c-475">Componente</span><span class="sxs-lookup"><span data-stu-id="8ef6c-475">Component</span></span></th>
<th><span data-ttu-id="8ef6c-476">Puerto</span><span class="sxs-lookup"><span data-stu-id="8ef6c-476">Port</span></span></th>
<th><span data-ttu-id="8ef6c-477">Protocolo</span><span class="sxs-lookup"><span data-stu-id="8ef6c-477">Protocol</span></span></th>
<th><span data-ttu-id="8ef6c-478">Notas</span><span class="sxs-lookup"><span data-stu-id="8ef6c-478">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-479">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-479">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-480">67/68</span><span class="sxs-lookup"><span data-stu-id="8ef6c-480">67/68</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-481">DHCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-481">DHCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-482">Utilizado por Lync Server para encontrar el nombre completo del registrador (es decir, si no se puede establecer la configuración manual de DNS SRV).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-482">Used by Lync Server to find the Registrar FQDN (that is, if DNS SRV fails and manual settings are not configured).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-483">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-483">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-484">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-484">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-485">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-485">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-486">Se usa para el tráfico SIP de cliente a servidor para el acceso de usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-486">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-487">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-487">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-488">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-488">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-489">TCP (PSOM/TLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-489">TCP (PSOM/TLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-490">Se usa para el acceso de usuarios externos a las sesiones de conferencia web.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-490">Used for external user access to web conferencing sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-491">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-491">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-492">443</span><span class="sxs-lookup"><span data-stu-id="8ef6c-492">443</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-493">TCP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-493">TCP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-494">Se usa para el acceso de usuarios externos a las sesiones de A/V y a los medios (TCP).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-494">Used for external user access to A/V sessions and media (TCP)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-495">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-495">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-496">3478</span><span class="sxs-lookup"><span data-stu-id="8ef6c-496">3478</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-497">UDP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-497">UDP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-498">Se usa para el acceso de usuarios externos a los medios y las sesiones de A/V (UDP)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-498">Used for external user access to A/V sessions and media (UDP)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-499">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-499">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-500">5061</span><span class="sxs-lookup"><span data-stu-id="8ef6c-500">5061</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-501">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-501">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-502">Se usa para el tráfico SIP de cliente a servidor para el acceso de usuarios externos.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-502">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-503">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-503">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-504">6891-6901</span><span class="sxs-lookup"><span data-stu-id="8ef6c-504">6891-6901</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-505">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-505">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-506">Se usa para la transferencia de archivos entre clientes de Lync y clientes anteriores (clientes de Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007 y Live Communications Server 2005).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-506">Used for file transfer between Lync clients and previous clients (clients of Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007, and Live Communications Server 2005).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-507">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-507">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-508">1024-65535\*</span><span class="sxs-lookup"><span data-stu-id="8ef6c-508">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-509">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-509">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-510">Intervalo de puertos de audio (se requieren 20 puertos como mínimo).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-510">Audio port range (minimum of 20 ports required)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-511">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-511">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-512">1024-65535\*</span><span class="sxs-lookup"><span data-stu-id="8ef6c-512">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-513">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-513">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-514">Intervalo de puertos de vídeo (se requieren 20 puertos como mínimo).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-514">Video port range (minimum of 20 ports required).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-515">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-515">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-516">1024-65535\*</span><span class="sxs-lookup"><span data-stu-id="8ef6c-516">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-517">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-517">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-518">Transferencias de archivos de punto a punto (para la transferencia de archivos de conferencia, los clientes usan PSOM).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-518">Peer-to-peer file transfer (for conferencing file transfer, clients use PSOM).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ef6c-519">Clientes</span><span class="sxs-lookup"><span data-stu-id="8ef6c-519">Clients</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-520">1024-65535\*</span><span class="sxs-lookup"><span data-stu-id="8ef6c-520">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-521">TCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-521">TCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-522">Uso compartido de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-522">Application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ef6c-523">Teléfono de área común Aastra 6721ip</span><span class="sxs-lookup"><span data-stu-id="8ef6c-523">Aastra 6721ip common area phone</span></span></p>
<p><span data-ttu-id="8ef6c-524">Teléfono de escritorio Aastra 6725ip</span><span class="sxs-lookup"><span data-stu-id="8ef6c-524">Aastra 6725ip desk phone</span></span></p>
<p><span data-ttu-id="8ef6c-525">Teléfono IP HP 4110 (teléfono de área común)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-525">HP 4110 IP Phone (common area phone)</span></span></p>
<p><span data-ttu-id="8ef6c-526">Teléfono IP HP 4120 (teléfono de escritorio)</span><span class="sxs-lookup"><span data-stu-id="8ef6c-526">HP 4120 IP Phone (desk phone)</span></span></p>
<p><span data-ttu-id="8ef6c-527">Teléfono de área común Polycom CX500 IP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-527">Polycom CX500 IP common area phone</span></span></p>
<p><span data-ttu-id="8ef6c-528">Teléfono de escritorio Polycom CX600 IP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-528">Polycom CX600 IP desk phone</span></span></p>
<p><span data-ttu-id="8ef6c-529">Teléfono de escritorio Polycom CX700 IP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-529">Polycom CX700 IP desk phone</span></span></p>
<p><span data-ttu-id="8ef6c-530">Teléfono de conferencia Polycom CX3000 IP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-530">Polycom CX3000 IP conference phone</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-531">67/68</span><span class="sxs-lookup"><span data-stu-id="8ef6c-531">67/68</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-532">DHCP</span><span class="sxs-lookup"><span data-stu-id="8ef6c-532">DHCP</span></span></p></td>
<td><p><span data-ttu-id="8ef6c-533">Usado por los dispositivos de la lista para buscar el certificado de Lync Server, el FQDN de aprovisionamiento y el registrador de FQDN.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-533">Used by the listed devices to find the Lync Server certificate, provisioning FQDN, and Registrar FQDN.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8ef6c-534">**\*** Para configurar puertos específicos para estos tipos de medios, use el cmdlet CsConferencingConfiguration (ClientMediaPortRangeEnabled, ClientMediaPort y ClientMediaPortRange parámetros).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-534">**\*** To configure specific ports for these media types, use the CsConferencingConfiguration cmdlet (ClientMediaPortRangeEnabled, ClientMediaPort, and ClientMediaPortRange parameters).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8ef6c-535">El conjunto de programas para clientes de Lync crea automáticamente las excepciones de firewall del sistema operativo necesarias en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="8ef6c-535">The set programs for Lync clients automatically create the required operating-system firewall exceptions on the client computer.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="8ef6c-536">Los puertos que se usan para el acceso de usuarios externos son necesarios en cualquier escenario en el que el cliente deba atravesar el firewall de la organización (por ejemplo, las comunicaciones o reuniones externas que se hospedan en otras organizaciones).</span><span class="sxs-lookup"><span data-stu-id="8ef6c-536">The ports that are used for external user access are required for any scenario in which the client must traverse the organization’s firewall (for example, any external communications or meetings hosted by other organizations).</span></span>



<span data-ttu-id="8ef6c-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ef6c-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

