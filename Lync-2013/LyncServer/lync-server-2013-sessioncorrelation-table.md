---
title: 'Lync Server 2013: Tabla SessionCorrelation'
description: 'Lync Server 2013: tabla SessionCorrelation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionCorrelation table
ms:assetid: 041705e1-7290-464f-95f8-96256cfa2e3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398091(v=OCS.15)
ms:contentKeyID: 48183267
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 814b7e8539d89f87e7df60ceb03e70800553fb55
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424082"
---
# <a name="sessioncorrelation-table-in-lync-server-2013"></a><span data-ttu-id="03cd6-103">Tabla SessionCorrelation en Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03cd6-103">SessionCorrelation table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03cd6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03cd6-104">

<span> </span></span></span>

<span data-ttu-id="03cd6-105">_**Última modificación del tema:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="03cd6-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="03cd6-106">La tabla SessionCorrelation es una tabla de soporte.</span><span class="sxs-lookup"><span data-stu-id="03cd6-106">The SessionCorrelation table is a supporting table.</span></span> <span data-ttu-id="03cd6-107">Cada registro representa un CorrelationID que se usa para correlacionar varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="03cd6-107">Each record represents one CorrelationID which is used to correlate multiple sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03cd6-108"><strong>Columna</strong></span><span class="sxs-lookup"><span data-stu-id="03cd6-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="03cd6-109"><strong>Tipo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="03cd6-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="03cd6-110"><strong>Clave o índice</strong></span><span class="sxs-lookup"><span data-stu-id="03cd6-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="03cd6-111"><strong>Detalles</strong></span><span class="sxs-lookup"><span data-stu-id="03cd6-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03cd6-112"><strong>Comprobación</strong></span><span class="sxs-lookup"><span data-stu-id="03cd6-112"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="03cd6-113">int</span><span class="sxs-lookup"><span data-stu-id="03cd6-113">int</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03cd6-114"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="03cd6-114"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="03cd6-115">int</span><span class="sxs-lookup"><span data-stu-id="03cd6-115">int</span></span></p></td>
<td><p><span data-ttu-id="03cd6-116">Primary</span><span class="sxs-lookup"><span data-stu-id="03cd6-116">Primary</span></span></p></td>
<td><p><span data-ttu-id="03cd6-117">Número único que identifica este servidor de conferencia A/V.</span><span class="sxs-lookup"><span data-stu-id="03cd6-117">Unique number identifying this A/V Conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03cd6-118"><strong>CorrelationID</strong></span><span class="sxs-lookup"><span data-stu-id="03cd6-118"><strong>CorrelationID</strong></span></span></p></td>
<td><p><span data-ttu-id="03cd6-119">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="03cd6-119">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="03cd6-120">Solo</span><span class="sxs-lookup"><span data-stu-id="03cd6-120">Unique</span></span></p></td>
<td><p><span data-ttu-id="03cd6-121">Las sesiones correlacionadas tendrán el mismo identificador de correlación.</span><span class="sxs-lookup"><span data-stu-id="03cd6-121">Sessions that are correlated will have the same correlation ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03cd6-122"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="03cd6-122"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="03cd6-123">datetime</span><span class="sxs-lookup"><span data-stu-id="03cd6-123">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="03cd6-124">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="03cd6-124">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="03cd6-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03cd6-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

