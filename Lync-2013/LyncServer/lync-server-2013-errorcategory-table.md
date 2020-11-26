---
title: 'Lync Server 2013: tabla ErrorCategory'
description: 'Lync Server 2013: tabla ErrorCategory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorCategory table
ms:assetid: 0fde3b73-9a2f-44dd-b8dc-6df512303ff1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204675(v=OCS.15)
ms:contentKeyID: 48183425
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8154c73f33b5dad62a338335a960553cfc06ec13
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428569"
---
# <a name="errorcategory-table-in-lync-server-2013"></a><span data-ttu-id="3fd46-103">Tabla ErrorCategory en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fd46-103">ErrorCategory table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fd46-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fd46-104">

<span> </span></span></span>

<span data-ttu-id="3fd46-105">_**Última modificación del tema:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="3fd46-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="3fd46-106">La tabla ErrorCategory contiene el nombre descriptivo de cada clasificación de diagnóstico de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3fd46-106">The ErrorCategory table contains the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span> <span data-ttu-id="3fd46-107">De forma predeterminada, Lync Server 2013 usa las siguientes clasificaciones:</span><span class="sxs-lookup"><span data-stu-id="3fd46-107">By default, Lync Server 2013 uses the following classifications:</span></span>

  - <span data-ttu-id="3fd46-108">0---correcto</span><span class="sxs-lookup"><span data-stu-id="3fd46-108">0 -- Success</span></span>

  - <span data-ttu-id="3fd46-109">1: error esperado</span><span class="sxs-lookup"><span data-stu-id="3fd46-109">1 -- Expected failure</span></span>

  - <span data-ttu-id="3fd46-110">2: error inesperado</span><span class="sxs-lookup"><span data-stu-id="3fd46-110">2 – Unexpected failure</span></span>

<span data-ttu-id="3fd46-111">Esta tabla se introdujo en Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3fd46-111">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3fd46-112">Columna</span><span class="sxs-lookup"><span data-stu-id="3fd46-112">Column</span></span></th>
<th><span data-ttu-id="3fd46-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3fd46-113">Data Type</span></span></th>
<th><span data-ttu-id="3fd46-114">Clave o índice</span><span class="sxs-lookup"><span data-stu-id="3fd46-114">Key/Index</span></span></th>
<th><span data-ttu-id="3fd46-115">Detalles</span><span class="sxs-lookup"><span data-stu-id="3fd46-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fd46-116"><strong>IdCategoría</strong></span><span class="sxs-lookup"><span data-stu-id="3fd46-116"><strong>CategoryId</strong></span></span></p></td>
<td><p><span data-ttu-id="3fd46-117">tinyint</span><span class="sxs-lookup"><span data-stu-id="3fd46-117">tinyint</span></span></p></td>
<td><p><span data-ttu-id="3fd46-118">Primary</span><span class="sxs-lookup"><span data-stu-id="3fd46-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="3fd46-119">Identificador único de la clasificación.</span><span class="sxs-lookup"><span data-stu-id="3fd46-119">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd46-120"><strong>Nombre.</strong></span><span class="sxs-lookup"><span data-stu-id="3fd46-120"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3fd46-121">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3fd46-121">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3fd46-122">Valor y nombre descriptivo asignados a la clasificación.</span><span class="sxs-lookup"><span data-stu-id="3fd46-122">Value and friendly name assigned to the classification.</span></span> <span data-ttu-id="3fd46-123">Los valores permitidos son:</span><span class="sxs-lookup"><span data-stu-id="3fd46-123">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3fd46-124">0---correcto</span><span class="sxs-lookup"><span data-stu-id="3fd46-124">0 -- Success</span></span></p></li>
<li><p><span data-ttu-id="3fd46-125">1: error esperado</span><span class="sxs-lookup"><span data-stu-id="3fd46-125">1 -- Expected failure</span></span></p></li>
<li><p><span data-ttu-id="3fd46-126">2: error inesperado</span><span class="sxs-lookup"><span data-stu-id="3fd46-126">2 – Unexpected failure</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="3fd46-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fd46-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

