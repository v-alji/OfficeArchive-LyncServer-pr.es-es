---
title: 'Lync Server 2013: Resumen de certificado - Carga equilibrada DNS y HLB'
description: 'Lync Server 2013: Resumen del certificado: carga equilibrada de DNS y HLB.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - DNS and HLB load balanced
ms:assetid: 8318a1a4-b423-47b7-95e6-9541adfad391
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205047(v=OCS.15)
ms:contentKeyID: 48184676
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 97a89975af16b6e39625677f787d3726f00c76c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435323"
---
# <a name="certificate-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="30622-103">Resumen de certificado - Carga equilibrada DNS y HLB en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30622-103">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30622-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30622-104">

<span> </span></span></span>

<span data-ttu-id="30622-105">_**Última modificación del tema:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="30622-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="30622-106">Los requisitos de certificado para un director con el equilibrio de carga de DNS y un equilibrador de carga de hardware usarán un certificado predeterminado que tiene un nombre de sujeto y nombres alternativos de asunto para los servicios que el director puede recibir.</span><span class="sxs-lookup"><span data-stu-id="30622-106">Certificate requirements for a Director with DNS load balancing and a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="30622-107">Se solicita un certificado para cada director del grupo.</span><span class="sxs-lookup"><span data-stu-id="30622-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="30622-108">Es importante recordar que el equilibrador de carga de hardware equilibra la carga del tráfico del proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="30622-108">It is important to remember that the hardware load balancer is load balancing only the traffic from the reverse proxy.</span></span> <span data-ttu-id="30622-109">Además, hay un certificado de token de OAuth para la autenticación de servidor a servidor que se instala en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="30622-109">Additionally, there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="30622-110">Certificados para Director</span><span class="sxs-lookup"><span data-stu-id="30622-110">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30622-111">Componente</span><span class="sxs-lookup"><span data-stu-id="30622-111">Component</span></span></th>
<th><span data-ttu-id="30622-112">Nombre de sujeto</span><span class="sxs-lookup"><span data-stu-id="30622-112">Subject name (SN)</span></span></th>
<th><span data-ttu-id="30622-113">Nombres alternativos de asunto (SAN)</span><span class="sxs-lookup"><span data-stu-id="30622-113">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="30622-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30622-114">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30622-115">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="30622-115">Default</span></span></p></td>
<td><p><span data-ttu-id="30622-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="30622-116">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="30622-117">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="30622-117">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="30622-118">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="30622-118">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="30622-119">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="30622-119">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="30622-120">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="30622-120">meet.contoso.com</span></span></p>
<p><span data-ttu-id="30622-121">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="30622-121">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="30622-122">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="30622-122">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="30622-123">(Opcional) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="30622-123">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="30622-124">Los certificados de director se pueden solicitar desde una entidad de certificación (CA) administrada internamente o desde una CA pública.</span><span class="sxs-lookup"><span data-stu-id="30622-124">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="30622-125">El Director responde a las solicitudes del proxy inverso en el perímetro o del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="30622-125">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="30622-126">Los clientes internos no usarán el director.</span><span class="sxs-lookup"><span data-stu-id="30622-126">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="30622-127">O bien, una entrada comodín para las direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="30622-127">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30622-128">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="30622-128">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="30622-129">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="30622-129">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="30622-130">Ninguna entrada</span><span class="sxs-lookup"><span data-stu-id="30622-130">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="30622-131">Tenga en cuenta que la longitud de clave mínima es 1024, pero es posible que reciba una advertencia que indica que la longitud de clave mínima recomendada es de 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="30622-131">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="30622-132">El certificado OAuthTokenIssuer es un certificado de un único propósito para el propósito de autenticar servidores en un entorno de gran escala y se puede solicitar desde una entidad de certificación interna o desde una CA pública.</span><span class="sxs-lookup"><span data-stu-id="30622-132">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="30622-133">El certificado es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="30622-133">The certificate is required.</span></span></p><span data-ttu-id="30622-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30622-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

