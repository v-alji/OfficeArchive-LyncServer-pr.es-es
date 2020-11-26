---
title: 'Lync Server 2013: Compatibilidad con infraestructura de DNS'
description: 'Lync Server 2013: compatibilidad con la infraestructura DNS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Domain Name System (DNS) infrastructure support
ms:assetid: 37777c16-94ce-436d-b517-bcf53a564513
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425850(v=OCS.15)
ms:contentKeyID: 48183878
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea65907eba13367fd92e546d62994d10907bf89
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429080"
---
# <a name="dns-infrastructure-support-in-lync-server-2013"></a><span data-ttu-id="5e248-103">Compatibilidad con infraestructura de DNS en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5e248-103">DNS infrastructure support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5e248-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5e248-104">

<span> </span></span></span>

<span data-ttu-id="5e248-105">_**Última modificación del tema:** 2013-03-08_</span><span class="sxs-lookup"><span data-stu-id="5e248-105">_**Topic Last Modified:** 2013-03-08_</span></span>

<span data-ttu-id="5e248-106">Lync Server 2013 requiere el sistema de nombres de dominio (DNS) y lo usa de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="5e248-106">Lync Server 2013 requires Domain Name System (DNS) and uses it in the following ways:</span></span>

  - <span data-ttu-id="5e248-107">Para detectar los servidores o grupos de servidores internos para las comunicaciones de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="5e248-107">To discover internal servers or pools for server-to-server communications.</span></span>

  - <span data-ttu-id="5e248-108">Para permitir que los clientes descubran el grupo de servidores front-end o el servidor Standard Edition usado para varias transacciones SIP.</span><span class="sxs-lookup"><span data-stu-id="5e248-108">To enable clients to discover the Front End pool or Standard Edition server used for various SIP transactions.</span></span>

  - <span data-ttu-id="5e248-109">Para asociar las direcciones URL simples a las conferencias con los servidores que hospedan esas conferencias.</span><span class="sxs-lookup"><span data-stu-id="5e248-109">To associate the simple URLs for conferences with the servers hosting those conferences.</span></span>

  - <span data-ttu-id="5e248-110">Para permitir que los servidores y clientes externos se conecten a servidores perimetrales o al proxy inverso HTTP para mensajería instantánea (mi) o conferencias.</span><span class="sxs-lookup"><span data-stu-id="5e248-110">To enable external servers and clients to connect to Edge Servers or the HTTP reverse proxy for instant messaging (IM) or conferencing.</span></span>

  - <span data-ttu-id="5e248-111">Para habilitar los dispositivos de comunicaciones unificadas (UC) que no han iniciado sesión para detectar el grupo de servidores front-end o el servidor Standard Edition que ejecuta el servicio Web de actualización de dispositivos, obtener actualizaciones y enviar registros.</span><span class="sxs-lookup"><span data-stu-id="5e248-111">To enable unified communications (UC) devices that are not logged in to discover the Front End pool or Standard Edition server running Device Update Web service, obtain updates, and send logs.</span></span>

  - <span data-ttu-id="5e248-112">Para permitir que los clientes móviles detecten automáticamente recursos de servicios web sin que los usuarios tengan que introducir direcciones URL en la configuración del dispositivo de forma manual.</span><span class="sxs-lookup"><span data-stu-id="5e248-112">To enable mobile clients to automatically discover Web Services resources without requiring users to manually enter URLs in device settings.</span></span>

  - <span data-ttu-id="5e248-113">Para el equilibrio de carga de DNS.</span><span class="sxs-lookup"><span data-stu-id="5e248-113">For DNS load balancing.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5e248-114">Lync Server 2013 no admite nombres de dominio internacionalizados (IDNs).</span><span class="sxs-lookup"><span data-stu-id="5e248-114">Lync Server 2013 does not support internationalized domain names (IDNs).</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5e248-115">El nombre que especifique debe ser idéntico al nombre de equipo configurado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5e248-115">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="5e248-116">De forma predeterminada, el nombre de equipo en el caso de un equipo que no está unido a un dominio es un nombre corto, no un nombre de dominio completo (FQDN).</span><span class="sxs-lookup"><span data-stu-id="5e248-116">By default, the computer name of a computer that is not joined to a domain is a short name, not a fully qualified domain name (FQDN).</span></span> <span data-ttu-id="5e248-117">El Generador de topologías usa nombres de dominio completos, no nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="5e248-117">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="5e248-118">Por lo tanto, debe configurar un sufijo DNS en el nombre del equipo para implementarse como servidor perimetral que no está unido a un dominio.</span><span class="sxs-lookup"><span data-stu-id="5e248-118">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="5e248-119"><STRONG>Utilice únicamente caracteres estándar</STRONG> (incluyendo A–Z, a–z, 0–9 y guiones) a la hora de asignar FQDN de sus Lync Server, servidores perimetrales y grupos.</span><span class="sxs-lookup"><span data-stu-id="5e248-119"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="5e248-120">No utilice caracteres Unicode ni de subrayado.</span><span class="sxs-lookup"><span data-stu-id="5e248-120">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="5e248-121">Los caracteres no estándar en una dirección URL o un FQDN a menudo no son compatibles con DNS externas y CA públicas (es decir, cuando el FQDN debe asignarse al SN en el certificado).</span><span class="sxs-lookup"><span data-stu-id="5e248-121">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (that is, when the FQDN must be assigned to the SN in the certificate).</span></span>



<span data-ttu-id="5e248-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5e248-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

