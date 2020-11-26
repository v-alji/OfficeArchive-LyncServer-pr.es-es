---
title: 'Lync Server 2013: Resumen de certificado - Director único'
description: 'Lync Server 2013: Resumen del certificado: un único Director.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Single Director
ms:assetid: 1b769a76-cbf3-46e9-a955-f6cde5faff93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204720(v=OCS.15)
ms:contentKeyID: 48183546
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cf930a73d9989ec44f52f1d70ee9e0f900e4d6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435197"
---
# <a name="certificate-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="871c0-103">Resumen de certificado - Director único en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="871c0-103">Certificate summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="871c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="871c0-104">

<span> </span></span></span>

<span data-ttu-id="871c0-105">_**Última modificación del tema:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="871c0-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="871c0-106">Los requisitos de certificado para un único Director consisten en un certificado predeterminado que tiene un nombre de sujeto y nombres alternativos de sujeto para los servicios que el director puede recibir.</span><span class="sxs-lookup"><span data-stu-id="871c0-106">Certificate requirements for a single Director consist of a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="871c0-107">Además, hay un certificado de token de OAuth para propósitos de autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="871c0-107">Additionally, there is an OAuth Token certificate for server to server authentication purposes.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="871c0-108">Certificados para Director</span><span class="sxs-lookup"><span data-stu-id="871c0-108">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="871c0-109">Componente</span><span class="sxs-lookup"><span data-stu-id="871c0-109">Component</span></span></th>
<th><span data-ttu-id="871c0-110">Nombre de sujeto</span><span class="sxs-lookup"><span data-stu-id="871c0-110">Subject name (SN)</span></span></th>
<th><span data-ttu-id="871c0-111">Nombres alternativos de asunto (SAN)</span><span class="sxs-lookup"><span data-stu-id="871c0-111">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="871c0-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="871c0-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="871c0-113">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="871c0-113">Default</span></span></p></td>
<td><p><span data-ttu-id="871c0-114">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="871c0-114">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="871c0-115">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="871c0-115">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="871c0-116">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="871c0-116">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="871c0-117">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="871c0-117">meet.contoso.com</span></span></p>
<p><span data-ttu-id="871c0-118">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="871c0-118">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="871c0-119">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="871c0-119">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="871c0-120">(Opcional) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="871c0-120">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="871c0-121">Los certificados de director se pueden solicitar desde una entidad de certificación (CA) administrada internamente o desde una CA pública.</span><span class="sxs-lookup"><span data-stu-id="871c0-121">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="871c0-122">El Director responde a las solicitudes del proxy inverso en el perímetro o del servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="871c0-122">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="871c0-123">Los clientes internos no usarán el director.</span><span class="sxs-lookup"><span data-stu-id="871c0-123">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="871c0-124">O bien, una entrada comodín para las direcciones URL simples</span><span class="sxs-lookup"><span data-stu-id="871c0-124">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="871c0-125">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="871c0-125">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="871c0-126">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="871c0-126">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="871c0-127">Ninguna entrada</span><span class="sxs-lookup"><span data-stu-id="871c0-127">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="871c0-128">Tenga en cuenta que la longitud de clave mínima es 1024, pero es posible que reciba una advertencia que indica que la longitud de clave mínima recomendada es de 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="871c0-128">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="871c0-129">El certificado OAuthTokenIssuer es un certificado de un único propósito para el propósito de autenticar servidores en un entorno de gran escala y se puede solicitar desde una entidad de certificación interna o desde una CA pública.</span><span class="sxs-lookup"><span data-stu-id="871c0-129">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="871c0-130">El certificado es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="871c0-130">The certificate is required.</span></span></p><span data-ttu-id="871c0-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="871c0-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

