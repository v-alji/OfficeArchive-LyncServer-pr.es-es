---
title: 'Lync Server 2013: Tabla Endpoint'
description: 'Lync Server 2013: tabla de extremos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Endpoint table
ms:assetid: 500f330d-4d7d-4e88-b1cc-fef9a9de6b5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398327(v=OCS.15)
ms:contentKeyID: 48184098
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614872eee41b5d8e56da4b96cf5bbe3a4a1cf4d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428681"
---
# <a name="endpoint-table-in-lync-server-2013"></a><span data-ttu-id="be88a-103">Tabla Endpoint en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be88a-103">Endpoint table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be88a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be88a-104">

<span> </span></span></span>

<span data-ttu-id="be88a-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="be88a-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="be88a-106">La tabla de extremos es una tabla de soporte que almacena información sobre los puntos de conexión que participaron en sesiones registradas en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="be88a-106">The Endpoint table is a supporting table that stores information about the endpoints that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="be88a-107">Cada registro de la tabla representa un punto final.</span><span class="sxs-lookup"><span data-stu-id="be88a-107">Each record in the table represents one endpoint.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be88a-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="be88a-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="be88a-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="be88a-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be88a-112"><strong>EndpointKey</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-112"><strong>EndpointKey</strong></span></span></p></td>
<td><p><span data-ttu-id="be88a-113">int</span><span class="sxs-lookup"><span data-stu-id="be88a-113">int</span></span></p></td>
<td><p><span data-ttu-id="be88a-114">Primary</span><span class="sxs-lookup"><span data-stu-id="be88a-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="be88a-115">Número único que identifica este punto final.</span><span class="sxs-lookup"><span data-stu-id="be88a-115">Unique number identifying this endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be88a-116"><strong>Nombre.</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-116"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="be88a-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="be88a-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be88a-118">Solo</span><span class="sxs-lookup"><span data-stu-id="be88a-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="be88a-119">Nombre del extremo.</span><span class="sxs-lookup"><span data-stu-id="be88a-119">Endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be88a-120"><strong>Sistema operativo</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-120"><strong>OS</strong></span></span></p></td>
<td><p><span data-ttu-id="be88a-121">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be88a-121">nvarchar(128)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="be88a-122">Sistema operativo (SO) del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="be88a-122">Operating system (OS) of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be88a-123"><strong>CPUName</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-123"><strong>CPUName</strong></span></span></p></td>
<td><p><span data-ttu-id="be88a-124">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be88a-124">nvarchar(128)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be88a-125">Nombre de la CPU del extremo.</span><span class="sxs-lookup"><span data-stu-id="be88a-125">CPU name of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be88a-126"><strong>CPUNumberOfCores</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-126"><strong>CPUNumberOfCores</strong></span></span></p></td>
<td><p><span data-ttu-id="be88a-127">smallint</span><span class="sxs-lookup"><span data-stu-id="be88a-127">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be88a-128">Número de núcleos de CPU del extremo.</span><span class="sxs-lookup"><span data-stu-id="be88a-128">Number of CPU cores of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be88a-129"><strong>CPUProcessorSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-129"><strong>CPUProcessorSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="be88a-130">int</span><span class="sxs-lookup"><span data-stu-id="be88a-130">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be88a-131">Velocidad del procesador de la CPU del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="be88a-131">CPU processor speed of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be88a-132"><strong>VirtualizationFlag</strong></span><span class="sxs-lookup"><span data-stu-id="be88a-132"><strong>VirtualizationFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="be88a-133">tinyint</span><span class="sxs-lookup"><span data-stu-id="be88a-133">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be88a-134">Marcador de bits que indica si el sistema se está ejecutando en un entorno virtualizado:</span><span class="sxs-lookup"><span data-stu-id="be88a-134">Bit flag that indicates if the system is running in a virtualized environment:</span></span></p>
<ul>
<li><p><span data-ttu-id="be88a-135">0x0000: ninguna</span><span class="sxs-lookup"><span data-stu-id="be88a-135">0x0000 – None</span></span></p></li>
<li><p><span data-ttu-id="be88a-136">0x0001: HyperV</span><span class="sxs-lookup"><span data-stu-id="be88a-136">0x0001 – HyperV</span></span></p></li>
<li><p><span data-ttu-id="be88a-137">0x0002: VMWare</span><span class="sxs-lookup"><span data-stu-id="be88a-137">0x0002 – VMWare</span></span></p></li>
<li><p><span data-ttu-id="be88a-138">0x0004: Virtual PC</span><span class="sxs-lookup"><span data-stu-id="be88a-138">0x0004 – Virtual PC</span></span></p></li>
<li><p><span data-ttu-id="be88a-139">0x0008: Xen PC</span><span class="sxs-lookup"><span data-stu-id="be88a-139">0x0008 – Xen PC</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="be88a-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be88a-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

