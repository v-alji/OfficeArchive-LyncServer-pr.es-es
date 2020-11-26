---
title: 'Lync Server 2013: Plataformas de hardware de servidor'
description: Plataformas de hardware de servidor de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server hardware platforms
ms:assetid: c964c1c0-0153-472b-88ad-a38866e0df0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398835(v=OCS.15)
ms:contentKeyID: 48185395
ms.date: 07/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d55deec50994d70cf305b794662a630c16c3af14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441875"
---
# <a name="server-hardware-platforms-for-lync-server-2013"></a><span data-ttu-id="63f51-103">Plataformas de hardware de servidor para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="63f51-103">Server hardware platforms for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63f51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63f51-104">

<span> </span></span></span>

<span data-ttu-id="63f51-105">_**Última modificación del tema:** 2016-07-28_</span><span class="sxs-lookup"><span data-stu-id="63f51-105">_**Topic Last Modified:** 2016-07-28_</span></span>

<span data-ttu-id="63f51-106">Los roles de servidor de Lync Server 2013 y los equipos que ejecutan las herramientas administrativas de Lync Server requieren hardware de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="63f51-106">Lync Server 2013 server roles and computers running Lync Server administrative tools require 64-bit hardware.</span></span>

<span data-ttu-id="63f51-107">El hardware específico que se usa para la implementación de Lync Server 2013 puede variar en función de los requisitos de tamaño y uso.</span><span class="sxs-lookup"><span data-stu-id="63f51-107">The specific hardware used for Lync Server 2013 deployment can vary, depending on size and usage requirements.</span></span> <span data-ttu-id="63f51-108">En esta sección se describe el hardware recomendado.</span><span class="sxs-lookup"><span data-stu-id="63f51-108">This section describes the recommended hardware.</span></span> <span data-ttu-id="63f51-109">Aunque se trata de recomendaciones y no de requisitos, el uso de hardware que no cumpla estas recomendaciones puede repercutir considerablemente en el rendimiento y ocasionar otros problemas.</span><span class="sxs-lookup"><span data-stu-id="63f51-109">Although these are recommendations, not requirements, using hardware that does not meet these recommendations may result in significant performance issues and other issues.</span></span>

<div>

## <a name="recommended-hardware-platform"></a><span data-ttu-id="63f51-110">Plataforma de hardware recomendada</span><span class="sxs-lookup"><span data-stu-id="63f51-110">Recommended Hardware Platform</span></span>

<span data-ttu-id="63f51-111">Para obtener un rendimiento óptimo, le recomendamos que ejecute Lync Server en servidores con hardware que cumpla los requisitos de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="63f51-111">For best performance, we recommend that you run Lync Server on servers with hardware that meets the requirements in the following table.</span></span> <span data-ttu-id="63f51-112">Si usa un hardware menos eficaz, puede tener problemas de funcionalidad o un rendimiento deficiente.</span><span class="sxs-lookup"><span data-stu-id="63f51-112">If you use less powerful hardware, you may experience functionality problems or poor performance.</span></span> <span data-ttu-id="63f51-113">Tenga en cuenta que estos requisitos de hardware son superiores a los de las versiones anteriores de Lync Server, principalmente porque en Lync Server 2013, todos los servidores front-end ejecutan SQL Server.</span><span class="sxs-lookup"><span data-stu-id="63f51-113">Note that these hardware requirements are higher than those of previous versions of Lync Server, primarily because in Lync Server 2013, all Front End Servers run SQL Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="63f51-114">La formación de equipos NIC es compatible y debe ser transparente para Lync Server.</span><span class="sxs-lookup"><span data-stu-id="63f51-114">NIC teaming is supported and should be transparent to Lync Server.</span></span> <span data-ttu-id="63f51-115">Para obtener más información, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=389910">Communications Server o Lync Server y la formación de equipos de adaptadores de red</A>.</span><span class="sxs-lookup"><span data-stu-id="63f51-115">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=389910">Communications Server or Lync Server and network adapter teaming</A>.</span></span>



</div>

### <a name="recommended-hardware-for-front-end-servers-back-end-servers-standard-edition-servers-persistent-chat-servers-and-persistent-chat-store-and-persistent-chat-compliance-store-back-end-server-roles-for-persistent-chat-server"></a><span data-ttu-id="63f51-116">Hardware recomendado para los servidores front-end, back-end, Standard Edition, de chat persistente y para el Almacén de chat persistente y el Almacén de cumplimiento de chat persistente (roles de servidor back-end del servidor de chat persistente)</span><span class="sxs-lookup"><span data-stu-id="63f51-116">Recommended Hardware for Front End Servers, Back End Servers, Standard Edition Servers, Persistent Chat Servers, and Persistent Chat Store and Persistent Chat Compliance Store (Back End Server Roles for Persistent Chat Server)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63f51-117">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="63f51-117">Hardware component</span></span></th>
<th><span data-ttu-id="63f51-118">Recomendado</span><span class="sxs-lookup"><span data-stu-id="63f51-118">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63f51-119">CPU</span><span class="sxs-lookup"><span data-stu-id="63f51-119">CPU</span></span></p></td>
<td><p><span data-ttu-id="63f51-120">Procesador dual de 64 bits, seis núcleos y 2,26 gigahercios (GHz) o superior.</span><span class="sxs-lookup"><span data-stu-id="63f51-120">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher.</span></span></p>
<p><span data-ttu-id="63f51-121">Los procesadores Intel Itanium no son compatibles con los roles de servidor de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="63f51-121">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63f51-122">Memoria</span><span class="sxs-lookup"><span data-stu-id="63f51-122">Memory</span></span></p></td>
<td><p><span data-ttu-id="63f51-123">32 gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="63f51-123">32 gigabytes (GB).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63f51-124">Disco</span><span class="sxs-lookup"><span data-stu-id="63f51-124">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="63f51-125">8 o más unidades de disco duro (HHD) de 10 000 RPM con al menos 72 GB de espacio libre en disco.</span><span class="sxs-lookup"><span data-stu-id="63f51-125">8 or more 10,000 RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="63f51-126">Dos de los discos deben usar RAID 1 y seis deben usar RAID 10.</span><span class="sxs-lookup"><span data-stu-id="63f51-126">Two of the disks should use RAID 1, and six should use RAID 10.</span></span></p>
<p><span data-ttu-id="63f51-127">- Ni</span><span class="sxs-lookup"><span data-stu-id="63f51-127">- OR -</span></span></p></li>
<li><p><span data-ttu-id="63f51-128">Unidades de estado sólido (SSD) con un rendimiento igual al de 8 unidades de disco duro mecánicas de 10.000 rpm.</span><span class="sxs-lookup"><span data-stu-id="63f51-128">Solid state drives (SSDs) which provide performance similar to 8 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63f51-129">Red</span><span class="sxs-lookup"><span data-stu-id="63f51-129">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="63f51-130">1 adaptador de red de puerto doble, 1 Gbps o superior (recomendado: 2, lo que requiere la formación de equipos con una sola dirección MAC y una sola dirección IP).</span><span class="sxs-lookup"><span data-stu-id="63f51-130">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address).</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="63f51-131">Las configuraciones dual o multitarjeta no son compatibles con los servidores front-end, los servidores de back-end, los servidores Standard Edition y los servidores de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="63f51-131">Dual or multi-homed configurations are not supported for Front End Servers, Back End Servers, Standard Edition servers, and Persistent Chat Servers.</span></span><BR><span data-ttu-id="63f51-132">ILO/DRAC/etc. las conexiones que no se exponen al sistema operativo y se usan para supervisar y administrar el hardware del servidor no constituyen un servidor multitarjeta y, por lo tanto, son compatibles.</span><span class="sxs-lookup"><span data-stu-id="63f51-132">ILO/DRAC/etc. connections not exposed to the Operating System and used to monitor and manage the server hardware do not constitute a multi-homed server and thus are supported.</span></span>


</div></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="recommended-hardware-for-edge-servers-standalone-mediation-servers-and-directors"></a><span data-ttu-id="63f51-133">Hardware recomendado para los servidores perimetrales, los servidores de mediación autónomos y los Directores</span><span class="sxs-lookup"><span data-stu-id="63f51-133">Recommended Hardware for Edge Servers, Standalone Mediation Servers, and Directors</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63f51-134">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="63f51-134">Hardware component</span></span></th>
<th><span data-ttu-id="63f51-135">Recomendado</span><span class="sxs-lookup"><span data-stu-id="63f51-135">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63f51-136">CPU</span><span class="sxs-lookup"><span data-stu-id="63f51-136">CPU</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="63f51-137">procesador dual de 64 bits, núcleo cuádruple, 2,0 gigahercios (GHz) o superior.</span><span class="sxs-lookup"><span data-stu-id="63f51-137">64-bit dual processor, quad-core, 2.0 gigahertz (GHz) or higher.</span></span></p>
<p><span data-ttu-id="63f51-138">- Ni</span><span class="sxs-lookup"><span data-stu-id="63f51-138">- OR -</span></span></p></li>
<li><p><span data-ttu-id="63f51-139">procesador de 4 bits de 64, doble núcleo, 2,0 GHz o superior.</span><span class="sxs-lookup"><span data-stu-id="63f51-139">64-bit 4-way processor, dual-core, 2.0 GHz or higher.</span></span></p></li>
</ul>
<p><span data-ttu-id="63f51-140">Los procesadores Intel Itanium no son compatibles con los roles de servidor de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="63f51-140">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63f51-141">Memoria</span><span class="sxs-lookup"><span data-stu-id="63f51-141">Memory</span></span></p></td>
<td><p><span data-ttu-id="63f51-142">16 gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="63f51-142">16 gigabytes (GB).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63f51-143">Disco</span><span class="sxs-lookup"><span data-stu-id="63f51-143">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="63f51-144">4 unidades de disco duro de 10.000 RPM con un mínimo de 72 GB de espacio libre en disco.</span><span class="sxs-lookup"><span data-stu-id="63f51-144">4 or more 10,000 RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="63f51-145">Los discos deben presentar una configuración de 2 unidades RAID 1.</span><span class="sxs-lookup"><span data-stu-id="63f51-145">The disks should be in a 2x RAID 1 configuration.</span></span></p>
<p><span data-ttu-id="63f51-146">- Ni</span><span class="sxs-lookup"><span data-stu-id="63f51-146">- OR -</span></span></p></li>
<li><p><span data-ttu-id="63f51-147">Unidades de estado sólido (SSD) con un rendimiento igual al de 4 unidades de disco duro mecánicas de 10 000 rpm.</span><span class="sxs-lookup"><span data-stu-id="63f51-147">Solid state drives (SSDs) which provide performance similar to 4 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63f51-148">Red</span><span class="sxs-lookup"><span data-stu-id="63f51-148">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="63f51-149">1 adaptador de red de puerto doble, 1 Gbps o superior (recomendado: 2, lo que requiere la formación de equipos con una sola dirección MAC y una sola dirección IP).</span><span class="sxs-lookup"><span data-stu-id="63f51-149">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address).</span></span> <span data-ttu-id="63f51-150">en los servidores perimetrales se necesitan dos interfaces de red y se admiten en servidores de mediación independientes.</span><span class="sxs-lookup"><span data-stu-id="63f51-150">2 network interfaces are required on Edge Servers, and are supported on standalone Mediation Servers.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="63f51-151">Las configuraciones dual o multitarjeta no son compatibles con los directores.</span><span class="sxs-lookup"><span data-stu-id="63f51-151">Dual or multi-homed configurations are not supported for Directors.</span></span><BR><span data-ttu-id="63f51-152">ILO/DRAC/etc. las conexiones que no se exponen al sistema operativo y se usan para supervisar y administrar el hardware del servidor no constituyen un servidor multitarjeta y, por lo tanto, son compatibles.</span><span class="sxs-lookup"><span data-stu-id="63f51-152">ILO/DRAC/etc. connections not exposed to the Operating System and used to monitor and manage the server hardware do not constitute a multi-homed server and thus are supported.</span></span>


</div>
<p><span data-ttu-id="63f51-153">Los servidores perimetrales requerirán dos interfaces de red que sean adaptadores de red de dos puertos, 1 Gbps o superior (o dos adaptadores de red con dos pares, para un total de cuatro, cada pareja se acoplará con una única dirección MAC y una única dirección IP, para un total de dos pares).</span><span class="sxs-lookup"><span data-stu-id="63f51-153">Edge Servers will require two network interfaces that are dual-port network adapters, 1 Gbps or higher (or two paired network adapters, for a total of four, each pair being teamed with a single MAC address and a single IP address, for a total of two pairs).</span></span></p>
<p><span data-ttu-id="63f51-154">La instalación de tarjetas de interfaz de red (NICs) adicionales para permitir la configuración de una dirección IP de RTC específica es compatible con servidores de mediación independiente.</span><span class="sxs-lookup"><span data-stu-id="63f51-154">Installation of additional network interface cards (NICs) to allow the configuration of a specific PSTN IP address is supported on standalone Mediation Servers.</span></span></p><span data-ttu-id="63f51-155"></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63f51-155"></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

