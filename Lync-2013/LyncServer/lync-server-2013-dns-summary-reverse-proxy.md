---
title: 'Lync Server 2013: Resumen DNS - Proxy inverso'
description: 'Lync Server 2013: Resumen de DNS: proxy inverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Reverse proxy
ms:assetid: 3073affa-4d92-4453-9974-3a82ca0c6445
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204781(v=OCS.15)
ms:contentKeyID: 48183755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc2d806893786a11317be1eff9bfdc08c9230bf3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437724"
---
# <a name="dns-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="ce00b-103">Resumen DNS - Proxy inverso en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce00b-103">DNS summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce00b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce00b-104">

<span> </span></span></span>

<span data-ttu-id="ce00b-105">_**Última modificación del tema:** 2013-03-22_</span><span class="sxs-lookup"><span data-stu-id="ce00b-105">_**Topic Last Modified:** 2013-03-22_</span></span>

<span data-ttu-id="ce00b-106">Para configurar dos adaptadores de red en el proxy inverso, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ce00b-106">You configure two network adapters in your reverse proxy as follows:</span></span>

<div>

## <a name="reverse-proxy-network-adapter-requirements"></a><span data-ttu-id="ce00b-107">Requisitos del adaptador de red de proxy inverso</span><span class="sxs-lookup"><span data-stu-id="ce00b-107">Reverse Proxy Network Adapter Requirements</span></span>

  - <span data-ttu-id="ce00b-108">Ejemplo de **adaptador de red 1 (interfaz interna)**</span><span class="sxs-lookup"><span data-stu-id="ce00b-108">**Network adapter 1 (Internal Interface)** example</span></span>
    
    <span data-ttu-id="ce00b-109">Interfaz interna con 172.25.33.40 asignado.</span><span class="sxs-lookup"><span data-stu-id="ce00b-109">Internal interface with 172.25.33.40 assigned.</span></span>
    
    <span data-ttu-id="ce00b-110">No hay ninguna puerta de enlace predeterminada definida.</span><span class="sxs-lookup"><span data-stu-id="ce00b-110">No default gateway is defined.</span></span>
    
    <span data-ttu-id="ce00b-111">Asegúrese de que haya una ruta desde la red que contiene la interfaz interna de proxy inverso a cualquier red que contenga servidores de grupos de servidores de aplicaciones para el usuario de Lync Server (por ejemplo, de 172.25.33.0 a 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="ce00b-111">Ensure there is a route from the network containing the reverse proxy internal interface to any networks that contain Lync Server Front End pool servers (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="ce00b-112">Ejemplo de **adaptador de red 2 (interfaz externa)**</span><span class="sxs-lookup"><span data-stu-id="ce00b-112">**Network adapter 2 (External Interface)** example</span></span>
    
    <span data-ttu-id="ce00b-113">Se asigna al menos una dirección IP pública a este adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="ce00b-113">A minimum of one public IP address is assigned to this network adapter.</span></span>
    
    <span data-ttu-id="ce00b-114">La puerta de enlace está definida para señalar el router o el firewall integrado en el perímetro exterior.</span><span class="sxs-lookup"><span data-stu-id="ce00b-114">Gateway is defined to point to the router or integrated firewall in your outer perimeter.</span></span> <span data-ttu-id="ce00b-115">(10.45.16.1 en el escenario ejemplos)</span><span class="sxs-lookup"><span data-stu-id="ce00b-115">(10.45.16.1 in the scenario examples)</span></span>

### <a name="dns-records-required-for-reverse-proxy"></a><span data-ttu-id="ce00b-116">Registros DNS necesarios para el proxy inverso</span><span class="sxs-lookup"><span data-stu-id="ce00b-116">DNS Records Required for Reverse Proxy</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce00b-117">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="ce00b-117">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="ce00b-118">FQDN</span><span class="sxs-lookup"><span data-stu-id="ce00b-118">FQDN</span></span></th>
<th><span data-ttu-id="ce00b-119">Dirección IP</span><span class="sxs-lookup"><span data-stu-id="ce00b-119">IP address</span></span></th>
<th><span data-ttu-id="ce00b-120">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="ce00b-120">Maps to/comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce00b-121">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="ce00b-121">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ce00b-122">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ce00b-122">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ce00b-123">Escucha asignada para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="ce00b-123">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="ce00b-124">Servicios web externos de la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="ce00b-124">External web services from the internal deployment.</span></span> <span data-ttu-id="ce00b-125">Se pueden definir y crear registros adicionales para todos los grupos y servidores únicos para cualquier dominio SIP que use este proxy inverso y para los que haya definido servicios web externos.</span><span class="sxs-lookup"><span data-stu-id="ce00b-125">Additional records can be defined and created for all pools and single servers for any SIP domain that will use this reverse proxy, and has defined external web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce00b-126">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="ce00b-126">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ce00b-127">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ce00b-127">webdirext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ce00b-128">Escucha asignada para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="ce00b-128">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="ce00b-129">Servicios web externos para los grupos de directores o directores de su implementación.</span><span class="sxs-lookup"><span data-stu-id="ce00b-129">External web services for the Directors or Director pools in your deployment.</span></span> <span data-ttu-id="ce00b-130">Puede definir tantos directores como un número de directores distintos, de los cuales pueden estar asociados a otros dominios SIP.</span><span class="sxs-lookup"><span data-stu-id="ce00b-130">You can define as many Directors as there are distinct Directors, of which may be associated with other SIP domains.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="ce00b-131">Definir los registros DNS para y publicar los directores no es una de las agrupaciones front-end ni la decisión de director.</span><span class="sxs-lookup"><span data-stu-id="ce00b-131">Defining the DNS records for and publishing the Directors is not an either the Front End pool or the Director decision.</span></span> <span data-ttu-id="ce00b-132">Si está usando directores, debe definir y publicar el director y los servicios web externos del grupo de servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="ce00b-132">You must define and publish both the Director and the Front End pool external web services if you are using Directors.</span></span> <span data-ttu-id="ce00b-133">Los tipos de tráfico específicos (para autenticación y otros usos) se enviarán primero al Director, si está definido en la topología.</span><span class="sxs-lookup"><span data-stu-id="ce00b-133">Specific traffic types (for authentication and other uses) will be sent to the Director first, if it is defined in the topology.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce00b-134">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="ce00b-134">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ce00b-135">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ce00b-135">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ce00b-136">Escucha asignada para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="ce00b-136">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="ce00b-137">Conferencias de acceso telefónico local publicadas externamente</span><span class="sxs-lookup"><span data-stu-id="ce00b-137">Dial-in conferencing published externally</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce00b-138">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="ce00b-138">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ce00b-139">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ce00b-139">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ce00b-140">Escucha asignada para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="ce00b-140">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="ce00b-141">Conferencias publicadas externamente</span><span class="sxs-lookup"><span data-stu-id="ce00b-141">Conferences published externally</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce00b-142">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="ce00b-142">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ce00b-143">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ce00b-143">officewebapps01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ce00b-144">Escucha asignada para el servidor de Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="ce00b-144">Assigned listener for Office Web Apps Server</span></span></p></td>
<td><p><span data-ttu-id="ce00b-145">Office Web Apps Server implementado internamente o en el perímetro, y publicado para acceso externo de clientes</span><span class="sxs-lookup"><span data-stu-id="ce00b-145">Office Web Apps Server deployed internally or in the perimeter, and published for external client access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce00b-146">DNS externo/A</span><span class="sxs-lookup"><span data-stu-id="ce00b-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ce00b-147">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ce00b-147">lyncdiscover.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ce00b-148">Escucha asignada para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="ce00b-148">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="ce00b-149">Registro externo de detección de Lync para detección automática publicada externamente e incluye movilidad, Microsoft Lync Web App y la aplicación Web de programador</span><span class="sxs-lookup"><span data-stu-id="ce00b-149">Lync Discover External record for externally published AutoDiscover, and includes Mobility, Microsoft Lync Web App, and scheduler Web app</span></span></p></td>
</tr><span data-ttu-id="ce00b-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce00b-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

