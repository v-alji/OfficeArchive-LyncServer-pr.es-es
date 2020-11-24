---
title: 'Lync Server 2013: Compatibilidad de certificado de comodín'
description: Compatibilidad con certificados comodín de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Wildcard certificate support
ms:assetid: 0bae2aa8-b6dc-46f5-a3be-3fe7581809d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202161(v=OCS.15)
ms:contentKeyID: 48183382
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 46cc362eb925a86b5e90d51569db6d425ba88fa6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398915"
---
# <a name="wildcard-certificate-support-in-lync-server-2013"></a><span data-ttu-id="a06b4-103">Compatibilidad de certificado de comodín en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a06b4-103">Wildcard certificate support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a06b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a06b4-104">

<span> </span></span></span>

<span data-ttu-id="a06b4-105">_**Última modificación del tema:** 2013-03-21_</span><span class="sxs-lookup"><span data-stu-id="a06b4-105">_**Topic Last Modified:** 2013-03-21_</span></span>

<span data-ttu-id="a06b4-106">Lync Server 2013 usa certificados para proporcionar cifrado de comunicaciones y autenticación de identidades de servidor.</span><span class="sxs-lookup"><span data-stu-id="a06b4-106">Lync Server 2013 uses certificates to provide communications encryption and server identity authentication.</span></span> <span data-ttu-id="a06b4-107">En algunos casos, como la publicación web a través del proxy inverso, la coincidencia de entrada de nombre alternativo de asunto (SAN) con el nombre de dominio completo (FQDN) del servidor que presenta el servicio no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="a06b4-107">In some cases, such as web publishing through the reverse proxy, strong subject alternative name (SAN) entry matching to the fully qualified domain name (FQDN) of the server presenting the service is not required.</span></span> <span data-ttu-id="a06b4-108">En estos casos, puede usar certificados con entradas SAN con comodín (comúnmente conocidos como "certificados comodín") para reducir el costo de un certificado solicitado por una entidad de certificación pública y reducir la complejidad del proceso de planeación de certificados.</span><span class="sxs-lookup"><span data-stu-id="a06b4-108">In these cases, you can use certificates with wildcard SAN entries (commonly known as “wildcard certificates”) to reduce the cost of a certificate requested from a public certification authority and to reduce the complexity of the planning process for certificates.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="a06b4-109">Para conservar la funcionalidad de los dispositivos de comunicaciones unificadas (por ejemplo, los teléfonos de escritorio), debe probar el certificado implementado con cuidado para asegurarse de que los dispositivos funcionan correctamente después de implementar un certificado de comodín.</span><span class="sxs-lookup"><span data-stu-id="a06b4-109">To retain the functionality of unified communications (UC) devices (for example, desk phones), you should test the deployed certificate carefully to ensure that devices function properly after you implement a wildcard certificate.</span></span>



</div>

<span data-ttu-id="a06b4-110">No se admite una entrada de comodín como nombre de asunto (también denominado nombre común o CN) para cualquier rol.</span><span class="sxs-lookup"><span data-stu-id="a06b4-110">There is no support for a wildcard entry as the subject name (also referred to as the common name or CN) for any role.</span></span> <span data-ttu-id="a06b4-111">Los siguientes roles de servidor se admiten al usar entradas con comodín en el SAN:</span><span class="sxs-lookup"><span data-stu-id="a06b4-111">The following server roles are supported when using wildcard entries in the SAN:</span></span>

  - <span></span>  
    <span data-ttu-id="a06b4-112">**Proxy inverso.**</span><span class="sxs-lookup"><span data-stu-id="a06b4-112">**Reverse proxy.**</span></span>   <span data-ttu-id="a06b4-113">La entrada SAN con comodín es compatible con el certificado de publicación de URL simple (reunirse y llamar).</span><span class="sxs-lookup"><span data-stu-id="a06b4-113">Wildcard SAN entry is supported for Simple URL (meet and dialin) publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="a06b4-114">**Proxy inverso.**</span><span class="sxs-lookup"><span data-stu-id="a06b4-114">**Reverse proxy.**</span></span>   <span data-ttu-id="a06b4-115">La entrada SAN con comodín es compatible con las entradas SAN para LyncDiscover en el certificado de publicación.</span><span class="sxs-lookup"><span data-stu-id="a06b4-115">Wildcard SAN entry is supported for the SAN entries for LyncDiscover on the publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="a06b4-116">**Director.**</span><span class="sxs-lookup"><span data-stu-id="a06b4-116">**Director.**</span></span>   <span data-ttu-id="a06b4-117">La entrada SAN con comodín es compatible con las direcciones URL simples (reunirse y llamar) y para las entradas de SAN para LyncDiscover y LyncDiscoverInternal en los componentes Web de director.</span><span class="sxs-lookup"><span data-stu-id="a06b4-117">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Director web components.</span></span>

  - <span></span>  
    <span data-ttu-id="a06b4-118">**Servidor front end (Standard Edition) y grupo de servidores front-end (Enterprise Edition).**</span><span class="sxs-lookup"><span data-stu-id="a06b4-118">**Front End Server (Standard Edition) and Front End pool (Enterprise Edition).**</span></span> <span data-ttu-id="a06b4-119">La entrada SAN con comodín es compatible con las direcciones URL simples (reunirse y llamar) y para las entradas de SAN para LyncDiscover y LyncDiscoverInternal en los componentes Web front-end.</span><span class="sxs-lookup"><span data-stu-id="a06b4-119">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Front End web components.</span></span>

  - <span></span>  
    <span data-ttu-id="a06b4-120">**Mensajería unificada de Exchange (UM).**</span><span class="sxs-lookup"><span data-stu-id="a06b4-120">**Exchange Unified Messaging (UM).**</span></span>   <span data-ttu-id="a06b4-121">El servidor no usa entradas SAN cuando se implementa como un servidor independiente.</span><span class="sxs-lookup"><span data-stu-id="a06b4-121">The server does not use SAN entries when deployed as a stand-alone server.</span></span>

  - <span></span>  
    <span data-ttu-id="a06b4-122">**Servidor de acceso de cliente de Microsoft Exchange Server.**</span><span class="sxs-lookup"><span data-stu-id="a06b4-122">**Microsoft Exchange Server Client Access server.**</span></span>   <span data-ttu-id="a06b4-123">Las entradas con comodín en el SAN son compatibles con los clientes internos y externos.</span><span class="sxs-lookup"><span data-stu-id="a06b4-123">Wildcard entries in the SAN are supported for internal and external clients.</span></span>

  - <span></span>  
    <span data-ttu-id="a06b4-124">**Mensajería unificada de Exchange y servidor de acceso de cliente de Microsoft Exchange Server en el mismo servidor.**</span><span class="sxs-lookup"><span data-stu-id="a06b4-124">**Exchange Unified Messaging (UM) and Microsoft Exchange Server Client Access server on same server.**</span></span>   <span data-ttu-id="a06b4-125">Se admiten entradas SAN con comodín.</span><span class="sxs-lookup"><span data-stu-id="a06b4-125">Wildcard SAN entries are supported.</span></span>

<span data-ttu-id="a06b4-126">Roles de servidor que no se tratan en este tema:</span><span class="sxs-lookup"><span data-stu-id="a06b4-126">Server roles that are not addressed in this topic:</span></span>

  - <span data-ttu-id="a06b4-127">Roles de servidor interno (incluidos, entre otros, el servidor de mediación, el servidor de archivado y el servidor de supervisión, el dispositivo de sucursal con supervivencia o el servidor de sucursal superviviente)</span><span class="sxs-lookup"><span data-stu-id="a06b4-127">Internal server roles (including, but not limited to the Mediation Server, Archiving and Monitoring Server, Survivable Branch Appliance, or Survivable Branch Server)</span></span>

  - <span data-ttu-id="a06b4-128">Interfaces de servidor perimetral externo</span><span class="sxs-lookup"><span data-stu-id="a06b4-128">External Edge Server interfaces</span></span>

  - <span data-ttu-id="a06b4-129">Servidor perimetral interno</span><span class="sxs-lookup"><span data-stu-id="a06b4-129">Internal Edge Server</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06b4-130">Para la interfaz de servidor perimetral interno, se puede asignar una entrada comodín a la SAN y es compatible.</span><span class="sxs-lookup"><span data-stu-id="a06b4-130">For the internal Edge Server interface, a wildcard entry can be assigned to the SAN, and is supported.</span></span> <span data-ttu-id="a06b4-131">No se consulta la SAN en el servidor perimetral interno y una entrada SAN con comodín tiene un valor limitado.</span><span class="sxs-lookup"><span data-stu-id="a06b4-131">The SAN on the internal Edge Server is not queried, and a wildcard SAN entry is of limited value.</span></span>

    
    </div>

<span data-ttu-id="a06b4-132">Para obtener más información sobre la configuración de certificados, incluido el uso de caracteres comodín en los certificados, consulte los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="a06b4-132">For details about certificate configurations, including the use of wildcards in certificates, see the following topics:</span></span>

  - [<span data-ttu-id="a06b4-133">Requisitos de certificado para Servidores internos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a06b4-133">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="a06b4-134">Requisitos de certificado para el acceso de usuarios externos en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a06b4-134">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="a06b4-135">Resumen de certificado - Carga equilibrada DNS y HLB en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a06b4-135">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="a06b4-136">Resumen de certificado - Director único en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a06b4-136">Certificate summary - Single Director in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-director.md)

  - [<span data-ttu-id="a06b4-137">Resumen de certificado - Grupo de director escalado, equilibrador de carga de hardware en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a06b4-137">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="a06b4-138">Resumen de certificado - Proxy inverso en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a06b4-138">Certificate summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-reverse-proxy.md)

  - [<span data-ttu-id="a06b4-139">Instrucciones para integrar mensajería unificada local y Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a06b4-139">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="a06b4-140">Para obtener detalles sobre la configuración de certificados para Exchange, incluido el uso de caracteres comodín, consulte la documentación del producto Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="a06b4-140">For details about configuring certificates for Exchange, including the use of wildcards, see the Exchange 2013 product documentation.</span></span>

<span data-ttu-id="a06b4-141"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a06b4-141"></div>

<span> </span>

</div>

</div>

</span></span></div>

