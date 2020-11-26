---
title: 'Lync Server 2013: Resumen del certificado-conectividad de mensajería instantánea pública'
description: 'Lync Server 2013: Resumen del certificado-conectividad de mensajería instantánea pública.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Public instant messaging connectivity
ms:assetid: 2b3687ee-50c2-4c1c-880e-8dcf8bd4f309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618370(v=OCS.15)
ms:contentKeyID: 49105657
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: abf5a01bdeb03da158e221c623417a1b42cc82f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435295"
---
# <a name="certificate-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="903f9-103">Resumen del certificado: conectividad de mensajería instantánea pública en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="903f9-103">Certificate summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="903f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="903f9-104">

<span> </span></span></span>

<span data-ttu-id="903f9-105">_**Última modificación del tema:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="903f9-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="903f9-106">Para configurar certificados para la conectividad de mensajería instantánea pública, debe tener en cuenta primero que no hay nada diferente de otros tipos de Federación SIP o incluso certificados de servidor perimetral estándar, excepto que America Online (AOL) requiere una configuración de certificado única.</span><span class="sxs-lookup"><span data-stu-id="903f9-106">To configure certificates for public Instant Messaging connectivity, you should first notice that there is nothing different from other SIP federation types or even standard Edge Server certificates, except that America Online (AOL) requires a unique certificate configuration.</span></span> <span data-ttu-id="903f9-107">Además del uso mejorado de claves (EKU) del servidor, America Online requiere que el certificado o los certificados (en el caso de un grupo de límites) contengan también el EKU de cliente.</span><span class="sxs-lookup"><span data-stu-id="903f9-107">In addition to the usual server enhanced key usage (EKU), America Online requires the certificate or certificates (in the case of an Edge pool) to also contain the client EKU.</span></span> <span data-ttu-id="903f9-108">El EKU de cliente es una adición al certificado y forma parte del certificado público externo que se asigna al servidor perimetral.</span><span class="sxs-lookup"><span data-stu-id="903f9-108">The client EKU is an addition to the certificate, and is part of the external public certificate that is assigned to your Edge Server.</span></span>

<div>

## <a name="certificate-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="903f9-109">Resumen del certificado: conectividad de mensajería instantánea pública</span><span class="sxs-lookup"><span data-stu-id="903f9-109">Certificate Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="903f9-110">Componente</span><span class="sxs-lookup"><span data-stu-id="903f9-110">Component</span></span></th>
<th><span data-ttu-id="903f9-111">Nombre del asunto</span><span class="sxs-lookup"><span data-stu-id="903f9-111">Subject name</span></span></th>
<th><span data-ttu-id="903f9-112">Nombres alternativos de asunto (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="903f9-112">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="903f9-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="903f9-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="903f9-114">Perimetral de acceso externo</span><span class="sxs-lookup"><span data-stu-id="903f9-114">External/Access Edge</span></span></p></td>
<td><p><span data-ttu-id="903f9-115">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="903f9-115">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="903f9-116">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="903f9-116">sip.contoso.com</span></span></p>
<p><span data-ttu-id="903f9-117">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="903f9-117">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="903f9-118">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="903f9-118">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="903f9-119">El certificado debe ser de una entidad de certificación pública y debe tener el EKU de servidor y el EKU de cliente si se va a implementar la conectividad de mensajería instantánea pública con AOL.</span><span class="sxs-lookup"><span data-stu-id="903f9-119">The certificate must be from a Public CA, and must have the server EKU and client EKU if public IM connectivity with AOL is to be deployed.</span></span> <span data-ttu-id="903f9-120">El certificado se asigna a las interfaces del servidor perimetral externo para:</span><span class="sxs-lookup"><span data-stu-id="903f9-120">The certificate is assigned to the external Edge Server interfaces for:</span></span></p>
<ul>
<li><p><span data-ttu-id="903f9-121">Servicio perimetral de acceso</span><span class="sxs-lookup"><span data-stu-id="903f9-121">Access Edge service</span></span></p></li>
<li><p><span data-ttu-id="903f9-122">Servicio perimetral de conferencia web</span><span class="sxs-lookup"><span data-stu-id="903f9-122">Web Conferencing Edge service</span></span></p></li>
<li><p><span data-ttu-id="903f9-123">Servicio perimetral A/V</span><span class="sxs-lookup"><span data-stu-id="903f9-123">A/V Edge service</span></span></p></li>
</ul>
<p><span data-ttu-id="903f9-124">Tenga en cuenta que las redes San se agregan automáticamente al certificado según sus definiciones en el generador de topologías.</span><span class="sxs-lookup"><span data-stu-id="903f9-124">Note that SANs are automatically added to the certificate based on your definitions in Topology Builder.</span></span> <span data-ttu-id="903f9-125">Agregue las entradas de SAN según sea necesario para dominios SIP adicionales y otras entradas que necesite admitir.</span><span class="sxs-lookup"><span data-stu-id="903f9-125">You add SAN entries as needed for additional SIP domains and other entries that you need to support.</span></span> <span data-ttu-id="903f9-126">El nombre del asunto se replica en el SAN y debe estar presente para que funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="903f9-126">The subject name is replicated in the SAN and must be present for correct operation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="903f9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="903f9-127">See Also</span></span>


[<span data-ttu-id="903f9-128">Escenarios para el acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="903f9-128">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
  

<span data-ttu-id="903f9-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="903f9-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

