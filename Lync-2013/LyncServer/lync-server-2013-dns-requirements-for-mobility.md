---
title: 'Lync Server 2013: requisitos de DNS para movilidad'
description: 'Lync Server 2013: requisitos de DNS para la movilidad.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for mobility
ms:assetid: df6962bc-2a16-440e-a333-022ebd14f957
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690040(v=OCS.15)
ms:contentKeyID: 48185624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2a8377dc7c856bb7250817cb3b8b66ed7789d3b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437808"
---
# <a name="dns-requirements-for-mobility-with-lync-server-2013"></a><span data-ttu-id="bc268-103">Requisitos de DNS para movilidad con Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc268-103">DNS requirements for mobility with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc268-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc268-104">

<span> </span></span></span>

<span data-ttu-id="bc268-105">_**Última modificación del tema:** 2012-11-13_</span><span class="sxs-lookup"><span data-stu-id="bc268-105">_**Topic Last Modified:** 2012-11-13_</span></span>

<span data-ttu-id="bc268-106">Al implementar la característica de movilidad de Lync Server 2013, puede usar las nuevas direcciones URL que están disponibles con el servicio Detección automática de Microsoft Lync Server 2013 o puede usar las direcciones URL de los servicios Web existentes.</span><span class="sxs-lookup"><span data-stu-id="bc268-106">When you deploy the Lync Server 2013 mobility feature, you can use the new URLs that are available with the Microsoft Lync Server 2013 Autodiscover Service, or you can use your existing Web Services URLs.</span></span> <span data-ttu-id="bc268-107">Si usa las direcciones URL existentes, los usuarios necesitan introducir manualmente las direcciones URL en la configuración del dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="bc268-107">If you use your existing URLs, users need to manually enter the URLs in their mobile device settings.</span></span> <span data-ttu-id="bc268-108">Normalmente, esta opción se usa para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="bc268-108">This option is typically used for troubleshooting.</span></span> <span data-ttu-id="bc268-109">Al usar las nuevas direcciones URL, los clientes móviles pueden descubrir automáticamente recursos de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bc268-109">When you use the new URLs, mobile clients can automatically discover Lync Server 2013 resources.</span></span> <span data-ttu-id="bc268-110">Cuando admite la detección automática, necesita agregar los registros del sistema de nombres de dominio (DNS) nuevos.</span><span class="sxs-lookup"><span data-stu-id="bc268-110">When you support automatic discovery, you need to add new Domain Name System (DNS) records.</span></span> <span data-ttu-id="bc268-111">En esta sección se describen los registros de DNS necesarios para la detección automática.</span><span class="sxs-lookup"><span data-stu-id="bc268-111">This section describes the DNS records that are required for automatic discovery.</span></span>

<span data-ttu-id="bc268-112">Para admitir la detección automática, cree los siguientes registros de DNS para cada dominio SIP:</span><span class="sxs-lookup"><span data-stu-id="bc268-112">To support automatic discovery, you need to create the following DNS records for each SIP domain:</span></span>

  - <span data-ttu-id="bc268-113">Un registro de DNS interno para admitir usuarios móviles que se conectan desde la red de su organización</span><span class="sxs-lookup"><span data-stu-id="bc268-113">An internal DNS record to support mobile users who connect from within your organization's network</span></span>

  - <span data-ttu-id="bc268-114">Un registro de DNS externo, o público, para admitir usuarios móviles que se conectan desde Internet</span><span class="sxs-lookup"><span data-stu-id="bc268-114">An external, or public, DNS record to support mobile users who connect from the Internet</span></span>

<span data-ttu-id="bc268-p102">La URL de detección automática interna no tiene que ser direccionable desde fuera de su red. La dirección URL de detección automática externa no tiene que ser direccionable desde dentro de su red. Pero, si no cumple este requisito para la dirección URL externa, la funcionalidad del cliente móvil no tendría que verse afectada.</span><span class="sxs-lookup"><span data-stu-id="bc268-p102">The internal automatic discovery URL should not be addressable from outside your network. The external automatic discovery URL should not be addressable from within your network. However, if you cannot meet this requirement for the external URL, mobile client functionally should not be affected.</span></span>

<span data-ttu-id="bc268-118">Los registros de DNS pueden ser registros CNAME o registros A (host).</span><span class="sxs-lookup"><span data-stu-id="bc268-118">The DNS records can be either CNAME records or A (host) records.</span></span>

<span data-ttu-id="bc268-119">**Registros de DNS internos**</span><span class="sxs-lookup"><span data-stu-id="bc268-119">**Internal DNS records**</span></span>

<span data-ttu-id="bc268-120">Cree uno de los siguientes registros de DNS internos:</span><span class="sxs-lookup"><span data-stu-id="bc268-120">You need to create one of the following internal DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc268-121">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="bc268-121">Record type</span></span></th>
<th><span data-ttu-id="bc268-122">Nombre de host o definición SRV</span><span class="sxs-lookup"><span data-stu-id="bc268-122">Host name or SRV definition</span></span></th>
<th><span data-ttu-id="bc268-123">Se resuelve en</span><span class="sxs-lookup"><span data-stu-id="bc268-123">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc268-124">CNAME</span><span class="sxs-lookup"><span data-stu-id="bc268-124">CNAME</span></span></p></td>
<td><p><span data-ttu-id="bc268-125">lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="bc268-125">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="bc268-126">Nombre de dominio completo (FQDN) de servicios Web internos para el grupo de directores, si tiene uno, o para el grupo de servidores front-end si no tiene un director</span><span class="sxs-lookup"><span data-stu-id="bc268-126">Internal Web Services fully qualified domain name (FQDN) for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc268-127">A (host)</span><span class="sxs-lookup"><span data-stu-id="bc268-127">A (host)</span></span></p></td>
<td><p><span data-ttu-id="bc268-128">lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="bc268-128">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="bc268-129">Dirección IP de los servicios Web internos (dirección IP virtual (VIP) si usa un equilibrador de carga) de su grupo de directores, si tiene uno o el grupo de servidores front-end si no tiene un director</span><span class="sxs-lookup"><span data-stu-id="bc268-129">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bc268-130">**Registros de DNS externos**</span><span class="sxs-lookup"><span data-stu-id="bc268-130">**External DNS records**</span></span>

<span data-ttu-id="bc268-131">Cree uno de los siguientes registros de DNS externos:</span><span class="sxs-lookup"><span data-stu-id="bc268-131">You need to create one of the following external DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc268-132">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="bc268-132">Record type</span></span></th>
<th><span data-ttu-id="bc268-133">Nombre de host</span><span class="sxs-lookup"><span data-stu-id="bc268-133">Host name</span></span></th>
<th><span data-ttu-id="bc268-134">Se resuelve en</span><span class="sxs-lookup"><span data-stu-id="bc268-134">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc268-135">CNAME</span><span class="sxs-lookup"><span data-stu-id="bc268-135">CNAME</span></span></p></td>
<td><p><span data-ttu-id="bc268-136">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="bc268-136">lyncdiscover.</span></span> <span data-ttu-id="bc268-137">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="bc268-137">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="bc268-138">El FQDN de servicios web externos para el grupo de directores, si tiene uno, o para el grupo de servidores front-end si no tiene un director</span><span class="sxs-lookup"><span data-stu-id="bc268-138">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc268-139">A (host)</span><span class="sxs-lookup"><span data-stu-id="bc268-139">A (host)</span></span></p></td>
<td><p><span data-ttu-id="bc268-140">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="bc268-140">lyncdiscover.</span></span> <span data-ttu-id="bc268-141">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="bc268-141">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="bc268-142">Dirección IP externa o pública (dirección VIP si usa un equilibrador de carga) del proxy inverso</span><span class="sxs-lookup"><span data-stu-id="bc268-142">External or public IP address (VIP address if you use a load balancer) of the reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc268-143">SRV</span><span class="sxs-lookup"><span data-stu-id="bc268-143">SRV</span></span></p></td>
<td><p><span data-ttu-id="bc268-144">_sipfederationtls._tcp.</span><span class="sxs-lookup"><span data-stu-id="bc268-144">_sipfederationtls._tcp.</span></span> <span data-ttu-id="bc268-145">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="bc268-145">&lt;sipdomain&gt;</span></span></p>
<p><span data-ttu-id="bc268-146">Se resuelve en un registro de host (A o AAAA) para el servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="bc268-146">Resolves to host (A or AAAA) record for the Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="bc268-147">Para admitir el servicio de notificaciones de inserción y el servicio de notificaciones push de Apple, puede crear un registro SRV para cada dominio SIP que tenga clientes móviles de Microsoft Lync.</span><span class="sxs-lookup"><span data-stu-id="bc268-147">To support Push Notification Service and Apple Push Notification service, you create one SRV record for each SIP domain that has Microsoft Lync Mobile clients.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="bc268-148">Este requisito se aplica únicamente a los clientes móviles de Microsoft Lync en Apple o en dispositivos móviles basados en Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bc268-148">This requirement applies only to Microsoft Lync Mobile clients on Apple or Microsoft based mobile devices.</span></span> <span data-ttu-id="bc268-149">Android y los dispositivos Nokia Symbian no usan la notificación push.</span><span class="sxs-lookup"><span data-stu-id="bc268-149">Andriod and Nokia Symbian devices do not use push notification.</span></span>


</div></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="bc268-150">Lyncdiscover, también conocido como detección automática, el tráfico pasa por el proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="bc268-150">Lyncdiscover, also known as autodiscover, traffic goes through the reverse proxy.</span></span> <span data-ttu-id="bc268-151">El registro SRV apunta a un registro que se resuelve a través del servicio perimetral de acceso.</span><span class="sxs-lookup"><span data-stu-id="bc268-151">SRV record points to a record that resolves through the Access Edge service.</span></span>



<span data-ttu-id="bc268-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc268-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

