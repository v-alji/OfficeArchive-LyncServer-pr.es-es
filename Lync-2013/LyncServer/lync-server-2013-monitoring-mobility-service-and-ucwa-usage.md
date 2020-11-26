---
title: 'Lync Server 2013: supervisar el servicio de movilidad y el uso de UCWA'
description: 'Lync Server 2013: supervisar el servicio de movilidad y el uso de UCWA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Mobility Service and UCWA usage
ms:assetid: 8389b37a-ca3e-4047-8b51-85bc07da87e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690025(v=OCS.15)
ms:contentKeyID: 48184683
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6575941faf904e46cd1f66d7226a16c88e8cbaa3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425398"
---
# <a name="monitoring-mobility-service-and-ucwa-usage-in-lync-server-2013"></a><span data-ttu-id="121af-103">Supervisar el uso del servicio de movilidad y de UCWA en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="121af-103">Monitoring Mobility Service and UCWA usage in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="121af-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="121af-104">

<span> </span></span></span>

<span data-ttu-id="121af-105">_**Última modificación del tema:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="121af-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="121af-106">De manera continua, debe supervisar la CPU y la memoria que usa el servicio de movilidad de Lync Server (MCX) y la API Web de comunicaciones unificadas (UCWA).</span><span class="sxs-lookup"><span data-stu-id="121af-106">On an ongoing basis, you should monitor the CPU and memory that is used by the Lync Server Mobility Service (Mcx) and the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="121af-107">Para supervisar el uso, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="121af-107">To monitor usage, you can use the following:</span></span>

<span data-ttu-id="121af-108">**Para la API web de comunicaciones unificadas (UCWA):**</span><span class="sxs-lookup"><span data-stu-id="121af-108">**For Unified Communications Web API (UCWA):**</span></span>

  - <span data-ttu-id="121af-109">El proceso de trabajo **LyncUcwa** en el administrador de Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="121af-109">The **LyncUcwa** worker process in Internet Information Services (IIS) Manager.</span></span> <span data-ttu-id="121af-110">En el panel **Procesos de trabajo**, mire las columnas **% de CPU** y **Bytes privados (KB)** (memoria).</span><span class="sxs-lookup"><span data-stu-id="121af-110">In the **Worker Processes** pane, look at the **CPU %** and **Private Bytes (KB)** (memory) columns.</span></span>

  - <span data-ttu-id="121af-111">Los contadores de rendimiento **CPU** y **Procesador**.</span><span class="sxs-lookup"><span data-stu-id="121af-111">The **CPU** and **Processor** performance counters.</span></span>

<span data-ttu-id="121af-112">Para la mayoría de las implementaciones, el uso de la CPU de UCWA tendría que estar por debajo del 15 % como promedio.</span><span class="sxs-lookup"><span data-stu-id="121af-112">For most deployments, UCWA CPU usage should be below 15 percent on average.</span></span> <span data-ttu-id="121af-113">El uso de memoria debe estar dentro de los límites descritos en [supervisión de los límites de capacidad de memoria del servidor en Lync server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span><span class="sxs-lookup"><span data-stu-id="121af-113">Memory usage should fall within the limits described in [Monitoring for server memory capacity limits in Lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span></span>

<span data-ttu-id="121af-114">Además de los contadores del uso de la CPU y de la memoria, puede usar los siguientes contadores de rendimiento para determinar cuándo un servidor está sobrecargado de solicitudes:</span><span class="sxs-lookup"><span data-stu-id="121af-114">In addition to CPU and memory usage counters, you can use the following performance counters to help determine when a server is overloaded with requests:</span></span>

  - <span data-ttu-id="121af-115">**LS: Web: limitación y autenticación \\ WEB: total de solicitudes en procesamiento**, que indica el número de solicitudes web pendientes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="121af-115">**LS:WEB – Throttling and Authentication\\WEB – Total Requests in Processing**, which indicates the number of pending web requests on the server.</span></span> <span data-ttu-id="121af-116">Cuando este contador alcanza las 10.000, las solicitudes posteriores provocarán el error “503 - Servicio no disponible”.</span><span class="sxs-lookup"><span data-stu-id="121af-116">When this counter reaches 10,000, subsequent requests will fail, with the error message, "503 - Service Unavailable."</span></span>

  - <span data-ttu-id="121af-117">**ASP.net \\ Solicitudes en cola** (siempre deben ser cero).</span><span class="sxs-lookup"><span data-stu-id="121af-117">**ASP.NET\\Requests Queued** (should always be zero).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="121af-118">Si cumple o supera estos valores, debe volver a visitar y calcular su plan de capacidad para la determinación correcta de la CPU, el número de núcleos y la memoria de los equipos que hospedan los servicios Web.</span><span class="sxs-lookup"><span data-stu-id="121af-118">If you meet or exceed these values, you should revisit and re-compute your capacity planning for the correct sizing of CPU, number of cores and memory for the computers hosting the Web services.</span></span>



</div>

<span data-ttu-id="121af-119">**Para el servicio de movilidad (Mcx):**</span><span class="sxs-lookup"><span data-stu-id="121af-119">**For the Mobility Service (Mcx):**</span></span>

  - <span data-ttu-id="121af-120">Los procesos de trabajo **CSIntMcxAppPool** y **CSExtMcxAppPool** en el administrador de Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="121af-120">The **CSIntMcxAppPool** and **CSExtMcxAppPool** worker processes in Internet Information Services (IIS) Manager.</span></span> <span data-ttu-id="121af-121">En el panel **Procesos de trabajo**, mire las columnas **% de CPU** y **Bytes privados (KB)** (memoria).</span><span class="sxs-lookup"><span data-stu-id="121af-121">In the **Worker Processes** pane, look at the **CPU %** and **Private Bytes (KB)** (memory) columns.</span></span>

  - <span data-ttu-id="121af-122">Los contadores de rendimiento **CPU** y **Procesador**.</span><span class="sxs-lookup"><span data-stu-id="121af-122">The **CPU** and **Processor** performance counters.</span></span>

<span data-ttu-id="121af-123">En la mayoría de las implementaciones, el uso de la CPU por parte del servicio Movilidad tendría que estar por debajo del 15 por ciento de media.</span><span class="sxs-lookup"><span data-stu-id="121af-123">For most deployments, Mobility Service CPU usage should be below 15 percent, on average.</span></span> <span data-ttu-id="121af-124">El uso de memoria debe estar dentro de los límites descritos en [supervisión de los límites de capacidad de memoria del servidor en Lync server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span><span class="sxs-lookup"><span data-stu-id="121af-124">Memory usage should fall within the limits described in [Monitoring for server memory capacity limits in Lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span></span>

<span data-ttu-id="121af-125">Además de los contadores del uso de la CPU y de la memoria, puede usar los siguientes contadores de rendimiento de ASP.NET para determinar cuándo un servidor está sobrecargado de solicitudes:</span><span class="sxs-lookup"><span data-stu-id="121af-125">In addition to CPU and memory usage counters, you can use the following ASP.NET performance counters to help determine when a server is overloaded with requests:</span></span>

  - <span data-ttu-id="121af-126">**ASP.net v 2.0.50727 \\ Requests Current**, que indica el número de solicitudes web pendientes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="121af-126">**ASP.NET v2.0.50727\\Requests Current**, which indicates the number of pending web requests on the server.</span></span> <span data-ttu-id="121af-127">Cuando este contador alcanza las 5.000, las solicitudes posteriores provocarán el error “503 - Servicio no disponible”.</span><span class="sxs-lookup"><span data-stu-id="121af-127">When this counter reaches 5,000, subsequent requests will fail with the error message, "503 - Service Unavailable."</span></span>

  - <span data-ttu-id="121af-128">**ASP.net \\ Solicitudes en cola** (siempre deben ser cero).</span><span class="sxs-lookup"><span data-stu-id="121af-128">**ASP.NET\\Requests Queued** (should always be zero).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="121af-129">Si cumple o supera estos valores, debe volver a revisar y recalcular su plan de capacidad para el tamaño correcto de la CPU, el número de núcleos y la memoria de los equipos que hospedan los servicios Web.</span><span class="sxs-lookup"><span data-stu-id="121af-129">If you meet or exceed these values, you should revisit and recompute your capacity planning for the correct sizing of CPU, number of cores, and memory for the computers hosting the Web services.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="121af-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="121af-130">See Also</span></span>


[<span data-ttu-id="121af-131">Supervisión de los límites de capacidad de memoria del servidor en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="121af-131">Monitoring for server memory capacity limits in Lync Server 2013</span></span>](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)  
  

<span data-ttu-id="121af-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="121af-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

