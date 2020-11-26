---
title: 'Lync Server 2013: Resumen DNS - Grupo de director escalado, equilibrador de carga de hardware'
description: 'Lync Server 2013: Grupo de directores de Resumen escalados por DNS, equilibrador de carga de hardware.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled Director pool, hardware load balancer
ms:assetid: 08ba48e6-bfa1-4ab0-bc89-d58ddb9c20af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204655(v=OCS.15)
ms:contentKeyID: 48183340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7198e6a97feed8ce70cb16753ad1f21d58ef246c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428996"
---
# <a name="dns-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="0939a-103">Resumen DNS - Grupo de director escalado, equilibrador de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0939a-103">DNS summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0939a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0939a-104">

<span> </span></span></span>

<span data-ttu-id="0939a-105">_**Última modificación del tema:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="0939a-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="0939a-106">La tabla siguiente contiene un resumen de los registros DNS necesarios para admitir el director equilibrio de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="0939a-106">The following table contains a summary of the DNS records that are required to support the hardware load balanced Director.</span></span> <span data-ttu-id="0939a-107">La función del Director requiere registros DNS similares como servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="0939a-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="0939a-108">El número de registros necesarios se refleja en el asunto nombres alternativos requeridos en el certificado de director.</span><span class="sxs-lookup"><span data-stu-id="0939a-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="0939a-109">Diferente al servidor front-end, el grupo de directores no hospeda cuentas de usuario ni hospeda los servicios de movilidad.</span><span class="sxs-lookup"><span data-stu-id="0939a-109">Different from the Front End Server, the Director pool does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director-pool-using-a-hardware-load-balancer-and-dns-load-balancing"></a><span data-ttu-id="0939a-110">Registros DNS necesarios para el grupo de directores con un equilibrador de carga de hardware y el equilibrio de carga de DNS</span><span class="sxs-lookup"><span data-stu-id="0939a-110">DNS Records Required for the Director pool using a Hardware Load Balancer and DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0939a-111">Ubicación/tipo/puerto</span><span class="sxs-lookup"><span data-stu-id="0939a-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="0939a-112">FQDN/registro DNS</span><span class="sxs-lookup"><span data-stu-id="0939a-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="0939a-113">Dirección IP/FQDN</span><span class="sxs-lookup"><span data-stu-id="0939a-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="0939a-114">Se asigna a/comentarios</span><span class="sxs-lookup"><span data-stu-id="0939a-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0939a-115">DNS/A interno</span><span class="sxs-lookup"><span data-stu-id="0939a-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="0939a-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="0939a-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="0939a-117">Director</span><span class="sxs-lookup"><span data-stu-id="0939a-117">Director</span></span></p></td>
<td><p><span data-ttu-id="0939a-118">Registro de host de Director usado para la comunicación de servidor a servidor y de replicación</span><span class="sxs-lookup"><span data-stu-id="0939a-118">Director host record used for replication and server to server communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0939a-119">DNS/A interno</span><span class="sxs-lookup"><span data-stu-id="0939a-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="0939a-120">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="0939a-120">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="0939a-121">Grupo de directores HLB VIP</span><span class="sxs-lookup"><span data-stu-id="0939a-121">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="0939a-122">Registro de host para el grupo de directores de carga equilibrada de DNS</span><span class="sxs-lookup"><span data-stu-id="0939a-122">Host record for the DNS load balanced Director pool</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0939a-123">DNS/A interno</span><span class="sxs-lookup"><span data-stu-id="0939a-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="0939a-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0939a-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="0939a-125">Grupo de directores HLB VIP</span><span class="sxs-lookup"><span data-stu-id="0939a-125">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="0939a-126">Protocolo de inicio de sesión (SIP) entrante de la interfaz interna del servidor perimetral</span><span class="sxs-lookup"><span data-stu-id="0939a-126">Inbound session initiation protocol (SIP) from the internal interface of the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0939a-127">DNS/A interno</span><span class="sxs-lookup"><span data-stu-id="0939a-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="0939a-128">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0939a-128">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="0939a-129">Grupo de directores HLB VIP</span><span class="sxs-lookup"><span data-stu-id="0939a-129">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="0939a-130">Equilibrio de carga de hardware publicado servicios Web de marcado desde proxy inverso</span><span class="sxs-lookup"><span data-stu-id="0939a-130">Hardware load balanced published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0939a-131">DNS/A interno</span><span class="sxs-lookup"><span data-stu-id="0939a-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="0939a-132">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0939a-132">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="0939a-133">Grupo de directores HLB VIP</span><span class="sxs-lookup"><span data-stu-id="0939a-133">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="0939a-134">El equilibrio de carga de hardware publicado cumple con los servicios web del proxy inverso</span><span class="sxs-lookup"><span data-stu-id="0939a-134">Hardware load balanced published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0939a-135">DNS/A interno</span><span class="sxs-lookup"><span data-stu-id="0939a-135">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="0939a-136">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0939a-136">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="0939a-137">Grupo de directores HLB VIP</span><span class="sxs-lookup"><span data-stu-id="0939a-137">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="0939a-138">Equilibrio de carga de hardware publicado y definido por el vale Web de proxy inverso servicios web externos para el grupo de directores</span><span class="sxs-lookup"><span data-stu-id="0939a-138">Hardware load balanced published and defined by the reverse proxy Web Ticket external web services for the Director pool</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0939a-139">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0939a-139">


</div>

<span> </span>

</div>

</div>

</span></span></div>

