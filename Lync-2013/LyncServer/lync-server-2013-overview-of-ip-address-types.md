---
title: 'Lync Server 2013: Información general sobre los tipos de direcciones IP'
description: 'Lync Server 2013: información general sobre los tipos de direcciones IP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of IP address types for Lync Server
ms:assetid: ee9a695f-5cf5-441e-94fb-6adeca50e8d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205363(v=OCS.15)
ms:contentKeyID: 48185759
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81492b2e006a6f44f6deb78e6a0560f6e319992f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445137"
---
# <a name="overview-of-ip-address-types-for-lync-server-2013"></a><span data-ttu-id="06947-103">Información general sobre los tipos de direcciones IP en Lync Server para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06947-103">Overview of IP address types for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06947-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06947-104">

<span> </span></span></span>

<span data-ttu-id="06947-105">_**Última modificación del tema:** 2013-01-29_</span><span class="sxs-lookup"><span data-stu-id="06947-105">_**Topic Last Modified:** 2013-01-29_</span></span>

<span data-ttu-id="06947-106">Tiene tres opciones para configurar las direcciones IP en Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06947-106">You have three options when configuring IP addresses in Lync Server 2013.</span></span> <span data-ttu-id="06947-107">Puede configurar Lync Server 2013 para que admita solo IP versión 4 (IPv4), solo IP versión 6 (IPv6) o una combinación de ambos (conocido como una *pila doble*).</span><span class="sxs-lookup"><span data-stu-id="06947-107">You can configure Lync Server 2013 to support only IP version 4 (IPv4), only IP version 6 (IPv6), or a combination of both (known as a *dual stack*).</span></span> <span data-ttu-id="06947-108">Cada tipo de configuración entraña varios aspectos que necesita tener en cuenta:</span><span class="sxs-lookup"><span data-stu-id="06947-108">There are several issues to consider with each type of configuration:</span></span>

  - <span data-ttu-id="06947-109">**Solo IPv4**   Se creó IPv6 porque el mundo se está quedando sin direcciones IPv4.</span><span class="sxs-lookup"><span data-stu-id="06947-109">**IPv4 only**   IPv6 was created because the world is running out of IPv4 addresses.</span></span> <span data-ttu-id="06947-110">En última instancia, IPv6 será totalmente compatible en todo el mundo, pero en este momento, muchas de las compañías y dispositivos que su empresa podría necesitar para comunicarse aún no son compatibles con IPv6, y es posible que no lo hagan durante algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="06947-110">Ultimately, IPv6 will be fully supported worldwide, but at this time, many companies and devices that your enterprise might need to communicate with do not yet support IPv6, and may not for some time.</span></span> <span data-ttu-id="06947-111">Una configuración de solo IPv4 le ayudará a asegurarse de que su implementación de Lync Server pueda comunicarse con la mayoría de los dispositivos existentes.</span><span class="sxs-lookup"><span data-stu-id="06947-111">An IPv4-only configuration will help to ensure that your Lync Server implementation can communicate with most existing devices.</span></span>

  - <span data-ttu-id="06947-112">**Solo IPv6**   A la inversa, una implementación de IPv6 completa, en este momento, evitará la comunicación con muchos dispositivos existentes.</span><span class="sxs-lookup"><span data-stu-id="06947-112">**IPv6 only**   Conversely, a full IPv6 implementation, at this time, will exclude communication with many existing devices.</span></span>

  - <span data-ttu-id="06947-113">**Pila dual**   Dual Stack es una red en la que se habilitan las direcciones IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="06947-113">**Dual Stack**   Dual stack is a network where both IPv4 and IPv6 addresses are enabled.</span></span> <span data-ttu-id="06947-114">Esta configuración es compatible con Lync Server 2013 porque, en la mayoría de los casos, la transición de IPv4 completa a Full-IPv6 llevará varios años.</span><span class="sxs-lookup"><span data-stu-id="06947-114">This configuration is supported in Lync Server 2013 because in most cases the transition from full-IPv4 to full-IPv6 will take several years.</span></span>

<span data-ttu-id="06947-115">En las secciones siguientes se describe la compatibilidad entre estas tres configuraciones para varias características de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="06947-115">The following sections outline the compatibility among these three configurations for various Lync Server features.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="06947-p104">La configuración de tipo solo IPv6 en el cliente o el servidor solo se admite en entornos de laboratorio y con fines de validación, no se admite en implementaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="06947-p104">Client or server configuration with IPv6 only is supported only for lab or validation purposes. IPv6 only configuration is not supported in the production deployment.</span></span>



</div>

<div>

## <a name="client-registration"></a><span data-ttu-id="06947-118">Registro de clientes</span><span class="sxs-lookup"><span data-stu-id="06947-118">Client Registration</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06947-119">Red de extremo de cliente</span><span class="sxs-lookup"><span data-stu-id="06947-119">Client endpoint network</span></span></th>
<th><span data-ttu-id="06947-120">Red del servidor</span><span class="sxs-lookup"><span data-stu-id="06947-120">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06947-121">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-121">IPv4</span></span></p></td>
<td><p><span data-ttu-id="06947-122">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-122">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-123">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-123">IPv4</span></span></p></td>
<td><p><span data-ttu-id="06947-124">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-124">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-125">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-125">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-126">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-126">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-127">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-127">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-128">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-128">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-129">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-129">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-130">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-130">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-131">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-131">IPv6</span></span></p></td>
<td><p><span data-ttu-id="06947-132">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-132">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-133">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-133">IPv6</span></span></p></td>
<td><p><span data-ttu-id="06947-134">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-134">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="peer-to-peer-client"></a><span data-ttu-id="06947-135">Cliente de punto a punto</span><span class="sxs-lookup"><span data-stu-id="06947-135">Peer-to-Peer Client</span></span>

<span data-ttu-id="06947-p105">Las comunicaciones de punto a punto incluyen audio, audio y vídeo, uso compartido de aplicaciones y transferencia de archivos. Después de que se hayan registrado con éxito ambos clientes, se admiten las combinaciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="06947-p105">Peer-to-peer communications include audio, audio/video, application sharing, and file transfer. After both clients have successfully registered, the following combinations are supported.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06947-138">Extremo de cliente 1</span><span class="sxs-lookup"><span data-stu-id="06947-138">Client endpoint 1</span></span></th>
<th><span data-ttu-id="06947-139">Extremo de cliente 2</span><span class="sxs-lookup"><span data-stu-id="06947-139">Client endpoint 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06947-140">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-140">IPv4</span></span></p></td>
<td><p><span data-ttu-id="06947-141">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-141">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-142">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-142">IPv4</span></span></p></td>
<td><p><span data-ttu-id="06947-143">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-143">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-144">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-144">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-145">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-145">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-146">IPv6</span></span></p></td>
<td><p><span data-ttu-id="06947-147">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-147">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-148">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-148">IPv6</span></span></p></td>
<td><p><span data-ttu-id="06947-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-149">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="conferencing"></a><span data-ttu-id="06947-150">Conferencia</span><span class="sxs-lookup"><span data-stu-id="06947-150">Conferencing</span></span>

<span data-ttu-id="06947-151">Las conferencias incluyen audio/vídeo, uso compartido de aplicaciones y colaboración de datos (pizarras y uso compartido de archivos).</span><span class="sxs-lookup"><span data-stu-id="06947-151">Conferencing includes audio/video, application sharing, and data collaboration (whiteboarding and file sharing).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06947-152">Red de extremo de cliente</span><span class="sxs-lookup"><span data-stu-id="06947-152">Client endpoint network</span></span></th>
<th><span data-ttu-id="06947-153">Red del servidor</span><span class="sxs-lookup"><span data-stu-id="06947-153">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06947-154">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-154">IPv4</span></span></p></td>
<td><p><span data-ttu-id="06947-155">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-155">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-156">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-156">IPv4</span></span></p></td>
<td><p><span data-ttu-id="06947-157">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-157">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-158">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-158">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-159">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-159">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-160">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-160">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-161">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-161">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-162">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-162">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-163">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-163">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-164">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-164">IPv6</span></span></p></td>
<td><p><span data-ttu-id="06947-165">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-165">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-166">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-166">IPv6</span></span></p></td>
<td><p><span data-ttu-id="06947-167">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-167">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="mediation-serverpstn"></a><span data-ttu-id="06947-168">Servidor de mediación/RTC</span><span class="sxs-lookup"><span data-stu-id="06947-168">Mediation Server/PSTN</span></span>

<span data-ttu-id="06947-169">Lync Server 2013 no admite omisión de multimedia para llamadas de red telefónica conmutada (RTC) si el tráfico se realiza a través de una interfaz de IPv6.</span><span class="sxs-lookup"><span data-stu-id="06947-169">Lync Server 2013 does not support media bypass for public switched telephone network (PSTN) calls if the traffic is through an IPv6 interface.</span></span> <span data-ttu-id="06947-170">Si se requiere la omisión de medios, recomendamos que la puerta de enlace RTC se configure con IPv4.</span><span class="sxs-lookup"><span data-stu-id="06947-170">If media bypass is required, we recommend that the PSTN gateway is configured to IPv4.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06947-171">Interfaz principal\*</span><span class="sxs-lookup"><span data-stu-id="06947-171">Primary interface\*</span></span></th>
<th><span data-ttu-id="06947-172">Interfaz RTC (en el servidor de mediación)</span><span class="sxs-lookup"><span data-stu-id="06947-172">PSTN interface (on Mediation Server)</span></span></th>
<th><span data-ttu-id="06947-173">Configuración de la puerta de enlace RTC</span><span class="sxs-lookup"><span data-stu-id="06947-173">PSTN gateway setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06947-174">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-174">IPv4</span></span></p></td>
<td><p><span data-ttu-id="06947-175">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-175">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-176">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-176">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-177">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-177">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-178">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-178">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-179">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-179">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-180">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-180">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-181">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-181">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-182">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-182">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="06947-183">\* La interfaz principal es la interfaz que se comunica con los componentes de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="06947-183">\* The primary interface is the interface that communicates with the Lync Server components.</span></span>

</div>

<div>

## <a name="remote-user-peer-to-peer-communications"></a><span data-ttu-id="06947-184">Comunicaciones de punto a punto de usuarios remotos</span><span class="sxs-lookup"><span data-stu-id="06947-184">Remote User Peer-to-Peer Communications</span></span>

<span data-ttu-id="06947-185">Las comunicaciones de punto a punto con usuarios remotos incluyen mensajería instantánea, audio y vídeo, uso compartido de aplicaciones y transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="06947-185">Peer-to-peer communications with remote users include instant messaging, audio/video, application sharing, and file transfer.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06947-186">Red de usuarios remotos</span><span class="sxs-lookup"><span data-stu-id="06947-186">Remote user network</span></span></th>
<th><span data-ttu-id="06947-187">Servidor perimetral (perímetro externo)</span><span class="sxs-lookup"><span data-stu-id="06947-187">Edge server (External edge)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06947-188">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-188">IPv4</span></span></p></td>
<td><p><span data-ttu-id="06947-189">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-189">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-190">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-190">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-191">IPv4</span><span class="sxs-lookup"><span data-stu-id="06947-191">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-192">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-192">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="06947-193">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-193">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-194">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-194">IPv6</span></span></p></td>
<td><p><span data-ttu-id="06947-195">Pila dual</span><span class="sxs-lookup"><span data-stu-id="06947-195">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-196">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-196">IPv6</span></span></p></td>
<td><p><span data-ttu-id="06947-197">IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-197">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="front-end-pool-and-edge-pool-configuration"></a><span data-ttu-id="06947-198">Configuración del grupo de servidores front-end y del grupo de servidores perimetrales</span><span class="sxs-lookup"><span data-stu-id="06947-198">Front End Pool and Edge Pool Configuration</span></span>

<span data-ttu-id="06947-199">En la tabla siguiente se muestra la matriz de soporte técnico entre el grupo de servidores front-end y el grupo de servidores perimetrales internos.</span><span class="sxs-lookup"><span data-stu-id="06947-199">The following table shows the support matrix between the Front End Server pool and the internal Edge Server pool.</span></span>

### <a name="front-end-pool-and-edge-pool-internal-edge-matrix"></a><span data-ttu-id="06947-200">Matriz del grupo de servidores front-end y del grupo de servidores perimetrales (perímetro interno)</span><span class="sxs-lookup"><span data-stu-id="06947-200">Front End Pool and Edge Pool (Internal Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="06947-201"><strong>Grupo de servidores perimetrales: IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="06947-201"><strong>Edge Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-202"><strong>Grupo de servidores perimetrales: pila dual</strong></span><span class="sxs-lookup"><span data-stu-id="06947-202"><strong>Edge Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-203"><strong>Grupo de servidores perimetrales: IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="06947-203"><strong>Edge Pool: IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-204"><strong>Grupo de servidores front-end: IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="06947-204"><strong>Front End Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-205">Sí</span><span class="sxs-lookup"><span data-stu-id="06947-205">Yes</span></span></p></td>
<td><p><span data-ttu-id="06947-206">Sí</span><span class="sxs-lookup"><span data-stu-id="06947-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="06947-207">No</span><span class="sxs-lookup"><span data-stu-id="06947-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-208"><strong>Grupo de servidores front-end: pila dual</strong></span><span class="sxs-lookup"><span data-stu-id="06947-208"><strong>Front End Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-209">Sí</span><span class="sxs-lookup"><span data-stu-id="06947-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="06947-210">Sí</span><span class="sxs-lookup"><span data-stu-id="06947-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="06947-211">No</span><span class="sxs-lookup"><span data-stu-id="06947-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-212"><strong>Grupo de servidores front-end: IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="06947-212"><strong>Front End Pool: IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-213">No</span><span class="sxs-lookup"><span data-stu-id="06947-213">No</span></span></p></td>
<td><p><span data-ttu-id="06947-214">No</span><span class="sxs-lookup"><span data-stu-id="06947-214">No</span></span></p></td>
<td><p><span data-ttu-id="06947-215">Sí</span><span class="sxs-lookup"><span data-stu-id="06947-215">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="06947-216">\* Use esta combinación solo en un entorno de laboratorio.</span><span class="sxs-lookup"><span data-stu-id="06947-216">\* Use this combination only in a lab environment.</span></span>

<span data-ttu-id="06947-217">La tabla siguiente es una matriz de combinaciones admitidas de las interfaces perimetrales interna y externa.</span><span class="sxs-lookup"><span data-stu-id="06947-217">The following table is a matrix of the supported combinations of internal and external edge interfaces.</span></span>

### <a name="edge-pool-internal-edge-and-edge-pool-external-edge-matrix"></a><span data-ttu-id="06947-218">Matriz del grupo de servidores perimetrales (perímetro interno) y del grupo de servidores perimetrales (perímetro externo)</span><span class="sxs-lookup"><span data-stu-id="06947-218">Edge Pool (Internal Edge) and Edge pool (External Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="06947-219"><strong>Grupo de servidores perimetrales (perímetro externo): IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="06947-219"><strong>Edge Pool (External Edge) : IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-220"><strong>Grupo de servidores perimetrales (perímetro externo): pila dual</strong></span><span class="sxs-lookup"><span data-stu-id="06947-220"><strong>Edge Pool (External Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-221"><strong>Grupo de servidores perimetrales (perímetro externo): IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="06947-221"><strong>Edge Pool (External Edge): IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-222"><strong>Grupo de servidores perimetrales (perímetro interno): IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="06947-222"><strong>Edge Pool (Internal Edge): IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-223">Sí</span><span class="sxs-lookup"><span data-stu-id="06947-223">Yes</span></span></p></td>
<td><p><span data-ttu-id="06947-224">Sí</span><span class="sxs-lookup"><span data-stu-id="06947-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="06947-225">No</span><span class="sxs-lookup"><span data-stu-id="06947-225">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06947-226"><strong>Grupo de servidores perimetrales (perímetro interno): pila dual</strong></span><span class="sxs-lookup"><span data-stu-id="06947-226"><strong>Edge Pool (Internal Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-227">No</span><span class="sxs-lookup"><span data-stu-id="06947-227">No</span></span></p></td>
<td><p><span data-ttu-id="06947-228">Sí</span><span class="sxs-lookup"><span data-stu-id="06947-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="06947-229">No</span><span class="sxs-lookup"><span data-stu-id="06947-229">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06947-230"><strong>Grupo de servidores perimetrales (perímetro interno): IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="06947-230"><strong>Edge Pool (Internal Edge): IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="06947-231">No</span><span class="sxs-lookup"><span data-stu-id="06947-231">No</span></span></p></td>
<td><p><span data-ttu-id="06947-232">No</span><span class="sxs-lookup"><span data-stu-id="06947-232">No</span></span></p></td>
<td><p><span data-ttu-id="06947-233">Sí</span><span class="sxs-lookup"><span data-stu-id="06947-233">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="06947-234">\* Use esta combinación solo en un entorno de laboratorio.</span><span class="sxs-lookup"><span data-stu-id="06947-234">\* Use this combination only in a lab environment.</span></span>

</div>

<div>

## <a name="advanced-enterprise-voice-support-for-ipv6"></a><span data-ttu-id="06947-235">Compatibilidad avanzada de Telefonía IP empresarial para IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-235">Advanced Enterprise Voice Support for IPv6</span></span>

<span data-ttu-id="06947-236">Las implementaciones que incluyen el control de admisión de llamadas (CAC), Enhanced 9-1-1 (E9-1-1) o la omisión de medios se deben configurar como implementaciones de solo IPv4 o de pila dual.</span><span class="sxs-lookup"><span data-stu-id="06947-236">Deployments that include call admission control (CAC), Enhanced 9-1-1 (E9-1-1), or media bypass must be configured as IPv4 only or as a dual-stacked implementation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="06947-237">En una implementación con dos pilas, incluso si un cliente de Lync se conecta a un servidor de Lync mediante IPv6, Lync hará todo lo posible para asignar una dirección IPv4 adecuada para admitir E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="06947-237">In a dual-stacked deployment, even if a Lync client connects to a Lync Server by using IPv6, Lync will make a best effort to map an appropriate IPv4 address to support E9-1-1.</span></span>



</div>

<span data-ttu-id="06947-238">No se admite el servicio de información de ubicación con direcciones IPv6.</span><span class="sxs-lookup"><span data-stu-id="06947-238">Location Information service with IPv6 addresses is not supported.</span></span>

<span data-ttu-id="06947-p107">La mensajería unificada (MU) de Exchange no admite IPv6. Para la MU de Exchange, asegúrese de que la resolución de DNS no devuelve una dirección IPv6. El uso de IPv6 puede provocar un fallo cuando se envían las llamadas al correo de voz.</span><span class="sxs-lookup"><span data-stu-id="06947-p107">Exchange Unified Messaging (UM) does not support IPv6. For Exchange UM, be sure that DNS resolution does not return an IPv6 address. Using IPv6 may cause failure when calls are sent to voice mail.</span></span>

</div>

<div>

## <a name="other-lync-server-2013-feature-support-for-ipv6"></a><span data-ttu-id="06947-242">Otra compatibilidad con características de Lync Server 2013 para IPv6</span><span class="sxs-lookup"><span data-stu-id="06947-242">Other Lync Server 2013 Feature Support for IPv6</span></span>

<span data-ttu-id="06947-243">Además de las características y componentes mencionados anteriormente, Lync Server 2013 admite IPv6 para las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="06947-243">In addition to the features and components mentioned previously, Lync Server 2013 supports IPv6 for the following features:</span></span>

  - <span data-ttu-id="06947-244">**Chat persistente**</span><span class="sxs-lookup"><span data-stu-id="06947-244">**Persistent Chat**</span></span>
    
    <span data-ttu-id="06947-245">Para configurar IPv6 para la conversación persistente, use el generador de topología.</span><span class="sxs-lookup"><span data-stu-id="06947-245">You configure IPv6 for Persistent Chat by using Topology Builder.</span></span> <span data-ttu-id="06947-246">Para obtener más información sobre cómo configurar una conversación persistente, consulte la documentación de implementación del servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="06947-246">For details about configuring Persistent Chat, see the Deploying Persistent Chat Server documentation.</span></span>

  - <span data-ttu-id="06947-247">**Informes de Calidad de la experiencia (QoE) y registro detallado de llamadas (CDR)**</span><span class="sxs-lookup"><span data-stu-id="06947-247">**Quality of Experience (QoE) and call detail recording (CDR) reports**</span></span>
    
    <span data-ttu-id="06947-248">Los informes de supervisión incluyen la dirección IP cuando se guarda en la base de datos del servidor de supervisión, tanto del tipo IPv4 como IPv6.</span><span class="sxs-lookup"><span data-stu-id="06947-248">Monitoring reports include the IP address as it is stored in the Monitoring Server database, whether of type IPv4 or IPv6.</span></span>

<span data-ttu-id="06947-249"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06947-249"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

