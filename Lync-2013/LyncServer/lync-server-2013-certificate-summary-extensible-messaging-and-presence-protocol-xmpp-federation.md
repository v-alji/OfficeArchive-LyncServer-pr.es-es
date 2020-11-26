---
title: 'Lync Server 2013: Resumen de certificado-Federación de protocolo de presencia y mensajería extensible (XMPP)'
description: 'Lync Server 2013: Resumen de certificado-Federación de protocolo de presencia y mensajería extensible (XMPP).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Extensible messaging and presence protocol (XMPP) federation
ms:assetid: b059a34e-99df-40af-91fe-fe2aa52841f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618374(v=OCS.15)
ms:contentKeyID: 49105661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6e2bb593d909c2eec6032dc89c07cc5f5b1a72db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435302"
---
# <a name="certificate-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="7f3b4-103">Resumen de certificados: Federación de protocolo de presencia y mensajería extensible (XMPP) en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f3b4-103">Certificate summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f3b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f3b4-104">

<span> </span></span></span>

<span data-ttu-id="7f3b4-105">_**Última modificación del tema:** 2012-12-23_</span><span class="sxs-lookup"><span data-stu-id="7f3b4-105">_**Topic Last Modified:** 2012-12-23_</span></span>

<span data-ttu-id="7f3b4-106">Los requisitos de certificados para habilitar y establecer comunicaciones con los partners de protocolo de presencia y mensajería extensible (XMPP) requieren el registro adicional de los dominios XMPP.</span><span class="sxs-lookup"><span data-stu-id="7f3b4-106">Certificate requirements for enabling and establishing communications with extensible messaging and presence protocol (XMPP) partners require the additional record of your XMPP domains.</span></span> <span data-ttu-id="7f3b4-107">El registro que se incluye en el certificado como un nombre alternativo del sujeto (SAN) será el dominio que puede participar en las comunicaciones XMPP.</span><span class="sxs-lookup"><span data-stu-id="7f3b4-107">The record that is included on the certificate as a subject alternative name (SAN) will be the domain that can participate in XMPP communications.</span></span> <span data-ttu-id="7f3b4-108">El dominio puede ser el dominio de nivel raíz (por ejemplo, contoso.com) Si desea habilitar XMPP para todo el dominio o puede seleccionar dominios secundarios (por ejemplo, corp.contoso.com, finance.contoso.com) si va a habilitar XMPP para un subconjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="7f3b4-108">The domain can be the root-level domain (for example, contoso.com) if you want to enable XMPP for your entire domain, or can be selected child domains (for example, corp.contoso.com, finance.contoso.com) if you are enabling XMPP for a subset of users.</span></span>

<div>

## <a name="certificate-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="7f3b4-109">Resumen del certificado para el protocolo de presencia y mensajería extensible</span><span class="sxs-lookup"><span data-stu-id="7f3b4-109">Certificate Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f3b4-110">Componente</span><span class="sxs-lookup"><span data-stu-id="7f3b4-110">Component</span></span></th>
<th><span data-ttu-id="7f3b4-111">Nombre del asunto</span><span class="sxs-lookup"><span data-stu-id="7f3b4-111">Subject name</span></span></th>
<th><span data-ttu-id="7f3b4-112">Nombres alternativos de asunto (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="7f3b4-112">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="7f3b4-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f3b4-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f3b4-114">Asignar a servicio perimetral de acceso al servidor perimetral o grupo de servidores perimetrales</span><span class="sxs-lookup"><span data-stu-id="7f3b4-114">Assign to Access Edge service of Edge Server or Edge pool</span></span></p></td>
<td><p><span data-ttu-id="7f3b4-115">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7f3b4-115">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7f3b4-116">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7f3b4-116">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="7f3b4-117">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7f3b4-117">sip.contoso.com</span></span></p>
<p><span data-ttu-id="7f3b4-118">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="7f3b4-118">sip.fabrikam.com</span></span></p>
<p><span data-ttu-id="7f3b4-119">contoso.com</span><span class="sxs-lookup"><span data-stu-id="7f3b4-119">contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7f3b4-120">Las tres primeras entradas de SAN son las entradas normales de SAN para un servidor de borde completo.</span><span class="sxs-lookup"><span data-stu-id="7f3b4-120">The first three SAN entries are the normal SAN entries for a full Edge Server.</span></span> <span data-ttu-id="7f3b4-121">La contoso.com es la entrada necesaria para la Federación con el socio XMPP en el nivel de dominio raíz.</span><span class="sxs-lookup"><span data-stu-id="7f3b4-121">The contoso.com is the entry required for federation with the XMPP partner at the root domain level.</span></span> <span data-ttu-id="7f3b4-122">Esta entrada permitirá que XMPP para todos los dominios con el sufijo contoso.com.</span><span class="sxs-lookup"><span data-stu-id="7f3b4-122">This entry will allow XMPP for all domains with the suffix contoso.com.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7f3b4-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f3b4-123">See Also</span></span>


[<span data-ttu-id="7f3b4-124">Configuración XMPP de ejemplo en Lync Server 2013 - Federación XMPP con Google Talk</span><span class="sxs-lookup"><span data-stu-id="7f3b4-124">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="7f3b4-125">Plan para certificados de servidores perimetrales en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f3b4-125">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)  


[<span data-ttu-id="7f3b4-126">Configurar certificados perimetrales para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f3b4-126">Set up Edge certificates for Lync Server 2013</span></span>](lync-server-2013-set-up-edge-certificates.md)  
[<span data-ttu-id="7f3b4-127">Solicitud-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="7f3b4-127">Request-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Request-CsCertificate)  
[<span data-ttu-id="7f3b4-128">Set-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="7f3b4-128">Set-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  
  

<span data-ttu-id="7f3b4-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f3b4-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

