---
title: 'Lync Server 2013: Tabla CallPriorities'
description: 'Lync Server 2013: tabla CallPriorities.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CallPriorities table
ms:assetid: 043b63ae-2d64-4f38-a0df-18aa08d6caf5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398093(v=OCS.15)
ms:contentKeyID: 48183275
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe3cd1639921c63630e157744dbc8af22c50fac7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435645"
---
# <a name="callpriorities-table-in-lync-server-2013"></a><span data-ttu-id="295fe-103">Tabla CallPriorities en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="295fe-103">CallPriorities table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="295fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="295fe-104">

<span> </span></span></span>

<span data-ttu-id="295fe-105">_**Última modificación del tema:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="295fe-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="295fe-106">La tabla CallPriorities es una tabla estática que almacena la lista de posibles prioridades de llamadas, como ' Emergency ', ' urgente ' o ' normal '.</span><span class="sxs-lookup"><span data-stu-id="295fe-106">The CallPriorities table is a static table that stores the list of possible call priorities, such as ‘emergency’, ‘urgent’, or ‘normal’.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="295fe-107">Columna</span><span class="sxs-lookup"><span data-stu-id="295fe-107">Column</span></span></th>
<th><span data-ttu-id="295fe-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="295fe-108">Data Type</span></span></th>
<th><span data-ttu-id="295fe-109">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="295fe-109">Key/Index</span></span></th>
<th><span data-ttu-id="295fe-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="295fe-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="295fe-111"><strong>PriorityId</strong></span><span class="sxs-lookup"><span data-stu-id="295fe-111"><strong>PriorityId</strong></span></span></p></td>
<td><p><span data-ttu-id="295fe-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="295fe-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="295fe-113">Primary</span><span class="sxs-lookup"><span data-stu-id="295fe-113">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="295fe-114"><strong>Prioridad</strong></span><span class="sxs-lookup"><span data-stu-id="295fe-114"><strong>Priority</strong></span></span></p></td>
<td><p><span data-ttu-id="295fe-115">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="295fe-115">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="295fe-116">Valores permitidos:</span><span class="sxs-lookup"><span data-stu-id="295fe-116">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="295fe-117">0: desconocido</span><span class="sxs-lookup"><span data-stu-id="295fe-117">0 - Unknown</span></span></p></li>
<li><p><span data-ttu-id="295fe-118">1: no urgente</span><span class="sxs-lookup"><span data-stu-id="295fe-118">1 – Non-Urgent</span></span></p></li>
<li><p><span data-ttu-id="295fe-119">2-normal</span><span class="sxs-lookup"><span data-stu-id="295fe-119">2 - Normal</span></span></p></li>
<li><p><span data-ttu-id="295fe-120">3-urgente</span><span class="sxs-lookup"><span data-stu-id="295fe-120">3 - Urgent</span></span></p></li>
<li><p><span data-ttu-id="295fe-121">4-emergencia</span><span class="sxs-lookup"><span data-stu-id="295fe-121">4 - Emergency</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="295fe-122">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="295fe-122">


</div>

<span> </span>

</div>

</div>

</span></span></div>

