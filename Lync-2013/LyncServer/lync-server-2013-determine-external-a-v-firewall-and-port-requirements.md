---
title: 'Lync Server 2013: Determinar los requisitos de los puertos y el firewall de A/V externos'
description: 'Lync Server 2013: determinar los requisitos de los puertos y el Firewall A/V externo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determine external A/V firewall and port requirements
ms:assetid: 3b849dc7-175d-40d1-820d-80e6ade6d332
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425882(v=OCS.15)
ms:contentKeyID: 48183872
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 38c2a8c1e8e332a4a1e65adb87a1e962e82941c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429517"
---
# <a name="determine-external-av-firewall-and-port-requirements-for-lync-server-2013"></a><span data-ttu-id="c55b4-103">Determinar los requisitos de los puertos y el firewall de A/V externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c55b4-103">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c55b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c55b4-104">

<span> </span></span></span>

<span data-ttu-id="c55b4-105">_**Última modificación del tema:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="c55b4-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="c55b4-106">La comunicación de audio/vídeo (A/V) puede ser compleja.</span><span class="sxs-lookup"><span data-stu-id="c55b4-106">Audio/Video (A/V) communication can be a complex.</span></span> <span data-ttu-id="c55b4-107">Debido a la naturaleza de los protocolos que se usan en A/V y a la forma en que los clientes y servidores usan los protocolos, se garantiza una sección especial para explicar las diferencias entre las versiones de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="c55b4-107">Because of the nature of protocols used in A/V and how clients and servers use the protocols, a special section is warranted to explain the differences between client and server versions.</span></span>

<span data-ttu-id="c55b4-108">Use la siguiente tabla de puertos y de Firewall a/V para determinar los requisitos de firewall y qué puertos se deben abrir.</span><span class="sxs-lookup"><span data-stu-id="c55b4-108">Use the following A/V Firewall and Port table to determine firewall requirements and which ports to open.</span></span> <span data-ttu-id="c55b4-109">A continuación, revise la terminología de traducción de direcciones de red (NAT) porque NAT se puede implementar de muchas formas diferentes.</span><span class="sxs-lookup"><span data-stu-id="c55b4-109">Then, review the network address translation (NAT) terminology because NAT can be implemented in many different ways.</span></span> <span data-ttu-id="c55b4-110">Para obtener un ejemplo detallado de la configuración del puerto del firewall, vea las arquitecturas de referencia en [escenarios para el acceso de usuarios externos en Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="c55b4-110">For a detailed example of firewall port settings, see the reference architectures in [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

### <a name="general-protocol-usage-for-udp-and-tcp-in-audiovideo-and-media-traffic"></a><span data-ttu-id="c55b4-111">Uso general del protocolo para UDP y TCP en el tráfico de audio, vídeo y multimedia</span><span class="sxs-lookup"><span data-stu-id="c55b4-111">General Protocol Usage for UDP and TCP in Audio/Video and Media Traffic</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c55b4-112">Transporte de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="c55b4-112">Audio/Video Transport</span></span></th>
<th><span data-ttu-id="c55b4-113">Uso</span><span class="sxs-lookup"><span data-stu-id="c55b4-113">Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c55b4-114">UDP</span><span class="sxs-lookup"><span data-stu-id="c55b4-114">UDP</span></span></p></td>
<td><p><span data-ttu-id="c55b4-115">Protocolo de capa de transporte preferido para audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="c55b4-115">Preferred transport layer protocol for audio and video</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c55b4-116">TCP</span><span class="sxs-lookup"><span data-stu-id="c55b4-116">TCP</span></span></p></td>
<td><p><span data-ttu-id="c55b4-117">Protocolo de nivel de transporte de reserva para audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="c55b4-117">Fallback transport layer protocol for audio and video</span></span></p>
<p><span data-ttu-id="c55b4-118">Protocolo de capa de transporte requerido para compartir aplicaciones a Office Communications Server 2007 R2, Lync Server 2010 y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c55b4-118">Required transport layer protocol for application sharing to Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013</span></span></p>
<p><span data-ttu-id="c55b4-119">Protocolo de nivel de transporte requerido para la transferencia de archivos a Lync Server 2010 y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c55b4-119">Required transport layer protocol for file transfer to Lync Server 2010 and Lync Server 2013</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="external-av-firewall-port-requirements-for-external-user-access"></a><span data-ttu-id="c55b4-120">Requisitos del puerto de Firewall A/V externo para el acceso de usuarios externos</span><span class="sxs-lookup"><span data-stu-id="c55b4-120">External A/V Firewall Port Requirements for External User Access</span></span>

<span data-ttu-id="c55b4-121">Los requisitos de puerto de Firewall para las interfaces SIP y de conferencia externas (y internas) son coherentes, independientemente de la versión de su cliente o de la versión del socio de Federación.</span><span class="sxs-lookup"><span data-stu-id="c55b4-121">The firewall port requirements for external (and internal) SIP and conferencing interfaces are consistent, regardless of the version of your client or the version of the federation partner.</span></span>

<span data-ttu-id="c55b4-122">Lo mismo no sucede con la interfaz externa del borde de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="c55b4-122">The same is not true for the Audio/Video Edge external interface.</span></span> <span data-ttu-id="c55b4-123">Para la Federación con Office Communications Server 2007, el servicio perimetral A/V requiere que las reglas de Firewall externas permitan el tráfico RTP/TCP y RTP/UDP en el intervalo de puertos de 50.000 a 59.999 y fluyan en ambas direcciones.</span><span class="sxs-lookup"><span data-stu-id="c55b4-123">For federation with Office Communications Server 2007, the A/V Edge service requires that external firewall rules allow RTP/TCP and RTP/UDP traffic in the 50,000 through 59,999 port range to flow in both directions.</span></span> <span data-ttu-id="c55b4-124">En la tabla anterior se supone que Lync Server 2013 es el socio de Federación principal y que se está configurando para comunicarse con uno de los otros tipos de asociados de Federación de la lista.</span><span class="sxs-lookup"><span data-stu-id="c55b4-124">The previous table assumes that Lync Server 2013 is the primary federation partner and it is being configured to communicate with one of the other federation partner types listed.</span></span>

<span data-ttu-id="c55b4-125">La configuración del intervalo de puertos de audio/vídeo de 50000-59.999 sesiones debe tener en cuenta que el intervalo de puertos contendrá los puertos de origen de las comunicaciones con los socios de la Federación.</span><span class="sxs-lookup"><span data-stu-id="c55b4-125">Configuring the Audio/Video port range of 50,000-59,999 must take into account that the port range will contain the source ports for communications to federation partners.</span></span> <span data-ttu-id="c55b4-126">En detalle, considere la posibilidad de iniciar una comunicación desde un asociado de Federación.</span><span class="sxs-lookup"><span data-stu-id="c55b4-126">In detail, consider that a communication is initiated from a federation partner.</span></span> <span data-ttu-id="c55b4-127">La comunicación de los puertos de servicio perimetral A/V del intervalo de 50000-59.999 sesiones se conectará al puerto TCP 443 esperado del servicio perimetral A/V del socio.</span><span class="sxs-lookup"><span data-stu-id="c55b4-127">The communication from the A/V Edge service ports in the 50,000-59,999 range will connect to the expected port TCP 443 of the partner’s A/V Edge service.</span></span> <span data-ttu-id="c55b4-128">A la inversa, el tráfico entrante a su puerto de servicio perimetral de A/V TCP 443 tendrá un puerto de origen en el rango de 50.000 59.999 sesiones.</span><span class="sxs-lookup"><span data-stu-id="c55b4-128">Conversely, inbound traffic to your A/V Edge service port TCP 443 will have a source port in the range of 50,000-59,999.</span></span>

<span data-ttu-id="c55b4-129">Los distintos firewalls y directivas de administración de Firewall pueden requerir la configuración de reglas de destino, o bien pueden requerir la configuración de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="c55b4-129">Different firewalls and policies for firewall administration may require only destination rules to be configured, or they may require both source and destination to be configured.</span></span> <span data-ttu-id="c55b4-130">Si sus requisitos son solo para puertos de destino, los requisitos de audio y vídeo son:</span><span class="sxs-lookup"><span data-stu-id="c55b4-130">If your requirements are for destination ports only, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c55b4-131">IP de origen</span><span class="sxs-lookup"><span data-stu-id="c55b4-131">Source IP</span></span></th>
<th><span data-ttu-id="c55b4-132">IP de destino</span><span class="sxs-lookup"><span data-stu-id="c55b4-132">Destination IP</span></span></th>
<th><span data-ttu-id="c55b4-133">Puerto de destino</span><span class="sxs-lookup"><span data-stu-id="c55b4-133">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c55b4-134">Interfaz de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="c55b4-134">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c55b4-135">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-135">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-136">TCP 443</span><span class="sxs-lookup"><span data-stu-id="c55b4-136">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c55b4-137">Interfaz de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="c55b4-137">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c55b4-138">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-138">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-139">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c55b4-139">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c55b4-140">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-140">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-141">Interfaz de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="c55b4-141">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c55b4-142">TCP 443</span><span class="sxs-lookup"><span data-stu-id="c55b4-142">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c55b4-143">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-143">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-144">Interfaz de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="c55b4-144">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c55b4-145">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c55b4-145">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c55b4-146">Si las directivas requieren definiciones de reglas de Firewall de entrada y salida, los requisitos de audio y vídeo son:</span><span class="sxs-lookup"><span data-stu-id="c55b4-146">If your policies require both inbound and outbound firewall rule definitions, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c55b4-147">IP de origen</span><span class="sxs-lookup"><span data-stu-id="c55b4-147">Source IP</span></span></th>
<th><span data-ttu-id="c55b4-148">IP de destino</span><span class="sxs-lookup"><span data-stu-id="c55b4-148">Destination IP</span></span></th>
<th><span data-ttu-id="c55b4-149">Puerto de origen</span><span class="sxs-lookup"><span data-stu-id="c55b4-149">Source Port</span></span></th>
<th><span data-ttu-id="c55b4-150">Puerto de destino</span><span class="sxs-lookup"><span data-stu-id="c55b4-150">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c55b4-151">Interfaz de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="c55b4-151">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c55b4-152">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-152">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-153">TCP 50.000-59.999</span><span class="sxs-lookup"><span data-stu-id="c55b4-153">TCP 50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="c55b4-154">TCP 443</span><span class="sxs-lookup"><span data-stu-id="c55b4-154">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c55b4-155">Interfaz de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="c55b4-155">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c55b4-156">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-156">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-157">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c55b4-157">UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="c55b4-158">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c55b4-158">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c55b4-159">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-159">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-160">Interfaz de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="c55b4-160">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c55b4-161">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-161">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-162">TCP 443</span><span class="sxs-lookup"><span data-stu-id="c55b4-162">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c55b4-163">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-163">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-164">Interfaz de servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="c55b4-164">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="c55b4-165">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c55b4-165">Any</span></span></p></td>
<td><p><span data-ttu-id="c55b4-166">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="c55b4-166">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="c55b4-167">Microsoft Office Communications Server 2007 requiere una configuración ligeramente distinta.</span><span class="sxs-lookup"><span data-stu-id="c55b4-167">Microsoft Office Communications Server 2007 requires a slightly different configuration.</span></span> <span data-ttu-id="c55b4-168">El intervalo de puertos TCP y UDP de 50000-59.999 sesiones debe estar abierto entrante y saliente.</span><span class="sxs-lookup"><span data-stu-id="c55b4-168">The TCP and UDP port range of 50,000-59,999 must be open inbound and outbound.</span></span> <span data-ttu-id="c55b4-169">Este requisito es solo para Office Communicator 2007.</span><span class="sxs-lookup"><span data-stu-id="c55b4-169">This requirement is only for Office Communicator 2007.</span></span> <span data-ttu-id="c55b4-170">Office Communications Server 2007 R2, Lync Server 2010 y Lync Server 2013 solo requieren el intervalo TCP 50000-59.999 sesiones de salida abierto.</span><span class="sxs-lookup"><span data-stu-id="c55b4-170">Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013 only require TCP range 50,000-59,999 open outbound.</span></span>



</div>

</div>

<div>

## <a name="nat-requirements-for-the-edge-service"></a><span data-ttu-id="c55b4-171">Requisitos de NAT para el servicio perimetral</span><span class="sxs-lookup"><span data-stu-id="c55b4-171">NAT requirements for the Edge service</span></span>

<span data-ttu-id="c55b4-172">Si decide configurar direcciones IP privadas no enrutables para el servicio perimetral, se aplicarán los siguientes requisitos de NAT:</span><span class="sxs-lookup"><span data-stu-id="c55b4-172">The following NAT requirements apply if you choose to configure non-routable private IP addresses for the Edge service:</span></span>

  - <span data-ttu-id="c55b4-173">NAT solo se puede usar con el equilibrio de carga de DNS.</span><span class="sxs-lookup"><span data-stu-id="c55b4-173">NAT can only be used with DNS load-balancing.</span></span> <span data-ttu-id="c55b4-174">NAT no es compatible con una topología perimetral de equilibrio de carga de hardware (HLB).</span><span class="sxs-lookup"><span data-stu-id="c55b4-174">NAT is not supported with a hardware load balancing (HLB) Edge topology.</span></span>

  - <span data-ttu-id="c55b4-175">NAT solo se puede usar en la interfaz de borde externo.</span><span class="sxs-lookup"><span data-stu-id="c55b4-175">NAT can only be used on the external Edge interface.</span></span> <span data-ttu-id="c55b4-176">NAT no es compatible con la interfaz de borde interno.</span><span class="sxs-lookup"><span data-stu-id="c55b4-176">NAT is not supported on the internal Edge interface.</span></span>

  - <span data-ttu-id="c55b4-177">NAT debe ser simétrico para el tráfico entrante y saliente.</span><span class="sxs-lookup"><span data-stu-id="c55b4-177">NAT must be symmetric for incoming and outgoing traffic.</span></span>
    
  - <span data-ttu-id="c55b4-178">Para el tráfico de Internet, NAT debe cambiar la dirección IP de destino de la dirección IP pública habilitada para NAT del servicio perimetral a/V a su dirección IP externa.</span><span class="sxs-lookup"><span data-stu-id="c55b4-178">For traffic from the Internet, NAT must change the destination IP address from the NAT-enabled public IP address of the A/V Edge service to its external IP address.</span></span> <span data-ttu-id="c55b4-179">La dirección IP de origen debe permanecer intacta, de modo que el servicio perimetral A/V pueda encontrar la ruta de medios óptima.</span><span class="sxs-lookup"><span data-stu-id="c55b4-179">The source IP address must remain intact, so that the A/V Edge service can find the optimal media path.</span></span>
  
  <span data-ttu-id="c55b4-180">Por ejemplo, en la dirección de entrada en la siguiente ilustración, la dirección IP pública 131.107.155.30 se cambió a la dirección IP externa (privada) 10.45.16.10.</span><span class="sxs-lookup"><span data-stu-id="c55b4-180">For example, in the inbound direction in the figure below, the public IP address 131.107.155.30 was changed to the external (private) IP address 10.45.16.10.</span></span> <span data-ttu-id="c55b4-181">La dirección IP de origen permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="c55b4-181">The source IP address remained unchanged.</span></span>
  
  - <span data-ttu-id="c55b4-182">Para el tráfico del servicio perimetral a/V a Internet, NAT debe cambiar la dirección IP de origen de la dirección IP externa del servicio perimetral a/V a la dirección IP pública habilitada para NAT.</span><span class="sxs-lookup"><span data-stu-id="c55b4-182">For traffic from the A/V Edge service to the Internet, NAT must change the source IP address from the external IP address of the A/V Edge service to the NAT-enabled public IP address.</span></span>

<span data-ttu-id="c55b4-183">Por ejemplo, en la dirección de salida de la siguiente ilustración, el 10.45.16.10 de la dirección IP externa (privada) se cambió a la dirección IP pública 131.107.155.30.</span><span class="sxs-lookup"><span data-stu-id="c55b4-183">For example, in the outbound direction in the figure below, the external (private) IP address 10.45.16.10 was changed to the public IP address 131.107.155.30.</span></span>

<span data-ttu-id="c55b4-184">**En la siguiente ilustración se muestra cómo la NAT cambia la dirección IP de destino para el tráfico entrante y la dirección IP de origen para el tráfico saliente.**</span><span class="sxs-lookup"><span data-stu-id="c55b4-184">**The figure below shows how NAT changes the destination IP address for inbound traffic and the source IP Address for outbound traffic.**</span></span>

<span data-ttu-id="c55b4-185">![Cambio de direcciones IP de destino/origen](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "Cambio de direcciones IP de destino/origen")</span><span class="sxs-lookup"><span data-stu-id="c55b4-185">![Changing destination/source IP addresses](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "Changing destination/source IP addresses")</span></span>

<span data-ttu-id="c55b4-186">Los puntos clave son:</span><span class="sxs-lookup"><span data-stu-id="c55b4-186">The key points are:</span></span>

  - <span data-ttu-id="c55b4-187">El tráfico entrante al servidor que ejecuta el servicio perimetral A/V, la dirección IP de origen no cambia, pero la dirección IP de destino cambia de 131.107.155.30 a la dirección IP traducida de 10.45.16.10.</span><span class="sxs-lookup"><span data-stu-id="c55b4-187">Traffic that is inbound to the server running the A/V Edge service, the source IP address does not change but the destination IP address changes from 131.107.155.30 to the translated IP address of 10.45.16.10.</span></span>

  - <span data-ttu-id="c55b4-188">El tráfico saliente del servidor que ejecuta el servicio perimetral A/V a la estación de trabajo, la dirección IP de origen cambia de la dirección IP pública del servidor a la dirección IP pública del servidor que ejecuta el servicio perimetral A/V.</span><span class="sxs-lookup"><span data-stu-id="c55b4-188">Traffic that is outbound from the server running the A/V Edge service back to the workstation, the source IP address changes from the server’s public IP address to the public IP address of the server running the A/V Edge service.</span></span> <span data-ttu-id="c55b4-189">La IP de destino sigue siendo la dirección IP pública de la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c55b4-189">The destination IP remains the workstation’s public IP address.</span></span> <span data-ttu-id="c55b4-190">Una vez que el paquete deja el primer dispositivo NAT saliente, la regla del dispositivo NAT cambia la dirección IP de origen del servidor que ejecuta la dirección IP de la interfaz externa del servicio de borde a/V (10.45.16.10) a su dirección IP pública (131.107.155.30).</span><span class="sxs-lookup"><span data-stu-id="c55b4-190">After the packet leaves the first NAT device outbound, the rule on the NAT device changes the source IP address of the server running the A/V Edge service external interface IP address (10.45.16.10) to its public IP address (131.107.155.30).</span></span>

<span data-ttu-id="c55b4-191"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c55b4-191"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

