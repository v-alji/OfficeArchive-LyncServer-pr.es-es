---
title: Resumen de certificado - Grupo de director escalado, equilibrador de carga de hardware
description: 'Resumen de certificado: Grupo de directores de la carga del hardware.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Scaled Director pool, hardware load balancer
ms:assetid: 45940add-8027-418d-b79a-9033b494762f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204846(v=OCS.15)
ms:contentKeyID: 48183992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08abc37940cd41a29d6620cfc0a2a801de4a8e38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399413"
---
# <a name="certificate-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="1c47e-103">Resumen de certificado - Grupo de director escalado, equilibrador de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c47e-103">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c47e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c47e-104">

<span> </span></span></span>

<span data-ttu-id="1c47e-105">_**Última modificación del tema:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="1c47e-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="1c47e-106">Los requisitos de certificado para un director con un equilibrador de carga de hardware usarán un certificado predeterminado que tiene un nombre de sujeto y nombres alternativos de asunto para los servicios que el grupo de directores puede recibir.</span><span class="sxs-lookup"><span data-stu-id="1c47e-106">Certificate requirements for a Director with a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director pool can receive.</span></span> <span data-ttu-id="1c47e-107">Se solicita un certificado para cada director del grupo.</span><span class="sxs-lookup"><span data-stu-id="1c47e-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="1c47e-108">Además, hay un certificado de token de OAuth para la autenticación de servidor a servidor que se instala en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="1c47e-108">Additionally there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-a-scaled-director-using-a-hardware-load-balancer"></a><span data-ttu-id="1c47e-109">Certificados para un director con escala usando un equilibrador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="1c47e-109">Certificates for a Scaled Director Using a Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c47e-110">Componente</span><span class="sxs-lookup"><span data-stu-id="1c47e-110">Component</span></span></th>
<th><span data-ttu-id="1c47e-111">Nombre de sujeto</span><span class="sxs-lookup"><span data-stu-id="1c47e-111">Subject name (SN)</span></span></th>
<th><span data-ttu-id="1c47e-112">Nombres alternativos de asunto (SAN)</span><span class="sxs-lookup"><span data-stu-id="1c47e-112">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="1c47e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c47e-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c47e-114">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="1c47e-114">Default</span></span></p></td>
<td><p><span data-ttu-id="1c47e-115">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="1c47e-115">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="1c47e-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="1c47e-116">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="1c47e-117">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="1c47e-117">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="1c47e-118">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c47e-118">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="1c47e-119">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c47e-119">meet.contoso.com</span></span></p>
<p><span data-ttu-id="1c47e-120">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c47e-120">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="1c47e-121">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c47e-121">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="1c47e-122">(Opcional) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c47e-122">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c47e-123">Los certificados de director se pueden solicitar desde una entidad de certificación (CA) administrada internamente o desde una CA pública.</span><span class="sxs-lookup"><span data-stu-id="1c47e-123">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="1c47e-124">El Director responde a las solicitudes del proxy inverso en el perímetro o del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="1c47e-124">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span></p>
<p><span data-ttu-id="1c47e-125">O bien, una entrada comodín para las direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="1c47e-125">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c47e-126">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="1c47e-126">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="1c47e-127">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="1c47e-127">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="1c47e-128">Ninguna entrada</span><span class="sxs-lookup"><span data-stu-id="1c47e-128">No Entry</span></span></p></td>
<td>


> [!IMPORTANT]
> <span data-ttu-id="1c47e-129">Tenga en cuenta que la longitud de clave mínima es 1024, pero es posible que reciba una advertencia que indica que la longitud de clave mínima recomendada es de 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="1c47e-129">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


<p><span data-ttu-id="1c47e-130">El certificado OAuthTokenIssuer es un certificado de un único propósito para el propósito de autenticar servidores en un entorno de gran escala y se puede solicitar desde una entidad de certificación interna o desde una CA pública.</span><span class="sxs-lookup"><span data-stu-id="1c47e-130">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="1c47e-131">El certificado es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1c47e-131">The certificate is required.</span></span></p><span data-ttu-id="1c47e-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c47e-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

