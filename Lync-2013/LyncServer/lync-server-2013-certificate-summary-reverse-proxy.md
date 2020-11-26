---
title: 'Lync Server 2013: Resumen de certificado - Proxy inverso'
description: 'Lync Server 2013: Resumen del certificado: proxy inverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Reverse proxy
ms:assetid: f2b9a53f-aead-413d-81e9-4a294a010fbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205381(v=OCS.15)
ms:contentKeyID: 48185820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cc250d6de2eb1a0b6c3ad3495c8df62942f9a81
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435278"
---
# <a name="certificate-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="3fac2-103">Resumen de certificado - Proxy inverso en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fac2-103">Certificate summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fac2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fac2-104">

<span> </span></span></span>

<span data-ttu-id="3fac2-105">_**Última modificación del tema:** 2012-11-14_</span><span class="sxs-lookup"><span data-stu-id="3fac2-105">_**Topic Last Modified:** 2012-11-14_</span></span>

<span data-ttu-id="3fac2-106">Los requisitos de certificados para el proxy inverso son mucho más simples que el de los servidores perimetrales.</span><span class="sxs-lookup"><span data-stu-id="3fac2-106">Certificate requirements for the reverse proxy are much simpler than that for the Edge Servers.</span></span> <span data-ttu-id="3fac2-107">El diagrama de flujo proporcionado presenta los requisitos necesarios.</span><span class="sxs-lookup"><span data-stu-id="3fac2-107">The provided flowchart presents the requirements necessary.</span></span> <span data-ttu-id="3fac2-108">La tabla adjunta presenta el nombre de asunto del certificado y los nombres alternativos del sujeto típicos en relación con los escenarios que hemos revisado en las discusiones del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="3fac2-108">The accompanying table presents typical certificate subject name and subject alternative names in relation to the scenarios that we have been reviewed in the Edge Server discussions.</span></span> <span data-ttu-id="3fac2-109">Para obtener más información sobre los escenarios del servidor perimetral, consulte [escenarios para el acceso de usuarios externos en Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="3fac2-109">For more details on the Edge Server scenarios, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="3fac2-110">**Diagrama de flujo de certificados para el proxy inverso**</span><span class="sxs-lookup"><span data-stu-id="3fac2-110">**Certificates Flow Chart for Reverse Proxy**</span></span>

<span data-ttu-id="3fac2-111">![Diagrama de flujo de certificados para el servidor perimetral](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "Diagrama de flujo de certificados para el servidor perimetral")</span><span class="sxs-lookup"><span data-stu-id="3fac2-111">![Certificates Flow Chart for Edge Server](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "Certificates Flow Chart for Edge Server")</span></span>

### <a name="reverse-proxy-external-interface"></a><span data-ttu-id="3fac2-112">Proxy inverso: interfaz externa</span><span class="sxs-lookup"><span data-stu-id="3fac2-112">Reverse Proxy: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3fac2-113">Componente</span><span class="sxs-lookup"><span data-stu-id="3fac2-113">Component</span></span></th>
<th><span data-ttu-id="3fac2-114">Nombre del asunto</span><span class="sxs-lookup"><span data-stu-id="3fac2-114">Subject name</span></span></th>
<th><span data-ttu-id="3fac2-115">Nombre alternativo de asunto (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="3fac2-115">Subject alternative name (SAN)/Order</span></span></th>
<th><span data-ttu-id="3fac2-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fac2-116">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fac2-117">Proxy inverso</span><span class="sxs-lookup"><span data-stu-id="3fac2-117">Reverse Proxy</span></span></p></td>
<td><p><span data-ttu-id="3fac2-118">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3fac2-118">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3fac2-119">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3fac2-119">webext.contoso.com</span></span></p>
<p><span data-ttu-id="3fac2-120">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3fac2-120">webdirext.contoso.com</span></span></p>
<p><span data-ttu-id="3fac2-121">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3fac2-121">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="3fac2-122">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3fac2-122">meet.contoso.com</span></span></p>
<p><span data-ttu-id="3fac2-123">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3fac2-123">officewebapps01.contoso.com</span></span></p>
<p><span data-ttu-id="3fac2-124">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3fac2-124">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="3fac2-125">(Opcional):\*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="3fac2-125">(Optional):\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3fac2-126">El certificado debe ser emitido por una entidad de certificación pública y con el EKU de servidor.</span><span class="sxs-lookup"><span data-stu-id="3fac2-126">Certificate must be issued by a public CA and with the server EKU.</span></span> <span data-ttu-id="3fac2-127">Los servicios incluyen el servicio de libreta de direcciones, Office Web Apps para conferencias y las reglas de publicación de dispositivos IP de Lync.</span><span class="sxs-lookup"><span data-stu-id="3fac2-127">Services include Address Book Service, distribution group expansion Office Web Apps for conferencing, and Lync IP Device publishing rules.</span></span> <span data-ttu-id="3fac2-128">El nombre alternativo del firmante incluye:</span><span class="sxs-lookup"><span data-stu-id="3fac2-128">Subject alternative name includes:</span></span></p>
<ul>
<li><p><span data-ttu-id="3fac2-129">FQDN de servicios web externos para servidor front-end o grupo front-end</span><span class="sxs-lookup"><span data-stu-id="3fac2-129">External Web Services FQDN for Front End Server or Front End pool</span></span></p></li>
<li><p><span data-ttu-id="3fac2-130">FQDN de servicios web externos para el grupo de directores o directores</span><span class="sxs-lookup"><span data-stu-id="3fac2-130">External Web Services FQDN for Director or Director pool</span></span></p></li>
<li><p><span data-ttu-id="3fac2-131">Conferencia de acceso telefónico local</span><span class="sxs-lookup"><span data-stu-id="3fac2-131">Dial-in conferencing</span></span></p></li>
<li><p><span data-ttu-id="3fac2-132">Regla de publicación de reuniones en línea</span><span class="sxs-lookup"><span data-stu-id="3fac2-132">Online meeting publishing rule</span></span></p></li>
<li><p><span data-ttu-id="3fac2-133">Office Web Apps para conferencias</span><span class="sxs-lookup"><span data-stu-id="3fac2-133">Office Web Apps for conferencing</span></span></p></li>
<li><p><span data-ttu-id="3fac2-134">Lyncdiscover (detección automática)</span><span class="sxs-lookup"><span data-stu-id="3fac2-134">Lyncdiscover (Autodiscover)</span></span></p></li>
</ul>
<p><span data-ttu-id="3fac2-135">El comodín opcional reemplaza a reunirse y a través de SAN</span><span class="sxs-lookup"><span data-stu-id="3fac2-135">The optional wildcard replaces both meet and dialin SAN</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3fac2-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fac2-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

