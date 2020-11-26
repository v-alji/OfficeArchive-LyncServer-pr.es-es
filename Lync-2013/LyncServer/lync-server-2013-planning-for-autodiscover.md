---
title: 'Lync Server 2013: planeamiento de la detección automática'
description: 'Lync Server 2013: planeamiento de la detección automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Autodiscover
ms:assetid: 51f1ff94-1d64-4e6d-a878-b86fa07edc2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945628(v=OCS.15)
ms:contentKeyID: 51541474
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e28a6a3a317f063151eadde7c5de51b02a46b482
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437080"
---
# <a name="planning-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="a4259-103">Planificación de la detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4259-103">Planning for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a4259-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a4259-104">

<span> </span></span></span>

<span data-ttu-id="a4259-105">_**Última modificación del tema:** 2013-02-16_</span><span class="sxs-lookup"><span data-stu-id="a4259-105">_**Topic Last Modified:** 2013-02-16_</span></span>

<span data-ttu-id="a4259-106">La detección automática se presentó en Lync Server en la actualización acumulativa para Lync Server 2010: noviembre de 2011.</span><span class="sxs-lookup"><span data-stu-id="a4259-106">Autodiscover was introduced for Lync Server in the Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="a4259-107">El principal objetivo de esta implementación inicial de la detección automática es proporcionar un medio para que Lync Mobile encuentre el servicio de movilidad (MCX).</span><span class="sxs-lookup"><span data-stu-id="a4259-107">The primary purpose for this initial implementation of Autodiscover was to provide a means for Lync Mobile to locate the Mobility service (Mcx).</span></span> <span data-ttu-id="a4259-108">El servicio de detección automática de Lync Server 2013 es un servicio usado por todos los clientes para ubicar servicios de servidor y de usuario.</span><span class="sxs-lookup"><span data-stu-id="a4259-108">The Autodiscover service in Lync Server 2013 is now a service used by all clients to locate server and user services.</span></span> <span data-ttu-id="a4259-109">El servicio de detección automática de Microsoft Lync Server 2013 se ejecuta en directores y servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="a4259-109">The Microsoft Lync Server 2013 Autodiscover service runs on Directors and Front End Servers.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="a4259-110">Para obtener más información técnica sobre la detección automática y sobre lo que se comunica a los clientes, consulte Descripción de la <A href="lync-server-2013-understanding-autodiscover.md">detección automática en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a4259-110">For a more technical understanding of Autodiscover and what is communicated to clients, see <A href="lync-server-2013-understanding-autodiscover.md">Understanding Autodiscover in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="a4259-111">La movilidad sigue siendo un escenario diferenciado y los servicios de movilidad aún requieren una planificación especial.</span><span class="sxs-lookup"><span data-stu-id="a4259-111">Mobility is still a distinct scenario and the Mobility services still require some special planning.</span></span> <span data-ttu-id="a4259-112">Para obtener más información, consulte <A href="lync-server-2013-planning-for-mobility.md">planificación de movilidad en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a4259-112">For additional details, see <A href="lync-server-2013-planning-for-mobility.md">Planning for mobility in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="a4259-113">Cuando se introdujo la detección automática en Lync Server 2010, había comprometeciones que era necesario realizar para implementar un servicio que requiriera posibles cambios de certificados en las implementaciones existentes de servidor.</span><span class="sxs-lookup"><span data-stu-id="a4259-113">When Autodiscover was introduced in Lync Server 2010, there were compromises that needed to be made in order to implement a service that required potential certificate changes to existing server deployments.</span></span> <span data-ttu-id="a4259-114">La detección automática podría usarse en el puerto TCP 443 para HTTPS o en el puerto TCP 80 para HTTP.</span><span class="sxs-lookup"><span data-stu-id="a4259-114">Autodiscover could be used over port TCP 443 for HTTPS or over port TCP 80 for HTTP.</span></span> <span data-ttu-id="a4259-115">Si se tomó la decisión de usar HTTPS, es necesario volver a emitir certificados en los servidores proxy inversos, directores y servidores de aplicaciones para el usuario para poder dar cabida a los `lyncdiscover.<domain>` registros necesarios y `lyncdiscoverinternal.<domain>` DNS.</span><span class="sxs-lookup"><span data-stu-id="a4259-115">If the decision was made to use HTTPS, certificates on reverse proxies, Directors, and Front End Servers needed to be reissued in order to accommodate the required `lyncdiscover.<domain>` and `lyncdiscoverinternal.<domain>` DNS records.</span></span> <span data-ttu-id="a4259-116">Si la decisión fue utilizar HTTP, la reemisión de certificados podría evitarse mediante el uso de registros CNAME (o alias) DNS para usar los nombres existentes en los certificados.</span><span class="sxs-lookup"><span data-stu-id="a4259-116">If the decision was to use HTTP, the reissue of certificates could be avoided by using DNS CNAME (or alias) records to use existing names on the certificates.</span></span> <span data-ttu-id="a4259-117">El uso de HTTP significa que las comunicaciones iniciales no estaban cifradas.</span><span class="sxs-lookup"><span data-stu-id="a4259-117">Using HTTP did mean that the initial communications were unencrypted.</span></span>

<span data-ttu-id="a4259-118">Puesto que Lync Server 2013 usa la detección automática para todos los clientes, el escenario principal es usar HTTPS de forma exclusiva y para crear certificados con lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="a4259-118">Because Lync Server 2013 uses Autodiscover for all clients, the main scenario is to use HTTPS exclusively and to create certificates with lyncdiscover.\<domain\></span></span> <span data-ttu-id="a4259-119">como parte de la configuración de servidores proxy inversos, directores y servidores de aplicaciones para el usuario.</span><span class="sxs-lookup"><span data-stu-id="a4259-119">as part of the configuration of reverse proxies, Directors and Front End Servers.</span></span> <span data-ttu-id="a4259-120">Si implementa la detección automática en una implementación actualizada de Lync Server 2010, es posible que desee usar HTTP para evitar la emisión de certificados.</span><span class="sxs-lookup"><span data-stu-id="a4259-120">If you are implementing Autodiscover into an upgraded deployment from Lync Server 2010, you may want to use HTTP to avoid reissuing certificates.</span></span> <span data-ttu-id="a4259-121">En las siguientes secciones se proporciona una guía para ambos escenarios.</span><span class="sxs-lookup"><span data-stu-id="a4259-121">Guidance for both scenarios is provided in the following sections.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a4259-122">La lista de nombres alternativos de asunto en certificados usados por la regla de publicación de servicios web externos debe contener un <EM>lyncdiscover. &lt; sipdomain &gt; </EM> entrada para cada dominio SIP de su organización.</span><span class="sxs-lookup"><span data-stu-id="a4259-122">The subject alternative name list on certificates used by the external web services publishing rule must contain a <EM>lyncdiscover.&lt;sipdomain&gt;</EM> entry for each SIP domain within your organization.</span></span> <span data-ttu-id="a4259-123">Para obtener información sobre las entradas de nombre alternativo de asunto necesarias para los directores, servidores de aplicaciones para el usuario y proxy inversos, consulte <A href="lync-server-2013-certificate-summary-autodiscover.md">Resumen del certificado: detección automática en Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a4259-123">For details about the subject alternative name entries that are required for Directors, Front End Servers, and reverse proxies, see <A href="lync-server-2013-certificate-summary-autodiscover.md">Certificate summary - Autodiscover in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a4259-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a4259-124">In This Section</span></span>

  - [<span data-ttu-id="a4259-125">Resumen del certificado: detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4259-125">Certificate summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-autodiscover.md)

  - [<span data-ttu-id="a4259-126">Resumen de puertos-detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4259-126">Port summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-port-summary-autodiscover.md)

  - [<span data-ttu-id="a4259-127">Resumen de DNS-detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4259-127">DNS summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-dns-summary-autodiscover.md)

  - [<span data-ttu-id="a4259-128">Híbrida y dividida en dominios: detección automática en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4259-128">Hybrid and split-domain - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-hybrid-and-split-domain-autodiscover.md)

<span data-ttu-id="a4259-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a4259-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

