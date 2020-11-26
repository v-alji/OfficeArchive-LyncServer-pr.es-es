---
title: 'Lync Server 2013: Compatibilidad de Active Directory'
description: Compatibilidad de Active Directory de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory support
ms:assetid: 28ed9ac4-586d-4803-ad45-99c4fa793f54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425756(v=OCS.15)
ms:contentKeyID: 48183679
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 349862b2f541ef3033c9a725a6ff04c6a4e219f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439411"
---
# <a name="active-directory-support-in-lync-server-2013"></a><span data-ttu-id="2f334-103">Compatibilidad de Active Directory en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f334-103">Active Directory support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f334-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f334-104">

<span> </span></span></span>

<span data-ttu-id="2f334-105">_**Última modificación del tema:** 2012-12-04_</span><span class="sxs-lookup"><span data-stu-id="2f334-105">_**Topic Last Modified:** 2012-12-04_</span></span>

<span data-ttu-id="2f334-106">Las topologías locales de los servicios de dominio de Active Directory que admite Lync Server 2013 son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="2f334-106">The Active Directory Domain Services on-premises topologies that are supported by Lync Server 2013 are as follows:</span></span>

  - <span data-ttu-id="2f334-107">Un solo bosque con un solo dominio</span><span class="sxs-lookup"><span data-stu-id="2f334-107">Single forest with single domain</span></span>

  - <span data-ttu-id="2f334-108">Un solo bosque con un solo árbol y varios dominios</span><span class="sxs-lookup"><span data-stu-id="2f334-108">Single forest with a single tree and multiple domains</span></span>

  - <span data-ttu-id="2f334-109">Un solo bosque con varios árboles y espacios de nombres separados</span><span class="sxs-lookup"><span data-stu-id="2f334-109">Single forest with multiple trees and disjoint namespaces</span></span>

  - <span data-ttu-id="2f334-110">Varios bosques en una topología de bosque central</span><span class="sxs-lookup"><span data-stu-id="2f334-110">Multiple forests in a central forest topology</span></span>

  - <span data-ttu-id="2f334-111">Varios bosques en una topología de bosque de recursos</span><span class="sxs-lookup"><span data-stu-id="2f334-111">Multiple forests in a resource forest topology</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2f334-112">Lync Server 2013 no admite dominios de etiqueta única.</span><span class="sxs-lookup"><span data-stu-id="2f334-112">Lync Server 2013 does not support single-label domains.</span></span> <span data-ttu-id="2f334-113">Por ejemplo, un bosque con un dominio raíz denominado <STRONG>contoso. local</STRONG> es compatible, pero no se admite un dominio raíz de una sola etiqueta denominado <STRONG>local</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="2f334-113">For example, a forest with a root domain named <STRONG>contoso.local</STRONG> is supported, but a single-label root domain named <STRONG>local</STRONG> is not supported.</span></span> <span data-ttu-id="2f334-114">Para obtener más información, consulte el artículo 300684 de Microsoft Knowledge base, "información sobre la configuración de Windows para dominios con nombres DNS de etiqueta única" en <A href="https://go.microsoft.com/fwlink/p/?linkid=143752">https://go.microsoft.com/fwlink/p/?linkId=143752</A> .</span><span class="sxs-lookup"><span data-stu-id="2f334-114">For details, see Microsoft Knowledge Base article 300684, "Information about configuring Windows for domains with single-label DNS names," at <A href="https://go.microsoft.com/fwlink/p/?linkid=143752">https://go.microsoft.com/fwlink/p/?linkId=143752</A>.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="2f334-115">Lync Server 2013 no permite cambiar el nombre de los dominios.</span><span class="sxs-lookup"><span data-stu-id="2f334-115">Lync Server 2013 does not support renaming domains.</span></span> <span data-ttu-id="2f334-116">Si necesita cambiar el nombre de un dominio donde se ha implementado Lync Server, primero debe desinstalar Lync Server, después cambiar el nombre del dominio y, a continuación, volver a instalar Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2f334-116">If you need to rename a domain where Lync Server is deployed, you need to first uninstall Lync Server, then rename the domain, and then reinstall Lync Server.</span></span>



</div>

<span data-ttu-id="2f334-117">Para obtener detalles sobre las topologías y los requisitos admitidos para implementaciones locales, consulte [requisitos, compatibilidad y topologías de los servicios de dominio de Active Directory en Lync Server 2013](lync-server-2013-active-directory-domain-services-requirements-support-and-topologies.md) en la documentación de planeación.</span><span class="sxs-lookup"><span data-stu-id="2f334-117">For details about supported topologies and requirements for on-premises deployments, see [Active Directory Domain Services requirements, support, and topologies in Lync Server 2013](lync-server-2013-active-directory-domain-services-requirements-support-and-topologies.md) in the Planning documentation.</span></span>

<span data-ttu-id="2f334-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f334-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

