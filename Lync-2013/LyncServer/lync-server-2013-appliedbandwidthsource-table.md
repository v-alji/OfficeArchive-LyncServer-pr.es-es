---
title: 'Lync Server 2013: Tabla AppliedBandwidthSource'
description: 'Lync Server 2013: tabla AppliedBandwidthSource.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppliedBandwidthSource table
ms:assetid: 24fb3caf-19b3-4c0a-90d7-ca5d53de32ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425725(v=OCS.15)
ms:contentKeyID: 48183638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3dc22d3a978a99cb13317e2a32fdb65382ce106c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440601"
---
# <a name="appliedbandwidthsource-table-in-lync-server-2013"></a><span data-ttu-id="d9b82-103">Tabla AppliedBandwidthSource en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9b82-103">AppliedBandwidthSource table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9b82-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9b82-104">

<span> </span></span></span>

<span data-ttu-id="d9b82-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="d9b82-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="d9b82-106">La tabla AppliedBandwidthSource es una tabla de soporte.</span><span class="sxs-lookup"><span data-stu-id="d9b82-106">The AppliedBandwidthSource table is a supporting table.</span></span> <span data-ttu-id="d9b82-107">Cada registro representa un origen.</span><span class="sxs-lookup"><span data-stu-id="d9b82-107">Each record represents one source.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9b82-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="d9b82-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="d9b82-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="d9b82-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="d9b82-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="d9b82-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="d9b82-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="d9b82-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9b82-112"><strong>AppliedBandwidthSourceKey</strong></span><span class="sxs-lookup"><span data-stu-id="d9b82-112"><strong>AppliedBandwidthSourceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="d9b82-113">int</span><span class="sxs-lookup"><span data-stu-id="d9b82-113">int</span></span></p></td>
<td><p><span data-ttu-id="d9b82-114">Primary</span><span class="sxs-lookup"><span data-stu-id="d9b82-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="d9b82-115">Número único que identifica el origen.</span><span class="sxs-lookup"><span data-stu-id="d9b82-115">Unique number identifying the source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9b82-116"><strong>AppliedBandwidthSource</strong></span><span class="sxs-lookup"><span data-stu-id="d9b82-116"><strong>AppliedBandwidthSource</strong></span></span></p></td>
<td><p><span data-ttu-id="d9b82-117">VARCHAR (256)</span><span class="sxs-lookup"><span data-stu-id="d9b82-117">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d9b82-118">Solo</span><span class="sxs-lookup"><span data-stu-id="d9b82-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="d9b82-119">Este es el origen del límite de ancho de banda que se impone.</span><span class="sxs-lookup"><span data-stu-id="d9b82-119">This is the source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="d9b82-120">Describe de dónde viene el límite de ancho de banda (por ejemplo, "servidor de directivas", "convertir servidor" o "modalidad de moda").</span><span class="sxs-lookup"><span data-stu-id="d9b82-120">It describes where the bandwidth limit is coming from (for example, “Policy Server”, “TURN Server”, or “Modality”).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d9b82-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9b82-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

