---
title: 'Lync Server 2013: configuración del servicio de movilidad para un alto rendimiento'
description: 'Lync Server 2013: configuración del servicio de movilidad para un alto rendimiento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Mobility Service for high performance
ms:assetid: c2b8aadb-cffb-49f0-ba7a-e8541a1ff475
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690042(v=OCS.15)
ms:contentKeyID: 48185332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4732d9f6a92c383a105a6f0d7162c9b6c798de24
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432887"
---
# <a name="configuring-mobility-service-for-high-performance-in-lync-server-2013"></a><span data-ttu-id="37299-103">Configurar el servicio de movilidad para un alto rendimiento en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37299-103">Configuring Mobility Service for high performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37299-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37299-104">

<span> </span></span></span>

<span data-ttu-id="37299-105">_**Última modificación del tema:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="37299-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="37299-106">Este tema se aplica solo al servicio de movilidad de Lync Server 2013 (MCX) y no se aplica a la API Web de comunicaciones unificadas (UCWA), tal como se proporciona en las actualizaciones acumulativas para Lync Server 2013: febrero de 2013.</span><span class="sxs-lookup"><span data-stu-id="37299-106">This topic applies only to the Lync Server 2013 Mobility Service (Mcx), and does not apply to Unified Communications Web API (UCWA), as delivered in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="37299-107">Al instalar el servicio de movilidad (MCX) en servicios de Internet Information Server (IIS) 7,5, el instalador del servicio de movilidad configura algunos valores de rendimiento en el servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="37299-107">When you install the Mobility Service (Mcx) on Internet Information Services (IIS) 7.5, the Mobility Service installer configures some performance settings on the Front End Server.</span></span> <span data-ttu-id="37299-108">Recomendamos usar IIS 7.5 para la movilidad.</span><span class="sxs-lookup"><span data-stu-id="37299-108">We recommend that you use IIS 7.5 for mobility.</span></span> <span data-ttu-id="37299-109">Los parámetros afectan al número máximo de solicitudes de usuario simultáneas y al número máximo de subprocesos permitidos para el servicio de movilidad.</span><span class="sxs-lookup"><span data-stu-id="37299-109">The settings affect the maximum number of concurrent user requests and the maximum number of threads that are allowed for the Mobility Service.</span></span>

<span data-ttu-id="37299-110">Estos son los parámetros de rendimiento:</span><span class="sxs-lookup"><span data-stu-id="37299-110">Here are the performance settings:</span></span>

<div>

## <a name="settings-for-mcx-on-iis-75"></a><span data-ttu-id="37299-111">Parámetros para Mcx en IIS 7.5</span><span class="sxs-lookup"><span data-stu-id="37299-111">Settings for Mcx on IIS 7.5</span></span>

1.  <span data-ttu-id="37299-112">**maxConcurrentThreadsPerCPU** está configurado en cero (0).</span><span class="sxs-lookup"><span data-stu-id="37299-112">**maxConcurrentThreadsPerCPU** is set to zero (0).</span></span>

2.  <span data-ttu-id="37299-113">**maxConcurrentRequestsPerCPU** está configurado en cero (0).</span><span class="sxs-lookup"><span data-stu-id="37299-113">**maxConcurrentRequestsPerCPU** is set to zero (0).</span></span>

3.  <span data-ttu-id="37299-114">El modelo del proceso ASP.NET está configurado en AutoConfig (solo para IIS 7.5).</span><span class="sxs-lookup"><span data-stu-id="37299-114">ASP.NET process model is set to AutoConfig (for IIS 7.5 only).</span></span>

4.  <span data-ttu-id="37299-115">El límite de cola HTTP.sys está configurado en 1.000 (de manera predeterminada).</span><span class="sxs-lookup"><span data-stu-id="37299-115">HTTP.sys queue limit is set to 1,000 (by default).</span></span>

<span data-ttu-id="37299-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37299-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

